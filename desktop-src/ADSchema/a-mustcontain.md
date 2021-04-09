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
# <a name="must-contain-attribute"></a><span data-ttu-id="e8e70-106">Must-Contain 屬性</span><span class="sxs-lookup"><span data-stu-id="e8e70-106">Must-Contain attribute</span></span>

<span data-ttu-id="e8e70-107">類別的強制屬性清單。</span><span class="sxs-lookup"><span data-stu-id="e8e70-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="e8e70-108">建立類別的實例時，必須指定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e8e70-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="e8e70-109">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-109">Entry</span></span> | <span data-ttu-id="e8e70-110">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="e8e70-111">CN</span><span class="sxs-lookup"><span data-stu-id="e8e70-111">CN</span></span>                | <span data-ttu-id="e8e70-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="e8e70-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="e8e70-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e8e70-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e8e70-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="e8e70-114">mustContain</span></span>                                                     |
| <span data-ttu-id="e8e70-115">大小</span><span class="sxs-lookup"><span data-stu-id="e8e70-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="e8e70-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e8e70-116">Update Privilege</span></span>  | <span data-ttu-id="e8e70-117">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="e8e70-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="e8e70-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e8e70-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="e8e70-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-119">Attribute-Id</span></span>      | <span data-ttu-id="e8e70-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="e8e70-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="e8e70-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e8e70-121">System-Id-Guid</span></span>    | <span data-ttu-id="e8e70-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e8e70-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="e8e70-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8e70-123">Syntax</span></span>            | [<span data-ttu-id="e8e70-124">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="e8e70-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="e8e70-125">實作</span><span class="sxs-lookup"><span data-stu-id="e8e70-125">Implementations</span></span>

-   [<span data-ttu-id="e8e70-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e8e70-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e8e70-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8e70-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8e70-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e8e70-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e8e70-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8e70-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8e70-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8e70-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8e70-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8e70-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8e70-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8e70-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e8e70-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e8e70-133">Windows 2000 Server</span></span>



| <span data-ttu-id="e8e70-134">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-134">Entry</span></span> | <span data-ttu-id="e8e70-135">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8e70-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e70-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8e70-138">System-Only</span></span>            | <span data-ttu-id="e8e70-139">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-139">False</span></span>                                            |
| <span data-ttu-id="e8e70-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8e70-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e8e70-141">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-141">False</span></span>                                            |
| <span data-ttu-id="e8e70-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8e70-142">Is Indexed</span></span>             | <span data-ttu-id="e8e70-143">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-143">False</span></span>                                            |
| <span data-ttu-id="e8e70-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8e70-144">In Global Catalog</span></span>      | <span data-ttu-id="e8e70-145">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-145">False</span></span>                                            |
| <span data-ttu-id="e8e70-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8e70-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8e70-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8e70-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8e70-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8e70-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8e70-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-150">Search-Flags</span></span>           | <span data-ttu-id="e8e70-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8e70-151">0x00000000</span></span>                                       |
| <span data-ttu-id="e8e70-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-152">System-Flags</span></span>           | <span data-ttu-id="e8e70-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8e70-153">0x00000010</span></span>                                       |
| <span data-ttu-id="e8e70-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8e70-154">Classes used in</span></span>        | [<span data-ttu-id="e8e70-155">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="e8e70-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e8e70-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8e70-156">Windows Server 2003</span></span>



| <span data-ttu-id="e8e70-157">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-157">Entry</span></span> | <span data-ttu-id="e8e70-158">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8e70-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e70-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8e70-161">System-Only</span></span>            | <span data-ttu-id="e8e70-162">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-162">False</span></span>                                            |
| <span data-ttu-id="e8e70-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8e70-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e8e70-164">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-164">False</span></span>                                            |
| <span data-ttu-id="e8e70-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8e70-165">Is Indexed</span></span>             | <span data-ttu-id="e8e70-166">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-166">False</span></span>                                            |
| <span data-ttu-id="e8e70-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8e70-167">In Global Catalog</span></span>      | <span data-ttu-id="e8e70-168">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-168">False</span></span>                                            |
| <span data-ttu-id="e8e70-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8e70-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8e70-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8e70-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8e70-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8e70-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8e70-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-173">Search-Flags</span></span>           | <span data-ttu-id="e8e70-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8e70-174">0x00000000</span></span>                                       |
| <span data-ttu-id="e8e70-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-175">System-Flags</span></span>           | <span data-ttu-id="e8e70-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8e70-176">0x00000010</span></span>                                       |
| <span data-ttu-id="e8e70-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8e70-177">Classes used in</span></span>        | [<span data-ttu-id="e8e70-178">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="e8e70-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e8e70-179">亞當</span><span class="sxs-lookup"><span data-stu-id="e8e70-179">ADAM</span></span>



| <span data-ttu-id="e8e70-180">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-180">Entry</span></span> | <span data-ttu-id="e8e70-181">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8e70-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e70-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8e70-184">System-Only</span></span>            | <span data-ttu-id="e8e70-185">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-185">False</span></span>                                            |
| <span data-ttu-id="e8e70-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8e70-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e8e70-187">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-187">False</span></span>                                            |
| <span data-ttu-id="e8e70-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8e70-188">Is Indexed</span></span>             | <span data-ttu-id="e8e70-189">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-189">False</span></span>                                            |
| <span data-ttu-id="e8e70-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8e70-190">In Global Catalog</span></span>      | <span data-ttu-id="e8e70-191">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-191">False</span></span>                                            |
| <span data-ttu-id="e8e70-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8e70-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8e70-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8e70-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8e70-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8e70-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8e70-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-196">Search-Flags</span></span>           | <span data-ttu-id="e8e70-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8e70-197">0x00000000</span></span>                                       |
| <span data-ttu-id="e8e70-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-198">System-Flags</span></span>           | <span data-ttu-id="e8e70-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8e70-199">0x00000010</span></span>                                       |
| <span data-ttu-id="e8e70-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8e70-200">Classes used in</span></span>        | [<span data-ttu-id="e8e70-201">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="e8e70-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8e70-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8e70-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8e70-203">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-203">Entry</span></span> | <span data-ttu-id="e8e70-204">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8e70-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e70-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8e70-207">System-Only</span></span>            | <span data-ttu-id="e8e70-208">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-208">False</span></span>                                            |
| <span data-ttu-id="e8e70-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8e70-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e8e70-210">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-210">False</span></span>                                            |
| <span data-ttu-id="e8e70-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8e70-211">Is Indexed</span></span>             | <span data-ttu-id="e8e70-212">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-212">False</span></span>                                            |
| <span data-ttu-id="e8e70-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8e70-213">In Global Catalog</span></span>      | <span data-ttu-id="e8e70-214">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-214">False</span></span>                                            |
| <span data-ttu-id="e8e70-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8e70-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8e70-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8e70-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8e70-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8e70-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8e70-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-219">Search-Flags</span></span>           | <span data-ttu-id="e8e70-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8e70-220">0x00000000</span></span>                                       |
| <span data-ttu-id="e8e70-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-221">System-Flags</span></span>           | <span data-ttu-id="e8e70-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8e70-222">0x00000010</span></span>                                       |
| <span data-ttu-id="e8e70-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8e70-223">Classes used in</span></span>        | [<span data-ttu-id="e8e70-224">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="e8e70-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8e70-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8e70-225">Windows Server 2008</span></span>



| <span data-ttu-id="e8e70-226">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-226">Entry</span></span> | <span data-ttu-id="e8e70-227">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8e70-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e70-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8e70-230">System-Only</span></span>            | <span data-ttu-id="e8e70-231">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-231">False</span></span>                                            |
| <span data-ttu-id="e8e70-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8e70-232">Is-Single-Valued</span></span>       | <span data-ttu-id="e8e70-233">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-233">False</span></span>                                            |
| <span data-ttu-id="e8e70-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8e70-234">Is Indexed</span></span>             | <span data-ttu-id="e8e70-235">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-235">False</span></span>                                            |
| <span data-ttu-id="e8e70-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8e70-236">In Global Catalog</span></span>      | <span data-ttu-id="e8e70-237">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-237">False</span></span>                                            |
| <span data-ttu-id="e8e70-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8e70-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8e70-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8e70-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8e70-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8e70-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8e70-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-242">Search-Flags</span></span>           | <span data-ttu-id="e8e70-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8e70-243">0x00000000</span></span>                                       |
| <span data-ttu-id="e8e70-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-244">System-Flags</span></span>           | <span data-ttu-id="e8e70-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8e70-245">0x00000010</span></span>                                       |
| <span data-ttu-id="e8e70-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8e70-246">Classes used in</span></span>        | [<span data-ttu-id="e8e70-247">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="e8e70-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8e70-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8e70-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8e70-249">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-249">Entry</span></span> | <span data-ttu-id="e8e70-250">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8e70-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e70-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8e70-253">System-Only</span></span>            | <span data-ttu-id="e8e70-254">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-254">False</span></span>                                            |
| <span data-ttu-id="e8e70-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8e70-255">Is-Single-Valued</span></span>       | <span data-ttu-id="e8e70-256">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-256">False</span></span>                                            |
| <span data-ttu-id="e8e70-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8e70-257">Is Indexed</span></span>             | <span data-ttu-id="e8e70-258">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-258">False</span></span>                                            |
| <span data-ttu-id="e8e70-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8e70-259">In Global Catalog</span></span>      | <span data-ttu-id="e8e70-260">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-260">False</span></span>                                            |
| <span data-ttu-id="e8e70-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8e70-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8e70-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8e70-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8e70-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8e70-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8e70-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-265">Search-Flags</span></span>           | <span data-ttu-id="e8e70-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8e70-266">0x00000000</span></span>                                       |
| <span data-ttu-id="e8e70-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-267">System-Flags</span></span>           | <span data-ttu-id="e8e70-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8e70-268">0x00000010</span></span>                                       |
| <span data-ttu-id="e8e70-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8e70-269">Classes used in</span></span>        | [<span data-ttu-id="e8e70-270">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="e8e70-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8e70-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8e70-271">Windows Server 2012</span></span>



| <span data-ttu-id="e8e70-272">進入</span><span class="sxs-lookup"><span data-stu-id="e8e70-272">Entry</span></span> | <span data-ttu-id="e8e70-273">值</span><span class="sxs-lookup"><span data-stu-id="e8e70-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="e8e70-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e70-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8e70-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="e8e70-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8e70-276">System-Only</span></span>            | <span data-ttu-id="e8e70-277">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-277">False</span></span>                                            |
| <span data-ttu-id="e8e70-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e8e70-278">Is-Single-Valued</span></span>       | <span data-ttu-id="e8e70-279">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-279">False</span></span>                                            |
| <span data-ttu-id="e8e70-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e8e70-280">Is Indexed</span></span>             | <span data-ttu-id="e8e70-281">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-281">False</span></span>                                            |
| <span data-ttu-id="e8e70-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e8e70-282">In Global Catalog</span></span>      | <span data-ttu-id="e8e70-283">否</span><span class="sxs-lookup"><span data-stu-id="e8e70-283">False</span></span>                                            |
| <span data-ttu-id="e8e70-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e8e70-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8e70-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e8e70-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="e8e70-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8e70-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8e70-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="e8e70-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-288">Search-Flags</span></span>           | <span data-ttu-id="e8e70-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8e70-289">0x00000000</span></span>                                       |
| <span data-ttu-id="e8e70-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8e70-290">System-Flags</span></span>           | <span data-ttu-id="e8e70-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8e70-291">0x00000010</span></span>                                       |
| <span data-ttu-id="e8e70-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e8e70-292">Classes used in</span></span>        | [<span data-ttu-id="e8e70-293">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="e8e70-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





