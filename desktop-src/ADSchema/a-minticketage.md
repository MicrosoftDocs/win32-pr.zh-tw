---
title: 最小票證-年齡屬性
description: 這個屬性會決定使用者的票證授與票證 (TGT) 的最小時間週期（以小時為單位），在提出要求以更新票證之前，可以使用 Kerberos 驗證。
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- 最小票證-年齡屬性 AD 架構
- minTicketAge 屬性 AD 架構
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc43277bb3750ee0e759baa4348e85ef826ce010
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107201"
---
# <a name="min-ticket-age-attribute"></a><span data-ttu-id="545f2-105">最小票證-年齡屬性</span><span class="sxs-lookup"><span data-stu-id="545f2-105">Min-Ticket-Age attribute</span></span>

<span data-ttu-id="545f2-106">這個屬性會決定使用者的票證授與票證 (TGT) 的最小時間週期（以小時為單位），在提出要求以更新票證之前，可以使用 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="545f2-106">This attribute determines the minimum time period, in hours, that a user's ticket-granting ticket (TGT) can be used for Kerberos authentication before a request can be made to renew the ticket.</span></span>



| <span data-ttu-id="545f2-107">進入</span><span class="sxs-lookup"><span data-stu-id="545f2-107">Entry</span></span> | <span data-ttu-id="545f2-108">值</span><span class="sxs-lookup"><span data-stu-id="545f2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="545f2-109">CN</span><span class="sxs-lookup"><span data-stu-id="545f2-109">CN</span></span>                | <span data-ttu-id="545f2-110">最小票證-年齡</span><span class="sxs-lookup"><span data-stu-id="545f2-110">Min-Ticket-Age</span></span>                       |
| <span data-ttu-id="545f2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="545f2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="545f2-112">minTicketAge</span><span class="sxs-lookup"><span data-stu-id="545f2-112">minTicketAge</span></span>                         |
| <span data-ttu-id="545f2-113">大小</span><span class="sxs-lookup"><span data-stu-id="545f2-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="545f2-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="545f2-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="545f2-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="545f2-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="545f2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="545f2-116">Attribute-Id</span></span>      | <span data-ttu-id="545f2-117">1.2.840.113556.1.4.80</span><span class="sxs-lookup"><span data-stu-id="545f2-117">1.2.840.113556.1.4.80</span></span>                |
| <span data-ttu-id="545f2-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="545f2-118">System-Id-Guid</span></span>    | <span data-ttu-id="545f2-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="545f2-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="545f2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="545f2-120">Syntax</span></span>            | [<span data-ttu-id="545f2-121">**間隔**</span><span class="sxs-lookup"><span data-stu-id="545f2-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="545f2-122">實作</span><span class="sxs-lookup"><span data-stu-id="545f2-122">Implementations</span></span>

-   [<span data-ttu-id="545f2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="545f2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="545f2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="545f2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="545f2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="545f2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="545f2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="545f2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="545f2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="545f2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="545f2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="545f2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="545f2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="545f2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="545f2-130">進入</span><span class="sxs-lookup"><span data-stu-id="545f2-130">Entry</span></span> | <span data-ttu-id="545f2-131">值</span><span class="sxs-lookup"><span data-stu-id="545f2-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="545f2-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="545f2-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="545f2-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="545f2-134">System-Only</span></span>            | <span data-ttu-id="545f2-135">否</span><span class="sxs-lookup"><span data-stu-id="545f2-135">False</span></span>                                              |
| <span data-ttu-id="545f2-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="545f2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="545f2-137">對</span><span class="sxs-lookup"><span data-stu-id="545f2-137">True</span></span>                                               |
| <span data-ttu-id="545f2-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="545f2-138">Is Indexed</span></span>             | <span data-ttu-id="545f2-139">否</span><span class="sxs-lookup"><span data-stu-id="545f2-139">False</span></span>                                              |
| <span data-ttu-id="545f2-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="545f2-140">In Global Catalog</span></span>      | <span data-ttu-id="545f2-141">否</span><span class="sxs-lookup"><span data-stu-id="545f2-141">False</span></span>                                              |
| <span data-ttu-id="545f2-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="545f2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="545f2-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="545f2-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="545f2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="545f2-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="545f2-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-146">Search-Flags</span></span>           | <span data-ttu-id="545f2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="545f2-147">0x00000000</span></span>                                         |
| <span data-ttu-id="545f2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-148">System-Flags</span></span>           | <span data-ttu-id="545f2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="545f2-149">0x00000010</span></span>                                         |
| <span data-ttu-id="545f2-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="545f2-150">Classes used in</span></span>        | [<span data-ttu-id="545f2-151">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="545f2-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="545f2-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="545f2-152">Windows Server 2003</span></span>



| <span data-ttu-id="545f2-153">進入</span><span class="sxs-lookup"><span data-stu-id="545f2-153">Entry</span></span> | <span data-ttu-id="545f2-154">值</span><span class="sxs-lookup"><span data-stu-id="545f2-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="545f2-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="545f2-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="545f2-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="545f2-157">System-Only</span></span>            | <span data-ttu-id="545f2-158">否</span><span class="sxs-lookup"><span data-stu-id="545f2-158">False</span></span>                                              |
| <span data-ttu-id="545f2-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="545f2-159">Is-Single-Valued</span></span>       | <span data-ttu-id="545f2-160">對</span><span class="sxs-lookup"><span data-stu-id="545f2-160">True</span></span>                                               |
| <span data-ttu-id="545f2-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="545f2-161">Is Indexed</span></span>             | <span data-ttu-id="545f2-162">否</span><span class="sxs-lookup"><span data-stu-id="545f2-162">False</span></span>                                              |
| <span data-ttu-id="545f2-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="545f2-163">In Global Catalog</span></span>      | <span data-ttu-id="545f2-164">否</span><span class="sxs-lookup"><span data-stu-id="545f2-164">False</span></span>                                              |
| <span data-ttu-id="545f2-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="545f2-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="545f2-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="545f2-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="545f2-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="545f2-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="545f2-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-169">Search-Flags</span></span>           | <span data-ttu-id="545f2-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="545f2-170">0x00000000</span></span>                                         |
| <span data-ttu-id="545f2-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-171">System-Flags</span></span>           | <span data-ttu-id="545f2-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="545f2-172">0x00000010</span></span>                                         |
| <span data-ttu-id="545f2-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="545f2-173">Classes used in</span></span>        | [<span data-ttu-id="545f2-174">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="545f2-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="545f2-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="545f2-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="545f2-176">進入</span><span class="sxs-lookup"><span data-stu-id="545f2-176">Entry</span></span> | <span data-ttu-id="545f2-177">值</span><span class="sxs-lookup"><span data-stu-id="545f2-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="545f2-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="545f2-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="545f2-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="545f2-180">System-Only</span></span>            | <span data-ttu-id="545f2-181">否</span><span class="sxs-lookup"><span data-stu-id="545f2-181">False</span></span>                                              |
| <span data-ttu-id="545f2-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="545f2-182">Is-Single-Valued</span></span>       | <span data-ttu-id="545f2-183">對</span><span class="sxs-lookup"><span data-stu-id="545f2-183">True</span></span>                                               |
| <span data-ttu-id="545f2-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="545f2-184">Is Indexed</span></span>             | <span data-ttu-id="545f2-185">否</span><span class="sxs-lookup"><span data-stu-id="545f2-185">False</span></span>                                              |
| <span data-ttu-id="545f2-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="545f2-186">In Global Catalog</span></span>      | <span data-ttu-id="545f2-187">否</span><span class="sxs-lookup"><span data-stu-id="545f2-187">False</span></span>                                              |
| <span data-ttu-id="545f2-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="545f2-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="545f2-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="545f2-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="545f2-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="545f2-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="545f2-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-192">Search-Flags</span></span>           | <span data-ttu-id="545f2-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="545f2-193">0x00000000</span></span>                                         |
| <span data-ttu-id="545f2-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-194">System-Flags</span></span>           | <span data-ttu-id="545f2-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="545f2-195">0x00000010</span></span>                                         |
| <span data-ttu-id="545f2-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="545f2-196">Classes used in</span></span>        | [<span data-ttu-id="545f2-197">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="545f2-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="545f2-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="545f2-198">Windows Server 2008</span></span>



| <span data-ttu-id="545f2-199">進入</span><span class="sxs-lookup"><span data-stu-id="545f2-199">Entry</span></span> | <span data-ttu-id="545f2-200">值</span><span class="sxs-lookup"><span data-stu-id="545f2-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="545f2-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="545f2-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="545f2-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="545f2-203">System-Only</span></span>            | <span data-ttu-id="545f2-204">否</span><span class="sxs-lookup"><span data-stu-id="545f2-204">False</span></span>                                              |
| <span data-ttu-id="545f2-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="545f2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="545f2-206">對</span><span class="sxs-lookup"><span data-stu-id="545f2-206">True</span></span>                                               |
| <span data-ttu-id="545f2-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="545f2-207">Is Indexed</span></span>             | <span data-ttu-id="545f2-208">否</span><span class="sxs-lookup"><span data-stu-id="545f2-208">False</span></span>                                              |
| <span data-ttu-id="545f2-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="545f2-209">In Global Catalog</span></span>      | <span data-ttu-id="545f2-210">否</span><span class="sxs-lookup"><span data-stu-id="545f2-210">False</span></span>                                              |
| <span data-ttu-id="545f2-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="545f2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="545f2-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="545f2-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="545f2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="545f2-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="545f2-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-215">Search-Flags</span></span>           | <span data-ttu-id="545f2-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="545f2-216">0x00000000</span></span>                                         |
| <span data-ttu-id="545f2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-217">System-Flags</span></span>           | <span data-ttu-id="545f2-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="545f2-218">0x00000010</span></span>                                         |
| <span data-ttu-id="545f2-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="545f2-219">Classes used in</span></span>        | [<span data-ttu-id="545f2-220">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="545f2-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="545f2-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="545f2-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="545f2-222">進入</span><span class="sxs-lookup"><span data-stu-id="545f2-222">Entry</span></span> | <span data-ttu-id="545f2-223">值</span><span class="sxs-lookup"><span data-stu-id="545f2-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="545f2-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="545f2-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="545f2-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="545f2-226">System-Only</span></span>            | <span data-ttu-id="545f2-227">否</span><span class="sxs-lookup"><span data-stu-id="545f2-227">False</span></span>                                              |
| <span data-ttu-id="545f2-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="545f2-228">Is-Single-Valued</span></span>       | <span data-ttu-id="545f2-229">對</span><span class="sxs-lookup"><span data-stu-id="545f2-229">True</span></span>                                               |
| <span data-ttu-id="545f2-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="545f2-230">Is Indexed</span></span>             | <span data-ttu-id="545f2-231">否</span><span class="sxs-lookup"><span data-stu-id="545f2-231">False</span></span>                                              |
| <span data-ttu-id="545f2-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="545f2-232">In Global Catalog</span></span>      | <span data-ttu-id="545f2-233">否</span><span class="sxs-lookup"><span data-stu-id="545f2-233">False</span></span>                                              |
| <span data-ttu-id="545f2-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="545f2-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="545f2-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="545f2-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="545f2-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="545f2-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="545f2-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-238">Search-Flags</span></span>           | <span data-ttu-id="545f2-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="545f2-239">0x00000000</span></span>                                         |
| <span data-ttu-id="545f2-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-240">System-Flags</span></span>           | <span data-ttu-id="545f2-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="545f2-241">0x00000010</span></span>                                         |
| <span data-ttu-id="545f2-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="545f2-242">Classes used in</span></span>        | [<span data-ttu-id="545f2-243">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="545f2-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="545f2-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="545f2-244">Windows Server 2012</span></span>



| <span data-ttu-id="545f2-245">進入</span><span class="sxs-lookup"><span data-stu-id="545f2-245">Entry</span></span> | <span data-ttu-id="545f2-246">值</span><span class="sxs-lookup"><span data-stu-id="545f2-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="545f2-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="545f2-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="545f2-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="545f2-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="545f2-249">System-Only</span></span>            | <span data-ttu-id="545f2-250">否</span><span class="sxs-lookup"><span data-stu-id="545f2-250">False</span></span>                                              |
| <span data-ttu-id="545f2-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="545f2-251">Is-Single-Valued</span></span>       | <span data-ttu-id="545f2-252">對</span><span class="sxs-lookup"><span data-stu-id="545f2-252">True</span></span>                                               |
| <span data-ttu-id="545f2-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="545f2-253">Is Indexed</span></span>             | <span data-ttu-id="545f2-254">否</span><span class="sxs-lookup"><span data-stu-id="545f2-254">False</span></span>                                              |
| <span data-ttu-id="545f2-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="545f2-255">In Global Catalog</span></span>      | <span data-ttu-id="545f2-256">否</span><span class="sxs-lookup"><span data-stu-id="545f2-256">False</span></span>                                              |
| <span data-ttu-id="545f2-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="545f2-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="545f2-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="545f2-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="545f2-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="545f2-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="545f2-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="545f2-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-261">Search-Flags</span></span>           | <span data-ttu-id="545f2-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="545f2-262">0x00000000</span></span>                                         |
| <span data-ttu-id="545f2-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="545f2-263">System-Flags</span></span>           | <span data-ttu-id="545f2-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="545f2-264">0x00000010</span></span>                                         |
| <span data-ttu-id="545f2-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="545f2-265">Classes used in</span></span>        | [<span data-ttu-id="545f2-266">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="545f2-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





