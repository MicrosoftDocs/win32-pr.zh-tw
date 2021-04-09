---
title: Alt-Security-識別屬性
description: 針對驗證目的，包含 x.509 憑證或外部 Kerberos 使用者帳戶到此使用者的對應。
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Alt-Security-身分識別屬性 AD 架構
- altSecurityIdentities 屬性 AD 架構
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935300"
---
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="d90c5-105">Alt-Security-識別屬性</span><span class="sxs-lookup"><span data-stu-id="d90c5-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="d90c5-106">針對驗證目的，包含 x.509 憑證或外部 Kerberos 使用者帳戶到此使用者的對應。</span><span class="sxs-lookup"><span data-stu-id="d90c5-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="d90c5-107">進入</span><span class="sxs-lookup"><span data-stu-id="d90c5-107">Entry</span></span> | <span data-ttu-id="d90c5-108">值</span><span class="sxs-lookup"><span data-stu-id="d90c5-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="d90c5-109">CN</span><span class="sxs-lookup"><span data-stu-id="d90c5-109">CN</span></span>                | <span data-ttu-id="d90c5-110">Alt-Security-身分識別</span><span class="sxs-lookup"><span data-stu-id="d90c5-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="d90c5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d90c5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d90c5-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="d90c5-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="d90c5-113">大小</span><span class="sxs-lookup"><span data-stu-id="d90c5-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="d90c5-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d90c5-114">Update Privilege</span></span>  | <span data-ttu-id="d90c5-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="d90c5-115">Domain administrator</span></span>                                |
| <span data-ttu-id="d90c5-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d90c5-116">Update Frequency</span></span>  | <span data-ttu-id="d90c5-117">每次需要新的驗證機制時。</span><span class="sxs-lookup"><span data-stu-id="d90c5-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="d90c5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d90c5-118">Attribute-Id</span></span>      | <span data-ttu-id="d90c5-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="d90c5-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="d90c5-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d90c5-120">System-Id-Guid</span></span>    | <span data-ttu-id="d90c5-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d90c5-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="d90c5-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90c5-122">Syntax</span></span>            | [<span data-ttu-id="d90c5-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d90c5-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="d90c5-124">實作</span><span class="sxs-lookup"><span data-stu-id="d90c5-124">Implementations</span></span>

-   [<span data-ttu-id="d90c5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d90c5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d90c5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d90c5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d90c5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d90c5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d90c5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d90c5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d90c5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d90c5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d90c5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d90c5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d90c5-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d90c5-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d90c5-132">進入</span><span class="sxs-lookup"><span data-stu-id="d90c5-132">Entry</span></span> | <span data-ttu-id="d90c5-133">值</span><span class="sxs-lookup"><span data-stu-id="d90c5-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d90c5-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d90c5-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d90c5-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d90c5-136">System-Only</span></span>            | <span data-ttu-id="d90c5-137">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-137">False</span></span>                                                        |
| <span data-ttu-id="d90c5-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d90c5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d90c5-139">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-139">False</span></span>                                                        |
| <span data-ttu-id="d90c5-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d90c5-140">Is Indexed</span></span>             | <span data-ttu-id="d90c5-141">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-141">True</span></span>                                                         |
| <span data-ttu-id="d90c5-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d90c5-142">In Global Catalog</span></span>      | <span data-ttu-id="d90c5-143">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-143">True</span></span>                                                         |
| <span data-ttu-id="d90c5-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d90c5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d90c5-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d90c5-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d90c5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d90c5-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d90c5-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-148">Search-Flags</span></span>           | <span data-ttu-id="d90c5-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d90c5-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="d90c5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-150">System-Flags</span></span>           | <span data-ttu-id="d90c5-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d90c5-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="d90c5-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d90c5-152">Classes used in</span></span>        | [<span data-ttu-id="d90c5-153">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d90c5-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d90c5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d90c5-154">Windows Server 2003</span></span>



| <span data-ttu-id="d90c5-155">進入</span><span class="sxs-lookup"><span data-stu-id="d90c5-155">Entry</span></span> | <span data-ttu-id="d90c5-156">值</span><span class="sxs-lookup"><span data-stu-id="d90c5-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d90c5-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d90c5-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d90c5-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d90c5-159">System-Only</span></span>            | <span data-ttu-id="d90c5-160">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-160">False</span></span>                                                        |
| <span data-ttu-id="d90c5-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d90c5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d90c5-162">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-162">False</span></span>                                                        |
| <span data-ttu-id="d90c5-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d90c5-163">Is Indexed</span></span>             | <span data-ttu-id="d90c5-164">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-164">True</span></span>                                                         |
| <span data-ttu-id="d90c5-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d90c5-165">In Global Catalog</span></span>      | <span data-ttu-id="d90c5-166">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-166">True</span></span>                                                         |
| <span data-ttu-id="d90c5-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d90c5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d90c5-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d90c5-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d90c5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d90c5-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d90c5-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-171">Search-Flags</span></span>           | <span data-ttu-id="d90c5-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d90c5-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="d90c5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-173">System-Flags</span></span>           | <span data-ttu-id="d90c5-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d90c5-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="d90c5-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d90c5-175">Classes used in</span></span>        | [<span data-ttu-id="d90c5-176">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d90c5-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d90c5-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d90c5-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d90c5-178">進入</span><span class="sxs-lookup"><span data-stu-id="d90c5-178">Entry</span></span> | <span data-ttu-id="d90c5-179">值</span><span class="sxs-lookup"><span data-stu-id="d90c5-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d90c5-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d90c5-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d90c5-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d90c5-182">System-Only</span></span>            | <span data-ttu-id="d90c5-183">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-183">False</span></span>                                                        |
| <span data-ttu-id="d90c5-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d90c5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d90c5-185">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-185">False</span></span>                                                        |
| <span data-ttu-id="d90c5-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d90c5-186">Is Indexed</span></span>             | <span data-ttu-id="d90c5-187">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-187">True</span></span>                                                         |
| <span data-ttu-id="d90c5-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d90c5-188">In Global Catalog</span></span>      | <span data-ttu-id="d90c5-189">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-189">True</span></span>                                                         |
| <span data-ttu-id="d90c5-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d90c5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d90c5-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d90c5-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d90c5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d90c5-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d90c5-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-194">Search-Flags</span></span>           | <span data-ttu-id="d90c5-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d90c5-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="d90c5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-196">System-Flags</span></span>           | <span data-ttu-id="d90c5-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d90c5-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="d90c5-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d90c5-198">Classes used in</span></span>        | [<span data-ttu-id="d90c5-199">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d90c5-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d90c5-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d90c5-200">Windows Server 2008</span></span>



| <span data-ttu-id="d90c5-201">進入</span><span class="sxs-lookup"><span data-stu-id="d90c5-201">Entry</span></span> | <span data-ttu-id="d90c5-202">值</span><span class="sxs-lookup"><span data-stu-id="d90c5-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d90c5-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d90c5-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d90c5-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d90c5-205">System-Only</span></span>            | <span data-ttu-id="d90c5-206">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-206">False</span></span>                                                        |
| <span data-ttu-id="d90c5-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d90c5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d90c5-208">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-208">False</span></span>                                                        |
| <span data-ttu-id="d90c5-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d90c5-209">Is Indexed</span></span>             | <span data-ttu-id="d90c5-210">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-210">True</span></span>                                                         |
| <span data-ttu-id="d90c5-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d90c5-211">In Global Catalog</span></span>      | <span data-ttu-id="d90c5-212">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-212">True</span></span>                                                         |
| <span data-ttu-id="d90c5-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d90c5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d90c5-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d90c5-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d90c5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d90c5-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d90c5-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-217">Search-Flags</span></span>           | <span data-ttu-id="d90c5-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d90c5-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="d90c5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-219">System-Flags</span></span>           | <span data-ttu-id="d90c5-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d90c5-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="d90c5-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d90c5-221">Classes used in</span></span>        | [<span data-ttu-id="d90c5-222">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d90c5-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d90c5-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d90c5-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d90c5-224">進入</span><span class="sxs-lookup"><span data-stu-id="d90c5-224">Entry</span></span> | <span data-ttu-id="d90c5-225">值</span><span class="sxs-lookup"><span data-stu-id="d90c5-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d90c5-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d90c5-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d90c5-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d90c5-228">System-Only</span></span>            | <span data-ttu-id="d90c5-229">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-229">False</span></span>                                                        |
| <span data-ttu-id="d90c5-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d90c5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d90c5-231">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-231">False</span></span>                                                        |
| <span data-ttu-id="d90c5-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d90c5-232">Is Indexed</span></span>             | <span data-ttu-id="d90c5-233">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-233">True</span></span>                                                         |
| <span data-ttu-id="d90c5-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d90c5-234">In Global Catalog</span></span>      | <span data-ttu-id="d90c5-235">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-235">True</span></span>                                                         |
| <span data-ttu-id="d90c5-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d90c5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d90c5-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d90c5-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d90c5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d90c5-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d90c5-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-240">Search-Flags</span></span>           | <span data-ttu-id="d90c5-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d90c5-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="d90c5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-242">System-Flags</span></span>           | <span data-ttu-id="d90c5-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d90c5-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="d90c5-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d90c5-244">Classes used in</span></span>        | [<span data-ttu-id="d90c5-245">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d90c5-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d90c5-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d90c5-246">Windows Server 2012</span></span>



| <span data-ttu-id="d90c5-247">進入</span><span class="sxs-lookup"><span data-stu-id="d90c5-247">Entry</span></span> | <span data-ttu-id="d90c5-248">值</span><span class="sxs-lookup"><span data-stu-id="d90c5-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d90c5-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d90c5-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d90c5-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d90c5-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d90c5-251">System-Only</span></span>            | <span data-ttu-id="d90c5-252">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-252">False</span></span>                                                        |
| <span data-ttu-id="d90c5-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d90c5-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d90c5-254">否</span><span class="sxs-lookup"><span data-stu-id="d90c5-254">False</span></span>                                                        |
| <span data-ttu-id="d90c5-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d90c5-255">Is Indexed</span></span>             | <span data-ttu-id="d90c5-256">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-256">True</span></span>                                                         |
| <span data-ttu-id="d90c5-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d90c5-257">In Global Catalog</span></span>      | <span data-ttu-id="d90c5-258">對</span><span class="sxs-lookup"><span data-stu-id="d90c5-258">True</span></span>                                                         |
| <span data-ttu-id="d90c5-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d90c5-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d90c5-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d90c5-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d90c5-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d90c5-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d90c5-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d90c5-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-263">Search-Flags</span></span>           | <span data-ttu-id="d90c5-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d90c5-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="d90c5-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d90c5-265">System-Flags</span></span>           | <span data-ttu-id="d90c5-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d90c5-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="d90c5-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d90c5-267">Classes used in</span></span>        | [<span data-ttu-id="d90c5-268">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="d90c5-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





