---
title: ncadg_mq 屬性
description: Ncadg \_ mq 關鍵字會識別 Microsoft Message Queuing 服務 (MSMQ) 作為端點的傳輸通訊協定。 此通訊協定已淘汰，不應在新的應用程式中使用。
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq 屬性 MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164211a267760a533d8d164a76387dbbcfba8a0aad8e4ac6ecaf20ed770708a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067018"
---
# <a name="ncadg_mq-attribute"></a>ncadg \_ mq 屬性

**Ncadg \_ mq** 關鍵字會識別 MICROSOFT MESSAGE QUEUING 服務 (MSMQ) 作為端點的傳輸通訊協定。 此通訊協定已淘汰，不應在新的應用程式中使用。

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>參數

<dl> <dt>

*伺服器名稱* 
</dt> <dd>

指定伺服器或主機的電腦名稱稱。 名稱是字元字串，而且可能是完整的功能變數名稱。

</dd> </dl>

## <a name="remarks"></a>備註

若要使用 **ncadg \_ mq** 傳輸通訊協定，必須完整安裝 MSMQ 元件，而且用戶端和伺服器系統必須可透過 mq 通訊協定連線。

**Ncadg \_ mq** 通訊協定不支援動態端點或 [**廣播**](broadcast.md)呼叫。 如同其他資料包通訊協定， **ncadg \_ mq** 不支援回呼; 使用 [**回呼**](callback.md) 屬性的任何函式都將會失敗。

> [!Note]  
> Windows XP 不支援此通訊協定系列。

 

## <a name="examples"></a>範例

訊息佇列通訊協定的語法會與 IDL 規格分開定義。 MIDL 編譯器會執行一些語法檢查，但不保證端點規格是正確的。 某些錯誤可能會在執行時間（而不是在編譯期間）回報。

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**廣播**](broadcast.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**消息**](message.md)
</dt> <dt>

[RPC 訊息佇列](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[字串系結](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 