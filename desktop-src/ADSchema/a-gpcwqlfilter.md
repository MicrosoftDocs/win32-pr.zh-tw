---
title: GPC-WQL-Filter 屬性
description: 用來儲存包含篩選的 GUID 和 WMI 命名空間路徑的字串。
ms.assetid: ea76239b-79e2-49b2-a848-a924450d332a
ms.tgt_platform: multiple
keywords:
- GPC-WQL-Filter 屬性 AD 架構
- gPCWQLFilter 屬性 AD 架構
topic_type:
- apiref
api_name:
- GPC-WQL-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9a6b8d3715c1692e93579d3c94cdfa44f4192e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845247"
---
# <a name="gpc-wql-filter-attribute"></a><span data-ttu-id="8d430-105">GPC-WQL-Filter 屬性</span><span class="sxs-lookup"><span data-stu-id="8d430-105">GPC-WQL-Filter attribute</span></span>

<span data-ttu-id="8d430-106">用來儲存包含篩選的 GUID 和 WMI 命名空間路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="8d430-106">Used to store a string that contains a GUID for the filter and a WMI namespace path.</span></span>



| <span data-ttu-id="8d430-107">進入</span><span class="sxs-lookup"><span data-stu-id="8d430-107">Entry</span></span> | <span data-ttu-id="8d430-108">值</span><span class="sxs-lookup"><span data-stu-id="8d430-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8d430-109">CN</span><span class="sxs-lookup"><span data-stu-id="8d430-109">CN</span></span>                | <span data-ttu-id="8d430-110">GPC-WQL-篩選</span><span class="sxs-lookup"><span data-stu-id="8d430-110">GPC-WQL-Filter</span></span>                                                                  |
| <span data-ttu-id="8d430-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8d430-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8d430-112">gPCWQLFilter</span><span class="sxs-lookup"><span data-stu-id="8d430-112">gPCWQLFilter</span></span>                                                                    |
| <span data-ttu-id="8d430-113">大小</span><span class="sxs-lookup"><span data-stu-id="8d430-113">Size</span></span>              | \-                                                                              |
| <span data-ttu-id="8d430-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8d430-114">Update Privilege</span></span>  | <span data-ttu-id="8d430-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="8d430-115">Domain administrator</span></span>                                                            |
| <span data-ttu-id="8d430-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8d430-116">Update Frequency</span></span>  | <span data-ttu-id="8d430-117">只有當系統管理員變更群組原則 UI 中的篩選屬性時。</span><span class="sxs-lookup"><span data-stu-id="8d430-117">Only when the administrator changes the filter property in the Group Policy UI.</span></span> |
| <span data-ttu-id="8d430-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8d430-118">Attribute-Id</span></span>      | <span data-ttu-id="8d430-119">1.2.840.113556.1.4.1694</span><span class="sxs-lookup"><span data-stu-id="8d430-119">1.2.840.113556.1.4.1694</span></span>                                                         |
| <span data-ttu-id="8d430-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8d430-120">System-Id-Guid</span></span>    | <span data-ttu-id="8d430-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span><span class="sxs-lookup"><span data-stu-id="8d430-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span></span>                                            |
| <span data-ttu-id="8d430-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d430-122">Syntax</span></span>            | [<span data-ttu-id="8d430-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8d430-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="8d430-124">實作</span><span class="sxs-lookup"><span data-stu-id="8d430-124">Implementations</span></span>

-   [<span data-ttu-id="8d430-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8d430-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8d430-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8d430-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8d430-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8d430-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8d430-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8d430-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8d430-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8d430-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8d430-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d430-130">Windows Server 2003</span></span>



| <span data-ttu-id="8d430-131">進入</span><span class="sxs-lookup"><span data-stu-id="8d430-131">Entry</span></span> | <span data-ttu-id="8d430-132">值</span><span class="sxs-lookup"><span data-stu-id="8d430-132">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8d430-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d430-133">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d430-134">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d430-135">System-Only</span></span>            | <span data-ttu-id="8d430-136">否</span><span class="sxs-lookup"><span data-stu-id="8d430-136">False</span></span>                                                               |
| <span data-ttu-id="8d430-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d430-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8d430-138">對</span><span class="sxs-lookup"><span data-stu-id="8d430-138">True</span></span>                                                                |
| <span data-ttu-id="8d430-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d430-139">Is Indexed</span></span>             | <span data-ttu-id="8d430-140">否</span><span class="sxs-lookup"><span data-stu-id="8d430-140">False</span></span>                                                               |
| <span data-ttu-id="8d430-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d430-141">In Global Catalog</span></span>      | <span data-ttu-id="8d430-142">否</span><span class="sxs-lookup"><span data-stu-id="8d430-142">False</span></span>                                                               |
| <span data-ttu-id="8d430-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d430-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d430-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d430-144">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8d430-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d430-145">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d430-146">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-147">Search-Flags</span></span>           | <span data-ttu-id="8d430-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d430-148">0x00000000</span></span>                                                          |
| <span data-ttu-id="8d430-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-149">System-Flags</span></span>           | <span data-ttu-id="8d430-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d430-150">0x00000010</span></span>                                                          |
| <span data-ttu-id="8d430-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d430-151">Classes used in</span></span>        | [<span data-ttu-id="8d430-152">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="8d430-152">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8d430-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8d430-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8d430-154">進入</span><span class="sxs-lookup"><span data-stu-id="8d430-154">Entry</span></span> | <span data-ttu-id="8d430-155">值</span><span class="sxs-lookup"><span data-stu-id="8d430-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8d430-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d430-156">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d430-157">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d430-158">System-Only</span></span>            | <span data-ttu-id="8d430-159">否</span><span class="sxs-lookup"><span data-stu-id="8d430-159">False</span></span>                                                               |
| <span data-ttu-id="8d430-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d430-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8d430-161">對</span><span class="sxs-lookup"><span data-stu-id="8d430-161">True</span></span>                                                                |
| <span data-ttu-id="8d430-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d430-162">Is Indexed</span></span>             | <span data-ttu-id="8d430-163">否</span><span class="sxs-lookup"><span data-stu-id="8d430-163">False</span></span>                                                               |
| <span data-ttu-id="8d430-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d430-164">In Global Catalog</span></span>      | <span data-ttu-id="8d430-165">否</span><span class="sxs-lookup"><span data-stu-id="8d430-165">False</span></span>                                                               |
| <span data-ttu-id="8d430-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d430-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d430-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d430-167">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8d430-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d430-168">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d430-169">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-170">Search-Flags</span></span>           | <span data-ttu-id="8d430-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d430-171">0x00000000</span></span>                                                          |
| <span data-ttu-id="8d430-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-172">System-Flags</span></span>           | <span data-ttu-id="8d430-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d430-173">0x00000010</span></span>                                                          |
| <span data-ttu-id="8d430-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d430-174">Classes used in</span></span>        | [<span data-ttu-id="8d430-175">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="8d430-175">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8d430-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d430-176">Windows Server 2008</span></span>



| <span data-ttu-id="8d430-177">進入</span><span class="sxs-lookup"><span data-stu-id="8d430-177">Entry</span></span> | <span data-ttu-id="8d430-178">值</span><span class="sxs-lookup"><span data-stu-id="8d430-178">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8d430-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d430-179">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d430-180">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d430-181">System-Only</span></span>            | <span data-ttu-id="8d430-182">否</span><span class="sxs-lookup"><span data-stu-id="8d430-182">False</span></span>                                                               |
| <span data-ttu-id="8d430-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d430-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8d430-184">對</span><span class="sxs-lookup"><span data-stu-id="8d430-184">True</span></span>                                                                |
| <span data-ttu-id="8d430-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d430-185">Is Indexed</span></span>             | <span data-ttu-id="8d430-186">否</span><span class="sxs-lookup"><span data-stu-id="8d430-186">False</span></span>                                                               |
| <span data-ttu-id="8d430-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d430-187">In Global Catalog</span></span>      | <span data-ttu-id="8d430-188">否</span><span class="sxs-lookup"><span data-stu-id="8d430-188">False</span></span>                                                               |
| <span data-ttu-id="8d430-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d430-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d430-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d430-190">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8d430-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d430-191">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d430-192">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-193">Search-Flags</span></span>           | <span data-ttu-id="8d430-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d430-194">0x00000000</span></span>                                                          |
| <span data-ttu-id="8d430-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-195">System-Flags</span></span>           | <span data-ttu-id="8d430-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d430-196">0x00000010</span></span>                                                          |
| <span data-ttu-id="8d430-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d430-197">Classes used in</span></span>        | [<span data-ttu-id="8d430-198">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="8d430-198">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8d430-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d430-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8d430-200">進入</span><span class="sxs-lookup"><span data-stu-id="8d430-200">Entry</span></span> | <span data-ttu-id="8d430-201">值</span><span class="sxs-lookup"><span data-stu-id="8d430-201">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8d430-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d430-202">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d430-203">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d430-204">System-Only</span></span>            | <span data-ttu-id="8d430-205">否</span><span class="sxs-lookup"><span data-stu-id="8d430-205">False</span></span>                                                               |
| <span data-ttu-id="8d430-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d430-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8d430-207">對</span><span class="sxs-lookup"><span data-stu-id="8d430-207">True</span></span>                                                                |
| <span data-ttu-id="8d430-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d430-208">Is Indexed</span></span>             | <span data-ttu-id="8d430-209">否</span><span class="sxs-lookup"><span data-stu-id="8d430-209">False</span></span>                                                               |
| <span data-ttu-id="8d430-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d430-210">In Global Catalog</span></span>      | <span data-ttu-id="8d430-211">否</span><span class="sxs-lookup"><span data-stu-id="8d430-211">False</span></span>                                                               |
| <span data-ttu-id="8d430-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d430-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d430-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d430-213">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8d430-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d430-214">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d430-215">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-216">Search-Flags</span></span>           | <span data-ttu-id="8d430-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d430-217">0x00000000</span></span>                                                          |
| <span data-ttu-id="8d430-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-218">System-Flags</span></span>           | <span data-ttu-id="8d430-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d430-219">0x00000010</span></span>                                                          |
| <span data-ttu-id="8d430-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d430-220">Classes used in</span></span>        | [<span data-ttu-id="8d430-221">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="8d430-221">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8d430-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d430-222">Windows Server 2012</span></span>



| <span data-ttu-id="8d430-223">進入</span><span class="sxs-lookup"><span data-stu-id="8d430-223">Entry</span></span> | <span data-ttu-id="8d430-224">值</span><span class="sxs-lookup"><span data-stu-id="8d430-224">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8d430-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8d430-225">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d430-226">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="8d430-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d430-227">System-Only</span></span>            | <span data-ttu-id="8d430-228">否</span><span class="sxs-lookup"><span data-stu-id="8d430-228">False</span></span>                                                               |
| <span data-ttu-id="8d430-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8d430-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8d430-230">對</span><span class="sxs-lookup"><span data-stu-id="8d430-230">True</span></span>                                                                |
| <span data-ttu-id="8d430-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8d430-231">Is Indexed</span></span>             | <span data-ttu-id="8d430-232">否</span><span class="sxs-lookup"><span data-stu-id="8d430-232">False</span></span>                                                               |
| <span data-ttu-id="8d430-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8d430-233">In Global Catalog</span></span>      | <span data-ttu-id="8d430-234">否</span><span class="sxs-lookup"><span data-stu-id="8d430-234">False</span></span>                                                               |
| <span data-ttu-id="8d430-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8d430-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d430-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8d430-236">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="8d430-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d430-237">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d430-238">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="8d430-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-239">Search-Flags</span></span>           | <span data-ttu-id="8d430-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d430-240">0x00000000</span></span>                                                          |
| <span data-ttu-id="8d430-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d430-241">System-Flags</span></span>           | <span data-ttu-id="8d430-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d430-242">0x00000010</span></span>                                                          |
| <span data-ttu-id="8d430-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8d430-243">Classes used in</span></span>        | [<span data-ttu-id="8d430-244">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="8d430-244">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





