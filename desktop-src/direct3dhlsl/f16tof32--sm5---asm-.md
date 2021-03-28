---
title: 'f16tof32 (sm5-asm) '
description: 'Float16 至 float32 轉換的元件。 |f16tof32 (sm5-asm) '
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974140"
---
# <a name="f16tof32-sm5---asm"></a><span data-ttu-id="b7493-104">f16tof32 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="b7493-104">f16tof32 (sm5 - asm)</span></span>

<span data-ttu-id="b7493-105">Float16 至 float32 轉換的元件。</span><span class="sxs-lookup"><span data-stu-id="b7493-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="b7493-106">f16tof32 dest \[ . mask \] ， \[ - \] src \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b7493-106">f16tof32 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="b7493-107">項目</span><span class="sxs-lookup"><span data-stu-id="b7493-107">Item</span></span>                                                            | <span data-ttu-id="b7493-108">描述</span><span class="sxs-lookup"><span data-stu-id="b7493-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b7493-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="b7493-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b7493-110">\[在 \] float32 結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="b7493-110">\[in\] The address of the float32 result.</span></span><br/> |
| <span data-ttu-id="b7493-111"><span id="src"></span><span id="SRC"></span>*Src*</span><span class="sxs-lookup"><span data-stu-id="b7493-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="b7493-112">\[\]要轉換的 float16 值。</span><span class="sxs-lookup"><span data-stu-id="b7493-112">\[in\] The float16 value to convert.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="b7493-113">備註</span><span class="sxs-lookup"><span data-stu-id="b7493-113">Remarks</span></span>

<span data-ttu-id="b7493-114">這項作業會執行從 LSB 位到 float32 結果之 float16 值的元件轉換。</span><span class="sxs-lookup"><span data-stu-id="b7493-114">This operation performs a component-wise conversion of a float16 value from LSB bits to a float32 result.</span></span>

<span data-ttu-id="b7493-115">這種作業遵循浮點數轉換的 D3D 規則。</span><span class="sxs-lookup"><span data-stu-id="b7493-115">This operation follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="b7493-116">針對著色器驅動的資料解壓縮，請使用此指令。</span><span class="sxs-lookup"><span data-stu-id="b7493-116">Use this instruction for shader-driven data decompression.</span></span>

<span data-ttu-id="b7493-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b7493-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b7493-118">頂點</span><span class="sxs-lookup"><span data-stu-id="b7493-118">Vertex</span></span> | <span data-ttu-id="b7493-119">船體</span><span class="sxs-lookup"><span data-stu-id="b7493-119">Hull</span></span> | <span data-ttu-id="b7493-120">網域</span><span class="sxs-lookup"><span data-stu-id="b7493-120">Domain</span></span> | <span data-ttu-id="b7493-121">幾何</span><span class="sxs-lookup"><span data-stu-id="b7493-121">Geometry</span></span> | <span data-ttu-id="b7493-122">像素</span><span class="sxs-lookup"><span data-stu-id="b7493-122">Pixel</span></span> | <span data-ttu-id="b7493-123">計算</span><span class="sxs-lookup"><span data-stu-id="b7493-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b7493-124">X</span><span class="sxs-lookup"><span data-stu-id="b7493-124">X</span></span>      | <span data-ttu-id="b7493-125">X</span><span class="sxs-lookup"><span data-stu-id="b7493-125">X</span></span>    | <span data-ttu-id="b7493-126">X</span><span class="sxs-lookup"><span data-stu-id="b7493-126">X</span></span>      | <span data-ttu-id="b7493-127">X</span><span class="sxs-lookup"><span data-stu-id="b7493-127">X</span></span>        | <span data-ttu-id="b7493-128">X</span><span class="sxs-lookup"><span data-stu-id="b7493-128">X</span></span>     | <span data-ttu-id="b7493-129">X</span><span class="sxs-lookup"><span data-stu-id="b7493-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7493-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b7493-130">Minimum Shader Model</span></span>

<span data-ttu-id="b7493-131">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="b7493-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b7493-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b7493-132">Shader Model</span></span>                                              | <span data-ttu-id="b7493-133">支援</span><span class="sxs-lookup"><span data-stu-id="b7493-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b7493-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b7493-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b7493-135">是</span><span class="sxs-lookup"><span data-stu-id="b7493-135">yes</span></span>       |
| [<span data-ttu-id="b7493-136">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b7493-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b7493-137">不可以</span><span class="sxs-lookup"><span data-stu-id="b7493-137">no</span></span>        |
| [<span data-ttu-id="b7493-138">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b7493-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b7493-139">不可以</span><span class="sxs-lookup"><span data-stu-id="b7493-139">no</span></span>        |
| [<span data-ttu-id="b7493-140">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b7493-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b7493-141">不可以</span><span class="sxs-lookup"><span data-stu-id="b7493-141">no</span></span>        |
| [<span data-ttu-id="b7493-142">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b7493-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b7493-143">不可以</span><span class="sxs-lookup"><span data-stu-id="b7493-143">no</span></span>        |
| [<span data-ttu-id="b7493-144">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b7493-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b7493-145">不可以</span><span class="sxs-lookup"><span data-stu-id="b7493-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b7493-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7493-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7493-147">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b7493-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





