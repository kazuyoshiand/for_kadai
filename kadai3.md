カラー画像を白黒濃淡画像へ変換閾値を4パターン設定し,閾値処理た画像示す。  
  
ORG=imread('dandakeyMV2_TP_V.jpg'); % 原画像の入力  

ORG= rgb2gray(ORG); %  
元画像の表示結果は図１のようになった。  
![untitled2](https://user-images.githubusercontent.com/35324583/34821142-201c3a48-f706-11e7-8cc2-9f2e39a3091a.jpg)  
図１
   
  
輝度値が64以上の画素を1，その他を0に変換した場合  

IMG = ORG > 64; % 

imagesc(IMG); colormap(gray); colorbar;  
結果は図２のようになった。  
![untitled3](https://user-images.githubusercontent.com/35324583/34821187-421cf434-f706-11e7-9218-84057da732d7.jpg)  
図２
  
輝度値が96以上の画素を1，その他を0に変換した場合   
IMG = ORG > 96;  

imagesc(IMG); colormap(gray); colorbar;  
結果は図３のようになった。  
![untitled4](https://user-images.githubusercontent.com/35324583/34821250-75a08a3c-f706-11e7-977b-61115e3d26db.jpg)  
図３  
    
    
輝度値が128以上の画素を1，その他を0に変換した場合   
IMG = ORG > 128;  

imagesc(IMG); colormap(gray); colorbar;  
結果は図４のようになった。  
![untitled5](https://user-images.githubusercontent.com/35324583/34821344-be54a24a-f706-11e7-804d-bbf9e97c2abb.jpg)  
図４  

輝度値が192以上の画素を1，その他を0に変換した場合  
IMG = ORG > 192;  

imagesc(IMG); colormap(gray); colorbar;  
結果は図５のようになった。  
![untitled6](https://user-images.githubusercontent.com/35324583/34821386-e331130a-f706-11e7-9951-fa04829ee562.jpg)  
図５
