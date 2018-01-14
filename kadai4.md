# 課題４レポート

課題１同様「eagle.jpg」を原画像とする．この画像の画素濃度ヒストグラムを表示する。


ORG=imread('C:\work\3rd3rd\gazo\eagle.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  
pause;

imhist(ORG); % ヒストグラムの表示  

によって，作成した画像を図１,ヒストグラムを図２に示す



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai4_1.png?raw=true)  


図1 白黒濃淡画像




![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai4_2.png?raw=true)  


図2 ヒストグラム
