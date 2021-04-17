---
title: 'WM_CAP_GRAB_FRAME 訊息 (Vfw .h) '
description: WM \_ CAP \_ 抓取 \_ 框架訊息會從 capture 驅動程式取出並顯示單一畫面格。 在 capture 之後，會停用覆迭和預覽。 您可以使用 capGrabFrame 宏明確地傳送此訊息。
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465665"
---
# <a name="wm_cap_grab_frame-message"></a><span data-ttu-id="24c44-106">WM \_ 上限 \_ 抓取 \_ 框架訊息</span><span class="sxs-lookup"><span data-stu-id="24c44-106">WM\_CAP\_GRAB\_FRAME message</span></span>

<span data-ttu-id="24c44-107">**WM \_ CAP \_ 抓取 \_ 框架** 訊息會從 capture 驅動程式取出並顯示單一畫面格。</span><span class="sxs-lookup"><span data-stu-id="24c44-107">The **WM\_CAP\_GRAB\_FRAME** message retrieves and displays a single frame from the capture driver.</span></span> <span data-ttu-id="24c44-108">在 capture 之後，會停用覆迭和預覽。</span><span class="sxs-lookup"><span data-stu-id="24c44-108">After capture, overlay and preview are disabled.</span></span> <span data-ttu-id="24c44-109">您可以使用 [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="24c44-109">You can send this message explicitly or by using the [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a><span data-ttu-id="24c44-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="24c44-110">Return Value</span></span>

<span data-ttu-id="24c44-111">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="24c44-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c44-112">備註</span><span class="sxs-lookup"><span data-stu-id="24c44-112">Remarks</span></span>

<span data-ttu-id="24c44-113">如需安裝回呼函式的詳細資訊，請參閱 [**wm \_ cap \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 和 [**wm \_ \_ 設定 \_ 回呼 \_ 框架**](wm-cap-set-callback-frame.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="24c44-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c44-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="24c44-114">Requirements</span></span>



| <span data-ttu-id="24c44-115">需求</span><span class="sxs-lookup"><span data-stu-id="24c44-115">Requirement</span></span> | <span data-ttu-id="24c44-116">值</span><span class="sxs-lookup"><span data-stu-id="24c44-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="24c44-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24c44-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24c44-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24c44-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="24c44-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24c44-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24c44-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24c44-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="24c44-121">標頭</span><span class="sxs-lookup"><span data-stu-id="24c44-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="24c44-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="24c44-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c44-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24c44-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c44-124">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="24c44-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="24c44-125">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="24c44-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





