---
title: 屬性 ID 屬性
description: 用來識別屬性的唯一 X.x OID。
ms.assetid: e1cdf94b-9bb6-4cff-8555-da4cc9600174
ms.tgt_platform: multiple
keywords:
- 屬性 ID 屬性 AD 架構
- attributeID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Attribute-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5fc99dee7d25b7e3fd20ca7bd27598c4531f91a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971065"
---
# <a name="attribute-id-attribute"></a><span data-ttu-id="1b3bc-105">屬性 ID 屬性</span><span class="sxs-lookup"><span data-stu-id="1b3bc-105">Attribute-ID attribute</span></span>

<span data-ttu-id="1b3bc-106">用來識別屬性的唯一 X.x OID。</span><span class="sxs-lookup"><span data-stu-id="1b3bc-106">The unique X.500 OID for identifying an attribute.</span></span>



| <span data-ttu-id="1b3bc-107">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-107">Entry</span></span> | <span data-ttu-id="1b3bc-108">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1b3bc-109">CN</span><span class="sxs-lookup"><span data-stu-id="1b3bc-109">CN</span></span>                | <span data-ttu-id="1b3bc-110">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-110">Attribute-ID</span></span>                                                    |
| <span data-ttu-id="1b3bc-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1b3bc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1b3bc-112">attributeID</span><span class="sxs-lookup"><span data-stu-id="1b3bc-112">attributeID</span></span>                                                     |
| <span data-ttu-id="1b3bc-113">大小</span><span class="sxs-lookup"><span data-stu-id="1b3bc-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="1b3bc-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1b3bc-114">Update Privilege</span></span>  | <span data-ttu-id="1b3bc-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="1b3bc-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="1b3bc-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1b3bc-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="1b3bc-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-117">Attribute-Id</span></span>      | <span data-ttu-id="1b3bc-118">1.2.840.113556.1.2.30</span><span class="sxs-lookup"><span data-stu-id="1b3bc-118">1.2.840.113556.1.2.30</span></span>                                           |
| <span data-ttu-id="1b3bc-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1b3bc-119">System-Id-Guid</span></span>    | <span data-ttu-id="1b3bc-120">bf967922-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1b3bc-120">bf967922-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="1b3bc-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b3bc-121">Syntax</span></span>            | [<span data-ttu-id="1b3bc-122">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="1b3bc-123">實作</span><span class="sxs-lookup"><span data-stu-id="1b3bc-123">Implementations</span></span>

-   [<span data-ttu-id="1b3bc-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1b3bc-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b3bc-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1b3bc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b3bc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b3bc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b3bc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1b3bc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b3bc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1b3bc-132">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-132">Entry</span></span> | <span data-ttu-id="1b3bc-133">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="1b3bc-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b3bc-136">System-Only</span></span>            | <span data-ttu-id="1b3bc-137">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-137">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1b3bc-139">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-139">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1b3bc-140">Is Indexed</span></span>             | <span data-ttu-id="1b3bc-141">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-141">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1b3bc-142">In Global Catalog</span></span>      | <span data-ttu-id="1b3bc-143">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-143">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1b3bc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b3bc-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1b3bc-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="1b3bc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b3bc-146">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b3bc-147">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-148">Search-Flags</span></span>           | <span data-ttu-id="1b3bc-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-149">0x00000008</span></span>                                               |
| <span data-ttu-id="1b3bc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-150">System-Flags</span></span>           | <span data-ttu-id="1b3bc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b3bc-151">0x00000010</span></span>                                               |
| <span data-ttu-id="1b3bc-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1b3bc-152">Classes used in</span></span>        | [<span data-ttu-id="1b3bc-153">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1b3bc-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b3bc-154">Windows Server 2003</span></span>



| <span data-ttu-id="1b3bc-155">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-155">Entry</span></span> | <span data-ttu-id="1b3bc-156">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-156">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="1b3bc-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-157">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-158">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b3bc-159">System-Only</span></span>            | <span data-ttu-id="1b3bc-160">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-160">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1b3bc-162">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-162">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1b3bc-163">Is Indexed</span></span>             | <span data-ttu-id="1b3bc-164">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-164">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1b3bc-165">In Global Catalog</span></span>      | <span data-ttu-id="1b3bc-166">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-166">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1b3bc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b3bc-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1b3bc-168">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="1b3bc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b3bc-169">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b3bc-170">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-171">Search-Flags</span></span>           | <span data-ttu-id="1b3bc-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-172">0x00000008</span></span>                                               |
| <span data-ttu-id="1b3bc-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-173">System-Flags</span></span>           | <span data-ttu-id="1b3bc-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b3bc-174">0x00000010</span></span>                                               |
| <span data-ttu-id="1b3bc-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1b3bc-175">Classes used in</span></span>        | [<span data-ttu-id="1b3bc-176">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-176">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1b3bc-177">亞當</span><span class="sxs-lookup"><span data-stu-id="1b3bc-177">ADAM</span></span>



| <span data-ttu-id="1b3bc-178">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-178">Entry</span></span> | <span data-ttu-id="1b3bc-179">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-179">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="1b3bc-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-180">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-181">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b3bc-182">System-Only</span></span>            | <span data-ttu-id="1b3bc-183">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-183">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1b3bc-185">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-185">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1b3bc-186">Is Indexed</span></span>             | <span data-ttu-id="1b3bc-187">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-187">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1b3bc-188">In Global Catalog</span></span>      | <span data-ttu-id="1b3bc-189">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-189">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1b3bc-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b3bc-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1b3bc-191">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="1b3bc-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b3bc-192">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b3bc-193">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-194">Search-Flags</span></span>           | <span data-ttu-id="1b3bc-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-195">0x00000008</span></span>                                               |
| <span data-ttu-id="1b3bc-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-196">System-Flags</span></span>           | <span data-ttu-id="1b3bc-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b3bc-197">0x00000010</span></span>                                               |
| <span data-ttu-id="1b3bc-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1b3bc-198">Classes used in</span></span>        | [<span data-ttu-id="1b3bc-199">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-199">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b3bc-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b3bc-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b3bc-201">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-201">Entry</span></span> | <span data-ttu-id="1b3bc-202">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-202">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="1b3bc-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-203">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-204">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b3bc-205">System-Only</span></span>            | <span data-ttu-id="1b3bc-206">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-206">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1b3bc-208">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-208">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1b3bc-209">Is Indexed</span></span>             | <span data-ttu-id="1b3bc-210">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-210">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1b3bc-211">In Global Catalog</span></span>      | <span data-ttu-id="1b3bc-212">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-212">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1b3bc-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b3bc-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1b3bc-214">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="1b3bc-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b3bc-215">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b3bc-216">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-217">Search-Flags</span></span>           | <span data-ttu-id="1b3bc-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-218">0x00000008</span></span>                                               |
| <span data-ttu-id="1b3bc-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-219">System-Flags</span></span>           | <span data-ttu-id="1b3bc-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b3bc-220">0x00000010</span></span>                                               |
| <span data-ttu-id="1b3bc-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1b3bc-221">Classes used in</span></span>        | [<span data-ttu-id="1b3bc-222">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-222">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b3bc-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-223">Windows Server 2008</span></span>



| <span data-ttu-id="1b3bc-224">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-224">Entry</span></span> | <span data-ttu-id="1b3bc-225">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-225">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="1b3bc-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-226">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-227">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b3bc-228">System-Only</span></span>            | <span data-ttu-id="1b3bc-229">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-229">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1b3bc-231">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-231">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1b3bc-232">Is Indexed</span></span>             | <span data-ttu-id="1b3bc-233">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-233">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1b3bc-234">In Global Catalog</span></span>      | <span data-ttu-id="1b3bc-235">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-235">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1b3bc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b3bc-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1b3bc-237">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="1b3bc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b3bc-238">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b3bc-239">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-240">Search-Flags</span></span>           | <span data-ttu-id="1b3bc-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-241">0x00000008</span></span>                                               |
| <span data-ttu-id="1b3bc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-242">System-Flags</span></span>           | <span data-ttu-id="1b3bc-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b3bc-243">0x00000010</span></span>                                               |
| <span data-ttu-id="1b3bc-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1b3bc-244">Classes used in</span></span>        | [<span data-ttu-id="1b3bc-245">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-245">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b3bc-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b3bc-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b3bc-247">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-247">Entry</span></span> | <span data-ttu-id="1b3bc-248">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-248">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="1b3bc-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-249">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-250">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b3bc-251">System-Only</span></span>            | <span data-ttu-id="1b3bc-252">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-252">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1b3bc-254">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-254">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1b3bc-255">Is Indexed</span></span>             | <span data-ttu-id="1b3bc-256">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-256">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1b3bc-257">In Global Catalog</span></span>      | <span data-ttu-id="1b3bc-258">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-258">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1b3bc-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b3bc-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1b3bc-260">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="1b3bc-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b3bc-261">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b3bc-262">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-263">Search-Flags</span></span>           | <span data-ttu-id="1b3bc-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-264">0x00000008</span></span>                                               |
| <span data-ttu-id="1b3bc-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-265">System-Flags</span></span>           | <span data-ttu-id="1b3bc-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b3bc-266">0x00000010</span></span>                                               |
| <span data-ttu-id="1b3bc-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1b3bc-267">Classes used in</span></span>        | [<span data-ttu-id="1b3bc-268">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-268">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b3bc-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b3bc-269">Windows Server 2012</span></span>



| <span data-ttu-id="1b3bc-270">進入</span><span class="sxs-lookup"><span data-stu-id="1b3bc-270">Entry</span></span> | <span data-ttu-id="1b3bc-271">值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-271">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="1b3bc-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1b3bc-272">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b3bc-273">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="1b3bc-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b3bc-274">System-Only</span></span>            | <span data-ttu-id="1b3bc-275">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-275">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1b3bc-276">Is-Single-Valued</span></span>       | <span data-ttu-id="1b3bc-277">對</span><span class="sxs-lookup"><span data-stu-id="1b3bc-277">True</span></span>                                                     |
| <span data-ttu-id="1b3bc-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1b3bc-278">Is Indexed</span></span>             | <span data-ttu-id="1b3bc-279">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-279">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1b3bc-280">In Global Catalog</span></span>      | <span data-ttu-id="1b3bc-281">否</span><span class="sxs-lookup"><span data-stu-id="1b3bc-281">False</span></span>                                                    |
| <span data-ttu-id="1b3bc-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1b3bc-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b3bc-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1b3bc-283">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="1b3bc-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b3bc-284">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b3bc-285">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="1b3bc-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-286">Search-Flags</span></span>           | <span data-ttu-id="1b3bc-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1b3bc-287">0x00000008</span></span>                                               |
| <span data-ttu-id="1b3bc-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b3bc-288">System-Flags</span></span>           | <span data-ttu-id="1b3bc-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b3bc-289">0x00000010</span></span>                                               |
| <span data-ttu-id="1b3bc-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1b3bc-290">Classes used in</span></span>        | [<span data-ttu-id="1b3bc-291">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="1b3bc-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





