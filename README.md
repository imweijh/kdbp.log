# logstash处理金证BP日志
给柜台系统安装个X光机，看清系统内部运行细节，快速回答柜台系统以下问题：
- 哪些功能号调用最多；
- 登录、委托平均耗时多少，最大耗时多少
- 哪些BP处理的快哪些慢
- 哪些BP承载业务多

BP日志公司已统一采集放在kafka，和公司kafka版本能匹配的logstash最高版本是v2.4.1，采用两级logstash模式：
- 第一级由三台机器四个logstash v2.4.1实例从kafka读取-处理-存入redis；
- 第二级由一个logstash v5.x 从redis 取出存入elasticsearch v5.x 和 udp给另外一台机器


一共三台机器
>-  三台共运行四个logstash v2.4.1，根据机器配置和kafka分区数量，调整工作线程参数
>-  其中一台运行logstash v5.x 和 redis
>-  每台都运行一个elasticsearch v5.x实例，组成集群
```
cd /root/logstash-2.4.1A && nohup bin/logstash -f logstash2.4.1-A.conf -w 8 -b 600 &
cd /root/logstash-2.4.1B && nohup bin/logstash -f logstash2.4.1-B.conf -w 4 -b 300 &
cd /root/logstash-2.4.1C && nohup bin/logstash -f logstash2.4.1-C.conf -w 4 -b 300 &
cd /root/logstash-2.4.1D && nohup bin/logstash -f logstash2.4.1-D.conf -w 4 -b 300 &
```

监控kafka lag
```
watch -n 30 "bin/kafka-run-class.sh kafka.tools.ConsumerOffsetChecker --zkconnect kafka17:2181 --group logstash 2>&1"
```

redis配置和监控
```
# redis
echo never > /sys/kernel/mm/transparent_hugepage/enabled

watch "redis-cli -p 7379 -n 0 LLEN logstash"
watch "redis-cli -p 7379 -n 1 LLEN logstash"
```


![image](https://user-images.githubusercontent.com/23710675/117533269-7302c180-b01e-11eb-86de-eff4b1eafa3a.png)

