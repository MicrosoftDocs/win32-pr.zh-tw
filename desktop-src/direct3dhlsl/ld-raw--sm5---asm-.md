---
title: 'ld_raw (sm5-asm) '
description: 從原始緩衝區隨機存取 1-4 32 位元件。
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971572"
---
# <a name="ld_raw-sm5---asm"></a><span data-ttu-id="e20e1-103">ld \_ raw (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="e20e1-103">ld\_raw (sm5 - asm)</span></span>

<span data-ttu-id="e20e1-104">從原始緩衝區隨機存取 1-4 32 位元件。</span><span class="sxs-lookup"><span data-stu-id="e20e1-104">Random-access read of 1-4 32bit components from a raw buffer.</span></span>



| <span data-ttu-id="e20e1-105">ld \_ raw dst0 \[ mask \] ，srcByteOffset \[ . select \_ component \] ，src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e20e1-105">ld\_raw dst0\[.mask\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="e20e1-106">項目</span><span class="sxs-lookup"><span data-stu-id="e20e1-106">Item</span></span>                                                                                                                       | <span data-ttu-id="e20e1-107">描述</span><span class="sxs-lookup"><span data-stu-id="e20e1-107">Description</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e20e1-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="e20e1-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="e20e1-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="e20e1-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e20e1-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="e20e1-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="e20e1-111">\[在中， \] 指定要讀取的位移。</span><span class="sxs-lookup"><span data-stu-id="e20e1-111">\[in\] Specifies the offset to read from.</span></span><br/>          |
| <span data-ttu-id="e20e1-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e20e1-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="e20e1-113">\[在 \] 要讀取的元件中。</span><span class="sxs-lookup"><span data-stu-id="e20e1-113">\[in\] The component to read.</span></span> <br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e20e1-114">備註</span><span class="sxs-lookup"><span data-stu-id="e20e1-114">Remarks</span></span>

<span data-ttu-id="e20e1-115">*src0* 必須是：</span><span class="sxs-lookup"><span data-stu-id="e20e1-115">*src0* must be:</span></span>

-   <span data-ttu-id="e20e1-116">任何著色器階段： SRV (t \#) ld st</span><span class="sxs-lookup"><span data-stu-id="e20e1-116">Any shader stage: SRV (t\#)ld st</span></span>
-   <span data-ttu-id="e20e1-117">計算著色器或圖元著色器： UAV (u \#) </span><span class="sxs-lookup"><span data-stu-id="e20e1-117">Compute shader or pixel shader: UAV (u\#)</span></span>
-   <span data-ttu-id="e20e1-118">計算著色器：執行緒群組共用記憶體 (g \#) </span><span class="sxs-lookup"><span data-stu-id="e20e1-118">Compute shader: thread group shared memory (g\#)</span></span>

<span data-ttu-id="e20e1-119">*srcByteOffset* 會將基底32位值指定在記憶體中，以供可讀取資料的4個連續32位值的視窗使用，視其他參數上的 swizzle 和遮罩而定。</span><span class="sxs-lookup"><span data-stu-id="e20e1-119">*srcByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be read, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="e20e1-120">從原始緩衝區讀取的資料相當於下列虛擬程式碼：其中有位移、位址、緩衝區內容的指標、來源的 stride，以及以線性方式儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="e20e1-120">The data read from the raw buffer is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="e20e1-121">\#任何指定32位元件之 u/t 上的界限定址 \# 都為該元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="e20e1-121">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component.</span></span>

<span data-ttu-id="e20e1-122">G (界限的範圍外， \# 該特定 g 的界限 \# ，而非任何指定32位元件的所有共用記憶體) 會傳回未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="e20e1-122">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="e20e1-123">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此 UAV 和 SRV 指令。</span><span class="sxs-lookup"><span data-stu-id="e20e1-123">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

<span data-ttu-id="e20e1-124">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="e20e1-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e20e1-125">頂點</span><span class="sxs-lookup"><span data-stu-id="e20e1-125">Vertex</span></span> | <span data-ttu-id="e20e1-126">船體</span><span class="sxs-lookup"><span data-stu-id="e20e1-126">Hull</span></span> | <span data-ttu-id="e20e1-127">網域</span><span class="sxs-lookup"><span data-stu-id="e20e1-127">Domain</span></span> | <span data-ttu-id="e20e1-128">幾何</span><span class="sxs-lookup"><span data-stu-id="e20e1-128">Geometry</span></span> | <span data-ttu-id="e20e1-129">像素</span><span class="sxs-lookup"><span data-stu-id="e20e1-129">Pixel</span></span> | <span data-ttu-id="e20e1-130">計算</span><span class="sxs-lookup"><span data-stu-id="e20e1-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e20e1-131">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-131">X</span></span>      | <span data-ttu-id="e20e1-132">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-132">X</span></span>    | <span data-ttu-id="e20e1-133">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-133">X</span></span>      | <span data-ttu-id="e20e1-134">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-134">X</span></span>        | <span data-ttu-id="e20e1-135">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-135">X</span></span>     | <span data-ttu-id="e20e1-136">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-136">X</span></span>       |



 

<span data-ttu-id="e20e1-137">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此，此指示適用于適用于 Direct3D 11.1 執行時間的所有 UAVs 著色器階段（從 Windows 8 開始提供）。</span><span class="sxs-lookup"><span data-stu-id="e20e1-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e20e1-138">頂點</span><span class="sxs-lookup"><span data-stu-id="e20e1-138">Vertex</span></span> | <span data-ttu-id="e20e1-139">船體</span><span class="sxs-lookup"><span data-stu-id="e20e1-139">Hull</span></span> | <span data-ttu-id="e20e1-140">網域</span><span class="sxs-lookup"><span data-stu-id="e20e1-140">Domain</span></span> | <span data-ttu-id="e20e1-141">幾何</span><span class="sxs-lookup"><span data-stu-id="e20e1-141">Geometry</span></span> | <span data-ttu-id="e20e1-142">像素</span><span class="sxs-lookup"><span data-stu-id="e20e1-142">Pixel</span></span> | <span data-ttu-id="e20e1-143">計算</span><span class="sxs-lookup"><span data-stu-id="e20e1-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e20e1-144">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-144">X</span></span>      | <span data-ttu-id="e20e1-145">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-145">X</span></span>    | <span data-ttu-id="e20e1-146">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-146">X</span></span>      | <span data-ttu-id="e20e1-147">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-147">X</span></span>        | <span data-ttu-id="e20e1-148">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-148">X</span></span>     | <span data-ttu-id="e20e1-149">X</span><span class="sxs-lookup"><span data-stu-id="e20e1-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e20e1-150">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e20e1-150">Minimum Shader Model</span></span>

<span data-ttu-id="e20e1-151">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="e20e1-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e20e1-152">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e20e1-152">Shader Model</span></span>                                              | <span data-ttu-id="e20e1-153">支援</span><span class="sxs-lookup"><span data-stu-id="e20e1-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e20e1-154">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e20e1-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e20e1-155">是</span><span class="sxs-lookup"><span data-stu-id="e20e1-155">yes</span></span>       |
| [<span data-ttu-id="e20e1-156">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="e20e1-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e20e1-157">不可以</span><span class="sxs-lookup"><span data-stu-id="e20e1-157">no</span></span>        |
| [<span data-ttu-id="e20e1-158">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e20e1-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e20e1-159">不可以</span><span class="sxs-lookup"><span data-stu-id="e20e1-159">no</span></span>        |
| [<span data-ttu-id="e20e1-160">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e20e1-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e20e1-161">不可以</span><span class="sxs-lookup"><span data-stu-id="e20e1-161">no</span></span>        |
| [<span data-ttu-id="e20e1-162">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e20e1-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e20e1-163">不可以</span><span class="sxs-lookup"><span data-stu-id="e20e1-163">no</span></span>        |
| [<span data-ttu-id="e20e1-164">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e20e1-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e20e1-165">不可以</span><span class="sxs-lookup"><span data-stu-id="e20e1-165">no</span></span>        |



 

<span data-ttu-id="e20e1-166">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此 UAV 和 SRV 指令。</span><span class="sxs-lookup"><span data-stu-id="e20e1-166">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e20e1-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="e20e1-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e20e1-168">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e20e1-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





