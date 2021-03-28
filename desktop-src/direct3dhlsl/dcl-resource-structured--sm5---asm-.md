---
title: 'dcl_resource 結構化 (sm5-asm) '
description: '宣告著色器資源輸入，並將其指派給資源的 t-a 預留位置註冊。 |dcl_resource 結構化 (sm5-asm) '
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195925"
---
# <a name="dcl_resource-structured-sm5---asm"></a><span data-ttu-id="78302-104">dcl \_ 資源結構化 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="78302-104">dcl\_resource structured (sm5 - asm)</span></span>

<span data-ttu-id="78302-105">宣告著色器資源輸入，並將其指派給 \# 資源的 t a 預留位置暫存器。</span><span class="sxs-lookup"><span data-stu-id="78302-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="78302-106">dcl \_ 資源 \_ 結構化 DstSRV，structByteStride</span><span class="sxs-lookup"><span data-stu-id="78302-106">dcl\_resource\_structured dstSRV, structByteStride</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="78302-107">項目</span><span class="sxs-lookup"><span data-stu-id="78302-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="78302-108">描述</span><span class="sxs-lookup"><span data-stu-id="78302-108">Description</span></span>                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78302-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="78302-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/>                                         | <span data-ttu-id="78302-110">\[在宣告 \] \# 為參考之結構化緩衝區 ShaderResourceView 的 t 暫存器中，具有指定的 stride 必須系結至 API 的 SRV \# 位置。</span><span class="sxs-lookup"><span data-stu-id="78302-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound to SRV slot \# at the API.</span></span> <br/> |
| <span data-ttu-id="78302-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="78302-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="78302-112">\[以 \] 位元組為單位，指定要宣告的緩衝區中的結構大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="78302-112">\[in\] A uint that specifies the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="78302-113">這個值必須大於零。</span><span class="sxs-lookup"><span data-stu-id="78302-113">This value must be greater than zero.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="78302-114">備註</span><span class="sxs-lookup"><span data-stu-id="78302-114">Remarks</span></span>

<span data-ttu-id="78302-115">結構的內容沒有類型;在記憶體上執行的作業可能會隱含地將資料解讀為具有類型。</span><span class="sxs-lookup"><span data-stu-id="78302-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="78302-116">參考結構化 t 的指示 \# 會採用2d 位址，其中第一個元件挑選 \[ 結構 \] ，而第二個元件則挑選 \[ 結構內的位移，32位的倍數 \] 。</span><span class="sxs-lookup"><span data-stu-id="78302-116">Instructions that reference a structured t\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, multiple of 32-bits\].</span></span>

<span data-ttu-id="78302-117">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此指令。</span><span class="sxs-lookup"><span data-stu-id="78302-117">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="78302-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="78302-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="78302-119">頂點</span><span class="sxs-lookup"><span data-stu-id="78302-119">Vertex</span></span> | <span data-ttu-id="78302-120">船體</span><span class="sxs-lookup"><span data-stu-id="78302-120">Hull</span></span> | <span data-ttu-id="78302-121">網域</span><span class="sxs-lookup"><span data-stu-id="78302-121">Domain</span></span> | <span data-ttu-id="78302-122">幾何</span><span class="sxs-lookup"><span data-stu-id="78302-122">Geometry</span></span> | <span data-ttu-id="78302-123">像素</span><span class="sxs-lookup"><span data-stu-id="78302-123">Pixel</span></span> | <span data-ttu-id="78302-124">計算</span><span class="sxs-lookup"><span data-stu-id="78302-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="78302-125">X</span><span class="sxs-lookup"><span data-stu-id="78302-125">X</span></span>      | <span data-ttu-id="78302-126">X</span><span class="sxs-lookup"><span data-stu-id="78302-126">X</span></span>    | <span data-ttu-id="78302-127">X</span><span class="sxs-lookup"><span data-stu-id="78302-127">X</span></span>      | <span data-ttu-id="78302-128">X</span><span class="sxs-lookup"><span data-stu-id="78302-128">X</span></span>        | <span data-ttu-id="78302-129">X</span><span class="sxs-lookup"><span data-stu-id="78302-129">X</span></span>     | <span data-ttu-id="78302-130">X</span><span class="sxs-lookup"><span data-stu-id="78302-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="78302-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="78302-131">Minimum Shader Model</span></span>

<span data-ttu-id="78302-132">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="78302-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="78302-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="78302-133">Shader Model</span></span>                                              | <span data-ttu-id="78302-134">支援</span><span class="sxs-lookup"><span data-stu-id="78302-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="78302-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="78302-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="78302-136">是</span><span class="sxs-lookup"><span data-stu-id="78302-136">yes</span></span>       |
| [<span data-ttu-id="78302-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="78302-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="78302-138">不可以</span><span class="sxs-lookup"><span data-stu-id="78302-138">no</span></span>        |
| [<span data-ttu-id="78302-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="78302-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="78302-140">不可以</span><span class="sxs-lookup"><span data-stu-id="78302-140">no</span></span>        |
| [<span data-ttu-id="78302-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78302-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="78302-142">不可以</span><span class="sxs-lookup"><span data-stu-id="78302-142">no</span></span>        |
| [<span data-ttu-id="78302-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78302-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="78302-144">不可以</span><span class="sxs-lookup"><span data-stu-id="78302-144">no</span></span>        |
| [<span data-ttu-id="78302-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78302-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="78302-146">不可以</span><span class="sxs-lookup"><span data-stu-id="78302-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="78302-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="78302-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78302-148">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="78302-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





