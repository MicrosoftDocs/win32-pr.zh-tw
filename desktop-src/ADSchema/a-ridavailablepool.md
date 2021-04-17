---
title: RID 可用-集區屬性
description: 用來配置 RID 集區的空間。
ms.assetid: abb6218f-def2-4a38-964f-3f0ee6c6f917
ms.tgt_platform: multiple
keywords:
- RID 可用-集區屬性 AD 架構
- rIDAvailablePool 屬性 AD 架構
topic_type:
- apiref
api_name:
- RID-Available-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59faf801b7f6f70e92c55a1d2a27857ed6ecb0c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187352"
---
# <a name="rid-available-pool-attribute"></a><span data-ttu-id="7fd6a-105">RID 可用-集區屬性</span><span class="sxs-lookup"><span data-stu-id="7fd6a-105">RID-Available-Pool attribute</span></span>

<span data-ttu-id="7fd6a-106">用來配置 RID 集區的空間。</span><span class="sxs-lookup"><span data-stu-id="7fd6a-106">The space from which RID Pools are allocated.</span></span>



| <span data-ttu-id="7fd6a-107">進入</span><span class="sxs-lookup"><span data-stu-id="7fd6a-107">Entry</span></span> | <span data-ttu-id="7fd6a-108">值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7fd6a-109">CN</span><span class="sxs-lookup"><span data-stu-id="7fd6a-109">CN</span></span>                | <span data-ttu-id="7fd6a-110">RID 可用-集區</span><span class="sxs-lookup"><span data-stu-id="7fd6a-110">RID-Available-Pool</span></span>                   |
| <span data-ttu-id="7fd6a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7fd6a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7fd6a-112">rIDAvailablePool</span><span class="sxs-lookup"><span data-stu-id="7fd6a-112">rIDAvailablePool</span></span>                     |
| <span data-ttu-id="7fd6a-113">大小</span><span class="sxs-lookup"><span data-stu-id="7fd6a-113">Size</span></span>              | <span data-ttu-id="7fd6a-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="7fd6a-114">8 bytes</span></span>                              |
| <span data-ttu-id="7fd6a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7fd6a-115">Update Privilege</span></span>  | <span data-ttu-id="7fd6a-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7fd6a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7fd6a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7fd6a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7fd6a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7fd6a-118">Attribute-Id</span></span>      | <span data-ttu-id="7fd6a-119">1.2.840.113556.1.4.370</span><span class="sxs-lookup"><span data-stu-id="7fd6a-119">1.2.840.113556.1.4.370</span></span>               |
| <span data-ttu-id="7fd6a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7fd6a-120">System-Id-Guid</span></span>    | <span data-ttu-id="7fd6a-121">66171888-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7fd6a-121">66171888-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="7fd6a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fd6a-122">Syntax</span></span>            | [<span data-ttu-id="7fd6a-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7fd6a-124">實作</span><span class="sxs-lookup"><span data-stu-id="7fd6a-124">Implementations</span></span>

-   [<span data-ttu-id="7fd6a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7fd6a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7fd6a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7fd6a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7fd6a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7fd6a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7fd6a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7fd6a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7fd6a-132">進入</span><span class="sxs-lookup"><span data-stu-id="7fd6a-132">Entry</span></span> | <span data-ttu-id="7fd6a-133">值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="7fd6a-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fd6a-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd6a-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd6a-136">System-Only</span></span>            | <span data-ttu-id="7fd6a-137">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-137">False</span></span>                                          |
| <span data-ttu-id="7fd6a-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd6a-139">對</span><span class="sxs-lookup"><span data-stu-id="7fd6a-139">True</span></span>                                           |
| <span data-ttu-id="7fd6a-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fd6a-140">Is Indexed</span></span>             | <span data-ttu-id="7fd6a-141">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-141">False</span></span>                                          |
| <span data-ttu-id="7fd6a-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fd6a-142">In Global Catalog</span></span>      | <span data-ttu-id="7fd6a-143">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-143">False</span></span>                                          |
| <span data-ttu-id="7fd6a-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fd6a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd6a-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fd6a-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="7fd6a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd6a-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd6a-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-148">Search-Flags</span></span>           | <span data-ttu-id="7fd6a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd6a-149">0x00000000</span></span>                                     |
| <span data-ttu-id="7fd6a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-150">System-Flags</span></span>           | <span data-ttu-id="7fd6a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7fd6a-151">0x00000010</span></span>                                     |
| <span data-ttu-id="7fd6a-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fd6a-152">Classes used in</span></span>        | [<span data-ttu-id="7fd6a-153">**RID 管理員**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-153">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7fd6a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7fd6a-154">Windows Server 2003</span></span>



| <span data-ttu-id="7fd6a-155">進入</span><span class="sxs-lookup"><span data-stu-id="7fd6a-155">Entry</span></span> | <span data-ttu-id="7fd6a-156">值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-156">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="7fd6a-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fd6a-157">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd6a-158">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd6a-159">System-Only</span></span>            | <span data-ttu-id="7fd6a-160">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-160">False</span></span>                                          |
| <span data-ttu-id="7fd6a-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd6a-162">對</span><span class="sxs-lookup"><span data-stu-id="7fd6a-162">True</span></span>                                           |
| <span data-ttu-id="7fd6a-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fd6a-163">Is Indexed</span></span>             | <span data-ttu-id="7fd6a-164">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-164">False</span></span>                                          |
| <span data-ttu-id="7fd6a-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fd6a-165">In Global Catalog</span></span>      | <span data-ttu-id="7fd6a-166">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-166">False</span></span>                                          |
| <span data-ttu-id="7fd6a-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fd6a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd6a-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fd6a-168">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="7fd6a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd6a-169">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd6a-170">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-171">Search-Flags</span></span>           | <span data-ttu-id="7fd6a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd6a-172">0x00000000</span></span>                                     |
| <span data-ttu-id="7fd6a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-173">System-Flags</span></span>           | <span data-ttu-id="7fd6a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7fd6a-174">0x00000010</span></span>                                     |
| <span data-ttu-id="7fd6a-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fd6a-175">Classes used in</span></span>        | [<span data-ttu-id="7fd6a-176">**RID 管理員**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-176">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7fd6a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7fd6a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7fd6a-178">進入</span><span class="sxs-lookup"><span data-stu-id="7fd6a-178">Entry</span></span> | <span data-ttu-id="7fd6a-179">值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-179">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="7fd6a-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fd6a-180">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd6a-181">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd6a-182">System-Only</span></span>            | <span data-ttu-id="7fd6a-183">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-183">False</span></span>                                          |
| <span data-ttu-id="7fd6a-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd6a-185">對</span><span class="sxs-lookup"><span data-stu-id="7fd6a-185">True</span></span>                                           |
| <span data-ttu-id="7fd6a-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fd6a-186">Is Indexed</span></span>             | <span data-ttu-id="7fd6a-187">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-187">False</span></span>                                          |
| <span data-ttu-id="7fd6a-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fd6a-188">In Global Catalog</span></span>      | <span data-ttu-id="7fd6a-189">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-189">False</span></span>                                          |
| <span data-ttu-id="7fd6a-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fd6a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd6a-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fd6a-191">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="7fd6a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd6a-192">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd6a-193">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-194">Search-Flags</span></span>           | <span data-ttu-id="7fd6a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd6a-195">0x00000000</span></span>                                     |
| <span data-ttu-id="7fd6a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-196">System-Flags</span></span>           | <span data-ttu-id="7fd6a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7fd6a-197">0x00000010</span></span>                                     |
| <span data-ttu-id="7fd6a-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fd6a-198">Classes used in</span></span>        | [<span data-ttu-id="7fd6a-199">**RID 管理員**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-199">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7fd6a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fd6a-200">Windows Server 2008</span></span>



| <span data-ttu-id="7fd6a-201">進入</span><span class="sxs-lookup"><span data-stu-id="7fd6a-201">Entry</span></span> | <span data-ttu-id="7fd6a-202">值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-202">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="7fd6a-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fd6a-203">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd6a-204">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd6a-205">System-Only</span></span>            | <span data-ttu-id="7fd6a-206">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-206">False</span></span>                                          |
| <span data-ttu-id="7fd6a-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd6a-208">對</span><span class="sxs-lookup"><span data-stu-id="7fd6a-208">True</span></span>                                           |
| <span data-ttu-id="7fd6a-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fd6a-209">Is Indexed</span></span>             | <span data-ttu-id="7fd6a-210">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-210">False</span></span>                                          |
| <span data-ttu-id="7fd6a-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fd6a-211">In Global Catalog</span></span>      | <span data-ttu-id="7fd6a-212">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-212">False</span></span>                                          |
| <span data-ttu-id="7fd6a-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fd6a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd6a-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fd6a-214">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="7fd6a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd6a-215">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd6a-216">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-217">Search-Flags</span></span>           | <span data-ttu-id="7fd6a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd6a-218">0x00000000</span></span>                                     |
| <span data-ttu-id="7fd6a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-219">System-Flags</span></span>           | <span data-ttu-id="7fd6a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7fd6a-220">0x00000010</span></span>                                     |
| <span data-ttu-id="7fd6a-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fd6a-221">Classes used in</span></span>        | [<span data-ttu-id="7fd6a-222">**RID 管理員**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-222">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7fd6a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7fd6a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7fd6a-224">進入</span><span class="sxs-lookup"><span data-stu-id="7fd6a-224">Entry</span></span> | <span data-ttu-id="7fd6a-225">值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-225">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="7fd6a-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fd6a-226">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd6a-227">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd6a-228">System-Only</span></span>            | <span data-ttu-id="7fd6a-229">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-229">False</span></span>                                          |
| <span data-ttu-id="7fd6a-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd6a-231">對</span><span class="sxs-lookup"><span data-stu-id="7fd6a-231">True</span></span>                                           |
| <span data-ttu-id="7fd6a-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fd6a-232">Is Indexed</span></span>             | <span data-ttu-id="7fd6a-233">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-233">False</span></span>                                          |
| <span data-ttu-id="7fd6a-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fd6a-234">In Global Catalog</span></span>      | <span data-ttu-id="7fd6a-235">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-235">False</span></span>                                          |
| <span data-ttu-id="7fd6a-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fd6a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd6a-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fd6a-237">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="7fd6a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd6a-238">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd6a-239">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-240">Search-Flags</span></span>           | <span data-ttu-id="7fd6a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd6a-241">0x00000000</span></span>                                     |
| <span data-ttu-id="7fd6a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-242">System-Flags</span></span>           | <span data-ttu-id="7fd6a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7fd6a-243">0x00000010</span></span>                                     |
| <span data-ttu-id="7fd6a-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fd6a-244">Classes used in</span></span>        | [<span data-ttu-id="7fd6a-245">**RID 管理員**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-245">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7fd6a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7fd6a-246">Windows Server 2012</span></span>



| <span data-ttu-id="7fd6a-247">進入</span><span class="sxs-lookup"><span data-stu-id="7fd6a-247">Entry</span></span> | <span data-ttu-id="7fd6a-248">值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-248">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="7fd6a-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7fd6a-249">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7fd6a-250">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="7fd6a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7fd6a-251">System-Only</span></span>            | <span data-ttu-id="7fd6a-252">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-252">False</span></span>                                          |
| <span data-ttu-id="7fd6a-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7fd6a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7fd6a-254">對</span><span class="sxs-lookup"><span data-stu-id="7fd6a-254">True</span></span>                                           |
| <span data-ttu-id="7fd6a-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7fd6a-255">Is Indexed</span></span>             | <span data-ttu-id="7fd6a-256">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-256">False</span></span>                                          |
| <span data-ttu-id="7fd6a-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7fd6a-257">In Global Catalog</span></span>      | <span data-ttu-id="7fd6a-258">否</span><span class="sxs-lookup"><span data-stu-id="7fd6a-258">False</span></span>                                          |
| <span data-ttu-id="7fd6a-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7fd6a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7fd6a-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7fd6a-260">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="7fd6a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7fd6a-261">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7fd6a-262">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="7fd6a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-263">Search-Flags</span></span>           | <span data-ttu-id="7fd6a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7fd6a-264">0x00000000</span></span>                                     |
| <span data-ttu-id="7fd6a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7fd6a-265">System-Flags</span></span>           | <span data-ttu-id="7fd6a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7fd6a-266">0x00000010</span></span>                                     |
| <span data-ttu-id="7fd6a-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7fd6a-267">Classes used in</span></span>        | [<span data-ttu-id="7fd6a-268">**RID 管理員**</span><span class="sxs-lookup"><span data-stu-id="7fd6a-268">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



 

 





