# Mobile ID API

For integration guides and technical documentation, please visit the official Mobile ID documentation:

**[docs.mobileid.ch](https://docs.mobileid.ch/)**

- [REST API Guide](https://docs.mobileid.ch/rest-api-guide/)
- [OIDC Integration Guide](https://docs.mobileid.ch/oidc-integration-guide/)
- [RADIUS Gateway Guide](https://docs.mobileid.ch/radius-interface-gateway-guide/)


## Mobile ID Root CA Certificate

There are two different scenarios, where x.509 certificates are involved.
Since they do not have the same root CA, you must ensure that your TrustStore contains all root CA certificates.

### Mobile ID Server Certificate
To validate the chain of trust of the Mobile ID server certificate, it will be enough to add the SwissSign root certificate to the client TrustStore.
The intermediate CAs are returned by the MID server and may change!

You can download the certificate also from https://www.swisssign.com

* [SwissSign_Gold_CA_-_G2.crt](root-certs/SwissSign_Gold_CA_-_G2.crt) - "SwissSign Gold CA - G2" Root Certificate

### Mobile ID End-User Certificate
The Mobile ID authentication response contains a digital signature and the end-user's x.509 certificate.
The customer (client) should validate the signature as well as the x.509 certificate's trust chain.

You can download the certificate also from http://www.swissdigicert.ch

* [Swisscom_Root_CA_2.crt](root-certs/Swisscom_Root_CA_2.crt) - Swisscom Root CA 2 (current)
* [Swisscom_Root_CA_4.crt](root-certs/Swisscom_Root_CA_4.crt) - Swisscom Root CA 4 (RFU)



