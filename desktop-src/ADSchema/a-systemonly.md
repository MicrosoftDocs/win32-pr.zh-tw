---
title: System-Only 屬性
description: 布林值，指定是否只有 Active Directory 可以修改類別。 只能由目錄服務代理程式來建立或刪除僅限系統的類別。
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- System-Only 屬性 AD 架構
- systemOnly 屬性 AD 架構
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844915"
---
# <a name="system-only-attribute"></a><span data-ttu-id="297ac-106">System-Only 屬性</span><span class="sxs-lookup"><span data-stu-id="297ac-106">System-Only attribute</span></span>

<span data-ttu-id="297ac-107">布林值，指定是否只有 Active Directory 可以修改類別。</span><span class="sxs-lookup"><span data-stu-id="297ac-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="297ac-108">只能由目錄服務代理程式來建立或刪除僅限系統的類別。</span><span class="sxs-lookup"><span data-stu-id="297ac-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="297ac-109">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-109">Entry</span></span> | <span data-ttu-id="297ac-110">值</span><span class="sxs-lookup"><span data-stu-id="297ac-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="297ac-111">CN</span><span class="sxs-lookup"><span data-stu-id="297ac-111">CN</span></span>                | <span data-ttu-id="297ac-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-112">System-Only</span></span>                          |
| <span data-ttu-id="297ac-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="297ac-113">Ldap-Display-Name</span></span> | <span data-ttu-id="297ac-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="297ac-114">systemOnly</span></span>                           |
| <span data-ttu-id="297ac-115">大小</span><span class="sxs-lookup"><span data-stu-id="297ac-115">Size</span></span>              | <span data-ttu-id="297ac-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="297ac-116">4 bytes</span></span>                              |
| <span data-ttu-id="297ac-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="297ac-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="297ac-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="297ac-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="297ac-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-119">Attribute-Id</span></span>      | <span data-ttu-id="297ac-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="297ac-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="297ac-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="297ac-121">System-Id-Guid</span></span>    | <span data-ttu-id="297ac-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="297ac-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="297ac-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="297ac-123">Syntax</span></span>            | [<span data-ttu-id="297ac-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="297ac-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="297ac-125">實作</span><span class="sxs-lookup"><span data-stu-id="297ac-125">Implementations</span></span>

-   [<span data-ttu-id="297ac-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="297ac-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="297ac-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="297ac-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="297ac-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="297ac-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="297ac-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="297ac-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="297ac-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="297ac-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="297ac-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="297ac-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="297ac-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="297ac-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="297ac-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="297ac-133">Windows 2000 Server</span></span>



| <span data-ttu-id="297ac-134">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-134">Entry</span></span> | <span data-ttu-id="297ac-135">值</span><span class="sxs-lookup"><span data-stu-id="297ac-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297ac-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="297ac-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-138">System-Only</span></span>            | <span data-ttu-id="297ac-139">對</span><span class="sxs-lookup"><span data-stu-id="297ac-139">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="297ac-140">Is-Single-Valued</span></span>       | <span data-ttu-id="297ac-141">對</span><span class="sxs-lookup"><span data-stu-id="297ac-141">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="297ac-142">Is Indexed</span></span>             | <span data-ttu-id="297ac-143">否</span><span class="sxs-lookup"><span data-stu-id="297ac-143">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="297ac-144">In Global Catalog</span></span>      | <span data-ttu-id="297ac-145">否</span><span class="sxs-lookup"><span data-stu-id="297ac-145">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="297ac-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="297ac-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="297ac-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="297ac-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="297ac-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="297ac-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-150">Search-Flags</span></span>           | <span data-ttu-id="297ac-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="297ac-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="297ac-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-152">System-Flags</span></span>           | <span data-ttu-id="297ac-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="297ac-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="297ac-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="297ac-154">Classes used in</span></span>        | [<span data-ttu-id="297ac-155">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="297ac-156">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="297ac-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="297ac-157">Windows Server 2003</span></span>



| <span data-ttu-id="297ac-158">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-158">Entry</span></span> | <span data-ttu-id="297ac-159">值</span><span class="sxs-lookup"><span data-stu-id="297ac-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297ac-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="297ac-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-162">System-Only</span></span>            | <span data-ttu-id="297ac-163">對</span><span class="sxs-lookup"><span data-stu-id="297ac-163">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="297ac-164">Is-Single-Valued</span></span>       | <span data-ttu-id="297ac-165">對</span><span class="sxs-lookup"><span data-stu-id="297ac-165">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="297ac-166">Is Indexed</span></span>             | <span data-ttu-id="297ac-167">否</span><span class="sxs-lookup"><span data-stu-id="297ac-167">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="297ac-168">In Global Catalog</span></span>      | <span data-ttu-id="297ac-169">否</span><span class="sxs-lookup"><span data-stu-id="297ac-169">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="297ac-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="297ac-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="297ac-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="297ac-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="297ac-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="297ac-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-174">Search-Flags</span></span>           | <span data-ttu-id="297ac-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="297ac-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="297ac-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-176">System-Flags</span></span>           | <span data-ttu-id="297ac-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="297ac-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="297ac-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="297ac-178">Classes used in</span></span>        | [<span data-ttu-id="297ac-179">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="297ac-180">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="297ac-181">亞當</span><span class="sxs-lookup"><span data-stu-id="297ac-181">ADAM</span></span>



| <span data-ttu-id="297ac-182">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-182">Entry</span></span> | <span data-ttu-id="297ac-183">值</span><span class="sxs-lookup"><span data-stu-id="297ac-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297ac-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="297ac-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-186">System-Only</span></span>            | <span data-ttu-id="297ac-187">對</span><span class="sxs-lookup"><span data-stu-id="297ac-187">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="297ac-188">Is-Single-Valued</span></span>       | <span data-ttu-id="297ac-189">對</span><span class="sxs-lookup"><span data-stu-id="297ac-189">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="297ac-190">Is Indexed</span></span>             | <span data-ttu-id="297ac-191">否</span><span class="sxs-lookup"><span data-stu-id="297ac-191">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="297ac-192">In Global Catalog</span></span>      | <span data-ttu-id="297ac-193">否</span><span class="sxs-lookup"><span data-stu-id="297ac-193">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="297ac-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="297ac-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="297ac-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="297ac-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="297ac-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="297ac-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-198">Search-Flags</span></span>           | <span data-ttu-id="297ac-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="297ac-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="297ac-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-200">System-Flags</span></span>           | <span data-ttu-id="297ac-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="297ac-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="297ac-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="297ac-202">Classes used in</span></span>        | [<span data-ttu-id="297ac-203">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="297ac-204">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="297ac-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="297ac-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="297ac-206">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-206">Entry</span></span> | <span data-ttu-id="297ac-207">值</span><span class="sxs-lookup"><span data-stu-id="297ac-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297ac-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="297ac-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-210">System-Only</span></span>            | <span data-ttu-id="297ac-211">對</span><span class="sxs-lookup"><span data-stu-id="297ac-211">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="297ac-212">Is-Single-Valued</span></span>       | <span data-ttu-id="297ac-213">對</span><span class="sxs-lookup"><span data-stu-id="297ac-213">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="297ac-214">Is Indexed</span></span>             | <span data-ttu-id="297ac-215">否</span><span class="sxs-lookup"><span data-stu-id="297ac-215">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="297ac-216">In Global Catalog</span></span>      | <span data-ttu-id="297ac-217">否</span><span class="sxs-lookup"><span data-stu-id="297ac-217">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="297ac-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="297ac-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="297ac-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="297ac-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="297ac-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="297ac-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-222">Search-Flags</span></span>           | <span data-ttu-id="297ac-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="297ac-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="297ac-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-224">System-Flags</span></span>           | <span data-ttu-id="297ac-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="297ac-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="297ac-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="297ac-226">Classes used in</span></span>        | [<span data-ttu-id="297ac-227">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="297ac-228">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="297ac-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="297ac-229">Windows Server 2008</span></span>



| <span data-ttu-id="297ac-230">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-230">Entry</span></span> | <span data-ttu-id="297ac-231">值</span><span class="sxs-lookup"><span data-stu-id="297ac-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297ac-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="297ac-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-234">System-Only</span></span>            | <span data-ttu-id="297ac-235">對</span><span class="sxs-lookup"><span data-stu-id="297ac-235">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="297ac-236">Is-Single-Valued</span></span>       | <span data-ttu-id="297ac-237">對</span><span class="sxs-lookup"><span data-stu-id="297ac-237">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="297ac-238">Is Indexed</span></span>             | <span data-ttu-id="297ac-239">否</span><span class="sxs-lookup"><span data-stu-id="297ac-239">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="297ac-240">In Global Catalog</span></span>      | <span data-ttu-id="297ac-241">否</span><span class="sxs-lookup"><span data-stu-id="297ac-241">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="297ac-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="297ac-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="297ac-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="297ac-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="297ac-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="297ac-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-246">Search-Flags</span></span>           | <span data-ttu-id="297ac-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="297ac-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="297ac-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-248">System-Flags</span></span>           | <span data-ttu-id="297ac-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="297ac-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="297ac-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="297ac-250">Classes used in</span></span>        | [<span data-ttu-id="297ac-251">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="297ac-252">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="297ac-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="297ac-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="297ac-254">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-254">Entry</span></span> | <span data-ttu-id="297ac-255">值</span><span class="sxs-lookup"><span data-stu-id="297ac-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297ac-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="297ac-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-258">System-Only</span></span>            | <span data-ttu-id="297ac-259">對</span><span class="sxs-lookup"><span data-stu-id="297ac-259">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="297ac-260">Is-Single-Valued</span></span>       | <span data-ttu-id="297ac-261">對</span><span class="sxs-lookup"><span data-stu-id="297ac-261">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="297ac-262">Is Indexed</span></span>             | <span data-ttu-id="297ac-263">否</span><span class="sxs-lookup"><span data-stu-id="297ac-263">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="297ac-264">In Global Catalog</span></span>      | <span data-ttu-id="297ac-265">否</span><span class="sxs-lookup"><span data-stu-id="297ac-265">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="297ac-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="297ac-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="297ac-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="297ac-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="297ac-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="297ac-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-270">Search-Flags</span></span>           | <span data-ttu-id="297ac-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="297ac-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="297ac-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-272">System-Flags</span></span>           | <span data-ttu-id="297ac-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="297ac-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="297ac-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="297ac-274">Classes used in</span></span>        | [<span data-ttu-id="297ac-275">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="297ac-276">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="297ac-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="297ac-277">Windows Server 2012</span></span>



| <span data-ttu-id="297ac-278">進入</span><span class="sxs-lookup"><span data-stu-id="297ac-278">Entry</span></span> | <span data-ttu-id="297ac-279">值</span><span class="sxs-lookup"><span data-stu-id="297ac-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297ac-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="297ac-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="297ac-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="297ac-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="297ac-282">System-Only</span></span>            | <span data-ttu-id="297ac-283">對</span><span class="sxs-lookup"><span data-stu-id="297ac-283">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="297ac-284">Is-Single-Valued</span></span>       | <span data-ttu-id="297ac-285">對</span><span class="sxs-lookup"><span data-stu-id="297ac-285">True</span></span>                                                                                                      |
| <span data-ttu-id="297ac-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="297ac-286">Is Indexed</span></span>             | <span data-ttu-id="297ac-287">否</span><span class="sxs-lookup"><span data-stu-id="297ac-287">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="297ac-288">In Global Catalog</span></span>      | <span data-ttu-id="297ac-289">否</span><span class="sxs-lookup"><span data-stu-id="297ac-289">False</span></span>                                                                                                     |
| <span data-ttu-id="297ac-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="297ac-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="297ac-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="297ac-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="297ac-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="297ac-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="297ac-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="297ac-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-294">Search-Flags</span></span>           | <span data-ttu-id="297ac-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="297ac-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="297ac-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="297ac-296">System-Flags</span></span>           | <span data-ttu-id="297ac-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="297ac-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="297ac-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="297ac-298">Classes used in</span></span>        | [<span data-ttu-id="297ac-299">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="297ac-300">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="297ac-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





