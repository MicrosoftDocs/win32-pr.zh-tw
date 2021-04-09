---
title: DWM 結構
description: 本節包含桌面視窗管理員 (DWM) 結構的相關資訊。
ms.assetid: 26b36617-54c2-405a-9a7d-bd86fefa94b6
keywords:
- 桌面視窗管理員 (DWM) ，參考
- DWM (桌面視窗管理員) ，參考
- 桌面視窗管理員 (DWM) 、結構
- DWM (桌面視窗管理員) 、結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f212d248c0f70cfd51e6e47b2d37c89d24f630b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021480"
---
# <a name="dwm-structures"></a><span data-ttu-id="028ad-107">DWM 結構</span><span class="sxs-lookup"><span data-stu-id="028ad-107">DWM Structures</span></span>

<span data-ttu-id="028ad-108">本節包含桌面視窗管理員 (DWM) 結構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="028ad-108">This section contains information about the Desktop Window Manager (DWM) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="028ad-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="028ad-109">In this section</span></span>



| <span data-ttu-id="028ad-110">主題</span><span class="sxs-lookup"><span data-stu-id="028ad-110">Topic</span></span>                                                                     | <span data-ttu-id="028ad-111">描述</span><span class="sxs-lookup"><span data-stu-id="028ad-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="028ad-112">**DWM \_ BLURBEHIND**</span><span class="sxs-lookup"><span data-stu-id="028ad-112">**DWM\_BLURBEHIND**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)<br/>                      | <span data-ttu-id="028ad-113">指定 DWM 模糊後屬性。</span><span class="sxs-lookup"><span data-stu-id="028ad-113">Specifies DWM blur-behind properties.</span></span> <span data-ttu-id="028ad-114">由 [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="028ad-114">Used by the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function.</span></span><br/>                     |
| [<span data-ttu-id="028ad-115">**DWM \_ 存在 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="028ad-115">**DWM\_PRESENT\_PARAMETERS**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_present_parameters)<br/>     | <span data-ttu-id="028ad-116">指定框架組合的 DWM 影片框架參數。</span><span class="sxs-lookup"><span data-stu-id="028ad-116">Specifies DWM video frame parameters for frame composition.</span></span> <span data-ttu-id="028ad-117">由 [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="028ad-117">Used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function.</span></span><br/>   |
| [<span data-ttu-id="028ad-118">**DWM \_ 縮圖 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="028ad-118">**DWM\_THUMBNAIL\_PROPERTIES**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)<br/> | <span data-ttu-id="028ad-119">指定 DWM 縮圖屬性。</span><span class="sxs-lookup"><span data-stu-id="028ad-119">Specifies DWM thumbnail properties.</span></span> <span data-ttu-id="028ad-120">由 [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="028ad-120">Used by the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function.</span></span><br/>                 |
| [<span data-ttu-id="028ad-121">**DWM \_ 計時 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="028ad-121">**DWM\_TIMING\_INFO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_timing_info)<br/>                   | <span data-ttu-id="028ad-122">指定 DWM 組合計時資訊。</span><span class="sxs-lookup"><span data-stu-id="028ad-122">Specifies DWM composition timing information.</span></span> <span data-ttu-id="028ad-123">由 [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="028ad-123">Used by the [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) function.</span></span><br/>         |
| [<span data-ttu-id="028ad-124">**MilMatrix3x2D**</span><span class="sxs-lookup"><span data-stu-id="028ad-124">**MilMatrix3x2D**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-milmatrix3x2d)<br/>                         | <span data-ttu-id="028ad-125">指定描述轉換的3x2 矩陣。</span><span class="sxs-lookup"><span data-stu-id="028ad-125">Specifies a 3x2 matrix that describes a transform.</span></span> <br/>                                                                                            |
| [<span data-ttu-id="028ad-126">**不帶正負號 \_ 比例**</span><span class="sxs-lookup"><span data-stu-id="028ad-126">**UNSIGNED\_RATIO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-unsigned_ratio)<br/>                      | <span data-ttu-id="028ad-127">定義 DWM Api 所使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="028ad-127">Defines a data type used by the DWM APIs.</span></span> <span data-ttu-id="028ad-128">它代表一般比例，而且即使是在單一 API 內，也會用於不同的用途和單位。</span><span class="sxs-lookup"><span data-stu-id="028ad-128">It represents a generic ratio and is used for different purposes and units even within a single API.</span></span><br/> |



 

 

 





