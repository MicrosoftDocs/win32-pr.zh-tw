---
title: '否則 (sm4-asm) '
description: 啟動其他區塊。
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971601"
---
# <a name="else-sm4---asm"></a><span data-ttu-id="3a4f6-103">否則 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="3a4f6-103">else (sm4 - asm)</span></span>

<span data-ttu-id="3a4f6-104">啟動 **其他** 區塊。</span><span class="sxs-lookup"><span data-stu-id="3a4f6-104">Starts an **else** block.</span></span>



| <span data-ttu-id="3a4f6-105">else</span><span class="sxs-lookup"><span data-stu-id="3a4f6-105">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="3a4f6-106">備註</span><span class="sxs-lookup"><span data-stu-id="3a4f6-106">Remarks</span></span>

<span data-ttu-id="3a4f6-107">Token 格式會在著色器中包含對應的 [endif](endif--sm4---asm-.md) 指令位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="3a4f6-107">The token format contains the offset of the corresponding [endif](endif--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="3a4f6-108">下列範例顯示如何使用 **else** 指令。</span><span class="sxs-lookup"><span data-stu-id="3a4f6-108">The following example shows how to use the **else** instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="3a4f6-109">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="3a4f6-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3a4f6-110">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="3a4f6-110">Vertex Shader</span></span> | <span data-ttu-id="3a4f6-111">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="3a4f6-111">Geometry Shader</span></span> | <span data-ttu-id="3a4f6-112">像素著色器</span><span class="sxs-lookup"><span data-stu-id="3a4f6-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3a4f6-113">x</span><span class="sxs-lookup"><span data-stu-id="3a4f6-113">x</span></span>             | <span data-ttu-id="3a4f6-114">x</span><span class="sxs-lookup"><span data-stu-id="3a4f6-114">x</span></span>               | <span data-ttu-id="3a4f6-115">x</span><span class="sxs-lookup"><span data-stu-id="3a4f6-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a4f6-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3a4f6-116">Minimum Shader Model</span></span>

<span data-ttu-id="3a4f6-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3a4f6-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3a4f6-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3a4f6-118">Shader Model</span></span>                                              | <span data-ttu-id="3a4f6-119">支援</span><span class="sxs-lookup"><span data-stu-id="3a4f6-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a4f6-120">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3a4f6-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3a4f6-121">是</span><span class="sxs-lookup"><span data-stu-id="3a4f6-121">yes</span></span>       |
| [<span data-ttu-id="3a4f6-122">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="3a4f6-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3a4f6-123">是</span><span class="sxs-lookup"><span data-stu-id="3a4f6-123">yes</span></span>       |
| [<span data-ttu-id="3a4f6-124">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="3a4f6-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a4f6-125">是</span><span class="sxs-lookup"><span data-stu-id="3a4f6-125">yes</span></span>       |
| [<span data-ttu-id="3a4f6-126">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3a4f6-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a4f6-127">不可以</span><span class="sxs-lookup"><span data-stu-id="3a4f6-127">no</span></span>        |
| [<span data-ttu-id="3a4f6-128">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3a4f6-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a4f6-129">不可以</span><span class="sxs-lookup"><span data-stu-id="3a4f6-129">no</span></span>        |
| [<span data-ttu-id="3a4f6-130">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3a4f6-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a4f6-131">不可以</span><span class="sxs-lookup"><span data-stu-id="3a4f6-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a4f6-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a4f6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a4f6-133">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3a4f6-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




