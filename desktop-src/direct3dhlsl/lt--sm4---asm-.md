---
title: 'lt (sm4-asm) '
description: 元件的向量浮點數小於比較。
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a727987e4eaee017137d62dbe12f8581540876
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313676"
---
# <a name="lt-sm4---asm"></a><span data-ttu-id="72639-103">lt (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="72639-103">lt (sm4 - asm)</span></span>

<span data-ttu-id="72639-104">元件的向量浮點數小於比較。</span><span class="sxs-lookup"><span data-stu-id="72639-104">Component-wise vector floating point less-than comparison.</span></span>



| <span data-ttu-id="72639-105">lt dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="72639-105">lt dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="72639-106">項目</span><span class="sxs-lookup"><span data-stu-id="72639-106">Item</span></span>                                                            | <span data-ttu-id="72639-107">描述</span><span class="sxs-lookup"><span data-stu-id="72639-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="72639-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="72639-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="72639-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="72639-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="72639-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="72639-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="72639-111">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="72639-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="72639-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="72639-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="72639-113">\[在 \] [要與 *src0* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="72639-113">\[in\] The value to compare to *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="72639-114">備註</span><span class="sxs-lookup"><span data-stu-id="72639-114">Remarks</span></span>

<span data-ttu-id="72639-115">此指令會針對每個元件執行浮點數比較 (*src0*  <  *src1*) ，並將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="72639-115">This instruction performs the float comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="72639-116">如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="72639-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="72639-117">否則會傳回0x0000000</span><span class="sxs-lookup"><span data-stu-id="72639-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="72639-118">Denorms 會在比較之前排清;原始來源暫存器沒有改變。</span><span class="sxs-lookup"><span data-stu-id="72639-118">Denorms are flushed before comparison; original source registers are untouched.</span></span>

<span data-ttu-id="72639-119">+ 0 等於-0。</span><span class="sxs-lookup"><span data-stu-id="72639-119">+0 equals -0.</span></span>

<span data-ttu-id="72639-120">與 NaN 的比較會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="72639-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="72639-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="72639-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="72639-122">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="72639-122">Vertex Shader</span></span> | <span data-ttu-id="72639-123">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="72639-123">Geometry Shader</span></span> | <span data-ttu-id="72639-124">像素著色器</span><span class="sxs-lookup"><span data-stu-id="72639-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="72639-125">x</span><span class="sxs-lookup"><span data-stu-id="72639-125">x</span></span>             | <span data-ttu-id="72639-126">x</span><span class="sxs-lookup"><span data-stu-id="72639-126">x</span></span>               | <span data-ttu-id="72639-127">x</span><span class="sxs-lookup"><span data-stu-id="72639-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="72639-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="72639-128">Minimum Shader Model</span></span>

<span data-ttu-id="72639-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="72639-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="72639-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="72639-130">Shader Model</span></span>                                              | <span data-ttu-id="72639-131">支援</span><span class="sxs-lookup"><span data-stu-id="72639-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="72639-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="72639-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="72639-133">是</span><span class="sxs-lookup"><span data-stu-id="72639-133">yes</span></span>       |
| [<span data-ttu-id="72639-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="72639-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="72639-135">是</span><span class="sxs-lookup"><span data-stu-id="72639-135">yes</span></span>       |
| [<span data-ttu-id="72639-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="72639-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="72639-137">是</span><span class="sxs-lookup"><span data-stu-id="72639-137">yes</span></span>       |
| [<span data-ttu-id="72639-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="72639-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="72639-139">不可以</span><span class="sxs-lookup"><span data-stu-id="72639-139">no</span></span>        |
| [<span data-ttu-id="72639-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="72639-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="72639-141">不可以</span><span class="sxs-lookup"><span data-stu-id="72639-141">no</span></span>        |
| [<span data-ttu-id="72639-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="72639-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="72639-143">不可以</span><span class="sxs-lookup"><span data-stu-id="72639-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="72639-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="72639-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72639-145">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="72639-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





