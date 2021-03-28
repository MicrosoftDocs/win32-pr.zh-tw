---
title: 'dcl_immediateConstantBuffer (sm4-asm) '
description: 'dcl \_ immediateConstantBuffer (sm4-asm) '
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313767"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a><span data-ttu-id="6de43-103">dcl \_ immediateConstantBuffer (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="6de43-103">dcl\_immediateConstantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="6de43-104">宣告著色器的立即常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6de43-104">Declares a shader immediate-constant buffer.</span></span>



| <span data-ttu-id="6de43-105">\_ *(s)* 的 dcl immediateConstantBuffer 值</span><span class="sxs-lookup"><span data-stu-id="6de43-105">dcl\_immediateConstantBuffer *value(s)*</span></span> |
|-----------------------------------------|



 

<dl> <dt>

<span data-ttu-id="6de43-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*值 (s)*</span><span class="sxs-lookup"><span data-stu-id="6de43-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*</span></span>
</dt> <dd>

<span data-ttu-id="6de43-107">\[\]緩衝區中必須包含至少一個值，但不能超過4096的值。</span><span class="sxs-lookup"><span data-stu-id="6de43-107">\[in\] The buffer must contain at least one value, but not more than 4096 values.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="6de43-108">備註</span><span class="sxs-lookup"><span data-stu-id="6de43-108">Remarks</span></span>

<span data-ttu-id="6de43-109">著色器允許一個立即常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6de43-109">A shader is allowed one immediate-constant buffer.</span></span> <span data-ttu-id="6de43-110">直接常數緩衝區的存取方式就像是具有動態索引的常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6de43-110">An immediate-constant buffer is accessed just like a constant buffer with dynamic indexing.</span></span>

<span data-ttu-id="6de43-111">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6de43-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6de43-112">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="6de43-112">Vertex Shader</span></span> | <span data-ttu-id="6de43-113">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="6de43-113">Geometry Shader</span></span> | <span data-ttu-id="6de43-114">像素著色器</span><span class="sxs-lookup"><span data-stu-id="6de43-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6de43-115">x</span><span class="sxs-lookup"><span data-stu-id="6de43-115">x</span></span>             | <span data-ttu-id="6de43-116">x</span><span class="sxs-lookup"><span data-stu-id="6de43-116">x</span></span>               | <span data-ttu-id="6de43-117">x</span><span class="sxs-lookup"><span data-stu-id="6de43-117">x</span></span>            |



 

<span data-ttu-id="6de43-118">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="6de43-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6de43-119">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6de43-119">Minimum Shader Model</span></span>

<span data-ttu-id="6de43-120">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6de43-120">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6de43-121">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6de43-121">Shader Model</span></span>                                              | <span data-ttu-id="6de43-122">支援</span><span class="sxs-lookup"><span data-stu-id="6de43-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6de43-123">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6de43-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6de43-124">是</span><span class="sxs-lookup"><span data-stu-id="6de43-124">yes</span></span>       |
| [<span data-ttu-id="6de43-125">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6de43-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6de43-126">是</span><span class="sxs-lookup"><span data-stu-id="6de43-126">yes</span></span>       |
| [<span data-ttu-id="6de43-127">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6de43-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6de43-128">是</span><span class="sxs-lookup"><span data-stu-id="6de43-128">yes</span></span>       |
| [<span data-ttu-id="6de43-129">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de43-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6de43-130">不可以</span><span class="sxs-lookup"><span data-stu-id="6de43-130">no</span></span>        |
| [<span data-ttu-id="6de43-131">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de43-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6de43-132">不可以</span><span class="sxs-lookup"><span data-stu-id="6de43-132">no</span></span>        |
| [<span data-ttu-id="6de43-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de43-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6de43-134">不可以</span><span class="sxs-lookup"><span data-stu-id="6de43-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6de43-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="6de43-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6de43-136">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de43-136">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




