---
title: 'ld2dms (sm 4.1-asm) '
description: 從二維多範例紋理讀取個別樣本。
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092457"
---
# <a name="ld2dms-sm41---asm"></a><span data-ttu-id="2401a-103">ld2dms (sm 4.1-asm) </span><span class="sxs-lookup"><span data-stu-id="2401a-103">ld2dms (sm4.1 - asm)</span></span>

<span data-ttu-id="2401a-104">從二維多範例紋理讀取個別樣本。</span><span class="sxs-lookup"><span data-stu-id="2401a-104">Reads individual samples out of 2-dimensional multi-sample textures.</span></span>



| <span data-ttu-id="2401a-105">ld2dms \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource、swizzle \[ \] 、sampleIndex (純量運算元) </span><span class="sxs-lookup"><span data-stu-id="2401a-105">ld2dms\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2401a-106">項目</span><span class="sxs-lookup"><span data-stu-id="2401a-106">Item</span></span>                                                                                                               | <span data-ttu-id="2401a-107">描述</span><span class="sxs-lookup"><span data-stu-id="2401a-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2401a-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="2401a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="2401a-109">\[在作業的 \] 結果位址中。</span><span class="sxs-lookup"><span data-stu-id="2401a-109">\[in\] The address of result of the operation.</span></span> <br/>                                                                 |
| <span data-ttu-id="2401a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2401a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="2401a-111">\[在 \] 執行範例所需的材質座標中。</span><span class="sxs-lookup"><span data-stu-id="2401a-111">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                    |
| <span data-ttu-id="2401a-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="2401a-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="2401a-113">\[在材質暫存器中 \] (t) 必須已經宣告， \# 以識別要從中提取的材質或緩衝區</span><span class="sxs-lookup"><span data-stu-id="2401a-113">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from</span></span><br/> |
| <span data-ttu-id="2401a-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="2401a-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="2401a-115">\[在 \] Idendifies 中，從 *srcResource* 讀取的範例。</span><span class="sxs-lookup"><span data-stu-id="2401a-115">\[in\] Idendifies the samples to read from *srcResource*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="2401a-116">備註</span><span class="sxs-lookup"><span data-stu-id="2401a-116">Remarks</span></span>

<span data-ttu-id="2401a-117">此指令是 [範例](sample--sm4---asm-.md) 指令的簡化替代方法。</span><span class="sxs-lookup"><span data-stu-id="2401a-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="2401a-118">它會從指定的材質中提取資料，而不需要任何篩選 (例如，使用提供的整數 *srcAddress* 和 *sampleIndex* 點取樣) 。</span><span class="sxs-lookup"><span data-stu-id="2401a-118">It fetches data from the specified Texture without any filtering (e.g. point sampling) using the provided integer *srcAddress* and *sampleIndex*.</span></span>

<span data-ttu-id="2401a-119">*srcAddress* 提供以不帶正負號整數形式執行範例所需的材質座標集合。</span><span class="sxs-lookup"><span data-stu-id="2401a-119">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="2401a-120">如果 *srcAddress* 超出 \[ 維度-1) 的範圍 0 ... (\# 材質 \] ， **ld2dms** 一律會在以資源格式呈現的所有元件中傳回0，並預設 (0、0、0、1.0 f/0x00000001) 用於遺漏的元件。</span><span class="sxs-lookup"><span data-stu-id="2401a-120">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="2401a-121">*sampleIndex* 不必是常值。</span><span class="sxs-lookup"><span data-stu-id="2401a-121">*sampleIndex* does not have to be a literal.</span></span> <span data-ttu-id="2401a-122">不需要在材質資源上指定多樣本計數，它可以搭配深度或樣板視圖使用。</span><span class="sxs-lookup"><span data-stu-id="2401a-122">The multi-sample count does not have to be specified on the texture resource, and it works with depth or stencil views.</span></span>

<span data-ttu-id="2401a-123">希望能更靈活地控制超出範圍的位址行為的應用程式應該改用 **範例** 指令，因為它會接受定義為取樣器狀態的位址包裝/鏡像/夾具/框線行為。</span><span class="sxs-lookup"><span data-stu-id="2401a-123">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="2401a-124">Texture2Ds 會忽略 *srcAddress. b* (swizzle 後) 。</span><span class="sxs-lookup"><span data-stu-id="2401a-124">*srcAddress.b* (post-swizzle) is ignored for Texture2Ds.</span></span> <span data-ttu-id="2401a-125">如果值超出可用陣列索引的範圍 \[ 0 ... (陣列大小-1) \] ，則 **ld2dms** 一律會在以資源格式呈現的所有元件中傳回0，並預設 (0、0、0、1.0 f/0x00000001) 用於遺漏的元件。</span><span class="sxs-lookup"><span data-stu-id="2401a-125">If the value is out of the range of available array indices \[0...(array size-1)\], then **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="2401a-126">若是 Texture2D 陣列， *srcAddress. b* (swizzle 後) 會提供陣列索引。</span><span class="sxs-lookup"><span data-stu-id="2401a-126">For Texture2D Arrays, *srcAddress.b* (post-swizzle) provides the array index.</span></span> <span data-ttu-id="2401a-127">Oherwise 與 Texture2D 具有相同的行為。</span><span class="sxs-lookup"><span data-stu-id="2401a-127">Oherwise it has the same behavior as Texture2D.</span></span>

<span data-ttu-id="2401a-128">*srcAddress* swizzle 後 (的) 一律會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2401a-128">*srcAddress.a* (post-swizzle) is always ignored.</span></span> <span data-ttu-id="2401a-129">HLSL 編譯器永遠不會輸出任何結果。</span><span class="sxs-lookup"><span data-stu-id="2401a-129">The HLSL compiler will never output anything there.</span></span>

<span data-ttu-id="2401a-130">*srcResource* 是 (t) 的材質暫存器 \# ，必須宣告為 (22.3.11) ，以識別要從中提取的材質。</span><span class="sxs-lookup"><span data-stu-id="2401a-130">*srcResource* is a texture register (t\#) which must have been declared(22.3.11), identifying which Texture to fetch from.</span></span>

<span data-ttu-id="2401a-131">從沒有任何系結的 t 進行提取 \# ，會針對所有元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="2401a-131">Fetching from t\# that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="2401a-132">位址位移</span><span class="sxs-lookup"><span data-stu-id="2401a-132">Address Offset</span></span>

<span data-ttu-id="2401a-133">選擇性的 \[ \_ aoffimmi (u，v，w) \] 尾碼 (以立即整數的位址位移) 表示 **ld2dms** 的材質座標是以一組提供的立即材質空間整數常數值來位移。</span><span class="sxs-lookup"><span data-stu-id="2401a-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld2dms** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="2401a-134">常值是一組4位2的補數數位，具有整數範圍 \[ -8，7 \] 。</span><span class="sxs-lookup"><span data-stu-id="2401a-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span>

<span data-ttu-id="2401a-135">位移會新增至材質座標的材質空間中。</span><span class="sxs-lookup"><span data-stu-id="2401a-135">The offsets are added to the texture coordinates, in texel space.</span></span>

<span data-ttu-id="2401a-136">Texture1D/2D 陣列的陣列軸並不會套用位址位移。</span><span class="sxs-lookup"><span data-stu-id="2401a-136">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="2401a-137">*\_ Aoffimmi v （w）* 會忽略 Texture1Ds 的元件。</span><span class="sxs-lookup"><span data-stu-id="2401a-137">The *\_aoffimmi v,w* components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="2401a-138">Texture2Ds 會忽略 *\_ aoffimmi w* 元件。</span><span class="sxs-lookup"><span data-stu-id="2401a-138">The *\_aoffimmi w* component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="2401a-139">因為 **ld2dms** 的材質座標是不帶正負號的整數，所以如果位移導致位址小於零，則會將它換成較大的位址，並產生超出範圍的存取權，例如 **ld** 會在以資源格式呈現的所有元件中傳回0，而遺漏元件的預設值 (0、0、0、1.0 f/0x00000001) 。</span><span class="sxs-lookup"><span data-stu-id="2401a-139">Because the texture coordinates for **ld2dms** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access, which like **ld** returns 0 in all components present in the format of the resource, and the defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

### <a name="sample-number"></a><span data-ttu-id="2401a-140">範例編號</span><span class="sxs-lookup"><span data-stu-id="2401a-140">Sample Number</span></span>

<span data-ttu-id="2401a-141">**ld2dms** 可用於任何資源。</span><span class="sxs-lookup"><span data-stu-id="2401a-141">**ld2dms** is available for use on any resource.</span></span> <span data-ttu-id="2401a-142">**ld2dms** 的運作方式與 **ld** 相同（除了 2d multsample 資源），方法是使用額外的 (0 為基礎的) *sampleIndex* 運算元來識別要從資源中讀取的範例。</span><span class="sxs-lookup"><span data-stu-id="2401a-142">**ld2dms** operates identically to **ld** except on 2D multsample resources, by using the additional (0-based) *sampleIndex* operand to identify which sample to read from the resource.</span></span>

<span data-ttu-id="2401a-143">指定 *sampleIndex* 超過資源中樣本數目的結果是未定義的，但無法傳回裝置內容之位址空間以外的資料。</span><span class="sxs-lookup"><span data-stu-id="2401a-143">The result of specifying a *sampleIndex* that exceeds the number of samples in the resource is undefined, but cannot return data outside of the address space of the device context.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="2401a-144">傳回型別控制項</span><span class="sxs-lookup"><span data-stu-id="2401a-144">Return Type Control</span></span>

<span data-ttu-id="2401a-145">**Ld2dms** 所傳回的資料格式是以與 **範例** 指令所述的相同方式來決定。</span><span class="sxs-lookup"><span data-stu-id="2401a-145">The data format returned by **ld2dms** to the destination register is determined in the same way as described for the **sample** instruction.</span></span> <span data-ttu-id="2401a-146">它是以系結至 *srcResource* 參數 (t) 的格式為基礎 \# 。</span><span class="sxs-lookup"><span data-stu-id="2401a-146">It is based on the format bound to the *srcResource* parameter (t\#).</span></span>

<span data-ttu-id="2401a-147">如同 **範例** 指令一樣， **ld2dms** 的傳回值為4向量，以及格式不存在之元件的格式特定預設值。</span><span class="sxs-lookup"><span data-stu-id="2401a-147">As with the **sample** instruction, returned values for **ld2dms** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="2401a-148">*SrcResource* 上的 swizzle 會決定如何 swizzle 從材質載入傳回的4個元件結果。在 *目的地* 上的遮罩可判斷在 *dest* 中的哪些元件已更新。</span><span class="sxs-lookup"><span data-stu-id="2401a-148">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="2401a-149">當 **ld2dms** 將32位的 float 值讀入32位的暫存器時，不會改變位;也就是說，denormal 值仍維持 denormal。</span><span class="sxs-lookup"><span data-stu-id="2401a-149">When a 32-bit float value is read by **ld2dms** into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="2401a-150">這與 **範例** 指令不同。</span><span class="sxs-lookup"><span data-stu-id="2401a-150">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="2401a-151">其他詳細資料</span><span class="sxs-lookup"><span data-stu-id="2401a-151">Miscellaneous Details</span></span>

<span data-ttu-id="2401a-152">因為沒有與此指令相關聯的篩選，所以不適用」 LOD 偏差之類的概念。</span><span class="sxs-lookup"><span data-stu-id="2401a-152">As there is no filtering associated with this instruction, concepts like LOD bias do not apply.</span></span> <span data-ttu-id="2401a-153">因此，沒有任何 *取樣器 \# s* 參數。</span><span class="sxs-lookup"><span data-stu-id="2401a-153">Accordingly there is no *sampler s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="2401a-154">限制</span><span class="sxs-lookup"><span data-stu-id="2401a-154">Restrictions</span></span>

-   <span data-ttu-id="2401a-155">*srcResource* 必須是 t \# 註冊，而不是 TextureCube、Texture1D 或 Texture1DArray。</span><span class="sxs-lookup"><span data-stu-id="2401a-155">*srcResource* must be a t\# register, and not a TextureCube, Texture1D or Texture1DArray.</span></span> <span data-ttu-id="2401a-156">*srcResource* 不能是無法系結至 t 註冊的 ConstantBuffer \# 。</span><span class="sxs-lookup"><span data-stu-id="2401a-156">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="2401a-157">不允許 *srcResource* 的相對定址。</span><span class="sxs-lookup"><span data-stu-id="2401a-157">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="2401a-158">*srcAddress* 和 *sampleIndex* 必須是 temp (r \# /x \#) 、常數 (cb \#) 或輸入 (v \#) register。</span><span class="sxs-lookup"><span data-stu-id="2401a-158">*srcAddress* and *sampleIndex* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="2401a-159">*dest* 必須是 temp (r \# /x \#) 或 output (o \* \#) register。</span><span class="sxs-lookup"><span data-stu-id="2401a-159">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="2401a-160">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="2401a-160">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2401a-161">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="2401a-161">Vertex Shader</span></span> | <span data-ttu-id="2401a-162">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="2401a-162">Geometry Shader</span></span> | <span data-ttu-id="2401a-163">像素著色器</span><span class="sxs-lookup"><span data-stu-id="2401a-163">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2401a-164">x</span><span class="sxs-lookup"><span data-stu-id="2401a-164">x</span></span>             | <span data-ttu-id="2401a-165">x</span><span class="sxs-lookup"><span data-stu-id="2401a-165">x</span></span>               | <span data-ttu-id="2401a-166">x</span><span class="sxs-lookup"><span data-stu-id="2401a-166">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2401a-167">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2401a-167">Minimum Shader Model</span></span>

<span data-ttu-id="2401a-168">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2401a-168">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2401a-169">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2401a-169">Shader Model</span></span>                                              | <span data-ttu-id="2401a-170">支援</span><span class="sxs-lookup"><span data-stu-id="2401a-170">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2401a-171">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2401a-171">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2401a-172">是</span><span class="sxs-lookup"><span data-stu-id="2401a-172">yes</span></span>       |
| [<span data-ttu-id="2401a-173">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="2401a-173">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2401a-174">是</span><span class="sxs-lookup"><span data-stu-id="2401a-174">yes</span></span>       |
| [<span data-ttu-id="2401a-175">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="2401a-175">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2401a-176">不可以</span><span class="sxs-lookup"><span data-stu-id="2401a-176">no</span></span>        |
| [<span data-ttu-id="2401a-177">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2401a-177">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2401a-178">不可以</span><span class="sxs-lookup"><span data-stu-id="2401a-178">no</span></span>        |
| [<span data-ttu-id="2401a-179">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2401a-179">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2401a-180">不可以</span><span class="sxs-lookup"><span data-stu-id="2401a-180">no</span></span>        |
| [<span data-ttu-id="2401a-181">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2401a-181">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2401a-182">不可以</span><span class="sxs-lookup"><span data-stu-id="2401a-182">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2401a-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="2401a-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2401a-184">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2401a-184">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





