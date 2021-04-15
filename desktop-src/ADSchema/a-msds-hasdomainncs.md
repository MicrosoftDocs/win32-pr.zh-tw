---
title: Nc 屬性（ms DS）
description: 詳細說明特定伺服器上存在之網域命名內容的目錄服務複寫資訊。
ms.assetid: e5a7c371-5a37-466e-b56f-ee261b48e3b2
ms.tgt_platform: multiple
keywords:
- ms-chap-Nc 屬性 AD 架構
- HasDomainNCs 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Has-Domain-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b946286974cc6ba4e6d30484e7768a1daeccb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467285"
---
# <a name="ms-ds-has-domain-ncs-attribute"></a><span data-ttu-id="0b8fe-105">Nc 屬性（ms DS）</span><span class="sxs-lookup"><span data-stu-id="0b8fe-105">ms-DS-Has-Domain-NCs attribute</span></span>

<span data-ttu-id="0b8fe-106">詳細說明特定伺服器上存在之網域命名內容的目錄服務複寫資訊。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-106">Directory service replication information that details the domain naming contexts present on a particular server.</span></span>



| <span data-ttu-id="0b8fe-107">進入</span><span class="sxs-lookup"><span data-stu-id="0b8fe-107">Entry</span></span> | <span data-ttu-id="0b8fe-108">值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="0b8fe-109">CN</span><span class="sxs-lookup"><span data-stu-id="0b8fe-109">CN</span></span>                | <span data-ttu-id="0b8fe-110">ms-DS-Nc</span><span class="sxs-lookup"><span data-stu-id="0b8fe-110">ms-DS-Has-Domain-NCs</span></span>                                |
| <span data-ttu-id="0b8fe-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0b8fe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0b8fe-112">HasDomainNCs</span><span class="sxs-lookup"><span data-stu-id="0b8fe-112">msDS-HasDomainNCs</span></span>                                   |
| <span data-ttu-id="0b8fe-113">大小</span><span class="sxs-lookup"><span data-stu-id="0b8fe-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="0b8fe-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0b8fe-114">Update Privilege</span></span>  | <span data-ttu-id="0b8fe-115">此值是由系統所設定</span><span class="sxs-lookup"><span data-stu-id="0b8fe-115">This value is set by the system</span></span>                     |
| <span data-ttu-id="0b8fe-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0b8fe-116">Update Frequency</span></span>  | <span data-ttu-id="0b8fe-117">它是由 DCPromo 設定，之後也未曾修改過。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-117">It is set by DCPromo and never modified thereafter.</span></span> |
| <span data-ttu-id="0b8fe-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b8fe-118">Attribute-Id</span></span>      | <span data-ttu-id="0b8fe-119">1.2.840.113556.1.4.1820</span><span class="sxs-lookup"><span data-stu-id="0b8fe-119">1.2.840.113556.1.4.1820</span></span>                             |
| <span data-ttu-id="0b8fe-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0b8fe-120">System-Id-Guid</span></span>    | <span data-ttu-id="0b8fe-121">6f17e347-a842-4498-b8b3-15e007da4fed</span><span class="sxs-lookup"><span data-stu-id="0b8fe-121">6f17e347-a842-4498-b8b3-15e007da4fed</span></span>                |
| <span data-ttu-id="0b8fe-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b8fe-122">Syntax</span></span>            | [<span data-ttu-id="0b8fe-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)             |



## <a name="implementations"></a><span data-ttu-id="0b8fe-124">實作</span><span class="sxs-lookup"><span data-stu-id="0b8fe-124">Implementations</span></span>

-   [<span data-ttu-id="0b8fe-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b8fe-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0b8fe-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b8fe-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b8fe-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b8fe-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0b8fe-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b8fe-131">Windows Server 2003</span></span>



| <span data-ttu-id="0b8fe-132">進入</span><span class="sxs-lookup"><span data-stu-id="0b8fe-132">Entry</span></span> | <span data-ttu-id="0b8fe-133">值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0b8fe-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b8fe-134">Link-Id</span></span>                | <span data-ttu-id="0b8fe-135">2026</span><span class="sxs-lookup"><span data-stu-id="0b8fe-135">2026</span></span>                                     |
| <span data-ttu-id="0b8fe-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b8fe-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0b8fe-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b8fe-137">System-Only</span></span>            | <span data-ttu-id="0b8fe-138">對</span><span class="sxs-lookup"><span data-stu-id="0b8fe-138">True</span></span>                                     |
| <span data-ttu-id="0b8fe-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0b8fe-140">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-140">False</span></span>                                    |
| <span data-ttu-id="0b8fe-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b8fe-141">Is Indexed</span></span>             | <span data-ttu-id="0b8fe-142">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-142">False</span></span>                                    |
| <span data-ttu-id="0b8fe-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b8fe-143">In Global Catalog</span></span>      | <span data-ttu-id="0b8fe-144">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-144">False</span></span>                                    |
| <span data-ttu-id="0b8fe-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b8fe-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b8fe-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b8fe-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0b8fe-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b8fe-147">Range-Lower</span></span>            | <span data-ttu-id="0b8fe-148">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-148">4</span></span>                                        |
| <span data-ttu-id="0b8fe-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b8fe-149">Range-Upper</span></span>            | <span data-ttu-id="0b8fe-150">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-150">4</span></span>                                        |
| <span data-ttu-id="0b8fe-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-151">Search-Flags</span></span>           | <span data-ttu-id="0b8fe-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b8fe-152">0x00000000</span></span>                               |
| <span data-ttu-id="0b8fe-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-153">System-Flags</span></span>           | <span data-ttu-id="0b8fe-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b8fe-154">0x00000010</span></span>                               |
| <span data-ttu-id="0b8fe-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b8fe-155">Classes used in</span></span>        | [<span data-ttu-id="0b8fe-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0b8fe-157">亞當</span><span class="sxs-lookup"><span data-stu-id="0b8fe-157">ADAM</span></span>



| <span data-ttu-id="0b8fe-158">進入</span><span class="sxs-lookup"><span data-stu-id="0b8fe-158">Entry</span></span> | <span data-ttu-id="0b8fe-159">值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0b8fe-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b8fe-160">Link-Id</span></span>                | <span data-ttu-id="0b8fe-161">2026</span><span class="sxs-lookup"><span data-stu-id="0b8fe-161">2026</span></span>                                     |
| <span data-ttu-id="0b8fe-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b8fe-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0b8fe-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b8fe-163">System-Only</span></span>            | <span data-ttu-id="0b8fe-164">對</span><span class="sxs-lookup"><span data-stu-id="0b8fe-164">True</span></span>                                     |
| <span data-ttu-id="0b8fe-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-165">Is-Single-Valued</span></span>       | <span data-ttu-id="0b8fe-166">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-166">False</span></span>                                    |
| <span data-ttu-id="0b8fe-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b8fe-167">Is Indexed</span></span>             | <span data-ttu-id="0b8fe-168">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-168">False</span></span>                                    |
| <span data-ttu-id="0b8fe-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b8fe-169">In Global Catalog</span></span>      | <span data-ttu-id="0b8fe-170">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-170">False</span></span>                                    |
| <span data-ttu-id="0b8fe-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b8fe-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b8fe-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b8fe-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0b8fe-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b8fe-173">Range-Lower</span></span>            | <span data-ttu-id="0b8fe-174">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-174">4</span></span>                                        |
| <span data-ttu-id="0b8fe-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b8fe-175">Range-Upper</span></span>            | <span data-ttu-id="0b8fe-176">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-176">4</span></span>                                        |
| <span data-ttu-id="0b8fe-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-177">Search-Flags</span></span>           | <span data-ttu-id="0b8fe-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b8fe-178">0x00000000</span></span>                               |
| <span data-ttu-id="0b8fe-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-179">System-Flags</span></span>           | <span data-ttu-id="0b8fe-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b8fe-180">0x00000010</span></span>                               |
| <span data-ttu-id="0b8fe-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b8fe-181">Classes used in</span></span>        | [<span data-ttu-id="0b8fe-182">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-182">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b8fe-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b8fe-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b8fe-184">進入</span><span class="sxs-lookup"><span data-stu-id="0b8fe-184">Entry</span></span> | <span data-ttu-id="0b8fe-185">值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-185">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0b8fe-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b8fe-186">Link-Id</span></span>                | <span data-ttu-id="0b8fe-187">2026</span><span class="sxs-lookup"><span data-stu-id="0b8fe-187">2026</span></span>                                     |
| <span data-ttu-id="0b8fe-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b8fe-188">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0b8fe-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b8fe-189">System-Only</span></span>            | <span data-ttu-id="0b8fe-190">對</span><span class="sxs-lookup"><span data-stu-id="0b8fe-190">True</span></span>                                     |
| <span data-ttu-id="0b8fe-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-191">Is-Single-Valued</span></span>       | <span data-ttu-id="0b8fe-192">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-192">False</span></span>                                    |
| <span data-ttu-id="0b8fe-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b8fe-193">Is Indexed</span></span>             | <span data-ttu-id="0b8fe-194">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-194">False</span></span>                                    |
| <span data-ttu-id="0b8fe-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b8fe-195">In Global Catalog</span></span>      | <span data-ttu-id="0b8fe-196">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-196">False</span></span>                                    |
| <span data-ttu-id="0b8fe-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b8fe-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b8fe-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b8fe-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0b8fe-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b8fe-199">Range-Lower</span></span>            | <span data-ttu-id="0b8fe-200">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-200">4</span></span>                                        |
| <span data-ttu-id="0b8fe-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b8fe-201">Range-Upper</span></span>            | <span data-ttu-id="0b8fe-202">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-202">4</span></span>                                        |
| <span data-ttu-id="0b8fe-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-203">Search-Flags</span></span>           | <span data-ttu-id="0b8fe-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b8fe-204">0x00000000</span></span>                               |
| <span data-ttu-id="0b8fe-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-205">System-Flags</span></span>           | <span data-ttu-id="0b8fe-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b8fe-206">0x00000010</span></span>                               |
| <span data-ttu-id="0b8fe-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b8fe-207">Classes used in</span></span>        | [<span data-ttu-id="0b8fe-208">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-208">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b8fe-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b8fe-209">Windows Server 2008</span></span>



| <span data-ttu-id="0b8fe-210">進入</span><span class="sxs-lookup"><span data-stu-id="0b8fe-210">Entry</span></span> | <span data-ttu-id="0b8fe-211">值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-211">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0b8fe-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b8fe-212">Link-Id</span></span>                | <span data-ttu-id="0b8fe-213">2026</span><span class="sxs-lookup"><span data-stu-id="0b8fe-213">2026</span></span>                                     |
| <span data-ttu-id="0b8fe-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b8fe-214">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0b8fe-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b8fe-215">System-Only</span></span>            | <span data-ttu-id="0b8fe-216">對</span><span class="sxs-lookup"><span data-stu-id="0b8fe-216">True</span></span>                                     |
| <span data-ttu-id="0b8fe-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-217">Is-Single-Valued</span></span>       | <span data-ttu-id="0b8fe-218">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-218">False</span></span>                                    |
| <span data-ttu-id="0b8fe-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b8fe-219">Is Indexed</span></span>             | <span data-ttu-id="0b8fe-220">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-220">False</span></span>                                    |
| <span data-ttu-id="0b8fe-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b8fe-221">In Global Catalog</span></span>      | <span data-ttu-id="0b8fe-222">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-222">False</span></span>                                    |
| <span data-ttu-id="0b8fe-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b8fe-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b8fe-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b8fe-224">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0b8fe-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b8fe-225">Range-Lower</span></span>            | <span data-ttu-id="0b8fe-226">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-226">4</span></span>                                        |
| <span data-ttu-id="0b8fe-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b8fe-227">Range-Upper</span></span>            | <span data-ttu-id="0b8fe-228">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-228">4</span></span>                                        |
| <span data-ttu-id="0b8fe-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-229">Search-Flags</span></span>           | <span data-ttu-id="0b8fe-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b8fe-230">0x00000000</span></span>                               |
| <span data-ttu-id="0b8fe-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-231">System-Flags</span></span>           | <span data-ttu-id="0b8fe-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b8fe-232">0x00000010</span></span>                               |
| <span data-ttu-id="0b8fe-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b8fe-233">Classes used in</span></span>        | [<span data-ttu-id="0b8fe-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b8fe-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b8fe-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b8fe-236">進入</span><span class="sxs-lookup"><span data-stu-id="0b8fe-236">Entry</span></span> | <span data-ttu-id="0b8fe-237">值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-237">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0b8fe-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b8fe-238">Link-Id</span></span>                | <span data-ttu-id="0b8fe-239">2026</span><span class="sxs-lookup"><span data-stu-id="0b8fe-239">2026</span></span>                                     |
| <span data-ttu-id="0b8fe-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b8fe-240">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0b8fe-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b8fe-241">System-Only</span></span>            | <span data-ttu-id="0b8fe-242">對</span><span class="sxs-lookup"><span data-stu-id="0b8fe-242">True</span></span>                                     |
| <span data-ttu-id="0b8fe-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-243">Is-Single-Valued</span></span>       | <span data-ttu-id="0b8fe-244">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-244">False</span></span>                                    |
| <span data-ttu-id="0b8fe-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b8fe-245">Is Indexed</span></span>             | <span data-ttu-id="0b8fe-246">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-246">False</span></span>                                    |
| <span data-ttu-id="0b8fe-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b8fe-247">In Global Catalog</span></span>      | <span data-ttu-id="0b8fe-248">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-248">False</span></span>                                    |
| <span data-ttu-id="0b8fe-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b8fe-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b8fe-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b8fe-250">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0b8fe-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b8fe-251">Range-Lower</span></span>            | <span data-ttu-id="0b8fe-252">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-252">4</span></span>                                        |
| <span data-ttu-id="0b8fe-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b8fe-253">Range-Upper</span></span>            | <span data-ttu-id="0b8fe-254">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-254">4</span></span>                                        |
| <span data-ttu-id="0b8fe-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-255">Search-Flags</span></span>           | <span data-ttu-id="0b8fe-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b8fe-256">0x00000000</span></span>                               |
| <span data-ttu-id="0b8fe-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-257">System-Flags</span></span>           | <span data-ttu-id="0b8fe-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b8fe-258">0x00000010</span></span>                               |
| <span data-ttu-id="0b8fe-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b8fe-259">Classes used in</span></span>        | [<span data-ttu-id="0b8fe-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b8fe-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b8fe-261">Windows Server 2012</span></span>



| <span data-ttu-id="0b8fe-262">進入</span><span class="sxs-lookup"><span data-stu-id="0b8fe-262">Entry</span></span> | <span data-ttu-id="0b8fe-263">值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-263">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="0b8fe-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b8fe-264">Link-Id</span></span>                | <span data-ttu-id="0b8fe-265">2026</span><span class="sxs-lookup"><span data-stu-id="0b8fe-265">2026</span></span>                                     |
| <span data-ttu-id="0b8fe-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b8fe-266">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="0b8fe-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b8fe-267">System-Only</span></span>            | <span data-ttu-id="0b8fe-268">對</span><span class="sxs-lookup"><span data-stu-id="0b8fe-268">True</span></span>                                     |
| <span data-ttu-id="0b8fe-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b8fe-269">Is-Single-Valued</span></span>       | <span data-ttu-id="0b8fe-270">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-270">False</span></span>                                    |
| <span data-ttu-id="0b8fe-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b8fe-271">Is Indexed</span></span>             | <span data-ttu-id="0b8fe-272">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-272">False</span></span>                                    |
| <span data-ttu-id="0b8fe-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b8fe-273">In Global Catalog</span></span>      | <span data-ttu-id="0b8fe-274">否</span><span class="sxs-lookup"><span data-stu-id="0b8fe-274">False</span></span>                                    |
| <span data-ttu-id="0b8fe-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b8fe-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b8fe-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b8fe-276">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="0b8fe-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b8fe-277">Range-Lower</span></span>            | <span data-ttu-id="0b8fe-278">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-278">4</span></span>                                        |
| <span data-ttu-id="0b8fe-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b8fe-279">Range-Upper</span></span>            | <span data-ttu-id="0b8fe-280">4</span><span class="sxs-lookup"><span data-stu-id="0b8fe-280">4</span></span>                                        |
| <span data-ttu-id="0b8fe-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-281">Search-Flags</span></span>           | <span data-ttu-id="0b8fe-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b8fe-282">0x00000000</span></span>                               |
| <span data-ttu-id="0b8fe-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8fe-283">System-Flags</span></span>           | <span data-ttu-id="0b8fe-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b8fe-284">0x00000010</span></span>                               |
| <span data-ttu-id="0b8fe-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b8fe-285">Classes used in</span></span>        | [<span data-ttu-id="0b8fe-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="0b8fe-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





