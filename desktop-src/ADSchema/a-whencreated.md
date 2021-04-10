---
title: When-Created 屬性
description: 此物件的建立日期。 此值會複寫並位於通用類別目錄中。
ms.assetid: d66084f0-5a82-4a8c-86ee-7e41887d9b90
ms.tgt_platform: multiple
keywords:
- When-Created 屬性 AD 架構
- whenCreated 屬性 AD 架構
topic_type:
- apiref
api_name:
- When-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634918e29a4c8ef9c62d2b8949d253c80fe17d67
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107917"
---
# <a name="when-created-attribute"></a><span data-ttu-id="97740-106">When-Created 屬性</span><span class="sxs-lookup"><span data-stu-id="97740-106">When-Created attribute</span></span>

<span data-ttu-id="97740-107">此物件的建立日期。</span><span class="sxs-lookup"><span data-stu-id="97740-107">The date when this object was created.</span></span> <span data-ttu-id="97740-108">此值會複寫並位於通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="97740-108">This value is replicated and is in the global catalog.</span></span>



| <span data-ttu-id="97740-109">進入</span><span class="sxs-lookup"><span data-stu-id="97740-109">Entry</span></span> | <span data-ttu-id="97740-110">值</span><span class="sxs-lookup"><span data-stu-id="97740-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="97740-111">CN</span><span class="sxs-lookup"><span data-stu-id="97740-111">CN</span></span>                | <span data-ttu-id="97740-112">When-Created</span><span class="sxs-lookup"><span data-stu-id="97740-112">When-Created</span></span>                                                  |
| <span data-ttu-id="97740-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="97740-113">Ldap-Display-Name</span></span> | <span data-ttu-id="97740-114">whenCreated</span><span class="sxs-lookup"><span data-stu-id="97740-114">whenCreated</span></span>                                                   |
| <span data-ttu-id="97740-115">大小</span><span class="sxs-lookup"><span data-stu-id="97740-115">Size</span></span>              | <span data-ttu-id="97740-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="97740-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="97740-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="97740-117">Update Privilege</span></span>  | <span data-ttu-id="97740-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="97740-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="97740-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="97740-119">Update Frequency</span></span>  | <span data-ttu-id="97740-120">建立物件時。</span><span class="sxs-lookup"><span data-stu-id="97740-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="97740-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="97740-121">Attribute-Id</span></span>      | <span data-ttu-id="97740-122">1.2.840.113556.1.2.2</span><span class="sxs-lookup"><span data-stu-id="97740-122">1.2.840.113556.1.2.2</span></span>                                          |
| <span data-ttu-id="97740-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="97740-123">System-Id-Guid</span></span>    | <span data-ttu-id="97740-124">bf967a78-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="97740-124">bf967a78-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="97740-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="97740-125">Syntax</span></span>            | [<span data-ttu-id="97740-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="97740-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="97740-127">實作</span><span class="sxs-lookup"><span data-stu-id="97740-127">Implementations</span></span>

-   [<span data-ttu-id="97740-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="97740-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="97740-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="97740-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="97740-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="97740-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="97740-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="97740-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="97740-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="97740-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="97740-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="97740-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="97740-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="97740-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="97740-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="97740-135">Windows 2000 Server</span></span>



| <span data-ttu-id="97740-136">進入</span><span class="sxs-lookup"><span data-stu-id="97740-136">Entry</span></span> | <span data-ttu-id="97740-137">值</span><span class="sxs-lookup"><span data-stu-id="97740-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97740-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97740-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97740-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97740-139">MAPI-Id</span></span>                | <span data-ttu-id="97740-140">0x3007</span><span class="sxs-lookup"><span data-stu-id="97740-140">0x3007</span></span>                          |
| <span data-ttu-id="97740-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="97740-141">System-Only</span></span>            | <span data-ttu-id="97740-142">對</span><span class="sxs-lookup"><span data-stu-id="97740-142">True</span></span>                            |
| <span data-ttu-id="97740-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97740-143">Is-Single-Valued</span></span>       | <span data-ttu-id="97740-144">對</span><span class="sxs-lookup"><span data-stu-id="97740-144">True</span></span>                            |
| <span data-ttu-id="97740-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97740-145">Is Indexed</span></span>             | <span data-ttu-id="97740-146">否</span><span class="sxs-lookup"><span data-stu-id="97740-146">False</span></span>                           |
| <span data-ttu-id="97740-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97740-147">In Global Catalog</span></span>      | <span data-ttu-id="97740-148">對</span><span class="sxs-lookup"><span data-stu-id="97740-148">True</span></span>                            |
| <span data-ttu-id="97740-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97740-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="97740-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97740-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97740-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97740-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97740-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97740-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97740-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-153">Search-Flags</span></span>           | <span data-ttu-id="97740-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97740-154">0x00000000</span></span>                      |
| <span data-ttu-id="97740-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-155">System-Flags</span></span>           | <span data-ttu-id="97740-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97740-156">0x00000010</span></span>                      |
| <span data-ttu-id="97740-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97740-157">Classes used in</span></span>        | [<span data-ttu-id="97740-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97740-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="97740-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97740-159">Windows Server 2003</span></span>



| <span data-ttu-id="97740-160">進入</span><span class="sxs-lookup"><span data-stu-id="97740-160">Entry</span></span> | <span data-ttu-id="97740-161">值</span><span class="sxs-lookup"><span data-stu-id="97740-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97740-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97740-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97740-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97740-163">MAPI-Id</span></span>                | <span data-ttu-id="97740-164">0x3007</span><span class="sxs-lookup"><span data-stu-id="97740-164">0x3007</span></span>                          |
| <span data-ttu-id="97740-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="97740-165">System-Only</span></span>            | <span data-ttu-id="97740-166">對</span><span class="sxs-lookup"><span data-stu-id="97740-166">True</span></span>                            |
| <span data-ttu-id="97740-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97740-167">Is-Single-Valued</span></span>       | <span data-ttu-id="97740-168">對</span><span class="sxs-lookup"><span data-stu-id="97740-168">True</span></span>                            |
| <span data-ttu-id="97740-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97740-169">Is Indexed</span></span>             | <span data-ttu-id="97740-170">否</span><span class="sxs-lookup"><span data-stu-id="97740-170">False</span></span>                           |
| <span data-ttu-id="97740-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97740-171">In Global Catalog</span></span>      | <span data-ttu-id="97740-172">對</span><span class="sxs-lookup"><span data-stu-id="97740-172">True</span></span>                            |
| <span data-ttu-id="97740-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97740-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="97740-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97740-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97740-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97740-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97740-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97740-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97740-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-177">Search-Flags</span></span>           | <span data-ttu-id="97740-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97740-178">0x00000000</span></span>                      |
| <span data-ttu-id="97740-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-179">System-Flags</span></span>           | <span data-ttu-id="97740-180">0x00000012</span><span class="sxs-lookup"><span data-stu-id="97740-180">0x00000012</span></span>                      |
| <span data-ttu-id="97740-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97740-181">Classes used in</span></span>        | [<span data-ttu-id="97740-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97740-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="97740-183">亞當</span><span class="sxs-lookup"><span data-stu-id="97740-183">ADAM</span></span>



| <span data-ttu-id="97740-184">進入</span><span class="sxs-lookup"><span data-stu-id="97740-184">Entry</span></span> | <span data-ttu-id="97740-185">值</span><span class="sxs-lookup"><span data-stu-id="97740-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97740-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97740-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97740-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97740-187">MAPI-Id</span></span>                | <span data-ttu-id="97740-188">0x3007</span><span class="sxs-lookup"><span data-stu-id="97740-188">0x3007</span></span>                          |
| <span data-ttu-id="97740-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="97740-189">System-Only</span></span>            | <span data-ttu-id="97740-190">對</span><span class="sxs-lookup"><span data-stu-id="97740-190">True</span></span>                            |
| <span data-ttu-id="97740-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97740-191">Is-Single-Valued</span></span>       | <span data-ttu-id="97740-192">對</span><span class="sxs-lookup"><span data-stu-id="97740-192">True</span></span>                            |
| <span data-ttu-id="97740-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97740-193">Is Indexed</span></span>             | <span data-ttu-id="97740-194">否</span><span class="sxs-lookup"><span data-stu-id="97740-194">False</span></span>                           |
| <span data-ttu-id="97740-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97740-195">In Global Catalog</span></span>      | <span data-ttu-id="97740-196">對</span><span class="sxs-lookup"><span data-stu-id="97740-196">True</span></span>                            |
| <span data-ttu-id="97740-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97740-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="97740-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97740-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97740-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97740-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97740-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97740-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97740-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-201">Search-Flags</span></span>           | <span data-ttu-id="97740-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97740-202">0x00000000</span></span>                      |
| <span data-ttu-id="97740-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-203">System-Flags</span></span>           | <span data-ttu-id="97740-204">0x00000012</span><span class="sxs-lookup"><span data-stu-id="97740-204">0x00000012</span></span>                      |
| <span data-ttu-id="97740-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97740-205">Classes used in</span></span>        | [<span data-ttu-id="97740-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97740-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="97740-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="97740-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="97740-208">進入</span><span class="sxs-lookup"><span data-stu-id="97740-208">Entry</span></span> | <span data-ttu-id="97740-209">值</span><span class="sxs-lookup"><span data-stu-id="97740-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97740-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97740-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97740-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97740-211">MAPI-Id</span></span>                | <span data-ttu-id="97740-212">0x3007</span><span class="sxs-lookup"><span data-stu-id="97740-212">0x3007</span></span>                          |
| <span data-ttu-id="97740-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="97740-213">System-Only</span></span>            | <span data-ttu-id="97740-214">對</span><span class="sxs-lookup"><span data-stu-id="97740-214">True</span></span>                            |
| <span data-ttu-id="97740-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97740-215">Is-Single-Valued</span></span>       | <span data-ttu-id="97740-216">對</span><span class="sxs-lookup"><span data-stu-id="97740-216">True</span></span>                            |
| <span data-ttu-id="97740-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97740-217">Is Indexed</span></span>             | <span data-ttu-id="97740-218">否</span><span class="sxs-lookup"><span data-stu-id="97740-218">False</span></span>                           |
| <span data-ttu-id="97740-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97740-219">In Global Catalog</span></span>      | <span data-ttu-id="97740-220">對</span><span class="sxs-lookup"><span data-stu-id="97740-220">True</span></span>                            |
| <span data-ttu-id="97740-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97740-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="97740-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97740-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97740-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97740-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97740-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97740-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97740-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-225">Search-Flags</span></span>           | <span data-ttu-id="97740-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97740-226">0x00000000</span></span>                      |
| <span data-ttu-id="97740-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-227">System-Flags</span></span>           | <span data-ttu-id="97740-228">0x00000012</span><span class="sxs-lookup"><span data-stu-id="97740-228">0x00000012</span></span>                      |
| <span data-ttu-id="97740-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97740-229">Classes used in</span></span>        | [<span data-ttu-id="97740-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97740-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="97740-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97740-231">Windows Server 2008</span></span>



| <span data-ttu-id="97740-232">進入</span><span class="sxs-lookup"><span data-stu-id="97740-232">Entry</span></span> | <span data-ttu-id="97740-233">值</span><span class="sxs-lookup"><span data-stu-id="97740-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97740-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97740-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97740-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97740-235">MAPI-Id</span></span>                | <span data-ttu-id="97740-236">0x3007</span><span class="sxs-lookup"><span data-stu-id="97740-236">0x3007</span></span>                          |
| <span data-ttu-id="97740-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="97740-237">System-Only</span></span>            | <span data-ttu-id="97740-238">對</span><span class="sxs-lookup"><span data-stu-id="97740-238">True</span></span>                            |
| <span data-ttu-id="97740-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97740-239">Is-Single-Valued</span></span>       | <span data-ttu-id="97740-240">對</span><span class="sxs-lookup"><span data-stu-id="97740-240">True</span></span>                            |
| <span data-ttu-id="97740-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97740-241">Is Indexed</span></span>             | <span data-ttu-id="97740-242">否</span><span class="sxs-lookup"><span data-stu-id="97740-242">False</span></span>                           |
| <span data-ttu-id="97740-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97740-243">In Global Catalog</span></span>      | <span data-ttu-id="97740-244">對</span><span class="sxs-lookup"><span data-stu-id="97740-244">True</span></span>                            |
| <span data-ttu-id="97740-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97740-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="97740-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97740-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97740-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97740-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97740-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97740-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97740-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-249">Search-Flags</span></span>           | <span data-ttu-id="97740-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97740-250">0x00000000</span></span>                      |
| <span data-ttu-id="97740-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-251">System-Flags</span></span>           | <span data-ttu-id="97740-252">0x00000012</span><span class="sxs-lookup"><span data-stu-id="97740-252">0x00000012</span></span>                      |
| <span data-ttu-id="97740-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97740-253">Classes used in</span></span>        | [<span data-ttu-id="97740-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97740-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="97740-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97740-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="97740-256">進入</span><span class="sxs-lookup"><span data-stu-id="97740-256">Entry</span></span> | <span data-ttu-id="97740-257">值</span><span class="sxs-lookup"><span data-stu-id="97740-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97740-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97740-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97740-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97740-259">MAPI-Id</span></span>                | <span data-ttu-id="97740-260">0x3007</span><span class="sxs-lookup"><span data-stu-id="97740-260">0x3007</span></span>                          |
| <span data-ttu-id="97740-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="97740-261">System-Only</span></span>            | <span data-ttu-id="97740-262">對</span><span class="sxs-lookup"><span data-stu-id="97740-262">True</span></span>                            |
| <span data-ttu-id="97740-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97740-263">Is-Single-Valued</span></span>       | <span data-ttu-id="97740-264">對</span><span class="sxs-lookup"><span data-stu-id="97740-264">True</span></span>                            |
| <span data-ttu-id="97740-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97740-265">Is Indexed</span></span>             | <span data-ttu-id="97740-266">否</span><span class="sxs-lookup"><span data-stu-id="97740-266">False</span></span>                           |
| <span data-ttu-id="97740-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97740-267">In Global Catalog</span></span>      | <span data-ttu-id="97740-268">對</span><span class="sxs-lookup"><span data-stu-id="97740-268">True</span></span>                            |
| <span data-ttu-id="97740-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97740-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="97740-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97740-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97740-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97740-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97740-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97740-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97740-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-273">Search-Flags</span></span>           | <span data-ttu-id="97740-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97740-274">0x00000000</span></span>                      |
| <span data-ttu-id="97740-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-275">System-Flags</span></span>           | <span data-ttu-id="97740-276">0x00000012</span><span class="sxs-lookup"><span data-stu-id="97740-276">0x00000012</span></span>                      |
| <span data-ttu-id="97740-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97740-277">Classes used in</span></span>        | [<span data-ttu-id="97740-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97740-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="97740-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97740-279">Windows Server 2012</span></span>



| <span data-ttu-id="97740-280">進入</span><span class="sxs-lookup"><span data-stu-id="97740-280">Entry</span></span> | <span data-ttu-id="97740-281">值</span><span class="sxs-lookup"><span data-stu-id="97740-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97740-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97740-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97740-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97740-283">MAPI-Id</span></span>                | <span data-ttu-id="97740-284">0x3007</span><span class="sxs-lookup"><span data-stu-id="97740-284">0x3007</span></span>                          |
| <span data-ttu-id="97740-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="97740-285">System-Only</span></span>            | <span data-ttu-id="97740-286">對</span><span class="sxs-lookup"><span data-stu-id="97740-286">True</span></span>                            |
| <span data-ttu-id="97740-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97740-287">Is-Single-Valued</span></span>       | <span data-ttu-id="97740-288">對</span><span class="sxs-lookup"><span data-stu-id="97740-288">True</span></span>                            |
| <span data-ttu-id="97740-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97740-289">Is Indexed</span></span>             | <span data-ttu-id="97740-290">否</span><span class="sxs-lookup"><span data-stu-id="97740-290">False</span></span>                           |
| <span data-ttu-id="97740-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97740-291">In Global Catalog</span></span>      | <span data-ttu-id="97740-292">對</span><span class="sxs-lookup"><span data-stu-id="97740-292">True</span></span>                            |
| <span data-ttu-id="97740-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97740-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="97740-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97740-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97740-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97740-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97740-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97740-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97740-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-297">Search-Flags</span></span>           | <span data-ttu-id="97740-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97740-298">0x00000000</span></span>                      |
| <span data-ttu-id="97740-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97740-299">System-Flags</span></span>           | <span data-ttu-id="97740-300">0x00000012</span><span class="sxs-lookup"><span data-stu-id="97740-300">0x00000012</span></span>                      |
| <span data-ttu-id="97740-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97740-301">Classes used in</span></span>        | [<span data-ttu-id="97740-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97740-302">**Top**</span></span>](c-top.md)<br/> |



 

 





