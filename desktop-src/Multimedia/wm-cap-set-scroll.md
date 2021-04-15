---
title: 'WM_CAP_SET_SCROLL 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 捲軸訊息會定義要在 [捕捉] 視窗中顯示的影片畫面部分。
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466865"
---
# <a name="wm_cap_set_scroll-message"></a><span data-ttu-id="608b0-104">WM \_ CAP \_ 設定 \_ 捲軸訊息</span><span class="sxs-lookup"><span data-stu-id="608b0-104">WM\_CAP\_SET\_SCROLL message</span></span>

<span data-ttu-id="608b0-105">**WM \_ CAP \_ 設定 \_ 滾動** 條訊息會定義要在 [捕捉] 視窗中顯示的影片畫面部分。</span><span class="sxs-lookup"><span data-stu-id="608b0-105">The **WM\_CAP\_SET\_SCROLL** message defines the portion of the video frame to display in the capture window.</span></span> <span data-ttu-id="608b0-106">這則訊息會將 [capture] 視窗工作區的左上角，設定為影片框架內指定圖元的座標。</span><span class="sxs-lookup"><span data-stu-id="608b0-106">This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame.</span></span> <span data-ttu-id="608b0-107">您可以使用 [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="608b0-107">You can send this message explicitly or by using the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro.</span></span>


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a><span data-ttu-id="608b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="608b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="608b0-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span><span class="sxs-lookup"><span data-stu-id="608b0-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span></span>
</dt> <dd>

<span data-ttu-id="608b0-110">要包含所需滾動位置的位址。</span><span class="sxs-lookup"><span data-stu-id="608b0-110">Address to contain the desired scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="608b0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="608b0-111">Return Value</span></span>

<span data-ttu-id="608b0-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="608b0-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="608b0-113">備註</span><span class="sxs-lookup"><span data-stu-id="608b0-113">Remarks</span></span>

<span data-ttu-id="608b0-114">捲軸位置會影響預覽和重迭模式中的影像。</span><span class="sxs-lookup"><span data-stu-id="608b0-114">The scroll position affects the image in both preview and overlay modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="608b0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="608b0-115">Requirements</span></span>



| <span data-ttu-id="608b0-116">需求</span><span class="sxs-lookup"><span data-stu-id="608b0-116">Requirement</span></span> | <span data-ttu-id="608b0-117">值</span><span class="sxs-lookup"><span data-stu-id="608b0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="608b0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="608b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="608b0-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="608b0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="608b0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="608b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="608b0-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="608b0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="608b0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="608b0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="608b0-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="608b0-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="608b0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="608b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="608b0-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="608b0-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="608b0-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="608b0-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





