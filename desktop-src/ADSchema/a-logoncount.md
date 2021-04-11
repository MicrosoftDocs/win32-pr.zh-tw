---
title: Logon-Count 屬性
description: 帳戶成功登入的次數。 值為0表示值不明。
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Logon-Count 屬性 AD 架構
- logonCount 屬性 AD 架構
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845227"
---
# <a name="logon-count-attribute"></a><span data-ttu-id="dd651-106">Logon-Count 屬性</span><span class="sxs-lookup"><span data-stu-id="dd651-106">Logon-Count attribute</span></span>

<span data-ttu-id="dd651-107">帳戶成功登入的次數。</span><span class="sxs-lookup"><span data-stu-id="dd651-107">The number of times the account has successfully logged on.</span></span> <span data-ttu-id="dd651-108">值為0表示值不明。</span><span class="sxs-lookup"><span data-stu-id="dd651-108">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="dd651-109">進入</span><span class="sxs-lookup"><span data-stu-id="dd651-109">Entry</span></span> | <span data-ttu-id="dd651-110">值</span><span class="sxs-lookup"><span data-stu-id="dd651-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="dd651-111">CN</span><span class="sxs-lookup"><span data-stu-id="dd651-111">CN</span></span>                | <span data-ttu-id="dd651-112">Logon-Count</span><span class="sxs-lookup"><span data-stu-id="dd651-112">Logon-Count</span></span>                          |
| <span data-ttu-id="dd651-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dd651-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dd651-114">logonCount</span><span class="sxs-lookup"><span data-stu-id="dd651-114">logonCount</span></span>                           |
| <span data-ttu-id="dd651-115">大小</span><span class="sxs-lookup"><span data-stu-id="dd651-115">Size</span></span>              | <span data-ttu-id="dd651-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="dd651-116">4 bytes</span></span>                              |
| <span data-ttu-id="dd651-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dd651-117">Update Privilege</span></span>  | <span data-ttu-id="dd651-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="dd651-118">Domain administrator</span></span>                 |
| <span data-ttu-id="dd651-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dd651-119">Update Frequency</span></span>  | <span data-ttu-id="dd651-120">每次使用者登入時。</span><span class="sxs-lookup"><span data-stu-id="dd651-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="dd651-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dd651-121">Attribute-Id</span></span>      | <span data-ttu-id="dd651-122">1.2.840.113556.1.4.169</span><span class="sxs-lookup"><span data-stu-id="dd651-122">1.2.840.113556.1.4.169</span></span>               |
| <span data-ttu-id="dd651-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dd651-123">System-Id-Guid</span></span>    | <span data-ttu-id="dd651-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dd651-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="dd651-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd651-125">Syntax</span></span>            | [<span data-ttu-id="dd651-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="dd651-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="dd651-127">實作</span><span class="sxs-lookup"><span data-stu-id="dd651-127">Implementations</span></span>

-   [<span data-ttu-id="dd651-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dd651-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dd651-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dd651-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dd651-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dd651-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dd651-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dd651-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dd651-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dd651-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dd651-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dd651-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dd651-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd651-134">Windows 2000 Server</span></span>



| <span data-ttu-id="dd651-135">進入</span><span class="sxs-lookup"><span data-stu-id="dd651-135">Entry</span></span> | <span data-ttu-id="dd651-136">值</span><span class="sxs-lookup"><span data-stu-id="dd651-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dd651-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd651-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd651-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd651-139">System-Only</span></span>            | <span data-ttu-id="dd651-140">否</span><span class="sxs-lookup"><span data-stu-id="dd651-140">False</span></span>                             |
| <span data-ttu-id="dd651-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd651-141">Is-Single-Valued</span></span>       | <span data-ttu-id="dd651-142">對</span><span class="sxs-lookup"><span data-stu-id="dd651-142">True</span></span>                              |
| <span data-ttu-id="dd651-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd651-143">Is Indexed</span></span>             | <span data-ttu-id="dd651-144">否</span><span class="sxs-lookup"><span data-stu-id="dd651-144">False</span></span>                             |
| <span data-ttu-id="dd651-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd651-145">In Global Catalog</span></span>      | <span data-ttu-id="dd651-146">否</span><span class="sxs-lookup"><span data-stu-id="dd651-146">False</span></span>                             |
| <span data-ttu-id="dd651-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd651-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd651-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd651-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dd651-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd651-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dd651-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd651-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dd651-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-151">Search-Flags</span></span>           | <span data-ttu-id="dd651-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd651-152">0x00000000</span></span>                        |
| <span data-ttu-id="dd651-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-153">System-Flags</span></span>           | <span data-ttu-id="dd651-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="dd651-154">0x00000011</span></span>                        |
| <span data-ttu-id="dd651-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd651-155">Classes used in</span></span>        | [<span data-ttu-id="dd651-156">**User**</span><span class="sxs-lookup"><span data-stu-id="dd651-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dd651-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd651-157">Windows Server 2003</span></span>



| <span data-ttu-id="dd651-158">進入</span><span class="sxs-lookup"><span data-stu-id="dd651-158">Entry</span></span> | <span data-ttu-id="dd651-159">值</span><span class="sxs-lookup"><span data-stu-id="dd651-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dd651-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd651-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd651-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd651-162">System-Only</span></span>            | <span data-ttu-id="dd651-163">否</span><span class="sxs-lookup"><span data-stu-id="dd651-163">False</span></span>                             |
| <span data-ttu-id="dd651-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd651-164">Is-Single-Valued</span></span>       | <span data-ttu-id="dd651-165">對</span><span class="sxs-lookup"><span data-stu-id="dd651-165">True</span></span>                              |
| <span data-ttu-id="dd651-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd651-166">Is Indexed</span></span>             | <span data-ttu-id="dd651-167">否</span><span class="sxs-lookup"><span data-stu-id="dd651-167">False</span></span>                             |
| <span data-ttu-id="dd651-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd651-168">In Global Catalog</span></span>      | <span data-ttu-id="dd651-169">否</span><span class="sxs-lookup"><span data-stu-id="dd651-169">False</span></span>                             |
| <span data-ttu-id="dd651-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd651-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd651-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd651-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dd651-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd651-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dd651-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd651-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dd651-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-174">Search-Flags</span></span>           | <span data-ttu-id="dd651-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd651-175">0x00000000</span></span>                        |
| <span data-ttu-id="dd651-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-176">System-Flags</span></span>           | <span data-ttu-id="dd651-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="dd651-177">0x00000011</span></span>                        |
| <span data-ttu-id="dd651-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd651-178">Classes used in</span></span>        | [<span data-ttu-id="dd651-179">**User**</span><span class="sxs-lookup"><span data-stu-id="dd651-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dd651-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dd651-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dd651-181">進入</span><span class="sxs-lookup"><span data-stu-id="dd651-181">Entry</span></span> | <span data-ttu-id="dd651-182">值</span><span class="sxs-lookup"><span data-stu-id="dd651-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dd651-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd651-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd651-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd651-185">System-Only</span></span>            | <span data-ttu-id="dd651-186">否</span><span class="sxs-lookup"><span data-stu-id="dd651-186">False</span></span>                             |
| <span data-ttu-id="dd651-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd651-187">Is-Single-Valued</span></span>       | <span data-ttu-id="dd651-188">對</span><span class="sxs-lookup"><span data-stu-id="dd651-188">True</span></span>                              |
| <span data-ttu-id="dd651-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd651-189">Is Indexed</span></span>             | <span data-ttu-id="dd651-190">否</span><span class="sxs-lookup"><span data-stu-id="dd651-190">False</span></span>                             |
| <span data-ttu-id="dd651-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd651-191">In Global Catalog</span></span>      | <span data-ttu-id="dd651-192">否</span><span class="sxs-lookup"><span data-stu-id="dd651-192">False</span></span>                             |
| <span data-ttu-id="dd651-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd651-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd651-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd651-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dd651-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd651-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dd651-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd651-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dd651-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-197">Search-Flags</span></span>           | <span data-ttu-id="dd651-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd651-198">0x00000000</span></span>                        |
| <span data-ttu-id="dd651-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-199">System-Flags</span></span>           | <span data-ttu-id="dd651-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="dd651-200">0x00000011</span></span>                        |
| <span data-ttu-id="dd651-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd651-201">Classes used in</span></span>        | [<span data-ttu-id="dd651-202">**User**</span><span class="sxs-lookup"><span data-stu-id="dd651-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dd651-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd651-203">Windows Server 2008</span></span>



| <span data-ttu-id="dd651-204">進入</span><span class="sxs-lookup"><span data-stu-id="dd651-204">Entry</span></span> | <span data-ttu-id="dd651-205">值</span><span class="sxs-lookup"><span data-stu-id="dd651-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dd651-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd651-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd651-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd651-208">System-Only</span></span>            | <span data-ttu-id="dd651-209">否</span><span class="sxs-lookup"><span data-stu-id="dd651-209">False</span></span>                             |
| <span data-ttu-id="dd651-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd651-210">Is-Single-Valued</span></span>       | <span data-ttu-id="dd651-211">對</span><span class="sxs-lookup"><span data-stu-id="dd651-211">True</span></span>                              |
| <span data-ttu-id="dd651-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd651-212">Is Indexed</span></span>             | <span data-ttu-id="dd651-213">否</span><span class="sxs-lookup"><span data-stu-id="dd651-213">False</span></span>                             |
| <span data-ttu-id="dd651-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd651-214">In Global Catalog</span></span>      | <span data-ttu-id="dd651-215">否</span><span class="sxs-lookup"><span data-stu-id="dd651-215">False</span></span>                             |
| <span data-ttu-id="dd651-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd651-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd651-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd651-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dd651-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd651-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dd651-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd651-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dd651-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-220">Search-Flags</span></span>           | <span data-ttu-id="dd651-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd651-221">0x00000000</span></span>                        |
| <span data-ttu-id="dd651-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-222">System-Flags</span></span>           | <span data-ttu-id="dd651-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="dd651-223">0x00000011</span></span>                        |
| <span data-ttu-id="dd651-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd651-224">Classes used in</span></span>        | [<span data-ttu-id="dd651-225">**User**</span><span class="sxs-lookup"><span data-stu-id="dd651-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dd651-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd651-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dd651-227">進入</span><span class="sxs-lookup"><span data-stu-id="dd651-227">Entry</span></span> | <span data-ttu-id="dd651-228">值</span><span class="sxs-lookup"><span data-stu-id="dd651-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dd651-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd651-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd651-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd651-231">System-Only</span></span>            | <span data-ttu-id="dd651-232">否</span><span class="sxs-lookup"><span data-stu-id="dd651-232">False</span></span>                             |
| <span data-ttu-id="dd651-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd651-233">Is-Single-Valued</span></span>       | <span data-ttu-id="dd651-234">對</span><span class="sxs-lookup"><span data-stu-id="dd651-234">True</span></span>                              |
| <span data-ttu-id="dd651-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd651-235">Is Indexed</span></span>             | <span data-ttu-id="dd651-236">否</span><span class="sxs-lookup"><span data-stu-id="dd651-236">False</span></span>                             |
| <span data-ttu-id="dd651-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd651-237">In Global Catalog</span></span>      | <span data-ttu-id="dd651-238">否</span><span class="sxs-lookup"><span data-stu-id="dd651-238">False</span></span>                             |
| <span data-ttu-id="dd651-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd651-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd651-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd651-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dd651-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd651-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dd651-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd651-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dd651-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-243">Search-Flags</span></span>           | <span data-ttu-id="dd651-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd651-244">0x00000000</span></span>                        |
| <span data-ttu-id="dd651-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-245">System-Flags</span></span>           | <span data-ttu-id="dd651-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="dd651-246">0x00000011</span></span>                        |
| <span data-ttu-id="dd651-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd651-247">Classes used in</span></span>        | [<span data-ttu-id="dd651-248">**User**</span><span class="sxs-lookup"><span data-stu-id="dd651-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dd651-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd651-249">Windows Server 2012</span></span>



| <span data-ttu-id="dd651-250">進入</span><span class="sxs-lookup"><span data-stu-id="dd651-250">Entry</span></span> | <span data-ttu-id="dd651-251">值</span><span class="sxs-lookup"><span data-stu-id="dd651-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dd651-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd651-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd651-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dd651-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd651-254">System-Only</span></span>            | <span data-ttu-id="dd651-255">否</span><span class="sxs-lookup"><span data-stu-id="dd651-255">False</span></span>                             |
| <span data-ttu-id="dd651-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd651-256">Is-Single-Valued</span></span>       | <span data-ttu-id="dd651-257">對</span><span class="sxs-lookup"><span data-stu-id="dd651-257">True</span></span>                              |
| <span data-ttu-id="dd651-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd651-258">Is Indexed</span></span>             | <span data-ttu-id="dd651-259">否</span><span class="sxs-lookup"><span data-stu-id="dd651-259">False</span></span>                             |
| <span data-ttu-id="dd651-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd651-260">In Global Catalog</span></span>      | <span data-ttu-id="dd651-261">否</span><span class="sxs-lookup"><span data-stu-id="dd651-261">False</span></span>                             |
| <span data-ttu-id="dd651-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd651-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd651-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd651-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dd651-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd651-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dd651-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd651-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dd651-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-266">Search-Flags</span></span>           | <span data-ttu-id="dd651-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd651-267">0x00000000</span></span>                        |
| <span data-ttu-id="dd651-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd651-268">System-Flags</span></span>           | <span data-ttu-id="dd651-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="dd651-269">0x00000011</span></span>                        |
| <span data-ttu-id="dd651-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd651-270">Classes used in</span></span>        | [<span data-ttu-id="dd651-271">**User**</span><span class="sxs-lookup"><span data-stu-id="dd651-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="dd651-272">備註</span><span class="sxs-lookup"><span data-stu-id="dd651-272">Remarks</span></span>

<span data-ttu-id="dd651-273">這個屬性不會複寫，並且會保留在網域中的每個網域控制站上。</span><span class="sxs-lookup"><span data-stu-id="dd651-273">This attribute is not replicated and is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="dd651-274">若要取得使用者在網域中成功登入嘗試總數的精確值，必須查詢網域中的每個網域控制站，並使用值的總和。</span><span class="sxs-lookup"><span data-stu-id="dd651-274">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span> <span data-ttu-id="dd651-275">請記住，此屬性不會複寫，因此已淘汰的網域控制站也可能會有使用者的計數登入，而這將會從計數中遺失。</span><span class="sxs-lookup"><span data-stu-id="dd651-275">Keep in mind that the attribute is not replicated, therefore domain controllers that are retired may have counted logons for the user as well, and these will be missing from the count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd651-276">由於與16位版 LAN Manager 的相容性，因此屬性的上限為65535。</span><span class="sxs-lookup"><span data-stu-id="dd651-276">Due to compatibility with 16-bit versions of LAN Manager, the attribute has an upper limit of 65535.</span></span> <span data-ttu-id="dd651-277">達到此限制之後，您就無法將它用作為此網域控制站上的使用者活動指標。</span><span class="sxs-lookup"><span data-stu-id="dd651-277">After this limit has been reached, you cannot use it as an indicator of user activity on this domain controller.</span></span>

 

 

 





