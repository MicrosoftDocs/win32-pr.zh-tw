---
title: FRS 層級限制屬性
description: 要複寫以進行檔案複寫的目錄樹狀目錄深度限制。
ms.assetid: e2916cbd-1ce7-4ff7-82a2-5fbdae3c6a1b
ms.tgt_platform: multiple
keywords:
- FRS 層級限制屬性 AD 架構
- fRSLevelLimit 屬性 AD 架構
topic_type:
- apiref
api_name:
- FRS-Level-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c587565eb10014ef638a2320dd9229d8409ba06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106968808"
---
# <a name="frs-level-limit-attribute"></a><span data-ttu-id="84bef-105">FRS 層級限制屬性</span><span class="sxs-lookup"><span data-stu-id="84bef-105">FRS-Level-Limit attribute</span></span>

<span data-ttu-id="84bef-106">要複寫以進行檔案複寫的目錄樹狀目錄深度限制。</span><span class="sxs-lookup"><span data-stu-id="84bef-106">Limit depth of directory tree to replicate for file replication.</span></span>



| <span data-ttu-id="84bef-107">進入</span><span class="sxs-lookup"><span data-stu-id="84bef-107">Entry</span></span> | <span data-ttu-id="84bef-108">值</span><span class="sxs-lookup"><span data-stu-id="84bef-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="84bef-109">CN</span><span class="sxs-lookup"><span data-stu-id="84bef-109">CN</span></span>                | <span data-ttu-id="84bef-110">FRS 層級限制</span><span class="sxs-lookup"><span data-stu-id="84bef-110">FRS-Level-Limit</span></span>                      |
| <span data-ttu-id="84bef-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="84bef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="84bef-112">fRSLevelLimit</span><span class="sxs-lookup"><span data-stu-id="84bef-112">fRSLevelLimit</span></span>                        |
| <span data-ttu-id="84bef-113">大小</span><span class="sxs-lookup"><span data-stu-id="84bef-113">Size</span></span>              | <span data-ttu-id="84bef-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="84bef-114">4 bytes</span></span>                              |
| <span data-ttu-id="84bef-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="84bef-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="84bef-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="84bef-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="84bef-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="84bef-117">Attribute-Id</span></span>      | <span data-ttu-id="84bef-118">1.2.840.113556.1.4.534</span><span class="sxs-lookup"><span data-stu-id="84bef-118">1.2.840.113556.1.4.534</span></span>               |
| <span data-ttu-id="84bef-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="84bef-119">System-Id-Guid</span></span>    | <span data-ttu-id="84bef-120">5245801e-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="84bef-120">5245801e-ca6a-11d0-afff-0000f80367c1</span></span> |
| <span data-ttu-id="84bef-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="84bef-121">Syntax</span></span>            | [<span data-ttu-id="84bef-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="84bef-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="84bef-123">實作</span><span class="sxs-lookup"><span data-stu-id="84bef-123">Implementations</span></span>

-   [<span data-ttu-id="84bef-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="84bef-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="84bef-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="84bef-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="84bef-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="84bef-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="84bef-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="84bef-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="84bef-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="84bef-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="84bef-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="84bef-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="84bef-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84bef-130">Windows 2000 Server</span></span>



| <span data-ttu-id="84bef-131">進入</span><span class="sxs-lookup"><span data-stu-id="84bef-131">Entry</span></span> | <span data-ttu-id="84bef-132">值</span><span class="sxs-lookup"><span data-stu-id="84bef-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84bef-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84bef-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84bef-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="84bef-135">System-Only</span></span>            | <span data-ttu-id="84bef-136">否</span><span class="sxs-lookup"><span data-stu-id="84bef-136">False</span></span>                                                     |
| <span data-ttu-id="84bef-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84bef-137">Is-Single-Valued</span></span>       | <span data-ttu-id="84bef-138">對</span><span class="sxs-lookup"><span data-stu-id="84bef-138">True</span></span>                                                      |
| <span data-ttu-id="84bef-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84bef-139">Is Indexed</span></span>             | <span data-ttu-id="84bef-140">否</span><span class="sxs-lookup"><span data-stu-id="84bef-140">False</span></span>                                                     |
| <span data-ttu-id="84bef-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84bef-141">In Global Catalog</span></span>      | <span data-ttu-id="84bef-142">否</span><span class="sxs-lookup"><span data-stu-id="84bef-142">False</span></span>                                                     |
| <span data-ttu-id="84bef-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84bef-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="84bef-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84bef-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84bef-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84bef-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84bef-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-147">Search-Flags</span></span>           | <span data-ttu-id="84bef-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84bef-148">0x00000000</span></span>                                                |
| <span data-ttu-id="84bef-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-149">System-Flags</span></span>           | <span data-ttu-id="84bef-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84bef-150">0x00000010</span></span>                                                |
| <span data-ttu-id="84bef-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84bef-151">Classes used in</span></span>        | [<span data-ttu-id="84bef-152">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="84bef-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="84bef-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84bef-153">Windows Server 2003</span></span>



| <span data-ttu-id="84bef-154">進入</span><span class="sxs-lookup"><span data-stu-id="84bef-154">Entry</span></span> | <span data-ttu-id="84bef-155">值</span><span class="sxs-lookup"><span data-stu-id="84bef-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84bef-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84bef-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84bef-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="84bef-158">System-Only</span></span>            | <span data-ttu-id="84bef-159">否</span><span class="sxs-lookup"><span data-stu-id="84bef-159">False</span></span>                                                     |
| <span data-ttu-id="84bef-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84bef-160">Is-Single-Valued</span></span>       | <span data-ttu-id="84bef-161">對</span><span class="sxs-lookup"><span data-stu-id="84bef-161">True</span></span>                                                      |
| <span data-ttu-id="84bef-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84bef-162">Is Indexed</span></span>             | <span data-ttu-id="84bef-163">否</span><span class="sxs-lookup"><span data-stu-id="84bef-163">False</span></span>                                                     |
| <span data-ttu-id="84bef-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84bef-164">In Global Catalog</span></span>      | <span data-ttu-id="84bef-165">否</span><span class="sxs-lookup"><span data-stu-id="84bef-165">False</span></span>                                                     |
| <span data-ttu-id="84bef-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84bef-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="84bef-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84bef-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84bef-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84bef-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84bef-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-170">Search-Flags</span></span>           | <span data-ttu-id="84bef-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84bef-171">0x00000000</span></span>                                                |
| <span data-ttu-id="84bef-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-172">System-Flags</span></span>           | <span data-ttu-id="84bef-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84bef-173">0x00000010</span></span>                                                |
| <span data-ttu-id="84bef-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84bef-174">Classes used in</span></span>        | [<span data-ttu-id="84bef-175">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="84bef-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="84bef-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="84bef-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="84bef-177">進入</span><span class="sxs-lookup"><span data-stu-id="84bef-177">Entry</span></span> | <span data-ttu-id="84bef-178">值</span><span class="sxs-lookup"><span data-stu-id="84bef-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84bef-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84bef-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84bef-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="84bef-181">System-Only</span></span>            | <span data-ttu-id="84bef-182">否</span><span class="sxs-lookup"><span data-stu-id="84bef-182">False</span></span>                                                     |
| <span data-ttu-id="84bef-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84bef-183">Is-Single-Valued</span></span>       | <span data-ttu-id="84bef-184">對</span><span class="sxs-lookup"><span data-stu-id="84bef-184">True</span></span>                                                      |
| <span data-ttu-id="84bef-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84bef-185">Is Indexed</span></span>             | <span data-ttu-id="84bef-186">否</span><span class="sxs-lookup"><span data-stu-id="84bef-186">False</span></span>                                                     |
| <span data-ttu-id="84bef-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84bef-187">In Global Catalog</span></span>      | <span data-ttu-id="84bef-188">否</span><span class="sxs-lookup"><span data-stu-id="84bef-188">False</span></span>                                                     |
| <span data-ttu-id="84bef-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84bef-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="84bef-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84bef-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84bef-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84bef-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84bef-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-193">Search-Flags</span></span>           | <span data-ttu-id="84bef-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84bef-194">0x00000000</span></span>                                                |
| <span data-ttu-id="84bef-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-195">System-Flags</span></span>           | <span data-ttu-id="84bef-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84bef-196">0x00000010</span></span>                                                |
| <span data-ttu-id="84bef-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84bef-197">Classes used in</span></span>        | [<span data-ttu-id="84bef-198">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="84bef-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="84bef-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84bef-199">Windows Server 2008</span></span>



| <span data-ttu-id="84bef-200">進入</span><span class="sxs-lookup"><span data-stu-id="84bef-200">Entry</span></span> | <span data-ttu-id="84bef-201">值</span><span class="sxs-lookup"><span data-stu-id="84bef-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84bef-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84bef-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84bef-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="84bef-204">System-Only</span></span>            | <span data-ttu-id="84bef-205">否</span><span class="sxs-lookup"><span data-stu-id="84bef-205">False</span></span>                                                     |
| <span data-ttu-id="84bef-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84bef-206">Is-Single-Valued</span></span>       | <span data-ttu-id="84bef-207">對</span><span class="sxs-lookup"><span data-stu-id="84bef-207">True</span></span>                                                      |
| <span data-ttu-id="84bef-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84bef-208">Is Indexed</span></span>             | <span data-ttu-id="84bef-209">否</span><span class="sxs-lookup"><span data-stu-id="84bef-209">False</span></span>                                                     |
| <span data-ttu-id="84bef-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84bef-210">In Global Catalog</span></span>      | <span data-ttu-id="84bef-211">否</span><span class="sxs-lookup"><span data-stu-id="84bef-211">False</span></span>                                                     |
| <span data-ttu-id="84bef-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84bef-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="84bef-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84bef-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84bef-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84bef-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84bef-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-216">Search-Flags</span></span>           | <span data-ttu-id="84bef-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84bef-217">0x00000000</span></span>                                                |
| <span data-ttu-id="84bef-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-218">System-Flags</span></span>           | <span data-ttu-id="84bef-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84bef-219">0x00000010</span></span>                                                |
| <span data-ttu-id="84bef-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84bef-220">Classes used in</span></span>        | [<span data-ttu-id="84bef-221">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="84bef-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="84bef-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84bef-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="84bef-223">進入</span><span class="sxs-lookup"><span data-stu-id="84bef-223">Entry</span></span> | <span data-ttu-id="84bef-224">值</span><span class="sxs-lookup"><span data-stu-id="84bef-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84bef-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84bef-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84bef-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="84bef-227">System-Only</span></span>            | <span data-ttu-id="84bef-228">否</span><span class="sxs-lookup"><span data-stu-id="84bef-228">False</span></span>                                                     |
| <span data-ttu-id="84bef-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84bef-229">Is-Single-Valued</span></span>       | <span data-ttu-id="84bef-230">對</span><span class="sxs-lookup"><span data-stu-id="84bef-230">True</span></span>                                                      |
| <span data-ttu-id="84bef-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84bef-231">Is Indexed</span></span>             | <span data-ttu-id="84bef-232">否</span><span class="sxs-lookup"><span data-stu-id="84bef-232">False</span></span>                                                     |
| <span data-ttu-id="84bef-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84bef-233">In Global Catalog</span></span>      | <span data-ttu-id="84bef-234">否</span><span class="sxs-lookup"><span data-stu-id="84bef-234">False</span></span>                                                     |
| <span data-ttu-id="84bef-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84bef-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="84bef-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84bef-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84bef-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84bef-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84bef-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-239">Search-Flags</span></span>           | <span data-ttu-id="84bef-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84bef-240">0x00000000</span></span>                                                |
| <span data-ttu-id="84bef-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-241">System-Flags</span></span>           | <span data-ttu-id="84bef-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84bef-242">0x00000010</span></span>                                                |
| <span data-ttu-id="84bef-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84bef-243">Classes used in</span></span>        | [<span data-ttu-id="84bef-244">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="84bef-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="84bef-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84bef-245">Windows Server 2012</span></span>



| <span data-ttu-id="84bef-246">進入</span><span class="sxs-lookup"><span data-stu-id="84bef-246">Entry</span></span> | <span data-ttu-id="84bef-247">值</span><span class="sxs-lookup"><span data-stu-id="84bef-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="84bef-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="84bef-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84bef-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="84bef-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="84bef-250">System-Only</span></span>            | <span data-ttu-id="84bef-251">否</span><span class="sxs-lookup"><span data-stu-id="84bef-251">False</span></span>                                                     |
| <span data-ttu-id="84bef-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="84bef-252">Is-Single-Valued</span></span>       | <span data-ttu-id="84bef-253">對</span><span class="sxs-lookup"><span data-stu-id="84bef-253">True</span></span>                                                      |
| <span data-ttu-id="84bef-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="84bef-254">Is Indexed</span></span>             | <span data-ttu-id="84bef-255">否</span><span class="sxs-lookup"><span data-stu-id="84bef-255">False</span></span>                                                     |
| <span data-ttu-id="84bef-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="84bef-256">In Global Catalog</span></span>      | <span data-ttu-id="84bef-257">否</span><span class="sxs-lookup"><span data-stu-id="84bef-257">False</span></span>                                                     |
| <span data-ttu-id="84bef-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="84bef-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="84bef-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="84bef-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="84bef-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84bef-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84bef-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="84bef-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-262">Search-Flags</span></span>           | <span data-ttu-id="84bef-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84bef-263">0x00000000</span></span>                                                |
| <span data-ttu-id="84bef-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84bef-264">System-Flags</span></span>           | <span data-ttu-id="84bef-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84bef-265">0x00000010</span></span>                                                |
| <span data-ttu-id="84bef-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="84bef-266">Classes used in</span></span>        | [<span data-ttu-id="84bef-267">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="84bef-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





