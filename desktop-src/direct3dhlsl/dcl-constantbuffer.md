---
title: 'dcl_constantBuffer (sm4-asm) '
description: 'dcl \_ constantBuffer (sm4-asm) '
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092459"
---
# <a name="dcl_constantbuffer-sm4---asm"></a><span data-ttu-id="569a5-103">dcl \_ constantBuffer (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="569a5-103">dcl\_constantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="569a5-104">宣告著色器常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="569a5-104">Declares a shader constant buffer.</span></span>



| <span data-ttu-id="569a5-105">dcl \_ constantBuffer *cbN \[ size \]*， *AccessPattern*</span><span class="sxs-lookup"><span data-stu-id="569a5-105">dcl\_constantBuffer *cbN\[size\]*, *AccessPattern*</span></span> |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="569a5-106">項目</span><span class="sxs-lookup"><span data-stu-id="569a5-106">Item</span></span></th>
<th><span data-ttu-id="569a5-107">描述</span><span class="sxs-lookup"><span data-stu-id="569a5-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="569a5-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N [大小]</em></span><span class="sxs-lookup"><span data-stu-id="569a5-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em></span></span><br/></td>
<td><span data-ttu-id="569a5-109">在著色器常數緩衝區，其中 N 是表示常數緩衝區暫存器編號的整數，而 size 是表示緩衝區中專案數目的整數。</span><span class="sxs-lookup"><span data-stu-id="569a5-109">[in] A shader constant buffer where N is an integer that denotes the constant-buffer-register number and size is an integer that denotes the number of elements in the buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="569a5-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span><span class="sxs-lookup"><span data-stu-id="569a5-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span></span><br/></td>
<td><span data-ttu-id="569a5-111">在著色器程式碼將存取緩衝區的方式，這是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="569a5-111">[in] The way that the buffer will be accessed by shader code, which is one of the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="569a5-112">Name</span><span class="sxs-lookup"><span data-stu-id="569a5-112">Name</span></span></th>
<th><span data-ttu-id="569a5-113">描述</span><span class="sxs-lookup"><span data-stu-id="569a5-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="569a5-114">immediateIndexed</span><span class="sxs-lookup"><span data-stu-id="569a5-114">immediateIndexed</span></span></td>
<td><span data-ttu-id="569a5-115">使用常值為緩衝區編制索引。</span><span class="sxs-lookup"><span data-stu-id="569a5-115">Index the buffer with a literal value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="569a5-116">dynamic_indexed</span><span class="sxs-lookup"><span data-stu-id="569a5-116">dynamic_indexed</span></span></td>
<td><span data-ttu-id="569a5-117">使用評估運算式的結果來編制緩衝區的索引。</span><span class="sxs-lookup"><span data-stu-id="569a5-117">Index the buffer with the result of an evaluated expression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="569a5-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="569a5-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="569a5-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="569a5-119">Vertex Shader</span></span> | <span data-ttu-id="569a5-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="569a5-120">Geometry Shader</span></span> | <span data-ttu-id="569a5-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="569a5-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="569a5-122">x</span><span class="sxs-lookup"><span data-stu-id="569a5-122">x</span></span>             | <span data-ttu-id="569a5-123">x</span><span class="sxs-lookup"><span data-stu-id="569a5-123">x</span></span>               | <span data-ttu-id="569a5-124">x</span><span class="sxs-lookup"><span data-stu-id="569a5-124">x</span></span>            |



 

<span data-ttu-id="569a5-125">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="569a5-125">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="569a5-126">範例</span><span class="sxs-lookup"><span data-stu-id="569a5-126">Example</span></span>

<span data-ttu-id="569a5-127">此範例會為 register cb0 宣告常數緩衝區，其中有19個元素。</span><span class="sxs-lookup"><span data-stu-id="569a5-127">This example declares a constant buffer for register cb0, which has 19 elements.</span></span> <span data-ttu-id="569a5-128">您可以使用常值索引來存取這些元素。</span><span class="sxs-lookup"><span data-stu-id="569a5-128">These elements are accessed with a literal index.</span></span>


```
dcl_constantbuffer  cb0[19], immediateIndexed
```



## <a name="minimum-shader-model"></a><span data-ttu-id="569a5-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="569a5-129">Minimum Shader Model</span></span>

<span data-ttu-id="569a5-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="569a5-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="569a5-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="569a5-131">Shader Model</span></span>                                              | <span data-ttu-id="569a5-132">支援</span><span class="sxs-lookup"><span data-stu-id="569a5-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="569a5-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="569a5-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="569a5-134">是</span><span class="sxs-lookup"><span data-stu-id="569a5-134">yes</span></span>       |
| [<span data-ttu-id="569a5-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="569a5-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="569a5-136">是</span><span class="sxs-lookup"><span data-stu-id="569a5-136">yes</span></span>       |
| [<span data-ttu-id="569a5-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="569a5-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="569a5-138">是</span><span class="sxs-lookup"><span data-stu-id="569a5-138">yes</span></span>       |
| [<span data-ttu-id="569a5-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="569a5-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="569a5-140">不可以</span><span class="sxs-lookup"><span data-stu-id="569a5-140">no</span></span>        |
| [<span data-ttu-id="569a5-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="569a5-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="569a5-142">不可以</span><span class="sxs-lookup"><span data-stu-id="569a5-142">no</span></span>        |
| [<span data-ttu-id="569a5-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="569a5-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="569a5-144">不可以</span><span class="sxs-lookup"><span data-stu-id="569a5-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="569a5-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="569a5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="569a5-146">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="569a5-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





