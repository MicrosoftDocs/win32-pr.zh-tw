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
# <a name="max-pwd-age-attribute"></a><span data-ttu-id="0a7f6-105">Max-Pwd-Age 屬性</span><span class="sxs-lookup"><span data-stu-id="0a7f6-105">Max-Pwd-Age attribute</span></span>

<span data-ttu-id="0a7f6-106">密碼的最大時間量，以 100-毫微秒間隔為有效。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-106">The maximum amount of time, in 100-nanosecond intervals, a password is valid.</span></span> <span data-ttu-id="0a7f6-107">此值會儲存為一個大型整數，表示密碼在密碼到期前的設定時間，100-納秒間隔的數目。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals from the time the password was set before the password expires.</span></span>



| <span data-ttu-id="0a7f6-108">進入</span><span class="sxs-lookup"><span data-stu-id="0a7f6-108">Entry</span></span> | <span data-ttu-id="0a7f6-109">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0a7f6-110">CN</span><span class="sxs-lookup"><span data-stu-id="0a7f6-110">CN</span></span>                | <span data-ttu-id="0a7f6-111">最大-Pwd-使用期限</span><span class="sxs-lookup"><span data-stu-id="0a7f6-111">Max-Pwd-Age</span></span>                          |
| <span data-ttu-id="0a7f6-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0a7f6-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0a7f6-113">maxPwdAge</span><span class="sxs-lookup"><span data-stu-id="0a7f6-113">maxPwdAge</span></span>                            |
| <span data-ttu-id="0a7f6-114">大小</span><span class="sxs-lookup"><span data-stu-id="0a7f6-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="0a7f6-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0a7f6-115">Update Privilege</span></span>  | <span data-ttu-id="0a7f6-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="0a7f6-116">Domain administrator</span></span>                 |
| <span data-ttu-id="0a7f6-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0a7f6-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0a7f6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0a7f6-118">Attribute-Id</span></span>      | <span data-ttu-id="0a7f6-119">1.2.840.113556.1.4.74</span><span class="sxs-lookup"><span data-stu-id="0a7f6-119">1.2.840.113556.1.4.74</span></span>                |
| <span data-ttu-id="0a7f6-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0a7f6-120">System-Id-Guid</span></span>    | <span data-ttu-id="0a7f6-121">bf9679bb-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0a7f6-121">bf9679bb-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="0a7f6-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a7f6-122">Syntax</span></span>            | [<span data-ttu-id="0a7f6-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0a7f6-124">實作</span><span class="sxs-lookup"><span data-stu-id="0a7f6-124">Implementations</span></span>

-   [<span data-ttu-id="0a7f6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0a7f6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0a7f6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0a7f6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0a7f6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0a7f6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0a7f6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a7f6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0a7f6-132">進入</span><span class="sxs-lookup"><span data-stu-id="0a7f6-132">Entry</span></span> | <span data-ttu-id="0a7f6-133">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7f6-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-134">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a7f6-135">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a7f6-136">System-Only</span></span>            | <span data-ttu-id="0a7f6-137">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-137">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0a7f6-139">對</span><span class="sxs-lookup"><span data-stu-id="0a7f6-139">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0a7f6-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0a7f6-140">Is Indexed</span></span>             | <span data-ttu-id="0a7f6-141">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-141">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0a7f6-142">In Global Catalog</span></span>      | <span data-ttu-id="0a7f6-143">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-143">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0a7f6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a7f6-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0a7f6-145">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0a7f6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a7f6-146">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a7f6-147">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-148">Search-Flags</span></span>           | <span data-ttu-id="0a7f6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a7f6-149">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-150">System-Flags</span></span>           | <span data-ttu-id="0a7f6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a7f6-151">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0a7f6-152">Classes used in</span></span>        | [<span data-ttu-id="0a7f6-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0a7f6-154">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0a7f6-155">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-155">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0a7f6-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0a7f6-156">Windows Server 2003</span></span>



| <span data-ttu-id="0a7f6-157">進入</span><span class="sxs-lookup"><span data-stu-id="0a7f6-157">Entry</span></span> | <span data-ttu-id="0a7f6-158">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7f6-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-159">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a7f6-160">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a7f6-161">System-Only</span></span>            | <span data-ttu-id="0a7f6-162">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-162">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-163">Is-Single-Valued</span></span>       | <span data-ttu-id="0a7f6-164">對</span><span class="sxs-lookup"><span data-stu-id="0a7f6-164">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0a7f6-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0a7f6-165">Is Indexed</span></span>             | <span data-ttu-id="0a7f6-166">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-166">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0a7f6-167">In Global Catalog</span></span>      | <span data-ttu-id="0a7f6-168">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-168">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0a7f6-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a7f6-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0a7f6-170">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0a7f6-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a7f6-171">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a7f6-172">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-173">Search-Flags</span></span>           | <span data-ttu-id="0a7f6-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a7f6-174">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-175">System-Flags</span></span>           | <span data-ttu-id="0a7f6-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a7f6-176">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0a7f6-177">Classes used in</span></span>        | [<span data-ttu-id="0a7f6-178">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-178">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0a7f6-179">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0a7f6-180">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0a7f6-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0a7f6-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0a7f6-182">進入</span><span class="sxs-lookup"><span data-stu-id="0a7f6-182">Entry</span></span> | <span data-ttu-id="0a7f6-183">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7f6-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-184">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a7f6-185">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a7f6-186">System-Only</span></span>            | <span data-ttu-id="0a7f6-187">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-187">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0a7f6-189">對</span><span class="sxs-lookup"><span data-stu-id="0a7f6-189">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0a7f6-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0a7f6-190">Is Indexed</span></span>             | <span data-ttu-id="0a7f6-191">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-191">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0a7f6-192">In Global Catalog</span></span>      | <span data-ttu-id="0a7f6-193">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-193">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0a7f6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a7f6-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0a7f6-195">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0a7f6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a7f6-196">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a7f6-197">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-198">Search-Flags</span></span>           | <span data-ttu-id="0a7f6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a7f6-199">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-200">System-Flags</span></span>           | <span data-ttu-id="0a7f6-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a7f6-201">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0a7f6-202">Classes used in</span></span>        | [<span data-ttu-id="0a7f6-203">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-203">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0a7f6-204">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-204">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0a7f6-205">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-205">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0a7f6-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a7f6-206">Windows Server 2008</span></span>



| <span data-ttu-id="0a7f6-207">進入</span><span class="sxs-lookup"><span data-stu-id="0a7f6-207">Entry</span></span> | <span data-ttu-id="0a7f6-208">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7f6-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-209">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a7f6-210">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a7f6-211">System-Only</span></span>            | <span data-ttu-id="0a7f6-212">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-212">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-213">Is-Single-Valued</span></span>       | <span data-ttu-id="0a7f6-214">對</span><span class="sxs-lookup"><span data-stu-id="0a7f6-214">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0a7f6-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0a7f6-215">Is Indexed</span></span>             | <span data-ttu-id="0a7f6-216">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-216">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0a7f6-217">In Global Catalog</span></span>      | <span data-ttu-id="0a7f6-218">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-218">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0a7f6-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a7f6-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0a7f6-220">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0a7f6-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a7f6-221">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a7f6-222">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-223">Search-Flags</span></span>           | <span data-ttu-id="0a7f6-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a7f6-224">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-225">System-Flags</span></span>           | <span data-ttu-id="0a7f6-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a7f6-226">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0a7f6-227">Classes used in</span></span>        | [<span data-ttu-id="0a7f6-228">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-228">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0a7f6-229">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-229">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0a7f6-230">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-230">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0a7f6-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0a7f6-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0a7f6-232">進入</span><span class="sxs-lookup"><span data-stu-id="0a7f6-232">Entry</span></span> | <span data-ttu-id="0a7f6-233">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7f6-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-234">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a7f6-235">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a7f6-236">System-Only</span></span>            | <span data-ttu-id="0a7f6-237">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-237">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-238">Is-Single-Valued</span></span>       | <span data-ttu-id="0a7f6-239">對</span><span class="sxs-lookup"><span data-stu-id="0a7f6-239">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0a7f6-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0a7f6-240">Is Indexed</span></span>             | <span data-ttu-id="0a7f6-241">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-241">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0a7f6-242">In Global Catalog</span></span>      | <span data-ttu-id="0a7f6-243">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-243">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0a7f6-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a7f6-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0a7f6-245">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0a7f6-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a7f6-246">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a7f6-247">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-248">Search-Flags</span></span>           | <span data-ttu-id="0a7f6-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a7f6-249">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-250">System-Flags</span></span>           | <span data-ttu-id="0a7f6-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a7f6-251">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0a7f6-252">Classes used in</span></span>        | [<span data-ttu-id="0a7f6-253">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-253">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0a7f6-254">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-254">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0a7f6-255">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-255">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0a7f6-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0a7f6-256">Windows Server 2012</span></span>



| <span data-ttu-id="0a7f6-257">進入</span><span class="sxs-lookup"><span data-stu-id="0a7f6-257">Entry</span></span> | <span data-ttu-id="0a7f6-258">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7f6-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-259">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a7f6-260">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a7f6-261">System-Only</span></span>            | <span data-ttu-id="0a7f6-262">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-262">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-263">Is-Single-Valued</span></span>       | <span data-ttu-id="0a7f6-264">對</span><span class="sxs-lookup"><span data-stu-id="0a7f6-264">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="0a7f6-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0a7f6-265">Is Indexed</span></span>             | <span data-ttu-id="0a7f6-266">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-266">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0a7f6-267">In Global Catalog</span></span>      | <span data-ttu-id="0a7f6-268">否</span><span class="sxs-lookup"><span data-stu-id="0a7f6-268">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="0a7f6-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0a7f6-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a7f6-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0a7f6-270">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="0a7f6-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a7f6-271">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a7f6-272">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="0a7f6-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-273">Search-Flags</span></span>           | <span data-ttu-id="0a7f6-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a7f6-274">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a7f6-275">System-Flags</span></span>           | <span data-ttu-id="0a7f6-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a7f6-276">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="0a7f6-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0a7f6-277">Classes used in</span></span>        | [<span data-ttu-id="0a7f6-278">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-278">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="0a7f6-279">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-279">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="0a7f6-280">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-280">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





