---
description: 這個類別是執行緒結束事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Thread_V1_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512188"
---
# <a name="thread_v1_typegroup2-class"></a>Thread \_ V1 \_ TypeGroup2 類別

這個類別是執行緒結束事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a>成員

**Thread \_ V1 \_ TypeGroup2** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Thread \_ V1 \_ TypeGroup2** 類別具有這些屬性。

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

事件所涉及之執行緒的處理序識別碼。

**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

事件所涉及之執行緒的執行緒識別碼。

**Windows Server 2003：** 包含 ( "x" ) 限定詞的格式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**執行緒 \_ V1**](thread-v1.md)
</dt> </dl>

 

 




