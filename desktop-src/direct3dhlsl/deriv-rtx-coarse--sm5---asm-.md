---
title: 'deriv_rtx_coarse (sm5-asm) '
description: '計算元件變更的速率。 |deriv_rtx_coarse (sm5-asm) '
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991922"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a><span data-ttu-id="20064-104">deriv \_ rtx \_ 粗略 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="20064-104">deriv\_rtx\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="20064-105">計算元件變更的速率。</span><span class="sxs-lookup"><span data-stu-id="20064-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="20064-106">deriv \_ rtx \_ 粗略 \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="20064-106">deriv\_rtx\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="20064-107">項目</span><span class="sxs-lookup"><span data-stu-id="20064-107">Item</span></span>                                                            | <span data-ttu-id="20064-108">描述</span><span class="sxs-lookup"><span data-stu-id="20064-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="20064-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="20064-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="20064-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="20064-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="20064-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="20064-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="20064-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="20064-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="20064-113">備註</span><span class="sxs-lookup"><span data-stu-id="20064-113">Remarks</span></span>

<span data-ttu-id="20064-114">此指令會計算 *src0* 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向 (請參閱 [deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md)) 。</span><span class="sxs-lookup"><span data-stu-id="20064-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)).</span></span> <span data-ttu-id="20064-115">每個2x2 的圖元戳記都只會計算單一 x、y 衍生配對。</span><span class="sxs-lookup"><span data-stu-id="20064-115">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="20064-116">目前圖元著色器調用中的資料不一定會參與要求之衍生的計算，因為每個2x2 四次的衍生只會計算一次。</span><span class="sxs-lookup"><span data-stu-id="20064-116">The data in the current pixel shader invocation may or may not participate in the calculation of the requested derivative, because the derivative will be calculated only once per 2x2 quad.</span></span> <span data-ttu-id="20064-117">例如，x 導數可能是最上層資料列的差異，而 y 方向 ([deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md)) 可能是來自圖元左邊資料行的差異。</span><span class="sxs-lookup"><span data-stu-id="20064-117">For example, the x derivative could be a delta from the top row of pixels, and the y direction ([deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)) could be a delta from the left column of pixels.</span></span> <span data-ttu-id="20064-118">確切的計算是由硬體廠商所組成。</span><span class="sxs-lookup"><span data-stu-id="20064-118">The exact calculation is up to the hardware vendor.</span></span> <span data-ttu-id="20064-119">此外，也不會有任何規格會聽寫2x2 四邊形如何對齊或在基本型別上並排顯示。</span><span class="sxs-lookup"><span data-stu-id="20064-119">There is also no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="20064-120">衍生會以粗略的層級計算，每個2x2 圖元四次。</span><span class="sxs-lookup"><span data-stu-id="20064-120">Derivatives are calculated at a coarse level, once per 2x2 pixel quad.</span></span> <span data-ttu-id="20064-121">這個指令和 [deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md) 是 [deriv \_ rtx \_ 精細](deriv-rtx-fine--sm5---asm-.md) 和 [deriv \_ rty \_ ](deriv-rty-fine--sm5---asm-.md)的替代方案。</span><span class="sxs-lookup"><span data-stu-id="20064-121">This instruction and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md) are alternatives to [deriv\_rtx\_fine](deriv-rtx-fine--sm5---asm-.md) and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md).</span></span> <span data-ttu-id="20064-122">這些 \_ 粗略和 \_ 精細的說明，是從先前的著色器模型中 **deriv \_ rtxderiv \_ rty** 的替代方案。</span><span class="sxs-lookup"><span data-stu-id="20064-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtxderiv\_rty** from previous shader models .</span></span>

<span data-ttu-id="20064-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="20064-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="20064-124">頂點</span><span class="sxs-lookup"><span data-stu-id="20064-124">Vertex</span></span> | <span data-ttu-id="20064-125">船體</span><span class="sxs-lookup"><span data-stu-id="20064-125">Hull</span></span> | <span data-ttu-id="20064-126">網域</span><span class="sxs-lookup"><span data-stu-id="20064-126">Domain</span></span> | <span data-ttu-id="20064-127">幾何</span><span class="sxs-lookup"><span data-stu-id="20064-127">Geometry</span></span> | <span data-ttu-id="20064-128">像素</span><span class="sxs-lookup"><span data-stu-id="20064-128">Pixel</span></span> | <span data-ttu-id="20064-129">計算</span><span class="sxs-lookup"><span data-stu-id="20064-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="20064-130">X</span><span class="sxs-lookup"><span data-stu-id="20064-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="20064-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="20064-131">Minimum Shader Model</span></span>

<span data-ttu-id="20064-132">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="20064-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="20064-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="20064-133">Shader Model</span></span>                                              | <span data-ttu-id="20064-134">支援</span><span class="sxs-lookup"><span data-stu-id="20064-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="20064-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="20064-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="20064-136">是</span><span class="sxs-lookup"><span data-stu-id="20064-136">yes</span></span>       |
| [<span data-ttu-id="20064-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="20064-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="20064-138">不可以</span><span class="sxs-lookup"><span data-stu-id="20064-138">no</span></span>        |
| [<span data-ttu-id="20064-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="20064-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="20064-140">不可以</span><span class="sxs-lookup"><span data-stu-id="20064-140">no</span></span>        |
| [<span data-ttu-id="20064-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="20064-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="20064-142">不可以</span><span class="sxs-lookup"><span data-stu-id="20064-142">no</span></span>        |
| [<span data-ttu-id="20064-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="20064-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="20064-144">不可以</span><span class="sxs-lookup"><span data-stu-id="20064-144">no</span></span>        |
| [<span data-ttu-id="20064-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="20064-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="20064-146">不可以</span><span class="sxs-lookup"><span data-stu-id="20064-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="20064-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="20064-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20064-148">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="20064-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





