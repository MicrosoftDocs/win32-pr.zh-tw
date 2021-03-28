---
title: 'emitThenCut (sm4-asm) '
description: '相當於發出命令，後面接著剪下命令。 |emitThenCut (sm4-asm) '
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322520"
---
# <a name="emitthencut-sm4---asm"></a><span data-ttu-id="3582a-104">emitThenCut (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="3582a-104">emitThenCut (sm4 - asm)</span></span>

<span data-ttu-id="3582a-105">相當於 [發出](emit--sm4---asm-.md) 命令，後面接著 [剪](cut--sm4---asm-.md) 下命令。</span><span class="sxs-lookup"><span data-stu-id="3582a-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="3582a-106">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="3582a-106">emitThenCut</span></span> |
|-------------|



 

## <a name="remarks"></a><span data-ttu-id="3582a-107">備註</span><span class="sxs-lookup"><span data-stu-id="3582a-107">Remarks</span></span>

<span data-ttu-id="3582a-108">當故意輸出拓撲中的最後一個頂點時，此命令很有用。</span><span class="sxs-lookup"><span data-stu-id="3582a-108">This command is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="3582a-109">如果已宣告資料流程，您必須使用 [emitthencut \_ 資料流程](emitthencut-stream--sm5---asm-.md)。</span><span class="sxs-lookup"><span data-stu-id="3582a-109">If streams have been declared, you must use [emitthencut\_stream](emitthencut-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="3582a-110">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="3582a-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3582a-111">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="3582a-111">Vertex Shader</span></span> | <span data-ttu-id="3582a-112">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="3582a-112">Geometry Shader</span></span> | <span data-ttu-id="3582a-113">像素著色器</span><span class="sxs-lookup"><span data-stu-id="3582a-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="3582a-114">x</span><span class="sxs-lookup"><span data-stu-id="3582a-114">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3582a-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3582a-115">Minimum Shader Model</span></span>

<span data-ttu-id="3582a-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3582a-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3582a-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3582a-117">Shader Model</span></span>                                              | <span data-ttu-id="3582a-118">支援</span><span class="sxs-lookup"><span data-stu-id="3582a-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3582a-119">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3582a-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3582a-120">是</span><span class="sxs-lookup"><span data-stu-id="3582a-120">yes</span></span>       |
| [<span data-ttu-id="3582a-121">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="3582a-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3582a-122">是</span><span class="sxs-lookup"><span data-stu-id="3582a-122">yes</span></span>       |
| [<span data-ttu-id="3582a-123">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="3582a-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3582a-124">是</span><span class="sxs-lookup"><span data-stu-id="3582a-124">yes</span></span>       |
| [<span data-ttu-id="3582a-125">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3582a-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3582a-126">不可以</span><span class="sxs-lookup"><span data-stu-id="3582a-126">no</span></span>        |
| [<span data-ttu-id="3582a-127">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3582a-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3582a-128">不可以</span><span class="sxs-lookup"><span data-stu-id="3582a-128">no</span></span>        |
| [<span data-ttu-id="3582a-129">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3582a-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3582a-130">不可以</span><span class="sxs-lookup"><span data-stu-id="3582a-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3582a-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="3582a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3582a-132">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3582a-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




