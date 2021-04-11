---
title: 'WM_CAP_SINGLE_FRAME 訊息 (Vfw .h) '
description: WM \_ cap \_ 單一 \_ 框架訊息會將單一畫面附加至使用 WM \_ cap \_ 單一 \_ 框架 \_ 開啟訊息開啟的捕獲檔案。 您可以使用 capCaptureSingleFrame 宏明確地傳送此訊息。
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106098"
---
# <a name="wm_cap_single_frame-message"></a><span data-ttu-id="9034a-105">WM \_ CAP \_ 單一 \_ 畫面格訊息</span><span class="sxs-lookup"><span data-stu-id="9034a-105">WM\_CAP\_SINGLE\_FRAME message</span></span>

<span data-ttu-id="9034a-106">**WM \_ cap \_ 單一 \_ 框架** 訊息會將單一畫面附加至使用 [**WM \_ cap \_ 單一 \_ 框架 \_ 開啟**](wm-cap-single-frame-open.md)訊息開啟的捕獲檔案。</span><span class="sxs-lookup"><span data-stu-id="9034a-106">The **WM\_CAP\_SINGLE\_FRAME** message appends a single frame to a capture file that was opened using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="9034a-107">您可以使用 [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9034a-107">You can send this message explicitly or by using the [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="9034a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9034a-108">Return Value</span></span>

<span data-ttu-id="9034a-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9034a-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9034a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9034a-110">Requirements</span></span>



| <span data-ttu-id="9034a-111">需求</span><span class="sxs-lookup"><span data-stu-id="9034a-111">Requirement</span></span> | <span data-ttu-id="9034a-112">值</span><span class="sxs-lookup"><span data-stu-id="9034a-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9034a-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9034a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9034a-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9034a-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9034a-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9034a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9034a-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9034a-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9034a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="9034a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9034a-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="9034a-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9034a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9034a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9034a-120">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="9034a-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9034a-121">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="9034a-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





