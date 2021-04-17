---
title: '繼續 (sm4-asm) '
description: 在目前迴圈的開頭繼續執行。
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53b023e998fcf131a387fc009cfc8cb133ff6a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990755"
---
# <a name="continue-sm4---asm"></a><span data-ttu-id="b3803-103">繼續 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="b3803-103">continue (sm4 - asm)</span></span>

<span data-ttu-id="b3803-104">在目前迴圈的開頭繼續執行。</span><span class="sxs-lookup"><span data-stu-id="b3803-104">Continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="b3803-105">continue</span><span class="sxs-lookup"><span data-stu-id="b3803-105">continue</span></span> |
|----------|



 

## <a name="remarks"></a><span data-ttu-id="b3803-106">備註</span><span class="sxs-lookup"><span data-stu-id="b3803-106">Remarks</span></span>

<span data-ttu-id="b3803-107">**continue** 只能用在 [迴圈](loop--sm4---asm-.md) 或 [endloop](endloop--sm4---asm-.md)中。</span><span class="sxs-lookup"><span data-stu-id="b3803-107">**continue** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="b3803-108">下列範例顯示如何使用 **continue** 指令。</span><span class="sxs-lookup"><span data-stu-id="b3803-108">The following example shows how to use the **continue** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
                    ...
                endloop
```



<span data-ttu-id="b3803-109">Token 格式包含著色器中對應迴圈指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="b3803-109">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="b3803-110">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b3803-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b3803-111">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="b3803-111">Vertex Shader</span></span> | <span data-ttu-id="b3803-112">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="b3803-112">Geometry Shader</span></span> | <span data-ttu-id="b3803-113">像素著色器</span><span class="sxs-lookup"><span data-stu-id="b3803-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b3803-114">x</span><span class="sxs-lookup"><span data-stu-id="b3803-114">x</span></span>             | <span data-ttu-id="b3803-115">x</span><span class="sxs-lookup"><span data-stu-id="b3803-115">x</span></span>               | <span data-ttu-id="b3803-116">x</span><span class="sxs-lookup"><span data-stu-id="b3803-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b3803-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b3803-117">Minimum Shader Model</span></span>

<span data-ttu-id="b3803-118">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="b3803-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b3803-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b3803-119">Shader Model</span></span>                                              | <span data-ttu-id="b3803-120">支援</span><span class="sxs-lookup"><span data-stu-id="b3803-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b3803-121">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b3803-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b3803-122">是</span><span class="sxs-lookup"><span data-stu-id="b3803-122">yes</span></span>       |
| [<span data-ttu-id="b3803-123">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b3803-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b3803-124">是</span><span class="sxs-lookup"><span data-stu-id="b3803-124">yes</span></span>       |
| [<span data-ttu-id="b3803-125">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b3803-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b3803-126">是</span><span class="sxs-lookup"><span data-stu-id="b3803-126">yes</span></span>       |
| [<span data-ttu-id="b3803-127">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3803-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b3803-128">不可以</span><span class="sxs-lookup"><span data-stu-id="b3803-128">no</span></span>        |
| [<span data-ttu-id="b3803-129">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3803-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b3803-130">不可以</span><span class="sxs-lookup"><span data-stu-id="b3803-130">no</span></span>        |
| [<span data-ttu-id="b3803-131">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3803-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b3803-132">不可以</span><span class="sxs-lookup"><span data-stu-id="b3803-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b3803-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3803-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3803-134">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b3803-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




