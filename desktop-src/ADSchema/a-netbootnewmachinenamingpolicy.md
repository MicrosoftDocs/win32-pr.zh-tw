---
title: netboot-新增-電腦-命名原則屬性
description: 指出新的用戶端電腦帳戶將使用的命名配置。
ms.assetid: e8ffc9b1-b2a2-4216-8498-85cb6c8cc7ae
ms.tgt_platform: multiple
keywords:
- netboot-新增-電腦-命名原則屬性 AD 架構
- netbootNewMachineNamingPolicy 屬性 AD 架構
topic_type:
- apiref
api_name:
- netboot-New-Machine-Naming-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da6cb51ced16da6510f3fb85ec80e4fa641603b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108005"
---
# <a name="netboot-new-machine-naming-policy-attribute"></a><span data-ttu-id="9053c-105">netboot-新增-電腦-命名原則屬性</span><span class="sxs-lookup"><span data-stu-id="9053c-105">netboot-New-Machine-Naming-Policy attribute</span></span>

<span data-ttu-id="9053c-106">指出新的用戶端電腦帳戶將使用的命名配置。</span><span class="sxs-lookup"><span data-stu-id="9053c-106">Indicates the naming scheme which new client computer accounts will use.</span></span>



| <span data-ttu-id="9053c-107">進入</span><span class="sxs-lookup"><span data-stu-id="9053c-107">Entry</span></span> | <span data-ttu-id="9053c-108">值</span><span class="sxs-lookup"><span data-stu-id="9053c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9053c-109">CN</span><span class="sxs-lookup"><span data-stu-id="9053c-109">CN</span></span>                | <span data-ttu-id="9053c-110">netboot-新增-電腦-命名原則</span><span class="sxs-lookup"><span data-stu-id="9053c-110">netboot-New-Machine-Naming-Policy</span></span>           |
| <span data-ttu-id="9053c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9053c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9053c-112">netbootNewMachineNamingPolicy</span><span class="sxs-lookup"><span data-stu-id="9053c-112">netbootNewMachineNamingPolicy</span></span>               |
| <span data-ttu-id="9053c-113">大小</span><span class="sxs-lookup"><span data-stu-id="9053c-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9053c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9053c-114">Update Privilege</span></span>  | <span data-ttu-id="9053c-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9053c-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="9053c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9053c-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9053c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9053c-117">Attribute-Id</span></span>      | <span data-ttu-id="9053c-118">1.2.840.113556.1.4.855</span><span class="sxs-lookup"><span data-stu-id="9053c-118">1.2.840.113556.1.4.855</span></span>                      |
| <span data-ttu-id="9053c-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9053c-119">System-Id-Guid</span></span>    | <span data-ttu-id="9053c-120">0738307c-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9053c-120">0738307c-91df-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="9053c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="9053c-121">Syntax</span></span>            | [<span data-ttu-id="9053c-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9053c-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9053c-123">實作</span><span class="sxs-lookup"><span data-stu-id="9053c-123">Implementations</span></span>

-   [<span data-ttu-id="9053c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9053c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9053c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9053c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9053c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9053c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9053c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9053c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9053c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9053c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9053c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9053c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9053c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9053c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="9053c-131">進入</span><span class="sxs-lookup"><span data-stu-id="9053c-131">Entry</span></span> | <span data-ttu-id="9053c-132">值</span><span class="sxs-lookup"><span data-stu-id="9053c-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9053c-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9053c-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9053c-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="9053c-135">System-Only</span></span>            | <span data-ttu-id="9053c-136">否</span><span class="sxs-lookup"><span data-stu-id="9053c-136">False</span></span>                                                      |
| <span data-ttu-id="9053c-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9053c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="9053c-138">否</span><span class="sxs-lookup"><span data-stu-id="9053c-138">False</span></span>                                                      |
| <span data-ttu-id="9053c-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9053c-139">Is Indexed</span></span>             | <span data-ttu-id="9053c-140">否</span><span class="sxs-lookup"><span data-stu-id="9053c-140">False</span></span>                                                      |
| <span data-ttu-id="9053c-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9053c-141">In Global Catalog</span></span>      | <span data-ttu-id="9053c-142">否</span><span class="sxs-lookup"><span data-stu-id="9053c-142">False</span></span>                                                      |
| <span data-ttu-id="9053c-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9053c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="9053c-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9053c-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9053c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9053c-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9053c-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-147">Search-Flags</span></span>           | <span data-ttu-id="9053c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9053c-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="9053c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-149">System-Flags</span></span>           | <span data-ttu-id="9053c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9053c-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="9053c-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9053c-151">Classes used in</span></span>        | [<span data-ttu-id="9053c-152">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9053c-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9053c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9053c-153">Windows Server 2003</span></span>



| <span data-ttu-id="9053c-154">進入</span><span class="sxs-lookup"><span data-stu-id="9053c-154">Entry</span></span> | <span data-ttu-id="9053c-155">值</span><span class="sxs-lookup"><span data-stu-id="9053c-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9053c-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9053c-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9053c-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="9053c-158">System-Only</span></span>            | <span data-ttu-id="9053c-159">否</span><span class="sxs-lookup"><span data-stu-id="9053c-159">False</span></span>                                                      |
| <span data-ttu-id="9053c-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9053c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="9053c-161">否</span><span class="sxs-lookup"><span data-stu-id="9053c-161">False</span></span>                                                      |
| <span data-ttu-id="9053c-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9053c-162">Is Indexed</span></span>             | <span data-ttu-id="9053c-163">否</span><span class="sxs-lookup"><span data-stu-id="9053c-163">False</span></span>                                                      |
| <span data-ttu-id="9053c-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9053c-164">In Global Catalog</span></span>      | <span data-ttu-id="9053c-165">否</span><span class="sxs-lookup"><span data-stu-id="9053c-165">False</span></span>                                                      |
| <span data-ttu-id="9053c-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9053c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="9053c-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9053c-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9053c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9053c-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9053c-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-170">Search-Flags</span></span>           | <span data-ttu-id="9053c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9053c-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="9053c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-172">System-Flags</span></span>           | <span data-ttu-id="9053c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9053c-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="9053c-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9053c-174">Classes used in</span></span>        | [<span data-ttu-id="9053c-175">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9053c-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9053c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9053c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9053c-177">進入</span><span class="sxs-lookup"><span data-stu-id="9053c-177">Entry</span></span> | <span data-ttu-id="9053c-178">值</span><span class="sxs-lookup"><span data-stu-id="9053c-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9053c-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9053c-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9053c-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="9053c-181">System-Only</span></span>            | <span data-ttu-id="9053c-182">否</span><span class="sxs-lookup"><span data-stu-id="9053c-182">False</span></span>                                                      |
| <span data-ttu-id="9053c-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9053c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="9053c-184">否</span><span class="sxs-lookup"><span data-stu-id="9053c-184">False</span></span>                                                      |
| <span data-ttu-id="9053c-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9053c-185">Is Indexed</span></span>             | <span data-ttu-id="9053c-186">否</span><span class="sxs-lookup"><span data-stu-id="9053c-186">False</span></span>                                                      |
| <span data-ttu-id="9053c-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9053c-187">In Global Catalog</span></span>      | <span data-ttu-id="9053c-188">否</span><span class="sxs-lookup"><span data-stu-id="9053c-188">False</span></span>                                                      |
| <span data-ttu-id="9053c-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9053c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="9053c-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9053c-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9053c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9053c-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9053c-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-193">Search-Flags</span></span>           | <span data-ttu-id="9053c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9053c-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="9053c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-195">System-Flags</span></span>           | <span data-ttu-id="9053c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9053c-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="9053c-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9053c-197">Classes used in</span></span>        | [<span data-ttu-id="9053c-198">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9053c-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9053c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9053c-199">Windows Server 2008</span></span>



| <span data-ttu-id="9053c-200">進入</span><span class="sxs-lookup"><span data-stu-id="9053c-200">Entry</span></span> | <span data-ttu-id="9053c-201">值</span><span class="sxs-lookup"><span data-stu-id="9053c-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9053c-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9053c-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9053c-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9053c-204">System-Only</span></span>            | <span data-ttu-id="9053c-205">否</span><span class="sxs-lookup"><span data-stu-id="9053c-205">False</span></span>                                                      |
| <span data-ttu-id="9053c-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9053c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9053c-207">否</span><span class="sxs-lookup"><span data-stu-id="9053c-207">False</span></span>                                                      |
| <span data-ttu-id="9053c-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9053c-208">Is Indexed</span></span>             | <span data-ttu-id="9053c-209">否</span><span class="sxs-lookup"><span data-stu-id="9053c-209">False</span></span>                                                      |
| <span data-ttu-id="9053c-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9053c-210">In Global Catalog</span></span>      | <span data-ttu-id="9053c-211">否</span><span class="sxs-lookup"><span data-stu-id="9053c-211">False</span></span>                                                      |
| <span data-ttu-id="9053c-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9053c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9053c-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9053c-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9053c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9053c-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9053c-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-216">Search-Flags</span></span>           | <span data-ttu-id="9053c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9053c-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="9053c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-218">System-Flags</span></span>           | <span data-ttu-id="9053c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9053c-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="9053c-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9053c-220">Classes used in</span></span>        | [<span data-ttu-id="9053c-221">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9053c-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9053c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9053c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9053c-223">進入</span><span class="sxs-lookup"><span data-stu-id="9053c-223">Entry</span></span> | <span data-ttu-id="9053c-224">值</span><span class="sxs-lookup"><span data-stu-id="9053c-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9053c-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9053c-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9053c-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9053c-227">System-Only</span></span>            | <span data-ttu-id="9053c-228">否</span><span class="sxs-lookup"><span data-stu-id="9053c-228">False</span></span>                                                      |
| <span data-ttu-id="9053c-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9053c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9053c-230">否</span><span class="sxs-lookup"><span data-stu-id="9053c-230">False</span></span>                                                      |
| <span data-ttu-id="9053c-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9053c-231">Is Indexed</span></span>             | <span data-ttu-id="9053c-232">否</span><span class="sxs-lookup"><span data-stu-id="9053c-232">False</span></span>                                                      |
| <span data-ttu-id="9053c-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9053c-233">In Global Catalog</span></span>      | <span data-ttu-id="9053c-234">否</span><span class="sxs-lookup"><span data-stu-id="9053c-234">False</span></span>                                                      |
| <span data-ttu-id="9053c-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9053c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9053c-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9053c-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9053c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9053c-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9053c-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-239">Search-Flags</span></span>           | <span data-ttu-id="9053c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9053c-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="9053c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-241">System-Flags</span></span>           | <span data-ttu-id="9053c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9053c-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="9053c-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9053c-243">Classes used in</span></span>        | [<span data-ttu-id="9053c-244">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9053c-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9053c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9053c-245">Windows Server 2012</span></span>



| <span data-ttu-id="9053c-246">進入</span><span class="sxs-lookup"><span data-stu-id="9053c-246">Entry</span></span> | <span data-ttu-id="9053c-247">值</span><span class="sxs-lookup"><span data-stu-id="9053c-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="9053c-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9053c-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9053c-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="9053c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="9053c-250">System-Only</span></span>            | <span data-ttu-id="9053c-251">否</span><span class="sxs-lookup"><span data-stu-id="9053c-251">False</span></span>                                                      |
| <span data-ttu-id="9053c-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9053c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="9053c-253">否</span><span class="sxs-lookup"><span data-stu-id="9053c-253">False</span></span>                                                      |
| <span data-ttu-id="9053c-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9053c-254">Is Indexed</span></span>             | <span data-ttu-id="9053c-255">否</span><span class="sxs-lookup"><span data-stu-id="9053c-255">False</span></span>                                                      |
| <span data-ttu-id="9053c-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9053c-256">In Global Catalog</span></span>      | <span data-ttu-id="9053c-257">否</span><span class="sxs-lookup"><span data-stu-id="9053c-257">False</span></span>                                                      |
| <span data-ttu-id="9053c-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9053c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="9053c-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9053c-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="9053c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9053c-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9053c-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="9053c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-262">Search-Flags</span></span>           | <span data-ttu-id="9053c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9053c-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="9053c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9053c-264">System-Flags</span></span>           | <span data-ttu-id="9053c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9053c-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="9053c-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9053c-266">Classes used in</span></span>        | [<span data-ttu-id="9053c-267">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="9053c-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





