---
description: 定義在將材質調整為曲線表面時，執行測式距離計算的選項。 使用此旗標可在計算紋理塔時，選擇高品質與快速計算。
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: 'D3DXU加值稅LAS 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982875"
---
# <a name="d3dxuvatlas-enumeration"></a><span data-ttu-id="44a91-104">D3DXU加值稅LAS 列舉</span><span class="sxs-lookup"><span data-stu-id="44a91-104">D3DXUVATLAS enumeration</span></span>

<span data-ttu-id="44a91-105">定義在將材質調整為曲線表面時，執行測式距離計算的選項。</span><span class="sxs-lookup"><span data-stu-id="44a91-105">Defines options for performing geodesic distance calculations, when fitting a texture to a curved surface.</span></span> <span data-ttu-id="44a91-106">使用此旗標可在計算紋理塔時，選擇高品質與快速計算。</span><span class="sxs-lookup"><span data-stu-id="44a91-106">Use this flag to choose between high quality versus fast calculations when computing a texture atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a91-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="44a91-107">Syntax</span></span>


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a><span data-ttu-id="44a91-108">常數</span><span class="sxs-lookup"><span data-stu-id="44a91-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="44a91-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXU加值稅LAS \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="44a91-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="44a91-110">具有超過25k 臉部的網格將會套用 fast geodasic 距離方法，而小於25k 臉部的網格會改為套用較高品質的地線距離方法。</span><span class="sxs-lookup"><span data-stu-id="44a91-110">Meshes with more than 25k faces will have the fast geodasic distance method applied to them while meshes with fewer than 25k faces will have the higher quality geodesic distance method applied to them instead.</span></span>

</dd> <dt>

<span data-ttu-id="44a91-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**\_快速 D3DXU加值稅LAS 測測 \_**</span><span class="sxs-lookup"><span data-stu-id="44a91-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS\_GEODESIC\_FAST**</span></span>
</dt> <dd>

<span data-ttu-id="44a91-112">使用近似值來改善圖表速度，代價是新增的延展或更多圖表是網格的輸出。</span><span class="sxs-lookup"><span data-stu-id="44a91-112">Uses approximations to improve charting speed at the cost of added stretch or more charts being output for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="44a91-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXU加值稅LAS \_ 地線 \_ 品質**</span><span class="sxs-lookup"><span data-stu-id="44a91-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS\_GEODESIC\_QUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="44a91-114">提供更高品質的圖表，但需要的時間和記憶體比快得多。</span><span class="sxs-lookup"><span data-stu-id="44a91-114">Provides better quality charts, but requires more time and memory than fast.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44a91-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="44a91-115">Requirements</span></span>



| <span data-ttu-id="44a91-116">需求</span><span class="sxs-lookup"><span data-stu-id="44a91-116">Requirement</span></span> | <span data-ttu-id="44a91-117">值</span><span class="sxs-lookup"><span data-stu-id="44a91-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44a91-118">標頭</span><span class="sxs-lookup"><span data-stu-id="44a91-118">Header</span></span><br/> | <dl> <span data-ttu-id="44a91-119"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="44a91-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44a91-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44a91-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a91-121">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="44a91-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




