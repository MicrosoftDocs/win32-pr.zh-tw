---
title: 複寫-屬性中繼資料屬性
description: 追蹤 DS 物件的內部複寫狀態資訊。 您可以透過公用 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。 存在於所有 DS 物件上。
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- 複寫-屬性-中繼資料屬性 AD 架構
- replPropertyMetaData 屬性 AD 架構
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7639d9bca600457d519862e1f57d9ee698d2a155
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687131"
---
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="c729c-107">複寫-屬性中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="c729c-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="c729c-108">追蹤 DS 物件的內部複寫狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="c729c-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="c729c-109">您可以透過公用 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。</span><span class="sxs-lookup"><span data-stu-id="c729c-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="c729c-110">存在於所有 DS 物件上。</span><span class="sxs-lookup"><span data-stu-id="c729c-110">Present on all DS objects.</span></span>



| <span data-ttu-id="c729c-111">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-111">Entry</span></span> | <span data-ttu-id="c729c-112">值</span><span class="sxs-lookup"><span data-stu-id="c729c-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c729c-113">CN</span><span class="sxs-lookup"><span data-stu-id="c729c-113">CN</span></span>                | <span data-ttu-id="c729c-114">複寫-屬性中繼資料</span><span class="sxs-lookup"><span data-stu-id="c729c-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="c729c-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c729c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c729c-116">replPropertyMetaData</span><span class="sxs-lookup"><span data-stu-id="c729c-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="c729c-117">大小</span><span class="sxs-lookup"><span data-stu-id="c729c-117">Size</span></span>              | <span data-ttu-id="c729c-118">長度與物件上可複製屬性的數目成正比。</span><span class="sxs-lookup"><span data-stu-id="c729c-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="c729c-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c729c-119">Update Privilege</span></span>  | <span data-ttu-id="c729c-120">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="c729c-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="c729c-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c729c-121">Update Frequency</span></span>  | <span data-ttu-id="c729c-122">變更，以回應物件中的任何複寫變更。</span><span class="sxs-lookup"><span data-stu-id="c729c-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="c729c-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-123">Attribute-Id</span></span>      | <span data-ttu-id="c729c-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="c729c-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="c729c-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c729c-125">System-Id-Guid</span></span>    | <span data-ttu-id="c729c-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c729c-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="c729c-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="c729c-127">Syntax</span></span>            | [<span data-ttu-id="c729c-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c729c-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="c729c-129">實作</span><span class="sxs-lookup"><span data-stu-id="c729c-129">Implementations</span></span>

-   [<span data-ttu-id="c729c-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c729c-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c729c-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c729c-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c729c-132">**亞當**</span><span class="sxs-lookup"><span data-stu-id="c729c-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c729c-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c729c-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c729c-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c729c-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c729c-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c729c-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c729c-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c729c-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c729c-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c729c-137">Windows 2000 Server</span></span>



| <span data-ttu-id="c729c-138">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-138">Entry</span></span> | <span data-ttu-id="c729c-139">值</span><span class="sxs-lookup"><span data-stu-id="c729c-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c729c-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c729c-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="c729c-142">System-Only</span></span>            | <span data-ttu-id="c729c-143">對</span><span class="sxs-lookup"><span data-stu-id="c729c-143">True</span></span>                            |
| <span data-ttu-id="c729c-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c729c-144">Is-Single-Valued</span></span>       | <span data-ttu-id="c729c-145">對</span><span class="sxs-lookup"><span data-stu-id="c729c-145">True</span></span>                            |
| <span data-ttu-id="c729c-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c729c-146">Is Indexed</span></span>             | <span data-ttu-id="c729c-147">否</span><span class="sxs-lookup"><span data-stu-id="c729c-147">False</span></span>                           |
| <span data-ttu-id="c729c-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c729c-148">In Global Catalog</span></span>      | <span data-ttu-id="c729c-149">對</span><span class="sxs-lookup"><span data-stu-id="c729c-149">True</span></span>                            |
| <span data-ttu-id="c729c-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c729c-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="c729c-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c729c-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c729c-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c729c-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c729c-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c729c-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c729c-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-154">Search-Flags</span></span>           | <span data-ttu-id="c729c-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c729c-155">0x00000008</span></span>                      |
| <span data-ttu-id="c729c-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-156">System-Flags</span></span>           | <span data-ttu-id="c729c-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="c729c-157">0x00000013</span></span>                      |
| <span data-ttu-id="c729c-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c729c-158">Classes used in</span></span>        | [<span data-ttu-id="c729c-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c729c-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c729c-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c729c-160">Windows Server 2003</span></span>



| <span data-ttu-id="c729c-161">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-161">Entry</span></span> | <span data-ttu-id="c729c-162">值</span><span class="sxs-lookup"><span data-stu-id="c729c-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c729c-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c729c-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="c729c-165">System-Only</span></span>            | <span data-ttu-id="c729c-166">對</span><span class="sxs-lookup"><span data-stu-id="c729c-166">True</span></span>                            |
| <span data-ttu-id="c729c-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c729c-167">Is-Single-Valued</span></span>       | <span data-ttu-id="c729c-168">對</span><span class="sxs-lookup"><span data-stu-id="c729c-168">True</span></span>                            |
| <span data-ttu-id="c729c-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c729c-169">Is Indexed</span></span>             | <span data-ttu-id="c729c-170">否</span><span class="sxs-lookup"><span data-stu-id="c729c-170">False</span></span>                           |
| <span data-ttu-id="c729c-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c729c-171">In Global Catalog</span></span>      | <span data-ttu-id="c729c-172">對</span><span class="sxs-lookup"><span data-stu-id="c729c-172">True</span></span>                            |
| <span data-ttu-id="c729c-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c729c-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="c729c-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c729c-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c729c-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c729c-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c729c-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c729c-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c729c-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-177">Search-Flags</span></span>           | <span data-ttu-id="c729c-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c729c-178">0x00000008</span></span>                      |
| <span data-ttu-id="c729c-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-179">System-Flags</span></span>           | <span data-ttu-id="c729c-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="c729c-180">0x0000001B</span></span>                      |
| <span data-ttu-id="c729c-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c729c-181">Classes used in</span></span>        | [<span data-ttu-id="c729c-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c729c-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c729c-183">亞當</span><span class="sxs-lookup"><span data-stu-id="c729c-183">ADAM</span></span>



| <span data-ttu-id="c729c-184">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-184">Entry</span></span> | <span data-ttu-id="c729c-185">值</span><span class="sxs-lookup"><span data-stu-id="c729c-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c729c-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c729c-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="c729c-188">System-Only</span></span>            | <span data-ttu-id="c729c-189">對</span><span class="sxs-lookup"><span data-stu-id="c729c-189">True</span></span>                            |
| <span data-ttu-id="c729c-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c729c-190">Is-Single-Valued</span></span>       | <span data-ttu-id="c729c-191">對</span><span class="sxs-lookup"><span data-stu-id="c729c-191">True</span></span>                            |
| <span data-ttu-id="c729c-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c729c-192">Is Indexed</span></span>             | <span data-ttu-id="c729c-193">否</span><span class="sxs-lookup"><span data-stu-id="c729c-193">False</span></span>                           |
| <span data-ttu-id="c729c-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c729c-194">In Global Catalog</span></span>      | <span data-ttu-id="c729c-195">對</span><span class="sxs-lookup"><span data-stu-id="c729c-195">True</span></span>                            |
| <span data-ttu-id="c729c-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c729c-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="c729c-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c729c-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c729c-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c729c-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c729c-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c729c-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c729c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-200">Search-Flags</span></span>           | <span data-ttu-id="c729c-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c729c-201">0x00000008</span></span>                      |
| <span data-ttu-id="c729c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-202">System-Flags</span></span>           | <span data-ttu-id="c729c-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="c729c-203">0x0000001B</span></span>                      |
| <span data-ttu-id="c729c-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c729c-204">Classes used in</span></span>        | [<span data-ttu-id="c729c-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c729c-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c729c-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c729c-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c729c-207">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-207">Entry</span></span> | <span data-ttu-id="c729c-208">值</span><span class="sxs-lookup"><span data-stu-id="c729c-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c729c-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c729c-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="c729c-211">System-Only</span></span>            | <span data-ttu-id="c729c-212">對</span><span class="sxs-lookup"><span data-stu-id="c729c-212">True</span></span>                            |
| <span data-ttu-id="c729c-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c729c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="c729c-214">對</span><span class="sxs-lookup"><span data-stu-id="c729c-214">True</span></span>                            |
| <span data-ttu-id="c729c-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c729c-215">Is Indexed</span></span>             | <span data-ttu-id="c729c-216">否</span><span class="sxs-lookup"><span data-stu-id="c729c-216">False</span></span>                           |
| <span data-ttu-id="c729c-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c729c-217">In Global Catalog</span></span>      | <span data-ttu-id="c729c-218">對</span><span class="sxs-lookup"><span data-stu-id="c729c-218">True</span></span>                            |
| <span data-ttu-id="c729c-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c729c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="c729c-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c729c-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c729c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c729c-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c729c-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c729c-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c729c-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-223">Search-Flags</span></span>           | <span data-ttu-id="c729c-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c729c-224">0x00000008</span></span>                      |
| <span data-ttu-id="c729c-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-225">System-Flags</span></span>           | <span data-ttu-id="c729c-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="c729c-226">0x0000001B</span></span>                      |
| <span data-ttu-id="c729c-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c729c-227">Classes used in</span></span>        | [<span data-ttu-id="c729c-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c729c-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c729c-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c729c-229">Windows Server 2008</span></span>



| <span data-ttu-id="c729c-230">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-230">Entry</span></span> | <span data-ttu-id="c729c-231">值</span><span class="sxs-lookup"><span data-stu-id="c729c-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c729c-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c729c-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="c729c-234">System-Only</span></span>            | <span data-ttu-id="c729c-235">對</span><span class="sxs-lookup"><span data-stu-id="c729c-235">True</span></span>                            |
| <span data-ttu-id="c729c-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c729c-236">Is-Single-Valued</span></span>       | <span data-ttu-id="c729c-237">對</span><span class="sxs-lookup"><span data-stu-id="c729c-237">True</span></span>                            |
| <span data-ttu-id="c729c-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c729c-238">Is Indexed</span></span>             | <span data-ttu-id="c729c-239">否</span><span class="sxs-lookup"><span data-stu-id="c729c-239">False</span></span>                           |
| <span data-ttu-id="c729c-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c729c-240">In Global Catalog</span></span>      | <span data-ttu-id="c729c-241">對</span><span class="sxs-lookup"><span data-stu-id="c729c-241">True</span></span>                            |
| <span data-ttu-id="c729c-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c729c-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="c729c-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c729c-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c729c-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c729c-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c729c-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c729c-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c729c-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-246">Search-Flags</span></span>           | <span data-ttu-id="c729c-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c729c-247">0x00000008</span></span>                      |
| <span data-ttu-id="c729c-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-248">System-Flags</span></span>           | <span data-ttu-id="c729c-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="c729c-249">0x0000001B</span></span>                      |
| <span data-ttu-id="c729c-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c729c-250">Classes used in</span></span>        | [<span data-ttu-id="c729c-251">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c729c-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c729c-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c729c-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c729c-253">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-253">Entry</span></span> | <span data-ttu-id="c729c-254">值</span><span class="sxs-lookup"><span data-stu-id="c729c-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c729c-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c729c-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="c729c-257">System-Only</span></span>            | <span data-ttu-id="c729c-258">對</span><span class="sxs-lookup"><span data-stu-id="c729c-258">True</span></span>                            |
| <span data-ttu-id="c729c-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c729c-259">Is-Single-Valued</span></span>       | <span data-ttu-id="c729c-260">對</span><span class="sxs-lookup"><span data-stu-id="c729c-260">True</span></span>                            |
| <span data-ttu-id="c729c-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c729c-261">Is Indexed</span></span>             | <span data-ttu-id="c729c-262">否</span><span class="sxs-lookup"><span data-stu-id="c729c-262">False</span></span>                           |
| <span data-ttu-id="c729c-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c729c-263">In Global Catalog</span></span>      | <span data-ttu-id="c729c-264">對</span><span class="sxs-lookup"><span data-stu-id="c729c-264">True</span></span>                            |
| <span data-ttu-id="c729c-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c729c-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="c729c-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c729c-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c729c-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c729c-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c729c-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c729c-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c729c-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-269">Search-Flags</span></span>           | <span data-ttu-id="c729c-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c729c-270">0x00000008</span></span>                      |
| <span data-ttu-id="c729c-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-271">System-Flags</span></span>           | <span data-ttu-id="c729c-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="c729c-272">0x0000001B</span></span>                      |
| <span data-ttu-id="c729c-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c729c-273">Classes used in</span></span>        | [<span data-ttu-id="c729c-274">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c729c-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c729c-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c729c-275">Windows Server 2012</span></span>



| <span data-ttu-id="c729c-276">進入</span><span class="sxs-lookup"><span data-stu-id="c729c-276">Entry</span></span> | <span data-ttu-id="c729c-277">值</span><span class="sxs-lookup"><span data-stu-id="c729c-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c729c-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c729c-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c729c-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c729c-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="c729c-280">System-Only</span></span>            | <span data-ttu-id="c729c-281">對</span><span class="sxs-lookup"><span data-stu-id="c729c-281">True</span></span>                            |
| <span data-ttu-id="c729c-282">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c729c-282">Is-Single-Valued</span></span>       | <span data-ttu-id="c729c-283">對</span><span class="sxs-lookup"><span data-stu-id="c729c-283">True</span></span>                            |
| <span data-ttu-id="c729c-284">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c729c-284">Is Indexed</span></span>             | <span data-ttu-id="c729c-285">否</span><span class="sxs-lookup"><span data-stu-id="c729c-285">False</span></span>                           |
| <span data-ttu-id="c729c-286">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c729c-286">In Global Catalog</span></span>      | <span data-ttu-id="c729c-287">對</span><span class="sxs-lookup"><span data-stu-id="c729c-287">True</span></span>                            |
| <span data-ttu-id="c729c-288">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c729c-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="c729c-289">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c729c-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c729c-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c729c-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c729c-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c729c-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c729c-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-292">Search-Flags</span></span>           | <span data-ttu-id="c729c-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c729c-293">0x00000008</span></span>                      |
| <span data-ttu-id="c729c-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c729c-294">System-Flags</span></span>           | <span data-ttu-id="c729c-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="c729c-295">0x0000001B</span></span>                      |
| <span data-ttu-id="c729c-296">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c729c-296">Classes used in</span></span>        | [<span data-ttu-id="c729c-297">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="c729c-297">**Top**</span></span>](c-top.md)<br/> |



 

 





