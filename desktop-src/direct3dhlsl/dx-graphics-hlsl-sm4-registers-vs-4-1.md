---
title: 註冊-vs_4_1
description: 本章節包含頂點著色器第4版所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183690"
---
# <a name="registers---vs_4_1"></a><span data-ttu-id="1c9fa-103">暫存器-vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c9fa-103">Registers - vs\_4\_1</span></span>

<span data-ttu-id="1c9fa-104">本章節包含頂點著色器第4版所實之輸入和輸出暫存器的參考資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1c9fa-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="1c9fa-105">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="1c9fa-105">Input Registers</span></span>



| <span data-ttu-id="1c9fa-106">註冊</span><span class="sxs-lookup"><span data-stu-id="1c9fa-106">Register</span></span>      | <span data-ttu-id="1c9fa-107">Name</span><span class="sxs-lookup"><span data-stu-id="1c9fa-107">Name</span></span> | <span data-ttu-id="1c9fa-108">Count</span><span class="sxs-lookup"><span data-stu-id="1c9fa-108">Count</span></span>              | <span data-ttu-id="1c9fa-109">R/W</span><span class="sxs-lookup"><span data-stu-id="1c9fa-109">R/W</span></span> | <span data-ttu-id="1c9fa-110">維度</span><span class="sxs-lookup"><span data-stu-id="1c9fa-110">Dimension</span></span> | <span data-ttu-id="1c9fa-111">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="1c9fa-111">Indexable by r\#</span></span> | <span data-ttu-id="1c9fa-112">Defaults</span><span class="sxs-lookup"><span data-stu-id="1c9fa-112">Defaults</span></span> | <span data-ttu-id="1c9fa-113">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="1c9fa-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="1c9fa-114">R\#</span><span class="sxs-lookup"><span data-stu-id="1c9fa-114">r\#</span></span>           |      | <span data-ttu-id="1c9fa-115">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="1c9fa-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="1c9fa-116">R/W</span><span class="sxs-lookup"><span data-stu-id="1c9fa-116">R/W</span></span> | <span data-ttu-id="1c9fa-117">4</span><span class="sxs-lookup"><span data-stu-id="1c9fa-117">4</span></span>         | <span data-ttu-id="1c9fa-118">否</span><span class="sxs-lookup"><span data-stu-id="1c9fa-118">No</span></span>               | <span data-ttu-id="1c9fa-119">None</span><span class="sxs-lookup"><span data-stu-id="1c9fa-119">None</span></span>     | <span data-ttu-id="1c9fa-120">Yes</span><span class="sxs-lookup"><span data-stu-id="1c9fa-120">Yes</span></span>          |
| <span data-ttu-id="1c9fa-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="1c9fa-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="1c9fa-122">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="1c9fa-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="1c9fa-123">R/W</span><span class="sxs-lookup"><span data-stu-id="1c9fa-123">R/W</span></span> | <span data-ttu-id="1c9fa-124">4</span><span class="sxs-lookup"><span data-stu-id="1c9fa-124">4</span></span>         | <span data-ttu-id="1c9fa-125">是</span><span class="sxs-lookup"><span data-stu-id="1c9fa-125">Yes</span></span>              | <span data-ttu-id="1c9fa-126">無</span><span class="sxs-lookup"><span data-stu-id="1c9fa-126">None</span></span>     | <span data-ttu-id="1c9fa-127">Yes</span><span class="sxs-lookup"><span data-stu-id="1c9fa-127">Yes</span></span>          |
| <span data-ttu-id="1c9fa-128">V\#</span><span class="sxs-lookup"><span data-stu-id="1c9fa-128">v\#</span></span>           |      | <span data-ttu-id="1c9fa-129">32</span><span class="sxs-lookup"><span data-stu-id="1c9fa-129">32</span></span>                 | <span data-ttu-id="1c9fa-130">R</span><span class="sxs-lookup"><span data-stu-id="1c9fa-130">R</span></span>   | <span data-ttu-id="1c9fa-131">4</span><span class="sxs-lookup"><span data-stu-id="1c9fa-131">4</span></span>         | <span data-ttu-id="1c9fa-132">是</span><span class="sxs-lookup"><span data-stu-id="1c9fa-132">Yes</span></span>              | <span data-ttu-id="1c9fa-133">無</span><span class="sxs-lookup"><span data-stu-id="1c9fa-133">None</span></span>     | <span data-ttu-id="1c9fa-134">Yes</span><span class="sxs-lookup"><span data-stu-id="1c9fa-134">Yes</span></span>          |
| <span data-ttu-id="1c9fa-135">10gbase-t\#</span><span class="sxs-lookup"><span data-stu-id="1c9fa-135">t\#</span></span>           |      | <span data-ttu-id="1c9fa-136">128</span><span class="sxs-lookup"><span data-stu-id="1c9fa-136">128</span></span>                | <span data-ttu-id="1c9fa-137">R</span><span class="sxs-lookup"><span data-stu-id="1c9fa-137">R</span></span>   | <span data-ttu-id="1c9fa-138">1</span><span class="sxs-lookup"><span data-stu-id="1c9fa-138">1</span></span>         | <span data-ttu-id="1c9fa-139">否</span><span class="sxs-lookup"><span data-stu-id="1c9fa-139">No</span></span>               | <span data-ttu-id="1c9fa-140">None</span><span class="sxs-lookup"><span data-stu-id="1c9fa-140">None</span></span>     | <span data-ttu-id="1c9fa-141">Yes</span><span class="sxs-lookup"><span data-stu-id="1c9fa-141">Yes</span></span>          |
| <span data-ttu-id="1c9fa-142">s\#</span><span class="sxs-lookup"><span data-stu-id="1c9fa-142">s\#</span></span>           |      | <span data-ttu-id="1c9fa-143">16</span><span class="sxs-lookup"><span data-stu-id="1c9fa-143">16</span></span>                 | <span data-ttu-id="1c9fa-144">R</span><span class="sxs-lookup"><span data-stu-id="1c9fa-144">R</span></span>   | <span data-ttu-id="1c9fa-145">1</span><span class="sxs-lookup"><span data-stu-id="1c9fa-145">1</span></span>         | <span data-ttu-id="1c9fa-146">否</span><span class="sxs-lookup"><span data-stu-id="1c9fa-146">No</span></span>               | <span data-ttu-id="1c9fa-147">None</span><span class="sxs-lookup"><span data-stu-id="1c9fa-147">None</span></span>     | <span data-ttu-id="1c9fa-148">Yes</span><span class="sxs-lookup"><span data-stu-id="1c9fa-148">Yes</span></span>          |
| <span data-ttu-id="1c9fa-149">cb \# \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="1c9fa-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="1c9fa-150">15</span><span class="sxs-lookup"><span data-stu-id="1c9fa-150">15</span></span>                 | <span data-ttu-id="1c9fa-151">R</span><span class="sxs-lookup"><span data-stu-id="1c9fa-151">R</span></span>   | <span data-ttu-id="1c9fa-152">4</span><span class="sxs-lookup"><span data-stu-id="1c9fa-152">4</span></span>         | <span data-ttu-id="1c9fa-153">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="1c9fa-153">Yes(Contents)</span></span>    | <span data-ttu-id="1c9fa-154">無</span><span class="sxs-lookup"><span data-stu-id="1c9fa-154">None</span></span>     | <span data-ttu-id="1c9fa-155">Yes</span><span class="sxs-lookup"><span data-stu-id="1c9fa-155">Yes</span></span>          |
| <span data-ttu-id="1c9fa-156">icb \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="1c9fa-156">icb\[index\]</span></span>  |      | <span data-ttu-id="1c9fa-157">1</span><span class="sxs-lookup"><span data-stu-id="1c9fa-157">1</span></span>                  | <span data-ttu-id="1c9fa-158">R</span><span class="sxs-lookup"><span data-stu-id="1c9fa-158">R</span></span>   | <span data-ttu-id="1c9fa-159">4</span><span class="sxs-lookup"><span data-stu-id="1c9fa-159">4</span></span>         | <span data-ttu-id="1c9fa-160">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="1c9fa-160">Yes(Contents)</span></span>    | <span data-ttu-id="1c9fa-161">無</span><span class="sxs-lookup"><span data-stu-id="1c9fa-161">None</span></span>     | <span data-ttu-id="1c9fa-162">Yes</span><span class="sxs-lookup"><span data-stu-id="1c9fa-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="1c9fa-163">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="1c9fa-163">Output Registers</span></span>



| <span data-ttu-id="1c9fa-164">註冊</span><span class="sxs-lookup"><span data-stu-id="1c9fa-164">Register</span></span> | <span data-ttu-id="1c9fa-165">Name</span><span class="sxs-lookup"><span data-stu-id="1c9fa-165">Name</span></span>            | <span data-ttu-id="1c9fa-166">Count</span><span class="sxs-lookup"><span data-stu-id="1c9fa-166">Count</span></span> | <span data-ttu-id="1c9fa-167">R/W</span><span class="sxs-lookup"><span data-stu-id="1c9fa-167">R/W</span></span> | <span data-ttu-id="1c9fa-168">維度</span><span class="sxs-lookup"><span data-stu-id="1c9fa-168">Dimension</span></span> | <span data-ttu-id="1c9fa-169">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="1c9fa-169">Indexable by r\#</span></span> | <span data-ttu-id="1c9fa-170">Defaults</span><span class="sxs-lookup"><span data-stu-id="1c9fa-170">Defaults</span></span> | <span data-ttu-id="1c9fa-171">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="1c9fa-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="1c9fa-172">NULL</span><span class="sxs-lookup"><span data-stu-id="1c9fa-172">NULL</span></span>     | <span data-ttu-id="1c9fa-173">捨棄結果</span><span class="sxs-lookup"><span data-stu-id="1c9fa-173">Discard Result</span></span>  | <span data-ttu-id="1c9fa-174">N/A</span><span class="sxs-lookup"><span data-stu-id="1c9fa-174">N/A</span></span>   | <span data-ttu-id="1c9fa-175">W</span><span class="sxs-lookup"><span data-stu-id="1c9fa-175">W</span></span>   | <span data-ttu-id="1c9fa-176">N/A</span><span class="sxs-lookup"><span data-stu-id="1c9fa-176">N/A</span></span>       | <span data-ttu-id="1c9fa-177">N/A</span><span class="sxs-lookup"><span data-stu-id="1c9fa-177">N/A</span></span>              | <span data-ttu-id="1c9fa-178">N/A</span><span class="sxs-lookup"><span data-stu-id="1c9fa-178">N/A</span></span>      | <span data-ttu-id="1c9fa-179">否</span><span class="sxs-lookup"><span data-stu-id="1c9fa-179">No</span></span>           |
| <span data-ttu-id="1c9fa-180">輸出\#</span><span class="sxs-lookup"><span data-stu-id="1c9fa-180">o\#</span></span>      | <span data-ttu-id="1c9fa-181">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="1c9fa-181">Output Register</span></span> | <span data-ttu-id="1c9fa-182">32</span><span class="sxs-lookup"><span data-stu-id="1c9fa-182">32</span></span>    | <span data-ttu-id="1c9fa-183">W</span><span class="sxs-lookup"><span data-stu-id="1c9fa-183">W</span></span>   | <span data-ttu-id="1c9fa-184">N/A</span><span class="sxs-lookup"><span data-stu-id="1c9fa-184">N/A</span></span>       | <span data-ttu-id="1c9fa-185">N/A</span><span class="sxs-lookup"><span data-stu-id="1c9fa-185">N/A</span></span>              | <span data-ttu-id="1c9fa-186">4</span><span class="sxs-lookup"><span data-stu-id="1c9fa-186">4</span></span>        | <span data-ttu-id="1c9fa-187">是</span><span class="sxs-lookup"><span data-stu-id="1c9fa-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="1c9fa-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c9fa-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c9fa-189">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1c9fa-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




