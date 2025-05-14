# Remove a team member


POST https://trustme-ed.com/api/v1/team/members/remove

Example request:
```json
const url = new URL(
    "https://trustme-ed.com/api/v1/team/members/remove"
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

Example Response:
```json
{
    "success": {
        "message": "User removed from team",
        "status_code": 200
    }
}
```

Example Errors:
```json
"error": {
    "message": "Team or user not found",
    "status_code": 404
}
```
