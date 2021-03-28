---
title: 'dcl_uav_raw (sm5-asm) '
description: '宣告未排序的存取視圖 (UAV) 供著色器使用。 |dcl_uav_raw (sm5-asm) '
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991950"
---
# <a name="dcl_uav_raw-sm5---asm"></a><span data-ttu-id="d3324-104">dcl \_ uav \_ 原始 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d3324-104">dcl\_uav\_raw (sm5 - asm)</span></span>

<span data-ttu-id="d3324-105">宣告未排序的存取視圖 (UAV) 供著色器使用。</span><span class="sxs-lookup"><span data-stu-id="d3324-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="d3324-106">dcl \_ uav \_ 原始 \[ \_ glc \] dstUAV</span><span class="sxs-lookup"><span data-stu-id="d3324-106">dcl\_uav\_raw\[\_glc\] dstUAV</span></span> |
|-------------------------------|



 



| <span data-ttu-id="d3324-107">項目</span><span class="sxs-lookup"><span data-stu-id="d3324-107">Item</span></span>                                                                                           | <span data-ttu-id="d3324-108">描述</span><span class="sxs-lookup"><span data-stu-id="d3324-108">Description</span></span>                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="d3324-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="d3324-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="d3324-110">\[在 \] UAV 中。</span><span class="sxs-lookup"><span data-stu-id="d3324-110">\[in\] The UAV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3324-111">備註</span><span class="sxs-lookup"><span data-stu-id="d3324-111">Remarks</span></span>

<span data-ttu-id="d3324-112">*dstUAV* 是宣告 \# 為緩衝區 UnorderedAccessView 參考的 u 註冊程式，其中緩衝區會顯示為32位不具類型專案的簡單1d 陣列。</span><span class="sxs-lookup"><span data-stu-id="d3324-112">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a Buffer, where the buffer appears as a simple 1D array of 32-bit untyped entries.</span></span>

<span data-ttu-id="d3324-113">在記憶體上執行的作業可能會隱含地將資料解讀為具有類型。</span><span class="sxs-lookup"><span data-stu-id="d3324-113">Operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="d3324-114">\_Glc 旗標表示「全域一致」。</span><span class="sxs-lookup"><span data-stu-id="d3324-114">The \_glc flag means "globally coherent".</span></span> <span data-ttu-id="d3324-115">缺少 \_ glc 表示 UAV 在計算著色器中宣告為「群組一致」，或在單一圖元著色器調用中宣告為「本機一致」。</span><span class="sxs-lookup"><span data-stu-id="d3324-115">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="d3324-116">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d3324-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d3324-117">頂點</span><span class="sxs-lookup"><span data-stu-id="d3324-117">Vertex</span></span> | <span data-ttu-id="d3324-118">船體</span><span class="sxs-lookup"><span data-stu-id="d3324-118">Hull</span></span> | <span data-ttu-id="d3324-119">網域</span><span class="sxs-lookup"><span data-stu-id="d3324-119">Domain</span></span> | <span data-ttu-id="d3324-120">幾何</span><span class="sxs-lookup"><span data-stu-id="d3324-120">Geometry</span></span> | <span data-ttu-id="d3324-121">像素</span><span class="sxs-lookup"><span data-stu-id="d3324-121">Pixel</span></span> | <span data-ttu-id="d3324-122">計算</span><span class="sxs-lookup"><span data-stu-id="d3324-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d3324-123">X</span><span class="sxs-lookup"><span data-stu-id="d3324-123">X</span></span>     | <span data-ttu-id="d3324-124">X</span><span class="sxs-lookup"><span data-stu-id="d3324-124">X</span></span>       |



 

<span data-ttu-id="d3324-125">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="d3324-125">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="d3324-126">頂點</span><span class="sxs-lookup"><span data-stu-id="d3324-126">Vertex</span></span> | <span data-ttu-id="d3324-127">船體</span><span class="sxs-lookup"><span data-stu-id="d3324-127">Hull</span></span> | <span data-ttu-id="d3324-128">網域</span><span class="sxs-lookup"><span data-stu-id="d3324-128">Domain</span></span> | <span data-ttu-id="d3324-129">幾何</span><span class="sxs-lookup"><span data-stu-id="d3324-129">Geometry</span></span> | <span data-ttu-id="d3324-130">像素</span><span class="sxs-lookup"><span data-stu-id="d3324-130">Pixel</span></span> | <span data-ttu-id="d3324-131">計算</span><span class="sxs-lookup"><span data-stu-id="d3324-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d3324-132">X</span><span class="sxs-lookup"><span data-stu-id="d3324-132">X</span></span>      | <span data-ttu-id="d3324-133">X</span><span class="sxs-lookup"><span data-stu-id="d3324-133">X</span></span>    | <span data-ttu-id="d3324-134">X</span><span class="sxs-lookup"><span data-stu-id="d3324-134">X</span></span>      | <span data-ttu-id="d3324-135">X</span><span class="sxs-lookup"><span data-stu-id="d3324-135">X</span></span>        | <span data-ttu-id="d3324-136">X</span><span class="sxs-lookup"><span data-stu-id="d3324-136">X</span></span>     | <span data-ttu-id="d3324-137">X</span><span class="sxs-lookup"><span data-stu-id="d3324-137">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d3324-138">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d3324-138">Minimum Shader Model</span></span>

<span data-ttu-id="d3324-139">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d3324-139">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d3324-140">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d3324-140">Shader Model</span></span>                                              | <span data-ttu-id="d3324-141">支援</span><span class="sxs-lookup"><span data-stu-id="d3324-141">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d3324-142">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d3324-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d3324-143">是</span><span class="sxs-lookup"><span data-stu-id="d3324-143">yes</span></span>       |
| [<span data-ttu-id="d3324-144">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d3324-144">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d3324-145">不可以</span><span class="sxs-lookup"><span data-stu-id="d3324-145">no</span></span>        |
| [<span data-ttu-id="d3324-146">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d3324-146">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d3324-147">不可以</span><span class="sxs-lookup"><span data-stu-id="d3324-147">no</span></span>        |
| [<span data-ttu-id="d3324-148">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d3324-148">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d3324-149">不可以</span><span class="sxs-lookup"><span data-stu-id="d3324-149">no</span></span>        |
| [<span data-ttu-id="d3324-150">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d3324-150">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d3324-151">不可以</span><span class="sxs-lookup"><span data-stu-id="d3324-151">no</span></span>        |
| [<span data-ttu-id="d3324-152">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d3324-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d3324-153">不可以</span><span class="sxs-lookup"><span data-stu-id="d3324-153">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="d3324-154">Cs \_ 4 \_ 0 和 cs \_ 4 1 支援這個指令 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d3324-154">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d3324-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3324-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3324-156">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d3324-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





