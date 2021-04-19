---
title: Account-Expires 屬性
description: 帳戶到期的日期。
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- Account-Expires 屬性 AD 架構
- accountExpires 屬性 AD 架構
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106997054"
---
# <a name="account-expires-attribute"></a><span data-ttu-id="100c7-105">Account-Expires 屬性</span><span class="sxs-lookup"><span data-stu-id="100c7-105">Account-Expires attribute</span></span>

<span data-ttu-id="100c7-106">帳戶到期的日期。</span><span class="sxs-lookup"><span data-stu-id="100c7-106">The date when the account expires.</span></span> <span data-ttu-id="100c7-107">此值代表自1601年1月1日 (UTC) 起的 100-毫微秒間隔數。</span><span class="sxs-lookup"><span data-stu-id="100c7-107">This value represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="100c7-108">值為0或 0x7FFFFFFFFFFFFFFF (9223372036854775807) 表示帳戶永遠不會過期。</span><span class="sxs-lookup"><span data-stu-id="100c7-108">A value of 0 or 0x7FFFFFFFFFFFFFFF (9223372036854775807) indicates that the account never expires.</span></span>



| <span data-ttu-id="100c7-109">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-109">Entry</span></span> | <span data-ttu-id="100c7-110">值</span><span class="sxs-lookup"><span data-stu-id="100c7-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="100c7-111">CN</span><span class="sxs-lookup"><span data-stu-id="100c7-111">CN</span></span>                | <span data-ttu-id="100c7-112">Account-Expires</span><span class="sxs-lookup"><span data-stu-id="100c7-112">Account-Expires</span></span>                                                        |
| <span data-ttu-id="100c7-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="100c7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="100c7-114">accountExpires</span><span class="sxs-lookup"><span data-stu-id="100c7-114">accountExpires</span></span>                                                         |
| <span data-ttu-id="100c7-115">大小</span><span class="sxs-lookup"><span data-stu-id="100c7-115">Size</span></span>              | <span data-ttu-id="100c7-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="100c7-116">8 bytes</span></span>                                                                |
| <span data-ttu-id="100c7-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="100c7-117">Update Privilege</span></span>  | <span data-ttu-id="100c7-118">網域系統管理員會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="100c7-118">The domain administrator sets this attribute.</span></span>                          |
| <span data-ttu-id="100c7-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="100c7-119">Update Frequency</span></span>  | <span data-ttu-id="100c7-120">當先前的到期日過期且需要更新時。</span><span class="sxs-lookup"><span data-stu-id="100c7-120">Whenever the previous expiration date expires and needs to be updated.</span></span> |
| <span data-ttu-id="100c7-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-121">Attribute-Id</span></span>      | <span data-ttu-id="100c7-122">1.2.840.113556.1.4.159</span><span class="sxs-lookup"><span data-stu-id="100c7-122">1.2.840.113556.1.4.159</span></span>                                                 |
| <span data-ttu-id="100c7-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="100c7-123">System-Id-Guid</span></span>    | <span data-ttu-id="100c7-124">bf967915-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="100c7-124">bf967915-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="100c7-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="100c7-125">Syntax</span></span>            | [<span data-ttu-id="100c7-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="100c7-126">**Interval**</span></span>](s-interval.md)                                         |



## <a name="implementations"></a><span data-ttu-id="100c7-127">實作</span><span class="sxs-lookup"><span data-stu-id="100c7-127">Implementations</span></span>

-   [<span data-ttu-id="100c7-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="100c7-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="100c7-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="100c7-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="100c7-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="100c7-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="100c7-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="100c7-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="100c7-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="100c7-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="100c7-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="100c7-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="100c7-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="100c7-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="100c7-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="100c7-135">Windows 2000 Server</span></span>



| <span data-ttu-id="100c7-136">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-136">Entry</span></span> | <span data-ttu-id="100c7-137">值</span><span class="sxs-lookup"><span data-stu-id="100c7-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="100c7-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="100c7-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="100c7-140">System-Only</span></span>            | <span data-ttu-id="100c7-141">否</span><span class="sxs-lookup"><span data-stu-id="100c7-141">False</span></span>                             |
| <span data-ttu-id="100c7-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="100c7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="100c7-143">對</span><span class="sxs-lookup"><span data-stu-id="100c7-143">True</span></span>                              |
| <span data-ttu-id="100c7-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="100c7-144">Is Indexed</span></span>             | <span data-ttu-id="100c7-145">否</span><span class="sxs-lookup"><span data-stu-id="100c7-145">False</span></span>                             |
| <span data-ttu-id="100c7-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="100c7-146">In Global Catalog</span></span>      | <span data-ttu-id="100c7-147">否</span><span class="sxs-lookup"><span data-stu-id="100c7-147">False</span></span>                             |
| <span data-ttu-id="100c7-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="100c7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="100c7-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="100c7-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="100c7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="100c7-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="100c7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="100c7-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="100c7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-152">Search-Flags</span></span>           | <span data-ttu-id="100c7-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-153">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-154">System-Flags</span></span>           | <span data-ttu-id="100c7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-155">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="100c7-156">Classes used in</span></span>        | [<span data-ttu-id="100c7-157">**User**</span><span class="sxs-lookup"><span data-stu-id="100c7-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="100c7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="100c7-158">Windows Server 2003</span></span>



| <span data-ttu-id="100c7-159">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-159">Entry</span></span> | <span data-ttu-id="100c7-160">值</span><span class="sxs-lookup"><span data-stu-id="100c7-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="100c7-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="100c7-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="100c7-163">System-Only</span></span>            | <span data-ttu-id="100c7-164">否</span><span class="sxs-lookup"><span data-stu-id="100c7-164">False</span></span>                             |
| <span data-ttu-id="100c7-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="100c7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="100c7-166">對</span><span class="sxs-lookup"><span data-stu-id="100c7-166">True</span></span>                              |
| <span data-ttu-id="100c7-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="100c7-167">Is Indexed</span></span>             | <span data-ttu-id="100c7-168">否</span><span class="sxs-lookup"><span data-stu-id="100c7-168">False</span></span>                             |
| <span data-ttu-id="100c7-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="100c7-169">In Global Catalog</span></span>      | <span data-ttu-id="100c7-170">否</span><span class="sxs-lookup"><span data-stu-id="100c7-170">False</span></span>                             |
| <span data-ttu-id="100c7-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="100c7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="100c7-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="100c7-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="100c7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="100c7-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="100c7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="100c7-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="100c7-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-175">Search-Flags</span></span>           | <span data-ttu-id="100c7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-176">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-177">System-Flags</span></span>           | <span data-ttu-id="100c7-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-178">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="100c7-179">Classes used in</span></span>        | [<span data-ttu-id="100c7-180">**User**</span><span class="sxs-lookup"><span data-stu-id="100c7-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="100c7-181">亞當</span><span class="sxs-lookup"><span data-stu-id="100c7-181">ADAM</span></span>



| <span data-ttu-id="100c7-182">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-182">Entry</span></span> | <span data-ttu-id="100c7-183">值</span><span class="sxs-lookup"><span data-stu-id="100c7-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="100c7-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="100c7-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="100c7-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="100c7-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="100c7-186">System-Only</span></span>            | <span data-ttu-id="100c7-187">否</span><span class="sxs-lookup"><span data-stu-id="100c7-187">False</span></span>                                                             |
| <span data-ttu-id="100c7-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="100c7-188">Is-Single-Valued</span></span>       | <span data-ttu-id="100c7-189">對</span><span class="sxs-lookup"><span data-stu-id="100c7-189">True</span></span>                                                              |
| <span data-ttu-id="100c7-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="100c7-190">Is Indexed</span></span>             | <span data-ttu-id="100c7-191">否</span><span class="sxs-lookup"><span data-stu-id="100c7-191">False</span></span>                                                             |
| <span data-ttu-id="100c7-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="100c7-192">In Global Catalog</span></span>      | <span data-ttu-id="100c7-193">否</span><span class="sxs-lookup"><span data-stu-id="100c7-193">False</span></span>                                                             |
| <span data-ttu-id="100c7-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="100c7-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="100c7-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="100c7-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="100c7-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="100c7-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="100c7-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="100c7-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="100c7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-198">Search-Flags</span></span>           | <span data-ttu-id="100c7-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-199">0x00000010</span></span>                                                        |
| <span data-ttu-id="100c7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-200">System-Flags</span></span>           | <span data-ttu-id="100c7-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="100c7-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="100c7-202">Classes used in</span></span>        | [<span data-ttu-id="100c7-203">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="100c7-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="100c7-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="100c7-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="100c7-205">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-205">Entry</span></span> | <span data-ttu-id="100c7-206">值</span><span class="sxs-lookup"><span data-stu-id="100c7-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="100c7-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="100c7-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="100c7-209">System-Only</span></span>            | <span data-ttu-id="100c7-210">否</span><span class="sxs-lookup"><span data-stu-id="100c7-210">False</span></span>                             |
| <span data-ttu-id="100c7-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="100c7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="100c7-212">對</span><span class="sxs-lookup"><span data-stu-id="100c7-212">True</span></span>                              |
| <span data-ttu-id="100c7-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="100c7-213">Is Indexed</span></span>             | <span data-ttu-id="100c7-214">否</span><span class="sxs-lookup"><span data-stu-id="100c7-214">False</span></span>                             |
| <span data-ttu-id="100c7-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="100c7-215">In Global Catalog</span></span>      | <span data-ttu-id="100c7-216">否</span><span class="sxs-lookup"><span data-stu-id="100c7-216">False</span></span>                             |
| <span data-ttu-id="100c7-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="100c7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="100c7-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="100c7-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="100c7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="100c7-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="100c7-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="100c7-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="100c7-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-221">Search-Flags</span></span>           | <span data-ttu-id="100c7-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-222">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-223">System-Flags</span></span>           | <span data-ttu-id="100c7-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-224">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="100c7-225">Classes used in</span></span>        | [<span data-ttu-id="100c7-226">**User**</span><span class="sxs-lookup"><span data-stu-id="100c7-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="100c7-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="100c7-227">Windows Server 2008</span></span>



| <span data-ttu-id="100c7-228">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-228">Entry</span></span> | <span data-ttu-id="100c7-229">值</span><span class="sxs-lookup"><span data-stu-id="100c7-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="100c7-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="100c7-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="100c7-232">System-Only</span></span>            | <span data-ttu-id="100c7-233">否</span><span class="sxs-lookup"><span data-stu-id="100c7-233">False</span></span>                             |
| <span data-ttu-id="100c7-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="100c7-234">Is-Single-Valued</span></span>       | <span data-ttu-id="100c7-235">對</span><span class="sxs-lookup"><span data-stu-id="100c7-235">True</span></span>                              |
| <span data-ttu-id="100c7-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="100c7-236">Is Indexed</span></span>             | <span data-ttu-id="100c7-237">否</span><span class="sxs-lookup"><span data-stu-id="100c7-237">False</span></span>                             |
| <span data-ttu-id="100c7-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="100c7-238">In Global Catalog</span></span>      | <span data-ttu-id="100c7-239">否</span><span class="sxs-lookup"><span data-stu-id="100c7-239">False</span></span>                             |
| <span data-ttu-id="100c7-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="100c7-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="100c7-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="100c7-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="100c7-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="100c7-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="100c7-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="100c7-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="100c7-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-244">Search-Flags</span></span>           | <span data-ttu-id="100c7-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-245">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-246">System-Flags</span></span>           | <span data-ttu-id="100c7-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-247">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="100c7-248">Classes used in</span></span>        | [<span data-ttu-id="100c7-249">**User**</span><span class="sxs-lookup"><span data-stu-id="100c7-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="100c7-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="100c7-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="100c7-251">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-251">Entry</span></span> | <span data-ttu-id="100c7-252">值</span><span class="sxs-lookup"><span data-stu-id="100c7-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="100c7-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="100c7-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="100c7-255">System-Only</span></span>            | <span data-ttu-id="100c7-256">否</span><span class="sxs-lookup"><span data-stu-id="100c7-256">False</span></span>                             |
| <span data-ttu-id="100c7-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="100c7-257">Is-Single-Valued</span></span>       | <span data-ttu-id="100c7-258">對</span><span class="sxs-lookup"><span data-stu-id="100c7-258">True</span></span>                              |
| <span data-ttu-id="100c7-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="100c7-259">Is Indexed</span></span>             | <span data-ttu-id="100c7-260">否</span><span class="sxs-lookup"><span data-stu-id="100c7-260">False</span></span>                             |
| <span data-ttu-id="100c7-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="100c7-261">In Global Catalog</span></span>      | <span data-ttu-id="100c7-262">否</span><span class="sxs-lookup"><span data-stu-id="100c7-262">False</span></span>                             |
| <span data-ttu-id="100c7-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="100c7-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="100c7-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="100c7-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="100c7-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="100c7-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="100c7-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="100c7-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="100c7-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-267">Search-Flags</span></span>           | <span data-ttu-id="100c7-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-268">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-269">System-Flags</span></span>           | <span data-ttu-id="100c7-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-270">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="100c7-271">Classes used in</span></span>        | [<span data-ttu-id="100c7-272">**User**</span><span class="sxs-lookup"><span data-stu-id="100c7-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="100c7-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="100c7-273">Windows Server 2012</span></span>



| <span data-ttu-id="100c7-274">進入</span><span class="sxs-lookup"><span data-stu-id="100c7-274">Entry</span></span> | <span data-ttu-id="100c7-275">值</span><span class="sxs-lookup"><span data-stu-id="100c7-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="100c7-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="100c7-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="100c7-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="100c7-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="100c7-278">System-Only</span></span>            | <span data-ttu-id="100c7-279">否</span><span class="sxs-lookup"><span data-stu-id="100c7-279">False</span></span>                             |
| <span data-ttu-id="100c7-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="100c7-280">Is-Single-Valued</span></span>       | <span data-ttu-id="100c7-281">對</span><span class="sxs-lookup"><span data-stu-id="100c7-281">True</span></span>                              |
| <span data-ttu-id="100c7-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="100c7-282">Is Indexed</span></span>             | <span data-ttu-id="100c7-283">否</span><span class="sxs-lookup"><span data-stu-id="100c7-283">False</span></span>                             |
| <span data-ttu-id="100c7-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="100c7-284">In Global Catalog</span></span>      | <span data-ttu-id="100c7-285">否</span><span class="sxs-lookup"><span data-stu-id="100c7-285">False</span></span>                             |
| <span data-ttu-id="100c7-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="100c7-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="100c7-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="100c7-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="100c7-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="100c7-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="100c7-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="100c7-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="100c7-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-290">Search-Flags</span></span>           | <span data-ttu-id="100c7-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-291">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="100c7-292">System-Flags</span></span>           | <span data-ttu-id="100c7-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="100c7-293">0x00000010</span></span>                        |
| <span data-ttu-id="100c7-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="100c7-294">Classes used in</span></span>        | [<span data-ttu-id="100c7-295">**User**</span><span class="sxs-lookup"><span data-stu-id="100c7-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="100c7-296">備註</span><span class="sxs-lookup"><span data-stu-id="100c7-296">Remarks</span></span>

<span data-ttu-id="100c7-297">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="100c7-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

 

