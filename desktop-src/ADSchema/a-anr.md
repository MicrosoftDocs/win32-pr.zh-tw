---
title: ANR 屬性
description: 在物件之間進行選擇時，要使用的明確名稱解析屬性。
ms.assetid: 9057dc7e-f669-4821-86b0-703ff7e5b120
ms.tgt_platform: multiple
keywords:
- ANR 屬性 AD 架構
- aNR 屬性 AD 架構
topic_type:
- apiref
api_name:
- ANR
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28efc6d6871eb737f9c1953fbdb5ad5798f7fd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467382"
---
# <a name="anr-attribute"></a><span data-ttu-id="218ee-105">ANR 屬性</span><span class="sxs-lookup"><span data-stu-id="218ee-105">ANR attribute</span></span>

<span data-ttu-id="218ee-106">在物件之間進行選擇時，要使用的明確名稱解析屬性。</span><span class="sxs-lookup"><span data-stu-id="218ee-106">Ambiguous name resolution attribute to be used when choosing between objects.</span></span>



| <span data-ttu-id="218ee-107">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-107">Entry</span></span> | <span data-ttu-id="218ee-108">值</span><span class="sxs-lookup"><span data-stu-id="218ee-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="218ee-109">CN</span><span class="sxs-lookup"><span data-stu-id="218ee-109">CN</span></span>                | <span data-ttu-id="218ee-110">Anr</span><span class="sxs-lookup"><span data-stu-id="218ee-110">ANR</span></span>                                                               |
| <span data-ttu-id="218ee-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="218ee-111">Ldap-Display-Name</span></span> | <span data-ttu-id="218ee-112">Anr</span><span class="sxs-lookup"><span data-stu-id="218ee-112">aNR</span></span>                                                               |
| <span data-ttu-id="218ee-113">大小</span><span class="sxs-lookup"><span data-stu-id="218ee-113">Size</span></span>              | \-                                                                |
| <span data-ttu-id="218ee-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="218ee-114">Update Privilege</span></span>  | <span data-ttu-id="218ee-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="218ee-115">Schema administrator</span></span>                                              |
| <span data-ttu-id="218ee-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="218ee-116">Update Frequency</span></span>  | <span data-ttu-id="218ee-117">當需要在 ANR 清單中新增或移除屬性時。</span><span class="sxs-lookup"><span data-stu-id="218ee-117">When an attribute needs to be added or removed from the ANR list.</span></span> |
| <span data-ttu-id="218ee-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-118">Attribute-Id</span></span>      | <span data-ttu-id="218ee-119">1.2.840.113556.1.4.1208</span><span class="sxs-lookup"><span data-stu-id="218ee-119">1.2.840.113556.1.4.1208</span></span>                                           |
| <span data-ttu-id="218ee-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="218ee-120">System-Id-Guid</span></span>    | <span data-ttu-id="218ee-121">45b01500-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="218ee-121">45b01500-c419-11d1-bbc9-0080c76670c0</span></span>                              |
| <span data-ttu-id="218ee-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="218ee-122">Syntax</span></span>            | [<span data-ttu-id="218ee-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="218ee-123">**String(Unicode)**</span></span>](s-string-unicode.md)                       |



## <a name="implementations"></a><span data-ttu-id="218ee-124">實作</span><span class="sxs-lookup"><span data-stu-id="218ee-124">Implementations</span></span>

-   [<span data-ttu-id="218ee-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="218ee-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="218ee-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="218ee-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="218ee-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="218ee-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="218ee-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="218ee-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="218ee-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="218ee-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="218ee-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="218ee-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="218ee-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="218ee-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="218ee-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="218ee-132">Windows 2000 Server</span></span>



| <span data-ttu-id="218ee-133">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-133">Entry</span></span> | <span data-ttu-id="218ee-134">值</span><span class="sxs-lookup"><span data-stu-id="218ee-134">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="218ee-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="218ee-135">Link-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-136">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="218ee-137">System-Only</span></span>            | <span data-ttu-id="218ee-138">否</span><span class="sxs-lookup"><span data-stu-id="218ee-138">False</span></span>        |
| <span data-ttu-id="218ee-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="218ee-139">Is-Single-Valued</span></span>       | <span data-ttu-id="218ee-140">對</span><span class="sxs-lookup"><span data-stu-id="218ee-140">True</span></span>         |
| <span data-ttu-id="218ee-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="218ee-141">Is Indexed</span></span>             | <span data-ttu-id="218ee-142">否</span><span class="sxs-lookup"><span data-stu-id="218ee-142">False</span></span>        |
| <span data-ttu-id="218ee-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="218ee-143">In Global Catalog</span></span>      | <span data-ttu-id="218ee-144">否</span><span class="sxs-lookup"><span data-stu-id="218ee-144">False</span></span>        |
| <span data-ttu-id="218ee-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="218ee-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="218ee-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="218ee-146">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="218ee-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="218ee-147">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="218ee-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="218ee-148">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="218ee-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-149">Search-Flags</span></span>           | <span data-ttu-id="218ee-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="218ee-150">0x00000000</span></span>   |
| <span data-ttu-id="218ee-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-151">System-Flags</span></span>           | <span data-ttu-id="218ee-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="218ee-152">0x08000014</span></span>   |
| <span data-ttu-id="218ee-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="218ee-153">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="218ee-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="218ee-154">Windows Server 2003</span></span>



| <span data-ttu-id="218ee-155">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-155">Entry</span></span> | <span data-ttu-id="218ee-156">值</span><span class="sxs-lookup"><span data-stu-id="218ee-156">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="218ee-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="218ee-157">Link-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-158">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="218ee-159">System-Only</span></span>            | <span data-ttu-id="218ee-160">否</span><span class="sxs-lookup"><span data-stu-id="218ee-160">False</span></span>        |
| <span data-ttu-id="218ee-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="218ee-161">Is-Single-Valued</span></span>       | <span data-ttu-id="218ee-162">對</span><span class="sxs-lookup"><span data-stu-id="218ee-162">True</span></span>         |
| <span data-ttu-id="218ee-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="218ee-163">Is Indexed</span></span>             | <span data-ttu-id="218ee-164">否</span><span class="sxs-lookup"><span data-stu-id="218ee-164">False</span></span>        |
| <span data-ttu-id="218ee-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="218ee-165">In Global Catalog</span></span>      | <span data-ttu-id="218ee-166">否</span><span class="sxs-lookup"><span data-stu-id="218ee-166">False</span></span>        |
| <span data-ttu-id="218ee-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="218ee-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="218ee-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="218ee-168">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="218ee-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="218ee-169">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="218ee-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="218ee-170">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="218ee-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-171">Search-Flags</span></span>           | <span data-ttu-id="218ee-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="218ee-172">0x00000000</span></span>   |
| <span data-ttu-id="218ee-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-173">System-Flags</span></span>           | <span data-ttu-id="218ee-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="218ee-174">0x08000014</span></span>   |
| <span data-ttu-id="218ee-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="218ee-175">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="218ee-176">亞當</span><span class="sxs-lookup"><span data-stu-id="218ee-176">ADAM</span></span>



| <span data-ttu-id="218ee-177">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-177">Entry</span></span> | <span data-ttu-id="218ee-178">值</span><span class="sxs-lookup"><span data-stu-id="218ee-178">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="218ee-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="218ee-179">Link-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="218ee-181">System-Only</span></span>            | <span data-ttu-id="218ee-182">否</span><span class="sxs-lookup"><span data-stu-id="218ee-182">False</span></span>        |
| <span data-ttu-id="218ee-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="218ee-183">Is-Single-Valued</span></span>       | <span data-ttu-id="218ee-184">對</span><span class="sxs-lookup"><span data-stu-id="218ee-184">True</span></span>         |
| <span data-ttu-id="218ee-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="218ee-185">Is Indexed</span></span>             | <span data-ttu-id="218ee-186">否</span><span class="sxs-lookup"><span data-stu-id="218ee-186">False</span></span>        |
| <span data-ttu-id="218ee-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="218ee-187">In Global Catalog</span></span>      | <span data-ttu-id="218ee-188">否</span><span class="sxs-lookup"><span data-stu-id="218ee-188">False</span></span>        |
| <span data-ttu-id="218ee-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="218ee-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="218ee-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="218ee-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="218ee-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="218ee-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="218ee-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="218ee-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="218ee-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-193">Search-Flags</span></span>           | <span data-ttu-id="218ee-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="218ee-194">0x00000000</span></span>   |
| <span data-ttu-id="218ee-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-195">System-Flags</span></span>           | <span data-ttu-id="218ee-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="218ee-196">0x08000014</span></span>   |
| <span data-ttu-id="218ee-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="218ee-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="218ee-198">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="218ee-198">Windows Server 2003 R2</span></span>



| <span data-ttu-id="218ee-199">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-199">Entry</span></span> | <span data-ttu-id="218ee-200">值</span><span class="sxs-lookup"><span data-stu-id="218ee-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="218ee-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="218ee-201">Link-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-202">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="218ee-203">System-Only</span></span>            | <span data-ttu-id="218ee-204">否</span><span class="sxs-lookup"><span data-stu-id="218ee-204">False</span></span>        |
| <span data-ttu-id="218ee-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="218ee-205">Is-Single-Valued</span></span>       | <span data-ttu-id="218ee-206">對</span><span class="sxs-lookup"><span data-stu-id="218ee-206">True</span></span>         |
| <span data-ttu-id="218ee-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="218ee-207">Is Indexed</span></span>             | <span data-ttu-id="218ee-208">否</span><span class="sxs-lookup"><span data-stu-id="218ee-208">False</span></span>        |
| <span data-ttu-id="218ee-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="218ee-209">In Global Catalog</span></span>      | <span data-ttu-id="218ee-210">否</span><span class="sxs-lookup"><span data-stu-id="218ee-210">False</span></span>        |
| <span data-ttu-id="218ee-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="218ee-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="218ee-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="218ee-212">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="218ee-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="218ee-213">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="218ee-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="218ee-214">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="218ee-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-215">Search-Flags</span></span>           | <span data-ttu-id="218ee-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="218ee-216">0x00000000</span></span>   |
| <span data-ttu-id="218ee-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-217">System-Flags</span></span>           | <span data-ttu-id="218ee-218">0x08000014</span><span class="sxs-lookup"><span data-stu-id="218ee-218">0x08000014</span></span>   |
| <span data-ttu-id="218ee-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="218ee-219">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="218ee-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="218ee-220">Windows Server 2008</span></span>



| <span data-ttu-id="218ee-221">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-221">Entry</span></span> | <span data-ttu-id="218ee-222">值</span><span class="sxs-lookup"><span data-stu-id="218ee-222">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="218ee-223">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="218ee-223">Link-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-224">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="218ee-225">System-Only</span></span>            | <span data-ttu-id="218ee-226">否</span><span class="sxs-lookup"><span data-stu-id="218ee-226">False</span></span>        |
| <span data-ttu-id="218ee-227">是-單一值</span><span class="sxs-lookup"><span data-stu-id="218ee-227">Is-Single-Valued</span></span>       | <span data-ttu-id="218ee-228">對</span><span class="sxs-lookup"><span data-stu-id="218ee-228">True</span></span>         |
| <span data-ttu-id="218ee-229">已編制索引</span><span class="sxs-lookup"><span data-stu-id="218ee-229">Is Indexed</span></span>             | <span data-ttu-id="218ee-230">否</span><span class="sxs-lookup"><span data-stu-id="218ee-230">False</span></span>        |
| <span data-ttu-id="218ee-231">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="218ee-231">In Global Catalog</span></span>      | <span data-ttu-id="218ee-232">否</span><span class="sxs-lookup"><span data-stu-id="218ee-232">False</span></span>        |
| <span data-ttu-id="218ee-233">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="218ee-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="218ee-234">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="218ee-234">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="218ee-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="218ee-235">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="218ee-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="218ee-236">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="218ee-237">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-237">Search-Flags</span></span>           | <span data-ttu-id="218ee-238">0x00000000</span><span class="sxs-lookup"><span data-stu-id="218ee-238">0x00000000</span></span>   |
| <span data-ttu-id="218ee-239">System-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-239">System-Flags</span></span>           | <span data-ttu-id="218ee-240">0x08000014</span><span class="sxs-lookup"><span data-stu-id="218ee-240">0x08000014</span></span>   |
| <span data-ttu-id="218ee-241">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="218ee-241">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="218ee-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="218ee-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="218ee-243">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-243">Entry</span></span> | <span data-ttu-id="218ee-244">值</span><span class="sxs-lookup"><span data-stu-id="218ee-244">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="218ee-245">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="218ee-245">Link-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-246">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="218ee-247">System-Only</span></span>            | <span data-ttu-id="218ee-248">否</span><span class="sxs-lookup"><span data-stu-id="218ee-248">False</span></span>        |
| <span data-ttu-id="218ee-249">是-單一值</span><span class="sxs-lookup"><span data-stu-id="218ee-249">Is-Single-Valued</span></span>       | <span data-ttu-id="218ee-250">對</span><span class="sxs-lookup"><span data-stu-id="218ee-250">True</span></span>         |
| <span data-ttu-id="218ee-251">已編制索引</span><span class="sxs-lookup"><span data-stu-id="218ee-251">Is Indexed</span></span>             | <span data-ttu-id="218ee-252">否</span><span class="sxs-lookup"><span data-stu-id="218ee-252">False</span></span>        |
| <span data-ttu-id="218ee-253">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="218ee-253">In Global Catalog</span></span>      | <span data-ttu-id="218ee-254">否</span><span class="sxs-lookup"><span data-stu-id="218ee-254">False</span></span>        |
| <span data-ttu-id="218ee-255">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="218ee-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="218ee-256">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="218ee-256">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="218ee-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="218ee-257">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="218ee-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="218ee-258">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="218ee-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-259">Search-Flags</span></span>           | <span data-ttu-id="218ee-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="218ee-260">0x00000000</span></span>   |
| <span data-ttu-id="218ee-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-261">System-Flags</span></span>           | <span data-ttu-id="218ee-262">0x08000014</span><span class="sxs-lookup"><span data-stu-id="218ee-262">0x08000014</span></span>   |
| <span data-ttu-id="218ee-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="218ee-263">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="218ee-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="218ee-264">Windows Server 2012</span></span>



| <span data-ttu-id="218ee-265">進入</span><span class="sxs-lookup"><span data-stu-id="218ee-265">Entry</span></span> | <span data-ttu-id="218ee-266">值</span><span class="sxs-lookup"><span data-stu-id="218ee-266">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="218ee-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="218ee-267">Link-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="218ee-268">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="218ee-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="218ee-269">System-Only</span></span>            | <span data-ttu-id="218ee-270">否</span><span class="sxs-lookup"><span data-stu-id="218ee-270">False</span></span>        |
| <span data-ttu-id="218ee-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="218ee-271">Is-Single-Valued</span></span>       | <span data-ttu-id="218ee-272">對</span><span class="sxs-lookup"><span data-stu-id="218ee-272">True</span></span>         |
| <span data-ttu-id="218ee-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="218ee-273">Is Indexed</span></span>             | <span data-ttu-id="218ee-274">否</span><span class="sxs-lookup"><span data-stu-id="218ee-274">False</span></span>        |
| <span data-ttu-id="218ee-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="218ee-275">In Global Catalog</span></span>      | <span data-ttu-id="218ee-276">否</span><span class="sxs-lookup"><span data-stu-id="218ee-276">False</span></span>        |
| <span data-ttu-id="218ee-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="218ee-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="218ee-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="218ee-278">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="218ee-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="218ee-279">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="218ee-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="218ee-280">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="218ee-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-281">Search-Flags</span></span>           | <span data-ttu-id="218ee-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="218ee-282">0x00000000</span></span>   |
| <span data-ttu-id="218ee-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="218ee-283">System-Flags</span></span>           | <span data-ttu-id="218ee-284">0x08000014</span><span class="sxs-lookup"><span data-stu-id="218ee-284">0x08000014</span></span>   |
| <span data-ttu-id="218ee-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="218ee-285">Classes used in</span></span>        | \-           |



 

 




