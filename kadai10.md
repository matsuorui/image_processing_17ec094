課題10


カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像

画像のエッジを抽出する．

ここでは,プレウィット法・ソベル法・キャニー法の3つの方法を用いてエッジの抽出をする．


：

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）

:

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k10-1.png)

図2 プレウィット法


:

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）

:

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k10-2.png)

図3 ソベル法

:

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）

:

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k10-3.png)

図4 キャニー法

図2と図3のプレウィット法とソベル法ではほとんど同じようにエッジの抽出ができるが,図4のキャニー法は一筆書きのように線がすべて繋がっているような抽出方法であることがわかる．
