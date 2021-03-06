---
title: ncacn_nb_nb attribute
description: The ncacn\_nb\_nb keyword identifies NetBEUI over NetBIOS as the protocol family for the endpoint. This protocol family is obsolete and should not be used in new applications.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb attribute MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
---

# ncacn\_nb\_nb attribute

The **ncacn\_nb\_nb** keyword identifies NetBEUI over NetBIOS as the protocol family for the endpoint. This protocol family is obsolete and should not be used in new applications.

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## Parameters

<dl> <dt>

*port-name* 
</dt> <dd>

Specifies an optional 8-bit value ranging from 1 to 255. Values of less than 0x20 are reserved. If the *port-name* value is not specified, the endpoint-mapping service selects the port value.

</dd> </dl>

## Remarks

The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification. The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct. Some classes of errors may be reported at run time rather than at compile time.

> [!Note]  
> This protocol family is not supported in WindowsÂ XP.

 

## Examples

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## See also

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Interface Definition (IDL) File](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn\_ip\_tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn\_nb\_tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn\_np**](ncacn-np.md)
</dt> <dt>

[**ncacn\_spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**string binding**](https://docs.microsoft.com/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 




