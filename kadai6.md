画像を輝度値１２８とディザ法によって二値化せよ．  

clear; % 変数のオールクリア  

ORG=imread('Lenna.png'); % 原画像の入力  

ORG = rgb2gray(ORG);  

imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

pause; % 一時停止  

IMG = ORG>128; % 128による二値化  

imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

pause;  

IMG = dither(ORG); % ディザ法による二値化  

imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
結果は輝度値１２８では図１のようになり、ディザ法では図２のようになった。  
![untitled](https://user-images.githubusercontent.com/35324583/34823985-f6f99318-f70f-11e7-9ceb-3ded95a9b81b.jpg)

  
  図１  
![untitled1](https://user-images.githubusercontent.com/35324583/34823994-02a799d0-f710-11e7-9609-148c389350fb.jpg)
  
  図２