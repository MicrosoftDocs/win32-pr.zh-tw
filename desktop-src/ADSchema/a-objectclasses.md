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
# <a name="object-classes-attribute"></a><span data-ttu-id="4fbe5-106">Object-Classes 屬性</span><span class="sxs-lookup"><span data-stu-id="4fbe5-106">Object-Classes attribute</span></span>

<span data-ttu-id="4fbe5-107">多值屬性，其中包含表示架構中每個類別的字串。</span><span class="sxs-lookup"><span data-stu-id="4fbe5-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="4fbe5-108">每個值都包含 governsID、lDAPDisplayName、mustContain、mayContain 等等。</span><span class="sxs-lookup"><span data-stu-id="4fbe5-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="4fbe5-109">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-109">Entry</span></span> | <span data-ttu-id="4fbe5-110">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="4fbe5-111">CN</span><span class="sxs-lookup"><span data-stu-id="4fbe5-111">CN</span></span>                | <span data-ttu-id="4fbe5-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="4fbe5-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="4fbe5-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4fbe5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4fbe5-114">objectClasses</span><span class="sxs-lookup"><span data-stu-id="4fbe5-114">objectClasses</span></span>                                    |
| <span data-ttu-id="4fbe5-115">大小</span><span class="sxs-lookup"><span data-stu-id="4fbe5-115">Size</span></span>              | <span data-ttu-id="4fbe5-116">每個類別名稱平均大約20個位元組。</span><span class="sxs-lookup"><span data-stu-id="4fbe5-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="4fbe5-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4fbe5-117">Update Privilege</span></span>  | <span data-ttu-id="4fbe5-118">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="4fbe5-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="4fbe5-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4fbe5-119">Update Frequency</span></span>  | <span data-ttu-id="4fbe5-120">每當類別的設計變更時。</span><span class="sxs-lookup"><span data-stu-id="4fbe5-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="4fbe5-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-121">Attribute-Id</span></span>      | <span data-ttu-id="4fbe5-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="4fbe5-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="4fbe5-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4fbe5-123">System-Id-Guid</span></span>    | <span data-ttu-id="4fbe5-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="4fbe5-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="4fbe5-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fbe5-125">Syntax</span></span>            | [<span data-ttu-id="4fbe5-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="4fbe5-127">實作</span><span class="sxs-lookup"><span data-stu-id="4fbe5-127">Implementations</span></span>

-   [<span data-ttu-id="4fbe5-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4fbe5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4fbe5-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4fbe5-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4fbe5-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4fbe5-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4fbe5-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4fbe5-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4fbe5-135">Windows 2000 Server</span></span>



| <span data-ttu-id="4fbe5-136">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-136">Entry</span></span> | <span data-ttu-id="4fbe5-137">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4fbe5-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4fbe5-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fbe5-140">System-Only</span></span>            | <span data-ttu-id="4fbe5-141">對</span><span class="sxs-lookup"><span data-stu-id="4fbe5-141">True</span></span>                                        |
| <span data-ttu-id="4fbe5-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4fbe5-143">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-143">False</span></span>                                       |
| <span data-ttu-id="4fbe5-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4fbe5-144">Is Indexed</span></span>             | <span data-ttu-id="4fbe5-145">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-145">False</span></span>                                       |
| <span data-ttu-id="4fbe5-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4fbe5-146">In Global Catalog</span></span>      | <span data-ttu-id="4fbe5-147">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-147">False</span></span>                                       |
| <span data-ttu-id="4fbe5-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4fbe5-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fbe5-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4fbe5-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4fbe5-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fbe5-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fbe5-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-152">Search-Flags</span></span>           | <span data-ttu-id="4fbe5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fbe5-153">0x00000000</span></span>                                  |
| <span data-ttu-id="4fbe5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-154">System-Flags</span></span>           | <span data-ttu-id="4fbe5-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4fbe5-155">0x08000014</span></span>                                  |
| <span data-ttu-id="4fbe5-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4fbe5-156">Classes used in</span></span>        | [<span data-ttu-id="4fbe5-157">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4fbe5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4fbe5-158">Windows Server 2003</span></span>



| <span data-ttu-id="4fbe5-159">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-159">Entry</span></span> | <span data-ttu-id="4fbe5-160">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4fbe5-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4fbe5-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fbe5-163">System-Only</span></span>            | <span data-ttu-id="4fbe5-164">對</span><span class="sxs-lookup"><span data-stu-id="4fbe5-164">True</span></span>                                        |
| <span data-ttu-id="4fbe5-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4fbe5-166">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-166">False</span></span>                                       |
| <span data-ttu-id="4fbe5-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4fbe5-167">Is Indexed</span></span>             | <span data-ttu-id="4fbe5-168">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-168">False</span></span>                                       |
| <span data-ttu-id="4fbe5-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4fbe5-169">In Global Catalog</span></span>      | <span data-ttu-id="4fbe5-170">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-170">False</span></span>                                       |
| <span data-ttu-id="4fbe5-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4fbe5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fbe5-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4fbe5-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4fbe5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fbe5-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fbe5-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-175">Search-Flags</span></span>           | <span data-ttu-id="4fbe5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fbe5-176">0x00000000</span></span>                                  |
| <span data-ttu-id="4fbe5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-177">System-Flags</span></span>           | <span data-ttu-id="4fbe5-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4fbe5-178">0x08000014</span></span>                                  |
| <span data-ttu-id="4fbe5-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4fbe5-179">Classes used in</span></span>        | [<span data-ttu-id="4fbe5-180">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4fbe5-181">亞當</span><span class="sxs-lookup"><span data-stu-id="4fbe5-181">ADAM</span></span>



| <span data-ttu-id="4fbe5-182">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-182">Entry</span></span> | <span data-ttu-id="4fbe5-183">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4fbe5-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4fbe5-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fbe5-186">System-Only</span></span>            | <span data-ttu-id="4fbe5-187">對</span><span class="sxs-lookup"><span data-stu-id="4fbe5-187">True</span></span>                                        |
| <span data-ttu-id="4fbe5-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-188">Is-Single-Valued</span></span>       | <span data-ttu-id="4fbe5-189">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-189">False</span></span>                                       |
| <span data-ttu-id="4fbe5-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4fbe5-190">Is Indexed</span></span>             | <span data-ttu-id="4fbe5-191">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-191">False</span></span>                                       |
| <span data-ttu-id="4fbe5-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4fbe5-192">In Global Catalog</span></span>      | <span data-ttu-id="4fbe5-193">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-193">False</span></span>                                       |
| <span data-ttu-id="4fbe5-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4fbe5-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fbe5-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4fbe5-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4fbe5-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fbe5-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fbe5-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-198">Search-Flags</span></span>           | <span data-ttu-id="4fbe5-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fbe5-199">0x00000000</span></span>                                  |
| <span data-ttu-id="4fbe5-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-200">System-Flags</span></span>           | <span data-ttu-id="4fbe5-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4fbe5-201">0x08000014</span></span>                                  |
| <span data-ttu-id="4fbe5-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4fbe5-202">Classes used in</span></span>        | [<span data-ttu-id="4fbe5-203">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4fbe5-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4fbe5-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4fbe5-205">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-205">Entry</span></span> | <span data-ttu-id="4fbe5-206">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4fbe5-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4fbe5-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fbe5-209">System-Only</span></span>            | <span data-ttu-id="4fbe5-210">對</span><span class="sxs-lookup"><span data-stu-id="4fbe5-210">True</span></span>                                        |
| <span data-ttu-id="4fbe5-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-211">Is-Single-Valued</span></span>       | <span data-ttu-id="4fbe5-212">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-212">False</span></span>                                       |
| <span data-ttu-id="4fbe5-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4fbe5-213">Is Indexed</span></span>             | <span data-ttu-id="4fbe5-214">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-214">False</span></span>                                       |
| <span data-ttu-id="4fbe5-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4fbe5-215">In Global Catalog</span></span>      | <span data-ttu-id="4fbe5-216">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-216">False</span></span>                                       |
| <span data-ttu-id="4fbe5-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4fbe5-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fbe5-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4fbe5-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4fbe5-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fbe5-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fbe5-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-221">Search-Flags</span></span>           | <span data-ttu-id="4fbe5-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fbe5-222">0x00000000</span></span>                                  |
| <span data-ttu-id="4fbe5-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-223">System-Flags</span></span>           | <span data-ttu-id="4fbe5-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4fbe5-224">0x08000014</span></span>                                  |
| <span data-ttu-id="4fbe5-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4fbe5-225">Classes used in</span></span>        | [<span data-ttu-id="4fbe5-226">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4fbe5-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fbe5-227">Windows Server 2008</span></span>



| <span data-ttu-id="4fbe5-228">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-228">Entry</span></span> | <span data-ttu-id="4fbe5-229">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4fbe5-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4fbe5-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fbe5-232">System-Only</span></span>            | <span data-ttu-id="4fbe5-233">對</span><span class="sxs-lookup"><span data-stu-id="4fbe5-233">True</span></span>                                        |
| <span data-ttu-id="4fbe5-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4fbe5-235">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-235">False</span></span>                                       |
| <span data-ttu-id="4fbe5-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4fbe5-236">Is Indexed</span></span>             | <span data-ttu-id="4fbe5-237">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-237">False</span></span>                                       |
| <span data-ttu-id="4fbe5-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4fbe5-238">In Global Catalog</span></span>      | <span data-ttu-id="4fbe5-239">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-239">False</span></span>                                       |
| <span data-ttu-id="4fbe5-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4fbe5-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fbe5-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4fbe5-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4fbe5-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fbe5-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fbe5-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-244">Search-Flags</span></span>           | <span data-ttu-id="4fbe5-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fbe5-245">0x00000000</span></span>                                  |
| <span data-ttu-id="4fbe5-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-246">System-Flags</span></span>           | <span data-ttu-id="4fbe5-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4fbe5-247">0x08000014</span></span>                                  |
| <span data-ttu-id="4fbe5-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4fbe5-248">Classes used in</span></span>        | [<span data-ttu-id="4fbe5-249">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4fbe5-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fbe5-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4fbe5-251">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-251">Entry</span></span> | <span data-ttu-id="4fbe5-252">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4fbe5-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4fbe5-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fbe5-255">System-Only</span></span>            | <span data-ttu-id="4fbe5-256">對</span><span class="sxs-lookup"><span data-stu-id="4fbe5-256">True</span></span>                                        |
| <span data-ttu-id="4fbe5-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-257">Is-Single-Valued</span></span>       | <span data-ttu-id="4fbe5-258">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-258">False</span></span>                                       |
| <span data-ttu-id="4fbe5-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4fbe5-259">Is Indexed</span></span>             | <span data-ttu-id="4fbe5-260">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-260">False</span></span>                                       |
| <span data-ttu-id="4fbe5-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4fbe5-261">In Global Catalog</span></span>      | <span data-ttu-id="4fbe5-262">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-262">False</span></span>                                       |
| <span data-ttu-id="4fbe5-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4fbe5-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fbe5-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4fbe5-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4fbe5-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fbe5-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fbe5-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-267">Search-Flags</span></span>           | <span data-ttu-id="4fbe5-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fbe5-268">0x00000000</span></span>                                  |
| <span data-ttu-id="4fbe5-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-269">System-Flags</span></span>           | <span data-ttu-id="4fbe5-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4fbe5-270">0x08000014</span></span>                                  |
| <span data-ttu-id="4fbe5-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4fbe5-271">Classes used in</span></span>        | [<span data-ttu-id="4fbe5-272">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4fbe5-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4fbe5-273">Windows Server 2012</span></span>



| <span data-ttu-id="4fbe5-274">進入</span><span class="sxs-lookup"><span data-stu-id="4fbe5-274">Entry</span></span> | <span data-ttu-id="4fbe5-275">值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="4fbe5-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4fbe5-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fbe5-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="4fbe5-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fbe5-278">System-Only</span></span>            | <span data-ttu-id="4fbe5-279">對</span><span class="sxs-lookup"><span data-stu-id="4fbe5-279">True</span></span>                                        |
| <span data-ttu-id="4fbe5-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4fbe5-280">Is-Single-Valued</span></span>       | <span data-ttu-id="4fbe5-281">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-281">False</span></span>                                       |
| <span data-ttu-id="4fbe5-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4fbe5-282">Is Indexed</span></span>             | <span data-ttu-id="4fbe5-283">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-283">False</span></span>                                       |
| <span data-ttu-id="4fbe5-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4fbe5-284">In Global Catalog</span></span>      | <span data-ttu-id="4fbe5-285">否</span><span class="sxs-lookup"><span data-stu-id="4fbe5-285">False</span></span>                                       |
| <span data-ttu-id="4fbe5-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4fbe5-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fbe5-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4fbe5-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="4fbe5-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fbe5-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fbe5-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="4fbe5-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-290">Search-Flags</span></span>           | <span data-ttu-id="4fbe5-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fbe5-291">0x00000000</span></span>                                  |
| <span data-ttu-id="4fbe5-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fbe5-292">System-Flags</span></span>           | <span data-ttu-id="4fbe5-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="4fbe5-293">0x08000014</span></span>                                  |
| <span data-ttu-id="4fbe5-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4fbe5-294">Classes used in</span></span>        | [<span data-ttu-id="4fbe5-295">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="4fbe5-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





