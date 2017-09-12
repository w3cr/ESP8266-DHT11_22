# ESP8266接入DHT11模块读取温湿度
> Power By : oneHacking     欢迎转载请注明出处

> 出自本群作品：[跑在树莓派上的智能家居](http://iot0.tk:8081)

> 技术支持群组：[Q群 300717117](https://jq.qq.com/?_wv=1027&k=51EYE42)

###1.固件刷入
*   一. 先将ESP8266与电脑连接，并查看设备管理器，记录COM端口
        ![3.png](https://i.loli.net/2017/09/13/59b81adfba00b.png)
        
*   二. 使用ESP8266Flasher.exe上传固件

    *   设置如下参数

       ![flash1.jpg](https://i.loli.net/2017/09/13/59b817c99acb3.jpg)
    
    *   点击小齿轮选择要刷入的固件(文件名后缀为波特率)，并设置地址为0x00000

       ![flash2.jpg](https://i.loli.net/2017/09/13/59b817c9a3846.jpg)
    
    *   选择记录下的COM端口，并点击flash按钮，等待固件上传完成

       ![flash3.jpg](https://ooo.0o0.ooo/2017/09/13/59b83df32af33.jpg)

###2.电路连接
>3v3 => 3v3，GND => GND，out => GPIO14（请参考如下引脚图）

>![20160612155802584.png](https://i.loli.net/2017/09/13/59b82333564fc.png)

###3.查看温湿度数据
>使用串口助手，设置波特率为（74880 及 115200）
>temp为当前温度，humi为当前湿度
