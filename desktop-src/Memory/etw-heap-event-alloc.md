---
description: 堆積配置作業的記憶體管理追蹤事件。
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: 'ETW_HEAP_EVENT_ALLOC (Ntwmi 的事件) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318424"
---
# <a name="etw_heap_event_alloc-event"></a><span data-ttu-id="1c337-103">ETW \_ 堆積 \_ 事件 \_ 分配事件</span><span class="sxs-lookup"><span data-stu-id="1c337-103">ETW\_HEAP\_EVENT\_ALLOC event</span></span>

<span data-ttu-id="1c337-104">**ETW \_ 堆積 \_ 事件 \_ 分配** 事件是堆積配置作業的記憶體管理追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="1c337-104">The **ETW\_HEAP\_EVENT\_ALLOC** event is a memory management tracing event for a heap allocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a><span data-ttu-id="1c337-105">參數</span><span class="sxs-lookup"><span data-stu-id="1c337-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c337-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="1c337-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="1c337-107">配置記憶體之堆積的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c337-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="1c337-108">這是在配置記憶體時，處理傳遞至 [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) 函式的應用程式的堆積。</span><span class="sxs-lookup"><span data-stu-id="1c337-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="1c337-109">*大小*</span><span class="sxs-lookup"><span data-stu-id="1c337-109">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="1c337-110">從堆積配置的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1c337-110">The size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="1c337-111">*位址*</span><span class="sxs-lookup"><span data-stu-id="1c337-111">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="1c337-112">已配置之記憶體的位址。</span><span class="sxs-lookup"><span data-stu-id="1c337-112">The address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="1c337-113">*來源*</span><span class="sxs-lookup"><span data-stu-id="1c337-113">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="1c337-114">配置器用於堆積配置的記憶體來源。</span><span class="sxs-lookup"><span data-stu-id="1c337-114">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="1c337-115">下表列出 *ntetw .h* 標頭檔中所定義之 *Source* 參數的可能值：</span><span class="sxs-lookup"><span data-stu-id="1c337-115">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="1c337-116">值</span><span class="sxs-lookup"><span data-stu-id="1c337-116">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="1c337-117">意義</span><span class="sxs-lookup"><span data-stu-id="1c337-117">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="1c337-118"><dt>**記憶體 \_從 \_ 對應**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1c337-118"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="1c337-119">對應清單中的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1c337-119">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="1c337-120"><dt>**記憶體 \_從 \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1c337-120"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="1c337-121">來自低片段堆積的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1c337-121">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="1c337-122"><dt>**記憶體 \_從 \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1c337-122"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="1c337-123">主要程式碼路徑中的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1c337-123">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="1c337-124"><dt> **\_ \_ SLOWPATH 4 的記憶體**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1c337-124"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="1c337-125">來自慢速路徑的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1c337-125">Memory from slow path.</span></span><br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="1c337-126"><dt>**記憶體 \_從 \_ 不正確**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1c337-126"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="1c337-127">不正確記憶體。</span><span class="sxs-lookup"><span data-stu-id="1c337-127">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="1c337-128"><dt>**記憶體 \_從 \_ 區段 \_ 堆積**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1c337-128"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="1c337-129">此值已保留供日後使用，且永遠不會傳回。</span><span class="sxs-lookup"><span data-stu-id="1c337-129">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c337-130">備註</span><span class="sxs-lookup"><span data-stu-id="1c337-130">Remarks</span></span>

<span data-ttu-id="1c337-131">**ETW \_ 堆積 \_ 事件 \_ 分配** 事件會記錄在所有堆積配置上。</span><span class="sxs-lookup"><span data-stu-id="1c337-131">The **ETW\_HEAP\_EVENT\_ALLOC** event is logged on all heap allocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c337-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c337-132">Requirements</span></span>



| <span data-ttu-id="1c337-133">需求</span><span class="sxs-lookup"><span data-stu-id="1c337-133">Requirement</span></span> | <span data-ttu-id="1c337-134">值</span><span class="sxs-lookup"><span data-stu-id="1c337-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c337-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c337-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1c337-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c337-136">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1c337-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c337-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1c337-138">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c337-138">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1c337-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1c337-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c337-140"><dt>Ntwmi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c337-140"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c337-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c337-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c337-142">記憶體管理追蹤事件</span><span class="sxs-lookup"><span data-stu-id="1c337-142">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
