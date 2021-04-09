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
# <a name="ms-sql-allowknownpullsubscription-attribute"></a><span data-ttu-id="ca6da-105">AllowKnownPullSubscription 屬性</span><span class="sxs-lookup"><span data-stu-id="ca6da-105">MS-SQL-AllowKnownPullSubscription attribute</span></span>

<span data-ttu-id="ca6da-106">如果發行集允許已註冊的訂閱者訂閱，則為 True。</span><span class="sxs-lookup"><span data-stu-id="ca6da-106">True if the publication allows registered subscribers to subscribe.</span></span>



| <span data-ttu-id="ca6da-107">進入</span><span class="sxs-lookup"><span data-stu-id="ca6da-107">Entry</span></span> | <span data-ttu-id="ca6da-108">值</span><span class="sxs-lookup"><span data-stu-id="ca6da-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ca6da-109">CN</span><span class="sxs-lookup"><span data-stu-id="ca6da-109">CN</span></span>                | <span data-ttu-id="ca6da-110">AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="ca6da-110">MS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="ca6da-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ca6da-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ca6da-112">AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="ca6da-112">mS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="ca6da-113">大小</span><span class="sxs-lookup"><span data-stu-id="ca6da-113">Size</span></span>              | <span data-ttu-id="ca6da-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ca6da-114">4 bytes</span></span>                              |
| <span data-ttu-id="ca6da-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ca6da-115">Update Privilege</span></span>  | <span data-ttu-id="ca6da-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ca6da-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ca6da-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ca6da-117">Update Frequency</span></span>  | <span data-ttu-id="ca6da-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="ca6da-118">When replication is setup.</span></span>           |
| <span data-ttu-id="ca6da-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ca6da-119">Attribute-Id</span></span>      | <span data-ttu-id="ca6da-120">1.2.840.113556.1.4.1403</span><span class="sxs-lookup"><span data-stu-id="ca6da-120">1.2.840.113556.1.4.1403</span></span>              |
| <span data-ttu-id="ca6da-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ca6da-121">System-Id-Guid</span></span>    | <span data-ttu-id="ca6da-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ca6da-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="ca6da-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca6da-123">Syntax</span></span>            | [<span data-ttu-id="ca6da-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ca6da-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="ca6da-125">實作</span><span class="sxs-lookup"><span data-stu-id="ca6da-125">Implementations</span></span>

-   [<span data-ttu-id="ca6da-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ca6da-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ca6da-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ca6da-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ca6da-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ca6da-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ca6da-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ca6da-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ca6da-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ca6da-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ca6da-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ca6da-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ca6da-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ca6da-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ca6da-133">進入</span><span class="sxs-lookup"><span data-stu-id="ca6da-133">Entry</span></span> | <span data-ttu-id="ca6da-134">值</span><span class="sxs-lookup"><span data-stu-id="ca6da-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ca6da-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ca6da-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6da-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6da-137">System-Only</span></span>            | <span data-ttu-id="ca6da-138">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-138">False</span></span>                                                               |
| <span data-ttu-id="ca6da-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ca6da-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6da-140">對</span><span class="sxs-lookup"><span data-stu-id="ca6da-140">True</span></span>                                                                |
| <span data-ttu-id="ca6da-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ca6da-141">Is Indexed</span></span>             | <span data-ttu-id="ca6da-142">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-142">False</span></span>                                                               |
| <span data-ttu-id="ca6da-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ca6da-143">In Global Catalog</span></span>      | <span data-ttu-id="ca6da-144">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-144">False</span></span>                                                               |
| <span data-ttu-id="ca6da-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ca6da-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6da-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ca6da-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ca6da-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6da-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6da-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-149">Search-Flags</span></span>           | <span data-ttu-id="ca6da-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6da-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="ca6da-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-151">System-Flags</span></span>           | <span data-ttu-id="ca6da-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6da-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="ca6da-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ca6da-153">Classes used in</span></span>        | [<span data-ttu-id="ca6da-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ca6da-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ca6da-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca6da-155">Windows Server 2003</span></span>



| <span data-ttu-id="ca6da-156">進入</span><span class="sxs-lookup"><span data-stu-id="ca6da-156">Entry</span></span> | <span data-ttu-id="ca6da-157">值</span><span class="sxs-lookup"><span data-stu-id="ca6da-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ca6da-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ca6da-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6da-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6da-160">System-Only</span></span>            | <span data-ttu-id="ca6da-161">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-161">False</span></span>                                                               |
| <span data-ttu-id="ca6da-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ca6da-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6da-163">對</span><span class="sxs-lookup"><span data-stu-id="ca6da-163">True</span></span>                                                                |
| <span data-ttu-id="ca6da-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ca6da-164">Is Indexed</span></span>             | <span data-ttu-id="ca6da-165">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-165">False</span></span>                                                               |
| <span data-ttu-id="ca6da-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ca6da-166">In Global Catalog</span></span>      | <span data-ttu-id="ca6da-167">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-167">False</span></span>                                                               |
| <span data-ttu-id="ca6da-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ca6da-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6da-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ca6da-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ca6da-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6da-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6da-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-172">Search-Flags</span></span>           | <span data-ttu-id="ca6da-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6da-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="ca6da-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-174">System-Flags</span></span>           | <span data-ttu-id="ca6da-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6da-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="ca6da-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ca6da-176">Classes used in</span></span>        | [<span data-ttu-id="ca6da-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ca6da-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ca6da-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ca6da-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ca6da-179">進入</span><span class="sxs-lookup"><span data-stu-id="ca6da-179">Entry</span></span> | <span data-ttu-id="ca6da-180">值</span><span class="sxs-lookup"><span data-stu-id="ca6da-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ca6da-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ca6da-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6da-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6da-183">System-Only</span></span>            | <span data-ttu-id="ca6da-184">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-184">False</span></span>                                                               |
| <span data-ttu-id="ca6da-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ca6da-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6da-186">對</span><span class="sxs-lookup"><span data-stu-id="ca6da-186">True</span></span>                                                                |
| <span data-ttu-id="ca6da-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ca6da-187">Is Indexed</span></span>             | <span data-ttu-id="ca6da-188">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-188">False</span></span>                                                               |
| <span data-ttu-id="ca6da-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ca6da-189">In Global Catalog</span></span>      | <span data-ttu-id="ca6da-190">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-190">False</span></span>                                                               |
| <span data-ttu-id="ca6da-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ca6da-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6da-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ca6da-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ca6da-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6da-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6da-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-195">Search-Flags</span></span>           | <span data-ttu-id="ca6da-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6da-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="ca6da-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-197">System-Flags</span></span>           | <span data-ttu-id="ca6da-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6da-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="ca6da-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ca6da-199">Classes used in</span></span>        | [<span data-ttu-id="ca6da-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ca6da-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ca6da-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca6da-201">Windows Server 2008</span></span>



| <span data-ttu-id="ca6da-202">進入</span><span class="sxs-lookup"><span data-stu-id="ca6da-202">Entry</span></span> | <span data-ttu-id="ca6da-203">值</span><span class="sxs-lookup"><span data-stu-id="ca6da-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ca6da-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ca6da-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6da-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6da-206">System-Only</span></span>            | <span data-ttu-id="ca6da-207">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-207">False</span></span>                                                               |
| <span data-ttu-id="ca6da-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ca6da-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6da-209">對</span><span class="sxs-lookup"><span data-stu-id="ca6da-209">True</span></span>                                                                |
| <span data-ttu-id="ca6da-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ca6da-210">Is Indexed</span></span>             | <span data-ttu-id="ca6da-211">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-211">False</span></span>                                                               |
| <span data-ttu-id="ca6da-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ca6da-212">In Global Catalog</span></span>      | <span data-ttu-id="ca6da-213">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-213">False</span></span>                                                               |
| <span data-ttu-id="ca6da-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ca6da-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6da-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ca6da-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ca6da-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6da-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6da-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-218">Search-Flags</span></span>           | <span data-ttu-id="ca6da-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6da-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="ca6da-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-220">System-Flags</span></span>           | <span data-ttu-id="ca6da-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6da-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="ca6da-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ca6da-222">Classes used in</span></span>        | [<span data-ttu-id="ca6da-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ca6da-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ca6da-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca6da-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ca6da-225">進入</span><span class="sxs-lookup"><span data-stu-id="ca6da-225">Entry</span></span> | <span data-ttu-id="ca6da-226">值</span><span class="sxs-lookup"><span data-stu-id="ca6da-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ca6da-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ca6da-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6da-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6da-229">System-Only</span></span>            | <span data-ttu-id="ca6da-230">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-230">False</span></span>                                                               |
| <span data-ttu-id="ca6da-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ca6da-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6da-232">對</span><span class="sxs-lookup"><span data-stu-id="ca6da-232">True</span></span>                                                                |
| <span data-ttu-id="ca6da-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ca6da-233">Is Indexed</span></span>             | <span data-ttu-id="ca6da-234">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-234">False</span></span>                                                               |
| <span data-ttu-id="ca6da-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ca6da-235">In Global Catalog</span></span>      | <span data-ttu-id="ca6da-236">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-236">False</span></span>                                                               |
| <span data-ttu-id="ca6da-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ca6da-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6da-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ca6da-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ca6da-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6da-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6da-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-241">Search-Flags</span></span>           | <span data-ttu-id="ca6da-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6da-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="ca6da-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-243">System-Flags</span></span>           | <span data-ttu-id="ca6da-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6da-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="ca6da-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ca6da-245">Classes used in</span></span>        | [<span data-ttu-id="ca6da-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ca6da-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ca6da-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca6da-247">Windows Server 2012</span></span>



| <span data-ttu-id="ca6da-248">進入</span><span class="sxs-lookup"><span data-stu-id="ca6da-248">Entry</span></span> | <span data-ttu-id="ca6da-249">值</span><span class="sxs-lookup"><span data-stu-id="ca6da-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ca6da-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ca6da-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca6da-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ca6da-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca6da-252">System-Only</span></span>            | <span data-ttu-id="ca6da-253">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-253">False</span></span>                                                               |
| <span data-ttu-id="ca6da-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ca6da-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ca6da-255">對</span><span class="sxs-lookup"><span data-stu-id="ca6da-255">True</span></span>                                                                |
| <span data-ttu-id="ca6da-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ca6da-256">Is Indexed</span></span>             | <span data-ttu-id="ca6da-257">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-257">False</span></span>                                                               |
| <span data-ttu-id="ca6da-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ca6da-258">In Global Catalog</span></span>      | <span data-ttu-id="ca6da-259">否</span><span class="sxs-lookup"><span data-stu-id="ca6da-259">False</span></span>                                                               |
| <span data-ttu-id="ca6da-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ca6da-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca6da-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ca6da-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ca6da-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca6da-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca6da-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ca6da-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-264">Search-Flags</span></span>           | <span data-ttu-id="ca6da-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ca6da-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="ca6da-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca6da-266">System-Flags</span></span>           | <span data-ttu-id="ca6da-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca6da-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="ca6da-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ca6da-268">Classes used in</span></span>        | [<span data-ttu-id="ca6da-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ca6da-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





