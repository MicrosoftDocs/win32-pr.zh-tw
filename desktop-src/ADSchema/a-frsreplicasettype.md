---
title: FRS-Replica-Set 類型屬性
description: 這是一段程式碼，指出這是否為 sysvol 複本集、DFS 複本集或其他複本集。
ms.assetid: 687a854f-ffa1-41f4-a515-5224759696ab
ms.tgt_platform: multiple
keywords:
- FRS-複本集-類型屬性 AD 架構
- fRSReplicaSetType 屬性 AD 架構
topic_type:
- apiref
api_name:
- FRS-Replica-Set-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18046c9b4edb794687d275af52e35416419c7e2d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844660"
---
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="c9e26-105">FRS-Replica-Set 類型屬性</span><span class="sxs-lookup"><span data-stu-id="c9e26-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="c9e26-106">這是一段程式碼，指出這是否為 sysvol 複本集、DFS 複本集或其他複本集。</span><span class="sxs-lookup"><span data-stu-id="c9e26-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="c9e26-107">進入</span><span class="sxs-lookup"><span data-stu-id="c9e26-107">Entry</span></span> | <span data-ttu-id="c9e26-108">值</span><span class="sxs-lookup"><span data-stu-id="c9e26-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c9e26-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9e26-109">CN</span></span>                | <span data-ttu-id="c9e26-110">FRS-複本集類型</span><span class="sxs-lookup"><span data-stu-id="c9e26-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="c9e26-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c9e26-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9e26-112">fRSReplicaSetType</span><span class="sxs-lookup"><span data-stu-id="c9e26-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="c9e26-113">大小</span><span class="sxs-lookup"><span data-stu-id="c9e26-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="c9e26-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c9e26-114">Update Privilege</span></span>  | <span data-ttu-id="c9e26-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="c9e26-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="c9e26-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c9e26-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c9e26-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9e26-117">Attribute-Id</span></span>      | <span data-ttu-id="c9e26-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="c9e26-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="c9e26-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c9e26-119">System-Id-Guid</span></span>    | <span data-ttu-id="c9e26-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c9e26-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="c9e26-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9e26-121">Syntax</span></span>            | [<span data-ttu-id="c9e26-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="c9e26-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c9e26-123">實作</span><span class="sxs-lookup"><span data-stu-id="c9e26-123">Implementations</span></span>

-   [<span data-ttu-id="c9e26-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9e26-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9e26-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9e26-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9e26-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9e26-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9e26-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9e26-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9e26-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9e26-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9e26-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9e26-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9e26-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9e26-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c9e26-131">進入</span><span class="sxs-lookup"><span data-stu-id="c9e26-131">Entry</span></span> | <span data-ttu-id="c9e26-132">值</span><span class="sxs-lookup"><span data-stu-id="c9e26-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9e26-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9e26-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9e26-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9e26-135">System-Only</span></span>            | <span data-ttu-id="c9e26-136">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-136">False</span></span>                                                     |
| <span data-ttu-id="c9e26-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9e26-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c9e26-138">對</span><span class="sxs-lookup"><span data-stu-id="c9e26-138">True</span></span>                                                      |
| <span data-ttu-id="c9e26-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9e26-139">Is Indexed</span></span>             | <span data-ttu-id="c9e26-140">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-140">False</span></span>                                                     |
| <span data-ttu-id="c9e26-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9e26-141">In Global Catalog</span></span>      | <span data-ttu-id="c9e26-142">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-142">False</span></span>                                                     |
| <span data-ttu-id="c9e26-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9e26-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9e26-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9e26-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9e26-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9e26-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9e26-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-147">Search-Flags</span></span>           | <span data-ttu-id="c9e26-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9e26-148">0x00000000</span></span>                                                |
| <span data-ttu-id="c9e26-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-149">System-Flags</span></span>           | <span data-ttu-id="c9e26-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9e26-150">0x00000010</span></span>                                                |
| <span data-ttu-id="c9e26-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9e26-151">Classes used in</span></span>        | [<span data-ttu-id="c9e26-152">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9e26-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9e26-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9e26-153">Windows Server 2003</span></span>



| <span data-ttu-id="c9e26-154">進入</span><span class="sxs-lookup"><span data-stu-id="c9e26-154">Entry</span></span> | <span data-ttu-id="c9e26-155">值</span><span class="sxs-lookup"><span data-stu-id="c9e26-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9e26-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9e26-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9e26-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9e26-158">System-Only</span></span>            | <span data-ttu-id="c9e26-159">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-159">False</span></span>                                                     |
| <span data-ttu-id="c9e26-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9e26-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c9e26-161">對</span><span class="sxs-lookup"><span data-stu-id="c9e26-161">True</span></span>                                                      |
| <span data-ttu-id="c9e26-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9e26-162">Is Indexed</span></span>             | <span data-ttu-id="c9e26-163">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-163">False</span></span>                                                     |
| <span data-ttu-id="c9e26-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9e26-164">In Global Catalog</span></span>      | <span data-ttu-id="c9e26-165">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-165">False</span></span>                                                     |
| <span data-ttu-id="c9e26-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9e26-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9e26-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9e26-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9e26-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9e26-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9e26-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-170">Search-Flags</span></span>           | <span data-ttu-id="c9e26-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9e26-171">0x00000000</span></span>                                                |
| <span data-ttu-id="c9e26-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-172">System-Flags</span></span>           | <span data-ttu-id="c9e26-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9e26-173">0x00000010</span></span>                                                |
| <span data-ttu-id="c9e26-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9e26-174">Classes used in</span></span>        | [<span data-ttu-id="c9e26-175">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9e26-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9e26-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9e26-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9e26-177">進入</span><span class="sxs-lookup"><span data-stu-id="c9e26-177">Entry</span></span> | <span data-ttu-id="c9e26-178">值</span><span class="sxs-lookup"><span data-stu-id="c9e26-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9e26-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9e26-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9e26-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9e26-181">System-Only</span></span>            | <span data-ttu-id="c9e26-182">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-182">False</span></span>                                                     |
| <span data-ttu-id="c9e26-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9e26-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c9e26-184">對</span><span class="sxs-lookup"><span data-stu-id="c9e26-184">True</span></span>                                                      |
| <span data-ttu-id="c9e26-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9e26-185">Is Indexed</span></span>             | <span data-ttu-id="c9e26-186">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-186">False</span></span>                                                     |
| <span data-ttu-id="c9e26-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9e26-187">In Global Catalog</span></span>      | <span data-ttu-id="c9e26-188">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-188">False</span></span>                                                     |
| <span data-ttu-id="c9e26-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9e26-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9e26-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9e26-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9e26-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9e26-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9e26-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-193">Search-Flags</span></span>           | <span data-ttu-id="c9e26-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9e26-194">0x00000000</span></span>                                                |
| <span data-ttu-id="c9e26-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-195">System-Flags</span></span>           | <span data-ttu-id="c9e26-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9e26-196">0x00000010</span></span>                                                |
| <span data-ttu-id="c9e26-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9e26-197">Classes used in</span></span>        | [<span data-ttu-id="c9e26-198">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9e26-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9e26-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9e26-199">Windows Server 2008</span></span>



| <span data-ttu-id="c9e26-200">進入</span><span class="sxs-lookup"><span data-stu-id="c9e26-200">Entry</span></span> | <span data-ttu-id="c9e26-201">值</span><span class="sxs-lookup"><span data-stu-id="c9e26-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9e26-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9e26-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9e26-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9e26-204">System-Only</span></span>            | <span data-ttu-id="c9e26-205">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-205">False</span></span>                                                     |
| <span data-ttu-id="c9e26-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9e26-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c9e26-207">對</span><span class="sxs-lookup"><span data-stu-id="c9e26-207">True</span></span>                                                      |
| <span data-ttu-id="c9e26-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9e26-208">Is Indexed</span></span>             | <span data-ttu-id="c9e26-209">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-209">False</span></span>                                                     |
| <span data-ttu-id="c9e26-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9e26-210">In Global Catalog</span></span>      | <span data-ttu-id="c9e26-211">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-211">False</span></span>                                                     |
| <span data-ttu-id="c9e26-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9e26-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9e26-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9e26-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9e26-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9e26-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9e26-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-216">Search-Flags</span></span>           | <span data-ttu-id="c9e26-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9e26-217">0x00000000</span></span>                                                |
| <span data-ttu-id="c9e26-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-218">System-Flags</span></span>           | <span data-ttu-id="c9e26-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9e26-219">0x00000010</span></span>                                                |
| <span data-ttu-id="c9e26-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9e26-220">Classes used in</span></span>        | [<span data-ttu-id="c9e26-221">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9e26-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9e26-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9e26-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9e26-223">進入</span><span class="sxs-lookup"><span data-stu-id="c9e26-223">Entry</span></span> | <span data-ttu-id="c9e26-224">值</span><span class="sxs-lookup"><span data-stu-id="c9e26-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9e26-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9e26-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9e26-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9e26-227">System-Only</span></span>            | <span data-ttu-id="c9e26-228">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-228">False</span></span>                                                     |
| <span data-ttu-id="c9e26-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9e26-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c9e26-230">對</span><span class="sxs-lookup"><span data-stu-id="c9e26-230">True</span></span>                                                      |
| <span data-ttu-id="c9e26-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9e26-231">Is Indexed</span></span>             | <span data-ttu-id="c9e26-232">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-232">False</span></span>                                                     |
| <span data-ttu-id="c9e26-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9e26-233">In Global Catalog</span></span>      | <span data-ttu-id="c9e26-234">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-234">False</span></span>                                                     |
| <span data-ttu-id="c9e26-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9e26-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9e26-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9e26-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9e26-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9e26-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9e26-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-239">Search-Flags</span></span>           | <span data-ttu-id="c9e26-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9e26-240">0x00000000</span></span>                                                |
| <span data-ttu-id="c9e26-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-241">System-Flags</span></span>           | <span data-ttu-id="c9e26-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9e26-242">0x00000010</span></span>                                                |
| <span data-ttu-id="c9e26-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9e26-243">Classes used in</span></span>        | [<span data-ttu-id="c9e26-244">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9e26-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9e26-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9e26-245">Windows Server 2012</span></span>



| <span data-ttu-id="c9e26-246">進入</span><span class="sxs-lookup"><span data-stu-id="c9e26-246">Entry</span></span> | <span data-ttu-id="c9e26-247">值</span><span class="sxs-lookup"><span data-stu-id="c9e26-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c9e26-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9e26-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9e26-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c9e26-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9e26-250">System-Only</span></span>            | <span data-ttu-id="c9e26-251">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-251">False</span></span>                                                     |
| <span data-ttu-id="c9e26-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9e26-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c9e26-253">對</span><span class="sxs-lookup"><span data-stu-id="c9e26-253">True</span></span>                                                      |
| <span data-ttu-id="c9e26-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9e26-254">Is Indexed</span></span>             | <span data-ttu-id="c9e26-255">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-255">False</span></span>                                                     |
| <span data-ttu-id="c9e26-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9e26-256">In Global Catalog</span></span>      | <span data-ttu-id="c9e26-257">否</span><span class="sxs-lookup"><span data-stu-id="c9e26-257">False</span></span>                                                     |
| <span data-ttu-id="c9e26-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9e26-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9e26-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9e26-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c9e26-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9e26-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9e26-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c9e26-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-262">Search-Flags</span></span>           | <span data-ttu-id="c9e26-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9e26-263">0x00000000</span></span>                                                |
| <span data-ttu-id="c9e26-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9e26-264">System-Flags</span></span>           | <span data-ttu-id="c9e26-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9e26-265">0x00000010</span></span>                                                |
| <span data-ttu-id="c9e26-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9e26-266">Classes used in</span></span>        | [<span data-ttu-id="c9e26-267">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c9e26-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





