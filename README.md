# Todo List API
## API Documentation

---
`POST` newproject/todo/new

Created new task on todo list
```
Example request body:
{
    "id": 0,
    "text": "string",
    "isDone: false 
}
```
Response 201:
field | type | description |
----    | ---      | ---
`id`| "int"| new item ID  
`text`| "string"| new task description
`isDone`| "boolean"| status

---

`GET`
newproject.com/todo/all

returns all tasks from todo list

Response 200:
field | type | description |
----    | ---      | ---
`id`| "int"| new item ID  
`text`| "string"| new task description
`isDone`| "boolean" | status
```
Example request body:
[{
    "id": 0,
    "text": "string",
    "isDone": false
}]
 ```

---

 `PUT` newproject.com/todo/update/{id}

 updates data in given task from todo list
 ```
Example request body:
{
    "isDone": "true" 
    "text": "string"
}
 ```
 Response 200:
 field | type | description |
----    | ---      | ---
`id`| "int"| new item ID  
`text`| "string"| changed text
`isDone`| "boolean" | status

---

`DELETE`
newproject.com/todo/{id}

`{id}` - removes task with given ID
```
Example request body:
none
```
Response 204

---

`DELETE`
newproject.com/todo/all

`all` - removes all tasks
```
Example request body:
none
```
Response 204

---
Status codes summary:
Method | RESPONSE | ERROR HANDLING |
----    | ---      | ---
`GET`| 200 (OK) |  400 (BAD REQUEST)
`POST`| 201 (CREATED)| 409 (CONFLICT)
`PUT`| 200 (OK) | 400 (BAD REQUEST)
`DELETE` | 204 (NO CONTENT) |404 (NOT FOUND)
