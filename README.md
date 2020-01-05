## 设计
### 数据库设计
#### C端数据库设计
- 用户表-user

字段名|类型|含义|其他
-|:-:|-:|-:|
id|int|编号|主键
user_name|varchar(255)|用户名|
sex|int|性别|0为男,1为女.默认0|
password|varchar(255)|密码|
avatar|varchar(255)|头像|
alias|varchar(255)|别名|
collect_quantity|int|收藏数|
like_quantity|int|点赞数|
follow_quantity|int|关注数|

- 话题表-topic

字段名|类型|含义|其他
-|:-:|-:|-:|
id|int|编号|主键
title|varchar(255)|标题|
content|varchar(255)|内容|
image|varchar(255)|插图|
collect_quantity|int|收藏数|
like_quantity|int|点赞数|
follow_quantity|int|关注数|

- 用户话题关系表-user_topic

字段名|类型|含义|其他
-|:-:|-:|-:|
id|int|编号|主键
user_id|int|用户编号
topic_id|int|话题编号

- 评论表-comment

字段名|类型|含义|其他
-|:-:|-:|-:|
id|int|编号|主键
content|varchar(255)|内容|
collect_quantity|int|收藏数|
like_quantity|int|点赞数|
follow_quantity|int|关注数|

- 话题评论关系表

字段名|类型|含义|其他
-|:-:|-:|-:|
id|int|编号|主键
topic_id|int|话题编号|
comment_id|int|评论编号|

- 用户评论关系表

字段名|类型|含义|其他
-|:-:|-:|-:|
id|int|编号|主键
user_id|int|用户编号|
comment_id|int|评论编号|
#### B端数据库设计
### 接口设计
#### C端接口设计
- 用户登录
- 用户注册
- 用户修改密码
- 用户发表话题
- 用户删除话题
- 用户修改话题
- 用户添加评论
- 用户修改评论
- 用户删除评论
#### B端接口设计
- 管理员登录
- 运营人员登录
- 管理员审核话题
- 管理员审核运营人员
- 管理员删除评论
- 运营人员审核话题
- 运营人员审核评论
## 本地运行
```bash
$ npm i
$ npm run dev
$ open http://localhost:7001/
```

## 编译
```bash
$ npm run tsc
$ npm start
```

## 依赖环境
- Node.js 8.x
- Typescript 2.8+
