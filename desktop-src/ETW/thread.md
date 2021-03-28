---
description: 這個類別是執行緒事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: c4af87462607b675e46b3459a811925fbefe3ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195605"
---
# <a name="thread-class"></a><span data-ttu-id="53c9b-104">Thread 類別</span><span class="sxs-lookup"><span data-stu-id="53c9b-104">Thread class</span></span>

<span data-ttu-id="53c9b-105">這個類別是執行緒事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="53c9b-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="53c9b-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="53c9b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c9b-107">語法</span><span class="sxs-lookup"><span data-stu-id="53c9b-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="53c9b-108">成員</span><span class="sxs-lookup"><span data-stu-id="53c9b-108">Members</span></span>

<span data-ttu-id="53c9b-109">**Thread** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="53c9b-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c9b-110">備註</span><span class="sxs-lookup"><span data-stu-id="53c9b-110">Remarks</span></span>

<span data-ttu-id="53c9b-111">若要在 NT 核心記錄會話中啟用執行緒事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 執行緒** 旗標。</span><span class="sxs-lookup"><span data-stu-id="53c9b-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="53c9b-112">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**ThreadGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對執行緒事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="53c9b-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="53c9b-113">使用下列事件種類來識別使用事件時的實際執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="53c9b-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="53c9b-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="53c9b-114">Event type</span></span>                                                      | <span data-ttu-id="53c9b-115">描述</span><span class="sxs-lookup"><span data-stu-id="53c9b-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c9b-116">**活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) </span><span class="sxs-lookup"><span data-stu-id="53c9b-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="53c9b-117">結束執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="53c9b-117">End thread event.</span></span> <span data-ttu-id="53c9b-118">[**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="53c9b-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="53c9b-119">**活動 \_追蹤 \_ 類型 \_ 開始** (事件種類值為 1) </span><span class="sxs-lookup"><span data-stu-id="53c9b-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="53c9b-120">啟動執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="53c9b-120">Start thread event.</span></span> <span data-ttu-id="53c9b-121">[**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="53c9b-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="53c9b-122">事件種類值、3</span><span class="sxs-lookup"><span data-stu-id="53c9b-122">Event type value, 3</span></span>                                             | <span data-ttu-id="53c9b-123">開始資料收集執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="53c9b-123">Start data collection thread event.</span></span> <span data-ttu-id="53c9b-124">列舉核心會話開始時正在執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="53c9b-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="53c9b-125">[**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="53c9b-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="53c9b-126">事件種類值，4</span><span class="sxs-lookup"><span data-stu-id="53c9b-126">Event type value, 4</span></span>                                             | <span data-ttu-id="53c9b-127">結束資料收集執行緒事件。</span><span class="sxs-lookup"><span data-stu-id="53c9b-127">End data collection thread event.</span></span> <span data-ttu-id="53c9b-128">列舉核心會話結束時目前正在執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="53c9b-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="53c9b-129">[**Thread \_ TypeGroup1**](thread-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="53c9b-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="53c9b-130">進程和執行緒啟動事件可能會記錄在父進程或執行緒的內容中。</span><span class="sxs-lookup"><span data-stu-id="53c9b-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="53c9b-131">因此，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的 **ProcessId** 和 **ThreadId** 成員可能不會對應到正在建立的進程和執行緒。</span><span class="sxs-lookup"><span data-stu-id="53c9b-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="53c9b-132">這就是為什麼這些事件包含事件資料 (中的進程和執行緒識別碼，以及事件標頭) 中的識別碼。</span><span class="sxs-lookup"><span data-stu-id="53c9b-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="53c9b-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="53c9b-133">Requirements</span></span>



| <span data-ttu-id="53c9b-134">需求</span><span class="sxs-lookup"><span data-stu-id="53c9b-134">Requirement</span></span> | <span data-ttu-id="53c9b-135">值</span><span class="sxs-lookup"><span data-stu-id="53c9b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53c9b-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53c9b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="53c9b-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53c9b-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53c9b-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53c9b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="53c9b-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53c9b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53c9b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53c9b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c9b-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="53c9b-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="53c9b-142">**執行緒 \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="53c9b-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="53c9b-143">**執行緒 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="53c9b-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="53c9b-144">**執行緒 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="53c9b-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="53c9b-145">**執行緒 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="53c9b-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
