# Digital-Watermark
数字水印算法小试
在文件中添加一张1980*1080的图像
并且命名为shuiyin.jpg
就可以进行数字水印的嵌入和提取了
![image](https://user-images.githubusercontent.com/61741332/147665150-16a4551f-922d-4942-b90e-d28b8da85380.png)
算法语言：python3.8
变量说明： 
变量符号 说明 img_A 要加数字水印的图像
Img_B 要嵌入的水印图像
image_A 要加数字水印的图像 img_A 对应矩阵
image_A
image_W 要嵌入的水印图像img_W矩阵image_W
alpha 水印强度参数
U,V,S Image_A 进行 svd 后得到的正交矩阵
和对角矩阵
L L = S+alpha*image_W
U1,V1,S1 L 进行 svd 后得到的正交矩阵和对角
矩阵
Aw 加入数字水印后的图片对应的矩阵
Image_P 待检测是否加入水印的图片对应的矩阵
Up,Sp,Vp Image_P 进行 svd 后得到的正交矩阵
和对角矩阵
F F=U1SpV1
WE svd 解密出的水印图像对应的矩阵
image_WE WE 矩阵对应的图片形式
WE_compare 将没加入水印的 image_A 做 svd 分解
得到的矩阵，与 WE 做对比
image_WE_compare WE_compare 矩阵对应的图片形式
