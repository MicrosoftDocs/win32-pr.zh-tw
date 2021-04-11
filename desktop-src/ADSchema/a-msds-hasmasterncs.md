---
title: Nc 屬性（ms DS）
description: 包含網域控制站所持有的命名內容。 這個屬性淘汰具有-Nc。
ms.assetid: 5325db42-afd7-472c-8797-447e752a3907
ms.tgt_platform: multiple
keywords:
- Nc 屬性 AD 架構（ms DS）
- hasMasterNCs 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Has-Master-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24507460eaa7653cfc2c98d3772942de9936162c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845491"
---
# <a name="ms-ds-has-master-ncs-attribute"></a><span data-ttu-id="0e4db-106">Nc 屬性（ms DS）</span><span class="sxs-lookup"><span data-stu-id="0e4db-106">ms-DS-Has-Master-NCs attribute</span></span>

<span data-ttu-id="0e4db-107">包含網域控制站所持有的命名內容。</span><span class="sxs-lookup"><span data-stu-id="0e4db-107">Contains the naming contexts held by a domain controller.</span></span> <span data-ttu-id="0e4db-108">這個屬性淘汰具有-Nc。</span><span class="sxs-lookup"><span data-stu-id="0e4db-108">This attribute deprecates has-Master-NCs.</span></span>



| <span data-ttu-id="0e4db-109">進入</span><span class="sxs-lookup"><span data-stu-id="0e4db-109">Entry</span></span> | <span data-ttu-id="0e4db-110">值</span><span class="sxs-lookup"><span data-stu-id="0e4db-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0e4db-111">CN</span><span class="sxs-lookup"><span data-stu-id="0e4db-111">CN</span></span>                | <span data-ttu-id="0e4db-112">ms-DS-Nc</span><span class="sxs-lookup"><span data-stu-id="0e4db-112">ms-DS-Has-Master-NCs</span></span>                    |
| <span data-ttu-id="0e4db-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0e4db-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0e4db-114">hasMasterNCs</span><span class="sxs-lookup"><span data-stu-id="0e4db-114">msDS-hasMasterNCs</span></span>                       |
| <span data-ttu-id="0e4db-115">大小</span><span class="sxs-lookup"><span data-stu-id="0e4db-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="0e4db-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0e4db-116">Update Privilege</span></span>  | <span data-ttu-id="0e4db-117">此值是由系統所設定</span><span class="sxs-lookup"><span data-stu-id="0e4db-117">This value is set by the system</span></span>         |
| <span data-ttu-id="0e4db-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0e4db-118">Update Frequency</span></span>  | <span data-ttu-id="0e4db-119">每次建立新 NC 時。</span><span class="sxs-lookup"><span data-stu-id="0e4db-119">Each time a new NC is created.</span></span>          |
| <span data-ttu-id="0e4db-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0e4db-120">Attribute-Id</span></span>      | <span data-ttu-id="0e4db-121">1.2.840.113556.1.4.1836</span><span class="sxs-lookup"><span data-stu-id="0e4db-121">1.2.840.113556.1.4.1836</span></span>                 |
| <span data-ttu-id="0e4db-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0e4db-122">System-Id-Guid</span></span>    | <span data-ttu-id="0e4db-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span><span class="sxs-lookup"><span data-stu-id="0e4db-123">ae2de0e2-59d7-4d47-8d47-ed4dfe4357ad</span></span>    |
| <span data-ttu-id="0e4db-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e4db-124">Syntax</span></span>            | [<span data-ttu-id="0e4db-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0e4db-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="0e4db-126">實作</span><span class="sxs-lookup"><span data-stu-id="0e4db-126">Implementations</span></span>

-   [<span data-ttu-id="0e4db-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0e4db-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0e4db-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="0e4db-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0e4db-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0e4db-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0e4db-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0e4db-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0e4db-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0e4db-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0e4db-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0e4db-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0e4db-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e4db-133">Windows Server 2003</span></span>



| <span data-ttu-id="0e4db-134">進入</span><span class="sxs-lookup"><span data-stu-id="0e4db-134">Entry</span></span> | <span data-ttu-id="0e4db-135">值</span><span class="sxs-lookup"><span data-stu-id="0e4db-135">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e4db-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e4db-136">Link-Id</span></span>                | <span data-ttu-id="0e4db-137">2036</span><span class="sxs-lookup"><span data-stu-id="0e4db-137">2036</span></span>                                     |
| <span data-ttu-id="0e4db-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e4db-138">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e4db-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e4db-139">System-Only</span></span>            | <span data-ttu-id="0e4db-140">對</span><span class="sxs-lookup"><span data-stu-id="0e4db-140">True</span></span>                                     |
| <span data-ttu-id="0e4db-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e4db-141">Is-Single-Valued</span></span>       | <span data-ttu-id="0e4db-142">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-142">False</span></span>                                    |
| <span data-ttu-id="0e4db-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e4db-143">Is Indexed</span></span>             | <span data-ttu-id="0e4db-144">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-144">False</span></span>                                    |
| <span data-ttu-id="0e4db-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e4db-145">In Global Catalog</span></span>      | <span data-ttu-id="0e4db-146">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-146">False</span></span>                                    |
| <span data-ttu-id="0e4db-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e4db-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e4db-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e4db-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e4db-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e4db-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e4db-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-151">Search-Flags</span></span>           | <span data-ttu-id="0e4db-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e4db-152">0x00000000</span></span>                               |
| <span data-ttu-id="0e4db-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-153">System-Flags</span></span>           | <span data-ttu-id="0e4db-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e4db-154">0x00000010</span></span>                               |
| <span data-ttu-id="0e4db-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e4db-155">Classes used in</span></span>        | [<span data-ttu-id="0e4db-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0e4db-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0e4db-157">亞當</span><span class="sxs-lookup"><span data-stu-id="0e4db-157">ADAM</span></span>



| <span data-ttu-id="0e4db-158">進入</span><span class="sxs-lookup"><span data-stu-id="0e4db-158">Entry</span></span> | <span data-ttu-id="0e4db-159">值</span><span class="sxs-lookup"><span data-stu-id="0e4db-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e4db-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e4db-160">Link-Id</span></span>                | <span data-ttu-id="0e4db-161">2036</span><span class="sxs-lookup"><span data-stu-id="0e4db-161">2036</span></span>                                     |
| <span data-ttu-id="0e4db-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e4db-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e4db-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e4db-163">System-Only</span></span>            | <span data-ttu-id="0e4db-164">對</span><span class="sxs-lookup"><span data-stu-id="0e4db-164">True</span></span>                                     |
| <span data-ttu-id="0e4db-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e4db-165">Is-Single-Valued</span></span>       | <span data-ttu-id="0e4db-166">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-166">False</span></span>                                    |
| <span data-ttu-id="0e4db-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e4db-167">Is Indexed</span></span>             | <span data-ttu-id="0e4db-168">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-168">False</span></span>                                    |
| <span data-ttu-id="0e4db-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e4db-169">In Global Catalog</span></span>      | <span data-ttu-id="0e4db-170">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-170">False</span></span>                                    |
| <span data-ttu-id="0e4db-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e4db-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e4db-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e4db-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e4db-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e4db-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e4db-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-175">Search-Flags</span></span>           | <span data-ttu-id="0e4db-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e4db-176">0x00000000</span></span>                               |
| <span data-ttu-id="0e4db-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-177">System-Flags</span></span>           | <span data-ttu-id="0e4db-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e4db-178">0x00000010</span></span>                               |
| <span data-ttu-id="0e4db-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e4db-179">Classes used in</span></span>        | [<span data-ttu-id="0e4db-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0e4db-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0e4db-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0e4db-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0e4db-182">進入</span><span class="sxs-lookup"><span data-stu-id="0e4db-182">Entry</span></span> | <span data-ttu-id="0e4db-183">值</span><span class="sxs-lookup"><span data-stu-id="0e4db-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e4db-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e4db-184">Link-Id</span></span>                | <span data-ttu-id="0e4db-185">2036</span><span class="sxs-lookup"><span data-stu-id="0e4db-185">2036</span></span>                                     |
| <span data-ttu-id="0e4db-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e4db-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e4db-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e4db-187">System-Only</span></span>            | <span data-ttu-id="0e4db-188">對</span><span class="sxs-lookup"><span data-stu-id="0e4db-188">True</span></span>                                     |
| <span data-ttu-id="0e4db-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e4db-189">Is-Single-Valued</span></span>       | <span data-ttu-id="0e4db-190">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-190">False</span></span>                                    |
| <span data-ttu-id="0e4db-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e4db-191">Is Indexed</span></span>             | <span data-ttu-id="0e4db-192">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-192">False</span></span>                                    |
| <span data-ttu-id="0e4db-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e4db-193">In Global Catalog</span></span>      | <span data-ttu-id="0e4db-194">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-194">False</span></span>                                    |
| <span data-ttu-id="0e4db-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e4db-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e4db-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e4db-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e4db-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e4db-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e4db-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-199">Search-Flags</span></span>           | <span data-ttu-id="0e4db-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e4db-200">0x00000000</span></span>                               |
| <span data-ttu-id="0e4db-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-201">System-Flags</span></span>           | <span data-ttu-id="0e4db-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e4db-202">0x00000010</span></span>                               |
| <span data-ttu-id="0e4db-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e4db-203">Classes used in</span></span>        | [<span data-ttu-id="0e4db-204">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0e4db-204">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0e4db-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e4db-205">Windows Server 2008</span></span>



| <span data-ttu-id="0e4db-206">進入</span><span class="sxs-lookup"><span data-stu-id="0e4db-206">Entry</span></span> | <span data-ttu-id="0e4db-207">值</span><span class="sxs-lookup"><span data-stu-id="0e4db-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e4db-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e4db-208">Link-Id</span></span>                | <span data-ttu-id="0e4db-209">2036</span><span class="sxs-lookup"><span data-stu-id="0e4db-209">2036</span></span>                                     |
| <span data-ttu-id="0e4db-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e4db-210">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e4db-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e4db-211">System-Only</span></span>            | <span data-ttu-id="0e4db-212">對</span><span class="sxs-lookup"><span data-stu-id="0e4db-212">True</span></span>                                     |
| <span data-ttu-id="0e4db-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e4db-213">Is-Single-Valued</span></span>       | <span data-ttu-id="0e4db-214">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-214">False</span></span>                                    |
| <span data-ttu-id="0e4db-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e4db-215">Is Indexed</span></span>             | <span data-ttu-id="0e4db-216">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-216">False</span></span>                                    |
| <span data-ttu-id="0e4db-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e4db-217">In Global Catalog</span></span>      | <span data-ttu-id="0e4db-218">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-218">False</span></span>                                    |
| <span data-ttu-id="0e4db-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e4db-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e4db-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e4db-220">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e4db-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e4db-221">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e4db-222">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-223">Search-Flags</span></span>           | <span data-ttu-id="0e4db-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e4db-224">0x00000000</span></span>                               |
| <span data-ttu-id="0e4db-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-225">System-Flags</span></span>           | <span data-ttu-id="0e4db-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e4db-226">0x00000010</span></span>                               |
| <span data-ttu-id="0e4db-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e4db-227">Classes used in</span></span>        | [<span data-ttu-id="0e4db-228">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0e4db-228">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0e4db-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e4db-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0e4db-230">進入</span><span class="sxs-lookup"><span data-stu-id="0e4db-230">Entry</span></span> | <span data-ttu-id="0e4db-231">值</span><span class="sxs-lookup"><span data-stu-id="0e4db-231">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e4db-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e4db-232">Link-Id</span></span>                | <span data-ttu-id="0e4db-233">2036</span><span class="sxs-lookup"><span data-stu-id="0e4db-233">2036</span></span>                                     |
| <span data-ttu-id="0e4db-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e4db-234">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e4db-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e4db-235">System-Only</span></span>            | <span data-ttu-id="0e4db-236">對</span><span class="sxs-lookup"><span data-stu-id="0e4db-236">True</span></span>                                     |
| <span data-ttu-id="0e4db-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e4db-237">Is-Single-Valued</span></span>       | <span data-ttu-id="0e4db-238">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-238">False</span></span>                                    |
| <span data-ttu-id="0e4db-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e4db-239">Is Indexed</span></span>             | <span data-ttu-id="0e4db-240">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-240">False</span></span>                                    |
| <span data-ttu-id="0e4db-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e4db-241">In Global Catalog</span></span>      | <span data-ttu-id="0e4db-242">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-242">False</span></span>                                    |
| <span data-ttu-id="0e4db-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e4db-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e4db-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e4db-244">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e4db-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e4db-245">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e4db-246">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-247">Search-Flags</span></span>           | <span data-ttu-id="0e4db-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e4db-248">0x00000000</span></span>                               |
| <span data-ttu-id="0e4db-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-249">System-Flags</span></span>           | <span data-ttu-id="0e4db-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e4db-250">0x00000010</span></span>                               |
| <span data-ttu-id="0e4db-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e4db-251">Classes used in</span></span>        | [<span data-ttu-id="0e4db-252">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0e4db-252">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0e4db-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e4db-253">Windows Server 2012</span></span>



| <span data-ttu-id="0e4db-254">進入</span><span class="sxs-lookup"><span data-stu-id="0e4db-254">Entry</span></span> | <span data-ttu-id="0e4db-255">值</span><span class="sxs-lookup"><span data-stu-id="0e4db-255">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0e4db-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e4db-256">Link-Id</span></span>                | <span data-ttu-id="0e4db-257">2036</span><span class="sxs-lookup"><span data-stu-id="0e4db-257">2036</span></span>                                     |
| <span data-ttu-id="0e4db-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e4db-258">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0e4db-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e4db-259">System-Only</span></span>            | <span data-ttu-id="0e4db-260">對</span><span class="sxs-lookup"><span data-stu-id="0e4db-260">True</span></span>                                     |
| <span data-ttu-id="0e4db-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e4db-261">Is-Single-Valued</span></span>       | <span data-ttu-id="0e4db-262">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-262">False</span></span>                                    |
| <span data-ttu-id="0e4db-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e4db-263">Is Indexed</span></span>             | <span data-ttu-id="0e4db-264">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-264">False</span></span>                                    |
| <span data-ttu-id="0e4db-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e4db-265">In Global Catalog</span></span>      | <span data-ttu-id="0e4db-266">否</span><span class="sxs-lookup"><span data-stu-id="0e4db-266">False</span></span>                                    |
| <span data-ttu-id="0e4db-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e4db-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e4db-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e4db-268">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0e4db-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e4db-269">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e4db-270">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="0e4db-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-271">Search-Flags</span></span>           | <span data-ttu-id="0e4db-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e4db-272">0x00000000</span></span>                               |
| <span data-ttu-id="0e4db-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e4db-273">System-Flags</span></span>           | <span data-ttu-id="0e4db-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e4db-274">0x00000010</span></span>                               |
| <span data-ttu-id="0e4db-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e4db-275">Classes used in</span></span>        | [<span data-ttu-id="0e4db-276">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0e4db-276">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





