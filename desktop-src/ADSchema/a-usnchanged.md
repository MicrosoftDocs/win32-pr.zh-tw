---
title: USN-Changed 屬性
description: 更新序號 (USN) 由本機目錄指派以進行最新變更，包括建立。 另請參閱 USN 建立。
ms.assetid: ccd61940-2c0a-4d46-af9f-5f23f577a1ad
ms.tgt_platform: multiple
keywords:
- USN-Changed 屬性 AD 架構
- uSNChanged 屬性 AD 架構
topic_type:
- apiref
api_name:
- USN-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c00f30a2ba7ca38f78246cd14b33ea358da6fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687111"
---
# <a name="usn-changed-attribute"></a><span data-ttu-id="17513-106">USN-Changed 屬性</span><span class="sxs-lookup"><span data-stu-id="17513-106">USN-Changed attribute</span></span>

<span data-ttu-id="17513-107">更新序號 (USN) 由本機目錄指派以進行最新變更，包括建立。</span><span class="sxs-lookup"><span data-stu-id="17513-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="17513-108">另請參閱 [**USN 建立**](a-usncreated.md)。</span><span class="sxs-lookup"><span data-stu-id="17513-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="17513-109">進入</span><span class="sxs-lookup"><span data-stu-id="17513-109">Entry</span></span> | <span data-ttu-id="17513-110">值</span><span class="sxs-lookup"><span data-stu-id="17513-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="17513-111">CN</span><span class="sxs-lookup"><span data-stu-id="17513-111">CN</span></span>                | <span data-ttu-id="17513-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="17513-112">USN-Changed</span></span>                          |
| <span data-ttu-id="17513-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="17513-113">Ldap-Display-Name</span></span> | <span data-ttu-id="17513-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="17513-114">uSNChanged</span></span>                           |
| <span data-ttu-id="17513-115">大小</span><span class="sxs-lookup"><span data-stu-id="17513-115">Size</span></span>              | <span data-ttu-id="17513-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="17513-116">8 bytes</span></span>                              |
| <span data-ttu-id="17513-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="17513-117">Update Privilege</span></span>  | <span data-ttu-id="17513-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="17513-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="17513-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="17513-119">Update Frequency</span></span>  | <span data-ttu-id="17513-120">當物件變更時。</span><span class="sxs-lookup"><span data-stu-id="17513-120">When the object is changed.</span></span>          |
| <span data-ttu-id="17513-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17513-121">Attribute-Id</span></span>      | <span data-ttu-id="17513-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="17513-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="17513-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="17513-123">System-Id-Guid</span></span>    | <span data-ttu-id="17513-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="17513-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="17513-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="17513-125">Syntax</span></span>            | [<span data-ttu-id="17513-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="17513-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="17513-127">實作</span><span class="sxs-lookup"><span data-stu-id="17513-127">Implementations</span></span>

-   [<span data-ttu-id="17513-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="17513-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="17513-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17513-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17513-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="17513-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="17513-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17513-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17513-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17513-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17513-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17513-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17513-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17513-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="17513-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17513-135">Windows 2000 Server</span></span>



| <span data-ttu-id="17513-136">進入</span><span class="sxs-lookup"><span data-stu-id="17513-136">Entry</span></span> | <span data-ttu-id="17513-137">值</span><span class="sxs-lookup"><span data-stu-id="17513-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="17513-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17513-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="17513-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17513-139">MAPI-Id</span></span>                | <span data-ttu-id="17513-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="17513-140">0x8029</span></span>                          |
| <span data-ttu-id="17513-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="17513-141">System-Only</span></span>            | <span data-ttu-id="17513-142">對</span><span class="sxs-lookup"><span data-stu-id="17513-142">True</span></span>                            |
| <span data-ttu-id="17513-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17513-143">Is-Single-Valued</span></span>       | <span data-ttu-id="17513-144">對</span><span class="sxs-lookup"><span data-stu-id="17513-144">True</span></span>                            |
| <span data-ttu-id="17513-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17513-145">Is Indexed</span></span>             | <span data-ttu-id="17513-146">對</span><span class="sxs-lookup"><span data-stu-id="17513-146">True</span></span>                            |
| <span data-ttu-id="17513-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17513-147">In Global Catalog</span></span>      | <span data-ttu-id="17513-148">對</span><span class="sxs-lookup"><span data-stu-id="17513-148">True</span></span>                            |
| <span data-ttu-id="17513-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17513-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="17513-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17513-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="17513-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17513-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="17513-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17513-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="17513-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-153">Search-Flags</span></span>           | <span data-ttu-id="17513-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="17513-154">0x00000009</span></span>                      |
| <span data-ttu-id="17513-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-155">System-Flags</span></span>           | <span data-ttu-id="17513-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="17513-156">0x00000013</span></span>                      |
| <span data-ttu-id="17513-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17513-157">Classes used in</span></span>        | [<span data-ttu-id="17513-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="17513-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="17513-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17513-159">Windows Server 2003</span></span>



| <span data-ttu-id="17513-160">進入</span><span class="sxs-lookup"><span data-stu-id="17513-160">Entry</span></span> | <span data-ttu-id="17513-161">值</span><span class="sxs-lookup"><span data-stu-id="17513-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="17513-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17513-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="17513-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17513-163">MAPI-Id</span></span>                | <span data-ttu-id="17513-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="17513-164">0x8029</span></span>                          |
| <span data-ttu-id="17513-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="17513-165">System-Only</span></span>            | <span data-ttu-id="17513-166">對</span><span class="sxs-lookup"><span data-stu-id="17513-166">True</span></span>                            |
| <span data-ttu-id="17513-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17513-167">Is-Single-Valued</span></span>       | <span data-ttu-id="17513-168">對</span><span class="sxs-lookup"><span data-stu-id="17513-168">True</span></span>                            |
| <span data-ttu-id="17513-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17513-169">Is Indexed</span></span>             | <span data-ttu-id="17513-170">對</span><span class="sxs-lookup"><span data-stu-id="17513-170">True</span></span>                            |
| <span data-ttu-id="17513-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17513-171">In Global Catalog</span></span>      | <span data-ttu-id="17513-172">對</span><span class="sxs-lookup"><span data-stu-id="17513-172">True</span></span>                            |
| <span data-ttu-id="17513-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17513-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="17513-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17513-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="17513-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17513-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="17513-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17513-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="17513-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-177">Search-Flags</span></span>           | <span data-ttu-id="17513-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="17513-178">0x00000009</span></span>                      |
| <span data-ttu-id="17513-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-179">System-Flags</span></span>           | <span data-ttu-id="17513-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="17513-180">0x00000013</span></span>                      |
| <span data-ttu-id="17513-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17513-181">Classes used in</span></span>        | [<span data-ttu-id="17513-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="17513-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="17513-183">亞當</span><span class="sxs-lookup"><span data-stu-id="17513-183">ADAM</span></span>



| <span data-ttu-id="17513-184">進入</span><span class="sxs-lookup"><span data-stu-id="17513-184">Entry</span></span> | <span data-ttu-id="17513-185">值</span><span class="sxs-lookup"><span data-stu-id="17513-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="17513-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17513-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="17513-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17513-187">MAPI-Id</span></span>                | <span data-ttu-id="17513-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="17513-188">0x8029</span></span>                          |
| <span data-ttu-id="17513-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="17513-189">System-Only</span></span>            | <span data-ttu-id="17513-190">對</span><span class="sxs-lookup"><span data-stu-id="17513-190">True</span></span>                            |
| <span data-ttu-id="17513-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17513-191">Is-Single-Valued</span></span>       | <span data-ttu-id="17513-192">對</span><span class="sxs-lookup"><span data-stu-id="17513-192">True</span></span>                            |
| <span data-ttu-id="17513-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17513-193">Is Indexed</span></span>             | <span data-ttu-id="17513-194">對</span><span class="sxs-lookup"><span data-stu-id="17513-194">True</span></span>                            |
| <span data-ttu-id="17513-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17513-195">In Global Catalog</span></span>      | <span data-ttu-id="17513-196">對</span><span class="sxs-lookup"><span data-stu-id="17513-196">True</span></span>                            |
| <span data-ttu-id="17513-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17513-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="17513-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17513-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="17513-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17513-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="17513-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17513-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="17513-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-201">Search-Flags</span></span>           | <span data-ttu-id="17513-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="17513-202">0x00000009</span></span>                      |
| <span data-ttu-id="17513-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-203">System-Flags</span></span>           | <span data-ttu-id="17513-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="17513-204">0x00000013</span></span>                      |
| <span data-ttu-id="17513-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17513-205">Classes used in</span></span>        | [<span data-ttu-id="17513-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="17513-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17513-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17513-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17513-208">進入</span><span class="sxs-lookup"><span data-stu-id="17513-208">Entry</span></span> | <span data-ttu-id="17513-209">值</span><span class="sxs-lookup"><span data-stu-id="17513-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="17513-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17513-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="17513-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17513-211">MAPI-Id</span></span>                | <span data-ttu-id="17513-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="17513-212">0x8029</span></span>                          |
| <span data-ttu-id="17513-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="17513-213">System-Only</span></span>            | <span data-ttu-id="17513-214">對</span><span class="sxs-lookup"><span data-stu-id="17513-214">True</span></span>                            |
| <span data-ttu-id="17513-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17513-215">Is-Single-Valued</span></span>       | <span data-ttu-id="17513-216">對</span><span class="sxs-lookup"><span data-stu-id="17513-216">True</span></span>                            |
| <span data-ttu-id="17513-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17513-217">Is Indexed</span></span>             | <span data-ttu-id="17513-218">對</span><span class="sxs-lookup"><span data-stu-id="17513-218">True</span></span>                            |
| <span data-ttu-id="17513-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17513-219">In Global Catalog</span></span>      | <span data-ttu-id="17513-220">對</span><span class="sxs-lookup"><span data-stu-id="17513-220">True</span></span>                            |
| <span data-ttu-id="17513-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17513-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="17513-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17513-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="17513-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17513-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="17513-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17513-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="17513-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-225">Search-Flags</span></span>           | <span data-ttu-id="17513-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="17513-226">0x00000009</span></span>                      |
| <span data-ttu-id="17513-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-227">System-Flags</span></span>           | <span data-ttu-id="17513-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="17513-228">0x00000013</span></span>                      |
| <span data-ttu-id="17513-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17513-229">Classes used in</span></span>        | [<span data-ttu-id="17513-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="17513-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17513-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17513-231">Windows Server 2008</span></span>



| <span data-ttu-id="17513-232">進入</span><span class="sxs-lookup"><span data-stu-id="17513-232">Entry</span></span> | <span data-ttu-id="17513-233">值</span><span class="sxs-lookup"><span data-stu-id="17513-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="17513-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17513-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="17513-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17513-235">MAPI-Id</span></span>                | <span data-ttu-id="17513-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="17513-236">0x8029</span></span>                          |
| <span data-ttu-id="17513-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="17513-237">System-Only</span></span>            | <span data-ttu-id="17513-238">對</span><span class="sxs-lookup"><span data-stu-id="17513-238">True</span></span>                            |
| <span data-ttu-id="17513-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17513-239">Is-Single-Valued</span></span>       | <span data-ttu-id="17513-240">對</span><span class="sxs-lookup"><span data-stu-id="17513-240">True</span></span>                            |
| <span data-ttu-id="17513-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17513-241">Is Indexed</span></span>             | <span data-ttu-id="17513-242">對</span><span class="sxs-lookup"><span data-stu-id="17513-242">True</span></span>                            |
| <span data-ttu-id="17513-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17513-243">In Global Catalog</span></span>      | <span data-ttu-id="17513-244">對</span><span class="sxs-lookup"><span data-stu-id="17513-244">True</span></span>                            |
| <span data-ttu-id="17513-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17513-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="17513-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17513-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="17513-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17513-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="17513-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17513-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="17513-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-249">Search-Flags</span></span>           | <span data-ttu-id="17513-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="17513-250">0x00000009</span></span>                      |
| <span data-ttu-id="17513-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-251">System-Flags</span></span>           | <span data-ttu-id="17513-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="17513-252">0x00000013</span></span>                      |
| <span data-ttu-id="17513-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17513-253">Classes used in</span></span>        | [<span data-ttu-id="17513-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="17513-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17513-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17513-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17513-256">進入</span><span class="sxs-lookup"><span data-stu-id="17513-256">Entry</span></span> | <span data-ttu-id="17513-257">值</span><span class="sxs-lookup"><span data-stu-id="17513-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="17513-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17513-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="17513-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17513-259">MAPI-Id</span></span>                | <span data-ttu-id="17513-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="17513-260">0x8029</span></span>                          |
| <span data-ttu-id="17513-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="17513-261">System-Only</span></span>            | <span data-ttu-id="17513-262">對</span><span class="sxs-lookup"><span data-stu-id="17513-262">True</span></span>                            |
| <span data-ttu-id="17513-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17513-263">Is-Single-Valued</span></span>       | <span data-ttu-id="17513-264">對</span><span class="sxs-lookup"><span data-stu-id="17513-264">True</span></span>                            |
| <span data-ttu-id="17513-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17513-265">Is Indexed</span></span>             | <span data-ttu-id="17513-266">對</span><span class="sxs-lookup"><span data-stu-id="17513-266">True</span></span>                            |
| <span data-ttu-id="17513-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17513-267">In Global Catalog</span></span>      | <span data-ttu-id="17513-268">對</span><span class="sxs-lookup"><span data-stu-id="17513-268">True</span></span>                            |
| <span data-ttu-id="17513-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17513-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="17513-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17513-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="17513-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17513-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="17513-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17513-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="17513-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-273">Search-Flags</span></span>           | <span data-ttu-id="17513-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="17513-274">0x00000009</span></span>                      |
| <span data-ttu-id="17513-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-275">System-Flags</span></span>           | <span data-ttu-id="17513-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="17513-276">0x00000013</span></span>                      |
| <span data-ttu-id="17513-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17513-277">Classes used in</span></span>        | [<span data-ttu-id="17513-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="17513-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17513-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17513-279">Windows Server 2012</span></span>



| <span data-ttu-id="17513-280">進入</span><span class="sxs-lookup"><span data-stu-id="17513-280">Entry</span></span> | <span data-ttu-id="17513-281">值</span><span class="sxs-lookup"><span data-stu-id="17513-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="17513-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="17513-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="17513-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17513-283">MAPI-Id</span></span>                | <span data-ttu-id="17513-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="17513-284">0x8029</span></span>                          |
| <span data-ttu-id="17513-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="17513-285">System-Only</span></span>            | <span data-ttu-id="17513-286">對</span><span class="sxs-lookup"><span data-stu-id="17513-286">True</span></span>                            |
| <span data-ttu-id="17513-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="17513-287">Is-Single-Valued</span></span>       | <span data-ttu-id="17513-288">對</span><span class="sxs-lookup"><span data-stu-id="17513-288">True</span></span>                            |
| <span data-ttu-id="17513-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="17513-289">Is Indexed</span></span>             | <span data-ttu-id="17513-290">對</span><span class="sxs-lookup"><span data-stu-id="17513-290">True</span></span>                            |
| <span data-ttu-id="17513-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="17513-291">In Global Catalog</span></span>      | <span data-ttu-id="17513-292">對</span><span class="sxs-lookup"><span data-stu-id="17513-292">True</span></span>                            |
| <span data-ttu-id="17513-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="17513-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="17513-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="17513-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="17513-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17513-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="17513-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17513-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="17513-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-297">Search-Flags</span></span>           | <span data-ttu-id="17513-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="17513-298">0x00000009</span></span>                      |
| <span data-ttu-id="17513-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17513-299">System-Flags</span></span>           | <span data-ttu-id="17513-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="17513-300">0x00000013</span></span>                      |
| <span data-ttu-id="17513-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="17513-301">Classes used in</span></span>        | [<span data-ttu-id="17513-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="17513-302">**Top**</span></span>](c-top.md)<br/> |



 

 





