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
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="5b7f4-106">修改時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="5b7f4-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="5b7f4-107">計算的屬性，表示上次變更此物件的日期。</span><span class="sxs-lookup"><span data-stu-id="5b7f4-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="5b7f4-108">此值不會複寫。</span><span class="sxs-lookup"><span data-stu-id="5b7f4-108">This value is not replicated.</span></span>



| <span data-ttu-id="5b7f4-109">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-109">Entry</span></span> | <span data-ttu-id="5b7f4-110">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="5b7f4-111">CN</span><span class="sxs-lookup"><span data-stu-id="5b7f4-111">CN</span></span>                | <span data-ttu-id="5b7f4-112">修改時間戳記</span><span class="sxs-lookup"><span data-stu-id="5b7f4-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="5b7f4-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5b7f4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5b7f4-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="5b7f4-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="5b7f4-115">大小</span><span class="sxs-lookup"><span data-stu-id="5b7f4-115">Size</span></span>              | <span data-ttu-id="5b7f4-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="5b7f4-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="5b7f4-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5b7f4-117">Update Privilege</span></span>  | <span data-ttu-id="5b7f4-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="5b7f4-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="5b7f4-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5b7f4-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="5b7f4-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-120">Attribute-Id</span></span>      | <span data-ttu-id="5b7f4-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="5b7f4-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="5b7f4-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5b7f4-122">System-Id-Guid</span></span>    | <span data-ttu-id="5b7f4-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="5b7f4-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="5b7f4-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b7f4-124">Syntax</span></span>            | [<span data-ttu-id="5b7f4-125">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="5b7f4-126">實作</span><span class="sxs-lookup"><span data-stu-id="5b7f4-126">Implementations</span></span>

-   [<span data-ttu-id="5b7f4-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5b7f4-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5b7f4-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5b7f4-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5b7f4-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5b7f4-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5b7f4-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5b7f4-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b7f4-134">Windows 2000 Server</span></span>



| <span data-ttu-id="5b7f4-135">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-135">Entry</span></span> | <span data-ttu-id="5b7f4-136">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b7f4-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5b7f4-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7f4-139">System-Only</span></span>            | <span data-ttu-id="5b7f4-140">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-140">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-141">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7f4-142">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-142">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5b7f4-143">Is Indexed</span></span>             | <span data-ttu-id="5b7f4-144">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-144">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5b7f4-145">In Global Catalog</span></span>      | <span data-ttu-id="5b7f4-146">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-146">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5b7f4-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7f4-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5b7f4-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="5b7f4-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7f4-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7f4-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-151">Search-Flags</span></span>           | <span data-ttu-id="5b7f4-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7f4-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="5b7f4-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-153">System-Flags</span></span>           | <span data-ttu-id="5b7f4-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5b7f4-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="5b7f4-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5b7f4-155">Classes used in</span></span>        | [<span data-ttu-id="5b7f4-156">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="5b7f4-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5b7f4-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5b7f4-158">Windows Server 2003</span></span>



| <span data-ttu-id="5b7f4-159">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-159">Entry</span></span> | <span data-ttu-id="5b7f4-160">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b7f4-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5b7f4-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7f4-163">System-Only</span></span>            | <span data-ttu-id="5b7f4-164">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-164">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-165">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7f4-166">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-166">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5b7f4-167">Is Indexed</span></span>             | <span data-ttu-id="5b7f4-168">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-168">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5b7f4-169">In Global Catalog</span></span>      | <span data-ttu-id="5b7f4-170">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-170">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5b7f4-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7f4-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5b7f4-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="5b7f4-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7f4-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7f4-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-175">Search-Flags</span></span>           | <span data-ttu-id="5b7f4-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7f4-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="5b7f4-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-177">System-Flags</span></span>           | <span data-ttu-id="5b7f4-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5b7f4-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="5b7f4-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5b7f4-179">Classes used in</span></span>        | [<span data-ttu-id="5b7f4-180">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="5b7f4-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5b7f4-182">亞當</span><span class="sxs-lookup"><span data-stu-id="5b7f4-182">ADAM</span></span>



| <span data-ttu-id="5b7f4-183">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-183">Entry</span></span> | <span data-ttu-id="5b7f4-184">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b7f4-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5b7f4-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7f4-187">System-Only</span></span>            | <span data-ttu-id="5b7f4-188">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-188">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-189">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7f4-190">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-190">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5b7f4-191">Is Indexed</span></span>             | <span data-ttu-id="5b7f4-192">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-192">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5b7f4-193">In Global Catalog</span></span>      | <span data-ttu-id="5b7f4-194">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-194">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5b7f4-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7f4-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5b7f4-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="5b7f4-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7f4-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7f4-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-199">Search-Flags</span></span>           | <span data-ttu-id="5b7f4-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7f4-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="5b7f4-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-201">System-Flags</span></span>           | <span data-ttu-id="5b7f4-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5b7f4-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="5b7f4-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5b7f4-203">Classes used in</span></span>        | [<span data-ttu-id="5b7f4-204">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="5b7f4-205">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5b7f4-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5b7f4-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5b7f4-207">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-207">Entry</span></span> | <span data-ttu-id="5b7f4-208">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b7f4-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5b7f4-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7f4-211">System-Only</span></span>            | <span data-ttu-id="5b7f4-212">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-212">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-213">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7f4-214">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-214">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5b7f4-215">Is Indexed</span></span>             | <span data-ttu-id="5b7f4-216">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-216">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5b7f4-217">In Global Catalog</span></span>      | <span data-ttu-id="5b7f4-218">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-218">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5b7f4-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7f4-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5b7f4-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="5b7f4-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7f4-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7f4-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-223">Search-Flags</span></span>           | <span data-ttu-id="5b7f4-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7f4-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="5b7f4-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-225">System-Flags</span></span>           | <span data-ttu-id="5b7f4-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5b7f4-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="5b7f4-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5b7f4-227">Classes used in</span></span>        | [<span data-ttu-id="5b7f4-228">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="5b7f4-229">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5b7f4-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b7f4-230">Windows Server 2008</span></span>



| <span data-ttu-id="5b7f4-231">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-231">Entry</span></span> | <span data-ttu-id="5b7f4-232">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b7f4-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5b7f4-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7f4-235">System-Only</span></span>            | <span data-ttu-id="5b7f4-236">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-236">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-237">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7f4-238">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-238">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5b7f4-239">Is Indexed</span></span>             | <span data-ttu-id="5b7f4-240">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-240">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5b7f4-241">In Global Catalog</span></span>      | <span data-ttu-id="5b7f4-242">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-242">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5b7f4-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7f4-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5b7f4-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="5b7f4-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7f4-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7f4-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-247">Search-Flags</span></span>           | <span data-ttu-id="5b7f4-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7f4-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="5b7f4-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-249">System-Flags</span></span>           | <span data-ttu-id="5b7f4-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5b7f4-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="5b7f4-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5b7f4-251">Classes used in</span></span>        | [<span data-ttu-id="5b7f4-252">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="5b7f4-253">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5b7f4-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5b7f4-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5b7f4-255">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-255">Entry</span></span> | <span data-ttu-id="5b7f4-256">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b7f4-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5b7f4-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7f4-259">System-Only</span></span>            | <span data-ttu-id="5b7f4-260">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-260">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-261">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7f4-262">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-262">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5b7f4-263">Is Indexed</span></span>             | <span data-ttu-id="5b7f4-264">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-264">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5b7f4-265">In Global Catalog</span></span>      | <span data-ttu-id="5b7f4-266">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-266">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5b7f4-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7f4-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5b7f4-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="5b7f4-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7f4-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7f4-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-271">Search-Flags</span></span>           | <span data-ttu-id="5b7f4-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7f4-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="5b7f4-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-273">System-Flags</span></span>           | <span data-ttu-id="5b7f4-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5b7f4-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="5b7f4-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5b7f4-275">Classes used in</span></span>        | [<span data-ttu-id="5b7f4-276">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="5b7f4-277">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5b7f4-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b7f4-278">Windows Server 2012</span></span>



| <span data-ttu-id="5b7f4-279">進入</span><span class="sxs-lookup"><span data-stu-id="5b7f4-279">Entry</span></span> | <span data-ttu-id="5b7f4-280">值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5b7f4-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5b7f4-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7f4-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="5b7f4-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7f4-283">System-Only</span></span>            | <span data-ttu-id="5b7f4-284">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-284">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5b7f4-285">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7f4-286">對</span><span class="sxs-lookup"><span data-stu-id="5b7f4-286">True</span></span>                                                                        |
| <span data-ttu-id="5b7f4-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5b7f4-287">Is Indexed</span></span>             | <span data-ttu-id="5b7f4-288">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-288">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5b7f4-289">In Global Catalog</span></span>      | <span data-ttu-id="5b7f4-290">否</span><span class="sxs-lookup"><span data-stu-id="5b7f4-290">False</span></span>                                                                       |
| <span data-ttu-id="5b7f4-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5b7f4-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7f4-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5b7f4-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="5b7f4-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7f4-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7f4-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="5b7f4-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-295">Search-Flags</span></span>           | <span data-ttu-id="5b7f4-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7f4-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="5b7f4-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7f4-297">System-Flags</span></span>           | <span data-ttu-id="5b7f4-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="5b7f4-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="5b7f4-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5b7f4-299">Classes used in</span></span>        | [<span data-ttu-id="5b7f4-300">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="5b7f4-301">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="5b7f4-301">**Top**</span></span>](c-top.md)<br/> |



 

 





