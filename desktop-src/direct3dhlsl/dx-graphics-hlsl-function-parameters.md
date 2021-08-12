---
title: 函數引數
description: 函數接受一或多個輸入引數;使用下列語法來宣告每個引數。
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a2f2fdb656917ccf9dc57f06713fe01d77398d35776ac0c479b7d088281bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514761"
---
# <a name="function-arguments"></a>函數引數

函數接受一或多個輸入引數;使用下列語法來宣告每個引數。



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[InputModifier \] 類型名稱 \[ ：語義 \] \[ InterpolationModifier \] \[ = 初始化運算式\]** |



 

\[修飾詞 \] 型別名稱 \[ ：語義 \] \[ ：插補修飾詞 \] \[ = 初始化運算式 (s) \]

如果有多個函數引數，則會以逗號分隔。

## <a name="parameters"></a>參數



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong><br/></td>
<td>將引數識別為輸入、輸出或兩者的選擇性字詞。<br/> 
<table>
<tbody>
<tr class="odd">
<td>值</td>
<td>描述</td>
</tr>
<tr class="even">
<td><strong>in</strong></td>
<td>僅輸入</td>
</tr>
<tr class="odd">
<td><strong>inout</strong></td>
<td>輸入和輸出</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>僅輸出</td>
</tr>
<tr class="odd">
<td><strong>uniform</strong></td>
<td>只輸入常數資料</td>
</tr>
</tbody>
</table>

<p> </p>
<p>參數一律會以傳值方式傳遞。 中的表示在函式開始之前，應該從呼叫應用程式複製參數的值。 out 表示應該複製參數的最後一個值，並在函式傳回時將其傳回給呼叫的應用程式。 inout 是指定兩者的縮寫。</p>
<p>統一值來自常數暫存器;每個頂點著色器或圖元著色器調用都會看到相同的統一變數初始值。 全域變數會被視為一致的宣告。 針對非最上層函式，統一與 <strong>中</strong>的同義。 如果未指定參數使用方式，則會假設參數使用 <strong>方式在中</strong>。</p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>類型</strong></p></td>
<td><p>引數類型;可以是任何有效的 HLSL <a href="dx-graphics-hlsl-data-types.md">型</a>別。</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>名字</strong></p></td>
<td><p>能唯一識別著色器函式名稱的 ASCII 字串。</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>語義</strong></p></td>
<td><p>選擇性字串，可識別資料的預期使用方式 (請參閱 <a href="dx-graphics-hlsl-semantics.md"> (DIRECTX HLSL) </a>) 的語義。</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></p></td>
<td><p>選擇性的 <a href="dx-graphics-hlsl-struct.md">插補修飾</a> 詞，可讓著色器判斷插補的方法。 函式引數上的插補修飾元只適用于做為圖元著色器函式輸入的引數。</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>項</strong></p></td>
<td><p>初始化的選擇性值;需要多個值，才能初始化多元件資料類型。</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

函式引數會列在函式宣告中以逗號分隔的引數清單中。 如同在 C 函數中，每個引數都必須宣告參數名稱和類型;HLSL 函式的引數可選擇性地包含語義、初始值和圖元著色器輸入，可包含插補類型。

函數引數的 *型* 別可以是結構，其中可能包含每個成員的插補修飾元。 如果函式引數也具有插補修飾詞，則函式引數修飾詞會覆寫在型別中宣告的插補修飾元

## <a name="examples"></a>範例

此範例 (從 [BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) 說明頂點著色器函式的統一和非統一輸入。


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



此範例 (從 [ContentStreaming 範例](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) 使用輸入結構將引數傳遞給圖元著色器函式。


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL) 的函式 ](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





