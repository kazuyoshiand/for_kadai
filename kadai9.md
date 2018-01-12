メディアンフィルターを適用し，ノイズ除去を体験せよ．  
ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  

imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

pause;  
ノイズを添付した画像は図１のようになった。  
![untitled](https://user-images.githubusercontent.com/35324583/34825253-17519ab6-f715-11e7-8989-9f11d7c1d08f.jpg)
  
  図１

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  

imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

pause;  
平滑化フィルタで雑音除去を行った結果は図２のようになった。   
![untitled1](https://user-images.githubusercontent.com/35324583/34825286-328379bc-f715-11e7-9be9-8cf53ee26e64.jpg)  
図２  

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  

imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

pause;  
メディアンフィルタで雑音除去を行うと図３のようになった。  
![untitled2](https://user-images.githubusercontent.com/35324583/34825309-4c390dd6-f715-11e7-8584-9b1e879c0503.jpg)  
図３


f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  

IMG = filter2(f,IMG,'same'); % フィルタの適用  

imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

pause;  
フィルタの適応を行うと図４のようになった。  
![untitled3](https://user-images.githubusercontent.com/35324583/34825342-67890d0c-f715-11e7-8d4b-88c17e78d695.jpg)  
図４
