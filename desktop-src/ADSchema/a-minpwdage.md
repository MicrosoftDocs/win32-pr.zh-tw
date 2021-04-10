---
title: 最小-Pwd-Age 屬性
description: 密碼有效的最小時間量（以 100-毫微秒間隔）。
ms.assetid: c1ddd8a3-8481-4b6e-95ac-1cdc81a4cf78
ms.tgt_platform: multiple
keywords:
- 最小-Pwd-Age 屬性 AD 架構
- minPwdAge 屬性 AD 架構
topic_type:
- apiref
api_name:
- Min-Pwd-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c733f1a6f6803b10f04d6b0f9e367a9933cd9330
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107207"
---
# <a name="min-pwd-age-attribute"></a><span data-ttu-id="d9a6e-105">最小-Pwd-Age 屬性</span><span class="sxs-lookup"><span data-stu-id="d9a6e-105">Min-Pwd-Age attribute</span></span>

<span data-ttu-id="d9a6e-106">密碼有效的最小時間量（以 100-毫微秒間隔）。</span><span class="sxs-lookup"><span data-stu-id="d9a6e-106">The minimum amount of time, in 100-nanosecond intervals, that a password is valid.</span></span>



| <span data-ttu-id="d9a6e-107">進入</span><span class="sxs-lookup"><span data-stu-id="d9a6e-107">Entry</span></span> | <span data-ttu-id="d9a6e-108">值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d9a6e-109">CN</span><span class="sxs-lookup"><span data-stu-id="d9a6e-109">CN</span></span>                | <span data-ttu-id="d9a6e-110">最小-Pwd-使用期限</span><span class="sxs-lookup"><span data-stu-id="d9a6e-110">Min-Pwd-Age</span></span>                          |
| <span data-ttu-id="d9a6e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d9a6e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d9a6e-112">minPwdAge</span><span class="sxs-lookup"><span data-stu-id="d9a6e-112">minPwdAge</span></span>                            |
| <span data-ttu-id="d9a6e-113">大小</span><span class="sxs-lookup"><span data-stu-id="d9a6e-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="d9a6e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d9a6e-114">Update Privilege</span></span>  | <span data-ttu-id="d9a6e-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="d9a6e-115">Domain administrator</span></span>                 |
| <span data-ttu-id="d9a6e-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d9a6e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d9a6e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d9a6e-117">Attribute-Id</span></span>      | <span data-ttu-id="d9a6e-118">1.2.840.113556.1.4.78</span><span class="sxs-lookup"><span data-stu-id="d9a6e-118">1.2.840.113556.1.4.78</span></span>                |
| <span data-ttu-id="d9a6e-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d9a6e-119">System-Id-Guid</span></span>    | <span data-ttu-id="d9a6e-120">bf9679c2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d9a6e-120">bf9679c2-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="d9a6e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9a6e-121">Syntax</span></span>            | [<span data-ttu-id="d9a6e-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="d9a6e-123">實作</span><span class="sxs-lookup"><span data-stu-id="d9a6e-123">Implementations</span></span>

-   [<span data-ttu-id="d9a6e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d9a6e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d9a6e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d9a6e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d9a6e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d9a6e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d9a6e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d9a6e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d9a6e-131">進入</span><span class="sxs-lookup"><span data-stu-id="d9a6e-131">Entry</span></span> | <span data-ttu-id="d9a6e-132">值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6e-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d9a6e-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a6e-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a6e-135">System-Only</span></span>            | <span data-ttu-id="d9a6e-136">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a6e-138">對</span><span class="sxs-lookup"><span data-stu-id="d9a6e-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="d9a6e-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d9a6e-139">Is Indexed</span></span>             | <span data-ttu-id="d9a6e-140">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d9a6e-141">In Global Catalog</span></span>      | <span data-ttu-id="d9a6e-142">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d9a6e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a6e-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d9a6e-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="d9a6e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a6e-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a6e-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-147">Search-Flags</span></span>           | <span data-ttu-id="d9a6e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a6e-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-149">System-Flags</span></span>           | <span data-ttu-id="d9a6e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a6e-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d9a6e-151">Classes used in</span></span>        | [<span data-ttu-id="d9a6e-152">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9a6e-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="d9a6e-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d9a6e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9a6e-155">Windows Server 2003</span></span>



| <span data-ttu-id="d9a6e-156">進入</span><span class="sxs-lookup"><span data-stu-id="d9a6e-156">Entry</span></span> | <span data-ttu-id="d9a6e-157">值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6e-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d9a6e-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a6e-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a6e-160">System-Only</span></span>            | <span data-ttu-id="d9a6e-161">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a6e-163">對</span><span class="sxs-lookup"><span data-stu-id="d9a6e-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="d9a6e-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d9a6e-164">Is Indexed</span></span>             | <span data-ttu-id="d9a6e-165">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d9a6e-166">In Global Catalog</span></span>      | <span data-ttu-id="d9a6e-167">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d9a6e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a6e-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d9a6e-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="d9a6e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a6e-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a6e-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-172">Search-Flags</span></span>           | <span data-ttu-id="d9a6e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a6e-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-174">System-Flags</span></span>           | <span data-ttu-id="d9a6e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a6e-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d9a6e-176">Classes used in</span></span>        | [<span data-ttu-id="d9a6e-177">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9a6e-178">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="d9a6e-179">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d9a6e-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d9a6e-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d9a6e-181">進入</span><span class="sxs-lookup"><span data-stu-id="d9a6e-181">Entry</span></span> | <span data-ttu-id="d9a6e-182">值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6e-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d9a6e-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a6e-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a6e-185">System-Only</span></span>            | <span data-ttu-id="d9a6e-186">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-187">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a6e-188">對</span><span class="sxs-lookup"><span data-stu-id="d9a6e-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="d9a6e-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d9a6e-189">Is Indexed</span></span>             | <span data-ttu-id="d9a6e-190">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d9a6e-191">In Global Catalog</span></span>      | <span data-ttu-id="d9a6e-192">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d9a6e-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a6e-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d9a6e-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="d9a6e-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a6e-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a6e-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-197">Search-Flags</span></span>           | <span data-ttu-id="d9a6e-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a6e-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-199">System-Flags</span></span>           | <span data-ttu-id="d9a6e-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a6e-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d9a6e-201">Classes used in</span></span>        | [<span data-ttu-id="d9a6e-202">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9a6e-203">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="d9a6e-204">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d9a6e-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9a6e-205">Windows Server 2008</span></span>



| <span data-ttu-id="d9a6e-206">進入</span><span class="sxs-lookup"><span data-stu-id="d9a6e-206">Entry</span></span> | <span data-ttu-id="d9a6e-207">值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6e-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d9a6e-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a6e-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a6e-210">System-Only</span></span>            | <span data-ttu-id="d9a6e-211">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a6e-213">對</span><span class="sxs-lookup"><span data-stu-id="d9a6e-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="d9a6e-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d9a6e-214">Is Indexed</span></span>             | <span data-ttu-id="d9a6e-215">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d9a6e-216">In Global Catalog</span></span>      | <span data-ttu-id="d9a6e-217">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d9a6e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a6e-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d9a6e-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="d9a6e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a6e-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a6e-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-222">Search-Flags</span></span>           | <span data-ttu-id="d9a6e-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a6e-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-224">System-Flags</span></span>           | <span data-ttu-id="d9a6e-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a6e-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d9a6e-226">Classes used in</span></span>        | [<span data-ttu-id="d9a6e-227">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9a6e-228">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="d9a6e-229">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d9a6e-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9a6e-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d9a6e-231">進入</span><span class="sxs-lookup"><span data-stu-id="d9a6e-231">Entry</span></span> | <span data-ttu-id="d9a6e-232">值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6e-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d9a6e-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a6e-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a6e-235">System-Only</span></span>            | <span data-ttu-id="d9a6e-236">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-237">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a6e-238">對</span><span class="sxs-lookup"><span data-stu-id="d9a6e-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="d9a6e-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d9a6e-239">Is Indexed</span></span>             | <span data-ttu-id="d9a6e-240">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d9a6e-241">In Global Catalog</span></span>      | <span data-ttu-id="d9a6e-242">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d9a6e-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a6e-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d9a6e-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="d9a6e-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a6e-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a6e-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-247">Search-Flags</span></span>           | <span data-ttu-id="d9a6e-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a6e-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-249">System-Flags</span></span>           | <span data-ttu-id="d9a6e-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a6e-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d9a6e-251">Classes used in</span></span>        | [<span data-ttu-id="d9a6e-252">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9a6e-253">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="d9a6e-254">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d9a6e-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9a6e-255">Windows Server 2012</span></span>



| <span data-ttu-id="d9a6e-256">進入</span><span class="sxs-lookup"><span data-stu-id="d9a6e-256">Entry</span></span> | <span data-ttu-id="d9a6e-257">值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6e-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d9a6e-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9a6e-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9a6e-260">System-Only</span></span>            | <span data-ttu-id="d9a6e-261">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d9a6e-262">Is-Single-Valued</span></span>       | <span data-ttu-id="d9a6e-263">對</span><span class="sxs-lookup"><span data-stu-id="d9a6e-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="d9a6e-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d9a6e-264">Is Indexed</span></span>             | <span data-ttu-id="d9a6e-265">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d9a6e-266">In Global Catalog</span></span>      | <span data-ttu-id="d9a6e-267">否</span><span class="sxs-lookup"><span data-stu-id="d9a6e-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="d9a6e-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d9a6e-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9a6e-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d9a6e-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="d9a6e-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9a6e-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9a6e-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="d9a6e-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-272">Search-Flags</span></span>           | <span data-ttu-id="d9a6e-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9a6e-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9a6e-274">System-Flags</span></span>           | <span data-ttu-id="d9a6e-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9a6e-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="d9a6e-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d9a6e-276">Classes used in</span></span>        | [<span data-ttu-id="d9a6e-277">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="d9a6e-278">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="d9a6e-279">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="d9a6e-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





