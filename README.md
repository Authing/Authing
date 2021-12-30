<h1 align="center">
  <a href="https://authing.cn"><img width="300" src="https://files.authing.co/authing-console/authing-logo-new-20210924.svg?a=1" alt="Authing" /></a>
</h1>
<div align="center">
  <a href="https://docs.authing.cn/v2/" target="_blank"><img src="https://img.shields.io/badge/docs-passing-success"></a>
  <a href="https://forum.authing.cn/" target="_blank"><img src="https://img.shields.io/badge/chat-on%20forum-blue"></a>
  <a href="javascript:;"><img src="https://img.shields.io/badge/License-MIT-brightgreen"></a>
  <a href="javascript:;"><img src="https://img.shields.io/badge/PRs-welcome-green"></a>
</div>
<br />


<h3 align="center">Authing —— IDaaS Provider that can Auth to Everything</h3>

Authing can help you rapidly integrate authentication and authorization for web, mobile, and legacy applications so you can focus on your core business.

We have deployed a cloud version, welcome to visit [Authing.cn](https://authing.cn) to try it out.

## What is Authing

Authing provides authentication and authorization as a service.

We are here to give developers and companies the building blocks they need to secure their applications without having to become security experts.

You can connect any application (written in any language or on any stack) to Authing and define the identity providers you want to use (how you want your users to log in).

Based on your app's technology, choose one of our SDKs (or call our API), and hook it up to your app. Now each time a user tries to authenticate, Authing will verify their identity and send the required information back to your app.

![https://cdn.authing.cn/github/customers/authing-pos.png](https://cdn.authing.cn/github/customers/authing-pos.png)

Develop Roadmap: [Authing Roadmap](https://github.com/Authing/authing/projects/1).

<details>
<summary><strong>What is IDaaS ?</strong></summary>

Identity as a Service (IDaaS) is a new generation of cloud computing application, which is also called Authentication as a service (AaaS) in some occasions. IDaaS is a cloud infrastructure provided by a third party to solve the problems of identity authentication and user management.

IDaaS provides secure access and data storage. When a user or an app attempts to access a protected resource, he must provide authentication information. For example, if you want to use Facebook, you must provide the account password. For example, when you vote on some wechat pages, the system will obtain your wechat personal information. In this scenario, authentication service, as a middleware, ensures that compliant users refuse illegal requests. When the authentication process is over, users can normally access the resources or application dashboard they want to access.

IDaaS generally need to support multiple languages:

1. **Java/Kotlin** - used to develop Andorid or Web applications.
1. **Node/Python/PHP/Go/Dart/Rust...** - used to develop Back-end applications.
1. **JavaScript** - used to develop Web or Desktop applications.
1. **Swift/Flutter/OC** - used to develop iOS applications.

There's a huge amount of work to support all these languages, and IDaaS makes it easy because it has integrated all the technology stacks since it was born.
</details>

## Why Authing

- You built an awesome app and you want to add user authentication and authorization. Your users should be able to log in either with username/password or with their social accounts (Facebook, Twitter, and so on). You want to retrieve the user's profile after the login so you can customize the UI and apply your authorization policies.
- You built an API and you want to secure it with OAuth 2.0.
- You have more than one app, and you want to implement Single Sing On.
- You built a JavaScript front-end app and a mobile app, and you want them both to securely access your API.
- You have a web app which needs to authenticate users using SAML.
- You believe passwords are broken and you want your users to log in with one-time codes delivered by email or SMS.
<details>
<summary><strong>Click here to see more reasons</strong></summary>

<ul>
<li>If one of your user's email addresses is compromised in some site's public data breach, you want to be notified, and you want to notify the users and/or block them from logging in to your app until they reset their password.</li>
<li>You want to act proactively to block suspicious IP addresses if they make consecutive failed login attempts, in order to avoid DDoS attacks.</li>
<li>You are part of a large organization who wants to federate their existing enterprise directory service to allow employees to log in to the various internal and third-party applications using their existing enterprise credentials.</li>
<li>You don't want (or you don't know how) to implement your own user management solution. Password resets, creating, provisioning, blocking, and deleting users, and the UI to manage all these. You just want to focus on your app.</li>
<li>You want to enforce multi-factor authentication when your users want to access sensitive data.</li>
<li>You are looking for an identity solution that will help you stay on top of the constantly growing compliance requirements of SOC2, GDPR, OpenID Connect, and others.</li>
<li>You want to use analytics to track users on your site or application. You plan on using this data to create funnels, measure user retention, and improve your sign up flow.</li>
</ul>
</details>

## Features

1. Mainstream third-party social login integrations(Wechat, QQ, Github, Weibo, DingTalk, Alipay).
1. SSO based on OAuth2.0, OpenID Connect, SAML, LDAP and CAS.
1. User management system based on Web (authorization management, identity management, basic data crud).
1. Role Based Access Control to authorizate users.
1. User's geographical location record, login and registration history, easy to audit.
1. Multifactor Authentication System.
1. Cross platform integration capability (Android, iOS, Web).
1. Multi language SDK (JavaScript, Node, Java, Python, OC, PHP, 小程序, ReactNative).
1. Secure identity authentication based on HTTPS, JWT, MD5, RSA, sha256, salt.
1. Mail service based on message queue, mail template configuration service based on Web and the ability to customize the third-party mail provider.
1. Easy to integrate and expand plug-in system and access to programmable rules.
1. User login location and IP monitoring.
1. Use the Wechat Miniprogram to scan the QRCode to log in.
1. Easy implementation of web page QRCode scanning login in app.
1. Log in with mobile phone verification code.
1. Six lines of code generates a cross-platform login form.

<details>
<summary><strong>Which industry standards does Authing use?</strong></summary>
Once upon a time, when computers were standalone systems, all the authentication and user data lived in a single machine. Times have changed, and now you can use the same login information across multiple apps and sites. This has been achieved through widespread adoption of identity industry standards across the web.

These are a set of open specifications and protocols that specify how to design an authentication and authorization system. They specify how you should manage identity, move personal data securely, and decide who can access applications and data.

The identity industry standards that we use here in Authing are:

- **OAuth 2**: an authorization standard that allows a user to grant limited access to their resources on one site, to another site, without having to expose their credentials. You use this standard every time you log in to a site using your Google account and you are asked if you agree with sharing your email address and your contacts list with that site.
- **Open ID Connect**: an identity layer that sits on top of OAuth 2 and allows for easy verification of the user's identity, as well the ability to get basic profile information from the identity provider.
- **JSON Web Tokens**: an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.
- **Security Assertion Markup Language (SAML)**: an open-standard, XML-based data format that allows businesses to communicate user authentication and authorization information to partner companies and enterprise applications their employees may use.
</details>

<details>
<summary><strong>Click here to see part of screenshots of Authing</strong></summary>

<img src="https://cdn.authing.cn/github/screenshots/sample-sso.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/dashboard.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/dash-geo.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/social-login.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/users-management.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/users.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/geo-user.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/email-tpl.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/email-tpls.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/api.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/sdk.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/security.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/settings.png" width="250px"/>
<img src="https://cdn.authing.cn/github/screenshots/audit.png" width="250px"/>

</details>

## Built With

1. **TypeScript** - TypeScript is a superset of JavaScript that compiles to clean JavaScript output.
1. **Nest.js** - A progressive Node.js framework.
1. **Vue.js** - A JavaScript framework for building UI on the web.
1. **MongoDB** - A NoSQL Database.
1. **GraphQL** - A query language and execution engine tied to any backend service.
1. **Docker** - Containers.
1. **RabbitMQ** - Open source multi-protocol messaging broker.

## Installation

Under Construction.

## Quickstart

Under Construction.

## Document

Document of authing is Deployed on Gitbook:

1. Mainland China users please visit: [docs.authing.cn](https://docs.authing.cn).
1. Non mainland China users please visit: [learn.authing.cn](https://learn.authing.cn).

## Videos And Articles

1. [Authing 是什么以及为什么需要 Authing](https://mp.weixin.qq.com/s/ispl1F1q5hhUEKSfzOsqgw)
1. [为什么身份认证值得上云](https://mp.weixin.qq.com/s/TlYmDRg1q_glJ7Icsj0arw)
1. [一键认证让移动应用都不需要发短信了，Web 怎么办？](https://mp.weixin.qq.com/s/iL0OW-q7ljP0S6769GMdPg)
1. [函数计算在身份认证云中的应用场景](https://mp.weixin.qq.com/s/cthD1Df19v15QEovKkeSzw)
1. [用 Authing 10 分钟实现单点登录](https://mp.weixin.qq.com/s/ZVGZA9zx-v2atBwqF5l4Nw)
1. [Serverless 最佳实践：在云上认证身份授权资源](https://mp.weixin.qq.com/s/ZO28EBS0kZAJJzOLg2mdZQ)
1. [为什么所有软件都应该使用单点登录来管理用户？](https://mp.weixin.qq.com/s/XaMaiZ0NC7xydQPI1CraIQ)
1. [身份上云 or 自建？这里有 20 个问题值得你思考](https://mp.weixin.qq.com/s/_-oJhTVLhre3uk-knR5Dnw)
1. [Auth0 和 Authing，谁是身份云的高脚杯](https://mp.weixin.qq.com/s/_o1P00IEWU_3_k4AGaQZdQ)
1. [五分钟接入微信网页授权登录](https://mp.weixin.qq.com/s/YFrVFEK_xCtOE7dFZEzyyw)
1. [六个步骤实施零信任网络](https://mp.weixin.qq.com/s/0us26wUrDtVHB6Ir99s2aA)
1. [五分钟实现小程序登录](https://mp.weixin.qq.com/s/Y7Y2lYY2tO2Z2j8zNku_tg)
1. [Authing 开发资源最全合集](https://mp.weixin.qq.com/s/coOqRAu7G5FdQlWU8FiZBA)
1. [五分钟在移动端实现完整用户认证](https://mp.weixin.qq.com/s/_-zS618cVuSyVGvhcAFOeg)
1. [使用 Authing 快速集成 AWS 服务](https://mp.weixin.qq.com/s/G8Hdf7O4_h48mk5PkbkOxA)
1. [从几个细节看身份认证这件事不简单](https://mp.weixin.qq.com/s/crLNBsGYQP9i0qtsQfQrAQ)
1. [GraphQL 在身份认证场景中的深度使用实践（一）](https://mp.weixin.qq.com/s/BSnEptyBg7HAYGyKHQ-Xjg)

## Who Uses Authing?

<p float="left">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/seu.png" width="60px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/kingdomai.png" width="60px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/KaiYuanShe-logo.png" width="60px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/pocoweb.jpg" width="60px">
<br>
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/hephep.gif" width="120px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/memect.png" width="120px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/chatopera.png" width="120px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/juzi.png" width="120px">
<br>
<img style="display:inline-block" src="https://fcc.authing.cn/images/logo-navbar.png" width="120px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/stackchat.png" width="120px">
<img style="display:inline-block" src="https://cdn.authing.cn/github/customers/lz.png" width="120px">
</p>

Users are encouraged to add themselves to the Powered By page.

## Contributing

Under Construction.

## Community

1. Join us on forum: [#authing-chat](https://forum.authing.cn/)
2. QQ group: 543317789

### Wechat

<img src="https://usercontents.authing.cn/qrcode_for_steamory.jgp" width="150px">

## Contributors
<div>
  <a href="https://github.com/leinue"><img width="40px" src="https://avatars.githubusercontent.com/u/2469688?v=4" /></a>
  <a href="https://github.com/lixpng"><img width="40px" src="https://avatars.githubusercontent.com/u/19266401?v=4" /></a>
  <a href="https://github.com/kelvinji2009"><img width="40px" src="https://avatars.githubusercontent.com/u/881201?v=4" /></a>
  <a href="https://github.com/vexilligera"><img width="40px" src="https://avatars.githubusercontent.com/u/20215432?v=4" /></a>
  <a href="https://github.com/gouyaming"><img width="40px" src="https://avatars.githubusercontent.com/u/24635178?v=4" /></a>
  <a href="https://github.com/willin"><img width="40px" src="https://avatars.githubusercontent.com/u/1890238?v=4" /></a>
  <a href="https://github.com/TingYinHelen"><img width="40px" src="https://avatars.githubusercontent.com/u/14006826?v=4" /></a>
  <a href="https://github.com/Meeken1998"><img width="40px" src="https://avatars.githubusercontent.com/u/42825670?v=4" /></a>
  <a href="https://github.com/yelexin"><img width="40px" src="https://avatars.githubusercontent.com/u/27125445?v=4" /></a>
  <a href="https://github.com/HowieWolf"><img width="40px" src="https://avatars.githubusercontent.com/u/14340114?v=4" /></a>
  <a href="https://github.com/JackJin2014"><img width="40px" src="https://avatars.githubusercontent.com/u/1982447?v=4" /></a>
  <a href="https://github.com/fuergaosi233"><img width="40px" src="https://avatars.githubusercontent.com/u/22197568?v=4" /></a>
  <a href="https://github.com/clearloop"><img width="40px" src="https://avatars.githubusercontent.com/u/26088946?v=4" /></a>
  <a href="https://github.com/liaochangjiang"><img width="40px" src="https://avatars.githubusercontent.com/u/35447896?v=4" /></a>
  <a href="https://github.com/andyzhaozhao"><img width="40px" src="https://avatars.githubusercontent.com/u/7730080?s=96&v=4" /></a>
  <a href="https://github.com/authing-wangck"><img width="40px" src="https://avatars.githubusercontent.com/u/78251114?s=96&v=4" /></a>
  <a href="https://github.com/chho93"><img width="40px" src="https://avatars.githubusercontent.com/u/56515268?s=96&v=4" /></a>
  <a href="https://github.com/Donglyrun"><img width="40px" src="https://avatars.githubusercontent.com/u/17630579?s=120&v=4" /></a>
  <a href="https://github.com/gouyaming"><img width="40px" src="https://avatars.githubusercontent.com/u/24635178?s=96&v=4" /></a>
  <a href="https://github.com/lancemao"><img width="40px" src="https://avatars.githubusercontent.com/u/5020396?s=96&v=4" /></a>
  <a href="https://github.com/limejuiceOwO"><img width="40px" src="https://avatars.githubusercontent.com/u/59465535?v=4" /></a>
  <a href="https://github.com/luojielin"><img width="40px" src="https://avatars.githubusercontent.com/u/29780568?v=4" /></a>
  <a href="https://github.com/Mereithhh"><img width="40px" src="https://avatars.githubusercontent.com/u/22872368?s=96&v=4" /></a>
  <a href="https://github.com/qianfeiqianlan"><img width="40px" src="https://avatars.githubusercontent.com/u/12892568?s=96&v=4" /></a>
  <a href="https://github.com/shangsinian"><img width="40px" src="https://avatars.githubusercontent.com/u/6363555?s=96&v=4" /></a>
  <a href="https://github.com/stan071408"><img width="40px" src="https://avatars.githubusercontent.com/u/6972394?s=96&v=4" /></a>
  <a href="https://github.com/wajiao"><img width="40px" src="https://avatars.githubusercontent.com/u/20143458?s=96&v=4" /></a>
  <a href="https://github.com/wedreamer"><img width="40px" src="https://avatars.githubusercontent.com/u/43949542?s=96&v=4" /></a>
  <a href="https://github.com/Xuancaosu"><img width="40px" src="https://avatars.githubusercontent.com/u/51688262?s=96&v=4" /></a>
  <a href="https://github.com/zhaoyiming0803"><img width="40px" src="https://avatars.githubusercontent.com/u/25874685?s=96&v=4" /></a>
</div>

## License

MIT
