---
title: 'WM_CAP_SET_CALLBACK_STATUS 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態訊息會在應用程式中設定狀態回呼函數。 當捕捉視窗狀態變更時，AVICap 會呼叫這個程式。 您可以使用 capSetCallbackOnStatus 宏明確地傳送此訊息。
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464492"
---
# <a name="wm_cap_set_callback_status-message"></a><span data-ttu-id="25908-106">WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態訊息</span><span class="sxs-lookup"><span data-stu-id="25908-106">WM\_CAP\_SET\_CALLBACK\_STATUS message</span></span>

<span data-ttu-id="25908-107">**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態** 消息會在應用程式中設定狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="25908-107">The **WM\_CAP\_SET\_CALLBACK\_STATUS** message sets a status callback function in the application.</span></span> <span data-ttu-id="25908-108">當捕捉視窗狀態變更時，AVICap 會呼叫這個程式。</span><span class="sxs-lookup"><span data-stu-id="25908-108">AVICap calls this procedure whenever the capture window status changes.</span></span> <span data-ttu-id="25908-109">您可以使用 [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="25908-109">You can send this message explicitly or by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="25908-110">參數</span><span class="sxs-lookup"><span data-stu-id="25908-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25908-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="25908-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="25908-112">狀態回呼函數的指標，其類型為 [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)。</span><span class="sxs-lookup"><span data-stu-id="25908-112">Pointer to the status callback function, of type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span></span> <span data-ttu-id="25908-113">針對此參數指定 **Null** ，以停用先前安裝的狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="25908-113">Specify **NULL** for this parameter to disable a previously installed status callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25908-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="25908-114">Return Value</span></span>

<span data-ttu-id="25908-115">如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="25908-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="25908-116">備註</span><span class="sxs-lookup"><span data-stu-id="25908-116">Remarks</span></span>

<span data-ttu-id="25908-117">應用程式可以選擇性地設定狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="25908-117">Applications can optionally set a status callback function.</span></span> <span data-ttu-id="25908-118">如果設定，AVICap 會在下列情況下呼叫此程式：</span><span class="sxs-lookup"><span data-stu-id="25908-118">If set, AVICap calls this procedure in the following situations:</span></span>

-   <span data-ttu-id="25908-119">已完成捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="25908-119">A capture session is completed.</span></span>
-   <span data-ttu-id="25908-120">Capture 驅動程式已成功連線到捕捉視窗。</span><span class="sxs-lookup"><span data-stu-id="25908-120">A capture driver successfully connected to a capture window.</span></span>
-   <span data-ttu-id="25908-121">建立最佳的調色板。</span><span class="sxs-lookup"><span data-stu-id="25908-121">An optimal palette is created.</span></span>
-   <span data-ttu-id="25908-122">報告的已捕獲框架數目。</span><span class="sxs-lookup"><span data-stu-id="25908-122">The number of captured frames is reported.</span></span>

## <a name="requirements"></a><span data-ttu-id="25908-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="25908-123">Requirements</span></span>



| <span data-ttu-id="25908-124">需求</span><span class="sxs-lookup"><span data-stu-id="25908-124">Requirement</span></span> | <span data-ttu-id="25908-125">值</span><span class="sxs-lookup"><span data-stu-id="25908-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="25908-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25908-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25908-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25908-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="25908-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25908-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25908-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25908-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="25908-130">標頭</span><span class="sxs-lookup"><span data-stu-id="25908-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="25908-131"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="25908-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25908-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25908-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25908-133">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="25908-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="25908-134">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="25908-134">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





