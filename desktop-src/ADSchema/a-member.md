---
title: Member 屬性
description: 屬於群組的使用者清單。
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- 成員屬性 AD 架構
- 成員屬性 AD 架構
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106967384"
---
# <a name="member-attribute"></a><span data-ttu-id="81b44-105">Member 屬性</span><span class="sxs-lookup"><span data-stu-id="81b44-105">Member attribute</span></span>

<span data-ttu-id="81b44-106">屬於群組的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="81b44-106">The list of users that belong to the group.</span></span>



| <span data-ttu-id="81b44-107">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-107">Entry</span></span> | <span data-ttu-id="81b44-108">值</span><span class="sxs-lookup"><span data-stu-id="81b44-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="81b44-109">CN</span><span class="sxs-lookup"><span data-stu-id="81b44-109">CN</span></span>                | <span data-ttu-id="81b44-110">成員</span><span class="sxs-lookup"><span data-stu-id="81b44-110">Member</span></span>                                                |
| <span data-ttu-id="81b44-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="81b44-111">Ldap-Display-Name</span></span> | <span data-ttu-id="81b44-112">member</span><span class="sxs-lookup"><span data-stu-id="81b44-112">member</span></span>                                                |
| <span data-ttu-id="81b44-113">大小</span><span class="sxs-lookup"><span data-stu-id="81b44-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="81b44-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="81b44-114">Update Privilege</span></span>  | <span data-ttu-id="81b44-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="81b44-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="81b44-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="81b44-116">Update Frequency</span></span>  | <span data-ttu-id="81b44-117">每次在群組中新增或移除使用者時。</span><span class="sxs-lookup"><span data-stu-id="81b44-117">Each time a user is added to or removed from a group.</span></span> |
| <span data-ttu-id="81b44-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-118">Attribute-Id</span></span>      | <span data-ttu-id="81b44-119">2.5.4.31</span><span class="sxs-lookup"><span data-stu-id="81b44-119">2.5.4.31</span></span>                                              |
| <span data-ttu-id="81b44-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="81b44-120">System-Id-Guid</span></span>    | <span data-ttu-id="81b44-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="81b44-121">bf9679c0-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="81b44-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="81b44-122">Syntax</span></span>            | [<span data-ttu-id="81b44-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="81b44-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)               |



## <a name="implementations"></a><span data-ttu-id="81b44-124">實作</span><span class="sxs-lookup"><span data-stu-id="81b44-124">Implementations</span></span>

-   [<span data-ttu-id="81b44-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="81b44-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="81b44-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="81b44-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="81b44-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="81b44-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="81b44-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="81b44-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="81b44-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="81b44-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="81b44-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="81b44-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="81b44-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="81b44-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="81b44-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81b44-132">Windows 2000 Server</span></span>



| <span data-ttu-id="81b44-133">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-133">Entry</span></span> | <span data-ttu-id="81b44-134">值</span><span class="sxs-lookup"><span data-stu-id="81b44-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81b44-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81b44-135">Link-Id</span></span>                | <span data-ttu-id="81b44-136">2</span><span class="sxs-lookup"><span data-stu-id="81b44-136">2</span></span>                                                                                       |
| <span data-ttu-id="81b44-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-137">MAPI-Id</span></span>                | <span data-ttu-id="81b44-138">0x8009</span><span class="sxs-lookup"><span data-stu-id="81b44-138">0x8009</span></span>                                                                                  |
| <span data-ttu-id="81b44-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="81b44-139">System-Only</span></span>            | <span data-ttu-id="81b44-140">否</span><span class="sxs-lookup"><span data-stu-id="81b44-140">False</span></span>                                                                                   |
| <span data-ttu-id="81b44-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81b44-141">Is-Single-Valued</span></span>       | <span data-ttu-id="81b44-142">否</span><span class="sxs-lookup"><span data-stu-id="81b44-142">False</span></span>                                                                                   |
| <span data-ttu-id="81b44-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81b44-143">Is Indexed</span></span>             | <span data-ttu-id="81b44-144">否</span><span class="sxs-lookup"><span data-stu-id="81b44-144">False</span></span>                                                                                   |
| <span data-ttu-id="81b44-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81b44-145">In Global Catalog</span></span>      | <span data-ttu-id="81b44-146">對</span><span class="sxs-lookup"><span data-stu-id="81b44-146">True</span></span>                                                                                    |
| <span data-ttu-id="81b44-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81b44-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="81b44-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81b44-148">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="81b44-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81b44-149">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="81b44-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81b44-150">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="81b44-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-151">Search-Flags</span></span>           | <span data-ttu-id="81b44-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81b44-152">0x00000000</span></span>                                                                              |
| <span data-ttu-id="81b44-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-153">System-Flags</span></span>           | <span data-ttu-id="81b44-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="81b44-154">0x00000012</span></span>                                                                              |
| <span data-ttu-id="81b44-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81b44-155">Classes used in</span></span>        | [<span data-ttu-id="81b44-156">**Group**</span><span class="sxs-lookup"><span data-stu-id="81b44-156">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="81b44-157">**名稱群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-157">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="81b44-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81b44-158">Windows Server 2003</span></span>



| <span data-ttu-id="81b44-159">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-159">Entry</span></span> | <span data-ttu-id="81b44-160">值</span><span class="sxs-lookup"><span data-stu-id="81b44-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b44-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81b44-161">Link-Id</span></span>                | <span data-ttu-id="81b44-162">2</span><span class="sxs-lookup"><span data-stu-id="81b44-162">2</span></span>                                                                                                                                     |
| <span data-ttu-id="81b44-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-163">MAPI-Id</span></span>                | <span data-ttu-id="81b44-164">0x8009</span><span class="sxs-lookup"><span data-stu-id="81b44-164">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="81b44-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="81b44-165">System-Only</span></span>            | <span data-ttu-id="81b44-166">否</span><span class="sxs-lookup"><span data-stu-id="81b44-166">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81b44-167">Is-Single-Valued</span></span>       | <span data-ttu-id="81b44-168">否</span><span class="sxs-lookup"><span data-stu-id="81b44-168">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81b44-169">Is Indexed</span></span>             | <span data-ttu-id="81b44-170">否</span><span class="sxs-lookup"><span data-stu-id="81b44-170">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81b44-171">In Global Catalog</span></span>      | <span data-ttu-id="81b44-172">對</span><span class="sxs-lookup"><span data-stu-id="81b44-172">True</span></span>                                                                                                                                  |
| <span data-ttu-id="81b44-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81b44-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="81b44-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81b44-174">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="81b44-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81b44-175">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81b44-176">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-177">Search-Flags</span></span>           | <span data-ttu-id="81b44-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81b44-178">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-179">System-Flags</span></span>           | <span data-ttu-id="81b44-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="81b44-180">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81b44-181">Classes used in</span></span>        | [<span data-ttu-id="81b44-182">**Group**</span><span class="sxs-lookup"><span data-stu-id="81b44-182">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="81b44-183">**名稱群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-183">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="81b44-184">**MSMQ 群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-184">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="81b44-185">亞當</span><span class="sxs-lookup"><span data-stu-id="81b44-185">ADAM</span></span>



| <span data-ttu-id="81b44-186">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-186">Entry</span></span> | <span data-ttu-id="81b44-187">值</span><span class="sxs-lookup"><span data-stu-id="81b44-187">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="81b44-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81b44-188">Link-Id</span></span>                | <span data-ttu-id="81b44-189">2</span><span class="sxs-lookup"><span data-stu-id="81b44-189">2</span></span>                                   |
| <span data-ttu-id="81b44-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-190">MAPI-Id</span></span>                | <span data-ttu-id="81b44-191">0x8009</span><span class="sxs-lookup"><span data-stu-id="81b44-191">0x8009</span></span>                              |
| <span data-ttu-id="81b44-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="81b44-192">System-Only</span></span>            | <span data-ttu-id="81b44-193">否</span><span class="sxs-lookup"><span data-stu-id="81b44-193">False</span></span>                               |
| <span data-ttu-id="81b44-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81b44-194">Is-Single-Valued</span></span>       | <span data-ttu-id="81b44-195">否</span><span class="sxs-lookup"><span data-stu-id="81b44-195">False</span></span>                               |
| <span data-ttu-id="81b44-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81b44-196">Is Indexed</span></span>             | <span data-ttu-id="81b44-197">否</span><span class="sxs-lookup"><span data-stu-id="81b44-197">False</span></span>                               |
| <span data-ttu-id="81b44-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81b44-198">In Global Catalog</span></span>      | <span data-ttu-id="81b44-199">對</span><span class="sxs-lookup"><span data-stu-id="81b44-199">True</span></span>                                |
| <span data-ttu-id="81b44-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81b44-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="81b44-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81b44-201">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="81b44-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81b44-202">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="81b44-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81b44-203">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="81b44-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-204">Search-Flags</span></span>           | <span data-ttu-id="81b44-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81b44-205">0x00000000</span></span>                          |
| <span data-ttu-id="81b44-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-206">System-Flags</span></span>           | <span data-ttu-id="81b44-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="81b44-207">0x00000012</span></span>                          |
| <span data-ttu-id="81b44-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81b44-208">Classes used in</span></span>        | [<span data-ttu-id="81b44-209">**Group**</span><span class="sxs-lookup"><span data-stu-id="81b44-209">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="81b44-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="81b44-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="81b44-211">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-211">Entry</span></span> | <span data-ttu-id="81b44-212">值</span><span class="sxs-lookup"><span data-stu-id="81b44-212">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b44-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81b44-213">Link-Id</span></span>                | <span data-ttu-id="81b44-214">2</span><span class="sxs-lookup"><span data-stu-id="81b44-214">2</span></span>                                                                                                                                     |
| <span data-ttu-id="81b44-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-215">MAPI-Id</span></span>                | <span data-ttu-id="81b44-216">0x8009</span><span class="sxs-lookup"><span data-stu-id="81b44-216">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="81b44-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="81b44-217">System-Only</span></span>            | <span data-ttu-id="81b44-218">否</span><span class="sxs-lookup"><span data-stu-id="81b44-218">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81b44-219">Is-Single-Valued</span></span>       | <span data-ttu-id="81b44-220">否</span><span class="sxs-lookup"><span data-stu-id="81b44-220">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81b44-221">Is Indexed</span></span>             | <span data-ttu-id="81b44-222">否</span><span class="sxs-lookup"><span data-stu-id="81b44-222">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81b44-223">In Global Catalog</span></span>      | <span data-ttu-id="81b44-224">對</span><span class="sxs-lookup"><span data-stu-id="81b44-224">True</span></span>                                                                                                                                  |
| <span data-ttu-id="81b44-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81b44-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="81b44-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81b44-226">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="81b44-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81b44-227">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81b44-228">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-229">Search-Flags</span></span>           | <span data-ttu-id="81b44-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81b44-230">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-231">System-Flags</span></span>           | <span data-ttu-id="81b44-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="81b44-232">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81b44-233">Classes used in</span></span>        | [<span data-ttu-id="81b44-234">**Group**</span><span class="sxs-lookup"><span data-stu-id="81b44-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="81b44-235">**名稱群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-235">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="81b44-236">**MSMQ 群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-236">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="81b44-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81b44-237">Windows Server 2008</span></span>



| <span data-ttu-id="81b44-238">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-238">Entry</span></span> | <span data-ttu-id="81b44-239">值</span><span class="sxs-lookup"><span data-stu-id="81b44-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b44-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81b44-240">Link-Id</span></span>                | <span data-ttu-id="81b44-241">2</span><span class="sxs-lookup"><span data-stu-id="81b44-241">2</span></span>                                                                                                                                     |
| <span data-ttu-id="81b44-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-242">MAPI-Id</span></span>                | <span data-ttu-id="81b44-243">0x8009</span><span class="sxs-lookup"><span data-stu-id="81b44-243">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="81b44-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="81b44-244">System-Only</span></span>            | <span data-ttu-id="81b44-245">否</span><span class="sxs-lookup"><span data-stu-id="81b44-245">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81b44-246">Is-Single-Valued</span></span>       | <span data-ttu-id="81b44-247">否</span><span class="sxs-lookup"><span data-stu-id="81b44-247">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81b44-248">Is Indexed</span></span>             | <span data-ttu-id="81b44-249">否</span><span class="sxs-lookup"><span data-stu-id="81b44-249">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81b44-250">In Global Catalog</span></span>      | <span data-ttu-id="81b44-251">對</span><span class="sxs-lookup"><span data-stu-id="81b44-251">True</span></span>                                                                                                                                  |
| <span data-ttu-id="81b44-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81b44-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="81b44-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81b44-253">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="81b44-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81b44-254">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81b44-255">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-256">Search-Flags</span></span>           | <span data-ttu-id="81b44-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81b44-257">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-258">System-Flags</span></span>           | <span data-ttu-id="81b44-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="81b44-259">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81b44-260">Classes used in</span></span>        | [<span data-ttu-id="81b44-261">**Group**</span><span class="sxs-lookup"><span data-stu-id="81b44-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="81b44-262">**名稱群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-262">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="81b44-263">**MSMQ 群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-263">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="81b44-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81b44-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="81b44-265">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-265">Entry</span></span> | <span data-ttu-id="81b44-266">值</span><span class="sxs-lookup"><span data-stu-id="81b44-266">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b44-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81b44-267">Link-Id</span></span>                | <span data-ttu-id="81b44-268">2</span><span class="sxs-lookup"><span data-stu-id="81b44-268">2</span></span>                                                                                                                                     |
| <span data-ttu-id="81b44-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-269">MAPI-Id</span></span>                | <span data-ttu-id="81b44-270">0x8009</span><span class="sxs-lookup"><span data-stu-id="81b44-270">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="81b44-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="81b44-271">System-Only</span></span>            | <span data-ttu-id="81b44-272">否</span><span class="sxs-lookup"><span data-stu-id="81b44-272">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-273">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81b44-273">Is-Single-Valued</span></span>       | <span data-ttu-id="81b44-274">否</span><span class="sxs-lookup"><span data-stu-id="81b44-274">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-275">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81b44-275">Is Indexed</span></span>             | <span data-ttu-id="81b44-276">否</span><span class="sxs-lookup"><span data-stu-id="81b44-276">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-277">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81b44-277">In Global Catalog</span></span>      | <span data-ttu-id="81b44-278">對</span><span class="sxs-lookup"><span data-stu-id="81b44-278">True</span></span>                                                                                                                                  |
| <span data-ttu-id="81b44-279">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81b44-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="81b44-280">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81b44-280">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="81b44-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81b44-281">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81b44-282">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-283">Search-Flags</span></span>           | <span data-ttu-id="81b44-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81b44-284">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-285">System-Flags</span></span>           | <span data-ttu-id="81b44-286">0x00000012</span><span class="sxs-lookup"><span data-stu-id="81b44-286">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81b44-287">Classes used in</span></span>        | [<span data-ttu-id="81b44-288">**Group**</span><span class="sxs-lookup"><span data-stu-id="81b44-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="81b44-289">**名稱群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-289">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="81b44-290">**MSMQ 群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-290">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="81b44-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81b44-291">Windows Server 2012</span></span>



| <span data-ttu-id="81b44-292">進入</span><span class="sxs-lookup"><span data-stu-id="81b44-292">Entry</span></span> | <span data-ttu-id="81b44-293">值</span><span class="sxs-lookup"><span data-stu-id="81b44-293">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b44-294">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81b44-294">Link-Id</span></span>                | <span data-ttu-id="81b44-295">2</span><span class="sxs-lookup"><span data-stu-id="81b44-295">2</span></span>                                                                                                                                     |
| <span data-ttu-id="81b44-296">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81b44-296">MAPI-Id</span></span>                | <span data-ttu-id="81b44-297">0x8009</span><span class="sxs-lookup"><span data-stu-id="81b44-297">0x8009</span></span>                                                                                                                                |
| <span data-ttu-id="81b44-298">System-Only</span><span class="sxs-lookup"><span data-stu-id="81b44-298">System-Only</span></span>            | <span data-ttu-id="81b44-299">否</span><span class="sxs-lookup"><span data-stu-id="81b44-299">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-300">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81b44-300">Is-Single-Valued</span></span>       | <span data-ttu-id="81b44-301">否</span><span class="sxs-lookup"><span data-stu-id="81b44-301">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-302">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81b44-302">Is Indexed</span></span>             | <span data-ttu-id="81b44-303">否</span><span class="sxs-lookup"><span data-stu-id="81b44-303">False</span></span>                                                                                                                                 |
| <span data-ttu-id="81b44-304">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81b44-304">In Global Catalog</span></span>      | <span data-ttu-id="81b44-305">對</span><span class="sxs-lookup"><span data-stu-id="81b44-305">True</span></span>                                                                                                                                  |
| <span data-ttu-id="81b44-306">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81b44-306">NT-Security-Descriptor</span></span> | <span data-ttu-id="81b44-307">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81b44-307">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="81b44-308">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81b44-308">Range-Lower</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81b44-309">Range-Upper</span></span>            | \-                                                                                                                                    |
| <span data-ttu-id="81b44-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-310">Search-Flags</span></span>           | <span data-ttu-id="81b44-311">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81b44-311">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81b44-312">System-Flags</span></span>           | <span data-ttu-id="81b44-313">0x00000012</span><span class="sxs-lookup"><span data-stu-id="81b44-313">0x00000012</span></span>                                                                                                                            |
| <span data-ttu-id="81b44-314">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81b44-314">Classes used in</span></span>        | [<span data-ttu-id="81b44-315">**Group**</span><span class="sxs-lookup"><span data-stu-id="81b44-315">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="81b44-316">**名稱群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-316">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="81b44-317">**MSMQ 群組**</span><span class="sxs-lookup"><span data-stu-id="81b44-317">**MSMQ-Group**</span></span>](c-msmq-group.md)<br/> |



 

 





