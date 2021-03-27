---
description: 這個類別是效能計數器事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: PerfInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972225"
---
# <a name="perfinfo-class"></a><span data-ttu-id="35ee8-104">PerfInfo 類別</span><span class="sxs-lookup"><span data-stu-id="35ee8-104">PerfInfo class</span></span>

<span data-ttu-id="35ee8-105">這個類別是效能計數器事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="35ee8-105">This class is the parent class for performance counter events.</span></span>

<span data-ttu-id="35ee8-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="35ee8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ee8-107">語法</span><span class="sxs-lookup"><span data-stu-id="35ee8-107">Syntax</span></span>

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="35ee8-108">成員</span><span class="sxs-lookup"><span data-stu-id="35ee8-108">Members</span></span>

<span data-ttu-id="35ee8-109">**PerfInfo** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="35ee8-109">The **PerfInfo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ee8-110">備註</span><span class="sxs-lookup"><span data-stu-id="35ee8-110">Remarks</span></span>

<span data-ttu-id="35ee8-111">若要在 NT 核心記錄會話中啟用延遲程序呼叫 (DPC) 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函式時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ DPC** 旗標。</span><span class="sxs-lookup"><span data-stu-id="35ee8-111">To enable deferred procedure call (DPC) events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="35ee8-112">您也可以指定下列一或多個旗標：</span><span class="sxs-lookup"><span data-stu-id="35ee8-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="35ee8-113">**事件 \_ 追蹤 \_ 旗標 \_ 中斷**</span><span class="sxs-lookup"><span data-stu-id="35ee8-113">**EVENT\_TRACE\_FLAG\_INTERRUPT**</span></span>
-   <span data-ttu-id="35ee8-114">**事件 \_ 追蹤 \_ 旗標 \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="35ee8-114">**EVENT\_TRACE\_FLAG\_PROFILE**</span></span>
-   <span data-ttu-id="35ee8-115">**事件 \_ 追蹤 \_ 旗標 \_ SYSTEMCALL**</span><span class="sxs-lookup"><span data-stu-id="35ee8-115">**EVENT\_TRACE\_FLAG\_SYSTEMCALL**</span></span>

<span data-ttu-id="35ee8-116">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**PerfInfoGuid**](nt-kernel-logger-constants.md) 指定為 *PGUID* 參數，來執行 DPC 事件的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="35ee8-116">Event trace consumers can implement special processing for DPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PerfInfoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="35ee8-117">使用下列事件種類來識別使用事件時的實際事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-117">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="35ee8-118">事件類型</span><span class="sxs-lookup"><span data-stu-id="35ee8-118">Event type</span></span>           | <span data-ttu-id="35ee8-119">描述</span><span class="sxs-lookup"><span data-stu-id="35ee8-119">Description</span></span>                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ee8-120">事件種類值，46</span><span class="sxs-lookup"><span data-stu-id="35ee8-120">Event type value, 46</span></span> | <span data-ttu-id="35ee8-121">取樣設定檔事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-121">Sampled profile event.</span></span> <span data-ttu-id="35ee8-122">[**SampledProfile**](sampledprofile.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="35ee8-122">The [**SampledProfile**](sampledprofile.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="35ee8-123">事件種類值，51</span><span class="sxs-lookup"><span data-stu-id="35ee8-123">Event type value, 51</span></span> | <span data-ttu-id="35ee8-124">系統呼叫進入事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-124">System call enter event.</span></span> <span data-ttu-id="35ee8-125">[**SysCallEnter**](syscallenter.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="35ee8-125">The [**SysCallEnter**](syscallenter.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="35ee8-126">事件種類值，52</span><span class="sxs-lookup"><span data-stu-id="35ee8-126">Event type value, 52</span></span> | <span data-ttu-id="35ee8-127">系統呼叫離開事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-127">System call exit event.</span></span> <span data-ttu-id="35ee8-128">[**SysCallExit**](syscallexit.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="35ee8-128">The [**SysCallExit**](syscallexit.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="35ee8-129">事件種類值，66</span><span class="sxs-lookup"><span data-stu-id="35ee8-129">Event type value, 66</span></span> | <span data-ttu-id="35ee8-130">執行緒 DPC 事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-130">Threaded DPC event.</span></span> <span data-ttu-id="35ee8-131">[**DPC**](dpc.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="35ee8-131">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                          |
| <span data-ttu-id="35ee8-132">事件種類值，67</span><span class="sxs-lookup"><span data-stu-id="35ee8-132">Event type value, 67</span></span> | <span data-ttu-id="35ee8-133">插斷服務常式 (ISR) 事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-133">Interrupt service routine (ISR) event.</span></span> <span data-ttu-id="35ee8-134">[**ISR**](isr.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="35ee8-134">The [**ISR**](isr.md) MOF class defines the event data for this event.</span></span>       |
| <span data-ttu-id="35ee8-135">事件種類值，68</span><span class="sxs-lookup"><span data-stu-id="35ee8-135">Event type value, 68</span></span> | <span data-ttu-id="35ee8-136">DPC 事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-136">DPC event.</span></span> <span data-ttu-id="35ee8-137">[**DPC**](dpc.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="35ee8-137">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="35ee8-138">事件種類值，69</span><span class="sxs-lookup"><span data-stu-id="35ee8-138">Event type value, 69</span></span> | <span data-ttu-id="35ee8-139">DPC 計時器事件。</span><span class="sxs-lookup"><span data-stu-id="35ee8-139">DPC timer event.</span></span> <span data-ttu-id="35ee8-140">[**DPC**](dpc.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="35ee8-140">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="35ee8-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="35ee8-141">Requirements</span></span>



| <span data-ttu-id="35ee8-142">需求</span><span class="sxs-lookup"><span data-stu-id="35ee8-142">Requirement</span></span> | <span data-ttu-id="35ee8-143">值</span><span class="sxs-lookup"><span data-stu-id="35ee8-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35ee8-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35ee8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="35ee8-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35ee8-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35ee8-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35ee8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="35ee8-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35ee8-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
