# MobileID API Postman Collection

This folder contains a Postman collection and sample environment variables for interacting with the MobileID REST API. 
Follow the instructions below to import the collection and environment into Postman, configure necessary settings, and understand the provided scripts.

## Files

- `MobileID-RestAPI.postman_collection.json`: Postman collection for MobileID API.
- `Env-Sample.postman_environment.json`: Sample environment variables for the MobileID API.

## Getting Started

### Importing into Postman

1. **Import Collection:**
   - Open Postman.
   - Click on `Import` in the top-left corner.
   - Select `Upload Files`.
   - Choose `MobileID-RestAPI.postman_collection.json`.
   - Click `Import`.

2. **Import Environment:**
   - Open Postman.
   - Click on `Environment` in the top-right corner.
   - Click on `Import`.
   - Select `Upload Files`.
   - Choose `Env-Sample.postman_environment.json`.
   - Click `Import`.

### Pre-Requisites

Before sending requests to the API, ensure the following configurations are made:

1. **Add Client Certificate:**
   - Go to Postman Settings (`File > Settings` or `Ctrl+,`).
   - Navigate to the `Certificates` tab.
   - Click on `Add Certificate`.
   - For the `Host`, enter `mobileid.swisscom.com`.
   - Set the `Port` to `443`.
   - Upload your MobileID account related `CRT` and `KEY` files.
   - Click `Add`.

2. **Network Configuration:**
   - Ensure your `sourceIP` is whitelisted on the Firewall.
   - Verify connectivity to `mobileid.swisscom.com:443`.
   - Configure the proxy settings if required.

### Scripts

The collection contains scripts located in the `rest` folder:

- **Pre-request Scripts:** Scripts executed before sending the request.
- **Test Scripts:** Scripts executed after receiving the response.

Inspect these scripts to understand their functionality and how they can be utilized or modified for your needs.

### Example Environment Variables

The provided environment file includes the following variables:

- `baseUrl`: Base URL for the MobileID API (eg. `https://mobileid.swisscom.com`).
- `AP_ID`: Your MobileID Account / Application Provider ID (eg. `mid://ap.mycompany.com`).
- `MSISDN`: Mobile user phone number (eg. `41700092501` is a test number you may use for testing purpose).
- `DataToBeSigned`: Is the same as "DataToBeDisplayed (DTBD)" (`MyCompany: Sign in from Postman?`).
- `SignatureProfile`: URL for the signature profile (eg. `http://mid.swisscom.ch/Any-LoA4`).
- `UserLang`: User language (one of `en`,`de`,`fr`,`it`).
- `Message`: Custom message (`An example receipt message from PostMan`).
- `MSSP_TransID`: MSSP Transaction ID.

Ensure to replace placeholder values (e.g., `<your-APID>`) with actual values specific to your use case.

## Usage

Once you have configured your environment and imported the collection, you can start sending requests to the MobileID API. 
Select the appropriate environment from the `Environment` dropdown in the top-right corner of Postman and explore the collection to execute API requests.

## Support

For further assistance, refer to the MobileID Reference Guide or contact support.

---

**Note:** Proper security measures should be taken to protect your API keys and sensitive data.
