---
title: 註冊-vs_5_0
description: 下列輸入和輸出暫存器會在頂點著色器版本 5 0 中實作為 \_ 。
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1dc211f5f3dd8819577c796849dcb86012cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971440"
---
# <a name="registers---vs_5_0"></a><span data-ttu-id="3263a-103">註冊-vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3263a-103">Registers - vs\_5\_0</span></span>

<span data-ttu-id="3263a-104">下列輸入和輸出暫存器會在頂點著色器版本 5 0 中實作為 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3263a-104">The following input and output registers are implemented in the vertex shader version 5\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="3263a-105">輸入暫存器</span><span class="sxs-lookup"><span data-stu-id="3263a-105">Input Registers</span></span>



| <span data-ttu-id="3263a-106">註冊類型</span><span class="sxs-lookup"><span data-stu-id="3263a-106">Register Type</span></span>                                      | <span data-ttu-id="3263a-107">Count</span><span class="sxs-lookup"><span data-stu-id="3263a-107">Count</span></span>              | <span data-ttu-id="3263a-108">R/W</span><span class="sxs-lookup"><span data-stu-id="3263a-108">R/W</span></span> | <span data-ttu-id="3263a-109">維度</span><span class="sxs-lookup"><span data-stu-id="3263a-109">Dimension</span></span> | <span data-ttu-id="3263a-110">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="3263a-110">Indexable by r\#</span></span> | <span data-ttu-id="3263a-111">Defaults</span><span class="sxs-lookup"><span data-stu-id="3263a-111">Defaults</span></span> | <span data-ttu-id="3263a-112">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="3263a-112">Requires DCL</span></span> |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="3263a-113">32位 Temp (r \#) </span><span class="sxs-lookup"><span data-stu-id="3263a-113">32-bit Temp (r\#)</span></span>                                  | <span data-ttu-id="3263a-114">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="3263a-114">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="3263a-115">R/W</span><span class="sxs-lookup"><span data-stu-id="3263a-115">R/W</span></span> | <span data-ttu-id="3263a-116">4</span><span class="sxs-lookup"><span data-stu-id="3263a-116">4</span></span>         | <span data-ttu-id="3263a-117">否</span><span class="sxs-lookup"><span data-stu-id="3263a-117">No</span></span>               | <span data-ttu-id="3263a-118">None</span><span class="sxs-lookup"><span data-stu-id="3263a-118">None</span></span>     | <span data-ttu-id="3263a-119">Yes</span><span class="sxs-lookup"><span data-stu-id="3263a-119">Yes</span></span>          |
| <span data-ttu-id="3263a-120">32位可編制索引的暫存陣列 (x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="3263a-120">32-bit indexable Temp Array (x\#\[n\])</span></span>             | <span data-ttu-id="3263a-121">4096 (r \# + x \# \[ n \]) </span><span class="sxs-lookup"><span data-stu-id="3263a-121">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="3263a-122">R/W</span><span class="sxs-lookup"><span data-stu-id="3263a-122">R/W</span></span> | <span data-ttu-id="3263a-123">4</span><span class="sxs-lookup"><span data-stu-id="3263a-123">4</span></span>         | <span data-ttu-id="3263a-124">是</span><span class="sxs-lookup"><span data-stu-id="3263a-124">Yes</span></span>              | <span data-ttu-id="3263a-125">無</span><span class="sxs-lookup"><span data-stu-id="3263a-125">None</span></span>     | <span data-ttu-id="3263a-126">Yes</span><span class="sxs-lookup"><span data-stu-id="3263a-126">Yes</span></span>          |
| <span data-ttu-id="3263a-127">32位輸入 (v \#) </span><span class="sxs-lookup"><span data-stu-id="3263a-127">32-bit input (v\#)</span></span>                                 | <span data-ttu-id="3263a-128">32</span><span class="sxs-lookup"><span data-stu-id="3263a-128">32</span></span>                 | <span data-ttu-id="3263a-129">R</span><span class="sxs-lookup"><span data-stu-id="3263a-129">R</span></span>   | <span data-ttu-id="3263a-130">4</span><span class="sxs-lookup"><span data-stu-id="3263a-130">4</span></span>         | <span data-ttu-id="3263a-131">是</span><span class="sxs-lookup"><span data-stu-id="3263a-131">Yes</span></span>              | <span data-ttu-id="3263a-132">無</span><span class="sxs-lookup"><span data-stu-id="3263a-132">None</span></span>     | <span data-ttu-id="3263a-133">Yes</span><span class="sxs-lookup"><span data-stu-id="3263a-133">Yes</span></span>          |
| <span data-ttu-id="3263a-134">輸入資源中的元素 (t \#) </span><span class="sxs-lookup"><span data-stu-id="3263a-134">Element in an input resource (t\#)</span></span>                 | <span data-ttu-id="3263a-135">128</span><span class="sxs-lookup"><span data-stu-id="3263a-135">128</span></span>                | <span data-ttu-id="3263a-136">R</span><span class="sxs-lookup"><span data-stu-id="3263a-136">R</span></span>   | <span data-ttu-id="3263a-137">1</span><span class="sxs-lookup"><span data-stu-id="3263a-137">1</span></span>         | <span data-ttu-id="3263a-138">否</span><span class="sxs-lookup"><span data-stu-id="3263a-138">No</span></span>               | <span data-ttu-id="3263a-139">None</span><span class="sxs-lookup"><span data-stu-id="3263a-139">None</span></span>     | <span data-ttu-id="3263a-140">Yes</span><span class="sxs-lookup"><span data-stu-id="3263a-140">Yes</span></span>          |
| <span data-ttu-id="3263a-141">取樣器 (s \#) </span><span class="sxs-lookup"><span data-stu-id="3263a-141">Sampler (s\#)</span></span>                                      | <span data-ttu-id="3263a-142">16</span><span class="sxs-lookup"><span data-stu-id="3263a-142">16</span></span>                 | <span data-ttu-id="3263a-143">R</span><span class="sxs-lookup"><span data-stu-id="3263a-143">R</span></span>   | <span data-ttu-id="3263a-144">1</span><span class="sxs-lookup"><span data-stu-id="3263a-144">1</span></span>         | <span data-ttu-id="3263a-145">否</span><span class="sxs-lookup"><span data-stu-id="3263a-145">No</span></span>               | <span data-ttu-id="3263a-146">None</span><span class="sxs-lookup"><span data-stu-id="3263a-146">None</span></span>     | <span data-ttu-id="3263a-147">Yes</span><span class="sxs-lookup"><span data-stu-id="3263a-147">Yes</span></span>          |
| <span data-ttu-id="3263a-148">ConstantBuffer 參考 (cb \# \[ 索引 \]) </span><span class="sxs-lookup"><span data-stu-id="3263a-148">ConstantBuffer reference (cb\#\[index\])</span></span>           | <span data-ttu-id="3263a-149">15</span><span class="sxs-lookup"><span data-stu-id="3263a-149">15</span></span>                 | <span data-ttu-id="3263a-150">R</span><span class="sxs-lookup"><span data-stu-id="3263a-150">R</span></span>   | <span data-ttu-id="3263a-151">4</span><span class="sxs-lookup"><span data-stu-id="3263a-151">4</span></span>         | <span data-ttu-id="3263a-152">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="3263a-152">Yes(contents)</span></span>    | <span data-ttu-id="3263a-153">無</span><span class="sxs-lookup"><span data-stu-id="3263a-153">None</span></span>     | <span data-ttu-id="3263a-154">Yes</span><span class="sxs-lookup"><span data-stu-id="3263a-154">Yes</span></span>          |
| <span data-ttu-id="3263a-155">iImmediate ConstantBuffer 參考 (的 icb \[ 索引 \]) </span><span class="sxs-lookup"><span data-stu-id="3263a-155">iImmediate ConstantBuffer reference (icb\[index\])</span></span> | <span data-ttu-id="3263a-156">1</span><span class="sxs-lookup"><span data-stu-id="3263a-156">1</span></span>                  | <span data-ttu-id="3263a-157">R</span><span class="sxs-lookup"><span data-stu-id="3263a-157">R</span></span>   | <span data-ttu-id="3263a-158">4</span><span class="sxs-lookup"><span data-stu-id="3263a-158">4</span></span>         | <span data-ttu-id="3263a-159">是 (內容) </span><span class="sxs-lookup"><span data-stu-id="3263a-159">Yes(contents)</span></span>    | <span data-ttu-id="3263a-160">無</span><span class="sxs-lookup"><span data-stu-id="3263a-160">None</span></span>     | <span data-ttu-id="3263a-161">Yes</span><span class="sxs-lookup"><span data-stu-id="3263a-161">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="3263a-162">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="3263a-162">Output Registers</span></span>



| <span data-ttu-id="3263a-163">註冊類型</span><span class="sxs-lookup"><span data-stu-id="3263a-163">Register Type</span></span>                                                      | <span data-ttu-id="3263a-164">Count</span><span class="sxs-lookup"><span data-stu-id="3263a-164">Count</span></span> | <span data-ttu-id="3263a-165">R/W</span><span class="sxs-lookup"><span data-stu-id="3263a-165">R/W</span></span> | <span data-ttu-id="3263a-166">維度</span><span class="sxs-lookup"><span data-stu-id="3263a-166">Dimension</span></span> | <span data-ttu-id="3263a-167">R 可編制索引\#</span><span class="sxs-lookup"><span data-stu-id="3263a-167">Indexable by r\#</span></span> | <span data-ttu-id="3263a-168">Defaults</span><span class="sxs-lookup"><span data-stu-id="3263a-168">Defaults</span></span> | <span data-ttu-id="3263a-169">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="3263a-169">Requires DCL</span></span> |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="3263a-170">Null (捨棄結果，適用于具有多個結果的作業) </span><span class="sxs-lookup"><span data-stu-id="3263a-170">NULL (discard result, useful for operations with multiple results)</span></span> | <span data-ttu-id="3263a-171">N/A</span><span class="sxs-lookup"><span data-stu-id="3263a-171">N/A</span></span>   | <span data-ttu-id="3263a-172">W</span><span class="sxs-lookup"><span data-stu-id="3263a-172">W</span></span>   | <span data-ttu-id="3263a-173">N/A</span><span class="sxs-lookup"><span data-stu-id="3263a-173">N/A</span></span>       | <span data-ttu-id="3263a-174">N/A</span><span class="sxs-lookup"><span data-stu-id="3263a-174">N/A</span></span>              | <span data-ttu-id="3263a-175">N/A</span><span class="sxs-lookup"><span data-stu-id="3263a-175">N/A</span></span>      | <span data-ttu-id="3263a-176">否</span><span class="sxs-lookup"><span data-stu-id="3263a-176">No</span></span>           |
| <span data-ttu-id="3263a-177">32位輸出頂點資料元素 (o \#) </span><span class="sxs-lookup"><span data-stu-id="3263a-177">32-bit output Vertex Data Element (o\#)</span></span>                            | <span data-ttu-id="3263a-178">32</span><span class="sxs-lookup"><span data-stu-id="3263a-178">32</span></span>    | <span data-ttu-id="3263a-179">W</span><span class="sxs-lookup"><span data-stu-id="3263a-179">W</span></span>   | <span data-ttu-id="3263a-180">4</span><span class="sxs-lookup"><span data-stu-id="3263a-180">4</span></span>         | <span data-ttu-id="3263a-181">N/A</span><span class="sxs-lookup"><span data-stu-id="3263a-181">N/A</span></span>              | <span data-ttu-id="3263a-182">N/A</span><span class="sxs-lookup"><span data-stu-id="3263a-182">N/A</span></span>      | <span data-ttu-id="3263a-183">是</span><span class="sxs-lookup"><span data-stu-id="3263a-183">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="3263a-184">相關主題</span><span class="sxs-lookup"><span data-stu-id="3263a-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3263a-185">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3263a-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




