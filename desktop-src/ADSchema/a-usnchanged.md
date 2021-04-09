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
# <a name="usn-changed-attribute"></a><span data-ttu-id="df256-106">USN-Changed 屬性</span><span class="sxs-lookup"><span data-stu-id="df256-106">USN-Changed attribute</span></span>

<span data-ttu-id="df256-107">更新序號 (USN) 由本機目錄指派以進行最新變更，包括建立。</span><span class="sxs-lookup"><span data-stu-id="df256-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="df256-108">另請參閱 [**USN 建立**](a-usncreated.md)。</span><span class="sxs-lookup"><span data-stu-id="df256-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="df256-109">進入</span><span class="sxs-lookup"><span data-stu-id="df256-109">Entry</span></span> | <span data-ttu-id="df256-110">值</span><span class="sxs-lookup"><span data-stu-id="df256-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="df256-111">CN</span><span class="sxs-lookup"><span data-stu-id="df256-111">CN</span></span>                | <span data-ttu-id="df256-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="df256-112">USN-Changed</span></span>                          |
| <span data-ttu-id="df256-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="df256-113">Ldap-Display-Name</span></span> | <span data-ttu-id="df256-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="df256-114">uSNChanged</span></span>                           |
| <span data-ttu-id="df256-115">大小</span><span class="sxs-lookup"><span data-stu-id="df256-115">Size</span></span>              | <span data-ttu-id="df256-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="df256-116">8 bytes</span></span>                              |
| <span data-ttu-id="df256-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="df256-117">Update Privilege</span></span>  | <span data-ttu-id="df256-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="df256-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="df256-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="df256-119">Update Frequency</span></span>  | <span data-ttu-id="df256-120">當物件變更時。</span><span class="sxs-lookup"><span data-stu-id="df256-120">When the object is changed.</span></span>          |
| <span data-ttu-id="df256-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df256-121">Attribute-Id</span></span>      | <span data-ttu-id="df256-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="df256-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="df256-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="df256-123">System-Id-Guid</span></span>    | <span data-ttu-id="df256-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="df256-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="df256-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="df256-125">Syntax</span></span>            | [<span data-ttu-id="df256-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="df256-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="df256-127">實作</span><span class="sxs-lookup"><span data-stu-id="df256-127">Implementations</span></span>

-   [<span data-ttu-id="df256-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="df256-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="df256-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df256-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df256-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="df256-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="df256-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df256-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df256-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df256-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df256-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df256-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df256-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df256-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="df256-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df256-135">Windows 2000 Server</span></span>



| <span data-ttu-id="df256-136">進入</span><span class="sxs-lookup"><span data-stu-id="df256-136">Entry</span></span> | <span data-ttu-id="df256-137">值</span><span class="sxs-lookup"><span data-stu-id="df256-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df256-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df256-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df256-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df256-139">MAPI-Id</span></span>                | <span data-ttu-id="df256-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="df256-140">0x8029</span></span>                          |
| <span data-ttu-id="df256-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="df256-141">System-Only</span></span>            | <span data-ttu-id="df256-142">對</span><span class="sxs-lookup"><span data-stu-id="df256-142">True</span></span>                            |
| <span data-ttu-id="df256-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df256-143">Is-Single-Valued</span></span>       | <span data-ttu-id="df256-144">對</span><span class="sxs-lookup"><span data-stu-id="df256-144">True</span></span>                            |
| <span data-ttu-id="df256-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df256-145">Is Indexed</span></span>             | <span data-ttu-id="df256-146">對</span><span class="sxs-lookup"><span data-stu-id="df256-146">True</span></span>                            |
| <span data-ttu-id="df256-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df256-147">In Global Catalog</span></span>      | <span data-ttu-id="df256-148">對</span><span class="sxs-lookup"><span data-stu-id="df256-148">True</span></span>                            |
| <span data-ttu-id="df256-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df256-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="df256-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df256-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df256-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df256-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df256-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df256-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df256-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-153">Search-Flags</span></span>           | <span data-ttu-id="df256-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="df256-154">0x00000009</span></span>                      |
| <span data-ttu-id="df256-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-155">System-Flags</span></span>           | <span data-ttu-id="df256-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="df256-156">0x00000013</span></span>                      |
| <span data-ttu-id="df256-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df256-157">Classes used in</span></span>        | [<span data-ttu-id="df256-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df256-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="df256-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df256-159">Windows Server 2003</span></span>



| <span data-ttu-id="df256-160">進入</span><span class="sxs-lookup"><span data-stu-id="df256-160">Entry</span></span> | <span data-ttu-id="df256-161">值</span><span class="sxs-lookup"><span data-stu-id="df256-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df256-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df256-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df256-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df256-163">MAPI-Id</span></span>                | <span data-ttu-id="df256-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="df256-164">0x8029</span></span>                          |
| <span data-ttu-id="df256-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="df256-165">System-Only</span></span>            | <span data-ttu-id="df256-166">對</span><span class="sxs-lookup"><span data-stu-id="df256-166">True</span></span>                            |
| <span data-ttu-id="df256-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df256-167">Is-Single-Valued</span></span>       | <span data-ttu-id="df256-168">對</span><span class="sxs-lookup"><span data-stu-id="df256-168">True</span></span>                            |
| <span data-ttu-id="df256-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df256-169">Is Indexed</span></span>             | <span data-ttu-id="df256-170">對</span><span class="sxs-lookup"><span data-stu-id="df256-170">True</span></span>                            |
| <span data-ttu-id="df256-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df256-171">In Global Catalog</span></span>      | <span data-ttu-id="df256-172">對</span><span class="sxs-lookup"><span data-stu-id="df256-172">True</span></span>                            |
| <span data-ttu-id="df256-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df256-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="df256-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df256-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df256-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df256-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df256-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df256-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df256-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-177">Search-Flags</span></span>           | <span data-ttu-id="df256-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="df256-178">0x00000009</span></span>                      |
| <span data-ttu-id="df256-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-179">System-Flags</span></span>           | <span data-ttu-id="df256-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="df256-180">0x00000013</span></span>                      |
| <span data-ttu-id="df256-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df256-181">Classes used in</span></span>        | [<span data-ttu-id="df256-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df256-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="df256-183">亞當</span><span class="sxs-lookup"><span data-stu-id="df256-183">ADAM</span></span>



| <span data-ttu-id="df256-184">進入</span><span class="sxs-lookup"><span data-stu-id="df256-184">Entry</span></span> | <span data-ttu-id="df256-185">值</span><span class="sxs-lookup"><span data-stu-id="df256-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df256-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df256-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df256-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df256-187">MAPI-Id</span></span>                | <span data-ttu-id="df256-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="df256-188">0x8029</span></span>                          |
| <span data-ttu-id="df256-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="df256-189">System-Only</span></span>            | <span data-ttu-id="df256-190">對</span><span class="sxs-lookup"><span data-stu-id="df256-190">True</span></span>                            |
| <span data-ttu-id="df256-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df256-191">Is-Single-Valued</span></span>       | <span data-ttu-id="df256-192">對</span><span class="sxs-lookup"><span data-stu-id="df256-192">True</span></span>                            |
| <span data-ttu-id="df256-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df256-193">Is Indexed</span></span>             | <span data-ttu-id="df256-194">對</span><span class="sxs-lookup"><span data-stu-id="df256-194">True</span></span>                            |
| <span data-ttu-id="df256-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df256-195">In Global Catalog</span></span>      | <span data-ttu-id="df256-196">對</span><span class="sxs-lookup"><span data-stu-id="df256-196">True</span></span>                            |
| <span data-ttu-id="df256-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df256-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="df256-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df256-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df256-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df256-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df256-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df256-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df256-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-201">Search-Flags</span></span>           | <span data-ttu-id="df256-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="df256-202">0x00000009</span></span>                      |
| <span data-ttu-id="df256-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-203">System-Flags</span></span>           | <span data-ttu-id="df256-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="df256-204">0x00000013</span></span>                      |
| <span data-ttu-id="df256-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df256-205">Classes used in</span></span>        | [<span data-ttu-id="df256-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df256-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df256-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df256-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df256-208">進入</span><span class="sxs-lookup"><span data-stu-id="df256-208">Entry</span></span> | <span data-ttu-id="df256-209">值</span><span class="sxs-lookup"><span data-stu-id="df256-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df256-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df256-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df256-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df256-211">MAPI-Id</span></span>                | <span data-ttu-id="df256-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="df256-212">0x8029</span></span>                          |
| <span data-ttu-id="df256-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="df256-213">System-Only</span></span>            | <span data-ttu-id="df256-214">對</span><span class="sxs-lookup"><span data-stu-id="df256-214">True</span></span>                            |
| <span data-ttu-id="df256-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df256-215">Is-Single-Valued</span></span>       | <span data-ttu-id="df256-216">對</span><span class="sxs-lookup"><span data-stu-id="df256-216">True</span></span>                            |
| <span data-ttu-id="df256-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df256-217">Is Indexed</span></span>             | <span data-ttu-id="df256-218">對</span><span class="sxs-lookup"><span data-stu-id="df256-218">True</span></span>                            |
| <span data-ttu-id="df256-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df256-219">In Global Catalog</span></span>      | <span data-ttu-id="df256-220">對</span><span class="sxs-lookup"><span data-stu-id="df256-220">True</span></span>                            |
| <span data-ttu-id="df256-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df256-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="df256-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df256-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df256-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df256-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df256-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df256-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df256-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-225">Search-Flags</span></span>           | <span data-ttu-id="df256-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="df256-226">0x00000009</span></span>                      |
| <span data-ttu-id="df256-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-227">System-Flags</span></span>           | <span data-ttu-id="df256-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="df256-228">0x00000013</span></span>                      |
| <span data-ttu-id="df256-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df256-229">Classes used in</span></span>        | [<span data-ttu-id="df256-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df256-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df256-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df256-231">Windows Server 2008</span></span>



| <span data-ttu-id="df256-232">進入</span><span class="sxs-lookup"><span data-stu-id="df256-232">Entry</span></span> | <span data-ttu-id="df256-233">值</span><span class="sxs-lookup"><span data-stu-id="df256-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df256-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df256-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df256-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df256-235">MAPI-Id</span></span>                | <span data-ttu-id="df256-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="df256-236">0x8029</span></span>                          |
| <span data-ttu-id="df256-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="df256-237">System-Only</span></span>            | <span data-ttu-id="df256-238">對</span><span class="sxs-lookup"><span data-stu-id="df256-238">True</span></span>                            |
| <span data-ttu-id="df256-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df256-239">Is-Single-Valued</span></span>       | <span data-ttu-id="df256-240">對</span><span class="sxs-lookup"><span data-stu-id="df256-240">True</span></span>                            |
| <span data-ttu-id="df256-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df256-241">Is Indexed</span></span>             | <span data-ttu-id="df256-242">對</span><span class="sxs-lookup"><span data-stu-id="df256-242">True</span></span>                            |
| <span data-ttu-id="df256-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df256-243">In Global Catalog</span></span>      | <span data-ttu-id="df256-244">對</span><span class="sxs-lookup"><span data-stu-id="df256-244">True</span></span>                            |
| <span data-ttu-id="df256-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df256-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="df256-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df256-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df256-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df256-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df256-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df256-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df256-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-249">Search-Flags</span></span>           | <span data-ttu-id="df256-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="df256-250">0x00000009</span></span>                      |
| <span data-ttu-id="df256-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-251">System-Flags</span></span>           | <span data-ttu-id="df256-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="df256-252">0x00000013</span></span>                      |
| <span data-ttu-id="df256-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df256-253">Classes used in</span></span>        | [<span data-ttu-id="df256-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df256-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df256-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df256-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df256-256">進入</span><span class="sxs-lookup"><span data-stu-id="df256-256">Entry</span></span> | <span data-ttu-id="df256-257">值</span><span class="sxs-lookup"><span data-stu-id="df256-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df256-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df256-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df256-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df256-259">MAPI-Id</span></span>                | <span data-ttu-id="df256-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="df256-260">0x8029</span></span>                          |
| <span data-ttu-id="df256-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="df256-261">System-Only</span></span>            | <span data-ttu-id="df256-262">對</span><span class="sxs-lookup"><span data-stu-id="df256-262">True</span></span>                            |
| <span data-ttu-id="df256-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df256-263">Is-Single-Valued</span></span>       | <span data-ttu-id="df256-264">對</span><span class="sxs-lookup"><span data-stu-id="df256-264">True</span></span>                            |
| <span data-ttu-id="df256-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df256-265">Is Indexed</span></span>             | <span data-ttu-id="df256-266">對</span><span class="sxs-lookup"><span data-stu-id="df256-266">True</span></span>                            |
| <span data-ttu-id="df256-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df256-267">In Global Catalog</span></span>      | <span data-ttu-id="df256-268">對</span><span class="sxs-lookup"><span data-stu-id="df256-268">True</span></span>                            |
| <span data-ttu-id="df256-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df256-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="df256-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df256-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df256-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df256-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df256-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df256-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df256-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-273">Search-Flags</span></span>           | <span data-ttu-id="df256-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="df256-274">0x00000009</span></span>                      |
| <span data-ttu-id="df256-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-275">System-Flags</span></span>           | <span data-ttu-id="df256-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="df256-276">0x00000013</span></span>                      |
| <span data-ttu-id="df256-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df256-277">Classes used in</span></span>        | [<span data-ttu-id="df256-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df256-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df256-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df256-279">Windows Server 2012</span></span>



| <span data-ttu-id="df256-280">進入</span><span class="sxs-lookup"><span data-stu-id="df256-280">Entry</span></span> | <span data-ttu-id="df256-281">值</span><span class="sxs-lookup"><span data-stu-id="df256-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="df256-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="df256-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="df256-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df256-283">MAPI-Id</span></span>                | <span data-ttu-id="df256-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="df256-284">0x8029</span></span>                          |
| <span data-ttu-id="df256-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="df256-285">System-Only</span></span>            | <span data-ttu-id="df256-286">對</span><span class="sxs-lookup"><span data-stu-id="df256-286">True</span></span>                            |
| <span data-ttu-id="df256-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="df256-287">Is-Single-Valued</span></span>       | <span data-ttu-id="df256-288">對</span><span class="sxs-lookup"><span data-stu-id="df256-288">True</span></span>                            |
| <span data-ttu-id="df256-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="df256-289">Is Indexed</span></span>             | <span data-ttu-id="df256-290">對</span><span class="sxs-lookup"><span data-stu-id="df256-290">True</span></span>                            |
| <span data-ttu-id="df256-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="df256-291">In Global Catalog</span></span>      | <span data-ttu-id="df256-292">對</span><span class="sxs-lookup"><span data-stu-id="df256-292">True</span></span>                            |
| <span data-ttu-id="df256-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="df256-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="df256-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="df256-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="df256-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df256-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="df256-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df256-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="df256-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-297">Search-Flags</span></span>           | <span data-ttu-id="df256-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="df256-298">0x00000009</span></span>                      |
| <span data-ttu-id="df256-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df256-299">System-Flags</span></span>           | <span data-ttu-id="df256-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="df256-300">0x00000013</span></span>                      |
| <span data-ttu-id="df256-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="df256-301">Classes used in</span></span>        | [<span data-ttu-id="df256-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="df256-302">**Top**</span></span>](c-top.md)<br/> |



 

 





