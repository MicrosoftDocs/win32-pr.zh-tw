---
description: 這個類別是登錄事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7ad92377-3fd7-47e0-b96e-bab530ea9d99
title: Registry_V1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1
api_type:
- NA
api_location: ''
ms.openlocfilehash: 320a2bce9213228be4ff5c1880d884ee9622b68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972277"
---
# <a name="registry_v1-class"></a><span data-ttu-id="67cbb-104">登錄 \_ V1 類別</span><span class="sxs-lookup"><span data-stu-id="67cbb-104">Registry\_V1 class</span></span>

<span data-ttu-id="67cbb-105">這個類別是登錄事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="67cbb-105">This class is the parent class for registry events.</span></span>

<span data-ttu-id="67cbb-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="67cbb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="67cbb-107">語法</span><span class="sxs-lookup"><span data-stu-id="67cbb-107">Syntax</span></span>

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="67cbb-108">成員</span><span class="sxs-lookup"><span data-stu-id="67cbb-108">Members</span></span>

<span data-ttu-id="67cbb-109">登錄 **\_ V1** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="67cbb-109">The **Registry\_V1** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="67cbb-110">備註</span><span class="sxs-lookup"><span data-stu-id="67cbb-110">Remarks</span></span>

<span data-ttu-id="67cbb-111">若要在 NT 核心記錄會話中啟用登錄事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗 \_** 標登錄。</span><span class="sxs-lookup"><span data-stu-id="67cbb-111">To enable registry events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_REGISTRY** in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="67cbb-112">事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 **RegistryGuid** 指定為 *pGuid* 參數，以執行登錄事件的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="67cbb-112">Event trace consumers can implement special processing for registry events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying **RegistryGuid** as the *pGuid* parameter.</span></span> <span data-ttu-id="67cbb-113">使用事件時，請使用下列事件種類來識別實際的登錄事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-113">Use the following event types to identify the actual registry event when consuming events.</span></span>



| <span data-ttu-id="67cbb-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="67cbb-114">Event type</span></span>                                                                       | <span data-ttu-id="67cbb-115">描述</span><span class="sxs-lookup"><span data-stu-id="67cbb-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67cbb-116">**活動 \_追蹤 \_ 類型 \_ REGCREATE** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="67cbb-116">**EVENT\_TRACE\_TYPE\_REGCREATE**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="67cbb-117">建立索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-117">Create key event.</span></span> <span data-ttu-id="67cbb-118">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-118">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="67cbb-119">**活動 \_追蹤 \_ 類型 \_ REGDELETE** (事件種類值為 12) </span><span class="sxs-lookup"><span data-stu-id="67cbb-119">**EVENT\_TRACE\_TYPE\_REGDELETE**(Event type value is 12)</span></span><br/>             | <span data-ttu-id="67cbb-120">刪除索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-120">Delete key event.</span></span> <span data-ttu-id="67cbb-121">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-121">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="67cbb-122">**活動 \_追蹤 \_ 類型 \_ REGDELETEVALUE** (事件種類值為 15) </span><span class="sxs-lookup"><span data-stu-id="67cbb-122">**EVENT\_TRACE\_TYPE\_REGDELETEVALUE**(Event type value is 15)</span></span><br/>        | <span data-ttu-id="67cbb-123">刪除值事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-123">Delete value event.</span></span> <span data-ttu-id="67cbb-124">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-124">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="67cbb-125">**活動 \_追蹤 \_ 類型 \_ REGENUMERATEKEY** (事件種類值為 17) </span><span class="sxs-lookup"><span data-stu-id="67cbb-125">**EVENT\_TRACE\_TYPE\_REGENUMERATEKEY**(Event type value is 17)</span></span><br/>       | <span data-ttu-id="67cbb-126">列舉索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-126">Enumerate key event.</span></span> <span data-ttu-id="67cbb-127">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-127">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="67cbb-128">**活動 \_追蹤 \_ 類型 \_ REGENUMERATEVALUEKEY** (事件種類值為 18) </span><span class="sxs-lookup"><span data-stu-id="67cbb-128">**EVENT\_TRACE\_TYPE\_REGENUMERATEVALUEKEY**(Event type value is 18)</span></span><br/>  | <span data-ttu-id="67cbb-129">列舉值索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-129">Enumerate value key event.</span></span> <span data-ttu-id="67cbb-130">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-130">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="67cbb-131">**活動 \_追蹤 \_ 類型 \_ REGFLUSH** (事件種類值為 21) </span><span class="sxs-lookup"><span data-stu-id="67cbb-131">**EVENT\_TRACE\_TYPE\_REGFLUSH**(Event type value is 21)</span></span><br/>              | <span data-ttu-id="67cbb-132">清除索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-132">Flush key event.</span></span> <span data-ttu-id="67cbb-133">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-133">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="67cbb-134">**活動 \_追蹤 \_ 類型 \_ REGKCBDMP** (事件種類值為 22) </span><span class="sxs-lookup"><span data-stu-id="67cbb-134">**EVENT\_TRACE\_TYPE\_REGKCBDMP**(Event type value is 22)</span></span><br/>             | <span data-ttu-id="67cbb-135">當登錄作業使用控制碼而非字串來參考子機碼時產生。</span><span class="sxs-lookup"><span data-stu-id="67cbb-135">Generated when a registry operation uses handles rather than strings to reference subkeys.</span></span> <span data-ttu-id="67cbb-136">每個控制碼都會記錄這些事件一次，第一次是參考控制碼。</span><span class="sxs-lookup"><span data-stu-id="67cbb-136">These events are recorded once for each handle—the first time the handle is referenced.</span></span> <span data-ttu-id="67cbb-137">控制碼的重複參考不會產生多個事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-137">Repeated references to the handle do not generate multiple events.</span></span><br/> <span data-ttu-id="67cbb-138">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-138">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span><br/> <span data-ttu-id="67cbb-139">**Windows 2000：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="67cbb-139">**Windows 2000:** This value is not supported.</span></span><br/> |
| <span data-ttu-id="67cbb-140">**活動 \_追蹤 \_ 類型 \_ REGOPEN** (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="67cbb-140">**EVENT\_TRACE\_TYPE\_REGOPEN**(Event type value is 11)</span></span><br/>               | <span data-ttu-id="67cbb-141">開啟金鑰事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-141">Open key event.</span></span> <span data-ttu-id="67cbb-142">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-142">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="67cbb-143">**活動 \_追蹤 \_ 類型 \_ REGQUERY** (事件種類值為 13) </span><span class="sxs-lookup"><span data-stu-id="67cbb-143">**EVENT\_TRACE\_TYPE\_REGQUERY**(Event type value is 13)</span></span><br/>              | <span data-ttu-id="67cbb-144">查詢索引鍵事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-144">Query key event.</span></span> <span data-ttu-id="67cbb-145">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-145">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="67cbb-146">**活動 \_追蹤 \_ 類型 \_ REGQUERYMULTIPLEVALUE** (事件種類值為 19) </span><span class="sxs-lookup"><span data-stu-id="67cbb-146">**EVENT\_TRACE\_TYPE\_REGQUERYMULTIPLEVALUE**(Event type value is 19)</span></span><br/> | <span data-ttu-id="67cbb-147">查詢多個值事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-147">Query multiple value event.</span></span> <span data-ttu-id="67cbb-148">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-148">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="67cbb-149">**活動 \_追蹤 \_ 類型 \_ REGQUERYVALUE** (事件種類值為 16) </span><span class="sxs-lookup"><span data-stu-id="67cbb-149">**EVENT\_TRACE\_TYPE\_REGQUERYVALUE**(Event type value is 16)</span></span><br/>         | <span data-ttu-id="67cbb-150">查詢值事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-150">Query value event.</span></span> <span data-ttu-id="67cbb-151">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-151">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="67cbb-152">**活動 \_追蹤 \_ 類型 \_ REGSETINFORMATION** (事件種類值為 20) </span><span class="sxs-lookup"><span data-stu-id="67cbb-152">**EVENT\_TRACE\_TYPE\_REGSETINFORMATION**(Event type value is 20)</span></span><br/>     | <span data-ttu-id="67cbb-153">設定資訊事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-153">Set information event.</span></span> <span data-ttu-id="67cbb-154">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-154">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="67cbb-155">**活動 \_追蹤 \_ 類型 \_ REGSETVALUE** (事件種類值為 14) </span><span class="sxs-lookup"><span data-stu-id="67cbb-155">**EVENT\_TRACE\_TYPE\_REGSETVALUE**(Event type value is 14)</span></span><br/>           | <span data-ttu-id="67cbb-156">設定值事件。</span><span class="sxs-lookup"><span data-stu-id="67cbb-156">Set value event.</span></span> <span data-ttu-id="67cbb-157">[**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="67cbb-157">The [**Registry\_TypeGroup1**](registry-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="67cbb-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="67cbb-158">Requirements</span></span>



| <span data-ttu-id="67cbb-159">需求</span><span class="sxs-lookup"><span data-stu-id="67cbb-159">Requirement</span></span> | <span data-ttu-id="67cbb-160">值</span><span class="sxs-lookup"><span data-stu-id="67cbb-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67cbb-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67cbb-161">Minimum supported client</span></span><br/> | <span data-ttu-id="67cbb-162">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67cbb-162">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="67cbb-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67cbb-163">Minimum supported server</span></span><br/> | <span data-ttu-id="67cbb-164">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67cbb-164">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67cbb-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67cbb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cbb-166">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="67cbb-166">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="67cbb-167">**登錄**</span><span class="sxs-lookup"><span data-stu-id="67cbb-167">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="67cbb-168">**登錄 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="67cbb-168">**Registry\_V0**</span></span>](registry-v0.md)
</dt> <dt>

[<span data-ttu-id="67cbb-169">**登錄 \_ V1 \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="67cbb-169">**Registry\_V1\_TypeGroup1**</span></span>](registry-v1-typegroup1.md)
</dt> </dl>

 

 
