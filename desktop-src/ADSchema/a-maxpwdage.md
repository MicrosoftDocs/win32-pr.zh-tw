---
title: Max-Pwd-Age 屬性
description: 密碼的最大時間量，以 100-毫微秒間隔為有效。
ms.assetid: b4b48207-6481-42a1-b848-6baf37a367ce
ms.tgt_platform: multiple
keywords:
- Max-Pwd-Age 屬性 AD 架構
- maxPwdAge 屬性 AD 架構
topic_type:
- apiref
api_name:
- Max-Pwd-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc754b7cab86dc205eb14d58db73aab64685d07a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935447"
---
# <a name="max-pwd-age-attribute"></a><span data-ttu-id="b799f-105">Max-Pwd-Age 屬性</span><span class="sxs-lookup"><span data-stu-id="b799f-105">Max-Pwd-Age attribute</span></span>

<span data-ttu-id="b799f-106">密碼的最大時間量，以 100-毫微秒間隔為有效。</span><span class="sxs-lookup"><span data-stu-id="b799f-106">The maximum amount of time, in 100-nanosecond intervals, a password is valid.</span></span> <span data-ttu-id="b799f-107">此值會儲存為一個大型整數，表示密碼在密碼到期前的設定時間，100-納秒間隔的數目。</span><span class="sxs-lookup"><span data-stu-id="b799f-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals from the time the password was set before the password expires.</span></span>



| <span data-ttu-id="b799f-108">進入</span><span class="sxs-lookup"><span data-stu-id="b799f-108">Entry</span></span> | <span data-ttu-id="b799f-109">值</span><span class="sxs-lookup"><span data-stu-id="b799f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b799f-110">CN</span><span class="sxs-lookup"><span data-stu-id="b799f-110">CN</span></span>                | <span data-ttu-id="b799f-111">最大-Pwd-使用期限</span><span class="sxs-lookup"><span data-stu-id="b799f-111">Max-Pwd-Age</span></span>                          |
| <span data-ttu-id="b799f-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b799f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b799f-113">maxPwdAge</span><span class="sxs-lookup"><span data-stu-id="b799f-113">maxPwdAge</span></span>                            |
| <span data-ttu-id="b799f-114">大小</span><span class="sxs-lookup"><span data-stu-id="b799f-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="b799f-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b799f-115">Update Privilege</span></span>  | <span data-ttu-id="b799f-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="b799f-116">Domain administrator</span></span>                 |
| <span data-ttu-id="b799f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b799f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b799f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b799f-118">Attribute-Id</span></span>      | <span data-ttu-id="b799f-119">1.2.840.113556.1.4.74</span><span class="sxs-lookup"><span data-stu-id="b799f-119">1.2.840.113556.1.4.74</span></span>                |
| <span data-ttu-id="b799f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b799f-120">System-Id-Guid</span></span>    | <span data-ttu-id="b799f-121">bf9679bb-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b799f-121">bf9679bb-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b799f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b799f-122">Syntax</span></span>            | [<span data-ttu-id="b799f-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="b799f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b799f-124">實作</span><span class="sxs-lookup"><span data-stu-id="b799f-124">Implementations</span></span>

-   [<span data-ttu-id="b799f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b799f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b799f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b799f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b799f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b799f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b799f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b799f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b799f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b799f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b799f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b799f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b799f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b799f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b799f-132">進入</span><span class="sxs-lookup"><span data-stu-id="b799f-132">Entry</span></span> | <span data-ttu-id="b799f-133">值</span><span class="sxs-lookup"><span data-stu-id="b799f-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b799f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b799f-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b799f-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b799f-136">System-Only</span></span>            | <span data-ttu-id="b799f-137">否</span><span class="sxs-lookup"><span data-stu-id="b799f-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b799f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b799f-139">對</span><span class="sxs-lookup"><span data-stu-id="b799f-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b799f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b799f-140">Is Indexed</span></span>             | <span data-ttu-id="b799f-141">否</span><span class="sxs-lookup"><span data-stu-id="b799f-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b799f-142">In Global Catalog</span></span>      | <span data-ttu-id="b799f-143">否</span><span class="sxs-lookup"><span data-stu-id="b799f-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b799f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b799f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b799f-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b799f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b799f-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b799f-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-148">Search-Flags</span></span>           | <span data-ttu-id="b799f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b799f-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-150">System-Flags</span></span>           | <span data-ttu-id="b799f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b799f-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b799f-152">Classes used in</span></span>        | [<span data-ttu-id="b799f-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b799f-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b799f-154">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b799f-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b799f-155">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b799f-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b799f-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b799f-156">Windows Server 2003</span></span>



| <span data-ttu-id="b799f-157">進入</span><span class="sxs-lookup"><span data-stu-id="b799f-157">Entry</span></span> | <span data-ttu-id="b799f-158">值</span><span class="sxs-lookup"><span data-stu-id="b799f-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b799f-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b799f-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b799f-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b799f-161">System-Only</span></span>            | <span data-ttu-id="b799f-162">否</span><span class="sxs-lookup"><span data-stu-id="b799f-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b799f-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b799f-164">對</span><span class="sxs-lookup"><span data-stu-id="b799f-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b799f-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b799f-165">Is Indexed</span></span>             | <span data-ttu-id="b799f-166">否</span><span class="sxs-lookup"><span data-stu-id="b799f-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b799f-167">In Global Catalog</span></span>      | <span data-ttu-id="b799f-168">否</span><span class="sxs-lookup"><span data-stu-id="b799f-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b799f-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b799f-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b799f-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b799f-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b799f-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b799f-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-173">Search-Flags</span></span>           | <span data-ttu-id="b799f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b799f-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-175">System-Flags</span></span>           | <span data-ttu-id="b799f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b799f-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b799f-177">Classes used in</span></span>        | [<span data-ttu-id="b799f-178">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b799f-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b799f-179">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b799f-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b799f-180">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b799f-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b799f-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b799f-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b799f-182">進入</span><span class="sxs-lookup"><span data-stu-id="b799f-182">Entry</span></span> | <span data-ttu-id="b799f-183">值</span><span class="sxs-lookup"><span data-stu-id="b799f-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b799f-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b799f-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b799f-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b799f-186">System-Only</span></span>            | <span data-ttu-id="b799f-187">否</span><span class="sxs-lookup"><span data-stu-id="b799f-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b799f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b799f-189">對</span><span class="sxs-lookup"><span data-stu-id="b799f-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b799f-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b799f-190">Is Indexed</span></span>             | <span data-ttu-id="b799f-191">否</span><span class="sxs-lookup"><span data-stu-id="b799f-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b799f-192">In Global Catalog</span></span>      | <span data-ttu-id="b799f-193">否</span><span class="sxs-lookup"><span data-stu-id="b799f-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b799f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b799f-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b799f-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b799f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b799f-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b799f-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-198">Search-Flags</span></span>           | <span data-ttu-id="b799f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b799f-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-200">System-Flags</span></span>           | <span data-ttu-id="b799f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b799f-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b799f-202">Classes used in</span></span>        | [<span data-ttu-id="b799f-203">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b799f-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b799f-204">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b799f-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b799f-205">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b799f-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b799f-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b799f-206">Windows Server 2008</span></span>



| <span data-ttu-id="b799f-207">進入</span><span class="sxs-lookup"><span data-stu-id="b799f-207">Entry</span></span> | <span data-ttu-id="b799f-208">值</span><span class="sxs-lookup"><span data-stu-id="b799f-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b799f-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b799f-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b799f-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b799f-211">System-Only</span></span>            | <span data-ttu-id="b799f-212">否</span><span class="sxs-lookup"><span data-stu-id="b799f-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b799f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b799f-214">對</span><span class="sxs-lookup"><span data-stu-id="b799f-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b799f-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b799f-215">Is Indexed</span></span>             | <span data-ttu-id="b799f-216">否</span><span class="sxs-lookup"><span data-stu-id="b799f-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b799f-217">In Global Catalog</span></span>      | <span data-ttu-id="b799f-218">否</span><span class="sxs-lookup"><span data-stu-id="b799f-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b799f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b799f-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b799f-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b799f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b799f-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b799f-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-223">Search-Flags</span></span>           | <span data-ttu-id="b799f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b799f-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-225">System-Flags</span></span>           | <span data-ttu-id="b799f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b799f-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b799f-227">Classes used in</span></span>        | [<span data-ttu-id="b799f-228">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b799f-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b799f-229">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b799f-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b799f-230">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b799f-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b799f-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b799f-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b799f-232">進入</span><span class="sxs-lookup"><span data-stu-id="b799f-232">Entry</span></span> | <span data-ttu-id="b799f-233">值</span><span class="sxs-lookup"><span data-stu-id="b799f-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b799f-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b799f-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b799f-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="b799f-236">System-Only</span></span>            | <span data-ttu-id="b799f-237">否</span><span class="sxs-lookup"><span data-stu-id="b799f-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b799f-238">Is-Single-Valued</span></span>       | <span data-ttu-id="b799f-239">對</span><span class="sxs-lookup"><span data-stu-id="b799f-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b799f-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b799f-240">Is Indexed</span></span>             | <span data-ttu-id="b799f-241">否</span><span class="sxs-lookup"><span data-stu-id="b799f-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b799f-242">In Global Catalog</span></span>      | <span data-ttu-id="b799f-243">否</span><span class="sxs-lookup"><span data-stu-id="b799f-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b799f-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="b799f-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b799f-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b799f-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b799f-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b799f-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-248">Search-Flags</span></span>           | <span data-ttu-id="b799f-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b799f-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-250">System-Flags</span></span>           | <span data-ttu-id="b799f-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b799f-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b799f-252">Classes used in</span></span>        | [<span data-ttu-id="b799f-253">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b799f-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b799f-254">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b799f-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b799f-255">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b799f-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b799f-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b799f-256">Windows Server 2012</span></span>



| <span data-ttu-id="b799f-257">進入</span><span class="sxs-lookup"><span data-stu-id="b799f-257">Entry</span></span> | <span data-ttu-id="b799f-258">值</span><span class="sxs-lookup"><span data-stu-id="b799f-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b799f-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b799f-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b799f-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="b799f-261">System-Only</span></span>            | <span data-ttu-id="b799f-262">否</span><span class="sxs-lookup"><span data-stu-id="b799f-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b799f-263">Is-Single-Valued</span></span>       | <span data-ttu-id="b799f-264">對</span><span class="sxs-lookup"><span data-stu-id="b799f-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="b799f-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b799f-265">Is Indexed</span></span>             | <span data-ttu-id="b799f-266">否</span><span class="sxs-lookup"><span data-stu-id="b799f-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b799f-267">In Global Catalog</span></span>      | <span data-ttu-id="b799f-268">否</span><span class="sxs-lookup"><span data-stu-id="b799f-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="b799f-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b799f-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="b799f-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b799f-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="b799f-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b799f-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b799f-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="b799f-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-273">Search-Flags</span></span>           | <span data-ttu-id="b799f-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b799f-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b799f-275">System-Flags</span></span>           | <span data-ttu-id="b799f-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b799f-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="b799f-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b799f-277">Classes used in</span></span>        | [<span data-ttu-id="b799f-278">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b799f-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b799f-279">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="b799f-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="b799f-280">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b799f-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





