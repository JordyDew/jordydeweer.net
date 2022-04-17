+++
title = "Why an Own Authentication System Is Not a Good Idea"
description = ""
author = "Jordy Deweer"
date = 2022-04-16T23:38:33+02:00
tags = []
draft = true
+++

Developing an own authentication system is a very bad idea. It's a big security risk you don't want to take, unless there's a very specific use case or need to do so.

In this article, I'll explain in more detail what the risks are and why third-party systems are 'better'.

## A few terms explained

Throughout this post, I'll be using some specific words. It's important you understand them and/or the difference between them.

* An authentication system: a libary or platform that makes sure the user can authenticate and sometimes authorize his/herself to your application. Good examples of third-party authentication platforms are Okta, Auth0, but also the well-known "Log in with Facebook" button.
* Authentication: It is the technique to proove an application you have access to secured parts. You can compare it with a lock and a key: when you have the correct key, you can 'authenticate' by opening the lock. That doesn't mean you have access to all parts of the house or the room behind the locked door. The best-knwon authetication system si a username and a password.
* Authorization: Authorization at the other hand is the mechanism to proove you have access to certain secured parts based on a role or some rights. For example: an employee can view his or her own file, but a manager can view all files of all employees.
* Data encryption: obscuring data so it can't be read easily. Instead you need a 'key' to decipher the contents.
* Data hashing: Making a unique 'fingerprint' of the stored data, which cannot be reversed to its original value. Two times the same word hashed with the same hashing algorithm will result in the same hash, but changing one little thing will result in a totally different hash. It's used to store passwords.
* A salt: something you add - mostly a cryptographic random value, that makes hashes even more difficult to crack using brute force.

## Security is a risk

> The most secure system is one that is turned off, covered in cement, and located at the bottom of the ocean
>
> &nbsp;&nbsp;&mdash; LinuxSecurity Founder Dave Wreski

That's true, no doubt, but not useful either. Instead, one should configure the system to be as secure as possible in the required use case.

The configuration is the first possible security issue. It is so easy to leave all values to their default, but that causes problems in the long run. Most applications have very flexible default configuration values. That ensures a smooth user experience for sure, but it doens't secure anything. You have to know the application you're installing well so you can change the important values to secure the application better. 'Dumb' values like CPU usage and maximum memory usage seem unimportant, but that's how DDoS attacks are cast and successful. So alter every (partially) important configuration option.

A second problem is data storage. From data encryption to hashing. It's all so important to keep upir's data secure. Passwords neet to be hashes, not encrypted. Each password needs its own salt.

Besides that, encryption with a key needs safe key storage, in some encrypted place. For that there exist third-party key vaults.

Apart from all this, your aplication itself has to be secure as well. It should never and nowhere allow for SQL Injection, crosss-site request forgery (CSRF) XSS (Cross-Site Scripting) and so forth. All these hacking techniques can cause your user's data to become freely available on the (dark) web for malafide people to misuse them.

## Possible solutions

Yeah, there are plenty of things you can do to protect your users.

### Third-party identity providers

These are companies which provide some platform to register your users, store their data and provide authentication and in some cases authorization as well.

Good options there are Okta and Auth0.  They provide functionality to do all identity management (accounts, profiles, data,...) for you. Is there something they don't save for you: add custom fields and let your users enter it there.

Authentication ahppens with a token, mostly. In the token, all data you need is provided and if not, you can request more details vai an API.

### Third-party actively maintained libraries and projects

The third option is for the users who need some more flexibility.

These give the option to implement your own identity management but by using well tested code and projects of others. YUou should use an actively maintained project so all possible security risks are handled imme3diately.

In .NET, IdentityServer4 is a good option. It provides a full implementation of all authentication and authorization technologies and methodologies you would like, e.g. OAuth2, JWT, Username/Password,...

## What if you need a custom system

If you _really need to_, then there is always the possibility to develop yuour own authentication system with all security measurements in place. However, keep in mind how dangerous that can be.

When you do so, make sure you have at least a good security team, security-aware developers and one or two penetration testers which can assess the self-written auth system.

## Conclusion

It is possible to develop your own authentication and authorizaion system if you really need to, if you have a good team of security-aware developers and security experts who can test/assess the self-developed system.

However, it';s more advisible to use a third-party provide or project which is continously developed and maintained, which provides correct encryption, hashing and so forth.

<hr />

Any comments? Please leave them. Think anyone could benefit from this blog? Share it!