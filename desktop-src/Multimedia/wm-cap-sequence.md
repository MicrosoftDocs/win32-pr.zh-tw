---
title: 'WM_CAP_SEQUENCE 訊息 (Vfw .h) '
description: WM \_ CAP \_ 序列訊息會起始串流影片和音訊捕獲至檔案。 您可以使用 capCaptureSequence 宏明確地傳送此訊息。
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934519"
---
# <a name="wm_cap_sequence-message"></a><span data-ttu-id="8363d-105">WM \_ CAP \_ 序列訊息</span><span class="sxs-lookup"><span data-stu-id="8363d-105">WM\_CAP\_SEQUENCE message</span></span>

<span data-ttu-id="8363d-106">**WM \_ CAP \_ 序列** 訊息會起始串流影片和音訊捕獲至檔案。</span><span class="sxs-lookup"><span data-stu-id="8363d-106">The **WM\_CAP\_SEQUENCE** message initiates streaming video and audio capture to a file.</span></span> <span data-ttu-id="8363d-107">您可以使用 [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8363d-107">You can send this message explicitly or by using the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro.</span></span>


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="8363d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8363d-108">Return Value</span></span>

<span data-ttu-id="8363d-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8363d-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="8363d-110">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="8363d-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="8363d-111">備註</span><span class="sxs-lookup"><span data-stu-id="8363d-111">Remarks</span></span>

<span data-ttu-id="8363d-112">如果您想要改變控制串流處理捕獲的參數，請在啟動 capture 之前，先使用 [**WM \_ CAP \_ SET \_ SEQUENCE \_ 安裝程式**](wm-cap-set-sequence-setup.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8363d-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="8363d-113">根據預設，「捕獲」視窗不允許其他應用程式在捕捉期間繼續執行。</span><span class="sxs-lookup"><span data-stu-id="8363d-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="8363d-114">若要覆寫此屬性，請將 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fYield** 成員設為 **TRUE**，或安裝 yield 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8363d-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="8363d-115">在串流處理期間，[捕獲] 視窗可以選擇性地將通知發行至特定類型條件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8363d-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="8363d-116">若要安裝這些通知的回呼程式，請使用下列訊息：</span><span class="sxs-lookup"><span data-stu-id="8363d-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="8363d-117">**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="8363d-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="8363d-118">**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="8363d-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="8363d-119">**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**</span><span class="sxs-lookup"><span data-stu-id="8363d-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="8363d-120">**WM \_ CAP \_ 設定 \_ 回呼 \_ M**</span><span class="sxs-lookup"><span data-stu-id="8363d-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="8363d-121">**WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM**</span><span class="sxs-lookup"><span data-stu-id="8363d-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="8363d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8363d-122">Requirements</span></span>



| <span data-ttu-id="8363d-123">需求</span><span class="sxs-lookup"><span data-stu-id="8363d-123">Requirement</span></span> | <span data-ttu-id="8363d-124">值</span><span class="sxs-lookup"><span data-stu-id="8363d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8363d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8363d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8363d-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8363d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8363d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8363d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8363d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8363d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8363d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="8363d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8363d-130"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8363d-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8363d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8363d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8363d-132">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="8363d-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8363d-133">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="8363d-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





