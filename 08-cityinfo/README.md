# city.py

利用高德地图api查询城市信息

## 获取高德地图API_KEY

```
API_KEY ＝ 'YOUR_API_KEY'
```

## 用法

```
usage: city.py [-h] [-k KEYWORD] {info,place,bus} ...

城市信息查询.

optional arguments:
  -h, --help            show this help message and exit
  -k KEYWORD, --keyword KEYWORD
                        关键词

操作命令:
  {info,place,bus}
    info                查询城市简介
    place               查询城市信息
    bus                 查询公交信息
```

### 查询城市简介

```
usage: city.py info [-h] [city]

查询城市简介

positional arguments:
  city        查询城市（默认为ip所在城市）
```

```
python city.py info 珠海
```

输出

```
珠海，珠江口西岸的核心城市，经济特区，珠江三角洲南端的一个重要城市，位于广东省珠江口的西南部，区位优越，东与香港隔海相望，南与澳门相连，西邻新会、台山市，北与中山市接壤。设有拱北、九洲、珠海港、万山、横琴、斗门、湾仔、珠澳跨境工业区等8个国家一类口岸，是珠三角中海洋面积最大、岛屿最多、海岸线最长的城市，素有“百岛之市”之称。珠海生态环境优美，山水相间，陆岛相望，气候宜人，是全国唯一以整体城市景观入选“全国旅游胜地四十佳”的城市。人居环境一流。珠海是中国最早实行对外开放政策的四个经济特区之一，陆地面积有1701平方千米，户籍人口106.01万（2011年末），是广东省人口规模最小的地级市。2013中国城市可持续发展指数报告珠海综合排名全国第一，珠海为中国新兴城市50强，新型花园城市；珠海属国家新颁布的“幸福之城”，有“浪漫之城”的称号。
```

### 查询城市信息

```
usage: city.py place [-h] keyword [city]

查询城市信息

positional arguments:
  keyword     查询的关键词
  city        查询城市（默认为ip所在城市）
```

```
python city.py place 肯德基
```

输出

```
+-------------------------+-------------------------------------------------------+--------------------------------------+
|           名称          |                          地址                         |                 电话                 |
+-------------------------+-------------------------------------------------------+--------------------------------------+
|    肯德基(人民西路店)   |             人民西路仁恒星园商业街一层商铺            |             0756-2608108             |
|      肯德基(三灶店)     |                    映月路65-67号1层                   |  4008823823;0756-7511166;4009200715  |
|   肯德基(拱北汽车站店)  |                    友谊路20号1、2层                   |       0756-8887871;4009200715        |
|      肯德基(迎宾店)     |             迎宾南路1126号迎宾百货广场2层             |              4008823823              |
|      肯德基(吉大店)     |                景山路220号珠海免税商场                |       0756-3374325;13680023140       |
|      肯德基(明珠店)     |             明珠南路1389号明珠商业广场1层             |       0756-8629257;4009200715        |
|      肯德基(井岸店)     |                 井岸镇新民路18-22号1层                | 0756-5559659;0756-5111163;4009200715 |
|    肯德基(时代广场店)   |                人民西路808号华润万佳1层               |       0756-2651502;4008823823        |
|    肯德基(凤凰南路店)   |                     凤凰南路1128号                    |       0756-2115782;4009200715        |
|      肯德基(柠溪店)     |                  柠溪路284号文化广场                  |       0756-2625733;4008823823        |
|      肯德基(夏湾店)     |                   夏湾路夏湾市场1层                   | 0756-8882821;0756-8884008;4009200715 |
|      肯德基(朝福店)     |                 井岸步行街新民路144号                 |             0756-5111163             |
|      肯德基(南坑店)     |                 市场集团南坑商贸楼1层                 |       0756-2169018;4009208801        |
|     肯德基(南屏路店)    |           南屏镇环屏路1号华夏国际商务酒店2层          |             0756-8911006             |
|      肯德基(前山店)     |          前山路前山市场A圈一二层(近得一超市)          |             0756-8986233             |
|     肯德基(九洲港店)    |             情侣路599号九洲港客运大楼一层             |             0756-3262230             |
|      肯德基(紫荆店)     |               紫荆路301号至尊宝大厦1-2层              | 0756-2127203;0756-2127662;4008823823 |
|      肯德基(口岸店)     |                      口岸广场B1层                     |             0756-8307613             |
|     肯德基(山场路店)    |                  山场路1号五洲花城1层                 |  0756-2535337;4008823823;4009200715  |
|      肯德基(侨光店)     |               拱北侨光路37号国泰酒店一层              |             0756-8889017             |
| 肯德基(珠海机场店kfc店) | 三灶镇海澄机场候机大楼主楼(中指廊)二楼出发大厅SD025号 |       0756-7680932;4009200715        |
|    肯德基(华发商都店)   |       珠海大道8号华发商都2号楼1层A1028、A1029号       |      0756-8921086;0756-8921085       |
+-------------------------+-------------------------------------------------------+--------------------------------------+
```

### 查询巴士信息

```
usage: city.py bus [-h] start end [city]

查询公交信息

positional arguments:
  start       出发地
  end         目的地
  city        查询城市
```

```
python city.py bus 唐家市场 圆明新园
```

输出

```
+-----------------------------------+----------+----------+----------+--------+--------+----------+-----------+
|                路线               |  上车站  |  下车站  | 途径站数 | 首班车 | 末班车 | 预计时间 |  步行距离 |
+-----------------------------------+----------+----------+----------+--------+--------+----------+-----------+
|               方案1               |          |          |          |        |        |          | 0.844公里 |
|    69路(城轨唐家湾站--圆明新园)   | 唐家市场 | 圆明新园 |    28    | 06:05  | 22:20  |  48分钟  |           |
|                                   |          |          |          |        |        |          |           |
|               方案2               |          |          |          |        |        |          | 0.861公里 |
|  K3路(城轨唐家湾站--拱北口岸总站) | 唐家市场 |  九洲城  |    6     | 06:05  | 20:50  |  29分钟  |           |
|             ---换乘---            |          |          |          |        |        |          |           |
|      25路(九洲港--屏北三路西)     |  九洲城  | 圆明新园 |    5     | 06:15  | 23:10  |  20分钟  |           |
|     40路(吉大总站--上冲检查站)    |  九洲城  | 圆明新园 |    5     | 06:15  | 23:30  |  20分钟  |           |
|        60路(吉大总站--湾仔)       |  九洲城  | 圆明新园 |    8     | 06:20  | 22:20  |  24分钟  |           |
|                                   |          |          |          |        |        |          |           |
|               方案3               |          |          |          |        |        |          | 0.949公里 |
|  K1路(城轨珠海北站--拱北口岸总站) | 唐家市场 | 摩尔广场 |    8     | 06:05  | 21:15  |  34分钟  |           |
|             ---换乘---            |          |          |          |        |        |          |           |
|       1路(城轨珠海站--香洲)       | 摩尔广场 | 圆明新园 |    1     | 06:20  | 01:15  |  15分钟  |           |
|     62路(横琴口岸西--圆明新园)    | 摩尔广场 | 圆明新园 |    2     | 07:20  | 20:30  |  16分钟  |           |
|                                   |          |          |          |        |        |          |           |
|               方案4               |          |          |          |        |        |          | 0.872公里 |
|  K3路(城轨唐家湾站--拱北口岸总站) | 唐家市场 |   吉大   |    7     | 06:05  | 20:50  |  30分钟  |           |
|             ---换乘---            |          |          |          |        |        |          |           |
|   992路(光大国贸--锦绣国际花城)   |   吉大   | 圆明新园 |    3     | 06:25  | 21:00  |  18分钟  |           |
|                                   |          |          |          |        |        |          |           |
|               方案5               |          |          |          |        |        |          | 2.067公里 |
|  K1路(城轨珠海北站--拱北口岸总站) | 唐家市场 |  隧道南  |    7     | 06:05  | 21:15  |  33分钟  |           |
| 10A路(城轨唐家湾站--拱北口岸总站) | 唐家市场 |  隧道南  |    18    | 06:15  | 22:05  |  38分钟  |           |
|  10F路(金鼎工业园北--城轨珠海站)  | 唐家市场 |  隧道南  |    21    | 06:10  | 21:50  |  39分钟  |           |
|    10路(下栅检查站--城轨珠海站)   | 唐家市场 |  隧道南  |    21    | 06:05  | 22:00  |  39分钟  |           |
|             ---换乘---            |          |          |          |        |        |          |           |
|                                   |          |          |          |        |        |          |           |
+-----------------------------------+----------+----------+----------+--------+--------+----------+-----------+
```
