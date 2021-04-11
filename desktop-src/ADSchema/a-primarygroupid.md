---
title: 主要群組-識別碼屬性
description: 包含使用者主要群組 (RID) 的相對識別碼。 根據預設，這是 Domain Users 群組的 RID。
ms.assetid: 80803734-f7dd-4348-a110-ca6b8bccb60b
ms.tgt_platform: multiple
keywords:
- 主要群組-識別碼屬性 AD 架構
- primaryGroupID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Primary-Group-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2b6237ff6e49a01da3b960b58103ae10dca7b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687156"
---
# <a name="primary-group-id-attribute"></a><span data-ttu-id="50330-106">主要群組-識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="50330-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="50330-107">包含使用者主要群組 (RID) 的相對識別碼。</span><span class="sxs-lookup"><span data-stu-id="50330-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="50330-108">根據預設，這是 Domain Users 群組的 RID。</span><span class="sxs-lookup"><span data-stu-id="50330-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="50330-109">進入</span><span class="sxs-lookup"><span data-stu-id="50330-109">Entry</span></span> | <span data-ttu-id="50330-110">值</span><span class="sxs-lookup"><span data-stu-id="50330-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="50330-111">CN</span><span class="sxs-lookup"><span data-stu-id="50330-111">CN</span></span>                | <span data-ttu-id="50330-112">主要群組-識別碼</span><span class="sxs-lookup"><span data-stu-id="50330-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="50330-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="50330-113">Ldap-Display-Name</span></span> | <span data-ttu-id="50330-114">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="50330-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="50330-115">大小</span><span class="sxs-lookup"><span data-stu-id="50330-115">Size</span></span>              | <span data-ttu-id="50330-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="50330-116">4 bytes</span></span>                              |
| <span data-ttu-id="50330-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="50330-117">Update Privilege</span></span>  | <span data-ttu-id="50330-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="50330-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="50330-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="50330-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="50330-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50330-120">Attribute-Id</span></span>      | <span data-ttu-id="50330-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="50330-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="50330-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="50330-122">System-Id-Guid</span></span>    | <span data-ttu-id="50330-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="50330-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="50330-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="50330-124">Syntax</span></span>            | [<span data-ttu-id="50330-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="50330-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="50330-126">實作</span><span class="sxs-lookup"><span data-stu-id="50330-126">Implementations</span></span>

-   [<span data-ttu-id="50330-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="50330-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="50330-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50330-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50330-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50330-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50330-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50330-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50330-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50330-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50330-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50330-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="50330-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="50330-133">Windows 2000 Server</span></span>



| <span data-ttu-id="50330-134">進入</span><span class="sxs-lookup"><span data-stu-id="50330-134">Entry</span></span> | <span data-ttu-id="50330-135">值</span><span class="sxs-lookup"><span data-stu-id="50330-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="50330-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50330-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50330-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="50330-138">System-Only</span></span>            | <span data-ttu-id="50330-139">否</span><span class="sxs-lookup"><span data-stu-id="50330-139">False</span></span>                             |
| <span data-ttu-id="50330-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50330-140">Is-Single-Valued</span></span>       | <span data-ttu-id="50330-141">對</span><span class="sxs-lookup"><span data-stu-id="50330-141">True</span></span>                              |
| <span data-ttu-id="50330-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50330-142">Is Indexed</span></span>             | <span data-ttu-id="50330-143">對</span><span class="sxs-lookup"><span data-stu-id="50330-143">True</span></span>                              |
| <span data-ttu-id="50330-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50330-144">In Global Catalog</span></span>      | <span data-ttu-id="50330-145">對</span><span class="sxs-lookup"><span data-stu-id="50330-145">True</span></span>                              |
| <span data-ttu-id="50330-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50330-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="50330-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50330-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="50330-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50330-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="50330-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50330-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="50330-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-150">Search-Flags</span></span>           | <span data-ttu-id="50330-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="50330-151">0x00000011</span></span>                        |
| <span data-ttu-id="50330-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-152">System-Flags</span></span>           | <span data-ttu-id="50330-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50330-153">0x00000012</span></span>                        |
| <span data-ttu-id="50330-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50330-154">Classes used in</span></span>        | [<span data-ttu-id="50330-155">**User**</span><span class="sxs-lookup"><span data-stu-id="50330-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="50330-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50330-156">Windows Server 2003</span></span>



| <span data-ttu-id="50330-157">進入</span><span class="sxs-lookup"><span data-stu-id="50330-157">Entry</span></span> | <span data-ttu-id="50330-158">值</span><span class="sxs-lookup"><span data-stu-id="50330-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="50330-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50330-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50330-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="50330-161">System-Only</span></span>            | <span data-ttu-id="50330-162">否</span><span class="sxs-lookup"><span data-stu-id="50330-162">False</span></span>                             |
| <span data-ttu-id="50330-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50330-163">Is-Single-Valued</span></span>       | <span data-ttu-id="50330-164">對</span><span class="sxs-lookup"><span data-stu-id="50330-164">True</span></span>                              |
| <span data-ttu-id="50330-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50330-165">Is Indexed</span></span>             | <span data-ttu-id="50330-166">對</span><span class="sxs-lookup"><span data-stu-id="50330-166">True</span></span>                              |
| <span data-ttu-id="50330-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50330-167">In Global Catalog</span></span>      | <span data-ttu-id="50330-168">對</span><span class="sxs-lookup"><span data-stu-id="50330-168">True</span></span>                              |
| <span data-ttu-id="50330-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50330-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="50330-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50330-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="50330-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50330-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="50330-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50330-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="50330-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-173">Search-Flags</span></span>           | <span data-ttu-id="50330-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="50330-174">0x00000011</span></span>                        |
| <span data-ttu-id="50330-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-175">System-Flags</span></span>           | <span data-ttu-id="50330-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50330-176">0x00000012</span></span>                        |
| <span data-ttu-id="50330-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50330-177">Classes used in</span></span>        | [<span data-ttu-id="50330-178">**User**</span><span class="sxs-lookup"><span data-stu-id="50330-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50330-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50330-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50330-180">進入</span><span class="sxs-lookup"><span data-stu-id="50330-180">Entry</span></span> | <span data-ttu-id="50330-181">值</span><span class="sxs-lookup"><span data-stu-id="50330-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="50330-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50330-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50330-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="50330-184">System-Only</span></span>            | <span data-ttu-id="50330-185">否</span><span class="sxs-lookup"><span data-stu-id="50330-185">False</span></span>                             |
| <span data-ttu-id="50330-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50330-186">Is-Single-Valued</span></span>       | <span data-ttu-id="50330-187">對</span><span class="sxs-lookup"><span data-stu-id="50330-187">True</span></span>                              |
| <span data-ttu-id="50330-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50330-188">Is Indexed</span></span>             | <span data-ttu-id="50330-189">對</span><span class="sxs-lookup"><span data-stu-id="50330-189">True</span></span>                              |
| <span data-ttu-id="50330-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50330-190">In Global Catalog</span></span>      | <span data-ttu-id="50330-191">對</span><span class="sxs-lookup"><span data-stu-id="50330-191">True</span></span>                              |
| <span data-ttu-id="50330-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50330-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="50330-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50330-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="50330-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50330-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="50330-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50330-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="50330-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-196">Search-Flags</span></span>           | <span data-ttu-id="50330-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="50330-197">0x00000011</span></span>                        |
| <span data-ttu-id="50330-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-198">System-Flags</span></span>           | <span data-ttu-id="50330-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50330-199">0x00000012</span></span>                        |
| <span data-ttu-id="50330-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50330-200">Classes used in</span></span>        | [<span data-ttu-id="50330-201">**User**</span><span class="sxs-lookup"><span data-stu-id="50330-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="50330-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50330-202">Windows Server 2008</span></span>



| <span data-ttu-id="50330-203">進入</span><span class="sxs-lookup"><span data-stu-id="50330-203">Entry</span></span> | <span data-ttu-id="50330-204">值</span><span class="sxs-lookup"><span data-stu-id="50330-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="50330-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50330-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50330-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="50330-207">System-Only</span></span>            | <span data-ttu-id="50330-208">否</span><span class="sxs-lookup"><span data-stu-id="50330-208">False</span></span>                             |
| <span data-ttu-id="50330-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50330-209">Is-Single-Valued</span></span>       | <span data-ttu-id="50330-210">對</span><span class="sxs-lookup"><span data-stu-id="50330-210">True</span></span>                              |
| <span data-ttu-id="50330-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50330-211">Is Indexed</span></span>             | <span data-ttu-id="50330-212">對</span><span class="sxs-lookup"><span data-stu-id="50330-212">True</span></span>                              |
| <span data-ttu-id="50330-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50330-213">In Global Catalog</span></span>      | <span data-ttu-id="50330-214">對</span><span class="sxs-lookup"><span data-stu-id="50330-214">True</span></span>                              |
| <span data-ttu-id="50330-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50330-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="50330-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50330-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="50330-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50330-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="50330-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50330-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="50330-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-219">Search-Flags</span></span>           | <span data-ttu-id="50330-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="50330-220">0x00000011</span></span>                        |
| <span data-ttu-id="50330-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-221">System-Flags</span></span>           | <span data-ttu-id="50330-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50330-222">0x00000012</span></span>                        |
| <span data-ttu-id="50330-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50330-223">Classes used in</span></span>        | [<span data-ttu-id="50330-224">**User**</span><span class="sxs-lookup"><span data-stu-id="50330-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50330-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50330-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50330-226">進入</span><span class="sxs-lookup"><span data-stu-id="50330-226">Entry</span></span> | <span data-ttu-id="50330-227">值</span><span class="sxs-lookup"><span data-stu-id="50330-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="50330-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50330-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50330-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="50330-230">System-Only</span></span>            | <span data-ttu-id="50330-231">否</span><span class="sxs-lookup"><span data-stu-id="50330-231">False</span></span>                             |
| <span data-ttu-id="50330-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50330-232">Is-Single-Valued</span></span>       | <span data-ttu-id="50330-233">對</span><span class="sxs-lookup"><span data-stu-id="50330-233">True</span></span>                              |
| <span data-ttu-id="50330-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50330-234">Is Indexed</span></span>             | <span data-ttu-id="50330-235">對</span><span class="sxs-lookup"><span data-stu-id="50330-235">True</span></span>                              |
| <span data-ttu-id="50330-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50330-236">In Global Catalog</span></span>      | <span data-ttu-id="50330-237">對</span><span class="sxs-lookup"><span data-stu-id="50330-237">True</span></span>                              |
| <span data-ttu-id="50330-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50330-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="50330-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50330-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="50330-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50330-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="50330-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50330-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="50330-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-242">Search-Flags</span></span>           | <span data-ttu-id="50330-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="50330-243">0x00000011</span></span>                        |
| <span data-ttu-id="50330-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-244">System-Flags</span></span>           | <span data-ttu-id="50330-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50330-245">0x00000012</span></span>                        |
| <span data-ttu-id="50330-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50330-246">Classes used in</span></span>        | [<span data-ttu-id="50330-247">**User**</span><span class="sxs-lookup"><span data-stu-id="50330-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50330-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50330-248">Windows Server 2012</span></span>



| <span data-ttu-id="50330-249">進入</span><span class="sxs-lookup"><span data-stu-id="50330-249">Entry</span></span> | <span data-ttu-id="50330-250">值</span><span class="sxs-lookup"><span data-stu-id="50330-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="50330-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50330-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50330-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="50330-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="50330-253">System-Only</span></span>            | <span data-ttu-id="50330-254">否</span><span class="sxs-lookup"><span data-stu-id="50330-254">False</span></span>                             |
| <span data-ttu-id="50330-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50330-255">Is-Single-Valued</span></span>       | <span data-ttu-id="50330-256">對</span><span class="sxs-lookup"><span data-stu-id="50330-256">True</span></span>                              |
| <span data-ttu-id="50330-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50330-257">Is Indexed</span></span>             | <span data-ttu-id="50330-258">對</span><span class="sxs-lookup"><span data-stu-id="50330-258">True</span></span>                              |
| <span data-ttu-id="50330-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50330-259">In Global Catalog</span></span>      | <span data-ttu-id="50330-260">對</span><span class="sxs-lookup"><span data-stu-id="50330-260">True</span></span>                              |
| <span data-ttu-id="50330-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50330-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="50330-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50330-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="50330-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50330-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="50330-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50330-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="50330-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-265">Search-Flags</span></span>           | <span data-ttu-id="50330-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="50330-266">0x00000011</span></span>                        |
| <span data-ttu-id="50330-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50330-267">System-Flags</span></span>           | <span data-ttu-id="50330-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="50330-268">0x00000012</span></span>                        |
| <span data-ttu-id="50330-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50330-269">Classes used in</span></span>        | [<span data-ttu-id="50330-270">**User**</span><span class="sxs-lookup"><span data-stu-id="50330-270">**User**</span></span>](c-user.md)<br/> |



 

 





