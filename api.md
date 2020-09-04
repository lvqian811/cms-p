## 接口文档

Base 地址: http://localhost:3000

版本 :  v1



### 用户创建

- 简单描述

  - 增加新用户接口

- 请求路径

  - /users

- 请求方式

  - POST

- 请求参数

  | 名称       | 必选 | 类型           | 说明                    |
  | ---------- | ---- | -------------- | :---------------------- |
  | username   | 是   | string         | 账号名 唯一             |
  | password   | 是   | string         | 用户密码                |
  | nickname   | 是   | string         | 用户名称                |
  | role       | 否   | [admin,normal] | 角色类型                |
  | createtime | 否   | Date           | 创建日期 默认: Date.now |
  | status     | 否   | Number         | 1:激活 0:未激活 默认: 1 |
  | avatar     | 否   | String         | 头像                    |

  

- 返回数据

```json
{
	status:0,
	msg:'增加用户成功'
}
```

```json
{
    status:-1,
	msg:'增加用户失败'
}
```



### 用户列表

