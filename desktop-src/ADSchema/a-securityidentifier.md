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
# <a name="security-identifier-attribute"></a><span data-ttu-id="3c937-105">Security-Identifier 屬性</span><span class="sxs-lookup"><span data-stu-id="3c937-105">Security-Identifier attribute</span></span>

<span data-ttu-id="3c937-106">變數長度的唯一值，用來識別套用 ACE 的使用者帳戶、群組帳戶或登入會話。</span><span class="sxs-lookup"><span data-stu-id="3c937-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="3c937-107">進入</span><span class="sxs-lookup"><span data-stu-id="3c937-107">Entry</span></span> | <span data-ttu-id="3c937-108">值</span><span class="sxs-lookup"><span data-stu-id="3c937-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3c937-109">CN</span><span class="sxs-lookup"><span data-stu-id="3c937-109">CN</span></span>                | <span data-ttu-id="3c937-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="3c937-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="3c937-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3c937-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3c937-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="3c937-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="3c937-113">大小</span><span class="sxs-lookup"><span data-stu-id="3c937-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="3c937-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3c937-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3c937-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3c937-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3c937-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3c937-116">Attribute-Id</span></span>      | <span data-ttu-id="3c937-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="3c937-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="3c937-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3c937-118">System-Id-Guid</span></span>    | <span data-ttu-id="3c937-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3c937-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="3c937-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c937-120">Syntax</span></span>            | [<span data-ttu-id="3c937-121">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="3c937-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="3c937-122">實作</span><span class="sxs-lookup"><span data-stu-id="3c937-122">Implementations</span></span>

-   [<span data-ttu-id="3c937-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3c937-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3c937-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3c937-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3c937-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3c937-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3c937-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3c937-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3c937-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3c937-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3c937-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3c937-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3c937-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c937-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3c937-130">進入</span><span class="sxs-lookup"><span data-stu-id="3c937-130">Entry</span></span> | <span data-ttu-id="3c937-131">值</span><span class="sxs-lookup"><span data-stu-id="3c937-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c937-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3c937-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c937-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c937-134">System-Only</span></span>            | <span data-ttu-id="3c937-135">否</span><span class="sxs-lookup"><span data-stu-id="3c937-135">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3c937-136">Is-Single-Valued</span></span>       | <span data-ttu-id="3c937-137">對</span><span class="sxs-lookup"><span data-stu-id="3c937-137">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3c937-138">Is Indexed</span></span>             | <span data-ttu-id="3c937-139">否</span><span class="sxs-lookup"><span data-stu-id="3c937-139">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3c937-140">In Global Catalog</span></span>      | <span data-ttu-id="3c937-141">否</span><span class="sxs-lookup"><span data-stu-id="3c937-141">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3c937-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c937-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3c937-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="3c937-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c937-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c937-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-146">Search-Flags</span></span>           | <span data-ttu-id="3c937-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c937-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="3c937-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-148">System-Flags</span></span>           | <span data-ttu-id="3c937-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c937-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="3c937-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3c937-150">Classes used in</span></span>        | [<span data-ttu-id="3c937-151">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="3c937-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="3c937-152">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="3c937-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3c937-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c937-153">Windows Server 2003</span></span>



| <span data-ttu-id="3c937-154">進入</span><span class="sxs-lookup"><span data-stu-id="3c937-154">Entry</span></span> | <span data-ttu-id="3c937-155">值</span><span class="sxs-lookup"><span data-stu-id="3c937-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c937-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3c937-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c937-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c937-158">System-Only</span></span>            | <span data-ttu-id="3c937-159">否</span><span class="sxs-lookup"><span data-stu-id="3c937-159">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3c937-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3c937-161">對</span><span class="sxs-lookup"><span data-stu-id="3c937-161">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3c937-162">Is Indexed</span></span>             | <span data-ttu-id="3c937-163">否</span><span class="sxs-lookup"><span data-stu-id="3c937-163">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3c937-164">In Global Catalog</span></span>      | <span data-ttu-id="3c937-165">對</span><span class="sxs-lookup"><span data-stu-id="3c937-165">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3c937-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c937-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3c937-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="3c937-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c937-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c937-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-170">Search-Flags</span></span>           | <span data-ttu-id="3c937-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c937-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="3c937-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-172">System-Flags</span></span>           | <span data-ttu-id="3c937-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c937-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="3c937-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3c937-174">Classes used in</span></span>        | [<span data-ttu-id="3c937-175">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="3c937-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="3c937-176">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="3c937-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3c937-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3c937-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3c937-178">進入</span><span class="sxs-lookup"><span data-stu-id="3c937-178">Entry</span></span> | <span data-ttu-id="3c937-179">值</span><span class="sxs-lookup"><span data-stu-id="3c937-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c937-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3c937-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c937-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c937-182">System-Only</span></span>            | <span data-ttu-id="3c937-183">否</span><span class="sxs-lookup"><span data-stu-id="3c937-183">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3c937-184">Is-Single-Valued</span></span>       | <span data-ttu-id="3c937-185">對</span><span class="sxs-lookup"><span data-stu-id="3c937-185">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3c937-186">Is Indexed</span></span>             | <span data-ttu-id="3c937-187">否</span><span class="sxs-lookup"><span data-stu-id="3c937-187">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3c937-188">In Global Catalog</span></span>      | <span data-ttu-id="3c937-189">對</span><span class="sxs-lookup"><span data-stu-id="3c937-189">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3c937-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c937-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3c937-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="3c937-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c937-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c937-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-194">Search-Flags</span></span>           | <span data-ttu-id="3c937-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c937-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="3c937-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-196">System-Flags</span></span>           | <span data-ttu-id="3c937-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c937-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="3c937-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3c937-198">Classes used in</span></span>        | [<span data-ttu-id="3c937-199">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="3c937-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="3c937-200">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="3c937-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3c937-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c937-201">Windows Server 2008</span></span>



| <span data-ttu-id="3c937-202">進入</span><span class="sxs-lookup"><span data-stu-id="3c937-202">Entry</span></span> | <span data-ttu-id="3c937-203">值</span><span class="sxs-lookup"><span data-stu-id="3c937-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c937-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3c937-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c937-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c937-206">System-Only</span></span>            | <span data-ttu-id="3c937-207">否</span><span class="sxs-lookup"><span data-stu-id="3c937-207">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3c937-208">Is-Single-Valued</span></span>       | <span data-ttu-id="3c937-209">對</span><span class="sxs-lookup"><span data-stu-id="3c937-209">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3c937-210">Is Indexed</span></span>             | <span data-ttu-id="3c937-211">否</span><span class="sxs-lookup"><span data-stu-id="3c937-211">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3c937-212">In Global Catalog</span></span>      | <span data-ttu-id="3c937-213">對</span><span class="sxs-lookup"><span data-stu-id="3c937-213">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3c937-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c937-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3c937-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="3c937-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c937-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c937-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-218">Search-Flags</span></span>           | <span data-ttu-id="3c937-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c937-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="3c937-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-220">System-Flags</span></span>           | <span data-ttu-id="3c937-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c937-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="3c937-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3c937-222">Classes used in</span></span>        | [<span data-ttu-id="3c937-223">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="3c937-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="3c937-224">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="3c937-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3c937-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c937-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3c937-226">進入</span><span class="sxs-lookup"><span data-stu-id="3c937-226">Entry</span></span> | <span data-ttu-id="3c937-227">值</span><span class="sxs-lookup"><span data-stu-id="3c937-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c937-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3c937-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c937-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c937-230">System-Only</span></span>            | <span data-ttu-id="3c937-231">否</span><span class="sxs-lookup"><span data-stu-id="3c937-231">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3c937-232">Is-Single-Valued</span></span>       | <span data-ttu-id="3c937-233">對</span><span class="sxs-lookup"><span data-stu-id="3c937-233">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3c937-234">Is Indexed</span></span>             | <span data-ttu-id="3c937-235">否</span><span class="sxs-lookup"><span data-stu-id="3c937-235">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3c937-236">In Global Catalog</span></span>      | <span data-ttu-id="3c937-237">對</span><span class="sxs-lookup"><span data-stu-id="3c937-237">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3c937-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c937-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3c937-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="3c937-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c937-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c937-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-242">Search-Flags</span></span>           | <span data-ttu-id="3c937-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c937-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="3c937-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-244">System-Flags</span></span>           | <span data-ttu-id="3c937-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c937-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="3c937-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3c937-246">Classes used in</span></span>        | [<span data-ttu-id="3c937-247">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="3c937-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="3c937-248">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="3c937-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3c937-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c937-249">Windows Server 2012</span></span>



| <span data-ttu-id="3c937-250">進入</span><span class="sxs-lookup"><span data-stu-id="3c937-250">Entry</span></span> | <span data-ttu-id="3c937-251">值</span><span class="sxs-lookup"><span data-stu-id="3c937-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c937-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3c937-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c937-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="3c937-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c937-254">System-Only</span></span>            | <span data-ttu-id="3c937-255">否</span><span class="sxs-lookup"><span data-stu-id="3c937-255">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3c937-256">Is-Single-Valued</span></span>       | <span data-ttu-id="3c937-257">對</span><span class="sxs-lookup"><span data-stu-id="3c937-257">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3c937-258">Is Indexed</span></span>             | <span data-ttu-id="3c937-259">否</span><span class="sxs-lookup"><span data-stu-id="3c937-259">False</span></span>                                                                                                             |
| <span data-ttu-id="3c937-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3c937-260">In Global Catalog</span></span>      | <span data-ttu-id="3c937-261">對</span><span class="sxs-lookup"><span data-stu-id="3c937-261">True</span></span>                                                                                                              |
| <span data-ttu-id="3c937-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3c937-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c937-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3c937-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="3c937-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c937-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c937-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="3c937-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-266">Search-Flags</span></span>           | <span data-ttu-id="3c937-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c937-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="3c937-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c937-268">System-Flags</span></span>           | <span data-ttu-id="3c937-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c937-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="3c937-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3c937-270">Classes used in</span></span>        | [<span data-ttu-id="3c937-271">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="3c937-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="3c937-272">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="3c937-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





