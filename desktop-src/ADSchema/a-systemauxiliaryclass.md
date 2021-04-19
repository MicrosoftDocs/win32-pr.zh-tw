---
title: 系統輔助類別屬性
description: 使用者無法修改的輔助類別清單。
ms.assetid: 6d629925-7321-4f3a-bf4c-4adf0d33c946
ms.tgt_platform: multiple
keywords:
- 系統輔助類別屬性 AD 架構
- systemAuxiliaryClass 屬性 AD 架構
topic_type:
- apiref
api_name:
- System-Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe70899ba2bda8fe98b38228cb661e7a773ec1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970045"
---
# <a name="system-auxiliary-class-attribute"></a><span data-ttu-id="ed365-105">系統輔助類別屬性</span><span class="sxs-lookup"><span data-stu-id="ed365-105">System-Auxiliary-Class attribute</span></span>

<span data-ttu-id="ed365-106">使用者無法修改的輔助類別清單。</span><span class="sxs-lookup"><span data-stu-id="ed365-106">A list of auxiliary classes that cannot be modified by the user.</span></span>



| <span data-ttu-id="ed365-107">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-107">Entry</span></span> | <span data-ttu-id="ed365-108">值</span><span class="sxs-lookup"><span data-stu-id="ed365-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ed365-109">CN</span><span class="sxs-lookup"><span data-stu-id="ed365-109">CN</span></span>                | <span data-ttu-id="ed365-110">系統輔助類別</span><span class="sxs-lookup"><span data-stu-id="ed365-110">System-Auxiliary-Class</span></span>                                             |
| <span data-ttu-id="ed365-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ed365-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ed365-112">systemAuxiliaryClass</span><span class="sxs-lookup"><span data-stu-id="ed365-112">systemAuxiliaryClass</span></span>                                               |
| <span data-ttu-id="ed365-113">大小</span><span class="sxs-lookup"><span data-stu-id="ed365-113">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="ed365-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ed365-114">Update Privilege</span></span>  | <span data-ttu-id="ed365-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="ed365-115">Schema administrator</span></span>                                               |
| <span data-ttu-id="ed365-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ed365-116">Update Frequency</span></span>  | <span data-ttu-id="ed365-117">建立類別或加入新的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="ed365-117">When the class is created or a new auxiliary class is added to it.</span></span> |
| <span data-ttu-id="ed365-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-118">Attribute-Id</span></span>      | <span data-ttu-id="ed365-119">1.2.840.113556.1.4.198</span><span class="sxs-lookup"><span data-stu-id="ed365-119">1.2.840.113556.1.4.198</span></span>                                             |
| <span data-ttu-id="ed365-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ed365-120">System-Id-Guid</span></span>    | <span data-ttu-id="ed365-121">bf967a43-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ed365-121">bf967a43-0de6-11d0-a285-00aa003049e2</span></span>                               |
| <span data-ttu-id="ed365-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed365-122">Syntax</span></span>            | [<span data-ttu-id="ed365-123">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="ed365-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)    |



## <a name="implementations"></a><span data-ttu-id="ed365-124">實作</span><span class="sxs-lookup"><span data-stu-id="ed365-124">Implementations</span></span>

-   [<span data-ttu-id="ed365-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ed365-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ed365-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ed365-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ed365-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ed365-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ed365-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ed365-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ed365-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ed365-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ed365-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ed365-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ed365-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ed365-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ed365-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ed365-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ed365-133">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-133">Entry</span></span> | <span data-ttu-id="ed365-134">值</span><span class="sxs-lookup"><span data-stu-id="ed365-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ed365-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed365-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed365-137">System-Only</span></span>            | <span data-ttu-id="ed365-138">對</span><span class="sxs-lookup"><span data-stu-id="ed365-138">True</span></span>                                             |
| <span data-ttu-id="ed365-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed365-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ed365-140">否</span><span class="sxs-lookup"><span data-stu-id="ed365-140">False</span></span>                                            |
| <span data-ttu-id="ed365-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed365-141">Is Indexed</span></span>             | <span data-ttu-id="ed365-142">否</span><span class="sxs-lookup"><span data-stu-id="ed365-142">False</span></span>                                            |
| <span data-ttu-id="ed365-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed365-143">In Global Catalog</span></span>      | <span data-ttu-id="ed365-144">否</span><span class="sxs-lookup"><span data-stu-id="ed365-144">False</span></span>                                            |
| <span data-ttu-id="ed365-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed365-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed365-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed365-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ed365-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed365-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ed365-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed365-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ed365-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-149">Search-Flags</span></span>           | <span data-ttu-id="ed365-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed365-150">0x00000000</span></span>                                       |
| <span data-ttu-id="ed365-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-151">System-Flags</span></span>           | <span data-ttu-id="ed365-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed365-152">0x00000010</span></span>                                       |
| <span data-ttu-id="ed365-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed365-153">Classes used in</span></span>        | [<span data-ttu-id="ed365-154">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ed365-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ed365-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed365-155">Windows Server 2003</span></span>



| <span data-ttu-id="ed365-156">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-156">Entry</span></span> | <span data-ttu-id="ed365-157">值</span><span class="sxs-lookup"><span data-stu-id="ed365-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ed365-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed365-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed365-160">System-Only</span></span>            | <span data-ttu-id="ed365-161">對</span><span class="sxs-lookup"><span data-stu-id="ed365-161">True</span></span>                                             |
| <span data-ttu-id="ed365-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed365-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ed365-163">否</span><span class="sxs-lookup"><span data-stu-id="ed365-163">False</span></span>                                            |
| <span data-ttu-id="ed365-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed365-164">Is Indexed</span></span>             | <span data-ttu-id="ed365-165">否</span><span class="sxs-lookup"><span data-stu-id="ed365-165">False</span></span>                                            |
| <span data-ttu-id="ed365-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed365-166">In Global Catalog</span></span>      | <span data-ttu-id="ed365-167">否</span><span class="sxs-lookup"><span data-stu-id="ed365-167">False</span></span>                                            |
| <span data-ttu-id="ed365-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed365-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed365-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed365-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ed365-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed365-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ed365-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed365-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ed365-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-172">Search-Flags</span></span>           | <span data-ttu-id="ed365-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed365-173">0x00000000</span></span>                                       |
| <span data-ttu-id="ed365-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-174">System-Flags</span></span>           | <span data-ttu-id="ed365-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed365-175">0x00000010</span></span>                                       |
| <span data-ttu-id="ed365-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed365-176">Classes used in</span></span>        | [<span data-ttu-id="ed365-177">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ed365-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ed365-178">亞當</span><span class="sxs-lookup"><span data-stu-id="ed365-178">ADAM</span></span>



| <span data-ttu-id="ed365-179">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-179">Entry</span></span> | <span data-ttu-id="ed365-180">值</span><span class="sxs-lookup"><span data-stu-id="ed365-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ed365-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed365-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed365-183">System-Only</span></span>            | <span data-ttu-id="ed365-184">對</span><span class="sxs-lookup"><span data-stu-id="ed365-184">True</span></span>                                             |
| <span data-ttu-id="ed365-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed365-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ed365-186">否</span><span class="sxs-lookup"><span data-stu-id="ed365-186">False</span></span>                                            |
| <span data-ttu-id="ed365-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed365-187">Is Indexed</span></span>             | <span data-ttu-id="ed365-188">否</span><span class="sxs-lookup"><span data-stu-id="ed365-188">False</span></span>                                            |
| <span data-ttu-id="ed365-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed365-189">In Global Catalog</span></span>      | <span data-ttu-id="ed365-190">否</span><span class="sxs-lookup"><span data-stu-id="ed365-190">False</span></span>                                            |
| <span data-ttu-id="ed365-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed365-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed365-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed365-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ed365-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed365-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ed365-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed365-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ed365-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-195">Search-Flags</span></span>           | <span data-ttu-id="ed365-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed365-196">0x00000000</span></span>                                       |
| <span data-ttu-id="ed365-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-197">System-Flags</span></span>           | <span data-ttu-id="ed365-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed365-198">0x00000010</span></span>                                       |
| <span data-ttu-id="ed365-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed365-199">Classes used in</span></span>        | [<span data-ttu-id="ed365-200">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ed365-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ed365-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ed365-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ed365-202">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-202">Entry</span></span> | <span data-ttu-id="ed365-203">值</span><span class="sxs-lookup"><span data-stu-id="ed365-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ed365-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed365-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed365-206">System-Only</span></span>            | <span data-ttu-id="ed365-207">對</span><span class="sxs-lookup"><span data-stu-id="ed365-207">True</span></span>                                             |
| <span data-ttu-id="ed365-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed365-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ed365-209">否</span><span class="sxs-lookup"><span data-stu-id="ed365-209">False</span></span>                                            |
| <span data-ttu-id="ed365-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed365-210">Is Indexed</span></span>             | <span data-ttu-id="ed365-211">否</span><span class="sxs-lookup"><span data-stu-id="ed365-211">False</span></span>                                            |
| <span data-ttu-id="ed365-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed365-212">In Global Catalog</span></span>      | <span data-ttu-id="ed365-213">否</span><span class="sxs-lookup"><span data-stu-id="ed365-213">False</span></span>                                            |
| <span data-ttu-id="ed365-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed365-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed365-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed365-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ed365-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed365-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ed365-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed365-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ed365-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-218">Search-Flags</span></span>           | <span data-ttu-id="ed365-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed365-219">0x00000000</span></span>                                       |
| <span data-ttu-id="ed365-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-220">System-Flags</span></span>           | <span data-ttu-id="ed365-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed365-221">0x00000010</span></span>                                       |
| <span data-ttu-id="ed365-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed365-222">Classes used in</span></span>        | [<span data-ttu-id="ed365-223">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ed365-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ed365-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed365-224">Windows Server 2008</span></span>



| <span data-ttu-id="ed365-225">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-225">Entry</span></span> | <span data-ttu-id="ed365-226">值</span><span class="sxs-lookup"><span data-stu-id="ed365-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ed365-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed365-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed365-229">System-Only</span></span>            | <span data-ttu-id="ed365-230">對</span><span class="sxs-lookup"><span data-stu-id="ed365-230">True</span></span>                                             |
| <span data-ttu-id="ed365-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed365-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ed365-232">否</span><span class="sxs-lookup"><span data-stu-id="ed365-232">False</span></span>                                            |
| <span data-ttu-id="ed365-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed365-233">Is Indexed</span></span>             | <span data-ttu-id="ed365-234">否</span><span class="sxs-lookup"><span data-stu-id="ed365-234">False</span></span>                                            |
| <span data-ttu-id="ed365-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed365-235">In Global Catalog</span></span>      | <span data-ttu-id="ed365-236">否</span><span class="sxs-lookup"><span data-stu-id="ed365-236">False</span></span>                                            |
| <span data-ttu-id="ed365-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed365-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed365-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed365-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ed365-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed365-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ed365-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed365-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ed365-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-241">Search-Flags</span></span>           | <span data-ttu-id="ed365-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed365-242">0x00000000</span></span>                                       |
| <span data-ttu-id="ed365-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-243">System-Flags</span></span>           | <span data-ttu-id="ed365-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed365-244">0x00000010</span></span>                                       |
| <span data-ttu-id="ed365-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed365-245">Classes used in</span></span>        | [<span data-ttu-id="ed365-246">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ed365-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ed365-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed365-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ed365-248">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-248">Entry</span></span> | <span data-ttu-id="ed365-249">值</span><span class="sxs-lookup"><span data-stu-id="ed365-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ed365-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed365-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed365-252">System-Only</span></span>            | <span data-ttu-id="ed365-253">對</span><span class="sxs-lookup"><span data-stu-id="ed365-253">True</span></span>                                             |
| <span data-ttu-id="ed365-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed365-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ed365-255">否</span><span class="sxs-lookup"><span data-stu-id="ed365-255">False</span></span>                                            |
| <span data-ttu-id="ed365-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed365-256">Is Indexed</span></span>             | <span data-ttu-id="ed365-257">否</span><span class="sxs-lookup"><span data-stu-id="ed365-257">False</span></span>                                            |
| <span data-ttu-id="ed365-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed365-258">In Global Catalog</span></span>      | <span data-ttu-id="ed365-259">否</span><span class="sxs-lookup"><span data-stu-id="ed365-259">False</span></span>                                            |
| <span data-ttu-id="ed365-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed365-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed365-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed365-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ed365-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed365-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ed365-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed365-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ed365-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-264">Search-Flags</span></span>           | <span data-ttu-id="ed365-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed365-265">0x00000000</span></span>                                       |
| <span data-ttu-id="ed365-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-266">System-Flags</span></span>           | <span data-ttu-id="ed365-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed365-267">0x00000010</span></span>                                       |
| <span data-ttu-id="ed365-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed365-268">Classes used in</span></span>        | [<span data-ttu-id="ed365-269">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ed365-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ed365-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed365-270">Windows Server 2012</span></span>



| <span data-ttu-id="ed365-271">進入</span><span class="sxs-lookup"><span data-stu-id="ed365-271">Entry</span></span> | <span data-ttu-id="ed365-272">值</span><span class="sxs-lookup"><span data-stu-id="ed365-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ed365-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ed365-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed365-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ed365-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed365-275">System-Only</span></span>            | <span data-ttu-id="ed365-276">對</span><span class="sxs-lookup"><span data-stu-id="ed365-276">True</span></span>                                             |
| <span data-ttu-id="ed365-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ed365-277">Is-Single-Valued</span></span>       | <span data-ttu-id="ed365-278">否</span><span class="sxs-lookup"><span data-stu-id="ed365-278">False</span></span>                                            |
| <span data-ttu-id="ed365-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ed365-279">Is Indexed</span></span>             | <span data-ttu-id="ed365-280">否</span><span class="sxs-lookup"><span data-stu-id="ed365-280">False</span></span>                                            |
| <span data-ttu-id="ed365-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ed365-281">In Global Catalog</span></span>      | <span data-ttu-id="ed365-282">否</span><span class="sxs-lookup"><span data-stu-id="ed365-282">False</span></span>                                            |
| <span data-ttu-id="ed365-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ed365-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed365-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ed365-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ed365-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed365-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ed365-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed365-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ed365-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-287">Search-Flags</span></span>           | <span data-ttu-id="ed365-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed365-288">0x00000000</span></span>                                       |
| <span data-ttu-id="ed365-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed365-289">System-Flags</span></span>           | <span data-ttu-id="ed365-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed365-290">0x00000010</span></span>                                       |
| <span data-ttu-id="ed365-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ed365-291">Classes used in</span></span>        | [<span data-ttu-id="ed365-292">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ed365-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





