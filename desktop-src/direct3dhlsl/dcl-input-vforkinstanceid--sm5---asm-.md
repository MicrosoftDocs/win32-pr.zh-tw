---
title: 'dcl_input vForkInstanceID (sm5-asm) '
description: 在輪廓著色器分叉階段中宣告實例識別碼。
ms.assetid: AA73E8B6-C6D7-4483-B46E-C733341F552C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ce5fcf111a59abb0c9a6ccb36de63d94dcb11e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022861"
---
# <a name="dcl_input-vforkinstanceid-sm5---asm"></a><span data-ttu-id="50812-103">dcl \_ 輸入 vForkInstanceID (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="50812-103">dcl\_input vForkInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="50812-104">在輪廓著色器分叉階段中宣告實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="50812-104">Declare the instance ID in a hull shader fork phase.</span></span>



| <span data-ttu-id="50812-105">dcl \_ 輸入 vForkInstanceID</span><span class="sxs-lookup"><span data-stu-id="50812-105">dcl\_input vForkInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="50812-106">項目</span><span class="sxs-lookup"><span data-stu-id="50812-106">Item</span></span>                                                                                                                               | <span data-ttu-id="50812-107">描述</span><span class="sxs-lookup"><span data-stu-id="50812-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="50812-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span><span class="sxs-lookup"><span data-stu-id="50812-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span></span><br/> | <span data-ttu-id="50812-109">\[在 \] 實例識別碼中。</span><span class="sxs-lookup"><span data-stu-id="50812-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50812-110">備註</span><span class="sxs-lookup"><span data-stu-id="50812-110">Remarks</span></span>

<span data-ttu-id="50812-111">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="50812-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="50812-112">頂點</span><span class="sxs-lookup"><span data-stu-id="50812-112">Vertex</span></span> | <span data-ttu-id="50812-113">船體</span><span class="sxs-lookup"><span data-stu-id="50812-113">Hull</span></span> | <span data-ttu-id="50812-114">網域</span><span class="sxs-lookup"><span data-stu-id="50812-114">Domain</span></span> | <span data-ttu-id="50812-115">幾何</span><span class="sxs-lookup"><span data-stu-id="50812-115">Geometry</span></span> | <span data-ttu-id="50812-116">像素</span><span class="sxs-lookup"><span data-stu-id="50812-116">Pixel</span></span> | <span data-ttu-id="50812-117">計算</span><span class="sxs-lookup"><span data-stu-id="50812-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="50812-118">X</span><span class="sxs-lookup"><span data-stu-id="50812-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="50812-119">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="50812-119">Minimum Shader Model</span></span>

<span data-ttu-id="50812-120">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="50812-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="50812-121">著色器模型</span><span class="sxs-lookup"><span data-stu-id="50812-121">Shader Model</span></span>                                              | <span data-ttu-id="50812-122">支援</span><span class="sxs-lookup"><span data-stu-id="50812-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="50812-123">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="50812-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="50812-124">是</span><span class="sxs-lookup"><span data-stu-id="50812-124">yes</span></span>       |
| [<span data-ttu-id="50812-125">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="50812-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="50812-126">不可以</span><span class="sxs-lookup"><span data-stu-id="50812-126">no</span></span>        |
| [<span data-ttu-id="50812-127">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="50812-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="50812-128">不可以</span><span class="sxs-lookup"><span data-stu-id="50812-128">no</span></span>        |
| [<span data-ttu-id="50812-129">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50812-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="50812-130">不可以</span><span class="sxs-lookup"><span data-stu-id="50812-130">no</span></span>        |
| [<span data-ttu-id="50812-131">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50812-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="50812-132">不可以</span><span class="sxs-lookup"><span data-stu-id="50812-132">no</span></span>        |
| [<span data-ttu-id="50812-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50812-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="50812-134">不可以</span><span class="sxs-lookup"><span data-stu-id="50812-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="50812-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="50812-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50812-136">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50812-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





