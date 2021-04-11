---
title: 'WM_CAP_SET_PREVIEW 訊息 (Vfw .h) '
description: WM \_ CAP \_ 集 \_ 預覽訊息會啟用或停用預覽模式。
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106115"
---
# <a name="wm_cap_set_preview-message"></a><span data-ttu-id="6a571-104">WM \_ CAP \_ 設定 \_ 預覽訊息</span><span class="sxs-lookup"><span data-stu-id="6a571-104">WM\_CAP\_SET\_PREVIEW message</span></span>

<span data-ttu-id="6a571-105">**WM \_ CAP \_ 集 \_ 預覽** 訊息會啟用或停用預覽模式。</span><span class="sxs-lookup"><span data-stu-id="6a571-105">The **WM\_CAP\_SET\_PREVIEW** message enables or disables preview mode.</span></span> <span data-ttu-id="6a571-106">在 [預覽] 模式中，畫面格會從捕獲硬體傳輸到系統記憶體，然後使用 GDI 函數顯示在 [捕捉] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="6a571-106">In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions.</span></span> <span data-ttu-id="6a571-107">您可以使用 [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="6a571-107">You can send this message explicitly or by using the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro.</span></span>


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="6a571-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a571-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a571-109"><span id="f"></span><span id="F"></span>*F*</span><span class="sxs-lookup"><span data-stu-id="6a571-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="6a571-110">預覽旗標。</span><span class="sxs-lookup"><span data-stu-id="6a571-110">Preview flag.</span></span> <span data-ttu-id="6a571-111">針對此參數指定 **TRUE** 以啟用預覽模式，或指定 **FALSE** 來停用它。</span><span class="sxs-lookup"><span data-stu-id="6a571-111">Specify **TRUE** for this parameter to enable preview mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a571-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a571-112">Return Value</span></span>

<span data-ttu-id="6a571-113">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6a571-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a571-114">備註</span><span class="sxs-lookup"><span data-stu-id="6a571-114">Remarks</span></span>

<span data-ttu-id="6a571-115">預覽模式會使用大量的 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="6a571-115">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="6a571-116">當另一個應用程式具有焦點時，應用程式可以停用預覽或降低預覽率。</span><span class="sxs-lookup"><span data-stu-id="6a571-116">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="6a571-117">[**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構的 **fLiveWindow** 成員會指出目前是否已啟用預覽模式。</span><span class="sxs-lookup"><span data-stu-id="6a571-117">The **fLiveWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates if preview mode is currently enabled.</span></span>

<span data-ttu-id="6a571-118">啟用預覽模式會自動停用覆迭模式。</span><span class="sxs-lookup"><span data-stu-id="6a571-118">Enabling preview mode automatically disables overlay mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a571-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a571-119">Requirements</span></span>



| <span data-ttu-id="6a571-120">需求</span><span class="sxs-lookup"><span data-stu-id="6a571-120">Requirement</span></span> | <span data-ttu-id="6a571-121">值</span><span class="sxs-lookup"><span data-stu-id="6a571-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6a571-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a571-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6a571-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a571-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6a571-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a571-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6a571-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a571-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a571-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6a571-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a571-127"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a571-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a571-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a571-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a571-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="6a571-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6a571-130">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="6a571-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





