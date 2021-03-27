---
title: 'dcl_output (sm4-asm) '
description: 'dcl \_ 輸出 (sm4-asm) '
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971617"
---
# <a name="dcl_output-sm4---asm"></a><span data-ttu-id="db7c7-103">dcl \_ 輸出 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="db7c7-103">dcl\_output (sm4 - asm)</span></span>

<span data-ttu-id="db7c7-104">宣告著色器輸出暫存器。</span><span class="sxs-lookup"><span data-stu-id="db7c7-104">Declares a shader-output register.</span></span>



| <span data-ttu-id="db7c7-105">dcl \_ 輸出 o *N \[ . mask \]*</span><span class="sxs-lookup"><span data-stu-id="db7c7-105">dcl\_output o *N\[.mask\]*</span></span> |
|---------------------------|



 



| <span data-ttu-id="db7c7-106">項目</span><span class="sxs-lookup"><span data-stu-id="db7c7-106">Item</span></span>                                                                           | <span data-ttu-id="db7c7-107">描述</span><span class="sxs-lookup"><span data-stu-id="db7c7-107">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db7c7-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="db7c7-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/> | <span data-ttu-id="db7c7-109">\[在 \] 輸出資料註冊中; *N* 是表示註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="db7c7-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>               |
| <span data-ttu-id="db7c7-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[mask\]*</span><span class="sxs-lookup"><span data-stu-id="db7c7-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>     | <span data-ttu-id="db7c7-111">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="db7c7-111">\[in\] Optional.</span></span> <span data-ttu-id="db7c7-112">元件遮罩 ( xyzw) ，可指定要使用的註冊元件。</span><span class="sxs-lookup"><span data-stu-id="db7c7-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/> |



 

<span data-ttu-id="db7c7-113">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="db7c7-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="db7c7-114">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="db7c7-114">Vertex Shader</span></span> | <span data-ttu-id="db7c7-115">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="db7c7-115">Geometry Shader</span></span> | <span data-ttu-id="db7c7-116">像素著色器</span><span class="sxs-lookup"><span data-stu-id="db7c7-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="db7c7-117">x</span><span class="sxs-lookup"><span data-stu-id="db7c7-117">x</span></span>             | <span data-ttu-id="db7c7-118">x</span><span class="sxs-lookup"><span data-stu-id="db7c7-118">x</span></span>               | <span data-ttu-id="db7c7-119">x</span><span class="sxs-lookup"><span data-stu-id="db7c7-119">x</span></span>            |



 

<span data-ttu-id="db7c7-120">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="db7c7-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="db7c7-121">範例</span><span class="sxs-lookup"><span data-stu-id="db7c7-121">Example</span></span>

<span data-ttu-id="db7c7-122">以下是一些範例。</span><span class="sxs-lookup"><span data-stu-id="db7c7-122">Here are some examples.</span></span>


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



## <a name="minimum-shader-model"></a><span data-ttu-id="db7c7-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="db7c7-123">Minimum Shader Model</span></span>

<span data-ttu-id="db7c7-124">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="db7c7-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="db7c7-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="db7c7-125">Shader Model</span></span>                                              | <span data-ttu-id="db7c7-126">支援</span><span class="sxs-lookup"><span data-stu-id="db7c7-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="db7c7-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="db7c7-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="db7c7-128">是</span><span class="sxs-lookup"><span data-stu-id="db7c7-128">yes</span></span>       |
| [<span data-ttu-id="db7c7-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="db7c7-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="db7c7-130">是</span><span class="sxs-lookup"><span data-stu-id="db7c7-130">yes</span></span>       |
| [<span data-ttu-id="db7c7-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="db7c7-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="db7c7-132">是</span><span class="sxs-lookup"><span data-stu-id="db7c7-132">yes</span></span>       |
| [<span data-ttu-id="db7c7-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="db7c7-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="db7c7-134">不可以</span><span class="sxs-lookup"><span data-stu-id="db7c7-134">no</span></span>        |
| [<span data-ttu-id="db7c7-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="db7c7-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="db7c7-136">不可以</span><span class="sxs-lookup"><span data-stu-id="db7c7-136">no</span></span>        |
| [<span data-ttu-id="db7c7-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="db7c7-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="db7c7-138">不可以</span><span class="sxs-lookup"><span data-stu-id="db7c7-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="db7c7-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="db7c7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db7c7-140">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="db7c7-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





