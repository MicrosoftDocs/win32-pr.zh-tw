---
description: 這個類別是堆疊追蹤事件的事件種類類別。
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: StackWalk_Event 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973413"
---
# <a name="stackwalk_event-class"></a>StackWalk \_ 事件類別

這個類別是堆疊追蹤事件的事件種類類別。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a>成員

**StackWalk \_ 事件** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**StackWalk \_ 事件** 類別具有這些屬性。

<dl> <dt>

**EventTimeStamp**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

事件標頭中的原始事件時間戳記。 您可以使用此時間戳記，將堆疊與事件進行比對。

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，指標
</dt> </dl>

呼叫的位址。

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (195) ，指標
</dt> </dl>

呼叫的位址。

</dd> <dt>

**StackProcess**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，格式 ( "x" ) 
</dt> </dl>

原始事件的處理序識別碼。

</dd> <dt>

**StackThread**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

原始事件的執行緒識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，此類別不會顯示存在於 **Stack1** 與 **Stack192** 之間的所有 **Stack * n*** 屬性。 使用事件的大小，判斷有多少 **Stack * n*** 屬性包含有效的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 




