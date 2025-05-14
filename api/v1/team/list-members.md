# Get a list of all your members

GET https://trustme-ed.com/api/v1/team/members

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

fetch(url, {
    method: "GET",
    headers: headers
})
    .then(response => response.json())
    .then(json => console.log(json));
```

Example Response:
```json
{
    "success": {
        "message": "Here are the members of your team",
        "status_code": 200
    },
    "data": {
        "total": 42,
        "members": [
            {
                "uuid": "74cec428-a7e9-4ee2-975f-758601fa3c7b",
                "name": "User Name",
                "email": "email@address.com",
                "phone": "",
                "role": "owner",
                "status": "active",
                "member_created_at": "2023-07-27 10:32:43"
            },
            ...
        ]
    }
}
```