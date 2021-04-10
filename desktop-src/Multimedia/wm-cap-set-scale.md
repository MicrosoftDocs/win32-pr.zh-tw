---
title: 'WM_CAP_SET_SCALE 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 規模訊息可啟用或停用預覽版影片影像的縮放比例。
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106110"
---
# <a name="wm_cap_set_scale-message"></a><span data-ttu-id="762f5-104">WM \_ CAP \_ 設定 \_ 調整訊息</span><span class="sxs-lookup"><span data-stu-id="762f5-104">WM\_CAP\_SET\_SCALE message</span></span>

<span data-ttu-id="762f5-105">**WM \_ CAP \_ 設定 \_ 規模** 訊息可啟用或停用預覽版影片影像的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="762f5-105">The **WM\_CAP\_SET\_SCALE** message enables or disables scaling of the preview video images.</span></span> <span data-ttu-id="762f5-106">如果已啟用縮放，則會將已捕捉的影片畫面延展至 [捕獲] 視窗的維度。</span><span class="sxs-lookup"><span data-stu-id="762f5-106">If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="762f5-107">您可以使用 [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="762f5-107">You can send this message explicitly or by using the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro.</span></span>


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="762f5-108">參數</span><span class="sxs-lookup"><span data-stu-id="762f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762f5-109"><span id="f"></span><span id="F"></span>*F*</span><span class="sxs-lookup"><span data-stu-id="762f5-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="762f5-110">預覽調整旗標。</span><span class="sxs-lookup"><span data-stu-id="762f5-110">Preview scaling flag.</span></span> <span data-ttu-id="762f5-111">針對此參數指定 **TRUE** ，以將預覽框架延展至 [捕獲] 視窗的大小，或為 **FALSE** 以其自然大小顯示。</span><span class="sxs-lookup"><span data-stu-id="762f5-111">Specify **TRUE** for this parameter to stretch preview frames to the size of the capture window or **FALSE** to display them at their natural size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762f5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="762f5-112">Return Value</span></span>

<span data-ttu-id="762f5-113">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="762f5-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="762f5-114">備註</span><span class="sxs-lookup"><span data-stu-id="762f5-114">Remarks</span></span>

<span data-ttu-id="762f5-115">調整預覽影像會控制捕捉視窗內所捕獲框架的立即呈現。</span><span class="sxs-lookup"><span data-stu-id="762f5-115">Scaling preview images controls the immediate presentation of captured frames within the capture window.</span></span> <span data-ttu-id="762f5-116">它不會影響儲存至檔案的框架大小。</span><span class="sxs-lookup"><span data-stu-id="762f5-116">It has no effect on the size of the frames saved to file.</span></span>

<span data-ttu-id="762f5-117">使用重迭來顯示框架緩衝區中的影片時，縮放比例沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="762f5-117">Scaling has no effect when using overlay to display video in the frame buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="762f5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="762f5-118">Requirements</span></span>



| <span data-ttu-id="762f5-119">需求</span><span class="sxs-lookup"><span data-stu-id="762f5-119">Requirement</span></span> | <span data-ttu-id="762f5-120">值</span><span class="sxs-lookup"><span data-stu-id="762f5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="762f5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="762f5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="762f5-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="762f5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="762f5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="762f5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="762f5-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="762f5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="762f5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="762f5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="762f5-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="762f5-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="762f5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="762f5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762f5-128">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="762f5-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="762f5-129">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="762f5-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





