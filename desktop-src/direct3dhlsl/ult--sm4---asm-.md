---
title: 'u)  (sm4-asm) '
description: 元件型向量不帶正負號的整數小於比較。
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990739"
---
# <a name="ult-sm4---asm"></a><span data-ttu-id="9483f-103">u)  (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="9483f-103">ult (sm4 - asm)</span></span>

<span data-ttu-id="9483f-104">元件型向量不帶正負號的整數小於比較。</span><span class="sxs-lookup"><span data-stu-id="9483f-104">Component-wise vector unsigned integer less-than comparison.</span></span>



| <span data-ttu-id="9483f-105">u) dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9483f-105">ult dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="9483f-106">項目</span><span class="sxs-lookup"><span data-stu-id="9483f-106">Item</span></span>                                                            | <span data-ttu-id="9483f-107">描述</span><span class="sxs-lookup"><span data-stu-id="9483f-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9483f-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="9483f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9483f-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="9483f-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="9483f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9483f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9483f-111">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="9483f-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="9483f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="9483f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9483f-113">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="9483f-113">\[in\] The value to compare to *src1*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="9483f-114">備註</span><span class="sxs-lookup"><span data-stu-id="9483f-114">Remarks</span></span>

<span data-ttu-id="9483f-115">針對每個元件執行不帶正負號的整數比較 (*src0*  <  *src1*) ，並將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="9483f-115">Performs the unsigned integer comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="9483f-116">如果比較結果為 true，則此指令會傳回該元件的0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="9483f-116">If the comparison is true, this instruction returns 0xFFFFFFFF for that component.</span></span> <span data-ttu-id="9483f-117">否則，它會傳回0x0000000。</span><span class="sxs-lookup"><span data-stu-id="9483f-117">Otherwise it returns 0x0000000.</span></span>

<span data-ttu-id="9483f-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9483f-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9483f-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="9483f-119">Vertex Shader</span></span> | <span data-ttu-id="9483f-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="9483f-120">Geometry Shader</span></span> | <span data-ttu-id="9483f-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="9483f-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9483f-122">x</span><span class="sxs-lookup"><span data-stu-id="9483f-122">x</span></span>             | <span data-ttu-id="9483f-123">x</span><span class="sxs-lookup"><span data-stu-id="9483f-123">x</span></span>               | <span data-ttu-id="9483f-124">x</span><span class="sxs-lookup"><span data-stu-id="9483f-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9483f-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9483f-125">Minimum Shader Model</span></span>

<span data-ttu-id="9483f-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9483f-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9483f-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9483f-127">Shader Model</span></span>                                              | <span data-ttu-id="9483f-128">支援</span><span class="sxs-lookup"><span data-stu-id="9483f-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9483f-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9483f-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9483f-130">是</span><span class="sxs-lookup"><span data-stu-id="9483f-130">yes</span></span>       |
| [<span data-ttu-id="9483f-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9483f-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9483f-132">是</span><span class="sxs-lookup"><span data-stu-id="9483f-132">yes</span></span>       |
| [<span data-ttu-id="9483f-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9483f-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9483f-134">是</span><span class="sxs-lookup"><span data-stu-id="9483f-134">yes</span></span>       |
| [<span data-ttu-id="9483f-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9483f-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9483f-136">不可以</span><span class="sxs-lookup"><span data-stu-id="9483f-136">no</span></span>        |
| [<span data-ttu-id="9483f-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9483f-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9483f-138">不可以</span><span class="sxs-lookup"><span data-stu-id="9483f-138">no</span></span>        |
| [<span data-ttu-id="9483f-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9483f-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9483f-140">不可以</span><span class="sxs-lookup"><span data-stu-id="9483f-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9483f-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="9483f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9483f-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9483f-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





