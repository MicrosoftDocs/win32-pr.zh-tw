---
title: 'dcl_output oMask (sm5-asm) '
description: 宣告要由著色器寫入的輸出暫存器。
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373914"
---
# <a name="dcl_output-omask-sm5---asm"></a><span data-ttu-id="0a805-103">dcl \_ 輸出 oMask (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="0a805-103">dcl\_output oMask (sm5 - asm)</span></span>

<span data-ttu-id="0a805-104">宣告要由著色器寫入的輸出暫存器。</span><span class="sxs-lookup"><span data-stu-id="0a805-104">Declare an output register to be written by the shader.</span></span>



| <span data-ttu-id="0a805-105">dcl \_ 輸出 o \# \[ . mask\]</span><span class="sxs-lookup"><span data-stu-id="0a805-105">dcl\_output o\#\[.mask\]</span></span> |
|--------------------------|



 



| <span data-ttu-id="0a805-106">項目</span><span class="sxs-lookup"><span data-stu-id="0a805-106">Item</span></span>                                                   | <span data-ttu-id="0a805-107">描述</span><span class="sxs-lookup"><span data-stu-id="0a805-107">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="0a805-108"><span id="o"></span><span id="O"></span>*輸出*</span><span class="sxs-lookup"><span data-stu-id="0a805-108"><span id="o"></span><span id="O"></span>*o*</span></span><br/> | <span data-ttu-id="0a805-109">\[在輸出暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="0a805-109">\[in\] The output register.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0a805-110">備註</span><span class="sxs-lookup"><span data-stu-id="0a805-110">Remarks</span></span>


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a><span data-ttu-id="0a805-111">限制</span><span class="sxs-lookup"><span data-stu-id="0a805-111">Restrictions</span></span>

-   <span data-ttu-id="0a805-112">元件遮罩可以是 xyzw 的任何子集 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="0a805-112">The component mask can be any subset of \[xyzw\].</span></span> <span data-ttu-id="0a805-113">不過，保留元件之間的間距會浪費空間。</span><span class="sxs-lookup"><span data-stu-id="0a805-113">However, leaving gaps between components wastes space.</span></span>
-   <span data-ttu-id="0a805-114">宣告針對下一個階段所宣告的元件遮罩的超集合，是合法的。</span><span class="sxs-lookup"><span data-stu-id="0a805-114">It is legal to declare a superset of the component mask declared for input by the next stage.</span></span> <span data-ttu-id="0a805-115">但是，不允許互斥的遮罩。</span><span class="sxs-lookup"><span data-stu-id="0a805-115">However mutually exclusive masks are not allowed.</span></span> <span data-ttu-id="0a805-116">頂點著色器輸出 o3，表示圖元著色器輸入 v3. z 無效，但輸入 v3. x 或 v3. y 或 v3。</span><span class="sxs-lookup"><span data-stu-id="0a805-116">The vertex shader outputting o3.xy, means the pixel shader inputting v3.z is invalid, but inputting v3.x or v3.y or v3.xy is valid.</span></span>

<span data-ttu-id="0a805-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="0a805-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0a805-118">頂點</span><span class="sxs-lookup"><span data-stu-id="0a805-118">Vertex</span></span> | <span data-ttu-id="0a805-119">船體</span><span class="sxs-lookup"><span data-stu-id="0a805-119">Hull</span></span> | <span data-ttu-id="0a805-120">網域</span><span class="sxs-lookup"><span data-stu-id="0a805-120">Domain</span></span> | <span data-ttu-id="0a805-121">幾何</span><span class="sxs-lookup"><span data-stu-id="0a805-121">Geometry</span></span> | <span data-ttu-id="0a805-122">像素</span><span class="sxs-lookup"><span data-stu-id="0a805-122">Pixel</span></span> | <span data-ttu-id="0a805-123">計算</span><span class="sxs-lookup"><span data-stu-id="0a805-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0a805-124">X</span><span class="sxs-lookup"><span data-stu-id="0a805-124">X</span></span>      | <span data-ttu-id="0a805-125">X</span><span class="sxs-lookup"><span data-stu-id="0a805-125">X</span></span>    | <span data-ttu-id="0a805-126">X</span><span class="sxs-lookup"><span data-stu-id="0a805-126">X</span></span>      | <span data-ttu-id="0a805-127">X</span><span class="sxs-lookup"><span data-stu-id="0a805-127">X</span></span>        | <span data-ttu-id="0a805-128">X</span><span class="sxs-lookup"><span data-stu-id="0a805-128">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0a805-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0a805-129">Minimum Shader Model</span></span>

<span data-ttu-id="0a805-130">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="0a805-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0a805-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0a805-131">Shader Model</span></span>                                              | <span data-ttu-id="0a805-132">支援</span><span class="sxs-lookup"><span data-stu-id="0a805-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0a805-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="0a805-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0a805-134">是</span><span class="sxs-lookup"><span data-stu-id="0a805-134">yes</span></span>       |
| [<span data-ttu-id="0a805-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="0a805-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0a805-136">不可以</span><span class="sxs-lookup"><span data-stu-id="0a805-136">no</span></span>        |
| [<span data-ttu-id="0a805-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="0a805-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0a805-138">不可以</span><span class="sxs-lookup"><span data-stu-id="0a805-138">no</span></span>        |
| [<span data-ttu-id="0a805-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a805-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0a805-140">不可以</span><span class="sxs-lookup"><span data-stu-id="0a805-140">no</span></span>        |
| [<span data-ttu-id="0a805-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a805-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0a805-142">不可以</span><span class="sxs-lookup"><span data-stu-id="0a805-142">no</span></span>        |
| [<span data-ttu-id="0a805-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a805-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0a805-144">不可以</span><span class="sxs-lookup"><span data-stu-id="0a805-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0a805-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a805-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a805-146">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0a805-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





