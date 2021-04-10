---
title: Force-Logoff 屬性
description: 用來計算 SamIGetAccountRestrictions 的啟動時間。 登出時間減去強制登出的時間等於啟動時間。
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- Force-Logoff 屬性 AD 架構
- forceLogoff 屬性 AD 架構
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e31cb241cde4deb40d5978594b4354fbcc564b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107087"
---
# <a name="force-logoff-attribute"></a><span data-ttu-id="b2be6-106">Force-Logoff 屬性</span><span class="sxs-lookup"><span data-stu-id="b2be6-106">Force-Logoff attribute</span></span>

<span data-ttu-id="b2be6-107">用來計算 SamIGetAccountRestrictions 的啟動時間。</span><span class="sxs-lookup"><span data-stu-id="b2be6-107">Used in computing the kick off time in SamIGetAccountRestrictions.</span></span> <span data-ttu-id="b2be6-108">登出時間減去強制登出的時間等於啟動時間。</span><span class="sxs-lookup"><span data-stu-id="b2be6-108">Logoff time minus Force Log off equals kick off time.</span></span>



| <span data-ttu-id="b2be6-109">進入</span><span class="sxs-lookup"><span data-stu-id="b2be6-109">Entry</span></span> | <span data-ttu-id="b2be6-110">值</span><span class="sxs-lookup"><span data-stu-id="b2be6-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b2be6-111">CN</span><span class="sxs-lookup"><span data-stu-id="b2be6-111">CN</span></span>                | <span data-ttu-id="b2be6-112">Force-Logoff</span><span class="sxs-lookup"><span data-stu-id="b2be6-112">Force-Logoff</span></span>                         |
| <span data-ttu-id="b2be6-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b2be6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b2be6-114">forceLogoff</span><span class="sxs-lookup"><span data-stu-id="b2be6-114">forceLogoff</span></span>                          |
| <span data-ttu-id="b2be6-115">大小</span><span class="sxs-lookup"><span data-stu-id="b2be6-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b2be6-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b2be6-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b2be6-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b2be6-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b2be6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b2be6-118">Attribute-Id</span></span>      | <span data-ttu-id="b2be6-119">1.2.840.113556.1.4.39</span><span class="sxs-lookup"><span data-stu-id="b2be6-119">1.2.840.113556.1.4.39</span></span>                |
| <span data-ttu-id="b2be6-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b2be6-120">System-Id-Guid</span></span>    | <span data-ttu-id="b2be6-121">bf967977-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b2be6-121">bf967977-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b2be6-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2be6-122">Syntax</span></span>            | [<span data-ttu-id="b2be6-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="b2be6-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b2be6-124">實作</span><span class="sxs-lookup"><span data-stu-id="b2be6-124">Implementations</span></span>

-   [<span data-ttu-id="b2be6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b2be6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b2be6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b2be6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b2be6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b2be6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b2be6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b2be6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b2be6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b2be6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b2be6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b2be6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b2be6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2be6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b2be6-132">進入</span><span class="sxs-lookup"><span data-stu-id="b2be6-132">Entry</span></span> | <span data-ttu-id="b2be6-133">值</span><span class="sxs-lookup"><span data-stu-id="b2be6-133">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2be6-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2be6-134">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2be6-135">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2be6-136">System-Only</span></span>            | <span data-ttu-id="b2be6-137">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-137">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2be6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b2be6-139">對</span><span class="sxs-lookup"><span data-stu-id="b2be6-139">True</span></span>                                                                                                     |
| <span data-ttu-id="b2be6-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2be6-140">Is Indexed</span></span>             | <span data-ttu-id="b2be6-141">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-141">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2be6-142">In Global Catalog</span></span>      | <span data-ttu-id="b2be6-143">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-143">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2be6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2be6-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2be6-145">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="b2be6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2be6-146">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2be6-147">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-148">Search-Flags</span></span>           | <span data-ttu-id="b2be6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2be6-149">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="b2be6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-150">System-Flags</span></span>           | <span data-ttu-id="b2be6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2be6-151">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="b2be6-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2be6-152">Classes used in</span></span>        | [<span data-ttu-id="b2be6-153">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b2be6-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b2be6-154">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b2be6-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b2be6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2be6-155">Windows Server 2003</span></span>



| <span data-ttu-id="b2be6-156">進入</span><span class="sxs-lookup"><span data-stu-id="b2be6-156">Entry</span></span> | <span data-ttu-id="b2be6-157">值</span><span class="sxs-lookup"><span data-stu-id="b2be6-157">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2be6-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2be6-158">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2be6-159">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2be6-160">System-Only</span></span>            | <span data-ttu-id="b2be6-161">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-161">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2be6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b2be6-163">對</span><span class="sxs-lookup"><span data-stu-id="b2be6-163">True</span></span>                                                                                                     |
| <span data-ttu-id="b2be6-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2be6-164">Is Indexed</span></span>             | <span data-ttu-id="b2be6-165">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-165">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2be6-166">In Global Catalog</span></span>      | <span data-ttu-id="b2be6-167">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-167">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2be6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2be6-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2be6-169">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="b2be6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2be6-170">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2be6-171">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-172">Search-Flags</span></span>           | <span data-ttu-id="b2be6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2be6-173">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="b2be6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-174">System-Flags</span></span>           | <span data-ttu-id="b2be6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2be6-175">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="b2be6-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2be6-176">Classes used in</span></span>        | [<span data-ttu-id="b2be6-177">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b2be6-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b2be6-178">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b2be6-178">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b2be6-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b2be6-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b2be6-180">進入</span><span class="sxs-lookup"><span data-stu-id="b2be6-180">Entry</span></span> | <span data-ttu-id="b2be6-181">值</span><span class="sxs-lookup"><span data-stu-id="b2be6-181">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2be6-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2be6-182">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2be6-183">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2be6-184">System-Only</span></span>            | <span data-ttu-id="b2be6-185">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-185">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2be6-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b2be6-187">對</span><span class="sxs-lookup"><span data-stu-id="b2be6-187">True</span></span>                                                                                                     |
| <span data-ttu-id="b2be6-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2be6-188">Is Indexed</span></span>             | <span data-ttu-id="b2be6-189">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-189">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2be6-190">In Global Catalog</span></span>      | <span data-ttu-id="b2be6-191">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-191">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2be6-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2be6-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2be6-193">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="b2be6-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2be6-194">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2be6-195">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-196">Search-Flags</span></span>           | <span data-ttu-id="b2be6-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2be6-197">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="b2be6-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-198">System-Flags</span></span>           | <span data-ttu-id="b2be6-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2be6-199">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="b2be6-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2be6-200">Classes used in</span></span>        | [<span data-ttu-id="b2be6-201">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b2be6-201">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b2be6-202">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b2be6-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b2be6-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2be6-203">Windows Server 2008</span></span>



| <span data-ttu-id="b2be6-204">進入</span><span class="sxs-lookup"><span data-stu-id="b2be6-204">Entry</span></span> | <span data-ttu-id="b2be6-205">值</span><span class="sxs-lookup"><span data-stu-id="b2be6-205">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2be6-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2be6-206">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2be6-207">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2be6-208">System-Only</span></span>            | <span data-ttu-id="b2be6-209">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-209">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2be6-210">Is-Single-Valued</span></span>       | <span data-ttu-id="b2be6-211">對</span><span class="sxs-lookup"><span data-stu-id="b2be6-211">True</span></span>                                                                                                     |
| <span data-ttu-id="b2be6-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2be6-212">Is Indexed</span></span>             | <span data-ttu-id="b2be6-213">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-213">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2be6-214">In Global Catalog</span></span>      | <span data-ttu-id="b2be6-215">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-215">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2be6-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2be6-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2be6-217">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="b2be6-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2be6-218">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2be6-219">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-220">Search-Flags</span></span>           | <span data-ttu-id="b2be6-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2be6-221">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="b2be6-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-222">System-Flags</span></span>           | <span data-ttu-id="b2be6-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2be6-223">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="b2be6-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2be6-224">Classes used in</span></span>        | [<span data-ttu-id="b2be6-225">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b2be6-225">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b2be6-226">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b2be6-226">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b2be6-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2be6-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b2be6-228">進入</span><span class="sxs-lookup"><span data-stu-id="b2be6-228">Entry</span></span> | <span data-ttu-id="b2be6-229">值</span><span class="sxs-lookup"><span data-stu-id="b2be6-229">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2be6-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2be6-230">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2be6-231">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2be6-232">System-Only</span></span>            | <span data-ttu-id="b2be6-233">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-233">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2be6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="b2be6-235">對</span><span class="sxs-lookup"><span data-stu-id="b2be6-235">True</span></span>                                                                                                     |
| <span data-ttu-id="b2be6-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2be6-236">Is Indexed</span></span>             | <span data-ttu-id="b2be6-237">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-237">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2be6-238">In Global Catalog</span></span>      | <span data-ttu-id="b2be6-239">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-239">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2be6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2be6-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2be6-241">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="b2be6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2be6-242">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2be6-243">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-244">Search-Flags</span></span>           | <span data-ttu-id="b2be6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2be6-245">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="b2be6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-246">System-Flags</span></span>           | <span data-ttu-id="b2be6-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2be6-247">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="b2be6-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2be6-248">Classes used in</span></span>        | [<span data-ttu-id="b2be6-249">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b2be6-249">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b2be6-250">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b2be6-250">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b2be6-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2be6-251">Windows Server 2012</span></span>



| <span data-ttu-id="b2be6-252">進入</span><span class="sxs-lookup"><span data-stu-id="b2be6-252">Entry</span></span> | <span data-ttu-id="b2be6-253">值</span><span class="sxs-lookup"><span data-stu-id="b2be6-253">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2be6-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b2be6-254">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2be6-255">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="b2be6-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2be6-256">System-Only</span></span>            | <span data-ttu-id="b2be6-257">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-257">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b2be6-258">Is-Single-Valued</span></span>       | <span data-ttu-id="b2be6-259">對</span><span class="sxs-lookup"><span data-stu-id="b2be6-259">True</span></span>                                                                                                     |
| <span data-ttu-id="b2be6-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b2be6-260">Is Indexed</span></span>             | <span data-ttu-id="b2be6-261">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-261">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b2be6-262">In Global Catalog</span></span>      | <span data-ttu-id="b2be6-263">否</span><span class="sxs-lookup"><span data-stu-id="b2be6-263">False</span></span>                                                                                                    |
| <span data-ttu-id="b2be6-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b2be6-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2be6-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b2be6-265">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="b2be6-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2be6-266">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2be6-267">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="b2be6-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-268">Search-Flags</span></span>           | <span data-ttu-id="b2be6-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2be6-269">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="b2be6-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2be6-270">System-Flags</span></span>           | <span data-ttu-id="b2be6-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2be6-271">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="b2be6-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b2be6-272">Classes used in</span></span>        | [<span data-ttu-id="b2be6-273">**網域原則**</span><span class="sxs-lookup"><span data-stu-id="b2be6-273">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="b2be6-274">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="b2be6-274">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





