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
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="2d22f-105">RID-先前組態集區屬性</span><span class="sxs-lookup"><span data-stu-id="2d22f-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="2d22f-106">**Rid-Previous 組態集** 區屬性包含網域控制站所配置的 (rid) 的相對識別碼集區。</span><span class="sxs-lookup"><span data-stu-id="2d22f-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="2d22f-107">這個屬性是八位元組的值，其中包含一組四個位元組的整數，表示 RID 集區的開始和結束值。</span><span class="sxs-lookup"><span data-stu-id="2d22f-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="2d22f-108">開始值是在四個位元組的下方，而結束值是在四個位元組內。</span><span class="sxs-lookup"><span data-stu-id="2d22f-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="2d22f-109">進入</span><span class="sxs-lookup"><span data-stu-id="2d22f-109">Entry</span></span> | <span data-ttu-id="2d22f-110">值</span><span class="sxs-lookup"><span data-stu-id="2d22f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2d22f-111">CN</span><span class="sxs-lookup"><span data-stu-id="2d22f-111">CN</span></span>                | <span data-ttu-id="2d22f-112">RID-先前組態集區</span><span class="sxs-lookup"><span data-stu-id="2d22f-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="2d22f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2d22f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2d22f-114">rIDPreviousAllocationPool</span><span class="sxs-lookup"><span data-stu-id="2d22f-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="2d22f-115">大小</span><span class="sxs-lookup"><span data-stu-id="2d22f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="2d22f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2d22f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2d22f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2d22f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2d22f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d22f-118">Attribute-Id</span></span>      | <span data-ttu-id="2d22f-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="2d22f-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="2d22f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2d22f-120">System-Id-Guid</span></span>    | <span data-ttu-id="2d22f-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="2d22f-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="2d22f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d22f-122">Syntax</span></span>            | [<span data-ttu-id="2d22f-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="2d22f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2d22f-124">實作</span><span class="sxs-lookup"><span data-stu-id="2d22f-124">Implementations</span></span>

-   [<span data-ttu-id="2d22f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2d22f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2d22f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2d22f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2d22f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2d22f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2d22f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2d22f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2d22f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2d22f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2d22f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d22f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2d22f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d22f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2d22f-132">進入</span><span class="sxs-lookup"><span data-stu-id="2d22f-132">Entry</span></span> | <span data-ttu-id="2d22f-133">值</span><span class="sxs-lookup"><span data-stu-id="2d22f-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="2d22f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2d22f-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d22f-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d22f-136">System-Only</span></span>            | <span data-ttu-id="2d22f-137">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-137">True</span></span>                                   |
| <span data-ttu-id="2d22f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2d22f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2d22f-139">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-139">True</span></span>                                   |
| <span data-ttu-id="2d22f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2d22f-140">Is Indexed</span></span>             | <span data-ttu-id="2d22f-141">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-141">False</span></span>                                  |
| <span data-ttu-id="2d22f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2d22f-142">In Global Catalog</span></span>      | <span data-ttu-id="2d22f-143">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-143">False</span></span>                                  |
| <span data-ttu-id="2d22f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2d22f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d22f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2d22f-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="2d22f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d22f-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d22f-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-148">Search-Flags</span></span>           | <span data-ttu-id="2d22f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d22f-149">0x00000000</span></span>                             |
| <span data-ttu-id="2d22f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-150">System-Flags</span></span>           | <span data-ttu-id="2d22f-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2d22f-151">0x00000011</span></span>                             |
| <span data-ttu-id="2d22f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2d22f-152">Classes used in</span></span>        | [<span data-ttu-id="2d22f-153">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="2d22f-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2d22f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d22f-154">Windows Server 2003</span></span>



| <span data-ttu-id="2d22f-155">進入</span><span class="sxs-lookup"><span data-stu-id="2d22f-155">Entry</span></span> | <span data-ttu-id="2d22f-156">值</span><span class="sxs-lookup"><span data-stu-id="2d22f-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="2d22f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2d22f-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d22f-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d22f-159">System-Only</span></span>            | <span data-ttu-id="2d22f-160">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-160">True</span></span>                                   |
| <span data-ttu-id="2d22f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2d22f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2d22f-162">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-162">True</span></span>                                   |
| <span data-ttu-id="2d22f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2d22f-163">Is Indexed</span></span>             | <span data-ttu-id="2d22f-164">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-164">False</span></span>                                  |
| <span data-ttu-id="2d22f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2d22f-165">In Global Catalog</span></span>      | <span data-ttu-id="2d22f-166">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-166">False</span></span>                                  |
| <span data-ttu-id="2d22f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2d22f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d22f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2d22f-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="2d22f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d22f-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d22f-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-171">Search-Flags</span></span>           | <span data-ttu-id="2d22f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d22f-172">0x00000000</span></span>                             |
| <span data-ttu-id="2d22f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-173">System-Flags</span></span>           | <span data-ttu-id="2d22f-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2d22f-174">0x00000011</span></span>                             |
| <span data-ttu-id="2d22f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2d22f-175">Classes used in</span></span>        | [<span data-ttu-id="2d22f-176">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="2d22f-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2d22f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2d22f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2d22f-178">進入</span><span class="sxs-lookup"><span data-stu-id="2d22f-178">Entry</span></span> | <span data-ttu-id="2d22f-179">值</span><span class="sxs-lookup"><span data-stu-id="2d22f-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="2d22f-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2d22f-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d22f-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d22f-182">System-Only</span></span>            | <span data-ttu-id="2d22f-183">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-183">True</span></span>                                   |
| <span data-ttu-id="2d22f-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2d22f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2d22f-185">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-185">True</span></span>                                   |
| <span data-ttu-id="2d22f-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2d22f-186">Is Indexed</span></span>             | <span data-ttu-id="2d22f-187">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-187">False</span></span>                                  |
| <span data-ttu-id="2d22f-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2d22f-188">In Global Catalog</span></span>      | <span data-ttu-id="2d22f-189">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-189">False</span></span>                                  |
| <span data-ttu-id="2d22f-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2d22f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d22f-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2d22f-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="2d22f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d22f-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d22f-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-194">Search-Flags</span></span>           | <span data-ttu-id="2d22f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d22f-195">0x00000000</span></span>                             |
| <span data-ttu-id="2d22f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-196">System-Flags</span></span>           | <span data-ttu-id="2d22f-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2d22f-197">0x00000011</span></span>                             |
| <span data-ttu-id="2d22f-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2d22f-198">Classes used in</span></span>        | [<span data-ttu-id="2d22f-199">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="2d22f-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2d22f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d22f-200">Windows Server 2008</span></span>



| <span data-ttu-id="2d22f-201">進入</span><span class="sxs-lookup"><span data-stu-id="2d22f-201">Entry</span></span> | <span data-ttu-id="2d22f-202">值</span><span class="sxs-lookup"><span data-stu-id="2d22f-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="2d22f-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2d22f-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d22f-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d22f-205">System-Only</span></span>            | <span data-ttu-id="2d22f-206">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-206">True</span></span>                                   |
| <span data-ttu-id="2d22f-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2d22f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2d22f-208">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-208">True</span></span>                                   |
| <span data-ttu-id="2d22f-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2d22f-209">Is Indexed</span></span>             | <span data-ttu-id="2d22f-210">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-210">False</span></span>                                  |
| <span data-ttu-id="2d22f-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2d22f-211">In Global Catalog</span></span>      | <span data-ttu-id="2d22f-212">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-212">False</span></span>                                  |
| <span data-ttu-id="2d22f-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2d22f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d22f-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2d22f-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="2d22f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d22f-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d22f-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-217">Search-Flags</span></span>           | <span data-ttu-id="2d22f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d22f-218">0x00000000</span></span>                             |
| <span data-ttu-id="2d22f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-219">System-Flags</span></span>           | <span data-ttu-id="2d22f-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2d22f-220">0x00000011</span></span>                             |
| <span data-ttu-id="2d22f-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2d22f-221">Classes used in</span></span>        | [<span data-ttu-id="2d22f-222">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="2d22f-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2d22f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d22f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2d22f-224">進入</span><span class="sxs-lookup"><span data-stu-id="2d22f-224">Entry</span></span> | <span data-ttu-id="2d22f-225">值</span><span class="sxs-lookup"><span data-stu-id="2d22f-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="2d22f-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2d22f-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d22f-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d22f-228">System-Only</span></span>            | <span data-ttu-id="2d22f-229">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-229">True</span></span>                                   |
| <span data-ttu-id="2d22f-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2d22f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2d22f-231">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-231">True</span></span>                                   |
| <span data-ttu-id="2d22f-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2d22f-232">Is Indexed</span></span>             | <span data-ttu-id="2d22f-233">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-233">False</span></span>                                  |
| <span data-ttu-id="2d22f-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2d22f-234">In Global Catalog</span></span>      | <span data-ttu-id="2d22f-235">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-235">False</span></span>                                  |
| <span data-ttu-id="2d22f-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2d22f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d22f-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2d22f-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="2d22f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d22f-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d22f-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-240">Search-Flags</span></span>           | <span data-ttu-id="2d22f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d22f-241">0x00000000</span></span>                             |
| <span data-ttu-id="2d22f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-242">System-Flags</span></span>           | <span data-ttu-id="2d22f-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2d22f-243">0x00000011</span></span>                             |
| <span data-ttu-id="2d22f-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2d22f-244">Classes used in</span></span>        | [<span data-ttu-id="2d22f-245">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="2d22f-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2d22f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d22f-246">Windows Server 2012</span></span>



| <span data-ttu-id="2d22f-247">進入</span><span class="sxs-lookup"><span data-stu-id="2d22f-247">Entry</span></span> | <span data-ttu-id="2d22f-248">值</span><span class="sxs-lookup"><span data-stu-id="2d22f-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="2d22f-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2d22f-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d22f-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="2d22f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d22f-251">System-Only</span></span>            | <span data-ttu-id="2d22f-252">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-252">True</span></span>                                   |
| <span data-ttu-id="2d22f-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2d22f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2d22f-254">對</span><span class="sxs-lookup"><span data-stu-id="2d22f-254">True</span></span>                                   |
| <span data-ttu-id="2d22f-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2d22f-255">Is Indexed</span></span>             | <span data-ttu-id="2d22f-256">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-256">False</span></span>                                  |
| <span data-ttu-id="2d22f-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2d22f-257">In Global Catalog</span></span>      | <span data-ttu-id="2d22f-258">否</span><span class="sxs-lookup"><span data-stu-id="2d22f-258">False</span></span>                                  |
| <span data-ttu-id="2d22f-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2d22f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d22f-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2d22f-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="2d22f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d22f-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d22f-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="2d22f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-263">Search-Flags</span></span>           | <span data-ttu-id="2d22f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d22f-264">0x00000000</span></span>                             |
| <span data-ttu-id="2d22f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d22f-265">System-Flags</span></span>           | <span data-ttu-id="2d22f-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="2d22f-266">0x00000011</span></span>                             |
| <span data-ttu-id="2d22f-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2d22f-267">Classes used in</span></span>        | [<span data-ttu-id="2d22f-268">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="2d22f-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





