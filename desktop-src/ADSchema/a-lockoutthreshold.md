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
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="197ea-105">Lockout-Threshold 屬性</span><span class="sxs-lookup"><span data-stu-id="197ea-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="197ea-106">帳戶遭到鎖定之前允許的無效登入嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="197ea-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="197ea-107">進入</span><span class="sxs-lookup"><span data-stu-id="197ea-107">Entry</span></span> | <span data-ttu-id="197ea-108">值</span><span class="sxs-lookup"><span data-stu-id="197ea-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="197ea-109">CN</span><span class="sxs-lookup"><span data-stu-id="197ea-109">CN</span></span>                | <span data-ttu-id="197ea-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="197ea-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="197ea-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="197ea-111">Ldap-Display-Name</span></span> | <span data-ttu-id="197ea-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="197ea-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="197ea-113">大小</span><span class="sxs-lookup"><span data-stu-id="197ea-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="197ea-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="197ea-114">Update Privilege</span></span>  | <span data-ttu-id="197ea-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="197ea-115">Domain administrator</span></span>                 |
| <span data-ttu-id="197ea-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="197ea-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="197ea-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="197ea-117">Attribute-Id</span></span>      | <span data-ttu-id="197ea-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="197ea-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="197ea-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="197ea-119">System-Id-Guid</span></span>    | <span data-ttu-id="197ea-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="197ea-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="197ea-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="197ea-121">Syntax</span></span>            | [<span data-ttu-id="197ea-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="197ea-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="197ea-123">實作</span><span class="sxs-lookup"><span data-stu-id="197ea-123">Implementations</span></span>

-   [<span data-ttu-id="197ea-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="197ea-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="197ea-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="197ea-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="197ea-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="197ea-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="197ea-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="197ea-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="197ea-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="197ea-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="197ea-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="197ea-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="197ea-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="197ea-130">Windows 2000 Server</span></span>



| <span data-ttu-id="197ea-131">進入</span><span class="sxs-lookup"><span data-stu-id="197ea-131">Entry</span></span> | <span data-ttu-id="197ea-132">值</span><span class="sxs-lookup"><span data-stu-id="197ea-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197ea-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="197ea-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="197ea-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="197ea-135">System-Only</span></span>            | <span data-ttu-id="197ea-136">否</span><span class="sxs-lookup"><span data-stu-id="197ea-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="197ea-137">Is-Single-Valued</span></span>       | <span data-ttu-id="197ea-138">對</span><span class="sxs-lookup"><span data-stu-id="197ea-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="197ea-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="197ea-139">Is Indexed</span></span>             | <span data-ttu-id="197ea-140">否</span><span class="sxs-lookup"><span data-stu-id="197ea-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="197ea-141">In Global Catalog</span></span>      | <span data-ttu-id="197ea-142">否</span><span class="sxs-lookup"><span data-stu-id="197ea-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="197ea-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="197ea-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="197ea-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="197ea-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="197ea-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="197ea-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-147">Search-Flags</span></span>           | <span data-ttu-id="197ea-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="197ea-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-149">System-Flags</span></span>           | <span data-ttu-id="197ea-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="197ea-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="197ea-151">Classes used in</span></span>        | [<span data-ttu-id="197ea-152">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="197ea-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="197ea-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="197ea-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="197ea-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="197ea-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="197ea-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="197ea-155">Windows Server 2003</span></span>



| <span data-ttu-id="197ea-156">進入</span><span class="sxs-lookup"><span data-stu-id="197ea-156">Entry</span></span> | <span data-ttu-id="197ea-157">值</span><span class="sxs-lookup"><span data-stu-id="197ea-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197ea-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="197ea-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="197ea-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="197ea-160">System-Only</span></span>            | <span data-ttu-id="197ea-161">否</span><span class="sxs-lookup"><span data-stu-id="197ea-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="197ea-162">Is-Single-Valued</span></span>       | <span data-ttu-id="197ea-163">對</span><span class="sxs-lookup"><span data-stu-id="197ea-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="197ea-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="197ea-164">Is Indexed</span></span>             | <span data-ttu-id="197ea-165">否</span><span class="sxs-lookup"><span data-stu-id="197ea-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="197ea-166">In Global Catalog</span></span>      | <span data-ttu-id="197ea-167">否</span><span class="sxs-lookup"><span data-stu-id="197ea-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="197ea-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="197ea-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="197ea-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="197ea-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="197ea-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="197ea-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-172">Search-Flags</span></span>           | <span data-ttu-id="197ea-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="197ea-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-174">System-Flags</span></span>           | <span data-ttu-id="197ea-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="197ea-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="197ea-176">Classes used in</span></span>        | [<span data-ttu-id="197ea-177">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="197ea-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="197ea-178">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="197ea-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="197ea-179">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="197ea-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="197ea-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="197ea-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="197ea-181">進入</span><span class="sxs-lookup"><span data-stu-id="197ea-181">Entry</span></span> | <span data-ttu-id="197ea-182">值</span><span class="sxs-lookup"><span data-stu-id="197ea-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197ea-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="197ea-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="197ea-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="197ea-185">System-Only</span></span>            | <span data-ttu-id="197ea-186">否</span><span class="sxs-lookup"><span data-stu-id="197ea-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="197ea-187">Is-Single-Valued</span></span>       | <span data-ttu-id="197ea-188">對</span><span class="sxs-lookup"><span data-stu-id="197ea-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="197ea-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="197ea-189">Is Indexed</span></span>             | <span data-ttu-id="197ea-190">否</span><span class="sxs-lookup"><span data-stu-id="197ea-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="197ea-191">In Global Catalog</span></span>      | <span data-ttu-id="197ea-192">否</span><span class="sxs-lookup"><span data-stu-id="197ea-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="197ea-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="197ea-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="197ea-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="197ea-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="197ea-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="197ea-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-197">Search-Flags</span></span>           | <span data-ttu-id="197ea-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="197ea-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-199">System-Flags</span></span>           | <span data-ttu-id="197ea-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="197ea-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="197ea-201">Classes used in</span></span>        | [<span data-ttu-id="197ea-202">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="197ea-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="197ea-203">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="197ea-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="197ea-204">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="197ea-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="197ea-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="197ea-205">Windows Server 2008</span></span>



| <span data-ttu-id="197ea-206">進入</span><span class="sxs-lookup"><span data-stu-id="197ea-206">Entry</span></span> | <span data-ttu-id="197ea-207">值</span><span class="sxs-lookup"><span data-stu-id="197ea-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197ea-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="197ea-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="197ea-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="197ea-210">System-Only</span></span>            | <span data-ttu-id="197ea-211">否</span><span class="sxs-lookup"><span data-stu-id="197ea-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="197ea-212">Is-Single-Valued</span></span>       | <span data-ttu-id="197ea-213">對</span><span class="sxs-lookup"><span data-stu-id="197ea-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="197ea-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="197ea-214">Is Indexed</span></span>             | <span data-ttu-id="197ea-215">否</span><span class="sxs-lookup"><span data-stu-id="197ea-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="197ea-216">In Global Catalog</span></span>      | <span data-ttu-id="197ea-217">否</span><span class="sxs-lookup"><span data-stu-id="197ea-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="197ea-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="197ea-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="197ea-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="197ea-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="197ea-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="197ea-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-222">Search-Flags</span></span>           | <span data-ttu-id="197ea-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="197ea-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-224">System-Flags</span></span>           | <span data-ttu-id="197ea-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="197ea-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="197ea-226">Classes used in</span></span>        | [<span data-ttu-id="197ea-227">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="197ea-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="197ea-228">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="197ea-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="197ea-229">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="197ea-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="197ea-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="197ea-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="197ea-231">進入</span><span class="sxs-lookup"><span data-stu-id="197ea-231">Entry</span></span> | <span data-ttu-id="197ea-232">值</span><span class="sxs-lookup"><span data-stu-id="197ea-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197ea-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="197ea-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="197ea-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="197ea-235">System-Only</span></span>            | <span data-ttu-id="197ea-236">否</span><span class="sxs-lookup"><span data-stu-id="197ea-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="197ea-237">Is-Single-Valued</span></span>       | <span data-ttu-id="197ea-238">對</span><span class="sxs-lookup"><span data-stu-id="197ea-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="197ea-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="197ea-239">Is Indexed</span></span>             | <span data-ttu-id="197ea-240">否</span><span class="sxs-lookup"><span data-stu-id="197ea-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="197ea-241">In Global Catalog</span></span>      | <span data-ttu-id="197ea-242">否</span><span class="sxs-lookup"><span data-stu-id="197ea-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="197ea-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="197ea-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="197ea-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="197ea-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="197ea-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="197ea-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-247">Search-Flags</span></span>           | <span data-ttu-id="197ea-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="197ea-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-249">System-Flags</span></span>           | <span data-ttu-id="197ea-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="197ea-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="197ea-251">Classes used in</span></span>        | [<span data-ttu-id="197ea-252">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="197ea-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="197ea-253">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="197ea-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="197ea-254">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="197ea-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="197ea-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="197ea-255">Windows Server 2012</span></span>



| <span data-ttu-id="197ea-256">進入</span><span class="sxs-lookup"><span data-stu-id="197ea-256">Entry</span></span> | <span data-ttu-id="197ea-257">值</span><span class="sxs-lookup"><span data-stu-id="197ea-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197ea-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="197ea-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="197ea-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="197ea-260">System-Only</span></span>            | <span data-ttu-id="197ea-261">否</span><span class="sxs-lookup"><span data-stu-id="197ea-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="197ea-262">Is-Single-Valued</span></span>       | <span data-ttu-id="197ea-263">對</span><span class="sxs-lookup"><span data-stu-id="197ea-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="197ea-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="197ea-264">Is Indexed</span></span>             | <span data-ttu-id="197ea-265">否</span><span class="sxs-lookup"><span data-stu-id="197ea-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="197ea-266">In Global Catalog</span></span>      | <span data-ttu-id="197ea-267">否</span><span class="sxs-lookup"><span data-stu-id="197ea-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="197ea-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="197ea-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="197ea-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="197ea-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="197ea-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="197ea-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="197ea-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="197ea-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-272">Search-Flags</span></span>           | <span data-ttu-id="197ea-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="197ea-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="197ea-274">System-Flags</span></span>           | <span data-ttu-id="197ea-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="197ea-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="197ea-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="197ea-276">Classes used in</span></span>        | [<span data-ttu-id="197ea-277">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="197ea-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="197ea-278">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="197ea-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="197ea-279">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="197ea-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="197ea-280">另請參閱</span><span class="sxs-lookup"><span data-stu-id="197ea-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197ea-281">**鎖定-持續時間**</span><span class="sxs-lookup"><span data-stu-id="197ea-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





