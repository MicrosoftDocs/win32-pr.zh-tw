---
description: Process 類別-這個類別是處理事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Process 類別
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
ms.openlocfilehash: 8085bae0d00ebe830efff420744f6b7e9b4bf23c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106266"
---
# <a name="process-class"></a><span data-ttu-id="4c4df-104">Process 類別</span><span class="sxs-lookup"><span data-stu-id="4c4df-104">Process class</span></span>

<span data-ttu-id="4c4df-105">這個類別是處理事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="4c4df-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="4c4df-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="4c4df-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4df-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c4df-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="4c4df-108">成員</span><span class="sxs-lookup"><span data-stu-id="4c4df-108">Members</span></span>

<span data-ttu-id="4c4df-109">**Process** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="4c4df-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4df-110">備註</span><span class="sxs-lookup"><span data-stu-id="4c4df-110">Remarks</span></span>

<span data-ttu-id="4c4df-111">若要在 NT 核心記錄會話中啟用處理事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 處理** 旗標。</span><span class="sxs-lookup"><span data-stu-id="4c4df-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="4c4df-112">您也可以指定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="4c4df-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="4c4df-113">**事件 \_ 追蹤 \_ 旗標 \_ 進程 \_ 計數器**</span><span class="sxs-lookup"><span data-stu-id="4c4df-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="4c4df-114">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**ProcessGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來為進程事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="4c4df-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="4c4df-115">使用下列事件種類來識別使用事件時的實際處理事件。</span><span class="sxs-lookup"><span data-stu-id="4c4df-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="4c4df-116">事件類型</span><span class="sxs-lookup"><span data-stu-id="4c4df-116">Event type</span></span>                                                      | <span data-ttu-id="4c4df-117">描述</span><span class="sxs-lookup"><span data-stu-id="4c4df-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4df-118">**活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) </span><span class="sxs-lookup"><span data-stu-id="4c4df-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="4c4df-119">結束進程事件。</span><span class="sxs-lookup"><span data-stu-id="4c4df-119">End process event.</span></span> <span data-ttu-id="4c4df-120">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="4c4df-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="4c4df-121">**活動 \_追蹤 \_ 類型 \_ 開始** (事件種類值為 1) </span><span class="sxs-lookup"><span data-stu-id="4c4df-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="4c4df-122">開始處理事件。</span><span class="sxs-lookup"><span data-stu-id="4c4df-122">Start process event.</span></span> <span data-ttu-id="4c4df-123">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="4c4df-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="4c4df-124">事件種類值、3</span><span class="sxs-lookup"><span data-stu-id="4c4df-124">Event type value, 3</span></span>                                             | <span data-ttu-id="4c4df-125">開始資料收集處理事件。</span><span class="sxs-lookup"><span data-stu-id="4c4df-125">Start data collection process event.</span></span> <span data-ttu-id="4c4df-126">列舉核心會話開始時正在執行的進程。</span><span class="sxs-lookup"><span data-stu-id="4c4df-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="4c4df-127">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="4c4df-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="4c4df-128">事件種類值，4</span><span class="sxs-lookup"><span data-stu-id="4c4df-128">Event type value, 4</span></span>                                             | <span data-ttu-id="4c4df-129">結束資料收集處理事件。</span><span class="sxs-lookup"><span data-stu-id="4c4df-129">End data collection process event.</span></span> <span data-ttu-id="4c4df-130">列舉核心會話結束時目前正在執行的進程。</span><span class="sxs-lookup"><span data-stu-id="4c4df-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="4c4df-131">[**Process \_ TypeGroup1**](process-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="4c4df-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="4c4df-132">進程和執行緒啟動事件可能會記錄在父進程或執行緒的內容中。</span><span class="sxs-lookup"><span data-stu-id="4c4df-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="4c4df-133">因此，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員可能不會對應到正在建立的進程和執行緒。</span><span class="sxs-lookup"><span data-stu-id="4c4df-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="4c4df-134">這就是為什麼這些事件包含事件資料 (中的進程和執行緒識別碼，以及事件標頭) 中的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c4df-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4df-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c4df-135">Requirements</span></span>



| <span data-ttu-id="4c4df-136">需求</span><span class="sxs-lookup"><span data-stu-id="4c4df-136">Requirement</span></span> | <span data-ttu-id="4c4df-137">值</span><span class="sxs-lookup"><span data-stu-id="4c4df-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="4c4df-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c4df-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4df-139">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c4df-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="4c4df-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c4df-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4df-141">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c4df-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c4df-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c4df-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4df-143">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="4c4df-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="4c4df-144">**進程 \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="4c4df-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="4c4df-145">**進程 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="4c4df-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="4c4df-146">**進程 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="4c4df-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="4c4df-147">**進程 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="4c4df-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
