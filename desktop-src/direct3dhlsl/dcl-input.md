---
title: 'dcl_input (sm4-asm) '
description: 'dcl \_ 輸入 (sm4-asm) '
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990838"
---
# <a name="dcl_input-sm4---asm"></a><span data-ttu-id="6a4ed-103">dcl \_ 輸入 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="6a4ed-103">dcl\_input (sm4 - asm)</span></span>

<span data-ttu-id="6a4ed-104">宣告著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-104">Declares a shader-input register.</span></span>



| <span data-ttu-id="6a4ed-105">dcl \_ 輸入 v *N \[ . mask \] \[ ，interpolationMode \]*</span><span class="sxs-lookup"><span data-stu-id="6a4ed-105">dcl\_input v *N\[.mask\]\[, interpolationMode\]*</span></span> |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a4ed-106">項目</span><span class="sxs-lookup"><span data-stu-id="6a4ed-106">Item</span></span></th>
<th><span data-ttu-id="6a4ed-107">描述</span><span class="sxs-lookup"><span data-stu-id="6a4ed-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a4ed-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [mask]</em></span><span class="sxs-lookup"><span data-stu-id="6a4ed-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="6a4ed-109">在頂點資料註冊。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="6a4ed-110"><em>N</em> 是識別註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="6a4ed-111"><em>[mask]</em> 是選擇性的元件遮罩 ( xyzw) ，可指定要使用的註冊元件。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a4ed-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="6a4ed-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="6a4ed-113">[in] 選用。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-113">[in] Optional.</span></span> <span data-ttu-id="6a4ed-114">插補模式，僅適用于圖元著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-114">The interpolation mode, which is only honored on pixel shader input registers.</span></span> <span data-ttu-id="6a4ed-115">它可能是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="6a4ed-115">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="6a4ed-116">常數-不在暫存器值之間插補。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-116">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="6a4ed-117">線性-在註冊值之間以線性方式插補。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-117">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="6a4ed-118">linearCentroid-與線性相同，但在取樣時距心壓制。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-118">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="6a4ed-119">linearNoperspective-與線性相同，但沒有透視校正。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-119">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="6a4ed-120">linearNoperspectiveCentroid-與線性相同，距心壓制，在取樣時，不會進行透視校正。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-120">linearNoperspectiveCentroid - same as linear, centroid clamped when multisampling, no perspective correction.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a><span data-ttu-id="6a4ed-121">插補附注</span><span class="sxs-lookup"><span data-stu-id="6a4ed-121">Interpolation Notes</span></span>

<span data-ttu-id="6a4ed-122">依預設，在執行效能高效能消除鋸齒時，會從圖元中心內插上頂點屬性。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-122">By default, vertex attributes are interpolated from a pixel center when performing multisample antialiasing.</span></span> <span data-ttu-id="6a4ed-123">如果未涵蓋圖元中心，則會在插補之前將屬性推斷到圖元中心。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-123">If a pixel center is not covered, an attribute is extrapolated to a pixel center before interpolation.</span></span>

<span data-ttu-id="6a4ed-124">針對未完全涵蓋的圖元或未涵蓋圖元中心的屬性，您可以指定距心取樣，以強制取樣在圖元涵蓋區域內的某處發生。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-124">For a pixel that is not fully covered or an attribute that does not cover a pixel center, you can specify centroid sampling which forces sampling to occur somewhere within the covered area of the pixel.</span></span> <span data-ttu-id="6a4ed-125">因為範例遮罩 (如果在計算距心之前套用了使用的) ，所以不能將範例遮罩所遮罩的任何範例位置選擇為距心位置。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-125">Because a sample mask (if used) is applied before the centroid is computed, any sample location masked out by the sample mask cannot be chosen as a centroid location.</span></span>

<span data-ttu-id="6a4ed-126">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6a4ed-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a4ed-127">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="6a4ed-127">Vertex Shader</span></span> | <span data-ttu-id="6a4ed-128">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="6a4ed-128">Geometry Shader</span></span> | <span data-ttu-id="6a4ed-129">像素著色器</span><span class="sxs-lookup"><span data-stu-id="6a4ed-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6a4ed-130">x</span><span class="sxs-lookup"><span data-stu-id="6a4ed-130">x</span></span>             | <span data-ttu-id="6a4ed-131">x</span><span class="sxs-lookup"><span data-stu-id="6a4ed-131">x</span></span>               | <span data-ttu-id="6a4ed-132">x</span><span class="sxs-lookup"><span data-stu-id="6a4ed-132">x</span></span>            |



 

<span data-ttu-id="6a4ed-133">若要將輸入識別為系統值，請使用 [dcl \_ 輸入 \_ sv (sm4-asm) ](dcl-input-sv.md)。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-133">To identify the input as a system value, use [dcl\_input\_sv (sm4 - asm)](dcl-input-sv.md).</span></span>

<span data-ttu-id="6a4ed-134">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-134">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="6a4ed-135">範例</span><span class="sxs-lookup"><span data-stu-id="6a4ed-135">Example</span></span>

<span data-ttu-id="6a4ed-136">以下是一些範例。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-136">Here are some examples.</span></span>


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a><span data-ttu-id="6a4ed-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a4ed-137">Minimum Shader Model</span></span>

<span data-ttu-id="6a4ed-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6a4ed-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a4ed-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a4ed-139">Shader Model</span></span>                                              | <span data-ttu-id="6a4ed-140">支援</span><span class="sxs-lookup"><span data-stu-id="6a4ed-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a4ed-141">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6a4ed-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a4ed-142">是</span><span class="sxs-lookup"><span data-stu-id="6a4ed-142">yes</span></span>       |
| [<span data-ttu-id="6a4ed-143">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6a4ed-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a4ed-144">是</span><span class="sxs-lookup"><span data-stu-id="6a4ed-144">yes</span></span>       |
| [<span data-ttu-id="6a4ed-145">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6a4ed-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a4ed-146">是</span><span class="sxs-lookup"><span data-stu-id="6a4ed-146">yes</span></span>       |
| [<span data-ttu-id="6a4ed-147">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a4ed-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a4ed-148">不可以</span><span class="sxs-lookup"><span data-stu-id="6a4ed-148">no</span></span>        |
| [<span data-ttu-id="6a4ed-149">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a4ed-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a4ed-150">不可以</span><span class="sxs-lookup"><span data-stu-id="6a4ed-150">no</span></span>        |
| [<span data-ttu-id="6a4ed-151">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a4ed-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a4ed-152">不可以</span><span class="sxs-lookup"><span data-stu-id="6a4ed-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a4ed-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a4ed-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a4ed-154">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a4ed-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





