
# 接口：getCourse  [返回](../README.md)
用例： [选课](../use_case/select_work.md)

- 权限：
    老师：可以看到TOTAL，TIME,YEAR,CLASS。
    学生：可以看到TEACHER，TIME,YEAR,CLASS。

- 功能：
    学生和老师选择课程。

- API请求地址：
   接口基本地址/interface/getCourse

- 请求方式 ：
    POST

- 请求参数说明:
    无

- 返回实例：

        {
            "status": true,
            "info": NULL,
            "data": [
                {"WEB_SUM": "Y,Y,Y,Y,Y,N",
                "GITHUB_USERNAME": "joe",
                "COURSE_ID": "201510414666",
                "NAME":"软件工程"
                "TOTAL": "60",
                "TIME":"16"
                "YEAR":"2018上学期"
                "CLASS":"软件工程2015级6班"
                "TEACHER":"昆哥"
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |data|所有课程的数组|
  |WEB_SUM|网址是否正确的汇总|
  |GITHUB_USERNAME|GITHUB 用户名|
  |COURSE_ID|课程的课程号|
  |NAME|课程名称|
  |TOTAL|上课总人数|
  |TIME|上课的总学时|
  |YEAR|上课的年份和学期|
  |CLASS|上课的专业和班级|
  |TEACHER|上课的老师|