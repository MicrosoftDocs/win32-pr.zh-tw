---
title: 'WM_CAP_SET_CALLBACK_VIDEOSTREAM 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ m 訊息會在應用程式中設定回呼函數。
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383922"
---
# <a name="wm_cap_set_callback_videostream-message"></a><span data-ttu-id="8ab70-104">WM \_ CAP \_ 設定 \_ 回呼 \_ m 訊息</span><span class="sxs-lookup"><span data-stu-id="8ab70-104">WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM message</span></span>

<span data-ttu-id="8ab70-105">**WM \_ CAP \_ SET \_ 回呼 \_ m** 訊息會在應用程式中設定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8ab70-105">The **WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="8ab70-106">當視訊緩衝區填滿時，AVICap 會在串流處理期間呼叫此程式。</span><span class="sxs-lookup"><span data-stu-id="8ab70-106">AVICap calls this procedure during streaming capture when a video buffer is filled.</span></span> <span data-ttu-id="8ab70-107">您可以使用 [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8ab70-107">You can send this message explicitly or by using the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="8ab70-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ab70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ab70-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="8ab70-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="8ab70-110">影片資料流程回呼函數的指標，其類型為 [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)。</span><span class="sxs-lookup"><span data-stu-id="8ab70-110">Pointer to the video-stream callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="8ab70-111">針對此參數指定 **Null** ，以停用先前安裝的影片資料流程回呼函式。</span><span class="sxs-lookup"><span data-stu-id="8ab70-111">Specify **NULL** for this parameter to disable a previously installed video-stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ab70-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ab70-112">Return Value</span></span>

<span data-ttu-id="8ab70-113">如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8ab70-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ab70-114">備註</span><span class="sxs-lookup"><span data-stu-id="8ab70-114">Remarks</span></span>

<span data-ttu-id="8ab70-115">捕捉視窗會先呼叫回呼函式，再將捕獲的框架寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab70-115">The capture window calls the callback function before writing the captured frame to disk.</span></span> <span data-ttu-id="8ab70-116">這可讓應用程式視需要修改框架。</span><span class="sxs-lookup"><span data-stu-id="8ab70-116">This allows applications to modify the frame if desired.</span></span>

<span data-ttu-id="8ab70-117">如果影片資料流程回呼函式用於串流捕捉，則必須先安裝該程式，然後再啟動 capture 會話，而且在會話期間必須保持啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="8ab70-117">If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="8ab70-118">您可以在串流處理的結束之後停用此功能。</span><span class="sxs-lookup"><span data-stu-id="8ab70-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ab70-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ab70-119">Requirements</span></span>



| <span data-ttu-id="8ab70-120">需求</span><span class="sxs-lookup"><span data-stu-id="8ab70-120">Requirement</span></span> | <span data-ttu-id="8ab70-121">值</span><span class="sxs-lookup"><span data-stu-id="8ab70-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8ab70-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ab70-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab70-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ab70-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8ab70-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ab70-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab70-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ab70-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8ab70-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8ab70-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ab70-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ab70-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ab70-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ab70-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab70-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="8ab70-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8ab70-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="8ab70-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





