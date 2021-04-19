---
title: Pwd-Last-Set 屬性
description: 此帳戶的密碼上次變更的日期和時間。
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- Pwd-Last-Set attribute AD Schema
- pwdLastSet 屬性 AD 架構
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc49fbbf768d2ca873f6f35f61022cc9182830b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970481"
---
# <a name="pwd-last-set-attribute"></a><span data-ttu-id="a3f34-105">Pwd-Last-Set 屬性</span><span class="sxs-lookup"><span data-stu-id="a3f34-105">Pwd-Last-Set attribute</span></span>

<span data-ttu-id="a3f34-106">此帳戶的密碼上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a3f34-106">The date and time that the password for this account was last changed.</span></span> <span data-ttu-id="a3f34-107">此值會儲存為大整數，表示自1601年1月1日 (UTC) 起的100毫微秒間隔數。</span><span class="sxs-lookup"><span data-stu-id="a3f34-107">This value is stored as a large integer that represents the number of 100 nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="a3f34-108">如果這個值設定為0，而且 [**使用者-帳戶控制**](a-useraccountcontrol.md) 屬性不包含 [UF] 未 **過期的 [ \_ \_ \_ PASSWD** ] 旗標，則使用者必須在下次登入時設定密碼。</span><span class="sxs-lookup"><span data-stu-id="a3f34-108">If this value is set to 0 and the [**User-Account-Control**](a-useraccountcontrol.md) attribute does not contain the **UF\_DONT\_EXPIRE\_PASSWD** flag, then the user must set the password at the next logon.</span></span>



| <span data-ttu-id="a3f34-109">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-109">Entry</span></span> | <span data-ttu-id="a3f34-110">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a3f34-111">CN</span><span class="sxs-lookup"><span data-stu-id="a3f34-111">CN</span></span>                | <span data-ttu-id="a3f34-112">Pwd-上次設定</span><span class="sxs-lookup"><span data-stu-id="a3f34-112">Pwd-Last-Set</span></span>                         |
| <span data-ttu-id="a3f34-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a3f34-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a3f34-114">pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="a3f34-114">pwdLastSet</span></span>                           |
| <span data-ttu-id="a3f34-115">大小</span><span class="sxs-lookup"><span data-stu-id="a3f34-115">Size</span></span>              | <span data-ttu-id="a3f34-116">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="a3f34-116">8 bytes</span></span>                              |
| <span data-ttu-id="a3f34-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a3f34-117">Update Privilege</span></span>  | <span data-ttu-id="a3f34-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a3f34-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="a3f34-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a3f34-119">Update Frequency</span></span>  | <span data-ttu-id="a3f34-120">每次密碼變更時。</span><span class="sxs-lookup"><span data-stu-id="a3f34-120">Each time the password is changed.</span></span>   |
| <span data-ttu-id="a3f34-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-121">Attribute-Id</span></span>      | <span data-ttu-id="a3f34-122">1.2.840.113556.1.4.96</span><span class="sxs-lookup"><span data-stu-id="a3f34-122">1.2.840.113556.1.4.96</span></span>                |
| <span data-ttu-id="a3f34-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a3f34-123">System-Id-Guid</span></span>    | <span data-ttu-id="a3f34-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a3f34-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a3f34-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3f34-125">Syntax</span></span>            | [<span data-ttu-id="a3f34-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="a3f34-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="a3f34-127">實作</span><span class="sxs-lookup"><span data-stu-id="a3f34-127">Implementations</span></span>

-   [<span data-ttu-id="a3f34-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a3f34-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a3f34-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3f34-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3f34-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a3f34-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a3f34-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3f34-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3f34-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3f34-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3f34-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3f34-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3f34-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3f34-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a3f34-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3f34-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a3f34-136">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-136">Entry</span></span> | <span data-ttu-id="a3f34-137">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3f34-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f34-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3f34-140">System-Only</span></span>            | <span data-ttu-id="a3f34-141">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-141">False</span></span>                             |
| <span data-ttu-id="a3f34-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3f34-142">Is-Single-Valued</span></span>       | <span data-ttu-id="a3f34-143">對</span><span class="sxs-lookup"><span data-stu-id="a3f34-143">True</span></span>                              |
| <span data-ttu-id="a3f34-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3f34-144">Is Indexed</span></span>             | <span data-ttu-id="a3f34-145">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-145">False</span></span>                             |
| <span data-ttu-id="a3f34-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3f34-146">In Global Catalog</span></span>      | <span data-ttu-id="a3f34-147">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-147">False</span></span>                             |
| <span data-ttu-id="a3f34-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3f34-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3f34-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3f34-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3f34-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3f34-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3f34-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3f34-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3f34-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-152">Search-Flags</span></span>           | <span data-ttu-id="a3f34-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3f34-153">0x00000000</span></span>                        |
| <span data-ttu-id="a3f34-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-154">System-Flags</span></span>           | <span data-ttu-id="a3f34-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3f34-155">0x00000010</span></span>                        |
| <span data-ttu-id="a3f34-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3f34-156">Classes used in</span></span>        | [<span data-ttu-id="a3f34-157">**User**</span><span class="sxs-lookup"><span data-stu-id="a3f34-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a3f34-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3f34-158">Windows Server 2003</span></span>



| <span data-ttu-id="a3f34-159">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-159">Entry</span></span> | <span data-ttu-id="a3f34-160">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3f34-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f34-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3f34-163">System-Only</span></span>            | <span data-ttu-id="a3f34-164">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-164">False</span></span>                             |
| <span data-ttu-id="a3f34-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3f34-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a3f34-166">對</span><span class="sxs-lookup"><span data-stu-id="a3f34-166">True</span></span>                              |
| <span data-ttu-id="a3f34-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3f34-167">Is Indexed</span></span>             | <span data-ttu-id="a3f34-168">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-168">False</span></span>                             |
| <span data-ttu-id="a3f34-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3f34-169">In Global Catalog</span></span>      | <span data-ttu-id="a3f34-170">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-170">False</span></span>                             |
| <span data-ttu-id="a3f34-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3f34-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3f34-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3f34-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3f34-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3f34-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3f34-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3f34-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3f34-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-175">Search-Flags</span></span>           | <span data-ttu-id="a3f34-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3f34-176">0x00000000</span></span>                        |
| <span data-ttu-id="a3f34-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-177">System-Flags</span></span>           | <span data-ttu-id="a3f34-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3f34-178">0x00000010</span></span>                        |
| <span data-ttu-id="a3f34-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3f34-179">Classes used in</span></span>        | [<span data-ttu-id="a3f34-180">**User**</span><span class="sxs-lookup"><span data-stu-id="a3f34-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a3f34-181">亞當</span><span class="sxs-lookup"><span data-stu-id="a3f34-181">ADAM</span></span>



| <span data-ttu-id="a3f34-182">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-182">Entry</span></span> | <span data-ttu-id="a3f34-183">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a3f34-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f34-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a3f34-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a3f34-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3f34-186">System-Only</span></span>            | <span data-ttu-id="a3f34-187">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-187">False</span></span>                                                             |
| <span data-ttu-id="a3f34-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3f34-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a3f34-189">對</span><span class="sxs-lookup"><span data-stu-id="a3f34-189">True</span></span>                                                              |
| <span data-ttu-id="a3f34-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3f34-190">Is Indexed</span></span>             | <span data-ttu-id="a3f34-191">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-191">False</span></span>                                                             |
| <span data-ttu-id="a3f34-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3f34-192">In Global Catalog</span></span>      | <span data-ttu-id="a3f34-193">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-193">False</span></span>                                                             |
| <span data-ttu-id="a3f34-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3f34-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3f34-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3f34-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a3f34-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3f34-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a3f34-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3f34-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a3f34-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-198">Search-Flags</span></span>           | <span data-ttu-id="a3f34-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3f34-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="a3f34-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-200">System-Flags</span></span>           | <span data-ttu-id="a3f34-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3f34-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="a3f34-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3f34-202">Classes used in</span></span>        | [<span data-ttu-id="a3f34-203">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="a3f34-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3f34-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3f34-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3f34-205">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-205">Entry</span></span> | <span data-ttu-id="a3f34-206">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3f34-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f34-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3f34-209">System-Only</span></span>            | <span data-ttu-id="a3f34-210">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-210">False</span></span>                             |
| <span data-ttu-id="a3f34-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3f34-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a3f34-212">對</span><span class="sxs-lookup"><span data-stu-id="a3f34-212">True</span></span>                              |
| <span data-ttu-id="a3f34-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3f34-213">Is Indexed</span></span>             | <span data-ttu-id="a3f34-214">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-214">False</span></span>                             |
| <span data-ttu-id="a3f34-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3f34-215">In Global Catalog</span></span>      | <span data-ttu-id="a3f34-216">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-216">False</span></span>                             |
| <span data-ttu-id="a3f34-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3f34-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3f34-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3f34-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3f34-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3f34-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3f34-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3f34-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3f34-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-221">Search-Flags</span></span>           | <span data-ttu-id="a3f34-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3f34-222">0x00000000</span></span>                        |
| <span data-ttu-id="a3f34-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-223">System-Flags</span></span>           | <span data-ttu-id="a3f34-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3f34-224">0x00000010</span></span>                        |
| <span data-ttu-id="a3f34-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3f34-225">Classes used in</span></span>        | [<span data-ttu-id="a3f34-226">**User**</span><span class="sxs-lookup"><span data-stu-id="a3f34-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3f34-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3f34-227">Windows Server 2008</span></span>



| <span data-ttu-id="a3f34-228">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-228">Entry</span></span> | <span data-ttu-id="a3f34-229">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3f34-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f34-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3f34-232">System-Only</span></span>            | <span data-ttu-id="a3f34-233">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-233">False</span></span>                             |
| <span data-ttu-id="a3f34-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3f34-234">Is-Single-Valued</span></span>       | <span data-ttu-id="a3f34-235">對</span><span class="sxs-lookup"><span data-stu-id="a3f34-235">True</span></span>                              |
| <span data-ttu-id="a3f34-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3f34-236">Is Indexed</span></span>             | <span data-ttu-id="a3f34-237">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-237">False</span></span>                             |
| <span data-ttu-id="a3f34-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3f34-238">In Global Catalog</span></span>      | <span data-ttu-id="a3f34-239">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-239">False</span></span>                             |
| <span data-ttu-id="a3f34-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3f34-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3f34-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3f34-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3f34-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3f34-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3f34-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3f34-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3f34-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-244">Search-Flags</span></span>           | <span data-ttu-id="a3f34-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3f34-245">0x00000000</span></span>                        |
| <span data-ttu-id="a3f34-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-246">System-Flags</span></span>           | <span data-ttu-id="a3f34-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3f34-247">0x00000010</span></span>                        |
| <span data-ttu-id="a3f34-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3f34-248">Classes used in</span></span>        | [<span data-ttu-id="a3f34-249">**User**</span><span class="sxs-lookup"><span data-stu-id="a3f34-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3f34-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3f34-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3f34-251">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-251">Entry</span></span> | <span data-ttu-id="a3f34-252">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3f34-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f34-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3f34-255">System-Only</span></span>            | <span data-ttu-id="a3f34-256">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-256">False</span></span>                             |
| <span data-ttu-id="a3f34-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3f34-257">Is-Single-Valued</span></span>       | <span data-ttu-id="a3f34-258">對</span><span class="sxs-lookup"><span data-stu-id="a3f34-258">True</span></span>                              |
| <span data-ttu-id="a3f34-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3f34-259">Is Indexed</span></span>             | <span data-ttu-id="a3f34-260">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-260">False</span></span>                             |
| <span data-ttu-id="a3f34-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3f34-261">In Global Catalog</span></span>      | <span data-ttu-id="a3f34-262">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-262">False</span></span>                             |
| <span data-ttu-id="a3f34-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3f34-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3f34-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3f34-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3f34-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3f34-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3f34-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3f34-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3f34-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-267">Search-Flags</span></span>           | <span data-ttu-id="a3f34-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3f34-268">0x00000000</span></span>                        |
| <span data-ttu-id="a3f34-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-269">System-Flags</span></span>           | <span data-ttu-id="a3f34-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3f34-270">0x00000010</span></span>                        |
| <span data-ttu-id="a3f34-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3f34-271">Classes used in</span></span>        | [<span data-ttu-id="a3f34-272">**User**</span><span class="sxs-lookup"><span data-stu-id="a3f34-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3f34-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3f34-273">Windows Server 2012</span></span>



| <span data-ttu-id="a3f34-274">進入</span><span class="sxs-lookup"><span data-stu-id="a3f34-274">Entry</span></span> | <span data-ttu-id="a3f34-275">值</span><span class="sxs-lookup"><span data-stu-id="a3f34-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a3f34-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f34-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3f34-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a3f34-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3f34-278">System-Only</span></span>            | <span data-ttu-id="a3f34-279">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-279">False</span></span>                             |
| <span data-ttu-id="a3f34-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3f34-280">Is-Single-Valued</span></span>       | <span data-ttu-id="a3f34-281">對</span><span class="sxs-lookup"><span data-stu-id="a3f34-281">True</span></span>                              |
| <span data-ttu-id="a3f34-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3f34-282">Is Indexed</span></span>             | <span data-ttu-id="a3f34-283">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-283">False</span></span>                             |
| <span data-ttu-id="a3f34-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3f34-284">In Global Catalog</span></span>      | <span data-ttu-id="a3f34-285">否</span><span class="sxs-lookup"><span data-stu-id="a3f34-285">False</span></span>                             |
| <span data-ttu-id="a3f34-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3f34-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3f34-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3f34-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a3f34-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3f34-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a3f34-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3f34-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a3f34-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-290">Search-Flags</span></span>           | <span data-ttu-id="a3f34-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3f34-291">0x00000000</span></span>                        |
| <span data-ttu-id="a3f34-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3f34-292">System-Flags</span></span>           | <span data-ttu-id="a3f34-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3f34-293">0x00000010</span></span>                        |
| <span data-ttu-id="a3f34-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3f34-294">Classes used in</span></span>        | [<span data-ttu-id="a3f34-295">**User**</span><span class="sxs-lookup"><span data-stu-id="a3f34-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a3f34-296">備註</span><span class="sxs-lookup"><span data-stu-id="a3f34-296">Remarks</span></span>

<span data-ttu-id="a3f34-297">這個大型整數的最高部分對應至 [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)結構的 **dwHighDateTime** 成員，而低部分則對應至 **filetime** 結構的 **dwLowDateTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="a3f34-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3f34-298">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3f34-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f34-299">**使用者帳戶控制**</span><span class="sxs-lookup"><span data-stu-id="a3f34-299">**User-Account-Control**</span></span>](a-useraccountcontrol.md)
</dt> </dl>

 

