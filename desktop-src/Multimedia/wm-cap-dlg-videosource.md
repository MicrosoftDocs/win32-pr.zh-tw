---
title: 'WM_CAP_DLG_VIDEOSOURCE 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEOSOURCE] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中控制影片來源。'
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464977"
---
# <a name="wm_cap_dlg_videosource-message"></a><span data-ttu-id="b9889-104">WM \_ CAP \_ DLG \_ VIDEOSOURCE 訊息</span><span class="sxs-lookup"><span data-stu-id="b9889-104">WM\_CAP\_DLG\_VIDEOSOURCE message</span></span>

<span data-ttu-id="b9889-105">[ **WM \_ CAP \_ DLG \_ VIDEOSOURCE** ] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中控制影片來源。</span><span class="sxs-lookup"><span data-stu-id="b9889-105">The **WM\_CAP\_DLG\_VIDEOSOURCE** message displays a dialog box in which the user can control the video source.</span></span> <span data-ttu-id="b9889-106">[影片來源] 對話方塊可能包含選取輸入來源的控制項;改變影像的色調、對比、亮度;並在將影像數位化至框架緩衝區之前修改影片品質。</span><span class="sxs-lookup"><span data-stu-id="b9889-106">The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer.</span></span> <span data-ttu-id="b9889-107">您可以使用 [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b9889-107">You can send this message explicitly or by using the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="b9889-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9889-108">Return Value</span></span>

<span data-ttu-id="b9889-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b9889-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9889-110">備註</span><span class="sxs-lookup"><span data-stu-id="b9889-110">Remarks</span></span>

<span data-ttu-id="b9889-111">[影片來源] 對話方塊對每個 capture 驅動程式而言都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b9889-111">The Video Source dialog box is unique for each capture driver.</span></span> <span data-ttu-id="b9889-112">某些捕獲驅動程式可能不支援 [影片來源] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b9889-112">Some capture drivers might not support a Video Source dialog box.</span></span> <span data-ttu-id="b9889-113">應用程式可以藉由檢查 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構的 **fHasDlgVideoSource** 成員，判斷 capture 驅動程式是否支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="b9889-113">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoSource** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9889-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9889-114">Requirements</span></span>



| <span data-ttu-id="b9889-115">需求</span><span class="sxs-lookup"><span data-stu-id="b9889-115">Requirement</span></span> | <span data-ttu-id="b9889-116">值</span><span class="sxs-lookup"><span data-stu-id="b9889-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b9889-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9889-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b9889-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9889-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b9889-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9889-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b9889-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9889-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b9889-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b9889-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9889-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9889-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9889-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9889-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9889-124">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="b9889-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b9889-125">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="b9889-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





