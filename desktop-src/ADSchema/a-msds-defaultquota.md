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
# <a name="ms-ds-default-quota-attribute"></a><span data-ttu-id="f68d4-105">ms DS-預設配額屬性</span><span class="sxs-lookup"><span data-stu-id="f68d4-105">ms-DS-Default-Quota attribute</span></span>

<span data-ttu-id="f68d4-106">如果沒有涵蓋安全性主體的配額規格，則會套用至在 NC 中建立物件的安全性主體所適用的預設配額。</span><span class="sxs-lookup"><span data-stu-id="f68d4-106">The default quota that will apply to a security principal that creates an object in the NC if no quota specification exists that covers the security principal.</span></span>



| <span data-ttu-id="f68d4-107">進入</span><span class="sxs-lookup"><span data-stu-id="f68d4-107">Entry</span></span> | <span data-ttu-id="f68d4-108">值</span><span class="sxs-lookup"><span data-stu-id="f68d4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f68d4-109">CN</span><span class="sxs-lookup"><span data-stu-id="f68d4-109">CN</span></span>                | <span data-ttu-id="f68d4-110">ms DS-預設配額</span><span class="sxs-lookup"><span data-stu-id="f68d4-110">ms-DS-Default-Quota</span></span>                  |
| <span data-ttu-id="f68d4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f68d4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f68d4-112">DefaultQuota</span><span class="sxs-lookup"><span data-stu-id="f68d4-112">msDS-DefaultQuota</span></span>                    |
| <span data-ttu-id="f68d4-113">大小</span><span class="sxs-lookup"><span data-stu-id="f68d4-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f68d4-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f68d4-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f68d4-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f68d4-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f68d4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f68d4-116">Attribute-Id</span></span>      | <span data-ttu-id="f68d4-117">1.2.840.113556.1.4.1846</span><span class="sxs-lookup"><span data-stu-id="f68d4-117">1.2.840.113556.1.4.1846</span></span>              |
| <span data-ttu-id="f68d4-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f68d4-118">System-Id-Guid</span></span>    | <span data-ttu-id="f68d4-119">6818f726-674b-441b-8a3a-f40596374cea</span><span class="sxs-lookup"><span data-stu-id="f68d4-119">6818f726-674b-441b-8a3a-f40596374cea</span></span> |
| <span data-ttu-id="f68d4-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f68d4-120">Syntax</span></span>            | [<span data-ttu-id="f68d4-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="f68d4-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f68d4-122">實作</span><span class="sxs-lookup"><span data-stu-id="f68d4-122">Implementations</span></span>

-   [<span data-ttu-id="f68d4-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f68d4-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f68d4-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f68d4-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f68d4-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f68d4-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f68d4-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f68d4-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f68d4-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f68d4-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f68d4-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f68d4-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f68d4-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f68d4-129">Windows Server 2003</span></span>



| <span data-ttu-id="f68d4-130">進入</span><span class="sxs-lookup"><span data-stu-id="f68d4-130">Entry</span></span> | <span data-ttu-id="f68d4-131">值</span><span class="sxs-lookup"><span data-stu-id="f68d4-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f68d4-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f68d4-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f68d4-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f68d4-134">System-Only</span></span>            | <span data-ttu-id="f68d4-135">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-135">False</span></span>                                                             |
| <span data-ttu-id="f68d4-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f68d4-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f68d4-137">對</span><span class="sxs-lookup"><span data-stu-id="f68d4-137">True</span></span>                                                              |
| <span data-ttu-id="f68d4-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f68d4-138">Is Indexed</span></span>             | <span data-ttu-id="f68d4-139">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-139">False</span></span>                                                             |
| <span data-ttu-id="f68d4-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f68d4-140">In Global Catalog</span></span>      | <span data-ttu-id="f68d4-141">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-141">False</span></span>                                                             |
| <span data-ttu-id="f68d4-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f68d4-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f68d4-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f68d4-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f68d4-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f68d4-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f68d4-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-146">Search-Flags</span></span>           | <span data-ttu-id="f68d4-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f68d4-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="f68d4-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-148">System-Flags</span></span>           | <span data-ttu-id="f68d4-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f68d4-149">0x00000010</span></span>                                                        |
| <span data-ttu-id="f68d4-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f68d4-150">Classes used in</span></span>        | [<span data-ttu-id="f68d4-151">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="f68d4-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f68d4-152">亞當</span><span class="sxs-lookup"><span data-stu-id="f68d4-152">ADAM</span></span>



| <span data-ttu-id="f68d4-153">進入</span><span class="sxs-lookup"><span data-stu-id="f68d4-153">Entry</span></span> | <span data-ttu-id="f68d4-154">值</span><span class="sxs-lookup"><span data-stu-id="f68d4-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f68d4-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f68d4-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f68d4-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f68d4-157">System-Only</span></span>            | <span data-ttu-id="f68d4-158">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-158">False</span></span>                                                             |
| <span data-ttu-id="f68d4-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f68d4-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f68d4-160">對</span><span class="sxs-lookup"><span data-stu-id="f68d4-160">True</span></span>                                                              |
| <span data-ttu-id="f68d4-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f68d4-161">Is Indexed</span></span>             | <span data-ttu-id="f68d4-162">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-162">False</span></span>                                                             |
| <span data-ttu-id="f68d4-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f68d4-163">In Global Catalog</span></span>      | <span data-ttu-id="f68d4-164">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-164">False</span></span>                                                             |
| <span data-ttu-id="f68d4-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f68d4-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f68d4-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f68d4-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f68d4-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f68d4-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f68d4-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-169">Search-Flags</span></span>           | <span data-ttu-id="f68d4-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f68d4-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="f68d4-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-171">System-Flags</span></span>           | <span data-ttu-id="f68d4-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f68d4-172">0x00000010</span></span>                                                        |
| <span data-ttu-id="f68d4-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f68d4-173">Classes used in</span></span>        | [<span data-ttu-id="f68d4-174">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="f68d4-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f68d4-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f68d4-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f68d4-176">進入</span><span class="sxs-lookup"><span data-stu-id="f68d4-176">Entry</span></span> | <span data-ttu-id="f68d4-177">值</span><span class="sxs-lookup"><span data-stu-id="f68d4-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f68d4-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f68d4-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f68d4-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f68d4-180">System-Only</span></span>            | <span data-ttu-id="f68d4-181">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-181">False</span></span>                                                             |
| <span data-ttu-id="f68d4-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f68d4-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f68d4-183">對</span><span class="sxs-lookup"><span data-stu-id="f68d4-183">True</span></span>                                                              |
| <span data-ttu-id="f68d4-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f68d4-184">Is Indexed</span></span>             | <span data-ttu-id="f68d4-185">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-185">False</span></span>                                                             |
| <span data-ttu-id="f68d4-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f68d4-186">In Global Catalog</span></span>      | <span data-ttu-id="f68d4-187">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-187">False</span></span>                                                             |
| <span data-ttu-id="f68d4-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f68d4-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f68d4-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f68d4-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f68d4-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f68d4-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f68d4-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-192">Search-Flags</span></span>           | <span data-ttu-id="f68d4-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f68d4-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="f68d4-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-194">System-Flags</span></span>           | <span data-ttu-id="f68d4-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f68d4-195">0x00000010</span></span>                                                        |
| <span data-ttu-id="f68d4-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f68d4-196">Classes used in</span></span>        | [<span data-ttu-id="f68d4-197">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="f68d4-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f68d4-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f68d4-198">Windows Server 2008</span></span>



| <span data-ttu-id="f68d4-199">進入</span><span class="sxs-lookup"><span data-stu-id="f68d4-199">Entry</span></span> | <span data-ttu-id="f68d4-200">值</span><span class="sxs-lookup"><span data-stu-id="f68d4-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f68d4-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f68d4-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f68d4-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f68d4-203">System-Only</span></span>            | <span data-ttu-id="f68d4-204">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-204">False</span></span>                                                             |
| <span data-ttu-id="f68d4-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f68d4-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f68d4-206">對</span><span class="sxs-lookup"><span data-stu-id="f68d4-206">True</span></span>                                                              |
| <span data-ttu-id="f68d4-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f68d4-207">Is Indexed</span></span>             | <span data-ttu-id="f68d4-208">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-208">False</span></span>                                                             |
| <span data-ttu-id="f68d4-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f68d4-209">In Global Catalog</span></span>      | <span data-ttu-id="f68d4-210">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-210">False</span></span>                                                             |
| <span data-ttu-id="f68d4-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f68d4-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f68d4-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f68d4-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f68d4-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f68d4-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f68d4-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-215">Search-Flags</span></span>           | <span data-ttu-id="f68d4-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f68d4-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="f68d4-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-217">System-Flags</span></span>           | <span data-ttu-id="f68d4-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f68d4-218">0x00000010</span></span>                                                        |
| <span data-ttu-id="f68d4-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f68d4-219">Classes used in</span></span>        | [<span data-ttu-id="f68d4-220">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="f68d4-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f68d4-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f68d4-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f68d4-222">進入</span><span class="sxs-lookup"><span data-stu-id="f68d4-222">Entry</span></span> | <span data-ttu-id="f68d4-223">值</span><span class="sxs-lookup"><span data-stu-id="f68d4-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f68d4-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f68d4-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f68d4-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f68d4-226">System-Only</span></span>            | <span data-ttu-id="f68d4-227">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-227">False</span></span>                                                             |
| <span data-ttu-id="f68d4-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f68d4-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f68d4-229">對</span><span class="sxs-lookup"><span data-stu-id="f68d4-229">True</span></span>                                                              |
| <span data-ttu-id="f68d4-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f68d4-230">Is Indexed</span></span>             | <span data-ttu-id="f68d4-231">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-231">False</span></span>                                                             |
| <span data-ttu-id="f68d4-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f68d4-232">In Global Catalog</span></span>      | <span data-ttu-id="f68d4-233">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-233">False</span></span>                                                             |
| <span data-ttu-id="f68d4-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f68d4-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f68d4-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f68d4-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f68d4-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f68d4-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f68d4-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-238">Search-Flags</span></span>           | <span data-ttu-id="f68d4-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f68d4-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="f68d4-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-240">System-Flags</span></span>           | <span data-ttu-id="f68d4-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f68d4-241">0x00000010</span></span>                                                        |
| <span data-ttu-id="f68d4-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f68d4-242">Classes used in</span></span>        | [<span data-ttu-id="f68d4-243">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="f68d4-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f68d4-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f68d4-244">Windows Server 2012</span></span>



| <span data-ttu-id="f68d4-245">進入</span><span class="sxs-lookup"><span data-stu-id="f68d4-245">Entry</span></span> | <span data-ttu-id="f68d4-246">值</span><span class="sxs-lookup"><span data-stu-id="f68d4-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f68d4-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f68d4-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f68d4-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f68d4-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f68d4-249">System-Only</span></span>            | <span data-ttu-id="f68d4-250">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-250">False</span></span>                                                             |
| <span data-ttu-id="f68d4-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f68d4-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f68d4-252">對</span><span class="sxs-lookup"><span data-stu-id="f68d4-252">True</span></span>                                                              |
| <span data-ttu-id="f68d4-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f68d4-253">Is Indexed</span></span>             | <span data-ttu-id="f68d4-254">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-254">False</span></span>                                                             |
| <span data-ttu-id="f68d4-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f68d4-255">In Global Catalog</span></span>      | <span data-ttu-id="f68d4-256">否</span><span class="sxs-lookup"><span data-stu-id="f68d4-256">False</span></span>                                                             |
| <span data-ttu-id="f68d4-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f68d4-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f68d4-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f68d4-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f68d4-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f68d4-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f68d4-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f68d4-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-261">Search-Flags</span></span>           | <span data-ttu-id="f68d4-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f68d4-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="f68d4-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f68d4-263">System-Flags</span></span>           | <span data-ttu-id="f68d4-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f68d4-264">0x00000010</span></span>                                                        |
| <span data-ttu-id="f68d4-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f68d4-265">Classes used in</span></span>        | [<span data-ttu-id="f68d4-266">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="f68d4-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





