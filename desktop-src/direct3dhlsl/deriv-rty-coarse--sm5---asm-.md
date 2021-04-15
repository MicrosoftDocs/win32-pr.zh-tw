---
title: 'deriv_rty_coarse (sm5-asm) '
description: '計算元件變更的速率。 |deriv_rty_coarse (sm5-asm) '
ms.assetid: 1EBCC0B9-BD3E-46DD-AC17-F7167F892195
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7fd539adf8587118a6bdfdcb5959925e6a97f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992026"
---
# <a name="deriv_rty_coarse-sm5---asm"></a><span data-ttu-id="05fb6-104">deriv \_ rty \_ 粗略 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="05fb6-104">deriv\_rty\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="05fb6-105">計算元件變更的速率。</span><span class="sxs-lookup"><span data-stu-id="05fb6-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="05fb6-106">deriv \_ rty \_ 粗略 \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="05fb6-106">deriv\_rty\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="05fb6-107">項目</span><span class="sxs-lookup"><span data-stu-id="05fb6-107">Item</span></span>                                                            | <span data-ttu-id="05fb6-108">描述</span><span class="sxs-lookup"><span data-stu-id="05fb6-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="05fb6-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="05fb6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="05fb6-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="05fb6-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="05fb6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="05fb6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="05fb6-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="05fb6-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="05fb6-113">備註</span><span class="sxs-lookup"><span data-stu-id="05fb6-113">Remarks</span></span>

<span data-ttu-id="05fb6-114">如需詳細資訊，請參閱 [deriv \_ rtx \_ 粗糙。](deriv-rtx-coarse--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="05fb6-114">For more information, see [deriv\_rtx\_coarse.](deriv-rtx-coarse--sm5---asm-.md)</span></span>

<span data-ttu-id="05fb6-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="05fb6-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="05fb6-116">頂點</span><span class="sxs-lookup"><span data-stu-id="05fb6-116">Vertex</span></span> | <span data-ttu-id="05fb6-117">船體</span><span class="sxs-lookup"><span data-stu-id="05fb6-117">Hull</span></span> | <span data-ttu-id="05fb6-118">網域</span><span class="sxs-lookup"><span data-stu-id="05fb6-118">Domain</span></span> | <span data-ttu-id="05fb6-119">幾何</span><span class="sxs-lookup"><span data-stu-id="05fb6-119">Geometry</span></span> | <span data-ttu-id="05fb6-120">像素</span><span class="sxs-lookup"><span data-stu-id="05fb6-120">Pixel</span></span> | <span data-ttu-id="05fb6-121">計算</span><span class="sxs-lookup"><span data-stu-id="05fb6-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="05fb6-122">X</span><span class="sxs-lookup"><span data-stu-id="05fb6-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="05fb6-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="05fb6-123">Minimum Shader Model</span></span>

<span data-ttu-id="05fb6-124">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="05fb6-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="05fb6-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="05fb6-125">Shader Model</span></span>                                              | <span data-ttu-id="05fb6-126">支援</span><span class="sxs-lookup"><span data-stu-id="05fb6-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="05fb6-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="05fb6-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="05fb6-128">是</span><span class="sxs-lookup"><span data-stu-id="05fb6-128">yes</span></span>       |
| [<span data-ttu-id="05fb6-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="05fb6-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="05fb6-130">不可以</span><span class="sxs-lookup"><span data-stu-id="05fb6-130">no</span></span>        |
| [<span data-ttu-id="05fb6-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="05fb6-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="05fb6-132">不可以</span><span class="sxs-lookup"><span data-stu-id="05fb6-132">no</span></span>        |
| [<span data-ttu-id="05fb6-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="05fb6-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="05fb6-134">不可以</span><span class="sxs-lookup"><span data-stu-id="05fb6-134">no</span></span>        |
| [<span data-ttu-id="05fb6-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="05fb6-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="05fb6-136">不可以</span><span class="sxs-lookup"><span data-stu-id="05fb6-136">no</span></span>        |
| [<span data-ttu-id="05fb6-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="05fb6-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="05fb6-138">不可以</span><span class="sxs-lookup"><span data-stu-id="05fb6-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="05fb6-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="05fb6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05fb6-140">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="05fb6-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





