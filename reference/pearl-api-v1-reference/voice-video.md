# Voice

## Transcribe

<mark style="color:blue;">`POST`</mark> `/voice/api/v1/listen-transcribe`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field      | Type   | Optional | Desc |
| ---------- | ------ | -------- | ---- |
| audio\_url | String | no       |      |

**Response**

| Field   | Type                                                                                                              | Desc        |
| ------- | ----------------------------------------------------------------------------------------------------------------- | ----------- |
| code    | String                                                                                                            | <p><br></p> |
| message | String                                                                                                            | <p><br></p> |
| data    | [VoiceTranscribeResp](https://z0hqbo7agth.feishu.cn/wiki/I246wMeT6irdhkk5ES4cPwqZn9c#OpaAdP7T3oPidsxhcGScpHeVnxb) | <p><br></p> |

