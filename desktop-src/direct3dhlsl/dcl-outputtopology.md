---
title: 'dcl_outputTopology (sm4-asm) '
description: 'dcl \_ outputTopology (sm4-asm) '
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679183"
---
# <a name="dcl_outputtopology-sm4---asm"></a><span data-ttu-id="d748b-103">dcl \_ outputTopology (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="d748b-103">dcl\_outputTopology (sm4 - asm)</span></span>

<span data-ttu-id="d748b-104">宣告基本類型幾何著色器輸出資料。</span><span class="sxs-lookup"><span data-stu-id="d748b-104">Declares the primitive type geometry-shader output data.</span></span>



| <span data-ttu-id="d748b-105">dcl \_ OutputTopology *類型*</span><span class="sxs-lookup"><span data-stu-id="d748b-105">dcl\_outputTopology *Type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d748b-106">項目</span><span class="sxs-lookup"><span data-stu-id="d748b-106">Item</span></span></th>
<th><span data-ttu-id="d748b-107">描述</span><span class="sxs-lookup"><span data-stu-id="d748b-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d748b-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>類型</em></span><span class="sxs-lookup"><span data-stu-id="d748b-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span><br/></td>
<td><span data-ttu-id="d748b-109">在輸出基本拓撲，這是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="d748b-109">[in] An output primitive topology, which is one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="d748b-110"><em>pointlist</em></span><span class="sxs-lookup"><span data-stu-id="d748b-110"><em>pointlist</em></span></span></li>
<li><span data-ttu-id="d748b-111"><em>linestrip</em></span><span class="sxs-lookup"><span data-stu-id="d748b-111"><em>linestrip</em></span></span></li>
<li><span data-ttu-id="d748b-112"><em>trianglestrip</em></span><span class="sxs-lookup"><span data-stu-id="d748b-112"><em>trianglestrip</em></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d748b-113">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d748b-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d748b-114">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="d748b-114">Vertex Shader</span></span> | <span data-ttu-id="d748b-115">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="d748b-115">Geometry Shader</span></span> | <span data-ttu-id="d748b-116">像素著色器</span><span class="sxs-lookup"><span data-stu-id="d748b-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="d748b-117">x</span><span class="sxs-lookup"><span data-stu-id="d748b-117">x</span></span>               |              |



 

<span data-ttu-id="d748b-118">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="d748b-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="d748b-119">範例</span><span class="sxs-lookup"><span data-stu-id="d748b-119">Example</span></span>

<span data-ttu-id="d748b-120">範例如下。</span><span class="sxs-lookup"><span data-stu-id="d748b-120">Here is an example.</span></span>


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a><span data-ttu-id="d748b-121">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d748b-121">Minimum Shader Model</span></span>

<span data-ttu-id="d748b-122">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d748b-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d748b-123">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d748b-123">Shader Model</span></span>                                              | <span data-ttu-id="d748b-124">支援</span><span class="sxs-lookup"><span data-stu-id="d748b-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d748b-125">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d748b-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d748b-126">是</span><span class="sxs-lookup"><span data-stu-id="d748b-126">yes</span></span>       |
| [<span data-ttu-id="d748b-127">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d748b-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d748b-128">是</span><span class="sxs-lookup"><span data-stu-id="d748b-128">yes</span></span>       |
| [<span data-ttu-id="d748b-129">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d748b-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d748b-130">是</span><span class="sxs-lookup"><span data-stu-id="d748b-130">yes</span></span>       |
| [<span data-ttu-id="d748b-131">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d748b-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d748b-132">不可以</span><span class="sxs-lookup"><span data-stu-id="d748b-132">no</span></span>        |
| [<span data-ttu-id="d748b-133">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d748b-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d748b-134">不可以</span><span class="sxs-lookup"><span data-stu-id="d748b-134">no</span></span>        |
| [<span data-ttu-id="d748b-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d748b-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d748b-136">不可以</span><span class="sxs-lookup"><span data-stu-id="d748b-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d748b-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="d748b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d748b-138">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d748b-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





