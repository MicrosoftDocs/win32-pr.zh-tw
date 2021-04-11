---
title: SAM-Account-Type 屬性
description: 此屬性包含每個帳戶類型物件的相關資訊。
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- SAM-帳戶-類型屬性 AD 架構
- sAMAccountType 屬性 AD 架構
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935352"
---
# <a name="sam-account-type-attribute"></a><span data-ttu-id="909f4-105">SAM-Account-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="909f4-105">SAM-Account-Type attribute</span></span>

<span data-ttu-id="909f4-106">此屬性包含每個帳戶類型物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="909f4-106">This attribute contains information about every account type object.</span></span> <span data-ttu-id="909f4-107">您可以列舉帳戶類型清單，也可以使用顯示資訊 API 來建立清單。</span><span class="sxs-lookup"><span data-stu-id="909f4-107">You can enumerate a list of account types or you can use the Display Information API to create a list.</span></span> <span data-ttu-id="909f4-108">因為電腦、一般使用者帳戶和信任帳戶也可以列舉為使用者物件，所以這些帳戶的值必須是連續的範圍。</span><span class="sxs-lookup"><span data-stu-id="909f4-108">Because computers, normal user accounts, and trust accounts can also be enumerated as user objects, the values for these accounts must be a contiguous range.</span></span>

<span data-ttu-id="909f4-109">這個屬性的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="909f4-109">The possible values for this attribute are the following:</span></span>

-   <span data-ttu-id="909f4-110">SAM \_ 網域 \_ 物件0x0</span><span class="sxs-lookup"><span data-stu-id="909f4-110">SAM\_DOMAIN\_OBJECT 0x0</span></span>
-   <span data-ttu-id="909f4-111">SAM \_ 群組 \_ 物件0x10000000</span><span class="sxs-lookup"><span data-stu-id="909f4-111">SAM\_GROUP\_OBJECT 0x10000000</span></span>
-   <span data-ttu-id="909f4-112">SAM \_ 非 \_ 安全 \_ 組 \_ 物件0x10000001</span><span class="sxs-lookup"><span data-stu-id="909f4-112">SAM\_NON\_SECURITY\_GROUP\_OBJECT 0x10000001</span></span>
-   <span data-ttu-id="909f4-113">SAM \_ 別名 \_ 物件0x20000000</span><span class="sxs-lookup"><span data-stu-id="909f4-113">SAM\_ALIAS\_OBJECT 0x20000000</span></span>
-   <span data-ttu-id="909f4-114">SAM \_ 非 \_ 安全性 \_ 別名 \_ 物件0x20000001</span><span class="sxs-lookup"><span data-stu-id="909f4-114">SAM\_NON\_SECURITY\_ALIAS\_OBJECT 0x20000001</span></span>
-   <span data-ttu-id="909f4-115">SAM \_ 使用者 \_ 物件0x30000000</span><span class="sxs-lookup"><span data-stu-id="909f4-115">SAM\_USER\_OBJECT 0x30000000</span></span>
-   <span data-ttu-id="909f4-116">SAM \_ 一般 \_ 使用者 \_ 帳戶0x30000000</span><span class="sxs-lookup"><span data-stu-id="909f4-116">SAM\_NORMAL\_USER\_ACCOUNT 0x30000000</span></span>
-   <span data-ttu-id="909f4-117">SAM \_ 電腦 \_ 帳戶0x30000001</span><span class="sxs-lookup"><span data-stu-id="909f4-117">SAM\_MACHINE\_ACCOUNT 0x30000001</span></span>
-   <span data-ttu-id="909f4-118">SAM \_ 信任 \_ 帳戶0x30000002</span><span class="sxs-lookup"><span data-stu-id="909f4-118">SAM\_TRUST\_ACCOUNT 0x30000002</span></span>
-   <span data-ttu-id="909f4-119">SAM \_ 應用程式 \_ 基本 \_ 群組0x40000000</span><span class="sxs-lookup"><span data-stu-id="909f4-119">SAM\_APP\_BASIC\_GROUP 0x40000000</span></span>
-   <span data-ttu-id="909f4-120">SAM \_ 應用程式 \_ 查詢 \_ 群組0x40000001</span><span class="sxs-lookup"><span data-stu-id="909f4-120">SAM\_APP\_QUERY\_GROUP 0x40000001</span></span>
-   <span data-ttu-id="909f4-121">SAM \_ 帳戶 \_ 類型 \_ 最大的0x7fffffff</span><span class="sxs-lookup"><span data-stu-id="909f4-121">SAM\_ACCOUNT\_TYPE\_MAX 0x7fffffff</span></span>



| <span data-ttu-id="909f4-122">進入</span><span class="sxs-lookup"><span data-stu-id="909f4-122">Entry</span></span> | <span data-ttu-id="909f4-123">值</span><span class="sxs-lookup"><span data-stu-id="909f4-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="909f4-124">CN</span><span class="sxs-lookup"><span data-stu-id="909f4-124">CN</span></span>                | <span data-ttu-id="909f4-125">SAM-帳戶-類型</span><span class="sxs-lookup"><span data-stu-id="909f4-125">SAM-Account-Type</span></span>                                                |
| <span data-ttu-id="909f4-126">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="909f4-126">Ldap-Display-Name</span></span> | <span data-ttu-id="909f4-127">sAMAccountType</span><span class="sxs-lookup"><span data-stu-id="909f4-127">sAMAccountType</span></span>                                                  |
| <span data-ttu-id="909f4-128">大小</span><span class="sxs-lookup"><span data-stu-id="909f4-128">Size</span></span>              | \-                                                              |
| <span data-ttu-id="909f4-129">更新許可權</span><span class="sxs-lookup"><span data-stu-id="909f4-129">Update Privilege</span></span>  | <span data-ttu-id="909f4-130">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="909f4-130">This value is set by the system.</span></span>                                |
| <span data-ttu-id="909f4-131">更新頻率</span><span class="sxs-lookup"><span data-stu-id="909f4-131">Update Frequency</span></span>  | <span data-ttu-id="909f4-132">這是在建立物件時由作業系統設定。</span><span class="sxs-lookup"><span data-stu-id="909f4-132">This is set by the operating system when the object is created.</span></span> |
| <span data-ttu-id="909f4-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-133">Attribute-Id</span></span>      | <span data-ttu-id="909f4-134">1.2.840.113556.1.4.302</span><span class="sxs-lookup"><span data-stu-id="909f4-134">1.2.840.113556.1.4.302</span></span>                                          |
| <span data-ttu-id="909f4-135">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="909f4-135">System-Id-Guid</span></span>    | <span data-ttu-id="909f4-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="909f4-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span></span>                            |
| <span data-ttu-id="909f4-137">Syntax</span><span class="sxs-lookup"><span data-stu-id="909f4-137">Syntax</span></span>            | [<span data-ttu-id="909f4-138">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="909f4-138">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="909f4-139">實作</span><span class="sxs-lookup"><span data-stu-id="909f4-139">Implementations</span></span>

-   [<span data-ttu-id="909f4-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="909f4-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="909f4-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="909f4-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="909f4-142">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="909f4-142">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="909f4-143">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="909f4-143">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="909f4-144">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="909f4-144">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="909f4-145">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="909f4-145">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="909f4-146">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="909f4-146">Windows 2000 Server</span></span>



| <span data-ttu-id="909f4-147">進入</span><span class="sxs-lookup"><span data-stu-id="909f4-147">Entry</span></span> | <span data-ttu-id="909f4-148">值</span><span class="sxs-lookup"><span data-stu-id="909f4-148">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="909f4-149">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="909f4-149">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-150">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-150">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-151">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-151">System-Only</span></span>            | <span data-ttu-id="909f4-152">否</span><span class="sxs-lookup"><span data-stu-id="909f4-152">False</span></span>                                                        |
| <span data-ttu-id="909f4-153">是-單一值</span><span class="sxs-lookup"><span data-stu-id="909f4-153">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-154">對</span><span class="sxs-lookup"><span data-stu-id="909f4-154">True</span></span>                                                         |
| <span data-ttu-id="909f4-155">已編制索引</span><span class="sxs-lookup"><span data-stu-id="909f4-155">Is Indexed</span></span>             | <span data-ttu-id="909f4-156">對</span><span class="sxs-lookup"><span data-stu-id="909f4-156">True</span></span>                                                         |
| <span data-ttu-id="909f4-157">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="909f4-157">In Global Catalog</span></span>      | <span data-ttu-id="909f4-158">對</span><span class="sxs-lookup"><span data-stu-id="909f4-158">True</span></span>                                                         |
| <span data-ttu-id="909f4-159">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="909f4-159">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-160">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="909f4-160">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="909f4-161">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-161">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-162">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-162">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-163">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-163">Search-Flags</span></span>           | <span data-ttu-id="909f4-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="909f4-164">0x00000001</span></span>                                                   |
| <span data-ttu-id="909f4-165">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-165">System-Flags</span></span>           | <span data-ttu-id="909f4-166">0x00000012</span><span class="sxs-lookup"><span data-stu-id="909f4-166">0x00000012</span></span>                                                   |
| <span data-ttu-id="909f4-167">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="909f4-167">Classes used in</span></span>        | [<span data-ttu-id="909f4-168">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="909f4-168">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="909f4-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="909f4-169">Windows Server 2003</span></span>



| <span data-ttu-id="909f4-170">進入</span><span class="sxs-lookup"><span data-stu-id="909f4-170">Entry</span></span> | <span data-ttu-id="909f4-171">值</span><span class="sxs-lookup"><span data-stu-id="909f4-171">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="909f4-172">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="909f4-172">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-173">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-173">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-174">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-174">System-Only</span></span>            | <span data-ttu-id="909f4-175">否</span><span class="sxs-lookup"><span data-stu-id="909f4-175">False</span></span>                                                        |
| <span data-ttu-id="909f4-176">是-單一值</span><span class="sxs-lookup"><span data-stu-id="909f4-176">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-177">對</span><span class="sxs-lookup"><span data-stu-id="909f4-177">True</span></span>                                                         |
| <span data-ttu-id="909f4-178">已編制索引</span><span class="sxs-lookup"><span data-stu-id="909f4-178">Is Indexed</span></span>             | <span data-ttu-id="909f4-179">對</span><span class="sxs-lookup"><span data-stu-id="909f4-179">True</span></span>                                                         |
| <span data-ttu-id="909f4-180">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="909f4-180">In Global Catalog</span></span>      | <span data-ttu-id="909f4-181">對</span><span class="sxs-lookup"><span data-stu-id="909f4-181">True</span></span>                                                         |
| <span data-ttu-id="909f4-182">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="909f4-182">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-183">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="909f4-183">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="909f4-184">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-184">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-185">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-185">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-186">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-186">Search-Flags</span></span>           | <span data-ttu-id="909f4-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="909f4-187">0x00000001</span></span>                                                   |
| <span data-ttu-id="909f4-188">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-188">System-Flags</span></span>           | <span data-ttu-id="909f4-189">0x00000012</span><span class="sxs-lookup"><span data-stu-id="909f4-189">0x00000012</span></span>                                                   |
| <span data-ttu-id="909f4-190">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="909f4-190">Classes used in</span></span>        | [<span data-ttu-id="909f4-191">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="909f4-191">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="909f4-192">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="909f4-192">Windows Server 2003 R2</span></span>



| <span data-ttu-id="909f4-193">進入</span><span class="sxs-lookup"><span data-stu-id="909f4-193">Entry</span></span> | <span data-ttu-id="909f4-194">值</span><span class="sxs-lookup"><span data-stu-id="909f4-194">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="909f4-195">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="909f4-195">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-196">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-196">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-197">System-Only</span></span>            | <span data-ttu-id="909f4-198">否</span><span class="sxs-lookup"><span data-stu-id="909f4-198">False</span></span>                                                        |
| <span data-ttu-id="909f4-199">是-單一值</span><span class="sxs-lookup"><span data-stu-id="909f4-199">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-200">對</span><span class="sxs-lookup"><span data-stu-id="909f4-200">True</span></span>                                                         |
| <span data-ttu-id="909f4-201">已編制索引</span><span class="sxs-lookup"><span data-stu-id="909f4-201">Is Indexed</span></span>             | <span data-ttu-id="909f4-202">對</span><span class="sxs-lookup"><span data-stu-id="909f4-202">True</span></span>                                                         |
| <span data-ttu-id="909f4-203">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="909f4-203">In Global Catalog</span></span>      | <span data-ttu-id="909f4-204">對</span><span class="sxs-lookup"><span data-stu-id="909f4-204">True</span></span>                                                         |
| <span data-ttu-id="909f4-205">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="909f4-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-206">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="909f4-206">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="909f4-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-207">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-208">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-208">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-209">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-209">Search-Flags</span></span>           | <span data-ttu-id="909f4-210">0x00000001</span><span class="sxs-lookup"><span data-stu-id="909f4-210">0x00000001</span></span>                                                   |
| <span data-ttu-id="909f4-211">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-211">System-Flags</span></span>           | <span data-ttu-id="909f4-212">0x00000012</span><span class="sxs-lookup"><span data-stu-id="909f4-212">0x00000012</span></span>                                                   |
| <span data-ttu-id="909f4-213">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="909f4-213">Classes used in</span></span>        | [<span data-ttu-id="909f4-214">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="909f4-214">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="909f4-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="909f4-215">Windows Server 2008</span></span>



| <span data-ttu-id="909f4-216">進入</span><span class="sxs-lookup"><span data-stu-id="909f4-216">Entry</span></span> | <span data-ttu-id="909f4-217">值</span><span class="sxs-lookup"><span data-stu-id="909f4-217">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="909f4-218">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="909f4-218">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-219">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-219">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-220">System-Only</span></span>            | <span data-ttu-id="909f4-221">否</span><span class="sxs-lookup"><span data-stu-id="909f4-221">False</span></span>                                                        |
| <span data-ttu-id="909f4-222">是-單一值</span><span class="sxs-lookup"><span data-stu-id="909f4-222">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-223">對</span><span class="sxs-lookup"><span data-stu-id="909f4-223">True</span></span>                                                         |
| <span data-ttu-id="909f4-224">已編制索引</span><span class="sxs-lookup"><span data-stu-id="909f4-224">Is Indexed</span></span>             | <span data-ttu-id="909f4-225">對</span><span class="sxs-lookup"><span data-stu-id="909f4-225">True</span></span>                                                         |
| <span data-ttu-id="909f4-226">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="909f4-226">In Global Catalog</span></span>      | <span data-ttu-id="909f4-227">對</span><span class="sxs-lookup"><span data-stu-id="909f4-227">True</span></span>                                                         |
| <span data-ttu-id="909f4-228">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="909f4-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-229">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="909f4-229">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="909f4-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-230">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-231">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-232">Search-Flags</span></span>           | <span data-ttu-id="909f4-233">0x00000001</span><span class="sxs-lookup"><span data-stu-id="909f4-233">0x00000001</span></span>                                                   |
| <span data-ttu-id="909f4-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-234">System-Flags</span></span>           | <span data-ttu-id="909f4-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="909f4-235">0x00000012</span></span>                                                   |
| <span data-ttu-id="909f4-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="909f4-236">Classes used in</span></span>        | [<span data-ttu-id="909f4-237">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="909f4-237">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="909f4-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="909f4-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="909f4-239">進入</span><span class="sxs-lookup"><span data-stu-id="909f4-239">Entry</span></span> | <span data-ttu-id="909f4-240">值</span><span class="sxs-lookup"><span data-stu-id="909f4-240">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="909f4-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="909f4-241">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-242">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-243">System-Only</span></span>            | <span data-ttu-id="909f4-244">否</span><span class="sxs-lookup"><span data-stu-id="909f4-244">False</span></span>                                                        |
| <span data-ttu-id="909f4-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="909f4-245">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-246">對</span><span class="sxs-lookup"><span data-stu-id="909f4-246">True</span></span>                                                         |
| <span data-ttu-id="909f4-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="909f4-247">Is Indexed</span></span>             | <span data-ttu-id="909f4-248">對</span><span class="sxs-lookup"><span data-stu-id="909f4-248">True</span></span>                                                         |
| <span data-ttu-id="909f4-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="909f4-249">In Global Catalog</span></span>      | <span data-ttu-id="909f4-250">對</span><span class="sxs-lookup"><span data-stu-id="909f4-250">True</span></span>                                                         |
| <span data-ttu-id="909f4-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="909f4-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="909f4-252">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="909f4-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-253">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-254">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-255">Search-Flags</span></span>           | <span data-ttu-id="909f4-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="909f4-256">0x00000001</span></span>                                                   |
| <span data-ttu-id="909f4-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-257">System-Flags</span></span>           | <span data-ttu-id="909f4-258">0x00000012</span><span class="sxs-lookup"><span data-stu-id="909f4-258">0x00000012</span></span>                                                   |
| <span data-ttu-id="909f4-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="909f4-259">Classes used in</span></span>        | [<span data-ttu-id="909f4-260">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="909f4-260">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="909f4-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="909f4-261">Windows Server 2012</span></span>



| <span data-ttu-id="909f4-262">進入</span><span class="sxs-lookup"><span data-stu-id="909f4-262">Entry</span></span> | <span data-ttu-id="909f4-263">值</span><span class="sxs-lookup"><span data-stu-id="909f4-263">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="909f4-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="909f4-264">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-265">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="909f4-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-266">System-Only</span></span>            | <span data-ttu-id="909f4-267">否</span><span class="sxs-lookup"><span data-stu-id="909f4-267">False</span></span>                                                        |
| <span data-ttu-id="909f4-268">是-單一值</span><span class="sxs-lookup"><span data-stu-id="909f4-268">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-269">對</span><span class="sxs-lookup"><span data-stu-id="909f4-269">True</span></span>                                                         |
| <span data-ttu-id="909f4-270">已編制索引</span><span class="sxs-lookup"><span data-stu-id="909f4-270">Is Indexed</span></span>             | <span data-ttu-id="909f4-271">對</span><span class="sxs-lookup"><span data-stu-id="909f4-271">True</span></span>                                                         |
| <span data-ttu-id="909f4-272">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="909f4-272">In Global Catalog</span></span>      | <span data-ttu-id="909f4-273">對</span><span class="sxs-lookup"><span data-stu-id="909f4-273">True</span></span>                                                         |
| <span data-ttu-id="909f4-274">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="909f4-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-275">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="909f4-275">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="909f4-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-276">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-277">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="909f4-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-278">Search-Flags</span></span>           | <span data-ttu-id="909f4-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="909f4-279">0x00000001</span></span>                                                   |
| <span data-ttu-id="909f4-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-280">System-Flags</span></span>           | <span data-ttu-id="909f4-281">0x00000012</span><span class="sxs-lookup"><span data-stu-id="909f4-281">0x00000012</span></span>                                                   |
| <span data-ttu-id="909f4-282">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="909f4-282">Classes used in</span></span>        | [<span data-ttu-id="909f4-283">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="909f4-283">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





