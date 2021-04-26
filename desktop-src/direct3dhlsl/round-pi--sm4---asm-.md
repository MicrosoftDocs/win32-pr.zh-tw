---
title: 'round_pi (sm4-asm) '
description: '浮點數舍入整數浮點數。 |round_pi (sm4-asm) '
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997105"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="78bf4-104">round \_ pi (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="78bf4-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="78bf4-105">浮點數舍入整數浮點數。</span><span class="sxs-lookup"><span data-stu-id="78bf4-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="78bf4-106">四捨五入 \_ pi \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="78bf4-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="78bf4-107">項目</span><span class="sxs-lookup"><span data-stu-id="78bf4-107">Item</span></span>                                                            | <span data-ttu-id="78bf4-108">描述</span><span class="sxs-lookup"><span data-stu-id="78bf4-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="78bf4-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="78bf4-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="78bf4-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="78bf4-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="78bf4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="78bf4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="78bf4-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="78bf4-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="78bf4-113">備註</span><span class="sxs-lookup"><span data-stu-id="78bf4-113">Remarks</span></span>

<span data-ttu-id="78bf4-114">此指令會在 *src0* 中執行以元件為依據的浮點舍入值，並將整數浮點值寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="78bf4-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="78bf4-115">**舍入 \_ pi** 會四捨五入到 + 無限大，通常稱為 ceil () 。</span><span class="sxs-lookup"><span data-stu-id="78bf4-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="78bf4-116">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="78bf4-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="78bf4-117">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="78bf4-117">F means finite-real number.</span></span>



| <span data-ttu-id="78bf4-118">**src**</span><span class="sxs-lookup"><span data-stu-id="78bf4-118">**src**</span></span>  | <span data-ttu-id="78bf4-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="78bf4-119">**-inf**</span></span> | <span data-ttu-id="78bf4-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="78bf4-120">**-F**</span></span> | <span data-ttu-id="78bf4-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="78bf4-121">**-denorm**</span></span> | <span data-ttu-id="78bf4-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="78bf4-122">**-0**</span></span> | <span data-ttu-id="78bf4-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="78bf4-123">**+0**</span></span> | <span data-ttu-id="78bf4-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="78bf4-124">**+denorm**</span></span> | <span data-ttu-id="78bf4-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="78bf4-125">**+F**</span></span> | <span data-ttu-id="78bf4-126">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="78bf4-126">**+inf**</span></span> | <span data-ttu-id="78bf4-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="78bf4-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="78bf4-128">**目標**</span><span class="sxs-lookup"><span data-stu-id="78bf4-128">**dest**</span></span> | <span data-ttu-id="78bf4-129">-inf</span><span class="sxs-lookup"><span data-stu-id="78bf4-129">-inf</span></span>     | <span data-ttu-id="78bf4-130">-F</span><span class="sxs-lookup"><span data-stu-id="78bf4-130">-F</span></span>     | <span data-ttu-id="78bf4-131">-0</span><span class="sxs-lookup"><span data-stu-id="78bf4-131">-0</span></span>          | <span data-ttu-id="78bf4-132">-0</span><span class="sxs-lookup"><span data-stu-id="78bf4-132">-0</span></span>     | <span data-ttu-id="78bf4-133">+0</span><span class="sxs-lookup"><span data-stu-id="78bf4-133">+0</span></span>     | <span data-ttu-id="78bf4-134">+0</span><span class="sxs-lookup"><span data-stu-id="78bf4-134">+0</span></span>          | <span data-ttu-id="78bf4-135">+F</span><span class="sxs-lookup"><span data-stu-id="78bf4-135">+F</span></span>     | <span data-ttu-id="78bf4-136">+inf</span><span class="sxs-lookup"><span data-stu-id="78bf4-136">+inf</span></span>     | <span data-ttu-id="78bf4-137">NaN</span><span class="sxs-lookup"><span data-stu-id="78bf4-137">NaN</span></span>     |



 

<span data-ttu-id="78bf4-138">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="78bf4-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="78bf4-139">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="78bf4-139">Vertex Shader</span></span> | <span data-ttu-id="78bf4-140">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="78bf4-140">Geometry Shader</span></span> | <span data-ttu-id="78bf4-141">像素著色器</span><span class="sxs-lookup"><span data-stu-id="78bf4-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="78bf4-142">x</span><span class="sxs-lookup"><span data-stu-id="78bf4-142">x</span></span>             | <span data-ttu-id="78bf4-143">x</span><span class="sxs-lookup"><span data-stu-id="78bf4-143">x</span></span>               | <span data-ttu-id="78bf4-144">x</span><span class="sxs-lookup"><span data-stu-id="78bf4-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="78bf4-145">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="78bf4-145">Minimum Shader Model</span></span>

<span data-ttu-id="78bf4-146">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="78bf4-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="78bf4-147">著色器模型</span><span class="sxs-lookup"><span data-stu-id="78bf4-147">Shader Model</span></span>                                              | <span data-ttu-id="78bf4-148">支援</span><span class="sxs-lookup"><span data-stu-id="78bf4-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="78bf4-149">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="78bf4-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="78bf4-150">是</span><span class="sxs-lookup"><span data-stu-id="78bf4-150">yes</span></span>       |
| [<span data-ttu-id="78bf4-151">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="78bf4-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="78bf4-152">是</span><span class="sxs-lookup"><span data-stu-id="78bf4-152">yes</span></span>       |
| [<span data-ttu-id="78bf4-153">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="78bf4-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="78bf4-154">是</span><span class="sxs-lookup"><span data-stu-id="78bf4-154">yes</span></span>       |
| [<span data-ttu-id="78bf4-155">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78bf4-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="78bf4-156">否</span><span class="sxs-lookup"><span data-stu-id="78bf4-156">no</span></span>        |
| [<span data-ttu-id="78bf4-157">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78bf4-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="78bf4-158">否</span><span class="sxs-lookup"><span data-stu-id="78bf4-158">no</span></span>        |
| [<span data-ttu-id="78bf4-159">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78bf4-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="78bf4-160">否</span><span class="sxs-lookup"><span data-stu-id="78bf4-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="78bf4-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="78bf4-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78bf4-162">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78bf4-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





