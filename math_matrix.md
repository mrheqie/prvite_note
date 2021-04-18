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