# Docker-UbiFunction-node10Action

Base Docker to execute UbiFunction python actions. Based on the original IBM Openwhisk action runner: https://github.com/ibm-functions/runtime-nodejs and Apache Openwhisk node action: https://github.com/apache/openwhisk-runtime-nodejs

# Supported Libraries

Default Python packages supported by the container

- @cloudantcloudant:  4.3.1:
- @ibmfunctions/iam-token-manager: 1.0.5:
- @sendgridmail: 7.4.4:
- @wiotpsdk: 0.7.8:
- amqplib: 0.8.0:
- apn: 2.2.0:
- async: 3.2.0:
- axios: 0.21.1:
- bent: 7.3.12:
- bodyparser: 1.19.0:
- btoa: 1.2.1:
- bufferutil: 4.0.3:
- canvas: 2.8.0:
- cassandradriver: 4.6.3:
- commander: 7.2.0:
- composeaddresstranslator: 1.0.4:
- consul: 0.40.0:
- cookieparser:  1.4.5:
- corejs:  3.13.0:
- elasticsearch: 16.7.2:
- errorhandler: 1.5.1:
- etcd3: 1.1.0:
- express: 4.17.1:
- expresssession:  1.17.2:
- formidable: 1.2.2:
- glob: 7.1.7:
- gm: 1.23.1:
- got: 11.8.2:
- ibmcos-sdk:  1.10.0:
- ibm_db: 2.7.3:
- ibmwatson:  6.0.4:
- iconvlite:  0.6.3:
- jest: 27.0.1:
- jsdom: 16.6.0:
- jsforce: 2.0.0-alpha.12:
- jsonwebtoken: 8.5.1:
- lodash: 4.17.21:
- log4js: 6.3.0:
- marked: 2.0.5:
- merge: 2.1.1:
- moment: 2.29.1:
- mongodb: 3.6.9:
- mustache: 4.2.0:
- mysql: 2.18.1:
- nano: 9.0.3:
- needle: 2.6.0:
- nodemailer: 6.6.1:
- oauth2server:  3.1.1:
- openwhisk: 3.21.4:
- pathto-regexp:  6.2.0:
- pg: 8.6.0:
- process: 0.11.10:
- pug: 3.0.2:
- redis: 3.1.2:
- rimraf: 3.0.2:
- semver: 7.3.5:
- serializeerror:  8.1.0:
- servefavicon:  2.5.0:
- socketio:  4.1.2:
- socketio-client:  4.1.2:
- superagent: 6.1.0:
- swaggertools:  0.10.4:
- tmp: 0.2.1:
- tsjest:  27.0.1:
- twilio: 3.63.0:
- underscore: 1.13.1:
- urlpattern:  1.0.3:
- utf8-validate:  5.0.5:
- uuid: 8.3.2:
- validator: 13.6.0:
- vcap_services: 0.7.1:
- when: 3.7.8:
- winston: 3.3.3:
- ws: 7.4.6:
- xlsx: 0.17.0:
- xml2js: 0.4.23:
- xmlhttprequest: 1.8.0:
- yauzl: 2.10.0:
- yazl: 2.5.1"
# Examples

## Hello Action
Write a simple function and save it as hello.js

```js
function main(args){
    console.log("hello!");
    return {args: args}
}
```

## IBM Cloud Functions (based on Apache OpenWhisk)

### To use as a node kind action

```bash
ibmcloud wsk action create helloJs hello.js --kind nodejs:10
```

### Invoke the action

```bash
ibmcloud wsk action invoke helloJs
```

### How to use as a docker Action locally

To use as a docker action based on this container

```
ibmcloud wsk action update helloJs hello.js --docker ubidots/docker-ubifunction-node10Action
```
