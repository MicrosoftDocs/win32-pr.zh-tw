---
title: SAM-Account-Name 屬性
description: 用來支援執行舊版作業系統之用戶端和伺服器的登入名稱，例如 Windows NT 4.0、Windows 95、Windows 98 和 LAN Manager。
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- SAM-帳戶-名稱屬性 AD 架構
- sAMAccountName 屬性 AD 架構
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845312"
---
# <a name="sam-account-name-attribute"></a><span data-ttu-id="43917-105">SAM-Account-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="43917-105">SAM-Account-Name attribute</span></span>

<span data-ttu-id="43917-106">用來支援執行舊版作業系統之用戶端和伺服器的登入名稱，例如 Windows NT 4.0、Windows 95、Windows 98 和 LAN Manager。</span><span class="sxs-lookup"><span data-stu-id="43917-106">The logon name used to support clients and servers running earlier versions of the operating system, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span>

<span data-ttu-id="43917-107">這個屬性必須是20個字元以上，才能支援較早的用戶端，而且不能包含下列任何字元：</span><span class="sxs-lookup"><span data-stu-id="43917-107">This attribute must be 20 characters or less to support earlier clients, and cannot contain any of these characters:</span></span>

-   <span data-ttu-id="43917-108">"/ \\ \[ \] : ; \| = , + \* ?</span><span class="sxs-lookup"><span data-stu-id="43917-108">"/ \\ \[ \] : ; \| = , + \* ?</span></span> <span data-ttu-id="43917-109">< ></span><span class="sxs-lookup"><span data-stu-id="43917-109">< ></span></span>



| <span data-ttu-id="43917-110">進入</span><span class="sxs-lookup"><span data-stu-id="43917-110">Entry</span></span> | <span data-ttu-id="43917-111">值</span><span class="sxs-lookup"><span data-stu-id="43917-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43917-112">CN</span><span class="sxs-lookup"><span data-stu-id="43917-112">CN</span></span>                | <span data-ttu-id="43917-113">SAM-帳戶-名稱</span><span class="sxs-lookup"><span data-stu-id="43917-113">SAM-Account-Name</span></span>                                                                         |
| <span data-ttu-id="43917-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="43917-114">Ldap-Display-Name</span></span> | <span data-ttu-id="43917-115">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="43917-115">sAMAccountName</span></span>                                                                           |
| <span data-ttu-id="43917-116">大小</span><span class="sxs-lookup"><span data-stu-id="43917-116">Size</span></span>              | <span data-ttu-id="43917-117">20個字元或更少。</span><span class="sxs-lookup"><span data-stu-id="43917-117">20 characters or less.</span></span>                                                                   |
| <span data-ttu-id="43917-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="43917-118">Update Privilege</span></span>  | <span data-ttu-id="43917-119">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="43917-119">Domain administrator</span></span>                                                                     |
| <span data-ttu-id="43917-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="43917-120">Update Frequency</span></span>  | <span data-ttu-id="43917-121">建立客戶紀錄時，應該指派此值，而且不應該變更。</span><span class="sxs-lookup"><span data-stu-id="43917-121">This value should be assigned when the account record is created, and should not change.</span></span> |
| <span data-ttu-id="43917-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="43917-122">Attribute-Id</span></span>      | <span data-ttu-id="43917-123">1.2.840.113556.1.4.221</span><span class="sxs-lookup"><span data-stu-id="43917-123">1.2.840.113556.1.4.221</span></span>                                                                   |
| <span data-ttu-id="43917-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="43917-124">System-Id-Guid</span></span>    | <span data-ttu-id="43917-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="43917-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span></span>                                                     |
| <span data-ttu-id="43917-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="43917-126">Syntax</span></span>            | [<span data-ttu-id="43917-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="43917-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                              |



## <a name="implementations"></a><span data-ttu-id="43917-128">實作</span><span class="sxs-lookup"><span data-stu-id="43917-128">Implementations</span></span>

-   [<span data-ttu-id="43917-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="43917-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="43917-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="43917-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="43917-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="43917-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="43917-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="43917-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="43917-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="43917-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="43917-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="43917-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="43917-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="43917-135">Windows 2000 Server</span></span>



| <span data-ttu-id="43917-136">進入</span><span class="sxs-lookup"><span data-stu-id="43917-136">Entry</span></span> | <span data-ttu-id="43917-137">值</span><span class="sxs-lookup"><span data-stu-id="43917-137">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="43917-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43917-138">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43917-139">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="43917-140">System-Only</span></span>            | <span data-ttu-id="43917-141">否</span><span class="sxs-lookup"><span data-stu-id="43917-141">False</span></span>                                                        |
| <span data-ttu-id="43917-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43917-142">Is-Single-Valued</span></span>       | <span data-ttu-id="43917-143">對</span><span class="sxs-lookup"><span data-stu-id="43917-143">True</span></span>                                                         |
| <span data-ttu-id="43917-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43917-144">Is Indexed</span></span>             | <span data-ttu-id="43917-145">對</span><span class="sxs-lookup"><span data-stu-id="43917-145">True</span></span>                                                         |
| <span data-ttu-id="43917-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43917-146">In Global Catalog</span></span>      | <span data-ttu-id="43917-147">對</span><span class="sxs-lookup"><span data-stu-id="43917-147">True</span></span>                                                         |
| <span data-ttu-id="43917-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43917-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="43917-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43917-149">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="43917-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43917-150">Range-Lower</span></span>            | <span data-ttu-id="43917-151">0</span><span class="sxs-lookup"><span data-stu-id="43917-151">0</span></span>                                                            |
| <span data-ttu-id="43917-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43917-152">Range-Upper</span></span>            | <span data-ttu-id="43917-153">256</span><span class="sxs-lookup"><span data-stu-id="43917-153">256</span></span>                                                          |
| <span data-ttu-id="43917-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-154">Search-Flags</span></span>           | <span data-ttu-id="43917-155">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="43917-155">0x0000000D</span></span>                                                   |
| <span data-ttu-id="43917-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-156">System-Flags</span></span>           | <span data-ttu-id="43917-157">0x00000012</span><span class="sxs-lookup"><span data-stu-id="43917-157">0x00000012</span></span>                                                   |
| <span data-ttu-id="43917-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43917-158">Classes used in</span></span>        | [<span data-ttu-id="43917-159">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="43917-159">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="43917-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="43917-160">Windows Server 2003</span></span>



| <span data-ttu-id="43917-161">進入</span><span class="sxs-lookup"><span data-stu-id="43917-161">Entry</span></span> | <span data-ttu-id="43917-162">值</span><span class="sxs-lookup"><span data-stu-id="43917-162">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="43917-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43917-163">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43917-164">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="43917-165">System-Only</span></span>            | <span data-ttu-id="43917-166">否</span><span class="sxs-lookup"><span data-stu-id="43917-166">False</span></span>                                                        |
| <span data-ttu-id="43917-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43917-167">Is-Single-Valued</span></span>       | <span data-ttu-id="43917-168">對</span><span class="sxs-lookup"><span data-stu-id="43917-168">True</span></span>                                                         |
| <span data-ttu-id="43917-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43917-169">Is Indexed</span></span>             | <span data-ttu-id="43917-170">對</span><span class="sxs-lookup"><span data-stu-id="43917-170">True</span></span>                                                         |
| <span data-ttu-id="43917-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43917-171">In Global Catalog</span></span>      | <span data-ttu-id="43917-172">對</span><span class="sxs-lookup"><span data-stu-id="43917-172">True</span></span>                                                         |
| <span data-ttu-id="43917-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43917-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="43917-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43917-174">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="43917-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43917-175">Range-Lower</span></span>            | <span data-ttu-id="43917-176">0</span><span class="sxs-lookup"><span data-stu-id="43917-176">0</span></span>                                                            |
| <span data-ttu-id="43917-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43917-177">Range-Upper</span></span>            | <span data-ttu-id="43917-178">256</span><span class="sxs-lookup"><span data-stu-id="43917-178">256</span></span>                                                          |
| <span data-ttu-id="43917-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-179">Search-Flags</span></span>           | <span data-ttu-id="43917-180">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="43917-180">0x0000000D</span></span>                                                   |
| <span data-ttu-id="43917-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-181">System-Flags</span></span>           | <span data-ttu-id="43917-182">0x00000012</span><span class="sxs-lookup"><span data-stu-id="43917-182">0x00000012</span></span>                                                   |
| <span data-ttu-id="43917-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43917-183">Classes used in</span></span>        | [<span data-ttu-id="43917-184">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="43917-184">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="43917-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="43917-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="43917-186">進入</span><span class="sxs-lookup"><span data-stu-id="43917-186">Entry</span></span> | <span data-ttu-id="43917-187">值</span><span class="sxs-lookup"><span data-stu-id="43917-187">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="43917-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43917-188">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43917-189">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="43917-190">System-Only</span></span>            | <span data-ttu-id="43917-191">否</span><span class="sxs-lookup"><span data-stu-id="43917-191">False</span></span>                                                        |
| <span data-ttu-id="43917-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43917-192">Is-Single-Valued</span></span>       | <span data-ttu-id="43917-193">對</span><span class="sxs-lookup"><span data-stu-id="43917-193">True</span></span>                                                         |
| <span data-ttu-id="43917-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43917-194">Is Indexed</span></span>             | <span data-ttu-id="43917-195">對</span><span class="sxs-lookup"><span data-stu-id="43917-195">True</span></span>                                                         |
| <span data-ttu-id="43917-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43917-196">In Global Catalog</span></span>      | <span data-ttu-id="43917-197">對</span><span class="sxs-lookup"><span data-stu-id="43917-197">True</span></span>                                                         |
| <span data-ttu-id="43917-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43917-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="43917-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43917-199">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="43917-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43917-200">Range-Lower</span></span>            | <span data-ttu-id="43917-201">0</span><span class="sxs-lookup"><span data-stu-id="43917-201">0</span></span>                                                            |
| <span data-ttu-id="43917-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43917-202">Range-Upper</span></span>            | <span data-ttu-id="43917-203">256</span><span class="sxs-lookup"><span data-stu-id="43917-203">256</span></span>                                                          |
| <span data-ttu-id="43917-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-204">Search-Flags</span></span>           | <span data-ttu-id="43917-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="43917-205">0x0000000D</span></span>                                                   |
| <span data-ttu-id="43917-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-206">System-Flags</span></span>           | <span data-ttu-id="43917-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="43917-207">0x00000012</span></span>                                                   |
| <span data-ttu-id="43917-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43917-208">Classes used in</span></span>        | [<span data-ttu-id="43917-209">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="43917-209">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="43917-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43917-210">Windows Server 2008</span></span>



| <span data-ttu-id="43917-211">進入</span><span class="sxs-lookup"><span data-stu-id="43917-211">Entry</span></span> | <span data-ttu-id="43917-212">值</span><span class="sxs-lookup"><span data-stu-id="43917-212">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="43917-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43917-213">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43917-214">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="43917-215">System-Only</span></span>            | <span data-ttu-id="43917-216">否</span><span class="sxs-lookup"><span data-stu-id="43917-216">False</span></span>                                                        |
| <span data-ttu-id="43917-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43917-217">Is-Single-Valued</span></span>       | <span data-ttu-id="43917-218">對</span><span class="sxs-lookup"><span data-stu-id="43917-218">True</span></span>                                                         |
| <span data-ttu-id="43917-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43917-219">Is Indexed</span></span>             | <span data-ttu-id="43917-220">對</span><span class="sxs-lookup"><span data-stu-id="43917-220">True</span></span>                                                         |
| <span data-ttu-id="43917-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43917-221">In Global Catalog</span></span>      | <span data-ttu-id="43917-222">對</span><span class="sxs-lookup"><span data-stu-id="43917-222">True</span></span>                                                         |
| <span data-ttu-id="43917-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43917-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="43917-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43917-224">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="43917-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43917-225">Range-Lower</span></span>            | <span data-ttu-id="43917-226">0</span><span class="sxs-lookup"><span data-stu-id="43917-226">0</span></span>                                                            |
| <span data-ttu-id="43917-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43917-227">Range-Upper</span></span>            | <span data-ttu-id="43917-228">256</span><span class="sxs-lookup"><span data-stu-id="43917-228">256</span></span>                                                          |
| <span data-ttu-id="43917-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-229">Search-Flags</span></span>           | <span data-ttu-id="43917-230">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="43917-230">0x0000000D</span></span>                                                   |
| <span data-ttu-id="43917-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-231">System-Flags</span></span>           | <span data-ttu-id="43917-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="43917-232">0x00000012</span></span>                                                   |
| <span data-ttu-id="43917-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43917-233">Classes used in</span></span>        | [<span data-ttu-id="43917-234">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="43917-234">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="43917-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="43917-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="43917-236">進入</span><span class="sxs-lookup"><span data-stu-id="43917-236">Entry</span></span> | <span data-ttu-id="43917-237">值</span><span class="sxs-lookup"><span data-stu-id="43917-237">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="43917-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43917-238">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43917-239">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="43917-240">System-Only</span></span>            | <span data-ttu-id="43917-241">否</span><span class="sxs-lookup"><span data-stu-id="43917-241">False</span></span>                                                        |
| <span data-ttu-id="43917-242">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43917-242">Is-Single-Valued</span></span>       | <span data-ttu-id="43917-243">對</span><span class="sxs-lookup"><span data-stu-id="43917-243">True</span></span>                                                         |
| <span data-ttu-id="43917-244">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43917-244">Is Indexed</span></span>             | <span data-ttu-id="43917-245">對</span><span class="sxs-lookup"><span data-stu-id="43917-245">True</span></span>                                                         |
| <span data-ttu-id="43917-246">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43917-246">In Global Catalog</span></span>      | <span data-ttu-id="43917-247">對</span><span class="sxs-lookup"><span data-stu-id="43917-247">True</span></span>                                                         |
| <span data-ttu-id="43917-248">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43917-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="43917-249">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43917-249">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="43917-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43917-250">Range-Lower</span></span>            | <span data-ttu-id="43917-251">0</span><span class="sxs-lookup"><span data-stu-id="43917-251">0</span></span>                                                            |
| <span data-ttu-id="43917-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43917-252">Range-Upper</span></span>            | <span data-ttu-id="43917-253">256</span><span class="sxs-lookup"><span data-stu-id="43917-253">256</span></span>                                                          |
| <span data-ttu-id="43917-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-254">Search-Flags</span></span>           | <span data-ttu-id="43917-255">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="43917-255">0x0000000D</span></span>                                                   |
| <span data-ttu-id="43917-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-256">System-Flags</span></span>           | <span data-ttu-id="43917-257">0x00000012</span><span class="sxs-lookup"><span data-stu-id="43917-257">0x00000012</span></span>                                                   |
| <span data-ttu-id="43917-258">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43917-258">Classes used in</span></span>        | [<span data-ttu-id="43917-259">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="43917-259">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="43917-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="43917-260">Windows Server 2012</span></span>



| <span data-ttu-id="43917-261">進入</span><span class="sxs-lookup"><span data-stu-id="43917-261">Entry</span></span> | <span data-ttu-id="43917-262">值</span><span class="sxs-lookup"><span data-stu-id="43917-262">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="43917-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43917-263">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43917-264">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="43917-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="43917-265">System-Only</span></span>            | <span data-ttu-id="43917-266">否</span><span class="sxs-lookup"><span data-stu-id="43917-266">False</span></span>                                                        |
| <span data-ttu-id="43917-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43917-267">Is-Single-Valued</span></span>       | <span data-ttu-id="43917-268">對</span><span class="sxs-lookup"><span data-stu-id="43917-268">True</span></span>                                                         |
| <span data-ttu-id="43917-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43917-269">Is Indexed</span></span>             | <span data-ttu-id="43917-270">對</span><span class="sxs-lookup"><span data-stu-id="43917-270">True</span></span>                                                         |
| <span data-ttu-id="43917-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43917-271">In Global Catalog</span></span>      | <span data-ttu-id="43917-272">對</span><span class="sxs-lookup"><span data-stu-id="43917-272">True</span></span>                                                         |
| <span data-ttu-id="43917-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43917-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="43917-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43917-274">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="43917-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43917-275">Range-Lower</span></span>            | <span data-ttu-id="43917-276">0</span><span class="sxs-lookup"><span data-stu-id="43917-276">0</span></span>                                                            |
| <span data-ttu-id="43917-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43917-277">Range-Upper</span></span>            | <span data-ttu-id="43917-278">256</span><span class="sxs-lookup"><span data-stu-id="43917-278">256</span></span>                                                          |
| <span data-ttu-id="43917-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-279">Search-Flags</span></span>           | <span data-ttu-id="43917-280">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="43917-280">0x0000000D</span></span>                                                   |
| <span data-ttu-id="43917-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43917-281">System-Flags</span></span>           | <span data-ttu-id="43917-282">0x00000012</span><span class="sxs-lookup"><span data-stu-id="43917-282">0x00000012</span></span>                                                   |
| <span data-ttu-id="43917-283">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43917-283">Classes used in</span></span>        | [<span data-ttu-id="43917-284">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="43917-284">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





