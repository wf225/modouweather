魔豆天气
=============
![](https://github.com/wf225/modou/blob/master/screenshot.png)

为魔豆路由器量身定做的天气预报 app。

## 下载 & 安装 ##
* 详见地址：http://bbs.modouwifi.cn/thread-11459-1-1.html。

## 更新历史 ##

>【0.8.3】2015-5-20
* 1.修改定时机制不起作用的bug
* 2.修改manifest.json文件开始处有两个不可见字符的问题
* 3.加上启动时的转菊花效果

>【0.8.2】2015-3-15
* 1 支持OP。同时提供 SDK 版本的更新，下载请留意文件后缀名。系统版本是 1.3.06 的，请下载 _op 后缀名文件。
* 2 支持路由宝使用城市名称配置。（支持城市列表详见）
* 3 此版本使用雅虎数据源。提供：三天预报，实时天气，空气质量 pm2.5，日出日落时间。
* 4 修正了图标无法显示问题。
* 5 添加了web 配置功能。

>【0.7.1】2015-1-22
* 无需手动设置自动更新，程序启动后自动每30分钟更新一次。

>【0.7.0】2015-1-20
* 1 支持自动更新. (此版本需手动配置，参考这里 )
* a.修改/data/conf/cron.d/matrix文件加入以下代码，代表每30分钟更新一次
* */30 * * * * /data/apps/91350939/modouweather.sh download >/dev/null （注：黄色字体换成自己的路径。强烈更新频率建议大于等于30分钟，因为服务器端数据是30分钟更新一次，客户端刷新太频繁也没用！）
* b. 执行crontab进程PID脚本，使配置项生效  /system/sbin/crond.sh restart
* 2 修复关闭按钮会打开其他应用的问题。
* 3 AQI支持城市增加到369个，戳这里看 空气质量排行榜。

>【0.6.0】2014-12-27
* 1 客户端加入"霾"的图标
* 2 加入空气质量AQI 显示，实施了新《环境空气质量标准》的城市列表，即有 PM2.5数据的城市列表。

>【0.5.5】2014-12-24
* 修复运行时间久了会闪屏的问题。

>【0.5.4】2014-11-27
* 修复在正式版固件 app 无法启的问题。

>【0.5.3】2014-11-26
* 1 修复长时间开启天气，app 无法退出、白屏的问题。
* 2 解决开机黑屏的问题，默认设置为“开机不自启动”。

>【0.5.2】2014-11-16
* 1 改用中国天气网数据源，更权威。优化界面显示，加入天气指数，当前温度、湿度、风速等，方便出行。
* 2 注：此版本不再支持IP自动获取天气功能，支持在路由宝上配置。
* 3 关于城市代码，参见http://www.cnblogs.com/wf225/p/4090737.html。
* 4 手工配置(针对没有Android的童鞋)：找到 天气安装目录下 conf/data.json 文件，把 city_id 的 value 改为你想要的城市代码。
* 5 固件版本要求: 0.7.06 及更新版本

>【0.4.0】2014-09-27
* 更名为“天气时钟。-加入时钟动态显示。
* 和之前版本一样，支持IP自动获取天气，和手工指定城市名称。【0.3.2】2014-08-31
* 增加了天气指数: PM2.5，穿衣，洗车，紫外线。 注：此版本只更了新服务器端，客户端无需升级！

>【0.3.1】2014-08-27
* 修复了新固件(0.6.21)无法安装的问题【0.30】2014-08-17
* 解决了断网不能使用的问题。断网重启后，会显示上次查询结果。
* 优化显示速度，0 秒等待（安装后第一次启动除外），3秒左右（根据时间网速）完成更新。
* 优化默认主题。

>【0.21】2014-08-12
* 解决了 0.1 版本中安装脚本没有被执行的问题。非常感谢魔豆团队所有人员的大力支持！谢谢技术大牛军建！
* 支持 IP 自动获取天气。
* 支持两种style：黑底白字 和 白底黑字 (默认)，更换了天气图标以适应不同style。
* 修正了 manifest.json 不起作用的问题。(modou-weather_v0.21 安装包)
* 注：此版本支持一键安装，用户无需任何配置！在此向所有 v0.1 的用户表示感谢，谢谢你们的意见和建议！

>【0.10】2014-08-02
* install 没有被执行，要在屏幕显示图标，请解压安装后将 /data/apps/*/weather.conf 手工复制到 /data/conf/launcher/conf.d 中，并将对应路径改为 /data/apps/*/。[ * 星号代表魔豆天气安装后的文件夹]
* 打开 /data/apps/*/weather.sh, 修改城市代码 [注意这次是 weather.sh] url="http://woa.hk/weather/?city=CHXX0116"    默认城市是上海-CHXX0116，用户根据附件查找对应城市代码，将其替换。
