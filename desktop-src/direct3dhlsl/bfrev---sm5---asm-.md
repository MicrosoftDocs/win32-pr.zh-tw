---
title: 'bfrev (sm5-asm) '
description: 反轉32位的數位。
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990783"
---
# <a name="bfrev-sm5---asm"></a><span data-ttu-id="a10ad-103">bfrev (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="a10ad-103">bfrev (sm5 - asm)</span></span>

<span data-ttu-id="a10ad-104">反轉32位的數位。</span><span class="sxs-lookup"><span data-stu-id="a10ad-104">Reverse a 32-bit number.</span></span>



| <span data-ttu-id="a10ad-105">bfrev dest \[ . mask \] ，src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a10ad-105">bfrev dest\[.mask\], src0\[.swizzle\]</span></span> |
|---------------------------------------|



 



| <span data-ttu-id="a10ad-106">項目</span><span class="sxs-lookup"><span data-stu-id="a10ad-106">Item</span></span>                                                            | <span data-ttu-id="a10ad-107">描述</span><span class="sxs-lookup"><span data-stu-id="a10ad-107">Description</span></span>                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a10ad-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="a10ad-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a10ad-109">\[在 \] *src0* 的位址中，bits 反轉。</span><span class="sxs-lookup"><span data-stu-id="a10ad-109">\[in\] The address for *src0* with bits reversed.</span></span><br/> |
| <span data-ttu-id="a10ad-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a10ad-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a10ad-111">\[\]要反轉的32位數位。</span><span class="sxs-lookup"><span data-stu-id="a10ad-111">\[in\] The 32-bit number to reverse.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="a10ad-112">備註</span><span class="sxs-lookup"><span data-stu-id="a10ad-112">Remarks</span></span>

<span data-ttu-id="a10ad-113">例如，假設0x12345678，結果會是0x1e6a2c48。</span><span class="sxs-lookup"><span data-stu-id="a10ad-113">For example, given 0x12345678 the result would be 0x1e6a2c48.</span></span>

<span data-ttu-id="a10ad-114">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a10ad-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a10ad-115">頂點</span><span class="sxs-lookup"><span data-stu-id="a10ad-115">Vertex</span></span> | <span data-ttu-id="a10ad-116">船體</span><span class="sxs-lookup"><span data-stu-id="a10ad-116">Hull</span></span> | <span data-ttu-id="a10ad-117">網域</span><span class="sxs-lookup"><span data-stu-id="a10ad-117">Domain</span></span> | <span data-ttu-id="a10ad-118">幾何</span><span class="sxs-lookup"><span data-stu-id="a10ad-118">Geometry</span></span> | <span data-ttu-id="a10ad-119">像素</span><span class="sxs-lookup"><span data-stu-id="a10ad-119">Pixel</span></span> | <span data-ttu-id="a10ad-120">計算</span><span class="sxs-lookup"><span data-stu-id="a10ad-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a10ad-121">X</span><span class="sxs-lookup"><span data-stu-id="a10ad-121">X</span></span>      | <span data-ttu-id="a10ad-122">X</span><span class="sxs-lookup"><span data-stu-id="a10ad-122">X</span></span>    | <span data-ttu-id="a10ad-123">X</span><span class="sxs-lookup"><span data-stu-id="a10ad-123">X</span></span>      | <span data-ttu-id="a10ad-124">X</span><span class="sxs-lookup"><span data-stu-id="a10ad-124">X</span></span>        | <span data-ttu-id="a10ad-125">X</span><span class="sxs-lookup"><span data-stu-id="a10ad-125">X</span></span>     | <span data-ttu-id="a10ad-126">X</span><span class="sxs-lookup"><span data-stu-id="a10ad-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a10ad-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a10ad-127">Minimum Shader Model</span></span>

<span data-ttu-id="a10ad-128">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="a10ad-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a10ad-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a10ad-129">Shader Model</span></span>                                              | <span data-ttu-id="a10ad-130">支援</span><span class="sxs-lookup"><span data-stu-id="a10ad-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a10ad-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a10ad-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a10ad-132">是</span><span class="sxs-lookup"><span data-stu-id="a10ad-132">yes</span></span>       |
| [<span data-ttu-id="a10ad-133">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a10ad-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a10ad-134">不可以</span><span class="sxs-lookup"><span data-stu-id="a10ad-134">no</span></span>        |
| [<span data-ttu-id="a10ad-135">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a10ad-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a10ad-136">不可以</span><span class="sxs-lookup"><span data-stu-id="a10ad-136">no</span></span>        |
| [<span data-ttu-id="a10ad-137">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a10ad-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a10ad-138">不可以</span><span class="sxs-lookup"><span data-stu-id="a10ad-138">no</span></span>        |
| [<span data-ttu-id="a10ad-139">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a10ad-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a10ad-140">不可以</span><span class="sxs-lookup"><span data-stu-id="a10ad-140">no</span></span>        |
| [<span data-ttu-id="a10ad-141">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a10ad-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a10ad-142">不可以</span><span class="sxs-lookup"><span data-stu-id="a10ad-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a10ad-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="a10ad-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a10ad-144">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a10ad-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





