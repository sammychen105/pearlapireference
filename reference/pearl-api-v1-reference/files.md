# Files

## Generate Upload Url

<mark style="color:blue;">`POST`</mark> `/files/api/v1/files/gen_upload_presign_url`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field      | Type   | Optional | Desc                                       |
| ---------- | ------ | -------- | ------------------------------------------ |
| did        | String | no       |                                            |
| file\_type | String | no       | Current support: audio / image             |
| scope      | String | yes      | private / public-read . default is private |

**Response**

| Field   | Type           | Desc        |
| ------- | -------------- | ----------- |
| code    | String         | <p><br></p> |
| message | String         | <p><br></p> |
| data    | UploadFileResp |             |

## Generate Download Url

<mark style="color:blue;">`POST`</mark> `/files/api/v1/files/gen_upload_presign_url`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field      | Type   | Optional | Desc                                       |
| ---------- | ------ | -------- | ------------------------------------------ |
| did        | String | no       |                                            |
| file\_type | String | no       | Current support: audio / image             |
| scope      | String | yes      | private / public-read . default is private |

**Response**

| Field   | Type           | Desc        |
| ------- | -------------- | ----------- |
| code    | String         | <p><br></p> |
| message | String         | <p><br></p> |
| data    | UploadFileResp |             |
