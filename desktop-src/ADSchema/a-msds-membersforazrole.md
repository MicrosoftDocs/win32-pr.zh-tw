---
title: ms DS-成員--Az-Role 屬性
description: 連結至 Az 角色的成員應用程式群組或使用者清單。
ms.assetid: c1234443-fd25-4ed8-a8ee-9853810ebe7d
ms.tgt_platform: multiple
keywords:
- ms DS-成員--Az-Role attribute AD Schema
- MembersForAzRole 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Members-For-Az-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b19203e5c44d0389e64531867444d1bb2865196
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467354"
---
# <a name="ms-ds-members-for-az-role-attribute"></a><span data-ttu-id="dfa44-105">ms DS-成員--Az-Role 屬性</span><span class="sxs-lookup"><span data-stu-id="dfa44-105">ms-DS-Members-For-Az-Role attribute</span></span>

<span data-ttu-id="dfa44-106">連結至 Az 角色的成員應用程式群組或使用者清單。</span><span class="sxs-lookup"><span data-stu-id="dfa44-106">List of member application groups or users linked to Az-Role.</span></span>



| <span data-ttu-id="dfa44-107">進入</span><span class="sxs-lookup"><span data-stu-id="dfa44-107">Entry</span></span> | <span data-ttu-id="dfa44-108">值</span><span class="sxs-lookup"><span data-stu-id="dfa44-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="dfa44-109">CN</span><span class="sxs-lookup"><span data-stu-id="dfa44-109">CN</span></span>                | <span data-ttu-id="dfa44-110">ms DS-成員--Az-Role</span><span class="sxs-lookup"><span data-stu-id="dfa44-110">ms-DS-Members-For-Az-Role</span></span>               |
| <span data-ttu-id="dfa44-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dfa44-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dfa44-112">MembersForAzRole</span><span class="sxs-lookup"><span data-stu-id="dfa44-112">msDS-MembersForAzRole</span></span>                   |
| <span data-ttu-id="dfa44-113">大小</span><span class="sxs-lookup"><span data-stu-id="dfa44-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="dfa44-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dfa44-114">Update Privilege</span></span>  | <span data-ttu-id="dfa44-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="dfa44-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="dfa44-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dfa44-116">Update Frequency</span></span>  | <span data-ttu-id="dfa44-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="dfa44-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="dfa44-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dfa44-118">Attribute-Id</span></span>      | <span data-ttu-id="dfa44-119">1.2.840.113556.1.4.1806</span><span class="sxs-lookup"><span data-stu-id="dfa44-119">1.2.840.113556.1.4.1806</span></span>                 |
| <span data-ttu-id="dfa44-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dfa44-120">System-Id-Guid</span></span>    | <span data-ttu-id="dfa44-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span><span class="sxs-lookup"><span data-stu-id="dfa44-121">cbf7e6cd-85a4-4314-8939-8bfe80597835</span></span>    |
| <span data-ttu-id="dfa44-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfa44-122">Syntax</span></span>            | [<span data-ttu-id="dfa44-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="dfa44-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="dfa44-124">實作</span><span class="sxs-lookup"><span data-stu-id="dfa44-124">Implementations</span></span>

-   [<span data-ttu-id="dfa44-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dfa44-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dfa44-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dfa44-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dfa44-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dfa44-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dfa44-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dfa44-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dfa44-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dfa44-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="dfa44-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfa44-130">Windows Server 2003</span></span>



| <span data-ttu-id="dfa44-131">進入</span><span class="sxs-lookup"><span data-stu-id="dfa44-131">Entry</span></span> | <span data-ttu-id="dfa44-132">值</span><span class="sxs-lookup"><span data-stu-id="dfa44-132">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="dfa44-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dfa44-133">Link-Id</span></span>                | <span data-ttu-id="dfa44-134">2016</span><span class="sxs-lookup"><span data-stu-id="dfa44-134">2016</span></span>                                              |
| <span data-ttu-id="dfa44-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfa44-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="dfa44-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfa44-136">System-Only</span></span>            | <span data-ttu-id="dfa44-137">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-137">False</span></span>                                             |
| <span data-ttu-id="dfa44-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dfa44-138">Is-Single-Valued</span></span>       | <span data-ttu-id="dfa44-139">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-139">False</span></span>                                             |
| <span data-ttu-id="dfa44-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dfa44-140">Is Indexed</span></span>             | <span data-ttu-id="dfa44-141">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-141">False</span></span>                                             |
| <span data-ttu-id="dfa44-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dfa44-142">In Global Catalog</span></span>      | <span data-ttu-id="dfa44-143">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-143">False</span></span>                                             |
| <span data-ttu-id="dfa44-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dfa44-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfa44-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dfa44-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="dfa44-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfa44-146">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfa44-147">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-148">Search-Flags</span></span>           | <span data-ttu-id="dfa44-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfa44-149">0x00000000</span></span>                                        |
| <span data-ttu-id="dfa44-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-150">System-Flags</span></span>           | <span data-ttu-id="dfa44-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfa44-151">0x00000010</span></span>                                        |
| <span data-ttu-id="dfa44-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dfa44-152">Classes used in</span></span>        | [<span data-ttu-id="dfa44-153">**ms DS-Az-Role**</span><span class="sxs-lookup"><span data-stu-id="dfa44-153">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dfa44-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dfa44-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dfa44-155">進入</span><span class="sxs-lookup"><span data-stu-id="dfa44-155">Entry</span></span> | <span data-ttu-id="dfa44-156">值</span><span class="sxs-lookup"><span data-stu-id="dfa44-156">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="dfa44-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dfa44-157">Link-Id</span></span>                | <span data-ttu-id="dfa44-158">2016</span><span class="sxs-lookup"><span data-stu-id="dfa44-158">2016</span></span>                                              |
| <span data-ttu-id="dfa44-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfa44-159">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="dfa44-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfa44-160">System-Only</span></span>            | <span data-ttu-id="dfa44-161">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-161">False</span></span>                                             |
| <span data-ttu-id="dfa44-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dfa44-162">Is-Single-Valued</span></span>       | <span data-ttu-id="dfa44-163">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-163">False</span></span>                                             |
| <span data-ttu-id="dfa44-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dfa44-164">Is Indexed</span></span>             | <span data-ttu-id="dfa44-165">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-165">False</span></span>                                             |
| <span data-ttu-id="dfa44-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dfa44-166">In Global Catalog</span></span>      | <span data-ttu-id="dfa44-167">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-167">False</span></span>                                             |
| <span data-ttu-id="dfa44-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dfa44-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfa44-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dfa44-169">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="dfa44-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfa44-170">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfa44-171">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-172">Search-Flags</span></span>           | <span data-ttu-id="dfa44-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfa44-173">0x00000000</span></span>                                        |
| <span data-ttu-id="dfa44-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-174">System-Flags</span></span>           | <span data-ttu-id="dfa44-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfa44-175">0x00000010</span></span>                                        |
| <span data-ttu-id="dfa44-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dfa44-176">Classes used in</span></span>        | [<span data-ttu-id="dfa44-177">**ms DS-Az-Role**</span><span class="sxs-lookup"><span data-stu-id="dfa44-177">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dfa44-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfa44-178">Windows Server 2008</span></span>



| <span data-ttu-id="dfa44-179">進入</span><span class="sxs-lookup"><span data-stu-id="dfa44-179">Entry</span></span> | <span data-ttu-id="dfa44-180">值</span><span class="sxs-lookup"><span data-stu-id="dfa44-180">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="dfa44-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dfa44-181">Link-Id</span></span>                | <span data-ttu-id="dfa44-182">2016</span><span class="sxs-lookup"><span data-stu-id="dfa44-182">2016</span></span>                                              |
| <span data-ttu-id="dfa44-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfa44-183">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="dfa44-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfa44-184">System-Only</span></span>            | <span data-ttu-id="dfa44-185">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-185">False</span></span>                                             |
| <span data-ttu-id="dfa44-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dfa44-186">Is-Single-Valued</span></span>       | <span data-ttu-id="dfa44-187">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-187">False</span></span>                                             |
| <span data-ttu-id="dfa44-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dfa44-188">Is Indexed</span></span>             | <span data-ttu-id="dfa44-189">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-189">False</span></span>                                             |
| <span data-ttu-id="dfa44-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dfa44-190">In Global Catalog</span></span>      | <span data-ttu-id="dfa44-191">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-191">False</span></span>                                             |
| <span data-ttu-id="dfa44-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dfa44-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfa44-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dfa44-193">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="dfa44-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfa44-194">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfa44-195">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-196">Search-Flags</span></span>           | <span data-ttu-id="dfa44-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfa44-197">0x00000000</span></span>                                        |
| <span data-ttu-id="dfa44-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-198">System-Flags</span></span>           | <span data-ttu-id="dfa44-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfa44-199">0x00000010</span></span>                                        |
| <span data-ttu-id="dfa44-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dfa44-200">Classes used in</span></span>        | [<span data-ttu-id="dfa44-201">**ms DS-Az-Role**</span><span class="sxs-lookup"><span data-stu-id="dfa44-201">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dfa44-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfa44-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dfa44-203">進入</span><span class="sxs-lookup"><span data-stu-id="dfa44-203">Entry</span></span> | <span data-ttu-id="dfa44-204">值</span><span class="sxs-lookup"><span data-stu-id="dfa44-204">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="dfa44-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dfa44-205">Link-Id</span></span>                | <span data-ttu-id="dfa44-206">2016</span><span class="sxs-lookup"><span data-stu-id="dfa44-206">2016</span></span>                                              |
| <span data-ttu-id="dfa44-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfa44-207">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="dfa44-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfa44-208">System-Only</span></span>            | <span data-ttu-id="dfa44-209">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-209">False</span></span>                                             |
| <span data-ttu-id="dfa44-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dfa44-210">Is-Single-Valued</span></span>       | <span data-ttu-id="dfa44-211">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-211">False</span></span>                                             |
| <span data-ttu-id="dfa44-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dfa44-212">Is Indexed</span></span>             | <span data-ttu-id="dfa44-213">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-213">False</span></span>                                             |
| <span data-ttu-id="dfa44-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dfa44-214">In Global Catalog</span></span>      | <span data-ttu-id="dfa44-215">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-215">False</span></span>                                             |
| <span data-ttu-id="dfa44-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dfa44-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfa44-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dfa44-217">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="dfa44-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfa44-218">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfa44-219">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-220">Search-Flags</span></span>           | <span data-ttu-id="dfa44-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfa44-221">0x00000000</span></span>                                        |
| <span data-ttu-id="dfa44-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-222">System-Flags</span></span>           | <span data-ttu-id="dfa44-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfa44-223">0x00000010</span></span>                                        |
| <span data-ttu-id="dfa44-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dfa44-224">Classes used in</span></span>        | [<span data-ttu-id="dfa44-225">**ms DS-Az-Role**</span><span class="sxs-lookup"><span data-stu-id="dfa44-225">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dfa44-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfa44-226">Windows Server 2012</span></span>



| <span data-ttu-id="dfa44-227">進入</span><span class="sxs-lookup"><span data-stu-id="dfa44-227">Entry</span></span> | <span data-ttu-id="dfa44-228">值</span><span class="sxs-lookup"><span data-stu-id="dfa44-228">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="dfa44-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dfa44-229">Link-Id</span></span>                | <span data-ttu-id="dfa44-230">2016</span><span class="sxs-lookup"><span data-stu-id="dfa44-230">2016</span></span>                                              |
| <span data-ttu-id="dfa44-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfa44-231">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="dfa44-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfa44-232">System-Only</span></span>            | <span data-ttu-id="dfa44-233">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-233">False</span></span>                                             |
| <span data-ttu-id="dfa44-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dfa44-234">Is-Single-Valued</span></span>       | <span data-ttu-id="dfa44-235">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-235">False</span></span>                                             |
| <span data-ttu-id="dfa44-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dfa44-236">Is Indexed</span></span>             | <span data-ttu-id="dfa44-237">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-237">False</span></span>                                             |
| <span data-ttu-id="dfa44-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dfa44-238">In Global Catalog</span></span>      | <span data-ttu-id="dfa44-239">否</span><span class="sxs-lookup"><span data-stu-id="dfa44-239">False</span></span>                                             |
| <span data-ttu-id="dfa44-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dfa44-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfa44-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dfa44-241">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="dfa44-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfa44-242">Range-Lower</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfa44-243">Range-Upper</span></span>            | \-                                                |
| <span data-ttu-id="dfa44-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-244">Search-Flags</span></span>           | <span data-ttu-id="dfa44-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfa44-245">0x00000000</span></span>                                        |
| <span data-ttu-id="dfa44-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfa44-246">System-Flags</span></span>           | <span data-ttu-id="dfa44-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfa44-247">0x00000010</span></span>                                        |
| <span data-ttu-id="dfa44-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dfa44-248">Classes used in</span></span>        | [<span data-ttu-id="dfa44-249">**ms DS-Az-Role**</span><span class="sxs-lookup"><span data-stu-id="dfa44-249">**ms-DS-Az-Role**</span></span>](c-msds-azrole.md)<br/> |



 

 





