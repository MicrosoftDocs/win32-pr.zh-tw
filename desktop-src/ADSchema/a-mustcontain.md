---
title: Must-Contain 屬性
description: 類別的強制屬性清單。 建立類別的實例時，必須指定這些屬性。
ms.assetid: ad112640-0e99-453a-8eff-f964419d8631
ms.tgt_platform: multiple
keywords:
- Must-Contain 屬性 AD 架構
- mustContain 屬性 AD 架構
topic_type:
- apiref
api_name:
- Must-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791468691f438d01161f0d6252f7b995fc0f51e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686972"
---
# <a name="must-contain-attribute"></a><span data-ttu-id="ae95e-106">Must-Contain 屬性</span><span class="sxs-lookup"><span data-stu-id="ae95e-106">Must-Contain attribute</span></span>

<span data-ttu-id="ae95e-107">類別的強制屬性清單。</span><span class="sxs-lookup"><span data-stu-id="ae95e-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="ae95e-108">建立類別的實例時，必須指定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ae95e-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="ae95e-109">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-109">Entry</span></span> | <span data-ttu-id="ae95e-110">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ae95e-111">CN</span><span class="sxs-lookup"><span data-stu-id="ae95e-111">CN</span></span>                | <span data-ttu-id="ae95e-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="ae95e-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="ae95e-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ae95e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ae95e-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="ae95e-114">mustContain</span></span>                                                     |
| <span data-ttu-id="ae95e-115">大小</span><span class="sxs-lookup"><span data-stu-id="ae95e-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="ae95e-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ae95e-116">Update Privilege</span></span>  | <span data-ttu-id="ae95e-117">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="ae95e-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="ae95e-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ae95e-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="ae95e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-119">Attribute-Id</span></span>      | <span data-ttu-id="ae95e-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="ae95e-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="ae95e-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ae95e-121">System-Id-Guid</span></span>    | <span data-ttu-id="ae95e-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ae95e-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="ae95e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae95e-123">Syntax</span></span>            | [<span data-ttu-id="ae95e-124">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="ae95e-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="ae95e-125">實作</span><span class="sxs-lookup"><span data-stu-id="ae95e-125">Implementations</span></span>

-   [<span data-ttu-id="ae95e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ae95e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ae95e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ae95e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ae95e-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="ae95e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ae95e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ae95e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ae95e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ae95e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ae95e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ae95e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ae95e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ae95e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ae95e-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae95e-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ae95e-134">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-134">Entry</span></span> | <span data-ttu-id="ae95e-135">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ae95e-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ae95e-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae95e-138">System-Only</span></span>            | <span data-ttu-id="ae95e-139">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-139">False</span></span>                                            |
| <span data-ttu-id="ae95e-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ae95e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ae95e-141">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-141">False</span></span>                                            |
| <span data-ttu-id="ae95e-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ae95e-142">Is Indexed</span></span>             | <span data-ttu-id="ae95e-143">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-143">False</span></span>                                            |
| <span data-ttu-id="ae95e-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ae95e-144">In Global Catalog</span></span>      | <span data-ttu-id="ae95e-145">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-145">False</span></span>                                            |
| <span data-ttu-id="ae95e-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ae95e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae95e-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ae95e-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ae95e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae95e-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae95e-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-150">Search-Flags</span></span>           | <span data-ttu-id="ae95e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae95e-151">0x00000000</span></span>                                       |
| <span data-ttu-id="ae95e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-152">System-Flags</span></span>           | <span data-ttu-id="ae95e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae95e-153">0x00000010</span></span>                                       |
| <span data-ttu-id="ae95e-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ae95e-154">Classes used in</span></span>        | [<span data-ttu-id="ae95e-155">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ae95e-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ae95e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae95e-156">Windows Server 2003</span></span>



| <span data-ttu-id="ae95e-157">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-157">Entry</span></span> | <span data-ttu-id="ae95e-158">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ae95e-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ae95e-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae95e-161">System-Only</span></span>            | <span data-ttu-id="ae95e-162">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-162">False</span></span>                                            |
| <span data-ttu-id="ae95e-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ae95e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ae95e-164">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-164">False</span></span>                                            |
| <span data-ttu-id="ae95e-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ae95e-165">Is Indexed</span></span>             | <span data-ttu-id="ae95e-166">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-166">False</span></span>                                            |
| <span data-ttu-id="ae95e-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ae95e-167">In Global Catalog</span></span>      | <span data-ttu-id="ae95e-168">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-168">False</span></span>                                            |
| <span data-ttu-id="ae95e-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ae95e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae95e-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ae95e-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ae95e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae95e-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae95e-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-173">Search-Flags</span></span>           | <span data-ttu-id="ae95e-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae95e-174">0x00000000</span></span>                                       |
| <span data-ttu-id="ae95e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-175">System-Flags</span></span>           | <span data-ttu-id="ae95e-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae95e-176">0x00000010</span></span>                                       |
| <span data-ttu-id="ae95e-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ae95e-177">Classes used in</span></span>        | [<span data-ttu-id="ae95e-178">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ae95e-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ae95e-179">亞當</span><span class="sxs-lookup"><span data-stu-id="ae95e-179">ADAM</span></span>



| <span data-ttu-id="ae95e-180">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-180">Entry</span></span> | <span data-ttu-id="ae95e-181">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ae95e-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ae95e-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae95e-184">System-Only</span></span>            | <span data-ttu-id="ae95e-185">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-185">False</span></span>                                            |
| <span data-ttu-id="ae95e-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ae95e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ae95e-187">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-187">False</span></span>                                            |
| <span data-ttu-id="ae95e-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ae95e-188">Is Indexed</span></span>             | <span data-ttu-id="ae95e-189">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-189">False</span></span>                                            |
| <span data-ttu-id="ae95e-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ae95e-190">In Global Catalog</span></span>      | <span data-ttu-id="ae95e-191">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-191">False</span></span>                                            |
| <span data-ttu-id="ae95e-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ae95e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae95e-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ae95e-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ae95e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae95e-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae95e-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-196">Search-Flags</span></span>           | <span data-ttu-id="ae95e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae95e-197">0x00000000</span></span>                                       |
| <span data-ttu-id="ae95e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-198">System-Flags</span></span>           | <span data-ttu-id="ae95e-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae95e-199">0x00000010</span></span>                                       |
| <span data-ttu-id="ae95e-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ae95e-200">Classes used in</span></span>        | [<span data-ttu-id="ae95e-201">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ae95e-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ae95e-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ae95e-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ae95e-203">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-203">Entry</span></span> | <span data-ttu-id="ae95e-204">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ae95e-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ae95e-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae95e-207">System-Only</span></span>            | <span data-ttu-id="ae95e-208">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-208">False</span></span>                                            |
| <span data-ttu-id="ae95e-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ae95e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ae95e-210">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-210">False</span></span>                                            |
| <span data-ttu-id="ae95e-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ae95e-211">Is Indexed</span></span>             | <span data-ttu-id="ae95e-212">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-212">False</span></span>                                            |
| <span data-ttu-id="ae95e-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ae95e-213">In Global Catalog</span></span>      | <span data-ttu-id="ae95e-214">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-214">False</span></span>                                            |
| <span data-ttu-id="ae95e-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ae95e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae95e-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ae95e-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ae95e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae95e-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae95e-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-219">Search-Flags</span></span>           | <span data-ttu-id="ae95e-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae95e-220">0x00000000</span></span>                                       |
| <span data-ttu-id="ae95e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-221">System-Flags</span></span>           | <span data-ttu-id="ae95e-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae95e-222">0x00000010</span></span>                                       |
| <span data-ttu-id="ae95e-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ae95e-223">Classes used in</span></span>        | [<span data-ttu-id="ae95e-224">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ae95e-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ae95e-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae95e-225">Windows Server 2008</span></span>



| <span data-ttu-id="ae95e-226">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-226">Entry</span></span> | <span data-ttu-id="ae95e-227">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ae95e-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ae95e-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae95e-230">System-Only</span></span>            | <span data-ttu-id="ae95e-231">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-231">False</span></span>                                            |
| <span data-ttu-id="ae95e-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ae95e-232">Is-Single-Valued</span></span>       | <span data-ttu-id="ae95e-233">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-233">False</span></span>                                            |
| <span data-ttu-id="ae95e-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ae95e-234">Is Indexed</span></span>             | <span data-ttu-id="ae95e-235">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-235">False</span></span>                                            |
| <span data-ttu-id="ae95e-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ae95e-236">In Global Catalog</span></span>      | <span data-ttu-id="ae95e-237">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-237">False</span></span>                                            |
| <span data-ttu-id="ae95e-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ae95e-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae95e-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ae95e-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ae95e-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae95e-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae95e-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-242">Search-Flags</span></span>           | <span data-ttu-id="ae95e-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae95e-243">0x00000000</span></span>                                       |
| <span data-ttu-id="ae95e-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-244">System-Flags</span></span>           | <span data-ttu-id="ae95e-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae95e-245">0x00000010</span></span>                                       |
| <span data-ttu-id="ae95e-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ae95e-246">Classes used in</span></span>        | [<span data-ttu-id="ae95e-247">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ae95e-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ae95e-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae95e-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ae95e-249">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-249">Entry</span></span> | <span data-ttu-id="ae95e-250">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ae95e-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ae95e-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae95e-253">System-Only</span></span>            | <span data-ttu-id="ae95e-254">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-254">False</span></span>                                            |
| <span data-ttu-id="ae95e-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ae95e-255">Is-Single-Valued</span></span>       | <span data-ttu-id="ae95e-256">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-256">False</span></span>                                            |
| <span data-ttu-id="ae95e-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ae95e-257">Is Indexed</span></span>             | <span data-ttu-id="ae95e-258">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-258">False</span></span>                                            |
| <span data-ttu-id="ae95e-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ae95e-259">In Global Catalog</span></span>      | <span data-ttu-id="ae95e-260">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-260">False</span></span>                                            |
| <span data-ttu-id="ae95e-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ae95e-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae95e-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ae95e-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ae95e-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae95e-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae95e-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-265">Search-Flags</span></span>           | <span data-ttu-id="ae95e-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae95e-266">0x00000000</span></span>                                       |
| <span data-ttu-id="ae95e-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-267">System-Flags</span></span>           | <span data-ttu-id="ae95e-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae95e-268">0x00000010</span></span>                                       |
| <span data-ttu-id="ae95e-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ae95e-269">Classes used in</span></span>        | [<span data-ttu-id="ae95e-270">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ae95e-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ae95e-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae95e-271">Windows Server 2012</span></span>



| <span data-ttu-id="ae95e-272">進入</span><span class="sxs-lookup"><span data-stu-id="ae95e-272">Entry</span></span> | <span data-ttu-id="ae95e-273">值</span><span class="sxs-lookup"><span data-stu-id="ae95e-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ae95e-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ae95e-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae95e-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ae95e-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae95e-276">System-Only</span></span>            | <span data-ttu-id="ae95e-277">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-277">False</span></span>                                            |
| <span data-ttu-id="ae95e-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ae95e-278">Is-Single-Valued</span></span>       | <span data-ttu-id="ae95e-279">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-279">False</span></span>                                            |
| <span data-ttu-id="ae95e-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ae95e-280">Is Indexed</span></span>             | <span data-ttu-id="ae95e-281">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-281">False</span></span>                                            |
| <span data-ttu-id="ae95e-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ae95e-282">In Global Catalog</span></span>      | <span data-ttu-id="ae95e-283">否</span><span class="sxs-lookup"><span data-stu-id="ae95e-283">False</span></span>                                            |
| <span data-ttu-id="ae95e-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ae95e-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae95e-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ae95e-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ae95e-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae95e-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae95e-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ae95e-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-288">Search-Flags</span></span>           | <span data-ttu-id="ae95e-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae95e-289">0x00000000</span></span>                                       |
| <span data-ttu-id="ae95e-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae95e-290">System-Flags</span></span>           | <span data-ttu-id="ae95e-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae95e-291">0x00000010</span></span>                                       |
| <span data-ttu-id="ae95e-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ae95e-292">Classes used in</span></span>        | [<span data-ttu-id="ae95e-293">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="ae95e-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





