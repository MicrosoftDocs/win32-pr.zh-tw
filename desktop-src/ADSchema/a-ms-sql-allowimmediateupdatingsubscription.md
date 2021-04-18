---
title: AllowImmediateUpdatingSubscription 屬性
description: 如果發行集允許同步處理的交易更新訂閱，則為 True。
ms.assetid: 7efa4b8f-77ad-4f68-9852-7dac9f922d95
ms.tgt_platform: multiple
keywords:
- AllowImmediateUpdatingSubscription 屬性 AD 架構
- AllowImmediateUpdatingSubscription 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-AllowImmediateUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed7970aa4b4f26a7221ea9a0c3d4e279ddc5db1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509541"
---
# <a name="ms-sql-allowimmediateupdatingsubscription-attribute"></a><span data-ttu-id="9d263-105">AllowImmediateUpdatingSubscription 屬性</span><span class="sxs-lookup"><span data-stu-id="9d263-105">MS-SQL-AllowImmediateUpdatingSubscription attribute</span></span>

<span data-ttu-id="9d263-106">如果發行集允許同步處理的交易更新訂閱，則為 True。</span><span class="sxs-lookup"><span data-stu-id="9d263-106">True if the publication allows synchronized transaction updating subscriptions.</span></span>



| <span data-ttu-id="9d263-107">進入</span><span class="sxs-lookup"><span data-stu-id="9d263-107">Entry</span></span> | <span data-ttu-id="9d263-108">值</span><span class="sxs-lookup"><span data-stu-id="9d263-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="9d263-109">CN</span><span class="sxs-lookup"><span data-stu-id="9d263-109">CN</span></span>                | <span data-ttu-id="9d263-110">AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="9d263-110">MS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="9d263-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9d263-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9d263-112">AllowImmediateUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="9d263-112">mS-SQL-AllowImmediateUpdatingSubscription</span></span> |
| <span data-ttu-id="9d263-113">大小</span><span class="sxs-lookup"><span data-stu-id="9d263-113">Size</span></span>              | <span data-ttu-id="9d263-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="9d263-114">4 bytes</span></span>                                   |
| <span data-ttu-id="9d263-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9d263-115">Update Privilege</span></span>  | <span data-ttu-id="9d263-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9d263-116">This value is set by the system.</span></span>          |
| <span data-ttu-id="9d263-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9d263-117">Update Frequency</span></span>  | <span data-ttu-id="9d263-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="9d263-118">When replication is setup.</span></span>                |
| <span data-ttu-id="9d263-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9d263-119">Attribute-Id</span></span>      | <span data-ttu-id="9d263-120">1.2.840.113556.1.4.1404</span><span class="sxs-lookup"><span data-stu-id="9d263-120">1.2.840.113556.1.4.1404</span></span>                   |
| <span data-ttu-id="9d263-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9d263-121">System-Id-Guid</span></span>    | <span data-ttu-id="9d263-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9d263-122">c4186b6e-d34b-11d2-999a-0000f87a57d4</span></span>      |
| <span data-ttu-id="9d263-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d263-123">Syntax</span></span>            | [<span data-ttu-id="9d263-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9d263-124">**Boolean**</span></span>](s-boolean.md)              |



## <a name="implementations"></a><span data-ttu-id="9d263-125">實作</span><span class="sxs-lookup"><span data-stu-id="9d263-125">Implementations</span></span>

-   [<span data-ttu-id="9d263-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9d263-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9d263-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9d263-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9d263-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9d263-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9d263-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9d263-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9d263-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9d263-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9d263-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9d263-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9d263-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d263-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9d263-133">進入</span><span class="sxs-lookup"><span data-stu-id="9d263-133">Entry</span></span> | <span data-ttu-id="9d263-134">值</span><span class="sxs-lookup"><span data-stu-id="9d263-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9d263-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d263-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d263-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d263-137">System-Only</span></span>            | <span data-ttu-id="9d263-138">否</span><span class="sxs-lookup"><span data-stu-id="9d263-138">False</span></span>                                                               |
| <span data-ttu-id="9d263-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d263-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9d263-140">對</span><span class="sxs-lookup"><span data-stu-id="9d263-140">True</span></span>                                                                |
| <span data-ttu-id="9d263-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d263-141">Is Indexed</span></span>             | <span data-ttu-id="9d263-142">否</span><span class="sxs-lookup"><span data-stu-id="9d263-142">False</span></span>                                                               |
| <span data-ttu-id="9d263-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d263-143">In Global Catalog</span></span>      | <span data-ttu-id="9d263-144">否</span><span class="sxs-lookup"><span data-stu-id="9d263-144">False</span></span>                                                               |
| <span data-ttu-id="9d263-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d263-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d263-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d263-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9d263-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d263-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d263-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-149">Search-Flags</span></span>           | <span data-ttu-id="9d263-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d263-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="9d263-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-151">System-Flags</span></span>           | <span data-ttu-id="9d263-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d263-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="9d263-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d263-153">Classes used in</span></span>        | [<span data-ttu-id="9d263-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9d263-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9d263-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d263-155">Windows Server 2003</span></span>



| <span data-ttu-id="9d263-156">進入</span><span class="sxs-lookup"><span data-stu-id="9d263-156">Entry</span></span> | <span data-ttu-id="9d263-157">值</span><span class="sxs-lookup"><span data-stu-id="9d263-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9d263-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d263-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d263-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d263-160">System-Only</span></span>            | <span data-ttu-id="9d263-161">否</span><span class="sxs-lookup"><span data-stu-id="9d263-161">False</span></span>                                                               |
| <span data-ttu-id="9d263-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d263-162">Is-Single-Valued</span></span>       | <span data-ttu-id="9d263-163">對</span><span class="sxs-lookup"><span data-stu-id="9d263-163">True</span></span>                                                                |
| <span data-ttu-id="9d263-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d263-164">Is Indexed</span></span>             | <span data-ttu-id="9d263-165">否</span><span class="sxs-lookup"><span data-stu-id="9d263-165">False</span></span>                                                               |
| <span data-ttu-id="9d263-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d263-166">In Global Catalog</span></span>      | <span data-ttu-id="9d263-167">否</span><span class="sxs-lookup"><span data-stu-id="9d263-167">False</span></span>                                                               |
| <span data-ttu-id="9d263-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d263-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d263-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d263-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9d263-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d263-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d263-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-172">Search-Flags</span></span>           | <span data-ttu-id="9d263-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d263-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="9d263-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-174">System-Flags</span></span>           | <span data-ttu-id="9d263-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d263-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="9d263-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d263-176">Classes used in</span></span>        | [<span data-ttu-id="9d263-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9d263-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9d263-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9d263-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9d263-179">進入</span><span class="sxs-lookup"><span data-stu-id="9d263-179">Entry</span></span> | <span data-ttu-id="9d263-180">值</span><span class="sxs-lookup"><span data-stu-id="9d263-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9d263-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d263-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d263-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d263-183">System-Only</span></span>            | <span data-ttu-id="9d263-184">否</span><span class="sxs-lookup"><span data-stu-id="9d263-184">False</span></span>                                                               |
| <span data-ttu-id="9d263-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d263-185">Is-Single-Valued</span></span>       | <span data-ttu-id="9d263-186">對</span><span class="sxs-lookup"><span data-stu-id="9d263-186">True</span></span>                                                                |
| <span data-ttu-id="9d263-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d263-187">Is Indexed</span></span>             | <span data-ttu-id="9d263-188">否</span><span class="sxs-lookup"><span data-stu-id="9d263-188">False</span></span>                                                               |
| <span data-ttu-id="9d263-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d263-189">In Global Catalog</span></span>      | <span data-ttu-id="9d263-190">否</span><span class="sxs-lookup"><span data-stu-id="9d263-190">False</span></span>                                                               |
| <span data-ttu-id="9d263-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d263-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d263-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d263-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9d263-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d263-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d263-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-195">Search-Flags</span></span>           | <span data-ttu-id="9d263-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d263-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="9d263-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-197">System-Flags</span></span>           | <span data-ttu-id="9d263-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d263-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="9d263-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d263-199">Classes used in</span></span>        | [<span data-ttu-id="9d263-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9d263-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9d263-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d263-201">Windows Server 2008</span></span>



| <span data-ttu-id="9d263-202">進入</span><span class="sxs-lookup"><span data-stu-id="9d263-202">Entry</span></span> | <span data-ttu-id="9d263-203">值</span><span class="sxs-lookup"><span data-stu-id="9d263-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9d263-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d263-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d263-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d263-206">System-Only</span></span>            | <span data-ttu-id="9d263-207">否</span><span class="sxs-lookup"><span data-stu-id="9d263-207">False</span></span>                                                               |
| <span data-ttu-id="9d263-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d263-208">Is-Single-Valued</span></span>       | <span data-ttu-id="9d263-209">對</span><span class="sxs-lookup"><span data-stu-id="9d263-209">True</span></span>                                                                |
| <span data-ttu-id="9d263-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d263-210">Is Indexed</span></span>             | <span data-ttu-id="9d263-211">否</span><span class="sxs-lookup"><span data-stu-id="9d263-211">False</span></span>                                                               |
| <span data-ttu-id="9d263-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d263-212">In Global Catalog</span></span>      | <span data-ttu-id="9d263-213">否</span><span class="sxs-lookup"><span data-stu-id="9d263-213">False</span></span>                                                               |
| <span data-ttu-id="9d263-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d263-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d263-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d263-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9d263-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d263-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d263-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-218">Search-Flags</span></span>           | <span data-ttu-id="9d263-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d263-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="9d263-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-220">System-Flags</span></span>           | <span data-ttu-id="9d263-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d263-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="9d263-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d263-222">Classes used in</span></span>        | [<span data-ttu-id="9d263-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9d263-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9d263-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d263-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9d263-225">進入</span><span class="sxs-lookup"><span data-stu-id="9d263-225">Entry</span></span> | <span data-ttu-id="9d263-226">值</span><span class="sxs-lookup"><span data-stu-id="9d263-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9d263-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d263-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d263-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d263-229">System-Only</span></span>            | <span data-ttu-id="9d263-230">否</span><span class="sxs-lookup"><span data-stu-id="9d263-230">False</span></span>                                                               |
| <span data-ttu-id="9d263-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d263-231">Is-Single-Valued</span></span>       | <span data-ttu-id="9d263-232">對</span><span class="sxs-lookup"><span data-stu-id="9d263-232">True</span></span>                                                                |
| <span data-ttu-id="9d263-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d263-233">Is Indexed</span></span>             | <span data-ttu-id="9d263-234">否</span><span class="sxs-lookup"><span data-stu-id="9d263-234">False</span></span>                                                               |
| <span data-ttu-id="9d263-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d263-235">In Global Catalog</span></span>      | <span data-ttu-id="9d263-236">否</span><span class="sxs-lookup"><span data-stu-id="9d263-236">False</span></span>                                                               |
| <span data-ttu-id="9d263-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d263-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d263-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d263-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9d263-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d263-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d263-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-241">Search-Flags</span></span>           | <span data-ttu-id="9d263-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d263-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="9d263-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-243">System-Flags</span></span>           | <span data-ttu-id="9d263-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d263-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="9d263-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d263-245">Classes used in</span></span>        | [<span data-ttu-id="9d263-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9d263-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9d263-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d263-247">Windows Server 2012</span></span>



| <span data-ttu-id="9d263-248">進入</span><span class="sxs-lookup"><span data-stu-id="9d263-248">Entry</span></span> | <span data-ttu-id="9d263-249">值</span><span class="sxs-lookup"><span data-stu-id="9d263-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9d263-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d263-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d263-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="9d263-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d263-252">System-Only</span></span>            | <span data-ttu-id="9d263-253">否</span><span class="sxs-lookup"><span data-stu-id="9d263-253">False</span></span>                                                               |
| <span data-ttu-id="9d263-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d263-254">Is-Single-Valued</span></span>       | <span data-ttu-id="9d263-255">對</span><span class="sxs-lookup"><span data-stu-id="9d263-255">True</span></span>                                                                |
| <span data-ttu-id="9d263-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d263-256">Is Indexed</span></span>             | <span data-ttu-id="9d263-257">否</span><span class="sxs-lookup"><span data-stu-id="9d263-257">False</span></span>                                                               |
| <span data-ttu-id="9d263-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d263-258">In Global Catalog</span></span>      | <span data-ttu-id="9d263-259">否</span><span class="sxs-lookup"><span data-stu-id="9d263-259">False</span></span>                                                               |
| <span data-ttu-id="9d263-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d263-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d263-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d263-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="9d263-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d263-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d263-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="9d263-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-264">Search-Flags</span></span>           | <span data-ttu-id="9d263-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d263-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="9d263-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d263-266">System-Flags</span></span>           | <span data-ttu-id="9d263-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d263-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="9d263-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d263-268">Classes used in</span></span>        | [<span data-ttu-id="9d263-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="9d263-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





