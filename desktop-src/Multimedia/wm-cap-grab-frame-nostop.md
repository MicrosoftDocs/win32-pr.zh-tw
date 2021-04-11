---
title: 'WM_CAP_GRAB_FRAME_NOSTOP 訊息 (Vfw .h) '
description: '[WM \_ 端點 \_ 抓取 \_ 框架] \_ NOSTOP 訊息會以單一未壓縮的框架（取自捕獲裝置）填滿框架緩衝區，並加以顯示。'
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844064"
---
# <a name="wm_cap_grab_frame_nostop-message"></a><span data-ttu-id="4a986-104">WM \_ CAP \_ 抓取 \_ 框架 \_ NOSTOP 訊息</span><span class="sxs-lookup"><span data-stu-id="4a986-104">WM\_CAP\_GRAB\_FRAME\_NOSTOP message</span></span>

<span data-ttu-id="4a986-105">[ **WM \_ 端點 \_ 抓取 \_ 框架] \_ NOSTOP** 訊息會以單一未壓縮的框架（取自捕獲裝置）填滿框架緩衝區，並加以顯示。</span><span class="sxs-lookup"><span data-stu-id="4a986-105">The **WM\_CAP\_GRAB\_FRAME\_NOSTOP** message fills the frame buffer with a single uncompressed frame from the capture device and displays it.</span></span> <span data-ttu-id="4a986-106">不同于 [**WM \_ CAP \_ 抓取 \_ 框架**](wm-cap-grab-frame.md) 訊息，此訊息不會改變重迭或預覽的狀態。</span><span class="sxs-lookup"><span data-stu-id="4a986-106">Unlike with the [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message, the state of overlay or preview is not altered by this message.</span></span> <span data-ttu-id="4a986-107">您可以使用 [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4a986-107">You can send this message explicitly or by using the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="4a986-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a986-108">Return Value</span></span>

<span data-ttu-id="4a986-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4a986-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a986-110">備註</span><span class="sxs-lookup"><span data-stu-id="4a986-110">Remarks</span></span>

<span data-ttu-id="4a986-111">如需安裝回呼函式的詳細資訊，請參閱 [**wm \_ cap \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 和 [**wm \_ \_ 設定 \_ 回呼 \_ 框架**](wm-cap-set-callback-frame.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="4a986-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a986-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a986-112">Requirements</span></span>



| <span data-ttu-id="4a986-113">需求</span><span class="sxs-lookup"><span data-stu-id="4a986-113">Requirement</span></span> | <span data-ttu-id="4a986-114">值</span><span class="sxs-lookup"><span data-stu-id="4a986-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4a986-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a986-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4a986-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a986-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4a986-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a986-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4a986-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a986-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a986-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4a986-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a986-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a986-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a986-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a986-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a986-122">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="4a986-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4a986-123">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="4a986-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





