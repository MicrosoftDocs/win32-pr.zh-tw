---
description: 影片轉譯器已從圖形終結或移除。
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: 'EC_WINDOW_DESTROYED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992557"
---
# <a name="ec_window_destroyed"></a><span data-ttu-id="bce9a-103">EC \_ 視窗已 \_ 損毀</span><span class="sxs-lookup"><span data-stu-id="bce9a-103">EC\_WINDOW\_DESTROYED</span></span>

<span data-ttu-id="bce9a-104">影片轉譯器已從圖形終結或移除。</span><span class="sxs-lookup"><span data-stu-id="bce9a-104">The video renderer was destroyed or removed from the graph.</span></span>

## <a name="parameters"></a><span data-ttu-id="bce9a-105">參數</span><span class="sxs-lookup"><span data-stu-id="bce9a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce9a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bce9a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bce9a-107"> (**IUnknown** \*) 指標指向影片轉譯器的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面。</span><span class="sxs-lookup"><span data-stu-id="bce9a-107">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> <dt>

<span data-ttu-id="bce9a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bce9a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bce9a-109">零個。</span><span class="sxs-lookup"><span data-stu-id="bce9a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="bce9a-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="bce9a-110">Default Action</span></span>

<span data-ttu-id="bce9a-111">篩選圖形管理員會透過 [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) 介面，將此視窗以焦點的形式釋放。</span><span class="sxs-lookup"><span data-stu-id="bce9a-111">The filter graph manager releases this window as the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="bce9a-112">它不會將事件通知傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="bce9a-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="bce9a-113">備註</span><span class="sxs-lookup"><span data-stu-id="bce9a-113">Remarks</span></span>

<span data-ttu-id="bce9a-114">影片轉譯器會在其 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法中離開篩選圖形時傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="bce9a-114">The video renderer sends this event when it leaves the filter graph, in its [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="bce9a-115">當篩選損毀時 (傳送事件可能太晚，因為篩選圖形管理員可能也會終結。 ) </span><span class="sxs-lookup"><span data-stu-id="bce9a-115">(Sending the event when the filter is destroyed might be too late, because at that point the filter graph manager might also be destroyed.)</span></span>

<span data-ttu-id="bce9a-116">此事件可讓其他篩選器取得相依于視窗焦點的資源，例如音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="bce9a-116">This event enables other filters to acquire resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce9a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bce9a-117">Requirements</span></span>



| <span data-ttu-id="bce9a-118">需求</span><span class="sxs-lookup"><span data-stu-id="bce9a-118">Requirement</span></span> | <span data-ttu-id="bce9a-119">值</span><span class="sxs-lookup"><span data-stu-id="bce9a-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bce9a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="bce9a-120">Header</span></span><br/> | <dl> <span data-ttu-id="bce9a-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="bce9a-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce9a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bce9a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce9a-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="bce9a-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bce9a-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="bce9a-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




