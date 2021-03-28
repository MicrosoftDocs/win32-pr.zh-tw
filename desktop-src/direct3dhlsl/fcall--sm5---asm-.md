---
title: 'fcall (sm5-asm) '
description: 介面函式呼叫。
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373891"
---
# <a name="fcall-sm5---asm"></a><span data-ttu-id="2e8d9-103">fcall (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="2e8d9-103">fcall (sm5 - asm)</span></span>

<span data-ttu-id="2e8d9-104">介面函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-104">Interface function call.</span></span>



| <span data-ttu-id="2e8d9-105">fcall fp \# \[ arrayIndex \] \[ callSite\]</span><span class="sxs-lookup"><span data-stu-id="2e8d9-105">fcall fp\#\[arrayIndex\]\[callSite\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="2e8d9-106">項目</span><span class="sxs-lookup"><span data-stu-id="2e8d9-106">Item</span></span>                                                                                                           | <span data-ttu-id="2e8d9-107">描述</span><span class="sxs-lookup"><span data-stu-id="2e8d9-107">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8d9-108"><span id="fp_"></span><span id="FP_"></span>*Fp\#*</span><span class="sxs-lookup"><span data-stu-id="2e8d9-108"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/>                                                  | <span data-ttu-id="2e8d9-109">\[在 \] 函數指標中。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-109">\[in\] The function pointer.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2e8d9-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span><span class="sxs-lookup"><span data-stu-id="2e8d9-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span></span><br/> | <span data-ttu-id="2e8d9-111">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-111">\[in\] Optional.</span></span> <span data-ttu-id="2e8d9-112">指定函式指標陣列中的位移。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-112">Specifies an offset into the function pointer array.</span></span> <span data-ttu-id="2e8d9-113">如果 fp 未宣告為可索引，則此參數必須是常值不帶正負號的整數 \# 。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-113">This parameter must be a literal unsigned integer if fp\# was not declared as indexable.</span></span> <span data-ttu-id="2e8d9-114">否則，arrayIndex 可能是來自著色器暫存器的表單常值基底 + 位移。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-114">Otherwise, arrayIndex may be of the form literal base + offset from a shader register.</span></span> <span data-ttu-id="2e8d9-115">例如，fcall fp1 \[ r1. w + 0 \] \[ 0 \] 。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-115">For example, fcall fp1\[r1.w + 0\]\[0\] .</span></span><br/> |
| <span data-ttu-id="2e8d9-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*</span><span class="sxs-lookup"><span data-stu-id="2e8d9-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span> *callSite*</span></span><br/>     | <span data-ttu-id="2e8d9-117">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-117">\[in\] Optional.</span></span> <span data-ttu-id="2e8d9-118">選取的函式資料表中不帶正負號的整數位移，選取了不常執行的函數主體 \# 。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-118">A literal unsigned integer offset into the selected function table, selecting a function body fb\# to execute.</span></span> <br/>                                                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="2e8d9-119">備註</span><span class="sxs-lookup"><span data-stu-id="2e8d9-119">Remarks</span></span>

<span data-ttu-id="2e8d9-120">*fp \#* \[ \] \[ arrayIndex \]解析為特定的函式表，從著色 *器的宣告 \#* 中所列的函式資料表選項，在著色器以外的 API 中選取。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-120">*fp\#*\[*arrayIndex*\]\[\] resolves to a particular function table, selected from the API outside the shader from the function table choices listed in the declaration of *fp\#*.</span></span>

<span data-ttu-id="2e8d9-121">\# *Fp \#* 和 *arrayIndex* 中的總和會選取函數資料表。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-121">The sum of \# in *fp\#* and *arrayIndex* select the function table.</span></span> <span data-ttu-id="2e8d9-122">例如，如果介面宣告為 fp4 \[ 4 \] \[ 3 \] (陣列大小為 4) ，則下列 **fcall** 是相等的： fcall fp4 \[ 2 \] \[ 3 \] 和 fp5 \[ 1 \] \[ 3 \] ，因為 4 + 2 = 5 + 1。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-122">For example, if an interface is declared as fp4\[4\]\[3\] (array size of 4), the following **fcall** s are equivalent: fcall fp4\[2\]\[3\] and fp5\[1\]\[3\], because 4+2 = 5+1.</span></span>

### <a name="restrictions"></a><span data-ttu-id="2e8d9-123">限制</span><span class="sxs-lookup"><span data-stu-id="2e8d9-123">Restrictions</span></span>

-   <span data-ttu-id="2e8d9-124">如果 *arrayIndex* 使用動態索引，則如果 *arrayIndex* 分歧在連續的著色器調用（可能在密集建置中執行），則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-124">If *arrayIndex* uses dynamic indexing, behavior is undefined if *arrayIndex* diverges on adjacent shader invocations, which could be executing in lockstep.</span></span> <span data-ttu-id="2e8d9-125">HLSL 編譯器會嘗試不允許這種情況。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-125">The HLSL compiler will attempt to disallow this case.</span></span>

    <span data-ttu-id="2e8d9-126">相鄰調用可能因為流量控制而處於非使用中狀態，因為它不會中斷密集建置執行。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-126">Adjacent invocations can be inactive due to flow control, because it doesn t break lockstep execution.</span></span>

-   <span data-ttu-id="2e8d9-127">如果 *fp \#*  +  *arrayIndex* 指定超出範圍的索引，則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-127">If *fp\#* + *arrayIndex* specifies an out of bounds index, behavior is undefined.</span></span>
-   <span data-ttu-id="2e8d9-128">針對此處所述的未定義案例，這表示目前 D3D 裝置的行為變成未定義，包括裝置可能遺失的可能性。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-128">For the undefined cases described here, it means the behavior of the current D3D device becomes undefined, including the possibility of Device Lost.</span></span> <span data-ttu-id="2e8d9-129">不過，目前 D3D 裝置以外的記憶體不會以程式碼的形式存取或執行。</span><span class="sxs-lookup"><span data-stu-id="2e8d9-129">However no memory outside the current D3D device will be accessed or executed as code.</span></span>

<span data-ttu-id="2e8d9-130">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="2e8d9-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2e8d9-131">頂點</span><span class="sxs-lookup"><span data-stu-id="2e8d9-131">Vertex</span></span> | <span data-ttu-id="2e8d9-132">船體</span><span class="sxs-lookup"><span data-stu-id="2e8d9-132">Hull</span></span> | <span data-ttu-id="2e8d9-133">網域</span><span class="sxs-lookup"><span data-stu-id="2e8d9-133">Domain</span></span> | <span data-ttu-id="2e8d9-134">幾何</span><span class="sxs-lookup"><span data-stu-id="2e8d9-134">Geometry</span></span> | <span data-ttu-id="2e8d9-135">像素</span><span class="sxs-lookup"><span data-stu-id="2e8d9-135">Pixel</span></span> | <span data-ttu-id="2e8d9-136">計算</span><span class="sxs-lookup"><span data-stu-id="2e8d9-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2e8d9-137">X</span><span class="sxs-lookup"><span data-stu-id="2e8d9-137">X</span></span>      | <span data-ttu-id="2e8d9-138">X</span><span class="sxs-lookup"><span data-stu-id="2e8d9-138">X</span></span>    | <span data-ttu-id="2e8d9-139">X</span><span class="sxs-lookup"><span data-stu-id="2e8d9-139">X</span></span>      | <span data-ttu-id="2e8d9-140">X</span><span class="sxs-lookup"><span data-stu-id="2e8d9-140">X</span></span>        | <span data-ttu-id="2e8d9-141">X</span><span class="sxs-lookup"><span data-stu-id="2e8d9-141">X</span></span>     | <span data-ttu-id="2e8d9-142">X</span><span class="sxs-lookup"><span data-stu-id="2e8d9-142">X</span></span>       |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="2e8d9-143">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2e8d9-143">Minimum Shader Model</span></span>

<span data-ttu-id="2e8d9-144">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="2e8d9-144">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2e8d9-145">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2e8d9-145">Shader Model</span></span>                                              | <span data-ttu-id="2e8d9-146">支援</span><span class="sxs-lookup"><span data-stu-id="2e8d9-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2e8d9-147">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2e8d9-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2e8d9-148">是</span><span class="sxs-lookup"><span data-stu-id="2e8d9-148">yes</span></span>       |
| [<span data-ttu-id="2e8d9-149">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="2e8d9-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2e8d9-150">不可以</span><span class="sxs-lookup"><span data-stu-id="2e8d9-150">no</span></span>        |
| [<span data-ttu-id="2e8d9-151">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="2e8d9-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2e8d9-152">不可以</span><span class="sxs-lookup"><span data-stu-id="2e8d9-152">no</span></span>        |
| [<span data-ttu-id="2e8d9-153">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2e8d9-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2e8d9-154">不可以</span><span class="sxs-lookup"><span data-stu-id="2e8d9-154">no</span></span>        |
| [<span data-ttu-id="2e8d9-155">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2e8d9-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2e8d9-156">不可以</span><span class="sxs-lookup"><span data-stu-id="2e8d9-156">no</span></span>        |
| [<span data-ttu-id="2e8d9-157">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2e8d9-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2e8d9-158">不可以</span><span class="sxs-lookup"><span data-stu-id="2e8d9-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2e8d9-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e8d9-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e8d9-160">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2e8d9-160">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





