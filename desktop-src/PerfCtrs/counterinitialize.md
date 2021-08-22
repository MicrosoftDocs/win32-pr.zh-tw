---
description: 註冊提供者，並初始化計數器集合。
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: CounterInitialize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: e7c2fb61b53ca1847eefcc453a91f69b3c0602e06277b4858b8f0b733be7f71b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517678"
---
# <a name="counterinitialize-function"></a>CounterInitialize 函式

註冊提供者，並初始化計數器集合。

## <a name="syntax"></a>語法


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

成功時傳回錯誤 \_ 成功，否則為標準 Win32 錯誤碼。

## <a name="remarks"></a>備註

您的提供者會呼叫這個函數。 函數包含對 [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) 函式和 [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) 函數的呼叫。

當您指定 **-o** 引數時， [**CTRPP**](ctrpp.md)工具會產生這個內嵌函數。 如果您指定 **-prefix** 引數，函式的名稱會包含 *前置* 字串。

如果您指定 **-MemoryRoutines** 或 **-NotificationCallback** 引數 (或指定 [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)元素) 的 **回呼** 屬性，則 **CounterInitialize** 簽章會變更為下列內容：

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

其中

<dl> <dt>

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback
</dt> <dd>

您 [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) 回呼函式的名稱，此函式可讓您用來接收取用者要求的通知 (例如，在查詢) 中加入或移除計數器的要求。 如果您未執行 *ControlCallback* 回呼函式，則設定為 **Null** 。

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction
</dt> <dd>

PERFLIB 呼叫以配置記憶體的 [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) 回呼函式名稱。 如果您未指定 **-MemoryRoutines** 引數，則設定為 **Null** 。

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction
</dt> <dd>

[*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)回呼函式的名稱，這個函式會 PERFLIB 呼叫來釋放使用 [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)函數配置的記憶體。 如果 *MemoryAllocationFunction* 為 **null**，則設定為 **null** 。

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionCoNtext
</dt> <dd>

要傳遞至記憶體配置和免費常式的內容資訊。 可以是 **Null**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

