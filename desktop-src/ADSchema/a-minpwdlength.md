---
title: 最小值-Pwd 長度屬性
description: 密碼必須包含的最小字元數。
ms.assetid: f1bd7b0c-cb78-4b03-88fe-dbdf472dab06
ms.tgt_platform: multiple
keywords:
- 最小-Pwd 長度屬性 AD 架構
- minPwdLength 屬性 AD 架構
topic_type:
- apiref
api_name:
- Min-Pwd-Length
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0d9a50ed05a651d7dd2d029d1c0b21c247c0ed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845212"
---
# <a name="min-pwd-length-attribute"></a><span data-ttu-id="ad184-105">最小值-Pwd 長度屬性</span><span class="sxs-lookup"><span data-stu-id="ad184-105">Min-Pwd-Length attribute</span></span>

<span data-ttu-id="ad184-106">密碼必須包含的最小字元數。</span><span class="sxs-lookup"><span data-stu-id="ad184-106">The minimum number of characters that a password must contain.</span></span>



| <span data-ttu-id="ad184-107">進入</span><span class="sxs-lookup"><span data-stu-id="ad184-107">Entry</span></span> | <span data-ttu-id="ad184-108">值</span><span class="sxs-lookup"><span data-stu-id="ad184-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ad184-109">CN</span><span class="sxs-lookup"><span data-stu-id="ad184-109">CN</span></span>                | <span data-ttu-id="ad184-110">最小-Pwd-長度</span><span class="sxs-lookup"><span data-stu-id="ad184-110">Min-Pwd-Length</span></span>                       |
| <span data-ttu-id="ad184-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ad184-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ad184-112">minPwdLength</span><span class="sxs-lookup"><span data-stu-id="ad184-112">minPwdLength</span></span>                         |
| <span data-ttu-id="ad184-113">大小</span><span class="sxs-lookup"><span data-stu-id="ad184-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="ad184-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ad184-114">Update Privilege</span></span>  | <span data-ttu-id="ad184-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="ad184-115">Domain administrator</span></span>                 |
| <span data-ttu-id="ad184-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ad184-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ad184-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad184-117">Attribute-Id</span></span>      | <span data-ttu-id="ad184-118">1.2.840.113556.1.4.79</span><span class="sxs-lookup"><span data-stu-id="ad184-118">1.2.840.113556.1.4.79</span></span>                |
| <span data-ttu-id="ad184-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ad184-119">System-Id-Guid</span></span>    | <span data-ttu-id="ad184-120">bf9679c3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ad184-120">bf9679c3-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ad184-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad184-121">Syntax</span></span>            | [<span data-ttu-id="ad184-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ad184-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ad184-123">實作</span><span class="sxs-lookup"><span data-stu-id="ad184-123">Implementations</span></span>

-   [<span data-ttu-id="ad184-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ad184-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ad184-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad184-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad184-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad184-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad184-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad184-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad184-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad184-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad184-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad184-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ad184-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad184-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ad184-131">進入</span><span class="sxs-lookup"><span data-stu-id="ad184-131">Entry</span></span> | <span data-ttu-id="ad184-132">值</span><span class="sxs-lookup"><span data-stu-id="ad184-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad184-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ad184-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad184-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad184-135">System-Only</span></span>            | <span data-ttu-id="ad184-136">否</span><span class="sxs-lookup"><span data-stu-id="ad184-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ad184-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ad184-138">對</span><span class="sxs-lookup"><span data-stu-id="ad184-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ad184-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ad184-139">Is Indexed</span></span>             | <span data-ttu-id="ad184-140">否</span><span class="sxs-lookup"><span data-stu-id="ad184-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ad184-141">In Global Catalog</span></span>      | <span data-ttu-id="ad184-142">否</span><span class="sxs-lookup"><span data-stu-id="ad184-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ad184-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad184-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ad184-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ad184-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad184-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad184-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-147">Search-Flags</span></span>           | <span data-ttu-id="ad184-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad184-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-149">System-Flags</span></span>           | <span data-ttu-id="ad184-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad184-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ad184-151">Classes used in</span></span>        | [<span data-ttu-id="ad184-152">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="ad184-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ad184-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="ad184-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ad184-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="ad184-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ad184-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad184-155">Windows Server 2003</span></span>



| <span data-ttu-id="ad184-156">進入</span><span class="sxs-lookup"><span data-stu-id="ad184-156">Entry</span></span> | <span data-ttu-id="ad184-157">值</span><span class="sxs-lookup"><span data-stu-id="ad184-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad184-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ad184-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad184-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad184-160">System-Only</span></span>            | <span data-ttu-id="ad184-161">否</span><span class="sxs-lookup"><span data-stu-id="ad184-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ad184-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ad184-163">對</span><span class="sxs-lookup"><span data-stu-id="ad184-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ad184-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ad184-164">Is Indexed</span></span>             | <span data-ttu-id="ad184-165">否</span><span class="sxs-lookup"><span data-stu-id="ad184-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ad184-166">In Global Catalog</span></span>      | <span data-ttu-id="ad184-167">否</span><span class="sxs-lookup"><span data-stu-id="ad184-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ad184-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad184-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ad184-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ad184-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad184-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad184-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-172">Search-Flags</span></span>           | <span data-ttu-id="ad184-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad184-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-174">System-Flags</span></span>           | <span data-ttu-id="ad184-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad184-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ad184-176">Classes used in</span></span>        | [<span data-ttu-id="ad184-177">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="ad184-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ad184-178">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="ad184-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ad184-179">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="ad184-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad184-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad184-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad184-181">進入</span><span class="sxs-lookup"><span data-stu-id="ad184-181">Entry</span></span> | <span data-ttu-id="ad184-182">值</span><span class="sxs-lookup"><span data-stu-id="ad184-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad184-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ad184-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad184-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad184-185">System-Only</span></span>            | <span data-ttu-id="ad184-186">否</span><span class="sxs-lookup"><span data-stu-id="ad184-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ad184-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ad184-188">對</span><span class="sxs-lookup"><span data-stu-id="ad184-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ad184-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ad184-189">Is Indexed</span></span>             | <span data-ttu-id="ad184-190">否</span><span class="sxs-lookup"><span data-stu-id="ad184-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ad184-191">In Global Catalog</span></span>      | <span data-ttu-id="ad184-192">否</span><span class="sxs-lookup"><span data-stu-id="ad184-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ad184-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad184-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ad184-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ad184-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad184-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad184-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-197">Search-Flags</span></span>           | <span data-ttu-id="ad184-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad184-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-199">System-Flags</span></span>           | <span data-ttu-id="ad184-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad184-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ad184-201">Classes used in</span></span>        | [<span data-ttu-id="ad184-202">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="ad184-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ad184-203">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="ad184-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ad184-204">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="ad184-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad184-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad184-205">Windows Server 2008</span></span>



| <span data-ttu-id="ad184-206">進入</span><span class="sxs-lookup"><span data-stu-id="ad184-206">Entry</span></span> | <span data-ttu-id="ad184-207">值</span><span class="sxs-lookup"><span data-stu-id="ad184-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad184-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ad184-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad184-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad184-210">System-Only</span></span>            | <span data-ttu-id="ad184-211">否</span><span class="sxs-lookup"><span data-stu-id="ad184-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ad184-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ad184-213">對</span><span class="sxs-lookup"><span data-stu-id="ad184-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ad184-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ad184-214">Is Indexed</span></span>             | <span data-ttu-id="ad184-215">否</span><span class="sxs-lookup"><span data-stu-id="ad184-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ad184-216">In Global Catalog</span></span>      | <span data-ttu-id="ad184-217">否</span><span class="sxs-lookup"><span data-stu-id="ad184-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ad184-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad184-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ad184-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ad184-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad184-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad184-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-222">Search-Flags</span></span>           | <span data-ttu-id="ad184-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad184-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-224">System-Flags</span></span>           | <span data-ttu-id="ad184-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad184-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ad184-226">Classes used in</span></span>        | [<span data-ttu-id="ad184-227">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="ad184-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ad184-228">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="ad184-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ad184-229">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="ad184-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad184-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad184-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad184-231">進入</span><span class="sxs-lookup"><span data-stu-id="ad184-231">Entry</span></span> | <span data-ttu-id="ad184-232">值</span><span class="sxs-lookup"><span data-stu-id="ad184-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad184-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ad184-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad184-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad184-235">System-Only</span></span>            | <span data-ttu-id="ad184-236">否</span><span class="sxs-lookup"><span data-stu-id="ad184-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ad184-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ad184-238">對</span><span class="sxs-lookup"><span data-stu-id="ad184-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ad184-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ad184-239">Is Indexed</span></span>             | <span data-ttu-id="ad184-240">否</span><span class="sxs-lookup"><span data-stu-id="ad184-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ad184-241">In Global Catalog</span></span>      | <span data-ttu-id="ad184-242">否</span><span class="sxs-lookup"><span data-stu-id="ad184-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ad184-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad184-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ad184-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ad184-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad184-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad184-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-247">Search-Flags</span></span>           | <span data-ttu-id="ad184-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad184-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-249">System-Flags</span></span>           | <span data-ttu-id="ad184-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad184-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ad184-251">Classes used in</span></span>        | [<span data-ttu-id="ad184-252">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="ad184-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ad184-253">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="ad184-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ad184-254">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="ad184-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad184-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad184-255">Windows Server 2012</span></span>



| <span data-ttu-id="ad184-256">進入</span><span class="sxs-lookup"><span data-stu-id="ad184-256">Entry</span></span> | <span data-ttu-id="ad184-257">值</span><span class="sxs-lookup"><span data-stu-id="ad184-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad184-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ad184-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad184-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad184-260">System-Only</span></span>            | <span data-ttu-id="ad184-261">否</span><span class="sxs-lookup"><span data-stu-id="ad184-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ad184-262">Is-Single-Valued</span></span>       | <span data-ttu-id="ad184-263">對</span><span class="sxs-lookup"><span data-stu-id="ad184-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ad184-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ad184-264">Is Indexed</span></span>             | <span data-ttu-id="ad184-265">否</span><span class="sxs-lookup"><span data-stu-id="ad184-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ad184-266">In Global Catalog</span></span>      | <span data-ttu-id="ad184-267">否</span><span class="sxs-lookup"><span data-stu-id="ad184-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ad184-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ad184-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad184-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ad184-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ad184-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad184-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad184-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ad184-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-272">Search-Flags</span></span>           | <span data-ttu-id="ad184-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad184-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad184-274">System-Flags</span></span>           | <span data-ttu-id="ad184-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad184-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ad184-276">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ad184-276">Classes used in</span></span>        | [<span data-ttu-id="ad184-277">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="ad184-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ad184-278">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="ad184-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ad184-279">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="ad184-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





