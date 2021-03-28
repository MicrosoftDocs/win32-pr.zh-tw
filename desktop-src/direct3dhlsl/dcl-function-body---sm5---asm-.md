---
title: 'dcl_function_body (sm5-asm) '
description: 宣告函數主體。
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092469"
---
# <a name="dcl_function_body-sm5---asm"></a><span data-ttu-id="4041d-103">\_ \_ (的 dcl 函數主體) sm5-asm</span><span class="sxs-lookup"><span data-stu-id="4041d-103">dcl\_function\_body (sm5 - asm)</span></span>

<span data-ttu-id="4041d-104">宣告函數主體。</span><span class="sxs-lookup"><span data-stu-id="4041d-104">Declare a function body.</span></span>



| <span data-ttu-id="4041d-105">dcl \_ 函數 \_ 主體 fb\#</span><span class="sxs-lookup"><span data-stu-id="4041d-105">dcl\_function\_body fb\#</span></span> |
|--------------------------|



 



| <span data-ttu-id="4041d-106">項目</span><span class="sxs-lookup"><span data-stu-id="4041d-106">Item</span></span>                                                          | <span data-ttu-id="4041d-107">描述</span><span class="sxs-lookup"><span data-stu-id="4041d-107">Description</span></span>                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="4041d-108"><span id="fb_"></span><span id="FB_"></span>*Fb\#*</span><span class="sxs-lookup"><span data-stu-id="4041d-108"><span id="fb_"></span><span id="FB_"></span>*fb\#*</span></span><br/> | <span data-ttu-id="4041d-109">\[在將出現函式 \] 之位置的標籤中。</span><span class="sxs-lookup"><span data-stu-id="4041d-109">\[in\] The label of the place where the function will appear.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4041d-110">備註</span><span class="sxs-lookup"><span data-stu-id="4041d-110">Remarks</span></span>

<span data-ttu-id="4041d-111">此指令宣告了唯一的函式主體，其程式碼稍後會在標籤為 fb 的程式中顯示 \# 。</span><span class="sxs-lookup"><span data-stu-id="4041d-111">This instruction declares a unique function body whose code will appear later in the program at label fb\#.</span></span>

<span data-ttu-id="4041d-112">函數主體用於函數表聲明中。</span><span class="sxs-lookup"><span data-stu-id="4041d-112">Function bodies are used in function table declarations.</span></span> <span data-ttu-id="4041d-113">如需詳細資訊，請參閱 [dcl \_ 函數 \_ 表](dcl-function-table---sm5---asm-.md)。</span><span class="sxs-lookup"><span data-stu-id="4041d-113">For more info, see [dcl\_function\_table](dcl-function-table---sm5---asm-.md).</span></span>

<span data-ttu-id="4041d-114">在輪廓著色器和網域著色器中，其中有多個階段 (控制點階段、分支階段和聯結階段) ，所有的函式主體 (標籤 fb \#) 會出現在所有階段之後，而不是依階段分組。</span><span class="sxs-lookup"><span data-stu-id="4041d-114">In the hull shader and domain shader, where there are multiple phases (control point phase, fork phase, and join phase), all function bodies (label fb\#) appear after all the phases, rather than being grouped by phase.</span></span>

<span data-ttu-id="4041d-115">有多少個函數主體可以存在。</span><span class="sxs-lookup"><span data-stu-id="4041d-115">There is no limit to how many function bodies can be present.</span></span>

<span data-ttu-id="4041d-116">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4041d-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4041d-117">頂點</span><span class="sxs-lookup"><span data-stu-id="4041d-117">Vertex</span></span> | <span data-ttu-id="4041d-118">船體</span><span class="sxs-lookup"><span data-stu-id="4041d-118">Hull</span></span> | <span data-ttu-id="4041d-119">網域</span><span class="sxs-lookup"><span data-stu-id="4041d-119">Domain</span></span> | <span data-ttu-id="4041d-120">幾何</span><span class="sxs-lookup"><span data-stu-id="4041d-120">Geometry</span></span> | <span data-ttu-id="4041d-121">像素</span><span class="sxs-lookup"><span data-stu-id="4041d-121">Pixel</span></span> | <span data-ttu-id="4041d-122">計算</span><span class="sxs-lookup"><span data-stu-id="4041d-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4041d-123">X</span><span class="sxs-lookup"><span data-stu-id="4041d-123">X</span></span>      | <span data-ttu-id="4041d-124">X</span><span class="sxs-lookup"><span data-stu-id="4041d-124">X</span></span>    | <span data-ttu-id="4041d-125">X</span><span class="sxs-lookup"><span data-stu-id="4041d-125">X</span></span>      | <span data-ttu-id="4041d-126">X</span><span class="sxs-lookup"><span data-stu-id="4041d-126">X</span></span>        | <span data-ttu-id="4041d-127">X</span><span class="sxs-lookup"><span data-stu-id="4041d-127">X</span></span>     | <span data-ttu-id="4041d-128">X</span><span class="sxs-lookup"><span data-stu-id="4041d-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4041d-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4041d-129">Minimum Shader Model</span></span>

<span data-ttu-id="4041d-130">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="4041d-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4041d-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4041d-131">Shader Model</span></span>                                              | <span data-ttu-id="4041d-132">支援</span><span class="sxs-lookup"><span data-stu-id="4041d-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4041d-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4041d-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4041d-134">是</span><span class="sxs-lookup"><span data-stu-id="4041d-134">yes</span></span>       |
| [<span data-ttu-id="4041d-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4041d-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4041d-136">不可以</span><span class="sxs-lookup"><span data-stu-id="4041d-136">no</span></span>        |
| [<span data-ttu-id="4041d-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4041d-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4041d-138">不可以</span><span class="sxs-lookup"><span data-stu-id="4041d-138">no</span></span>        |
| [<span data-ttu-id="4041d-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4041d-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4041d-140">不可以</span><span class="sxs-lookup"><span data-stu-id="4041d-140">no</span></span>        |
| [<span data-ttu-id="4041d-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4041d-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4041d-142">不可以</span><span class="sxs-lookup"><span data-stu-id="4041d-142">no</span></span>        |
| [<span data-ttu-id="4041d-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4041d-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4041d-144">不可以</span><span class="sxs-lookup"><span data-stu-id="4041d-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4041d-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="4041d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4041d-146">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4041d-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





