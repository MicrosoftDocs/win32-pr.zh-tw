---
title: 最大票證-存留期屬性
description: 這個屬性會決定使用者的票證授與票證 (TGT) 可用於 Kerberos 驗證的最大時間量（以小時為單位）。
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- 最大票證-存留期屬性 AD 架構
- maxTicketAge 屬性 AD 架構
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686851"
---
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="54025-105">最大票證-存留期屬性</span><span class="sxs-lookup"><span data-stu-id="54025-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="54025-106">這個屬性會決定使用者的票證授與票證 (TGT) 可用於 Kerberos 驗證的最大時間量（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="54025-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="54025-107">當使用者的 TGT 過期時，必須要求新的 TGT，或必須更新現有的 TGT。</span><span class="sxs-lookup"><span data-stu-id="54025-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="54025-108">根據預設，在預設網域群組原則物件 (GPO) 中，此設定為10小時。</span><span class="sxs-lookup"><span data-stu-id="54025-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="54025-109">進入</span><span class="sxs-lookup"><span data-stu-id="54025-109">Entry</span></span> | <span data-ttu-id="54025-110">值</span><span class="sxs-lookup"><span data-stu-id="54025-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="54025-111">CN</span><span class="sxs-lookup"><span data-stu-id="54025-111">CN</span></span>                | <span data-ttu-id="54025-112">最大票證-存留期</span><span class="sxs-lookup"><span data-stu-id="54025-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="54025-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="54025-113">Ldap-Display-Name</span></span> | <span data-ttu-id="54025-114">maxTicketAge</span><span class="sxs-lookup"><span data-stu-id="54025-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="54025-115">大小</span><span class="sxs-lookup"><span data-stu-id="54025-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="54025-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="54025-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="54025-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="54025-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="54025-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="54025-118">Attribute-Id</span></span>      | <span data-ttu-id="54025-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="54025-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="54025-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="54025-120">System-Id-Guid</span></span>    | <span data-ttu-id="54025-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="54025-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="54025-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="54025-122">Syntax</span></span>            | [<span data-ttu-id="54025-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="54025-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="54025-124">實作</span><span class="sxs-lookup"><span data-stu-id="54025-124">Implementations</span></span>

-   [<span data-ttu-id="54025-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="54025-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="54025-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="54025-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="54025-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="54025-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="54025-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="54025-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="54025-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="54025-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="54025-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="54025-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="54025-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="54025-131">Windows 2000 Server</span></span>



| <span data-ttu-id="54025-132">進入</span><span class="sxs-lookup"><span data-stu-id="54025-132">Entry</span></span> | <span data-ttu-id="54025-133">值</span><span class="sxs-lookup"><span data-stu-id="54025-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="54025-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54025-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54025-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="54025-136">System-Only</span></span>            | <span data-ttu-id="54025-137">否</span><span class="sxs-lookup"><span data-stu-id="54025-137">False</span></span>                                              |
| <span data-ttu-id="54025-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54025-138">Is-Single-Valued</span></span>       | <span data-ttu-id="54025-139">對</span><span class="sxs-lookup"><span data-stu-id="54025-139">True</span></span>                                               |
| <span data-ttu-id="54025-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54025-140">Is Indexed</span></span>             | <span data-ttu-id="54025-141">否</span><span class="sxs-lookup"><span data-stu-id="54025-141">False</span></span>                                              |
| <span data-ttu-id="54025-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54025-142">In Global Catalog</span></span>      | <span data-ttu-id="54025-143">否</span><span class="sxs-lookup"><span data-stu-id="54025-143">False</span></span>                                              |
| <span data-ttu-id="54025-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54025-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="54025-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54025-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="54025-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54025-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="54025-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54025-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="54025-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-148">Search-Flags</span></span>           | <span data-ttu-id="54025-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54025-149">0x00000000</span></span>                                         |
| <span data-ttu-id="54025-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-150">System-Flags</span></span>           | <span data-ttu-id="54025-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54025-151">0x00000010</span></span>                                         |
| <span data-ttu-id="54025-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54025-152">Classes used in</span></span>        | [<span data-ttu-id="54025-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="54025-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="54025-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="54025-154">Windows Server 2003</span></span>



| <span data-ttu-id="54025-155">進入</span><span class="sxs-lookup"><span data-stu-id="54025-155">Entry</span></span> | <span data-ttu-id="54025-156">值</span><span class="sxs-lookup"><span data-stu-id="54025-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="54025-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54025-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54025-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="54025-159">System-Only</span></span>            | <span data-ttu-id="54025-160">否</span><span class="sxs-lookup"><span data-stu-id="54025-160">False</span></span>                                              |
| <span data-ttu-id="54025-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54025-161">Is-Single-Valued</span></span>       | <span data-ttu-id="54025-162">對</span><span class="sxs-lookup"><span data-stu-id="54025-162">True</span></span>                                               |
| <span data-ttu-id="54025-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54025-163">Is Indexed</span></span>             | <span data-ttu-id="54025-164">否</span><span class="sxs-lookup"><span data-stu-id="54025-164">False</span></span>                                              |
| <span data-ttu-id="54025-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54025-165">In Global Catalog</span></span>      | <span data-ttu-id="54025-166">否</span><span class="sxs-lookup"><span data-stu-id="54025-166">False</span></span>                                              |
| <span data-ttu-id="54025-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54025-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="54025-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54025-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="54025-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54025-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="54025-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54025-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="54025-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-171">Search-Flags</span></span>           | <span data-ttu-id="54025-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54025-172">0x00000000</span></span>                                         |
| <span data-ttu-id="54025-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-173">System-Flags</span></span>           | <span data-ttu-id="54025-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54025-174">0x00000010</span></span>                                         |
| <span data-ttu-id="54025-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54025-175">Classes used in</span></span>        | [<span data-ttu-id="54025-176">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="54025-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="54025-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="54025-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="54025-178">進入</span><span class="sxs-lookup"><span data-stu-id="54025-178">Entry</span></span> | <span data-ttu-id="54025-179">值</span><span class="sxs-lookup"><span data-stu-id="54025-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="54025-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54025-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54025-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="54025-182">System-Only</span></span>            | <span data-ttu-id="54025-183">否</span><span class="sxs-lookup"><span data-stu-id="54025-183">False</span></span>                                              |
| <span data-ttu-id="54025-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54025-184">Is-Single-Valued</span></span>       | <span data-ttu-id="54025-185">對</span><span class="sxs-lookup"><span data-stu-id="54025-185">True</span></span>                                               |
| <span data-ttu-id="54025-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54025-186">Is Indexed</span></span>             | <span data-ttu-id="54025-187">否</span><span class="sxs-lookup"><span data-stu-id="54025-187">False</span></span>                                              |
| <span data-ttu-id="54025-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54025-188">In Global Catalog</span></span>      | <span data-ttu-id="54025-189">否</span><span class="sxs-lookup"><span data-stu-id="54025-189">False</span></span>                                              |
| <span data-ttu-id="54025-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54025-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="54025-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54025-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="54025-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54025-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="54025-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54025-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="54025-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-194">Search-Flags</span></span>           | <span data-ttu-id="54025-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54025-195">0x00000000</span></span>                                         |
| <span data-ttu-id="54025-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-196">System-Flags</span></span>           | <span data-ttu-id="54025-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54025-197">0x00000010</span></span>                                         |
| <span data-ttu-id="54025-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54025-198">Classes used in</span></span>        | [<span data-ttu-id="54025-199">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="54025-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="54025-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54025-200">Windows Server 2008</span></span>



| <span data-ttu-id="54025-201">進入</span><span class="sxs-lookup"><span data-stu-id="54025-201">Entry</span></span> | <span data-ttu-id="54025-202">值</span><span class="sxs-lookup"><span data-stu-id="54025-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="54025-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54025-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54025-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="54025-205">System-Only</span></span>            | <span data-ttu-id="54025-206">否</span><span class="sxs-lookup"><span data-stu-id="54025-206">False</span></span>                                              |
| <span data-ttu-id="54025-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54025-207">Is-Single-Valued</span></span>       | <span data-ttu-id="54025-208">對</span><span class="sxs-lookup"><span data-stu-id="54025-208">True</span></span>                                               |
| <span data-ttu-id="54025-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54025-209">Is Indexed</span></span>             | <span data-ttu-id="54025-210">否</span><span class="sxs-lookup"><span data-stu-id="54025-210">False</span></span>                                              |
| <span data-ttu-id="54025-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54025-211">In Global Catalog</span></span>      | <span data-ttu-id="54025-212">否</span><span class="sxs-lookup"><span data-stu-id="54025-212">False</span></span>                                              |
| <span data-ttu-id="54025-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54025-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="54025-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54025-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="54025-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54025-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="54025-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54025-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="54025-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-217">Search-Flags</span></span>           | <span data-ttu-id="54025-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54025-218">0x00000000</span></span>                                         |
| <span data-ttu-id="54025-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-219">System-Flags</span></span>           | <span data-ttu-id="54025-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54025-220">0x00000010</span></span>                                         |
| <span data-ttu-id="54025-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54025-221">Classes used in</span></span>        | [<span data-ttu-id="54025-222">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="54025-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="54025-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54025-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="54025-224">進入</span><span class="sxs-lookup"><span data-stu-id="54025-224">Entry</span></span> | <span data-ttu-id="54025-225">值</span><span class="sxs-lookup"><span data-stu-id="54025-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="54025-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54025-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54025-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="54025-228">System-Only</span></span>            | <span data-ttu-id="54025-229">否</span><span class="sxs-lookup"><span data-stu-id="54025-229">False</span></span>                                              |
| <span data-ttu-id="54025-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54025-230">Is-Single-Valued</span></span>       | <span data-ttu-id="54025-231">對</span><span class="sxs-lookup"><span data-stu-id="54025-231">True</span></span>                                               |
| <span data-ttu-id="54025-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54025-232">Is Indexed</span></span>             | <span data-ttu-id="54025-233">否</span><span class="sxs-lookup"><span data-stu-id="54025-233">False</span></span>                                              |
| <span data-ttu-id="54025-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54025-234">In Global Catalog</span></span>      | <span data-ttu-id="54025-235">否</span><span class="sxs-lookup"><span data-stu-id="54025-235">False</span></span>                                              |
| <span data-ttu-id="54025-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54025-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="54025-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54025-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="54025-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54025-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="54025-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54025-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="54025-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-240">Search-Flags</span></span>           | <span data-ttu-id="54025-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54025-241">0x00000000</span></span>                                         |
| <span data-ttu-id="54025-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-242">System-Flags</span></span>           | <span data-ttu-id="54025-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54025-243">0x00000010</span></span>                                         |
| <span data-ttu-id="54025-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54025-244">Classes used in</span></span>        | [<span data-ttu-id="54025-245">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="54025-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="54025-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54025-246">Windows Server 2012</span></span>



| <span data-ttu-id="54025-247">進入</span><span class="sxs-lookup"><span data-stu-id="54025-247">Entry</span></span> | <span data-ttu-id="54025-248">值</span><span class="sxs-lookup"><span data-stu-id="54025-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="54025-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="54025-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54025-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="54025-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="54025-251">System-Only</span></span>            | <span data-ttu-id="54025-252">否</span><span class="sxs-lookup"><span data-stu-id="54025-252">False</span></span>                                              |
| <span data-ttu-id="54025-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="54025-253">Is-Single-Valued</span></span>       | <span data-ttu-id="54025-254">對</span><span class="sxs-lookup"><span data-stu-id="54025-254">True</span></span>                                               |
| <span data-ttu-id="54025-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="54025-255">Is Indexed</span></span>             | <span data-ttu-id="54025-256">否</span><span class="sxs-lookup"><span data-stu-id="54025-256">False</span></span>                                              |
| <span data-ttu-id="54025-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="54025-257">In Global Catalog</span></span>      | <span data-ttu-id="54025-258">否</span><span class="sxs-lookup"><span data-stu-id="54025-258">False</span></span>                                              |
| <span data-ttu-id="54025-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="54025-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="54025-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="54025-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="54025-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54025-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="54025-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54025-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="54025-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-263">Search-Flags</span></span>           | <span data-ttu-id="54025-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54025-264">0x00000000</span></span>                                         |
| <span data-ttu-id="54025-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54025-265">System-Flags</span></span>           | <span data-ttu-id="54025-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54025-266">0x00000010</span></span>                                         |
| <span data-ttu-id="54025-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="54025-267">Classes used in</span></span>        | [<span data-ttu-id="54025-268">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="54025-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





