---
title: 'WM_CAP_SET_CALLBACK_ERROR 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤訊息會在用戶端應用程式中設定錯誤回呼函數。 當發生錯誤時，AVICap 會呼叫這個程式。 您可以使用 capSetCallbackOnError 宏明確地傳送此訊息。
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465661"
---
# <a name="wm_cap_set_callback_error-message"></a><span data-ttu-id="daec1-106">WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="daec1-106">WM\_CAP\_SET\_CALLBACK\_ERROR message</span></span>

<span data-ttu-id="daec1-107">**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤** 訊息會在用戶端應用程式中設定錯誤回呼函數。</span><span class="sxs-lookup"><span data-stu-id="daec1-107">The **WM\_CAP\_SET\_CALLBACK\_ERROR** message sets an error callback function in the client application.</span></span> <span data-ttu-id="daec1-108">當發生錯誤時，AVICap 會呼叫這個程式。</span><span class="sxs-lookup"><span data-stu-id="daec1-108">AVICap calls this procedure when errors occur.</span></span> <span data-ttu-id="daec1-109">您可以使用 [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="daec1-109">You can send this message explicitly or by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="daec1-110">參數</span><span class="sxs-lookup"><span data-stu-id="daec1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daec1-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="daec1-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="daec1-112">錯誤回呼函數的指標，其類型為 [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)。</span><span class="sxs-lookup"><span data-stu-id="daec1-112">Pointer to the error callback function, of type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span></span> <span data-ttu-id="daec1-113">針對此參數指定 **Null** ，以停用先前安裝的錯誤回呼函數。</span><span class="sxs-lookup"><span data-stu-id="daec1-113">Specify **NULL** for this parameter to disable a previously installed error callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daec1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="daec1-114">Return Value</span></span>

<span data-ttu-id="daec1-115">如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="daec1-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="daec1-116">備註</span><span class="sxs-lookup"><span data-stu-id="daec1-116">Remarks</span></span>

<span data-ttu-id="daec1-117">應用程式可以選擇性地設定錯誤回呼函數。</span><span class="sxs-lookup"><span data-stu-id="daec1-117">Applications can optionally set an error callback function.</span></span> <span data-ttu-id="daec1-118">如果設定，AVICap 會在下列情況下呼叫錯誤程式：</span><span class="sxs-lookup"><span data-stu-id="daec1-118">If set, AVICap calls the error procedure in the following situations:</span></span>

-   <span data-ttu-id="daec1-119">磁碟已滿。</span><span class="sxs-lookup"><span data-stu-id="daec1-119">The disk is full.</span></span>
-   <span data-ttu-id="daec1-120">無法使用 capture 驅動程式連接捕獲視窗。</span><span class="sxs-lookup"><span data-stu-id="daec1-120">A capture window cannot be connected with a capture driver.</span></span>
-   <span data-ttu-id="daec1-121">無法開啟波形音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="daec1-121">A waveform-audio device cannot be opened.</span></span>
-   <span data-ttu-id="daec1-122">在 capture 期間卸載的框架數目超過指定的百分比。</span><span class="sxs-lookup"><span data-stu-id="daec1-122">The number of frames dropped during capture exceeds the specified percentage.</span></span>
-   <span data-ttu-id="daec1-123">由於有垂直的同步處理中斷問題，因此無法捕獲框架。</span><span class="sxs-lookup"><span data-stu-id="daec1-123">The frames cannot be captured due to vertical synchronization interrupt problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="daec1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="daec1-124">Requirements</span></span>



| <span data-ttu-id="daec1-125">需求</span><span class="sxs-lookup"><span data-stu-id="daec1-125">Requirement</span></span> | <span data-ttu-id="daec1-126">值</span><span class="sxs-lookup"><span data-stu-id="daec1-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="daec1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="daec1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="daec1-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="daec1-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="daec1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="daec1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="daec1-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="daec1-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="daec1-131">標頭</span><span class="sxs-lookup"><span data-stu-id="daec1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="daec1-132"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="daec1-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daec1-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="daec1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daec1-134">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="daec1-134">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="daec1-135">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="daec1-135">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





