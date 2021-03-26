---
description: 此類別是就緒執行緒事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: ReadyThread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848170"
---
# <a name="readythread-class"></a>ReadyThread 類別

此類別是就緒執行緒事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a>成員

**ReadyThread** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ReadyThread** 類別具有這些屬性。

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

要調整優先順序的值。

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

提高優先順序的原因。



| 值                                                                        | 意義                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 略過增量。<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | 套用增量，這會在每個量子的結尾以累加方式衰減。<br/>                              |
| <dl> <dt>2</dt> </dl> | 套用增量作為提升，在量子 (通常會在優先順序捐贈) 中全面衰減。<br/> |



 

</dd> <dt>

旗標
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

以下是可能的狀態旗標：



| 值                                                                          | 意義                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | 已經從 DPC 準備好執行緒 (延後程序呼叫) 。<br/> |
| <dl> <dt>0x2</dt> </dl> | 核心堆疊目前已交換。<br/>                      |
| <dl> <dt>0x4</dt> </dl> | 進程位址空間已交換。<br/>                       |



 

請注意，當核心堆疊或進程位址空間已交換時，會在核心堆疊或進程位址空間交換之後，還有一個額外的 ReadyThread 事件，並讓執行緒準備好分派。

</dd> <dt>

保留
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

保留的。

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，格式 ( "x" ) 
</dt> </dl>

要準備好執行之執行緒的執行緒識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**執行緒 \_ V2**](thread-v2.md)
</dt> </dl>

 

 




