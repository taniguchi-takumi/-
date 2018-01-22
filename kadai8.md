# 課題８レポート

課題１同様「eagle.jpg」を原画像とする。  
この画像を二値化し、連結部分にラベルを付ける。
  
まずは原画像を表示する。  


ORG = imread('C:\work\3rd3rd\gazo\eagle.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  

これにより作用した原画像を図１に示す。


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai8_1.png?raw=true)

図1　原画像のグレースケール

原画像を以下のコードで二値化する。

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai8_2.png?raw=true)

図2　二値化の結果


以下より連結部分にラベルを付ける。

IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示  
pause;  




![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai8_3.png?raw=true)  


図3  図2をラベリングした画像


