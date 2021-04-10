---
title: ms DS-Az-LDAP-查詢屬性
description: 定義 LDAP 查詢的字串， (最大長度 4096) ，以決定使用者物件對群組的成員資格。
ms.assetid: e24d4c50-2153-49a6-8aef-4872ccaab13e
ms.tgt_platform: multiple
keywords:
- ms DS-Az-LDAP-查詢屬性 AD 架構
- AzLDAPQuery 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-LDAP-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1f6c21d5ed28a9d2419b16c6ce7986f3250488
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107843"
---
# <a name="ms-ds-az-ldap-query-attribute"></a><span data-ttu-id="b1728-105">ms DS-Az-LDAP-查詢屬性</span><span class="sxs-lookup"><span data-stu-id="b1728-105">ms-DS-Az-LDAP-Query attribute</span></span>

<span data-ttu-id="b1728-106">定義 LDAP 查詢的字串， (最大長度 4096) ，以決定使用者物件對群組的成員資格。</span><span class="sxs-lookup"><span data-stu-id="b1728-106">A string that defines the LDAP query (max length 4096) which determines the membership of a user object to the group.</span></span>



| <span data-ttu-id="b1728-107">進入</span><span class="sxs-lookup"><span data-stu-id="b1728-107">Entry</span></span> | <span data-ttu-id="b1728-108">值</span><span class="sxs-lookup"><span data-stu-id="b1728-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b1728-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1728-109">CN</span></span>                | <span data-ttu-id="b1728-110">ms DS-Az-LDAP-查詢</span><span class="sxs-lookup"><span data-stu-id="b1728-110">ms-DS-Az-LDAP-Query</span></span>                         |
| <span data-ttu-id="b1728-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b1728-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1728-112">AzLDAPQuery</span><span class="sxs-lookup"><span data-stu-id="b1728-112">msDS-AzLDAPQuery</span></span>                            |
| <span data-ttu-id="b1728-113">大小</span><span class="sxs-lookup"><span data-stu-id="b1728-113">Size</span></span>              | <span data-ttu-id="b1728-114">4096個字元</span><span class="sxs-lookup"><span data-stu-id="b1728-114">4096 characters</span></span>                             |
| <span data-ttu-id="b1728-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b1728-115">Update Privilege</span></span>  | <span data-ttu-id="b1728-116">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="b1728-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="b1728-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b1728-117">Update Frequency</span></span>  | <span data-ttu-id="b1728-118">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="b1728-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="b1728-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1728-119">Attribute-Id</span></span>      | <span data-ttu-id="b1728-120">1.2.840.113556.1.4.1792</span><span class="sxs-lookup"><span data-stu-id="b1728-120">1.2.840.113556.1.4.1792</span></span>                     |
| <span data-ttu-id="b1728-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b1728-121">System-Id-Guid</span></span>    | <span data-ttu-id="b1728-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span><span class="sxs-lookup"><span data-stu-id="b1728-122">5e53368b-fc94-45c8-9d7d-daf31ee7112d</span></span>        |
| <span data-ttu-id="b1728-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1728-123">Syntax</span></span>            | [<span data-ttu-id="b1728-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b1728-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b1728-125">實作</span><span class="sxs-lookup"><span data-stu-id="b1728-125">Implementations</span></span>

-   [<span data-ttu-id="b1728-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1728-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1728-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1728-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1728-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1728-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1728-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1728-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1728-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1728-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b1728-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1728-131">Windows Server 2003</span></span>



| <span data-ttu-id="b1728-132">進入</span><span class="sxs-lookup"><span data-stu-id="b1728-132">Entry</span></span> | <span data-ttu-id="b1728-133">值</span><span class="sxs-lookup"><span data-stu-id="b1728-133">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b1728-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1728-134">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1728-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1728-136">System-Only</span></span>            | <span data-ttu-id="b1728-137">否</span><span class="sxs-lookup"><span data-stu-id="b1728-137">False</span></span>                               |
| <span data-ttu-id="b1728-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1728-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b1728-139">對</span><span class="sxs-lookup"><span data-stu-id="b1728-139">True</span></span>                                |
| <span data-ttu-id="b1728-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1728-140">Is Indexed</span></span>             | <span data-ttu-id="b1728-141">否</span><span class="sxs-lookup"><span data-stu-id="b1728-141">False</span></span>                               |
| <span data-ttu-id="b1728-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1728-142">In Global Catalog</span></span>      | <span data-ttu-id="b1728-143">否</span><span class="sxs-lookup"><span data-stu-id="b1728-143">False</span></span>                               |
| <span data-ttu-id="b1728-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1728-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1728-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1728-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b1728-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1728-146">Range-Lower</span></span>            | <span data-ttu-id="b1728-147">0</span><span class="sxs-lookup"><span data-stu-id="b1728-147">0</span></span>                                   |
| <span data-ttu-id="b1728-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1728-148">Range-Upper</span></span>            | <span data-ttu-id="b1728-149">4096</span><span class="sxs-lookup"><span data-stu-id="b1728-149">4096</span></span>                                |
| <span data-ttu-id="b1728-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-150">Search-Flags</span></span>           | <span data-ttu-id="b1728-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1728-151">0x00000000</span></span>                          |
| <span data-ttu-id="b1728-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-152">System-Flags</span></span>           | <span data-ttu-id="b1728-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1728-153">0x00000010</span></span>                          |
| <span data-ttu-id="b1728-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1728-154">Classes used in</span></span>        | [<span data-ttu-id="b1728-155">**Group**</span><span class="sxs-lookup"><span data-stu-id="b1728-155">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1728-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1728-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1728-157">進入</span><span class="sxs-lookup"><span data-stu-id="b1728-157">Entry</span></span> | <span data-ttu-id="b1728-158">值</span><span class="sxs-lookup"><span data-stu-id="b1728-158">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b1728-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1728-159">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1728-160">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1728-161">System-Only</span></span>            | <span data-ttu-id="b1728-162">否</span><span class="sxs-lookup"><span data-stu-id="b1728-162">False</span></span>                               |
| <span data-ttu-id="b1728-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1728-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b1728-164">對</span><span class="sxs-lookup"><span data-stu-id="b1728-164">True</span></span>                                |
| <span data-ttu-id="b1728-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1728-165">Is Indexed</span></span>             | <span data-ttu-id="b1728-166">否</span><span class="sxs-lookup"><span data-stu-id="b1728-166">False</span></span>                               |
| <span data-ttu-id="b1728-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1728-167">In Global Catalog</span></span>      | <span data-ttu-id="b1728-168">否</span><span class="sxs-lookup"><span data-stu-id="b1728-168">False</span></span>                               |
| <span data-ttu-id="b1728-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1728-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1728-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1728-170">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b1728-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1728-171">Range-Lower</span></span>            | <span data-ttu-id="b1728-172">0</span><span class="sxs-lookup"><span data-stu-id="b1728-172">0</span></span>                                   |
| <span data-ttu-id="b1728-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1728-173">Range-Upper</span></span>            | <span data-ttu-id="b1728-174">4096</span><span class="sxs-lookup"><span data-stu-id="b1728-174">4096</span></span>                                |
| <span data-ttu-id="b1728-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-175">Search-Flags</span></span>           | <span data-ttu-id="b1728-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1728-176">0x00000000</span></span>                          |
| <span data-ttu-id="b1728-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-177">System-Flags</span></span>           | <span data-ttu-id="b1728-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1728-178">0x00000010</span></span>                          |
| <span data-ttu-id="b1728-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1728-179">Classes used in</span></span>        | [<span data-ttu-id="b1728-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="b1728-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1728-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1728-181">Windows Server 2008</span></span>



| <span data-ttu-id="b1728-182">進入</span><span class="sxs-lookup"><span data-stu-id="b1728-182">Entry</span></span> | <span data-ttu-id="b1728-183">值</span><span class="sxs-lookup"><span data-stu-id="b1728-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b1728-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1728-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1728-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1728-186">System-Only</span></span>            | <span data-ttu-id="b1728-187">否</span><span class="sxs-lookup"><span data-stu-id="b1728-187">False</span></span>                               |
| <span data-ttu-id="b1728-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1728-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b1728-189">對</span><span class="sxs-lookup"><span data-stu-id="b1728-189">True</span></span>                                |
| <span data-ttu-id="b1728-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1728-190">Is Indexed</span></span>             | <span data-ttu-id="b1728-191">否</span><span class="sxs-lookup"><span data-stu-id="b1728-191">False</span></span>                               |
| <span data-ttu-id="b1728-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1728-192">In Global Catalog</span></span>      | <span data-ttu-id="b1728-193">否</span><span class="sxs-lookup"><span data-stu-id="b1728-193">False</span></span>                               |
| <span data-ttu-id="b1728-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1728-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1728-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1728-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b1728-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1728-196">Range-Lower</span></span>            | <span data-ttu-id="b1728-197">0</span><span class="sxs-lookup"><span data-stu-id="b1728-197">0</span></span>                                   |
| <span data-ttu-id="b1728-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1728-198">Range-Upper</span></span>            | <span data-ttu-id="b1728-199">4096</span><span class="sxs-lookup"><span data-stu-id="b1728-199">4096</span></span>                                |
| <span data-ttu-id="b1728-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-200">Search-Flags</span></span>           | <span data-ttu-id="b1728-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1728-201">0x00000000</span></span>                          |
| <span data-ttu-id="b1728-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-202">System-Flags</span></span>           | <span data-ttu-id="b1728-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1728-203">0x00000010</span></span>                          |
| <span data-ttu-id="b1728-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1728-204">Classes used in</span></span>        | [<span data-ttu-id="b1728-205">**Group**</span><span class="sxs-lookup"><span data-stu-id="b1728-205">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1728-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1728-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1728-207">進入</span><span class="sxs-lookup"><span data-stu-id="b1728-207">Entry</span></span> | <span data-ttu-id="b1728-208">值</span><span class="sxs-lookup"><span data-stu-id="b1728-208">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b1728-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1728-209">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1728-210">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1728-211">System-Only</span></span>            | <span data-ttu-id="b1728-212">否</span><span class="sxs-lookup"><span data-stu-id="b1728-212">False</span></span>                               |
| <span data-ttu-id="b1728-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1728-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b1728-214">對</span><span class="sxs-lookup"><span data-stu-id="b1728-214">True</span></span>                                |
| <span data-ttu-id="b1728-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1728-215">Is Indexed</span></span>             | <span data-ttu-id="b1728-216">否</span><span class="sxs-lookup"><span data-stu-id="b1728-216">False</span></span>                               |
| <span data-ttu-id="b1728-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1728-217">In Global Catalog</span></span>      | <span data-ttu-id="b1728-218">否</span><span class="sxs-lookup"><span data-stu-id="b1728-218">False</span></span>                               |
| <span data-ttu-id="b1728-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1728-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1728-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1728-220">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b1728-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1728-221">Range-Lower</span></span>            | <span data-ttu-id="b1728-222">0</span><span class="sxs-lookup"><span data-stu-id="b1728-222">0</span></span>                                   |
| <span data-ttu-id="b1728-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1728-223">Range-Upper</span></span>            | <span data-ttu-id="b1728-224">4096</span><span class="sxs-lookup"><span data-stu-id="b1728-224">4096</span></span>                                |
| <span data-ttu-id="b1728-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-225">Search-Flags</span></span>           | <span data-ttu-id="b1728-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1728-226">0x00000000</span></span>                          |
| <span data-ttu-id="b1728-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-227">System-Flags</span></span>           | <span data-ttu-id="b1728-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1728-228">0x00000010</span></span>                          |
| <span data-ttu-id="b1728-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1728-229">Classes used in</span></span>        | [<span data-ttu-id="b1728-230">**Group**</span><span class="sxs-lookup"><span data-stu-id="b1728-230">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1728-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1728-231">Windows Server 2012</span></span>



| <span data-ttu-id="b1728-232">進入</span><span class="sxs-lookup"><span data-stu-id="b1728-232">Entry</span></span> | <span data-ttu-id="b1728-233">值</span><span class="sxs-lookup"><span data-stu-id="b1728-233">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="b1728-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b1728-234">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1728-235">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="b1728-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1728-236">System-Only</span></span>            | <span data-ttu-id="b1728-237">否</span><span class="sxs-lookup"><span data-stu-id="b1728-237">False</span></span>                               |
| <span data-ttu-id="b1728-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b1728-238">Is-Single-Valued</span></span>       | <span data-ttu-id="b1728-239">對</span><span class="sxs-lookup"><span data-stu-id="b1728-239">True</span></span>                                |
| <span data-ttu-id="b1728-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b1728-240">Is Indexed</span></span>             | <span data-ttu-id="b1728-241">否</span><span class="sxs-lookup"><span data-stu-id="b1728-241">False</span></span>                               |
| <span data-ttu-id="b1728-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b1728-242">In Global Catalog</span></span>      | <span data-ttu-id="b1728-243">否</span><span class="sxs-lookup"><span data-stu-id="b1728-243">False</span></span>                               |
| <span data-ttu-id="b1728-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b1728-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1728-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b1728-245">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="b1728-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1728-246">Range-Lower</span></span>            | <span data-ttu-id="b1728-247">0</span><span class="sxs-lookup"><span data-stu-id="b1728-247">0</span></span>                                   |
| <span data-ttu-id="b1728-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1728-248">Range-Upper</span></span>            | <span data-ttu-id="b1728-249">4096</span><span class="sxs-lookup"><span data-stu-id="b1728-249">4096</span></span>                                |
| <span data-ttu-id="b1728-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-250">Search-Flags</span></span>           | <span data-ttu-id="b1728-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1728-251">0x00000000</span></span>                          |
| <span data-ttu-id="b1728-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1728-252">System-Flags</span></span>           | <span data-ttu-id="b1728-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1728-253">0x00000010</span></span>                          |
| <span data-ttu-id="b1728-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b1728-254">Classes used in</span></span>        | [<span data-ttu-id="b1728-255">**Group**</span><span class="sxs-lookup"><span data-stu-id="b1728-255">**Group**</span></span>](c-group.md)<br/> |



 

 





