# 卫星姿态仿真Adams与Simulink联合


## 1，输出设置
### 卫星姿态
通过创建三个系统变量（系统单元）来获取三个轴的姿态变化，通过选择系统变量里的函数（位移目录———B321 ...ROTATION）选中后的函数为PITCH( To_Marker , From_Marker ) To-Marker为目标局部坐标系也就是本次仿真中星本体姿态坐标系，From-Marker为全局坐标系。
![img](images\shchu.png)

### 设置输出变量
单元-数据单元--poutput，跟创建的系统变量一一关联
![img](images\shuchu2.png)

## 2，输入设置
### 力矩
创建系统变量（系统单元），创建单元——数据单元——pinput关联该输入系统变量。
完成后修改刚刚创建的那个系统变量的函数：选中 数据单元——plant inputvlaue 点辅助选中创建的pinput并确定。
## 3，导出系统
![img](images\shuchu3.png)



![img](images\shuchu4.png)

生成三个文件.m,.adm,.cdm，注意文件生成的位置可能不在模型文件目录

## 4，Matlab中打开
更改工作目录，运行.m文件，后在命令行中输入adams_sys
