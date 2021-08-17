---
title: ncadg_ip_udp 屬性
description: Ncadg \_ ip \_ udp 關鍵字會識別 tcp/ip 的資料包版本，作為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp 屬性 MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91db32fd7636f956e64dafc0db15efb520e643b435995dd977db7a631a20c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067058"
---
# <a name="ncadg_ip_udp-attribute"></a>ncadg \_ ip \_ udp 屬性

**Ncadg \_ ip \_ udp** 關鍵字會識別 tcp/ip 的資料包版本，作為端點的通訊協定系列。 此通訊協定系列已淘汰，不應在新的應用程式中使用。

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*伺服器名稱* 
</dt> <dd>

指定伺服器或主機電腦的名稱或網際網路位址。 名稱是字元字串，而且可能是完整的功能變數名稱。 網際網路位址是常見的網際網路位址標記法。

</dd> <dt>

*埠名稱* 
</dt> <dd>

指定選用的16位數位。 通常會保留小於1024的值。 如果未指定任何值，則端點對應服務會選取有效的 *埠名稱* 值。

</dd> </dl>

## <a name="remarks"></a>備註

下列限制適用于資料包協定、 [**ncadg \_ ipx**](ncadg-ipx.md) 和 **ncadg \_ ip \_ udp**：

-   它們不支援回呼。 使用回呼屬性的任何函數 **\[** [](callback.md) **\]** 都會失敗。
-   它們不支援使用 [**管道**](pipe.md) 類型的函式。

TCP/IP 傳輸埠字串的語法（像是所有的埠字串），會與 IDL 規格分開定義。 編譯器會執行一些語法檢查，但不保證端點規格是正確的。 某些錯誤可能會在執行時間（而不是在編譯時期）回報。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
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

[**\_在 \_ dsp ncacn**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[字串系結](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 