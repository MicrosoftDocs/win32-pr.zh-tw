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
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="b5719-105">Lockout-Threshold 屬性</span><span class="sxs-lookup"><span data-stu-id="b5719-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="b5719-106">帳戶遭到鎖定之前允許的無效登入嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="b5719-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="b5719-107">進入</span><span class="sxs-lookup"><span data-stu-id="b5719-107">Entry</span></span> | <span data-ttu-id="b5719-108">值</span><span class="sxs-lookup"><span data-stu-id="b5719-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b5719-109">CN</span><span class="sxs-lookup"><span data-stu-id="b5719-109">CN</span></span>                | <span data-ttu-id="b5719-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="b5719-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="b5719-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b5719-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b5719-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="b5719-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="b5719-113">大小</span><span class="sxs-lookup"><span data-stu-id="b5719-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="b5719-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b5719-114">Update Privilege</span></span>  | <span data-ttu-id="b5719-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="b5719-115">Domain administrator</span></span>                 |
| <span data-ttu-id="b5719-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b5719-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b5719-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5719-117">Attribute-Id</span></span>      | <span data-ttu-id="b5719-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="b5719-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="b5719-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b5719-119">System-Id-Guid</span></span>    | <span data-ttu-id="b5719-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b5719-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b5719-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5719-121">Syntax</span></span>            | [<span data-ttu-id="b5719-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="b5719-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b5719-123">實作</span><span class="sxs-lookup"><span data-stu-id="b5719-123">Implementations</span></span>

-   [<span data-ttu-id="b5719-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b5719-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b5719-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5719-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5719-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5719-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5719-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5719-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5719-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5719-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5719-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5719-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b5719-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5719-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b5719-131">進入</span><span class="sxs-lookup"><span data-stu-id="b5719-131">Entry</span></span> | <span data-ttu-id="b5719-132">值</span><span class="sxs-lookup"><span data-stu-id="b5719-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5719-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b5719-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5719-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5719-135">System-Only</span></span>            | <span data-ttu-id="b5719-136">否</span><span class="sxs-lookup"><span data-stu-id="b5719-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b5719-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b5719-138">對</span><span class="sxs-lookup"><span data-stu-id="b5719-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b5719-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b5719-139">Is Indexed</span></span>             | <span data-ttu-id="b5719-140">否</span><span class="sxs-lookup"><span data-stu-id="b5719-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b5719-141">In Global Catalog</span></span>      | <span data-ttu-id="b5719-142">否</span><span class="sxs-lookup"><span data-stu-id="b5719-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b5719-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5719-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b5719-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b5719-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5719-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5719-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-147">Search-Flags</span></span>           | <span data-ttu-id="b5719-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5719-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-149">System-Flags</span></span>           | <span data-ttu-id="b5719-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5719-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b5719-151">Classes used in</span></span>        | [<span data-ttu-id="b5719-152">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b5719-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b5719-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b5719-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b5719-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b5719-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b5719-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5719-155">Windows Server 2003</span></span>



| <span data-ttu-id="b5719-156">進入</span><span class="sxs-lookup"><span data-stu-id="b5719-156">Entry</span></span> | <span data-ttu-id="b5719-157">值</span><span class="sxs-lookup"><span data-stu-id="b5719-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5719-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b5719-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5719-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5719-160">System-Only</span></span>            | <span data-ttu-id="b5719-161">否</span><span class="sxs-lookup"><span data-stu-id="b5719-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b5719-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b5719-163">對</span><span class="sxs-lookup"><span data-stu-id="b5719-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b5719-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b5719-164">Is Indexed</span></span>             | <span data-ttu-id="b5719-165">否</span><span class="sxs-lookup"><span data-stu-id="b5719-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b5719-166">In Global Catalog</span></span>      | <span data-ttu-id="b5719-167">否</span><span class="sxs-lookup"><span data-stu-id="b5719-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b5719-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5719-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b5719-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b5719-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5719-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5719-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-172">Search-Flags</span></span>           | <span data-ttu-id="b5719-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5719-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-174">System-Flags</span></span>           | <span data-ttu-id="b5719-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5719-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b5719-176">Classes used in</span></span>        | [<span data-ttu-id="b5719-177">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b5719-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b5719-178">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b5719-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b5719-179">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b5719-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5719-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5719-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5719-181">進入</span><span class="sxs-lookup"><span data-stu-id="b5719-181">Entry</span></span> | <span data-ttu-id="b5719-182">值</span><span class="sxs-lookup"><span data-stu-id="b5719-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5719-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b5719-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5719-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5719-185">System-Only</span></span>            | <span data-ttu-id="b5719-186">否</span><span class="sxs-lookup"><span data-stu-id="b5719-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b5719-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b5719-188">對</span><span class="sxs-lookup"><span data-stu-id="b5719-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b5719-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b5719-189">Is Indexed</span></span>             | <span data-ttu-id="b5719-190">否</span><span class="sxs-lookup"><span data-stu-id="b5719-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b5719-191">In Global Catalog</span></span>      | <span data-ttu-id="b5719-192">否</span><span class="sxs-lookup"><span data-stu-id="b5719-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b5719-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5719-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b5719-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b5719-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5719-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5719-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-197">Search-Flags</span></span>           | <span data-ttu-id="b5719-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5719-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-199">System-Flags</span></span>           | <span data-ttu-id="b5719-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5719-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b5719-201">Classes used in</span></span>        | [<span data-ttu-id="b5719-202">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b5719-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b5719-203">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b5719-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b5719-204">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b5719-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b5719-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5719-205">Windows Server 2008</span></span>



| <span data-ttu-id="b5719-206">進入</span><span class="sxs-lookup"><span data-stu-id="b5719-206">Entry</span></span> | <span data-ttu-id="b5719-207">值</span><span class="sxs-lookup"><span data-stu-id="b5719-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5719-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b5719-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5719-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5719-210">System-Only</span></span>            | <span data-ttu-id="b5719-211">否</span><span class="sxs-lookup"><span data-stu-id="b5719-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b5719-212">Is-Single-Valued</span></span>       | <span data-ttu-id="b5719-213">對</span><span class="sxs-lookup"><span data-stu-id="b5719-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b5719-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b5719-214">Is Indexed</span></span>             | <span data-ttu-id="b5719-215">否</span><span class="sxs-lookup"><span data-stu-id="b5719-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b5719-216">In Global Catalog</span></span>      | <span data-ttu-id="b5719-217">否</span><span class="sxs-lookup"><span data-stu-id="b5719-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b5719-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5719-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b5719-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b5719-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5719-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5719-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-222">Search-Flags</span></span>           | <span data-ttu-id="b5719-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5719-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-224">System-Flags</span></span>           | <span data-ttu-id="b5719-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5719-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b5719-226">Classes used in</span></span>        | [<span data-ttu-id="b5719-227">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b5719-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b5719-228">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b5719-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b5719-229">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b5719-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5719-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5719-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5719-231">進入</span><span class="sxs-lookup"><span data-stu-id="b5719-231">Entry</span></span> | <span data-ttu-id="b5719-232">值</span><span class="sxs-lookup"><span data-stu-id="b5719-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5719-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b5719-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5719-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5719-235">System-Only</span></span>            | <span data-ttu-id="b5719-236">否</span><span class="sxs-lookup"><span data-stu-id="b5719-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b5719-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b5719-238">對</span><span class="sxs-lookup"><span data-stu-id="b5719-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b5719-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b5719-239">Is Indexed</span></span>             | <span data-ttu-id="b5719-240">否</span><span class="sxs-lookup"><span data-stu-id="b5719-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b5719-241">In Global Catalog</span></span>      | <span data-ttu-id="b5719-242">否</span><span class="sxs-lookup"><span data-stu-id="b5719-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b5719-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5719-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b5719-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b5719-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5719-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5719-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-247">Search-Flags</span></span>           | <span data-ttu-id="b5719-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5719-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-249">System-Flags</span></span>           | <span data-ttu-id="b5719-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5719-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b5719-251">Classes used in</span></span>        | [<span data-ttu-id="b5719-252">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b5719-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b5719-253">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b5719-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b5719-254">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b5719-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b5719-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5719-255">Windows Server 2012</span></span>



| <span data-ttu-id="b5719-256">進入</span><span class="sxs-lookup"><span data-stu-id="b5719-256">Entry</span></span> | <span data-ttu-id="b5719-257">值</span><span class="sxs-lookup"><span data-stu-id="b5719-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5719-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b5719-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5719-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5719-260">System-Only</span></span>            | <span data-ttu-id="b5719-261">否</span><span class="sxs-lookup"><span data-stu-id="b5719-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b5719-262">Is-Single-Valued</span></span>       | <span data-ttu-id="b5719-263">對</span><span class="sxs-lookup"><span data-stu-id="b5719-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b5719-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b5719-264">Is Indexed</span></span>             | <span data-ttu-id="b5719-265">否</span><span class="sxs-lookup"><span data-stu-id="b5719-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b5719-266">In Global Catalog</span></span>      | <span data-ttu-id="b5719-267">否</span><span class="sxs-lookup"><span data-stu-id="b5719-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b5719-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b5719-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5719-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b5719-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b5719-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5719-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5719-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b5719-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-272">Search-Flags</span></span>           | <span data-ttu-id="b5719-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5719-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5719-274">System-Flags</span></span>           | <span data-ttu-id="b5719-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5719-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b5719-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b5719-276">Classes used in</span></span>        | [<span data-ttu-id="b5719-277">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b5719-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b5719-278">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b5719-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b5719-279">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b5719-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="b5719-280">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5719-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5719-281">**鎖定-持續時間**</span><span class="sxs-lookup"><span data-stu-id="b5719-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





