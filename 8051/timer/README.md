# 定时器程序说明

额外的指令周期数：2+2+2+2+1+1+1+2+...+ = 34

1ms = 1000us

计数次数X  + 34 = 期望周期数

* 频率为12MHz时：
指令周期：1.0000us

1000us / 1.00000 = 1000  （期望周期数）

即需要1000次计数来表示1ms
```
X  + 34 = 1000
X = 1000 - 34
      = 966
      = 03C6H
FFFFH - 03C6H = FC39H  (THx & TLx)
```


* 频率为11.0592MHz时：

指令周期：1.0403us

1000us / 1.0403 = 961  （期望周期数）

即需要961次计数来表示1ms

```
X  + 34 = 961
X = 961 - 34
      = 927
      = 039FH
FFFFH - 039FH = FC60H  (THx & TLx)
```