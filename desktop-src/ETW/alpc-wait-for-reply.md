---
description: 此類別是 ALPC 等候回復事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: ALPC_Wait_For_Reply 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b2f2e867e3e95e8ba0916ad288363db7ad8b6a7753f956df5415529d8ec5e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070308"
---
# <a name="alpc_wait_for_reply-class"></a>ALPC \_ 等候 \_ \_ 回復類別

此類別是 ALPC 等候回復事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>成員

**ALPC \_ 等候 \_ \_ 回復** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ALPC \_ 等候 \_ \_ 回復** 類別具有這些屬性。

<dl> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

訊息識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




