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
# <a name="usn-changed-attribute"></a><span data-ttu-id="0b824-106">USN-Changed 屬性</span><span class="sxs-lookup"><span data-stu-id="0b824-106">USN-Changed attribute</span></span>

<span data-ttu-id="0b824-107">更新序號 (USN) 由本機目錄指派以進行最新變更，包括建立。</span><span class="sxs-lookup"><span data-stu-id="0b824-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="0b824-108">另請參閱 [**USN 建立**](a-usncreated.md)。</span><span class="sxs-lookup"><span data-stu-id="0b824-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="0b824-109">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-109">Entry</span></span> | <span data-ttu-id="0b824-110">值</span><span class="sxs-lookup"><span data-stu-id="0b824-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0b824-111">CN</span><span class="sxs-lookup"><span data-stu-id="0b824-111">CN</span></span>                | <span data-ttu-id="0b824-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="0b824-112">USN-Changed</span></span>                          |
| <span data-ttu-id="0b824-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0b824-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0b824-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="0b824-114">uSNChanged</span></span>                           |
| <span data-ttu-id="0b824-115">大小</span><span class="sxs-lookup"><span data-stu-id="0b824-115">Size</span></span>              | <span data-ttu-id="0b824-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="0b824-116">8 bytes</span></span>                              |
| <span data-ttu-id="0b824-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0b824-117">Update Privilege</span></span>  | <span data-ttu-id="0b824-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0b824-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="0b824-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0b824-119">Update Frequency</span></span>  | <span data-ttu-id="0b824-120">當物件變更時。</span><span class="sxs-lookup"><span data-stu-id="0b824-120">When the object is changed.</span></span>          |
| <span data-ttu-id="0b824-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-121">Attribute-Id</span></span>      | <span data-ttu-id="0b824-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="0b824-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="0b824-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0b824-123">System-Id-Guid</span></span>    | <span data-ttu-id="0b824-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0b824-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0b824-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b824-125">Syntax</span></span>            | [<span data-ttu-id="0b824-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="0b824-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0b824-127">實作</span><span class="sxs-lookup"><span data-stu-id="0b824-127">Implementations</span></span>

-   [<span data-ttu-id="0b824-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b824-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b824-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b824-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b824-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="0b824-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0b824-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b824-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b824-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b824-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b824-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b824-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b824-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b824-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b824-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b824-135">Windows 2000 Server</span></span>



| <span data-ttu-id="0b824-136">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-136">Entry</span></span> | <span data-ttu-id="0b824-137">值</span><span class="sxs-lookup"><span data-stu-id="0b824-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b824-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b824-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b824-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-139">MAPI-Id</span></span>                | <span data-ttu-id="0b824-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="0b824-140">0x8029</span></span>                          |
| <span data-ttu-id="0b824-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b824-141">System-Only</span></span>            | <span data-ttu-id="0b824-142">對</span><span class="sxs-lookup"><span data-stu-id="0b824-142">True</span></span>                            |
| <span data-ttu-id="0b824-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b824-143">Is-Single-Valued</span></span>       | <span data-ttu-id="0b824-144">對</span><span class="sxs-lookup"><span data-stu-id="0b824-144">True</span></span>                            |
| <span data-ttu-id="0b824-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b824-145">Is Indexed</span></span>             | <span data-ttu-id="0b824-146">對</span><span class="sxs-lookup"><span data-stu-id="0b824-146">True</span></span>                            |
| <span data-ttu-id="0b824-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b824-147">In Global Catalog</span></span>      | <span data-ttu-id="0b824-148">對</span><span class="sxs-lookup"><span data-stu-id="0b824-148">True</span></span>                            |
| <span data-ttu-id="0b824-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b824-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b824-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b824-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b824-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b824-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b824-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b824-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b824-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-153">Search-Flags</span></span>           | <span data-ttu-id="0b824-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="0b824-154">0x00000009</span></span>                      |
| <span data-ttu-id="0b824-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-155">System-Flags</span></span>           | <span data-ttu-id="0b824-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0b824-156">0x00000013</span></span>                      |
| <span data-ttu-id="0b824-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b824-157">Classes used in</span></span>        | [<span data-ttu-id="0b824-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0b824-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b824-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b824-159">Windows Server 2003</span></span>



| <span data-ttu-id="0b824-160">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-160">Entry</span></span> | <span data-ttu-id="0b824-161">值</span><span class="sxs-lookup"><span data-stu-id="0b824-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b824-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b824-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b824-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-163">MAPI-Id</span></span>                | <span data-ttu-id="0b824-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="0b824-164">0x8029</span></span>                          |
| <span data-ttu-id="0b824-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b824-165">System-Only</span></span>            | <span data-ttu-id="0b824-166">對</span><span class="sxs-lookup"><span data-stu-id="0b824-166">True</span></span>                            |
| <span data-ttu-id="0b824-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b824-167">Is-Single-Valued</span></span>       | <span data-ttu-id="0b824-168">對</span><span class="sxs-lookup"><span data-stu-id="0b824-168">True</span></span>                            |
| <span data-ttu-id="0b824-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b824-169">Is Indexed</span></span>             | <span data-ttu-id="0b824-170">對</span><span class="sxs-lookup"><span data-stu-id="0b824-170">True</span></span>                            |
| <span data-ttu-id="0b824-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b824-171">In Global Catalog</span></span>      | <span data-ttu-id="0b824-172">對</span><span class="sxs-lookup"><span data-stu-id="0b824-172">True</span></span>                            |
| <span data-ttu-id="0b824-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b824-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b824-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b824-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b824-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b824-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b824-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b824-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b824-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-177">Search-Flags</span></span>           | <span data-ttu-id="0b824-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="0b824-178">0x00000009</span></span>                      |
| <span data-ttu-id="0b824-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-179">System-Flags</span></span>           | <span data-ttu-id="0b824-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0b824-180">0x00000013</span></span>                      |
| <span data-ttu-id="0b824-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b824-181">Classes used in</span></span>        | [<span data-ttu-id="0b824-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0b824-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0b824-183">亞當</span><span class="sxs-lookup"><span data-stu-id="0b824-183">ADAM</span></span>



| <span data-ttu-id="0b824-184">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-184">Entry</span></span> | <span data-ttu-id="0b824-185">值</span><span class="sxs-lookup"><span data-stu-id="0b824-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b824-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b824-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b824-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-187">MAPI-Id</span></span>                | <span data-ttu-id="0b824-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="0b824-188">0x8029</span></span>                          |
| <span data-ttu-id="0b824-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b824-189">System-Only</span></span>            | <span data-ttu-id="0b824-190">對</span><span class="sxs-lookup"><span data-stu-id="0b824-190">True</span></span>                            |
| <span data-ttu-id="0b824-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b824-191">Is-Single-Valued</span></span>       | <span data-ttu-id="0b824-192">對</span><span class="sxs-lookup"><span data-stu-id="0b824-192">True</span></span>                            |
| <span data-ttu-id="0b824-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b824-193">Is Indexed</span></span>             | <span data-ttu-id="0b824-194">對</span><span class="sxs-lookup"><span data-stu-id="0b824-194">True</span></span>                            |
| <span data-ttu-id="0b824-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b824-195">In Global Catalog</span></span>      | <span data-ttu-id="0b824-196">對</span><span class="sxs-lookup"><span data-stu-id="0b824-196">True</span></span>                            |
| <span data-ttu-id="0b824-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b824-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b824-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b824-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b824-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b824-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b824-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b824-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b824-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-201">Search-Flags</span></span>           | <span data-ttu-id="0b824-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="0b824-202">0x00000009</span></span>                      |
| <span data-ttu-id="0b824-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-203">System-Flags</span></span>           | <span data-ttu-id="0b824-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0b824-204">0x00000013</span></span>                      |
| <span data-ttu-id="0b824-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b824-205">Classes used in</span></span>        | [<span data-ttu-id="0b824-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0b824-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b824-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b824-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b824-208">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-208">Entry</span></span> | <span data-ttu-id="0b824-209">值</span><span class="sxs-lookup"><span data-stu-id="0b824-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b824-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b824-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b824-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-211">MAPI-Id</span></span>                | <span data-ttu-id="0b824-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="0b824-212">0x8029</span></span>                          |
| <span data-ttu-id="0b824-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b824-213">System-Only</span></span>            | <span data-ttu-id="0b824-214">對</span><span class="sxs-lookup"><span data-stu-id="0b824-214">True</span></span>                            |
| <span data-ttu-id="0b824-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b824-215">Is-Single-Valued</span></span>       | <span data-ttu-id="0b824-216">對</span><span class="sxs-lookup"><span data-stu-id="0b824-216">True</span></span>                            |
| <span data-ttu-id="0b824-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b824-217">Is Indexed</span></span>             | <span data-ttu-id="0b824-218">對</span><span class="sxs-lookup"><span data-stu-id="0b824-218">True</span></span>                            |
| <span data-ttu-id="0b824-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b824-219">In Global Catalog</span></span>      | <span data-ttu-id="0b824-220">對</span><span class="sxs-lookup"><span data-stu-id="0b824-220">True</span></span>                            |
| <span data-ttu-id="0b824-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b824-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b824-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b824-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b824-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b824-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b824-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b824-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b824-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-225">Search-Flags</span></span>           | <span data-ttu-id="0b824-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="0b824-226">0x00000009</span></span>                      |
| <span data-ttu-id="0b824-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-227">System-Flags</span></span>           | <span data-ttu-id="0b824-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0b824-228">0x00000013</span></span>                      |
| <span data-ttu-id="0b824-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b824-229">Classes used in</span></span>        | [<span data-ttu-id="0b824-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0b824-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b824-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b824-231">Windows Server 2008</span></span>



| <span data-ttu-id="0b824-232">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-232">Entry</span></span> | <span data-ttu-id="0b824-233">值</span><span class="sxs-lookup"><span data-stu-id="0b824-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b824-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b824-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b824-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-235">MAPI-Id</span></span>                | <span data-ttu-id="0b824-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="0b824-236">0x8029</span></span>                          |
| <span data-ttu-id="0b824-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b824-237">System-Only</span></span>            | <span data-ttu-id="0b824-238">對</span><span class="sxs-lookup"><span data-stu-id="0b824-238">True</span></span>                            |
| <span data-ttu-id="0b824-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b824-239">Is-Single-Valued</span></span>       | <span data-ttu-id="0b824-240">對</span><span class="sxs-lookup"><span data-stu-id="0b824-240">True</span></span>                            |
| <span data-ttu-id="0b824-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b824-241">Is Indexed</span></span>             | <span data-ttu-id="0b824-242">對</span><span class="sxs-lookup"><span data-stu-id="0b824-242">True</span></span>                            |
| <span data-ttu-id="0b824-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b824-243">In Global Catalog</span></span>      | <span data-ttu-id="0b824-244">對</span><span class="sxs-lookup"><span data-stu-id="0b824-244">True</span></span>                            |
| <span data-ttu-id="0b824-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b824-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b824-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b824-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b824-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b824-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b824-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b824-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b824-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-249">Search-Flags</span></span>           | <span data-ttu-id="0b824-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="0b824-250">0x00000009</span></span>                      |
| <span data-ttu-id="0b824-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-251">System-Flags</span></span>           | <span data-ttu-id="0b824-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0b824-252">0x00000013</span></span>                      |
| <span data-ttu-id="0b824-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b824-253">Classes used in</span></span>        | [<span data-ttu-id="0b824-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0b824-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b824-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b824-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b824-256">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-256">Entry</span></span> | <span data-ttu-id="0b824-257">值</span><span class="sxs-lookup"><span data-stu-id="0b824-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b824-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b824-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b824-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-259">MAPI-Id</span></span>                | <span data-ttu-id="0b824-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="0b824-260">0x8029</span></span>                          |
| <span data-ttu-id="0b824-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b824-261">System-Only</span></span>            | <span data-ttu-id="0b824-262">對</span><span class="sxs-lookup"><span data-stu-id="0b824-262">True</span></span>                            |
| <span data-ttu-id="0b824-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b824-263">Is-Single-Valued</span></span>       | <span data-ttu-id="0b824-264">對</span><span class="sxs-lookup"><span data-stu-id="0b824-264">True</span></span>                            |
| <span data-ttu-id="0b824-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b824-265">Is Indexed</span></span>             | <span data-ttu-id="0b824-266">對</span><span class="sxs-lookup"><span data-stu-id="0b824-266">True</span></span>                            |
| <span data-ttu-id="0b824-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b824-267">In Global Catalog</span></span>      | <span data-ttu-id="0b824-268">對</span><span class="sxs-lookup"><span data-stu-id="0b824-268">True</span></span>                            |
| <span data-ttu-id="0b824-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b824-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b824-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b824-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b824-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b824-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b824-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b824-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b824-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-273">Search-Flags</span></span>           | <span data-ttu-id="0b824-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="0b824-274">0x00000009</span></span>                      |
| <span data-ttu-id="0b824-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-275">System-Flags</span></span>           | <span data-ttu-id="0b824-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0b824-276">0x00000013</span></span>                      |
| <span data-ttu-id="0b824-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b824-277">Classes used in</span></span>        | [<span data-ttu-id="0b824-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0b824-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b824-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b824-279">Windows Server 2012</span></span>



| <span data-ttu-id="0b824-280">進入</span><span class="sxs-lookup"><span data-stu-id="0b824-280">Entry</span></span> | <span data-ttu-id="0b824-281">值</span><span class="sxs-lookup"><span data-stu-id="0b824-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0b824-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b824-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0b824-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b824-283">MAPI-Id</span></span>                | <span data-ttu-id="0b824-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="0b824-284">0x8029</span></span>                          |
| <span data-ttu-id="0b824-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b824-285">System-Only</span></span>            | <span data-ttu-id="0b824-286">對</span><span class="sxs-lookup"><span data-stu-id="0b824-286">True</span></span>                            |
| <span data-ttu-id="0b824-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b824-287">Is-Single-Valued</span></span>       | <span data-ttu-id="0b824-288">對</span><span class="sxs-lookup"><span data-stu-id="0b824-288">True</span></span>                            |
| <span data-ttu-id="0b824-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b824-289">Is Indexed</span></span>             | <span data-ttu-id="0b824-290">對</span><span class="sxs-lookup"><span data-stu-id="0b824-290">True</span></span>                            |
| <span data-ttu-id="0b824-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b824-291">In Global Catalog</span></span>      | <span data-ttu-id="0b824-292">對</span><span class="sxs-lookup"><span data-stu-id="0b824-292">True</span></span>                            |
| <span data-ttu-id="0b824-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b824-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b824-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b824-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0b824-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b824-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0b824-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b824-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0b824-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-297">Search-Flags</span></span>           | <span data-ttu-id="0b824-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="0b824-298">0x00000009</span></span>                      |
| <span data-ttu-id="0b824-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b824-299">System-Flags</span></span>           | <span data-ttu-id="0b824-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="0b824-300">0x00000013</span></span>                      |
| <span data-ttu-id="0b824-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b824-301">Classes used in</span></span>        | [<span data-ttu-id="0b824-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="0b824-302">**Top**</span></span>](c-top.md)<br/> |



 

 





