---
title: 'dcl_resource 原始 (sm5-asm) '
description: '宣告著色器資源輸入，並將其指派給資源的 t-a 預留位置註冊。 |dcl_resource 原始 (sm5-asm) '
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195988"
---
# <a name="dcl_resource-raw-sm5---asm"></a><span data-ttu-id="d1a3d-104">dcl \_ 資源原始 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d1a3d-104">dcl\_resource raw (sm5 - asm)</span></span>

<span data-ttu-id="d1a3d-105">宣告著色器資源輸入，並將其指派給 \# 資源的 t a 預留位置暫存器。</span><span class="sxs-lookup"><span data-stu-id="d1a3d-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="d1a3d-106">dcl \_ 資源 \_ 原始 dstSRV</span><span class="sxs-lookup"><span data-stu-id="d1a3d-106">dcl\_resource\_raw dstSRV</span></span> |
|---------------------------|



 



| <span data-ttu-id="d1a3d-107">項目</span><span class="sxs-lookup"><span data-stu-id="d1a3d-107">Item</span></span>                                                                                           | <span data-ttu-id="d1a3d-108">描述</span><span class="sxs-lookup"><span data-stu-id="d1a3d-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a3d-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="d1a3d-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/> | <span data-ttu-id="d1a3d-110">\[在宣告 \] \# 為原始緩衝區之 ShaderResourceView 參考的 t 註冊程式中。</span><span class="sxs-lookup"><span data-stu-id="d1a3d-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a raw buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1a3d-111">備註</span><span class="sxs-lookup"><span data-stu-id="d1a3d-111">Remarks</span></span>

<span data-ttu-id="d1a3d-112">結構的內容沒有類型;在記憶體上執行的作業可能會隱含地將資料解讀為具有類型。</span><span class="sxs-lookup"><span data-stu-id="d1a3d-112">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="d1a3d-113">參考原始 t 的指示 \# 會採用1d 位址，這是一個不帶正負號的32位值，可指定緩衝區中32位對齊位置的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="d1a3d-113">Instructions that reference a raw t\# take a 1D address, an unsigned 32-bit value specifying the byte offset to a 32-bit aligned location in the Buffer.</span></span> <span data-ttu-id="d1a3d-114">位址必須是 4 (個位元組) 的倍數。</span><span class="sxs-lookup"><span data-stu-id="d1a3d-114">The address must be a multiple of 4 (bytes).</span></span>

<span data-ttu-id="d1a3d-115">系結至 t \# 但宣告為 raw 的視圖必須在其建立時指定 raw; 否則，從著色器存取時的行為未定義。</span><span class="sxs-lookup"><span data-stu-id="d1a3d-115">Views bound to t\# declared as raw must have RAW specified on their creation; otherwise behavior when accessed from a shader is undefined.</span></span>

<span data-ttu-id="d1a3d-116">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此指令。</span><span class="sxs-lookup"><span data-stu-id="d1a3d-116">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="d1a3d-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d1a3d-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d1a3d-118">頂點</span><span class="sxs-lookup"><span data-stu-id="d1a3d-118">Vertex</span></span> | <span data-ttu-id="d1a3d-119">船體</span><span class="sxs-lookup"><span data-stu-id="d1a3d-119">Hull</span></span> | <span data-ttu-id="d1a3d-120">網域</span><span class="sxs-lookup"><span data-stu-id="d1a3d-120">Domain</span></span> | <span data-ttu-id="d1a3d-121">幾何</span><span class="sxs-lookup"><span data-stu-id="d1a3d-121">Geometry</span></span> | <span data-ttu-id="d1a3d-122">像素</span><span class="sxs-lookup"><span data-stu-id="d1a3d-122">Pixel</span></span> | <span data-ttu-id="d1a3d-123">計算</span><span class="sxs-lookup"><span data-stu-id="d1a3d-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d1a3d-124">X</span><span class="sxs-lookup"><span data-stu-id="d1a3d-124">X</span></span>      | <span data-ttu-id="d1a3d-125">X</span><span class="sxs-lookup"><span data-stu-id="d1a3d-125">X</span></span>    | <span data-ttu-id="d1a3d-126">X</span><span class="sxs-lookup"><span data-stu-id="d1a3d-126">X</span></span>      | <span data-ttu-id="d1a3d-127">X</span><span class="sxs-lookup"><span data-stu-id="d1a3d-127">X</span></span>        | <span data-ttu-id="d1a3d-128">X</span><span class="sxs-lookup"><span data-stu-id="d1a3d-128">X</span></span>     | <span data-ttu-id="d1a3d-129">X</span><span class="sxs-lookup"><span data-stu-id="d1a3d-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d1a3d-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d1a3d-130">Minimum Shader Model</span></span>

<span data-ttu-id="d1a3d-131">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d1a3d-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d1a3d-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d1a3d-132">Shader Model</span></span>                                              | <span data-ttu-id="d1a3d-133">支援</span><span class="sxs-lookup"><span data-stu-id="d1a3d-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d1a3d-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d1a3d-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d1a3d-135">是</span><span class="sxs-lookup"><span data-stu-id="d1a3d-135">yes</span></span>       |
| [<span data-ttu-id="d1a3d-136">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d1a3d-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d1a3d-137">不可以</span><span class="sxs-lookup"><span data-stu-id="d1a3d-137">no</span></span>        |
| [<span data-ttu-id="d1a3d-138">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d1a3d-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d1a3d-139">不可以</span><span class="sxs-lookup"><span data-stu-id="d1a3d-139">no</span></span>        |
| [<span data-ttu-id="d1a3d-140">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d1a3d-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d1a3d-141">不可以</span><span class="sxs-lookup"><span data-stu-id="d1a3d-141">no</span></span>        |
| [<span data-ttu-id="d1a3d-142">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d1a3d-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d1a3d-143">不可以</span><span class="sxs-lookup"><span data-stu-id="d1a3d-143">no</span></span>        |
| [<span data-ttu-id="d1a3d-144">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d1a3d-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d1a3d-145">不可以</span><span class="sxs-lookup"><span data-stu-id="d1a3d-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d1a3d-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1a3d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1a3d-147">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d1a3d-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





