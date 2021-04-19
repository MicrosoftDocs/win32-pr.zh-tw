---
title: 最大值-續約-存留期屬性
description: 這個屬性會決定使用者的票證授權票證 (TGT) 可針對 Kerberos 驗證進行更新的時間週期（以天為單位）。 預設值是預設網域中的7天群組原則物件 (GPO) 。
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- 最大-更新-存留期屬性 AD 架構
- maxRenewAge 屬性 AD 架構
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966557"
---
# <a name="max-renew-age-attribute"></a><span data-ttu-id="5316f-106">最大值-續約-存留期屬性</span><span class="sxs-lookup"><span data-stu-id="5316f-106">Max-Renew-Age attribute</span></span>

<span data-ttu-id="5316f-107">這個屬性會決定使用者的票證授權票證 (TGT) 可針對 Kerberos 驗證進行更新的時間週期（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="5316f-107">This attribute determines the time period, in days, during which a user's ticket-granting ticket (TGT) can be renewed for purposes of Kerberos authentication.</span></span> <span data-ttu-id="5316f-108">預設值是預設網域中的7天群組原則物件 (GPO) 。</span><span class="sxs-lookup"><span data-stu-id="5316f-108">The default setting is 7 days in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="5316f-109">進入</span><span class="sxs-lookup"><span data-stu-id="5316f-109">Entry</span></span> | <span data-ttu-id="5316f-110">值</span><span class="sxs-lookup"><span data-stu-id="5316f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5316f-111">CN</span><span class="sxs-lookup"><span data-stu-id="5316f-111">CN</span></span>                | <span data-ttu-id="5316f-112">最大續約-期限</span><span class="sxs-lookup"><span data-stu-id="5316f-112">Max-Renew-Age</span></span>                        |
| <span data-ttu-id="5316f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5316f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5316f-114">maxRenewAge</span><span class="sxs-lookup"><span data-stu-id="5316f-114">maxRenewAge</span></span>                          |
| <span data-ttu-id="5316f-115">大小</span><span class="sxs-lookup"><span data-stu-id="5316f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="5316f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5316f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5316f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5316f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5316f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5316f-118">Attribute-Id</span></span>      | <span data-ttu-id="5316f-119">1.2.840.113556.1.4.75</span><span class="sxs-lookup"><span data-stu-id="5316f-119">1.2.840.113556.1.4.75</span></span>                |
| <span data-ttu-id="5316f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5316f-120">System-Id-Guid</span></span>    | <span data-ttu-id="5316f-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5316f-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5316f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5316f-122">Syntax</span></span>            | [<span data-ttu-id="5316f-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="5316f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5316f-124">實作</span><span class="sxs-lookup"><span data-stu-id="5316f-124">Implementations</span></span>

-   [<span data-ttu-id="5316f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5316f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5316f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5316f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5316f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5316f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5316f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5316f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5316f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5316f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5316f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5316f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5316f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5316f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5316f-132">進入</span><span class="sxs-lookup"><span data-stu-id="5316f-132">Entry</span></span> | <span data-ttu-id="5316f-133">值</span><span class="sxs-lookup"><span data-stu-id="5316f-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5316f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5316f-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5316f-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5316f-136">System-Only</span></span>            | <span data-ttu-id="5316f-137">否</span><span class="sxs-lookup"><span data-stu-id="5316f-137">False</span></span>                                              |
| <span data-ttu-id="5316f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5316f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5316f-139">對</span><span class="sxs-lookup"><span data-stu-id="5316f-139">True</span></span>                                               |
| <span data-ttu-id="5316f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5316f-140">Is Indexed</span></span>             | <span data-ttu-id="5316f-141">否</span><span class="sxs-lookup"><span data-stu-id="5316f-141">False</span></span>                                              |
| <span data-ttu-id="5316f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5316f-142">In Global Catalog</span></span>      | <span data-ttu-id="5316f-143">否</span><span class="sxs-lookup"><span data-stu-id="5316f-143">False</span></span>                                              |
| <span data-ttu-id="5316f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5316f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5316f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5316f-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5316f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5316f-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5316f-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-148">Search-Flags</span></span>           | <span data-ttu-id="5316f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5316f-149">0x00000000</span></span>                                         |
| <span data-ttu-id="5316f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-150">System-Flags</span></span>           | <span data-ttu-id="5316f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5316f-151">0x00000010</span></span>                                         |
| <span data-ttu-id="5316f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5316f-152">Classes used in</span></span>        | [<span data-ttu-id="5316f-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5316f-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5316f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5316f-154">Windows Server 2003</span></span>



| <span data-ttu-id="5316f-155">進入</span><span class="sxs-lookup"><span data-stu-id="5316f-155">Entry</span></span> | <span data-ttu-id="5316f-156">值</span><span class="sxs-lookup"><span data-stu-id="5316f-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5316f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5316f-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5316f-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5316f-159">System-Only</span></span>            | <span data-ttu-id="5316f-160">否</span><span class="sxs-lookup"><span data-stu-id="5316f-160">False</span></span>                                              |
| <span data-ttu-id="5316f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5316f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5316f-162">對</span><span class="sxs-lookup"><span data-stu-id="5316f-162">True</span></span>                                               |
| <span data-ttu-id="5316f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5316f-163">Is Indexed</span></span>             | <span data-ttu-id="5316f-164">否</span><span class="sxs-lookup"><span data-stu-id="5316f-164">False</span></span>                                              |
| <span data-ttu-id="5316f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5316f-165">In Global Catalog</span></span>      | <span data-ttu-id="5316f-166">否</span><span class="sxs-lookup"><span data-stu-id="5316f-166">False</span></span>                                              |
| <span data-ttu-id="5316f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5316f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5316f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5316f-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5316f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5316f-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5316f-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-171">Search-Flags</span></span>           | <span data-ttu-id="5316f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5316f-172">0x00000000</span></span>                                         |
| <span data-ttu-id="5316f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-173">System-Flags</span></span>           | <span data-ttu-id="5316f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5316f-174">0x00000010</span></span>                                         |
| <span data-ttu-id="5316f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5316f-175">Classes used in</span></span>        | [<span data-ttu-id="5316f-176">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5316f-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5316f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5316f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5316f-178">進入</span><span class="sxs-lookup"><span data-stu-id="5316f-178">Entry</span></span> | <span data-ttu-id="5316f-179">值</span><span class="sxs-lookup"><span data-stu-id="5316f-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5316f-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5316f-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5316f-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5316f-182">System-Only</span></span>            | <span data-ttu-id="5316f-183">否</span><span class="sxs-lookup"><span data-stu-id="5316f-183">False</span></span>                                              |
| <span data-ttu-id="5316f-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5316f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5316f-185">對</span><span class="sxs-lookup"><span data-stu-id="5316f-185">True</span></span>                                               |
| <span data-ttu-id="5316f-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5316f-186">Is Indexed</span></span>             | <span data-ttu-id="5316f-187">否</span><span class="sxs-lookup"><span data-stu-id="5316f-187">False</span></span>                                              |
| <span data-ttu-id="5316f-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5316f-188">In Global Catalog</span></span>      | <span data-ttu-id="5316f-189">否</span><span class="sxs-lookup"><span data-stu-id="5316f-189">False</span></span>                                              |
| <span data-ttu-id="5316f-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5316f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5316f-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5316f-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5316f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5316f-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5316f-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-194">Search-Flags</span></span>           | <span data-ttu-id="5316f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5316f-195">0x00000000</span></span>                                         |
| <span data-ttu-id="5316f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-196">System-Flags</span></span>           | <span data-ttu-id="5316f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5316f-197">0x00000010</span></span>                                         |
| <span data-ttu-id="5316f-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5316f-198">Classes used in</span></span>        | [<span data-ttu-id="5316f-199">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5316f-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5316f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5316f-200">Windows Server 2008</span></span>



| <span data-ttu-id="5316f-201">進入</span><span class="sxs-lookup"><span data-stu-id="5316f-201">Entry</span></span> | <span data-ttu-id="5316f-202">值</span><span class="sxs-lookup"><span data-stu-id="5316f-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5316f-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5316f-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5316f-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5316f-205">System-Only</span></span>            | <span data-ttu-id="5316f-206">否</span><span class="sxs-lookup"><span data-stu-id="5316f-206">False</span></span>                                              |
| <span data-ttu-id="5316f-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5316f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5316f-208">對</span><span class="sxs-lookup"><span data-stu-id="5316f-208">True</span></span>                                               |
| <span data-ttu-id="5316f-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5316f-209">Is Indexed</span></span>             | <span data-ttu-id="5316f-210">否</span><span class="sxs-lookup"><span data-stu-id="5316f-210">False</span></span>                                              |
| <span data-ttu-id="5316f-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5316f-211">In Global Catalog</span></span>      | <span data-ttu-id="5316f-212">否</span><span class="sxs-lookup"><span data-stu-id="5316f-212">False</span></span>                                              |
| <span data-ttu-id="5316f-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5316f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5316f-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5316f-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5316f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5316f-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5316f-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-217">Search-Flags</span></span>           | <span data-ttu-id="5316f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5316f-218">0x00000000</span></span>                                         |
| <span data-ttu-id="5316f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-219">System-Flags</span></span>           | <span data-ttu-id="5316f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5316f-220">0x00000010</span></span>                                         |
| <span data-ttu-id="5316f-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5316f-221">Classes used in</span></span>        | [<span data-ttu-id="5316f-222">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5316f-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5316f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5316f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5316f-224">進入</span><span class="sxs-lookup"><span data-stu-id="5316f-224">Entry</span></span> | <span data-ttu-id="5316f-225">值</span><span class="sxs-lookup"><span data-stu-id="5316f-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5316f-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5316f-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5316f-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5316f-228">System-Only</span></span>            | <span data-ttu-id="5316f-229">否</span><span class="sxs-lookup"><span data-stu-id="5316f-229">False</span></span>                                              |
| <span data-ttu-id="5316f-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5316f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5316f-231">對</span><span class="sxs-lookup"><span data-stu-id="5316f-231">True</span></span>                                               |
| <span data-ttu-id="5316f-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5316f-232">Is Indexed</span></span>             | <span data-ttu-id="5316f-233">否</span><span class="sxs-lookup"><span data-stu-id="5316f-233">False</span></span>                                              |
| <span data-ttu-id="5316f-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5316f-234">In Global Catalog</span></span>      | <span data-ttu-id="5316f-235">否</span><span class="sxs-lookup"><span data-stu-id="5316f-235">False</span></span>                                              |
| <span data-ttu-id="5316f-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5316f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5316f-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5316f-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5316f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5316f-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5316f-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-240">Search-Flags</span></span>           | <span data-ttu-id="5316f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5316f-241">0x00000000</span></span>                                         |
| <span data-ttu-id="5316f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-242">System-Flags</span></span>           | <span data-ttu-id="5316f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5316f-243">0x00000010</span></span>                                         |
| <span data-ttu-id="5316f-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5316f-244">Classes used in</span></span>        | [<span data-ttu-id="5316f-245">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5316f-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5316f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5316f-246">Windows Server 2012</span></span>



| <span data-ttu-id="5316f-247">進入</span><span class="sxs-lookup"><span data-stu-id="5316f-247">Entry</span></span> | <span data-ttu-id="5316f-248">值</span><span class="sxs-lookup"><span data-stu-id="5316f-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5316f-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5316f-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5316f-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5316f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5316f-251">System-Only</span></span>            | <span data-ttu-id="5316f-252">否</span><span class="sxs-lookup"><span data-stu-id="5316f-252">False</span></span>                                              |
| <span data-ttu-id="5316f-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5316f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5316f-254">對</span><span class="sxs-lookup"><span data-stu-id="5316f-254">True</span></span>                                               |
| <span data-ttu-id="5316f-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5316f-255">Is Indexed</span></span>             | <span data-ttu-id="5316f-256">否</span><span class="sxs-lookup"><span data-stu-id="5316f-256">False</span></span>                                              |
| <span data-ttu-id="5316f-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5316f-257">In Global Catalog</span></span>      | <span data-ttu-id="5316f-258">否</span><span class="sxs-lookup"><span data-stu-id="5316f-258">False</span></span>                                              |
| <span data-ttu-id="5316f-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5316f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5316f-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5316f-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5316f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5316f-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5316f-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5316f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-263">Search-Flags</span></span>           | <span data-ttu-id="5316f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5316f-264">0x00000000</span></span>                                         |
| <span data-ttu-id="5316f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5316f-265">System-Flags</span></span>           | <span data-ttu-id="5316f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5316f-266">0x00000010</span></span>                                         |
| <span data-ttu-id="5316f-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5316f-267">Classes used in</span></span>        | [<span data-ttu-id="5316f-268">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5316f-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





