# Chat

## Chat

> **The backend needs to establish a connection pool with the gateway instead of having one connection per user.**

<mark style="color:blue;">`WebSocket`</mark>`/ws/v1/chat?app_token=APP_TOKEN (APP_TOKEN Don’t need Bearer prefix)`

**Body**

| Field         | Type   | Optional | Desc                                                                          |
| ------------- | ------ | -------- | ----------------------------------------------------------------------------- |
| chat\_type    | number | no       | Private Chat: 1 , Group Chat: 2                                               |
| msg\_id       | string | no       | unique identifier of a message.                                               |
| ref\_msg\_id  | string | yes      | <p><br></p>                                                                   |
| timestamp     | number | no       | The timestamp of the message sending, accurate to milliseconds.               |
| group\_id     | string | yes      | unique identifier of a group.                                                 |
| sender\_type  | number | no       | BY\_USER: 1 , BY\_AGENT: 2                                                    |
| sender\_id    | string | no       | Who sent this message. The id is the user id                                  |
| receiver\_id  | string | yes      | Who will receive this message. The id is user id                              |
| content\_type | number | no       | Text: 1, Image: 2, Voice: 3                                                   |
| content       | string | no       | If ContentType is image or voice, the content format need be{"file\_id":xxxx} |
