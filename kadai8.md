二値化された画像の連結成分にラベルをつけよ.  

IMG = ORG > 128; % 閾値128で二値化  

imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

pause;  
閾値１２８での二値化の結果は図１のようになった。  
![untitled](https://user-images.githubusercontent.com/35324583/34825000-19fe5138-f714-11e7-9c9e-5d7a30329aea.jpg)  
図１

IMG = bwlabeln(IMG);  

imagesc(IMG); colormap(jet); colorbar; % 画像の表示  

pause;  
ラベルを付けた結果図２のようになった。  
![untitled1](https://user-images.githubusercontent.com/35324583/34825051-4dedd608-f714-11e7-9645-57a19d4a67b6.jpg)  
図２
