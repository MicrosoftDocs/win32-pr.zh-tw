---
title: 是-局部屬性集屬性的成員
description: 若為 TRUE，則會將此屬性複寫至通用類別目錄。
ms.assetid: 9ffd85e8-da1a-4b39-9758-2dc049204ca0
ms.tgt_platform: multiple
keywords:
- 是-Partial 屬性-Set 屬性 AD 架構的成員
- isMemberOfPartialAttributeSet 屬性 AD 架構
topic_type:
- apiref
api_name:
- Is-Member-Of-Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbbd05f95a46ec4e42c139ddda157a4057bde60
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935241"
---
# <a name="is-member-of-partial-attribute-set-attribute"></a><span data-ttu-id="48897-105">是-局部屬性集屬性的成員</span><span class="sxs-lookup"><span data-stu-id="48897-105">Is-Member-Of-Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="48897-106">若 **為 TRUE**，則會將此屬性複寫至通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="48897-106">If **TRUE**, this attribute is replicated to the global catalog.</span></span>



| <span data-ttu-id="48897-107">進入</span><span class="sxs-lookup"><span data-stu-id="48897-107">Entry</span></span> | <span data-ttu-id="48897-108">值</span><span class="sxs-lookup"><span data-stu-id="48897-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="48897-109">CN</span><span class="sxs-lookup"><span data-stu-id="48897-109">CN</span></span>                | <span data-ttu-id="48897-110">是-Partial 屬性集的成員</span><span class="sxs-lookup"><span data-stu-id="48897-110">Is-Member-Of-Partial-Attribute-Set</span></span>   |
| <span data-ttu-id="48897-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="48897-111">Ldap-Display-Name</span></span> | <span data-ttu-id="48897-112">isMemberOfPartialAttributeSet</span><span class="sxs-lookup"><span data-stu-id="48897-112">isMemberOfPartialAttributeSet</span></span>        |
| <span data-ttu-id="48897-113">大小</span><span class="sxs-lookup"><span data-stu-id="48897-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="48897-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="48897-114">Update Privilege</span></span>  | <span data-ttu-id="48897-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="48897-115">Schema administrator</span></span>                 |
| <span data-ttu-id="48897-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="48897-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="48897-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48897-117">Attribute-Id</span></span>      | <span data-ttu-id="48897-118">1.2.840.113556.1.4.639</span><span class="sxs-lookup"><span data-stu-id="48897-118">1.2.840.113556.1.4.639</span></span>               |
| <span data-ttu-id="48897-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="48897-119">System-Id-Guid</span></span>    | <span data-ttu-id="48897-120">19405b9d-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="48897-120">19405b9d-3cfa-11d1-a9c0-0000f80367c1</span></span> |
| <span data-ttu-id="48897-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="48897-121">Syntax</span></span>            | [<span data-ttu-id="48897-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="48897-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="48897-123">實作</span><span class="sxs-lookup"><span data-stu-id="48897-123">Implementations</span></span>

-   [<span data-ttu-id="48897-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="48897-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="48897-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48897-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48897-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="48897-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="48897-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48897-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48897-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48897-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48897-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48897-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48897-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48897-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="48897-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="48897-131">Windows 2000 Server</span></span>



| <span data-ttu-id="48897-132">進入</span><span class="sxs-lookup"><span data-stu-id="48897-132">Entry</span></span> | <span data-ttu-id="48897-133">值</span><span class="sxs-lookup"><span data-stu-id="48897-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48897-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48897-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48897-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="48897-136">System-Only</span></span>            | <span data-ttu-id="48897-137">否</span><span class="sxs-lookup"><span data-stu-id="48897-137">False</span></span>                                                    |
| <span data-ttu-id="48897-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48897-138">Is-Single-Valued</span></span>       | <span data-ttu-id="48897-139">對</span><span class="sxs-lookup"><span data-stu-id="48897-139">True</span></span>                                                     |
| <span data-ttu-id="48897-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48897-140">Is Indexed</span></span>             | <span data-ttu-id="48897-141">否</span><span class="sxs-lookup"><span data-stu-id="48897-141">False</span></span>                                                    |
| <span data-ttu-id="48897-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48897-142">In Global Catalog</span></span>      | <span data-ttu-id="48897-143">否</span><span class="sxs-lookup"><span data-stu-id="48897-143">False</span></span>                                                    |
| <span data-ttu-id="48897-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48897-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="48897-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48897-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48897-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48897-146">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48897-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48897-147">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48897-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-148">Search-Flags</span></span>           | <span data-ttu-id="48897-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48897-149">0x00000000</span></span>                                               |
| <span data-ttu-id="48897-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-150">System-Flags</span></span>           | <span data-ttu-id="48897-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48897-151">0x00000010</span></span>                                               |
| <span data-ttu-id="48897-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48897-152">Classes used in</span></span>        | [<span data-ttu-id="48897-153">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="48897-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="48897-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48897-154">Windows Server 2003</span></span>



| <span data-ttu-id="48897-155">進入</span><span class="sxs-lookup"><span data-stu-id="48897-155">Entry</span></span> | <span data-ttu-id="48897-156">值</span><span class="sxs-lookup"><span data-stu-id="48897-156">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48897-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48897-157">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48897-158">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="48897-159">System-Only</span></span>            | <span data-ttu-id="48897-160">否</span><span class="sxs-lookup"><span data-stu-id="48897-160">False</span></span>                                                    |
| <span data-ttu-id="48897-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48897-161">Is-Single-Valued</span></span>       | <span data-ttu-id="48897-162">對</span><span class="sxs-lookup"><span data-stu-id="48897-162">True</span></span>                                                     |
| <span data-ttu-id="48897-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48897-163">Is Indexed</span></span>             | <span data-ttu-id="48897-164">否</span><span class="sxs-lookup"><span data-stu-id="48897-164">False</span></span>                                                    |
| <span data-ttu-id="48897-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48897-165">In Global Catalog</span></span>      | <span data-ttu-id="48897-166">否</span><span class="sxs-lookup"><span data-stu-id="48897-166">False</span></span>                                                    |
| <span data-ttu-id="48897-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48897-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="48897-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48897-168">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48897-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48897-169">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48897-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48897-170">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48897-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-171">Search-Flags</span></span>           | <span data-ttu-id="48897-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48897-172">0x00000000</span></span>                                               |
| <span data-ttu-id="48897-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-173">System-Flags</span></span>           | <span data-ttu-id="48897-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48897-174">0x00000010</span></span>                                               |
| <span data-ttu-id="48897-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48897-175">Classes used in</span></span>        | [<span data-ttu-id="48897-176">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="48897-176">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="48897-177">亞當</span><span class="sxs-lookup"><span data-stu-id="48897-177">ADAM</span></span>



| <span data-ttu-id="48897-178">進入</span><span class="sxs-lookup"><span data-stu-id="48897-178">Entry</span></span> | <span data-ttu-id="48897-179">值</span><span class="sxs-lookup"><span data-stu-id="48897-179">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48897-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48897-180">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48897-181">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="48897-182">System-Only</span></span>            | <span data-ttu-id="48897-183">否</span><span class="sxs-lookup"><span data-stu-id="48897-183">False</span></span>                                                    |
| <span data-ttu-id="48897-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48897-184">Is-Single-Valued</span></span>       | <span data-ttu-id="48897-185">對</span><span class="sxs-lookup"><span data-stu-id="48897-185">True</span></span>                                                     |
| <span data-ttu-id="48897-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48897-186">Is Indexed</span></span>             | <span data-ttu-id="48897-187">否</span><span class="sxs-lookup"><span data-stu-id="48897-187">False</span></span>                                                    |
| <span data-ttu-id="48897-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48897-188">In Global Catalog</span></span>      | <span data-ttu-id="48897-189">否</span><span class="sxs-lookup"><span data-stu-id="48897-189">False</span></span>                                                    |
| <span data-ttu-id="48897-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48897-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="48897-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48897-191">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48897-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48897-192">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48897-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48897-193">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48897-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-194">Search-Flags</span></span>           | <span data-ttu-id="48897-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48897-195">0x00000000</span></span>                                               |
| <span data-ttu-id="48897-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-196">System-Flags</span></span>           | <span data-ttu-id="48897-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48897-197">0x00000010</span></span>                                               |
| <span data-ttu-id="48897-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48897-198">Classes used in</span></span>        | [<span data-ttu-id="48897-199">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="48897-199">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48897-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48897-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48897-201">進入</span><span class="sxs-lookup"><span data-stu-id="48897-201">Entry</span></span> | <span data-ttu-id="48897-202">值</span><span class="sxs-lookup"><span data-stu-id="48897-202">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48897-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48897-203">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48897-204">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="48897-205">System-Only</span></span>            | <span data-ttu-id="48897-206">否</span><span class="sxs-lookup"><span data-stu-id="48897-206">False</span></span>                                                    |
| <span data-ttu-id="48897-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48897-207">Is-Single-Valued</span></span>       | <span data-ttu-id="48897-208">對</span><span class="sxs-lookup"><span data-stu-id="48897-208">True</span></span>                                                     |
| <span data-ttu-id="48897-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48897-209">Is Indexed</span></span>             | <span data-ttu-id="48897-210">否</span><span class="sxs-lookup"><span data-stu-id="48897-210">False</span></span>                                                    |
| <span data-ttu-id="48897-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48897-211">In Global Catalog</span></span>      | <span data-ttu-id="48897-212">否</span><span class="sxs-lookup"><span data-stu-id="48897-212">False</span></span>                                                    |
| <span data-ttu-id="48897-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48897-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="48897-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48897-214">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48897-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48897-215">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48897-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48897-216">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48897-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-217">Search-Flags</span></span>           | <span data-ttu-id="48897-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48897-218">0x00000000</span></span>                                               |
| <span data-ttu-id="48897-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-219">System-Flags</span></span>           | <span data-ttu-id="48897-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48897-220">0x00000010</span></span>                                               |
| <span data-ttu-id="48897-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48897-221">Classes used in</span></span>        | [<span data-ttu-id="48897-222">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="48897-222">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48897-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48897-223">Windows Server 2008</span></span>



| <span data-ttu-id="48897-224">進入</span><span class="sxs-lookup"><span data-stu-id="48897-224">Entry</span></span> | <span data-ttu-id="48897-225">值</span><span class="sxs-lookup"><span data-stu-id="48897-225">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48897-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48897-226">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48897-227">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="48897-228">System-Only</span></span>            | <span data-ttu-id="48897-229">否</span><span class="sxs-lookup"><span data-stu-id="48897-229">False</span></span>                                                    |
| <span data-ttu-id="48897-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48897-230">Is-Single-Valued</span></span>       | <span data-ttu-id="48897-231">對</span><span class="sxs-lookup"><span data-stu-id="48897-231">True</span></span>                                                     |
| <span data-ttu-id="48897-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48897-232">Is Indexed</span></span>             | <span data-ttu-id="48897-233">否</span><span class="sxs-lookup"><span data-stu-id="48897-233">False</span></span>                                                    |
| <span data-ttu-id="48897-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48897-234">In Global Catalog</span></span>      | <span data-ttu-id="48897-235">否</span><span class="sxs-lookup"><span data-stu-id="48897-235">False</span></span>                                                    |
| <span data-ttu-id="48897-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48897-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="48897-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48897-237">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48897-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48897-238">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48897-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48897-239">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48897-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-240">Search-Flags</span></span>           | <span data-ttu-id="48897-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48897-241">0x00000000</span></span>                                               |
| <span data-ttu-id="48897-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-242">System-Flags</span></span>           | <span data-ttu-id="48897-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48897-243">0x00000010</span></span>                                               |
| <span data-ttu-id="48897-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48897-244">Classes used in</span></span>        | [<span data-ttu-id="48897-245">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="48897-245">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48897-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48897-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48897-247">進入</span><span class="sxs-lookup"><span data-stu-id="48897-247">Entry</span></span> | <span data-ttu-id="48897-248">值</span><span class="sxs-lookup"><span data-stu-id="48897-248">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48897-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48897-249">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48897-250">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="48897-251">System-Only</span></span>            | <span data-ttu-id="48897-252">否</span><span class="sxs-lookup"><span data-stu-id="48897-252">False</span></span>                                                    |
| <span data-ttu-id="48897-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48897-253">Is-Single-Valued</span></span>       | <span data-ttu-id="48897-254">對</span><span class="sxs-lookup"><span data-stu-id="48897-254">True</span></span>                                                     |
| <span data-ttu-id="48897-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48897-255">Is Indexed</span></span>             | <span data-ttu-id="48897-256">否</span><span class="sxs-lookup"><span data-stu-id="48897-256">False</span></span>                                                    |
| <span data-ttu-id="48897-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48897-257">In Global Catalog</span></span>      | <span data-ttu-id="48897-258">否</span><span class="sxs-lookup"><span data-stu-id="48897-258">False</span></span>                                                    |
| <span data-ttu-id="48897-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48897-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="48897-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48897-260">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48897-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48897-261">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48897-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48897-262">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48897-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-263">Search-Flags</span></span>           | <span data-ttu-id="48897-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48897-264">0x00000000</span></span>                                               |
| <span data-ttu-id="48897-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-265">System-Flags</span></span>           | <span data-ttu-id="48897-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48897-266">0x00000010</span></span>                                               |
| <span data-ttu-id="48897-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48897-267">Classes used in</span></span>        | [<span data-ttu-id="48897-268">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="48897-268">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48897-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48897-269">Windows Server 2012</span></span>



| <span data-ttu-id="48897-270">進入</span><span class="sxs-lookup"><span data-stu-id="48897-270">Entry</span></span> | <span data-ttu-id="48897-271">值</span><span class="sxs-lookup"><span data-stu-id="48897-271">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="48897-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48897-272">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48897-273">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="48897-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="48897-274">System-Only</span></span>            | <span data-ttu-id="48897-275">否</span><span class="sxs-lookup"><span data-stu-id="48897-275">False</span></span>                                                    |
| <span data-ttu-id="48897-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48897-276">Is-Single-Valued</span></span>       | <span data-ttu-id="48897-277">對</span><span class="sxs-lookup"><span data-stu-id="48897-277">True</span></span>                                                     |
| <span data-ttu-id="48897-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48897-278">Is Indexed</span></span>             | <span data-ttu-id="48897-279">否</span><span class="sxs-lookup"><span data-stu-id="48897-279">False</span></span>                                                    |
| <span data-ttu-id="48897-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48897-280">In Global Catalog</span></span>      | <span data-ttu-id="48897-281">否</span><span class="sxs-lookup"><span data-stu-id="48897-281">False</span></span>                                                    |
| <span data-ttu-id="48897-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48897-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="48897-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48897-283">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="48897-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48897-284">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="48897-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48897-285">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="48897-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-286">Search-Flags</span></span>           | <span data-ttu-id="48897-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48897-287">0x00000000</span></span>                                               |
| <span data-ttu-id="48897-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48897-288">System-Flags</span></span>           | <span data-ttu-id="48897-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48897-289">0x00000010</span></span>                                               |
| <span data-ttu-id="48897-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48897-290">Classes used in</span></span>        | [<span data-ttu-id="48897-291">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="48897-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





