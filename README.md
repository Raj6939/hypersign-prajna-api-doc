# hypersign-prajna-api-doc

## Create App on Entity API Dashboard

1. Navigate to ```https://entity.dashboard.hypersign.id/#/studio/login```

   ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/2598fe8b-9552-4474-914b-f55c3f402a22)

3. Login by Hypersign Web Wallet by clicking Click To Login Button

   ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/6178646e-8e75-45b0-ac46-d46998e668fc)

4. Click on the +Create button for creating an app, here is the example, Click on Save Button.

   ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/a3fecc9e-bc08-4202-a7ec-36e6fa062ef7)

   > If the app doesn't appear, try refreshing the page.

5. Copy the Application ID from the created App and click on the API red button, paste it to get the API Secret Key

   ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/d128d6f3-5919-4c67-83e8-9c80ad01af1a)
   

   ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/96eaa410-c94f-4ff4-98dd-1da3fba5ac3b)


   > Store the API Secret key safe, for further use

 6. Get Balance to your App

    Copy the wallet address from clicking Edit button on your app

    ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/f414c156-678f-4a64-b772-510740b8eeb2)

    You can claim the balance in one from any of the two ways,
       
       1. Join our Discord [server](https://discord.gg/xUCxWtu9dj), you will get entered in ```prajna-faucet-1``` channel

          Type this command to get balance, ```$request <your-wallet-address>```

       2. Join our hack:DiD Telegram [group](https://t.me/hackdid) and ping your wallet address in a chat


## Create Auth Token on Entity Developer Dashboard Service API

  1. Navigate to ```https://api.entity.dashboard.hypersign.id/```

     ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/b519793b-08a4-43c5-bb16-5c2fc419aa96)

  2. Click on ```/api/v1/app/oauth``` tab and click on Try it out button on the right and enter the API Secret key you copied from after app creation and Execute

     ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/2bea9ec0-2793-4d39-9fc8-b1212e7531da)

  3. Copy the Access Token Generated below in the response body

     ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/04a6d279-50f5-4522-903b-3aa2a6895b61)

     
## API PLayground
  
  1. Navigate to your APP at ```https://entity.dashboard.hypersign.id/#/studio/dashboard``` and click on the Edit button on your App, copy the Tenant Url part shown below

     ![Screenshot from 2024-01-18 10-54-14](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/d6c85201-db63-4231-a8bf-ee4413b26972)

 2. Navigate to ```https://<your-tenant-url-string>.api.entity.hypersign.id/ssi```

    ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/dfac0752-8508-414a-822a-5949ae83b9a9)

 3. Click on the Authorize button on the right side, enter the Access Token you generated previously, and authorize it.

    ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/33437937-e4bd-4d0d-84e7-f7456bce7a90)

## SSI Operations

  1. **Create DID**

  Click on ```/api/v1/did/create``` tab of POST and Try it out, follow the below Request Body

  ![Screenshot from 2024-01-18 11-22-19](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/ecc040b1-401f-48d6-aef9-67916ca3dd19)

  Here is the example for response you will get
  
  Response Body:

    {
      "did": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy",
      "registrationStatus": "UNREGISTRED",
      "metaData": {
        "didDocument": {
          "@context": [
            "https://www.w3.org/ns/did/v1",
            "https://w3id.org/security/suites/ed25519-2020/v1"
          ],
          "id": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy",
          "controller": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy"
          ],
          "alsoKnownAs": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy"
          ],
          "verificationMethod": [
            {
              "id": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1",
              "type": "Ed25519VerificationKey2020",
              "controller": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy",
              "publicKeyMultibase": "z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy"
            }
          ],
          "authentication": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "assertionMethod": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "keyAgreement": [],
          "capabilityInvocation": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "capabilityDelegation": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "service": []
        }
      }
    }

2. **Register DID Document**
   
   Copy the ```didDocument``` object only from DID Create API response
   
   Click on ```/api/v1/did/register``` tab, try it out. remove the selected part from the request body.

   ![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/793c34ea-c0b1-4bc5-9202-6880ad4a2a95)

   Paste the Copied didDocument in value of ```didDocument``` key by removing {} braces

   replace the ```verificationMethodId``` value by actual verificationMethodId from your ```didDocument```

   You can get the verificationMethodId from your didDocument ```verificationMethod``` arrays first ```id``` value like below,

![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/58ca74bf-5d21-4fe4-8d2f-de68be32d705)

   Your Request body will look like this, Click on Execute button and see response

![image](https://github.com/Raj6939/hypersign-prajna-api-doc/assets/67961128/9b594d2a-dc9a-4524-9a8f-2ecc018c2a8c)


Your DID Register Response will look like this
  
    {
      "did": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy",
      "registrationStatus": "COMPLETED",
      "transactionHash": "9C05A42F791452B2EBD867203B69E4EDEA54D7D487EE063983E9664D57B20AD7",
      "metaData": {
        "didDocument": {
          "@context": [
            "https://www.w3.org/ns/did/v1",
            "https://w3id.org/security/suites/ed25519-2020/v1"
          ],
          "id": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy",
          "controller": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy"
          ],
          "alsoKnownAs": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy"
          ],
          "verificationMethod": [
            {
              "id": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1",
              "type": "Ed25519VerificationKey2020",
              "controller": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy",
              "publicKeyMultibase": "z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy"
            }
          ],
          "authentication": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "assertionMethod": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "keyAgreement": [],
          "capabilityInvocation": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "capabilityDelegation": [
            "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
          ],
          "service": []
        }
      }
    }

Keep more than 2 DID registered for further SSI Operations. You can follow the same steps for Creating DID and then Registering it.

3. **Create Schema**

   Now click on ```/api/v1/schema``` tab of POST and try it out by following

   Replace the name value under schema object as ```PascalCase```, ```author``` value by registerd DID id and ```verificationMethodId``` as same we did in Registering DID Document

   For fields in the schema you have to choose ```camelCase``` variable names

   Here is an example of a request body

         {
           "schema": {
             "name": "RailwayTicketSchema",
             "author": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy",
             "description": "Railway ticket schema\"",
             "additionalProperties": false,
             "fields": [
               {
                 "name": "firstName",
                 "format": ",
                 "type": "string",
                 "required": false
               },
               {
                 "name": "lastName",
                 "format": ",
                 "type": "string",
                 "required": false
               }
             ]
           },
           "namespace": "testnet",
           "verificationMethodId": "did:hid:testnet:z6MkfUjJyJCCxTXU6N6om8B2WAubhCMECgVpBSwBbqbvVYEy#key-1"
         }

   


   

   


    


  

  


   


   
