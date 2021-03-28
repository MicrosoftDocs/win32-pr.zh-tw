---
title: 'dcl_tessellator_output_primitive (sm5-asm) '
description: 在 [輪廓著色器宣告] 區段中宣告鑲嵌輸出基本類型。
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022854"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a><span data-ttu-id="4a9e0-103">dcl \_ 鑲嵌 \_ 輸出 \_ 基本 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="4a9e0-103">dcl\_tessellator\_output\_primitive (sm5 - asm)</span></span>

<span data-ttu-id="4a9e0-104">在 [輪廓著色器宣告] 區段中宣告鑲嵌輸出基本類型。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-104">Declare the tessellator output primitive type in a hull shader declaration section.</span></span>



| <span data-ttu-id="4a9e0-105">dcl \_ 鑲嵌 \_ 輸出 \_ 基本 {輸出 \_ 點 </span><span class="sxs-lookup"><span data-stu-id="4a9e0-105">dcl\_tessellator\_output\_primitive {output\_point </span></span>\| <span data-ttu-id="4a9e0-106">輸出 \_ 行 </span><span class="sxs-lookup"><span data-stu-id="4a9e0-106">output\_line </span></span>\| <span data-ttu-id="4a9e0-107">triangloutput \_ e \_ cw </span><span class="sxs-lookup"><span data-stu-id="4a9e0-107">triangloutput\_e\_cw </span></span>\| <span data-ttu-id="4a9e0-108">輸出 \_ 三角形 \_ ccw}</span><span class="sxs-lookup"><span data-stu-id="4a9e0-108">output\_triangle\_ccw}</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4a9e0-109">項目</span><span class="sxs-lookup"><span data-stu-id="4a9e0-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="4a9e0-110">描述</span><span class="sxs-lookup"><span data-stu-id="4a9e0-110">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="4a9e0-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*輸出 \_ 點 \| 輸出 \_ 行 \| triangloutput \_ e \_ cw \| 輸出 \_ 三角形 \_ ccw*</span><span class="sxs-lookup"><span data-stu-id="4a9e0-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*output\_point \| output\_line \| triangloutput\_e\_cw \| output\_triangle\_ccw*</span></span><br/> | <span data-ttu-id="4a9e0-112">\[在 \] 輸出基本類型中。</span><span class="sxs-lookup"><span data-stu-id="4a9e0-112">\[in\] The output primitive type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a9e0-113">備註</span><span class="sxs-lookup"><span data-stu-id="4a9e0-113">Remarks</span></span>

<span data-ttu-id="4a9e0-114">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4a9e0-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4a9e0-115">頂點</span><span class="sxs-lookup"><span data-stu-id="4a9e0-115">Vertex</span></span> | <span data-ttu-id="4a9e0-116">船體</span><span class="sxs-lookup"><span data-stu-id="4a9e0-116">Hull</span></span>                 | <span data-ttu-id="4a9e0-117">網域</span><span class="sxs-lookup"><span data-stu-id="4a9e0-117">Domain</span></span> | <span data-ttu-id="4a9e0-118">幾何</span><span class="sxs-lookup"><span data-stu-id="4a9e0-118">Geometry</span></span> | <span data-ttu-id="4a9e0-119">像素</span><span class="sxs-lookup"><span data-stu-id="4a9e0-119">Pixel</span></span> | <span data-ttu-id="4a9e0-120">計算</span><span class="sxs-lookup"><span data-stu-id="4a9e0-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="4a9e0-121">宣告區段</span><span class="sxs-lookup"><span data-stu-id="4a9e0-121">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4a9e0-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4a9e0-122">Minimum Shader Model</span></span>

<span data-ttu-id="4a9e0-123">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="4a9e0-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4a9e0-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4a9e0-124">Shader Model</span></span>                                              | <span data-ttu-id="4a9e0-125">支援</span><span class="sxs-lookup"><span data-stu-id="4a9e0-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4a9e0-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4a9e0-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4a9e0-127">是</span><span class="sxs-lookup"><span data-stu-id="4a9e0-127">yes</span></span>       |
| [<span data-ttu-id="4a9e0-128">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4a9e0-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4a9e0-129">不可以</span><span class="sxs-lookup"><span data-stu-id="4a9e0-129">no</span></span>        |
| [<span data-ttu-id="4a9e0-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4a9e0-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4a9e0-131">不可以</span><span class="sxs-lookup"><span data-stu-id="4a9e0-131">no</span></span>        |
| [<span data-ttu-id="4a9e0-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4a9e0-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4a9e0-133">不可以</span><span class="sxs-lookup"><span data-stu-id="4a9e0-133">no</span></span>        |
| [<span data-ttu-id="4a9e0-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4a9e0-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4a9e0-135">不可以</span><span class="sxs-lookup"><span data-stu-id="4a9e0-135">no</span></span>        |
| [<span data-ttu-id="4a9e0-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4a9e0-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4a9e0-137">不可以</span><span class="sxs-lookup"><span data-stu-id="4a9e0-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4a9e0-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a9e0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a9e0-139">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4a9e0-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





