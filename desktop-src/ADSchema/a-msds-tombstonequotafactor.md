---
title: ms DS-標記-配額因素屬性
description: 因配額帳戶處理的目的，應減少標記物件計數的百分比因數。
ms.assetid: 602c2fe0-d3b7-45e8-8ce8-35a7163f7b25
ms.tgt_platform: multiple
keywords:
- ms DS-標記-配額要素屬性 AD 架構
- TombstoneQuotaFactor 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Tombstone-Quota-Factor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a44dd7f648754c2ded7334c9b221022d936ebfb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509612"
---
# <a name="ms-ds-tombstone-quota-factor-attribute"></a><span data-ttu-id="9ac7f-105">ms DS-標記-配額因素屬性</span><span class="sxs-lookup"><span data-stu-id="9ac7f-105">ms-DS-Tombstone-Quota-Factor attribute</span></span>

<span data-ttu-id="9ac7f-106">因配額帳戶處理的目的，應減少標記物件計數的百分比因數。</span><span class="sxs-lookup"><span data-stu-id="9ac7f-106">The percentage factor by which the tombstone object count should be reduced for the purpose of quota accounting.</span></span>



| <span data-ttu-id="9ac7f-107">進入</span><span class="sxs-lookup"><span data-stu-id="9ac7f-107">Entry</span></span> | <span data-ttu-id="9ac7f-108">值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9ac7f-109">CN</span><span class="sxs-lookup"><span data-stu-id="9ac7f-109">CN</span></span>                | <span data-ttu-id="9ac7f-110">ms-DS-標記-配額因素</span><span class="sxs-lookup"><span data-stu-id="9ac7f-110">ms-DS-Tombstone-Quota-Factor</span></span>         |
| <span data-ttu-id="9ac7f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9ac7f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9ac7f-112">TombstoneQuotaFactor</span><span class="sxs-lookup"><span data-stu-id="9ac7f-112">msDS-TombstoneQuotaFactor</span></span>            |
| <span data-ttu-id="9ac7f-113">大小</span><span class="sxs-lookup"><span data-stu-id="9ac7f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9ac7f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9ac7f-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9ac7f-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9ac7f-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9ac7f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ac7f-116">Attribute-Id</span></span>      | <span data-ttu-id="9ac7f-117">1.2.840.113556.1.4.1847</span><span class="sxs-lookup"><span data-stu-id="9ac7f-117">1.2.840.113556.1.4.1847</span></span>              |
| <span data-ttu-id="9ac7f-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9ac7f-118">System-Id-Guid</span></span>    | <span data-ttu-id="9ac7f-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span><span class="sxs-lookup"><span data-stu-id="9ac7f-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span></span> |
| <span data-ttu-id="9ac7f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ac7f-120">Syntax</span></span>            | [<span data-ttu-id="9ac7f-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="9ac7f-122">實作</span><span class="sxs-lookup"><span data-stu-id="9ac7f-122">Implementations</span></span>

-   [<span data-ttu-id="9ac7f-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ac7f-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9ac7f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ac7f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ac7f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ac7f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9ac7f-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ac7f-129">Windows Server 2003</span></span>



| <span data-ttu-id="9ac7f-130">進入</span><span class="sxs-lookup"><span data-stu-id="9ac7f-130">Entry</span></span> | <span data-ttu-id="9ac7f-131">值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9ac7f-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ac7f-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ac7f-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ac7f-134">System-Only</span></span>            | <span data-ttu-id="9ac7f-135">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-135">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9ac7f-137">對</span><span class="sxs-lookup"><span data-stu-id="9ac7f-137">True</span></span>                                                              |
| <span data-ttu-id="9ac7f-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ac7f-138">Is Indexed</span></span>             | <span data-ttu-id="9ac7f-139">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-139">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ac7f-140">In Global Catalog</span></span>      | <span data-ttu-id="9ac7f-141">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-141">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ac7f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ac7f-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ac7f-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9ac7f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ac7f-144">Range-Lower</span></span>            | <span data-ttu-id="9ac7f-145">0</span><span class="sxs-lookup"><span data-stu-id="9ac7f-145">0</span></span>                                                                 |
| <span data-ttu-id="9ac7f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ac7f-146">Range-Upper</span></span>            | <span data-ttu-id="9ac7f-147">100</span><span class="sxs-lookup"><span data-stu-id="9ac7f-147">100</span></span>                                                               |
| <span data-ttu-id="9ac7f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-148">Search-Flags</span></span>           | <span data-ttu-id="9ac7f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ac7f-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="9ac7f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-150">System-Flags</span></span>           | <span data-ttu-id="9ac7f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ac7f-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="9ac7f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ac7f-152">Classes used in</span></span>        | [<span data-ttu-id="9ac7f-153">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-153">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9ac7f-154">亞當</span><span class="sxs-lookup"><span data-stu-id="9ac7f-154">ADAM</span></span>



| <span data-ttu-id="9ac7f-155">進入</span><span class="sxs-lookup"><span data-stu-id="9ac7f-155">Entry</span></span> | <span data-ttu-id="9ac7f-156">值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9ac7f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ac7f-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ac7f-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ac7f-159">System-Only</span></span>            | <span data-ttu-id="9ac7f-160">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-160">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9ac7f-162">對</span><span class="sxs-lookup"><span data-stu-id="9ac7f-162">True</span></span>                                                              |
| <span data-ttu-id="9ac7f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ac7f-163">Is Indexed</span></span>             | <span data-ttu-id="9ac7f-164">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-164">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ac7f-165">In Global Catalog</span></span>      | <span data-ttu-id="9ac7f-166">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-166">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ac7f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ac7f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ac7f-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9ac7f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ac7f-169">Range-Lower</span></span>            | <span data-ttu-id="9ac7f-170">0</span><span class="sxs-lookup"><span data-stu-id="9ac7f-170">0</span></span>                                                                 |
| <span data-ttu-id="9ac7f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ac7f-171">Range-Upper</span></span>            | <span data-ttu-id="9ac7f-172">100</span><span class="sxs-lookup"><span data-stu-id="9ac7f-172">100</span></span>                                                               |
| <span data-ttu-id="9ac7f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-173">Search-Flags</span></span>           | <span data-ttu-id="9ac7f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ac7f-174">0x00000000</span></span>                                                        |
| <span data-ttu-id="9ac7f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-175">System-Flags</span></span>           | <span data-ttu-id="9ac7f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ac7f-176">0x00000010</span></span>                                                        |
| <span data-ttu-id="9ac7f-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ac7f-177">Classes used in</span></span>        | [<span data-ttu-id="9ac7f-178">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-178">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ac7f-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ac7f-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ac7f-180">進入</span><span class="sxs-lookup"><span data-stu-id="9ac7f-180">Entry</span></span> | <span data-ttu-id="9ac7f-181">值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9ac7f-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ac7f-182">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ac7f-183">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ac7f-184">System-Only</span></span>            | <span data-ttu-id="9ac7f-185">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-185">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9ac7f-187">對</span><span class="sxs-lookup"><span data-stu-id="9ac7f-187">True</span></span>                                                              |
| <span data-ttu-id="9ac7f-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ac7f-188">Is Indexed</span></span>             | <span data-ttu-id="9ac7f-189">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-189">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ac7f-190">In Global Catalog</span></span>      | <span data-ttu-id="9ac7f-191">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-191">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ac7f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ac7f-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ac7f-193">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9ac7f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ac7f-194">Range-Lower</span></span>            | <span data-ttu-id="9ac7f-195">0</span><span class="sxs-lookup"><span data-stu-id="9ac7f-195">0</span></span>                                                                 |
| <span data-ttu-id="9ac7f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ac7f-196">Range-Upper</span></span>            | <span data-ttu-id="9ac7f-197">100</span><span class="sxs-lookup"><span data-stu-id="9ac7f-197">100</span></span>                                                               |
| <span data-ttu-id="9ac7f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-198">Search-Flags</span></span>           | <span data-ttu-id="9ac7f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ac7f-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="9ac7f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-200">System-Flags</span></span>           | <span data-ttu-id="9ac7f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ac7f-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="9ac7f-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ac7f-202">Classes used in</span></span>        | [<span data-ttu-id="9ac7f-203">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-203">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ac7f-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ac7f-204">Windows Server 2008</span></span>



| <span data-ttu-id="9ac7f-205">進入</span><span class="sxs-lookup"><span data-stu-id="9ac7f-205">Entry</span></span> | <span data-ttu-id="9ac7f-206">值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9ac7f-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ac7f-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ac7f-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ac7f-209">System-Only</span></span>            | <span data-ttu-id="9ac7f-210">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-210">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9ac7f-212">對</span><span class="sxs-lookup"><span data-stu-id="9ac7f-212">True</span></span>                                                              |
| <span data-ttu-id="9ac7f-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ac7f-213">Is Indexed</span></span>             | <span data-ttu-id="9ac7f-214">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-214">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ac7f-215">In Global Catalog</span></span>      | <span data-ttu-id="9ac7f-216">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-216">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ac7f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ac7f-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ac7f-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9ac7f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ac7f-219">Range-Lower</span></span>            | <span data-ttu-id="9ac7f-220">0</span><span class="sxs-lookup"><span data-stu-id="9ac7f-220">0</span></span>                                                                 |
| <span data-ttu-id="9ac7f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ac7f-221">Range-Upper</span></span>            | <span data-ttu-id="9ac7f-222">100</span><span class="sxs-lookup"><span data-stu-id="9ac7f-222">100</span></span>                                                               |
| <span data-ttu-id="9ac7f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-223">Search-Flags</span></span>           | <span data-ttu-id="9ac7f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ac7f-224">0x00000000</span></span>                                                        |
| <span data-ttu-id="9ac7f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-225">System-Flags</span></span>           | <span data-ttu-id="9ac7f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ac7f-226">0x00000010</span></span>                                                        |
| <span data-ttu-id="9ac7f-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ac7f-227">Classes used in</span></span>        | [<span data-ttu-id="9ac7f-228">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-228">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ac7f-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ac7f-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ac7f-230">進入</span><span class="sxs-lookup"><span data-stu-id="9ac7f-230">Entry</span></span> | <span data-ttu-id="9ac7f-231">值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9ac7f-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ac7f-232">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ac7f-233">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ac7f-234">System-Only</span></span>            | <span data-ttu-id="9ac7f-235">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-235">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="9ac7f-237">對</span><span class="sxs-lookup"><span data-stu-id="9ac7f-237">True</span></span>                                                              |
| <span data-ttu-id="9ac7f-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ac7f-238">Is Indexed</span></span>             | <span data-ttu-id="9ac7f-239">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-239">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ac7f-240">In Global Catalog</span></span>      | <span data-ttu-id="9ac7f-241">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-241">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ac7f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ac7f-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ac7f-243">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9ac7f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ac7f-244">Range-Lower</span></span>            | <span data-ttu-id="9ac7f-245">0</span><span class="sxs-lookup"><span data-stu-id="9ac7f-245">0</span></span>                                                                 |
| <span data-ttu-id="9ac7f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ac7f-246">Range-Upper</span></span>            | <span data-ttu-id="9ac7f-247">100</span><span class="sxs-lookup"><span data-stu-id="9ac7f-247">100</span></span>                                                               |
| <span data-ttu-id="9ac7f-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-248">Search-Flags</span></span>           | <span data-ttu-id="9ac7f-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ac7f-249">0x00000000</span></span>                                                        |
| <span data-ttu-id="9ac7f-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-250">System-Flags</span></span>           | <span data-ttu-id="9ac7f-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ac7f-251">0x00000010</span></span>                                                        |
| <span data-ttu-id="9ac7f-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ac7f-252">Classes used in</span></span>        | [<span data-ttu-id="9ac7f-253">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-253">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ac7f-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ac7f-254">Windows Server 2012</span></span>



| <span data-ttu-id="9ac7f-255">進入</span><span class="sxs-lookup"><span data-stu-id="9ac7f-255">Entry</span></span> | <span data-ttu-id="9ac7f-256">值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9ac7f-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ac7f-257">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ac7f-258">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9ac7f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ac7f-259">System-Only</span></span>            | <span data-ttu-id="9ac7f-260">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-260">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ac7f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="9ac7f-262">對</span><span class="sxs-lookup"><span data-stu-id="9ac7f-262">True</span></span>                                                              |
| <span data-ttu-id="9ac7f-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ac7f-263">Is Indexed</span></span>             | <span data-ttu-id="9ac7f-264">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-264">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ac7f-265">In Global Catalog</span></span>      | <span data-ttu-id="9ac7f-266">否</span><span class="sxs-lookup"><span data-stu-id="9ac7f-266">False</span></span>                                                             |
| <span data-ttu-id="9ac7f-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ac7f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ac7f-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ac7f-268">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9ac7f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ac7f-269">Range-Lower</span></span>            | <span data-ttu-id="9ac7f-270">0</span><span class="sxs-lookup"><span data-stu-id="9ac7f-270">0</span></span>                                                                 |
| <span data-ttu-id="9ac7f-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ac7f-271">Range-Upper</span></span>            | <span data-ttu-id="9ac7f-272">100</span><span class="sxs-lookup"><span data-stu-id="9ac7f-272">100</span></span>                                                               |
| <span data-ttu-id="9ac7f-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-273">Search-Flags</span></span>           | <span data-ttu-id="9ac7f-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ac7f-274">0x00000000</span></span>                                                        |
| <span data-ttu-id="9ac7f-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ac7f-275">System-Flags</span></span>           | <span data-ttu-id="9ac7f-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ac7f-276">0x00000010</span></span>                                                        |
| <span data-ttu-id="9ac7f-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ac7f-277">Classes used in</span></span>        | [<span data-ttu-id="9ac7f-278">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="9ac7f-278">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





