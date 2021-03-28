---
title: 'hs_fork_phase (sm5-asm) '
description: 在輪廓著色器中啟動「分叉」階段。
ms.assetid: 13D6A06C-F001-45BE-8AB4-D7ACA73BF535
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9316cc92c1bf5683afa620927b3c6f38432c3c4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373871"
---
# <a name="hs_fork_phase-sm5---asm"></a><span data-ttu-id="1c5b1-103">hs \_ 分叉 \_ 階段 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="1c5b1-103">hs\_fork\_phase (sm5 - asm)</span></span>

<span data-ttu-id="1c5b1-104">在輪廓著色器中啟動「分叉」階段。</span><span class="sxs-lookup"><span data-stu-id="1c5b1-104">Start the fork phase in a hull shader.</span></span>



| <span data-ttu-id="1c5b1-105">hs \_ 分叉 \_ 階段</span><span class="sxs-lookup"><span data-stu-id="1c5b1-105">hs\_fork\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="1c5b1-106">備註</span><span class="sxs-lookup"><span data-stu-id="1c5b1-106">Remarks</span></span>

<span data-ttu-id="1c5b1-107">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="1c5b1-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1c5b1-108">頂點</span><span class="sxs-lookup"><span data-stu-id="1c5b1-108">Vertex</span></span> | <span data-ttu-id="1c5b1-109">船體</span><span class="sxs-lookup"><span data-stu-id="1c5b1-109">Hull</span></span> | <span data-ttu-id="1c5b1-110">網域</span><span class="sxs-lookup"><span data-stu-id="1c5b1-110">Domain</span></span> | <span data-ttu-id="1c5b1-111">幾何</span><span class="sxs-lookup"><span data-stu-id="1c5b1-111">Geometry</span></span> | <span data-ttu-id="1c5b1-112">像素</span><span class="sxs-lookup"><span data-stu-id="1c5b1-112">Pixel</span></span> | <span data-ttu-id="1c5b1-113">計算</span><span class="sxs-lookup"><span data-stu-id="1c5b1-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="1c5b1-114">X</span><span class="sxs-lookup"><span data-stu-id="1c5b1-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c5b1-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1c5b1-115">Minimum Shader Model</span></span>

<span data-ttu-id="1c5b1-116">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="1c5b1-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1c5b1-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1c5b1-117">Shader Model</span></span>                                              | <span data-ttu-id="1c5b1-118">支援</span><span class="sxs-lookup"><span data-stu-id="1c5b1-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1c5b1-119">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1c5b1-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1c5b1-120">是</span><span class="sxs-lookup"><span data-stu-id="1c5b1-120">yes</span></span>       |
| [<span data-ttu-id="1c5b1-121">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="1c5b1-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1c5b1-122">不可以</span><span class="sxs-lookup"><span data-stu-id="1c5b1-122">no</span></span>        |
| [<span data-ttu-id="1c5b1-123">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1c5b1-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1c5b1-124">不可以</span><span class="sxs-lookup"><span data-stu-id="1c5b1-124">no</span></span>        |
| [<span data-ttu-id="1c5b1-125">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1c5b1-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1c5b1-126">不可以</span><span class="sxs-lookup"><span data-stu-id="1c5b1-126">no</span></span>        |
| [<span data-ttu-id="1c5b1-127">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1c5b1-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1c5b1-128">不可以</span><span class="sxs-lookup"><span data-stu-id="1c5b1-128">no</span></span>        |
| [<span data-ttu-id="1c5b1-129">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1c5b1-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1c5b1-130">不可以</span><span class="sxs-lookup"><span data-stu-id="1c5b1-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1c5b1-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c5b1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c5b1-132">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1c5b1-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




