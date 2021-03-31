---
title: 'deriv_rtx (sm4-asm) '
description: Src0 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向有關。
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373723"
---
# <a name="deriv_rtx-sm4---asm"></a><span data-ttu-id="68553-103">deriv \_ rtx (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="68553-103">deriv\_rtx (sm4 - asm)</span></span>

<span data-ttu-id="68553-104">*Src0* 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向有關。</span><span class="sxs-lookup"><span data-stu-id="68553-104">Rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction.</span></span>



| <span data-ttu-id="68553-105">deriv \_ rtx \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ，</span><span class="sxs-lookup"><span data-stu-id="68553-105">deriv\_rtx\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="68553-106">項目</span><span class="sxs-lookup"><span data-stu-id="68553-106">Item</span></span>                                                            | <span data-ttu-id="68553-107">描述</span><span class="sxs-lookup"><span data-stu-id="68553-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="68553-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="68553-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="68553-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="68553-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="68553-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="68553-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="68553-111">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="68553-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="68553-112">備註</span><span class="sxs-lookup"><span data-stu-id="68553-112">Remarks</span></span>

<span data-ttu-id="68553-113">每個2x2 的圖元戳記都只會計算單一 x、y 衍生配對。</span><span class="sxs-lookup"><span data-stu-id="68553-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="68553-114">這項操作與硬體相依。</span><span class="sxs-lookup"><span data-stu-id="68553-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="68553-115">三角形的參考轉譯器執行：</span><span class="sxs-lookup"><span data-stu-id="68553-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="68553-116">圖元著色器一律會透過密集建置 (中的2x2 四個圖元來執行著色器，即使是透過流量控制、遮罩停用的圖元) 。</span><span class="sxs-lookup"><span data-stu-id="68553-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="68553-117">四邊形永遠有偶數的圖元座標， (左上圖元的 x 和 y) 。</span><span class="sxs-lookup"><span data-stu-id="68553-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="68553-118">如果基本類型太小，無法填滿2x2 的四個，則虛擬圖元會關閉基本型別。</span><span class="sxs-lookup"><span data-stu-id="68553-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="68553-119">**deriv \_ rtx** 的計算方式是先選擇2圖元：目前的圖元，以及與四的 y 座標相同的另一個圖元。</span><span class="sxs-lookup"><span data-stu-id="68553-119">**deriv\_rtx** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="68553-120">然後，結果會計算為： *src0* (奇數 x 圖元) - *src0* (偶數 x 圖元) \[ 每個元件\]</span><span class="sxs-lookup"><span data-stu-id="68553-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="68553-121">[deriv \_ rty](deriv-rty--sm4---asm-.md) 的計算方式是先選擇2個圖元：目前的圖元，以及與四個相同 x 座標的另一個圖元。</span><span class="sxs-lookup"><span data-stu-id="68553-121">[deriv\_rty](deriv-rty--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="68553-122">然後，結果會計算為： *src0* (奇數 y 圖元) - *src0* (偶數 y 圖元) \[ 每個元件\]</span><span class="sxs-lookup"><span data-stu-id="68553-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="68553-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="68553-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="68553-124">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="68553-124">Vertex Shader</span></span> | <span data-ttu-id="68553-125">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="68553-125">Geometry Shader</span></span> | <span data-ttu-id="68553-126">像素著色器</span><span class="sxs-lookup"><span data-stu-id="68553-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="68553-127">x</span><span class="sxs-lookup"><span data-stu-id="68553-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="68553-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="68553-128">Minimum Shader Model</span></span>

<span data-ttu-id="68553-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="68553-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="68553-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="68553-130">Shader Model</span></span>                                              | <span data-ttu-id="68553-131">支援</span><span class="sxs-lookup"><span data-stu-id="68553-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="68553-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="68553-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="68553-133">是</span><span class="sxs-lookup"><span data-stu-id="68553-133">yes</span></span>       |
| [<span data-ttu-id="68553-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="68553-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="68553-135">是</span><span class="sxs-lookup"><span data-stu-id="68553-135">yes</span></span>       |
| [<span data-ttu-id="68553-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="68553-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="68553-137">是</span><span class="sxs-lookup"><span data-stu-id="68553-137">yes</span></span>       |
| [<span data-ttu-id="68553-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="68553-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="68553-139">不可以</span><span class="sxs-lookup"><span data-stu-id="68553-139">no</span></span>        |
| [<span data-ttu-id="68553-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="68553-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="68553-141">不可以</span><span class="sxs-lookup"><span data-stu-id="68553-141">no</span></span>        |
| [<span data-ttu-id="68553-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="68553-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="68553-143">不可以</span><span class="sxs-lookup"><span data-stu-id="68553-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="68553-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="68553-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68553-145">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="68553-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





