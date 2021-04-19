---
title: 'WM_CAP_SET_CALLBACK_FRAME 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 回呼 \_ 框架訊息會在應用程式中設定預覽回撥函式。 當捕捉視窗捕獲預覽畫面時，AVICap 會呼叫這個程式。 您可以使用 capSetCallbackOnFrame 宏明確地傳送此訊息。
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966320"
---
# <a name="wm_cap_set_callback_frame-message"></a><span data-ttu-id="2b892-106">WM \_ CAP \_ 設定 \_ 回呼 \_ 框架訊息</span><span class="sxs-lookup"><span data-stu-id="2b892-106">WM\_CAP\_SET\_CALLBACK\_FRAME message</span></span>

<span data-ttu-id="2b892-107">**WM \_ CAP \_ 設定 \_ 回呼 \_ 框架** 訊息會在應用程式中設定預覽回撥函式。</span><span class="sxs-lookup"><span data-stu-id="2b892-107">The **WM\_CAP\_SET\_CALLBACK\_FRAME** message sets a preview callback function in the application.</span></span> <span data-ttu-id="2b892-108">當捕捉視窗捕獲預覽畫面時，AVICap 會呼叫這個程式。</span><span class="sxs-lookup"><span data-stu-id="2b892-108">AVICap calls this procedure when the capture window captures preview frames.</span></span> <span data-ttu-id="2b892-109">您可以使用 [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2b892-109">You can send this message explicitly or by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="2b892-110">參數</span><span class="sxs-lookup"><span data-stu-id="2b892-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b892-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="2b892-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="2b892-112">預覽回呼函式的指標，其類型為 [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)。</span><span class="sxs-lookup"><span data-stu-id="2b892-112">Pointer to the preview callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="2b892-113">針對此參數指定 **Null** ，以停用先前安裝的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="2b892-113">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b892-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b892-114">Return Value</span></span>

<span data-ttu-id="2b892-115">如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2b892-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b892-116">備註</span><span class="sxs-lookup"><span data-stu-id="2b892-116">Remarks</span></span>

<span data-ttu-id="2b892-117">捕捉視窗會先呼叫回呼函式，再顯示預覽框架。</span><span class="sxs-lookup"><span data-stu-id="2b892-117">The capture window calls the callback function before displaying preview frames.</span></span> <span data-ttu-id="2b892-118">這可讓應用程式視需要修改框架。</span><span class="sxs-lookup"><span data-stu-id="2b892-118">This allows an application to modify the frame if desired.</span></span> <span data-ttu-id="2b892-119">串流處理影片捕獲期間未使用此回呼函數。</span><span class="sxs-lookup"><span data-stu-id="2b892-119">This callback function is not used during streaming video capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b892-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b892-120">Requirements</span></span>



| <span data-ttu-id="2b892-121">需求</span><span class="sxs-lookup"><span data-stu-id="2b892-121">Requirement</span></span> | <span data-ttu-id="2b892-122">值</span><span class="sxs-lookup"><span data-stu-id="2b892-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2b892-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b892-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b892-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b892-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2b892-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b892-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b892-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b892-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b892-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2b892-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b892-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b892-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b892-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b892-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b892-130">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="2b892-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2b892-131">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="2b892-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





