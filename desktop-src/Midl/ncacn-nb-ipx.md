---
title: ncacn_nb_ipx 屬性
description: Ncacn \_ nb \_ ipx 關鍵字會將 NETBIOS 透過 ipx 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106995565"
---
# <a name="ncacn_nb_ipx-attribute"></a>ncacn \_ nb \_ ipx 屬性

**Ncacn \_ nb \_ ipx** 關鍵字會將 NetBIOS 透過 ipx 識別為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*埠名稱* 
</dt> <dd>

指定選擇性的8位值範圍從1到254。 小於0x20 的值會保留下來。 如果未指定 *埠名稱* 值，則端點對應服務會選取埠值。

</dd> </dl>

## <a name="remarks"></a>備註

NetBIOS 埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。 MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。 某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。

> [!Note]  
> Windows XP 不支援此通訊協定系列。

 

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**\_在 \_ dsp ncacn**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**字串系結**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 