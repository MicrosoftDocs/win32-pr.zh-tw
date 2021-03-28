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
# <a name="sampler-type"></a>取樣器類型

使用下列語法來宣告取樣器狀態以及取樣器的比較狀態。



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 10 和更新版本之間的差異：<br/> 以下是 Direct3D 9 中取樣器的語法。<br/> 
<table>
<tbody>
<tr class="odd">
<td>取樣器<em>名稱</em>  =  <em>SamplerType</em>{材質 = <<em>texture_variable</em> > ;  [<em>state_name = state_value;</em>]  ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Direct3D 10 和更新版本中的取樣器語法會稍微變更，以支援材質物件和取樣器陣列。</p>

<table>
<tbody>
<tr class="odd">
<td><em>SamplerType 名稱 [Index]</em>{[<em>state_name = state_value;</em>]  ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>採樣
</dt> <dd>

僅限 Direct3D 9。 必要關鍵字。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

可唯一識別取樣器變數名稱的 ASCII 字串。

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[指數\]*
</dt> <dd>

僅限 Direct3D 10 和更新版本。 選擇性陣列大小;大於或等於1的正整數。

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*
</dt> <dd>

\[在 \] 取樣器型別中，也就是下列其中一項： *取樣* 器、 *sampler1D*、 *sampler2D*、 *sampler3D*、 *samplerCUBE*、 *取樣器 \_ 狀態*、 *SamplerState*。



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 10 和更新版本之間的差異：<br/> Direct3D 10 和更新版本支援一個額外的取樣器類型： *SamplerComparisonState*。<br/> |



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*材質* = <*材質 \_ 變數*>;
</dt> <dd>

僅限 Direct3D 9。 材質變數。 左邊必須有 *材質* 關鍵字;變數名稱是在角括弧內運算式的右手邊。

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*狀態 \_ 名稱 = 狀態值 \_*
</dt> <dd>

\[在 [ \] 選用狀態指派] (s) 。 指派的左邊是州/省，右邊則是 state 值。 所有狀態指派都必須出現在語句區塊中， (以大括弧) 。 每個語句都以分號分隔。 下表列出可能的狀態名稱。


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



每個運算式的右邊都是指派給每個狀態的值。 如需 Direct3D 11 可能狀態值的詳細資料，請參閱 [**D3D11 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) 結構。 狀態名稱與結構的成員之間有1對1的關聯性。 請參閱下列範例。

</dd> </dl>

## <a name="remarks"></a>備註

當您執行效果時，取樣器狀態是數種類型的其中一種，您可能需要在管線中設定這些狀態，才能進行呈現。 如需您可以在效果中設定的所有可能狀態清單，請參閱：

-   Direct3D 10 使用 [狀態群組](/windows/desktop/direct3d10/d3d10-effect-states)。
-   Direct3D 9 使用個別的 [狀態](/windows/desktop/direct3d9/effect-states)。

## <a name="example"></a>範例



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 10 之間的差異：<br/> 以下是來自 <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL 範例</a>的 Direct3D 9 取樣器的部分範例。<br/> <span data-codelanguage=""></span>
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

<p>以下是來自 <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 範例</a>的 Direct3D 10 取樣器的部分範例。</p>
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



 

以下是宣告取樣器比較狀態，以及在 Direct3D 10 中呼叫比較取樣器的部分範例。


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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

