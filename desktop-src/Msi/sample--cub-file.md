---
description: 此範例說明包含兩個等的 .cub 檔案配置。 安裝程式會執行序列中的自訂動作： ICE01 和 ICE08。
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: 範例 .cub 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943381"
---
# <a name="sample-cub-file"></a><span data-ttu-id="e6abd-104">範例 .cub 檔案</span><span class="sxs-lookup"><span data-stu-id="e6abd-104">Sample .cub File</span></span>

<span data-ttu-id="e6abd-105">此範例說明 [包含兩個](internal-consistency-evaluators-ices.md)等的 .cub 檔案配置。</span><span class="sxs-lookup"><span data-stu-id="e6abd-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="e6abd-106">安裝程式會執行序列中的自訂動作： ICE01 和 ICE08。</span><span class="sxs-lookup"><span data-stu-id="e6abd-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="e6abd-107">自訂動作 ICE01 是 [自訂動作類型 1](custom-action-type-1.md)。</span><span class="sxs-lookup"><span data-stu-id="e6abd-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="e6abd-108">它是在 .cub 檔案中儲存為數據流的 DLL 進入點。</span><span class="sxs-lookup"><span data-stu-id="e6abd-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="e6abd-109">此資料流程會列在 ice.dll 的二進位資料表中。</span><span class="sxs-lookup"><span data-stu-id="e6abd-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="e6abd-110">自訂動作 ICE08 是 [自訂動作類型 6](custom-action-type-6.md)。</span><span class="sxs-lookup"><span data-stu-id="e6abd-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="e6abd-111">它是 VBScript 中函式的進入點，會在 .cub 檔案中儲存為數據流。</span><span class="sxs-lookup"><span data-stu-id="e6abd-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="e6abd-112">此資料流程會以 ice.vbs 的形式列于二進位資料表中。</span><span class="sxs-lookup"><span data-stu-id="e6abd-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="e6abd-113">二進位資料表</span><span class="sxs-lookup"><span data-stu-id="e6abd-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="e6abd-114">Name</span><span class="sxs-lookup"><span data-stu-id="e6abd-114">Name</span></span>    | <span data-ttu-id="e6abd-115">資料</span><span class="sxs-lookup"><span data-stu-id="e6abd-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="e6abd-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="e6abd-116">ice.vbs</span></span> | <span data-ttu-id="e6abd-117">ice.vbs 的未格式化二進位資料</span><span class="sxs-lookup"><span data-stu-id="e6abd-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="e6abd-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="e6abd-118">ice.dll</span></span> | <span data-ttu-id="e6abd-119">ice.dll 的未格式化二進位資料</span><span class="sxs-lookup"><span data-stu-id="e6abd-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="e6abd-120">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="e6abd-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="e6abd-121">動作</span><span class="sxs-lookup"><span data-stu-id="e6abd-121">Action</span></span> | <span data-ttu-id="e6abd-122">類型</span><span class="sxs-lookup"><span data-stu-id="e6abd-122">Type</span></span> | <span data-ttu-id="e6abd-123">來源</span><span class="sxs-lookup"><span data-stu-id="e6abd-123">Source</span></span>  | <span data-ttu-id="e6abd-124">目標</span><span class="sxs-lookup"><span data-stu-id="e6abd-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="e6abd-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="e6abd-125">ICE01</span></span>  | <span data-ttu-id="e6abd-126">1</span><span class="sxs-lookup"><span data-stu-id="e6abd-126">1</span></span>    | <span data-ttu-id="e6abd-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="e6abd-127">ice.dll</span></span> | <span data-ttu-id="e6abd-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="e6abd-128">ICE01</span></span>  |
| <span data-ttu-id="e6abd-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="e6abd-129">ICE08</span></span>  | <span data-ttu-id="e6abd-130">6</span><span class="sxs-lookup"><span data-stu-id="e6abd-130">6</span></span>    | <span data-ttu-id="e6abd-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="e6abd-131">ice.vbs</span></span> | <span data-ttu-id="e6abd-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="e6abd-132">ICE02</span></span>  |



 

<span data-ttu-id="e6abd-133">\_ICESequence 資料表</span><span class="sxs-lookup"><span data-stu-id="e6abd-133">\_ICESequence Table</span></span>



| <span data-ttu-id="e6abd-134">動作</span><span class="sxs-lookup"><span data-stu-id="e6abd-134">Action</span></span> | <span data-ttu-id="e6abd-135">條件</span><span class="sxs-lookup"><span data-stu-id="e6abd-135">Condition</span></span> | <span data-ttu-id="e6abd-136">順序</span><span class="sxs-lookup"><span data-stu-id="e6abd-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="e6abd-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="e6abd-137">ICE01</span></span>  |           | <span data-ttu-id="e6abd-138">10</span><span class="sxs-lookup"><span data-stu-id="e6abd-138">10</span></span>       |
| <span data-ttu-id="e6abd-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="e6abd-139">ICE08</span></span>  |           | <span data-ttu-id="e6abd-140">20</span><span class="sxs-lookup"><span data-stu-id="e6abd-140">20</span></span>       |



 

<span data-ttu-id="e6abd-141">\_特殊資料表</span><span class="sxs-lookup"><span data-stu-id="e6abd-141">\_Special Table</span></span>

<span data-ttu-id="e6abd-142">ICE01 和 ICE08 不需要包含特殊的處理資料表。</span><span class="sxs-lookup"><span data-stu-id="e6abd-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="e6abd-143">當 .cub 檔案包含特殊資料表時，它們也必須包含在 \_ 驗證資料表中。</span><span class="sxs-lookup"><span data-stu-id="e6abd-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="e6abd-144">\_驗證資料表</span><span class="sxs-lookup"><span data-stu-id="e6abd-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="e6abd-145">資料表</span><span class="sxs-lookup"><span data-stu-id="e6abd-145">Table</span></span>         | <span data-ttu-id="e6abd-146">資料行</span><span class="sxs-lookup"><span data-stu-id="e6abd-146">Column</span></span>    | <span data-ttu-id="e6abd-147">Nullable</span><span class="sxs-lookup"><span data-stu-id="e6abd-147">Nullable</span></span> | <span data-ttu-id="e6abd-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="e6abd-148">MinValue</span></span> | <span data-ttu-id="e6abd-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e6abd-149">MaxValue</span></span> | <span data-ttu-id="e6abd-150">KeyTable</span><span class="sxs-lookup"><span data-stu-id="e6abd-150">KeyTable</span></span> | <span data-ttu-id="e6abd-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="e6abd-151">KeyColumn</span></span> | <span data-ttu-id="e6abd-152">類別</span><span class="sxs-lookup"><span data-stu-id="e6abd-152">Category</span></span>                         | <span data-ttu-id="e6abd-153">設定</span><span class="sxs-lookup"><span data-stu-id="e6abd-153">Set</span></span> | <span data-ttu-id="e6abd-154">Description</span><span class="sxs-lookup"><span data-stu-id="e6abd-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="e6abd-155">Binary</span><span class="sxs-lookup"><span data-stu-id="e6abd-155">Binary</span></span>        | <span data-ttu-id="e6abd-156">Name</span><span class="sxs-lookup"><span data-stu-id="e6abd-156">Name</span></span>      | <span data-ttu-id="e6abd-157">N</span><span class="sxs-lookup"><span data-stu-id="e6abd-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-158">識別碼</span><span class="sxs-lookup"><span data-stu-id="e6abd-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="e6abd-159">Binary</span><span class="sxs-lookup"><span data-stu-id="e6abd-159">Binary</span></span>        | <span data-ttu-id="e6abd-160">資料</span><span class="sxs-lookup"><span data-stu-id="e6abd-160">Data</span></span>      | <span data-ttu-id="e6abd-161">N</span><span class="sxs-lookup"><span data-stu-id="e6abd-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-162">二進位</span><span class="sxs-lookup"><span data-stu-id="e6abd-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="e6abd-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="e6abd-163">CustomAction</span></span>  | <span data-ttu-id="e6abd-164">動作</span><span class="sxs-lookup"><span data-stu-id="e6abd-164">Action</span></span>    | <span data-ttu-id="e6abd-165">N</span><span class="sxs-lookup"><span data-stu-id="e6abd-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-166">識別碼</span><span class="sxs-lookup"><span data-stu-id="e6abd-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="e6abd-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="e6abd-167">CustomAction</span></span>  | <span data-ttu-id="e6abd-168">類型</span><span class="sxs-lookup"><span data-stu-id="e6abd-168">Type</span></span>      | <span data-ttu-id="e6abd-169">N</span><span class="sxs-lookup"><span data-stu-id="e6abd-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-170">整數</span><span class="sxs-lookup"><span data-stu-id="e6abd-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="e6abd-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="e6abd-171">CustomAction</span></span>  | <span data-ttu-id="e6abd-172">來源</span><span class="sxs-lookup"><span data-stu-id="e6abd-172">Source</span></span>    | <span data-ttu-id="e6abd-173">Y</span><span class="sxs-lookup"><span data-stu-id="e6abd-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-174">CustomSource</span><span class="sxs-lookup"><span data-stu-id="e6abd-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="e6abd-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="e6abd-175">CustomAction</span></span>  | <span data-ttu-id="e6abd-176">目標</span><span class="sxs-lookup"><span data-stu-id="e6abd-176">Target</span></span>    | <span data-ttu-id="e6abd-177">Y</span><span class="sxs-lookup"><span data-stu-id="e6abd-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-178">格式 化</span><span class="sxs-lookup"><span data-stu-id="e6abd-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="e6abd-179">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="e6abd-179">\_ICESequence</span></span> | <span data-ttu-id="e6abd-180">動作</span><span class="sxs-lookup"><span data-stu-id="e6abd-180">Action</span></span>    | <span data-ttu-id="e6abd-181">N</span><span class="sxs-lookup"><span data-stu-id="e6abd-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-182">識別碼</span><span class="sxs-lookup"><span data-stu-id="e6abd-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="e6abd-183">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="e6abd-183">\_ICESequence</span></span> | <span data-ttu-id="e6abd-184">條件</span><span class="sxs-lookup"><span data-stu-id="e6abd-184">Condition</span></span> | <span data-ttu-id="e6abd-185">Y</span><span class="sxs-lookup"><span data-stu-id="e6abd-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-186">Condition</span><span class="sxs-lookup"><span data-stu-id="e6abd-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="e6abd-187">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="e6abd-187">\_ICESequence</span></span> | <span data-ttu-id="e6abd-188">順序</span><span class="sxs-lookup"><span data-stu-id="e6abd-188">Sequence</span></span>  | <span data-ttu-id="e6abd-189">Y</span><span class="sxs-lookup"><span data-stu-id="e6abd-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="e6abd-190">整數</span><span class="sxs-lookup"><span data-stu-id="e6abd-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



