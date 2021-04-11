---
title: RID 使用的集區屬性
description: DC 所使用的 RID 集區。
ms.assetid: ca779461-5b8f-4ab2-b9cf-5f829889f10d
ms.tgt_platform: multiple
keywords:
- RID 使用的集區屬性 AD 架構
- rIDUsedPool 屬性 AD 架構
topic_type:
- apiref
api_name:
- RID-Used-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84547d99b162da9da6e634a7c35eb9700e84e2a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107573"
---
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="34c8a-105">RID 使用的集區屬性</span><span class="sxs-lookup"><span data-stu-id="34c8a-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="34c8a-106">DC 所使用的 RID 集區。</span><span class="sxs-lookup"><span data-stu-id="34c8a-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="34c8a-107">進入</span><span class="sxs-lookup"><span data-stu-id="34c8a-107">Entry</span></span> | <span data-ttu-id="34c8a-108">值</span><span class="sxs-lookup"><span data-stu-id="34c8a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="34c8a-109">CN</span><span class="sxs-lookup"><span data-stu-id="34c8a-109">CN</span></span>                | <span data-ttu-id="34c8a-110">RID-已使用集區</span><span class="sxs-lookup"><span data-stu-id="34c8a-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="34c8a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="34c8a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="34c8a-112">rIDUsedPool</span><span class="sxs-lookup"><span data-stu-id="34c8a-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="34c8a-113">大小</span><span class="sxs-lookup"><span data-stu-id="34c8a-113">Size</span></span>              | <span data-ttu-id="34c8a-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="34c8a-114">8 bytes</span></span>                              |
| <span data-ttu-id="34c8a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="34c8a-115">Update Privilege</span></span>  | <span data-ttu-id="34c8a-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="34c8a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="34c8a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="34c8a-117">Update Frequency</span></span>  | <span data-ttu-id="34c8a-118">每次清空 RID 集區時。</span><span class="sxs-lookup"><span data-stu-id="34c8a-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="34c8a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="34c8a-119">Attribute-Id</span></span>      | <span data-ttu-id="34c8a-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="34c8a-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="34c8a-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="34c8a-121">System-Id-Guid</span></span>    | <span data-ttu-id="34c8a-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="34c8a-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="34c8a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="34c8a-123">Syntax</span></span>            | [<span data-ttu-id="34c8a-124">**間隔**</span><span class="sxs-lookup"><span data-stu-id="34c8a-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="34c8a-125">實作</span><span class="sxs-lookup"><span data-stu-id="34c8a-125">Implementations</span></span>

-   [<span data-ttu-id="34c8a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="34c8a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="34c8a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="34c8a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="34c8a-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="34c8a-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="34c8a-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="34c8a-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="34c8a-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="34c8a-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="34c8a-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="34c8a-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="34c8a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34c8a-132">Windows 2000 Server</span></span>



| <span data-ttu-id="34c8a-133">進入</span><span class="sxs-lookup"><span data-stu-id="34c8a-133">Entry</span></span> | <span data-ttu-id="34c8a-134">值</span><span class="sxs-lookup"><span data-stu-id="34c8a-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="34c8a-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34c8a-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34c8a-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="34c8a-137">System-Only</span></span>            | <span data-ttu-id="34c8a-138">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-138">True</span></span>                                   |
| <span data-ttu-id="34c8a-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34c8a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="34c8a-140">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-140">True</span></span>                                   |
| <span data-ttu-id="34c8a-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34c8a-141">Is Indexed</span></span>             | <span data-ttu-id="34c8a-142">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-142">False</span></span>                                  |
| <span data-ttu-id="34c8a-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34c8a-143">In Global Catalog</span></span>      | <span data-ttu-id="34c8a-144">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-144">False</span></span>                                  |
| <span data-ttu-id="34c8a-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34c8a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="34c8a-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34c8a-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="34c8a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34c8a-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34c8a-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-149">Search-Flags</span></span>           | <span data-ttu-id="34c8a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34c8a-150">0x00000000</span></span>                             |
| <span data-ttu-id="34c8a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-151">System-Flags</span></span>           | <span data-ttu-id="34c8a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34c8a-152">0x00000010</span></span>                             |
| <span data-ttu-id="34c8a-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34c8a-153">Classes used in</span></span>        | [<span data-ttu-id="34c8a-154">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="34c8a-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="34c8a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34c8a-155">Windows Server 2003</span></span>



| <span data-ttu-id="34c8a-156">進入</span><span class="sxs-lookup"><span data-stu-id="34c8a-156">Entry</span></span> | <span data-ttu-id="34c8a-157">值</span><span class="sxs-lookup"><span data-stu-id="34c8a-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="34c8a-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34c8a-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34c8a-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="34c8a-160">System-Only</span></span>            | <span data-ttu-id="34c8a-161">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-161">True</span></span>                                   |
| <span data-ttu-id="34c8a-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34c8a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="34c8a-163">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-163">True</span></span>                                   |
| <span data-ttu-id="34c8a-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34c8a-164">Is Indexed</span></span>             | <span data-ttu-id="34c8a-165">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-165">False</span></span>                                  |
| <span data-ttu-id="34c8a-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34c8a-166">In Global Catalog</span></span>      | <span data-ttu-id="34c8a-167">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-167">False</span></span>                                  |
| <span data-ttu-id="34c8a-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34c8a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="34c8a-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34c8a-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="34c8a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34c8a-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34c8a-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-172">Search-Flags</span></span>           | <span data-ttu-id="34c8a-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34c8a-173">0x00000000</span></span>                             |
| <span data-ttu-id="34c8a-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-174">System-Flags</span></span>           | <span data-ttu-id="34c8a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34c8a-175">0x00000010</span></span>                             |
| <span data-ttu-id="34c8a-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34c8a-176">Classes used in</span></span>        | [<span data-ttu-id="34c8a-177">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="34c8a-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="34c8a-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="34c8a-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="34c8a-179">進入</span><span class="sxs-lookup"><span data-stu-id="34c8a-179">Entry</span></span> | <span data-ttu-id="34c8a-180">值</span><span class="sxs-lookup"><span data-stu-id="34c8a-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="34c8a-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34c8a-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34c8a-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="34c8a-183">System-Only</span></span>            | <span data-ttu-id="34c8a-184">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-184">True</span></span>                                   |
| <span data-ttu-id="34c8a-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34c8a-185">Is-Single-Valued</span></span>       | <span data-ttu-id="34c8a-186">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-186">True</span></span>                                   |
| <span data-ttu-id="34c8a-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34c8a-187">Is Indexed</span></span>             | <span data-ttu-id="34c8a-188">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-188">False</span></span>                                  |
| <span data-ttu-id="34c8a-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34c8a-189">In Global Catalog</span></span>      | <span data-ttu-id="34c8a-190">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-190">False</span></span>                                  |
| <span data-ttu-id="34c8a-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34c8a-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="34c8a-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34c8a-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="34c8a-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34c8a-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34c8a-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-195">Search-Flags</span></span>           | <span data-ttu-id="34c8a-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34c8a-196">0x00000000</span></span>                             |
| <span data-ttu-id="34c8a-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-197">System-Flags</span></span>           | <span data-ttu-id="34c8a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34c8a-198">0x00000010</span></span>                             |
| <span data-ttu-id="34c8a-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34c8a-199">Classes used in</span></span>        | [<span data-ttu-id="34c8a-200">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="34c8a-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="34c8a-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34c8a-201">Windows Server 2008</span></span>



| <span data-ttu-id="34c8a-202">進入</span><span class="sxs-lookup"><span data-stu-id="34c8a-202">Entry</span></span> | <span data-ttu-id="34c8a-203">值</span><span class="sxs-lookup"><span data-stu-id="34c8a-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="34c8a-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34c8a-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34c8a-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="34c8a-206">System-Only</span></span>            | <span data-ttu-id="34c8a-207">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-207">True</span></span>                                   |
| <span data-ttu-id="34c8a-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34c8a-208">Is-Single-Valued</span></span>       | <span data-ttu-id="34c8a-209">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-209">True</span></span>                                   |
| <span data-ttu-id="34c8a-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34c8a-210">Is Indexed</span></span>             | <span data-ttu-id="34c8a-211">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-211">False</span></span>                                  |
| <span data-ttu-id="34c8a-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34c8a-212">In Global Catalog</span></span>      | <span data-ttu-id="34c8a-213">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-213">False</span></span>                                  |
| <span data-ttu-id="34c8a-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34c8a-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="34c8a-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34c8a-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="34c8a-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34c8a-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34c8a-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-218">Search-Flags</span></span>           | <span data-ttu-id="34c8a-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34c8a-219">0x00000000</span></span>                             |
| <span data-ttu-id="34c8a-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-220">System-Flags</span></span>           | <span data-ttu-id="34c8a-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34c8a-221">0x00000010</span></span>                             |
| <span data-ttu-id="34c8a-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34c8a-222">Classes used in</span></span>        | [<span data-ttu-id="34c8a-223">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="34c8a-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="34c8a-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34c8a-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="34c8a-225">進入</span><span class="sxs-lookup"><span data-stu-id="34c8a-225">Entry</span></span> | <span data-ttu-id="34c8a-226">值</span><span class="sxs-lookup"><span data-stu-id="34c8a-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="34c8a-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34c8a-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34c8a-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="34c8a-229">System-Only</span></span>            | <span data-ttu-id="34c8a-230">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-230">True</span></span>                                   |
| <span data-ttu-id="34c8a-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34c8a-231">Is-Single-Valued</span></span>       | <span data-ttu-id="34c8a-232">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-232">True</span></span>                                   |
| <span data-ttu-id="34c8a-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34c8a-233">Is Indexed</span></span>             | <span data-ttu-id="34c8a-234">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-234">False</span></span>                                  |
| <span data-ttu-id="34c8a-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34c8a-235">In Global Catalog</span></span>      | <span data-ttu-id="34c8a-236">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-236">False</span></span>                                  |
| <span data-ttu-id="34c8a-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34c8a-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="34c8a-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34c8a-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="34c8a-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34c8a-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34c8a-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-241">Search-Flags</span></span>           | <span data-ttu-id="34c8a-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34c8a-242">0x00000000</span></span>                             |
| <span data-ttu-id="34c8a-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-243">System-Flags</span></span>           | <span data-ttu-id="34c8a-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34c8a-244">0x00000010</span></span>                             |
| <span data-ttu-id="34c8a-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34c8a-245">Classes used in</span></span>        | [<span data-ttu-id="34c8a-246">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="34c8a-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="34c8a-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34c8a-247">Windows Server 2012</span></span>



| <span data-ttu-id="34c8a-248">進入</span><span class="sxs-lookup"><span data-stu-id="34c8a-248">Entry</span></span> | <span data-ttu-id="34c8a-249">值</span><span class="sxs-lookup"><span data-stu-id="34c8a-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="34c8a-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="34c8a-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34c8a-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="34c8a-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="34c8a-252">System-Only</span></span>            | <span data-ttu-id="34c8a-253">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-253">True</span></span>                                   |
| <span data-ttu-id="34c8a-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="34c8a-254">Is-Single-Valued</span></span>       | <span data-ttu-id="34c8a-255">對</span><span class="sxs-lookup"><span data-stu-id="34c8a-255">True</span></span>                                   |
| <span data-ttu-id="34c8a-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="34c8a-256">Is Indexed</span></span>             | <span data-ttu-id="34c8a-257">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-257">False</span></span>                                  |
| <span data-ttu-id="34c8a-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="34c8a-258">In Global Catalog</span></span>      | <span data-ttu-id="34c8a-259">否</span><span class="sxs-lookup"><span data-stu-id="34c8a-259">False</span></span>                                  |
| <span data-ttu-id="34c8a-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="34c8a-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="34c8a-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="34c8a-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="34c8a-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34c8a-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34c8a-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="34c8a-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-264">Search-Flags</span></span>           | <span data-ttu-id="34c8a-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34c8a-265">0x00000000</span></span>                             |
| <span data-ttu-id="34c8a-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34c8a-266">System-Flags</span></span>           | <span data-ttu-id="34c8a-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34c8a-267">0x00000010</span></span>                             |
| <span data-ttu-id="34c8a-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="34c8a-268">Classes used in</span></span>        | [<span data-ttu-id="34c8a-269">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="34c8a-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





