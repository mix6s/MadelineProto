---
title: dh_gen_retry
description: dh_gen_retry attributes, type and example
---
## Constructor: dh\_gen\_retry  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|nonce|[int128](../types/int128.md) | Required|
|server\_nonce|[int128](../types/int128.md) | Required|
|new\_nonce\_hash2|[int128](../types/int128.md) | Required|



### Type: [Set\_client\_DH\_params\_answer](../types/Set_client_DH_params_answer.md)


### Example:

```
$dh_gen_retry = ['_' => 'dh_gen_retry', 'nonce' => int128, 'server_nonce' => int128, 'new_nonce_hash2' => int128, ];
```  

