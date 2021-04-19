---
title: 最後一個已知的父屬性
description: 孤立物件的最後一個已知父系 (DN) 的分辨名稱。
ms.assetid: 6cf7be1a-8ff0-42f7-9e7a-c15cbc652ec5
ms.tgt_platform: multiple
keywords:
- 最後一個已知的父屬性 AD 架構
- lastKnownParent 屬性 AD 架構
topic_type:
- apiref
api_name:
- Last-Known-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d83ae15f910d2e2f2dbc23ff39bb28cd27d56b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106980920"
---
# <a name="last-known-parent-attribute"></a><span data-ttu-id="76067-105">最後一個已知的父屬性</span><span class="sxs-lookup"><span data-stu-id="76067-105">Last-Known-Parent attribute</span></span>

<span data-ttu-id="76067-106">孤立物件的最後一個已知父系 (DN) 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="76067-106">The Distinguished Name (DN) of the last known parent of an orphaned object.</span></span>



| <span data-ttu-id="76067-107">進入</span><span class="sxs-lookup"><span data-stu-id="76067-107">Entry</span></span> | <span data-ttu-id="76067-108">值</span><span class="sxs-lookup"><span data-stu-id="76067-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="76067-109">CN</span><span class="sxs-lookup"><span data-stu-id="76067-109">CN</span></span>                | <span data-ttu-id="76067-110">最後一個已知-父系</span><span class="sxs-lookup"><span data-stu-id="76067-110">Last-Known-Parent</span></span>                       |
| <span data-ttu-id="76067-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="76067-111">Ldap-Display-Name</span></span> | <span data-ttu-id="76067-112">lastKnownParent</span><span class="sxs-lookup"><span data-stu-id="76067-112">lastKnownParent</span></span>                         |
| <span data-ttu-id="76067-113">大小</span><span class="sxs-lookup"><span data-stu-id="76067-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="76067-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="76067-114">Update Privilege</span></span>  | <span data-ttu-id="76067-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="76067-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="76067-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="76067-116">Update Frequency</span></span>  | <span data-ttu-id="76067-117">每次物件孤立時。</span><span class="sxs-lookup"><span data-stu-id="76067-117">Whenever an object is orphaned.</span></span>         |
| <span data-ttu-id="76067-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76067-118">Attribute-Id</span></span>      | <span data-ttu-id="76067-119">1.2.840.113556.1.4.781</span><span class="sxs-lookup"><span data-stu-id="76067-119">1.2.840.113556.1.4.781</span></span>                  |
| <span data-ttu-id="76067-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="76067-120">System-Id-Guid</span></span>    | <span data-ttu-id="76067-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="76067-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="76067-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="76067-122">Syntax</span></span>            | [<span data-ttu-id="76067-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="76067-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="76067-124">實作</span><span class="sxs-lookup"><span data-stu-id="76067-124">Implementations</span></span>

-   [<span data-ttu-id="76067-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="76067-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="76067-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="76067-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="76067-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="76067-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="76067-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="76067-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="76067-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="76067-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="76067-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="76067-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="76067-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="76067-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="76067-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="76067-132">Windows 2000 Server</span></span>



| <span data-ttu-id="76067-133">進入</span><span class="sxs-lookup"><span data-stu-id="76067-133">Entry</span></span> | <span data-ttu-id="76067-134">值</span><span class="sxs-lookup"><span data-stu-id="76067-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76067-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76067-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76067-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="76067-137">System-Only</span></span>            | <span data-ttu-id="76067-138">否</span><span class="sxs-lookup"><span data-stu-id="76067-138">False</span></span>                           |
| <span data-ttu-id="76067-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76067-139">Is-Single-Valued</span></span>       | <span data-ttu-id="76067-140">對</span><span class="sxs-lookup"><span data-stu-id="76067-140">True</span></span>                            |
| <span data-ttu-id="76067-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76067-141">Is Indexed</span></span>             | <span data-ttu-id="76067-142">否</span><span class="sxs-lookup"><span data-stu-id="76067-142">False</span></span>                           |
| <span data-ttu-id="76067-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76067-143">In Global Catalog</span></span>      | <span data-ttu-id="76067-144">否</span><span class="sxs-lookup"><span data-stu-id="76067-144">False</span></span>                           |
| <span data-ttu-id="76067-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76067-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="76067-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76067-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76067-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76067-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76067-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76067-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76067-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-149">Search-Flags</span></span>           | <span data-ttu-id="76067-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76067-150">0x00000000</span></span>                      |
| <span data-ttu-id="76067-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-151">System-Flags</span></span>           | <span data-ttu-id="76067-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76067-152">0x00000010</span></span>                      |
| <span data-ttu-id="76067-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76067-153">Classes used in</span></span>        | [<span data-ttu-id="76067-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76067-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="76067-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76067-155">Windows Server 2003</span></span>



| <span data-ttu-id="76067-156">進入</span><span class="sxs-lookup"><span data-stu-id="76067-156">Entry</span></span> | <span data-ttu-id="76067-157">值</span><span class="sxs-lookup"><span data-stu-id="76067-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76067-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76067-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76067-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="76067-160">System-Only</span></span>            | <span data-ttu-id="76067-161">否</span><span class="sxs-lookup"><span data-stu-id="76067-161">False</span></span>                           |
| <span data-ttu-id="76067-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76067-162">Is-Single-Valued</span></span>       | <span data-ttu-id="76067-163">對</span><span class="sxs-lookup"><span data-stu-id="76067-163">True</span></span>                            |
| <span data-ttu-id="76067-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76067-164">Is Indexed</span></span>             | <span data-ttu-id="76067-165">否</span><span class="sxs-lookup"><span data-stu-id="76067-165">False</span></span>                           |
| <span data-ttu-id="76067-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76067-166">In Global Catalog</span></span>      | <span data-ttu-id="76067-167">否</span><span class="sxs-lookup"><span data-stu-id="76067-167">False</span></span>                           |
| <span data-ttu-id="76067-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76067-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="76067-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76067-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76067-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76067-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76067-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76067-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76067-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-172">Search-Flags</span></span>           | <span data-ttu-id="76067-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76067-173">0x00000000</span></span>                      |
| <span data-ttu-id="76067-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-174">System-Flags</span></span>           | <span data-ttu-id="76067-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76067-175">0x00000010</span></span>                      |
| <span data-ttu-id="76067-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76067-176">Classes used in</span></span>        | [<span data-ttu-id="76067-177">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76067-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="76067-178">亞當</span><span class="sxs-lookup"><span data-stu-id="76067-178">ADAM</span></span>



| <span data-ttu-id="76067-179">進入</span><span class="sxs-lookup"><span data-stu-id="76067-179">Entry</span></span> | <span data-ttu-id="76067-180">值</span><span class="sxs-lookup"><span data-stu-id="76067-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76067-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76067-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76067-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="76067-183">System-Only</span></span>            | <span data-ttu-id="76067-184">否</span><span class="sxs-lookup"><span data-stu-id="76067-184">False</span></span>                           |
| <span data-ttu-id="76067-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76067-185">Is-Single-Valued</span></span>       | <span data-ttu-id="76067-186">對</span><span class="sxs-lookup"><span data-stu-id="76067-186">True</span></span>                            |
| <span data-ttu-id="76067-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76067-187">Is Indexed</span></span>             | <span data-ttu-id="76067-188">否</span><span class="sxs-lookup"><span data-stu-id="76067-188">False</span></span>                           |
| <span data-ttu-id="76067-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76067-189">In Global Catalog</span></span>      | <span data-ttu-id="76067-190">否</span><span class="sxs-lookup"><span data-stu-id="76067-190">False</span></span>                           |
| <span data-ttu-id="76067-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76067-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="76067-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76067-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76067-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76067-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76067-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76067-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76067-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-195">Search-Flags</span></span>           | <span data-ttu-id="76067-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76067-196">0x00000000</span></span>                      |
| <span data-ttu-id="76067-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-197">System-Flags</span></span>           | <span data-ttu-id="76067-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76067-198">0x00000010</span></span>                      |
| <span data-ttu-id="76067-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76067-199">Classes used in</span></span>        | [<span data-ttu-id="76067-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76067-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="76067-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="76067-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="76067-202">進入</span><span class="sxs-lookup"><span data-stu-id="76067-202">Entry</span></span> | <span data-ttu-id="76067-203">值</span><span class="sxs-lookup"><span data-stu-id="76067-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76067-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76067-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76067-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="76067-206">System-Only</span></span>            | <span data-ttu-id="76067-207">否</span><span class="sxs-lookup"><span data-stu-id="76067-207">False</span></span>                           |
| <span data-ttu-id="76067-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76067-208">Is-Single-Valued</span></span>       | <span data-ttu-id="76067-209">對</span><span class="sxs-lookup"><span data-stu-id="76067-209">True</span></span>                            |
| <span data-ttu-id="76067-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76067-210">Is Indexed</span></span>             | <span data-ttu-id="76067-211">否</span><span class="sxs-lookup"><span data-stu-id="76067-211">False</span></span>                           |
| <span data-ttu-id="76067-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76067-212">In Global Catalog</span></span>      | <span data-ttu-id="76067-213">否</span><span class="sxs-lookup"><span data-stu-id="76067-213">False</span></span>                           |
| <span data-ttu-id="76067-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76067-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="76067-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76067-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76067-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76067-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76067-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76067-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76067-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-218">Search-Flags</span></span>           | <span data-ttu-id="76067-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76067-219">0x00000000</span></span>                      |
| <span data-ttu-id="76067-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-220">System-Flags</span></span>           | <span data-ttu-id="76067-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76067-221">0x00000010</span></span>                      |
| <span data-ttu-id="76067-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76067-222">Classes used in</span></span>        | [<span data-ttu-id="76067-223">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76067-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="76067-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76067-224">Windows Server 2008</span></span>



| <span data-ttu-id="76067-225">進入</span><span class="sxs-lookup"><span data-stu-id="76067-225">Entry</span></span> | <span data-ttu-id="76067-226">值</span><span class="sxs-lookup"><span data-stu-id="76067-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76067-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76067-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76067-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="76067-229">System-Only</span></span>            | <span data-ttu-id="76067-230">否</span><span class="sxs-lookup"><span data-stu-id="76067-230">False</span></span>                           |
| <span data-ttu-id="76067-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76067-231">Is-Single-Valued</span></span>       | <span data-ttu-id="76067-232">對</span><span class="sxs-lookup"><span data-stu-id="76067-232">True</span></span>                            |
| <span data-ttu-id="76067-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76067-233">Is Indexed</span></span>             | <span data-ttu-id="76067-234">否</span><span class="sxs-lookup"><span data-stu-id="76067-234">False</span></span>                           |
| <span data-ttu-id="76067-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76067-235">In Global Catalog</span></span>      | <span data-ttu-id="76067-236">否</span><span class="sxs-lookup"><span data-stu-id="76067-236">False</span></span>                           |
| <span data-ttu-id="76067-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76067-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="76067-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76067-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76067-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76067-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76067-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76067-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76067-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-241">Search-Flags</span></span>           | <span data-ttu-id="76067-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76067-242">0x00000000</span></span>                      |
| <span data-ttu-id="76067-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-243">System-Flags</span></span>           | <span data-ttu-id="76067-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76067-244">0x00000010</span></span>                      |
| <span data-ttu-id="76067-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76067-245">Classes used in</span></span>        | [<span data-ttu-id="76067-246">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76067-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="76067-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76067-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="76067-248">進入</span><span class="sxs-lookup"><span data-stu-id="76067-248">Entry</span></span> | <span data-ttu-id="76067-249">值</span><span class="sxs-lookup"><span data-stu-id="76067-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76067-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76067-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76067-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="76067-252">System-Only</span></span>            | <span data-ttu-id="76067-253">否</span><span class="sxs-lookup"><span data-stu-id="76067-253">False</span></span>                           |
| <span data-ttu-id="76067-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76067-254">Is-Single-Valued</span></span>       | <span data-ttu-id="76067-255">對</span><span class="sxs-lookup"><span data-stu-id="76067-255">True</span></span>                            |
| <span data-ttu-id="76067-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76067-256">Is Indexed</span></span>             | <span data-ttu-id="76067-257">否</span><span class="sxs-lookup"><span data-stu-id="76067-257">False</span></span>                           |
| <span data-ttu-id="76067-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76067-258">In Global Catalog</span></span>      | <span data-ttu-id="76067-259">否</span><span class="sxs-lookup"><span data-stu-id="76067-259">False</span></span>                           |
| <span data-ttu-id="76067-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76067-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="76067-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76067-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76067-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76067-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76067-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76067-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76067-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-264">Search-Flags</span></span>           | <span data-ttu-id="76067-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76067-265">0x00000000</span></span>                      |
| <span data-ttu-id="76067-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-266">System-Flags</span></span>           | <span data-ttu-id="76067-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76067-267">0x00000010</span></span>                      |
| <span data-ttu-id="76067-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76067-268">Classes used in</span></span>        | [<span data-ttu-id="76067-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76067-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="76067-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76067-270">Windows Server 2012</span></span>



| <span data-ttu-id="76067-271">進入</span><span class="sxs-lookup"><span data-stu-id="76067-271">Entry</span></span> | <span data-ttu-id="76067-272">值</span><span class="sxs-lookup"><span data-stu-id="76067-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76067-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="76067-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76067-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76067-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="76067-275">System-Only</span></span>            | <span data-ttu-id="76067-276">否</span><span class="sxs-lookup"><span data-stu-id="76067-276">False</span></span>                           |
| <span data-ttu-id="76067-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="76067-277">Is-Single-Valued</span></span>       | <span data-ttu-id="76067-278">對</span><span class="sxs-lookup"><span data-stu-id="76067-278">True</span></span>                            |
| <span data-ttu-id="76067-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="76067-279">Is Indexed</span></span>             | <span data-ttu-id="76067-280">否</span><span class="sxs-lookup"><span data-stu-id="76067-280">False</span></span>                           |
| <span data-ttu-id="76067-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="76067-281">In Global Catalog</span></span>      | <span data-ttu-id="76067-282">否</span><span class="sxs-lookup"><span data-stu-id="76067-282">False</span></span>                           |
| <span data-ttu-id="76067-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="76067-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="76067-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="76067-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76067-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76067-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76067-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76067-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76067-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-287">Search-Flags</span></span>           | <span data-ttu-id="76067-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76067-288">0x00000000</span></span>                      |
| <span data-ttu-id="76067-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76067-289">System-Flags</span></span>           | <span data-ttu-id="76067-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76067-290">0x00000010</span></span>                      |
| <span data-ttu-id="76067-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="76067-291">Classes used in</span></span>        | [<span data-ttu-id="76067-292">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="76067-292">**Top**</span></span>](c-top.md)<br/> |



 

 





