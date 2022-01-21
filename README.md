# F5-AGC-API

![Templates](https://github.com/dfs5/F5-AGC-API/blob/main/Templates.png)

Currently this repo contains only one example of a deployment of the F5 BIG-IP APM Azure AD integration.
In order to apply this configuration you need:

- BIG-IP                16.1x or later
- Guided Configuration  8.0 or later

Rest API can be accessed via: https://{{bigip}}/mgmt/shared/iapp/gcapi/v1.0/guided-config-api

- In order to deploy send a POST request with "action" : "ADD" in the payload provided in 'Azure_AD_Integration.json"
- In order to delete send a POST request with "action" : "DELETE" in the payload provided in 'Azure_AD_Integration.json"
- In order to verify the progress send a GET Request to: https://{{bigip}}/mgmt/tm/access/gcapi-config-status

For authorization use Basic Auth. 

Before deployment modify in the json file all sections marked with <some-text> to satisfy your environmental requirements.

