---
title: LDAP-IPDeny-List 屬性
description: 保存拒絕 LDAP 伺服器存取的二進位 IP 位址清單。
ms.assetid: 7d554d49-8934-4d71-b32f-8e59c22faf8c
ms.tgt_platform: multiple
keywords:
- LDAP-IPDeny-List 屬性 AD 架構
- lDAPIPDenyList 屬性 AD 架構
topic_type:
- apiref
api_name:
- LDAP-IPDeny-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43246b5bb5786eefafc8598e9d729d9a2f308e08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107893"
---
# <a name="ldap-ipdeny-list-attribute"></a><span data-ttu-id="d6afc-105">LDAP-IPDeny-List 屬性</span><span class="sxs-lookup"><span data-stu-id="d6afc-105">LDAP-IPDeny-List attribute</span></span>

<span data-ttu-id="d6afc-106">保存拒絕 LDAP 伺服器存取的二進位 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="d6afc-106">Holds a list of binary IP addresses that are denied access to an LDAP server.</span></span>



| <span data-ttu-id="d6afc-107">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-107">Entry</span></span> | <span data-ttu-id="d6afc-108">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d6afc-109">CN</span><span class="sxs-lookup"><span data-stu-id="d6afc-109">CN</span></span>                | <span data-ttu-id="d6afc-110">LDAP-IPDeny-清單</span><span class="sxs-lookup"><span data-stu-id="d6afc-110">LDAP-IPDeny-List</span></span>                                      |
| <span data-ttu-id="d6afc-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d6afc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d6afc-112">lDAPIPDenyList</span><span class="sxs-lookup"><span data-stu-id="d6afc-112">lDAPIPDenyList</span></span>                                        |
| <span data-ttu-id="d6afc-113">大小</span><span class="sxs-lookup"><span data-stu-id="d6afc-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="d6afc-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d6afc-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="d6afc-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d6afc-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="d6afc-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-116">Attribute-Id</span></span>      | <span data-ttu-id="d6afc-117">1.2.840.113556.1.4.844</span><span class="sxs-lookup"><span data-stu-id="d6afc-117">1.2.840.113556.1.4.844</span></span>                                |
| <span data-ttu-id="d6afc-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d6afc-118">System-Id-Guid</span></span>    | <span data-ttu-id="d6afc-119">7359a353-90f7-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d6afc-119">7359a353-90f7-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="d6afc-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6afc-120">Syntax</span></span>            | [<span data-ttu-id="d6afc-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="d6afc-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="d6afc-122">實作</span><span class="sxs-lookup"><span data-stu-id="d6afc-122">Implementations</span></span>

-   [<span data-ttu-id="d6afc-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d6afc-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d6afc-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d6afc-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d6afc-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="d6afc-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d6afc-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d6afc-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d6afc-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d6afc-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d6afc-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d6afc-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d6afc-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d6afc-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d6afc-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d6afc-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d6afc-131">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-131">Entry</span></span> | <span data-ttu-id="d6afc-132">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-132">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d6afc-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d6afc-133">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-134">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6afc-135">System-Only</span></span>            | <span data-ttu-id="d6afc-136">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-136">False</span></span>                                            |
| <span data-ttu-id="d6afc-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d6afc-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d6afc-138">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-138">False</span></span>                                            |
| <span data-ttu-id="d6afc-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d6afc-139">Is Indexed</span></span>             | <span data-ttu-id="d6afc-140">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-140">False</span></span>                                            |
| <span data-ttu-id="d6afc-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d6afc-141">In Global Catalog</span></span>      | <span data-ttu-id="d6afc-142">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-142">False</span></span>                                            |
| <span data-ttu-id="d6afc-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d6afc-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6afc-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d6afc-144">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d6afc-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6afc-145">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6afc-146">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-147">Search-Flags</span></span>           | <span data-ttu-id="d6afc-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6afc-148">0x00000000</span></span>                                       |
| <span data-ttu-id="d6afc-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-149">System-Flags</span></span>           | <span data-ttu-id="d6afc-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6afc-150">0x00000010</span></span>                                       |
| <span data-ttu-id="d6afc-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d6afc-151">Classes used in</span></span>        | [<span data-ttu-id="d6afc-152">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d6afc-152">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d6afc-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6afc-153">Windows Server 2003</span></span>



| <span data-ttu-id="d6afc-154">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-154">Entry</span></span> | <span data-ttu-id="d6afc-155">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-155">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d6afc-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d6afc-156">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-157">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6afc-158">System-Only</span></span>            | <span data-ttu-id="d6afc-159">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-159">False</span></span>                                            |
| <span data-ttu-id="d6afc-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d6afc-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d6afc-161">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-161">False</span></span>                                            |
| <span data-ttu-id="d6afc-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d6afc-162">Is Indexed</span></span>             | <span data-ttu-id="d6afc-163">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-163">False</span></span>                                            |
| <span data-ttu-id="d6afc-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d6afc-164">In Global Catalog</span></span>      | <span data-ttu-id="d6afc-165">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-165">False</span></span>                                            |
| <span data-ttu-id="d6afc-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d6afc-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6afc-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d6afc-167">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d6afc-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6afc-168">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6afc-169">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-170">Search-Flags</span></span>           | <span data-ttu-id="d6afc-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6afc-171">0x00000000</span></span>                                       |
| <span data-ttu-id="d6afc-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-172">System-Flags</span></span>           | <span data-ttu-id="d6afc-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6afc-173">0x00000010</span></span>                                       |
| <span data-ttu-id="d6afc-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d6afc-174">Classes used in</span></span>        | [<span data-ttu-id="d6afc-175">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d6afc-175">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d6afc-176">亞當</span><span class="sxs-lookup"><span data-stu-id="d6afc-176">ADAM</span></span>



| <span data-ttu-id="d6afc-177">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-177">Entry</span></span> | <span data-ttu-id="d6afc-178">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-178">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d6afc-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d6afc-179">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-180">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6afc-181">System-Only</span></span>            | <span data-ttu-id="d6afc-182">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-182">False</span></span>                                            |
| <span data-ttu-id="d6afc-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d6afc-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d6afc-184">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-184">False</span></span>                                            |
| <span data-ttu-id="d6afc-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d6afc-185">Is Indexed</span></span>             | <span data-ttu-id="d6afc-186">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-186">False</span></span>                                            |
| <span data-ttu-id="d6afc-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d6afc-187">In Global Catalog</span></span>      | <span data-ttu-id="d6afc-188">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-188">False</span></span>                                            |
| <span data-ttu-id="d6afc-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d6afc-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6afc-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d6afc-190">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d6afc-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6afc-191">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6afc-192">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-193">Search-Flags</span></span>           | <span data-ttu-id="d6afc-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6afc-194">0x00000000</span></span>                                       |
| <span data-ttu-id="d6afc-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-195">System-Flags</span></span>           | <span data-ttu-id="d6afc-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6afc-196">0x00000010</span></span>                                       |
| <span data-ttu-id="d6afc-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d6afc-197">Classes used in</span></span>        | [<span data-ttu-id="d6afc-198">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d6afc-198">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d6afc-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d6afc-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d6afc-200">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-200">Entry</span></span> | <span data-ttu-id="d6afc-201">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-201">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d6afc-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d6afc-202">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-203">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6afc-204">System-Only</span></span>            | <span data-ttu-id="d6afc-205">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-205">False</span></span>                                            |
| <span data-ttu-id="d6afc-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d6afc-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d6afc-207">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-207">False</span></span>                                            |
| <span data-ttu-id="d6afc-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d6afc-208">Is Indexed</span></span>             | <span data-ttu-id="d6afc-209">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-209">False</span></span>                                            |
| <span data-ttu-id="d6afc-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d6afc-210">In Global Catalog</span></span>      | <span data-ttu-id="d6afc-211">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-211">False</span></span>                                            |
| <span data-ttu-id="d6afc-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d6afc-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6afc-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d6afc-213">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d6afc-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6afc-214">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6afc-215">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-216">Search-Flags</span></span>           | <span data-ttu-id="d6afc-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6afc-217">0x00000000</span></span>                                       |
| <span data-ttu-id="d6afc-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-218">System-Flags</span></span>           | <span data-ttu-id="d6afc-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6afc-219">0x00000010</span></span>                                       |
| <span data-ttu-id="d6afc-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d6afc-220">Classes used in</span></span>        | [<span data-ttu-id="d6afc-221">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d6afc-221">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d6afc-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6afc-222">Windows Server 2008</span></span>



| <span data-ttu-id="d6afc-223">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-223">Entry</span></span> | <span data-ttu-id="d6afc-224">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-224">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d6afc-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d6afc-225">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-226">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6afc-227">System-Only</span></span>            | <span data-ttu-id="d6afc-228">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-228">False</span></span>                                            |
| <span data-ttu-id="d6afc-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d6afc-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d6afc-230">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-230">False</span></span>                                            |
| <span data-ttu-id="d6afc-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d6afc-231">Is Indexed</span></span>             | <span data-ttu-id="d6afc-232">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-232">False</span></span>                                            |
| <span data-ttu-id="d6afc-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d6afc-233">In Global Catalog</span></span>      | <span data-ttu-id="d6afc-234">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-234">False</span></span>                                            |
| <span data-ttu-id="d6afc-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d6afc-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6afc-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d6afc-236">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d6afc-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6afc-237">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6afc-238">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-239">Search-Flags</span></span>           | <span data-ttu-id="d6afc-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6afc-240">0x00000000</span></span>                                       |
| <span data-ttu-id="d6afc-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-241">System-Flags</span></span>           | <span data-ttu-id="d6afc-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6afc-242">0x00000010</span></span>                                       |
| <span data-ttu-id="d6afc-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d6afc-243">Classes used in</span></span>        | [<span data-ttu-id="d6afc-244">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d6afc-244">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d6afc-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d6afc-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d6afc-246">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-246">Entry</span></span> | <span data-ttu-id="d6afc-247">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-247">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d6afc-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d6afc-248">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-249">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6afc-250">System-Only</span></span>            | <span data-ttu-id="d6afc-251">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-251">False</span></span>                                            |
| <span data-ttu-id="d6afc-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d6afc-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d6afc-253">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-253">False</span></span>                                            |
| <span data-ttu-id="d6afc-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d6afc-254">Is Indexed</span></span>             | <span data-ttu-id="d6afc-255">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-255">False</span></span>                                            |
| <span data-ttu-id="d6afc-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d6afc-256">In Global Catalog</span></span>      | <span data-ttu-id="d6afc-257">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-257">False</span></span>                                            |
| <span data-ttu-id="d6afc-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d6afc-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6afc-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d6afc-259">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d6afc-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6afc-260">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6afc-261">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-262">Search-Flags</span></span>           | <span data-ttu-id="d6afc-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6afc-263">0x00000000</span></span>                                       |
| <span data-ttu-id="d6afc-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-264">System-Flags</span></span>           | <span data-ttu-id="d6afc-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6afc-265">0x00000010</span></span>                                       |
| <span data-ttu-id="d6afc-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d6afc-266">Classes used in</span></span>        | [<span data-ttu-id="d6afc-267">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d6afc-267">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d6afc-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d6afc-268">Windows Server 2012</span></span>



| <span data-ttu-id="d6afc-269">進入</span><span class="sxs-lookup"><span data-stu-id="d6afc-269">Entry</span></span> | <span data-ttu-id="d6afc-270">值</span><span class="sxs-lookup"><span data-stu-id="d6afc-270">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d6afc-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d6afc-271">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d6afc-272">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d6afc-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="d6afc-273">System-Only</span></span>            | <span data-ttu-id="d6afc-274">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-274">False</span></span>                                            |
| <span data-ttu-id="d6afc-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d6afc-275">Is-Single-Valued</span></span>       | <span data-ttu-id="d6afc-276">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-276">False</span></span>                                            |
| <span data-ttu-id="d6afc-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d6afc-277">Is Indexed</span></span>             | <span data-ttu-id="d6afc-278">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-278">False</span></span>                                            |
| <span data-ttu-id="d6afc-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d6afc-279">In Global Catalog</span></span>      | <span data-ttu-id="d6afc-280">否</span><span class="sxs-lookup"><span data-stu-id="d6afc-280">False</span></span>                                            |
| <span data-ttu-id="d6afc-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d6afc-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="d6afc-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d6afc-282">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d6afc-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d6afc-283">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d6afc-284">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d6afc-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-285">Search-Flags</span></span>           | <span data-ttu-id="d6afc-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6afc-286">0x00000000</span></span>                                       |
| <span data-ttu-id="d6afc-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d6afc-287">System-Flags</span></span>           | <span data-ttu-id="d6afc-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d6afc-288">0x00000010</span></span>                                       |
| <span data-ttu-id="d6afc-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d6afc-289">Classes used in</span></span>        | [<span data-ttu-id="d6afc-290">**查詢原則**</span><span class="sxs-lookup"><span data-stu-id="d6afc-290">**Query-Policy**</span></span>](c-querypolicy.md)<br/> |



 

 





