# Avatar

## Generate Avatar

<mark style="color:blue;">`POST`</mark> `/imgs/api/v1/imgs/gen-avatar`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field    | Type   | Optional | Desc             |
| -------- | ------ | -------- | ---------------- |
| img\_url | String | no       | User's photo url |
| did      | String | no       |                  |

**Response**

| Field | Type   | Desc                  |
| ----- | ------ | --------------------- |
| code  | String | <p><br></p>           |
| msg   | String | <p><br></p>           |
| data  | String | <p>avatar url<br></p> |

