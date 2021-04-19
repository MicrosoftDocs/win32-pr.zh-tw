---
title: Search-Flags 屬性
description: 包含一組旗標，可指定屬性的搜尋和索引資訊。
ms.assetid: 55fc4398-25d2-466a-9aa9-fa375d827023
ms.tgt_platform: multiple
keywords:
- Search-Flags 屬性 AD 架構
- searchFlags 屬性 AD 架構
topic_type:
- apiref
api_name:
- Search-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f615464aa0aed69dd9590f668e37ec8c789c88
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991572"
---
# <a name="search-flags-attribute"></a><span data-ttu-id="6025a-105">Search-Flags 屬性</span><span class="sxs-lookup"><span data-stu-id="6025a-105">Search-Flags attribute</span></span>

<span data-ttu-id="6025a-106">包含一組旗標，可指定屬性的搜尋和索引資訊。</span><span class="sxs-lookup"><span data-stu-id="6025a-106">Contains a set of flags that specify search and indexing information for an attribute.</span></span> <span data-ttu-id="6025a-107">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="6025a-107">See Remarks.</span></span>



| <span data-ttu-id="6025a-108">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-108">Entry</span></span> | <span data-ttu-id="6025a-109">值</span><span class="sxs-lookup"><span data-stu-id="6025a-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6025a-110">CN</span><span class="sxs-lookup"><span data-stu-id="6025a-110">CN</span></span>                | <span data-ttu-id="6025a-111">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-111">Search-Flags</span></span>                         |
| <span data-ttu-id="6025a-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6025a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="6025a-113">searchFlags</span><span class="sxs-lookup"><span data-stu-id="6025a-113">searchFlags</span></span>                          |
| <span data-ttu-id="6025a-114">大小</span><span class="sxs-lookup"><span data-stu-id="6025a-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="6025a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6025a-115">Update Privilege</span></span>  | <span data-ttu-id="6025a-116">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="6025a-116">Schema administrator</span></span>                 |
| <span data-ttu-id="6025a-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6025a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6025a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-118">Attribute-Id</span></span>      | <span data-ttu-id="6025a-119">1.2.840.113556.1.2.334</span><span class="sxs-lookup"><span data-stu-id="6025a-119">1.2.840.113556.1.2.334</span></span>               |
| <span data-ttu-id="6025a-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6025a-120">System-Id-Guid</span></span>    | <span data-ttu-id="6025a-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6025a-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6025a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6025a-122">Syntax</span></span>            | [<span data-ttu-id="6025a-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="6025a-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6025a-124">實作</span><span class="sxs-lookup"><span data-stu-id="6025a-124">Implementations</span></span>

-   [<span data-ttu-id="6025a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6025a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6025a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6025a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6025a-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6025a-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6025a-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6025a-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6025a-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6025a-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6025a-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6025a-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6025a-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6025a-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6025a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6025a-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6025a-133">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-133">Entry</span></span> | <span data-ttu-id="6025a-134">值</span><span class="sxs-lookup"><span data-stu-id="6025a-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6025a-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6025a-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6025a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-136">MAPI-Id</span></span>                | <span data-ttu-id="6025a-137">0x812D</span><span class="sxs-lookup"><span data-stu-id="6025a-137">0x812D</span></span>                                                   |
| <span data-ttu-id="6025a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6025a-138">System-Only</span></span>            | <span data-ttu-id="6025a-139">否</span><span class="sxs-lookup"><span data-stu-id="6025a-139">False</span></span>                                                    |
| <span data-ttu-id="6025a-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6025a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6025a-141">對</span><span class="sxs-lookup"><span data-stu-id="6025a-141">True</span></span>                                                     |
| <span data-ttu-id="6025a-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6025a-142">Is Indexed</span></span>             | <span data-ttu-id="6025a-143">否</span><span class="sxs-lookup"><span data-stu-id="6025a-143">False</span></span>                                                    |
| <span data-ttu-id="6025a-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6025a-144">In Global Catalog</span></span>      | <span data-ttu-id="6025a-145">否</span><span class="sxs-lookup"><span data-stu-id="6025a-145">False</span></span>                                                    |
| <span data-ttu-id="6025a-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6025a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6025a-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6025a-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6025a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6025a-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6025a-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-150">Search-Flags</span></span>           | <span data-ttu-id="6025a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6025a-151">0x00000000</span></span>                                               |
| <span data-ttu-id="6025a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-152">System-Flags</span></span>           | <span data-ttu-id="6025a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6025a-153">0x00000010</span></span>                                               |
| <span data-ttu-id="6025a-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6025a-154">Classes used in</span></span>        | [<span data-ttu-id="6025a-155">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6025a-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6025a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6025a-156">Windows Server 2003</span></span>



| <span data-ttu-id="6025a-157">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-157">Entry</span></span> | <span data-ttu-id="6025a-158">值</span><span class="sxs-lookup"><span data-stu-id="6025a-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6025a-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6025a-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6025a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-160">MAPI-Id</span></span>                | <span data-ttu-id="6025a-161">0x812D</span><span class="sxs-lookup"><span data-stu-id="6025a-161">0x812D</span></span>                                                   |
| <span data-ttu-id="6025a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6025a-162">System-Only</span></span>            | <span data-ttu-id="6025a-163">否</span><span class="sxs-lookup"><span data-stu-id="6025a-163">False</span></span>                                                    |
| <span data-ttu-id="6025a-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6025a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6025a-165">對</span><span class="sxs-lookup"><span data-stu-id="6025a-165">True</span></span>                                                     |
| <span data-ttu-id="6025a-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6025a-166">Is Indexed</span></span>             | <span data-ttu-id="6025a-167">否</span><span class="sxs-lookup"><span data-stu-id="6025a-167">False</span></span>                                                    |
| <span data-ttu-id="6025a-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6025a-168">In Global Catalog</span></span>      | <span data-ttu-id="6025a-169">否</span><span class="sxs-lookup"><span data-stu-id="6025a-169">False</span></span>                                                    |
| <span data-ttu-id="6025a-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6025a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6025a-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6025a-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6025a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6025a-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6025a-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-174">Search-Flags</span></span>           | <span data-ttu-id="6025a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6025a-175">0x00000000</span></span>                                               |
| <span data-ttu-id="6025a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-176">System-Flags</span></span>           | <span data-ttu-id="6025a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6025a-177">0x00000010</span></span>                                               |
| <span data-ttu-id="6025a-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6025a-178">Classes used in</span></span>        | [<span data-ttu-id="6025a-179">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6025a-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6025a-180">亞當</span><span class="sxs-lookup"><span data-stu-id="6025a-180">ADAM</span></span>



| <span data-ttu-id="6025a-181">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-181">Entry</span></span> | <span data-ttu-id="6025a-182">值</span><span class="sxs-lookup"><span data-stu-id="6025a-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6025a-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6025a-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6025a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-184">MAPI-Id</span></span>                | <span data-ttu-id="6025a-185">0x812D</span><span class="sxs-lookup"><span data-stu-id="6025a-185">0x812D</span></span>                                                   |
| <span data-ttu-id="6025a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6025a-186">System-Only</span></span>            | <span data-ttu-id="6025a-187">否</span><span class="sxs-lookup"><span data-stu-id="6025a-187">False</span></span>                                                    |
| <span data-ttu-id="6025a-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6025a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6025a-189">對</span><span class="sxs-lookup"><span data-stu-id="6025a-189">True</span></span>                                                     |
| <span data-ttu-id="6025a-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6025a-190">Is Indexed</span></span>             | <span data-ttu-id="6025a-191">否</span><span class="sxs-lookup"><span data-stu-id="6025a-191">False</span></span>                                                    |
| <span data-ttu-id="6025a-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6025a-192">In Global Catalog</span></span>      | <span data-ttu-id="6025a-193">否</span><span class="sxs-lookup"><span data-stu-id="6025a-193">False</span></span>                                                    |
| <span data-ttu-id="6025a-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6025a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6025a-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6025a-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6025a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6025a-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6025a-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-198">Search-Flags</span></span>           | <span data-ttu-id="6025a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6025a-199">0x00000000</span></span>                                               |
| <span data-ttu-id="6025a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-200">System-Flags</span></span>           | <span data-ttu-id="6025a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6025a-201">0x00000010</span></span>                                               |
| <span data-ttu-id="6025a-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6025a-202">Classes used in</span></span>        | [<span data-ttu-id="6025a-203">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6025a-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6025a-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6025a-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6025a-205">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-205">Entry</span></span> | <span data-ttu-id="6025a-206">值</span><span class="sxs-lookup"><span data-stu-id="6025a-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6025a-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6025a-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6025a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-208">MAPI-Id</span></span>                | <span data-ttu-id="6025a-209">0x812D</span><span class="sxs-lookup"><span data-stu-id="6025a-209">0x812D</span></span>                                                   |
| <span data-ttu-id="6025a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="6025a-210">System-Only</span></span>            | <span data-ttu-id="6025a-211">否</span><span class="sxs-lookup"><span data-stu-id="6025a-211">False</span></span>                                                    |
| <span data-ttu-id="6025a-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6025a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="6025a-213">對</span><span class="sxs-lookup"><span data-stu-id="6025a-213">True</span></span>                                                     |
| <span data-ttu-id="6025a-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6025a-214">Is Indexed</span></span>             | <span data-ttu-id="6025a-215">否</span><span class="sxs-lookup"><span data-stu-id="6025a-215">False</span></span>                                                    |
| <span data-ttu-id="6025a-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6025a-216">In Global Catalog</span></span>      | <span data-ttu-id="6025a-217">否</span><span class="sxs-lookup"><span data-stu-id="6025a-217">False</span></span>                                                    |
| <span data-ttu-id="6025a-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6025a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="6025a-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6025a-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6025a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6025a-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6025a-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-222">Search-Flags</span></span>           | <span data-ttu-id="6025a-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6025a-223">0x00000000</span></span>                                               |
| <span data-ttu-id="6025a-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-224">System-Flags</span></span>           | <span data-ttu-id="6025a-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6025a-225">0x00000010</span></span>                                               |
| <span data-ttu-id="6025a-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6025a-226">Classes used in</span></span>        | [<span data-ttu-id="6025a-227">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6025a-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6025a-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6025a-228">Windows Server 2008</span></span>



| <span data-ttu-id="6025a-229">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-229">Entry</span></span> | <span data-ttu-id="6025a-230">值</span><span class="sxs-lookup"><span data-stu-id="6025a-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6025a-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6025a-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6025a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-232">MAPI-Id</span></span>                | <span data-ttu-id="6025a-233">0x812D</span><span class="sxs-lookup"><span data-stu-id="6025a-233">0x812D</span></span>                                                   |
| <span data-ttu-id="6025a-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="6025a-234">System-Only</span></span>            | <span data-ttu-id="6025a-235">否</span><span class="sxs-lookup"><span data-stu-id="6025a-235">False</span></span>                                                    |
| <span data-ttu-id="6025a-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6025a-236">Is-Single-Valued</span></span>       | <span data-ttu-id="6025a-237">對</span><span class="sxs-lookup"><span data-stu-id="6025a-237">True</span></span>                                                     |
| <span data-ttu-id="6025a-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6025a-238">Is Indexed</span></span>             | <span data-ttu-id="6025a-239">否</span><span class="sxs-lookup"><span data-stu-id="6025a-239">False</span></span>                                                    |
| <span data-ttu-id="6025a-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6025a-240">In Global Catalog</span></span>      | <span data-ttu-id="6025a-241">否</span><span class="sxs-lookup"><span data-stu-id="6025a-241">False</span></span>                                                    |
| <span data-ttu-id="6025a-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6025a-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="6025a-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6025a-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6025a-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6025a-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6025a-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-246">Search-Flags</span></span>           | <span data-ttu-id="6025a-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6025a-247">0x00000000</span></span>                                               |
| <span data-ttu-id="6025a-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-248">System-Flags</span></span>           | <span data-ttu-id="6025a-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6025a-249">0x00000010</span></span>                                               |
| <span data-ttu-id="6025a-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6025a-250">Classes used in</span></span>        | [<span data-ttu-id="6025a-251">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6025a-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6025a-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6025a-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6025a-253">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-253">Entry</span></span> | <span data-ttu-id="6025a-254">值</span><span class="sxs-lookup"><span data-stu-id="6025a-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6025a-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6025a-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6025a-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-256">MAPI-Id</span></span>                | <span data-ttu-id="6025a-257">0x812D</span><span class="sxs-lookup"><span data-stu-id="6025a-257">0x812D</span></span>                                                   |
| <span data-ttu-id="6025a-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="6025a-258">System-Only</span></span>            | <span data-ttu-id="6025a-259">否</span><span class="sxs-lookup"><span data-stu-id="6025a-259">False</span></span>                                                    |
| <span data-ttu-id="6025a-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6025a-260">Is-Single-Valued</span></span>       | <span data-ttu-id="6025a-261">對</span><span class="sxs-lookup"><span data-stu-id="6025a-261">True</span></span>                                                     |
| <span data-ttu-id="6025a-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6025a-262">Is Indexed</span></span>             | <span data-ttu-id="6025a-263">否</span><span class="sxs-lookup"><span data-stu-id="6025a-263">False</span></span>                                                    |
| <span data-ttu-id="6025a-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6025a-264">In Global Catalog</span></span>      | <span data-ttu-id="6025a-265">否</span><span class="sxs-lookup"><span data-stu-id="6025a-265">False</span></span>                                                    |
| <span data-ttu-id="6025a-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6025a-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="6025a-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6025a-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6025a-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6025a-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6025a-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-270">Search-Flags</span></span>           | <span data-ttu-id="6025a-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6025a-271">0x00000000</span></span>                                               |
| <span data-ttu-id="6025a-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-272">System-Flags</span></span>           | <span data-ttu-id="6025a-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6025a-273">0x00000010</span></span>                                               |
| <span data-ttu-id="6025a-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6025a-274">Classes used in</span></span>        | [<span data-ttu-id="6025a-275">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6025a-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6025a-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6025a-276">Windows Server 2012</span></span>



| <span data-ttu-id="6025a-277">進入</span><span class="sxs-lookup"><span data-stu-id="6025a-277">Entry</span></span> | <span data-ttu-id="6025a-278">值</span><span class="sxs-lookup"><span data-stu-id="6025a-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6025a-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6025a-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6025a-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6025a-280">MAPI-Id</span></span>                | <span data-ttu-id="6025a-281">0x812D</span><span class="sxs-lookup"><span data-stu-id="6025a-281">0x812D</span></span>                                                   |
| <span data-ttu-id="6025a-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="6025a-282">System-Only</span></span>            | <span data-ttu-id="6025a-283">否</span><span class="sxs-lookup"><span data-stu-id="6025a-283">False</span></span>                                                    |
| <span data-ttu-id="6025a-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6025a-284">Is-Single-Valued</span></span>       | <span data-ttu-id="6025a-285">對</span><span class="sxs-lookup"><span data-stu-id="6025a-285">True</span></span>                                                     |
| <span data-ttu-id="6025a-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6025a-286">Is Indexed</span></span>             | <span data-ttu-id="6025a-287">否</span><span class="sxs-lookup"><span data-stu-id="6025a-287">False</span></span>                                                    |
| <span data-ttu-id="6025a-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6025a-288">In Global Catalog</span></span>      | <span data-ttu-id="6025a-289">否</span><span class="sxs-lookup"><span data-stu-id="6025a-289">False</span></span>                                                    |
| <span data-ttu-id="6025a-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6025a-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="6025a-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6025a-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6025a-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6025a-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6025a-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6025a-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-294">Search-Flags</span></span>           | <span data-ttu-id="6025a-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6025a-295">0x00000000</span></span>                                               |
| <span data-ttu-id="6025a-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6025a-296">System-Flags</span></span>           | <span data-ttu-id="6025a-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6025a-297">0x00000010</span></span>                                               |
| <span data-ttu-id="6025a-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6025a-298">Classes used in</span></span>        | [<span data-ttu-id="6025a-299">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6025a-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6025a-300">備註</span><span class="sxs-lookup"><span data-stu-id="6025a-300">Remarks</span></span>

<span data-ttu-id="6025a-301">這個屬性可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="6025a-301">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="6025a-302">值</span><span class="sxs-lookup"><span data-stu-id="6025a-302">Value</span></span>            | <span data-ttu-id="6025a-303">描述</span><span class="sxs-lookup"><span data-stu-id="6025a-303">Description</span></span>                                                                                                                                                                                                                                                                                                                                                               |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6025a-304">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="6025a-304">1 (0x00000001)</span></span>   | <span data-ttu-id="6025a-305">建立屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="6025a-305">Create an index for the attribute.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6025a-306">2 (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="6025a-306">2 (0x00000002)</span></span>   | <span data-ttu-id="6025a-307">在每個容器中建立屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="6025a-307">Create an index for the attribute in each container.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6025a-308">4 (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="6025a-308">4 (0x00000004)</span></span>   | <span data-ttu-id="6025a-309">將此屬性新增至 (ANR) 設定的明確名稱解析。</span><span class="sxs-lookup"><span data-stu-id="6025a-309">Add this attribute to the Ambiguous Name Resolution (ANR) set.</span></span> <span data-ttu-id="6025a-310">這是用來協助在只提供部分資訊時尋找物件。</span><span class="sxs-lookup"><span data-stu-id="6025a-310">This is used to assist in finding an object when only partial information is given.</span></span> <span data-ttu-id="6025a-311">例如，如果 LDAP 篩選準則是 (ANR = JEFF) ，搜尋會尋找每個物件，其中的名字、姓氏、電子郵件地址或其他 ANR 屬性等於 JEFF。</span><span class="sxs-lookup"><span data-stu-id="6025a-311">For example, if the LDAP filter is (ANR=JEFF), the search will find each object where the first name, last name, email address, or other ANR attribute is equal to JEFF.</span></span> <span data-ttu-id="6025a-312">必須為此索引設定 Bit 0 才會生效。</span><span class="sxs-lookup"><span data-stu-id="6025a-312">Bit 0 must be set for this index take affect.</span></span> |
| <span data-ttu-id="6025a-313">8 (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="6025a-313">8 (0x00000008)</span></span>   | <span data-ttu-id="6025a-314">針對已刪除的物件，將這個屬性保留在標記物件中。</span><span class="sxs-lookup"><span data-stu-id="6025a-314">Preserve this attribute in the tombstone object for deleted objects.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6025a-315">16 (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="6025a-315">16 (0x00000010)</span></span>  | <span data-ttu-id="6025a-316">複製物件時，請複製這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6025a-316">Copy the value for this attribute when the object is copied.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6025a-317">32 (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="6025a-317">32 (0x00000020)</span></span>  | <span data-ttu-id="6025a-318">建立屬性的元組索引。</span><span class="sxs-lookup"><span data-stu-id="6025a-318">Create a tuple index for the attribute.</span></span> <span data-ttu-id="6025a-319">這會改善搜尋字串開頭出現萬用字元的搜尋。</span><span class="sxs-lookup"><span data-stu-id="6025a-319">This will improve searches where the wildcard appears at the front of the search string.</span></span> <span data-ttu-id="6025a-320">例如， (sn = \* mith) 。</span><span class="sxs-lookup"><span data-stu-id="6025a-320">For example, (sn=\*mith).</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="6025a-321">64 (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="6025a-321">64(0x00000040)</span></span>   | <span data-ttu-id="6025a-322">從 ADAM 開始支援。</span><span class="sxs-lookup"><span data-stu-id="6025a-322">Supported beginning with ADAM.</span></span> <span data-ttu-id="6025a-323">建立索引，以大幅協助 VLV 任意屬性的效能。</span><span class="sxs-lookup"><span data-stu-id="6025a-323">Creates an index to greatly help VLV performance on arbitrary attributes.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6025a-324">128 (0x00000080) </span><span class="sxs-lookup"><span data-stu-id="6025a-324">128 (0x00000080)</span></span> | <span data-ttu-id="6025a-325">將屬性標示為機密。</span><span class="sxs-lookup"><span data-stu-id="6025a-325">Mark attribute as confidential.</span></span> <span data-ttu-id="6025a-326">已忽略基底架構屬性 (systemFlags = 0x10) 。</span><span class="sxs-lookup"><span data-stu-id="6025a-326">Ignored for base schema attributes (systemFlags=0x10).</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6025a-327">64 (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="6025a-327">64 (0x00000040)</span></span>  | <span data-ttu-id="6025a-328">從 Windows Server 2008 開始支援。</span><span class="sxs-lookup"><span data-stu-id="6025a-328">Supported beginning with Windows Server 2008.</span></span> <span data-ttu-id="6025a-329">建立索引，以改善這個屬性的 VLV 搜尋效能。</span><span class="sxs-lookup"><span data-stu-id="6025a-329">Create an index to improve VLV search performance on this attribute.</span></span>                                                                                                                                                                                                                                                        |



 

 

 





