---
title: 原則-複寫-旗標屬性
description: 決定要將哪些 LSA 屬性複寫到用戶端。
ms.assetid: 2dadd659-c834-4105-ab3e-8ce0b8811212
ms.tgt_platform: multiple
keywords:
- 原則-複寫-旗標屬性 AD 架構
- policyReplicationFlags 屬性 AD 架構
topic_type:
- apiref
api_name:
- Policy-Replication-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42da6509662d11c4a069ba58dff5f648e7ab2261
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106969829"
---
# <a name="policy-replication-flags-attribute"></a><span data-ttu-id="4b663-105">原則-複寫-旗標屬性</span><span class="sxs-lookup"><span data-stu-id="4b663-105">Policy-Replication-Flags attribute</span></span>

<span data-ttu-id="4b663-106">決定要將哪些 LSA 屬性複寫到用戶端。</span><span class="sxs-lookup"><span data-stu-id="4b663-106">Determines which LSA properties are replicated to clients.</span></span>



| <span data-ttu-id="4b663-107">進入</span><span class="sxs-lookup"><span data-stu-id="4b663-107">Entry</span></span> | <span data-ttu-id="4b663-108">值</span><span class="sxs-lookup"><span data-stu-id="4b663-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4b663-109">CN</span><span class="sxs-lookup"><span data-stu-id="4b663-109">CN</span></span>                | <span data-ttu-id="4b663-110">原則-複寫-旗標</span><span class="sxs-lookup"><span data-stu-id="4b663-110">Policy-Replication-Flags</span></span>             |
| <span data-ttu-id="4b663-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4b663-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4b663-112">policyReplicationFlags</span><span class="sxs-lookup"><span data-stu-id="4b663-112">policyReplicationFlags</span></span>               |
| <span data-ttu-id="4b663-113">大小</span><span class="sxs-lookup"><span data-stu-id="4b663-113">Size</span></span>              | <span data-ttu-id="4b663-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="4b663-114">4 bytes</span></span>                              |
| <span data-ttu-id="4b663-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4b663-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4b663-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4b663-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4b663-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b663-117">Attribute-Id</span></span>      | <span data-ttu-id="4b663-118">1.2.840.113556.1.4.633</span><span class="sxs-lookup"><span data-stu-id="4b663-118">1.2.840.113556.1.4.633</span></span>               |
| <span data-ttu-id="4b663-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4b663-119">System-Id-Guid</span></span>    | <span data-ttu-id="4b663-120">19405b96-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4b663-120">19405b96-3cfa-11d1-a9c0-0000f80367c1</span></span> |
| <span data-ttu-id="4b663-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b663-121">Syntax</span></span>            | [<span data-ttu-id="4b663-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="4b663-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="4b663-123">實作</span><span class="sxs-lookup"><span data-stu-id="4b663-123">Implementations</span></span>

-   [<span data-ttu-id="4b663-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4b663-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4b663-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b663-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b663-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b663-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b663-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b663-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b663-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b663-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b663-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b663-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4b663-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b663-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4b663-131">進入</span><span class="sxs-lookup"><span data-stu-id="4b663-131">Entry</span></span> | <span data-ttu-id="4b663-132">值</span><span class="sxs-lookup"><span data-stu-id="4b663-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="4b663-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4b663-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b663-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b663-135">System-Only</span></span>            | <span data-ttu-id="4b663-136">否</span><span class="sxs-lookup"><span data-stu-id="4b663-136">False</span></span>                                     |
| <span data-ttu-id="4b663-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4b663-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4b663-138">對</span><span class="sxs-lookup"><span data-stu-id="4b663-138">True</span></span>                                      |
| <span data-ttu-id="4b663-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4b663-139">Is Indexed</span></span>             | <span data-ttu-id="4b663-140">否</span><span class="sxs-lookup"><span data-stu-id="4b663-140">False</span></span>                                     |
| <span data-ttu-id="4b663-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4b663-141">In Global Catalog</span></span>      | <span data-ttu-id="4b663-142">否</span><span class="sxs-lookup"><span data-stu-id="4b663-142">False</span></span>                                     |
| <span data-ttu-id="4b663-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4b663-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b663-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4b663-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="4b663-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b663-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="4b663-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b663-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="4b663-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-147">Search-Flags</span></span>           | <span data-ttu-id="4b663-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b663-148">0x00000000</span></span>                                |
| <span data-ttu-id="4b663-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-149">System-Flags</span></span>           | <span data-ttu-id="4b663-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b663-150">0x00000010</span></span>                                |
| <span data-ttu-id="4b663-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4b663-151">Classes used in</span></span>        | [<span data-ttu-id="4b663-152">**電腦**</span><span class="sxs-lookup"><span data-stu-id="4b663-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4b663-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b663-153">Windows Server 2003</span></span>



| <span data-ttu-id="4b663-154">進入</span><span class="sxs-lookup"><span data-stu-id="4b663-154">Entry</span></span> | <span data-ttu-id="4b663-155">值</span><span class="sxs-lookup"><span data-stu-id="4b663-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="4b663-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4b663-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b663-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b663-158">System-Only</span></span>            | <span data-ttu-id="4b663-159">否</span><span class="sxs-lookup"><span data-stu-id="4b663-159">False</span></span>                                     |
| <span data-ttu-id="4b663-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4b663-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4b663-161">對</span><span class="sxs-lookup"><span data-stu-id="4b663-161">True</span></span>                                      |
| <span data-ttu-id="4b663-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4b663-162">Is Indexed</span></span>             | <span data-ttu-id="4b663-163">否</span><span class="sxs-lookup"><span data-stu-id="4b663-163">False</span></span>                                     |
| <span data-ttu-id="4b663-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4b663-164">In Global Catalog</span></span>      | <span data-ttu-id="4b663-165">否</span><span class="sxs-lookup"><span data-stu-id="4b663-165">False</span></span>                                     |
| <span data-ttu-id="4b663-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4b663-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b663-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4b663-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="4b663-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b663-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="4b663-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b663-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="4b663-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-170">Search-Flags</span></span>           | <span data-ttu-id="4b663-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b663-171">0x00000000</span></span>                                |
| <span data-ttu-id="4b663-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-172">System-Flags</span></span>           | <span data-ttu-id="4b663-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b663-173">0x00000010</span></span>                                |
| <span data-ttu-id="4b663-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4b663-174">Classes used in</span></span>        | [<span data-ttu-id="4b663-175">**電腦**</span><span class="sxs-lookup"><span data-stu-id="4b663-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b663-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b663-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b663-177">進入</span><span class="sxs-lookup"><span data-stu-id="4b663-177">Entry</span></span> | <span data-ttu-id="4b663-178">值</span><span class="sxs-lookup"><span data-stu-id="4b663-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="4b663-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4b663-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b663-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b663-181">System-Only</span></span>            | <span data-ttu-id="4b663-182">否</span><span class="sxs-lookup"><span data-stu-id="4b663-182">False</span></span>                                     |
| <span data-ttu-id="4b663-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4b663-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4b663-184">對</span><span class="sxs-lookup"><span data-stu-id="4b663-184">True</span></span>                                      |
| <span data-ttu-id="4b663-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4b663-185">Is Indexed</span></span>             | <span data-ttu-id="4b663-186">否</span><span class="sxs-lookup"><span data-stu-id="4b663-186">False</span></span>                                     |
| <span data-ttu-id="4b663-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4b663-187">In Global Catalog</span></span>      | <span data-ttu-id="4b663-188">否</span><span class="sxs-lookup"><span data-stu-id="4b663-188">False</span></span>                                     |
| <span data-ttu-id="4b663-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4b663-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b663-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4b663-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="4b663-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b663-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="4b663-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b663-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="4b663-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-193">Search-Flags</span></span>           | <span data-ttu-id="4b663-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b663-194">0x00000000</span></span>                                |
| <span data-ttu-id="4b663-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-195">System-Flags</span></span>           | <span data-ttu-id="4b663-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b663-196">0x00000010</span></span>                                |
| <span data-ttu-id="4b663-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4b663-197">Classes used in</span></span>        | [<span data-ttu-id="4b663-198">**電腦**</span><span class="sxs-lookup"><span data-stu-id="4b663-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b663-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b663-199">Windows Server 2008</span></span>



| <span data-ttu-id="4b663-200">進入</span><span class="sxs-lookup"><span data-stu-id="4b663-200">Entry</span></span> | <span data-ttu-id="4b663-201">值</span><span class="sxs-lookup"><span data-stu-id="4b663-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="4b663-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4b663-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b663-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b663-204">System-Only</span></span>            | <span data-ttu-id="4b663-205">否</span><span class="sxs-lookup"><span data-stu-id="4b663-205">False</span></span>                                     |
| <span data-ttu-id="4b663-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4b663-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4b663-207">對</span><span class="sxs-lookup"><span data-stu-id="4b663-207">True</span></span>                                      |
| <span data-ttu-id="4b663-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4b663-208">Is Indexed</span></span>             | <span data-ttu-id="4b663-209">否</span><span class="sxs-lookup"><span data-stu-id="4b663-209">False</span></span>                                     |
| <span data-ttu-id="4b663-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4b663-210">In Global Catalog</span></span>      | <span data-ttu-id="4b663-211">否</span><span class="sxs-lookup"><span data-stu-id="4b663-211">False</span></span>                                     |
| <span data-ttu-id="4b663-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4b663-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b663-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4b663-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="4b663-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b663-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="4b663-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b663-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="4b663-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-216">Search-Flags</span></span>           | <span data-ttu-id="4b663-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b663-217">0x00000000</span></span>                                |
| <span data-ttu-id="4b663-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-218">System-Flags</span></span>           | <span data-ttu-id="4b663-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b663-219">0x00000010</span></span>                                |
| <span data-ttu-id="4b663-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4b663-220">Classes used in</span></span>        | [<span data-ttu-id="4b663-221">**電腦**</span><span class="sxs-lookup"><span data-stu-id="4b663-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b663-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b663-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b663-223">進入</span><span class="sxs-lookup"><span data-stu-id="4b663-223">Entry</span></span> | <span data-ttu-id="4b663-224">值</span><span class="sxs-lookup"><span data-stu-id="4b663-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="4b663-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4b663-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b663-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b663-227">System-Only</span></span>            | <span data-ttu-id="4b663-228">否</span><span class="sxs-lookup"><span data-stu-id="4b663-228">False</span></span>                                     |
| <span data-ttu-id="4b663-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4b663-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4b663-230">對</span><span class="sxs-lookup"><span data-stu-id="4b663-230">True</span></span>                                      |
| <span data-ttu-id="4b663-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4b663-231">Is Indexed</span></span>             | <span data-ttu-id="4b663-232">否</span><span class="sxs-lookup"><span data-stu-id="4b663-232">False</span></span>                                     |
| <span data-ttu-id="4b663-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4b663-233">In Global Catalog</span></span>      | <span data-ttu-id="4b663-234">否</span><span class="sxs-lookup"><span data-stu-id="4b663-234">False</span></span>                                     |
| <span data-ttu-id="4b663-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4b663-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b663-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4b663-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="4b663-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b663-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="4b663-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b663-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="4b663-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-239">Search-Flags</span></span>           | <span data-ttu-id="4b663-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b663-240">0x00000000</span></span>                                |
| <span data-ttu-id="4b663-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-241">System-Flags</span></span>           | <span data-ttu-id="4b663-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b663-242">0x00000010</span></span>                                |
| <span data-ttu-id="4b663-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4b663-243">Classes used in</span></span>        | [<span data-ttu-id="4b663-244">**電腦**</span><span class="sxs-lookup"><span data-stu-id="4b663-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b663-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b663-245">Windows Server 2012</span></span>



| <span data-ttu-id="4b663-246">進入</span><span class="sxs-lookup"><span data-stu-id="4b663-246">Entry</span></span> | <span data-ttu-id="4b663-247">值</span><span class="sxs-lookup"><span data-stu-id="4b663-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="4b663-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4b663-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b663-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="4b663-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b663-250">System-Only</span></span>            | <span data-ttu-id="4b663-251">否</span><span class="sxs-lookup"><span data-stu-id="4b663-251">False</span></span>                                     |
| <span data-ttu-id="4b663-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4b663-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4b663-253">對</span><span class="sxs-lookup"><span data-stu-id="4b663-253">True</span></span>                                      |
| <span data-ttu-id="4b663-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4b663-254">Is Indexed</span></span>             | <span data-ttu-id="4b663-255">否</span><span class="sxs-lookup"><span data-stu-id="4b663-255">False</span></span>                                     |
| <span data-ttu-id="4b663-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4b663-256">In Global Catalog</span></span>      | <span data-ttu-id="4b663-257">否</span><span class="sxs-lookup"><span data-stu-id="4b663-257">False</span></span>                                     |
| <span data-ttu-id="4b663-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4b663-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b663-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4b663-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="4b663-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b663-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="4b663-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b663-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="4b663-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-262">Search-Flags</span></span>           | <span data-ttu-id="4b663-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b663-263">0x00000000</span></span>                                |
| <span data-ttu-id="4b663-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b663-264">System-Flags</span></span>           | <span data-ttu-id="4b663-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b663-265">0x00000010</span></span>                                |
| <span data-ttu-id="4b663-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4b663-266">Classes used in</span></span>        | [<span data-ttu-id="4b663-267">**電腦**</span><span class="sxs-lookup"><span data-stu-id="4b663-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





