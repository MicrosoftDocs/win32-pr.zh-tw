---
title: USN-最新-Obj-已移除屬性
description: 包含從伺服器移除之最後一個系統物件的更新序號 (USN) 。
ms.assetid: af0afd80-fe4a-4bc6-84e3-14c2900bec93
ms.tgt_platform: multiple
keywords:
- USN-DSA-最後一個-Obj-已移除的屬性 AD 架構
- uSNDSALastObjRemoved 屬性 AD 架構
topic_type:
- apiref
api_name:
- USN-DSA-Last-Obj-Removed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbc246aa1a0f7c794b9dc0a9d2a725273a918e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935470"
---
# <a name="usn-dsa-last-obj-removed-attribute"></a><span data-ttu-id="97757-105">USN-最新-Obj-已移除屬性</span><span class="sxs-lookup"><span data-stu-id="97757-105">USN-DSA-Last-Obj-Removed attribute</span></span>

<span data-ttu-id="97757-106">包含從伺服器移除之最後一個系統物件的更新序號 (USN) 。</span><span class="sxs-lookup"><span data-stu-id="97757-106">Contains the update sequence number (USN) for the last system object that was removed from a server.</span></span>



| <span data-ttu-id="97757-107">進入</span><span class="sxs-lookup"><span data-stu-id="97757-107">Entry</span></span> | <span data-ttu-id="97757-108">值</span><span class="sxs-lookup"><span data-stu-id="97757-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="97757-109">CN</span><span class="sxs-lookup"><span data-stu-id="97757-109">CN</span></span>                | <span data-ttu-id="97757-110">USN-已移除-最後-Obj</span><span class="sxs-lookup"><span data-stu-id="97757-110">USN-DSA-Last-Obj-Removed</span></span>             |
| <span data-ttu-id="97757-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="97757-111">Ldap-Display-Name</span></span> | <span data-ttu-id="97757-112">uSNDSALastObjRemoved</span><span class="sxs-lookup"><span data-stu-id="97757-112">uSNDSALastObjRemoved</span></span>                 |
| <span data-ttu-id="97757-113">大小</span><span class="sxs-lookup"><span data-stu-id="97757-113">Size</span></span>              | <span data-ttu-id="97757-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="97757-114">8 bytes</span></span>                              |
| <span data-ttu-id="97757-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="97757-115">Update Privilege</span></span>  | <span data-ttu-id="97757-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="97757-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="97757-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="97757-117">Update Frequency</span></span>  | <span data-ttu-id="97757-118">每當目錄物件變更時。</span><span class="sxs-lookup"><span data-stu-id="97757-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="97757-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="97757-119">Attribute-Id</span></span>      | <span data-ttu-id="97757-120">1.2.840.113556.1.2.267</span><span class="sxs-lookup"><span data-stu-id="97757-120">1.2.840.113556.1.2.267</span></span>               |
| <span data-ttu-id="97757-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="97757-121">System-Id-Guid</span></span>    | <span data-ttu-id="97757-122">bf967a71-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="97757-122">bf967a71-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="97757-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="97757-123">Syntax</span></span>            | [<span data-ttu-id="97757-124">**間隔**</span><span class="sxs-lookup"><span data-stu-id="97757-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="97757-125">實作</span><span class="sxs-lookup"><span data-stu-id="97757-125">Implementations</span></span>

-   [<span data-ttu-id="97757-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="97757-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="97757-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="97757-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="97757-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="97757-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="97757-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="97757-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="97757-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="97757-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="97757-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="97757-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="97757-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="97757-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="97757-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="97757-133">Windows 2000 Server</span></span>



| <span data-ttu-id="97757-134">進入</span><span class="sxs-lookup"><span data-stu-id="97757-134">Entry</span></span> | <span data-ttu-id="97757-135">值</span><span class="sxs-lookup"><span data-stu-id="97757-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97757-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97757-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97757-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97757-137">MAPI-Id</span></span>                | <span data-ttu-id="97757-138">0x8155</span><span class="sxs-lookup"><span data-stu-id="97757-138">0x8155</span></span>                          |
| <span data-ttu-id="97757-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="97757-139">System-Only</span></span>            | <span data-ttu-id="97757-140">對</span><span class="sxs-lookup"><span data-stu-id="97757-140">True</span></span>                            |
| <span data-ttu-id="97757-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97757-141">Is-Single-Valued</span></span>       | <span data-ttu-id="97757-142">對</span><span class="sxs-lookup"><span data-stu-id="97757-142">True</span></span>                            |
| <span data-ttu-id="97757-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97757-143">Is Indexed</span></span>             | <span data-ttu-id="97757-144">否</span><span class="sxs-lookup"><span data-stu-id="97757-144">False</span></span>                           |
| <span data-ttu-id="97757-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97757-145">In Global Catalog</span></span>      | <span data-ttu-id="97757-146">否</span><span class="sxs-lookup"><span data-stu-id="97757-146">False</span></span>                           |
| <span data-ttu-id="97757-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97757-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="97757-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97757-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97757-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97757-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97757-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97757-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97757-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-151">Search-Flags</span></span>           | <span data-ttu-id="97757-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97757-152">0x00000000</span></span>                      |
| <span data-ttu-id="97757-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-153">System-Flags</span></span>           | <span data-ttu-id="97757-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97757-154">0x00000010</span></span>                      |
| <span data-ttu-id="97757-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97757-155">Classes used in</span></span>        | [<span data-ttu-id="97757-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97757-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="97757-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97757-157">Windows Server 2003</span></span>



| <span data-ttu-id="97757-158">進入</span><span class="sxs-lookup"><span data-stu-id="97757-158">Entry</span></span> | <span data-ttu-id="97757-159">值</span><span class="sxs-lookup"><span data-stu-id="97757-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97757-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97757-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97757-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97757-161">MAPI-Id</span></span>                | <span data-ttu-id="97757-162">0x8155</span><span class="sxs-lookup"><span data-stu-id="97757-162">0x8155</span></span>                          |
| <span data-ttu-id="97757-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="97757-163">System-Only</span></span>            | <span data-ttu-id="97757-164">對</span><span class="sxs-lookup"><span data-stu-id="97757-164">True</span></span>                            |
| <span data-ttu-id="97757-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97757-165">Is-Single-Valued</span></span>       | <span data-ttu-id="97757-166">對</span><span class="sxs-lookup"><span data-stu-id="97757-166">True</span></span>                            |
| <span data-ttu-id="97757-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97757-167">Is Indexed</span></span>             | <span data-ttu-id="97757-168">否</span><span class="sxs-lookup"><span data-stu-id="97757-168">False</span></span>                           |
| <span data-ttu-id="97757-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97757-169">In Global Catalog</span></span>      | <span data-ttu-id="97757-170">否</span><span class="sxs-lookup"><span data-stu-id="97757-170">False</span></span>                           |
| <span data-ttu-id="97757-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97757-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="97757-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97757-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97757-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97757-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97757-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97757-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97757-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-175">Search-Flags</span></span>           | <span data-ttu-id="97757-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97757-176">0x00000000</span></span>                      |
| <span data-ttu-id="97757-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-177">System-Flags</span></span>           | <span data-ttu-id="97757-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97757-178">0x00000010</span></span>                      |
| <span data-ttu-id="97757-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97757-179">Classes used in</span></span>        | [<span data-ttu-id="97757-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97757-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="97757-181">亞當</span><span class="sxs-lookup"><span data-stu-id="97757-181">ADAM</span></span>



| <span data-ttu-id="97757-182">進入</span><span class="sxs-lookup"><span data-stu-id="97757-182">Entry</span></span> | <span data-ttu-id="97757-183">值</span><span class="sxs-lookup"><span data-stu-id="97757-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97757-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97757-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97757-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97757-185">MAPI-Id</span></span>                | <span data-ttu-id="97757-186">0x8155</span><span class="sxs-lookup"><span data-stu-id="97757-186">0x8155</span></span>                          |
| <span data-ttu-id="97757-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="97757-187">System-Only</span></span>            | <span data-ttu-id="97757-188">對</span><span class="sxs-lookup"><span data-stu-id="97757-188">True</span></span>                            |
| <span data-ttu-id="97757-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97757-189">Is-Single-Valued</span></span>       | <span data-ttu-id="97757-190">對</span><span class="sxs-lookup"><span data-stu-id="97757-190">True</span></span>                            |
| <span data-ttu-id="97757-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97757-191">Is Indexed</span></span>             | <span data-ttu-id="97757-192">否</span><span class="sxs-lookup"><span data-stu-id="97757-192">False</span></span>                           |
| <span data-ttu-id="97757-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97757-193">In Global Catalog</span></span>      | <span data-ttu-id="97757-194">否</span><span class="sxs-lookup"><span data-stu-id="97757-194">False</span></span>                           |
| <span data-ttu-id="97757-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97757-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="97757-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97757-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97757-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97757-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97757-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97757-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97757-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-199">Search-Flags</span></span>           | <span data-ttu-id="97757-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97757-200">0x00000000</span></span>                      |
| <span data-ttu-id="97757-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-201">System-Flags</span></span>           | <span data-ttu-id="97757-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97757-202">0x00000010</span></span>                      |
| <span data-ttu-id="97757-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97757-203">Classes used in</span></span>        | [<span data-ttu-id="97757-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97757-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="97757-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="97757-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="97757-206">進入</span><span class="sxs-lookup"><span data-stu-id="97757-206">Entry</span></span> | <span data-ttu-id="97757-207">值</span><span class="sxs-lookup"><span data-stu-id="97757-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97757-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97757-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97757-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97757-209">MAPI-Id</span></span>                | <span data-ttu-id="97757-210">0x8155</span><span class="sxs-lookup"><span data-stu-id="97757-210">0x8155</span></span>                          |
| <span data-ttu-id="97757-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="97757-211">System-Only</span></span>            | <span data-ttu-id="97757-212">對</span><span class="sxs-lookup"><span data-stu-id="97757-212">True</span></span>                            |
| <span data-ttu-id="97757-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97757-213">Is-Single-Valued</span></span>       | <span data-ttu-id="97757-214">對</span><span class="sxs-lookup"><span data-stu-id="97757-214">True</span></span>                            |
| <span data-ttu-id="97757-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97757-215">Is Indexed</span></span>             | <span data-ttu-id="97757-216">否</span><span class="sxs-lookup"><span data-stu-id="97757-216">False</span></span>                           |
| <span data-ttu-id="97757-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97757-217">In Global Catalog</span></span>      | <span data-ttu-id="97757-218">否</span><span class="sxs-lookup"><span data-stu-id="97757-218">False</span></span>                           |
| <span data-ttu-id="97757-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97757-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="97757-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97757-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97757-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97757-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97757-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97757-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97757-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-223">Search-Flags</span></span>           | <span data-ttu-id="97757-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97757-224">0x00000000</span></span>                      |
| <span data-ttu-id="97757-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-225">System-Flags</span></span>           | <span data-ttu-id="97757-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97757-226">0x00000010</span></span>                      |
| <span data-ttu-id="97757-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97757-227">Classes used in</span></span>        | [<span data-ttu-id="97757-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97757-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="97757-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97757-229">Windows Server 2008</span></span>



| <span data-ttu-id="97757-230">進入</span><span class="sxs-lookup"><span data-stu-id="97757-230">Entry</span></span> | <span data-ttu-id="97757-231">值</span><span class="sxs-lookup"><span data-stu-id="97757-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97757-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97757-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97757-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97757-233">MAPI-Id</span></span>                | <span data-ttu-id="97757-234">0x8155</span><span class="sxs-lookup"><span data-stu-id="97757-234">0x8155</span></span>                          |
| <span data-ttu-id="97757-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="97757-235">System-Only</span></span>            | <span data-ttu-id="97757-236">對</span><span class="sxs-lookup"><span data-stu-id="97757-236">True</span></span>                            |
| <span data-ttu-id="97757-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97757-237">Is-Single-Valued</span></span>       | <span data-ttu-id="97757-238">對</span><span class="sxs-lookup"><span data-stu-id="97757-238">True</span></span>                            |
| <span data-ttu-id="97757-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97757-239">Is Indexed</span></span>             | <span data-ttu-id="97757-240">否</span><span class="sxs-lookup"><span data-stu-id="97757-240">False</span></span>                           |
| <span data-ttu-id="97757-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97757-241">In Global Catalog</span></span>      | <span data-ttu-id="97757-242">否</span><span class="sxs-lookup"><span data-stu-id="97757-242">False</span></span>                           |
| <span data-ttu-id="97757-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97757-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="97757-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97757-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97757-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97757-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97757-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97757-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97757-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-247">Search-Flags</span></span>           | <span data-ttu-id="97757-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97757-248">0x00000000</span></span>                      |
| <span data-ttu-id="97757-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-249">System-Flags</span></span>           | <span data-ttu-id="97757-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97757-250">0x00000010</span></span>                      |
| <span data-ttu-id="97757-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97757-251">Classes used in</span></span>        | [<span data-ttu-id="97757-252">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97757-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="97757-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97757-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="97757-254">進入</span><span class="sxs-lookup"><span data-stu-id="97757-254">Entry</span></span> | <span data-ttu-id="97757-255">值</span><span class="sxs-lookup"><span data-stu-id="97757-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97757-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97757-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97757-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97757-257">MAPI-Id</span></span>                | <span data-ttu-id="97757-258">0x8155</span><span class="sxs-lookup"><span data-stu-id="97757-258">0x8155</span></span>                          |
| <span data-ttu-id="97757-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="97757-259">System-Only</span></span>            | <span data-ttu-id="97757-260">對</span><span class="sxs-lookup"><span data-stu-id="97757-260">True</span></span>                            |
| <span data-ttu-id="97757-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97757-261">Is-Single-Valued</span></span>       | <span data-ttu-id="97757-262">對</span><span class="sxs-lookup"><span data-stu-id="97757-262">True</span></span>                            |
| <span data-ttu-id="97757-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97757-263">Is Indexed</span></span>             | <span data-ttu-id="97757-264">否</span><span class="sxs-lookup"><span data-stu-id="97757-264">False</span></span>                           |
| <span data-ttu-id="97757-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97757-265">In Global Catalog</span></span>      | <span data-ttu-id="97757-266">否</span><span class="sxs-lookup"><span data-stu-id="97757-266">False</span></span>                           |
| <span data-ttu-id="97757-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97757-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="97757-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97757-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97757-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97757-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97757-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97757-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97757-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-271">Search-Flags</span></span>           | <span data-ttu-id="97757-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97757-272">0x00000000</span></span>                      |
| <span data-ttu-id="97757-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-273">System-Flags</span></span>           | <span data-ttu-id="97757-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97757-274">0x00000010</span></span>                      |
| <span data-ttu-id="97757-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97757-275">Classes used in</span></span>        | [<span data-ttu-id="97757-276">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97757-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="97757-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97757-277">Windows Server 2012</span></span>



| <span data-ttu-id="97757-278">進入</span><span class="sxs-lookup"><span data-stu-id="97757-278">Entry</span></span> | <span data-ttu-id="97757-279">值</span><span class="sxs-lookup"><span data-stu-id="97757-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="97757-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97757-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="97757-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97757-281">MAPI-Id</span></span>                | <span data-ttu-id="97757-282">0x8155</span><span class="sxs-lookup"><span data-stu-id="97757-282">0x8155</span></span>                          |
| <span data-ttu-id="97757-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="97757-283">System-Only</span></span>            | <span data-ttu-id="97757-284">對</span><span class="sxs-lookup"><span data-stu-id="97757-284">True</span></span>                            |
| <span data-ttu-id="97757-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97757-285">Is-Single-Valued</span></span>       | <span data-ttu-id="97757-286">對</span><span class="sxs-lookup"><span data-stu-id="97757-286">True</span></span>                            |
| <span data-ttu-id="97757-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97757-287">Is Indexed</span></span>             | <span data-ttu-id="97757-288">否</span><span class="sxs-lookup"><span data-stu-id="97757-288">False</span></span>                           |
| <span data-ttu-id="97757-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97757-289">In Global Catalog</span></span>      | <span data-ttu-id="97757-290">否</span><span class="sxs-lookup"><span data-stu-id="97757-290">False</span></span>                           |
| <span data-ttu-id="97757-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97757-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="97757-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97757-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="97757-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97757-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="97757-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97757-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="97757-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-295">Search-Flags</span></span>           | <span data-ttu-id="97757-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97757-296">0x00000000</span></span>                      |
| <span data-ttu-id="97757-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97757-297">System-Flags</span></span>           | <span data-ttu-id="97757-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97757-298">0x00000010</span></span>                      |
| <span data-ttu-id="97757-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97757-299">Classes used in</span></span>        | [<span data-ttu-id="97757-300">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="97757-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="97757-301">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97757-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97757-302">**USN-最後-Obj-Rem**</span><span class="sxs-lookup"><span data-stu-id="97757-302">**USN-Last-Obj-Rem**</span></span>](a-usnlastobjrem.md)
</dt> </dl>

 

 





