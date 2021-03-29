---
title: 'dcl_function_table (sm5-asm) '
description: 宣告函數資料表。
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990850"
---
# <a name="dcl_function_table-sm5---asm"></a><span data-ttu-id="c06b6-103">dcl \_ 函數 \_ 表 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="c06b6-103">dcl\_function\_table (sm5 - asm)</span></span>

<span data-ttu-id="c06b6-104">宣告函數資料表。</span><span class="sxs-lookup"><span data-stu-id="c06b6-104">Declare a function table.</span></span>



| <span data-ttu-id="c06b6-105">dcl \_ 函數 \_ 表格 ft \# = {fb \# ，fb \# ，...}</span><span class="sxs-lookup"><span data-stu-id="c06b6-105">dcl\_function\_table ft\# = {fb\#, fb\#, ...}</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="c06b6-106">項目</span><span class="sxs-lookup"><span data-stu-id="c06b6-106">Item</span></span>                                                      | <span data-ttu-id="c06b6-107">描述</span><span class="sxs-lookup"><span data-stu-id="c06b6-107">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="c06b6-108"><span id="ft"></span><span id="FT"></span>*英尺*</span><span class="sxs-lookup"><span data-stu-id="c06b6-108"><span id="ft"></span><span id="FT"></span>*ft*</span></span><br/> | <span data-ttu-id="c06b6-109">\[在 \] 函數資料表專案中。</span><span class="sxs-lookup"><span data-stu-id="c06b6-109">\[in\] The function table entries.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c06b6-110">備註</span><span class="sxs-lookup"><span data-stu-id="c06b6-110">Remarks</span></span>

<span data-ttu-id="c06b6-111">此函式會將函式資料表宣告為一組稍早宣告的函式主體。</span><span class="sxs-lookup"><span data-stu-id="c06b6-111">This function declares a function table as a set of function bodies that have been declared earlier.</span></span>

<span data-ttu-id="c06b6-112">這就像是 c + + vtable，但介面的每個呼叫位置都有一個專案，而不是每個方法的專案。</span><span class="sxs-lookup"><span data-stu-id="c06b6-112">This is like a C++ vtable except there is an entry per call site for an interface instead of per method.</span></span>

<span data-ttu-id="c06b6-113">函數資料表中可列出的函式主體數目沒有限制。</span><span class="sxs-lookup"><span data-stu-id="c06b6-113">There is no limit to how many function bodies can be listed in a function table.</span></span>

<span data-ttu-id="c06b6-114">在一或多個函式資料表中，將指定的函式主體 \# 視為不常被參考，作為共用通用程式碼的一種方式，這是有效的。</span><span class="sxs-lookup"><span data-stu-id="c06b6-114">It is valid for a given function body fb\# to be referenced multiple times in one or more function tables, as a way of sharing common code.</span></span>

<span data-ttu-id="c06b6-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="c06b6-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c06b6-116">頂點</span><span class="sxs-lookup"><span data-stu-id="c06b6-116">Vertex</span></span> | <span data-ttu-id="c06b6-117">船體</span><span class="sxs-lookup"><span data-stu-id="c06b6-117">Hull</span></span> | <span data-ttu-id="c06b6-118">網域</span><span class="sxs-lookup"><span data-stu-id="c06b6-118">Domain</span></span> | <span data-ttu-id="c06b6-119">幾何</span><span class="sxs-lookup"><span data-stu-id="c06b6-119">Geometry</span></span> | <span data-ttu-id="c06b6-120">像素</span><span class="sxs-lookup"><span data-stu-id="c06b6-120">Pixel</span></span> | <span data-ttu-id="c06b6-121">計算</span><span class="sxs-lookup"><span data-stu-id="c06b6-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c06b6-122">X</span><span class="sxs-lookup"><span data-stu-id="c06b6-122">X</span></span>      | <span data-ttu-id="c06b6-123">X</span><span class="sxs-lookup"><span data-stu-id="c06b6-123">X</span></span>    | <span data-ttu-id="c06b6-124">X</span><span class="sxs-lookup"><span data-stu-id="c06b6-124">X</span></span>      | <span data-ttu-id="c06b6-125">X</span><span class="sxs-lookup"><span data-stu-id="c06b6-125">X</span></span>        | <span data-ttu-id="c06b6-126">X</span><span class="sxs-lookup"><span data-stu-id="c06b6-126">X</span></span>     | <span data-ttu-id="c06b6-127">X</span><span class="sxs-lookup"><span data-stu-id="c06b6-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c06b6-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c06b6-128">Minimum Shader Model</span></span>

<span data-ttu-id="c06b6-129">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="c06b6-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c06b6-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c06b6-130">Shader Model</span></span>                                              | <span data-ttu-id="c06b6-131">支援</span><span class="sxs-lookup"><span data-stu-id="c06b6-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c06b6-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c06b6-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c06b6-133">是</span><span class="sxs-lookup"><span data-stu-id="c06b6-133">yes</span></span>       |
| [<span data-ttu-id="c06b6-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="c06b6-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c06b6-135">不可以</span><span class="sxs-lookup"><span data-stu-id="c06b6-135">no</span></span>        |
| [<span data-ttu-id="c06b6-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="c06b6-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c06b6-137">不可以</span><span class="sxs-lookup"><span data-stu-id="c06b6-137">no</span></span>        |
| [<span data-ttu-id="c06b6-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c06b6-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c06b6-139">不可以</span><span class="sxs-lookup"><span data-stu-id="c06b6-139">no</span></span>        |
| [<span data-ttu-id="c06b6-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c06b6-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c06b6-141">不可以</span><span class="sxs-lookup"><span data-stu-id="c06b6-141">no</span></span>        |
| [<span data-ttu-id="c06b6-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c06b6-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c06b6-143">不可以</span><span class="sxs-lookup"><span data-stu-id="c06b6-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c06b6-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="c06b6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c06b6-145">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c06b6-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





