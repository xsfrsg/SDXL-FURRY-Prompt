# FURRY DIFFUSION TUTORIAL 
- 基于Illustrious（光辉）类模型的提示词及lora组合探究，展示已发现的平涂及伪厚涂风格下的FURRY向提示词书写技巧

## 基础模型 (Checkpoint)

- Indigo Furry Mix XL NoobAI_EPS_Ⅹ_7 
- Indigo Furry Mix XL NoobAI_EPS_Ⅹ_10  

## LORA 
1. Art-山楂糖_1  
https://www.liblib.art/modelinfo/64d5025db1c64fb596af342f66a921c5  
<img src="/image/LORA1.jpg" alt="示例图片" width="600" >  

2. 有兽焉漫画  
https://www.liblib.art/modelinfo/6fc79150990447409a3ad5feb75a77d8    
<img src="/image/LORA_YSY.jpg" alt="示例图片" width="600" >  

3. 

## 入口
- 由于部分LORA独占性，在其他平台不可用，推荐在LiblibAI中的webui进行绘制 
<img src="/image/inter.jpg" alt="示例图片" width="600" >  
<img src="/image/inter2.jpg" alt="示例图片" width="600" >  


## 1. 平涂类  
  提示词推荐遵从主体, 背景, 画面材质顺序书写，增加可读性和可维护性

## 起手式
```  
furry,kemono,solo,chibi,cat feature，pastel color,simple white background，(kamikiririp:0.2),(soresaki:0.4),
```
``` 
LORA
Art-山楂糖_1: 0.5
有兽焉漫画_兔爷: 0.8
```
<img src="/image/1.png" alt="起手式" width="300" >


## 和服套装
``` 
chibi,furry,solo,
green hair,knee-high socks,one eye half-lidded,long hair tied back,chibi,kimono,fox ears,subtle blush,wide sleeves,bangs swept to side,sun (symbol),obi sash,hakama pants,simple traditional outfit,plain white,holding a fan,looking at viewer,hair tie,white undergarments,kimono slightly open,foreshortening,gradient color,one eye closed,from below,
white background,
```
<img src="/image/2.jpg" alt="和服套装" width="300" >


