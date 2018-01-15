エッジ抽出を行う。  


IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  

imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

pause; % 一時停止  
結果は図１のようになった。  
![untitled](https://user-images.githubusercontent.com/35324583/34929078-01ceb91a-fa05-11e7-9b5b-2afa16e176a8.jpg)

図１  


IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  

imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

pause; % 一時停止  
結果は図２のようになった。  
![untitled1](https://user-images.githubusercontent.com/35324583/34929103-398ff9ae-fa05-11e7-944c-4a98b1e520b7.jpg)

図２

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  

imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

pause; % 一時停止  
結果は図３のようになった。  
![untitled2](https://user-images.githubusercontent.com/35324583/34929125-5d24ecd0-fa05-11e7-856d-fb0b53413034.jpg)

図３