---
title: photos_updateProfilePhoto
description: photos_updateProfilePhoto parameters, return type and example
---
## Method: photos\_updateProfilePhoto  
[Back to methods index](index.md)


### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|id|[InputPhoto](../types/InputPhoto.md) | Required|
|crop|[InputPhotoCrop](../types/InputPhotoCrop.md) | Required|


### Return type: [UserProfilePhoto](../types/UserProfilePhoto.md)

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

$UserProfilePhoto = $MadelineProto->photos->updateProfilePhoto(['id' => InputPhoto, 'crop' => InputPhotoCrop, ]);
```