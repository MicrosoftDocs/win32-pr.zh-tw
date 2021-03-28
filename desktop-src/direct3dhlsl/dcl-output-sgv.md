---
title: 'dcl_output_sgv (sm4-asm) '
description: 'dcl \_ 輸出 \_ sgv (sm4-asm) '
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373911"
---
# <a name="dcl_output_sgv-sm4---asm"></a><span data-ttu-id="af8dc-103">dcl \_ 輸出 \_ sgv (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="af8dc-103">dcl\_output\_sgv (sm4 - asm)</span></span>

<span data-ttu-id="af8dc-104">宣告包含 [系統值](dx-graphics-hlsl-semantics.md) 參數的輸出暫存器。</span><span class="sxs-lookup"><span data-stu-id="af8dc-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="af8dc-105">\_ \_ sgv 上的 dcl 輸出：*\[ mask \]*、 *systemValue*</span><span class="sxs-lookup"><span data-stu-id="af8dc-105">dcl\_output\_sgv oN *\[.mask\]*, *systemValue*</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="af8dc-106">項目</span><span class="sxs-lookup"><span data-stu-id="af8dc-106">Item</span></span>                                                                                                                               | <span data-ttu-id="af8dc-107">描述</span><span class="sxs-lookup"><span data-stu-id="af8dc-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af8dc-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="af8dc-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="af8dc-109">\[在 \] 輸出資料註冊中; *N* 是表示註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="af8dc-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="af8dc-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[mask\]*</span><span class="sxs-lookup"><span data-stu-id="af8dc-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="af8dc-111">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="af8dc-111">\[in\] Optional.</span></span> <span data-ttu-id="af8dc-112">元件遮罩 ( xyzw) ，可指定要使用的註冊元件。</span><span class="sxs-lookup"><span data-stu-id="af8dc-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="af8dc-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="af8dc-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="af8dc-114">\[在 \] 系統值名稱中是字串 (請參閱 [系統值語義](dx-graphics-hlsl-semantics.md)) ，但不含 "SV \_ " 前置詞。</span><span class="sxs-lookup"><span data-stu-id="af8dc-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="af8dc-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="af8dc-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="af8dc-116">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="af8dc-116">Vertex Shader</span></span> | <span data-ttu-id="af8dc-117">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="af8dc-117">Geometry Shader</span></span> | <span data-ttu-id="af8dc-118">像素著色器</span><span class="sxs-lookup"><span data-stu-id="af8dc-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="af8dc-119">x</span><span class="sxs-lookup"><span data-stu-id="af8dc-119">x</span></span>               |              |



 

<span data-ttu-id="af8dc-120">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="af8dc-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="af8dc-121">範例</span><span class="sxs-lookup"><span data-stu-id="af8dc-121">Example</span></span>

<span data-ttu-id="af8dc-122">範例如下。</span><span class="sxs-lookup"><span data-stu-id="af8dc-122">Here is an example.</span></span>


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a><span data-ttu-id="af8dc-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="af8dc-123">Minimum Shader Model</span></span>

<span data-ttu-id="af8dc-124">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="af8dc-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="af8dc-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="af8dc-125">Shader Model</span></span>                                              | <span data-ttu-id="af8dc-126">支援</span><span class="sxs-lookup"><span data-stu-id="af8dc-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="af8dc-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="af8dc-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="af8dc-128">是</span><span class="sxs-lookup"><span data-stu-id="af8dc-128">yes</span></span>       |
| [<span data-ttu-id="af8dc-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="af8dc-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="af8dc-130">是</span><span class="sxs-lookup"><span data-stu-id="af8dc-130">yes</span></span>       |
| [<span data-ttu-id="af8dc-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="af8dc-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="af8dc-132">是</span><span class="sxs-lookup"><span data-stu-id="af8dc-132">yes</span></span>       |
| [<span data-ttu-id="af8dc-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="af8dc-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="af8dc-134">不可以</span><span class="sxs-lookup"><span data-stu-id="af8dc-134">no</span></span>        |
| [<span data-ttu-id="af8dc-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="af8dc-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="af8dc-136">不可以</span><span class="sxs-lookup"><span data-stu-id="af8dc-136">no</span></span>        |
| [<span data-ttu-id="af8dc-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="af8dc-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="af8dc-138">不可以</span><span class="sxs-lookup"><span data-stu-id="af8dc-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="af8dc-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="af8dc-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af8dc-140">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="af8dc-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





