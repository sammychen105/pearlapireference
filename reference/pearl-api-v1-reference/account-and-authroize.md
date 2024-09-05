# Account and Authroize

## Create DID

<mark style="color:green;">`POST`</mark> `/auth/api/v1/did/create`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

[#did-document](data-models.md#did-document "mention")

**Request Body Example**

<pre class="language-json"><code class="lang-json">{
  "@context": "https://w3id.org/did/v1", // fixed value
<strong>  "id": "did:protocols:&#x3C;method-specific-id>"
</strong>  "version": 1,
  "createdAt": "2024-08-13T12:00:00Z",
  "updatedAt": "2024-08-13T12:00:00Z"
  "verificationMethod": [
    {
      "id": "#keys-1",
      "type": "Secp256k1",
      "publicKeyHex": "xxxx"},
    {
      "id": "#keys-2",
      "type": "Secp256k1",
      "publicKeyHex": "xxx"}
  ],
  "authentication": ["#key-1"],
  "recovery": ["#key-2"]
  "proof": {
            "type": "Secp256k1",
            "creator": "did:xxx:xxx#key-1",
            "signatureValue": "xxx"
  }
}
</code></pre>

**Response**

<table><thead><tr><th width="193">Field</th><th>Type</th><th>Desc</th></tr></thead><tbody><tr><td>code</td><td>String</td><td><br></td></tr><tr><td>msg</td><td>String</td><td><br></td></tr><tr><td>data</td><td>String</td><td><br></td></tr></tbody></table>

## Update DID

<mark style="color:blue;">`PUT`</mark> `/auth/api/v1/did/update`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field     | Type                                            | Optional | Desc        |
| --------- | ----------------------------------------------- | -------- | ----------- |
| did       | [DID Definition](data-models.md#did-definition) | no       | User did    |
| document  | [DID Document](data-models.md#did-document)     | no       | <p><br></p> |
| timestamp | Millisecond timestamp                           | no       | <p><br></p> |

**Response**

| Field | Type                                        | Desc        |
| ----- | ------------------------------------------- | ----------- |
| code  | String                                      | <p><br></p> |
| msg   | String                                      | <p><br></p> |
| data  | [DID Document](data-models.md#did-document) | <p><br></p> |

## Deactivation DID

`DELETE` `/auth/api/v1/did/deactivate`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field     | Type   | Optional | Desc                                   |
| --------- | ------ | -------- | -------------------------------------- |
| did       | String | no       | User did                               |
| timestamp | String | no       | time in second                         |
| signature | String | no       | <p>signature using private key<br></p> |

**Response**

| Field | Type   | Desc        |
| ----- | ------ | ----------- |
| code  | String | <p><br></p> |
| msg   | String | <p><br></p> |
| data  | String | <p><br></p> |

## DID Resolution

<mark style="color:blue;">`GET`</mark> `/auth/api/v1/did/resolve/{did}`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Path Variable**

| Field | Type   | Optional | Desc |
| ----- | ------ | -------- | ---- |
| `did` | String | no       | did  |

**Response**

| Field | Type                                        | Desc        |
| ----- | ------------------------------------------- | ----------- |
| code  | String                                      | <p><br></p> |
| msg   | String                                      | <p><br></p> |
| data  | [DID Document](data-models.md#did-document) | <p><br></p> |

## DID Auth

<mark style="color:blue;">`POST`</mark> `/auth/api/v1/did/auth`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field     | Type   | Optional | Desc                                   |
| --------- | ------ | -------- | -------------------------------------- |
| did       | String | no       | User did                               |
| timestamp | String | no       | time in second                         |
| signature | String | no       | <p>signature using private key<br></p> |

**Response**

| Field | Type                                        | Desc        |
| ----- | ------------------------------------------- | ----------- |
| code  | String                                      | <p><br></p> |
| msg   | String                                      | <p><br></p> |
| data  | [DID Auth Resp](data-models.md#didauthresp) | <p><br></p> |





















