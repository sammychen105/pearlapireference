# Data Models

### DID definition

The DID Format

<pre class="language-SQL"><code class="lang-SQL"><strong>did:&#x3C;method>:&#x3C;method-specific-id>
</strong></code></pre>

#### DID Fragment syntax

```JSON
did-url = did#fragment
```

* Example

```JSON
did:example:123#public-key-0
```

### DID Document

| name                          | required      | Value constraints                                                                                                                                                                                                                                   |
| ----------------------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id                            | YES           | A string that conforms to the rules in [DID definition](https://z0hqbo7agth.feishu.cn/wiki/KYKqww8ALiuc2skZJCfcaOfmnpd#IZFpdc1y8ovNUxxLVkIckNAJnXf)                                                                                                 |
| version                       | YES           | Interger value                                                                                                                                                                                                                                      |
| created                       | <p>NO<br></p> | Datetime with format `yyyy-MM-DDTHH:mm:ss.SSST`,example: `2024-10-21T11:12:13.065Z`                                                                                                                                                                 |
| updated                       | NO            | Datetime with format `yyyy-MM-DDTHH:mm:ss.SSST`,example: `2024-10-21T11:12:13.065Z`                                                                                                                                                                 |
| <p>verificationMethod<br></p> | <p>No<br></p> | A set of Verification Method maps that conform to the rules in [VerificationMethod](https://z0hqbo7agth.feishu.cn/wiki/KYKqww8ALiuc2skZJCfcaOfmnpd#CujFdDZCXop6VQxGWSsc3Q3jnge) properties.PublicKey's ID must conform to the rule:`id#key-{index}` |
| authentication                | YES           | A set of [VerificationMethod](https://z0hqbo7agth.feishu.cn/wiki/KYKqww8ALiuc2skZJCfcaOfmnpd#CujFdDZCXop6VQxGWSsc3Q3jnge) id                                                                                                                        |
| recovery                      | NO            | A set of [VerificationMethod](https://z0hqbo7agth.feishu.cn/wiki/KYKqww8ALiuc2skZJCfcaOfmnpd#CujFdDZCXop6VQxGWSsc3Q3jnge) id                                                                                                                        |
| proof                         | NO            | An object of [Proof](https://z0hqbo7agth.feishu.cn/wiki/KYKqww8ALiuc2skZJCfcaOfmnpd#K8p1dBaMSogaJ1xmpfLcvWlWn6b)                                                                                                                                    |

### Proof

| name                       | required | Value constraints                                                                                                                                        | <p><br></p> |
| -------------------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| id                         | YES      | A string that conforms to the rules in [DID Fragment syntax](https://z0hqbo7agth.feishu.cn/wiki/KYKqww8ALiuc2skZJCfcaOfmnpd#BPYddp01hoUi4HxdRn2cfmdknwf) | <p><br></p> |
| <p>type<br></p>            | YES      | <p>public key cryptography type<br></p>                                                                                                                  | <p><br></p> |
| <p>signature_value<br></p> | YES      | Signature value                                                                                                                                          | <p><br></p> |

### VerificationMethod

| name                    | required | Value constraints                                                                                                                                            | <p><br></p> |
| ----------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------- |
| id                      | YES      | A string that conforms to the rules in [DID Fragment definition](https://z0hqbo7agth.feishu.cn/wiki/KYKqww8ALiuc2skZJCfcaOfmnpd#BPYddp01hoUi4HxdRn2cfmdknwf) | <p><br></p> |
| <p>type<br></p>         | YES      | public key cryptography type                                                                                                                                 | <p><br></p> |
| <p>publicKeyHex<br></p> | YES      | Public key hex value                                                                                                                                         | <p><br></p> |

```JSON
{
  "@context": "https://w3id.org/did/v1",
  "verificationMethod": [
    {
      "id": "#keys-1",
      "type": "Secp256k1",
      "publicKeyHex": "02b97c30de767f084ce3080168ee293053ba33b235d7116a3263d29f1450936b71"},
    {
      "id": "#keys-2",
      "type": "Secp256k1",
      "publicKeyHex": "4b4042665b3235a12fb49730ff620fef1c96e9efa5c90119abd2e8acfe856053"}
  ],
  "authentication": ["#key-1"],
  "recovery": ["#key-2"]
}
```

### QuestionContent

| Field    | Type   | Desc        |
| -------- | ------ | ----------- |
| question | String | <p><br></p> |
| answer   | String | <p><br></p> |

### AgentCreationResp

| Field     | Type   | Desc        |
| --------- | ------ | ----------- |
| agent\_id | String | <p><br></p> |

### AgentUpdateResp

| Field     | Type   | Desc        |
| --------- | ------ | ----------- |
| agent\_id | String | <p><br></p> |

### UploadFileResp

| Field         | Type   | Desc                                                                                                                                        |
| ------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| file\_id      | String | <p><br></p>                                                                                                                                 |
| upload\_url   | String | The upload\_url will expire in 10 minutes.                                                                                                  |
| download\_url | String | If the scope is private, the download link will expire in 10 minutes; if the scope is public-read, the download link will be valid forever. |

### VoiceTranscribeResp

| Field    | Type   | Desc        |
| -------- | ------ | ----------- |
| text     | String | <p><br></p> |
| language | String | <p><br></p> |

###
