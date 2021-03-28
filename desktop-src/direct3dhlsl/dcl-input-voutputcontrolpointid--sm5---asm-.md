---
title: 'dcl_input vOutputControlPointID (sm5-asm) '
description: 在「輪廓著色器」控制點階段中宣告輸出控制點識別碼。
ms.assetid: 376ECA4F-DD71-4466-8A9D-E92A536832BC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cee49a8a825f25b0fbbccff027d5ad1b9ade514
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022860"
---
# <a name="dcl_input-voutputcontrolpointid-sm5---asm"></a><span data-ttu-id="0e495-103">dcl \_ 輸入 vOutputControlPointID (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="0e495-103">dcl\_input vOutputControlPointID (sm5 - asm)</span></span>

<span data-ttu-id="0e495-104">在「輪廓著色器」控制點階段中宣告輸出控制點識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e495-104">Declare the output control point ID in a hull shader control point phase.</span></span>



| <span data-ttu-id="0e495-105">dcl \_ 輸入 vOutputControlPointID</span><span class="sxs-lookup"><span data-stu-id="0e495-105">dcl\_input vOutputControlPointID</span></span> |
|----------------------------------|



 



| <span data-ttu-id="0e495-106">項目</span><span class="sxs-lookup"><span data-stu-id="0e495-106">Item</span></span>                                                                                                                                                       | <span data-ttu-id="0e495-107">描述</span><span class="sxs-lookup"><span data-stu-id="0e495-107">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="0e495-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span><span class="sxs-lookup"><span data-stu-id="0e495-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span></span><br/> | <span data-ttu-id="0e495-109">\[在 \] 輸出控制點識別碼中。</span><span class="sxs-lookup"><span data-stu-id="0e495-109">\[in\] The output control point ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e495-110">備註</span><span class="sxs-lookup"><span data-stu-id="0e495-110">Remarks</span></span>

<span data-ttu-id="0e495-111">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="0e495-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0e495-112">頂點</span><span class="sxs-lookup"><span data-stu-id="0e495-112">Vertex</span></span> | <span data-ttu-id="0e495-113">船體</span><span class="sxs-lookup"><span data-stu-id="0e495-113">Hull</span></span> | <span data-ttu-id="0e495-114">網域</span><span class="sxs-lookup"><span data-stu-id="0e495-114">Domain</span></span> | <span data-ttu-id="0e495-115">幾何</span><span class="sxs-lookup"><span data-stu-id="0e495-115">Geometry</span></span> | <span data-ttu-id="0e495-116">像素</span><span class="sxs-lookup"><span data-stu-id="0e495-116">Pixel</span></span> | <span data-ttu-id="0e495-117">計算</span><span class="sxs-lookup"><span data-stu-id="0e495-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="0e495-118">X</span><span class="sxs-lookup"><span data-stu-id="0e495-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0e495-119">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0e495-119">Minimum Shader Model</span></span>

<span data-ttu-id="0e495-120">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="0e495-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0e495-121">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0e495-121">Shader Model</span></span>                                              | <span data-ttu-id="0e495-122">支援</span><span class="sxs-lookup"><span data-stu-id="0e495-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0e495-123">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="0e495-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0e495-124">是</span><span class="sxs-lookup"><span data-stu-id="0e495-124">yes</span></span>       |
| [<span data-ttu-id="0e495-125">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="0e495-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0e495-126">不可以</span><span class="sxs-lookup"><span data-stu-id="0e495-126">no</span></span>        |
| [<span data-ttu-id="0e495-127">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="0e495-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0e495-128">不可以</span><span class="sxs-lookup"><span data-stu-id="0e495-128">no</span></span>        |
| [<span data-ttu-id="0e495-129">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0e495-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0e495-130">不可以</span><span class="sxs-lookup"><span data-stu-id="0e495-130">no</span></span>        |
| [<span data-ttu-id="0e495-131">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0e495-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0e495-132">不可以</span><span class="sxs-lookup"><span data-stu-id="0e495-132">no</span></span>        |
| [<span data-ttu-id="0e495-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0e495-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0e495-134">不可以</span><span class="sxs-lookup"><span data-stu-id="0e495-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0e495-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e495-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e495-136">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0e495-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





