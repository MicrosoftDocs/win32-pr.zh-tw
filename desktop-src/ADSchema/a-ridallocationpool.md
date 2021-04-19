---
title: RID 組態集區屬性
description: 當 RID 先前的組態集區已用完時，被 RID 管理員所使用的集區。
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- RID 組態集區屬性 AD 架構
- rIDAllocationPool 屬性 AD 架構
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a035cef460cc3081144d66391db78fb32c61108b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966980"
---
# <a name="rid-allocation-pool-attribute"></a><span data-ttu-id="baae3-105">RID 組態集區屬性</span><span class="sxs-lookup"><span data-stu-id="baae3-105">RID-Allocation-Pool attribute</span></span>

<span data-ttu-id="baae3-106">當 RID 先前的組態集區已用完時，被 RID 管理員所使用的集區。</span><span class="sxs-lookup"><span data-stu-id="baae3-106">A pool that was prefetched for use by the RID manager when the RID-Previous-Allocation-Pool has been used up.</span></span>



| <span data-ttu-id="baae3-107">進入</span><span class="sxs-lookup"><span data-stu-id="baae3-107">Entry</span></span> | <span data-ttu-id="baae3-108">值</span><span class="sxs-lookup"><span data-stu-id="baae3-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="baae3-109">CN</span><span class="sxs-lookup"><span data-stu-id="baae3-109">CN</span></span>                | <span data-ttu-id="baae3-110">RID-組態集區</span><span class="sxs-lookup"><span data-stu-id="baae3-110">RID-Allocation-Pool</span></span>                  |
| <span data-ttu-id="baae3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="baae3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="baae3-112">rIDAllocationPool</span><span class="sxs-lookup"><span data-stu-id="baae3-112">rIDAllocationPool</span></span>                    |
| <span data-ttu-id="baae3-113">大小</span><span class="sxs-lookup"><span data-stu-id="baae3-113">Size</span></span>              | <span data-ttu-id="baae3-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="baae3-114">8 bytes</span></span>                              |
| <span data-ttu-id="baae3-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="baae3-115">Update Privilege</span></span>  | <span data-ttu-id="baae3-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="baae3-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="baae3-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="baae3-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="baae3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="baae3-118">Attribute-Id</span></span>      | <span data-ttu-id="baae3-119">1.2.840.113556.1.4.371</span><span class="sxs-lookup"><span data-stu-id="baae3-119">1.2.840.113556.1.4.371</span></span>               |
| <span data-ttu-id="baae3-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="baae3-120">System-Id-Guid</span></span>    | <span data-ttu-id="baae3-121">66171889-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="baae3-121">66171889-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="baae3-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="baae3-122">Syntax</span></span>            | [<span data-ttu-id="baae3-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="baae3-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="baae3-124">實作</span><span class="sxs-lookup"><span data-stu-id="baae3-124">Implementations</span></span>

-   [<span data-ttu-id="baae3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="baae3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="baae3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="baae3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="baae3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="baae3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="baae3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="baae3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="baae3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="baae3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="baae3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="baae3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="baae3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="baae3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="baae3-132">進入</span><span class="sxs-lookup"><span data-stu-id="baae3-132">Entry</span></span> | <span data-ttu-id="baae3-133">值</span><span class="sxs-lookup"><span data-stu-id="baae3-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="baae3-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="baae3-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baae3-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="baae3-136">System-Only</span></span>            | <span data-ttu-id="baae3-137">對</span><span class="sxs-lookup"><span data-stu-id="baae3-137">True</span></span>                                   |
| <span data-ttu-id="baae3-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="baae3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="baae3-139">對</span><span class="sxs-lookup"><span data-stu-id="baae3-139">True</span></span>                                   |
| <span data-ttu-id="baae3-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="baae3-140">Is Indexed</span></span>             | <span data-ttu-id="baae3-141">否</span><span class="sxs-lookup"><span data-stu-id="baae3-141">False</span></span>                                  |
| <span data-ttu-id="baae3-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="baae3-142">In Global Catalog</span></span>      | <span data-ttu-id="baae3-143">否</span><span class="sxs-lookup"><span data-stu-id="baae3-143">False</span></span>                                  |
| <span data-ttu-id="baae3-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="baae3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="baae3-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="baae3-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="baae3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baae3-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="baae3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baae3-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="baae3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-148">Search-Flags</span></span>           | <span data-ttu-id="baae3-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baae3-149">0x00000000</span></span>                             |
| <span data-ttu-id="baae3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-150">System-Flags</span></span>           | <span data-ttu-id="baae3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baae3-151">0x00000010</span></span>                             |
| <span data-ttu-id="baae3-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="baae3-152">Classes used in</span></span>        | [<span data-ttu-id="baae3-153">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="baae3-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="baae3-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="baae3-154">Windows Server 2003</span></span>



| <span data-ttu-id="baae3-155">進入</span><span class="sxs-lookup"><span data-stu-id="baae3-155">Entry</span></span> | <span data-ttu-id="baae3-156">值</span><span class="sxs-lookup"><span data-stu-id="baae3-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="baae3-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="baae3-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baae3-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="baae3-159">System-Only</span></span>            | <span data-ttu-id="baae3-160">對</span><span class="sxs-lookup"><span data-stu-id="baae3-160">True</span></span>                                   |
| <span data-ttu-id="baae3-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="baae3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="baae3-162">對</span><span class="sxs-lookup"><span data-stu-id="baae3-162">True</span></span>                                   |
| <span data-ttu-id="baae3-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="baae3-163">Is Indexed</span></span>             | <span data-ttu-id="baae3-164">否</span><span class="sxs-lookup"><span data-stu-id="baae3-164">False</span></span>                                  |
| <span data-ttu-id="baae3-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="baae3-165">In Global Catalog</span></span>      | <span data-ttu-id="baae3-166">否</span><span class="sxs-lookup"><span data-stu-id="baae3-166">False</span></span>                                  |
| <span data-ttu-id="baae3-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="baae3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="baae3-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="baae3-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="baae3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baae3-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="baae3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baae3-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="baae3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-171">Search-Flags</span></span>           | <span data-ttu-id="baae3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baae3-172">0x00000000</span></span>                             |
| <span data-ttu-id="baae3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-173">System-Flags</span></span>           | <span data-ttu-id="baae3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baae3-174">0x00000010</span></span>                             |
| <span data-ttu-id="baae3-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="baae3-175">Classes used in</span></span>        | [<span data-ttu-id="baae3-176">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="baae3-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="baae3-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="baae3-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="baae3-178">進入</span><span class="sxs-lookup"><span data-stu-id="baae3-178">Entry</span></span> | <span data-ttu-id="baae3-179">值</span><span class="sxs-lookup"><span data-stu-id="baae3-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="baae3-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="baae3-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baae3-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="baae3-182">System-Only</span></span>            | <span data-ttu-id="baae3-183">對</span><span class="sxs-lookup"><span data-stu-id="baae3-183">True</span></span>                                   |
| <span data-ttu-id="baae3-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="baae3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="baae3-185">對</span><span class="sxs-lookup"><span data-stu-id="baae3-185">True</span></span>                                   |
| <span data-ttu-id="baae3-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="baae3-186">Is Indexed</span></span>             | <span data-ttu-id="baae3-187">否</span><span class="sxs-lookup"><span data-stu-id="baae3-187">False</span></span>                                  |
| <span data-ttu-id="baae3-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="baae3-188">In Global Catalog</span></span>      | <span data-ttu-id="baae3-189">否</span><span class="sxs-lookup"><span data-stu-id="baae3-189">False</span></span>                                  |
| <span data-ttu-id="baae3-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="baae3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="baae3-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="baae3-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="baae3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baae3-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="baae3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baae3-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="baae3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-194">Search-Flags</span></span>           | <span data-ttu-id="baae3-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baae3-195">0x00000000</span></span>                             |
| <span data-ttu-id="baae3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-196">System-Flags</span></span>           | <span data-ttu-id="baae3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baae3-197">0x00000010</span></span>                             |
| <span data-ttu-id="baae3-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="baae3-198">Classes used in</span></span>        | [<span data-ttu-id="baae3-199">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="baae3-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="baae3-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baae3-200">Windows Server 2008</span></span>



| <span data-ttu-id="baae3-201">進入</span><span class="sxs-lookup"><span data-stu-id="baae3-201">Entry</span></span> | <span data-ttu-id="baae3-202">值</span><span class="sxs-lookup"><span data-stu-id="baae3-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="baae3-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="baae3-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baae3-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="baae3-205">System-Only</span></span>            | <span data-ttu-id="baae3-206">對</span><span class="sxs-lookup"><span data-stu-id="baae3-206">True</span></span>                                   |
| <span data-ttu-id="baae3-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="baae3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="baae3-208">對</span><span class="sxs-lookup"><span data-stu-id="baae3-208">True</span></span>                                   |
| <span data-ttu-id="baae3-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="baae3-209">Is Indexed</span></span>             | <span data-ttu-id="baae3-210">否</span><span class="sxs-lookup"><span data-stu-id="baae3-210">False</span></span>                                  |
| <span data-ttu-id="baae3-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="baae3-211">In Global Catalog</span></span>      | <span data-ttu-id="baae3-212">否</span><span class="sxs-lookup"><span data-stu-id="baae3-212">False</span></span>                                  |
| <span data-ttu-id="baae3-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="baae3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="baae3-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="baae3-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="baae3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baae3-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="baae3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baae3-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="baae3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-217">Search-Flags</span></span>           | <span data-ttu-id="baae3-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baae3-218">0x00000000</span></span>                             |
| <span data-ttu-id="baae3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-219">System-Flags</span></span>           | <span data-ttu-id="baae3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baae3-220">0x00000010</span></span>                             |
| <span data-ttu-id="baae3-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="baae3-221">Classes used in</span></span>        | [<span data-ttu-id="baae3-222">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="baae3-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="baae3-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="baae3-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="baae3-224">進入</span><span class="sxs-lookup"><span data-stu-id="baae3-224">Entry</span></span> | <span data-ttu-id="baae3-225">值</span><span class="sxs-lookup"><span data-stu-id="baae3-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="baae3-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="baae3-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baae3-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="baae3-228">System-Only</span></span>            | <span data-ttu-id="baae3-229">對</span><span class="sxs-lookup"><span data-stu-id="baae3-229">True</span></span>                                   |
| <span data-ttu-id="baae3-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="baae3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="baae3-231">對</span><span class="sxs-lookup"><span data-stu-id="baae3-231">True</span></span>                                   |
| <span data-ttu-id="baae3-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="baae3-232">Is Indexed</span></span>             | <span data-ttu-id="baae3-233">否</span><span class="sxs-lookup"><span data-stu-id="baae3-233">False</span></span>                                  |
| <span data-ttu-id="baae3-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="baae3-234">In Global Catalog</span></span>      | <span data-ttu-id="baae3-235">否</span><span class="sxs-lookup"><span data-stu-id="baae3-235">False</span></span>                                  |
| <span data-ttu-id="baae3-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="baae3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="baae3-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="baae3-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="baae3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baae3-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="baae3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baae3-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="baae3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-240">Search-Flags</span></span>           | <span data-ttu-id="baae3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baae3-241">0x00000000</span></span>                             |
| <span data-ttu-id="baae3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-242">System-Flags</span></span>           | <span data-ttu-id="baae3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baae3-243">0x00000010</span></span>                             |
| <span data-ttu-id="baae3-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="baae3-244">Classes used in</span></span>        | [<span data-ttu-id="baae3-245">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="baae3-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="baae3-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="baae3-246">Windows Server 2012</span></span>



| <span data-ttu-id="baae3-247">進入</span><span class="sxs-lookup"><span data-stu-id="baae3-247">Entry</span></span> | <span data-ttu-id="baae3-248">值</span><span class="sxs-lookup"><span data-stu-id="baae3-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="baae3-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="baae3-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baae3-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="baae3-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="baae3-251">System-Only</span></span>            | <span data-ttu-id="baae3-252">對</span><span class="sxs-lookup"><span data-stu-id="baae3-252">True</span></span>                                   |
| <span data-ttu-id="baae3-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="baae3-253">Is-Single-Valued</span></span>       | <span data-ttu-id="baae3-254">對</span><span class="sxs-lookup"><span data-stu-id="baae3-254">True</span></span>                                   |
| <span data-ttu-id="baae3-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="baae3-255">Is Indexed</span></span>             | <span data-ttu-id="baae3-256">否</span><span class="sxs-lookup"><span data-stu-id="baae3-256">False</span></span>                                  |
| <span data-ttu-id="baae3-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="baae3-257">In Global Catalog</span></span>      | <span data-ttu-id="baae3-258">否</span><span class="sxs-lookup"><span data-stu-id="baae3-258">False</span></span>                                  |
| <span data-ttu-id="baae3-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="baae3-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="baae3-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="baae3-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="baae3-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baae3-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="baae3-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baae3-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="baae3-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-263">Search-Flags</span></span>           | <span data-ttu-id="baae3-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baae3-264">0x00000000</span></span>                             |
| <span data-ttu-id="baae3-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baae3-265">System-Flags</span></span>           | <span data-ttu-id="baae3-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baae3-266">0x00000010</span></span>                             |
| <span data-ttu-id="baae3-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="baae3-267">Classes used in</span></span>        | [<span data-ttu-id="baae3-268">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="baae3-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





