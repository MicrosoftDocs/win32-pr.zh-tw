---
title: '標籤 (sm4-asm) '
description: 指出副程式的開頭。
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679144"
---
# <a name="label-sm4---asm"></a><span data-ttu-id="2156a-103">標籤 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="2156a-103">label (sm4 - asm)</span></span>

<span data-ttu-id="2156a-104">指出副程式的開頭。</span><span class="sxs-lookup"><span data-stu-id="2156a-104">Indicates the beginning of a subroutine.</span></span>



| <span data-ttu-id="2156a-105">標籤 l\#</span><span class="sxs-lookup"><span data-stu-id="2156a-105">label l\#</span></span> |
|-----------|



 



| <span data-ttu-id="2156a-106">項目</span><span class="sxs-lookup"><span data-stu-id="2156a-106">Item</span></span>                                                       | <span data-ttu-id="2156a-107">描述</span><span class="sxs-lookup"><span data-stu-id="2156a-107">Description</span></span>                         |
|------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="2156a-108"><span id="l_"></span><span id="L_"></span>*我\#*</span><span class="sxs-lookup"><span data-stu-id="2156a-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="2156a-109">\[在 \] 標籤編號中。</span><span class="sxs-lookup"><span data-stu-id="2156a-109">\[in\] The label number.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2156a-110">備註</span><span class="sxs-lookup"><span data-stu-id="2156a-110">Remarks</span></span>

<span data-ttu-id="2156a-111">**標籤** 只能出現在未在任何流程式控制制語句中嵌套之 [**ret**](ret--sm4---asm-.md)指令的正上方。</span><span class="sxs-lookup"><span data-stu-id="2156a-111">A **label** can only appear directly after a [**ret**](ret--sm4---asm-.md) instruction which is not nested in any flow control statements.</span></span>

<span data-ttu-id="2156a-112">程式中第一個 **標籤** 前面的程式碼是主要程式。</span><span class="sxs-lookup"><span data-stu-id="2156a-112">The code before the first **label** in a program is the main program.</span></span> <span data-ttu-id="2156a-113">所有副程式都會出現在程式的結尾，並以 **label** 語句表示。</span><span class="sxs-lookup"><span data-stu-id="2156a-113">All subroutines appear at the end of the program, indicated by **label** statements.</span></span>

<span data-ttu-id="2156a-114">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="2156a-114">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

<span data-ttu-id="2156a-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="2156a-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2156a-116">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="2156a-116">Vertex Shader</span></span> | <span data-ttu-id="2156a-117">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="2156a-117">Geometry Shader</span></span> | <span data-ttu-id="2156a-118">像素著色器</span><span class="sxs-lookup"><span data-stu-id="2156a-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2156a-119">x</span><span class="sxs-lookup"><span data-stu-id="2156a-119">x</span></span>             | <span data-ttu-id="2156a-120">x</span><span class="sxs-lookup"><span data-stu-id="2156a-120">x</span></span>               | <span data-ttu-id="2156a-121">x</span><span class="sxs-lookup"><span data-stu-id="2156a-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2156a-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2156a-122">Minimum Shader Model</span></span>

<span data-ttu-id="2156a-123">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2156a-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2156a-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2156a-124">Shader Model</span></span>                                              | <span data-ttu-id="2156a-125">支援</span><span class="sxs-lookup"><span data-stu-id="2156a-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2156a-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2156a-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2156a-127">是</span><span class="sxs-lookup"><span data-stu-id="2156a-127">yes</span></span>       |
| [<span data-ttu-id="2156a-128">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="2156a-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2156a-129">是</span><span class="sxs-lookup"><span data-stu-id="2156a-129">yes</span></span>       |
| [<span data-ttu-id="2156a-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="2156a-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2156a-131">是</span><span class="sxs-lookup"><span data-stu-id="2156a-131">yes</span></span>       |
| [<span data-ttu-id="2156a-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2156a-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2156a-133">不可以</span><span class="sxs-lookup"><span data-stu-id="2156a-133">no</span></span>        |
| [<span data-ttu-id="2156a-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2156a-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2156a-135">不可以</span><span class="sxs-lookup"><span data-stu-id="2156a-135">no</span></span>        |
| [<span data-ttu-id="2156a-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2156a-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2156a-137">不可以</span><span class="sxs-lookup"><span data-stu-id="2156a-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2156a-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="2156a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2156a-139">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2156a-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





