---
title: AllowKnownPullSubscription 屬性
description: 如果發行集允許已註冊的訂閱者訂閱，則為 True。
ms.assetid: be3b618e-bdf5-4bb4-ac4d-51dc97e73408
ms.tgt_platform: multiple
keywords:
- AllowKnownPullSubscription 屬性 AD 架構
- AllowKnownPullSubscription 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-AllowKnownPullSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07789bf68f470db69219765628ebc82b2014428
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845560"
---
# <a name="ms-sql-allowknownpullsubscription-attribute"></a><span data-ttu-id="7d071-105">AllowKnownPullSubscription 屬性</span><span class="sxs-lookup"><span data-stu-id="7d071-105">MS-SQL-AllowKnownPullSubscription attribute</span></span>

<span data-ttu-id="7d071-106">如果發行集允許已註冊的訂閱者訂閱，則為 True。</span><span class="sxs-lookup"><span data-stu-id="7d071-106">True if the publication allows registered subscribers to subscribe.</span></span>



| <span data-ttu-id="7d071-107">進入</span><span class="sxs-lookup"><span data-stu-id="7d071-107">Entry</span></span> | <span data-ttu-id="7d071-108">值</span><span class="sxs-lookup"><span data-stu-id="7d071-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7d071-109">CN</span><span class="sxs-lookup"><span data-stu-id="7d071-109">CN</span></span>                | <span data-ttu-id="7d071-110">AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="7d071-110">MS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="7d071-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7d071-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7d071-112">AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="7d071-112">mS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="7d071-113">大小</span><span class="sxs-lookup"><span data-stu-id="7d071-113">Size</span></span>              | <span data-ttu-id="7d071-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="7d071-114">4 bytes</span></span>                              |
| <span data-ttu-id="7d071-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7d071-115">Update Privilege</span></span>  | <span data-ttu-id="7d071-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7d071-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7d071-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7d071-117">Update Frequency</span></span>  | <span data-ttu-id="7d071-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="7d071-118">When replication is setup.</span></span>           |
| <span data-ttu-id="7d071-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7d071-119">Attribute-Id</span></span>      | <span data-ttu-id="7d071-120">1.2.840.113556.1.4.1403</span><span class="sxs-lookup"><span data-stu-id="7d071-120">1.2.840.113556.1.4.1403</span></span>              |
| <span data-ttu-id="7d071-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7d071-121">System-Id-Guid</span></span>    | <span data-ttu-id="7d071-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="7d071-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="7d071-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d071-123">Syntax</span></span>            | [<span data-ttu-id="7d071-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7d071-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="7d071-125">實作</span><span class="sxs-lookup"><span data-stu-id="7d071-125">Implementations</span></span>

-   [<span data-ttu-id="7d071-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7d071-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7d071-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7d071-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7d071-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7d071-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7d071-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7d071-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7d071-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7d071-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7d071-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7d071-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7d071-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d071-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7d071-133">進入</span><span class="sxs-lookup"><span data-stu-id="7d071-133">Entry</span></span> | <span data-ttu-id="7d071-134">值</span><span class="sxs-lookup"><span data-stu-id="7d071-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7d071-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d071-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d071-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d071-137">System-Only</span></span>            | <span data-ttu-id="7d071-138">否</span><span class="sxs-lookup"><span data-stu-id="7d071-138">False</span></span>                                                               |
| <span data-ttu-id="7d071-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d071-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7d071-140">對</span><span class="sxs-lookup"><span data-stu-id="7d071-140">True</span></span>                                                                |
| <span data-ttu-id="7d071-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d071-141">Is Indexed</span></span>             | <span data-ttu-id="7d071-142">否</span><span class="sxs-lookup"><span data-stu-id="7d071-142">False</span></span>                                                               |
| <span data-ttu-id="7d071-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d071-143">In Global Catalog</span></span>      | <span data-ttu-id="7d071-144">否</span><span class="sxs-lookup"><span data-stu-id="7d071-144">False</span></span>                                                               |
| <span data-ttu-id="7d071-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d071-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d071-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d071-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7d071-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d071-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d071-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-149">Search-Flags</span></span>           | <span data-ttu-id="7d071-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d071-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="7d071-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-151">System-Flags</span></span>           | <span data-ttu-id="7d071-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d071-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="7d071-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d071-153">Classes used in</span></span>        | [<span data-ttu-id="7d071-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7d071-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7d071-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d071-155">Windows Server 2003</span></span>



| <span data-ttu-id="7d071-156">進入</span><span class="sxs-lookup"><span data-stu-id="7d071-156">Entry</span></span> | <span data-ttu-id="7d071-157">值</span><span class="sxs-lookup"><span data-stu-id="7d071-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7d071-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d071-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d071-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d071-160">System-Only</span></span>            | <span data-ttu-id="7d071-161">否</span><span class="sxs-lookup"><span data-stu-id="7d071-161">False</span></span>                                                               |
| <span data-ttu-id="7d071-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d071-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7d071-163">對</span><span class="sxs-lookup"><span data-stu-id="7d071-163">True</span></span>                                                                |
| <span data-ttu-id="7d071-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d071-164">Is Indexed</span></span>             | <span data-ttu-id="7d071-165">否</span><span class="sxs-lookup"><span data-stu-id="7d071-165">False</span></span>                                                               |
| <span data-ttu-id="7d071-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d071-166">In Global Catalog</span></span>      | <span data-ttu-id="7d071-167">否</span><span class="sxs-lookup"><span data-stu-id="7d071-167">False</span></span>                                                               |
| <span data-ttu-id="7d071-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d071-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d071-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d071-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7d071-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d071-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d071-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-172">Search-Flags</span></span>           | <span data-ttu-id="7d071-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d071-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="7d071-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-174">System-Flags</span></span>           | <span data-ttu-id="7d071-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d071-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="7d071-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d071-176">Classes used in</span></span>        | [<span data-ttu-id="7d071-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7d071-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7d071-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7d071-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7d071-179">進入</span><span class="sxs-lookup"><span data-stu-id="7d071-179">Entry</span></span> | <span data-ttu-id="7d071-180">值</span><span class="sxs-lookup"><span data-stu-id="7d071-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7d071-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d071-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d071-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d071-183">System-Only</span></span>            | <span data-ttu-id="7d071-184">否</span><span class="sxs-lookup"><span data-stu-id="7d071-184">False</span></span>                                                               |
| <span data-ttu-id="7d071-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d071-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7d071-186">對</span><span class="sxs-lookup"><span data-stu-id="7d071-186">True</span></span>                                                                |
| <span data-ttu-id="7d071-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d071-187">Is Indexed</span></span>             | <span data-ttu-id="7d071-188">否</span><span class="sxs-lookup"><span data-stu-id="7d071-188">False</span></span>                                                               |
| <span data-ttu-id="7d071-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d071-189">In Global Catalog</span></span>      | <span data-ttu-id="7d071-190">否</span><span class="sxs-lookup"><span data-stu-id="7d071-190">False</span></span>                                                               |
| <span data-ttu-id="7d071-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d071-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d071-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d071-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7d071-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d071-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d071-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-195">Search-Flags</span></span>           | <span data-ttu-id="7d071-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d071-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="7d071-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-197">System-Flags</span></span>           | <span data-ttu-id="7d071-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d071-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="7d071-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d071-199">Classes used in</span></span>        | [<span data-ttu-id="7d071-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7d071-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7d071-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d071-201">Windows Server 2008</span></span>



| <span data-ttu-id="7d071-202">進入</span><span class="sxs-lookup"><span data-stu-id="7d071-202">Entry</span></span> | <span data-ttu-id="7d071-203">值</span><span class="sxs-lookup"><span data-stu-id="7d071-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7d071-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d071-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d071-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d071-206">System-Only</span></span>            | <span data-ttu-id="7d071-207">否</span><span class="sxs-lookup"><span data-stu-id="7d071-207">False</span></span>                                                               |
| <span data-ttu-id="7d071-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d071-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7d071-209">對</span><span class="sxs-lookup"><span data-stu-id="7d071-209">True</span></span>                                                                |
| <span data-ttu-id="7d071-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d071-210">Is Indexed</span></span>             | <span data-ttu-id="7d071-211">否</span><span class="sxs-lookup"><span data-stu-id="7d071-211">False</span></span>                                                               |
| <span data-ttu-id="7d071-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d071-212">In Global Catalog</span></span>      | <span data-ttu-id="7d071-213">否</span><span class="sxs-lookup"><span data-stu-id="7d071-213">False</span></span>                                                               |
| <span data-ttu-id="7d071-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d071-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d071-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d071-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7d071-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d071-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d071-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-218">Search-Flags</span></span>           | <span data-ttu-id="7d071-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d071-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="7d071-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-220">System-Flags</span></span>           | <span data-ttu-id="7d071-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d071-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="7d071-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d071-222">Classes used in</span></span>        | [<span data-ttu-id="7d071-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7d071-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7d071-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d071-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7d071-225">進入</span><span class="sxs-lookup"><span data-stu-id="7d071-225">Entry</span></span> | <span data-ttu-id="7d071-226">值</span><span class="sxs-lookup"><span data-stu-id="7d071-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7d071-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d071-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d071-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d071-229">System-Only</span></span>            | <span data-ttu-id="7d071-230">否</span><span class="sxs-lookup"><span data-stu-id="7d071-230">False</span></span>                                                               |
| <span data-ttu-id="7d071-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d071-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7d071-232">對</span><span class="sxs-lookup"><span data-stu-id="7d071-232">True</span></span>                                                                |
| <span data-ttu-id="7d071-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d071-233">Is Indexed</span></span>             | <span data-ttu-id="7d071-234">否</span><span class="sxs-lookup"><span data-stu-id="7d071-234">False</span></span>                                                               |
| <span data-ttu-id="7d071-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d071-235">In Global Catalog</span></span>      | <span data-ttu-id="7d071-236">否</span><span class="sxs-lookup"><span data-stu-id="7d071-236">False</span></span>                                                               |
| <span data-ttu-id="7d071-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d071-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d071-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d071-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7d071-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d071-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d071-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-241">Search-Flags</span></span>           | <span data-ttu-id="7d071-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d071-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="7d071-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-243">System-Flags</span></span>           | <span data-ttu-id="7d071-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d071-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="7d071-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d071-245">Classes used in</span></span>        | [<span data-ttu-id="7d071-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7d071-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7d071-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d071-247">Windows Server 2012</span></span>



| <span data-ttu-id="7d071-248">進入</span><span class="sxs-lookup"><span data-stu-id="7d071-248">Entry</span></span> | <span data-ttu-id="7d071-249">值</span><span class="sxs-lookup"><span data-stu-id="7d071-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7d071-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7d071-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d071-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7d071-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d071-252">System-Only</span></span>            | <span data-ttu-id="7d071-253">否</span><span class="sxs-lookup"><span data-stu-id="7d071-253">False</span></span>                                                               |
| <span data-ttu-id="7d071-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7d071-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7d071-255">對</span><span class="sxs-lookup"><span data-stu-id="7d071-255">True</span></span>                                                                |
| <span data-ttu-id="7d071-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7d071-256">Is Indexed</span></span>             | <span data-ttu-id="7d071-257">否</span><span class="sxs-lookup"><span data-stu-id="7d071-257">False</span></span>                                                               |
| <span data-ttu-id="7d071-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7d071-258">In Global Catalog</span></span>      | <span data-ttu-id="7d071-259">否</span><span class="sxs-lookup"><span data-stu-id="7d071-259">False</span></span>                                                               |
| <span data-ttu-id="7d071-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7d071-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d071-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7d071-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7d071-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d071-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d071-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7d071-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-264">Search-Flags</span></span>           | <span data-ttu-id="7d071-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d071-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="7d071-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d071-266">System-Flags</span></span>           | <span data-ttu-id="7d071-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d071-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="7d071-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7d071-268">Classes used in</span></span>        | [<span data-ttu-id="7d071-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="7d071-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





