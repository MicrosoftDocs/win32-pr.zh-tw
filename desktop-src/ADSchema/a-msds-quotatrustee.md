---
title: ms DS-配額-受信任的屬性
description: 指派配額之安全性主體的 SID。
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- ms DS-配額-受信任的屬性 AD 架構
- QuotaTrustee 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7733e74c2f5d381aa6f52ea58bb03c377fab7cbe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970657"
---
# <a name="ms-ds-quota-trustee-attribute"></a><span data-ttu-id="f90ab-105">ms DS-配額-受信任的屬性</span><span class="sxs-lookup"><span data-stu-id="f90ab-105">ms-DS-Quota-Trustee attribute</span></span>

<span data-ttu-id="f90ab-106">指派配額之安全性主體的 SID。</span><span class="sxs-lookup"><span data-stu-id="f90ab-106">The SID of the security principal for which the quota is being assigned.</span></span>



| <span data-ttu-id="f90ab-107">進入</span><span class="sxs-lookup"><span data-stu-id="f90ab-107">Entry</span></span> | <span data-ttu-id="f90ab-108">值</span><span class="sxs-lookup"><span data-stu-id="f90ab-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f90ab-109">CN</span><span class="sxs-lookup"><span data-stu-id="f90ab-109">CN</span></span>                | <span data-ttu-id="f90ab-110">ms DS-配額-信任者</span><span class="sxs-lookup"><span data-stu-id="f90ab-110">ms-DS-Quota-Trustee</span></span>                  |
| <span data-ttu-id="f90ab-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f90ab-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f90ab-112">QuotaTrustee</span><span class="sxs-lookup"><span data-stu-id="f90ab-112">msDS-QuotaTrustee</span></span>                    |
| <span data-ttu-id="f90ab-113">大小</span><span class="sxs-lookup"><span data-stu-id="f90ab-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f90ab-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f90ab-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f90ab-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f90ab-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f90ab-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f90ab-116">Attribute-Id</span></span>      | <span data-ttu-id="f90ab-117">1.2.840.113556.1.4.1844</span><span class="sxs-lookup"><span data-stu-id="f90ab-117">1.2.840.113556.1.4.1844</span></span>              |
| <span data-ttu-id="f90ab-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f90ab-118">System-Id-Guid</span></span>    | <span data-ttu-id="f90ab-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span><span class="sxs-lookup"><span data-stu-id="f90ab-119">16378906-4ea5-49be-a8d1-bfd41dff4f65</span></span> |
| <span data-ttu-id="f90ab-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f90ab-120">Syntax</span></span>            | [<span data-ttu-id="f90ab-121">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="f90ab-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="f90ab-122">實作</span><span class="sxs-lookup"><span data-stu-id="f90ab-122">Implementations</span></span>

-   [<span data-ttu-id="f90ab-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f90ab-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f90ab-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f90ab-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f90ab-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f90ab-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f90ab-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f90ab-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f90ab-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f90ab-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f90ab-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f90ab-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f90ab-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f90ab-129">Windows Server 2003</span></span>



| <span data-ttu-id="f90ab-130">進入</span><span class="sxs-lookup"><span data-stu-id="f90ab-130">Entry</span></span> | <span data-ttu-id="f90ab-131">值</span><span class="sxs-lookup"><span data-stu-id="f90ab-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f90ab-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f90ab-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f90ab-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f90ab-134">System-Only</span></span>            | <span data-ttu-id="f90ab-135">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-135">False</span></span>                                                         |
| <span data-ttu-id="f90ab-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f90ab-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f90ab-137">對</span><span class="sxs-lookup"><span data-stu-id="f90ab-137">True</span></span>                                                          |
| <span data-ttu-id="f90ab-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f90ab-138">Is Indexed</span></span>             | <span data-ttu-id="f90ab-139">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-139">False</span></span>                                                         |
| <span data-ttu-id="f90ab-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f90ab-140">In Global Catalog</span></span>      | <span data-ttu-id="f90ab-141">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-141">False</span></span>                                                         |
| <span data-ttu-id="f90ab-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f90ab-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f90ab-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f90ab-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f90ab-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f90ab-144">Range-Lower</span></span>            | <span data-ttu-id="f90ab-145">0</span><span class="sxs-lookup"><span data-stu-id="f90ab-145">0</span></span>                                                             |
| <span data-ttu-id="f90ab-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f90ab-146">Range-Upper</span></span>            | <span data-ttu-id="f90ab-147">28</span><span class="sxs-lookup"><span data-stu-id="f90ab-147">28</span></span>                                                            |
| <span data-ttu-id="f90ab-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-148">Search-Flags</span></span>           | <span data-ttu-id="f90ab-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f90ab-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="f90ab-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-150">System-Flags</span></span>           | <span data-ttu-id="f90ab-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f90ab-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="f90ab-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f90ab-152">Classes used in</span></span>        | [<span data-ttu-id="f90ab-153">**ms-DS-配額-控制**</span><span class="sxs-lookup"><span data-stu-id="f90ab-153">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f90ab-154">亞當</span><span class="sxs-lookup"><span data-stu-id="f90ab-154">ADAM</span></span>



| <span data-ttu-id="f90ab-155">進入</span><span class="sxs-lookup"><span data-stu-id="f90ab-155">Entry</span></span> | <span data-ttu-id="f90ab-156">值</span><span class="sxs-lookup"><span data-stu-id="f90ab-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f90ab-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f90ab-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f90ab-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f90ab-159">System-Only</span></span>            | <span data-ttu-id="f90ab-160">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-160">False</span></span>                                                         |
| <span data-ttu-id="f90ab-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f90ab-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f90ab-162">對</span><span class="sxs-lookup"><span data-stu-id="f90ab-162">True</span></span>                                                          |
| <span data-ttu-id="f90ab-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f90ab-163">Is Indexed</span></span>             | <span data-ttu-id="f90ab-164">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-164">False</span></span>                                                         |
| <span data-ttu-id="f90ab-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f90ab-165">In Global Catalog</span></span>      | <span data-ttu-id="f90ab-166">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-166">False</span></span>                                                         |
| <span data-ttu-id="f90ab-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f90ab-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f90ab-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f90ab-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f90ab-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f90ab-169">Range-Lower</span></span>            | <span data-ttu-id="f90ab-170">0</span><span class="sxs-lookup"><span data-stu-id="f90ab-170">0</span></span>                                                             |
| <span data-ttu-id="f90ab-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f90ab-171">Range-Upper</span></span>            | <span data-ttu-id="f90ab-172">28</span><span class="sxs-lookup"><span data-stu-id="f90ab-172">28</span></span>                                                            |
| <span data-ttu-id="f90ab-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-173">Search-Flags</span></span>           | <span data-ttu-id="f90ab-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f90ab-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="f90ab-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-175">System-Flags</span></span>           | <span data-ttu-id="f90ab-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f90ab-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="f90ab-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f90ab-177">Classes used in</span></span>        | [<span data-ttu-id="f90ab-178">**ms-DS-配額-控制**</span><span class="sxs-lookup"><span data-stu-id="f90ab-178">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f90ab-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f90ab-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f90ab-180">進入</span><span class="sxs-lookup"><span data-stu-id="f90ab-180">Entry</span></span> | <span data-ttu-id="f90ab-181">值</span><span class="sxs-lookup"><span data-stu-id="f90ab-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f90ab-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f90ab-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f90ab-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f90ab-184">System-Only</span></span>            | <span data-ttu-id="f90ab-185">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-185">False</span></span>                                                         |
| <span data-ttu-id="f90ab-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f90ab-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f90ab-187">對</span><span class="sxs-lookup"><span data-stu-id="f90ab-187">True</span></span>                                                          |
| <span data-ttu-id="f90ab-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f90ab-188">Is Indexed</span></span>             | <span data-ttu-id="f90ab-189">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-189">False</span></span>                                                         |
| <span data-ttu-id="f90ab-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f90ab-190">In Global Catalog</span></span>      | <span data-ttu-id="f90ab-191">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-191">False</span></span>                                                         |
| <span data-ttu-id="f90ab-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f90ab-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f90ab-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f90ab-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f90ab-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f90ab-194">Range-Lower</span></span>            | <span data-ttu-id="f90ab-195">0</span><span class="sxs-lookup"><span data-stu-id="f90ab-195">0</span></span>                                                             |
| <span data-ttu-id="f90ab-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f90ab-196">Range-Upper</span></span>            | <span data-ttu-id="f90ab-197">28</span><span class="sxs-lookup"><span data-stu-id="f90ab-197">28</span></span>                                                            |
| <span data-ttu-id="f90ab-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-198">Search-Flags</span></span>           | <span data-ttu-id="f90ab-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f90ab-199">0x00000000</span></span>                                                    |
| <span data-ttu-id="f90ab-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-200">System-Flags</span></span>           | <span data-ttu-id="f90ab-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f90ab-201">0x00000010</span></span>                                                    |
| <span data-ttu-id="f90ab-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f90ab-202">Classes used in</span></span>        | [<span data-ttu-id="f90ab-203">**ms-DS-配額-控制**</span><span class="sxs-lookup"><span data-stu-id="f90ab-203">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f90ab-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f90ab-204">Windows Server 2008</span></span>



| <span data-ttu-id="f90ab-205">進入</span><span class="sxs-lookup"><span data-stu-id="f90ab-205">Entry</span></span> | <span data-ttu-id="f90ab-206">值</span><span class="sxs-lookup"><span data-stu-id="f90ab-206">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f90ab-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f90ab-207">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f90ab-208">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f90ab-209">System-Only</span></span>            | <span data-ttu-id="f90ab-210">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-210">False</span></span>                                                         |
| <span data-ttu-id="f90ab-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f90ab-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f90ab-212">對</span><span class="sxs-lookup"><span data-stu-id="f90ab-212">True</span></span>                                                          |
| <span data-ttu-id="f90ab-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f90ab-213">Is Indexed</span></span>             | <span data-ttu-id="f90ab-214">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-214">False</span></span>                                                         |
| <span data-ttu-id="f90ab-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f90ab-215">In Global Catalog</span></span>      | <span data-ttu-id="f90ab-216">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-216">False</span></span>                                                         |
| <span data-ttu-id="f90ab-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f90ab-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f90ab-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f90ab-218">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f90ab-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f90ab-219">Range-Lower</span></span>            | <span data-ttu-id="f90ab-220">0</span><span class="sxs-lookup"><span data-stu-id="f90ab-220">0</span></span>                                                             |
| <span data-ttu-id="f90ab-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f90ab-221">Range-Upper</span></span>            | <span data-ttu-id="f90ab-222">28</span><span class="sxs-lookup"><span data-stu-id="f90ab-222">28</span></span>                                                            |
| <span data-ttu-id="f90ab-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-223">Search-Flags</span></span>           | <span data-ttu-id="f90ab-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f90ab-224">0x00000000</span></span>                                                    |
| <span data-ttu-id="f90ab-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-225">System-Flags</span></span>           | <span data-ttu-id="f90ab-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f90ab-226">0x00000010</span></span>                                                    |
| <span data-ttu-id="f90ab-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f90ab-227">Classes used in</span></span>        | [<span data-ttu-id="f90ab-228">**ms-DS-配額-控制**</span><span class="sxs-lookup"><span data-stu-id="f90ab-228">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f90ab-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f90ab-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f90ab-230">進入</span><span class="sxs-lookup"><span data-stu-id="f90ab-230">Entry</span></span> | <span data-ttu-id="f90ab-231">值</span><span class="sxs-lookup"><span data-stu-id="f90ab-231">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f90ab-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f90ab-232">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f90ab-233">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="f90ab-234">System-Only</span></span>            | <span data-ttu-id="f90ab-235">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-235">False</span></span>                                                         |
| <span data-ttu-id="f90ab-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f90ab-236">Is-Single-Valued</span></span>       | <span data-ttu-id="f90ab-237">對</span><span class="sxs-lookup"><span data-stu-id="f90ab-237">True</span></span>                                                          |
| <span data-ttu-id="f90ab-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f90ab-238">Is Indexed</span></span>             | <span data-ttu-id="f90ab-239">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-239">False</span></span>                                                         |
| <span data-ttu-id="f90ab-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f90ab-240">In Global Catalog</span></span>      | <span data-ttu-id="f90ab-241">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-241">False</span></span>                                                         |
| <span data-ttu-id="f90ab-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f90ab-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="f90ab-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f90ab-243">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f90ab-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f90ab-244">Range-Lower</span></span>            | <span data-ttu-id="f90ab-245">0</span><span class="sxs-lookup"><span data-stu-id="f90ab-245">0</span></span>                                                             |
| <span data-ttu-id="f90ab-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f90ab-246">Range-Upper</span></span>            | <span data-ttu-id="f90ab-247">28</span><span class="sxs-lookup"><span data-stu-id="f90ab-247">28</span></span>                                                            |
| <span data-ttu-id="f90ab-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-248">Search-Flags</span></span>           | <span data-ttu-id="f90ab-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f90ab-249">0x00000000</span></span>                                                    |
| <span data-ttu-id="f90ab-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-250">System-Flags</span></span>           | <span data-ttu-id="f90ab-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f90ab-251">0x00000010</span></span>                                                    |
| <span data-ttu-id="f90ab-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f90ab-252">Classes used in</span></span>        | [<span data-ttu-id="f90ab-253">**ms-DS-配額-控制**</span><span class="sxs-lookup"><span data-stu-id="f90ab-253">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f90ab-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f90ab-254">Windows Server 2012</span></span>



| <span data-ttu-id="f90ab-255">進入</span><span class="sxs-lookup"><span data-stu-id="f90ab-255">Entry</span></span> | <span data-ttu-id="f90ab-256">值</span><span class="sxs-lookup"><span data-stu-id="f90ab-256">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f90ab-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f90ab-257">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f90ab-258">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f90ab-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="f90ab-259">System-Only</span></span>            | <span data-ttu-id="f90ab-260">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-260">False</span></span>                                                         |
| <span data-ttu-id="f90ab-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f90ab-261">Is-Single-Valued</span></span>       | <span data-ttu-id="f90ab-262">對</span><span class="sxs-lookup"><span data-stu-id="f90ab-262">True</span></span>                                                          |
| <span data-ttu-id="f90ab-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f90ab-263">Is Indexed</span></span>             | <span data-ttu-id="f90ab-264">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-264">False</span></span>                                                         |
| <span data-ttu-id="f90ab-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f90ab-265">In Global Catalog</span></span>      | <span data-ttu-id="f90ab-266">否</span><span class="sxs-lookup"><span data-stu-id="f90ab-266">False</span></span>                                                         |
| <span data-ttu-id="f90ab-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f90ab-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="f90ab-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f90ab-268">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f90ab-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f90ab-269">Range-Lower</span></span>            | <span data-ttu-id="f90ab-270">0</span><span class="sxs-lookup"><span data-stu-id="f90ab-270">0</span></span>                                                             |
| <span data-ttu-id="f90ab-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f90ab-271">Range-Upper</span></span>            | <span data-ttu-id="f90ab-272">28</span><span class="sxs-lookup"><span data-stu-id="f90ab-272">28</span></span>                                                            |
| <span data-ttu-id="f90ab-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-273">Search-Flags</span></span>           | <span data-ttu-id="f90ab-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f90ab-274">0x00000000</span></span>                                                    |
| <span data-ttu-id="f90ab-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f90ab-275">System-Flags</span></span>           | <span data-ttu-id="f90ab-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f90ab-276">0x00000010</span></span>                                                    |
| <span data-ttu-id="f90ab-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f90ab-277">Classes used in</span></span>        | [<span data-ttu-id="f90ab-278">**ms-DS-配額-控制**</span><span class="sxs-lookup"><span data-stu-id="f90ab-278">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





