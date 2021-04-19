---
title: UpToDate-Vector 屬性
description: 追蹤整個 NC 的內部複寫狀態資訊。 您可以透過 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。 存在於所有 NC 根物件上。
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- 複寫-UpToDate-向量屬性 AD 架構
- replUpToDateVector 屬性 AD 架構
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972720"
---
# <a name="repl-uptodate-vector-attribute"></a><span data-ttu-id="00d20-107">UpToDate-Vector 屬性</span><span class="sxs-lookup"><span data-stu-id="00d20-107">Repl-UpToDate-Vector attribute</span></span>

<span data-ttu-id="00d20-108">追蹤整個 NC 的內部複寫狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="00d20-108">Tracks internal replication state information for an entire NC.</span></span> <span data-ttu-id="00d20-109">您可以透過 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。</span><span class="sxs-lookup"><span data-stu-id="00d20-109">Information here can be extracted in public form through the API DsReplicaGetInfo().</span></span> <span data-ttu-id="00d20-110">存在於所有 NC 根物件上。</span><span class="sxs-lookup"><span data-stu-id="00d20-110">Present on all NC root objects.</span></span>



| <span data-ttu-id="00d20-111">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-111">Entry</span></span> | <span data-ttu-id="00d20-112">值</span><span class="sxs-lookup"><span data-stu-id="00d20-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="00d20-113">CN</span><span class="sxs-lookup"><span data-stu-id="00d20-113">CN</span></span>                | <span data-ttu-id="00d20-114">複寫-UpToDate-向量</span><span class="sxs-lookup"><span data-stu-id="00d20-114">Repl-UpToDate-Vector</span></span>                                                           |
| <span data-ttu-id="00d20-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="00d20-115">Ldap-Display-Name</span></span> | <span data-ttu-id="00d20-116">replUpToDateVector</span><span class="sxs-lookup"><span data-stu-id="00d20-116">replUpToDateVector</span></span>                                                             |
| <span data-ttu-id="00d20-117">大小</span><span class="sxs-lookup"><span data-stu-id="00d20-117">Size</span></span>              | <span data-ttu-id="00d20-118">長度與 NC 的 (過去和目前) 的複本數目成正比。</span><span class="sxs-lookup"><span data-stu-id="00d20-118">Length is proportional to the number of replicas (past and present) of the NC.</span></span> |
| <span data-ttu-id="00d20-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="00d20-119">Update Privilege</span></span>  | <span data-ttu-id="00d20-120">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="00d20-120">This value is set by the system.</span></span>                                               |
| <span data-ttu-id="00d20-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="00d20-121">Update Frequency</span></span>  | <span data-ttu-id="00d20-122">回應已完成的輸入複寫週期的變更。</span><span class="sxs-lookup"><span data-stu-id="00d20-122">Changes in response to completed inbound replication cycles.</span></span>                   |
| <span data-ttu-id="00d20-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-123">Attribute-Id</span></span>      | <span data-ttu-id="00d20-124">1.2.840.113556.1.4.4</span><span class="sxs-lookup"><span data-stu-id="00d20-124">1.2.840.113556.1.4.4</span></span>                                                           |
| <span data-ttu-id="00d20-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="00d20-125">System-Id-Guid</span></span>    | <span data-ttu-id="00d20-126">bf967a16-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="00d20-126">bf967a16-0de6-11d0-a285-00aa003049e2</span></span>                                           |
| <span data-ttu-id="00d20-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="00d20-127">Syntax</span></span>            | [<span data-ttu-id="00d20-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="00d20-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                          |



## <a name="implementations"></a><span data-ttu-id="00d20-129">實作</span><span class="sxs-lookup"><span data-stu-id="00d20-129">Implementations</span></span>

-   [<span data-ttu-id="00d20-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="00d20-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="00d20-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00d20-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00d20-132">**亞當**</span><span class="sxs-lookup"><span data-stu-id="00d20-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="00d20-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00d20-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00d20-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00d20-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00d20-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00d20-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00d20-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00d20-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="00d20-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00d20-137">Windows 2000 Server</span></span>



| <span data-ttu-id="00d20-138">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-138">Entry</span></span> | <span data-ttu-id="00d20-139">值</span><span class="sxs-lookup"><span data-stu-id="00d20-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00d20-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00d20-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d20-142">System-Only</span></span>            | <span data-ttu-id="00d20-143">對</span><span class="sxs-lookup"><span data-stu-id="00d20-143">True</span></span>                            |
| <span data-ttu-id="00d20-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00d20-144">Is-Single-Valued</span></span>       | <span data-ttu-id="00d20-145">對</span><span class="sxs-lookup"><span data-stu-id="00d20-145">True</span></span>                            |
| <span data-ttu-id="00d20-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00d20-146">Is Indexed</span></span>             | <span data-ttu-id="00d20-147">否</span><span class="sxs-lookup"><span data-stu-id="00d20-147">False</span></span>                           |
| <span data-ttu-id="00d20-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00d20-148">In Global Catalog</span></span>      | <span data-ttu-id="00d20-149">對</span><span class="sxs-lookup"><span data-stu-id="00d20-149">True</span></span>                            |
| <span data-ttu-id="00d20-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00d20-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d20-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00d20-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00d20-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d20-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00d20-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d20-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00d20-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-154">Search-Flags</span></span>           | <span data-ttu-id="00d20-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d20-155">0x00000000</span></span>                      |
| <span data-ttu-id="00d20-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-156">System-Flags</span></span>           | <span data-ttu-id="00d20-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="00d20-157">0x00000013</span></span>                      |
| <span data-ttu-id="00d20-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00d20-158">Classes used in</span></span>        | [<span data-ttu-id="00d20-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00d20-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="00d20-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00d20-160">Windows Server 2003</span></span>



| <span data-ttu-id="00d20-161">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-161">Entry</span></span> | <span data-ttu-id="00d20-162">值</span><span class="sxs-lookup"><span data-stu-id="00d20-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00d20-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00d20-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d20-165">System-Only</span></span>            | <span data-ttu-id="00d20-166">對</span><span class="sxs-lookup"><span data-stu-id="00d20-166">True</span></span>                            |
| <span data-ttu-id="00d20-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00d20-167">Is-Single-Valued</span></span>       | <span data-ttu-id="00d20-168">對</span><span class="sxs-lookup"><span data-stu-id="00d20-168">True</span></span>                            |
| <span data-ttu-id="00d20-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00d20-169">Is Indexed</span></span>             | <span data-ttu-id="00d20-170">否</span><span class="sxs-lookup"><span data-stu-id="00d20-170">False</span></span>                           |
| <span data-ttu-id="00d20-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00d20-171">In Global Catalog</span></span>      | <span data-ttu-id="00d20-172">對</span><span class="sxs-lookup"><span data-stu-id="00d20-172">True</span></span>                            |
| <span data-ttu-id="00d20-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00d20-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d20-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00d20-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00d20-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d20-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00d20-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d20-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00d20-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-177">Search-Flags</span></span>           | <span data-ttu-id="00d20-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d20-178">0x00000000</span></span>                      |
| <span data-ttu-id="00d20-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-179">System-Flags</span></span>           | <span data-ttu-id="00d20-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="00d20-180">0x00000013</span></span>                      |
| <span data-ttu-id="00d20-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00d20-181">Classes used in</span></span>        | [<span data-ttu-id="00d20-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00d20-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="00d20-183">亞當</span><span class="sxs-lookup"><span data-stu-id="00d20-183">ADAM</span></span>



| <span data-ttu-id="00d20-184">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-184">Entry</span></span> | <span data-ttu-id="00d20-185">值</span><span class="sxs-lookup"><span data-stu-id="00d20-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00d20-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00d20-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d20-188">System-Only</span></span>            | <span data-ttu-id="00d20-189">對</span><span class="sxs-lookup"><span data-stu-id="00d20-189">True</span></span>                            |
| <span data-ttu-id="00d20-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00d20-190">Is-Single-Valued</span></span>       | <span data-ttu-id="00d20-191">對</span><span class="sxs-lookup"><span data-stu-id="00d20-191">True</span></span>                            |
| <span data-ttu-id="00d20-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00d20-192">Is Indexed</span></span>             | <span data-ttu-id="00d20-193">否</span><span class="sxs-lookup"><span data-stu-id="00d20-193">False</span></span>                           |
| <span data-ttu-id="00d20-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00d20-194">In Global Catalog</span></span>      | <span data-ttu-id="00d20-195">對</span><span class="sxs-lookup"><span data-stu-id="00d20-195">True</span></span>                            |
| <span data-ttu-id="00d20-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00d20-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d20-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00d20-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00d20-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d20-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00d20-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d20-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00d20-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-200">Search-Flags</span></span>           | <span data-ttu-id="00d20-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d20-201">0x00000000</span></span>                      |
| <span data-ttu-id="00d20-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-202">System-Flags</span></span>           | <span data-ttu-id="00d20-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="00d20-203">0x00000013</span></span>                      |
| <span data-ttu-id="00d20-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00d20-204">Classes used in</span></span>        | [<span data-ttu-id="00d20-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00d20-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00d20-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00d20-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00d20-207">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-207">Entry</span></span> | <span data-ttu-id="00d20-208">值</span><span class="sxs-lookup"><span data-stu-id="00d20-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00d20-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00d20-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d20-211">System-Only</span></span>            | <span data-ttu-id="00d20-212">對</span><span class="sxs-lookup"><span data-stu-id="00d20-212">True</span></span>                            |
| <span data-ttu-id="00d20-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00d20-213">Is-Single-Valued</span></span>       | <span data-ttu-id="00d20-214">對</span><span class="sxs-lookup"><span data-stu-id="00d20-214">True</span></span>                            |
| <span data-ttu-id="00d20-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00d20-215">Is Indexed</span></span>             | <span data-ttu-id="00d20-216">否</span><span class="sxs-lookup"><span data-stu-id="00d20-216">False</span></span>                           |
| <span data-ttu-id="00d20-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00d20-217">In Global Catalog</span></span>      | <span data-ttu-id="00d20-218">對</span><span class="sxs-lookup"><span data-stu-id="00d20-218">True</span></span>                            |
| <span data-ttu-id="00d20-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00d20-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d20-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00d20-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00d20-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d20-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00d20-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d20-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00d20-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-223">Search-Flags</span></span>           | <span data-ttu-id="00d20-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d20-224">0x00000000</span></span>                      |
| <span data-ttu-id="00d20-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-225">System-Flags</span></span>           | <span data-ttu-id="00d20-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="00d20-226">0x00000013</span></span>                      |
| <span data-ttu-id="00d20-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00d20-227">Classes used in</span></span>        | [<span data-ttu-id="00d20-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00d20-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00d20-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00d20-229">Windows Server 2008</span></span>



| <span data-ttu-id="00d20-230">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-230">Entry</span></span> | <span data-ttu-id="00d20-231">值</span><span class="sxs-lookup"><span data-stu-id="00d20-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00d20-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00d20-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d20-234">System-Only</span></span>            | <span data-ttu-id="00d20-235">對</span><span class="sxs-lookup"><span data-stu-id="00d20-235">True</span></span>                            |
| <span data-ttu-id="00d20-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00d20-236">Is-Single-Valued</span></span>       | <span data-ttu-id="00d20-237">對</span><span class="sxs-lookup"><span data-stu-id="00d20-237">True</span></span>                            |
| <span data-ttu-id="00d20-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00d20-238">Is Indexed</span></span>             | <span data-ttu-id="00d20-239">否</span><span class="sxs-lookup"><span data-stu-id="00d20-239">False</span></span>                           |
| <span data-ttu-id="00d20-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00d20-240">In Global Catalog</span></span>      | <span data-ttu-id="00d20-241">對</span><span class="sxs-lookup"><span data-stu-id="00d20-241">True</span></span>                            |
| <span data-ttu-id="00d20-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00d20-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d20-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00d20-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00d20-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d20-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00d20-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d20-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00d20-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-246">Search-Flags</span></span>           | <span data-ttu-id="00d20-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d20-247">0x00000000</span></span>                      |
| <span data-ttu-id="00d20-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-248">System-Flags</span></span>           | <span data-ttu-id="00d20-249">0x00000013</span><span class="sxs-lookup"><span data-stu-id="00d20-249">0x00000013</span></span>                      |
| <span data-ttu-id="00d20-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00d20-250">Classes used in</span></span>        | [<span data-ttu-id="00d20-251">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00d20-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00d20-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00d20-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00d20-253">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-253">Entry</span></span> | <span data-ttu-id="00d20-254">值</span><span class="sxs-lookup"><span data-stu-id="00d20-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00d20-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00d20-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d20-257">System-Only</span></span>            | <span data-ttu-id="00d20-258">對</span><span class="sxs-lookup"><span data-stu-id="00d20-258">True</span></span>                            |
| <span data-ttu-id="00d20-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00d20-259">Is-Single-Valued</span></span>       | <span data-ttu-id="00d20-260">對</span><span class="sxs-lookup"><span data-stu-id="00d20-260">True</span></span>                            |
| <span data-ttu-id="00d20-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00d20-261">Is Indexed</span></span>             | <span data-ttu-id="00d20-262">否</span><span class="sxs-lookup"><span data-stu-id="00d20-262">False</span></span>                           |
| <span data-ttu-id="00d20-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00d20-263">In Global Catalog</span></span>      | <span data-ttu-id="00d20-264">對</span><span class="sxs-lookup"><span data-stu-id="00d20-264">True</span></span>                            |
| <span data-ttu-id="00d20-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00d20-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d20-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00d20-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00d20-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d20-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00d20-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d20-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00d20-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-269">Search-Flags</span></span>           | <span data-ttu-id="00d20-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d20-270">0x00000000</span></span>                      |
| <span data-ttu-id="00d20-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-271">System-Flags</span></span>           | <span data-ttu-id="00d20-272">0x00000013</span><span class="sxs-lookup"><span data-stu-id="00d20-272">0x00000013</span></span>                      |
| <span data-ttu-id="00d20-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00d20-273">Classes used in</span></span>        | [<span data-ttu-id="00d20-274">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00d20-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00d20-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00d20-275">Windows Server 2012</span></span>



| <span data-ttu-id="00d20-276">進入</span><span class="sxs-lookup"><span data-stu-id="00d20-276">Entry</span></span> | <span data-ttu-id="00d20-277">值</span><span class="sxs-lookup"><span data-stu-id="00d20-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="00d20-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="00d20-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d20-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="00d20-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d20-280">System-Only</span></span>            | <span data-ttu-id="00d20-281">對</span><span class="sxs-lookup"><span data-stu-id="00d20-281">True</span></span>                            |
| <span data-ttu-id="00d20-282">是-單一值</span><span class="sxs-lookup"><span data-stu-id="00d20-282">Is-Single-Valued</span></span>       | <span data-ttu-id="00d20-283">對</span><span class="sxs-lookup"><span data-stu-id="00d20-283">True</span></span>                            |
| <span data-ttu-id="00d20-284">已編制索引</span><span class="sxs-lookup"><span data-stu-id="00d20-284">Is Indexed</span></span>             | <span data-ttu-id="00d20-285">否</span><span class="sxs-lookup"><span data-stu-id="00d20-285">False</span></span>                           |
| <span data-ttu-id="00d20-286">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="00d20-286">In Global Catalog</span></span>      | <span data-ttu-id="00d20-287">對</span><span class="sxs-lookup"><span data-stu-id="00d20-287">True</span></span>                            |
| <span data-ttu-id="00d20-288">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="00d20-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d20-289">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="00d20-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="00d20-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d20-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="00d20-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d20-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="00d20-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-292">Search-Flags</span></span>           | <span data-ttu-id="00d20-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d20-293">0x00000000</span></span>                      |
| <span data-ttu-id="00d20-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d20-294">System-Flags</span></span>           | <span data-ttu-id="00d20-295">0x00000013</span><span class="sxs-lookup"><span data-stu-id="00d20-295">0x00000013</span></span>                      |
| <span data-ttu-id="00d20-296">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="00d20-296">Classes used in</span></span>        | [<span data-ttu-id="00d20-297">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="00d20-297">**Top**</span></span>](c-top.md)<br/> |



 

 





