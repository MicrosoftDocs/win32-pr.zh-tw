---
title: 'bufinfo (sm5-asm) '
description: 查詢緩衝區上的元素計數 (但不是常數緩衝區) 。
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990762"
---
# <a name="bufinfo-sm5---asm"></a><span data-ttu-id="fa2f6-103">bufinfo (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="fa2f6-103">bufinfo (sm5 - asm)</span></span>

<span data-ttu-id="fa2f6-104">查詢緩衝區上的元素計數 (但不是常數緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-104">Query the element count on a buffer (but not the constant buffer).</span></span>



| <span data-ttu-id="fa2f6-105">bufinfo dest \[ . mask \] ，srcResource</span><span class="sxs-lookup"><span data-stu-id="fa2f6-105">bufinfo dest\[.mask\], srcResource</span></span> |
|------------------------------------|



 



| <span data-ttu-id="fa2f6-106">項目</span><span class="sxs-lookup"><span data-stu-id="fa2f6-106">Item</span></span>                                                                                                               | <span data-ttu-id="fa2f6-107">描述</span><span class="sxs-lookup"><span data-stu-id="fa2f6-107">Description</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2f6-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="fa2f6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="fa2f6-109">\[在 \] 結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-109">\[in\] The address of the results.</span></span><br/>                                         |
| <span data-ttu-id="fa2f6-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="fa2f6-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="fa2f6-111">\[在 \] 緩衝區中，不是常數緩衝區，而是在 SRV (t \#) 或 UAV (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-111">\[in\] Buffer, other than a constant Buffer, in an SRV (t\#) or UAV (u\#).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa2f6-112">備註</span><span class="sxs-lookup"><span data-stu-id="fa2f6-112">Remarks</span></span>

<span data-ttu-id="fa2f6-113">*Dest* 中的所有元件都會收到緩衝區 s 著色器資源檢視中的整數元素數。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-113">All components in *dest* receive the integer number of elements in the buffer s shader resource view.</span></span> <span data-ttu-id="fa2f6-114">元素數目取決於 view 參數，例如記憶體格式。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-114">The number of elements depends on the view parameters such as memory format.</span></span>

<span data-ttu-id="fa2f6-115">如果是具類型的緩衝區 SRV 或 UAV，則傳回值是 view 中的元素數目 (其中元素是) 類型的一個單位。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-115">For a typed buffer SRV or UAV, the return value is the number of elements in the view (where an element is one unit of the typed format).</span></span>

<span data-ttu-id="fa2f6-116">若為原始緩衝區 SRV 或 UAV，則傳回值為 view 中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-116">For a raw buffer SRV or UAV, the return value is the number of bytes in the view.</span></span>

<span data-ttu-id="fa2f6-117">若為結構化緩衝區 SRV 或 UAV，則傳回值為視圖中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="fa2f6-117">For a structured buffer SRV or UAV, the return value is the number of structures in the view.</span></span>

<span data-ttu-id="fa2f6-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="fa2f6-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fa2f6-119">頂點</span><span class="sxs-lookup"><span data-stu-id="fa2f6-119">Vertex</span></span> | <span data-ttu-id="fa2f6-120">船體</span><span class="sxs-lookup"><span data-stu-id="fa2f6-120">Hull</span></span> | <span data-ttu-id="fa2f6-121">網域</span><span class="sxs-lookup"><span data-stu-id="fa2f6-121">Domain</span></span> | <span data-ttu-id="fa2f6-122">幾何</span><span class="sxs-lookup"><span data-stu-id="fa2f6-122">Geometry</span></span> | <span data-ttu-id="fa2f6-123">像素</span><span class="sxs-lookup"><span data-stu-id="fa2f6-123">Pixel</span></span> | <span data-ttu-id="fa2f6-124">計算</span><span class="sxs-lookup"><span data-stu-id="fa2f6-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fa2f6-125">X</span><span class="sxs-lookup"><span data-stu-id="fa2f6-125">X</span></span>      | <span data-ttu-id="fa2f6-126">X</span><span class="sxs-lookup"><span data-stu-id="fa2f6-126">X</span></span>    | <span data-ttu-id="fa2f6-127">X</span><span class="sxs-lookup"><span data-stu-id="fa2f6-127">X</span></span>      | <span data-ttu-id="fa2f6-128">X</span><span class="sxs-lookup"><span data-stu-id="fa2f6-128">X</span></span>        | <span data-ttu-id="fa2f6-129">X</span><span class="sxs-lookup"><span data-stu-id="fa2f6-129">X</span></span>     | <span data-ttu-id="fa2f6-130">X</span><span class="sxs-lookup"><span data-stu-id="fa2f6-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fa2f6-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="fa2f6-131">Minimum Shader Model</span></span>

<span data-ttu-id="fa2f6-132">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="fa2f6-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fa2f6-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="fa2f6-133">Shader Model</span></span>                                              | <span data-ttu-id="fa2f6-134">支援</span><span class="sxs-lookup"><span data-stu-id="fa2f6-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fa2f6-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fa2f6-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fa2f6-136">是</span><span class="sxs-lookup"><span data-stu-id="fa2f6-136">yes</span></span>       |
| [<span data-ttu-id="fa2f6-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="fa2f6-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fa2f6-138">不可以</span><span class="sxs-lookup"><span data-stu-id="fa2f6-138">no</span></span>        |
| [<span data-ttu-id="fa2f6-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="fa2f6-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fa2f6-140">不可以</span><span class="sxs-lookup"><span data-stu-id="fa2f6-140">no</span></span>        |
| [<span data-ttu-id="fa2f6-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa2f6-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fa2f6-142">不可以</span><span class="sxs-lookup"><span data-stu-id="fa2f6-142">no</span></span>        |
| [<span data-ttu-id="fa2f6-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa2f6-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fa2f6-144">不可以</span><span class="sxs-lookup"><span data-stu-id="fa2f6-144">no</span></span>        |
| [<span data-ttu-id="fa2f6-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa2f6-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fa2f6-146">不可以</span><span class="sxs-lookup"><span data-stu-id="fa2f6-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fa2f6-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa2f6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa2f6-148">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa2f6-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





