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
# <a name="security-identifier-attribute"></a><span data-ttu-id="a31b0-105">Security-Identifier 屬性</span><span class="sxs-lookup"><span data-stu-id="a31b0-105">Security-Identifier attribute</span></span>

<span data-ttu-id="a31b0-106">變數長度的唯一值，用來識別套用 ACE 的使用者帳戶、群組帳戶或登入會話。</span><span class="sxs-lookup"><span data-stu-id="a31b0-106">A unique value of variable length used to identify a user account, group account, or logon session to which an ACE applies.</span></span>



| <span data-ttu-id="a31b0-107">進入</span><span class="sxs-lookup"><span data-stu-id="a31b0-107">Entry</span></span> | <span data-ttu-id="a31b0-108">值</span><span class="sxs-lookup"><span data-stu-id="a31b0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a31b0-109">CN</span><span class="sxs-lookup"><span data-stu-id="a31b0-109">CN</span></span>                | <span data-ttu-id="a31b0-110">Security-Identifier</span><span class="sxs-lookup"><span data-stu-id="a31b0-110">Security-Identifier</span></span>                  |
| <span data-ttu-id="a31b0-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a31b0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a31b0-112">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="a31b0-112">securityIdentifier</span></span>                   |
| <span data-ttu-id="a31b0-113">大小</span><span class="sxs-lookup"><span data-stu-id="a31b0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="a31b0-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a31b0-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a31b0-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a31b0-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a31b0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a31b0-116">Attribute-Id</span></span>      | <span data-ttu-id="a31b0-117">1.2.840.113556.1.4.121</span><span class="sxs-lookup"><span data-stu-id="a31b0-117">1.2.840.113556.1.4.121</span></span>               |
| <span data-ttu-id="a31b0-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a31b0-118">System-Id-Guid</span></span>    | <span data-ttu-id="a31b0-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a31b0-119">bf967a2f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a31b0-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a31b0-120">Syntax</span></span>            | [<span data-ttu-id="a31b0-121">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="a31b0-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="a31b0-122">實作</span><span class="sxs-lookup"><span data-stu-id="a31b0-122">Implementations</span></span>

-   [<span data-ttu-id="a31b0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a31b0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a31b0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a31b0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a31b0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a31b0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a31b0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a31b0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a31b0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a31b0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a31b0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a31b0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a31b0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a31b0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="a31b0-130">進入</span><span class="sxs-lookup"><span data-stu-id="a31b0-130">Entry</span></span> | <span data-ttu-id="a31b0-131">值</span><span class="sxs-lookup"><span data-stu-id="a31b0-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31b0-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a31b0-132">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a31b0-133">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a31b0-134">System-Only</span></span>            | <span data-ttu-id="a31b0-135">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-135">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a31b0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a31b0-137">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-137">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a31b0-138">Is Indexed</span></span>             | <span data-ttu-id="a31b0-139">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-139">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a31b0-140">In Global Catalog</span></span>      | <span data-ttu-id="a31b0-141">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-141">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a31b0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a31b0-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a31b0-143">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="a31b0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a31b0-144">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a31b0-145">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-146">Search-Flags</span></span>           | <span data-ttu-id="a31b0-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a31b0-147">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-148">System-Flags</span></span>           | <span data-ttu-id="a31b0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a31b0-149">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a31b0-150">Classes used in</span></span>        | [<span data-ttu-id="a31b0-151">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a31b0-151">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="a31b0-152">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a31b0-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a31b0-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a31b0-153">Windows Server 2003</span></span>



| <span data-ttu-id="a31b0-154">進入</span><span class="sxs-lookup"><span data-stu-id="a31b0-154">Entry</span></span> | <span data-ttu-id="a31b0-155">值</span><span class="sxs-lookup"><span data-stu-id="a31b0-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31b0-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a31b0-156">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a31b0-157">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a31b0-158">System-Only</span></span>            | <span data-ttu-id="a31b0-159">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-159">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a31b0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a31b0-161">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-161">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a31b0-162">Is Indexed</span></span>             | <span data-ttu-id="a31b0-163">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-163">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a31b0-164">In Global Catalog</span></span>      | <span data-ttu-id="a31b0-165">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-165">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a31b0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a31b0-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a31b0-167">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="a31b0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a31b0-168">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a31b0-169">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-170">Search-Flags</span></span>           | <span data-ttu-id="a31b0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a31b0-171">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-172">System-Flags</span></span>           | <span data-ttu-id="a31b0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a31b0-173">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a31b0-174">Classes used in</span></span>        | [<span data-ttu-id="a31b0-175">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a31b0-175">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="a31b0-176">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a31b0-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a31b0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a31b0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a31b0-178">進入</span><span class="sxs-lookup"><span data-stu-id="a31b0-178">Entry</span></span> | <span data-ttu-id="a31b0-179">值</span><span class="sxs-lookup"><span data-stu-id="a31b0-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31b0-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a31b0-180">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a31b0-181">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a31b0-182">System-Only</span></span>            | <span data-ttu-id="a31b0-183">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-183">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a31b0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a31b0-185">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-185">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a31b0-186">Is Indexed</span></span>             | <span data-ttu-id="a31b0-187">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-187">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a31b0-188">In Global Catalog</span></span>      | <span data-ttu-id="a31b0-189">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-189">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a31b0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a31b0-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a31b0-191">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="a31b0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a31b0-192">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a31b0-193">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-194">Search-Flags</span></span>           | <span data-ttu-id="a31b0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a31b0-195">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-196">System-Flags</span></span>           | <span data-ttu-id="a31b0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a31b0-197">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a31b0-198">Classes used in</span></span>        | [<span data-ttu-id="a31b0-199">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a31b0-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="a31b0-200">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a31b0-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a31b0-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a31b0-201">Windows Server 2008</span></span>



| <span data-ttu-id="a31b0-202">進入</span><span class="sxs-lookup"><span data-stu-id="a31b0-202">Entry</span></span> | <span data-ttu-id="a31b0-203">值</span><span class="sxs-lookup"><span data-stu-id="a31b0-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31b0-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a31b0-204">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a31b0-205">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a31b0-206">System-Only</span></span>            | <span data-ttu-id="a31b0-207">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-207">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a31b0-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a31b0-209">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-209">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a31b0-210">Is Indexed</span></span>             | <span data-ttu-id="a31b0-211">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-211">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a31b0-212">In Global Catalog</span></span>      | <span data-ttu-id="a31b0-213">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-213">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a31b0-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a31b0-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a31b0-215">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="a31b0-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a31b0-216">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a31b0-217">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-218">Search-Flags</span></span>           | <span data-ttu-id="a31b0-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a31b0-219">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-220">System-Flags</span></span>           | <span data-ttu-id="a31b0-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a31b0-221">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a31b0-222">Classes used in</span></span>        | [<span data-ttu-id="a31b0-223">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a31b0-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="a31b0-224">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a31b0-224">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a31b0-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a31b0-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a31b0-226">進入</span><span class="sxs-lookup"><span data-stu-id="a31b0-226">Entry</span></span> | <span data-ttu-id="a31b0-227">值</span><span class="sxs-lookup"><span data-stu-id="a31b0-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31b0-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a31b0-228">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a31b0-229">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a31b0-230">System-Only</span></span>            | <span data-ttu-id="a31b0-231">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-231">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a31b0-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a31b0-233">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-233">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a31b0-234">Is Indexed</span></span>             | <span data-ttu-id="a31b0-235">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-235">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a31b0-236">In Global Catalog</span></span>      | <span data-ttu-id="a31b0-237">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-237">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a31b0-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a31b0-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a31b0-239">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="a31b0-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a31b0-240">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a31b0-241">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-242">Search-Flags</span></span>           | <span data-ttu-id="a31b0-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a31b0-243">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-244">System-Flags</span></span>           | <span data-ttu-id="a31b0-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a31b0-245">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a31b0-246">Classes used in</span></span>        | [<span data-ttu-id="a31b0-247">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a31b0-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="a31b0-248">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a31b0-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a31b0-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a31b0-249">Windows Server 2012</span></span>



| <span data-ttu-id="a31b0-250">進入</span><span class="sxs-lookup"><span data-stu-id="a31b0-250">Entry</span></span> | <span data-ttu-id="a31b0-251">值</span><span class="sxs-lookup"><span data-stu-id="a31b0-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31b0-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a31b0-252">Link-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a31b0-253">MAPI-Id</span></span>                | \-                                                                                                                |
| <span data-ttu-id="a31b0-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="a31b0-254">System-Only</span></span>            | <span data-ttu-id="a31b0-255">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-255">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a31b0-256">Is-Single-Valued</span></span>       | <span data-ttu-id="a31b0-257">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-257">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a31b0-258">Is Indexed</span></span>             | <span data-ttu-id="a31b0-259">否</span><span class="sxs-lookup"><span data-stu-id="a31b0-259">False</span></span>                                                                                                             |
| <span data-ttu-id="a31b0-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a31b0-260">In Global Catalog</span></span>      | <span data-ttu-id="a31b0-261">對</span><span class="sxs-lookup"><span data-stu-id="a31b0-261">True</span></span>                                                                                                              |
| <span data-ttu-id="a31b0-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a31b0-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="a31b0-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a31b0-263">O:BAG:BAD:S:</span></span>                                                                                                      |
| <span data-ttu-id="a31b0-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a31b0-264">Range-Lower</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a31b0-265">Range-Upper</span></span>            | \-                                                                                                                |
| <span data-ttu-id="a31b0-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-266">Search-Flags</span></span>           | <span data-ttu-id="a31b0-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a31b0-267">0x00000000</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a31b0-268">System-Flags</span></span>           | <span data-ttu-id="a31b0-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a31b0-269">0x00000010</span></span>                                                                                                        |
| <span data-ttu-id="a31b0-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a31b0-270">Classes used in</span></span>        | [<span data-ttu-id="a31b0-271">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="a31b0-271">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> [<span data-ttu-id="a31b0-272">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="a31b0-272">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





