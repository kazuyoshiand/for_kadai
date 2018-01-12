２階調，４階調，８階調の画像を生する。  

ORG=imread('dandakeyMV2_TP_V.jpg'); % 原画像の入力  

ORG = rgb2gray(ORG); colormap(gray); colorbar;  

によって，原画像を読み込み，表示した結果を図１に示す。  
![untitled1](https://user-images.githubusercontent.com/35324583/34819511-4313412c-f701-11e7-9ccf-5dd41fb5a9de.jpg)  
図1  
  
２階調画像の表示を行う。  
IMG = ORG>128;  

imagesc(IMG); colormap(gray); colorbar;  axis image;  
によって２階調画像の表示を行った。結果は図２ののようになった。  
![untitled2](https://user-images.githubusercontent.com/35324583/34819689-d0eee654-f701-11e7-8be2-d7da738b03e6.jpg)
図２  
  
４階調画像の表示を行う。   

IMG0 = ORG>64;

IMG1 = ORG>128;

IMG2 = ORG>192;

IMG = IMG0 + IMG1 + IMG2;  
によって４階調画像の表示を行った。結果は図３のようになった。   
![untitled3](https://user-images.githubusercontent.com/35324583/34819998-b2fd65d4-f702-11e7-99d9-8d51c943bcdd.jpg)  
図３
