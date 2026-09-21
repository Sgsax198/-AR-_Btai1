# -AR-_Btai1
Btai1光波导眼镜使用microled,支持单绿色640*480显示，方案为全志V821+EMMC+杰理JL7016，硬件集成扬声器，800w摄像头,线性马达，具有可插拔300mah磁吸电池

# **一.视频链接**：
[B站视频--功能演示及介绍](https://www.bilibili.com/)**（强烈推荐）**
立创主页有【开源】同系列智能眼镜盒
# **二.项目简介**
从25到26年，meta、阿里、华为一众大厂涌入智能眼镜行业，也不乏rokid、雷鸟等新秀发布一系列ai或ar眼镜
智能眼镜到底凭什么被看好，到底哪里吸引人眼球？
下文将带你从了解智能眼镜到从0手搓媲美市面产品的光波导AR眼镜
我们为它取名Btai 1
![8098c764a4e5d3f0c75b2cb7b8b7cfea.jpg](https://image.lceda.cn/oshwhub/pullImage/886e3202275946979ee19be873b3800f.jpg)
# **三.成品展示**
### **（全文照片均无ai,均为手机实拍无修图）**
![image.png](https://image.lceda.cn/oshwhub/pullImage/ce8859596bf14a608f235f835e0c37a7.png)
上图是眼镜的打开状态，我们不难发现大多数个人博主开源的眼镜是镜框镜腿一体不可折叠的，而Btai 1是完全贴合实际眼镜来做的，不仅可折叠，铰链还是金属可调松紧度的

![image.png](https://image.lceda.cn/oshwhub/pullImage/1c31406c250c4c6fae03ff09ffb5c492.png)
我们自制时外壳为3D打印，因此配色也是可自由选择的

![b9b31c74da4876a2da5a5567257bcd4f.jpg](https://image.lceda.cn/oshwhub/pullImage/a39a4618c8684b51b80c8f28e1ede2c0.jpg)
下图是显示效果
![e6b339efa85b8f2514ba8ed1782bc2ff.jpg](https://image.lceda.cn/oshwhub/pullImage/fcc69cc95981422c8f86359763df280a.jpg)
下图是部分PCB
![7008a1755a83b02f1ba10db2d40afcca.jpg](https://image.lceda.cn/oshwhub/pullImage/a632d31a991341dc85d389d9f7aad550.jpg)
言归正传，接下来我们将一步步带你手搓上述智能眼镜，包括配套的智能眼镜盒以及手机软件

# **四.什么是光波导**
光线从光机投射进入镜片内部，依靠**全内反射**，光线在镜片内部来回反弹向前传播，不会直接透出镜片；到达人眼区域再把光耦合输出投射进眼睛。
下图为珠海莫界科技的单绿色树脂衍射光波导镜片（有左右镜片之分）
![66e0826f1406edc1cb192004122b8376.jpg](https://image.lceda.cn/oshwhub/pullImage/319d52ae25f548b2b893b1c48f84f8db.jpg)

# **五.镜片是怎么显示内容的**
**镜片本身不会发光**，它只负责 “传输 + 投射图像”，真正生成画面的是**微型光机（微显示芯片）**。整套分为：光机成像 → 耦合进镜片 → 镜片内部传播 → 输出到眼睛

以下是上海显耀的蜂鸟单绿色光机JBD013(官网：https://www.jb-display.com.cn/)

![image.png](https://image.lceda.cn/oshwhub/pullImage/83fcd3f8b9b8475f982b9e8fbfbee29f.png)
下面是实机
![61e4da2dc1399aa54d5dfc851c8b8083.jpg](https://image.lceda.cn/oshwhub/pullImage/e35851dbcc3441299ad84bd136e00116.jpg)
光机是microled+光学镜头，拆除镜头后如下

![640ed991af74cf1e389ce9cdeccb1cc5.jpg](https://image.lceda.cn/oshwhub/pullImage/bbb2a67b95bb4b988cd4aea034c1c49e.jpg)
光波导只能通过固定颜色的的光

![56fe15a6248f880f57a2e9a0780632ca.jpg](https://image.lceda.cn/oshwhub/pullImage/2811719633784acb8669fde1a329fcd1.jpg)
光机直接投影到墙上和投影到光波导镜片的显示效果，下图为jbd013的光机自检图案

![dfd774db05be9b5fda6408f80f44cb5b.jpg](https://image.lceda.cn/oshwhub/pullImage/2c96b151d94f4faeb02480deda191b4a.jpg)

# **六.眼镜机械层器件选型**
##  1.鼻托
这里有两种我比较喜欢的，，开源模型用的是第二种，缺点是牢固性不如一，但价格为一的一半，3元左右，链接在器件清单里有总结
![b928699e3e2f55d8024c56ce17c10aba.jpg](https://image.lceda.cn/oshwhub/pullImage/c714962a298d492a9e81bc0cc54b69f2.jpg)
##  2.铰链
大厂的智能眼镜铰链基本上都是粉末冶金工艺，优点是适配眼镜，可穿插fpc排线，但是价格高达百元，考虑到自制，这里用常规眼镜铰链，价格约3元，好歹也是金属的，缺点是镜腿结构设计困难
作者尝试设计过一体打印的铰链，但是实际效果远不如金属，折叠困难+容易损坏
![9c6a05eaacde6e8278dbd6c9ce52db8a.jpg](https://image.lceda.cn/oshwhub/pullImage/fe2d92e09e83488d9b1e3e8ea4cc8708.jpg)
##  3.可拆电池磁吸座及锂电池
Btai 1眼镜使用了可拆的磁吸电池，磁吸座同样是市面上难以找到合适的，最好我选择了自制，通过打印&lt;10mm的pcb和结构件+**pogopin**
锂电池的型号是701438，容量是**300mah**,普遍大于市面上的光波导眼镜
![341b05def11011d47a66b7fc46dffe85.jpg](https://image.lceda.cn/oshwhub/pullImage/2f97410eb59e4301a851396b9c01ca41.jpg)
##  4.机载按键
既然是为了去贴合市面上的产品，我们在按键上也是精益求精，选择了手机的侧方按键，也可自行打印
![402e170f476f4b8e9b4f75337adf76a2.jpg](https://image.lceda.cn/oshwhub/pullImage/3898bbf317c94f58a79cae72a1e284a2.jpg)
##  5.扬声器
智能眼镜缺少不了ai对话、听歌等功能，因此扬声器必不可少，左右各一
以下两种型号，前者1306，后者1508，1508更好，但是开源的这款是镜腿7.6mm规格，我们暂时选择前者，当然作者我已经在尝试研发2代，大概率能上后者更好的喇叭
![fb6191704bdd753f2016405073e78e6c.jpg](https://image.lceda.cn/oshwhub/pullImage/0e49f864e3a0454a9e9a6ad740e94f20.jpg)
##  6.摄像头
摄像头使用的是索尼的imx219,像素800w,价格约30元，
![20f1dc064fdab97b922b754ebf0a406a.jpg](https://image.lceda.cn/oshwhub/pullImage/809ba8632beb47c2b168a61f917bcda6.jpg)
##  7.线性马达
智能眼镜为什么用线性马达呢？作者这里留下点悬念，因为相关的软件功能还没有开发好
下图的马达为1906规格的x轴线性马达，不用猜就知道是用来做交互反馈
![6e7b3760171c6f02bc4403ebd31a36a4.jpg](https://image.lceda.cn/oshwhub/pullImage/56f1e96d667342ce9e2f2c208000fc79.jpg)

# **七.芯片选型**
全志V821_WBX是专门为智能眼镜设计的芯片，也是目前我们能够买到的最适合的眼镜芯片之一，其量产于2025，有相当多的华强北和正规厂商使用该芯片做ai眼镜，当然支持光波导的我还没有看见，当然如果主播有得选的话，主播更加喜欢展锐的W517等或星宸的SSC309这些更好的
这时候有人就要问了，小米眼镜用的啥芯片，没错，高通的ar系列，单价高达400人民币。。。
下面有全志官网对该芯片的全套开发教程，简直是yyds
&gt; 全志V821开发教程：https://docs.aw-ol.com/docs/soc/v821/
![image.png](https://image.lceda.cn/oshwhub/pullImage/177d5e832c524a15bff3368386be40e9.png)
![image.png](https://image.lceda.cn/oshwhub/pullImage/148f6a2036c34e8ab2c863fd4b91a502.png)

三星KLM
杰理JL7016G8
为什么要选杰理这颗芯片呢
- 1.专业耳机芯片
- 2.这个系列是杰理里开源的比较好的，JL7018更好，但是价格偏高
- 3.恒玄bes2700,物奇为wq7036这些大厂喜欢的主播买不到
- 4.中科蓝讯同样买不到不开源
杰理官网同样给了JL701n系列的sdk,但是开发编译链比较复杂，光是一个下载器就要80元
&gt; 杰理JL701N开源SDK链接：https://gitlab.zh-jieli.com/soundbox/novisualization
&gt; ![dd542e0a7b6c733382ca1a87afb0415f.jpg](https://image.lceda.cn/oshwhub/pullImage/f489f3b0fa7c4cc1b2d919a19eb37775.jpg)

# **八.整体框架**
![image.png](https://image.lceda.cn/oshwhub/pullImage/a727f723bbb34556ace9f04ec4afd17b.png)

# **九.原理图绘制**
嗯，对，硬件部分相当复杂，特别是FPC部分，但是大部分智能眼镜的设计都如此
全板最关键的芯片当然是全志V821，下面是其外围电路，射频天线我们使用陶瓷天线，也可以焊接天线弹片对接fpc天线，晶振是1206规格的40M晶振，麦克风是差分输入，
全志V821电源需要3路且要启动顺序，0.9v,1.5v,3.3v,该芯片内部也有ldo能输出1.8v,可供摄像头或按钮的上拉
下面有全志官网对该芯片的全套开发教程，简直是yyds
![SCH_Schematic1_1-cpu_v821_2026-09-04.png](https://image.lceda.cn/oshwhub/pullImage/ebc5a7168086498da5751f44684e328c.png)

EMMC是一个对学生比较新奇的芯片，最近价格也是水涨船高，主播在淘宝大约是4G就要25元，8G以上就很贵了，这里只用了4data数据线，全志只支持该速度，EMMC芯片封装是通用的，所以不需要就着型号买
norflash是用来存储固件的，用来实现快启动，也可以把固件下载到emmc,不焊接flash
![0ea0f0b24ee02153efba6a769f817f2d.png](https://image.lceda.cn/oshwhub/pullImage/02ebe11733a646e09635cea9b8edea7c.png)
我们用到的芯片比较多，下面单独列出了io口的连接关系
![8e76a5e724cd4f7023c4f7bd6bae4288.png](https://image.lceda.cn/oshwhub/pullImage/bcb32f23ff754da28bb5fdf15c2c71dc.png)


然后是两个比较关键的组件的外围电路
首先是摄像头IMX219，这个摄像头的引脚是博主当时从树莓派引脚反推出来的，所以摄像头缺少复位引脚，不过驱动时我们用不到，如果需要复位，可以直接控制LDO的en引脚，摄像头是2lane的mipi+1路时钟，都需要做等长控制和阻抗
![22dd8988fcdc953bb32e425679937ff5.png](https://image.lceda.cn/oshwhub/pullImage/943baec62bc34bc992257e0a485fa89d.png)
然后是关键的MicroLED的驱动电路，同样是3路电源，因为驱动屏幕有一路2.0v负压比较少见，2.5v电压是io口电压，也可以给3.3v,保险起见我们给2.5V

![SCH_Schematic2_4-mled_jbd013_2026-09-05.png](https://image.lceda.cn/oshwhub/pullImage/8ac804b4d3f14704a8f305c9a08609b6.png)
还有一个关键控制芯片，因为是双芯片方案全志+杰理，所以有俩路音频输出，因此需要把它们整合成一路，我们选择一颗专门为音频设计的通道选择芯片，选择引脚由全志决定，默认输出是杰理，负责常用耳机功能
![956aee7ec33a48129f0f74ebd1b317ef.jpg](https://image.lceda.cn/oshwhub/pullImage/26fa366a30a0451892cc1ad4d9e3be2c.jpg)
电源控制又是一块很复杂的部分，主要原因是充电回路这一块，怎么在充电时选择外部电源，怎么在外部电压输入时内部电压能不偏离，以及如何避免低电压时候逆差烧坏芯片，怎么确保电池低于3.3v时还能输出3.3v,所以还要先升压再降压
![image.png](https://image.lceda.cn/oshwhub/pullImage/e8d8170775544dd6b1f98e88dd740c5c.png)
# **十.PCB绘制、焊接**
嗯，对，PCB部分相当复杂
首当其冲的就是6层的主控板，分为2块叠层6+4，btb对接，如果你问我为什么不打成一块，我会说没钱打高层板
![e0f5be9252a5d788e8cc429bac90d367.jpg](https://image.lceda.cn/oshwhub/pullImage/9bcb628cb0f54a139ea71322d864b04e.jpg)
下面是2D和3D图
![783d312cb56e043e0a4107b02b2490f0.jpg](https://image.lceda.cn/oshwhub/pullImage/0e2e0b99e349408a933b97188dc20047.jpg)
V821开发是使用Linux开发，难度偏高，所以我们当时其实也做了一版学生更加熟悉的stm32版本，芯片是stm32h750ibk6

![5bde9ee7072237a23d01614a01f051f1.jpg](https://image.lceda.cn/oshwhub/pullImage/cd98e33f96564f9ea21ef94ecf63be51.jpg)
下面是下层的layout图
![7d2c3fead50de4fdd3188b28759d5408.jpg](https://image.lceda.cn/oshwhub/pullImage/77d610c9df694358b77c3214a76306e7.jpg)
下面是下层的2D和3D图
![47b4df44421070f486b088136595b6f8.jpg](https://image.lceda.cn/oshwhub/pullImage/4c4a83a90846455fad7acc26f7051317.jpg)
下面是安装在右镜腿处得按键小板
![f11db0648fe6b3c96a1e8035516c87bb.jpg](https://image.lceda.cn/oshwhub/pullImage/b4cd07cc958c467b8810cc006db74d2b.jpg)

# **十一.FPC绘制、焊接**
FPC这块更加令人头疼，为了把眼镜做的够细够薄，fpc也设计得很极限，因为怕4层fpc太贵，所以实际得都是2层，结果后来发现其实4层更加省钱，但是主包我懒得继续优化了，主包要找工作了
### 1.首先是信号排线、光波导排线、主电源排线，从右镜腿尾部到前镜腿尾部
![cba3d9181e5cbab81ce457d8351e83fd.jpg](https://image.lceda.cn/oshwhub/pullImage/26d63e24d25445cebfd192dc2c01454f.jpg)
### 2.触摸模块排线
![724edf760853f96fdefc169b92637b60.jpg](https://image.lceda.cn/oshwhub/pullImage/10aa9b261ac0484abd8ad4e5f68321b3.jpg)
### 3.喇叭引出排线
![98bfcd65c651354a5a5ccb880a8298b1.jpg](https://image.lceda.cn/oshwhub/pullImage/9839fc27cff7431998042a65f8cc7bc3.jpg)
# **十二.外壳建模**
让主包一个干电子的来设计这种复杂曲面建模真是难为我了，下面是主包前后的两次主要版本，左上角是本次开源的一版
![image.png](https://image.lceda.cn/oshwhub/pullImage/b830a6b86aa3495487c575e2fe5b97a1.png)

主要还是镜腿处和主板放置处的不同，下面两种大致外型也是市面两大主流
![40c491caba09fdc18868e189ed86c046.jpg](https://image.lceda.cn/oshwhub/pullImage/a527042dc24f4864a513d44095387afd.jpg)
下面是内部的结构

![image.png](https://image.lceda.cn/oshwhub/pullImage/072e82de89df48b18ce28750c5fbedc0.png)
下面是铰链，光机，摄像头的重要关键结构细节

![287b548616be6c309926a382b8ef2f3b.jpg](https://image.lceda.cn/oshwhub/pullImage/6f819184a604464fae1b72be81065d9f.jpg)
下面是左右镜腿尾部关键结构，右尾部是电池安装处，左镜腿尾部是主板安装处

![15dd9e392ab54b1d30bcd34dcaaebe98.jpg](https://image.lceda.cn/oshwhub/pullImage/344ef203019549f0975515f3b4d4ee63.jpg)
# **十三.实物装配**
嗯，对，硬件部分相当复杂，特别是FPC部分，但是大部分智能眼镜的设计都如此


# **十四.芯片固件下载及SDK开发**
##  1.全志V821_WBX
使用ADB推送或PhoenixSuit下载，需要按住下载键插入电脑进入下载模式

![image.png](https://image.lceda.cn/oshwhub/pullImage/c6294cd5fe13406e89f89e7def95172f.png)
##  2.杰理JL7016G8（可选）
使用杰理编译链及codeblocks下载
![933c47e5cf2a812f38b28e9f05d32b55.jpg](https://image.lceda.cn/oshwhub/pullImage/7dd7f38acae04599926ee7cb9f31fa4f.jpg)
在IDE里点击编译下载，有下载完毕就可以了，不得不说，这个软件做的可真烂
![image.png](https://image.lceda.cn/oshwhub/pullImage/1a2f885936ed4326a0276737b279f7e1.png)
##  3.沁恒CH582M（可选）
使用沁恒Mounriver studio/tool下载

# **十五.眼镜页面/功能**
下图展示的分别是菜单页，ai对话，实时翻译，手机互联

![image.png](https://image.lceda.cn/oshwhub/pullImage/6c4c30d451594e0886452f912418ba53.png)

# **十六.近视眼能不能戴**
作者我自己就是近视，目前行业还没有一个好的方法解决这一问题，大厂也基本是外挂镜片，所以我们也是，未来如果该问题突破，智能眼镜将真正具备影响力
下图为Btai 1适配的近视镜片
![7bc6fafa95dc4fa8af7f0ccc28480c0e.jpg](https://image.lceda.cn/oshwhub/pullImage/324f4338e3c84e1f84bbb8264cdf8181.jpg)


# **十七.带起来累不累**
如果是有戴眼镜习惯的话，Btai 1的重量是可接受的，当然40几克的重量也是和大厂一样了，对于无佩戴习惯的人来讲其实是需要时间适应的，刚开始会累
![image.png](https://image.lceda.cn/oshwhub/pullImage/66c5559076a54cf9b4933849fe0ef7d1.png)

![image.png](https://image.lceda.cn/oshwhub/pullImage/0c454a78b79648b38f56b451c68a8f5a.png)
# **十八.配套安卓软件**
软件使用的flutter框架，不过目前只适配了安卓，当然源码开源，可以自己继续优化软件，毕竟我们开源出的软件功能还不完善
![98dc6eeeaeaea2755f5a1d5ba4f234df.jpg](https://image.lceda.cn/oshwhub/pullImage/84aad53739f14380940998f0276c62cb.jpg)
打开软件后主导航栏有4个，分别是
- 1. **主页**:快捷管理设备智能眼镜，配网，眼镜信息等
- 2. **应用**页:打开/管理已下载的应用
- 3. **软件商店**页:下载小程序/软件/智能体/到智能眼镜
- 4. **我的**页面:管理账号几各种玩法规则，加入开发者，提交帖子/应用

 <img src="https://image.lceda.cn/oshwhub/pullImage/0ea9a17e98244b0994bb174db4957901.jpg" width="800" /> 

下图是眼镜初次配网流程


