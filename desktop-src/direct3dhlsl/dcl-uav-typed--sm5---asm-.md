---
title: 'dcl_uav_typed (sm5-asm) '
description: '宣告未排序的存取視圖 (UAV) 供著色器使用。 |dcl_uav_typed (sm5-asm) '
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992102"
---
# <a name="dcl_uav_typed-sm5---asm"></a><span data-ttu-id="849c5-104">\_uav 具 \_ 類型的 sm5-asm)  (</span><span class="sxs-lookup"><span data-stu-id="849c5-104">dcl\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="849c5-105">宣告未排序的存取視圖 (UAV) 供著色器使用。</span><span class="sxs-lookup"><span data-stu-id="849c5-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="849c5-106">dcl \_ uav 具 \_ 類型 \[ \_ \] 的 glc dstUAV、dimension、type</span><span class="sxs-lookup"><span data-stu-id="849c5-106">dcl\_uav\_typed\[\_glc\] dstUAV, dimension, type</span></span> |
|--------------------------------------------------|



 



| <span data-ttu-id="849c5-107">項目</span><span class="sxs-lookup"><span data-stu-id="849c5-107">Item</span></span>                                                                                           | <span data-ttu-id="849c5-108">描述</span><span class="sxs-lookup"><span data-stu-id="849c5-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="849c5-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="849c5-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="849c5-110">\[在 \] UAV 中。</span><span class="sxs-lookup"><span data-stu-id="849c5-110">\[in\] The UAV.</span></span><br/>                                                                        |
| <span data-ttu-id="849c5-111"><span id="dimension"></span><span id="DIMENSION"></span>*維 度*</span><span class="sxs-lookup"><span data-stu-id="849c5-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimension*</span></span><br/>                 | <span data-ttu-id="849c5-112">\[中的 \] 會指定存取 UAV 的指示所提供的維度數目。</span><span class="sxs-lookup"><span data-stu-id="849c5-112">\[in\] Specifies how many dimensions the instructions accessing the UAV are providing.</span></span><br/> |
| <span data-ttu-id="849c5-113"><span id="type"></span><span id="TYPE"></span>*類型*</span><span class="sxs-lookup"><span data-stu-id="849c5-113"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                                | <span data-ttu-id="849c5-114">\[在 \] UAV 的類型中。</span><span class="sxs-lookup"><span data-stu-id="849c5-114">\[in\] The type of the UAV.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="849c5-115">備註</span><span class="sxs-lookup"><span data-stu-id="849c5-115">Remarks</span></span>

<span data-ttu-id="849c5-116">*dstUAV* 是宣告 \# 為 UnorderedAccessView 的參考，而該必須系結至 API 的 UAV \# 位置。</span><span class="sxs-lookup"><span data-stu-id="849c5-116">*dstUAV* is a u\# register being declared as a reference to an UnorderedAccessView that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="849c5-117">維度必須是 buffer、Texture1D、Texture1DArray、Texture2D、Texture2DArray 或 Texture3D。</span><span class="sxs-lookup"><span data-stu-id="849c5-117">The dimension must be buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray, or Texture3D.</span></span> <span data-ttu-id="849c5-118">這表示有多少維度可存取 UAV 的任何指示提供： 1 (Texture1D、Buffer) 、2 (Texture1DArray、Texture2D) 或 3 (Texture2DArray、Texture3D) 。</span><span class="sxs-lookup"><span data-stu-id="849c5-118">This indicates how many dimensions any instructions accessing the UAV are providing: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) or 3 (Texture2DArray, Texture3D).</span></span>

<span data-ttu-id="849c5-119">類型為 {UNORM，SNORM，UINT，聖，FLOAT}。</span><span class="sxs-lookup"><span data-stu-id="849c5-119">Type is {UNORM,SNORM,UINT,SINT,FLOAT}.</span></span> <span data-ttu-id="849c5-120">使用宣告 u 完成的作業 \# 必須與此處宣告的型別相容，而且系結至位置的 UAV \# 也必須具有相同的類型。</span><span class="sxs-lookup"><span data-stu-id="849c5-120">Operations done with the declared u\# must be compatible with the type declared here, and the UAV bound to slot \# must also have the same type.</span></span>

<span data-ttu-id="849c5-121">\_Glc 旗標代表「全域一致」。</span><span class="sxs-lookup"><span data-stu-id="849c5-121">The \_glc flag stands for "globally coherent".</span></span> <span data-ttu-id="849c5-122">缺少 \_ glc 表示 UAV 在計算著色器中宣告為「群組一致」，或在單一圖元著色器調用中宣告為「本機一致」。</span><span class="sxs-lookup"><span data-stu-id="849c5-122">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="849c5-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="849c5-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="849c5-124">頂點</span><span class="sxs-lookup"><span data-stu-id="849c5-124">Vertex</span></span> | <span data-ttu-id="849c5-125">船體</span><span class="sxs-lookup"><span data-stu-id="849c5-125">Hull</span></span> | <span data-ttu-id="849c5-126">網域</span><span class="sxs-lookup"><span data-stu-id="849c5-126">Domain</span></span> | <span data-ttu-id="849c5-127">幾何</span><span class="sxs-lookup"><span data-stu-id="849c5-127">Geometry</span></span> | <span data-ttu-id="849c5-128">像素</span><span class="sxs-lookup"><span data-stu-id="849c5-128">Pixel</span></span> | <span data-ttu-id="849c5-129">計算</span><span class="sxs-lookup"><span data-stu-id="849c5-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="849c5-130">X</span><span class="sxs-lookup"><span data-stu-id="849c5-130">X</span></span>     | <span data-ttu-id="849c5-131">X</span><span class="sxs-lookup"><span data-stu-id="849c5-131">X</span></span>       |



 

<span data-ttu-id="849c5-132">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="849c5-132">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="849c5-133">頂點</span><span class="sxs-lookup"><span data-stu-id="849c5-133">Vertex</span></span> | <span data-ttu-id="849c5-134">船體</span><span class="sxs-lookup"><span data-stu-id="849c5-134">Hull</span></span> | <span data-ttu-id="849c5-135">網域</span><span class="sxs-lookup"><span data-stu-id="849c5-135">Domain</span></span> | <span data-ttu-id="849c5-136">幾何</span><span class="sxs-lookup"><span data-stu-id="849c5-136">Geometry</span></span> | <span data-ttu-id="849c5-137">像素</span><span class="sxs-lookup"><span data-stu-id="849c5-137">Pixel</span></span> | <span data-ttu-id="849c5-138">計算</span><span class="sxs-lookup"><span data-stu-id="849c5-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="849c5-139">X</span><span class="sxs-lookup"><span data-stu-id="849c5-139">X</span></span>      | <span data-ttu-id="849c5-140">X</span><span class="sxs-lookup"><span data-stu-id="849c5-140">X</span></span>    | <span data-ttu-id="849c5-141">X</span><span class="sxs-lookup"><span data-stu-id="849c5-141">X</span></span>      | <span data-ttu-id="849c5-142">X</span><span class="sxs-lookup"><span data-stu-id="849c5-142">X</span></span>        | <span data-ttu-id="849c5-143">X</span><span class="sxs-lookup"><span data-stu-id="849c5-143">X</span></span>     | <span data-ttu-id="849c5-144">X</span><span class="sxs-lookup"><span data-stu-id="849c5-144">X</span></span>       |



 

> [!Note]  
> <span data-ttu-id="849c5-145">計算著色器4.x 不支援此指令。</span><span class="sxs-lookup"><span data-stu-id="849c5-145">This instruction is not supported in compute shader 4.x.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="849c5-146">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="849c5-146">Minimum Shader Model</span></span>

<span data-ttu-id="849c5-147">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="849c5-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="849c5-148">著色器模型</span><span class="sxs-lookup"><span data-stu-id="849c5-148">Shader Model</span></span>                                              | <span data-ttu-id="849c5-149">支援</span><span class="sxs-lookup"><span data-stu-id="849c5-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="849c5-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="849c5-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="849c5-151">是</span><span class="sxs-lookup"><span data-stu-id="849c5-151">yes</span></span>       |
| [<span data-ttu-id="849c5-152">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="849c5-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="849c5-153">不可以</span><span class="sxs-lookup"><span data-stu-id="849c5-153">no</span></span>        |
| [<span data-ttu-id="849c5-154">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="849c5-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="849c5-155">不可以</span><span class="sxs-lookup"><span data-stu-id="849c5-155">no</span></span>        |
| [<span data-ttu-id="849c5-156">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="849c5-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="849c5-157">不可以</span><span class="sxs-lookup"><span data-stu-id="849c5-157">no</span></span>        |
| [<span data-ttu-id="849c5-158">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="849c5-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="849c5-159">不可以</span><span class="sxs-lookup"><span data-stu-id="849c5-159">no</span></span>        |
| [<span data-ttu-id="849c5-160">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="849c5-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="849c5-161">不可以</span><span class="sxs-lookup"><span data-stu-id="849c5-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="849c5-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="849c5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="849c5-163">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="849c5-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





