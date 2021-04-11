---
title: 全網域原則屬性
description: 這是為了將使用者可延伸的原則複寫到用戶端。
ms.assetid: 930a2733-31c4-45de-a611-437e3d61d304
ms.tgt_platform: multiple
keywords:
- 全網域原則屬性 AD 架構
- domainWidePolicy 屬性 AD 架構
topic_type:
- apiref
api_name:
- Domain-Wide-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc732ee761ee6c294ffb14dac832c36d5821927
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686803"
---
# <a name="domain-wide-policy-attribute"></a><span data-ttu-id="b8051-105">全網域原則屬性</span><span class="sxs-lookup"><span data-stu-id="b8051-105">Domain-Wide-Policy attribute</span></span>

<span data-ttu-id="b8051-106">這是為了將使用者可延伸的原則複寫到用戶端。</span><span class="sxs-lookup"><span data-stu-id="b8051-106">This is for user extensible policy to be replicated to the clients.</span></span>



| <span data-ttu-id="b8051-107">進入</span><span class="sxs-lookup"><span data-stu-id="b8051-107">Entry</span></span> | <span data-ttu-id="b8051-108">值</span><span class="sxs-lookup"><span data-stu-id="b8051-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b8051-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8051-109">CN</span></span>                | <span data-ttu-id="b8051-110">全網域原則</span><span class="sxs-lookup"><span data-stu-id="b8051-110">Domain-Wide-Policy</span></span>                                    |
| <span data-ttu-id="b8051-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b8051-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8051-112">domainWidePolicy</span><span class="sxs-lookup"><span data-stu-id="b8051-112">domainWidePolicy</span></span>                                      |
| <span data-ttu-id="b8051-113">大小</span><span class="sxs-lookup"><span data-stu-id="b8051-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b8051-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b8051-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b8051-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b8051-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b8051-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8051-116">Attribute-Id</span></span>      | <span data-ttu-id="b8051-117">1.2.840.113556.1.4.421</span><span class="sxs-lookup"><span data-stu-id="b8051-117">1.2.840.113556.1.4.421</span></span>                                |
| <span data-ttu-id="b8051-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b8051-118">System-Id-Guid</span></span>    | <span data-ttu-id="b8051-119">80a67e29-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="b8051-119">80a67e29-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="b8051-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8051-120">Syntax</span></span>            | [<span data-ttu-id="b8051-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b8051-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b8051-122">實作</span><span class="sxs-lookup"><span data-stu-id="b8051-122">Implementations</span></span>

-   [<span data-ttu-id="b8051-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8051-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8051-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8051-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8051-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8051-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8051-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8051-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8051-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8051-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8051-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8051-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8051-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8051-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b8051-130">進入</span><span class="sxs-lookup"><span data-stu-id="b8051-130">Entry</span></span> | <span data-ttu-id="b8051-131">值</span><span class="sxs-lookup"><span data-stu-id="b8051-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b8051-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8051-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8051-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8051-134">System-Only</span></span>            | <span data-ttu-id="b8051-135">否</span><span class="sxs-lookup"><span data-stu-id="b8051-135">False</span></span>                                              |
| <span data-ttu-id="b8051-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8051-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b8051-137">否</span><span class="sxs-lookup"><span data-stu-id="b8051-137">False</span></span>                                              |
| <span data-ttu-id="b8051-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8051-138">Is Indexed</span></span>             | <span data-ttu-id="b8051-139">否</span><span class="sxs-lookup"><span data-stu-id="b8051-139">False</span></span>                                              |
| <span data-ttu-id="b8051-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8051-140">In Global Catalog</span></span>      | <span data-ttu-id="b8051-141">否</span><span class="sxs-lookup"><span data-stu-id="b8051-141">False</span></span>                                              |
| <span data-ttu-id="b8051-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8051-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8051-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8051-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b8051-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8051-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8051-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-146">Search-Flags</span></span>           | <span data-ttu-id="b8051-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8051-147">0x00000000</span></span>                                         |
| <span data-ttu-id="b8051-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-148">System-Flags</span></span>           | <span data-ttu-id="b8051-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8051-149">0x00000010</span></span>                                         |
| <span data-ttu-id="b8051-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8051-150">Classes used in</span></span>        | [<span data-ttu-id="b8051-151">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b8051-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8051-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8051-152">Windows Server 2003</span></span>



| <span data-ttu-id="b8051-153">進入</span><span class="sxs-lookup"><span data-stu-id="b8051-153">Entry</span></span> | <span data-ttu-id="b8051-154">值</span><span class="sxs-lookup"><span data-stu-id="b8051-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b8051-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8051-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8051-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8051-157">System-Only</span></span>            | <span data-ttu-id="b8051-158">否</span><span class="sxs-lookup"><span data-stu-id="b8051-158">False</span></span>                                              |
| <span data-ttu-id="b8051-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8051-159">Is-Single-Valued</span></span>       | <span data-ttu-id="b8051-160">否</span><span class="sxs-lookup"><span data-stu-id="b8051-160">False</span></span>                                              |
| <span data-ttu-id="b8051-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8051-161">Is Indexed</span></span>             | <span data-ttu-id="b8051-162">否</span><span class="sxs-lookup"><span data-stu-id="b8051-162">False</span></span>                                              |
| <span data-ttu-id="b8051-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8051-163">In Global Catalog</span></span>      | <span data-ttu-id="b8051-164">否</span><span class="sxs-lookup"><span data-stu-id="b8051-164">False</span></span>                                              |
| <span data-ttu-id="b8051-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8051-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8051-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8051-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b8051-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8051-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8051-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-169">Search-Flags</span></span>           | <span data-ttu-id="b8051-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8051-170">0x00000000</span></span>                                         |
| <span data-ttu-id="b8051-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-171">System-Flags</span></span>           | <span data-ttu-id="b8051-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8051-172">0x00000010</span></span>                                         |
| <span data-ttu-id="b8051-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8051-173">Classes used in</span></span>        | [<span data-ttu-id="b8051-174">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b8051-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8051-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8051-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8051-176">進入</span><span class="sxs-lookup"><span data-stu-id="b8051-176">Entry</span></span> | <span data-ttu-id="b8051-177">值</span><span class="sxs-lookup"><span data-stu-id="b8051-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b8051-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8051-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8051-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8051-180">System-Only</span></span>            | <span data-ttu-id="b8051-181">否</span><span class="sxs-lookup"><span data-stu-id="b8051-181">False</span></span>                                              |
| <span data-ttu-id="b8051-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8051-182">Is-Single-Valued</span></span>       | <span data-ttu-id="b8051-183">否</span><span class="sxs-lookup"><span data-stu-id="b8051-183">False</span></span>                                              |
| <span data-ttu-id="b8051-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8051-184">Is Indexed</span></span>             | <span data-ttu-id="b8051-185">否</span><span class="sxs-lookup"><span data-stu-id="b8051-185">False</span></span>                                              |
| <span data-ttu-id="b8051-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8051-186">In Global Catalog</span></span>      | <span data-ttu-id="b8051-187">否</span><span class="sxs-lookup"><span data-stu-id="b8051-187">False</span></span>                                              |
| <span data-ttu-id="b8051-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8051-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8051-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8051-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b8051-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8051-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8051-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-192">Search-Flags</span></span>           | <span data-ttu-id="b8051-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8051-193">0x00000000</span></span>                                         |
| <span data-ttu-id="b8051-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-194">System-Flags</span></span>           | <span data-ttu-id="b8051-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8051-195">0x00000010</span></span>                                         |
| <span data-ttu-id="b8051-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8051-196">Classes used in</span></span>        | [<span data-ttu-id="b8051-197">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b8051-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8051-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8051-198">Windows Server 2008</span></span>



| <span data-ttu-id="b8051-199">進入</span><span class="sxs-lookup"><span data-stu-id="b8051-199">Entry</span></span> | <span data-ttu-id="b8051-200">值</span><span class="sxs-lookup"><span data-stu-id="b8051-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b8051-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8051-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8051-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8051-203">System-Only</span></span>            | <span data-ttu-id="b8051-204">否</span><span class="sxs-lookup"><span data-stu-id="b8051-204">False</span></span>                                              |
| <span data-ttu-id="b8051-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8051-205">Is-Single-Valued</span></span>       | <span data-ttu-id="b8051-206">否</span><span class="sxs-lookup"><span data-stu-id="b8051-206">False</span></span>                                              |
| <span data-ttu-id="b8051-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8051-207">Is Indexed</span></span>             | <span data-ttu-id="b8051-208">否</span><span class="sxs-lookup"><span data-stu-id="b8051-208">False</span></span>                                              |
| <span data-ttu-id="b8051-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8051-209">In Global Catalog</span></span>      | <span data-ttu-id="b8051-210">否</span><span class="sxs-lookup"><span data-stu-id="b8051-210">False</span></span>                                              |
| <span data-ttu-id="b8051-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8051-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8051-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8051-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b8051-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8051-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8051-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-215">Search-Flags</span></span>           | <span data-ttu-id="b8051-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8051-216">0x00000000</span></span>                                         |
| <span data-ttu-id="b8051-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-217">System-Flags</span></span>           | <span data-ttu-id="b8051-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8051-218">0x00000010</span></span>                                         |
| <span data-ttu-id="b8051-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8051-219">Classes used in</span></span>        | [<span data-ttu-id="b8051-220">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b8051-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8051-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8051-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8051-222">進入</span><span class="sxs-lookup"><span data-stu-id="b8051-222">Entry</span></span> | <span data-ttu-id="b8051-223">值</span><span class="sxs-lookup"><span data-stu-id="b8051-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b8051-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8051-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8051-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8051-226">System-Only</span></span>            | <span data-ttu-id="b8051-227">否</span><span class="sxs-lookup"><span data-stu-id="b8051-227">False</span></span>                                              |
| <span data-ttu-id="b8051-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8051-228">Is-Single-Valued</span></span>       | <span data-ttu-id="b8051-229">否</span><span class="sxs-lookup"><span data-stu-id="b8051-229">False</span></span>                                              |
| <span data-ttu-id="b8051-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8051-230">Is Indexed</span></span>             | <span data-ttu-id="b8051-231">否</span><span class="sxs-lookup"><span data-stu-id="b8051-231">False</span></span>                                              |
| <span data-ttu-id="b8051-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8051-232">In Global Catalog</span></span>      | <span data-ttu-id="b8051-233">否</span><span class="sxs-lookup"><span data-stu-id="b8051-233">False</span></span>                                              |
| <span data-ttu-id="b8051-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8051-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8051-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8051-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b8051-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8051-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8051-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-238">Search-Flags</span></span>           | <span data-ttu-id="b8051-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8051-239">0x00000000</span></span>                                         |
| <span data-ttu-id="b8051-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-240">System-Flags</span></span>           | <span data-ttu-id="b8051-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8051-241">0x00000010</span></span>                                         |
| <span data-ttu-id="b8051-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8051-242">Classes used in</span></span>        | [<span data-ttu-id="b8051-243">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b8051-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8051-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8051-244">Windows Server 2012</span></span>



| <span data-ttu-id="b8051-245">進入</span><span class="sxs-lookup"><span data-stu-id="b8051-245">Entry</span></span> | <span data-ttu-id="b8051-246">值</span><span class="sxs-lookup"><span data-stu-id="b8051-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b8051-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b8051-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8051-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b8051-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8051-249">System-Only</span></span>            | <span data-ttu-id="b8051-250">否</span><span class="sxs-lookup"><span data-stu-id="b8051-250">False</span></span>                                              |
| <span data-ttu-id="b8051-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b8051-251">Is-Single-Valued</span></span>       | <span data-ttu-id="b8051-252">否</span><span class="sxs-lookup"><span data-stu-id="b8051-252">False</span></span>                                              |
| <span data-ttu-id="b8051-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b8051-253">Is Indexed</span></span>             | <span data-ttu-id="b8051-254">否</span><span class="sxs-lookup"><span data-stu-id="b8051-254">False</span></span>                                              |
| <span data-ttu-id="b8051-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b8051-255">In Global Catalog</span></span>      | <span data-ttu-id="b8051-256">否</span><span class="sxs-lookup"><span data-stu-id="b8051-256">False</span></span>                                              |
| <span data-ttu-id="b8051-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b8051-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8051-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b8051-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b8051-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8051-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8051-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b8051-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-261">Search-Flags</span></span>           | <span data-ttu-id="b8051-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8051-262">0x00000000</span></span>                                         |
| <span data-ttu-id="b8051-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8051-263">System-Flags</span></span>           | <span data-ttu-id="b8051-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8051-264">0x00000010</span></span>                                         |
| <span data-ttu-id="b8051-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b8051-265">Classes used in</span></span>        | [<span data-ttu-id="b8051-266">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b8051-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





