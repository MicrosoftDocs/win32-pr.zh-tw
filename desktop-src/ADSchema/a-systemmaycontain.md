---
title: System-可包含屬性
description: 類別的選擇性屬性清單。 屬性清單只能由系統修改。
ms.assetid: b2fbeb64-d147-4c1a-a609-4f16327609ce
ms.tgt_platform: multiple
keywords:
- System-可包含屬性 AD 架構
- systemMayContain 屬性 AD 架構
topic_type:
- apiref
api_name:
- System-May-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03730e9904cbaa6ee5954662556fba261c51cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107502"
---
# <a name="system-may-contain-attribute"></a><span data-ttu-id="dc421-106">System-可包含屬性</span><span class="sxs-lookup"><span data-stu-id="dc421-106">System-May-Contain attribute</span></span>

<span data-ttu-id="dc421-107">類別的選擇性屬性清單。</span><span class="sxs-lookup"><span data-stu-id="dc421-107">The list of optional attributes for a class.</span></span> <span data-ttu-id="dc421-108">屬性清單只能由系統修改。</span><span class="sxs-lookup"><span data-stu-id="dc421-108">The list of attributes can only be modified by the system.</span></span>



| <span data-ttu-id="dc421-109">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-109">Entry</span></span> | <span data-ttu-id="dc421-110">值</span><span class="sxs-lookup"><span data-stu-id="dc421-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="dc421-111">CN</span><span class="sxs-lookup"><span data-stu-id="dc421-111">CN</span></span>                | <span data-ttu-id="dc421-112">系統-可能包含</span><span class="sxs-lookup"><span data-stu-id="dc421-112">System-May-Contain</span></span>                                                           |
| <span data-ttu-id="dc421-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dc421-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dc421-114">systemMayContain</span><span class="sxs-lookup"><span data-stu-id="dc421-114">systemMayContain</span></span>                                                             |
| <span data-ttu-id="dc421-115">大小</span><span class="sxs-lookup"><span data-stu-id="dc421-115">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="dc421-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dc421-116">Update Privilege</span></span>  | <span data-ttu-id="dc421-117">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="dc421-117">Schema administrator</span></span>                                                         |
| <span data-ttu-id="dc421-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dc421-118">Update Frequency</span></span>  | <span data-ttu-id="dc421-119">建立類別時，或將新的選擇性屬性加入至類別。</span><span class="sxs-lookup"><span data-stu-id="dc421-119">When the class is created or a new optional attribute is added to the class.</span></span> |
| <span data-ttu-id="dc421-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-120">Attribute-Id</span></span>      | <span data-ttu-id="dc421-121">1.2.840.113556.1.4.196</span><span class="sxs-lookup"><span data-stu-id="dc421-121">1.2.840.113556.1.4.196</span></span>                                                       |
| <span data-ttu-id="dc421-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dc421-122">System-Id-Guid</span></span>    | <span data-ttu-id="dc421-123">bf967a44-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dc421-123">bf967a44-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="dc421-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc421-124">Syntax</span></span>            | [<span data-ttu-id="dc421-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="dc421-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)              |



## <a name="implementations"></a><span data-ttu-id="dc421-126">實作</span><span class="sxs-lookup"><span data-stu-id="dc421-126">Implementations</span></span>

-   [<span data-ttu-id="dc421-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dc421-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dc421-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dc421-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dc421-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="dc421-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dc421-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dc421-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dc421-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dc421-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dc421-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dc421-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dc421-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dc421-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dc421-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc421-134">Windows 2000 Server</span></span>



| <span data-ttu-id="dc421-135">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-135">Entry</span></span> | <span data-ttu-id="dc421-136">值</span><span class="sxs-lookup"><span data-stu-id="dc421-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dc421-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc421-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc421-139">System-Only</span></span>            | <span data-ttu-id="dc421-140">對</span><span class="sxs-lookup"><span data-stu-id="dc421-140">True</span></span>                                             |
| <span data-ttu-id="dc421-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc421-141">Is-Single-Valued</span></span>       | <span data-ttu-id="dc421-142">否</span><span class="sxs-lookup"><span data-stu-id="dc421-142">False</span></span>                                            |
| <span data-ttu-id="dc421-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc421-143">Is Indexed</span></span>             | <span data-ttu-id="dc421-144">否</span><span class="sxs-lookup"><span data-stu-id="dc421-144">False</span></span>                                            |
| <span data-ttu-id="dc421-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc421-145">In Global Catalog</span></span>      | <span data-ttu-id="dc421-146">否</span><span class="sxs-lookup"><span data-stu-id="dc421-146">False</span></span>                                            |
| <span data-ttu-id="dc421-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc421-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc421-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc421-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dc421-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc421-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dc421-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc421-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dc421-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-151">Search-Flags</span></span>           | <span data-ttu-id="dc421-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc421-152">0x00000000</span></span>                                       |
| <span data-ttu-id="dc421-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-153">System-Flags</span></span>           | <span data-ttu-id="dc421-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc421-154">0x00000010</span></span>                                       |
| <span data-ttu-id="dc421-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc421-155">Classes used in</span></span>        | [<span data-ttu-id="dc421-156">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="dc421-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dc421-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc421-157">Windows Server 2003</span></span>



| <span data-ttu-id="dc421-158">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-158">Entry</span></span> | <span data-ttu-id="dc421-159">值</span><span class="sxs-lookup"><span data-stu-id="dc421-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dc421-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc421-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc421-162">System-Only</span></span>            | <span data-ttu-id="dc421-163">對</span><span class="sxs-lookup"><span data-stu-id="dc421-163">True</span></span>                                             |
| <span data-ttu-id="dc421-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc421-164">Is-Single-Valued</span></span>       | <span data-ttu-id="dc421-165">否</span><span class="sxs-lookup"><span data-stu-id="dc421-165">False</span></span>                                            |
| <span data-ttu-id="dc421-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc421-166">Is Indexed</span></span>             | <span data-ttu-id="dc421-167">否</span><span class="sxs-lookup"><span data-stu-id="dc421-167">False</span></span>                                            |
| <span data-ttu-id="dc421-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc421-168">In Global Catalog</span></span>      | <span data-ttu-id="dc421-169">否</span><span class="sxs-lookup"><span data-stu-id="dc421-169">False</span></span>                                            |
| <span data-ttu-id="dc421-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc421-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc421-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc421-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dc421-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc421-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dc421-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc421-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dc421-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-174">Search-Flags</span></span>           | <span data-ttu-id="dc421-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc421-175">0x00000000</span></span>                                       |
| <span data-ttu-id="dc421-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-176">System-Flags</span></span>           | <span data-ttu-id="dc421-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc421-177">0x00000010</span></span>                                       |
| <span data-ttu-id="dc421-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc421-178">Classes used in</span></span>        | [<span data-ttu-id="dc421-179">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="dc421-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dc421-180">亞當</span><span class="sxs-lookup"><span data-stu-id="dc421-180">ADAM</span></span>



| <span data-ttu-id="dc421-181">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-181">Entry</span></span> | <span data-ttu-id="dc421-182">值</span><span class="sxs-lookup"><span data-stu-id="dc421-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dc421-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc421-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc421-185">System-Only</span></span>            | <span data-ttu-id="dc421-186">對</span><span class="sxs-lookup"><span data-stu-id="dc421-186">True</span></span>                                             |
| <span data-ttu-id="dc421-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc421-187">Is-Single-Valued</span></span>       | <span data-ttu-id="dc421-188">否</span><span class="sxs-lookup"><span data-stu-id="dc421-188">False</span></span>                                            |
| <span data-ttu-id="dc421-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc421-189">Is Indexed</span></span>             | <span data-ttu-id="dc421-190">否</span><span class="sxs-lookup"><span data-stu-id="dc421-190">False</span></span>                                            |
| <span data-ttu-id="dc421-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc421-191">In Global Catalog</span></span>      | <span data-ttu-id="dc421-192">否</span><span class="sxs-lookup"><span data-stu-id="dc421-192">False</span></span>                                            |
| <span data-ttu-id="dc421-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc421-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc421-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc421-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dc421-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc421-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dc421-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc421-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dc421-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-197">Search-Flags</span></span>           | <span data-ttu-id="dc421-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc421-198">0x00000000</span></span>                                       |
| <span data-ttu-id="dc421-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-199">System-Flags</span></span>           | <span data-ttu-id="dc421-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc421-200">0x00000010</span></span>                                       |
| <span data-ttu-id="dc421-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc421-201">Classes used in</span></span>        | [<span data-ttu-id="dc421-202">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="dc421-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dc421-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dc421-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dc421-204">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-204">Entry</span></span> | <span data-ttu-id="dc421-205">值</span><span class="sxs-lookup"><span data-stu-id="dc421-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dc421-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc421-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc421-208">System-Only</span></span>            | <span data-ttu-id="dc421-209">對</span><span class="sxs-lookup"><span data-stu-id="dc421-209">True</span></span>                                             |
| <span data-ttu-id="dc421-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc421-210">Is-Single-Valued</span></span>       | <span data-ttu-id="dc421-211">否</span><span class="sxs-lookup"><span data-stu-id="dc421-211">False</span></span>                                            |
| <span data-ttu-id="dc421-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc421-212">Is Indexed</span></span>             | <span data-ttu-id="dc421-213">否</span><span class="sxs-lookup"><span data-stu-id="dc421-213">False</span></span>                                            |
| <span data-ttu-id="dc421-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc421-214">In Global Catalog</span></span>      | <span data-ttu-id="dc421-215">否</span><span class="sxs-lookup"><span data-stu-id="dc421-215">False</span></span>                                            |
| <span data-ttu-id="dc421-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc421-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc421-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc421-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dc421-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc421-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dc421-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc421-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dc421-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-220">Search-Flags</span></span>           | <span data-ttu-id="dc421-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc421-221">0x00000000</span></span>                                       |
| <span data-ttu-id="dc421-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-222">System-Flags</span></span>           | <span data-ttu-id="dc421-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc421-223">0x00000010</span></span>                                       |
| <span data-ttu-id="dc421-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc421-224">Classes used in</span></span>        | [<span data-ttu-id="dc421-225">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="dc421-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dc421-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc421-226">Windows Server 2008</span></span>



| <span data-ttu-id="dc421-227">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-227">Entry</span></span> | <span data-ttu-id="dc421-228">值</span><span class="sxs-lookup"><span data-stu-id="dc421-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dc421-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc421-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc421-231">System-Only</span></span>            | <span data-ttu-id="dc421-232">對</span><span class="sxs-lookup"><span data-stu-id="dc421-232">True</span></span>                                             |
| <span data-ttu-id="dc421-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc421-233">Is-Single-Valued</span></span>       | <span data-ttu-id="dc421-234">否</span><span class="sxs-lookup"><span data-stu-id="dc421-234">False</span></span>                                            |
| <span data-ttu-id="dc421-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc421-235">Is Indexed</span></span>             | <span data-ttu-id="dc421-236">否</span><span class="sxs-lookup"><span data-stu-id="dc421-236">False</span></span>                                            |
| <span data-ttu-id="dc421-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc421-237">In Global Catalog</span></span>      | <span data-ttu-id="dc421-238">否</span><span class="sxs-lookup"><span data-stu-id="dc421-238">False</span></span>                                            |
| <span data-ttu-id="dc421-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc421-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc421-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc421-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dc421-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc421-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dc421-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc421-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dc421-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-243">Search-Flags</span></span>           | <span data-ttu-id="dc421-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc421-244">0x00000000</span></span>                                       |
| <span data-ttu-id="dc421-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-245">System-Flags</span></span>           | <span data-ttu-id="dc421-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc421-246">0x00000010</span></span>                                       |
| <span data-ttu-id="dc421-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc421-247">Classes used in</span></span>        | [<span data-ttu-id="dc421-248">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="dc421-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dc421-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc421-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dc421-250">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-250">Entry</span></span> | <span data-ttu-id="dc421-251">值</span><span class="sxs-lookup"><span data-stu-id="dc421-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dc421-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc421-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc421-254">System-Only</span></span>            | <span data-ttu-id="dc421-255">對</span><span class="sxs-lookup"><span data-stu-id="dc421-255">True</span></span>                                             |
| <span data-ttu-id="dc421-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc421-256">Is-Single-Valued</span></span>       | <span data-ttu-id="dc421-257">否</span><span class="sxs-lookup"><span data-stu-id="dc421-257">False</span></span>                                            |
| <span data-ttu-id="dc421-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc421-258">Is Indexed</span></span>             | <span data-ttu-id="dc421-259">否</span><span class="sxs-lookup"><span data-stu-id="dc421-259">False</span></span>                                            |
| <span data-ttu-id="dc421-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc421-260">In Global Catalog</span></span>      | <span data-ttu-id="dc421-261">否</span><span class="sxs-lookup"><span data-stu-id="dc421-261">False</span></span>                                            |
| <span data-ttu-id="dc421-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc421-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc421-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc421-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dc421-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc421-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dc421-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc421-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dc421-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-266">Search-Flags</span></span>           | <span data-ttu-id="dc421-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc421-267">0x00000000</span></span>                                       |
| <span data-ttu-id="dc421-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-268">System-Flags</span></span>           | <span data-ttu-id="dc421-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc421-269">0x00000010</span></span>                                       |
| <span data-ttu-id="dc421-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc421-270">Classes used in</span></span>        | [<span data-ttu-id="dc421-271">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="dc421-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dc421-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc421-272">Windows Server 2012</span></span>



| <span data-ttu-id="dc421-273">進入</span><span class="sxs-lookup"><span data-stu-id="dc421-273">Entry</span></span> | <span data-ttu-id="dc421-274">值</span><span class="sxs-lookup"><span data-stu-id="dc421-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dc421-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc421-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc421-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="dc421-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc421-277">System-Only</span></span>            | <span data-ttu-id="dc421-278">對</span><span class="sxs-lookup"><span data-stu-id="dc421-278">True</span></span>                                             |
| <span data-ttu-id="dc421-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc421-279">Is-Single-Valued</span></span>       | <span data-ttu-id="dc421-280">否</span><span class="sxs-lookup"><span data-stu-id="dc421-280">False</span></span>                                            |
| <span data-ttu-id="dc421-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc421-281">Is Indexed</span></span>             | <span data-ttu-id="dc421-282">否</span><span class="sxs-lookup"><span data-stu-id="dc421-282">False</span></span>                                            |
| <span data-ttu-id="dc421-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc421-283">In Global Catalog</span></span>      | <span data-ttu-id="dc421-284">否</span><span class="sxs-lookup"><span data-stu-id="dc421-284">False</span></span>                                            |
| <span data-ttu-id="dc421-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc421-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc421-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc421-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dc421-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc421-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dc421-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc421-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dc421-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-289">Search-Flags</span></span>           | <span data-ttu-id="dc421-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc421-290">0x00000000</span></span>                                       |
| <span data-ttu-id="dc421-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc421-291">System-Flags</span></span>           | <span data-ttu-id="dc421-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc421-292">0x00000010</span></span>                                       |
| <span data-ttu-id="dc421-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc421-293">Classes used in</span></span>        | [<span data-ttu-id="dc421-294">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="dc421-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





