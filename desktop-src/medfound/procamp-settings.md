---
description: 這些旗標會定義影片處理器 (ProcAmp) 設定。
ms.assetid: 60d97b9e-d77c-4e53-94ea-ebd59c2601df
title: 'ProcAmp 設定 (Dxva2api .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0181d7491d948a4ec4219ada4241397b8a721b0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979753"
---
# <a name="procamp-settings"></a><span data-ttu-id="ac9ad-103">ProcAmp 設定</span><span class="sxs-lookup"><span data-stu-id="ac9ad-103">ProcAmp Settings</span></span>

<span data-ttu-id="ac9ad-104">這些旗標會定義影片處理器 (ProcAmp) 設定。</span><span class="sxs-lookup"><span data-stu-id="ac9ad-104">These flags define video processor (ProcAmp) settings.</span></span>



| <span data-ttu-id="ac9ad-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="ac9ad-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="ac9ad-106">Description</span><span class="sxs-lookup"><span data-stu-id="ac9ad-106">Description</span></span>           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------|
| <span id="DXVA2_ProcAmp_None"></span><span id="dxva2_procamp_none"></span><span id="DXVA2_PROCAMP_NONE"></span><dl> <span data-ttu-id="ac9ad-107"><dt>**DXVA2 \_ProcAmp \_ 無**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="ac9ad-107"><dt>**DXVA2\_ProcAmp\_None**</dt> <dt>0x0000</dt></span></span> </dl>                         | <span data-ttu-id="ac9ad-108">無</span><span class="sxs-lookup"><span data-stu-id="ac9ad-108">None</span></span><br/>       |
| <span id="DXVA2_ProcAmp_Brightness"></span><span id="dxva2_procamp_brightness"></span><span id="DXVA2_PROCAMP_BRIGHTNESS"></span><dl> <span data-ttu-id="ac9ad-109"><dt>**DXVA2 \_ProcAmp \_ 亮度**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ac9ad-109"><dt>**DXVA2\_ProcAmp\_Brightness**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="ac9ad-110">亮度</span><span class="sxs-lookup"><span data-stu-id="ac9ad-110">Brightness</span></span><br/> |
| <span id="DXVA2_ProcAmp_Contrast"></span><span id="dxva2_procamp_contrast"></span><span id="DXVA2_PROCAMP_CONTRAST"></span><dl> <span data-ttu-id="ac9ad-111"><dt>**DXVA2 \_ProcAmp \_ 對比**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="ac9ad-111"><dt>**DXVA2\_ProcAmp\_Contrast**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="ac9ad-112">這個</span><span class="sxs-lookup"><span data-stu-id="ac9ad-112">Contrast</span></span><br/>   |
| <span id="DXVA2_ProcAmp_Hue"></span><span id="dxva2_procamp_hue"></span><span id="DXVA2_PROCAMP_HUE"></span><dl> <span data-ttu-id="ac9ad-113"><dt>**DXVA2 \_ProcAmp \_ 色調**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="ac9ad-113"><dt>**DXVA2\_ProcAmp\_Hue**</dt> <dt>0x0004</dt></span></span> </dl>                             | <span data-ttu-id="ac9ad-114">色調</span><span class="sxs-lookup"><span data-stu-id="ac9ad-114">Hue</span></span><br/>        |
| <span id="DXVA2_ProcAmp_Saturation"></span><span id="dxva2_procamp_saturation"></span><span id="DXVA2_PROCAMP_SATURATION"></span><dl> <span data-ttu-id="ac9ad-115"><dt>**DXVA2 \_ProcAmp \_ 飽和度**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="ac9ad-115"><dt>**DXVA2\_ProcAmp\_Saturation**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="ac9ad-116">飽和度</span><span class="sxs-lookup"><span data-stu-id="ac9ad-116">Saturation</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ac9ad-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac9ad-117">Requirements</span></span>



| <span data-ttu-id="ac9ad-118">需求</span><span class="sxs-lookup"><span data-stu-id="ac9ad-118">Requirement</span></span> | <span data-ttu-id="ac9ad-119">值</span><span class="sxs-lookup"><span data-stu-id="ac9ad-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac9ad-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac9ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac9ad-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac9ad-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac9ad-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac9ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac9ad-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac9ad-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac9ad-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ac9ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac9ad-125"><dt>Dxva2api。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac9ad-125"><dt>Dxva2api.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac9ad-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac9ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac9ad-127">媒體基礎常數</span><span class="sxs-lookup"><span data-stu-id="ac9ad-127">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




