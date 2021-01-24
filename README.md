<h1 align="center"> Rentomojo Contact API </center>

---

NOTE: Mongolab addon has been discontinued on heroku so I was unable to host my work there.

---

### Index

- Update Record

When done via Postman, the API takes the request in the given form followed by ID and updates the record -

```
{"name":"Abhinav","email":"abhinav.agrahari2@gmail.com","phone":null,"_v":0}
```

---

- Delete Record

In order to delete the data of specific user, we'll need `key` to do so - `<url>/remove/?id=id`

`http://localhost:3000/remove/?id=600d167d4484853518d03c18`

```json
[
    {
        "_id": "600d167d4484853518d03c18",
        "name": "User",
        "email": "user@gmail.com",
        "phone": null,
        "__v": 0
    }
]
```
---

- __Search__

The API gives users flexibility to search the database by passing the parameters `name` and `email` separately or together.

*For example*

- By Name - `http://localhost:3000/contactsapi/username`

- By Email - `http://localhost:3000/contactsapi/email`


---

- __Expose All Data__

You can expose all the data by making request to `<url>/contactsapi`

`http://localhost:3000/contactsapi`


```json
[
    {
        "_id": "600c5a83336b5c33e4cfaf06",
        "name": "User Zero",
        "email": "abc.dyz@gmail.com",
        "phone": 7632345876,
        "__v": 0
    },
    {
        "_id": "600c5a9e336b5c33e4cfaf07",
        "name": "User One",
        "email": "abc.mno@gmail.com",
        "phone": null,
        "__v": 0
    },
    {
        "_id": "600cd92035459d0d5095193b",
        "name": "User Two",
        "email": "abc.man@gmail.com",
        "phone": 8623456789,
        "__v": 0
    }
]
```
