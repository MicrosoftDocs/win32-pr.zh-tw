---
title: 取樣器類型
description: 使用下列語法來宣告取樣器狀態以及取樣器的比較狀態。
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- 取樣器類型 HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023502"
---
# <a name="sampler-type"></a><span data-ttu-id="86dd9-104">取樣器類型</span><span class="sxs-lookup"><span data-stu-id="86dd9-104">Sampler Type</span></span>

<span data-ttu-id="86dd9-105">使用下列語法來宣告取樣器狀態以及取樣器的比較狀態。</span><span class="sxs-lookup"><span data-stu-id="86dd9-105">Use the following syntax to declare sampler state as well as sampler-comparison state.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86dd9-106">Direct3D 9 與 Direct3D 10 和更新版本之間的差異：</span><span class="sxs-lookup"><span data-stu-id="86dd9-106">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="86dd9-107">以下是 Direct3D 9 中取樣器的語法。</span><span class="sxs-lookup"><span data-stu-id="86dd9-107">Here is the syntax for a sampler in Direct3D 9.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86dd9-108">取樣器<em>名稱</em>  =  <em>SamplerType</em>{材質 = <<em>texture_variable</em> > ;  [<em>state_name = state_value;</em>]  ... };</span><span class="sxs-lookup"><span data-stu-id="86dd9-108">sampler <em>Name</em> = <em>SamplerType</em>{   Texture = <<em>texture_variable</em>>;   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="86dd9-109">Direct3D 10 和更新版本中的取樣器語法會稍微變更，以支援材質物件和取樣器陣列。</span><span class="sxs-lookup"><span data-stu-id="86dd9-109">The syntax for a sampler in Direct3D 10 and later is changed slightly to support texture objects and sampler arrays.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86dd9-110"><em>SamplerType 名稱 [Index]</em>{[<em>state_name = state_value;</em>]  ... };</span><span class="sxs-lookup"><span data-stu-id="86dd9-110"><em>SamplerType Name[Index]</em>{   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a><span data-ttu-id="86dd9-111">參數</span><span class="sxs-lookup"><span data-stu-id="86dd9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86dd9-112"><span id="sampler"></span><span id="SAMPLER"></span>採樣</span><span class="sxs-lookup"><span data-stu-id="86dd9-112"><span id="sampler"></span><span id="SAMPLER"></span>sampler</span></span>
</dt> <dd>

<span data-ttu-id="86dd9-113">僅限 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="86dd9-113">Direct3D 9 only.</span></span> <span data-ttu-id="86dd9-114">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="86dd9-114">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="86dd9-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="86dd9-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="86dd9-116">可唯一識別取樣器變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="86dd9-116">ASCII string that uniquely identifies the sampler variable name.</span></span>

</dd> <dt>

<span data-ttu-id="86dd9-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[指數\]*</span><span class="sxs-lookup"><span data-stu-id="86dd9-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span></span>
</dt> <dd>

<span data-ttu-id="86dd9-118">僅限 Direct3D 10 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="86dd9-118">Direct3D 10 and later only.</span></span> <span data-ttu-id="86dd9-119">選擇性陣列大小;大於或等於1的正整數。</span><span class="sxs-lookup"><span data-stu-id="86dd9-119">Optional array size; a positive integer greater than or equal to 1.</span></span>

</dd> <dt>

<span data-ttu-id="86dd9-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span><span class="sxs-lookup"><span data-stu-id="86dd9-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span></span>
</dt> <dd>

<span data-ttu-id="86dd9-121">\[在 \] 取樣器型別中，也就是下列其中一項： *取樣* 器、 *sampler1D*、 *sampler2D*、 *sampler3D*、 *samplerCUBE*、 *取樣器 \_ 狀態*、 *SamplerState*。</span><span class="sxs-lookup"><span data-stu-id="86dd9-121">\[in\] The sampler type, which is one of the following: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler\_state*, *SamplerState*.</span></span>



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86dd9-122">Direct3D 9 與 Direct3D 10 和更新版本之間的差異：</span><span class="sxs-lookup"><span data-stu-id="86dd9-122">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="86dd9-123">Direct3D 10 和更新版本支援一個額外的取樣器類型： *SamplerComparisonState*。</span><span class="sxs-lookup"><span data-stu-id="86dd9-123">Direct3D 10 and later supports one additional sampler type: *SamplerComparisonState*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="86dd9-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*材質* = <*材質 \_ 變數*>;</span><span class="sxs-lookup"><span data-stu-id="86dd9-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*texture\_variable*>;</span></span>
</dt> <dd>

<span data-ttu-id="86dd9-125">僅限 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="86dd9-125">Direct3D 9 only.</span></span> <span data-ttu-id="86dd9-126">材質變數。</span><span class="sxs-lookup"><span data-stu-id="86dd9-126">A texture variable.</span></span> <span data-ttu-id="86dd9-127">左邊必須有 *材質* 關鍵字;變數名稱是在角括弧內運算式的右手邊。</span><span class="sxs-lookup"><span data-stu-id="86dd9-127">The *Texture* keyword is required on the left-hand side; the variable name belongs on the right-hand side of the expression within the angle brackets.</span></span>

</dd> <dt>

<span data-ttu-id="86dd9-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*狀態 \_ 名稱 = 狀態值 \_*</span><span class="sxs-lookup"><span data-stu-id="86dd9-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state\_name = state\_value*</span></span>
</dt> <dd>

<span data-ttu-id="86dd9-129">\[在 [ \] 選用狀態指派] (s) 。</span><span class="sxs-lookup"><span data-stu-id="86dd9-129">\[in\] Optional state assignment(s).</span></span> <span data-ttu-id="86dd9-130">指派的左邊是州/省，右邊則是 state 值。</span><span class="sxs-lookup"><span data-stu-id="86dd9-130">The left hand side of an assignment is a state name, the right hand side is the state value.</span></span> <span data-ttu-id="86dd9-131">所有狀態指派都必須出現在語句區塊中， (以大括弧) 。</span><span class="sxs-lookup"><span data-stu-id="86dd9-131">All state assignments must appear within a statement block (in curly brackets).</span></span> <span data-ttu-id="86dd9-132">每個語句都以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="86dd9-132">Each statement is separated with a semicolon.</span></span> <span data-ttu-id="86dd9-133">下表列出可能的狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="86dd9-133">The following table lists the possible state names.</span></span>


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



<span data-ttu-id="86dd9-134">每個運算式的右邊都是指派給每個狀態的值。</span><span class="sxs-lookup"><span data-stu-id="86dd9-134">The right side of each expression is the value assigned to each state.</span></span> <span data-ttu-id="86dd9-135">如需 Direct3D 11 可能狀態值的詳細資料，請參閱 [**D3D11 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="86dd9-135">See the [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) structure for the possible state values for Direct3D 11.</span></span> <span data-ttu-id="86dd9-136">狀態名稱與結構的成員之間有1對1的關聯性。</span><span class="sxs-lookup"><span data-stu-id="86dd9-136">There is a 1 to 1 relationship between the state names and the members of the structure.</span></span> <span data-ttu-id="86dd9-137">請參閱下列範例。</span><span class="sxs-lookup"><span data-stu-id="86dd9-137">See the following example.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86dd9-138">備註</span><span class="sxs-lookup"><span data-stu-id="86dd9-138">Remarks</span></span>

<span data-ttu-id="86dd9-139">當您執行效果時，取樣器狀態是數種類型的其中一種，您可能需要在管線中設定這些狀態，才能進行呈現。</span><span class="sxs-lookup"><span data-stu-id="86dd9-139">When you implement an effect, sampler state is one of several types of state that you might need to set up in the pipeline for rendering.</span></span> <span data-ttu-id="86dd9-140">如需您可以在效果中設定的所有可能狀態清單，請參閱：</span><span class="sxs-lookup"><span data-stu-id="86dd9-140">For a list of all the possible states that you can set in an effect, see:</span></span>

-   <span data-ttu-id="86dd9-141">Direct3D 10 使用 [狀態群組](/windows/desktop/direct3d10/d3d10-effect-states)。</span><span class="sxs-lookup"><span data-stu-id="86dd9-141">Direct3D 10 uses [state groups](/windows/desktop/direct3d10/d3d10-effect-states).</span></span>
-   <span data-ttu-id="86dd9-142">Direct3D 9 使用個別的 [狀態](/windows/desktop/direct3d9/effect-states)。</span><span class="sxs-lookup"><span data-stu-id="86dd9-142">Direct3D 9 uses individual [states](/windows/desktop/direct3d9/effect-states).</span></span>

## <a name="example"></a><span data-ttu-id="86dd9-143">範例</span><span class="sxs-lookup"><span data-stu-id="86dd9-143">Example</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86dd9-144">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="86dd9-144">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="86dd9-145">以下是來自 <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL 範例</a>的 Direct3D 9 取樣器的部分範例。</span><span class="sxs-lookup"><span data-stu-id="86dd9-145">Here is a partial example of a Direct3D 9 sampler from <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL Sample</a>.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="86dd9-146">以下是來自 <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 範例</a>的 Direct3D 10 取樣器的部分範例。</span><span class="sxs-lookup"><span data-stu-id="86dd9-146">Here is a partial example of a Direct3D 10 sampler from <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample</a>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="86dd9-147">以下是宣告取樣器比較狀態，以及在 Direct3D 10 中呼叫比較取樣器的部分範例。</span><span class="sxs-lookup"><span data-stu-id="86dd9-147">Here is a partial example of declaring sampler-comparison state, and calling a comparison sampler in Direct3D 10.</span></span>


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a><span data-ttu-id="86dd9-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86dd9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86dd9-149"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="86dd9-149">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

