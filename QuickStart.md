# 快速开始

## 模型准备(Checkpoint)
- Indigo Furry Mix XL NoobAI_EPS_Ⅹ_10  
<https://www.liblib.art/modelinfo/681c469852ce4d78a2653a2d3b571414>

## LORA准备  
![alt text](/image/ALL_LORA.jpg)  

- Art-山楂糖_1（Lib独占）
<https://www.liblib.art/modelinfo/64d5025db1c64fb596af342f66a921c5>  
<img src="/image/LORA1.jpg" alt="示例图片" width="600" >  

- 有兽焉漫画（可下载）
<https://www.liblib.art/modelinfo/6fc79150990447409a3ad5feb75a77d8>  
<img src="/image/LORA_YSY.jpg" alt="示例图片" width="600" >

## 绘画入口  

- 由于部分LORA独占性，在其他平台不可用，推荐在LiblibAI中的webui进行绘制
- 会员最低档40元一个月，15000积分能差不多画4000多张，正常玩玩是非常足够了；免费一天的200点也足够试一试
（需要充值会员的话可以走此邀请码，应该会有一定折扣 <https://www.liblib.art/viphome?referralCode=9hysq3HU> ）

<img src="/image/inter.jpg" alt="示例图片" width="600" >  

<img src="/image/inter2.jpg" alt="示例图片" width="600" >  

- Webui基础使用参考教程  
<https://www.bilibili.com/video/BV1VXYszZEvD/>  

- 个人主页 点击图片可以看到参数
https://www.liblib.art/userpage/d4ce153ffe1a451395af4c1d174a463c/publish/image 
## QuickStart 起手式

<img src="/image/起手式1.jpg" alt="起手式" width="600" >  

<img src="/image/起手式画幅参数.jpg" alt="画幅 & CFG" width="600" >

- CFG 5-7即可
- 竖幅1024x1536

``` txt
PROMPT:
furry,chibi,solo,cat feature，pastel color,simple white background，(kamikiririp:0.2),(soresaki:0.4),
====
LORA:
Art-山楂糖_1: 0.5
有兽焉漫画_兔爷: 0.8
```

- 得到类似效果表示成功   
<img src="/image/1.jpg" alt="起手式" width="300" >  

### 起手式 [25.12.04]
```
furry,chibi,solo,cat feature,pastel color,simple white background,(kamikiririp:0.2),(tianliang_duohe_fangdongye:0.7),
====
LORA:
Art-山楂糖_1: 0.5
有兽焉漫画_兔爷: 0.8
```

### 起手式 [25.12.29]

```
no humans,(claws:0.6),dated,white background,solo,animal focus,smile,
(tianliang_duohe_fangdongye:0.8),(chibi:0.9),gradient color,(kamikiririp:0.2),(soresaki:0.1),forest,flat color,no shading,
====
LORA:
有兽焉漫画_兔爷: 0.7
XL-藏色彩感: 0.2
```

接下来是
[提示词及LORA权重案例分析](prompt.md)

