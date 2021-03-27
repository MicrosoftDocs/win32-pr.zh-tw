---
title: 'ret (sm4-asm) '
description: Return 語句。
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679120"
---
# <a name="ret-sm4---asm"></a><span data-ttu-id="dbf5e-103">ret (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="dbf5e-103">ret (sm4 - asm)</span></span>

<span data-ttu-id="dbf5e-104">Return 語句。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-104">Return statement.</span></span>



| <span data-ttu-id="dbf5e-105">Ret</span><span class="sxs-lookup"><span data-stu-id="dbf5e-105">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="dbf5e-106">備註</span><span class="sxs-lookup"><span data-stu-id="dbf5e-106">Remarks</span></span>

<span data-ttu-id="dbf5e-107">如果在副程式中，請在呼叫之後返回指令。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-107">If within a subroutine, return to the instruction after the call.</span></span> <span data-ttu-id="dbf5e-108">如果不在副程式中，請終止程式執行。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-108">If not inside a subroutine, terminate program execution.</span></span>

<span data-ttu-id="dbf5e-109">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-109">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a><span data-ttu-id="dbf5e-110">限制</span><span class="sxs-lookup"><span data-stu-id="dbf5e-110">Restrictions</span></span>

-   <span data-ttu-id="dbf5e-111">**ret** 可以出現在程式中的任何位置，任意次數。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-111">**ret** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="dbf5e-112">如果 [標籤](label--sm4---asm-.md) 指令出現在著色器中，則前面必須加上不是任何流程式控制制語句中的 **ret** 命令。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-112">If a [label](label--sm4---asm-.md) instruction appears in a Shader, it must be preceded by a **ret** command that is not nested in any flow control statements.</span></span>
-   <span data-ttu-id="dbf5e-113">如果著色器中有副程式，著色器中的最後一個指令必須是 **ret**。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-113">If there are subroutines in a Shader, the last instruction in the Shader must be a **ret**.</span></span>

<span data-ttu-id="dbf5e-114">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="dbf5e-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dbf5e-115">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="dbf5e-115">Vertex Shader</span></span> | <span data-ttu-id="dbf5e-116">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="dbf5e-116">Geometry Shader</span></span> | <span data-ttu-id="dbf5e-117">像素著色器</span><span class="sxs-lookup"><span data-stu-id="dbf5e-117">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dbf5e-118">x</span><span class="sxs-lookup"><span data-stu-id="dbf5e-118">x</span></span>             | <span data-ttu-id="dbf5e-119">x</span><span class="sxs-lookup"><span data-stu-id="dbf5e-119">x</span></span>               | <span data-ttu-id="dbf5e-120">x</span><span class="sxs-lookup"><span data-stu-id="dbf5e-120">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dbf5e-121">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="dbf5e-121">Minimum Shader Model</span></span>

<span data-ttu-id="dbf5e-122">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="dbf5e-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dbf5e-123">著色器模型</span><span class="sxs-lookup"><span data-stu-id="dbf5e-123">Shader Model</span></span>                                              | <span data-ttu-id="dbf5e-124">支援</span><span class="sxs-lookup"><span data-stu-id="dbf5e-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dbf5e-125">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="dbf5e-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dbf5e-126">是</span><span class="sxs-lookup"><span data-stu-id="dbf5e-126">yes</span></span>       |
| [<span data-ttu-id="dbf5e-127">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="dbf5e-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dbf5e-128">是</span><span class="sxs-lookup"><span data-stu-id="dbf5e-128">yes</span></span>       |
| [<span data-ttu-id="dbf5e-129">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="dbf5e-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dbf5e-130">是</span><span class="sxs-lookup"><span data-stu-id="dbf5e-130">yes</span></span>       |
| [<span data-ttu-id="dbf5e-131">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dbf5e-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dbf5e-132">不可以</span><span class="sxs-lookup"><span data-stu-id="dbf5e-132">no</span></span>        |
| [<span data-ttu-id="dbf5e-133">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dbf5e-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dbf5e-134">不可以</span><span class="sxs-lookup"><span data-stu-id="dbf5e-134">no</span></span>        |
| [<span data-ttu-id="dbf5e-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dbf5e-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dbf5e-136">不可以</span><span class="sxs-lookup"><span data-stu-id="dbf5e-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dbf5e-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="dbf5e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf5e-138">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dbf5e-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




