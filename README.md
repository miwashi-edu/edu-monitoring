# edu-monitoring

## Monitoring

> Monitoring is an important part of internet development. Monitoring services offer automated systems to check the health of your systems and also monitor for attacks and other unhealthy states.

(PC Magazine about monitoring services)[https://uk.pcmag.com/migrated-46739-onlinecloud-backup-services/72231/the-best-website-monitoring-services-for-2020]  

## Node packages for monitoring

[healthcheck](https://www.npmjs.com/package/healthcheck)  
[nodejs-health-checker](https://www.npmjs.com/package/nodejs-health-checker)  
[Nodejs Healthcheck](https://www.npmjs.com/package/@hmcts/nodejs-healthcheck)  


## Instructions

```bash
cd ~
cd ws
mkdir edu-monitoring
cd edu-monitoring
npm init -y
mkdir routes
curl -L https://gist.github.com/miwashiab/560c59105116df6b728e2057457c246a/raw/server.js -o server.js
curl -L https://gist.github.com/miwashiab/560c59105116df6b728e2057457c246a/raw/server.js -o ./routes/healthcheck.js
npm install express --save
npm install healthcheck --save
npm install nodemon --save-dev
npm install nodejs-health-checker
npm pkg set main="server.js"
npm pkg set scripts.start="node server.js" 
npm pkg set scripts.dev="nodemon server.js" 
code .
```
