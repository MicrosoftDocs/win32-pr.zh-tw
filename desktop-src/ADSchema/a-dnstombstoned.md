---
title: DNS-Tombstoned 屬性
description: 如果此物件已被加上標記，則為 True。 這個屬性可讓您更輕鬆且快速地搜尋已標記的記錄。 已刪除的物件是已刪除但尚未從目錄移除的物件。
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- DNS-Tombstoned 屬性 AD 架構
- dNSTombstoned 屬性 AD 架構
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844764"
---
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="10161-107">DNS-Tombstoned 屬性</span><span class="sxs-lookup"><span data-stu-id="10161-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="10161-108">如果此物件已被加上標記，則為 True。</span><span class="sxs-lookup"><span data-stu-id="10161-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="10161-109">這個屬性可讓您更輕鬆且快速地搜尋已標記的記錄。</span><span class="sxs-lookup"><span data-stu-id="10161-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="10161-110">已刪除的物件是已刪除但尚未從目錄移除的物件。</span><span class="sxs-lookup"><span data-stu-id="10161-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="10161-111">進入</span><span class="sxs-lookup"><span data-stu-id="10161-111">Entry</span></span> | <span data-ttu-id="10161-112">值</span><span class="sxs-lookup"><span data-stu-id="10161-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="10161-113">CN</span><span class="sxs-lookup"><span data-stu-id="10161-113">CN</span></span>                | <span data-ttu-id="10161-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="10161-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="10161-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="10161-115">Ldap-Display-Name</span></span> | <span data-ttu-id="10161-116">dNSTombstoned</span><span class="sxs-lookup"><span data-stu-id="10161-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="10161-117">大小</span><span class="sxs-lookup"><span data-stu-id="10161-117">Size</span></span>              | <span data-ttu-id="10161-118">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="10161-118">4 bytes</span></span>                              |
| <span data-ttu-id="10161-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="10161-119">Update Privilege</span></span>  | <span data-ttu-id="10161-120">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="10161-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="10161-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="10161-121">Update Frequency</span></span>  | <span data-ttu-id="10161-122">每次刪除物件時。</span><span class="sxs-lookup"><span data-stu-id="10161-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="10161-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="10161-123">Attribute-Id</span></span>      | <span data-ttu-id="10161-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="10161-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="10161-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="10161-125">System-Id-Guid</span></span>    | <span data-ttu-id="10161-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="10161-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="10161-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="10161-127">Syntax</span></span>            | [<span data-ttu-id="10161-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="10161-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="10161-129">實作</span><span class="sxs-lookup"><span data-stu-id="10161-129">Implementations</span></span>

-   [<span data-ttu-id="10161-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="10161-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="10161-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="10161-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="10161-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="10161-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="10161-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="10161-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="10161-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="10161-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="10161-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="10161-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="10161-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10161-136">Windows 2000 Server</span></span>



| <span data-ttu-id="10161-137">進入</span><span class="sxs-lookup"><span data-stu-id="10161-137">Entry</span></span> | <span data-ttu-id="10161-138">值</span><span class="sxs-lookup"><span data-stu-id="10161-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="10161-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10161-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10161-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="10161-141">System-Only</span></span>            | <span data-ttu-id="10161-142">否</span><span class="sxs-lookup"><span data-stu-id="10161-142">False</span></span>                                    |
| <span data-ttu-id="10161-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10161-143">Is-Single-Valued</span></span>       | <span data-ttu-id="10161-144">對</span><span class="sxs-lookup"><span data-stu-id="10161-144">True</span></span>                                     |
| <span data-ttu-id="10161-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10161-145">Is Indexed</span></span>             | <span data-ttu-id="10161-146">對</span><span class="sxs-lookup"><span data-stu-id="10161-146">True</span></span>                                     |
| <span data-ttu-id="10161-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10161-147">In Global Catalog</span></span>      | <span data-ttu-id="10161-148">否</span><span class="sxs-lookup"><span data-stu-id="10161-148">False</span></span>                                    |
| <span data-ttu-id="10161-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10161-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="10161-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10161-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="10161-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10161-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="10161-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10161-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="10161-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-153">Search-Flags</span></span>           | <span data-ttu-id="10161-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10161-154">0x00000001</span></span>                               |
| <span data-ttu-id="10161-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-155">System-Flags</span></span>           | <span data-ttu-id="10161-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10161-156">0x00000010</span></span>                               |
| <span data-ttu-id="10161-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10161-157">Classes used in</span></span>        | [<span data-ttu-id="10161-158">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="10161-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="10161-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10161-159">Windows Server 2003</span></span>



| <span data-ttu-id="10161-160">進入</span><span class="sxs-lookup"><span data-stu-id="10161-160">Entry</span></span> | <span data-ttu-id="10161-161">值</span><span class="sxs-lookup"><span data-stu-id="10161-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="10161-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10161-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10161-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="10161-164">System-Only</span></span>            | <span data-ttu-id="10161-165">否</span><span class="sxs-lookup"><span data-stu-id="10161-165">False</span></span>                                    |
| <span data-ttu-id="10161-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10161-166">Is-Single-Valued</span></span>       | <span data-ttu-id="10161-167">對</span><span class="sxs-lookup"><span data-stu-id="10161-167">True</span></span>                                     |
| <span data-ttu-id="10161-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10161-168">Is Indexed</span></span>             | <span data-ttu-id="10161-169">對</span><span class="sxs-lookup"><span data-stu-id="10161-169">True</span></span>                                     |
| <span data-ttu-id="10161-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10161-170">In Global Catalog</span></span>      | <span data-ttu-id="10161-171">否</span><span class="sxs-lookup"><span data-stu-id="10161-171">False</span></span>                                    |
| <span data-ttu-id="10161-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10161-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="10161-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10161-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="10161-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10161-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="10161-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10161-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="10161-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-176">Search-Flags</span></span>           | <span data-ttu-id="10161-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10161-177">0x00000001</span></span>                               |
| <span data-ttu-id="10161-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-178">System-Flags</span></span>           | <span data-ttu-id="10161-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10161-179">0x00000010</span></span>                               |
| <span data-ttu-id="10161-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10161-180">Classes used in</span></span>        | [<span data-ttu-id="10161-181">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="10161-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="10161-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10161-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="10161-183">進入</span><span class="sxs-lookup"><span data-stu-id="10161-183">Entry</span></span> | <span data-ttu-id="10161-184">值</span><span class="sxs-lookup"><span data-stu-id="10161-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="10161-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10161-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10161-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="10161-187">System-Only</span></span>            | <span data-ttu-id="10161-188">否</span><span class="sxs-lookup"><span data-stu-id="10161-188">False</span></span>                                    |
| <span data-ttu-id="10161-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10161-189">Is-Single-Valued</span></span>       | <span data-ttu-id="10161-190">對</span><span class="sxs-lookup"><span data-stu-id="10161-190">True</span></span>                                     |
| <span data-ttu-id="10161-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10161-191">Is Indexed</span></span>             | <span data-ttu-id="10161-192">對</span><span class="sxs-lookup"><span data-stu-id="10161-192">True</span></span>                                     |
| <span data-ttu-id="10161-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10161-193">In Global Catalog</span></span>      | <span data-ttu-id="10161-194">否</span><span class="sxs-lookup"><span data-stu-id="10161-194">False</span></span>                                    |
| <span data-ttu-id="10161-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10161-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="10161-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10161-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="10161-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10161-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="10161-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10161-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="10161-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-199">Search-Flags</span></span>           | <span data-ttu-id="10161-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10161-200">0x00000001</span></span>                               |
| <span data-ttu-id="10161-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-201">System-Flags</span></span>           | <span data-ttu-id="10161-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10161-202">0x00000010</span></span>                               |
| <span data-ttu-id="10161-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10161-203">Classes used in</span></span>        | [<span data-ttu-id="10161-204">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="10161-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="10161-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10161-205">Windows Server 2008</span></span>



| <span data-ttu-id="10161-206">進入</span><span class="sxs-lookup"><span data-stu-id="10161-206">Entry</span></span> | <span data-ttu-id="10161-207">值</span><span class="sxs-lookup"><span data-stu-id="10161-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="10161-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10161-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10161-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="10161-210">System-Only</span></span>            | <span data-ttu-id="10161-211">否</span><span class="sxs-lookup"><span data-stu-id="10161-211">False</span></span>                                    |
| <span data-ttu-id="10161-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10161-212">Is-Single-Valued</span></span>       | <span data-ttu-id="10161-213">對</span><span class="sxs-lookup"><span data-stu-id="10161-213">True</span></span>                                     |
| <span data-ttu-id="10161-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10161-214">Is Indexed</span></span>             | <span data-ttu-id="10161-215">對</span><span class="sxs-lookup"><span data-stu-id="10161-215">True</span></span>                                     |
| <span data-ttu-id="10161-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10161-216">In Global Catalog</span></span>      | <span data-ttu-id="10161-217">否</span><span class="sxs-lookup"><span data-stu-id="10161-217">False</span></span>                                    |
| <span data-ttu-id="10161-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10161-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="10161-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10161-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="10161-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10161-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="10161-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10161-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="10161-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-222">Search-Flags</span></span>           | <span data-ttu-id="10161-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10161-223">0x00000001</span></span>                               |
| <span data-ttu-id="10161-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-224">System-Flags</span></span>           | <span data-ttu-id="10161-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10161-225">0x00000010</span></span>                               |
| <span data-ttu-id="10161-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10161-226">Classes used in</span></span>        | [<span data-ttu-id="10161-227">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="10161-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="10161-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10161-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="10161-229">進入</span><span class="sxs-lookup"><span data-stu-id="10161-229">Entry</span></span> | <span data-ttu-id="10161-230">值</span><span class="sxs-lookup"><span data-stu-id="10161-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="10161-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10161-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10161-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="10161-233">System-Only</span></span>            | <span data-ttu-id="10161-234">否</span><span class="sxs-lookup"><span data-stu-id="10161-234">False</span></span>                                    |
| <span data-ttu-id="10161-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10161-235">Is-Single-Valued</span></span>       | <span data-ttu-id="10161-236">對</span><span class="sxs-lookup"><span data-stu-id="10161-236">True</span></span>                                     |
| <span data-ttu-id="10161-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10161-237">Is Indexed</span></span>             | <span data-ttu-id="10161-238">對</span><span class="sxs-lookup"><span data-stu-id="10161-238">True</span></span>                                     |
| <span data-ttu-id="10161-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10161-239">In Global Catalog</span></span>      | <span data-ttu-id="10161-240">否</span><span class="sxs-lookup"><span data-stu-id="10161-240">False</span></span>                                    |
| <span data-ttu-id="10161-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10161-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="10161-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10161-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="10161-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10161-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="10161-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10161-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="10161-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-245">Search-Flags</span></span>           | <span data-ttu-id="10161-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10161-246">0x00000001</span></span>                               |
| <span data-ttu-id="10161-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-247">System-Flags</span></span>           | <span data-ttu-id="10161-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10161-248">0x00000010</span></span>                               |
| <span data-ttu-id="10161-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10161-249">Classes used in</span></span>        | [<span data-ttu-id="10161-250">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="10161-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="10161-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10161-251">Windows Server 2012</span></span>



| <span data-ttu-id="10161-252">進入</span><span class="sxs-lookup"><span data-stu-id="10161-252">Entry</span></span> | <span data-ttu-id="10161-253">值</span><span class="sxs-lookup"><span data-stu-id="10161-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="10161-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10161-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10161-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="10161-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="10161-256">System-Only</span></span>            | <span data-ttu-id="10161-257">否</span><span class="sxs-lookup"><span data-stu-id="10161-257">False</span></span>                                    |
| <span data-ttu-id="10161-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10161-258">Is-Single-Valued</span></span>       | <span data-ttu-id="10161-259">對</span><span class="sxs-lookup"><span data-stu-id="10161-259">True</span></span>                                     |
| <span data-ttu-id="10161-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10161-260">Is Indexed</span></span>             | <span data-ttu-id="10161-261">對</span><span class="sxs-lookup"><span data-stu-id="10161-261">True</span></span>                                     |
| <span data-ttu-id="10161-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10161-262">In Global Catalog</span></span>      | <span data-ttu-id="10161-263">否</span><span class="sxs-lookup"><span data-stu-id="10161-263">False</span></span>                                    |
| <span data-ttu-id="10161-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10161-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="10161-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10161-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="10161-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10161-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="10161-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10161-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="10161-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-268">Search-Flags</span></span>           | <span data-ttu-id="10161-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10161-269">0x00000001</span></span>                               |
| <span data-ttu-id="10161-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10161-270">System-Flags</span></span>           | <span data-ttu-id="10161-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10161-271">0x00000010</span></span>                               |
| <span data-ttu-id="10161-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10161-272">Classes used in</span></span>        | [<span data-ttu-id="10161-273">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="10161-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





