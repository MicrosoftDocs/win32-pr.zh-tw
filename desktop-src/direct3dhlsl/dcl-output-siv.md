---
title: 'dcl_output_siv (sm4-asm) '
description: 'dcl \_ 輸出 \_ siv (sm4-asm) '
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df57ea991b9177dc081443301e426560834df894
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990831"
---
# <a name="dcl_output_siv-sm4---asm"></a><span data-ttu-id="f2ca9-103">dcl \_ 輸出 \_ siv (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="f2ca9-103">dcl\_output\_siv (sm4 - asm)</span></span>

<span data-ttu-id="f2ca9-104">宣告包含 [系統值](dx-graphics-hlsl-semantics.md) 參數的輸出暫存器。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="f2ca9-105">\_ \_ siv 上的 dcl 輸出： \[ *遮罩* \] 、 *systemValue*</span><span class="sxs-lookup"><span data-stu-id="f2ca9-105">dcl\_output\_siv oN\[*.masks*\], *systemValue*</span></span> |
|------------------------------------------------|



 



| <span data-ttu-id="f2ca9-106">項目</span><span class="sxs-lookup"><span data-stu-id="f2ca9-106">Item</span></span>                                                                                                                               | <span data-ttu-id="f2ca9-107">描述</span><span class="sxs-lookup"><span data-stu-id="f2ca9-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ca9-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="f2ca9-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="f2ca9-109">\[在 \] 輸出資料註冊中; *N* 是表示註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="f2ca9-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[mask\]*</span><span class="sxs-lookup"><span data-stu-id="f2ca9-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="f2ca9-111">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-111">\[in\] Optional.</span></span> <span data-ttu-id="f2ca9-112">元件遮罩 ( xyzw) ，可指定要使用的註冊元件。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="f2ca9-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="f2ca9-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="f2ca9-114">\[在 \] 系統值名稱中是字串 (請參閱 [系統值語義](dx-graphics-hlsl-semantics.md)) ，但不含 "SV \_ " 前置詞。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="f2ca9-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f2ca9-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f2ca9-116">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="f2ca9-116">Vertex Shader</span></span> | <span data-ttu-id="f2ca9-117">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="f2ca9-117">Geometry Shader</span></span> | <span data-ttu-id="f2ca9-118">像素著色器</span><span class="sxs-lookup"><span data-stu-id="f2ca9-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f2ca9-119">x</span><span class="sxs-lookup"><span data-stu-id="f2ca9-119">x</span></span>             | <span data-ttu-id="f2ca9-120">x</span><span class="sxs-lookup"><span data-stu-id="f2ca9-120">x</span></span>               |              |



 

<span data-ttu-id="f2ca9-121">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-121">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="f2ca9-122">範例</span><span class="sxs-lookup"><span data-stu-id="f2ca9-122">Example</span></span>

<span data-ttu-id="f2ca9-123">以下是一些範例。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-123">Here are some examples.</span></span>


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a><span data-ttu-id="f2ca9-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2ca9-124">Minimum Shader Model</span></span>

<span data-ttu-id="f2ca9-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f2ca9-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2ca9-126">Shader Model</span></span>                                              | <span data-ttu-id="f2ca9-127">支援</span><span class="sxs-lookup"><span data-stu-id="f2ca9-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f2ca9-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f2ca9-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f2ca9-129">是</span><span class="sxs-lookup"><span data-stu-id="f2ca9-129">yes</span></span>       |
| [<span data-ttu-id="f2ca9-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f2ca9-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f2ca9-131">是</span><span class="sxs-lookup"><span data-stu-id="f2ca9-131">yes</span></span>       |
| [<span data-ttu-id="f2ca9-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f2ca9-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f2ca9-133">是</span><span class="sxs-lookup"><span data-stu-id="f2ca9-133">yes</span></span>       |
| [<span data-ttu-id="f2ca9-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f2ca9-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f2ca9-135">不可以</span><span class="sxs-lookup"><span data-stu-id="f2ca9-135">no</span></span>        |
| [<span data-ttu-id="f2ca9-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f2ca9-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f2ca9-137">不可以</span><span class="sxs-lookup"><span data-stu-id="f2ca9-137">no</span></span>        |
| [<span data-ttu-id="f2ca9-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f2ca9-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f2ca9-139">不可以</span><span class="sxs-lookup"><span data-stu-id="f2ca9-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f2ca9-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2ca9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2ca9-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f2ca9-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





