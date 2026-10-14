# **一.📺视频链接**：
## &gt; 🎬 **[B 站视频 —— 功能演示及介绍](https://b23.tv/uXxuHkm)**（强烈推荐先看！）
立创主页有【开源】同系列智能眼镜盒

# **二.📖 项目简介**
2025 到 2026 年，Meta、阿里、华为一众大厂纷纷涌入智能眼镜行业，Rokid、雷鸟等新秀也发布了一系列 AI / AR 眼镜。

智能眼镜到底凭什么被看好？究竟哪里吸引人眼球？

本文将带你从了解智能眼镜开始，**从 0 手搓一副媲美市面产品的光波导 AR 眼镜**，我们为它取名 —— **Btai 1**。
![8098c764a4e5d3f0c75b2cb7b8b7cfea.jpg](https://image.lceda.cn/oshwhub/pullImage/886e3202275946979ee19be873b3800f.jpg)
 # **三、🕶️ 成品展示**

## &gt; 📷 **全文照片均为手机实拍、无修图、无 AI 生成。**

![眼镜打开状态 1](https://image.lceda.cn/oshwhub/pullImage/eda79a05c26143a599966eb52de6abc2.png)

![眼镜打开状态 2](https://image.lceda.cn/oshwhub/pullImage/ce8859596bf14a608f235f835e0c37a7.png)

上图是眼镜的打开状态。不难发现，大多数个人博主开源的眼镜镜框与镜腿一体、**不可折叠**；而 Btai 1 完全贴合真实眼镜设计：

- ✅ **可折叠**结构
- ✅ **金属铰链**，还可以调节松紧度

![3D 打印外壳，配色自由](https://image.lceda.cn/oshwhub/pullImage/1c31406c250c4c6fae03ff09ffb5c492.png)

自制外壳采用 **3D 打印**，因此配色也可以自由选择。

![实机实拍](https://image.lceda.cn/oshwhub/pullImage/e939ebf30dd240a5aa2efe97ce443394.jpg)

下图是 **显示效果**：

![显示效果 1](https://image.lceda.cn/oshwhub/pullImage/4987ba33051f43f282a5ab90240250ed.jpeg)

![显示效果 2](https://image.lceda.cn/oshwhub/pullImage/94a9765737004c77bd38ac88b729919e.jpeg)

下图是 **部分 PCB**：

![部分 PCB](https://image.lceda.cn/oshwhub/pullImage/05a279d789c74ebbaa2e4d11ca1c2199.png)

言归正传，接下来将一步步带你手搓上述智能眼镜，包括配套的 **智能眼镜盒** 以及 **手机软件**。

![智能眼镜全家桶](https://image.lceda.cn/oshwhub/pullImage/4be0d304b6b144c691522e5fc78930d4.png)

---

# **四、🌈 什么是光波导**

光线从光机投射进入镜片内部，依靠 **全内反射（TIR）**，光线在镜片内部来回反弹向前传播，不会直接透出镜片；到达人眼区域后，再把光 **耦合输出** 投射进眼睛。

下图为珠海莫界科技的 **单绿色树脂衍射光波导镜片**（有左右镜片之分）：

![莫界单绿色衍射光波导镜片](https://image.lceda.cn/oshwhub/pullImage/319d52ae25f548b2b893b1c48f84f8db.jpg)

---

# **五、💡 镜片如何显示内容**

**镜片本身不会发光**，它只负责 “传输 + 投射图像”，真正生成画面的是 **微型光机（微显示芯片）**。整套链路如下：

```
光机成像  →  耦合进镜片  →  镜片内部全反射传播  →  耦合输出到眼睛
```

以下是上海显耀的 **蜂鸟单绿色光机 JBD013**（官网：）：

![JBD013 光机](https://image.lceda.cn/oshwhub/pullImage/83fcd3f8b9b8475f982b9e8fbfbee29f.png)

下面是实机：

![光机实机](https://image.lceda.cn/oshwhub/pullImage/fc57b00de7804c1ca3eb151d4bb60864.png)


光机由 **MicroLED + 光学镜头** 组成，拆除镜头后如下：

![拆除镜头后的光机](https://image.lceda.cn/oshwhub/pullImage/41b53f58bc134fd2b99fc777c4c5c066.png)


&gt; ⚠️ 光波导只能通过 **固定颜色** 的光。

![光波导单色特性](https://image.lceda.cn/oshwhub/pullImage/2811719633784acb8669fde1a329fcd1.jpg)

下图分别为光机直接投影到墙上、与投影到光波导镜片的显示效果对比（JBD013 的光机自检图案）：

![墙投 vs 光波导显示](https://image.lceda.cn/oshwhub/pullImage/2c96b151d94f4faeb02480deda191b4a.jpg)

---

# **六、🔩 机械层器件选型**

### 1. 鼻托

这里有两种我比较喜欢的，开源模型用的是第二种。缺点是牢固性不如第一种，但价格仅为第一种的一半，**3 元左右**，

![两种鼻托](https://image.lceda.cn/oshwhub/pullImage/c714962a298d492a9e81bc0cc54b69f2.jpg)

### 2. 铰链

大厂智能眼镜的铰链基本都是 **粉末冶金工艺**，优点是专为眼镜适配、可穿插 FPC 排线，但价格高达百元。考虑到自制，这里采用常规眼镜铰链，价格约 **3 元**，好歹也是金属的，缺点是镜腿结构设计困难。

作者尝试设计过一体打印的铰链，但实际效果远不如金属：**折叠困难 + 容易损坏**。

![金属铰链](https://image.lceda.cn/oshwhub/pullImage/fe2d92e09e83488d9b1e3e8ea4cc8708.jpg)

### 3. 可拆电池磁吸座及锂电池

Btai 1 使用了 **可拆的磁吸电池**。磁吸座在市面上难以找到合适的，最后我选择了自制：通过打印 **&lt; 10 mm** 的 PCB 和结构件，配合 **Pogo Pin** 实现。

锂电池型号为 **701438**，容量 **300 mAh**，普遍大于市面上的光波导眼镜。

![磁吸电池座与 701438 电池](https://image.lceda.cn/oshwhub/pullImage/2f97410eb59e4301a851396b9c01ca41.jpg)

### 4. 机载按键

为了贴合市面产品，按键上也精益求精，选择了 **手机侧方按键**，也可自行打印。

![机载按键](https://image.lceda.cn/oshwhub/pullImage/3898bbf317c94f58a79cae72a1e284a2.jpg)

### 5. 扬声器

智能眼镜少不了 AI 对话、听歌等功能，因此扬声器必不可少，**左右各一**。

以下两种型号：前者 **1306**，后者 **1508**。1508 效果更好，但开源这款是 **7.6 mm** 规格镜腿，暂时选择前者。当然作者已经在尝试研发二代，大概率能上更好的后者喇叭。

![1306 与 1508 扬声器](https://image.lceda.cn/oshwhub/pullImage/0e49f864e3a0454a9e9a6ad740e94f20.jpg)

### 6. 摄像头

摄像头使用索尼 **IMX219**，**800 万像素**，价格约 **30 元**。

![Sony IMX219 摄像头](https://image.lceda.cn/oshwhub/pullImage/809ba8632beb47c2b168a61f917bcda6.jpg)

### 7. 线性马达

智能眼镜为什么用线性马达？作者这里先留点悬念，因为相关软件功能还没有开发好。

下图马达为 **1906 规格的 X 轴线性马达**，不用猜就知道是用来做 **交互反馈** 的。

![1906 X 轴线性马达](https://image.lceda.cn/oshwhub/pullImage/56f1e96d667342ce9e2f2c208000fc79.jpg)

---

# **七、🧠 芯片选型**

| 芯片 | 厂商 | 角色 |
| :--- | :--- | :--- |
| **V821_WBX** | 全志 | 主控（为智能眼镜设计，2025 年量产） |
| **KLM 系列** | 三星 | eMMC 存储 |
| **JL7016G8** | 杰理 | 专业耳机 / 音频协处理器 |

### 1. 主控：全志 V821_WBX

全志 V821_WBX 是专门为智能眼镜设计的芯片，也是目前能买到的最适合眼镜的芯片之一。它量产于 2025 年，有相当多的华强北厂商和正规厂商使用该芯片做 AI 眼镜，不过支持光波导的我还没有见到。

当然，如果有的选，我更偏爱展锐 **W517** 或星宸 **SSC309** 这些更好的选择。

这时候有人就要问了：小米眼镜用的啥芯片？没错，高通 AR 系列，单价高达 **400 元人民币**……

&gt; 📚 全志官网提供了该芯片的全套开发教程，简直是 yyds：
&gt; **全志 V821 开发教程：**

![V821 资源 1](https://image.lceda.cn/oshwhub/pullImage/177d5e832c524a15bff3368386be40e9.png)

![V821 资源 2](https://image.lceda.cn/oshwhub/pullImage/148f6a2036c34e8ab2c863fd4b91a502.png)

### 2. 存储：三星 KLM（eMMC）

用于系统与数据存储，封装通用，不必拘泥于具体型号。

![image.png](https://image.lceda.cn/oshwhub/pullImage/5b87a450b9ff4b20b64d122112900838.png)
### 3. 音频协处理器：杰理 JL7016G8

为什么选杰理这颗芯片？

1. **专业耳机芯片**；
2. 这个系列是杰理开源得比较好的，JL7018 更好，但价格偏高；
3. 恒玄 BES2700、物奇 WQ7036 这些大厂喜欢的型号买不到；
4. 中科蓝讯同样买不到、不开源。

杰理官网同样提供了 JL701N 系列的 SDK，但开发编译链比较复杂，光是一个下载器就要 **80 元**。

&gt; 📦 **杰理 JL701N 开源 SDK：**

![杰理 SDK](https://image.lceda.cn/oshwhub/pullImage/f489f3b0fa7c4cc1b2d919a19eb37775.jpg)

---

# **八、🏗️ 整体框架**

![系统整体框架图](https://image.lceda.cn/oshwhub/pullImage/a727f723bbb34556ace9f04ec4afd17b.png)

---

# **九、📐 原理图绘制**

硬件部分相当复杂，尤其是 FPC 部分，不过大部分智能眼镜的设计都是如此。

### 1. 主控 V821 外围电路

全板最关键的芯片当然是全志 V821，下图是其外围电路：

- 📡 **射频天线**：使用陶瓷天线，也可焊接天线弹片对接 FPC 天线；
- ⏱️ **晶振**：1206 封装的 **40 MHz** 晶振；
- 🎙️ **麦克风**：差分输入；
- ⚡ **电源**：需要 **3 路** 电源且有上电时序要求 —— **0.9 V / 1.5 V / 3.3 V**；
- 芯片内部 LDO 可输出 **1.8 V**，可供摄像头或按键上拉使用。

&gt; 📚 全志官网对该芯片有全套开发教程：

![V821 主控原理图](https://image.lceda.cn/oshwhub/pullImage/ebc5a7168086498da5751f44684e328c.png)

### 2. 存储电路（eMMC / NorFlash）

eMMC 对学生来说是比较新奇的芯片，最近价格也水涨船高：淘宝上 **4 GB 约 25 元**，8 GB 以上就很贵了。这里只使用了 **4 条 Data 数据线**（全志只支持该速度）。eMMC 芯片封装是通用的，不需要拘泥于具体型号购买。

**NorFlash** 用来存储固件，可实现快速启动；也可以把固件下载到 eMMC，不焊接 Flash。

![eMMC / NorFlash 电路](https://image.lceda.cn/oshwhub/pullImage/02ebe11733a646e09635cea9b8edea7c.png)

### 3. IO 连接关系总表

用到的芯片比较多，下面单独列出了各 IO 口的连接关系：

![IO 连接关系](https://image.lceda.cn/oshwhub/pullImage/bcb32f23ff754da28bb5fdf15c2c71dc.png)

### 4. 摄像头 IMX219

摄像头 IMX219 的引脚是当时从树莓派引脚反推出来的，所以缺少复位引脚，不过驱动时用不到；如果需要复位，可以直接控制 LDO 的 EN 引脚。

摄像头是 **2-Lane MIPI + 1 路时钟**，都需要做 **等长控制和阻抗控制**。

![IMX219 摄像头电路](https://image.lceda.cn/oshwhub/pullImage/943baec62bc34bc992257e0a485fa89d.png)

### 5. MicroLED 驱动电路（JBD013）

同样是 **3 路电源**。驱动屏幕有一路 **2.0 V 负压** 比较少见；2.5 V 是 IO 口电压，也可以给 1.8 V等，保险起见给 **2.5 V**。该驱动芯片选型和部分电路参考了开源作者**wwwwyt**的先进的光波导AR眼镜工程，在此致谢

![MicroLED JBD013 驱动电路](https://image.lceda.cn/oshwhub/pullImage/8ac804b4d3f14704a8f305c9a08609b6.png)

### 6. 音频通道切换

还有一颗关键控制芯片。因为是 **全志 + 杰理双芯片方案**，所以有两路音频输出，需要整合成一路。这里选择了一颗专为音频设计的 **通道选择芯片**：

- 选择引脚由 **全志** 控制；
- 默认输出 **杰理** 通道，负责常用耳机功能。

![音频通道选择电路](https://image.lceda.cn/oshwhub/pullImage/26fa366a30a0451892cc1ad4d9e3be2c.jpg)

### 7. 电源控制

电源控制是很复杂的一部分，难点主要在充电回路：

- 充电时如何选择外部电源；
- 外部电压输入时，如何保证内部电压不偏离；
- 如何避免低电压时压差倒灌烧坏芯片；
- 电池低于 3.3 V 时如何仍能输出 3.3 V —— 需要 **先升压再降压**。

![电源控制电路](https://image.lceda.cn/oshwhub/pullImage/e8d8170775544dd6b1f98e88dd740c5c.png)

---

# **十、🔌 PCB 绘制**

PCB 部分全部以0201封装为基础

### 1. 主控板（6 层叠板）

首当其冲的是 **6 层主控板**，分为 **2 块叠层（6 + 4）**，通过 **BTB 连接器** 对接。如果问为什么不打成一块板——答案是：**没钱**打高层多阶板。

![6 + 4 叠层主控板](https://image.lceda.cn/oshwhub/pullImage/9bcb628cb0f54a139ea71322d864b04e.jpg)

下面是 2D 和 3D 图：

![主控板 2D / 3D](https://image.lceda.cn/oshwhub/pullImage/0e2e0b99e349408a933b97188dc20047.jpg)

### 2. STM32 教学备选版

V821 使用 Linux 开发，难度偏高，所以当时还做了一版学生更熟悉的 **STM32 版本**，芯片为 **STM32H750IBK6**。

![STM32H750 版本](https://image.lceda.cn/oshwhub/pullImage/cd98e33f96564f9ea21ef94ecf63be51.jpg)

下面是下层板的 Layout 图：

![下层板 Layout](https://image.lceda.cn/oshwhub/pullImage/77d610c9df694358b77c3214a76306e7.jpg)

下面是下层板的 2D 和 3D 图：

![下层板 2D / 3D](https://image.lceda.cn/oshwhub/pullImage/4c4a83a90846455fad7acc26f7051317.jpg)

### 3. 镜腿按键小板

安装在左右镜腿处的按键小板相对简单：为了免费打样 **1.0 mm** 厚度，采用两层板设计，PCB 宽度 **6 mm**，放进镜腿不会太宽；但阻容元件仍是 **0201** 封装，比较难焊。

- 🔹 **左镜腿 PCB**：连接主板与光波导，承载光波导驱动、镜腿喇叭功放、开关机开关、拍照录像开关，以及一颗 **光强度传感器**；
- 🔹 **右镜腿 PCB**：承载右喇叭功放、线性马达驱动，以及开关机键和音量键。

![左右镜腿按键小板](https://image.lceda.cn/oshwhub/pullImage/7f27f384231d4dafa48dc5ef271253b1.jpg)

---

# **十一、🧵 FPC 绘制**

FPC 更加令人头疼。为了把眼镜做得够细够薄，FPC 也设计得很极限。因为怕 4 层 FPC 太贵，实际用的都是 2 层；结果后来发现其实 **4 层反而更省钱**，不过作者懒得继续优化了——主包要找工作了。

### 1. 信号排线 / 光波导排线 / 主电源排线

从右镜腿尾部到前镜腿尾部：

![信号 / 光波导 / 主电源排线](https://image.lceda.cn/oshwhub/pullImage/26d63e24d25445cebfd192dc2c01454f.jpg)

### 2. 触摸模块排线

![触摸模块排线](https://image.lceda.cn/oshwhub/pullImage/10aa9b261ac0484abd8ad4e5f68321b3.jpg)

### 3. 喇叭引出排线

![喇叭引出排线](https://image.lceda.cn/oshwhub/pullImage/9839fc27cff7431998042a65f8cc7bc3.jpg)

### 4. 单目光波导版本（V2.0）

后来实在没钱打大面积 FPC 了，所以设计了 **V2.0 单目光波导排线**，可以免费打样。

![V2.0 单目光波导排线](https://image.lceda.cn/oshwhub/pullImage/6d14609dbfb74de4827b2e4cd009f655.jpg)

---

# **十二、🖨️ 外壳建模**

让一个干电子的来设计这种复杂曲面建模，真是难为我了。下面是前后两次主要版本，**左上角即本次开源的一版**：

![外壳版本演进 1](https://image.lceda.cn/oshwhub/pullImage/b830a6b86aa3495487c575e2fe5b97a1.png)

![外壳版本演进 2](https://image.lceda.cn/oshwhub/pullImage/840c4c1cbf884b4faf09c3c47895e667.png)

主要区别在镜腿处与主板放置处，下面两种大致外型也是市面两大主流：

![两种主流外型](https://image.lceda.cn/oshwhub/pullImage/a527042dc24f4864a513d44095387afd.jpg)

下面是内部结构：

![外壳内部结构](https://image.lceda.cn/oshwhub/pullImage/072e82de89df48b18ce28750c5fbedc0.png)

下面是 **铰链、光机、摄像头** 的关键结构细节：

![铰链 / 光机 / 摄像头结构](https://image.lceda.cn/oshwhub/pullImage/6f819184a604464fae1b72be81065d9f.jpg)

下面是左右镜腿尾部关键结构：**右尾部是电池安装处，左镜腿尾部是主板安装处**。

![左右镜腿尾部结构](https://image.lceda.cn/oshwhub/pullImage/344ef203019549f0975515f3b4d4ee63.jpg)

---

# **十三、✨ 焊接 / 打印成品**

![焊接完成的 PCB](https://image.lceda.cn/oshwhub/pullImage/05a279d789c74ebbaa2e4d11ca1c2199.png)

![整机成品 1](https://image.lceda.cn/oshwhub/pullImage/561916cf37654abc802c72445636bd34.jpg)

![整机成品 2](https://image.lceda.cn/oshwhub/pullImage/78fd22955dca4223ac2817a8b10a4680.png)

**镜框颜色选择：**

![多色镜框](https://image.lceda.cn/oshwhub/pullImage/af82d02e46fa44c090f06e1c92036d0d.jpg)

---

# **十四、💾 固件下载与 SDK 开发**

### 1. 全志 V821_WBX

使用 **ADB 推送** 或 **PhoenixSuit** 下载：需要按住下载键插入电脑，进入下载模式。

![PhoenixSuit 下载](https://image.lceda.cn/oshwhub/pullImage/c6294cd5fe13406e89f89e7def95172f.png)

### 2. 杰理 JL7016G8（可选）

使用杰理编译链及 **CodeBlocks** 下载：

![杰理编译链](https://image.lceda.cn/oshwhub/pullImage/7dd7f38acae04599926ee7cb9f31fa4f.jpg)

在 IDE 里点击编译下载，提示下载完毕即可。不得不说，这个软件做得可真烂。

![CodeBlocks 下载界面](https://image.lceda.cn/oshwhub/pullImage/1a2f885936ed4326a0276737b279f7e1.png)

---

# **十五、📱 眼镜页面与功能**

下图展示的分别是：**菜单页、AI 对话、实时翻译、手机互联**。

![菜单 / AI 对话 / 翻译 / 互联](https://image.lceda.cn/oshwhub/pullImage/6c4c30d451594e0886452f912418ba53.png)

以下是一些其他应用：

![其他应用](https://image.lceda.cn/oshwhub/pullImage/31e0df3b6a914f12a7b3cae625cca028.jpeg)

以下是一些游戏：

![眼镜游戏](https://image.lceda.cn/oshwhub/pullImage/855c749d18cd4e11b49cce0d0a36ffb8.jpeg)

以下是修仙面板：

![修仙面板](https://image.lceda.cn/oshwhub/pullImage/ff2444edb442451782d088f40ab767b4.jpeg)

---

# **十六、👓 近视可以戴吗**

作者自己就是近视。目前行业还没有一个很好的方法解决这个问题，大厂也基本采用 **外挂镜片** 方案，所以我们也是。未来如果该问题被突破，智能眼镜将真正具备影响力。

下图为 Btai 1 适配的 **近视镜片**：

![适配近视镜片](https://image.lceda.cn/oshwhub/pullImage/b3257544f7164e27a8e5db12c36b7db5.png)

---

# **十七、⚖️ 戴起来累不累**

如果有戴眼镜的习惯，Btai 1 **40 余克** 的重量是可接受的，与大厂产品处于同一水平；对于没有佩戴习惯的人来讲，需要时间适应，刚开始会累。

![重量展示](https://image.lceda.cn/oshwhub/pullImage/837175639f2a469cacfd793e5bbeaacb.jpg)

![佩戴展示](https://image.lceda.cn/oshwhub/pullImage/0c454a78b79648b38f56b451c68a8f5a.png)

---

# **十八、🤖 配套安卓软件**

软件使用 **Flutter** 框架开发，目前只适配了安卓。还会继续优化——毕竟目前开源出的软件功能还不完善。

![配套安卓 App](https://image.lceda.cn/oshwhub/pullImage/84aad53739f14380940998f0276c62cb.jpg)

打开软件后，底部主导航栏有 **4 个 Tab**：

1. 🏠 **主页**：快捷管理智能眼镜设备、配网、眼镜信息等；
2. 📲 **应用页**：打开 / 管理已下载的应用；
3. 🛒 **软件商店**：下载小程序 / 软件 / 智能体到智能眼镜；
4. 👤 **我的**：管理账号及各种玩法规则，加入开发者、提交帖子 / 应用。

![主导航与功能页](https://image.lceda.cn/oshwhub/pullImage/0ea9a17e98244b0994bb174db4957901.jpg)

**眼镜初次配网流程：**

![初次配网流程](https://image.lceda.cn/oshwhub/pullImage/0f35495a23f149d687ab5cd5c73f369e.jpg)

**文件传输：**

![文件传输](https://image.lceda.cn/oshwhub/pullImage/391a48f5e3d942f5910ae322dfb17530.jpg)
