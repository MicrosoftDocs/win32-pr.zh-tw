---
title: ms DS-配額-有效的屬性
description: 從為目錄分割指派配額計算的安全性主體有效配額。
ms.assetid: 22422499-9b56-4d74-a30e-63917abacdd1
ms.tgt_platform: multiple
keywords:
- ms DS-配額-有效的屬性 AD 架構
- QuotaEffective 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Quota-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe610c87c356431883cecded5eda3e0a9c42297
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467351"
---
# <a name="ms-ds-quota-effective-attribute"></a><span data-ttu-id="a0a15-105">ms DS-配額-有效的屬性</span><span class="sxs-lookup"><span data-stu-id="a0a15-105">ms-DS-Quota-Effective attribute</span></span>

<span data-ttu-id="a0a15-106">從為目錄分割指派配額計算的安全性主體有效配額。</span><span class="sxs-lookup"><span data-stu-id="a0a15-106">The effective quota for a security principal computed from the assigned quotas for a directory partition.</span></span>



| <span data-ttu-id="a0a15-107">進入</span><span class="sxs-lookup"><span data-stu-id="a0a15-107">Entry</span></span> | <span data-ttu-id="a0a15-108">值</span><span class="sxs-lookup"><span data-stu-id="a0a15-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a0a15-109">CN</span><span class="sxs-lookup"><span data-stu-id="a0a15-109">CN</span></span>                | <span data-ttu-id="a0a15-110">ms DS-配額-有效</span><span class="sxs-lookup"><span data-stu-id="a0a15-110">ms-DS-Quota-Effective</span></span>                |
| <span data-ttu-id="a0a15-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a0a15-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a0a15-112">QuotaEffective</span><span class="sxs-lookup"><span data-stu-id="a0a15-112">msDS-QuotaEffective</span></span>                  |
| <span data-ttu-id="a0a15-113">大小</span><span class="sxs-lookup"><span data-stu-id="a0a15-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="a0a15-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a0a15-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a0a15-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a0a15-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a0a15-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a0a15-116">Attribute-Id</span></span>      | <span data-ttu-id="a0a15-117">1.2.840.113556.1.4.1848</span><span class="sxs-lookup"><span data-stu-id="a0a15-117">1.2.840.113556.1.4.1848</span></span>              |
| <span data-ttu-id="a0a15-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a0a15-118">System-Id-Guid</span></span>    | <span data-ttu-id="a0a15-119">6655b152-101c-48b4-b347-e1fcebc60157</span><span class="sxs-lookup"><span data-stu-id="a0a15-119">6655b152-101c-48b4-b347-e1fcebc60157</span></span> |
| <span data-ttu-id="a0a15-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0a15-120">Syntax</span></span>            | [<span data-ttu-id="a0a15-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="a0a15-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a0a15-122">實作</span><span class="sxs-lookup"><span data-stu-id="a0a15-122">Implementations</span></span>

-   [<span data-ttu-id="a0a15-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a0a15-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a0a15-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a0a15-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a0a15-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a0a15-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a0a15-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a0a15-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a0a15-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a0a15-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a0a15-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a0a15-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a0a15-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0a15-129">Windows Server 2003</span></span>



| <span data-ttu-id="a0a15-130">進入</span><span class="sxs-lookup"><span data-stu-id="a0a15-130">Entry</span></span> | <span data-ttu-id="a0a15-131">值</span><span class="sxs-lookup"><span data-stu-id="a0a15-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a0a15-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0a15-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a15-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a15-134">System-Only</span></span>            | <span data-ttu-id="a0a15-135">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-135">False</span></span>                                                             |
| <span data-ttu-id="a0a15-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0a15-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a15-137">對</span><span class="sxs-lookup"><span data-stu-id="a0a15-137">True</span></span>                                                              |
| <span data-ttu-id="a0a15-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0a15-138">Is Indexed</span></span>             | <span data-ttu-id="a0a15-139">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-139">False</span></span>                                                             |
| <span data-ttu-id="a0a15-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0a15-140">In Global Catalog</span></span>      | <span data-ttu-id="a0a15-141">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-141">False</span></span>                                                             |
| <span data-ttu-id="a0a15-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0a15-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a15-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0a15-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a0a15-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a15-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a15-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-146">Search-Flags</span></span>           | <span data-ttu-id="a0a15-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a15-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="a0a15-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-148">System-Flags</span></span>           | <span data-ttu-id="a0a15-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a0a15-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="a0a15-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0a15-150">Classes used in</span></span>        | [<span data-ttu-id="a0a15-151">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="a0a15-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a0a15-152">亞當</span><span class="sxs-lookup"><span data-stu-id="a0a15-152">ADAM</span></span>



| <span data-ttu-id="a0a15-153">進入</span><span class="sxs-lookup"><span data-stu-id="a0a15-153">Entry</span></span> | <span data-ttu-id="a0a15-154">值</span><span class="sxs-lookup"><span data-stu-id="a0a15-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a0a15-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0a15-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a15-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a15-157">System-Only</span></span>            | <span data-ttu-id="a0a15-158">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-158">False</span></span>                                                             |
| <span data-ttu-id="a0a15-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0a15-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a15-160">對</span><span class="sxs-lookup"><span data-stu-id="a0a15-160">True</span></span>                                                              |
| <span data-ttu-id="a0a15-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0a15-161">Is Indexed</span></span>             | <span data-ttu-id="a0a15-162">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-162">False</span></span>                                                             |
| <span data-ttu-id="a0a15-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0a15-163">In Global Catalog</span></span>      | <span data-ttu-id="a0a15-164">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-164">False</span></span>                                                             |
| <span data-ttu-id="a0a15-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0a15-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a15-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0a15-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a0a15-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a15-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a15-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-169">Search-Flags</span></span>           | <span data-ttu-id="a0a15-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a15-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="a0a15-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-171">System-Flags</span></span>           | <span data-ttu-id="a0a15-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a0a15-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="a0a15-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0a15-173">Classes used in</span></span>        | [<span data-ttu-id="a0a15-174">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="a0a15-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a0a15-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a0a15-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a0a15-176">進入</span><span class="sxs-lookup"><span data-stu-id="a0a15-176">Entry</span></span> | <span data-ttu-id="a0a15-177">值</span><span class="sxs-lookup"><span data-stu-id="a0a15-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a0a15-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0a15-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a15-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a15-180">System-Only</span></span>            | <span data-ttu-id="a0a15-181">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-181">False</span></span>                                                             |
| <span data-ttu-id="a0a15-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0a15-182">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a15-183">對</span><span class="sxs-lookup"><span data-stu-id="a0a15-183">True</span></span>                                                              |
| <span data-ttu-id="a0a15-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0a15-184">Is Indexed</span></span>             | <span data-ttu-id="a0a15-185">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-185">False</span></span>                                                             |
| <span data-ttu-id="a0a15-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0a15-186">In Global Catalog</span></span>      | <span data-ttu-id="a0a15-187">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-187">False</span></span>                                                             |
| <span data-ttu-id="a0a15-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0a15-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a15-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0a15-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a0a15-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a15-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a15-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-192">Search-Flags</span></span>           | <span data-ttu-id="a0a15-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a15-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="a0a15-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-194">System-Flags</span></span>           | <span data-ttu-id="a0a15-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a0a15-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="a0a15-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0a15-196">Classes used in</span></span>        | [<span data-ttu-id="a0a15-197">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="a0a15-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a0a15-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0a15-198">Windows Server 2008</span></span>



| <span data-ttu-id="a0a15-199">進入</span><span class="sxs-lookup"><span data-stu-id="a0a15-199">Entry</span></span> | <span data-ttu-id="a0a15-200">值</span><span class="sxs-lookup"><span data-stu-id="a0a15-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a0a15-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0a15-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a15-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a15-203">System-Only</span></span>            | <span data-ttu-id="a0a15-204">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-204">False</span></span>                                                             |
| <span data-ttu-id="a0a15-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0a15-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a15-206">對</span><span class="sxs-lookup"><span data-stu-id="a0a15-206">True</span></span>                                                              |
| <span data-ttu-id="a0a15-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0a15-207">Is Indexed</span></span>             | <span data-ttu-id="a0a15-208">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-208">False</span></span>                                                             |
| <span data-ttu-id="a0a15-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0a15-209">In Global Catalog</span></span>      | <span data-ttu-id="a0a15-210">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-210">False</span></span>                                                             |
| <span data-ttu-id="a0a15-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0a15-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a15-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0a15-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a0a15-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a15-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a15-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-215">Search-Flags</span></span>           | <span data-ttu-id="a0a15-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a15-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="a0a15-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-217">System-Flags</span></span>           | <span data-ttu-id="a0a15-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a0a15-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="a0a15-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0a15-219">Classes used in</span></span>        | [<span data-ttu-id="a0a15-220">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="a0a15-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a0a15-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0a15-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a0a15-222">進入</span><span class="sxs-lookup"><span data-stu-id="a0a15-222">Entry</span></span> | <span data-ttu-id="a0a15-223">值</span><span class="sxs-lookup"><span data-stu-id="a0a15-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a0a15-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0a15-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a15-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a15-226">System-Only</span></span>            | <span data-ttu-id="a0a15-227">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-227">False</span></span>                                                             |
| <span data-ttu-id="a0a15-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0a15-228">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a15-229">對</span><span class="sxs-lookup"><span data-stu-id="a0a15-229">True</span></span>                                                              |
| <span data-ttu-id="a0a15-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0a15-230">Is Indexed</span></span>             | <span data-ttu-id="a0a15-231">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-231">False</span></span>                                                             |
| <span data-ttu-id="a0a15-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0a15-232">In Global Catalog</span></span>      | <span data-ttu-id="a0a15-233">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-233">False</span></span>                                                             |
| <span data-ttu-id="a0a15-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0a15-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a15-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0a15-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a0a15-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a15-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a15-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-238">Search-Flags</span></span>           | <span data-ttu-id="a0a15-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a15-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="a0a15-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-240">System-Flags</span></span>           | <span data-ttu-id="a0a15-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a0a15-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="a0a15-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0a15-242">Classes used in</span></span>        | [<span data-ttu-id="a0a15-243">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="a0a15-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a0a15-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0a15-244">Windows Server 2012</span></span>



| <span data-ttu-id="a0a15-245">進入</span><span class="sxs-lookup"><span data-stu-id="a0a15-245">Entry</span></span> | <span data-ttu-id="a0a15-246">值</span><span class="sxs-lookup"><span data-stu-id="a0a15-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a0a15-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a0a15-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a15-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a0a15-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a15-249">System-Only</span></span>            | <span data-ttu-id="a0a15-250">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-250">False</span></span>                                                             |
| <span data-ttu-id="a0a15-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a0a15-251">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a15-252">對</span><span class="sxs-lookup"><span data-stu-id="a0a15-252">True</span></span>                                                              |
| <span data-ttu-id="a0a15-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a0a15-253">Is Indexed</span></span>             | <span data-ttu-id="a0a15-254">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-254">False</span></span>                                                             |
| <span data-ttu-id="a0a15-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a0a15-255">In Global Catalog</span></span>      | <span data-ttu-id="a0a15-256">否</span><span class="sxs-lookup"><span data-stu-id="a0a15-256">False</span></span>                                                             |
| <span data-ttu-id="a0a15-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a0a15-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a15-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a0a15-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a0a15-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a15-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a15-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a0a15-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-261">Search-Flags</span></span>           | <span data-ttu-id="a0a15-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a15-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="a0a15-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a15-263">System-Flags</span></span>           | <span data-ttu-id="a0a15-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a0a15-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="a0a15-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a0a15-265">Classes used in</span></span>        | [<span data-ttu-id="a0a15-266">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="a0a15-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





