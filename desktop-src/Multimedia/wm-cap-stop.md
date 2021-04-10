---
title: 'WM_CAP_STOP 訊息 (Vfw .h) '
description: WM \_ CAP \_ 停止訊息會停止捕獲操作。 您可以使用 capCaptureStop 宏明確地傳送此訊息。
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686447"
---
# <a name="wm_cap_stop-message"></a><span data-ttu-id="b78ef-105">WM \_ CAP \_ 停止訊息</span><span class="sxs-lookup"><span data-stu-id="b78ef-105">WM\_CAP\_STOP message</span></span>

<span data-ttu-id="b78ef-106">**WM \_ CAP \_ 停止** 訊息會停止捕獲操作。</span><span class="sxs-lookup"><span data-stu-id="b78ef-106">The **WM\_CAP\_STOP** message stops the capture operation.</span></span> <span data-ttu-id="b78ef-107">您可以使用 [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b78ef-107">You can send this message explicitly or by using the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro.</span></span>

<span data-ttu-id="b78ef-108">在步驟框架捕獲中，傳送此訊息之前所收集的影像資料會保留在 capture 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b78ef-108">In step frame capture, the image data that was collected before this message was sent is retained in the capture file.</span></span> <span data-ttu-id="b78ef-109">如果啟用音訊捕捉，則相同的音訊資料持續時間也會保留在 capture 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b78ef-109">An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.</span></span>


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="b78ef-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b78ef-110">Return Value</span></span>

<span data-ttu-id="b78ef-111">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b78ef-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b78ef-112">備註</span><span class="sxs-lookup"><span data-stu-id="b78ef-112">Remarks</span></span>

<span data-ttu-id="b78ef-113">捕捉作業必須採用此訊息。</span><span class="sxs-lookup"><span data-stu-id="b78ef-113">The capture operation must yield to use this message.</span></span> <span data-ttu-id="b78ef-114">使用 [**WM \_ CAP \_ ABORT**](wm-cap-abort.md) 訊息放棄目前的捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="b78ef-114">Use the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message to abandon the current capture operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b78ef-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b78ef-115">Requirements</span></span>



| <span data-ttu-id="b78ef-116">需求</span><span class="sxs-lookup"><span data-stu-id="b78ef-116">Requirement</span></span> | <span data-ttu-id="b78ef-117">值</span><span class="sxs-lookup"><span data-stu-id="b78ef-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b78ef-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b78ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b78ef-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b78ef-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b78ef-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b78ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b78ef-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b78ef-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b78ef-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b78ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b78ef-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b78ef-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78ef-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b78ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78ef-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="b78ef-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b78ef-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="b78ef-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





