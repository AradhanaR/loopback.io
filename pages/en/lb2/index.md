---
lang: en
title: LoopBack 2.x
toc: false
keywords: LoopBack 2.x
tags: [getting_started]
sidebar: lb2_sidebar
permalink: /doc/en/lb2/index.html
summary: LoopBack is a highly-extensible, open-source Node.js framework that enables you to&#58; <ul><li>Create dynamic end-to-end REST APIs with little or no coding.</li><li>Access data from major relational and NoSQL databases, SOAP and REST APIs.</li><li>Incorporate model relationships and access controls for complex APIs.</li></ul>
---
Read [LoopBack core concepts](/doc/{{page.lang}}/lb2/LoopBack-core-concepts.html) to learn about key concepts you need to understand to use LoopBack.

Follow [Getting started with LoopBack](Getting-started-with-LoopBack.html) for a quick tutorial introduction.

Check out the [LoopBack Developer Forum](https://groups.google.com/forum/#!forum/loopbackjs) to ask questions and discuss how you are using LoopBack.

{% include styled-box.html
content="
[IBM API Connect](https://developer.ibm.com/apiconnect/) is an end-to-end API management solution that uses LoopBack to create APIs, and provides integrated build and deployment tools:

- **Integrated experience across the entire API lifecycle**, including API and micro-service creation in Node.js and Java.
-  **Self-service access to APIs** with built-in developer portals and social collaboration tools.
-  **Unified management and orchestration of Node.js and Java** for deployment on-premises and in Bluemix.
-  **Built-in security and gateway policies** with extensive security options and governance policies.

For more information, see [IBM API Connect](https://developer.ibm.com/apiconnect/).
" %}    

**If you are an IBM customer, for technical support see the [IBM Support Portal](http://www-01.ibm.com/support/docview.wss?uid=swg21593214).**

## The LoopBack framework

The LoopBack framework is a set of Node.js modules that you can use independently or together to quickly build REST APIs.

A LoopBack application interacts with data sources through the LoopBack model API, available locally within Node.js, [remotely over REST](/doc/{{page.lang}}/lb2/Built-in-models-REST-API), and via native client APIs for
[iOS, Android, and HTML5](/doc/{{page.lang}}/lb2/Client-SDKs). Using these APIs, apps can query databases,
store data, upload files, send emails, create push notifications, register users, and perform other actions provided by data sources and services.

Clients can call LoopBack APIs directly using [Strong Remoting](/doc/{{page.lang}}/lb2/Strong-Remoting.html), a pluggable transport layer that enables you to provide backend APIs over REST, WebSockets, and other transports.

The following diagram illustrates key LoopBack modules, how they are related, and their dependencies.

{% include image.html file="9830413.png" alt="LoopBack modules" %}

### LoopBack framework modules

<table style="width: 1000px;">
  <thead>
    <tr>
      <th style="width: 80px;">Category</th>
      <th style="width:200px;">Description</th>
      <th>Use to…</th>
      <th style="width: 280px;">Modules</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Models</td>
      <td>Model and API server</td>
      <td>Dynamically mock-up models and expose them as APIs without worrying about persisting.</td>
      <td>loopback</td>
    </tr>
    <tr>
      <td>Abstraction</td>
      <td>Model data abstraction to physical persistence</td>
      <td>Connect to multiple data sources or services and get back an abstracted model with CRUD capabilities independent of backing data source.</td>
      <td>loopback-datasource-juggler</td>
    </tr>
    <tr>
      <td>Initialization</td>
      <td>Application initialization</td>
      <td>Configure data sources, customize models, configure models and attach them to data sources; Configure application settings and run custom boot scripts.</td>
      <td>loopback-boot</td>
    </tr>
    <tr>
      <td>Sequencing</td>
      <td>Middleware execution</td>
      <td>Configure middleware to be executed at various points during application lifecycle.</td>
      <td>loopback-phase</td>
    </tr>
    <tr>
      <td>Data</td>
      <td>RDBMS and noSQL physical data sources</td>
      <td>Enable connections to RDBMS and noSQL data sources and get back an abstracted model.</td>
      <td markdown="1">
- loopback-connector-mongodb
- loopback-connector-mysql   
- loopback-connector-postgresql
- loopback-connector-msssql
- loopback-connector-oracle
- [Many others...](Connectors-reference.html)
</td>
    </tr>
    <tr>
      <td>Integration</td>
      <td>General system connectors</td>
      <td>Connect to an existing system that expose APIs through common enterprise and web interfaces</td>
      <td markdown="1">
- loopback-connector-rest   
- loopback-connector-soap
</td>
    </tr>
    <tr>
      <td>Components</td>
      <td>Add-ons to core LoopBack</td>
      <td>Integrate with pre-built services packaged into components.</td>
      <td markdown="1">
- loopback-component-push
- loopback-component-storage  
- loopback-component-passport
</td>
    </tr>
    <tr>
      <td>Clients</td>
      <td>Client SDKs</td>
      <td>Develop client app using native platform objects (iOS, Android, AngularJS) that interact with LoopBack APIs via REST.</td>
<td markdown="1">
- loopback-sdk-ios
- loopback-sdk-android
- loopback-sdk-angular
</td>
    </tr>
  </tbody>
</table>
