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
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="4ff9d-105">複寫-拓撲-持續執行屬性</span><span class="sxs-lookup"><span data-stu-id="4ff9d-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="4ff9d-106">刪除伺服器物件與從複寫拓撲中永久移除之間的延遲。</span><span class="sxs-lookup"><span data-stu-id="4ff9d-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="4ff9d-107">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-107">Entry</span></span> | <span data-ttu-id="4ff9d-108">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4ff9d-109">CN</span><span class="sxs-lookup"><span data-stu-id="4ff9d-109">CN</span></span>                | <span data-ttu-id="4ff9d-110">複寫-拓撲-持續執行</span><span class="sxs-lookup"><span data-stu-id="4ff9d-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="4ff9d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4ff9d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4ff9d-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="4ff9d-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="4ff9d-113">大小</span><span class="sxs-lookup"><span data-stu-id="4ff9d-113">Size</span></span>              | <span data-ttu-id="4ff9d-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="4ff9d-114">4 bytes</span></span>                              |
| <span data-ttu-id="4ff9d-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4ff9d-115">Update Privilege</span></span>  | <span data-ttu-id="4ff9d-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="4ff9d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="4ff9d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4ff9d-117">Update Frequency</span></span>  | <span data-ttu-id="4ff9d-118">每次刪除伺服器物件時。</span><span class="sxs-lookup"><span data-stu-id="4ff9d-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="4ff9d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-119">Attribute-Id</span></span>      | <span data-ttu-id="4ff9d-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="4ff9d-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="4ff9d-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4ff9d-121">System-Id-Guid</span></span>    | <span data-ttu-id="4ff9d-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4ff9d-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="4ff9d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ff9d-123">Syntax</span></span>            | [<span data-ttu-id="4ff9d-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="4ff9d-125">實作</span><span class="sxs-lookup"><span data-stu-id="4ff9d-125">Implementations</span></span>

-   [<span data-ttu-id="4ff9d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4ff9d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ff9d-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4ff9d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ff9d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ff9d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ff9d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4ff9d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ff9d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="4ff9d-134">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-134">Entry</span></span> | <span data-ttu-id="4ff9d-135">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4ff9d-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff9d-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ff9d-138">System-Only</span></span>            | <span data-ttu-id="4ff9d-139">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-139">False</span></span>                                            |
| <span data-ttu-id="4ff9d-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="4ff9d-141">對</span><span class="sxs-lookup"><span data-stu-id="4ff9d-141">True</span></span>                                             |
| <span data-ttu-id="4ff9d-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ff9d-142">Is Indexed</span></span>             | <span data-ttu-id="4ff9d-143">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-143">False</span></span>                                            |
| <span data-ttu-id="4ff9d-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ff9d-144">In Global Catalog</span></span>      | <span data-ttu-id="4ff9d-145">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-145">False</span></span>                                            |
| <span data-ttu-id="4ff9d-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ff9d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ff9d-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ff9d-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4ff9d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ff9d-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ff9d-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-150">Search-Flags</span></span>           | <span data-ttu-id="4ff9d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ff9d-151">0x00000000</span></span>                                       |
| <span data-ttu-id="4ff9d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-152">System-Flags</span></span>           | <span data-ttu-id="4ff9d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ff9d-153">0x00000010</span></span>                                       |
| <span data-ttu-id="4ff9d-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ff9d-154">Classes used in</span></span>        | [<span data-ttu-id="4ff9d-155">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4ff9d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ff9d-156">Windows Server 2003</span></span>



| <span data-ttu-id="4ff9d-157">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-157">Entry</span></span> | <span data-ttu-id="4ff9d-158">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4ff9d-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff9d-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ff9d-161">System-Only</span></span>            | <span data-ttu-id="4ff9d-162">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-162">False</span></span>                                            |
| <span data-ttu-id="4ff9d-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="4ff9d-164">對</span><span class="sxs-lookup"><span data-stu-id="4ff9d-164">True</span></span>                                             |
| <span data-ttu-id="4ff9d-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ff9d-165">Is Indexed</span></span>             | <span data-ttu-id="4ff9d-166">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-166">False</span></span>                                            |
| <span data-ttu-id="4ff9d-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ff9d-167">In Global Catalog</span></span>      | <span data-ttu-id="4ff9d-168">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-168">False</span></span>                                            |
| <span data-ttu-id="4ff9d-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ff9d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ff9d-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ff9d-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4ff9d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ff9d-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ff9d-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-173">Search-Flags</span></span>           | <span data-ttu-id="4ff9d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ff9d-174">0x00000000</span></span>                                       |
| <span data-ttu-id="4ff9d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-175">System-Flags</span></span>           | <span data-ttu-id="4ff9d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ff9d-176">0x00000010</span></span>                                       |
| <span data-ttu-id="4ff9d-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ff9d-177">Classes used in</span></span>        | [<span data-ttu-id="4ff9d-178">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4ff9d-179">亞當</span><span class="sxs-lookup"><span data-stu-id="4ff9d-179">ADAM</span></span>



| <span data-ttu-id="4ff9d-180">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-180">Entry</span></span> | <span data-ttu-id="4ff9d-181">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4ff9d-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff9d-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ff9d-184">System-Only</span></span>            | <span data-ttu-id="4ff9d-185">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-185">False</span></span>                                            |
| <span data-ttu-id="4ff9d-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4ff9d-187">對</span><span class="sxs-lookup"><span data-stu-id="4ff9d-187">True</span></span>                                             |
| <span data-ttu-id="4ff9d-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ff9d-188">Is Indexed</span></span>             | <span data-ttu-id="4ff9d-189">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-189">False</span></span>                                            |
| <span data-ttu-id="4ff9d-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ff9d-190">In Global Catalog</span></span>      | <span data-ttu-id="4ff9d-191">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-191">False</span></span>                                            |
| <span data-ttu-id="4ff9d-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ff9d-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ff9d-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ff9d-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4ff9d-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ff9d-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ff9d-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-196">Search-Flags</span></span>           | <span data-ttu-id="4ff9d-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ff9d-197">0x00000000</span></span>                                       |
| <span data-ttu-id="4ff9d-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-198">System-Flags</span></span>           | <span data-ttu-id="4ff9d-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ff9d-199">0x00000010</span></span>                                       |
| <span data-ttu-id="4ff9d-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ff9d-200">Classes used in</span></span>        | [<span data-ttu-id="4ff9d-201">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ff9d-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ff9d-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ff9d-203">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-203">Entry</span></span> | <span data-ttu-id="4ff9d-204">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4ff9d-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff9d-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ff9d-207">System-Only</span></span>            | <span data-ttu-id="4ff9d-208">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-208">False</span></span>                                            |
| <span data-ttu-id="4ff9d-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-209">Is-Single-Valued</span></span>       | <span data-ttu-id="4ff9d-210">對</span><span class="sxs-lookup"><span data-stu-id="4ff9d-210">True</span></span>                                             |
| <span data-ttu-id="4ff9d-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ff9d-211">Is Indexed</span></span>             | <span data-ttu-id="4ff9d-212">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-212">False</span></span>                                            |
| <span data-ttu-id="4ff9d-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ff9d-213">In Global Catalog</span></span>      | <span data-ttu-id="4ff9d-214">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-214">False</span></span>                                            |
| <span data-ttu-id="4ff9d-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ff9d-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ff9d-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ff9d-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4ff9d-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ff9d-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ff9d-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-219">Search-Flags</span></span>           | <span data-ttu-id="4ff9d-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ff9d-220">0x00000000</span></span>                                       |
| <span data-ttu-id="4ff9d-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-221">System-Flags</span></span>           | <span data-ttu-id="4ff9d-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ff9d-222">0x00000010</span></span>                                       |
| <span data-ttu-id="4ff9d-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ff9d-223">Classes used in</span></span>        | [<span data-ttu-id="4ff9d-224">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4ff9d-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ff9d-225">Windows Server 2008</span></span>



| <span data-ttu-id="4ff9d-226">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-226">Entry</span></span> | <span data-ttu-id="4ff9d-227">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4ff9d-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff9d-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ff9d-230">System-Only</span></span>            | <span data-ttu-id="4ff9d-231">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-231">False</span></span>                                            |
| <span data-ttu-id="4ff9d-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-232">Is-Single-Valued</span></span>       | <span data-ttu-id="4ff9d-233">對</span><span class="sxs-lookup"><span data-stu-id="4ff9d-233">True</span></span>                                             |
| <span data-ttu-id="4ff9d-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ff9d-234">Is Indexed</span></span>             | <span data-ttu-id="4ff9d-235">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-235">False</span></span>                                            |
| <span data-ttu-id="4ff9d-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ff9d-236">In Global Catalog</span></span>      | <span data-ttu-id="4ff9d-237">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-237">False</span></span>                                            |
| <span data-ttu-id="4ff9d-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ff9d-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ff9d-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ff9d-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4ff9d-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ff9d-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ff9d-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-242">Search-Flags</span></span>           | <span data-ttu-id="4ff9d-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ff9d-243">0x00000000</span></span>                                       |
| <span data-ttu-id="4ff9d-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-244">System-Flags</span></span>           | <span data-ttu-id="4ff9d-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ff9d-245">0x00000010</span></span>                                       |
| <span data-ttu-id="4ff9d-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ff9d-246">Classes used in</span></span>        | [<span data-ttu-id="4ff9d-247">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ff9d-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ff9d-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ff9d-249">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-249">Entry</span></span> | <span data-ttu-id="4ff9d-250">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4ff9d-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff9d-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ff9d-253">System-Only</span></span>            | <span data-ttu-id="4ff9d-254">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-254">False</span></span>                                            |
| <span data-ttu-id="4ff9d-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-255">Is-Single-Valued</span></span>       | <span data-ttu-id="4ff9d-256">對</span><span class="sxs-lookup"><span data-stu-id="4ff9d-256">True</span></span>                                             |
| <span data-ttu-id="4ff9d-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ff9d-257">Is Indexed</span></span>             | <span data-ttu-id="4ff9d-258">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-258">False</span></span>                                            |
| <span data-ttu-id="4ff9d-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ff9d-259">In Global Catalog</span></span>      | <span data-ttu-id="4ff9d-260">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-260">False</span></span>                                            |
| <span data-ttu-id="4ff9d-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ff9d-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ff9d-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ff9d-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4ff9d-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ff9d-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ff9d-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-265">Search-Flags</span></span>           | <span data-ttu-id="4ff9d-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ff9d-266">0x00000000</span></span>                                       |
| <span data-ttu-id="4ff9d-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-267">System-Flags</span></span>           | <span data-ttu-id="4ff9d-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ff9d-268">0x00000010</span></span>                                       |
| <span data-ttu-id="4ff9d-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ff9d-269">Classes used in</span></span>        | [<span data-ttu-id="4ff9d-270">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4ff9d-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ff9d-271">Windows Server 2012</span></span>



| <span data-ttu-id="4ff9d-272">進入</span><span class="sxs-lookup"><span data-stu-id="4ff9d-272">Entry</span></span> | <span data-ttu-id="4ff9d-273">值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="4ff9d-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff9d-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ff9d-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="4ff9d-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ff9d-276">System-Only</span></span>            | <span data-ttu-id="4ff9d-277">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-277">False</span></span>                                            |
| <span data-ttu-id="4ff9d-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4ff9d-278">Is-Single-Valued</span></span>       | <span data-ttu-id="4ff9d-279">對</span><span class="sxs-lookup"><span data-stu-id="4ff9d-279">True</span></span>                                             |
| <span data-ttu-id="4ff9d-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4ff9d-280">Is Indexed</span></span>             | <span data-ttu-id="4ff9d-281">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-281">False</span></span>                                            |
| <span data-ttu-id="4ff9d-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4ff9d-282">In Global Catalog</span></span>      | <span data-ttu-id="4ff9d-283">否</span><span class="sxs-lookup"><span data-stu-id="4ff9d-283">False</span></span>                                            |
| <span data-ttu-id="4ff9d-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4ff9d-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ff9d-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4ff9d-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="4ff9d-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ff9d-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ff9d-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="4ff9d-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-288">Search-Flags</span></span>           | <span data-ttu-id="4ff9d-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ff9d-289">0x00000000</span></span>                                       |
| <span data-ttu-id="4ff9d-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ff9d-290">System-Flags</span></span>           | <span data-ttu-id="4ff9d-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ff9d-291">0x00000010</span></span>                                       |
| <span data-ttu-id="4ff9d-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4ff9d-292">Classes used in</span></span>        | [<span data-ttu-id="4ff9d-293">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="4ff9d-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





