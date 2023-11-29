## 本项目实现的最终作用是基于JSP二手自行车在线销售商城平台系统
## 分为2个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 商品管理
 - 用户管理
 - 留言和公告管理
 - 管理员登录
 - 自行车分类管理
 - 订单管理
### 第2个角色为用户角色，实现了如下功能：
 - 在线留言
 - 查看自行车
 - 查看订单
 - 浏览自行车
 - 用户登录注册
 - 结算订单
## 数据库设计如下：
# 数据库设计文档

**数据库名：** ershoubike_shop

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [easybuy_comment](#easybuy_comment) |  |
| [easybuy_news](#easybuy_news) |  |
| [easybuy_order](#easybuy_order) |  |
| [easybuy_order_detail](#easybuy_order_detail) |  |
| [easybuy_product](#easybuy_product) |  |
| [easybuy_product_category](#easybuy_product_category) |  |
| [easybuy_shop](#easybuy_shop) |  |
| [easybuy_user](#easybuy_user) |  |

**表名：** <a id="easybuy_comment">easybuy_comment</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | EC_ID |   int   | 10 |   0    |    N     |  Y   |       | 评论ID  |
|  2   | EC_CONTENT |   varchar   | 255 |   0    |    N     |  N   |       | 评论内容  |
|  3   | EC_CREATE_TIME |   datetime   | 19 |   0    |    N     |  N   |       |   |
|  4   | EC_REPLY |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 回复  |
|  5   | EC_REPLY_TIME |   datetime   | 19 |   0    |    Y     |  N   |   NULL    |   |
|  6   | EC_NICK_NAME |   varchar   | 255 |   0    |    N     |  N   |       | 昵称  |

**表名：** <a id="easybuy_news">easybuy_news</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | EN_ID |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | EN_TITLE |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  3   | EN_CONTENT |   varchar   | 1000 |   0    |    N     |  N   |       |   |
|  4   | EN_CREATE_TIME |   datetime   | 19 |   0    |    N     |  N   |       |   |

**表名：** <a id="easybuy_order">easybuy_order</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | EO_ID |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | EO_USER_ID |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  3   | EO_USER_NAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | EO_USER_ADDRESS |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | EO_CREATE_TIME |   datetime   | 19 |   0    |    N     |  N   |       |   |
|  6   | EO_COST |   decimal   | 11 |   2    |    N     |  N   |       |   |
|  7   | EO_STATUS |   decimal   | 7 |   0    |    N     |  N   |       |   |
|  8   | EO_TYPE |   decimal   | 7 |   0    |    N     |  N   |       |   |

**表名：** <a id="easybuy_order_detail">easybuy_order_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | EOD_ID |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | EO_ID |   decimal   | 11 |   0    |    N     |  N   |       |   |
|  3   | EP_ID |   decimal   | 11 |   0    |    N     |  N   |       |   |
|  4   | EOD_QUANTITY |   decimal   | 7 |   0    |    N     |  N   |       |   |
|  5   | EOD_COST |   decimal   | 11 |   2    |    N     |  N   |       |   |

**表名：** <a id="easybuy_product">easybuy_product</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | EP_ID |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | EP_NAME |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  3   | EP_DESCRIPTION |   varchar   | 512 |   0    |    Y     |  N   |   NULL    |   |
|  4   | EP_PRICE |   decimal   | 11 |   2    |    N     |  N   |       |   |
|  5   | EP_STOCK |   decimal   | 11 |   0    |    N     |  N   |       |   |
|  6   | EPC_ID |   decimal   | 11 |   0    |    Y     |  N   |   NULL    |   |
|  7   | EPC_CHILD_ID |   decimal   | 11 |   0    |    Y     |  N   |   NULL    |   |
|  8   | EP_FILE_NAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="easybuy_product_category">easybuy_product_category</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | EPC_ID |   int   | 10 |   0    |    N     |  Y   |       | 分类ID  |
|  2   | EPC_NAME |   varchar   | 255 |   0    |    N     |  N   |       | 分类名称  |
|  3   | EPC_PARENT_ID |   decimal   | 11 |   0    |    N     |  N   |       | 父分类ID  |

**表名：** <a id="easybuy_shop">easybuy_shop</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | es_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | es_ep_file_name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | es_ep_name |   varchar   | 64 |   0    |    Y     |  N   |   NULL    |   |
|  4   | es_ep_price |   decimal   | 11 |   0    |    Y     |  N   |   NULL    |   |
|  5   | es_eod_quantity |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  6   | es_ep_stock |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  7   | es_ep_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  8   | es_eu_user_id |   varchar   | 64 |   0    |    Y     |  N   |   NULL    |   |
|  9   | es_valid |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="easybuy_user">easybuy_user</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | EU_USER_ID |   varchar   | 255 |   0    |    N     |  Y   |       |   |
|  2   | EU_USER_NAME |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  3   | EU_PASSWORD |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  4   | EU_SEX |   varchar   | 1 |   0    |    N     |  N   |       |   |
|  5   | EU_BIRTHDAY |   datetime   | 19 |   0    |    Y     |  N   |   NULL    |   |
|  6   | EU_IDENTITY_CODE |   varchar   | 60 |   0    |    Y     |  N   |   NULL    |   |
|  7   | EU_EMAIL |   varchar   | 80 |   0    |    Y     |  N   |   NULL    |   |
|  8   | EU_MOBILE |   varchar   | 11 |   0    |    Y     |  N   |   NULL    |   |
|  9   | EU_ADDRESS |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  10   | EU_STATUS |   decimal   | 7 |   0    |    N     |  N   |       |   |

**运行不出来可以微信 javape 我的公众号：源码码头**
