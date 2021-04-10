---
title: 物件類別類別目錄屬性
description: 這個屬性包含類別類型，例如 abstract、輔助或結構化。
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- 物件類別類別目錄屬性 AD 架構
- objectClassCategory 屬性 AD 架構
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935364"
---
# <a name="object-class-category-attribute"></a><span data-ttu-id="30482-105">物件類別類別目錄屬性</span><span class="sxs-lookup"><span data-stu-id="30482-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="30482-106">這個屬性包含類別類型，例如 abstract、輔助或結構化。</span><span class="sxs-lookup"><span data-stu-id="30482-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="30482-107">進入</span><span class="sxs-lookup"><span data-stu-id="30482-107">Entry</span></span> | <span data-ttu-id="30482-108">值</span><span class="sxs-lookup"><span data-stu-id="30482-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="30482-109">CN</span><span class="sxs-lookup"><span data-stu-id="30482-109">CN</span></span>                | <span data-ttu-id="30482-110">物件類別-類別目錄</span><span class="sxs-lookup"><span data-stu-id="30482-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="30482-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="30482-111">Ldap-Display-Name</span></span> | <span data-ttu-id="30482-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="30482-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="30482-113">大小</span><span class="sxs-lookup"><span data-stu-id="30482-113">Size</span></span>              | <span data-ttu-id="30482-114">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="30482-114">4 bytes.</span></span> <span data-ttu-id="30482-115">結構1、抽象2、輔助3。</span><span class="sxs-lookup"><span data-stu-id="30482-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="30482-116">不應使用類別88、0。</span><span class="sxs-lookup"><span data-stu-id="30482-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="30482-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="30482-117">Update Privilege</span></span>  | <span data-ttu-id="30482-118">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="30482-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="30482-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="30482-119">Update Frequency</span></span>  | <span data-ttu-id="30482-120">此值永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="30482-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="30482-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="30482-121">Attribute-Id</span></span>      | <span data-ttu-id="30482-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="30482-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="30482-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="30482-123">System-Id-Guid</span></span>    | <span data-ttu-id="30482-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="30482-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="30482-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="30482-125">Syntax</span></span>            | [<span data-ttu-id="30482-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="30482-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="30482-127">實作</span><span class="sxs-lookup"><span data-stu-id="30482-127">Implementations</span></span>

-   [<span data-ttu-id="30482-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="30482-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="30482-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="30482-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="30482-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="30482-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="30482-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="30482-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="30482-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="30482-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="30482-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="30482-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="30482-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="30482-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="30482-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="30482-135">Windows 2000 Server</span></span>



| <span data-ttu-id="30482-136">進入</span><span class="sxs-lookup"><span data-stu-id="30482-136">Entry</span></span> | <span data-ttu-id="30482-137">值</span><span class="sxs-lookup"><span data-stu-id="30482-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="30482-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="30482-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="30482-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30482-139">MAPI-Id</span></span>                | <span data-ttu-id="30482-140">0x80F6</span><span class="sxs-lookup"><span data-stu-id="30482-140">0x80F6</span></span>                                           |
| <span data-ttu-id="30482-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="30482-141">System-Only</span></span>            | <span data-ttu-id="30482-142">對</span><span class="sxs-lookup"><span data-stu-id="30482-142">True</span></span>                                             |
| <span data-ttu-id="30482-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="30482-143">Is-Single-Valued</span></span>       | <span data-ttu-id="30482-144">對</span><span class="sxs-lookup"><span data-stu-id="30482-144">True</span></span>                                             |
| <span data-ttu-id="30482-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="30482-145">Is Indexed</span></span>             | <span data-ttu-id="30482-146">否</span><span class="sxs-lookup"><span data-stu-id="30482-146">False</span></span>                                            |
| <span data-ttu-id="30482-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="30482-147">In Global Catalog</span></span>      | <span data-ttu-id="30482-148">否</span><span class="sxs-lookup"><span data-stu-id="30482-148">False</span></span>                                            |
| <span data-ttu-id="30482-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="30482-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="30482-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="30482-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="30482-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30482-151">Range-Lower</span></span>            | <span data-ttu-id="30482-152">0</span><span class="sxs-lookup"><span data-stu-id="30482-152">0</span></span>                                                |
| <span data-ttu-id="30482-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30482-153">Range-Upper</span></span>            | <span data-ttu-id="30482-154">3</span><span class="sxs-lookup"><span data-stu-id="30482-154">3</span></span>                                                |
| <span data-ttu-id="30482-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-155">Search-Flags</span></span>           | <span data-ttu-id="30482-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30482-156">0x00000000</span></span>                                       |
| <span data-ttu-id="30482-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-157">System-Flags</span></span>           | <span data-ttu-id="30482-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30482-158">0x00000010</span></span>                                       |
| <span data-ttu-id="30482-159">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="30482-159">Classes used in</span></span>        | [<span data-ttu-id="30482-160">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="30482-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="30482-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30482-161">Windows Server 2003</span></span>



| <span data-ttu-id="30482-162">進入</span><span class="sxs-lookup"><span data-stu-id="30482-162">Entry</span></span> | <span data-ttu-id="30482-163">值</span><span class="sxs-lookup"><span data-stu-id="30482-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="30482-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="30482-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="30482-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30482-165">MAPI-Id</span></span>                | <span data-ttu-id="30482-166">0x80F6</span><span class="sxs-lookup"><span data-stu-id="30482-166">0x80F6</span></span>                                           |
| <span data-ttu-id="30482-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="30482-167">System-Only</span></span>            | <span data-ttu-id="30482-168">對</span><span class="sxs-lookup"><span data-stu-id="30482-168">True</span></span>                                             |
| <span data-ttu-id="30482-169">是-單一值</span><span class="sxs-lookup"><span data-stu-id="30482-169">Is-Single-Valued</span></span>       | <span data-ttu-id="30482-170">對</span><span class="sxs-lookup"><span data-stu-id="30482-170">True</span></span>                                             |
| <span data-ttu-id="30482-171">已編制索引</span><span class="sxs-lookup"><span data-stu-id="30482-171">Is Indexed</span></span>             | <span data-ttu-id="30482-172">否</span><span class="sxs-lookup"><span data-stu-id="30482-172">False</span></span>                                            |
| <span data-ttu-id="30482-173">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="30482-173">In Global Catalog</span></span>      | <span data-ttu-id="30482-174">否</span><span class="sxs-lookup"><span data-stu-id="30482-174">False</span></span>                                            |
| <span data-ttu-id="30482-175">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="30482-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="30482-176">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="30482-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="30482-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30482-177">Range-Lower</span></span>            | <span data-ttu-id="30482-178">0</span><span class="sxs-lookup"><span data-stu-id="30482-178">0</span></span>                                                |
| <span data-ttu-id="30482-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30482-179">Range-Upper</span></span>            | <span data-ttu-id="30482-180">3</span><span class="sxs-lookup"><span data-stu-id="30482-180">3</span></span>                                                |
| <span data-ttu-id="30482-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-181">Search-Flags</span></span>           | <span data-ttu-id="30482-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30482-182">0x00000000</span></span>                                       |
| <span data-ttu-id="30482-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-183">System-Flags</span></span>           | <span data-ttu-id="30482-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30482-184">0x00000010</span></span>                                       |
| <span data-ttu-id="30482-185">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="30482-185">Classes used in</span></span>        | [<span data-ttu-id="30482-186">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="30482-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="30482-187">亞當</span><span class="sxs-lookup"><span data-stu-id="30482-187">ADAM</span></span>



| <span data-ttu-id="30482-188">進入</span><span class="sxs-lookup"><span data-stu-id="30482-188">Entry</span></span> | <span data-ttu-id="30482-189">值</span><span class="sxs-lookup"><span data-stu-id="30482-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="30482-190">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="30482-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="30482-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30482-191">MAPI-Id</span></span>                | <span data-ttu-id="30482-192">0x80F6</span><span class="sxs-lookup"><span data-stu-id="30482-192">0x80F6</span></span>                                           |
| <span data-ttu-id="30482-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="30482-193">System-Only</span></span>            | <span data-ttu-id="30482-194">對</span><span class="sxs-lookup"><span data-stu-id="30482-194">True</span></span>                                             |
| <span data-ttu-id="30482-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="30482-195">Is-Single-Valued</span></span>       | <span data-ttu-id="30482-196">對</span><span class="sxs-lookup"><span data-stu-id="30482-196">True</span></span>                                             |
| <span data-ttu-id="30482-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="30482-197">Is Indexed</span></span>             | <span data-ttu-id="30482-198">否</span><span class="sxs-lookup"><span data-stu-id="30482-198">False</span></span>                                            |
| <span data-ttu-id="30482-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="30482-199">In Global Catalog</span></span>      | <span data-ttu-id="30482-200">否</span><span class="sxs-lookup"><span data-stu-id="30482-200">False</span></span>                                            |
| <span data-ttu-id="30482-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="30482-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="30482-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="30482-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="30482-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30482-203">Range-Lower</span></span>            | <span data-ttu-id="30482-204">0</span><span class="sxs-lookup"><span data-stu-id="30482-204">0</span></span>                                                |
| <span data-ttu-id="30482-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30482-205">Range-Upper</span></span>            | <span data-ttu-id="30482-206">3</span><span class="sxs-lookup"><span data-stu-id="30482-206">3</span></span>                                                |
| <span data-ttu-id="30482-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-207">Search-Flags</span></span>           | <span data-ttu-id="30482-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30482-208">0x00000000</span></span>                                       |
| <span data-ttu-id="30482-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-209">System-Flags</span></span>           | <span data-ttu-id="30482-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30482-210">0x00000010</span></span>                                       |
| <span data-ttu-id="30482-211">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="30482-211">Classes used in</span></span>        | [<span data-ttu-id="30482-212">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="30482-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="30482-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="30482-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="30482-214">進入</span><span class="sxs-lookup"><span data-stu-id="30482-214">Entry</span></span> | <span data-ttu-id="30482-215">值</span><span class="sxs-lookup"><span data-stu-id="30482-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="30482-216">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="30482-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="30482-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30482-217">MAPI-Id</span></span>                | <span data-ttu-id="30482-218">0x80F6</span><span class="sxs-lookup"><span data-stu-id="30482-218">0x80F6</span></span>                                           |
| <span data-ttu-id="30482-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="30482-219">System-Only</span></span>            | <span data-ttu-id="30482-220">對</span><span class="sxs-lookup"><span data-stu-id="30482-220">True</span></span>                                             |
| <span data-ttu-id="30482-221">是-單一值</span><span class="sxs-lookup"><span data-stu-id="30482-221">Is-Single-Valued</span></span>       | <span data-ttu-id="30482-222">對</span><span class="sxs-lookup"><span data-stu-id="30482-222">True</span></span>                                             |
| <span data-ttu-id="30482-223">已編制索引</span><span class="sxs-lookup"><span data-stu-id="30482-223">Is Indexed</span></span>             | <span data-ttu-id="30482-224">否</span><span class="sxs-lookup"><span data-stu-id="30482-224">False</span></span>                                            |
| <span data-ttu-id="30482-225">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="30482-225">In Global Catalog</span></span>      | <span data-ttu-id="30482-226">否</span><span class="sxs-lookup"><span data-stu-id="30482-226">False</span></span>                                            |
| <span data-ttu-id="30482-227">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="30482-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="30482-228">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="30482-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="30482-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30482-229">Range-Lower</span></span>            | <span data-ttu-id="30482-230">0</span><span class="sxs-lookup"><span data-stu-id="30482-230">0</span></span>                                                |
| <span data-ttu-id="30482-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30482-231">Range-Upper</span></span>            | <span data-ttu-id="30482-232">3</span><span class="sxs-lookup"><span data-stu-id="30482-232">3</span></span>                                                |
| <span data-ttu-id="30482-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-233">Search-Flags</span></span>           | <span data-ttu-id="30482-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30482-234">0x00000000</span></span>                                       |
| <span data-ttu-id="30482-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-235">System-Flags</span></span>           | <span data-ttu-id="30482-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30482-236">0x00000010</span></span>                                       |
| <span data-ttu-id="30482-237">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="30482-237">Classes used in</span></span>        | [<span data-ttu-id="30482-238">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="30482-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="30482-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30482-239">Windows Server 2008</span></span>



| <span data-ttu-id="30482-240">進入</span><span class="sxs-lookup"><span data-stu-id="30482-240">Entry</span></span> | <span data-ttu-id="30482-241">值</span><span class="sxs-lookup"><span data-stu-id="30482-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="30482-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="30482-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="30482-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30482-243">MAPI-Id</span></span>                | <span data-ttu-id="30482-244">0x80F6</span><span class="sxs-lookup"><span data-stu-id="30482-244">0x80F6</span></span>                                           |
| <span data-ttu-id="30482-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="30482-245">System-Only</span></span>            | <span data-ttu-id="30482-246">對</span><span class="sxs-lookup"><span data-stu-id="30482-246">True</span></span>                                             |
| <span data-ttu-id="30482-247">是-單一值</span><span class="sxs-lookup"><span data-stu-id="30482-247">Is-Single-Valued</span></span>       | <span data-ttu-id="30482-248">對</span><span class="sxs-lookup"><span data-stu-id="30482-248">True</span></span>                                             |
| <span data-ttu-id="30482-249">已編制索引</span><span class="sxs-lookup"><span data-stu-id="30482-249">Is Indexed</span></span>             | <span data-ttu-id="30482-250">否</span><span class="sxs-lookup"><span data-stu-id="30482-250">False</span></span>                                            |
| <span data-ttu-id="30482-251">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="30482-251">In Global Catalog</span></span>      | <span data-ttu-id="30482-252">否</span><span class="sxs-lookup"><span data-stu-id="30482-252">False</span></span>                                            |
| <span data-ttu-id="30482-253">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="30482-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="30482-254">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="30482-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="30482-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30482-255">Range-Lower</span></span>            | <span data-ttu-id="30482-256">0</span><span class="sxs-lookup"><span data-stu-id="30482-256">0</span></span>                                                |
| <span data-ttu-id="30482-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30482-257">Range-Upper</span></span>            | <span data-ttu-id="30482-258">3</span><span class="sxs-lookup"><span data-stu-id="30482-258">3</span></span>                                                |
| <span data-ttu-id="30482-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-259">Search-Flags</span></span>           | <span data-ttu-id="30482-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30482-260">0x00000000</span></span>                                       |
| <span data-ttu-id="30482-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-261">System-Flags</span></span>           | <span data-ttu-id="30482-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30482-262">0x00000010</span></span>                                       |
| <span data-ttu-id="30482-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="30482-263">Classes used in</span></span>        | [<span data-ttu-id="30482-264">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="30482-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="30482-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30482-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="30482-266">進入</span><span class="sxs-lookup"><span data-stu-id="30482-266">Entry</span></span> | <span data-ttu-id="30482-267">值</span><span class="sxs-lookup"><span data-stu-id="30482-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="30482-268">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="30482-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="30482-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30482-269">MAPI-Id</span></span>                | <span data-ttu-id="30482-270">0x80F6</span><span class="sxs-lookup"><span data-stu-id="30482-270">0x80F6</span></span>                                           |
| <span data-ttu-id="30482-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="30482-271">System-Only</span></span>            | <span data-ttu-id="30482-272">對</span><span class="sxs-lookup"><span data-stu-id="30482-272">True</span></span>                                             |
| <span data-ttu-id="30482-273">是-單一值</span><span class="sxs-lookup"><span data-stu-id="30482-273">Is-Single-Valued</span></span>       | <span data-ttu-id="30482-274">對</span><span class="sxs-lookup"><span data-stu-id="30482-274">True</span></span>                                             |
| <span data-ttu-id="30482-275">已編制索引</span><span class="sxs-lookup"><span data-stu-id="30482-275">Is Indexed</span></span>             | <span data-ttu-id="30482-276">否</span><span class="sxs-lookup"><span data-stu-id="30482-276">False</span></span>                                            |
| <span data-ttu-id="30482-277">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="30482-277">In Global Catalog</span></span>      | <span data-ttu-id="30482-278">否</span><span class="sxs-lookup"><span data-stu-id="30482-278">False</span></span>                                            |
| <span data-ttu-id="30482-279">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="30482-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="30482-280">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="30482-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="30482-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30482-281">Range-Lower</span></span>            | <span data-ttu-id="30482-282">0</span><span class="sxs-lookup"><span data-stu-id="30482-282">0</span></span>                                                |
| <span data-ttu-id="30482-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30482-283">Range-Upper</span></span>            | <span data-ttu-id="30482-284">3</span><span class="sxs-lookup"><span data-stu-id="30482-284">3</span></span>                                                |
| <span data-ttu-id="30482-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-285">Search-Flags</span></span>           | <span data-ttu-id="30482-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30482-286">0x00000000</span></span>                                       |
| <span data-ttu-id="30482-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-287">System-Flags</span></span>           | <span data-ttu-id="30482-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30482-288">0x00000010</span></span>                                       |
| <span data-ttu-id="30482-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="30482-289">Classes used in</span></span>        | [<span data-ttu-id="30482-290">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="30482-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="30482-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30482-291">Windows Server 2012</span></span>



| <span data-ttu-id="30482-292">進入</span><span class="sxs-lookup"><span data-stu-id="30482-292">Entry</span></span> | <span data-ttu-id="30482-293">值</span><span class="sxs-lookup"><span data-stu-id="30482-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="30482-294">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="30482-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="30482-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30482-295">MAPI-Id</span></span>                | <span data-ttu-id="30482-296">0x80F6</span><span class="sxs-lookup"><span data-stu-id="30482-296">0x80F6</span></span>                                           |
| <span data-ttu-id="30482-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="30482-297">System-Only</span></span>            | <span data-ttu-id="30482-298">對</span><span class="sxs-lookup"><span data-stu-id="30482-298">True</span></span>                                             |
| <span data-ttu-id="30482-299">是-單一值</span><span class="sxs-lookup"><span data-stu-id="30482-299">Is-Single-Valued</span></span>       | <span data-ttu-id="30482-300">對</span><span class="sxs-lookup"><span data-stu-id="30482-300">True</span></span>                                             |
| <span data-ttu-id="30482-301">已編制索引</span><span class="sxs-lookup"><span data-stu-id="30482-301">Is Indexed</span></span>             | <span data-ttu-id="30482-302">否</span><span class="sxs-lookup"><span data-stu-id="30482-302">False</span></span>                                            |
| <span data-ttu-id="30482-303">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="30482-303">In Global Catalog</span></span>      | <span data-ttu-id="30482-304">否</span><span class="sxs-lookup"><span data-stu-id="30482-304">False</span></span>                                            |
| <span data-ttu-id="30482-305">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="30482-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="30482-306">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="30482-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="30482-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30482-307">Range-Lower</span></span>            | <span data-ttu-id="30482-308">0</span><span class="sxs-lookup"><span data-stu-id="30482-308">0</span></span>                                                |
| <span data-ttu-id="30482-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30482-309">Range-Upper</span></span>            | <span data-ttu-id="30482-310">3</span><span class="sxs-lookup"><span data-stu-id="30482-310">3</span></span>                                                |
| <span data-ttu-id="30482-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-311">Search-Flags</span></span>           | <span data-ttu-id="30482-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30482-312">0x00000000</span></span>                                       |
| <span data-ttu-id="30482-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30482-313">System-Flags</span></span>           | <span data-ttu-id="30482-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30482-314">0x00000010</span></span>                                       |
| <span data-ttu-id="30482-315">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="30482-315">Classes used in</span></span>        | [<span data-ttu-id="30482-316">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="30482-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





