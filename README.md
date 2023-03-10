# AI4S-Mapping
录音：
https://miracleplus.feishu.cn/minutes/obcnc893ba8ad1stro1tfo14?from=from_copylink

基本背景
---

<div align=center>
<image src="https://user-images.githubusercontent.com/118708553/210036227-fc22a8c9-b9a1-49a8-883c-3cb566411f78.PNG"/>
</div>

“不同的道路，是否在山顶能看到相同的月亮”？

科学
---
物理学，天文学，化学，生物，地球科学等

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036240-a2de605b-6d73-4c8a-b94c-88cd8616de55.PNG"/>
</div>


越往下越是理论驱动，越往上越是数据驱动

## 科学的核心在于观察和逻辑推理 （实验以及理论）
实验是一切的基石，所有与可重复实验结果不符合的都是错误的
逻辑推理让我们用清晰的语言，基于简单的假设去预测广泛的现象

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036248-398eedd3-89c7-43b2-b025-6d49cde3e18a.PNG"/>
<img src="https://user-images.githubusercontent.com/118708553/210036255-39bb7e98-f6dc-43af-8367-70c3d3901490.PNG"/>
</div>


## 逻辑推理将科学问题转变成计算问题
从理论层面，我们对于低复杂度的体系以及特别复杂（e.g. Omega(10^{23})）的体系可以建立很好的预测

本世纪的科学理论重点是<b>量子力学</b>

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036269-62292a88-1818-41ff-8297-de3b3edb41ac.png"/>
</div>


化学反应本质也是粒子的演化过程，可以被量子力学的语言去描述
比如我们可以写出薛定谔方程，把方程解出来我们就能得到预测（第一性原理计算）

但是，
<b>维度灾难让我们无法有效计算这些科学问题 </b>

有以下几种原因：

#### 1. 原理上讲计算就是困难的
一般来说，想计算n个粒子的体系，计算薛定谔方程的复杂度在$$O(2^{n})$$     
一个有机高分子的分子量在10^4~10^6，2^{10^4}这种天文数字不是我们能够接受的

#### 2. 复杂的体系可能蕴含着不一样的现象和理论
  - 物理学家Anderson在1972年提出“More is different” （还原论不能指导我们对于复杂体系的理解，直接带动了凝聚态物理的发展，目前已经是物理最主要研究领域之一）
  - 21世纪开始的复杂系统：简单行动规则，涌现复杂现象
        e.g. Conway的生命游戏（game of life）     动态视频可以搜索'Rule 30'
<div align=center>        
<img src="https://user-images.githubusercontent.com/118708553/210036301-83f0979b-2dcb-4792-ba95-07dc06d9091e.png"/>
</div>


#### 3. 人脑就不擅长复杂的计算（个人觉得）
  - 混沌理论（非线性）的诞生源于计算机模拟时的一次失误

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036308-46814473-0fa3-4701-868b-fd8a3ed67efa.png"/>
</div>


## 对抗维度灾难的一些尝试

#### 1. 将方程简化的近似手段
<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036314-d8de85af-c0e6-4bf5-b276-842bd1159d66.png">
</div>

计算精度
薛定谔方程 > 密度泛函 > 分子动力学
计算时间
薛定谔方程 >> 密度泛函 > 分子动力学

#### 2. 量子计算--利用量子体系直接搭建计算机
“为了模拟量子的体系，我们应该造一台量子的计算机” -- 费曼
![9](https://user-images.githubusercontent.com/118708553/210036326-7e072b45-428f-449b-92d1-540d9b27edb9.png)


总结
<b>虽然不同学科关注不同对象，但是都面对着难以处理高维问题的瓶颈。</b>

## ML
### 数据可以降低问题的难度

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036337-ec94a338-7637-4a9b-8071-83975c27a606.png"/>
</div>

### 计算能力的直观表示
直观的理解是，数据代表着我们对于一个问题的理解，我们知道这个问题的信息越多，我们就更容易去解决这个问题。

### ML的本质在于数据的处理以及学习

#### 1. 监督学习（Supervised learning）
针对于一个目标（函数），我们有一些数据并且知道对应的答案，希望通过学习这些数据之后可以给出其它的准确预测。
经典问题：“是猫还是狗？”
我们假设，存在一个真实函数，使得可以对于输入的图像或者其他东西，给出它所对应的准确分类。
通过已有的数据，我们去近似这个真实函数。

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036349-e93c4f6f-909d-4ec1-a03e-9269d2d07762.png">
</div>


#### 2. 非监督学习（Unsupervised learning）
我们有一些数据但不知道对应的答案，希望去挖掘数据内在的一些信息（比如生成这些数据的概率分布是什么，比如数据的聚类问题等等），也可能会想进一步基于学习出的答案，去生成新的数据。
经典例子：人脸学习以及生成
![12](https://user-images.githubusercontent.com/118708553/210036367-95032f8e-c3bf-4e66-958f-81053d062bfb.png)


#### 3. 强化学习（Reinforcement Learning）
我们没有数据，但我们会设置一些规则，希望通过不断的试错来让ai实现我们的目标。换句话说，ai自己会生成数据（试错）来学习，最终希望满足我们的目标。

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036380-25af14a6-2861-40b6-ae50-c878f3230955.png"/>
</div>


这三种典型方法其实都是基于数据的处理以及学习，区分在于一开始数据的不同，以及基于此我们想实现的不同的目标。

ML擅长处理高维（复杂）的问题

AI的理论基础是统计学习learning theory，主要讨论了 “如果我们想有效的给出预测，到底需要多少个数据的问题”。
一般来说，数据本身的维度，不会太影响到AI学习的有效性。

对于大量的高维函数，使用深度神经网络进行逼近时，逼近误差的速率与维度无关。因此，机器学习是处理高维问题的有效工具。

## AI for Science

### AI for 生命科学

#### 中心法则：DNA→RNA→蛋白质
  - 微观到宏观：大分子→单细胞→多细胞集群（器官）→生命体
  - 空间维度结合时间维度
#### AI能辅助做的：
  - 中心法则的一维序列、三维空间结构→预测，de novo设计→机理探究，药物研发
  - 大分子间的相互作用预测→通路→机理探究，药物研发
  - 测序技术→海量组学数据：基因组、转录组、蛋白质组、代谢组，宏组学、单细胞测序→基因表达调控解析，代谢通路的解析和构建，代谢产物的解析与合成→精准医疗，药物研发，合成生物学
  - 自动化
 #### AI模型的两个作用：
  - 海量数据的分析和挖掘：比如测序数据集、各层次的组学数据等，NLP的Lark model，embedding 等方向目前比较火。
  - 创造与生成：比如大小分子设计、crisper工具改造
####  AI模型的两种用法：
  - Domain specific：模型的设计非常关键，重点在利用模型把特定领域的数据capture，比如做单细胞测序的数据、蛋白质序列的数据
  - General：很有潜力，但由于训练数据来自自然语言，所以会出现事实上的谬误。需要关注如何grounding、如何约束在certain region里，根据真正的事实产生推理。
#### AI辅助的具体五个方向：

1. 测序技术相关
      人类基因测序完成后，测序技术推进了基因组， 转录组，蛋白质组等高通量数据的产生
  - 降低分析的时间/人力成本
  - 基于AI，可以高通量的去挖掘跨尺度、多模态的信息
  - 研究基因表达水平的调控机制 （98%碱基序列不参与编码蛋白质，但参与调控）
  
<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036404-8d3ba93f-179a-406a-99ec-7904f3a8fd78.png"/>
<img src="https://user-images.githubusercontent.com/118708553/210036411-17fbeb23-0e53-4f32-a178-e80fcb6b025e.png"/>
</div>

2. 精准医疗
  - AI辅助基因筛查来进行疾病早筛
  e.g. 产前检测、遗传风险检测和癌症早筛
  - AI辅助临床
     e.g. 计算机视觉算法辅助医学影像识别如肿瘤组织病理分型
  辅助临床治疗时靶向药物的选择，预测临床获益情况
  基因治疗

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036424-2b4938a4-0167-4c9c-a9dc-021a0cab04e9.png">
</div>


3. 药物开发
  目前药物研发的主流范式，是基于靶标与疾病的关系，开发能够干预靶标生物功能的药物分子
  - 早期生物学研究阶段：探索靶标与疾病的关系
    - 基因调控的原理发掘
    - 健康与病理多组学数据进行对比
    - 利用NLP，检索已知疾病机制已报道信息，挖掘疾病与靶点的相互联系，发现靶标相关的更多疾病，辅助发掘潜在“老药新用“的机会
  - 降低靶标成药难度
    80%-95%难成药靶标
    - 蛋白质结构解析和微观机理研究：序列-结构-动力学
    - 药物作用位点探索：位点的微观环境以及靶标蛋白的整体性质进行药物设计
  - 促进药物分子的开发
    - 苗头化合物发现：先导化合物，能靶向靶标蛋白，通过药效学评价
    - 先导化合物优化：对化合物从药效学、理化性质与药代动力学性质、毒理学等多参数优化，筛选出PCC
    - 临床前验证：药物制备工艺的优化与杂质含量的控制、晶型和剂型的确证及针对不同动物种属的药效学、药代动力学和毒理性评价
    AI辅助实验设计和数据分析
    - 临床研究：AI辅助实验设计，数据分析
数据驱动，物理模型模拟，两者结合
        e.g. AlphaFold2预测蛋白结构
  冷冻电镜数据三维结构的自动化搭建
  蛋白质结构精修
      DNA/RNA 折叠结构探索，助力药物靶点的开发

![17](https://user-images.githubusercontent.com/118708553/210036432-18a07367-5740-4c01-8db8-de2bb27dc2bc.png)

  
4. 合成生物学——DBTL
  - 自动化加速DBTL周期
  - 定量设计湿实验
  - 逆合成算法预测生物合成途径
  - 蛋白质智能设计
  - 调控元件的智能设计和优化
  - 代谢网络的智能优化
![18](https://user-images.githubusercontent.com/118708553/210036438-4404b4db-b0c8-482d-b7bf-4fdb4ecf633a.png)


5. 自动化实验——高通量全自动化实验室和云端实验室：黑灯实验室
  - 自动化是获得训练人工智能算法所需的高质量、大容量、低偏差数据的最可靠的方式，是海量工程试错的福音。
  - 发展：存量变革+增量崛起，未来5-10年会集中爆发
    - 自动化的形式在不断升级、需要更新换代，目前主要应用在药物研发、临床检验、基因组学解决方案等领域（10%）
    - 一些新的场景正在被挖掘和应用，形成一个增量市场，涉及生命科学研究、分子诊断、合成生物、细胞培养等
    - 行业大部分玩家普遍未到规模量产的阶段；在某些特定细分场景开发自动化应用
  - 类型：从辅助人到替代人的方向演进
    - 软件类
      - 数字智能实验室综合服务：物数据记录和管理，电子实验记录本，项目管理等
    - 硬件类
      - 单模块形式自动化：目前国内的主要形式
      - 工作站形式自动化：集成程度有限，百万人民币级别，包括药企、疾控中心、第三方检测中心等，代表公司有赛默飞、贝克曼、安捷伦
      - 流水线形式自动化：常见于检验科，以生化免疫为主，如贝克曼、罗氏、西门子等
      - 机器人形式智能化：目前创业公司发力点，处于早期发展阶段，未形成规模化应用，且海内外无太大差距
    - 软硬件一体化

![19](https://user-images.githubusercontent.com/118708553/210036446-195d0ba9-c4c6-4c52-b2a0-76de9e31c184.png)

      
#### AI for life science的现状：
  AI模型的通用性更强了，源自其他领域AI模型逐渐在生命科学领域发光发热，比如AIGC背后源自于图像领域的diffusion模型、大规模与训练模型等现在被用于蛋白质结构预测，用于材料科学领域的图像神经模型被用于生物大分子设计
  - AI仍带有很强的工具性，但是尚未真正推动对基础科学的研究（逻辑性学习）
需要解决的问题：
- 模型设计
  - 模型的制约在reasoning的原理性，通用大模型目前的科学推理能力较弱，原理性不足，大脑的工作原理还不明晰，也制约着大模型的设计。
- 数据
  - 某些方向的数据不够，质量、可靠性等问题尚未解决，针对这个问题，目前有考虑AI和数据建设交互机制。 
- 算力
  - 原子分子层面的结构解析需要大算力
  - 单完全依靠大算力去‘硬算’未必是最优解，可以考虑设计融合第一性原理和纯数据的混合模型框架
一些具体问题和信号
- 多细胞模拟问题：真正生物体的离子通道是非常随机的，很难模拟，找到能够验证模型的实验手段和模拟技术的平衡点，目前是一个挑战。
- 高通量实验：瓶颈主要还在湿实验，一方面实验室验证阶段耗时较长，另一方面，湿实验所提供的数据远远达不到计算模型的要求。这个方向有很多可以用AI去优化的靶点探索方法。
- 干湿算法平衡：干湿实验可以看作一个完整的loop，每一个环节都是可以优化的，一是预训练模型可以用较小数据量很好的表征模型，可以减少数据需求；二是可以通过优化湿实验，使数据迭代更快更准。三是主动ML，比如贝叶斯优化，优化实验设计。
- 壁垒：实验能力+算力，现在去做垂直领域的基础通用模型并分享，会加速整个领域的发展，这个过程中也有政府的推动，比如建立国家级实验室，能更好的将算力普及。将算力充分调动很重要，能更好的推动算法的发展，模型与应用适配很重要。

### AI for 材料科学 
![20](https://user-images.githubusercontent.com/118708553/210036459-49bbb48a-2c66-492b-a827-a1605432eea2.png)
![21](https://user-images.githubusercontent.com/118708553/210036463-0c412845-6399-48c3-9dc6-a3bc9706f928.png)

#### 1. 微观层面模拟计算 （上面已经提到）
#### 2. 合金结构搜索
  e.g. Al-Mg合金 因其轻巧型和优异的机械性能广泛应用于汽车、航空航天和电子设备行业
  什么结构能给我们最好的性质？Mg12Al8, Mg5Al27

![22](https://user-images.githubusercontent.com/118708553/210036468-ae9ed8f3-f493-4c36-8357-6f4bc03c0ca8.png)

#### 3. 催化材料
工业制品中超过 80％ 都涉及催化剂， 提高生产力降低反应要求
<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036473-e94977a3-d3ee-4a66-a572-81b60963094f.png"/>
</div>

e.g. 电解氢的催化材料 CoFeB
<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036480-0c38d13c-5c85-4f5d-a99f-134438007999.png"/>
</div>

#### 4. 高熵材料 （大于五种元素等量配置，航天核能等）
<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036494-a4387921-8d79-43dd-b63c-42c74169beff.png"/>
<img src="https://user-images.githubusercontent.com/118708553/210036497-bd6290d5-b1c1-450a-9318-9f346c221287.png"/>
</div>

#### 5. 纳米材料  e.g. 石墨烯
#### 6. 复合材料
好用工具
如 DeePMD（模型构建），ABACUS（跨尺度联动），RiD（强化采样）。此外结构搜索领域也出现了诸如 CALYPSO 这样的工具

### AI for 能源
#### 1. 燃烧以及发动机效率
![27](https://user-images.githubusercontent.com/118708553/210036505-44d104be-d21a-4255-bd62-389617cde08b.png)

#### 2. 电池 （高能量密度，高安全性，长循环寿命，高倍率）
![28](https://user-images.githubusercontent.com/118708553/210036525-bc1124a6-8276-401c-b2df-c6fdf3503ae0.png)

#### 3. 太阳能，核能

<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036543-889da718-b1b3-4f20-95dd-4d1684c32942.png"/>
<img src="https://user-images.githubusercontent.com/118708553/210036557-298326d7-c139-45b3-9dc9-00b20adc0b7c.png"/>
</div>

### AI for 地球科学
#### 1. 同位素扩散过程
![31](https://user-images.githubusercontent.com/118708553/210036569-07469aae-97fe-44af-8ef4-3f454947d738.png)

#### 2. 天气预测
![32](https://user-images.githubusercontent.com/118708553/210036573-250d982b-d724-4477-a9d4-8dc44708307b.png)

###AI for 天文学
#### 1. AI+天文望远镜数据，寻找新行星
例子：谷歌处理了开普勒望远镜4年来记录的图像中的140亿个数据点，发现在我们所在的太阳系之外，还存在另一个拥有8颗行星的太阳系。
![33](https://user-images.githubusercontent.com/118708553/210036583-85522e6e-8e34-4c84-8ce2-9218d4fb3c70.png)

#### 2. AI查看海量天文图片，寻找“引力透镜”
当宇宙中一个巨大的物体（通常是一个星系或黑洞）出现在一个遥远的光源和地球上的观测点之间时，它会使空间和光线在其周围环绕，形成一个“镜头”，就像“太空望远镜”一样，让天文学家得以更近距离的观察此前看不到的宇宙中古老而遥远的部分。这就是“引力透镜”，它对天文学家研究宇宙暗物质产生的引力效应非常重要。
![34](https://user-images.githubusercontent.com/118708553/210036587-ed8e71d3-360a-40a0-b843-f15568080ad2.png)

#### 3. AI可以创造信息，填补宇宙观测的盲点
比如通过生成式对抗网络GAN，AI可以大幅改善模糊的天文望远镜照片，甚至可以用来发现黑洞。
![35](https://user-images.githubusercontent.com/118708553/210036590-f57cc8ff-5fa0-427f-8d83-3f09ebd9a0cf.png)

从科学的角度来说，AI for Science其实就是使用新的方法，去更好的挖掘数据的内在关系，以及从learning的角度去更深的理解自己关注的体系。
从AI的角度来说，是AI可能落地的方向之一。重点还是在科学这边。
![36](https://user-images.githubusercontent.com/118708553/210036594-1c9d38af-4042-4342-be5b-3e742a30948d.png)

让我们重新回顾一下科学的阶层结构
<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210036611-6ac4920b-9589-4e70-8db3-8d1377f0010d.png"/>
</div>

越往上越是数据驱动，越往下越是逻辑推理驱动。

### 小结
1. 大规模数据处理
![38](https://user-images.githubusercontent.com/118708553/210036635-8f6e6c95-0285-400e-b71b-6f25ba4512e8.png)

蛋白质折叠是一个典型的高维问题，通过AI有了非常好的突破 （AlphaFold2）
以前也有生物物理学家研究理论视角的相关研究，但AlphaFold2很好的体现了数据驱动的优越性。

除此之外，其实欧洲的核子研究中心CERN，非常早就有使用ML的方法来进行数据处理。现在也有很多实验组，使用ML的方法来对于自己的实验数据进行处理。


2. 高精度模型求解
![39](https://user-images.githubusercontent.com/118708553/210036654-0c0db1af-3814-48b0-a570-acf42e5147b2.png)

传统分子动力学的方程求解，有一定的经验参数在里面，导致精度较低。
第一性原理的密度泛函计算精度会高一些，但是计算时间很长。
通过学习第一性原理计算得来的数据，用深度神经网络来对于高维的经验参数进行耦合，可以得到很好的结果。（相关研究获得了2020年高性能计算的最高奖 戈登贝尔奖）
可以模拟每天超过1亿个原子的超过1纳秒长的轨迹

3. 模型求解+数据处理
暂无经典例子

4. 概念方面的融合
量子力学提供了将科学问题转化为算法等等问题的途径。
  - 信息论与量子论融合在一起，诞生了量子信息 
  - 算法理论，复杂性与量子论融合在一起，诞生了量子计算
  - AI与量子论融合在一起，可以诞生？
    A. 从可学习性的角度去了解量子体系 （数值有不少结果，理论正在发展）
    B. 量子计算能否加速AI计算过程 （已有一些结果）
    C. xxx
![40](https://user-images.githubusercontent.com/118708553/210036718-9d17b3bf-5632-4dfc-baa3-6b9147111001.png)

### AI做科学家？第五范式？

#### 1. AI 能成为科学家么？
目前ML主要基于数据的统计相关性来进行建模拟合。
统计相关性分以下三种：
![41](https://user-images.githubusercontent.com/118708553/210038784-b4b35322-7e96-4f22-b0bf-0e8b1dabcc1f.png)

 <div aliagn=center>
  因果，混淆，样本选择偏差
</div>

其中只有因果关系这种结构是稳定的，可解释的。
目前盛行的深度学习等方法，无法进行因果推断，更无法实现通用人工智能（AGI）。
最近很火的大模型 （GPT-3，4还是DALL-E），面对AGI的目标，我认为只是在错误的方向上狂飙。
深度学习的大佬们（图灵奖们）近几年也在尝试拨乱反正，希望回归正确的AGI发展道路。
AGI如果实现，成为科学家这个说法是可靠的。

#### 2. AI4S是科学的第五范式？
![42](https://user-images.githubusercontent.com/118708553/210038712-e7d7d830-e71b-4607-a060-2ea1685ffab6.png)


微软研究院和IBM提出AI4S是科学的第五范式。
有待商榷，至少学界很多人还不太认可。

从科学和技术发展来说，AI应用到Science是十分自然的考虑。
在AI与科学的结合发展上，我对其中蕴含的巨大潜力充满信心。
总结

### What
用ML技术对于科学的应用
### Why
基本每个学科都面对着高维问题计算困难，希望新的方法解决
对于数据驱动的学科，需要更好的手段处理数据
新的概念，认知想法的出现
### How
AI大规模数据处理
AI高精度模型求解
AI理论融合
### Why now
硬件的驱动下，AI技术的成熟
AI促进干实验飞速发展需要更多更快的湿实验验证
实验技术的进步导致更多数据需要处理
### Why us
AI4S是非常大而且不是很成体系的赛道，挖掘人才的时候，需要去关注所对应学科的研究室。
AI4S我认为是科学为主，而非AI。AI只是技术上驱动科学发展的手段。
人才往往集中在鼓励交叉学科的研究所，高校以及公司等
比如Caltech等有在推出AI4S的Program，可以关注

值得重点关注的公司是Deepmind以及国内的深度势能；以及海外大厂的研究所

### 发展阶段预测
#### 1.  以科学家为主导的概念导入期
    我认为公司需要一位首席科学家，同时高度掌握AI以及某一门科学
#### 2.  以科学家和工程师协作为标志的大规模基础设施建设期
#### 3.  以工程师为主导的应用期

### 第三阶段的机会主要是在
- 新计算工具定义新研发流程
- 软件定义硬件
最近参加的很多学会上发现物理学家们打算使用ai优化实验装置搭建，软件定义硬件或许会更早发生？

### 贡献名单
郭乃绪，落落（陈军玉），Jack，杨婧， 李湃 




<div align=center>
<img src="https://user-images.githubusercontent.com/118708553/210037473-7ee0ac08-02a6-421c-85ef-07333c984445.png">
</div>

### 相关文章推荐

AI 4 Science https://github.com/wangzuzihan/AI4S/blob/main/README.md

AI4Science @ Caltech https://www.ai4science.caltech.edu/

How AI is helping the natural sciences  https://security.feishu.cn/link/safety?target=https%3A%2F%2Fwww.nature.com%2Farticles%2Fd41586-021-02762-6&scene=ccm&logParams=%7B%22location%22%3A%22ccm_docs%22%7D&lang=en-US

你真的了解计算生物学和AI for Science吗?https://www.msra.cn/zh-cn/news/features/qbitai-ai-for-science

A new technique speeds up deep neural networks for selecting proton–proton collisions  https://security.feishu.cn/link/safety?target=https%3A%2F%2Fhome.cern%2Fnews%2Fnews%2Fphysics%2Fspeeding-machine-learning-particle-physics&scene=ccm&logParams=%7B%22location%22%3A%22ccm_docs%22%7D&lang=en-US


