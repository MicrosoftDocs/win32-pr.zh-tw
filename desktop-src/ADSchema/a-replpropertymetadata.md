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
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="06b18-107">複寫-屬性中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="06b18-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="06b18-108">追蹤 DS 物件的內部複寫狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="06b18-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="06b18-109">您可以透過公用 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。</span><span class="sxs-lookup"><span data-stu-id="06b18-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="06b18-110">存在於所有 DS 物件上。</span><span class="sxs-lookup"><span data-stu-id="06b18-110">Present on all DS objects.</span></span>



| <span data-ttu-id="06b18-111">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-111">Entry</span></span> | <span data-ttu-id="06b18-112">值</span><span class="sxs-lookup"><span data-stu-id="06b18-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="06b18-113">CN</span><span class="sxs-lookup"><span data-stu-id="06b18-113">CN</span></span>                | <span data-ttu-id="06b18-114">複寫-屬性中繼資料</span><span class="sxs-lookup"><span data-stu-id="06b18-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="06b18-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="06b18-115">Ldap-Display-Name</span></span> | <span data-ttu-id="06b18-116">replPropertyMetaData</span><span class="sxs-lookup"><span data-stu-id="06b18-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="06b18-117">大小</span><span class="sxs-lookup"><span data-stu-id="06b18-117">Size</span></span>              | <span data-ttu-id="06b18-118">長度與物件上可複製屬性的數目成正比。</span><span class="sxs-lookup"><span data-stu-id="06b18-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="06b18-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="06b18-119">Update Privilege</span></span>  | <span data-ttu-id="06b18-120">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="06b18-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="06b18-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="06b18-121">Update Frequency</span></span>  | <span data-ttu-id="06b18-122">變更，以回應物件中的任何複寫變更。</span><span class="sxs-lookup"><span data-stu-id="06b18-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="06b18-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-123">Attribute-Id</span></span>      | <span data-ttu-id="06b18-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="06b18-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="06b18-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="06b18-125">System-Id-Guid</span></span>    | <span data-ttu-id="06b18-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="06b18-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="06b18-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="06b18-127">Syntax</span></span>            | [<span data-ttu-id="06b18-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="06b18-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="06b18-129">實作</span><span class="sxs-lookup"><span data-stu-id="06b18-129">Implementations</span></span>

-   [<span data-ttu-id="06b18-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="06b18-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="06b18-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="06b18-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="06b18-132">**亞當**</span><span class="sxs-lookup"><span data-stu-id="06b18-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="06b18-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="06b18-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="06b18-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="06b18-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="06b18-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="06b18-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="06b18-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="06b18-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="06b18-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06b18-137">Windows 2000 Server</span></span>



| <span data-ttu-id="06b18-138">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-138">Entry</span></span> | <span data-ttu-id="06b18-139">值</span><span class="sxs-lookup"><span data-stu-id="06b18-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="06b18-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06b18-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="06b18-142">System-Only</span></span>            | <span data-ttu-id="06b18-143">對</span><span class="sxs-lookup"><span data-stu-id="06b18-143">True</span></span>                            |
| <span data-ttu-id="06b18-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06b18-144">Is-Single-Valued</span></span>       | <span data-ttu-id="06b18-145">對</span><span class="sxs-lookup"><span data-stu-id="06b18-145">True</span></span>                            |
| <span data-ttu-id="06b18-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06b18-146">Is Indexed</span></span>             | <span data-ttu-id="06b18-147">否</span><span class="sxs-lookup"><span data-stu-id="06b18-147">False</span></span>                           |
| <span data-ttu-id="06b18-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06b18-148">In Global Catalog</span></span>      | <span data-ttu-id="06b18-149">對</span><span class="sxs-lookup"><span data-stu-id="06b18-149">True</span></span>                            |
| <span data-ttu-id="06b18-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06b18-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="06b18-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06b18-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="06b18-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06b18-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="06b18-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06b18-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="06b18-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-154">Search-Flags</span></span>           | <span data-ttu-id="06b18-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06b18-155">0x00000008</span></span>                      |
| <span data-ttu-id="06b18-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-156">System-Flags</span></span>           | <span data-ttu-id="06b18-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="06b18-157">0x00000013</span></span>                      |
| <span data-ttu-id="06b18-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06b18-158">Classes used in</span></span>        | [<span data-ttu-id="06b18-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="06b18-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="06b18-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06b18-160">Windows Server 2003</span></span>



| <span data-ttu-id="06b18-161">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-161">Entry</span></span> | <span data-ttu-id="06b18-162">值</span><span class="sxs-lookup"><span data-stu-id="06b18-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="06b18-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06b18-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="06b18-165">System-Only</span></span>            | <span data-ttu-id="06b18-166">對</span><span class="sxs-lookup"><span data-stu-id="06b18-166">True</span></span>                            |
| <span data-ttu-id="06b18-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06b18-167">Is-Single-Valued</span></span>       | <span data-ttu-id="06b18-168">對</span><span class="sxs-lookup"><span data-stu-id="06b18-168">True</span></span>                            |
| <span data-ttu-id="06b18-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06b18-169">Is Indexed</span></span>             | <span data-ttu-id="06b18-170">否</span><span class="sxs-lookup"><span data-stu-id="06b18-170">False</span></span>                           |
| <span data-ttu-id="06b18-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06b18-171">In Global Catalog</span></span>      | <span data-ttu-id="06b18-172">對</span><span class="sxs-lookup"><span data-stu-id="06b18-172">True</span></span>                            |
| <span data-ttu-id="06b18-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06b18-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="06b18-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06b18-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="06b18-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06b18-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="06b18-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06b18-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="06b18-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-177">Search-Flags</span></span>           | <span data-ttu-id="06b18-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06b18-178">0x00000008</span></span>                      |
| <span data-ttu-id="06b18-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-179">System-Flags</span></span>           | <span data-ttu-id="06b18-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="06b18-180">0x0000001B</span></span>                      |
| <span data-ttu-id="06b18-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06b18-181">Classes used in</span></span>        | [<span data-ttu-id="06b18-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="06b18-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="06b18-183">亞當</span><span class="sxs-lookup"><span data-stu-id="06b18-183">ADAM</span></span>



| <span data-ttu-id="06b18-184">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-184">Entry</span></span> | <span data-ttu-id="06b18-185">值</span><span class="sxs-lookup"><span data-stu-id="06b18-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="06b18-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06b18-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="06b18-188">System-Only</span></span>            | <span data-ttu-id="06b18-189">對</span><span class="sxs-lookup"><span data-stu-id="06b18-189">True</span></span>                            |
| <span data-ttu-id="06b18-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06b18-190">Is-Single-Valued</span></span>       | <span data-ttu-id="06b18-191">對</span><span class="sxs-lookup"><span data-stu-id="06b18-191">True</span></span>                            |
| <span data-ttu-id="06b18-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06b18-192">Is Indexed</span></span>             | <span data-ttu-id="06b18-193">否</span><span class="sxs-lookup"><span data-stu-id="06b18-193">False</span></span>                           |
| <span data-ttu-id="06b18-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06b18-194">In Global Catalog</span></span>      | <span data-ttu-id="06b18-195">對</span><span class="sxs-lookup"><span data-stu-id="06b18-195">True</span></span>                            |
| <span data-ttu-id="06b18-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06b18-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="06b18-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06b18-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="06b18-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06b18-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="06b18-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06b18-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="06b18-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-200">Search-Flags</span></span>           | <span data-ttu-id="06b18-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06b18-201">0x00000008</span></span>                      |
| <span data-ttu-id="06b18-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-202">System-Flags</span></span>           | <span data-ttu-id="06b18-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="06b18-203">0x0000001B</span></span>                      |
| <span data-ttu-id="06b18-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06b18-204">Classes used in</span></span>        | [<span data-ttu-id="06b18-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="06b18-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="06b18-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="06b18-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="06b18-207">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-207">Entry</span></span> | <span data-ttu-id="06b18-208">值</span><span class="sxs-lookup"><span data-stu-id="06b18-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="06b18-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06b18-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="06b18-211">System-Only</span></span>            | <span data-ttu-id="06b18-212">對</span><span class="sxs-lookup"><span data-stu-id="06b18-212">True</span></span>                            |
| <span data-ttu-id="06b18-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06b18-213">Is-Single-Valued</span></span>       | <span data-ttu-id="06b18-214">對</span><span class="sxs-lookup"><span data-stu-id="06b18-214">True</span></span>                            |
| <span data-ttu-id="06b18-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06b18-215">Is Indexed</span></span>             | <span data-ttu-id="06b18-216">否</span><span class="sxs-lookup"><span data-stu-id="06b18-216">False</span></span>                           |
| <span data-ttu-id="06b18-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06b18-217">In Global Catalog</span></span>      | <span data-ttu-id="06b18-218">對</span><span class="sxs-lookup"><span data-stu-id="06b18-218">True</span></span>                            |
| <span data-ttu-id="06b18-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06b18-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="06b18-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06b18-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="06b18-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06b18-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="06b18-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06b18-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="06b18-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-223">Search-Flags</span></span>           | <span data-ttu-id="06b18-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06b18-224">0x00000008</span></span>                      |
| <span data-ttu-id="06b18-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-225">System-Flags</span></span>           | <span data-ttu-id="06b18-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="06b18-226">0x0000001B</span></span>                      |
| <span data-ttu-id="06b18-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06b18-227">Classes used in</span></span>        | [<span data-ttu-id="06b18-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="06b18-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="06b18-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06b18-229">Windows Server 2008</span></span>



| <span data-ttu-id="06b18-230">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-230">Entry</span></span> | <span data-ttu-id="06b18-231">值</span><span class="sxs-lookup"><span data-stu-id="06b18-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="06b18-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06b18-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="06b18-234">System-Only</span></span>            | <span data-ttu-id="06b18-235">對</span><span class="sxs-lookup"><span data-stu-id="06b18-235">True</span></span>                            |
| <span data-ttu-id="06b18-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06b18-236">Is-Single-Valued</span></span>       | <span data-ttu-id="06b18-237">對</span><span class="sxs-lookup"><span data-stu-id="06b18-237">True</span></span>                            |
| <span data-ttu-id="06b18-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06b18-238">Is Indexed</span></span>             | <span data-ttu-id="06b18-239">否</span><span class="sxs-lookup"><span data-stu-id="06b18-239">False</span></span>                           |
| <span data-ttu-id="06b18-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06b18-240">In Global Catalog</span></span>      | <span data-ttu-id="06b18-241">對</span><span class="sxs-lookup"><span data-stu-id="06b18-241">True</span></span>                            |
| <span data-ttu-id="06b18-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06b18-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="06b18-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06b18-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="06b18-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06b18-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="06b18-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06b18-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="06b18-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-246">Search-Flags</span></span>           | <span data-ttu-id="06b18-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06b18-247">0x00000008</span></span>                      |
| <span data-ttu-id="06b18-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-248">System-Flags</span></span>           | <span data-ttu-id="06b18-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="06b18-249">0x0000001B</span></span>                      |
| <span data-ttu-id="06b18-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06b18-250">Classes used in</span></span>        | [<span data-ttu-id="06b18-251">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="06b18-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="06b18-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06b18-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="06b18-253">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-253">Entry</span></span> | <span data-ttu-id="06b18-254">值</span><span class="sxs-lookup"><span data-stu-id="06b18-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="06b18-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06b18-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="06b18-257">System-Only</span></span>            | <span data-ttu-id="06b18-258">對</span><span class="sxs-lookup"><span data-stu-id="06b18-258">True</span></span>                            |
| <span data-ttu-id="06b18-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06b18-259">Is-Single-Valued</span></span>       | <span data-ttu-id="06b18-260">對</span><span class="sxs-lookup"><span data-stu-id="06b18-260">True</span></span>                            |
| <span data-ttu-id="06b18-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06b18-261">Is Indexed</span></span>             | <span data-ttu-id="06b18-262">否</span><span class="sxs-lookup"><span data-stu-id="06b18-262">False</span></span>                           |
| <span data-ttu-id="06b18-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06b18-263">In Global Catalog</span></span>      | <span data-ttu-id="06b18-264">對</span><span class="sxs-lookup"><span data-stu-id="06b18-264">True</span></span>                            |
| <span data-ttu-id="06b18-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06b18-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="06b18-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06b18-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="06b18-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06b18-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="06b18-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06b18-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="06b18-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-269">Search-Flags</span></span>           | <span data-ttu-id="06b18-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06b18-270">0x00000008</span></span>                      |
| <span data-ttu-id="06b18-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-271">System-Flags</span></span>           | <span data-ttu-id="06b18-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="06b18-272">0x0000001B</span></span>                      |
| <span data-ttu-id="06b18-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06b18-273">Classes used in</span></span>        | [<span data-ttu-id="06b18-274">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="06b18-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="06b18-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06b18-275">Windows Server 2012</span></span>



| <span data-ttu-id="06b18-276">進入</span><span class="sxs-lookup"><span data-stu-id="06b18-276">Entry</span></span> | <span data-ttu-id="06b18-277">值</span><span class="sxs-lookup"><span data-stu-id="06b18-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="06b18-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="06b18-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06b18-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="06b18-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="06b18-280">System-Only</span></span>            | <span data-ttu-id="06b18-281">對</span><span class="sxs-lookup"><span data-stu-id="06b18-281">True</span></span>                            |
| <span data-ttu-id="06b18-282">是-單一值</span><span class="sxs-lookup"><span data-stu-id="06b18-282">Is-Single-Valued</span></span>       | <span data-ttu-id="06b18-283">對</span><span class="sxs-lookup"><span data-stu-id="06b18-283">True</span></span>                            |
| <span data-ttu-id="06b18-284">已編制索引</span><span class="sxs-lookup"><span data-stu-id="06b18-284">Is Indexed</span></span>             | <span data-ttu-id="06b18-285">否</span><span class="sxs-lookup"><span data-stu-id="06b18-285">False</span></span>                           |
| <span data-ttu-id="06b18-286">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="06b18-286">In Global Catalog</span></span>      | <span data-ttu-id="06b18-287">對</span><span class="sxs-lookup"><span data-stu-id="06b18-287">True</span></span>                            |
| <span data-ttu-id="06b18-288">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="06b18-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="06b18-289">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="06b18-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="06b18-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06b18-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="06b18-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06b18-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="06b18-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-292">Search-Flags</span></span>           | <span data-ttu-id="06b18-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="06b18-293">0x00000008</span></span>                      |
| <span data-ttu-id="06b18-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06b18-294">System-Flags</span></span>           | <span data-ttu-id="06b18-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="06b18-295">0x0000001B</span></span>                      |
| <span data-ttu-id="06b18-296">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="06b18-296">Classes used in</span></span>        | [<span data-ttu-id="06b18-297">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="06b18-297">**Top**</span></span>](c-top.md)<br/> |



 

 





