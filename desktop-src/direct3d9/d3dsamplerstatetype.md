---
description: 取樣器狀態定義紋理取樣作業，例如紋理定址和材質篩選。
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: 'D3DSAMPLERSTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988582"
---
# <a name="d3dsamplerstatetype-enumeration"></a><span data-ttu-id="e00b5-103">D3DSAMPLERSTATETYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="e00b5-103">D3DSAMPLERSTATETYPE enumeration</span></span>

<span data-ttu-id="e00b5-104">取樣器狀態定義紋理取樣作業，例如紋理定址和材質篩選。</span><span class="sxs-lookup"><span data-stu-id="e00b5-104">Sampler states define texture sampling operations such as texture addressing and texture filtering.</span></span> <span data-ttu-id="e00b5-105">某些取樣器狀態設定頂點處理，以及一些設定圖元處理。</span><span class="sxs-lookup"><span data-stu-id="e00b5-105">Some sampler states set-up vertex processing, and some set-up pixel processing.</span></span> <span data-ttu-id="e00b5-106">您可以使用 stateblocks 來儲存和還原取樣器狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="e00b5-106">Sampler states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="e00b5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e00b5-107">Syntax</span></span>


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="e00b5-108">常數</span><span class="sxs-lookup"><span data-stu-id="e00b5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e00b5-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ ADDRESSU**</span><span class="sxs-lookup"><span data-stu-id="e00b5-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP\_ADDRESSU**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-110">U 座標的材質位址模式。</span><span class="sxs-lookup"><span data-stu-id="e00b5-110">Texture-address mode for the u coordinate.</span></span> <span data-ttu-id="e00b5-111">預設值為 D3DTADDRESS \_ WRAP。</span><span class="sxs-lookup"><span data-stu-id="e00b5-111">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="e00b5-112">如需詳細資訊，請參閱 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)。</span><span class="sxs-lookup"><span data-stu-id="e00b5-112">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**</span><span class="sxs-lookup"><span data-stu-id="e00b5-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP\_ADDRESSV**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-114">V 座標的材質位址模式。</span><span class="sxs-lookup"><span data-stu-id="e00b5-114">Texture-address mode for the v coordinate.</span></span> <span data-ttu-id="e00b5-115">預設值為 D3DTADDRESS \_ WRAP。</span><span class="sxs-lookup"><span data-stu-id="e00b5-115">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="e00b5-116">如需詳細資訊，請參閱 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)。</span><span class="sxs-lookup"><span data-stu-id="e00b5-116">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**</span><span class="sxs-lookup"><span data-stu-id="e00b5-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP\_ADDRESSW**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-118">W 座標的材質位址模式。</span><span class="sxs-lookup"><span data-stu-id="e00b5-118">Texture-address mode for the w coordinate.</span></span> <span data-ttu-id="e00b5-119">預設值為 D3DTADDRESS \_ WRAP。</span><span class="sxs-lookup"><span data-stu-id="e00b5-119">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="e00b5-120">如需詳細資訊，請參閱 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)。</span><span class="sxs-lookup"><span data-stu-id="e00b5-120">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ 邊框**</span><span class="sxs-lookup"><span data-stu-id="e00b5-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP\_BORDERCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-122">框線色彩或類型 [**D3DCOLOR**](d3dcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="e00b5-122">Border color or type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="e00b5-123">預設色彩為0x00000000。</span><span class="sxs-lookup"><span data-stu-id="e00b5-123">The default color is 0x00000000.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**</span><span class="sxs-lookup"><span data-stu-id="e00b5-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP\_MAGFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-125">[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)類型的放大篩選。</span><span class="sxs-lookup"><span data-stu-id="e00b5-125">Magnification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="e00b5-126">預設值為 D3DTEXF \_ 點。</span><span class="sxs-lookup"><span data-stu-id="e00b5-126">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**</span><span class="sxs-lookup"><span data-stu-id="e00b5-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP\_MINFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-128">[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)類型的縮制篩選。</span><span class="sxs-lookup"><span data-stu-id="e00b5-128">Minification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="e00b5-129">預設值為 D3DTEXF \_ 點。</span><span class="sxs-lookup"><span data-stu-id="e00b5-129">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**</span><span class="sxs-lookup"><span data-stu-id="e00b5-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP\_MIPFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-131">要在縮制期間使用的 Mipmap 篩選準則。</span><span class="sxs-lookup"><span data-stu-id="e00b5-131">Mipmap filter to use during minification.</span></span> <span data-ttu-id="e00b5-132">請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。</span><span class="sxs-lookup"><span data-stu-id="e00b5-132">See [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="e00b5-133">預設值為 [無] D3DTEXF \_ 。</span><span class="sxs-lookup"><span data-stu-id="e00b5-133">The default value is D3DTEXF\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**</span><span class="sxs-lookup"><span data-stu-id="e00b5-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP\_MIPMAPLODBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-135">Mipmap 詳細資料偏差。</span><span class="sxs-lookup"><span data-stu-id="e00b5-135">Mipmap level-of-detail bias.</span></span> <span data-ttu-id="e00b5-136">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="e00b5-136">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="e00b5-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP\_MAXMIPLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-138">要使用的最大地圖的詳細層級索引。</span><span class="sxs-lookup"><span data-stu-id="e00b5-138">level-of-detail index of largest map to use.</span></span> <span data-ttu-id="e00b5-139">值的範圍是從0到 (n-1-1) 其中0是最大值。</span><span class="sxs-lookup"><span data-stu-id="e00b5-139">Values range from 0 to (n - 1) where 0 is the largest.</span></span> <span data-ttu-id="e00b5-140">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="e00b5-140">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**</span><span class="sxs-lookup"><span data-stu-id="e00b5-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP\_MAXANISOTROPY**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-142">DWORD 最大 anisotropy。</span><span class="sxs-lookup"><span data-stu-id="e00b5-142">DWORD maximum anisotropy.</span></span> <span data-ttu-id="e00b5-143">值的範圍是從1到 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 **MaxAnisotropy** 成員中指定的值。</span><span class="sxs-lookup"><span data-stu-id="e00b5-143">Values range from 1 to the value that is specified in the **MaxAnisotropy** member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="e00b5-144">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="e00b5-144">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="e00b5-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP\_SRGBTEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-146">Gamma 修正值。</span><span class="sxs-lookup"><span data-stu-id="e00b5-146">Gamma correction value.</span></span> <span data-ttu-id="e00b5-147">預設值為0，表示 gamma 為1.0，且不需要任何更正。</span><span class="sxs-lookup"><span data-stu-id="e00b5-147">The default value is 0, which means gamma is 1.0 and no correction is required.</span></span> <span data-ttu-id="e00b5-148">否則，此值表示取樣器在內容上應該採用2.2 的 gamma，並將其轉換為線性 (gamma 1.0) ，然後再呈現給圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="e00b5-148">Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**</span><span class="sxs-lookup"><span data-stu-id="e00b5-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP\_ELEMENTINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-150">將 multielement 材質指派給取樣器時，這會指出要使用的元素索引。</span><span class="sxs-lookup"><span data-stu-id="e00b5-150">When a multielement texture is assigned to the sampler, this indicates which element index to use.</span></span> <span data-ttu-id="e00b5-151">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="e00b5-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**</span><span class="sxs-lookup"><span data-stu-id="e00b5-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP\_DMAPOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-153">Presampled 置換地圖中的頂點位移。</span><span class="sxs-lookup"><span data-stu-id="e00b5-153">Vertex offset in the presampled displacement map.</span></span> <span data-ttu-id="e00b5-154">這是鑲嵌所使用的常數，其預設值為0。</span><span class="sxs-lookup"><span data-stu-id="e00b5-154">This is a constant used by the tessellator, its default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="e00b5-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e00b5-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e00b5-156">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="e00b5-156">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e00b5-157">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="e00b5-157">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e00b5-158">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="e00b5-158">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e00b5-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="e00b5-159">Requirements</span></span>



| <span data-ttu-id="e00b5-160">需求</span><span class="sxs-lookup"><span data-stu-id="e00b5-160">Requirement</span></span> | <span data-ttu-id="e00b5-161">值</span><span class="sxs-lookup"><span data-stu-id="e00b5-161">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e00b5-162">標頭</span><span class="sxs-lookup"><span data-stu-id="e00b5-162">Header</span></span><br/> | <dl> <span data-ttu-id="e00b5-163"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e00b5-163"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00b5-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e00b5-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00b5-165">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="e00b5-165">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
