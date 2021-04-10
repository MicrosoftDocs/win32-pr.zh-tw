---
title: Nc 屬性
description: DC 命名內容的分辨名稱。 Mastered-By 屬性的轉寄連結。
ms.assetid: 77a7e693-513f-4f76-8c4f-d2ef3240323b
ms.tgt_platform: multiple
keywords:
- Nc 屬性 AD 架構
- hasMasterNCs 屬性 AD 架構
topic_type:
- apiref
api_name:
- Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34756c491c5228c58da1b95d4fd7b838c691f38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935458"
---
# <a name="has-master-ncs-attribute"></a><span data-ttu-id="fef84-106">Nc 屬性</span><span class="sxs-lookup"><span data-stu-id="fef84-106">Has-Master-NCs attribute</span></span>

<span data-ttu-id="fef84-107">DC 命名內容的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="fef84-107">The distinguished name for the naming contexts for the DC.</span></span> <span data-ttu-id="fef84-108">Mastered-By 屬性的轉寄連結。</span><span class="sxs-lookup"><span data-stu-id="fef84-108">Forward link for the Mastered-By attribute.</span></span>



| <span data-ttu-id="fef84-109">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-109">Entry</span></span> | <span data-ttu-id="fef84-110">值</span><span class="sxs-lookup"><span data-stu-id="fef84-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="fef84-111">CN</span><span class="sxs-lookup"><span data-stu-id="fef84-111">CN</span></span>                | <span data-ttu-id="fef84-112">具有-Master-Nc</span><span class="sxs-lookup"><span data-stu-id="fef84-112">Has-Master-NCs</span></span>                          |
| <span data-ttu-id="fef84-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fef84-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fef84-114">hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="fef84-114">hasMasterNCs</span></span>                            |
| <span data-ttu-id="fef84-115">大小</span><span class="sxs-lookup"><span data-stu-id="fef84-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="fef84-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fef84-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="fef84-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fef84-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="fef84-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-118">Attribute-Id</span></span>      | <span data-ttu-id="fef84-119">1.2.840.113556.1.2.14</span><span class="sxs-lookup"><span data-stu-id="fef84-119">1.2.840.113556.1.2.14</span></span>                   |
| <span data-ttu-id="fef84-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fef84-120">System-Id-Guid</span></span>    | <span data-ttu-id="fef84-121">bf967982-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="fef84-121">bf967982-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="fef84-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="fef84-122">Syntax</span></span>            | [<span data-ttu-id="fef84-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="fef84-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="fef84-124">實作</span><span class="sxs-lookup"><span data-stu-id="fef84-124">Implementations</span></span>

-   [<span data-ttu-id="fef84-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fef84-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fef84-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fef84-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fef84-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="fef84-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fef84-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fef84-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fef84-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fef84-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fef84-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fef84-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fef84-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fef84-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fef84-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fef84-132">Windows 2000 Server</span></span>



| <span data-ttu-id="fef84-133">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-133">Entry</span></span> | <span data-ttu-id="fef84-134">值</span><span class="sxs-lookup"><span data-stu-id="fef84-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="fef84-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fef84-135">Link-Id</span></span>                | <span data-ttu-id="fef84-136">76</span><span class="sxs-lookup"><span data-stu-id="fef84-136">76</span></span>                                       |
| <span data-ttu-id="fef84-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-137">MAPI-Id</span></span>                | <span data-ttu-id="fef84-138">0x80B6</span><span class="sxs-lookup"><span data-stu-id="fef84-138">0x80B6</span></span>                                   |
| <span data-ttu-id="fef84-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef84-139">System-Only</span></span>            | <span data-ttu-id="fef84-140">對</span><span class="sxs-lookup"><span data-stu-id="fef84-140">True</span></span>                                     |
| <span data-ttu-id="fef84-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fef84-141">Is-Single-Valued</span></span>       | <span data-ttu-id="fef84-142">否</span><span class="sxs-lookup"><span data-stu-id="fef84-142">False</span></span>                                    |
| <span data-ttu-id="fef84-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fef84-143">Is Indexed</span></span>             | <span data-ttu-id="fef84-144">否</span><span class="sxs-lookup"><span data-stu-id="fef84-144">False</span></span>                                    |
| <span data-ttu-id="fef84-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fef84-145">In Global Catalog</span></span>      | <span data-ttu-id="fef84-146">否</span><span class="sxs-lookup"><span data-stu-id="fef84-146">False</span></span>                                    |
| <span data-ttu-id="fef84-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fef84-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef84-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fef84-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="fef84-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef84-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="fef84-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef84-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="fef84-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-151">Search-Flags</span></span>           | <span data-ttu-id="fef84-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef84-152">0x00000000</span></span>                               |
| <span data-ttu-id="fef84-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-153">System-Flags</span></span>           | <span data-ttu-id="fef84-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef84-154">0x00000010</span></span>                               |
| <span data-ttu-id="fef84-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fef84-155">Classes used in</span></span>        | [<span data-ttu-id="fef84-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fef84-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fef84-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fef84-157">Windows Server 2003</span></span>



| <span data-ttu-id="fef84-158">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-158">Entry</span></span> | <span data-ttu-id="fef84-159">值</span><span class="sxs-lookup"><span data-stu-id="fef84-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="fef84-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fef84-160">Link-Id</span></span>                | <span data-ttu-id="fef84-161">76</span><span class="sxs-lookup"><span data-stu-id="fef84-161">76</span></span>                                       |
| <span data-ttu-id="fef84-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-162">MAPI-Id</span></span>                | <span data-ttu-id="fef84-163">0x80B6</span><span class="sxs-lookup"><span data-stu-id="fef84-163">0x80B6</span></span>                                   |
| <span data-ttu-id="fef84-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef84-164">System-Only</span></span>            | <span data-ttu-id="fef84-165">對</span><span class="sxs-lookup"><span data-stu-id="fef84-165">True</span></span>                                     |
| <span data-ttu-id="fef84-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fef84-166">Is-Single-Valued</span></span>       | <span data-ttu-id="fef84-167">否</span><span class="sxs-lookup"><span data-stu-id="fef84-167">False</span></span>                                    |
| <span data-ttu-id="fef84-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fef84-168">Is Indexed</span></span>             | <span data-ttu-id="fef84-169">否</span><span class="sxs-lookup"><span data-stu-id="fef84-169">False</span></span>                                    |
| <span data-ttu-id="fef84-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fef84-170">In Global Catalog</span></span>      | <span data-ttu-id="fef84-171">否</span><span class="sxs-lookup"><span data-stu-id="fef84-171">False</span></span>                                    |
| <span data-ttu-id="fef84-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fef84-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef84-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fef84-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="fef84-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef84-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="fef84-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef84-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="fef84-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-176">Search-Flags</span></span>           | <span data-ttu-id="fef84-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef84-177">0x00000000</span></span>                               |
| <span data-ttu-id="fef84-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-178">System-Flags</span></span>           | <span data-ttu-id="fef84-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef84-179">0x00000010</span></span>                               |
| <span data-ttu-id="fef84-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fef84-180">Classes used in</span></span>        | [<span data-ttu-id="fef84-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fef84-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fef84-182">亞當</span><span class="sxs-lookup"><span data-stu-id="fef84-182">ADAM</span></span>



| <span data-ttu-id="fef84-183">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-183">Entry</span></span> | <span data-ttu-id="fef84-184">值</span><span class="sxs-lookup"><span data-stu-id="fef84-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="fef84-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fef84-185">Link-Id</span></span>                | <span data-ttu-id="fef84-186">76</span><span class="sxs-lookup"><span data-stu-id="fef84-186">76</span></span>                                       |
| <span data-ttu-id="fef84-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-187">MAPI-Id</span></span>                | <span data-ttu-id="fef84-188">0x80B6</span><span class="sxs-lookup"><span data-stu-id="fef84-188">0x80B6</span></span>                                   |
| <span data-ttu-id="fef84-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef84-189">System-Only</span></span>            | <span data-ttu-id="fef84-190">對</span><span class="sxs-lookup"><span data-stu-id="fef84-190">True</span></span>                                     |
| <span data-ttu-id="fef84-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fef84-191">Is-Single-Valued</span></span>       | <span data-ttu-id="fef84-192">否</span><span class="sxs-lookup"><span data-stu-id="fef84-192">False</span></span>                                    |
| <span data-ttu-id="fef84-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fef84-193">Is Indexed</span></span>             | <span data-ttu-id="fef84-194">否</span><span class="sxs-lookup"><span data-stu-id="fef84-194">False</span></span>                                    |
| <span data-ttu-id="fef84-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fef84-195">In Global Catalog</span></span>      | <span data-ttu-id="fef84-196">否</span><span class="sxs-lookup"><span data-stu-id="fef84-196">False</span></span>                                    |
| <span data-ttu-id="fef84-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fef84-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef84-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fef84-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="fef84-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef84-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="fef84-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef84-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="fef84-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-201">Search-Flags</span></span>           | <span data-ttu-id="fef84-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef84-202">0x00000000</span></span>                               |
| <span data-ttu-id="fef84-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-203">System-Flags</span></span>           | <span data-ttu-id="fef84-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef84-204">0x00000010</span></span>                               |
| <span data-ttu-id="fef84-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fef84-205">Classes used in</span></span>        | [<span data-ttu-id="fef84-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fef84-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fef84-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fef84-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fef84-208">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-208">Entry</span></span> | <span data-ttu-id="fef84-209">值</span><span class="sxs-lookup"><span data-stu-id="fef84-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="fef84-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fef84-210">Link-Id</span></span>                | <span data-ttu-id="fef84-211">76</span><span class="sxs-lookup"><span data-stu-id="fef84-211">76</span></span>                                       |
| <span data-ttu-id="fef84-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-212">MAPI-Id</span></span>                | <span data-ttu-id="fef84-213">0x80B6</span><span class="sxs-lookup"><span data-stu-id="fef84-213">0x80B6</span></span>                                   |
| <span data-ttu-id="fef84-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef84-214">System-Only</span></span>            | <span data-ttu-id="fef84-215">對</span><span class="sxs-lookup"><span data-stu-id="fef84-215">True</span></span>                                     |
| <span data-ttu-id="fef84-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fef84-216">Is-Single-Valued</span></span>       | <span data-ttu-id="fef84-217">否</span><span class="sxs-lookup"><span data-stu-id="fef84-217">False</span></span>                                    |
| <span data-ttu-id="fef84-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fef84-218">Is Indexed</span></span>             | <span data-ttu-id="fef84-219">否</span><span class="sxs-lookup"><span data-stu-id="fef84-219">False</span></span>                                    |
| <span data-ttu-id="fef84-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fef84-220">In Global Catalog</span></span>      | <span data-ttu-id="fef84-221">否</span><span class="sxs-lookup"><span data-stu-id="fef84-221">False</span></span>                                    |
| <span data-ttu-id="fef84-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fef84-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef84-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fef84-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="fef84-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef84-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="fef84-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef84-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="fef84-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-226">Search-Flags</span></span>           | <span data-ttu-id="fef84-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef84-227">0x00000000</span></span>                               |
| <span data-ttu-id="fef84-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-228">System-Flags</span></span>           | <span data-ttu-id="fef84-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef84-229">0x00000010</span></span>                               |
| <span data-ttu-id="fef84-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fef84-230">Classes used in</span></span>        | [<span data-ttu-id="fef84-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fef84-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fef84-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fef84-232">Windows Server 2008</span></span>



| <span data-ttu-id="fef84-233">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-233">Entry</span></span> | <span data-ttu-id="fef84-234">值</span><span class="sxs-lookup"><span data-stu-id="fef84-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="fef84-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fef84-235">Link-Id</span></span>                | <span data-ttu-id="fef84-236">76</span><span class="sxs-lookup"><span data-stu-id="fef84-236">76</span></span>                                       |
| <span data-ttu-id="fef84-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-237">MAPI-Id</span></span>                | <span data-ttu-id="fef84-238">0x80B6</span><span class="sxs-lookup"><span data-stu-id="fef84-238">0x80B6</span></span>                                   |
| <span data-ttu-id="fef84-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef84-239">System-Only</span></span>            | <span data-ttu-id="fef84-240">對</span><span class="sxs-lookup"><span data-stu-id="fef84-240">True</span></span>                                     |
| <span data-ttu-id="fef84-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fef84-241">Is-Single-Valued</span></span>       | <span data-ttu-id="fef84-242">否</span><span class="sxs-lookup"><span data-stu-id="fef84-242">False</span></span>                                    |
| <span data-ttu-id="fef84-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fef84-243">Is Indexed</span></span>             | <span data-ttu-id="fef84-244">否</span><span class="sxs-lookup"><span data-stu-id="fef84-244">False</span></span>                                    |
| <span data-ttu-id="fef84-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fef84-245">In Global Catalog</span></span>      | <span data-ttu-id="fef84-246">否</span><span class="sxs-lookup"><span data-stu-id="fef84-246">False</span></span>                                    |
| <span data-ttu-id="fef84-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fef84-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef84-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fef84-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="fef84-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef84-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="fef84-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef84-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="fef84-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-251">Search-Flags</span></span>           | <span data-ttu-id="fef84-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef84-252">0x00000000</span></span>                               |
| <span data-ttu-id="fef84-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-253">System-Flags</span></span>           | <span data-ttu-id="fef84-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef84-254">0x00000010</span></span>                               |
| <span data-ttu-id="fef84-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fef84-255">Classes used in</span></span>        | [<span data-ttu-id="fef84-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fef84-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fef84-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fef84-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fef84-258">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-258">Entry</span></span> | <span data-ttu-id="fef84-259">值</span><span class="sxs-lookup"><span data-stu-id="fef84-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="fef84-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fef84-260">Link-Id</span></span>                | <span data-ttu-id="fef84-261">76</span><span class="sxs-lookup"><span data-stu-id="fef84-261">76</span></span>                                       |
| <span data-ttu-id="fef84-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-262">MAPI-Id</span></span>                | <span data-ttu-id="fef84-263">0x80B6</span><span class="sxs-lookup"><span data-stu-id="fef84-263">0x80B6</span></span>                                   |
| <span data-ttu-id="fef84-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef84-264">System-Only</span></span>            | <span data-ttu-id="fef84-265">對</span><span class="sxs-lookup"><span data-stu-id="fef84-265">True</span></span>                                     |
| <span data-ttu-id="fef84-266">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fef84-266">Is-Single-Valued</span></span>       | <span data-ttu-id="fef84-267">否</span><span class="sxs-lookup"><span data-stu-id="fef84-267">False</span></span>                                    |
| <span data-ttu-id="fef84-268">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fef84-268">Is Indexed</span></span>             | <span data-ttu-id="fef84-269">否</span><span class="sxs-lookup"><span data-stu-id="fef84-269">False</span></span>                                    |
| <span data-ttu-id="fef84-270">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fef84-270">In Global Catalog</span></span>      | <span data-ttu-id="fef84-271">否</span><span class="sxs-lookup"><span data-stu-id="fef84-271">False</span></span>                                    |
| <span data-ttu-id="fef84-272">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fef84-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef84-273">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fef84-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="fef84-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef84-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="fef84-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef84-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="fef84-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-276">Search-Flags</span></span>           | <span data-ttu-id="fef84-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef84-277">0x00000000</span></span>                               |
| <span data-ttu-id="fef84-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-278">System-Flags</span></span>           | <span data-ttu-id="fef84-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef84-279">0x00000010</span></span>                               |
| <span data-ttu-id="fef84-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fef84-280">Classes used in</span></span>        | [<span data-ttu-id="fef84-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fef84-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fef84-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fef84-282">Windows Server 2012</span></span>



| <span data-ttu-id="fef84-283">進入</span><span class="sxs-lookup"><span data-stu-id="fef84-283">Entry</span></span> | <span data-ttu-id="fef84-284">值</span><span class="sxs-lookup"><span data-stu-id="fef84-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="fef84-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fef84-285">Link-Id</span></span>                | <span data-ttu-id="fef84-286">76</span><span class="sxs-lookup"><span data-stu-id="fef84-286">76</span></span>                                       |
| <span data-ttu-id="fef84-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef84-287">MAPI-Id</span></span>                | <span data-ttu-id="fef84-288">0x80B6</span><span class="sxs-lookup"><span data-stu-id="fef84-288">0x80B6</span></span>                                   |
| <span data-ttu-id="fef84-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef84-289">System-Only</span></span>            | <span data-ttu-id="fef84-290">對</span><span class="sxs-lookup"><span data-stu-id="fef84-290">True</span></span>                                     |
| <span data-ttu-id="fef84-291">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fef84-291">Is-Single-Valued</span></span>       | <span data-ttu-id="fef84-292">否</span><span class="sxs-lookup"><span data-stu-id="fef84-292">False</span></span>                                    |
| <span data-ttu-id="fef84-293">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fef84-293">Is Indexed</span></span>             | <span data-ttu-id="fef84-294">否</span><span class="sxs-lookup"><span data-stu-id="fef84-294">False</span></span>                                    |
| <span data-ttu-id="fef84-295">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fef84-295">In Global Catalog</span></span>      | <span data-ttu-id="fef84-296">否</span><span class="sxs-lookup"><span data-stu-id="fef84-296">False</span></span>                                    |
| <span data-ttu-id="fef84-297">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fef84-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef84-298">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fef84-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="fef84-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef84-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="fef84-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef84-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="fef84-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-301">Search-Flags</span></span>           | <span data-ttu-id="fef84-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef84-302">0x00000000</span></span>                               |
| <span data-ttu-id="fef84-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef84-303">System-Flags</span></span>           | <span data-ttu-id="fef84-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef84-304">0x00000010</span></span>                               |
| <span data-ttu-id="fef84-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fef84-305">Classes used in</span></span>        | [<span data-ttu-id="fef84-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fef84-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





