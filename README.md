# MaicroDX-Controller
基于CH552的一体化圆形控制轮盘，适配大多数的11英寸平板与[MaicroDX框体](https://github.com/freebird233/MaicroDX)
<br>
<br>
**· 特点:**  一体化主控；全彩灯效；所有内容开源；
<br>
**· 存在的问题:**  仅6键无冲；非回馈式灯光；留待发现；
<br> <br> 
**施工中...** <br>
截至目前说明文件尚未完成，如果您在过程中遇到了问题，请在群聊内提问，不要在issue区留言<br>
最后更新 2026.7.3
 <br> <br> 
[MaicroDX技术交流社区](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=uaJAwiIXVH5AWTCzZIfZjyvK5NMUc5RV&authKey=3EfBhaKBnfT3eZ%2F9ZlTbbR4r84ucNtt%2F%2FNDzzINnJAItXKx8PftKUk%2FCVn4rtrLw&noverify=0&group_code=1055571063)
 <br> <br> 
 
# 关于许可
-----
我在个人时间内制作了这个项目，没有任何经济利益或赞助。我将继续改进这个项目。我已尽我所能确保所有内容的准确性和功能性，但总有可能出现错误。如果你因使用这个开源项目而造成时间或金钱的损失，我不能负责。感谢你的理解。MaicroDX系列遵循 [by-nc-sa规则](https://creativecommons.org/licenses/by-nc-sa/4.0/) 。所以你只能给自己和你的朋友 DIY，不能利用这个项目赚钱，比如收费的代做，出售整机等,注意团购和拼单订购原始元器件是合理的，非盈利的方式卖掉剩余的元器件也是可以接受的。
<br> <br> <br> 
# 特别感谢
- __@Fandorabox__ 为本项目命名
- **「和音屋」 立直麻将/音游/电玩** 提供实体机台作为扫描参考
- **嘉立创**公司为个人创作者降低打样成本

<br> <br> <br> 
# 工作模式介绍
maicrodx controller (以下简称mdxc) 共有两个模式，请依据使用场景确定方案后再开始制作<br>
<br> 
<br>

| **A_mode**  (短接STBY) | B_mode （开路STBY） |
| :--- | :--- |
| 一体化模式，便携首选。cc线直连轮盘与设备。用"纳米"胶布把轮盘贴在在平板上游玩 (**焊接所有元器件**) | 外接控制模式, 搭配Maicrodx框体使用,**只焊ws2802灯珠与FPC底座**,连接到外部控制板再通过数据线传给平板。(因为大多数的数据线没有足够的空间容纳进框体 |
<br>
<br> 
<img width="270"  alt="_cgi-bin_mmwebwx-bin_webwxgetmsgimg__ MsgID=5978720347427026372 skey=@crypt_5b51cbfd_c97b3b7ed41217eeedefb33553f2231f mmweb_appid=wx_webfilehelper" src="https://github.com/user-attachments/assets/31d41ac2-2bd1-482f-ad18-089340bdea1b" />
<img width="310"  alt="Snipaste_2026-06-20_23-03-16" src="https://github.com/user-attachments/assets/fcc64922-dd17-4255-9f67-8fe9722c466b" />

<img width="365"  alt="MVIMG_20260702_210600" src="https://github.com/user-attachments/assets/7261631c-6163-49fe-ba23-75936402fdc6" />


<br> <br> <br> 
# 1.购买元件
1. 电阻5.1KΩ ±1% 0805封装 *2 2元
2. 电阻10KΩ ±1% 0805封装 *1 2元
3. 电容0.1uf ±1% 0805封装 *2 2元
4. ws2812B 幻彩灯珠 侧投式 *8  6元
5. Cheery 矮红轴 *8 20元
6. USBC母座 卧贴 TYPE-C 16PIN 2MD(073) 1元
7. CH552g 单片机 *1 2元
8. FPC排线底座 12P *1 AFC01-S12FCA-00 1元
9. HC-1.25-2PWT 平衡头座 （可选，mdx外框使用，热插拔9P按键排线) 1元
10. FPC排线 12P 反向 (可选B_mode外接板方案使用) 1元
11.  M1.4*4.5镍 沉头自攻螺丝 *8 (可选，装饰用) 5.8元
<br> <br>
请注意:电烙铁，焊锡膏，助焊剂，吸锡带等工具没有在此列出
<br> <br>

# 2.订购PCB板
-尽可能选择较薄的板厚<br><br>
例如嘉立创最近取消了冷门工艺费用，双层板，0.8厚，白色。样板订单单件价格约 16/张


<br> <br>
# 3.打印外壳
在Release处下载Model.STEP <br>
<img width="1200" alt="Snipaste_2026-07-02_23-48-56" src="https://github.com/user-attachments/assets/4cb6bfd1-12f3-4750-9b2f-d03b26c6ff84" />
它由两部分组成: "外壳" "外壳底板" 使用切片软件内的拆分功能，单独打印。(过盈配合) <br> 
外壳有比较大的悬空区域，在打印时，最好用不同材料的耗材作为支撑接触面。例如:PLA作为PETG的支撑 <br>
按键同理 <br>
(后续我会上传3MF文件) <br>

<br> <br>
# 4.焊接元器件
焊接通常遵循从难到易的顺序，比如TYPE-C母座，FPC母座，WS2812B灯珠这些部件推荐优先处理 <br> ps:使用锡膏与大量的助焊剂 <br>
如果使用回流焊工艺，请注意FPC底座在板子的底面

<br> <br>
# 5.烧录程序
在官网下载烧录软件[WCHISPStudio](https://www.wch.cn/downloads/WCHISPTool_Setup_exe.html) <br> 
在Release下载.hex固件程序<br>
    （1~8号键输出cxzaqwed,9号键为3.同时长按3456键400ms在选曲灯效与游戏灯效之间切换，长按7812键400ms进入彩虹渐变灯效模式，退出长按3456）<br>
上电前记得用万用表测量5V与GND焊盘是否短接<br>
<img width="720" alt="Snipaste_2026-07-02_20-34-18" src="https://github.com/user-attachments/assets/3abe23a6-3a7c-488c-9f09-9790bfdc47e0" /> <br>
将板子连接电脑，此时会显示出设备名<br>
点击烧录<br>
完成烧录<br>

https://github.com/user-attachments/assets/6a8587d2-b886-4417-bf86-0edc023bd731

<br>
检查信号灯是否依次亮起（就像上面的视频）由于WS2812的串联信号传输特性，当一个灯珠信号脱焊，会导致后面的所有灯熄灭。<br>
短接各按键的两个焊盘，检查是否有输出(白灯转变为黄灯)<br>
<br>
<br>
如果使用外接控制板，圆盘pcb只焊接灯光与FPC底座，其余的在外界控制板中，如图所示<br>
<img width="480" alt="abd05224c374d1d27d987409a571683e" src="https://github.com/user-attachments/assets/f13a7d16-cb30-456b-a744-40a4c49857ca" />
<br>(12P FPC座位于底层)



