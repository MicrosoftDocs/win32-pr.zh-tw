---
title: Reports 屬性
description: 包含直接向使用者報告的使用者清單。 列為 [報表] 的使用者，是將 [屬性管理員] 屬性設定為 [此使用者] 的使用者。 清單中的每個專案都是代表使用者之物件的連結參考。
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- 報表屬性 AD 架構
- directReports 屬性 AD 架構
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef5a555b7c1d48fdb337f2c876abf3f15ae8daa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106980303"
---
# <a name="reports-attribute"></a><span data-ttu-id="4136f-107">Reports 屬性</span><span class="sxs-lookup"><span data-stu-id="4136f-107">Reports attribute</span></span>

<span data-ttu-id="4136f-108">包含直接向使用者報告的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="4136f-108">Contains the list of users that directly report to the user.</span></span> <span data-ttu-id="4136f-109">列為 [報表] 的使用者，是將 [屬性管理員] 屬性設定為 [此使用者] 的使用者。</span><span class="sxs-lookup"><span data-stu-id="4136f-109">The users listed as reports are those that have the property manager property set to this user.</span></span> <span data-ttu-id="4136f-110">清單中的每個專案都是代表使用者之物件的連結參考。</span><span class="sxs-lookup"><span data-stu-id="4136f-110">Each item in the list is a linked reference to the object that represents the user.</span></span>



| <span data-ttu-id="4136f-111">進入</span><span class="sxs-lookup"><span data-stu-id="4136f-111">Entry</span></span> | <span data-ttu-id="4136f-112">值</span><span class="sxs-lookup"><span data-stu-id="4136f-112">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="4136f-113">CN</span><span class="sxs-lookup"><span data-stu-id="4136f-113">CN</span></span>                | <span data-ttu-id="4136f-114">報表</span><span class="sxs-lookup"><span data-stu-id="4136f-114">Reports</span></span>                                         |
| <span data-ttu-id="4136f-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4136f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4136f-116">directReports</span><span class="sxs-lookup"><span data-stu-id="4136f-116">directReports</span></span>                                   |
| <span data-ttu-id="4136f-117">大小</span><span class="sxs-lookup"><span data-stu-id="4136f-117">Size</span></span>              | \-                                              |
| <span data-ttu-id="4136f-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4136f-118">Update Privilege</span></span>  | <span data-ttu-id="4136f-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="4136f-119">This value is set by the system.</span></span>                |
| <span data-ttu-id="4136f-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4136f-120">Update Frequency</span></span>  | <span data-ttu-id="4136f-121">當使用者的直屬員工變更時。</span><span class="sxs-lookup"><span data-stu-id="4136f-121">Whenever the direct reports for a user changes.</span></span> |
| <span data-ttu-id="4136f-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4136f-122">Attribute-Id</span></span>      | <span data-ttu-id="4136f-123">1.2.840.113556.1.2.436</span><span class="sxs-lookup"><span data-stu-id="4136f-123">1.2.840.113556.1.2.436</span></span>                          |
| <span data-ttu-id="4136f-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4136f-124">System-Id-Guid</span></span>    | <span data-ttu-id="4136f-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4136f-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span></span>            |
| <span data-ttu-id="4136f-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="4136f-126">Syntax</span></span>            | [<span data-ttu-id="4136f-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4136f-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)         |



## <a name="implementations"></a><span data-ttu-id="4136f-128">實作</span><span class="sxs-lookup"><span data-stu-id="4136f-128">Implementations</span></span>

-   [<span data-ttu-id="4136f-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4136f-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4136f-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4136f-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4136f-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4136f-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4136f-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4136f-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4136f-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4136f-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4136f-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4136f-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4136f-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4136f-135">Windows 2000 Server</span></span>



| <span data-ttu-id="4136f-136">進入</span><span class="sxs-lookup"><span data-stu-id="4136f-136">Entry</span></span> | <span data-ttu-id="4136f-137">值</span><span class="sxs-lookup"><span data-stu-id="4136f-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4136f-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4136f-138">Link-Id</span></span>                | <span data-ttu-id="4136f-139">43</span><span class="sxs-lookup"><span data-stu-id="4136f-139">43</span></span>                              |
| <span data-ttu-id="4136f-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4136f-140">MAPI-Id</span></span>                | <span data-ttu-id="4136f-141">0x800E</span><span class="sxs-lookup"><span data-stu-id="4136f-141">0x800E</span></span>                          |
| <span data-ttu-id="4136f-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="4136f-142">System-Only</span></span>            | <span data-ttu-id="4136f-143">對</span><span class="sxs-lookup"><span data-stu-id="4136f-143">True</span></span>                            |
| <span data-ttu-id="4136f-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4136f-144">Is-Single-Valued</span></span>       | <span data-ttu-id="4136f-145">否</span><span class="sxs-lookup"><span data-stu-id="4136f-145">False</span></span>                           |
| <span data-ttu-id="4136f-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4136f-146">Is Indexed</span></span>             | <span data-ttu-id="4136f-147">否</span><span class="sxs-lookup"><span data-stu-id="4136f-147">False</span></span>                           |
| <span data-ttu-id="4136f-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4136f-148">In Global Catalog</span></span>      | <span data-ttu-id="4136f-149">否</span><span class="sxs-lookup"><span data-stu-id="4136f-149">False</span></span>                           |
| <span data-ttu-id="4136f-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4136f-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="4136f-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4136f-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4136f-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4136f-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4136f-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4136f-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4136f-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-154">Search-Flags</span></span>           | <span data-ttu-id="4136f-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4136f-155">0x00000000</span></span>                      |
| <span data-ttu-id="4136f-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-156">System-Flags</span></span>           | <span data-ttu-id="4136f-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4136f-157">0x00000010</span></span>                      |
| <span data-ttu-id="4136f-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4136f-158">Classes used in</span></span>        | [<span data-ttu-id="4136f-159">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4136f-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4136f-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4136f-160">Windows Server 2003</span></span>



| <span data-ttu-id="4136f-161">進入</span><span class="sxs-lookup"><span data-stu-id="4136f-161">Entry</span></span> | <span data-ttu-id="4136f-162">值</span><span class="sxs-lookup"><span data-stu-id="4136f-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4136f-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4136f-163">Link-Id</span></span>                | <span data-ttu-id="4136f-164">43</span><span class="sxs-lookup"><span data-stu-id="4136f-164">43</span></span>                              |
| <span data-ttu-id="4136f-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4136f-165">MAPI-Id</span></span>                | <span data-ttu-id="4136f-166">0x800E</span><span class="sxs-lookup"><span data-stu-id="4136f-166">0x800E</span></span>                          |
| <span data-ttu-id="4136f-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="4136f-167">System-Only</span></span>            | <span data-ttu-id="4136f-168">對</span><span class="sxs-lookup"><span data-stu-id="4136f-168">True</span></span>                            |
| <span data-ttu-id="4136f-169">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4136f-169">Is-Single-Valued</span></span>       | <span data-ttu-id="4136f-170">否</span><span class="sxs-lookup"><span data-stu-id="4136f-170">False</span></span>                           |
| <span data-ttu-id="4136f-171">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4136f-171">Is Indexed</span></span>             | <span data-ttu-id="4136f-172">否</span><span class="sxs-lookup"><span data-stu-id="4136f-172">False</span></span>                           |
| <span data-ttu-id="4136f-173">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4136f-173">In Global Catalog</span></span>      | <span data-ttu-id="4136f-174">否</span><span class="sxs-lookup"><span data-stu-id="4136f-174">False</span></span>                           |
| <span data-ttu-id="4136f-175">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4136f-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="4136f-176">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4136f-176">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4136f-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4136f-177">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4136f-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4136f-178">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4136f-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-179">Search-Flags</span></span>           | <span data-ttu-id="4136f-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4136f-180">0x00000000</span></span>                      |
| <span data-ttu-id="4136f-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-181">System-Flags</span></span>           | <span data-ttu-id="4136f-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4136f-182">0x00000010</span></span>                      |
| <span data-ttu-id="4136f-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4136f-183">Classes used in</span></span>        | [<span data-ttu-id="4136f-184">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4136f-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4136f-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4136f-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4136f-186">進入</span><span class="sxs-lookup"><span data-stu-id="4136f-186">Entry</span></span> | <span data-ttu-id="4136f-187">值</span><span class="sxs-lookup"><span data-stu-id="4136f-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4136f-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4136f-188">Link-Id</span></span>                | <span data-ttu-id="4136f-189">43</span><span class="sxs-lookup"><span data-stu-id="4136f-189">43</span></span>                              |
| <span data-ttu-id="4136f-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4136f-190">MAPI-Id</span></span>                | <span data-ttu-id="4136f-191">0x800E</span><span class="sxs-lookup"><span data-stu-id="4136f-191">0x800E</span></span>                          |
| <span data-ttu-id="4136f-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="4136f-192">System-Only</span></span>            | <span data-ttu-id="4136f-193">對</span><span class="sxs-lookup"><span data-stu-id="4136f-193">True</span></span>                            |
| <span data-ttu-id="4136f-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4136f-194">Is-Single-Valued</span></span>       | <span data-ttu-id="4136f-195">否</span><span class="sxs-lookup"><span data-stu-id="4136f-195">False</span></span>                           |
| <span data-ttu-id="4136f-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4136f-196">Is Indexed</span></span>             | <span data-ttu-id="4136f-197">否</span><span class="sxs-lookup"><span data-stu-id="4136f-197">False</span></span>                           |
| <span data-ttu-id="4136f-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4136f-198">In Global Catalog</span></span>      | <span data-ttu-id="4136f-199">否</span><span class="sxs-lookup"><span data-stu-id="4136f-199">False</span></span>                           |
| <span data-ttu-id="4136f-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4136f-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="4136f-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4136f-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4136f-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4136f-202">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4136f-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4136f-203">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4136f-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-204">Search-Flags</span></span>           | <span data-ttu-id="4136f-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4136f-205">0x00000000</span></span>                      |
| <span data-ttu-id="4136f-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-206">System-Flags</span></span>           | <span data-ttu-id="4136f-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4136f-207">0x00000010</span></span>                      |
| <span data-ttu-id="4136f-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4136f-208">Classes used in</span></span>        | [<span data-ttu-id="4136f-209">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4136f-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4136f-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4136f-210">Windows Server 2008</span></span>



| <span data-ttu-id="4136f-211">進入</span><span class="sxs-lookup"><span data-stu-id="4136f-211">Entry</span></span> | <span data-ttu-id="4136f-212">值</span><span class="sxs-lookup"><span data-stu-id="4136f-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4136f-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4136f-213">Link-Id</span></span>                | <span data-ttu-id="4136f-214">43</span><span class="sxs-lookup"><span data-stu-id="4136f-214">43</span></span>                              |
| <span data-ttu-id="4136f-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4136f-215">MAPI-Id</span></span>                | <span data-ttu-id="4136f-216">0x800E</span><span class="sxs-lookup"><span data-stu-id="4136f-216">0x800E</span></span>                          |
| <span data-ttu-id="4136f-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="4136f-217">System-Only</span></span>            | <span data-ttu-id="4136f-218">對</span><span class="sxs-lookup"><span data-stu-id="4136f-218">True</span></span>                            |
| <span data-ttu-id="4136f-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4136f-219">Is-Single-Valued</span></span>       | <span data-ttu-id="4136f-220">否</span><span class="sxs-lookup"><span data-stu-id="4136f-220">False</span></span>                           |
| <span data-ttu-id="4136f-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4136f-221">Is Indexed</span></span>             | <span data-ttu-id="4136f-222">否</span><span class="sxs-lookup"><span data-stu-id="4136f-222">False</span></span>                           |
| <span data-ttu-id="4136f-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4136f-223">In Global Catalog</span></span>      | <span data-ttu-id="4136f-224">否</span><span class="sxs-lookup"><span data-stu-id="4136f-224">False</span></span>                           |
| <span data-ttu-id="4136f-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4136f-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="4136f-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4136f-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4136f-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4136f-227">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4136f-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4136f-228">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4136f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-229">Search-Flags</span></span>           | <span data-ttu-id="4136f-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4136f-230">0x00000000</span></span>                      |
| <span data-ttu-id="4136f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-231">System-Flags</span></span>           | <span data-ttu-id="4136f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4136f-232">0x00000010</span></span>                      |
| <span data-ttu-id="4136f-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4136f-233">Classes used in</span></span>        | [<span data-ttu-id="4136f-234">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4136f-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4136f-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4136f-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4136f-236">進入</span><span class="sxs-lookup"><span data-stu-id="4136f-236">Entry</span></span> | <span data-ttu-id="4136f-237">值</span><span class="sxs-lookup"><span data-stu-id="4136f-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4136f-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4136f-238">Link-Id</span></span>                | <span data-ttu-id="4136f-239">43</span><span class="sxs-lookup"><span data-stu-id="4136f-239">43</span></span>                              |
| <span data-ttu-id="4136f-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4136f-240">MAPI-Id</span></span>                | <span data-ttu-id="4136f-241">0x800E</span><span class="sxs-lookup"><span data-stu-id="4136f-241">0x800E</span></span>                          |
| <span data-ttu-id="4136f-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="4136f-242">System-Only</span></span>            | <span data-ttu-id="4136f-243">對</span><span class="sxs-lookup"><span data-stu-id="4136f-243">True</span></span>                            |
| <span data-ttu-id="4136f-244">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4136f-244">Is-Single-Valued</span></span>       | <span data-ttu-id="4136f-245">否</span><span class="sxs-lookup"><span data-stu-id="4136f-245">False</span></span>                           |
| <span data-ttu-id="4136f-246">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4136f-246">Is Indexed</span></span>             | <span data-ttu-id="4136f-247">否</span><span class="sxs-lookup"><span data-stu-id="4136f-247">False</span></span>                           |
| <span data-ttu-id="4136f-248">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4136f-248">In Global Catalog</span></span>      | <span data-ttu-id="4136f-249">否</span><span class="sxs-lookup"><span data-stu-id="4136f-249">False</span></span>                           |
| <span data-ttu-id="4136f-250">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4136f-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="4136f-251">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4136f-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4136f-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4136f-252">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4136f-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4136f-253">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4136f-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-254">Search-Flags</span></span>           | <span data-ttu-id="4136f-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4136f-255">0x00000000</span></span>                      |
| <span data-ttu-id="4136f-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-256">System-Flags</span></span>           | <span data-ttu-id="4136f-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4136f-257">0x00000010</span></span>                      |
| <span data-ttu-id="4136f-258">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4136f-258">Classes used in</span></span>        | [<span data-ttu-id="4136f-259">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4136f-259">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4136f-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4136f-260">Windows Server 2012</span></span>



| <span data-ttu-id="4136f-261">進入</span><span class="sxs-lookup"><span data-stu-id="4136f-261">Entry</span></span> | <span data-ttu-id="4136f-262">值</span><span class="sxs-lookup"><span data-stu-id="4136f-262">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4136f-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4136f-263">Link-Id</span></span>                | <span data-ttu-id="4136f-264">43</span><span class="sxs-lookup"><span data-stu-id="4136f-264">43</span></span>                              |
| <span data-ttu-id="4136f-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4136f-265">MAPI-Id</span></span>                | <span data-ttu-id="4136f-266">0x800E</span><span class="sxs-lookup"><span data-stu-id="4136f-266">0x800E</span></span>                          |
| <span data-ttu-id="4136f-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="4136f-267">System-Only</span></span>            | <span data-ttu-id="4136f-268">對</span><span class="sxs-lookup"><span data-stu-id="4136f-268">True</span></span>                            |
| <span data-ttu-id="4136f-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4136f-269">Is-Single-Valued</span></span>       | <span data-ttu-id="4136f-270">否</span><span class="sxs-lookup"><span data-stu-id="4136f-270">False</span></span>                           |
| <span data-ttu-id="4136f-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4136f-271">Is Indexed</span></span>             | <span data-ttu-id="4136f-272">否</span><span class="sxs-lookup"><span data-stu-id="4136f-272">False</span></span>                           |
| <span data-ttu-id="4136f-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4136f-273">In Global Catalog</span></span>      | <span data-ttu-id="4136f-274">否</span><span class="sxs-lookup"><span data-stu-id="4136f-274">False</span></span>                           |
| <span data-ttu-id="4136f-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4136f-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="4136f-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4136f-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4136f-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4136f-277">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="4136f-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4136f-278">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="4136f-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-279">Search-Flags</span></span>           | <span data-ttu-id="4136f-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4136f-280">0x00000000</span></span>                      |
| <span data-ttu-id="4136f-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4136f-281">System-Flags</span></span>           | <span data-ttu-id="4136f-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4136f-282">0x00000010</span></span>                      |
| <span data-ttu-id="4136f-283">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4136f-283">Classes used in</span></span>        | [<span data-ttu-id="4136f-284">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="4136f-284">**Top**</span></span>](c-top.md)<br/> |



 

 





