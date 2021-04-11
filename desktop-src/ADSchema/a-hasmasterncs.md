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
# <a name="has-master-ncs-attribute"></a><span data-ttu-id="b4730-106">Nc 屬性</span><span class="sxs-lookup"><span data-stu-id="b4730-106">Has-Master-NCs attribute</span></span>

<span data-ttu-id="b4730-107">DC 命名內容的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="b4730-107">The distinguished name for the naming contexts for the DC.</span></span> <span data-ttu-id="b4730-108">Mastered-By 屬性的轉寄連結。</span><span class="sxs-lookup"><span data-stu-id="b4730-108">Forward link for the Mastered-By attribute.</span></span>



| <span data-ttu-id="b4730-109">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-109">Entry</span></span> | <span data-ttu-id="b4730-110">值</span><span class="sxs-lookup"><span data-stu-id="b4730-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b4730-111">CN</span><span class="sxs-lookup"><span data-stu-id="b4730-111">CN</span></span>                | <span data-ttu-id="b4730-112">具有-Master-Nc</span><span class="sxs-lookup"><span data-stu-id="b4730-112">Has-Master-NCs</span></span>                          |
| <span data-ttu-id="b4730-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b4730-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b4730-114">hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="b4730-114">hasMasterNCs</span></span>                            |
| <span data-ttu-id="b4730-115">大小</span><span class="sxs-lookup"><span data-stu-id="b4730-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="b4730-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b4730-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="b4730-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b4730-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="b4730-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-118">Attribute-Id</span></span>      | <span data-ttu-id="b4730-119">1.2.840.113556.1.2.14</span><span class="sxs-lookup"><span data-stu-id="b4730-119">1.2.840.113556.1.2.14</span></span>                   |
| <span data-ttu-id="b4730-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b4730-120">System-Id-Guid</span></span>    | <span data-ttu-id="b4730-121">bf967982-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b4730-121">bf967982-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="b4730-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4730-122">Syntax</span></span>            | [<span data-ttu-id="b4730-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b4730-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b4730-124">實作</span><span class="sxs-lookup"><span data-stu-id="b4730-124">Implementations</span></span>

-   [<span data-ttu-id="b4730-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4730-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4730-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4730-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4730-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b4730-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b4730-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4730-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4730-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4730-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4730-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4730-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4730-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4730-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4730-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4730-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b4730-133">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-133">Entry</span></span> | <span data-ttu-id="b4730-134">值</span><span class="sxs-lookup"><span data-stu-id="b4730-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b4730-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4730-135">Link-Id</span></span>                | <span data-ttu-id="b4730-136">76</span><span class="sxs-lookup"><span data-stu-id="b4730-136">76</span></span>                                       |
| <span data-ttu-id="b4730-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-137">MAPI-Id</span></span>                | <span data-ttu-id="b4730-138">0x80B6</span><span class="sxs-lookup"><span data-stu-id="b4730-138">0x80B6</span></span>                                   |
| <span data-ttu-id="b4730-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4730-139">System-Only</span></span>            | <span data-ttu-id="b4730-140">對</span><span class="sxs-lookup"><span data-stu-id="b4730-140">True</span></span>                                     |
| <span data-ttu-id="b4730-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4730-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b4730-142">否</span><span class="sxs-lookup"><span data-stu-id="b4730-142">False</span></span>                                    |
| <span data-ttu-id="b4730-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4730-143">Is Indexed</span></span>             | <span data-ttu-id="b4730-144">否</span><span class="sxs-lookup"><span data-stu-id="b4730-144">False</span></span>                                    |
| <span data-ttu-id="b4730-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4730-145">In Global Catalog</span></span>      | <span data-ttu-id="b4730-146">否</span><span class="sxs-lookup"><span data-stu-id="b4730-146">False</span></span>                                    |
| <span data-ttu-id="b4730-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4730-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4730-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4730-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b4730-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4730-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b4730-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4730-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b4730-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-151">Search-Flags</span></span>           | <span data-ttu-id="b4730-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4730-152">0x00000000</span></span>                               |
| <span data-ttu-id="b4730-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-153">System-Flags</span></span>           | <span data-ttu-id="b4730-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4730-154">0x00000010</span></span>                               |
| <span data-ttu-id="b4730-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4730-155">Classes used in</span></span>        | [<span data-ttu-id="b4730-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b4730-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4730-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4730-157">Windows Server 2003</span></span>



| <span data-ttu-id="b4730-158">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-158">Entry</span></span> | <span data-ttu-id="b4730-159">值</span><span class="sxs-lookup"><span data-stu-id="b4730-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b4730-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4730-160">Link-Id</span></span>                | <span data-ttu-id="b4730-161">76</span><span class="sxs-lookup"><span data-stu-id="b4730-161">76</span></span>                                       |
| <span data-ttu-id="b4730-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-162">MAPI-Id</span></span>                | <span data-ttu-id="b4730-163">0x80B6</span><span class="sxs-lookup"><span data-stu-id="b4730-163">0x80B6</span></span>                                   |
| <span data-ttu-id="b4730-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4730-164">System-Only</span></span>            | <span data-ttu-id="b4730-165">對</span><span class="sxs-lookup"><span data-stu-id="b4730-165">True</span></span>                                     |
| <span data-ttu-id="b4730-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4730-166">Is-Single-Valued</span></span>       | <span data-ttu-id="b4730-167">否</span><span class="sxs-lookup"><span data-stu-id="b4730-167">False</span></span>                                    |
| <span data-ttu-id="b4730-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4730-168">Is Indexed</span></span>             | <span data-ttu-id="b4730-169">否</span><span class="sxs-lookup"><span data-stu-id="b4730-169">False</span></span>                                    |
| <span data-ttu-id="b4730-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4730-170">In Global Catalog</span></span>      | <span data-ttu-id="b4730-171">否</span><span class="sxs-lookup"><span data-stu-id="b4730-171">False</span></span>                                    |
| <span data-ttu-id="b4730-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4730-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4730-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4730-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b4730-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4730-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b4730-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4730-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b4730-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-176">Search-Flags</span></span>           | <span data-ttu-id="b4730-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4730-177">0x00000000</span></span>                               |
| <span data-ttu-id="b4730-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-178">System-Flags</span></span>           | <span data-ttu-id="b4730-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4730-179">0x00000010</span></span>                               |
| <span data-ttu-id="b4730-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4730-180">Classes used in</span></span>        | [<span data-ttu-id="b4730-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b4730-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b4730-182">亞當</span><span class="sxs-lookup"><span data-stu-id="b4730-182">ADAM</span></span>



| <span data-ttu-id="b4730-183">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-183">Entry</span></span> | <span data-ttu-id="b4730-184">值</span><span class="sxs-lookup"><span data-stu-id="b4730-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b4730-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4730-185">Link-Id</span></span>                | <span data-ttu-id="b4730-186">76</span><span class="sxs-lookup"><span data-stu-id="b4730-186">76</span></span>                                       |
| <span data-ttu-id="b4730-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-187">MAPI-Id</span></span>                | <span data-ttu-id="b4730-188">0x80B6</span><span class="sxs-lookup"><span data-stu-id="b4730-188">0x80B6</span></span>                                   |
| <span data-ttu-id="b4730-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4730-189">System-Only</span></span>            | <span data-ttu-id="b4730-190">對</span><span class="sxs-lookup"><span data-stu-id="b4730-190">True</span></span>                                     |
| <span data-ttu-id="b4730-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4730-191">Is-Single-Valued</span></span>       | <span data-ttu-id="b4730-192">否</span><span class="sxs-lookup"><span data-stu-id="b4730-192">False</span></span>                                    |
| <span data-ttu-id="b4730-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4730-193">Is Indexed</span></span>             | <span data-ttu-id="b4730-194">否</span><span class="sxs-lookup"><span data-stu-id="b4730-194">False</span></span>                                    |
| <span data-ttu-id="b4730-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4730-195">In Global Catalog</span></span>      | <span data-ttu-id="b4730-196">否</span><span class="sxs-lookup"><span data-stu-id="b4730-196">False</span></span>                                    |
| <span data-ttu-id="b4730-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4730-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4730-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4730-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b4730-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4730-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b4730-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4730-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b4730-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-201">Search-Flags</span></span>           | <span data-ttu-id="b4730-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4730-202">0x00000000</span></span>                               |
| <span data-ttu-id="b4730-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-203">System-Flags</span></span>           | <span data-ttu-id="b4730-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4730-204">0x00000010</span></span>                               |
| <span data-ttu-id="b4730-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4730-205">Classes used in</span></span>        | [<span data-ttu-id="b4730-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b4730-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4730-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4730-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4730-208">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-208">Entry</span></span> | <span data-ttu-id="b4730-209">值</span><span class="sxs-lookup"><span data-stu-id="b4730-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b4730-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4730-210">Link-Id</span></span>                | <span data-ttu-id="b4730-211">76</span><span class="sxs-lookup"><span data-stu-id="b4730-211">76</span></span>                                       |
| <span data-ttu-id="b4730-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-212">MAPI-Id</span></span>                | <span data-ttu-id="b4730-213">0x80B6</span><span class="sxs-lookup"><span data-stu-id="b4730-213">0x80B6</span></span>                                   |
| <span data-ttu-id="b4730-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4730-214">System-Only</span></span>            | <span data-ttu-id="b4730-215">對</span><span class="sxs-lookup"><span data-stu-id="b4730-215">True</span></span>                                     |
| <span data-ttu-id="b4730-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4730-216">Is-Single-Valued</span></span>       | <span data-ttu-id="b4730-217">否</span><span class="sxs-lookup"><span data-stu-id="b4730-217">False</span></span>                                    |
| <span data-ttu-id="b4730-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4730-218">Is Indexed</span></span>             | <span data-ttu-id="b4730-219">否</span><span class="sxs-lookup"><span data-stu-id="b4730-219">False</span></span>                                    |
| <span data-ttu-id="b4730-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4730-220">In Global Catalog</span></span>      | <span data-ttu-id="b4730-221">否</span><span class="sxs-lookup"><span data-stu-id="b4730-221">False</span></span>                                    |
| <span data-ttu-id="b4730-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4730-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4730-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4730-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b4730-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4730-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b4730-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4730-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b4730-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-226">Search-Flags</span></span>           | <span data-ttu-id="b4730-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4730-227">0x00000000</span></span>                               |
| <span data-ttu-id="b4730-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-228">System-Flags</span></span>           | <span data-ttu-id="b4730-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4730-229">0x00000010</span></span>                               |
| <span data-ttu-id="b4730-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4730-230">Classes used in</span></span>        | [<span data-ttu-id="b4730-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b4730-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4730-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4730-232">Windows Server 2008</span></span>



| <span data-ttu-id="b4730-233">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-233">Entry</span></span> | <span data-ttu-id="b4730-234">值</span><span class="sxs-lookup"><span data-stu-id="b4730-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b4730-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4730-235">Link-Id</span></span>                | <span data-ttu-id="b4730-236">76</span><span class="sxs-lookup"><span data-stu-id="b4730-236">76</span></span>                                       |
| <span data-ttu-id="b4730-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-237">MAPI-Id</span></span>                | <span data-ttu-id="b4730-238">0x80B6</span><span class="sxs-lookup"><span data-stu-id="b4730-238">0x80B6</span></span>                                   |
| <span data-ttu-id="b4730-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4730-239">System-Only</span></span>            | <span data-ttu-id="b4730-240">對</span><span class="sxs-lookup"><span data-stu-id="b4730-240">True</span></span>                                     |
| <span data-ttu-id="b4730-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4730-241">Is-Single-Valued</span></span>       | <span data-ttu-id="b4730-242">否</span><span class="sxs-lookup"><span data-stu-id="b4730-242">False</span></span>                                    |
| <span data-ttu-id="b4730-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4730-243">Is Indexed</span></span>             | <span data-ttu-id="b4730-244">否</span><span class="sxs-lookup"><span data-stu-id="b4730-244">False</span></span>                                    |
| <span data-ttu-id="b4730-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4730-245">In Global Catalog</span></span>      | <span data-ttu-id="b4730-246">否</span><span class="sxs-lookup"><span data-stu-id="b4730-246">False</span></span>                                    |
| <span data-ttu-id="b4730-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4730-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4730-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4730-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b4730-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4730-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b4730-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4730-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b4730-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-251">Search-Flags</span></span>           | <span data-ttu-id="b4730-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4730-252">0x00000000</span></span>                               |
| <span data-ttu-id="b4730-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-253">System-Flags</span></span>           | <span data-ttu-id="b4730-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4730-254">0x00000010</span></span>                               |
| <span data-ttu-id="b4730-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4730-255">Classes used in</span></span>        | [<span data-ttu-id="b4730-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b4730-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4730-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4730-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4730-258">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-258">Entry</span></span> | <span data-ttu-id="b4730-259">值</span><span class="sxs-lookup"><span data-stu-id="b4730-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b4730-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4730-260">Link-Id</span></span>                | <span data-ttu-id="b4730-261">76</span><span class="sxs-lookup"><span data-stu-id="b4730-261">76</span></span>                                       |
| <span data-ttu-id="b4730-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-262">MAPI-Id</span></span>                | <span data-ttu-id="b4730-263">0x80B6</span><span class="sxs-lookup"><span data-stu-id="b4730-263">0x80B6</span></span>                                   |
| <span data-ttu-id="b4730-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4730-264">System-Only</span></span>            | <span data-ttu-id="b4730-265">對</span><span class="sxs-lookup"><span data-stu-id="b4730-265">True</span></span>                                     |
| <span data-ttu-id="b4730-266">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4730-266">Is-Single-Valued</span></span>       | <span data-ttu-id="b4730-267">否</span><span class="sxs-lookup"><span data-stu-id="b4730-267">False</span></span>                                    |
| <span data-ttu-id="b4730-268">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4730-268">Is Indexed</span></span>             | <span data-ttu-id="b4730-269">否</span><span class="sxs-lookup"><span data-stu-id="b4730-269">False</span></span>                                    |
| <span data-ttu-id="b4730-270">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4730-270">In Global Catalog</span></span>      | <span data-ttu-id="b4730-271">否</span><span class="sxs-lookup"><span data-stu-id="b4730-271">False</span></span>                                    |
| <span data-ttu-id="b4730-272">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4730-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4730-273">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4730-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b4730-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4730-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b4730-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4730-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b4730-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-276">Search-Flags</span></span>           | <span data-ttu-id="b4730-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4730-277">0x00000000</span></span>                               |
| <span data-ttu-id="b4730-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-278">System-Flags</span></span>           | <span data-ttu-id="b4730-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4730-279">0x00000010</span></span>                               |
| <span data-ttu-id="b4730-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4730-280">Classes used in</span></span>        | [<span data-ttu-id="b4730-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b4730-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4730-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4730-282">Windows Server 2012</span></span>



| <span data-ttu-id="b4730-283">進入</span><span class="sxs-lookup"><span data-stu-id="b4730-283">Entry</span></span> | <span data-ttu-id="b4730-284">值</span><span class="sxs-lookup"><span data-stu-id="b4730-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b4730-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4730-285">Link-Id</span></span>                | <span data-ttu-id="b4730-286">76</span><span class="sxs-lookup"><span data-stu-id="b4730-286">76</span></span>                                       |
| <span data-ttu-id="b4730-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4730-287">MAPI-Id</span></span>                | <span data-ttu-id="b4730-288">0x80B6</span><span class="sxs-lookup"><span data-stu-id="b4730-288">0x80B6</span></span>                                   |
| <span data-ttu-id="b4730-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4730-289">System-Only</span></span>            | <span data-ttu-id="b4730-290">對</span><span class="sxs-lookup"><span data-stu-id="b4730-290">True</span></span>                                     |
| <span data-ttu-id="b4730-291">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4730-291">Is-Single-Valued</span></span>       | <span data-ttu-id="b4730-292">否</span><span class="sxs-lookup"><span data-stu-id="b4730-292">False</span></span>                                    |
| <span data-ttu-id="b4730-293">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4730-293">Is Indexed</span></span>             | <span data-ttu-id="b4730-294">否</span><span class="sxs-lookup"><span data-stu-id="b4730-294">False</span></span>                                    |
| <span data-ttu-id="b4730-295">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4730-295">In Global Catalog</span></span>      | <span data-ttu-id="b4730-296">否</span><span class="sxs-lookup"><span data-stu-id="b4730-296">False</span></span>                                    |
| <span data-ttu-id="b4730-297">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4730-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4730-298">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4730-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b4730-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4730-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b4730-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4730-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b4730-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-301">Search-Flags</span></span>           | <span data-ttu-id="b4730-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4730-302">0x00000000</span></span>                               |
| <span data-ttu-id="b4730-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4730-303">System-Flags</span></span>           | <span data-ttu-id="b4730-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4730-304">0x00000010</span></span>                               |
| <span data-ttu-id="b4730-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4730-305">Classes used in</span></span>        | [<span data-ttu-id="b4730-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b4730-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





