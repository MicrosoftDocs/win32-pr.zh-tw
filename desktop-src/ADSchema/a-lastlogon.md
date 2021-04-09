---
title: Last-Logon 屬性
description: 使用者上次登入的時間。
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Last-Logon 屬性 AD 架構
- lastLogon 屬性 AD 架構
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845235"
---
# <a name="last-logon-attribute"></a><span data-ttu-id="21845-105">Last-Logon 屬性</span><span class="sxs-lookup"><span data-stu-id="21845-105">Last-Logon attribute</span></span>

<span data-ttu-id="21845-106">使用者上次登入的時間。</span><span class="sxs-lookup"><span data-stu-id="21845-106">The last time the user logged on.</span></span> <span data-ttu-id="21845-107">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="21845-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="21845-108">值為零表示最後一個登入時間未知。</span><span class="sxs-lookup"><span data-stu-id="21845-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="21845-109">進入</span><span class="sxs-lookup"><span data-stu-id="21845-109">Entry</span></span> | <span data-ttu-id="21845-110">值</span><span class="sxs-lookup"><span data-stu-id="21845-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="21845-111">CN</span><span class="sxs-lookup"><span data-stu-id="21845-111">CN</span></span>                | <span data-ttu-id="21845-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="21845-112">Last-Logon</span></span>                           |
| <span data-ttu-id="21845-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="21845-113">Ldap-Display-Name</span></span> | <span data-ttu-id="21845-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="21845-114">lastLogon</span></span>                            |
| <span data-ttu-id="21845-115">大小</span><span class="sxs-lookup"><span data-stu-id="21845-115">Size</span></span>              | <span data-ttu-id="21845-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="21845-116">8 bytes</span></span>                              |
| <span data-ttu-id="21845-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="21845-117">Update Privilege</span></span>  | <span data-ttu-id="21845-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="21845-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="21845-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="21845-119">Update Frequency</span></span>  | <span data-ttu-id="21845-120">每次使用者登入時。</span><span class="sxs-lookup"><span data-stu-id="21845-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="21845-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21845-121">Attribute-Id</span></span>      | <span data-ttu-id="21845-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="21845-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="21845-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="21845-123">System-Id-Guid</span></span>    | <span data-ttu-id="21845-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="21845-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="21845-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="21845-125">Syntax</span></span>            | [<span data-ttu-id="21845-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="21845-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="21845-127">實作</span><span class="sxs-lookup"><span data-stu-id="21845-127">Implementations</span></span>

-   [<span data-ttu-id="21845-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21845-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21845-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21845-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21845-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21845-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21845-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21845-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21845-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21845-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21845-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21845-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21845-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21845-134">Windows 2000 Server</span></span>



| <span data-ttu-id="21845-135">進入</span><span class="sxs-lookup"><span data-stu-id="21845-135">Entry</span></span> | <span data-ttu-id="21845-136">值</span><span class="sxs-lookup"><span data-stu-id="21845-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="21845-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21845-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21845-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="21845-139">System-Only</span></span>            | <span data-ttu-id="21845-140">否</span><span class="sxs-lookup"><span data-stu-id="21845-140">False</span></span>                             |
| <span data-ttu-id="21845-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21845-141">Is-Single-Valued</span></span>       | <span data-ttu-id="21845-142">對</span><span class="sxs-lookup"><span data-stu-id="21845-142">True</span></span>                              |
| <span data-ttu-id="21845-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21845-143">Is Indexed</span></span>             | <span data-ttu-id="21845-144">否</span><span class="sxs-lookup"><span data-stu-id="21845-144">False</span></span>                             |
| <span data-ttu-id="21845-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21845-145">In Global Catalog</span></span>      | <span data-ttu-id="21845-146">否</span><span class="sxs-lookup"><span data-stu-id="21845-146">False</span></span>                             |
| <span data-ttu-id="21845-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21845-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="21845-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21845-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="21845-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21845-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="21845-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21845-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="21845-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-151">Search-Flags</span></span>           | <span data-ttu-id="21845-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21845-152">0x00000000</span></span>                        |
| <span data-ttu-id="21845-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-153">System-Flags</span></span>           | <span data-ttu-id="21845-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="21845-154">0x00000011</span></span>                        |
| <span data-ttu-id="21845-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21845-155">Classes used in</span></span>        | [<span data-ttu-id="21845-156">**User**</span><span class="sxs-lookup"><span data-stu-id="21845-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21845-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21845-157">Windows Server 2003</span></span>



| <span data-ttu-id="21845-158">進入</span><span class="sxs-lookup"><span data-stu-id="21845-158">Entry</span></span> | <span data-ttu-id="21845-159">值</span><span class="sxs-lookup"><span data-stu-id="21845-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="21845-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21845-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21845-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="21845-162">System-Only</span></span>            | <span data-ttu-id="21845-163">否</span><span class="sxs-lookup"><span data-stu-id="21845-163">False</span></span>                             |
| <span data-ttu-id="21845-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21845-164">Is-Single-Valued</span></span>       | <span data-ttu-id="21845-165">對</span><span class="sxs-lookup"><span data-stu-id="21845-165">True</span></span>                              |
| <span data-ttu-id="21845-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21845-166">Is Indexed</span></span>             | <span data-ttu-id="21845-167">否</span><span class="sxs-lookup"><span data-stu-id="21845-167">False</span></span>                             |
| <span data-ttu-id="21845-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21845-168">In Global Catalog</span></span>      | <span data-ttu-id="21845-169">否</span><span class="sxs-lookup"><span data-stu-id="21845-169">False</span></span>                             |
| <span data-ttu-id="21845-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21845-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="21845-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21845-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="21845-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21845-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="21845-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21845-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="21845-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-174">Search-Flags</span></span>           | <span data-ttu-id="21845-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21845-175">0x00000000</span></span>                        |
| <span data-ttu-id="21845-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-176">System-Flags</span></span>           | <span data-ttu-id="21845-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="21845-177">0x00000011</span></span>                        |
| <span data-ttu-id="21845-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21845-178">Classes used in</span></span>        | [<span data-ttu-id="21845-179">**User**</span><span class="sxs-lookup"><span data-stu-id="21845-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21845-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21845-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21845-181">進入</span><span class="sxs-lookup"><span data-stu-id="21845-181">Entry</span></span> | <span data-ttu-id="21845-182">值</span><span class="sxs-lookup"><span data-stu-id="21845-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="21845-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21845-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21845-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="21845-185">System-Only</span></span>            | <span data-ttu-id="21845-186">否</span><span class="sxs-lookup"><span data-stu-id="21845-186">False</span></span>                             |
| <span data-ttu-id="21845-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21845-187">Is-Single-Valued</span></span>       | <span data-ttu-id="21845-188">對</span><span class="sxs-lookup"><span data-stu-id="21845-188">True</span></span>                              |
| <span data-ttu-id="21845-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21845-189">Is Indexed</span></span>             | <span data-ttu-id="21845-190">否</span><span class="sxs-lookup"><span data-stu-id="21845-190">False</span></span>                             |
| <span data-ttu-id="21845-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21845-191">In Global Catalog</span></span>      | <span data-ttu-id="21845-192">否</span><span class="sxs-lookup"><span data-stu-id="21845-192">False</span></span>                             |
| <span data-ttu-id="21845-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21845-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="21845-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21845-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="21845-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21845-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="21845-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21845-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="21845-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-197">Search-Flags</span></span>           | <span data-ttu-id="21845-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21845-198">0x00000000</span></span>                        |
| <span data-ttu-id="21845-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-199">System-Flags</span></span>           | <span data-ttu-id="21845-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="21845-200">0x00000011</span></span>                        |
| <span data-ttu-id="21845-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21845-201">Classes used in</span></span>        | [<span data-ttu-id="21845-202">**User**</span><span class="sxs-lookup"><span data-stu-id="21845-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21845-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21845-203">Windows Server 2008</span></span>



| <span data-ttu-id="21845-204">進入</span><span class="sxs-lookup"><span data-stu-id="21845-204">Entry</span></span> | <span data-ttu-id="21845-205">值</span><span class="sxs-lookup"><span data-stu-id="21845-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="21845-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21845-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21845-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="21845-208">System-Only</span></span>            | <span data-ttu-id="21845-209">否</span><span class="sxs-lookup"><span data-stu-id="21845-209">False</span></span>                             |
| <span data-ttu-id="21845-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21845-210">Is-Single-Valued</span></span>       | <span data-ttu-id="21845-211">對</span><span class="sxs-lookup"><span data-stu-id="21845-211">True</span></span>                              |
| <span data-ttu-id="21845-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21845-212">Is Indexed</span></span>             | <span data-ttu-id="21845-213">否</span><span class="sxs-lookup"><span data-stu-id="21845-213">False</span></span>                             |
| <span data-ttu-id="21845-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21845-214">In Global Catalog</span></span>      | <span data-ttu-id="21845-215">否</span><span class="sxs-lookup"><span data-stu-id="21845-215">False</span></span>                             |
| <span data-ttu-id="21845-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21845-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="21845-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21845-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="21845-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21845-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="21845-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21845-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="21845-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-220">Search-Flags</span></span>           | <span data-ttu-id="21845-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21845-221">0x00000000</span></span>                        |
| <span data-ttu-id="21845-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-222">System-Flags</span></span>           | <span data-ttu-id="21845-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="21845-223">0x00000011</span></span>                        |
| <span data-ttu-id="21845-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21845-224">Classes used in</span></span>        | [<span data-ttu-id="21845-225">**User**</span><span class="sxs-lookup"><span data-stu-id="21845-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21845-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21845-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21845-227">進入</span><span class="sxs-lookup"><span data-stu-id="21845-227">Entry</span></span> | <span data-ttu-id="21845-228">值</span><span class="sxs-lookup"><span data-stu-id="21845-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="21845-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21845-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21845-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="21845-231">System-Only</span></span>            | <span data-ttu-id="21845-232">否</span><span class="sxs-lookup"><span data-stu-id="21845-232">False</span></span>                             |
| <span data-ttu-id="21845-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21845-233">Is-Single-Valued</span></span>       | <span data-ttu-id="21845-234">對</span><span class="sxs-lookup"><span data-stu-id="21845-234">True</span></span>                              |
| <span data-ttu-id="21845-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21845-235">Is Indexed</span></span>             | <span data-ttu-id="21845-236">否</span><span class="sxs-lookup"><span data-stu-id="21845-236">False</span></span>                             |
| <span data-ttu-id="21845-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21845-237">In Global Catalog</span></span>      | <span data-ttu-id="21845-238">否</span><span class="sxs-lookup"><span data-stu-id="21845-238">False</span></span>                             |
| <span data-ttu-id="21845-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21845-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="21845-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21845-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="21845-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21845-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="21845-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21845-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="21845-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-243">Search-Flags</span></span>           | <span data-ttu-id="21845-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21845-244">0x00000000</span></span>                        |
| <span data-ttu-id="21845-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-245">System-Flags</span></span>           | <span data-ttu-id="21845-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="21845-246">0x00000011</span></span>                        |
| <span data-ttu-id="21845-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21845-247">Classes used in</span></span>        | [<span data-ttu-id="21845-248">**User**</span><span class="sxs-lookup"><span data-stu-id="21845-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21845-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21845-249">Windows Server 2012</span></span>



| <span data-ttu-id="21845-250">進入</span><span class="sxs-lookup"><span data-stu-id="21845-250">Entry</span></span> | <span data-ttu-id="21845-251">值</span><span class="sxs-lookup"><span data-stu-id="21845-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="21845-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21845-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21845-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="21845-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="21845-254">System-Only</span></span>            | <span data-ttu-id="21845-255">否</span><span class="sxs-lookup"><span data-stu-id="21845-255">False</span></span>                             |
| <span data-ttu-id="21845-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21845-256">Is-Single-Valued</span></span>       | <span data-ttu-id="21845-257">對</span><span class="sxs-lookup"><span data-stu-id="21845-257">True</span></span>                              |
| <span data-ttu-id="21845-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21845-258">Is Indexed</span></span>             | <span data-ttu-id="21845-259">否</span><span class="sxs-lookup"><span data-stu-id="21845-259">False</span></span>                             |
| <span data-ttu-id="21845-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21845-260">In Global Catalog</span></span>      | <span data-ttu-id="21845-261">否</span><span class="sxs-lookup"><span data-stu-id="21845-261">False</span></span>                             |
| <span data-ttu-id="21845-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21845-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="21845-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21845-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="21845-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21845-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="21845-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21845-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="21845-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-266">Search-Flags</span></span>           | <span data-ttu-id="21845-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21845-267">0x00000000</span></span>                        |
| <span data-ttu-id="21845-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21845-268">System-Flags</span></span>           | <span data-ttu-id="21845-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="21845-269">0x00000011</span></span>                        |
| <span data-ttu-id="21845-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21845-270">Classes used in</span></span>        | [<span data-ttu-id="21845-271">**User**</span><span class="sxs-lookup"><span data-stu-id="21845-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="21845-272">備註</span><span class="sxs-lookup"><span data-stu-id="21845-272">Remarks</span></span>

<span data-ttu-id="21845-273">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="21845-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="21845-274">這個屬性不會複寫，並且會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="21845-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="21845-275">若要取得使用者在網域中最後一次登入的精確值，必須從網域中的每個網域控制站取出使用者的 **最後一個登** 入屬性。</span><span class="sxs-lookup"><span data-stu-id="21845-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="21845-276">所抓取的最大值是該使用者的最後登入時間。</span><span class="sxs-lookup"><span data-stu-id="21845-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="21845-277">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21845-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21845-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="21845-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

