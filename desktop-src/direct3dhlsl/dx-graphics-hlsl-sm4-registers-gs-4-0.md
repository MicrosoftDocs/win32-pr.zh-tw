---
title: 註冊-gs_4_0
description: 本章節包含幾何著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507264"
---
# <a name="registers---gs_4_0"></a><span data-ttu-id="9dedf-103">註冊-gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9dedf-103">Registers - gs\_4\_0</span></span>

<span data-ttu-id="9dedf-104">本章節包含幾何著色器第4版所執行之輸入和輸出暫存器的參考資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9dedf-104">This section contains reference information for the input and output registers implemented by geometry shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="9dedf-105">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="9dedf-105">Input Registers</span></span>



| <span data-ttu-id="9dedf-106">註冊</span><span class="sxs-lookup"><span data-stu-id="9dedf-106">Register</span></span>                 | <span data-ttu-id="9dedf-107">Name</span><span class="sxs-lookup"><span data-stu-id="9dedf-107">Name</span></span> | <span data-ttu-id="9dedf-108">Count</span><span class="sxs-lookup"><span data-stu-id="9dedf-108">Count</span></span>              | <span data-ttu-id="9dedf-109">R/W</span><span class="sxs-lookup"><span data-stu-id="9dedf-109">R/W</span></span> | <span data-ttu-id="9dedf-110">維度</span><span class="sxs-lookup"><span data-stu-id="9dedf-110">Dimension</span></span>        | <span data-ttu-id="9dedf-111">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="9dedf-111">Indexable by r\#</span></span> | <span data-ttu-id="9dedf-112">Defaults</span><span class="sxs-lookup"><span data-stu-id="9dedf-112">Defaults</span></span> | <span data-ttu-id="9dedf-113">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="9dedf-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="9dedf-114">R\#</span><span class="sxs-lookup"><span data-stu-id="9dedf-114">r\#</span></span>                      |      | <span data-ttu-id="9dedf-115">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="9dedf-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="9dedf-116">R/W</span><span class="sxs-lookup"><span data-stu-id="9dedf-116">R/W</span></span> | <span data-ttu-id="9dedf-117">4</span><span class="sxs-lookup"><span data-stu-id="9dedf-117">4</span></span>                | <span data-ttu-id="9dedf-118">否</span><span class="sxs-lookup"><span data-stu-id="9dedf-118">No</span></span>               | <span data-ttu-id="9dedf-119">None</span><span class="sxs-lookup"><span data-stu-id="9dedf-119">None</span></span>     | <span data-ttu-id="9dedf-120">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-120">Yes</span></span>          |
| <span data-ttu-id="9dedf-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="9dedf-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="9dedf-122">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="9dedf-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="9dedf-123">R/W</span><span class="sxs-lookup"><span data-stu-id="9dedf-123">R/W</span></span> | <span data-ttu-id="9dedf-124">4</span><span class="sxs-lookup"><span data-stu-id="9dedf-124">4</span></span>                | <span data-ttu-id="9dedf-125">是</span><span class="sxs-lookup"><span data-stu-id="9dedf-125">Yes</span></span>              | <span data-ttu-id="9dedf-126">無</span><span class="sxs-lookup"><span data-stu-id="9dedf-126">None</span></span>     | <span data-ttu-id="9dedf-127">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-127">Yes</span></span>          |
| <span data-ttu-id="9dedf-128">v \# \[ 頂點 \] \[ 元素\]</span><span class="sxs-lookup"><span data-stu-id="9dedf-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="9dedf-129">32</span><span class="sxs-lookup"><span data-stu-id="9dedf-129">32</span></span>                 | <span data-ttu-id="9dedf-130">R</span><span class="sxs-lookup"><span data-stu-id="9dedf-130">R</span></span>   | <span data-ttu-id="9dedf-131">4 (複合) \* 6 (垂直) </span><span class="sxs-lookup"><span data-stu-id="9dedf-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="9dedf-132">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-132">Yes</span></span>              | <span data-ttu-id="9dedf-133">無</span><span class="sxs-lookup"><span data-stu-id="9dedf-133">None</span></span>     | <span data-ttu-id="9dedf-134">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-134">Yes</span></span>          |
| <span data-ttu-id="9dedf-135">vprim</span><span class="sxs-lookup"><span data-stu-id="9dedf-135">vprim</span></span>                    |      | <span data-ttu-id="9dedf-136">1</span><span class="sxs-lookup"><span data-stu-id="9dedf-136">1</span></span>                  | <span data-ttu-id="9dedf-137">R</span><span class="sxs-lookup"><span data-stu-id="9dedf-137">R</span></span>   | <span data-ttu-id="9dedf-138">1</span><span class="sxs-lookup"><span data-stu-id="9dedf-138">1</span></span>                | <span data-ttu-id="9dedf-139">否</span><span class="sxs-lookup"><span data-stu-id="9dedf-139">No</span></span>               | <span data-ttu-id="9dedf-140">None</span><span class="sxs-lookup"><span data-stu-id="9dedf-140">None</span></span>     | <span data-ttu-id="9dedf-141">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-141">Yes</span></span>          |
| <span data-ttu-id="9dedf-142">10gbase-t\#</span><span class="sxs-lookup"><span data-stu-id="9dedf-142">t\#</span></span>                      |      | <span data-ttu-id="9dedf-143">128</span><span class="sxs-lookup"><span data-stu-id="9dedf-143">128</span></span>                | <span data-ttu-id="9dedf-144">R</span><span class="sxs-lookup"><span data-stu-id="9dedf-144">R</span></span>   | <span data-ttu-id="9dedf-145">1</span><span class="sxs-lookup"><span data-stu-id="9dedf-145">1</span></span>                | <span data-ttu-id="9dedf-146">否</span><span class="sxs-lookup"><span data-stu-id="9dedf-146">No</span></span>               | <span data-ttu-id="9dedf-147">None</span><span class="sxs-lookup"><span data-stu-id="9dedf-147">None</span></span>     | <span data-ttu-id="9dedf-148">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-148">Yes</span></span>          |
| <span data-ttu-id="9dedf-149">s\#</span><span class="sxs-lookup"><span data-stu-id="9dedf-149">s\#</span></span>                      |      | <span data-ttu-id="9dedf-150">16</span><span class="sxs-lookup"><span data-stu-id="9dedf-150">16</span></span>                 | <span data-ttu-id="9dedf-151">R</span><span class="sxs-lookup"><span data-stu-id="9dedf-151">R</span></span>   | <span data-ttu-id="9dedf-152">1</span><span class="sxs-lookup"><span data-stu-id="9dedf-152">1</span></span>                | <span data-ttu-id="9dedf-153">否</span><span class="sxs-lookup"><span data-stu-id="9dedf-153">No</span></span>               | <span data-ttu-id="9dedf-154">None</span><span class="sxs-lookup"><span data-stu-id="9dedf-154">None</span></span>     | <span data-ttu-id="9dedf-155">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-155">Yes</span></span>          |
| <span data-ttu-id="9dedf-156">cb \# \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="9dedf-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="9dedf-157">15</span><span class="sxs-lookup"><span data-stu-id="9dedf-157">15</span></span>                 | <span data-ttu-id="9dedf-158">R</span><span class="sxs-lookup"><span data-stu-id="9dedf-158">R</span></span>   | <span data-ttu-id="9dedf-159">4</span><span class="sxs-lookup"><span data-stu-id="9dedf-159">4</span></span>                | <span data-ttu-id="9dedf-160">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="9dedf-160">Yes(Contents)</span></span>    | <span data-ttu-id="9dedf-161">無</span><span class="sxs-lookup"><span data-stu-id="9dedf-161">None</span></span>     | <span data-ttu-id="9dedf-162">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-162">Yes</span></span>          |
| <span data-ttu-id="9dedf-163">icb \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="9dedf-163">icb\[index\]</span></span>             |      | <span data-ttu-id="9dedf-164">1</span><span class="sxs-lookup"><span data-stu-id="9dedf-164">1</span></span>                  | <span data-ttu-id="9dedf-165">R</span><span class="sxs-lookup"><span data-stu-id="9dedf-165">R</span></span>   | <span data-ttu-id="9dedf-166">4</span><span class="sxs-lookup"><span data-stu-id="9dedf-166">4</span></span>                | <span data-ttu-id="9dedf-167">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="9dedf-167">Yes(Contents)</span></span>    | <span data-ttu-id="9dedf-168">無</span><span class="sxs-lookup"><span data-stu-id="9dedf-168">None</span></span>     | <span data-ttu-id="9dedf-169">Yes</span><span class="sxs-lookup"><span data-stu-id="9dedf-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="9dedf-170">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="9dedf-170">Output Registers</span></span>



| <span data-ttu-id="9dedf-171">註冊</span><span class="sxs-lookup"><span data-stu-id="9dedf-171">Register</span></span> | <span data-ttu-id="9dedf-172">Name</span><span class="sxs-lookup"><span data-stu-id="9dedf-172">Name</span></span>            | <span data-ttu-id="9dedf-173">Count</span><span class="sxs-lookup"><span data-stu-id="9dedf-173">Count</span></span> | <span data-ttu-id="9dedf-174">R/W</span><span class="sxs-lookup"><span data-stu-id="9dedf-174">R/W</span></span> | <span data-ttu-id="9dedf-175">維度</span><span class="sxs-lookup"><span data-stu-id="9dedf-175">Dimension</span></span> | <span data-ttu-id="9dedf-176">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="9dedf-176">Indexable by r\#</span></span> | <span data-ttu-id="9dedf-177">Defaults</span><span class="sxs-lookup"><span data-stu-id="9dedf-177">Defaults</span></span> | <span data-ttu-id="9dedf-178">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="9dedf-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="9dedf-179">NULL</span><span class="sxs-lookup"><span data-stu-id="9dedf-179">NULL</span></span>     | <span data-ttu-id="9dedf-180">捨棄結果</span><span class="sxs-lookup"><span data-stu-id="9dedf-180">Discard Result</span></span>  | <span data-ttu-id="9dedf-181">N/A</span><span class="sxs-lookup"><span data-stu-id="9dedf-181">N/A</span></span>   | <span data-ttu-id="9dedf-182">W</span><span class="sxs-lookup"><span data-stu-id="9dedf-182">W</span></span>   | <span data-ttu-id="9dedf-183">N/A</span><span class="sxs-lookup"><span data-stu-id="9dedf-183">N/A</span></span>       | <span data-ttu-id="9dedf-184">N/A</span><span class="sxs-lookup"><span data-stu-id="9dedf-184">N/A</span></span>              | <span data-ttu-id="9dedf-185">N/A</span><span class="sxs-lookup"><span data-stu-id="9dedf-185">N/A</span></span>      | <span data-ttu-id="9dedf-186">否</span><span class="sxs-lookup"><span data-stu-id="9dedf-186">No</span></span>           |
| <span data-ttu-id="9dedf-187">輸出\#</span><span class="sxs-lookup"><span data-stu-id="9dedf-187">o\#</span></span>      | <span data-ttu-id="9dedf-188">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="9dedf-188">Output Register</span></span> | <span data-ttu-id="9dedf-189">32</span><span class="sxs-lookup"><span data-stu-id="9dedf-189">32</span></span>    | <span data-ttu-id="9dedf-190">W</span><span class="sxs-lookup"><span data-stu-id="9dedf-190">W</span></span>   | <span data-ttu-id="9dedf-191">N/A</span><span class="sxs-lookup"><span data-stu-id="9dedf-191">N/A</span></span>       | <span data-ttu-id="9dedf-192">N/A</span><span class="sxs-lookup"><span data-stu-id="9dedf-192">N/A</span></span>              | <span data-ttu-id="9dedf-193">4</span><span class="sxs-lookup"><span data-stu-id="9dedf-193">4</span></span>        | <span data-ttu-id="9dedf-194">是</span><span class="sxs-lookup"><span data-stu-id="9dedf-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="9dedf-195">相關主題</span><span class="sxs-lookup"><span data-stu-id="9dedf-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dedf-196">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9dedf-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




