---
title: 修改時間戳記屬性
description: 計算的屬性，表示上次變更此物件的日期。 此值不會複寫。
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- 修改時間戳記屬性 AD 架構
- modifyTimeStamp 屬性 AD 架構
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c032d19c3bd2bf5a6ee0cfe038e9fa9b184d36
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686847"
---
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="6a585-106">修改時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="6a585-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="6a585-107">計算的屬性，表示上次變更此物件的日期。</span><span class="sxs-lookup"><span data-stu-id="6a585-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="6a585-108">此值不會複寫。</span><span class="sxs-lookup"><span data-stu-id="6a585-108">This value is not replicated.</span></span>



| <span data-ttu-id="6a585-109">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-109">Entry</span></span> | <span data-ttu-id="6a585-110">值</span><span class="sxs-lookup"><span data-stu-id="6a585-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="6a585-111">CN</span><span class="sxs-lookup"><span data-stu-id="6a585-111">CN</span></span>                | <span data-ttu-id="6a585-112">修改時間戳記</span><span class="sxs-lookup"><span data-stu-id="6a585-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="6a585-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6a585-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6a585-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="6a585-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="6a585-115">大小</span><span class="sxs-lookup"><span data-stu-id="6a585-115">Size</span></span>              | <span data-ttu-id="6a585-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="6a585-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="6a585-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6a585-117">Update Privilege</span></span>  | <span data-ttu-id="6a585-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="6a585-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="6a585-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6a585-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="6a585-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-120">Attribute-Id</span></span>      | <span data-ttu-id="6a585-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="6a585-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="6a585-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6a585-122">System-Id-Guid</span></span>    | <span data-ttu-id="6a585-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6a585-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="6a585-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a585-124">Syntax</span></span>            | [<span data-ttu-id="6a585-125">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="6a585-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="6a585-126">實作</span><span class="sxs-lookup"><span data-stu-id="6a585-126">Implementations</span></span>

-   [<span data-ttu-id="6a585-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6a585-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6a585-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a585-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a585-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6a585-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6a585-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a585-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a585-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a585-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a585-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a585-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a585-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a585-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6a585-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a585-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6a585-135">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-135">Entry</span></span> | <span data-ttu-id="6a585-136">值</span><span class="sxs-lookup"><span data-stu-id="6a585-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a585-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a585-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a585-139">System-Only</span></span>            | <span data-ttu-id="6a585-140">對</span><span class="sxs-lookup"><span data-stu-id="6a585-140">True</span></span>                                                                        |
| <span data-ttu-id="6a585-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a585-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6a585-142">對</span><span class="sxs-lookup"><span data-stu-id="6a585-142">True</span></span>                                                                        |
| <span data-ttu-id="6a585-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a585-143">Is Indexed</span></span>             | <span data-ttu-id="6a585-144">否</span><span class="sxs-lookup"><span data-stu-id="6a585-144">False</span></span>                                                                       |
| <span data-ttu-id="6a585-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a585-145">In Global Catalog</span></span>      | <span data-ttu-id="6a585-146">否</span><span class="sxs-lookup"><span data-stu-id="6a585-146">False</span></span>                                                                       |
| <span data-ttu-id="6a585-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a585-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a585-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a585-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6a585-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a585-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a585-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-151">Search-Flags</span></span>           | <span data-ttu-id="6a585-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a585-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6a585-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-153">System-Flags</span></span>           | <span data-ttu-id="6a585-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a585-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6a585-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a585-155">Classes used in</span></span>        | [<span data-ttu-id="6a585-156">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="6a585-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6a585-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6a585-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6a585-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a585-158">Windows Server 2003</span></span>



| <span data-ttu-id="6a585-159">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-159">Entry</span></span> | <span data-ttu-id="6a585-160">值</span><span class="sxs-lookup"><span data-stu-id="6a585-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a585-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a585-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a585-163">System-Only</span></span>            | <span data-ttu-id="6a585-164">對</span><span class="sxs-lookup"><span data-stu-id="6a585-164">True</span></span>                                                                        |
| <span data-ttu-id="6a585-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a585-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6a585-166">對</span><span class="sxs-lookup"><span data-stu-id="6a585-166">True</span></span>                                                                        |
| <span data-ttu-id="6a585-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a585-167">Is Indexed</span></span>             | <span data-ttu-id="6a585-168">否</span><span class="sxs-lookup"><span data-stu-id="6a585-168">False</span></span>                                                                       |
| <span data-ttu-id="6a585-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a585-169">In Global Catalog</span></span>      | <span data-ttu-id="6a585-170">否</span><span class="sxs-lookup"><span data-stu-id="6a585-170">False</span></span>                                                                       |
| <span data-ttu-id="6a585-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a585-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a585-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a585-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6a585-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a585-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a585-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-175">Search-Flags</span></span>           | <span data-ttu-id="6a585-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a585-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6a585-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-177">System-Flags</span></span>           | <span data-ttu-id="6a585-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a585-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6a585-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a585-179">Classes used in</span></span>        | [<span data-ttu-id="6a585-180">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="6a585-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6a585-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6a585-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6a585-182">亞當</span><span class="sxs-lookup"><span data-stu-id="6a585-182">ADAM</span></span>



| <span data-ttu-id="6a585-183">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-183">Entry</span></span> | <span data-ttu-id="6a585-184">值</span><span class="sxs-lookup"><span data-stu-id="6a585-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a585-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a585-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a585-187">System-Only</span></span>            | <span data-ttu-id="6a585-188">對</span><span class="sxs-lookup"><span data-stu-id="6a585-188">True</span></span>                                                                        |
| <span data-ttu-id="6a585-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a585-189">Is-Single-Valued</span></span>       | <span data-ttu-id="6a585-190">對</span><span class="sxs-lookup"><span data-stu-id="6a585-190">True</span></span>                                                                        |
| <span data-ttu-id="6a585-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a585-191">Is Indexed</span></span>             | <span data-ttu-id="6a585-192">否</span><span class="sxs-lookup"><span data-stu-id="6a585-192">False</span></span>                                                                       |
| <span data-ttu-id="6a585-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a585-193">In Global Catalog</span></span>      | <span data-ttu-id="6a585-194">否</span><span class="sxs-lookup"><span data-stu-id="6a585-194">False</span></span>                                                                       |
| <span data-ttu-id="6a585-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a585-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a585-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a585-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6a585-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a585-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a585-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-199">Search-Flags</span></span>           | <span data-ttu-id="6a585-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a585-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6a585-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-201">System-Flags</span></span>           | <span data-ttu-id="6a585-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a585-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6a585-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a585-203">Classes used in</span></span>        | [<span data-ttu-id="6a585-204">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="6a585-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6a585-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6a585-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a585-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a585-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a585-207">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-207">Entry</span></span> | <span data-ttu-id="6a585-208">值</span><span class="sxs-lookup"><span data-stu-id="6a585-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a585-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a585-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a585-211">System-Only</span></span>            | <span data-ttu-id="6a585-212">對</span><span class="sxs-lookup"><span data-stu-id="6a585-212">True</span></span>                                                                        |
| <span data-ttu-id="6a585-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a585-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6a585-214">對</span><span class="sxs-lookup"><span data-stu-id="6a585-214">True</span></span>                                                                        |
| <span data-ttu-id="6a585-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a585-215">Is Indexed</span></span>             | <span data-ttu-id="6a585-216">否</span><span class="sxs-lookup"><span data-stu-id="6a585-216">False</span></span>                                                                       |
| <span data-ttu-id="6a585-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a585-217">In Global Catalog</span></span>      | <span data-ttu-id="6a585-218">否</span><span class="sxs-lookup"><span data-stu-id="6a585-218">False</span></span>                                                                       |
| <span data-ttu-id="6a585-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a585-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a585-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a585-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6a585-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a585-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a585-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-223">Search-Flags</span></span>           | <span data-ttu-id="6a585-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a585-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6a585-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-225">System-Flags</span></span>           | <span data-ttu-id="6a585-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a585-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6a585-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a585-227">Classes used in</span></span>        | [<span data-ttu-id="6a585-228">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="6a585-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6a585-229">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6a585-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a585-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a585-230">Windows Server 2008</span></span>



| <span data-ttu-id="6a585-231">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-231">Entry</span></span> | <span data-ttu-id="6a585-232">值</span><span class="sxs-lookup"><span data-stu-id="6a585-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a585-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a585-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a585-235">System-Only</span></span>            | <span data-ttu-id="6a585-236">對</span><span class="sxs-lookup"><span data-stu-id="6a585-236">True</span></span>                                                                        |
| <span data-ttu-id="6a585-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a585-237">Is-Single-Valued</span></span>       | <span data-ttu-id="6a585-238">對</span><span class="sxs-lookup"><span data-stu-id="6a585-238">True</span></span>                                                                        |
| <span data-ttu-id="6a585-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a585-239">Is Indexed</span></span>             | <span data-ttu-id="6a585-240">否</span><span class="sxs-lookup"><span data-stu-id="6a585-240">False</span></span>                                                                       |
| <span data-ttu-id="6a585-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a585-241">In Global Catalog</span></span>      | <span data-ttu-id="6a585-242">否</span><span class="sxs-lookup"><span data-stu-id="6a585-242">False</span></span>                                                                       |
| <span data-ttu-id="6a585-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a585-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a585-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a585-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6a585-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a585-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a585-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-247">Search-Flags</span></span>           | <span data-ttu-id="6a585-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a585-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6a585-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-249">System-Flags</span></span>           | <span data-ttu-id="6a585-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a585-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6a585-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a585-251">Classes used in</span></span>        | [<span data-ttu-id="6a585-252">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="6a585-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6a585-253">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6a585-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a585-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a585-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a585-255">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-255">Entry</span></span> | <span data-ttu-id="6a585-256">值</span><span class="sxs-lookup"><span data-stu-id="6a585-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a585-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a585-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a585-259">System-Only</span></span>            | <span data-ttu-id="6a585-260">對</span><span class="sxs-lookup"><span data-stu-id="6a585-260">True</span></span>                                                                        |
| <span data-ttu-id="6a585-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a585-261">Is-Single-Valued</span></span>       | <span data-ttu-id="6a585-262">對</span><span class="sxs-lookup"><span data-stu-id="6a585-262">True</span></span>                                                                        |
| <span data-ttu-id="6a585-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a585-263">Is Indexed</span></span>             | <span data-ttu-id="6a585-264">否</span><span class="sxs-lookup"><span data-stu-id="6a585-264">False</span></span>                                                                       |
| <span data-ttu-id="6a585-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a585-265">In Global Catalog</span></span>      | <span data-ttu-id="6a585-266">否</span><span class="sxs-lookup"><span data-stu-id="6a585-266">False</span></span>                                                                       |
| <span data-ttu-id="6a585-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a585-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a585-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a585-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6a585-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a585-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a585-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-271">Search-Flags</span></span>           | <span data-ttu-id="6a585-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a585-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6a585-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-273">System-Flags</span></span>           | <span data-ttu-id="6a585-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a585-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6a585-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a585-275">Classes used in</span></span>        | [<span data-ttu-id="6a585-276">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="6a585-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6a585-277">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6a585-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a585-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a585-278">Windows Server 2012</span></span>



| <span data-ttu-id="6a585-279">進入</span><span class="sxs-lookup"><span data-stu-id="6a585-279">Entry</span></span> | <span data-ttu-id="6a585-280">值</span><span class="sxs-lookup"><span data-stu-id="6a585-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6a585-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a585-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a585-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6a585-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a585-283">System-Only</span></span>            | <span data-ttu-id="6a585-284">對</span><span class="sxs-lookup"><span data-stu-id="6a585-284">True</span></span>                                                                        |
| <span data-ttu-id="6a585-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a585-285">Is-Single-Valued</span></span>       | <span data-ttu-id="6a585-286">對</span><span class="sxs-lookup"><span data-stu-id="6a585-286">True</span></span>                                                                        |
| <span data-ttu-id="6a585-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a585-287">Is Indexed</span></span>             | <span data-ttu-id="6a585-288">否</span><span class="sxs-lookup"><span data-stu-id="6a585-288">False</span></span>                                                                       |
| <span data-ttu-id="6a585-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a585-289">In Global Catalog</span></span>      | <span data-ttu-id="6a585-290">否</span><span class="sxs-lookup"><span data-stu-id="6a585-290">False</span></span>                                                                       |
| <span data-ttu-id="6a585-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a585-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a585-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a585-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6a585-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a585-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a585-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6a585-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-295">Search-Flags</span></span>           | <span data-ttu-id="6a585-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a585-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6a585-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a585-297">System-Flags</span></span>           | <span data-ttu-id="6a585-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a585-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6a585-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a585-299">Classes used in</span></span>        | [<span data-ttu-id="6a585-300">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="6a585-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6a585-301">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6a585-301">**Top**</span></span>](c-top.md)<br/> |



 

 





