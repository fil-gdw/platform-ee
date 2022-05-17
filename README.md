# GDW: Coding Problems for Expert Engineer

### Problem Statement 1/2

Write a Lambda Function that when invoked with a predefined event can make a GET call to a 3rd party API `https://schedule.com/schedules/self`

Please note that:
1. API Keys for the authentication are stored in a secrets manager : `schedules-secrets`, as a key value pair: 
```json
{ "api-key": "12345678-abcd-0987-efgh" }
```
2. All outbound http/s calls must go via a provided proxy in the account. Proxy end point is: `http://my-proxy.vpc.com:8000`

>Assumptions:
>1. Choose any language of your choice (Python/NodeJS)
>2. Response from the 3rd party can be of any format - feel free to define one

### Problem Statement 2/2

You need to write code for the function and the required infra code to deploy it. Consider writing test cases as well for the function code to test cover it.

>Assumptions:
>1. Lambda must run in the account’s VPC to avail the Proxy service
>2. Declare if you wish to access Secrets Manager service via VPC Endpoint - Choice is all yours
>3. Secret in the Secrets Manager is encrypted via a CMK
