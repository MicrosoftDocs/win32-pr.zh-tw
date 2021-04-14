---
title: 'sincos (sm4-asm) '
description: 元件取向的 sin (theta) 和 cos (弧度的 theta) 。
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990719"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="7d0c0-103">sincos (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="7d0c0-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="7d0c0-104">元件取向的 sin (theta) 和 cos (弧度的 theta) 。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="7d0c0-105">sincos \[ \_ sat \] destSIN \[ mask \] 、destCOS \[ mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7d0c0-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7d0c0-106">項目</span><span class="sxs-lookup"><span data-stu-id="7d0c0-106">Item</span></span>                                                                                               | <span data-ttu-id="7d0c0-107">描述</span><span class="sxs-lookup"><span data-stu-id="7d0c0-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="7d0c0-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="7d0c0-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="7d0c0-109">\[在 \] sin (*src0*) 的位址中，每個元件都會計算。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="7d0c0-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="7d0c0-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="7d0c0-111">\[在 \] cos (*src0*) 的位址中，每個元件都會計算。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="7d0c0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7d0c0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="7d0c0-113">\[在 \] 要計算 sin 和 cos 的元件中。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="7d0c0-114">備註</span><span class="sxs-lookup"><span data-stu-id="7d0c0-114">Remarks</span></span>

<span data-ttu-id="7d0c0-115">如果不需要結果，您可以將 *destSIN* 和 *DESTCOS* 指定為 Null，而不是指定註冊。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="7d0c0-116">Theta 值可以是任何 IEEE 32 位浮點值。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="7d0c0-117">從-100 \* pi 到 + 100 Pi 的間隔中，最大的絕對錯誤為 0.0008 \* 。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="7d0c0-118">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="7d0c0-119">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-119">F means finite-real number.</span></span>



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="7d0c0-120">**src**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-120">**src**</span></span>     | <span data-ttu-id="7d0c0-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-121">**-inf**</span></span> | <span data-ttu-id="7d0c0-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-122">**-F**</span></span>       | <span data-ttu-id="7d0c0-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-123">**-denorm**</span></span> | <span data-ttu-id="7d0c0-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-124">**-0**</span></span> | <span data-ttu-id="7d0c0-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-125">**+0**</span></span> | <span data-ttu-id="7d0c0-126">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-126">**+denorm**</span></span> | <span data-ttu-id="7d0c0-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-127">**+F**</span></span>       | <span data-ttu-id="7d0c0-128">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-128">**+inf**</span></span> | <span data-ttu-id="7d0c0-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-129">**NaN**</span></span> |
| <span data-ttu-id="7d0c0-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-130">**destSIN**</span></span> | <span data-ttu-id="7d0c0-131">NaN</span><span class="sxs-lookup"><span data-stu-id="7d0c0-131">NaN</span></span>      | <span data-ttu-id="7d0c0-132">\[-1 到 + 1\]</span><span class="sxs-lookup"><span data-stu-id="7d0c0-132">\[-1 to +1\]</span></span> | <span data-ttu-id="7d0c0-133">-0</span><span class="sxs-lookup"><span data-stu-id="7d0c0-133">-0</span></span>          | <span data-ttu-id="7d0c0-134">-0</span><span class="sxs-lookup"><span data-stu-id="7d0c0-134">-0</span></span>     | <span data-ttu-id="7d0c0-135">+0</span><span class="sxs-lookup"><span data-stu-id="7d0c0-135">+0</span></span>     | <span data-ttu-id="7d0c0-136">+0</span><span class="sxs-lookup"><span data-stu-id="7d0c0-136">+0</span></span>          | <span data-ttu-id="7d0c0-137">\[-1 到 + 1\]</span><span class="sxs-lookup"><span data-stu-id="7d0c0-137">\[-1 to +1\]</span></span> | <span data-ttu-id="7d0c0-138">NaN</span><span class="sxs-lookup"><span data-stu-id="7d0c0-138">NaN</span></span>      | <span data-ttu-id="7d0c0-139">NaN</span><span class="sxs-lookup"><span data-stu-id="7d0c0-139">NaN</span></span>     |
| <span data-ttu-id="7d0c0-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="7d0c0-140">**destCOS**</span></span> | <span data-ttu-id="7d0c0-141">NaN</span><span class="sxs-lookup"><span data-stu-id="7d0c0-141">NaN</span></span>      | <span data-ttu-id="7d0c0-142">\[-1 到 + 1\]</span><span class="sxs-lookup"><span data-stu-id="7d0c0-142">\[-1 to +1\]</span></span> | <span data-ttu-id="7d0c0-143">+1</span><span class="sxs-lookup"><span data-stu-id="7d0c0-143">+1</span></span>          | <span data-ttu-id="7d0c0-144">+1</span><span class="sxs-lookup"><span data-stu-id="7d0c0-144">+1</span></span>     | <span data-ttu-id="7d0c0-145">+1</span><span class="sxs-lookup"><span data-stu-id="7d0c0-145">+1</span></span>     | <span data-ttu-id="7d0c0-146">+1</span><span class="sxs-lookup"><span data-stu-id="7d0c0-146">+1</span></span>          | <span data-ttu-id="7d0c0-147">\[-1 到 + 1\]</span><span class="sxs-lookup"><span data-stu-id="7d0c0-147">\[-1 to +1\]</span></span> | <span data-ttu-id="7d0c0-148">NaN</span><span class="sxs-lookup"><span data-stu-id="7d0c0-148">NaN</span></span>      | <span data-ttu-id="7d0c0-149">NaN</span><span class="sxs-lookup"><span data-stu-id="7d0c0-149">NaN</span></span>     |



 

<span data-ttu-id="7d0c0-150">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="7d0c0-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7d0c0-151">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="7d0c0-151">Vertex Shader</span></span> | <span data-ttu-id="7d0c0-152">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="7d0c0-152">Geometry Shader</span></span> | <span data-ttu-id="7d0c0-153">像素著色器</span><span class="sxs-lookup"><span data-stu-id="7d0c0-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7d0c0-154">x</span><span class="sxs-lookup"><span data-stu-id="7d0c0-154">x</span></span>             | <span data-ttu-id="7d0c0-155">x</span><span class="sxs-lookup"><span data-stu-id="7d0c0-155">x</span></span>               | <span data-ttu-id="7d0c0-156">x</span><span class="sxs-lookup"><span data-stu-id="7d0c0-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7d0c0-157">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="7d0c0-157">Minimum Shader Model</span></span>

<span data-ttu-id="7d0c0-158">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="7d0c0-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7d0c0-159">著色器模型</span><span class="sxs-lookup"><span data-stu-id="7d0c0-159">Shader Model</span></span>                                              | <span data-ttu-id="7d0c0-160">支援</span><span class="sxs-lookup"><span data-stu-id="7d0c0-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7d0c0-161">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="7d0c0-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7d0c0-162">是</span><span class="sxs-lookup"><span data-stu-id="7d0c0-162">yes</span></span>       |
| [<span data-ttu-id="7d0c0-163">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="7d0c0-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7d0c0-164">是</span><span class="sxs-lookup"><span data-stu-id="7d0c0-164">yes</span></span>       |
| [<span data-ttu-id="7d0c0-165">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="7d0c0-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7d0c0-166">是</span><span class="sxs-lookup"><span data-stu-id="7d0c0-166">yes</span></span>       |
| [<span data-ttu-id="7d0c0-167">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7d0c0-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7d0c0-168">不可以</span><span class="sxs-lookup"><span data-stu-id="7d0c0-168">no</span></span>        |
| [<span data-ttu-id="7d0c0-169">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7d0c0-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7d0c0-170">不可以</span><span class="sxs-lookup"><span data-stu-id="7d0c0-170">no</span></span>        |
| [<span data-ttu-id="7d0c0-171">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7d0c0-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7d0c0-172">不可以</span><span class="sxs-lookup"><span data-stu-id="7d0c0-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7d0c0-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d0c0-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d0c0-174">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7d0c0-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





