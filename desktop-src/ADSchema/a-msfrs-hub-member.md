---
title: ms-FRS-Hub 成員屬性
description: Ms-chap 中樞成員屬性是用來記錄慣用的 NTFRS 拓撲設定。
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- ms-FRS-中樞-成員屬性 AD 架構
- msFRS-中樞-成員屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970858"
---
# <a name="ms-frs-hub-member-attribute"></a><span data-ttu-id="3279a-105">ms-FRS-Hub 成員屬性</span><span class="sxs-lookup"><span data-stu-id="3279a-105">ms-FRS-Hub-Member attribute</span></span>

<span data-ttu-id="3279a-106">**Ms-chap 中樞成員** 屬性是用來記錄慣用的 NTFRS 拓撲設定。</span><span class="sxs-lookup"><span data-stu-id="3279a-106">The **ms-FRS-Hub-Member** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="3279a-107">將 FRS 成員新增或刪除至複本集時，會參考這些屬性，並對複本集中的其他 FRS 成員之間的連接進行適當的調整。</span><span class="sxs-lookup"><span data-stu-id="3279a-107">When an FRS member gets added or deleted to a replica set, these attributes are referred and appropriate adjustments are made to the connections between the rest of the FRS members in the replica set.</span></span>



| <span data-ttu-id="3279a-108">進入</span><span class="sxs-lookup"><span data-stu-id="3279a-108">Entry</span></span> | <span data-ttu-id="3279a-109">值</span><span class="sxs-lookup"><span data-stu-id="3279a-109">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="3279a-110">CN</span><span class="sxs-lookup"><span data-stu-id="3279a-110">CN</span></span>                | <span data-ttu-id="3279a-111">ms-FRS-中樞成員</span><span class="sxs-lookup"><span data-stu-id="3279a-111">ms-FRS-Hub-Member</span></span>                                                  |
| <span data-ttu-id="3279a-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3279a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="3279a-113">msFRS-中樞-成員</span><span class="sxs-lookup"><span data-stu-id="3279a-113">msFRS-Hub-Member</span></span>                                                   |
| <span data-ttu-id="3279a-114">大小</span><span class="sxs-lookup"><span data-stu-id="3279a-114">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="3279a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3279a-115">Update Privilege</span></span>  | <span data-ttu-id="3279a-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="3279a-116">Domain administrator</span></span>                                               |
| <span data-ttu-id="3279a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3279a-117">Update Frequency</span></span>  | <span data-ttu-id="3279a-118">建立複本集或偏好的拓撲變更時。</span><span class="sxs-lookup"><span data-stu-id="3279a-118">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="3279a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3279a-119">Attribute-Id</span></span>      | <span data-ttu-id="3279a-120">1.2.840.113556.1.4.1693</span><span class="sxs-lookup"><span data-stu-id="3279a-120">1.2.840.113556.1.4.1693</span></span>                                            |
| <span data-ttu-id="3279a-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3279a-121">System-Id-Guid</span></span>    | <span data-ttu-id="3279a-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span><span class="sxs-lookup"><span data-stu-id="3279a-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span></span>                               |
| <span data-ttu-id="3279a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3279a-123">Syntax</span></span>            | [<span data-ttu-id="3279a-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3279a-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                            |



## <a name="implementations"></a><span data-ttu-id="3279a-125">實作</span><span class="sxs-lookup"><span data-stu-id="3279a-125">Implementations</span></span>

-   [<span data-ttu-id="3279a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3279a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3279a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3279a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3279a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3279a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3279a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3279a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3279a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3279a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3279a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3279a-131">Windows Server 2003</span></span>



| <span data-ttu-id="3279a-132">進入</span><span class="sxs-lookup"><span data-stu-id="3279a-132">Entry</span></span> | <span data-ttu-id="3279a-133">值</span><span class="sxs-lookup"><span data-stu-id="3279a-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3279a-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3279a-134">Link-Id</span></span>                | <span data-ttu-id="3279a-135">1046</span><span class="sxs-lookup"><span data-stu-id="3279a-135">1046</span></span>                                                      |
| <span data-ttu-id="3279a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3279a-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3279a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3279a-137">System-Only</span></span>            | <span data-ttu-id="3279a-138">否</span><span class="sxs-lookup"><span data-stu-id="3279a-138">False</span></span>                                                     |
| <span data-ttu-id="3279a-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3279a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3279a-140">對</span><span class="sxs-lookup"><span data-stu-id="3279a-140">True</span></span>                                                      |
| <span data-ttu-id="3279a-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3279a-141">Is Indexed</span></span>             | <span data-ttu-id="3279a-142">否</span><span class="sxs-lookup"><span data-stu-id="3279a-142">False</span></span>                                                     |
| <span data-ttu-id="3279a-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3279a-143">In Global Catalog</span></span>      | <span data-ttu-id="3279a-144">否</span><span class="sxs-lookup"><span data-stu-id="3279a-144">False</span></span>                                                     |
| <span data-ttu-id="3279a-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3279a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3279a-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3279a-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3279a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3279a-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3279a-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-149">Search-Flags</span></span>           | <span data-ttu-id="3279a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-150">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-151">System-Flags</span></span>           | <span data-ttu-id="3279a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-152">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3279a-153">Classes used in</span></span>        | [<span data-ttu-id="3279a-154">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3279a-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3279a-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3279a-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3279a-156">進入</span><span class="sxs-lookup"><span data-stu-id="3279a-156">Entry</span></span> | <span data-ttu-id="3279a-157">值</span><span class="sxs-lookup"><span data-stu-id="3279a-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3279a-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3279a-158">Link-Id</span></span>                | <span data-ttu-id="3279a-159">1046</span><span class="sxs-lookup"><span data-stu-id="3279a-159">1046</span></span>                                                      |
| <span data-ttu-id="3279a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3279a-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3279a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3279a-161">System-Only</span></span>            | <span data-ttu-id="3279a-162">否</span><span class="sxs-lookup"><span data-stu-id="3279a-162">False</span></span>                                                     |
| <span data-ttu-id="3279a-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3279a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3279a-164">對</span><span class="sxs-lookup"><span data-stu-id="3279a-164">True</span></span>                                                      |
| <span data-ttu-id="3279a-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3279a-165">Is Indexed</span></span>             | <span data-ttu-id="3279a-166">否</span><span class="sxs-lookup"><span data-stu-id="3279a-166">False</span></span>                                                     |
| <span data-ttu-id="3279a-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3279a-167">In Global Catalog</span></span>      | <span data-ttu-id="3279a-168">否</span><span class="sxs-lookup"><span data-stu-id="3279a-168">False</span></span>                                                     |
| <span data-ttu-id="3279a-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3279a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3279a-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3279a-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3279a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3279a-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3279a-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-173">Search-Flags</span></span>           | <span data-ttu-id="3279a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-174">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-175">System-Flags</span></span>           | <span data-ttu-id="3279a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-176">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3279a-177">Classes used in</span></span>        | [<span data-ttu-id="3279a-178">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3279a-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3279a-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3279a-179">Windows Server 2008</span></span>



| <span data-ttu-id="3279a-180">進入</span><span class="sxs-lookup"><span data-stu-id="3279a-180">Entry</span></span> | <span data-ttu-id="3279a-181">值</span><span class="sxs-lookup"><span data-stu-id="3279a-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3279a-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3279a-182">Link-Id</span></span>                | <span data-ttu-id="3279a-183">1046</span><span class="sxs-lookup"><span data-stu-id="3279a-183">1046</span></span>                                                      |
| <span data-ttu-id="3279a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3279a-184">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3279a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3279a-185">System-Only</span></span>            | <span data-ttu-id="3279a-186">否</span><span class="sxs-lookup"><span data-stu-id="3279a-186">False</span></span>                                                     |
| <span data-ttu-id="3279a-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3279a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3279a-188">對</span><span class="sxs-lookup"><span data-stu-id="3279a-188">True</span></span>                                                      |
| <span data-ttu-id="3279a-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3279a-189">Is Indexed</span></span>             | <span data-ttu-id="3279a-190">否</span><span class="sxs-lookup"><span data-stu-id="3279a-190">False</span></span>                                                     |
| <span data-ttu-id="3279a-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3279a-191">In Global Catalog</span></span>      | <span data-ttu-id="3279a-192">否</span><span class="sxs-lookup"><span data-stu-id="3279a-192">False</span></span>                                                     |
| <span data-ttu-id="3279a-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3279a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3279a-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3279a-194">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3279a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3279a-195">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3279a-196">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-197">Search-Flags</span></span>           | <span data-ttu-id="3279a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-198">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-199">System-Flags</span></span>           | <span data-ttu-id="3279a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-200">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3279a-201">Classes used in</span></span>        | [<span data-ttu-id="3279a-202">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3279a-202">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3279a-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3279a-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3279a-204">進入</span><span class="sxs-lookup"><span data-stu-id="3279a-204">Entry</span></span> | <span data-ttu-id="3279a-205">值</span><span class="sxs-lookup"><span data-stu-id="3279a-205">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3279a-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3279a-206">Link-Id</span></span>                | <span data-ttu-id="3279a-207">1046</span><span class="sxs-lookup"><span data-stu-id="3279a-207">1046</span></span>                                                      |
| <span data-ttu-id="3279a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3279a-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3279a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="3279a-209">System-Only</span></span>            | <span data-ttu-id="3279a-210">否</span><span class="sxs-lookup"><span data-stu-id="3279a-210">False</span></span>                                                     |
| <span data-ttu-id="3279a-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3279a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="3279a-212">對</span><span class="sxs-lookup"><span data-stu-id="3279a-212">True</span></span>                                                      |
| <span data-ttu-id="3279a-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3279a-213">Is Indexed</span></span>             | <span data-ttu-id="3279a-214">否</span><span class="sxs-lookup"><span data-stu-id="3279a-214">False</span></span>                                                     |
| <span data-ttu-id="3279a-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3279a-215">In Global Catalog</span></span>      | <span data-ttu-id="3279a-216">否</span><span class="sxs-lookup"><span data-stu-id="3279a-216">False</span></span>                                                     |
| <span data-ttu-id="3279a-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3279a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="3279a-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3279a-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3279a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3279a-219">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3279a-220">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-221">Search-Flags</span></span>           | <span data-ttu-id="3279a-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-222">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-223">System-Flags</span></span>           | <span data-ttu-id="3279a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-224">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3279a-225">Classes used in</span></span>        | [<span data-ttu-id="3279a-226">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3279a-226">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3279a-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3279a-227">Windows Server 2012</span></span>



| <span data-ttu-id="3279a-228">進入</span><span class="sxs-lookup"><span data-stu-id="3279a-228">Entry</span></span> | <span data-ttu-id="3279a-229">值</span><span class="sxs-lookup"><span data-stu-id="3279a-229">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3279a-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3279a-230">Link-Id</span></span>                | <span data-ttu-id="3279a-231">1046</span><span class="sxs-lookup"><span data-stu-id="3279a-231">1046</span></span>                                                      |
| <span data-ttu-id="3279a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3279a-232">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="3279a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="3279a-233">System-Only</span></span>            | <span data-ttu-id="3279a-234">否</span><span class="sxs-lookup"><span data-stu-id="3279a-234">False</span></span>                                                     |
| <span data-ttu-id="3279a-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3279a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="3279a-236">對</span><span class="sxs-lookup"><span data-stu-id="3279a-236">True</span></span>                                                      |
| <span data-ttu-id="3279a-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3279a-237">Is Indexed</span></span>             | <span data-ttu-id="3279a-238">否</span><span class="sxs-lookup"><span data-stu-id="3279a-238">False</span></span>                                                     |
| <span data-ttu-id="3279a-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3279a-239">In Global Catalog</span></span>      | <span data-ttu-id="3279a-240">否</span><span class="sxs-lookup"><span data-stu-id="3279a-240">False</span></span>                                                     |
| <span data-ttu-id="3279a-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3279a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="3279a-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3279a-242">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="3279a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3279a-243">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3279a-244">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="3279a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-245">Search-Flags</span></span>           | <span data-ttu-id="3279a-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-246">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3279a-247">System-Flags</span></span>           | <span data-ttu-id="3279a-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3279a-248">0x00000000</span></span>                                                |
| <span data-ttu-id="3279a-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3279a-249">Classes used in</span></span>        | [<span data-ttu-id="3279a-250">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="3279a-250">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3279a-251">備註</span><span class="sxs-lookup"><span data-stu-id="3279a-251">Remarks</span></span>

<span data-ttu-id="3279a-252">這是 [**NTFRS 成員**](c-ntfrsmember.md) 物件的完整分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="3279a-252">This is the fully qualified distinguished name of an [**NTFRS-Member**](c-ntfrsmember.md) object.</span></span> <span data-ttu-id="3279a-253">辨別名稱的格式為 "CN = *<computerGuid>* ，cn = *<Dfs Link Name>* ，cn = *<Dfs Root name>* ，Cn = DFS 磁片區，Cn = File REPLICATION Service，cn = System，DC = ..."</span><span class="sxs-lookup"><span data-stu-id="3279a-253">The distinguished name is in the format of "CN=*<computerGuid>*, CN=*<Dfs Link Name>*, CN=*<Dfs Root name>*, CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."</span></span>

 

 





