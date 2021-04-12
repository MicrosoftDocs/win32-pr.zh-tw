---
title: ReplicationEpoch 屬性
description: 這是用來保存所有 Dc 正在複寫的 epoch。 Epoch 是網域具有特定名稱的時間週期。 新的 epoch 會在定義功能變數名稱稱變更時啟動。
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- ReplicationEpoch 屬性 AD 架構
- ReplicationEpoch 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509614"
---
# <a name="ms-ds-replicationepoch-attribute"></a><span data-ttu-id="55d2a-107">ReplicationEpoch 屬性</span><span class="sxs-lookup"><span data-stu-id="55d2a-107">ms-DS-ReplicationEpoch attribute</span></span>

<span data-ttu-id="55d2a-108">這是用來保存所有 Dc 正在複寫的 epoch。</span><span class="sxs-lookup"><span data-stu-id="55d2a-108">This is used to hold the epoch under which all the DCs are replicating.</span></span> <span data-ttu-id="55d2a-109">Epoch 是網域具有特定名稱的時間週期。</span><span class="sxs-lookup"><span data-stu-id="55d2a-109">An epoch is the period of time in which a domain has a specific name.</span></span> <span data-ttu-id="55d2a-110">新的 epoch 會在定義功能變數名稱稱變更時啟動。</span><span class="sxs-lookup"><span data-stu-id="55d2a-110">A new epoch starts when a domain name change occurs.</span></span>



| <span data-ttu-id="55d2a-111">進入</span><span class="sxs-lookup"><span data-stu-id="55d2a-111">Entry</span></span> | <span data-ttu-id="55d2a-112">值</span><span class="sxs-lookup"><span data-stu-id="55d2a-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="55d2a-113">CN</span><span class="sxs-lookup"><span data-stu-id="55d2a-113">CN</span></span>                | <span data-ttu-id="55d2a-114">ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="55d2a-114">ms-DS-ReplicationEpoch</span></span>               |
| <span data-ttu-id="55d2a-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="55d2a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="55d2a-116">ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="55d2a-116">msDS-ReplicationEpoch</span></span>                |
| <span data-ttu-id="55d2a-117">大小</span><span class="sxs-lookup"><span data-stu-id="55d2a-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="55d2a-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="55d2a-118">Update Privilege</span></span>  | <span data-ttu-id="55d2a-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="55d2a-119">This value is set by the system.</span></span>     |
| <span data-ttu-id="55d2a-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="55d2a-120">Update Frequency</span></span>  | <span data-ttu-id="55d2a-121">只有在網域重建時。</span><span class="sxs-lookup"><span data-stu-id="55d2a-121">Only during domain restructure.</span></span>      |
| <span data-ttu-id="55d2a-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="55d2a-122">Attribute-Id</span></span>      | <span data-ttu-id="55d2a-123">1.2.840.113556.1.4.1720</span><span class="sxs-lookup"><span data-stu-id="55d2a-123">1.2.840.113556.1.4.1720</span></span>              |
| <span data-ttu-id="55d2a-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="55d2a-124">System-Id-Guid</span></span>    | <span data-ttu-id="55d2a-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span><span class="sxs-lookup"><span data-stu-id="55d2a-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span></span> |
| <span data-ttu-id="55d2a-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="55d2a-126">Syntax</span></span>            | [<span data-ttu-id="55d2a-127">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="55d2a-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="55d2a-128">實作</span><span class="sxs-lookup"><span data-stu-id="55d2a-128">Implementations</span></span>

-   [<span data-ttu-id="55d2a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="55d2a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="55d2a-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="55d2a-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="55d2a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="55d2a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="55d2a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="55d2a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="55d2a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="55d2a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="55d2a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="55d2a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="55d2a-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55d2a-135">Windows Server 2003</span></span>



| <span data-ttu-id="55d2a-136">進入</span><span class="sxs-lookup"><span data-stu-id="55d2a-136">Entry</span></span> | <span data-ttu-id="55d2a-137">值</span><span class="sxs-lookup"><span data-stu-id="55d2a-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="55d2a-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="55d2a-138">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d2a-139">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d2a-140">System-Only</span></span>            | <span data-ttu-id="55d2a-141">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-141">False</span></span>                                    |
| <span data-ttu-id="55d2a-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="55d2a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="55d2a-143">對</span><span class="sxs-lookup"><span data-stu-id="55d2a-143">True</span></span>                                     |
| <span data-ttu-id="55d2a-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="55d2a-144">Is Indexed</span></span>             | <span data-ttu-id="55d2a-145">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-145">False</span></span>                                    |
| <span data-ttu-id="55d2a-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="55d2a-146">In Global Catalog</span></span>      | <span data-ttu-id="55d2a-147">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-147">False</span></span>                                    |
| <span data-ttu-id="55d2a-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="55d2a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d2a-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="55d2a-149">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="55d2a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d2a-150">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d2a-151">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-152">Search-Flags</span></span>           | <span data-ttu-id="55d2a-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d2a-153">0x00000000</span></span>                               |
| <span data-ttu-id="55d2a-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-154">System-Flags</span></span>           | <span data-ttu-id="55d2a-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="55d2a-155">0x00000011</span></span>                               |
| <span data-ttu-id="55d2a-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="55d2a-156">Classes used in</span></span>        | [<span data-ttu-id="55d2a-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="55d2a-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="55d2a-158">亞當</span><span class="sxs-lookup"><span data-stu-id="55d2a-158">ADAM</span></span>



| <span data-ttu-id="55d2a-159">進入</span><span class="sxs-lookup"><span data-stu-id="55d2a-159">Entry</span></span> | <span data-ttu-id="55d2a-160">值</span><span class="sxs-lookup"><span data-stu-id="55d2a-160">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="55d2a-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="55d2a-161">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d2a-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d2a-163">System-Only</span></span>            | <span data-ttu-id="55d2a-164">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-164">False</span></span>                                    |
| <span data-ttu-id="55d2a-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="55d2a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="55d2a-166">對</span><span class="sxs-lookup"><span data-stu-id="55d2a-166">True</span></span>                                     |
| <span data-ttu-id="55d2a-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="55d2a-167">Is Indexed</span></span>             | <span data-ttu-id="55d2a-168">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-168">False</span></span>                                    |
| <span data-ttu-id="55d2a-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="55d2a-169">In Global Catalog</span></span>      | <span data-ttu-id="55d2a-170">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-170">False</span></span>                                    |
| <span data-ttu-id="55d2a-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="55d2a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d2a-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="55d2a-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="55d2a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d2a-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d2a-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-175">Search-Flags</span></span>           | <span data-ttu-id="55d2a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d2a-176">0x00000000</span></span>                               |
| <span data-ttu-id="55d2a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-177">System-Flags</span></span>           | <span data-ttu-id="55d2a-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="55d2a-178">0x00000011</span></span>                               |
| <span data-ttu-id="55d2a-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="55d2a-179">Classes used in</span></span>        | [<span data-ttu-id="55d2a-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="55d2a-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="55d2a-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="55d2a-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="55d2a-182">進入</span><span class="sxs-lookup"><span data-stu-id="55d2a-182">Entry</span></span> | <span data-ttu-id="55d2a-183">值</span><span class="sxs-lookup"><span data-stu-id="55d2a-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="55d2a-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="55d2a-184">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d2a-185">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d2a-186">System-Only</span></span>            | <span data-ttu-id="55d2a-187">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-187">False</span></span>                                    |
| <span data-ttu-id="55d2a-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="55d2a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="55d2a-189">對</span><span class="sxs-lookup"><span data-stu-id="55d2a-189">True</span></span>                                     |
| <span data-ttu-id="55d2a-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="55d2a-190">Is Indexed</span></span>             | <span data-ttu-id="55d2a-191">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-191">False</span></span>                                    |
| <span data-ttu-id="55d2a-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="55d2a-192">In Global Catalog</span></span>      | <span data-ttu-id="55d2a-193">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-193">False</span></span>                                    |
| <span data-ttu-id="55d2a-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="55d2a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d2a-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="55d2a-195">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="55d2a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d2a-196">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d2a-197">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-198">Search-Flags</span></span>           | <span data-ttu-id="55d2a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d2a-199">0x00000000</span></span>                               |
| <span data-ttu-id="55d2a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-200">System-Flags</span></span>           | <span data-ttu-id="55d2a-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="55d2a-201">0x00000011</span></span>                               |
| <span data-ttu-id="55d2a-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="55d2a-202">Classes used in</span></span>        | [<span data-ttu-id="55d2a-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="55d2a-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="55d2a-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55d2a-204">Windows Server 2008</span></span>



| <span data-ttu-id="55d2a-205">進入</span><span class="sxs-lookup"><span data-stu-id="55d2a-205">Entry</span></span> | <span data-ttu-id="55d2a-206">值</span><span class="sxs-lookup"><span data-stu-id="55d2a-206">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="55d2a-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="55d2a-207">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d2a-208">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d2a-209">System-Only</span></span>            | <span data-ttu-id="55d2a-210">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-210">False</span></span>                                    |
| <span data-ttu-id="55d2a-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="55d2a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="55d2a-212">對</span><span class="sxs-lookup"><span data-stu-id="55d2a-212">True</span></span>                                     |
| <span data-ttu-id="55d2a-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="55d2a-213">Is Indexed</span></span>             | <span data-ttu-id="55d2a-214">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-214">False</span></span>                                    |
| <span data-ttu-id="55d2a-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="55d2a-215">In Global Catalog</span></span>      | <span data-ttu-id="55d2a-216">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-216">False</span></span>                                    |
| <span data-ttu-id="55d2a-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="55d2a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d2a-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="55d2a-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="55d2a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d2a-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d2a-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-221">Search-Flags</span></span>           | <span data-ttu-id="55d2a-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d2a-222">0x00000000</span></span>                               |
| <span data-ttu-id="55d2a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-223">System-Flags</span></span>           | <span data-ttu-id="55d2a-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="55d2a-224">0x00000011</span></span>                               |
| <span data-ttu-id="55d2a-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="55d2a-225">Classes used in</span></span>        | [<span data-ttu-id="55d2a-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="55d2a-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="55d2a-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="55d2a-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="55d2a-228">進入</span><span class="sxs-lookup"><span data-stu-id="55d2a-228">Entry</span></span> | <span data-ttu-id="55d2a-229">值</span><span class="sxs-lookup"><span data-stu-id="55d2a-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="55d2a-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="55d2a-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d2a-231">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d2a-232">System-Only</span></span>            | <span data-ttu-id="55d2a-233">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-233">False</span></span>                                    |
| <span data-ttu-id="55d2a-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="55d2a-234">Is-Single-Valued</span></span>       | <span data-ttu-id="55d2a-235">對</span><span class="sxs-lookup"><span data-stu-id="55d2a-235">True</span></span>                                     |
| <span data-ttu-id="55d2a-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="55d2a-236">Is Indexed</span></span>             | <span data-ttu-id="55d2a-237">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-237">False</span></span>                                    |
| <span data-ttu-id="55d2a-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="55d2a-238">In Global Catalog</span></span>      | <span data-ttu-id="55d2a-239">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-239">False</span></span>                                    |
| <span data-ttu-id="55d2a-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="55d2a-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d2a-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="55d2a-241">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="55d2a-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d2a-242">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d2a-243">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-244">Search-Flags</span></span>           | <span data-ttu-id="55d2a-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d2a-245">0x00000000</span></span>                               |
| <span data-ttu-id="55d2a-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-246">System-Flags</span></span>           | <span data-ttu-id="55d2a-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="55d2a-247">0x00000011</span></span>                               |
| <span data-ttu-id="55d2a-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="55d2a-248">Classes used in</span></span>        | [<span data-ttu-id="55d2a-249">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="55d2a-249">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="55d2a-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55d2a-250">Windows Server 2012</span></span>



| <span data-ttu-id="55d2a-251">進入</span><span class="sxs-lookup"><span data-stu-id="55d2a-251">Entry</span></span> | <span data-ttu-id="55d2a-252">值</span><span class="sxs-lookup"><span data-stu-id="55d2a-252">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="55d2a-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="55d2a-253">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55d2a-254">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="55d2a-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="55d2a-255">System-Only</span></span>            | <span data-ttu-id="55d2a-256">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-256">False</span></span>                                    |
| <span data-ttu-id="55d2a-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="55d2a-257">Is-Single-Valued</span></span>       | <span data-ttu-id="55d2a-258">對</span><span class="sxs-lookup"><span data-stu-id="55d2a-258">True</span></span>                                     |
| <span data-ttu-id="55d2a-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="55d2a-259">Is Indexed</span></span>             | <span data-ttu-id="55d2a-260">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-260">False</span></span>                                    |
| <span data-ttu-id="55d2a-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="55d2a-261">In Global Catalog</span></span>      | <span data-ttu-id="55d2a-262">否</span><span class="sxs-lookup"><span data-stu-id="55d2a-262">False</span></span>                                    |
| <span data-ttu-id="55d2a-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="55d2a-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="55d2a-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="55d2a-264">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="55d2a-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55d2a-265">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55d2a-266">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="55d2a-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-267">Search-Flags</span></span>           | <span data-ttu-id="55d2a-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55d2a-268">0x00000000</span></span>                               |
| <span data-ttu-id="55d2a-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55d2a-269">System-Flags</span></span>           | <span data-ttu-id="55d2a-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="55d2a-270">0x00000011</span></span>                               |
| <span data-ttu-id="55d2a-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="55d2a-271">Classes used in</span></span>        | [<span data-ttu-id="55d2a-272">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="55d2a-272">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





