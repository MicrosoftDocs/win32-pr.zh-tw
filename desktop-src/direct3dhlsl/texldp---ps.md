---
title: texldp-ps
description: 投射的材質載入指示。 此指令會將輸入材質座標除以第四個元素 (. w) 在取樣之前。
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316393"
---
# <a name="texldp---ps"></a><span data-ttu-id="2e6f7-104">texldp-ps</span><span class="sxs-lookup"><span data-stu-id="2e6f7-104">texldp - ps</span></span>

<span data-ttu-id="2e6f7-105">投射的材質載入指示。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-105">Projected texture load instruction.</span></span> <span data-ttu-id="2e6f7-106">此指令會將輸入材質座標除以第四個元素 (. w) 在取樣之前。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-106">This instruction divides the input texture coordinate by the fourth element (.a or .w) just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e6f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e6f7-107">Syntax</span></span>



| <span data-ttu-id="2e6f7-108">texldp dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="2e6f7-108">texldp dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="2e6f7-109">其中</span><span class="sxs-lookup"><span data-stu-id="2e6f7-109">where</span></span>

-   <span data-ttu-id="2e6f7-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-110">dst is the destination register.</span></span>
-   <span data-ttu-id="2e6f7-111">src0 是一種來源暫存器，可提供紋理範例的材質座標。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="2e6f7-112">請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="2e6f7-113">src1 會識別 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，其中 \# 指定要取樣的材質取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="2e6f7-114">取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)定義的材質和取樣器狀態相關聯。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="2e6f7-115">如需使用 texldp 時的限制集合，請參閱 [texld](texld---ps-2-0.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-115">For the set of restrictions when using texldp, see [texld](texld---ps-2-0.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e6f7-116">備註</span><span class="sxs-lookup"><span data-stu-id="2e6f7-116">Remarks</span></span>

<span data-ttu-id="2e6f7-117">texldp 會在執行範例之前，對從 src0 讀取的座標執行投射。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-117">texldp performs projection on the coordinates read from src0 before performing the sample.</span></span> <span data-ttu-id="2e6f7-118">每個材質座標都會以 src0 除以 w，然後取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-118">Each texture coordinate is divided by src0.w, then the texture is sampled.</span></span> <span data-ttu-id="2e6f7-119">當 texldp 完成時，除非 dst 是相同的註冊) ，否則 src0 的內容不會受到 (的影響。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-119">When texldp completes, the contents of src0 are unaffected (unless dst is the same register).</span></span> <span data-ttu-id="2e6f7-120">使用 texldp 的另一種方式是在著色器中手動執行投影除法。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-120">An alternative to using texldp is to manually perform the projection division in the shader.</span></span> <span data-ttu-id="2e6f7-121">不過，在著色器程式碼中執行除法通常比 texldp 指令執行的速度慢，因此請盡可能避免這類額外的數學運算。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-121">However, performing the division in shader code is usually slower than when performed by the texldp instruction, so avoid such additional math when possible.</span></span>

<span data-ttu-id="2e6f7-122">Src0 執行材質範例所需的座標數目取決於 src1 的宣告方式，以及 w 元件。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-122">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="2e6f7-123">取樣器型別是以 [dcl \_ samplerType 宣告 (sm2、sm3 ps asm) ](dcl-samplertype---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-123">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="2e6f7-124">如果 src1 宣告為2D 取樣器，則 src0 必須包含 xyw 座標;如果 src1 宣告為 cube 取樣器或磁片區取樣器，則 src0 必須包含 xyzw 座標。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-124">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="2e6f7-125">使用 xyzw 座標取樣2D 材質 (會忽略) 的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-125">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="2e6f7-126">如果來源材質包含四個以上的元件，預設值就會放置在遺漏的元件中。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-126">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="2e6f7-127">預設值取決於下表所示的材質格式。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-127">Defaults depend on the texture format as shown in the following table.</span></span>



| <span data-ttu-id="2e6f7-128">材質格式</span><span class="sxs-lookup"><span data-stu-id="2e6f7-128">Texture Format</span></span>                                                                                          | <span data-ttu-id="2e6f7-129">遺漏元件的預設值</span><span class="sxs-lookup"><span data-stu-id="2e6f7-129">Default Values for missing components</span></span> |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="2e6f7-130">D3DFMT \_ R5G6B5、D3DFMT \_ R8G8B8、D3DFMT \_ L8、D3DFMT \_ l16 也、D3DFMT \_ R3G3B2、D3DFMT \_ CxV8U8、D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="2e6f7-130">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="2e6f7-131">A = 1。0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-131">A = 1.0</span></span>                               |
| <span data-ttu-id="2e6f7-132">D3DFMT \_ V8U8、D3DFMT \_ V16U16、D3DFMT \_ G16R16、D3DFMT \_ G16R16F、D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="2e6f7-132">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="2e6f7-133">B = A = 1。0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-133">B = A = 1.0</span></span>                           |
| <span data-ttu-id="2e6f7-134">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="2e6f7-134">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="2e6f7-135">R = G = B = 0。0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-135">R = G = B = 0.0</span></span>                       |
| <span data-ttu-id="2e6f7-136">D3DFMT \_ R16F、D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="2e6f7-136">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="2e6f7-137">G = B = A = 1。0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-137">G = B = A = 1.0</span></span>                       |
| <span data-ttu-id="2e6f7-138">所有深度/樣板格式</span><span class="sxs-lookup"><span data-stu-id="2e6f7-138">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="2e6f7-139">R = B = 0.0，A = 1。0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-139">R = B = 0.0, A = 1.0</span></span>                  |



 

<span data-ttu-id="2e6f7-140">下列版本支援此指令：</span><span class="sxs-lookup"><span data-stu-id="2e6f7-140">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="2e6f7-141">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="2e6f7-141">Pixel shader versions</span></span> | <span data-ttu-id="2e6f7-142">1\_1</span><span class="sxs-lookup"><span data-stu-id="2e6f7-142">1\_1</span></span> | <span data-ttu-id="2e6f7-143">1\_2</span><span class="sxs-lookup"><span data-stu-id="2e6f7-143">1\_2</span></span> | <span data-ttu-id="2e6f7-144">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2e6f7-144">1\_3</span></span> | <span data-ttu-id="2e6f7-145">1\_4</span><span class="sxs-lookup"><span data-stu-id="2e6f7-145">1\_4</span></span> | <span data-ttu-id="2e6f7-146">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-146">2\_0</span></span> | <span data-ttu-id="2e6f7-147">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e6f7-147">2\_x</span></span> | <span data-ttu-id="2e6f7-148">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2e6f7-148">2\_sw</span></span> | <span data-ttu-id="2e6f7-149">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-149">3\_0</span></span> | <span data-ttu-id="2e6f7-150">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2e6f7-150">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2e6f7-151">texldp</span><span class="sxs-lookup"><span data-stu-id="2e6f7-151">texldp</span></span>                |      |      |      |      | <span data-ttu-id="2e6f7-152">x</span><span class="sxs-lookup"><span data-stu-id="2e6f7-152">x</span></span>    | <span data-ttu-id="2e6f7-153">x</span><span class="sxs-lookup"><span data-stu-id="2e6f7-153">x</span></span>    | <span data-ttu-id="2e6f7-154">x</span><span class="sxs-lookup"><span data-stu-id="2e6f7-154">x</span></span>     | <span data-ttu-id="2e6f7-155">x</span><span class="sxs-lookup"><span data-stu-id="2e6f7-155">x</span></span>    | <span data-ttu-id="2e6f7-156">x</span><span class="sxs-lookup"><span data-stu-id="2e6f7-156">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="2e6f7-157">ps \_ 2 \_ 0 和 ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e6f7-157">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="2e6f7-158">dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) ，而且只允許) 的 xyzw mask (預設遮罩。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-158">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="2e6f7-159">src0 必須是 [紋理座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器 (t \#) 或 (r) 的 [臨時](dx9-graphics-reference-asm-ps-registers-temporary.md) 暫存器 \# ，但不含修飾詞或 swizzle。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-159">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="2e6f7-160">src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞或 swizzle。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-160">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="2e6f7-161">如果 D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT cap 位未設定 (在 D3DPSHADERCAPS2 \_ 0) 中，指定的材質指令 ([texld](texld---ps-1-4.md)、texldp、 [texldb-ps](texldb---ps.md)、 [texldd](texldd---ps.md) ) 可能會相依于最多第三個順序。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-161">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="2e6f7-162">第一個順序相依材質指令是一個材質指令，其中：</span><span class="sxs-lookup"><span data-stu-id="2e6f7-162">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="2e6f7-163">src0 是 (r) 的[暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \#</span><span class="sxs-lookup"><span data-stu-id="2e6f7-163">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#)</span></span>
-   <span data-ttu-id="2e6f7-164">dst 先前已寫入，現在正在撰寫中。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-164">dst was previously written, now being written again.</span></span>

<span data-ttu-id="2e6f7-165">第二個順序相依的材質指令定義為材質指令，可讀取或寫入 [暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 其內容在執行材質 (指令之前的內容，可能會在第一個順序相依材質指令的結果上間接) 。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-165">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="2e6f7-166"> (n) <sup>第</sup>一個順序的相依材質指令會衍生自 (n-1) <sup>第</sup>一個順序的材質指令。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-166">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="2e6f7-167">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e6f7-167">ps\_3\_0</span></span>

<span data-ttu-id="2e6f7-168">針對 ps \_ 3 \_ 0，src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-168">For ps\_3\_0, src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="2e6f7-169">Swizzle 可在 src1 上使用，並且在套用時，紋理查閱結果會在寫入 dst 之前預先 swizzled。</span><span class="sxs-lookup"><span data-stu-id="2e6f7-169">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e6f7-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e6f7-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e6f7-171">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="2e6f7-171">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 