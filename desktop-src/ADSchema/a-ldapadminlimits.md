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
# <a name="ldap-admin-limits-attribute"></a><span data-ttu-id="d4c85-105">LDAP-管理-限制屬性</span><span class="sxs-lookup"><span data-stu-id="d4c85-105">LDAP-Admin-Limits attribute</span></span>

<span data-ttu-id="d4c85-106">包含一組定義 LDAP 伺服器管理限制的屬性值組。</span><span class="sxs-lookup"><span data-stu-id="d4c85-106">Contains a set of attribute-value pairs defining LDAP server administrative limits.</span></span>



| <span data-ttu-id="d4c85-107">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-107">Entry</span></span> | <span data-ttu-id="d4c85-108">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d4c85-109">CN</span><span class="sxs-lookup"><span data-stu-id="d4c85-109">CN</span></span>                | <span data-ttu-id="d4c85-110">LDAP-管理-限制</span><span class="sxs-lookup"><span data-stu-id="d4c85-110">LDAP-Admin-Limits</span></span>                           |
| <span data-ttu-id="d4c85-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d4c85-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d4c85-112">lDAPAdminLimits</span><span class="sxs-lookup"><span data-stu-id="d4c85-112">lDAPAdminLimits</span></span>                             |
| <span data-ttu-id="d4c85-113">大小</span><span class="sxs-lookup"><span data-stu-id="d4c85-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d4c85-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d4c85-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d4c85-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d4c85-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d4c85-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-116">Attribute-Id</span></span>      | <span data-ttu-id="d4c85-117">1.2.840.113556.1.4.843</span><span class="sxs-lookup"><span data-stu-id="d4c85-117">1.2.840.113556.1.4.843</span></span>                      |
| <span data-ttu-id="d4c85-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d4c85-118">System-Id-Guid</span></span>    | <span data-ttu-id="d4c85-119">7359a352-90f7-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d4c85-119">7359a352-90f7-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="d4c85-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4c85-120">Syntax</span></span>            | [<span data-ttu-id="d4c85-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d4c85-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d4c85-122">實作</span><span class="sxs-lookup"><span data-stu-id="d4c85-122">Implementations</span></span>

-   [<span data-ttu-id="d4c85-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d4c85-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d4c85-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d4c85-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d4c85-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="d4c85-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d4c85-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d4c85-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d4c85-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d4c85-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d4c85-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d4c85-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d4c85-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d4c85-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d4c85-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4c85-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d4c85-131">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-131">Entry</span></span> | <span data-ttu-id="d4c85-132">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d4c85-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4c85-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4c85-135">System-Only</span></span>            | <span data-ttu-id="d4c85-136">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-136">False</span></span>                                            |
| <span data-ttu-id="d4c85-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4c85-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d4c85-138">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-138">False</span></span>                                            |
| <span data-ttu-id="d4c85-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4c85-139">Is Indexed</span></span>             | <span data-ttu-id="d4c85-140">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-140">False</span></span>                                            |
| <span data-ttu-id="d4c85-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4c85-141">In Global Catalog</span></span>      | <span data-ttu-id="d4c85-142">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-142">False</span></span>                                            |
| <span data-ttu-id="d4c85-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4c85-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4c85-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4c85-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d4c85-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4c85-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4c85-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-147">Search-Flags</span></span>           | <span data-ttu-id="d4c85-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4c85-148">0x00000000</span></span>                                       |
| <span data-ttu-id="d4c85-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-149">System-Flags</span></span>           | <span data-ttu-id="d4c85-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4c85-150">0x00000010</span></span>                                       |
| <span data-ttu-id="d4c85-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4c85-151">Classes used in</span></span>        | [<span data-ttu-id="d4c85-152">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d4c85-152">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d4c85-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4c85-153">Windows Server 2003</span></span>



| <span data-ttu-id="d4c85-154">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-154">Entry</span></span> | <span data-ttu-id="d4c85-155">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d4c85-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4c85-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4c85-158">System-Only</span></span>            | <span data-ttu-id="d4c85-159">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-159">False</span></span>                                            |
| <span data-ttu-id="d4c85-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4c85-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d4c85-161">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-161">False</span></span>                                            |
| <span data-ttu-id="d4c85-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4c85-162">Is Indexed</span></span>             | <span data-ttu-id="d4c85-163">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-163">False</span></span>                                            |
| <span data-ttu-id="d4c85-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4c85-164">In Global Catalog</span></span>      | <span data-ttu-id="d4c85-165">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-165">False</span></span>                                            |
| <span data-ttu-id="d4c85-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4c85-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4c85-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4c85-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d4c85-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4c85-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4c85-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-170">Search-Flags</span></span>           | <span data-ttu-id="d4c85-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4c85-171">0x00000000</span></span>                                       |
| <span data-ttu-id="d4c85-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-172">System-Flags</span></span>           | <span data-ttu-id="d4c85-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4c85-173">0x00000010</span></span>                                       |
| <span data-ttu-id="d4c85-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4c85-174">Classes used in</span></span>        | [<span data-ttu-id="d4c85-175">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d4c85-175">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d4c85-176">亞當</span><span class="sxs-lookup"><span data-stu-id="d4c85-176">ADAM</span></span>



| <span data-ttu-id="d4c85-177">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-177">Entry</span></span> | <span data-ttu-id="d4c85-178">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d4c85-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4c85-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4c85-181">System-Only</span></span>            | <span data-ttu-id="d4c85-182">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-182">False</span></span>                                            |
| <span data-ttu-id="d4c85-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4c85-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d4c85-184">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-184">False</span></span>                                            |
| <span data-ttu-id="d4c85-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4c85-185">Is Indexed</span></span>             | <span data-ttu-id="d4c85-186">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-186">False</span></span>                                            |
| <span data-ttu-id="d4c85-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4c85-187">In Global Catalog</span></span>      | <span data-ttu-id="d4c85-188">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-188">False</span></span>                                            |
| <span data-ttu-id="d4c85-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4c85-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4c85-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4c85-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d4c85-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4c85-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4c85-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-193">Search-Flags</span></span>           | <span data-ttu-id="d4c85-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4c85-194">0x00000000</span></span>                                       |
| <span data-ttu-id="d4c85-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-195">System-Flags</span></span>           | <span data-ttu-id="d4c85-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4c85-196">0x00000010</span></span>                                       |
| <span data-ttu-id="d4c85-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4c85-197">Classes used in</span></span>        | [<span data-ttu-id="d4c85-198">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d4c85-198">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d4c85-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d4c85-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d4c85-200">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-200">Entry</span></span> | <span data-ttu-id="d4c85-201">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d4c85-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4c85-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4c85-204">System-Only</span></span>            | <span data-ttu-id="d4c85-205">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-205">False</span></span>                                            |
| <span data-ttu-id="d4c85-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4c85-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d4c85-207">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-207">False</span></span>                                            |
| <span data-ttu-id="d4c85-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4c85-208">Is Indexed</span></span>             | <span data-ttu-id="d4c85-209">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-209">False</span></span>                                            |
| <span data-ttu-id="d4c85-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4c85-210">In Global Catalog</span></span>      | <span data-ttu-id="d4c85-211">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-211">False</span></span>                                            |
| <span data-ttu-id="d4c85-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4c85-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4c85-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4c85-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d4c85-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4c85-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4c85-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-216">Search-Flags</span></span>           | <span data-ttu-id="d4c85-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4c85-217">0x00000000</span></span>                                       |
| <span data-ttu-id="d4c85-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-218">System-Flags</span></span>           | <span data-ttu-id="d4c85-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4c85-219">0x00000010</span></span>                                       |
| <span data-ttu-id="d4c85-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4c85-220">Classes used in</span></span>        | [<span data-ttu-id="d4c85-221">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d4c85-221">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d4c85-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4c85-222">Windows Server 2008</span></span>



| <span data-ttu-id="d4c85-223">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-223">Entry</span></span> | <span data-ttu-id="d4c85-224">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d4c85-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4c85-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4c85-227">System-Only</span></span>            | <span data-ttu-id="d4c85-228">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-228">False</span></span>                                            |
| <span data-ttu-id="d4c85-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4c85-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d4c85-230">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-230">False</span></span>                                            |
| <span data-ttu-id="d4c85-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4c85-231">Is Indexed</span></span>             | <span data-ttu-id="d4c85-232">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-232">False</span></span>                                            |
| <span data-ttu-id="d4c85-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4c85-233">In Global Catalog</span></span>      | <span data-ttu-id="d4c85-234">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-234">False</span></span>                                            |
| <span data-ttu-id="d4c85-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4c85-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4c85-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4c85-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d4c85-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4c85-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4c85-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-239">Search-Flags</span></span>           | <span data-ttu-id="d4c85-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4c85-240">0x00000000</span></span>                                       |
| <span data-ttu-id="d4c85-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-241">System-Flags</span></span>           | <span data-ttu-id="d4c85-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4c85-242">0x00000010</span></span>                                       |
| <span data-ttu-id="d4c85-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4c85-243">Classes used in</span></span>        | [<span data-ttu-id="d4c85-244">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d4c85-244">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d4c85-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d4c85-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d4c85-246">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-246">Entry</span></span> | <span data-ttu-id="d4c85-247">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d4c85-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4c85-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4c85-250">System-Only</span></span>            | <span data-ttu-id="d4c85-251">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-251">False</span></span>                                            |
| <span data-ttu-id="d4c85-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4c85-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d4c85-253">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-253">False</span></span>                                            |
| <span data-ttu-id="d4c85-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4c85-254">Is Indexed</span></span>             | <span data-ttu-id="d4c85-255">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-255">False</span></span>                                            |
| <span data-ttu-id="d4c85-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4c85-256">In Global Catalog</span></span>      | <span data-ttu-id="d4c85-257">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-257">False</span></span>                                            |
| <span data-ttu-id="d4c85-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4c85-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4c85-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4c85-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d4c85-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4c85-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4c85-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-262">Search-Flags</span></span>           | <span data-ttu-id="d4c85-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4c85-263">0x00000000</span></span>                                       |
| <span data-ttu-id="d4c85-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-264">System-Flags</span></span>           | <span data-ttu-id="d4c85-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4c85-265">0x00000010</span></span>                                       |
| <span data-ttu-id="d4c85-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4c85-266">Classes used in</span></span>        | [<span data-ttu-id="d4c85-267">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d4c85-267">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d4c85-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4c85-268">Windows Server 2012</span></span>



| <span data-ttu-id="d4c85-269">進入</span><span class="sxs-lookup"><span data-stu-id="d4c85-269">Entry</span></span> | <span data-ttu-id="d4c85-270">值</span><span class="sxs-lookup"><span data-stu-id="d4c85-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d4c85-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d4c85-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d4c85-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d4c85-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="d4c85-273">System-Only</span></span>            | <span data-ttu-id="d4c85-274">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-274">False</span></span>                                            |
| <span data-ttu-id="d4c85-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d4c85-275">Is-Single-Valued</span></span>       | <span data-ttu-id="d4c85-276">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-276">False</span></span>                                            |
| <span data-ttu-id="d4c85-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d4c85-277">Is Indexed</span></span>             | <span data-ttu-id="d4c85-278">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-278">False</span></span>                                            |
| <span data-ttu-id="d4c85-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d4c85-279">In Global Catalog</span></span>      | <span data-ttu-id="d4c85-280">否</span><span class="sxs-lookup"><span data-stu-id="d4c85-280">False</span></span>                                            |
| <span data-ttu-id="d4c85-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d4c85-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="d4c85-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d4c85-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d4c85-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d4c85-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d4c85-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d4c85-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-285">Search-Flags</span></span>           | <span data-ttu-id="d4c85-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d4c85-286">0x00000000</span></span>                                       |
| <span data-ttu-id="d4c85-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d4c85-287">System-Flags</span></span>           | <span data-ttu-id="d4c85-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4c85-288">0x00000010</span></span>                                       |
| <span data-ttu-id="d4c85-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d4c85-289">Classes used in</span></span>        | [<span data-ttu-id="d4c85-290">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d4c85-290">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



 

 





