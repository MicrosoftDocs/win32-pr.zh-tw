---
title: 連結識別碼屬性
description: 表示屬性為連結屬性的整數。 偶數的整數是轉寄連結，而奇數整數是反向連結。
ms.assetid: 73851839-f70c-40c6-976c-0bf727083791
ms.tgt_platform: multiple
keywords:
- 連結識別碼屬性 AD 架構
- linkID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Link-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64ad1d26ce5510ac5643419ade46d0565df6487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509638"
---
# <a name="link-id-attribute"></a><span data-ttu-id="6e6dd-106">連結識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="6e6dd-106">Link-ID attribute</span></span>

<span data-ttu-id="6e6dd-107">表示屬性為連結屬性的整數。</span><span class="sxs-lookup"><span data-stu-id="6e6dd-107">An integer that indicates that the attribute is a linked attribute.</span></span> <span data-ttu-id="6e6dd-108">偶數的整數是轉寄連結，而奇數整數是反向連結。</span><span class="sxs-lookup"><span data-stu-id="6e6dd-108">An even integer is a forward link and an odd integer is a backward link.</span></span>



| <span data-ttu-id="6e6dd-109">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-109">Entry</span></span> | <span data-ttu-id="6e6dd-110">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6e6dd-111">CN</span><span class="sxs-lookup"><span data-stu-id="6e6dd-111">CN</span></span>                | <span data-ttu-id="6e6dd-112">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-112">Link-ID</span></span>                              |
| <span data-ttu-id="6e6dd-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6e6dd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6e6dd-114">linkID</span><span class="sxs-lookup"><span data-stu-id="6e6dd-114">linkID</span></span>                               |
| <span data-ttu-id="6e6dd-115">大小</span><span class="sxs-lookup"><span data-stu-id="6e6dd-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="6e6dd-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6e6dd-116">Update Privilege</span></span>  | <span data-ttu-id="6e6dd-117">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="6e6dd-117">Schema administrator</span></span>                 |
| <span data-ttu-id="6e6dd-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6e6dd-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6e6dd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-119">Attribute-Id</span></span>      | <span data-ttu-id="6e6dd-120">1.2.840.113556.1.2.50</span><span class="sxs-lookup"><span data-stu-id="6e6dd-120">1.2.840.113556.1.2.50</span></span>                |
| <span data-ttu-id="6e6dd-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6e6dd-121">System-Id-Guid</span></span>    | <span data-ttu-id="6e6dd-122">bf96799b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6e6dd-122">bf96799b-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6e6dd-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e6dd-123">Syntax</span></span>            | [<span data-ttu-id="6e6dd-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6e6dd-125">實作</span><span class="sxs-lookup"><span data-stu-id="6e6dd-125">Implementations</span></span>

-   [<span data-ttu-id="6e6dd-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6e6dd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6e6dd-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6e6dd-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6e6dd-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6e6dd-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6e6dd-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6e6dd-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e6dd-133">Windows 2000 Server</span></span>



| <span data-ttu-id="6e6dd-134">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-134">Entry</span></span> | <span data-ttu-id="6e6dd-135">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-135">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e6dd-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-136">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e6dd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-137">MAPI-Id</span></span>                | <span data-ttu-id="6e6dd-138">0x80C5</span><span class="sxs-lookup"><span data-stu-id="6e6dd-138">0x80C5</span></span>                                                   |
| <span data-ttu-id="6e6dd-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6dd-139">System-Only</span></span>            | <span data-ttu-id="6e6dd-140">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-140">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6dd-142">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-142">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e6dd-143">Is Indexed</span></span>             | <span data-ttu-id="6e6dd-144">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-144">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e6dd-145">In Global Catalog</span></span>      | <span data-ttu-id="6e6dd-146">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-146">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e6dd-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6dd-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e6dd-148">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e6dd-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6dd-149">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6dd-150">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-151">Search-Flags</span></span>           | <span data-ttu-id="6e6dd-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e6dd-152">0x00000000</span></span>                                               |
| <span data-ttu-id="6e6dd-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-153">System-Flags</span></span>           | <span data-ttu-id="6e6dd-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6dd-154">0x00000010</span></span>                                               |
| <span data-ttu-id="6e6dd-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e6dd-155">Classes used in</span></span>        | [<span data-ttu-id="6e6dd-156">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6e6dd-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e6dd-157">Windows Server 2003</span></span>



| <span data-ttu-id="6e6dd-158">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-158">Entry</span></span> | <span data-ttu-id="6e6dd-159">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-159">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e6dd-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-160">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e6dd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-161">MAPI-Id</span></span>                | <span data-ttu-id="6e6dd-162">0x80C5</span><span class="sxs-lookup"><span data-stu-id="6e6dd-162">0x80C5</span></span>                                                   |
| <span data-ttu-id="6e6dd-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6dd-163">System-Only</span></span>            | <span data-ttu-id="6e6dd-164">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-164">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6dd-166">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-166">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e6dd-167">Is Indexed</span></span>             | <span data-ttu-id="6e6dd-168">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-168">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e6dd-169">In Global Catalog</span></span>      | <span data-ttu-id="6e6dd-170">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-170">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e6dd-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6dd-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e6dd-172">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e6dd-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6dd-173">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6dd-174">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-175">Search-Flags</span></span>           | <span data-ttu-id="6e6dd-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e6dd-176">0x00000000</span></span>                                               |
| <span data-ttu-id="6e6dd-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-177">System-Flags</span></span>           | <span data-ttu-id="6e6dd-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6dd-178">0x00000010</span></span>                                               |
| <span data-ttu-id="6e6dd-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e6dd-179">Classes used in</span></span>        | [<span data-ttu-id="6e6dd-180">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6e6dd-181">亞當</span><span class="sxs-lookup"><span data-stu-id="6e6dd-181">ADAM</span></span>



| <span data-ttu-id="6e6dd-182">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-182">Entry</span></span> | <span data-ttu-id="6e6dd-183">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e6dd-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e6dd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-185">MAPI-Id</span></span>                | <span data-ttu-id="6e6dd-186">0x80C5</span><span class="sxs-lookup"><span data-stu-id="6e6dd-186">0x80C5</span></span>                                                   |
| <span data-ttu-id="6e6dd-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6dd-187">System-Only</span></span>            | <span data-ttu-id="6e6dd-188">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-188">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-189">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6dd-190">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-190">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e6dd-191">Is Indexed</span></span>             | <span data-ttu-id="6e6dd-192">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-192">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e6dd-193">In Global Catalog</span></span>      | <span data-ttu-id="6e6dd-194">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-194">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e6dd-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6dd-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e6dd-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e6dd-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6dd-197">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6dd-198">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-199">Search-Flags</span></span>           | <span data-ttu-id="6e6dd-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e6dd-200">0x00000000</span></span>                                               |
| <span data-ttu-id="6e6dd-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-201">System-Flags</span></span>           | <span data-ttu-id="6e6dd-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6dd-202">0x00000010</span></span>                                               |
| <span data-ttu-id="6e6dd-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e6dd-203">Classes used in</span></span>        | [<span data-ttu-id="6e6dd-204">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-204">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6e6dd-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6e6dd-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6e6dd-206">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-206">Entry</span></span> | <span data-ttu-id="6e6dd-207">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-207">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e6dd-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-208">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e6dd-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-209">MAPI-Id</span></span>                | <span data-ttu-id="6e6dd-210">0x80C5</span><span class="sxs-lookup"><span data-stu-id="6e6dd-210">0x80C5</span></span>                                                   |
| <span data-ttu-id="6e6dd-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6dd-211">System-Only</span></span>            | <span data-ttu-id="6e6dd-212">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-212">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6dd-214">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-214">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e6dd-215">Is Indexed</span></span>             | <span data-ttu-id="6e6dd-216">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-216">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e6dd-217">In Global Catalog</span></span>      | <span data-ttu-id="6e6dd-218">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-218">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e6dd-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6dd-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e6dd-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e6dd-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6dd-221">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6dd-222">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-223">Search-Flags</span></span>           | <span data-ttu-id="6e6dd-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e6dd-224">0x00000000</span></span>                                               |
| <span data-ttu-id="6e6dd-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-225">System-Flags</span></span>           | <span data-ttu-id="6e6dd-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6dd-226">0x00000010</span></span>                                               |
| <span data-ttu-id="6e6dd-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e6dd-227">Classes used in</span></span>        | [<span data-ttu-id="6e6dd-228">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6e6dd-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e6dd-229">Windows Server 2008</span></span>



| <span data-ttu-id="6e6dd-230">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-230">Entry</span></span> | <span data-ttu-id="6e6dd-231">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e6dd-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e6dd-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-233">MAPI-Id</span></span>                | <span data-ttu-id="6e6dd-234">0x80C5</span><span class="sxs-lookup"><span data-stu-id="6e6dd-234">0x80C5</span></span>                                                   |
| <span data-ttu-id="6e6dd-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6dd-235">System-Only</span></span>            | <span data-ttu-id="6e6dd-236">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-236">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-237">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6dd-238">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-238">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e6dd-239">Is Indexed</span></span>             | <span data-ttu-id="6e6dd-240">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-240">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e6dd-241">In Global Catalog</span></span>      | <span data-ttu-id="6e6dd-242">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-242">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e6dd-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6dd-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e6dd-244">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e6dd-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6dd-245">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6dd-246">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-247">Search-Flags</span></span>           | <span data-ttu-id="6e6dd-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e6dd-248">0x00000000</span></span>                                               |
| <span data-ttu-id="6e6dd-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-249">System-Flags</span></span>           | <span data-ttu-id="6e6dd-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6dd-250">0x00000010</span></span>                                               |
| <span data-ttu-id="6e6dd-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e6dd-251">Classes used in</span></span>        | [<span data-ttu-id="6e6dd-252">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-252">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6e6dd-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e6dd-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6e6dd-254">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-254">Entry</span></span> | <span data-ttu-id="6e6dd-255">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-255">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e6dd-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-256">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e6dd-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-257">MAPI-Id</span></span>                | <span data-ttu-id="6e6dd-258">0x80C5</span><span class="sxs-lookup"><span data-stu-id="6e6dd-258">0x80C5</span></span>                                                   |
| <span data-ttu-id="6e6dd-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6dd-259">System-Only</span></span>            | <span data-ttu-id="6e6dd-260">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-260">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-261">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6dd-262">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-262">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e6dd-263">Is Indexed</span></span>             | <span data-ttu-id="6e6dd-264">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-264">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e6dd-265">In Global Catalog</span></span>      | <span data-ttu-id="6e6dd-266">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-266">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e6dd-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6dd-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e6dd-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e6dd-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6dd-269">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6dd-270">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-271">Search-Flags</span></span>           | <span data-ttu-id="6e6dd-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e6dd-272">0x00000000</span></span>                                               |
| <span data-ttu-id="6e6dd-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-273">System-Flags</span></span>           | <span data-ttu-id="6e6dd-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6dd-274">0x00000010</span></span>                                               |
| <span data-ttu-id="6e6dd-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e6dd-275">Classes used in</span></span>        | [<span data-ttu-id="6e6dd-276">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-276">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6e6dd-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e6dd-277">Windows Server 2012</span></span>



| <span data-ttu-id="6e6dd-278">進入</span><span class="sxs-lookup"><span data-stu-id="6e6dd-278">Entry</span></span> | <span data-ttu-id="6e6dd-279">值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-279">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e6dd-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e6dd-280">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e6dd-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6dd-281">MAPI-Id</span></span>                | <span data-ttu-id="6e6dd-282">0x80C5</span><span class="sxs-lookup"><span data-stu-id="6e6dd-282">0x80C5</span></span>                                                   |
| <span data-ttu-id="6e6dd-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6dd-283">System-Only</span></span>            | <span data-ttu-id="6e6dd-284">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-284">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e6dd-285">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6dd-286">對</span><span class="sxs-lookup"><span data-stu-id="6e6dd-286">True</span></span>                                                     |
| <span data-ttu-id="6e6dd-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e6dd-287">Is Indexed</span></span>             | <span data-ttu-id="6e6dd-288">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-288">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e6dd-289">In Global Catalog</span></span>      | <span data-ttu-id="6e6dd-290">否</span><span class="sxs-lookup"><span data-stu-id="6e6dd-290">False</span></span>                                                    |
| <span data-ttu-id="6e6dd-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e6dd-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6dd-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e6dd-292">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e6dd-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6dd-293">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6dd-294">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="6e6dd-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-295">Search-Flags</span></span>           | <span data-ttu-id="6e6dd-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e6dd-296">0x00000000</span></span>                                               |
| <span data-ttu-id="6e6dd-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6dd-297">System-Flags</span></span>           | <span data-ttu-id="6e6dd-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6dd-298">0x00000010</span></span>                                               |
| <span data-ttu-id="6e6dd-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e6dd-299">Classes used in</span></span>        | [<span data-ttu-id="6e6dd-300">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="6e6dd-300">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





