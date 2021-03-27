---
title: '發出 (sm4-asm) '
description: 發出頂點。
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679104"
---
# <a name="emit-sm4---asm"></a><span data-ttu-id="ec6c3-103">發出 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="ec6c3-103">emit (sm4 - asm)</span></span>

<span data-ttu-id="ec6c3-104">發出頂點。</span><span class="sxs-lookup"><span data-stu-id="ec6c3-104">Emit a vertex.</span></span>



| <span data-ttu-id="ec6c3-105">發出</span><span class="sxs-lookup"><span data-stu-id="ec6c3-105">emit</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="ec6c3-106">備註</span><span class="sxs-lookup"><span data-stu-id="ec6c3-106">Remarks</span></span>

<span data-ttu-id="ec6c3-107">**發出** 會導致 \# 從幾何著色器讀取所有宣告的 o 暫存器，以產生頂點。</span><span class="sxs-lookup"><span data-stu-id="ec6c3-107">**emit** causes all declared o\# registers to be read out of the Geometry Shader to generate a vertex.</span></span>

<span data-ttu-id="ec6c3-108">發出多個 **發出** 呼叫時，會產生基本專案。</span><span class="sxs-lookup"><span data-stu-id="ec6c3-108">As multiple **emit** calls are issued, primitives are generated.</span></span>

<span data-ttu-id="ec6c3-109">**發出** 可能會在幾何著色器中出現任何次數，包括 flow 控制項。</span><span class="sxs-lookup"><span data-stu-id="ec6c3-109">**emit** can appear any number of times in a Geometry Shader, including within flow control.</span></span>

<span data-ttu-id="ec6c3-110">如果已宣告資料流程，您必須使用 [發出 \_ 資料流程](emit-stream--sm5---asm-.md)。</span><span class="sxs-lookup"><span data-stu-id="ec6c3-110">If streams have been declared, you must use [emit\_stream](emit-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="ec6c3-111">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ec6c3-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ec6c3-112">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="ec6c3-112">Vertex Shader</span></span> | <span data-ttu-id="ec6c3-113">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="ec6c3-113">Geometry Shader</span></span> | <span data-ttu-id="ec6c3-114">像素著色器</span><span class="sxs-lookup"><span data-stu-id="ec6c3-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="ec6c3-115">x</span><span class="sxs-lookup"><span data-stu-id="ec6c3-115">x</span></span>               |              |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="ec6c3-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ec6c3-116">Minimum Shader Model</span></span>

<span data-ttu-id="ec6c3-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ec6c3-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ec6c3-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ec6c3-118">Shader Model</span></span>                                              | <span data-ttu-id="ec6c3-119">支援</span><span class="sxs-lookup"><span data-stu-id="ec6c3-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ec6c3-120">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ec6c3-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ec6c3-121">是</span><span class="sxs-lookup"><span data-stu-id="ec6c3-121">yes</span></span>       |
| [<span data-ttu-id="ec6c3-122">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ec6c3-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ec6c3-123">是</span><span class="sxs-lookup"><span data-stu-id="ec6c3-123">yes</span></span>       |
| [<span data-ttu-id="ec6c3-124">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ec6c3-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ec6c3-125">是</span><span class="sxs-lookup"><span data-stu-id="ec6c3-125">yes</span></span>       |
| [<span data-ttu-id="ec6c3-126">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ec6c3-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ec6c3-127">不可以</span><span class="sxs-lookup"><span data-stu-id="ec6c3-127">no</span></span>        |
| [<span data-ttu-id="ec6c3-128">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ec6c3-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ec6c3-129">不可以</span><span class="sxs-lookup"><span data-stu-id="ec6c3-129">no</span></span>        |
| [<span data-ttu-id="ec6c3-130">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ec6c3-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ec6c3-131">不可以</span><span class="sxs-lookup"><span data-stu-id="ec6c3-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ec6c3-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec6c3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec6c3-133">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ec6c3-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




