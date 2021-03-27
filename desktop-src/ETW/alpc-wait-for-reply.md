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
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972237"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




