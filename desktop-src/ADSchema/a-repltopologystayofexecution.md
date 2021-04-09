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
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="3b1fd-105">複寫-拓撲-持續執行屬性</span><span class="sxs-lookup"><span data-stu-id="3b1fd-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="3b1fd-106">刪除伺服器物件與從複寫拓撲中永久移除之間的延遲。</span><span class="sxs-lookup"><span data-stu-id="3b1fd-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="3b1fd-107">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-107">Entry</span></span> | <span data-ttu-id="3b1fd-108">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3b1fd-109">CN</span><span class="sxs-lookup"><span data-stu-id="3b1fd-109">CN</span></span>                | <span data-ttu-id="3b1fd-110">複寫-拓撲-持續執行</span><span class="sxs-lookup"><span data-stu-id="3b1fd-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="3b1fd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3b1fd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3b1fd-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="3b1fd-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="3b1fd-113">大小</span><span class="sxs-lookup"><span data-stu-id="3b1fd-113">Size</span></span>              | <span data-ttu-id="3b1fd-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="3b1fd-114">4 bytes</span></span>                              |
| <span data-ttu-id="3b1fd-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3b1fd-115">Update Privilege</span></span>  | <span data-ttu-id="3b1fd-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="3b1fd-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="3b1fd-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3b1fd-117">Update Frequency</span></span>  | <span data-ttu-id="3b1fd-118">每次刪除伺服器物件時。</span><span class="sxs-lookup"><span data-stu-id="3b1fd-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="3b1fd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-119">Attribute-Id</span></span>      | <span data-ttu-id="3b1fd-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="3b1fd-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="3b1fd-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3b1fd-121">System-Id-Guid</span></span>    | <span data-ttu-id="3b1fd-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3b1fd-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="3b1fd-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b1fd-123">Syntax</span></span>            | [<span data-ttu-id="3b1fd-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3b1fd-125">實作</span><span class="sxs-lookup"><span data-stu-id="3b1fd-125">Implementations</span></span>

-   [<span data-ttu-id="3b1fd-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3b1fd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3b1fd-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3b1fd-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3b1fd-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3b1fd-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3b1fd-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3b1fd-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b1fd-133">Windows 2000 Server</span></span>



| <span data-ttu-id="3b1fd-134">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-134">Entry</span></span> | <span data-ttu-id="3b1fd-135">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b1fd-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3b1fd-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b1fd-138">System-Only</span></span>            | <span data-ttu-id="3b1fd-139">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-139">False</span></span>                                            |
| <span data-ttu-id="3b1fd-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3b1fd-141">對</span><span class="sxs-lookup"><span data-stu-id="3b1fd-141">True</span></span>                                             |
| <span data-ttu-id="3b1fd-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3b1fd-142">Is Indexed</span></span>             | <span data-ttu-id="3b1fd-143">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-143">False</span></span>                                            |
| <span data-ttu-id="3b1fd-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3b1fd-144">In Global Catalog</span></span>      | <span data-ttu-id="3b1fd-145">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-145">False</span></span>                                            |
| <span data-ttu-id="3b1fd-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3b1fd-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b1fd-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3b1fd-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b1fd-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b1fd-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b1fd-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-150">Search-Flags</span></span>           | <span data-ttu-id="3b1fd-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b1fd-151">0x00000000</span></span>                                       |
| <span data-ttu-id="3b1fd-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-152">System-Flags</span></span>           | <span data-ttu-id="3b1fd-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b1fd-153">0x00000010</span></span>                                       |
| <span data-ttu-id="3b1fd-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3b1fd-154">Classes used in</span></span>        | [<span data-ttu-id="3b1fd-155">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3b1fd-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b1fd-156">Windows Server 2003</span></span>



| <span data-ttu-id="3b1fd-157">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-157">Entry</span></span> | <span data-ttu-id="3b1fd-158">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b1fd-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3b1fd-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b1fd-161">System-Only</span></span>            | <span data-ttu-id="3b1fd-162">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-162">False</span></span>                                            |
| <span data-ttu-id="3b1fd-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3b1fd-164">對</span><span class="sxs-lookup"><span data-stu-id="3b1fd-164">True</span></span>                                             |
| <span data-ttu-id="3b1fd-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3b1fd-165">Is Indexed</span></span>             | <span data-ttu-id="3b1fd-166">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-166">False</span></span>                                            |
| <span data-ttu-id="3b1fd-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3b1fd-167">In Global Catalog</span></span>      | <span data-ttu-id="3b1fd-168">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-168">False</span></span>                                            |
| <span data-ttu-id="3b1fd-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3b1fd-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b1fd-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3b1fd-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b1fd-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b1fd-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b1fd-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-173">Search-Flags</span></span>           | <span data-ttu-id="3b1fd-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b1fd-174">0x00000000</span></span>                                       |
| <span data-ttu-id="3b1fd-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-175">System-Flags</span></span>           | <span data-ttu-id="3b1fd-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b1fd-176">0x00000010</span></span>                                       |
| <span data-ttu-id="3b1fd-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3b1fd-177">Classes used in</span></span>        | [<span data-ttu-id="3b1fd-178">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3b1fd-179">亞當</span><span class="sxs-lookup"><span data-stu-id="3b1fd-179">ADAM</span></span>



| <span data-ttu-id="3b1fd-180">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-180">Entry</span></span> | <span data-ttu-id="3b1fd-181">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b1fd-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3b1fd-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b1fd-184">System-Only</span></span>            | <span data-ttu-id="3b1fd-185">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-185">False</span></span>                                            |
| <span data-ttu-id="3b1fd-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-186">Is-Single-Valued</span></span>       | <span data-ttu-id="3b1fd-187">對</span><span class="sxs-lookup"><span data-stu-id="3b1fd-187">True</span></span>                                             |
| <span data-ttu-id="3b1fd-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3b1fd-188">Is Indexed</span></span>             | <span data-ttu-id="3b1fd-189">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-189">False</span></span>                                            |
| <span data-ttu-id="3b1fd-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3b1fd-190">In Global Catalog</span></span>      | <span data-ttu-id="3b1fd-191">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-191">False</span></span>                                            |
| <span data-ttu-id="3b1fd-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3b1fd-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b1fd-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3b1fd-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b1fd-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b1fd-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b1fd-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-196">Search-Flags</span></span>           | <span data-ttu-id="3b1fd-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b1fd-197">0x00000000</span></span>                                       |
| <span data-ttu-id="3b1fd-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-198">System-Flags</span></span>           | <span data-ttu-id="3b1fd-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b1fd-199">0x00000010</span></span>                                       |
| <span data-ttu-id="3b1fd-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3b1fd-200">Classes used in</span></span>        | [<span data-ttu-id="3b1fd-201">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3b1fd-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3b1fd-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3b1fd-203">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-203">Entry</span></span> | <span data-ttu-id="3b1fd-204">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b1fd-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3b1fd-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b1fd-207">System-Only</span></span>            | <span data-ttu-id="3b1fd-208">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-208">False</span></span>                                            |
| <span data-ttu-id="3b1fd-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-209">Is-Single-Valued</span></span>       | <span data-ttu-id="3b1fd-210">對</span><span class="sxs-lookup"><span data-stu-id="3b1fd-210">True</span></span>                                             |
| <span data-ttu-id="3b1fd-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3b1fd-211">Is Indexed</span></span>             | <span data-ttu-id="3b1fd-212">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-212">False</span></span>                                            |
| <span data-ttu-id="3b1fd-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3b1fd-213">In Global Catalog</span></span>      | <span data-ttu-id="3b1fd-214">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-214">False</span></span>                                            |
| <span data-ttu-id="3b1fd-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3b1fd-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b1fd-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3b1fd-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b1fd-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b1fd-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b1fd-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-219">Search-Flags</span></span>           | <span data-ttu-id="3b1fd-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b1fd-220">0x00000000</span></span>                                       |
| <span data-ttu-id="3b1fd-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-221">System-Flags</span></span>           | <span data-ttu-id="3b1fd-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b1fd-222">0x00000010</span></span>                                       |
| <span data-ttu-id="3b1fd-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3b1fd-223">Classes used in</span></span>        | [<span data-ttu-id="3b1fd-224">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3b1fd-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b1fd-225">Windows Server 2008</span></span>



| <span data-ttu-id="3b1fd-226">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-226">Entry</span></span> | <span data-ttu-id="3b1fd-227">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b1fd-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3b1fd-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b1fd-230">System-Only</span></span>            | <span data-ttu-id="3b1fd-231">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-231">False</span></span>                                            |
| <span data-ttu-id="3b1fd-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-232">Is-Single-Valued</span></span>       | <span data-ttu-id="3b1fd-233">對</span><span class="sxs-lookup"><span data-stu-id="3b1fd-233">True</span></span>                                             |
| <span data-ttu-id="3b1fd-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3b1fd-234">Is Indexed</span></span>             | <span data-ttu-id="3b1fd-235">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-235">False</span></span>                                            |
| <span data-ttu-id="3b1fd-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3b1fd-236">In Global Catalog</span></span>      | <span data-ttu-id="3b1fd-237">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-237">False</span></span>                                            |
| <span data-ttu-id="3b1fd-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3b1fd-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b1fd-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3b1fd-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b1fd-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b1fd-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b1fd-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-242">Search-Flags</span></span>           | <span data-ttu-id="3b1fd-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b1fd-243">0x00000000</span></span>                                       |
| <span data-ttu-id="3b1fd-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-244">System-Flags</span></span>           | <span data-ttu-id="3b1fd-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b1fd-245">0x00000010</span></span>                                       |
| <span data-ttu-id="3b1fd-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3b1fd-246">Classes used in</span></span>        | [<span data-ttu-id="3b1fd-247">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3b1fd-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3b1fd-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3b1fd-249">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-249">Entry</span></span> | <span data-ttu-id="3b1fd-250">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b1fd-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3b1fd-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b1fd-253">System-Only</span></span>            | <span data-ttu-id="3b1fd-254">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-254">False</span></span>                                            |
| <span data-ttu-id="3b1fd-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-255">Is-Single-Valued</span></span>       | <span data-ttu-id="3b1fd-256">對</span><span class="sxs-lookup"><span data-stu-id="3b1fd-256">True</span></span>                                             |
| <span data-ttu-id="3b1fd-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3b1fd-257">Is Indexed</span></span>             | <span data-ttu-id="3b1fd-258">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-258">False</span></span>                                            |
| <span data-ttu-id="3b1fd-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3b1fd-259">In Global Catalog</span></span>      | <span data-ttu-id="3b1fd-260">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-260">False</span></span>                                            |
| <span data-ttu-id="3b1fd-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3b1fd-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b1fd-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3b1fd-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b1fd-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b1fd-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b1fd-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-265">Search-Flags</span></span>           | <span data-ttu-id="3b1fd-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b1fd-266">0x00000000</span></span>                                       |
| <span data-ttu-id="3b1fd-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-267">System-Flags</span></span>           | <span data-ttu-id="3b1fd-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b1fd-268">0x00000010</span></span>                                       |
| <span data-ttu-id="3b1fd-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3b1fd-269">Classes used in</span></span>        | [<span data-ttu-id="3b1fd-270">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3b1fd-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b1fd-271">Windows Server 2012</span></span>



| <span data-ttu-id="3b1fd-272">進入</span><span class="sxs-lookup"><span data-stu-id="3b1fd-272">Entry</span></span> | <span data-ttu-id="3b1fd-273">值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="3b1fd-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3b1fd-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3b1fd-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="3b1fd-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="3b1fd-276">System-Only</span></span>            | <span data-ttu-id="3b1fd-277">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-277">False</span></span>                                            |
| <span data-ttu-id="3b1fd-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3b1fd-278">Is-Single-Valued</span></span>       | <span data-ttu-id="3b1fd-279">對</span><span class="sxs-lookup"><span data-stu-id="3b1fd-279">True</span></span>                                             |
| <span data-ttu-id="3b1fd-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3b1fd-280">Is Indexed</span></span>             | <span data-ttu-id="3b1fd-281">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-281">False</span></span>                                            |
| <span data-ttu-id="3b1fd-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3b1fd-282">In Global Catalog</span></span>      | <span data-ttu-id="3b1fd-283">否</span><span class="sxs-lookup"><span data-stu-id="3b1fd-283">False</span></span>                                            |
| <span data-ttu-id="3b1fd-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3b1fd-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="3b1fd-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3b1fd-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="3b1fd-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3b1fd-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3b1fd-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="3b1fd-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-288">Search-Flags</span></span>           | <span data-ttu-id="3b1fd-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3b1fd-289">0x00000000</span></span>                                       |
| <span data-ttu-id="3b1fd-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3b1fd-290">System-Flags</span></span>           | <span data-ttu-id="3b1fd-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3b1fd-291">0x00000010</span></span>                                       |
| <span data-ttu-id="3b1fd-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3b1fd-292">Classes used in</span></span>        | [<span data-ttu-id="3b1fd-293">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="3b1fd-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





