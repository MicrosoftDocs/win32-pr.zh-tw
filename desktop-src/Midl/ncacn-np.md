---
title: ncacn_np 屬性
description: Ncacn \_ np 關鍵字會將具名管道識別為端點的通訊協定系列。
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np 屬性 MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7acf294241c1d38b2067ba54e315fc3240e5bb6eca81a6b12012f8dec457a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013756"
---
# <a name="ncacn_np-attribute"></a>ncacn \_ np 屬性

**Ncacn \_ np** 關鍵字會將具名管道識別為端點的通訊協定系列。

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>參數

<dl> <dt>

*伺服器名稱* 
</dt> <dd>

選擇性。 指定伺服器的名稱。 反斜線字元是選擇性的。

</dd> <dt>

*管道名稱* 
</dt> <dd>

指定有效的管道名稱。 有效的管道名稱是一個字串，其中包含以反斜線字元分隔的識別碼。 第一個識別碼必須是 [**管道**](pipe.md)。 每個識別碼都必須以兩個反斜線字元分隔。

</dd> </dl>

## <a name="remarks"></a>備註

伺服器會建立具名管道的實例，然後可供任何用戶端使用。 當用戶端嘗試連接時，現有的實例會與該用戶端相關聯。 在另一個用戶端可以連線之前，伺服器必須建立另一個具名管道的實例。 如果用戶端在建立新的實例之前嘗試系結至伺服器，系結呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding)可能會失敗，並出現錯誤訊息： RPC \_ S \_ 伺服器 \_ 太 \_ 忙碌。 因此，您必須確定您的用戶端應用程式會處理伺服器太忙碌而無法接受連接的情況。 用戶端應該會自動重試、提示使用者進行動作，或正常地失敗。

具名管道埠字串的語法（如同所有的埠字串）是由傳輸執行所定義，而且與 IDL 規格無關。 MIDL 編譯器會執行有限的語法檢查，但不保證端點規格是正確的。 某些錯誤類別可能會在執行時間（而不是在編譯時期）回報。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
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

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**字串系結**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 