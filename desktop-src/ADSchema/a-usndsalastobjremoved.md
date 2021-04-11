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
# <a name="usn-dsa-last-obj-removed-attribute"></a><span data-ttu-id="87085-105">USN-最新-Obj-已移除屬性</span><span class="sxs-lookup"><span data-stu-id="87085-105">USN-DSA-Last-Obj-Removed attribute</span></span>

<span data-ttu-id="87085-106">包含從伺服器移除之最後一個系統物件的更新序號 (USN) 。</span><span class="sxs-lookup"><span data-stu-id="87085-106">Contains the update sequence number (USN) for the last system object that was removed from a server.</span></span>



| <span data-ttu-id="87085-107">進入</span><span class="sxs-lookup"><span data-stu-id="87085-107">Entry</span></span> | <span data-ttu-id="87085-108">值</span><span class="sxs-lookup"><span data-stu-id="87085-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="87085-109">CN</span><span class="sxs-lookup"><span data-stu-id="87085-109">CN</span></span>                | <span data-ttu-id="87085-110">USN-已移除-最後-Obj</span><span class="sxs-lookup"><span data-stu-id="87085-110">USN-DSA-Last-Obj-Removed</span></span>             |
| <span data-ttu-id="87085-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="87085-111">Ldap-Display-Name</span></span> | <span data-ttu-id="87085-112">uSNDSALastObjRemoved</span><span class="sxs-lookup"><span data-stu-id="87085-112">uSNDSALastObjRemoved</span></span>                 |
| <span data-ttu-id="87085-113">大小</span><span class="sxs-lookup"><span data-stu-id="87085-113">Size</span></span>              | <span data-ttu-id="87085-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="87085-114">8 bytes</span></span>                              |
| <span data-ttu-id="87085-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="87085-115">Update Privilege</span></span>  | <span data-ttu-id="87085-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="87085-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="87085-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="87085-117">Update Frequency</span></span>  | <span data-ttu-id="87085-118">每當目錄物件變更時。</span><span class="sxs-lookup"><span data-stu-id="87085-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="87085-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="87085-119">Attribute-Id</span></span>      | <span data-ttu-id="87085-120">1.2.840.113556.1.2.267</span><span class="sxs-lookup"><span data-stu-id="87085-120">1.2.840.113556.1.2.267</span></span>               |
| <span data-ttu-id="87085-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="87085-121">System-Id-Guid</span></span>    | <span data-ttu-id="87085-122">bf967a71-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="87085-122">bf967a71-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="87085-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="87085-123">Syntax</span></span>            | [<span data-ttu-id="87085-124">**間隔**</span><span class="sxs-lookup"><span data-stu-id="87085-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="87085-125">實作</span><span class="sxs-lookup"><span data-stu-id="87085-125">Implementations</span></span>

-   [<span data-ttu-id="87085-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="87085-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="87085-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="87085-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="87085-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="87085-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="87085-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="87085-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="87085-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="87085-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="87085-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="87085-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="87085-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="87085-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="87085-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="87085-133">Windows 2000 Server</span></span>



| <span data-ttu-id="87085-134">進入</span><span class="sxs-lookup"><span data-stu-id="87085-134">Entry</span></span> | <span data-ttu-id="87085-135">值</span><span class="sxs-lookup"><span data-stu-id="87085-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="87085-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87085-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="87085-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87085-137">MAPI-Id</span></span>                | <span data-ttu-id="87085-138">0x8155</span><span class="sxs-lookup"><span data-stu-id="87085-138">0x8155</span></span>                          |
| <span data-ttu-id="87085-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="87085-139">System-Only</span></span>            | <span data-ttu-id="87085-140">對</span><span class="sxs-lookup"><span data-stu-id="87085-140">True</span></span>                            |
| <span data-ttu-id="87085-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87085-141">Is-Single-Valued</span></span>       | <span data-ttu-id="87085-142">對</span><span class="sxs-lookup"><span data-stu-id="87085-142">True</span></span>                            |
| <span data-ttu-id="87085-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87085-143">Is Indexed</span></span>             | <span data-ttu-id="87085-144">否</span><span class="sxs-lookup"><span data-stu-id="87085-144">False</span></span>                           |
| <span data-ttu-id="87085-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87085-145">In Global Catalog</span></span>      | <span data-ttu-id="87085-146">否</span><span class="sxs-lookup"><span data-stu-id="87085-146">False</span></span>                           |
| <span data-ttu-id="87085-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87085-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="87085-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87085-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="87085-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87085-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="87085-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87085-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="87085-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-151">Search-Flags</span></span>           | <span data-ttu-id="87085-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87085-152">0x00000000</span></span>                      |
| <span data-ttu-id="87085-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-153">System-Flags</span></span>           | <span data-ttu-id="87085-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87085-154">0x00000010</span></span>                      |
| <span data-ttu-id="87085-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87085-155">Classes used in</span></span>        | [<span data-ttu-id="87085-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="87085-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="87085-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="87085-157">Windows Server 2003</span></span>



| <span data-ttu-id="87085-158">進入</span><span class="sxs-lookup"><span data-stu-id="87085-158">Entry</span></span> | <span data-ttu-id="87085-159">值</span><span class="sxs-lookup"><span data-stu-id="87085-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="87085-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87085-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="87085-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87085-161">MAPI-Id</span></span>                | <span data-ttu-id="87085-162">0x8155</span><span class="sxs-lookup"><span data-stu-id="87085-162">0x8155</span></span>                          |
| <span data-ttu-id="87085-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="87085-163">System-Only</span></span>            | <span data-ttu-id="87085-164">對</span><span class="sxs-lookup"><span data-stu-id="87085-164">True</span></span>                            |
| <span data-ttu-id="87085-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87085-165">Is-Single-Valued</span></span>       | <span data-ttu-id="87085-166">對</span><span class="sxs-lookup"><span data-stu-id="87085-166">True</span></span>                            |
| <span data-ttu-id="87085-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87085-167">Is Indexed</span></span>             | <span data-ttu-id="87085-168">否</span><span class="sxs-lookup"><span data-stu-id="87085-168">False</span></span>                           |
| <span data-ttu-id="87085-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87085-169">In Global Catalog</span></span>      | <span data-ttu-id="87085-170">否</span><span class="sxs-lookup"><span data-stu-id="87085-170">False</span></span>                           |
| <span data-ttu-id="87085-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87085-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="87085-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87085-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="87085-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87085-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="87085-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87085-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="87085-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-175">Search-Flags</span></span>           | <span data-ttu-id="87085-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87085-176">0x00000000</span></span>                      |
| <span data-ttu-id="87085-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-177">System-Flags</span></span>           | <span data-ttu-id="87085-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87085-178">0x00000010</span></span>                      |
| <span data-ttu-id="87085-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87085-179">Classes used in</span></span>        | [<span data-ttu-id="87085-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="87085-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="87085-181">亞當</span><span class="sxs-lookup"><span data-stu-id="87085-181">ADAM</span></span>



| <span data-ttu-id="87085-182">進入</span><span class="sxs-lookup"><span data-stu-id="87085-182">Entry</span></span> | <span data-ttu-id="87085-183">值</span><span class="sxs-lookup"><span data-stu-id="87085-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="87085-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87085-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="87085-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87085-185">MAPI-Id</span></span>                | <span data-ttu-id="87085-186">0x8155</span><span class="sxs-lookup"><span data-stu-id="87085-186">0x8155</span></span>                          |
| <span data-ttu-id="87085-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="87085-187">System-Only</span></span>            | <span data-ttu-id="87085-188">對</span><span class="sxs-lookup"><span data-stu-id="87085-188">True</span></span>                            |
| <span data-ttu-id="87085-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87085-189">Is-Single-Valued</span></span>       | <span data-ttu-id="87085-190">對</span><span class="sxs-lookup"><span data-stu-id="87085-190">True</span></span>                            |
| <span data-ttu-id="87085-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87085-191">Is Indexed</span></span>             | <span data-ttu-id="87085-192">否</span><span class="sxs-lookup"><span data-stu-id="87085-192">False</span></span>                           |
| <span data-ttu-id="87085-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87085-193">In Global Catalog</span></span>      | <span data-ttu-id="87085-194">否</span><span class="sxs-lookup"><span data-stu-id="87085-194">False</span></span>                           |
| <span data-ttu-id="87085-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87085-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="87085-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87085-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="87085-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87085-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="87085-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87085-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="87085-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-199">Search-Flags</span></span>           | <span data-ttu-id="87085-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87085-200">0x00000000</span></span>                      |
| <span data-ttu-id="87085-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-201">System-Flags</span></span>           | <span data-ttu-id="87085-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87085-202">0x00000010</span></span>                      |
| <span data-ttu-id="87085-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87085-203">Classes used in</span></span>        | [<span data-ttu-id="87085-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="87085-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="87085-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="87085-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="87085-206">進入</span><span class="sxs-lookup"><span data-stu-id="87085-206">Entry</span></span> | <span data-ttu-id="87085-207">值</span><span class="sxs-lookup"><span data-stu-id="87085-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="87085-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87085-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="87085-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87085-209">MAPI-Id</span></span>                | <span data-ttu-id="87085-210">0x8155</span><span class="sxs-lookup"><span data-stu-id="87085-210">0x8155</span></span>                          |
| <span data-ttu-id="87085-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="87085-211">System-Only</span></span>            | <span data-ttu-id="87085-212">對</span><span class="sxs-lookup"><span data-stu-id="87085-212">True</span></span>                            |
| <span data-ttu-id="87085-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87085-213">Is-Single-Valued</span></span>       | <span data-ttu-id="87085-214">對</span><span class="sxs-lookup"><span data-stu-id="87085-214">True</span></span>                            |
| <span data-ttu-id="87085-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87085-215">Is Indexed</span></span>             | <span data-ttu-id="87085-216">否</span><span class="sxs-lookup"><span data-stu-id="87085-216">False</span></span>                           |
| <span data-ttu-id="87085-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87085-217">In Global Catalog</span></span>      | <span data-ttu-id="87085-218">否</span><span class="sxs-lookup"><span data-stu-id="87085-218">False</span></span>                           |
| <span data-ttu-id="87085-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87085-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="87085-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87085-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="87085-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87085-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="87085-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87085-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="87085-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-223">Search-Flags</span></span>           | <span data-ttu-id="87085-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87085-224">0x00000000</span></span>                      |
| <span data-ttu-id="87085-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-225">System-Flags</span></span>           | <span data-ttu-id="87085-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87085-226">0x00000010</span></span>                      |
| <span data-ttu-id="87085-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87085-227">Classes used in</span></span>        | [<span data-ttu-id="87085-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="87085-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="87085-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87085-229">Windows Server 2008</span></span>



| <span data-ttu-id="87085-230">進入</span><span class="sxs-lookup"><span data-stu-id="87085-230">Entry</span></span> | <span data-ttu-id="87085-231">值</span><span class="sxs-lookup"><span data-stu-id="87085-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="87085-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87085-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="87085-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87085-233">MAPI-Id</span></span>                | <span data-ttu-id="87085-234">0x8155</span><span class="sxs-lookup"><span data-stu-id="87085-234">0x8155</span></span>                          |
| <span data-ttu-id="87085-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="87085-235">System-Only</span></span>            | <span data-ttu-id="87085-236">對</span><span class="sxs-lookup"><span data-stu-id="87085-236">True</span></span>                            |
| <span data-ttu-id="87085-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87085-237">Is-Single-Valued</span></span>       | <span data-ttu-id="87085-238">對</span><span class="sxs-lookup"><span data-stu-id="87085-238">True</span></span>                            |
| <span data-ttu-id="87085-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87085-239">Is Indexed</span></span>             | <span data-ttu-id="87085-240">否</span><span class="sxs-lookup"><span data-stu-id="87085-240">False</span></span>                           |
| <span data-ttu-id="87085-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87085-241">In Global Catalog</span></span>      | <span data-ttu-id="87085-242">否</span><span class="sxs-lookup"><span data-stu-id="87085-242">False</span></span>                           |
| <span data-ttu-id="87085-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87085-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="87085-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87085-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="87085-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87085-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="87085-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87085-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="87085-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-247">Search-Flags</span></span>           | <span data-ttu-id="87085-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87085-248">0x00000000</span></span>                      |
| <span data-ttu-id="87085-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-249">System-Flags</span></span>           | <span data-ttu-id="87085-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87085-250">0x00000010</span></span>                      |
| <span data-ttu-id="87085-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87085-251">Classes used in</span></span>        | [<span data-ttu-id="87085-252">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="87085-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="87085-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="87085-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="87085-254">進入</span><span class="sxs-lookup"><span data-stu-id="87085-254">Entry</span></span> | <span data-ttu-id="87085-255">值</span><span class="sxs-lookup"><span data-stu-id="87085-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="87085-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87085-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="87085-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87085-257">MAPI-Id</span></span>                | <span data-ttu-id="87085-258">0x8155</span><span class="sxs-lookup"><span data-stu-id="87085-258">0x8155</span></span>                          |
| <span data-ttu-id="87085-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="87085-259">System-Only</span></span>            | <span data-ttu-id="87085-260">對</span><span class="sxs-lookup"><span data-stu-id="87085-260">True</span></span>                            |
| <span data-ttu-id="87085-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87085-261">Is-Single-Valued</span></span>       | <span data-ttu-id="87085-262">對</span><span class="sxs-lookup"><span data-stu-id="87085-262">True</span></span>                            |
| <span data-ttu-id="87085-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87085-263">Is Indexed</span></span>             | <span data-ttu-id="87085-264">否</span><span class="sxs-lookup"><span data-stu-id="87085-264">False</span></span>                           |
| <span data-ttu-id="87085-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87085-265">In Global Catalog</span></span>      | <span data-ttu-id="87085-266">否</span><span class="sxs-lookup"><span data-stu-id="87085-266">False</span></span>                           |
| <span data-ttu-id="87085-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87085-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="87085-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87085-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="87085-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87085-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="87085-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87085-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="87085-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-271">Search-Flags</span></span>           | <span data-ttu-id="87085-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87085-272">0x00000000</span></span>                      |
| <span data-ttu-id="87085-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-273">System-Flags</span></span>           | <span data-ttu-id="87085-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87085-274">0x00000010</span></span>                      |
| <span data-ttu-id="87085-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87085-275">Classes used in</span></span>        | [<span data-ttu-id="87085-276">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="87085-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="87085-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87085-277">Windows Server 2012</span></span>



| <span data-ttu-id="87085-278">進入</span><span class="sxs-lookup"><span data-stu-id="87085-278">Entry</span></span> | <span data-ttu-id="87085-279">值</span><span class="sxs-lookup"><span data-stu-id="87085-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="87085-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87085-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="87085-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87085-281">MAPI-Id</span></span>                | <span data-ttu-id="87085-282">0x8155</span><span class="sxs-lookup"><span data-stu-id="87085-282">0x8155</span></span>                          |
| <span data-ttu-id="87085-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="87085-283">System-Only</span></span>            | <span data-ttu-id="87085-284">對</span><span class="sxs-lookup"><span data-stu-id="87085-284">True</span></span>                            |
| <span data-ttu-id="87085-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87085-285">Is-Single-Valued</span></span>       | <span data-ttu-id="87085-286">對</span><span class="sxs-lookup"><span data-stu-id="87085-286">True</span></span>                            |
| <span data-ttu-id="87085-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87085-287">Is Indexed</span></span>             | <span data-ttu-id="87085-288">否</span><span class="sxs-lookup"><span data-stu-id="87085-288">False</span></span>                           |
| <span data-ttu-id="87085-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87085-289">In Global Catalog</span></span>      | <span data-ttu-id="87085-290">否</span><span class="sxs-lookup"><span data-stu-id="87085-290">False</span></span>                           |
| <span data-ttu-id="87085-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87085-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="87085-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87085-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="87085-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87085-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="87085-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87085-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="87085-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-295">Search-Flags</span></span>           | <span data-ttu-id="87085-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87085-296">0x00000000</span></span>                      |
| <span data-ttu-id="87085-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87085-297">System-Flags</span></span>           | <span data-ttu-id="87085-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87085-298">0x00000010</span></span>                      |
| <span data-ttu-id="87085-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87085-299">Classes used in</span></span>        | [<span data-ttu-id="87085-300">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="87085-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="87085-301">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87085-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87085-302">**USN-最後-Obj-Rem**</span><span class="sxs-lookup"><span data-stu-id="87085-302">**USN-Last-Obj-Rem**</span></span>](a-usnlastobjrem.md)
</dt> </dl>

 

 





