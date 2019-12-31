課題8


カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像

二値化された画像の連結成分にラベルをつける．閾値を128にした白黒濃淡画像を用いる．

IMG = bwlabeln(IMG);

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k8-1.png)

図2 連結成分をラベリング処理した画像
