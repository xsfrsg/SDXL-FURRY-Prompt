# FURRY DIFFUSION TUTORIAL 
- 基于Illustrious（光辉）类模型的提示词及lora组合探究，展示已发现的平涂及伪厚涂风格下的FURRY向提示词书写技巧，分享当下SD的使用心得, 同时作为备忘。

## 基础模型 (Checkpoint)

- Indigo Furry Mix XL NoobAI_EPS_Ⅹ_7 
- Indigo Furry Mix XL NoobAI_EPS_Ⅹ_10  

## LORA 
![alt text](/image/ALL_LORA.png)  

### 1. 画风类
-  Art-山楂糖_1（Lib独占）
https://www.liblib.art/modelinfo/64d5025db1c64fb596af342f66a921c5  
<img src="/image/LORA1.jpg" alt="示例图片" width="600" >  

- 有兽焉漫画（可下载）
https://www.liblib.art/modelinfo/6fc79150990447409a3ad5feb75a77d8    
<img src="/image/LORA_YSY.jpg" alt="示例图片" width="600" >

### 2. 画面材质类 
- 幻月重光_暖色滤镜（最安全的滤镜lora，不会破坏画风）
  https://www.liblib.art/modelinfo/3fc51122271047e99a8beb5c9f0e976b
- XL-藏色彩感 （和chibi风格冲突，但会强化透视质量）
  https://www.liblib.art/modelinfo/85be701b3321450dbe6cfba673380f4d
- 战斗狂草乱线风草稿风 （增加线稿笔触）
  https://www.liblib.art/modelinfo/67b8eab839254bf3b4c6539b6760781e
- 米山舞-yoneyama mai （大张力画面，但及其容易崩手）
  https://www.liblib.art/modelinfo/36afc64367c24006a7922ae1301b2f5e
- 大笔触厚涂（仅限会员，但作用有限） 
  https://www.liblib.art/modelinfo/e8e7ffdbf2304943967f03ce56c586dc
- Impressioncolor l 印象色彩-SDXL（仅限会员，但作用也有限） 
  https://www.liblib.art/modelinfo/66e8874fc4fd4a0db55cc3a473ad2470


## 绘画入口  

- 由于部分LORA独占性，在其他平台不可用，推荐在LiblibAI中的webui进行绘制
- 会员最低档40元一个月，15000积分能差不多画4000多张，正常玩玩是非常足够了；免费一天的200点也足够试一试 
（需要充值会员的话可以走此邀请码，应该会有一定折扣 https://www.liblib.art/viphome?referralCode=9hysq3HU ）

<img src="/image/inter.jpg" alt="示例图片" width="600" >  
<img src="/image/inter2.jpg" alt="示例图片" width="600" >  

- Webui基础使用参考教程  
https://www.bilibili.com/video/BV1VXYszZEvD/  

## Tips 
  - 提示词推荐遵从主体, 背景, 画面材质顺序书写，增加可读性和可维护性
  - 正面提示词不必使用质量词（best quality等），属于SD1.5时期的过时操作，现在实测并没有显著影响，只会影响可读性，浪费prompt词条位置。总之，应该用尽可能简明的词组指出画面成分
  - 负面提示词看情况补充 （watermark：2.0）去除画面水印即可，同样不需要堆叠负向质量词
  - 提示词权重，lora都要依少到多逐个调试，找到合适的范围区间；尽量避免联调，会难以定位导致问题出现的部分
  - 画师串遵从huggingface的csv文件（可以在danbooru搜索，再查csv表确定提示词中的名称），但其实如同大海捞针，遇到可用的串组合相当困难，应该直接参考他人已经使用的组合。  
   https://drive.google.com/file/d/1FuME-Ch5a9PsfDX5DN68ygjQaR28EdXZ/view?usp=drive_link

## 1. 平涂类  
 
### QuickStart 起手式

<img src="/image/起手式1.png" alt="起手式" height="300" >

<img src="/image/起手式画幅参数.png" alt="画幅 & CFG" height="300" >

- CFG 5-7即可 
- 画幅有:竖幅1024x1536(2:3) 横幅1536x864(16:9) 正方形（1024x1024）正确的画幅参数绘制效果最好
- 记得随机种子设置为-1 ，画面过于固定时看一下是不是锁了种子

```  
PROMPT:
furry,chibi,solo,cat feature，pastel color,simple white background，(kamikiririp:0.2),(soresaki:0.4),
====
LORA:
Art-山楂糖_1: 0.5
有兽焉漫画_兔爷: 0.8
```
| prompt | 作用 | 延申 |
|-------|-------|-------|
| furry,chibi,solo | 固定组合 | 不需要萌系便去掉chibi |
| cat feature | 指定动物特征 | 避免直接写动物导致背景出现一群相应动物的情况 |
| pastel color | 柔和配色 | xxx color scheme 指定画面配色|
| simple white background | 指定背景 | dark,abstract background  |
| (kamikiririp:0.2),(soresaki:0.4), | 画师串 | - |

<img src="/image/1.jpg" alt="起手式" width="300" >


### 和服套装
- 看到不错的服装搭配 ，可以复制进来
``` 
furry,chibi,solo,
green hair,knee-high socks,one eye half-lidded,long hair tied back,kimono,fox ears,subtle blush,wide sleeves,bangs swept to side,sun (symbol),obi sash,hakama pants,simple traditional outfit,plain white,holding a fan,looking at viewer,hair tie,white undergarments,kimono slightly open,
foreshortening,gradient color,one eye closed,from below,simple white background,

LORA:
Art-山楂糖_1: 0.7
```
<img src="/image/2.jpg" alt="和服套装" width="300" >

| prompt | 作用 | 延申 |
|-------|-------|-------|
| green hair | 发色 | xxx fur毛发颜色,加stripe有条纹效果，xxx eyes 眼睛颜色 |
| foreshortening | 透视法 | 增强透视表现，更有立体感（但搭配一些lora可能导致动作过于激烈而崩手崩脚） |
| gradient color | 渐变色 | 丰富画面表现，使颜色有过渡质感 |
| one eye closed | 指定动作 | v(v手势)，颜文字等都可，也可直接翻译软件 |

- 多翻一翻提示词表，这些原生词汇会识别的更好
![alt text](/image/props.png)

### 表情包 expressions
```
chibi,furry,kemono,(solo:1.5),chibi,(kamikiririp:0.2),(soresaki:0.4),(head focus:1.2),(simple white background:1.4),gradient color,light green hair,red eyes,expressions,
``` 
<img src="/image/expressions.png" alt="表情包" width="300" >

| prompt | 作用 | 延申 |
|-------|-------|-------|
| (head focus:1.2) | 聚焦于头部，画头像时用 | 还有upperbody上半身，full body全身，portrait肖像构图|
| expressions | 表情差分 | 会画出各种表情，可以指定多种，但不太稳定，抽盲盒一样 |


## 2. 伪厚涂类

- 宝可梦简易速查
<img src="/image/宝可梦.png" alt="pkm"  width="300" >  

- 宝可梦百科  
  https://wiki.52poke.com/wiki/

### 沙奈朵-和风

<img src="/image/houtu1.jpg" alt="snd" width="300" >  

```
Gardevoir,kimono,holding a sword,solo,(soresaki:0.2),foreshortening,smile,cinematic light,hdr shadow,blurry,chromatic aberration,(sketch:0.8),simple background,pastel color,
====
LORA
米山舞-yoneyama mai: 0.1
幻月重光_暖色滤镜: 0.8
XL-藏色彩感: 0.4
战斗狂草乱线风草稿风: 0.5
```
| prompt | 作用 | 解释 |
|-------|-------|-------|
| Gardevoir | 使用官方的标准英文名称即可 | 不需要写furry，写了很可能导致意料之外的结果 |
| cinematic light，hdr shadow | 强调明暗光影对照 | - |
| blurry | 大光圈焦散效果 | - |
| chromatic aberration | 色差 | 轮廓边缘模拟相机色散效果 |
| sketch | 线稿 | 此处主要作为lora触发词，单独使用作用不明显 |


- 提一下高清重绘，一般放大1.25倍，重绘幅度0.4附近即可
<img src="/image/upscale.png" alt="wt ht" height="500" >  

### 白虎-武侠

<img src="/image/伪厚涂2.jpg" alt="wt ht" width="300" >  

```
furry,solo,tiger feature,white and black stripe fur,Wuxia,bamboo hat,looking away,
close up,upper body,vibrant color,gradient color,cinematic light,hdr shadow,blurry,chromatic aberration,sketch,(kamikiririp:0.1),(soresaki:0.2),
```
| prompt | 作用 | 解释 |
|-------|-------|-------|
| Wuxia | 指定题材 | 模型可以自动脑补一定的细节，快速出效果，再酌情手工补充 |
| looking away | 视线 | 常用的有looking at viewer等 | 
| close up | 相机距离 | 还有midshot wideshot等 但由于是专注于立绘的模型，效果不佳 |

- 由此见得，当画风描述框架确定下来后，模型足够的泛化性使得绘画内容有很灵活的变化空间。

### 指定配色

<img src="/image/伪厚涂3.png" alt="wt ht" width="300" >    

```
furry,chibi,white fur,tiger feature,(solo:1.5),tall and thin,gradient color,smile,flowers,foreshortening,cinematic light,hdr shadow,blurry,chromatic aberration,sketch,grey scale,looking away,dark green and light orange color scheme,loose hoodie,hand in pocket,(soresaki:0.2)
===
LORA
幻月重光_暖色滤镜
Art-山楂糖
战斗狂草乱线风草稿风
```

| prompt | 作用 | 解释 |
|-------|-------|-------|
| dark green and light orange color scheme | 指定配色 | 如图可见，可以轻松做出颜色统一的画面，并且能智能的指定到近似颜色的物体上 |

## 写在最后
  
未完待续。  




