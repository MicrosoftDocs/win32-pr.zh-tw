---
title: 註冊-gs_4_1
description: 本章節包含幾何著色器 4 \_ 0 和 4 1 所執行之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183691"
---
# <a name="registers---gs_4_1"></a><span data-ttu-id="92e83-103">註冊-gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="92e83-103">Registers - gs\_4\_1</span></span>

<span data-ttu-id="92e83-104">本章節包含幾何著色器 4 \_ 0 和 4 1 所執行之輸入和輸出暫存器的參考資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="92e83-104">This section contains reference information for the input and output registers implemented by geometry shader versions 4\_0 and 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="92e83-105">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="92e83-105">Input Registers</span></span>



| <span data-ttu-id="92e83-106">註冊</span><span class="sxs-lookup"><span data-stu-id="92e83-106">Register</span></span>                 | <span data-ttu-id="92e83-107">Name</span><span class="sxs-lookup"><span data-stu-id="92e83-107">Name</span></span> | <span data-ttu-id="92e83-108">Count</span><span class="sxs-lookup"><span data-stu-id="92e83-108">Count</span></span>              | <span data-ttu-id="92e83-109">R/W</span><span class="sxs-lookup"><span data-stu-id="92e83-109">R/W</span></span> | <span data-ttu-id="92e83-110">維度</span><span class="sxs-lookup"><span data-stu-id="92e83-110">Dimension</span></span>        | <span data-ttu-id="92e83-111">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="92e83-111">Indexable by r\#</span></span> | <span data-ttu-id="92e83-112">Defaults</span><span class="sxs-lookup"><span data-stu-id="92e83-112">Defaults</span></span> | <span data-ttu-id="92e83-113">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="92e83-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="92e83-114">R\#</span><span class="sxs-lookup"><span data-stu-id="92e83-114">r\#</span></span>                      |      | <span data-ttu-id="92e83-115">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="92e83-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="92e83-116">R/W</span><span class="sxs-lookup"><span data-stu-id="92e83-116">R/W</span></span> | <span data-ttu-id="92e83-117">4</span><span class="sxs-lookup"><span data-stu-id="92e83-117">4</span></span>                | <span data-ttu-id="92e83-118">否</span><span class="sxs-lookup"><span data-stu-id="92e83-118">No</span></span>               | <span data-ttu-id="92e83-119">None</span><span class="sxs-lookup"><span data-stu-id="92e83-119">None</span></span>     | <span data-ttu-id="92e83-120">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-120">Yes</span></span>          |
| <span data-ttu-id="92e83-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="92e83-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="92e83-122">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="92e83-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="92e83-123">R/W</span><span class="sxs-lookup"><span data-stu-id="92e83-123">R/W</span></span> | <span data-ttu-id="92e83-124">4</span><span class="sxs-lookup"><span data-stu-id="92e83-124">4</span></span>                | <span data-ttu-id="92e83-125">是</span><span class="sxs-lookup"><span data-stu-id="92e83-125">Yes</span></span>              | <span data-ttu-id="92e83-126">無</span><span class="sxs-lookup"><span data-stu-id="92e83-126">None</span></span>     | <span data-ttu-id="92e83-127">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-127">Yes</span></span>          |
| <span data-ttu-id="92e83-128">v \# \[ 頂點 \] \[ 元素\]</span><span class="sxs-lookup"><span data-stu-id="92e83-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="92e83-129">32</span><span class="sxs-lookup"><span data-stu-id="92e83-129">32</span></span>                 | <span data-ttu-id="92e83-130">R</span><span class="sxs-lookup"><span data-stu-id="92e83-130">R</span></span>   | <span data-ttu-id="92e83-131">4 (複合) \* 6 (垂直) </span><span class="sxs-lookup"><span data-stu-id="92e83-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="92e83-132">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-132">Yes</span></span>              | <span data-ttu-id="92e83-133">無</span><span class="sxs-lookup"><span data-stu-id="92e83-133">None</span></span>     | <span data-ttu-id="92e83-134">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-134">Yes</span></span>          |
| <span data-ttu-id="92e83-135">vprim</span><span class="sxs-lookup"><span data-stu-id="92e83-135">vprim</span></span>                    |      | <span data-ttu-id="92e83-136">1</span><span class="sxs-lookup"><span data-stu-id="92e83-136">1</span></span>                  | <span data-ttu-id="92e83-137">R</span><span class="sxs-lookup"><span data-stu-id="92e83-137">R</span></span>   | <span data-ttu-id="92e83-138">1</span><span class="sxs-lookup"><span data-stu-id="92e83-138">1</span></span>                | <span data-ttu-id="92e83-139">否</span><span class="sxs-lookup"><span data-stu-id="92e83-139">No</span></span>               | <span data-ttu-id="92e83-140">None</span><span class="sxs-lookup"><span data-stu-id="92e83-140">None</span></span>     | <span data-ttu-id="92e83-141">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-141">Yes</span></span>          |
| <span data-ttu-id="92e83-142">10gbase-t\#</span><span class="sxs-lookup"><span data-stu-id="92e83-142">t\#</span></span>                      |      | <span data-ttu-id="92e83-143">128</span><span class="sxs-lookup"><span data-stu-id="92e83-143">128</span></span>                | <span data-ttu-id="92e83-144">R</span><span class="sxs-lookup"><span data-stu-id="92e83-144">R</span></span>   | <span data-ttu-id="92e83-145">1</span><span class="sxs-lookup"><span data-stu-id="92e83-145">1</span></span>                | <span data-ttu-id="92e83-146">否</span><span class="sxs-lookup"><span data-stu-id="92e83-146">No</span></span>               | <span data-ttu-id="92e83-147">None</span><span class="sxs-lookup"><span data-stu-id="92e83-147">None</span></span>     | <span data-ttu-id="92e83-148">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-148">Yes</span></span>          |
| <span data-ttu-id="92e83-149">s\#</span><span class="sxs-lookup"><span data-stu-id="92e83-149">s\#</span></span>                      |      | <span data-ttu-id="92e83-150">16</span><span class="sxs-lookup"><span data-stu-id="92e83-150">16</span></span>                 | <span data-ttu-id="92e83-151">R</span><span class="sxs-lookup"><span data-stu-id="92e83-151">R</span></span>   | <span data-ttu-id="92e83-152">1</span><span class="sxs-lookup"><span data-stu-id="92e83-152">1</span></span>                | <span data-ttu-id="92e83-153">否</span><span class="sxs-lookup"><span data-stu-id="92e83-153">No</span></span>               | <span data-ttu-id="92e83-154">None</span><span class="sxs-lookup"><span data-stu-id="92e83-154">None</span></span>     | <span data-ttu-id="92e83-155">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-155">Yes</span></span>          |
| <span data-ttu-id="92e83-156">cb \# \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="92e83-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="92e83-157">15</span><span class="sxs-lookup"><span data-stu-id="92e83-157">15</span></span>                 | <span data-ttu-id="92e83-158">R</span><span class="sxs-lookup"><span data-stu-id="92e83-158">R</span></span>   | <span data-ttu-id="92e83-159">4</span><span class="sxs-lookup"><span data-stu-id="92e83-159">4</span></span>                | <span data-ttu-id="92e83-160">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="92e83-160">Yes(Contents)</span></span>    | <span data-ttu-id="92e83-161">無</span><span class="sxs-lookup"><span data-stu-id="92e83-161">None</span></span>     | <span data-ttu-id="92e83-162">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-162">Yes</span></span>          |
| <span data-ttu-id="92e83-163">icb \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="92e83-163">icb\[index\]</span></span>             |      | <span data-ttu-id="92e83-164">1</span><span class="sxs-lookup"><span data-stu-id="92e83-164">1</span></span>                  | <span data-ttu-id="92e83-165">R</span><span class="sxs-lookup"><span data-stu-id="92e83-165">R</span></span>   | <span data-ttu-id="92e83-166">4</span><span class="sxs-lookup"><span data-stu-id="92e83-166">4</span></span>                | <span data-ttu-id="92e83-167">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="92e83-167">Yes(Contents)</span></span>    | <span data-ttu-id="92e83-168">無</span><span class="sxs-lookup"><span data-stu-id="92e83-168">None</span></span>     | <span data-ttu-id="92e83-169">Yes</span><span class="sxs-lookup"><span data-stu-id="92e83-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="92e83-170">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="92e83-170">Output Registers</span></span>



| <span data-ttu-id="92e83-171">註冊</span><span class="sxs-lookup"><span data-stu-id="92e83-171">Register</span></span> | <span data-ttu-id="92e83-172">Name</span><span class="sxs-lookup"><span data-stu-id="92e83-172">Name</span></span>            | <span data-ttu-id="92e83-173">Count</span><span class="sxs-lookup"><span data-stu-id="92e83-173">Count</span></span> | <span data-ttu-id="92e83-174">R/W</span><span class="sxs-lookup"><span data-stu-id="92e83-174">R/W</span></span> | <span data-ttu-id="92e83-175">維度</span><span class="sxs-lookup"><span data-stu-id="92e83-175">Dimension</span></span> | <span data-ttu-id="92e83-176">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="92e83-176">Indexable by r\#</span></span> | <span data-ttu-id="92e83-177">Defaults</span><span class="sxs-lookup"><span data-stu-id="92e83-177">Defaults</span></span> | <span data-ttu-id="92e83-178">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="92e83-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="92e83-179">NULL</span><span class="sxs-lookup"><span data-stu-id="92e83-179">NULL</span></span>     | <span data-ttu-id="92e83-180">捨棄結果</span><span class="sxs-lookup"><span data-stu-id="92e83-180">Discard Result</span></span>  | <span data-ttu-id="92e83-181">N/A</span><span class="sxs-lookup"><span data-stu-id="92e83-181">N/A</span></span>   | <span data-ttu-id="92e83-182">W</span><span class="sxs-lookup"><span data-stu-id="92e83-182">W</span></span>   | <span data-ttu-id="92e83-183">N/A</span><span class="sxs-lookup"><span data-stu-id="92e83-183">N/A</span></span>       | <span data-ttu-id="92e83-184">N/A</span><span class="sxs-lookup"><span data-stu-id="92e83-184">N/A</span></span>              | <span data-ttu-id="92e83-185">N/A</span><span class="sxs-lookup"><span data-stu-id="92e83-185">N/A</span></span>      | <span data-ttu-id="92e83-186">否</span><span class="sxs-lookup"><span data-stu-id="92e83-186">No</span></span>           |
| <span data-ttu-id="92e83-187">輸出\#</span><span class="sxs-lookup"><span data-stu-id="92e83-187">o\#</span></span>      | <span data-ttu-id="92e83-188">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="92e83-188">Output Register</span></span> | <span data-ttu-id="92e83-189">32</span><span class="sxs-lookup"><span data-stu-id="92e83-189">32</span></span>    | <span data-ttu-id="92e83-190">W</span><span class="sxs-lookup"><span data-stu-id="92e83-190">W</span></span>   | <span data-ttu-id="92e83-191">N/A</span><span class="sxs-lookup"><span data-stu-id="92e83-191">N/A</span></span>       | <span data-ttu-id="92e83-192">N/A</span><span class="sxs-lookup"><span data-stu-id="92e83-192">N/A</span></span>              | <span data-ttu-id="92e83-193">4</span><span class="sxs-lookup"><span data-stu-id="92e83-193">4</span></span>        | <span data-ttu-id="92e83-194">是</span><span class="sxs-lookup"><span data-stu-id="92e83-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="92e83-195">相關主題</span><span class="sxs-lookup"><span data-stu-id="92e83-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e83-196">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="92e83-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




