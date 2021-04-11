---
title: 'WM_CAP_SINGLE_FRAME_OPEN 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 單一 \_ 畫面格 \_ 開啟訊息] 會開啟單一畫面格捕獲的捕獲檔案。 捕捉檔案中的任何先前資訊都會遭到覆寫。 您可以使用 capCaptureSingleFrameOpen 宏明確地傳送此訊息。'
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844283"
---
# <a name="wm_cap_single_frame_open-message"></a><span data-ttu-id="2bbfb-106">WM \_ CAP \_ 單一 \_ 框架 \_ 開啟訊息</span><span class="sxs-lookup"><span data-stu-id="2bbfb-106">WM\_CAP\_SINGLE\_FRAME\_OPEN message</span></span>

<span data-ttu-id="2bbfb-107">[ **WM \_ CAP \_ 單一 \_ 畫面格 \_ 開啟** 訊息] 會開啟單一畫面格捕獲的捕獲檔案。</span><span class="sxs-lookup"><span data-stu-id="2bbfb-107">The **WM\_CAP\_SINGLE\_FRAME\_OPEN** message opens the capture file for single-frame capturing.</span></span> <span data-ttu-id="2bbfb-108">捕捉檔案中的任何先前資訊都會遭到覆寫。</span><span class="sxs-lookup"><span data-stu-id="2bbfb-108">Any previous information in the capture file is overwritten.</span></span> <span data-ttu-id="2bbfb-109">您可以使用 [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2bbfb-109">You can send this message explicitly or by using the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="2bbfb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bbfb-110">Return Value</span></span>

<span data-ttu-id="2bbfb-111">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2bbfb-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bbfb-112">備註</span><span class="sxs-lookup"><span data-stu-id="2bbfb-112">Remarks</span></span>

<span data-ttu-id="2bbfb-113">如需安裝回呼函式的詳細資訊，請參閱 [**wm \_ cap \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 和 [**wm \_ \_ 設定 \_ 回呼 \_ 框架**](wm-cap-set-callback-frame.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="2bbfb-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bbfb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bbfb-114">Requirements</span></span>



| <span data-ttu-id="2bbfb-115">需求</span><span class="sxs-lookup"><span data-stu-id="2bbfb-115">Requirement</span></span> | <span data-ttu-id="2bbfb-116">值</span><span class="sxs-lookup"><span data-stu-id="2bbfb-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2bbfb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bbfb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2bbfb-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bbfb-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2bbfb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bbfb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2bbfb-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bbfb-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2bbfb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2bbfb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bbfb-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bbfb-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bbfb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bbfb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbfb-124">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="2bbfb-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2bbfb-125">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="2bbfb-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





