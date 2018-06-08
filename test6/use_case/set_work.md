#安排实验用例[返回](../README.md)
## 1. 用例规约

|用例名称|安排实验|
|-------|:-------------|
|功能|老师对于自己的课程进行实验的安排|
|参与者|老师|
|前置条件| 需要先选择课程|
|后置条件|安排后需要得到教务处审核才能成功|
|主流事件| 1.教师点击“添加实验”进入添加实验界面<br/>2.教师填写“实验名称”、“截止日期”、“实验内容”<br/>3.点击发布|

## 2. 业务流程[源码](../sequence_diagram/set_work.puml)
![sequence1](../sequence_diagram/set_work.png) 


## 3. 界面设计
- 界面参照:  https://yhw0709.github.io/is_analysis/test6/ui/class_teacher.html
- API接口调用
    - 接口1：[getTest](../interface/getTest.md)

## 4. 算法描述
- WEB_SUM解析为列表  
  - WEB_SUM是接口getTest的返回值中的一部分，形如："WEB_SUM": "Y,Y,Y,Y,Y,N"。需要在前端进行解析。  
  - 作用是判断GitHub网址是否正确，用逗号分开，Y代表正确，N代表不正确。  
  - 第1位代表总的GitHUB地址是否正确，第2位表示第1次实验的地址，第3位表示第2位实验地址，依此类推。
  - 比如：“Y,Y,Y,Y,Y,N”表示第5次实验地址不正确，其他地址正确。  
  - 算法是使用使用字符串分离方法将其分开。

    
## 5. 参照表

- [TEST](../database.md/#TEST)
- [COURSE](../database.md/#COURSE)
- [STUEDNTS](../database.md/#STUDENTS)

