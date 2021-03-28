---
description: 這個類別是處理事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: c055dc1f78da13c0dfa29bea948a8f0c94363ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944985"
---
# <a name="process_v2-class"></a><span data-ttu-id="ef58e-104">進程 \_ V2 類別</span><span class="sxs-lookup"><span data-stu-id="ef58e-104">Process\_V2 class</span></span>

<span data-ttu-id="ef58e-105">這個類別是處理事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="ef58e-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="ef58e-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="ef58e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef58e-107">語法</span><span class="sxs-lookup"><span data-stu-id="ef58e-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="ef58e-108">成員</span><span class="sxs-lookup"><span data-stu-id="ef58e-108">Members</span></span>

<span data-ttu-id="ef58e-109">**Process** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="ef58e-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef58e-110">備註</span><span class="sxs-lookup"><span data-stu-id="ef58e-110">Remarks</span></span>

<span data-ttu-id="ef58e-111">若要在 NT 核心記錄會話中啟用處理事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 處理** 旗標。</span><span class="sxs-lookup"><span data-stu-id="ef58e-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="ef58e-112">您也可以指定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="ef58e-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="ef58e-113">**事件 \_ 追蹤 \_ 旗標 \_ 進程 \_ 計數器**</span><span class="sxs-lookup"><span data-stu-id="ef58e-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="ef58e-114">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**ProcessGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來為進程事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="ef58e-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="ef58e-115">使用下列事件種類來識別使用事件時的實際處理事件。</span><span class="sxs-lookup"><span data-stu-id="ef58e-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="ef58e-116">事件類型</span><span class="sxs-lookup"><span data-stu-id="ef58e-116">Event type</span></span>                                                      | <span data-ttu-id="ef58e-117">描述</span><span class="sxs-lookup"><span data-stu-id="ef58e-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef58e-118">**活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) </span><span class="sxs-lookup"><span data-stu-id="ef58e-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="ef58e-119">結束進程事件。</span><span class="sxs-lookup"><span data-stu-id="ef58e-119">End process event.</span></span> <span data-ttu-id="ef58e-120">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="ef58e-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="ef58e-121">**活動 \_追蹤 \_ 類型 \_ 開始** (事件種類值為 1) </span><span class="sxs-lookup"><span data-stu-id="ef58e-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="ef58e-122">開始處理事件。</span><span class="sxs-lookup"><span data-stu-id="ef58e-122">Start process event.</span></span> <span data-ttu-id="ef58e-123">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="ef58e-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="ef58e-124">事件種類值、3</span><span class="sxs-lookup"><span data-stu-id="ef58e-124">Event type value, 3</span></span>                                             | <span data-ttu-id="ef58e-125">開始資料收集處理事件。</span><span class="sxs-lookup"><span data-stu-id="ef58e-125">Start data collection process event.</span></span> <span data-ttu-id="ef58e-126">列舉核心會話開始時正在執行的進程。</span><span class="sxs-lookup"><span data-stu-id="ef58e-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="ef58e-127">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="ef58e-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="ef58e-128">事件種類值，4</span><span class="sxs-lookup"><span data-stu-id="ef58e-128">Event type value, 4</span></span>                                             | <span data-ttu-id="ef58e-129">結束資料收集處理事件。</span><span class="sxs-lookup"><span data-stu-id="ef58e-129">End data collection process event.</span></span> <span data-ttu-id="ef58e-130">列舉核心會話結束時目前正在執行的進程。</span><span class="sxs-lookup"><span data-stu-id="ef58e-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="ef58e-131">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="ef58e-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="ef58e-132">事件種類值，32</span><span class="sxs-lookup"><span data-stu-id="ef58e-132">Event type value, 32</span></span>                                            | <span data-ttu-id="ef58e-133">效能計數器事件。</span><span class="sxs-lookup"><span data-stu-id="ef58e-133">Performance counters event.</span></span> <span data-ttu-id="ef58e-134">[**Process \_ V2 \_ TypeGroup2**](process-v2-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="ef58e-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="ef58e-135">事件種類值，33</span><span class="sxs-lookup"><span data-stu-id="ef58e-135">Event type value, 33</span></span>                                            | <span data-ttu-id="ef58e-136">會話開始時的效能計數器。</span><span class="sxs-lookup"><span data-stu-id="ef58e-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="ef58e-137">[**Process \_ V2 \_ TypeGroup2**](process-v2-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="ef58e-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="ef58e-138">事件種類值，39</span><span class="sxs-lookup"><span data-stu-id="ef58e-138">Event type value, 39</span></span>                                            | <span data-ttu-id="ef58e-139">無用的進程事件。</span><span class="sxs-lookup"><span data-stu-id="ef58e-139">Defunct process event.</span></span> <span data-ttu-id="ef58e-140">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="ef58e-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="ef58e-141">進程和執行緒啟動事件可能會記錄在父進程或執行緒的內容中。</span><span class="sxs-lookup"><span data-stu-id="ef58e-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="ef58e-142">因此，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員可能不會對應到正在建立的進程和執行緒。</span><span class="sxs-lookup"><span data-stu-id="ef58e-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="ef58e-143">這就是為什麼這些事件包含事件資料 (中的進程和執行緒識別碼，以及事件標頭) 中的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef58e-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef58e-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef58e-144">Requirements</span></span>



| <span data-ttu-id="ef58e-145">需求</span><span class="sxs-lookup"><span data-stu-id="ef58e-145">Requirement</span></span> | <span data-ttu-id="ef58e-146">值</span><span class="sxs-lookup"><span data-stu-id="ef58e-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="ef58e-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef58e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ef58e-148">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef58e-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="ef58e-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef58e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ef58e-150">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef58e-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef58e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef58e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef58e-152">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="ef58e-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="ef58e-153">**處理序**</span><span class="sxs-lookup"><span data-stu-id="ef58e-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="ef58e-154">**進程 \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="ef58e-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="ef58e-155">**進程 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="ef58e-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="ef58e-156">**進程 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="ef58e-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
