---
title: ms DS-NC-複寫-輸入-相鄰屬性
description: 此分割區的複寫協力電腦。 此伺服器會從其他可作為來源的伺服器取得複寫資料。
ms.assetid: 0a1ed4f6-38ae-4823-a26d-5c0d56e59280
ms.tgt_platform: multiple
keywords:
- ms DS-NC-複寫-輸入-相鄰屬性 AD 架構
- NCReplInboundNeighbors 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Inbound-Neighbors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173c42720d76730bff974b5571e75732d0802066
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687239"
---
# <a name="ms-ds-nc-repl-inbound-neighbors-attribute"></a><span data-ttu-id="f6083-106">ms DS-NC-複寫-輸入-相鄰屬性</span><span class="sxs-lookup"><span data-stu-id="f6083-106">ms-DS-NC-Repl-Inbound-Neighbors attribute</span></span>

<span data-ttu-id="f6083-107">此分割區的複寫協力電腦。</span><span class="sxs-lookup"><span data-stu-id="f6083-107">Replication partners for this partition.</span></span> <span data-ttu-id="f6083-108">此伺服器會從其他可作為來源的伺服器取得複寫資料。</span><span class="sxs-lookup"><span data-stu-id="f6083-108">This server obtains replication data from these other servers, which act as sources.</span></span>



| <span data-ttu-id="f6083-109">進入</span><span class="sxs-lookup"><span data-stu-id="f6083-109">Entry</span></span> | <span data-ttu-id="f6083-110">值</span><span class="sxs-lookup"><span data-stu-id="f6083-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f6083-111">CN</span><span class="sxs-lookup"><span data-stu-id="f6083-111">CN</span></span>                | <span data-ttu-id="f6083-112">ms-DS-NC-複寫-輸入-相鄰</span><span class="sxs-lookup"><span data-stu-id="f6083-112">ms-DS-NC-Repl-Inbound-Neighbors</span></span>             |
| <span data-ttu-id="f6083-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f6083-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f6083-114">NCReplInboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="f6083-114">msDS-NCReplInboundNeighbors</span></span>                 |
| <span data-ttu-id="f6083-115">大小</span><span class="sxs-lookup"><span data-stu-id="f6083-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="f6083-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f6083-116">Update Privilege</span></span>  | <span data-ttu-id="f6083-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="f6083-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="f6083-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f6083-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f6083-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f6083-119">Attribute-Id</span></span>      | <span data-ttu-id="f6083-120">1.2.840.113556.1.4.1705</span><span class="sxs-lookup"><span data-stu-id="f6083-120">1.2.840.113556.1.4.1705</span></span>                     |
| <span data-ttu-id="f6083-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f6083-121">System-Id-Guid</span></span>    | <span data-ttu-id="f6083-122">9edba85a-3e9e-431b-9b1a-a5b6e9eda796</span><span class="sxs-lookup"><span data-stu-id="f6083-122">9edba85a-3e9e-431b-9b1a-a5b6e9eda796</span></span>        |
| <span data-ttu-id="f6083-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6083-123">Syntax</span></span>            | [<span data-ttu-id="f6083-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f6083-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f6083-125">實作</span><span class="sxs-lookup"><span data-stu-id="f6083-125">Implementations</span></span>

-   [<span data-ttu-id="f6083-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f6083-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f6083-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f6083-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f6083-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f6083-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f6083-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f6083-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f6083-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f6083-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f6083-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f6083-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f6083-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f6083-132">Windows Server 2003</span></span>



| <span data-ttu-id="f6083-133">進入</span><span class="sxs-lookup"><span data-stu-id="f6083-133">Entry</span></span> | <span data-ttu-id="f6083-134">值</span><span class="sxs-lookup"><span data-stu-id="f6083-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6083-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f6083-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6083-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6083-137">System-Only</span></span>            | <span data-ttu-id="f6083-138">否</span><span class="sxs-lookup"><span data-stu-id="f6083-138">False</span></span>                           |
| <span data-ttu-id="f6083-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f6083-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f6083-140">否</span><span class="sxs-lookup"><span data-stu-id="f6083-140">False</span></span>                           |
| <span data-ttu-id="f6083-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f6083-141">Is Indexed</span></span>             | <span data-ttu-id="f6083-142">否</span><span class="sxs-lookup"><span data-stu-id="f6083-142">False</span></span>                           |
| <span data-ttu-id="f6083-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f6083-143">In Global Catalog</span></span>      | <span data-ttu-id="f6083-144">否</span><span class="sxs-lookup"><span data-stu-id="f6083-144">False</span></span>                           |
| <span data-ttu-id="f6083-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f6083-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6083-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f6083-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6083-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6083-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6083-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6083-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6083-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-149">Search-Flags</span></span>           | <span data-ttu-id="f6083-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6083-150">0x00000000</span></span>                      |
| <span data-ttu-id="f6083-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-151">System-Flags</span></span>           | <span data-ttu-id="f6083-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f6083-152">0x00000014</span></span>                      |
| <span data-ttu-id="f6083-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f6083-153">Classes used in</span></span>        | [<span data-ttu-id="f6083-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f6083-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f6083-155">亞當</span><span class="sxs-lookup"><span data-stu-id="f6083-155">ADAM</span></span>



| <span data-ttu-id="f6083-156">進入</span><span class="sxs-lookup"><span data-stu-id="f6083-156">Entry</span></span> | <span data-ttu-id="f6083-157">值</span><span class="sxs-lookup"><span data-stu-id="f6083-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6083-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f6083-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6083-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6083-160">System-Only</span></span>            | <span data-ttu-id="f6083-161">否</span><span class="sxs-lookup"><span data-stu-id="f6083-161">False</span></span>                           |
| <span data-ttu-id="f6083-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f6083-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f6083-163">否</span><span class="sxs-lookup"><span data-stu-id="f6083-163">False</span></span>                           |
| <span data-ttu-id="f6083-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f6083-164">Is Indexed</span></span>             | <span data-ttu-id="f6083-165">否</span><span class="sxs-lookup"><span data-stu-id="f6083-165">False</span></span>                           |
| <span data-ttu-id="f6083-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f6083-166">In Global Catalog</span></span>      | <span data-ttu-id="f6083-167">否</span><span class="sxs-lookup"><span data-stu-id="f6083-167">False</span></span>                           |
| <span data-ttu-id="f6083-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f6083-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6083-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f6083-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6083-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6083-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6083-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6083-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6083-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-172">Search-Flags</span></span>           | <span data-ttu-id="f6083-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6083-173">0x00000000</span></span>                      |
| <span data-ttu-id="f6083-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-174">System-Flags</span></span>           | <span data-ttu-id="f6083-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f6083-175">0x00000014</span></span>                      |
| <span data-ttu-id="f6083-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f6083-176">Classes used in</span></span>        | [<span data-ttu-id="f6083-177">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f6083-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f6083-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f6083-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f6083-179">進入</span><span class="sxs-lookup"><span data-stu-id="f6083-179">Entry</span></span> | <span data-ttu-id="f6083-180">值</span><span class="sxs-lookup"><span data-stu-id="f6083-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6083-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f6083-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6083-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6083-183">System-Only</span></span>            | <span data-ttu-id="f6083-184">否</span><span class="sxs-lookup"><span data-stu-id="f6083-184">False</span></span>                           |
| <span data-ttu-id="f6083-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f6083-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f6083-186">否</span><span class="sxs-lookup"><span data-stu-id="f6083-186">False</span></span>                           |
| <span data-ttu-id="f6083-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f6083-187">Is Indexed</span></span>             | <span data-ttu-id="f6083-188">否</span><span class="sxs-lookup"><span data-stu-id="f6083-188">False</span></span>                           |
| <span data-ttu-id="f6083-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f6083-189">In Global Catalog</span></span>      | <span data-ttu-id="f6083-190">否</span><span class="sxs-lookup"><span data-stu-id="f6083-190">False</span></span>                           |
| <span data-ttu-id="f6083-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f6083-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6083-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f6083-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6083-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6083-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6083-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6083-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6083-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-195">Search-Flags</span></span>           | <span data-ttu-id="f6083-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6083-196">0x00000000</span></span>                      |
| <span data-ttu-id="f6083-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-197">System-Flags</span></span>           | <span data-ttu-id="f6083-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f6083-198">0x00000014</span></span>                      |
| <span data-ttu-id="f6083-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f6083-199">Classes used in</span></span>        | [<span data-ttu-id="f6083-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f6083-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f6083-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6083-201">Windows Server 2008</span></span>



| <span data-ttu-id="f6083-202">進入</span><span class="sxs-lookup"><span data-stu-id="f6083-202">Entry</span></span> | <span data-ttu-id="f6083-203">值</span><span class="sxs-lookup"><span data-stu-id="f6083-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6083-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f6083-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6083-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6083-206">System-Only</span></span>            | <span data-ttu-id="f6083-207">否</span><span class="sxs-lookup"><span data-stu-id="f6083-207">False</span></span>                           |
| <span data-ttu-id="f6083-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f6083-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f6083-209">否</span><span class="sxs-lookup"><span data-stu-id="f6083-209">False</span></span>                           |
| <span data-ttu-id="f6083-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f6083-210">Is Indexed</span></span>             | <span data-ttu-id="f6083-211">否</span><span class="sxs-lookup"><span data-stu-id="f6083-211">False</span></span>                           |
| <span data-ttu-id="f6083-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f6083-212">In Global Catalog</span></span>      | <span data-ttu-id="f6083-213">否</span><span class="sxs-lookup"><span data-stu-id="f6083-213">False</span></span>                           |
| <span data-ttu-id="f6083-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f6083-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6083-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f6083-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6083-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6083-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6083-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6083-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6083-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-218">Search-Flags</span></span>           | <span data-ttu-id="f6083-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6083-219">0x00000000</span></span>                      |
| <span data-ttu-id="f6083-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-220">System-Flags</span></span>           | <span data-ttu-id="f6083-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f6083-221">0x00000014</span></span>                      |
| <span data-ttu-id="f6083-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f6083-222">Classes used in</span></span>        | [<span data-ttu-id="f6083-223">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f6083-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f6083-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f6083-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f6083-225">進入</span><span class="sxs-lookup"><span data-stu-id="f6083-225">Entry</span></span> | <span data-ttu-id="f6083-226">值</span><span class="sxs-lookup"><span data-stu-id="f6083-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6083-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f6083-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6083-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6083-229">System-Only</span></span>            | <span data-ttu-id="f6083-230">否</span><span class="sxs-lookup"><span data-stu-id="f6083-230">False</span></span>                           |
| <span data-ttu-id="f6083-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f6083-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f6083-232">否</span><span class="sxs-lookup"><span data-stu-id="f6083-232">False</span></span>                           |
| <span data-ttu-id="f6083-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f6083-233">Is Indexed</span></span>             | <span data-ttu-id="f6083-234">否</span><span class="sxs-lookup"><span data-stu-id="f6083-234">False</span></span>                           |
| <span data-ttu-id="f6083-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f6083-235">In Global Catalog</span></span>      | <span data-ttu-id="f6083-236">否</span><span class="sxs-lookup"><span data-stu-id="f6083-236">False</span></span>                           |
| <span data-ttu-id="f6083-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f6083-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6083-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f6083-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6083-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6083-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6083-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6083-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6083-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-241">Search-Flags</span></span>           | <span data-ttu-id="f6083-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6083-242">0x00000000</span></span>                      |
| <span data-ttu-id="f6083-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-243">System-Flags</span></span>           | <span data-ttu-id="f6083-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f6083-244">0x00000014</span></span>                      |
| <span data-ttu-id="f6083-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f6083-245">Classes used in</span></span>        | [<span data-ttu-id="f6083-246">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f6083-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f6083-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6083-247">Windows Server 2012</span></span>



| <span data-ttu-id="f6083-248">進入</span><span class="sxs-lookup"><span data-stu-id="f6083-248">Entry</span></span> | <span data-ttu-id="f6083-249">值</span><span class="sxs-lookup"><span data-stu-id="f6083-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f6083-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f6083-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f6083-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f6083-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f6083-252">System-Only</span></span>            | <span data-ttu-id="f6083-253">否</span><span class="sxs-lookup"><span data-stu-id="f6083-253">False</span></span>                           |
| <span data-ttu-id="f6083-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f6083-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f6083-255">否</span><span class="sxs-lookup"><span data-stu-id="f6083-255">False</span></span>                           |
| <span data-ttu-id="f6083-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f6083-256">Is Indexed</span></span>             | <span data-ttu-id="f6083-257">否</span><span class="sxs-lookup"><span data-stu-id="f6083-257">False</span></span>                           |
| <span data-ttu-id="f6083-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f6083-258">In Global Catalog</span></span>      | <span data-ttu-id="f6083-259">否</span><span class="sxs-lookup"><span data-stu-id="f6083-259">False</span></span>                           |
| <span data-ttu-id="f6083-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f6083-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f6083-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f6083-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f6083-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f6083-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f6083-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f6083-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f6083-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-264">Search-Flags</span></span>           | <span data-ttu-id="f6083-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f6083-265">0x00000000</span></span>                      |
| <span data-ttu-id="f6083-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f6083-266">System-Flags</span></span>           | <span data-ttu-id="f6083-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f6083-267">0x00000014</span></span>                      |
| <span data-ttu-id="f6083-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f6083-268">Classes used in</span></span>        | [<span data-ttu-id="f6083-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f6083-269">**Top**</span></span>](c-top.md)<br/> |



 

 





