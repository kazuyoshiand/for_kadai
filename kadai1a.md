標準画像「dandakeyMV2_TP_V」を原画像とする．この画像は縦843画素，横1600画素による長方形のディジタルカラー画像である．  
ORG=imread('dandakeyMV2_TP_V.jpg'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示  
によって，原画像を読み込み，表示した結果を図１に示す．  
![untitled](https://user-images.githubusercontent.com/35324583/34813403-47f4ada2-f6ed-11e7-8e84-007adcd769bb.jpg)

図1 原画像
原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．なお，拡大する際には，単純補間するために「box」オプションを設定する．
IMG = imresize(ORG,0.5); % 画像の縮小
IMG2 = imresize(IMG,2,'box'); % 画像の拡大
1/2サンプリングの結果を図２に示す．
![untitled2](https://user-images.githubusercontent.com/35324583/34813925-35ed9392-f6ef-11e7-8d87-6c8478d6c450.jpg)

図2 1/2サンプリング
同様に原画像を1/4サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．すなわち，
IMG = imresize(ORG,0.5); % 画像の縮小
IMG2 = imresize(IMG,2,'box'); % 画像の拡大
とする．1/4サンプリングの結果を図３に示す．
![untitled4](https://user-images.githubusercontent.com/35324583/34813944-4dd8c378-f6ef-11e7-856f-156452fb8e05.jpg)
図3 1/4サンプリング
1/8から1/32サンプリングは，
IMG = imresize(ORG,0.5); % 画像の縮小
IMG2 = imresize(IMG,2,'box'); % 画像の拡大
を繰り返す．サンプリングの結果を図４～６に示す．

![untitled3](https://user-images.githubusercontent.com/35324583/34813936-43b37870-f6ef-11e7-97c8-01d94a25d371.jpg)
図4 1/8サンプリング
![untitled5](https://user-images.githubusercontent.com/35324583/34813957-5869b5d6-f6ef-11e7-8478-b3b77babf947.jpg)
図5 1/16サンプリング
![untitled6](https://user-images.githubusercontent.com/35324583/34813972-66968846-f6ef-11e7-8f5f-059ea50b9536.jpg)
図6 1/32サンプリング
このようにサンプリング幅が大きくなると，モザイク状のサンプリング歪みが発生する