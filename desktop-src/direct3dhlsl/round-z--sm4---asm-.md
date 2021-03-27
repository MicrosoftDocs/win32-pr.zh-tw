---
title: 'round_z (sm4-asm) '
description: '浮點數舍入整數浮點數。 |round_z (sm4-asm) '
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed79a60bf122163b49411a3b3197ccdacba1311
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853607"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="9771f-104">圓形 \_ z (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="9771f-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="9771f-105">浮點數舍入整數浮點數。</span><span class="sxs-lookup"><span data-stu-id="9771f-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="9771f-106">圓形 \_ z \[ \_ sat \] dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9771f-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="9771f-107">項目</span><span class="sxs-lookup"><span data-stu-id="9771f-107">Item</span></span>                                                            | <span data-ttu-id="9771f-108">描述</span><span class="sxs-lookup"><span data-stu-id="9771f-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9771f-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="9771f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9771f-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="9771f-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="9771f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9771f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9771f-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="9771f-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="9771f-113">備註</span><span class="sxs-lookup"><span data-stu-id="9771f-113">Remarks</span></span>

<span data-ttu-id="9771f-114">此指令會在 *src0* 中執行以元件為依據的浮點舍入值，並將整數浮點值寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="9771f-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="9771f-115">**圓形 \_ z** 四捨五入為零。</span><span class="sxs-lookup"><span data-stu-id="9771f-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="9771f-116">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="9771f-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="9771f-117">**src**</span><span class="sxs-lookup"><span data-stu-id="9771f-117">**src**</span></span>  | <span data-ttu-id="9771f-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="9771f-118">**-inf**</span></span> | <span data-ttu-id="9771f-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="9771f-119">**-F**</span></span> | <span data-ttu-id="9771f-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="9771f-120">**-denorm**</span></span> | <span data-ttu-id="9771f-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="9771f-121">**-0**</span></span> | <span data-ttu-id="9771f-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="9771f-122">**+0**</span></span> | <span data-ttu-id="9771f-123">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="9771f-123">**+denorm**</span></span> | <span data-ttu-id="9771f-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9771f-124">**+F**</span></span> | <span data-ttu-id="9771f-125">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="9771f-125">**+inf**</span></span> | <span data-ttu-id="9771f-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9771f-126">**NaN**</span></span> |
| <span data-ttu-id="9771f-127">**目標**</span><span class="sxs-lookup"><span data-stu-id="9771f-127">**dest**</span></span> | <span data-ttu-id="9771f-128">-inf</span><span class="sxs-lookup"><span data-stu-id="9771f-128">-inf</span></span>     | <span data-ttu-id="9771f-129">-F</span><span class="sxs-lookup"><span data-stu-id="9771f-129">-F</span></span>     | <span data-ttu-id="9771f-130">-0</span><span class="sxs-lookup"><span data-stu-id="9771f-130">-0</span></span>          | <span data-ttu-id="9771f-131">-0</span><span class="sxs-lookup"><span data-stu-id="9771f-131">-0</span></span>     | <span data-ttu-id="9771f-132">+0</span><span class="sxs-lookup"><span data-stu-id="9771f-132">+0</span></span>     | <span data-ttu-id="9771f-133">+0</span><span class="sxs-lookup"><span data-stu-id="9771f-133">+0</span></span>          | <span data-ttu-id="9771f-134">+F</span><span class="sxs-lookup"><span data-stu-id="9771f-134">+F</span></span>     | <span data-ttu-id="9771f-135">+inf</span><span class="sxs-lookup"><span data-stu-id="9771f-135">+inf</span></span>     | <span data-ttu-id="9771f-136">NaN</span><span class="sxs-lookup"><span data-stu-id="9771f-136">NaN</span></span>     |



 

<span data-ttu-id="9771f-137">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="9771f-137">F means finite-real number.</span></span>

<span data-ttu-id="9771f-138">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9771f-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9771f-139">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="9771f-139">Vertex Shader</span></span> | <span data-ttu-id="9771f-140">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="9771f-140">Geometry Shader</span></span> | <span data-ttu-id="9771f-141">像素著色器</span><span class="sxs-lookup"><span data-stu-id="9771f-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9771f-142">x</span><span class="sxs-lookup"><span data-stu-id="9771f-142">x</span></span>             | <span data-ttu-id="9771f-143">x</span><span class="sxs-lookup"><span data-stu-id="9771f-143">x</span></span>               | <span data-ttu-id="9771f-144">x</span><span class="sxs-lookup"><span data-stu-id="9771f-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9771f-145">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9771f-145">Minimum Shader Model</span></span>

<span data-ttu-id="9771f-146">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9771f-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9771f-147">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9771f-147">Shader Model</span></span>                                              | <span data-ttu-id="9771f-148">支援</span><span class="sxs-lookup"><span data-stu-id="9771f-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9771f-149">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9771f-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9771f-150">是</span><span class="sxs-lookup"><span data-stu-id="9771f-150">yes</span></span>       |
| [<span data-ttu-id="9771f-151">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9771f-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9771f-152">是</span><span class="sxs-lookup"><span data-stu-id="9771f-152">yes</span></span>       |
| [<span data-ttu-id="9771f-153">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9771f-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9771f-154">是</span><span class="sxs-lookup"><span data-stu-id="9771f-154">yes</span></span>       |
| [<span data-ttu-id="9771f-155">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9771f-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9771f-156">不可以</span><span class="sxs-lookup"><span data-stu-id="9771f-156">no</span></span>        |
| [<span data-ttu-id="9771f-157">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9771f-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9771f-158">不可以</span><span class="sxs-lookup"><span data-stu-id="9771f-158">no</span></span>        |
| [<span data-ttu-id="9771f-159">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9771f-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9771f-160">不可以</span><span class="sxs-lookup"><span data-stu-id="9771f-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9771f-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="9771f-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9771f-162">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9771f-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





