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
# <a name="ms-ds-nc-repl-inbound-neighbors-attribute"></a><span data-ttu-id="47fcb-106">ms DS-NC-複寫-輸入-相鄰屬性</span><span class="sxs-lookup"><span data-stu-id="47fcb-106">ms-DS-NC-Repl-Inbound-Neighbors attribute</span></span>

<span data-ttu-id="47fcb-107">此分割區的複寫協力電腦。</span><span class="sxs-lookup"><span data-stu-id="47fcb-107">Replication partners for this partition.</span></span> <span data-ttu-id="47fcb-108">此伺服器會從其他可作為來源的伺服器取得複寫資料。</span><span class="sxs-lookup"><span data-stu-id="47fcb-108">This server obtains replication data from these other servers, which act as sources.</span></span>



| <span data-ttu-id="47fcb-109">進入</span><span class="sxs-lookup"><span data-stu-id="47fcb-109">Entry</span></span> | <span data-ttu-id="47fcb-110">值</span><span class="sxs-lookup"><span data-stu-id="47fcb-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="47fcb-111">CN</span><span class="sxs-lookup"><span data-stu-id="47fcb-111">CN</span></span>                | <span data-ttu-id="47fcb-112">ms-DS-NC-複寫-輸入-相鄰</span><span class="sxs-lookup"><span data-stu-id="47fcb-112">ms-DS-NC-Repl-Inbound-Neighbors</span></span>             |
| <span data-ttu-id="47fcb-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="47fcb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="47fcb-114">NCReplInboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="47fcb-114">msDS-NCReplInboundNeighbors</span></span>                 |
| <span data-ttu-id="47fcb-115">大小</span><span class="sxs-lookup"><span data-stu-id="47fcb-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="47fcb-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="47fcb-116">Update Privilege</span></span>  | <span data-ttu-id="47fcb-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="47fcb-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="47fcb-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="47fcb-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="47fcb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="47fcb-119">Attribute-Id</span></span>      | <span data-ttu-id="47fcb-120">1.2.840.113556.1.4.1705</span><span class="sxs-lookup"><span data-stu-id="47fcb-120">1.2.840.113556.1.4.1705</span></span>                     |
| <span data-ttu-id="47fcb-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="47fcb-121">System-Id-Guid</span></span>    | <span data-ttu-id="47fcb-122">9edba85a-3e9e-431b-9b1a-a5b6e9eda796</span><span class="sxs-lookup"><span data-stu-id="47fcb-122">9edba85a-3e9e-431b-9b1a-a5b6e9eda796</span></span>        |
| <span data-ttu-id="47fcb-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="47fcb-123">Syntax</span></span>            | [<span data-ttu-id="47fcb-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="47fcb-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="47fcb-125">實作</span><span class="sxs-lookup"><span data-stu-id="47fcb-125">Implementations</span></span>

-   [<span data-ttu-id="47fcb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="47fcb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="47fcb-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="47fcb-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="47fcb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="47fcb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="47fcb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="47fcb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="47fcb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="47fcb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="47fcb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="47fcb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="47fcb-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47fcb-132">Windows Server 2003</span></span>



| <span data-ttu-id="47fcb-133">進入</span><span class="sxs-lookup"><span data-stu-id="47fcb-133">Entry</span></span> | <span data-ttu-id="47fcb-134">值</span><span class="sxs-lookup"><span data-stu-id="47fcb-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47fcb-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="47fcb-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47fcb-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="47fcb-137">System-Only</span></span>            | <span data-ttu-id="47fcb-138">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-138">False</span></span>                           |
| <span data-ttu-id="47fcb-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="47fcb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="47fcb-140">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-140">False</span></span>                           |
| <span data-ttu-id="47fcb-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="47fcb-141">Is Indexed</span></span>             | <span data-ttu-id="47fcb-142">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-142">False</span></span>                           |
| <span data-ttu-id="47fcb-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="47fcb-143">In Global Catalog</span></span>      | <span data-ttu-id="47fcb-144">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-144">False</span></span>                           |
| <span data-ttu-id="47fcb-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="47fcb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="47fcb-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="47fcb-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47fcb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47fcb-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47fcb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47fcb-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47fcb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-149">Search-Flags</span></span>           | <span data-ttu-id="47fcb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47fcb-150">0x00000000</span></span>                      |
| <span data-ttu-id="47fcb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-151">System-Flags</span></span>           | <span data-ttu-id="47fcb-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="47fcb-152">0x00000014</span></span>                      |
| <span data-ttu-id="47fcb-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="47fcb-153">Classes used in</span></span>        | [<span data-ttu-id="47fcb-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="47fcb-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="47fcb-155">亞當</span><span class="sxs-lookup"><span data-stu-id="47fcb-155">ADAM</span></span>



| <span data-ttu-id="47fcb-156">進入</span><span class="sxs-lookup"><span data-stu-id="47fcb-156">Entry</span></span> | <span data-ttu-id="47fcb-157">值</span><span class="sxs-lookup"><span data-stu-id="47fcb-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47fcb-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="47fcb-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47fcb-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="47fcb-160">System-Only</span></span>            | <span data-ttu-id="47fcb-161">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-161">False</span></span>                           |
| <span data-ttu-id="47fcb-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="47fcb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="47fcb-163">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-163">False</span></span>                           |
| <span data-ttu-id="47fcb-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="47fcb-164">Is Indexed</span></span>             | <span data-ttu-id="47fcb-165">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-165">False</span></span>                           |
| <span data-ttu-id="47fcb-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="47fcb-166">In Global Catalog</span></span>      | <span data-ttu-id="47fcb-167">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-167">False</span></span>                           |
| <span data-ttu-id="47fcb-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="47fcb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="47fcb-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="47fcb-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47fcb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47fcb-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47fcb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47fcb-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47fcb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-172">Search-Flags</span></span>           | <span data-ttu-id="47fcb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47fcb-173">0x00000000</span></span>                      |
| <span data-ttu-id="47fcb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-174">System-Flags</span></span>           | <span data-ttu-id="47fcb-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="47fcb-175">0x00000014</span></span>                      |
| <span data-ttu-id="47fcb-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="47fcb-176">Classes used in</span></span>        | [<span data-ttu-id="47fcb-177">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="47fcb-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="47fcb-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="47fcb-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="47fcb-179">進入</span><span class="sxs-lookup"><span data-stu-id="47fcb-179">Entry</span></span> | <span data-ttu-id="47fcb-180">值</span><span class="sxs-lookup"><span data-stu-id="47fcb-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47fcb-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="47fcb-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47fcb-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="47fcb-183">System-Only</span></span>            | <span data-ttu-id="47fcb-184">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-184">False</span></span>                           |
| <span data-ttu-id="47fcb-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="47fcb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="47fcb-186">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-186">False</span></span>                           |
| <span data-ttu-id="47fcb-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="47fcb-187">Is Indexed</span></span>             | <span data-ttu-id="47fcb-188">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-188">False</span></span>                           |
| <span data-ttu-id="47fcb-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="47fcb-189">In Global Catalog</span></span>      | <span data-ttu-id="47fcb-190">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-190">False</span></span>                           |
| <span data-ttu-id="47fcb-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="47fcb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="47fcb-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="47fcb-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47fcb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47fcb-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47fcb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47fcb-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47fcb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-195">Search-Flags</span></span>           | <span data-ttu-id="47fcb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47fcb-196">0x00000000</span></span>                      |
| <span data-ttu-id="47fcb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-197">System-Flags</span></span>           | <span data-ttu-id="47fcb-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="47fcb-198">0x00000014</span></span>                      |
| <span data-ttu-id="47fcb-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="47fcb-199">Classes used in</span></span>        | [<span data-ttu-id="47fcb-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="47fcb-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="47fcb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47fcb-201">Windows Server 2008</span></span>



| <span data-ttu-id="47fcb-202">進入</span><span class="sxs-lookup"><span data-stu-id="47fcb-202">Entry</span></span> | <span data-ttu-id="47fcb-203">值</span><span class="sxs-lookup"><span data-stu-id="47fcb-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47fcb-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="47fcb-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47fcb-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="47fcb-206">System-Only</span></span>            | <span data-ttu-id="47fcb-207">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-207">False</span></span>                           |
| <span data-ttu-id="47fcb-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="47fcb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="47fcb-209">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-209">False</span></span>                           |
| <span data-ttu-id="47fcb-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="47fcb-210">Is Indexed</span></span>             | <span data-ttu-id="47fcb-211">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-211">False</span></span>                           |
| <span data-ttu-id="47fcb-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="47fcb-212">In Global Catalog</span></span>      | <span data-ttu-id="47fcb-213">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-213">False</span></span>                           |
| <span data-ttu-id="47fcb-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="47fcb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="47fcb-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="47fcb-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47fcb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47fcb-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47fcb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47fcb-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47fcb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-218">Search-Flags</span></span>           | <span data-ttu-id="47fcb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47fcb-219">0x00000000</span></span>                      |
| <span data-ttu-id="47fcb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-220">System-Flags</span></span>           | <span data-ttu-id="47fcb-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="47fcb-221">0x00000014</span></span>                      |
| <span data-ttu-id="47fcb-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="47fcb-222">Classes used in</span></span>        | [<span data-ttu-id="47fcb-223">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="47fcb-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="47fcb-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47fcb-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="47fcb-225">進入</span><span class="sxs-lookup"><span data-stu-id="47fcb-225">Entry</span></span> | <span data-ttu-id="47fcb-226">值</span><span class="sxs-lookup"><span data-stu-id="47fcb-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47fcb-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="47fcb-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47fcb-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="47fcb-229">System-Only</span></span>            | <span data-ttu-id="47fcb-230">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-230">False</span></span>                           |
| <span data-ttu-id="47fcb-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="47fcb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="47fcb-232">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-232">False</span></span>                           |
| <span data-ttu-id="47fcb-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="47fcb-233">Is Indexed</span></span>             | <span data-ttu-id="47fcb-234">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-234">False</span></span>                           |
| <span data-ttu-id="47fcb-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="47fcb-235">In Global Catalog</span></span>      | <span data-ttu-id="47fcb-236">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-236">False</span></span>                           |
| <span data-ttu-id="47fcb-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="47fcb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="47fcb-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="47fcb-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47fcb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47fcb-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47fcb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47fcb-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47fcb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-241">Search-Flags</span></span>           | <span data-ttu-id="47fcb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47fcb-242">0x00000000</span></span>                      |
| <span data-ttu-id="47fcb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-243">System-Flags</span></span>           | <span data-ttu-id="47fcb-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="47fcb-244">0x00000014</span></span>                      |
| <span data-ttu-id="47fcb-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="47fcb-245">Classes used in</span></span>        | [<span data-ttu-id="47fcb-246">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="47fcb-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="47fcb-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47fcb-247">Windows Server 2012</span></span>



| <span data-ttu-id="47fcb-248">進入</span><span class="sxs-lookup"><span data-stu-id="47fcb-248">Entry</span></span> | <span data-ttu-id="47fcb-249">值</span><span class="sxs-lookup"><span data-stu-id="47fcb-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="47fcb-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="47fcb-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47fcb-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="47fcb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="47fcb-252">System-Only</span></span>            | <span data-ttu-id="47fcb-253">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-253">False</span></span>                           |
| <span data-ttu-id="47fcb-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="47fcb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="47fcb-255">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-255">False</span></span>                           |
| <span data-ttu-id="47fcb-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="47fcb-256">Is Indexed</span></span>             | <span data-ttu-id="47fcb-257">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-257">False</span></span>                           |
| <span data-ttu-id="47fcb-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="47fcb-258">In Global Catalog</span></span>      | <span data-ttu-id="47fcb-259">否</span><span class="sxs-lookup"><span data-stu-id="47fcb-259">False</span></span>                           |
| <span data-ttu-id="47fcb-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="47fcb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="47fcb-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="47fcb-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="47fcb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47fcb-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="47fcb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47fcb-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="47fcb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-264">Search-Flags</span></span>           | <span data-ttu-id="47fcb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="47fcb-265">0x00000000</span></span>                      |
| <span data-ttu-id="47fcb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47fcb-266">System-Flags</span></span>           | <span data-ttu-id="47fcb-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="47fcb-267">0x00000014</span></span>                      |
| <span data-ttu-id="47fcb-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="47fcb-268">Classes used in</span></span>        | [<span data-ttu-id="47fcb-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="47fcb-269">**Top**</span></span>](c-top.md)<br/> |



 

 





