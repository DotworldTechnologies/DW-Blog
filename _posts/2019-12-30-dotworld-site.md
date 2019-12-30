---
layout: post
title:  "About Dotworld Site"
author: naveens
image: assets/images/dotworld-site/dotworld-site.png
description: "A tour on the technologies used in Dotworld Technologies Site"
featured: true
hidden: false
comments: false
---

A tour on the technologies used in Dotworld Technologies Site. You can learn about the implementation of SEO, Variable Fonts, Service Workers, PWA and more

#### Where it is hosted?

 Site is currently hosted on AWS Amplify which provides the necessary CI/CD integrations and also the SSL Certificates. We are using free tier of AWS Amplify which is well enough for the current traffic. One of the major problem with AWS Amplify is the redirections. I don't know now to configure url redirects.

#### About DNS

We are using Cloudflare as the DNS providers. They provide nice analytics on the page views, DDoS mitigation, caching and more. Cloudflare also provides the full SSL Certificates.

#### React

Yes! You read it right. We used React for developing a static site. We regret it. We are planing to move to next.js on our next major release. Since, I personally started learning React at the time of development, I though of going with React. But in the midway I realised there are many alternatives for static site development with Server Side Rendering(SSR).

#### Typography

The first huge stride in typographic detail on the web was the introduction of web fonts, which allowed designers and developers to use many other fonts besides the handful generally available on user’s operating systems. Currently to create a sentence with different weights we have to download three different font files, one for each type face. It looks cool on the website but it has noticeable impact on the performance and overall experience. 

To help solve this problem, one of the most impactful changes was made to the OpenType font format in collaboration by Adobe, Apple, Google, Microsoft and others. The solution was to enable font designers to provide various axes that could be adjusted dynamically by the software rendering the font, such as a web browser.

You can experience the power of variable fonts on dotworld product detail page. Learn more about vairable fonts [here](https://developer.microsoft.com/en-us/microsoft-edge/testdrive/demos/variable-fonts/)

![Variable fonts](//blog.dotworld.in/assets/images/dotworld-site/variable-fonts.gif)

#### Service Workers

Ever heard of opening a website in without internet? Try loading the Dotworld site with internet and disconnect the internet and try loading it again. Voila! It works just like that. No!. That's the magic of service workers. It caches the site in local storage and loads it from there when you have no internet access. There are many use cases for service workers. Offline loading is one of them.

#### PWA

A progressive web application (PWA) is a type of application software delivered through the web, built using common web technologies including HTML, CSS and JavaScript. Yes! You can install the Dotworld Site on your PC or Tablet or Mobile. And it works on offline too. It is not the exact use case of PWA, but **why not?**