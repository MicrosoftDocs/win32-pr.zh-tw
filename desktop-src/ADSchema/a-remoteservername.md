---
title: 遠端伺服器名稱屬性
description: 在必須儲存一或多個電腦名稱稱的地方使用。
ms.assetid: d09fe925-2137-478d-8630-5220fadedeab
ms.tgt_platform: multiple
keywords:
- 遠端伺服器名稱屬性 AD 架構
- remoteServerName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Remote-Server-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02362c7ef3ba485795a2f27005a8fa2a793f004b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935226"
---
# <a name="remote-server-name-attribute"></a><span data-ttu-id="889ba-105">遠端伺服器名稱屬性</span><span class="sxs-lookup"><span data-stu-id="889ba-105">Remote-Server-Name attribute</span></span>

<span data-ttu-id="889ba-106">在必須儲存一或多個電腦名稱稱的地方使用。</span><span class="sxs-lookup"><span data-stu-id="889ba-106">Used wherever one or more computer names must be stored.</span></span>



| <span data-ttu-id="889ba-107">進入</span><span class="sxs-lookup"><span data-stu-id="889ba-107">Entry</span></span> | <span data-ttu-id="889ba-108">值</span><span class="sxs-lookup"><span data-stu-id="889ba-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="889ba-109">CN</span><span class="sxs-lookup"><span data-stu-id="889ba-109">CN</span></span>                | <span data-ttu-id="889ba-110">遠端伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="889ba-110">Remote-Server-Name</span></span>                          |
| <span data-ttu-id="889ba-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="889ba-111">Ldap-Display-Name</span></span> | <span data-ttu-id="889ba-112">remoteServerName</span><span class="sxs-lookup"><span data-stu-id="889ba-112">remoteServerName</span></span>                            |
| <span data-ttu-id="889ba-113">大小</span><span class="sxs-lookup"><span data-stu-id="889ba-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="889ba-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="889ba-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="889ba-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="889ba-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="889ba-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="889ba-116">Attribute-Id</span></span>      | <span data-ttu-id="889ba-117">1.2.840.113556.1.4.105</span><span class="sxs-lookup"><span data-stu-id="889ba-117">1.2.840.113556.1.4.105</span></span>                      |
| <span data-ttu-id="889ba-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="889ba-118">System-Id-Guid</span></span>    | <span data-ttu-id="889ba-119">bf967a12-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="889ba-119">bf967a12-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="889ba-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="889ba-120">Syntax</span></span>            | [<span data-ttu-id="889ba-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="889ba-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="889ba-122">實作</span><span class="sxs-lookup"><span data-stu-id="889ba-122">Implementations</span></span>

-   [<span data-ttu-id="889ba-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="889ba-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="889ba-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="889ba-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="889ba-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="889ba-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="889ba-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="889ba-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="889ba-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="889ba-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="889ba-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="889ba-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="889ba-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="889ba-129">Windows 2000 Server</span></span>



| <span data-ttu-id="889ba-130">進入</span><span class="sxs-lookup"><span data-stu-id="889ba-130">Entry</span></span> | <span data-ttu-id="889ba-131">值</span><span class="sxs-lookup"><span data-stu-id="889ba-131">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="889ba-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889ba-132">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889ba-133">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="889ba-134">System-Only</span></span>            | <span data-ttu-id="889ba-135">否</span><span class="sxs-lookup"><span data-stu-id="889ba-135">False</span></span>                                |
| <span data-ttu-id="889ba-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889ba-136">Is-Single-Valued</span></span>       | <span data-ttu-id="889ba-137">否</span><span class="sxs-lookup"><span data-stu-id="889ba-137">False</span></span>                                |
| <span data-ttu-id="889ba-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889ba-138">Is Indexed</span></span>             | <span data-ttu-id="889ba-139">否</span><span class="sxs-lookup"><span data-stu-id="889ba-139">False</span></span>                                |
| <span data-ttu-id="889ba-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889ba-140">In Global Catalog</span></span>      | <span data-ttu-id="889ba-141">否</span><span class="sxs-lookup"><span data-stu-id="889ba-141">False</span></span>                                |
| <span data-ttu-id="889ba-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889ba-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="889ba-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889ba-143">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="889ba-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889ba-144">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="889ba-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889ba-145">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="889ba-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-146">Search-Flags</span></span>           | <span data-ttu-id="889ba-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="889ba-147">0x00000000</span></span>                           |
| <span data-ttu-id="889ba-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-148">System-Flags</span></span>           | <span data-ttu-id="889ba-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889ba-149">0x00000010</span></span>                           |
| <span data-ttu-id="889ba-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889ba-150">Classes used in</span></span>        | [<span data-ttu-id="889ba-151">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="889ba-151">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="889ba-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="889ba-152">Windows Server 2003</span></span>



| <span data-ttu-id="889ba-153">進入</span><span class="sxs-lookup"><span data-stu-id="889ba-153">Entry</span></span> | <span data-ttu-id="889ba-154">值</span><span class="sxs-lookup"><span data-stu-id="889ba-154">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="889ba-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889ba-155">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889ba-156">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="889ba-157">System-Only</span></span>            | <span data-ttu-id="889ba-158">否</span><span class="sxs-lookup"><span data-stu-id="889ba-158">False</span></span>                                |
| <span data-ttu-id="889ba-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889ba-159">Is-Single-Valued</span></span>       | <span data-ttu-id="889ba-160">否</span><span class="sxs-lookup"><span data-stu-id="889ba-160">False</span></span>                                |
| <span data-ttu-id="889ba-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889ba-161">Is Indexed</span></span>             | <span data-ttu-id="889ba-162">否</span><span class="sxs-lookup"><span data-stu-id="889ba-162">False</span></span>                                |
| <span data-ttu-id="889ba-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889ba-163">In Global Catalog</span></span>      | <span data-ttu-id="889ba-164">否</span><span class="sxs-lookup"><span data-stu-id="889ba-164">False</span></span>                                |
| <span data-ttu-id="889ba-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889ba-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="889ba-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889ba-166">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="889ba-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889ba-167">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="889ba-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889ba-168">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="889ba-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-169">Search-Flags</span></span>           | <span data-ttu-id="889ba-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="889ba-170">0x00000000</span></span>                           |
| <span data-ttu-id="889ba-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-171">System-Flags</span></span>           | <span data-ttu-id="889ba-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889ba-172">0x00000010</span></span>                           |
| <span data-ttu-id="889ba-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889ba-173">Classes used in</span></span>        | [<span data-ttu-id="889ba-174">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="889ba-174">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="889ba-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="889ba-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="889ba-176">進入</span><span class="sxs-lookup"><span data-stu-id="889ba-176">Entry</span></span> | <span data-ttu-id="889ba-177">值</span><span class="sxs-lookup"><span data-stu-id="889ba-177">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="889ba-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889ba-178">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889ba-179">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="889ba-180">System-Only</span></span>            | <span data-ttu-id="889ba-181">否</span><span class="sxs-lookup"><span data-stu-id="889ba-181">False</span></span>                                |
| <span data-ttu-id="889ba-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889ba-182">Is-Single-Valued</span></span>       | <span data-ttu-id="889ba-183">否</span><span class="sxs-lookup"><span data-stu-id="889ba-183">False</span></span>                                |
| <span data-ttu-id="889ba-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889ba-184">Is Indexed</span></span>             | <span data-ttu-id="889ba-185">否</span><span class="sxs-lookup"><span data-stu-id="889ba-185">False</span></span>                                |
| <span data-ttu-id="889ba-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889ba-186">In Global Catalog</span></span>      | <span data-ttu-id="889ba-187">否</span><span class="sxs-lookup"><span data-stu-id="889ba-187">False</span></span>                                |
| <span data-ttu-id="889ba-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889ba-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="889ba-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889ba-189">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="889ba-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889ba-190">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="889ba-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889ba-191">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="889ba-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-192">Search-Flags</span></span>           | <span data-ttu-id="889ba-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="889ba-193">0x00000000</span></span>                           |
| <span data-ttu-id="889ba-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-194">System-Flags</span></span>           | <span data-ttu-id="889ba-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889ba-195">0x00000010</span></span>                           |
| <span data-ttu-id="889ba-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889ba-196">Classes used in</span></span>        | [<span data-ttu-id="889ba-197">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="889ba-197">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="889ba-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="889ba-198">Windows Server 2008</span></span>



| <span data-ttu-id="889ba-199">進入</span><span class="sxs-lookup"><span data-stu-id="889ba-199">Entry</span></span> | <span data-ttu-id="889ba-200">值</span><span class="sxs-lookup"><span data-stu-id="889ba-200">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="889ba-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889ba-201">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889ba-202">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="889ba-203">System-Only</span></span>            | <span data-ttu-id="889ba-204">否</span><span class="sxs-lookup"><span data-stu-id="889ba-204">False</span></span>                                |
| <span data-ttu-id="889ba-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889ba-205">Is-Single-Valued</span></span>       | <span data-ttu-id="889ba-206">否</span><span class="sxs-lookup"><span data-stu-id="889ba-206">False</span></span>                                |
| <span data-ttu-id="889ba-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889ba-207">Is Indexed</span></span>             | <span data-ttu-id="889ba-208">否</span><span class="sxs-lookup"><span data-stu-id="889ba-208">False</span></span>                                |
| <span data-ttu-id="889ba-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889ba-209">In Global Catalog</span></span>      | <span data-ttu-id="889ba-210">否</span><span class="sxs-lookup"><span data-stu-id="889ba-210">False</span></span>                                |
| <span data-ttu-id="889ba-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889ba-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="889ba-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889ba-212">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="889ba-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889ba-213">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="889ba-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889ba-214">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="889ba-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-215">Search-Flags</span></span>           | <span data-ttu-id="889ba-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="889ba-216">0x00000000</span></span>                           |
| <span data-ttu-id="889ba-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-217">System-Flags</span></span>           | <span data-ttu-id="889ba-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889ba-218">0x00000010</span></span>                           |
| <span data-ttu-id="889ba-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889ba-219">Classes used in</span></span>        | [<span data-ttu-id="889ba-220">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="889ba-220">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="889ba-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="889ba-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="889ba-222">進入</span><span class="sxs-lookup"><span data-stu-id="889ba-222">Entry</span></span> | <span data-ttu-id="889ba-223">值</span><span class="sxs-lookup"><span data-stu-id="889ba-223">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="889ba-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889ba-224">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889ba-225">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="889ba-226">System-Only</span></span>            | <span data-ttu-id="889ba-227">否</span><span class="sxs-lookup"><span data-stu-id="889ba-227">False</span></span>                                |
| <span data-ttu-id="889ba-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889ba-228">Is-Single-Valued</span></span>       | <span data-ttu-id="889ba-229">否</span><span class="sxs-lookup"><span data-stu-id="889ba-229">False</span></span>                                |
| <span data-ttu-id="889ba-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889ba-230">Is Indexed</span></span>             | <span data-ttu-id="889ba-231">否</span><span class="sxs-lookup"><span data-stu-id="889ba-231">False</span></span>                                |
| <span data-ttu-id="889ba-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889ba-232">In Global Catalog</span></span>      | <span data-ttu-id="889ba-233">否</span><span class="sxs-lookup"><span data-stu-id="889ba-233">False</span></span>                                |
| <span data-ttu-id="889ba-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889ba-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="889ba-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889ba-235">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="889ba-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889ba-236">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="889ba-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889ba-237">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="889ba-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-238">Search-Flags</span></span>           | <span data-ttu-id="889ba-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="889ba-239">0x00000000</span></span>                           |
| <span data-ttu-id="889ba-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-240">System-Flags</span></span>           | <span data-ttu-id="889ba-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889ba-241">0x00000010</span></span>                           |
| <span data-ttu-id="889ba-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889ba-242">Classes used in</span></span>        | [<span data-ttu-id="889ba-243">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="889ba-243">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="889ba-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="889ba-244">Windows Server 2012</span></span>



| <span data-ttu-id="889ba-245">進入</span><span class="sxs-lookup"><span data-stu-id="889ba-245">Entry</span></span> | <span data-ttu-id="889ba-246">值</span><span class="sxs-lookup"><span data-stu-id="889ba-246">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="889ba-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="889ba-247">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="889ba-248">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="889ba-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="889ba-249">System-Only</span></span>            | <span data-ttu-id="889ba-250">否</span><span class="sxs-lookup"><span data-stu-id="889ba-250">False</span></span>                                |
| <span data-ttu-id="889ba-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="889ba-251">Is-Single-Valued</span></span>       | <span data-ttu-id="889ba-252">否</span><span class="sxs-lookup"><span data-stu-id="889ba-252">False</span></span>                                |
| <span data-ttu-id="889ba-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="889ba-253">Is Indexed</span></span>             | <span data-ttu-id="889ba-254">否</span><span class="sxs-lookup"><span data-stu-id="889ba-254">False</span></span>                                |
| <span data-ttu-id="889ba-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="889ba-255">In Global Catalog</span></span>      | <span data-ttu-id="889ba-256">否</span><span class="sxs-lookup"><span data-stu-id="889ba-256">False</span></span>                                |
| <span data-ttu-id="889ba-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="889ba-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="889ba-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="889ba-258">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="889ba-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="889ba-259">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="889ba-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="889ba-260">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="889ba-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-261">Search-Flags</span></span>           | <span data-ttu-id="889ba-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="889ba-262">0x00000000</span></span>                           |
| <span data-ttu-id="889ba-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="889ba-263">System-Flags</span></span>           | <span data-ttu-id="889ba-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="889ba-264">0x00000010</span></span>                           |
| <span data-ttu-id="889ba-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="889ba-265">Classes used in</span></span>        | [<span data-ttu-id="889ba-266">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="889ba-266">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





