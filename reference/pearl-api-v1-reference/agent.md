# Agent

## Create Agent

<mark style="color:blue;">`POST`</mark> `/iagent/api/v1/agents_def`

**Headers**

| Name          | Value                |
| ------------- | -------------------- |
| Content-Type  | `application/json`   |
| Authorization | `Bearer <APP_TOKEN>` |

**Body**

| Field           | Type                                                    | Optional | Desc         |
| --------------- | ------------------------------------------------------- | -------- | ------------ |
| did             | String                                                  | no       | User did     |
| name            | String                                                  | no       | Agent's name |
| gender          | String                                                  | no       | Famale/Male  |
| age             | Integer                                                 | no       | <p><br></p>  |
| hobbies         | String                                                  | no       | <p><br></p>  |
| experience      | String                                                  | no       | <p><br></p>  |
| perl\_questions | list\[[QuetionContent](data-models.md#questioncontent)] | no       | <p><br></p>  |

**Response**

| Field   | Type                                                  | Desc        |
| ------- | ----------------------------------------------------- | ----------- |
| code    | String                                                | <p><br></p> |
| message | String                                                | <p><br></p> |
| data    | [AgentCreationResp](data-models.md#agentcreationresp) | <p><br></p> |

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

| Field   | Type                                         | Desc        |
| ------- | -------------------------------------------- | ----------- |
| code    | String                                       | <p><br></p> |
| message | String                                       | <p><br></p> |
| data    | [UpdateResp](data-models.md#agentupdateresp) | <p><br></p> |

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

| Field   | Type                                              | Desc        |
| ------- | ------------------------------------------------- | ----------- |
| code    | String                                            | <p><br></p> |
| message | String                                            | <p><br></p> |
| data    | [AgentUpdateResp](data-models.md#agentupdateresp) | <p><br></p> |

