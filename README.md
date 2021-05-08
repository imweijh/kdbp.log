# logstash处理金证BP日志

BP日志公司已统一采集放在kafka，和公司kafka版本能匹配的logstash最高版本是v2.4.1，估采用两级logstash模式：
- 第一级由三台机器四个logstash v2.4.1实例从kafka读取，处理，存入redis；
- 第二级由logstash v5.x从redis取出存入elasticsearch。


