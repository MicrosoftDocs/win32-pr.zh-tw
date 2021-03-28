---
title: 'dcl_sampler (sm4-asm) '
description: 'dcl \_ 取樣器 (sm4-asm) '
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383061"
---
# <a name="dcl_sampler-sm4---asm"></a><span data-ttu-id="5d66e-103">dcl \_ 取樣器 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="5d66e-103">dcl\_sampler (sm4 - asm)</span></span>

<span data-ttu-id="5d66e-104">宣告取樣器暫存器。</span><span class="sxs-lookup"><span data-stu-id="5d66e-104">Declares a sampler register.</span></span>



| <span data-ttu-id="5d66e-105">dcl \_ 取樣器 sN，模式</span><span class="sxs-lookup"><span data-stu-id="5d66e-105">dcl\_sampler sN, mode</span></span> |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d66e-106">項目</span><span class="sxs-lookup"><span data-stu-id="5d66e-106">Item</span></span></th>
<th><span data-ttu-id="5d66e-107">描述</span><span class="sxs-lookup"><span data-stu-id="5d66e-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d66e-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span><span class="sxs-lookup"><span data-stu-id="5d66e-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span></span><br/></td>
<td><span data-ttu-id="5d66e-109">在取樣器暫存器，其中 <em>N</em> 是表示註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="5d66e-109">[in] A sampler register, where <em>N</em> is an integer that denotes the register number.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d66e-110"><span id="mode"></span><span id="MODE"></span><em>模式</em></span><span class="sxs-lookup"><span data-stu-id="5d66e-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span></span><br/></td>
<td><span data-ttu-id="5d66e-111">在取樣器模式，限制 <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) 的成員中所列的取樣器狀態 (。</span><span class="sxs-lookup"><span data-stu-id="5d66e-111">[in] A sampler mode, which constrains which sampler states (listed in the members of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) are honored.</span></span> <span data-ttu-id="5d66e-112">下表列出模式和狀態。</span><span class="sxs-lookup"><span data-stu-id="5d66e-112">The modes and states are listed in the following table.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5d66e-113">模式</span><span class="sxs-lookup"><span data-stu-id="5d66e-113">Mode</span></span></th>
<th><span data-ttu-id="5d66e-114">已接受取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="5d66e-114">Sampler States Honored</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d66e-115">預設</span><span class="sxs-lookup"><span data-stu-id="5d66e-115">default</span></span></td>
<td><span data-ttu-id="5d66e-116"><em>篩選</em> (可能不會使用 _COMPARISON 或 _TEXT 值) 、 <em>AddressU/V/W</em>、 <em>MinLOD/MaxLOD</em>、 <em>MipLODBias</em>、 <em>MaxAnisotropy</em>、加 <em>邊框 [4]</em></span><span class="sxs-lookup"><span data-stu-id="5d66e-116"><em>Filter</em> (may not use the _COMPARISON or _TEXT values), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d66e-117">比較</span><span class="sxs-lookup"><span data-stu-id="5d66e-117">comparison</span></span></td>
<td><span data-ttu-id="5d66e-118"><em>Filter</em>、 <em>ComparisonFunction</em>、 <em>AddressU/V/W</em>、 <em>MinLOD、MaxLOD</em>、 <em>MipLODBias</em>、 <em>MaxAnisotropy</em>、加 <em>邊框 [4]</em></span><span class="sxs-lookup"><span data-stu-id="5d66e-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d66e-119">單</span><span class="sxs-lookup"><span data-stu-id="5d66e-119">mono</span></span></td>
<td><span data-ttu-id="5d66e-120"><em>篩選</em> (必須是其中一個 _TEXT 值) 、 <em>MonoFilterWidth</em>、 <em>MonoFilterHeight</em> (這兩個狀態為全域裝置狀態) 、 <em>MinLOD</em>、 <em>MipLODBias</em>、 <em>MaxAnisotropy</em></span><span class="sxs-lookup"><span data-stu-id="5d66e-120"><em>Filter</em> (must be one of the _TEXT values), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (these two states are global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5d66e-121">此模式會限制可使用的範例指令;下表列出每個模式都支援的材質物件方法。</span><span class="sxs-lookup"><span data-stu-id="5d66e-121">The mode restricts the sample instructions that can be used; this table lists the texture-object methods that are supported for each mode.</span></span>



| <span data-ttu-id="5d66e-122">在此模式中操作的取樣器</span><span class="sxs-lookup"><span data-stu-id="5d66e-122">A Sampler Operating in this Mode</span></span> | <span data-ttu-id="5d66e-123">可以使用這些 Texture-Object 方法</span><span class="sxs-lookup"><span data-stu-id="5d66e-123">Can Use these Texture-Object Methods</span></span>                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d66e-124">預設</span><span class="sxs-lookup"><span data-stu-id="5d66e-124">default</span></span>                          | <span data-ttu-id="5d66e-125">[Sample](dx-graphics-hlsl-to-sample.md)、 [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)、 [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span><span class="sxs-lookup"><span data-stu-id="5d66e-125">[Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span></span> |
| <span data-ttu-id="5d66e-126">比較</span><span class="sxs-lookup"><span data-stu-id="5d66e-126">comparison</span></span>                       | <span data-ttu-id="5d66e-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md)、 [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span><span class="sxs-lookup"><span data-stu-id="5d66e-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span></span>                               |
| <span data-ttu-id="5d66e-128">單</span><span class="sxs-lookup"><span data-stu-id="5d66e-128">mono</span></span>                             | [<span data-ttu-id="5d66e-129">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="5d66e-129">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

<span data-ttu-id="5d66e-130">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="5d66e-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5d66e-131">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="5d66e-131">Vertex Shader</span></span> | <span data-ttu-id="5d66e-132">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="5d66e-132">Geometry Shader</span></span> | <span data-ttu-id="5d66e-133">像素著色器</span><span class="sxs-lookup"><span data-stu-id="5d66e-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5d66e-134">x</span><span class="sxs-lookup"><span data-stu-id="5d66e-134">x</span></span>             | <span data-ttu-id="5d66e-135">x</span><span class="sxs-lookup"><span data-stu-id="5d66e-135">x</span></span>               | <span data-ttu-id="5d66e-136">x\*</span><span class="sxs-lookup"><span data-stu-id="5d66e-136">x\*</span></span>          |



 

<span data-ttu-id="5d66e-137">\* -只有在圖元著色器中才支援使用 mono 模式的取樣器。</span><span class="sxs-lookup"><span data-stu-id="5d66e-137">\* - Using a sampler in mono mode is supported only in a pixel shader.</span></span>

<span data-ttu-id="5d66e-138">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="5d66e-138">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="5d66e-139">範例</span><span class="sxs-lookup"><span data-stu-id="5d66e-139">Example</span></span>

<span data-ttu-id="5d66e-140">範例如下。</span><span class="sxs-lookup"><span data-stu-id="5d66e-140">Here is an example.</span></span>


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a><span data-ttu-id="5d66e-141">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5d66e-141">Minimum Shader Model</span></span>

<span data-ttu-id="5d66e-142">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="5d66e-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5d66e-143">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5d66e-143">Shader Model</span></span>                                              | <span data-ttu-id="5d66e-144">支援</span><span class="sxs-lookup"><span data-stu-id="5d66e-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5d66e-145">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5d66e-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5d66e-146">是</span><span class="sxs-lookup"><span data-stu-id="5d66e-146">yes</span></span>       |
| [<span data-ttu-id="5d66e-147">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="5d66e-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5d66e-148">是</span><span class="sxs-lookup"><span data-stu-id="5d66e-148">yes</span></span>       |
| [<span data-ttu-id="5d66e-149">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5d66e-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5d66e-150">是</span><span class="sxs-lookup"><span data-stu-id="5d66e-150">yes</span></span>       |
| [<span data-ttu-id="5d66e-151">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5d66e-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5d66e-152">不可以</span><span class="sxs-lookup"><span data-stu-id="5d66e-152">no</span></span>        |
| [<span data-ttu-id="5d66e-153">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5d66e-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5d66e-154">不可以</span><span class="sxs-lookup"><span data-stu-id="5d66e-154">no</span></span>        |
| [<span data-ttu-id="5d66e-155">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5d66e-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5d66e-156">不可以</span><span class="sxs-lookup"><span data-stu-id="5d66e-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5d66e-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d66e-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d66e-158">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5d66e-158">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

