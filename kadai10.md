# 課題１０レポート

課題１同様「eagle.jpg」を原画像とする。  
この画像にエッジ抽出を行なう。
  
まずは原画像を表示する。  


ORG = imread('C:\work\3rd3rd\gazo\eagle.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); % カラーからグレイへの変換  
imagesc(ORG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止   

これにより作用した原画像を図１に示す。


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai10_1.png?raw=true)

図1　原画像のグレースケール

原画像に以下のコードでプレウィット法によるエッジ抽出を行なう。

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止   



![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai10_2.png?raw=true)

図2　プレウィット法による結果


以下よりソベル法によるエッジ抽出を行なう。

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止  




![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai10_3.png?raw=true)  


図3  ソベル法による結果


以下よりキャニー法によるエッジ抽出を行なう。

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  
pause; % 一時停止  


![原画像](https://github.com/taniguchi-takumi/gazousyorikougaku/blob/master/image/kadai10_4.png?raw=true)  


図4  キャニー法による結果


キャニー法が他の方法よりより細かくエッジを検出しているとわかる。