---
title: 'WM_CAP_PAL_MANUALCREATE 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL \_ MANUALCREATE 訊息要求 capture 驅動程式手動取樣影片畫面，並建立新的調色板。 您可以使用 capPaletteManual 宏明確地傳送此訊息。
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685772"
---
# <a name="wm_cap_pal_manualcreate-message"></a><span data-ttu-id="f86b9-105">WM \_ CAP \_ PAL \_ MANUALCREATE 訊息</span><span class="sxs-lookup"><span data-stu-id="f86b9-105">WM\_CAP\_PAL\_MANUALCREATE message</span></span>

<span data-ttu-id="f86b9-106">**WM \_ CAP \_ PAL \_ MANUALCREATE** 訊息要求 capture 驅動程式手動取樣影片畫面，並建立新的調色板。</span><span class="sxs-lookup"><span data-stu-id="f86b9-106">The **WM\_CAP\_PAL\_MANUALCREATE** message requests that the capture driver manually sample video frames and create a new palette.</span></span> <span data-ttu-id="f86b9-107">您可以使用 [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f86b9-107">You can send this message explicitly or by using the [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro.</span></span>


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="f86b9-108">參數</span><span class="sxs-lookup"><span data-stu-id="f86b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f86b9-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span><span class="sxs-lookup"><span data-stu-id="f86b9-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span></span>
</dt> <dd>

<span data-ttu-id="f86b9-110">選用區長條圖旗標。</span><span class="sxs-lookup"><span data-stu-id="f86b9-110">Palette histogram flag.</span></span> <span data-ttu-id="f86b9-111">針對建立最佳調色板中包含的每個畫面格，將此參數設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f86b9-111">Set this parameter to **TRUE** for each frame included in creating the optimal palette.</span></span> <span data-ttu-id="f86b9-112">在收集最後一個畫面格之後，請將此參數設定為 **FALSE** ，以計算最佳的選擇區，並將它傳送至 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f86b9-112">After the last frame has been collected, set this parameter to **FALSE** to calculate the optimal palette and send it to the capture driver.</span></span>

</dd> <dt>

<span data-ttu-id="f86b9-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="f86b9-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="f86b9-114">調色板中的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="f86b9-114">Number of colors in the palette.</span></span> <span data-ttu-id="f86b9-115">此參數的最大值為256。</span><span class="sxs-lookup"><span data-stu-id="f86b9-115">The maximum value for this parameter is 256.</span></span> <span data-ttu-id="f86b9-116">只有在序列中的第一個框架收集期間，才會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f86b9-116">This value is used only during collection of the first frame in a sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f86b9-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f86b9-117">Return Value</span></span>

<span data-ttu-id="f86b9-118">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f86b9-118">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="f86b9-119">如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。</span><span class="sxs-lookup"><span data-stu-id="f86b9-119">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f86b9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f86b9-120">Requirements</span></span>



| <span data-ttu-id="f86b9-121">需求</span><span class="sxs-lookup"><span data-stu-id="f86b9-121">Requirement</span></span> | <span data-ttu-id="f86b9-122">值</span><span class="sxs-lookup"><span data-stu-id="f86b9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f86b9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f86b9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f86b9-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f86b9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f86b9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f86b9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f86b9-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f86b9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f86b9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f86b9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f86b9-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="f86b9-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f86b9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f86b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86b9-130">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="f86b9-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f86b9-131">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="f86b9-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





