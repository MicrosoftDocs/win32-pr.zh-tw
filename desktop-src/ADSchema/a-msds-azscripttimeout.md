---
title: ms DS-Az-Script-Timeout 屬性
description: 等候腳本完成審核特定原則的最長時間（以毫秒為單位）。
ms.assetid: 166d87a3-8768-42d9-9041-21f272059fbf
ms.tgt_platform: multiple
keywords:
- ms DS-Az-Script-Timeout 屬性 AD 架構
- AzScriptTimeout 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-Script-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67de4230c3f4710a3eefe6edab896d4fcadcb91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385461"
---
# <a name="ms-ds-az-script-timeout-attribute"></a><span data-ttu-id="98125-105">ms DS-Az-Script-Timeout 屬性</span><span class="sxs-lookup"><span data-stu-id="98125-105">ms-DS-Az-Script-Timeout attribute</span></span>

<span data-ttu-id="98125-106">等候腳本完成審核特定原則的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="98125-106">The maximum time, in milliseconds, to wait for a script to finish auditing a specific policy.</span></span>



| <span data-ttu-id="98125-107">進入</span><span class="sxs-lookup"><span data-stu-id="98125-107">Entry</span></span> | <span data-ttu-id="98125-108">值</span><span class="sxs-lookup"><span data-stu-id="98125-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="98125-109">CN</span><span class="sxs-lookup"><span data-stu-id="98125-109">CN</span></span>                | <span data-ttu-id="98125-110">ms DS-Az-Script-Timeout</span><span class="sxs-lookup"><span data-stu-id="98125-110">ms-DS-Az-Script-Timeout</span></span>                 |
| <span data-ttu-id="98125-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="98125-111">Ldap-Display-Name</span></span> | <span data-ttu-id="98125-112">AzScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="98125-112">msDS-AzScriptTimeout</span></span>                    |
| <span data-ttu-id="98125-113">大小</span><span class="sxs-lookup"><span data-stu-id="98125-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="98125-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="98125-114">Update Privilege</span></span>  | <span data-ttu-id="98125-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="98125-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="98125-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="98125-116">Update Frequency</span></span>  | <span data-ttu-id="98125-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="98125-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="98125-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="98125-118">Attribute-Id</span></span>      | <span data-ttu-id="98125-119">1.2.840.113556.1.4.1797</span><span class="sxs-lookup"><span data-stu-id="98125-119">1.2.840.113556.1.4.1797</span></span>                 |
| <span data-ttu-id="98125-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="98125-120">System-Id-Guid</span></span>    | <span data-ttu-id="98125-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span><span class="sxs-lookup"><span data-stu-id="98125-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span></span>    |
| <span data-ttu-id="98125-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="98125-122">Syntax</span></span>            | [<span data-ttu-id="98125-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="98125-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="98125-124">實作</span><span class="sxs-lookup"><span data-stu-id="98125-124">Implementations</span></span>

-   [<span data-ttu-id="98125-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="98125-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="98125-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="98125-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="98125-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="98125-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="98125-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="98125-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="98125-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="98125-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="98125-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="98125-130">Windows Server 2003</span></span>



| <span data-ttu-id="98125-131">進入</span><span class="sxs-lookup"><span data-stu-id="98125-131">Entry</span></span> | <span data-ttu-id="98125-132">值</span><span class="sxs-lookup"><span data-stu-id="98125-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="98125-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98125-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98125-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="98125-135">System-Only</span></span>            | <span data-ttu-id="98125-136">否</span><span class="sxs-lookup"><span data-stu-id="98125-136">False</span></span>                                                              |
| <span data-ttu-id="98125-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98125-137">Is-Single-Valued</span></span>       | <span data-ttu-id="98125-138">對</span><span class="sxs-lookup"><span data-stu-id="98125-138">True</span></span>                                                               |
| <span data-ttu-id="98125-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98125-139">Is Indexed</span></span>             | <span data-ttu-id="98125-140">否</span><span class="sxs-lookup"><span data-stu-id="98125-140">False</span></span>                                                              |
| <span data-ttu-id="98125-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98125-141">In Global Catalog</span></span>      | <span data-ttu-id="98125-142">否</span><span class="sxs-lookup"><span data-stu-id="98125-142">False</span></span>                                                              |
| <span data-ttu-id="98125-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98125-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="98125-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98125-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="98125-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98125-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98125-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-147">Search-Flags</span></span>           | <span data-ttu-id="98125-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98125-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="98125-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-149">System-Flags</span></span>           | <span data-ttu-id="98125-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98125-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="98125-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98125-151">Classes used in</span></span>        | [<span data-ttu-id="98125-152">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="98125-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="98125-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="98125-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="98125-154">進入</span><span class="sxs-lookup"><span data-stu-id="98125-154">Entry</span></span> | <span data-ttu-id="98125-155">值</span><span class="sxs-lookup"><span data-stu-id="98125-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="98125-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98125-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98125-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="98125-158">System-Only</span></span>            | <span data-ttu-id="98125-159">否</span><span class="sxs-lookup"><span data-stu-id="98125-159">False</span></span>                                                              |
| <span data-ttu-id="98125-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98125-160">Is-Single-Valued</span></span>       | <span data-ttu-id="98125-161">對</span><span class="sxs-lookup"><span data-stu-id="98125-161">True</span></span>                                                               |
| <span data-ttu-id="98125-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98125-162">Is Indexed</span></span>             | <span data-ttu-id="98125-163">否</span><span class="sxs-lookup"><span data-stu-id="98125-163">False</span></span>                                                              |
| <span data-ttu-id="98125-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98125-164">In Global Catalog</span></span>      | <span data-ttu-id="98125-165">否</span><span class="sxs-lookup"><span data-stu-id="98125-165">False</span></span>                                                              |
| <span data-ttu-id="98125-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98125-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="98125-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98125-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="98125-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98125-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98125-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-170">Search-Flags</span></span>           | <span data-ttu-id="98125-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98125-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="98125-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-172">System-Flags</span></span>           | <span data-ttu-id="98125-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98125-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="98125-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98125-174">Classes used in</span></span>        | [<span data-ttu-id="98125-175">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="98125-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="98125-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98125-176">Windows Server 2008</span></span>



| <span data-ttu-id="98125-177">進入</span><span class="sxs-lookup"><span data-stu-id="98125-177">Entry</span></span> | <span data-ttu-id="98125-178">值</span><span class="sxs-lookup"><span data-stu-id="98125-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="98125-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98125-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98125-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="98125-181">System-Only</span></span>            | <span data-ttu-id="98125-182">否</span><span class="sxs-lookup"><span data-stu-id="98125-182">False</span></span>                                                              |
| <span data-ttu-id="98125-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98125-183">Is-Single-Valued</span></span>       | <span data-ttu-id="98125-184">對</span><span class="sxs-lookup"><span data-stu-id="98125-184">True</span></span>                                                               |
| <span data-ttu-id="98125-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98125-185">Is Indexed</span></span>             | <span data-ttu-id="98125-186">否</span><span class="sxs-lookup"><span data-stu-id="98125-186">False</span></span>                                                              |
| <span data-ttu-id="98125-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98125-187">In Global Catalog</span></span>      | <span data-ttu-id="98125-188">否</span><span class="sxs-lookup"><span data-stu-id="98125-188">False</span></span>                                                              |
| <span data-ttu-id="98125-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98125-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="98125-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98125-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="98125-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98125-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98125-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-193">Search-Flags</span></span>           | <span data-ttu-id="98125-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98125-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="98125-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-195">System-Flags</span></span>           | <span data-ttu-id="98125-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98125-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="98125-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98125-197">Classes used in</span></span>        | [<span data-ttu-id="98125-198">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="98125-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="98125-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="98125-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="98125-200">進入</span><span class="sxs-lookup"><span data-stu-id="98125-200">Entry</span></span> | <span data-ttu-id="98125-201">值</span><span class="sxs-lookup"><span data-stu-id="98125-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="98125-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98125-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98125-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="98125-204">System-Only</span></span>            | <span data-ttu-id="98125-205">否</span><span class="sxs-lookup"><span data-stu-id="98125-205">False</span></span>                                                              |
| <span data-ttu-id="98125-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98125-206">Is-Single-Valued</span></span>       | <span data-ttu-id="98125-207">對</span><span class="sxs-lookup"><span data-stu-id="98125-207">True</span></span>                                                               |
| <span data-ttu-id="98125-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98125-208">Is Indexed</span></span>             | <span data-ttu-id="98125-209">否</span><span class="sxs-lookup"><span data-stu-id="98125-209">False</span></span>                                                              |
| <span data-ttu-id="98125-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98125-210">In Global Catalog</span></span>      | <span data-ttu-id="98125-211">否</span><span class="sxs-lookup"><span data-stu-id="98125-211">False</span></span>                                                              |
| <span data-ttu-id="98125-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98125-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="98125-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98125-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="98125-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98125-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98125-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-216">Search-Flags</span></span>           | <span data-ttu-id="98125-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98125-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="98125-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-218">System-Flags</span></span>           | <span data-ttu-id="98125-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98125-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="98125-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98125-220">Classes used in</span></span>        | [<span data-ttu-id="98125-221">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="98125-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="98125-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98125-222">Windows Server 2012</span></span>



| <span data-ttu-id="98125-223">進入</span><span class="sxs-lookup"><span data-stu-id="98125-223">Entry</span></span> | <span data-ttu-id="98125-224">值</span><span class="sxs-lookup"><span data-stu-id="98125-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="98125-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="98125-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98125-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="98125-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="98125-227">System-Only</span></span>            | <span data-ttu-id="98125-228">否</span><span class="sxs-lookup"><span data-stu-id="98125-228">False</span></span>                                                              |
| <span data-ttu-id="98125-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="98125-229">Is-Single-Valued</span></span>       | <span data-ttu-id="98125-230">對</span><span class="sxs-lookup"><span data-stu-id="98125-230">True</span></span>                                                               |
| <span data-ttu-id="98125-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="98125-231">Is Indexed</span></span>             | <span data-ttu-id="98125-232">否</span><span class="sxs-lookup"><span data-stu-id="98125-232">False</span></span>                                                              |
| <span data-ttu-id="98125-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="98125-233">In Global Catalog</span></span>      | <span data-ttu-id="98125-234">否</span><span class="sxs-lookup"><span data-stu-id="98125-234">False</span></span>                                                              |
| <span data-ttu-id="98125-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="98125-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="98125-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="98125-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="98125-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98125-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98125-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="98125-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-239">Search-Flags</span></span>           | <span data-ttu-id="98125-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98125-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="98125-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98125-241">System-Flags</span></span>           | <span data-ttu-id="98125-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98125-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="98125-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="98125-243">Classes used in</span></span>        | [<span data-ttu-id="98125-244">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="98125-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





