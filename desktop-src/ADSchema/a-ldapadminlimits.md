---
title: LDAP-管理-限制屬性
description: 包含一組定義 LDAP 伺服器管理限制的屬性值組。
ms.assetid: 335d666e-3f96-4df8-9555-e913efb8da2d
ms.tgt_platform: multiple
keywords:
- LDAP-管理-限制屬性 AD 架構
- lDAPAdminLimits 屬性 AD 架構
topic_type:
- apiref
api_name:
- LDAP-Admin-Limits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99d3dc16bdc16b04fe0dbfe295fbece83d57ebda
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845232"
---
# <a name="ldap-admin-limits-attribute"></a><span data-ttu-id="6e24e-105">LDAP-管理-限制屬性</span><span class="sxs-lookup"><span data-stu-id="6e24e-105">LDAP-Admin-Limits attribute</span></span>

<span data-ttu-id="6e24e-106">包含一組定義 LDAP 伺服器管理限制的屬性值組。</span><span class="sxs-lookup"><span data-stu-id="6e24e-106">Contains a set of attribute-value pairs defining LDAP server administrative limits.</span></span>



| <span data-ttu-id="6e24e-107">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-107">Entry</span></span> | <span data-ttu-id="6e24e-108">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6e24e-109">CN</span><span class="sxs-lookup"><span data-stu-id="6e24e-109">CN</span></span>                | <span data-ttu-id="6e24e-110">LDAP-管理-限制</span><span class="sxs-lookup"><span data-stu-id="6e24e-110">LDAP-Admin-Limits</span></span>                           |
| <span data-ttu-id="6e24e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6e24e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6e24e-112">lDAPAdminLimits</span><span class="sxs-lookup"><span data-stu-id="6e24e-112">lDAPAdminLimits</span></span>                             |
| <span data-ttu-id="6e24e-113">大小</span><span class="sxs-lookup"><span data-stu-id="6e24e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6e24e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6e24e-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6e24e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6e24e-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6e24e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-116">Attribute-Id</span></span>      | <span data-ttu-id="6e24e-117">1.2.840.113556.1.4.843</span><span class="sxs-lookup"><span data-stu-id="6e24e-117">1.2.840.113556.1.4.843</span></span>                      |
| <span data-ttu-id="6e24e-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6e24e-118">System-Id-Guid</span></span>    | <span data-ttu-id="6e24e-119">7359a352-90f7-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6e24e-119">7359a352-90f7-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="6e24e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e24e-120">Syntax</span></span>            | [<span data-ttu-id="6e24e-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6e24e-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6e24e-122">實作</span><span class="sxs-lookup"><span data-stu-id="6e24e-122">Implementations</span></span>

-   [<span data-ttu-id="6e24e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6e24e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6e24e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6e24e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6e24e-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6e24e-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6e24e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6e24e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6e24e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6e24e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6e24e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6e24e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6e24e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6e24e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6e24e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e24e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="6e24e-131">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-131">Entry</span></span> | <span data-ttu-id="6e24e-132">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e24e-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e24e-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e24e-135">System-Only</span></span>            | <span data-ttu-id="6e24e-136">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-136">False</span></span>                                            |
| <span data-ttu-id="6e24e-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e24e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6e24e-138">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-138">False</span></span>                                            |
| <span data-ttu-id="6e24e-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e24e-139">Is Indexed</span></span>             | <span data-ttu-id="6e24e-140">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-140">False</span></span>                                            |
| <span data-ttu-id="6e24e-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e24e-141">In Global Catalog</span></span>      | <span data-ttu-id="6e24e-142">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-142">False</span></span>                                            |
| <span data-ttu-id="6e24e-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e24e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e24e-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e24e-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e24e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e24e-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e24e-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-147">Search-Flags</span></span>           | <span data-ttu-id="6e24e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e24e-148">0x00000000</span></span>                                       |
| <span data-ttu-id="6e24e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-149">System-Flags</span></span>           | <span data-ttu-id="6e24e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e24e-150">0x00000010</span></span>                                       |
| <span data-ttu-id="6e24e-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e24e-151">Classes used in</span></span>        | [<span data-ttu-id="6e24e-152">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="6e24e-152">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6e24e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e24e-153">Windows Server 2003</span></span>



| <span data-ttu-id="6e24e-154">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-154">Entry</span></span> | <span data-ttu-id="6e24e-155">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e24e-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e24e-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e24e-158">System-Only</span></span>            | <span data-ttu-id="6e24e-159">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-159">False</span></span>                                            |
| <span data-ttu-id="6e24e-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e24e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6e24e-161">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-161">False</span></span>                                            |
| <span data-ttu-id="6e24e-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e24e-162">Is Indexed</span></span>             | <span data-ttu-id="6e24e-163">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-163">False</span></span>                                            |
| <span data-ttu-id="6e24e-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e24e-164">In Global Catalog</span></span>      | <span data-ttu-id="6e24e-165">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-165">False</span></span>                                            |
| <span data-ttu-id="6e24e-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e24e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e24e-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e24e-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e24e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e24e-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e24e-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-170">Search-Flags</span></span>           | <span data-ttu-id="6e24e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e24e-171">0x00000000</span></span>                                       |
| <span data-ttu-id="6e24e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-172">System-Flags</span></span>           | <span data-ttu-id="6e24e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e24e-173">0x00000010</span></span>                                       |
| <span data-ttu-id="6e24e-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e24e-174">Classes used in</span></span>        | [<span data-ttu-id="6e24e-175">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="6e24e-175">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6e24e-176">亞當</span><span class="sxs-lookup"><span data-stu-id="6e24e-176">ADAM</span></span>



| <span data-ttu-id="6e24e-177">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-177">Entry</span></span> | <span data-ttu-id="6e24e-178">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e24e-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e24e-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e24e-181">System-Only</span></span>            | <span data-ttu-id="6e24e-182">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-182">False</span></span>                                            |
| <span data-ttu-id="6e24e-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e24e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6e24e-184">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-184">False</span></span>                                            |
| <span data-ttu-id="6e24e-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e24e-185">Is Indexed</span></span>             | <span data-ttu-id="6e24e-186">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-186">False</span></span>                                            |
| <span data-ttu-id="6e24e-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e24e-187">In Global Catalog</span></span>      | <span data-ttu-id="6e24e-188">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-188">False</span></span>                                            |
| <span data-ttu-id="6e24e-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e24e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e24e-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e24e-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e24e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e24e-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e24e-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-193">Search-Flags</span></span>           | <span data-ttu-id="6e24e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e24e-194">0x00000000</span></span>                                       |
| <span data-ttu-id="6e24e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-195">System-Flags</span></span>           | <span data-ttu-id="6e24e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e24e-196">0x00000010</span></span>                                       |
| <span data-ttu-id="6e24e-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e24e-197">Classes used in</span></span>        | [<span data-ttu-id="6e24e-198">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="6e24e-198">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6e24e-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6e24e-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6e24e-200">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-200">Entry</span></span> | <span data-ttu-id="6e24e-201">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e24e-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e24e-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e24e-204">System-Only</span></span>            | <span data-ttu-id="6e24e-205">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-205">False</span></span>                                            |
| <span data-ttu-id="6e24e-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e24e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="6e24e-207">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-207">False</span></span>                                            |
| <span data-ttu-id="6e24e-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e24e-208">Is Indexed</span></span>             | <span data-ttu-id="6e24e-209">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-209">False</span></span>                                            |
| <span data-ttu-id="6e24e-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e24e-210">In Global Catalog</span></span>      | <span data-ttu-id="6e24e-211">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-211">False</span></span>                                            |
| <span data-ttu-id="6e24e-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e24e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e24e-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e24e-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e24e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e24e-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e24e-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-216">Search-Flags</span></span>           | <span data-ttu-id="6e24e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e24e-217">0x00000000</span></span>                                       |
| <span data-ttu-id="6e24e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-218">System-Flags</span></span>           | <span data-ttu-id="6e24e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e24e-219">0x00000010</span></span>                                       |
| <span data-ttu-id="6e24e-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e24e-220">Classes used in</span></span>        | [<span data-ttu-id="6e24e-221">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="6e24e-221">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6e24e-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e24e-222">Windows Server 2008</span></span>



| <span data-ttu-id="6e24e-223">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-223">Entry</span></span> | <span data-ttu-id="6e24e-224">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e24e-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e24e-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e24e-227">System-Only</span></span>            | <span data-ttu-id="6e24e-228">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-228">False</span></span>                                            |
| <span data-ttu-id="6e24e-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e24e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="6e24e-230">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-230">False</span></span>                                            |
| <span data-ttu-id="6e24e-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e24e-231">Is Indexed</span></span>             | <span data-ttu-id="6e24e-232">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-232">False</span></span>                                            |
| <span data-ttu-id="6e24e-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e24e-233">In Global Catalog</span></span>      | <span data-ttu-id="6e24e-234">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-234">False</span></span>                                            |
| <span data-ttu-id="6e24e-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e24e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e24e-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e24e-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e24e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e24e-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e24e-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-239">Search-Flags</span></span>           | <span data-ttu-id="6e24e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e24e-240">0x00000000</span></span>                                       |
| <span data-ttu-id="6e24e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-241">System-Flags</span></span>           | <span data-ttu-id="6e24e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e24e-242">0x00000010</span></span>                                       |
| <span data-ttu-id="6e24e-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e24e-243">Classes used in</span></span>        | [<span data-ttu-id="6e24e-244">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="6e24e-244">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6e24e-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e24e-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6e24e-246">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-246">Entry</span></span> | <span data-ttu-id="6e24e-247">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e24e-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e24e-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e24e-250">System-Only</span></span>            | <span data-ttu-id="6e24e-251">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-251">False</span></span>                                            |
| <span data-ttu-id="6e24e-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e24e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="6e24e-253">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-253">False</span></span>                                            |
| <span data-ttu-id="6e24e-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e24e-254">Is Indexed</span></span>             | <span data-ttu-id="6e24e-255">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-255">False</span></span>                                            |
| <span data-ttu-id="6e24e-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e24e-256">In Global Catalog</span></span>      | <span data-ttu-id="6e24e-257">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-257">False</span></span>                                            |
| <span data-ttu-id="6e24e-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e24e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e24e-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e24e-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e24e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e24e-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e24e-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-262">Search-Flags</span></span>           | <span data-ttu-id="6e24e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e24e-263">0x00000000</span></span>                                       |
| <span data-ttu-id="6e24e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-264">System-Flags</span></span>           | <span data-ttu-id="6e24e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e24e-265">0x00000010</span></span>                                       |
| <span data-ttu-id="6e24e-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e24e-266">Classes used in</span></span>        | [<span data-ttu-id="6e24e-267">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="6e24e-267">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6e24e-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e24e-268">Windows Server 2012</span></span>



| <span data-ttu-id="6e24e-269">進入</span><span class="sxs-lookup"><span data-stu-id="6e24e-269">Entry</span></span> | <span data-ttu-id="6e24e-270">值</span><span class="sxs-lookup"><span data-stu-id="6e24e-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e24e-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6e24e-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e24e-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e24e-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e24e-273">System-Only</span></span>            | <span data-ttu-id="6e24e-274">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-274">False</span></span>                                            |
| <span data-ttu-id="6e24e-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6e24e-275">Is-Single-Valued</span></span>       | <span data-ttu-id="6e24e-276">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-276">False</span></span>                                            |
| <span data-ttu-id="6e24e-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6e24e-277">Is Indexed</span></span>             | <span data-ttu-id="6e24e-278">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-278">False</span></span>                                            |
| <span data-ttu-id="6e24e-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6e24e-279">In Global Catalog</span></span>      | <span data-ttu-id="6e24e-280">否</span><span class="sxs-lookup"><span data-stu-id="6e24e-280">False</span></span>                                            |
| <span data-ttu-id="6e24e-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6e24e-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e24e-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6e24e-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e24e-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e24e-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e24e-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e24e-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-285">Search-Flags</span></span>           | <span data-ttu-id="6e24e-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e24e-286">0x00000000</span></span>                                       |
| <span data-ttu-id="6e24e-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e24e-287">System-Flags</span></span>           | <span data-ttu-id="6e24e-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e24e-288">0x00000010</span></span>                                       |
| <span data-ttu-id="6e24e-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6e24e-289">Classes used in</span></span>        | [<span data-ttu-id="6e24e-290">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="6e24e-290">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



 

 





