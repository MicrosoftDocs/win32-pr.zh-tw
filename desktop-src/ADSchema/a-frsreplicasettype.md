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
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="38b4b-105">FRS-Replica-Set 類型屬性</span><span class="sxs-lookup"><span data-stu-id="38b4b-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="38b4b-106">這是一段程式碼，指出這是否為 sysvol 複本集、DFS 複本集或其他複本集。</span><span class="sxs-lookup"><span data-stu-id="38b4b-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="38b4b-107">進入</span><span class="sxs-lookup"><span data-stu-id="38b4b-107">Entry</span></span> | <span data-ttu-id="38b4b-108">值</span><span class="sxs-lookup"><span data-stu-id="38b4b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="38b4b-109">CN</span><span class="sxs-lookup"><span data-stu-id="38b4b-109">CN</span></span>                | <span data-ttu-id="38b4b-110">FRS-複本集類型</span><span class="sxs-lookup"><span data-stu-id="38b4b-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="38b4b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="38b4b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="38b4b-112">fRSReplicaSetType</span><span class="sxs-lookup"><span data-stu-id="38b4b-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="38b4b-113">大小</span><span class="sxs-lookup"><span data-stu-id="38b4b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="38b4b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="38b4b-114">Update Privilege</span></span>  | <span data-ttu-id="38b4b-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="38b4b-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="38b4b-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="38b4b-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="38b4b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38b4b-117">Attribute-Id</span></span>      | <span data-ttu-id="38b4b-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="38b4b-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="38b4b-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="38b4b-119">System-Id-Guid</span></span>    | <span data-ttu-id="38b4b-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="38b4b-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="38b4b-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="38b4b-121">Syntax</span></span>            | [<span data-ttu-id="38b4b-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="38b4b-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="38b4b-123">實作</span><span class="sxs-lookup"><span data-stu-id="38b4b-123">Implementations</span></span>

-   [<span data-ttu-id="38b4b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38b4b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38b4b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38b4b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38b4b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38b4b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38b4b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38b4b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38b4b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38b4b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38b4b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38b4b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38b4b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38b4b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="38b4b-131">進入</span><span class="sxs-lookup"><span data-stu-id="38b4b-131">Entry</span></span> | <span data-ttu-id="38b4b-132">值</span><span class="sxs-lookup"><span data-stu-id="38b4b-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38b4b-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38b4b-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b4b-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b4b-135">System-Only</span></span>            | <span data-ttu-id="38b4b-136">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-136">False</span></span>                                                     |
| <span data-ttu-id="38b4b-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38b4b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="38b4b-138">對</span><span class="sxs-lookup"><span data-stu-id="38b4b-138">True</span></span>                                                      |
| <span data-ttu-id="38b4b-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38b4b-139">Is Indexed</span></span>             | <span data-ttu-id="38b4b-140">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-140">False</span></span>                                                     |
| <span data-ttu-id="38b4b-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38b4b-141">In Global Catalog</span></span>      | <span data-ttu-id="38b4b-142">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-142">False</span></span>                                                     |
| <span data-ttu-id="38b4b-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38b4b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b4b-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38b4b-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38b4b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b4b-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b4b-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-147">Search-Flags</span></span>           | <span data-ttu-id="38b4b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38b4b-148">0x00000000</span></span>                                                |
| <span data-ttu-id="38b4b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-149">System-Flags</span></span>           | <span data-ttu-id="38b4b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b4b-150">0x00000010</span></span>                                                |
| <span data-ttu-id="38b4b-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38b4b-151">Classes used in</span></span>        | [<span data-ttu-id="38b4b-152">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="38b4b-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38b4b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38b4b-153">Windows Server 2003</span></span>



| <span data-ttu-id="38b4b-154">進入</span><span class="sxs-lookup"><span data-stu-id="38b4b-154">Entry</span></span> | <span data-ttu-id="38b4b-155">值</span><span class="sxs-lookup"><span data-stu-id="38b4b-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38b4b-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38b4b-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b4b-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b4b-158">System-Only</span></span>            | <span data-ttu-id="38b4b-159">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-159">False</span></span>                                                     |
| <span data-ttu-id="38b4b-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38b4b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="38b4b-161">對</span><span class="sxs-lookup"><span data-stu-id="38b4b-161">True</span></span>                                                      |
| <span data-ttu-id="38b4b-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38b4b-162">Is Indexed</span></span>             | <span data-ttu-id="38b4b-163">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-163">False</span></span>                                                     |
| <span data-ttu-id="38b4b-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38b4b-164">In Global Catalog</span></span>      | <span data-ttu-id="38b4b-165">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-165">False</span></span>                                                     |
| <span data-ttu-id="38b4b-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38b4b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b4b-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38b4b-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38b4b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b4b-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b4b-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-170">Search-Flags</span></span>           | <span data-ttu-id="38b4b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38b4b-171">0x00000000</span></span>                                                |
| <span data-ttu-id="38b4b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-172">System-Flags</span></span>           | <span data-ttu-id="38b4b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b4b-173">0x00000010</span></span>                                                |
| <span data-ttu-id="38b4b-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38b4b-174">Classes used in</span></span>        | [<span data-ttu-id="38b4b-175">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="38b4b-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38b4b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38b4b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38b4b-177">進入</span><span class="sxs-lookup"><span data-stu-id="38b4b-177">Entry</span></span> | <span data-ttu-id="38b4b-178">值</span><span class="sxs-lookup"><span data-stu-id="38b4b-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38b4b-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38b4b-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b4b-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b4b-181">System-Only</span></span>            | <span data-ttu-id="38b4b-182">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-182">False</span></span>                                                     |
| <span data-ttu-id="38b4b-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38b4b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="38b4b-184">對</span><span class="sxs-lookup"><span data-stu-id="38b4b-184">True</span></span>                                                      |
| <span data-ttu-id="38b4b-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38b4b-185">Is Indexed</span></span>             | <span data-ttu-id="38b4b-186">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-186">False</span></span>                                                     |
| <span data-ttu-id="38b4b-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38b4b-187">In Global Catalog</span></span>      | <span data-ttu-id="38b4b-188">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-188">False</span></span>                                                     |
| <span data-ttu-id="38b4b-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38b4b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b4b-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38b4b-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38b4b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b4b-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b4b-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-193">Search-Flags</span></span>           | <span data-ttu-id="38b4b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38b4b-194">0x00000000</span></span>                                                |
| <span data-ttu-id="38b4b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-195">System-Flags</span></span>           | <span data-ttu-id="38b4b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b4b-196">0x00000010</span></span>                                                |
| <span data-ttu-id="38b4b-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38b4b-197">Classes used in</span></span>        | [<span data-ttu-id="38b4b-198">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="38b4b-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38b4b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38b4b-199">Windows Server 2008</span></span>



| <span data-ttu-id="38b4b-200">進入</span><span class="sxs-lookup"><span data-stu-id="38b4b-200">Entry</span></span> | <span data-ttu-id="38b4b-201">值</span><span class="sxs-lookup"><span data-stu-id="38b4b-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38b4b-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38b4b-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b4b-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b4b-204">System-Only</span></span>            | <span data-ttu-id="38b4b-205">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-205">False</span></span>                                                     |
| <span data-ttu-id="38b4b-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38b4b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="38b4b-207">對</span><span class="sxs-lookup"><span data-stu-id="38b4b-207">True</span></span>                                                      |
| <span data-ttu-id="38b4b-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38b4b-208">Is Indexed</span></span>             | <span data-ttu-id="38b4b-209">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-209">False</span></span>                                                     |
| <span data-ttu-id="38b4b-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38b4b-210">In Global Catalog</span></span>      | <span data-ttu-id="38b4b-211">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-211">False</span></span>                                                     |
| <span data-ttu-id="38b4b-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38b4b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b4b-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38b4b-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38b4b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b4b-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b4b-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-216">Search-Flags</span></span>           | <span data-ttu-id="38b4b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38b4b-217">0x00000000</span></span>                                                |
| <span data-ttu-id="38b4b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-218">System-Flags</span></span>           | <span data-ttu-id="38b4b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b4b-219">0x00000010</span></span>                                                |
| <span data-ttu-id="38b4b-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38b4b-220">Classes used in</span></span>        | [<span data-ttu-id="38b4b-221">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="38b4b-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38b4b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38b4b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38b4b-223">進入</span><span class="sxs-lookup"><span data-stu-id="38b4b-223">Entry</span></span> | <span data-ttu-id="38b4b-224">值</span><span class="sxs-lookup"><span data-stu-id="38b4b-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38b4b-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38b4b-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b4b-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b4b-227">System-Only</span></span>            | <span data-ttu-id="38b4b-228">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-228">False</span></span>                                                     |
| <span data-ttu-id="38b4b-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38b4b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="38b4b-230">對</span><span class="sxs-lookup"><span data-stu-id="38b4b-230">True</span></span>                                                      |
| <span data-ttu-id="38b4b-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38b4b-231">Is Indexed</span></span>             | <span data-ttu-id="38b4b-232">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-232">False</span></span>                                                     |
| <span data-ttu-id="38b4b-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38b4b-233">In Global Catalog</span></span>      | <span data-ttu-id="38b4b-234">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-234">False</span></span>                                                     |
| <span data-ttu-id="38b4b-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38b4b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b4b-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38b4b-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38b4b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b4b-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b4b-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-239">Search-Flags</span></span>           | <span data-ttu-id="38b4b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38b4b-240">0x00000000</span></span>                                                |
| <span data-ttu-id="38b4b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-241">System-Flags</span></span>           | <span data-ttu-id="38b4b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b4b-242">0x00000010</span></span>                                                |
| <span data-ttu-id="38b4b-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38b4b-243">Classes used in</span></span>        | [<span data-ttu-id="38b4b-244">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="38b4b-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38b4b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38b4b-245">Windows Server 2012</span></span>



| <span data-ttu-id="38b4b-246">進入</span><span class="sxs-lookup"><span data-stu-id="38b4b-246">Entry</span></span> | <span data-ttu-id="38b4b-247">值</span><span class="sxs-lookup"><span data-stu-id="38b4b-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="38b4b-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="38b4b-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38b4b-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="38b4b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="38b4b-250">System-Only</span></span>            | <span data-ttu-id="38b4b-251">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-251">False</span></span>                                                     |
| <span data-ttu-id="38b4b-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="38b4b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="38b4b-253">對</span><span class="sxs-lookup"><span data-stu-id="38b4b-253">True</span></span>                                                      |
| <span data-ttu-id="38b4b-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="38b4b-254">Is Indexed</span></span>             | <span data-ttu-id="38b4b-255">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-255">False</span></span>                                                     |
| <span data-ttu-id="38b4b-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="38b4b-256">In Global Catalog</span></span>      | <span data-ttu-id="38b4b-257">否</span><span class="sxs-lookup"><span data-stu-id="38b4b-257">False</span></span>                                                     |
| <span data-ttu-id="38b4b-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="38b4b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="38b4b-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="38b4b-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="38b4b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38b4b-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38b4b-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="38b4b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-262">Search-Flags</span></span>           | <span data-ttu-id="38b4b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38b4b-263">0x00000000</span></span>                                                |
| <span data-ttu-id="38b4b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38b4b-264">System-Flags</span></span>           | <span data-ttu-id="38b4b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38b4b-265">0x00000010</span></span>                                                |
| <span data-ttu-id="38b4b-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="38b4b-266">Classes used in</span></span>        | [<span data-ttu-id="38b4b-267">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="38b4b-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





