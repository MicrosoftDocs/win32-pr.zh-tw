---
title: 'dcl_indexableTemp (sm4-asm) '
description: 'dcl \_ indexableTemp (sm4-asm) '
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990843"
---
# <a name="dcl_indexabletemp-sm4---asm"></a><span data-ttu-id="31957-103">dcl \_ indexableTemp (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="31957-103">dcl\_indexableTemp (sm4 - asm)</span></span>

<span data-ttu-id="31957-104">宣告可編制索引的臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="31957-104">Declares an indexable, temporary register.</span></span>



| <span data-ttu-id="31957-105">dcl \_ indexableTemp x *N \[ 大小 \] ，ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="31957-105">dcl\_indexableTemp x *N\[size\], ComponentCount*</span></span> |
|-------------------------------------------------|



 



| <span data-ttu-id="31957-106">項目</span><span class="sxs-lookup"><span data-stu-id="31957-106">Item</span></span>                                                                                                                           | <span data-ttu-id="31957-107">描述</span><span class="sxs-lookup"><span data-stu-id="31957-107">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="31957-108"><span id="N"></span><span id="n"></span>*N-1*</span><span class="sxs-lookup"><span data-stu-id="31957-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/>                                                                         | <span data-ttu-id="31957-109">\[\]代表註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="31957-109">\[in\] An integer that denotes the register number.</span></span><br/>                              |
| <span data-ttu-id="31957-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[大小\]*</span><span class="sxs-lookup"><span data-stu-id="31957-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[size\]*</span></span><br/>                                                        | <span data-ttu-id="31957-111">\[在 \] 選擇性的整數值中。</span><span class="sxs-lookup"><span data-stu-id="31957-111">\[in\] An optional integer value.</span></span> <span data-ttu-id="31957-112">暫存器陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="31957-112">The number of elements in the register array.</span></span><br/>  |
| <span data-ttu-id="31957-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="31957-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span></span><br/> | <span data-ttu-id="31957-114">\[在 \] 選擇性的整數值中。暫存器陣列中的元件數目。</span><span class="sxs-lookup"><span data-stu-id="31957-114">\[in\] An optional integer value.The number of components in the register array.</span></span><br/> |



 

<span data-ttu-id="31957-115">暫存器包含足夠的空間來容納32位的四個元件值;臨時暫存器陣列中的元素數目 (可編制索引和 [不可索引](dcl-temps.md) 的) 不能超過4096。</span><span class="sxs-lookup"><span data-stu-id="31957-115">A register contains enough space for a 32-bit four-component value; the number of elements in the array of temporary registers (indexable and [non-indexable](dcl-temps.md)) cannot exceed 4096.</span></span>

<span data-ttu-id="31957-116">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="31957-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="31957-117">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="31957-117">Vertex Shader</span></span> | <span data-ttu-id="31957-118">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="31957-118">Geometry Shader</span></span> | <span data-ttu-id="31957-119">像素著色器</span><span class="sxs-lookup"><span data-stu-id="31957-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="31957-120">x</span><span class="sxs-lookup"><span data-stu-id="31957-120">x</span></span>             | <span data-ttu-id="31957-121">x</span><span class="sxs-lookup"><span data-stu-id="31957-121">x</span></span>               | <span data-ttu-id="31957-122">x</span><span class="sxs-lookup"><span data-stu-id="31957-122">x</span></span>            |



 

<span data-ttu-id="31957-123">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="31957-123">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="31957-124">範例</span><span class="sxs-lookup"><span data-stu-id="31957-124">Example</span></span>

<span data-ttu-id="31957-125">以下是針對可編制索引的暫存器所產生之程式碼的一些範例。</span><span class="sxs-lookup"><span data-stu-id="31957-125">Here are some examples of the code generated for indexable registers.</span></span>


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a><span data-ttu-id="31957-126">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="31957-126">Minimum Shader Model</span></span>

<span data-ttu-id="31957-127">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="31957-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="31957-128">著色器模型</span><span class="sxs-lookup"><span data-stu-id="31957-128">Shader Model</span></span>                                              | <span data-ttu-id="31957-129">支援</span><span class="sxs-lookup"><span data-stu-id="31957-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="31957-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="31957-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="31957-131">是</span><span class="sxs-lookup"><span data-stu-id="31957-131">yes</span></span>       |
| [<span data-ttu-id="31957-132">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="31957-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="31957-133">是</span><span class="sxs-lookup"><span data-stu-id="31957-133">yes</span></span>       |
| [<span data-ttu-id="31957-134">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="31957-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="31957-135">是</span><span class="sxs-lookup"><span data-stu-id="31957-135">yes</span></span>       |
| [<span data-ttu-id="31957-136">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="31957-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="31957-137">不可以</span><span class="sxs-lookup"><span data-stu-id="31957-137">no</span></span>        |
| [<span data-ttu-id="31957-138">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="31957-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="31957-139">不可以</span><span class="sxs-lookup"><span data-stu-id="31957-139">no</span></span>        |
| [<span data-ttu-id="31957-140">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="31957-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="31957-141">不可以</span><span class="sxs-lookup"><span data-stu-id="31957-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="31957-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="31957-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31957-143">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="31957-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





