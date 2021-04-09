---
title: AVICap 回呼函式
description: AVICap 回呼函式
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- AVICap 類別，回呼函數
- AVICap 回呼函式，關於
- WM_CAP_SET_CALLBACK_CAPCONTROL 訊息
- WM_CAP_SET_CALLBACK_ERROR 訊息
- WM_CAP_SET_CALLBACK_FRAME 訊息
- WM_CAP_SET_CALLBACK_STATUS 訊息
- WM_CAP_SET_CALLBACK_VIDEOSTREAM 訊息
- WM_CAP_SET_CALLBACK_WAVESTREAM 訊息
- WM_CAP_SET_CALLBACK_YIELD 訊息
- capSetCallbackOnCapControl 宏
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame 宏
- capSetCallbackOnStatus 宏
- capSetCallbackOnVideoStream 宏
- capSetCallbackOnWaveStream 宏
- capSetCallbackOnYield 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932547"
---
# <a name="avicap-callback-functions"></a><span data-ttu-id="e2d4c-119">AVICap 回呼函式</span><span class="sxs-lookup"><span data-stu-id="e2d4c-119">AVICap Callback Functions</span></span>

<span data-ttu-id="e2d4c-120">您的應用程式可以使用捕捉視窗註冊回呼函式，讓它在狀態變更、發生錯誤、當影片畫面格和音訊緩衝區可供使用，以及在串流捕獲期間產生時，通知您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-120">Your application can register callback functions with a capture window to have it notify your application when the status changes, when errors occur, when video frame and audio buffers become available, and to yield during streaming capture.</span></span> <span data-ttu-id="e2d4c-121">下列訊息會設定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-121">The following messages set the callback function.</span></span>



| <span data-ttu-id="e2d4c-122">訊息</span><span class="sxs-lookup"><span data-stu-id="e2d4c-122">Message</span></span>                                                                        | <span data-ttu-id="e2d4c-123">描述</span><span class="sxs-lookup"><span data-stu-id="e2d4c-123">Description</span></span>                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2d4c-124">**WM \_ CAP \_ 設定 \_ 回呼 \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="e2d4c-124">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)   | <span data-ttu-id="e2d4c-125">指定應用程式中呼叫的回呼函式，以提供對開始和結束的精確控制。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-125">Specifies the callback function in the application called to give precise control over capture start and end.</span></span> <span data-ttu-id="e2d4c-126">您也可以使用 [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-126">You can also use the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro to send this message.</span></span>                   |
| [<span data-ttu-id="e2d4c-127">**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e2d4c-127">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)             | <span data-ttu-id="e2d4c-128">指定在發生錯誤時呼叫的應用程式中的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-128">Specifies the callback function in the application called when an error occurs.</span></span> <span data-ttu-id="e2d4c-129">您也可以使用 [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-129">You can also use the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro to send this message.</span></span>                                                           |
| [<span data-ttu-id="e2d4c-130">**WM \_ CAP \_ 設定 \_ 回呼 \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="e2d4c-130">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)             | <span data-ttu-id="e2d4c-131">指定在捕獲預覽框架時呼叫的應用程式中的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-131">Specifies the callback function in the application called when preview frames are captured.</span></span> <span data-ttu-id="e2d4c-132">您也可以使用 [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-132">You can also use the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro to send this message.</span></span>                                               |
| [<span data-ttu-id="e2d4c-133">**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e2d4c-133">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)           | <span data-ttu-id="e2d4c-134">指定當狀態變更時所呼叫之應用程式中的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-134">Specifies the callback function in the application called when the status changes.</span></span> <span data-ttu-id="e2d4c-135">您也可以使用 [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-135">You can also use the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro to send this message.</span></span>                                                      |
| [<span data-ttu-id="e2d4c-136">**WM \_ CAP \_ 設定 \_ 回呼 \_ M**</span><span class="sxs-lookup"><span data-stu-id="e2d4c-136">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md) | <span data-ttu-id="e2d4c-137">指定當新的影片緩衝區變成可用時，在串流處理期間呼叫的應用程式中所呼叫的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-137">Specifies the callback function in the application called during streaming capture when a new video buffer becomes available.</span></span> <span data-ttu-id="e2d4c-138">您也可以使用 [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-138">You can also use the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro to send this message.</span></span> |
| [<span data-ttu-id="e2d4c-139">**WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM**</span><span class="sxs-lookup"><span data-stu-id="e2d4c-139">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)   | <span data-ttu-id="e2d4c-140">指定當新的音訊緩衝區變成可用時，在串流處理期間呼叫的應用程式中的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-140">Specifies the callback function in the application called during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="e2d4c-141">您也可以使用 [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-141">You can also use the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro to send this message.</span></span>   |
| [<span data-ttu-id="e2d4c-142">**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**</span><span class="sxs-lookup"><span data-stu-id="e2d4c-142">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)             | <span data-ttu-id="e2d4c-143">指定在串流捕獲期間產生的應用程式中所呼叫的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-143">Specifies the callback function in the application called when yielding during streaming capture.</span></span> <span data-ttu-id="e2d4c-144">您也可以使用 [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) 宏來傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-144">You can also use the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro to send this message.</span></span>                                         |



 

<span data-ttu-id="e2d4c-145">下列主題描述不同的回呼函式、傳送至函式的通知，以及其使用方式。</span><span class="sxs-lookup"><span data-stu-id="e2d4c-145">The following topics describe the different callback functions, the notifications sent to the functions, and their uses.</span></span>

 

 




