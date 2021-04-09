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
# <a name="primary-group-id-attribute"></a><span data-ttu-id="28ef0-106">主要群組-識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="28ef0-106">Primary-Group-ID attribute</span></span>

<span data-ttu-id="28ef0-107">包含使用者主要群組 (RID) 的相對識別碼。</span><span class="sxs-lookup"><span data-stu-id="28ef0-107">Contains the relative identifier (RID) for the primary group of the user.</span></span> <span data-ttu-id="28ef0-108">根據預設，這是 Domain Users 群組的 RID。</span><span class="sxs-lookup"><span data-stu-id="28ef0-108">By default, this is the RID for the Domain Users group.</span></span>



| <span data-ttu-id="28ef0-109">進入</span><span class="sxs-lookup"><span data-stu-id="28ef0-109">Entry</span></span> | <span data-ttu-id="28ef0-110">值</span><span class="sxs-lookup"><span data-stu-id="28ef0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="28ef0-111">CN</span><span class="sxs-lookup"><span data-stu-id="28ef0-111">CN</span></span>                | <span data-ttu-id="28ef0-112">主要群組-識別碼</span><span class="sxs-lookup"><span data-stu-id="28ef0-112">Primary-Group-ID</span></span>                     |
| <span data-ttu-id="28ef0-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="28ef0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="28ef0-114">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="28ef0-114">primaryGroupID</span></span>                       |
| <span data-ttu-id="28ef0-115">大小</span><span class="sxs-lookup"><span data-stu-id="28ef0-115">Size</span></span>              | <span data-ttu-id="28ef0-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="28ef0-116">4 bytes</span></span>                              |
| <span data-ttu-id="28ef0-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="28ef0-117">Update Privilege</span></span>  | <span data-ttu-id="28ef0-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="28ef0-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="28ef0-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="28ef0-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="28ef0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28ef0-120">Attribute-Id</span></span>      | <span data-ttu-id="28ef0-121">1.2.840.113556.1.4.98</span><span class="sxs-lookup"><span data-stu-id="28ef0-121">1.2.840.113556.1.4.98</span></span>                |
| <span data-ttu-id="28ef0-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="28ef0-122">System-Id-Guid</span></span>    | <span data-ttu-id="28ef0-123">bf967a00-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="28ef0-123">bf967a00-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="28ef0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="28ef0-124">Syntax</span></span>            | [<span data-ttu-id="28ef0-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="28ef0-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="28ef0-126">實作</span><span class="sxs-lookup"><span data-stu-id="28ef0-126">Implementations</span></span>

-   [<span data-ttu-id="28ef0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28ef0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28ef0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28ef0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28ef0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28ef0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28ef0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28ef0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28ef0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28ef0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28ef0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28ef0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28ef0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28ef0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="28ef0-134">進入</span><span class="sxs-lookup"><span data-stu-id="28ef0-134">Entry</span></span> | <span data-ttu-id="28ef0-135">值</span><span class="sxs-lookup"><span data-stu-id="28ef0-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28ef0-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28ef0-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28ef0-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="28ef0-138">System-Only</span></span>            | <span data-ttu-id="28ef0-139">否</span><span class="sxs-lookup"><span data-stu-id="28ef0-139">False</span></span>                             |
| <span data-ttu-id="28ef0-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28ef0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="28ef0-141">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-141">True</span></span>                              |
| <span data-ttu-id="28ef0-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28ef0-142">Is Indexed</span></span>             | <span data-ttu-id="28ef0-143">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-143">True</span></span>                              |
| <span data-ttu-id="28ef0-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28ef0-144">In Global Catalog</span></span>      | <span data-ttu-id="28ef0-145">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-145">True</span></span>                              |
| <span data-ttu-id="28ef0-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28ef0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="28ef0-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28ef0-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28ef0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28ef0-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28ef0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28ef0-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28ef0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-150">Search-Flags</span></span>           | <span data-ttu-id="28ef0-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="28ef0-151">0x00000011</span></span>                        |
| <span data-ttu-id="28ef0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-152">System-Flags</span></span>           | <span data-ttu-id="28ef0-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="28ef0-153">0x00000012</span></span>                        |
| <span data-ttu-id="28ef0-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28ef0-154">Classes used in</span></span>        | [<span data-ttu-id="28ef0-155">**User**</span><span class="sxs-lookup"><span data-stu-id="28ef0-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="28ef0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28ef0-156">Windows Server 2003</span></span>



| <span data-ttu-id="28ef0-157">進入</span><span class="sxs-lookup"><span data-stu-id="28ef0-157">Entry</span></span> | <span data-ttu-id="28ef0-158">值</span><span class="sxs-lookup"><span data-stu-id="28ef0-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28ef0-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28ef0-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28ef0-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="28ef0-161">System-Only</span></span>            | <span data-ttu-id="28ef0-162">否</span><span class="sxs-lookup"><span data-stu-id="28ef0-162">False</span></span>                             |
| <span data-ttu-id="28ef0-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28ef0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="28ef0-164">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-164">True</span></span>                              |
| <span data-ttu-id="28ef0-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28ef0-165">Is Indexed</span></span>             | <span data-ttu-id="28ef0-166">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-166">True</span></span>                              |
| <span data-ttu-id="28ef0-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28ef0-167">In Global Catalog</span></span>      | <span data-ttu-id="28ef0-168">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-168">True</span></span>                              |
| <span data-ttu-id="28ef0-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28ef0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="28ef0-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28ef0-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28ef0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28ef0-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28ef0-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28ef0-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28ef0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-173">Search-Flags</span></span>           | <span data-ttu-id="28ef0-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="28ef0-174">0x00000011</span></span>                        |
| <span data-ttu-id="28ef0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-175">System-Flags</span></span>           | <span data-ttu-id="28ef0-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="28ef0-176">0x00000012</span></span>                        |
| <span data-ttu-id="28ef0-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28ef0-177">Classes used in</span></span>        | [<span data-ttu-id="28ef0-178">**User**</span><span class="sxs-lookup"><span data-stu-id="28ef0-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28ef0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28ef0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28ef0-180">進入</span><span class="sxs-lookup"><span data-stu-id="28ef0-180">Entry</span></span> | <span data-ttu-id="28ef0-181">值</span><span class="sxs-lookup"><span data-stu-id="28ef0-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28ef0-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28ef0-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28ef0-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="28ef0-184">System-Only</span></span>            | <span data-ttu-id="28ef0-185">否</span><span class="sxs-lookup"><span data-stu-id="28ef0-185">False</span></span>                             |
| <span data-ttu-id="28ef0-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28ef0-186">Is-Single-Valued</span></span>       | <span data-ttu-id="28ef0-187">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-187">True</span></span>                              |
| <span data-ttu-id="28ef0-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28ef0-188">Is Indexed</span></span>             | <span data-ttu-id="28ef0-189">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-189">True</span></span>                              |
| <span data-ttu-id="28ef0-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28ef0-190">In Global Catalog</span></span>      | <span data-ttu-id="28ef0-191">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-191">True</span></span>                              |
| <span data-ttu-id="28ef0-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28ef0-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="28ef0-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28ef0-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28ef0-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28ef0-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28ef0-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28ef0-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28ef0-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-196">Search-Flags</span></span>           | <span data-ttu-id="28ef0-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="28ef0-197">0x00000011</span></span>                        |
| <span data-ttu-id="28ef0-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-198">System-Flags</span></span>           | <span data-ttu-id="28ef0-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="28ef0-199">0x00000012</span></span>                        |
| <span data-ttu-id="28ef0-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28ef0-200">Classes used in</span></span>        | [<span data-ttu-id="28ef0-201">**User**</span><span class="sxs-lookup"><span data-stu-id="28ef0-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28ef0-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28ef0-202">Windows Server 2008</span></span>



| <span data-ttu-id="28ef0-203">進入</span><span class="sxs-lookup"><span data-stu-id="28ef0-203">Entry</span></span> | <span data-ttu-id="28ef0-204">值</span><span class="sxs-lookup"><span data-stu-id="28ef0-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28ef0-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28ef0-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28ef0-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="28ef0-207">System-Only</span></span>            | <span data-ttu-id="28ef0-208">否</span><span class="sxs-lookup"><span data-stu-id="28ef0-208">False</span></span>                             |
| <span data-ttu-id="28ef0-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28ef0-209">Is-Single-Valued</span></span>       | <span data-ttu-id="28ef0-210">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-210">True</span></span>                              |
| <span data-ttu-id="28ef0-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28ef0-211">Is Indexed</span></span>             | <span data-ttu-id="28ef0-212">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-212">True</span></span>                              |
| <span data-ttu-id="28ef0-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28ef0-213">In Global Catalog</span></span>      | <span data-ttu-id="28ef0-214">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-214">True</span></span>                              |
| <span data-ttu-id="28ef0-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28ef0-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="28ef0-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28ef0-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28ef0-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28ef0-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28ef0-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28ef0-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28ef0-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-219">Search-Flags</span></span>           | <span data-ttu-id="28ef0-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="28ef0-220">0x00000011</span></span>                        |
| <span data-ttu-id="28ef0-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-221">System-Flags</span></span>           | <span data-ttu-id="28ef0-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="28ef0-222">0x00000012</span></span>                        |
| <span data-ttu-id="28ef0-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28ef0-223">Classes used in</span></span>        | [<span data-ttu-id="28ef0-224">**User**</span><span class="sxs-lookup"><span data-stu-id="28ef0-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28ef0-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28ef0-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28ef0-226">進入</span><span class="sxs-lookup"><span data-stu-id="28ef0-226">Entry</span></span> | <span data-ttu-id="28ef0-227">值</span><span class="sxs-lookup"><span data-stu-id="28ef0-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28ef0-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28ef0-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28ef0-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="28ef0-230">System-Only</span></span>            | <span data-ttu-id="28ef0-231">否</span><span class="sxs-lookup"><span data-stu-id="28ef0-231">False</span></span>                             |
| <span data-ttu-id="28ef0-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28ef0-232">Is-Single-Valued</span></span>       | <span data-ttu-id="28ef0-233">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-233">True</span></span>                              |
| <span data-ttu-id="28ef0-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28ef0-234">Is Indexed</span></span>             | <span data-ttu-id="28ef0-235">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-235">True</span></span>                              |
| <span data-ttu-id="28ef0-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28ef0-236">In Global Catalog</span></span>      | <span data-ttu-id="28ef0-237">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-237">True</span></span>                              |
| <span data-ttu-id="28ef0-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28ef0-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="28ef0-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28ef0-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28ef0-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28ef0-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28ef0-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28ef0-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28ef0-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-242">Search-Flags</span></span>           | <span data-ttu-id="28ef0-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="28ef0-243">0x00000011</span></span>                        |
| <span data-ttu-id="28ef0-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-244">System-Flags</span></span>           | <span data-ttu-id="28ef0-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="28ef0-245">0x00000012</span></span>                        |
| <span data-ttu-id="28ef0-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28ef0-246">Classes used in</span></span>        | [<span data-ttu-id="28ef0-247">**User**</span><span class="sxs-lookup"><span data-stu-id="28ef0-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28ef0-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28ef0-248">Windows Server 2012</span></span>



| <span data-ttu-id="28ef0-249">進入</span><span class="sxs-lookup"><span data-stu-id="28ef0-249">Entry</span></span> | <span data-ttu-id="28ef0-250">值</span><span class="sxs-lookup"><span data-stu-id="28ef0-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28ef0-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28ef0-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28ef0-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28ef0-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="28ef0-253">System-Only</span></span>            | <span data-ttu-id="28ef0-254">否</span><span class="sxs-lookup"><span data-stu-id="28ef0-254">False</span></span>                             |
| <span data-ttu-id="28ef0-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28ef0-255">Is-Single-Valued</span></span>       | <span data-ttu-id="28ef0-256">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-256">True</span></span>                              |
| <span data-ttu-id="28ef0-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28ef0-257">Is Indexed</span></span>             | <span data-ttu-id="28ef0-258">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-258">True</span></span>                              |
| <span data-ttu-id="28ef0-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28ef0-259">In Global Catalog</span></span>      | <span data-ttu-id="28ef0-260">對</span><span class="sxs-lookup"><span data-stu-id="28ef0-260">True</span></span>                              |
| <span data-ttu-id="28ef0-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28ef0-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="28ef0-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28ef0-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28ef0-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28ef0-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28ef0-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28ef0-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28ef0-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-265">Search-Flags</span></span>           | <span data-ttu-id="28ef0-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="28ef0-266">0x00000011</span></span>                        |
| <span data-ttu-id="28ef0-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28ef0-267">System-Flags</span></span>           | <span data-ttu-id="28ef0-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="28ef0-268">0x00000012</span></span>                        |
| <span data-ttu-id="28ef0-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28ef0-269">Classes used in</span></span>        | [<span data-ttu-id="28ef0-270">**User**</span><span class="sxs-lookup"><span data-stu-id="28ef0-270">**User**</span></span>](c-user.md)<br/> |



 

 





