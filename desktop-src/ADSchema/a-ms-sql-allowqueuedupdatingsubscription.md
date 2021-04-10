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
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="c3a1e-105">AllowQueuedUpdatingSubscription 屬性</span><span class="sxs-lookup"><span data-stu-id="c3a1e-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="c3a1e-106">True 表示在更新訂閱時允許佇列的交易。</span><span class="sxs-lookup"><span data-stu-id="c3a1e-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="c3a1e-107">進入</span><span class="sxs-lookup"><span data-stu-id="c3a1e-107">Entry</span></span> | <span data-ttu-id="c3a1e-108">值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="c3a1e-109">CN</span><span class="sxs-lookup"><span data-stu-id="c3a1e-109">CN</span></span>                | <span data-ttu-id="c3a1e-110">AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="c3a1e-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="c3a1e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c3a1e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c3a1e-112">AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="c3a1e-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="c3a1e-113">大小</span><span class="sxs-lookup"><span data-stu-id="c3a1e-113">Size</span></span>              | <span data-ttu-id="c3a1e-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="c3a1e-114">4 bytes</span></span>                                |
| <span data-ttu-id="c3a1e-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c3a1e-115">Update Privilege</span></span>  | <span data-ttu-id="c3a1e-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="c3a1e-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="c3a1e-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c3a1e-117">Update Frequency</span></span>  | <span data-ttu-id="c3a1e-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="c3a1e-118">When replication is setup.</span></span>             |
| <span data-ttu-id="c3a1e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3a1e-119">Attribute-Id</span></span>      | <span data-ttu-id="c3a1e-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="c3a1e-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="c3a1e-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c3a1e-121">System-Id-Guid</span></span>    | <span data-ttu-id="c3a1e-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c3a1e-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="c3a1e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a1e-123">Syntax</span></span>            | [<span data-ttu-id="c3a1e-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="c3a1e-125">實作</span><span class="sxs-lookup"><span data-stu-id="c3a1e-125">Implementations</span></span>

-   [<span data-ttu-id="c3a1e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c3a1e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3a1e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3a1e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3a1e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3a1e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c3a1e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3a1e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c3a1e-133">進入</span><span class="sxs-lookup"><span data-stu-id="c3a1e-133">Entry</span></span> | <span data-ttu-id="c3a1e-134">值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3a1e-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3a1e-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3a1e-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3a1e-137">System-Only</span></span>            | <span data-ttu-id="c3a1e-138">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-138">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c3a1e-140">對</span><span class="sxs-lookup"><span data-stu-id="c3a1e-140">True</span></span>                                                                |
| <span data-ttu-id="c3a1e-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3a1e-141">Is Indexed</span></span>             | <span data-ttu-id="c3a1e-142">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-142">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3a1e-143">In Global Catalog</span></span>      | <span data-ttu-id="c3a1e-144">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-144">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3a1e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3a1e-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3a1e-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c3a1e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3a1e-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3a1e-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-149">Search-Flags</span></span>           | <span data-ttu-id="c3a1e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3a1e-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="c3a1e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-151">System-Flags</span></span>           | <span data-ttu-id="c3a1e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3a1e-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="c3a1e-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3a1e-153">Classes used in</span></span>        | [<span data-ttu-id="c3a1e-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c3a1e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3a1e-155">Windows Server 2003</span></span>



| <span data-ttu-id="c3a1e-156">進入</span><span class="sxs-lookup"><span data-stu-id="c3a1e-156">Entry</span></span> | <span data-ttu-id="c3a1e-157">值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3a1e-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3a1e-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3a1e-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3a1e-160">System-Only</span></span>            | <span data-ttu-id="c3a1e-161">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-161">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c3a1e-163">對</span><span class="sxs-lookup"><span data-stu-id="c3a1e-163">True</span></span>                                                                |
| <span data-ttu-id="c3a1e-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3a1e-164">Is Indexed</span></span>             | <span data-ttu-id="c3a1e-165">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-165">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3a1e-166">In Global Catalog</span></span>      | <span data-ttu-id="c3a1e-167">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-167">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3a1e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3a1e-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3a1e-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c3a1e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3a1e-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3a1e-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-172">Search-Flags</span></span>           | <span data-ttu-id="c3a1e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3a1e-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="c3a1e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-174">System-Flags</span></span>           | <span data-ttu-id="c3a1e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3a1e-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="c3a1e-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3a1e-176">Classes used in</span></span>        | [<span data-ttu-id="c3a1e-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3a1e-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3a1e-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3a1e-179">進入</span><span class="sxs-lookup"><span data-stu-id="c3a1e-179">Entry</span></span> | <span data-ttu-id="c3a1e-180">值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3a1e-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3a1e-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3a1e-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3a1e-183">System-Only</span></span>            | <span data-ttu-id="c3a1e-184">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-184">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c3a1e-186">對</span><span class="sxs-lookup"><span data-stu-id="c3a1e-186">True</span></span>                                                                |
| <span data-ttu-id="c3a1e-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3a1e-187">Is Indexed</span></span>             | <span data-ttu-id="c3a1e-188">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-188">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3a1e-189">In Global Catalog</span></span>      | <span data-ttu-id="c3a1e-190">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-190">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3a1e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3a1e-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3a1e-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c3a1e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3a1e-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3a1e-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-195">Search-Flags</span></span>           | <span data-ttu-id="c3a1e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3a1e-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="c3a1e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-197">System-Flags</span></span>           | <span data-ttu-id="c3a1e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3a1e-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="c3a1e-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3a1e-199">Classes used in</span></span>        | [<span data-ttu-id="c3a1e-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3a1e-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3a1e-201">Windows Server 2008</span></span>



| <span data-ttu-id="c3a1e-202">進入</span><span class="sxs-lookup"><span data-stu-id="c3a1e-202">Entry</span></span> | <span data-ttu-id="c3a1e-203">值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3a1e-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3a1e-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3a1e-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3a1e-206">System-Only</span></span>            | <span data-ttu-id="c3a1e-207">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-207">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c3a1e-209">對</span><span class="sxs-lookup"><span data-stu-id="c3a1e-209">True</span></span>                                                                |
| <span data-ttu-id="c3a1e-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3a1e-210">Is Indexed</span></span>             | <span data-ttu-id="c3a1e-211">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-211">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3a1e-212">In Global Catalog</span></span>      | <span data-ttu-id="c3a1e-213">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-213">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3a1e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3a1e-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3a1e-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c3a1e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3a1e-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3a1e-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-218">Search-Flags</span></span>           | <span data-ttu-id="c3a1e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3a1e-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="c3a1e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-220">System-Flags</span></span>           | <span data-ttu-id="c3a1e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3a1e-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="c3a1e-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3a1e-222">Classes used in</span></span>        | [<span data-ttu-id="c3a1e-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3a1e-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3a1e-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3a1e-225">進入</span><span class="sxs-lookup"><span data-stu-id="c3a1e-225">Entry</span></span> | <span data-ttu-id="c3a1e-226">值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3a1e-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3a1e-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3a1e-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3a1e-229">System-Only</span></span>            | <span data-ttu-id="c3a1e-230">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-230">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c3a1e-232">對</span><span class="sxs-lookup"><span data-stu-id="c3a1e-232">True</span></span>                                                                |
| <span data-ttu-id="c3a1e-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3a1e-233">Is Indexed</span></span>             | <span data-ttu-id="c3a1e-234">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-234">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3a1e-235">In Global Catalog</span></span>      | <span data-ttu-id="c3a1e-236">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-236">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3a1e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3a1e-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3a1e-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c3a1e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3a1e-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3a1e-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-241">Search-Flags</span></span>           | <span data-ttu-id="c3a1e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3a1e-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="c3a1e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-243">System-Flags</span></span>           | <span data-ttu-id="c3a1e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3a1e-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="c3a1e-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3a1e-245">Classes used in</span></span>        | [<span data-ttu-id="c3a1e-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3a1e-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3a1e-247">Windows Server 2012</span></span>



| <span data-ttu-id="c3a1e-248">進入</span><span class="sxs-lookup"><span data-stu-id="c3a1e-248">Entry</span></span> | <span data-ttu-id="c3a1e-249">值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c3a1e-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c3a1e-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3a1e-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c3a1e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3a1e-252">System-Only</span></span>            | <span data-ttu-id="c3a1e-253">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-253">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c3a1e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c3a1e-255">對</span><span class="sxs-lookup"><span data-stu-id="c3a1e-255">True</span></span>                                                                |
| <span data-ttu-id="c3a1e-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c3a1e-256">Is Indexed</span></span>             | <span data-ttu-id="c3a1e-257">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-257">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c3a1e-258">In Global Catalog</span></span>      | <span data-ttu-id="c3a1e-259">否</span><span class="sxs-lookup"><span data-stu-id="c3a1e-259">False</span></span>                                                               |
| <span data-ttu-id="c3a1e-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c3a1e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3a1e-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c3a1e-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c3a1e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3a1e-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3a1e-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c3a1e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-264">Search-Flags</span></span>           | <span data-ttu-id="c3a1e-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3a1e-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="c3a1e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3a1e-266">System-Flags</span></span>           | <span data-ttu-id="c3a1e-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3a1e-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="c3a1e-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c3a1e-268">Classes used in</span></span>        | [<span data-ttu-id="c3a1e-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c3a1e-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





