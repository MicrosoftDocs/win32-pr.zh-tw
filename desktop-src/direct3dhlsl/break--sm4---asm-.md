---
title: 'break (sm4-asm) '
description: 在下一個 endloop 或 endswitch 之後，將執行點移至指令。
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313664"
---
# <a name="break-sm4---asm"></a><span data-ttu-id="10a6f-103">break (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="10a6f-103">break (sm4 - asm)</span></span>

<span data-ttu-id="10a6f-104">在下一個 [endloop](endloop--sm4---asm-.md) 或 [endswitch](endswitch--sm4---asm-.md)之後，將執行點移至指令。</span><span class="sxs-lookup"><span data-stu-id="10a6f-104">Moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="10a6f-105">break</span><span class="sxs-lookup"><span data-stu-id="10a6f-105">break</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="10a6f-106">備註</span><span class="sxs-lookup"><span data-stu-id="10a6f-106">Remarks</span></span>

<span data-ttu-id="10a6f-107">標記格式包含著色器中對應 **endloop** 或 **endswitch** 指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="10a6f-107">The token format contains the offset of the corresponding **endloop** or **endswitch** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="10a6f-108">下列範例顯示 **break** 指令。</span><span class="sxs-lookup"><span data-stu-id="10a6f-108">The following example shows the **break** instruction.</span></span>


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



<span data-ttu-id="10a6f-109">此指令必須出現在 **迴圈** / **endloop** 或 **switch** endswitch 的 **案例** 中 / \*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="10a6f-109">This instruction must appear within a **loop**/**endloop** or in a **case** in a **switch**/**endswitch**.</span></span>

<span data-ttu-id="10a6f-110">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="10a6f-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="10a6f-111">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="10a6f-111">Vertex Shader</span></span> | <span data-ttu-id="10a6f-112">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="10a6f-112">Geometry Shader</span></span> | <span data-ttu-id="10a6f-113">像素著色器</span><span class="sxs-lookup"><span data-stu-id="10a6f-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="10a6f-114">x</span><span class="sxs-lookup"><span data-stu-id="10a6f-114">x</span></span>             | <span data-ttu-id="10a6f-115">x</span><span class="sxs-lookup"><span data-stu-id="10a6f-115">x</span></span>               | <span data-ttu-id="10a6f-116">x</span><span class="sxs-lookup"><span data-stu-id="10a6f-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="10a6f-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="10a6f-117">Minimum Shader Model</span></span>

<span data-ttu-id="10a6f-118">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="10a6f-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="10a6f-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="10a6f-119">Shader Model</span></span>                                              | <span data-ttu-id="10a6f-120">支援</span><span class="sxs-lookup"><span data-stu-id="10a6f-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="10a6f-121">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="10a6f-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="10a6f-122">是</span><span class="sxs-lookup"><span data-stu-id="10a6f-122">yes</span></span>       |
| [<span data-ttu-id="10a6f-123">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="10a6f-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="10a6f-124">是</span><span class="sxs-lookup"><span data-stu-id="10a6f-124">yes</span></span>       |
| [<span data-ttu-id="10a6f-125">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="10a6f-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="10a6f-126">是</span><span class="sxs-lookup"><span data-stu-id="10a6f-126">yes</span></span>       |
| [<span data-ttu-id="10a6f-127">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="10a6f-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="10a6f-128">不可以</span><span class="sxs-lookup"><span data-stu-id="10a6f-128">no</span></span>        |
| [<span data-ttu-id="10a6f-129">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="10a6f-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="10a6f-130">不可以</span><span class="sxs-lookup"><span data-stu-id="10a6f-130">no</span></span>        |
| [<span data-ttu-id="10a6f-131">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="10a6f-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="10a6f-132">不可以</span><span class="sxs-lookup"><span data-stu-id="10a6f-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="10a6f-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="10a6f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10a6f-134">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="10a6f-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




