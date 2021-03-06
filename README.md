# getmap
给定矩形区域的左上角和右下角的经纬度坐标，下载网络地图（路网图或卫星图）。

目前有两个分支，Python3版和Golang版，若不需要坐标点的输出，请选择速度更快的[golang版本](https://github.com/yuansushow/getmap/releases)。

目前支持的地图有：
- 谷歌 
- 高德 
- 腾讯


## 2017.09.07更新
1. 把协程改为多线程实现，增加兼容，减少复杂性，不需要过高的python版本。
2. 增加GCJ的纠偏功能
3. 增加链接文件的输出，可用于arcgis的地理配准。输出文件可选择原样输出，或gcj02转wgs84，以及wgs84转gcj02。

## 2018.04.12更新

增加了Golang的版本。(golang版本暂时没有输出坐标功能)  <br>
增加了Golang编译好的可执行版本->[Releases](https://github.com/yuansushow/getmap/releases)。
```
>getmap -h
Usage of getmap:
  -f string
        输出文件名称（以.jpg结尾） (default "OUT[0412_211623].jpg")
  -m string
        s - 卫星图   m - 路网图 (default "s")
  -n int
        下载线程数 (default 10)
  -p1 string
        第一个对角点的经纬度，如 104.08028,30.67101 逗号前后不要加空格
  -p2 string
        第二个对角点的经纬度，如 104.08028,30.67101 逗号前后不要加空格
  -s string
        地图源(目前仅支持 google/amap/tencent) (default "google")
  -z int
        缩放级别，级别越大图幅越清晰。请取[1,19] (default 2)
```
