---
title: 'round_ne (sm4-asm) '
description: '浮點數舍入整數浮點數。 |round_ne (sm4-asm) '
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0efb2ff10b75e50ec05847dd25aa8448c760c7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993925"
---
# <a name="round_ne-sm4---asm"></a><span data-ttu-id="5ce18-104">四捨五入 \_ (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="5ce18-104">round\_ne (sm4 - asm)</span></span>

<span data-ttu-id="5ce18-105">浮點數舍入整數浮點數。</span><span class="sxs-lookup"><span data-stu-id="5ce18-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="5ce18-106">round \_ ne \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5ce18-106">round\_ne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="5ce18-107">項目</span><span class="sxs-lookup"><span data-stu-id="5ce18-107">Item</span></span>                                                            | <span data-ttu-id="5ce18-108">描述</span><span class="sxs-lookup"><span data-stu-id="5ce18-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5ce18-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="5ce18-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5ce18-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="5ce18-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5ce18-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5ce18-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5ce18-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="5ce18-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5ce18-113">備註</span><span class="sxs-lookup"><span data-stu-id="5ce18-113">Remarks</span></span>

<span data-ttu-id="5ce18-114">此指令會在 *src0* 中執行以元件為依據的浮點舍入值，並將整數浮點值寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="5ce18-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="5ce18-115">**四捨五入 \_** 會四捨五入到最接近的偶數。</span><span class="sxs-lookup"><span data-stu-id="5ce18-115">**round\_ne** rounds towards nearest even.</span></span>

<span data-ttu-id="5ce18-116">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="5ce18-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="5ce18-117">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="5ce18-117">F means finite-real number.</span></span>



| <span data-ttu-id="5ce18-118">**src**</span><span class="sxs-lookup"><span data-stu-id="5ce18-118">**src**</span></span>  | <span data-ttu-id="5ce18-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="5ce18-119">**-inf**</span></span> | <span data-ttu-id="5ce18-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="5ce18-120">**-F**</span></span> | <span data-ttu-id="5ce18-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="5ce18-121">**-denorm**</span></span> | <span data-ttu-id="5ce18-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="5ce18-122">**-0**</span></span> | <span data-ttu-id="5ce18-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="5ce18-123">**+0**</span></span> | <span data-ttu-id="5ce18-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="5ce18-124">**+denorm**</span></span> | <span data-ttu-id="5ce18-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="5ce18-125">**+F**</span></span> | <span data-ttu-id="5ce18-126">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="5ce18-126">**+inf**</span></span> | <span data-ttu-id="5ce18-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5ce18-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="5ce18-128">**目標**</span><span class="sxs-lookup"><span data-stu-id="5ce18-128">**dest**</span></span> | <span data-ttu-id="5ce18-129">-inf</span><span class="sxs-lookup"><span data-stu-id="5ce18-129">-inf</span></span>     | <span data-ttu-id="5ce18-130">-F</span><span class="sxs-lookup"><span data-stu-id="5ce18-130">-F</span></span>     | <span data-ttu-id="5ce18-131">-0</span><span class="sxs-lookup"><span data-stu-id="5ce18-131">-0</span></span>          | <span data-ttu-id="5ce18-132">-0</span><span class="sxs-lookup"><span data-stu-id="5ce18-132">-0</span></span>     | <span data-ttu-id="5ce18-133">+0</span><span class="sxs-lookup"><span data-stu-id="5ce18-133">+0</span></span>     | <span data-ttu-id="5ce18-134">+0</span><span class="sxs-lookup"><span data-stu-id="5ce18-134">+0</span></span>          | <span data-ttu-id="5ce18-135">+F</span><span class="sxs-lookup"><span data-stu-id="5ce18-135">+F</span></span>     | <span data-ttu-id="5ce18-136">+inf</span><span class="sxs-lookup"><span data-stu-id="5ce18-136">+inf</span></span>     | <span data-ttu-id="5ce18-137">NaN</span><span class="sxs-lookup"><span data-stu-id="5ce18-137">NaN</span></span>     |



 

<span data-ttu-id="5ce18-138">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="5ce18-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5ce18-139">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="5ce18-139">Vertex Shader</span></span> | <span data-ttu-id="5ce18-140">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="5ce18-140">Geometry Shader</span></span> | <span data-ttu-id="5ce18-141">像素著色器</span><span class="sxs-lookup"><span data-stu-id="5ce18-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5ce18-142">x</span><span class="sxs-lookup"><span data-stu-id="5ce18-142">x</span></span>             | <span data-ttu-id="5ce18-143">x</span><span class="sxs-lookup"><span data-stu-id="5ce18-143">x</span></span>               | <span data-ttu-id="5ce18-144">x</span><span class="sxs-lookup"><span data-stu-id="5ce18-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ce18-145">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5ce18-145">Minimum Shader Model</span></span>

<span data-ttu-id="5ce18-146">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="5ce18-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5ce18-147">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5ce18-147">Shader Model</span></span>                                              | <span data-ttu-id="5ce18-148">支援</span><span class="sxs-lookup"><span data-stu-id="5ce18-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5ce18-149">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5ce18-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5ce18-150">是</span><span class="sxs-lookup"><span data-stu-id="5ce18-150">yes</span></span>       |
| [<span data-ttu-id="5ce18-151">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="5ce18-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5ce18-152">是</span><span class="sxs-lookup"><span data-stu-id="5ce18-152">yes</span></span>       |
| [<span data-ttu-id="5ce18-153">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5ce18-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5ce18-154">是</span><span class="sxs-lookup"><span data-stu-id="5ce18-154">yes</span></span>       |
| [<span data-ttu-id="5ce18-155">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ce18-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5ce18-156">否</span><span class="sxs-lookup"><span data-stu-id="5ce18-156">no</span></span>        |
| [<span data-ttu-id="5ce18-157">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ce18-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5ce18-158">否</span><span class="sxs-lookup"><span data-stu-id="5ce18-158">no</span></span>        |
| [<span data-ttu-id="5ce18-159">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ce18-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5ce18-160">否</span><span class="sxs-lookup"><span data-stu-id="5ce18-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5ce18-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ce18-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce18-162">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5ce18-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





