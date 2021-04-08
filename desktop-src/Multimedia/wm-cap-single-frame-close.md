---
title: 'WM_CAP_SINGLE_FRAME_CLOSE 訊息 (Vfw .h) '
description: WM \_ cap \_ 單一 \_ 框架 \_ 關閉訊息會關閉由 wm \_ cap \_ 單一 \_ 框架開啟的 \_ 訊息開啟的捕獲檔案。 您可以使用 capCaptureSingleFrameClose 宏明確地傳送此訊息。
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686451"
---
# <a name="wm_cap_single_frame_close-message"></a><span data-ttu-id="75725-105">WM \_ CAP \_ 單一 \_ 框架 \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="75725-105">WM\_CAP\_SINGLE\_FRAME\_CLOSE message</span></span>

<span data-ttu-id="75725-106">**Wm \_ cap \_ 單一 \_ 框架 \_ 關閉** 訊息會關閉由 [**wm \_ cap \_ 單一 \_ 框架 \_ 開啟**](wm-cap-single-frame-open.md)的訊息開啟的捕獲檔案。</span><span class="sxs-lookup"><span data-stu-id="75725-106">The **WM\_CAP\_SINGLE\_FRAME\_CLOSE** message closes the capture file opened by the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="75725-107">您可以使用 [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="75725-107">You can send this message explicitly or by using the [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="75725-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="75725-108">Return Value</span></span>

<span data-ttu-id="75725-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="75725-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="75725-110">備註</span><span class="sxs-lookup"><span data-stu-id="75725-110">Remarks</span></span>

<span data-ttu-id="75725-111">如需安裝回呼函式的詳細資訊，請參閱 [**wm \_ cap \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 和 [**wm \_ \_ 設定 \_ 回呼 \_ 框架**](wm-cap-set-callback-frame.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="75725-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="75725-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="75725-112">Requirements</span></span>



| <span data-ttu-id="75725-113">需求</span><span class="sxs-lookup"><span data-stu-id="75725-113">Requirement</span></span> | <span data-ttu-id="75725-114">值</span><span class="sxs-lookup"><span data-stu-id="75725-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75725-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75725-115">Minimum supported client</span></span><br/> | <span data-ttu-id="75725-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75725-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="75725-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75725-117">Minimum supported server</span></span><br/> | <span data-ttu-id="75725-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75725-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="75725-119">標頭</span><span class="sxs-lookup"><span data-stu-id="75725-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="75725-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="75725-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75725-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75725-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75725-122">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="75725-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="75725-123">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="75725-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





