---
title: 'WM_CAP_DLG_VIDEODISPLAY 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEODISPLAY] 訊息會顯示一個對話方塊，讓使用者可以在其中設定或調整影片輸出。'
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934344"
---
# <a name="wm_cap_dlg_videodisplay-message"></a><span data-ttu-id="42bdd-104">WM \_ CAP \_ DLG \_ VIDEODISPLAY 訊息</span><span class="sxs-lookup"><span data-stu-id="42bdd-104">WM\_CAP\_DLG\_VIDEODISPLAY message</span></span>

<span data-ttu-id="42bdd-105">[ **WM \_ CAP \_ DLG \_ VIDEODISPLAY** ] 訊息會顯示一個對話方塊，讓使用者可以在其中設定或調整影片輸出。</span><span class="sxs-lookup"><span data-stu-id="42bdd-105">The **WM\_CAP\_DLG\_VIDEODISPLAY** message displays a dialog box in which the user can set or adjust the video output.</span></span> <span data-ttu-id="42bdd-106">此對話方塊可能包含影響所顯示影像的色調、對比和亮度，以及按鍵色彩對齊的控制項。</span><span class="sxs-lookup"><span data-stu-id="42bdd-106">This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment.</span></span> <span data-ttu-id="42bdd-107">您可以使用 [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="42bdd-107">You can send this message explicitly or by using the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro.</span></span>


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="42bdd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="42bdd-108">Return Value</span></span>

<span data-ttu-id="42bdd-109">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="42bdd-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="42bdd-110">備註</span><span class="sxs-lookup"><span data-stu-id="42bdd-110">Remarks</span></span>

<span data-ttu-id="42bdd-111">此對話方塊中的控制項不會影響數位化的影片資料。它們只會影響視訊訊號的輸出或重新顯示。</span><span class="sxs-lookup"><span data-stu-id="42bdd-111">The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.</span></span>

<span data-ttu-id="42bdd-112">[影片顯示] 對話方塊對每個 capture 驅動程式而言都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="42bdd-112">The Video Display dialog box is unique for each capture driver.</span></span> <span data-ttu-id="42bdd-113">某些捕獲驅動程式可能不支援 [影片顯示] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="42bdd-113">Some capture drivers might not support a Video Display dialog box.</span></span> <span data-ttu-id="42bdd-114">應用程式可以藉由檢查 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構的 **fHasDlgVideoDisplay** 成員，判斷 capture 驅動程式是否支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="42bdd-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoDisplay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="42bdd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="42bdd-115">Requirements</span></span>



| <span data-ttu-id="42bdd-116">需求</span><span class="sxs-lookup"><span data-stu-id="42bdd-116">Requirement</span></span> | <span data-ttu-id="42bdd-117">值</span><span class="sxs-lookup"><span data-stu-id="42bdd-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="42bdd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42bdd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42bdd-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42bdd-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="42bdd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42bdd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42bdd-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42bdd-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="42bdd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="42bdd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42bdd-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="42bdd-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42bdd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42bdd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42bdd-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="42bdd-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="42bdd-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="42bdd-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





