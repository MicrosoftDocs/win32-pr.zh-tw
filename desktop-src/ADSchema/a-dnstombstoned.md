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
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="72f4e-107">DNS-Tombstoned 屬性</span><span class="sxs-lookup"><span data-stu-id="72f4e-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="72f4e-108">如果此物件已被加上標記，則為 True。</span><span class="sxs-lookup"><span data-stu-id="72f4e-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="72f4e-109">這個屬性可讓您更輕鬆且快速地搜尋已標記的記錄。</span><span class="sxs-lookup"><span data-stu-id="72f4e-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="72f4e-110">已刪除的物件是已刪除但尚未從目錄移除的物件。</span><span class="sxs-lookup"><span data-stu-id="72f4e-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="72f4e-111">進入</span><span class="sxs-lookup"><span data-stu-id="72f4e-111">Entry</span></span> | <span data-ttu-id="72f4e-112">值</span><span class="sxs-lookup"><span data-stu-id="72f4e-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="72f4e-113">CN</span><span class="sxs-lookup"><span data-stu-id="72f4e-113">CN</span></span>                | <span data-ttu-id="72f4e-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="72f4e-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="72f4e-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="72f4e-115">Ldap-Display-Name</span></span> | <span data-ttu-id="72f4e-116">dNSTombstoned</span><span class="sxs-lookup"><span data-stu-id="72f4e-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="72f4e-117">大小</span><span class="sxs-lookup"><span data-stu-id="72f4e-117">Size</span></span>              | <span data-ttu-id="72f4e-118">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="72f4e-118">4 bytes</span></span>                              |
| <span data-ttu-id="72f4e-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="72f4e-119">Update Privilege</span></span>  | <span data-ttu-id="72f4e-120">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="72f4e-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="72f4e-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="72f4e-121">Update Frequency</span></span>  | <span data-ttu-id="72f4e-122">每次刪除物件時。</span><span class="sxs-lookup"><span data-stu-id="72f4e-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="72f4e-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72f4e-123">Attribute-Id</span></span>      | <span data-ttu-id="72f4e-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="72f4e-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="72f4e-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="72f4e-125">System-Id-Guid</span></span>    | <span data-ttu-id="72f4e-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="72f4e-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="72f4e-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="72f4e-127">Syntax</span></span>            | [<span data-ttu-id="72f4e-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="72f4e-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="72f4e-129">實作</span><span class="sxs-lookup"><span data-stu-id="72f4e-129">Implementations</span></span>

-   [<span data-ttu-id="72f4e-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72f4e-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72f4e-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72f4e-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72f4e-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72f4e-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72f4e-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72f4e-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72f4e-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72f4e-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72f4e-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72f4e-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72f4e-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72f4e-136">Windows 2000 Server</span></span>



| <span data-ttu-id="72f4e-137">進入</span><span class="sxs-lookup"><span data-stu-id="72f4e-137">Entry</span></span> | <span data-ttu-id="72f4e-138">值</span><span class="sxs-lookup"><span data-stu-id="72f4e-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="72f4e-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72f4e-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72f4e-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="72f4e-141">System-Only</span></span>            | <span data-ttu-id="72f4e-142">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-142">False</span></span>                                    |
| <span data-ttu-id="72f4e-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72f4e-143">Is-Single-Valued</span></span>       | <span data-ttu-id="72f4e-144">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-144">True</span></span>                                     |
| <span data-ttu-id="72f4e-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72f4e-145">Is Indexed</span></span>             | <span data-ttu-id="72f4e-146">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-146">True</span></span>                                     |
| <span data-ttu-id="72f4e-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72f4e-147">In Global Catalog</span></span>      | <span data-ttu-id="72f4e-148">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-148">False</span></span>                                    |
| <span data-ttu-id="72f4e-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72f4e-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="72f4e-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72f4e-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="72f4e-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72f4e-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72f4e-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-153">Search-Flags</span></span>           | <span data-ttu-id="72f4e-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72f4e-154">0x00000001</span></span>                               |
| <span data-ttu-id="72f4e-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-155">System-Flags</span></span>           | <span data-ttu-id="72f4e-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72f4e-156">0x00000010</span></span>                               |
| <span data-ttu-id="72f4e-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72f4e-157">Classes used in</span></span>        | [<span data-ttu-id="72f4e-158">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="72f4e-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72f4e-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72f4e-159">Windows Server 2003</span></span>



| <span data-ttu-id="72f4e-160">進入</span><span class="sxs-lookup"><span data-stu-id="72f4e-160">Entry</span></span> | <span data-ttu-id="72f4e-161">值</span><span class="sxs-lookup"><span data-stu-id="72f4e-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="72f4e-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72f4e-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72f4e-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="72f4e-164">System-Only</span></span>            | <span data-ttu-id="72f4e-165">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-165">False</span></span>                                    |
| <span data-ttu-id="72f4e-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72f4e-166">Is-Single-Valued</span></span>       | <span data-ttu-id="72f4e-167">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-167">True</span></span>                                     |
| <span data-ttu-id="72f4e-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72f4e-168">Is Indexed</span></span>             | <span data-ttu-id="72f4e-169">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-169">True</span></span>                                     |
| <span data-ttu-id="72f4e-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72f4e-170">In Global Catalog</span></span>      | <span data-ttu-id="72f4e-171">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-171">False</span></span>                                    |
| <span data-ttu-id="72f4e-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72f4e-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="72f4e-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72f4e-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="72f4e-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72f4e-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72f4e-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-176">Search-Flags</span></span>           | <span data-ttu-id="72f4e-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72f4e-177">0x00000001</span></span>                               |
| <span data-ttu-id="72f4e-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-178">System-Flags</span></span>           | <span data-ttu-id="72f4e-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72f4e-179">0x00000010</span></span>                               |
| <span data-ttu-id="72f4e-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72f4e-180">Classes used in</span></span>        | [<span data-ttu-id="72f4e-181">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="72f4e-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72f4e-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72f4e-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72f4e-183">進入</span><span class="sxs-lookup"><span data-stu-id="72f4e-183">Entry</span></span> | <span data-ttu-id="72f4e-184">值</span><span class="sxs-lookup"><span data-stu-id="72f4e-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="72f4e-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72f4e-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72f4e-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="72f4e-187">System-Only</span></span>            | <span data-ttu-id="72f4e-188">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-188">False</span></span>                                    |
| <span data-ttu-id="72f4e-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72f4e-189">Is-Single-Valued</span></span>       | <span data-ttu-id="72f4e-190">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-190">True</span></span>                                     |
| <span data-ttu-id="72f4e-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72f4e-191">Is Indexed</span></span>             | <span data-ttu-id="72f4e-192">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-192">True</span></span>                                     |
| <span data-ttu-id="72f4e-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72f4e-193">In Global Catalog</span></span>      | <span data-ttu-id="72f4e-194">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-194">False</span></span>                                    |
| <span data-ttu-id="72f4e-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72f4e-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="72f4e-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72f4e-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="72f4e-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72f4e-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72f4e-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-199">Search-Flags</span></span>           | <span data-ttu-id="72f4e-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72f4e-200">0x00000001</span></span>                               |
| <span data-ttu-id="72f4e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-201">System-Flags</span></span>           | <span data-ttu-id="72f4e-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72f4e-202">0x00000010</span></span>                               |
| <span data-ttu-id="72f4e-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72f4e-203">Classes used in</span></span>        | [<span data-ttu-id="72f4e-204">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="72f4e-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72f4e-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72f4e-205">Windows Server 2008</span></span>



| <span data-ttu-id="72f4e-206">進入</span><span class="sxs-lookup"><span data-stu-id="72f4e-206">Entry</span></span> | <span data-ttu-id="72f4e-207">值</span><span class="sxs-lookup"><span data-stu-id="72f4e-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="72f4e-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72f4e-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72f4e-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="72f4e-210">System-Only</span></span>            | <span data-ttu-id="72f4e-211">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-211">False</span></span>                                    |
| <span data-ttu-id="72f4e-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72f4e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="72f4e-213">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-213">True</span></span>                                     |
| <span data-ttu-id="72f4e-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72f4e-214">Is Indexed</span></span>             | <span data-ttu-id="72f4e-215">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-215">True</span></span>                                     |
| <span data-ttu-id="72f4e-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72f4e-216">In Global Catalog</span></span>      | <span data-ttu-id="72f4e-217">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-217">False</span></span>                                    |
| <span data-ttu-id="72f4e-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72f4e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="72f4e-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72f4e-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="72f4e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72f4e-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72f4e-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-222">Search-Flags</span></span>           | <span data-ttu-id="72f4e-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72f4e-223">0x00000001</span></span>                               |
| <span data-ttu-id="72f4e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-224">System-Flags</span></span>           | <span data-ttu-id="72f4e-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72f4e-225">0x00000010</span></span>                               |
| <span data-ttu-id="72f4e-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72f4e-226">Classes used in</span></span>        | [<span data-ttu-id="72f4e-227">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="72f4e-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72f4e-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72f4e-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72f4e-229">進入</span><span class="sxs-lookup"><span data-stu-id="72f4e-229">Entry</span></span> | <span data-ttu-id="72f4e-230">值</span><span class="sxs-lookup"><span data-stu-id="72f4e-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="72f4e-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72f4e-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72f4e-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="72f4e-233">System-Only</span></span>            | <span data-ttu-id="72f4e-234">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-234">False</span></span>                                    |
| <span data-ttu-id="72f4e-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72f4e-235">Is-Single-Valued</span></span>       | <span data-ttu-id="72f4e-236">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-236">True</span></span>                                     |
| <span data-ttu-id="72f4e-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72f4e-237">Is Indexed</span></span>             | <span data-ttu-id="72f4e-238">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-238">True</span></span>                                     |
| <span data-ttu-id="72f4e-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72f4e-239">In Global Catalog</span></span>      | <span data-ttu-id="72f4e-240">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-240">False</span></span>                                    |
| <span data-ttu-id="72f4e-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72f4e-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="72f4e-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72f4e-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="72f4e-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72f4e-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72f4e-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-245">Search-Flags</span></span>           | <span data-ttu-id="72f4e-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72f4e-246">0x00000001</span></span>                               |
| <span data-ttu-id="72f4e-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-247">System-Flags</span></span>           | <span data-ttu-id="72f4e-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72f4e-248">0x00000010</span></span>                               |
| <span data-ttu-id="72f4e-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72f4e-249">Classes used in</span></span>        | [<span data-ttu-id="72f4e-250">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="72f4e-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72f4e-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72f4e-251">Windows Server 2012</span></span>



| <span data-ttu-id="72f4e-252">進入</span><span class="sxs-lookup"><span data-stu-id="72f4e-252">Entry</span></span> | <span data-ttu-id="72f4e-253">值</span><span class="sxs-lookup"><span data-stu-id="72f4e-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="72f4e-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72f4e-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72f4e-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="72f4e-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="72f4e-256">System-Only</span></span>            | <span data-ttu-id="72f4e-257">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-257">False</span></span>                                    |
| <span data-ttu-id="72f4e-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72f4e-258">Is-Single-Valued</span></span>       | <span data-ttu-id="72f4e-259">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-259">True</span></span>                                     |
| <span data-ttu-id="72f4e-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72f4e-260">Is Indexed</span></span>             | <span data-ttu-id="72f4e-261">對</span><span class="sxs-lookup"><span data-stu-id="72f4e-261">True</span></span>                                     |
| <span data-ttu-id="72f4e-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72f4e-262">In Global Catalog</span></span>      | <span data-ttu-id="72f4e-263">否</span><span class="sxs-lookup"><span data-stu-id="72f4e-263">False</span></span>                                    |
| <span data-ttu-id="72f4e-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72f4e-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="72f4e-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72f4e-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="72f4e-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72f4e-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72f4e-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="72f4e-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-268">Search-Flags</span></span>           | <span data-ttu-id="72f4e-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72f4e-269">0x00000001</span></span>                               |
| <span data-ttu-id="72f4e-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72f4e-270">System-Flags</span></span>           | <span data-ttu-id="72f4e-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72f4e-271">0x00000010</span></span>                               |
| <span data-ttu-id="72f4e-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72f4e-272">Classes used in</span></span>        | [<span data-ttu-id="72f4e-273">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="72f4e-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





