---
title: 'ne (sm4-asm) '
description: 元件的向量浮點數不相等比較。
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e53ff726047bd1870e6c836f4508bdf87001b3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373799"
---
# <a name="ne-sm4---asm"></a><span data-ttu-id="d2429-103">ne (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="d2429-103">ne (sm4 - asm)</span></span>

<span data-ttu-id="d2429-104">元件的向量浮點數不相等比較。</span><span class="sxs-lookup"><span data-stu-id="d2429-104">Component-wise vector floating point not-equal comparison.</span></span>



| <span data-ttu-id="d2429-105">ne dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d2429-105">ne dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="d2429-106">項目</span><span class="sxs-lookup"><span data-stu-id="d2429-106">Item</span></span>                                                            | <span data-ttu-id="d2429-107">描述</span><span class="sxs-lookup"><span data-stu-id="d2429-107">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2429-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="d2429-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d2429-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="d2429-109">\[in\] The result of the operation.</span></span><br/>         |
| <span data-ttu-id="d2429-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d2429-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d2429-111">\[在 \] [要與 *src1* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="d2429-111">\[in\] The components to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="d2429-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d2429-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d2429-113">\[在 \] [要與 *src0* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="d2429-113">\[in\] The components to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2429-114">備註</span><span class="sxs-lookup"><span data-stu-id="d2429-114">Remarks</span></span>

<span data-ttu-id="d2429-115">此指令會針對每個元件執行 float 比較 (*src0* ！ = *src1*) ，並將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="d2429-115">This instruction performs the float comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="d2429-116">如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="d2429-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="d2429-117">否則會傳回0x0000000。</span><span class="sxs-lookup"><span data-stu-id="d2429-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="d2429-118">Denorms 會在與原始來源登錄沒有改變之前排清。</span><span class="sxs-lookup"><span data-stu-id="d2429-118">Denorms are flushed before comparison with original source registers untouched.</span></span>

<span data-ttu-id="d2429-119">+ 0 等於-0。</span><span class="sxs-lookup"><span data-stu-id="d2429-119">+0 equals -0.</span></span>

<span data-ttu-id="d2429-120">與 NaN 的比較會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="d2429-120">Comparison with NaN returns true.</span></span>

<span data-ttu-id="d2429-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d2429-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d2429-122">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="d2429-122">Vertex Shader</span></span> | <span data-ttu-id="d2429-123">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="d2429-123">Geometry Shader</span></span> | <span data-ttu-id="d2429-124">像素著色器</span><span class="sxs-lookup"><span data-stu-id="d2429-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d2429-125">x</span><span class="sxs-lookup"><span data-stu-id="d2429-125">x</span></span>             | <span data-ttu-id="d2429-126">x</span><span class="sxs-lookup"><span data-stu-id="d2429-126">x</span></span>               | <span data-ttu-id="d2429-127">x</span><span class="sxs-lookup"><span data-stu-id="d2429-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d2429-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d2429-128">Minimum Shader Model</span></span>

<span data-ttu-id="d2429-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d2429-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2429-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d2429-130">Shader Model</span></span>                                              | <span data-ttu-id="d2429-131">支援</span><span class="sxs-lookup"><span data-stu-id="d2429-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d2429-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d2429-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d2429-133">是</span><span class="sxs-lookup"><span data-stu-id="d2429-133">yes</span></span>       |
| [<span data-ttu-id="d2429-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d2429-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d2429-135">是</span><span class="sxs-lookup"><span data-stu-id="d2429-135">yes</span></span>       |
| [<span data-ttu-id="d2429-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d2429-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d2429-137">是</span><span class="sxs-lookup"><span data-stu-id="d2429-137">yes</span></span>       |
| [<span data-ttu-id="d2429-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2429-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d2429-139">不可以</span><span class="sxs-lookup"><span data-stu-id="d2429-139">no</span></span>        |
| [<span data-ttu-id="d2429-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2429-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d2429-141">不可以</span><span class="sxs-lookup"><span data-stu-id="d2429-141">no</span></span>        |
| [<span data-ttu-id="d2429-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2429-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d2429-143">不可以</span><span class="sxs-lookup"><span data-stu-id="d2429-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d2429-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2429-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2429-145">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2429-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





