---
title: 'f32tof16 (sm5-asm) '
description: 'Float16 至 float32 轉換的元件。 |f32tof16 (sm5-asm) '
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974397"
---
# <a name="f32tof16-sm5---asm"></a><span data-ttu-id="61746-104">f32tof16 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="61746-104">f32tof16 (sm5 - asm)</span></span>

<span data-ttu-id="61746-105">Float16 至 float32 轉換的元件。</span><span class="sxs-lookup"><span data-stu-id="61746-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="61746-106">f32tof16 dest \[ . mask \] ， \[ - \] src \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="61746-106">f32tof16 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="61746-107">項目</span><span class="sxs-lookup"><span data-stu-id="61746-107">Item</span></span>                                                            | <span data-ttu-id="61746-108">描述</span><span class="sxs-lookup"><span data-stu-id="61746-108">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="61746-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="61746-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="61746-110">\[在 \] float16 結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="61746-110">\[in\] The address of float16 result.</span></span><br/> |
| <span data-ttu-id="61746-111"><span id="src"></span><span id="SRC"></span>*Src*</span><span class="sxs-lookup"><span data-stu-id="61746-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="61746-112">\[在 \] 要轉換的 float32 值中。</span><span class="sxs-lookup"><span data-stu-id="61746-112">\[in\] The float32 value to convert.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="61746-113">備註</span><span class="sxs-lookup"><span data-stu-id="61746-113">Remarks</span></span>

<span data-ttu-id="61746-114">此指令會執行將 float32 值轉換為 float16 值結果（放置於 LSB 16 位）的元件。</span><span class="sxs-lookup"><span data-stu-id="61746-114">This instruction performs a component-wise conversion of a float32 value to a float16 value result placed in LSB 16 bits.</span></span>

<span data-ttu-id="61746-115">此指示遵循 D3D 規則來進行浮點數轉換。</span><span class="sxs-lookup"><span data-stu-id="61746-115">This instruction follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="61746-116">針對著色器驅動的資料壓縮，請使用此指令。</span><span class="sxs-lookup"><span data-stu-id="61746-116">Use this instruction for shader-driven data compression.</span></span>

<span data-ttu-id="61746-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="61746-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="61746-118">頂點</span><span class="sxs-lookup"><span data-stu-id="61746-118">Vertex</span></span> | <span data-ttu-id="61746-119">船體</span><span class="sxs-lookup"><span data-stu-id="61746-119">Hull</span></span> | <span data-ttu-id="61746-120">網域</span><span class="sxs-lookup"><span data-stu-id="61746-120">Domain</span></span> | <span data-ttu-id="61746-121">幾何</span><span class="sxs-lookup"><span data-stu-id="61746-121">Geometry</span></span> | <span data-ttu-id="61746-122">像素</span><span class="sxs-lookup"><span data-stu-id="61746-122">Pixel</span></span> | <span data-ttu-id="61746-123">計算</span><span class="sxs-lookup"><span data-stu-id="61746-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="61746-124">X</span><span class="sxs-lookup"><span data-stu-id="61746-124">X</span></span>      | <span data-ttu-id="61746-125">X</span><span class="sxs-lookup"><span data-stu-id="61746-125">X</span></span>    | <span data-ttu-id="61746-126">X</span><span class="sxs-lookup"><span data-stu-id="61746-126">X</span></span>      | <span data-ttu-id="61746-127">X</span><span class="sxs-lookup"><span data-stu-id="61746-127">X</span></span>        | <span data-ttu-id="61746-128">X</span><span class="sxs-lookup"><span data-stu-id="61746-128">X</span></span>     | <span data-ttu-id="61746-129">X</span><span class="sxs-lookup"><span data-stu-id="61746-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="61746-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="61746-130">Minimum Shader Model</span></span>

<span data-ttu-id="61746-131">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="61746-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="61746-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="61746-132">Shader Model</span></span>                                              | <span data-ttu-id="61746-133">支援</span><span class="sxs-lookup"><span data-stu-id="61746-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="61746-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="61746-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="61746-135">是</span><span class="sxs-lookup"><span data-stu-id="61746-135">yes</span></span>       |
| [<span data-ttu-id="61746-136">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="61746-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="61746-137">不可以</span><span class="sxs-lookup"><span data-stu-id="61746-137">no</span></span>        |
| [<span data-ttu-id="61746-138">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="61746-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="61746-139">不可以</span><span class="sxs-lookup"><span data-stu-id="61746-139">no</span></span>        |
| [<span data-ttu-id="61746-140">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="61746-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="61746-141">不可以</span><span class="sxs-lookup"><span data-stu-id="61746-141">no</span></span>        |
| [<span data-ttu-id="61746-142">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="61746-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="61746-143">不可以</span><span class="sxs-lookup"><span data-stu-id="61746-143">no</span></span>        |
| [<span data-ttu-id="61746-144">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="61746-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="61746-145">不可以</span><span class="sxs-lookup"><span data-stu-id="61746-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="61746-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="61746-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61746-147">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="61746-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





