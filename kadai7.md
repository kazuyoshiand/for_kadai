画素のダイナミックレンジを０から２５５にせよ．   

ORG = imread('Lenna.jpg'); % 画像の読み込み  

ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  

imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

pause;  

imhist(ORG); % 濃度ヒストグラムを生成、表示  

pause;  
濃度ヒストグラムの表示結果は図１のようになった。  
![untitled](https://user-images.githubusercontent.com/35324583/34824372-8a7af112-f711-11e7-84e8-f9e643826db5.jpg)  
図１


ORG = double(ORG);  

mn = min(ORG(:)); % 濃度値の最小値を算出  

mx = max(ORG(:)); % 濃度値の最大値を算出  

ORG = (ORG-mn)/(mx-mn)*255;  

imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

pause;  
画像の表示結果は図２のようになった。  
![untitled3](https://user-images.githubusercontent.com/35324583/34824411-a6cf7f2c-f711-11e7-9aeb-83b72664c107.jpg)  
図２


ORG = uint8(ORG); % 符号なし整数へのシンボリック行列の変換  

imhist(ORG); % 濃度ヒストグラムを生成、表示  
濃度ヒストグラムの表示結果は図３のようになった。  
![untitled2](https://user-images.githubusercontent.com/35324583/34824453-ce3c89ec-f711-11e7-9e36-78cdb6fac4f9.jpg)  
図３


