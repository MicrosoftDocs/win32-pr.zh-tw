---
description: 這個類別是分頁錯誤事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972192"
---
# <a name="pagefault_v2-class"></a><span data-ttu-id="d57b9-104">PageFault \_ V2 類別</span><span class="sxs-lookup"><span data-stu-id="d57b9-104">PageFault\_V2 class</span></span>

<span data-ttu-id="d57b9-105">這個類別是分頁錯誤事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="d57b9-105">This class is the parent class for page fault events.</span></span>

<span data-ttu-id="d57b9-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d57b9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57b9-107">語法</span><span class="sxs-lookup"><span data-stu-id="d57b9-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d57b9-108">成員</span><span class="sxs-lookup"><span data-stu-id="d57b9-108">Members</span></span>

<span data-ttu-id="d57b9-109">**PageFault \_ V2** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="d57b9-109">The **PageFault\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57b9-110">備註</span><span class="sxs-lookup"><span data-stu-id="d57b9-110">Remarks</span></span>

<span data-ttu-id="d57b9-111">若要在 NT 核心記錄會話中啟用所有分頁錯誤事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 記憶體 \_ 頁面 \_ 錯誤** 旗標。</span><span class="sxs-lookup"><span data-stu-id="d57b9-111">To enable all page fault events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="d57b9-112">您也可以指定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="d57b9-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="d57b9-113">**事件 \_ 追蹤 \_ 旗標 \_ 記憶體 \_ 硬性 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d57b9-113">**EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS**</span></span>
-   <span data-ttu-id="d57b9-114">**事件 \_ 追蹤 \_ 旗標 \_ 虛擬 \_ 分配**</span><span class="sxs-lookup"><span data-stu-id="d57b9-114">**EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC**</span></span>

<span data-ttu-id="d57b9-115">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**PageFaultGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對所有分頁錯誤事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="d57b9-115">Event trace consumers can implement special processing for all page fault events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PageFaultGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="d57b9-116">使用下列事件種類來識別使用事件時的實際記憶體事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-116">Use the following event types to identify the actual memory event when consuming events.</span></span>



| <span data-ttu-id="d57b9-117">事件類型</span><span class="sxs-lookup"><span data-stu-id="d57b9-117">Event type</span></span>                                                     | <span data-ttu-id="d57b9-118">描述</span><span class="sxs-lookup"><span data-stu-id="d57b9-118">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57b9-119">事件 \_ 追蹤 \_ 類型 \_ MM \_ 牛 (事件種類值為 12) </span><span class="sxs-lookup"><span data-stu-id="d57b9-119">EVENT\_TRACE\_TYPE\_MM\_COW(Event type value is 12)</span></span><br/> | <span data-ttu-id="d57b9-120">複製時寫入事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-120">Copy-on-write event.</span></span> <span data-ttu-id="d57b9-121">[**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-121">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d57b9-122">在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-122">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>     |
| <span data-ttu-id="d57b9-123">事件 \_ 追蹤 \_ 類型 \_ MM \_ DZF (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="d57b9-123">EVENT\_TRACE\_TYPE\_MM\_DZF(Event type value is 11)</span></span><br/> | <span data-ttu-id="d57b9-124">要求零錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-124">Demand zero fault event.</span></span> <span data-ttu-id="d57b9-125">[**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-125">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d57b9-126">在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-126">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span> |
| <span data-ttu-id="d57b9-127">事件 \_ 追蹤 \_ 類型 \_ MM \_ GPF (事件種類值為 13) </span><span class="sxs-lookup"><span data-stu-id="d57b9-127">EVENT\_TRACE\_TYPE\_MM\_GPF(Event type value is 13)</span></span><br/> | <span data-ttu-id="d57b9-128">防護分頁錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-128">Guard page fault event.</span></span> <span data-ttu-id="d57b9-129">[**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-129">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d57b9-130">在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-130">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="d57b9-131">事件 \_ 追蹤 \_ 類型 \_ MM \_ HPF (事件種類值為 14) </span><span class="sxs-lookup"><span data-stu-id="d57b9-131">EVENT\_TRACE\_TYPE\_MM\_HPF(Event type value is 14)</span></span><br/> | <span data-ttu-id="d57b9-132">硬分頁錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-132">Hard page fault event.</span></span> <span data-ttu-id="d57b9-133">[**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-133">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d57b9-134">在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-134">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>   |
| <span data-ttu-id="d57b9-135">事件 \_ 追蹤 \_ 類型 \_ MM \_ TF (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="d57b9-135">EVENT\_TRACE\_TYPE\_MM\_TF(Event type value is 10)</span></span><br/>  | <span data-ttu-id="d57b9-136">轉換錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-136">Transition fault event.</span></span> <span data-ttu-id="d57b9-137">[**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-137">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="d57b9-138">在 Windows Vista 之前， [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) MOF 類別會定義事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-138">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="d57b9-139">事件 \_ 追蹤 \_ 類型 \_ MM \_ AV (事件種類值為 15) </span><span class="sxs-lookup"><span data-stu-id="d57b9-139">EVENT\_TRACE\_TYPE\_MM\_AV(Event type value is 15)</span></span><br/>  | <span data-ttu-id="d57b9-140">存取違規事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-140">Access violation event.</span></span> <span data-ttu-id="d57b9-141">[**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-141">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                           |
| <span data-ttu-id="d57b9-142">事件種類值，32</span><span class="sxs-lookup"><span data-stu-id="d57b9-142">Event type value, 32</span></span>                                           | <span data-ttu-id="d57b9-143">硬分頁錯誤事件。 [**PageFault \_ HardFault**](pagefault-hardfault.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-143">Hard page fault event.The [**PageFault\_HardFault**](pagefault-hardfault.md) MOF class defines the event data for this event.</span></span>                                                                                                                               |
| <span data-ttu-id="d57b9-144">事件種類值，105</span><span class="sxs-lookup"><span data-stu-id="d57b9-144">Event type value, 105</span></span>                                          | <span data-ttu-id="d57b9-145">分頁檔案事件中的影像載入。</span><span class="sxs-lookup"><span data-stu-id="d57b9-145">Image load in page file event.</span></span> <span data-ttu-id="d57b9-146">[**PageFault \_ ImageLoadBacked**](pagefault-imageloadbacked.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-146">The [**PageFault\_ImageLoadBacked**](pagefault-imageloadbacked.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="d57b9-147">事件種類值，98</span><span class="sxs-lookup"><span data-stu-id="d57b9-147">Event type value, 98</span></span>                                           | <span data-ttu-id="d57b9-148">虛擬配置事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-148">Virtual allocation event.</span></span> <span data-ttu-id="d57b9-149">[**VirtualAlloc**](pagefault-virtualalloc.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-149">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="d57b9-150">事件種類值，99</span><span class="sxs-lookup"><span data-stu-id="d57b9-150">Event type value, 99</span></span>                                           | <span data-ttu-id="d57b9-151">虛擬釋放事件。</span><span class="sxs-lookup"><span data-stu-id="d57b9-151">Virtual free event.</span></span> <span data-ttu-id="d57b9-152">[**VirtualAlloc**](pagefault-virtualalloc.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="d57b9-152">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                      |



 

<span data-ttu-id="d57b9-153">您可以使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員，找出錯誤的進程或執行緒。</span><span class="sxs-lookup"><span data-stu-id="d57b9-153">You can use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the faulting process or thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="d57b9-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="d57b9-154">Requirements</span></span>



| <span data-ttu-id="d57b9-155">需求</span><span class="sxs-lookup"><span data-stu-id="d57b9-155">Requirement</span></span> | <span data-ttu-id="d57b9-156">值</span><span class="sxs-lookup"><span data-stu-id="d57b9-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d57b9-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d57b9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d57b9-158">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d57b9-158">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d57b9-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d57b9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d57b9-160">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d57b9-160">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
