---
title: 色彩空間類型識別碼
description: 這些常數會指定 Postscript 2 色彩空間陣列的類型。 下列值是有效的色彩空間陣列類型。
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/02/2021
ms.locfileid: "106988511"
---
# <a name="color-space-type-identifiers"></a><span data-ttu-id="19506-104">色彩空間類型識別碼</span><span class="sxs-lookup"><span data-stu-id="19506-104">Color Space Type Identifiers</span></span>

<span data-ttu-id="19506-105">這些常數會指定 Postscript 2 色彩空間陣列的類型。</span><span class="sxs-lookup"><span data-stu-id="19506-105">These constants specify the type of a Postscript 2 color space array.</span></span> <span data-ttu-id="19506-106">下列值是有效的色彩空間陣列類型。</span><span class="sxs-lookup"><span data-stu-id="19506-106">The following values are valid color space array types.</span></span>

<dl> <dt>

<span data-ttu-id="19506-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**</span><span class="sxs-lookup"><span data-stu-id="19506-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA\_A**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-108">從單色設定檔取得 CIEBasedA 色彩空間陣列。</span><span class="sxs-lookup"><span data-stu-id="19506-108">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19506-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA \_ 灰色**</span><span class="sxs-lookup"><span data-stu-id="19506-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA\_GRAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-110">從單色設定檔取得 CIEBasedA 色彩空間陣列。</span><span class="sxs-lookup"><span data-stu-id="19506-110">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19506-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**</span><span class="sxs-lookup"><span data-stu-id="19506-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA\_ABC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-112">從 RGB 或 L <sup>\*</sup> a b 設定檔取得 CIEBasedABC 色彩空間陣列 <sup>\*</sup> 。</span><span class="sxs-lookup"><span data-stu-id="19506-112">Get a CIEBasedABC color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19506-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ DEF**</span><span class="sxs-lookup"><span data-stu-id="19506-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA\_DEF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-114">從 RGB 或 L <sup>\*</sup> a b 設定檔取得 CIEBasedDEF 色彩空間陣列 <sup>\*</sup> 。</span><span class="sxs-lookup"><span data-stu-id="19506-114">Get a CIEBasedDEF color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19506-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="19506-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA\_RGB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-116">從 RGB 設定檔取得 CIEBasedDEF 色彩空間陣列，後面接著 CIEBasedABC 色彩空間陣列。</span><span class="sxs-lookup"><span data-stu-id="19506-116">Get a CIEBasedDEF color space array followed by a CIEBasedABC color space array from the RGB profile.</span></span> <span data-ttu-id="19506-117">執行時，如果印表機不支援 CIEBasedDEF 色彩空間，此函數會使用 CIEBasedABC 定義。</span><span class="sxs-lookup"><span data-stu-id="19506-117">On execution, if the printer doesn't support CIEBasedDEF color spaces, the function uses the CIEBasedABC definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19506-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA \_ 實驗室**</span><span class="sxs-lookup"><span data-stu-id="19506-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA\_Lab**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-119">從 L <sup>\*</sup> a b 設定檔取得 CIEBasedABC 色彩空間陣列 <sup>\*</sup> 。</span><span class="sxs-lookup"><span data-stu-id="19506-119">Gets a CIEBasedABC color space array from the L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19506-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA \_ DEFG**</span><span class="sxs-lookup"><span data-stu-id="19506-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA\_DEFG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-121">從 CMYK 設定檔取得 CIEBasedDEFG 色彩空間陣列。</span><span class="sxs-lookup"><span data-stu-id="19506-121">Get a CIEBasedDEFG color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19506-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**</span><span class="sxs-lookup"><span data-stu-id="19506-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA\_CMYK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19506-123">從 CMYK 設定檔取得 CIEBasedCMYK 色彩空間陣列。</span><span class="sxs-lookup"><span data-stu-id="19506-123">Get a CIEBasedCMYK color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> </dl>

## <a name="see-also"></a><span data-ttu-id="19506-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19506-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19506-125">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="19506-125">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="19506-126">ICM 常數</span><span class="sxs-lookup"><span data-stu-id="19506-126">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




