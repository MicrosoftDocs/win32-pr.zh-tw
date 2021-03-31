---
title: 'ld_structured (sm5-asm) '
description: 從結構化緩衝區中讀取 1-4 32 位元件的隨機存取。
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373831"
---
# <a name="ld_structured-sm5---asm"></a><span data-ttu-id="2ac72-103">ld \_ 結構化 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="2ac72-103">ld\_structured (sm5 - asm)</span></span>

<span data-ttu-id="2ac72-104">從結構化緩衝區中讀取 1-4 32 位元件的隨機存取。</span><span class="sxs-lookup"><span data-stu-id="2ac72-104">Random-access read of 1-4 32bit components from a structured buffer.</span></span>



| <span data-ttu-id="2ac72-105">： ld \_ 結構化 dst0 \[ . mask \] ，srcAddress \[ . select \_ component \] ，srcByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2ac72-105">: ld\_structured dst0\[.mask\], srcAddress\[.select\_component\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2ac72-106">項目</span><span class="sxs-lookup"><span data-stu-id="2ac72-106">Item</span></span>                                                                                                                       | <span data-ttu-id="2ac72-107">描述</span><span class="sxs-lookup"><span data-stu-id="2ac72-107">Description</span></span>                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac72-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="2ac72-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="2ac72-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="2ac72-109">\[in\] The address of the results of the operation.</span></span><br/>                                                                                             |
| <span data-ttu-id="2ac72-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2ac72-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>             | <span data-ttu-id="2ac72-111">\[在中， \] 指定要讀取之結構的索引。</span><span class="sxs-lookup"><span data-stu-id="2ac72-111">\[in\] Specifies the index of the structure to read.</span></span><br/>                                                                                            |
| <span data-ttu-id="2ac72-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="2ac72-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="2ac72-113">\[在中， \] 指定要開始讀取的結構中的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="2ac72-113">\[in\] Specifies the byte offset in the structure to start reading from.</span></span> <br/>                                                                       |
| <span data-ttu-id="2ac72-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2ac72-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="2ac72-115">要從中讀取的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2ac72-115">The buffer to read from.</span></span> <span data-ttu-id="2ac72-116">此參數必須是 SRV (t \#) ，UAV (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="2ac72-116">This parameter must be a SRV (t\#), UAV (u\#).</span></span> <span data-ttu-id="2ac72-117">在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="2ac72-117">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ac72-118">備註</span><span class="sxs-lookup"><span data-stu-id="2ac72-118">Remarks</span></span>

<span data-ttu-id="2ac72-119">從結構讀取的資料相當於下列虛擬程式碼：其中有位移、位址、緩衝區內容的指標、來源的 stride，以及以線性方式儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="2ac72-119">The data read from the structure is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="2ac72-120">這個虛擬虛擬的會顯示作業的運作方式，但實際的資料不需要以線性方式儲存。</span><span class="sxs-lookup"><span data-stu-id="2ac72-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="2ac72-121">如果資料不是以線性方式儲存，則實際的指令運算必須符合上述作業的行為。</span><span class="sxs-lookup"><span data-stu-id="2ac72-121">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="2ac72-122">除了 SrcByteOffset 之外，任何給定32位元件之 u/t 上的界限定址都會傳回 \# \# 0，但除了，加上 swizzle 也會導致超出範圍存取您/t 的限制之外 \# \# ，所有元件)  (的傳回值都是未定義的。</span><span class="sxs-lookup"><span data-stu-id="2ac72-122">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component, except if *srcByteOffset*, plus swizzle is what causes out of bounds access to u\#/t\#, the returned value for all component(s) is undefined.</span></span>

<span data-ttu-id="2ac72-123">G (界限的範圍外， \# 該特定 g 的界限 \# ，而非任何指定32位元件的所有共用記憶體) 會傳回未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="2ac72-123">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="2ac72-124">*srcByteOffset* 是不同于 *srcAddress* 的引數，因為它通常是常值。</span><span class="sxs-lookup"><span data-stu-id="2ac72-124">*srcByteOffset* is a separate argument from *srcAddress* because it is commonly a literal.</span></span> <span data-ttu-id="2ac72-125">尚未對結構化記憶體上的 atomics 執行此參數分離。</span><span class="sxs-lookup"><span data-stu-id="2ac72-125">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="2ac72-126">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV、SRV 和 TGSM 的指令。</span><span class="sxs-lookup"><span data-stu-id="2ac72-126">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV, and TGSM.</span></span>

<span data-ttu-id="2ac72-127">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="2ac72-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2ac72-128">頂點</span><span class="sxs-lookup"><span data-stu-id="2ac72-128">Vertex</span></span> | <span data-ttu-id="2ac72-129">船體</span><span class="sxs-lookup"><span data-stu-id="2ac72-129">Hull</span></span> | <span data-ttu-id="2ac72-130">網域</span><span class="sxs-lookup"><span data-stu-id="2ac72-130">Domain</span></span> | <span data-ttu-id="2ac72-131">幾何</span><span class="sxs-lookup"><span data-stu-id="2ac72-131">Geometry</span></span> | <span data-ttu-id="2ac72-132">像素</span><span class="sxs-lookup"><span data-stu-id="2ac72-132">Pixel</span></span> | <span data-ttu-id="2ac72-133">計算</span><span class="sxs-lookup"><span data-stu-id="2ac72-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2ac72-134">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-134">X</span></span>      | <span data-ttu-id="2ac72-135">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-135">X</span></span>    | <span data-ttu-id="2ac72-136">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-136">X</span></span>      | <span data-ttu-id="2ac72-137">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-137">X</span></span>        | <span data-ttu-id="2ac72-138">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-138">X</span></span>     | <span data-ttu-id="2ac72-139">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-139">X</span></span>       |



 

<span data-ttu-id="2ac72-140">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此，此指示適用于適用于 Direct3D 11.1 執行時間的所有 UAVs 著色器階段（從 Windows 8 開始提供）。</span><span class="sxs-lookup"><span data-stu-id="2ac72-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2ac72-141">頂點</span><span class="sxs-lookup"><span data-stu-id="2ac72-141">Vertex</span></span> | <span data-ttu-id="2ac72-142">船體</span><span class="sxs-lookup"><span data-stu-id="2ac72-142">Hull</span></span> | <span data-ttu-id="2ac72-143">網域</span><span class="sxs-lookup"><span data-stu-id="2ac72-143">Domain</span></span> | <span data-ttu-id="2ac72-144">幾何</span><span class="sxs-lookup"><span data-stu-id="2ac72-144">Geometry</span></span> | <span data-ttu-id="2ac72-145">像素</span><span class="sxs-lookup"><span data-stu-id="2ac72-145">Pixel</span></span> | <span data-ttu-id="2ac72-146">計算</span><span class="sxs-lookup"><span data-stu-id="2ac72-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2ac72-147">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-147">X</span></span>      | <span data-ttu-id="2ac72-148">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-148">X</span></span>    | <span data-ttu-id="2ac72-149">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-149">X</span></span>      | <span data-ttu-id="2ac72-150">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-150">X</span></span>        | <span data-ttu-id="2ac72-151">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-151">X</span></span>     | <span data-ttu-id="2ac72-152">X</span><span class="sxs-lookup"><span data-stu-id="2ac72-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2ac72-153">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2ac72-153">Minimum Shader Model</span></span>

<span data-ttu-id="2ac72-154">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="2ac72-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2ac72-155">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2ac72-155">Shader Model</span></span>                                              | <span data-ttu-id="2ac72-156">支援</span><span class="sxs-lookup"><span data-stu-id="2ac72-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2ac72-157">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2ac72-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2ac72-158">是</span><span class="sxs-lookup"><span data-stu-id="2ac72-158">yes</span></span>       |
| [<span data-ttu-id="2ac72-159">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="2ac72-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2ac72-160">不可以</span><span class="sxs-lookup"><span data-stu-id="2ac72-160">no</span></span>        |
| [<span data-ttu-id="2ac72-161">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="2ac72-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2ac72-162">不可以</span><span class="sxs-lookup"><span data-stu-id="2ac72-162">no</span></span>        |
| [<span data-ttu-id="2ac72-163">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2ac72-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2ac72-164">不可以</span><span class="sxs-lookup"><span data-stu-id="2ac72-164">no</span></span>        |
| [<span data-ttu-id="2ac72-165">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2ac72-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2ac72-166">不可以</span><span class="sxs-lookup"><span data-stu-id="2ac72-166">no</span></span>        |
| [<span data-ttu-id="2ac72-167">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2ac72-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2ac72-168">不可以</span><span class="sxs-lookup"><span data-stu-id="2ac72-168">no</span></span>        |



 

<span data-ttu-id="2ac72-169">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV、SRV 和 TGSM 的指令。</span><span class="sxs-lookup"><span data-stu-id="2ac72-169">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ac72-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ac72-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ac72-171">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2ac72-171">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





