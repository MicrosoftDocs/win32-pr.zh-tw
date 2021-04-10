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
# <a name="must-contain-attribute"></a><span data-ttu-id="2c85a-106">Must-Contain 屬性</span><span class="sxs-lookup"><span data-stu-id="2c85a-106">Must-Contain attribute</span></span>

<span data-ttu-id="2c85a-107">類別的強制屬性清單。</span><span class="sxs-lookup"><span data-stu-id="2c85a-107">The list of mandatory attributes for a class.</span></span> <span data-ttu-id="2c85a-108">建立類別的實例時，必須指定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c85a-108">These attributes must be specified when an instance of the class is created.</span></span>



| <span data-ttu-id="2c85a-109">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-109">Entry</span></span> | <span data-ttu-id="2c85a-110">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="2c85a-111">CN</span><span class="sxs-lookup"><span data-stu-id="2c85a-111">CN</span></span>                | <span data-ttu-id="2c85a-112">Must-Contain</span><span class="sxs-lookup"><span data-stu-id="2c85a-112">Must-Contain</span></span>                                                    |
| <span data-ttu-id="2c85a-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2c85a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2c85a-114">mustContain</span><span class="sxs-lookup"><span data-stu-id="2c85a-114">mustContain</span></span>                                                     |
| <span data-ttu-id="2c85a-115">大小</span><span class="sxs-lookup"><span data-stu-id="2c85a-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="2c85a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2c85a-116">Update Privilege</span></span>  | <span data-ttu-id="2c85a-117">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="2c85a-117">Schema administrator</span></span>                                            |
| <span data-ttu-id="2c85a-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2c85a-118">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="2c85a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-119">Attribute-Id</span></span>      | <span data-ttu-id="2c85a-120">1.2.840.113556.1.2.24</span><span class="sxs-lookup"><span data-stu-id="2c85a-120">1.2.840.113556.1.2.24</span></span>                                           |
| <span data-ttu-id="2c85a-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2c85a-121">System-Id-Guid</span></span>    | <span data-ttu-id="2c85a-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2c85a-122">bf9679d3-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="2c85a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c85a-123">Syntax</span></span>            | [<span data-ttu-id="2c85a-124">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="2c85a-124">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="2c85a-125">實作</span><span class="sxs-lookup"><span data-stu-id="2c85a-125">Implementations</span></span>

-   [<span data-ttu-id="2c85a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2c85a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2c85a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2c85a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2c85a-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="2c85a-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2c85a-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2c85a-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2c85a-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2c85a-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2c85a-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2c85a-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2c85a-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c85a-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2c85a-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c85a-133">Windows 2000 Server</span></span>



| <span data-ttu-id="2c85a-134">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-134">Entry</span></span> | <span data-ttu-id="2c85a-135">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2c85a-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c85a-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c85a-138">System-Only</span></span>            | <span data-ttu-id="2c85a-139">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-139">False</span></span>                                            |
| <span data-ttu-id="2c85a-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c85a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="2c85a-141">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-141">False</span></span>                                            |
| <span data-ttu-id="2c85a-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c85a-142">Is Indexed</span></span>             | <span data-ttu-id="2c85a-143">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-143">False</span></span>                                            |
| <span data-ttu-id="2c85a-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c85a-144">In Global Catalog</span></span>      | <span data-ttu-id="2c85a-145">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-145">False</span></span>                                            |
| <span data-ttu-id="2c85a-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c85a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c85a-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c85a-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2c85a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c85a-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c85a-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-150">Search-Flags</span></span>           | <span data-ttu-id="2c85a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c85a-151">0x00000000</span></span>                                       |
| <span data-ttu-id="2c85a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-152">System-Flags</span></span>           | <span data-ttu-id="2c85a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c85a-153">0x00000010</span></span>                                       |
| <span data-ttu-id="2c85a-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c85a-154">Classes used in</span></span>        | [<span data-ttu-id="2c85a-155">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="2c85a-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2c85a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c85a-156">Windows Server 2003</span></span>



| <span data-ttu-id="2c85a-157">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-157">Entry</span></span> | <span data-ttu-id="2c85a-158">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2c85a-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c85a-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c85a-161">System-Only</span></span>            | <span data-ttu-id="2c85a-162">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-162">False</span></span>                                            |
| <span data-ttu-id="2c85a-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c85a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="2c85a-164">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-164">False</span></span>                                            |
| <span data-ttu-id="2c85a-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c85a-165">Is Indexed</span></span>             | <span data-ttu-id="2c85a-166">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-166">False</span></span>                                            |
| <span data-ttu-id="2c85a-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c85a-167">In Global Catalog</span></span>      | <span data-ttu-id="2c85a-168">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-168">False</span></span>                                            |
| <span data-ttu-id="2c85a-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c85a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c85a-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c85a-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2c85a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c85a-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c85a-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-173">Search-Flags</span></span>           | <span data-ttu-id="2c85a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c85a-174">0x00000000</span></span>                                       |
| <span data-ttu-id="2c85a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-175">System-Flags</span></span>           | <span data-ttu-id="2c85a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c85a-176">0x00000010</span></span>                                       |
| <span data-ttu-id="2c85a-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c85a-177">Classes used in</span></span>        | [<span data-ttu-id="2c85a-178">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="2c85a-178">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2c85a-179">亞當</span><span class="sxs-lookup"><span data-stu-id="2c85a-179">ADAM</span></span>



| <span data-ttu-id="2c85a-180">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-180">Entry</span></span> | <span data-ttu-id="2c85a-181">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2c85a-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c85a-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c85a-184">System-Only</span></span>            | <span data-ttu-id="2c85a-185">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-185">False</span></span>                                            |
| <span data-ttu-id="2c85a-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c85a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="2c85a-187">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-187">False</span></span>                                            |
| <span data-ttu-id="2c85a-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c85a-188">Is Indexed</span></span>             | <span data-ttu-id="2c85a-189">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-189">False</span></span>                                            |
| <span data-ttu-id="2c85a-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c85a-190">In Global Catalog</span></span>      | <span data-ttu-id="2c85a-191">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-191">False</span></span>                                            |
| <span data-ttu-id="2c85a-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c85a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c85a-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c85a-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2c85a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c85a-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c85a-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-196">Search-Flags</span></span>           | <span data-ttu-id="2c85a-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c85a-197">0x00000000</span></span>                                       |
| <span data-ttu-id="2c85a-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-198">System-Flags</span></span>           | <span data-ttu-id="2c85a-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c85a-199">0x00000010</span></span>                                       |
| <span data-ttu-id="2c85a-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c85a-200">Classes used in</span></span>        | [<span data-ttu-id="2c85a-201">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="2c85a-201">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2c85a-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2c85a-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2c85a-203">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-203">Entry</span></span> | <span data-ttu-id="2c85a-204">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2c85a-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c85a-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c85a-207">System-Only</span></span>            | <span data-ttu-id="2c85a-208">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-208">False</span></span>                                            |
| <span data-ttu-id="2c85a-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c85a-209">Is-Single-Valued</span></span>       | <span data-ttu-id="2c85a-210">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-210">False</span></span>                                            |
| <span data-ttu-id="2c85a-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c85a-211">Is Indexed</span></span>             | <span data-ttu-id="2c85a-212">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-212">False</span></span>                                            |
| <span data-ttu-id="2c85a-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c85a-213">In Global Catalog</span></span>      | <span data-ttu-id="2c85a-214">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-214">False</span></span>                                            |
| <span data-ttu-id="2c85a-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c85a-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c85a-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c85a-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2c85a-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c85a-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c85a-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-219">Search-Flags</span></span>           | <span data-ttu-id="2c85a-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c85a-220">0x00000000</span></span>                                       |
| <span data-ttu-id="2c85a-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-221">System-Flags</span></span>           | <span data-ttu-id="2c85a-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c85a-222">0x00000010</span></span>                                       |
| <span data-ttu-id="2c85a-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c85a-223">Classes used in</span></span>        | [<span data-ttu-id="2c85a-224">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="2c85a-224">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2c85a-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c85a-225">Windows Server 2008</span></span>



| <span data-ttu-id="2c85a-226">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-226">Entry</span></span> | <span data-ttu-id="2c85a-227">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2c85a-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c85a-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c85a-230">System-Only</span></span>            | <span data-ttu-id="2c85a-231">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-231">False</span></span>                                            |
| <span data-ttu-id="2c85a-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c85a-232">Is-Single-Valued</span></span>       | <span data-ttu-id="2c85a-233">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-233">False</span></span>                                            |
| <span data-ttu-id="2c85a-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c85a-234">Is Indexed</span></span>             | <span data-ttu-id="2c85a-235">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-235">False</span></span>                                            |
| <span data-ttu-id="2c85a-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c85a-236">In Global Catalog</span></span>      | <span data-ttu-id="2c85a-237">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-237">False</span></span>                                            |
| <span data-ttu-id="2c85a-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c85a-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c85a-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c85a-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2c85a-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c85a-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c85a-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-242">Search-Flags</span></span>           | <span data-ttu-id="2c85a-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c85a-243">0x00000000</span></span>                                       |
| <span data-ttu-id="2c85a-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-244">System-Flags</span></span>           | <span data-ttu-id="2c85a-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c85a-245">0x00000010</span></span>                                       |
| <span data-ttu-id="2c85a-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c85a-246">Classes used in</span></span>        | [<span data-ttu-id="2c85a-247">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="2c85a-247">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2c85a-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c85a-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2c85a-249">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-249">Entry</span></span> | <span data-ttu-id="2c85a-250">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2c85a-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c85a-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c85a-253">System-Only</span></span>            | <span data-ttu-id="2c85a-254">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-254">False</span></span>                                            |
| <span data-ttu-id="2c85a-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c85a-255">Is-Single-Valued</span></span>       | <span data-ttu-id="2c85a-256">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-256">False</span></span>                                            |
| <span data-ttu-id="2c85a-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c85a-257">Is Indexed</span></span>             | <span data-ttu-id="2c85a-258">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-258">False</span></span>                                            |
| <span data-ttu-id="2c85a-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c85a-259">In Global Catalog</span></span>      | <span data-ttu-id="2c85a-260">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-260">False</span></span>                                            |
| <span data-ttu-id="2c85a-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c85a-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c85a-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c85a-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2c85a-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c85a-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c85a-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-265">Search-Flags</span></span>           | <span data-ttu-id="2c85a-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c85a-266">0x00000000</span></span>                                       |
| <span data-ttu-id="2c85a-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-267">System-Flags</span></span>           | <span data-ttu-id="2c85a-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c85a-268">0x00000010</span></span>                                       |
| <span data-ttu-id="2c85a-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c85a-269">Classes used in</span></span>        | [<span data-ttu-id="2c85a-270">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="2c85a-270">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2c85a-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c85a-271">Windows Server 2012</span></span>



| <span data-ttu-id="2c85a-272">進入</span><span class="sxs-lookup"><span data-stu-id="2c85a-272">Entry</span></span> | <span data-ttu-id="2c85a-273">值</span><span class="sxs-lookup"><span data-stu-id="2c85a-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2c85a-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c85a-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c85a-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2c85a-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c85a-276">System-Only</span></span>            | <span data-ttu-id="2c85a-277">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-277">False</span></span>                                            |
| <span data-ttu-id="2c85a-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c85a-278">Is-Single-Valued</span></span>       | <span data-ttu-id="2c85a-279">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-279">False</span></span>                                            |
| <span data-ttu-id="2c85a-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c85a-280">Is Indexed</span></span>             | <span data-ttu-id="2c85a-281">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-281">False</span></span>                                            |
| <span data-ttu-id="2c85a-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c85a-282">In Global Catalog</span></span>      | <span data-ttu-id="2c85a-283">否</span><span class="sxs-lookup"><span data-stu-id="2c85a-283">False</span></span>                                            |
| <span data-ttu-id="2c85a-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c85a-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c85a-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c85a-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2c85a-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c85a-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c85a-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="2c85a-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-288">Search-Flags</span></span>           | <span data-ttu-id="2c85a-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c85a-289">0x00000000</span></span>                                       |
| <span data-ttu-id="2c85a-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c85a-290">System-Flags</span></span>           | <span data-ttu-id="2c85a-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c85a-291">0x00000010</span></span>                                       |
| <span data-ttu-id="2c85a-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c85a-292">Classes used in</span></span>        | [<span data-ttu-id="2c85a-293">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="2c85a-293">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





