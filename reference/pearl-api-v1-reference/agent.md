# Agent

## Create Agent

<mark style="color:blue;">`POST`</mark> `/iagent/api/v1/agents_def`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field           | Type                                                                                                                | Optional | Desc         |
| --------------- | ------------------------------------------------------------------------------------------------------------------- | -------- | ------------ |
| did             | String                                                                                                              | no       | User did     |
| name            | String                                                                                                              | no       | Agent's name |
| gender          | String                                                                                                              | no       | Famale/Male  |
| age             | Integer                                                                                                             | no       | <p><br></p>  |
| hobbies         | String                                                                                                              | no       | <p><br></p>  |
| experience      | String                                                                                                              | no       | <p><br></p>  |
| perl\_questions | list\[[QuetionContent](https://z0hqbo7agth.feishu.cn/wiki/I246wMeT6irdhkk5ES4cPwqZn9c#K1ucd8gaioWx80xp86Ac2KOhnsc)] | no       | <p><br></p>  |

**Response**

| Field   | Type                                                                                                            | Desc        |
| ------- | --------------------------------------------------------------------------------------------------------------- | ----------- |
| code    | String                                                                                                          | <p><br></p> |
| message | String                                                                                                          | <p><br></p> |
| data    | [AgentCreationResp](https://z0hqbo7agth.feishu.cn/wiki/I246wMeT6irdhkk5ES4cPwqZn9c#QnHVdj8cYo8XoXxdwEJcqEFMnfd) | <p><br></p> |

## Update Agent

<mark style="color:blue;">`PATCH`</mark> `/iagent/api/v1/agents_def/update`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field      | Type    | Optional | Desc         |
| ---------- | ------- | -------- | ------------ |
| did        | String  | no       | User did     |
| name       | String  | no       | Agent's name |
| gender     | String  | no       | Famale/Male  |
| age        | Integer | no       | <p><br></p>  |
| hobbies    | String  | no       | <p><br></p>  |
| experience | String  | no       | <p><br></p>  |

**Response**

| Field   | Type                                                                                                          | Desc        |
| ------- | ------------------------------------------------------------------------------------------------------------- | ----------- |
| code    | String                                                                                                        | <p><br></p> |
| message | String                                                                                                        | <p><br></p> |
| data    | [Agent](https://z0hqbo7agth.feishu.cn/wiki/I246wMeT6irdhkk5ES4cPwqZn9c#QnHVdj8cYo8XoXxdwEJcqEFMnfd)UpdateResp | <p><br></p> |

## Get Agent

<mark style="color:blue;">`GET`</mark> `/iagent/api/v1/agents_def/{agent_id}`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Path Variable**

| Field     | Type   | Optional | Desc |
| --------- | ------ | -------- | ---- |
| agent\_id | String | no       | did  |

**Response**

| Field   | Type   | Desc        |
| ------- | ------ | ----------- |
| code    | String | <p><br></p> |
| message | String | <p><br></p> |
| data    |        | <p><br></p> |

