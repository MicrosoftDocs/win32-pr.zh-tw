---
title: ms DS-預設配額屬性
description: 如果沒有涵蓋安全性主體的配額規格，則會套用至在 NC 中建立物件的安全性主體所適用的預設配額。
ms.assetid: 48074aaa-3997-40ac-92fe-b3112408ab45
ms.tgt_platform: multiple
keywords:
- ms DS-預設配額屬性 AD 架構
- DefaultQuota 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Default-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96f1429be72c623843608856da88729b1240c38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935548"
---
# <a name="ms-ds-default-quota-attribute"></a><span data-ttu-id="bdddb-105">ms DS-預設配額屬性</span><span class="sxs-lookup"><span data-stu-id="bdddb-105">ms-DS-Default-Quota attribute</span></span>

<span data-ttu-id="bdddb-106">如果沒有涵蓋安全性主體的配額規格，則會套用至在 NC 中建立物件的安全性主體所適用的預設配額。</span><span class="sxs-lookup"><span data-stu-id="bdddb-106">The default quota that will apply to a security principal that creates an object in the NC if no quota specification exists that covers the security principal.</span></span>



| <span data-ttu-id="bdddb-107">進入</span><span class="sxs-lookup"><span data-stu-id="bdddb-107">Entry</span></span> | <span data-ttu-id="bdddb-108">值</span><span class="sxs-lookup"><span data-stu-id="bdddb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bdddb-109">CN</span><span class="sxs-lookup"><span data-stu-id="bdddb-109">CN</span></span>                | <span data-ttu-id="bdddb-110">ms DS-預設配額</span><span class="sxs-lookup"><span data-stu-id="bdddb-110">ms-DS-Default-Quota</span></span>                  |
| <span data-ttu-id="bdddb-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bdddb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bdddb-112">DefaultQuota</span><span class="sxs-lookup"><span data-stu-id="bdddb-112">msDS-DefaultQuota</span></span>                    |
| <span data-ttu-id="bdddb-113">大小</span><span class="sxs-lookup"><span data-stu-id="bdddb-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="bdddb-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bdddb-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="bdddb-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bdddb-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bdddb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bdddb-116">Attribute-Id</span></span>      | <span data-ttu-id="bdddb-117">1.2.840.113556.1.4.1846</span><span class="sxs-lookup"><span data-stu-id="bdddb-117">1.2.840.113556.1.4.1846</span></span>              |
| <span data-ttu-id="bdddb-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bdddb-118">System-Id-Guid</span></span>    | <span data-ttu-id="bdddb-119">6818f726-674b-441b-8a3a-f40596374cea</span><span class="sxs-lookup"><span data-stu-id="bdddb-119">6818f726-674b-441b-8a3a-f40596374cea</span></span> |
| <span data-ttu-id="bdddb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdddb-120">Syntax</span></span>            | [<span data-ttu-id="bdddb-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="bdddb-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bdddb-122">實作</span><span class="sxs-lookup"><span data-stu-id="bdddb-122">Implementations</span></span>

-   [<span data-ttu-id="bdddb-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bdddb-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bdddb-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="bdddb-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bdddb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bdddb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bdddb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bdddb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bdddb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bdddb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bdddb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bdddb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="bdddb-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bdddb-129">Windows Server 2003</span></span>



| <span data-ttu-id="bdddb-130">進入</span><span class="sxs-lookup"><span data-stu-id="bdddb-130">Entry</span></span> | <span data-ttu-id="bdddb-131">值</span><span class="sxs-lookup"><span data-stu-id="bdddb-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bdddb-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bdddb-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdddb-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdddb-134">System-Only</span></span>            | <span data-ttu-id="bdddb-135">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-135">False</span></span>                                                             |
| <span data-ttu-id="bdddb-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bdddb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="bdddb-137">對</span><span class="sxs-lookup"><span data-stu-id="bdddb-137">True</span></span>                                                              |
| <span data-ttu-id="bdddb-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bdddb-138">Is Indexed</span></span>             | <span data-ttu-id="bdddb-139">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-139">False</span></span>                                                             |
| <span data-ttu-id="bdddb-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bdddb-140">In Global Catalog</span></span>      | <span data-ttu-id="bdddb-141">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-141">False</span></span>                                                             |
| <span data-ttu-id="bdddb-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bdddb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdddb-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bdddb-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bdddb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdddb-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdddb-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-146">Search-Flags</span></span>           | <span data-ttu-id="bdddb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdddb-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="bdddb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-148">System-Flags</span></span>           | <span data-ttu-id="bdddb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdddb-149">0x00000010</span></span>                                                        |
| <span data-ttu-id="bdddb-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bdddb-150">Classes used in</span></span>        | [<span data-ttu-id="bdddb-151">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="bdddb-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bdddb-152">亞當</span><span class="sxs-lookup"><span data-stu-id="bdddb-152">ADAM</span></span>



| <span data-ttu-id="bdddb-153">進入</span><span class="sxs-lookup"><span data-stu-id="bdddb-153">Entry</span></span> | <span data-ttu-id="bdddb-154">值</span><span class="sxs-lookup"><span data-stu-id="bdddb-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bdddb-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bdddb-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdddb-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdddb-157">System-Only</span></span>            | <span data-ttu-id="bdddb-158">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-158">False</span></span>                                                             |
| <span data-ttu-id="bdddb-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bdddb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="bdddb-160">對</span><span class="sxs-lookup"><span data-stu-id="bdddb-160">True</span></span>                                                              |
| <span data-ttu-id="bdddb-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bdddb-161">Is Indexed</span></span>             | <span data-ttu-id="bdddb-162">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-162">False</span></span>                                                             |
| <span data-ttu-id="bdddb-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bdddb-163">In Global Catalog</span></span>      | <span data-ttu-id="bdddb-164">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-164">False</span></span>                                                             |
| <span data-ttu-id="bdddb-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bdddb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdddb-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bdddb-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bdddb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdddb-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdddb-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-169">Search-Flags</span></span>           | <span data-ttu-id="bdddb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdddb-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="bdddb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-171">System-Flags</span></span>           | <span data-ttu-id="bdddb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdddb-172">0x00000010</span></span>                                                        |
| <span data-ttu-id="bdddb-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bdddb-173">Classes used in</span></span>        | [<span data-ttu-id="bdddb-174">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="bdddb-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bdddb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bdddb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bdddb-176">進入</span><span class="sxs-lookup"><span data-stu-id="bdddb-176">Entry</span></span> | <span data-ttu-id="bdddb-177">值</span><span class="sxs-lookup"><span data-stu-id="bdddb-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bdddb-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bdddb-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdddb-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdddb-180">System-Only</span></span>            | <span data-ttu-id="bdddb-181">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-181">False</span></span>                                                             |
| <span data-ttu-id="bdddb-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bdddb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="bdddb-183">對</span><span class="sxs-lookup"><span data-stu-id="bdddb-183">True</span></span>                                                              |
| <span data-ttu-id="bdddb-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bdddb-184">Is Indexed</span></span>             | <span data-ttu-id="bdddb-185">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-185">False</span></span>                                                             |
| <span data-ttu-id="bdddb-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bdddb-186">In Global Catalog</span></span>      | <span data-ttu-id="bdddb-187">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-187">False</span></span>                                                             |
| <span data-ttu-id="bdddb-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bdddb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdddb-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bdddb-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bdddb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdddb-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdddb-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-192">Search-Flags</span></span>           | <span data-ttu-id="bdddb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdddb-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="bdddb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-194">System-Flags</span></span>           | <span data-ttu-id="bdddb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdddb-195">0x00000010</span></span>                                                        |
| <span data-ttu-id="bdddb-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bdddb-196">Classes used in</span></span>        | [<span data-ttu-id="bdddb-197">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="bdddb-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bdddb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdddb-198">Windows Server 2008</span></span>



| <span data-ttu-id="bdddb-199">進入</span><span class="sxs-lookup"><span data-stu-id="bdddb-199">Entry</span></span> | <span data-ttu-id="bdddb-200">值</span><span class="sxs-lookup"><span data-stu-id="bdddb-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bdddb-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bdddb-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdddb-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdddb-203">System-Only</span></span>            | <span data-ttu-id="bdddb-204">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-204">False</span></span>                                                             |
| <span data-ttu-id="bdddb-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bdddb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="bdddb-206">對</span><span class="sxs-lookup"><span data-stu-id="bdddb-206">True</span></span>                                                              |
| <span data-ttu-id="bdddb-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bdddb-207">Is Indexed</span></span>             | <span data-ttu-id="bdddb-208">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-208">False</span></span>                                                             |
| <span data-ttu-id="bdddb-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bdddb-209">In Global Catalog</span></span>      | <span data-ttu-id="bdddb-210">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-210">False</span></span>                                                             |
| <span data-ttu-id="bdddb-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bdddb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdddb-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bdddb-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bdddb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdddb-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdddb-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-215">Search-Flags</span></span>           | <span data-ttu-id="bdddb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdddb-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="bdddb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-217">System-Flags</span></span>           | <span data-ttu-id="bdddb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdddb-218">0x00000010</span></span>                                                        |
| <span data-ttu-id="bdddb-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bdddb-219">Classes used in</span></span>        | [<span data-ttu-id="bdddb-220">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="bdddb-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bdddb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bdddb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bdddb-222">進入</span><span class="sxs-lookup"><span data-stu-id="bdddb-222">Entry</span></span> | <span data-ttu-id="bdddb-223">值</span><span class="sxs-lookup"><span data-stu-id="bdddb-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bdddb-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bdddb-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdddb-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdddb-226">System-Only</span></span>            | <span data-ttu-id="bdddb-227">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-227">False</span></span>                                                             |
| <span data-ttu-id="bdddb-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bdddb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="bdddb-229">對</span><span class="sxs-lookup"><span data-stu-id="bdddb-229">True</span></span>                                                              |
| <span data-ttu-id="bdddb-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bdddb-230">Is Indexed</span></span>             | <span data-ttu-id="bdddb-231">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-231">False</span></span>                                                             |
| <span data-ttu-id="bdddb-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bdddb-232">In Global Catalog</span></span>      | <span data-ttu-id="bdddb-233">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-233">False</span></span>                                                             |
| <span data-ttu-id="bdddb-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bdddb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdddb-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bdddb-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bdddb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdddb-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdddb-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-238">Search-Flags</span></span>           | <span data-ttu-id="bdddb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdddb-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="bdddb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-240">System-Flags</span></span>           | <span data-ttu-id="bdddb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdddb-241">0x00000010</span></span>                                                        |
| <span data-ttu-id="bdddb-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bdddb-242">Classes used in</span></span>        | [<span data-ttu-id="bdddb-243">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="bdddb-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bdddb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bdddb-244">Windows Server 2012</span></span>



| <span data-ttu-id="bdddb-245">進入</span><span class="sxs-lookup"><span data-stu-id="bdddb-245">Entry</span></span> | <span data-ttu-id="bdddb-246">值</span><span class="sxs-lookup"><span data-stu-id="bdddb-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bdddb-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bdddb-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdddb-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bdddb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdddb-249">System-Only</span></span>            | <span data-ttu-id="bdddb-250">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-250">False</span></span>                                                             |
| <span data-ttu-id="bdddb-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bdddb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="bdddb-252">對</span><span class="sxs-lookup"><span data-stu-id="bdddb-252">True</span></span>                                                              |
| <span data-ttu-id="bdddb-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bdddb-253">Is Indexed</span></span>             | <span data-ttu-id="bdddb-254">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-254">False</span></span>                                                             |
| <span data-ttu-id="bdddb-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bdddb-255">In Global Catalog</span></span>      | <span data-ttu-id="bdddb-256">否</span><span class="sxs-lookup"><span data-stu-id="bdddb-256">False</span></span>                                                             |
| <span data-ttu-id="bdddb-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bdddb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdddb-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bdddb-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bdddb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdddb-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdddb-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bdddb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-261">Search-Flags</span></span>           | <span data-ttu-id="bdddb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdddb-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="bdddb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdddb-263">System-Flags</span></span>           | <span data-ttu-id="bdddb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdddb-264">0x00000010</span></span>                                                        |
| <span data-ttu-id="bdddb-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bdddb-265">Classes used in</span></span>        | [<span data-ttu-id="bdddb-266">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="bdddb-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





