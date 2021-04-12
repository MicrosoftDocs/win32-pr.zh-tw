---
title: Supplemental-Credentials 屬性
description: 用於驗證的預存認證。 使用者密碼的加密版本。 這個屬性不是可讀取或可寫入的。
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- Supplemental-Credentials 屬性 AD 架構
- supplementalCredentials 屬性 AD 架構
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19a73b3ae3cf19745fc995a59c336b72d264e78
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509576"
---
# <a name="supplemental-credentials-attribute"></a><span data-ttu-id="0c975-107">Supplemental-Credentials 屬性</span><span class="sxs-lookup"><span data-stu-id="0c975-107">Supplemental-Credentials attribute</span></span>

<span data-ttu-id="0c975-108">用於驗證的預存認證。</span><span class="sxs-lookup"><span data-stu-id="0c975-108">Stored credentials for use in authenticating.</span></span> <span data-ttu-id="0c975-109">使用者密碼的加密版本。</span><span class="sxs-lookup"><span data-stu-id="0c975-109">The encrypted version of the user's password.</span></span> <span data-ttu-id="0c975-110">這個屬性不是可讀取或可寫入的。</span><span class="sxs-lookup"><span data-stu-id="0c975-110">This attribute is neither readable nor writable.</span></span>



| <span data-ttu-id="0c975-111">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-111">Entry</span></span> | <span data-ttu-id="0c975-112">值</span><span class="sxs-lookup"><span data-stu-id="0c975-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0c975-113">CN</span><span class="sxs-lookup"><span data-stu-id="0c975-113">CN</span></span>                | <span data-ttu-id="0c975-114">Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="0c975-114">Supplemental-Credentials</span></span>                              |
| <span data-ttu-id="0c975-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0c975-115">Ldap-Display-Name</span></span> | <span data-ttu-id="0c975-116">supplementalCredentials</span><span class="sxs-lookup"><span data-stu-id="0c975-116">supplementalCredentials</span></span>                               |
| <span data-ttu-id="0c975-117">大小</span><span class="sxs-lookup"><span data-stu-id="0c975-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0c975-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0c975-118">Update Privilege</span></span>  | <span data-ttu-id="0c975-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0c975-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="0c975-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0c975-120">Update Frequency</span></span>  | <span data-ttu-id="0c975-121">當使用者的密碼變更時。</span><span class="sxs-lookup"><span data-stu-id="0c975-121">When the user's password changes.</span></span>                     |
| <span data-ttu-id="0c975-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-122">Attribute-Id</span></span>      | <span data-ttu-id="0c975-123">1.2.840.113556.1.4.125</span><span class="sxs-lookup"><span data-stu-id="0c975-123">1.2.840.113556.1.4.125</span></span>                                |
| <span data-ttu-id="0c975-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0c975-124">System-Id-Guid</span></span>    | <span data-ttu-id="0c975-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0c975-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="0c975-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c975-126">Syntax</span></span>            | [<span data-ttu-id="0c975-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="0c975-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0c975-128">實作</span><span class="sxs-lookup"><span data-stu-id="0c975-128">Implementations</span></span>

-   [<span data-ttu-id="0c975-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c975-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c975-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c975-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c975-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="0c975-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0c975-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c975-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c975-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c975-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c975-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c975-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c975-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c975-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c975-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c975-136">Windows 2000 Server</span></span>



| <span data-ttu-id="0c975-137">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-137">Entry</span></span> | <span data-ttu-id="0c975-138">值</span><span class="sxs-lookup"><span data-stu-id="0c975-138">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0c975-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c975-139">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-140">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c975-141">System-Only</span></span>            | <span data-ttu-id="0c975-142">否</span><span class="sxs-lookup"><span data-stu-id="0c975-142">False</span></span>                                                        |
| <span data-ttu-id="0c975-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c975-143">Is-Single-Valued</span></span>       | <span data-ttu-id="0c975-144">否</span><span class="sxs-lookup"><span data-stu-id="0c975-144">False</span></span>                                                        |
| <span data-ttu-id="0c975-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c975-145">Is Indexed</span></span>             | <span data-ttu-id="0c975-146">否</span><span class="sxs-lookup"><span data-stu-id="0c975-146">False</span></span>                                                        |
| <span data-ttu-id="0c975-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c975-147">In Global Catalog</span></span>      | <span data-ttu-id="0c975-148">否</span><span class="sxs-lookup"><span data-stu-id="0c975-148">False</span></span>                                                        |
| <span data-ttu-id="0c975-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c975-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c975-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c975-150">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="0c975-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c975-151">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c975-152">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-153">Search-Flags</span></span>           | <span data-ttu-id="0c975-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c975-154">0x00000000</span></span>                                                   |
| <span data-ttu-id="0c975-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-155">System-Flags</span></span>           | <span data-ttu-id="0c975-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c975-156">0x00000010</span></span>                                                   |
| <span data-ttu-id="0c975-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c975-157">Classes used in</span></span>        | [<span data-ttu-id="0c975-158">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="0c975-158">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c975-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c975-159">Windows Server 2003</span></span>



| <span data-ttu-id="0c975-160">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-160">Entry</span></span> | <span data-ttu-id="0c975-161">值</span><span class="sxs-lookup"><span data-stu-id="0c975-161">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0c975-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c975-162">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-163">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c975-164">System-Only</span></span>            | <span data-ttu-id="0c975-165">否</span><span class="sxs-lookup"><span data-stu-id="0c975-165">False</span></span>                                                        |
| <span data-ttu-id="0c975-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c975-166">Is-Single-Valued</span></span>       | <span data-ttu-id="0c975-167">否</span><span class="sxs-lookup"><span data-stu-id="0c975-167">False</span></span>                                                        |
| <span data-ttu-id="0c975-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c975-168">Is Indexed</span></span>             | <span data-ttu-id="0c975-169">否</span><span class="sxs-lookup"><span data-stu-id="0c975-169">False</span></span>                                                        |
| <span data-ttu-id="0c975-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c975-170">In Global Catalog</span></span>      | <span data-ttu-id="0c975-171">否</span><span class="sxs-lookup"><span data-stu-id="0c975-171">False</span></span>                                                        |
| <span data-ttu-id="0c975-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c975-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c975-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c975-173">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="0c975-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c975-174">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c975-175">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-176">Search-Flags</span></span>           | <span data-ttu-id="0c975-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c975-177">0x00000000</span></span>                                                   |
| <span data-ttu-id="0c975-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-178">System-Flags</span></span>           | <span data-ttu-id="0c975-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c975-179">0x00000010</span></span>                                                   |
| <span data-ttu-id="0c975-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c975-180">Classes used in</span></span>        | [<span data-ttu-id="0c975-181">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="0c975-181">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0c975-182">亞當</span><span class="sxs-lookup"><span data-stu-id="0c975-182">ADAM</span></span>



| <span data-ttu-id="0c975-183">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-183">Entry</span></span> | <span data-ttu-id="0c975-184">值</span><span class="sxs-lookup"><span data-stu-id="0c975-184">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0c975-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c975-185">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-186">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c975-187">System-Only</span></span>            | <span data-ttu-id="0c975-188">否</span><span class="sxs-lookup"><span data-stu-id="0c975-188">False</span></span>                                                        |
| <span data-ttu-id="0c975-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c975-189">Is-Single-Valued</span></span>       | <span data-ttu-id="0c975-190">否</span><span class="sxs-lookup"><span data-stu-id="0c975-190">False</span></span>                                                        |
| <span data-ttu-id="0c975-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c975-191">Is Indexed</span></span>             | <span data-ttu-id="0c975-192">否</span><span class="sxs-lookup"><span data-stu-id="0c975-192">False</span></span>                                                        |
| <span data-ttu-id="0c975-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c975-193">In Global Catalog</span></span>      | <span data-ttu-id="0c975-194">否</span><span class="sxs-lookup"><span data-stu-id="0c975-194">False</span></span>                                                        |
| <span data-ttu-id="0c975-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c975-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c975-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c975-196">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="0c975-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c975-197">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c975-198">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-199">Search-Flags</span></span>           | <span data-ttu-id="0c975-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c975-200">0x00000000</span></span>                                                   |
| <span data-ttu-id="0c975-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-201">System-Flags</span></span>           | <span data-ttu-id="0c975-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c975-202">0x00000010</span></span>                                                   |
| <span data-ttu-id="0c975-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c975-203">Classes used in</span></span>        | [<span data-ttu-id="0c975-204">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="0c975-204">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c975-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c975-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c975-206">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-206">Entry</span></span> | <span data-ttu-id="0c975-207">值</span><span class="sxs-lookup"><span data-stu-id="0c975-207">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0c975-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c975-208">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-209">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c975-210">System-Only</span></span>            | <span data-ttu-id="0c975-211">否</span><span class="sxs-lookup"><span data-stu-id="0c975-211">False</span></span>                                                        |
| <span data-ttu-id="0c975-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c975-212">Is-Single-Valued</span></span>       | <span data-ttu-id="0c975-213">否</span><span class="sxs-lookup"><span data-stu-id="0c975-213">False</span></span>                                                        |
| <span data-ttu-id="0c975-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c975-214">Is Indexed</span></span>             | <span data-ttu-id="0c975-215">否</span><span class="sxs-lookup"><span data-stu-id="0c975-215">False</span></span>                                                        |
| <span data-ttu-id="0c975-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c975-216">In Global Catalog</span></span>      | <span data-ttu-id="0c975-217">否</span><span class="sxs-lookup"><span data-stu-id="0c975-217">False</span></span>                                                        |
| <span data-ttu-id="0c975-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c975-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c975-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c975-219">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="0c975-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c975-220">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c975-221">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-222">Search-Flags</span></span>           | <span data-ttu-id="0c975-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c975-223">0x00000000</span></span>                                                   |
| <span data-ttu-id="0c975-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-224">System-Flags</span></span>           | <span data-ttu-id="0c975-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c975-225">0x00000010</span></span>                                                   |
| <span data-ttu-id="0c975-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c975-226">Classes used in</span></span>        | [<span data-ttu-id="0c975-227">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="0c975-227">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c975-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c975-228">Windows Server 2008</span></span>



| <span data-ttu-id="0c975-229">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-229">Entry</span></span> | <span data-ttu-id="0c975-230">值</span><span class="sxs-lookup"><span data-stu-id="0c975-230">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0c975-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c975-231">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-232">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c975-233">System-Only</span></span>            | <span data-ttu-id="0c975-234">否</span><span class="sxs-lookup"><span data-stu-id="0c975-234">False</span></span>                                                        |
| <span data-ttu-id="0c975-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c975-235">Is-Single-Valued</span></span>       | <span data-ttu-id="0c975-236">否</span><span class="sxs-lookup"><span data-stu-id="0c975-236">False</span></span>                                                        |
| <span data-ttu-id="0c975-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c975-237">Is Indexed</span></span>             | <span data-ttu-id="0c975-238">否</span><span class="sxs-lookup"><span data-stu-id="0c975-238">False</span></span>                                                        |
| <span data-ttu-id="0c975-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c975-239">In Global Catalog</span></span>      | <span data-ttu-id="0c975-240">否</span><span class="sxs-lookup"><span data-stu-id="0c975-240">False</span></span>                                                        |
| <span data-ttu-id="0c975-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c975-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c975-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c975-242">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="0c975-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c975-243">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c975-244">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-245">Search-Flags</span></span>           | <span data-ttu-id="0c975-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c975-246">0x00000000</span></span>                                                   |
| <span data-ttu-id="0c975-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-247">System-Flags</span></span>           | <span data-ttu-id="0c975-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c975-248">0x00000010</span></span>                                                   |
| <span data-ttu-id="0c975-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c975-249">Classes used in</span></span>        | [<span data-ttu-id="0c975-250">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="0c975-250">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c975-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c975-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c975-252">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-252">Entry</span></span> | <span data-ttu-id="0c975-253">值</span><span class="sxs-lookup"><span data-stu-id="0c975-253">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0c975-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c975-254">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-255">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c975-256">System-Only</span></span>            | <span data-ttu-id="0c975-257">否</span><span class="sxs-lookup"><span data-stu-id="0c975-257">False</span></span>                                                        |
| <span data-ttu-id="0c975-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c975-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0c975-259">否</span><span class="sxs-lookup"><span data-stu-id="0c975-259">False</span></span>                                                        |
| <span data-ttu-id="0c975-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c975-260">Is Indexed</span></span>             | <span data-ttu-id="0c975-261">否</span><span class="sxs-lookup"><span data-stu-id="0c975-261">False</span></span>                                                        |
| <span data-ttu-id="0c975-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c975-262">In Global Catalog</span></span>      | <span data-ttu-id="0c975-263">否</span><span class="sxs-lookup"><span data-stu-id="0c975-263">False</span></span>                                                        |
| <span data-ttu-id="0c975-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c975-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c975-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c975-265">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="0c975-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c975-266">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c975-267">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-268">Search-Flags</span></span>           | <span data-ttu-id="0c975-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c975-269">0x00000000</span></span>                                                   |
| <span data-ttu-id="0c975-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-270">System-Flags</span></span>           | <span data-ttu-id="0c975-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c975-271">0x00000010</span></span>                                                   |
| <span data-ttu-id="0c975-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c975-272">Classes used in</span></span>        | [<span data-ttu-id="0c975-273">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="0c975-273">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c975-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c975-274">Windows Server 2012</span></span>



| <span data-ttu-id="0c975-275">進入</span><span class="sxs-lookup"><span data-stu-id="0c975-275">Entry</span></span> | <span data-ttu-id="0c975-276">值</span><span class="sxs-lookup"><span data-stu-id="0c975-276">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0c975-277">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0c975-277">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c975-278">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="0c975-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c975-279">System-Only</span></span>            | <span data-ttu-id="0c975-280">否</span><span class="sxs-lookup"><span data-stu-id="0c975-280">False</span></span>                                                        |
| <span data-ttu-id="0c975-281">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0c975-281">Is-Single-Valued</span></span>       | <span data-ttu-id="0c975-282">否</span><span class="sxs-lookup"><span data-stu-id="0c975-282">False</span></span>                                                        |
| <span data-ttu-id="0c975-283">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0c975-283">Is Indexed</span></span>             | <span data-ttu-id="0c975-284">否</span><span class="sxs-lookup"><span data-stu-id="0c975-284">False</span></span>                                                        |
| <span data-ttu-id="0c975-285">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0c975-285">In Global Catalog</span></span>      | <span data-ttu-id="0c975-286">否</span><span class="sxs-lookup"><span data-stu-id="0c975-286">False</span></span>                                                        |
| <span data-ttu-id="0c975-287">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0c975-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c975-288">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0c975-288">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="0c975-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c975-289">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c975-290">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="0c975-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-291">Search-Flags</span></span>           | <span data-ttu-id="0c975-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c975-292">0x00000000</span></span>                                                   |
| <span data-ttu-id="0c975-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c975-293">System-Flags</span></span>           | <span data-ttu-id="0c975-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c975-294">0x00000010</span></span>                                                   |
| <span data-ttu-id="0c975-295">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0c975-295">Classes used in</span></span>        | [<span data-ttu-id="0c975-296">**安全性-主體**</span><span class="sxs-lookup"><span data-stu-id="0c975-296">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





