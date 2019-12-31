課題3

カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像

ここで,閾値を4パターンに設定し,閾値処理した画像を示す．輝度値が閾値以上の画素を1，その他を0に変換する．

：

IMG = ORG > 64; %閾値64

IMG = ORG > 96;%閾値96

IMG = ORG > 128;%閾値128

IMG = ORG > 192;%閾値192

：

処理の結果を図10～13に示す．

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k3-1.png)

図10 処理画像(閾値64)

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k3-2.png)

図11 処理画像(閾値96)


![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k3-3.png)

図12 処理画像(閾値128)


![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k3-4.png)

図13 処理画像(閾値192)
