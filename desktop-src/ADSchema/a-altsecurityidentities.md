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
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="fe6ef-105">Alt-Security-識別屬性</span><span class="sxs-lookup"><span data-stu-id="fe6ef-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="fe6ef-106">針對驗證目的，包含 x.509 憑證或外部 Kerberos 使用者帳戶到此使用者的對應。</span><span class="sxs-lookup"><span data-stu-id="fe6ef-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="fe6ef-107">進入</span><span class="sxs-lookup"><span data-stu-id="fe6ef-107">Entry</span></span> | <span data-ttu-id="fe6ef-108">值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="fe6ef-109">CN</span><span class="sxs-lookup"><span data-stu-id="fe6ef-109">CN</span></span>                | <span data-ttu-id="fe6ef-110">Alt-Security-身分識別</span><span class="sxs-lookup"><span data-stu-id="fe6ef-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="fe6ef-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fe6ef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fe6ef-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="fe6ef-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="fe6ef-113">大小</span><span class="sxs-lookup"><span data-stu-id="fe6ef-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="fe6ef-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fe6ef-114">Update Privilege</span></span>  | <span data-ttu-id="fe6ef-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="fe6ef-115">Domain administrator</span></span>                                |
| <span data-ttu-id="fe6ef-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fe6ef-116">Update Frequency</span></span>  | <span data-ttu-id="fe6ef-117">每次需要新的驗證機制時。</span><span class="sxs-lookup"><span data-stu-id="fe6ef-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="fe6ef-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fe6ef-118">Attribute-Id</span></span>      | <span data-ttu-id="fe6ef-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="fe6ef-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="fe6ef-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fe6ef-120">System-Id-Guid</span></span>    | <span data-ttu-id="fe6ef-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fe6ef-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="fe6ef-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe6ef-122">Syntax</span></span>            | [<span data-ttu-id="fe6ef-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="fe6ef-124">實作</span><span class="sxs-lookup"><span data-stu-id="fe6ef-124">Implementations</span></span>

-   [<span data-ttu-id="fe6ef-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fe6ef-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fe6ef-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fe6ef-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fe6ef-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fe6ef-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fe6ef-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fe6ef-131">Windows 2000 Server</span></span>



| <span data-ttu-id="fe6ef-132">進入</span><span class="sxs-lookup"><span data-stu-id="fe6ef-132">Entry</span></span> | <span data-ttu-id="fe6ef-133">值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fe6ef-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe6ef-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe6ef-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe6ef-136">System-Only</span></span>            | <span data-ttu-id="fe6ef-137">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-137">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fe6ef-139">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-139">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe6ef-140">Is Indexed</span></span>             | <span data-ttu-id="fe6ef-141">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-141">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe6ef-142">In Global Catalog</span></span>      | <span data-ttu-id="fe6ef-143">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-143">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe6ef-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe6ef-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe6ef-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fe6ef-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe6ef-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe6ef-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-148">Search-Flags</span></span>           | <span data-ttu-id="fe6ef-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe6ef-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="fe6ef-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-150">System-Flags</span></span>           | <span data-ttu-id="fe6ef-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fe6ef-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="fe6ef-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe6ef-152">Classes used in</span></span>        | [<span data-ttu-id="fe6ef-153">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fe6ef-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe6ef-154">Windows Server 2003</span></span>



| <span data-ttu-id="fe6ef-155">進入</span><span class="sxs-lookup"><span data-stu-id="fe6ef-155">Entry</span></span> | <span data-ttu-id="fe6ef-156">值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fe6ef-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe6ef-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe6ef-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe6ef-159">System-Only</span></span>            | <span data-ttu-id="fe6ef-160">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-160">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fe6ef-162">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-162">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe6ef-163">Is Indexed</span></span>             | <span data-ttu-id="fe6ef-164">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-164">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe6ef-165">In Global Catalog</span></span>      | <span data-ttu-id="fe6ef-166">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-166">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe6ef-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe6ef-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe6ef-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fe6ef-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe6ef-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe6ef-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-171">Search-Flags</span></span>           | <span data-ttu-id="fe6ef-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe6ef-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="fe6ef-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-173">System-Flags</span></span>           | <span data-ttu-id="fe6ef-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fe6ef-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="fe6ef-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe6ef-175">Classes used in</span></span>        | [<span data-ttu-id="fe6ef-176">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fe6ef-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe6ef-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fe6ef-178">進入</span><span class="sxs-lookup"><span data-stu-id="fe6ef-178">Entry</span></span> | <span data-ttu-id="fe6ef-179">值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fe6ef-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe6ef-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe6ef-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe6ef-182">System-Only</span></span>            | <span data-ttu-id="fe6ef-183">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-183">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fe6ef-185">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-185">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe6ef-186">Is Indexed</span></span>             | <span data-ttu-id="fe6ef-187">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-187">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe6ef-188">In Global Catalog</span></span>      | <span data-ttu-id="fe6ef-189">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-189">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe6ef-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe6ef-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe6ef-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fe6ef-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe6ef-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe6ef-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-194">Search-Flags</span></span>           | <span data-ttu-id="fe6ef-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe6ef-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="fe6ef-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-196">System-Flags</span></span>           | <span data-ttu-id="fe6ef-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fe6ef-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="fe6ef-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe6ef-198">Classes used in</span></span>        | [<span data-ttu-id="fe6ef-199">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fe6ef-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe6ef-200">Windows Server 2008</span></span>



| <span data-ttu-id="fe6ef-201">進入</span><span class="sxs-lookup"><span data-stu-id="fe6ef-201">Entry</span></span> | <span data-ttu-id="fe6ef-202">值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fe6ef-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe6ef-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe6ef-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe6ef-205">System-Only</span></span>            | <span data-ttu-id="fe6ef-206">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-206">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fe6ef-208">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-208">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe6ef-209">Is Indexed</span></span>             | <span data-ttu-id="fe6ef-210">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-210">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe6ef-211">In Global Catalog</span></span>      | <span data-ttu-id="fe6ef-212">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-212">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe6ef-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe6ef-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe6ef-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fe6ef-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe6ef-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe6ef-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-217">Search-Flags</span></span>           | <span data-ttu-id="fe6ef-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe6ef-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="fe6ef-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-219">System-Flags</span></span>           | <span data-ttu-id="fe6ef-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fe6ef-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="fe6ef-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe6ef-221">Classes used in</span></span>        | [<span data-ttu-id="fe6ef-222">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fe6ef-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe6ef-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fe6ef-224">進入</span><span class="sxs-lookup"><span data-stu-id="fe6ef-224">Entry</span></span> | <span data-ttu-id="fe6ef-225">值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fe6ef-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe6ef-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe6ef-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe6ef-228">System-Only</span></span>            | <span data-ttu-id="fe6ef-229">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-229">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fe6ef-231">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-231">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe6ef-232">Is Indexed</span></span>             | <span data-ttu-id="fe6ef-233">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-233">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe6ef-234">In Global Catalog</span></span>      | <span data-ttu-id="fe6ef-235">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-235">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe6ef-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe6ef-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe6ef-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fe6ef-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe6ef-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe6ef-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-240">Search-Flags</span></span>           | <span data-ttu-id="fe6ef-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe6ef-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="fe6ef-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-242">System-Flags</span></span>           | <span data-ttu-id="fe6ef-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fe6ef-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="fe6ef-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe6ef-244">Classes used in</span></span>        | [<span data-ttu-id="fe6ef-245">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fe6ef-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe6ef-246">Windows Server 2012</span></span>



| <span data-ttu-id="fe6ef-247">進入</span><span class="sxs-lookup"><span data-stu-id="fe6ef-247">Entry</span></span> | <span data-ttu-id="fe6ef-248">值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fe6ef-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe6ef-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe6ef-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fe6ef-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe6ef-251">System-Only</span></span>            | <span data-ttu-id="fe6ef-252">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-252">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe6ef-253">Is-Single-Valued</span></span>       | <span data-ttu-id="fe6ef-254">否</span><span class="sxs-lookup"><span data-stu-id="fe6ef-254">False</span></span>                                                        |
| <span data-ttu-id="fe6ef-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe6ef-255">Is Indexed</span></span>             | <span data-ttu-id="fe6ef-256">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-256">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe6ef-257">In Global Catalog</span></span>      | <span data-ttu-id="fe6ef-258">對</span><span class="sxs-lookup"><span data-stu-id="fe6ef-258">True</span></span>                                                         |
| <span data-ttu-id="fe6ef-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe6ef-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe6ef-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe6ef-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fe6ef-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe6ef-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe6ef-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fe6ef-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-263">Search-Flags</span></span>           | <span data-ttu-id="fe6ef-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe6ef-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="fe6ef-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe6ef-265">System-Flags</span></span>           | <span data-ttu-id="fe6ef-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="fe6ef-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="fe6ef-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe6ef-267">Classes used in</span></span>        | [<span data-ttu-id="fe6ef-268">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="fe6ef-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





