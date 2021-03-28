---
description: 這個類別是 ALPC 傳送訊息事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: ALPC_Send_Message 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113892"
---
# <a name="alpc_send_message-class"></a>ALPC \_ 傳送 \_ 訊息類別

這個類別是 ALPC 傳送訊息事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>成員

**ALPC \_ 傳送 \_ 訊息** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ALPC \_ 傳送 \_ 訊息** 類別具有這些屬性。

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



 

 




