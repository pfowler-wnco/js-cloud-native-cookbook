# Implementing backpressure and rate limiting

## How to do it...
1. sls create --template-url https://github.com/danteinc/js-cloud-native-cookbook/tree/master/ch8/backpressure-ratelimit --path cncb-backpressure-ratelimit
2. cd cncb-backpressure-ratelimit
3. npm install
4. npm test -- -s $MY_STAGE
5. npm run dp:lcl -- -s $MY_STAGE
6. sls invoke -f simulate -r us-east-1 -s $MY_STAGE
7. sls logs -f listener -r us-east-1 -s $MY_STAGE --filter 'event count'
8. npm run rm:lcl -- -s $MY_STAGE
