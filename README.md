# Mobile ID Web Service Documentation

Swisscom Mobile ID is a cost-efficient, managed authentication service from Swisscom. 
The customer-facing API is based on open standard ETSI 102 2041.

## Mobile ID Reference Guide
The Mobile ID Reference Guide provides technical documentation and guidelines to use the Swisscom Mobile ID Authentication Web Service. 

* [mobile-id-reference-guide-v-3-2.pdf](mobile-id-reference-guide-v-3-2.pdf) - Latest Version 3.2

## Web Service Description
Description documents for the Mobile ID SOAP and RESTful web service.

* [mobileid.yaml](mobileid.yaml) - Mobile ID RESTful Web Service OpenAPI Specification
* [mobileid.wsdl](mobileid.wsdl) - Mobile ID SOAP Web Service Description

## Mobile ID Root CA Certificate

There are two different scenarios, where x.509 certificates are involved. 
Since they do not have the same root CA, you must ensure that your TrustStore contains all root CA certificates.

### Mobile ID X509 Server Certificate 
To validate the chain of trust of the Mobile ID server certificate, it will be enough to add the SwissSign root certificate to the client TrustStore. 
The intermediate CAs are returned by the MID server and may change!

You can download the "SwissSign Gold CA - G2" certificate also from the SwissSign site: 
https://www.swisssign.com/en/support/faq.html

* [SwissSign_Gold_CA_-_G2.crt](SwissSign_Gold_CA_-_G2.crt) - "SwissSign Gold CA - G2" Root Certificate

### Mobile ID User X509 Certificate
The Mobile ID authentication response contains a digital signature and the end-user's x.509 certificate. 
The customer (client) should validate the signature as well as the x.509 certificate's trust chain.

You can download the "Swisscom Root CA 2" certificate also from the Swisscom Digital Certificate Service site:
http://www.swissdigicert.ch

* [Swisscom_Root_CA_2.crt](Swisscom_Root_CA_2.crt) - Swisscom Root CA 2 (current)
* [Swisscom_Root_CA_4.crt](Swisscom_Root_CA_4.crt) - Swisscom Root CA 4 (RFU)


