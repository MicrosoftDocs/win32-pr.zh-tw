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
# <a name="remote-server-name-attribute"></a><span data-ttu-id="7de55-105">遠端伺服器名稱屬性</span><span class="sxs-lookup"><span data-stu-id="7de55-105">Remote-Server-Name attribute</span></span>

<span data-ttu-id="7de55-106">在必須儲存一或多個電腦名稱稱的地方使用。</span><span class="sxs-lookup"><span data-stu-id="7de55-106">Used wherever one or more computer names must be stored.</span></span>



| <span data-ttu-id="7de55-107">進入</span><span class="sxs-lookup"><span data-stu-id="7de55-107">Entry</span></span> | <span data-ttu-id="7de55-108">值</span><span class="sxs-lookup"><span data-stu-id="7de55-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7de55-109">CN</span><span class="sxs-lookup"><span data-stu-id="7de55-109">CN</span></span>                | <span data-ttu-id="7de55-110">遠端伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="7de55-110">Remote-Server-Name</span></span>                          |
| <span data-ttu-id="7de55-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7de55-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7de55-112">remoteServerName</span><span class="sxs-lookup"><span data-stu-id="7de55-112">remoteServerName</span></span>                            |
| <span data-ttu-id="7de55-113">大小</span><span class="sxs-lookup"><span data-stu-id="7de55-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7de55-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7de55-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="7de55-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7de55-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7de55-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7de55-116">Attribute-Id</span></span>      | <span data-ttu-id="7de55-117">1.2.840.113556.1.4.105</span><span class="sxs-lookup"><span data-stu-id="7de55-117">1.2.840.113556.1.4.105</span></span>                      |
| <span data-ttu-id="7de55-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7de55-118">System-Id-Guid</span></span>    | <span data-ttu-id="7de55-119">bf967a12-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7de55-119">bf967a12-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="7de55-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de55-120">Syntax</span></span>            | [<span data-ttu-id="7de55-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7de55-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7de55-122">實作</span><span class="sxs-lookup"><span data-stu-id="7de55-122">Implementations</span></span>

-   [<span data-ttu-id="7de55-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7de55-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7de55-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7de55-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7de55-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7de55-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7de55-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7de55-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7de55-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7de55-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7de55-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7de55-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7de55-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7de55-129">Windows 2000 Server</span></span>



| <span data-ttu-id="7de55-130">進入</span><span class="sxs-lookup"><span data-stu-id="7de55-130">Entry</span></span> | <span data-ttu-id="7de55-131">值</span><span class="sxs-lookup"><span data-stu-id="7de55-131">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="7de55-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de55-132">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de55-133">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de55-134">System-Only</span></span>            | <span data-ttu-id="7de55-135">否</span><span class="sxs-lookup"><span data-stu-id="7de55-135">False</span></span>                                |
| <span data-ttu-id="7de55-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de55-136">Is-Single-Valued</span></span>       | <span data-ttu-id="7de55-137">否</span><span class="sxs-lookup"><span data-stu-id="7de55-137">False</span></span>                                |
| <span data-ttu-id="7de55-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de55-138">Is Indexed</span></span>             | <span data-ttu-id="7de55-139">否</span><span class="sxs-lookup"><span data-stu-id="7de55-139">False</span></span>                                |
| <span data-ttu-id="7de55-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de55-140">In Global Catalog</span></span>      | <span data-ttu-id="7de55-141">否</span><span class="sxs-lookup"><span data-stu-id="7de55-141">False</span></span>                                |
| <span data-ttu-id="7de55-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de55-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de55-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de55-143">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="7de55-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de55-144">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="7de55-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de55-145">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="7de55-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-146">Search-Flags</span></span>           | <span data-ttu-id="7de55-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de55-147">0x00000000</span></span>                           |
| <span data-ttu-id="7de55-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-148">System-Flags</span></span>           | <span data-ttu-id="7de55-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de55-149">0x00000010</span></span>                           |
| <span data-ttu-id="7de55-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de55-150">Classes used in</span></span>        | [<span data-ttu-id="7de55-151">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="7de55-151">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7de55-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7de55-152">Windows Server 2003</span></span>



| <span data-ttu-id="7de55-153">進入</span><span class="sxs-lookup"><span data-stu-id="7de55-153">Entry</span></span> | <span data-ttu-id="7de55-154">值</span><span class="sxs-lookup"><span data-stu-id="7de55-154">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="7de55-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de55-155">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de55-156">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de55-157">System-Only</span></span>            | <span data-ttu-id="7de55-158">否</span><span class="sxs-lookup"><span data-stu-id="7de55-158">False</span></span>                                |
| <span data-ttu-id="7de55-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de55-159">Is-Single-Valued</span></span>       | <span data-ttu-id="7de55-160">否</span><span class="sxs-lookup"><span data-stu-id="7de55-160">False</span></span>                                |
| <span data-ttu-id="7de55-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de55-161">Is Indexed</span></span>             | <span data-ttu-id="7de55-162">否</span><span class="sxs-lookup"><span data-stu-id="7de55-162">False</span></span>                                |
| <span data-ttu-id="7de55-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de55-163">In Global Catalog</span></span>      | <span data-ttu-id="7de55-164">否</span><span class="sxs-lookup"><span data-stu-id="7de55-164">False</span></span>                                |
| <span data-ttu-id="7de55-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de55-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de55-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de55-166">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="7de55-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de55-167">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="7de55-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de55-168">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="7de55-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-169">Search-Flags</span></span>           | <span data-ttu-id="7de55-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de55-170">0x00000000</span></span>                           |
| <span data-ttu-id="7de55-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-171">System-Flags</span></span>           | <span data-ttu-id="7de55-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de55-172">0x00000010</span></span>                           |
| <span data-ttu-id="7de55-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de55-173">Classes used in</span></span>        | [<span data-ttu-id="7de55-174">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="7de55-174">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7de55-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7de55-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7de55-176">進入</span><span class="sxs-lookup"><span data-stu-id="7de55-176">Entry</span></span> | <span data-ttu-id="7de55-177">值</span><span class="sxs-lookup"><span data-stu-id="7de55-177">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="7de55-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de55-178">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de55-179">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de55-180">System-Only</span></span>            | <span data-ttu-id="7de55-181">否</span><span class="sxs-lookup"><span data-stu-id="7de55-181">False</span></span>                                |
| <span data-ttu-id="7de55-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de55-182">Is-Single-Valued</span></span>       | <span data-ttu-id="7de55-183">否</span><span class="sxs-lookup"><span data-stu-id="7de55-183">False</span></span>                                |
| <span data-ttu-id="7de55-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de55-184">Is Indexed</span></span>             | <span data-ttu-id="7de55-185">否</span><span class="sxs-lookup"><span data-stu-id="7de55-185">False</span></span>                                |
| <span data-ttu-id="7de55-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de55-186">In Global Catalog</span></span>      | <span data-ttu-id="7de55-187">否</span><span class="sxs-lookup"><span data-stu-id="7de55-187">False</span></span>                                |
| <span data-ttu-id="7de55-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de55-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de55-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de55-189">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="7de55-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de55-190">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="7de55-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de55-191">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="7de55-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-192">Search-Flags</span></span>           | <span data-ttu-id="7de55-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de55-193">0x00000000</span></span>                           |
| <span data-ttu-id="7de55-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-194">System-Flags</span></span>           | <span data-ttu-id="7de55-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de55-195">0x00000010</span></span>                           |
| <span data-ttu-id="7de55-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de55-196">Classes used in</span></span>        | [<span data-ttu-id="7de55-197">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="7de55-197">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7de55-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7de55-198">Windows Server 2008</span></span>



| <span data-ttu-id="7de55-199">進入</span><span class="sxs-lookup"><span data-stu-id="7de55-199">Entry</span></span> | <span data-ttu-id="7de55-200">值</span><span class="sxs-lookup"><span data-stu-id="7de55-200">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="7de55-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de55-201">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de55-202">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de55-203">System-Only</span></span>            | <span data-ttu-id="7de55-204">否</span><span class="sxs-lookup"><span data-stu-id="7de55-204">False</span></span>                                |
| <span data-ttu-id="7de55-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de55-205">Is-Single-Valued</span></span>       | <span data-ttu-id="7de55-206">否</span><span class="sxs-lookup"><span data-stu-id="7de55-206">False</span></span>                                |
| <span data-ttu-id="7de55-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de55-207">Is Indexed</span></span>             | <span data-ttu-id="7de55-208">否</span><span class="sxs-lookup"><span data-stu-id="7de55-208">False</span></span>                                |
| <span data-ttu-id="7de55-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de55-209">In Global Catalog</span></span>      | <span data-ttu-id="7de55-210">否</span><span class="sxs-lookup"><span data-stu-id="7de55-210">False</span></span>                                |
| <span data-ttu-id="7de55-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de55-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de55-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de55-212">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="7de55-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de55-213">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="7de55-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de55-214">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="7de55-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-215">Search-Flags</span></span>           | <span data-ttu-id="7de55-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de55-216">0x00000000</span></span>                           |
| <span data-ttu-id="7de55-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-217">System-Flags</span></span>           | <span data-ttu-id="7de55-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de55-218">0x00000010</span></span>                           |
| <span data-ttu-id="7de55-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de55-219">Classes used in</span></span>        | [<span data-ttu-id="7de55-220">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="7de55-220">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7de55-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7de55-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7de55-222">進入</span><span class="sxs-lookup"><span data-stu-id="7de55-222">Entry</span></span> | <span data-ttu-id="7de55-223">值</span><span class="sxs-lookup"><span data-stu-id="7de55-223">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="7de55-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de55-224">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de55-225">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de55-226">System-Only</span></span>            | <span data-ttu-id="7de55-227">否</span><span class="sxs-lookup"><span data-stu-id="7de55-227">False</span></span>                                |
| <span data-ttu-id="7de55-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de55-228">Is-Single-Valued</span></span>       | <span data-ttu-id="7de55-229">否</span><span class="sxs-lookup"><span data-stu-id="7de55-229">False</span></span>                                |
| <span data-ttu-id="7de55-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de55-230">Is Indexed</span></span>             | <span data-ttu-id="7de55-231">否</span><span class="sxs-lookup"><span data-stu-id="7de55-231">False</span></span>                                |
| <span data-ttu-id="7de55-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de55-232">In Global Catalog</span></span>      | <span data-ttu-id="7de55-233">否</span><span class="sxs-lookup"><span data-stu-id="7de55-233">False</span></span>                                |
| <span data-ttu-id="7de55-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de55-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de55-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de55-235">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="7de55-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de55-236">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="7de55-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de55-237">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="7de55-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-238">Search-Flags</span></span>           | <span data-ttu-id="7de55-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de55-239">0x00000000</span></span>                           |
| <span data-ttu-id="7de55-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-240">System-Flags</span></span>           | <span data-ttu-id="7de55-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de55-241">0x00000010</span></span>                           |
| <span data-ttu-id="7de55-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de55-242">Classes used in</span></span>        | [<span data-ttu-id="7de55-243">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="7de55-243">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7de55-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7de55-244">Windows Server 2012</span></span>



| <span data-ttu-id="7de55-245">進入</span><span class="sxs-lookup"><span data-stu-id="7de55-245">Entry</span></span> | <span data-ttu-id="7de55-246">值</span><span class="sxs-lookup"><span data-stu-id="7de55-246">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="7de55-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de55-247">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de55-248">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="7de55-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de55-249">System-Only</span></span>            | <span data-ttu-id="7de55-250">否</span><span class="sxs-lookup"><span data-stu-id="7de55-250">False</span></span>                                |
| <span data-ttu-id="7de55-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de55-251">Is-Single-Valued</span></span>       | <span data-ttu-id="7de55-252">否</span><span class="sxs-lookup"><span data-stu-id="7de55-252">False</span></span>                                |
| <span data-ttu-id="7de55-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de55-253">Is Indexed</span></span>             | <span data-ttu-id="7de55-254">否</span><span class="sxs-lookup"><span data-stu-id="7de55-254">False</span></span>                                |
| <span data-ttu-id="7de55-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de55-255">In Global Catalog</span></span>      | <span data-ttu-id="7de55-256">否</span><span class="sxs-lookup"><span data-stu-id="7de55-256">False</span></span>                                |
| <span data-ttu-id="7de55-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de55-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de55-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de55-258">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="7de55-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de55-259">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="7de55-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de55-260">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="7de55-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-261">Search-Flags</span></span>           | <span data-ttu-id="7de55-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de55-262">0x00000000</span></span>                           |
| <span data-ttu-id="7de55-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de55-263">System-Flags</span></span>           | <span data-ttu-id="7de55-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de55-264">0x00000010</span></span>                           |
| <span data-ttu-id="7de55-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de55-265">Classes used in</span></span>        | [<span data-ttu-id="7de55-266">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="7de55-266">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





