---
title: 複寫-拓撲-持續執行屬性
description: 刪除伺服器物件與從複寫拓撲中永久移除之間的延遲。
ms.assetid: 770231b0-4886-41c2-a3b5-ac488ac09669
ms.tgt_platform: multiple
keywords:
- 複寫-拓撲-持續執行屬性 AD 架構
- replTopologyStayOfExecution 屬性 AD 架構
topic_type:
- apiref
api_name:
- Repl-Topology-Stay-Of-Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51c74c477cce926dd18ea17b8df2b1adcf99df1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686955"
---
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="717a6-105">複寫-拓撲-持續執行屬性</span><span class="sxs-lookup"><span data-stu-id="717a6-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="717a6-106">刪除伺服器物件與從複寫拓撲中永久移除之間的延遲。</span><span class="sxs-lookup"><span data-stu-id="717a6-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="717a6-107">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-107">Entry</span></span> | <span data-ttu-id="717a6-108">值</span><span class="sxs-lookup"><span data-stu-id="717a6-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="717a6-109">CN</span><span class="sxs-lookup"><span data-stu-id="717a6-109">CN</span></span>                | <span data-ttu-id="717a6-110">複寫-拓撲-持續執行</span><span class="sxs-lookup"><span data-stu-id="717a6-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="717a6-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="717a6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="717a6-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="717a6-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="717a6-113">大小</span><span class="sxs-lookup"><span data-stu-id="717a6-113">Size</span></span>              | <span data-ttu-id="717a6-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="717a6-114">4 bytes</span></span>                              |
| <span data-ttu-id="717a6-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="717a6-115">Update Privilege</span></span>  | <span data-ttu-id="717a6-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="717a6-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="717a6-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="717a6-117">Update Frequency</span></span>  | <span data-ttu-id="717a6-118">每次刪除伺服器物件時。</span><span class="sxs-lookup"><span data-stu-id="717a6-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="717a6-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-119">Attribute-Id</span></span>      | <span data-ttu-id="717a6-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="717a6-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="717a6-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="717a6-121">System-Id-Guid</span></span>    | <span data-ttu-id="717a6-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="717a6-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="717a6-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="717a6-123">Syntax</span></span>            | [<span data-ttu-id="717a6-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="717a6-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="717a6-125">實作</span><span class="sxs-lookup"><span data-stu-id="717a6-125">Implementations</span></span>

-   [<span data-ttu-id="717a6-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="717a6-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="717a6-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="717a6-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="717a6-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="717a6-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="717a6-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="717a6-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="717a6-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="717a6-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="717a6-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="717a6-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="717a6-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="717a6-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="717a6-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="717a6-133">Windows 2000 Server</span></span>



| <span data-ttu-id="717a6-134">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-134">Entry</span></span> | <span data-ttu-id="717a6-135">值</span><span class="sxs-lookup"><span data-stu-id="717a6-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="717a6-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="717a6-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="717a6-138">System-Only</span></span>            | <span data-ttu-id="717a6-139">否</span><span class="sxs-lookup"><span data-stu-id="717a6-139">False</span></span>                                            |
| <span data-ttu-id="717a6-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="717a6-140">Is-Single-Valued</span></span>       | <span data-ttu-id="717a6-141">對</span><span class="sxs-lookup"><span data-stu-id="717a6-141">True</span></span>                                             |
| <span data-ttu-id="717a6-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="717a6-142">Is Indexed</span></span>             | <span data-ttu-id="717a6-143">否</span><span class="sxs-lookup"><span data-stu-id="717a6-143">False</span></span>                                            |
| <span data-ttu-id="717a6-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="717a6-144">In Global Catalog</span></span>      | <span data-ttu-id="717a6-145">否</span><span class="sxs-lookup"><span data-stu-id="717a6-145">False</span></span>                                            |
| <span data-ttu-id="717a6-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="717a6-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="717a6-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="717a6-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="717a6-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="717a6-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="717a6-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="717a6-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="717a6-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-150">Search-Flags</span></span>           | <span data-ttu-id="717a6-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="717a6-151">0x00000000</span></span>                                       |
| <span data-ttu-id="717a6-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-152">System-Flags</span></span>           | <span data-ttu-id="717a6-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="717a6-153">0x00000010</span></span>                                       |
| <span data-ttu-id="717a6-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="717a6-154">Classes used in</span></span>        | [<span data-ttu-id="717a6-155">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="717a6-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="717a6-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="717a6-156">Windows Server 2003</span></span>



| <span data-ttu-id="717a6-157">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-157">Entry</span></span> | <span data-ttu-id="717a6-158">值</span><span class="sxs-lookup"><span data-stu-id="717a6-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="717a6-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="717a6-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="717a6-161">System-Only</span></span>            | <span data-ttu-id="717a6-162">否</span><span class="sxs-lookup"><span data-stu-id="717a6-162">False</span></span>                                            |
| <span data-ttu-id="717a6-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="717a6-163">Is-Single-Valued</span></span>       | <span data-ttu-id="717a6-164">對</span><span class="sxs-lookup"><span data-stu-id="717a6-164">True</span></span>                                             |
| <span data-ttu-id="717a6-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="717a6-165">Is Indexed</span></span>             | <span data-ttu-id="717a6-166">否</span><span class="sxs-lookup"><span data-stu-id="717a6-166">False</span></span>                                            |
| <span data-ttu-id="717a6-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="717a6-167">In Global Catalog</span></span>      | <span data-ttu-id="717a6-168">否</span><span class="sxs-lookup"><span data-stu-id="717a6-168">False</span></span>                                            |
| <span data-ttu-id="717a6-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="717a6-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="717a6-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="717a6-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="717a6-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="717a6-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="717a6-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="717a6-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="717a6-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-173">Search-Flags</span></span>           | <span data-ttu-id="717a6-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="717a6-174">0x00000000</span></span>                                       |
| <span data-ttu-id="717a6-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-175">System-Flags</span></span>           | <span data-ttu-id="717a6-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="717a6-176">0x00000010</span></span>                                       |
| <span data-ttu-id="717a6-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="717a6-177">Classes used in</span></span>        | [<span data-ttu-id="717a6-178">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="717a6-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="717a6-179">亞當</span><span class="sxs-lookup"><span data-stu-id="717a6-179">ADAM</span></span>



| <span data-ttu-id="717a6-180">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-180">Entry</span></span> | <span data-ttu-id="717a6-181">值</span><span class="sxs-lookup"><span data-stu-id="717a6-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="717a6-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="717a6-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="717a6-184">System-Only</span></span>            | <span data-ttu-id="717a6-185">否</span><span class="sxs-lookup"><span data-stu-id="717a6-185">False</span></span>                                            |
| <span data-ttu-id="717a6-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="717a6-186">Is-Single-Valued</span></span>       | <span data-ttu-id="717a6-187">對</span><span class="sxs-lookup"><span data-stu-id="717a6-187">True</span></span>                                             |
| <span data-ttu-id="717a6-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="717a6-188">Is Indexed</span></span>             | <span data-ttu-id="717a6-189">否</span><span class="sxs-lookup"><span data-stu-id="717a6-189">False</span></span>                                            |
| <span data-ttu-id="717a6-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="717a6-190">In Global Catalog</span></span>      | <span data-ttu-id="717a6-191">否</span><span class="sxs-lookup"><span data-stu-id="717a6-191">False</span></span>                                            |
| <span data-ttu-id="717a6-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="717a6-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="717a6-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="717a6-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="717a6-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="717a6-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="717a6-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="717a6-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="717a6-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-196">Search-Flags</span></span>           | <span data-ttu-id="717a6-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="717a6-197">0x00000000</span></span>                                       |
| <span data-ttu-id="717a6-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-198">System-Flags</span></span>           | <span data-ttu-id="717a6-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="717a6-199">0x00000010</span></span>                                       |
| <span data-ttu-id="717a6-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="717a6-200">Classes used in</span></span>        | [<span data-ttu-id="717a6-201">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="717a6-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="717a6-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="717a6-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="717a6-203">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-203">Entry</span></span> | <span data-ttu-id="717a6-204">值</span><span class="sxs-lookup"><span data-stu-id="717a6-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="717a6-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="717a6-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="717a6-207">System-Only</span></span>            | <span data-ttu-id="717a6-208">否</span><span class="sxs-lookup"><span data-stu-id="717a6-208">False</span></span>                                            |
| <span data-ttu-id="717a6-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="717a6-209">Is-Single-Valued</span></span>       | <span data-ttu-id="717a6-210">對</span><span class="sxs-lookup"><span data-stu-id="717a6-210">True</span></span>                                             |
| <span data-ttu-id="717a6-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="717a6-211">Is Indexed</span></span>             | <span data-ttu-id="717a6-212">否</span><span class="sxs-lookup"><span data-stu-id="717a6-212">False</span></span>                                            |
| <span data-ttu-id="717a6-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="717a6-213">In Global Catalog</span></span>      | <span data-ttu-id="717a6-214">否</span><span class="sxs-lookup"><span data-stu-id="717a6-214">False</span></span>                                            |
| <span data-ttu-id="717a6-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="717a6-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="717a6-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="717a6-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="717a6-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="717a6-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="717a6-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="717a6-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="717a6-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-219">Search-Flags</span></span>           | <span data-ttu-id="717a6-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="717a6-220">0x00000000</span></span>                                       |
| <span data-ttu-id="717a6-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-221">System-Flags</span></span>           | <span data-ttu-id="717a6-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="717a6-222">0x00000010</span></span>                                       |
| <span data-ttu-id="717a6-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="717a6-223">Classes used in</span></span>        | [<span data-ttu-id="717a6-224">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="717a6-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="717a6-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="717a6-225">Windows Server 2008</span></span>



| <span data-ttu-id="717a6-226">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-226">Entry</span></span> | <span data-ttu-id="717a6-227">值</span><span class="sxs-lookup"><span data-stu-id="717a6-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="717a6-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="717a6-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="717a6-230">System-Only</span></span>            | <span data-ttu-id="717a6-231">否</span><span class="sxs-lookup"><span data-stu-id="717a6-231">False</span></span>                                            |
| <span data-ttu-id="717a6-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="717a6-232">Is-Single-Valued</span></span>       | <span data-ttu-id="717a6-233">對</span><span class="sxs-lookup"><span data-stu-id="717a6-233">True</span></span>                                             |
| <span data-ttu-id="717a6-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="717a6-234">Is Indexed</span></span>             | <span data-ttu-id="717a6-235">否</span><span class="sxs-lookup"><span data-stu-id="717a6-235">False</span></span>                                            |
| <span data-ttu-id="717a6-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="717a6-236">In Global Catalog</span></span>      | <span data-ttu-id="717a6-237">否</span><span class="sxs-lookup"><span data-stu-id="717a6-237">False</span></span>                                            |
| <span data-ttu-id="717a6-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="717a6-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="717a6-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="717a6-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="717a6-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="717a6-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="717a6-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="717a6-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="717a6-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-242">Search-Flags</span></span>           | <span data-ttu-id="717a6-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="717a6-243">0x00000000</span></span>                                       |
| <span data-ttu-id="717a6-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-244">System-Flags</span></span>           | <span data-ttu-id="717a6-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="717a6-245">0x00000010</span></span>                                       |
| <span data-ttu-id="717a6-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="717a6-246">Classes used in</span></span>        | [<span data-ttu-id="717a6-247">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="717a6-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="717a6-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="717a6-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="717a6-249">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-249">Entry</span></span> | <span data-ttu-id="717a6-250">值</span><span class="sxs-lookup"><span data-stu-id="717a6-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="717a6-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="717a6-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="717a6-253">System-Only</span></span>            | <span data-ttu-id="717a6-254">否</span><span class="sxs-lookup"><span data-stu-id="717a6-254">False</span></span>                                            |
| <span data-ttu-id="717a6-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="717a6-255">Is-Single-Valued</span></span>       | <span data-ttu-id="717a6-256">對</span><span class="sxs-lookup"><span data-stu-id="717a6-256">True</span></span>                                             |
| <span data-ttu-id="717a6-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="717a6-257">Is Indexed</span></span>             | <span data-ttu-id="717a6-258">否</span><span class="sxs-lookup"><span data-stu-id="717a6-258">False</span></span>                                            |
| <span data-ttu-id="717a6-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="717a6-259">In Global Catalog</span></span>      | <span data-ttu-id="717a6-260">否</span><span class="sxs-lookup"><span data-stu-id="717a6-260">False</span></span>                                            |
| <span data-ttu-id="717a6-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="717a6-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="717a6-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="717a6-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="717a6-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="717a6-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="717a6-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="717a6-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="717a6-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-265">Search-Flags</span></span>           | <span data-ttu-id="717a6-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="717a6-266">0x00000000</span></span>                                       |
| <span data-ttu-id="717a6-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-267">System-Flags</span></span>           | <span data-ttu-id="717a6-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="717a6-268">0x00000010</span></span>                                       |
| <span data-ttu-id="717a6-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="717a6-269">Classes used in</span></span>        | [<span data-ttu-id="717a6-270">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="717a6-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="717a6-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="717a6-271">Windows Server 2012</span></span>



| <span data-ttu-id="717a6-272">進入</span><span class="sxs-lookup"><span data-stu-id="717a6-272">Entry</span></span> | <span data-ttu-id="717a6-273">值</span><span class="sxs-lookup"><span data-stu-id="717a6-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="717a6-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="717a6-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="717a6-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="717a6-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="717a6-276">System-Only</span></span>            | <span data-ttu-id="717a6-277">否</span><span class="sxs-lookup"><span data-stu-id="717a6-277">False</span></span>                                            |
| <span data-ttu-id="717a6-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="717a6-278">Is-Single-Valued</span></span>       | <span data-ttu-id="717a6-279">對</span><span class="sxs-lookup"><span data-stu-id="717a6-279">True</span></span>                                             |
| <span data-ttu-id="717a6-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="717a6-280">Is Indexed</span></span>             | <span data-ttu-id="717a6-281">否</span><span class="sxs-lookup"><span data-stu-id="717a6-281">False</span></span>                                            |
| <span data-ttu-id="717a6-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="717a6-282">In Global Catalog</span></span>      | <span data-ttu-id="717a6-283">否</span><span class="sxs-lookup"><span data-stu-id="717a6-283">False</span></span>                                            |
| <span data-ttu-id="717a6-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="717a6-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="717a6-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="717a6-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="717a6-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="717a6-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="717a6-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="717a6-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="717a6-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-288">Search-Flags</span></span>           | <span data-ttu-id="717a6-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="717a6-289">0x00000000</span></span>                                       |
| <span data-ttu-id="717a6-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="717a6-290">System-Flags</span></span>           | <span data-ttu-id="717a6-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="717a6-291">0x00000010</span></span>                                       |
| <span data-ttu-id="717a6-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="717a6-292">Classes used in</span></span>        | [<span data-ttu-id="717a6-293">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="717a6-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





