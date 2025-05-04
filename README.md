\# 硬件技术团队编程基础作业 

 ## 一、简介 

本仓库是硬件技术团队编程基础作业的成果，旨在实现一个线性代数计算库，通过C语言编程完成矩阵的各种运算，并运用Git、CMake等工具进行工程管理。 

## 二、实现思路 

### （一）整体思路 

根据题目要求，我首先完善了工程模板中的文件夹结构，在`src`文件夹下实现矩阵运算函数，通过`CMakeLists.txt`文件进行项目编译配置。在函数实现上，依据线性代数的理论知识，结合C语言语法，逐步完成每个矩阵运算函数的编写。 

### （二）函数实现思路

1. #### `add_matrix` 函数

   检查两个矩阵的行数和列数是否相同，若不同则输出错误信息并返回空矩阵。

   创建一个新矩阵用于存储结果。

   遍历两个矩阵，将对应位置的元素相加存入结果矩阵。

   返回结果矩阵。

2. #### `sub_matrix` 函数

   检查两个矩阵的行数和列数是否相同，不相同则输出错误信息并返回空矩阵。

   创建一个新矩阵用于存储结果。

   遍历两个矩阵，将对应位置的元素相减存入结果矩阵。

   返回结果矩阵。

3. #### `mul_matrix` 函数

   检查矩阵 `a` 的列数是否等于矩阵 `b` 的行数，不等则输出错误信息并返回空矩阵。

   创建一个新矩阵用于存储结果。

   遍历矩阵 `a` 的行和矩阵 `b` 的列，通过累加乘积的方式计算结果矩阵对应位置的元素。

   返回结果矩阵。

4. #### `scale_matrix` 函数

   创建一个新矩阵，大小与原矩阵相同。

   遍历原矩阵，将每个元素乘以给定的数 `k` 存入新矩阵。

   返回新矩阵。

5. #### `transpose_matrix` 函数

   创建一个新矩阵，行数和列数与原矩阵交换。

   遍历原矩阵，将元素按转置规则存入新矩阵（`a[i][j]` 变为 `result[j][i]`）。

   返回转置后的矩阵。

6. #### `det_matrix` 函数

   检查矩阵是否为方阵，不是则输出错误信息并返回 0。

   若为一阶矩阵，直接返回该元素。

   若为二阶矩阵，使用公式 `a[0][0]*a[1][1] - a[0][1]*a[1][0]` 计算行列式。

   对于更高阶矩阵，通过代数余子式递归计算行列式。

7. #### `inv_matrix` 函数

   检查矩阵是否为方阵，不是则输出错误信息并返回空矩阵。

   计算矩阵的行列式，若行列式接近 0 则输出错误信息并返回空矩阵。

   对于二阶矩阵，使用公式计算逆矩阵。

   对于更高阶矩阵，通过计算伴随矩阵并除以行列式得到逆矩阵。

8. #### `trace_matrix` 函数

   检查矩阵是否为方阵，不是则输出错误信息并返回 0。

   遍历矩阵主对角线元素，累加这些元素的值得到矩阵的迹



## 三、本地运行截图 

![]([photo/1.png at master · GEM520/photo](https://github.com/GEM520/photo/blob/master/1.png)



![]([photo/2.png at master · GEM520/photo

[](https://github.com/GEM520/photo/blob/master/2.png)

![]([photo/3.png at master · GEM520/photo

[](https://github.com/GEM520/photo/blob/master/3.png)

![]([photo/4.png at master · GEM520/photo](https://github.com/GEM520/photo/blob/master/4.png)



![]([photo/5.png at master · GEM520/photo

[](https://github.com/GEM520/photo/blob/master/5.png)

![]([photo/6.png at master · GEM520/photo

[](https://github.com/GEM520/photo/blob/master/6.png)

![]([photo/7.png at master · GEM520/photo](https://github.com/GEM520/photo/blob/master/7.png)



![]([photo/8.png at master · GEM520/photo

[](https://github.com/GEM520/photo/blob/master/8.png)

![]([photo/9.png at master · GEM520/photo

[](https://github.com/GEM520/photo/blob/master/9.png)

![]([photo/10.png at master · GEM520/photo](https://github.com/GEM520/photo/blob/master/10.png)

## 四、工程结构说明 

`inc`文件夹用于存放头文件，声明矩阵运算函数；`src`文件夹包含实现矩阵运算功能的源文件；`build`文件夹用于存放编译生成的可执行文件和中间文件；`CMakeLists.txt`文件定义了项目的编译规则，如设置C标准、添加头文件目录和源文件，以及生成可执行文件的名称等。 
