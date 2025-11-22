# 便捷取用

## 起手式  

``` txt
furry,chibi,solo,cat feature，pastel color,gradient color,simple white background，(kamikiririp:0.2),(soresaki:0.4),
```

## 基于一定主题的提示词组合 ⭐

结合deepseek快速设计出合理的角色
![alt text](/image/角色快速设计.jpg)  

| 时代背景 |  |
|-------|-------|
|cyberpunk|赛博朋克|
|steampunk|蒸汽朋克|
|biopunk|生物朋克|
|dieselpunk|柴油朋克|
|atompunk|原子朋克|
|raygun gothic|射线枪哥特|
|lovecraftian horror|克苏鲁风格|
|synthwave|合成器浪潮|
|cassette futurism|磁带未来主义|
|wuxia|武侠|

问deepseek

``` txt
帮我生成一段SDXL提示词，绘制拟人角色立绘，在xxx时代背景xxx职业的xxx动物, 绘制场景只要一个角色，不要差分图，避免character design sheet 类的词汇，用尽可能简洁的词组表示
```

“万能头”  + deepseek 给出的提示词。如果出现多人，可以找有没有xxx sheet, 增加solo（单人）权重

``` txt
furry,chibi,(solo:1.2),(kamikiririp:0.2),(soresaki:0.4),gradient color, 
```

| 平涂LORA |  |
|-------|-------|
| 有兽焉漫画 | 1.0 |
| Art-山楂糖 | 0.5 |

| 加光影笔触LORA |  |
|-------|-------|
| 战斗狂草乱线风草稿风 | 0.2 |
| 米山舞-yoneyama mai | 0.1 |



## 配色  

|  |  |
|-------|-------|
| 颜色饱和度过高或者指定亮部 | light xxx (浅色) |
| 指定暗部颜色| dark xxx（深色）|
| 渐变色 |  gradient color ⭐ |
| 指定局部颜色| xxx hair, xxx eyes, xxx fur, xxx clothes |
| 指定全局颜色 | xxx color scheme ⭐(配色方案) |
| 条纹颜色 | striped  例如：Black and white striped hair |

``` txt
dark blue and light purple color scheme
dark green and light orange color scheme
light blue and pink color scheme
blue and orange color scheme
rainbow color scheme
pastel color ⭐
vibrant color 
monochrome
grey scale

```

## 镜头效果

|  |  |
|-------|-------|
|仰视| from below |
|俯视| from above |
|透视效果|foreshortening ⭐ |
|近距离| close up|
| 上半身 | upper body |
|全身|full body|
|头部|head focus|

- 光影套餐  

``` txt
foreshortening,cinematic light,hdr shadow,blurry,chromatic aberration
透视缩短、电影级灯光、高分辨率阴影、模糊、色差
```

## 材质 （在自身风格确定的模型下不是很起作用）

- 手绘材质

``` txt
sketch, traditional media ⭐
water color 
poster 
```



## 杂项

<https://www.liblib.art/imageinfo/891bed4414d5429f953efb03c0714c7e>

```txt
chibi,lue3style,yoneyama mai,furry,kemono,(solo:1.5),chibi,(kamikiririp:0.2),(soresaki:0.4),pastel color,tiger feature,white fur,simple white background,smile,scarf,
```

| LORA | 权重 |
|-------|-------|
| 米山舞-yoneyama mai | 0.1 |
| 有兽焉漫画 | 1.0 |
| Art-山楂糖 | 0.5 |
| 战斗狂草乱线风草稿风 | 0.2 |

<https://www.liblib.art/imageinfo/3efe548db81c4c4b8b2242530cc3b4d6>

- 魔法森林-avali  

``` txt
avali,(kemono:0.8),(furry:0.8),(transparent body:1.4),hoodie,hat,shorts,chibi,solo,dynamic pose,forest background,smile,
holding a book and Cast a spell,from below,pastel colors,
vine,night,looking away,magic,cinematic light,soresaki,source_cartoon,light green color scheme,foreshortening,gradient color,
```  

- Grim Reaper-avali

``` txt
avali,(kemono:0.8),(furry:0.8),(transparent body:1.1),loose hoodie,shorts,chibi,solo,(dynamic pose:1.2),smile,looking away,white face,wings,from below,holding a book,Grim Reaper,huge Scythe of Death,glowing magic particles,
dark blue and light purple color scheme,pixel art,glitch art,abstract,cinematic light,pastel colors,source_cartoon,soresaki,(nuu \(nu-nyu\):0.6),foreshortening,gradient color,
```
