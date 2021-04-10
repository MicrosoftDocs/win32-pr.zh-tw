---
title: RID-先前組態集區屬性
description: 包含網域控制站所配置的 (Rid) 的相對識別碼集區。
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-先前組態集區屬性 AD 架構
- rIDPreviousAllocationPool 屬性 AD 架構
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844939"
---
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="6eee8-105">RID-先前組態集區屬性</span><span class="sxs-lookup"><span data-stu-id="6eee8-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="6eee8-106">**Rid-Previous 組態集** 區屬性包含網域控制站所配置的 (rid) 的相對識別碼集區。</span><span class="sxs-lookup"><span data-stu-id="6eee8-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="6eee8-107">這個屬性是八位元組的值，其中包含一組四個位元組的整數，表示 RID 集區的開始和結束值。</span><span class="sxs-lookup"><span data-stu-id="6eee8-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="6eee8-108">開始值是在四個位元組的下方，而結束值是在四個位元組內。</span><span class="sxs-lookup"><span data-stu-id="6eee8-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="6eee8-109">進入</span><span class="sxs-lookup"><span data-stu-id="6eee8-109">Entry</span></span> | <span data-ttu-id="6eee8-110">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6eee8-111">CN</span><span class="sxs-lookup"><span data-stu-id="6eee8-111">CN</span></span>                | <span data-ttu-id="6eee8-112">RID-先前組態集區</span><span class="sxs-lookup"><span data-stu-id="6eee8-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="6eee8-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6eee8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6eee8-114">rIDPreviousAllocationPool</span><span class="sxs-lookup"><span data-stu-id="6eee8-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="6eee8-115">大小</span><span class="sxs-lookup"><span data-stu-id="6eee8-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="6eee8-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6eee8-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6eee8-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6eee8-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6eee8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6eee8-118">Attribute-Id</span></span>      | <span data-ttu-id="6eee8-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="6eee8-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="6eee8-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6eee8-120">System-Id-Guid</span></span>    | <span data-ttu-id="6eee8-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="6eee8-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="6eee8-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6eee8-122">Syntax</span></span>            | [<span data-ttu-id="6eee8-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="6eee8-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6eee8-124">實作</span><span class="sxs-lookup"><span data-stu-id="6eee8-124">Implementations</span></span>

-   [<span data-ttu-id="6eee8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6eee8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6eee8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6eee8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6eee8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6eee8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6eee8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6eee8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6eee8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6eee8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6eee8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6eee8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6eee8-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6eee8-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6eee8-132">進入</span><span class="sxs-lookup"><span data-stu-id="6eee8-132">Entry</span></span> | <span data-ttu-id="6eee8-133">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="6eee8-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6eee8-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eee8-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eee8-136">System-Only</span></span>            | <span data-ttu-id="6eee8-137">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-137">True</span></span>                                   |
| <span data-ttu-id="6eee8-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6eee8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6eee8-139">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-139">True</span></span>                                   |
| <span data-ttu-id="6eee8-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6eee8-140">Is Indexed</span></span>             | <span data-ttu-id="6eee8-141">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-141">False</span></span>                                  |
| <span data-ttu-id="6eee8-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6eee8-142">In Global Catalog</span></span>      | <span data-ttu-id="6eee8-143">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-143">False</span></span>                                  |
| <span data-ttu-id="6eee8-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6eee8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eee8-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6eee8-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="6eee8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eee8-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eee8-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-148">Search-Flags</span></span>           | <span data-ttu-id="6eee8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eee8-149">0x00000000</span></span>                             |
| <span data-ttu-id="6eee8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-150">System-Flags</span></span>           | <span data-ttu-id="6eee8-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6eee8-151">0x00000011</span></span>                             |
| <span data-ttu-id="6eee8-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6eee8-152">Classes used in</span></span>        | [<span data-ttu-id="6eee8-153">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="6eee8-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6eee8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6eee8-154">Windows Server 2003</span></span>



| <span data-ttu-id="6eee8-155">進入</span><span class="sxs-lookup"><span data-stu-id="6eee8-155">Entry</span></span> | <span data-ttu-id="6eee8-156">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="6eee8-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6eee8-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eee8-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eee8-159">System-Only</span></span>            | <span data-ttu-id="6eee8-160">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-160">True</span></span>                                   |
| <span data-ttu-id="6eee8-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6eee8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6eee8-162">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-162">True</span></span>                                   |
| <span data-ttu-id="6eee8-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6eee8-163">Is Indexed</span></span>             | <span data-ttu-id="6eee8-164">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-164">False</span></span>                                  |
| <span data-ttu-id="6eee8-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6eee8-165">In Global Catalog</span></span>      | <span data-ttu-id="6eee8-166">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-166">False</span></span>                                  |
| <span data-ttu-id="6eee8-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6eee8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eee8-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6eee8-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="6eee8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eee8-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eee8-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-171">Search-Flags</span></span>           | <span data-ttu-id="6eee8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eee8-172">0x00000000</span></span>                             |
| <span data-ttu-id="6eee8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-173">System-Flags</span></span>           | <span data-ttu-id="6eee8-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6eee8-174">0x00000011</span></span>                             |
| <span data-ttu-id="6eee8-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6eee8-175">Classes used in</span></span>        | [<span data-ttu-id="6eee8-176">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="6eee8-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6eee8-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6eee8-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6eee8-178">進入</span><span class="sxs-lookup"><span data-stu-id="6eee8-178">Entry</span></span> | <span data-ttu-id="6eee8-179">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="6eee8-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6eee8-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eee8-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eee8-182">System-Only</span></span>            | <span data-ttu-id="6eee8-183">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-183">True</span></span>                                   |
| <span data-ttu-id="6eee8-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6eee8-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6eee8-185">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-185">True</span></span>                                   |
| <span data-ttu-id="6eee8-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6eee8-186">Is Indexed</span></span>             | <span data-ttu-id="6eee8-187">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-187">False</span></span>                                  |
| <span data-ttu-id="6eee8-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6eee8-188">In Global Catalog</span></span>      | <span data-ttu-id="6eee8-189">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-189">False</span></span>                                  |
| <span data-ttu-id="6eee8-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6eee8-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eee8-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6eee8-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="6eee8-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eee8-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eee8-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-194">Search-Flags</span></span>           | <span data-ttu-id="6eee8-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eee8-195">0x00000000</span></span>                             |
| <span data-ttu-id="6eee8-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-196">System-Flags</span></span>           | <span data-ttu-id="6eee8-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6eee8-197">0x00000011</span></span>                             |
| <span data-ttu-id="6eee8-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6eee8-198">Classes used in</span></span>        | [<span data-ttu-id="6eee8-199">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="6eee8-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6eee8-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6eee8-200">Windows Server 2008</span></span>



| <span data-ttu-id="6eee8-201">進入</span><span class="sxs-lookup"><span data-stu-id="6eee8-201">Entry</span></span> | <span data-ttu-id="6eee8-202">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="6eee8-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6eee8-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eee8-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eee8-205">System-Only</span></span>            | <span data-ttu-id="6eee8-206">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-206">True</span></span>                                   |
| <span data-ttu-id="6eee8-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6eee8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6eee8-208">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-208">True</span></span>                                   |
| <span data-ttu-id="6eee8-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6eee8-209">Is Indexed</span></span>             | <span data-ttu-id="6eee8-210">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-210">False</span></span>                                  |
| <span data-ttu-id="6eee8-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6eee8-211">In Global Catalog</span></span>      | <span data-ttu-id="6eee8-212">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-212">False</span></span>                                  |
| <span data-ttu-id="6eee8-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6eee8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eee8-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6eee8-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="6eee8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eee8-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eee8-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-217">Search-Flags</span></span>           | <span data-ttu-id="6eee8-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eee8-218">0x00000000</span></span>                             |
| <span data-ttu-id="6eee8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-219">System-Flags</span></span>           | <span data-ttu-id="6eee8-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6eee8-220">0x00000011</span></span>                             |
| <span data-ttu-id="6eee8-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6eee8-221">Classes used in</span></span>        | [<span data-ttu-id="6eee8-222">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="6eee8-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6eee8-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6eee8-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6eee8-224">進入</span><span class="sxs-lookup"><span data-stu-id="6eee8-224">Entry</span></span> | <span data-ttu-id="6eee8-225">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="6eee8-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6eee8-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eee8-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eee8-228">System-Only</span></span>            | <span data-ttu-id="6eee8-229">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-229">True</span></span>                                   |
| <span data-ttu-id="6eee8-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6eee8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6eee8-231">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-231">True</span></span>                                   |
| <span data-ttu-id="6eee8-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6eee8-232">Is Indexed</span></span>             | <span data-ttu-id="6eee8-233">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-233">False</span></span>                                  |
| <span data-ttu-id="6eee8-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6eee8-234">In Global Catalog</span></span>      | <span data-ttu-id="6eee8-235">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-235">False</span></span>                                  |
| <span data-ttu-id="6eee8-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6eee8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eee8-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6eee8-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="6eee8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eee8-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eee8-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-240">Search-Flags</span></span>           | <span data-ttu-id="6eee8-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eee8-241">0x00000000</span></span>                             |
| <span data-ttu-id="6eee8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-242">System-Flags</span></span>           | <span data-ttu-id="6eee8-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6eee8-243">0x00000011</span></span>                             |
| <span data-ttu-id="6eee8-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6eee8-244">Classes used in</span></span>        | [<span data-ttu-id="6eee8-245">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="6eee8-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6eee8-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6eee8-246">Windows Server 2012</span></span>



| <span data-ttu-id="6eee8-247">進入</span><span class="sxs-lookup"><span data-stu-id="6eee8-247">Entry</span></span> | <span data-ttu-id="6eee8-248">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="6eee8-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6eee8-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6eee8-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="6eee8-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6eee8-251">System-Only</span></span>            | <span data-ttu-id="6eee8-252">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-252">True</span></span>                                   |
| <span data-ttu-id="6eee8-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6eee8-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6eee8-254">對</span><span class="sxs-lookup"><span data-stu-id="6eee8-254">True</span></span>                                   |
| <span data-ttu-id="6eee8-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6eee8-255">Is Indexed</span></span>             | <span data-ttu-id="6eee8-256">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-256">False</span></span>                                  |
| <span data-ttu-id="6eee8-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6eee8-257">In Global Catalog</span></span>      | <span data-ttu-id="6eee8-258">否</span><span class="sxs-lookup"><span data-stu-id="6eee8-258">False</span></span>                                  |
| <span data-ttu-id="6eee8-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6eee8-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6eee8-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6eee8-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="6eee8-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6eee8-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6eee8-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="6eee8-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-263">Search-Flags</span></span>           | <span data-ttu-id="6eee8-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6eee8-264">0x00000000</span></span>                             |
| <span data-ttu-id="6eee8-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6eee8-265">System-Flags</span></span>           | <span data-ttu-id="6eee8-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6eee8-266">0x00000011</span></span>                             |
| <span data-ttu-id="6eee8-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6eee8-267">Classes used in</span></span>        | [<span data-ttu-id="6eee8-268">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="6eee8-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





