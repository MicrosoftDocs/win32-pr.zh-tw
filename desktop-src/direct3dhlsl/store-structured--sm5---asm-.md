---
title: 'store_structured (sm5-asm) '
description: 以隨機方式將 1-4 32 位元件寫入至結構化緩衝區未排序的存取視圖 (UAV) 。
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022812"
---
# <a name="store_structured-sm5---asm"></a><span data-ttu-id="d6cc3-103">儲存 \_ 結構化 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d6cc3-103">store\_structured (sm5 - asm)</span></span>

<span data-ttu-id="d6cc3-104">以隨機方式將 1-4 32 位元件寫入至結構化緩衝區未排序的存取視圖 (UAV) 。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-104">Random-access write of 1-4 32-bit components into a structured buffer unordered access view (UAV).</span></span>



| <span data-ttu-id="d6cc3-105">儲存 \_ 結構化 dst0 \[ 。寫入 \_ mask \] ，dstAddress \[ 。 select component， \_ \] dstByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d6cc3-105">store\_structured dst0\[.write\_mask\], dstAddress\[.select\_component\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d6cc3-106">項目</span><span class="sxs-lookup"><span data-stu-id="d6cc3-106">Item</span></span>                                                                                                                       | <span data-ttu-id="d6cc3-107">描述</span><span class="sxs-lookup"><span data-stu-id="d6cc3-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d6cc3-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="d6cc3-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="d6cc3-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d6cc3-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="d6cc3-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/>             | <span data-ttu-id="d6cc3-111">\[在 \] 要寫入的位址中。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-111">\[in\] The address at which to write.</span></span><br/>               |
| <span data-ttu-id="d6cc3-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="d6cc3-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="d6cc3-113">\[在 \] 要寫入之結構的索引中。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-113">\[in\] The index of the structure to write.</span></span><br/>         |
| <span data-ttu-id="d6cc3-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d6cc3-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="d6cc3-115">\[在 \] 要寫入的元件中。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-115">\[in\] The components to write.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d6cc3-116">備註</span><span class="sxs-lookup"><span data-stu-id="d6cc3-116">Remarks</span></span>

<span data-ttu-id="d6cc3-117">此指令會在 \* *DstAddress* 和 *dstByteOffset* 中的位址，執行從 *src0* 寫入至 *dst0* 的1-4 元件32位元件。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-117">This instruction performs 1-4 component \*32bit components written from *src0* to *dst0* at the address in *dstAddress* and *dstByteOffset*.</span></span> <span data-ttu-id="d6cc3-118">沒有格式轉換。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-118">No format conversion.</span></span>

<span data-ttu-id="d6cc3-119">*dst0* 必須是 UAV (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-119">*dst0* must be a UAV (u\#).</span></span> <span data-ttu-id="d6cc3-120">在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-120">In the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="d6cc3-121">*dstAddress* 指定要寫入的結構索引。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-121">*dstAddress* specifies the index of the structure to write.</span></span>

<span data-ttu-id="d6cc3-122">寫入的資料位置相當於下列虛擬程式碼，它會顯示位移、位址、緩衝區內容的指標、來源的 stride，以及以線性方式儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-122">The location of the data written is equivalent to the following pseudocode which shows the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

<span data-ttu-id="d6cc3-123">這個虛擬虛擬的會顯示作業的運作方式，但實際的資料不需要以線性方式儲存。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-123">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="d6cc3-124">如果資料不是以線性方式儲存，則實際的指令運算必須符合上述作業的行為。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-124">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="d6cc3-125">*dst0* 只能有下列其中一項的寫入遮罩：. x、xy、.xyz、. xyzw。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-125">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="d6cc3-126">寫入遮罩可決定要在沒有間距的情況下寫入的32位元件數目。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-126">The write mask determines the number of 32-bit components to write without gaps.</span></span>

<span data-ttu-id="d6cc3-127">依 DstAddress 的 u casued 超出範圍定址， \# 表示不會將任何內容寫入超出範圍的記憶體。 </span><span class="sxs-lookup"><span data-stu-id="d6cc3-127">Out of bounds addressing on u\# casued by *dstAddress* means nothing is written to the out of bounds memory.</span></span>

<span data-ttu-id="d6cc3-128">如果 *dstByteOffset*（包括 *dstWriteMask*）是導致超出範圍存取權的原因，則 \# UAV 的整個內容都會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-128">If the *dstByteOffset*, including *dstWriteMask*, is what causes out of bounds access to u\#, the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="d6cc3-129">G (界限的範圍外， \# 該特定 g 的界限 \# ，而不是任何指定32位元件的所有共用記憶體) ，會導致所有共用記憶體的整個內容變成未定義。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-129">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="d6cc3-130">*dstByteOffset* 是不同于 *dstAddress* 的引數，因為它通常是常值。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-130">*dstByteOffset* is a separate argument from *dstAddress* because it is commonly a literal.</span></span> <span data-ttu-id="d6cc3-131">尚未對結構化記憶體上的 atomics 執行此參數分離。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-131">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="d6cc3-132">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援 UAV 和 TGSM 的這個指令。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-132">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and TGSM.</span></span>

<span data-ttu-id="d6cc3-133">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d6cc3-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d6cc3-134">頂點</span><span class="sxs-lookup"><span data-stu-id="d6cc3-134">Vertex</span></span> | <span data-ttu-id="d6cc3-135">船體</span><span class="sxs-lookup"><span data-stu-id="d6cc3-135">Hull</span></span> | <span data-ttu-id="d6cc3-136">網域</span><span class="sxs-lookup"><span data-stu-id="d6cc3-136">Domain</span></span> | <span data-ttu-id="d6cc3-137">幾何</span><span class="sxs-lookup"><span data-stu-id="d6cc3-137">Geometry</span></span> | <span data-ttu-id="d6cc3-138">像素</span><span class="sxs-lookup"><span data-stu-id="d6cc3-138">Pixel</span></span> | <span data-ttu-id="d6cc3-139">計算</span><span class="sxs-lookup"><span data-stu-id="d6cc3-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d6cc3-140">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-140">X</span></span>     | <span data-ttu-id="d6cc3-141">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-141">X</span></span>       |



 

<span data-ttu-id="d6cc3-142">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="d6cc3-142">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="d6cc3-143">頂點</span><span class="sxs-lookup"><span data-stu-id="d6cc3-143">Vertex</span></span> | <span data-ttu-id="d6cc3-144">船體</span><span class="sxs-lookup"><span data-stu-id="d6cc3-144">Hull</span></span> | <span data-ttu-id="d6cc3-145">網域</span><span class="sxs-lookup"><span data-stu-id="d6cc3-145">Domain</span></span> | <span data-ttu-id="d6cc3-146">幾何</span><span class="sxs-lookup"><span data-stu-id="d6cc3-146">Geometry</span></span> | <span data-ttu-id="d6cc3-147">像素</span><span class="sxs-lookup"><span data-stu-id="d6cc3-147">Pixel</span></span> | <span data-ttu-id="d6cc3-148">計算</span><span class="sxs-lookup"><span data-stu-id="d6cc3-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d6cc3-149">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-149">X</span></span>      | <span data-ttu-id="d6cc3-150">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-150">X</span></span>    | <span data-ttu-id="d6cc3-151">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-151">X</span></span>      | <span data-ttu-id="d6cc3-152">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-152">X</span></span>        | <span data-ttu-id="d6cc3-153">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-153">X</span></span>     | <span data-ttu-id="d6cc3-154">X</span><span class="sxs-lookup"><span data-stu-id="d6cc3-154">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d6cc3-155">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d6cc3-155">Minimum Shader Model</span></span>

<span data-ttu-id="d6cc3-156">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d6cc3-156">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d6cc3-157">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d6cc3-157">Shader Model</span></span>                                              | <span data-ttu-id="d6cc3-158">支援</span><span class="sxs-lookup"><span data-stu-id="d6cc3-158">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d6cc3-159">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d6cc3-159">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d6cc3-160">是</span><span class="sxs-lookup"><span data-stu-id="d6cc3-160">yes</span></span>       |
| [<span data-ttu-id="d6cc3-161">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d6cc3-161">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d6cc3-162">不可以</span><span class="sxs-lookup"><span data-stu-id="d6cc3-162">no</span></span>        |
| [<span data-ttu-id="d6cc3-163">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d6cc3-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d6cc3-164">不可以</span><span class="sxs-lookup"><span data-stu-id="d6cc3-164">no</span></span>        |
| [<span data-ttu-id="d6cc3-165">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6cc3-165">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d6cc3-166">不可以</span><span class="sxs-lookup"><span data-stu-id="d6cc3-166">no</span></span>        |
| [<span data-ttu-id="d6cc3-167">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6cc3-167">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d6cc3-168">不可以</span><span class="sxs-lookup"><span data-stu-id="d6cc3-168">no</span></span>        |
| [<span data-ttu-id="d6cc3-169">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6cc3-169">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d6cc3-170">不可以</span><span class="sxs-lookup"><span data-stu-id="d6cc3-170">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d6cc3-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6cc3-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6cc3-172">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6cc3-172">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





