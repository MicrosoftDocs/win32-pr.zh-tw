---
title: 錯誤的密碼時間屬性
description: 上次嘗試登入此帳戶的時間和日期，以及不正確密碼。
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- 錯誤的密碼時間屬性 AD 架構
- badPasswordTime 屬性 AD 架構
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47df09d0ff2d82a9180c43721aa09e5363884e24
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467378"
---
# <a name="bad-password-time-attribute"></a><span data-ttu-id="950f6-105">錯誤的密碼時間屬性</span><span class="sxs-lookup"><span data-stu-id="950f6-105">Bad-Password-Time attribute</span></span>

<span data-ttu-id="950f6-106">上次嘗試登入此帳戶的時間和日期，以及不正確密碼。</span><span class="sxs-lookup"><span data-stu-id="950f6-106">The last time and date that an attempt to log on to this account was made with a password that is not valid.</span></span> <span data-ttu-id="950f6-107">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="950f6-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="950f6-108">值為零表示最後一次使用不正確的密碼是未知的。</span><span class="sxs-lookup"><span data-stu-id="950f6-108">A value of zero means that the last time a incorrect password was used is unknown.</span></span>



| <span data-ttu-id="950f6-109">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-109">Entry</span></span> | <span data-ttu-id="950f6-110">值</span><span class="sxs-lookup"><span data-stu-id="950f6-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="950f6-111">CN</span><span class="sxs-lookup"><span data-stu-id="950f6-111">CN</span></span>                | <span data-ttu-id="950f6-112">錯誤的密碼時間</span><span class="sxs-lookup"><span data-stu-id="950f6-112">Bad-Password-Time</span></span>                         |
| <span data-ttu-id="950f6-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="950f6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="950f6-114">badPasswordTime</span><span class="sxs-lookup"><span data-stu-id="950f6-114">badPasswordTime</span></span>                           |
| <span data-ttu-id="950f6-115">大小</span><span class="sxs-lookup"><span data-stu-id="950f6-115">Size</span></span>              | <span data-ttu-id="950f6-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="950f6-116">8 bytes</span></span>                                   |
| <span data-ttu-id="950f6-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="950f6-117">Update Privilege</span></span>  | <span data-ttu-id="950f6-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="950f6-118">This value is set by the system.</span></span>          |
| <span data-ttu-id="950f6-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="950f6-119">Update Frequency</span></span>  | <span data-ttu-id="950f6-120">每次使用者輸入錯誤密碼時。</span><span class="sxs-lookup"><span data-stu-id="950f6-120">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="950f6-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-121">Attribute-Id</span></span>      | <span data-ttu-id="950f6-122">1.2.840.113556.1.4.49</span><span class="sxs-lookup"><span data-stu-id="950f6-122">1.2.840.113556.1.4.49</span></span>                     |
| <span data-ttu-id="950f6-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="950f6-123">System-Id-Guid</span></span>    | <span data-ttu-id="950f6-124">bf96792d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="950f6-124">bf96792d-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="950f6-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="950f6-125">Syntax</span></span>            | [<span data-ttu-id="950f6-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="950f6-126">**Interval**</span></span>](s-interval.md)            |



## <a name="implementations"></a><span data-ttu-id="950f6-127">實作</span><span class="sxs-lookup"><span data-stu-id="950f6-127">Implementations</span></span>

-   [<span data-ttu-id="950f6-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="950f6-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="950f6-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="950f6-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="950f6-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="950f6-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="950f6-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="950f6-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="950f6-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="950f6-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="950f6-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="950f6-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="950f6-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="950f6-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="950f6-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="950f6-135">Windows 2000 Server</span></span>



| <span data-ttu-id="950f6-136">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-136">Entry</span></span> | <span data-ttu-id="950f6-137">值</span><span class="sxs-lookup"><span data-stu-id="950f6-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="950f6-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="950f6-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="950f6-140">System-Only</span></span>            | <span data-ttu-id="950f6-141">否</span><span class="sxs-lookup"><span data-stu-id="950f6-141">False</span></span>                             |
| <span data-ttu-id="950f6-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="950f6-142">Is-Single-Valued</span></span>       | <span data-ttu-id="950f6-143">對</span><span class="sxs-lookup"><span data-stu-id="950f6-143">True</span></span>                              |
| <span data-ttu-id="950f6-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="950f6-144">Is Indexed</span></span>             | <span data-ttu-id="950f6-145">否</span><span class="sxs-lookup"><span data-stu-id="950f6-145">False</span></span>                             |
| <span data-ttu-id="950f6-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="950f6-146">In Global Catalog</span></span>      | <span data-ttu-id="950f6-147">否</span><span class="sxs-lookup"><span data-stu-id="950f6-147">False</span></span>                             |
| <span data-ttu-id="950f6-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="950f6-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="950f6-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="950f6-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="950f6-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="950f6-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="950f6-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="950f6-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="950f6-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-152">Search-Flags</span></span>           | <span data-ttu-id="950f6-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="950f6-153">0x00000000</span></span>                        |
| <span data-ttu-id="950f6-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-154">System-Flags</span></span>           | <span data-ttu-id="950f6-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="950f6-155">0x00000011</span></span>                        |
| <span data-ttu-id="950f6-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="950f6-156">Classes used in</span></span>        | [<span data-ttu-id="950f6-157">**User**</span><span class="sxs-lookup"><span data-stu-id="950f6-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="950f6-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="950f6-158">Windows Server 2003</span></span>



| <span data-ttu-id="950f6-159">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-159">Entry</span></span> | <span data-ttu-id="950f6-160">值</span><span class="sxs-lookup"><span data-stu-id="950f6-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="950f6-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="950f6-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="950f6-163">System-Only</span></span>            | <span data-ttu-id="950f6-164">否</span><span class="sxs-lookup"><span data-stu-id="950f6-164">False</span></span>                             |
| <span data-ttu-id="950f6-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="950f6-165">Is-Single-Valued</span></span>       | <span data-ttu-id="950f6-166">對</span><span class="sxs-lookup"><span data-stu-id="950f6-166">True</span></span>                              |
| <span data-ttu-id="950f6-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="950f6-167">Is Indexed</span></span>             | <span data-ttu-id="950f6-168">否</span><span class="sxs-lookup"><span data-stu-id="950f6-168">False</span></span>                             |
| <span data-ttu-id="950f6-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="950f6-169">In Global Catalog</span></span>      | <span data-ttu-id="950f6-170">否</span><span class="sxs-lookup"><span data-stu-id="950f6-170">False</span></span>                             |
| <span data-ttu-id="950f6-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="950f6-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="950f6-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="950f6-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="950f6-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="950f6-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="950f6-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="950f6-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="950f6-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-175">Search-Flags</span></span>           | <span data-ttu-id="950f6-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="950f6-176">0x00000000</span></span>                        |
| <span data-ttu-id="950f6-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-177">System-Flags</span></span>           | <span data-ttu-id="950f6-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="950f6-178">0x00000011</span></span>                        |
| <span data-ttu-id="950f6-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="950f6-179">Classes used in</span></span>        | [<span data-ttu-id="950f6-180">**User**</span><span class="sxs-lookup"><span data-stu-id="950f6-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="950f6-181">亞當</span><span class="sxs-lookup"><span data-stu-id="950f6-181">ADAM</span></span>



| <span data-ttu-id="950f6-182">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-182">Entry</span></span> | <span data-ttu-id="950f6-183">值</span><span class="sxs-lookup"><span data-stu-id="950f6-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="950f6-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="950f6-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="950f6-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="950f6-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="950f6-186">System-Only</span></span>            | <span data-ttu-id="950f6-187">對</span><span class="sxs-lookup"><span data-stu-id="950f6-187">True</span></span>                                                              |
| <span data-ttu-id="950f6-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="950f6-188">Is-Single-Valued</span></span>       | <span data-ttu-id="950f6-189">對</span><span class="sxs-lookup"><span data-stu-id="950f6-189">True</span></span>                                                              |
| <span data-ttu-id="950f6-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="950f6-190">Is Indexed</span></span>             | <span data-ttu-id="950f6-191">否</span><span class="sxs-lookup"><span data-stu-id="950f6-191">False</span></span>                                                             |
| <span data-ttu-id="950f6-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="950f6-192">In Global Catalog</span></span>      | <span data-ttu-id="950f6-193">否</span><span class="sxs-lookup"><span data-stu-id="950f6-193">False</span></span>                                                             |
| <span data-ttu-id="950f6-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="950f6-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="950f6-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="950f6-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="950f6-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="950f6-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="950f6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="950f6-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="950f6-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-198">Search-Flags</span></span>           | <span data-ttu-id="950f6-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="950f6-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="950f6-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-200">System-Flags</span></span>           | <span data-ttu-id="950f6-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="950f6-201">0x00000011</span></span>                                                        |
| <span data-ttu-id="950f6-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="950f6-202">Classes used in</span></span>        | [<span data-ttu-id="950f6-203">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="950f6-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="950f6-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="950f6-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="950f6-205">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-205">Entry</span></span> | <span data-ttu-id="950f6-206">值</span><span class="sxs-lookup"><span data-stu-id="950f6-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="950f6-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="950f6-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="950f6-209">System-Only</span></span>            | <span data-ttu-id="950f6-210">否</span><span class="sxs-lookup"><span data-stu-id="950f6-210">False</span></span>                             |
| <span data-ttu-id="950f6-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="950f6-211">Is-Single-Valued</span></span>       | <span data-ttu-id="950f6-212">對</span><span class="sxs-lookup"><span data-stu-id="950f6-212">True</span></span>                              |
| <span data-ttu-id="950f6-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="950f6-213">Is Indexed</span></span>             | <span data-ttu-id="950f6-214">否</span><span class="sxs-lookup"><span data-stu-id="950f6-214">False</span></span>                             |
| <span data-ttu-id="950f6-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="950f6-215">In Global Catalog</span></span>      | <span data-ttu-id="950f6-216">否</span><span class="sxs-lookup"><span data-stu-id="950f6-216">False</span></span>                             |
| <span data-ttu-id="950f6-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="950f6-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="950f6-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="950f6-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="950f6-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="950f6-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="950f6-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="950f6-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="950f6-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-221">Search-Flags</span></span>           | <span data-ttu-id="950f6-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="950f6-222">0x00000000</span></span>                        |
| <span data-ttu-id="950f6-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-223">System-Flags</span></span>           | <span data-ttu-id="950f6-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="950f6-224">0x00000011</span></span>                        |
| <span data-ttu-id="950f6-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="950f6-225">Classes used in</span></span>        | [<span data-ttu-id="950f6-226">**User**</span><span class="sxs-lookup"><span data-stu-id="950f6-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="950f6-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="950f6-227">Windows Server 2008</span></span>



| <span data-ttu-id="950f6-228">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-228">Entry</span></span> | <span data-ttu-id="950f6-229">值</span><span class="sxs-lookup"><span data-stu-id="950f6-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="950f6-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="950f6-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="950f6-232">System-Only</span></span>            | <span data-ttu-id="950f6-233">否</span><span class="sxs-lookup"><span data-stu-id="950f6-233">False</span></span>                             |
| <span data-ttu-id="950f6-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="950f6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="950f6-235">對</span><span class="sxs-lookup"><span data-stu-id="950f6-235">True</span></span>                              |
| <span data-ttu-id="950f6-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="950f6-236">Is Indexed</span></span>             | <span data-ttu-id="950f6-237">否</span><span class="sxs-lookup"><span data-stu-id="950f6-237">False</span></span>                             |
| <span data-ttu-id="950f6-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="950f6-238">In Global Catalog</span></span>      | <span data-ttu-id="950f6-239">否</span><span class="sxs-lookup"><span data-stu-id="950f6-239">False</span></span>                             |
| <span data-ttu-id="950f6-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="950f6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="950f6-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="950f6-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="950f6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="950f6-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="950f6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="950f6-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="950f6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-244">Search-Flags</span></span>           | <span data-ttu-id="950f6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="950f6-245">0x00000000</span></span>                        |
| <span data-ttu-id="950f6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-246">System-Flags</span></span>           | <span data-ttu-id="950f6-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="950f6-247">0x00000011</span></span>                        |
| <span data-ttu-id="950f6-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="950f6-248">Classes used in</span></span>        | [<span data-ttu-id="950f6-249">**User**</span><span class="sxs-lookup"><span data-stu-id="950f6-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="950f6-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="950f6-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="950f6-251">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-251">Entry</span></span> | <span data-ttu-id="950f6-252">值</span><span class="sxs-lookup"><span data-stu-id="950f6-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="950f6-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="950f6-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="950f6-255">System-Only</span></span>            | <span data-ttu-id="950f6-256">否</span><span class="sxs-lookup"><span data-stu-id="950f6-256">False</span></span>                             |
| <span data-ttu-id="950f6-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="950f6-257">Is-Single-Valued</span></span>       | <span data-ttu-id="950f6-258">對</span><span class="sxs-lookup"><span data-stu-id="950f6-258">True</span></span>                              |
| <span data-ttu-id="950f6-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="950f6-259">Is Indexed</span></span>             | <span data-ttu-id="950f6-260">否</span><span class="sxs-lookup"><span data-stu-id="950f6-260">False</span></span>                             |
| <span data-ttu-id="950f6-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="950f6-261">In Global Catalog</span></span>      | <span data-ttu-id="950f6-262">否</span><span class="sxs-lookup"><span data-stu-id="950f6-262">False</span></span>                             |
| <span data-ttu-id="950f6-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="950f6-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="950f6-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="950f6-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="950f6-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="950f6-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="950f6-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="950f6-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="950f6-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-267">Search-Flags</span></span>           | <span data-ttu-id="950f6-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="950f6-268">0x00000000</span></span>                        |
| <span data-ttu-id="950f6-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-269">System-Flags</span></span>           | <span data-ttu-id="950f6-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="950f6-270">0x00000011</span></span>                        |
| <span data-ttu-id="950f6-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="950f6-271">Classes used in</span></span>        | [<span data-ttu-id="950f6-272">**User**</span><span class="sxs-lookup"><span data-stu-id="950f6-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="950f6-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="950f6-273">Windows Server 2012</span></span>



| <span data-ttu-id="950f6-274">進入</span><span class="sxs-lookup"><span data-stu-id="950f6-274">Entry</span></span> | <span data-ttu-id="950f6-275">值</span><span class="sxs-lookup"><span data-stu-id="950f6-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="950f6-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="950f6-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="950f6-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="950f6-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="950f6-278">System-Only</span></span>            | <span data-ttu-id="950f6-279">否</span><span class="sxs-lookup"><span data-stu-id="950f6-279">False</span></span>                             |
| <span data-ttu-id="950f6-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="950f6-280">Is-Single-Valued</span></span>       | <span data-ttu-id="950f6-281">對</span><span class="sxs-lookup"><span data-stu-id="950f6-281">True</span></span>                              |
| <span data-ttu-id="950f6-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="950f6-282">Is Indexed</span></span>             | <span data-ttu-id="950f6-283">否</span><span class="sxs-lookup"><span data-stu-id="950f6-283">False</span></span>                             |
| <span data-ttu-id="950f6-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="950f6-284">In Global Catalog</span></span>      | <span data-ttu-id="950f6-285">否</span><span class="sxs-lookup"><span data-stu-id="950f6-285">False</span></span>                             |
| <span data-ttu-id="950f6-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="950f6-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="950f6-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="950f6-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="950f6-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="950f6-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="950f6-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="950f6-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="950f6-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-290">Search-Flags</span></span>           | <span data-ttu-id="950f6-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="950f6-291">0x00000000</span></span>                        |
| <span data-ttu-id="950f6-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="950f6-292">System-Flags</span></span>           | <span data-ttu-id="950f6-293">0x00000011</span><span class="sxs-lookup"><span data-stu-id="950f6-293">0x00000011</span></span>                        |
| <span data-ttu-id="950f6-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="950f6-294">Classes used in</span></span>        | [<span data-ttu-id="950f6-295">**User**</span><span class="sxs-lookup"><span data-stu-id="950f6-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="950f6-296">備註</span><span class="sxs-lookup"><span data-stu-id="950f6-296">Remarks</span></span>

<span data-ttu-id="950f6-297">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="950f6-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="950f6-298">這個屬性不會複寫，並且會在網域中的每個網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="950f6-298">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="950f6-299">若要取得使用者在網域中的上次錯誤密碼時間的準確值，您必須查詢網域中的每個網域控制站。</span><span class="sxs-lookup"><span data-stu-id="950f6-299">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried.</span></span> <span data-ttu-id="950f6-300">取得的最大值代表真正錯誤的密碼時間。</span><span class="sxs-lookup"><span data-stu-id="950f6-300">The largest value that is obtained represents the true bad password time.</span></span>

 

