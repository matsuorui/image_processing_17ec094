課題4


カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像


画素の濃度ヒストグラムを生成する．

：

imhist(ORG); % ヒストグラムの表示

：

によって図1のように濃度ヒストグラムを表示できる．

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k4.png)

図2 ヒストグラム

特にカラーバーの50~100での濃度が高いことが分かる．
