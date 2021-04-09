---
title: Object-Classes 屬性
description: 多值屬性，其中包含表示架構中每個類別的字串。 每個值都包含 governsID、lDAPDisplayName、mustContain、mayContain 等等。
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Object-Classes 屬性 AD 架構
- objectClasses 屬性 AD 架構
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b799c725790115152ac70c0214d82a8c242ea600
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845379"
---
# <a name="object-classes-attribute"></a><span data-ttu-id="51e8d-106">Object-Classes 屬性</span><span class="sxs-lookup"><span data-stu-id="51e8d-106">Object-Classes attribute</span></span>

<span data-ttu-id="51e8d-107">多值屬性，其中包含表示架構中每個類別的字串。</span><span class="sxs-lookup"><span data-stu-id="51e8d-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="51e8d-108">每個值都包含 governsID、lDAPDisplayName、mustContain、mayContain 等等。</span><span class="sxs-lookup"><span data-stu-id="51e8d-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="51e8d-109">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-109">Entry</span></span> | <span data-ttu-id="51e8d-110">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="51e8d-111">CN</span><span class="sxs-lookup"><span data-stu-id="51e8d-111">CN</span></span>                | <span data-ttu-id="51e8d-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="51e8d-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="51e8d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="51e8d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="51e8d-114">objectClasses</span><span class="sxs-lookup"><span data-stu-id="51e8d-114">objectClasses</span></span>                                    |
| <span data-ttu-id="51e8d-115">大小</span><span class="sxs-lookup"><span data-stu-id="51e8d-115">Size</span></span>              | <span data-ttu-id="51e8d-116">每個類別名稱平均大約20個位元組。</span><span class="sxs-lookup"><span data-stu-id="51e8d-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="51e8d-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="51e8d-117">Update Privilege</span></span>  | <span data-ttu-id="51e8d-118">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="51e8d-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="51e8d-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="51e8d-119">Update Frequency</span></span>  | <span data-ttu-id="51e8d-120">每當類別的設計變更時。</span><span class="sxs-lookup"><span data-stu-id="51e8d-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="51e8d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-121">Attribute-Id</span></span>      | <span data-ttu-id="51e8d-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="51e8d-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="51e8d-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="51e8d-123">System-Id-Guid</span></span>    | <span data-ttu-id="51e8d-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="51e8d-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="51e8d-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="51e8d-125">Syntax</span></span>            | [<span data-ttu-id="51e8d-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="51e8d-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="51e8d-127">實作</span><span class="sxs-lookup"><span data-stu-id="51e8d-127">Implementations</span></span>

-   [<span data-ttu-id="51e8d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="51e8d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="51e8d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51e8d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51e8d-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="51e8d-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="51e8d-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51e8d-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51e8d-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51e8d-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51e8d-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51e8d-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51e8d-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51e8d-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="51e8d-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51e8d-135">Windows 2000 Server</span></span>



| <span data-ttu-id="51e8d-136">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-136">Entry</span></span> | <span data-ttu-id="51e8d-137">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="51e8d-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51e8d-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="51e8d-140">System-Only</span></span>            | <span data-ttu-id="51e8d-141">對</span><span class="sxs-lookup"><span data-stu-id="51e8d-141">True</span></span>                                        |
| <span data-ttu-id="51e8d-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51e8d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="51e8d-143">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-143">False</span></span>                                       |
| <span data-ttu-id="51e8d-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51e8d-144">Is Indexed</span></span>             | <span data-ttu-id="51e8d-145">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-145">False</span></span>                                       |
| <span data-ttu-id="51e8d-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51e8d-146">In Global Catalog</span></span>      | <span data-ttu-id="51e8d-147">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-147">False</span></span>                                       |
| <span data-ttu-id="51e8d-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51e8d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="51e8d-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51e8d-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="51e8d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51e8d-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51e8d-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-152">Search-Flags</span></span>           | <span data-ttu-id="51e8d-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51e8d-153">0x00000000</span></span>                                  |
| <span data-ttu-id="51e8d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-154">System-Flags</span></span>           | <span data-ttu-id="51e8d-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="51e8d-155">0x08000014</span></span>                                  |
| <span data-ttu-id="51e8d-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51e8d-156">Classes used in</span></span>        | [<span data-ttu-id="51e8d-157">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="51e8d-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="51e8d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51e8d-158">Windows Server 2003</span></span>



| <span data-ttu-id="51e8d-159">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-159">Entry</span></span> | <span data-ttu-id="51e8d-160">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="51e8d-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51e8d-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="51e8d-163">System-Only</span></span>            | <span data-ttu-id="51e8d-164">對</span><span class="sxs-lookup"><span data-stu-id="51e8d-164">True</span></span>                                        |
| <span data-ttu-id="51e8d-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51e8d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="51e8d-166">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-166">False</span></span>                                       |
| <span data-ttu-id="51e8d-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51e8d-167">Is Indexed</span></span>             | <span data-ttu-id="51e8d-168">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-168">False</span></span>                                       |
| <span data-ttu-id="51e8d-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51e8d-169">In Global Catalog</span></span>      | <span data-ttu-id="51e8d-170">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-170">False</span></span>                                       |
| <span data-ttu-id="51e8d-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51e8d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="51e8d-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51e8d-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="51e8d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51e8d-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51e8d-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-175">Search-Flags</span></span>           | <span data-ttu-id="51e8d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51e8d-176">0x00000000</span></span>                                  |
| <span data-ttu-id="51e8d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-177">System-Flags</span></span>           | <span data-ttu-id="51e8d-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="51e8d-178">0x08000014</span></span>                                  |
| <span data-ttu-id="51e8d-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51e8d-179">Classes used in</span></span>        | [<span data-ttu-id="51e8d-180">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="51e8d-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="51e8d-181">亞當</span><span class="sxs-lookup"><span data-stu-id="51e8d-181">ADAM</span></span>



| <span data-ttu-id="51e8d-182">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-182">Entry</span></span> | <span data-ttu-id="51e8d-183">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="51e8d-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51e8d-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="51e8d-186">System-Only</span></span>            | <span data-ttu-id="51e8d-187">對</span><span class="sxs-lookup"><span data-stu-id="51e8d-187">True</span></span>                                        |
| <span data-ttu-id="51e8d-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51e8d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="51e8d-189">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-189">False</span></span>                                       |
| <span data-ttu-id="51e8d-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51e8d-190">Is Indexed</span></span>             | <span data-ttu-id="51e8d-191">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-191">False</span></span>                                       |
| <span data-ttu-id="51e8d-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51e8d-192">In Global Catalog</span></span>      | <span data-ttu-id="51e8d-193">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-193">False</span></span>                                       |
| <span data-ttu-id="51e8d-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51e8d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="51e8d-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51e8d-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="51e8d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51e8d-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51e8d-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-198">Search-Flags</span></span>           | <span data-ttu-id="51e8d-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51e8d-199">0x00000000</span></span>                                  |
| <span data-ttu-id="51e8d-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-200">System-Flags</span></span>           | <span data-ttu-id="51e8d-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="51e8d-201">0x08000014</span></span>                                  |
| <span data-ttu-id="51e8d-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51e8d-202">Classes used in</span></span>        | [<span data-ttu-id="51e8d-203">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="51e8d-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51e8d-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51e8d-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51e8d-205">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-205">Entry</span></span> | <span data-ttu-id="51e8d-206">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="51e8d-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51e8d-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="51e8d-209">System-Only</span></span>            | <span data-ttu-id="51e8d-210">對</span><span class="sxs-lookup"><span data-stu-id="51e8d-210">True</span></span>                                        |
| <span data-ttu-id="51e8d-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51e8d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="51e8d-212">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-212">False</span></span>                                       |
| <span data-ttu-id="51e8d-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51e8d-213">Is Indexed</span></span>             | <span data-ttu-id="51e8d-214">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-214">False</span></span>                                       |
| <span data-ttu-id="51e8d-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51e8d-215">In Global Catalog</span></span>      | <span data-ttu-id="51e8d-216">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-216">False</span></span>                                       |
| <span data-ttu-id="51e8d-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51e8d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="51e8d-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51e8d-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="51e8d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51e8d-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51e8d-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-221">Search-Flags</span></span>           | <span data-ttu-id="51e8d-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51e8d-222">0x00000000</span></span>                                  |
| <span data-ttu-id="51e8d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-223">System-Flags</span></span>           | <span data-ttu-id="51e8d-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="51e8d-224">0x08000014</span></span>                                  |
| <span data-ttu-id="51e8d-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51e8d-225">Classes used in</span></span>        | [<span data-ttu-id="51e8d-226">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="51e8d-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="51e8d-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51e8d-227">Windows Server 2008</span></span>



| <span data-ttu-id="51e8d-228">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-228">Entry</span></span> | <span data-ttu-id="51e8d-229">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="51e8d-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51e8d-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="51e8d-232">System-Only</span></span>            | <span data-ttu-id="51e8d-233">對</span><span class="sxs-lookup"><span data-stu-id="51e8d-233">True</span></span>                                        |
| <span data-ttu-id="51e8d-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51e8d-234">Is-Single-Valued</span></span>       | <span data-ttu-id="51e8d-235">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-235">False</span></span>                                       |
| <span data-ttu-id="51e8d-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51e8d-236">Is Indexed</span></span>             | <span data-ttu-id="51e8d-237">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-237">False</span></span>                                       |
| <span data-ttu-id="51e8d-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51e8d-238">In Global Catalog</span></span>      | <span data-ttu-id="51e8d-239">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-239">False</span></span>                                       |
| <span data-ttu-id="51e8d-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51e8d-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="51e8d-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51e8d-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="51e8d-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51e8d-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51e8d-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-244">Search-Flags</span></span>           | <span data-ttu-id="51e8d-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51e8d-245">0x00000000</span></span>                                  |
| <span data-ttu-id="51e8d-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-246">System-Flags</span></span>           | <span data-ttu-id="51e8d-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="51e8d-247">0x08000014</span></span>                                  |
| <span data-ttu-id="51e8d-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51e8d-248">Classes used in</span></span>        | [<span data-ttu-id="51e8d-249">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="51e8d-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51e8d-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51e8d-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51e8d-251">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-251">Entry</span></span> | <span data-ttu-id="51e8d-252">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="51e8d-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51e8d-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="51e8d-255">System-Only</span></span>            | <span data-ttu-id="51e8d-256">對</span><span class="sxs-lookup"><span data-stu-id="51e8d-256">True</span></span>                                        |
| <span data-ttu-id="51e8d-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51e8d-257">Is-Single-Valued</span></span>       | <span data-ttu-id="51e8d-258">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-258">False</span></span>                                       |
| <span data-ttu-id="51e8d-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51e8d-259">Is Indexed</span></span>             | <span data-ttu-id="51e8d-260">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-260">False</span></span>                                       |
| <span data-ttu-id="51e8d-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51e8d-261">In Global Catalog</span></span>      | <span data-ttu-id="51e8d-262">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-262">False</span></span>                                       |
| <span data-ttu-id="51e8d-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51e8d-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="51e8d-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51e8d-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="51e8d-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51e8d-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51e8d-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-267">Search-Flags</span></span>           | <span data-ttu-id="51e8d-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51e8d-268">0x00000000</span></span>                                  |
| <span data-ttu-id="51e8d-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-269">System-Flags</span></span>           | <span data-ttu-id="51e8d-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="51e8d-270">0x08000014</span></span>                                  |
| <span data-ttu-id="51e8d-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51e8d-271">Classes used in</span></span>        | [<span data-ttu-id="51e8d-272">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="51e8d-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="51e8d-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51e8d-273">Windows Server 2012</span></span>



| <span data-ttu-id="51e8d-274">進入</span><span class="sxs-lookup"><span data-stu-id="51e8d-274">Entry</span></span> | <span data-ttu-id="51e8d-275">值</span><span class="sxs-lookup"><span data-stu-id="51e8d-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="51e8d-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51e8d-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51e8d-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="51e8d-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="51e8d-278">System-Only</span></span>            | <span data-ttu-id="51e8d-279">對</span><span class="sxs-lookup"><span data-stu-id="51e8d-279">True</span></span>                                        |
| <span data-ttu-id="51e8d-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51e8d-280">Is-Single-Valued</span></span>       | <span data-ttu-id="51e8d-281">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-281">False</span></span>                                       |
| <span data-ttu-id="51e8d-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51e8d-282">Is Indexed</span></span>             | <span data-ttu-id="51e8d-283">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-283">False</span></span>                                       |
| <span data-ttu-id="51e8d-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51e8d-284">In Global Catalog</span></span>      | <span data-ttu-id="51e8d-285">否</span><span class="sxs-lookup"><span data-stu-id="51e8d-285">False</span></span>                                       |
| <span data-ttu-id="51e8d-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51e8d-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="51e8d-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51e8d-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="51e8d-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51e8d-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51e8d-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="51e8d-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-290">Search-Flags</span></span>           | <span data-ttu-id="51e8d-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51e8d-291">0x00000000</span></span>                                  |
| <span data-ttu-id="51e8d-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51e8d-292">System-Flags</span></span>           | <span data-ttu-id="51e8d-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="51e8d-293">0x08000014</span></span>                                  |
| <span data-ttu-id="51e8d-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51e8d-294">Classes used in</span></span>        | [<span data-ttu-id="51e8d-295">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="51e8d-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





