## 第一章：音乐的表现形式

> 我们跳过`1.1`和`1.2`的乐理相关内容，直接进入[`1.3`](#13-音频表现形式)。
> 大概带过一下，就是说本章的前三节主要介绍了3种音乐表现形式：
> `1.1` **乐谱 (sheet music)**
> `1.2` **符号 (symbolic)**
> `1.3` **音频 (audio)**

> **sheet music(乐谱)** 大家应该很熟悉了，就是五线谱、吉他谱之类的，一般指纸质的乐谱；<u> **symbolic(符号)** (翻译有点勉强)，代表所有能被计算机识别的，能表现音乐实体的数据</u>，比如midi文件，musicxml乐谱，cubase工程文件等等。audio(音频)，说白了就是平时在电脑和手机里听的音乐文件，常见格式有比如mp3，WAV等等。

### 1.3 音频表现形式

音乐不仅仅是对那些音符的演奏说明(比如乐谱)。音乐是关于如何制造、创造和塑造声音的。当音乐家们开始钻研音乐时，那些演奏说明就退回到了他们最初的背景中：音乐节拍有节奏地流动，不同的音符对象融合成和谐的声音与流畅的旋律线，乐器之间也在相互交流。音乐家把情感加入到他们的音乐中，通过不断调整节奏、力度和情感表达来与音乐交互。他们不是机械地演奏，而是在某些时点上加快速度，在另一些时点上放慢速度，以塑造一段音乐。同样地，他们不断地改变声音的强度并强调某些音符。所有这些，使得这段音乐能够被独特表演和诠释。  

从物理学的角度来看，演奏音乐会产生 **声音(sounds)** 或 **声波(acoustic waves)** ，这些声音或声波以压力振荡的形式通过空气传播。 **音频(audio)** 用于指在人类听力范围内的声音的传输、接收或再现。 **音频信号(audio signal)** 是声音的一种表现形式。与 **乐谱(sheet music)** 和 **符号表示(symbolic representations)** 不同，音频表现形式是对再现一段音乐的声学实现所需的所有信息进行编码。这包括构成音乐家特定表演风格的时间、动态和音调上的细微偏差。然而，在音频表示中，诸如开始时间、音调或音符持续时间等音符参数并没有明确给出。这使得音乐信号的分析和比较成为一项困难的任务，特别是在复调音乐中，不同的乐器和声音相互叠加。此外，对声音的感知不仅取决于声波的客观特性，还取决于一些主观标准，这是人类耳朵和大脑对声音进行复杂处理的结果。关于人类主观声音感知的研究被称为 **心理声学(psychoacoustics)** ，更多细节请见文献[5, 17]。在本节中，在了解了波和波形之后，我们总结了音频表示的最重要特性：频率和音调、动态(力度变化)、强度和响度，以及音色。


#### 1.3.1 波和波形

声音是由振动的物体所产生的，比如歌手的声带、小提琴的弦和音板、鼓的振膜和音叉的尖头等等。这些振动引起空气分子的位移和振荡，导致局部区域的空气被压缩和稀释。交变压力以波的形式在空气中传播，从它的来源传到听者或麦克风。当声音传播到目的地，人类听到后便能被感知到，或通过麦克风将其转换为电信号(见[图1.17](#fig1.17))。对于人类听者来说，耳朵的外部捕捉声波并将其传递到鼓膜，然后鼓膜根据空气的压力振荡进行相应的振动。在经过中耳和内耳的进一步处理之后，声波被转换成神经脉冲，这些神经脉冲最终被发送到大脑并被大脑解释。从图形上看，某个位置的气压变化可以用 **压力-时间图(pressure–time plot)** 表示，也称为声音的 **波形(waveform)** 。波形显示空气压力与平均空气压力的偏差。[图1.18](#fig1.18)显示了贝多芬第五交响曲录音的波形。

<span id="fig1.17"></span>
| ![](https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228201825.png) | 
|:--:| 
| *图1.17 振动的音叉致使周围空气粒子来回振动。压力振荡以纵波形式在空气中传播。波形显示了特定位置(如麦克风所示)的平均空气压力随时间的偏差* |

<span id="fig1.18"></span>
| ![](https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228214042.png) | 
|:--:| 
| *图1.18(a)贝多芬第五交响曲前五小节录音的前八秒波形(b)波形在7.3-7.8秒之间放大截面* |

一般来说，一个机械波可以描述为在空间中传播的一种振荡，能量从一点传递到另一点。当波通过某种介质时，构成这种介质的物质会暂时发生形变。如上所述，声波通过空气分子与其邻近的分子碰撞来传播。空气分子碰撞后，它们相互反弹(一种回复力)。这可以防止分子继续沿着波的方向运动。事实上，它们在几乎固定的位置上振荡。一般波可以是横向的，也可以是纵向的，这取决于它的振荡方向。当扰动产生与传播(能量传递方向)垂直(成直角)地振荡时，就会产生横波。当振荡与传播方向平行时，会出现纵向波。根据这个定义，弦中的振动是横波的一种情况，而声波的形式是纵波。横波实际上可以产生纵波，反之亦然。乐器的弦在两个固定端点之间振荡时(横波)，会逐渐向空中发射能量，从而产生纵向的声波。如果该声波撞击了人耳的鼓膜，则会反过来再次产生横波。

> 这一小节主要说明了声音是由空气振动产生的。判断一个机械波是横波还是纵波，只需看介质中粒子的振动方向和声音的传播方向之间的关系。声波是纵波，乐器的弦和人耳的鼓膜里的声波都是横波。


#### 1.3.2 频率和音调

我们已经看到声波可以用波形直观地表示。如果高气压点和低气压点以交替且规则的方式重复，则称由此产生的波形为 **周期性的(periodic)** 。在这种情况下，波的 **周期(period)** 定义为完成一个周期所需的时间。 **频率(frequency)** 以 **赫兹(Hertz，简写为Hz)** 为单位，是周期的倒数。[图1.19](#fig1.19)显示了一个 **正弦波(sinusoid)** ，这是最简单的一种周期波形。在此示例中，波形的周期为四分之一秒，因此频率为4Hz。正弦波完全由其频率、 **振幅(amplitude)** (正弦波与平均值的峰值偏差)和 **相位(phase)** (确定其周期中正弦波在时间零点的位置)来确定。在分析一般音频信号时，正弦曲线的这三个属性将变得非常重要(见第`2.3`节)。

> 正弦波的三个重要的属性：频率(或周期)、振幅、相位。

<center>
    <img id="fig1.19" style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228214755.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">
    图1.19 频率为4Hz的正弦波波形
    </div>
</center>

正弦波的频率越高，听起来就越“高”。人类的听觉频率范围在20Hz到20kHz之间。其他物种有不同的听力范围。例如，狗狗的听觉范围上界约为45 kHz，猫的听觉范围上界约为64 kHz，而蝙蝠甚至可以检测到超过100 kHz的频率。这就是为什么人们可以使用狗口哨来训练和指挥动物，而不会打扰附近的人。狗口哨发出的 **超声波(ultrasonic sound)** 超出了人类的听觉能力。

正弦波可以被认为是音乐音符声学实现的原型(后面会解释)。有时，由正弦波产生的声音被称为 **谐波(harmonic sound)** 或 **纯音(pure tone)** 。如第`1.1.1`节所示。频率的概念与决定音高的因素密切相关。一般来说，音高是声音的主观属性。对于复杂声音的混合，其与频率的关系可能特别模糊。然而，就纯音而言，频率和音高之间的关系是明确的。例如，频率为440Hz的正弦波对应的音高为A4，这个特殊的音高也被称为 **音乐会音高(concert pitch)** ，它被用作一组乐器在演奏时的参考音高。由于频率的微小变化不一定会导致人耳感知的变化，因此人们通常会将整个频率范围与单个音高联系起来。

> 音高A4(对应频率440Hz)也叫音乐会音高、参考音高、基准音高，是最重要的一个音高。
> 音高本身是表示一个频率区间，比如音高A4，其实是表示包括440Hz的一条“带”，这条带的中心频率为440Hz，因此有时候会用音高指代其中心频率，但是读者已应该内心知道两者之间的细微差别。

如第`1.1.1`节所述，如果两个频率相差二的某个幂次的倍数，则认为它们是相似的，这引出了八度音程的概念。例如，音高A3(220Hz)、A4(440Hz)和A5(880Hz)听起来相似。此外，音高A3和A4之间的感知距离与音高A4和A5之间的感知距离相同。换句话说，人类对音高的感知本质上是对数的(非线性)。这种人类感知的属性实际上已在第`1.1.1`节中涉及到，在那一节种我们定义基于对数频率轴将八度音阶细分为十二个半音的等调音阶(十二平均律)。更正式地说，使用第`1.2.2`节中介绍的MIDI音符来编号，我们可以将每个音调 $p\in[0,127]$ 映射为其 **中心频率(center frequency)** $F_{\text{pitch}}(p)$ (以Hz为单位)：

$$
F_{pitch}(p) = 2^{\frac{p-69}{12}}\times 440
$$

事实上，对于参考音高 $p=69$ (A4)来说，由该公式可以得出其对应的频率为 $F_{\text{pitch}}(p)=440$ 。将音高增加12(一个八度)将导致频率增加2倍，即 $F_{pitch}(p+12)=2 \cdot F_{\text{pitch}}(p)$ 。同样，很容易证明相邻两个音高 $p+1$ 和 $p$ 之间的频率比为一个常数(见练习1.6)：

$$
F_{\text {pitch}}(p+1) / F_{\text {pitch}}(p)=2^{1 / 12} \approx 1.059463
$$

换句话说，将任意音高的中心频率乘以这个常数，音高就会增加一个半音。 **音分(cent)** 表示用于音乐音程的对数度量单位。根据定义，一个八度音阶可以分为1200音分，因此每个半音对应100音分。同样，频率间隔为1音分之间比值是恒定的，这个比值为

$$
2^{1 / 1200} \approx 1.0005777895,
$$

两个频率(用 $\omega_1$ 和 $\omega_2$ 表示)之间的音分之差由下式给出:

$$
\log _{2}\left(\frac{\omega_{1}}{\omega_{2}}\right) \cdot 1200.
$$

一音分的间隔太小，以至于人耳无法分辨之间的差异。刚刚能引起差别感觉的刺激的最小差异量，也被称为 **差别感觉阈限(just noticeable difference)** ，因人而异，并取决于其他方面，如音色(第`1.3.4`节)和听者的音乐背景。根据经验，正常成年人能够非常确信地识别25音分的音高差异，只有经过训练的听众才能识别10音分的音高差异。

现实世界中的声音远不是一种有明确频率的简单的纯音，或者说。在乐器上弹奏单个音符可能会产生复杂的声音，其中包含随时间变化的不同频率的声音的混合。直观地说，这样的 **乐音(musical tone)** 可以被描述为纯音或正弦波的叠加，每个纯音或正弦波都有自己的振动频率、振幅和相位。 **分音(partial)** 指的是构成乐音的成分中的任何一种正弦波。对于频率最低的那个分音，其频率称为声音的 **基频(fundamental frequency)** 。音调的高低通常由该乐音的基频决定，基频是由乐器的弦或气柱的全长振动产生的频率。 **泛音(harmonic)** 是频率为基频整数倍的分音。分音以及泛音沿频率轴向上计数。这个惯例意味着基频是一个乐音的第一分音，也叫第一泛音。术语 **偏差音(inharmonicity)** 用于表示分音与最近理想泛音之间偏差的度量，通常每个分音的度量单位为音分。最后，音乐理论中经常使用的另一 个术语是**陪音(overtone)**，泛音是除最低分音以外的任何部分。当比较泛音和分音时，可能会导致编号的混乱，因为第一泛音其实指的是第二分音。

> 这一段概念比较多，需要消化一下。[关于泛音的一些直观解释](https://www.zhihu.com/question/360020228/answer/933611257)。

大多数音高乐器都设计为具有接近泛音的分音，不和谐度非常低。因此，为了简单起见，人们经常将这些乐器声音中的分音称为泛音，即使它们有一些不和谐。其他音高乐器，特别是某些打击乐器，如马林巴琴、颤音琴、铃铛和铜鼓(定音鼓)，含有非泛音的分音，但给耳朵一种良好的音调感。无音高或不定音高的乐器，如钹、锣或铜锣，发出的声音充满不和谐的分音。作为泛音声音的一个示例，[图1.18](#fig1.18)在其下部显示了7.3和7.8秒之间部分波形的放大，这揭示了声音信号大多具有周期性。在这500毫秒内的波形对应于一个衰减中的D音，由管弦乐队在第四和第五小节中齐声演奏所产生(见图1.1)。实际上，在这个部分中，我们可以统计出共有37个周期，对应于74Hz的频率，即D2的基频。

> 最后一句的解释：[图1.18(b)](#fig1.18)包含7.3~7.8共0.5秒的声音讯号，而这0.5秒中，我们可以数一下，发现一共有37个完整的周期，因此声音每运行一个周期需要的时间为0.5/37=1/74。而频率为周期的导数，即74Hz。

我们通过观察乐音中的泛音，来结束这一小节关于频率和音高的部分。用 $\omega$ 表示一个音符的中心频率，例如，对于C2，$\omega=65.4$ Hz(C2的MIDI音符编号为p=36)。泛音序列是一个算术级数 $\omega,2\omega,3\omega,4\omega,\dots$ ，其中相邻泛音之间的差值为常数 $\omega$ 。由于我们对音高的感知在频率上是对数的，我们的听觉会认为高频泛音之间比低频泛音之间“更接近”。另一方面，八度音程序列是一个几何级数 $\omega,2\omega,4\omega,8\omega,\dots$ ，我们听到这些距离在音乐间隔的意义上是“相同的”。因此，根据我们听到的声音，泛音序列中的每个八度音程被划分为越来越“小”和越来越多的间隔。在我们的例子中，二次泛音($2\omega$)听起来像C3(高出一个八度)，三次泛音($3\omega$)听起来像G3(在C3之上的所谓纯 **五度(perfect fifth)** )，四次泛音($4\omega$)听起来像C4(高出两个八度)。从C2开始，[图1.20](#fig1.20)显示了前16次泛音根据泛音频率得到的距离最近的音符，以及这些泛音和(1.1)中规定的音符中心频率之间的差异(另见练习1.9)。例如，三次泛音的频率仅比G3的中心频率高出2音分，这比差别感觉阈限要小得多。相比之下，第11次泛音的频率比音符 $F^{\sharp}5$ 的中心频率低49音分，这几乎为半个半音，清晰可辨。如果泛音被转换成一个八度音程(通过适当地将频率乘以或除以二的幂)，它们近似于十二平均律中的某些音符。十二平均律中的一些音近似得比较好，比如C(一次泛音，差0音分)、G(三次泛音，差+2音分)或D(九次泛音，差+4音分)，而其他音则存在问题，如 $F^{\sharp}$ (十一次泛音，差-49音分)、 $A^{\flat}$ (十三次泛音，差+41音分)或 $B^{\flat}$ (七次泛音，差-31音分)。

<center>
    <img id="fig1.20" style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228223717.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">
    图1.20 泛音序列的图解。从音符C2开始，对于前16个泛音中的每一个，显示最接近的音符。顶部显示了泛音频率与最近音符的中心频率之间的差值（单位：音分）
    </div>
</center>


#### 1.3.3 动态、强度和响度

如第`1.1.2`节所述，音乐的另一个重要特性涉及 **动态(dynamics)** ，动态是一个通用术语，可以用于指声音的音量，同时也是一个表示音量大小的音乐符号。例如， **弱音(piano)** (记为 $\mathcal{p}$ )表示音符要轻弹，而 **强音(forte)** (记为 $\mathcal{f}$ )表示音符要大声弹。除了 $\mathcal{p}$ 和 $\mathcal{f}$ ，乐谱中还有很多用来描述音符动态的符号，这里不再叙述。在音频方面，动态与一种称为 **响度(loudness)** 的感知特性相关，响度也是一种对声音大小的度量方式，通过响度，声音可以在从安静到响亮的范围内有序排列。与音高和频率之间的关系类似，响度是一种主观的度量方式，与 **声强(sound intensity)** 和 **声功率(sound power)** 这两种客观测量相关。然而，响度还取决于其他声音特征，如持续时间或频率。在仔细研究客观度量标准之后，我们再回过头来看这个主观度量。

> 乐谱中可以用一些特殊符号来表示动态，具体体现在演奏中就是演奏的力度大小。动态本身也是一个声学中的术语，用于刻画声音音量的大小。响度是一种声音大小的度量方式，但是涉及一些人的主观因素，和人的具体听感有关；声音强度和声音功率都是客观的声音大小的度量方式，和人的具体听感无关。

从物理学角度来看，严格定义声音的强度或功率并不容易。下面，我们只给出一些直观的解释。一般来说， **功率(power)** 是能量被传输、使用或转换的速率。功率以 **瓦特(watt)** (简写为W)为单位进行测量，瓦特(W)定义为焦耳/秒。例如，灯泡将电能转换为热能和光的速率是以瓦特为单位来测量的，瓦特数越大，功率越大，或者相当于单位时间内使用的电能越多。类似地， **声功率(sound power)** 表示声源在空气中向各个方向传播时每单位时间释放的能量。 **声强(sound intensity)** 用于表示单位面积的声功率。

在实际中，对于人类日常听到的那些声音，这些声音的声功率和声强一般都是非常小的值。例如， **听阈(threshold of hearing，TOH)** 是人类能听到的纯音的最小声强，它小到
$$
I_{TOH} := 10^{-12} W/m^{2}.
$$

此外，人类可以感知的声强范围非常大， $I_{TOP} := 10W/m^{2}$ 为 **疼痛阈值(threshold of pain，TOP)** 。出于实际应用考虑，人们会切换到对数刻度来表示声功率和声强。更准确地说， 我们使用 **分贝(decibel，dB)** 刻度，这是一个对数单位，表示两个值之间的比率。通常，其中一个值作为参考值，例如在声强情况下的 $I_{TOH}$ 。这样的话，以dB为单位度量的声强定义为

$$
\mathrm{dB}(I):=10 \cdot \log _{10}\left(\frac{I}{I_{\mathrm{TOH}}}\right).
$$

根据该定义，可得到 $\mathrm{dB}(I_{\mathrm{TOH}})=0$ ，强度每增加一倍可增加约3 dB：

$$
\mathrm{dB}(2 \cdot I)=10 \cdot \log _{10}(2)+\mathrm{dB}(I) \approx 3+\mathrm{dB}(I).
$$

当以分贝为单位规定声强时，我们也会提到 **声强级(intensity levels)** 。表1.1显示了一些典型声音的声强，单位为 $W/m^{2}$ 和对应的分贝数。例如，演奏 **轻低音(pianissimo)** 的音符通常会产生约40dB的强度级别，而演奏 **重低音(fortissimo)** 的音符可以达到高达100dB的级别。

<span id="fig1.17"></span>
| ![](https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228231812.png) | 
|:--:| 
| *表1.1 以$W/m^2$(声强)、分贝(声强级)以及与TOH相比的系数给出的典型声强值。* |

现在我们回到 **响度(loudness)** 这一概念。如前所述，响度受到许多因素的影响。首先，根据个人的不同，同一个声音可能被认为具有不同的响度。比如，年龄就是影响人耳对声音反应的一个因素。此外，声音的持续时间会影响感知，因为人类听觉系统会在长达一秒的时间间隔内平均化声音强度的影响。因此，人类感觉持续200ms的声音比仅持续50ms的类似声音更响亮。此外，两个强度相同但频率不同的声音通常不会被认为具有相同的响度。听力正常的人对2000~4000Hz左右的声音最敏感，对低频和高频的敏感度都会下降。基于心理声学实验，纯音的感知响度取决于频率，并用单位phon表示。[图1.21](#fig1.21)显示了 **等响度曲线(equal loudness contours)** 。每条等高线都固定了响度(响度作为外生变量)，以phon为单位，在(对数间隔的)频率轴上指定声音强度(单位dB)。phon的单位相对于1000Hz的频率进行标准化，其中phon值等于以dB为单位的强度水平。0 phon的轮廓显示了听力阈值如何取决于频率。

> “phon的单位相对于1000 Hz的频率进行标准化”这句话的意思是，在x轴1000Hz的地方，让声音响度的值恰好等于声音的频率。

<center>
    <img id="fig1.21" style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228232153.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">
    图1.21 等响度曲线
    </div>
</center>

#### 1.3.4 音色

除了音高、响度和持续时间之外，声音还有一个基本特征，即 **音色(timbre 或 tone color)** 。音色使听者能够区分小提琴、双簧管或小号所产生的声音，即使这些乐器都以相同的音高和响度来演奏。与音高和响度一样，音色也是声音的感知属性。然而，音色很难把握，而且由于其模糊性，通常以间接的方式来描述：音色是一种属性，听者可以使用除音高、响度和持续时间以外的任何标准来判断两种声音是否不同。例如，音色信息允许我们区分双簧管和小提琴发出的声音，即使声音的音调和响度相同。乐器的声音可以用明亮、黑暗、温暖、刺耳等词来描述。研究人员试图通过观察与更客观的声音特征的相关性来接近音色，如 **temporal and spectral evolution(待翻译)** 、音调和噪声成分的存在或不存在，或分音各部分的能量分布。在下文中，我们将更仔细地了解其中一些特征。

当敲击钢琴键时，产生的声音远不止是与基频及其泛音相对应的一些纯正弦波的叠加。演奏单个音符已经产生了复杂的声音混合，其特征可能会随着时间的推移而不断变化，包括周期性和非周期性成分。在一个乐音开始时，能量通常会突然增加。在这个短暂的阶段，音的 **起音阶段(attack phase)** ，声音逐渐增强。它包含高度非周期性成分，这些成分分布在整个频率范围内，这也是 **噪声(noise)** 固有的特性。在声学中，这种在波形开始时出现的短持续时间的高振幅声音也被称为 **瞬态(transient)** 。就钢琴而言，在锤子敲击一根或几根琴弦之前，敲击一个键会触发整个机械的一系列连锁反应。所有这些动作，从手指触键开始，到锤子敲击琴弦结束，都会产生机械噪音，与琴弦激发的声学效果相融合。在起音阶段之后，乐音的声音开始稳定( **衰减阶段(decay phase)** )，并以(或多或少)周期的模式达到稳定阶段。这第三个阶段，也被称为 **持续阶段(sustain phase)** ，构成了乐音的大部分持续时间，其中能量或多或少保持不变或略有减少。在乐音的最后阶段，也称为 **释音阶段(release phase)** ，乐音逐渐消失。对于钢琴来说，这一阶段在手指离开琴键和阻尼器阻止琴弦振动时开始。

直观地说，波形的 **包络(envelope)** 可以看作是一条平滑曲线，大致勾勒出了其振幅的极值(见[图1.22a](#fig1.22))。如上所述的不同阶段对乐音包络的形状有很大的影响。在声音合成中，要生成的信号包络通常由一个称为ADSR的模型来描述，该模型由起音(A)、衰减(D)、持续(S)和释音(R)阶段组成(见[图1.22b](#fig1.22))。四个相位的相对持续时间和振幅对合成音的发声方式有很大影响。

<center>
    <img id="fig1.22" style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228232412.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">
    图1.22(a)信号包络 (b) ADSR包络的示意图
    </div>
</center>

ADSR模型是一个很强的简化模型，对某些乐器产生的音调的振幅包络只产生有意义的近似值。例如，[图1.23a](#fig1.23)所示的乐音，即钢琴上弹奏的音符C4，由ADSR模型得到的信号包络和原始音频的振幅包络非常相似。在一次尖锐的起音(当锤子敲击琴弦)和一个稳定的衰减之后，音不断地消失。在钢琴发音的情况下，只要阻尼器不接触琴弦，声音强度的降低就会非常缓慢。因此，可以将该阶段视为一种持续阶段。当钢琴键松开，阻尼器停止琴弦的振动时，声音很快结束。然而，对于其他乐器，振幅可能以完全不同的方式演变。[图1.23b](#fig1.23)说明了这一点，其中显示了小提琴演奏的音符C4的声音信号包络。首先，由于声音是随着音量的逐渐增大而柔和地发出的，因此起音阶段随时间缓慢地进行。此外，似乎没有任何衰减阶段，随后的持续阶段也不稳定；相反，振幅包络线以规则方式振荡。当小提琴手停止拉动琴弦时，释音阶段开始。然后声音很快就消失了。

<center>
    <img id="fig1.23" style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/acgmusic/FigureBedForFmp/master/img/20211228232542.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">
    图1.23 不同乐器演奏同一音符C4(261.6 Hz)的波形、振幅包络和频谱图表示。(a)钢琴(b)小提琴
    </div>
</center>

以小提琴为例，我们可以观察到振幅的周期性变化。这种现象称为 **震音(tremolo)** ，是由弦乐或管乐器的某些演奏风格产生的。震音的效果通常伴随着 **颤音(vibrato)** ，颤音是一种由频率的有规律的脉冲变化造成的音乐效果。除了弦乐之外，颤音主要被人类歌手用来增加表现力。在技术术语中，震音对应于 **振幅调制(amplitude modulation)** ，而颤音对应于 **频率调制(frequency modulation)** 。震音和颤音都取决于两个参数：振幅(和频率)变化的程度和变化的速率。尽管震音和颤音只是强度和频率的局部变化，但它们不一定会引起整体音的响度或音调的感知变化。相反，它们是影响音色的特征。

> vibrato是音高的规律性改变，而tremolo则是音量的规律性改变

也许表征音色最重要和最著名的属性是某些分音的存在及其相对强度。回顾第`1.3.2`节，分音是构成乐音的主要频率，最低分音是基频。偏差音表示分音偏离最近理想泛音的程度。对于泛音，例如具有清晰可感知音调的乐音，大多数偏音接近于泛音。然而，并不是所有的分音都需要以相同的强度出现，我们将在稍后看到。

 **声谱图(spectrogram)** 显示了一段时间内频率的强度，可以通过声谱图直观地显示声音的组成部分。有关此类时间-频率表示的详细介绍，请参阅第`2.5`节。[图1.23a](#fig1.23)在底部显示了钢琴上弹奏的音符C4的声谱图，其中强度通过灰色阴影来表示(颜色越深，强度越高)。音符的基频(261.6 Hz)和泛音(261.6 Hz的整数倍)，都可以作为水平线被看到。乐音的衰减通过每个分音的相应衰减来反映。音的大部分能量都包含在较低的分音中，而较高分音的能量往往较低。这种声音能量的分布是许多乐器的典型分布。

对于弦乐器，声音往往具有丰富的分音频谱，其中大量能量也可能包含在高次泛音中(见[图1.23b](#fig1.23))。该图还显示了颤音在时间-频率图上的规则振荡。某些种类的管乐器，包括单簧管(所谓的闭管乐器)产生了非常独特的分音谱。对于一端打开，另一端关闭(在吹口处)的圆柱形管乐器，可以证明偶数泛音不会出现。换句话说，大部分能量包含在奇数泛音 $\omega_{0},3\omega_{0},5\omega_{0},\dots$ ，其中 $\omega_{0}$ 表示基频。对于在巴松管上演奏的乐音，基频通常比高次分音包含的能量少得多。相反，对于音叉来说，大部分能量都包含在基频中，从而产生接近合成正弦波的声音。像铃铛这样的乐器有着非常复杂的频谱，有着许多不和谐的地方，这常常让听者产生铃铛走调的感觉。对于弦乐器，人们通常可以测量到高次泛音和理论泛音之间的大量偏差。绳子的弹性越小(即，绳子越短、越粗、张力越高或越硬)，它可能表现出的不和谐性就越大。这对钢琴尤其适用，因为这种不和谐对音色有着至关重要的影响。

通过这一讨论，我们想指出音色是一种难以测量的多维现象。正是这种不规则和变化使音乐听起来有趣，并赋予它一种特殊和自然的品质。

