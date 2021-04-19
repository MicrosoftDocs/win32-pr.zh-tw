---
title: 'WM_CAP_SET_CALLBACK_CAPCONTROL 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ CAPCONTROL 訊息會在應用程式中設定回呼函式，以提供精確的錄製控制項。 您可以使用 capSetCallbackOnCapControl 宏明確地傳送此訊息。
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969177"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a><span data-ttu-id="f3737-105">WM \_ CAP \_ 設定 \_ 回呼 \_ CAPCONTROL 訊息</span><span class="sxs-lookup"><span data-stu-id="f3737-105">WM\_CAP\_SET\_CALLBACK\_CAPCONTROL message</span></span>

<span data-ttu-id="f3737-106">**WM \_ CAP \_ SET \_ 回呼 \_ CAPCONTROL** 訊息會在應用程式中設定回呼函式，以提供精確的錄製控制項。</span><span class="sxs-lookup"><span data-stu-id="f3737-106">The **WM\_CAP\_SET\_CALLBACK\_CAPCONTROL** message sets a callback function in the application giving it precise recording control.</span></span> <span data-ttu-id="f3737-107">您可以使用 [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f3737-107">You can send this message explicitly or by using the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="f3737-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3737-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3737-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="f3737-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="f3737-110">回呼函數的指標，其類型為 [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)。</span><span class="sxs-lookup"><span data-stu-id="f3737-110">Pointer to the callback function, of type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span></span> <span data-ttu-id="f3737-111">針對此參數指定 **Null** ，以停用先前安裝的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f3737-111">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3737-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3737-112">Return Value</span></span>

<span data-ttu-id="f3737-113">如果成功，則傳回 **TRUE** ; 如果串流處理捕獲或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f3737-113">Returns **TRUE** if successful or **FALSE** if a streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3737-114">備註</span><span class="sxs-lookup"><span data-stu-id="f3737-114">Remarks</span></span>

<span data-ttu-id="f3737-115">單一回呼函式可用來讓應用程式精確地控制串流處理的開始和完成時間。</span><span class="sxs-lookup"><span data-stu-id="f3737-115">A single callback function is used to give the application precise control over the moments that streaming capture begins and completes.</span></span> <span data-ttu-id="f3737-116">捕捉視窗會先呼叫 *nState* 設定為 CONTROLCALLBACK 預先處理的程式 \_ ，然後再配置所有緩衝區，並完成所有其他的捕獲準備工作。</span><span class="sxs-lookup"><span data-stu-id="f3737-116">The capture window first calls the procedure with *nState* set to CONTROLCALLBACK\_PREROLL after all buffers have been allocated and all other capture preparations have finished.</span></span> <span data-ttu-id="f3737-117">如此一來，應用程式就可以預先產生影片來源，從回呼函式在確切的錄音開始時傳回。</span><span class="sxs-lookup"><span data-stu-id="f3737-117">This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin.</span></span> <span data-ttu-id="f3737-118">回呼函式中 **TRUE** 的傳回值會繼續捕捉，並傳回 **FALSE** 中止捕捉的傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3737-118">A return value of **TRUE** from the callback function continues capture, and a return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="f3737-119">開始 capture 之後，會經常呼叫此回呼函式，並將 *nState* 設定為 CONTROLCALLBACK capture，藉 \_ 由傳回 **FALSE** 來允許應用程式結束捕捉。</span><span class="sxs-lookup"><span data-stu-id="f3737-119">After capture begins, this callback function will be called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3737-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3737-120">Requirements</span></span>



| <span data-ttu-id="f3737-121">需求</span><span class="sxs-lookup"><span data-stu-id="f3737-121">Requirement</span></span> | <span data-ttu-id="f3737-122">值</span><span class="sxs-lookup"><span data-stu-id="f3737-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3737-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3737-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f3737-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3737-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3737-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3737-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f3737-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3737-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3737-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f3737-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3737-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3737-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3737-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3737-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3737-130">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="f3737-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f3737-131">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="f3737-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





