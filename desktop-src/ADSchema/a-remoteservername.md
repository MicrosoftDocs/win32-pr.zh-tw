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
# <a name="remote-server-name-attribute"></a><span data-ttu-id="0c568-105">遠端伺服器名稱屬性</span><span class="sxs-lookup"><span data-stu-id="0c568-105">Remote-Server-Name attribute</span></span>

<span data-ttu-id="0c568-106">在必須儲存一或多個電腦名稱稱的地方使用。</span><span class="sxs-lookup"><span data-stu-id="0c568-106">Used wherever one or more computer names must be stored.</span></span>



| <span data-ttu-id="0c568-107">進入</span><span class="sxs-lookup"><span data-stu-id="0c568-107">Entry</span></span> | <span data-ttu-id="0c568-108">值</span><span class="sxs-lookup"><span data-stu-id="0c568-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0c568-109">CN</span><span class="sxs-lookup"><span data-stu-id="0c568-109">CN</span></span>                | <span data-ttu-id="0c568-110">遠端伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="0c568-110">Remote-Server-Name</span></span>                          |
| <span data-ttu-id="0c568-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0c568-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0c568-112">remoteServerName</span><span class="sxs-lookup"><span data-stu-id="0c568-112">remoteServerName</span></span>                            |
| <span data-ttu-id="0c568-113">大小</span><span class="sxs-lookup"><span data-stu-id="0c568-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0c568-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0c568-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="0c568-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0c568-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0c568-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c568-116">Attribute-Id</span></span>      | <span data-ttu-id="0c568-117">1.2.840.113556.1.4.105</span><span class="sxs-lookup"><span data-stu-id="0c568-117">1.2.840.113556.1.4.105</span></span>                      |
| <span data-ttu-id="0c568-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0c568-118">System-Id-Guid</span></span>    | <span data-ttu-id="0c568-119">bf967a12-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0c568-119">bf967a12-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="0c568-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c568-120">Syntax</span></span>            | [<span data-ttu-id="0c568-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0c568-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0c568-122">實作</span><span class="sxs-lookup"><span data-stu-id="0c568-122">Implementations</span></span>

-   [<span data-ttu-id="0c568-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c568-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c568-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c568-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c568-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c568-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c568-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c568-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c568-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c568-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c568-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c568-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c568-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c568-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0c568-130">進入</span><span class="sxs-lookup"><span data-stu-id="0c568-130">Entry</span></span> | <span data-ttu-id="0c568-131">值</span><span class="sxs-lookup"><span data-stu-id="0c568-131">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="0c568-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c568-132">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c568-133">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c568-134">System-Only</span></span>            | <span data-ttu-id="0c568-135">否</span><span class="sxs-lookup"><span data-stu-id="0c568-135">False</span></span>                                |
| <span data-ttu-id="0c568-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c568-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0c568-137">否</span><span class="sxs-lookup"><span data-stu-id="0c568-137">False</span></span>                                |
| <span data-ttu-id="0c568-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c568-138">Is Indexed</span></span>             | <span data-ttu-id="0c568-139">否</span><span class="sxs-lookup"><span data-stu-id="0c568-139">False</span></span>                                |
| <span data-ttu-id="0c568-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c568-140">In Global Catalog</span></span>      | <span data-ttu-id="0c568-141">否</span><span class="sxs-lookup"><span data-stu-id="0c568-141">False</span></span>                                |
| <span data-ttu-id="0c568-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c568-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c568-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c568-143">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="0c568-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c568-144">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="0c568-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c568-145">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="0c568-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-146">Search-Flags</span></span>           | <span data-ttu-id="0c568-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c568-147">0x00000000</span></span>                           |
| <span data-ttu-id="0c568-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-148">System-Flags</span></span>           | <span data-ttu-id="0c568-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c568-149">0x00000010</span></span>                           |
| <span data-ttu-id="0c568-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c568-150">Classes used in</span></span>        | [<span data-ttu-id="0c568-151">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="0c568-151">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c568-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c568-152">Windows Server 2003</span></span>



| <span data-ttu-id="0c568-153">進入</span><span class="sxs-lookup"><span data-stu-id="0c568-153">Entry</span></span> | <span data-ttu-id="0c568-154">值</span><span class="sxs-lookup"><span data-stu-id="0c568-154">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="0c568-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c568-155">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c568-156">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c568-157">System-Only</span></span>            | <span data-ttu-id="0c568-158">否</span><span class="sxs-lookup"><span data-stu-id="0c568-158">False</span></span>                                |
| <span data-ttu-id="0c568-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c568-159">Is-Single-Valued</span></span>       | <span data-ttu-id="0c568-160">否</span><span class="sxs-lookup"><span data-stu-id="0c568-160">False</span></span>                                |
| <span data-ttu-id="0c568-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c568-161">Is Indexed</span></span>             | <span data-ttu-id="0c568-162">否</span><span class="sxs-lookup"><span data-stu-id="0c568-162">False</span></span>                                |
| <span data-ttu-id="0c568-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c568-163">In Global Catalog</span></span>      | <span data-ttu-id="0c568-164">否</span><span class="sxs-lookup"><span data-stu-id="0c568-164">False</span></span>                                |
| <span data-ttu-id="0c568-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c568-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c568-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c568-166">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="0c568-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c568-167">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="0c568-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c568-168">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="0c568-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-169">Search-Flags</span></span>           | <span data-ttu-id="0c568-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c568-170">0x00000000</span></span>                           |
| <span data-ttu-id="0c568-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-171">System-Flags</span></span>           | <span data-ttu-id="0c568-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c568-172">0x00000010</span></span>                           |
| <span data-ttu-id="0c568-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c568-173">Classes used in</span></span>        | [<span data-ttu-id="0c568-174">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="0c568-174">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c568-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c568-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c568-176">進入</span><span class="sxs-lookup"><span data-stu-id="0c568-176">Entry</span></span> | <span data-ttu-id="0c568-177">值</span><span class="sxs-lookup"><span data-stu-id="0c568-177">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="0c568-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c568-178">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c568-179">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c568-180">System-Only</span></span>            | <span data-ttu-id="0c568-181">否</span><span class="sxs-lookup"><span data-stu-id="0c568-181">False</span></span>                                |
| <span data-ttu-id="0c568-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c568-182">Is-Single-Valued</span></span>       | <span data-ttu-id="0c568-183">否</span><span class="sxs-lookup"><span data-stu-id="0c568-183">False</span></span>                                |
| <span data-ttu-id="0c568-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c568-184">Is Indexed</span></span>             | <span data-ttu-id="0c568-185">否</span><span class="sxs-lookup"><span data-stu-id="0c568-185">False</span></span>                                |
| <span data-ttu-id="0c568-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c568-186">In Global Catalog</span></span>      | <span data-ttu-id="0c568-187">否</span><span class="sxs-lookup"><span data-stu-id="0c568-187">False</span></span>                                |
| <span data-ttu-id="0c568-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c568-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c568-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c568-189">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="0c568-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c568-190">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="0c568-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c568-191">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="0c568-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-192">Search-Flags</span></span>           | <span data-ttu-id="0c568-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c568-193">0x00000000</span></span>                           |
| <span data-ttu-id="0c568-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-194">System-Flags</span></span>           | <span data-ttu-id="0c568-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c568-195">0x00000010</span></span>                           |
| <span data-ttu-id="0c568-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c568-196">Classes used in</span></span>        | [<span data-ttu-id="0c568-197">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="0c568-197">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c568-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c568-198">Windows Server 2008</span></span>



| <span data-ttu-id="0c568-199">進入</span><span class="sxs-lookup"><span data-stu-id="0c568-199">Entry</span></span> | <span data-ttu-id="0c568-200">值</span><span class="sxs-lookup"><span data-stu-id="0c568-200">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="0c568-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c568-201">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c568-202">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c568-203">System-Only</span></span>            | <span data-ttu-id="0c568-204">否</span><span class="sxs-lookup"><span data-stu-id="0c568-204">False</span></span>                                |
| <span data-ttu-id="0c568-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c568-205">Is-Single-Valued</span></span>       | <span data-ttu-id="0c568-206">否</span><span class="sxs-lookup"><span data-stu-id="0c568-206">False</span></span>                                |
| <span data-ttu-id="0c568-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c568-207">Is Indexed</span></span>             | <span data-ttu-id="0c568-208">否</span><span class="sxs-lookup"><span data-stu-id="0c568-208">False</span></span>                                |
| <span data-ttu-id="0c568-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c568-209">In Global Catalog</span></span>      | <span data-ttu-id="0c568-210">否</span><span class="sxs-lookup"><span data-stu-id="0c568-210">False</span></span>                                |
| <span data-ttu-id="0c568-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c568-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c568-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c568-212">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="0c568-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c568-213">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="0c568-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c568-214">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="0c568-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-215">Search-Flags</span></span>           | <span data-ttu-id="0c568-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c568-216">0x00000000</span></span>                           |
| <span data-ttu-id="0c568-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-217">System-Flags</span></span>           | <span data-ttu-id="0c568-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c568-218">0x00000010</span></span>                           |
| <span data-ttu-id="0c568-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c568-219">Classes used in</span></span>        | [<span data-ttu-id="0c568-220">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="0c568-220">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c568-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c568-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c568-222">進入</span><span class="sxs-lookup"><span data-stu-id="0c568-222">Entry</span></span> | <span data-ttu-id="0c568-223">值</span><span class="sxs-lookup"><span data-stu-id="0c568-223">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="0c568-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c568-224">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c568-225">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c568-226">System-Only</span></span>            | <span data-ttu-id="0c568-227">否</span><span class="sxs-lookup"><span data-stu-id="0c568-227">False</span></span>                                |
| <span data-ttu-id="0c568-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c568-228">Is-Single-Valued</span></span>       | <span data-ttu-id="0c568-229">否</span><span class="sxs-lookup"><span data-stu-id="0c568-229">False</span></span>                                |
| <span data-ttu-id="0c568-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c568-230">Is Indexed</span></span>             | <span data-ttu-id="0c568-231">否</span><span class="sxs-lookup"><span data-stu-id="0c568-231">False</span></span>                                |
| <span data-ttu-id="0c568-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c568-232">In Global Catalog</span></span>      | <span data-ttu-id="0c568-233">否</span><span class="sxs-lookup"><span data-stu-id="0c568-233">False</span></span>                                |
| <span data-ttu-id="0c568-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c568-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c568-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c568-235">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="0c568-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c568-236">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="0c568-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c568-237">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="0c568-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-238">Search-Flags</span></span>           | <span data-ttu-id="0c568-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c568-239">0x00000000</span></span>                           |
| <span data-ttu-id="0c568-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-240">System-Flags</span></span>           | <span data-ttu-id="0c568-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c568-241">0x00000010</span></span>                           |
| <span data-ttu-id="0c568-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c568-242">Classes used in</span></span>        | [<span data-ttu-id="0c568-243">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="0c568-243">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c568-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c568-244">Windows Server 2012</span></span>



| <span data-ttu-id="0c568-245">進入</span><span class="sxs-lookup"><span data-stu-id="0c568-245">Entry</span></span> | <span data-ttu-id="0c568-246">值</span><span class="sxs-lookup"><span data-stu-id="0c568-246">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="0c568-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c568-247">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c568-248">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="0c568-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c568-249">System-Only</span></span>            | <span data-ttu-id="0c568-250">否</span><span class="sxs-lookup"><span data-stu-id="0c568-250">False</span></span>                                |
| <span data-ttu-id="0c568-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c568-251">Is-Single-Valued</span></span>       | <span data-ttu-id="0c568-252">否</span><span class="sxs-lookup"><span data-stu-id="0c568-252">False</span></span>                                |
| <span data-ttu-id="0c568-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c568-253">Is Indexed</span></span>             | <span data-ttu-id="0c568-254">否</span><span class="sxs-lookup"><span data-stu-id="0c568-254">False</span></span>                                |
| <span data-ttu-id="0c568-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c568-255">In Global Catalog</span></span>      | <span data-ttu-id="0c568-256">否</span><span class="sxs-lookup"><span data-stu-id="0c568-256">False</span></span>                                |
| <span data-ttu-id="0c568-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c568-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c568-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c568-258">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="0c568-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c568-259">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="0c568-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c568-260">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="0c568-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-261">Search-Flags</span></span>           | <span data-ttu-id="0c568-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c568-262">0x00000000</span></span>                           |
| <span data-ttu-id="0c568-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c568-263">System-Flags</span></span>           | <span data-ttu-id="0c568-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c568-264">0x00000010</span></span>                           |
| <span data-ttu-id="0c568-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c568-265">Classes used in</span></span>        | [<span data-ttu-id="0c568-266">**FT-Dfs**</span><span class="sxs-lookup"><span data-stu-id="0c568-266">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





