課題9


カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像


メディアンフィルタを適用し,ノイズを除去する．

：

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付

：


![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k9-1.png)

図2 ノイズ添付した画像

:

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去

:

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k9-2.png)

図3 平滑化フィルタで雑音除去した画像


:


IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去

:

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k9-3.png)

図4 メディアンフィルタで雑音除去した画像

:


f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計

IMG = filter2(f,IMG,'same'); % フィルタの適用

:

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k9-4.png)

図4 作成したフィルタを適用した画像

図4からわかるように画像は暗くなったが添付したノイズがなくなり,原画像に近く修復することができた．
