---
title: texld-ps_2_0 和更新
description: 使用提供的材質座標，在特定取樣器上取樣材質。 這個指令不同于 \_ \_ 圖元著色器第1版中所使用的 texld-ps 1 4 指令 \_ 。
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507980"
---
# <a name="texld---ps_2_0-and-up"></a><span data-ttu-id="4fed1-104">texld-ps \_ 2 \_ 0 和更新的</span><span class="sxs-lookup"><span data-stu-id="4fed1-104">texld - ps\_2\_0 and up</span></span>

<span data-ttu-id="4fed1-105">使用提供的材質座標，在特定取樣器上取樣材質。</span><span class="sxs-lookup"><span data-stu-id="4fed1-105">Sample a texture at a particular sampler, using provided texture coordinates.</span></span> <span data-ttu-id="4fed1-106">這個指令不同于圖元著色器第1版中所使用的 [texld-ps \_ 1 \_ 4](texld---ps-1-4.md) 指令 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4fed1-106">This instruction is different from the [texld - ps\_1\_4](texld---ps-1-4.md) instruction used in pixel shader version 1\_4.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fed1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fed1-107">Syntax</span></span>



| <span data-ttu-id="4fed1-108">texld dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="4fed1-108">texld dst, src0, src1</span></span> |
|-----------------------|



 

<span data-ttu-id="4fed1-109">其中：</span><span class="sxs-lookup"><span data-stu-id="4fed1-109">Where:</span></span>

-   <span data-ttu-id="4fed1-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="4fed1-110">dst is a destination register.</span></span>
-   <span data-ttu-id="4fed1-111">src0 是一種來源暫存器，可提供紋理範例的材質座標。</span><span class="sxs-lookup"><span data-stu-id="4fed1-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="4fed1-112">src1 會識別 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，其中 \# 指定要取樣的材質取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="4fed1-112">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="4fed1-113">取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)定義的材質和取樣器狀態相關聯。</span><span class="sxs-lookup"><span data-stu-id="4fed1-113">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="4fed1-114">ps \_ 2 \_ 0 和 ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4fed1-114">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="4fed1-115">dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) ，而且只允許) 的 xyzw mask (預設遮罩。</span><span class="sxs-lookup"><span data-stu-id="4fed1-115">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="4fed1-116">src0 必須是 [紋理座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器 (t \#) 或 (r) 的 [臨時](dx9-graphics-reference-asm-ps-registers-temporary.md) 暫存器 \# ，但不含修飾詞或 swizzle。</span><span class="sxs-lookup"><span data-stu-id="4fed1-116">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="4fed1-117">src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# ，沒有修飾詞或 swizzle。</span><span class="sxs-lookup"><span data-stu-id="4fed1-117">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="4fed1-118">如果 D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT cap 位未設定 (在 D3DPSHADERCAPS2 \_ 0) 中，指定的材質指令 ([texld](texld---ps-1-4.md)、 [texldp](texldp---ps.md)、 [texldb-ps](texldb---ps.md)、 [texldd](texldd---ps.md) ) 可能會相依于最多第三個順序。</span><span class="sxs-lookup"><span data-stu-id="4fed1-118">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="4fed1-119">第一個順序相依材質指令是一個材質指令，其中：</span><span class="sxs-lookup"><span data-stu-id="4fed1-119">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="4fed1-120">src0 是 (r) 的 [暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \# 。</span><span class="sxs-lookup"><span data-stu-id="4fed1-120">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="4fed1-121">dst 先前已寫入，現在正在撰寫中。</span><span class="sxs-lookup"><span data-stu-id="4fed1-121">dst was previously written, now being written again.</span></span>

<span data-ttu-id="4fed1-122">第二個順序相依的材質指令定義為材質指令，可讀取或寫入 [暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 其內容在執行材質 (指令之前的內容，可能會在第一個順序相依材質指令的結果上間接) 。</span><span class="sxs-lookup"><span data-stu-id="4fed1-122">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="4fed1-123"> (n) <sup>第</sup>一個順序的相依材質指令會衍生自 (n-1) <sup>第</sup>一個順序的材質指令。</span><span class="sxs-lookup"><span data-stu-id="4fed1-123">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="4fed1-124">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4fed1-124">ps\_3\_0</span></span>

<span data-ttu-id="4fed1-125">src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \#) ，沒有修飾詞的取樣器。</span><span class="sxs-lookup"><span data-stu-id="4fed1-125">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="4fed1-126">Swizzle 可在 src0 或 src1 上使用。</span><span class="sxs-lookup"><span data-stu-id="4fed1-126">Swizzle is allowed on src0 or src1.</span></span> <span data-ttu-id="4fed1-127">Swizzle 會在紋理查閱之前套用至材質 coordintates。</span><span class="sxs-lookup"><span data-stu-id="4fed1-127">The swizzle is applied to the texture coordintates before texture lookup.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fed1-128">備註</span><span class="sxs-lookup"><span data-stu-id="4fed1-128">Remarks</span></span>

<span data-ttu-id="4fed1-129">下列版本支援此指令：</span><span class="sxs-lookup"><span data-stu-id="4fed1-129">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="4fed1-130">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="4fed1-130">Pixel shader versions</span></span> | <span data-ttu-id="4fed1-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="4fed1-131">1\_1</span></span> | <span data-ttu-id="4fed1-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="4fed1-132">1\_2</span></span> | <span data-ttu-id="4fed1-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4fed1-133">1\_3</span></span> | <span data-ttu-id="4fed1-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="4fed1-134">1\_4</span></span> | <span data-ttu-id="4fed1-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4fed1-135">2\_0</span></span> | <span data-ttu-id="4fed1-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4fed1-136">2\_x</span></span> | <span data-ttu-id="4fed1-137">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4fed1-137">2\_sw</span></span> | <span data-ttu-id="4fed1-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4fed1-138">3\_0</span></span> | <span data-ttu-id="4fed1-139">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4fed1-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4fed1-140">texld</span><span class="sxs-lookup"><span data-stu-id="4fed1-140">texld</span></span>                 |      |      |      |      | <span data-ttu-id="4fed1-141">x</span><span class="sxs-lookup"><span data-stu-id="4fed1-141">x</span></span>    | <span data-ttu-id="4fed1-142">x</span><span class="sxs-lookup"><span data-stu-id="4fed1-142">x</span></span>    | <span data-ttu-id="4fed1-143">x</span><span class="sxs-lookup"><span data-stu-id="4fed1-143">x</span></span>     | <span data-ttu-id="4fed1-144">x</span><span class="sxs-lookup"><span data-stu-id="4fed1-144">x</span></span>    | <span data-ttu-id="4fed1-145">x</span><span class="sxs-lookup"><span data-stu-id="4fed1-145">x</span></span>     |



 

<span data-ttu-id="4fed1-146">Src0 執行材質範例所需的座標數目取決於 src1 的宣告方式，以及 w 元件。</span><span class="sxs-lookup"><span data-stu-id="4fed1-146">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="4fed1-147">取樣器型別是以 [dcl \_ samplerType 宣告 (sm2、sm3 ps asm) ](dcl-samplertype---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="4fed1-147">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="4fed1-148">如果 src1 宣告為2D 取樣器，則 src0 必須包含 xy 座標;如果 src1 宣告為 cube 取樣器或磁片區取樣器，則 src0 必須包含 xyz 座標。</span><span class="sxs-lookup"><span data-stu-id="4fed1-148">If src1 is declared as a 2D sampler, then src0 must contain .xy coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyz coordinates.</span></span> <span data-ttu-id="4fed1-149">因為已忽略額外的材質座標元件 () ，所以允許取樣的維度數量少於材質座標中的材質。</span><span class="sxs-lookup"><span data-stu-id="4fed1-149">Sampling a texture with fewer dimensions than are present in the texture coordinate is allowed since the extra texture coordinate component(s) are ignored.</span></span>

<span data-ttu-id="4fed1-150">如果來源材質包含四個以上的元件，預設值就會放置在遺漏的元件中。</span><span class="sxs-lookup"><span data-stu-id="4fed1-150">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="4fed1-151">預設值取決於下表所示的材質格式：</span><span class="sxs-lookup"><span data-stu-id="4fed1-151">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="4fed1-152">材質格式</span><span class="sxs-lookup"><span data-stu-id="4fed1-152">Texture Format</span></span>                                                                                          | <span data-ttu-id="4fed1-153">預設值</span><span class="sxs-lookup"><span data-stu-id="4fed1-153">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="4fed1-154">D3DFMT \_ R5G6B5、D3DFMT \_ R8G8B8、D3DFMT \_ L8、D3DFMT \_ l16 也、D3DFMT \_ R3G3B2、D3DFMT \_ CxV8U8、D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="4fed1-154">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="4fed1-155">A = 1。0</span><span class="sxs-lookup"><span data-stu-id="4fed1-155">A = 1.0</span></span>              |
| <span data-ttu-id="4fed1-156">D3DFMT \_ V8U8、D3DFMT \_ V16U16、D3DFMT \_ G16R16、D3DFMT \_ G16R16F、D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="4fed1-156">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="4fed1-157">B = A = 1。0</span><span class="sxs-lookup"><span data-stu-id="4fed1-157">B = A = 1.0</span></span>          |
| <span data-ttu-id="4fed1-158">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="4fed1-158">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="4fed1-159">R = G = B = 0。0</span><span class="sxs-lookup"><span data-stu-id="4fed1-159">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="4fed1-160">D3DFMT \_ R16F、D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="4fed1-160">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="4fed1-161">G = B = A = 1。0</span><span class="sxs-lookup"><span data-stu-id="4fed1-161">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="4fed1-162">所有深度/樣板格式</span><span class="sxs-lookup"><span data-stu-id="4fed1-162">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="4fed1-163">R = B = 0.0，A = 1。0</span><span class="sxs-lookup"><span data-stu-id="4fed1-163">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4fed1-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="4fed1-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fed1-165">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="4fed1-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 