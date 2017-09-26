# BookLibrary
NET Core 2.0 + DDD + CQRS + ES + RabbitMQ练习项目

## 服务说明
系统中提供验证服务，书籍库存服务，书籍租赁服务

### 验证服务
* 提供管理员及会员的登录

### 书籍库存服务
* 管理员可以管理书籍库存（新增，修改，删除）
* 为了简化逻辑，每一种书籍只有一本
* 书籍拥有以下属性
    *    书籍名称
    *    ISBN
    *    描述
* ISBN是系统中是唯一的，如果新增/修改库存书籍，需要保证ISBN系统唯一
* 如果书籍已经租借出去，书籍不能删除

### 书籍租赁服务
* 已租借状态的书籍不能再次租借
* 会员每次只能租借最多3本书
