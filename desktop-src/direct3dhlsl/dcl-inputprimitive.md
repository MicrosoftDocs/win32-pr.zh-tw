---
title: 'dcl_inputPrimitive (sm4-asm) '
description: 'dcl \_ inputPrimitive (sm4-asm) '
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932829"
---
# <a name="dcl_inputprimitive-sm4---asm"></a><span data-ttu-id="a5773-103">dcl \_ inputPrimitive (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="a5773-103">dcl\_inputPrimitive (sm4 - asm)</span></span>

<span data-ttu-id="a5773-104">宣告幾何著色器輸入的基本類型。</span><span class="sxs-lookup"><span data-stu-id="a5773-104">Declares the primitive type for geometry-shader inputs.</span></span>



| <span data-ttu-id="a5773-105">dcl \_ inputPrimitive *類型*</span><span class="sxs-lookup"><span data-stu-id="a5773-105">dcl\_inputPrimitive *type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5773-106">項目</span><span class="sxs-lookup"><span data-stu-id="a5773-106">Item</span></span></th>
<th><span data-ttu-id="a5773-107">描述</span><span class="sxs-lookup"><span data-stu-id="a5773-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5773-108"><span id="type"></span><span id="TYPE"></span><em>類型</em></span><span class="sxs-lookup"><span data-stu-id="a5773-108"><span id="type"></span><span id="TYPE"></span><em>type</em></span></span><br/></td>
<td><span data-ttu-id="a5773-109">在輸入-資料基本類型，這是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="a5773-109">[in] Input-data primitive type, which is one of the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="a5773-110"><em>點</em> - 點清單</span><span class="sxs-lookup"><span data-stu-id="a5773-110"><em>point</em> - point list</span></span></li>
<li><span data-ttu-id="a5773-111"><em>行</em> - 行清單</span><span class="sxs-lookup"><span data-stu-id="a5773-111"><em>line</em> - line list</span></span></li>
<li><span data-ttu-id="a5773-112"><em>三角形</em> - 三角形清單</span><span class="sxs-lookup"><span data-stu-id="a5773-112"><em>triangle</em> - triangle list</span></span></li>
<li><span data-ttu-id="a5773-113"><em>line_adj</em> - 具有相鄰資料的行清單</span><span class="sxs-lookup"><span data-stu-id="a5773-113"><em>line_adj</em> - line list with adjacency data</span></span></li>
<li><span data-ttu-id="a5773-114"><em>triangle_adj</em> - 具有相鄰資料的三角形清單</span><span class="sxs-lookup"><span data-stu-id="a5773-114"><em>triangle_adj</em> - triangle list with adjacency data</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a5773-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a5773-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a5773-116">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="a5773-116">Vertex Shader</span></span> | <span data-ttu-id="a5773-117">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="a5773-117">Geometry Shader</span></span> | <span data-ttu-id="a5773-118">像素著色器</span><span class="sxs-lookup"><span data-stu-id="a5773-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="a5773-119">x</span><span class="sxs-lookup"><span data-stu-id="a5773-119">x</span></span>               |              |



 

<span data-ttu-id="a5773-120">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="a5773-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="a5773-121">範例</span><span class="sxs-lookup"><span data-stu-id="a5773-121">Example</span></span>

<span data-ttu-id="a5773-122">範例如下。</span><span class="sxs-lookup"><span data-stu-id="a5773-122">Here is an example.</span></span>


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a><span data-ttu-id="a5773-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a5773-123">Minimum Shader Model</span></span>

<span data-ttu-id="a5773-124">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a5773-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a5773-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a5773-125">Shader Model</span></span>                                              | <span data-ttu-id="a5773-126">支援</span><span class="sxs-lookup"><span data-stu-id="a5773-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a5773-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a5773-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a5773-128">是</span><span class="sxs-lookup"><span data-stu-id="a5773-128">yes</span></span>       |
| [<span data-ttu-id="a5773-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a5773-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a5773-130">是</span><span class="sxs-lookup"><span data-stu-id="a5773-130">yes</span></span>       |
| [<span data-ttu-id="a5773-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a5773-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a5773-132">是</span><span class="sxs-lookup"><span data-stu-id="a5773-132">yes</span></span>       |
| [<span data-ttu-id="a5773-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5773-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a5773-134">不可以</span><span class="sxs-lookup"><span data-stu-id="a5773-134">no</span></span>        |
| [<span data-ttu-id="a5773-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5773-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a5773-136">不可以</span><span class="sxs-lookup"><span data-stu-id="a5773-136">no</span></span>        |
| [<span data-ttu-id="a5773-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5773-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a5773-138">不可以</span><span class="sxs-lookup"><span data-stu-id="a5773-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a5773-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5773-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5773-140">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5773-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





