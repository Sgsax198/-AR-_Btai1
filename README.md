# **一.视频链接：**
## [B站视频--功能演示及介绍](https://b23.tv/uXxuHkm)**（强烈推荐）**
立创主页有【开源】同系列智能眼镜

# **二.项目简介**
Btai box1智能眼镜盒配对Btai 1眼镜使用，方案为智融sw6208+沁恒ch582,可为AR眼镜充电，也可外做充电宝（22.5W），集成游戏手柄功能可蓝牙连接眼镜，集成屏幕

![操作使用图.png](https://image.lceda.cn/oshwhub/pullImage/4d937efa2ff945bcbda23f16c6c5d550.png)
# **三.成品展示**
### **（以下照片均无ai,手机实拍无修）**
![3bddea85d221e66f74de179e73728e14.png](https://image.lceda.cn/oshwhub/pullImage/831912d2d5ed47769fd4340091331f94.png)

![image.png](https://image.lceda.cn/oshwhub/pullImage/617e32faa7bf4da6be6fd9715c87dfb5.png)

![image.png](https://image.lceda.cn/oshwhub/pullImage/f618592b8adc435092d2df53ef2e3dee.png)

![屏幕截图 2026-10-10 011223.png](https://image.lceda.cn/oshwhub/pullImage/3beff21dc08143c5b7578b3b9924f569.png)

![屏幕截图 2026-10-10 011339.png](https://image.lceda.cn/oshwhub/pullImage/8b64a4ad99b44c658f579be9217b72e9.png)
# **四.眼镜机械层器件选型**
##  1.joycon摇杆
摇杆我们不用常见的手柄那种，使用了体型更小的switch同款的，有碳膜和霍尔两种，分别是5元/10元左右，有xy轴和下按按钮，使用adc采集

![e6dcd89c4be6c4915f4957320de446e7.jpg](https://image.lceda.cn/oshwhub/pullImage/1ae0f321d38f44ecb8373a6dbbfc1251.jpg)
##  2.2.8寸屏幕
屏幕是电容触摸屏，看起来透明度更好，，触摸芯片是cst836u，屏幕驱动芯片是st7789，都是常见芯片，分辨率是480*640，分辨率一般，但是价格还行，25元左右

![屏幕截图 2026-10-10 010450.png](https://image.lceda.cn/oshwhub/pullImage/8d33eff8f2fa4785ad81c215c88a9249.png)
##  3.3000mah锂电池
锂电池是2手淘来的，还挺便宜，规格书1307055，也可以用其他适合的规格，只要厚度在5.5mm及以下，电池输入是1s,多块则并联
![c62a6c17c9bfa30b2a6ec488b26572ec.jpg](https://image.lceda.cn/oshwhub/pullImage/feddb8b680234438afbaaf336ee10aa6.jpg)
##  4.磁吸充电卡座
适配眼镜的可拆卸电池电源座，pogopin接触充电
![4aae5d9cc9aa45d94db9525a993e7aa4.jpg](https://image.lceda.cn/oshwhub/pullImage/feaa0a5139584c148648658a67037c8b.jpg)


# **五.芯片选型**
### 1：充电宝芯片：智融SW6208
这颗芯片我们除了提供22.5w的typec输入和typea输出外，还集成了电量计，可以使用iic直接读取电池剩余电量及其他相关信息，以及集成了按键一键开关机
![fd4611d3c3b2f377934a81ca16835a61.jpg](https://image.lceda.cn/oshwhub/pullImage/08b013a6d51040c780cd259d1c9946ec.jpg)
### 2：蓝牙HID芯片：沁恒ch582m
沁恒同样是开源的好公司，，我们使用该芯片实现手柄/鼠标功能，582和583可以通用
> 下面是链接,沁恒蓝牙芯片开发：https://www.wch.cn/products/productsCenter/mcuInterface?categoryId=63&tName=%E9%9D%92%E7%A8%9ERISC-V%E8%93%9D%E7%89%99
> ![c18a39740dee25205543e2056aae3781.jpg](https://image.lceda.cn/oshwhub/pullImage/5148b8915eee48308a4856618aac4ee5.jpg)
### 3：磁吸电池充电芯片：LGS4056

![fa7054934747a64d52a79f8c0ef45fac.jpg](https://image.lceda.cn/oshwhub/pullImage/4dd06575479541e6b5586c70f88664b6.jpg)


# **六.整体框架**
![image.png](https://image.lceda.cn/oshwhub/pullImage/a727f723bbb34556ace9f04ec4afd17b.png)
下面是整个的电源环路框图，

![image.png](https://image.lceda.cn/oshwhub/pullImage/bb8c501a992646bf953d62b70d0e435c.png)

# **七.原理图绘制**
### 1：首先是充电宝这一块的实现，为右侧主板
![SCH_Schematic1_1-22.5w_sw6208_2026-09-05.png](https://image.lceda.cn/oshwhub/pullImage/657f5fcf0da941d5bdb08f7d4fc09a63.png)
### 2：然后是给眼镜磁吸电池充电的卡位，这是另一块小板
![SCH_Schematic5_2-charge_2026-09-05.png](https://image.lceda.cn/oshwhub/pullImage/b750e6e10e0c478a9cec7ae00bde5f8d.png)
### 3：接着就是mcu主控ch582m的外围电路
![SCH_Schematic1_3-ble_ch582m_2026-09-05.png](https://image.lceda.cn/oshwhub/pullImage/f7405b4752844f658477e48c263241c3.png)

# **八.PCB绘制、焊接**
pcb相对简单，1个主板4层集成绝大部分器件，充电输入输出及mcu电路
![90133054f4ff13c1978e2a10d4cbc221.jpg](https://image.lceda.cn/oshwhub/pullImage/ac2b7599b1294493988db51c3619a5af.jpg)
然后是3块小板，两块是左右各一的按键板，一块是盖子里的屏幕驱动板，这次没有话fpc，板与板之间直接用常见的标准0.5mm间距软排线
![5b85c054d8a0c87f54f05cd0696c9da3.jpg](https://image.lceda.cn/oshwhub/pullImage/c789212e2373438ab8cfbb2bac069701.jpg)

# **九.外壳建模**
首先是整体的一个模型
![image.png](https://image.lceda.cn/oshwhub/pullImage/f2f90d51ecce4a3c841a9266d3f7396a.png)
主要部件是外壳体、内胆和上盖

![image.png](https://image.lceda.cn/oshwhub/pullImage/e78fab9cfad3424bb874070ddc6e34f0.png)

![image.png](https://image.lceda.cn/oshwhub/pullImage/9d38b7d8379f44d68efbec5836902cfb.png)
以及装配电路板的细节

![5bef3600e23a0c5c32bb0c1d519c32f7.jpg](https://image.lceda.cn/oshwhub/pullImage/779d0d6c4bb546298f5a6ff505224fb0.jpg)
# **十.焊接后**
![屏幕截图 2026-10-10 005923.png](https://image.lceda.cn/oshwhub/pullImage/13404b0e36bc45fdb35d46a7f4144af8.png)


# **十一.芯片固件下载及SDK开发**
##  沁恒CH582M（BLE）
使用沁恒Mounriver studio/tool下载
![屏幕截图 2026-10-10 005238.png](https://image.lceda.cn/oshwhub/pullImage/a945d9e031824c2181404fc325d4166f.png)

# **十二.眼镜盒页面/功能**
##  1.充电宝输入输出
![给眼镜充电.jpg](https://image.lceda.cn/oshwhub/pullImage/5542583e5333477eb2261c2dc67e343e.jpg)
![眼镜盒充电1.jpg](https://image.lceda.cn/oshwhub/pullImage/8df321de1dee45399d741f8d8eb2b764.jpg)
##  2.蓝牙手柄/鼠标
![屏幕截图 2026-10-10 005012.png](https://image.lceda.cn/oshwhub/pullImage/71bb47f85fa54302b2acd089af102d74.png)
##  3.放眼镜
![眼镜眼镜盒4.jpg](https://image.lceda.cn/oshwhub/pullImage/3e46a36168ee4de3990f8aced14b2e47.jpg)
##  4.显示电量等
![119ae03857f9aad73ab2472eec0124a0.jpg](https://image.lceda.cn/oshwhub/pullImage/da6dabcfa19b4c9ca7f631220c092818.jpg)
##  5.给眼镜电池充电
![498f73424c228e9b054b3bc8d56fd6bd.jpg](https://image.lceda.cn/oshwhub/pullImage/486234fde6a445ceb6e56db5b6dc00e6.jpg)

