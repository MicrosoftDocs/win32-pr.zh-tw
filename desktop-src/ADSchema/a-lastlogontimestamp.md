---
title: 上次登入時間戳記屬性
description: 這是使用者上次登入網域的時間。
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- 上次登入時間戳記屬性 AD 架構
- lastLogonTimestamp 屬性 AD 架構
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107238"
---
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="f4e0b-105">上次登入時間戳記屬性</span><span class="sxs-lookup"><span data-stu-id="f4e0b-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="f4e0b-106">這是使用者上次登入網域的時間。</span><span class="sxs-lookup"><span data-stu-id="f4e0b-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="f4e0b-107">此值會儲存為大整數，表示自1601年1月1日起 (UTC) 的 100-2-2-2-2-秒間隔。</span><span class="sxs-lookup"><span data-stu-id="f4e0b-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="f4e0b-108">每當使用者登入時，就會從 DC 讀取這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="f4e0b-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="f4e0b-109">如果值較舊 \[ `current_time - msDS-LogonTimeSyncInterval` \] ，則會更新值。</span><span class="sxs-lookup"><span data-stu-id="f4e0b-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="f4e0b-110">網域功能等級提高之後的初始更新會計算為14天減去5天的隨機百分比。</span><span class="sxs-lookup"><span data-stu-id="f4e0b-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="f4e0b-111">進入</span><span class="sxs-lookup"><span data-stu-id="f4e0b-111">Entry</span></span> | <span data-ttu-id="f4e0b-112">值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e0b-113">CN</span><span class="sxs-lookup"><span data-stu-id="f4e0b-113">CN</span></span>                | <span data-ttu-id="f4e0b-114">上次登入時間戳記</span><span class="sxs-lookup"><span data-stu-id="f4e0b-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="f4e0b-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f4e0b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="f4e0b-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="f4e0b-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="f4e0b-117">大小</span><span class="sxs-lookup"><span data-stu-id="f4e0b-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="f4e0b-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f4e0b-118">Update Privilege</span></span>  | <span data-ttu-id="f4e0b-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="f4e0b-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="f4e0b-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f4e0b-120">Update Frequency</span></span>  | <span data-ttu-id="f4e0b-121">當使用者登入時，以及此值是否早于目前的時間減去 LogonTimeSyncInterval 的值。</span><span class="sxs-lookup"><span data-stu-id="f4e0b-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="f4e0b-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4e0b-122">Attribute-Id</span></span>      | <span data-ttu-id="f4e0b-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="f4e0b-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="f4e0b-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f4e0b-124">System-Id-Guid</span></span>    | <span data-ttu-id="f4e0b-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="f4e0b-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="f4e0b-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4e0b-126">Syntax</span></span>            | [<span data-ttu-id="f4e0b-127">**間隔**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="f4e0b-128">實作</span><span class="sxs-lookup"><span data-stu-id="f4e0b-128">Implementations</span></span>

-   [<span data-ttu-id="f4e0b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4e0b-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f4e0b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4e0b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4e0b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4e0b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f4e0b-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4e0b-135">Windows Server 2003</span></span>



| <span data-ttu-id="f4e0b-136">進入</span><span class="sxs-lookup"><span data-stu-id="f4e0b-136">Entry</span></span> | <span data-ttu-id="f4e0b-137">值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4e0b-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e0b-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e0b-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e0b-140">System-Only</span></span>            | <span data-ttu-id="f4e0b-141">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-141">False</span></span>                             |
| <span data-ttu-id="f4e0b-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e0b-143">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-143">True</span></span>                              |
| <span data-ttu-id="f4e0b-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e0b-144">Is Indexed</span></span>             | <span data-ttu-id="f4e0b-145">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-145">False</span></span>                             |
| <span data-ttu-id="f4e0b-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e0b-146">In Global Catalog</span></span>      | <span data-ttu-id="f4e0b-147">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-147">False</span></span>                             |
| <span data-ttu-id="f4e0b-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e0b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e0b-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e0b-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4e0b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e0b-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e0b-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-152">Search-Flags</span></span>           | <span data-ttu-id="f4e0b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e0b-153">0x00000000</span></span>                        |
| <span data-ttu-id="f4e0b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-154">System-Flags</span></span>           | <span data-ttu-id="f4e0b-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e0b-155">0x00000010</span></span>                        |
| <span data-ttu-id="f4e0b-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e0b-156">Classes used in</span></span>        | [<span data-ttu-id="f4e0b-157">**User**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f4e0b-158">亞當</span><span class="sxs-lookup"><span data-stu-id="f4e0b-158">ADAM</span></span>



| <span data-ttu-id="f4e0b-159">進入</span><span class="sxs-lookup"><span data-stu-id="f4e0b-159">Entry</span></span> | <span data-ttu-id="f4e0b-160">值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4e0b-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e0b-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4e0b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e0b-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f4e0b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e0b-163">System-Only</span></span>            | <span data-ttu-id="f4e0b-164">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-164">True</span></span>                                                              |
| <span data-ttu-id="f4e0b-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e0b-166">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-166">True</span></span>                                                              |
| <span data-ttu-id="f4e0b-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e0b-167">Is Indexed</span></span>             | <span data-ttu-id="f4e0b-168">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-168">False</span></span>                                                             |
| <span data-ttu-id="f4e0b-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e0b-169">In Global Catalog</span></span>      | <span data-ttu-id="f4e0b-170">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-170">False</span></span>                                                             |
| <span data-ttu-id="f4e0b-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e0b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e0b-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e0b-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f4e0b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e0b-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f4e0b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e0b-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f4e0b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-175">Search-Flags</span></span>           | <span data-ttu-id="f4e0b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e0b-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="f4e0b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-177">System-Flags</span></span>           | <span data-ttu-id="f4e0b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e0b-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="f4e0b-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e0b-179">Classes used in</span></span>        | [<span data-ttu-id="f4e0b-180">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4e0b-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4e0b-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4e0b-182">進入</span><span class="sxs-lookup"><span data-stu-id="f4e0b-182">Entry</span></span> | <span data-ttu-id="f4e0b-183">值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4e0b-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e0b-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e0b-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e0b-186">System-Only</span></span>            | <span data-ttu-id="f4e0b-187">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-187">False</span></span>                             |
| <span data-ttu-id="f4e0b-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e0b-189">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-189">True</span></span>                              |
| <span data-ttu-id="f4e0b-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e0b-190">Is Indexed</span></span>             | <span data-ttu-id="f4e0b-191">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-191">False</span></span>                             |
| <span data-ttu-id="f4e0b-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e0b-192">In Global Catalog</span></span>      | <span data-ttu-id="f4e0b-193">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-193">False</span></span>                             |
| <span data-ttu-id="f4e0b-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e0b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e0b-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e0b-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4e0b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e0b-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e0b-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-198">Search-Flags</span></span>           | <span data-ttu-id="f4e0b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4e0b-199">0x00000000</span></span>                        |
| <span data-ttu-id="f4e0b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-200">System-Flags</span></span>           | <span data-ttu-id="f4e0b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e0b-201">0x00000010</span></span>                        |
| <span data-ttu-id="f4e0b-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e0b-202">Classes used in</span></span>        | [<span data-ttu-id="f4e0b-203">**User**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4e0b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4e0b-204">Windows Server 2008</span></span>



| <span data-ttu-id="f4e0b-205">進入</span><span class="sxs-lookup"><span data-stu-id="f4e0b-205">Entry</span></span> | <span data-ttu-id="f4e0b-206">值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4e0b-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e0b-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e0b-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e0b-209">System-Only</span></span>            | <span data-ttu-id="f4e0b-210">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-210">False</span></span>                             |
| <span data-ttu-id="f4e0b-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e0b-212">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-212">True</span></span>                              |
| <span data-ttu-id="f4e0b-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e0b-213">Is Indexed</span></span>             | <span data-ttu-id="f4e0b-214">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-214">True</span></span>                              |
| <span data-ttu-id="f4e0b-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e0b-215">In Global Catalog</span></span>      | <span data-ttu-id="f4e0b-216">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-216">True</span></span>                              |
| <span data-ttu-id="f4e0b-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e0b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e0b-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e0b-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4e0b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e0b-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e0b-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-221">Search-Flags</span></span>           | <span data-ttu-id="f4e0b-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f4e0b-222">0x00000001</span></span>                        |
| <span data-ttu-id="f4e0b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-223">System-Flags</span></span>           | <span data-ttu-id="f4e0b-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e0b-224">0x00000010</span></span>                        |
| <span data-ttu-id="f4e0b-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e0b-225">Classes used in</span></span>        | [<span data-ttu-id="f4e0b-226">**User**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4e0b-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4e0b-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4e0b-228">進入</span><span class="sxs-lookup"><span data-stu-id="f4e0b-228">Entry</span></span> | <span data-ttu-id="f4e0b-229">值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4e0b-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e0b-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e0b-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e0b-232">System-Only</span></span>            | <span data-ttu-id="f4e0b-233">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-233">False</span></span>                             |
| <span data-ttu-id="f4e0b-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e0b-235">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-235">True</span></span>                              |
| <span data-ttu-id="f4e0b-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e0b-236">Is Indexed</span></span>             | <span data-ttu-id="f4e0b-237">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-237">True</span></span>                              |
| <span data-ttu-id="f4e0b-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e0b-238">In Global Catalog</span></span>      | <span data-ttu-id="f4e0b-239">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-239">True</span></span>                              |
| <span data-ttu-id="f4e0b-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e0b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e0b-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e0b-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4e0b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e0b-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e0b-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-244">Search-Flags</span></span>           | <span data-ttu-id="f4e0b-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f4e0b-245">0x00000001</span></span>                        |
| <span data-ttu-id="f4e0b-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-246">System-Flags</span></span>           | <span data-ttu-id="f4e0b-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e0b-247">0x00000010</span></span>                        |
| <span data-ttu-id="f4e0b-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e0b-248">Classes used in</span></span>        | [<span data-ttu-id="f4e0b-249">**User**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4e0b-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4e0b-250">Windows Server 2012</span></span>



| <span data-ttu-id="f4e0b-251">進入</span><span class="sxs-lookup"><span data-stu-id="f4e0b-251">Entry</span></span> | <span data-ttu-id="f4e0b-252">值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f4e0b-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4e0b-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4e0b-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f4e0b-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4e0b-255">System-Only</span></span>            | <span data-ttu-id="f4e0b-256">否</span><span class="sxs-lookup"><span data-stu-id="f4e0b-256">False</span></span>                             |
| <span data-ttu-id="f4e0b-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4e0b-257">Is-Single-Valued</span></span>       | <span data-ttu-id="f4e0b-258">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-258">True</span></span>                              |
| <span data-ttu-id="f4e0b-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4e0b-259">Is Indexed</span></span>             | <span data-ttu-id="f4e0b-260">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-260">True</span></span>                              |
| <span data-ttu-id="f4e0b-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4e0b-261">In Global Catalog</span></span>      | <span data-ttu-id="f4e0b-262">對</span><span class="sxs-lookup"><span data-stu-id="f4e0b-262">True</span></span>                              |
| <span data-ttu-id="f4e0b-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4e0b-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4e0b-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4e0b-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f4e0b-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4e0b-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4e0b-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f4e0b-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-267">Search-Flags</span></span>           | <span data-ttu-id="f4e0b-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f4e0b-268">0x00000001</span></span>                        |
| <span data-ttu-id="f4e0b-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4e0b-269">System-Flags</span></span>           | <span data-ttu-id="f4e0b-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4e0b-270">0x00000010</span></span>                        |
| <span data-ttu-id="f4e0b-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4e0b-271">Classes used in</span></span>        | [<span data-ttu-id="f4e0b-272">**User**</span><span class="sxs-lookup"><span data-stu-id="f4e0b-272">**User**</span></span>](c-user.md)<br/> |



 

 





