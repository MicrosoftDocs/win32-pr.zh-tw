---
title: Lockout-Duration 屬性
description: 因為超過 Lockout-Threshold 而鎖定帳戶的時間量。
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Lockout-Duration 屬性 AD 架構
- lockoutDuration 屬性 AD 架構
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972495"
---
# <a name="lockout-duration-attribute"></a><span data-ttu-id="41f70-105">Lockout-Duration 屬性</span><span class="sxs-lookup"><span data-stu-id="41f70-105">Lockout-Duration attribute</span></span>

<span data-ttu-id="41f70-106">因為超過 [**鎖定閾值**](a-lockoutthreshold.md) 而鎖定帳戶的時間量。</span><span class="sxs-lookup"><span data-stu-id="41f70-106">The amount of time that an account is locked due to the [**Lockout-Threshold**](a-lockoutthreshold.md) being exceeded.</span></span> <span data-ttu-id="41f70-107">此值會儲存為一個大型整數，以代表在解除鎖定帳戶之前必須 [**經過的時間長度為 100**](a-lockoutthreshold.md) -毫微秒間隔的負數。</span><span class="sxs-lookup"><span data-stu-id="41f70-107">This value is stored as a large integer that represents the negative of the number of 100-nanosecond intervals from the time the [**Lockout-Threshold**](a-lockoutthreshold.md) is exceeded that must elapse before the account is unlocked.</span></span>



| <span data-ttu-id="41f70-108">進入</span><span class="sxs-lookup"><span data-stu-id="41f70-108">Entry</span></span> | <span data-ttu-id="41f70-109">值</span><span class="sxs-lookup"><span data-stu-id="41f70-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="41f70-110">CN</span><span class="sxs-lookup"><span data-stu-id="41f70-110">CN</span></span>                | <span data-ttu-id="41f70-111">Lockout-Duration</span><span class="sxs-lookup"><span data-stu-id="41f70-111">Lockout-Duration</span></span>                     |
| <span data-ttu-id="41f70-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="41f70-112">Ldap-Display-Name</span></span> | <span data-ttu-id="41f70-113">lockoutDuration</span><span class="sxs-lookup"><span data-stu-id="41f70-113">lockoutDuration</span></span>                      |
| <span data-ttu-id="41f70-114">大小</span><span class="sxs-lookup"><span data-stu-id="41f70-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="41f70-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="41f70-115">Update Privilege</span></span>  | <span data-ttu-id="41f70-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="41f70-116">Domain administrator</span></span>                 |
| <span data-ttu-id="41f70-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="41f70-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="41f70-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="41f70-118">Attribute-Id</span></span>      | <span data-ttu-id="41f70-119">1.2.840.113556.1.4.60</span><span class="sxs-lookup"><span data-stu-id="41f70-119">1.2.840.113556.1.4.60</span></span>                |
| <span data-ttu-id="41f70-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="41f70-120">System-Id-Guid</span></span>    | <span data-ttu-id="41f70-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="41f70-121">bf9679a5-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="41f70-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="41f70-122">Syntax</span></span>            | [<span data-ttu-id="41f70-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="41f70-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="41f70-124">實作</span><span class="sxs-lookup"><span data-stu-id="41f70-124">Implementations</span></span>

-   [<span data-ttu-id="41f70-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="41f70-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="41f70-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="41f70-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="41f70-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="41f70-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="41f70-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="41f70-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="41f70-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="41f70-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="41f70-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="41f70-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="41f70-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41f70-131">Windows 2000 Server</span></span>



| <span data-ttu-id="41f70-132">進入</span><span class="sxs-lookup"><span data-stu-id="41f70-132">Entry</span></span> | <span data-ttu-id="41f70-133">值</span><span class="sxs-lookup"><span data-stu-id="41f70-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f70-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41f70-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41f70-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="41f70-136">System-Only</span></span>            | <span data-ttu-id="41f70-137">否</span><span class="sxs-lookup"><span data-stu-id="41f70-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41f70-138">Is-Single-Valued</span></span>       | <span data-ttu-id="41f70-139">對</span><span class="sxs-lookup"><span data-stu-id="41f70-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="41f70-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41f70-140">Is Indexed</span></span>             | <span data-ttu-id="41f70-141">否</span><span class="sxs-lookup"><span data-stu-id="41f70-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41f70-142">In Global Catalog</span></span>      | <span data-ttu-id="41f70-143">否</span><span class="sxs-lookup"><span data-stu-id="41f70-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41f70-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="41f70-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41f70-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="41f70-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41f70-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41f70-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-148">Search-Flags</span></span>           | <span data-ttu-id="41f70-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41f70-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-150">System-Flags</span></span>           | <span data-ttu-id="41f70-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41f70-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41f70-152">Classes used in</span></span>        | [<span data-ttu-id="41f70-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="41f70-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="41f70-154">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="41f70-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="41f70-155">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="41f70-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="41f70-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41f70-156">Windows Server 2003</span></span>



| <span data-ttu-id="41f70-157">進入</span><span class="sxs-lookup"><span data-stu-id="41f70-157">Entry</span></span> | <span data-ttu-id="41f70-158">值</span><span class="sxs-lookup"><span data-stu-id="41f70-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f70-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41f70-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41f70-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="41f70-161">System-Only</span></span>            | <span data-ttu-id="41f70-162">否</span><span class="sxs-lookup"><span data-stu-id="41f70-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41f70-163">Is-Single-Valued</span></span>       | <span data-ttu-id="41f70-164">對</span><span class="sxs-lookup"><span data-stu-id="41f70-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="41f70-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41f70-165">Is Indexed</span></span>             | <span data-ttu-id="41f70-166">否</span><span class="sxs-lookup"><span data-stu-id="41f70-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41f70-167">In Global Catalog</span></span>      | <span data-ttu-id="41f70-168">否</span><span class="sxs-lookup"><span data-stu-id="41f70-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41f70-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="41f70-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41f70-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="41f70-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41f70-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41f70-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-173">Search-Flags</span></span>           | <span data-ttu-id="41f70-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41f70-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-175">System-Flags</span></span>           | <span data-ttu-id="41f70-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41f70-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41f70-177">Classes used in</span></span>        | [<span data-ttu-id="41f70-178">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="41f70-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="41f70-179">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="41f70-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="41f70-180">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="41f70-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="41f70-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="41f70-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="41f70-182">進入</span><span class="sxs-lookup"><span data-stu-id="41f70-182">Entry</span></span> | <span data-ttu-id="41f70-183">值</span><span class="sxs-lookup"><span data-stu-id="41f70-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f70-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41f70-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41f70-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="41f70-186">System-Only</span></span>            | <span data-ttu-id="41f70-187">否</span><span class="sxs-lookup"><span data-stu-id="41f70-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41f70-188">Is-Single-Valued</span></span>       | <span data-ttu-id="41f70-189">對</span><span class="sxs-lookup"><span data-stu-id="41f70-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="41f70-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41f70-190">Is Indexed</span></span>             | <span data-ttu-id="41f70-191">否</span><span class="sxs-lookup"><span data-stu-id="41f70-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41f70-192">In Global Catalog</span></span>      | <span data-ttu-id="41f70-193">否</span><span class="sxs-lookup"><span data-stu-id="41f70-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41f70-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="41f70-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41f70-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="41f70-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41f70-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41f70-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-198">Search-Flags</span></span>           | <span data-ttu-id="41f70-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41f70-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-200">System-Flags</span></span>           | <span data-ttu-id="41f70-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41f70-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41f70-202">Classes used in</span></span>        | [<span data-ttu-id="41f70-203">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="41f70-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="41f70-204">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="41f70-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="41f70-205">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="41f70-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="41f70-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41f70-206">Windows Server 2008</span></span>



| <span data-ttu-id="41f70-207">進入</span><span class="sxs-lookup"><span data-stu-id="41f70-207">Entry</span></span> | <span data-ttu-id="41f70-208">值</span><span class="sxs-lookup"><span data-stu-id="41f70-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f70-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41f70-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41f70-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="41f70-211">System-Only</span></span>            | <span data-ttu-id="41f70-212">否</span><span class="sxs-lookup"><span data-stu-id="41f70-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41f70-213">Is-Single-Valued</span></span>       | <span data-ttu-id="41f70-214">對</span><span class="sxs-lookup"><span data-stu-id="41f70-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="41f70-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41f70-215">Is Indexed</span></span>             | <span data-ttu-id="41f70-216">否</span><span class="sxs-lookup"><span data-stu-id="41f70-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41f70-217">In Global Catalog</span></span>      | <span data-ttu-id="41f70-218">否</span><span class="sxs-lookup"><span data-stu-id="41f70-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41f70-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="41f70-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41f70-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="41f70-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41f70-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41f70-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-223">Search-Flags</span></span>           | <span data-ttu-id="41f70-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41f70-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-225">System-Flags</span></span>           | <span data-ttu-id="41f70-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41f70-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41f70-227">Classes used in</span></span>        | [<span data-ttu-id="41f70-228">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="41f70-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="41f70-229">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="41f70-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="41f70-230">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="41f70-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="41f70-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="41f70-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="41f70-232">進入</span><span class="sxs-lookup"><span data-stu-id="41f70-232">Entry</span></span> | <span data-ttu-id="41f70-233">值</span><span class="sxs-lookup"><span data-stu-id="41f70-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f70-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41f70-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41f70-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="41f70-236">System-Only</span></span>            | <span data-ttu-id="41f70-237">否</span><span class="sxs-lookup"><span data-stu-id="41f70-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41f70-238">Is-Single-Valued</span></span>       | <span data-ttu-id="41f70-239">對</span><span class="sxs-lookup"><span data-stu-id="41f70-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="41f70-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41f70-240">Is Indexed</span></span>             | <span data-ttu-id="41f70-241">否</span><span class="sxs-lookup"><span data-stu-id="41f70-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41f70-242">In Global Catalog</span></span>      | <span data-ttu-id="41f70-243">否</span><span class="sxs-lookup"><span data-stu-id="41f70-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41f70-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="41f70-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41f70-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="41f70-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41f70-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41f70-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-248">Search-Flags</span></span>           | <span data-ttu-id="41f70-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41f70-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-250">System-Flags</span></span>           | <span data-ttu-id="41f70-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41f70-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41f70-252">Classes used in</span></span>        | [<span data-ttu-id="41f70-253">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="41f70-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="41f70-254">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="41f70-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="41f70-255">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="41f70-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="41f70-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41f70-256">Windows Server 2012</span></span>



| <span data-ttu-id="41f70-257">進入</span><span class="sxs-lookup"><span data-stu-id="41f70-257">Entry</span></span> | <span data-ttu-id="41f70-258">值</span><span class="sxs-lookup"><span data-stu-id="41f70-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f70-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41f70-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41f70-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="41f70-261">System-Only</span></span>            | <span data-ttu-id="41f70-262">否</span><span class="sxs-lookup"><span data-stu-id="41f70-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41f70-263">Is-Single-Valued</span></span>       | <span data-ttu-id="41f70-264">對</span><span class="sxs-lookup"><span data-stu-id="41f70-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="41f70-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41f70-265">Is Indexed</span></span>             | <span data-ttu-id="41f70-266">否</span><span class="sxs-lookup"><span data-stu-id="41f70-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41f70-267">In Global Catalog</span></span>      | <span data-ttu-id="41f70-268">否</span><span class="sxs-lookup"><span data-stu-id="41f70-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="41f70-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41f70-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="41f70-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41f70-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="41f70-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41f70-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41f70-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="41f70-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-273">Search-Flags</span></span>           | <span data-ttu-id="41f70-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41f70-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41f70-275">System-Flags</span></span>           | <span data-ttu-id="41f70-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41f70-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="41f70-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41f70-277">Classes used in</span></span>        | [<span data-ttu-id="41f70-278">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="41f70-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="41f70-279">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="41f70-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="41f70-280">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="41f70-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="41f70-281">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41f70-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f70-282">**鎖定-閾值**</span><span class="sxs-lookup"><span data-stu-id="41f70-282">**Lockout-Threshold**</span></span>](a-lockoutthreshold.md)
</dt> </dl>

 

 





