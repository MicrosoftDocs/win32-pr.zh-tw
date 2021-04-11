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
# <a name="last-logon-attribute"></a><span data-ttu-id="7ffeb-105">Last-Logon 屬性</span><span class="sxs-lookup"><span data-stu-id="7ffeb-105">Last-Logon attribute</span></span>

<span data-ttu-id="7ffeb-106">使用者上次登入的時間。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-106">The last time the user logged on.</span></span> <span data-ttu-id="7ffeb-107">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="7ffeb-108">值為零表示最後一個登入時間未知。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="7ffeb-109">進入</span><span class="sxs-lookup"><span data-stu-id="7ffeb-109">Entry</span></span> | <span data-ttu-id="7ffeb-110">值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7ffeb-111">CN</span><span class="sxs-lookup"><span data-stu-id="7ffeb-111">CN</span></span>                | <span data-ttu-id="7ffeb-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="7ffeb-112">Last-Logon</span></span>                           |
| <span data-ttu-id="7ffeb-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7ffeb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7ffeb-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="7ffeb-114">lastLogon</span></span>                            |
| <span data-ttu-id="7ffeb-115">大小</span><span class="sxs-lookup"><span data-stu-id="7ffeb-115">Size</span></span>              | <span data-ttu-id="7ffeb-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="7ffeb-116">8 bytes</span></span>                              |
| <span data-ttu-id="7ffeb-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7ffeb-117">Update Privilege</span></span>  | <span data-ttu-id="7ffeb-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="7ffeb-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7ffeb-119">Update Frequency</span></span>  | <span data-ttu-id="7ffeb-120">每次使用者登入時。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="7ffeb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ffeb-121">Attribute-Id</span></span>      | <span data-ttu-id="7ffeb-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="7ffeb-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="7ffeb-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7ffeb-123">System-Id-Guid</span></span>    | <span data-ttu-id="7ffeb-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7ffeb-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7ffeb-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ffeb-125">Syntax</span></span>            | [<span data-ttu-id="7ffeb-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7ffeb-127">實作</span><span class="sxs-lookup"><span data-stu-id="7ffeb-127">Implementations</span></span>

-   [<span data-ttu-id="7ffeb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7ffeb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ffeb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ffeb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ffeb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ffeb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7ffeb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ffeb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="7ffeb-135">進入</span><span class="sxs-lookup"><span data-stu-id="7ffeb-135">Entry</span></span> | <span data-ttu-id="7ffeb-136">值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ffeb-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ffeb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ffeb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ffeb-139">System-Only</span></span>            | <span data-ttu-id="7ffeb-140">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-140">False</span></span>                             |
| <span data-ttu-id="7ffeb-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7ffeb-142">對</span><span class="sxs-lookup"><span data-stu-id="7ffeb-142">True</span></span>                              |
| <span data-ttu-id="7ffeb-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ffeb-143">Is Indexed</span></span>             | <span data-ttu-id="7ffeb-144">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-144">False</span></span>                             |
| <span data-ttu-id="7ffeb-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ffeb-145">In Global Catalog</span></span>      | <span data-ttu-id="7ffeb-146">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-146">False</span></span>                             |
| <span data-ttu-id="7ffeb-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ffeb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ffeb-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ffeb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ffeb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ffeb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ffeb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-151">Search-Flags</span></span>           | <span data-ttu-id="7ffeb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ffeb-152">0x00000000</span></span>                        |
| <span data-ttu-id="7ffeb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-153">System-Flags</span></span>           | <span data-ttu-id="7ffeb-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7ffeb-154">0x00000011</span></span>                        |
| <span data-ttu-id="7ffeb-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ffeb-155">Classes used in</span></span>        | [<span data-ttu-id="7ffeb-156">**User**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7ffeb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ffeb-157">Windows Server 2003</span></span>



| <span data-ttu-id="7ffeb-158">進入</span><span class="sxs-lookup"><span data-stu-id="7ffeb-158">Entry</span></span> | <span data-ttu-id="7ffeb-159">值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ffeb-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ffeb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ffeb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ffeb-162">System-Only</span></span>            | <span data-ttu-id="7ffeb-163">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-163">False</span></span>                             |
| <span data-ttu-id="7ffeb-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7ffeb-165">對</span><span class="sxs-lookup"><span data-stu-id="7ffeb-165">True</span></span>                              |
| <span data-ttu-id="7ffeb-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ffeb-166">Is Indexed</span></span>             | <span data-ttu-id="7ffeb-167">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-167">False</span></span>                             |
| <span data-ttu-id="7ffeb-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ffeb-168">In Global Catalog</span></span>      | <span data-ttu-id="7ffeb-169">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-169">False</span></span>                             |
| <span data-ttu-id="7ffeb-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ffeb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ffeb-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ffeb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ffeb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ffeb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ffeb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-174">Search-Flags</span></span>           | <span data-ttu-id="7ffeb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ffeb-175">0x00000000</span></span>                        |
| <span data-ttu-id="7ffeb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-176">System-Flags</span></span>           | <span data-ttu-id="7ffeb-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7ffeb-177">0x00000011</span></span>                        |
| <span data-ttu-id="7ffeb-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ffeb-178">Classes used in</span></span>        | [<span data-ttu-id="7ffeb-179">**User**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ffeb-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ffeb-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ffeb-181">進入</span><span class="sxs-lookup"><span data-stu-id="7ffeb-181">Entry</span></span> | <span data-ttu-id="7ffeb-182">值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ffeb-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ffeb-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ffeb-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ffeb-185">System-Only</span></span>            | <span data-ttu-id="7ffeb-186">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-186">False</span></span>                             |
| <span data-ttu-id="7ffeb-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7ffeb-188">對</span><span class="sxs-lookup"><span data-stu-id="7ffeb-188">True</span></span>                              |
| <span data-ttu-id="7ffeb-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ffeb-189">Is Indexed</span></span>             | <span data-ttu-id="7ffeb-190">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-190">False</span></span>                             |
| <span data-ttu-id="7ffeb-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ffeb-191">In Global Catalog</span></span>      | <span data-ttu-id="7ffeb-192">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-192">False</span></span>                             |
| <span data-ttu-id="7ffeb-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ffeb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ffeb-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ffeb-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ffeb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ffeb-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ffeb-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-197">Search-Flags</span></span>           | <span data-ttu-id="7ffeb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ffeb-198">0x00000000</span></span>                        |
| <span data-ttu-id="7ffeb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-199">System-Flags</span></span>           | <span data-ttu-id="7ffeb-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7ffeb-200">0x00000011</span></span>                        |
| <span data-ttu-id="7ffeb-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ffeb-201">Classes used in</span></span>        | [<span data-ttu-id="7ffeb-202">**User**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ffeb-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ffeb-203">Windows Server 2008</span></span>



| <span data-ttu-id="7ffeb-204">進入</span><span class="sxs-lookup"><span data-stu-id="7ffeb-204">Entry</span></span> | <span data-ttu-id="7ffeb-205">值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ffeb-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ffeb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ffeb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ffeb-208">System-Only</span></span>            | <span data-ttu-id="7ffeb-209">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-209">False</span></span>                             |
| <span data-ttu-id="7ffeb-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7ffeb-211">對</span><span class="sxs-lookup"><span data-stu-id="7ffeb-211">True</span></span>                              |
| <span data-ttu-id="7ffeb-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ffeb-212">Is Indexed</span></span>             | <span data-ttu-id="7ffeb-213">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-213">False</span></span>                             |
| <span data-ttu-id="7ffeb-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ffeb-214">In Global Catalog</span></span>      | <span data-ttu-id="7ffeb-215">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-215">False</span></span>                             |
| <span data-ttu-id="7ffeb-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ffeb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ffeb-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ffeb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ffeb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ffeb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ffeb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-220">Search-Flags</span></span>           | <span data-ttu-id="7ffeb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ffeb-221">0x00000000</span></span>                        |
| <span data-ttu-id="7ffeb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-222">System-Flags</span></span>           | <span data-ttu-id="7ffeb-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7ffeb-223">0x00000011</span></span>                        |
| <span data-ttu-id="7ffeb-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ffeb-224">Classes used in</span></span>        | [<span data-ttu-id="7ffeb-225">**User**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ffeb-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ffeb-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ffeb-227">進入</span><span class="sxs-lookup"><span data-stu-id="7ffeb-227">Entry</span></span> | <span data-ttu-id="7ffeb-228">值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ffeb-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ffeb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ffeb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ffeb-231">System-Only</span></span>            | <span data-ttu-id="7ffeb-232">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-232">False</span></span>                             |
| <span data-ttu-id="7ffeb-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="7ffeb-234">對</span><span class="sxs-lookup"><span data-stu-id="7ffeb-234">True</span></span>                              |
| <span data-ttu-id="7ffeb-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ffeb-235">Is Indexed</span></span>             | <span data-ttu-id="7ffeb-236">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-236">False</span></span>                             |
| <span data-ttu-id="7ffeb-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ffeb-237">In Global Catalog</span></span>      | <span data-ttu-id="7ffeb-238">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-238">False</span></span>                             |
| <span data-ttu-id="7ffeb-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ffeb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ffeb-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ffeb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ffeb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ffeb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ffeb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-243">Search-Flags</span></span>           | <span data-ttu-id="7ffeb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ffeb-244">0x00000000</span></span>                        |
| <span data-ttu-id="7ffeb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-245">System-Flags</span></span>           | <span data-ttu-id="7ffeb-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7ffeb-246">0x00000011</span></span>                        |
| <span data-ttu-id="7ffeb-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ffeb-247">Classes used in</span></span>        | [<span data-ttu-id="7ffeb-248">**User**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ffeb-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ffeb-249">Windows Server 2012</span></span>



| <span data-ttu-id="7ffeb-250">進入</span><span class="sxs-lookup"><span data-stu-id="7ffeb-250">Entry</span></span> | <span data-ttu-id="7ffeb-251">值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7ffeb-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7ffeb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ffeb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7ffeb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ffeb-254">System-Only</span></span>            | <span data-ttu-id="7ffeb-255">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-255">False</span></span>                             |
| <span data-ttu-id="7ffeb-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7ffeb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="7ffeb-257">對</span><span class="sxs-lookup"><span data-stu-id="7ffeb-257">True</span></span>                              |
| <span data-ttu-id="7ffeb-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7ffeb-258">Is Indexed</span></span>             | <span data-ttu-id="7ffeb-259">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-259">False</span></span>                             |
| <span data-ttu-id="7ffeb-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7ffeb-260">In Global Catalog</span></span>      | <span data-ttu-id="7ffeb-261">否</span><span class="sxs-lookup"><span data-stu-id="7ffeb-261">False</span></span>                             |
| <span data-ttu-id="7ffeb-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7ffeb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ffeb-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7ffeb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7ffeb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ffeb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ffeb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7ffeb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-266">Search-Flags</span></span>           | <span data-ttu-id="7ffeb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ffeb-267">0x00000000</span></span>                        |
| <span data-ttu-id="7ffeb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ffeb-268">System-Flags</span></span>           | <span data-ttu-id="7ffeb-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="7ffeb-269">0x00000011</span></span>                        |
| <span data-ttu-id="7ffeb-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7ffeb-270">Classes used in</span></span>        | [<span data-ttu-id="7ffeb-271">**User**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7ffeb-272">備註</span><span class="sxs-lookup"><span data-stu-id="7ffeb-272">Remarks</span></span>

<span data-ttu-id="7ffeb-273">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="7ffeb-274">這個屬性不會複寫，並且會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="7ffeb-275">若要取得使用者在網域中最後一次登入的精確值，必須從網域中的每個網域控制站取出使用者的 **最後一個登** 入屬性。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="7ffeb-276">所抓取的最大值是該使用者的最後登入時間。</span><span class="sxs-lookup"><span data-stu-id="7ffeb-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ffeb-277">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ffeb-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffeb-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="7ffeb-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

