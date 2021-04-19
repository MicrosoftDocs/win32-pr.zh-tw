---
title: Lockout-Time 屬性
description: 此帳戶被鎖定的日期和時間 (UTC) 。
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Lockout-Time 屬性 AD 架構
- lockoutTime 屬性 AD 架構
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966568"
---
# <a name="lockout-time-attribute"></a><span data-ttu-id="531fb-105">Lockout-Time 屬性</span><span class="sxs-lookup"><span data-stu-id="531fb-105">Lockout-Time attribute</span></span>

<span data-ttu-id="531fb-106">此帳戶被鎖定的日期和時間 (UTC) 。此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="531fb-106">The date and time (UTC) that this account was locked out. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="531fb-107">值為零表示帳戶目前未被鎖定。</span><span class="sxs-lookup"><span data-stu-id="531fb-107">A value of zero means that the account is not currently locked out.</span></span>



| <span data-ttu-id="531fb-108">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-108">Entry</span></span> | <span data-ttu-id="531fb-109">值</span><span class="sxs-lookup"><span data-stu-id="531fb-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="531fb-110">CN</span><span class="sxs-lookup"><span data-stu-id="531fb-110">CN</span></span>                | <span data-ttu-id="531fb-111">Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="531fb-111">Lockout-Time</span></span>                                                                     |
| <span data-ttu-id="531fb-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="531fb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="531fb-113">lockoutTime</span><span class="sxs-lookup"><span data-stu-id="531fb-113">lockoutTime</span></span>                                                                      |
| <span data-ttu-id="531fb-114">大小</span><span class="sxs-lookup"><span data-stu-id="531fb-114">Size</span></span>              | <span data-ttu-id="531fb-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="531fb-115">8 bytes</span></span>                                                                          |
| <span data-ttu-id="531fb-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="531fb-116">Update Privilege</span></span>  | <span data-ttu-id="531fb-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="531fb-117">Domain administrator</span></span>                                                             |
| <span data-ttu-id="531fb-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="531fb-118">Update Frequency</span></span>  | <span data-ttu-id="531fb-119">當使用者的記錄建立時，以及每次需要變更鎖定時間時。</span><span class="sxs-lookup"><span data-stu-id="531fb-119">When the user's record is created and whenever the lockout time needs to change.</span></span> |
| <span data-ttu-id="531fb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-120">Attribute-Id</span></span>      | <span data-ttu-id="531fb-121">1.2.840.113556.1.4.662</span><span class="sxs-lookup"><span data-stu-id="531fb-121">1.2.840.113556.1.4.662</span></span>                                                           |
| <span data-ttu-id="531fb-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="531fb-122">System-Id-Guid</span></span>    | <span data-ttu-id="531fb-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="531fb-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span></span>                                             |
| <span data-ttu-id="531fb-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="531fb-124">Syntax</span></span>            | [<span data-ttu-id="531fb-125">**間隔**</span><span class="sxs-lookup"><span data-stu-id="531fb-125">**Interval**</span></span>](s-interval.md)                                                   |



## <a name="implementations"></a><span data-ttu-id="531fb-126">實作</span><span class="sxs-lookup"><span data-stu-id="531fb-126">Implementations</span></span>

-   [<span data-ttu-id="531fb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="531fb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="531fb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="531fb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="531fb-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="531fb-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="531fb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="531fb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="531fb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="531fb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="531fb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="531fb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="531fb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="531fb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="531fb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="531fb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="531fb-135">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-135">Entry</span></span> | <span data-ttu-id="531fb-136">值</span><span class="sxs-lookup"><span data-stu-id="531fb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="531fb-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="531fb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="531fb-139">System-Only</span></span>            | <span data-ttu-id="531fb-140">否</span><span class="sxs-lookup"><span data-stu-id="531fb-140">False</span></span>                             |
| <span data-ttu-id="531fb-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="531fb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="531fb-142">對</span><span class="sxs-lookup"><span data-stu-id="531fb-142">True</span></span>                              |
| <span data-ttu-id="531fb-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="531fb-143">Is Indexed</span></span>             | <span data-ttu-id="531fb-144">否</span><span class="sxs-lookup"><span data-stu-id="531fb-144">False</span></span>                             |
| <span data-ttu-id="531fb-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="531fb-145">In Global Catalog</span></span>      | <span data-ttu-id="531fb-146">否</span><span class="sxs-lookup"><span data-stu-id="531fb-146">False</span></span>                             |
| <span data-ttu-id="531fb-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="531fb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="531fb-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="531fb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="531fb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="531fb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="531fb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="531fb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="531fb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-151">Search-Flags</span></span>           | <span data-ttu-id="531fb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="531fb-152">0x00000000</span></span>                        |
| <span data-ttu-id="531fb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-153">System-Flags</span></span>           | <span data-ttu-id="531fb-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="531fb-154">0x00000010</span></span>                        |
| <span data-ttu-id="531fb-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="531fb-155">Classes used in</span></span>        | [<span data-ttu-id="531fb-156">**User**</span><span class="sxs-lookup"><span data-stu-id="531fb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="531fb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="531fb-157">Windows Server 2003</span></span>



| <span data-ttu-id="531fb-158">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-158">Entry</span></span> | <span data-ttu-id="531fb-159">值</span><span class="sxs-lookup"><span data-stu-id="531fb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="531fb-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="531fb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="531fb-162">System-Only</span></span>            | <span data-ttu-id="531fb-163">否</span><span class="sxs-lookup"><span data-stu-id="531fb-163">False</span></span>                             |
| <span data-ttu-id="531fb-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="531fb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="531fb-165">對</span><span class="sxs-lookup"><span data-stu-id="531fb-165">True</span></span>                              |
| <span data-ttu-id="531fb-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="531fb-166">Is Indexed</span></span>             | <span data-ttu-id="531fb-167">否</span><span class="sxs-lookup"><span data-stu-id="531fb-167">False</span></span>                             |
| <span data-ttu-id="531fb-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="531fb-168">In Global Catalog</span></span>      | <span data-ttu-id="531fb-169">否</span><span class="sxs-lookup"><span data-stu-id="531fb-169">False</span></span>                             |
| <span data-ttu-id="531fb-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="531fb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="531fb-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="531fb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="531fb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="531fb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="531fb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="531fb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="531fb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-174">Search-Flags</span></span>           | <span data-ttu-id="531fb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="531fb-175">0x00000000</span></span>                        |
| <span data-ttu-id="531fb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-176">System-Flags</span></span>           | <span data-ttu-id="531fb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="531fb-177">0x00000010</span></span>                        |
| <span data-ttu-id="531fb-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="531fb-178">Classes used in</span></span>        | [<span data-ttu-id="531fb-179">**User**</span><span class="sxs-lookup"><span data-stu-id="531fb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="531fb-180">亞當</span><span class="sxs-lookup"><span data-stu-id="531fb-180">ADAM</span></span>



| <span data-ttu-id="531fb-181">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-181">Entry</span></span> | <span data-ttu-id="531fb-182">值</span><span class="sxs-lookup"><span data-stu-id="531fb-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="531fb-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="531fb-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="531fb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="531fb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="531fb-185">System-Only</span></span>            | <span data-ttu-id="531fb-186">否</span><span class="sxs-lookup"><span data-stu-id="531fb-186">False</span></span>                                                             |
| <span data-ttu-id="531fb-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="531fb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="531fb-188">對</span><span class="sxs-lookup"><span data-stu-id="531fb-188">True</span></span>                                                              |
| <span data-ttu-id="531fb-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="531fb-189">Is Indexed</span></span>             | <span data-ttu-id="531fb-190">否</span><span class="sxs-lookup"><span data-stu-id="531fb-190">False</span></span>                                                             |
| <span data-ttu-id="531fb-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="531fb-191">In Global Catalog</span></span>      | <span data-ttu-id="531fb-192">否</span><span class="sxs-lookup"><span data-stu-id="531fb-192">False</span></span>                                                             |
| <span data-ttu-id="531fb-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="531fb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="531fb-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="531fb-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="531fb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="531fb-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="531fb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="531fb-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="531fb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-197">Search-Flags</span></span>           | <span data-ttu-id="531fb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="531fb-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="531fb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-199">System-Flags</span></span>           | <span data-ttu-id="531fb-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="531fb-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="531fb-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="531fb-201">Classes used in</span></span>        | [<span data-ttu-id="531fb-202">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="531fb-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="531fb-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="531fb-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="531fb-204">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-204">Entry</span></span> | <span data-ttu-id="531fb-205">值</span><span class="sxs-lookup"><span data-stu-id="531fb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="531fb-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="531fb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="531fb-208">System-Only</span></span>            | <span data-ttu-id="531fb-209">否</span><span class="sxs-lookup"><span data-stu-id="531fb-209">False</span></span>                             |
| <span data-ttu-id="531fb-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="531fb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="531fb-211">對</span><span class="sxs-lookup"><span data-stu-id="531fb-211">True</span></span>                              |
| <span data-ttu-id="531fb-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="531fb-212">Is Indexed</span></span>             | <span data-ttu-id="531fb-213">否</span><span class="sxs-lookup"><span data-stu-id="531fb-213">False</span></span>                             |
| <span data-ttu-id="531fb-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="531fb-214">In Global Catalog</span></span>      | <span data-ttu-id="531fb-215">否</span><span class="sxs-lookup"><span data-stu-id="531fb-215">False</span></span>                             |
| <span data-ttu-id="531fb-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="531fb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="531fb-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="531fb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="531fb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="531fb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="531fb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="531fb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="531fb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-220">Search-Flags</span></span>           | <span data-ttu-id="531fb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="531fb-221">0x00000000</span></span>                        |
| <span data-ttu-id="531fb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-222">System-Flags</span></span>           | <span data-ttu-id="531fb-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="531fb-223">0x00000010</span></span>                        |
| <span data-ttu-id="531fb-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="531fb-224">Classes used in</span></span>        | [<span data-ttu-id="531fb-225">**User**</span><span class="sxs-lookup"><span data-stu-id="531fb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="531fb-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="531fb-226">Windows Server 2008</span></span>



| <span data-ttu-id="531fb-227">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-227">Entry</span></span> | <span data-ttu-id="531fb-228">值</span><span class="sxs-lookup"><span data-stu-id="531fb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="531fb-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="531fb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="531fb-231">System-Only</span></span>            | <span data-ttu-id="531fb-232">否</span><span class="sxs-lookup"><span data-stu-id="531fb-232">False</span></span>                             |
| <span data-ttu-id="531fb-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="531fb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="531fb-234">對</span><span class="sxs-lookup"><span data-stu-id="531fb-234">True</span></span>                              |
| <span data-ttu-id="531fb-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="531fb-235">Is Indexed</span></span>             | <span data-ttu-id="531fb-236">否</span><span class="sxs-lookup"><span data-stu-id="531fb-236">False</span></span>                             |
| <span data-ttu-id="531fb-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="531fb-237">In Global Catalog</span></span>      | <span data-ttu-id="531fb-238">否</span><span class="sxs-lookup"><span data-stu-id="531fb-238">False</span></span>                             |
| <span data-ttu-id="531fb-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="531fb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="531fb-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="531fb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="531fb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="531fb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="531fb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="531fb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="531fb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-243">Search-Flags</span></span>           | <span data-ttu-id="531fb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="531fb-244">0x00000000</span></span>                        |
| <span data-ttu-id="531fb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-245">System-Flags</span></span>           | <span data-ttu-id="531fb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="531fb-246">0x00000010</span></span>                        |
| <span data-ttu-id="531fb-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="531fb-247">Classes used in</span></span>        | [<span data-ttu-id="531fb-248">**User**</span><span class="sxs-lookup"><span data-stu-id="531fb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="531fb-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="531fb-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="531fb-250">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-250">Entry</span></span> | <span data-ttu-id="531fb-251">值</span><span class="sxs-lookup"><span data-stu-id="531fb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="531fb-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="531fb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="531fb-254">System-Only</span></span>            | <span data-ttu-id="531fb-255">否</span><span class="sxs-lookup"><span data-stu-id="531fb-255">False</span></span>                             |
| <span data-ttu-id="531fb-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="531fb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="531fb-257">對</span><span class="sxs-lookup"><span data-stu-id="531fb-257">True</span></span>                              |
| <span data-ttu-id="531fb-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="531fb-258">Is Indexed</span></span>             | <span data-ttu-id="531fb-259">否</span><span class="sxs-lookup"><span data-stu-id="531fb-259">False</span></span>                             |
| <span data-ttu-id="531fb-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="531fb-260">In Global Catalog</span></span>      | <span data-ttu-id="531fb-261">否</span><span class="sxs-lookup"><span data-stu-id="531fb-261">False</span></span>                             |
| <span data-ttu-id="531fb-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="531fb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="531fb-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="531fb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="531fb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="531fb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="531fb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="531fb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="531fb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-266">Search-Flags</span></span>           | <span data-ttu-id="531fb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="531fb-267">0x00000000</span></span>                        |
| <span data-ttu-id="531fb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-268">System-Flags</span></span>           | <span data-ttu-id="531fb-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="531fb-269">0x00000010</span></span>                        |
| <span data-ttu-id="531fb-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="531fb-270">Classes used in</span></span>        | [<span data-ttu-id="531fb-271">**User**</span><span class="sxs-lookup"><span data-stu-id="531fb-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="531fb-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="531fb-272">Windows Server 2012</span></span>



| <span data-ttu-id="531fb-273">進入</span><span class="sxs-lookup"><span data-stu-id="531fb-273">Entry</span></span> | <span data-ttu-id="531fb-274">值</span><span class="sxs-lookup"><span data-stu-id="531fb-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="531fb-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="531fb-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="531fb-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="531fb-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="531fb-277">System-Only</span></span>            | <span data-ttu-id="531fb-278">否</span><span class="sxs-lookup"><span data-stu-id="531fb-278">False</span></span>                             |
| <span data-ttu-id="531fb-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="531fb-279">Is-Single-Valued</span></span>       | <span data-ttu-id="531fb-280">對</span><span class="sxs-lookup"><span data-stu-id="531fb-280">True</span></span>                              |
| <span data-ttu-id="531fb-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="531fb-281">Is Indexed</span></span>             | <span data-ttu-id="531fb-282">否</span><span class="sxs-lookup"><span data-stu-id="531fb-282">False</span></span>                             |
| <span data-ttu-id="531fb-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="531fb-283">In Global Catalog</span></span>      | <span data-ttu-id="531fb-284">否</span><span class="sxs-lookup"><span data-stu-id="531fb-284">False</span></span>                             |
| <span data-ttu-id="531fb-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="531fb-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="531fb-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="531fb-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="531fb-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="531fb-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="531fb-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="531fb-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="531fb-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-289">Search-Flags</span></span>           | <span data-ttu-id="531fb-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="531fb-290">0x00000000</span></span>                        |
| <span data-ttu-id="531fb-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="531fb-291">System-Flags</span></span>           | <span data-ttu-id="531fb-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="531fb-292">0x00000010</span></span>                        |
| <span data-ttu-id="531fb-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="531fb-293">Classes used in</span></span>        | [<span data-ttu-id="531fb-294">**User**</span><span class="sxs-lookup"><span data-stu-id="531fb-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="531fb-295">備註</span><span class="sxs-lookup"><span data-stu-id="531fb-295">Remarks</span></span>

<span data-ttu-id="531fb-296">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="531fb-296">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="531fb-297">只有在成功登入帳戶時，才會重設此屬性值。</span><span class="sxs-lookup"><span data-stu-id="531fb-297">This attribute value is only reset when the account is logged onto successfully.</span></span> <span data-ttu-id="531fb-298">這表示這個值可能不是零，但不會鎖定帳戶。若要精確地判斷帳戶是否已被鎖定，您必須將 [**鎖定期間**](a-lockoutduration.md) 新增到這段時間，並將結果與目前時間進行比較，以考慮本地時區和日光節約時間。</span><span class="sxs-lookup"><span data-stu-id="531fb-298">This means that this value may be non zero, yet the account is not locked out. To accurately determine if the account is locked out, you must add the [**Lockout-Duration**](a-lockoutduration.md) to this time and compare the result to the current time, accounting for local time zones and daylight savings time.</span></span>

## <a name="see-also"></a><span data-ttu-id="531fb-299">另請參閱</span><span class="sxs-lookup"><span data-stu-id="531fb-299">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531fb-300">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="531fb-300">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="531fb-301">**鎖定-持續時間**</span><span class="sxs-lookup"><span data-stu-id="531fb-301">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

