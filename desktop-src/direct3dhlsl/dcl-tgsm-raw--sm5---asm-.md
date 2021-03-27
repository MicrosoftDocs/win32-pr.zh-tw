---
title: 'dcl_tgsm_raw (sm5-asm) '
description: 宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679176"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a><span data-ttu-id="4515c-103">dcl \_ tgsm \_ 原始 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="4515c-103">dcl\_tgsm\_raw (sm5 - asm)</span></span>

<span data-ttu-id="4515c-104">宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。</span><span class="sxs-lookup"><span data-stu-id="4515c-104">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span>



| <span data-ttu-id="4515c-105">dcl \_ tgsm \_ 原始 g \# ，byteCount</span><span class="sxs-lookup"><span data-stu-id="4515c-105">dcl\_tgsm\_raw g\#, byteCount</span></span> |
|-------------------------------|



 



| <span data-ttu-id="4515c-106">項目</span><span class="sxs-lookup"><span data-stu-id="4515c-106">Item</span></span>                                                                                                       | <span data-ttu-id="4515c-107">描述</span><span class="sxs-lookup"><span data-stu-id="4515c-107">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4515c-108"><span id="g_"></span><span id="G_"></span>*G\#*</span><span class="sxs-lookup"><span data-stu-id="4515c-108"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                 | <span data-ttu-id="4515c-109">\[在不具 \] 類型的共用記憶體的大小 *byteCount* 的參考中。</span><span class="sxs-lookup"><span data-stu-id="4515c-109">\[in\] A reference to a block of size *byteCount* of untyped shared memory.</span></span> <br/> |
| <span data-ttu-id="4515c-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span><span class="sxs-lookup"><span data-stu-id="4515c-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span></span><br/> | <span data-ttu-id="4515c-111">\[in \] 必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="4515c-111">\[in\] Must be a multiple of 4.</span></span> <br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="4515c-112">備註</span><span class="sxs-lookup"><span data-stu-id="4515c-112">Remarks</span></span>

<span data-ttu-id="4515c-113">所有 g 的總儲存空間 \# 必須 <= 每個執行緒群組可用的共用記憶體數量（32kB）。</span><span class="sxs-lookup"><span data-stu-id="4515c-113">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB.</span></span>

<span data-ttu-id="4515c-114">在極端情況下，您可以宣告 8192 total g \# s，每個都有4個 *byteCount* 。</span><span class="sxs-lookup"><span data-stu-id="4515c-114">In an extreme case, you can declare 8192 total g\# s, each with a *byteCount* of 4.</span></span>

<span data-ttu-id="4515c-115">在相反的極端情況下，您可以宣告 \# *byteCount* 為32768的單一 g。</span><span class="sxs-lookup"><span data-stu-id="4515c-115">In the opposite extreme, you can declare a single g\# with a *byteCount* of 32768.</span></span>

> [!Note]  
> <span data-ttu-id="4515c-116">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援 [ \_ tgsm \_ 結構化](dcl-tgsm-structured--sm5---asm-.md)，但不 **支援 \_ tgsm \_ 原始** 的 dcl。</span><span class="sxs-lookup"><span data-stu-id="4515c-116">cs\_4\_0 and cs\_4\_1 supports [dcl\_tgsm\_structured](dcl-tgsm-structured--sm5---asm-.md), but not **dcl\_tgsm\_raw**.</span></span>

 

<span data-ttu-id="4515c-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4515c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4515c-118">頂點</span><span class="sxs-lookup"><span data-stu-id="4515c-118">Vertex</span></span> | <span data-ttu-id="4515c-119">船體</span><span class="sxs-lookup"><span data-stu-id="4515c-119">Hull</span></span> | <span data-ttu-id="4515c-120">網域</span><span class="sxs-lookup"><span data-stu-id="4515c-120">Domain</span></span> | <span data-ttu-id="4515c-121">幾何</span><span class="sxs-lookup"><span data-stu-id="4515c-121">Geometry</span></span> | <span data-ttu-id="4515c-122">像素</span><span class="sxs-lookup"><span data-stu-id="4515c-122">Pixel</span></span> | <span data-ttu-id="4515c-123">計算</span><span class="sxs-lookup"><span data-stu-id="4515c-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="4515c-124">X</span><span class="sxs-lookup"><span data-stu-id="4515c-124">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4515c-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4515c-125">Minimum Shader Model</span></span>

<span data-ttu-id="4515c-126">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="4515c-126">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4515c-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4515c-127">Shader Model</span></span>                                              | <span data-ttu-id="4515c-128">支援</span><span class="sxs-lookup"><span data-stu-id="4515c-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4515c-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4515c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4515c-130">是</span><span class="sxs-lookup"><span data-stu-id="4515c-130">yes</span></span>       |
| [<span data-ttu-id="4515c-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4515c-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4515c-132">不可以</span><span class="sxs-lookup"><span data-stu-id="4515c-132">no</span></span>        |
| [<span data-ttu-id="4515c-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4515c-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4515c-134">不可以</span><span class="sxs-lookup"><span data-stu-id="4515c-134">no</span></span>        |
| [<span data-ttu-id="4515c-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4515c-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4515c-136">不可以</span><span class="sxs-lookup"><span data-stu-id="4515c-136">no</span></span>        |
| [<span data-ttu-id="4515c-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4515c-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4515c-138">不可以</span><span class="sxs-lookup"><span data-stu-id="4515c-138">no</span></span>        |
| [<span data-ttu-id="4515c-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4515c-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4515c-140">不可以</span><span class="sxs-lookup"><span data-stu-id="4515c-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4515c-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="4515c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4515c-142">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4515c-142">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





