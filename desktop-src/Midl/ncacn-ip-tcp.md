---
title: ncacn_ip_tcp 屬性
description: Ncacn \_ ip \_ tcp 關鍵字會將 tcp/ip 識別為端點的通訊協定系列。
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967479"
---
# <a name="ncacn_ip_tcp-attribute"></a>ncacn \_ ip \_ tcp 屬性

**Ncacn \_ ip \_ tcp** 關鍵字會將 tcp/ip 識別為端點的通訊協定系列。

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*伺服器名稱* 
</dt> <dd>

指定伺服器或主機電腦的名稱或網際網路位址。 名稱是字元字串。 網際網路位址是常見的網際網路位址標記法。

</dd> <dt>

*埠名稱* 
</dt> <dd>

指定選用的16位數位。 通常會保留小於1024的值。 如果未指定任何值，則端點對應服務會選取有效的 *埠名稱* 值。

</dd> </dl>

## <a name="remarks"></a>備註

TCP/IP 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。 編譯器會執行一些語法檢查，但不保證端點規格是正確的。 某些錯誤可能會在執行時間（而不是在編譯時期）回報。

## <a name="examples"></a>範例

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**字串系結**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 