課題6


画像を二値化する．

IMG = ORG>128; % 128による二値化
IMG = dither(ORG); % ディザ法による二値化


![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k3-3.png)

図16 二値化画像(128)


![画像](https://github.com/matsuorui/image_processing_17ec094/blob/master/image/image/k6-1.png)

図17 ディザ法による二値化画像
