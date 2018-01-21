# 課題６レポート

課題１同様「eagle.jpg」を原画像とする．この画像の二値化を行なう。  
数値を使った二値化とディザ法を使った二値化を行なう。


clear; % 変数のオールクリア  
ORG=imread('C:\work\3rd3rd\gazo\eagle.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause; % 一時停止  

これにより作用した原画像を図１に示す。


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai6_1.png?raw=true)


IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  

によって，二値化した原画像を図２に示す。



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai6_2.png?raw=true)  


図2 数値による二値化画像


IMG = dither(ORG); % ディザ法による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって二値化した画像を図３に示す。



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai6_3.png?raw=true)  


図3 ディザ法による二値化画像

このようにディザ法だと白が混じり色味に違いが出る。
