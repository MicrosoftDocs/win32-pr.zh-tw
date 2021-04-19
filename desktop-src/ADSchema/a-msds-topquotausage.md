---
title: ms DS-最上層配額-使用方式屬性
description: 目錄資料庫中目前的最高配額使用者清單，依遞減配額使用量排序。
ms.assetid: c52db8c8-233c-495f-b3fe-edbe1d723677
ms.tgt_platform: multiple
keywords:
- ms DS-最上層配額-使用方式屬性 AD 架構
- TopQuotaUsage 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Top-Quota-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db787c0360eff64c726ec680c9fd2a18da1e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973333"
---
# <a name="ms-ds-top-quota-usage-attribute"></a><span data-ttu-id="61ae1-105">ms DS-最上層配額-使用方式屬性</span><span class="sxs-lookup"><span data-stu-id="61ae1-105">ms-DS-Top-Quota-Usage attribute</span></span>

<span data-ttu-id="61ae1-106">目錄資料庫中目前的最高配額使用者清單，依遞減配額使用量排序。</span><span class="sxs-lookup"><span data-stu-id="61ae1-106">The list of top quota users currently in the directory database, ordered by decreasing quota usage.</span></span>



| <span data-ttu-id="61ae1-107">進入</span><span class="sxs-lookup"><span data-stu-id="61ae1-107">Entry</span></span> | <span data-ttu-id="61ae1-108">值</span><span class="sxs-lookup"><span data-stu-id="61ae1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="61ae1-109">CN</span><span class="sxs-lookup"><span data-stu-id="61ae1-109">CN</span></span>                | <span data-ttu-id="61ae1-110">ms-DS-最上層配額-使用量</span><span class="sxs-lookup"><span data-stu-id="61ae1-110">ms-DS-Top-Quota-Usage</span></span>                       |
| <span data-ttu-id="61ae1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="61ae1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="61ae1-112">TopQuotaUsage</span><span class="sxs-lookup"><span data-stu-id="61ae1-112">msDS-TopQuotaUsage</span></span>                          |
| <span data-ttu-id="61ae1-113">大小</span><span class="sxs-lookup"><span data-stu-id="61ae1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="61ae1-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="61ae1-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="61ae1-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="61ae1-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="61ae1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61ae1-116">Attribute-Id</span></span>      | <span data-ttu-id="61ae1-117">1.2.840.113556.1.4.1850</span><span class="sxs-lookup"><span data-stu-id="61ae1-117">1.2.840.113556.1.4.1850</span></span>                     |
| <span data-ttu-id="61ae1-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="61ae1-118">System-Id-Guid</span></span>    | <span data-ttu-id="61ae1-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span><span class="sxs-lookup"><span data-stu-id="61ae1-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span></span>        |
| <span data-ttu-id="61ae1-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="61ae1-120">Syntax</span></span>            | [<span data-ttu-id="61ae1-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="61ae1-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="61ae1-122">實作</span><span class="sxs-lookup"><span data-stu-id="61ae1-122">Implementations</span></span>

-   [<span data-ttu-id="61ae1-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61ae1-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61ae1-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="61ae1-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="61ae1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61ae1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61ae1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61ae1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61ae1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61ae1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61ae1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61ae1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="61ae1-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61ae1-129">Windows Server 2003</span></span>



| <span data-ttu-id="61ae1-130">進入</span><span class="sxs-lookup"><span data-stu-id="61ae1-130">Entry</span></span> | <span data-ttu-id="61ae1-131">值</span><span class="sxs-lookup"><span data-stu-id="61ae1-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="61ae1-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61ae1-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ae1-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ae1-134">System-Only</span></span>            | <span data-ttu-id="61ae1-135">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-135">False</span></span>                                                             |
| <span data-ttu-id="61ae1-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61ae1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="61ae1-137">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-137">False</span></span>                                                             |
| <span data-ttu-id="61ae1-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61ae1-138">Is Indexed</span></span>             | <span data-ttu-id="61ae1-139">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-139">False</span></span>                                                             |
| <span data-ttu-id="61ae1-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61ae1-140">In Global Catalog</span></span>      | <span data-ttu-id="61ae1-141">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-141">False</span></span>                                                             |
| <span data-ttu-id="61ae1-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61ae1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ae1-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61ae1-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="61ae1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ae1-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ae1-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-146">Search-Flags</span></span>           | <span data-ttu-id="61ae1-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ae1-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="61ae1-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-148">System-Flags</span></span>           | <span data-ttu-id="61ae1-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="61ae1-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="61ae1-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61ae1-150">Classes used in</span></span>        | [<span data-ttu-id="61ae1-151">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="61ae1-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="61ae1-152">亞當</span><span class="sxs-lookup"><span data-stu-id="61ae1-152">ADAM</span></span>



| <span data-ttu-id="61ae1-153">進入</span><span class="sxs-lookup"><span data-stu-id="61ae1-153">Entry</span></span> | <span data-ttu-id="61ae1-154">值</span><span class="sxs-lookup"><span data-stu-id="61ae1-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="61ae1-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61ae1-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ae1-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ae1-157">System-Only</span></span>            | <span data-ttu-id="61ae1-158">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-158">False</span></span>                                                             |
| <span data-ttu-id="61ae1-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61ae1-159">Is-Single-Valued</span></span>       | <span data-ttu-id="61ae1-160">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-160">False</span></span>                                                             |
| <span data-ttu-id="61ae1-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61ae1-161">Is Indexed</span></span>             | <span data-ttu-id="61ae1-162">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-162">False</span></span>                                                             |
| <span data-ttu-id="61ae1-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61ae1-163">In Global Catalog</span></span>      | <span data-ttu-id="61ae1-164">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-164">False</span></span>                                                             |
| <span data-ttu-id="61ae1-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61ae1-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ae1-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61ae1-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="61ae1-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ae1-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ae1-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-169">Search-Flags</span></span>           | <span data-ttu-id="61ae1-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ae1-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="61ae1-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-171">System-Flags</span></span>           | <span data-ttu-id="61ae1-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="61ae1-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="61ae1-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61ae1-173">Classes used in</span></span>        | [<span data-ttu-id="61ae1-174">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="61ae1-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61ae1-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61ae1-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61ae1-176">進入</span><span class="sxs-lookup"><span data-stu-id="61ae1-176">Entry</span></span> | <span data-ttu-id="61ae1-177">值</span><span class="sxs-lookup"><span data-stu-id="61ae1-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="61ae1-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61ae1-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ae1-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ae1-180">System-Only</span></span>            | <span data-ttu-id="61ae1-181">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-181">False</span></span>                                                             |
| <span data-ttu-id="61ae1-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61ae1-182">Is-Single-Valued</span></span>       | <span data-ttu-id="61ae1-183">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-183">False</span></span>                                                             |
| <span data-ttu-id="61ae1-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61ae1-184">Is Indexed</span></span>             | <span data-ttu-id="61ae1-185">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-185">False</span></span>                                                             |
| <span data-ttu-id="61ae1-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61ae1-186">In Global Catalog</span></span>      | <span data-ttu-id="61ae1-187">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-187">False</span></span>                                                             |
| <span data-ttu-id="61ae1-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61ae1-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ae1-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61ae1-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="61ae1-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ae1-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ae1-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-192">Search-Flags</span></span>           | <span data-ttu-id="61ae1-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ae1-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="61ae1-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-194">System-Flags</span></span>           | <span data-ttu-id="61ae1-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="61ae1-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="61ae1-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61ae1-196">Classes used in</span></span>        | [<span data-ttu-id="61ae1-197">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="61ae1-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61ae1-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61ae1-198">Windows Server 2008</span></span>



| <span data-ttu-id="61ae1-199">進入</span><span class="sxs-lookup"><span data-stu-id="61ae1-199">Entry</span></span> | <span data-ttu-id="61ae1-200">值</span><span class="sxs-lookup"><span data-stu-id="61ae1-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="61ae1-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61ae1-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ae1-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ae1-203">System-Only</span></span>            | <span data-ttu-id="61ae1-204">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-204">False</span></span>                                                             |
| <span data-ttu-id="61ae1-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61ae1-205">Is-Single-Valued</span></span>       | <span data-ttu-id="61ae1-206">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-206">False</span></span>                                                             |
| <span data-ttu-id="61ae1-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61ae1-207">Is Indexed</span></span>             | <span data-ttu-id="61ae1-208">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-208">False</span></span>                                                             |
| <span data-ttu-id="61ae1-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61ae1-209">In Global Catalog</span></span>      | <span data-ttu-id="61ae1-210">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-210">False</span></span>                                                             |
| <span data-ttu-id="61ae1-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61ae1-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ae1-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61ae1-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="61ae1-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ae1-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ae1-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-215">Search-Flags</span></span>           | <span data-ttu-id="61ae1-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ae1-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="61ae1-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-217">System-Flags</span></span>           | <span data-ttu-id="61ae1-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="61ae1-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="61ae1-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61ae1-219">Classes used in</span></span>        | [<span data-ttu-id="61ae1-220">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="61ae1-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61ae1-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61ae1-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61ae1-222">進入</span><span class="sxs-lookup"><span data-stu-id="61ae1-222">Entry</span></span> | <span data-ttu-id="61ae1-223">值</span><span class="sxs-lookup"><span data-stu-id="61ae1-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="61ae1-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61ae1-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ae1-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ae1-226">System-Only</span></span>            | <span data-ttu-id="61ae1-227">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-227">False</span></span>                                                             |
| <span data-ttu-id="61ae1-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61ae1-228">Is-Single-Valued</span></span>       | <span data-ttu-id="61ae1-229">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-229">False</span></span>                                                             |
| <span data-ttu-id="61ae1-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61ae1-230">Is Indexed</span></span>             | <span data-ttu-id="61ae1-231">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-231">False</span></span>                                                             |
| <span data-ttu-id="61ae1-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61ae1-232">In Global Catalog</span></span>      | <span data-ttu-id="61ae1-233">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-233">False</span></span>                                                             |
| <span data-ttu-id="61ae1-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61ae1-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ae1-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61ae1-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="61ae1-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ae1-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ae1-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-238">Search-Flags</span></span>           | <span data-ttu-id="61ae1-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ae1-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="61ae1-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-240">System-Flags</span></span>           | <span data-ttu-id="61ae1-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="61ae1-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="61ae1-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61ae1-242">Classes used in</span></span>        | [<span data-ttu-id="61ae1-243">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="61ae1-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61ae1-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61ae1-244">Windows Server 2012</span></span>



| <span data-ttu-id="61ae1-245">進入</span><span class="sxs-lookup"><span data-stu-id="61ae1-245">Entry</span></span> | <span data-ttu-id="61ae1-246">值</span><span class="sxs-lookup"><span data-stu-id="61ae1-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="61ae1-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61ae1-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ae1-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="61ae1-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ae1-249">System-Only</span></span>            | <span data-ttu-id="61ae1-250">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-250">False</span></span>                                                             |
| <span data-ttu-id="61ae1-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61ae1-251">Is-Single-Valued</span></span>       | <span data-ttu-id="61ae1-252">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-252">False</span></span>                                                             |
| <span data-ttu-id="61ae1-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61ae1-253">Is Indexed</span></span>             | <span data-ttu-id="61ae1-254">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-254">False</span></span>                                                             |
| <span data-ttu-id="61ae1-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61ae1-255">In Global Catalog</span></span>      | <span data-ttu-id="61ae1-256">否</span><span class="sxs-lookup"><span data-stu-id="61ae1-256">False</span></span>                                                             |
| <span data-ttu-id="61ae1-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61ae1-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ae1-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61ae1-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="61ae1-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ae1-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ae1-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="61ae1-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-261">Search-Flags</span></span>           | <span data-ttu-id="61ae1-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ae1-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="61ae1-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ae1-263">System-Flags</span></span>           | <span data-ttu-id="61ae1-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="61ae1-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="61ae1-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61ae1-265">Classes used in</span></span>        | [<span data-ttu-id="61ae1-266">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="61ae1-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





