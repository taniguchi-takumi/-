# 課題２レポート

課題１同様「eagle.jpg」を原画像とする．この画像をグレースケールに直す。


RG=imread('eagle.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，グレースケールで表示した結果を図１に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai2_1.png?raw=true)  


図1 グレースケール



原画像を２階調画像に生成するには，以下のようにする。



IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

２階調画像生成の結果を図２に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai2_2.png?raw=true)  


図2 ２階調画像


同様に原画像を４階調画像に生成するには，以下のようにする。


IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

とする．４階調画像に生成の結果を図３に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai2_3.png?raw=true)  


図3 ４階調画像

８階調画像に生成するには，



IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>128;
IMG3 = ORG>192;
IMG4 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4;
imagesc(IMG); colormap(gray); colorbar;  axis image;

とする．８階調画像に生成の結果を図４に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai2_4.png?raw=true)  


図4 ８階調画像



