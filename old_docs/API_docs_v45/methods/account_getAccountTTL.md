---
title: account_getAccountTTL
description: account_getAccountTTL parameters, return type and example
---
## Method: account\_getAccountTTL  
[Back to methods index](index.md)




### Return type: [AccountDaysTTL](../types/AccountDaysTTL.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) {
    $this->bot_login($token);
}
if (isset($number)) {
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$AccountDaysTTL = $MadelineProto->account->getAccountTTL();
```