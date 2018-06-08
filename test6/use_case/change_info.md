
# 修改用户信息用例 [返回](../README.md)
## 1. 用例规约

|用例名称|修改用户信息|
|-------|:-------------|
|功能|修改用户的GitHub用户名称|
|参与者|所有用户|
|前置条件|必须先登录，并且查看用户现有的GitHub用户名|
|主事件流| 1.用户填写GitHub用户名称 <br/> 2.用户提交修改信息 <br/>3.系统存储修改后的GitHub用户名称|
|备选事件流|1. 如果用户输入的GitHub用户名称为空 <br/>&nbsp;&nbsp; a.系统清空用户的GitHub用户名称<br/>2.用户输入内容中有非法字符<br/>&nbsp;&nbsp;b系统清空用户的GitHub用户名称|

## 2. 业务流程
无

## 3. 界面设计
- 界面参照: https://yhw0709.github.io/is_analysis/test6/ui/logout.html
- API接口调用
    - 接口1：[getUserInfo](../interface/getUserInfo.md)
    - 接口2：[setUserInfo](../interface/setUserInfo.md)
    
## 4. 算法描述
无
    
## 5. 参照表
- [USERS](../database.md/#USERS)
