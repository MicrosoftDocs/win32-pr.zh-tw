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
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944265"
---
# <a name="counterinitialize-function"></a><span data-ttu-id="eb2a9-103">CounterInitialize 函式</span><span class="sxs-lookup"><span data-stu-id="eb2a9-103">CounterInitialize function</span></span>

<span data-ttu-id="eb2a9-104">註冊提供者，並初始化計數器集合。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-104">Registers the provider and initializes the counter sets.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb2a9-105">Syntax</span></span>


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="eb2a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb2a9-106">Parameters</span></span>

<span data-ttu-id="eb2a9-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb2a9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb2a9-108">Return value</span></span>

<span data-ttu-id="eb2a9-109">成功時傳回錯誤 \_ 成功，否則為標準 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-109">Returns ERROR\_SUCCESS on success; otherwise, a standard Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb2a9-110">備註</span><span class="sxs-lookup"><span data-stu-id="eb2a9-110">Remarks</span></span>

<span data-ttu-id="eb2a9-111">您的提供者會呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-111">Your provider calls this function.</span></span> <span data-ttu-id="eb2a9-112">函數包含對 [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) 函式和 [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) 函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-112">The function includes calls to the [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) function and the [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) function.</span></span>

<span data-ttu-id="eb2a9-113">當您指定 **-o** 引數時， [**CTRPP**](ctrpp.md)工具會產生這個內嵌函數。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="eb2a9-114">如果您指定 **-prefix** 引數，函式的名稱會包含 *前置* 字串。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-114">The function's name include a *prefix* string if you specify the **-prefix** argument.</span></span>

<span data-ttu-id="eb2a9-115">如果您指定 **-MemoryRoutines** 或 **-NotificationCallback** 引數 (或指定 [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)元素) 的 **回呼** 屬性，則 **CounterInitialize** 簽章會變更為下列內容：</span><span class="sxs-lookup"><span data-stu-id="eb2a9-115">If you specify the **-MemoryRoutines** or **-NotificationCallback** arguments (or specify the **callback** attribute for the [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) element), the **CounterInitialize** signature changes to the following:</span></span>

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

<span data-ttu-id="eb2a9-116">其中</span><span class="sxs-lookup"><span data-stu-id="eb2a9-116">where,</span></span>

<dl> <dt>

<span data-ttu-id="eb2a9-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span><span class="sxs-lookup"><span data-stu-id="eb2a9-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span></span>
</dt> <dd>

<span data-ttu-id="eb2a9-118">您 [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) 回呼函式的名稱，此函式可讓您用來接收取用者要求的通知 (例如，在查詢) 中加入或移除計數器的要求。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-118">The name of your [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) callback function that you implement to receive notification of consumer requests (for example, requests to add or remove counters from the query).</span></span> <span data-ttu-id="eb2a9-119">如果您未執行 *ControlCallback* 回呼函式，則設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-119">Set to **NULL** if you do not implement the *ControlCallback* callback function.</span></span>

</dd> <dt>

<span data-ttu-id="eb2a9-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span><span class="sxs-lookup"><span data-stu-id="eb2a9-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span></span>
</dt> <dd>

<span data-ttu-id="eb2a9-121">PERFLIB 呼叫以配置記憶體的 [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) 回呼函式名稱。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-121">The name of your [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) callback function that PERFLIB calls to allocate memory.</span></span> <span data-ttu-id="eb2a9-122">如果您未指定 **-MemoryRoutines** 引數，則設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-122">Set to **NULL** if you did not specify the **-MemoryRoutines** argument.</span></span>

</dd> <dt>

<span data-ttu-id="eb2a9-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span><span class="sxs-lookup"><span data-stu-id="eb2a9-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span></span>
</dt> <dd>

<span data-ttu-id="eb2a9-124">[*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)回呼函式的名稱，這個函式會 PERFLIB 呼叫來釋放使用 [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)函數配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-124">The name of your [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) callback function that PERFLIB calls to free the memory allocated using the [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) function.</span></span> <span data-ttu-id="eb2a9-125">如果 *MemoryAllocationFunction* 為 **null**，則設定為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-125">Set to **NULL** if *MemoryAllocationFunction* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eb2a9-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionCoNtext</span><span class="sxs-lookup"><span data-stu-id="eb2a9-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span></span>
</dt> <dd>

<span data-ttu-id="eb2a9-127">要傳遞至記憶體配置和免費常式的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-127">Context information to pass to your memory allocation and free routines.</span></span> <span data-ttu-id="eb2a9-128">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="eb2a9-128">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb2a9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb2a9-129">Requirements</span></span>



| <span data-ttu-id="eb2a9-130">需求</span><span class="sxs-lookup"><span data-stu-id="eb2a9-130">Requirement</span></span> | <span data-ttu-id="eb2a9-131">值</span><span class="sxs-lookup"><span data-stu-id="eb2a9-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="eb2a9-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb2a9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eb2a9-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb2a9-133">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="eb2a9-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb2a9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eb2a9-135">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb2a9-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

