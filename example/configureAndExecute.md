# Positive-Field-Validation
Sample to create a policy focused on positive validation of attributes dynamically populated on policy call.

## Prerequisites

To follow this example you will need the following:

- A client public/private key pair with a single depth level.
- The issuer public certificate.
- A directory to lookup customer attributes.
- The policy export file that is part of this repository.
- Basic working knowledge of the Axway API Gateway software and Policy Studio.

A sample single depth client-issuer relationship can be seen here:
![alt text](https://github.com/Axway-API-Management-Plus/PKI_Client_Mutual_Auth/blob/master/example/src/certificateChain.png "Certificate and Issuer")

## Step By Step

1. Navigate to 'File --> Import --> Import Customization Fragment'. Select the policy fragment supplied in this repository. Resolve any dependency issues and complete import.

![alt text](https://github.com/Axway-API-Management-Plus/PKI_Client_Mutual_Auth/blob/master/example/src/importFrag.png "Import Policy Fragment")

2. Modify the policy to meet your environmental configuration and give it a relative path. Deploy the changes to your API Gateway.

3. Execute a request against the configured endpoint. Aside from using a certificate that meets the noted environmental configuration, you will need to supply URL params that meet the configuration in the policy.

4. Log into your API Gateway Management web console (eg https://hostmane:8090), and access the Traffic Monitor. Check the successful message to see the params and headers captured by your REST Attributes filter and the vetting done by the Compare Attributes filter as shown below. You may need to increase debugging to see full details. If you are having any issues with the validation, look through this log and note each validation and attribute value is individually tracked and capture for ease of debugging.

## API Management Version Compatibility
This artefact was successfully tested for the following versions:
- V7.5.3

## Contributing

Please read [Contributing.md](https://github.com/Axway-API-Management/Common/blob/master/Contributing.md) for details on our code of conduct, and the process for submitting pull requests to us.


## Team

![alt text][Axwaylogo] Axway Team

[Axwaylogo]: https://github.com/Axway-API-Management/Common/blob/master/img/AxwayLogoSmall.png  "Axway logo"

Contact - Daniel Wille: dwille@axway.com


## License
[Apache License 2.0](/LICENSE)
