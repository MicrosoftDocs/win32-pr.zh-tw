---
title: 'dcl_temps (sm4-asm) '
description: 'dcl \_ 溫度 (sm4-asm) '
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc3a468575b30836d4574edb13c4fc77a3505fc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990823"
---
# <a name="dcl_temps-sm4---asm"></a><span data-ttu-id="6c20a-103">dcl \_ 溫度 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="6c20a-103">dcl\_temps (sm4 - asm)</span></span>

<span data-ttu-id="6c20a-104">宣告暫存暫存器。</span><span class="sxs-lookup"><span data-stu-id="6c20a-104">Declares temporary registers.</span></span>



| <span data-ttu-id="6c20a-105">dcl \_ 溫度 N</span><span class="sxs-lookup"><span data-stu-id="6c20a-105">dcl\_temps N</span></span> |
|--------------|



 



| <span data-ttu-id="6c20a-106">項目</span><span class="sxs-lookup"><span data-stu-id="6c20a-106">Item</span></span>                                                   | <span data-ttu-id="6c20a-107">描述</span><span class="sxs-lookup"><span data-stu-id="6c20a-107">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c20a-108"><span id="N"></span><span id="n"></span>*N-1*</span><span class="sxs-lookup"><span data-stu-id="6c20a-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="6c20a-109">\[暫存登錄的 \] 數目。</span><span class="sxs-lookup"><span data-stu-id="6c20a-109">\[in\] The number of temporary registers.</span></span><br/> |



 

<span data-ttu-id="6c20a-110">每個註冊程式都有一個32位的四元件值空間。</span><span class="sxs-lookup"><span data-stu-id="6c20a-110">Each register has space for a 32-bit four-component value.</span></span> <span data-ttu-id="6c20a-111">暫存和可 [編制索引](dcl-indexabletemp.md) 的暫存暫存器總數必須小於或等於4096。</span><span class="sxs-lookup"><span data-stu-id="6c20a-111">The total number of temporary and [indexable-temporary](dcl-indexabletemp.md) registers must be less than or equal to 4096.</span></span>

<span data-ttu-id="6c20a-112">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6c20a-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6c20a-113">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="6c20a-113">Vertex Shader</span></span> | <span data-ttu-id="6c20a-114">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="6c20a-114">Geometry Shader</span></span> | <span data-ttu-id="6c20a-115">像素著色器</span><span class="sxs-lookup"><span data-stu-id="6c20a-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6c20a-116">x</span><span class="sxs-lookup"><span data-stu-id="6c20a-116">x</span></span>             | <span data-ttu-id="6c20a-117">x</span><span class="sxs-lookup"><span data-stu-id="6c20a-117">x</span></span>               | <span data-ttu-id="6c20a-118">x</span><span class="sxs-lookup"><span data-stu-id="6c20a-118">x</span></span>            |



 

<span data-ttu-id="6c20a-119">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="6c20a-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="6c20a-120">範例</span><span class="sxs-lookup"><span data-stu-id="6c20a-120">Example</span></span>

<span data-ttu-id="6c20a-121">範例如下。</span><span class="sxs-lookup"><span data-stu-id="6c20a-121">Here is an example.</span></span>


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="6c20a-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6c20a-122">Minimum Shader Model</span></span>

<span data-ttu-id="6c20a-123">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6c20a-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6c20a-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6c20a-124">Shader Model</span></span>                                              | <span data-ttu-id="6c20a-125">支援</span><span class="sxs-lookup"><span data-stu-id="6c20a-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6c20a-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6c20a-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6c20a-127">是</span><span class="sxs-lookup"><span data-stu-id="6c20a-127">yes</span></span>       |
| [<span data-ttu-id="6c20a-128">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6c20a-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6c20a-129">是</span><span class="sxs-lookup"><span data-stu-id="6c20a-129">yes</span></span>       |
| [<span data-ttu-id="6c20a-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6c20a-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6c20a-131">是</span><span class="sxs-lookup"><span data-stu-id="6c20a-131">yes</span></span>       |
| [<span data-ttu-id="6c20a-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6c20a-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6c20a-133">不可以</span><span class="sxs-lookup"><span data-stu-id="6c20a-133">no</span></span>        |
| [<span data-ttu-id="6c20a-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6c20a-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6c20a-135">不可以</span><span class="sxs-lookup"><span data-stu-id="6c20a-135">no</span></span>        |
| [<span data-ttu-id="6c20a-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6c20a-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6c20a-137">不可以</span><span class="sxs-lookup"><span data-stu-id="6c20a-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6c20a-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c20a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c20a-139">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6c20a-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





