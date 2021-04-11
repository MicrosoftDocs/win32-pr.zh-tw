---
title: 非安全性成員屬性
description: 非安全性群組的成員。 用於 Exchange 通訊群組清單。
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- 非安全性成員屬性 AD 架構
- nonSecurityMember 屬性 AD 架構
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a04919d9d538ff4da97d73e79d14e9a2706032b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935509"
---
# <a name="non-security-member-attribute"></a><span data-ttu-id="1cf28-106">非安全性成員屬性</span><span class="sxs-lookup"><span data-stu-id="1cf28-106">Non-Security-Member attribute</span></span>

<span data-ttu-id="1cf28-107">非安全性群組的成員。</span><span class="sxs-lookup"><span data-stu-id="1cf28-107">Nonsecurity members of a group.</span></span> <span data-ttu-id="1cf28-108">用於 Exchange 通訊群組清單。</span><span class="sxs-lookup"><span data-stu-id="1cf28-108">Used for Exchange distribution lists.</span></span>



| <span data-ttu-id="1cf28-109">進入</span><span class="sxs-lookup"><span data-stu-id="1cf28-109">Entry</span></span> | <span data-ttu-id="1cf28-110">值</span><span class="sxs-lookup"><span data-stu-id="1cf28-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="1cf28-111">CN</span><span class="sxs-lookup"><span data-stu-id="1cf28-111">CN</span></span>                | <span data-ttu-id="1cf28-112">非安全性成員</span><span class="sxs-lookup"><span data-stu-id="1cf28-112">Non-Security-Member</span></span>                              |
| <span data-ttu-id="1cf28-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1cf28-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1cf28-114">nonSecurityMember</span><span class="sxs-lookup"><span data-stu-id="1cf28-114">nonSecurityMember</span></span>                                |
| <span data-ttu-id="1cf28-115">大小</span><span class="sxs-lookup"><span data-stu-id="1cf28-115">Size</span></span>              | \-                                               |
| <span data-ttu-id="1cf28-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1cf28-116">Update Privilege</span></span>  | <span data-ttu-id="1cf28-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="1cf28-117">Domain administrator</span></span>                             |
| <span data-ttu-id="1cf28-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1cf28-118">Update Frequency</span></span>  | <span data-ttu-id="1cf28-119">每次在 DL 中新增或移除使用者時。</span><span class="sxs-lookup"><span data-stu-id="1cf28-119">Whenever a user is added or removed from the DL.</span></span> |
| <span data-ttu-id="1cf28-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1cf28-120">Attribute-Id</span></span>      | <span data-ttu-id="1cf28-121">1.2.840.113556.1.4.530</span><span class="sxs-lookup"><span data-stu-id="1cf28-121">1.2.840.113556.1.4.530</span></span>                           |
| <span data-ttu-id="1cf28-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1cf28-122">System-Id-Guid</span></span>    | <span data-ttu-id="1cf28-123">52458018-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1cf28-123">52458018-ca6a-11d0-afff-0000f80367c1</span></span>             |
| <span data-ttu-id="1cf28-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cf28-124">Syntax</span></span>            | [<span data-ttu-id="1cf28-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1cf28-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="1cf28-126">實作</span><span class="sxs-lookup"><span data-stu-id="1cf28-126">Implementations</span></span>

-   [<span data-ttu-id="1cf28-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1cf28-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1cf28-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1cf28-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1cf28-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1cf28-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1cf28-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1cf28-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1cf28-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1cf28-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1cf28-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1cf28-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1cf28-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cf28-133">Windows 2000 Server</span></span>



| <span data-ttu-id="1cf28-134">進入</span><span class="sxs-lookup"><span data-stu-id="1cf28-134">Entry</span></span> | <span data-ttu-id="1cf28-135">值</span><span class="sxs-lookup"><span data-stu-id="1cf28-135">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1cf28-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1cf28-136">Link-Id</span></span>                | <span data-ttu-id="1cf28-137">50</span><span class="sxs-lookup"><span data-stu-id="1cf28-137">50</span></span>                                  |
| <span data-ttu-id="1cf28-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf28-138">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1cf28-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf28-139">System-Only</span></span>            | <span data-ttu-id="1cf28-140">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-140">False</span></span>                               |
| <span data-ttu-id="1cf28-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1cf28-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf28-142">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-142">False</span></span>                               |
| <span data-ttu-id="1cf28-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1cf28-143">Is Indexed</span></span>             | <span data-ttu-id="1cf28-144">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-144">False</span></span>                               |
| <span data-ttu-id="1cf28-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1cf28-145">In Global Catalog</span></span>      | <span data-ttu-id="1cf28-146">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-146">False</span></span>                               |
| <span data-ttu-id="1cf28-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1cf28-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf28-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1cf28-148">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1cf28-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf28-149">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf28-150">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-151">Search-Flags</span></span>           | <span data-ttu-id="1cf28-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cf28-152">0x00000000</span></span>                          |
| <span data-ttu-id="1cf28-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-153">System-Flags</span></span>           | <span data-ttu-id="1cf28-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf28-154">0x00000010</span></span>                          |
| <span data-ttu-id="1cf28-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1cf28-155">Classes used in</span></span>        | [<span data-ttu-id="1cf28-156">**Group**</span><span class="sxs-lookup"><span data-stu-id="1cf28-156">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1cf28-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cf28-157">Windows Server 2003</span></span>



| <span data-ttu-id="1cf28-158">進入</span><span class="sxs-lookup"><span data-stu-id="1cf28-158">Entry</span></span> | <span data-ttu-id="1cf28-159">值</span><span class="sxs-lookup"><span data-stu-id="1cf28-159">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1cf28-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1cf28-160">Link-Id</span></span>                | <span data-ttu-id="1cf28-161">50</span><span class="sxs-lookup"><span data-stu-id="1cf28-161">50</span></span>                                  |
| <span data-ttu-id="1cf28-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf28-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1cf28-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf28-163">System-Only</span></span>            | <span data-ttu-id="1cf28-164">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-164">False</span></span>                               |
| <span data-ttu-id="1cf28-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1cf28-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf28-166">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-166">False</span></span>                               |
| <span data-ttu-id="1cf28-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1cf28-167">Is Indexed</span></span>             | <span data-ttu-id="1cf28-168">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-168">False</span></span>                               |
| <span data-ttu-id="1cf28-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1cf28-169">In Global Catalog</span></span>      | <span data-ttu-id="1cf28-170">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-170">False</span></span>                               |
| <span data-ttu-id="1cf28-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1cf28-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf28-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1cf28-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1cf28-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf28-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf28-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-175">Search-Flags</span></span>           | <span data-ttu-id="1cf28-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cf28-176">0x00000000</span></span>                          |
| <span data-ttu-id="1cf28-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-177">System-Flags</span></span>           | <span data-ttu-id="1cf28-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf28-178">0x00000010</span></span>                          |
| <span data-ttu-id="1cf28-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1cf28-179">Classes used in</span></span>        | [<span data-ttu-id="1cf28-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="1cf28-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1cf28-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1cf28-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1cf28-182">進入</span><span class="sxs-lookup"><span data-stu-id="1cf28-182">Entry</span></span> | <span data-ttu-id="1cf28-183">值</span><span class="sxs-lookup"><span data-stu-id="1cf28-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1cf28-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1cf28-184">Link-Id</span></span>                | <span data-ttu-id="1cf28-185">50</span><span class="sxs-lookup"><span data-stu-id="1cf28-185">50</span></span>                                  |
| <span data-ttu-id="1cf28-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf28-186">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1cf28-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf28-187">System-Only</span></span>            | <span data-ttu-id="1cf28-188">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-188">False</span></span>                               |
| <span data-ttu-id="1cf28-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1cf28-189">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf28-190">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-190">False</span></span>                               |
| <span data-ttu-id="1cf28-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1cf28-191">Is Indexed</span></span>             | <span data-ttu-id="1cf28-192">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-192">False</span></span>                               |
| <span data-ttu-id="1cf28-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1cf28-193">In Global Catalog</span></span>      | <span data-ttu-id="1cf28-194">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-194">False</span></span>                               |
| <span data-ttu-id="1cf28-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1cf28-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf28-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1cf28-196">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1cf28-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf28-197">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf28-198">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-199">Search-Flags</span></span>           | <span data-ttu-id="1cf28-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cf28-200">0x00000000</span></span>                          |
| <span data-ttu-id="1cf28-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-201">System-Flags</span></span>           | <span data-ttu-id="1cf28-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf28-202">0x00000010</span></span>                          |
| <span data-ttu-id="1cf28-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1cf28-203">Classes used in</span></span>        | [<span data-ttu-id="1cf28-204">**Group**</span><span class="sxs-lookup"><span data-stu-id="1cf28-204">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1cf28-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cf28-205">Windows Server 2008</span></span>



| <span data-ttu-id="1cf28-206">進入</span><span class="sxs-lookup"><span data-stu-id="1cf28-206">Entry</span></span> | <span data-ttu-id="1cf28-207">值</span><span class="sxs-lookup"><span data-stu-id="1cf28-207">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1cf28-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1cf28-208">Link-Id</span></span>                | <span data-ttu-id="1cf28-209">50</span><span class="sxs-lookup"><span data-stu-id="1cf28-209">50</span></span>                                  |
| <span data-ttu-id="1cf28-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf28-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1cf28-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf28-211">System-Only</span></span>            | <span data-ttu-id="1cf28-212">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-212">False</span></span>                               |
| <span data-ttu-id="1cf28-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1cf28-213">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf28-214">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-214">False</span></span>                               |
| <span data-ttu-id="1cf28-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1cf28-215">Is Indexed</span></span>             | <span data-ttu-id="1cf28-216">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-216">False</span></span>                               |
| <span data-ttu-id="1cf28-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1cf28-217">In Global Catalog</span></span>      | <span data-ttu-id="1cf28-218">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-218">False</span></span>                               |
| <span data-ttu-id="1cf28-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1cf28-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf28-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1cf28-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1cf28-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf28-221">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf28-222">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-223">Search-Flags</span></span>           | <span data-ttu-id="1cf28-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cf28-224">0x00000000</span></span>                          |
| <span data-ttu-id="1cf28-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-225">System-Flags</span></span>           | <span data-ttu-id="1cf28-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf28-226">0x00000010</span></span>                          |
| <span data-ttu-id="1cf28-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1cf28-227">Classes used in</span></span>        | [<span data-ttu-id="1cf28-228">**Group**</span><span class="sxs-lookup"><span data-stu-id="1cf28-228">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1cf28-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1cf28-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1cf28-230">進入</span><span class="sxs-lookup"><span data-stu-id="1cf28-230">Entry</span></span> | <span data-ttu-id="1cf28-231">值</span><span class="sxs-lookup"><span data-stu-id="1cf28-231">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1cf28-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1cf28-232">Link-Id</span></span>                | <span data-ttu-id="1cf28-233">50</span><span class="sxs-lookup"><span data-stu-id="1cf28-233">50</span></span>                                  |
| <span data-ttu-id="1cf28-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf28-234">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1cf28-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf28-235">System-Only</span></span>            | <span data-ttu-id="1cf28-236">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-236">False</span></span>                               |
| <span data-ttu-id="1cf28-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1cf28-237">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf28-238">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-238">False</span></span>                               |
| <span data-ttu-id="1cf28-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1cf28-239">Is Indexed</span></span>             | <span data-ttu-id="1cf28-240">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-240">False</span></span>                               |
| <span data-ttu-id="1cf28-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1cf28-241">In Global Catalog</span></span>      | <span data-ttu-id="1cf28-242">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-242">False</span></span>                               |
| <span data-ttu-id="1cf28-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1cf28-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf28-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1cf28-244">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1cf28-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf28-245">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf28-246">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-247">Search-Flags</span></span>           | <span data-ttu-id="1cf28-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cf28-248">0x00000000</span></span>                          |
| <span data-ttu-id="1cf28-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-249">System-Flags</span></span>           | <span data-ttu-id="1cf28-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf28-250">0x00000010</span></span>                          |
| <span data-ttu-id="1cf28-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1cf28-251">Classes used in</span></span>        | [<span data-ttu-id="1cf28-252">**Group**</span><span class="sxs-lookup"><span data-stu-id="1cf28-252">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1cf28-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1cf28-253">Windows Server 2012</span></span>



| <span data-ttu-id="1cf28-254">進入</span><span class="sxs-lookup"><span data-stu-id="1cf28-254">Entry</span></span> | <span data-ttu-id="1cf28-255">值</span><span class="sxs-lookup"><span data-stu-id="1cf28-255">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="1cf28-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1cf28-256">Link-Id</span></span>                | <span data-ttu-id="1cf28-257">50</span><span class="sxs-lookup"><span data-stu-id="1cf28-257">50</span></span>                                  |
| <span data-ttu-id="1cf28-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf28-258">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="1cf28-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf28-259">System-Only</span></span>            | <span data-ttu-id="1cf28-260">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-260">False</span></span>                               |
| <span data-ttu-id="1cf28-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1cf28-261">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf28-262">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-262">False</span></span>                               |
| <span data-ttu-id="1cf28-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1cf28-263">Is Indexed</span></span>             | <span data-ttu-id="1cf28-264">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-264">False</span></span>                               |
| <span data-ttu-id="1cf28-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1cf28-265">In Global Catalog</span></span>      | <span data-ttu-id="1cf28-266">否</span><span class="sxs-lookup"><span data-stu-id="1cf28-266">False</span></span>                               |
| <span data-ttu-id="1cf28-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1cf28-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf28-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1cf28-268">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="1cf28-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf28-269">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf28-270">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="1cf28-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-271">Search-Flags</span></span>           | <span data-ttu-id="1cf28-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1cf28-272">0x00000000</span></span>                          |
| <span data-ttu-id="1cf28-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf28-273">System-Flags</span></span>           | <span data-ttu-id="1cf28-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf28-274">0x00000010</span></span>                          |
| <span data-ttu-id="1cf28-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1cf28-275">Classes used in</span></span>        | [<span data-ttu-id="1cf28-276">**Group**</span><span class="sxs-lookup"><span data-stu-id="1cf28-276">**Group**</span></span>](c-group.md)<br/> |



 

 





