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
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="629a8-106">修改時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="629a8-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="629a8-107">計算的屬性，表示上次變更此物件的日期。</span><span class="sxs-lookup"><span data-stu-id="629a8-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="629a8-108">此值不會複寫。</span><span class="sxs-lookup"><span data-stu-id="629a8-108">This value is not replicated.</span></span>



| <span data-ttu-id="629a8-109">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-109">Entry</span></span> | <span data-ttu-id="629a8-110">值</span><span class="sxs-lookup"><span data-stu-id="629a8-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="629a8-111">CN</span><span class="sxs-lookup"><span data-stu-id="629a8-111">CN</span></span>                | <span data-ttu-id="629a8-112">修改時間戳記</span><span class="sxs-lookup"><span data-stu-id="629a8-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="629a8-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="629a8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="629a8-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="629a8-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="629a8-115">大小</span><span class="sxs-lookup"><span data-stu-id="629a8-115">Size</span></span>              | <span data-ttu-id="629a8-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="629a8-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="629a8-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="629a8-117">Update Privilege</span></span>  | <span data-ttu-id="629a8-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="629a8-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="629a8-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="629a8-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="629a8-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-120">Attribute-Id</span></span>      | <span data-ttu-id="629a8-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="629a8-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="629a8-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="629a8-122">System-Id-Guid</span></span>    | <span data-ttu-id="629a8-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="629a8-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="629a8-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="629a8-124">Syntax</span></span>            | [<span data-ttu-id="629a8-125">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="629a8-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="629a8-126">實作</span><span class="sxs-lookup"><span data-stu-id="629a8-126">Implementations</span></span>

-   [<span data-ttu-id="629a8-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="629a8-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="629a8-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="629a8-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="629a8-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="629a8-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="629a8-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="629a8-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="629a8-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="629a8-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="629a8-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="629a8-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="629a8-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="629a8-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="629a8-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="629a8-134">Windows 2000 Server</span></span>



| <span data-ttu-id="629a8-135">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-135">Entry</span></span> | <span data-ttu-id="629a8-136">值</span><span class="sxs-lookup"><span data-stu-id="629a8-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="629a8-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629a8-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="629a8-139">System-Only</span></span>            | <span data-ttu-id="629a8-140">對</span><span class="sxs-lookup"><span data-stu-id="629a8-140">True</span></span>                                                                        |
| <span data-ttu-id="629a8-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629a8-141">Is-Single-Valued</span></span>       | <span data-ttu-id="629a8-142">對</span><span class="sxs-lookup"><span data-stu-id="629a8-142">True</span></span>                                                                        |
| <span data-ttu-id="629a8-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629a8-143">Is Indexed</span></span>             | <span data-ttu-id="629a8-144">否</span><span class="sxs-lookup"><span data-stu-id="629a8-144">False</span></span>                                                                       |
| <span data-ttu-id="629a8-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629a8-145">In Global Catalog</span></span>      | <span data-ttu-id="629a8-146">否</span><span class="sxs-lookup"><span data-stu-id="629a8-146">False</span></span>                                                                       |
| <span data-ttu-id="629a8-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629a8-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="629a8-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629a8-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="629a8-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629a8-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629a8-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-151">Search-Flags</span></span>           | <span data-ttu-id="629a8-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629a8-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="629a8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-153">System-Flags</span></span>           | <span data-ttu-id="629a8-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="629a8-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="629a8-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629a8-155">Classes used in</span></span>        | [<span data-ttu-id="629a8-156">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="629a8-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="629a8-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="629a8-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="629a8-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="629a8-158">Windows Server 2003</span></span>



| <span data-ttu-id="629a8-159">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-159">Entry</span></span> | <span data-ttu-id="629a8-160">值</span><span class="sxs-lookup"><span data-stu-id="629a8-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="629a8-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629a8-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="629a8-163">System-Only</span></span>            | <span data-ttu-id="629a8-164">對</span><span class="sxs-lookup"><span data-stu-id="629a8-164">True</span></span>                                                                        |
| <span data-ttu-id="629a8-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629a8-165">Is-Single-Valued</span></span>       | <span data-ttu-id="629a8-166">對</span><span class="sxs-lookup"><span data-stu-id="629a8-166">True</span></span>                                                                        |
| <span data-ttu-id="629a8-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629a8-167">Is Indexed</span></span>             | <span data-ttu-id="629a8-168">否</span><span class="sxs-lookup"><span data-stu-id="629a8-168">False</span></span>                                                                       |
| <span data-ttu-id="629a8-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629a8-169">In Global Catalog</span></span>      | <span data-ttu-id="629a8-170">否</span><span class="sxs-lookup"><span data-stu-id="629a8-170">False</span></span>                                                                       |
| <span data-ttu-id="629a8-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629a8-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="629a8-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629a8-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="629a8-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629a8-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629a8-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-175">Search-Flags</span></span>           | <span data-ttu-id="629a8-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629a8-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="629a8-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-177">System-Flags</span></span>           | <span data-ttu-id="629a8-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="629a8-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="629a8-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629a8-179">Classes used in</span></span>        | [<span data-ttu-id="629a8-180">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="629a8-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="629a8-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="629a8-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="629a8-182">亞當</span><span class="sxs-lookup"><span data-stu-id="629a8-182">ADAM</span></span>



| <span data-ttu-id="629a8-183">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-183">Entry</span></span> | <span data-ttu-id="629a8-184">值</span><span class="sxs-lookup"><span data-stu-id="629a8-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="629a8-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629a8-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="629a8-187">System-Only</span></span>            | <span data-ttu-id="629a8-188">對</span><span class="sxs-lookup"><span data-stu-id="629a8-188">True</span></span>                                                                        |
| <span data-ttu-id="629a8-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629a8-189">Is-Single-Valued</span></span>       | <span data-ttu-id="629a8-190">對</span><span class="sxs-lookup"><span data-stu-id="629a8-190">True</span></span>                                                                        |
| <span data-ttu-id="629a8-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629a8-191">Is Indexed</span></span>             | <span data-ttu-id="629a8-192">否</span><span class="sxs-lookup"><span data-stu-id="629a8-192">False</span></span>                                                                       |
| <span data-ttu-id="629a8-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629a8-193">In Global Catalog</span></span>      | <span data-ttu-id="629a8-194">否</span><span class="sxs-lookup"><span data-stu-id="629a8-194">False</span></span>                                                                       |
| <span data-ttu-id="629a8-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629a8-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="629a8-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629a8-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="629a8-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629a8-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629a8-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-199">Search-Flags</span></span>           | <span data-ttu-id="629a8-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629a8-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="629a8-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-201">System-Flags</span></span>           | <span data-ttu-id="629a8-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="629a8-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="629a8-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629a8-203">Classes used in</span></span>        | [<span data-ttu-id="629a8-204">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="629a8-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="629a8-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="629a8-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="629a8-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="629a8-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="629a8-207">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-207">Entry</span></span> | <span data-ttu-id="629a8-208">值</span><span class="sxs-lookup"><span data-stu-id="629a8-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="629a8-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629a8-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="629a8-211">System-Only</span></span>            | <span data-ttu-id="629a8-212">對</span><span class="sxs-lookup"><span data-stu-id="629a8-212">True</span></span>                                                                        |
| <span data-ttu-id="629a8-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629a8-213">Is-Single-Valued</span></span>       | <span data-ttu-id="629a8-214">對</span><span class="sxs-lookup"><span data-stu-id="629a8-214">True</span></span>                                                                        |
| <span data-ttu-id="629a8-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629a8-215">Is Indexed</span></span>             | <span data-ttu-id="629a8-216">否</span><span class="sxs-lookup"><span data-stu-id="629a8-216">False</span></span>                                                                       |
| <span data-ttu-id="629a8-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629a8-217">In Global Catalog</span></span>      | <span data-ttu-id="629a8-218">否</span><span class="sxs-lookup"><span data-stu-id="629a8-218">False</span></span>                                                                       |
| <span data-ttu-id="629a8-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629a8-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="629a8-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629a8-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="629a8-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629a8-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629a8-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-223">Search-Flags</span></span>           | <span data-ttu-id="629a8-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629a8-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="629a8-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-225">System-Flags</span></span>           | <span data-ttu-id="629a8-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="629a8-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="629a8-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629a8-227">Classes used in</span></span>        | [<span data-ttu-id="629a8-228">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="629a8-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="629a8-229">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="629a8-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="629a8-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="629a8-230">Windows Server 2008</span></span>



| <span data-ttu-id="629a8-231">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-231">Entry</span></span> | <span data-ttu-id="629a8-232">值</span><span class="sxs-lookup"><span data-stu-id="629a8-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="629a8-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629a8-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="629a8-235">System-Only</span></span>            | <span data-ttu-id="629a8-236">對</span><span class="sxs-lookup"><span data-stu-id="629a8-236">True</span></span>                                                                        |
| <span data-ttu-id="629a8-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629a8-237">Is-Single-Valued</span></span>       | <span data-ttu-id="629a8-238">對</span><span class="sxs-lookup"><span data-stu-id="629a8-238">True</span></span>                                                                        |
| <span data-ttu-id="629a8-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629a8-239">Is Indexed</span></span>             | <span data-ttu-id="629a8-240">否</span><span class="sxs-lookup"><span data-stu-id="629a8-240">False</span></span>                                                                       |
| <span data-ttu-id="629a8-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629a8-241">In Global Catalog</span></span>      | <span data-ttu-id="629a8-242">否</span><span class="sxs-lookup"><span data-stu-id="629a8-242">False</span></span>                                                                       |
| <span data-ttu-id="629a8-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629a8-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="629a8-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629a8-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="629a8-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629a8-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629a8-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-247">Search-Flags</span></span>           | <span data-ttu-id="629a8-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629a8-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="629a8-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-249">System-Flags</span></span>           | <span data-ttu-id="629a8-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="629a8-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="629a8-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629a8-251">Classes used in</span></span>        | [<span data-ttu-id="629a8-252">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="629a8-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="629a8-253">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="629a8-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="629a8-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="629a8-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="629a8-255">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-255">Entry</span></span> | <span data-ttu-id="629a8-256">值</span><span class="sxs-lookup"><span data-stu-id="629a8-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="629a8-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629a8-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="629a8-259">System-Only</span></span>            | <span data-ttu-id="629a8-260">對</span><span class="sxs-lookup"><span data-stu-id="629a8-260">True</span></span>                                                                        |
| <span data-ttu-id="629a8-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629a8-261">Is-Single-Valued</span></span>       | <span data-ttu-id="629a8-262">對</span><span class="sxs-lookup"><span data-stu-id="629a8-262">True</span></span>                                                                        |
| <span data-ttu-id="629a8-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629a8-263">Is Indexed</span></span>             | <span data-ttu-id="629a8-264">否</span><span class="sxs-lookup"><span data-stu-id="629a8-264">False</span></span>                                                                       |
| <span data-ttu-id="629a8-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629a8-265">In Global Catalog</span></span>      | <span data-ttu-id="629a8-266">否</span><span class="sxs-lookup"><span data-stu-id="629a8-266">False</span></span>                                                                       |
| <span data-ttu-id="629a8-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629a8-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="629a8-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629a8-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="629a8-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629a8-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629a8-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-271">Search-Flags</span></span>           | <span data-ttu-id="629a8-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629a8-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="629a8-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-273">System-Flags</span></span>           | <span data-ttu-id="629a8-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="629a8-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="629a8-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629a8-275">Classes used in</span></span>        | [<span data-ttu-id="629a8-276">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="629a8-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="629a8-277">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="629a8-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="629a8-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="629a8-278">Windows Server 2012</span></span>



| <span data-ttu-id="629a8-279">進入</span><span class="sxs-lookup"><span data-stu-id="629a8-279">Entry</span></span> | <span data-ttu-id="629a8-280">值</span><span class="sxs-lookup"><span data-stu-id="629a8-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="629a8-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629a8-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629a8-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="629a8-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="629a8-283">System-Only</span></span>            | <span data-ttu-id="629a8-284">對</span><span class="sxs-lookup"><span data-stu-id="629a8-284">True</span></span>                                                                        |
| <span data-ttu-id="629a8-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629a8-285">Is-Single-Valued</span></span>       | <span data-ttu-id="629a8-286">對</span><span class="sxs-lookup"><span data-stu-id="629a8-286">True</span></span>                                                                        |
| <span data-ttu-id="629a8-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629a8-287">Is Indexed</span></span>             | <span data-ttu-id="629a8-288">否</span><span class="sxs-lookup"><span data-stu-id="629a8-288">False</span></span>                                                                       |
| <span data-ttu-id="629a8-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629a8-289">In Global Catalog</span></span>      | <span data-ttu-id="629a8-290">否</span><span class="sxs-lookup"><span data-stu-id="629a8-290">False</span></span>                                                                       |
| <span data-ttu-id="629a8-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629a8-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="629a8-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629a8-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="629a8-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629a8-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629a8-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="629a8-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-295">Search-Flags</span></span>           | <span data-ttu-id="629a8-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629a8-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="629a8-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629a8-297">System-Flags</span></span>           | <span data-ttu-id="629a8-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="629a8-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="629a8-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629a8-299">Classes used in</span></span>        | [<span data-ttu-id="629a8-300">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="629a8-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="629a8-301">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="629a8-301">**Top**</span></span>](c-top.md)<br/> |



 

 





