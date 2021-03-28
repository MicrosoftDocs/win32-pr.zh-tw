---
title: 'endloop (sm4-asm) '
description: 結束迴圈語句。
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655fa6addd19a6ce9f6f6b20a2677ef43cb8b751
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373690"
---
# <a name="endloop-sm4---asm"></a><span data-ttu-id="c66e4-103">endloop (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="c66e4-103">endloop (sm4 - asm)</span></span>

<span data-ttu-id="c66e4-104">結束迴圈語句。</span><span class="sxs-lookup"><span data-stu-id="c66e4-104">Ends a loop statement.</span></span>



| <span data-ttu-id="c66e4-105">endloop</span><span class="sxs-lookup"><span data-stu-id="c66e4-105">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="c66e4-106">備註</span><span class="sxs-lookup"><span data-stu-id="c66e4-106">Remarks</span></span>

<span data-ttu-id="c66e4-107">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="c66e4-107">The following example shows how to use this instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="c66e4-108">Token 格式包含著色器中對應迴圈指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="c66e4-108">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="c66e4-109">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="c66e4-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c66e4-110">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="c66e4-110">Vertex Shader</span></span> | <span data-ttu-id="c66e4-111">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="c66e4-111">Geometry Shader</span></span> | <span data-ttu-id="c66e4-112">像素著色器</span><span class="sxs-lookup"><span data-stu-id="c66e4-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c66e4-113">x</span><span class="sxs-lookup"><span data-stu-id="c66e4-113">x</span></span>             | <span data-ttu-id="c66e4-114">x</span><span class="sxs-lookup"><span data-stu-id="c66e4-114">x</span></span>               | <span data-ttu-id="c66e4-115">x</span><span class="sxs-lookup"><span data-stu-id="c66e4-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c66e4-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c66e4-116">Minimum Shader Model</span></span>

<span data-ttu-id="c66e4-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="c66e4-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c66e4-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c66e4-118">Shader Model</span></span>                                              | <span data-ttu-id="c66e4-119">支援</span><span class="sxs-lookup"><span data-stu-id="c66e4-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c66e4-120">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c66e4-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c66e4-121">是</span><span class="sxs-lookup"><span data-stu-id="c66e4-121">yes</span></span>       |
| [<span data-ttu-id="c66e4-122">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="c66e4-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c66e4-123">是</span><span class="sxs-lookup"><span data-stu-id="c66e4-123">yes</span></span>       |
| [<span data-ttu-id="c66e4-124">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="c66e4-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c66e4-125">是</span><span class="sxs-lookup"><span data-stu-id="c66e4-125">yes</span></span>       |
| [<span data-ttu-id="c66e4-126">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c66e4-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c66e4-127">不可以</span><span class="sxs-lookup"><span data-stu-id="c66e4-127">no</span></span>        |
| [<span data-ttu-id="c66e4-128">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c66e4-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c66e4-129">不可以</span><span class="sxs-lookup"><span data-stu-id="c66e4-129">no</span></span>        |
| [<span data-ttu-id="c66e4-130">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c66e4-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c66e4-131">不可以</span><span class="sxs-lookup"><span data-stu-id="c66e4-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c66e4-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="c66e4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c66e4-133">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c66e4-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




