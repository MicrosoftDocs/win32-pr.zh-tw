---
title: Object-Version 屬性
description: 這可以用來儲存物件的版本號碼。
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- Object-Version 屬性 AD 架構
- objectVersion 屬性 AD 架構
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f038f6286db575f4141c2e306086bb9a8faac71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966586"
---
# <a name="object-version-attribute"></a><span data-ttu-id="76af8-105">Object-Version 屬性</span><span class="sxs-lookup"><span data-stu-id="76af8-105">Object-Version attribute</span></span>

<span data-ttu-id="76af8-106">這可以用來儲存物件的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="76af8-106">This can be used to store a version number for the object.</span></span>



| <span data-ttu-id="76af8-107">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-107">Entry</span></span> | <span data-ttu-id="76af8-108">值</span><span class="sxs-lookup"><span data-stu-id="76af8-108">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="76af8-109">CN</span><span class="sxs-lookup"><span data-stu-id="76af8-109">CN</span></span>                | <span data-ttu-id="76af8-110">Object-Version</span><span class="sxs-lookup"><span data-stu-id="76af8-110">Object-Version</span></span>                                                 |
| <span data-ttu-id="76af8-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="76af8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="76af8-112">objectVersion</span><span class="sxs-lookup"><span data-stu-id="76af8-112">objectVersion</span></span>                                                  |
| <span data-ttu-id="76af8-113">大小</span><span class="sxs-lookup"><span data-stu-id="76af8-113">Size</span></span>              | <span data-ttu-id="76af8-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="76af8-114">4 bytes</span></span>                                                        |
| <span data-ttu-id="76af8-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="76af8-115">Update Privilege</span></span>  | <span data-ttu-id="76af8-116">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="76af8-116">The designer of the object would set this value.</span></span>               |
| <span data-ttu-id="76af8-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="76af8-117">Update Frequency</span></span>  | <span data-ttu-id="76af8-118">每次物件變更時，這個值就會遞增。</span><span class="sxs-lookup"><span data-stu-id="76af8-118">This value should be incremented each time the object changes.</span></span> |
| <span data-ttu-id="76af8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-119">Attribute-Id</span></span>      | <span data-ttu-id="76af8-120">1.2.840.113556.1.2.76</span><span class="sxs-lookup"><span data-stu-id="76af8-120">1.2.840.113556.1.2.76</span></span>                                          |
| <span data-ttu-id="76af8-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="76af8-121">System-Id-Guid</span></span>    | <span data-ttu-id="76af8-122">16775848-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="76af8-122">16775848-47f3-11d1-a9c3-0000f80367c1</span></span>                           |
| <span data-ttu-id="76af8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="76af8-123">Syntax</span></span>            | [<span data-ttu-id="76af8-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="76af8-124">**Enumeration**</span></span>](s-enumeration.md)                           |



## <a name="implementations"></a><span data-ttu-id="76af8-125">實作</span><span class="sxs-lookup"><span data-stu-id="76af8-125">Implementations</span></span>

-   [<span data-ttu-id="76af8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="76af8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="76af8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="76af8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="76af8-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="76af8-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="76af8-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="76af8-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="76af8-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="76af8-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="76af8-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="76af8-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="76af8-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="76af8-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="76af8-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="76af8-133">Windows 2000 Server</span></span>



| <span data-ttu-id="76af8-134">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-134">Entry</span></span> | <span data-ttu-id="76af8-135">值</span><span class="sxs-lookup"><span data-stu-id="76af8-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76af8-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76af8-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76af8-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-137">MAPI-Id</span></span>                | <span data-ttu-id="76af8-138">0x80F7</span><span class="sxs-lookup"><span data-stu-id="76af8-138">0x80F7</span></span>                          |
| <span data-ttu-id="76af8-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="76af8-139">System-Only</span></span>            | <span data-ttu-id="76af8-140">否</span><span class="sxs-lookup"><span data-stu-id="76af8-140">False</span></span>                           |
| <span data-ttu-id="76af8-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76af8-141">Is-Single-Valued</span></span>       | <span data-ttu-id="76af8-142">對</span><span class="sxs-lookup"><span data-stu-id="76af8-142">True</span></span>                            |
| <span data-ttu-id="76af8-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76af8-143">Is Indexed</span></span>             | <span data-ttu-id="76af8-144">否</span><span class="sxs-lookup"><span data-stu-id="76af8-144">False</span></span>                           |
| <span data-ttu-id="76af8-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76af8-145">In Global Catalog</span></span>      | <span data-ttu-id="76af8-146">否</span><span class="sxs-lookup"><span data-stu-id="76af8-146">False</span></span>                           |
| <span data-ttu-id="76af8-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76af8-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="76af8-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76af8-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76af8-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76af8-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76af8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76af8-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76af8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-151">Search-Flags</span></span>           | <span data-ttu-id="76af8-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76af8-152">0x00000000</span></span>                      |
| <span data-ttu-id="76af8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-153">System-Flags</span></span>           | <span data-ttu-id="76af8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76af8-154">0x00000010</span></span>                      |
| <span data-ttu-id="76af8-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76af8-155">Classes used in</span></span>        | [<span data-ttu-id="76af8-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76af8-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="76af8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76af8-157">Windows Server 2003</span></span>



| <span data-ttu-id="76af8-158">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-158">Entry</span></span> | <span data-ttu-id="76af8-159">值</span><span class="sxs-lookup"><span data-stu-id="76af8-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76af8-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76af8-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76af8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-161">MAPI-Id</span></span>                | <span data-ttu-id="76af8-162">0x80F7</span><span class="sxs-lookup"><span data-stu-id="76af8-162">0x80F7</span></span>                          |
| <span data-ttu-id="76af8-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="76af8-163">System-Only</span></span>            | <span data-ttu-id="76af8-164">否</span><span class="sxs-lookup"><span data-stu-id="76af8-164">False</span></span>                           |
| <span data-ttu-id="76af8-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76af8-165">Is-Single-Valued</span></span>       | <span data-ttu-id="76af8-166">對</span><span class="sxs-lookup"><span data-stu-id="76af8-166">True</span></span>                            |
| <span data-ttu-id="76af8-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76af8-167">Is Indexed</span></span>             | <span data-ttu-id="76af8-168">否</span><span class="sxs-lookup"><span data-stu-id="76af8-168">False</span></span>                           |
| <span data-ttu-id="76af8-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76af8-169">In Global Catalog</span></span>      | <span data-ttu-id="76af8-170">否</span><span class="sxs-lookup"><span data-stu-id="76af8-170">False</span></span>                           |
| <span data-ttu-id="76af8-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76af8-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="76af8-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76af8-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76af8-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76af8-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76af8-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76af8-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76af8-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-175">Search-Flags</span></span>           | <span data-ttu-id="76af8-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76af8-176">0x00000000</span></span>                      |
| <span data-ttu-id="76af8-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-177">System-Flags</span></span>           | <span data-ttu-id="76af8-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76af8-178">0x00000010</span></span>                      |
| <span data-ttu-id="76af8-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76af8-179">Classes used in</span></span>        | [<span data-ttu-id="76af8-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76af8-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="76af8-181">亞當</span><span class="sxs-lookup"><span data-stu-id="76af8-181">ADAM</span></span>



| <span data-ttu-id="76af8-182">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-182">Entry</span></span> | <span data-ttu-id="76af8-183">值</span><span class="sxs-lookup"><span data-stu-id="76af8-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76af8-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76af8-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76af8-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-185">MAPI-Id</span></span>                | <span data-ttu-id="76af8-186">0x80F7</span><span class="sxs-lookup"><span data-stu-id="76af8-186">0x80F7</span></span>                          |
| <span data-ttu-id="76af8-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="76af8-187">System-Only</span></span>            | <span data-ttu-id="76af8-188">否</span><span class="sxs-lookup"><span data-stu-id="76af8-188">False</span></span>                           |
| <span data-ttu-id="76af8-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76af8-189">Is-Single-Valued</span></span>       | <span data-ttu-id="76af8-190">對</span><span class="sxs-lookup"><span data-stu-id="76af8-190">True</span></span>                            |
| <span data-ttu-id="76af8-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76af8-191">Is Indexed</span></span>             | <span data-ttu-id="76af8-192">否</span><span class="sxs-lookup"><span data-stu-id="76af8-192">False</span></span>                           |
| <span data-ttu-id="76af8-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76af8-193">In Global Catalog</span></span>      | <span data-ttu-id="76af8-194">否</span><span class="sxs-lookup"><span data-stu-id="76af8-194">False</span></span>                           |
| <span data-ttu-id="76af8-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76af8-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="76af8-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76af8-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76af8-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76af8-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76af8-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76af8-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76af8-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-199">Search-Flags</span></span>           | <span data-ttu-id="76af8-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76af8-200">0x00000000</span></span>                      |
| <span data-ttu-id="76af8-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-201">System-Flags</span></span>           | <span data-ttu-id="76af8-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76af8-202">0x00000010</span></span>                      |
| <span data-ttu-id="76af8-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76af8-203">Classes used in</span></span>        | [<span data-ttu-id="76af8-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76af8-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="76af8-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="76af8-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="76af8-206">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-206">Entry</span></span> | <span data-ttu-id="76af8-207">值</span><span class="sxs-lookup"><span data-stu-id="76af8-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76af8-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76af8-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76af8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-209">MAPI-Id</span></span>                | <span data-ttu-id="76af8-210">0x80F7</span><span class="sxs-lookup"><span data-stu-id="76af8-210">0x80F7</span></span>                          |
| <span data-ttu-id="76af8-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="76af8-211">System-Only</span></span>            | <span data-ttu-id="76af8-212">否</span><span class="sxs-lookup"><span data-stu-id="76af8-212">False</span></span>                           |
| <span data-ttu-id="76af8-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76af8-213">Is-Single-Valued</span></span>       | <span data-ttu-id="76af8-214">對</span><span class="sxs-lookup"><span data-stu-id="76af8-214">True</span></span>                            |
| <span data-ttu-id="76af8-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76af8-215">Is Indexed</span></span>             | <span data-ttu-id="76af8-216">否</span><span class="sxs-lookup"><span data-stu-id="76af8-216">False</span></span>                           |
| <span data-ttu-id="76af8-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76af8-217">In Global Catalog</span></span>      | <span data-ttu-id="76af8-218">否</span><span class="sxs-lookup"><span data-stu-id="76af8-218">False</span></span>                           |
| <span data-ttu-id="76af8-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76af8-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="76af8-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76af8-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76af8-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76af8-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76af8-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76af8-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76af8-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-223">Search-Flags</span></span>           | <span data-ttu-id="76af8-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76af8-224">0x00000000</span></span>                      |
| <span data-ttu-id="76af8-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-225">System-Flags</span></span>           | <span data-ttu-id="76af8-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76af8-226">0x00000010</span></span>                      |
| <span data-ttu-id="76af8-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76af8-227">Classes used in</span></span>        | [<span data-ttu-id="76af8-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76af8-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="76af8-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76af8-229">Windows Server 2008</span></span>



| <span data-ttu-id="76af8-230">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-230">Entry</span></span> | <span data-ttu-id="76af8-231">值</span><span class="sxs-lookup"><span data-stu-id="76af8-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76af8-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76af8-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76af8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-233">MAPI-Id</span></span>                | <span data-ttu-id="76af8-234">0x80F7</span><span class="sxs-lookup"><span data-stu-id="76af8-234">0x80F7</span></span>                          |
| <span data-ttu-id="76af8-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="76af8-235">System-Only</span></span>            | <span data-ttu-id="76af8-236">否</span><span class="sxs-lookup"><span data-stu-id="76af8-236">False</span></span>                           |
| <span data-ttu-id="76af8-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76af8-237">Is-Single-Valued</span></span>       | <span data-ttu-id="76af8-238">對</span><span class="sxs-lookup"><span data-stu-id="76af8-238">True</span></span>                            |
| <span data-ttu-id="76af8-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76af8-239">Is Indexed</span></span>             | <span data-ttu-id="76af8-240">否</span><span class="sxs-lookup"><span data-stu-id="76af8-240">False</span></span>                           |
| <span data-ttu-id="76af8-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76af8-241">In Global Catalog</span></span>      | <span data-ttu-id="76af8-242">否</span><span class="sxs-lookup"><span data-stu-id="76af8-242">False</span></span>                           |
| <span data-ttu-id="76af8-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76af8-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="76af8-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76af8-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76af8-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76af8-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76af8-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76af8-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76af8-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-247">Search-Flags</span></span>           | <span data-ttu-id="76af8-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76af8-248">0x00000000</span></span>                      |
| <span data-ttu-id="76af8-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-249">System-Flags</span></span>           | <span data-ttu-id="76af8-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76af8-250">0x00000010</span></span>                      |
| <span data-ttu-id="76af8-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76af8-251">Classes used in</span></span>        | [<span data-ttu-id="76af8-252">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76af8-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="76af8-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76af8-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="76af8-254">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-254">Entry</span></span> | <span data-ttu-id="76af8-255">值</span><span class="sxs-lookup"><span data-stu-id="76af8-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76af8-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76af8-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76af8-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-257">MAPI-Id</span></span>                | <span data-ttu-id="76af8-258">0x80F7</span><span class="sxs-lookup"><span data-stu-id="76af8-258">0x80F7</span></span>                          |
| <span data-ttu-id="76af8-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="76af8-259">System-Only</span></span>            | <span data-ttu-id="76af8-260">否</span><span class="sxs-lookup"><span data-stu-id="76af8-260">False</span></span>                           |
| <span data-ttu-id="76af8-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76af8-261">Is-Single-Valued</span></span>       | <span data-ttu-id="76af8-262">對</span><span class="sxs-lookup"><span data-stu-id="76af8-262">True</span></span>                            |
| <span data-ttu-id="76af8-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76af8-263">Is Indexed</span></span>             | <span data-ttu-id="76af8-264">否</span><span class="sxs-lookup"><span data-stu-id="76af8-264">False</span></span>                           |
| <span data-ttu-id="76af8-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76af8-265">In Global Catalog</span></span>      | <span data-ttu-id="76af8-266">否</span><span class="sxs-lookup"><span data-stu-id="76af8-266">False</span></span>                           |
| <span data-ttu-id="76af8-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76af8-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="76af8-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76af8-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76af8-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76af8-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76af8-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76af8-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76af8-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-271">Search-Flags</span></span>           | <span data-ttu-id="76af8-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76af8-272">0x00000000</span></span>                      |
| <span data-ttu-id="76af8-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-273">System-Flags</span></span>           | <span data-ttu-id="76af8-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76af8-274">0x00000010</span></span>                      |
| <span data-ttu-id="76af8-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76af8-275">Classes used in</span></span>        | [<span data-ttu-id="76af8-276">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76af8-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="76af8-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76af8-277">Windows Server 2012</span></span>



| <span data-ttu-id="76af8-278">進入</span><span class="sxs-lookup"><span data-stu-id="76af8-278">Entry</span></span> | <span data-ttu-id="76af8-279">值</span><span class="sxs-lookup"><span data-stu-id="76af8-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76af8-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76af8-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76af8-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76af8-281">MAPI-Id</span></span>                | <span data-ttu-id="76af8-282">0x80F7</span><span class="sxs-lookup"><span data-stu-id="76af8-282">0x80F7</span></span>                          |
| <span data-ttu-id="76af8-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="76af8-283">System-Only</span></span>            | <span data-ttu-id="76af8-284">否</span><span class="sxs-lookup"><span data-stu-id="76af8-284">False</span></span>                           |
| <span data-ttu-id="76af8-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76af8-285">Is-Single-Valued</span></span>       | <span data-ttu-id="76af8-286">對</span><span class="sxs-lookup"><span data-stu-id="76af8-286">True</span></span>                            |
| <span data-ttu-id="76af8-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76af8-287">Is Indexed</span></span>             | <span data-ttu-id="76af8-288">否</span><span class="sxs-lookup"><span data-stu-id="76af8-288">False</span></span>                           |
| <span data-ttu-id="76af8-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76af8-289">In Global Catalog</span></span>      | <span data-ttu-id="76af8-290">否</span><span class="sxs-lookup"><span data-stu-id="76af8-290">False</span></span>                           |
| <span data-ttu-id="76af8-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76af8-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="76af8-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76af8-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76af8-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76af8-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76af8-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76af8-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76af8-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-295">Search-Flags</span></span>           | <span data-ttu-id="76af8-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76af8-296">0x00000000</span></span>                      |
| <span data-ttu-id="76af8-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76af8-297">System-Flags</span></span>           | <span data-ttu-id="76af8-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76af8-298">0x00000010</span></span>                      |
| <span data-ttu-id="76af8-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76af8-299">Classes used in</span></span>        | [<span data-ttu-id="76af8-300">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76af8-300">**Top**</span></span>](c-top.md)<br/> |



 

 





