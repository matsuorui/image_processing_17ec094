課題7


ダイナミックレンジの拡大を行う．画素のダイナミックレンジを0から255にする．

ORG = double(ORG);

mn = min(ORG(:)); % 濃度値の最小値を算出

mx = max(ORG(:)); % 濃度値の最大値を算出

ORG = (ORG-mn)/(mx-mn)*255;

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k7-1.png)

図1

ORG = uint8(ORG); % 8 ビット符号なし整数配列

imhist(ORG); % 濃度ヒストグラムを生成、表示



![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k7-2.png)

図2
