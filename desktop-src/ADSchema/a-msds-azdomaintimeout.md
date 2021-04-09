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
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="0fd76-105">ms-chap-Az-Domain-Timeout 屬性</span><span class="sxs-lookup"><span data-stu-id="0fd76-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="0fd76-106">偵測到無法連線到網域之後，以及重新嘗試 DC 之前的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0fd76-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="0fd76-107">進入</span><span class="sxs-lookup"><span data-stu-id="0fd76-107">Entry</span></span> | <span data-ttu-id="0fd76-108">值</span><span class="sxs-lookup"><span data-stu-id="0fd76-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0fd76-109">CN</span><span class="sxs-lookup"><span data-stu-id="0fd76-109">CN</span></span>                | <span data-ttu-id="0fd76-110">ms-chap-Az-Domain-Timeout</span><span class="sxs-lookup"><span data-stu-id="0fd76-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="0fd76-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0fd76-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0fd76-112">AzDomainTimeout</span><span class="sxs-lookup"><span data-stu-id="0fd76-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="0fd76-113">大小</span><span class="sxs-lookup"><span data-stu-id="0fd76-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="0fd76-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0fd76-114">Update Privilege</span></span>  | <span data-ttu-id="0fd76-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="0fd76-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="0fd76-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0fd76-116">Update Frequency</span></span>  | <span data-ttu-id="0fd76-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="0fd76-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="0fd76-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0fd76-118">Attribute-Id</span></span>      | <span data-ttu-id="0fd76-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="0fd76-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="0fd76-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0fd76-120">System-Id-Guid</span></span>    | <span data-ttu-id="0fd76-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="0fd76-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="0fd76-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd76-122">Syntax</span></span>            | [<span data-ttu-id="0fd76-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="0fd76-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="0fd76-124">實作</span><span class="sxs-lookup"><span data-stu-id="0fd76-124">Implementations</span></span>

-   [<span data-ttu-id="0fd76-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0fd76-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0fd76-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0fd76-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0fd76-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0fd76-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0fd76-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0fd76-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0fd76-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0fd76-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0fd76-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0fd76-130">Windows Server 2003</span></span>



| <span data-ttu-id="0fd76-131">進入</span><span class="sxs-lookup"><span data-stu-id="0fd76-131">Entry</span></span> | <span data-ttu-id="0fd76-132">值</span><span class="sxs-lookup"><span data-stu-id="0fd76-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0fd76-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0fd76-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fd76-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fd76-135">System-Only</span></span>            | <span data-ttu-id="0fd76-136">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-136">False</span></span>                                                              |
| <span data-ttu-id="0fd76-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0fd76-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0fd76-138">對</span><span class="sxs-lookup"><span data-stu-id="0fd76-138">True</span></span>                                                               |
| <span data-ttu-id="0fd76-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0fd76-139">Is Indexed</span></span>             | <span data-ttu-id="0fd76-140">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-140">False</span></span>                                                              |
| <span data-ttu-id="0fd76-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0fd76-141">In Global Catalog</span></span>      | <span data-ttu-id="0fd76-142">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-142">False</span></span>                                                              |
| <span data-ttu-id="0fd76-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0fd76-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fd76-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0fd76-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0fd76-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fd76-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fd76-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-147">Search-Flags</span></span>           | <span data-ttu-id="0fd76-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0fd76-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="0fd76-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-149">System-Flags</span></span>           | <span data-ttu-id="0fd76-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fd76-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="0fd76-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0fd76-151">Classes used in</span></span>        | [<span data-ttu-id="0fd76-152">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="0fd76-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0fd76-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0fd76-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0fd76-154">進入</span><span class="sxs-lookup"><span data-stu-id="0fd76-154">Entry</span></span> | <span data-ttu-id="0fd76-155">值</span><span class="sxs-lookup"><span data-stu-id="0fd76-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0fd76-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0fd76-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fd76-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fd76-158">System-Only</span></span>            | <span data-ttu-id="0fd76-159">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-159">False</span></span>                                                              |
| <span data-ttu-id="0fd76-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0fd76-160">Is-Single-Valued</span></span>       | <span data-ttu-id="0fd76-161">對</span><span class="sxs-lookup"><span data-stu-id="0fd76-161">True</span></span>                                                               |
| <span data-ttu-id="0fd76-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0fd76-162">Is Indexed</span></span>             | <span data-ttu-id="0fd76-163">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-163">False</span></span>                                                              |
| <span data-ttu-id="0fd76-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0fd76-164">In Global Catalog</span></span>      | <span data-ttu-id="0fd76-165">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-165">False</span></span>                                                              |
| <span data-ttu-id="0fd76-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0fd76-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fd76-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0fd76-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0fd76-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fd76-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fd76-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-170">Search-Flags</span></span>           | <span data-ttu-id="0fd76-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0fd76-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="0fd76-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-172">System-Flags</span></span>           | <span data-ttu-id="0fd76-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fd76-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="0fd76-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0fd76-174">Classes used in</span></span>        | [<span data-ttu-id="0fd76-175">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="0fd76-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0fd76-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fd76-176">Windows Server 2008</span></span>



| <span data-ttu-id="0fd76-177">進入</span><span class="sxs-lookup"><span data-stu-id="0fd76-177">Entry</span></span> | <span data-ttu-id="0fd76-178">值</span><span class="sxs-lookup"><span data-stu-id="0fd76-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0fd76-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0fd76-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fd76-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fd76-181">System-Only</span></span>            | <span data-ttu-id="0fd76-182">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-182">False</span></span>                                                              |
| <span data-ttu-id="0fd76-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0fd76-183">Is-Single-Valued</span></span>       | <span data-ttu-id="0fd76-184">對</span><span class="sxs-lookup"><span data-stu-id="0fd76-184">True</span></span>                                                               |
| <span data-ttu-id="0fd76-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0fd76-185">Is Indexed</span></span>             | <span data-ttu-id="0fd76-186">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-186">False</span></span>                                                              |
| <span data-ttu-id="0fd76-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0fd76-187">In Global Catalog</span></span>      | <span data-ttu-id="0fd76-188">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-188">False</span></span>                                                              |
| <span data-ttu-id="0fd76-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0fd76-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fd76-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0fd76-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0fd76-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fd76-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fd76-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-193">Search-Flags</span></span>           | <span data-ttu-id="0fd76-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0fd76-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="0fd76-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-195">System-Flags</span></span>           | <span data-ttu-id="0fd76-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fd76-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="0fd76-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0fd76-197">Classes used in</span></span>        | [<span data-ttu-id="0fd76-198">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="0fd76-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0fd76-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0fd76-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0fd76-200">進入</span><span class="sxs-lookup"><span data-stu-id="0fd76-200">Entry</span></span> | <span data-ttu-id="0fd76-201">值</span><span class="sxs-lookup"><span data-stu-id="0fd76-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0fd76-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0fd76-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fd76-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fd76-204">System-Only</span></span>            | <span data-ttu-id="0fd76-205">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-205">False</span></span>                                                              |
| <span data-ttu-id="0fd76-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0fd76-206">Is-Single-Valued</span></span>       | <span data-ttu-id="0fd76-207">對</span><span class="sxs-lookup"><span data-stu-id="0fd76-207">True</span></span>                                                               |
| <span data-ttu-id="0fd76-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0fd76-208">Is Indexed</span></span>             | <span data-ttu-id="0fd76-209">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-209">False</span></span>                                                              |
| <span data-ttu-id="0fd76-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0fd76-210">In Global Catalog</span></span>      | <span data-ttu-id="0fd76-211">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-211">False</span></span>                                                              |
| <span data-ttu-id="0fd76-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0fd76-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fd76-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0fd76-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0fd76-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fd76-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fd76-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-216">Search-Flags</span></span>           | <span data-ttu-id="0fd76-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0fd76-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="0fd76-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-218">System-Flags</span></span>           | <span data-ttu-id="0fd76-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fd76-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="0fd76-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0fd76-220">Classes used in</span></span>        | [<span data-ttu-id="0fd76-221">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="0fd76-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0fd76-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0fd76-222">Windows Server 2012</span></span>



| <span data-ttu-id="0fd76-223">進入</span><span class="sxs-lookup"><span data-stu-id="0fd76-223">Entry</span></span> | <span data-ttu-id="0fd76-224">值</span><span class="sxs-lookup"><span data-stu-id="0fd76-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0fd76-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0fd76-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0fd76-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0fd76-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="0fd76-227">System-Only</span></span>            | <span data-ttu-id="0fd76-228">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-228">False</span></span>                                                              |
| <span data-ttu-id="0fd76-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0fd76-229">Is-Single-Valued</span></span>       | <span data-ttu-id="0fd76-230">對</span><span class="sxs-lookup"><span data-stu-id="0fd76-230">True</span></span>                                                               |
| <span data-ttu-id="0fd76-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0fd76-231">Is Indexed</span></span>             | <span data-ttu-id="0fd76-232">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-232">False</span></span>                                                              |
| <span data-ttu-id="0fd76-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0fd76-233">In Global Catalog</span></span>      | <span data-ttu-id="0fd76-234">否</span><span class="sxs-lookup"><span data-stu-id="0fd76-234">False</span></span>                                                              |
| <span data-ttu-id="0fd76-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0fd76-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="0fd76-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0fd76-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0fd76-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0fd76-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0fd76-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0fd76-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-239">Search-Flags</span></span>           | <span data-ttu-id="0fd76-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0fd76-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="0fd76-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0fd76-241">System-Flags</span></span>           | <span data-ttu-id="0fd76-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0fd76-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="0fd76-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0fd76-243">Classes used in</span></span>        | [<span data-ttu-id="0fd76-244">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="0fd76-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





