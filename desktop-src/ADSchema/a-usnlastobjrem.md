---
title: USN-最後-Obj-Rem 屬性
description: 包含從伺服器移除之最後一個非系統物件的更新序號 (USN) 。
ms.assetid: 34718bea-fa19-4084-b97f-d72a1681c3f4
ms.tgt_platform: multiple
keywords:
- USN-Last-Obj-Rem attribute AD 架構
- uSNLastObjRem 屬性 AD 架構
topic_type:
- apiref
api_name:
- USN-Last-Obj-Rem
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9836bd93ca065fdfa53b0246a5bab0142e84ced6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509649"
---
# <a name="usn-last-obj-rem-attribute"></a><span data-ttu-id="ec5fc-105">USN-最後-Obj-Rem 屬性</span><span class="sxs-lookup"><span data-stu-id="ec5fc-105">USN-Last-Obj-Rem attribute</span></span>

<span data-ttu-id="ec5fc-106">包含從伺服器移除之最後一個非系統物件的更新序號 (USN) 。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-106">Contains the update sequence number (USN) for the last non-system object that was removed from a server.</span></span>



| <span data-ttu-id="ec5fc-107">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-107">Entry</span></span> | <span data-ttu-id="ec5fc-108">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ec5fc-109">CN</span><span class="sxs-lookup"><span data-stu-id="ec5fc-109">CN</span></span>                | <span data-ttu-id="ec5fc-110">USN-最後-Obj-Rem</span><span class="sxs-lookup"><span data-stu-id="ec5fc-110">USN-Last-Obj-Rem</span></span>                     |
| <span data-ttu-id="ec5fc-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ec5fc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ec5fc-112">uSNLastObjRem</span><span class="sxs-lookup"><span data-stu-id="ec5fc-112">uSNLastObjRem</span></span>                        |
| <span data-ttu-id="ec5fc-113">大小</span><span class="sxs-lookup"><span data-stu-id="ec5fc-113">Size</span></span>              | <span data-ttu-id="ec5fc-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="ec5fc-114">8 bytes</span></span>                              |
| <span data-ttu-id="ec5fc-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ec5fc-115">Update Privilege</span></span>  | <span data-ttu-id="ec5fc-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ec5fc-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ec5fc-117">Update Frequency</span></span>  | <span data-ttu-id="ec5fc-118">每當目錄物件變更時。</span><span class="sxs-lookup"><span data-stu-id="ec5fc-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="ec5fc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-119">Attribute-Id</span></span>      | <span data-ttu-id="ec5fc-120">1.2.840.113556.1.2.121</span><span class="sxs-lookup"><span data-stu-id="ec5fc-120">1.2.840.113556.1.2.121</span></span>               |
| <span data-ttu-id="ec5fc-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ec5fc-121">System-Id-Guid</span></span>    | <span data-ttu-id="ec5fc-122">bf967a73-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ec5fc-122">bf967a73-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ec5fc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec5fc-123">Syntax</span></span>            | [<span data-ttu-id="ec5fc-124">**間隔**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ec5fc-125">實作</span><span class="sxs-lookup"><span data-stu-id="ec5fc-125">Implementations</span></span>

-   [<span data-ttu-id="ec5fc-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec5fc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec5fc-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ec5fc-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec5fc-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec5fc-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec5fc-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec5fc-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec5fc-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ec5fc-134">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-134">Entry</span></span> | <span data-ttu-id="ec5fc-135">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec5fc-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec5fc-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec5fc-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-137">MAPI-Id</span></span>                | <span data-ttu-id="ec5fc-138">0x8156</span><span class="sxs-lookup"><span data-stu-id="ec5fc-138">0x8156</span></span>                          |
| <span data-ttu-id="ec5fc-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5fc-139">System-Only</span></span>            | <span data-ttu-id="ec5fc-140">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-140">True</span></span>                            |
| <span data-ttu-id="ec5fc-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5fc-142">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-142">True</span></span>                            |
| <span data-ttu-id="ec5fc-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec5fc-143">Is Indexed</span></span>             | <span data-ttu-id="ec5fc-144">否</span><span class="sxs-lookup"><span data-stu-id="ec5fc-144">False</span></span>                           |
| <span data-ttu-id="ec5fc-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec5fc-145">In Global Catalog</span></span>      | <span data-ttu-id="ec5fc-146">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-146">True</span></span>                            |
| <span data-ttu-id="ec5fc-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec5fc-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5fc-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec5fc-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec5fc-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5fc-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5fc-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-151">Search-Flags</span></span>           | <span data-ttu-id="ec5fc-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5fc-152">0x00000000</span></span>                      |
| <span data-ttu-id="ec5fc-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-153">System-Flags</span></span>           | <span data-ttu-id="ec5fc-154">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ec5fc-154">0x00000013</span></span>                      |
| <span data-ttu-id="ec5fc-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec5fc-155">Classes used in</span></span>        | [<span data-ttu-id="ec5fc-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec5fc-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec5fc-157">Windows Server 2003</span></span>



| <span data-ttu-id="ec5fc-158">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-158">Entry</span></span> | <span data-ttu-id="ec5fc-159">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec5fc-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec5fc-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec5fc-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-161">MAPI-Id</span></span>                | <span data-ttu-id="ec5fc-162">0x8156</span><span class="sxs-lookup"><span data-stu-id="ec5fc-162">0x8156</span></span>                          |
| <span data-ttu-id="ec5fc-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5fc-163">System-Only</span></span>            | <span data-ttu-id="ec5fc-164">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-164">True</span></span>                            |
| <span data-ttu-id="ec5fc-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5fc-166">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-166">True</span></span>                            |
| <span data-ttu-id="ec5fc-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec5fc-167">Is Indexed</span></span>             | <span data-ttu-id="ec5fc-168">否</span><span class="sxs-lookup"><span data-stu-id="ec5fc-168">False</span></span>                           |
| <span data-ttu-id="ec5fc-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec5fc-169">In Global Catalog</span></span>      | <span data-ttu-id="ec5fc-170">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-170">True</span></span>                            |
| <span data-ttu-id="ec5fc-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec5fc-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5fc-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec5fc-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec5fc-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5fc-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5fc-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-175">Search-Flags</span></span>           | <span data-ttu-id="ec5fc-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5fc-176">0x00000000</span></span>                      |
| <span data-ttu-id="ec5fc-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-177">System-Flags</span></span>           | <span data-ttu-id="ec5fc-178">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ec5fc-178">0x00000013</span></span>                      |
| <span data-ttu-id="ec5fc-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec5fc-179">Classes used in</span></span>        | [<span data-ttu-id="ec5fc-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ec5fc-181">亞當</span><span class="sxs-lookup"><span data-stu-id="ec5fc-181">ADAM</span></span>



| <span data-ttu-id="ec5fc-182">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-182">Entry</span></span> | <span data-ttu-id="ec5fc-183">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec5fc-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec5fc-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec5fc-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-185">MAPI-Id</span></span>                | <span data-ttu-id="ec5fc-186">0x8156</span><span class="sxs-lookup"><span data-stu-id="ec5fc-186">0x8156</span></span>                          |
| <span data-ttu-id="ec5fc-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5fc-187">System-Only</span></span>            | <span data-ttu-id="ec5fc-188">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-188">True</span></span>                            |
| <span data-ttu-id="ec5fc-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5fc-190">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-190">True</span></span>                            |
| <span data-ttu-id="ec5fc-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec5fc-191">Is Indexed</span></span>             | <span data-ttu-id="ec5fc-192">否</span><span class="sxs-lookup"><span data-stu-id="ec5fc-192">False</span></span>                           |
| <span data-ttu-id="ec5fc-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec5fc-193">In Global Catalog</span></span>      | <span data-ttu-id="ec5fc-194">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-194">True</span></span>                            |
| <span data-ttu-id="ec5fc-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec5fc-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5fc-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec5fc-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec5fc-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5fc-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5fc-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-199">Search-Flags</span></span>           | <span data-ttu-id="ec5fc-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5fc-200">0x00000000</span></span>                      |
| <span data-ttu-id="ec5fc-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-201">System-Flags</span></span>           | <span data-ttu-id="ec5fc-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ec5fc-202">0x00000013</span></span>                      |
| <span data-ttu-id="ec5fc-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec5fc-203">Classes used in</span></span>        | [<span data-ttu-id="ec5fc-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec5fc-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec5fc-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec5fc-206">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-206">Entry</span></span> | <span data-ttu-id="ec5fc-207">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec5fc-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec5fc-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec5fc-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-209">MAPI-Id</span></span>                | <span data-ttu-id="ec5fc-210">0x8156</span><span class="sxs-lookup"><span data-stu-id="ec5fc-210">0x8156</span></span>                          |
| <span data-ttu-id="ec5fc-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5fc-211">System-Only</span></span>            | <span data-ttu-id="ec5fc-212">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-212">True</span></span>                            |
| <span data-ttu-id="ec5fc-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-213">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5fc-214">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-214">True</span></span>                            |
| <span data-ttu-id="ec5fc-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec5fc-215">Is Indexed</span></span>             | <span data-ttu-id="ec5fc-216">否</span><span class="sxs-lookup"><span data-stu-id="ec5fc-216">False</span></span>                           |
| <span data-ttu-id="ec5fc-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec5fc-217">In Global Catalog</span></span>      | <span data-ttu-id="ec5fc-218">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-218">True</span></span>                            |
| <span data-ttu-id="ec5fc-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec5fc-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5fc-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec5fc-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec5fc-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5fc-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5fc-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-223">Search-Flags</span></span>           | <span data-ttu-id="ec5fc-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5fc-224">0x00000000</span></span>                      |
| <span data-ttu-id="ec5fc-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-225">System-Flags</span></span>           | <span data-ttu-id="ec5fc-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ec5fc-226">0x00000013</span></span>                      |
| <span data-ttu-id="ec5fc-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec5fc-227">Classes used in</span></span>        | [<span data-ttu-id="ec5fc-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec5fc-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec5fc-229">Windows Server 2008</span></span>



| <span data-ttu-id="ec5fc-230">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-230">Entry</span></span> | <span data-ttu-id="ec5fc-231">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec5fc-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec5fc-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec5fc-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-233">MAPI-Id</span></span>                | <span data-ttu-id="ec5fc-234">0x8156</span><span class="sxs-lookup"><span data-stu-id="ec5fc-234">0x8156</span></span>                          |
| <span data-ttu-id="ec5fc-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5fc-235">System-Only</span></span>            | <span data-ttu-id="ec5fc-236">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-236">True</span></span>                            |
| <span data-ttu-id="ec5fc-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5fc-238">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-238">True</span></span>                            |
| <span data-ttu-id="ec5fc-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec5fc-239">Is Indexed</span></span>             | <span data-ttu-id="ec5fc-240">否</span><span class="sxs-lookup"><span data-stu-id="ec5fc-240">False</span></span>                           |
| <span data-ttu-id="ec5fc-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec5fc-241">In Global Catalog</span></span>      | <span data-ttu-id="ec5fc-242">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-242">True</span></span>                            |
| <span data-ttu-id="ec5fc-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec5fc-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5fc-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec5fc-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec5fc-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5fc-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5fc-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-247">Search-Flags</span></span>           | <span data-ttu-id="ec5fc-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5fc-248">0x00000000</span></span>                      |
| <span data-ttu-id="ec5fc-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-249">System-Flags</span></span>           | <span data-ttu-id="ec5fc-250">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ec5fc-250">0x00000013</span></span>                      |
| <span data-ttu-id="ec5fc-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec5fc-251">Classes used in</span></span>        | [<span data-ttu-id="ec5fc-252">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec5fc-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec5fc-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec5fc-254">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-254">Entry</span></span> | <span data-ttu-id="ec5fc-255">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec5fc-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec5fc-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec5fc-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-257">MAPI-Id</span></span>                | <span data-ttu-id="ec5fc-258">0x8156</span><span class="sxs-lookup"><span data-stu-id="ec5fc-258">0x8156</span></span>                          |
| <span data-ttu-id="ec5fc-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5fc-259">System-Only</span></span>            | <span data-ttu-id="ec5fc-260">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-260">True</span></span>                            |
| <span data-ttu-id="ec5fc-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-261">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5fc-262">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-262">True</span></span>                            |
| <span data-ttu-id="ec5fc-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec5fc-263">Is Indexed</span></span>             | <span data-ttu-id="ec5fc-264">否</span><span class="sxs-lookup"><span data-stu-id="ec5fc-264">False</span></span>                           |
| <span data-ttu-id="ec5fc-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec5fc-265">In Global Catalog</span></span>      | <span data-ttu-id="ec5fc-266">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-266">True</span></span>                            |
| <span data-ttu-id="ec5fc-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec5fc-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5fc-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec5fc-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec5fc-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5fc-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5fc-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-271">Search-Flags</span></span>           | <span data-ttu-id="ec5fc-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5fc-272">0x00000000</span></span>                      |
| <span data-ttu-id="ec5fc-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-273">System-Flags</span></span>           | <span data-ttu-id="ec5fc-274">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ec5fc-274">0x00000013</span></span>                      |
| <span data-ttu-id="ec5fc-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec5fc-275">Classes used in</span></span>        | [<span data-ttu-id="ec5fc-276">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec5fc-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec5fc-277">Windows Server 2012</span></span>



| <span data-ttu-id="ec5fc-278">進入</span><span class="sxs-lookup"><span data-stu-id="ec5fc-278">Entry</span></span> | <span data-ttu-id="ec5fc-279">值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ec5fc-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec5fc-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ec5fc-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec5fc-281">MAPI-Id</span></span>                | <span data-ttu-id="ec5fc-282">0x8156</span><span class="sxs-lookup"><span data-stu-id="ec5fc-282">0x8156</span></span>                          |
| <span data-ttu-id="ec5fc-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec5fc-283">System-Only</span></span>            | <span data-ttu-id="ec5fc-284">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-284">True</span></span>                            |
| <span data-ttu-id="ec5fc-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec5fc-285">Is-Single-Valued</span></span>       | <span data-ttu-id="ec5fc-286">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-286">True</span></span>                            |
| <span data-ttu-id="ec5fc-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec5fc-287">Is Indexed</span></span>             | <span data-ttu-id="ec5fc-288">否</span><span class="sxs-lookup"><span data-stu-id="ec5fc-288">False</span></span>                           |
| <span data-ttu-id="ec5fc-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec5fc-289">In Global Catalog</span></span>      | <span data-ttu-id="ec5fc-290">對</span><span class="sxs-lookup"><span data-stu-id="ec5fc-290">True</span></span>                            |
| <span data-ttu-id="ec5fc-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec5fc-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec5fc-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec5fc-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ec5fc-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec5fc-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec5fc-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ec5fc-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-295">Search-Flags</span></span>           | <span data-ttu-id="ec5fc-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec5fc-296">0x00000000</span></span>                      |
| <span data-ttu-id="ec5fc-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec5fc-297">System-Flags</span></span>           | <span data-ttu-id="ec5fc-298">0x00000013</span><span class="sxs-lookup"><span data-stu-id="ec5fc-298">0x00000013</span></span>                      |
| <span data-ttu-id="ec5fc-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec5fc-299">Classes used in</span></span>        | [<span data-ttu-id="ec5fc-300">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="ec5fc-301">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec5fc-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5fc-302">**USN-已移除-最後-Obj**</span><span class="sxs-lookup"><span data-stu-id="ec5fc-302">**USN-DSA-Last-Obj-Removed**</span></span>](a-usndsalastobjremoved.md)
</dt> </dl>

 

 





