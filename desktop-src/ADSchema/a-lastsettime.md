---
title: Last 設定時間屬性
description: 上次變更密碼的時間。
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- 上次設定時間屬性 AD 架構
- lastSetTime 屬性 AD 架構
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce123377fac6e67de1ba84b906c9498d0a064936
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385414"
---
# <a name="last-set-time-attribute"></a><span data-ttu-id="37e84-105">Last 設定時間屬性</span><span class="sxs-lookup"><span data-stu-id="37e84-105">Last-Set-Time attribute</span></span>

<span data-ttu-id="37e84-106">上次變更密碼的時間。</span><span class="sxs-lookup"><span data-stu-id="37e84-106">The last time the secret was changed.</span></span> <span data-ttu-id="37e84-107">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="37e84-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>



| <span data-ttu-id="37e84-108">進入</span><span class="sxs-lookup"><span data-stu-id="37e84-108">Entry</span></span> | <span data-ttu-id="37e84-109">值</span><span class="sxs-lookup"><span data-stu-id="37e84-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="37e84-110">CN</span><span class="sxs-lookup"><span data-stu-id="37e84-110">CN</span></span>                | <span data-ttu-id="37e84-111">上次設定時間</span><span class="sxs-lookup"><span data-stu-id="37e84-111">Last-Set-Time</span></span>                        |
| <span data-ttu-id="37e84-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="37e84-112">Ldap-Display-Name</span></span> | <span data-ttu-id="37e84-113">lastSetTime</span><span class="sxs-lookup"><span data-stu-id="37e84-113">lastSetTime</span></span>                          |
| <span data-ttu-id="37e84-114">大小</span><span class="sxs-lookup"><span data-stu-id="37e84-114">Size</span></span>              | <span data-ttu-id="37e84-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="37e84-115">8 bytes</span></span>                              |
| <span data-ttu-id="37e84-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="37e84-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="37e84-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="37e84-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="37e84-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37e84-118">Attribute-Id</span></span>      | <span data-ttu-id="37e84-119">1.2.840.113556.1.4.53</span><span class="sxs-lookup"><span data-stu-id="37e84-119">1.2.840.113556.1.4.53</span></span>                |
| <span data-ttu-id="37e84-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="37e84-120">System-Id-Guid</span></span>    | <span data-ttu-id="37e84-121">bf967998-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="37e84-121">bf967998-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="37e84-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="37e84-122">Syntax</span></span>            | [<span data-ttu-id="37e84-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="37e84-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="37e84-124">實作</span><span class="sxs-lookup"><span data-stu-id="37e84-124">Implementations</span></span>

-   [<span data-ttu-id="37e84-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="37e84-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="37e84-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37e84-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37e84-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37e84-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37e84-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37e84-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37e84-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37e84-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37e84-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37e84-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="37e84-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37e84-131">Windows 2000 Server</span></span>



| <span data-ttu-id="37e84-132">進入</span><span class="sxs-lookup"><span data-stu-id="37e84-132">Entry</span></span> | <span data-ttu-id="37e84-133">值</span><span class="sxs-lookup"><span data-stu-id="37e84-133">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="37e84-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e84-134">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e84-135">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e84-136">System-Only</span></span>            | <span data-ttu-id="37e84-137">否</span><span class="sxs-lookup"><span data-stu-id="37e84-137">False</span></span>                                 |
| <span data-ttu-id="37e84-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e84-138">Is-Single-Valued</span></span>       | <span data-ttu-id="37e84-139">對</span><span class="sxs-lookup"><span data-stu-id="37e84-139">True</span></span>                                  |
| <span data-ttu-id="37e84-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e84-140">Is Indexed</span></span>             | <span data-ttu-id="37e84-141">否</span><span class="sxs-lookup"><span data-stu-id="37e84-141">False</span></span>                                 |
| <span data-ttu-id="37e84-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e84-142">In Global Catalog</span></span>      | <span data-ttu-id="37e84-143">否</span><span class="sxs-lookup"><span data-stu-id="37e84-143">False</span></span>                                 |
| <span data-ttu-id="37e84-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e84-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e84-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e84-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="37e84-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e84-146">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="37e84-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e84-147">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="37e84-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-148">Search-Flags</span></span>           | <span data-ttu-id="37e84-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e84-149">0x00000000</span></span>                            |
| <span data-ttu-id="37e84-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-150">System-Flags</span></span>           | <span data-ttu-id="37e84-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e84-151">0x00000010</span></span>                            |
| <span data-ttu-id="37e84-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e84-152">Classes used in</span></span>        | [<span data-ttu-id="37e84-153">**秘密**</span><span class="sxs-lookup"><span data-stu-id="37e84-153">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="37e84-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37e84-154">Windows Server 2003</span></span>



| <span data-ttu-id="37e84-155">進入</span><span class="sxs-lookup"><span data-stu-id="37e84-155">Entry</span></span> | <span data-ttu-id="37e84-156">值</span><span class="sxs-lookup"><span data-stu-id="37e84-156">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="37e84-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e84-157">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e84-158">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e84-159">System-Only</span></span>            | <span data-ttu-id="37e84-160">否</span><span class="sxs-lookup"><span data-stu-id="37e84-160">False</span></span>                                 |
| <span data-ttu-id="37e84-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e84-161">Is-Single-Valued</span></span>       | <span data-ttu-id="37e84-162">對</span><span class="sxs-lookup"><span data-stu-id="37e84-162">True</span></span>                                  |
| <span data-ttu-id="37e84-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e84-163">Is Indexed</span></span>             | <span data-ttu-id="37e84-164">否</span><span class="sxs-lookup"><span data-stu-id="37e84-164">False</span></span>                                 |
| <span data-ttu-id="37e84-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e84-165">In Global Catalog</span></span>      | <span data-ttu-id="37e84-166">否</span><span class="sxs-lookup"><span data-stu-id="37e84-166">False</span></span>                                 |
| <span data-ttu-id="37e84-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e84-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e84-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e84-168">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="37e84-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e84-169">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="37e84-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e84-170">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="37e84-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-171">Search-Flags</span></span>           | <span data-ttu-id="37e84-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e84-172">0x00000000</span></span>                            |
| <span data-ttu-id="37e84-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-173">System-Flags</span></span>           | <span data-ttu-id="37e84-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e84-174">0x00000010</span></span>                            |
| <span data-ttu-id="37e84-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e84-175">Classes used in</span></span>        | [<span data-ttu-id="37e84-176">**秘密**</span><span class="sxs-lookup"><span data-stu-id="37e84-176">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37e84-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37e84-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37e84-178">進入</span><span class="sxs-lookup"><span data-stu-id="37e84-178">Entry</span></span> | <span data-ttu-id="37e84-179">值</span><span class="sxs-lookup"><span data-stu-id="37e84-179">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="37e84-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e84-180">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e84-181">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e84-182">System-Only</span></span>            | <span data-ttu-id="37e84-183">否</span><span class="sxs-lookup"><span data-stu-id="37e84-183">False</span></span>                                 |
| <span data-ttu-id="37e84-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e84-184">Is-Single-Valued</span></span>       | <span data-ttu-id="37e84-185">對</span><span class="sxs-lookup"><span data-stu-id="37e84-185">True</span></span>                                  |
| <span data-ttu-id="37e84-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e84-186">Is Indexed</span></span>             | <span data-ttu-id="37e84-187">否</span><span class="sxs-lookup"><span data-stu-id="37e84-187">False</span></span>                                 |
| <span data-ttu-id="37e84-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e84-188">In Global Catalog</span></span>      | <span data-ttu-id="37e84-189">否</span><span class="sxs-lookup"><span data-stu-id="37e84-189">False</span></span>                                 |
| <span data-ttu-id="37e84-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e84-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e84-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e84-191">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="37e84-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e84-192">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="37e84-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e84-193">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="37e84-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-194">Search-Flags</span></span>           | <span data-ttu-id="37e84-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e84-195">0x00000000</span></span>                            |
| <span data-ttu-id="37e84-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-196">System-Flags</span></span>           | <span data-ttu-id="37e84-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e84-197">0x00000010</span></span>                            |
| <span data-ttu-id="37e84-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e84-198">Classes used in</span></span>        | [<span data-ttu-id="37e84-199">**秘密**</span><span class="sxs-lookup"><span data-stu-id="37e84-199">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37e84-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37e84-200">Windows Server 2008</span></span>



| <span data-ttu-id="37e84-201">進入</span><span class="sxs-lookup"><span data-stu-id="37e84-201">Entry</span></span> | <span data-ttu-id="37e84-202">值</span><span class="sxs-lookup"><span data-stu-id="37e84-202">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="37e84-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e84-203">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e84-204">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e84-205">System-Only</span></span>            | <span data-ttu-id="37e84-206">否</span><span class="sxs-lookup"><span data-stu-id="37e84-206">False</span></span>                                 |
| <span data-ttu-id="37e84-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e84-207">Is-Single-Valued</span></span>       | <span data-ttu-id="37e84-208">對</span><span class="sxs-lookup"><span data-stu-id="37e84-208">True</span></span>                                  |
| <span data-ttu-id="37e84-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e84-209">Is Indexed</span></span>             | <span data-ttu-id="37e84-210">否</span><span class="sxs-lookup"><span data-stu-id="37e84-210">False</span></span>                                 |
| <span data-ttu-id="37e84-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e84-211">In Global Catalog</span></span>      | <span data-ttu-id="37e84-212">否</span><span class="sxs-lookup"><span data-stu-id="37e84-212">False</span></span>                                 |
| <span data-ttu-id="37e84-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e84-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e84-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e84-214">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="37e84-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e84-215">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="37e84-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e84-216">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="37e84-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-217">Search-Flags</span></span>           | <span data-ttu-id="37e84-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e84-218">0x00000000</span></span>                            |
| <span data-ttu-id="37e84-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-219">System-Flags</span></span>           | <span data-ttu-id="37e84-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e84-220">0x00000010</span></span>                            |
| <span data-ttu-id="37e84-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e84-221">Classes used in</span></span>        | [<span data-ttu-id="37e84-222">**秘密**</span><span class="sxs-lookup"><span data-stu-id="37e84-222">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37e84-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37e84-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37e84-224">進入</span><span class="sxs-lookup"><span data-stu-id="37e84-224">Entry</span></span> | <span data-ttu-id="37e84-225">值</span><span class="sxs-lookup"><span data-stu-id="37e84-225">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="37e84-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e84-226">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e84-227">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e84-228">System-Only</span></span>            | <span data-ttu-id="37e84-229">否</span><span class="sxs-lookup"><span data-stu-id="37e84-229">False</span></span>                                 |
| <span data-ttu-id="37e84-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e84-230">Is-Single-Valued</span></span>       | <span data-ttu-id="37e84-231">對</span><span class="sxs-lookup"><span data-stu-id="37e84-231">True</span></span>                                  |
| <span data-ttu-id="37e84-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e84-232">Is Indexed</span></span>             | <span data-ttu-id="37e84-233">否</span><span class="sxs-lookup"><span data-stu-id="37e84-233">False</span></span>                                 |
| <span data-ttu-id="37e84-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e84-234">In Global Catalog</span></span>      | <span data-ttu-id="37e84-235">否</span><span class="sxs-lookup"><span data-stu-id="37e84-235">False</span></span>                                 |
| <span data-ttu-id="37e84-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e84-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e84-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e84-237">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="37e84-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e84-238">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="37e84-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e84-239">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="37e84-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-240">Search-Flags</span></span>           | <span data-ttu-id="37e84-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e84-241">0x00000000</span></span>                            |
| <span data-ttu-id="37e84-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-242">System-Flags</span></span>           | <span data-ttu-id="37e84-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e84-243">0x00000010</span></span>                            |
| <span data-ttu-id="37e84-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e84-244">Classes used in</span></span>        | [<span data-ttu-id="37e84-245">**秘密**</span><span class="sxs-lookup"><span data-stu-id="37e84-245">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37e84-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37e84-246">Windows Server 2012</span></span>



| <span data-ttu-id="37e84-247">進入</span><span class="sxs-lookup"><span data-stu-id="37e84-247">Entry</span></span> | <span data-ttu-id="37e84-248">值</span><span class="sxs-lookup"><span data-stu-id="37e84-248">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="37e84-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37e84-249">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e84-250">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="37e84-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e84-251">System-Only</span></span>            | <span data-ttu-id="37e84-252">否</span><span class="sxs-lookup"><span data-stu-id="37e84-252">False</span></span>                                 |
| <span data-ttu-id="37e84-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37e84-253">Is-Single-Valued</span></span>       | <span data-ttu-id="37e84-254">對</span><span class="sxs-lookup"><span data-stu-id="37e84-254">True</span></span>                                  |
| <span data-ttu-id="37e84-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37e84-255">Is Indexed</span></span>             | <span data-ttu-id="37e84-256">否</span><span class="sxs-lookup"><span data-stu-id="37e84-256">False</span></span>                                 |
| <span data-ttu-id="37e84-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37e84-257">In Global Catalog</span></span>      | <span data-ttu-id="37e84-258">否</span><span class="sxs-lookup"><span data-stu-id="37e84-258">False</span></span>                                 |
| <span data-ttu-id="37e84-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37e84-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e84-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37e84-260">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="37e84-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e84-261">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="37e84-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e84-262">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="37e84-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-263">Search-Flags</span></span>           | <span data-ttu-id="37e84-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37e84-264">0x00000000</span></span>                            |
| <span data-ttu-id="37e84-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e84-265">System-Flags</span></span>           | <span data-ttu-id="37e84-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e84-266">0x00000010</span></span>                            |
| <span data-ttu-id="37e84-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37e84-267">Classes used in</span></span>        | [<span data-ttu-id="37e84-268">**秘密**</span><span class="sxs-lookup"><span data-stu-id="37e84-268">**Secret**</span></span>](c-secret.md)<br/> |



 

 





