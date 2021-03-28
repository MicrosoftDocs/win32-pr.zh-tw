---
title: 'ld (sm4-asm) '
description: 從指定的緩衝區或紋理中提取資料，而不進行任何篩選 (例如，使用提供的整數位址) 點取樣。 來源資料可能來自于 TextureCube 以外的任何資源類型。
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313683"
---
# <a name="ld-sm4---asm"></a><span data-ttu-id="26f26-104">ld (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="26f26-104">ld (sm4 - asm)</span></span>

<span data-ttu-id="26f26-105">從指定的緩衝區或紋理中提取資料，而不進行任何篩選 (例如，使用提供的整數位址) 點取樣。</span><span class="sxs-lookup"><span data-stu-id="26f26-105">Fetches data from the specified buffer or texture without any filtering (e.g. point sampling) using the provided integer address.</span></span> <span data-ttu-id="26f26-106">來源資料可能來自于 TextureCube 以外的任何資源類型。</span><span class="sxs-lookup"><span data-stu-id="26f26-106">The source data may come from any resource type, other than TextureCube.</span></span>



| <span data-ttu-id="26f26-107">ld \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="26f26-107">ld\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="26f26-108">項目</span><span class="sxs-lookup"><span data-stu-id="26f26-108">Item</span></span>                                                                                                               | <span data-ttu-id="26f26-109">描述</span><span class="sxs-lookup"><span data-stu-id="26f26-109">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f26-110"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="26f26-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="26f26-111">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="26f26-111">\[in\] The address of the result of the operation.</span></span><br/>                                                               |
| <span data-ttu-id="26f26-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="26f26-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="26f26-113">\[在 \] 執行範例所需的材質座標中。</span><span class="sxs-lookup"><span data-stu-id="26f26-113">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                     |
| <span data-ttu-id="26f26-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="26f26-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="26f26-115">\[在材質暫存器中 \] (t) 必須已經宣告， \# 以識別要從中提取的材質或緩衝區。</span><span class="sxs-lookup"><span data-stu-id="26f26-115">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26f26-116">備註</span><span class="sxs-lookup"><span data-stu-id="26f26-116">Remarks</span></span>

<span data-ttu-id="26f26-117">此指令是 [範例](sample--sm4---asm-.md) 指令的簡化替代方法。</span><span class="sxs-lookup"><span data-stu-id="26f26-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="26f26-118">不同于 **範例**， **ld** 也可以從緩衝區中提取資料。</span><span class="sxs-lookup"><span data-stu-id="26f26-118">Unlike **sample**, **ld** is also capable of fetching data from buffers.</span></span> <span data-ttu-id="26f26-119">**ld** 也可以從多範例資源中提取 (只) 圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="26f26-119">**ld** is can also fetch from multi-sample resources (on pixel shader only).</span></span>

<span data-ttu-id="26f26-120">*srcAddress* 提供以不帶正負號整數形式執行範例所需的材質座標集合。</span><span class="sxs-lookup"><span data-stu-id="26f26-120">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="26f26-121">如果 *srcAddress* 超出 \[ 維度 1) 中的範圍 0 ... (\# 材質 \] ，則會叫用超出範圍的行為，其中 **ld** 會在 *srcResource* 格式的所有非遺漏元件中傳回0，並將遺漏元件的預設值傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="26f26-121">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], then out-of-bounds behavior is invoked, where **ld** returns 0 in all non-missing components of the format of the *srcResource*, and the default for missing components.</span></span> <span data-ttu-id="26f26-122">希望能更靈活地控制超出範圍的位址行為的應用程式應該改用 **範例** 指令，因為它會接受定義為取樣器狀態的位址包裝/鏡像/夾具/框線行為。</span><span class="sxs-lookup"><span data-stu-id="26f26-122">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="26f26-123">*srcAddress：* (POS swizzle) 一律提供不帶正負號的整數 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="26f26-123">*srcAddress.a* (POS-swizzle) always provides an unsigned integer mipmap level.</span></span> <span data-ttu-id="26f26-124">如果值超出範圍 \[ 0 ... (num miplevels 在資源 1) \]) 中，則會叫用超出範圍行為。</span><span class="sxs-lookup"><span data-stu-id="26f26-124">If the value is out of the range \[0...(num miplevels in resource-1)\]), then out-of-bounds behavior is invoked.</span></span> <span data-ttu-id="26f26-125">如果資源是緩衝區，它不能有任何 mipmap，則會忽略 *srcAddress*</span><span class="sxs-lookup"><span data-stu-id="26f26-125">If the resource is a buffer, which can not have any mipmaps, then *srcAddress.a* is ignored</span></span>

<span data-ttu-id="26f26-126">如果緩衝區和 texture1D (非陣列) ，則會忽略 *srcAddress* (POS-swizzle) 。</span><span class="sxs-lookup"><span data-stu-id="26f26-126">*srcAddress.gb* (POS-swizzle) is ignored for buffers and texture1D (non-Array).</span></span> <span data-ttu-id="26f26-127">texture1D 陣列和 texture2Ds 會忽略 *srcAddress b.* (POS-swizzle) 。</span><span class="sxs-lookup"><span data-stu-id="26f26-127">*srcAddress.b* (POS-swizzle) is ignored for texture1D arrays and texture2Ds.</span></span>

<span data-ttu-id="26f26-128">若是 texture1D 陣列， *srcAddress. g* (POS-swizzle) 提供陣列索引做為不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="26f26-128">For texture1D arrays, *srcAddress.g* (POS-swizzle) provides the array index as an unsigned integer.</span></span> <span data-ttu-id="26f26-129">如果值超出可用陣列索引的範圍 \[ 0 ... (陣列大小-1) \] ，則會叫用超出範圍行為。</span><span class="sxs-lookup"><span data-stu-id="26f26-129">If the value is out of the range of available array indices \[0...(array size-1)\], then out-of-bounds behavior is invoked.</span></span>

<span data-ttu-id="26f26-130">針對 texture2D 陣列， *srcAddress. b* (POS-swizzle) 提供陣列索引，否則為與 texture1D 相同的語義。</span><span class="sxs-lookup"><span data-stu-id="26f26-130">For texture2D arrays, *srcAddress.b* (POS-swizzle) provides the array index, otherwise with same semantics as for texture1D.</span></span>

<span data-ttu-id="26f26-131">從沒有任何系結的 *t \#* 進行提取，會針對所有元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="26f26-131">Fetching from *t\#* that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="26f26-132">位址位移</span><span class="sxs-lookup"><span data-stu-id="26f26-132">Address Offset</span></span>

<span data-ttu-id="26f26-133">選擇性的 \[ \_ aoffimmi (u，v，w) \] 尾碼 (以立即整數的位址位移) 表示 **ld** 的材質座標是以一組提供的立即材質空間整數常數值來位移。</span><span class="sxs-lookup"><span data-stu-id="26f26-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="26f26-134">常值是一組4位2的補數數位，具有整數範圍 \[ -8，7 \] 。</span><span class="sxs-lookup"><span data-stu-id="26f26-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="26f26-135">此修飾詞只會針對 texture1D/2D/3D 定義，包括陣列，而不是針對緩衝區。</span><span class="sxs-lookup"><span data-stu-id="26f26-135">This modifier is defined only for texture1D/2D/3D, including arrays, and not for buffers.</span></span>

<span data-ttu-id="26f26-136">位移會新增至材質座標（在材質空間中），相對於 **ld** 所存取的 miplevel。</span><span class="sxs-lookup"><span data-stu-id="26f26-136">The offsets are added to the texture coordinates, in texel space, relative to the miplevel being accessed by the **ld**.</span></span>

<span data-ttu-id="26f26-137">Texture1D/2D 陣列的陣列軸並不會套用位址位移。</span><span class="sxs-lookup"><span data-stu-id="26f26-137">Address offsets are not applied along the array axis of texture1D/2D arrays.</span></span>

<span data-ttu-id="26f26-138">*\_ Aoffimmi v （w）* 會忽略 texture1Ds 的元件。</span><span class="sxs-lookup"><span data-stu-id="26f26-138">The *\_aoffimmi v,w* components are ignored for texture1Ds.</span></span>

<span data-ttu-id="26f26-139">Texture2Ds 會忽略 *\_ aoffimmi w* 元件。</span><span class="sxs-lookup"><span data-stu-id="26f26-139">The *\_aoffimmi w* component is ignored for texture2Ds.</span></span>

<span data-ttu-id="26f26-140">因為 **ld** 的材質座標是不帶正負號的整數，所以如果位移導致位址小於零，則會換行至大型位址，並產生超出範圍的存取權。</span><span class="sxs-lookup"><span data-stu-id="26f26-140">Because the texture coordinates for **ld** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="26f26-141">傳回型別控制項</span><span class="sxs-lookup"><span data-stu-id="26f26-141">Return Type Control</span></span>

<span data-ttu-id="26f26-142">**Ld** 所傳回的資料格式會以與 **範例** 指令所述的相同方式來決定;它是以系結至 *srcResource* 參數 (*t \#*) 的格式為基礎。</span><span class="sxs-lookup"><span data-stu-id="26f26-142">The data format returned by **ld** to the destination register is determined in the same way as described for the **sample** instruction; it is based on the format bound to the *srcResource* parameter (*t\#*).</span></span>

<span data-ttu-id="26f26-143">如同 **範例** 指令一樣， **ld** 的傳回值為4向量，以及格式不存在之元件的格式特定預設值。</span><span class="sxs-lookup"><span data-stu-id="26f26-143">As with the **sample** instruction, returned values for **ld** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="26f26-144">*SrcResource* 上的 swizzle 會決定如何 swizzle 從材質載入傳回的4個元件結果。在 *目的地* 上的遮罩可判斷在 *dest* 中的哪些元件已更新。</span><span class="sxs-lookup"><span data-stu-id="26f26-144">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="26f26-145">當 *ld* 將32位浮點值讀入32位的暫存器時，不會改變位;也就是說，denormal 值仍維持 denormal。</span><span class="sxs-lookup"><span data-stu-id="26f26-145">When a 32-bit float value is read by *ld* into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="26f26-146">這與 **範例** 指令不同。</span><span class="sxs-lookup"><span data-stu-id="26f26-146">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="26f26-147">其他詳細資料</span><span class="sxs-lookup"><span data-stu-id="26f26-147">Miscellaneous Details</span></span>

<span data-ttu-id="26f26-148">因為沒有與 **ld** 指令相關聯的篩選，」 lod 偏差這類概念並不適用于 **ld**。</span><span class="sxs-lookup"><span data-stu-id="26f26-148">As there is no filtering associated with the **ld** instruction, concepts like LOD bias do not apply to **ld**.</span></span> <span data-ttu-id="26f26-149">因此，沒有任何取樣 *器 \# s* 參數。</span><span class="sxs-lookup"><span data-stu-id="26f26-149">Accordingly there is no sampler *s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="26f26-150">限制</span><span class="sxs-lookup"><span data-stu-id="26f26-150">Restrictions</span></span>

-   <span data-ttu-id="26f26-151">*srcResource* 必須是 t \# 註冊，而不是 TextureCube。</span><span class="sxs-lookup"><span data-stu-id="26f26-151">*srcResource* must be a t\# register, and not a TextureCube.</span></span> <span data-ttu-id="26f26-152">*srcResource* 不可以是 constantbuffer，因為無法系結至 t \# 註冊。</span><span class="sxs-lookup"><span data-stu-id="26f26-152">*srcResource* cannot be a constantbuffer either, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="26f26-153">不允許 *srcResource* 的相對定址。</span><span class="sxs-lookup"><span data-stu-id="26f26-153">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="26f26-154">*srcAddress* 必須是 temp (r \# /x \#) 、常數 (cb \#) 或輸入 (v \#) register。</span><span class="sxs-lookup"><span data-stu-id="26f26-154">*srcAddress* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="26f26-155">*dest* 必須是 temp (r \# /x \#) 或 output (o \* \#) register。</span><span class="sxs-lookup"><span data-stu-id="26f26-155">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="26f26-156">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="26f26-156">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="26f26-157">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="26f26-157">Vertex Shader</span></span> | <span data-ttu-id="26f26-158">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="26f26-158">Geometry Shader</span></span> | <span data-ttu-id="26f26-159">像素著色器</span><span class="sxs-lookup"><span data-stu-id="26f26-159">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="26f26-160">x</span><span class="sxs-lookup"><span data-stu-id="26f26-160">x</span></span>             | <span data-ttu-id="26f26-161">x</span><span class="sxs-lookup"><span data-stu-id="26f26-161">x</span></span>               | <span data-ttu-id="26f26-162">x</span><span class="sxs-lookup"><span data-stu-id="26f26-162">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="26f26-163">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="26f26-163">Minimum Shader Model</span></span>

<span data-ttu-id="26f26-164">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="26f26-164">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="26f26-165">著色器模型</span><span class="sxs-lookup"><span data-stu-id="26f26-165">Shader Model</span></span>                                              | <span data-ttu-id="26f26-166">支援</span><span class="sxs-lookup"><span data-stu-id="26f26-166">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="26f26-167">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="26f26-167">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="26f26-168">是</span><span class="sxs-lookup"><span data-stu-id="26f26-168">yes</span></span>       |
| [<span data-ttu-id="26f26-169">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="26f26-169">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="26f26-170">是</span><span class="sxs-lookup"><span data-stu-id="26f26-170">yes</span></span>       |
| [<span data-ttu-id="26f26-171">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="26f26-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="26f26-172">是</span><span class="sxs-lookup"><span data-stu-id="26f26-172">yes</span></span>       |
| [<span data-ttu-id="26f26-173">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="26f26-173">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="26f26-174">不可以</span><span class="sxs-lookup"><span data-stu-id="26f26-174">no</span></span>        |
| [<span data-ttu-id="26f26-175">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="26f26-175">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="26f26-176">不可以</span><span class="sxs-lookup"><span data-stu-id="26f26-176">no</span></span>        |
| [<span data-ttu-id="26f26-177">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="26f26-177">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="26f26-178">不可以</span><span class="sxs-lookup"><span data-stu-id="26f26-178">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="26f26-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="26f26-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f26-180">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="26f26-180">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





