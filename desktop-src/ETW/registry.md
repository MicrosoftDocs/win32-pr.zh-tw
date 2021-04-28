---
description: Registry 類別-這個類別是登錄事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 362d7653-1ba0-45b7-80f3-0fccca0badf1
title: Registry 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23cd59e8d6afeb7578bd65625741caaae8156066
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106126"
---
# <a name="registry-class"></a><span data-ttu-id="55b14-104">Registry 類別</span><span class="sxs-lookup"><span data-stu-id="55b14-104">Registry class</span></span>

<span data-ttu-id="55b14-105">這個類別是登錄事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="55b14-105">This class is the parent class for registry events.</span></span>

<span data-ttu-id="55b14-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="55b14-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b14-107">語法</span><span class="sxs-lookup"><span data-stu-id="55b14-107">Syntax</span></span>

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="55b14-108">成員</span><span class="sxs-lookup"><span data-stu-id="55b14-108">Members</span></span>

<span data-ttu-id="55b14-109">登錄 **類別未** 定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="55b14-109">The **Registry** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b14-110">備註</span><span class="sxs-lookup"><span data-stu-id="55b14-110">Remarks</span></span>

<span data-ttu-id="55b14-111">若要在 NT 核心記錄會話中啟用登錄事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗 \_** 標登錄。</span><span class="sxs-lookup"><span data-stu-id="55b14-111">To enable registry events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_REGISTRY** in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="55b14-112">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**RegistryGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以執行登錄事件的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="55b14-112">Event trace consumers can implement special processing for registry events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**RegistryGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="55b14-113">使用事件時，請使用下列事件種類來識別實際的登錄事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-113">Use the following event types to identify the actual registry event when consuming events.</span></span>



| <span data-ttu-id="55b14-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="55b14-114">Event type</span></span>                                                                       | <span data-ttu-id="55b14-115">描述</span><span class="sxs-lookup"><span data-stu-id="55b14-115">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b14-116">**活動 \_追蹤 \_ 類型 \_ REGCREATE** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="55b14-116">**EVENT\_TRACE\_TYPE\_REGCREATE**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="55b14-117">建立索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-117">Create key event.</span></span> <span data-ttu-id="55b14-118">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-118">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="55b14-119">**活動 \_追蹤 \_ 類型 \_ REGDELETE** (事件種類值為 12) </span><span class="sxs-lookup"><span data-stu-id="55b14-119">**EVENT\_TRACE\_TYPE\_REGDELETE**(Event type value is 12)</span></span><br/>             | <span data-ttu-id="55b14-120">刪除索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-120">Delete key event.</span></span> <span data-ttu-id="55b14-121">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-121">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="55b14-122">**活動 \_追蹤 \_ 類型 \_ REGDELETEVALUE** (事件種類值為 15) </span><span class="sxs-lookup"><span data-stu-id="55b14-122">**EVENT\_TRACE\_TYPE\_REGDELETEVALUE**(Event type value is 15)</span></span><br/>        | <span data-ttu-id="55b14-123">刪除值事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-123">Delete value event.</span></span> <span data-ttu-id="55b14-124">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-124">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="55b14-125">**活動 \_追蹤 \_ 類型 \_ REGENUMERATEKEY** (事件種類值為 17) </span><span class="sxs-lookup"><span data-stu-id="55b14-125">**EVENT\_TRACE\_TYPE\_REGENUMERATEKEY**(Event type value is 17)</span></span><br/>       | <span data-ttu-id="55b14-126">列舉索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-126">Enumerate key event.</span></span> <span data-ttu-id="55b14-127">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-127">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                         |
| <span data-ttu-id="55b14-128">**活動 \_追蹤 \_ 類型 \_ REGENUMERATEVALUEKEY** (事件種類值為 18) </span><span class="sxs-lookup"><span data-stu-id="55b14-128">**EVENT\_TRACE\_TYPE\_REGENUMERATEVALUEKEY**(Event type value is 18)</span></span><br/>  | <span data-ttu-id="55b14-129">列舉值索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-129">Enumerate value key event.</span></span> <span data-ttu-id="55b14-130">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-130">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                   |
| <span data-ttu-id="55b14-131">**活動 \_追蹤 \_ 類型 \_ REGFLUSH** (事件種類值為 21) </span><span class="sxs-lookup"><span data-stu-id="55b14-131">**EVENT\_TRACE\_TYPE\_REGFLUSH**(Event type value is 21)</span></span><br/>              | <span data-ttu-id="55b14-132">清除索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-132">Flush key event.</span></span> <span data-ttu-id="55b14-133">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-133">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                             |
| <span data-ttu-id="55b14-134">**活動 \_追蹤 \_ 類型 \_ REGKCBDMP** (事件種類值為 22) </span><span class="sxs-lookup"><span data-stu-id="55b14-134">**EVENT\_TRACE\_TYPE\_REGKCBDMP**(Event type value is 22)</span></span><br/>             | <span data-ttu-id="55b14-135">建立索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-135">Create key event.</span></span> <span data-ttu-id="55b14-136">當登錄作業使用控制碼而非字串來參考子機碼時產生。</span><span class="sxs-lookup"><span data-stu-id="55b14-136">Generated when a registry operation uses handles rather than strings to reference subkeys.</span></span> <span data-ttu-id="55b14-137">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-137">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="55b14-138">**活動 \_追蹤 \_ 類型 \_ REGOPEN** (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="55b14-138">**EVENT\_TRACE\_TYPE\_REGOPEN**(Event type value is 11)</span></span><br/>               | <span data-ttu-id="55b14-139">開啟金鑰事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-139">Open key event.</span></span> <span data-ttu-id="55b14-140">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-140">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                              |
| <span data-ttu-id="55b14-141">**活動 \_追蹤 \_ 類型 \_ REGQUERY** (事件種類值為 13) </span><span class="sxs-lookup"><span data-stu-id="55b14-141">**EVENT\_TRACE\_TYPE\_REGQUERY**(Event type value is 13)</span></span><br/>              | <span data-ttu-id="55b14-142">查詢索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-142">Query key event.</span></span> <span data-ttu-id="55b14-143">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-143">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                             |
| <span data-ttu-id="55b14-144">**活動 \_追蹤 \_ 類型 \_ REGQUERYMULTIPLEVALUE** (事件種類值為 19) </span><span class="sxs-lookup"><span data-stu-id="55b14-144">**EVENT\_TRACE\_TYPE\_REGQUERYMULTIPLEVALUE**(Event type value is 19)</span></span><br/> | <span data-ttu-id="55b14-145">查詢多個值事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-145">Query multiple value event.</span></span> <span data-ttu-id="55b14-146">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-146">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                  |
| <span data-ttu-id="55b14-147">**活動 \_追蹤 \_ 類型 \_ REGQUERYVALUE** (事件種類值為 16) </span><span class="sxs-lookup"><span data-stu-id="55b14-147">**EVENT\_TRACE\_TYPE\_REGQUERYVALUE**(Event type value is 16)</span></span><br/>         | <span data-ttu-id="55b14-148">查詢值事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-148">Query value event.</span></span> <span data-ttu-id="55b14-149">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-149">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                           |
| <span data-ttu-id="55b14-150">**活動 \_追蹤 \_ 類型 \_ REGSETINFORMATION** (事件種類值為 20) </span><span class="sxs-lookup"><span data-stu-id="55b14-150">**EVENT\_TRACE\_TYPE\_REGSETINFORMATION**(Event type value is 20)</span></span><br/>     | <span data-ttu-id="55b14-151">設定資訊事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-151">Set information event.</span></span> <span data-ttu-id="55b14-152">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-152">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                       |
| <span data-ttu-id="55b14-153">**活動 \_追蹤 \_ 類型 \_ REGSETVALUE** (事件種類值為 14) </span><span class="sxs-lookup"><span data-stu-id="55b14-153">**EVENT\_TRACE\_TYPE\_REGSETVALUE**(Event type value is 14)</span></span><br/>           | <span data-ttu-id="55b14-154">設定值事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-154">Set value event.</span></span> <span data-ttu-id="55b14-155">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-155">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                             |
| <span data-ttu-id="55b14-156">事件種類值，23</span><span class="sxs-lookup"><span data-stu-id="55b14-156">Event type value, 23</span></span>                                                             | <span data-ttu-id="55b14-157">刪除索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-157">delete key event.</span></span> <span data-ttu-id="55b14-158">當登錄作業使用控制碼而非字串來參考子機碼時產生。</span><span class="sxs-lookup"><span data-stu-id="55b14-158">Generated when a registry operation uses handles rather than strings to reference subkeys.</span></span> <span data-ttu-id="55b14-159">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-159">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="55b14-160">事件種類值，24</span><span class="sxs-lookup"><span data-stu-id="55b14-160">Event type value, 24</span></span>                                                             | <span data-ttu-id="55b14-161">列舉在會話開始時開啟的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="55b14-161">Enumerates the registry keys open at the beginning of the session.</span></span> <span data-ttu-id="55b14-162">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-162">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                           |
| <span data-ttu-id="55b14-163">事件種類值，25</span><span class="sxs-lookup"><span data-stu-id="55b14-163">Event type value, 25</span></span>                                                             | <span data-ttu-id="55b14-164">列舉在會話結束時開啟的登錄機碼。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-164">Enumerates the registry keys open at the end of the session.The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                  |
| <span data-ttu-id="55b14-165">事件種類值，26</span><span class="sxs-lookup"><span data-stu-id="55b14-165">Event type value, 26</span></span>                                                             | <span data-ttu-id="55b14-166">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-166">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                              |
| <span data-ttu-id="55b14-167">事件種類值，27</span><span class="sxs-lookup"><span data-stu-id="55b14-167">Event type value, 27</span></span>                                                             | <span data-ttu-id="55b14-168">開啟金鑰事件。</span><span class="sxs-lookup"><span data-stu-id="55b14-168">Open key event.</span></span> <span data-ttu-id="55b14-169">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="55b14-169">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="55b14-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="55b14-170">Requirements</span></span>



| <span data-ttu-id="55b14-171">需求</span><span class="sxs-lookup"><span data-stu-id="55b14-171">Requirement</span></span> | <span data-ttu-id="55b14-172">值</span><span class="sxs-lookup"><span data-stu-id="55b14-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55b14-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55b14-173">Minimum supported client</span></span><br/> | <span data-ttu-id="55b14-174">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55b14-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55b14-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55b14-175">Minimum supported server</span></span><br/> | <span data-ttu-id="55b14-176">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55b14-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55b14-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55b14-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b14-178">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="55b14-178">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="55b14-179">**登錄 \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="55b14-179">**Registry\_TypeGroup1**</span></span>](registry-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="55b14-180">**登錄 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="55b14-180">**Registry\_V0**</span></span>](registry-v0.md)
</dt> <dt>

[<span data-ttu-id="55b14-181">**登錄 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="55b14-181">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 
