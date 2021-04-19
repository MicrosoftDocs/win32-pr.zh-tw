---
description: 影片轉譯器需要重新繪製。
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: 'EC_REPAINT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982064"
---
# <a name="ec_repaint"></a><span data-ttu-id="25fc0-103">EC 重新 \_ 繪製</span><span class="sxs-lookup"><span data-stu-id="25fc0-103">EC\_REPAINT</span></span>

<span data-ttu-id="25fc0-104">影片轉譯器需要重新繪製。</span><span class="sxs-lookup"><span data-stu-id="25fc0-104">A video renderer requires a repaint.</span></span>

## <a name="parameters"></a><span data-ttu-id="25fc0-105">參數</span><span class="sxs-lookup"><span data-stu-id="25fc0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fc0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="25fc0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="25fc0-107"> (**IUnknown** \*) 指標指向影片轉譯器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="25fc0-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the video renderer's input pin, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25fc0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="25fc0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="25fc0-109">零個。</span><span class="sxs-lookup"><span data-stu-id="25fc0-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="25fc0-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="25fc0-110">Default Action</span></span>

<span data-ttu-id="25fc0-111">*LParam1* 參數可能會指定影片轉譯器的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="25fc0-111">The *lParam1* parameter might specify the video renderer's input pin.</span></span> <span data-ttu-id="25fc0-112">如果是這樣，則篩選圖形管理員會尋找連接到該 pin 的輸出連接，並針對 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面進行查詢。</span><span class="sxs-lookup"><span data-stu-id="25fc0-112">If so, the filter graph manager finds the output pin connected to that pin and queries it for the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="25fc0-113">如果輸出釘選支援 **IMediaEventSink**，則篩選圖形管理員會呼叫 [**IMediaEventSink：： NOTIFY**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) 以使用 EC 重新 \_ 繪製事件代碼。</span><span class="sxs-lookup"><span data-stu-id="25fc0-113">If the output pin supports **IMediaEventSink**, the filter graph manager calls [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) with the EC\_REPAINT event code.</span></span> <span data-ttu-id="25fc0-114">這可讓上游篩選器有機會重新傳送最後一個範例。</span><span class="sxs-lookup"><span data-stu-id="25fc0-114">This gives the upstream filter the opportunity to re-send the last sample.</span></span>

<span data-ttu-id="25fc0-115">如果 *lParam1* 為 **Null**，或 pin 不支援 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)，或如果 [**通知**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) 方法失敗，則篩選圖形管理員本身會處理 EC 重新 \_ 繪製事件。</span><span class="sxs-lookup"><span data-stu-id="25fc0-115">If *lParam1* is **NULL**, or if the pin does not support [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), or if the [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method fails, the filter graph manager handles the EC\_REPAINT event by itself.</span></span> <span data-ttu-id="25fc0-116">其行為取決於圖形的狀態：</span><span class="sxs-lookup"><span data-stu-id="25fc0-116">Its behavior depends on the state of the graph:</span></span>

-   <span data-ttu-id="25fc0-117">正在執行：忽略事件。</span><span class="sxs-lookup"><span data-stu-id="25fc0-117">Running: Ignores the event.</span></span> <span data-ttu-id="25fc0-118"> (轉譯器會接收資料流程中的下一個範例。 ) </span><span class="sxs-lookup"><span data-stu-id="25fc0-118">(The renderer will receive the next sample in the stream.)</span></span>
-   <span data-ttu-id="25fc0-119">已暫停：將圖形搜尋至其目前的位置，藉此清除篩選並重新將資料排入佇列。</span><span class="sxs-lookup"><span data-stu-id="25fc0-119">Paused: Seeks the graph to its current location, thereby flushing the filter and re-queuing the data.</span></span>
-   <span data-ttu-id="25fc0-120">已停止：暫停並停止圖形，藉此將資料重新排入佇列。</span><span class="sxs-lookup"><span data-stu-id="25fc0-120">Stopped: Pauses and stops the graph, thereby re-queuing the data.</span></span>

<span data-ttu-id="25fc0-121">篩選圖形管理員預設不會將此事件傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="25fc0-121">By default, the filter graph manager does not pass this event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="25fc0-122">備註</span><span class="sxs-lookup"><span data-stu-id="25fc0-122">Remarks</span></span>

<span data-ttu-id="25fc0-123">影片轉譯器會在收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息且沒有可顯示的資料時傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="25fc0-123">Video renderers send this message when they receive a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message and have no data to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fc0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="25fc0-124">Requirements</span></span>



| <span data-ttu-id="25fc0-125">需求</span><span class="sxs-lookup"><span data-stu-id="25fc0-125">Requirement</span></span> | <span data-ttu-id="25fc0-126">值</span><span class="sxs-lookup"><span data-stu-id="25fc0-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25fc0-127">標頭</span><span class="sxs-lookup"><span data-stu-id="25fc0-127">Header</span></span><br/> | <dl> <span data-ttu-id="25fc0-128"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="25fc0-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25fc0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25fc0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fc0-130">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="25fc0-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="25fc0-131">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="25fc0-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

