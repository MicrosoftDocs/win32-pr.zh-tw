---
description: 顯示模式已變更。
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: 'EC_DISPLAY_CHANGED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995023"
---
# <a name="ec_display_changed"></a><span data-ttu-id="3be02-103">EC \_ 顯示 \_ 已變更</span><span class="sxs-lookup"><span data-stu-id="3be02-103">EC\_DISPLAY\_CHANGED</span></span>

<span data-ttu-id="3be02-104">顯示模式已變更。</span><span class="sxs-lookup"><span data-stu-id="3be02-104">The display mode has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="3be02-105">參數</span><span class="sxs-lookup"><span data-stu-id="3be02-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be02-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3be02-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3be02-107"> (**IUnknown** \*) 指標指向影片轉譯器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面陣列。</span><span class="sxs-lookup"><span data-stu-id="3be02-107">(**IUnknown**\*) Pointer to an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces for the video renderer's input pins.</span></span> <span data-ttu-id="3be02-108">如果 *lParam2* 為零，則此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3be02-108">If *lParam2* is zero, this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3be02-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3be02-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3be02-110">如果 *lParam2* 為零，則 *LParam1* 包含單一 **IPin** 指標或等於 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3be02-110">If *lParam2* is zero, *lParam1* contains a single **IPin** pointer or equals **NULL**.</span></span> <span data-ttu-id="3be02-111">如果 *lParam2* 大於零， *lParam1* 就會包含 **IPin** 指標的陣列，而陣列中的元素數目則由 *lParam2* 指定。</span><span class="sxs-lookup"><span data-stu-id="3be02-111">If *lParam2* is greater than zero, *lParam1* contains an array of **IPin** pointers, and the number of elements in the array is given by *lParam2*.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="3be02-112">預設動作</span><span class="sxs-lookup"><span data-stu-id="3be02-112">Default Action</span></span>

<span data-ttu-id="3be02-113">篩選圖形管理員會暫時停止圖形，然後中斷連接並重新連接影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="3be02-113">The filter graph manager temporarily stops the graph, and then disconnects and reconnects the video renderer.</span></span> <span data-ttu-id="3be02-114">它不會將事件傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="3be02-114">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="3be02-115">備註</span><span class="sxs-lookup"><span data-stu-id="3be02-115">Remarks</span></span>

<span data-ttu-id="3be02-116">影片轉譯器可以傳送此事件以回應 [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) 訊息。</span><span class="sxs-lookup"><span data-stu-id="3be02-116">Video renderers can send this event in response to a [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span> <span data-ttu-id="3be02-117">**WM \_ DISPLAYCHANGE** 訊息表示使用者已變更顯示器解析度。</span><span class="sxs-lookup"><span data-stu-id="3be02-117">The **WM\_DISPLAYCHANGE** message indicates that the user has changed the display resolution.</span></span>

<span data-ttu-id="3be02-118">在 pin 連接期間，大部分的影片轉譯器會根據目前的顯示模式來挑選格式。</span><span class="sxs-lookup"><span data-stu-id="3be02-118">During pin connection, most video renderers pick a format based on the current display mode.</span></span> <span data-ttu-id="3be02-119">如果顯示模式變更，影片轉譯器可能需要選擇另一種格式。</span><span class="sxs-lookup"><span data-stu-id="3be02-119">If the display mode changes, the video renderer might need to choose another format.</span></span> <span data-ttu-id="3be02-120">藉由傳送此訊息，轉譯器會向篩選圖形管理員發出需要重新連接的信號。</span><span class="sxs-lookup"><span data-stu-id="3be02-120">By sending this message, the renderer signals to the filter graph manager that it needs to be reconnected.</span></span> <span data-ttu-id="3be02-121">在重新連接期間，轉譯器可以選取新的格式。</span><span class="sxs-lookup"><span data-stu-id="3be02-121">During the reconnection, the renderer can select a new format.</span></span> <span data-ttu-id="3be02-122">如果重新連接失敗，則篩選圖形管理員會將 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="3be02-122">If the reconnection fails, the filter graph manager sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the application.</span></span>

### <a name="enhanced-video-renderer"></a><span data-ttu-id="3be02-123">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="3be02-123">Enhanced Video Renderer</span></span>

<span data-ttu-id="3be02-124">[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的自訂展示者 (EVR) 應該會將此事件傳送到 EVR，如果顯示者的 Direct3D 裝置有變更。</span><span class="sxs-lookup"><span data-stu-id="3be02-124">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) should send this event to the EVR if the presenter's Direct3D device changes.</span></span> <span data-ttu-id="3be02-125">將 *lParam1* 和 *lParam2* 設定為零;EVR 會忽略事件參數。</span><span class="sxs-lookup"><span data-stu-id="3be02-125">Set *lParam1* and *lParam2* to zero; the EVR ignores the event parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be02-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3be02-126">Requirements</span></span>



| <span data-ttu-id="3be02-127">需求</span><span class="sxs-lookup"><span data-stu-id="3be02-127">Requirement</span></span> | <span data-ttu-id="3be02-128">值</span><span class="sxs-lookup"><span data-stu-id="3be02-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3be02-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3be02-129">Header</span></span><br/> | <dl> <span data-ttu-id="3be02-130"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="3be02-130"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be02-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3be02-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be02-132">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="3be02-132">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3be02-133">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="3be02-133">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

