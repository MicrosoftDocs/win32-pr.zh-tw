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
# <a name="is-single-valued-attribute"></a><span data-ttu-id="a65a9-105">是-單一值屬性</span><span class="sxs-lookup"><span data-stu-id="a65a9-105">Is-Single-Valued attribute</span></span>

<span data-ttu-id="a65a9-106">若 **為 TRUE**，則這個屬性只能儲存一個值。</span><span class="sxs-lookup"><span data-stu-id="a65a9-106">If **TRUE**, this attribute can only store one value.</span></span>



| <span data-ttu-id="a65a9-107">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-107">Entry</span></span> | <span data-ttu-id="a65a9-108">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a65a9-109">CN</span><span class="sxs-lookup"><span data-stu-id="a65a9-109">CN</span></span>                | <span data-ttu-id="a65a9-110">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-110">Is-Single-Valued</span></span>                     |
| <span data-ttu-id="a65a9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a65a9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a65a9-112">isSingleValued</span><span class="sxs-lookup"><span data-stu-id="a65a9-112">isSingleValued</span></span>                       |
| <span data-ttu-id="a65a9-113">大小</span><span class="sxs-lookup"><span data-stu-id="a65a9-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="a65a9-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a65a9-114">Update Privilege</span></span>  | <span data-ttu-id="a65a9-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="a65a9-115">Schema administrator</span></span>                 |
| <span data-ttu-id="a65a9-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a65a9-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a65a9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-117">Attribute-Id</span></span>      | <span data-ttu-id="a65a9-118">1.2.840.113556.1.2.33</span><span class="sxs-lookup"><span data-stu-id="a65a9-118">1.2.840.113556.1.2.33</span></span>                |
| <span data-ttu-id="a65a9-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a65a9-119">System-Id-Guid</span></span>    | <span data-ttu-id="a65a9-120">bf967992-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a65a9-120">bf967992-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a65a9-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="a65a9-121">Syntax</span></span>            | [<span data-ttu-id="a65a9-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a65a9-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a65a9-123">實作</span><span class="sxs-lookup"><span data-stu-id="a65a9-123">Implementations</span></span>

-   [<span data-ttu-id="a65a9-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a65a9-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a65a9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a65a9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a65a9-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a65a9-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a65a9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a65a9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a65a9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a65a9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a65a9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a65a9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a65a9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a65a9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a65a9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a65a9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a65a9-132">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-132">Entry</span></span> | <span data-ttu-id="a65a9-133">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a65a9-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a65a9-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a65a9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-135">MAPI-Id</span></span>                | <span data-ttu-id="a65a9-136">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a65a9-136">0x80C1</span></span>                                                   |
| <span data-ttu-id="a65a9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a65a9-137">System-Only</span></span>            | <span data-ttu-id="a65a9-138">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-138">True</span></span>                                                     |
| <span data-ttu-id="a65a9-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a65a9-140">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-140">True</span></span>                                                     |
| <span data-ttu-id="a65a9-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a65a9-141">Is Indexed</span></span>             | <span data-ttu-id="a65a9-142">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-142">False</span></span>                                                    |
| <span data-ttu-id="a65a9-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a65a9-143">In Global Catalog</span></span>      | <span data-ttu-id="a65a9-144">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-144">False</span></span>                                                    |
| <span data-ttu-id="a65a9-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a65a9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a65a9-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a65a9-146">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a65a9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a65a9-147">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a65a9-148">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-149">Search-Flags</span></span>           | <span data-ttu-id="a65a9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a65a9-150">0x00000000</span></span>                                               |
| <span data-ttu-id="a65a9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-151">System-Flags</span></span>           | <span data-ttu-id="a65a9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a65a9-152">0x00000010</span></span>                                               |
| <span data-ttu-id="a65a9-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a65a9-153">Classes used in</span></span>        | [<span data-ttu-id="a65a9-154">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a65a9-154">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a65a9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a65a9-155">Windows Server 2003</span></span>



| <span data-ttu-id="a65a9-156">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-156">Entry</span></span> | <span data-ttu-id="a65a9-157">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a65a9-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a65a9-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a65a9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-159">MAPI-Id</span></span>                | <span data-ttu-id="a65a9-160">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a65a9-160">0x80C1</span></span>                                                   |
| <span data-ttu-id="a65a9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a65a9-161">System-Only</span></span>            | <span data-ttu-id="a65a9-162">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-162">True</span></span>                                                     |
| <span data-ttu-id="a65a9-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a65a9-164">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-164">True</span></span>                                                     |
| <span data-ttu-id="a65a9-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a65a9-165">Is Indexed</span></span>             | <span data-ttu-id="a65a9-166">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-166">False</span></span>                                                    |
| <span data-ttu-id="a65a9-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a65a9-167">In Global Catalog</span></span>      | <span data-ttu-id="a65a9-168">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-168">False</span></span>                                                    |
| <span data-ttu-id="a65a9-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a65a9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a65a9-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a65a9-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a65a9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a65a9-171">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a65a9-172">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-173">Search-Flags</span></span>           | <span data-ttu-id="a65a9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a65a9-174">0x00000000</span></span>                                               |
| <span data-ttu-id="a65a9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-175">System-Flags</span></span>           | <span data-ttu-id="a65a9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a65a9-176">0x00000010</span></span>                                               |
| <span data-ttu-id="a65a9-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a65a9-177">Classes used in</span></span>        | [<span data-ttu-id="a65a9-178">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a65a9-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a65a9-179">亞當</span><span class="sxs-lookup"><span data-stu-id="a65a9-179">ADAM</span></span>



| <span data-ttu-id="a65a9-180">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-180">Entry</span></span> | <span data-ttu-id="a65a9-181">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-181">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a65a9-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a65a9-182">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a65a9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-183">MAPI-Id</span></span>                | <span data-ttu-id="a65a9-184">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a65a9-184">0x80C1</span></span>                                                   |
| <span data-ttu-id="a65a9-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a65a9-185">System-Only</span></span>            | <span data-ttu-id="a65a9-186">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-186">True</span></span>                                                     |
| <span data-ttu-id="a65a9-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a65a9-188">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-188">True</span></span>                                                     |
| <span data-ttu-id="a65a9-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a65a9-189">Is Indexed</span></span>             | <span data-ttu-id="a65a9-190">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-190">False</span></span>                                                    |
| <span data-ttu-id="a65a9-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a65a9-191">In Global Catalog</span></span>      | <span data-ttu-id="a65a9-192">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-192">False</span></span>                                                    |
| <span data-ttu-id="a65a9-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a65a9-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a65a9-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a65a9-194">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a65a9-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a65a9-195">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a65a9-196">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-197">Search-Flags</span></span>           | <span data-ttu-id="a65a9-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a65a9-198">0x00000000</span></span>                                               |
| <span data-ttu-id="a65a9-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-199">System-Flags</span></span>           | <span data-ttu-id="a65a9-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a65a9-200">0x00000010</span></span>                                               |
| <span data-ttu-id="a65a9-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a65a9-201">Classes used in</span></span>        | [<span data-ttu-id="a65a9-202">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a65a9-202">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a65a9-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a65a9-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a65a9-204">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-204">Entry</span></span> | <span data-ttu-id="a65a9-205">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-205">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a65a9-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a65a9-206">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a65a9-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-207">MAPI-Id</span></span>                | <span data-ttu-id="a65a9-208">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a65a9-208">0x80C1</span></span>                                                   |
| <span data-ttu-id="a65a9-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a65a9-209">System-Only</span></span>            | <span data-ttu-id="a65a9-210">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-210">True</span></span>                                                     |
| <span data-ttu-id="a65a9-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a65a9-212">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-212">True</span></span>                                                     |
| <span data-ttu-id="a65a9-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a65a9-213">Is Indexed</span></span>             | <span data-ttu-id="a65a9-214">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-214">False</span></span>                                                    |
| <span data-ttu-id="a65a9-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a65a9-215">In Global Catalog</span></span>      | <span data-ttu-id="a65a9-216">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-216">False</span></span>                                                    |
| <span data-ttu-id="a65a9-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a65a9-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a65a9-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a65a9-218">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a65a9-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a65a9-219">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a65a9-220">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-221">Search-Flags</span></span>           | <span data-ttu-id="a65a9-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a65a9-222">0x00000000</span></span>                                               |
| <span data-ttu-id="a65a9-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-223">System-Flags</span></span>           | <span data-ttu-id="a65a9-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a65a9-224">0x00000010</span></span>                                               |
| <span data-ttu-id="a65a9-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a65a9-225">Classes used in</span></span>        | [<span data-ttu-id="a65a9-226">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a65a9-226">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a65a9-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a65a9-227">Windows Server 2008</span></span>



| <span data-ttu-id="a65a9-228">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-228">Entry</span></span> | <span data-ttu-id="a65a9-229">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-229">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a65a9-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a65a9-230">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a65a9-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-231">MAPI-Id</span></span>                | <span data-ttu-id="a65a9-232">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a65a9-232">0x80C1</span></span>                                                   |
| <span data-ttu-id="a65a9-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="a65a9-233">System-Only</span></span>            | <span data-ttu-id="a65a9-234">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-234">True</span></span>                                                     |
| <span data-ttu-id="a65a9-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-235">Is-Single-Valued</span></span>       | <span data-ttu-id="a65a9-236">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-236">True</span></span>                                                     |
| <span data-ttu-id="a65a9-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a65a9-237">Is Indexed</span></span>             | <span data-ttu-id="a65a9-238">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-238">False</span></span>                                                    |
| <span data-ttu-id="a65a9-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a65a9-239">In Global Catalog</span></span>      | <span data-ttu-id="a65a9-240">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-240">False</span></span>                                                    |
| <span data-ttu-id="a65a9-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a65a9-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="a65a9-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a65a9-242">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a65a9-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a65a9-243">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a65a9-244">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-245">Search-Flags</span></span>           | <span data-ttu-id="a65a9-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a65a9-246">0x00000000</span></span>                                               |
| <span data-ttu-id="a65a9-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-247">System-Flags</span></span>           | <span data-ttu-id="a65a9-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a65a9-248">0x00000010</span></span>                                               |
| <span data-ttu-id="a65a9-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a65a9-249">Classes used in</span></span>        | [<span data-ttu-id="a65a9-250">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a65a9-250">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a65a9-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a65a9-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a65a9-252">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-252">Entry</span></span> | <span data-ttu-id="a65a9-253">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-253">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a65a9-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a65a9-254">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a65a9-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-255">MAPI-Id</span></span>                | <span data-ttu-id="a65a9-256">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a65a9-256">0x80C1</span></span>                                                   |
| <span data-ttu-id="a65a9-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="a65a9-257">System-Only</span></span>            | <span data-ttu-id="a65a9-258">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-258">True</span></span>                                                     |
| <span data-ttu-id="a65a9-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-259">Is-Single-Valued</span></span>       | <span data-ttu-id="a65a9-260">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-260">True</span></span>                                                     |
| <span data-ttu-id="a65a9-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a65a9-261">Is Indexed</span></span>             | <span data-ttu-id="a65a9-262">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-262">False</span></span>                                                    |
| <span data-ttu-id="a65a9-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a65a9-263">In Global Catalog</span></span>      | <span data-ttu-id="a65a9-264">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-264">False</span></span>                                                    |
| <span data-ttu-id="a65a9-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a65a9-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="a65a9-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a65a9-266">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a65a9-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a65a9-267">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a65a9-268">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-269">Search-Flags</span></span>           | <span data-ttu-id="a65a9-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a65a9-270">0x00000000</span></span>                                               |
| <span data-ttu-id="a65a9-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-271">System-Flags</span></span>           | <span data-ttu-id="a65a9-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a65a9-272">0x00000010</span></span>                                               |
| <span data-ttu-id="a65a9-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a65a9-273">Classes used in</span></span>        | [<span data-ttu-id="a65a9-274">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a65a9-274">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a65a9-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a65a9-275">Windows Server 2012</span></span>



| <span data-ttu-id="a65a9-276">進入</span><span class="sxs-lookup"><span data-stu-id="a65a9-276">Entry</span></span> | <span data-ttu-id="a65a9-277">值</span><span class="sxs-lookup"><span data-stu-id="a65a9-277">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="a65a9-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a65a9-278">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="a65a9-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a65a9-279">MAPI-Id</span></span>                | <span data-ttu-id="a65a9-280">0x80C1</span><span class="sxs-lookup"><span data-stu-id="a65a9-280">0x80C1</span></span>                                                   |
| <span data-ttu-id="a65a9-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="a65a9-281">System-Only</span></span>            | <span data-ttu-id="a65a9-282">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-282">True</span></span>                                                     |
| <span data-ttu-id="a65a9-283">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a65a9-283">Is-Single-Valued</span></span>       | <span data-ttu-id="a65a9-284">對</span><span class="sxs-lookup"><span data-stu-id="a65a9-284">True</span></span>                                                     |
| <span data-ttu-id="a65a9-285">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a65a9-285">Is Indexed</span></span>             | <span data-ttu-id="a65a9-286">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-286">False</span></span>                                                    |
| <span data-ttu-id="a65a9-287">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a65a9-287">In Global Catalog</span></span>      | <span data-ttu-id="a65a9-288">否</span><span class="sxs-lookup"><span data-stu-id="a65a9-288">False</span></span>                                                    |
| <span data-ttu-id="a65a9-289">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a65a9-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="a65a9-290">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a65a9-290">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="a65a9-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a65a9-291">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a65a9-292">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="a65a9-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-293">Search-Flags</span></span>           | <span data-ttu-id="a65a9-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a65a9-294">0x00000000</span></span>                                               |
| <span data-ttu-id="a65a9-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a65a9-295">System-Flags</span></span>           | <span data-ttu-id="a65a9-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a65a9-296">0x00000010</span></span>                                               |
| <span data-ttu-id="a65a9-297">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a65a9-297">Classes used in</span></span>        | [<span data-ttu-id="a65a9-298">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="a65a9-298">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





