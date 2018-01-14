# 課題３レポート

課題１同様「eagle.jpg」を原画像とする．この画像を白黒濃淡画像に変換。


ORG=imread('eagle.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，変換した結果を図１に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai3_1.png?raw=true)  


図1 白黒濃淡画像


以下より閾値処理を行なう。輝度値が64以上画像に生成するには，以下のようにする。



IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  

結果を図２に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai3_2.png?raw=true)  


図2 輝度64以上の画像


同様に輝度値が96以上画像に生成するには，以下のようにする。


IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  

とする．結果を図３に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai3_3.png?raw=true)  


図3 輝度96以上の画像

同様に輝度128以上、輝度192以上の画像を生成するには.



IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  


とする．生成の結果を図４,図５に示す．



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai3_4.png?raw=true)  


図4 輝度128以上の画像




![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai3_5.png?raw=true)  


図5 輝度192以上の画像


