# MaicroDX-Controller
基于CH552的一体化圆形控制轮盘，适配大多数的11英寸平板
<br> <br> <br> 
# 施工中...
 <br> <br> 

关于许可
-----
我在个人时间内制作了这个项目，没有任何经济利益或赞助。我将继续改进这个项目。我已尽我所能确保所有内容的准确性和功能性，但总有可能出现错误。如果你因使用这个开源项目而造成时间或金钱的损失，我不能负责。感谢你的理解。MaicroDX遵循 by-nc-sa规则 。所以你只能给自己和你的朋友 DIY，不能利用这个项目赚钱，比如收费的代做，出售整机等,注意团购和拼单订购原始元器件是合理的，非盈利的方式卖掉剩余的元器件也是可以接受的。
https://creativecommons.org/licenses/by-nc-sa/4.0/

<br> <br> <br> 
# 工作模式介绍
maicrodx controller (以下简称mdxc) 共有两个模式，目前没有办法热切换，建议先依据使用场景确定方案后再开始制作
<br> **短接STBY=A_mode 断路=B_mode**
<br>
<br>
A_mode:一体化模式，cc线直连轮盘与设备。用"纳米"胶布把轮盘贴在在平板上游玩 (短接STBY焊盘) 便携首选
<br> 
<img width="420"  alt="_cgi-bin_mmwebwx-bin_webwxgetmsgimg__ MsgID=5978720347427026372 skey=@crypt_5b51cbfd_c97b3b7ed41217eeedefb33553f2231f mmweb_appid=wx_webfilehelper" src="https://github.com/user-attachments/assets/31d41ac2-2bd1-482f-ad18-089340bdea1b" />
<img width="480"  alt="Snipaste_2026-06-20_23-03-16" src="https://github.com/user-attachments/assets/fcc64922-dd17-4255-9f67-8fe9722c466b" />

<br> <br> 
B_mode:外接控制模式, 适合搭配Maicrodx外框体使用,**只焊ws2802灯珠与FPC底座**,连接到外部控制板再通过数据线传给平板。(因为大多数的数据线没有足够的空间容纳进框体
<br> 外接模式演示

https://github.com/user-attachments/assets/6a8587d2-b886-4417-bf86-0edc023bd731

<br> <br> <br> 
# 选购元器件
1. 电阻5.1KΩ 0805封装 *2
2. 电阻1KΩ 0805封装 *1
3. 电容0.1uf 0805封装 *2
4. ws2812 幻彩灯珠 侧投式 *8  WS2812B-4020
5. Cheery 矮红轴 *8
6. USBC母座 卧贴 TYPE-C 16PIN 2MD(073)
7. CH552g 单片机 *1
8. 2.54-1*2P母 （可选，mdx外框使用，热插拔9P按键排线)
9. FPC排线底座 12P *1 AFC01-S12FCA-00
10. FPC排线 12P 反向




