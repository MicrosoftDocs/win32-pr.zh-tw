---
title: 部分屬性-刪除清單屬性
description: 追蹤部分複本的內部複寫狀態 (也就是在 Gc) 上。 部分複本 NC 物件的屬性。 當 GC 正在從其部分複本 Nc 中的物件中移除屬性時使用。
ms.assetid: 0084774b-7231-4cfc-8f60-c014006da2b9
ms.tgt_platform: multiple
keywords:
- 部分屬性-刪除-列出屬性 AD 架構
- partialAttributeDeletionList 屬性 AD 架構
topic_type:
- apiref
api_name:
- Partial-Attribute-Deletion-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2c6c0428d71dbba4199eeb441c838fb54a4463
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966981"
---
# <a name="partial-attribute-deletion-list-attribute"></a><span data-ttu-id="541a7-107">部分屬性-刪除清單屬性</span><span class="sxs-lookup"><span data-stu-id="541a7-107">Partial-Attribute-Deletion-List attribute</span></span>

<span data-ttu-id="541a7-108">追蹤部分複本的內部複寫狀態 (也就是在 Gc) 上。</span><span class="sxs-lookup"><span data-stu-id="541a7-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="541a7-109">部分複本 NC 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="541a7-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="541a7-110">當 GC 正在從其部分複本 Nc 中的物件中移除屬性時使用。</span><span class="sxs-lookup"><span data-stu-id="541a7-110">Used when the GC is in the process of removing attributes from the objects in its partial replica NCs.</span></span>



| <span data-ttu-id="541a7-111">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-111">Entry</span></span> | <span data-ttu-id="541a7-112">值</span><span class="sxs-lookup"><span data-stu-id="541a7-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="541a7-113">CN</span><span class="sxs-lookup"><span data-stu-id="541a7-113">CN</span></span>                | <span data-ttu-id="541a7-114">部分屬性-刪除-清單</span><span class="sxs-lookup"><span data-stu-id="541a7-114">Partial-Attribute-Deletion-List</span></span>                       |
| <span data-ttu-id="541a7-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="541a7-115">Ldap-Display-Name</span></span> | <span data-ttu-id="541a7-116">partialAttributeDeletionList</span><span class="sxs-lookup"><span data-stu-id="541a7-116">partialAttributeDeletionList</span></span>                          |
| <span data-ttu-id="541a7-117">大小</span><span class="sxs-lookup"><span data-stu-id="541a7-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="541a7-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="541a7-118">Update Privilege</span></span>  | <span data-ttu-id="541a7-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="541a7-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="541a7-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="541a7-120">Update Frequency</span></span>  | <span data-ttu-id="541a7-121">複寫期間</span><span class="sxs-lookup"><span data-stu-id="541a7-121">During replication</span></span>                                    |
| <span data-ttu-id="541a7-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-122">Attribute-Id</span></span>      | <span data-ttu-id="541a7-123">1.2.840.113556.1.4.663</span><span class="sxs-lookup"><span data-stu-id="541a7-123">1.2.840.113556.1.4.663</span></span>                                |
| <span data-ttu-id="541a7-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="541a7-124">System-Id-Guid</span></span>    | <span data-ttu-id="541a7-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="541a7-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span></span>                  |
| <span data-ttu-id="541a7-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="541a7-126">Syntax</span></span>            | [<span data-ttu-id="541a7-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="541a7-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="541a7-128">實作</span><span class="sxs-lookup"><span data-stu-id="541a7-128">Implementations</span></span>

-   [<span data-ttu-id="541a7-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="541a7-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="541a7-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="541a7-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="541a7-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="541a7-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="541a7-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="541a7-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="541a7-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="541a7-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="541a7-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="541a7-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="541a7-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="541a7-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="541a7-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="541a7-136">Windows 2000 Server</span></span>



| <span data-ttu-id="541a7-137">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-137">Entry</span></span> | <span data-ttu-id="541a7-138">值</span><span class="sxs-lookup"><span data-stu-id="541a7-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="541a7-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="541a7-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="541a7-141">System-Only</span></span>            | <span data-ttu-id="541a7-142">對</span><span class="sxs-lookup"><span data-stu-id="541a7-142">True</span></span>                            |
| <span data-ttu-id="541a7-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="541a7-143">Is-Single-Valued</span></span>       | <span data-ttu-id="541a7-144">對</span><span class="sxs-lookup"><span data-stu-id="541a7-144">True</span></span>                            |
| <span data-ttu-id="541a7-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="541a7-145">Is Indexed</span></span>             | <span data-ttu-id="541a7-146">否</span><span class="sxs-lookup"><span data-stu-id="541a7-146">False</span></span>                           |
| <span data-ttu-id="541a7-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="541a7-147">In Global Catalog</span></span>      | <span data-ttu-id="541a7-148">對</span><span class="sxs-lookup"><span data-stu-id="541a7-148">True</span></span>                            |
| <span data-ttu-id="541a7-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="541a7-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="541a7-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="541a7-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="541a7-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="541a7-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="541a7-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="541a7-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="541a7-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-153">Search-Flags</span></span>           | <span data-ttu-id="541a7-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="541a7-154">0x00000000</span></span>                      |
| <span data-ttu-id="541a7-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-155">System-Flags</span></span>           | <span data-ttu-id="541a7-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="541a7-156">0x00000013</span></span>                      |
| <span data-ttu-id="541a7-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="541a7-157">Classes used in</span></span>        | [<span data-ttu-id="541a7-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="541a7-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="541a7-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="541a7-159">Windows Server 2003</span></span>



| <span data-ttu-id="541a7-160">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-160">Entry</span></span> | <span data-ttu-id="541a7-161">值</span><span class="sxs-lookup"><span data-stu-id="541a7-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="541a7-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="541a7-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="541a7-164">System-Only</span></span>            | <span data-ttu-id="541a7-165">對</span><span class="sxs-lookup"><span data-stu-id="541a7-165">True</span></span>                            |
| <span data-ttu-id="541a7-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="541a7-166">Is-Single-Valued</span></span>       | <span data-ttu-id="541a7-167">對</span><span class="sxs-lookup"><span data-stu-id="541a7-167">True</span></span>                            |
| <span data-ttu-id="541a7-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="541a7-168">Is Indexed</span></span>             | <span data-ttu-id="541a7-169">否</span><span class="sxs-lookup"><span data-stu-id="541a7-169">False</span></span>                           |
| <span data-ttu-id="541a7-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="541a7-170">In Global Catalog</span></span>      | <span data-ttu-id="541a7-171">對</span><span class="sxs-lookup"><span data-stu-id="541a7-171">True</span></span>                            |
| <span data-ttu-id="541a7-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="541a7-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="541a7-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="541a7-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="541a7-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="541a7-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="541a7-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="541a7-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="541a7-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-176">Search-Flags</span></span>           | <span data-ttu-id="541a7-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="541a7-177">0x00000000</span></span>                      |
| <span data-ttu-id="541a7-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-178">System-Flags</span></span>           | <span data-ttu-id="541a7-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="541a7-179">0x00000013</span></span>                      |
| <span data-ttu-id="541a7-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="541a7-180">Classes used in</span></span>        | [<span data-ttu-id="541a7-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="541a7-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="541a7-182">亞當</span><span class="sxs-lookup"><span data-stu-id="541a7-182">ADAM</span></span>



| <span data-ttu-id="541a7-183">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-183">Entry</span></span> | <span data-ttu-id="541a7-184">值</span><span class="sxs-lookup"><span data-stu-id="541a7-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="541a7-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="541a7-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="541a7-187">System-Only</span></span>            | <span data-ttu-id="541a7-188">對</span><span class="sxs-lookup"><span data-stu-id="541a7-188">True</span></span>                            |
| <span data-ttu-id="541a7-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="541a7-189">Is-Single-Valued</span></span>       | <span data-ttu-id="541a7-190">對</span><span class="sxs-lookup"><span data-stu-id="541a7-190">True</span></span>                            |
| <span data-ttu-id="541a7-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="541a7-191">Is Indexed</span></span>             | <span data-ttu-id="541a7-192">否</span><span class="sxs-lookup"><span data-stu-id="541a7-192">False</span></span>                           |
| <span data-ttu-id="541a7-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="541a7-193">In Global Catalog</span></span>      | <span data-ttu-id="541a7-194">對</span><span class="sxs-lookup"><span data-stu-id="541a7-194">True</span></span>                            |
| <span data-ttu-id="541a7-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="541a7-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="541a7-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="541a7-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="541a7-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="541a7-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="541a7-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="541a7-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="541a7-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-199">Search-Flags</span></span>           | <span data-ttu-id="541a7-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="541a7-200">0x00000000</span></span>                      |
| <span data-ttu-id="541a7-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-201">System-Flags</span></span>           | <span data-ttu-id="541a7-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="541a7-202">0x00000013</span></span>                      |
| <span data-ttu-id="541a7-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="541a7-203">Classes used in</span></span>        | [<span data-ttu-id="541a7-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="541a7-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="541a7-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="541a7-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="541a7-206">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-206">Entry</span></span> | <span data-ttu-id="541a7-207">值</span><span class="sxs-lookup"><span data-stu-id="541a7-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="541a7-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="541a7-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="541a7-210">System-Only</span></span>            | <span data-ttu-id="541a7-211">對</span><span class="sxs-lookup"><span data-stu-id="541a7-211">True</span></span>                            |
| <span data-ttu-id="541a7-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="541a7-212">Is-Single-Valued</span></span>       | <span data-ttu-id="541a7-213">對</span><span class="sxs-lookup"><span data-stu-id="541a7-213">True</span></span>                            |
| <span data-ttu-id="541a7-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="541a7-214">Is Indexed</span></span>             | <span data-ttu-id="541a7-215">否</span><span class="sxs-lookup"><span data-stu-id="541a7-215">False</span></span>                           |
| <span data-ttu-id="541a7-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="541a7-216">In Global Catalog</span></span>      | <span data-ttu-id="541a7-217">對</span><span class="sxs-lookup"><span data-stu-id="541a7-217">True</span></span>                            |
| <span data-ttu-id="541a7-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="541a7-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="541a7-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="541a7-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="541a7-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="541a7-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="541a7-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="541a7-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="541a7-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-222">Search-Flags</span></span>           | <span data-ttu-id="541a7-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="541a7-223">0x00000000</span></span>                      |
| <span data-ttu-id="541a7-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-224">System-Flags</span></span>           | <span data-ttu-id="541a7-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="541a7-225">0x00000013</span></span>                      |
| <span data-ttu-id="541a7-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="541a7-226">Classes used in</span></span>        | [<span data-ttu-id="541a7-227">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="541a7-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="541a7-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="541a7-228">Windows Server 2008</span></span>



| <span data-ttu-id="541a7-229">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-229">Entry</span></span> | <span data-ttu-id="541a7-230">值</span><span class="sxs-lookup"><span data-stu-id="541a7-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="541a7-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="541a7-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="541a7-233">System-Only</span></span>            | <span data-ttu-id="541a7-234">對</span><span class="sxs-lookup"><span data-stu-id="541a7-234">True</span></span>                            |
| <span data-ttu-id="541a7-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="541a7-235">Is-Single-Valued</span></span>       | <span data-ttu-id="541a7-236">對</span><span class="sxs-lookup"><span data-stu-id="541a7-236">True</span></span>                            |
| <span data-ttu-id="541a7-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="541a7-237">Is Indexed</span></span>             | <span data-ttu-id="541a7-238">否</span><span class="sxs-lookup"><span data-stu-id="541a7-238">False</span></span>                           |
| <span data-ttu-id="541a7-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="541a7-239">In Global Catalog</span></span>      | <span data-ttu-id="541a7-240">對</span><span class="sxs-lookup"><span data-stu-id="541a7-240">True</span></span>                            |
| <span data-ttu-id="541a7-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="541a7-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="541a7-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="541a7-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="541a7-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="541a7-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="541a7-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="541a7-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="541a7-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-245">Search-Flags</span></span>           | <span data-ttu-id="541a7-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="541a7-246">0x00000000</span></span>                      |
| <span data-ttu-id="541a7-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-247">System-Flags</span></span>           | <span data-ttu-id="541a7-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="541a7-248">0x00000013</span></span>                      |
| <span data-ttu-id="541a7-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="541a7-249">Classes used in</span></span>        | [<span data-ttu-id="541a7-250">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="541a7-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="541a7-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="541a7-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="541a7-252">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-252">Entry</span></span> | <span data-ttu-id="541a7-253">值</span><span class="sxs-lookup"><span data-stu-id="541a7-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="541a7-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="541a7-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="541a7-256">System-Only</span></span>            | <span data-ttu-id="541a7-257">對</span><span class="sxs-lookup"><span data-stu-id="541a7-257">True</span></span>                            |
| <span data-ttu-id="541a7-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="541a7-258">Is-Single-Valued</span></span>       | <span data-ttu-id="541a7-259">對</span><span class="sxs-lookup"><span data-stu-id="541a7-259">True</span></span>                            |
| <span data-ttu-id="541a7-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="541a7-260">Is Indexed</span></span>             | <span data-ttu-id="541a7-261">否</span><span class="sxs-lookup"><span data-stu-id="541a7-261">False</span></span>                           |
| <span data-ttu-id="541a7-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="541a7-262">In Global Catalog</span></span>      | <span data-ttu-id="541a7-263">對</span><span class="sxs-lookup"><span data-stu-id="541a7-263">True</span></span>                            |
| <span data-ttu-id="541a7-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="541a7-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="541a7-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="541a7-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="541a7-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="541a7-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="541a7-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="541a7-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="541a7-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-268">Search-Flags</span></span>           | <span data-ttu-id="541a7-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="541a7-269">0x00000000</span></span>                      |
| <span data-ttu-id="541a7-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-270">System-Flags</span></span>           | <span data-ttu-id="541a7-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="541a7-271">0x00000013</span></span>                      |
| <span data-ttu-id="541a7-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="541a7-272">Classes used in</span></span>        | [<span data-ttu-id="541a7-273">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="541a7-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="541a7-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="541a7-274">Windows Server 2012</span></span>



| <span data-ttu-id="541a7-275">進入</span><span class="sxs-lookup"><span data-stu-id="541a7-275">Entry</span></span> | <span data-ttu-id="541a7-276">值</span><span class="sxs-lookup"><span data-stu-id="541a7-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="541a7-277">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="541a7-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="541a7-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="541a7-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="541a7-279">System-Only</span></span>            | <span data-ttu-id="541a7-280">對</span><span class="sxs-lookup"><span data-stu-id="541a7-280">True</span></span>                            |
| <span data-ttu-id="541a7-281">是-單一值</span><span class="sxs-lookup"><span data-stu-id="541a7-281">Is-Single-Valued</span></span>       | <span data-ttu-id="541a7-282">對</span><span class="sxs-lookup"><span data-stu-id="541a7-282">True</span></span>                            |
| <span data-ttu-id="541a7-283">已編制索引</span><span class="sxs-lookup"><span data-stu-id="541a7-283">Is Indexed</span></span>             | <span data-ttu-id="541a7-284">否</span><span class="sxs-lookup"><span data-stu-id="541a7-284">False</span></span>                           |
| <span data-ttu-id="541a7-285">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="541a7-285">In Global Catalog</span></span>      | <span data-ttu-id="541a7-286">對</span><span class="sxs-lookup"><span data-stu-id="541a7-286">True</span></span>                            |
| <span data-ttu-id="541a7-287">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="541a7-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="541a7-288">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="541a7-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="541a7-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="541a7-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="541a7-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="541a7-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="541a7-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-291">Search-Flags</span></span>           | <span data-ttu-id="541a7-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="541a7-292">0x00000000</span></span>                      |
| <span data-ttu-id="541a7-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="541a7-293">System-Flags</span></span>           | <span data-ttu-id="541a7-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="541a7-294">0x00000013</span></span>                      |
| <span data-ttu-id="541a7-295">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="541a7-295">Classes used in</span></span>        | [<span data-ttu-id="541a7-296">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="541a7-296">**Top**</span></span>](c-top.md)<br/> |



 

 





