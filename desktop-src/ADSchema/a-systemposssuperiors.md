---
title: 系統 Poss-Superiors 屬性
description: 可包含這個類別的類別清單。 這份清單只能由系統修改。
ms.assetid: 8b98249a-fe9a-4a42-abb8-a8b042250a76
ms.tgt_platform: multiple
keywords:
- 系統 Poss-Superiors 屬性 AD 架構
- systemPossSuperiors 屬性 AD 架構
topic_type:
- apiref
api_name:
- System-Poss-Superiors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b2116dfb8d2ad21d8a52854b1eb98ef156eb46a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845288"
---
# <a name="system-poss-superiors-attribute"></a><span data-ttu-id="bfe0e-106">系統 Poss-Superiors 屬性</span><span class="sxs-lookup"><span data-stu-id="bfe0e-106">System-Poss-Superiors attribute</span></span>

<span data-ttu-id="bfe0e-107">可包含這個類別的類別清單。</span><span class="sxs-lookup"><span data-stu-id="bfe0e-107">The list of classes that can contain this class.</span></span> <span data-ttu-id="bfe0e-108">這份清單只能由系統修改。</span><span class="sxs-lookup"><span data-stu-id="bfe0e-108">This list can only be modified by the system.</span></span>



| <span data-ttu-id="bfe0e-109">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-109">Entry</span></span> | <span data-ttu-id="bfe0e-110">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="bfe0e-111">CN</span><span class="sxs-lookup"><span data-stu-id="bfe0e-111">CN</span></span>                | <span data-ttu-id="bfe0e-112">系統-Poss-Superiors</span><span class="sxs-lookup"><span data-stu-id="bfe0e-112">System-Poss-Superiors</span></span>                                                       |
| <span data-ttu-id="bfe0e-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bfe0e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bfe0e-114">systemPossSuperiors</span><span class="sxs-lookup"><span data-stu-id="bfe0e-114">systemPossSuperiors</span></span>                                                         |
| <span data-ttu-id="bfe0e-115">大小</span><span class="sxs-lookup"><span data-stu-id="bfe0e-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="bfe0e-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bfe0e-116">Update Privilege</span></span>  | <span data-ttu-id="bfe0e-117">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="bfe0e-117">Schema administrator</span></span>                                                        |
| <span data-ttu-id="bfe0e-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bfe0e-118">Update Frequency</span></span>  | <span data-ttu-id="bfe0e-119">當建立類別，或將新的可能高階加入至類別時。</span><span class="sxs-lookup"><span data-stu-id="bfe0e-119">When the class is created or a new possible superior is added to the class.</span></span> |
| <span data-ttu-id="bfe0e-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-120">Attribute-Id</span></span>      | <span data-ttu-id="bfe0e-121">1.2.840.113556.1.4.195</span><span class="sxs-lookup"><span data-stu-id="bfe0e-121">1.2.840.113556.1.4.195</span></span>                                                      |
| <span data-ttu-id="bfe0e-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bfe0e-122">System-Id-Guid</span></span>    | <span data-ttu-id="bfe0e-123">bf967a47-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bfe0e-123">bf967a47-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="bfe0e-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfe0e-124">Syntax</span></span>            | [<span data-ttu-id="bfe0e-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)             |



## <a name="implementations"></a><span data-ttu-id="bfe0e-126">實作</span><span class="sxs-lookup"><span data-stu-id="bfe0e-126">Implementations</span></span>

-   [<span data-ttu-id="bfe0e-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bfe0e-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bfe0e-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bfe0e-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bfe0e-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bfe0e-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bfe0e-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bfe0e-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfe0e-134">Windows 2000 Server</span></span>



| <span data-ttu-id="bfe0e-135">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-135">Entry</span></span> | <span data-ttu-id="bfe0e-136">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bfe0e-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bfe0e-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-138">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe0e-139">System-Only</span></span>            | <span data-ttu-id="bfe0e-140">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-140">True</span></span>                                             |
| <span data-ttu-id="bfe0e-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-141">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe0e-142">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-142">False</span></span>                                            |
| <span data-ttu-id="bfe0e-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bfe0e-143">Is Indexed</span></span>             | <span data-ttu-id="bfe0e-144">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-144">False</span></span>                                            |
| <span data-ttu-id="bfe0e-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bfe0e-145">In Global Catalog</span></span>      | <span data-ttu-id="bfe0e-146">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-146">True</span></span>                                             |
| <span data-ttu-id="bfe0e-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bfe0e-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe0e-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bfe0e-148">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bfe0e-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe0e-149">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe0e-150">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-151">Search-Flags</span></span>           | <span data-ttu-id="bfe0e-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe0e-152">0x00000000</span></span>                                       |
| <span data-ttu-id="bfe0e-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-153">System-Flags</span></span>           | <span data-ttu-id="bfe0e-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfe0e-154">0x00000010</span></span>                                       |
| <span data-ttu-id="bfe0e-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bfe0e-155">Classes used in</span></span>        | [<span data-ttu-id="bfe0e-156">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bfe0e-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfe0e-157">Windows Server 2003</span></span>



| <span data-ttu-id="bfe0e-158">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-158">Entry</span></span> | <span data-ttu-id="bfe0e-159">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-159">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bfe0e-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bfe0e-160">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-161">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe0e-162">System-Only</span></span>            | <span data-ttu-id="bfe0e-163">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-163">True</span></span>                                             |
| <span data-ttu-id="bfe0e-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-164">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe0e-165">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-165">False</span></span>                                            |
| <span data-ttu-id="bfe0e-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bfe0e-166">Is Indexed</span></span>             | <span data-ttu-id="bfe0e-167">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-167">False</span></span>                                            |
| <span data-ttu-id="bfe0e-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bfe0e-168">In Global Catalog</span></span>      | <span data-ttu-id="bfe0e-169">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-169">True</span></span>                                             |
| <span data-ttu-id="bfe0e-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bfe0e-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe0e-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bfe0e-171">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bfe0e-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe0e-172">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe0e-173">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-174">Search-Flags</span></span>           | <span data-ttu-id="bfe0e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe0e-175">0x00000000</span></span>                                       |
| <span data-ttu-id="bfe0e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-176">System-Flags</span></span>           | <span data-ttu-id="bfe0e-177">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfe0e-177">0x00000012</span></span>                                       |
| <span data-ttu-id="bfe0e-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bfe0e-178">Classes used in</span></span>        | [<span data-ttu-id="bfe0e-179">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-179">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bfe0e-180">亞當</span><span class="sxs-lookup"><span data-stu-id="bfe0e-180">ADAM</span></span>



| <span data-ttu-id="bfe0e-181">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-181">Entry</span></span> | <span data-ttu-id="bfe0e-182">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-182">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bfe0e-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bfe0e-183">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-184">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe0e-185">System-Only</span></span>            | <span data-ttu-id="bfe0e-186">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-186">True</span></span>                                             |
| <span data-ttu-id="bfe0e-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-187">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe0e-188">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-188">False</span></span>                                            |
| <span data-ttu-id="bfe0e-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bfe0e-189">Is Indexed</span></span>             | <span data-ttu-id="bfe0e-190">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-190">False</span></span>                                            |
| <span data-ttu-id="bfe0e-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bfe0e-191">In Global Catalog</span></span>      | <span data-ttu-id="bfe0e-192">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-192">True</span></span>                                             |
| <span data-ttu-id="bfe0e-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bfe0e-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe0e-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bfe0e-194">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bfe0e-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe0e-195">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe0e-196">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-197">Search-Flags</span></span>           | <span data-ttu-id="bfe0e-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe0e-198">0x00000000</span></span>                                       |
| <span data-ttu-id="bfe0e-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-199">System-Flags</span></span>           | <span data-ttu-id="bfe0e-200">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfe0e-200">0x00000012</span></span>                                       |
| <span data-ttu-id="bfe0e-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bfe0e-201">Classes used in</span></span>        | [<span data-ttu-id="bfe0e-202">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-202">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bfe0e-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bfe0e-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bfe0e-204">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-204">Entry</span></span> | <span data-ttu-id="bfe0e-205">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-205">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bfe0e-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bfe0e-206">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-207">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe0e-208">System-Only</span></span>            | <span data-ttu-id="bfe0e-209">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-209">True</span></span>                                             |
| <span data-ttu-id="bfe0e-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-210">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe0e-211">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-211">False</span></span>                                            |
| <span data-ttu-id="bfe0e-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bfe0e-212">Is Indexed</span></span>             | <span data-ttu-id="bfe0e-213">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-213">False</span></span>                                            |
| <span data-ttu-id="bfe0e-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bfe0e-214">In Global Catalog</span></span>      | <span data-ttu-id="bfe0e-215">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-215">True</span></span>                                             |
| <span data-ttu-id="bfe0e-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bfe0e-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe0e-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bfe0e-217">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bfe0e-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe0e-218">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe0e-219">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-220">Search-Flags</span></span>           | <span data-ttu-id="bfe0e-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe0e-221">0x00000000</span></span>                                       |
| <span data-ttu-id="bfe0e-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-222">System-Flags</span></span>           | <span data-ttu-id="bfe0e-223">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfe0e-223">0x00000012</span></span>                                       |
| <span data-ttu-id="bfe0e-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bfe0e-224">Classes used in</span></span>        | [<span data-ttu-id="bfe0e-225">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-225">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bfe0e-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfe0e-226">Windows Server 2008</span></span>



| <span data-ttu-id="bfe0e-227">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-227">Entry</span></span> | <span data-ttu-id="bfe0e-228">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-228">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bfe0e-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bfe0e-229">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-230">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe0e-231">System-Only</span></span>            | <span data-ttu-id="bfe0e-232">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-232">True</span></span>                                             |
| <span data-ttu-id="bfe0e-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-233">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe0e-234">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-234">False</span></span>                                            |
| <span data-ttu-id="bfe0e-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bfe0e-235">Is Indexed</span></span>             | <span data-ttu-id="bfe0e-236">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-236">False</span></span>                                            |
| <span data-ttu-id="bfe0e-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bfe0e-237">In Global Catalog</span></span>      | <span data-ttu-id="bfe0e-238">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-238">True</span></span>                                             |
| <span data-ttu-id="bfe0e-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bfe0e-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe0e-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bfe0e-240">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bfe0e-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe0e-241">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe0e-242">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-243">Search-Flags</span></span>           | <span data-ttu-id="bfe0e-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe0e-244">0x00000000</span></span>                                       |
| <span data-ttu-id="bfe0e-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-245">System-Flags</span></span>           | <span data-ttu-id="bfe0e-246">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfe0e-246">0x00000012</span></span>                                       |
| <span data-ttu-id="bfe0e-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bfe0e-247">Classes used in</span></span>        | [<span data-ttu-id="bfe0e-248">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-248">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bfe0e-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfe0e-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bfe0e-250">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-250">Entry</span></span> | <span data-ttu-id="bfe0e-251">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-251">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bfe0e-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bfe0e-252">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-253">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe0e-254">System-Only</span></span>            | <span data-ttu-id="bfe0e-255">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-255">True</span></span>                                             |
| <span data-ttu-id="bfe0e-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-256">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe0e-257">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-257">False</span></span>                                            |
| <span data-ttu-id="bfe0e-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bfe0e-258">Is Indexed</span></span>             | <span data-ttu-id="bfe0e-259">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-259">False</span></span>                                            |
| <span data-ttu-id="bfe0e-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bfe0e-260">In Global Catalog</span></span>      | <span data-ttu-id="bfe0e-261">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-261">True</span></span>                                             |
| <span data-ttu-id="bfe0e-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bfe0e-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe0e-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bfe0e-263">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bfe0e-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe0e-264">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe0e-265">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-266">Search-Flags</span></span>           | <span data-ttu-id="bfe0e-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe0e-267">0x00000000</span></span>                                       |
| <span data-ttu-id="bfe0e-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-268">System-Flags</span></span>           | <span data-ttu-id="bfe0e-269">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfe0e-269">0x00000012</span></span>                                       |
| <span data-ttu-id="bfe0e-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bfe0e-270">Classes used in</span></span>        | [<span data-ttu-id="bfe0e-271">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-271">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bfe0e-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfe0e-272">Windows Server 2012</span></span>



| <span data-ttu-id="bfe0e-273">進入</span><span class="sxs-lookup"><span data-stu-id="bfe0e-273">Entry</span></span> | <span data-ttu-id="bfe0e-274">值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-274">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="bfe0e-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bfe0e-275">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfe0e-276">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="bfe0e-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfe0e-277">System-Only</span></span>            | <span data-ttu-id="bfe0e-278">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-278">True</span></span>                                             |
| <span data-ttu-id="bfe0e-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bfe0e-279">Is-Single-Valued</span></span>       | <span data-ttu-id="bfe0e-280">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-280">False</span></span>                                            |
| <span data-ttu-id="bfe0e-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bfe0e-281">Is Indexed</span></span>             | <span data-ttu-id="bfe0e-282">否</span><span class="sxs-lookup"><span data-stu-id="bfe0e-282">False</span></span>                                            |
| <span data-ttu-id="bfe0e-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bfe0e-283">In Global Catalog</span></span>      | <span data-ttu-id="bfe0e-284">對</span><span class="sxs-lookup"><span data-stu-id="bfe0e-284">True</span></span>                                             |
| <span data-ttu-id="bfe0e-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bfe0e-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfe0e-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bfe0e-286">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="bfe0e-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfe0e-287">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfe0e-288">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="bfe0e-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-289">Search-Flags</span></span>           | <span data-ttu-id="bfe0e-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfe0e-290">0x00000000</span></span>                                       |
| <span data-ttu-id="bfe0e-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfe0e-291">System-Flags</span></span>           | <span data-ttu-id="bfe0e-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bfe0e-292">0x00000012</span></span>                                       |
| <span data-ttu-id="bfe0e-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bfe0e-293">Classes used in</span></span>        | [<span data-ttu-id="bfe0e-294">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="bfe0e-294">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





