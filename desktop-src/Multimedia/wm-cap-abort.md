---
title: 'WM_CAP_ABORT 訊息 (Vfw .h) '
description: WM \_ CAP \_ ABORT 訊息會停止捕捉作業。
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508539"
---
# <a name="wm_cap_abort-message"></a><span data-ttu-id="78658-104">WM \_ CAP \_ 中止訊息</span><span class="sxs-lookup"><span data-stu-id="78658-104">WM\_CAP\_ABORT message</span></span>

<span data-ttu-id="78658-105">**WM \_ CAP \_ ABORT** 訊息會停止捕捉作業。</span><span class="sxs-lookup"><span data-stu-id="78658-105">The **WM\_CAP\_ABORT** message stops the capture operation.</span></span> <span data-ttu-id="78658-106">在步驟捕捉的案例中，會將收集到 **WM \_ CAP \_ 中止** 訊息點的影像資料保留在 capture 檔案中，但不會捕獲音訊。</span><span class="sxs-lookup"><span data-stu-id="78658-106">In the case of step capture, the image data collected up to the point of the **WM\_CAP\_ABORT** message will be retained in the capture file, but audio will not be captured.</span></span> <span data-ttu-id="78658-107">您可以使用 [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="78658-107">You can send this message explicitly or by using the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro.</span></span>


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="78658-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="78658-108">Return Value</span></span>

<span data-ttu-id="78658-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="78658-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="78658-110">備註</span><span class="sxs-lookup"><span data-stu-id="78658-110">Remarks</span></span>

<span data-ttu-id="78658-111">捕捉作業必須採用此訊息。</span><span class="sxs-lookup"><span data-stu-id="78658-111">The capture operation must yield to use this message.</span></span>

<span data-ttu-id="78658-112">使用 [**WM \_ CAP \_ 停止**](wm-cap-stop.md) 訊息，在目前的位置停止步驟捕捉，然後捕獲音訊。</span><span class="sxs-lookup"><span data-stu-id="78658-112">Use the [**WM\_CAP\_STOP**](wm-cap-stop.md) message to halt step capture at the current position, and then capture audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="78658-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="78658-113">Requirements</span></span>



| <span data-ttu-id="78658-114">需求</span><span class="sxs-lookup"><span data-stu-id="78658-114">Requirement</span></span> | <span data-ttu-id="78658-115">值</span><span class="sxs-lookup"><span data-stu-id="78658-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78658-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78658-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78658-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78658-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="78658-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78658-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78658-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78658-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="78658-120">標頭</span><span class="sxs-lookup"><span data-stu-id="78658-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78658-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="78658-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78658-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78658-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78658-123">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="78658-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="78658-124">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="78658-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





