---
description: Thread_V2_TypeGroup1 類別-這個類別是執行緒開始和結束事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 24ac4655fc374c40eb530828229a319f9ee1375e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105656"
---
# <a name="thread_v2_typegroup1-class"></a>執行緒 \_ V2 \_ TypeGroup1 類別

這個類別是執行緒開始和結束事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a>成員

**執行緒 \_ V2 \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**執行緒 \_ V2 \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，格式 ( "x" ) 
</dt> </dl>

事件所涉及之執行緒的處理序識別碼。

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

SubProcessTag
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (10) ，格式 ( "x" ) 
</dt> </dl>

識別服務（如果執行緒是由服務所擁有）;否則為零。

</dd> <dt>

TebBase
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (9) ，指標
</dt> </dl>

執行緒環境區塊基底位址。

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，格式 ( "x" ) 
</dt> </dl>

事件所涉及之執行緒的執行緒識別碼。

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

## <a name="remarks"></a>備註

DCStart 和 DCEnd 事件種類會列舉核心會話開始和結束時，目前正在執行的執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**執行緒**](thread.md)
</dt> <dt>

[**執行緒 \_ V2**](thread-v2.md)
</dt> </dl>

 

 




