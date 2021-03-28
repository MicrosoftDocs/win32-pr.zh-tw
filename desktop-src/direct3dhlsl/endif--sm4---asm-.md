---
title: 'endif (sm4-asm) '
description: 結束 if 語句。
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fa6cf0efd395843212f6bacac478285e496c2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022790"
---
# <a name="endif-sm4---asm"></a><span data-ttu-id="cec4b-103">endif (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="cec4b-103">endif (sm4 - asm)</span></span>

<span data-ttu-id="cec4b-104">結束 [if](if--sm4---asm-.md) 語句。</span><span class="sxs-lookup"><span data-stu-id="cec4b-104">Ends an [if](if--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="cec4b-105">endif</span><span class="sxs-lookup"><span data-stu-id="cec4b-105">endif</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="cec4b-106">備註</span><span class="sxs-lookup"><span data-stu-id="cec4b-106">Remarks</span></span>

<span data-ttu-id="cec4b-107">下列範例顯示如何使用 endif 指令。</span><span class="sxs-lookup"><span data-stu-id="cec4b-107">The following example shows how to use the endif instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="cec4b-108">Token 格式包含著色器中對應 **if** 指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="cec4b-108">The token format contains the offset of the corresponding **if** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="cec4b-109">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="cec4b-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cec4b-110">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="cec4b-110">Vertex Shader</span></span> | <span data-ttu-id="cec4b-111">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="cec4b-111">Geometry Shader</span></span> | <span data-ttu-id="cec4b-112">像素著色器</span><span class="sxs-lookup"><span data-stu-id="cec4b-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cec4b-113">x</span><span class="sxs-lookup"><span data-stu-id="cec4b-113">x</span></span>             | <span data-ttu-id="cec4b-114">x</span><span class="sxs-lookup"><span data-stu-id="cec4b-114">x</span></span>               | <span data-ttu-id="cec4b-115">x</span><span class="sxs-lookup"><span data-stu-id="cec4b-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cec4b-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="cec4b-116">Minimum Shader Model</span></span>

<span data-ttu-id="cec4b-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="cec4b-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cec4b-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="cec4b-118">Shader Model</span></span>                                              | <span data-ttu-id="cec4b-119">支援</span><span class="sxs-lookup"><span data-stu-id="cec4b-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cec4b-120">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="cec4b-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cec4b-121">是</span><span class="sxs-lookup"><span data-stu-id="cec4b-121">yes</span></span>       |
| [<span data-ttu-id="cec4b-122">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="cec4b-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cec4b-123">是</span><span class="sxs-lookup"><span data-stu-id="cec4b-123">yes</span></span>       |
| [<span data-ttu-id="cec4b-124">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="cec4b-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cec4b-125">是</span><span class="sxs-lookup"><span data-stu-id="cec4b-125">yes</span></span>       |
| [<span data-ttu-id="cec4b-126">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cec4b-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cec4b-127">不可以</span><span class="sxs-lookup"><span data-stu-id="cec4b-127">no</span></span>        |
| [<span data-ttu-id="cec4b-128">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cec4b-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cec4b-129">不可以</span><span class="sxs-lookup"><span data-stu-id="cec4b-129">no</span></span>        |
| [<span data-ttu-id="cec4b-130">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cec4b-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cec4b-131">不可以</span><span class="sxs-lookup"><span data-stu-id="cec4b-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cec4b-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="cec4b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cec4b-133">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cec4b-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




