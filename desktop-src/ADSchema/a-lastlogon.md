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
# <a name="last-logon-attribute"></a><span data-ttu-id="7f947-105">Last-Logon 屬性</span><span class="sxs-lookup"><span data-stu-id="7f947-105">Last-Logon attribute</span></span>

<span data-ttu-id="7f947-106">使用者上次登入的時間。</span><span class="sxs-lookup"><span data-stu-id="7f947-106">The last time the user logged on.</span></span> <span data-ttu-id="7f947-107">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="7f947-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="7f947-108">值為零表示最後一個登入時間未知。</span><span class="sxs-lookup"><span data-stu-id="7f947-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="7f947-109">進入</span><span class="sxs-lookup"><span data-stu-id="7f947-109">Entry</span></span> | <span data-ttu-id="7f947-110">值</span><span class="sxs-lookup"><span data-stu-id="7f947-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7f947-111">CN</span><span class="sxs-lookup"><span data-stu-id="7f947-111">CN</span></span>                | <span data-ttu-id="7f947-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="7f947-112">Last-Logon</span></span>                           |
| <span data-ttu-id="7f947-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7f947-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7f947-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="7f947-114">lastLogon</span></span>                            |
| <span data-ttu-id="7f947-115">大小</span><span class="sxs-lookup"><span data-stu-id="7f947-115">Size</span></span>              | <span data-ttu-id="7f947-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="7f947-116">8 bytes</span></span>                              |
| <span data-ttu-id="7f947-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7f947-117">Update Privilege</span></span>  | <span data-ttu-id="7f947-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7f947-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="7f947-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7f947-119">Update Frequency</span></span>  | <span data-ttu-id="7f947-120">每次使用者登入時。</span><span class="sxs-lookup"><span data-stu-id="7f947-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="7f947-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7f947-121">Attribute-Id</span></span>      | <span data-ttu-id="7f947-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="7f947-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="7f947-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7f947-123">System-Id-Guid</span></span>    | <span data-ttu-id="7f947-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7f947-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7f947-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f947-125">Syntax</span></span>            | [<span data-ttu-id="7f947-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="7f947-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7f947-127">實作</span><span class="sxs-lookup"><span data-stu-id="7f947-127">Implementations</span></span>

-   [<span data-ttu-id="7f947-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7f947-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7f947-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f947-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7f947-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7f947-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7f947-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7f947-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7f947-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7f947-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7f947-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7f947-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7f947-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f947-134">Windows 2000 Server</span></span>



| <span data-ttu-id="7f947-135">進入</span><span class="sxs-lookup"><span data-stu-id="7f947-135">Entry</span></span> | <span data-ttu-id="7f947-136">值</span><span class="sxs-lookup"><span data-stu-id="7f947-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f947-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f947-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f947-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f947-139">System-Only</span></span>            | <span data-ttu-id="7f947-140">否</span><span class="sxs-lookup"><span data-stu-id="7f947-140">False</span></span>                             |
| <span data-ttu-id="7f947-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f947-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7f947-142">對</span><span class="sxs-lookup"><span data-stu-id="7f947-142">True</span></span>                              |
| <span data-ttu-id="7f947-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f947-143">Is Indexed</span></span>             | <span data-ttu-id="7f947-144">否</span><span class="sxs-lookup"><span data-stu-id="7f947-144">False</span></span>                             |
| <span data-ttu-id="7f947-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f947-145">In Global Catalog</span></span>      | <span data-ttu-id="7f947-146">否</span><span class="sxs-lookup"><span data-stu-id="7f947-146">False</span></span>                             |
| <span data-ttu-id="7f947-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f947-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f947-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f947-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f947-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f947-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f947-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f947-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f947-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-151">Search-Flags</span></span>           | <span data-ttu-id="7f947-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f947-152">0x00000000</span></span>                        |
| <span data-ttu-id="7f947-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-153">System-Flags</span></span>           | <span data-ttu-id="7f947-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7f947-154">0x00000011</span></span>                        |
| <span data-ttu-id="7f947-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f947-155">Classes used in</span></span>        | [<span data-ttu-id="7f947-156">**User**</span><span class="sxs-lookup"><span data-stu-id="7f947-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7f947-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f947-157">Windows Server 2003</span></span>



| <span data-ttu-id="7f947-158">進入</span><span class="sxs-lookup"><span data-stu-id="7f947-158">Entry</span></span> | <span data-ttu-id="7f947-159">值</span><span class="sxs-lookup"><span data-stu-id="7f947-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f947-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f947-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f947-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f947-162">System-Only</span></span>            | <span data-ttu-id="7f947-163">否</span><span class="sxs-lookup"><span data-stu-id="7f947-163">False</span></span>                             |
| <span data-ttu-id="7f947-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f947-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7f947-165">對</span><span class="sxs-lookup"><span data-stu-id="7f947-165">True</span></span>                              |
| <span data-ttu-id="7f947-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f947-166">Is Indexed</span></span>             | <span data-ttu-id="7f947-167">否</span><span class="sxs-lookup"><span data-stu-id="7f947-167">False</span></span>                             |
| <span data-ttu-id="7f947-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f947-168">In Global Catalog</span></span>      | <span data-ttu-id="7f947-169">否</span><span class="sxs-lookup"><span data-stu-id="7f947-169">False</span></span>                             |
| <span data-ttu-id="7f947-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f947-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f947-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f947-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f947-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f947-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f947-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f947-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f947-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-174">Search-Flags</span></span>           | <span data-ttu-id="7f947-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f947-175">0x00000000</span></span>                        |
| <span data-ttu-id="7f947-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-176">System-Flags</span></span>           | <span data-ttu-id="7f947-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7f947-177">0x00000011</span></span>                        |
| <span data-ttu-id="7f947-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f947-178">Classes used in</span></span>        | [<span data-ttu-id="7f947-179">**User**</span><span class="sxs-lookup"><span data-stu-id="7f947-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7f947-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7f947-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7f947-181">進入</span><span class="sxs-lookup"><span data-stu-id="7f947-181">Entry</span></span> | <span data-ttu-id="7f947-182">值</span><span class="sxs-lookup"><span data-stu-id="7f947-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f947-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f947-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f947-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f947-185">System-Only</span></span>            | <span data-ttu-id="7f947-186">否</span><span class="sxs-lookup"><span data-stu-id="7f947-186">False</span></span>                             |
| <span data-ttu-id="7f947-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f947-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7f947-188">對</span><span class="sxs-lookup"><span data-stu-id="7f947-188">True</span></span>                              |
| <span data-ttu-id="7f947-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f947-189">Is Indexed</span></span>             | <span data-ttu-id="7f947-190">否</span><span class="sxs-lookup"><span data-stu-id="7f947-190">False</span></span>                             |
| <span data-ttu-id="7f947-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f947-191">In Global Catalog</span></span>      | <span data-ttu-id="7f947-192">否</span><span class="sxs-lookup"><span data-stu-id="7f947-192">False</span></span>                             |
| <span data-ttu-id="7f947-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f947-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f947-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f947-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f947-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f947-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f947-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f947-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f947-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-197">Search-Flags</span></span>           | <span data-ttu-id="7f947-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f947-198">0x00000000</span></span>                        |
| <span data-ttu-id="7f947-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-199">System-Flags</span></span>           | <span data-ttu-id="7f947-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7f947-200">0x00000011</span></span>                        |
| <span data-ttu-id="7f947-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f947-201">Classes used in</span></span>        | [<span data-ttu-id="7f947-202">**User**</span><span class="sxs-lookup"><span data-stu-id="7f947-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7f947-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f947-203">Windows Server 2008</span></span>



| <span data-ttu-id="7f947-204">進入</span><span class="sxs-lookup"><span data-stu-id="7f947-204">Entry</span></span> | <span data-ttu-id="7f947-205">值</span><span class="sxs-lookup"><span data-stu-id="7f947-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f947-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f947-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f947-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f947-208">System-Only</span></span>            | <span data-ttu-id="7f947-209">否</span><span class="sxs-lookup"><span data-stu-id="7f947-209">False</span></span>                             |
| <span data-ttu-id="7f947-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f947-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7f947-211">對</span><span class="sxs-lookup"><span data-stu-id="7f947-211">True</span></span>                              |
| <span data-ttu-id="7f947-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f947-212">Is Indexed</span></span>             | <span data-ttu-id="7f947-213">否</span><span class="sxs-lookup"><span data-stu-id="7f947-213">False</span></span>                             |
| <span data-ttu-id="7f947-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f947-214">In Global Catalog</span></span>      | <span data-ttu-id="7f947-215">否</span><span class="sxs-lookup"><span data-stu-id="7f947-215">False</span></span>                             |
| <span data-ttu-id="7f947-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f947-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f947-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f947-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f947-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f947-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f947-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f947-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f947-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-220">Search-Flags</span></span>           | <span data-ttu-id="7f947-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f947-221">0x00000000</span></span>                        |
| <span data-ttu-id="7f947-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-222">System-Flags</span></span>           | <span data-ttu-id="7f947-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7f947-223">0x00000011</span></span>                        |
| <span data-ttu-id="7f947-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f947-224">Classes used in</span></span>        | [<span data-ttu-id="7f947-225">**User**</span><span class="sxs-lookup"><span data-stu-id="7f947-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7f947-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f947-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7f947-227">進入</span><span class="sxs-lookup"><span data-stu-id="7f947-227">Entry</span></span> | <span data-ttu-id="7f947-228">值</span><span class="sxs-lookup"><span data-stu-id="7f947-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f947-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f947-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f947-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f947-231">System-Only</span></span>            | <span data-ttu-id="7f947-232">否</span><span class="sxs-lookup"><span data-stu-id="7f947-232">False</span></span>                             |
| <span data-ttu-id="7f947-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f947-233">Is-Single-Valued</span></span>       | <span data-ttu-id="7f947-234">對</span><span class="sxs-lookup"><span data-stu-id="7f947-234">True</span></span>                              |
| <span data-ttu-id="7f947-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f947-235">Is Indexed</span></span>             | <span data-ttu-id="7f947-236">否</span><span class="sxs-lookup"><span data-stu-id="7f947-236">False</span></span>                             |
| <span data-ttu-id="7f947-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f947-237">In Global Catalog</span></span>      | <span data-ttu-id="7f947-238">否</span><span class="sxs-lookup"><span data-stu-id="7f947-238">False</span></span>                             |
| <span data-ttu-id="7f947-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f947-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f947-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f947-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f947-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f947-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f947-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f947-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f947-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-243">Search-Flags</span></span>           | <span data-ttu-id="7f947-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f947-244">0x00000000</span></span>                        |
| <span data-ttu-id="7f947-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-245">System-Flags</span></span>           | <span data-ttu-id="7f947-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7f947-246">0x00000011</span></span>                        |
| <span data-ttu-id="7f947-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f947-247">Classes used in</span></span>        | [<span data-ttu-id="7f947-248">**User**</span><span class="sxs-lookup"><span data-stu-id="7f947-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7f947-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f947-249">Windows Server 2012</span></span>



| <span data-ttu-id="7f947-250">進入</span><span class="sxs-lookup"><span data-stu-id="7f947-250">Entry</span></span> | <span data-ttu-id="7f947-251">值</span><span class="sxs-lookup"><span data-stu-id="7f947-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7f947-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7f947-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7f947-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7f947-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="7f947-254">System-Only</span></span>            | <span data-ttu-id="7f947-255">否</span><span class="sxs-lookup"><span data-stu-id="7f947-255">False</span></span>                             |
| <span data-ttu-id="7f947-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7f947-256">Is-Single-Valued</span></span>       | <span data-ttu-id="7f947-257">對</span><span class="sxs-lookup"><span data-stu-id="7f947-257">True</span></span>                              |
| <span data-ttu-id="7f947-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7f947-258">Is Indexed</span></span>             | <span data-ttu-id="7f947-259">否</span><span class="sxs-lookup"><span data-stu-id="7f947-259">False</span></span>                             |
| <span data-ttu-id="7f947-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7f947-260">In Global Catalog</span></span>      | <span data-ttu-id="7f947-261">否</span><span class="sxs-lookup"><span data-stu-id="7f947-261">False</span></span>                             |
| <span data-ttu-id="7f947-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7f947-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="7f947-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7f947-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7f947-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7f947-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7f947-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7f947-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7f947-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-266">Search-Flags</span></span>           | <span data-ttu-id="7f947-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7f947-267">0x00000000</span></span>                        |
| <span data-ttu-id="7f947-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7f947-268">System-Flags</span></span>           | <span data-ttu-id="7f947-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7f947-269">0x00000011</span></span>                        |
| <span data-ttu-id="7f947-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7f947-270">Classes used in</span></span>        | [<span data-ttu-id="7f947-271">**User**</span><span class="sxs-lookup"><span data-stu-id="7f947-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7f947-272">備註</span><span class="sxs-lookup"><span data-stu-id="7f947-272">Remarks</span></span>

<span data-ttu-id="7f947-273">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="7f947-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="7f947-274">這個屬性不會複寫，並且會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="7f947-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="7f947-275">若要取得使用者在網域中最後一次登入的精確值，必須從網域中的每個網域控制站取出使用者的 **最後一個登** 入屬性。</span><span class="sxs-lookup"><span data-stu-id="7f947-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="7f947-276">所抓取的最大值是該使用者的最後登入時間。</span><span class="sxs-lookup"><span data-stu-id="7f947-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f947-277">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f947-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f947-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="7f947-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

