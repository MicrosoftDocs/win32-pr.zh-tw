---
title: Super-Scopes 屬性
description: 這個屬性是用來將 DHCP 類別中使用的所有不同範圍群組在一起，成為單一實體。
ms.assetid: c5c59a77-97d8-4f8b-9ac4-bc031333233f
ms.tgt_platform: multiple
keywords:
- Super-Scopes 屬性 AD 架構
- 超級領域屬性 AD 架構
topic_type:
- apiref
api_name:
- Super-Scopes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea8eba0856fd9a5a815f02bd2590b820e7b4d04
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107941"
---
# <a name="super-scopes-attribute"></a><span data-ttu-id="49d2c-105">Super-Scopes 屬性</span><span class="sxs-lookup"><span data-stu-id="49d2c-105">Super-Scopes attribute</span></span>

<span data-ttu-id="49d2c-106">這個屬性是用來將 DHCP 類別中使用的所有不同範圍群組在一起，成為單一實體。</span><span class="sxs-lookup"><span data-stu-id="49d2c-106">This attribute is used to group together all the different scopes used in the DHCP class into a single entity.</span></span>



| <span data-ttu-id="49d2c-107">進入</span><span class="sxs-lookup"><span data-stu-id="49d2c-107">Entry</span></span> | <span data-ttu-id="49d2c-108">值</span><span class="sxs-lookup"><span data-stu-id="49d2c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="49d2c-109">CN</span><span class="sxs-lookup"><span data-stu-id="49d2c-109">CN</span></span>                | <span data-ttu-id="49d2c-110">Super-Scopes</span><span class="sxs-lookup"><span data-stu-id="49d2c-110">Super-Scopes</span></span>                         |
| <span data-ttu-id="49d2c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="49d2c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="49d2c-112">超級領域</span><span class="sxs-lookup"><span data-stu-id="49d2c-112">superScopes</span></span>                          |
| <span data-ttu-id="49d2c-113">大小</span><span class="sxs-lookup"><span data-stu-id="49d2c-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="49d2c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="49d2c-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="49d2c-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="49d2c-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="49d2c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="49d2c-116">Attribute-Id</span></span>      | <span data-ttu-id="49d2c-117">1.2.840.113556.1.4.710</span><span class="sxs-lookup"><span data-stu-id="49d2c-117">1.2.840.113556.1.4.710</span></span>               |
| <span data-ttu-id="49d2c-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="49d2c-118">System-Id-Guid</span></span>    | <span data-ttu-id="49d2c-119">963d274b-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="49d2c-119">963d274b-48be-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="49d2c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="49d2c-120">Syntax</span></span>            | [<span data-ttu-id="49d2c-121">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="49d2c-121">**String(IA5)**</span></span>](s-string-ia5.md)  |



## <a name="implementations"></a><span data-ttu-id="49d2c-122">實作</span><span class="sxs-lookup"><span data-stu-id="49d2c-122">Implementations</span></span>

-   [<span data-ttu-id="49d2c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="49d2c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="49d2c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="49d2c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="49d2c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="49d2c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="49d2c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="49d2c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="49d2c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="49d2c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="49d2c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="49d2c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="49d2c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49d2c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="49d2c-130">進入</span><span class="sxs-lookup"><span data-stu-id="49d2c-130">Entry</span></span> | <span data-ttu-id="49d2c-131">值</span><span class="sxs-lookup"><span data-stu-id="49d2c-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="49d2c-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49d2c-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49d2c-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="49d2c-134">System-Only</span></span>            | <span data-ttu-id="49d2c-135">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-135">False</span></span>                                        |
| <span data-ttu-id="49d2c-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49d2c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="49d2c-137">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-137">False</span></span>                                        |
| <span data-ttu-id="49d2c-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49d2c-138">Is Indexed</span></span>             | <span data-ttu-id="49d2c-139">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-139">False</span></span>                                        |
| <span data-ttu-id="49d2c-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49d2c-140">In Global Catalog</span></span>      | <span data-ttu-id="49d2c-141">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-141">False</span></span>                                        |
| <span data-ttu-id="49d2c-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49d2c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="49d2c-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49d2c-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="49d2c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49d2c-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49d2c-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-146">Search-Flags</span></span>           | <span data-ttu-id="49d2c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49d2c-147">0x00000000</span></span>                                   |
| <span data-ttu-id="49d2c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-148">System-Flags</span></span>           | <span data-ttu-id="49d2c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49d2c-149">0x00000010</span></span>                                   |
| <span data-ttu-id="49d2c-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49d2c-150">Classes used in</span></span>        | [<span data-ttu-id="49d2c-151">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="49d2c-151">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="49d2c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49d2c-152">Windows Server 2003</span></span>



| <span data-ttu-id="49d2c-153">進入</span><span class="sxs-lookup"><span data-stu-id="49d2c-153">Entry</span></span> | <span data-ttu-id="49d2c-154">值</span><span class="sxs-lookup"><span data-stu-id="49d2c-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="49d2c-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49d2c-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49d2c-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="49d2c-157">System-Only</span></span>            | <span data-ttu-id="49d2c-158">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-158">False</span></span>                                        |
| <span data-ttu-id="49d2c-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49d2c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="49d2c-160">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-160">False</span></span>                                        |
| <span data-ttu-id="49d2c-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49d2c-161">Is Indexed</span></span>             | <span data-ttu-id="49d2c-162">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-162">False</span></span>                                        |
| <span data-ttu-id="49d2c-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49d2c-163">In Global Catalog</span></span>      | <span data-ttu-id="49d2c-164">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-164">False</span></span>                                        |
| <span data-ttu-id="49d2c-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49d2c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="49d2c-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49d2c-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="49d2c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49d2c-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49d2c-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-169">Search-Flags</span></span>           | <span data-ttu-id="49d2c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49d2c-170">0x00000000</span></span>                                   |
| <span data-ttu-id="49d2c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-171">System-Flags</span></span>           | <span data-ttu-id="49d2c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49d2c-172">0x00000010</span></span>                                   |
| <span data-ttu-id="49d2c-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49d2c-173">Classes used in</span></span>        | [<span data-ttu-id="49d2c-174">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="49d2c-174">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="49d2c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="49d2c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="49d2c-176">進入</span><span class="sxs-lookup"><span data-stu-id="49d2c-176">Entry</span></span> | <span data-ttu-id="49d2c-177">值</span><span class="sxs-lookup"><span data-stu-id="49d2c-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="49d2c-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49d2c-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49d2c-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="49d2c-180">System-Only</span></span>            | <span data-ttu-id="49d2c-181">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-181">False</span></span>                                        |
| <span data-ttu-id="49d2c-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49d2c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="49d2c-183">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-183">False</span></span>                                        |
| <span data-ttu-id="49d2c-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49d2c-184">Is Indexed</span></span>             | <span data-ttu-id="49d2c-185">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-185">False</span></span>                                        |
| <span data-ttu-id="49d2c-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49d2c-186">In Global Catalog</span></span>      | <span data-ttu-id="49d2c-187">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-187">False</span></span>                                        |
| <span data-ttu-id="49d2c-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49d2c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="49d2c-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49d2c-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="49d2c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49d2c-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49d2c-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-192">Search-Flags</span></span>           | <span data-ttu-id="49d2c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49d2c-193">0x00000000</span></span>                                   |
| <span data-ttu-id="49d2c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-194">System-Flags</span></span>           | <span data-ttu-id="49d2c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49d2c-195">0x00000010</span></span>                                   |
| <span data-ttu-id="49d2c-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49d2c-196">Classes used in</span></span>        | [<span data-ttu-id="49d2c-197">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="49d2c-197">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="49d2c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49d2c-198">Windows Server 2008</span></span>



| <span data-ttu-id="49d2c-199">進入</span><span class="sxs-lookup"><span data-stu-id="49d2c-199">Entry</span></span> | <span data-ttu-id="49d2c-200">值</span><span class="sxs-lookup"><span data-stu-id="49d2c-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="49d2c-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49d2c-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49d2c-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="49d2c-203">System-Only</span></span>            | <span data-ttu-id="49d2c-204">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-204">False</span></span>                                        |
| <span data-ttu-id="49d2c-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49d2c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="49d2c-206">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-206">False</span></span>                                        |
| <span data-ttu-id="49d2c-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49d2c-207">Is Indexed</span></span>             | <span data-ttu-id="49d2c-208">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-208">False</span></span>                                        |
| <span data-ttu-id="49d2c-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49d2c-209">In Global Catalog</span></span>      | <span data-ttu-id="49d2c-210">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-210">False</span></span>                                        |
| <span data-ttu-id="49d2c-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49d2c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="49d2c-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49d2c-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="49d2c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49d2c-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49d2c-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-215">Search-Flags</span></span>           | <span data-ttu-id="49d2c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49d2c-216">0x00000000</span></span>                                   |
| <span data-ttu-id="49d2c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-217">System-Flags</span></span>           | <span data-ttu-id="49d2c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49d2c-218">0x00000010</span></span>                                   |
| <span data-ttu-id="49d2c-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49d2c-219">Classes used in</span></span>        | [<span data-ttu-id="49d2c-220">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="49d2c-220">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="49d2c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="49d2c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="49d2c-222">進入</span><span class="sxs-lookup"><span data-stu-id="49d2c-222">Entry</span></span> | <span data-ttu-id="49d2c-223">值</span><span class="sxs-lookup"><span data-stu-id="49d2c-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="49d2c-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49d2c-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49d2c-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="49d2c-226">System-Only</span></span>            | <span data-ttu-id="49d2c-227">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-227">False</span></span>                                        |
| <span data-ttu-id="49d2c-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49d2c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="49d2c-229">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-229">False</span></span>                                        |
| <span data-ttu-id="49d2c-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49d2c-230">Is Indexed</span></span>             | <span data-ttu-id="49d2c-231">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-231">False</span></span>                                        |
| <span data-ttu-id="49d2c-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49d2c-232">In Global Catalog</span></span>      | <span data-ttu-id="49d2c-233">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-233">False</span></span>                                        |
| <span data-ttu-id="49d2c-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49d2c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="49d2c-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49d2c-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="49d2c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49d2c-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49d2c-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-238">Search-Flags</span></span>           | <span data-ttu-id="49d2c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49d2c-239">0x00000000</span></span>                                   |
| <span data-ttu-id="49d2c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-240">System-Flags</span></span>           | <span data-ttu-id="49d2c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49d2c-241">0x00000010</span></span>                                   |
| <span data-ttu-id="49d2c-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49d2c-242">Classes used in</span></span>        | [<span data-ttu-id="49d2c-243">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="49d2c-243">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="49d2c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49d2c-244">Windows Server 2012</span></span>



| <span data-ttu-id="49d2c-245">進入</span><span class="sxs-lookup"><span data-stu-id="49d2c-245">Entry</span></span> | <span data-ttu-id="49d2c-246">值</span><span class="sxs-lookup"><span data-stu-id="49d2c-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="49d2c-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49d2c-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49d2c-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="49d2c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="49d2c-249">System-Only</span></span>            | <span data-ttu-id="49d2c-250">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-250">False</span></span>                                        |
| <span data-ttu-id="49d2c-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49d2c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="49d2c-252">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-252">False</span></span>                                        |
| <span data-ttu-id="49d2c-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49d2c-253">Is Indexed</span></span>             | <span data-ttu-id="49d2c-254">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-254">False</span></span>                                        |
| <span data-ttu-id="49d2c-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49d2c-255">In Global Catalog</span></span>      | <span data-ttu-id="49d2c-256">否</span><span class="sxs-lookup"><span data-stu-id="49d2c-256">False</span></span>                                        |
| <span data-ttu-id="49d2c-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49d2c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="49d2c-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49d2c-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="49d2c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49d2c-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49d2c-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="49d2c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-261">Search-Flags</span></span>           | <span data-ttu-id="49d2c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49d2c-262">0x00000000</span></span>                                   |
| <span data-ttu-id="49d2c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49d2c-263">System-Flags</span></span>           | <span data-ttu-id="49d2c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49d2c-264">0x00000010</span></span>                                   |
| <span data-ttu-id="49d2c-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49d2c-265">Classes used in</span></span>        | [<span data-ttu-id="49d2c-266">**DHCP 類別**</span><span class="sxs-lookup"><span data-stu-id="49d2c-266">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





