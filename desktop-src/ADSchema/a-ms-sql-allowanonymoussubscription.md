---
title: AllowAnonymousSubscription 屬性
description: 如果發行集允許匿名訂閱者訂閱它，則為 True。
ms.assetid: d4ac86ce-d3c5-493e-8212-e9250671a522
ms.tgt_platform: multiple
keywords:
- AllowAnonymousSubscription 屬性 AD 架構
- AllowAnonymousSubscription 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-AllowAnonymousSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23de7f731ffaca310a39d81d4af80a5b0a23a84
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108209"
---
# <a name="ms-sql-allowanonymoussubscription-attribute"></a><span data-ttu-id="9dfaf-105">AllowAnonymousSubscription 屬性</span><span class="sxs-lookup"><span data-stu-id="9dfaf-105">MS-SQL-AllowAnonymousSubscription attribute</span></span>

<span data-ttu-id="9dfaf-106">如果發行集允許匿名訂閱者訂閱它，則為 True。</span><span class="sxs-lookup"><span data-stu-id="9dfaf-106">True if the publication allows anonymous subscribers to subscribe to it.</span></span>



| <span data-ttu-id="9dfaf-107">進入</span><span class="sxs-lookup"><span data-stu-id="9dfaf-107">Entry</span></span> | <span data-ttu-id="9dfaf-108">值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9dfaf-109">CN</span><span class="sxs-lookup"><span data-stu-id="9dfaf-109">CN</span></span>                | <span data-ttu-id="9dfaf-110">AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="9dfaf-110">MS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="9dfaf-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9dfaf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9dfaf-112">AllowAnonymousSubscription</span><span class="sxs-lookup"><span data-stu-id="9dfaf-112">mS-SQL-AllowAnonymousSubscription</span></span>    |
| <span data-ttu-id="9dfaf-113">大小</span><span class="sxs-lookup"><span data-stu-id="9dfaf-113">Size</span></span>              | <span data-ttu-id="9dfaf-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="9dfaf-114">4 bytes</span></span>                              |
| <span data-ttu-id="9dfaf-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9dfaf-115">Update Privilege</span></span>  | <span data-ttu-id="9dfaf-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9dfaf-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="9dfaf-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9dfaf-117">Update Frequency</span></span>  | <span data-ttu-id="9dfaf-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="9dfaf-118">When replication is setup.</span></span>           |
| <span data-ttu-id="9dfaf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9dfaf-119">Attribute-Id</span></span>      | <span data-ttu-id="9dfaf-120">1.2.840.113556.1.4.1394</span><span class="sxs-lookup"><span data-stu-id="9dfaf-120">1.2.840.113556.1.4.1394</span></span>              |
| <span data-ttu-id="9dfaf-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9dfaf-121">System-Id-Guid</span></span>    | <span data-ttu-id="9dfaf-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9dfaf-122">db77be4a-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="9dfaf-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dfaf-123">Syntax</span></span>            | [<span data-ttu-id="9dfaf-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="9dfaf-125">實作</span><span class="sxs-lookup"><span data-stu-id="9dfaf-125">Implementations</span></span>

-   [<span data-ttu-id="9dfaf-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9dfaf-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9dfaf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9dfaf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9dfaf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9dfaf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9dfaf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9dfaf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9dfaf-133">進入</span><span class="sxs-lookup"><span data-stu-id="9dfaf-133">Entry</span></span> | <span data-ttu-id="9dfaf-134">值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9dfaf-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfaf-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfaf-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfaf-137">System-Only</span></span>            | <span data-ttu-id="9dfaf-138">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-138">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfaf-140">對</span><span class="sxs-lookup"><span data-stu-id="9dfaf-140">True</span></span>                                                                |
| <span data-ttu-id="9dfaf-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfaf-141">Is Indexed</span></span>             | <span data-ttu-id="9dfaf-142">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-142">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfaf-143">In Global Catalog</span></span>      | <span data-ttu-id="9dfaf-144">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-144">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfaf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfaf-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfaf-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9dfaf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfaf-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfaf-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-149">Search-Flags</span></span>           | <span data-ttu-id="9dfaf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfaf-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="9dfaf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-151">System-Flags</span></span>           | <span data-ttu-id="9dfaf-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfaf-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="9dfaf-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfaf-153">Classes used in</span></span>        | [<span data-ttu-id="9dfaf-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9dfaf-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9dfaf-155">Windows Server 2003</span></span>



| <span data-ttu-id="9dfaf-156">進入</span><span class="sxs-lookup"><span data-stu-id="9dfaf-156">Entry</span></span> | <span data-ttu-id="9dfaf-157">值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9dfaf-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfaf-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfaf-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfaf-160">System-Only</span></span>            | <span data-ttu-id="9dfaf-161">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-161">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-162">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfaf-163">對</span><span class="sxs-lookup"><span data-stu-id="9dfaf-163">True</span></span>                                                                |
| <span data-ttu-id="9dfaf-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfaf-164">Is Indexed</span></span>             | <span data-ttu-id="9dfaf-165">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-165">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfaf-166">In Global Catalog</span></span>      | <span data-ttu-id="9dfaf-167">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-167">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfaf-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfaf-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfaf-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9dfaf-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfaf-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfaf-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-172">Search-Flags</span></span>           | <span data-ttu-id="9dfaf-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfaf-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="9dfaf-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-174">System-Flags</span></span>           | <span data-ttu-id="9dfaf-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfaf-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="9dfaf-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfaf-176">Classes used in</span></span>        | [<span data-ttu-id="9dfaf-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9dfaf-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9dfaf-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9dfaf-179">進入</span><span class="sxs-lookup"><span data-stu-id="9dfaf-179">Entry</span></span> | <span data-ttu-id="9dfaf-180">值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9dfaf-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfaf-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfaf-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfaf-183">System-Only</span></span>            | <span data-ttu-id="9dfaf-184">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-184">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-185">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfaf-186">對</span><span class="sxs-lookup"><span data-stu-id="9dfaf-186">True</span></span>                                                                |
| <span data-ttu-id="9dfaf-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfaf-187">Is Indexed</span></span>             | <span data-ttu-id="9dfaf-188">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-188">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfaf-189">In Global Catalog</span></span>      | <span data-ttu-id="9dfaf-190">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-190">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfaf-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfaf-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfaf-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9dfaf-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfaf-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfaf-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-195">Search-Flags</span></span>           | <span data-ttu-id="9dfaf-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfaf-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="9dfaf-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-197">System-Flags</span></span>           | <span data-ttu-id="9dfaf-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfaf-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="9dfaf-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfaf-199">Classes used in</span></span>        | [<span data-ttu-id="9dfaf-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9dfaf-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dfaf-201">Windows Server 2008</span></span>



| <span data-ttu-id="9dfaf-202">進入</span><span class="sxs-lookup"><span data-stu-id="9dfaf-202">Entry</span></span> | <span data-ttu-id="9dfaf-203">值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9dfaf-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfaf-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfaf-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfaf-206">System-Only</span></span>            | <span data-ttu-id="9dfaf-207">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-207">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfaf-209">對</span><span class="sxs-lookup"><span data-stu-id="9dfaf-209">True</span></span>                                                                |
| <span data-ttu-id="9dfaf-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfaf-210">Is Indexed</span></span>             | <span data-ttu-id="9dfaf-211">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-211">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfaf-212">In Global Catalog</span></span>      | <span data-ttu-id="9dfaf-213">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-213">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfaf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfaf-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfaf-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9dfaf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfaf-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfaf-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-218">Search-Flags</span></span>           | <span data-ttu-id="9dfaf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfaf-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="9dfaf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-220">System-Flags</span></span>           | <span data-ttu-id="9dfaf-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfaf-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="9dfaf-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfaf-222">Classes used in</span></span>        | [<span data-ttu-id="9dfaf-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9dfaf-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9dfaf-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9dfaf-225">進入</span><span class="sxs-lookup"><span data-stu-id="9dfaf-225">Entry</span></span> | <span data-ttu-id="9dfaf-226">值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9dfaf-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfaf-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfaf-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfaf-229">System-Only</span></span>            | <span data-ttu-id="9dfaf-230">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-230">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-231">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfaf-232">對</span><span class="sxs-lookup"><span data-stu-id="9dfaf-232">True</span></span>                                                                |
| <span data-ttu-id="9dfaf-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfaf-233">Is Indexed</span></span>             | <span data-ttu-id="9dfaf-234">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-234">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfaf-235">In Global Catalog</span></span>      | <span data-ttu-id="9dfaf-236">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-236">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfaf-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfaf-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfaf-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9dfaf-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfaf-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfaf-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-241">Search-Flags</span></span>           | <span data-ttu-id="9dfaf-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfaf-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="9dfaf-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-243">System-Flags</span></span>           | <span data-ttu-id="9dfaf-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfaf-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="9dfaf-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfaf-245">Classes used in</span></span>        | [<span data-ttu-id="9dfaf-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9dfaf-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9dfaf-247">Windows Server 2012</span></span>



| <span data-ttu-id="9dfaf-248">進入</span><span class="sxs-lookup"><span data-stu-id="9dfaf-248">Entry</span></span> | <span data-ttu-id="9dfaf-249">值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9dfaf-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfaf-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfaf-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9dfaf-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfaf-252">System-Only</span></span>            | <span data-ttu-id="9dfaf-253">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-253">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfaf-254">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfaf-255">對</span><span class="sxs-lookup"><span data-stu-id="9dfaf-255">True</span></span>                                                                |
| <span data-ttu-id="9dfaf-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfaf-256">Is Indexed</span></span>             | <span data-ttu-id="9dfaf-257">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-257">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfaf-258">In Global Catalog</span></span>      | <span data-ttu-id="9dfaf-259">否</span><span class="sxs-lookup"><span data-stu-id="9dfaf-259">False</span></span>                                                               |
| <span data-ttu-id="9dfaf-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfaf-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfaf-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfaf-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9dfaf-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfaf-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfaf-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9dfaf-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-264">Search-Flags</span></span>           | <span data-ttu-id="9dfaf-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfaf-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="9dfaf-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfaf-266">System-Flags</span></span>           | <span data-ttu-id="9dfaf-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfaf-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="9dfaf-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfaf-268">Classes used in</span></span>        | [<span data-ttu-id="9dfaf-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9dfaf-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





