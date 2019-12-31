課題6


カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像

画像を二値化する．


：

IMG = ORG>128; % 128による二値化

から,128以上を１,それ以下を0として図1のように表示する．

：

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k3-3.png)

図2 二値化画像(128)

：

IMG = dither(ORG); % ディザ法による二値化

：

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k6-1.png)

図3 ディザ法による二値化画像


図2と図3を比べると、図3の方がより濃度を表すモザイクが小さく再現度が高かった．
