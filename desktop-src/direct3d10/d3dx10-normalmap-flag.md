---
description: 這些旗標是用來控制 D3DX10ComputeNormalMap 產生一般對應的方式。 這些旗標的任意數目可能會以任何組合方式組合。
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: 'D3DX10_NORMALMAP_FLAG 列舉 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985532"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a><span data-ttu-id="53c36-104">D3DX10 \_ NORMALMAP \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="53c36-104">D3DX10\_NORMALMAP\_FLAG enumeration</span></span>

<span data-ttu-id="53c36-105">這些旗標是用來控制 [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) 產生一般對應的方式。</span><span class="sxs-lookup"><span data-stu-id="53c36-105">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="53c36-106">這些旗標的任意數目可能會以任何組合方式組合。</span><span class="sxs-lookup"><span data-stu-id="53c36-106">Any number of these flags may be OR'd together in any combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c36-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53c36-107">Syntax</span></span>


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="53c36-108">常數</span><span class="sxs-lookup"><span data-stu-id="53c36-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53c36-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NORMALMAP \_ 鏡像 \_ U**</span><span class="sxs-lookup"><span data-stu-id="53c36-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="53c36-110">指出 U 軸上材質邊緣的圖元應鏡像，而非 wraped。</span><span class="sxs-lookup"><span data-stu-id="53c36-110">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="53c36-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NORMALMAP \_ 鏡像 \_ V**</span><span class="sxs-lookup"><span data-stu-id="53c36-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="53c36-112">指出 V 軸上材質邊緣的圖元應鏡像，而非 wraped。</span><span class="sxs-lookup"><span data-stu-id="53c36-112">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="53c36-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10 \_ NORMALMAP \_ 鏡像**</span><span class="sxs-lookup"><span data-stu-id="53c36-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="53c36-114">與 D3DX10 \_ NORMALMAP \_ 鏡像 \_ U \| D3DX10 \_ NORMALMAP \_ 鏡像 V 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="53c36-114">Same as D3DX10\_NORMALMAP\_MIRROR\_U \| D3DX10\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="53c36-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NORMALMAP \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="53c36-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="53c36-116">反轉每個標準的方向。</span><span class="sxs-lookup"><span data-stu-id="53c36-116">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="53c36-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10 \_ NORMALMAP \_ COMPUTE \_ 遮蔽**</span><span class="sxs-lookup"><span data-stu-id="53c36-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="53c36-118">計算每個圖元的遮蔽詞彙，然後將其編碼成 Alpha。</span><span class="sxs-lookup"><span data-stu-id="53c36-118">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="53c36-119">Alpha 為1表示圖元不會以任何方式隱藏，而 Alpha 為0表示圖元完全隱藏。</span><span class="sxs-lookup"><span data-stu-id="53c36-119">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53c36-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="53c36-120">Requirements</span></span>



| <span data-ttu-id="53c36-121">需求</span><span class="sxs-lookup"><span data-stu-id="53c36-121">Requirement</span></span> | <span data-ttu-id="53c36-122">值</span><span class="sxs-lookup"><span data-stu-id="53c36-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53c36-123">標頭</span><span class="sxs-lookup"><span data-stu-id="53c36-123">Header</span></span><br/> | <dl> <span data-ttu-id="53c36-124"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="53c36-124"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c36-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53c36-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c36-126">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="53c36-126">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




