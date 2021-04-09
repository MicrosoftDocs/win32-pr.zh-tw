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
# <a name="ms-ds-nc-repl-outbound-neighbors-attribute"></a><span data-ttu-id="df2aa-107">ms DS-NC-複寫-輸出-相鄰屬性</span><span class="sxs-lookup"><span data-stu-id="df2aa-107">ms-DS-NC-Repl-Outbound-Neighbors attribute</span></span>

<span data-ttu-id="df2aa-108">此分割區的複寫協力電腦。</span><span class="sxs-lookup"><span data-stu-id="df2aa-108">Replication partners for this partition.</span></span> <span data-ttu-id="df2aa-109">此伺服器會將複寫資料傳送到其他可作為目的地的伺服器。</span><span class="sxs-lookup"><span data-stu-id="df2aa-109">This server sends replication data to these other servers, which act as destinations.</span></span> <span data-ttu-id="df2aa-110">當有新的資料可用時，此伺服器會通知這些其他伺服器。</span><span class="sxs-lookup"><span data-stu-id="df2aa-110">This server will notify these other servers when new data is available.</span></span>



| <span data-ttu-id="df2aa-111">進入</span><span class="sxs-lookup"><span data-stu-id="df2aa-111">Entry</span></span> | <span data-ttu-id="df2aa-112">值</span><span class="sxs-lookup"><span data-stu-id="df2aa-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="df2aa-113">CN</span><span class="sxs-lookup"><span data-stu-id="df2aa-113">CN</span></span>                | <span data-ttu-id="df2aa-114">ms DS-NC-複寫-輸出-相鄰</span><span class="sxs-lookup"><span data-stu-id="df2aa-114">ms-DS-NC-Repl-Outbound-Neighbors</span></span>            |
| <span data-ttu-id="df2aa-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="df2aa-115">Ldap-Display-Name</span></span> | <span data-ttu-id="df2aa-116">NCReplOutboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="df2aa-116">msDS-NCReplOutboundNeighbors</span></span>                |
| <span data-ttu-id="df2aa-117">大小</span><span class="sxs-lookup"><span data-stu-id="df2aa-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="df2aa-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="df2aa-118">Update Privilege</span></span>  | <span data-ttu-id="df2aa-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="df2aa-119">This value is set by the system.</span></span>            |
| <span data-ttu-id="df2aa-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="df2aa-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="df2aa-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df2aa-121">Attribute-Id</span></span>      | <span data-ttu-id="df2aa-122">1.2.840.113556.1.4.1706</span><span class="sxs-lookup"><span data-stu-id="df2aa-122">1.2.840.113556.1.4.1706</span></span>                     |
| <span data-ttu-id="df2aa-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="df2aa-123">System-Id-Guid</span></span>    | <span data-ttu-id="df2aa-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span><span class="sxs-lookup"><span data-stu-id="df2aa-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span></span>        |
| <span data-ttu-id="df2aa-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="df2aa-125">Syntax</span></span>            | [<span data-ttu-id="df2aa-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="df2aa-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="df2aa-127">實作</span><span class="sxs-lookup"><span data-stu-id="df2aa-127">Implementations</span></span>

-   [<span data-ttu-id="df2aa-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df2aa-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df2aa-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="df2aa-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="df2aa-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df2aa-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df2aa-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df2aa-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df2aa-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df2aa-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df2aa-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df2aa-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="df2aa-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df2aa-134">Windows Server 2003</span></span>



| <span data-ttu-id="df2aa-135">進入</span><span class="sxs-lookup"><span data-stu-id="df2aa-135">Entry</span></span> | <span data-ttu-id="df2aa-136">值</span><span class="sxs-lookup"><span data-stu-id="df2aa-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df2aa-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df2aa-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df2aa-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="df2aa-139">System-Only</span></span>            | <span data-ttu-id="df2aa-140">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-140">False</span></span>                           |
| <span data-ttu-id="df2aa-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df2aa-141">Is-Single-Valued</span></span>       | <span data-ttu-id="df2aa-142">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-142">False</span></span>                           |
| <span data-ttu-id="df2aa-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df2aa-143">Is Indexed</span></span>             | <span data-ttu-id="df2aa-144">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-144">False</span></span>                           |
| <span data-ttu-id="df2aa-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df2aa-145">In Global Catalog</span></span>      | <span data-ttu-id="df2aa-146">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-146">False</span></span>                           |
| <span data-ttu-id="df2aa-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df2aa-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="df2aa-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df2aa-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df2aa-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df2aa-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df2aa-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df2aa-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df2aa-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-151">Search-Flags</span></span>           | <span data-ttu-id="df2aa-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df2aa-152">0x00000000</span></span>                      |
| <span data-ttu-id="df2aa-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-153">System-Flags</span></span>           | <span data-ttu-id="df2aa-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df2aa-154">0x00000014</span></span>                      |
| <span data-ttu-id="df2aa-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df2aa-155">Classes used in</span></span>        | [<span data-ttu-id="df2aa-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df2aa-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="df2aa-157">亞當</span><span class="sxs-lookup"><span data-stu-id="df2aa-157">ADAM</span></span>



| <span data-ttu-id="df2aa-158">進入</span><span class="sxs-lookup"><span data-stu-id="df2aa-158">Entry</span></span> | <span data-ttu-id="df2aa-159">值</span><span class="sxs-lookup"><span data-stu-id="df2aa-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df2aa-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df2aa-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df2aa-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="df2aa-162">System-Only</span></span>            | <span data-ttu-id="df2aa-163">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-163">False</span></span>                           |
| <span data-ttu-id="df2aa-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df2aa-164">Is-Single-Valued</span></span>       | <span data-ttu-id="df2aa-165">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-165">False</span></span>                           |
| <span data-ttu-id="df2aa-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df2aa-166">Is Indexed</span></span>             | <span data-ttu-id="df2aa-167">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-167">False</span></span>                           |
| <span data-ttu-id="df2aa-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df2aa-168">In Global Catalog</span></span>      | <span data-ttu-id="df2aa-169">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-169">False</span></span>                           |
| <span data-ttu-id="df2aa-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df2aa-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="df2aa-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df2aa-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df2aa-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df2aa-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df2aa-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df2aa-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df2aa-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-174">Search-Flags</span></span>           | <span data-ttu-id="df2aa-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df2aa-175">0x00000000</span></span>                      |
| <span data-ttu-id="df2aa-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-176">System-Flags</span></span>           | <span data-ttu-id="df2aa-177">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df2aa-177">0x00000014</span></span>                      |
| <span data-ttu-id="df2aa-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df2aa-178">Classes used in</span></span>        | [<span data-ttu-id="df2aa-179">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df2aa-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df2aa-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df2aa-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df2aa-181">進入</span><span class="sxs-lookup"><span data-stu-id="df2aa-181">Entry</span></span> | <span data-ttu-id="df2aa-182">值</span><span class="sxs-lookup"><span data-stu-id="df2aa-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df2aa-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df2aa-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df2aa-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="df2aa-185">System-Only</span></span>            | <span data-ttu-id="df2aa-186">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-186">False</span></span>                           |
| <span data-ttu-id="df2aa-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df2aa-187">Is-Single-Valued</span></span>       | <span data-ttu-id="df2aa-188">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-188">False</span></span>                           |
| <span data-ttu-id="df2aa-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df2aa-189">Is Indexed</span></span>             | <span data-ttu-id="df2aa-190">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-190">False</span></span>                           |
| <span data-ttu-id="df2aa-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df2aa-191">In Global Catalog</span></span>      | <span data-ttu-id="df2aa-192">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-192">False</span></span>                           |
| <span data-ttu-id="df2aa-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df2aa-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="df2aa-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df2aa-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df2aa-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df2aa-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df2aa-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df2aa-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df2aa-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-197">Search-Flags</span></span>           | <span data-ttu-id="df2aa-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df2aa-198">0x00000000</span></span>                      |
| <span data-ttu-id="df2aa-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-199">System-Flags</span></span>           | <span data-ttu-id="df2aa-200">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df2aa-200">0x00000014</span></span>                      |
| <span data-ttu-id="df2aa-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df2aa-201">Classes used in</span></span>        | [<span data-ttu-id="df2aa-202">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df2aa-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df2aa-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df2aa-203">Windows Server 2008</span></span>



| <span data-ttu-id="df2aa-204">進入</span><span class="sxs-lookup"><span data-stu-id="df2aa-204">Entry</span></span> | <span data-ttu-id="df2aa-205">值</span><span class="sxs-lookup"><span data-stu-id="df2aa-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df2aa-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df2aa-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df2aa-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="df2aa-208">System-Only</span></span>            | <span data-ttu-id="df2aa-209">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-209">False</span></span>                           |
| <span data-ttu-id="df2aa-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df2aa-210">Is-Single-Valued</span></span>       | <span data-ttu-id="df2aa-211">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-211">False</span></span>                           |
| <span data-ttu-id="df2aa-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df2aa-212">Is Indexed</span></span>             | <span data-ttu-id="df2aa-213">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-213">False</span></span>                           |
| <span data-ttu-id="df2aa-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df2aa-214">In Global Catalog</span></span>      | <span data-ttu-id="df2aa-215">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-215">False</span></span>                           |
| <span data-ttu-id="df2aa-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df2aa-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="df2aa-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df2aa-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df2aa-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df2aa-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df2aa-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df2aa-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df2aa-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-220">Search-Flags</span></span>           | <span data-ttu-id="df2aa-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df2aa-221">0x00000000</span></span>                      |
| <span data-ttu-id="df2aa-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-222">System-Flags</span></span>           | <span data-ttu-id="df2aa-223">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df2aa-223">0x00000014</span></span>                      |
| <span data-ttu-id="df2aa-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df2aa-224">Classes used in</span></span>        | [<span data-ttu-id="df2aa-225">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df2aa-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df2aa-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df2aa-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df2aa-227">進入</span><span class="sxs-lookup"><span data-stu-id="df2aa-227">Entry</span></span> | <span data-ttu-id="df2aa-228">值</span><span class="sxs-lookup"><span data-stu-id="df2aa-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df2aa-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df2aa-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df2aa-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="df2aa-231">System-Only</span></span>            | <span data-ttu-id="df2aa-232">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-232">False</span></span>                           |
| <span data-ttu-id="df2aa-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df2aa-233">Is-Single-Valued</span></span>       | <span data-ttu-id="df2aa-234">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-234">False</span></span>                           |
| <span data-ttu-id="df2aa-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df2aa-235">Is Indexed</span></span>             | <span data-ttu-id="df2aa-236">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-236">False</span></span>                           |
| <span data-ttu-id="df2aa-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df2aa-237">In Global Catalog</span></span>      | <span data-ttu-id="df2aa-238">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-238">False</span></span>                           |
| <span data-ttu-id="df2aa-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df2aa-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="df2aa-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df2aa-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df2aa-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df2aa-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df2aa-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df2aa-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df2aa-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-243">Search-Flags</span></span>           | <span data-ttu-id="df2aa-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df2aa-244">0x00000000</span></span>                      |
| <span data-ttu-id="df2aa-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-245">System-Flags</span></span>           | <span data-ttu-id="df2aa-246">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df2aa-246">0x00000014</span></span>                      |
| <span data-ttu-id="df2aa-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df2aa-247">Classes used in</span></span>        | [<span data-ttu-id="df2aa-248">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df2aa-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df2aa-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df2aa-249">Windows Server 2012</span></span>



| <span data-ttu-id="df2aa-250">進入</span><span class="sxs-lookup"><span data-stu-id="df2aa-250">Entry</span></span> | <span data-ttu-id="df2aa-251">值</span><span class="sxs-lookup"><span data-stu-id="df2aa-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df2aa-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df2aa-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df2aa-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="df2aa-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="df2aa-254">System-Only</span></span>            | <span data-ttu-id="df2aa-255">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-255">False</span></span>                           |
| <span data-ttu-id="df2aa-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df2aa-256">Is-Single-Valued</span></span>       | <span data-ttu-id="df2aa-257">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-257">False</span></span>                           |
| <span data-ttu-id="df2aa-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df2aa-258">Is Indexed</span></span>             | <span data-ttu-id="df2aa-259">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-259">False</span></span>                           |
| <span data-ttu-id="df2aa-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df2aa-260">In Global Catalog</span></span>      | <span data-ttu-id="df2aa-261">否</span><span class="sxs-lookup"><span data-stu-id="df2aa-261">False</span></span>                           |
| <span data-ttu-id="df2aa-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df2aa-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="df2aa-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df2aa-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df2aa-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df2aa-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df2aa-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df2aa-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df2aa-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-266">Search-Flags</span></span>           | <span data-ttu-id="df2aa-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df2aa-267">0x00000000</span></span>                      |
| <span data-ttu-id="df2aa-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df2aa-268">System-Flags</span></span>           | <span data-ttu-id="df2aa-269">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df2aa-269">0x00000014</span></span>                      |
| <span data-ttu-id="df2aa-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df2aa-270">Classes used in</span></span>        | [<span data-ttu-id="df2aa-271">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df2aa-271">**Top**</span></span>](c-top.md)<br/> |



 

 





