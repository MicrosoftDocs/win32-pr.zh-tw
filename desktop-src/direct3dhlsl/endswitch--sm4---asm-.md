---
title: 'endswitch (sm4-asm) '
description: 結束 switch 語句。
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523a4008ab976ee299758349d57c6e32a3f336b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373687"
---
# <a name="endswitch-sm4---asm"></a><span data-ttu-id="d2490-103">endswitch (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="d2490-103">endswitch (sm4 - asm)</span></span>

<span data-ttu-id="d2490-104">結束 [switch](switch--sm4---asm-.md) 語句。</span><span class="sxs-lookup"><span data-stu-id="d2490-104">Ends a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="d2490-105">endswitch</span><span class="sxs-lookup"><span data-stu-id="d2490-105">endswitch</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="d2490-106">備註</span><span class="sxs-lookup"><span data-stu-id="d2490-106">Remarks</span></span>

<span data-ttu-id="d2490-107">Token 格式包含著色器中對應 switch 指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="d2490-107">The token format contains the offset of the corresponding switch instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="d2490-108">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d2490-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d2490-109">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="d2490-109">Vertex Shader</span></span> | <span data-ttu-id="d2490-110">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="d2490-110">Geometry Shader</span></span> | <span data-ttu-id="d2490-111">像素著色器</span><span class="sxs-lookup"><span data-stu-id="d2490-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d2490-112">x</span><span class="sxs-lookup"><span data-stu-id="d2490-112">x</span></span>             | <span data-ttu-id="d2490-113">x</span><span class="sxs-lookup"><span data-stu-id="d2490-113">x</span></span>               | <span data-ttu-id="d2490-114">x</span><span class="sxs-lookup"><span data-stu-id="d2490-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d2490-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d2490-115">Minimum Shader Model</span></span>

<span data-ttu-id="d2490-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d2490-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2490-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d2490-117">Shader Model</span></span>                                              | <span data-ttu-id="d2490-118">支援</span><span class="sxs-lookup"><span data-stu-id="d2490-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d2490-119">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d2490-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d2490-120">是</span><span class="sxs-lookup"><span data-stu-id="d2490-120">yes</span></span>       |
| [<span data-ttu-id="d2490-121">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d2490-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d2490-122">是</span><span class="sxs-lookup"><span data-stu-id="d2490-122">yes</span></span>       |
| [<span data-ttu-id="d2490-123">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d2490-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d2490-124">是</span><span class="sxs-lookup"><span data-stu-id="d2490-124">yes</span></span>       |
| [<span data-ttu-id="d2490-125">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2490-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d2490-126">不可以</span><span class="sxs-lookup"><span data-stu-id="d2490-126">no</span></span>        |
| [<span data-ttu-id="d2490-127">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2490-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d2490-128">不可以</span><span class="sxs-lookup"><span data-stu-id="d2490-128">no</span></span>        |
| [<span data-ttu-id="d2490-129">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2490-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d2490-130">不可以</span><span class="sxs-lookup"><span data-stu-id="d2490-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d2490-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2490-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2490-132">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d2490-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




