---
title: DWM 常數和列舉
description: 本節包含桌面視窗管理員 (DWM) Api 中所使用之常數和列舉的相關資訊。
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- 桌面視窗管理員 (DWM) ，參考
- DWM (桌面視窗管理員) ，參考
- 桌面視窗管理員 (DWM) ，常數
- DWM (桌面視窗管理員) ，常數
- 桌面視窗管理員 (DWM) 、列舉
- DWM (桌面視窗管理員) ，列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673656"
---
# <a name="dwm-constants-and-enumerations"></a><span data-ttu-id="3ef9f-109">DWM 常數和列舉</span><span class="sxs-lookup"><span data-stu-id="3ef9f-109">DWM Constants and Enumerations</span></span>

<span data-ttu-id="3ef9f-110">本節包含桌面視窗管理員 (DWM) Api 中所使用之常數和列舉的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-110">This section contains information about the constants and enumerations used in the Desktop Window Manager (DWM) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ef9f-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="3ef9f-111">In this section</span></span>



| <span data-ttu-id="3ef9f-112">主題</span><span class="sxs-lookup"><span data-stu-id="3ef9f-112">Topic</span></span>                                                                                     | <span data-ttu-id="3ef9f-113">描述</span><span class="sxs-lookup"><span data-stu-id="3ef9f-113">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ef9f-114">**常數模糊背後常數**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-114">**DWM Blur Behind Constants**</span></span>](dwm-bb-constants.md)<br/>                          | <span data-ttu-id="3ef9f-115">[**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)結構用來指出其中一個成員包含有效資訊的旗標。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-115">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span><br/>                                                                    |
| [<span data-ttu-id="3ef9f-116">**DWM 啟用組合常數**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-116">**DWM Enable Composition Constants**</span></span>](dwm-ec-constants.md)<br/>                   | <span data-ttu-id="3ef9f-117">[**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)函數用來變更 DWM 組合狀態的旗標。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-117">Flags used by the [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  function to change the state of DWM composition.</span></span><br/>                                                                             |
| [<span data-ttu-id="3ef9f-118">**DWM \_ 來源 \_ 畫面格 \_ 取樣**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-118">**DWM\_SOURCE\_FRAME\_SAMPLING**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | <span data-ttu-id="3ef9f-119">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters)函數用來指定框架取樣類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-119">Flags used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function to specify the frame sampling type.</span></span><br/>                                                                            |
| [<span data-ttu-id="3ef9f-120">**DWM 索引標籤 \_ \_ 視窗 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-120">**DWM\_TAB\_WINDOW\_REQUIREMENTS**</span></span>](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | <span data-ttu-id="3ef9f-121">由 DwmGetUnmetTabRequirements 傳回，指出視窗將索引標籤放在應用程式標題列中所需的需求。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-121">Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.</span></span><br/>                                                                    |
| [<span data-ttu-id="3ef9f-122">**DWM \_ TNP 常數**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-122">**DWM\_TNP Constants**</span></span>](dwm-tnp-constants.md)<br/>                                | <span data-ttu-id="3ef9f-123">[**DWM \_ 縮圖 \_ 屬性**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)結構所使用的旗標，用來指出其中一個成員包含有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-123">Flags used by the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) structure to indicate which of its members contain valid information.</span></span><br/>                                               |
| [<span data-ttu-id="3ef9f-124">**DWMFLIP3DWINDOWPOLICY**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-124">**DWMFLIP3DWINDOWPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | <span data-ttu-id="3ef9f-125">[**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)函數用來指定 Flip3D 視窗原則的旗標。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-125">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the Flip3D window policy.</span></span><br/>                                                                               |
| [<span data-ttu-id="3ef9f-126">**DWMNCRENDERINGPOLICY**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-126">**DWMNCRENDERINGPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | <span data-ttu-id="3ef9f-127">[**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)函數用來指定非工作區轉譯原則的旗標。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-127">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the non-client area rendering policy.</span></span><br/>                                                                   |
| [<span data-ttu-id="3ef9f-128">**DWMTRANSITION \_ OWNEDWINDOW \_ 目標**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-128">**DWMTRANSITION\_OWNEDWINDOW\_TARGET**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | <span data-ttu-id="3ef9f-129">識別目標。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-129">Identifies the target.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="3ef9f-130">**DWMWINDOWATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-130">**DWMWINDOWATTRIBUTE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | <span data-ttu-id="3ef9f-131">[**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute)和 [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)函數用來指定非用戶端轉譯之視窗屬性的旗標。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-131">Flags used by the [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions to specify window attributes for non-client rendering.</span></span><br/> |
| [<span data-ttu-id="3ef9f-132">**手勢 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-132">**GESTURE\_TYPE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | <span data-ttu-id="3ef9f-133">識別在 [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture)中指定的手勢類型。</span><span class="sxs-lookup"><span data-stu-id="3ef9f-133">Identifies the gesture type specified in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span></span><br/>                                                                                                               |



 

 

 





