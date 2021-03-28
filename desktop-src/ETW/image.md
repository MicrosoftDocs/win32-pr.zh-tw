---
description: 這個類別是影像事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Image 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973308"
---
# <a name="image-class"></a><span data-ttu-id="efe30-104">Image 類別</span><span class="sxs-lookup"><span data-stu-id="efe30-104">Image class</span></span>

<span data-ttu-id="efe30-105">這個類別是影像事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="efe30-105">This class is the parent class for image events.</span></span>

<span data-ttu-id="efe30-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="efe30-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe30-107">語法</span><span class="sxs-lookup"><span data-stu-id="efe30-107">Syntax</span></span>

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="efe30-108">成員</span><span class="sxs-lookup"><span data-stu-id="efe30-108">Members</span></span>

<span data-ttu-id="efe30-109">**Image** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="efe30-109">The **Image** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="efe30-110">備註</span><span class="sxs-lookup"><span data-stu-id="efe30-110">Remarks</span></span>

<span data-ttu-id="efe30-111">若要在 NT 核心記錄會話中啟用影像事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函式時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 影像 \_ 載入** 旗標。</span><span class="sxs-lookup"><span data-stu-id="efe30-111">To enable image events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_IMAGE\_LOAD** flag in the **EnableFlags** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="efe30-112">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**ImageLoadGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來為影像載入事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="efe30-112">Event trace consumers can implement special processing for image load events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ImageLoadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="efe30-113">使用下列事件種類來識別使用事件時的影像載入事件。</span><span class="sxs-lookup"><span data-stu-id="efe30-113">Use the following event types to identify image load events when consuming events.</span></span>



| <span data-ttu-id="efe30-114">事件類型</span><span class="sxs-lookup"><span data-stu-id="efe30-114">Event type</span></span>                                                          | <span data-ttu-id="efe30-115">描述</span><span class="sxs-lookup"><span data-stu-id="efe30-115">Description</span></span>                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe30-116">**活動 \_追蹤 \_ 類型 \_ 載入** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="efe30-116">**EVENT\_TRACE\_TYPE\_LOAD**(Event type value is 10)</span></span><br/>     | <span data-ttu-id="efe30-117">映射載入事件。</span><span class="sxs-lookup"><span data-stu-id="efe30-117">Image load event.</span></span> <span data-ttu-id="efe30-118">當 DLL 或可執行檔載入時產生。</span><span class="sxs-lookup"><span data-stu-id="efe30-118">Generated when a DLL or executable file is loaded.</span></span> <span data-ttu-id="efe30-119">在第一次載入指定的 DLL 時，提供者只會產生一個事件。</span><span class="sxs-lookup"><span data-stu-id="efe30-119">The provider generates only one event for the first time a given DLL is loaded.</span></span> <span data-ttu-id="efe30-120">[**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="efe30-120">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="efe30-121">**活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) </span><span class="sxs-lookup"><span data-stu-id="efe30-121">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>       | <span data-ttu-id="efe30-122">影像卸載事件。</span><span class="sxs-lookup"><span data-stu-id="efe30-122">Image unload event.</span></span> <span data-ttu-id="efe30-123">當 DLL 或可執行檔卸載時產生。</span><span class="sxs-lookup"><span data-stu-id="efe30-123">Generated when a DLL or executable file is unloaded.</span></span> <span data-ttu-id="efe30-124">在最後一次卸載指定的 DLL 時，提供者只會產生一個事件。</span><span class="sxs-lookup"><span data-stu-id="efe30-124">The provider generates only one event for the last time a given DLL is unloaded.</span></span> <span data-ttu-id="efe30-125">[**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="efe30-125">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="efe30-126">**活動 \_追蹤 \_ 類型 \_ DC \_ 開始** (事件種類值為 3) </span><span class="sxs-lookup"><span data-stu-id="efe30-126">**EVENT\_TRACE\_TYPE\_DC\_START**(Event type value is 3)</span></span><br/> | <span data-ttu-id="efe30-127">資料收集開始事件。</span><span class="sxs-lookup"><span data-stu-id="efe30-127">Data collection start event.</span></span> <span data-ttu-id="efe30-128">列舉追蹤開頭的所有載入的影像。</span><span class="sxs-lookup"><span data-stu-id="efe30-128">Enumerates all loaded images at the beginning of the trace.</span></span> <span data-ttu-id="efe30-129">[**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="efe30-129">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="efe30-130">**活動 \_追蹤 \_ 類型 \_ DC \_ END** (事件種類值為 4) </span><span class="sxs-lookup"><span data-stu-id="efe30-130">**EVENT\_TRACE\_TYPE\_DC\_END**(Event type value is 4)</span></span><br/>   | <span data-ttu-id="efe30-131">資料收集結束事件。</span><span class="sxs-lookup"><span data-stu-id="efe30-131">Data collection end event.</span></span> <span data-ttu-id="efe30-132">列舉追蹤結尾的所有載入的影像。</span><span class="sxs-lookup"><span data-stu-id="efe30-132">Enumerates all loaded images at the end of the trace.</span></span> <span data-ttu-id="efe30-133">[**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="efe30-133">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="efe30-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="efe30-134">Requirements</span></span>



| <span data-ttu-id="efe30-135">需求</span><span class="sxs-lookup"><span data-stu-id="efe30-135">Requirement</span></span> | <span data-ttu-id="efe30-136">值</span><span class="sxs-lookup"><span data-stu-id="efe30-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efe30-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="efe30-137">Minimum supported client</span></span><br/> | <span data-ttu-id="efe30-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efe30-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="efe30-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="efe30-139">Minimum supported server</span></span><br/> | <span data-ttu-id="efe30-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efe30-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efe30-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="efe30-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe30-142">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="efe30-142">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="efe30-143">**映射 \_ 載入**</span><span class="sxs-lookup"><span data-stu-id="efe30-143">**Image\_Load**</span></span>](image-load.md)
</dt> <dt>

[<span data-ttu-id="efe30-144">**影像 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="efe30-144">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="efe30-145">**映射 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="efe30-145">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 
