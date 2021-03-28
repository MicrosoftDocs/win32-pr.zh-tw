---
title: 'D3DX11_NORMALMAP_FLAG 列舉 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 一般對應選項。 您可以使用位 OR 運算來合併任何數目的旗標。
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG 列舉 Direct3D 11
- LPD3DX11_NORMALMAP_FLAG 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196444"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a><span data-ttu-id="2bbb9-107">D3DX11 \_ NORMALMAP \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="2bbb9-107">D3DX11\_NORMALMAP\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="2bbb9-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="2bbb9-109">一般對應選項。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-109">Normal map options.</span></span> <span data-ttu-id="2bbb9-110">您可以使用位 OR 運算來合併任何數目的旗標。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-110">You can combine any number of these flags by using a bitwise OR operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bbb9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bbb9-111">Syntax</span></span>


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="2bbb9-112">常數</span><span class="sxs-lookup"><span data-stu-id="2bbb9-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2bbb9-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ 鏡像 \_ U**</span><span class="sxs-lookup"><span data-stu-id="2bbb9-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="2bbb9-114">指出 U 軸上材質邊緣的圖元應鏡像，而非 wraped。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-114">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="2bbb9-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ 鏡像 \_ V**</span><span class="sxs-lookup"><span data-stu-id="2bbb9-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="2bbb9-116">指出 V 軸上材質邊緣的圖元應鏡像，而非 wraped。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-116">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="2bbb9-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NORMALMAP \_ 鏡像**</span><span class="sxs-lookup"><span data-stu-id="2bbb9-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="2bbb9-118">與 D3DX11 \_ NORMALMAP \_ 鏡像 \_ U \| D3DX11 \_ NORMALMAP \_ 鏡像 V 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-118">Same as D3DX11\_NORMALMAP\_MIRROR\_U \| D3DX11\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="2bbb9-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="2bbb9-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="2bbb9-120">反轉每個標準的方向。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-120">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="2bbb9-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ NORMALMAP \_ COMPUTE \_ 遮蔽**</span><span class="sxs-lookup"><span data-stu-id="2bbb9-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="2bbb9-122">計算每個圖元的遮蔽詞彙，然後將其編碼成 Alpha。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-122">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="2bbb9-123">Alpha 為1表示圖元不會以任何方式隱藏，而 Alpha 為0表示圖元完全隱藏。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-123">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bbb9-124">備註</span><span class="sxs-lookup"><span data-stu-id="2bbb9-124">Remarks</span></span>

<span data-ttu-id="2bbb9-125">[**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md)會使用這些旗標。</span><span class="sxs-lookup"><span data-stu-id="2bbb9-125">These flags are used by [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bbb9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bbb9-126">Requirements</span></span>



| <span data-ttu-id="2bbb9-127">需求</span><span class="sxs-lookup"><span data-stu-id="2bbb9-127">Requirement</span></span> | <span data-ttu-id="2bbb9-128">值</span><span class="sxs-lookup"><span data-stu-id="2bbb9-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bbb9-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2bbb9-129">Header</span></span><br/> | <dl> <span data-ttu-id="2bbb9-130"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bbb9-130"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bbb9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bbb9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbb9-132">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="2bbb9-132">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





