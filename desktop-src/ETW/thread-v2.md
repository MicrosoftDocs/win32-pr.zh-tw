---
description: 這個類別是執行緒事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: f28b68a2aac5f2d5293f94ed2bab366d238ae662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850008"
---
# <a name="thread_v2-class"></a><span data-ttu-id="3c0ed-104">執行緒 \_ V2 類別</span><span class="sxs-lookup"><span data-stu-id="3c0ed-104">Thread\_V2 class</span></span>

<span data-ttu-id="3c0ed-105">這個類別是執行緒事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="3c0ed-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0ed-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c0ed-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3c0ed-108">成員</span><span class="sxs-lookup"><span data-stu-id="3c0ed-108">Members</span></span>

<span data-ttu-id="3c0ed-109">**執行緒 \_ V2** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c0ed-110">備註</span><span class="sxs-lookup"><span data-stu-id="3c0ed-110">Remarks</span></span>

<span data-ttu-id="3c0ed-111">若要在 NT 核心記錄會話中啟用執行緒事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 執行緒** 旗標。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="3c0ed-112">您也可以指定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="3c0ed-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="3c0ed-113">**事件 \_ 追蹤 \_ 旗標 \_ CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="3c0ed-114">**事件 \_ 追蹤 \_ 旗標 \_ 發送器**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="3c0ed-115">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**ThreadGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對執行緒事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="3c0ed-116">使用下列事件種類來識別使用事件時的實際執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="3c0ed-117">事件類型</span><span class="sxs-lookup"><span data-stu-id="3c0ed-117">Event type</span></span>                                                      | <span data-ttu-id="3c0ed-118">描述</span><span class="sxs-lookup"><span data-stu-id="3c0ed-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0ed-119">**活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) </span><span class="sxs-lookup"><span data-stu-id="3c0ed-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="3c0ed-120">結束執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-120">End thread event.</span></span> <span data-ttu-id="3c0ed-121">[**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="3c0ed-122">**活動 \_追蹤 \_ 類型 \_ 開始** (事件種類值為 1) </span><span class="sxs-lookup"><span data-stu-id="3c0ed-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="3c0ed-123">啟動執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-123">Start thread event.</span></span> <span data-ttu-id="3c0ed-124">[**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="3c0ed-125">事件種類值、3</span><span class="sxs-lookup"><span data-stu-id="3c0ed-125">Event type value, 3</span></span>                                             | <span data-ttu-id="3c0ed-126">開始資料收集執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-126">Start data collection thread event.</span></span> <span data-ttu-id="3c0ed-127">列舉核心會話開始時正在執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="3c0ed-128">[**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3c0ed-129">事件種類值，4</span><span class="sxs-lookup"><span data-stu-id="3c0ed-129">Event type value, 4</span></span>                                             | <span data-ttu-id="3c0ed-130">結束資料收集執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-130">End data collection thread event.</span></span> <span data-ttu-id="3c0ed-131">列舉核心會話結束時目前正在執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="3c0ed-132">[**執行緒 \_ V2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="3c0ed-133">事件種類值，36</span><span class="sxs-lookup"><span data-stu-id="3c0ed-133">Event type value, 36</span></span>                                            | <span data-ttu-id="3c0ed-134">內容切換事件。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-134">Context switch event.</span></span> <span data-ttu-id="3c0ed-135">[**CSwitch**](cswitch.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="3c0ed-136">事件種類值，50</span><span class="sxs-lookup"><span data-stu-id="3c0ed-136">Event type value, 50</span></span>                                            | <span data-ttu-id="3c0ed-137">就緒的執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-137">Ready thread event.</span></span> <span data-ttu-id="3c0ed-138">[**ReadyThread**](readythread.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="3c0ed-139">進程和執行緒啟動事件可能會記錄在父進程或執行緒的內容中。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="3c0ed-140">因此，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員可能不會對應到正在建立的進程和執行緒。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="3c0ed-141">這就是為什麼這些事件包含事件資料 (中的進程和執行緒識別碼，以及事件標頭) 中的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c0ed-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0ed-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c0ed-142">Requirements</span></span>



| <span data-ttu-id="3c0ed-143">需求</span><span class="sxs-lookup"><span data-stu-id="3c0ed-143">Requirement</span></span> | <span data-ttu-id="3c0ed-144">值</span><span class="sxs-lookup"><span data-stu-id="3c0ed-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c0ed-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c0ed-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0ed-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0ed-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3c0ed-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c0ed-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0ed-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0ed-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c0ed-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c0ed-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0ed-150">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="3c0ed-151">**CSwitch**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="3c0ed-152">**執行緒**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="3c0ed-153">**執行緒 \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="3c0ed-154">**執行緒 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="3c0ed-155">**執行緒 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="3c0ed-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
