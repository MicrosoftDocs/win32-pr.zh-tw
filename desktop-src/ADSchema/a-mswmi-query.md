---
title: ms-WMI-查詢屬性
description: 單一 WQL 查詢。
ms.assetid: 3fb594fc-d160-4807-a019-3dec56d2262b
ms.tgt_platform: multiple
keywords:
- ms-WMI-查詢屬性 AD 架構
- msWMI-查詢屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-WMI-Query
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5bb5376cf957d46894c6fa2c59016564d28dfb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845391"
---
# <a name="ms-wmi-query-attribute"></a><span data-ttu-id="3d1b6-105">ms-WMI-查詢屬性</span><span class="sxs-lookup"><span data-stu-id="3d1b6-105">ms-WMI-Query attribute</span></span>

<span data-ttu-id="3d1b6-106">單一 WQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-106">A single WQL query.</span></span>



| <span data-ttu-id="3d1b6-107">進入</span><span class="sxs-lookup"><span data-stu-id="3d1b6-107">Entry</span></span> | <span data-ttu-id="3d1b6-108">值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3d1b6-109">CN</span><span class="sxs-lookup"><span data-stu-id="3d1b6-109">CN</span></span>                | <span data-ttu-id="3d1b6-110">ms-WMI-查詢</span><span class="sxs-lookup"><span data-stu-id="3d1b6-110">ms-WMI-Query</span></span>                                |
| <span data-ttu-id="3d1b6-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3d1b6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3d1b6-112">msWMI-查詢</span><span class="sxs-lookup"><span data-stu-id="3d1b6-112">msWMI-Query</span></span>                                 |
| <span data-ttu-id="3d1b6-113">大小</span><span class="sxs-lookup"><span data-stu-id="3d1b6-113">Size</span></span>              | <span data-ttu-id="3d1b6-114">少於250個字元。</span><span class="sxs-lookup"><span data-stu-id="3d1b6-114">Less than 250 characters.</span></span>                   |
| <span data-ttu-id="3d1b6-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3d1b6-115">Update Privilege</span></span>  | <span data-ttu-id="3d1b6-116">群組原則系統管理員</span><span class="sxs-lookup"><span data-stu-id="3d1b6-116">Group Policy Administrator</span></span>                  |
| <span data-ttu-id="3d1b6-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3d1b6-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3d1b6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d1b6-118">Attribute-Id</span></span>      | <span data-ttu-id="3d1b6-119">1.2.840.113556.1.4.1642</span><span class="sxs-lookup"><span data-stu-id="3d1b6-119">1.2.840.113556.1.4.1642</span></span>                     |
| <span data-ttu-id="3d1b6-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3d1b6-120">System-Id-Guid</span></span>    | <span data-ttu-id="3d1b6-121">65fff93e-35e3-45a3-85ae-876c6718297f</span><span class="sxs-lookup"><span data-stu-id="3d1b6-121">65fff93e-35e3-45a3-85ae-876c6718297f</span></span>        |
| <span data-ttu-id="3d1b6-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d1b6-122">Syntax</span></span>            | [<span data-ttu-id="3d1b6-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3d1b6-124">實作</span><span class="sxs-lookup"><span data-stu-id="3d1b6-124">Implementations</span></span>

-   [<span data-ttu-id="3d1b6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d1b6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d1b6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d1b6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d1b6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3d1b6-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d1b6-130">Windows Server 2003</span></span>



| <span data-ttu-id="3d1b6-131">進入</span><span class="sxs-lookup"><span data-stu-id="3d1b6-131">Entry</span></span> | <span data-ttu-id="3d1b6-132">值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="3d1b6-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d1b6-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d1b6-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d1b6-135">System-Only</span></span>            | <span data-ttu-id="3d1b6-136">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-136">False</span></span>                                          |
| <span data-ttu-id="3d1b6-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3d1b6-138">對</span><span class="sxs-lookup"><span data-stu-id="3d1b6-138">True</span></span>                                           |
| <span data-ttu-id="3d1b6-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d1b6-139">Is Indexed</span></span>             | <span data-ttu-id="3d1b6-140">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-140">False</span></span>                                          |
| <span data-ttu-id="3d1b6-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d1b6-141">In Global Catalog</span></span>      | <span data-ttu-id="3d1b6-142">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-142">False</span></span>                                          |
| <span data-ttu-id="3d1b6-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d1b6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d1b6-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d1b6-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="3d1b6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d1b6-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d1b6-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-147">Search-Flags</span></span>           | <span data-ttu-id="3d1b6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d1b6-148">0x00000000</span></span>                                     |
| <span data-ttu-id="3d1b6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-149">System-Flags</span></span>           | <span data-ttu-id="3d1b6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d1b6-150">0x00000010</span></span>                                     |
| <span data-ttu-id="3d1b6-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d1b6-151">Classes used in</span></span>        | [<span data-ttu-id="3d1b6-152">**ms-WMI-規則**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-152">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d1b6-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d1b6-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d1b6-154">進入</span><span class="sxs-lookup"><span data-stu-id="3d1b6-154">Entry</span></span> | <span data-ttu-id="3d1b6-155">值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="3d1b6-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d1b6-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d1b6-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d1b6-158">System-Only</span></span>            | <span data-ttu-id="3d1b6-159">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-159">False</span></span>                                          |
| <span data-ttu-id="3d1b6-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3d1b6-161">對</span><span class="sxs-lookup"><span data-stu-id="3d1b6-161">True</span></span>                                           |
| <span data-ttu-id="3d1b6-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d1b6-162">Is Indexed</span></span>             | <span data-ttu-id="3d1b6-163">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-163">False</span></span>                                          |
| <span data-ttu-id="3d1b6-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d1b6-164">In Global Catalog</span></span>      | <span data-ttu-id="3d1b6-165">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-165">False</span></span>                                          |
| <span data-ttu-id="3d1b6-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d1b6-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d1b6-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d1b6-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="3d1b6-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d1b6-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d1b6-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-170">Search-Flags</span></span>           | <span data-ttu-id="3d1b6-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d1b6-171">0x00000000</span></span>                                     |
| <span data-ttu-id="3d1b6-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-172">System-Flags</span></span>           | <span data-ttu-id="3d1b6-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d1b6-173">0x00000010</span></span>                                     |
| <span data-ttu-id="3d1b6-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d1b6-174">Classes used in</span></span>        | [<span data-ttu-id="3d1b6-175">**ms-WMI-規則**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-175">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d1b6-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d1b6-176">Windows Server 2008</span></span>



| <span data-ttu-id="3d1b6-177">進入</span><span class="sxs-lookup"><span data-stu-id="3d1b6-177">Entry</span></span> | <span data-ttu-id="3d1b6-178">值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="3d1b6-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d1b6-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d1b6-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d1b6-181">System-Only</span></span>            | <span data-ttu-id="3d1b6-182">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-182">False</span></span>                                          |
| <span data-ttu-id="3d1b6-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-183">Is-Single-Valued</span></span>       | <span data-ttu-id="3d1b6-184">對</span><span class="sxs-lookup"><span data-stu-id="3d1b6-184">True</span></span>                                           |
| <span data-ttu-id="3d1b6-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d1b6-185">Is Indexed</span></span>             | <span data-ttu-id="3d1b6-186">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-186">False</span></span>                                          |
| <span data-ttu-id="3d1b6-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d1b6-187">In Global Catalog</span></span>      | <span data-ttu-id="3d1b6-188">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-188">False</span></span>                                          |
| <span data-ttu-id="3d1b6-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d1b6-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d1b6-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d1b6-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="3d1b6-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d1b6-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d1b6-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-193">Search-Flags</span></span>           | <span data-ttu-id="3d1b6-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d1b6-194">0x00000000</span></span>                                     |
| <span data-ttu-id="3d1b6-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-195">System-Flags</span></span>           | <span data-ttu-id="3d1b6-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d1b6-196">0x00000010</span></span>                                     |
| <span data-ttu-id="3d1b6-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d1b6-197">Classes used in</span></span>        | [<span data-ttu-id="3d1b6-198">**ms-WMI-規則**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-198">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d1b6-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d1b6-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d1b6-200">進入</span><span class="sxs-lookup"><span data-stu-id="3d1b6-200">Entry</span></span> | <span data-ttu-id="3d1b6-201">值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="3d1b6-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d1b6-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d1b6-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d1b6-204">System-Only</span></span>            | <span data-ttu-id="3d1b6-205">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-205">False</span></span>                                          |
| <span data-ttu-id="3d1b6-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-206">Is-Single-Valued</span></span>       | <span data-ttu-id="3d1b6-207">對</span><span class="sxs-lookup"><span data-stu-id="3d1b6-207">True</span></span>                                           |
| <span data-ttu-id="3d1b6-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d1b6-208">Is Indexed</span></span>             | <span data-ttu-id="3d1b6-209">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-209">False</span></span>                                          |
| <span data-ttu-id="3d1b6-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d1b6-210">In Global Catalog</span></span>      | <span data-ttu-id="3d1b6-211">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-211">False</span></span>                                          |
| <span data-ttu-id="3d1b6-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d1b6-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d1b6-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d1b6-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="3d1b6-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d1b6-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d1b6-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-216">Search-Flags</span></span>           | <span data-ttu-id="3d1b6-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d1b6-217">0x00000000</span></span>                                     |
| <span data-ttu-id="3d1b6-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-218">System-Flags</span></span>           | <span data-ttu-id="3d1b6-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d1b6-219">0x00000010</span></span>                                     |
| <span data-ttu-id="3d1b6-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d1b6-220">Classes used in</span></span>        | [<span data-ttu-id="3d1b6-221">**ms-WMI-規則**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-221">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d1b6-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d1b6-222">Windows Server 2012</span></span>



| <span data-ttu-id="3d1b6-223">進入</span><span class="sxs-lookup"><span data-stu-id="3d1b6-223">Entry</span></span> | <span data-ttu-id="3d1b6-224">值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="3d1b6-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d1b6-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d1b6-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="3d1b6-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d1b6-227">System-Only</span></span>            | <span data-ttu-id="3d1b6-228">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-228">False</span></span>                                          |
| <span data-ttu-id="3d1b6-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d1b6-229">Is-Single-Valued</span></span>       | <span data-ttu-id="3d1b6-230">對</span><span class="sxs-lookup"><span data-stu-id="3d1b6-230">True</span></span>                                           |
| <span data-ttu-id="3d1b6-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d1b6-231">Is Indexed</span></span>             | <span data-ttu-id="3d1b6-232">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-232">False</span></span>                                          |
| <span data-ttu-id="3d1b6-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d1b6-233">In Global Catalog</span></span>      | <span data-ttu-id="3d1b6-234">否</span><span class="sxs-lookup"><span data-stu-id="3d1b6-234">False</span></span>                                          |
| <span data-ttu-id="3d1b6-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d1b6-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d1b6-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d1b6-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="3d1b6-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d1b6-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d1b6-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="3d1b6-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-239">Search-Flags</span></span>           | <span data-ttu-id="3d1b6-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d1b6-240">0x00000000</span></span>                                     |
| <span data-ttu-id="3d1b6-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d1b6-241">System-Flags</span></span>           | <span data-ttu-id="3d1b6-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d1b6-242">0x00000010</span></span>                                     |
| <span data-ttu-id="3d1b6-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d1b6-243">Classes used in</span></span>        | [<span data-ttu-id="3d1b6-244">**ms-WMI-規則**</span><span class="sxs-lookup"><span data-stu-id="3d1b6-244">**ms-WMI-Rule**</span></span>](c-mswmi-rule.md)<br/> |



 

 





