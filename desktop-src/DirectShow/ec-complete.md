---
description: 已轉譯特定資料流程中的所有資料。
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: 'EC_COMPLETE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987134"
---
# <a name="ec_complete"></a><span data-ttu-id="3a50d-103">EC \_ 完成</span><span class="sxs-lookup"><span data-stu-id="3a50d-103">EC\_COMPLETE</span></span>

<span data-ttu-id="3a50d-104">已轉譯特定資料流程中的所有資料。</span><span class="sxs-lookup"><span data-stu-id="3a50d-104">All data from a particular stream has been rendered.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a50d-105">參數</span><span class="sxs-lookup"><span data-stu-id="3a50d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a50d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3a50d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3a50d-107"> (**HRESULT**) 完成時的資料流程狀態。</span><span class="sxs-lookup"><span data-stu-id="3a50d-107">(**HRESULT**) Status of the stream on completion.</span></span> <span data-ttu-id="3a50d-108">如果播放期間未發生任何錯誤，則值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3a50d-108">If no errors occurred during playback, the value is S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="3a50d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3a50d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3a50d-110"> (**IUnknown** \*) 零或轉譯器的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面指標。</span><span class="sxs-lookup"><span data-stu-id="3a50d-110">(**IUnknown**\*) Zero, or a pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="3a50d-111">預設動作</span><span class="sxs-lookup"><span data-stu-id="3a50d-111">Default Action</span></span>

<span data-ttu-id="3a50d-112">篩選圖形管理員預設不會將此事件轉寄至應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a50d-112">By default, the filter graph manager does not forward this event to the application.</span></span> <span data-ttu-id="3a50d-113">不過，在圖形報表中的所有串流都 **\_ 完成** 後，篩選圖形管理員會將不同的 **EC \_ 完成** 事件張貼至應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a50d-113">However, after all the streams in the graph report **EC\_COMPLETE**, the filter graph manager posts a separate **EC\_COMPLETE** event to the application.</span></span>

<span data-ttu-id="3a50d-114">如果此事件的預設動作已停用，則應用程式會從轉譯器接收所有的 **EC \_ 完成** 事件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-114">If the default action is disabled for this event, the application receives all of the **EC\_COMPLETE** events from the renderers.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a50d-115">備註</span><span class="sxs-lookup"><span data-stu-id="3a50d-115">Remarks</span></span>

<span data-ttu-id="3a50d-116">轉譯器篩選器會在收到資料流程結尾通知時傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-116">A renderer filter sends this event when it receives an end-of-stream notice.</span></span> <span data-ttu-id="3a50d-117"> (結束資料流程會透過 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法發出信號。 ) 篩選器會為每個資料流程只傳送一個 **EC \_ 完成** 事件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-117">(End-of-stream is signaled through the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.) The filter sends exactly one **EC\_COMPLETE** event for each stream.</span></span> <span data-ttu-id="3a50d-118">篩選準則必須先處理任何擱置中的範例，才能傳送事件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-118">The filter must process any pending samples before it sends the event.</span></span> <span data-ttu-id="3a50d-119">停止轉譯器會重設已快取的任何資料流程結束狀態。</span><span class="sxs-lookup"><span data-stu-id="3a50d-119">Stopping a renderer resets any end-of-stream state that was cached.</span></span>

<span data-ttu-id="3a50d-120">如果已暫停轉譯器，則在呼叫 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)方法之前，不會將 **EC \_ 完成** 傳送。</span><span class="sxs-lookup"><span data-stu-id="3a50d-120">If the renderer is paused, it does not send **EC\_COMPLETE** until the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method is called.</span></span> <span data-ttu-id="3a50d-121">此外，它會繼續為每個轉換從 pause 傳送的 **EC \_ 完成** 事件傳送到執行，直到篩選器停止或清除為止。</span><span class="sxs-lookup"><span data-stu-id="3a50d-121">Furthermore, it continues to send **EC\_COMPLETE** events for each transition from pause to run, until the filter is either stopped or flushed.</span></span>

<span data-ttu-id="3a50d-122">篩選準則會將 *lParam2* 參數設定為 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 指標。</span><span class="sxs-lookup"><span data-stu-id="3a50d-122">Filters set the *lParam2* parameter to an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="3a50d-123">如果預設動作已啟用，則篩選圖形管理員會將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="3a50d-123">If the default action is enabled, the filter graph manager sets this parameter to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a50d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a50d-124">Requirements</span></span>



| <span data-ttu-id="3a50d-125">需求</span><span class="sxs-lookup"><span data-stu-id="3a50d-125">Requirement</span></span> | <span data-ttu-id="3a50d-126">值</span><span class="sxs-lookup"><span data-stu-id="3a50d-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a50d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3a50d-127">Header</span></span><br/> | <dl> <span data-ttu-id="3a50d-128"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a50d-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a50d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a50d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a50d-130">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="3a50d-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3a50d-131">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="3a50d-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="3a50d-132">替代影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="3a50d-132">Alternative Video Renderers</span></span>](alternative-video-renderers.md)
</dt> </dl>

 

 




