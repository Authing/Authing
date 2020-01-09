<h1 align="center">
  <a href="https://authing.cn"><img width="550" src="https://cdn.authing.cn/authing-logo@2.png?a=1" alt="Authing" /></a>
</h1>

<h3 align="center">Authing —— Open Source IDaaS Provider that can Auth to Everything</h3>

Authing can help you rapidly integrate authentication and authorization for web, mobile, and legacy applications so you can focus on your core business.

We also deploy a cloud version, welcome to visit [Authing.cn](https://authing.cn) to try it out.

## What is Authing

Authing provides authentication and authorization as a service.

We are here to give developers and companies the building blocks they need to secure their applications without having to become security experts.

You can connect any application (written in any language or on any stack) to Authing and define the identity providers you want to use (how you want your users to log in).

Based on your app's technology, choose one of our SDKs (or call our API), and hook it up to your app. Now each time a user tries to authenticate, Authing will verify their identity and send the required information back to your app.

![https://github.com/Authing/authing/blob/master/imgs/authing-pos.png?raw=true](https://github.com/Authing/authing/blob/master/imgs/authing-pos.png?raw=true)

Develop Roadmap: [Authing Roadmap](https://github.com/Authing/authing/projects/1).

## What is IDaaS

Identity as a Service (IDaaS) is a new generation of cloud computing application, which is also called Authentication as a service (AAAS) in some occasions. IDaaS is a cloud infrastructure provided by a third party to solve the problems of identity authentication and user management.

IDaaS provides secure access and data storage. When a user or an app attempts to access a protected resource, he must provide authentication information. For example, if you want to use Facebook, you must provide the account password. For example, when you vote on some wechat pages, the system will obtain your wechat personal information. In this scenario, authentication service, as a judge, ensures that compliant users refuse illegal requests. When the authentication process is over, users can normally access the resources or application dashboard they want to access.

IDaaS generally need to support multiple languages:

1. Java/Kotlin - used to develop Andorid or Web applications;
1. Node/Python/PHP/Go/Dart/Rust - used to develop Back-end applications;
1. JavaScript - used to develop Web or Desktop applications;
1. Swift/Flutter/OC - used to develop iOS applications;

There's a huge amount of work to support all these languages, and IDaaS makes it easy because it has integrated all the technology stacks since it was born.

## Why Authing

- You built an awesome app and you want to add user authentication and authorization. Your users should be able to log in either with username/password or with their social accounts (Facebook, Twitter, and so on). You want to retrieve the user's profile after the login so you can customize the UI and apply your authorization policies.
- You built an API and you want to secure it with OAuth 2.0.
- You have more than one app, and you want to implement Single Sing On.
- You built a JavaScript front-end app and a mobile app, and you want them both to securely access your API.
- You have a web app which needs to authenticate users using SAML.
- You believe passwords are broken and you want your users to log in with one-time codes delivered by email or SMS.
- If one of your user's email addresses is compromised in some site's public data breach, you want to be notified, and you want to notify the users and/or block them from logging in to your app until they reset their password.
- You want to act proactively to block suspicious IP addresses if they make consecutive failed login attempts, in order to avoid DDoS attacks.
- You are part of a large organization who wants to federate their existing enterprise directory service to allow employees to log in to the various internal and third-party applications using their existing enterprise credentials.
- You don't want (or you don't know how) to implement your own user management solution. Password resets, creating, provisioning, blocking, and deleting users, and the UI to manage all these. You just want to focus on your app.
- You want to enforce multi-factor authentication when your users want to access sensitive data.
- You are looking for an identity solution that will help you stay on top of the constantly growing compliance requirements of SOC2, GDPR, OpenID Connect, and others.
- You want to use analytics to track users on your site or application. You plan on using this data to create funnels, measure user retention, and improve your sign up flow.

## Features

1. Mainstream third-party social login integrations;
1. SSO based on OAuth2.0, OpenID Connect, SAML, LDAP and CAS；
1. User management system based on Web (authorization management, identity management, basic data crud);
1. Cross platform integration capability (Android, IOS, Web);
1. Multi language SDK (JavaScript, node, Java, python, swift, PHP);
1. Secure identity authentication based on HTTPS, JWT, MD5, RSA, sha256, salt;
1. Mail service based on message queue, mail template configuration service based on Web and the ability to customize the third-party mail provider;
1. Biometric authentication based on fingerprint verification;
1. Easy to integrate and expand plug-in system and access to programmable rules;
1. User login location and IP monitoring;
1. Use the Wechat Miniprogram to scan the QRCode to log in;
1. Log in with mobile phone verification code;
1. Six lines of code generates a web login form;

### **Which industry standards does Authing use?**

Once upon a time, when computers were standalone systems, all the authentication and user data lived in a single machine. Times have changed, and now you can use the same login information across multiple apps and sites. This has been achieved through widespread adoption of identity industry standards across the web.

These are a set of open specifications and protocols that specify how to design an authentication and authorization system. They specify how you should manage identity, move personal data securely, and decide who can access applications and data.

The identity industry standards that we use here in Authing are:

- **OAuth 2**: an authorization standard that allows a user to grant limited access to their resources on one site, to another site, without having to expose their credentials. You use this standard every time you log in to a site using your Google account and you are asked if you agree with sharing your email address and your contacts list with that site.
- **Open ID Connect**: an identity layer that sits on top of OAuth 2 and allows for easy verification of the user's identity, as well the ability to get basic profile information from the identity provider.
- **JSON Web Tokens**: an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.
- **Security Assertion Markup Language (SAML)**: an open-standard, XML-based data format that allows businesses to communicate user authentication and authorization information to partner companies and enterprise applications their employees may use.

## Installation

## Quickstart

## Document

Document of authing is Deployed on Gitbook:

1. Mainland China users please visit: [docs.authing.cn](https://docs.authing.cn).
1. Non mainland China users please visit: [learn.authing.cn](https://learn.authing.cn)

## Videos And Articles

## Who Uses Authing?

Users are encouraged to add themselves to the Powered By page.

## Contributing

## Get Help

1. Join us on Gitter: [#authing-chat](https://gitter.im/authing-chat/community)
2. QQ group: 543317789

