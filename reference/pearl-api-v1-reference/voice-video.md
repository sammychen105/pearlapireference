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

<table><thead><tr><th width="193">Field</th><th>Type</th><th>Desc</th></tr></thead><tbody><tr><td>code</td><td>String</td><td><br></td></tr><tr><td>message</td><td>String</td><td><br></td></tr><tr><td>data</td><td><a href="data-models.md#voicetranscriberesp">VoiceTranscribeResp</a></td><td><br></td></tr></tbody></table>

