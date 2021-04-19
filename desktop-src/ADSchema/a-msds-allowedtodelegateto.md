---
title: ms DS-允許委派至屬性
description: 這是服務帳戶 (電腦或使用者帳戶) 物件的屬性。
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- ms DS-允許委派至屬性 AD 架構
- AllowedToDelegateTo 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973920"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a><span data-ttu-id="fdfcd-105">ms DS-允許委派至屬性</span><span class="sxs-lookup"><span data-stu-id="fdfcd-105">ms-DS-Allowed-To-Delegate-To attribute</span></span>

<span data-ttu-id="fdfcd-106">這是服務帳戶 (電腦或使用者帳戶) 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="fdfcd-106">This is an attribute on service account (computer or user account) objects.</span></span> <span data-ttu-id="fdfcd-107">它包含)  (Spn 的服務主體名稱清單。</span><span class="sxs-lookup"><span data-stu-id="fdfcd-107">It contains a list of Service Principal Names (SPNs).</span></span> <span data-ttu-id="fdfcd-108">這個屬性是用來設定服務，讓它可以取得可用於限制委派的服務票證。</span><span class="sxs-lookup"><span data-stu-id="fdfcd-108">This attribute is used to configure a service so that it can obtain service tickets that can be used for Constrained Delegation.</span></span>



| <span data-ttu-id="fdfcd-109">進入</span><span class="sxs-lookup"><span data-stu-id="fdfcd-109">Entry</span></span> | <span data-ttu-id="fdfcd-110">值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fdfcd-111">CN</span><span class="sxs-lookup"><span data-stu-id="fdfcd-111">CN</span></span>                | <span data-ttu-id="fdfcd-112">允許對委派的 ms DS</span><span class="sxs-lookup"><span data-stu-id="fdfcd-112">ms-DS-Allowed-To-Delegate-To</span></span>                |
| <span data-ttu-id="fdfcd-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fdfcd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fdfcd-114">AllowedToDelegateTo</span><span class="sxs-lookup"><span data-stu-id="fdfcd-114">msDS-AllowedToDelegateTo</span></span>                    |
| <span data-ttu-id="fdfcd-115">大小</span><span class="sxs-lookup"><span data-stu-id="fdfcd-115">Size</span></span>              | <span data-ttu-id="fdfcd-116">0到64K</span><span class="sxs-lookup"><span data-stu-id="fdfcd-116">0 to 64K</span></span>                                    |
| <span data-ttu-id="fdfcd-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fdfcd-117">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="fdfcd-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fdfcd-118">Update Frequency</span></span>  | <span data-ttu-id="fdfcd-119">很少</span><span class="sxs-lookup"><span data-stu-id="fdfcd-119">Infrequently</span></span>                                |
| <span data-ttu-id="fdfcd-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fdfcd-120">Attribute-Id</span></span>      | <span data-ttu-id="fdfcd-121">1.2.840.113556.1.4.1787</span><span class="sxs-lookup"><span data-stu-id="fdfcd-121">1.2.840.113556.1.4.1787</span></span>                     |
| <span data-ttu-id="fdfcd-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fdfcd-122">System-Id-Guid</span></span>    | <span data-ttu-id="fdfcd-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span><span class="sxs-lookup"><span data-stu-id="fdfcd-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span></span>        |
| <span data-ttu-id="fdfcd-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdfcd-124">Syntax</span></span>            | [<span data-ttu-id="fdfcd-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fdfcd-126">實作</span><span class="sxs-lookup"><span data-stu-id="fdfcd-126">Implementations</span></span>

-   [<span data-ttu-id="fdfcd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fdfcd-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fdfcd-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fdfcd-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fdfcd-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fdfcd-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fdfcd-132">Windows Server 2003</span></span>



| <span data-ttu-id="fdfcd-133">進入</span><span class="sxs-lookup"><span data-stu-id="fdfcd-133">Entry</span></span> | <span data-ttu-id="fdfcd-134">值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="fdfcd-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fdfcd-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfcd-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfcd-137">System-Only</span></span>            | <span data-ttu-id="fdfcd-138">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-138">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-139">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfcd-140">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-140">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fdfcd-141">Is Indexed</span></span>             | <span data-ttu-id="fdfcd-142">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-142">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fdfcd-143">In Global Catalog</span></span>      | <span data-ttu-id="fdfcd-144">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-144">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fdfcd-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfcd-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fdfcd-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="fdfcd-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfcd-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfcd-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-149">Search-Flags</span></span>           | <span data-ttu-id="fdfcd-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfcd-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="fdfcd-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-151">System-Flags</span></span>           | <span data-ttu-id="fdfcd-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfcd-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="fdfcd-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fdfcd-153">Classes used in</span></span>        | [<span data-ttu-id="fdfcd-154">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fdfcd-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fdfcd-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fdfcd-156">進入</span><span class="sxs-lookup"><span data-stu-id="fdfcd-156">Entry</span></span> | <span data-ttu-id="fdfcd-157">值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="fdfcd-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fdfcd-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfcd-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfcd-160">System-Only</span></span>            | <span data-ttu-id="fdfcd-161">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-161">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfcd-163">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-163">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fdfcd-164">Is Indexed</span></span>             | <span data-ttu-id="fdfcd-165">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-165">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fdfcd-166">In Global Catalog</span></span>      | <span data-ttu-id="fdfcd-167">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-167">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fdfcd-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfcd-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fdfcd-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="fdfcd-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfcd-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfcd-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-172">Search-Flags</span></span>           | <span data-ttu-id="fdfcd-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfcd-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="fdfcd-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-174">System-Flags</span></span>           | <span data-ttu-id="fdfcd-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfcd-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="fdfcd-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fdfcd-176">Classes used in</span></span>        | [<span data-ttu-id="fdfcd-177">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-177">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fdfcd-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdfcd-178">Windows Server 2008</span></span>



| <span data-ttu-id="fdfcd-179">進入</span><span class="sxs-lookup"><span data-stu-id="fdfcd-179">Entry</span></span> | <span data-ttu-id="fdfcd-180">值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="fdfcd-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fdfcd-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfcd-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfcd-183">System-Only</span></span>            | <span data-ttu-id="fdfcd-184">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-184">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfcd-186">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-186">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fdfcd-187">Is Indexed</span></span>             | <span data-ttu-id="fdfcd-188">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-188">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fdfcd-189">In Global Catalog</span></span>      | <span data-ttu-id="fdfcd-190">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-190">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fdfcd-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfcd-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fdfcd-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="fdfcd-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfcd-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfcd-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-195">Search-Flags</span></span>           | <span data-ttu-id="fdfcd-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfcd-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="fdfcd-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-197">System-Flags</span></span>           | <span data-ttu-id="fdfcd-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfcd-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="fdfcd-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fdfcd-199">Classes used in</span></span>        | [<span data-ttu-id="fdfcd-200">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-200">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fdfcd-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fdfcd-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fdfcd-202">進入</span><span class="sxs-lookup"><span data-stu-id="fdfcd-202">Entry</span></span> | <span data-ttu-id="fdfcd-203">值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="fdfcd-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fdfcd-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfcd-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfcd-206">System-Only</span></span>            | <span data-ttu-id="fdfcd-207">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-207">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfcd-209">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-209">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fdfcd-210">Is Indexed</span></span>             | <span data-ttu-id="fdfcd-211">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-211">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fdfcd-212">In Global Catalog</span></span>      | <span data-ttu-id="fdfcd-213">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-213">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fdfcd-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfcd-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fdfcd-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="fdfcd-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfcd-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfcd-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-218">Search-Flags</span></span>           | <span data-ttu-id="fdfcd-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfcd-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="fdfcd-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-220">System-Flags</span></span>           | <span data-ttu-id="fdfcd-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfcd-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="fdfcd-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fdfcd-222">Classes used in</span></span>        | [<span data-ttu-id="fdfcd-223">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-223">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fdfcd-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdfcd-224">Windows Server 2012</span></span>



| <span data-ttu-id="fdfcd-225">進入</span><span class="sxs-lookup"><span data-stu-id="fdfcd-225">Entry</span></span> | <span data-ttu-id="fdfcd-226">值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="fdfcd-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fdfcd-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdfcd-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="fdfcd-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdfcd-229">System-Only</span></span>            | <span data-ttu-id="fdfcd-230">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-230">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fdfcd-231">Is-Single-Valued</span></span>       | <span data-ttu-id="fdfcd-232">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-232">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fdfcd-233">Is Indexed</span></span>             | <span data-ttu-id="fdfcd-234">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-234">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fdfcd-235">In Global Catalog</span></span>      | <span data-ttu-id="fdfcd-236">否</span><span class="sxs-lookup"><span data-stu-id="fdfcd-236">False</span></span>                                                              |
| <span data-ttu-id="fdfcd-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fdfcd-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdfcd-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fdfcd-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="fdfcd-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdfcd-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdfcd-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="fdfcd-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-241">Search-Flags</span></span>           | <span data-ttu-id="fdfcd-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdfcd-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="fdfcd-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdfcd-243">System-Flags</span></span>           | <span data-ttu-id="fdfcd-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdfcd-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="fdfcd-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fdfcd-245">Classes used in</span></span>        | [<span data-ttu-id="fdfcd-246">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="fdfcd-246">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





