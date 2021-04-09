---
title: ms-chap-Az-Domain-Timeout 屬性
description: 偵測到無法連線到網域之後，以及重新嘗試 DC 之前的時間（以毫秒為單位）。
ms.assetid: b2523faa-7cf1-4325-a3fa-70c5f568adaa
ms.tgt_platform: multiple
keywords:
- ms DS-Az-Domain-Timeout 屬性 AD 架構
- AzDomainTimeout 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-Domain-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce6f457977de1124438fa4b54e4a84d1cb6d54e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845176"
---
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="48744-105">ms-chap-Az-Domain-Timeout 屬性</span><span class="sxs-lookup"><span data-stu-id="48744-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="48744-106">偵測到無法連線到網域之後，以及重新嘗試 DC 之前的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="48744-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="48744-107">進入</span><span class="sxs-lookup"><span data-stu-id="48744-107">Entry</span></span> | <span data-ttu-id="48744-108">值</span><span class="sxs-lookup"><span data-stu-id="48744-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="48744-109">CN</span><span class="sxs-lookup"><span data-stu-id="48744-109">CN</span></span>                | <span data-ttu-id="48744-110">ms-chap-Az-Domain-Timeout</span><span class="sxs-lookup"><span data-stu-id="48744-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="48744-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="48744-111">Ldap-Display-Name</span></span> | <span data-ttu-id="48744-112">AzDomainTimeout</span><span class="sxs-lookup"><span data-stu-id="48744-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="48744-113">大小</span><span class="sxs-lookup"><span data-stu-id="48744-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="48744-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="48744-114">Update Privilege</span></span>  | <span data-ttu-id="48744-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="48744-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="48744-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="48744-116">Update Frequency</span></span>  | <span data-ttu-id="48744-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="48744-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="48744-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="48744-118">Attribute-Id</span></span>      | <span data-ttu-id="48744-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="48744-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="48744-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="48744-120">System-Id-Guid</span></span>    | <span data-ttu-id="48744-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="48744-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="48744-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="48744-122">Syntax</span></span>            | [<span data-ttu-id="48744-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="48744-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="48744-124">實作</span><span class="sxs-lookup"><span data-stu-id="48744-124">Implementations</span></span>

-   [<span data-ttu-id="48744-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="48744-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="48744-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="48744-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="48744-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="48744-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="48744-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48744-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="48744-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="48744-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="48744-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48744-130">Windows Server 2003</span></span>



| <span data-ttu-id="48744-131">進入</span><span class="sxs-lookup"><span data-stu-id="48744-131">Entry</span></span> | <span data-ttu-id="48744-132">值</span><span class="sxs-lookup"><span data-stu-id="48744-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="48744-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48744-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48744-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="48744-135">System-Only</span></span>            | <span data-ttu-id="48744-136">否</span><span class="sxs-lookup"><span data-stu-id="48744-136">False</span></span>                                                              |
| <span data-ttu-id="48744-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48744-137">Is-Single-Valued</span></span>       | <span data-ttu-id="48744-138">對</span><span class="sxs-lookup"><span data-stu-id="48744-138">True</span></span>                                                               |
| <span data-ttu-id="48744-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48744-139">Is Indexed</span></span>             | <span data-ttu-id="48744-140">否</span><span class="sxs-lookup"><span data-stu-id="48744-140">False</span></span>                                                              |
| <span data-ttu-id="48744-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48744-141">In Global Catalog</span></span>      | <span data-ttu-id="48744-142">否</span><span class="sxs-lookup"><span data-stu-id="48744-142">False</span></span>                                                              |
| <span data-ttu-id="48744-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48744-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="48744-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48744-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="48744-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48744-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48744-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-147">Search-Flags</span></span>           | <span data-ttu-id="48744-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48744-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="48744-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-149">System-Flags</span></span>           | <span data-ttu-id="48744-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48744-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="48744-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48744-151">Classes used in</span></span>        | [<span data-ttu-id="48744-152">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="48744-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="48744-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="48744-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="48744-154">進入</span><span class="sxs-lookup"><span data-stu-id="48744-154">Entry</span></span> | <span data-ttu-id="48744-155">值</span><span class="sxs-lookup"><span data-stu-id="48744-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="48744-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48744-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48744-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="48744-158">System-Only</span></span>            | <span data-ttu-id="48744-159">否</span><span class="sxs-lookup"><span data-stu-id="48744-159">False</span></span>                                                              |
| <span data-ttu-id="48744-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48744-160">Is-Single-Valued</span></span>       | <span data-ttu-id="48744-161">對</span><span class="sxs-lookup"><span data-stu-id="48744-161">True</span></span>                                                               |
| <span data-ttu-id="48744-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48744-162">Is Indexed</span></span>             | <span data-ttu-id="48744-163">否</span><span class="sxs-lookup"><span data-stu-id="48744-163">False</span></span>                                                              |
| <span data-ttu-id="48744-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48744-164">In Global Catalog</span></span>      | <span data-ttu-id="48744-165">否</span><span class="sxs-lookup"><span data-stu-id="48744-165">False</span></span>                                                              |
| <span data-ttu-id="48744-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48744-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="48744-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48744-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="48744-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48744-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48744-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-170">Search-Flags</span></span>           | <span data-ttu-id="48744-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48744-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="48744-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-172">System-Flags</span></span>           | <span data-ttu-id="48744-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48744-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="48744-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48744-174">Classes used in</span></span>        | [<span data-ttu-id="48744-175">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="48744-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="48744-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48744-176">Windows Server 2008</span></span>



| <span data-ttu-id="48744-177">進入</span><span class="sxs-lookup"><span data-stu-id="48744-177">Entry</span></span> | <span data-ttu-id="48744-178">值</span><span class="sxs-lookup"><span data-stu-id="48744-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="48744-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48744-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48744-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="48744-181">System-Only</span></span>            | <span data-ttu-id="48744-182">否</span><span class="sxs-lookup"><span data-stu-id="48744-182">False</span></span>                                                              |
| <span data-ttu-id="48744-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48744-183">Is-Single-Valued</span></span>       | <span data-ttu-id="48744-184">對</span><span class="sxs-lookup"><span data-stu-id="48744-184">True</span></span>                                                               |
| <span data-ttu-id="48744-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48744-185">Is Indexed</span></span>             | <span data-ttu-id="48744-186">否</span><span class="sxs-lookup"><span data-stu-id="48744-186">False</span></span>                                                              |
| <span data-ttu-id="48744-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48744-187">In Global Catalog</span></span>      | <span data-ttu-id="48744-188">否</span><span class="sxs-lookup"><span data-stu-id="48744-188">False</span></span>                                                              |
| <span data-ttu-id="48744-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48744-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="48744-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48744-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="48744-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48744-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48744-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-193">Search-Flags</span></span>           | <span data-ttu-id="48744-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48744-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="48744-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-195">System-Flags</span></span>           | <span data-ttu-id="48744-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48744-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="48744-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48744-197">Classes used in</span></span>        | [<span data-ttu-id="48744-198">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="48744-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="48744-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48744-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="48744-200">進入</span><span class="sxs-lookup"><span data-stu-id="48744-200">Entry</span></span> | <span data-ttu-id="48744-201">值</span><span class="sxs-lookup"><span data-stu-id="48744-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="48744-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48744-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48744-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="48744-204">System-Only</span></span>            | <span data-ttu-id="48744-205">否</span><span class="sxs-lookup"><span data-stu-id="48744-205">False</span></span>                                                              |
| <span data-ttu-id="48744-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48744-206">Is-Single-Valued</span></span>       | <span data-ttu-id="48744-207">對</span><span class="sxs-lookup"><span data-stu-id="48744-207">True</span></span>                                                               |
| <span data-ttu-id="48744-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48744-208">Is Indexed</span></span>             | <span data-ttu-id="48744-209">否</span><span class="sxs-lookup"><span data-stu-id="48744-209">False</span></span>                                                              |
| <span data-ttu-id="48744-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48744-210">In Global Catalog</span></span>      | <span data-ttu-id="48744-211">否</span><span class="sxs-lookup"><span data-stu-id="48744-211">False</span></span>                                                              |
| <span data-ttu-id="48744-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48744-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="48744-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48744-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="48744-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48744-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48744-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-216">Search-Flags</span></span>           | <span data-ttu-id="48744-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48744-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="48744-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-218">System-Flags</span></span>           | <span data-ttu-id="48744-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48744-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="48744-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48744-220">Classes used in</span></span>        | [<span data-ttu-id="48744-221">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="48744-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="48744-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48744-222">Windows Server 2012</span></span>



| <span data-ttu-id="48744-223">進入</span><span class="sxs-lookup"><span data-stu-id="48744-223">Entry</span></span> | <span data-ttu-id="48744-224">值</span><span class="sxs-lookup"><span data-stu-id="48744-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="48744-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="48744-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="48744-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="48744-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="48744-227">System-Only</span></span>            | <span data-ttu-id="48744-228">否</span><span class="sxs-lookup"><span data-stu-id="48744-228">False</span></span>                                                              |
| <span data-ttu-id="48744-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="48744-229">Is-Single-Valued</span></span>       | <span data-ttu-id="48744-230">對</span><span class="sxs-lookup"><span data-stu-id="48744-230">True</span></span>                                                               |
| <span data-ttu-id="48744-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="48744-231">Is Indexed</span></span>             | <span data-ttu-id="48744-232">否</span><span class="sxs-lookup"><span data-stu-id="48744-232">False</span></span>                                                              |
| <span data-ttu-id="48744-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="48744-233">In Global Catalog</span></span>      | <span data-ttu-id="48744-234">否</span><span class="sxs-lookup"><span data-stu-id="48744-234">False</span></span>                                                              |
| <span data-ttu-id="48744-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="48744-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="48744-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="48744-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="48744-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="48744-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="48744-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="48744-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-239">Search-Flags</span></span>           | <span data-ttu-id="48744-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="48744-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="48744-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="48744-241">System-Flags</span></span>           | <span data-ttu-id="48744-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="48744-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="48744-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="48744-243">Classes used in</span></span>        | [<span data-ttu-id="48744-244">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="48744-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





