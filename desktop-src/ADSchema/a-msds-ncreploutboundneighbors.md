---
title: ms DS-NC-複寫-輸出-相鄰屬性
description: 此分割區的複寫協力電腦。 此伺服器會將複寫資料傳送到其他可作為目的地的伺服器。 當有新的資料可用時，此伺服器會通知這些其他伺服器。
ms.assetid: 9dcc7485-1999-47ff-bb57-8193768a15a9
ms.tgt_platform: multiple
keywords:
- ms DS-NC-複寫-輸出-相鄰屬性 AD 架構
- NCReplOutboundNeighbors 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Outbound-Neighbors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fd37ccab1b3faef6ca2c84a52c05249a52ff38a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845155"
---
# <a name="ms-ds-nc-repl-outbound-neighbors-attribute"></a><span data-ttu-id="981ab-107">ms DS-NC-複寫-輸出-相鄰屬性</span><span class="sxs-lookup"><span data-stu-id="981ab-107">ms-DS-NC-Repl-Outbound-Neighbors attribute</span></span>

<span data-ttu-id="981ab-108">此分割區的複寫協力電腦。</span><span class="sxs-lookup"><span data-stu-id="981ab-108">Replication partners for this partition.</span></span> <span data-ttu-id="981ab-109">此伺服器會將複寫資料傳送到其他可作為目的地的伺服器。</span><span class="sxs-lookup"><span data-stu-id="981ab-109">This server sends replication data to these other servers, which act as destinations.</span></span> <span data-ttu-id="981ab-110">當有新的資料可用時，此伺服器會通知這些其他伺服器。</span><span class="sxs-lookup"><span data-stu-id="981ab-110">This server will notify these other servers when new data is available.</span></span>



| <span data-ttu-id="981ab-111">進入</span><span class="sxs-lookup"><span data-stu-id="981ab-111">Entry</span></span> | <span data-ttu-id="981ab-112">值</span><span class="sxs-lookup"><span data-stu-id="981ab-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="981ab-113">CN</span><span class="sxs-lookup"><span data-stu-id="981ab-113">CN</span></span>                | <span data-ttu-id="981ab-114">ms DS-NC-複寫-輸出-相鄰</span><span class="sxs-lookup"><span data-stu-id="981ab-114">ms-DS-NC-Repl-Outbound-Neighbors</span></span>            |
| <span data-ttu-id="981ab-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="981ab-115">Ldap-Display-Name</span></span> | <span data-ttu-id="981ab-116">NCReplOutboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="981ab-116">msDS-NCReplOutboundNeighbors</span></span>                |
| <span data-ttu-id="981ab-117">大小</span><span class="sxs-lookup"><span data-stu-id="981ab-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="981ab-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="981ab-118">Update Privilege</span></span>  | <span data-ttu-id="981ab-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="981ab-119">This value is set by the system.</span></span>            |
| <span data-ttu-id="981ab-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="981ab-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="981ab-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="981ab-121">Attribute-Id</span></span>      | <span data-ttu-id="981ab-122">1.2.840.113556.1.4.1706</span><span class="sxs-lookup"><span data-stu-id="981ab-122">1.2.840.113556.1.4.1706</span></span>                     |
| <span data-ttu-id="981ab-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="981ab-123">System-Id-Guid</span></span>    | <span data-ttu-id="981ab-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span><span class="sxs-lookup"><span data-stu-id="981ab-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span></span>        |
| <span data-ttu-id="981ab-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="981ab-125">Syntax</span></span>            | [<span data-ttu-id="981ab-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="981ab-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="981ab-127">實作</span><span class="sxs-lookup"><span data-stu-id="981ab-127">Implementations</span></span>

-   [<span data-ttu-id="981ab-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="981ab-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="981ab-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="981ab-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="981ab-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="981ab-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="981ab-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="981ab-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="981ab-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="981ab-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="981ab-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="981ab-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="981ab-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="981ab-134">Windows Server 2003</span></span>



| <span data-ttu-id="981ab-135">進入</span><span class="sxs-lookup"><span data-stu-id="981ab-135">Entry</span></span> | <span data-ttu-id="981ab-136">值</span><span class="sxs-lookup"><span data-stu-id="981ab-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="981ab-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981ab-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981ab-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="981ab-139">System-Only</span></span>            | <span data-ttu-id="981ab-140">否</span><span class="sxs-lookup"><span data-stu-id="981ab-140">False</span></span>                           |
| <span data-ttu-id="981ab-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981ab-141">Is-Single-Valued</span></span>       | <span data-ttu-id="981ab-142">否</span><span class="sxs-lookup"><span data-stu-id="981ab-142">False</span></span>                           |
| <span data-ttu-id="981ab-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981ab-143">Is Indexed</span></span>             | <span data-ttu-id="981ab-144">否</span><span class="sxs-lookup"><span data-stu-id="981ab-144">False</span></span>                           |
| <span data-ttu-id="981ab-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981ab-145">In Global Catalog</span></span>      | <span data-ttu-id="981ab-146">否</span><span class="sxs-lookup"><span data-stu-id="981ab-146">False</span></span>                           |
| <span data-ttu-id="981ab-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981ab-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="981ab-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981ab-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="981ab-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981ab-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="981ab-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981ab-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="981ab-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-151">Search-Flags</span></span>           | <span data-ttu-id="981ab-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981ab-152">0x00000000</span></span>                      |
| <span data-ttu-id="981ab-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-153">System-Flags</span></span>           | <span data-ttu-id="981ab-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="981ab-154">0x00000014</span></span>                      |
| <span data-ttu-id="981ab-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981ab-155">Classes used in</span></span>        | [<span data-ttu-id="981ab-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="981ab-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="981ab-157">亞當</span><span class="sxs-lookup"><span data-stu-id="981ab-157">ADAM</span></span>



| <span data-ttu-id="981ab-158">進入</span><span class="sxs-lookup"><span data-stu-id="981ab-158">Entry</span></span> | <span data-ttu-id="981ab-159">值</span><span class="sxs-lookup"><span data-stu-id="981ab-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="981ab-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981ab-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981ab-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="981ab-162">System-Only</span></span>            | <span data-ttu-id="981ab-163">否</span><span class="sxs-lookup"><span data-stu-id="981ab-163">False</span></span>                           |
| <span data-ttu-id="981ab-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981ab-164">Is-Single-Valued</span></span>       | <span data-ttu-id="981ab-165">否</span><span class="sxs-lookup"><span data-stu-id="981ab-165">False</span></span>                           |
| <span data-ttu-id="981ab-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981ab-166">Is Indexed</span></span>             | <span data-ttu-id="981ab-167">否</span><span class="sxs-lookup"><span data-stu-id="981ab-167">False</span></span>                           |
| <span data-ttu-id="981ab-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981ab-168">In Global Catalog</span></span>      | <span data-ttu-id="981ab-169">否</span><span class="sxs-lookup"><span data-stu-id="981ab-169">False</span></span>                           |
| <span data-ttu-id="981ab-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981ab-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="981ab-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981ab-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="981ab-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981ab-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="981ab-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981ab-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="981ab-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-174">Search-Flags</span></span>           | <span data-ttu-id="981ab-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981ab-175">0x00000000</span></span>                      |
| <span data-ttu-id="981ab-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-176">System-Flags</span></span>           | <span data-ttu-id="981ab-177">0x00000014</span><span class="sxs-lookup"><span data-stu-id="981ab-177">0x00000014</span></span>                      |
| <span data-ttu-id="981ab-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981ab-178">Classes used in</span></span>        | [<span data-ttu-id="981ab-179">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="981ab-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="981ab-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="981ab-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="981ab-181">進入</span><span class="sxs-lookup"><span data-stu-id="981ab-181">Entry</span></span> | <span data-ttu-id="981ab-182">值</span><span class="sxs-lookup"><span data-stu-id="981ab-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="981ab-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981ab-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981ab-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="981ab-185">System-Only</span></span>            | <span data-ttu-id="981ab-186">否</span><span class="sxs-lookup"><span data-stu-id="981ab-186">False</span></span>                           |
| <span data-ttu-id="981ab-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981ab-187">Is-Single-Valued</span></span>       | <span data-ttu-id="981ab-188">否</span><span class="sxs-lookup"><span data-stu-id="981ab-188">False</span></span>                           |
| <span data-ttu-id="981ab-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981ab-189">Is Indexed</span></span>             | <span data-ttu-id="981ab-190">否</span><span class="sxs-lookup"><span data-stu-id="981ab-190">False</span></span>                           |
| <span data-ttu-id="981ab-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981ab-191">In Global Catalog</span></span>      | <span data-ttu-id="981ab-192">否</span><span class="sxs-lookup"><span data-stu-id="981ab-192">False</span></span>                           |
| <span data-ttu-id="981ab-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981ab-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="981ab-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981ab-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="981ab-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981ab-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="981ab-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981ab-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="981ab-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-197">Search-Flags</span></span>           | <span data-ttu-id="981ab-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981ab-198">0x00000000</span></span>                      |
| <span data-ttu-id="981ab-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-199">System-Flags</span></span>           | <span data-ttu-id="981ab-200">0x00000014</span><span class="sxs-lookup"><span data-stu-id="981ab-200">0x00000014</span></span>                      |
| <span data-ttu-id="981ab-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981ab-201">Classes used in</span></span>        | [<span data-ttu-id="981ab-202">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="981ab-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="981ab-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="981ab-203">Windows Server 2008</span></span>



| <span data-ttu-id="981ab-204">進入</span><span class="sxs-lookup"><span data-stu-id="981ab-204">Entry</span></span> | <span data-ttu-id="981ab-205">值</span><span class="sxs-lookup"><span data-stu-id="981ab-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="981ab-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981ab-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981ab-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="981ab-208">System-Only</span></span>            | <span data-ttu-id="981ab-209">否</span><span class="sxs-lookup"><span data-stu-id="981ab-209">False</span></span>                           |
| <span data-ttu-id="981ab-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981ab-210">Is-Single-Valued</span></span>       | <span data-ttu-id="981ab-211">否</span><span class="sxs-lookup"><span data-stu-id="981ab-211">False</span></span>                           |
| <span data-ttu-id="981ab-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981ab-212">Is Indexed</span></span>             | <span data-ttu-id="981ab-213">否</span><span class="sxs-lookup"><span data-stu-id="981ab-213">False</span></span>                           |
| <span data-ttu-id="981ab-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981ab-214">In Global Catalog</span></span>      | <span data-ttu-id="981ab-215">否</span><span class="sxs-lookup"><span data-stu-id="981ab-215">False</span></span>                           |
| <span data-ttu-id="981ab-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981ab-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="981ab-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981ab-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="981ab-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981ab-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="981ab-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981ab-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="981ab-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-220">Search-Flags</span></span>           | <span data-ttu-id="981ab-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981ab-221">0x00000000</span></span>                      |
| <span data-ttu-id="981ab-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-222">System-Flags</span></span>           | <span data-ttu-id="981ab-223">0x00000014</span><span class="sxs-lookup"><span data-stu-id="981ab-223">0x00000014</span></span>                      |
| <span data-ttu-id="981ab-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981ab-224">Classes used in</span></span>        | [<span data-ttu-id="981ab-225">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="981ab-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="981ab-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="981ab-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="981ab-227">進入</span><span class="sxs-lookup"><span data-stu-id="981ab-227">Entry</span></span> | <span data-ttu-id="981ab-228">值</span><span class="sxs-lookup"><span data-stu-id="981ab-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="981ab-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981ab-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981ab-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="981ab-231">System-Only</span></span>            | <span data-ttu-id="981ab-232">否</span><span class="sxs-lookup"><span data-stu-id="981ab-232">False</span></span>                           |
| <span data-ttu-id="981ab-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981ab-233">Is-Single-Valued</span></span>       | <span data-ttu-id="981ab-234">否</span><span class="sxs-lookup"><span data-stu-id="981ab-234">False</span></span>                           |
| <span data-ttu-id="981ab-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981ab-235">Is Indexed</span></span>             | <span data-ttu-id="981ab-236">否</span><span class="sxs-lookup"><span data-stu-id="981ab-236">False</span></span>                           |
| <span data-ttu-id="981ab-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981ab-237">In Global Catalog</span></span>      | <span data-ttu-id="981ab-238">否</span><span class="sxs-lookup"><span data-stu-id="981ab-238">False</span></span>                           |
| <span data-ttu-id="981ab-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981ab-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="981ab-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981ab-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="981ab-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981ab-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="981ab-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981ab-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="981ab-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-243">Search-Flags</span></span>           | <span data-ttu-id="981ab-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981ab-244">0x00000000</span></span>                      |
| <span data-ttu-id="981ab-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-245">System-Flags</span></span>           | <span data-ttu-id="981ab-246">0x00000014</span><span class="sxs-lookup"><span data-stu-id="981ab-246">0x00000014</span></span>                      |
| <span data-ttu-id="981ab-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981ab-247">Classes used in</span></span>        | [<span data-ttu-id="981ab-248">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="981ab-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="981ab-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="981ab-249">Windows Server 2012</span></span>



| <span data-ttu-id="981ab-250">進入</span><span class="sxs-lookup"><span data-stu-id="981ab-250">Entry</span></span> | <span data-ttu-id="981ab-251">值</span><span class="sxs-lookup"><span data-stu-id="981ab-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="981ab-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981ab-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981ab-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="981ab-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="981ab-254">System-Only</span></span>            | <span data-ttu-id="981ab-255">否</span><span class="sxs-lookup"><span data-stu-id="981ab-255">False</span></span>                           |
| <span data-ttu-id="981ab-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981ab-256">Is-Single-Valued</span></span>       | <span data-ttu-id="981ab-257">否</span><span class="sxs-lookup"><span data-stu-id="981ab-257">False</span></span>                           |
| <span data-ttu-id="981ab-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981ab-258">Is Indexed</span></span>             | <span data-ttu-id="981ab-259">否</span><span class="sxs-lookup"><span data-stu-id="981ab-259">False</span></span>                           |
| <span data-ttu-id="981ab-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981ab-260">In Global Catalog</span></span>      | <span data-ttu-id="981ab-261">否</span><span class="sxs-lookup"><span data-stu-id="981ab-261">False</span></span>                           |
| <span data-ttu-id="981ab-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981ab-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="981ab-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981ab-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="981ab-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981ab-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="981ab-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981ab-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="981ab-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-266">Search-Flags</span></span>           | <span data-ttu-id="981ab-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981ab-267">0x00000000</span></span>                      |
| <span data-ttu-id="981ab-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981ab-268">System-Flags</span></span>           | <span data-ttu-id="981ab-269">0x00000014</span><span class="sxs-lookup"><span data-stu-id="981ab-269">0x00000014</span></span>                      |
| <span data-ttu-id="981ab-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981ab-270">Classes used in</span></span>        | [<span data-ttu-id="981ab-271">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="981ab-271">**Top**</span></span>](c-top.md)<br/> |



 

 





