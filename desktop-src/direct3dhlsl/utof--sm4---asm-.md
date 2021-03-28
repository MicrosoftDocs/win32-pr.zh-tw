---
title: 'utof (sm4-asm) '
description: 浮點數轉換的不帶正負號的整數。
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022852"
---
# <a name="utof-sm4---asm"></a><span data-ttu-id="aa55c-103">utof (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="aa55c-103">utof (sm4 - asm)</span></span>

<span data-ttu-id="aa55c-104">浮點數轉換的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="aa55c-104">Unsigned integer to floating point conversion.</span></span>



| <span data-ttu-id="aa55c-105">utof dest \[ . mask \] ，src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="aa55c-105">utof dest\[.mask\], src0\[.swizzle\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="aa55c-106">項目</span><span class="sxs-lookup"><span data-stu-id="aa55c-106">Item</span></span>                                                            | <span data-ttu-id="aa55c-107">描述</span><span class="sxs-lookup"><span data-stu-id="aa55c-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="aa55c-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="aa55c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="aa55c-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="aa55c-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="aa55c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aa55c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="aa55c-111">\[在 \] 要轉換的元件中。</span><span class="sxs-lookup"><span data-stu-id="aa55c-111">\[in\] The components to convert.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="aa55c-112">備註</span><span class="sxs-lookup"><span data-stu-id="aa55c-112">Remarks</span></span>

<span data-ttu-id="aa55c-113">*src0* 必須包含不帶正負號的32位整數4元組。</span><span class="sxs-lookup"><span data-stu-id="aa55c-113">*src0* must contain an unsigned 32-bit integer 4-tuple.</span></span> <span data-ttu-id="aa55c-114">在執行指令之後， *dest* 將包含浮點數4元組。</span><span class="sxs-lookup"><span data-stu-id="aa55c-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span> <span data-ttu-id="aa55c-115">每個元件都會執行轉換。</span><span class="sxs-lookup"><span data-stu-id="aa55c-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="aa55c-116">當整數輸入值太大而無法完全以浮點數格式表示時，請四捨五入到最接近的偶數模式。</span><span class="sxs-lookup"><span data-stu-id="aa55c-116">When an integer input value is too large to be represented exactly in the floating point format, round to nearest even mode.</span></span>

<span data-ttu-id="aa55c-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="aa55c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa55c-118">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="aa55c-118">Vertex Shader</span></span> | <span data-ttu-id="aa55c-119">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="aa55c-119">Geometry Shader</span></span> | <span data-ttu-id="aa55c-120">像素著色器</span><span class="sxs-lookup"><span data-stu-id="aa55c-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aa55c-121">x</span><span class="sxs-lookup"><span data-stu-id="aa55c-121">x</span></span>             | <span data-ttu-id="aa55c-122">x</span><span class="sxs-lookup"><span data-stu-id="aa55c-122">x</span></span>               | <span data-ttu-id="aa55c-123">x</span><span class="sxs-lookup"><span data-stu-id="aa55c-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aa55c-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="aa55c-124">Minimum Shader Model</span></span>

<span data-ttu-id="aa55c-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="aa55c-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa55c-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="aa55c-126">Shader Model</span></span>                                              | <span data-ttu-id="aa55c-127">支援</span><span class="sxs-lookup"><span data-stu-id="aa55c-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa55c-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="aa55c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa55c-129">是</span><span class="sxs-lookup"><span data-stu-id="aa55c-129">yes</span></span>       |
| [<span data-ttu-id="aa55c-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="aa55c-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa55c-131">是</span><span class="sxs-lookup"><span data-stu-id="aa55c-131">yes</span></span>       |
| [<span data-ttu-id="aa55c-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="aa55c-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa55c-133">是</span><span class="sxs-lookup"><span data-stu-id="aa55c-133">yes</span></span>       |
| [<span data-ttu-id="aa55c-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa55c-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa55c-135">不可以</span><span class="sxs-lookup"><span data-stu-id="aa55c-135">no</span></span>        |
| [<span data-ttu-id="aa55c-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa55c-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa55c-137">不可以</span><span class="sxs-lookup"><span data-stu-id="aa55c-137">no</span></span>        |
| [<span data-ttu-id="aa55c-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa55c-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa55c-139">不可以</span><span class="sxs-lookup"><span data-stu-id="aa55c-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa55c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa55c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa55c-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa55c-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





