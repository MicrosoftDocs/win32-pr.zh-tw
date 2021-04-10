---
title: 是-單一值屬性
description: 若為 TRUE，則這個屬性只能儲存一個值。
ms.assetid: 53dd8dfe-2123-4a61-a346-12abe340ea11
ms.tgt_platform: multiple
keywords:
- 為-單一值屬性 AD 架構
- isSingleValued 屬性 AD 架構
topic_type:
- apiref
api_name:
- Is-Single-Valued
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a1fafd047afa47b874fb0385a690e2c0d13161
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844740"
---
# <a name="is-single-valued-attribute"></a><span data-ttu-id="a1285-105">是-單一值屬性</span><span class="sxs-lookup"><span data-stu-id="a1285-105">Is-Single-Valued attribute</span></span>

<span data-ttu-id="a1285-106">若 **為 TRUE**，則這個屬性只能儲存一個值。</span><span class="sxs-lookup"><span data-stu-id="a1285-106">If **TRUE**, this attribute can only store one value.</span></span>



| <span data-ttu-id="a1285-107">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-107">Entry</span></span> | <span data-ttu-id="a1285-108">值</span><span class="sxs-lookup"><span data-stu-id="a1285-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a1285-109">CN</span><span class="sxs-lookup"><span data-stu-id="a1285-109">CN</span></span>                | <span data-ttu-id="a1285-110">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-110">Is-Single-Valued</span></span>                     |
| <span data-ttu-id="a1285-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a1285-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a1285-112">isSingleValued</span><span class="sxs-lookup"><span data-stu-id="a1285-112">isSingleValued</span></span>                       |
| <span data-ttu-id="a1285-113">大小</span><span class="sxs-lookup"><span data-stu-id="a1285-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="a1285-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a1285-114">Update Privilege</span></span>  | <span data-ttu-id="a1285-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="a1285-115">Schema administrator</span></span>                 |
| <span data-ttu-id="a1285-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a1285-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a1285-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-117">Attribute-Id</span></span>      | <span data-ttu-id="a1285-118">1.2.840.113556.1.2.33</span><span class="sxs-lookup"><span data-stu-id="a1285-118">1.2.840.113556.1.2.33</span></span>                |
| <span data-ttu-id="a1285-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a1285-119">System-Id-Guid</span></span>    | <span data-ttu-id="a1285-120">bf967992-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a1285-120">bf967992-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a1285-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1285-121">Syntax</span></span>            | [<span data-ttu-id="a1285-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1285-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a1285-123">實作</span><span class="sxs-lookup"><span data-stu-id="a1285-123">Implementations</span></span>

-   [<span data-ttu-id="a1285-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1285-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1285-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1285-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1285-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a1285-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a1285-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1285-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1285-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1285-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1285-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1285-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1285-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1285-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1285-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1285-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a1285-132">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-132">Entry</span></span> | <span data-ttu-id="a1285-133">值</span><span class="sxs-lookup"><span data-stu-id="a1285-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a1285-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a1285-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a1285-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-135">MAPI-Id</span></span>                | <span data-ttu-id="a1285-136">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a1285-136">0x80C1</span></span>                                                   |
| <span data-ttu-id="a1285-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1285-137">System-Only</span></span>            | <span data-ttu-id="a1285-138">對</span><span class="sxs-lookup"><span data-stu-id="a1285-138">True</span></span>                                                     |
| <span data-ttu-id="a1285-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a1285-140">對</span><span class="sxs-lookup"><span data-stu-id="a1285-140">True</span></span>                                                     |
| <span data-ttu-id="a1285-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a1285-141">Is Indexed</span></span>             | <span data-ttu-id="a1285-142">否</span><span class="sxs-lookup"><span data-stu-id="a1285-142">False</span></span>                                                    |
| <span data-ttu-id="a1285-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a1285-143">In Global Catalog</span></span>      | <span data-ttu-id="a1285-144">否</span><span class="sxs-lookup"><span data-stu-id="a1285-144">False</span></span>                                                    |
| <span data-ttu-id="a1285-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a1285-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1285-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a1285-146">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a1285-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1285-147">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1285-148">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-149">Search-Flags</span></span>           | <span data-ttu-id="a1285-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1285-150">0x00000000</span></span>                                               |
| <span data-ttu-id="a1285-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-151">System-Flags</span></span>           | <span data-ttu-id="a1285-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1285-152">0x00000010</span></span>                                               |
| <span data-ttu-id="a1285-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a1285-153">Classes used in</span></span>        | [<span data-ttu-id="a1285-154">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a1285-154">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1285-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1285-155">Windows Server 2003</span></span>



| <span data-ttu-id="a1285-156">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-156">Entry</span></span> | <span data-ttu-id="a1285-157">值</span><span class="sxs-lookup"><span data-stu-id="a1285-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a1285-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a1285-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a1285-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-159">MAPI-Id</span></span>                | <span data-ttu-id="a1285-160">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a1285-160">0x80C1</span></span>                                                   |
| <span data-ttu-id="a1285-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1285-161">System-Only</span></span>            | <span data-ttu-id="a1285-162">對</span><span class="sxs-lookup"><span data-stu-id="a1285-162">True</span></span>                                                     |
| <span data-ttu-id="a1285-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a1285-164">對</span><span class="sxs-lookup"><span data-stu-id="a1285-164">True</span></span>                                                     |
| <span data-ttu-id="a1285-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a1285-165">Is Indexed</span></span>             | <span data-ttu-id="a1285-166">否</span><span class="sxs-lookup"><span data-stu-id="a1285-166">False</span></span>                                                    |
| <span data-ttu-id="a1285-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a1285-167">In Global Catalog</span></span>      | <span data-ttu-id="a1285-168">否</span><span class="sxs-lookup"><span data-stu-id="a1285-168">False</span></span>                                                    |
| <span data-ttu-id="a1285-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a1285-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1285-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a1285-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a1285-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1285-171">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1285-172">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-173">Search-Flags</span></span>           | <span data-ttu-id="a1285-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1285-174">0x00000000</span></span>                                               |
| <span data-ttu-id="a1285-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-175">System-Flags</span></span>           | <span data-ttu-id="a1285-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1285-176">0x00000010</span></span>                                               |
| <span data-ttu-id="a1285-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a1285-177">Classes used in</span></span>        | [<span data-ttu-id="a1285-178">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a1285-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a1285-179">亞當</span><span class="sxs-lookup"><span data-stu-id="a1285-179">ADAM</span></span>



| <span data-ttu-id="a1285-180">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-180">Entry</span></span> | <span data-ttu-id="a1285-181">值</span><span class="sxs-lookup"><span data-stu-id="a1285-181">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a1285-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a1285-182">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a1285-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-183">MAPI-Id</span></span>                | <span data-ttu-id="a1285-184">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a1285-184">0x80C1</span></span>                                                   |
| <span data-ttu-id="a1285-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1285-185">System-Only</span></span>            | <span data-ttu-id="a1285-186">對</span><span class="sxs-lookup"><span data-stu-id="a1285-186">True</span></span>                                                     |
| <span data-ttu-id="a1285-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a1285-188">對</span><span class="sxs-lookup"><span data-stu-id="a1285-188">True</span></span>                                                     |
| <span data-ttu-id="a1285-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a1285-189">Is Indexed</span></span>             | <span data-ttu-id="a1285-190">否</span><span class="sxs-lookup"><span data-stu-id="a1285-190">False</span></span>                                                    |
| <span data-ttu-id="a1285-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a1285-191">In Global Catalog</span></span>      | <span data-ttu-id="a1285-192">否</span><span class="sxs-lookup"><span data-stu-id="a1285-192">False</span></span>                                                    |
| <span data-ttu-id="a1285-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a1285-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1285-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a1285-194">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a1285-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1285-195">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1285-196">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-197">Search-Flags</span></span>           | <span data-ttu-id="a1285-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1285-198">0x00000000</span></span>                                               |
| <span data-ttu-id="a1285-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-199">System-Flags</span></span>           | <span data-ttu-id="a1285-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1285-200">0x00000010</span></span>                                               |
| <span data-ttu-id="a1285-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a1285-201">Classes used in</span></span>        | [<span data-ttu-id="a1285-202">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a1285-202">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1285-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1285-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1285-204">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-204">Entry</span></span> | <span data-ttu-id="a1285-205">值</span><span class="sxs-lookup"><span data-stu-id="a1285-205">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a1285-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a1285-206">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a1285-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-207">MAPI-Id</span></span>                | <span data-ttu-id="a1285-208">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a1285-208">0x80C1</span></span>                                                   |
| <span data-ttu-id="a1285-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1285-209">System-Only</span></span>            | <span data-ttu-id="a1285-210">對</span><span class="sxs-lookup"><span data-stu-id="a1285-210">True</span></span>                                                     |
| <span data-ttu-id="a1285-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a1285-212">對</span><span class="sxs-lookup"><span data-stu-id="a1285-212">True</span></span>                                                     |
| <span data-ttu-id="a1285-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a1285-213">Is Indexed</span></span>             | <span data-ttu-id="a1285-214">否</span><span class="sxs-lookup"><span data-stu-id="a1285-214">False</span></span>                                                    |
| <span data-ttu-id="a1285-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a1285-215">In Global Catalog</span></span>      | <span data-ttu-id="a1285-216">否</span><span class="sxs-lookup"><span data-stu-id="a1285-216">False</span></span>                                                    |
| <span data-ttu-id="a1285-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a1285-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1285-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a1285-218">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a1285-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1285-219">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1285-220">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-221">Search-Flags</span></span>           | <span data-ttu-id="a1285-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1285-222">0x00000000</span></span>                                               |
| <span data-ttu-id="a1285-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-223">System-Flags</span></span>           | <span data-ttu-id="a1285-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1285-224">0x00000010</span></span>                                               |
| <span data-ttu-id="a1285-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a1285-225">Classes used in</span></span>        | [<span data-ttu-id="a1285-226">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a1285-226">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1285-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1285-227">Windows Server 2008</span></span>



| <span data-ttu-id="a1285-228">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-228">Entry</span></span> | <span data-ttu-id="a1285-229">值</span><span class="sxs-lookup"><span data-stu-id="a1285-229">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a1285-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a1285-230">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a1285-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-231">MAPI-Id</span></span>                | <span data-ttu-id="a1285-232">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a1285-232">0x80C1</span></span>                                                   |
| <span data-ttu-id="a1285-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1285-233">System-Only</span></span>            | <span data-ttu-id="a1285-234">對</span><span class="sxs-lookup"><span data-stu-id="a1285-234">True</span></span>                                                     |
| <span data-ttu-id="a1285-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-235">Is-Single-Valued</span></span>       | <span data-ttu-id="a1285-236">對</span><span class="sxs-lookup"><span data-stu-id="a1285-236">True</span></span>                                                     |
| <span data-ttu-id="a1285-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a1285-237">Is Indexed</span></span>             | <span data-ttu-id="a1285-238">否</span><span class="sxs-lookup"><span data-stu-id="a1285-238">False</span></span>                                                    |
| <span data-ttu-id="a1285-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a1285-239">In Global Catalog</span></span>      | <span data-ttu-id="a1285-240">否</span><span class="sxs-lookup"><span data-stu-id="a1285-240">False</span></span>                                                    |
| <span data-ttu-id="a1285-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a1285-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1285-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a1285-242">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a1285-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1285-243">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1285-244">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-245">Search-Flags</span></span>           | <span data-ttu-id="a1285-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1285-246">0x00000000</span></span>                                               |
| <span data-ttu-id="a1285-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-247">System-Flags</span></span>           | <span data-ttu-id="a1285-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1285-248">0x00000010</span></span>                                               |
| <span data-ttu-id="a1285-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a1285-249">Classes used in</span></span>        | [<span data-ttu-id="a1285-250">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a1285-250">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1285-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1285-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1285-252">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-252">Entry</span></span> | <span data-ttu-id="a1285-253">值</span><span class="sxs-lookup"><span data-stu-id="a1285-253">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a1285-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a1285-254">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a1285-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-255">MAPI-Id</span></span>                | <span data-ttu-id="a1285-256">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a1285-256">0x80C1</span></span>                                                   |
| <span data-ttu-id="a1285-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1285-257">System-Only</span></span>            | <span data-ttu-id="a1285-258">對</span><span class="sxs-lookup"><span data-stu-id="a1285-258">True</span></span>                                                     |
| <span data-ttu-id="a1285-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a1285-260">對</span><span class="sxs-lookup"><span data-stu-id="a1285-260">True</span></span>                                                     |
| <span data-ttu-id="a1285-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a1285-261">Is Indexed</span></span>             | <span data-ttu-id="a1285-262">否</span><span class="sxs-lookup"><span data-stu-id="a1285-262">False</span></span>                                                    |
| <span data-ttu-id="a1285-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a1285-263">In Global Catalog</span></span>      | <span data-ttu-id="a1285-264">否</span><span class="sxs-lookup"><span data-stu-id="a1285-264">False</span></span>                                                    |
| <span data-ttu-id="a1285-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a1285-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1285-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a1285-266">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a1285-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1285-267">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1285-268">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-269">Search-Flags</span></span>           | <span data-ttu-id="a1285-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1285-270">0x00000000</span></span>                                               |
| <span data-ttu-id="a1285-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-271">System-Flags</span></span>           | <span data-ttu-id="a1285-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1285-272">0x00000010</span></span>                                               |
| <span data-ttu-id="a1285-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a1285-273">Classes used in</span></span>        | [<span data-ttu-id="a1285-274">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a1285-274">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1285-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1285-275">Windows Server 2012</span></span>



| <span data-ttu-id="a1285-276">進入</span><span class="sxs-lookup"><span data-stu-id="a1285-276">Entry</span></span> | <span data-ttu-id="a1285-277">值</span><span class="sxs-lookup"><span data-stu-id="a1285-277">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a1285-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a1285-278">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a1285-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1285-279">MAPI-Id</span></span>                | <span data-ttu-id="a1285-280">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a1285-280">0x80C1</span></span>                                                   |
| <span data-ttu-id="a1285-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1285-281">System-Only</span></span>            | <span data-ttu-id="a1285-282">對</span><span class="sxs-lookup"><span data-stu-id="a1285-282">True</span></span>                                                     |
| <span data-ttu-id="a1285-283">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a1285-283">Is-Single-Valued</span></span>       | <span data-ttu-id="a1285-284">對</span><span class="sxs-lookup"><span data-stu-id="a1285-284">True</span></span>                                                     |
| <span data-ttu-id="a1285-285">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a1285-285">Is Indexed</span></span>             | <span data-ttu-id="a1285-286">否</span><span class="sxs-lookup"><span data-stu-id="a1285-286">False</span></span>                                                    |
| <span data-ttu-id="a1285-287">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a1285-287">In Global Catalog</span></span>      | <span data-ttu-id="a1285-288">否</span><span class="sxs-lookup"><span data-stu-id="a1285-288">False</span></span>                                                    |
| <span data-ttu-id="a1285-289">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a1285-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1285-290">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a1285-290">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a1285-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1285-291">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1285-292">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a1285-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-293">Search-Flags</span></span>           | <span data-ttu-id="a1285-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1285-294">0x00000000</span></span>                                               |
| <span data-ttu-id="a1285-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1285-295">System-Flags</span></span>           | <span data-ttu-id="a1285-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1285-296">0x00000010</span></span>                                               |
| <span data-ttu-id="a1285-297">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a1285-297">Classes used in</span></span>        | [<span data-ttu-id="a1285-298">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a1285-298">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





