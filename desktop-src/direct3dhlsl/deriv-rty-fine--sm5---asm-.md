---
title: 'deriv_rty_fine (sm5-asm) '
description: '計算元件變更的速率。 |deriv_rty_fine (sm5-asm) '
ms.assetid: 7C5769A6-443C-4208-BD09-3DF3C5902624
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f0274fd04ae88ee412c95947691628754ba197
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991967"
---
# <a name="deriv_rty_fine-sm5---asm"></a><span data-ttu-id="b3b86-104">deriv \_ rty \_ 良好 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="b3b86-104">deriv\_rty\_fine (sm5 - asm)</span></span>

<span data-ttu-id="b3b86-105">計算元件變更的速率。</span><span class="sxs-lookup"><span data-stu-id="b3b86-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="b3b86-106">deriv \_ rty \_ 精細的 \[ \_ sat： \] \[ mask \] 、 \[ - \] src0 \[ \_ abs \] \[ swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="b3b86-106">deriv\_rty\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="b3b86-107">項目</span><span class="sxs-lookup"><span data-stu-id="b3b86-107">Item</span></span>                                                            | <span data-ttu-id="b3b86-108">描述</span><span class="sxs-lookup"><span data-stu-id="b3b86-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b3b86-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="b3b86-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b3b86-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="b3b86-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="b3b86-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b3b86-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b3b86-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="b3b86-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="b3b86-113">備註</span><span class="sxs-lookup"><span data-stu-id="b3b86-113">Remarks</span></span>

<span data-ttu-id="b3b86-114">如需詳細資訊，請參閱 [deriv \_ rtx \_ 良好。](deriv-rtx-fine--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="b3b86-114">For more information, see [deriv\_rtx\_fine.](deriv-rtx-fine--sm5---asm-.md)</span></span>

<span data-ttu-id="b3b86-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b3b86-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b3b86-116">頂點</span><span class="sxs-lookup"><span data-stu-id="b3b86-116">Vertex</span></span> | <span data-ttu-id="b3b86-117">船體</span><span class="sxs-lookup"><span data-stu-id="b3b86-117">Hull</span></span> | <span data-ttu-id="b3b86-118">網域</span><span class="sxs-lookup"><span data-stu-id="b3b86-118">Domain</span></span> | <span data-ttu-id="b3b86-119">幾何</span><span class="sxs-lookup"><span data-stu-id="b3b86-119">Geometry</span></span> | <span data-ttu-id="b3b86-120">像素</span><span class="sxs-lookup"><span data-stu-id="b3b86-120">Pixel</span></span> | <span data-ttu-id="b3b86-121">計算</span><span class="sxs-lookup"><span data-stu-id="b3b86-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b3b86-122">X</span><span class="sxs-lookup"><span data-stu-id="b3b86-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b3b86-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b3b86-123">Minimum Shader Model</span></span>

<span data-ttu-id="b3b86-124">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="b3b86-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b3b86-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b3b86-125">Shader Model</span></span>                                              | <span data-ttu-id="b3b86-126">支援</span><span class="sxs-lookup"><span data-stu-id="b3b86-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b3b86-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b3b86-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b3b86-128">是</span><span class="sxs-lookup"><span data-stu-id="b3b86-128">yes</span></span>       |
| [<span data-ttu-id="b3b86-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b3b86-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b3b86-130">不可以</span><span class="sxs-lookup"><span data-stu-id="b3b86-130">no</span></span>        |
| [<span data-ttu-id="b3b86-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b3b86-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b3b86-132">不可以</span><span class="sxs-lookup"><span data-stu-id="b3b86-132">no</span></span>        |
| [<span data-ttu-id="b3b86-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3b86-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b3b86-134">不可以</span><span class="sxs-lookup"><span data-stu-id="b3b86-134">no</span></span>        |
| [<span data-ttu-id="b3b86-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3b86-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b3b86-136">不可以</span><span class="sxs-lookup"><span data-stu-id="b3b86-136">no</span></span>        |
| [<span data-ttu-id="b3b86-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3b86-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b3b86-138">不可以</span><span class="sxs-lookup"><span data-stu-id="b3b86-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b3b86-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3b86-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3b86-140">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3b86-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





