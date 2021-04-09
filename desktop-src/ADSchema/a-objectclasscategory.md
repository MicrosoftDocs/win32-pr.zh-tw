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
# <a name="object-class-category-attribute"></a><span data-ttu-id="be5f4-105">物件類別類別目錄屬性</span><span class="sxs-lookup"><span data-stu-id="be5f4-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="be5f4-106">這個屬性包含類別類型，例如 abstract、輔助或結構化。</span><span class="sxs-lookup"><span data-stu-id="be5f4-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="be5f4-107">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-107">Entry</span></span> | <span data-ttu-id="be5f4-108">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="be5f4-109">CN</span><span class="sxs-lookup"><span data-stu-id="be5f4-109">CN</span></span>                | <span data-ttu-id="be5f4-110">物件類別-類別目錄</span><span class="sxs-lookup"><span data-stu-id="be5f4-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="be5f4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="be5f4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="be5f4-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="be5f4-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="be5f4-113">大小</span><span class="sxs-lookup"><span data-stu-id="be5f4-113">Size</span></span>              | <span data-ttu-id="be5f4-114">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="be5f4-114">4 bytes.</span></span> <span data-ttu-id="be5f4-115">結構1、抽象2、輔助3。</span><span class="sxs-lookup"><span data-stu-id="be5f4-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="be5f4-116">不應使用類別88、0。</span><span class="sxs-lookup"><span data-stu-id="be5f4-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="be5f4-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="be5f4-117">Update Privilege</span></span>  | <span data-ttu-id="be5f4-118">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="be5f4-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="be5f4-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="be5f4-119">Update Frequency</span></span>  | <span data-ttu-id="be5f4-120">此值永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="be5f4-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="be5f4-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-121">Attribute-Id</span></span>      | <span data-ttu-id="be5f4-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="be5f4-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="be5f4-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="be5f4-123">System-Id-Guid</span></span>    | <span data-ttu-id="be5f4-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="be5f4-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="be5f4-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="be5f4-125">Syntax</span></span>            | [<span data-ttu-id="be5f4-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="be5f4-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="be5f4-127">實作</span><span class="sxs-lookup"><span data-stu-id="be5f4-127">Implementations</span></span>

-   [<span data-ttu-id="be5f4-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="be5f4-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="be5f4-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="be5f4-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="be5f4-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="be5f4-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="be5f4-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be5f4-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be5f4-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be5f4-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be5f4-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be5f4-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be5f4-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be5f4-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="be5f4-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be5f4-135">Windows 2000 Server</span></span>



| <span data-ttu-id="be5f4-136">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-136">Entry</span></span> | <span data-ttu-id="be5f4-137">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be5f4-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be5f4-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be5f4-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-139">MAPI-Id</span></span>                | <span data-ttu-id="be5f4-140">0x80F6</span><span class="sxs-lookup"><span data-stu-id="be5f4-140">0x80F6</span></span>                                           |
| <span data-ttu-id="be5f4-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="be5f4-141">System-Only</span></span>            | <span data-ttu-id="be5f4-142">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-142">True</span></span>                                             |
| <span data-ttu-id="be5f4-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be5f4-143">Is-Single-Valued</span></span>       | <span data-ttu-id="be5f4-144">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-144">True</span></span>                                             |
| <span data-ttu-id="be5f4-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be5f4-145">Is Indexed</span></span>             | <span data-ttu-id="be5f4-146">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-146">False</span></span>                                            |
| <span data-ttu-id="be5f4-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be5f4-147">In Global Catalog</span></span>      | <span data-ttu-id="be5f4-148">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-148">False</span></span>                                            |
| <span data-ttu-id="be5f4-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be5f4-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="be5f4-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be5f4-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be5f4-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be5f4-151">Range-Lower</span></span>            | <span data-ttu-id="be5f4-152">0</span><span class="sxs-lookup"><span data-stu-id="be5f4-152">0</span></span>                                                |
| <span data-ttu-id="be5f4-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be5f4-153">Range-Upper</span></span>            | <span data-ttu-id="be5f4-154">3</span><span class="sxs-lookup"><span data-stu-id="be5f4-154">3</span></span>                                                |
| <span data-ttu-id="be5f4-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-155">Search-Flags</span></span>           | <span data-ttu-id="be5f4-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be5f4-156">0x00000000</span></span>                                       |
| <span data-ttu-id="be5f4-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-157">System-Flags</span></span>           | <span data-ttu-id="be5f4-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be5f4-158">0x00000010</span></span>                                       |
| <span data-ttu-id="be5f4-159">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be5f4-159">Classes used in</span></span>        | [<span data-ttu-id="be5f4-160">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="be5f4-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="be5f4-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be5f4-161">Windows Server 2003</span></span>



| <span data-ttu-id="be5f4-162">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-162">Entry</span></span> | <span data-ttu-id="be5f4-163">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be5f4-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be5f4-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be5f4-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-165">MAPI-Id</span></span>                | <span data-ttu-id="be5f4-166">0x80F6</span><span class="sxs-lookup"><span data-stu-id="be5f4-166">0x80F6</span></span>                                           |
| <span data-ttu-id="be5f4-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="be5f4-167">System-Only</span></span>            | <span data-ttu-id="be5f4-168">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-168">True</span></span>                                             |
| <span data-ttu-id="be5f4-169">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be5f4-169">Is-Single-Valued</span></span>       | <span data-ttu-id="be5f4-170">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-170">True</span></span>                                             |
| <span data-ttu-id="be5f4-171">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be5f4-171">Is Indexed</span></span>             | <span data-ttu-id="be5f4-172">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-172">False</span></span>                                            |
| <span data-ttu-id="be5f4-173">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be5f4-173">In Global Catalog</span></span>      | <span data-ttu-id="be5f4-174">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-174">False</span></span>                                            |
| <span data-ttu-id="be5f4-175">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be5f4-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="be5f4-176">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be5f4-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be5f4-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be5f4-177">Range-Lower</span></span>            | <span data-ttu-id="be5f4-178">0</span><span class="sxs-lookup"><span data-stu-id="be5f4-178">0</span></span>                                                |
| <span data-ttu-id="be5f4-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be5f4-179">Range-Upper</span></span>            | <span data-ttu-id="be5f4-180">3</span><span class="sxs-lookup"><span data-stu-id="be5f4-180">3</span></span>                                                |
| <span data-ttu-id="be5f4-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-181">Search-Flags</span></span>           | <span data-ttu-id="be5f4-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be5f4-182">0x00000000</span></span>                                       |
| <span data-ttu-id="be5f4-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-183">System-Flags</span></span>           | <span data-ttu-id="be5f4-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be5f4-184">0x00000010</span></span>                                       |
| <span data-ttu-id="be5f4-185">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be5f4-185">Classes used in</span></span>        | [<span data-ttu-id="be5f4-186">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="be5f4-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="be5f4-187">亞當</span><span class="sxs-lookup"><span data-stu-id="be5f4-187">ADAM</span></span>



| <span data-ttu-id="be5f4-188">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-188">Entry</span></span> | <span data-ttu-id="be5f4-189">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be5f4-190">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be5f4-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be5f4-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-191">MAPI-Id</span></span>                | <span data-ttu-id="be5f4-192">0x80F6</span><span class="sxs-lookup"><span data-stu-id="be5f4-192">0x80F6</span></span>                                           |
| <span data-ttu-id="be5f4-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="be5f4-193">System-Only</span></span>            | <span data-ttu-id="be5f4-194">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-194">True</span></span>                                             |
| <span data-ttu-id="be5f4-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be5f4-195">Is-Single-Valued</span></span>       | <span data-ttu-id="be5f4-196">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-196">True</span></span>                                             |
| <span data-ttu-id="be5f4-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be5f4-197">Is Indexed</span></span>             | <span data-ttu-id="be5f4-198">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-198">False</span></span>                                            |
| <span data-ttu-id="be5f4-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be5f4-199">In Global Catalog</span></span>      | <span data-ttu-id="be5f4-200">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-200">False</span></span>                                            |
| <span data-ttu-id="be5f4-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be5f4-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="be5f4-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be5f4-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be5f4-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be5f4-203">Range-Lower</span></span>            | <span data-ttu-id="be5f4-204">0</span><span class="sxs-lookup"><span data-stu-id="be5f4-204">0</span></span>                                                |
| <span data-ttu-id="be5f4-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be5f4-205">Range-Upper</span></span>            | <span data-ttu-id="be5f4-206">3</span><span class="sxs-lookup"><span data-stu-id="be5f4-206">3</span></span>                                                |
| <span data-ttu-id="be5f4-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-207">Search-Flags</span></span>           | <span data-ttu-id="be5f4-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be5f4-208">0x00000000</span></span>                                       |
| <span data-ttu-id="be5f4-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-209">System-Flags</span></span>           | <span data-ttu-id="be5f4-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be5f4-210">0x00000010</span></span>                                       |
| <span data-ttu-id="be5f4-211">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be5f4-211">Classes used in</span></span>        | [<span data-ttu-id="be5f4-212">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="be5f4-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="be5f4-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be5f4-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be5f4-214">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-214">Entry</span></span> | <span data-ttu-id="be5f4-215">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be5f4-216">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be5f4-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be5f4-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-217">MAPI-Id</span></span>                | <span data-ttu-id="be5f4-218">0x80F6</span><span class="sxs-lookup"><span data-stu-id="be5f4-218">0x80F6</span></span>                                           |
| <span data-ttu-id="be5f4-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="be5f4-219">System-Only</span></span>            | <span data-ttu-id="be5f4-220">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-220">True</span></span>                                             |
| <span data-ttu-id="be5f4-221">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be5f4-221">Is-Single-Valued</span></span>       | <span data-ttu-id="be5f4-222">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-222">True</span></span>                                             |
| <span data-ttu-id="be5f4-223">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be5f4-223">Is Indexed</span></span>             | <span data-ttu-id="be5f4-224">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-224">False</span></span>                                            |
| <span data-ttu-id="be5f4-225">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be5f4-225">In Global Catalog</span></span>      | <span data-ttu-id="be5f4-226">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-226">False</span></span>                                            |
| <span data-ttu-id="be5f4-227">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be5f4-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="be5f4-228">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be5f4-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be5f4-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be5f4-229">Range-Lower</span></span>            | <span data-ttu-id="be5f4-230">0</span><span class="sxs-lookup"><span data-stu-id="be5f4-230">0</span></span>                                                |
| <span data-ttu-id="be5f4-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be5f4-231">Range-Upper</span></span>            | <span data-ttu-id="be5f4-232">3</span><span class="sxs-lookup"><span data-stu-id="be5f4-232">3</span></span>                                                |
| <span data-ttu-id="be5f4-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-233">Search-Flags</span></span>           | <span data-ttu-id="be5f4-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be5f4-234">0x00000000</span></span>                                       |
| <span data-ttu-id="be5f4-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-235">System-Flags</span></span>           | <span data-ttu-id="be5f4-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be5f4-236">0x00000010</span></span>                                       |
| <span data-ttu-id="be5f4-237">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be5f4-237">Classes used in</span></span>        | [<span data-ttu-id="be5f4-238">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="be5f4-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be5f4-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be5f4-239">Windows Server 2008</span></span>



| <span data-ttu-id="be5f4-240">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-240">Entry</span></span> | <span data-ttu-id="be5f4-241">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be5f4-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be5f4-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be5f4-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-243">MAPI-Id</span></span>                | <span data-ttu-id="be5f4-244">0x80F6</span><span class="sxs-lookup"><span data-stu-id="be5f4-244">0x80F6</span></span>                                           |
| <span data-ttu-id="be5f4-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="be5f4-245">System-Only</span></span>            | <span data-ttu-id="be5f4-246">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-246">True</span></span>                                             |
| <span data-ttu-id="be5f4-247">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be5f4-247">Is-Single-Valued</span></span>       | <span data-ttu-id="be5f4-248">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-248">True</span></span>                                             |
| <span data-ttu-id="be5f4-249">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be5f4-249">Is Indexed</span></span>             | <span data-ttu-id="be5f4-250">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-250">False</span></span>                                            |
| <span data-ttu-id="be5f4-251">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be5f4-251">In Global Catalog</span></span>      | <span data-ttu-id="be5f4-252">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-252">False</span></span>                                            |
| <span data-ttu-id="be5f4-253">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be5f4-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="be5f4-254">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be5f4-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be5f4-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be5f4-255">Range-Lower</span></span>            | <span data-ttu-id="be5f4-256">0</span><span class="sxs-lookup"><span data-stu-id="be5f4-256">0</span></span>                                                |
| <span data-ttu-id="be5f4-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be5f4-257">Range-Upper</span></span>            | <span data-ttu-id="be5f4-258">3</span><span class="sxs-lookup"><span data-stu-id="be5f4-258">3</span></span>                                                |
| <span data-ttu-id="be5f4-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-259">Search-Flags</span></span>           | <span data-ttu-id="be5f4-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be5f4-260">0x00000000</span></span>                                       |
| <span data-ttu-id="be5f4-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-261">System-Flags</span></span>           | <span data-ttu-id="be5f4-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be5f4-262">0x00000010</span></span>                                       |
| <span data-ttu-id="be5f4-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be5f4-263">Classes used in</span></span>        | [<span data-ttu-id="be5f4-264">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="be5f4-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be5f4-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be5f4-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be5f4-266">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-266">Entry</span></span> | <span data-ttu-id="be5f4-267">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be5f4-268">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be5f4-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be5f4-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-269">MAPI-Id</span></span>                | <span data-ttu-id="be5f4-270">0x80F6</span><span class="sxs-lookup"><span data-stu-id="be5f4-270">0x80F6</span></span>                                           |
| <span data-ttu-id="be5f4-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="be5f4-271">System-Only</span></span>            | <span data-ttu-id="be5f4-272">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-272">True</span></span>                                             |
| <span data-ttu-id="be5f4-273">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be5f4-273">Is-Single-Valued</span></span>       | <span data-ttu-id="be5f4-274">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-274">True</span></span>                                             |
| <span data-ttu-id="be5f4-275">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be5f4-275">Is Indexed</span></span>             | <span data-ttu-id="be5f4-276">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-276">False</span></span>                                            |
| <span data-ttu-id="be5f4-277">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be5f4-277">In Global Catalog</span></span>      | <span data-ttu-id="be5f4-278">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-278">False</span></span>                                            |
| <span data-ttu-id="be5f4-279">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be5f4-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="be5f4-280">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be5f4-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be5f4-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be5f4-281">Range-Lower</span></span>            | <span data-ttu-id="be5f4-282">0</span><span class="sxs-lookup"><span data-stu-id="be5f4-282">0</span></span>                                                |
| <span data-ttu-id="be5f4-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be5f4-283">Range-Upper</span></span>            | <span data-ttu-id="be5f4-284">3</span><span class="sxs-lookup"><span data-stu-id="be5f4-284">3</span></span>                                                |
| <span data-ttu-id="be5f4-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-285">Search-Flags</span></span>           | <span data-ttu-id="be5f4-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be5f4-286">0x00000000</span></span>                                       |
| <span data-ttu-id="be5f4-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-287">System-Flags</span></span>           | <span data-ttu-id="be5f4-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be5f4-288">0x00000010</span></span>                                       |
| <span data-ttu-id="be5f4-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be5f4-289">Classes used in</span></span>        | [<span data-ttu-id="be5f4-290">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="be5f4-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be5f4-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be5f4-291">Windows Server 2012</span></span>



| <span data-ttu-id="be5f4-292">進入</span><span class="sxs-lookup"><span data-stu-id="be5f4-292">Entry</span></span> | <span data-ttu-id="be5f4-293">值</span><span class="sxs-lookup"><span data-stu-id="be5f4-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="be5f4-294">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be5f4-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="be5f4-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be5f4-295">MAPI-Id</span></span>                | <span data-ttu-id="be5f4-296">0x80F6</span><span class="sxs-lookup"><span data-stu-id="be5f4-296">0x80F6</span></span>                                           |
| <span data-ttu-id="be5f4-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="be5f4-297">System-Only</span></span>            | <span data-ttu-id="be5f4-298">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-298">True</span></span>                                             |
| <span data-ttu-id="be5f4-299">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be5f4-299">Is-Single-Valued</span></span>       | <span data-ttu-id="be5f4-300">對</span><span class="sxs-lookup"><span data-stu-id="be5f4-300">True</span></span>                                             |
| <span data-ttu-id="be5f4-301">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be5f4-301">Is Indexed</span></span>             | <span data-ttu-id="be5f4-302">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-302">False</span></span>                                            |
| <span data-ttu-id="be5f4-303">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be5f4-303">In Global Catalog</span></span>      | <span data-ttu-id="be5f4-304">否</span><span class="sxs-lookup"><span data-stu-id="be5f4-304">False</span></span>                                            |
| <span data-ttu-id="be5f4-305">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be5f4-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="be5f4-306">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be5f4-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="be5f4-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be5f4-307">Range-Lower</span></span>            | <span data-ttu-id="be5f4-308">0</span><span class="sxs-lookup"><span data-stu-id="be5f4-308">0</span></span>                                                |
| <span data-ttu-id="be5f4-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be5f4-309">Range-Upper</span></span>            | <span data-ttu-id="be5f4-310">3</span><span class="sxs-lookup"><span data-stu-id="be5f4-310">3</span></span>                                                |
| <span data-ttu-id="be5f4-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-311">Search-Flags</span></span>           | <span data-ttu-id="be5f4-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be5f4-312">0x00000000</span></span>                                       |
| <span data-ttu-id="be5f4-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be5f4-313">System-Flags</span></span>           | <span data-ttu-id="be5f4-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be5f4-314">0x00000010</span></span>                                       |
| <span data-ttu-id="be5f4-315">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be5f4-315">Classes used in</span></span>        | [<span data-ttu-id="be5f4-316">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="be5f4-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





