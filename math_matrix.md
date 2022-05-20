 * **basic variable**  
  线性方程中对应于系数矩阵主元列的变量

  * **free variabke**   
    线性方程中基本变量之外的变量

* **简化行阶梯型**  
      每一个非零的先导元素是1  
      每一先导元素1是该元素所在列的唯一非零元素  
      example:  
      |1    0    0    29|  
      |0    1   0   16|  
      |0    0   1     3|  


 * **Row reduction algorithm**  
    ```
     倍加变换  对换变换 倍乘变换

    1 . forward phase
    2 . backward phase
    ```
* **存在与唯一性定理**
   线性方程组相容的冲要条件是增广矩阵的最右列不是主元列

* **R^n**  
   含有n个元素的列向量的集合
* **Span{v}**
   通过原点的直线
* **Span{u,v}**
   通过原点的平面

* **matrix  equation Ax = b**  
   ```  
                                       |x1|
                                       |x2|
   Ax =[a1,a2,...an]* |....| = x1 * a1 + x2 * a2..... xn*an
                                       |xn|

   ```    
 ### Solution set of linear equations  
* homogeneous equation  **Ax = 0**  
  ```   
  x  =  tv
  x = su +  tv
  ```   
* nonhomogeneous  equation  **Ax = b** 
   ```  
   x = p + tv

   ```  

##  linear combination  
      ( 线性组合 )   
      y = c1v1 + ....... +cpyp  

 ## linearly dependent ( vectors )  
     线性相关  
   x1v1 + x2v2 + ... + xpvp = 0  不仅有平凡解  
   列数大于行数时 这个向量组线性相关  
   包含 0 向量          这个向量组线性相关  

 ## linearly independent(vectors)  
      线性无关  
      x1v1 + x2v2 + ... + xpvp = 0  仅有平凡解  
      增广矩阵 行化简后 没有自由变量  

## linear  transformation T  
      线性变换
      T :  Rn -> Rm   
      矩阵变换 中 标准矩阵的
                行数决定余定义域的  m  
                列数决定定义域的       n  


      若 A 是 m*n 的矩阵 且T(x) = Ax :   
               A = [ T(e1)  T(e2)  ...... T(en) ]  ,ek为单位矩阵 In 的第k列 

      单位矩阵 : 对角线全为 1  , 其余全为 0 的方形矩阵

      当 Ax = 0 仅有平凡解时 , 该线性变换为一对一 



 ## mulitplication

* AB  
    ```  
         A 的列数必须与 B 的行数相等 乘机才有意义
         
         AB != BA
         
         A 的行数决定乘积的行数 B 的列数决定乘积的列数:
         ( m * n )*( n * p )  -> (m*p)

         把 A 依次去乘以 B 的各列

         ( AB )ij =     A 的第 i 行的元素 依次乘以 B 的第 j 列的元素，把所有结果相加

 ## inverse
 可逆性 : 存在一个矩阵 C 使得 矩阵 A 与之的乘积为 单位矩阵  ( CA = I  )  
 方形矩阵的求逆  : [ A I ] 行等价于 [ I   (A)-1 ]  
求矩阵的逆的某一列 ：A xn  = en   ( A 为原矩阵  ，en为单位矩阵的第 n 列 ，xn 为解)  

## LU factorization  
```
A = m*n       L = m*m     U = m*n
Ax = b    ---->   L(Ux) = b
L 是一个 m*m 的下三角矩阵 ( 右上部分全为 0  ,对角线全为 1  )
U 是一个阶梯形矩阵  (  左下部分全为0 )

funcation ( algorithm ) :
对矩阵进行 行化简 为阶梯形 为 U
将化简过程中左列主元下全为 0  的列用该列主元除以该列的每一个元素，将结果填入 L
```
## 矩阵在计算机图形学中的应用
```
对于 2*n 的矩阵中的 x 和 y
 | a     b|
 | c     d|
| x |
| y |
 X =  x*a  + y*b
 Y =  y*d + x*c

对于二维图形的任意线性变换 有以下分块矩阵实现
| A  0 |
| 0  1 |     A为 a,b,c,d构成的2*2矩阵，三维图形时为3*3矩阵
对于非线性变换 (  平移 )：
右上角的  0 向量 更换为 需要平移的向量即可

齐次坐标 ( X,Y,Z,H )  H 不必一定为 1 ，可以为(X ，Y ，Z )对(x,y,z) 的公除数
```