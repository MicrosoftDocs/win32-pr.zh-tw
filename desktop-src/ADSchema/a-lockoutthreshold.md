---
title: Lockout-Threshold 屬性
description: 帳戶遭到鎖定之前允許的無效登入嘗試次數。
ms.assetid: c4dcbbb6-0680-45f3-9b0b-f9c4bbf2b349
ms.tgt_platform: multiple
keywords:
- Lockout-Threshold 屬性 AD 架構
- lockoutThreshold 屬性 AD 架構
topic_type:
- apiref
api_name:
- Lockout-Threshold
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345977055597c48d70e30a20ce9bfbc9f07f3929
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844728"
---
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="8697f-105">Lockout-Threshold 屬性</span><span class="sxs-lookup"><span data-stu-id="8697f-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="8697f-106">帳戶遭到鎖定之前允許的無效登入嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="8697f-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="8697f-107">進入</span><span class="sxs-lookup"><span data-stu-id="8697f-107">Entry</span></span> | <span data-ttu-id="8697f-108">值</span><span class="sxs-lookup"><span data-stu-id="8697f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8697f-109">CN</span><span class="sxs-lookup"><span data-stu-id="8697f-109">CN</span></span>                | <span data-ttu-id="8697f-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="8697f-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="8697f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8697f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8697f-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="8697f-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="8697f-113">大小</span><span class="sxs-lookup"><span data-stu-id="8697f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8697f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8697f-114">Update Privilege</span></span>  | <span data-ttu-id="8697f-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="8697f-115">Domain administrator</span></span>                 |
| <span data-ttu-id="8697f-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8697f-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8697f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8697f-117">Attribute-Id</span></span>      | <span data-ttu-id="8697f-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="8697f-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="8697f-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8697f-119">System-Id-Guid</span></span>    | <span data-ttu-id="8697f-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8697f-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8697f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8697f-121">Syntax</span></span>            | [<span data-ttu-id="8697f-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="8697f-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8697f-123">實作</span><span class="sxs-lookup"><span data-stu-id="8697f-123">Implementations</span></span>

-   [<span data-ttu-id="8697f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8697f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8697f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8697f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8697f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8697f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8697f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8697f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8697f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8697f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8697f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8697f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8697f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8697f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8697f-131">進入</span><span class="sxs-lookup"><span data-stu-id="8697f-131">Entry</span></span> | <span data-ttu-id="8697f-132">值</span><span class="sxs-lookup"><span data-stu-id="8697f-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8697f-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8697f-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8697f-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8697f-135">System-Only</span></span>            | <span data-ttu-id="8697f-136">否</span><span class="sxs-lookup"><span data-stu-id="8697f-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8697f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8697f-138">對</span><span class="sxs-lookup"><span data-stu-id="8697f-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8697f-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8697f-139">Is Indexed</span></span>             | <span data-ttu-id="8697f-140">否</span><span class="sxs-lookup"><span data-stu-id="8697f-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8697f-141">In Global Catalog</span></span>      | <span data-ttu-id="8697f-142">否</span><span class="sxs-lookup"><span data-stu-id="8697f-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8697f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8697f-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8697f-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8697f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8697f-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8697f-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-147">Search-Flags</span></span>           | <span data-ttu-id="8697f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8697f-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-149">System-Flags</span></span>           | <span data-ttu-id="8697f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8697f-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8697f-151">Classes used in</span></span>        | [<span data-ttu-id="8697f-152">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="8697f-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8697f-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8697f-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8697f-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8697f-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8697f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8697f-155">Windows Server 2003</span></span>



| <span data-ttu-id="8697f-156">進入</span><span class="sxs-lookup"><span data-stu-id="8697f-156">Entry</span></span> | <span data-ttu-id="8697f-157">值</span><span class="sxs-lookup"><span data-stu-id="8697f-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8697f-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8697f-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8697f-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8697f-160">System-Only</span></span>            | <span data-ttu-id="8697f-161">否</span><span class="sxs-lookup"><span data-stu-id="8697f-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8697f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8697f-163">對</span><span class="sxs-lookup"><span data-stu-id="8697f-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8697f-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8697f-164">Is Indexed</span></span>             | <span data-ttu-id="8697f-165">否</span><span class="sxs-lookup"><span data-stu-id="8697f-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8697f-166">In Global Catalog</span></span>      | <span data-ttu-id="8697f-167">否</span><span class="sxs-lookup"><span data-stu-id="8697f-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8697f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8697f-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8697f-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8697f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8697f-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8697f-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-172">Search-Flags</span></span>           | <span data-ttu-id="8697f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8697f-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-174">System-Flags</span></span>           | <span data-ttu-id="8697f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8697f-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8697f-176">Classes used in</span></span>        | [<span data-ttu-id="8697f-177">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="8697f-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8697f-178">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8697f-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8697f-179">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8697f-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8697f-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8697f-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8697f-181">進入</span><span class="sxs-lookup"><span data-stu-id="8697f-181">Entry</span></span> | <span data-ttu-id="8697f-182">值</span><span class="sxs-lookup"><span data-stu-id="8697f-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8697f-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8697f-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8697f-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="8697f-185">System-Only</span></span>            | <span data-ttu-id="8697f-186">否</span><span class="sxs-lookup"><span data-stu-id="8697f-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8697f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="8697f-188">對</span><span class="sxs-lookup"><span data-stu-id="8697f-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8697f-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8697f-189">Is Indexed</span></span>             | <span data-ttu-id="8697f-190">否</span><span class="sxs-lookup"><span data-stu-id="8697f-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8697f-191">In Global Catalog</span></span>      | <span data-ttu-id="8697f-192">否</span><span class="sxs-lookup"><span data-stu-id="8697f-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8697f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="8697f-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8697f-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8697f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8697f-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8697f-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-197">Search-Flags</span></span>           | <span data-ttu-id="8697f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8697f-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-199">System-Flags</span></span>           | <span data-ttu-id="8697f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8697f-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8697f-201">Classes used in</span></span>        | [<span data-ttu-id="8697f-202">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="8697f-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8697f-203">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8697f-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8697f-204">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8697f-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8697f-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8697f-205">Windows Server 2008</span></span>



| <span data-ttu-id="8697f-206">進入</span><span class="sxs-lookup"><span data-stu-id="8697f-206">Entry</span></span> | <span data-ttu-id="8697f-207">值</span><span class="sxs-lookup"><span data-stu-id="8697f-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8697f-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8697f-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8697f-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="8697f-210">System-Only</span></span>            | <span data-ttu-id="8697f-211">否</span><span class="sxs-lookup"><span data-stu-id="8697f-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8697f-212">Is-Single-Valued</span></span>       | <span data-ttu-id="8697f-213">對</span><span class="sxs-lookup"><span data-stu-id="8697f-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8697f-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8697f-214">Is Indexed</span></span>             | <span data-ttu-id="8697f-215">否</span><span class="sxs-lookup"><span data-stu-id="8697f-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8697f-216">In Global Catalog</span></span>      | <span data-ttu-id="8697f-217">否</span><span class="sxs-lookup"><span data-stu-id="8697f-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8697f-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="8697f-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8697f-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8697f-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8697f-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8697f-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-222">Search-Flags</span></span>           | <span data-ttu-id="8697f-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8697f-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-224">System-Flags</span></span>           | <span data-ttu-id="8697f-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8697f-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8697f-226">Classes used in</span></span>        | [<span data-ttu-id="8697f-227">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="8697f-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8697f-228">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8697f-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8697f-229">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8697f-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8697f-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8697f-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8697f-231">進入</span><span class="sxs-lookup"><span data-stu-id="8697f-231">Entry</span></span> | <span data-ttu-id="8697f-232">值</span><span class="sxs-lookup"><span data-stu-id="8697f-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8697f-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8697f-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8697f-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8697f-235">System-Only</span></span>            | <span data-ttu-id="8697f-236">否</span><span class="sxs-lookup"><span data-stu-id="8697f-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8697f-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8697f-238">對</span><span class="sxs-lookup"><span data-stu-id="8697f-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8697f-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8697f-239">Is Indexed</span></span>             | <span data-ttu-id="8697f-240">否</span><span class="sxs-lookup"><span data-stu-id="8697f-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8697f-241">In Global Catalog</span></span>      | <span data-ttu-id="8697f-242">否</span><span class="sxs-lookup"><span data-stu-id="8697f-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8697f-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8697f-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8697f-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8697f-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8697f-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8697f-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-247">Search-Flags</span></span>           | <span data-ttu-id="8697f-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8697f-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-249">System-Flags</span></span>           | <span data-ttu-id="8697f-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8697f-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8697f-251">Classes used in</span></span>        | [<span data-ttu-id="8697f-252">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="8697f-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8697f-253">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8697f-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8697f-254">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8697f-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8697f-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8697f-255">Windows Server 2012</span></span>



| <span data-ttu-id="8697f-256">進入</span><span class="sxs-lookup"><span data-stu-id="8697f-256">Entry</span></span> | <span data-ttu-id="8697f-257">值</span><span class="sxs-lookup"><span data-stu-id="8697f-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8697f-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8697f-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8697f-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="8697f-260">System-Only</span></span>            | <span data-ttu-id="8697f-261">否</span><span class="sxs-lookup"><span data-stu-id="8697f-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8697f-262">Is-Single-Valued</span></span>       | <span data-ttu-id="8697f-263">對</span><span class="sxs-lookup"><span data-stu-id="8697f-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="8697f-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8697f-264">Is Indexed</span></span>             | <span data-ttu-id="8697f-265">否</span><span class="sxs-lookup"><span data-stu-id="8697f-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8697f-266">In Global Catalog</span></span>      | <span data-ttu-id="8697f-267">否</span><span class="sxs-lookup"><span data-stu-id="8697f-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="8697f-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8697f-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="8697f-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8697f-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="8697f-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8697f-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8697f-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="8697f-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-272">Search-Flags</span></span>           | <span data-ttu-id="8697f-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8697f-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8697f-274">System-Flags</span></span>           | <span data-ttu-id="8697f-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8697f-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="8697f-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8697f-276">Classes used in</span></span>        | [<span data-ttu-id="8697f-277">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="8697f-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="8697f-278">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="8697f-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="8697f-279">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8697f-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="8697f-280">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8697f-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8697f-281">**鎖定-持續時間**</span><span class="sxs-lookup"><span data-stu-id="8697f-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





