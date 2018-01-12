画像のヒストグラムを表示する。  

ORG=imread('dandakeyMV2_TP_V.jpg'); % 原画像の入力  

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  

imagesc(ORG); colormap(gray); colorbar;  

pause;  

imhist(ORG); % ヒストグラムの表示画素の濃度ヒストグラムを生成せよ  　  

  
結果は図１のようになった。  
![untitled](https://user-images.githubusercontent.com/35324583/34821801-362b9c82-f708-11e7-918b-c8030d8b1df6.jpg)  
図１
