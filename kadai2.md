課題2

カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像

2階調画像の生成をする．

：

IMG=ORG＞128;

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-2.png)

図2 2階調画像



4階調画像の生成．

：

IMG0=ORG>64;

IMG1=ORG>128;

IMG2=ORG>192;

IMG=IMG0 + IMG2;

：


![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-3.png)

図3 4階調画像


8階調画像の生成．

：

IMG0=ORG>32;

IMG1=ORG>64;

IMG2=ORG>128;

IMG3=ORG>160;

IMG4=ORG>192;

IMG5=ORG>224;

IMG6=ORG>256;

IMG=IMG0 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-4.png)

図4 8階調画像
