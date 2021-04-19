---
title: 'WM_CAP_PAL_AUTOCREATE 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL \_ 會自動建立訊息要求 capture 驅動程式範例影片框架，並自動建立新的調色板。 您可以使用 capPaletteAuto 宏明確地傳送此訊息。
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969575"
---
# <a name="wm_cap_pal_autocreate-message"></a><span data-ttu-id="dc4bb-105">WM \_ CAP \_ PAL 自動顯示 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="dc4bb-105">WM\_CAP\_PAL\_AUTOCREATE message</span></span>

<span data-ttu-id="dc4bb-106">**WM \_ CAP \_ PAL \_** 會自動建立訊息要求 capture 驅動程式範例影片框架，並自動建立新的調色板。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-106">The **WM\_CAP\_PAL\_AUTOCREATE** message requests that the capture driver sample video frames and automatically create a new palette.</span></span> <span data-ttu-id="dc4bb-107">您可以使用 [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-107">You can send this message explicitly or by using the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) macro.</span></span>


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="dc4bb-108">參數</span><span class="sxs-lookup"><span data-stu-id="dc4bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc4bb-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframe*</span><span class="sxs-lookup"><span data-stu-id="dc4bb-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="dc4bb-110">要取樣的框架數目。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-110">Number of frames to sample.</span></span>

</dd> <dt>

<span data-ttu-id="dc4bb-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="dc4bb-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="dc4bb-112">調色板中的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-112">Number of colors in the palette.</span></span> <span data-ttu-id="dc4bb-113">此參數的最大值為256。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-113">The maximum value for this parameter is 256.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc4bb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc4bb-114">Return Value</span></span>

<span data-ttu-id="dc4bb-115">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="dc4bb-116">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-116">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc4bb-117">備註</span><span class="sxs-lookup"><span data-stu-id="dc4bb-117">Remarks</span></span>

<span data-ttu-id="dc4bb-118">取樣的影片順序應該包含您在 [調色板] 中所需的所有色彩。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-118">The sampled video sequence should include all the colors you want in the palette.</span></span> <span data-ttu-id="dc4bb-119">若要取得最佳的調色板，您可能必須取樣整個序列，而不是它的一部分。</span><span class="sxs-lookup"><span data-stu-id="dc4bb-119">To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4bb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc4bb-120">Requirements</span></span>



| <span data-ttu-id="dc4bb-121">需求</span><span class="sxs-lookup"><span data-stu-id="dc4bb-121">Requirement</span></span> | <span data-ttu-id="dc4bb-122">值</span><span class="sxs-lookup"><span data-stu-id="dc4bb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dc4bb-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc4bb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4bb-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc4bb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dc4bb-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc4bb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4bb-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc4bb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dc4bb-127">標頭</span><span class="sxs-lookup"><span data-stu-id="dc4bb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc4bb-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc4bb-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc4bb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc4bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4bb-130">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="dc4bb-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="dc4bb-131">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="dc4bb-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





