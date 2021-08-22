---
description: 這個類別是 ALPC 接收訊息事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: ALPC_Receive_Message 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98a565ea445ddd803ce217abca3993c2561d464829635bbb1a546824f27c3b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070358"
---
# <a name="alpc_receive_message-class"></a>ALPC \_ Receive \_ Message 類別

這個類別是 ALPC 接收訊息事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>成員

**ALPC \_ Receive \_ Message** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ALPC \_ Receive \_ Message** 類別具有這些屬性。

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



 

 




