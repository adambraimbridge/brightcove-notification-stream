# Brightcove Dynamo Stream Call Back Updater

## Pre-requistes

### Install node and npm
#### Mac
```
$ brew install node
```

### Install Gulp
#### Mac
```
$ npm install gulp -g
```

## Deployment

### Setup

### AWS Credentials

#### Local
If deploying from a non-ec2 instance setup aws profile
http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-multiple-profiles

#### Set default profile in shell
'''export set AWS_DEFAULT_PROFILE=staging'''

#### Run gulp deployment
'''gulp --env=staging --lambdarole=FTFlexServices-Deployer --account=528773984231 --region=eu-west-1 --vpcSecurityGroupId=sg-e69c6480 --subNetOne=subnet-8406d5e0 --subNetTwo=subnet-0ecede57 --subNetGroupId=videotest --brightCoveClientId=XXX --brightCoveClientSecret=YYY --brightcoveAccount=2221711291001'''

## Testing

```
$ npm install nodeunit -g
$ nodeunit test/index.good.test.js
```
