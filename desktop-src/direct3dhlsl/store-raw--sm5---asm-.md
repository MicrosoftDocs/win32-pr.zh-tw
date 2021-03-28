---
title: 'store_raw (sm5-asm) '
description: 隨機存取將 1-4 32 位元件寫入至無型別的記憶體。
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373883"
---
# <a name="store_raw-sm5---asm"></a><span data-ttu-id="fe59a-103">儲存 \_ 原始 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="fe59a-103">store\_raw (sm5 - asm)</span></span>

<span data-ttu-id="fe59a-104">隨機存取將 1-4 32 位元件寫入至無型別的記憶體。</span><span class="sxs-lookup"><span data-stu-id="fe59a-104">Random-access write of 1-4 32bit components into typeless memory.</span></span>



| <span data-ttu-id="fe59a-105">store \_ raw dst0 \[ . write \_ mask \] ，dstByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="fe59a-105">store\_raw dst0\[.write\_mask\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="fe59a-106">項目</span><span class="sxs-lookup"><span data-stu-id="fe59a-106">Item</span></span>                                                                                                                       | <span data-ttu-id="fe59a-107">描述</span><span class="sxs-lookup"><span data-stu-id="fe59a-107">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="fe59a-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="fe59a-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="fe59a-109">\[在 \] 記憶體位址中。</span><span class="sxs-lookup"><span data-stu-id="fe59a-109">\[in\] The memory address.</span></span><br/>      |
| <span data-ttu-id="fe59a-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="fe59a-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="fe59a-111">\[在 \] 位移中。</span><span class="sxs-lookup"><span data-stu-id="fe59a-111">\[in\] The offset.</span></span><br/>              |
| <span data-ttu-id="fe59a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fe59a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="fe59a-113">\[在 \] 要寫入的元件中。</span><span class="sxs-lookup"><span data-stu-id="fe59a-113">\[in\] The components to write.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe59a-114">備註</span><span class="sxs-lookup"><span data-stu-id="fe59a-114">Remarks</span></span>

<span data-ttu-id="fe59a-115">此指令會 \* 在 *dstByteOffset* 中的位移執行從 *src0* 寫入至 *dst0* 的1-4 元件32位元件。</span><span class="sxs-lookup"><span data-stu-id="fe59a-115">This instruction performs 1-4 component \*32-bit components written from *src0* to *dst0* at the offset in *dstByteOffset*.</span></span> <span data-ttu-id="fe59a-116">沒有格式轉換。</span><span class="sxs-lookup"><span data-stu-id="fe59a-116">There is no format conversion.</span></span>

<span data-ttu-id="fe59a-117">*dst0* 必須是 UAV (u \#) ，或在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="fe59a-117">*dst0* must be a UAV (u\#), or in the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="fe59a-118">*dstByteOffset* 會根據其他參數上的 swizzle 和 mask，將記憶體中的基底32位值指定為4個連續32位值的視窗，其中可能會寫入資料。</span><span class="sxs-lookup"><span data-stu-id="fe59a-118">*dstByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be written, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="fe59a-119">寫入的資料位置相當於下列虛擬程式碼，它會顯示位址、緩衝區內容的指標，以及以線性方式儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="fe59a-119">The location of the data written is equivalent to the following pseudocode which show the address, pointer to the buffer contents, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

<span data-ttu-id="fe59a-120">這個虛擬虛擬的會顯示作業的運作方式，但實際的資料不需要以線性方式儲存。</span><span class="sxs-lookup"><span data-stu-id="fe59a-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="fe59a-121">*dst0* 只能有下列其中一項的寫入遮罩：. x、xy、.xyz、. xyzw。</span><span class="sxs-lookup"><span data-stu-id="fe59a-121">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="fe59a-122">寫入遮罩可決定要在沒有間距的情況下寫入的32位元件數目。</span><span class="sxs-lookup"><span data-stu-id="fe59a-122">The write mask determines the number of 32bit components to write without gaps.</span></span>

<span data-ttu-id="fe59a-123">U 的超出範圍定址 \# 表示不會將任何內容寫入超出範圍記憶體; 任何範圍內的部分都會正確寫入。</span><span class="sxs-lookup"><span data-stu-id="fe59a-123">Out of bounds addressing on u\# means nothing is written to the out of bounds memory; any part that is in bounds is written correctly.</span></span>

<span data-ttu-id="fe59a-124">G (界限的範圍外， \# 該特定 g 的界限 \# ，而不是任何指定32位元件的所有共用記憶體) ，會導致所有共用記憶體的整個內容變成未定義。</span><span class="sxs-lookup"><span data-stu-id="fe59a-124">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="fe59a-125">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援這個 UAV 指令。</span><span class="sxs-lookup"><span data-stu-id="fe59a-125">cs\_4\_0 and cs\_4\_1 support this instruction for UAV.</span></span>

<span data-ttu-id="fe59a-126">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="fe59a-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fe59a-127">頂點</span><span class="sxs-lookup"><span data-stu-id="fe59a-127">Vertex</span></span> | <span data-ttu-id="fe59a-128">船體</span><span class="sxs-lookup"><span data-stu-id="fe59a-128">Hull</span></span> | <span data-ttu-id="fe59a-129">網域</span><span class="sxs-lookup"><span data-stu-id="fe59a-129">Domain</span></span> | <span data-ttu-id="fe59a-130">幾何</span><span class="sxs-lookup"><span data-stu-id="fe59a-130">Geometry</span></span> | <span data-ttu-id="fe59a-131">像素</span><span class="sxs-lookup"><span data-stu-id="fe59a-131">Pixel</span></span> | <span data-ttu-id="fe59a-132">計算</span><span class="sxs-lookup"><span data-stu-id="fe59a-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fe59a-133">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-133">X</span></span>     | <span data-ttu-id="fe59a-134">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-134">X</span></span>       |



 

<span data-ttu-id="fe59a-135">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="fe59a-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="fe59a-136">頂點</span><span class="sxs-lookup"><span data-stu-id="fe59a-136">Vertex</span></span> | <span data-ttu-id="fe59a-137">船體</span><span class="sxs-lookup"><span data-stu-id="fe59a-137">Hull</span></span> | <span data-ttu-id="fe59a-138">網域</span><span class="sxs-lookup"><span data-stu-id="fe59a-138">Domain</span></span> | <span data-ttu-id="fe59a-139">幾何</span><span class="sxs-lookup"><span data-stu-id="fe59a-139">Geometry</span></span> | <span data-ttu-id="fe59a-140">像素</span><span class="sxs-lookup"><span data-stu-id="fe59a-140">Pixel</span></span> | <span data-ttu-id="fe59a-141">計算</span><span class="sxs-lookup"><span data-stu-id="fe59a-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fe59a-142">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-142">X</span></span>      | <span data-ttu-id="fe59a-143">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-143">X</span></span>    | <span data-ttu-id="fe59a-144">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-144">X</span></span>      | <span data-ttu-id="fe59a-145">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-145">X</span></span>        | <span data-ttu-id="fe59a-146">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-146">X</span></span>     | <span data-ttu-id="fe59a-147">X</span><span class="sxs-lookup"><span data-stu-id="fe59a-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fe59a-148">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="fe59a-148">Minimum Shader Model</span></span>

<span data-ttu-id="fe59a-149">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="fe59a-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fe59a-150">著色器模型</span><span class="sxs-lookup"><span data-stu-id="fe59a-150">Shader Model</span></span>                                              | <span data-ttu-id="fe59a-151">支援</span><span class="sxs-lookup"><span data-stu-id="fe59a-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fe59a-152">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fe59a-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fe59a-153">是</span><span class="sxs-lookup"><span data-stu-id="fe59a-153">yes</span></span>       |
| [<span data-ttu-id="fe59a-154">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="fe59a-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fe59a-155">不可以</span><span class="sxs-lookup"><span data-stu-id="fe59a-155">no</span></span>        |
| [<span data-ttu-id="fe59a-156">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="fe59a-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fe59a-157">不可以</span><span class="sxs-lookup"><span data-stu-id="fe59a-157">no</span></span>        |
| [<span data-ttu-id="fe59a-158">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fe59a-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fe59a-159">不可以</span><span class="sxs-lookup"><span data-stu-id="fe59a-159">no</span></span>        |
| [<span data-ttu-id="fe59a-160">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fe59a-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fe59a-161">不可以</span><span class="sxs-lookup"><span data-stu-id="fe59a-161">no</span></span>        |
| [<span data-ttu-id="fe59a-162">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fe59a-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fe59a-163">不可以</span><span class="sxs-lookup"><span data-stu-id="fe59a-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fe59a-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe59a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe59a-165">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fe59a-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





