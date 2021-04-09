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
# <a name="object-classes-attribute"></a><span data-ttu-id="12422-106">Object-Classes 屬性</span><span class="sxs-lookup"><span data-stu-id="12422-106">Object-Classes attribute</span></span>

<span data-ttu-id="12422-107">多值屬性，其中包含表示架構中每個類別的字串。</span><span class="sxs-lookup"><span data-stu-id="12422-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="12422-108">每個值都包含 governsID、lDAPDisplayName、mustContain、mayContain 等等。</span><span class="sxs-lookup"><span data-stu-id="12422-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="12422-109">進入</span><span class="sxs-lookup"><span data-stu-id="12422-109">Entry</span></span> | <span data-ttu-id="12422-110">值</span><span class="sxs-lookup"><span data-stu-id="12422-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="12422-111">CN</span><span class="sxs-lookup"><span data-stu-id="12422-111">CN</span></span>                | <span data-ttu-id="12422-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="12422-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="12422-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="12422-113">Ldap-Display-Name</span></span> | <span data-ttu-id="12422-114">objectClasses</span><span class="sxs-lookup"><span data-stu-id="12422-114">objectClasses</span></span>                                    |
| <span data-ttu-id="12422-115">大小</span><span class="sxs-lookup"><span data-stu-id="12422-115">Size</span></span>              | <span data-ttu-id="12422-116">每個類別名稱平均大約20個位元組。</span><span class="sxs-lookup"><span data-stu-id="12422-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="12422-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="12422-117">Update Privilege</span></span>  | <span data-ttu-id="12422-118">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="12422-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="12422-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="12422-119">Update Frequency</span></span>  | <span data-ttu-id="12422-120">每當類別的設計變更時。</span><span class="sxs-lookup"><span data-stu-id="12422-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="12422-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="12422-121">Attribute-Id</span></span>      | <span data-ttu-id="12422-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="12422-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="12422-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="12422-123">System-Id-Guid</span></span>    | <span data-ttu-id="12422-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="12422-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="12422-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="12422-125">Syntax</span></span>            | [<span data-ttu-id="12422-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="12422-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="12422-127">實作</span><span class="sxs-lookup"><span data-stu-id="12422-127">Implementations</span></span>

-   [<span data-ttu-id="12422-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="12422-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="12422-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="12422-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="12422-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="12422-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="12422-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="12422-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="12422-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="12422-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="12422-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="12422-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="12422-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="12422-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="12422-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12422-135">Windows 2000 Server</span></span>



| <span data-ttu-id="12422-136">進入</span><span class="sxs-lookup"><span data-stu-id="12422-136">Entry</span></span> | <span data-ttu-id="12422-137">值</span><span class="sxs-lookup"><span data-stu-id="12422-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="12422-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12422-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12422-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="12422-140">System-Only</span></span>            | <span data-ttu-id="12422-141">對</span><span class="sxs-lookup"><span data-stu-id="12422-141">True</span></span>                                        |
| <span data-ttu-id="12422-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12422-142">Is-Single-Valued</span></span>       | <span data-ttu-id="12422-143">否</span><span class="sxs-lookup"><span data-stu-id="12422-143">False</span></span>                                       |
| <span data-ttu-id="12422-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12422-144">Is Indexed</span></span>             | <span data-ttu-id="12422-145">否</span><span class="sxs-lookup"><span data-stu-id="12422-145">False</span></span>                                       |
| <span data-ttu-id="12422-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12422-146">In Global Catalog</span></span>      | <span data-ttu-id="12422-147">否</span><span class="sxs-lookup"><span data-stu-id="12422-147">False</span></span>                                       |
| <span data-ttu-id="12422-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12422-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="12422-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12422-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="12422-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12422-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="12422-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12422-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="12422-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-152">Search-Flags</span></span>           | <span data-ttu-id="12422-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12422-153">0x00000000</span></span>                                  |
| <span data-ttu-id="12422-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-154">System-Flags</span></span>           | <span data-ttu-id="12422-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12422-155">0x08000014</span></span>                                  |
| <span data-ttu-id="12422-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12422-156">Classes used in</span></span>        | [<span data-ttu-id="12422-157">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="12422-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="12422-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12422-158">Windows Server 2003</span></span>



| <span data-ttu-id="12422-159">進入</span><span class="sxs-lookup"><span data-stu-id="12422-159">Entry</span></span> | <span data-ttu-id="12422-160">值</span><span class="sxs-lookup"><span data-stu-id="12422-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="12422-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12422-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12422-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="12422-163">System-Only</span></span>            | <span data-ttu-id="12422-164">對</span><span class="sxs-lookup"><span data-stu-id="12422-164">True</span></span>                                        |
| <span data-ttu-id="12422-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12422-165">Is-Single-Valued</span></span>       | <span data-ttu-id="12422-166">否</span><span class="sxs-lookup"><span data-stu-id="12422-166">False</span></span>                                       |
| <span data-ttu-id="12422-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12422-167">Is Indexed</span></span>             | <span data-ttu-id="12422-168">否</span><span class="sxs-lookup"><span data-stu-id="12422-168">False</span></span>                                       |
| <span data-ttu-id="12422-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12422-169">In Global Catalog</span></span>      | <span data-ttu-id="12422-170">否</span><span class="sxs-lookup"><span data-stu-id="12422-170">False</span></span>                                       |
| <span data-ttu-id="12422-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12422-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="12422-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12422-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="12422-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12422-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="12422-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12422-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="12422-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-175">Search-Flags</span></span>           | <span data-ttu-id="12422-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12422-176">0x00000000</span></span>                                  |
| <span data-ttu-id="12422-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-177">System-Flags</span></span>           | <span data-ttu-id="12422-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12422-178">0x08000014</span></span>                                  |
| <span data-ttu-id="12422-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12422-179">Classes used in</span></span>        | [<span data-ttu-id="12422-180">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="12422-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="12422-181">亞當</span><span class="sxs-lookup"><span data-stu-id="12422-181">ADAM</span></span>



| <span data-ttu-id="12422-182">進入</span><span class="sxs-lookup"><span data-stu-id="12422-182">Entry</span></span> | <span data-ttu-id="12422-183">值</span><span class="sxs-lookup"><span data-stu-id="12422-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="12422-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12422-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12422-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="12422-186">System-Only</span></span>            | <span data-ttu-id="12422-187">對</span><span class="sxs-lookup"><span data-stu-id="12422-187">True</span></span>                                        |
| <span data-ttu-id="12422-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12422-188">Is-Single-Valued</span></span>       | <span data-ttu-id="12422-189">否</span><span class="sxs-lookup"><span data-stu-id="12422-189">False</span></span>                                       |
| <span data-ttu-id="12422-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12422-190">Is Indexed</span></span>             | <span data-ttu-id="12422-191">否</span><span class="sxs-lookup"><span data-stu-id="12422-191">False</span></span>                                       |
| <span data-ttu-id="12422-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12422-192">In Global Catalog</span></span>      | <span data-ttu-id="12422-193">否</span><span class="sxs-lookup"><span data-stu-id="12422-193">False</span></span>                                       |
| <span data-ttu-id="12422-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12422-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="12422-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12422-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="12422-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12422-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="12422-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12422-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="12422-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-198">Search-Flags</span></span>           | <span data-ttu-id="12422-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12422-199">0x00000000</span></span>                                  |
| <span data-ttu-id="12422-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-200">System-Flags</span></span>           | <span data-ttu-id="12422-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12422-201">0x08000014</span></span>                                  |
| <span data-ttu-id="12422-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12422-202">Classes used in</span></span>        | [<span data-ttu-id="12422-203">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="12422-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="12422-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="12422-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="12422-205">進入</span><span class="sxs-lookup"><span data-stu-id="12422-205">Entry</span></span> | <span data-ttu-id="12422-206">值</span><span class="sxs-lookup"><span data-stu-id="12422-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="12422-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12422-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12422-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="12422-209">System-Only</span></span>            | <span data-ttu-id="12422-210">對</span><span class="sxs-lookup"><span data-stu-id="12422-210">True</span></span>                                        |
| <span data-ttu-id="12422-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12422-211">Is-Single-Valued</span></span>       | <span data-ttu-id="12422-212">否</span><span class="sxs-lookup"><span data-stu-id="12422-212">False</span></span>                                       |
| <span data-ttu-id="12422-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12422-213">Is Indexed</span></span>             | <span data-ttu-id="12422-214">否</span><span class="sxs-lookup"><span data-stu-id="12422-214">False</span></span>                                       |
| <span data-ttu-id="12422-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12422-215">In Global Catalog</span></span>      | <span data-ttu-id="12422-216">否</span><span class="sxs-lookup"><span data-stu-id="12422-216">False</span></span>                                       |
| <span data-ttu-id="12422-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12422-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="12422-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12422-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="12422-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12422-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="12422-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12422-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="12422-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-221">Search-Flags</span></span>           | <span data-ttu-id="12422-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12422-222">0x00000000</span></span>                                  |
| <span data-ttu-id="12422-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-223">System-Flags</span></span>           | <span data-ttu-id="12422-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12422-224">0x08000014</span></span>                                  |
| <span data-ttu-id="12422-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12422-225">Classes used in</span></span>        | [<span data-ttu-id="12422-226">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="12422-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="12422-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12422-227">Windows Server 2008</span></span>



| <span data-ttu-id="12422-228">進入</span><span class="sxs-lookup"><span data-stu-id="12422-228">Entry</span></span> | <span data-ttu-id="12422-229">值</span><span class="sxs-lookup"><span data-stu-id="12422-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="12422-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12422-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12422-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="12422-232">System-Only</span></span>            | <span data-ttu-id="12422-233">對</span><span class="sxs-lookup"><span data-stu-id="12422-233">True</span></span>                                        |
| <span data-ttu-id="12422-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12422-234">Is-Single-Valued</span></span>       | <span data-ttu-id="12422-235">否</span><span class="sxs-lookup"><span data-stu-id="12422-235">False</span></span>                                       |
| <span data-ttu-id="12422-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12422-236">Is Indexed</span></span>             | <span data-ttu-id="12422-237">否</span><span class="sxs-lookup"><span data-stu-id="12422-237">False</span></span>                                       |
| <span data-ttu-id="12422-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12422-238">In Global Catalog</span></span>      | <span data-ttu-id="12422-239">否</span><span class="sxs-lookup"><span data-stu-id="12422-239">False</span></span>                                       |
| <span data-ttu-id="12422-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12422-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="12422-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12422-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="12422-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12422-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="12422-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12422-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="12422-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-244">Search-Flags</span></span>           | <span data-ttu-id="12422-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12422-245">0x00000000</span></span>                                  |
| <span data-ttu-id="12422-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-246">System-Flags</span></span>           | <span data-ttu-id="12422-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12422-247">0x08000014</span></span>                                  |
| <span data-ttu-id="12422-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12422-248">Classes used in</span></span>        | [<span data-ttu-id="12422-249">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="12422-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="12422-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12422-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="12422-251">進入</span><span class="sxs-lookup"><span data-stu-id="12422-251">Entry</span></span> | <span data-ttu-id="12422-252">值</span><span class="sxs-lookup"><span data-stu-id="12422-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="12422-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12422-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12422-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="12422-255">System-Only</span></span>            | <span data-ttu-id="12422-256">對</span><span class="sxs-lookup"><span data-stu-id="12422-256">True</span></span>                                        |
| <span data-ttu-id="12422-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12422-257">Is-Single-Valued</span></span>       | <span data-ttu-id="12422-258">否</span><span class="sxs-lookup"><span data-stu-id="12422-258">False</span></span>                                       |
| <span data-ttu-id="12422-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12422-259">Is Indexed</span></span>             | <span data-ttu-id="12422-260">否</span><span class="sxs-lookup"><span data-stu-id="12422-260">False</span></span>                                       |
| <span data-ttu-id="12422-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12422-261">In Global Catalog</span></span>      | <span data-ttu-id="12422-262">否</span><span class="sxs-lookup"><span data-stu-id="12422-262">False</span></span>                                       |
| <span data-ttu-id="12422-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12422-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="12422-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12422-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="12422-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12422-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="12422-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12422-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="12422-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-267">Search-Flags</span></span>           | <span data-ttu-id="12422-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12422-268">0x00000000</span></span>                                  |
| <span data-ttu-id="12422-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-269">System-Flags</span></span>           | <span data-ttu-id="12422-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12422-270">0x08000014</span></span>                                  |
| <span data-ttu-id="12422-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12422-271">Classes used in</span></span>        | [<span data-ttu-id="12422-272">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="12422-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="12422-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12422-273">Windows Server 2012</span></span>



| <span data-ttu-id="12422-274">進入</span><span class="sxs-lookup"><span data-stu-id="12422-274">Entry</span></span> | <span data-ttu-id="12422-275">值</span><span class="sxs-lookup"><span data-stu-id="12422-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="12422-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12422-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12422-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="12422-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="12422-278">System-Only</span></span>            | <span data-ttu-id="12422-279">對</span><span class="sxs-lookup"><span data-stu-id="12422-279">True</span></span>                                        |
| <span data-ttu-id="12422-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12422-280">Is-Single-Valued</span></span>       | <span data-ttu-id="12422-281">否</span><span class="sxs-lookup"><span data-stu-id="12422-281">False</span></span>                                       |
| <span data-ttu-id="12422-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12422-282">Is Indexed</span></span>             | <span data-ttu-id="12422-283">否</span><span class="sxs-lookup"><span data-stu-id="12422-283">False</span></span>                                       |
| <span data-ttu-id="12422-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12422-284">In Global Catalog</span></span>      | <span data-ttu-id="12422-285">否</span><span class="sxs-lookup"><span data-stu-id="12422-285">False</span></span>                                       |
| <span data-ttu-id="12422-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12422-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="12422-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12422-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="12422-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12422-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="12422-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12422-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="12422-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-290">Search-Flags</span></span>           | <span data-ttu-id="12422-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12422-291">0x00000000</span></span>                                  |
| <span data-ttu-id="12422-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12422-292">System-Flags</span></span>           | <span data-ttu-id="12422-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12422-293">0x08000014</span></span>                                  |
| <span data-ttu-id="12422-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12422-294">Classes used in</span></span>        | [<span data-ttu-id="12422-295">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="12422-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





