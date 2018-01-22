# 課題９レポート

課題１同様「eagle.jpg」を原画像とする。  
この画像にメディアンフィルタを適用し、ノイズ除去を行なう。
  
まずは原画像を表示する。  


ORG = imread('C:\work\3rd3rd\gazo\eagle.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  

これにより作用した原画像を図１に示す。


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai9_1.png?raw=true)

図1　原画像のグレースケール

原画像に以下のコードでノイズを添付する。

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai9_2.png?raw=true)

図2　ノイズ添付


以下より平滑化フィルタでノイズを除去する。

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  




![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai9_3.png?raw=true)  


図3  平滑化フィルタの結果


以下よりメディアンフィルタでノイズを除去する。

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai9_4.png?raw=true)  


図4  メディアンフィルタの結果


最後に以下よりフィルタをかけ、灰色の画像にする。

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai9_5.png?raw=true)  


図5  フィルタ適用結果