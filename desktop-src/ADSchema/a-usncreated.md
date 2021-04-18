---
title: USN-Created 屬性
description: 更新序號 (USN) 在建立物件時指派。 另請參閱 USN 變更。
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- USN-Created 屬性 AD 架構
- uSNCreated 屬性 AD 架構
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b950ddfe261de5d46980e51b236da0f775fcb01b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106969014"
---
# <a name="usn-created-attribute"></a><span data-ttu-id="6d297-106">USN-Created 屬性</span><span class="sxs-lookup"><span data-stu-id="6d297-106">USN-Created attribute</span></span>

<span data-ttu-id="6d297-107">更新序號 (USN) 在建立物件時指派。</span><span class="sxs-lookup"><span data-stu-id="6d297-107">The update sequence number (USN) assigned at object creation.</span></span> <span data-ttu-id="6d297-108">另請參閱 [**USN 變更**](a-usnchanged.md)。</span><span class="sxs-lookup"><span data-stu-id="6d297-108">See also, [**USN-Changed**](a-usnchanged.md).</span></span>



| <span data-ttu-id="6d297-109">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-109">Entry</span></span> | <span data-ttu-id="6d297-110">值</span><span class="sxs-lookup"><span data-stu-id="6d297-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6d297-111">CN</span><span class="sxs-lookup"><span data-stu-id="6d297-111">CN</span></span>                | <span data-ttu-id="6d297-112">USN-Created</span><span class="sxs-lookup"><span data-stu-id="6d297-112">USN-Created</span></span>                          |
| <span data-ttu-id="6d297-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6d297-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6d297-114">uSNCreated</span><span class="sxs-lookup"><span data-stu-id="6d297-114">uSNCreated</span></span>                           |
| <span data-ttu-id="6d297-115">大小</span><span class="sxs-lookup"><span data-stu-id="6d297-115">Size</span></span>              | <span data-ttu-id="6d297-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="6d297-116">8 bytes</span></span>                              |
| <span data-ttu-id="6d297-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6d297-117">Update Privilege</span></span>  | <span data-ttu-id="6d297-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="6d297-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="6d297-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6d297-119">Update Frequency</span></span>  | <span data-ttu-id="6d297-120">建立物件時。</span><span class="sxs-lookup"><span data-stu-id="6d297-120">When the object is created.</span></span>          |
| <span data-ttu-id="6d297-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-121">Attribute-Id</span></span>      | <span data-ttu-id="6d297-122">1.2.840.113556.1.2.19</span><span class="sxs-lookup"><span data-stu-id="6d297-122">1.2.840.113556.1.2.19</span></span>                |
| <span data-ttu-id="6d297-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6d297-123">System-Id-Guid</span></span>    | <span data-ttu-id="6d297-124">bf967a70-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6d297-124">bf967a70-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6d297-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d297-125">Syntax</span></span>            | [<span data-ttu-id="6d297-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="6d297-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6d297-127">實作</span><span class="sxs-lookup"><span data-stu-id="6d297-127">Implementations</span></span>

-   [<span data-ttu-id="6d297-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d297-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d297-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d297-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d297-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6d297-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6d297-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d297-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d297-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d297-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d297-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d297-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d297-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d297-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d297-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d297-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6d297-136">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-136">Entry</span></span> | <span data-ttu-id="6d297-137">值</span><span class="sxs-lookup"><span data-stu-id="6d297-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d297-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6d297-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d297-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-139">MAPI-Id</span></span>                | <span data-ttu-id="6d297-140">0x8154</span><span class="sxs-lookup"><span data-stu-id="6d297-140">0x8154</span></span>                          |
| <span data-ttu-id="6d297-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d297-141">System-Only</span></span>            | <span data-ttu-id="6d297-142">對</span><span class="sxs-lookup"><span data-stu-id="6d297-142">True</span></span>                            |
| <span data-ttu-id="6d297-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6d297-143">Is-Single-Valued</span></span>       | <span data-ttu-id="6d297-144">對</span><span class="sxs-lookup"><span data-stu-id="6d297-144">True</span></span>                            |
| <span data-ttu-id="6d297-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6d297-145">Is Indexed</span></span>             | <span data-ttu-id="6d297-146">對</span><span class="sxs-lookup"><span data-stu-id="6d297-146">True</span></span>                            |
| <span data-ttu-id="6d297-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6d297-147">In Global Catalog</span></span>      | <span data-ttu-id="6d297-148">對</span><span class="sxs-lookup"><span data-stu-id="6d297-148">True</span></span>                            |
| <span data-ttu-id="6d297-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6d297-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d297-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6d297-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d297-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d297-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d297-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d297-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d297-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-153">Search-Flags</span></span>           | <span data-ttu-id="6d297-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6d297-154">0x00000009</span></span>                      |
| <span data-ttu-id="6d297-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-155">System-Flags</span></span>           | <span data-ttu-id="6d297-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6d297-156">0x00000013</span></span>                      |
| <span data-ttu-id="6d297-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6d297-157">Classes used in</span></span>        | [<span data-ttu-id="6d297-158">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6d297-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d297-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d297-159">Windows Server 2003</span></span>



| <span data-ttu-id="6d297-160">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-160">Entry</span></span> | <span data-ttu-id="6d297-161">值</span><span class="sxs-lookup"><span data-stu-id="6d297-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d297-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6d297-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d297-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-163">MAPI-Id</span></span>                | <span data-ttu-id="6d297-164">0x8154</span><span class="sxs-lookup"><span data-stu-id="6d297-164">0x8154</span></span>                          |
| <span data-ttu-id="6d297-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d297-165">System-Only</span></span>            | <span data-ttu-id="6d297-166">對</span><span class="sxs-lookup"><span data-stu-id="6d297-166">True</span></span>                            |
| <span data-ttu-id="6d297-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6d297-167">Is-Single-Valued</span></span>       | <span data-ttu-id="6d297-168">對</span><span class="sxs-lookup"><span data-stu-id="6d297-168">True</span></span>                            |
| <span data-ttu-id="6d297-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6d297-169">Is Indexed</span></span>             | <span data-ttu-id="6d297-170">對</span><span class="sxs-lookup"><span data-stu-id="6d297-170">True</span></span>                            |
| <span data-ttu-id="6d297-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6d297-171">In Global Catalog</span></span>      | <span data-ttu-id="6d297-172">對</span><span class="sxs-lookup"><span data-stu-id="6d297-172">True</span></span>                            |
| <span data-ttu-id="6d297-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6d297-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d297-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6d297-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d297-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d297-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d297-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d297-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d297-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-177">Search-Flags</span></span>           | <span data-ttu-id="6d297-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6d297-178">0x00000009</span></span>                      |
| <span data-ttu-id="6d297-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-179">System-Flags</span></span>           | <span data-ttu-id="6d297-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6d297-180">0x00000013</span></span>                      |
| <span data-ttu-id="6d297-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6d297-181">Classes used in</span></span>        | [<span data-ttu-id="6d297-182">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6d297-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6d297-183">亞當</span><span class="sxs-lookup"><span data-stu-id="6d297-183">ADAM</span></span>



| <span data-ttu-id="6d297-184">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-184">Entry</span></span> | <span data-ttu-id="6d297-185">值</span><span class="sxs-lookup"><span data-stu-id="6d297-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d297-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6d297-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d297-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-187">MAPI-Id</span></span>                | <span data-ttu-id="6d297-188">0x8154</span><span class="sxs-lookup"><span data-stu-id="6d297-188">0x8154</span></span>                          |
| <span data-ttu-id="6d297-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d297-189">System-Only</span></span>            | <span data-ttu-id="6d297-190">對</span><span class="sxs-lookup"><span data-stu-id="6d297-190">True</span></span>                            |
| <span data-ttu-id="6d297-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6d297-191">Is-Single-Valued</span></span>       | <span data-ttu-id="6d297-192">對</span><span class="sxs-lookup"><span data-stu-id="6d297-192">True</span></span>                            |
| <span data-ttu-id="6d297-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6d297-193">Is Indexed</span></span>             | <span data-ttu-id="6d297-194">對</span><span class="sxs-lookup"><span data-stu-id="6d297-194">True</span></span>                            |
| <span data-ttu-id="6d297-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6d297-195">In Global Catalog</span></span>      | <span data-ttu-id="6d297-196">對</span><span class="sxs-lookup"><span data-stu-id="6d297-196">True</span></span>                            |
| <span data-ttu-id="6d297-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6d297-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d297-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6d297-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d297-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d297-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d297-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d297-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d297-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-201">Search-Flags</span></span>           | <span data-ttu-id="6d297-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6d297-202">0x00000009</span></span>                      |
| <span data-ttu-id="6d297-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-203">System-Flags</span></span>           | <span data-ttu-id="6d297-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6d297-204">0x00000013</span></span>                      |
| <span data-ttu-id="6d297-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6d297-205">Classes used in</span></span>        | [<span data-ttu-id="6d297-206">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6d297-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d297-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d297-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d297-208">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-208">Entry</span></span> | <span data-ttu-id="6d297-209">值</span><span class="sxs-lookup"><span data-stu-id="6d297-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d297-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6d297-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d297-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-211">MAPI-Id</span></span>                | <span data-ttu-id="6d297-212">0x8154</span><span class="sxs-lookup"><span data-stu-id="6d297-212">0x8154</span></span>                          |
| <span data-ttu-id="6d297-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d297-213">System-Only</span></span>            | <span data-ttu-id="6d297-214">對</span><span class="sxs-lookup"><span data-stu-id="6d297-214">True</span></span>                            |
| <span data-ttu-id="6d297-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6d297-215">Is-Single-Valued</span></span>       | <span data-ttu-id="6d297-216">對</span><span class="sxs-lookup"><span data-stu-id="6d297-216">True</span></span>                            |
| <span data-ttu-id="6d297-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6d297-217">Is Indexed</span></span>             | <span data-ttu-id="6d297-218">對</span><span class="sxs-lookup"><span data-stu-id="6d297-218">True</span></span>                            |
| <span data-ttu-id="6d297-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6d297-219">In Global Catalog</span></span>      | <span data-ttu-id="6d297-220">對</span><span class="sxs-lookup"><span data-stu-id="6d297-220">True</span></span>                            |
| <span data-ttu-id="6d297-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6d297-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d297-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6d297-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d297-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d297-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d297-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d297-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d297-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-225">Search-Flags</span></span>           | <span data-ttu-id="6d297-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6d297-226">0x00000009</span></span>                      |
| <span data-ttu-id="6d297-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-227">System-Flags</span></span>           | <span data-ttu-id="6d297-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6d297-228">0x00000013</span></span>                      |
| <span data-ttu-id="6d297-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6d297-229">Classes used in</span></span>        | [<span data-ttu-id="6d297-230">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6d297-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d297-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d297-231">Windows Server 2008</span></span>



| <span data-ttu-id="6d297-232">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-232">Entry</span></span> | <span data-ttu-id="6d297-233">值</span><span class="sxs-lookup"><span data-stu-id="6d297-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d297-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6d297-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d297-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-235">MAPI-Id</span></span>                | <span data-ttu-id="6d297-236">0x8154</span><span class="sxs-lookup"><span data-stu-id="6d297-236">0x8154</span></span>                          |
| <span data-ttu-id="6d297-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d297-237">System-Only</span></span>            | <span data-ttu-id="6d297-238">對</span><span class="sxs-lookup"><span data-stu-id="6d297-238">True</span></span>                            |
| <span data-ttu-id="6d297-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6d297-239">Is-Single-Valued</span></span>       | <span data-ttu-id="6d297-240">對</span><span class="sxs-lookup"><span data-stu-id="6d297-240">True</span></span>                            |
| <span data-ttu-id="6d297-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6d297-241">Is Indexed</span></span>             | <span data-ttu-id="6d297-242">對</span><span class="sxs-lookup"><span data-stu-id="6d297-242">True</span></span>                            |
| <span data-ttu-id="6d297-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6d297-243">In Global Catalog</span></span>      | <span data-ttu-id="6d297-244">對</span><span class="sxs-lookup"><span data-stu-id="6d297-244">True</span></span>                            |
| <span data-ttu-id="6d297-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6d297-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d297-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6d297-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d297-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d297-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d297-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d297-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d297-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-249">Search-Flags</span></span>           | <span data-ttu-id="6d297-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6d297-250">0x00000009</span></span>                      |
| <span data-ttu-id="6d297-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-251">System-Flags</span></span>           | <span data-ttu-id="6d297-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6d297-252">0x00000013</span></span>                      |
| <span data-ttu-id="6d297-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6d297-253">Classes used in</span></span>        | [<span data-ttu-id="6d297-254">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6d297-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d297-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d297-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d297-256">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-256">Entry</span></span> | <span data-ttu-id="6d297-257">值</span><span class="sxs-lookup"><span data-stu-id="6d297-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d297-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6d297-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d297-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-259">MAPI-Id</span></span>                | <span data-ttu-id="6d297-260">0x8154</span><span class="sxs-lookup"><span data-stu-id="6d297-260">0x8154</span></span>                          |
| <span data-ttu-id="6d297-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d297-261">System-Only</span></span>            | <span data-ttu-id="6d297-262">對</span><span class="sxs-lookup"><span data-stu-id="6d297-262">True</span></span>                            |
| <span data-ttu-id="6d297-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6d297-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6d297-264">對</span><span class="sxs-lookup"><span data-stu-id="6d297-264">True</span></span>                            |
| <span data-ttu-id="6d297-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6d297-265">Is Indexed</span></span>             | <span data-ttu-id="6d297-266">對</span><span class="sxs-lookup"><span data-stu-id="6d297-266">True</span></span>                            |
| <span data-ttu-id="6d297-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6d297-267">In Global Catalog</span></span>      | <span data-ttu-id="6d297-268">對</span><span class="sxs-lookup"><span data-stu-id="6d297-268">True</span></span>                            |
| <span data-ttu-id="6d297-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6d297-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d297-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6d297-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d297-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d297-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d297-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d297-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d297-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-273">Search-Flags</span></span>           | <span data-ttu-id="6d297-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6d297-274">0x00000009</span></span>                      |
| <span data-ttu-id="6d297-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-275">System-Flags</span></span>           | <span data-ttu-id="6d297-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6d297-276">0x00000013</span></span>                      |
| <span data-ttu-id="6d297-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6d297-277">Classes used in</span></span>        | [<span data-ttu-id="6d297-278">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6d297-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d297-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d297-279">Windows Server 2012</span></span>



| <span data-ttu-id="6d297-280">進入</span><span class="sxs-lookup"><span data-stu-id="6d297-280">Entry</span></span> | <span data-ttu-id="6d297-281">值</span><span class="sxs-lookup"><span data-stu-id="6d297-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6d297-282">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6d297-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6d297-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d297-283">MAPI-Id</span></span>                | <span data-ttu-id="6d297-284">0x8154</span><span class="sxs-lookup"><span data-stu-id="6d297-284">0x8154</span></span>                          |
| <span data-ttu-id="6d297-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d297-285">System-Only</span></span>            | <span data-ttu-id="6d297-286">對</span><span class="sxs-lookup"><span data-stu-id="6d297-286">True</span></span>                            |
| <span data-ttu-id="6d297-287">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6d297-287">Is-Single-Valued</span></span>       | <span data-ttu-id="6d297-288">對</span><span class="sxs-lookup"><span data-stu-id="6d297-288">True</span></span>                            |
| <span data-ttu-id="6d297-289">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6d297-289">Is Indexed</span></span>             | <span data-ttu-id="6d297-290">對</span><span class="sxs-lookup"><span data-stu-id="6d297-290">True</span></span>                            |
| <span data-ttu-id="6d297-291">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6d297-291">In Global Catalog</span></span>      | <span data-ttu-id="6d297-292">對</span><span class="sxs-lookup"><span data-stu-id="6d297-292">True</span></span>                            |
| <span data-ttu-id="6d297-293">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6d297-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d297-294">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6d297-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6d297-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d297-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6d297-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d297-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6d297-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-297">Search-Flags</span></span>           | <span data-ttu-id="6d297-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6d297-298">0x00000009</span></span>                      |
| <span data-ttu-id="6d297-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d297-299">System-Flags</span></span>           | <span data-ttu-id="6d297-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6d297-300">0x00000013</span></span>                      |
| <span data-ttu-id="6d297-301">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6d297-301">Classes used in</span></span>        | [<span data-ttu-id="6d297-302">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6d297-302">**Top**</span></span>](c-top.md)<br/> |



 

 





