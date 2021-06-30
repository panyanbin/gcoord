# gcoord



## 坐标系

地球上某个点，在不同的坐标系中其经纬度有所不同。目前中国国内常见的坐标系主要分为3种：

1. 地球坐标系——`WGS84`：目前广泛使用的坐标系，也是作为国际标准的坐标体系，常见于**GPS设备**，**谷歌地图**、**Bing地图**等。
2. 火星坐标系——`GCJ-02`：由中国国家测绘局制订的地理信息系统的坐标系统，是基于`WGS84`坐标系加密后的坐标系。国内的**高德地图**、**腾讯地图**、**谷歌中国**就是使用这种坐标系。
3. 百度坐标系——`BD-09`：这是百度基于火星坐标系的基础上又进行一次加密处理，**百度地图**就是使用这种坐标系。

> 若是不使用匹配的坐标系会导致展现出的点有少许位置偏移，因此需要把点的经纬度转换为地图对应的坐标系才可以显示正常。





## 坐标系转换

我把网上搜集到的坐标系转换[工具函数](./utils/geoTransform.js)放到仓库内，主要有`BD-09`与`GCJ-02`互转、`GCJ-02`与`WGS84`互转；也在GitHub上找到一个对地理坐标系转换工具的库：https://github.com/hujiulong/gcoord，可以自行选择。

收集了一个可视化的转换工具网页：https://tool.lu/coordinate/，可以进入该页面可视化查看`BD-09`、`GCJ-02`、`WGS84`多个转换结果。

如果想校验转换后经纬度是否正确，可以进入[百度拾取坐标系统](https://api.map.baidu.com/lbsapi/getpoint/index.html)，在系统中对百度坐标系的经纬度或经过工具转换后得到的百度坐标系的经纬度进行“坐标反查”搜索，然后看位置是否正确。



## 中国行政区GeoJSON数据

我把阿里网站维护的中国行政区划分数据下载到本仓库的map目录下，若想查看最新的数据可以进入到[这里](https://datav.aliyun.com/tools/atlas/)。

其中，带`full`表示包含子区域，即带更细致的子区域划分。

[中国_100000.json](./map/中国_100000.json)
[中国_100000_full.json](./map/中国_100000_full.json)

[上海市_310000.json](./map/上海市_310000.json)
[上海市_310000_full.json](./map/上海市_310000_full.json)
[云南省_530000.json](./map/云南省_530000.json)
[云南省_530000_full.json](./map/云南省_530000_full.json)
[内蒙古自治区_150000.json](./map/内蒙古自治区_150000.json)
[内蒙古自治区_150000_full.json](./map/内蒙古自治区_150000_full.json)    
[北京市_110000.json](./map/北京市_110000.json)
[北京市_110000_full.json](./map/北京市_110000_full.json)
[台湾省_710000.json](./map/台湾省_710000.json)
[台湾省_710000_full.json](./map/台湾省_710000_full.json)
[吉林省_220000.json](./map/吉林省_220000.json)
[吉林省_220000_full.json](./map/吉林省_220000_full.json)
[四川省_510000.json](./map/四川省_510000.json)
[四川省_510000_full.json](./map/四川省_510000_full.json)
[天津市_120000.json](./map/天津市_120000.json)
[天津市_120000_full.json](./map/天津市_120000_full.json)
[宁夏回族自治区_640000.json](./map/宁夏回族自治区_640000.json)
[宁夏回族自治区_640000_full.json](./map/宁夏回族自治区_640000_full.json)
[安徽省_340000.json](./map/安徽省_340000.json)
[安徽省_340000_full.json](./map/安徽省_340000_full.json)
[山东省_370000.json](./map/山东省_370000.json)
[山东省_370000_full.json](./map/山东省_370000_full.json)
[山西省_140000.json](./map/山西省_140000.json)
[山西省_140000_full.json](./map/山西省_140000_full.json)
[广东省_440000.json](./map/广东省_440000.json)
[广东省_440000_full.json](./map/广东省_440000_full.json)
[广西壮族自治区_450000.json](./map/广西壮族自治区_450000.json)
[广西壮族自治区_450000_full.json](./map/广西壮族自治区_450000_full.json)
[新疆维吾尔自治区_650000.json](./map/新疆维吾尔自治区_650000.json)
[新疆维吾尔自治区_650000_full.json](./map/新疆维吾尔自治区_650000_full.json)
[江苏省_320000.json](./map/江苏省_320000.json)
[江苏省_320000_full.json](./map/江苏省_320000_full.json)
[江西省_360000.json](./map/江西省_360000.json)
[江西省_360000_full.json](./map/江西省_360000_full.json)
[河北省_130000.json](./map/河北省_130000.json)
[河北省_130000_full.json](./map/河北省_130000_full.json)
[河南省_410000.json](./map/河南省_410000.json)
[河南省_410000_full.json](./map/河南省_410000_full.json)
[浙江省_330000.json](./map/浙江省_330000.json)
[浙江省_330000_full.json](./map/浙江省_330000_full.json)
[海南省_460000.json](./map/海南省_460000.json)
[海南省_460000_full.json](./map/海南省_460000_full.json)
[湖北省_420000.json](./map/湖北省_420000.json)
[湖北省_420000_full.json](./map/湖北省_420000_full.json)
[湖南省_430000.json](./map/湖南省_430000.json)
[湖南省_430000_full.json](./map/湖南省_430000_full.json)
[甘肃省_620000.json](./map/甘肃省_620000.json)
[甘肃省_620000_full.json](./map/甘肃省_620000_full.json)
[福建省_350000.json](./map/福建省_350000.json)
[福建省_350000_full.json](./map/福建省_350000_full.json)
[西藏自治区_540000.json](./map/西藏自治区_540000.json)
[西藏自治区_540000_full.json](./map/西藏自治区_540000_full.json)
[贵州省_520000.json](./map/贵州省_520000.json)
[贵州省_520000_full.json](./map/贵州省_520000_full.json)
[辽宁省_210000.json](./map/辽宁省_210000.json)
[辽宁省_210000_full.json](./map/辽宁省_210000_full.json)
[重庆市_500000.json](./map/重庆市_500000.json)
[重庆市_500000_full.json](./map/重庆市_500000_full.json)
[陕西省_610000.json](./map/陕西省_610000.json)
[陕西省_610000_full.json](./map/陕西省_610000_full.json)
[青海省_630000.json](./map/青海省_630000.json)
[青海省_630000_full.json](./map/青海省_630000_full.json)
[黑龙江省_230000.json](./map/黑龙江省_230000.json)
[黑龙江省_230000_full.json](./map/黑龙江省_230000_full.json)

> 注意：以上geojson对象中的经纬度坐标系信息均为`WGS84`。



## GeoJSON数据的查看

若已有GeoJSON数据，想看具体表示的区域划分可以进入GeoJSON官网：http://geojson.io/。可以在线查看，绘制和修改GeoJSON数据。





## 相关网址总结

| URL                                                  | 说明                                         |
| ---------------------------------------------------- | -------------------------------------------- |
| https://tool.lu/coordinate/                          | 转换多个坐标系经纬度的可视化界面             |
| https://api.map.baidu.com/lbsapi/getpoint/index.html | 百度拾取坐标系统，根据百度坐标系经纬度定位点 |
| http://datav.aliyun.com/tools/atlas/                 | 中国行政区划数据维护网站                     |
| http://geojson.io/                                   | 可在线查看，绘制，修改GeoJSON数据            |

