---
title: 'dcl_indexRange (sm4-asm) '
description: 'dcl \_ indexRange (sm4-asm) '
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971621"
---
# <a name="dcl_indexrange-sm4---asm"></a><span data-ttu-id="470a2-103">dcl \_ indexRange (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="470a2-103">dcl\_indexRange (sm4 - asm)</span></span>

<span data-ttu-id="470a2-104">宣告將由索引存取的暫存器範圍 (在著色器) 中計算的整數。</span><span class="sxs-lookup"><span data-stu-id="470a2-104">Declares a range of registers that will be accessed by index (an integer computed in the shader).</span></span>



| <span data-ttu-id="470a2-105">dcl \_ IndexRange *minRegisterM*， *maxRegisterN*</span><span class="sxs-lookup"><span data-stu-id="470a2-105">dcl\_indexRange *minRegisterM*, *maxRegisterN*</span></span> |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="470a2-106">項目</span><span class="sxs-lookup"><span data-stu-id="470a2-106">Item</span></span></th>
<th><span data-ttu-id="470a2-107">描述</span><span class="sxs-lookup"><span data-stu-id="470a2-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="470a2-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span><span class="sxs-lookup"><span data-stu-id="470a2-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span></span><br/></td>
<td><span data-ttu-id="470a2-109">在要依索引存取的第一個註冊。</span><span class="sxs-lookup"><span data-stu-id="470a2-109">[in] The first register to access by index.</span></span> <br/>
<ul>
<li><span data-ttu-id="470a2-110">針對頂點或圖元著色器輸入暫存器， <em>minRegister</em>是<strong>v</strong> ，或頂點著色器輸出暫存器的<strong>o</strong> 。</span><span class="sxs-lookup"><span data-stu-id="470a2-110"><em>minRegister</em> is either <strong>v</strong> for a vertex or pixel shader input register, or <strong>o</strong> for a vertex shader output register.</span></span></li>
<li><span data-ttu-id="470a2-111"><em>M</em> 是表示註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="470a2-111"><em>M</em> is an integer that denotes the register number.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="470a2-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span><span class="sxs-lookup"><span data-stu-id="470a2-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span></span><br/></td>
<td><span data-ttu-id="470a2-113">在要依索引存取的最後一個暫存器。</span><span class="sxs-lookup"><span data-stu-id="470a2-113">[in] The last register to access by index.</span></span> <span data-ttu-id="470a2-114">與 <em>minRegister</em> 相同的表單，但 <em>N</em> 是註冊編號。</span><span class="sxs-lookup"><span data-stu-id="470a2-114">Same form as <em>minRegister</em> except <em>N</em> is the register number.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="470a2-115">下列限制適用于所有註冊：</span><span class="sxs-lookup"><span data-stu-id="470a2-115">The following restrictions apply to all registers:</span></span>

-   <span data-ttu-id="470a2-116">最小和最大暫存器必須是相同的類型，而且如果遮罩宣告) ，則相同的元件遮罩 (。</span><span class="sxs-lookup"><span data-stu-id="470a2-116">The min and max registers must be the same type and have the same component masks (if masks are declared).</span></span>
-   <span data-ttu-id="470a2-117">註冊可以有多個索引範圍，只要它們不會重迭。</span><span class="sxs-lookup"><span data-stu-id="470a2-117">A register may have multiple index ranges, as long as they do no not overlap.</span></span>
-   <span data-ttu-id="470a2-118">最小注冊號碼必須小於最大註冊編號。</span><span class="sxs-lookup"><span data-stu-id="470a2-118">The min register number must be less than the max register number.</span></span>
-   <span data-ttu-id="470a2-119">索引暫存器不能包含 [系統值](dx-graphics-hlsl-semantics.md)。</span><span class="sxs-lookup"><span data-stu-id="470a2-119">An index register cannot contain a [system-value](dx-graphics-hlsl-semantics.md).</span></span>
-   <span data-ttu-id="470a2-120">在 max index 宣告之外索引暫存器會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="470a2-120">Indexing a register outside of the max index declaration produces undefined results.</span></span>

<span data-ttu-id="470a2-121">圖元著色器輸入暫存器必須使用相同的插補模式;圖元著色器輸出暫存器無法編制索引。</span><span class="sxs-lookup"><span data-stu-id="470a2-121">Pixel shader input registers must use the same interpolation mode; pixel shader output registers are not indexable.</span></span>

<span data-ttu-id="470a2-122">幾何著色器輸入暫存器有兩個維度 (頂點軸、屬性軸) ;索引範圍只適用于屬性軸，因為頂點軸永遠是可完全索引的。</span><span class="sxs-lookup"><span data-stu-id="470a2-122">A geometry shader input register has two dimensions (vertex axis, attribute axis); the index range applies only to the attribute axis because the vertex axis is always fully indexable.</span></span>

<span data-ttu-id="470a2-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="470a2-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="470a2-124">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="470a2-124">Vertex Shader</span></span> | <span data-ttu-id="470a2-125">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="470a2-125">Geometry Shader</span></span> | <span data-ttu-id="470a2-126">像素著色器</span><span class="sxs-lookup"><span data-stu-id="470a2-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="470a2-127">x</span><span class="sxs-lookup"><span data-stu-id="470a2-127">x</span></span>             | <span data-ttu-id="470a2-128">x</span><span class="sxs-lookup"><span data-stu-id="470a2-128">x</span></span>               | <span data-ttu-id="470a2-129">x</span><span class="sxs-lookup"><span data-stu-id="470a2-129">x</span></span>            |



 

<span data-ttu-id="470a2-130">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="470a2-130">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="470a2-131">範例</span><span class="sxs-lookup"><span data-stu-id="470a2-131">Example</span></span>

<span data-ttu-id="470a2-132">範例如下。</span><span class="sxs-lookup"><span data-stu-id="470a2-132">Here is an example.</span></span>


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="470a2-133">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="470a2-133">Minimum Shader Model</span></span>

<span data-ttu-id="470a2-134">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="470a2-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="470a2-135">著色器模型</span><span class="sxs-lookup"><span data-stu-id="470a2-135">Shader Model</span></span>                                              | <span data-ttu-id="470a2-136">支援</span><span class="sxs-lookup"><span data-stu-id="470a2-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="470a2-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="470a2-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="470a2-138">是</span><span class="sxs-lookup"><span data-stu-id="470a2-138">yes</span></span>       |
| [<span data-ttu-id="470a2-139">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="470a2-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="470a2-140">是</span><span class="sxs-lookup"><span data-stu-id="470a2-140">yes</span></span>       |
| [<span data-ttu-id="470a2-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="470a2-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="470a2-142">是</span><span class="sxs-lookup"><span data-stu-id="470a2-142">yes</span></span>       |
| [<span data-ttu-id="470a2-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="470a2-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="470a2-144">不可以</span><span class="sxs-lookup"><span data-stu-id="470a2-144">no</span></span>        |
| [<span data-ttu-id="470a2-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="470a2-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="470a2-146">不可以</span><span class="sxs-lookup"><span data-stu-id="470a2-146">no</span></span>        |
| [<span data-ttu-id="470a2-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="470a2-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="470a2-148">不可以</span><span class="sxs-lookup"><span data-stu-id="470a2-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="470a2-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="470a2-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="470a2-150">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="470a2-150">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





