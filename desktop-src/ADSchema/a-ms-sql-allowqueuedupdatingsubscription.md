---
title: AllowQueuedUpdatingSubscription 屬性
description: True 表示在更新訂閱時允許佇列的交易。
ms.assetid: 132c107f-8586-48db-b70c-027c619aadf7
ms.tgt_platform: multiple
keywords:
- AllowQueuedUpdatingSubscription 屬性 AD 架構
- AllowQueuedUpdatingSubscription 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-AllowQueuedUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2056a04b6e0f155c156cde06975e96eb13f61eb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844708"
---
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="cc504-105">AllowQueuedUpdatingSubscription 屬性</span><span class="sxs-lookup"><span data-stu-id="cc504-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="cc504-106">True 表示在更新訂閱時允許佇列的交易。</span><span class="sxs-lookup"><span data-stu-id="cc504-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="cc504-107">進入</span><span class="sxs-lookup"><span data-stu-id="cc504-107">Entry</span></span> | <span data-ttu-id="cc504-108">值</span><span class="sxs-lookup"><span data-stu-id="cc504-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="cc504-109">CN</span><span class="sxs-lookup"><span data-stu-id="cc504-109">CN</span></span>                | <span data-ttu-id="cc504-110">AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="cc504-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="cc504-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cc504-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cc504-112">AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="cc504-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="cc504-113">大小</span><span class="sxs-lookup"><span data-stu-id="cc504-113">Size</span></span>              | <span data-ttu-id="cc504-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="cc504-114">4 bytes</span></span>                                |
| <span data-ttu-id="cc504-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="cc504-115">Update Privilege</span></span>  | <span data-ttu-id="cc504-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="cc504-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="cc504-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="cc504-117">Update Frequency</span></span>  | <span data-ttu-id="cc504-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="cc504-118">When replication is setup.</span></span>             |
| <span data-ttu-id="cc504-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc504-119">Attribute-Id</span></span>      | <span data-ttu-id="cc504-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="cc504-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="cc504-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="cc504-121">System-Id-Guid</span></span>    | <span data-ttu-id="cc504-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cc504-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="cc504-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc504-123">Syntax</span></span>            | [<span data-ttu-id="cc504-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc504-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="cc504-125">實作</span><span class="sxs-lookup"><span data-stu-id="cc504-125">Implementations</span></span>

-   [<span data-ttu-id="cc504-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cc504-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cc504-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc504-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc504-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc504-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc504-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc504-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc504-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc504-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc504-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc504-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cc504-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc504-132">Windows 2000 Server</span></span>



| <span data-ttu-id="cc504-133">進入</span><span class="sxs-lookup"><span data-stu-id="cc504-133">Entry</span></span> | <span data-ttu-id="cc504-134">值</span><span class="sxs-lookup"><span data-stu-id="cc504-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cc504-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cc504-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc504-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc504-137">System-Only</span></span>            | <span data-ttu-id="cc504-138">否</span><span class="sxs-lookup"><span data-stu-id="cc504-138">False</span></span>                                                               |
| <span data-ttu-id="cc504-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cc504-139">Is-Single-Valued</span></span>       | <span data-ttu-id="cc504-140">對</span><span class="sxs-lookup"><span data-stu-id="cc504-140">True</span></span>                                                                |
| <span data-ttu-id="cc504-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cc504-141">Is Indexed</span></span>             | <span data-ttu-id="cc504-142">否</span><span class="sxs-lookup"><span data-stu-id="cc504-142">False</span></span>                                                               |
| <span data-ttu-id="cc504-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cc504-143">In Global Catalog</span></span>      | <span data-ttu-id="cc504-144">否</span><span class="sxs-lookup"><span data-stu-id="cc504-144">False</span></span>                                                               |
| <span data-ttu-id="cc504-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cc504-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc504-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cc504-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cc504-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc504-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc504-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-149">Search-Flags</span></span>           | <span data-ttu-id="cc504-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc504-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="cc504-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-151">System-Flags</span></span>           | <span data-ttu-id="cc504-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc504-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="cc504-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cc504-153">Classes used in</span></span>        | [<span data-ttu-id="cc504-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="cc504-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cc504-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc504-155">Windows Server 2003</span></span>



| <span data-ttu-id="cc504-156">進入</span><span class="sxs-lookup"><span data-stu-id="cc504-156">Entry</span></span> | <span data-ttu-id="cc504-157">值</span><span class="sxs-lookup"><span data-stu-id="cc504-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cc504-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cc504-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc504-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc504-160">System-Only</span></span>            | <span data-ttu-id="cc504-161">否</span><span class="sxs-lookup"><span data-stu-id="cc504-161">False</span></span>                                                               |
| <span data-ttu-id="cc504-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cc504-162">Is-Single-Valued</span></span>       | <span data-ttu-id="cc504-163">對</span><span class="sxs-lookup"><span data-stu-id="cc504-163">True</span></span>                                                                |
| <span data-ttu-id="cc504-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cc504-164">Is Indexed</span></span>             | <span data-ttu-id="cc504-165">否</span><span class="sxs-lookup"><span data-stu-id="cc504-165">False</span></span>                                                               |
| <span data-ttu-id="cc504-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cc504-166">In Global Catalog</span></span>      | <span data-ttu-id="cc504-167">否</span><span class="sxs-lookup"><span data-stu-id="cc504-167">False</span></span>                                                               |
| <span data-ttu-id="cc504-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cc504-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc504-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cc504-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cc504-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc504-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc504-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-172">Search-Flags</span></span>           | <span data-ttu-id="cc504-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc504-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="cc504-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-174">System-Flags</span></span>           | <span data-ttu-id="cc504-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc504-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="cc504-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cc504-176">Classes used in</span></span>        | [<span data-ttu-id="cc504-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="cc504-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc504-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc504-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc504-179">進入</span><span class="sxs-lookup"><span data-stu-id="cc504-179">Entry</span></span> | <span data-ttu-id="cc504-180">值</span><span class="sxs-lookup"><span data-stu-id="cc504-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cc504-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cc504-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc504-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc504-183">System-Only</span></span>            | <span data-ttu-id="cc504-184">否</span><span class="sxs-lookup"><span data-stu-id="cc504-184">False</span></span>                                                               |
| <span data-ttu-id="cc504-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cc504-185">Is-Single-Valued</span></span>       | <span data-ttu-id="cc504-186">對</span><span class="sxs-lookup"><span data-stu-id="cc504-186">True</span></span>                                                                |
| <span data-ttu-id="cc504-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cc504-187">Is Indexed</span></span>             | <span data-ttu-id="cc504-188">否</span><span class="sxs-lookup"><span data-stu-id="cc504-188">False</span></span>                                                               |
| <span data-ttu-id="cc504-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cc504-189">In Global Catalog</span></span>      | <span data-ttu-id="cc504-190">否</span><span class="sxs-lookup"><span data-stu-id="cc504-190">False</span></span>                                                               |
| <span data-ttu-id="cc504-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cc504-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc504-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cc504-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cc504-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc504-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc504-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-195">Search-Flags</span></span>           | <span data-ttu-id="cc504-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc504-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="cc504-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-197">System-Flags</span></span>           | <span data-ttu-id="cc504-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc504-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="cc504-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cc504-199">Classes used in</span></span>        | [<span data-ttu-id="cc504-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="cc504-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc504-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc504-201">Windows Server 2008</span></span>



| <span data-ttu-id="cc504-202">進入</span><span class="sxs-lookup"><span data-stu-id="cc504-202">Entry</span></span> | <span data-ttu-id="cc504-203">值</span><span class="sxs-lookup"><span data-stu-id="cc504-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cc504-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cc504-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc504-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc504-206">System-Only</span></span>            | <span data-ttu-id="cc504-207">否</span><span class="sxs-lookup"><span data-stu-id="cc504-207">False</span></span>                                                               |
| <span data-ttu-id="cc504-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cc504-208">Is-Single-Valued</span></span>       | <span data-ttu-id="cc504-209">對</span><span class="sxs-lookup"><span data-stu-id="cc504-209">True</span></span>                                                                |
| <span data-ttu-id="cc504-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cc504-210">Is Indexed</span></span>             | <span data-ttu-id="cc504-211">否</span><span class="sxs-lookup"><span data-stu-id="cc504-211">False</span></span>                                                               |
| <span data-ttu-id="cc504-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cc504-212">In Global Catalog</span></span>      | <span data-ttu-id="cc504-213">否</span><span class="sxs-lookup"><span data-stu-id="cc504-213">False</span></span>                                                               |
| <span data-ttu-id="cc504-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cc504-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc504-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cc504-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cc504-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc504-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc504-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-218">Search-Flags</span></span>           | <span data-ttu-id="cc504-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc504-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="cc504-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-220">System-Flags</span></span>           | <span data-ttu-id="cc504-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc504-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="cc504-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cc504-222">Classes used in</span></span>        | [<span data-ttu-id="cc504-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="cc504-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc504-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc504-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc504-225">進入</span><span class="sxs-lookup"><span data-stu-id="cc504-225">Entry</span></span> | <span data-ttu-id="cc504-226">值</span><span class="sxs-lookup"><span data-stu-id="cc504-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cc504-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cc504-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc504-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc504-229">System-Only</span></span>            | <span data-ttu-id="cc504-230">否</span><span class="sxs-lookup"><span data-stu-id="cc504-230">False</span></span>                                                               |
| <span data-ttu-id="cc504-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cc504-231">Is-Single-Valued</span></span>       | <span data-ttu-id="cc504-232">對</span><span class="sxs-lookup"><span data-stu-id="cc504-232">True</span></span>                                                                |
| <span data-ttu-id="cc504-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cc504-233">Is Indexed</span></span>             | <span data-ttu-id="cc504-234">否</span><span class="sxs-lookup"><span data-stu-id="cc504-234">False</span></span>                                                               |
| <span data-ttu-id="cc504-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cc504-235">In Global Catalog</span></span>      | <span data-ttu-id="cc504-236">否</span><span class="sxs-lookup"><span data-stu-id="cc504-236">False</span></span>                                                               |
| <span data-ttu-id="cc504-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cc504-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc504-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cc504-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cc504-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc504-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc504-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-241">Search-Flags</span></span>           | <span data-ttu-id="cc504-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc504-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="cc504-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-243">System-Flags</span></span>           | <span data-ttu-id="cc504-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc504-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="cc504-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cc504-245">Classes used in</span></span>        | [<span data-ttu-id="cc504-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="cc504-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc504-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc504-247">Windows Server 2012</span></span>



| <span data-ttu-id="cc504-248">進入</span><span class="sxs-lookup"><span data-stu-id="cc504-248">Entry</span></span> | <span data-ttu-id="cc504-249">值</span><span class="sxs-lookup"><span data-stu-id="cc504-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cc504-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cc504-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc504-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="cc504-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc504-252">System-Only</span></span>            | <span data-ttu-id="cc504-253">否</span><span class="sxs-lookup"><span data-stu-id="cc504-253">False</span></span>                                                               |
| <span data-ttu-id="cc504-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cc504-254">Is-Single-Valued</span></span>       | <span data-ttu-id="cc504-255">對</span><span class="sxs-lookup"><span data-stu-id="cc504-255">True</span></span>                                                                |
| <span data-ttu-id="cc504-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cc504-256">Is Indexed</span></span>             | <span data-ttu-id="cc504-257">否</span><span class="sxs-lookup"><span data-stu-id="cc504-257">False</span></span>                                                               |
| <span data-ttu-id="cc504-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cc504-258">In Global Catalog</span></span>      | <span data-ttu-id="cc504-259">否</span><span class="sxs-lookup"><span data-stu-id="cc504-259">False</span></span>                                                               |
| <span data-ttu-id="cc504-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cc504-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc504-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cc504-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="cc504-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc504-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc504-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="cc504-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-264">Search-Flags</span></span>           | <span data-ttu-id="cc504-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc504-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="cc504-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc504-266">System-Flags</span></span>           | <span data-ttu-id="cc504-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc504-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="cc504-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cc504-268">Classes used in</span></span>        | [<span data-ttu-id="cc504-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="cc504-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





