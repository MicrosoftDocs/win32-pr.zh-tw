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
# <a name="ms-sql-allowknownpullsubscription-attribute"></a><span data-ttu-id="d4f1f-105">AllowKnownPullSubscription 屬性</span><span class="sxs-lookup"><span data-stu-id="d4f1f-105">MS-SQL-AllowKnownPullSubscription attribute</span></span>

<span data-ttu-id="d4f1f-106">如果發行集允許已註冊的訂閱者訂閱，則為 True。</span><span class="sxs-lookup"><span data-stu-id="d4f1f-106">True if the publication allows registered subscribers to subscribe.</span></span>



| <span data-ttu-id="d4f1f-107">進入</span><span class="sxs-lookup"><span data-stu-id="d4f1f-107">Entry</span></span> | <span data-ttu-id="d4f1f-108">值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d4f1f-109">CN</span><span class="sxs-lookup"><span data-stu-id="d4f1f-109">CN</span></span>                | <span data-ttu-id="d4f1f-110">AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f1f-110">MS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="d4f1f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d4f1f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d4f1f-112">AllowKnownPullSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f1f-112">mS-SQL-AllowKnownPullSubscription</span></span>    |
| <span data-ttu-id="d4f1f-113">大小</span><span class="sxs-lookup"><span data-stu-id="d4f1f-113">Size</span></span>              | <span data-ttu-id="d4f1f-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="d4f1f-114">4 bytes</span></span>                              |
| <span data-ttu-id="d4f1f-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d4f1f-115">Update Privilege</span></span>  | <span data-ttu-id="d4f1f-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="d4f1f-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="d4f1f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d4f1f-117">Update Frequency</span></span>  | <span data-ttu-id="d4f1f-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="d4f1f-118">When replication is setup.</span></span>           |
| <span data-ttu-id="d4f1f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d4f1f-119">Attribute-Id</span></span>      | <span data-ttu-id="d4f1f-120">1.2.840.113556.1.4.1403</span><span class="sxs-lookup"><span data-stu-id="d4f1f-120">1.2.840.113556.1.4.1403</span></span>              |
| <span data-ttu-id="d4f1f-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d4f1f-121">System-Id-Guid</span></span>    | <span data-ttu-id="d4f1f-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d4f1f-122">c3bb7054-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="d4f1f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4f1f-123">Syntax</span></span>            | [<span data-ttu-id="d4f1f-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="d4f1f-125">實作</span><span class="sxs-lookup"><span data-stu-id="d4f1f-125">Implementations</span></span>

-   [<span data-ttu-id="d4f1f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d4f1f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d4f1f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d4f1f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d4f1f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d4f1f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d4f1f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4f1f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d4f1f-133">進入</span><span class="sxs-lookup"><span data-stu-id="d4f1f-133">Entry</span></span> | <span data-ttu-id="d4f1f-134">值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4f1f-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4f1f-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4f1f-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4f1f-137">System-Only</span></span>            | <span data-ttu-id="d4f1f-138">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-138">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d4f1f-140">對</span><span class="sxs-lookup"><span data-stu-id="d4f1f-140">True</span></span>                                                                |
| <span data-ttu-id="d4f1f-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4f1f-141">Is Indexed</span></span>             | <span data-ttu-id="d4f1f-142">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-142">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4f1f-143">In Global Catalog</span></span>      | <span data-ttu-id="d4f1f-144">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-144">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4f1f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4f1f-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4f1f-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d4f1f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4f1f-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4f1f-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-149">Search-Flags</span></span>           | <span data-ttu-id="d4f1f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4f1f-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="d4f1f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-151">System-Flags</span></span>           | <span data-ttu-id="d4f1f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4f1f-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="d4f1f-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4f1f-153">Classes used in</span></span>        | [<span data-ttu-id="d4f1f-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d4f1f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4f1f-155">Windows Server 2003</span></span>



| <span data-ttu-id="d4f1f-156">進入</span><span class="sxs-lookup"><span data-stu-id="d4f1f-156">Entry</span></span> | <span data-ttu-id="d4f1f-157">值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4f1f-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4f1f-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4f1f-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4f1f-160">System-Only</span></span>            | <span data-ttu-id="d4f1f-161">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-161">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d4f1f-163">對</span><span class="sxs-lookup"><span data-stu-id="d4f1f-163">True</span></span>                                                                |
| <span data-ttu-id="d4f1f-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4f1f-164">Is Indexed</span></span>             | <span data-ttu-id="d4f1f-165">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-165">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4f1f-166">In Global Catalog</span></span>      | <span data-ttu-id="d4f1f-167">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-167">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4f1f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4f1f-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4f1f-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d4f1f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4f1f-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4f1f-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-172">Search-Flags</span></span>           | <span data-ttu-id="d4f1f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4f1f-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="d4f1f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-174">System-Flags</span></span>           | <span data-ttu-id="d4f1f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4f1f-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="d4f1f-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4f1f-176">Classes used in</span></span>        | [<span data-ttu-id="d4f1f-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d4f1f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4f1f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d4f1f-179">進入</span><span class="sxs-lookup"><span data-stu-id="d4f1f-179">Entry</span></span> | <span data-ttu-id="d4f1f-180">值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4f1f-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4f1f-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4f1f-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4f1f-183">System-Only</span></span>            | <span data-ttu-id="d4f1f-184">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-184">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d4f1f-186">對</span><span class="sxs-lookup"><span data-stu-id="d4f1f-186">True</span></span>                                                                |
| <span data-ttu-id="d4f1f-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4f1f-187">Is Indexed</span></span>             | <span data-ttu-id="d4f1f-188">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-188">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4f1f-189">In Global Catalog</span></span>      | <span data-ttu-id="d4f1f-190">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-190">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4f1f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4f1f-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4f1f-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d4f1f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4f1f-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4f1f-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-195">Search-Flags</span></span>           | <span data-ttu-id="d4f1f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4f1f-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="d4f1f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-197">System-Flags</span></span>           | <span data-ttu-id="d4f1f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4f1f-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="d4f1f-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4f1f-199">Classes used in</span></span>        | [<span data-ttu-id="d4f1f-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d4f1f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4f1f-201">Windows Server 2008</span></span>



| <span data-ttu-id="d4f1f-202">進入</span><span class="sxs-lookup"><span data-stu-id="d4f1f-202">Entry</span></span> | <span data-ttu-id="d4f1f-203">值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4f1f-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4f1f-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4f1f-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4f1f-206">System-Only</span></span>            | <span data-ttu-id="d4f1f-207">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-207">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d4f1f-209">對</span><span class="sxs-lookup"><span data-stu-id="d4f1f-209">True</span></span>                                                                |
| <span data-ttu-id="d4f1f-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4f1f-210">Is Indexed</span></span>             | <span data-ttu-id="d4f1f-211">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-211">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4f1f-212">In Global Catalog</span></span>      | <span data-ttu-id="d4f1f-213">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-213">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4f1f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4f1f-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4f1f-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d4f1f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4f1f-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4f1f-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-218">Search-Flags</span></span>           | <span data-ttu-id="d4f1f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4f1f-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="d4f1f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-220">System-Flags</span></span>           | <span data-ttu-id="d4f1f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4f1f-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="d4f1f-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4f1f-222">Classes used in</span></span>        | [<span data-ttu-id="d4f1f-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d4f1f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4f1f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d4f1f-225">進入</span><span class="sxs-lookup"><span data-stu-id="d4f1f-225">Entry</span></span> | <span data-ttu-id="d4f1f-226">值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4f1f-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4f1f-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4f1f-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4f1f-229">System-Only</span></span>            | <span data-ttu-id="d4f1f-230">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-230">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d4f1f-232">對</span><span class="sxs-lookup"><span data-stu-id="d4f1f-232">True</span></span>                                                                |
| <span data-ttu-id="d4f1f-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4f1f-233">Is Indexed</span></span>             | <span data-ttu-id="d4f1f-234">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-234">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4f1f-235">In Global Catalog</span></span>      | <span data-ttu-id="d4f1f-236">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-236">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4f1f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4f1f-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4f1f-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d4f1f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4f1f-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4f1f-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-241">Search-Flags</span></span>           | <span data-ttu-id="d4f1f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4f1f-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="d4f1f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-243">System-Flags</span></span>           | <span data-ttu-id="d4f1f-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4f1f-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="d4f1f-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4f1f-245">Classes used in</span></span>        | [<span data-ttu-id="d4f1f-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d4f1f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4f1f-247">Windows Server 2012</span></span>



| <span data-ttu-id="d4f1f-248">進入</span><span class="sxs-lookup"><span data-stu-id="d4f1f-248">Entry</span></span> | <span data-ttu-id="d4f1f-249">值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4f1f-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4f1f-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4f1f-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d4f1f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4f1f-252">System-Only</span></span>            | <span data-ttu-id="d4f1f-253">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-253">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4f1f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d4f1f-255">對</span><span class="sxs-lookup"><span data-stu-id="d4f1f-255">True</span></span>                                                                |
| <span data-ttu-id="d4f1f-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4f1f-256">Is Indexed</span></span>             | <span data-ttu-id="d4f1f-257">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-257">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4f1f-258">In Global Catalog</span></span>      | <span data-ttu-id="d4f1f-259">否</span><span class="sxs-lookup"><span data-stu-id="d4f1f-259">False</span></span>                                                               |
| <span data-ttu-id="d4f1f-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4f1f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4f1f-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4f1f-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d4f1f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4f1f-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4f1f-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d4f1f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-264">Search-Flags</span></span>           | <span data-ttu-id="d4f1f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4f1f-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="d4f1f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4f1f-266">System-Flags</span></span>           | <span data-ttu-id="d4f1f-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4f1f-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="d4f1f-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4f1f-268">Classes used in</span></span>        | [<span data-ttu-id="d4f1f-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="d4f1f-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





