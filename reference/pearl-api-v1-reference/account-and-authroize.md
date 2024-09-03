# Account and Authroize

## Create Pearl ID

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

{% tabs %}
{% tab title="200" %}
```json
{
  "code": 200,
  "data": "success"
}
```
{% endtab %}

{% tab title="400" %}
```json
{
  "error": "Invalid request"
}
```
{% endtab %}
{% endtabs %}

