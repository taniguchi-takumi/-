# 課題７レポート

課題１同様「eagle.jpg」を原画像とする。  
この画像のダイナミックレンジを拡大する。  
画素のダイナミックレンジを０から２５５にする。  
  
まずは原画像を表示する。  


ORG = imread('C:\work\3rd3rd\gazo\eagle.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
imhist(ORG); % 濃度ヒストグラムを生成、表示  
pause;  

これにより作用した原画像を図１、そのヒストグラムを図２に示す。


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai7_1.png?raw=true)

図1　原画像のグレースケール


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai7_2.png?raw=true)

図2　原画像のヒストグラム


以下よりダイナミックレンジの拡大を行なう。

ORG = double(ORG);
mn = min(ORG(:)); % 濃度値の最小値を算出
mx = max(ORG(:)); % 濃度値の最大値を算出
ORG = (ORG-mn)/(mx-mn)*255;
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
ORG = uint8(ORG); % この行について考察せよ
imhist(ORG); % 濃度ヒストグラムを生成、表示




![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai7_3.png?raw=true)  


図3  原画像をダイナミックレンジ２５６に拡大したもの


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai7_4.png?raw=true)  


図4  図3のヒストグラム


#考察

考察せよとされている行は、画像の描画に使われているORGを、符号なしの8bit整数からなる行列に  
変換する関数。これで出力範囲を抑え、適した濃度のヒストグラム生成が可能になる。
