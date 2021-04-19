---
title: RDN-Att-ID 屬性
description: 用來命名類別之屬性的 RDN。
ms.assetid: 793199c4-6c5e-481f-8f73-bd59375ab51b
ms.tgt_platform: multiple
keywords:
- RDN-Att-ID 屬性 AD 架構
- rDNAttID 屬性 AD 架構
topic_type:
- apiref
api_name:
- RDN-Att-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b5fb573d289b71bb459cd8595b5df5115f42bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970030"
---
# <a name="rdn-att-id-attribute"></a><span data-ttu-id="f3639-105">RDN-Att-ID 屬性</span><span class="sxs-lookup"><span data-stu-id="f3639-105">RDN-Att-ID attribute</span></span>

<span data-ttu-id="f3639-106">用來命名類別之屬性的 RDN。</span><span class="sxs-lookup"><span data-stu-id="f3639-106">The RDN for the attribute that is used to name a class.</span></span>



| <span data-ttu-id="f3639-107">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-107">Entry</span></span> | <span data-ttu-id="f3639-108">值</span><span class="sxs-lookup"><span data-stu-id="f3639-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f3639-109">CN</span><span class="sxs-lookup"><span data-stu-id="f3639-109">CN</span></span>                | <span data-ttu-id="f3639-110">RDN-Att-ID</span><span class="sxs-lookup"><span data-stu-id="f3639-110">RDN-Att-ID</span></span>                                                      |
| <span data-ttu-id="f3639-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f3639-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f3639-112">rDNAttID</span><span class="sxs-lookup"><span data-stu-id="f3639-112">rDNAttID</span></span>                                                        |
| <span data-ttu-id="f3639-113">大小</span><span class="sxs-lookup"><span data-stu-id="f3639-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="f3639-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f3639-114">Update Privilege</span></span>  | <span data-ttu-id="f3639-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="f3639-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="f3639-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f3639-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="f3639-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-117">Attribute-Id</span></span>      | <span data-ttu-id="f3639-118">1.2.840.113556.1.2.26</span><span class="sxs-lookup"><span data-stu-id="f3639-118">1.2.840.113556.1.2.26</span></span>                                           |
| <span data-ttu-id="f3639-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f3639-119">System-Id-Guid</span></span>    | <span data-ttu-id="f3639-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f3639-120">bf967a0f-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="f3639-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3639-121">Syntax</span></span>            | [<span data-ttu-id="f3639-122">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="f3639-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="f3639-123">實作</span><span class="sxs-lookup"><span data-stu-id="f3639-123">Implementations</span></span>

-   [<span data-ttu-id="f3639-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3639-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3639-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3639-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3639-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f3639-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f3639-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3639-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3639-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3639-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3639-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3639-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3639-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3639-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3639-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3639-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f3639-132">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-132">Entry</span></span> | <span data-ttu-id="f3639-133">值</span><span class="sxs-lookup"><span data-stu-id="f3639-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3639-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f3639-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3639-136">System-Only</span></span>            | <span data-ttu-id="f3639-137">對</span><span class="sxs-lookup"><span data-stu-id="f3639-137">True</span></span>                                             |
| <span data-ttu-id="f3639-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f3639-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f3639-139">對</span><span class="sxs-lookup"><span data-stu-id="f3639-139">True</span></span>                                             |
| <span data-ttu-id="f3639-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f3639-140">Is Indexed</span></span>             | <span data-ttu-id="f3639-141">否</span><span class="sxs-lookup"><span data-stu-id="f3639-141">False</span></span>                                            |
| <span data-ttu-id="f3639-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f3639-142">In Global Catalog</span></span>      | <span data-ttu-id="f3639-143">否</span><span class="sxs-lookup"><span data-stu-id="f3639-143">False</span></span>                                            |
| <span data-ttu-id="f3639-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f3639-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3639-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f3639-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3639-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3639-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3639-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3639-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3639-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-148">Search-Flags</span></span>           | <span data-ttu-id="f3639-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3639-149">0x00000000</span></span>                                       |
| <span data-ttu-id="f3639-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-150">System-Flags</span></span>           | <span data-ttu-id="f3639-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3639-151">0x00000010</span></span>                                       |
| <span data-ttu-id="f3639-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f3639-152">Classes used in</span></span>        | [<span data-ttu-id="f3639-153">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="f3639-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3639-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3639-154">Windows Server 2003</span></span>



| <span data-ttu-id="f3639-155">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-155">Entry</span></span> | <span data-ttu-id="f3639-156">值</span><span class="sxs-lookup"><span data-stu-id="f3639-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3639-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f3639-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3639-159">System-Only</span></span>            | <span data-ttu-id="f3639-160">對</span><span class="sxs-lookup"><span data-stu-id="f3639-160">True</span></span>                                             |
| <span data-ttu-id="f3639-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f3639-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f3639-162">對</span><span class="sxs-lookup"><span data-stu-id="f3639-162">True</span></span>                                             |
| <span data-ttu-id="f3639-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f3639-163">Is Indexed</span></span>             | <span data-ttu-id="f3639-164">否</span><span class="sxs-lookup"><span data-stu-id="f3639-164">False</span></span>                                            |
| <span data-ttu-id="f3639-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f3639-165">In Global Catalog</span></span>      | <span data-ttu-id="f3639-166">否</span><span class="sxs-lookup"><span data-stu-id="f3639-166">False</span></span>                                            |
| <span data-ttu-id="f3639-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f3639-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3639-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f3639-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3639-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3639-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3639-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3639-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3639-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-171">Search-Flags</span></span>           | <span data-ttu-id="f3639-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3639-172">0x00000000</span></span>                                       |
| <span data-ttu-id="f3639-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-173">System-Flags</span></span>           | <span data-ttu-id="f3639-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3639-174">0x00000010</span></span>                                       |
| <span data-ttu-id="f3639-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f3639-175">Classes used in</span></span>        | [<span data-ttu-id="f3639-176">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="f3639-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f3639-177">亞當</span><span class="sxs-lookup"><span data-stu-id="f3639-177">ADAM</span></span>



| <span data-ttu-id="f3639-178">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-178">Entry</span></span> | <span data-ttu-id="f3639-179">值</span><span class="sxs-lookup"><span data-stu-id="f3639-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3639-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f3639-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3639-182">System-Only</span></span>            | <span data-ttu-id="f3639-183">對</span><span class="sxs-lookup"><span data-stu-id="f3639-183">True</span></span>                                             |
| <span data-ttu-id="f3639-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f3639-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f3639-185">對</span><span class="sxs-lookup"><span data-stu-id="f3639-185">True</span></span>                                             |
| <span data-ttu-id="f3639-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f3639-186">Is Indexed</span></span>             | <span data-ttu-id="f3639-187">否</span><span class="sxs-lookup"><span data-stu-id="f3639-187">False</span></span>                                            |
| <span data-ttu-id="f3639-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f3639-188">In Global Catalog</span></span>      | <span data-ttu-id="f3639-189">否</span><span class="sxs-lookup"><span data-stu-id="f3639-189">False</span></span>                                            |
| <span data-ttu-id="f3639-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f3639-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3639-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f3639-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3639-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3639-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3639-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3639-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3639-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-194">Search-Flags</span></span>           | <span data-ttu-id="f3639-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3639-195">0x00000000</span></span>                                       |
| <span data-ttu-id="f3639-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-196">System-Flags</span></span>           | <span data-ttu-id="f3639-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3639-197">0x00000010</span></span>                                       |
| <span data-ttu-id="f3639-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f3639-198">Classes used in</span></span>        | [<span data-ttu-id="f3639-199">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="f3639-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3639-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3639-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3639-201">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-201">Entry</span></span> | <span data-ttu-id="f3639-202">值</span><span class="sxs-lookup"><span data-stu-id="f3639-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3639-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f3639-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3639-205">System-Only</span></span>            | <span data-ttu-id="f3639-206">對</span><span class="sxs-lookup"><span data-stu-id="f3639-206">True</span></span>                                             |
| <span data-ttu-id="f3639-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f3639-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f3639-208">對</span><span class="sxs-lookup"><span data-stu-id="f3639-208">True</span></span>                                             |
| <span data-ttu-id="f3639-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f3639-209">Is Indexed</span></span>             | <span data-ttu-id="f3639-210">否</span><span class="sxs-lookup"><span data-stu-id="f3639-210">False</span></span>                                            |
| <span data-ttu-id="f3639-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f3639-211">In Global Catalog</span></span>      | <span data-ttu-id="f3639-212">否</span><span class="sxs-lookup"><span data-stu-id="f3639-212">False</span></span>                                            |
| <span data-ttu-id="f3639-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f3639-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3639-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f3639-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3639-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3639-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3639-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3639-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3639-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-217">Search-Flags</span></span>           | <span data-ttu-id="f3639-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3639-218">0x00000000</span></span>                                       |
| <span data-ttu-id="f3639-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-219">System-Flags</span></span>           | <span data-ttu-id="f3639-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3639-220">0x00000010</span></span>                                       |
| <span data-ttu-id="f3639-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f3639-221">Classes used in</span></span>        | [<span data-ttu-id="f3639-222">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="f3639-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3639-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3639-223">Windows Server 2008</span></span>



| <span data-ttu-id="f3639-224">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-224">Entry</span></span> | <span data-ttu-id="f3639-225">值</span><span class="sxs-lookup"><span data-stu-id="f3639-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3639-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f3639-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3639-228">System-Only</span></span>            | <span data-ttu-id="f3639-229">對</span><span class="sxs-lookup"><span data-stu-id="f3639-229">True</span></span>                                             |
| <span data-ttu-id="f3639-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f3639-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f3639-231">對</span><span class="sxs-lookup"><span data-stu-id="f3639-231">True</span></span>                                             |
| <span data-ttu-id="f3639-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f3639-232">Is Indexed</span></span>             | <span data-ttu-id="f3639-233">否</span><span class="sxs-lookup"><span data-stu-id="f3639-233">False</span></span>                                            |
| <span data-ttu-id="f3639-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f3639-234">In Global Catalog</span></span>      | <span data-ttu-id="f3639-235">否</span><span class="sxs-lookup"><span data-stu-id="f3639-235">False</span></span>                                            |
| <span data-ttu-id="f3639-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f3639-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3639-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f3639-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3639-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3639-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3639-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3639-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3639-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-240">Search-Flags</span></span>           | <span data-ttu-id="f3639-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3639-241">0x00000000</span></span>                                       |
| <span data-ttu-id="f3639-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-242">System-Flags</span></span>           | <span data-ttu-id="f3639-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3639-243">0x00000010</span></span>                                       |
| <span data-ttu-id="f3639-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f3639-244">Classes used in</span></span>        | [<span data-ttu-id="f3639-245">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="f3639-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3639-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3639-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3639-247">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-247">Entry</span></span> | <span data-ttu-id="f3639-248">值</span><span class="sxs-lookup"><span data-stu-id="f3639-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3639-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f3639-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3639-251">System-Only</span></span>            | <span data-ttu-id="f3639-252">對</span><span class="sxs-lookup"><span data-stu-id="f3639-252">True</span></span>                                             |
| <span data-ttu-id="f3639-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f3639-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f3639-254">對</span><span class="sxs-lookup"><span data-stu-id="f3639-254">True</span></span>                                             |
| <span data-ttu-id="f3639-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f3639-255">Is Indexed</span></span>             | <span data-ttu-id="f3639-256">否</span><span class="sxs-lookup"><span data-stu-id="f3639-256">False</span></span>                                            |
| <span data-ttu-id="f3639-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f3639-257">In Global Catalog</span></span>      | <span data-ttu-id="f3639-258">否</span><span class="sxs-lookup"><span data-stu-id="f3639-258">False</span></span>                                            |
| <span data-ttu-id="f3639-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f3639-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3639-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f3639-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3639-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3639-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3639-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3639-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3639-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-263">Search-Flags</span></span>           | <span data-ttu-id="f3639-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3639-264">0x00000000</span></span>                                       |
| <span data-ttu-id="f3639-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-265">System-Flags</span></span>           | <span data-ttu-id="f3639-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3639-266">0x00000010</span></span>                                       |
| <span data-ttu-id="f3639-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f3639-267">Classes used in</span></span>        | [<span data-ttu-id="f3639-268">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="f3639-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3639-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3639-269">Windows Server 2012</span></span>



| <span data-ttu-id="f3639-270">進入</span><span class="sxs-lookup"><span data-stu-id="f3639-270">Entry</span></span> | <span data-ttu-id="f3639-271">值</span><span class="sxs-lookup"><span data-stu-id="f3639-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="f3639-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f3639-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3639-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="f3639-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3639-274">System-Only</span></span>            | <span data-ttu-id="f3639-275">對</span><span class="sxs-lookup"><span data-stu-id="f3639-275">True</span></span>                                             |
| <span data-ttu-id="f3639-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f3639-276">Is-Single-Valued</span></span>       | <span data-ttu-id="f3639-277">對</span><span class="sxs-lookup"><span data-stu-id="f3639-277">True</span></span>                                             |
| <span data-ttu-id="f3639-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f3639-278">Is Indexed</span></span>             | <span data-ttu-id="f3639-279">否</span><span class="sxs-lookup"><span data-stu-id="f3639-279">False</span></span>                                            |
| <span data-ttu-id="f3639-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f3639-280">In Global Catalog</span></span>      | <span data-ttu-id="f3639-281">否</span><span class="sxs-lookup"><span data-stu-id="f3639-281">False</span></span>                                            |
| <span data-ttu-id="f3639-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f3639-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3639-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f3639-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="f3639-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3639-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="f3639-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3639-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="f3639-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-286">Search-Flags</span></span>           | <span data-ttu-id="f3639-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3639-287">0x00000000</span></span>                                       |
| <span data-ttu-id="f3639-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3639-288">System-Flags</span></span>           | <span data-ttu-id="f3639-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3639-289">0x00000010</span></span>                                       |
| <span data-ttu-id="f3639-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f3639-290">Classes used in</span></span>        | [<span data-ttu-id="f3639-291">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="f3639-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





