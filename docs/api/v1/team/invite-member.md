# Invite a new member to the team


POST https://trustme-ed.com/api/v1/team/members

Example request:
```json
const url = new URL(
    "https://trustme-ed.com/api/v1/team/members"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "name": "Firstname Lastname",
    "email": "email@address.com"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

Example Response:
```json
{
    "success": {
        "message": "Invitation created",
        "status_code": 200
    },
    "data": {
        "team": {
            "id": 421,
            "name": "Schouder Netwerk Nederland",
            "owner_name": "Erik Kieft",
            "owner_email": "Erikkieft@praktijkdeen.nl"
        },
        "invite": {
            "id": "241e6507-fc19-4604-8673-091c88f3e090",
            "name": "Firstname Lastname",
            "email": "email@address.com",
            "role": "user",
            "token": "HanIZqwxp3Y1jwXOwktJ3TL4mNjAFBFTsaEd5QYq",
            "signup_url": "https://trustme-ed.com/start/team/241e6507-fc19-4604-8673-091c88f3e090",
            "created_at": "2025-05-14T18:01:58.000000Z"
        },
        "request_data": {
            "name": "Firstname Lastname",
            "email": "email@address.com"
        }
    }
}
```

Example Errors:
```json
"error": {
    "message": "User already invited",
    "status_code": 200
},

"error": {
    "message": "User already belongs to this team",
    "status_code": 200
},

"error": {
    "message": "User belongs to another team",
    "status_code": 200
},
```
