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
# <a name="when-changed-attribute"></a><span data-ttu-id="0157a-106">When-Changed 屬性</span><span class="sxs-lookup"><span data-stu-id="0157a-106">When-Changed attribute</span></span>

<span data-ttu-id="0157a-107">上次變更此物件的日期。</span><span class="sxs-lookup"><span data-stu-id="0157a-107">The date when this object was last changed.</span></span> <span data-ttu-id="0157a-108">此值不會複寫，而且存在於通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="0157a-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="0157a-109">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-109">Entry</span></span> | <span data-ttu-id="0157a-110">值</span><span class="sxs-lookup"><span data-stu-id="0157a-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="0157a-111">CN</span><span class="sxs-lookup"><span data-stu-id="0157a-111">CN</span></span>                | <span data-ttu-id="0157a-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="0157a-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="0157a-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0157a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0157a-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="0157a-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="0157a-115">大小</span><span class="sxs-lookup"><span data-stu-id="0157a-115">Size</span></span>              | <span data-ttu-id="0157a-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="0157a-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="0157a-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0157a-117">Update Privilege</span></span>  | <span data-ttu-id="0157a-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0157a-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="0157a-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0157a-119">Update Frequency</span></span>  | <span data-ttu-id="0157a-120">每次物件變更時。</span><span class="sxs-lookup"><span data-stu-id="0157a-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="0157a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-121">Attribute-Id</span></span>      | <span data-ttu-id="0157a-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="0157a-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="0157a-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0157a-123">System-Id-Guid</span></span>    | <span data-ttu-id="0157a-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0157a-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="0157a-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="0157a-125">Syntax</span></span>            | [<span data-ttu-id="0157a-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="0157a-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="0157a-127">實作</span><span class="sxs-lookup"><span data-stu-id="0157a-127">Implementations</span></span>

-   [<span data-ttu-id="0157a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0157a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0157a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0157a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0157a-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="0157a-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0157a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0157a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0157a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0157a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0157a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0157a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0157a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0157a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0157a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0157a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="0157a-136">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-136">Entry</span></span> | <span data-ttu-id="0157a-137">值</span><span class="sxs-lookup"><span data-stu-id="0157a-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0157a-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0157a-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0157a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-139">MAPI-Id</span></span>                | <span data-ttu-id="0157a-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="0157a-140">0x3008</span></span>                          |
| <span data-ttu-id="0157a-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="0157a-141">System-Only</span></span>            | <span data-ttu-id="0157a-142">對</span><span class="sxs-lookup"><span data-stu-id="0157a-142">True</span></span>                            |
| <span data-ttu-id="0157a-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0157a-143">Is-Single-Valued</span></span>       | <span data-ttu-id="0157a-144">對</span><span class="sxs-lookup"><span data-stu-id="0157a-144">True</span></span>                            |
| <span data-ttu-id="0157a-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0157a-145">Is Indexed</span></span>             | <span data-ttu-id="0157a-146">否</span><span class="sxs-lookup"><span data-stu-id="0157a-146">False</span></span>                           |
| <span data-ttu-id="0157a-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0157a-147">In Global Catalog</span></span>      | <span data-ttu-id="0157a-148">對</span><span class="sxs-lookup"><span data-stu-id="0157a-148">True</span></span>                            |
| <span data-ttu-id="0157a-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0157a-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="0157a-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0157a-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0157a-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0157a-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0157a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0157a-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0157a-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-153">Search-Flags</span></span>           | <span data-ttu-id="0157a-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0157a-154">0x00000000</span></span>                      |
| <span data-ttu-id="0157a-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-155">System-Flags</span></span>           | <span data-ttu-id="0157a-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0157a-156">0x00000013</span></span>                      |
| <span data-ttu-id="0157a-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0157a-157">Classes used in</span></span>        | [<span data-ttu-id="0157a-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0157a-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0157a-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0157a-159">Windows Server 2003</span></span>



| <span data-ttu-id="0157a-160">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-160">Entry</span></span> | <span data-ttu-id="0157a-161">值</span><span class="sxs-lookup"><span data-stu-id="0157a-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0157a-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0157a-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0157a-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-163">MAPI-Id</span></span>                | <span data-ttu-id="0157a-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="0157a-164">0x3008</span></span>                          |
| <span data-ttu-id="0157a-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="0157a-165">System-Only</span></span>            | <span data-ttu-id="0157a-166">對</span><span class="sxs-lookup"><span data-stu-id="0157a-166">True</span></span>                            |
| <span data-ttu-id="0157a-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0157a-167">Is-Single-Valued</span></span>       | <span data-ttu-id="0157a-168">對</span><span class="sxs-lookup"><span data-stu-id="0157a-168">True</span></span>                            |
| <span data-ttu-id="0157a-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0157a-169">Is Indexed</span></span>             | <span data-ttu-id="0157a-170">否</span><span class="sxs-lookup"><span data-stu-id="0157a-170">False</span></span>                           |
| <span data-ttu-id="0157a-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0157a-171">In Global Catalog</span></span>      | <span data-ttu-id="0157a-172">對</span><span class="sxs-lookup"><span data-stu-id="0157a-172">True</span></span>                            |
| <span data-ttu-id="0157a-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0157a-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="0157a-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0157a-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0157a-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0157a-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0157a-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0157a-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0157a-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-177">Search-Flags</span></span>           | <span data-ttu-id="0157a-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0157a-178">0x00000000</span></span>                      |
| <span data-ttu-id="0157a-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-179">System-Flags</span></span>           | <span data-ttu-id="0157a-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0157a-180">0x00000013</span></span>                      |
| <span data-ttu-id="0157a-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0157a-181">Classes used in</span></span>        | [<span data-ttu-id="0157a-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0157a-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0157a-183">亞當</span><span class="sxs-lookup"><span data-stu-id="0157a-183">ADAM</span></span>



| <span data-ttu-id="0157a-184">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-184">Entry</span></span> | <span data-ttu-id="0157a-185">值</span><span class="sxs-lookup"><span data-stu-id="0157a-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0157a-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0157a-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0157a-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-187">MAPI-Id</span></span>                | <span data-ttu-id="0157a-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="0157a-188">0x3008</span></span>                          |
| <span data-ttu-id="0157a-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="0157a-189">System-Only</span></span>            | <span data-ttu-id="0157a-190">對</span><span class="sxs-lookup"><span data-stu-id="0157a-190">True</span></span>                            |
| <span data-ttu-id="0157a-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0157a-191">Is-Single-Valued</span></span>       | <span data-ttu-id="0157a-192">對</span><span class="sxs-lookup"><span data-stu-id="0157a-192">True</span></span>                            |
| <span data-ttu-id="0157a-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0157a-193">Is Indexed</span></span>             | <span data-ttu-id="0157a-194">否</span><span class="sxs-lookup"><span data-stu-id="0157a-194">False</span></span>                           |
| <span data-ttu-id="0157a-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0157a-195">In Global Catalog</span></span>      | <span data-ttu-id="0157a-196">對</span><span class="sxs-lookup"><span data-stu-id="0157a-196">True</span></span>                            |
| <span data-ttu-id="0157a-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0157a-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="0157a-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0157a-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0157a-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0157a-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0157a-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0157a-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0157a-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-201">Search-Flags</span></span>           | <span data-ttu-id="0157a-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0157a-202">0x00000000</span></span>                      |
| <span data-ttu-id="0157a-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-203">System-Flags</span></span>           | <span data-ttu-id="0157a-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0157a-204">0x00000013</span></span>                      |
| <span data-ttu-id="0157a-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0157a-205">Classes used in</span></span>        | [<span data-ttu-id="0157a-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0157a-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0157a-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0157a-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0157a-208">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-208">Entry</span></span> | <span data-ttu-id="0157a-209">值</span><span class="sxs-lookup"><span data-stu-id="0157a-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0157a-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0157a-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0157a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-211">MAPI-Id</span></span>                | <span data-ttu-id="0157a-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="0157a-212">0x3008</span></span>                          |
| <span data-ttu-id="0157a-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="0157a-213">System-Only</span></span>            | <span data-ttu-id="0157a-214">對</span><span class="sxs-lookup"><span data-stu-id="0157a-214">True</span></span>                            |
| <span data-ttu-id="0157a-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0157a-215">Is-Single-Valued</span></span>       | <span data-ttu-id="0157a-216">對</span><span class="sxs-lookup"><span data-stu-id="0157a-216">True</span></span>                            |
| <span data-ttu-id="0157a-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0157a-217">Is Indexed</span></span>             | <span data-ttu-id="0157a-218">否</span><span class="sxs-lookup"><span data-stu-id="0157a-218">False</span></span>                           |
| <span data-ttu-id="0157a-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0157a-219">In Global Catalog</span></span>      | <span data-ttu-id="0157a-220">對</span><span class="sxs-lookup"><span data-stu-id="0157a-220">True</span></span>                            |
| <span data-ttu-id="0157a-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0157a-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="0157a-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0157a-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0157a-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0157a-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0157a-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0157a-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0157a-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-225">Search-Flags</span></span>           | <span data-ttu-id="0157a-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0157a-226">0x00000000</span></span>                      |
| <span data-ttu-id="0157a-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-227">System-Flags</span></span>           | <span data-ttu-id="0157a-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0157a-228">0x00000013</span></span>                      |
| <span data-ttu-id="0157a-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0157a-229">Classes used in</span></span>        | [<span data-ttu-id="0157a-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0157a-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0157a-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0157a-231">Windows Server 2008</span></span>



| <span data-ttu-id="0157a-232">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-232">Entry</span></span> | <span data-ttu-id="0157a-233">值</span><span class="sxs-lookup"><span data-stu-id="0157a-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0157a-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0157a-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0157a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-235">MAPI-Id</span></span>                | <span data-ttu-id="0157a-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="0157a-236">0x3008</span></span>                          |
| <span data-ttu-id="0157a-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="0157a-237">System-Only</span></span>            | <span data-ttu-id="0157a-238">對</span><span class="sxs-lookup"><span data-stu-id="0157a-238">True</span></span>                            |
| <span data-ttu-id="0157a-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0157a-239">Is-Single-Valued</span></span>       | <span data-ttu-id="0157a-240">對</span><span class="sxs-lookup"><span data-stu-id="0157a-240">True</span></span>                            |
| <span data-ttu-id="0157a-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0157a-241">Is Indexed</span></span>             | <span data-ttu-id="0157a-242">否</span><span class="sxs-lookup"><span data-stu-id="0157a-242">False</span></span>                           |
| <span data-ttu-id="0157a-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0157a-243">In Global Catalog</span></span>      | <span data-ttu-id="0157a-244">對</span><span class="sxs-lookup"><span data-stu-id="0157a-244">True</span></span>                            |
| <span data-ttu-id="0157a-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0157a-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="0157a-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0157a-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0157a-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0157a-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0157a-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0157a-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0157a-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-249">Search-Flags</span></span>           | <span data-ttu-id="0157a-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0157a-250">0x00000000</span></span>                      |
| <span data-ttu-id="0157a-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-251">System-Flags</span></span>           | <span data-ttu-id="0157a-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0157a-252">0x00000013</span></span>                      |
| <span data-ttu-id="0157a-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0157a-253">Classes used in</span></span>        | [<span data-ttu-id="0157a-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0157a-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0157a-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0157a-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0157a-256">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-256">Entry</span></span> | <span data-ttu-id="0157a-257">值</span><span class="sxs-lookup"><span data-stu-id="0157a-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0157a-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0157a-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0157a-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-259">MAPI-Id</span></span>                | <span data-ttu-id="0157a-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="0157a-260">0x3008</span></span>                          |
| <span data-ttu-id="0157a-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="0157a-261">System-Only</span></span>            | <span data-ttu-id="0157a-262">對</span><span class="sxs-lookup"><span data-stu-id="0157a-262">True</span></span>                            |
| <span data-ttu-id="0157a-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0157a-263">Is-Single-Valued</span></span>       | <span data-ttu-id="0157a-264">對</span><span class="sxs-lookup"><span data-stu-id="0157a-264">True</span></span>                            |
| <span data-ttu-id="0157a-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0157a-265">Is Indexed</span></span>             | <span data-ttu-id="0157a-266">否</span><span class="sxs-lookup"><span data-stu-id="0157a-266">False</span></span>                           |
| <span data-ttu-id="0157a-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0157a-267">In Global Catalog</span></span>      | <span data-ttu-id="0157a-268">對</span><span class="sxs-lookup"><span data-stu-id="0157a-268">True</span></span>                            |
| <span data-ttu-id="0157a-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0157a-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="0157a-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0157a-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0157a-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0157a-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0157a-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0157a-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0157a-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-273">Search-Flags</span></span>           | <span data-ttu-id="0157a-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0157a-274">0x00000000</span></span>                      |
| <span data-ttu-id="0157a-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-275">System-Flags</span></span>           | <span data-ttu-id="0157a-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0157a-276">0x00000013</span></span>                      |
| <span data-ttu-id="0157a-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0157a-277">Classes used in</span></span>        | [<span data-ttu-id="0157a-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0157a-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0157a-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0157a-279">Windows Server 2012</span></span>



| <span data-ttu-id="0157a-280">進入</span><span class="sxs-lookup"><span data-stu-id="0157a-280">Entry</span></span> | <span data-ttu-id="0157a-281">值</span><span class="sxs-lookup"><span data-stu-id="0157a-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0157a-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0157a-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0157a-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0157a-283">MAPI-Id</span></span>                | <span data-ttu-id="0157a-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="0157a-284">0x3008</span></span>                          |
| <span data-ttu-id="0157a-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="0157a-285">System-Only</span></span>            | <span data-ttu-id="0157a-286">對</span><span class="sxs-lookup"><span data-stu-id="0157a-286">True</span></span>                            |
| <span data-ttu-id="0157a-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0157a-287">Is-Single-Valued</span></span>       | <span data-ttu-id="0157a-288">對</span><span class="sxs-lookup"><span data-stu-id="0157a-288">True</span></span>                            |
| <span data-ttu-id="0157a-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0157a-289">Is Indexed</span></span>             | <span data-ttu-id="0157a-290">否</span><span class="sxs-lookup"><span data-stu-id="0157a-290">False</span></span>                           |
| <span data-ttu-id="0157a-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0157a-291">In Global Catalog</span></span>      | <span data-ttu-id="0157a-292">對</span><span class="sxs-lookup"><span data-stu-id="0157a-292">True</span></span>                            |
| <span data-ttu-id="0157a-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0157a-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="0157a-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0157a-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0157a-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0157a-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0157a-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0157a-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0157a-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-297">Search-Flags</span></span>           | <span data-ttu-id="0157a-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0157a-298">0x00000000</span></span>                      |
| <span data-ttu-id="0157a-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0157a-299">System-Flags</span></span>           | <span data-ttu-id="0157a-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0157a-300">0x00000013</span></span>                      |
| <span data-ttu-id="0157a-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0157a-301">Classes used in</span></span>        | [<span data-ttu-id="0157a-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0157a-302">**Top**</span></span>](c-top.md)<br/> |



 

 





