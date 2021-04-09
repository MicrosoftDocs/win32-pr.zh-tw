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
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="5fc9c-105">最大票證-存留期屬性</span><span class="sxs-lookup"><span data-stu-id="5fc9c-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="5fc9c-106">這個屬性會決定使用者的票證授與票證 (TGT) 可用於 Kerberos 驗證的最大時間量（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="5fc9c-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="5fc9c-107">當使用者的 TGT 過期時，必須要求新的 TGT，或必須更新現有的 TGT。</span><span class="sxs-lookup"><span data-stu-id="5fc9c-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="5fc9c-108">根據預設，在預設網域群組原則物件 (GPO) 中，此設定為10小時。</span><span class="sxs-lookup"><span data-stu-id="5fc9c-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="5fc9c-109">進入</span><span class="sxs-lookup"><span data-stu-id="5fc9c-109">Entry</span></span> | <span data-ttu-id="5fc9c-110">值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5fc9c-111">CN</span><span class="sxs-lookup"><span data-stu-id="5fc9c-111">CN</span></span>                | <span data-ttu-id="5fc9c-112">最大票證-存留期</span><span class="sxs-lookup"><span data-stu-id="5fc9c-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="5fc9c-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5fc9c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5fc9c-114">maxTicketAge</span><span class="sxs-lookup"><span data-stu-id="5fc9c-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="5fc9c-115">大小</span><span class="sxs-lookup"><span data-stu-id="5fc9c-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="5fc9c-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5fc9c-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5fc9c-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5fc9c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5fc9c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5fc9c-118">Attribute-Id</span></span>      | <span data-ttu-id="5fc9c-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="5fc9c-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="5fc9c-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5fc9c-120">System-Id-Guid</span></span>    | <span data-ttu-id="5fc9c-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5fc9c-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5fc9c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fc9c-122">Syntax</span></span>            | [<span data-ttu-id="5fc9c-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5fc9c-124">實作</span><span class="sxs-lookup"><span data-stu-id="5fc9c-124">Implementations</span></span>

-   [<span data-ttu-id="5fc9c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5fc9c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5fc9c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5fc9c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5fc9c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5fc9c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5fc9c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5fc9c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5fc9c-132">進入</span><span class="sxs-lookup"><span data-stu-id="5fc9c-132">Entry</span></span> | <span data-ttu-id="5fc9c-133">值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5fc9c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5fc9c-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc9c-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc9c-136">System-Only</span></span>            | <span data-ttu-id="5fc9c-137">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-137">False</span></span>                                              |
| <span data-ttu-id="5fc9c-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc9c-139">對</span><span class="sxs-lookup"><span data-stu-id="5fc9c-139">True</span></span>                                               |
| <span data-ttu-id="5fc9c-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5fc9c-140">Is Indexed</span></span>             | <span data-ttu-id="5fc9c-141">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-141">False</span></span>                                              |
| <span data-ttu-id="5fc9c-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5fc9c-142">In Global Catalog</span></span>      | <span data-ttu-id="5fc9c-143">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-143">False</span></span>                                              |
| <span data-ttu-id="5fc9c-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5fc9c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc9c-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5fc9c-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5fc9c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc9c-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc9c-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-148">Search-Flags</span></span>           | <span data-ttu-id="5fc9c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc9c-149">0x00000000</span></span>                                         |
| <span data-ttu-id="5fc9c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-150">System-Flags</span></span>           | <span data-ttu-id="5fc9c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc9c-151">0x00000010</span></span>                                         |
| <span data-ttu-id="5fc9c-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5fc9c-152">Classes used in</span></span>        | [<span data-ttu-id="5fc9c-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5fc9c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fc9c-154">Windows Server 2003</span></span>



| <span data-ttu-id="5fc9c-155">進入</span><span class="sxs-lookup"><span data-stu-id="5fc9c-155">Entry</span></span> | <span data-ttu-id="5fc9c-156">值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5fc9c-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5fc9c-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc9c-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc9c-159">System-Only</span></span>            | <span data-ttu-id="5fc9c-160">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-160">False</span></span>                                              |
| <span data-ttu-id="5fc9c-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc9c-162">對</span><span class="sxs-lookup"><span data-stu-id="5fc9c-162">True</span></span>                                               |
| <span data-ttu-id="5fc9c-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5fc9c-163">Is Indexed</span></span>             | <span data-ttu-id="5fc9c-164">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-164">False</span></span>                                              |
| <span data-ttu-id="5fc9c-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5fc9c-165">In Global Catalog</span></span>      | <span data-ttu-id="5fc9c-166">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-166">False</span></span>                                              |
| <span data-ttu-id="5fc9c-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5fc9c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc9c-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5fc9c-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5fc9c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc9c-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc9c-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-171">Search-Flags</span></span>           | <span data-ttu-id="5fc9c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc9c-172">0x00000000</span></span>                                         |
| <span data-ttu-id="5fc9c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-173">System-Flags</span></span>           | <span data-ttu-id="5fc9c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc9c-174">0x00000010</span></span>                                         |
| <span data-ttu-id="5fc9c-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5fc9c-175">Classes used in</span></span>        | [<span data-ttu-id="5fc9c-176">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5fc9c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5fc9c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5fc9c-178">進入</span><span class="sxs-lookup"><span data-stu-id="5fc9c-178">Entry</span></span> | <span data-ttu-id="5fc9c-179">值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5fc9c-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5fc9c-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc9c-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc9c-182">System-Only</span></span>            | <span data-ttu-id="5fc9c-183">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-183">False</span></span>                                              |
| <span data-ttu-id="5fc9c-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc9c-185">對</span><span class="sxs-lookup"><span data-stu-id="5fc9c-185">True</span></span>                                               |
| <span data-ttu-id="5fc9c-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5fc9c-186">Is Indexed</span></span>             | <span data-ttu-id="5fc9c-187">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-187">False</span></span>                                              |
| <span data-ttu-id="5fc9c-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5fc9c-188">In Global Catalog</span></span>      | <span data-ttu-id="5fc9c-189">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-189">False</span></span>                                              |
| <span data-ttu-id="5fc9c-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5fc9c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc9c-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5fc9c-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5fc9c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc9c-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc9c-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-194">Search-Flags</span></span>           | <span data-ttu-id="5fc9c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc9c-195">0x00000000</span></span>                                         |
| <span data-ttu-id="5fc9c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-196">System-Flags</span></span>           | <span data-ttu-id="5fc9c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc9c-197">0x00000010</span></span>                                         |
| <span data-ttu-id="5fc9c-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5fc9c-198">Classes used in</span></span>        | [<span data-ttu-id="5fc9c-199">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5fc9c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fc9c-200">Windows Server 2008</span></span>



| <span data-ttu-id="5fc9c-201">進入</span><span class="sxs-lookup"><span data-stu-id="5fc9c-201">Entry</span></span> | <span data-ttu-id="5fc9c-202">值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5fc9c-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5fc9c-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc9c-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc9c-205">System-Only</span></span>            | <span data-ttu-id="5fc9c-206">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-206">False</span></span>                                              |
| <span data-ttu-id="5fc9c-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc9c-208">對</span><span class="sxs-lookup"><span data-stu-id="5fc9c-208">True</span></span>                                               |
| <span data-ttu-id="5fc9c-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5fc9c-209">Is Indexed</span></span>             | <span data-ttu-id="5fc9c-210">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-210">False</span></span>                                              |
| <span data-ttu-id="5fc9c-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5fc9c-211">In Global Catalog</span></span>      | <span data-ttu-id="5fc9c-212">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-212">False</span></span>                                              |
| <span data-ttu-id="5fc9c-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5fc9c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc9c-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5fc9c-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5fc9c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc9c-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc9c-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-217">Search-Flags</span></span>           | <span data-ttu-id="5fc9c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc9c-218">0x00000000</span></span>                                         |
| <span data-ttu-id="5fc9c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-219">System-Flags</span></span>           | <span data-ttu-id="5fc9c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc9c-220">0x00000010</span></span>                                         |
| <span data-ttu-id="5fc9c-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5fc9c-221">Classes used in</span></span>        | [<span data-ttu-id="5fc9c-222">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5fc9c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5fc9c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5fc9c-224">進入</span><span class="sxs-lookup"><span data-stu-id="5fc9c-224">Entry</span></span> | <span data-ttu-id="5fc9c-225">值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5fc9c-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5fc9c-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc9c-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc9c-228">System-Only</span></span>            | <span data-ttu-id="5fc9c-229">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-229">False</span></span>                                              |
| <span data-ttu-id="5fc9c-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc9c-231">對</span><span class="sxs-lookup"><span data-stu-id="5fc9c-231">True</span></span>                                               |
| <span data-ttu-id="5fc9c-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5fc9c-232">Is Indexed</span></span>             | <span data-ttu-id="5fc9c-233">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-233">False</span></span>                                              |
| <span data-ttu-id="5fc9c-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5fc9c-234">In Global Catalog</span></span>      | <span data-ttu-id="5fc9c-235">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-235">False</span></span>                                              |
| <span data-ttu-id="5fc9c-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5fc9c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc9c-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5fc9c-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5fc9c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc9c-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc9c-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-240">Search-Flags</span></span>           | <span data-ttu-id="5fc9c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc9c-241">0x00000000</span></span>                                         |
| <span data-ttu-id="5fc9c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-242">System-Flags</span></span>           | <span data-ttu-id="5fc9c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc9c-243">0x00000010</span></span>                                         |
| <span data-ttu-id="5fc9c-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5fc9c-244">Classes used in</span></span>        | [<span data-ttu-id="5fc9c-245">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5fc9c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fc9c-246">Windows Server 2012</span></span>



| <span data-ttu-id="5fc9c-247">進入</span><span class="sxs-lookup"><span data-stu-id="5fc9c-247">Entry</span></span> | <span data-ttu-id="5fc9c-248">值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5fc9c-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5fc9c-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5fc9c-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5fc9c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5fc9c-251">System-Only</span></span>            | <span data-ttu-id="5fc9c-252">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-252">False</span></span>                                              |
| <span data-ttu-id="5fc9c-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5fc9c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5fc9c-254">對</span><span class="sxs-lookup"><span data-stu-id="5fc9c-254">True</span></span>                                               |
| <span data-ttu-id="5fc9c-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5fc9c-255">Is Indexed</span></span>             | <span data-ttu-id="5fc9c-256">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-256">False</span></span>                                              |
| <span data-ttu-id="5fc9c-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5fc9c-257">In Global Catalog</span></span>      | <span data-ttu-id="5fc9c-258">否</span><span class="sxs-lookup"><span data-stu-id="5fc9c-258">False</span></span>                                              |
| <span data-ttu-id="5fc9c-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5fc9c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5fc9c-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5fc9c-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5fc9c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5fc9c-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5fc9c-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5fc9c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-263">Search-Flags</span></span>           | <span data-ttu-id="5fc9c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5fc9c-264">0x00000000</span></span>                                         |
| <span data-ttu-id="5fc9c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5fc9c-265">System-Flags</span></span>           | <span data-ttu-id="5fc9c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5fc9c-266">0x00000010</span></span>                                         |
| <span data-ttu-id="5fc9c-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5fc9c-267">Classes used in</span></span>        | [<span data-ttu-id="5fc9c-268">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="5fc9c-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





