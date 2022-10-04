# edu-monitoring

## Monitoring

> Monitoring is an important part of internet development. Monitoring services offer automated systems to check the health of your systems and also monitor for attacks and other unhealthy states.

[Pingdom](https://www.pingdom.com/product/uptime-monitoring/) -> [Getting started](https://www.youtube.com/watch?v=XT3cAIPCO1E)  

[PC Magazine about monitoring services](https://uk.pcmag.com/migrated-46739-onlinecloud-backup-services/72231/the-best-website-monitoring-services-for-2020)  

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
git init
npm init -y
mkdir routes
curl -L https://gist.github.com/miwashiab/560c59105116df6b728e2057457c246a/raw/server.js -o server.js
curl -L https://gist.github.com/miwashiab/3bb79a44d694664b46a31c8645aa816e/raw/healthcheck.js -o ./routes/healthcheck.js
curl -L https://gist.github.com/miwashiab/3378fc2e4ab5d2691fa5978822721796/raw/.gitignore -o .gitignore

npm install express --save
npm install healthcheck --save
npm install nodemon --save-dev
npm install nodejs-health-checker
npm pkg set main="server.js"
npm pkg set scripts.start="node server.js" 
npm pkg set scripts.dev="nodemon server.js" 
git add .
git commit -m "Initial Commit"
code .
```
