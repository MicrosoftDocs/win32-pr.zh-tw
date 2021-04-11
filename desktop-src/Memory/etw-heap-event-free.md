---
description: 堆積免費作業的記憶體管理追蹤事件。
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: 'ETW_HEAP_EVENT_FREE (Ntwmi 的事件) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847945"
---
# <a name="etw_heap_event_free-event"></a><span data-ttu-id="9f7da-103">ETW \_ 堆積 \_ 事件 \_ 可用事件</span><span class="sxs-lookup"><span data-stu-id="9f7da-103">ETW\_HEAP\_EVENT\_FREE event</span></span>

<span data-ttu-id="9f7da-104">**ETW \_ 堆積 \_ 事件 \_ 可用** 事件是堆積免費作業的記憶體管理追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="9f7da-104">The **ETW\_HEAP\_EVENT\_FREE** event is a memory management tracing event for a heap free operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a><span data-ttu-id="9f7da-105">參數</span><span class="sxs-lookup"><span data-stu-id="9f7da-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f7da-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="9f7da-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7da-107">配置記憶體之堆積的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9f7da-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="9f7da-108">這是在配置記憶體時，處理傳遞至 [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) 函式的應用程式的堆積。</span><span class="sxs-lookup"><span data-stu-id="9f7da-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="9f7da-109">*位址*</span><span class="sxs-lookup"><span data-stu-id="9f7da-109">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7da-110">已釋放的記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="9f7da-110">The address of the memory that was freed.</span></span>

</dd> <dt>

<span data-ttu-id="9f7da-111">*來源*</span><span class="sxs-lookup"><span data-stu-id="9f7da-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7da-112">配置器用於堆積配置的記憶體來源。</span><span class="sxs-lookup"><span data-stu-id="9f7da-112">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="9f7da-113">下表列出 *ntetw .h* 標頭檔中所定義之 *Source* 參數的可能值：</span><span class="sxs-lookup"><span data-stu-id="9f7da-113">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="9f7da-114">值</span><span class="sxs-lookup"><span data-stu-id="9f7da-114">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="9f7da-115">意義</span><span class="sxs-lookup"><span data-stu-id="9f7da-115">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="9f7da-116"><dt>**記憶體 \_從 \_ 對應**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9f7da-116"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="9f7da-117">對應清單中的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9f7da-117">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="9f7da-118"><dt>**記憶體 \_從 \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9f7da-118"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="9f7da-119">來自低片段堆積的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9f7da-119">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="9f7da-120"><dt>**記憶體 \_從 \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9f7da-120"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="9f7da-121">主要程式碼路徑中的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9f7da-121">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="9f7da-122"><dt> **\_ \_ SLOWPATH 4 的記憶體**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9f7da-122"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="9f7da-123">來自緩慢 c 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9f7da-123">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="9f7da-124"><dt>**記憶體 \_從 \_ 不正確**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9f7da-124"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="9f7da-125">不正確記憶體。</span><span class="sxs-lookup"><span data-stu-id="9f7da-125">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="9f7da-126"><dt>**記憶體 \_從 \_ 區段 \_ 堆積**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9f7da-126"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="9f7da-127">此值已保留供日後使用，且永遠不會傳回。</span><span class="sxs-lookup"><span data-stu-id="9f7da-127">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f7da-128">備註</span><span class="sxs-lookup"><span data-stu-id="9f7da-128">Remarks</span></span>

<span data-ttu-id="9f7da-129">**ETW \_ 堆積 \_ 事件 \_ 可用** 事件會記錄在所有堆積的可用作業中。</span><span class="sxs-lookup"><span data-stu-id="9f7da-129">The **ETW\_HEAP\_EVENT\_FREE** event is logged on all heap free operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f7da-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f7da-130">Requirements</span></span>



| <span data-ttu-id="9f7da-131">需求</span><span class="sxs-lookup"><span data-stu-id="9f7da-131">Requirement</span></span> | <span data-ttu-id="9f7da-132">值</span><span class="sxs-lookup"><span data-stu-id="9f7da-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f7da-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f7da-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9f7da-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f7da-134">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9f7da-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f7da-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9f7da-136">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f7da-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9f7da-137">標頭</span><span class="sxs-lookup"><span data-stu-id="9f7da-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f7da-138"><dt>Ntwmi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f7da-138"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f7da-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f7da-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f7da-140">記憶體管理追蹤事件</span><span class="sxs-lookup"><span data-stu-id="9f7da-140">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
