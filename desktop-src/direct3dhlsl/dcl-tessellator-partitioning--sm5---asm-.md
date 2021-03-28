---
title: 'dcl_tessellator_partitioning (sm5-asm) '
description: 在 [輪廓著色器宣告] 區段中宣告鑲嵌資料分割。
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373899"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a><span data-ttu-id="c45e2-103">dcl \_ 鑲嵌 \_ 分割 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="c45e2-103">dcl\_tessellator\_partitioning (sm5 - asm)</span></span>

<span data-ttu-id="c45e2-104">在 [輪廓著色器宣告] 區段中宣告鑲嵌資料分割。</span><span class="sxs-lookup"><span data-stu-id="c45e2-104">Declare the tessellator partitioning in a hull shader declaration section.</span></span>



| <span data-ttu-id="c45e2-105">dcl \_ 鑲嵌 \_ 分割 {資料分割 \_ 整數 </span><span class="sxs-lookup"><span data-stu-id="c45e2-105">dcl\_tessellator\_partitioning {partitioning\_integer</span></span>\| <span data-ttu-id="c45e2-106">資料分割 \_ pow2 </span><span class="sxs-lookup"><span data-stu-id="c45e2-106">partitioning\_pow2</span></span>\|<span data-ttu-id="c45e2-107">分割 \_ 小數 \_ 奇數</span><span class="sxs-lookup"><span data-stu-id="c45e2-107">partitioning\_fractional\_odd\</span></span>| <span data-ttu-id="c45e2-108">分割 \_ 小數 \_ 偶數}</span><span class="sxs-lookup"><span data-stu-id="c45e2-108">partitioning\_fractional\_even}</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c45e2-109">項目</span><span class="sxs-lookup"><span data-stu-id="c45e2-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="c45e2-110">描述</span><span class="sxs-lookup"><span data-stu-id="c45e2-110">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="c45e2-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*分割 \_ 整數資料 \| 分割 \_ pow2 \| 分割小數的 \_ \_ 奇數分割小數 \| \_ \_ 偶數*</span><span class="sxs-lookup"><span data-stu-id="c45e2-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitioning\_integer\| partitioning\_pow2\|partitioning\_fractional\_odd\| partitioning\_fractional\_even*</span></span><br/> | <span data-ttu-id="c45e2-112">\[在 \] 鑲嵌資料分割中。</span><span class="sxs-lookup"><span data-stu-id="c45e2-112">\[in\] The tessellator partitioning.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c45e2-113">備註</span><span class="sxs-lookup"><span data-stu-id="c45e2-113">Remarks</span></span>

<span data-ttu-id="c45e2-114">從硬體觀點來看， \_ pow2 的行為就像 \_ 整數一樣。</span><span class="sxs-lookup"><span data-stu-id="c45e2-114">From the hardware point of view, \_pow2 behaves just like \_integer.</span></span> <span data-ttu-id="c45e2-115">HLSL 著色器作者及/或 compilercode 將 TessFactors 四捨五入為2的乘冪。</span><span class="sxs-lookup"><span data-stu-id="c45e2-115">It is up to the HLSL shader author and/or compilercode to round TessFactors to powers of 2.</span></span>

<span data-ttu-id="c45e2-116">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="c45e2-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c45e2-117">頂點</span><span class="sxs-lookup"><span data-stu-id="c45e2-117">Vertex</span></span> | <span data-ttu-id="c45e2-118">船體</span><span class="sxs-lookup"><span data-stu-id="c45e2-118">Hull</span></span>                 | <span data-ttu-id="c45e2-119">網域</span><span class="sxs-lookup"><span data-stu-id="c45e2-119">Domain</span></span> | <span data-ttu-id="c45e2-120">幾何</span><span class="sxs-lookup"><span data-stu-id="c45e2-120">Geometry</span></span> | <span data-ttu-id="c45e2-121">像素</span><span class="sxs-lookup"><span data-stu-id="c45e2-121">Pixel</span></span> | <span data-ttu-id="c45e2-122">計算</span><span class="sxs-lookup"><span data-stu-id="c45e2-122">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="c45e2-123">宣告區段</span><span class="sxs-lookup"><span data-stu-id="c45e2-123">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c45e2-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c45e2-124">Minimum Shader Model</span></span>

<span data-ttu-id="c45e2-125">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="c45e2-125">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c45e2-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c45e2-126">Shader Model</span></span>                                              | <span data-ttu-id="c45e2-127">支援</span><span class="sxs-lookup"><span data-stu-id="c45e2-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c45e2-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c45e2-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c45e2-129">是</span><span class="sxs-lookup"><span data-stu-id="c45e2-129">yes</span></span>       |
| [<span data-ttu-id="c45e2-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="c45e2-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c45e2-131">不可以</span><span class="sxs-lookup"><span data-stu-id="c45e2-131">no</span></span>        |
| [<span data-ttu-id="c45e2-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="c45e2-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c45e2-133">不可以</span><span class="sxs-lookup"><span data-stu-id="c45e2-133">no</span></span>        |
| [<span data-ttu-id="c45e2-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c45e2-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c45e2-135">不可以</span><span class="sxs-lookup"><span data-stu-id="c45e2-135">no</span></span>        |
| [<span data-ttu-id="c45e2-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c45e2-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c45e2-137">不可以</span><span class="sxs-lookup"><span data-stu-id="c45e2-137">no</span></span>        |
| [<span data-ttu-id="c45e2-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c45e2-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c45e2-139">不可以</span><span class="sxs-lookup"><span data-stu-id="c45e2-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c45e2-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="c45e2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c45e2-141">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c45e2-141">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





