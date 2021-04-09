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
# <a name="object-classes-attribute"></a><span data-ttu-id="673e0-106">Object-Classes 屬性</span><span class="sxs-lookup"><span data-stu-id="673e0-106">Object-Classes attribute</span></span>

<span data-ttu-id="673e0-107">多值屬性，其中包含表示架構中每個類別的字串。</span><span class="sxs-lookup"><span data-stu-id="673e0-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="673e0-108">每個值都包含 governsID、lDAPDisplayName、mustContain、mayContain 等等。</span><span class="sxs-lookup"><span data-stu-id="673e0-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="673e0-109">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-109">Entry</span></span> | <span data-ttu-id="673e0-110">值</span><span class="sxs-lookup"><span data-stu-id="673e0-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="673e0-111">CN</span><span class="sxs-lookup"><span data-stu-id="673e0-111">CN</span></span>                | <span data-ttu-id="673e0-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="673e0-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="673e0-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="673e0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="673e0-114">objectClasses</span><span class="sxs-lookup"><span data-stu-id="673e0-114">objectClasses</span></span>                                    |
| <span data-ttu-id="673e0-115">大小</span><span class="sxs-lookup"><span data-stu-id="673e0-115">Size</span></span>              | <span data-ttu-id="673e0-116">每個類別名稱平均大約20個位元組。</span><span class="sxs-lookup"><span data-stu-id="673e0-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="673e0-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="673e0-117">Update Privilege</span></span>  | <span data-ttu-id="673e0-118">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="673e0-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="673e0-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="673e0-119">Update Frequency</span></span>  | <span data-ttu-id="673e0-120">每當類別的設計變更時。</span><span class="sxs-lookup"><span data-stu-id="673e0-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="673e0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-121">Attribute-Id</span></span>      | <span data-ttu-id="673e0-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="673e0-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="673e0-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="673e0-123">System-Id-Guid</span></span>    | <span data-ttu-id="673e0-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="673e0-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="673e0-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="673e0-125">Syntax</span></span>            | [<span data-ttu-id="673e0-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="673e0-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="673e0-127">實作</span><span class="sxs-lookup"><span data-stu-id="673e0-127">Implementations</span></span>

-   [<span data-ttu-id="673e0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="673e0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="673e0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="673e0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="673e0-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="673e0-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="673e0-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="673e0-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="673e0-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="673e0-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="673e0-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="673e0-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="673e0-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="673e0-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="673e0-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="673e0-135">Windows 2000 Server</span></span>



| <span data-ttu-id="673e0-136">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-136">Entry</span></span> | <span data-ttu-id="673e0-137">值</span><span class="sxs-lookup"><span data-stu-id="673e0-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="673e0-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="673e0-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="673e0-140">System-Only</span></span>            | <span data-ttu-id="673e0-141">對</span><span class="sxs-lookup"><span data-stu-id="673e0-141">True</span></span>                                        |
| <span data-ttu-id="673e0-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="673e0-142">Is-Single-Valued</span></span>       | <span data-ttu-id="673e0-143">否</span><span class="sxs-lookup"><span data-stu-id="673e0-143">False</span></span>                                       |
| <span data-ttu-id="673e0-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="673e0-144">Is Indexed</span></span>             | <span data-ttu-id="673e0-145">否</span><span class="sxs-lookup"><span data-stu-id="673e0-145">False</span></span>                                       |
| <span data-ttu-id="673e0-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="673e0-146">In Global Catalog</span></span>      | <span data-ttu-id="673e0-147">否</span><span class="sxs-lookup"><span data-stu-id="673e0-147">False</span></span>                                       |
| <span data-ttu-id="673e0-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="673e0-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="673e0-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="673e0-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="673e0-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="673e0-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="673e0-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="673e0-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="673e0-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-152">Search-Flags</span></span>           | <span data-ttu-id="673e0-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="673e0-153">0x00000000</span></span>                                  |
| <span data-ttu-id="673e0-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-154">System-Flags</span></span>           | <span data-ttu-id="673e0-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="673e0-155">0x08000014</span></span>                                  |
| <span data-ttu-id="673e0-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="673e0-156">Classes used in</span></span>        | [<span data-ttu-id="673e0-157">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="673e0-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="673e0-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="673e0-158">Windows Server 2003</span></span>



| <span data-ttu-id="673e0-159">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-159">Entry</span></span> | <span data-ttu-id="673e0-160">值</span><span class="sxs-lookup"><span data-stu-id="673e0-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="673e0-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="673e0-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="673e0-163">System-Only</span></span>            | <span data-ttu-id="673e0-164">對</span><span class="sxs-lookup"><span data-stu-id="673e0-164">True</span></span>                                        |
| <span data-ttu-id="673e0-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="673e0-165">Is-Single-Valued</span></span>       | <span data-ttu-id="673e0-166">否</span><span class="sxs-lookup"><span data-stu-id="673e0-166">False</span></span>                                       |
| <span data-ttu-id="673e0-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="673e0-167">Is Indexed</span></span>             | <span data-ttu-id="673e0-168">否</span><span class="sxs-lookup"><span data-stu-id="673e0-168">False</span></span>                                       |
| <span data-ttu-id="673e0-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="673e0-169">In Global Catalog</span></span>      | <span data-ttu-id="673e0-170">否</span><span class="sxs-lookup"><span data-stu-id="673e0-170">False</span></span>                                       |
| <span data-ttu-id="673e0-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="673e0-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="673e0-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="673e0-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="673e0-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="673e0-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="673e0-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="673e0-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="673e0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-175">Search-Flags</span></span>           | <span data-ttu-id="673e0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="673e0-176">0x00000000</span></span>                                  |
| <span data-ttu-id="673e0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-177">System-Flags</span></span>           | <span data-ttu-id="673e0-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="673e0-178">0x08000014</span></span>                                  |
| <span data-ttu-id="673e0-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="673e0-179">Classes used in</span></span>        | [<span data-ttu-id="673e0-180">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="673e0-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="673e0-181">亞當</span><span class="sxs-lookup"><span data-stu-id="673e0-181">ADAM</span></span>



| <span data-ttu-id="673e0-182">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-182">Entry</span></span> | <span data-ttu-id="673e0-183">值</span><span class="sxs-lookup"><span data-stu-id="673e0-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="673e0-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="673e0-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="673e0-186">System-Only</span></span>            | <span data-ttu-id="673e0-187">對</span><span class="sxs-lookup"><span data-stu-id="673e0-187">True</span></span>                                        |
| <span data-ttu-id="673e0-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="673e0-188">Is-Single-Valued</span></span>       | <span data-ttu-id="673e0-189">否</span><span class="sxs-lookup"><span data-stu-id="673e0-189">False</span></span>                                       |
| <span data-ttu-id="673e0-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="673e0-190">Is Indexed</span></span>             | <span data-ttu-id="673e0-191">否</span><span class="sxs-lookup"><span data-stu-id="673e0-191">False</span></span>                                       |
| <span data-ttu-id="673e0-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="673e0-192">In Global Catalog</span></span>      | <span data-ttu-id="673e0-193">否</span><span class="sxs-lookup"><span data-stu-id="673e0-193">False</span></span>                                       |
| <span data-ttu-id="673e0-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="673e0-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="673e0-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="673e0-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="673e0-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="673e0-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="673e0-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="673e0-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="673e0-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-198">Search-Flags</span></span>           | <span data-ttu-id="673e0-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="673e0-199">0x00000000</span></span>                                  |
| <span data-ttu-id="673e0-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-200">System-Flags</span></span>           | <span data-ttu-id="673e0-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="673e0-201">0x08000014</span></span>                                  |
| <span data-ttu-id="673e0-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="673e0-202">Classes used in</span></span>        | [<span data-ttu-id="673e0-203">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="673e0-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="673e0-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="673e0-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="673e0-205">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-205">Entry</span></span> | <span data-ttu-id="673e0-206">值</span><span class="sxs-lookup"><span data-stu-id="673e0-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="673e0-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="673e0-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="673e0-209">System-Only</span></span>            | <span data-ttu-id="673e0-210">對</span><span class="sxs-lookup"><span data-stu-id="673e0-210">True</span></span>                                        |
| <span data-ttu-id="673e0-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="673e0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="673e0-212">否</span><span class="sxs-lookup"><span data-stu-id="673e0-212">False</span></span>                                       |
| <span data-ttu-id="673e0-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="673e0-213">Is Indexed</span></span>             | <span data-ttu-id="673e0-214">否</span><span class="sxs-lookup"><span data-stu-id="673e0-214">False</span></span>                                       |
| <span data-ttu-id="673e0-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="673e0-215">In Global Catalog</span></span>      | <span data-ttu-id="673e0-216">否</span><span class="sxs-lookup"><span data-stu-id="673e0-216">False</span></span>                                       |
| <span data-ttu-id="673e0-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="673e0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="673e0-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="673e0-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="673e0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="673e0-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="673e0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="673e0-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="673e0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-221">Search-Flags</span></span>           | <span data-ttu-id="673e0-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="673e0-222">0x00000000</span></span>                                  |
| <span data-ttu-id="673e0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-223">System-Flags</span></span>           | <span data-ttu-id="673e0-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="673e0-224">0x08000014</span></span>                                  |
| <span data-ttu-id="673e0-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="673e0-225">Classes used in</span></span>        | [<span data-ttu-id="673e0-226">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="673e0-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="673e0-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="673e0-227">Windows Server 2008</span></span>



| <span data-ttu-id="673e0-228">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-228">Entry</span></span> | <span data-ttu-id="673e0-229">值</span><span class="sxs-lookup"><span data-stu-id="673e0-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="673e0-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="673e0-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="673e0-232">System-Only</span></span>            | <span data-ttu-id="673e0-233">對</span><span class="sxs-lookup"><span data-stu-id="673e0-233">True</span></span>                                        |
| <span data-ttu-id="673e0-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="673e0-234">Is-Single-Valued</span></span>       | <span data-ttu-id="673e0-235">否</span><span class="sxs-lookup"><span data-stu-id="673e0-235">False</span></span>                                       |
| <span data-ttu-id="673e0-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="673e0-236">Is Indexed</span></span>             | <span data-ttu-id="673e0-237">否</span><span class="sxs-lookup"><span data-stu-id="673e0-237">False</span></span>                                       |
| <span data-ttu-id="673e0-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="673e0-238">In Global Catalog</span></span>      | <span data-ttu-id="673e0-239">否</span><span class="sxs-lookup"><span data-stu-id="673e0-239">False</span></span>                                       |
| <span data-ttu-id="673e0-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="673e0-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="673e0-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="673e0-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="673e0-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="673e0-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="673e0-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="673e0-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="673e0-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-244">Search-Flags</span></span>           | <span data-ttu-id="673e0-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="673e0-245">0x00000000</span></span>                                  |
| <span data-ttu-id="673e0-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-246">System-Flags</span></span>           | <span data-ttu-id="673e0-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="673e0-247">0x08000014</span></span>                                  |
| <span data-ttu-id="673e0-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="673e0-248">Classes used in</span></span>        | [<span data-ttu-id="673e0-249">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="673e0-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="673e0-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="673e0-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="673e0-251">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-251">Entry</span></span> | <span data-ttu-id="673e0-252">值</span><span class="sxs-lookup"><span data-stu-id="673e0-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="673e0-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="673e0-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="673e0-255">System-Only</span></span>            | <span data-ttu-id="673e0-256">對</span><span class="sxs-lookup"><span data-stu-id="673e0-256">True</span></span>                                        |
| <span data-ttu-id="673e0-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="673e0-257">Is-Single-Valued</span></span>       | <span data-ttu-id="673e0-258">否</span><span class="sxs-lookup"><span data-stu-id="673e0-258">False</span></span>                                       |
| <span data-ttu-id="673e0-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="673e0-259">Is Indexed</span></span>             | <span data-ttu-id="673e0-260">否</span><span class="sxs-lookup"><span data-stu-id="673e0-260">False</span></span>                                       |
| <span data-ttu-id="673e0-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="673e0-261">In Global Catalog</span></span>      | <span data-ttu-id="673e0-262">否</span><span class="sxs-lookup"><span data-stu-id="673e0-262">False</span></span>                                       |
| <span data-ttu-id="673e0-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="673e0-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="673e0-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="673e0-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="673e0-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="673e0-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="673e0-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="673e0-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="673e0-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-267">Search-Flags</span></span>           | <span data-ttu-id="673e0-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="673e0-268">0x00000000</span></span>                                  |
| <span data-ttu-id="673e0-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-269">System-Flags</span></span>           | <span data-ttu-id="673e0-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="673e0-270">0x08000014</span></span>                                  |
| <span data-ttu-id="673e0-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="673e0-271">Classes used in</span></span>        | [<span data-ttu-id="673e0-272">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="673e0-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="673e0-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="673e0-273">Windows Server 2012</span></span>



| <span data-ttu-id="673e0-274">進入</span><span class="sxs-lookup"><span data-stu-id="673e0-274">Entry</span></span> | <span data-ttu-id="673e0-275">值</span><span class="sxs-lookup"><span data-stu-id="673e0-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="673e0-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="673e0-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="673e0-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="673e0-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="673e0-278">System-Only</span></span>            | <span data-ttu-id="673e0-279">對</span><span class="sxs-lookup"><span data-stu-id="673e0-279">True</span></span>                                        |
| <span data-ttu-id="673e0-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="673e0-280">Is-Single-Valued</span></span>       | <span data-ttu-id="673e0-281">否</span><span class="sxs-lookup"><span data-stu-id="673e0-281">False</span></span>                                       |
| <span data-ttu-id="673e0-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="673e0-282">Is Indexed</span></span>             | <span data-ttu-id="673e0-283">否</span><span class="sxs-lookup"><span data-stu-id="673e0-283">False</span></span>                                       |
| <span data-ttu-id="673e0-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="673e0-284">In Global Catalog</span></span>      | <span data-ttu-id="673e0-285">否</span><span class="sxs-lookup"><span data-stu-id="673e0-285">False</span></span>                                       |
| <span data-ttu-id="673e0-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="673e0-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="673e0-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="673e0-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="673e0-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="673e0-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="673e0-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="673e0-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="673e0-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-290">Search-Flags</span></span>           | <span data-ttu-id="673e0-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="673e0-291">0x00000000</span></span>                                  |
| <span data-ttu-id="673e0-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="673e0-292">System-Flags</span></span>           | <span data-ttu-id="673e0-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="673e0-293">0x08000014</span></span>                                  |
| <span data-ttu-id="673e0-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="673e0-294">Classes used in</span></span>        | [<span data-ttu-id="673e0-295">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="673e0-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





