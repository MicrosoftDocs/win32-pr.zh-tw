---
title: texldb-ps
description: 偏誤材質載入指示。 此指示會使用第四個元素 (. 或. w) ，在取樣之前，偏差紋理取樣的詳細程度。
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092803"
---
# <a name="texldb---ps"></a><span data-ttu-id="79834-104">texldb-ps</span><span class="sxs-lookup"><span data-stu-id="79834-104">texldb - ps</span></span>

<span data-ttu-id="79834-105">偏誤材質載入指示。</span><span class="sxs-lookup"><span data-stu-id="79834-105">Biased texture load instruction.</span></span> <span data-ttu-id="79834-106">此指示會使用第四個元素 (. 或. w) ，在取樣之前，偏差紋理取樣的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="79834-106">This instruction uses the fourth element (.a or .w) to bias the texture-sampling level-of-detail just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="79834-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79834-107">Syntax</span></span>



| <span data-ttu-id="79834-108">texldb dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="79834-108">texldb dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="79834-109">其中：</span><span class="sxs-lookup"><span data-stu-id="79834-109">Where:</span></span>

-   <span data-ttu-id="79834-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="79834-110">dst is the destination register.</span></span>
-   <span data-ttu-id="79834-111">src0 是一種來源暫存器，可提供紋理範例的材質座標。</span><span class="sxs-lookup"><span data-stu-id="79834-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="79834-112">請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。</span><span class="sxs-lookup"><span data-stu-id="79834-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="79834-113">src1 會識別 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，其中 \# 指定要取樣的材質取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="79834-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="79834-114">取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)定義的材質和取樣器狀態相關聯。</span><span class="sxs-lookup"><span data-stu-id="79834-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="79834-115">如需使用 texldb 的限制，請參閱 [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="79834-115">For the restrictions when using texldb, see the [texld - ps\_2\_0 and up](texld---ps-2-0.md) instruction.</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="79834-116">ps \_ 2 \_ 0 和 ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="79834-116">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="79834-117">dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) ，而且只允許) 的 xyzw mask (預設遮罩。</span><span class="sxs-lookup"><span data-stu-id="79834-117">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="79834-118">src0 必須是 [紋理座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器 (t \#) 或 (r) 的 [臨時](dx9-graphics-reference-asm-ps-registers-temporary.md) 暫存器 \# ，但不含修飾詞或 swizzle。</span><span class="sxs-lookup"><span data-stu-id="79834-118">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="79834-119">src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞或 swizzle。</span><span class="sxs-lookup"><span data-stu-id="79834-119">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="79834-120">如果 D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT cap 位未設定 (在 D3DPSHADERCAPS2 \_ 0) 中，指定的材質指令 (texld、texldp、texldb、texldd) 可能會相依于最多第三個順序。</span><span class="sxs-lookup"><span data-stu-id="79834-120">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction (texld, texldp, texldb, texldd) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="79834-121">第一個順序相依材質指令是一個材質指令，其中：</span><span class="sxs-lookup"><span data-stu-id="79834-121">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="79834-122">src0 是 (r) 的 [暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \# 。</span><span class="sxs-lookup"><span data-stu-id="79834-122">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="79834-123">dst 先前已寫入，現在正在撰寫中。</span><span class="sxs-lookup"><span data-stu-id="79834-123">dst was previously written, now being written again.</span></span>

<span data-ttu-id="79834-124">第二個順序相依的材質指令定義為材質指令，可讀取或寫入 [暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 其內容在執行材質 (指令之前的內容，可能會在第一個順序相依材質指令的結果上間接) 。</span><span class="sxs-lookup"><span data-stu-id="79834-124">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="79834-125"> (n) <sup>第</sup>一個順序的相依材質指令會衍生自 (n-1) <sup>第</sup>一個順序的材質指令。</span><span class="sxs-lookup"><span data-stu-id="79834-125">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="79834-126">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="79834-126">ps\_3\_0</span></span>

<span data-ttu-id="79834-127">src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \#) ，沒有修飾詞的取樣器。</span><span class="sxs-lookup"><span data-stu-id="79834-127">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="79834-128">Swizzle 可在 src1 上使用，並且在套用時，紋理查閱結果會在寫入 dst 之前預先 swizzled。</span><span class="sxs-lookup"><span data-stu-id="79834-128">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="remarks"></a><span data-ttu-id="79834-129">備註</span><span class="sxs-lookup"><span data-stu-id="79834-129">Remarks</span></span>



| <span data-ttu-id="79834-130">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="79834-130">Pixel shader versions</span></span> | <span data-ttu-id="79834-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="79834-131">1\_1</span></span> | <span data-ttu-id="79834-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="79834-132">1\_2</span></span> | <span data-ttu-id="79834-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="79834-133">1\_3</span></span> | <span data-ttu-id="79834-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="79834-134">1\_4</span></span> | <span data-ttu-id="79834-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="79834-135">2\_0</span></span> | <span data-ttu-id="79834-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="79834-136">2\_x</span></span> | <span data-ttu-id="79834-137">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="79834-137">2\_sw</span></span> | <span data-ttu-id="79834-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="79834-138">3\_0</span></span> | <span data-ttu-id="79834-139">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="79834-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="79834-140">texldb</span><span class="sxs-lookup"><span data-stu-id="79834-140">texldb</span></span>                |      |      |      |      | <span data-ttu-id="79834-141">x</span><span class="sxs-lookup"><span data-stu-id="79834-141">x</span></span>    | <span data-ttu-id="79834-142">x</span><span class="sxs-lookup"><span data-stu-id="79834-142">x</span></span>    | <span data-ttu-id="79834-143">x</span><span class="sxs-lookup"><span data-stu-id="79834-143">x</span></span>     | <span data-ttu-id="79834-144">x</span><span class="sxs-lookup"><span data-stu-id="79834-144">x</span></span>    | <span data-ttu-id="79834-145">x</span><span class="sxs-lookup"><span data-stu-id="79834-145">x</span></span>     |



 

<span data-ttu-id="79834-146">texldb 會偏差 mipmap 的詳細層級，並以 src0 中 (簽署的) 值做為範例進程的一部分來計算。</span><span class="sxs-lookup"><span data-stu-id="79834-146">texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w.</span></span> <span data-ttu-id="79834-147">正偏差值會導致選取較小的 mipmap，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="79834-147">Positive bias values will result in smaller mipmaps being selected and vice versa.</span></span> <span data-ttu-id="79834-148">針對 ps \_ 2 \_ 0 和 ps \_ 2 \_ x，偏差值可以在 \[ -3.0、+ 3.0 範圍內 \] 。</span><span class="sxs-lookup"><span data-stu-id="79834-148">For ps\_2\_0 and ps\_2\_x, bias values can be within the range \[-3.0, +3.0\].</span></span> <span data-ttu-id="79834-149">針對 ps \_ 3 \_ 0，偏差值可以在 \[ -16.0、+ 15.0 範圍內 \] 。</span><span class="sxs-lookup"><span data-stu-id="79834-149">For ps\_3\_0, bias values can be within the range \[-16.0, +15.0\].</span></span> <span data-ttu-id="79834-150">這些範圍之外的偏差值會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="79834-150">Bias values outside these ranges produce undefined results.</span></span> <span data-ttu-id="79834-151">仍會接受取樣器狀態 D3DSAMP \_ MIPMAPLODBIAS，並將 texldb 偏差新增至此，但以每圖元為基礎。</span><span class="sxs-lookup"><span data-stu-id="79834-151">The sampler state D3DSAMP\_MIPMAPLODBIAS is still honored, and the texldb bias is added to this, but on a per-pixel basis.</span></span> <span data-ttu-id="79834-152">計算出偏高的詳細資料層級之後， \_ 仍會接受 D3DSAMP MAXMIPLEVEL，並產生紋理範例。</span><span class="sxs-lookup"><span data-stu-id="79834-152">After the biased level-of-detail is computed, D3DSAMP\_MAXMIPLEVEL is still honored and the texture sample occurs.</span></span> <span data-ttu-id="79834-153">Texldb 之後，除非 dst 是相同的註冊) ，否則 src0 的內容不會受到 (的影響。</span><span class="sxs-lookup"><span data-stu-id="79834-153">After texldb, the contents of src0 are unaffected (unless dst is the same register).</span></span>

<span data-ttu-id="79834-154">Src0 執行材質範例所需的座標數目取決於 src1 的宣告方式，以及 w 元件。</span><span class="sxs-lookup"><span data-stu-id="79834-154">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="79834-155">取樣器型別是以 [dcl \_ samplerType 宣告 (sm2、sm3 ps asm) ](dcl-samplertype---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="79834-155">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="79834-156">如果 src1 宣告為2D 取樣器，則 src0 必須包含 xyw 座標;如果 src1 宣告為 cube 取樣器或磁片區取樣器，則 src0 必須包含 xyzw 座標。</span><span class="sxs-lookup"><span data-stu-id="79834-156">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="79834-157">使用 xyzw 座標取樣2D 材質 (會忽略) 的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="79834-157">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="79834-158">如果來源材質包含四個以上的元件，預設值就會放置在遺漏的元件中。</span><span class="sxs-lookup"><span data-stu-id="79834-158">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="79834-159">預設值取決於下表所示的材質格式：</span><span class="sxs-lookup"><span data-stu-id="79834-159">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="79834-160">材質格式</span><span class="sxs-lookup"><span data-stu-id="79834-160">Texture Format</span></span>                                                                                          | <span data-ttu-id="79834-161">預設值</span><span class="sxs-lookup"><span data-stu-id="79834-161">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="79834-162">D3DFMT \_ R5G6B5、D3DFMT \_ R8G8B8、D3DFMT \_ L8、D3DFMT \_ l16 也、D3DFMT \_ R3G3B2、D3DFMT \_ CxV8U8、D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="79834-162">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="79834-163">A = 1。0</span><span class="sxs-lookup"><span data-stu-id="79834-163">A = 1.0</span></span>              |
| <span data-ttu-id="79834-164">D3DFMT \_ V8U8、D3DFMT \_ V16U16、D3DFMT \_ G16R16、D3DFMT \_ G16R16F、D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="79834-164">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="79834-165">B = A = 1。0</span><span class="sxs-lookup"><span data-stu-id="79834-165">B = A = 1.0</span></span>          |
| <span data-ttu-id="79834-166">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="79834-166">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="79834-167">R = G = B = 0。0</span><span class="sxs-lookup"><span data-stu-id="79834-167">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="79834-168">D3DFMT \_ R16F、D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="79834-168">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="79834-169">G = B = A = 1。0</span><span class="sxs-lookup"><span data-stu-id="79834-169">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="79834-170">所有深度/樣板格式</span><span class="sxs-lookup"><span data-stu-id="79834-170">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="79834-171">R = B = 0.0，A = 1。0</span><span class="sxs-lookup"><span data-stu-id="79834-171">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="79834-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="79834-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79834-173">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="79834-173">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 