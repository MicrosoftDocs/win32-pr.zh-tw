---
title: 註冊-vs_4_0
description: 本章節包含頂點著色器 4 0 所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990615"
---
# <a name="registers---vs_4_0"></a><span data-ttu-id="39ca2-103">暫存器-vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="39ca2-103">Registers - vs\_4\_0</span></span>

<span data-ttu-id="39ca2-104">本章節包含頂點著色器 4 0 所實之輸入和輸出暫存器的參考資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="39ca2-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="39ca2-105">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="39ca2-105">Input Registers</span></span>



| <span data-ttu-id="39ca2-106">註冊</span><span class="sxs-lookup"><span data-stu-id="39ca2-106">Register</span></span>      | <span data-ttu-id="39ca2-107">Name</span><span class="sxs-lookup"><span data-stu-id="39ca2-107">Name</span></span> | <span data-ttu-id="39ca2-108">Count</span><span class="sxs-lookup"><span data-stu-id="39ca2-108">Count</span></span>              | <span data-ttu-id="39ca2-109">R/W</span><span class="sxs-lookup"><span data-stu-id="39ca2-109">R/W</span></span> | <span data-ttu-id="39ca2-110">維度</span><span class="sxs-lookup"><span data-stu-id="39ca2-110">Dimension</span></span> | <span data-ttu-id="39ca2-111">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="39ca2-111">Indexable by r\#</span></span> | <span data-ttu-id="39ca2-112">Defaults</span><span class="sxs-lookup"><span data-stu-id="39ca2-112">Defaults</span></span> | <span data-ttu-id="39ca2-113">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="39ca2-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="39ca2-114">R\#</span><span class="sxs-lookup"><span data-stu-id="39ca2-114">r\#</span></span>           |      | <span data-ttu-id="39ca2-115">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="39ca2-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="39ca2-116">R/W</span><span class="sxs-lookup"><span data-stu-id="39ca2-116">R/W</span></span> | <span data-ttu-id="39ca2-117">4</span><span class="sxs-lookup"><span data-stu-id="39ca2-117">4</span></span>         | <span data-ttu-id="39ca2-118">否</span><span class="sxs-lookup"><span data-stu-id="39ca2-118">No</span></span>               | <span data-ttu-id="39ca2-119">None</span><span class="sxs-lookup"><span data-stu-id="39ca2-119">None</span></span>     | <span data-ttu-id="39ca2-120">Yes</span><span class="sxs-lookup"><span data-stu-id="39ca2-120">Yes</span></span>          |
| <span data-ttu-id="39ca2-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="39ca2-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="39ca2-122">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="39ca2-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="39ca2-123">R/W</span><span class="sxs-lookup"><span data-stu-id="39ca2-123">R/W</span></span> | <span data-ttu-id="39ca2-124">4</span><span class="sxs-lookup"><span data-stu-id="39ca2-124">4</span></span>         | <span data-ttu-id="39ca2-125">是</span><span class="sxs-lookup"><span data-stu-id="39ca2-125">Yes</span></span>              | <span data-ttu-id="39ca2-126">無</span><span class="sxs-lookup"><span data-stu-id="39ca2-126">None</span></span>     | <span data-ttu-id="39ca2-127">Yes</span><span class="sxs-lookup"><span data-stu-id="39ca2-127">Yes</span></span>          |
| <span data-ttu-id="39ca2-128">V\#</span><span class="sxs-lookup"><span data-stu-id="39ca2-128">v\#</span></span>           |      | <span data-ttu-id="39ca2-129">16</span><span class="sxs-lookup"><span data-stu-id="39ca2-129">16</span></span>                 | <span data-ttu-id="39ca2-130">R</span><span class="sxs-lookup"><span data-stu-id="39ca2-130">R</span></span>   | <span data-ttu-id="39ca2-131">4</span><span class="sxs-lookup"><span data-stu-id="39ca2-131">4</span></span>         | <span data-ttu-id="39ca2-132">是</span><span class="sxs-lookup"><span data-stu-id="39ca2-132">Yes</span></span>              | <span data-ttu-id="39ca2-133">無</span><span class="sxs-lookup"><span data-stu-id="39ca2-133">None</span></span>     | <span data-ttu-id="39ca2-134">Yes</span><span class="sxs-lookup"><span data-stu-id="39ca2-134">Yes</span></span>          |
| <span data-ttu-id="39ca2-135">10gbase-t\#</span><span class="sxs-lookup"><span data-stu-id="39ca2-135">t\#</span></span>           |      | <span data-ttu-id="39ca2-136">128</span><span class="sxs-lookup"><span data-stu-id="39ca2-136">128</span></span>                | <span data-ttu-id="39ca2-137">R</span><span class="sxs-lookup"><span data-stu-id="39ca2-137">R</span></span>   | <span data-ttu-id="39ca2-138">1</span><span class="sxs-lookup"><span data-stu-id="39ca2-138">1</span></span>         | <span data-ttu-id="39ca2-139">否</span><span class="sxs-lookup"><span data-stu-id="39ca2-139">No</span></span>               | <span data-ttu-id="39ca2-140">None</span><span class="sxs-lookup"><span data-stu-id="39ca2-140">None</span></span>     | <span data-ttu-id="39ca2-141">Yes</span><span class="sxs-lookup"><span data-stu-id="39ca2-141">Yes</span></span>          |
| <span data-ttu-id="39ca2-142">s\#</span><span class="sxs-lookup"><span data-stu-id="39ca2-142">s\#</span></span>           |      | <span data-ttu-id="39ca2-143">16</span><span class="sxs-lookup"><span data-stu-id="39ca2-143">16</span></span>                 | <span data-ttu-id="39ca2-144">R</span><span class="sxs-lookup"><span data-stu-id="39ca2-144">R</span></span>   | <span data-ttu-id="39ca2-145">1</span><span class="sxs-lookup"><span data-stu-id="39ca2-145">1</span></span>         | <span data-ttu-id="39ca2-146">否</span><span class="sxs-lookup"><span data-stu-id="39ca2-146">No</span></span>               | <span data-ttu-id="39ca2-147">None</span><span class="sxs-lookup"><span data-stu-id="39ca2-147">None</span></span>     | <span data-ttu-id="39ca2-148">Yes</span><span class="sxs-lookup"><span data-stu-id="39ca2-148">Yes</span></span>          |
| <span data-ttu-id="39ca2-149">cb \# \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="39ca2-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="39ca2-150">15</span><span class="sxs-lookup"><span data-stu-id="39ca2-150">15</span></span>                 | <span data-ttu-id="39ca2-151">R</span><span class="sxs-lookup"><span data-stu-id="39ca2-151">R</span></span>   | <span data-ttu-id="39ca2-152">4</span><span class="sxs-lookup"><span data-stu-id="39ca2-152">4</span></span>         | <span data-ttu-id="39ca2-153">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="39ca2-153">Yes(Contents)</span></span>    | <span data-ttu-id="39ca2-154">無</span><span class="sxs-lookup"><span data-stu-id="39ca2-154">None</span></span>     | <span data-ttu-id="39ca2-155">Yes</span><span class="sxs-lookup"><span data-stu-id="39ca2-155">Yes</span></span>          |
| <span data-ttu-id="39ca2-156">icb \[ 索引\]</span><span class="sxs-lookup"><span data-stu-id="39ca2-156">icb\[index\]</span></span>  |      | <span data-ttu-id="39ca2-157">1</span><span class="sxs-lookup"><span data-stu-id="39ca2-157">1</span></span>                  | <span data-ttu-id="39ca2-158">R</span><span class="sxs-lookup"><span data-stu-id="39ca2-158">R</span></span>   | <span data-ttu-id="39ca2-159">4</span><span class="sxs-lookup"><span data-stu-id="39ca2-159">4</span></span>         | <span data-ttu-id="39ca2-160">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="39ca2-160">Yes(Contents)</span></span>    | <span data-ttu-id="39ca2-161">無</span><span class="sxs-lookup"><span data-stu-id="39ca2-161">None</span></span>     | <span data-ttu-id="39ca2-162">Yes</span><span class="sxs-lookup"><span data-stu-id="39ca2-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="39ca2-163">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="39ca2-163">Output Registers</span></span>



| <span data-ttu-id="39ca2-164">註冊</span><span class="sxs-lookup"><span data-stu-id="39ca2-164">Register</span></span> | <span data-ttu-id="39ca2-165">Name</span><span class="sxs-lookup"><span data-stu-id="39ca2-165">Name</span></span>            | <span data-ttu-id="39ca2-166">Count</span><span class="sxs-lookup"><span data-stu-id="39ca2-166">Count</span></span> | <span data-ttu-id="39ca2-167">R/W</span><span class="sxs-lookup"><span data-stu-id="39ca2-167">R/W</span></span> | <span data-ttu-id="39ca2-168">維度</span><span class="sxs-lookup"><span data-stu-id="39ca2-168">Dimension</span></span> | <span data-ttu-id="39ca2-169">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="39ca2-169">Indexable by r\#</span></span> | <span data-ttu-id="39ca2-170">Defaults</span><span class="sxs-lookup"><span data-stu-id="39ca2-170">Defaults</span></span> | <span data-ttu-id="39ca2-171">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="39ca2-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="39ca2-172">NULL</span><span class="sxs-lookup"><span data-stu-id="39ca2-172">NULL</span></span>     | <span data-ttu-id="39ca2-173">捨棄結果</span><span class="sxs-lookup"><span data-stu-id="39ca2-173">Discard Result</span></span>  | <span data-ttu-id="39ca2-174">N/A</span><span class="sxs-lookup"><span data-stu-id="39ca2-174">N/A</span></span>   | <span data-ttu-id="39ca2-175">W</span><span class="sxs-lookup"><span data-stu-id="39ca2-175">W</span></span>   | <span data-ttu-id="39ca2-176">N/A</span><span class="sxs-lookup"><span data-stu-id="39ca2-176">N/A</span></span>       | <span data-ttu-id="39ca2-177">N/A</span><span class="sxs-lookup"><span data-stu-id="39ca2-177">N/A</span></span>              | <span data-ttu-id="39ca2-178">N/A</span><span class="sxs-lookup"><span data-stu-id="39ca2-178">N/A</span></span>      | <span data-ttu-id="39ca2-179">否</span><span class="sxs-lookup"><span data-stu-id="39ca2-179">No</span></span>           |
| <span data-ttu-id="39ca2-180">輸出\#</span><span class="sxs-lookup"><span data-stu-id="39ca2-180">o\#</span></span>      | <span data-ttu-id="39ca2-181">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="39ca2-181">Output Register</span></span> | <span data-ttu-id="39ca2-182">16</span><span class="sxs-lookup"><span data-stu-id="39ca2-182">16</span></span>    | <span data-ttu-id="39ca2-183">W</span><span class="sxs-lookup"><span data-stu-id="39ca2-183">W</span></span>   | <span data-ttu-id="39ca2-184">N/A</span><span class="sxs-lookup"><span data-stu-id="39ca2-184">N/A</span></span>       | <span data-ttu-id="39ca2-185">N/A</span><span class="sxs-lookup"><span data-stu-id="39ca2-185">N/A</span></span>              | <span data-ttu-id="39ca2-186">4</span><span class="sxs-lookup"><span data-stu-id="39ca2-186">4</span></span>        | <span data-ttu-id="39ca2-187">是</span><span class="sxs-lookup"><span data-stu-id="39ca2-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="39ca2-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="39ca2-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39ca2-189">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="39ca2-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




