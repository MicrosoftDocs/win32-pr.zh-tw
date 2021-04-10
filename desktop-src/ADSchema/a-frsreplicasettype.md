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
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="8daa8-105">FRS-Replica-Set 類型屬性</span><span class="sxs-lookup"><span data-stu-id="8daa8-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="8daa8-106">這是一段程式碼，指出這是否為 sysvol 複本集、DFS 複本集或其他複本集。</span><span class="sxs-lookup"><span data-stu-id="8daa8-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="8daa8-107">進入</span><span class="sxs-lookup"><span data-stu-id="8daa8-107">Entry</span></span> | <span data-ttu-id="8daa8-108">值</span><span class="sxs-lookup"><span data-stu-id="8daa8-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8daa8-109">CN</span><span class="sxs-lookup"><span data-stu-id="8daa8-109">CN</span></span>                | <span data-ttu-id="8daa8-110">FRS-複本集類型</span><span class="sxs-lookup"><span data-stu-id="8daa8-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="8daa8-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8daa8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8daa8-112">fRSReplicaSetType</span><span class="sxs-lookup"><span data-stu-id="8daa8-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="8daa8-113">大小</span><span class="sxs-lookup"><span data-stu-id="8daa8-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8daa8-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8daa8-114">Update Privilege</span></span>  | <span data-ttu-id="8daa8-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="8daa8-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="8daa8-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8daa8-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8daa8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8daa8-117">Attribute-Id</span></span>      | <span data-ttu-id="8daa8-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="8daa8-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="8daa8-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8daa8-119">System-Id-Guid</span></span>    | <span data-ttu-id="8daa8-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8daa8-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="8daa8-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8daa8-121">Syntax</span></span>            | [<span data-ttu-id="8daa8-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="8daa8-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8daa8-123">實作</span><span class="sxs-lookup"><span data-stu-id="8daa8-123">Implementations</span></span>

-   [<span data-ttu-id="8daa8-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8daa8-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8daa8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8daa8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8daa8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8daa8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8daa8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8daa8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8daa8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8daa8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8daa8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8daa8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8daa8-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8daa8-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8daa8-131">進入</span><span class="sxs-lookup"><span data-stu-id="8daa8-131">Entry</span></span> | <span data-ttu-id="8daa8-132">值</span><span class="sxs-lookup"><span data-stu-id="8daa8-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8daa8-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8daa8-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8daa8-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8daa8-135">System-Only</span></span>            | <span data-ttu-id="8daa8-136">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-136">False</span></span>                                                     |
| <span data-ttu-id="8daa8-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8daa8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8daa8-138">對</span><span class="sxs-lookup"><span data-stu-id="8daa8-138">True</span></span>                                                      |
| <span data-ttu-id="8daa8-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8daa8-139">Is Indexed</span></span>             | <span data-ttu-id="8daa8-140">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-140">False</span></span>                                                     |
| <span data-ttu-id="8daa8-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8daa8-141">In Global Catalog</span></span>      | <span data-ttu-id="8daa8-142">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-142">False</span></span>                                                     |
| <span data-ttu-id="8daa8-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8daa8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8daa8-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8daa8-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8daa8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8daa8-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8daa8-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-147">Search-Flags</span></span>           | <span data-ttu-id="8daa8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8daa8-148">0x00000000</span></span>                                                |
| <span data-ttu-id="8daa8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-149">System-Flags</span></span>           | <span data-ttu-id="8daa8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8daa8-150">0x00000010</span></span>                                                |
| <span data-ttu-id="8daa8-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8daa8-151">Classes used in</span></span>        | [<span data-ttu-id="8daa8-152">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="8daa8-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8daa8-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8daa8-153">Windows Server 2003</span></span>



| <span data-ttu-id="8daa8-154">進入</span><span class="sxs-lookup"><span data-stu-id="8daa8-154">Entry</span></span> | <span data-ttu-id="8daa8-155">值</span><span class="sxs-lookup"><span data-stu-id="8daa8-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8daa8-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8daa8-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8daa8-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8daa8-158">System-Only</span></span>            | <span data-ttu-id="8daa8-159">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-159">False</span></span>                                                     |
| <span data-ttu-id="8daa8-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8daa8-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8daa8-161">對</span><span class="sxs-lookup"><span data-stu-id="8daa8-161">True</span></span>                                                      |
| <span data-ttu-id="8daa8-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8daa8-162">Is Indexed</span></span>             | <span data-ttu-id="8daa8-163">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-163">False</span></span>                                                     |
| <span data-ttu-id="8daa8-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8daa8-164">In Global Catalog</span></span>      | <span data-ttu-id="8daa8-165">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-165">False</span></span>                                                     |
| <span data-ttu-id="8daa8-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8daa8-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8daa8-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8daa8-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8daa8-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8daa8-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8daa8-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-170">Search-Flags</span></span>           | <span data-ttu-id="8daa8-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8daa8-171">0x00000000</span></span>                                                |
| <span data-ttu-id="8daa8-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-172">System-Flags</span></span>           | <span data-ttu-id="8daa8-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8daa8-173">0x00000010</span></span>                                                |
| <span data-ttu-id="8daa8-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8daa8-174">Classes used in</span></span>        | [<span data-ttu-id="8daa8-175">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="8daa8-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8daa8-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8daa8-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8daa8-177">進入</span><span class="sxs-lookup"><span data-stu-id="8daa8-177">Entry</span></span> | <span data-ttu-id="8daa8-178">值</span><span class="sxs-lookup"><span data-stu-id="8daa8-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8daa8-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8daa8-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8daa8-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8daa8-181">System-Only</span></span>            | <span data-ttu-id="8daa8-182">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-182">False</span></span>                                                     |
| <span data-ttu-id="8daa8-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8daa8-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8daa8-184">對</span><span class="sxs-lookup"><span data-stu-id="8daa8-184">True</span></span>                                                      |
| <span data-ttu-id="8daa8-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8daa8-185">Is Indexed</span></span>             | <span data-ttu-id="8daa8-186">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-186">False</span></span>                                                     |
| <span data-ttu-id="8daa8-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8daa8-187">In Global Catalog</span></span>      | <span data-ttu-id="8daa8-188">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-188">False</span></span>                                                     |
| <span data-ttu-id="8daa8-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8daa8-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8daa8-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8daa8-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8daa8-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8daa8-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8daa8-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-193">Search-Flags</span></span>           | <span data-ttu-id="8daa8-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8daa8-194">0x00000000</span></span>                                                |
| <span data-ttu-id="8daa8-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-195">System-Flags</span></span>           | <span data-ttu-id="8daa8-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8daa8-196">0x00000010</span></span>                                                |
| <span data-ttu-id="8daa8-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8daa8-197">Classes used in</span></span>        | [<span data-ttu-id="8daa8-198">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="8daa8-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8daa8-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8daa8-199">Windows Server 2008</span></span>



| <span data-ttu-id="8daa8-200">進入</span><span class="sxs-lookup"><span data-stu-id="8daa8-200">Entry</span></span> | <span data-ttu-id="8daa8-201">值</span><span class="sxs-lookup"><span data-stu-id="8daa8-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8daa8-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8daa8-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8daa8-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8daa8-204">System-Only</span></span>            | <span data-ttu-id="8daa8-205">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-205">False</span></span>                                                     |
| <span data-ttu-id="8daa8-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8daa8-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8daa8-207">對</span><span class="sxs-lookup"><span data-stu-id="8daa8-207">True</span></span>                                                      |
| <span data-ttu-id="8daa8-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8daa8-208">Is Indexed</span></span>             | <span data-ttu-id="8daa8-209">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-209">False</span></span>                                                     |
| <span data-ttu-id="8daa8-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8daa8-210">In Global Catalog</span></span>      | <span data-ttu-id="8daa8-211">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-211">False</span></span>                                                     |
| <span data-ttu-id="8daa8-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8daa8-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8daa8-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8daa8-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8daa8-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8daa8-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8daa8-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-216">Search-Flags</span></span>           | <span data-ttu-id="8daa8-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8daa8-217">0x00000000</span></span>                                                |
| <span data-ttu-id="8daa8-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-218">System-Flags</span></span>           | <span data-ttu-id="8daa8-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8daa8-219">0x00000010</span></span>                                                |
| <span data-ttu-id="8daa8-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8daa8-220">Classes used in</span></span>        | [<span data-ttu-id="8daa8-221">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="8daa8-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8daa8-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8daa8-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8daa8-223">進入</span><span class="sxs-lookup"><span data-stu-id="8daa8-223">Entry</span></span> | <span data-ttu-id="8daa8-224">值</span><span class="sxs-lookup"><span data-stu-id="8daa8-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8daa8-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8daa8-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8daa8-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8daa8-227">System-Only</span></span>            | <span data-ttu-id="8daa8-228">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-228">False</span></span>                                                     |
| <span data-ttu-id="8daa8-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8daa8-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8daa8-230">對</span><span class="sxs-lookup"><span data-stu-id="8daa8-230">True</span></span>                                                      |
| <span data-ttu-id="8daa8-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8daa8-231">Is Indexed</span></span>             | <span data-ttu-id="8daa8-232">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-232">False</span></span>                                                     |
| <span data-ttu-id="8daa8-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8daa8-233">In Global Catalog</span></span>      | <span data-ttu-id="8daa8-234">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-234">False</span></span>                                                     |
| <span data-ttu-id="8daa8-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8daa8-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8daa8-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8daa8-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8daa8-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8daa8-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8daa8-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-239">Search-Flags</span></span>           | <span data-ttu-id="8daa8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8daa8-240">0x00000000</span></span>                                                |
| <span data-ttu-id="8daa8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-241">System-Flags</span></span>           | <span data-ttu-id="8daa8-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8daa8-242">0x00000010</span></span>                                                |
| <span data-ttu-id="8daa8-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8daa8-243">Classes used in</span></span>        | [<span data-ttu-id="8daa8-244">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="8daa8-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8daa8-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8daa8-245">Windows Server 2012</span></span>



| <span data-ttu-id="8daa8-246">進入</span><span class="sxs-lookup"><span data-stu-id="8daa8-246">Entry</span></span> | <span data-ttu-id="8daa8-247">值</span><span class="sxs-lookup"><span data-stu-id="8daa8-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8daa8-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8daa8-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8daa8-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8daa8-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8daa8-250">System-Only</span></span>            | <span data-ttu-id="8daa8-251">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-251">False</span></span>                                                     |
| <span data-ttu-id="8daa8-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8daa8-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8daa8-253">對</span><span class="sxs-lookup"><span data-stu-id="8daa8-253">True</span></span>                                                      |
| <span data-ttu-id="8daa8-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8daa8-254">Is Indexed</span></span>             | <span data-ttu-id="8daa8-255">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-255">False</span></span>                                                     |
| <span data-ttu-id="8daa8-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8daa8-256">In Global Catalog</span></span>      | <span data-ttu-id="8daa8-257">否</span><span class="sxs-lookup"><span data-stu-id="8daa8-257">False</span></span>                                                     |
| <span data-ttu-id="8daa8-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8daa8-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8daa8-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8daa8-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8daa8-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8daa8-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8daa8-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8daa8-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-262">Search-Flags</span></span>           | <span data-ttu-id="8daa8-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8daa8-263">0x00000000</span></span>                                                |
| <span data-ttu-id="8daa8-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8daa8-264">System-Flags</span></span>           | <span data-ttu-id="8daa8-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8daa8-265">0x00000010</span></span>                                                |
| <span data-ttu-id="8daa8-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8daa8-266">Classes used in</span></span>        | [<span data-ttu-id="8daa8-267">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="8daa8-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





