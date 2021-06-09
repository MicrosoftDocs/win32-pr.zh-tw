---
title: packoffset
description: 選用的著色器常數封裝關鍵字，使用下列語法
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826077"
---
# <a name="packoffset"></a><span data-ttu-id="b0737-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="b0737-104">packoffset</span></span>

<span data-ttu-id="b0737-105">選用的著色器常數封裝關鍵字，使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="b0737-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>

<span data-ttu-id="b0737-106">： packoffset ( c \[ 子元件 \] \[ 。元件 \] ) </span><span class="sxs-lookup"><span data-stu-id="b0737-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span>



 

## <a name="parameters"></a><span data-ttu-id="b0737-107">參數</span><span class="sxs-lookup"><span data-stu-id="b0737-107">Parameters</span></span>



| <span data-ttu-id="b0737-108">項目</span><span class="sxs-lookup"><span data-stu-id="b0737-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="b0737-109">描述</span><span class="sxs-lookup"><span data-stu-id="b0737-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0737-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="b0737-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="b0737-111">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="b0737-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="b0737-112"><span id="c"></span><span id="C"></span>**C**</span><span class="sxs-lookup"><span data-stu-id="b0737-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="b0737-113">封裝僅適用于 (c) 的常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="b0737-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="b0737-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[子 \] \[ 元件\]**</span><span class="sxs-lookup"><span data-stu-id="b0737-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="b0737-115">選擇性的子元件和元件。</span><span class="sxs-lookup"><span data-stu-id="b0737-115">Optional subcomponents and components.</span></span> <span data-ttu-id="b0737-116">子元件是一個暫存器號碼，這是一個整數。</span><span class="sxs-lookup"><span data-stu-id="b0737-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="b0737-117">元件的格式為 \[ xyzw \] 。</span><span class="sxs-lookup"><span data-stu-id="b0737-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0737-118">備註</span><span class="sxs-lookup"><span data-stu-id="b0737-118">Remarks</span></span>

<span data-ttu-id="b0737-119">當宣告 [變數類型](dx-graphics-hlsl-variable-syntax.md)時，請使用這個關鍵字手動封裝著色器常數。</span><span class="sxs-lookup"><span data-stu-id="b0737-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="b0737-120">當封裝常數時，您無法混合常數類型。</span><span class="sxs-lookup"><span data-stu-id="b0737-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="b0737-121">針對全域常數和統一常數，編譯器的行為稍有不同：</span><span class="sxs-lookup"><span data-stu-id="b0737-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="b0737-122">全域常數。</span><span class="sxs-lookup"><span data-stu-id="b0737-122">A global constant.</span></span> <span data-ttu-id="b0737-123">全域變數會以全域常數的形式加入至編譯器所 cbuffer 的 *$Global* 。</span><span class="sxs-lookup"><span data-stu-id="b0737-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="b0737-124">自動封裝的元素 (不含 packoffset 的宣告) 將會出現在最後一個手動封裝的變數之後。</span><span class="sxs-lookup"><span data-stu-id="b0737-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="b0737-125">您可以在封裝全域常數時混合類型。</span><span class="sxs-lookup"><span data-stu-id="b0737-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="b0737-126">統一常數。</span><span class="sxs-lookup"><span data-stu-id="b0737-126">A uniform constant.</span></span> <span data-ttu-id="b0737-127">當著色器是在效果架構之外編譯時，編譯器會將函式參數清單中的統一參數加入至 *$Param* 常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b0737-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="b0737-128">在效果架構內編譯時，統一常數必須解析為全域範圍中定義的統一變數。</span><span class="sxs-lookup"><span data-stu-id="b0737-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="b0737-129">統一常數不能手動位移;它們的建議用途只是用來將著色器的別名特製化回全域，而不是將應用程式資料傳遞給著色器的方法。</span><span class="sxs-lookup"><span data-stu-id="b0737-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="b0737-130">以下是一些其他範例： [使用著色器模型4的封裝常數](dx-graphics-hlsl-packing-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="b0737-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b0737-131">範例</span><span class="sxs-lookup"><span data-stu-id="b0737-131">Examples</span></span>

<span data-ttu-id="b0737-132">以下是一些手動封裝著色器常數的範例。</span><span class="sxs-lookup"><span data-stu-id="b0737-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="b0737-133">封裝其大小夠大以防止暫存器界限的向量和純量子元件。</span><span class="sxs-lookup"><span data-stu-id="b0737-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="b0737-134">例如，這些都是有效的：</span><span class="sxs-lookup"><span data-stu-id="b0737-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="b0737-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0737-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0737-136">語法變數</span><span class="sxs-lookup"><span data-stu-id="b0737-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="b0737-137"> (DirectX HLSL) 的變數 </span><span class="sxs-lookup"><span data-stu-id="b0737-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





