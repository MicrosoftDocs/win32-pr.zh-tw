---
title: Security-Identifier 屬性
description: 變數長度的唯一值，用來識別套用 ACE 的使用者帳戶、群組帳戶或登入會話。
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Security-Identifier 屬性 AD 架構
- securityIdentifier 屬性 AD 架構
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686943"
---
# <a name="security-identifier-attribute"></a><span data-ttu-id="321c7-105">Security-Identifier 屬性</span><span class="sxs-lookup"><span data-stu-id="321c7-105">Security-Identifier attribute</span></span>

<span data-ttu-id="321c7-106">變數長度的唯一值，用來識別套用 ACE 的使用者帳戶、群組帳戶或登入會話。</span><span class="sxs-lookup"><span data-stu-id="321c7-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="321c7-107">進入</span><span class="sxs-lookup"><span data-stu-id="321c7-107">Entry</span></span> | <span data-ttu-id="321c7-108">值</span><span class="sxs-lookup"><span data-stu-id="321c7-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="321c7-109">CN</span><span class="sxs-lookup"><span data-stu-id="321c7-109">CN</span></span>                | <span data-ttu-id="321c7-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="321c7-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="321c7-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="321c7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="321c7-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="321c7-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="321c7-113">大小</span><span class="sxs-lookup"><span data-stu-id="321c7-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="321c7-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="321c7-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="321c7-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="321c7-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="321c7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="321c7-116">Attribute-Id</span></span>      | <span data-ttu-id="321c7-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="321c7-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="321c7-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="321c7-118">System-Id-Guid</span></span>    | <span data-ttu-id="321c7-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="321c7-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="321c7-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="321c7-120">Syntax</span></span>            | [<span data-ttu-id="321c7-121">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="321c7-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="321c7-122">實作</span><span class="sxs-lookup"><span data-stu-id="321c7-122">Implementations</span></span>

-   [<span data-ttu-id="321c7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="321c7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="321c7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="321c7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="321c7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="321c7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="321c7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="321c7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="321c7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="321c7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="321c7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="321c7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="321c7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="321c7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="321c7-130">進入</span><span class="sxs-lookup"><span data-stu-id="321c7-130">Entry</span></span> | <span data-ttu-id="321c7-131">值</span><span class="sxs-lookup"><span data-stu-id="321c7-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321c7-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="321c7-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="321c7-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="321c7-134">System-Only</span></span>            | <span data-ttu-id="321c7-135">否</span><span class="sxs-lookup"><span data-stu-id="321c7-135">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="321c7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="321c7-137">對</span><span class="sxs-lookup"><span data-stu-id="321c7-137">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="321c7-138">Is Indexed</span></span>             | <span data-ttu-id="321c7-139">否</span><span class="sxs-lookup"><span data-stu-id="321c7-139">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="321c7-140">In Global Catalog</span></span>      | <span data-ttu-id="321c7-141">否</span><span class="sxs-lookup"><span data-stu-id="321c7-141">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="321c7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="321c7-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="321c7-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="321c7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="321c7-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="321c7-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-146">Search-Flags</span></span>           | <span data-ttu-id="321c7-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="321c7-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="321c7-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-148">System-Flags</span></span>           | <span data-ttu-id="321c7-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="321c7-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="321c7-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="321c7-150">Classes used in</span></span>        | [<span data-ttu-id="321c7-151">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="321c7-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="321c7-152">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="321c7-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="321c7-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="321c7-153">Windows Server 2003</span></span>



| <span data-ttu-id="321c7-154">進入</span><span class="sxs-lookup"><span data-stu-id="321c7-154">Entry</span></span> | <span data-ttu-id="321c7-155">值</span><span class="sxs-lookup"><span data-stu-id="321c7-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321c7-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="321c7-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="321c7-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="321c7-158">System-Only</span></span>            | <span data-ttu-id="321c7-159">否</span><span class="sxs-lookup"><span data-stu-id="321c7-159">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="321c7-160">Is-Single-Valued</span></span>       | <span data-ttu-id="321c7-161">對</span><span class="sxs-lookup"><span data-stu-id="321c7-161">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="321c7-162">Is Indexed</span></span>             | <span data-ttu-id="321c7-163">否</span><span class="sxs-lookup"><span data-stu-id="321c7-163">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="321c7-164">In Global Catalog</span></span>      | <span data-ttu-id="321c7-165">對</span><span class="sxs-lookup"><span data-stu-id="321c7-165">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="321c7-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="321c7-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="321c7-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="321c7-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="321c7-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="321c7-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-170">Search-Flags</span></span>           | <span data-ttu-id="321c7-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="321c7-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="321c7-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-172">System-Flags</span></span>           | <span data-ttu-id="321c7-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="321c7-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="321c7-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="321c7-174">Classes used in</span></span>        | [<span data-ttu-id="321c7-175">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="321c7-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="321c7-176">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="321c7-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="321c7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="321c7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="321c7-178">進入</span><span class="sxs-lookup"><span data-stu-id="321c7-178">Entry</span></span> | <span data-ttu-id="321c7-179">值</span><span class="sxs-lookup"><span data-stu-id="321c7-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321c7-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="321c7-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="321c7-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="321c7-182">System-Only</span></span>            | <span data-ttu-id="321c7-183">否</span><span class="sxs-lookup"><span data-stu-id="321c7-183">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="321c7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="321c7-185">對</span><span class="sxs-lookup"><span data-stu-id="321c7-185">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="321c7-186">Is Indexed</span></span>             | <span data-ttu-id="321c7-187">否</span><span class="sxs-lookup"><span data-stu-id="321c7-187">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="321c7-188">In Global Catalog</span></span>      | <span data-ttu-id="321c7-189">對</span><span class="sxs-lookup"><span data-stu-id="321c7-189">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="321c7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="321c7-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="321c7-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="321c7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="321c7-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="321c7-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-194">Search-Flags</span></span>           | <span data-ttu-id="321c7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="321c7-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="321c7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-196">System-Flags</span></span>           | <span data-ttu-id="321c7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="321c7-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="321c7-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="321c7-198">Classes used in</span></span>        | [<span data-ttu-id="321c7-199">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="321c7-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="321c7-200">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="321c7-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="321c7-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="321c7-201">Windows Server 2008</span></span>



| <span data-ttu-id="321c7-202">進入</span><span class="sxs-lookup"><span data-stu-id="321c7-202">Entry</span></span> | <span data-ttu-id="321c7-203">值</span><span class="sxs-lookup"><span data-stu-id="321c7-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321c7-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="321c7-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="321c7-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="321c7-206">System-Only</span></span>            | <span data-ttu-id="321c7-207">否</span><span class="sxs-lookup"><span data-stu-id="321c7-207">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="321c7-208">Is-Single-Valued</span></span>       | <span data-ttu-id="321c7-209">對</span><span class="sxs-lookup"><span data-stu-id="321c7-209">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="321c7-210">Is Indexed</span></span>             | <span data-ttu-id="321c7-211">否</span><span class="sxs-lookup"><span data-stu-id="321c7-211">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="321c7-212">In Global Catalog</span></span>      | <span data-ttu-id="321c7-213">對</span><span class="sxs-lookup"><span data-stu-id="321c7-213">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="321c7-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="321c7-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="321c7-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="321c7-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="321c7-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="321c7-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-218">Search-Flags</span></span>           | <span data-ttu-id="321c7-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="321c7-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="321c7-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-220">System-Flags</span></span>           | <span data-ttu-id="321c7-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="321c7-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="321c7-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="321c7-222">Classes used in</span></span>        | [<span data-ttu-id="321c7-223">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="321c7-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="321c7-224">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="321c7-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="321c7-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="321c7-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="321c7-226">進入</span><span class="sxs-lookup"><span data-stu-id="321c7-226">Entry</span></span> | <span data-ttu-id="321c7-227">值</span><span class="sxs-lookup"><span data-stu-id="321c7-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321c7-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="321c7-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="321c7-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="321c7-230">System-Only</span></span>            | <span data-ttu-id="321c7-231">否</span><span class="sxs-lookup"><span data-stu-id="321c7-231">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="321c7-232">Is-Single-Valued</span></span>       | <span data-ttu-id="321c7-233">對</span><span class="sxs-lookup"><span data-stu-id="321c7-233">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="321c7-234">Is Indexed</span></span>             | <span data-ttu-id="321c7-235">否</span><span class="sxs-lookup"><span data-stu-id="321c7-235">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="321c7-236">In Global Catalog</span></span>      | <span data-ttu-id="321c7-237">對</span><span class="sxs-lookup"><span data-stu-id="321c7-237">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="321c7-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="321c7-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="321c7-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="321c7-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="321c7-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="321c7-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-242">Search-Flags</span></span>           | <span data-ttu-id="321c7-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="321c7-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="321c7-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-244">System-Flags</span></span>           | <span data-ttu-id="321c7-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="321c7-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="321c7-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="321c7-246">Classes used in</span></span>        | [<span data-ttu-id="321c7-247">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="321c7-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="321c7-248">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="321c7-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="321c7-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="321c7-249">Windows Server 2012</span></span>



| <span data-ttu-id="321c7-250">進入</span><span class="sxs-lookup"><span data-stu-id="321c7-250">Entry</span></span> | <span data-ttu-id="321c7-251">值</span><span class="sxs-lookup"><span data-stu-id="321c7-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321c7-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="321c7-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="321c7-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="321c7-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="321c7-254">System-Only</span></span>            | <span data-ttu-id="321c7-255">否</span><span class="sxs-lookup"><span data-stu-id="321c7-255">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="321c7-256">Is-Single-Valued</span></span>       | <span data-ttu-id="321c7-257">對</span><span class="sxs-lookup"><span data-stu-id="321c7-257">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="321c7-258">Is Indexed</span></span>             | <span data-ttu-id="321c7-259">否</span><span class="sxs-lookup"><span data-stu-id="321c7-259">False</span></span>                                                                                                             |
| <span data-ttu-id="321c7-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="321c7-260">In Global Catalog</span></span>      | <span data-ttu-id="321c7-261">對</span><span class="sxs-lookup"><span data-stu-id="321c7-261">True</span></span>                                                                                                              |
| <span data-ttu-id="321c7-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="321c7-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="321c7-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="321c7-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="321c7-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="321c7-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="321c7-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="321c7-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-266">Search-Flags</span></span>           | <span data-ttu-id="321c7-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="321c7-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="321c7-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="321c7-268">System-Flags</span></span>           | <span data-ttu-id="321c7-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="321c7-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="321c7-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="321c7-270">Classes used in</span></span>        | [<span data-ttu-id="321c7-271">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="321c7-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="321c7-272">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="321c7-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





