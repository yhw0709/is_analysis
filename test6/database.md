

<div id="TEACHERS"></div>

- ## TEACHERS表（教师表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |TEACHER_ID|NUMBER(8,0)|主键|否| | | 职工编号|
    |NAME|VARCHAR2(50 BYTE)| |否| | | 教师真实姓名|
    |SEX|VARCHAR2(2 BYTE)| |否| | | 教师的性别|
    |TITLE|VARCHAR2(50 BYTE)| |否| | | 教师的职业评称|
    |PHONE|NUMBER(12,0)| |否| | | 老师的电话|
    |E-MAIL|VARCHAR2(24 BYTE)| |否| | | 老师的邮箱
    |CLASS|VARCHAR2(13 BYTE)| |否| | | 老师的任课课程|

<div id="STUDNETS"></div>

- ## STUDENTS表（学生表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |STUDENT_ID|NUMBER(12,0)|主键|否| | | 学生的学号|
    |NAME|VARCHAR2(50 BYTE)| |否| | | 学生的真实姓名|
    |SEX|VARCHAR2(2 BYTE)| |否| | | 学生的性别|
    |MAJOR|VARCHAR2(30 BYTE)| |否| | | 学生的专业|
    |GRADE|VARCHAR2(6 BYTE)| |否| | | 学生的年级|
    |CLASS|VARCHAR2(4 BYTE)| |否| | | 学生的班级|
    |PHONE|NUMBER(12,0)| |否| | | 学生的电话|
    |E-MAIL|VARCHAR2(24 BYTE)| |否| | | 学生的邮箱|

    
    <div id="COURSE"></div>
    
- ## COURSE表（课程表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |COURSE_ID|NUMBER(13,0)|主键|否| | | 课程的编号，根据开课顺序自动递增生成|
    |NAME|VARCHAR2(50 BYTE)| |否| | | 课程的名字|
    |YEAR|VARCHAR2(14 BYTE)| |否| | | 课程的开课年份|
    |TIME|VARCHAR2(14 BYTE)| |否| | | 上课的总课时|
    |TOTAL|VARCHAR2(14 BYTE)| |否| | | 上课的总人数|
    |CLASS|VARCHAR2(14 BYTE)| |否| | | 上课的专业以及班级|
    |TEACHER|VARCHAR2(14 BYTE)| |是| | | 讲课教师|
    
    

   <div id="TEST"></div>


- ## TEST表（实验表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |TEST_ID|NUMBER(5,0)|主键|否| | |实验序号,根据实验安排顺序自动递增生成|
    |COURSE_ID|VARCHAR2(50 BYTE)|外键 |否| | | 此次实验的课程号|
    |NAME|VARCHAR2(50 BYTE)| |否| | | 实验名称|
    |COTENT|VARCHAR2(14 BYTE)| |否| | | 实验内容|
    |SCORE|FLOAT(4 BYTE)| |是| | | 实验成绩|
    |EVALUATE|VARCHAR2(200 BYTE)| |是| | |教师对学生此次实验的评价|
    
    
    
   <div id="OFFICE"></div>
    
- ## OFFICE表（教务处表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |MAJOR|VARCHAR2(20 BYTE)|主键|否| | |学院名称|
    |DIRECTER|VARCHAR2(10 BYTE)|主键|否| | |教务处主任姓名|
    |PHONE|NUMBER(12,0)| |否| | | 主任的电话|
    |E-MAIL|VARCHAR2(24 BYTE)| |否| | | 主任的邮箱|

<div id="USERS"></div>

- ## USERS表（用户表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |USER_ID|NUMBER(8,0)|主键|否| | | 用户ID|
    |NAME|VARCHAR2(50 BYTE)| |否| | | 用户真实姓名|
    |GITHUB_USERNAME|VARCHAR2(50 BYTE)| |是|空| | GitHUB用户名|
    |PASSWORD|VARCHAR2(512 BYTE)| |是|空| | 加密存储密码，为空表示密码就是学号|