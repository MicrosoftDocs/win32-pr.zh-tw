---
title: Attribute-Types 屬性
description: 多值屬性，其中包含表示架構中每個屬性的字串。
ms.assetid: 37d48944-b573-4067-982c-2e57db040b54
ms.tgt_platform: multiple
keywords:
- Attribute-Types 屬性 AD 架構
- attributeTypes 屬性 AD 架構
topic_type:
- apiref
api_name:
- Attribute-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99f587f1704f7e2ea393279a8dbf0a20be10ef02
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991579"
---
# <a name="attribute-types-attribute"></a><span data-ttu-id="b9f84-105">Attribute-Types 屬性</span><span class="sxs-lookup"><span data-stu-id="b9f84-105">Attribute-Types attribute</span></span>

<span data-ttu-id="b9f84-106">多值屬性，其中包含表示架構中每個屬性的字串。</span><span class="sxs-lookup"><span data-stu-id="b9f84-106">A multi-valued property that contains strings that represent each attribute in the schema.</span></span>



| <span data-ttu-id="b9f84-107">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-107">Entry</span></span> | <span data-ttu-id="b9f84-108">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-109">CN</span><span class="sxs-lookup"><span data-stu-id="b9f84-109">CN</span></span>                | <span data-ttu-id="b9f84-110">Attribute-Types</span><span class="sxs-lookup"><span data-stu-id="b9f84-110">Attribute-Types</span></span>                             |
| <span data-ttu-id="b9f84-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b9f84-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b9f84-112">attributeTypes</span><span class="sxs-lookup"><span data-stu-id="b9f84-112">attributeTypes</span></span>                              |
| <span data-ttu-id="b9f84-113">大小</span><span class="sxs-lookup"><span data-stu-id="b9f84-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b9f84-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b9f84-114">Update Privilege</span></span>  | <span data-ttu-id="b9f84-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="b9f84-115">Schema administrator</span></span>                        |
| <span data-ttu-id="b9f84-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b9f84-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b9f84-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-117">Attribute-Id</span></span>      | <span data-ttu-id="b9f84-118">2.5.21.5</span><span class="sxs-lookup"><span data-stu-id="b9f84-118">2.5.21.5</span></span>                                    |
| <span data-ttu-id="b9f84-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b9f84-119">System-Id-Guid</span></span>    | <span data-ttu-id="b9f84-120">9a7ad944-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b9f84-120">9a7ad944-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="b9f84-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9f84-121">Syntax</span></span>            | [<span data-ttu-id="b9f84-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b9f84-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b9f84-123">實作</span><span class="sxs-lookup"><span data-stu-id="b9f84-123">Implementations</span></span>

-   [<span data-ttu-id="b9f84-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b9f84-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b9f84-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b9f84-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b9f84-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b9f84-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b9f84-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b9f84-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b9f84-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b9f84-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b9f84-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b9f84-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b9f84-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b9f84-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b9f84-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b9f84-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b9f84-132">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-132">Entry</span></span> | <span data-ttu-id="b9f84-133">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-133">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b9f84-134">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-135">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f84-136">System-Only</span></span>            | <span data-ttu-id="b9f84-137">對</span><span class="sxs-lookup"><span data-stu-id="b9f84-137">True</span></span>                                        |
| <span data-ttu-id="b9f84-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b9f84-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f84-139">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-139">False</span></span>                                       |
| <span data-ttu-id="b9f84-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b9f84-140">Is Indexed</span></span>             | <span data-ttu-id="b9f84-141">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-141">False</span></span>                                       |
| <span data-ttu-id="b9f84-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b9f84-142">In Global Catalog</span></span>      | <span data-ttu-id="b9f84-143">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-143">False</span></span>                                       |
| <span data-ttu-id="b9f84-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b9f84-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f84-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b9f84-145">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b9f84-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f84-146">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f84-147">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-148">Search-Flags</span></span>           | <span data-ttu-id="b9f84-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f84-149">0x00000000</span></span>                                  |
| <span data-ttu-id="b9f84-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-150">System-Flags</span></span>           | <span data-ttu-id="b9f84-151">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b9f84-151">0x08000014</span></span>                                  |
| <span data-ttu-id="b9f84-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b9f84-152">Classes used in</span></span>        | [<span data-ttu-id="b9f84-153">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b9f84-153">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b9f84-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9f84-154">Windows Server 2003</span></span>



| <span data-ttu-id="b9f84-155">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-155">Entry</span></span> | <span data-ttu-id="b9f84-156">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-156">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b9f84-157">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-158">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f84-159">System-Only</span></span>            | <span data-ttu-id="b9f84-160">對</span><span class="sxs-lookup"><span data-stu-id="b9f84-160">True</span></span>                                        |
| <span data-ttu-id="b9f84-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b9f84-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f84-162">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-162">False</span></span>                                       |
| <span data-ttu-id="b9f84-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b9f84-163">Is Indexed</span></span>             | <span data-ttu-id="b9f84-164">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-164">False</span></span>                                       |
| <span data-ttu-id="b9f84-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b9f84-165">In Global Catalog</span></span>      | <span data-ttu-id="b9f84-166">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-166">False</span></span>                                       |
| <span data-ttu-id="b9f84-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b9f84-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f84-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b9f84-168">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b9f84-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f84-169">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f84-170">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-171">Search-Flags</span></span>           | <span data-ttu-id="b9f84-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f84-172">0x00000000</span></span>                                  |
| <span data-ttu-id="b9f84-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-173">System-Flags</span></span>           | <span data-ttu-id="b9f84-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b9f84-174">0x08000014</span></span>                                  |
| <span data-ttu-id="b9f84-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b9f84-175">Classes used in</span></span>        | [<span data-ttu-id="b9f84-176">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b9f84-176">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b9f84-177">亞當</span><span class="sxs-lookup"><span data-stu-id="b9f84-177">ADAM</span></span>



| <span data-ttu-id="b9f84-178">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-178">Entry</span></span> | <span data-ttu-id="b9f84-179">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-179">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b9f84-180">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-181">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f84-182">System-Only</span></span>            | <span data-ttu-id="b9f84-183">對</span><span class="sxs-lookup"><span data-stu-id="b9f84-183">True</span></span>                                        |
| <span data-ttu-id="b9f84-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b9f84-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f84-185">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-185">False</span></span>                                       |
| <span data-ttu-id="b9f84-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b9f84-186">Is Indexed</span></span>             | <span data-ttu-id="b9f84-187">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-187">False</span></span>                                       |
| <span data-ttu-id="b9f84-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b9f84-188">In Global Catalog</span></span>      | <span data-ttu-id="b9f84-189">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-189">False</span></span>                                       |
| <span data-ttu-id="b9f84-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b9f84-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f84-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b9f84-191">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b9f84-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f84-192">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f84-193">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-194">Search-Flags</span></span>           | <span data-ttu-id="b9f84-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f84-195">0x00000000</span></span>                                  |
| <span data-ttu-id="b9f84-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-196">System-Flags</span></span>           | <span data-ttu-id="b9f84-197">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b9f84-197">0x08000014</span></span>                                  |
| <span data-ttu-id="b9f84-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b9f84-198">Classes used in</span></span>        | [<span data-ttu-id="b9f84-199">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b9f84-199">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b9f84-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b9f84-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b9f84-201">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-201">Entry</span></span> | <span data-ttu-id="b9f84-202">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-202">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b9f84-203">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-204">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f84-205">System-Only</span></span>            | <span data-ttu-id="b9f84-206">對</span><span class="sxs-lookup"><span data-stu-id="b9f84-206">True</span></span>                                        |
| <span data-ttu-id="b9f84-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b9f84-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f84-208">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-208">False</span></span>                                       |
| <span data-ttu-id="b9f84-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b9f84-209">Is Indexed</span></span>             | <span data-ttu-id="b9f84-210">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-210">False</span></span>                                       |
| <span data-ttu-id="b9f84-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b9f84-211">In Global Catalog</span></span>      | <span data-ttu-id="b9f84-212">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-212">False</span></span>                                       |
| <span data-ttu-id="b9f84-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b9f84-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f84-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b9f84-214">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b9f84-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f84-215">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f84-216">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-217">Search-Flags</span></span>           | <span data-ttu-id="b9f84-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f84-218">0x00000000</span></span>                                  |
| <span data-ttu-id="b9f84-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-219">System-Flags</span></span>           | <span data-ttu-id="b9f84-220">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b9f84-220">0x08000014</span></span>                                  |
| <span data-ttu-id="b9f84-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b9f84-221">Classes used in</span></span>        | [<span data-ttu-id="b9f84-222">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b9f84-222">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b9f84-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9f84-223">Windows Server 2008</span></span>



| <span data-ttu-id="b9f84-224">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-224">Entry</span></span> | <span data-ttu-id="b9f84-225">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-225">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b9f84-226">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-227">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f84-228">System-Only</span></span>            | <span data-ttu-id="b9f84-229">對</span><span class="sxs-lookup"><span data-stu-id="b9f84-229">True</span></span>                                        |
| <span data-ttu-id="b9f84-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b9f84-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f84-231">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-231">False</span></span>                                       |
| <span data-ttu-id="b9f84-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b9f84-232">Is Indexed</span></span>             | <span data-ttu-id="b9f84-233">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-233">False</span></span>                                       |
| <span data-ttu-id="b9f84-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b9f84-234">In Global Catalog</span></span>      | <span data-ttu-id="b9f84-235">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-235">False</span></span>                                       |
| <span data-ttu-id="b9f84-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b9f84-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f84-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b9f84-237">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b9f84-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f84-238">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f84-239">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-240">Search-Flags</span></span>           | <span data-ttu-id="b9f84-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f84-241">0x00000000</span></span>                                  |
| <span data-ttu-id="b9f84-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-242">System-Flags</span></span>           | <span data-ttu-id="b9f84-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b9f84-243">0x08000014</span></span>                                  |
| <span data-ttu-id="b9f84-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b9f84-244">Classes used in</span></span>        | [<span data-ttu-id="b9f84-245">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b9f84-245">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b9f84-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9f84-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b9f84-247">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-247">Entry</span></span> | <span data-ttu-id="b9f84-248">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-248">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b9f84-249">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-250">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f84-251">System-Only</span></span>            | <span data-ttu-id="b9f84-252">對</span><span class="sxs-lookup"><span data-stu-id="b9f84-252">True</span></span>                                        |
| <span data-ttu-id="b9f84-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b9f84-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f84-254">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-254">False</span></span>                                       |
| <span data-ttu-id="b9f84-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b9f84-255">Is Indexed</span></span>             | <span data-ttu-id="b9f84-256">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-256">False</span></span>                                       |
| <span data-ttu-id="b9f84-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b9f84-257">In Global Catalog</span></span>      | <span data-ttu-id="b9f84-258">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-258">False</span></span>                                       |
| <span data-ttu-id="b9f84-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b9f84-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f84-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b9f84-260">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b9f84-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f84-261">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f84-262">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-263">Search-Flags</span></span>           | <span data-ttu-id="b9f84-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f84-264">0x00000000</span></span>                                  |
| <span data-ttu-id="b9f84-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-265">System-Flags</span></span>           | <span data-ttu-id="b9f84-266">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b9f84-266">0x08000014</span></span>                                  |
| <span data-ttu-id="b9f84-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b9f84-267">Classes used in</span></span>        | [<span data-ttu-id="b9f84-268">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b9f84-268">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b9f84-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9f84-269">Windows Server 2012</span></span>



| <span data-ttu-id="b9f84-270">進入</span><span class="sxs-lookup"><span data-stu-id="b9f84-270">Entry</span></span> | <span data-ttu-id="b9f84-271">值</span><span class="sxs-lookup"><span data-stu-id="b9f84-271">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b9f84-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b9f84-272">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f84-273">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b9f84-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f84-274">System-Only</span></span>            | <span data-ttu-id="b9f84-275">對</span><span class="sxs-lookup"><span data-stu-id="b9f84-275">True</span></span>                                        |
| <span data-ttu-id="b9f84-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b9f84-276">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f84-277">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-277">False</span></span>                                       |
| <span data-ttu-id="b9f84-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b9f84-278">Is Indexed</span></span>             | <span data-ttu-id="b9f84-279">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-279">False</span></span>                                       |
| <span data-ttu-id="b9f84-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b9f84-280">In Global Catalog</span></span>      | <span data-ttu-id="b9f84-281">否</span><span class="sxs-lookup"><span data-stu-id="b9f84-281">False</span></span>                                       |
| <span data-ttu-id="b9f84-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b9f84-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f84-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b9f84-283">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b9f84-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f84-284">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f84-285">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b9f84-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-286">Search-Flags</span></span>           | <span data-ttu-id="b9f84-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f84-287">0x00000000</span></span>                                  |
| <span data-ttu-id="b9f84-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f84-288">System-Flags</span></span>           | <span data-ttu-id="b9f84-289">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b9f84-289">0x08000014</span></span>                                  |
| <span data-ttu-id="b9f84-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b9f84-290">Classes used in</span></span>        | [<span data-ttu-id="b9f84-291">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b9f84-291">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





