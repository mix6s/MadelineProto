---
title: geochats_search
description: geochats_search parameters, return type and example
---
## Method: geochats\_search  
[Back to methods index](index.md)


### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|peer|[InputGeoChat](../types/InputGeoChat.md) | Required|
|q|[string](../types/string.md) | Required|
|filter|[MessagesFilter](../types/MessagesFilter.md) | Required|
|min\_date|[int](../types/int.md) | Required|
|max\_date|[int](../types/int.md) | Required|
|offset|[int](../types/int.md) | Required|
|max\_id|[int](../types/int.md) | Required|
|limit|[int](../types/int.md) | Required|


### Return type: [geochats\_Messages](../types/geochats_Messages.md)

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

$geochats_Messages = $MadelineProto->geochats->search(['peer' => InputGeoChat, 'q' => string, 'filter' => MessagesFilter, 'min_date' => int, 'max_date' => int, 'offset' => int, 'max_id' => int, 'limit' => int, ]);
```