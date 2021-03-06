---
title: auth.requestPasswordRecovery
description: auth.requestPasswordRecovery parameters, return type and example
---
## Method: auth.requestPasswordRecovery  
[Back to methods index](index.md)




### Return type: [auth\_PasswordRecovery](../types/auth_PasswordRecovery.md)

### Can bots use this method: **NO**


### Errors this method can return:

| Error    | Description   |
|----------|---------------|
|PASSWORD_EMPTY|The provided password is empty|


### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
$MadelineProto->session = 'mySession.madeline';
if (isset($number)) { // Login as a user
    $MadelineProto->phone_login($number);
    $code = readline('Enter the code you received: '); // Or do this in two separate steps in an HTTP API
    $MadelineProto->complete_phone_login($code);
}

$auth_PasswordRecovery = $MadelineProto->auth->requestPasswordRecovery();
```

Or, if you're using the [PWRTelegram HTTP API](https://pwrtelegram.xyz):



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/auth.requestPasswordRecovery`

Parameters:




Or, if you're into Lua:

```
auth_PasswordRecovery = auth.requestPasswordRecovery({})
```

