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
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374295"
---
# <a name="function-arguments"></a><span data-ttu-id="5ffd9-103">函數引數</span><span class="sxs-lookup"><span data-stu-id="5ffd9-103">Function Arguments</span></span>

<span data-ttu-id="5ffd9-104">函數接受一或多個輸入引數;使用下列語法來宣告每個引數。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-104">A function takes one or more input arguments; use the following syntax to declare each argument.</span></span>



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffd9-105">**\[InputModifier \] 類型名稱 \[ ：語義 \] \[ InterpolationModifier \] \[ = 初始化運算式\]**</span><span class="sxs-lookup"><span data-stu-id="5ffd9-105">**\[InputModifier\] Type Name \[: Semantic\] \[InterpolationModifier\] \[= Initializers\]**</span></span> |



 

<span data-ttu-id="5ffd9-106">\[修飾詞 \] 型別名稱 \[ ：語義 \] \[ ：插補修飾詞 \] \[ = 初始化運算式 (s) \]</span><span class="sxs-lookup"><span data-stu-id="5ffd9-106">\[Modifier\] Type Name \[: Semantic\] \[: Interpolation Modifier\] \[= Initializer(s)\]</span></span>

<span data-ttu-id="5ffd9-107">如果有多個函數引數，則會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-107">If there are multiple function arguments, they are separated by commas.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ffd9-108">參數</span><span class="sxs-lookup"><span data-stu-id="5ffd9-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ffd9-109">項目</span><span class="sxs-lookup"><span data-stu-id="5ffd9-109">Item</span></span></th>
<th><span data-ttu-id="5ffd9-110">描述</span><span class="sxs-lookup"><span data-stu-id="5ffd9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ffd9-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span></span><br/></td>
<td><span data-ttu-id="5ffd9-112">將引數識別為輸入、輸出或兩者的選擇性字詞。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-112">Optional term that identifies an argument as an input, an output, or both.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ffd9-113">值</span><span class="sxs-lookup"><span data-stu-id="5ffd9-113">Value</span></span></td>
<td><span data-ttu-id="5ffd9-114">描述</span><span class="sxs-lookup"><span data-stu-id="5ffd9-114">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ffd9-115"><strong>in</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-115"><strong>in</strong></span></span></td>
<td><span data-ttu-id="5ffd9-116">僅輸入</span><span class="sxs-lookup"><span data-stu-id="5ffd9-116">Input only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ffd9-117"><strong>inout</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-117"><strong>inout</strong></span></span></td>
<td><span data-ttu-id="5ffd9-118">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="5ffd9-118">Input and an output</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ffd9-119"><strong>out</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-119"><strong>out</strong></span></span></td>
<td><span data-ttu-id="5ffd9-120">僅輸出</span><span class="sxs-lookup"><span data-stu-id="5ffd9-120">Output only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ffd9-121"><strong>均勻</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-121"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="5ffd9-122">只輸入常數資料</span><span class="sxs-lookup"><span data-stu-id="5ffd9-122">Input only constant data</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="5ffd9-123">參數一律會以傳值方式傳遞。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-123">Parameters are always passed by value.</span></span> <span data-ttu-id="5ffd9-124">中的表示在函式開始之前，應該從呼叫應用程式複製參數的值。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-124">in indicates that the value of the parameter should be copied in from the calling application before the function begins.</span></span> <span data-ttu-id="5ffd9-125">out 表示應該複製參數的最後一個值，並在函式傳回時將其傳回給呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-125">out indicates that the last value of the parameter should be copied out, and returned to the calling application when the function returns.</span></span> <span data-ttu-id="5ffd9-126">inout 是指定兩者的縮寫。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-126">inout is a shorthand for specifying both.</span></span></p>
<p><span data-ttu-id="5ffd9-127">統一值來自常數暫存器;每個頂點著色器或圖元著色器調用都會看到相同的統一變數初始值。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-127">A uniform value comes from a constant register; each vertex shader or pixel shader invocation see the same initial value for a uniform variable.</span></span> <span data-ttu-id="5ffd9-128">全域變數會被視為一致的宣告。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-128">Global variables are treated as if they are declared uniform.</span></span> <span data-ttu-id="5ffd9-129">針對非最上層函式，統一與 <strong>中</strong>的同義。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-129">For non-top-level functions, uniform is synonymous with <strong>in</strong>.</span></span> <span data-ttu-id="5ffd9-130">如果未指定參數使用方式，則會假設參數使用 <strong>方式在中</strong>。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-130">If no parameter usage is specified, the parameter usage is assumed to be <strong>in</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ffd9-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>類型</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5ffd9-132">引數類型;可以是任何有效的 HLSL <a href="dx-graphics-hlsl-data-types.md">型</a>別。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-132">The argument type; can be any valid HLSL <a href="dx-graphics-hlsl-data-types.md">type</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ffd9-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>名字</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5ffd9-134">能唯一識別著色器函式名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-134">An ASCII string that uniquely identifies the name of the shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ffd9-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>語義</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantic</strong></span></span></p></td>
<td><p><span data-ttu-id="5ffd9-136">選擇性字串，可識別資料的預期使用方式 (請參閱 <a href="dx-graphics-hlsl-semantics.md"> (DIRECTX HLSL) </a>) 的語義。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-136">Optional string that identifies the intended usage of the data (see <a href="dx-graphics-hlsl-semantics.md">Semantics (DirectX HLSL)</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ffd9-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span></span></p></td>
<td><p><span data-ttu-id="5ffd9-138">選擇性的 <a href="dx-graphics-hlsl-struct.md">插補修飾</a> 詞，可讓著色器判斷插補的方法。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-138">Optional <a href="dx-graphics-hlsl-struct.md">interpolation modifier</a> which allows a shader to determine the method of interpolation.</span></span> <span data-ttu-id="5ffd9-139">函式引數上的插補修飾元只適用于做為圖元著色器函式輸入的引數。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-139">An interpolation modifier on a function argument only applies to an argument used as an input to a pixel shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ffd9-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>項</strong></span><span class="sxs-lookup"><span data-stu-id="5ffd9-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initializers</strong></span></span></p></td>
<td><p><span data-ttu-id="5ffd9-141">初始化的選擇性值;需要多個值，才能初始化多元件資料類型。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-141">Optional values for initialization; multiple values are required to initialize multi-component data types.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="5ffd9-142">備註</span><span class="sxs-lookup"><span data-stu-id="5ffd9-142">Remarks</span></span>

<span data-ttu-id="5ffd9-143">函式引數會列在函式宣告中以逗號分隔的引數清單中。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-143">Function arguments are listed in a comma-separated argument list in a function declaration.</span></span> <span data-ttu-id="5ffd9-144">如同在 C 函數中，每個引數都必須宣告參數名稱和類型;HLSL 函式的引數可選擇性地包含語義、初始值和圖元著色器輸入，可包含插補類型。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-144">As in C functions, each argument must have a parameter name and type declared; an argument to an HLSL function optionally can include a semantic, an initial value, and a pixel shader input can include an interpolation type.</span></span>

<span data-ttu-id="5ffd9-145">函數引數的 *型* 別可以是結構，其中可能包含每個成員的插補修飾元。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-145">The *Type* of a function argument could be a structure, which could include a per-member interpolation modifier.</span></span> <span data-ttu-id="5ffd9-146">如果函式引數也具有插補修飾詞，則函式引數修飾詞會覆寫在型別中宣告的插補修飾元</span><span class="sxs-lookup"><span data-stu-id="5ffd9-146">If the function argument also has an interpolation modifier, the function argument modifier overrides interpolation modifiers declared within the Type.</span></span>

## <a name="examples"></a><span data-ttu-id="5ffd9-147">範例</span><span class="sxs-lookup"><span data-stu-id="5ffd9-147">Examples</span></span>

<span data-ttu-id="5ffd9-148">此範例 (從 [BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) 說明頂點著色器函式的統一和非統一輸入。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-148">This example (from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustrates uniform and non-uniform inputs to a vertex shader function.</span></span>


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



<span data-ttu-id="5ffd9-149">此範例 (從 [ContentStreaming 範例](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) 使用輸入結構將引數傳遞給圖元著色器函式。</span><span class="sxs-lookup"><span data-stu-id="5ffd9-149">This example (from the [ContentStreaming Sample](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) uses an input structure to pass arguments to a pixel shader function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5ffd9-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ffd9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ffd9-151"> (DirectX HLSL) 的函式 </span><span class="sxs-lookup"><span data-stu-id="5ffd9-151">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





