# Check status for a team member


POST https://trustme-ed.com/api/v1/team/members/check

Example request:
```json
const url = new URL(
    "https://trustme-ed.com/api/v1/team/members/check"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
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

Example Responses:
```json
{
    "success": {
        "message": "We found your member",
        "status_code": 200
    },
    "data": {
        "uuid": "74cec428-a7e9-4ee2-975f-758601fa3c7b",
        "name": "User Name",
        "email": "email@address.com",
        "phone": "",
        "role": "owner",
        "status": "active",
        "member_created_at": "2023-07-27 10:32:43"
    }
}

or

{
    "success": {
        "message": "We found your invitation",
        "status_code": 200
    },
    "data": {
        "status": "pending",
        "id": "f04396be-7cf2-43ec-b806-b1f0581cf7f9",
        "name": "User Name",
        "email": "email@address.com",
        "role": "user",
        "token": "Hok0qcZffEucmhgTvTSCSvDlkrg5UbCIQrVZVg0C",
        "signup_url": "https://trustme-ed.com/start/team/f04396be-7cf2-43ec-b806-b1f0581cf7f9"
    }
}
```

Example Errors:
```json
"error": {
    "message": "Member not found",
    "status_code": 404
}
```
