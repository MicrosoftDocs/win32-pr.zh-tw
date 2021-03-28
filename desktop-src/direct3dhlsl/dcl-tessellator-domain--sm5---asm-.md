---
title: 'dcl_tessellator_domain (sm5-asm) '
description: 在 [輪廓著色器宣告] 區段和網域著色器中宣告鑲嵌網域。
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373902"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a><span data-ttu-id="f1424-103">dcl \_ 鑲嵌 \_ 網域 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="f1424-103">dcl\_tessellator\_domain (sm5 - asm)</span></span>

<span data-ttu-id="f1424-104">在 [輪廓著色器宣告] 區段和網域著色器中宣告鑲嵌網域。</span><span class="sxs-lookup"><span data-stu-id="f1424-104">Declare the tessellator domain in a hull shader declaration section, and the domain shader.</span></span>



| <span data-ttu-id="f1424-105">dcl \_ 鑲嵌 \_ 網域 {網域 \_ 等值線 </span><span class="sxs-lookup"><span data-stu-id="f1424-105">dcl\_tessellator\_domain {domain\_isoline </span></span>\| <span data-ttu-id="f1424-106">網域 \_ 三</span><span class="sxs-lookup"><span data-stu-id="f1424-106">domain\_tri \</span></span>| <span data-ttu-id="f1424-107">網域 \_ 四個</span><span class="sxs-lookup"><span data-stu-id="f1424-107">domain\_quad}</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="f1424-108">項目</span><span class="sxs-lookup"><span data-stu-id="f1424-108">Item</span></span>                                                                                                                                                                                | <span data-ttu-id="f1424-109">描述</span><span class="sxs-lookup"><span data-stu-id="f1424-109">Description</span></span>                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="f1424-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*網域 \_ 等值線 \| 網域 \_ 三個 \| 網域 \_ 四個*</span><span class="sxs-lookup"><span data-stu-id="f1424-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain\_isoline \| domain\_tri \| domain\_quad*</span></span><br/> | <span data-ttu-id="f1424-111">\[在 \] 網域中。</span><span class="sxs-lookup"><span data-stu-id="f1424-111">\[in\] The domain.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1424-112">備註</span><span class="sxs-lookup"><span data-stu-id="f1424-112">Remarks</span></span>

<span data-ttu-id="f1424-113">如果輪廓著色器和網域著色器提供不相符的網域或任何其他衝突的 decalarations，則行為是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f1424-113">Behavior is undefined if the hull shader and domain shader provide mismatching domains or any other conflicting decalarations.</span></span>

<span data-ttu-id="f1424-114">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f1424-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f1424-115">頂點</span><span class="sxs-lookup"><span data-stu-id="f1424-115">Vertex</span></span> | <span data-ttu-id="f1424-116">船體</span><span class="sxs-lookup"><span data-stu-id="f1424-116">Hull</span></span>                 | <span data-ttu-id="f1424-117">網域</span><span class="sxs-lookup"><span data-stu-id="f1424-117">Domain</span></span> | <span data-ttu-id="f1424-118">幾何</span><span class="sxs-lookup"><span data-stu-id="f1424-118">Geometry</span></span> | <span data-ttu-id="f1424-119">像素</span><span class="sxs-lookup"><span data-stu-id="f1424-119">Pixel</span></span> | <span data-ttu-id="f1424-120">計算</span><span class="sxs-lookup"><span data-stu-id="f1424-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="f1424-121">宣告區段</span><span class="sxs-lookup"><span data-stu-id="f1424-121">Declarations Section</span></span> | <span data-ttu-id="f1424-122">X</span><span class="sxs-lookup"><span data-stu-id="f1424-122">X</span></span>      |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f1424-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f1424-123">Minimum Shader Model</span></span>

<span data-ttu-id="f1424-124">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="f1424-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f1424-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f1424-125">Shader Model</span></span>                                              | <span data-ttu-id="f1424-126">支援</span><span class="sxs-lookup"><span data-stu-id="f1424-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f1424-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f1424-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f1424-128">是</span><span class="sxs-lookup"><span data-stu-id="f1424-128">yes</span></span>       |
| [<span data-ttu-id="f1424-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f1424-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f1424-130">不可以</span><span class="sxs-lookup"><span data-stu-id="f1424-130">no</span></span>        |
| [<span data-ttu-id="f1424-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f1424-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f1424-132">不可以</span><span class="sxs-lookup"><span data-stu-id="f1424-132">no</span></span>        |
| [<span data-ttu-id="f1424-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f1424-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f1424-134">不可以</span><span class="sxs-lookup"><span data-stu-id="f1424-134">no</span></span>        |
| [<span data-ttu-id="f1424-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f1424-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f1424-136">不可以</span><span class="sxs-lookup"><span data-stu-id="f1424-136">no</span></span>        |
| [<span data-ttu-id="f1424-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f1424-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f1424-138">不可以</span><span class="sxs-lookup"><span data-stu-id="f1424-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f1424-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1424-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1424-140">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f1424-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





