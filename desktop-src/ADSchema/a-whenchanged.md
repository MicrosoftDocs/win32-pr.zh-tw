---
title: When-Changed 屬性
description: 上次變更此物件的日期。 此值不會複寫，而且存在於通用類別目錄中。
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- When-Changed 屬性 AD 架構
- whenChanged 屬性 AD 架構
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844539"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="e2522-106">When-Changed 屬性</span><span class="sxs-lookup"><span data-stu-id="e2522-106">When-Changed attribute</span></span>

<span data-ttu-id="e2522-107">上次變更此物件的日期。</span><span class="sxs-lookup"><span data-stu-id="e2522-107">The date when this object was last changed.</span></span> <span data-ttu-id="e2522-108">此值不會複寫，而且存在於通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="e2522-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="e2522-109">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-109">Entry</span></span> | <span data-ttu-id="e2522-110">值</span><span class="sxs-lookup"><span data-stu-id="e2522-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="e2522-111">CN</span><span class="sxs-lookup"><span data-stu-id="e2522-111">CN</span></span>                | <span data-ttu-id="e2522-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="e2522-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="e2522-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e2522-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e2522-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="e2522-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="e2522-115">大小</span><span class="sxs-lookup"><span data-stu-id="e2522-115">Size</span></span>              | <span data-ttu-id="e2522-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="e2522-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="e2522-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e2522-117">Update Privilege</span></span>  | <span data-ttu-id="e2522-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="e2522-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="e2522-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e2522-119">Update Frequency</span></span>  | <span data-ttu-id="e2522-120">每次物件變更時。</span><span class="sxs-lookup"><span data-stu-id="e2522-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="e2522-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-121">Attribute-Id</span></span>      | <span data-ttu-id="e2522-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="e2522-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="e2522-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e2522-123">System-Id-Guid</span></span>    | <span data-ttu-id="e2522-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e2522-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="e2522-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2522-125">Syntax</span></span>            | [<span data-ttu-id="e2522-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="e2522-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="e2522-127">實作</span><span class="sxs-lookup"><span data-stu-id="e2522-127">Implementations</span></span>

-   [<span data-ttu-id="e2522-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e2522-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e2522-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e2522-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e2522-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e2522-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e2522-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e2522-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e2522-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e2522-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e2522-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e2522-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e2522-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e2522-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e2522-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2522-135">Windows 2000 Server</span></span>



| <span data-ttu-id="e2522-136">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-136">Entry</span></span> | <span data-ttu-id="e2522-137">值</span><span class="sxs-lookup"><span data-stu-id="e2522-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e2522-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2522-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e2522-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-139">MAPI-Id</span></span>                | <span data-ttu-id="e2522-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="e2522-140">0x3008</span></span>                          |
| <span data-ttu-id="e2522-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2522-141">System-Only</span></span>            | <span data-ttu-id="e2522-142">對</span><span class="sxs-lookup"><span data-stu-id="e2522-142">True</span></span>                            |
| <span data-ttu-id="e2522-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2522-143">Is-Single-Valued</span></span>       | <span data-ttu-id="e2522-144">對</span><span class="sxs-lookup"><span data-stu-id="e2522-144">True</span></span>                            |
| <span data-ttu-id="e2522-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2522-145">Is Indexed</span></span>             | <span data-ttu-id="e2522-146">否</span><span class="sxs-lookup"><span data-stu-id="e2522-146">False</span></span>                           |
| <span data-ttu-id="e2522-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2522-147">In Global Catalog</span></span>      | <span data-ttu-id="e2522-148">對</span><span class="sxs-lookup"><span data-stu-id="e2522-148">True</span></span>                            |
| <span data-ttu-id="e2522-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2522-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2522-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2522-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e2522-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2522-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e2522-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2522-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e2522-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-153">Search-Flags</span></span>           | <span data-ttu-id="e2522-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2522-154">0x00000000</span></span>                      |
| <span data-ttu-id="e2522-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-155">System-Flags</span></span>           | <span data-ttu-id="e2522-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e2522-156">0x00000013</span></span>                      |
| <span data-ttu-id="e2522-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2522-157">Classes used in</span></span>        | [<span data-ttu-id="e2522-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e2522-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e2522-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2522-159">Windows Server 2003</span></span>



| <span data-ttu-id="e2522-160">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-160">Entry</span></span> | <span data-ttu-id="e2522-161">值</span><span class="sxs-lookup"><span data-stu-id="e2522-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e2522-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2522-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e2522-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-163">MAPI-Id</span></span>                | <span data-ttu-id="e2522-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="e2522-164">0x3008</span></span>                          |
| <span data-ttu-id="e2522-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2522-165">System-Only</span></span>            | <span data-ttu-id="e2522-166">對</span><span class="sxs-lookup"><span data-stu-id="e2522-166">True</span></span>                            |
| <span data-ttu-id="e2522-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2522-167">Is-Single-Valued</span></span>       | <span data-ttu-id="e2522-168">對</span><span class="sxs-lookup"><span data-stu-id="e2522-168">True</span></span>                            |
| <span data-ttu-id="e2522-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2522-169">Is Indexed</span></span>             | <span data-ttu-id="e2522-170">否</span><span class="sxs-lookup"><span data-stu-id="e2522-170">False</span></span>                           |
| <span data-ttu-id="e2522-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2522-171">In Global Catalog</span></span>      | <span data-ttu-id="e2522-172">對</span><span class="sxs-lookup"><span data-stu-id="e2522-172">True</span></span>                            |
| <span data-ttu-id="e2522-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2522-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2522-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2522-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e2522-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2522-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e2522-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2522-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e2522-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-177">Search-Flags</span></span>           | <span data-ttu-id="e2522-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2522-178">0x00000000</span></span>                      |
| <span data-ttu-id="e2522-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-179">System-Flags</span></span>           | <span data-ttu-id="e2522-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e2522-180">0x00000013</span></span>                      |
| <span data-ttu-id="e2522-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2522-181">Classes used in</span></span>        | [<span data-ttu-id="e2522-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e2522-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e2522-183">亞當</span><span class="sxs-lookup"><span data-stu-id="e2522-183">ADAM</span></span>



| <span data-ttu-id="e2522-184">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-184">Entry</span></span> | <span data-ttu-id="e2522-185">值</span><span class="sxs-lookup"><span data-stu-id="e2522-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e2522-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2522-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e2522-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-187">MAPI-Id</span></span>                | <span data-ttu-id="e2522-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="e2522-188">0x3008</span></span>                          |
| <span data-ttu-id="e2522-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2522-189">System-Only</span></span>            | <span data-ttu-id="e2522-190">對</span><span class="sxs-lookup"><span data-stu-id="e2522-190">True</span></span>                            |
| <span data-ttu-id="e2522-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2522-191">Is-Single-Valued</span></span>       | <span data-ttu-id="e2522-192">對</span><span class="sxs-lookup"><span data-stu-id="e2522-192">True</span></span>                            |
| <span data-ttu-id="e2522-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2522-193">Is Indexed</span></span>             | <span data-ttu-id="e2522-194">否</span><span class="sxs-lookup"><span data-stu-id="e2522-194">False</span></span>                           |
| <span data-ttu-id="e2522-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2522-195">In Global Catalog</span></span>      | <span data-ttu-id="e2522-196">對</span><span class="sxs-lookup"><span data-stu-id="e2522-196">True</span></span>                            |
| <span data-ttu-id="e2522-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2522-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2522-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2522-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e2522-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2522-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e2522-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2522-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e2522-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-201">Search-Flags</span></span>           | <span data-ttu-id="e2522-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2522-202">0x00000000</span></span>                      |
| <span data-ttu-id="e2522-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-203">System-Flags</span></span>           | <span data-ttu-id="e2522-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e2522-204">0x00000013</span></span>                      |
| <span data-ttu-id="e2522-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2522-205">Classes used in</span></span>        | [<span data-ttu-id="e2522-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e2522-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e2522-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e2522-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e2522-208">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-208">Entry</span></span> | <span data-ttu-id="e2522-209">值</span><span class="sxs-lookup"><span data-stu-id="e2522-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e2522-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2522-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e2522-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-211">MAPI-Id</span></span>                | <span data-ttu-id="e2522-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="e2522-212">0x3008</span></span>                          |
| <span data-ttu-id="e2522-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2522-213">System-Only</span></span>            | <span data-ttu-id="e2522-214">對</span><span class="sxs-lookup"><span data-stu-id="e2522-214">True</span></span>                            |
| <span data-ttu-id="e2522-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2522-215">Is-Single-Valued</span></span>       | <span data-ttu-id="e2522-216">對</span><span class="sxs-lookup"><span data-stu-id="e2522-216">True</span></span>                            |
| <span data-ttu-id="e2522-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2522-217">Is Indexed</span></span>             | <span data-ttu-id="e2522-218">否</span><span class="sxs-lookup"><span data-stu-id="e2522-218">False</span></span>                           |
| <span data-ttu-id="e2522-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2522-219">In Global Catalog</span></span>      | <span data-ttu-id="e2522-220">對</span><span class="sxs-lookup"><span data-stu-id="e2522-220">True</span></span>                            |
| <span data-ttu-id="e2522-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2522-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2522-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2522-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e2522-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2522-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e2522-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2522-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e2522-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-225">Search-Flags</span></span>           | <span data-ttu-id="e2522-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2522-226">0x00000000</span></span>                      |
| <span data-ttu-id="e2522-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-227">System-Flags</span></span>           | <span data-ttu-id="e2522-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e2522-228">0x00000013</span></span>                      |
| <span data-ttu-id="e2522-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2522-229">Classes used in</span></span>        | [<span data-ttu-id="e2522-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e2522-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e2522-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2522-231">Windows Server 2008</span></span>



| <span data-ttu-id="e2522-232">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-232">Entry</span></span> | <span data-ttu-id="e2522-233">值</span><span class="sxs-lookup"><span data-stu-id="e2522-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e2522-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2522-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e2522-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-235">MAPI-Id</span></span>                | <span data-ttu-id="e2522-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="e2522-236">0x3008</span></span>                          |
| <span data-ttu-id="e2522-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2522-237">System-Only</span></span>            | <span data-ttu-id="e2522-238">對</span><span class="sxs-lookup"><span data-stu-id="e2522-238">True</span></span>                            |
| <span data-ttu-id="e2522-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2522-239">Is-Single-Valued</span></span>       | <span data-ttu-id="e2522-240">對</span><span class="sxs-lookup"><span data-stu-id="e2522-240">True</span></span>                            |
| <span data-ttu-id="e2522-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2522-241">Is Indexed</span></span>             | <span data-ttu-id="e2522-242">否</span><span class="sxs-lookup"><span data-stu-id="e2522-242">False</span></span>                           |
| <span data-ttu-id="e2522-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2522-243">In Global Catalog</span></span>      | <span data-ttu-id="e2522-244">對</span><span class="sxs-lookup"><span data-stu-id="e2522-244">True</span></span>                            |
| <span data-ttu-id="e2522-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2522-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2522-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2522-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e2522-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2522-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e2522-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2522-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e2522-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-249">Search-Flags</span></span>           | <span data-ttu-id="e2522-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2522-250">0x00000000</span></span>                      |
| <span data-ttu-id="e2522-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-251">System-Flags</span></span>           | <span data-ttu-id="e2522-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e2522-252">0x00000013</span></span>                      |
| <span data-ttu-id="e2522-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2522-253">Classes used in</span></span>        | [<span data-ttu-id="e2522-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e2522-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e2522-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2522-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e2522-256">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-256">Entry</span></span> | <span data-ttu-id="e2522-257">值</span><span class="sxs-lookup"><span data-stu-id="e2522-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e2522-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2522-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e2522-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-259">MAPI-Id</span></span>                | <span data-ttu-id="e2522-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="e2522-260">0x3008</span></span>                          |
| <span data-ttu-id="e2522-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2522-261">System-Only</span></span>            | <span data-ttu-id="e2522-262">對</span><span class="sxs-lookup"><span data-stu-id="e2522-262">True</span></span>                            |
| <span data-ttu-id="e2522-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2522-263">Is-Single-Valued</span></span>       | <span data-ttu-id="e2522-264">對</span><span class="sxs-lookup"><span data-stu-id="e2522-264">True</span></span>                            |
| <span data-ttu-id="e2522-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2522-265">Is Indexed</span></span>             | <span data-ttu-id="e2522-266">否</span><span class="sxs-lookup"><span data-stu-id="e2522-266">False</span></span>                           |
| <span data-ttu-id="e2522-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2522-267">In Global Catalog</span></span>      | <span data-ttu-id="e2522-268">對</span><span class="sxs-lookup"><span data-stu-id="e2522-268">True</span></span>                            |
| <span data-ttu-id="e2522-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2522-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2522-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2522-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e2522-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2522-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e2522-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2522-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e2522-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-273">Search-Flags</span></span>           | <span data-ttu-id="e2522-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2522-274">0x00000000</span></span>                      |
| <span data-ttu-id="e2522-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-275">System-Flags</span></span>           | <span data-ttu-id="e2522-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e2522-276">0x00000013</span></span>                      |
| <span data-ttu-id="e2522-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2522-277">Classes used in</span></span>        | [<span data-ttu-id="e2522-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e2522-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e2522-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2522-279">Windows Server 2012</span></span>



| <span data-ttu-id="e2522-280">進入</span><span class="sxs-lookup"><span data-stu-id="e2522-280">Entry</span></span> | <span data-ttu-id="e2522-281">值</span><span class="sxs-lookup"><span data-stu-id="e2522-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e2522-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2522-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e2522-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2522-283">MAPI-Id</span></span>                | <span data-ttu-id="e2522-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="e2522-284">0x3008</span></span>                          |
| <span data-ttu-id="e2522-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2522-285">System-Only</span></span>            | <span data-ttu-id="e2522-286">對</span><span class="sxs-lookup"><span data-stu-id="e2522-286">True</span></span>                            |
| <span data-ttu-id="e2522-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2522-287">Is-Single-Valued</span></span>       | <span data-ttu-id="e2522-288">對</span><span class="sxs-lookup"><span data-stu-id="e2522-288">True</span></span>                            |
| <span data-ttu-id="e2522-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2522-289">Is Indexed</span></span>             | <span data-ttu-id="e2522-290">否</span><span class="sxs-lookup"><span data-stu-id="e2522-290">False</span></span>                           |
| <span data-ttu-id="e2522-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2522-291">In Global Catalog</span></span>      | <span data-ttu-id="e2522-292">對</span><span class="sxs-lookup"><span data-stu-id="e2522-292">True</span></span>                            |
| <span data-ttu-id="e2522-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2522-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2522-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2522-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e2522-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2522-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e2522-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2522-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e2522-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-297">Search-Flags</span></span>           | <span data-ttu-id="e2522-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2522-298">0x00000000</span></span>                      |
| <span data-ttu-id="e2522-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2522-299">System-Flags</span></span>           | <span data-ttu-id="e2522-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="e2522-300">0x00000013</span></span>                      |
| <span data-ttu-id="e2522-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2522-301">Classes used in</span></span>        | [<span data-ttu-id="e2522-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e2522-302">**Top**</span></span>](c-top.md)<br/> |



 

 





