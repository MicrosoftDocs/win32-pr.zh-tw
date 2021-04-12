---
title: 網域原則參考屬性
description: 原則物件從中複製之網域原則物件的分辨名稱。
ms.assetid: 914920de-6dc2-4dda-bf10-a34f5315eb74
ms.tgt_platform: multiple
keywords:
- 網域原則-參考屬性 AD 架構
- domainPolicyReference 屬性 AD 架構
topic_type:
- apiref
api_name:
- Domain-Policy-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9723abde3bd04dc9c50f6b4c00f1ed80c4da0c2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935254"
---
# <a name="domain-policy-reference-attribute"></a><span data-ttu-id="971e0-105">網域原則參考屬性</span><span class="sxs-lookup"><span data-stu-id="971e0-105">Domain-Policy-Reference attribute</span></span>

<span data-ttu-id="971e0-106">原則物件從中複製之網域原則物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="971e0-106">The Distinguished Name of a domain policy object that a policy object copies from.</span></span>



| <span data-ttu-id="971e0-107">進入</span><span class="sxs-lookup"><span data-stu-id="971e0-107">Entry</span></span> | <span data-ttu-id="971e0-108">值</span><span class="sxs-lookup"><span data-stu-id="971e0-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="971e0-109">CN</span><span class="sxs-lookup"><span data-stu-id="971e0-109">CN</span></span>                | <span data-ttu-id="971e0-110">網域原則-參考</span><span class="sxs-lookup"><span data-stu-id="971e0-110">Domain-Policy-Reference</span></span>                 |
| <span data-ttu-id="971e0-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="971e0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="971e0-112">domainPolicyReference</span><span class="sxs-lookup"><span data-stu-id="971e0-112">domainPolicyReference</span></span>                   |
| <span data-ttu-id="971e0-113">大小</span><span class="sxs-lookup"><span data-stu-id="971e0-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="971e0-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="971e0-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="971e0-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="971e0-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="971e0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="971e0-116">Attribute-Id</span></span>      | <span data-ttu-id="971e0-117">1.2.840.113556.1.4.422</span><span class="sxs-lookup"><span data-stu-id="971e0-117">1.2.840.113556.1.4.422</span></span>                  |
| <span data-ttu-id="971e0-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="971e0-118">System-Id-Guid</span></span>    | <span data-ttu-id="971e0-119">80a67e2a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="971e0-119">80a67e2a-9f22-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="971e0-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="971e0-120">Syntax</span></span>            | [<span data-ttu-id="971e0-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="971e0-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="971e0-122">實作</span><span class="sxs-lookup"><span data-stu-id="971e0-122">Implementations</span></span>

-   [<span data-ttu-id="971e0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="971e0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="971e0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="971e0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="971e0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="971e0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="971e0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="971e0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="971e0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="971e0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="971e0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="971e0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="971e0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="971e0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="971e0-130">進入</span><span class="sxs-lookup"><span data-stu-id="971e0-130">Entry</span></span> | <span data-ttu-id="971e0-131">值</span><span class="sxs-lookup"><span data-stu-id="971e0-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="971e0-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="971e0-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="971e0-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="971e0-134">System-Only</span></span>            | <span data-ttu-id="971e0-135">否</span><span class="sxs-lookup"><span data-stu-id="971e0-135">False</span></span>                                              |
| <span data-ttu-id="971e0-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="971e0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="971e0-137">對</span><span class="sxs-lookup"><span data-stu-id="971e0-137">True</span></span>                                               |
| <span data-ttu-id="971e0-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="971e0-138">Is Indexed</span></span>             | <span data-ttu-id="971e0-139">否</span><span class="sxs-lookup"><span data-stu-id="971e0-139">False</span></span>                                              |
| <span data-ttu-id="971e0-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="971e0-140">In Global Catalog</span></span>      | <span data-ttu-id="971e0-141">否</span><span class="sxs-lookup"><span data-stu-id="971e0-141">False</span></span>                                              |
| <span data-ttu-id="971e0-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="971e0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="971e0-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="971e0-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="971e0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="971e0-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="971e0-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-146">Search-Flags</span></span>           | <span data-ttu-id="971e0-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="971e0-147">0x00000000</span></span>                                         |
| <span data-ttu-id="971e0-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-148">System-Flags</span></span>           | <span data-ttu-id="971e0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="971e0-149">0x00000010</span></span>                                         |
| <span data-ttu-id="971e0-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="971e0-150">Classes used in</span></span>        | [<span data-ttu-id="971e0-151">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="971e0-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="971e0-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="971e0-152">Windows Server 2003</span></span>



| <span data-ttu-id="971e0-153">進入</span><span class="sxs-lookup"><span data-stu-id="971e0-153">Entry</span></span> | <span data-ttu-id="971e0-154">值</span><span class="sxs-lookup"><span data-stu-id="971e0-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="971e0-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="971e0-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="971e0-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="971e0-157">System-Only</span></span>            | <span data-ttu-id="971e0-158">否</span><span class="sxs-lookup"><span data-stu-id="971e0-158">False</span></span>                                              |
| <span data-ttu-id="971e0-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="971e0-159">Is-Single-Valued</span></span>       | <span data-ttu-id="971e0-160">對</span><span class="sxs-lookup"><span data-stu-id="971e0-160">True</span></span>                                               |
| <span data-ttu-id="971e0-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="971e0-161">Is Indexed</span></span>             | <span data-ttu-id="971e0-162">否</span><span class="sxs-lookup"><span data-stu-id="971e0-162">False</span></span>                                              |
| <span data-ttu-id="971e0-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="971e0-163">In Global Catalog</span></span>      | <span data-ttu-id="971e0-164">否</span><span class="sxs-lookup"><span data-stu-id="971e0-164">False</span></span>                                              |
| <span data-ttu-id="971e0-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="971e0-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="971e0-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="971e0-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="971e0-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="971e0-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="971e0-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-169">Search-Flags</span></span>           | <span data-ttu-id="971e0-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="971e0-170">0x00000000</span></span>                                         |
| <span data-ttu-id="971e0-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-171">System-Flags</span></span>           | <span data-ttu-id="971e0-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="971e0-172">0x00000010</span></span>                                         |
| <span data-ttu-id="971e0-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="971e0-173">Classes used in</span></span>        | [<span data-ttu-id="971e0-174">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="971e0-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="971e0-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="971e0-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="971e0-176">進入</span><span class="sxs-lookup"><span data-stu-id="971e0-176">Entry</span></span> | <span data-ttu-id="971e0-177">值</span><span class="sxs-lookup"><span data-stu-id="971e0-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="971e0-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="971e0-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="971e0-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="971e0-180">System-Only</span></span>            | <span data-ttu-id="971e0-181">否</span><span class="sxs-lookup"><span data-stu-id="971e0-181">False</span></span>                                              |
| <span data-ttu-id="971e0-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="971e0-182">Is-Single-Valued</span></span>       | <span data-ttu-id="971e0-183">對</span><span class="sxs-lookup"><span data-stu-id="971e0-183">True</span></span>                                               |
| <span data-ttu-id="971e0-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="971e0-184">Is Indexed</span></span>             | <span data-ttu-id="971e0-185">否</span><span class="sxs-lookup"><span data-stu-id="971e0-185">False</span></span>                                              |
| <span data-ttu-id="971e0-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="971e0-186">In Global Catalog</span></span>      | <span data-ttu-id="971e0-187">否</span><span class="sxs-lookup"><span data-stu-id="971e0-187">False</span></span>                                              |
| <span data-ttu-id="971e0-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="971e0-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="971e0-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="971e0-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="971e0-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="971e0-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="971e0-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-192">Search-Flags</span></span>           | <span data-ttu-id="971e0-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="971e0-193">0x00000000</span></span>                                         |
| <span data-ttu-id="971e0-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-194">System-Flags</span></span>           | <span data-ttu-id="971e0-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="971e0-195">0x00000010</span></span>                                         |
| <span data-ttu-id="971e0-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="971e0-196">Classes used in</span></span>        | [<span data-ttu-id="971e0-197">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="971e0-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="971e0-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="971e0-198">Windows Server 2008</span></span>



| <span data-ttu-id="971e0-199">進入</span><span class="sxs-lookup"><span data-stu-id="971e0-199">Entry</span></span> | <span data-ttu-id="971e0-200">值</span><span class="sxs-lookup"><span data-stu-id="971e0-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="971e0-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="971e0-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="971e0-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="971e0-203">System-Only</span></span>            | <span data-ttu-id="971e0-204">否</span><span class="sxs-lookup"><span data-stu-id="971e0-204">False</span></span>                                              |
| <span data-ttu-id="971e0-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="971e0-205">Is-Single-Valued</span></span>       | <span data-ttu-id="971e0-206">對</span><span class="sxs-lookup"><span data-stu-id="971e0-206">True</span></span>                                               |
| <span data-ttu-id="971e0-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="971e0-207">Is Indexed</span></span>             | <span data-ttu-id="971e0-208">否</span><span class="sxs-lookup"><span data-stu-id="971e0-208">False</span></span>                                              |
| <span data-ttu-id="971e0-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="971e0-209">In Global Catalog</span></span>      | <span data-ttu-id="971e0-210">否</span><span class="sxs-lookup"><span data-stu-id="971e0-210">False</span></span>                                              |
| <span data-ttu-id="971e0-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="971e0-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="971e0-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="971e0-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="971e0-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="971e0-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="971e0-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-215">Search-Flags</span></span>           | <span data-ttu-id="971e0-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="971e0-216">0x00000000</span></span>                                         |
| <span data-ttu-id="971e0-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-217">System-Flags</span></span>           | <span data-ttu-id="971e0-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="971e0-218">0x00000010</span></span>                                         |
| <span data-ttu-id="971e0-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="971e0-219">Classes used in</span></span>        | [<span data-ttu-id="971e0-220">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="971e0-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="971e0-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="971e0-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="971e0-222">進入</span><span class="sxs-lookup"><span data-stu-id="971e0-222">Entry</span></span> | <span data-ttu-id="971e0-223">值</span><span class="sxs-lookup"><span data-stu-id="971e0-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="971e0-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="971e0-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="971e0-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="971e0-226">System-Only</span></span>            | <span data-ttu-id="971e0-227">否</span><span class="sxs-lookup"><span data-stu-id="971e0-227">False</span></span>                                              |
| <span data-ttu-id="971e0-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="971e0-228">Is-Single-Valued</span></span>       | <span data-ttu-id="971e0-229">對</span><span class="sxs-lookup"><span data-stu-id="971e0-229">True</span></span>                                               |
| <span data-ttu-id="971e0-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="971e0-230">Is Indexed</span></span>             | <span data-ttu-id="971e0-231">否</span><span class="sxs-lookup"><span data-stu-id="971e0-231">False</span></span>                                              |
| <span data-ttu-id="971e0-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="971e0-232">In Global Catalog</span></span>      | <span data-ttu-id="971e0-233">否</span><span class="sxs-lookup"><span data-stu-id="971e0-233">False</span></span>                                              |
| <span data-ttu-id="971e0-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="971e0-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="971e0-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="971e0-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="971e0-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="971e0-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="971e0-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-238">Search-Flags</span></span>           | <span data-ttu-id="971e0-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="971e0-239">0x00000000</span></span>                                         |
| <span data-ttu-id="971e0-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-240">System-Flags</span></span>           | <span data-ttu-id="971e0-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="971e0-241">0x00000010</span></span>                                         |
| <span data-ttu-id="971e0-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="971e0-242">Classes used in</span></span>        | [<span data-ttu-id="971e0-243">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="971e0-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="971e0-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="971e0-244">Windows Server 2012</span></span>



| <span data-ttu-id="971e0-245">進入</span><span class="sxs-lookup"><span data-stu-id="971e0-245">Entry</span></span> | <span data-ttu-id="971e0-246">值</span><span class="sxs-lookup"><span data-stu-id="971e0-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="971e0-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="971e0-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="971e0-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="971e0-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="971e0-249">System-Only</span></span>            | <span data-ttu-id="971e0-250">否</span><span class="sxs-lookup"><span data-stu-id="971e0-250">False</span></span>                                              |
| <span data-ttu-id="971e0-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="971e0-251">Is-Single-Valued</span></span>       | <span data-ttu-id="971e0-252">對</span><span class="sxs-lookup"><span data-stu-id="971e0-252">True</span></span>                                               |
| <span data-ttu-id="971e0-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="971e0-253">Is Indexed</span></span>             | <span data-ttu-id="971e0-254">否</span><span class="sxs-lookup"><span data-stu-id="971e0-254">False</span></span>                                              |
| <span data-ttu-id="971e0-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="971e0-255">In Global Catalog</span></span>      | <span data-ttu-id="971e0-256">否</span><span class="sxs-lookup"><span data-stu-id="971e0-256">False</span></span>                                              |
| <span data-ttu-id="971e0-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="971e0-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="971e0-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="971e0-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="971e0-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="971e0-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="971e0-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="971e0-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-261">Search-Flags</span></span>           | <span data-ttu-id="971e0-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="971e0-262">0x00000000</span></span>                                         |
| <span data-ttu-id="971e0-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="971e0-263">System-Flags</span></span>           | <span data-ttu-id="971e0-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="971e0-264">0x00000010</span></span>                                         |
| <span data-ttu-id="971e0-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="971e0-265">Classes used in</span></span>        | [<span data-ttu-id="971e0-266">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="971e0-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





