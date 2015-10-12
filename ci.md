# apigee-2015-notes
Notes from the October 2015 "I Love APIs" conference in San Jose

# Continuous Integration - https://github.com/mhuisman/apigee-2015-nodejs-ci

* Manual intevention in CI process to force a success - the Volkswagen approach.  False positives = expensive!

* CI does not necessarily mean automatic deploy to production, each organization must make its own decisions

* Apigee does not have native support of red/black or canary deployments - would have to be implemented ourselves

setup:

* update node:  npm cache clean ; npm update -g

* install yeoman: npm install -g yo

* install grunt: npm install -g grunt-cli

* install grunt plugin: npm install -g generator-apigee-deploy-grunt-api

* run yo: yo apigee-deploy-grunt-api