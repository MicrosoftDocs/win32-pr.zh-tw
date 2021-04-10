---
title: 'ICM_DRAW 訊息 (Vfw .h) '
description: ICM \_ 描繪訊息會通知轉譯驅動程式將資料框架解壓縮，並將其繪製到螢幕。
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685825"
---
# <a name="icm_draw-message"></a><span data-ttu-id="0c8ba-104">ICM \_ 繪製訊息</span><span class="sxs-lookup"><span data-stu-id="0c8ba-104">ICM\_DRAW message</span></span>

<span data-ttu-id="0c8ba-105">**ICM \_ 描繪** 訊息會通知轉譯驅動程式將資料框架解壓縮，並將其繪製到螢幕。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-105">The **ICM\_DRAW** message notifies a rendering driver to decompress a frame of data and draw it to the screen.</span></span>


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="0c8ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c8ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c8ba-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c8ba-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="0c8ba-108">[**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-108">Pointer to an [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c8ba-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c8ba-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0c8ba-110">[**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-110">Size, in bytes, of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c8ba-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c8ba-111">Return Value</span></span>

<span data-ttu-id="0c8ba-112">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c8ba-113">備註</span><span class="sxs-lookup"><span data-stu-id="0c8ba-113">Remarks</span></span>

<span data-ttu-id="0c8ba-114">如果 ICDRAW \_ 更新旗標是在 [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)的 **dwFlags** 成員中設定，則用於繪圖的畫面區域無效，需要更新。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-114">If the ICDRAW\_UPDATE flag is set in the **dwFlags** member of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), the area of the screen used for drawing is invalid and needs to be updated.</span></span> <span data-ttu-id="0c8ba-115">更新的範圍取決於 **lpData** 成員的內容而定。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-115">The extent of updating depends on the contents of the **lpData** member.</span></span>

<span data-ttu-id="0c8ba-116">如果 **lpData** 為 **Null**，驅動程式應該使用目前的影像來更新整個目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-116">If **lpData** is **NULL**, the driver should update the entire destination rectangle with the current image.</span></span> <span data-ttu-id="0c8ba-117">如果驅動程式在非螢幕緩衝區中維護映射的複本，它可能會讓此訊息失敗。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-117">If the driver maintains a copy of the image in an off-screen buffer, it can fail this message.</span></span> <span data-ttu-id="0c8ba-118">如果 **lpData** 不是 **Null**，驅動程式應該繪製資料，並確定整個目的地都已更新。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-118">If **lpData** is not **NULL**, the driver should draw the data and make sure the entire destination is updated.</span></span>

<span data-ttu-id="0c8ba-119">如果 \_ 已在 **dwFlags** 中設定 ICDRAW HURRYUP 旗標，則呼叫的應用程式會希望驅動程式儘快進行，甚至可能不會更新螢幕。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-119">If the ICDRAW\_HURRYUP flag is set in **dwFlags**, the calling application wants the driver to proceed as quickly as possible, possibly not even updating the screen.</span></span>

<span data-ttu-id="0c8ba-120">如果在 \_ **dwFlags** 中設定 ICDRAW 預先設置旗標，此影片畫面會是初步資訊，而且不應該在可能的情況下顯示。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-120">If the ICDRAW\_PREROLL flag is set in **dwFlags**, this video frame is preliminary information and should not be displayed if possible.</span></span> <span data-ttu-id="0c8ba-121">例如，如果播放是從畫面格10開始，而框架0是最接近的先前主要畫面格，則畫面格0到9將會設定 ICDRAW 的預先 \_ 設定。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-121">For example, if play is to start from frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 will have ICDRAW\_PREROLL set.</span></span>

<span data-ttu-id="0c8ba-122">如果您希望驅動程式將資料解壓縮到緩衝區中，請傳送 [**ICM \_ 解壓縮**](icm-decompress.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0c8ba-122">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS**](icm-decompress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8ba-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c8ba-123">Requirements</span></span>



| <span data-ttu-id="0c8ba-124">需求</span><span class="sxs-lookup"><span data-stu-id="0c8ba-124">Requirement</span></span> | <span data-ttu-id="0c8ba-125">值</span><span class="sxs-lookup"><span data-stu-id="0c8ba-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0c8ba-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c8ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0c8ba-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c8ba-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0c8ba-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c8ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0c8ba-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c8ba-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0c8ba-130">標頭</span><span class="sxs-lookup"><span data-stu-id="0c8ba-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c8ba-131"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c8ba-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c8ba-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c8ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c8ba-133">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="0c8ba-133">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0c8ba-134">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="0c8ba-134">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





