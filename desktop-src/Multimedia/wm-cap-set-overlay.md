---
title: 'WM_CAP_SET_OVERLAY 訊息 (Vfw .h) '
description: WM \_ CAP 集合重迭 \_ 訊息會 \_ 啟用或停用覆迭模式。 在重迭模式中，會使用硬體重迭來顯示影片。 您可以使用 capOverlay 宏明確地傳送此訊息。
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965326"
---
# <a name="wm_cap_set_overlay-message"></a><span data-ttu-id="1552b-106">WM \_ CAP \_ 設定重迭 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="1552b-106">WM\_CAP\_SET\_OVERLAY message</span></span>

<span data-ttu-id="1552b-107">**WM \_ CAP \_ 集合 \_** 重迭訊息會啟用或停用覆迭模式。</span><span class="sxs-lookup"><span data-stu-id="1552b-107">The **WM\_CAP\_SET\_OVERLAY** message enables or disables overlay mode.</span></span> <span data-ttu-id="1552b-108">在重迭模式中，會使用硬體重迭來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="1552b-108">In overlay mode, video is displayed using hardware overlay.</span></span> <span data-ttu-id="1552b-109">您可以使用 [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1552b-109">You can send this message explicitly or by using the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro.</span></span>


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="1552b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1552b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1552b-111"><span id="f"></span><span id="F"></span>*F*</span><span class="sxs-lookup"><span data-stu-id="1552b-111"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="1552b-112">覆迭旗標。</span><span class="sxs-lookup"><span data-stu-id="1552b-112">Overlay flag.</span></span> <span data-ttu-id="1552b-113">請為此參數指定 **TRUE** ，以啟用覆迭模式或 **FALSE** 來停用它。</span><span class="sxs-lookup"><span data-stu-id="1552b-113">Specify **TRUE** for this parameter to enable overlay mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1552b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1552b-114">Return Value</span></span>

<span data-ttu-id="1552b-115">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1552b-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1552b-116">備註</span><span class="sxs-lookup"><span data-stu-id="1552b-116">Remarks</span></span>

<span data-ttu-id="1552b-117">使用覆迭不需要 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="1552b-117">Using an overlay does not require CPU resources.</span></span>

<span data-ttu-id="1552b-118">[**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構的 **fHasOverlay** 成員會指出裝置是否能夠進行重迭。</span><span class="sxs-lookup"><span data-stu-id="1552b-118">The **fHasOverlay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure indicates whether the device is capable of overlay.</span></span> <span data-ttu-id="1552b-119">[**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構的 **fOverlayWindow** 成員會指出目前是否已啟用覆迭模式。</span><span class="sxs-lookup"><span data-stu-id="1552b-119">The **fOverlayWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates whether overlay mode is currently enabled.</span></span>

<span data-ttu-id="1552b-120">啟用覆迭模式會自動停用預覽模式。</span><span class="sxs-lookup"><span data-stu-id="1552b-120">Enabling overlay mode automatically disables preview mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="1552b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1552b-121">Requirements</span></span>



| <span data-ttu-id="1552b-122">需求</span><span class="sxs-lookup"><span data-stu-id="1552b-122">Requirement</span></span> | <span data-ttu-id="1552b-123">值</span><span class="sxs-lookup"><span data-stu-id="1552b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1552b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1552b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1552b-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1552b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1552b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1552b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1552b-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1552b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1552b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1552b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1552b-129"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="1552b-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1552b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1552b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1552b-131">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="1552b-131">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1552b-132">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="1552b-132">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





