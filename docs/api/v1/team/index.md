# Team API

Manage your team via our API

## 1. Get your API token
[Click here to get your token](https://trustme-ed.com/account/api)

Your user must have access to the API. Contact dev@trustme-ed.com if you have any trouble.

## 2. Passing The Access Token
When calling routes that are protected by access tokens, your application's API consumers should specify their access token as a Bearer token in the Authorization header of their request. For example, when using the Guzzle HTTP library:

```json
$response = $client->request('GET', '/api/v1/...', [
    'headers' => [
        'Accept' => 'application/json',
        'Authorization' => 'Bearer '.$accessToken,
    ],
]);
```

## 3. The Endpoints
Base route: /api/v1/team

01. [List members](list-members.md)

02. [Invite a new member](invite-member.md)

03. [Remove member](remove-member.md)

04. [Check member](check-member.md)