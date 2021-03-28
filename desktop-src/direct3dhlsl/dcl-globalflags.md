---
title: 'dcl_globalFlags (sm4-asm) '
description: 'dcl \_ globalFlags (sm4-asm) '
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e15fce958056f91a41954b987850ad4c5a43e521
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373927"
---
# <a name="dcl_globalflags-sm4---asm"></a><span data-ttu-id="8b525-103">dcl \_ globalFlags (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="8b525-103">dcl\_globalFlags (sm4 - asm)</span></span>

<span data-ttu-id="8b525-104">宣告著色器全域旗標。</span><span class="sxs-lookup"><span data-stu-id="8b525-104">Declares shader global flags.</span></span>



| <span data-ttu-id="8b525-105">dcl \_ globalFlags *旗標*</span><span class="sxs-lookup"><span data-stu-id="8b525-105">dcl\_globalFlags *flags*</span></span> |
|--------------------------|



 

<dl> <dt>

<span data-ttu-id="8b525-106"><span id="flags"></span><span id="FLAGS"></span>*標誌*</span><span class="sxs-lookup"><span data-stu-id="8b525-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span></span>
</dt> <dd>

<span data-ttu-id="8b525-107">\[在 \] 全域著色器旗標中。</span><span class="sxs-lookup"><span data-stu-id="8b525-107">\[in\] A global shader flag.</span></span> <span data-ttu-id="8b525-108">目前已定義一個旗標。</span><span class="sxs-lookup"><span data-stu-id="8b525-108">There is currently one flag defined.</span></span>

-   <span data-ttu-id="8b525-109">\_允許重構-允許驅動程式重新排列算數運算以進行優化，如下所示。</span><span class="sxs-lookup"><span data-stu-id="8b525-109">REFACTORING\_ALLOWED - Permits the driver to reorder arithmetic operations for optimization, as shown here.</span></span>

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> <span data-ttu-id="8b525-110">重新排列算數運算可能會產生不同的結果。</span><span class="sxs-lookup"><span data-stu-id="8b525-110">Reordering arithmetic operations may generate different results.</span></span>

 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8b525-111">備註</span><span class="sxs-lookup"><span data-stu-id="8b525-111">Remarks</span></span>

<span data-ttu-id="8b525-112">此選擇性指令適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="8b525-112">This optional instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8b525-113">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="8b525-113">Vertex Shader</span></span> | <span data-ttu-id="8b525-114">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="8b525-114">Geometry Shader</span></span> | <span data-ttu-id="8b525-115">像素著色器</span><span class="sxs-lookup"><span data-stu-id="8b525-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8b525-116">x</span><span class="sxs-lookup"><span data-stu-id="8b525-116">x</span></span>             | <span data-ttu-id="8b525-117">x</span><span class="sxs-lookup"><span data-stu-id="8b525-117">x</span></span>               | <span data-ttu-id="8b525-118">x</span><span class="sxs-lookup"><span data-stu-id="8b525-118">x</span></span>            |



 

<span data-ttu-id="8b525-119">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="8b525-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="8b525-120">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="8b525-120">Minimum Shader Model</span></span>

<span data-ttu-id="8b525-121">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="8b525-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8b525-122">著色器模型</span><span class="sxs-lookup"><span data-stu-id="8b525-122">Shader Model</span></span>                                              | <span data-ttu-id="8b525-123">支援</span><span class="sxs-lookup"><span data-stu-id="8b525-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8b525-124">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8b525-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8b525-125">是</span><span class="sxs-lookup"><span data-stu-id="8b525-125">yes</span></span>       |
| [<span data-ttu-id="8b525-126">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="8b525-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8b525-127">是</span><span class="sxs-lookup"><span data-stu-id="8b525-127">yes</span></span>       |
| [<span data-ttu-id="8b525-128">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="8b525-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8b525-129">是</span><span class="sxs-lookup"><span data-stu-id="8b525-129">yes</span></span>       |
| [<span data-ttu-id="8b525-130">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8b525-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8b525-131">不可以</span><span class="sxs-lookup"><span data-stu-id="8b525-131">no</span></span>        |
| [<span data-ttu-id="8b525-132">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8b525-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8b525-133">不可以</span><span class="sxs-lookup"><span data-stu-id="8b525-133">no</span></span>        |
| [<span data-ttu-id="8b525-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8b525-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8b525-135">不可以</span><span class="sxs-lookup"><span data-stu-id="8b525-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8b525-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b525-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b525-137">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8b525-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




