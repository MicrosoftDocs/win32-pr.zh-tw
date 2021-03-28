---
description: 這個類別是內容切換事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: CSwitch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191611"
---
# <a name="cswitch-class"></a>CSwitch 類別

這個類別是內容切換事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a>成員

**CSwitch** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CSwitch** 類別具有這些屬性。

<dl> <dt>

**NewThreadId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，格式 ( "x" ) 
</dt> </dl>

切換後的新執行緒識別碼。

</dd> <dt>

**NewThreadPriority**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

新執行緒的執行緒優先權。

</dd> <dt>

**NewThreadWaitTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (11) ，格式 ( "x" ) 
</dt> </dl>

新執行緒的等候時間。

</dd> <dt>

**OldThreadId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，格式 ( "x" ) 
</dt> </dl>

先前的執行緒識別碼。

</dd> <dt>

**OldThreadPriority**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

先前線程的執行緒優先權。

</dd> <dt>

**OldThreadState**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (9) 
</dt> </dl>

先前線程的狀態。 以下是可能的狀態值：

| 州 | 描述                                   |
|-------|-----------------------------------------------|
| 0     | Initialized                                   |
| 1     | 就緒                                         |
| 2     | 執行中                                       |
| 3     | 待命                                       |
| 4     | 已終止                                    |
| 5     | 等候中                                       |
| 6     | 轉換                                    |
| 7     | DeferredReady (為 Windows Server 2003) 新增 |



 

</dd> <dt>

**OldThreadWaitIdealProcessor**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (10) ，格式 ( "x" ) 
</dt> </dl>

先前線程的理想等候時間。

</dd> <dt>

**OldThreadWaitMode**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) 
</dt> </dl>

先前線程的等候模式。 以下是可能的值：

| 州 | 描述 |
|-------|-------------|
| 0     | KernelMode  |
| 1     | UserMode    |



 

</dd> <dt>

**OldThreadWaitReason**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) 
</dt> </dl>

先前線程的等候原因。 以下是可能的值：

| 州 | 描述       |
|-------|-------------------|
| 0     | 高階主管         |
| 1     | FreePage          |
| 2     | PageIn            |
| 3     | PoolAllocation    |
| 4     | DelayExecution    |
| 5     | 暫止         |
| 6     | UserRequest       |
| 7     | WrExecutive       |
| 8     | WrFreePage        |
| 9     | WrPageIn          |
| 10    | WrPoolAllocation  |
| 11    | WrDelayExecution  |
| 12    | WrSuspended       |
| 13    | WrUserRequest     |
| 14    | WrEventPair       |
| 15    | WrQueue           |
| 16    | WrLpcReceive      |
| 17    | WrLpcReply        |
| 18    | WrVirtualMemory   |
| 19    | WrPageOut         |
| 20    | WrRendezvous      |
| 21    | WrKeyedEvent      |
| 22    | WrTerminated      |
| 23    | WrProcessInSwap   |
| 24    | WrCpuRateControl  |
| 25    | WrCalloutStack    |
| 26    | WrKernel          |
| 27    | WrResource        |
| 28    | WrPushLock        |
| 29    | WrMutex           |
| 30    | WrQuantumEnd      |
| 31    | WrDispatchInt     |
| 32    | WrPreempted       |
| 33    | WrYieldExecution  |
| 34    | WrFastMutex       |
| 35    | WrGuardedMutex    |
| 36    | WrRundown         |
| 37    | MaximumWaitReason |



 

</dd> <dt>

**PreviousCState**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

處理器最後使用之 C 狀態的索引。 值為0表示最亮的閒置狀態，具有較高的值表示更深層的 C 狀態。

</dd> <dt>

**已保留**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (12) 
</dt> </dl>

保留的。

</dd> <dt>

**SpareByte**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

這些事件會產生大量的事件。

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

 

 




