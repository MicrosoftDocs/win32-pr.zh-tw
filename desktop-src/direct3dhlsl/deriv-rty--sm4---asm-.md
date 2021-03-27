---
title: 'deriv_rty (sm4-asm) '
description: 轉譯-目標 y 相當於 deriv \_ rtx。
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841636"
---
# <a name="deriv_rty-sm4---asm"></a><span data-ttu-id="4b37b-103">deriv \_ rty (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="4b37b-103">deriv\_rty (sm4 - asm)</span></span>

<span data-ttu-id="4b37b-104">轉譯-目標 y 相當於 [deriv \_ rtx](deriv-rtx--sm4---asm-.md)。</span><span class="sxs-lookup"><span data-stu-id="4b37b-104">Render-target y equivalent of [deriv\_rtx](deriv-rtx--sm4---asm-.md).</span></span>



| <span data-ttu-id="4b37b-105">deriv \_ rty \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ，</span><span class="sxs-lookup"><span data-stu-id="4b37b-105">deriv\_rty\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="4b37b-106">項目</span><span class="sxs-lookup"><span data-stu-id="4b37b-106">Item</span></span>                                                            | <span data-ttu-id="4b37b-107">描述</span><span class="sxs-lookup"><span data-stu-id="4b37b-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4b37b-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="4b37b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4b37b-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="4b37b-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="4b37b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4b37b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4b37b-111">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="4b37b-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4b37b-112">備註</span><span class="sxs-lookup"><span data-stu-id="4b37b-112">Remarks</span></span>

<span data-ttu-id="4b37b-113">每個2x2 的圖元戳記都只會計算單一 x、y 衍生配對。</span><span class="sxs-lookup"><span data-stu-id="4b37b-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="4b37b-114">這項操作與硬體相依。</span><span class="sxs-lookup"><span data-stu-id="4b37b-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="4b37b-115">三角形的參考轉譯器執行：</span><span class="sxs-lookup"><span data-stu-id="4b37b-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="4b37b-116">圖元著色器一律會透過密集建置 (中的2x2 四個圖元來執行著色器，即使是透過流量控制、遮罩停用的圖元) 。</span><span class="sxs-lookup"><span data-stu-id="4b37b-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="4b37b-117">四邊形永遠有偶數的圖元座標， (左上圖元的 x 和 y) 。</span><span class="sxs-lookup"><span data-stu-id="4b37b-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="4b37b-118">如果基本類型太小，無法填滿2x2 的四個，則虛擬圖元會關閉基本型別。</span><span class="sxs-lookup"><span data-stu-id="4b37b-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="4b37b-119">[deriv \_ rtx](deriv-rtx--sm4---asm-.md) 的計算方式是先選擇2圖元：目前的圖元，以及與四的 y 座標相同的另一個圖元。</span><span class="sxs-lookup"><span data-stu-id="4b37b-119">[deriv\_rtx](deriv-rtx--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="4b37b-120">然後，結果會計算為： *src0* (奇數 x 圖元) - *src0* (偶數 x 圖元) \[ 每個元件\]</span><span class="sxs-lookup"><span data-stu-id="4b37b-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="4b37b-121">**deriv \_ rty** 的計算方式是先選擇2個圖元：目前的圖元，以及與四個相同 x 座標的另一個圖元。</span><span class="sxs-lookup"><span data-stu-id="4b37b-121">**deriv\_rty** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="4b37b-122">然後，結果會計算為： *src0* (奇數 y 圖元) - *src0* (偶數 y 圖元) \[ 每個元件\]</span><span class="sxs-lookup"><span data-stu-id="4b37b-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="4b37b-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4b37b-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4b37b-124">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="4b37b-124">Vertex Shader</span></span> | <span data-ttu-id="4b37b-125">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="4b37b-125">Geometry Shader</span></span> | <span data-ttu-id="4b37b-126">像素著色器</span><span class="sxs-lookup"><span data-stu-id="4b37b-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="4b37b-127">x</span><span class="sxs-lookup"><span data-stu-id="4b37b-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4b37b-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4b37b-128">Minimum Shader Model</span></span>

<span data-ttu-id="4b37b-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="4b37b-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4b37b-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4b37b-130">Shader Model</span></span>                                              | <span data-ttu-id="4b37b-131">支援</span><span class="sxs-lookup"><span data-stu-id="4b37b-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4b37b-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4b37b-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4b37b-133">是</span><span class="sxs-lookup"><span data-stu-id="4b37b-133">yes</span></span>       |
| [<span data-ttu-id="4b37b-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4b37b-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4b37b-135">是</span><span class="sxs-lookup"><span data-stu-id="4b37b-135">yes</span></span>       |
| [<span data-ttu-id="4b37b-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4b37b-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4b37b-137">是</span><span class="sxs-lookup"><span data-stu-id="4b37b-137">yes</span></span>       |
| [<span data-ttu-id="4b37b-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b37b-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4b37b-139">不可以</span><span class="sxs-lookup"><span data-stu-id="4b37b-139">no</span></span>        |
| [<span data-ttu-id="4b37b-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b37b-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4b37b-141">不可以</span><span class="sxs-lookup"><span data-stu-id="4b37b-141">no</span></span>        |
| [<span data-ttu-id="4b37b-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b37b-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4b37b-143">不可以</span><span class="sxs-lookup"><span data-stu-id="4b37b-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4b37b-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b37b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b37b-145">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b37b-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





