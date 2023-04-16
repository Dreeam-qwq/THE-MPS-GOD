# THE-MPS-GOD

**在阅读之前，请各位：感恩🙏🙏🙏🙏**

**墨门🙏🙏🙏🙏**

**🙏🙏🙏🙏🙏🙏🙏🙏 蘑菇蓝先生维护好几个服务端还负债累累，依然夜以继日精益求精废寝忘食的给我们带来全球首款多线程重写版高并发服务端：MPS 🙏🙏🙏🙏🙏🙏🙏🙏**

**墨老如此努力工作，你怎么能诋毁他！！！没有他，你怎么开得了服务器！！！！**

**让我们再次感恩：墨门🙏🙏🙏🙏**

**本人不是也不打算成为国内 Minecraft 服务器圈子的成员。我只是做为一个围观者，发表我合理的批判。**

**关于作者：Minecraft 修改版服务器软件 KeYiMC 开发者。(由于我实在无法忍受国内服务器圈子的恶臭环境，KeYiMC 已经弃坑。)**

**本文不做任何排版，若您感到不舒服请停止阅读。**

**本文含有大体积图片，请确保您连接到 GitHub 的网络通畅无阻，否则会影响您的阅读体验。**

## 前情提要

本文中出现的所有人名均指代以下人士。为了对方的隐私安全，故不放出 QQ 号与昵称。

### 莫老

![image](https://user-images.githubusercontent.com/53771072/232274527-27858c4c-4d40-406f-b2ae-860ed14b8d82.png)

## Sakura 女士

![image](https://user-images.githubusercontent.com/53771072/232274401-e8af3c99-07a2-4a75-8935-1f3b222f67cc.png)

## 收银员

![image](https://user-images.githubusercontent.com/53771072/232274411-ded156bf-d0f0-497d-8f52-24618d906ccb.png)

## 起因

2023 年 3 月 5 日, Mohist 开发组宣布了全球首款重写版多线程高并发核心：MPS。

![@JE6FKNDF$ZINQCQ T51K0C_tmb](https://user-images.githubusercontent.com/53771072/232276715-0c190f3e-20be-43c6-8911-bc0a023fdd38.jpg)

*以下为当时 "核心文档页" 的截图归档，该页面在 MPS 真正发布的时候已经被修改去除了造假图片，后文会提到。*

![QQ图片20230416123746](https://user-images.githubusercontent.com/53771072/232273118-18bfc820-8044-4cdd-9cb4-32d471647616.jpg)

在本页面中，我们可以清楚的看到 MPS-Dev-0748 与 Paper 的对比：

![image](https://user-images.githubusercontent.com/53771072/232273239-f1662eca-e46f-493a-96ef-635c2edffe43.png)

![image](https://user-images.githubusercontent.com/53771072/232273247-e8ca07b1-3641-4aa5-97bd-5e3c3fd59523.png)

如果您仔细观察，您可以发现所谓 MPS 截图中，村民的位置很明显不对劲：

![image](https://user-images.githubusercontent.com/53771072/232273265-bc9fdec7-51fc-4302-8d41-b577028e055f.png)

他们通通朝向一个方向。

并且：

![image](https://user-images.githubusercontent.com/53771072/232273272-0eeb9b20-bf3e-49e8-b8c8-cea63e728fc6.png)

究竟是什么黑魔法，能让一个区域里塞入 6k+ 村民还不被挤压分散开？

实现方法很简单，在 Minecraft 服务端中有一个 `entityList` 变量来存储所有的实体。

我们只需要：

```java
entityList.forEach(entity -> {
    entity.setAI(false);
});
```

即可实现该效果。

您可能已经意识到了这端代码的作用：关闭生物 AI。

在 MPS 开发组宣布该项目成立后，本着怀疑的态度，我加入了 Mohist 交流群询问有无视频性能展示。

但开发组成员 Sakura 女士却回应到：视频录制好了正在剪辑。

我们曾叫她不要剪辑直接发出，她却一拖再拖。

此时 Mohist 群内的 "收银员" 开始找我们麻烦了。

"预售为什么有一个预字呢？"

我想，他可能没有使用过诸如 京东、淘宝 这样的电商平台。

电商平台预售都有完整的商品介绍，您的产品只放出来了一个虚假的截图，还有理由来质问我？

而且，"预售" 一词为什么有一个 "售" 字呢？

这位 "收银员" 的智商我们不得而知，也不知道他是在什么精神状态下发出了如此无脑的话语来保护他的 Mohist 开发组大爹。

我不想在别人的地盘惹麻烦，因此我打算到了他们发布的日子再次询问。

Sakura 女士是否真的了解 Minecraft 服务器，我们不得而知：

![Screenshot_2023_0416_141048](https://user-images.githubusercontent.com/53771072/232275324-0acd93e8-d3a3-4681-91fa-aa029a3370bd.jpg)

"收银员" 辩护 Mohist 大爹的截图：

![{X$L)BO78Q5 A%SO0_BWGLR](https://user-images.githubusercontent.com/53771072/232275255-1de7d699-8602-4caa-b3d0-2c0668ab616f.jpg)

## 发酵

在发布后，有许多人购买了 MPS。

以下为 MPS 发布时的价格截图与购买页面。

*这些页面在后来被修改了。后续会提到。*

![1](https://user-images.githubusercontent.com/53771072/232276540-a42fea80-759c-4ca9-8ee0-57faf2e0d966.jpg)
![2](https://user-images.githubusercontent.com/53771072/232276542-09e1cc00-3a4f-4983-a66b-db0918f86634.jpg)
![3](https://user-images.githubusercontent.com/53771072/232276543-96711069-1b7f-4413-a1ee-ca58e0cc77f8.jpg)
![4](https://user-images.githubusercontent.com/53771072/232276546-2a6375ac-b709-4979-81f6-5d9a2bba599d.jpg)
![5](https://user-images.githubusercontent.com/53771072/232276549-73879cda-8195-4484-81c9-6068b7380ba0.jpg)

本人家境贫寒，无法购买 MPS。只能靠着一张嘴来抨击了。不过这是我的好伙伴的购买截图。

*MPS 后续进行多次降价。且暂未将差价退款。*

![image](https://user-images.githubusercontent.com/53771072/232276625-dc203876-5990-4f5e-8842-b2624a1760f9.png)

有一个订单显示过期是因为最初购买的时候付款了但是订单出现了故障，经过极其长的等待我们终于联系上了 Sakura 女士 并让她为我们修复订单问题。

转眼间到了发布的日子。可是我们的 MPS 开发组似乎并没有完成项目并拖到了 2023 年 4 月 15 日。

![Screenshot_2023_0416_145840](https://user-images.githubusercontent.com/53771072/232278850-3af48da5-846b-4acb-a628-690f1135fa1e.jpg)
![Screenshot_2023_0416_144334](https://user-images.githubusercontent.com/53771072/232277964-ec72e919-384f-49fc-93a6-ea0c63f42531.jpg)

我曾进入群询问，可没有得到开发组的答复。

*此处他们多次说：重写验证后端。但实际上服务端本身并不包含任何验证，只有在下载的时候会检测 IP 地址。*

*他们的下载页面使用到了 vue.js。让人怀疑这么长的时间是不是拿去学习 vue.js 了。*

![image](https://user-images.githubusercontent.com/53771072/232277045-ab881a07-92be-45a6-adfb-eb68b016c65a.png)

后来，我因为无聊要我的一个朋友基于他的一个项目造了一个 假 MPS。

*由于该圈子的风气问题且该项目完全不稳定，我们不会发布该项目。*

该项目实际上拥有 MPS 最初宣发时的性能。

![QMF_7L{O8CT~X~GEOPDLP$0_tmb](https://user-images.githubusercontent.com/53771072/232277184-c970d892-75ad-489c-a686-6c25ca300177.jpg)
![(N3()2JHSRV)RXHWW0L4PU8_tmb](https://user-images.githubusercontent.com/53771072/232277203-f1018542-f151-4e72-b7ae-c143790adf6d.jpg)

我们将服务端的名字修改为 "MPS 先遣版" 并由我的小号发布到了 Mohist 群内。

*我们当时发布的群文件已经被删除。且消息也被撤回了。*

*在这段聊天记录里，我的小号 miyuki 和我的大号共同配合演了这场戏。*

![Screenshot_2023_0416_145817](https://user-images.githubusercontent.com/53771072/232279044-1c465217-074f-4ef8-90d6-a945ad23c922.jpg)

随后引起了一些轰动，并引起了 MPS 开发组的注意。

![Screenshot_2023_0416_145917](https://user-images.githubusercontent.com/53771072/232278976-bc7f16c8-40d7-4627-8ee4-4232651c5ac2.jpg)
![CK`NBMEHA}SIJ7VAFN4UOYC](https://user-images.githubusercontent.com/53771072/232277600-c2ffcbc8-f3f1-4f7a-9726-80019759fdd4.jpg)

好笑的是，`MPS-Dev-0748` 实际上是 MPS 文档内的版本号。

![image](https://user-images.githubusercontent.com/53771072/232277618-5514ecf0-0a87-4364-b9ee-a0db5d52e681.png)

并且，MPS 文档内的截图完全没有体现出所谓 "多核调用"。

![image](https://user-images.githubusercontent.com/53771072/232277647-b2ce5f98-2686-47fa-b5ee-a012ffa96578.png)

我们可以看到，系统的总 CPU 占用不过百分之十几。您的多核调用在哪里？

上图中假 MPS 的报错，实际上是通过达到一定时间阻塞主线程实现的。

## 真正的 "发布"

时间到了 4 月份。万众瞩目的 MPS 终于发布了。

可是，却变成了 "部分超过 Pufferfish+"。

![image](https://user-images.githubusercontent.com/53771072/232278213-2dc2cfb9-6d44-4009-bd33-d220bbd6bcf5.png)

文档页面也改成了这样，去除了图片。

![image](https://user-images.githubusercontent.com/53771072/232278198-de538417-897b-4a94-a357-73587f606083.png)

同时，继续下调价格。

![image](https://user-images.githubusercontent.com/53771072/232278238-cf606582-aeb4-44ae-a33b-8005770be14b.png)

*以下的内容足够重磅，请准备好。*

MPS 的配置文件实际上是有问题的。默认就无法加载。

![image](https://user-images.githubusercontent.com/53771072/232278382-dbd5aeec-da11-4138-aee3-ec33aedeefd0.png)

MPS 怎么把 Airplane 据为己有了？

![XQAFV}L}UKUG1}CULO3O~(E](https://user-images.githubusercontent.com/53771072/232278495-be9d786c-1d14-4c5d-a578-3347ff7c078c.png)
![@X{PX)MWW82JX(IRUEC0Y$F](https://user-images.githubusercontent.com/53771072/232278515-bd471abc-3652-45de-bc02-4e1b78641ad7.png)

*上：Airplane。*
*下: 反编译的 MPS 代码。*

与此同时...

当英明神武的 MPS 团队被揭发，会怎么说呢？

![image](https://user-images.githubusercontent.com/53771072/232278577-5a7a228b-2f0b-4697-8da7-b58aaeeb73b3.png)
![image](https://user-images.githubusercontent.com/53771072/232278592-31e4ee87-f429-41fb-8fe1-b3f687b15ee0.png)
![image](https://user-images.githubusercontent.com/53771072/232278598-ad789ce3-4419-4779-a267-32831d29113f.png)

等等...

![image](https://user-images.githubusercontent.com/53771072/232278611-b18415ad-b2f6-4de4-b314-68dd92a213ff.png)

您的宣传图就是使用村民测试的吧？
而且，为什么村民测试是违规的，这难道不意味着 MC 占用大头之一的村民没有得到任何优化吗？

![image](https://user-images.githubusercontent.com/53771072/232278662-0f7b0c10-bdff-4d3c-aee3-e75335c42792.png)

何为 "综合性能" ？

我们不得而知。

## 后记

这篇文档的作用只为了揭发 MPS。

如果您觉得本文有写错的地方，欢迎提交 issue 或自行提交 pull request 来帮我们修改。

是的，我可能只是互联网一角的多管闲事的人。

但我只是做着我觉得我应该做的时期。

本文作者 Nostal Yuu，感谢您能阅读到这里。

祝您阖家欢乐，身体健康。
