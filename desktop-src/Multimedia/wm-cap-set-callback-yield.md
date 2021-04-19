---
title: 'WM_CAP_SET_CALLBACK_YIELD 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ YIELD 訊息會在應用程式中設定回呼函式。 AVICap 會在串流捕捉期間產生捕捉視窗時呼叫此程式。 您可以使用 capSetCallbackOnYield 宏明確地傳送此訊息。
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965471"
---
# <a name="wm_cap_set_callback_yield-message"></a><span data-ttu-id="66eaa-106">WM \_ CAP \_ 設定 \_ 回呼 \_ 產生訊息</span><span class="sxs-lookup"><span data-stu-id="66eaa-106">WM\_CAP\_SET\_CALLBACK\_YIELD message</span></span>

<span data-ttu-id="66eaa-107">**WM \_ CAP \_ SET \_ 回呼 \_ YIELD** 訊息會在應用程式中設定回呼函式。</span><span class="sxs-lookup"><span data-stu-id="66eaa-107">The **WM\_CAP\_SET\_CALLBACK\_YIELD** message sets a callback function in the application.</span></span> <span data-ttu-id="66eaa-108">AVICap 會在串流捕捉期間產生捕捉視窗時呼叫此程式。</span><span class="sxs-lookup"><span data-stu-id="66eaa-108">AVICap calls this procedure when the capture window yields during streaming capture.</span></span> <span data-ttu-id="66eaa-109">您可以使用 [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="66eaa-109">You can send this message explicitly or by using the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="66eaa-110">參數</span><span class="sxs-lookup"><span data-stu-id="66eaa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66eaa-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="66eaa-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="66eaa-112">Yield 回呼函數的指標，其類型為 [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)。</span><span class="sxs-lookup"><span data-stu-id="66eaa-112">Pointer to the yield callback function, of type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span></span> <span data-ttu-id="66eaa-113">針對此參數指定 **Null** ，以停用先前安裝的 yield 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="66eaa-113">Specify **NULL** for this parameter to disable a previously installed yield callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66eaa-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="66eaa-114">Return Value</span></span>

<span data-ttu-id="66eaa-115">如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="66eaa-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="66eaa-116">備註</span><span class="sxs-lookup"><span data-stu-id="66eaa-116">Remarks</span></span>

<span data-ttu-id="66eaa-117">應用程式可以選擇性地設定 yield 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="66eaa-117">Applications can optionally set a yield callback function.</span></span> <span data-ttu-id="66eaa-118">針對串流捕獲期間所捕獲的每個影片框架，會至少呼叫 yield 回呼函式一次。</span><span class="sxs-lookup"><span data-stu-id="66eaa-118">The yield callback function is called at least once for each video frame captured during streaming capture.</span></span> <span data-ttu-id="66eaa-119">如果已安裝 yield 回呼函式，無論 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fYield** 成員狀態為何，都會呼叫它。</span><span class="sxs-lookup"><span data-stu-id="66eaa-119">If a yield callback function is installed, it will be called regardless of the state of the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

<span data-ttu-id="66eaa-120">如果使用 yield 回呼函式，則必須先安裝它，才能啟動 capture 會話，且必須在會話持續時間內保持啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="66eaa-120">If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="66eaa-121">您可以在串流處理的結束之後停用此功能。</span><span class="sxs-lookup"><span data-stu-id="66eaa-121">It can be disabled after streaming capture ends.</span></span>

<span data-ttu-id="66eaa-122">應用程式通常會在包含 [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea)、 [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)、 [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 迴圈的回呼函式中執行某種類型的訊息處理，如同 [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) 函數的訊息迴圈一樣。</span><span class="sxs-lookup"><span data-stu-id="66eaa-122">Applications typically perform some type of message processing in the callback function consisting of a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) loop, as in the message loop of a [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="66eaa-123">Yield 回呼函式也必須篩選和移除可能造成重新進入問題的訊息。</span><span class="sxs-lookup"><span data-stu-id="66eaa-123">The yield callback function must also filter and remove messages that can cause reentrancy problems.</span></span>

<span data-ttu-id="66eaa-124">應用程式通常會在 yield 程式中傳回 **TRUE** ，以繼續串流捕捉。</span><span class="sxs-lookup"><span data-stu-id="66eaa-124">An application typically returns **TRUE** in the yield procedure to continue streaming capture.</span></span> <span data-ttu-id="66eaa-125">如果 yield 回呼函式傳回 **FALSE**，則捕獲視窗會停止 capture 進程。</span><span class="sxs-lookup"><span data-stu-id="66eaa-125">If a yield callback function returns **FALSE**, the capture window stops the capture process.</span></span>

## <a name="requirements"></a><span data-ttu-id="66eaa-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="66eaa-126">Requirements</span></span>



| <span data-ttu-id="66eaa-127">需求</span><span class="sxs-lookup"><span data-stu-id="66eaa-127">Requirement</span></span> | <span data-ttu-id="66eaa-128">值</span><span class="sxs-lookup"><span data-stu-id="66eaa-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="66eaa-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66eaa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="66eaa-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66eaa-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="66eaa-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66eaa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="66eaa-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66eaa-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66eaa-133">標頭</span><span class="sxs-lookup"><span data-stu-id="66eaa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="66eaa-134"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="66eaa-134"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66eaa-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66eaa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66eaa-136">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="66eaa-136">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="66eaa-137">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="66eaa-137">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

