---
description: 影片轉譯器正在切換至全螢幕模式。
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: 'EC_FULLSCREEN_LOST (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994724"
---
# <a name="ec_fullscreen_lost"></a><span data-ttu-id="02809-103">EC \_ 全螢幕 \_ 遺失</span><span class="sxs-lookup"><span data-stu-id="02809-103">EC\_FULLSCREEN\_LOST</span></span>

<span data-ttu-id="02809-104">影片轉譯器正在切換至全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="02809-104">The video renderer is switching out of full-screen mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="02809-105">參數</span><span class="sxs-lookup"><span data-stu-id="02809-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02809-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="02809-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="02809-107">零個。</span><span class="sxs-lookup"><span data-stu-id="02809-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="02809-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="02809-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="02809-109"> (**IUnknown**) 指向影片轉譯器之 \* [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="02809-109">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="02809-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="02809-110">Default Action</span></span>

<span data-ttu-id="02809-111">無。</span><span class="sxs-lookup"><span data-stu-id="02809-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="02809-112">備註</span><span class="sxs-lookup"><span data-stu-id="02809-112">Remarks</span></span>

<span data-ttu-id="02809-113">當 [全螢幕](full-screen-renderer-filter.md) 轉譯器失去啟用時，它會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="02809-113">When the [Full Screen Renderer](full-screen-renderer-filter.md) loses activation, it sends this event.</span></span> <span data-ttu-id="02809-114">當另一個影片轉譯器切換至全螢幕模式時，篩選圖形管理員會傳送此事件，以回應轉譯器的 [**EC \_ 啟動**](ec-activate.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="02809-114">When another video renderer switches out of full-screen mode, the filter graph manager sends this event, in response to an [**EC\_ACTIVATE**](ec-activate.md) event from the renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="02809-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="02809-115">Requirements</span></span>



| <span data-ttu-id="02809-116">需求</span><span class="sxs-lookup"><span data-stu-id="02809-116">Requirement</span></span> | <span data-ttu-id="02809-117">值</span><span class="sxs-lookup"><span data-stu-id="02809-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02809-118">標頭</span><span class="sxs-lookup"><span data-stu-id="02809-118">Header</span></span><br/> | <dl> <span data-ttu-id="02809-119"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="02809-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02809-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02809-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02809-121">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="02809-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="02809-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="02809-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




