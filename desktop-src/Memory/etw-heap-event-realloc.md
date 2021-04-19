---
description: 堆積重新配置作業的記憶體管理追蹤事件。
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: 'ETW_HEAP_EVENT_REALLOC (Ntwmi 的事件) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975080"
---
# <a name="etw_heap_event_realloc-event"></a><span data-ttu-id="9310a-103">ETW \_ 堆積 \_ 事件 \_ REALLOC 事件</span><span class="sxs-lookup"><span data-stu-id="9310a-103">ETW\_HEAP\_EVENT\_REALLOC event</span></span>

<span data-ttu-id="9310a-104">**ETW \_ 堆積 \_ 事件 \_ REALLOC** 事件是堆積重新配置作業的記憶體管理追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="9310a-104">The **ETW\_HEAP\_EVENT\_REALLOC** event is a memory management tracing event for a heap reallocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a><span data-ttu-id="9310a-105">參數</span><span class="sxs-lookup"><span data-stu-id="9310a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9310a-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="9310a-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="9310a-107">配置記憶體之堆積的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9310a-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="9310a-108">這是在配置記憶體時，處理傳遞至 [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) 函式的應用程式的堆積。</span><span class="sxs-lookup"><span data-stu-id="9310a-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="9310a-109">*NewAddress*</span><span class="sxs-lookup"><span data-stu-id="9310a-109">*NewAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="9310a-110">已配置之記憶體的新位址。</span><span class="sxs-lookup"><span data-stu-id="9310a-110">The new address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="9310a-111">*OldAddress*</span><span class="sxs-lookup"><span data-stu-id="9310a-111">*OldAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="9310a-112">先前配置之記憶體的舊位址。</span><span class="sxs-lookup"><span data-stu-id="9310a-112">The old address of the memory that was previously allocated.</span></span>

</dd> <dt>

<span data-ttu-id="9310a-113">*NewSize*</span><span class="sxs-lookup"><span data-stu-id="9310a-113">*NewSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9310a-114">從堆積配置的新大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9310a-114">The new size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="9310a-115">*OldSize*</span><span class="sxs-lookup"><span data-stu-id="9310a-115">*OldSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9310a-116">先前從堆積配置的舊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9310a-116">The old size in bytes previously allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="9310a-117">*來源*</span><span class="sxs-lookup"><span data-stu-id="9310a-117">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="9310a-118">配置器用於堆積配置的記憶體來源。</span><span class="sxs-lookup"><span data-stu-id="9310a-118">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="9310a-119">下表列出 *ntetw .h* 標頭檔中所定義之 *Source* 參數的可能值：</span><span class="sxs-lookup"><span data-stu-id="9310a-119">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="9310a-120">值</span><span class="sxs-lookup"><span data-stu-id="9310a-120">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="9310a-121">意義</span><span class="sxs-lookup"><span data-stu-id="9310a-121">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="9310a-122"><dt>**記憶體 \_從 \_ 對應**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9310a-122"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="9310a-123">對應清單中的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9310a-123">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="9310a-124"><dt>**記憶體 \_從 \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9310a-124"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="9310a-125">來自低片段堆積的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9310a-125">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="9310a-126"><dt>**記憶體 \_從 \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9310a-126"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="9310a-127">主要程式碼路徑中的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9310a-127">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="9310a-128"><dt> **\_ \_ SLOWPATH 4 的記憶體**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9310a-128"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="9310a-129">來自緩慢 c 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9310a-129">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="9310a-130"><dt>**記憶體 \_從 \_ 不正確**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9310a-130"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="9310a-131">不正確記憶體。</span><span class="sxs-lookup"><span data-stu-id="9310a-131">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="9310a-132"><dt>**記憶體 \_從 \_ 區段 \_ 堆積**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9310a-132"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="9310a-133">此值已保留供日後使用，且永遠不會傳回。</span><span class="sxs-lookup"><span data-stu-id="9310a-133">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

<span data-ttu-id="9310a-134">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9310a-134">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9310a-135">備註</span><span class="sxs-lookup"><span data-stu-id="9310a-135">Remarks</span></span>

<span data-ttu-id="9310a-136">**ETW \_ 堆積 \_ 事件 \_ REALLOC** 事件會記錄在所有堆積重新分配上。</span><span class="sxs-lookup"><span data-stu-id="9310a-136">The **ETW\_HEAP\_EVENT\_REALLOC** event is logged on all heap reallocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="9310a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="9310a-137">Requirements</span></span>



| <span data-ttu-id="9310a-138">需求</span><span class="sxs-lookup"><span data-stu-id="9310a-138">Requirement</span></span> | <span data-ttu-id="9310a-139">值</span><span class="sxs-lookup"><span data-stu-id="9310a-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9310a-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9310a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9310a-141">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9310a-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9310a-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9310a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9310a-143">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9310a-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9310a-144">標頭</span><span class="sxs-lookup"><span data-stu-id="9310a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9310a-145"><dt>Ntwmi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9310a-145"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9310a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9310a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9310a-147">記憶體管理追蹤事件</span><span class="sxs-lookup"><span data-stu-id="9310a-147">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
