---
description: 這個類別是執行緒啟動事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Thread_V1_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 90d8f4afe9d78cc774dea3159a728ccc6d4db52314e692594d026f7e4fe2161c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069438"
---
# <a name="thread_v1_typegroup1-class"></a>Thread \_ V1 \_ TypeGroup1 類別

這個類別是執行緒啟動事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a>成員

**Thread \_ V1 \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Thread \_ V1 \_ TypeGroup1** 類別具有這些屬性。

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

StackBase
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，指標
</dt> </dl>

執行緒堆疊的基底位址。

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，指標
</dt> </dl>

執行緒堆疊的限制。

</dd> <dt>

StartAddr
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) ，指標
</dt> </dl>

追蹤開始的記憶體位址。

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

</dd> <dt>

UserStackBase
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) ，指標
</dt> </dl>

執行緒使用者模式堆疊的基底位址。

</dd> <dt>

UserStackLimit
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) ，指標
</dt> </dl>

執行緒使用者模式堆疊的限制。

</dd> <dt>

WaitMode
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (9) ，Format ( "c" ) 
</dt> </dl>

未使用。

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) ，指標
</dt> </dl>

此執行緒要執行之函式的起始位址。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**執行緒 \_ V1**](thread-v1.md)
</dt> </dl>

 

 




