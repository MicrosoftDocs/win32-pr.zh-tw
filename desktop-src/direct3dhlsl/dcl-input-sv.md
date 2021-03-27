---
title: 'dcl_input_sv (sm4-asm) '
description: 'dcl \_ 輸入 \_ sv (sm4-asm) '
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679191"
---
# <a name="dcl_input_sv-sm4---asm"></a><span data-ttu-id="7a49f-103">dcl \_ 輸入 \_ sv (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="7a49f-103">dcl\_input\_sv (sm4 - asm)</span></span>

<span data-ttu-id="7a49f-104">宣告需要從先前階段提供 [系統值](dx-graphics-hlsl-semantics.md) 的著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="7a49f-104">Declares a shader-input register that expects a [system-value](dx-graphics-hlsl-semantics.md) to be provided from a preceding stage.</span></span>



| <span data-ttu-id="7a49f-105">dcl \_ 輸入 \_ sv v *N \[ . mask \]*、 *systemValueName \[ 、interpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="7a49f-105">dcl\_input\_sv v *N\[.mask\]*, *systemValueName\[, interpolationMode\]*</span></span> |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a49f-106">項目</span><span class="sxs-lookup"><span data-stu-id="7a49f-106">Item</span></span></th>
<th><span data-ttu-id="7a49f-107">描述</span><span class="sxs-lookup"><span data-stu-id="7a49f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a49f-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [mask]</em></span><span class="sxs-lookup"><span data-stu-id="7a49f-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="7a49f-109">在頂點資料註冊。</span><span class="sxs-lookup"><span data-stu-id="7a49f-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="7a49f-110"><em>N</em> 是識別註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="7a49f-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="7a49f-111"><em>[mask]</em> 是選擇性的元件遮罩 ( xyzw) ，可指定要使用的註冊元件。</span><span class="sxs-lookup"><span data-stu-id="7a49f-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a49f-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span><span class="sxs-lookup"><span data-stu-id="7a49f-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span></span><br/></td>
<td><span data-ttu-id="7a49f-113">在系統值名稱，也就是字串 (請參閱 <a href="dx-graphics-hlsl-semantics.md">系統值語義</a>) ，而不使用 &quot; SV_ &quot; 前置詞。</span><span class="sxs-lookup"><span data-stu-id="7a49f-113">[in] The system-value name which is a string (see <a href="dx-graphics-hlsl-semantics.md">system-value semantics</a>) without the &quot;SV_&quot; prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a49f-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="7a49f-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="7a49f-115">[in] 選用。</span><span class="sxs-lookup"><span data-stu-id="7a49f-115">[in] Optional.</span></span> <span data-ttu-id="7a49f-116">插補模式，它會影響在點陣化期間計算值的方式;只有圖元著色器會使用此模式。</span><span class="sxs-lookup"><span data-stu-id="7a49f-116">The interpolation mode which affects how values are calculated during rasterization; the mode is only used by a pixel shader.</span></span> <span data-ttu-id="7a49f-117">它可能是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="7a49f-117">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="7a49f-118">常數-不在暫存器值之間插補。</span><span class="sxs-lookup"><span data-stu-id="7a49f-118">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="7a49f-119">線性-在註冊值之間以線性方式插補。</span><span class="sxs-lookup"><span data-stu-id="7a49f-119">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="7a49f-120">linearCentroid-與線性相同，但在取樣時距心壓制。</span><span class="sxs-lookup"><span data-stu-id="7a49f-120">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="7a49f-121">linearNoperspective-與線性相同，但沒有透視校正。</span><span class="sxs-lookup"><span data-stu-id="7a49f-121">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="7a49f-122">linearNoperspectiveCentroid-與線性相同，但在交叉取樣時沒有透視更正和距心壓制。</span><span class="sxs-lookup"><span data-stu-id="7a49f-122">linearNoperspectiveCentroid - same as linear but with no perspective correction and centroid clamped when multisampling.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7a49f-123">系統值宣告的元件遮罩可以是任何適當的 xyzw 子集; 宣告 \[ \] 可能不會重迭 (每個宣告都必須遵循序列 xyzw) 。</span><span class="sxs-lookup"><span data-stu-id="7a49f-123">A component mask for a system-value declaration can be any appropriate subset of \[xyzw\]; declarations may not overlap (each declaration must follow the sequence xyzw).</span></span> <span data-ttu-id="7a49f-124">宣告純量系統值 (剪切距離和剔除距離（例如) ）時，您可以在單一暫存器中宣告多個系統值。</span><span class="sxs-lookup"><span data-stu-id="7a49f-124">When declaring scalar system values (clip distance and cull distance for example), you can declare multiple system values in a single register.</span></span> <span data-ttu-id="7a49f-125">如果您這樣做，請確定其他修飾詞（例如插補模式）相符。</span><span class="sxs-lookup"><span data-stu-id="7a49f-125">If you do so, make sure other modifiers like the interpolation modes match.</span></span>

<span data-ttu-id="7a49f-126">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="7a49f-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7a49f-127">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="7a49f-127">Vertex Shader</span></span> | <span data-ttu-id="7a49f-128">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="7a49f-128">Geometry Shader</span></span> | <span data-ttu-id="7a49f-129">像素著色器</span><span class="sxs-lookup"><span data-stu-id="7a49f-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7a49f-130">x</span><span class="sxs-lookup"><span data-stu-id="7a49f-130">x</span></span>             | <span data-ttu-id="7a49f-131">x</span><span class="sxs-lookup"><span data-stu-id="7a49f-131">x</span></span>               | <span data-ttu-id="7a49f-132">x</span><span class="sxs-lookup"><span data-stu-id="7a49f-132">x</span></span>            |



 

<span data-ttu-id="7a49f-133">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="7a49f-133">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="7a49f-134">範例</span><span class="sxs-lookup"><span data-stu-id="7a49f-134">Example</span></span>

<span data-ttu-id="7a49f-135">以下是一些範例：</span><span class="sxs-lookup"><span data-stu-id="7a49f-135">Here are some examples:</span></span>


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a><span data-ttu-id="7a49f-136">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="7a49f-136">Minimum Shader Model</span></span>

<span data-ttu-id="7a49f-137">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="7a49f-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7a49f-138">著色器模型</span><span class="sxs-lookup"><span data-stu-id="7a49f-138">Shader Model</span></span>                                              | <span data-ttu-id="7a49f-139">支援</span><span class="sxs-lookup"><span data-stu-id="7a49f-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7a49f-140">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="7a49f-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7a49f-141">是</span><span class="sxs-lookup"><span data-stu-id="7a49f-141">yes</span></span>       |
| [<span data-ttu-id="7a49f-142">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="7a49f-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7a49f-143">是</span><span class="sxs-lookup"><span data-stu-id="7a49f-143">yes</span></span>       |
| [<span data-ttu-id="7a49f-144">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="7a49f-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7a49f-145">是</span><span class="sxs-lookup"><span data-stu-id="7a49f-145">yes</span></span>       |
| [<span data-ttu-id="7a49f-146">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7a49f-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7a49f-147">不可以</span><span class="sxs-lookup"><span data-stu-id="7a49f-147">no</span></span>        |
| [<span data-ttu-id="7a49f-148">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7a49f-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7a49f-149">不可以</span><span class="sxs-lookup"><span data-stu-id="7a49f-149">no</span></span>        |
| [<span data-ttu-id="7a49f-150">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7a49f-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7a49f-151">不可以</span><span class="sxs-lookup"><span data-stu-id="7a49f-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7a49f-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a49f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a49f-153">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7a49f-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





