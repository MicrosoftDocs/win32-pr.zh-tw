---
title: 結構類型
description: 結構類型
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- 結構類型 HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89435e9c8757d2e732bc6237b02a508d3af4b4db
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119093"
---
# <a name="struct-type"></a><span data-ttu-id="2f3de-104">結構類型</span><span class="sxs-lookup"><span data-stu-id="2f3de-104">Struct Type</span></span>

<span data-ttu-id="2f3de-105">使用下列語法，使用 HLSL 宣告結構。</span><span class="sxs-lookup"><span data-stu-id="2f3de-105">Use the following syntax to declare a structure using HLSL.</span></span>

<span data-ttu-id="2f3de-106">結構 *名稱*{ \[ *InterpolationModifier* \] *類型* \[ *R* x *C* \] *成員* 名稱;    ... };</span><span class="sxs-lookup"><span data-stu-id="2f3de-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="2f3de-107">參數</span><span class="sxs-lookup"><span data-stu-id="2f3de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f3de-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="2f3de-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="2f3de-109">可唯一識別結構名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="2f3de-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="2f3de-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span><span class="sxs-lookup"><span data-stu-id="2f3de-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3de-111">指定插補類型的選擇性修飾詞。</span><span class="sxs-lookup"><span data-stu-id="2f3de-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="2f3de-112">如需詳細資訊，請參閱 [備註](#remarks) 。</span><span class="sxs-lookup"><span data-stu-id="2f3de-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="2f3de-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*類型* \[*R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="2f3de-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3de-114">具有選擇性資料列 (*R*) x 資料行 (*C*) 陣列大小的成員類型。</span><span class="sxs-lookup"><span data-stu-id="2f3de-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="2f3de-115">結構至少包含一個元素;如果它包含一個以上的元素，則這些元素都是相同的類型。</span><span class="sxs-lookup"><span data-stu-id="2f3de-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="2f3de-116">資料列和資料行的數目是1到4（含）之間不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="2f3de-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="2f3de-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*名*</span><span class="sxs-lookup"><span data-stu-id="2f3de-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="2f3de-118">可唯一識別成員名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="2f3de-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f3de-119">備註</span><span class="sxs-lookup"><span data-stu-id="2f3de-119">Remarks</span></span>

<span data-ttu-id="2f3de-120">可以在任何結構成員或圖元著色器函式的引數上指定插補修飾元。</span><span class="sxs-lookup"><span data-stu-id="2f3de-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="2f3de-121">如果兩個位置都出現修飾詞， (圖元著色器引數修飾詞的外部修飾詞) overrules 結構修飾詞)  (的內部修飾詞。</span><span class="sxs-lookup"><span data-stu-id="2f3de-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="2f3de-122">編譯著色器或效果時，著色器編譯器會根據 [HLSL 封裝規則](dx-graphics-hlsl-packing-rules.md)來封裝結構成員。</span><span class="sxs-lookup"><span data-stu-id="2f3de-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="2f3de-123">著色器模型4中引進的插補修飾元</span><span class="sxs-lookup"><span data-stu-id="2f3de-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="2f3de-124">用於圖元著色器輸入的頂點著色器輸出會以線性方式插補，以在點陣化期間取得每圖元值。</span><span class="sxs-lookup"><span data-stu-id="2f3de-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="2f3de-125">若要設定插補的方法，請使用 [著色器模型 4](dx-graphics-hlsl-sm4.md) 或更新版本中支援的下列任何值。</span><span class="sxs-lookup"><span data-stu-id="2f3de-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="2f3de-126">任何未當做圖元著色器輸入使用的頂點著色器輸出，都會忽略修飾詞。</span><span class="sxs-lookup"><span data-stu-id="2f3de-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="2f3de-127">插補修飾元</span><span class="sxs-lookup"><span data-stu-id="2f3de-127">Interpolation Modifier</span></span> | <span data-ttu-id="2f3de-128">描述</span><span class="sxs-lookup"><span data-stu-id="2f3de-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3de-129">**線性**</span><span class="sxs-lookup"><span data-stu-id="2f3de-129">**linear**</span></span>             | <span data-ttu-id="2f3de-130">在著色器輸入之間插補;如果未指定插補修飾元，則 **線性** 是預設值。</span><span class="sxs-lookup"><span data-stu-id="2f3de-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2f3de-131">**質心**</span><span class="sxs-lookup"><span data-stu-id="2f3de-131">**centroid**</span></span>           | <span data-ttu-id="2f3de-132">在圖元的涵蓋區域內的某個位置內插補點 (這可能需要圖元中心) 的推斷端點。</span><span class="sxs-lookup"><span data-stu-id="2f3de-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="2f3de-133">如果圖元部分涵蓋 (，距心取樣可能會改善消除鋸齒，即使圖元中心未涵蓋) 也是如此。</span><span class="sxs-lookup"><span data-stu-id="2f3de-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="2f3de-134">**距心** 修飾詞必須與 **線性** 或 **noperspective** 修飾詞結合。</span><span class="sxs-lookup"><span data-stu-id="2f3de-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2f3de-135">**nointerpolation**</span><span class="sxs-lookup"><span data-stu-id="2f3de-135">**nointerpolation**</span></span>    | <span data-ttu-id="2f3de-136">不要插補。</span><span class="sxs-lookup"><span data-stu-id="2f3de-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="2f3de-137">**noperspective**</span><span class="sxs-lookup"><span data-stu-id="2f3de-137">**noperspective**</span></span>      | <span data-ttu-id="2f3de-138">請勿在插補期間執行角度修正。</span><span class="sxs-lookup"><span data-stu-id="2f3de-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="2f3de-139">**Noperspective** 修飾詞可以與 **距心** 修飾詞結合。</span><span class="sxs-lookup"><span data-stu-id="2f3de-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2f3de-140">**樣品**</span><span class="sxs-lookup"><span data-stu-id="2f3de-140">**sample**</span></span>             | <span data-ttu-id="2f3de-141">**適用于著色器模型4.1 和更新版本** 在樣本位置插入，而不是圖元中心。</span><span class="sxs-lookup"><span data-stu-id="2f3de-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="2f3de-142">這會讓圖元著色器執行每個樣本，而不是每個圖元。</span><span class="sxs-lookup"><span data-stu-id="2f3de-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="2f3de-143">另一種造成每個範例執行的方式是使用具有 [語義 SV \_ SampleIndex](dx-graphics-hlsl-semantics.md)的輸入，這表示目前的範例。</span><span class="sxs-lookup"><span data-stu-id="2f3de-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="2f3de-144">只有 **指定 (** 或輸入 SV) SampleIndex 的輸入 \_ 會在圖元中的著色器調用之間有所不同，而其他未指定修飾詞的輸入則不會指定修飾詞 (例如，如果您混用不同輸入的修飾詞) 仍插入圖元中心。</span><span class="sxs-lookup"><span data-stu-id="2f3de-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="2f3de-145">圖元著色器調用和深度/樣板測試都會針對圖元中的每個涵蓋樣本進行。</span><span class="sxs-lookup"><span data-stu-id="2f3de-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="2f3de-146">這有時也稱為 *supersampling*。</span><span class="sxs-lookup"><span data-stu-id="2f3de-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="2f3de-147">相反地，如果沒有取樣頻率叫用（稱為「 *取樣* 率」），就會針對每個圖元叫用一次圖元著色器，而不論涵蓋的樣本數為何，深度/樣板測試都會以取樣頻率進行。</span><span class="sxs-lookup"><span data-stu-id="2f3de-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="2f3de-148">這兩種模式都提供對等的邊緣消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="2f3de-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="2f3de-149">不過，supersampling 會更頻繁地叫用圖元著色器，以提供更佳的著色品質。</span><span class="sxs-lookup"><span data-stu-id="2f3de-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="2f3de-150">1. 使用 int/uint 型別時，唯一有效的選項為 **nointerpolation**。</span><span class="sxs-lookup"><span data-stu-id="2f3de-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="2f3de-151">插補修飾詞可以套用至結構成員或函式 [引數](dx-graphics-hlsl-function-parameters.md)，或兩者皆適用。</span><span class="sxs-lookup"><span data-stu-id="2f3de-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="2f3de-152">範例</span><span class="sxs-lookup"><span data-stu-id="2f3de-152">Examples</span></span>

<span data-ttu-id="2f3de-153">以下是一些範例結構聲明。</span><span class="sxs-lookup"><span data-stu-id="2f3de-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="2f3de-154">此宣告包含陣列。</span><span class="sxs-lookup"><span data-stu-id="2f3de-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="2f3de-155">此宣告包含插補修飾詞。</span><span class="sxs-lookup"><span data-stu-id="2f3de-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="2f3de-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f3de-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3de-157"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="2f3de-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





