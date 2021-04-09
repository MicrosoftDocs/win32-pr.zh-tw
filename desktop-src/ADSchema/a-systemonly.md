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
# <a name="system-only-attribute"></a><span data-ttu-id="c21fb-106">System-Only 屬性</span><span class="sxs-lookup"><span data-stu-id="c21fb-106">System-Only attribute</span></span>

<span data-ttu-id="c21fb-107">布林值，指定是否只有 Active Directory 可以修改類別。</span><span class="sxs-lookup"><span data-stu-id="c21fb-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="c21fb-108">只能由目錄服務代理程式來建立或刪除僅限系統的類別。</span><span class="sxs-lookup"><span data-stu-id="c21fb-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="c21fb-109">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-109">Entry</span></span> | <span data-ttu-id="c21fb-110">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c21fb-111">CN</span><span class="sxs-lookup"><span data-stu-id="c21fb-111">CN</span></span>                | <span data-ttu-id="c21fb-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-112">System-Only</span></span>                          |
| <span data-ttu-id="c21fb-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c21fb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c21fb-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="c21fb-114">systemOnly</span></span>                           |
| <span data-ttu-id="c21fb-115">大小</span><span class="sxs-lookup"><span data-stu-id="c21fb-115">Size</span></span>              | <span data-ttu-id="c21fb-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="c21fb-116">4 bytes</span></span>                              |
| <span data-ttu-id="c21fb-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c21fb-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c21fb-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c21fb-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c21fb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-119">Attribute-Id</span></span>      | <span data-ttu-id="c21fb-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="c21fb-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="c21fb-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c21fb-121">System-Id-Guid</span></span>    | <span data-ttu-id="c21fb-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c21fb-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c21fb-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c21fb-123">Syntax</span></span>            | [<span data-ttu-id="c21fb-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c21fb-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c21fb-125">實作</span><span class="sxs-lookup"><span data-stu-id="c21fb-125">Implementations</span></span>

-   [<span data-ttu-id="c21fb-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c21fb-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c21fb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c21fb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c21fb-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="c21fb-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c21fb-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c21fb-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c21fb-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c21fb-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c21fb-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c21fb-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c21fb-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c21fb-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c21fb-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c21fb-133">Windows 2000 Server</span></span>



| <span data-ttu-id="c21fb-134">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-134">Entry</span></span> | <span data-ttu-id="c21fb-135">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21fb-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c21fb-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-138">System-Only</span></span>            | <span data-ttu-id="c21fb-139">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-139">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c21fb-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c21fb-141">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-141">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c21fb-142">Is Indexed</span></span>             | <span data-ttu-id="c21fb-143">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-143">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c21fb-144">In Global Catalog</span></span>      | <span data-ttu-id="c21fb-145">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-145">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c21fb-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c21fb-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c21fb-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="c21fb-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c21fb-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c21fb-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-150">Search-Flags</span></span>           | <span data-ttu-id="c21fb-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c21fb-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="c21fb-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-152">System-Flags</span></span>           | <span data-ttu-id="c21fb-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c21fb-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="c21fb-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c21fb-154">Classes used in</span></span>        | [<span data-ttu-id="c21fb-155">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="c21fb-156">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c21fb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c21fb-157">Windows Server 2003</span></span>



| <span data-ttu-id="c21fb-158">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-158">Entry</span></span> | <span data-ttu-id="c21fb-159">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21fb-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c21fb-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-162">System-Only</span></span>            | <span data-ttu-id="c21fb-163">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-163">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c21fb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c21fb-165">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-165">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c21fb-166">Is Indexed</span></span>             | <span data-ttu-id="c21fb-167">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-167">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c21fb-168">In Global Catalog</span></span>      | <span data-ttu-id="c21fb-169">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-169">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c21fb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c21fb-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c21fb-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="c21fb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c21fb-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c21fb-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-174">Search-Flags</span></span>           | <span data-ttu-id="c21fb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c21fb-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="c21fb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-176">System-Flags</span></span>           | <span data-ttu-id="c21fb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c21fb-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="c21fb-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c21fb-178">Classes used in</span></span>        | [<span data-ttu-id="c21fb-179">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="c21fb-180">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c21fb-181">亞當</span><span class="sxs-lookup"><span data-stu-id="c21fb-181">ADAM</span></span>



| <span data-ttu-id="c21fb-182">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-182">Entry</span></span> | <span data-ttu-id="c21fb-183">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21fb-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c21fb-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-186">System-Only</span></span>            | <span data-ttu-id="c21fb-187">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-187">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c21fb-188">Is-Single-Valued</span></span>       | <span data-ttu-id="c21fb-189">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-189">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c21fb-190">Is Indexed</span></span>             | <span data-ttu-id="c21fb-191">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-191">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c21fb-192">In Global Catalog</span></span>      | <span data-ttu-id="c21fb-193">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-193">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c21fb-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="c21fb-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c21fb-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="c21fb-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c21fb-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c21fb-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-198">Search-Flags</span></span>           | <span data-ttu-id="c21fb-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c21fb-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="c21fb-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-200">System-Flags</span></span>           | <span data-ttu-id="c21fb-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c21fb-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="c21fb-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c21fb-202">Classes used in</span></span>        | [<span data-ttu-id="c21fb-203">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="c21fb-204">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c21fb-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c21fb-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c21fb-206">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-206">Entry</span></span> | <span data-ttu-id="c21fb-207">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21fb-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c21fb-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-210">System-Only</span></span>            | <span data-ttu-id="c21fb-211">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-211">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c21fb-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c21fb-213">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-213">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c21fb-214">Is Indexed</span></span>             | <span data-ttu-id="c21fb-215">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-215">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c21fb-216">In Global Catalog</span></span>      | <span data-ttu-id="c21fb-217">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-217">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c21fb-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c21fb-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c21fb-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="c21fb-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c21fb-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c21fb-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-222">Search-Flags</span></span>           | <span data-ttu-id="c21fb-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c21fb-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="c21fb-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-224">System-Flags</span></span>           | <span data-ttu-id="c21fb-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c21fb-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="c21fb-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c21fb-226">Classes used in</span></span>        | [<span data-ttu-id="c21fb-227">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="c21fb-228">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c21fb-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c21fb-229">Windows Server 2008</span></span>



| <span data-ttu-id="c21fb-230">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-230">Entry</span></span> | <span data-ttu-id="c21fb-231">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21fb-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c21fb-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-234">System-Only</span></span>            | <span data-ttu-id="c21fb-235">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-235">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c21fb-236">Is-Single-Valued</span></span>       | <span data-ttu-id="c21fb-237">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-237">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c21fb-238">Is Indexed</span></span>             | <span data-ttu-id="c21fb-239">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-239">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c21fb-240">In Global Catalog</span></span>      | <span data-ttu-id="c21fb-241">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-241">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c21fb-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="c21fb-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c21fb-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="c21fb-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c21fb-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c21fb-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-246">Search-Flags</span></span>           | <span data-ttu-id="c21fb-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c21fb-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="c21fb-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-248">System-Flags</span></span>           | <span data-ttu-id="c21fb-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c21fb-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="c21fb-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c21fb-250">Classes used in</span></span>        | [<span data-ttu-id="c21fb-251">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="c21fb-252">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c21fb-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c21fb-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c21fb-254">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-254">Entry</span></span> | <span data-ttu-id="c21fb-255">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21fb-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c21fb-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-258">System-Only</span></span>            | <span data-ttu-id="c21fb-259">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-259">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c21fb-260">Is-Single-Valued</span></span>       | <span data-ttu-id="c21fb-261">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-261">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c21fb-262">Is Indexed</span></span>             | <span data-ttu-id="c21fb-263">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-263">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c21fb-264">In Global Catalog</span></span>      | <span data-ttu-id="c21fb-265">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-265">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c21fb-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="c21fb-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c21fb-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="c21fb-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c21fb-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c21fb-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-270">Search-Flags</span></span>           | <span data-ttu-id="c21fb-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c21fb-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="c21fb-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-272">System-Flags</span></span>           | <span data-ttu-id="c21fb-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c21fb-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="c21fb-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c21fb-274">Classes used in</span></span>        | [<span data-ttu-id="c21fb-275">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="c21fb-276">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c21fb-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c21fb-277">Windows Server 2012</span></span>



| <span data-ttu-id="c21fb-278">進入</span><span class="sxs-lookup"><span data-stu-id="c21fb-278">Entry</span></span> | <span data-ttu-id="c21fb-279">值</span><span class="sxs-lookup"><span data-stu-id="c21fb-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21fb-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c21fb-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c21fb-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="c21fb-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="c21fb-282">System-Only</span></span>            | <span data-ttu-id="c21fb-283">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-283">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c21fb-284">Is-Single-Valued</span></span>       | <span data-ttu-id="c21fb-285">對</span><span class="sxs-lookup"><span data-stu-id="c21fb-285">True</span></span>                                                                                                      |
| <span data-ttu-id="c21fb-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c21fb-286">Is Indexed</span></span>             | <span data-ttu-id="c21fb-287">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-287">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c21fb-288">In Global Catalog</span></span>      | <span data-ttu-id="c21fb-289">否</span><span class="sxs-lookup"><span data-stu-id="c21fb-289">False</span></span>                                                                                                     |
| <span data-ttu-id="c21fb-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c21fb-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="c21fb-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c21fb-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="c21fb-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c21fb-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c21fb-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="c21fb-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-294">Search-Flags</span></span>           | <span data-ttu-id="c21fb-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c21fb-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="c21fb-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c21fb-296">System-Flags</span></span>           | <span data-ttu-id="c21fb-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c21fb-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="c21fb-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c21fb-298">Classes used in</span></span>        | [<span data-ttu-id="c21fb-299">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="c21fb-300">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="c21fb-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





