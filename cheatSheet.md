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
```
星星眼
sparkling anime eyes
```

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

## SORA 提示词赏析

```
#"Starry Gift" 
## Subject / Scene Settings - Audience: locale="EN"; 
Narrative tone: warm, wordless Christmas fantasy; 
high-tempo dance super-trailer - Subject type: humanoid child protagonist - Key features: small anime-style girl, round face, simple dot eyes, soft blush, blue winter coat and white knit hat outlined in glowing neon; she holds a bright cyan gift box in softly falling snow; 
《星之礼》
## 主题/场景设置 - 受众：本地化语言="英文"； 
叙事基调：温馨、无言的圣诞奇幻； 
快节奏舞蹈超级预告片 - 主题类型：拟人化儿童主角 - 关键特征：小巧的动漫风格女孩，圆润脸庞，简约圆点眼睛，柔和绯红，蓝色冬季外套与白色针织帽边缘泛着霓虹光晕；她手持明亮青色礼盒，置身于轻柔飘落的雪花中；
Scale: child in human-scale town; 
Motion: gentle but lively dance, 16fps animation with many hand-drawn in-betweens - Age: ~8; 
Vibe: innocent, curious, brave; Skin: fair with winter flush; Makeup: none;
Hair: medium-length dark hair with subtle highlights, slightly messy from snow - Outfit: thick navy coat with white trim + simple tights (mostly hidden by coat) + puffy winter sneakers with glowing laces; 
规模：儿童在人性化尺度的小镇中； 
动作：轻盈活泼的舞蹈，16帧/秒动画，含大量手绘中间帧——年龄：约8岁； 
氛围：天真、好奇、勇敢；肤色：白皙，略带冬日红晕；妆容：素颜；
发型：中长发，深色发质带淡雅挑染，雪天略显凌乱  
着装：厚款深蓝色大衣配白色装饰 + 简约连裤袜（大多被大衣遮住） + 气泡冬季运动鞋，鞋带散发荧光；
Accessories: knit hat with pom-pom, subtle scarf implied - Environment: quiet Japanese-style town plaza/side street; photoreal winter night; Christmas lights and shop windows glowing warmly under deep blue sky - Location: urban town plaza and rooftops;
Time: night; 
Weather/Light: steady snowfall, cold air; 
motivated light from streetlamps, shopfronts, and luminous gift - Key elements (FG/MG/BG): FG snow, light flares and occasional lens snow on glass; 
配饰：带毛球的针织帽，暗示性围巾——环境：宁静的日本风情小镇广场/小巷；写实风格的冬日夜晚；圣诞灯饰与店铺橱窗在深蓝色天空下温暖闪烁——地点：城镇广场与屋顶；
时间：夜晚； 
天气/光照：持续降雪，寒气袭人； 
受街道路灯、商店橱窗和发光礼品店灯光激发的光线——关键元素（前景/中景/背景）：前景为雪景，光线耀斑及玻璃上偶见的镜头雪花；
MG girl and dancers; 
BG detailed shops, signage, Christmas tree, distant high-rise skyline - Lighting: motivated key from gift and practical streetlamps; mostly soft; subtle rim/kicker from warm windows; 
neg fill on shadow side; bounce from snow-covered ground; 
light gobo from tree branches; 
thin cool haze; 
visible light beams/volumetrics - Grade: cool cyan/blue
MG女孩和舞者； 
BG详细的商店、标牌、圣诞树、远处的高层天际线——照明：来自礼物和实用路灯的动力钥匙；大多柔软；温暖窗户的微妙边缘/踢腿； 
阴影侧填充负；从白雪覆盖的地面反弹； 
从树枝上摘下轻盈的酒杯； 
薄凉雾； 
可见光束/体积测量.等级：冷青色/蓝色
```

```
# “RED BOUQUET” 
## Subject / Scene Settings - Audience: locale="EN"; 
Narrative tone: quiet, uncanny, surreal loneliness 
- Subject type: person (anime-stylized girl in sketchy line art) 
- Key features: 
thin doll-like girl with oversized dark eyes and unreadable face; 
clutching a bouquet of vivid red flowers in an otherwise monochrome world; 
background a chaotic web of hand-drawn lines; 
minimalist framing and empty negative space; 
Scale: MS→CU→ECU with occasional WS of blank voids; 
Motion: subtle, constant line boil on every stroke; 
stop-motion-like 16fps with many drawings per second 
- Age: 10–12; 
Vibe: fragile / solemn / faintly ominous; 
Skin: pale graphite; 
Makeup: none; 
Hair: short dark bob, solid ink mass framing her face 
- Outfit: simple black long-sleeve dress with small white collar + thin pale hands; 
implied simple shoes, no accessories 
- Lighting: motivated top/side key; 
mostly hard edges with soft roll-off; 
thin white rim on hair; 
aggressive neg fill swallowing one side of her face; 
occasional harsh window-slit gobo; 
faint “paper dust” haze; 
light volumes drawn as parallel hatching 
- Grade: stark monochrome line art; 
single accent color = deep crimson petals; 
high-contrast curve; 
subtle bloom on bright whites; 
gentle vignette and fine film grain; 
tiny chromatic shift only on reds; 
rare clean flare sketched as radial lines 
- Visual taste: monochrome
```


