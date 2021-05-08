BP登录耗时比较图
```
.es(index="jzjybp-*",q='"L0409101"',metric='avg:bptime',offset=-7d).label(登录7天前).color(green).yaxis(2), .es(index="jzjybp-*",q='"L0409101"',metric='avg:bptime').label(登录--耗时).color(blue).yaxis(2),   .es(index="jzjybp-*",q='L0409101',metric='max:bptime').label(登录-MAX).points().color(red).yaxis(1)
```

BP委托耗时比较图
```
.es(index="jzjybp-*",q='"L0303001"',metric='avg:bptime',offset=-7d).label(委托7天前).color(green).yaxis(2), .es(index="jzjybp-*",q='"L0303001"',metric='avg:bptime').label(委托--耗时).color(blue).yaxis(2),  .es(index="jzjybp-*",q='L0303001',metric='max:bptime').label(委托-MAX).points().color(red).yaxis(1)
```

集中交易BP登录耗时
```
.es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:rcjzbp-007004B',metric='avg:bptime').label(rc0704).color(Olive).yaxis(2),  .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:rcjzbp-007005B',metric='avg:bptime').label(rc0705).color(Teal).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:rcjzbp-007006B',metric='avg:bptime').label(rc0706).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:rcjzbp-007007B',metric='avg:bptime').label(rc0707).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:rcjzbp-007008B',metric='avg:bptime').label(rc0708).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:rcjzbp-007009B',metric='avg:bptime').label(rc0709).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:fgjzbp-017004B',metric='avg:bptime').label(fg1704).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:fgjzbp-017005B',metric='avg:bptime').label(fg1705).yaxis(2),  .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:fgjzbp-017006B',metric='avg:bptime').label(fg1706).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:fgjzbp-017007B',metric='avg:bptime').label(fg1707).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:fgjzbp-017008B',metric='avg:bptime').label(fg1708).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:fgjzbp-017009B',metric='avg:bptime').label(fg1709).yaxis(2), .es(index="jzjybp-*",q='(L0109101 OR L0409101) AND SOURCE_HOST.keyword:fgjzbp-017014B',metric='avg:bptime').label(fg1714).yaxis(2)
```

集中交易BP委托耗时
```
.es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:rcjzbp-007004B',metric='avg:bptime').label(rc0704).color(Olive).yaxis(2),  .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:rcjzbp-007005B',metric='avg:bptime').label(rc0705).color(Teal).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:rcjzbp-007006B',metric='avg:bptime').label(rc0706).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:rcjzbp-007007B',metric='avg:bptime').label(rc0707).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:rcjzbp-007008B',metric='avg:bptime').label(rc0708).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:rcjzbp-007009B',metric='avg:bptime').label(rc0709).yaxis(2),  .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:fgjzbp-017004B',metric='avg:bptime').label(fg1704).yaxis(2),  .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:fgjzbp-017005B',metric='avg:bptime').label(fg1705).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:fgjzbp-017006B',metric='avg:bptime').label(fg1706).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:fgjzbp-017007B',metric='avg:bptime').label(fg1707).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:fgjzbp-017008B',metric='avg:bptime').label(fg1708).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:fgjzbp-017009B',metric='avg:bptime').label(fg1709).yaxis(2), .es(index="jzjybp-*",q='"L0303001" AND SOURCE_HOST.keyword:fgjzbp-017014B',metric='avg:bptime').label(fg1714).yaxis(2)
```

BP撤单耗时比较图
```
.es(index="jzjybp-*",q='"L0303002"',metric='avg:bptime',offset=-7d).label(撤单7天前).color(green).yaxis(2), .es(index="jzjybp-*",q='"L0303002"',metric='avg:bptime').label(撤单--耗时).color(blue).yaxis(2),   .es(index="jzjybp-*",q='L0303002',metric='max:bptime').label(撤单-MAX).points().color(red).yaxis(1)
```

BP登录耗时比较图-两融
```
.es(index="rzrqbp-*",q='"L0109101"',metric='avg:bptime',offset=-7d).label(登录7天前).color(green).yaxis(2), .es(index="rzrqbp-*",q='"L0109101"',metric='avg:bptime').label(登录--耗时).color(blue).yaxis(2),  .es(index="rzrqbp-*",q='L0109101',metric='max:bptime').label(登录--MAX).points().color(red).yaxis(1)
```




