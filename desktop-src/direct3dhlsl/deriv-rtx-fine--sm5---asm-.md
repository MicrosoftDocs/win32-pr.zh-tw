---
title: 'deriv_rtx_fine (sm5-asm) '
description: '計算元件變更的速率。 |deriv_rtx_fine (sm5-asm) '
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992027"
---
# <a name="deriv_rtx_fine-sm5---asm"></a><span data-ttu-id="c8601-104">deriv \_ rtx \_ 良好 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="c8601-104">deriv\_rtx\_fine (sm5 - asm)</span></span>

<span data-ttu-id="c8601-105">計算元件變更的速率。</span><span class="sxs-lookup"><span data-stu-id="c8601-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="c8601-106">deriv \_ rtx \_ 精細的 \[ \_ sat： \] \[ mask \] 、 \[ - \] src0 \[ \_ abs \] \[ swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="c8601-106">deriv\_rtx\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="c8601-107">項目</span><span class="sxs-lookup"><span data-stu-id="c8601-107">Item</span></span>                                                            | <span data-ttu-id="c8601-108">描述</span><span class="sxs-lookup"><span data-stu-id="c8601-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c8601-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="c8601-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c8601-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="c8601-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="c8601-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c8601-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c8601-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="c8601-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c8601-113">備註</span><span class="sxs-lookup"><span data-stu-id="c8601-113">Remarks</span></span>

<span data-ttu-id="c8601-114">此指令會計算 *src0* 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向 (請參閱 [deriv \_ rty \_ 精細](deriv-rty-fine--sm5---asm-.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c8601-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md)).</span></span> <span data-ttu-id="c8601-115">2x2 戳記中的每個圖元都會取得一組獨特的 x/y 衍生計算</span><span class="sxs-lookup"><span data-stu-id="c8601-115">Each pixel in the 2x2 stamp gets a unique pair of x/y derivative calculations</span></span>

<span data-ttu-id="c8601-116">目前圖元著色器調用中的資料一律會參與所要求之衍生的計算。</span><span class="sxs-lookup"><span data-stu-id="c8601-116">The data in the current pixel shader invocation always participates in the calculation of the requested derivative.</span></span> <span data-ttu-id="c8601-117">在2x2 圖元中，目前的圖元落在四個圖元的範圍內，x 衍生是2圖元的資料列差異，包括目前的圖元。</span><span class="sxs-lookup"><span data-stu-id="c8601-117">In the 2x2 pixel quad the current pixel falls within, the x derivative is the delta of the row of 2 pixels including the current pixel.</span></span> <span data-ttu-id="c8601-118">Y 衍生資料行的差異是2圖元的資料行，包括目前的圖元。</span><span class="sxs-lookup"><span data-stu-id="c8601-118">The y derivative is the delta of the column of 2 pixels including the current pixel.</span></span> <span data-ttu-id="c8601-119">您不會在基本的情況上聽寫2x2 四邊形如何對齊或並排顯示。</span><span class="sxs-lookup"><span data-stu-id="c8601-119">There is no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="c8601-120">衍生的計算方式為精細層級 (2x2 四) 中每個圖元的 x/y 衍生配對的唯一計算。</span><span class="sxs-lookup"><span data-stu-id="c8601-120">Derivatives are calculated at a fine level (unique calculation of the x/y derivative pair for each pixel in a 2x2 quad).</span></span> <span data-ttu-id="c8601-121">這個指令和 [deriv \_ rty \_ ](deriv-rty-fine--sm5---asm-.md) 是 [deriv \_ rtx \_ 粗略](deriv-rtx-coarse--sm5---asm-.md) 和 [deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md)的替代方案。</span><span class="sxs-lookup"><span data-stu-id="c8601-121">This instruction and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md) are alternatives to [deriv\_rtx\_coarse](deriv-rtx-coarse--sm5---asm-.md) and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md).</span></span> <span data-ttu-id="c8601-122">這些 \_ 粗略和 \_ 精細的 **deriv \_ rtx** 取代了這些 \_ 粗略和 \_ 精細的說明，是從先前的著色器模型取代 **deriv \_ rtx** 和 **deriv \_ rty** 。</span><span class="sxs-lookup"><span data-stu-id="c8601-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** and **deriv\_rty** from previous shader models.</span></span>

<span data-ttu-id="c8601-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="c8601-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c8601-124">頂點</span><span class="sxs-lookup"><span data-stu-id="c8601-124">Vertex</span></span> | <span data-ttu-id="c8601-125">船體</span><span class="sxs-lookup"><span data-stu-id="c8601-125">Hull</span></span> | <span data-ttu-id="c8601-126">網域</span><span class="sxs-lookup"><span data-stu-id="c8601-126">Domain</span></span> | <span data-ttu-id="c8601-127">幾何</span><span class="sxs-lookup"><span data-stu-id="c8601-127">Geometry</span></span> | <span data-ttu-id="c8601-128">像素</span><span class="sxs-lookup"><span data-stu-id="c8601-128">Pixel</span></span> | <span data-ttu-id="c8601-129">計算</span><span class="sxs-lookup"><span data-stu-id="c8601-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c8601-130">X</span><span class="sxs-lookup"><span data-stu-id="c8601-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c8601-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c8601-131">Minimum Shader Model</span></span>

<span data-ttu-id="c8601-132">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="c8601-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c8601-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c8601-133">Shader Model</span></span>                                              | <span data-ttu-id="c8601-134">支援</span><span class="sxs-lookup"><span data-stu-id="c8601-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c8601-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c8601-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c8601-136">是</span><span class="sxs-lookup"><span data-stu-id="c8601-136">yes</span></span>       |
| [<span data-ttu-id="c8601-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="c8601-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c8601-138">不可以</span><span class="sxs-lookup"><span data-stu-id="c8601-138">no</span></span>        |
| [<span data-ttu-id="c8601-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="c8601-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c8601-140">不可以</span><span class="sxs-lookup"><span data-stu-id="c8601-140">no</span></span>        |
| [<span data-ttu-id="c8601-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c8601-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c8601-142">不可以</span><span class="sxs-lookup"><span data-stu-id="c8601-142">no</span></span>        |
| [<span data-ttu-id="c8601-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c8601-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c8601-144">不可以</span><span class="sxs-lookup"><span data-stu-id="c8601-144">no</span></span>        |
| [<span data-ttu-id="c8601-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c8601-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c8601-146">不可以</span><span class="sxs-lookup"><span data-stu-id="c8601-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c8601-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8601-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8601-148">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c8601-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





