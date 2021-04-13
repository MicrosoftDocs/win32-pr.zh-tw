---
title: 'ICM_DRAW_WINDOW 訊息 (Vfw .h) '
description: ICM \_ 繪圖 \_ 視窗訊息會通知轉譯驅動程式，表示需要重新繪製為 ICM \_ 繪圖 \_ 開始訊息指定的視窗。
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464992"
---
# <a name="icm_draw_window-message"></a><span data-ttu-id="ec5a5-104">ICM \_ 繪製 \_ 視窗訊息</span><span class="sxs-lookup"><span data-stu-id="ec5a5-104">ICM\_DRAW\_WINDOW message</span></span>

<span data-ttu-id="ec5a5-105">**Icm \_ 繪圖 \_ 視窗** 訊息會通知轉譯驅動程式，表示需要重新繪製為 [**ICM \_ 繪圖 \_ 開始**](icm-draw-begin.md)訊息指定的視窗。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-105">The **ICM\_DRAW\_WINDOW** message notifies a rendering driver that the window specified for the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message needs to be redrawn.</span></span> <span data-ttu-id="ec5a5-106">視窗已移動或暫時遮蔽。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-106">The window has moved or become temporarily obscured.</span></span> <span data-ttu-id="ec5a5-107">您可以使用 [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-107">You can send this message explicitly or by using the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro.</span></span>


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="ec5a5-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec5a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5a5-109"><span id="prc"></span><span id="PRC"></span>*中國*</span><span class="sxs-lookup"><span data-stu-id="ec5a5-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="ec5a5-110">螢幕座標中目的地矩形的指標。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-110">Pointer to the destination rectangle in screen coordinates.</span></span> <span data-ttu-id="ec5a5-111">如果這個參數指向空的矩形，則應該關閉繪製。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-111">If this parameter points to an empty rectangle, drawing should be turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5a5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec5a5-112">Return Value</span></span>

<span data-ttu-id="ec5a5-113">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec5a5-114">備註</span><span class="sxs-lookup"><span data-stu-id="ec5a5-114">Remarks</span></span>

<span data-ttu-id="ec5a5-115">此訊息是由執行自己的非同步解壓縮、時間和繪圖的硬體所支援。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-115">This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="ec5a5-116">影片重迭驅動程式會在視窗被遮蔽或移動時，使用此訊息來繪製。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-116">Video-overlay drivers use this message to draw when the window is obscured or moved.</span></span> <span data-ttu-id="ec5a5-117">當其他視窗完全隱藏指定給 [**ICM \_ 繪圖 \_ 開始**](icm-draw-begin.md) 的視窗時，目的地矩形會是空的。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-117">When a window specified for [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) is completely hidden by other windows, the destination rectangle is empty.</span></span> <span data-ttu-id="ec5a5-118">當發生這種情況時，驅動程式應該關閉影片重迭硬體。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-118">Drivers should turn off video-overlay hardware when this condition occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5a5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec5a5-119">Requirements</span></span>



| <span data-ttu-id="ec5a5-120">需求</span><span class="sxs-lookup"><span data-stu-id="ec5a5-120">Requirement</span></span> | <span data-ttu-id="ec5a5-121">值</span><span class="sxs-lookup"><span data-stu-id="ec5a5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec5a5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec5a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ec5a5-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5a5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec5a5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec5a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ec5a5-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5a5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec5a5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ec5a5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec5a5-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec5a5-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5a5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec5a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5a5-129">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="ec5a5-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ec5a5-130">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="ec5a5-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





