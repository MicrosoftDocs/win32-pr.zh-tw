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
# <a name="ms-ds-nc-repl-inbound-neighbors-attribute"></a><span data-ttu-id="dbf6b-106">ms DS-NC-複寫-輸入-相鄰屬性</span><span class="sxs-lookup"><span data-stu-id="dbf6b-106">ms-DS-NC-Repl-Inbound-Neighbors attribute</span></span>

<span data-ttu-id="dbf6b-107">此分割區的複寫協力電腦。</span><span class="sxs-lookup"><span data-stu-id="dbf6b-107">Replication partners for this partition.</span></span> <span data-ttu-id="dbf6b-108">此伺服器會從其他可作為來源的伺服器取得複寫資料。</span><span class="sxs-lookup"><span data-stu-id="dbf6b-108">This server obtains replication data from these other servers, which act as sources.</span></span>



| <span data-ttu-id="dbf6b-109">進入</span><span class="sxs-lookup"><span data-stu-id="dbf6b-109">Entry</span></span> | <span data-ttu-id="dbf6b-110">值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dbf6b-111">CN</span><span class="sxs-lookup"><span data-stu-id="dbf6b-111">CN</span></span>                | <span data-ttu-id="dbf6b-112">ms-DS-NC-複寫-輸入-相鄰</span><span class="sxs-lookup"><span data-stu-id="dbf6b-112">ms-DS-NC-Repl-Inbound-Neighbors</span></span>             |
| <span data-ttu-id="dbf6b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dbf6b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dbf6b-114">NCReplInboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="dbf6b-114">msDS-NCReplInboundNeighbors</span></span>                 |
| <span data-ttu-id="dbf6b-115">大小</span><span class="sxs-lookup"><span data-stu-id="dbf6b-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="dbf6b-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dbf6b-116">Update Privilege</span></span>  | <span data-ttu-id="dbf6b-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="dbf6b-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="dbf6b-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dbf6b-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="dbf6b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dbf6b-119">Attribute-Id</span></span>      | <span data-ttu-id="dbf6b-120">1.2.840.113556.1.4.1705</span><span class="sxs-lookup"><span data-stu-id="dbf6b-120">1.2.840.113556.1.4.1705</span></span>                     |
| <span data-ttu-id="dbf6b-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dbf6b-121">System-Id-Guid</span></span>    | <span data-ttu-id="dbf6b-122">9edba85a-3e9e-431b-9b1a-a5b6e9eda796</span><span class="sxs-lookup"><span data-stu-id="dbf6b-122">9edba85a-3e9e-431b-9b1a-a5b6e9eda796</span></span>        |
| <span data-ttu-id="dbf6b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf6b-123">Syntax</span></span>            | [<span data-ttu-id="dbf6b-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dbf6b-125">實作</span><span class="sxs-lookup"><span data-stu-id="dbf6b-125">Implementations</span></span>

-   [<span data-ttu-id="dbf6b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dbf6b-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dbf6b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dbf6b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dbf6b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dbf6b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="dbf6b-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dbf6b-132">Windows Server 2003</span></span>



| <span data-ttu-id="dbf6b-133">進入</span><span class="sxs-lookup"><span data-stu-id="dbf6b-133">Entry</span></span> | <span data-ttu-id="dbf6b-134">值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dbf6b-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dbf6b-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbf6b-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbf6b-137">System-Only</span></span>            | <span data-ttu-id="dbf6b-138">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-138">False</span></span>                           |
| <span data-ttu-id="dbf6b-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="dbf6b-140">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-140">False</span></span>                           |
| <span data-ttu-id="dbf6b-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dbf6b-141">Is Indexed</span></span>             | <span data-ttu-id="dbf6b-142">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-142">False</span></span>                           |
| <span data-ttu-id="dbf6b-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dbf6b-143">In Global Catalog</span></span>      | <span data-ttu-id="dbf6b-144">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-144">False</span></span>                           |
| <span data-ttu-id="dbf6b-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dbf6b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbf6b-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dbf6b-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dbf6b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbf6b-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbf6b-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-149">Search-Flags</span></span>           | <span data-ttu-id="dbf6b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbf6b-150">0x00000000</span></span>                      |
| <span data-ttu-id="dbf6b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-151">System-Flags</span></span>           | <span data-ttu-id="dbf6b-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="dbf6b-152">0x00000014</span></span>                      |
| <span data-ttu-id="dbf6b-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dbf6b-153">Classes used in</span></span>        | [<span data-ttu-id="dbf6b-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dbf6b-155">亞當</span><span class="sxs-lookup"><span data-stu-id="dbf6b-155">ADAM</span></span>



| <span data-ttu-id="dbf6b-156">進入</span><span class="sxs-lookup"><span data-stu-id="dbf6b-156">Entry</span></span> | <span data-ttu-id="dbf6b-157">值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dbf6b-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dbf6b-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbf6b-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbf6b-160">System-Only</span></span>            | <span data-ttu-id="dbf6b-161">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-161">False</span></span>                           |
| <span data-ttu-id="dbf6b-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="dbf6b-163">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-163">False</span></span>                           |
| <span data-ttu-id="dbf6b-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dbf6b-164">Is Indexed</span></span>             | <span data-ttu-id="dbf6b-165">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-165">False</span></span>                           |
| <span data-ttu-id="dbf6b-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dbf6b-166">In Global Catalog</span></span>      | <span data-ttu-id="dbf6b-167">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-167">False</span></span>                           |
| <span data-ttu-id="dbf6b-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dbf6b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbf6b-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dbf6b-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dbf6b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbf6b-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbf6b-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-172">Search-Flags</span></span>           | <span data-ttu-id="dbf6b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbf6b-173">0x00000000</span></span>                      |
| <span data-ttu-id="dbf6b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-174">System-Flags</span></span>           | <span data-ttu-id="dbf6b-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="dbf6b-175">0x00000014</span></span>                      |
| <span data-ttu-id="dbf6b-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dbf6b-176">Classes used in</span></span>        | [<span data-ttu-id="dbf6b-177">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dbf6b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dbf6b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dbf6b-179">進入</span><span class="sxs-lookup"><span data-stu-id="dbf6b-179">Entry</span></span> | <span data-ttu-id="dbf6b-180">值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dbf6b-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dbf6b-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbf6b-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbf6b-183">System-Only</span></span>            | <span data-ttu-id="dbf6b-184">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-184">False</span></span>                           |
| <span data-ttu-id="dbf6b-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="dbf6b-186">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-186">False</span></span>                           |
| <span data-ttu-id="dbf6b-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dbf6b-187">Is Indexed</span></span>             | <span data-ttu-id="dbf6b-188">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-188">False</span></span>                           |
| <span data-ttu-id="dbf6b-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dbf6b-189">In Global Catalog</span></span>      | <span data-ttu-id="dbf6b-190">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-190">False</span></span>                           |
| <span data-ttu-id="dbf6b-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dbf6b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbf6b-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dbf6b-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dbf6b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbf6b-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbf6b-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-195">Search-Flags</span></span>           | <span data-ttu-id="dbf6b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbf6b-196">0x00000000</span></span>                      |
| <span data-ttu-id="dbf6b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-197">System-Flags</span></span>           | <span data-ttu-id="dbf6b-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="dbf6b-198">0x00000014</span></span>                      |
| <span data-ttu-id="dbf6b-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dbf6b-199">Classes used in</span></span>        | [<span data-ttu-id="dbf6b-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dbf6b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbf6b-201">Windows Server 2008</span></span>



| <span data-ttu-id="dbf6b-202">進入</span><span class="sxs-lookup"><span data-stu-id="dbf6b-202">Entry</span></span> | <span data-ttu-id="dbf6b-203">值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dbf6b-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dbf6b-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbf6b-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbf6b-206">System-Only</span></span>            | <span data-ttu-id="dbf6b-207">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-207">False</span></span>                           |
| <span data-ttu-id="dbf6b-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="dbf6b-209">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-209">False</span></span>                           |
| <span data-ttu-id="dbf6b-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dbf6b-210">Is Indexed</span></span>             | <span data-ttu-id="dbf6b-211">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-211">False</span></span>                           |
| <span data-ttu-id="dbf6b-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dbf6b-212">In Global Catalog</span></span>      | <span data-ttu-id="dbf6b-213">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-213">False</span></span>                           |
| <span data-ttu-id="dbf6b-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dbf6b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbf6b-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dbf6b-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dbf6b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbf6b-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbf6b-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-218">Search-Flags</span></span>           | <span data-ttu-id="dbf6b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbf6b-219">0x00000000</span></span>                      |
| <span data-ttu-id="dbf6b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-220">System-Flags</span></span>           | <span data-ttu-id="dbf6b-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="dbf6b-221">0x00000014</span></span>                      |
| <span data-ttu-id="dbf6b-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dbf6b-222">Classes used in</span></span>        | [<span data-ttu-id="dbf6b-223">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dbf6b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbf6b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dbf6b-225">進入</span><span class="sxs-lookup"><span data-stu-id="dbf6b-225">Entry</span></span> | <span data-ttu-id="dbf6b-226">值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dbf6b-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dbf6b-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbf6b-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbf6b-229">System-Only</span></span>            | <span data-ttu-id="dbf6b-230">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-230">False</span></span>                           |
| <span data-ttu-id="dbf6b-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="dbf6b-232">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-232">False</span></span>                           |
| <span data-ttu-id="dbf6b-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dbf6b-233">Is Indexed</span></span>             | <span data-ttu-id="dbf6b-234">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-234">False</span></span>                           |
| <span data-ttu-id="dbf6b-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dbf6b-235">In Global Catalog</span></span>      | <span data-ttu-id="dbf6b-236">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-236">False</span></span>                           |
| <span data-ttu-id="dbf6b-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dbf6b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbf6b-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dbf6b-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dbf6b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbf6b-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbf6b-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-241">Search-Flags</span></span>           | <span data-ttu-id="dbf6b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbf6b-242">0x00000000</span></span>                      |
| <span data-ttu-id="dbf6b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-243">System-Flags</span></span>           | <span data-ttu-id="dbf6b-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="dbf6b-244">0x00000014</span></span>                      |
| <span data-ttu-id="dbf6b-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dbf6b-245">Classes used in</span></span>        | [<span data-ttu-id="dbf6b-246">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dbf6b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbf6b-247">Windows Server 2012</span></span>



| <span data-ttu-id="dbf6b-248">進入</span><span class="sxs-lookup"><span data-stu-id="dbf6b-248">Entry</span></span> | <span data-ttu-id="dbf6b-249">值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dbf6b-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dbf6b-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbf6b-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dbf6b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbf6b-252">System-Only</span></span>            | <span data-ttu-id="dbf6b-253">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-253">False</span></span>                           |
| <span data-ttu-id="dbf6b-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dbf6b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="dbf6b-255">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-255">False</span></span>                           |
| <span data-ttu-id="dbf6b-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dbf6b-256">Is Indexed</span></span>             | <span data-ttu-id="dbf6b-257">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-257">False</span></span>                           |
| <span data-ttu-id="dbf6b-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dbf6b-258">In Global Catalog</span></span>      | <span data-ttu-id="dbf6b-259">否</span><span class="sxs-lookup"><span data-stu-id="dbf6b-259">False</span></span>                           |
| <span data-ttu-id="dbf6b-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dbf6b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbf6b-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dbf6b-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dbf6b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbf6b-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbf6b-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dbf6b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-264">Search-Flags</span></span>           | <span data-ttu-id="dbf6b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbf6b-265">0x00000000</span></span>                      |
| <span data-ttu-id="dbf6b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbf6b-266">System-Flags</span></span>           | <span data-ttu-id="dbf6b-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="dbf6b-267">0x00000014</span></span>                      |
| <span data-ttu-id="dbf6b-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dbf6b-268">Classes used in</span></span>        | [<span data-ttu-id="dbf6b-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="dbf6b-269">**Top**</span></span>](c-top.md)<br/> |



 

 





