# Authing 云端身份认证服务 白皮书

----------

### 下一代身份认证系统

Authing通过简单易用、可拓展的集成平台提供了复杂身份认证的解决方案,目标是保证每个月数以百万计的安全登录。为了达成这一目标，Authing在中国华南、华北双区域做了应用部署，保证了服务99.99%的可用性。

Authing的产品目标，是让用户用最少的时间和最少的代码拥有以下功能：
* 主流第三方OAuth配置接入；
* 基于Web的用户管理系统（权限管理、身份管理、基础CRUD）；
* 跨平台多终端集成能力（Android、iOS、HTML5）；
* 多语言SDK（JavaScript、Node、Java、Python、Swift、PHP）；
* 基于HTTPS、JWT、MD5、SHA256、Salt和非对称加密的安全身份认证；
* 基于消息队列的邮件服务、基于Web的邮件模版配置服务以及自定义第三方邮件服务的能力；
* 基于指纹验证等的生物认证方式；
* 易集成、易拓展的插件系统和可编程规则接入；
* 用户登录地点、IP监控；

Authing的商业目标，是成为全球最大的云端身份认证服务（甚至统一互联网所有的身份认证），使互联网变得更加安全。服务行业可包括：B2B/B2E/B2C/CIAM/零售业/媒体/医疗保健/通讯等。

在未来，Authing会接入区块链保证更安全的服务。

### 内容导览

[TOC]

### AaaS(Authentication as a Service)介绍

Authentication as a Service（AssS）是新一代云计算应用，在有些场合也被称作Identity as a Service（IDaaS）。AssS是由第三方提供的用于解决身份认证、用户管理等问题的云端基础设施。

AaaS提供了安全的准入许可和数据存储。当一名用户或一款应用试图访问受保护资源时，他必须提供认证资料。比如你若想使用Facebook必须提供账号密码，再比如在微信一些网页上进行投票时系统会获取你的微信个人资料。认证服务（Authentication Service）在这种场景下作为一个法官，保证合规的用户，拒绝非法的请求。当认证过程结束后，用户可以正常访问他们想要访问的资源或应用控制台。

认证服务一般需要支持多种语言：
* Java - 用来开发Andorid或Web应用；
* Node/Python/PHP - 用来开发后端应用；
* JavaScript - 用来开发客户端应用；
* Swift - 用来开发iOS应用；

除了语言层面的支持外，还应拥有富文本客户端、数据可视化支持来保证用户运营。

----------

### 认证流程

![auth_uml](http://usercontents.authing.cn/white_paper/authing_auth_uml.png)

认证通过后，后端会生成基于JWT规范的Token。客户端将Token放到HTTP协议中的```Authorzation```头中并加上标注```Bearer```即可进行登录验证。

流程如下：

 - 用户使用用户名密码来请求服务器
 - 服务器进行验证用户的信息
 - 服务器通过验证发送给用户一个token
 - 客户端存储token，并在每次请求时附送上这个token值
 - 服务端验证token值，并返回数据

#### JWT

JWT是由三段信息构成的，将这三段信息文本用.链接一起就构成了JWT字符串。就像这样:

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWV9.TJVA95OrM7E2cBab30RMHrHDcEfxjoYZgeFONFh7HgQ
```

##### JWT的构成
第一部分我们称它为头部（header),第二部分我们称其为载荷（payload, 类似于飞机上承载的物品)，第三部分是签证（signature).

###### header
jwt的头部承载两部分信息：

- 声明类型，这里是jwt
- 声明加密的算法 通常直接使用 HMAC SHA256

完整的头部就像下面这样的JSON：

``` javascript
{
  'typ': 'JWT',
  'alg': 'HS256'
}
```

然后将头部进行base64加密（该加密是可以对称解密的),构成了第一部分.
```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9
playload
```

载荷就是存放有效信息的地方。这个名字像是特指飞机上承载的货品，这些有效信息包含三个部分

- 标准中注册的声明
- 公共的声明
- 私有的声明

标准中注册的声明 (建议但不强制使用) ：

- ```iss```: jwt签发者
- ```sub```: jwt所面向的用户
- ```aud```: 接收jwt的一方
- ```exp```: jwt的过期时间，这个过期时间必须要大于签发时间
- ```nbf```: 定义在什么时间之前，该jwt都是不可用的.
- ```iat```: jwt的签发时间
- ```jti```: jwt的唯一身份标识，主要用来作为一次性token,从而回避重放攻击。


**公共的声明 ：**

公共的声明可以添加任何的信息，一般添加用户的相关信息或其他业务需要的必要信息.但不建议添加敏感信息，因为该部分在客户端可解密.

** 私有的声明 ：**

私有声明是提供者和消费者所共同定义的声明，一般不建议存放敏感信息，因为base64是对称解密的，意味着该部分信息可以归类为明文信息。

定义一个payload:

``` javascript
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```

然后将其进行base64加密，得到Jwt的第二部分。

```
eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWV9
```

**signature**

jwt的第三部分是一个签证信息，这个签证信息由三部分组成：

- header (base64后的)
- payload (base64后的)
- secret

这个部分需要base64加密后的header和base64加密后的payload使用.连接组成的字符串，然后通过header中声明的加密方式进行加盐secret组合加密，然后就构成了jwt的第三部分。

``` javascript
var encodedString = base64UrlEncode(header) + '.' + base64UrlEncode(payload);

var signature = HMACSHA256(encodedString, 'secret'); // TJVA95OrM7E2cBab30RMHrHDcEfxjoYZgeFONFh7HgQ
```
将这三部分用.连接成一个完整的字符串,构成了最终的jwt:

```
  eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWV9.TJVA95OrM7E2cBab30RMHrHDcEfxjoYZgeFONFh7HgQ
```

注意：secret是保存在服务器端的，jwt的签发生成也是在服务器端的，secret就是用来进行jwt的签发和jwt的验证，所以，它就是你服务端的私钥，在任何场景都不应该流露出去。一旦客户端得知这个secret,那就意味着客户端是可以自我签发jwt了。


### 技术架构

Authing拥有4个模块，这四个模块支撑了Authing的所有流量，分别是：用户服务（Users）、OAuth服务（OAuth）、邮件服务（Emails）和支付服务（Pay）。此四项服务虽然都是分开部署，但有一定的强关联性。同时，为了保证服务的高可用，在互相请求时，会进行错误捕捉，在发生错误时，会使用默认数据。因此在某个服务不可用时，可能会导致某些服务的配置失效。

#### 后端

后端使用Node.js开发，结合RESTful API和GraphQL进行数据交换。在某些场景下（如发送邮件、日志记录）使用RabbitMQ实现消息队列。
整体使用docker-compose进行部署，全程无人化。

##### Koa.js

Koa.js是Authing主要使用的后端框架，和他一起配套使用的koa生态还包括：koa-bodyparser、koa-convert、koa-cors、koa-router。

##### GraphQL

使用了GraphQL官方推荐的客户端apollo-client进行GraphQL应用的开发。

##### 消息队列

使用由Docker构建的RabbtMQ和基于Node的rabbit.js。我们内部定义了一套RabbitMQ消息通信的规范。 

``` javascript
{
    action: 'ACTION_NAME', //要执行的动作（函数）
    payload: {} //附带的参数
}
```

#### 前端

Authing的前端基于现代Web技术开发而成，为SAP应用。具有响应式、国际化等特性。

前端的基本构件如下：

- **Vue**：Authing客户端的基石
- **状态管理**：使用Vuex
- **国际化**：使用vue-i18n
- **界面**：iView(Ant.design的Vue版)

基本上就是Vue全家桶。

除了基础的客户端功能外，Authing还应提供服务端渲染（SSR）的功能，这方面会选择Next.js作为主要的开发框架。

#### DevOps

Authing的运维指标是无人化、自动化。因此在前期采用以下技术方案（DevOps会随业务增长而改进）：

- Docker
- 微服务
- Nginx负载均衡
- Git Hook
- 业务与数据分离
- 核心业务多节点、多进程运行
- 跨主机、多节点部署
- 数据库主+从+仲裁部署+多节点部署

Authing关于DevOps的最终目标是实现ChatOps。

##### ChatOps

ChatOps简单来说就是聊天机器人+RESTful实现运维自动化的工具，他相当于一个最勤劳，最好沟通，从不休假并且随叫随到的同事。

ChatOps可以让我们在工作中pair all the time。
![pair all the time](https://upload-images.jianshu.io/upload_images/5064655-cecdf6d72a2fc425.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/700)

ChatOps这块业务有可能会成为继认证之后Authing的下一块拥有巨大增长潜力的业务。

----------

### SDK

SDK是Authing官方及社区提供的方便用户进行多端接入的开源软件包，该开源软件包支持以下语言：

- Java
- C#
- PHP
- Python
- Node/JavaScript
- Swift

查看官方文档，[请点击这里](http://docs.authing.cn)。

#### SDK规范

为了减少开发者在不同平台的学习成本，所以Authing必须保证SDK接口的一致性，当然在不同语言情境下，会做出少量调整。

##### 包名称

Authing官方提供的包统一命名为：```authing-js-sdk```。

这样无论在Python语言下还是Node语言下都可以以相同包名称进行安装。

如：

**Python**
``` shell
$ pip install authing-js-sdk
```

**Node/JavaScript**

``` shell
$ npm install authing-js-sdk --save
```

##### 初始化

在进行代码初始化时必须是初始化一个类，该类的构造函数接收一个对象作为参数：

``` javascript
{
    clientId: 'CLIENT_ID',
    secret: 'APP_SECRET'
}
```

如(**JavaScript**)：

``` shell
var auth = new Authing({
    clientId: 'your_client_id',
    secret: 'your_app_secret'
});
```

该构造函数在认证通过时应返回一个新的对象，该对象每次发送请求时携带SDK经过验证的Token。

如(**JavaScript**)：

``` shell
auth.then(function(validAuth) {

    //验证成功后返回新的authing-js-sdk实例(validAuth)，可以将此实例挂在全局

}).catch(function(error) {
    //验证失败
    console.log(error);
});
```

如果使用JavaScript开发SDK，必须保证兼容async/await和Promise。

##### 对象方法

可参考文档内的[用户接口列表](http://docs.authing.cn/#/user_service/user_service)。

### 未来规划

Authing的业务目标不会仅局限于用户认证这一块，云计算、区块链、大数据以及人工智能都有Authing的立足之地。

Authing的技术探索也一定是无边界的。

#### 云计算

Authing的定位是一家**云计算公司**，提供**AaaS**服务。在未来，Authing会有数十亿的认证事件处理，底层需要稳健的基础设施作支撑。

Authing会在大量使用现有云计算平台的基础上，实现函数计算（lambda computing），这是无服务器（serverless）技术的基础设施。

##### 函数计算和无服务器架构

所谓函数计算，就是指将函数直接上传至云计算平台，无需考虑服务器，为计算时长付费。

函数计算和无服务器架构是相辅相成的结果，同时需要大量的DevOps，最终会发展成为NoOps，这和Authing ChatOps的展望不谋而合。

所以函数计算和无服务器架构也会是Authing重点发力的一块业务，也是支撑Authing未来过亿身份认证的基石。

#### 区块链

区块链是分布式数据存储、点对点传输、共识机制、加密算法等计算机技术的新型应用模式。

在身份认证这种场景下，用户最大的要求是**安全**。而区块链就使现有身份认证变得安全成为可能。尤其是其中的非对称加密和授权技术，存储在区块链上的信息是公开的，但是账户身份信息是高度加密的，只有在数据拥有者授权的情况下才能访问到，从而保证了数据的安全和个人的隐私（即用户数据属于注册商，可以打消用户对于**Authing官方**可能会窃取用户信息的疑虑）。

基于分布式、点对点的特性，也可以使Authing的数据存储更加可靠。

#### 大数据

基于众多的登录数据，Authing可以做大量的数据分析和可视化。

以下场景可得到应用（不断拓展）：

- 分析人口流通（按行业）；
- 分析人口睡眠及活跃时间（按行业）；
- 分析人口地理、年龄分布；

基于以上数据，Authing可实现大量的数据可视化。

#### 人工智能

在人工智能方面，Authing可实现生物认证，如：

- 指纹识别
- 人脸识别
- 眼膜识别

从而保证认证过程的安全性更上一层楼。
