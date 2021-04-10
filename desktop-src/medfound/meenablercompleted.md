---
description: 當物件啟用動作完成時，由內容啟用物件引發。
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: 'MEEnablerCompleted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114629"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="e2570-103">MEEnablerCompleted 事件</span><span class="sxs-lookup"><span data-stu-id="e2570-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="e2570-104">當物件的啟用動作完成時，由內容啟用物件引發。</span><span class="sxs-lookup"><span data-stu-id="e2570-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="e2570-105">公開 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面的物件可能會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="e2570-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="e2570-106">如果發生下列其中一種情況，就會引發事件：</span><span class="sxs-lookup"><span data-stu-id="e2570-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="e2570-107">[**IMFContentEnabler：： AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)方法會以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="e2570-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="e2570-108">應用程式會呼叫 [**IMFContentEnabler：： MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)，然後應用程式會完成 HTTP POST 要求，如 **MonitorEnable** 方法中所述。</span><span class="sxs-lookup"><span data-stu-id="e2570-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="e2570-109">事件值</span><span class="sxs-lookup"><span data-stu-id="e2570-109">Event values</span></span>

<span data-ttu-id="e2570-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="e2570-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e2570-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e2570-111">VARTYPE</span></span>              | <span data-ttu-id="e2570-112">Description</span><span class="sxs-lookup"><span data-stu-id="e2570-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e2570-113">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="e2570-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e2570-114">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="e2570-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e2570-115">備註</span><span class="sxs-lookup"><span data-stu-id="e2570-115">Remarks</span></span>

<span data-ttu-id="e2570-116">事件的狀態碼可能包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e2570-116">The status code from the event may contain one of the following values.</span></span>



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2570-117">**S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="e2570-117">**S\_OK**</span></span>                            | <span data-ttu-id="e2570-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e2570-118">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e2570-119">**NS \_ E \_ DRM \_ 授權 \_ NOTACQUIRED**</span><span class="sxs-lookup"><span data-stu-id="e2570-119">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="e2570-120">未取得 DRM 授權。</span><span class="sxs-lookup"><span data-stu-id="e2570-120">The DRM license was not acquired.</span></span> <span data-ttu-id="e2570-121">如果先前的嘗試使用 [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)，應用程式應該嘗試非無訊息的取得。</span><span class="sxs-lookup"><span data-stu-id="e2570-121">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="e2570-122">**NS \_ S \_ DRM \_ 監視器已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="e2570-122">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="e2570-123">[**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)操作已取消。</span><span class="sxs-lookup"><span data-stu-id="e2570-123">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="e2570-124">若要接收此事件，請查詢 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)介面的 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)介面。</span><span class="sxs-lookup"><span data-stu-id="e2570-124">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="e2570-125">然後呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)，如「 [媒體事件](media-event-generators.md)產生器」主題所述。</span><span class="sxs-lookup"><span data-stu-id="e2570-125">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2570-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2570-126">Requirements</span></span>



| <span data-ttu-id="e2570-127">需求</span><span class="sxs-lookup"><span data-stu-id="e2570-127">Requirement</span></span> | <span data-ttu-id="e2570-128">值</span><span class="sxs-lookup"><span data-stu-id="e2570-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2570-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2570-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e2570-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2570-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2570-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2570-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e2570-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2570-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2570-133">標頭</span><span class="sxs-lookup"><span data-stu-id="e2570-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2570-134"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="e2570-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2570-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2570-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2570-136">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="e2570-136">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="e2570-137">媒體事件產生器</span><span class="sxs-lookup"><span data-stu-id="e2570-137">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="e2570-138">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="e2570-138">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




