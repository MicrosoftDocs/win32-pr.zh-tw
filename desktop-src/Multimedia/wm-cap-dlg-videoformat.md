---
title: 'WM_CAP_DLG_VIDEOFORMAT 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEOFORMAT] 訊息會顯示一個對話方塊，讓使用者可以在其中選取影片格式。'
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934251"
---
# <a name="wm_cap_dlg_videoformat-message"></a><span data-ttu-id="e6999-104">WM \_ CAP \_ DLG \_ VIDEOFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="e6999-104">WM\_CAP\_DLG\_VIDEOFORMAT message</span></span>

<span data-ttu-id="e6999-105">[ **WM \_ CAP \_ DLG \_ VIDEOFORMAT** ] 訊息會顯示一個對話方塊，讓使用者可以在其中選取影片格式。</span><span class="sxs-lookup"><span data-stu-id="e6999-105">The **WM\_CAP\_DLG\_VIDEOFORMAT** message displays a dialog box in which the user can select the video format.</span></span> <span data-ttu-id="e6999-106">您可以使用 [影片格式] 對話方塊來選取影像尺寸、位深度和硬體壓縮選項。</span><span class="sxs-lookup"><span data-stu-id="e6999-106">The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options.</span></span> <span data-ttu-id="e6999-107">您可以使用 [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e6999-107">You can send this message explicitly or by using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="e6999-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6999-108">Return Value</span></span>

<span data-ttu-id="e6999-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e6999-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6999-110">備註</span><span class="sxs-lookup"><span data-stu-id="e6999-110">Remarks</span></span>

<span data-ttu-id="e6999-111">此訊息傳回之後，應用程式可能需要更新 [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) 結構，因為使用者可能已變更影像維度。</span><span class="sxs-lookup"><span data-stu-id="e6999-111">After this message returns, applications might need to update the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure because the user might have changed the image dimensions.</span></span>

<span data-ttu-id="e6999-112">每個 capture 驅動程式的 [影片格式] 對話方塊都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e6999-112">The Video Format dialog box is unique for each capture driver.</span></span> <span data-ttu-id="e6999-113">某些捕獲驅動程式可能不支援 [影片格式] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e6999-113">Some capture drivers might not support a Video Format dialog box.</span></span> <span data-ttu-id="e6999-114">應用程式可以藉由檢查 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)的 **fHasDlgVideoFormat** 成員，判斷 capture 驅動程式是否支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="e6999-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoFormat** member of [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6999-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6999-115">Requirements</span></span>



| <span data-ttu-id="e6999-116">需求</span><span class="sxs-lookup"><span data-stu-id="e6999-116">Requirement</span></span> | <span data-ttu-id="e6999-117">值</span><span class="sxs-lookup"><span data-stu-id="e6999-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6999-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6999-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6999-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6999-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6999-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6999-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6999-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6999-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6999-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e6999-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6999-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6999-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6999-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6999-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6999-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="e6999-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e6999-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="e6999-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





