課題5


カラー画像を白黒濃淡画像に変換する．

：

ORG = rgb2gray(ORG); %カラーからグレイへの変換

：

![原画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k2-1.png)

図1白黒濃淡画像

判別分析法によって画像二値化を行う．

：

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納

myu_T = mean(H);

max_val = 0;

max_thres = 1;

for i=1:255

C1 = H(1:i); %ヒストグラムを2つのクラスに分ける

C2 = H(i+1:256);

n1 = sum(C1); %画素数の算出

n2 = sum(C2);

myu1 = mean(C1); %平均値の算出

myu2 = mean(C2);

sigma1 = var(C1); %分散の算出

sigma2 = var(C2);

sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出

sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出

if max_val<sigma_B/sigma_w

max_val = sigma_B/sigma_w;

max_thres =i;

end;

end;

IMG = ORG > max_thres;

：

以上のようにして分離度が最大となる閾値を算出し画像の二値化を行う．結果を図2に示す．

![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k5-1.png)

図2 二値化画像
