---
title: RID-下一個 RID 屬性
description: 目前集區中的下一個可用相對識別碼。
ms.assetid: 6e2339b2-fd4a-4175-a854-c0a4bd9ac599
ms.tgt_platform: multiple
keywords:
- RID-下一個 RID 屬性 AD 架構
- rIDNextRID 屬性 AD 架構
topic_type:
- apiref
api_name:
- RID-Next-RID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054d469bf5e6f29e7714e621b04270959b1df4e9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973326"
---
# <a name="rid-next-rid-attribute"></a><span data-ttu-id="90d96-105">RID-下一個 RID 屬性</span><span class="sxs-lookup"><span data-stu-id="90d96-105">RID-Next-RID attribute</span></span>

<span data-ttu-id="90d96-106">目前集區中的下一個可用相對識別碼。</span><span class="sxs-lookup"><span data-stu-id="90d96-106">The next free Relative Identifier in the current pool.</span></span>



| <span data-ttu-id="90d96-107">進入</span><span class="sxs-lookup"><span data-stu-id="90d96-107">Entry</span></span> | <span data-ttu-id="90d96-108">值</span><span class="sxs-lookup"><span data-stu-id="90d96-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="90d96-109">CN</span><span class="sxs-lookup"><span data-stu-id="90d96-109">CN</span></span>                | <span data-ttu-id="90d96-110">RID-下一個 RID</span><span class="sxs-lookup"><span data-stu-id="90d96-110">RID-Next-RID</span></span>                         |
| <span data-ttu-id="90d96-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="90d96-111">Ldap-Display-Name</span></span> | <span data-ttu-id="90d96-112">rIDNextRID</span><span class="sxs-lookup"><span data-stu-id="90d96-112">rIDNextRID</span></span>                           |
| <span data-ttu-id="90d96-113">大小</span><span class="sxs-lookup"><span data-stu-id="90d96-113">Size</span></span>              | <span data-ttu-id="90d96-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="90d96-114">4 bytes</span></span>                              |
| <span data-ttu-id="90d96-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="90d96-115">Update Privilege</span></span>  | <span data-ttu-id="90d96-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="90d96-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="90d96-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="90d96-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="90d96-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90d96-118">Attribute-Id</span></span>      | <span data-ttu-id="90d96-119">1.2.840.113556.1.4.374</span><span class="sxs-lookup"><span data-stu-id="90d96-119">1.2.840.113556.1.4.374</span></span>               |
| <span data-ttu-id="90d96-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="90d96-120">System-Id-Guid</span></span>    | <span data-ttu-id="90d96-121">6617188c-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="90d96-121">6617188c-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="90d96-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="90d96-122">Syntax</span></span>            | [<span data-ttu-id="90d96-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="90d96-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="90d96-124">實作</span><span class="sxs-lookup"><span data-stu-id="90d96-124">Implementations</span></span>

-   [<span data-ttu-id="90d96-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="90d96-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="90d96-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90d96-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90d96-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90d96-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90d96-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90d96-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90d96-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90d96-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90d96-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90d96-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="90d96-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90d96-131">Windows 2000 Server</span></span>



| <span data-ttu-id="90d96-132">進入</span><span class="sxs-lookup"><span data-stu-id="90d96-132">Entry</span></span> | <span data-ttu-id="90d96-133">值</span><span class="sxs-lookup"><span data-stu-id="90d96-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="90d96-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90d96-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90d96-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="90d96-136">System-Only</span></span>            | <span data-ttu-id="90d96-137">對</span><span class="sxs-lookup"><span data-stu-id="90d96-137">True</span></span>                                   |
| <span data-ttu-id="90d96-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90d96-138">Is-Single-Valued</span></span>       | <span data-ttu-id="90d96-139">對</span><span class="sxs-lookup"><span data-stu-id="90d96-139">True</span></span>                                   |
| <span data-ttu-id="90d96-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90d96-140">Is Indexed</span></span>             | <span data-ttu-id="90d96-141">否</span><span class="sxs-lookup"><span data-stu-id="90d96-141">False</span></span>                                  |
| <span data-ttu-id="90d96-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90d96-142">In Global Catalog</span></span>      | <span data-ttu-id="90d96-143">否</span><span class="sxs-lookup"><span data-stu-id="90d96-143">False</span></span>                                  |
| <span data-ttu-id="90d96-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90d96-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="90d96-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90d96-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="90d96-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90d96-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="90d96-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90d96-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="90d96-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-148">Search-Flags</span></span>           | <span data-ttu-id="90d96-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90d96-149">0x00000000</span></span>                             |
| <span data-ttu-id="90d96-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-150">System-Flags</span></span>           | <span data-ttu-id="90d96-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="90d96-151">0x00000011</span></span>                             |
| <span data-ttu-id="90d96-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90d96-152">Classes used in</span></span>        | [<span data-ttu-id="90d96-153">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="90d96-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="90d96-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90d96-154">Windows Server 2003</span></span>



| <span data-ttu-id="90d96-155">進入</span><span class="sxs-lookup"><span data-stu-id="90d96-155">Entry</span></span> | <span data-ttu-id="90d96-156">值</span><span class="sxs-lookup"><span data-stu-id="90d96-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="90d96-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90d96-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90d96-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="90d96-159">System-Only</span></span>            | <span data-ttu-id="90d96-160">對</span><span class="sxs-lookup"><span data-stu-id="90d96-160">True</span></span>                                   |
| <span data-ttu-id="90d96-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90d96-161">Is-Single-Valued</span></span>       | <span data-ttu-id="90d96-162">對</span><span class="sxs-lookup"><span data-stu-id="90d96-162">True</span></span>                                   |
| <span data-ttu-id="90d96-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90d96-163">Is Indexed</span></span>             | <span data-ttu-id="90d96-164">否</span><span class="sxs-lookup"><span data-stu-id="90d96-164">False</span></span>                                  |
| <span data-ttu-id="90d96-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90d96-165">In Global Catalog</span></span>      | <span data-ttu-id="90d96-166">否</span><span class="sxs-lookup"><span data-stu-id="90d96-166">False</span></span>                                  |
| <span data-ttu-id="90d96-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90d96-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="90d96-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90d96-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="90d96-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90d96-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="90d96-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90d96-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="90d96-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-171">Search-Flags</span></span>           | <span data-ttu-id="90d96-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90d96-172">0x00000000</span></span>                             |
| <span data-ttu-id="90d96-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-173">System-Flags</span></span>           | <span data-ttu-id="90d96-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="90d96-174">0x00000011</span></span>                             |
| <span data-ttu-id="90d96-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90d96-175">Classes used in</span></span>        | [<span data-ttu-id="90d96-176">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="90d96-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90d96-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90d96-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90d96-178">進入</span><span class="sxs-lookup"><span data-stu-id="90d96-178">Entry</span></span> | <span data-ttu-id="90d96-179">值</span><span class="sxs-lookup"><span data-stu-id="90d96-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="90d96-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90d96-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90d96-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="90d96-182">System-Only</span></span>            | <span data-ttu-id="90d96-183">對</span><span class="sxs-lookup"><span data-stu-id="90d96-183">True</span></span>                                   |
| <span data-ttu-id="90d96-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90d96-184">Is-Single-Valued</span></span>       | <span data-ttu-id="90d96-185">對</span><span class="sxs-lookup"><span data-stu-id="90d96-185">True</span></span>                                   |
| <span data-ttu-id="90d96-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90d96-186">Is Indexed</span></span>             | <span data-ttu-id="90d96-187">否</span><span class="sxs-lookup"><span data-stu-id="90d96-187">False</span></span>                                  |
| <span data-ttu-id="90d96-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90d96-188">In Global Catalog</span></span>      | <span data-ttu-id="90d96-189">否</span><span class="sxs-lookup"><span data-stu-id="90d96-189">False</span></span>                                  |
| <span data-ttu-id="90d96-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90d96-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="90d96-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90d96-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="90d96-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90d96-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="90d96-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90d96-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="90d96-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-194">Search-Flags</span></span>           | <span data-ttu-id="90d96-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90d96-195">0x00000000</span></span>                             |
| <span data-ttu-id="90d96-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-196">System-Flags</span></span>           | <span data-ttu-id="90d96-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="90d96-197">0x00000011</span></span>                             |
| <span data-ttu-id="90d96-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90d96-198">Classes used in</span></span>        | [<span data-ttu-id="90d96-199">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="90d96-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90d96-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90d96-200">Windows Server 2008</span></span>



| <span data-ttu-id="90d96-201">進入</span><span class="sxs-lookup"><span data-stu-id="90d96-201">Entry</span></span> | <span data-ttu-id="90d96-202">值</span><span class="sxs-lookup"><span data-stu-id="90d96-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="90d96-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90d96-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90d96-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="90d96-205">System-Only</span></span>            | <span data-ttu-id="90d96-206">對</span><span class="sxs-lookup"><span data-stu-id="90d96-206">True</span></span>                                   |
| <span data-ttu-id="90d96-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90d96-207">Is-Single-Valued</span></span>       | <span data-ttu-id="90d96-208">對</span><span class="sxs-lookup"><span data-stu-id="90d96-208">True</span></span>                                   |
| <span data-ttu-id="90d96-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90d96-209">Is Indexed</span></span>             | <span data-ttu-id="90d96-210">否</span><span class="sxs-lookup"><span data-stu-id="90d96-210">False</span></span>                                  |
| <span data-ttu-id="90d96-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90d96-211">In Global Catalog</span></span>      | <span data-ttu-id="90d96-212">否</span><span class="sxs-lookup"><span data-stu-id="90d96-212">False</span></span>                                  |
| <span data-ttu-id="90d96-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90d96-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="90d96-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90d96-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="90d96-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90d96-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="90d96-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90d96-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="90d96-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-217">Search-Flags</span></span>           | <span data-ttu-id="90d96-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90d96-218">0x00000000</span></span>                             |
| <span data-ttu-id="90d96-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-219">System-Flags</span></span>           | <span data-ttu-id="90d96-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="90d96-220">0x00000011</span></span>                             |
| <span data-ttu-id="90d96-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90d96-221">Classes used in</span></span>        | [<span data-ttu-id="90d96-222">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="90d96-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90d96-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90d96-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90d96-224">進入</span><span class="sxs-lookup"><span data-stu-id="90d96-224">Entry</span></span> | <span data-ttu-id="90d96-225">值</span><span class="sxs-lookup"><span data-stu-id="90d96-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="90d96-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90d96-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90d96-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="90d96-228">System-Only</span></span>            | <span data-ttu-id="90d96-229">對</span><span class="sxs-lookup"><span data-stu-id="90d96-229">True</span></span>                                   |
| <span data-ttu-id="90d96-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90d96-230">Is-Single-Valued</span></span>       | <span data-ttu-id="90d96-231">對</span><span class="sxs-lookup"><span data-stu-id="90d96-231">True</span></span>                                   |
| <span data-ttu-id="90d96-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90d96-232">Is Indexed</span></span>             | <span data-ttu-id="90d96-233">否</span><span class="sxs-lookup"><span data-stu-id="90d96-233">False</span></span>                                  |
| <span data-ttu-id="90d96-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90d96-234">In Global Catalog</span></span>      | <span data-ttu-id="90d96-235">否</span><span class="sxs-lookup"><span data-stu-id="90d96-235">False</span></span>                                  |
| <span data-ttu-id="90d96-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90d96-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="90d96-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90d96-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="90d96-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90d96-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="90d96-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90d96-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="90d96-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-240">Search-Flags</span></span>           | <span data-ttu-id="90d96-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90d96-241">0x00000000</span></span>                             |
| <span data-ttu-id="90d96-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-242">System-Flags</span></span>           | <span data-ttu-id="90d96-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="90d96-243">0x00000011</span></span>                             |
| <span data-ttu-id="90d96-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90d96-244">Classes used in</span></span>        | [<span data-ttu-id="90d96-245">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="90d96-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90d96-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90d96-246">Windows Server 2012</span></span>



| <span data-ttu-id="90d96-247">進入</span><span class="sxs-lookup"><span data-stu-id="90d96-247">Entry</span></span> | <span data-ttu-id="90d96-248">值</span><span class="sxs-lookup"><span data-stu-id="90d96-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="90d96-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90d96-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90d96-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="90d96-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="90d96-251">System-Only</span></span>            | <span data-ttu-id="90d96-252">對</span><span class="sxs-lookup"><span data-stu-id="90d96-252">True</span></span>                                   |
| <span data-ttu-id="90d96-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90d96-253">Is-Single-Valued</span></span>       | <span data-ttu-id="90d96-254">對</span><span class="sxs-lookup"><span data-stu-id="90d96-254">True</span></span>                                   |
| <span data-ttu-id="90d96-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90d96-255">Is Indexed</span></span>             | <span data-ttu-id="90d96-256">否</span><span class="sxs-lookup"><span data-stu-id="90d96-256">False</span></span>                                  |
| <span data-ttu-id="90d96-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90d96-257">In Global Catalog</span></span>      | <span data-ttu-id="90d96-258">否</span><span class="sxs-lookup"><span data-stu-id="90d96-258">False</span></span>                                  |
| <span data-ttu-id="90d96-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90d96-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="90d96-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90d96-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="90d96-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90d96-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="90d96-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90d96-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="90d96-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-263">Search-Flags</span></span>           | <span data-ttu-id="90d96-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90d96-264">0x00000000</span></span>                             |
| <span data-ttu-id="90d96-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90d96-265">System-Flags</span></span>           | <span data-ttu-id="90d96-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="90d96-266">0x00000011</span></span>                             |
| <span data-ttu-id="90d96-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90d96-267">Classes used in</span></span>        | [<span data-ttu-id="90d96-268">**RID 集**</span><span class="sxs-lookup"><span data-stu-id="90d96-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 





