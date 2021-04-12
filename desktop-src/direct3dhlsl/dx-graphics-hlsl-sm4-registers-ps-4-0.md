---
title: 註冊-ps_4_0
description: 本章節包含圖元著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372245"
---
# <a name="registers---ps_4_0"></a><span data-ttu-id="9b6a7-103">註冊-ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9b6a7-103">Registers - ps\_4\_0</span></span>

<span data-ttu-id="9b6a7-104">本章節包含圖元著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9b6a7-104">This section contains reference information for the input and output registers implemented by pixel shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="9b6a7-105">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="9b6a7-105">Input Registers</span></span>



| <span data-ttu-id="9b6a7-106">註冊</span><span class="sxs-lookup"><span data-stu-id="9b6a7-106">Register</span></span>      | <span data-ttu-id="9b6a7-107">Name</span><span class="sxs-lookup"><span data-stu-id="9b6a7-107">Name</span></span> | <span data-ttu-id="9b6a7-108">Count</span><span class="sxs-lookup"><span data-stu-id="9b6a7-108">Count</span></span>              | <span data-ttu-id="9b6a7-109">R/W</span><span class="sxs-lookup"><span data-stu-id="9b6a7-109">R/W</span></span> | <span data-ttu-id="9b6a7-110">維度</span><span class="sxs-lookup"><span data-stu-id="9b6a7-110">Dimension</span></span> | <span data-ttu-id="9b6a7-111">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="9b6a7-111">Indexable by r\#</span></span> | <span data-ttu-id="9b6a7-112">Defaults</span><span class="sxs-lookup"><span data-stu-id="9b6a7-112">Defaults</span></span> | <span data-ttu-id="9b6a7-113">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="9b6a7-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="9b6a7-114">R\#</span><span class="sxs-lookup"><span data-stu-id="9b6a7-114">r\#</span></span>           |      | <span data-ttu-id="9b6a7-115">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="9b6a7-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="9b6a7-116">R/W</span><span class="sxs-lookup"><span data-stu-id="9b6a7-116">R/W</span></span> | <span data-ttu-id="9b6a7-117">4</span><span class="sxs-lookup"><span data-stu-id="9b6a7-117">4</span></span>         | <span data-ttu-id="9b6a7-118">否</span><span class="sxs-lookup"><span data-stu-id="9b6a7-118">No</span></span>               | <span data-ttu-id="9b6a7-119">None</span><span class="sxs-lookup"><span data-stu-id="9b6a7-119">None</span></span>     | <span data-ttu-id="9b6a7-120">Yes</span><span class="sxs-lookup"><span data-stu-id="9b6a7-120">Yes</span></span>          |
| <span data-ttu-id="9b6a7-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="9b6a7-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="9b6a7-122">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="9b6a7-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="9b6a7-123">R/W</span><span class="sxs-lookup"><span data-stu-id="9b6a7-123">R/W</span></span> | <span data-ttu-id="9b6a7-124">4</span><span class="sxs-lookup"><span data-stu-id="9b6a7-124">4</span></span>         | <span data-ttu-id="9b6a7-125">是</span><span class="sxs-lookup"><span data-stu-id="9b6a7-125">Yes</span></span>              | <span data-ttu-id="9b6a7-126">無</span><span class="sxs-lookup"><span data-stu-id="9b6a7-126">None</span></span>     | <span data-ttu-id="9b6a7-127">Yes</span><span class="sxs-lookup"><span data-stu-id="9b6a7-127">Yes</span></span>          |
| <span data-ttu-id="9b6a7-128">V\#</span><span class="sxs-lookup"><span data-stu-id="9b6a7-128">v\#</span></span>           |      | <span data-ttu-id="9b6a7-129">32</span><span class="sxs-lookup"><span data-stu-id="9b6a7-129">32</span></span>                 | <span data-ttu-id="9b6a7-130">R</span><span class="sxs-lookup"><span data-stu-id="9b6a7-130">R</span></span>   | <span data-ttu-id="9b6a7-131">4</span><span class="sxs-lookup"><span data-stu-id="9b6a7-131">4</span></span>         | <span data-ttu-id="9b6a7-132">是</span><span class="sxs-lookup"><span data-stu-id="9b6a7-132">Yes</span></span>              | <span data-ttu-id="9b6a7-133">無</span><span class="sxs-lookup"><span data-stu-id="9b6a7-133">None</span></span>     | <span data-ttu-id="9b6a7-134">Yes</span><span class="sxs-lookup"><span data-stu-id="9b6a7-134">Yes</span></span>          |
| <span data-ttu-id="9b6a7-135">10gbase-t\#</span><span class="sxs-lookup"><span data-stu-id="9b6a7-135">t\#</span></span>           |      | <span data-ttu-id="9b6a7-136">128</span><span class="sxs-lookup"><span data-stu-id="9b6a7-136">128</span></span>                | <span data-ttu-id="9b6a7-137">R</span><span class="sxs-lookup"><span data-stu-id="9b6a7-137">R</span></span>   | <span data-ttu-id="9b6a7-138">1</span><span class="sxs-lookup"><span data-stu-id="9b6a7-138">1</span></span>         | <span data-ttu-id="9b6a7-139">否</span><span class="sxs-lookup"><span data-stu-id="9b6a7-139">No</span></span>               | <span data-ttu-id="9b6a7-140">None</span><span class="sxs-lookup"><span data-stu-id="9b6a7-140">None</span></span>     | <span data-ttu-id="9b6a7-141">Yes</span><span class="sxs-lookup"><span data-stu-id="9b6a7-141">Yes</span></span>          |
| <span data-ttu-id="9b6a7-142">s\#</span><span class="sxs-lookup"><span data-stu-id="9b6a7-142">s\#</span></span>           |      | <span data-ttu-id="9b6a7-143">16</span><span class="sxs-lookup"><span data-stu-id="9b6a7-143">16</span></span>                 | <span data-ttu-id="9b6a7-144">R</span><span class="sxs-lookup"><span data-stu-id="9b6a7-144">R</span></span>   | <span data-ttu-id="9b6a7-145">1</span><span class="sxs-lookup"><span data-stu-id="9b6a7-145">1</span></span>         | <span data-ttu-id="9b6a7-146">否</span><span class="sxs-lookup"><span data-stu-id="9b6a7-146">No</span></span>               | <span data-ttu-id="9b6a7-147">None</span><span class="sxs-lookup"><span data-stu-id="9b6a7-147">None</span></span>     | <span data-ttu-id="9b6a7-148">Yes</span><span class="sxs-lookup"><span data-stu-id="9b6a7-148">Yes</span></span>          |
| <span data-ttu-id="9b6a7-149">cb \# \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="9b6a7-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="9b6a7-150">15</span><span class="sxs-lookup"><span data-stu-id="9b6a7-150">15</span></span>                 | <span data-ttu-id="9b6a7-151">R</span><span class="sxs-lookup"><span data-stu-id="9b6a7-151">R</span></span>   | <span data-ttu-id="9b6a7-152">4</span><span class="sxs-lookup"><span data-stu-id="9b6a7-152">4</span></span>         | <span data-ttu-id="9b6a7-153">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="9b6a7-153">Yes(Contents)</span></span>    | <span data-ttu-id="9b6a7-154">無</span><span class="sxs-lookup"><span data-stu-id="9b6a7-154">None</span></span>     | <span data-ttu-id="9b6a7-155">Yes</span><span class="sxs-lookup"><span data-stu-id="9b6a7-155">Yes</span></span>          |
| <span data-ttu-id="9b6a7-156">icb \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="9b6a7-156">icb\[index\]</span></span>  |      | <span data-ttu-id="9b6a7-157">1</span><span class="sxs-lookup"><span data-stu-id="9b6a7-157">1</span></span>                  | <span data-ttu-id="9b6a7-158">R</span><span class="sxs-lookup"><span data-stu-id="9b6a7-158">R</span></span>   | <span data-ttu-id="9b6a7-159">4</span><span class="sxs-lookup"><span data-stu-id="9b6a7-159">4</span></span>         | <span data-ttu-id="9b6a7-160">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="9b6a7-160">Yes(Contents)</span></span>    | <span data-ttu-id="9b6a7-161">無</span><span class="sxs-lookup"><span data-stu-id="9b6a7-161">None</span></span>     | <span data-ttu-id="9b6a7-162">Yes</span><span class="sxs-lookup"><span data-stu-id="9b6a7-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="9b6a7-163">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="9b6a7-163">Output Registers</span></span>



| <span data-ttu-id="9b6a7-164">註冊</span><span class="sxs-lookup"><span data-stu-id="9b6a7-164">Register</span></span> | <span data-ttu-id="9b6a7-165">Name</span><span class="sxs-lookup"><span data-stu-id="9b6a7-165">Name</span></span>            | <span data-ttu-id="9b6a7-166">Count</span><span class="sxs-lookup"><span data-stu-id="9b6a7-166">Count</span></span> | <span data-ttu-id="9b6a7-167">R/W</span><span class="sxs-lookup"><span data-stu-id="9b6a7-167">R/W</span></span> | <span data-ttu-id="9b6a7-168">維度</span><span class="sxs-lookup"><span data-stu-id="9b6a7-168">Dimension</span></span> | <span data-ttu-id="9b6a7-169">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="9b6a7-169">Indexable by r\#</span></span> | <span data-ttu-id="9b6a7-170">Defaults</span><span class="sxs-lookup"><span data-stu-id="9b6a7-170">Defaults</span></span> | <span data-ttu-id="9b6a7-171">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="9b6a7-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="9b6a7-172">NULL</span><span class="sxs-lookup"><span data-stu-id="9b6a7-172">NULL</span></span>     | <span data-ttu-id="9b6a7-173">捨棄結果</span><span class="sxs-lookup"><span data-stu-id="9b6a7-173">Discard Result</span></span>  | <span data-ttu-id="9b6a7-174">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-174">N/A</span></span>   | <span data-ttu-id="9b6a7-175">W</span><span class="sxs-lookup"><span data-stu-id="9b6a7-175">W</span></span>   | <span data-ttu-id="9b6a7-176">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-176">N/A</span></span>       | <span data-ttu-id="9b6a7-177">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-177">N/A</span></span>              | <span data-ttu-id="9b6a7-178">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-178">N/A</span></span>      | <span data-ttu-id="9b6a7-179">否</span><span class="sxs-lookup"><span data-stu-id="9b6a7-179">No</span></span>           |
| <span data-ttu-id="9b6a7-180">輸出\#</span><span class="sxs-lookup"><span data-stu-id="9b6a7-180">o\#</span></span>      | <span data-ttu-id="9b6a7-181">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="9b6a7-181">Output Register</span></span> | <span data-ttu-id="9b6a7-182">8</span><span class="sxs-lookup"><span data-stu-id="9b6a7-182">8</span></span>     | <span data-ttu-id="9b6a7-183">W</span><span class="sxs-lookup"><span data-stu-id="9b6a7-183">W</span></span>   | <span data-ttu-id="9b6a7-184">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-184">N/A</span></span>       | <span data-ttu-id="9b6a7-185">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-185">N/A</span></span>              | <span data-ttu-id="9b6a7-186">4</span><span class="sxs-lookup"><span data-stu-id="9b6a7-186">4</span></span>        | <span data-ttu-id="9b6a7-187">否</span><span class="sxs-lookup"><span data-stu-id="9b6a7-187">No</span></span>           |
| <span data-ttu-id="9b6a7-188">oDepth</span><span class="sxs-lookup"><span data-stu-id="9b6a7-188">oDepth</span></span>   | <span data-ttu-id="9b6a7-189">輸出深度</span><span class="sxs-lookup"><span data-stu-id="9b6a7-189">Output Depth</span></span>    | <span data-ttu-id="9b6a7-190">1</span><span class="sxs-lookup"><span data-stu-id="9b6a7-190">1</span></span>     | <span data-ttu-id="9b6a7-191">W</span><span class="sxs-lookup"><span data-stu-id="9b6a7-191">W</span></span>   | <span data-ttu-id="9b6a7-192">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-192">N/A</span></span>       | <span data-ttu-id="9b6a7-193">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-193">N/A</span></span>              | <span data-ttu-id="9b6a7-194">1</span><span class="sxs-lookup"><span data-stu-id="9b6a7-194">1</span></span>        | <span data-ttu-id="9b6a7-195">N/A</span><span class="sxs-lookup"><span data-stu-id="9b6a7-195">N/A</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="9b6a7-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b6a7-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b6a7-197">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9b6a7-197">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




