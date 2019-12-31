課題10


画像のエッジを抽出する．

ここでは,プレウィット法・ソベル法・キャニー法の3つの方法を用いてエッジの抽出をする．




IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）


![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k10-1.png)

図1 プレウィット法

・

・

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k10-2.png)

図2 ソベル法

・

・

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k10-3.png)

図3 キャニー法
