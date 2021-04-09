---
title: 使用者主體名稱屬性
description: 此屬性包含 UPN，其為以網際網路標準 RFC 822 為基礎之使用者的網際網路樣式登入名稱。
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- 使用者主體名稱屬性 AD 架構
- userPrincipalName 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935340"
---
# <a name="user-principal-name-attribute"></a><span data-ttu-id="895fe-105">使用者主體名稱屬性</span><span class="sxs-lookup"><span data-stu-id="895fe-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="895fe-106">此屬性包含 UPN，其為以網際網路標準 [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)為基礎之使用者的網際網路樣式登入名稱。</span><span class="sxs-lookup"><span data-stu-id="895fe-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="895fe-107">UPN 比分辨名稱短，而且更容易記住。</span><span class="sxs-lookup"><span data-stu-id="895fe-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="895fe-108">依照慣例，這應該對應到使用者的電子郵件名稱。</span><span class="sxs-lookup"><span data-stu-id="895fe-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="895fe-109">為此屬性設定的值等於使用者識別碼和功能變數名稱的長度。</span><span class="sxs-lookup"><span data-stu-id="895fe-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="895fe-110">如需此屬性的詳細資訊，請參閱 [使用者命名屬性](/windows/desktop/AD/naming-properties)。</span><span class="sxs-lookup"><span data-stu-id="895fe-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="895fe-111">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-111">Entry</span></span> | <span data-ttu-id="895fe-112">值</span><span class="sxs-lookup"><span data-stu-id="895fe-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="895fe-113">CN</span><span class="sxs-lookup"><span data-stu-id="895fe-113">CN</span></span>                | <span data-ttu-id="895fe-114">使用者主體名稱</span><span class="sxs-lookup"><span data-stu-id="895fe-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="895fe-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="895fe-115">Ldap-Display-Name</span></span> | <span data-ttu-id="895fe-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="895fe-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="895fe-117">大小</span><span class="sxs-lookup"><span data-stu-id="895fe-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="895fe-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="895fe-118">Update Privilege</span></span>  | <span data-ttu-id="895fe-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="895fe-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="895fe-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="895fe-120">Update Frequency</span></span>  | <span data-ttu-id="895fe-121">理論上，這絕對不會改變。</span><span class="sxs-lookup"><span data-stu-id="895fe-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="895fe-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-122">Attribute-Id</span></span>      | <span data-ttu-id="895fe-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="895fe-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="895fe-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="895fe-124">System-Id-Guid</span></span>    | <span data-ttu-id="895fe-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="895fe-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="895fe-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="895fe-126">Syntax</span></span>            | [<span data-ttu-id="895fe-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="895fe-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="895fe-128">實作</span><span class="sxs-lookup"><span data-stu-id="895fe-128">Implementations</span></span>

-   [<span data-ttu-id="895fe-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="895fe-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="895fe-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="895fe-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="895fe-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="895fe-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="895fe-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="895fe-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="895fe-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="895fe-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="895fe-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="895fe-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="895fe-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="895fe-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="895fe-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="895fe-136">Windows 2000 Server</span></span>



| <span data-ttu-id="895fe-137">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-137">Entry</span></span> | <span data-ttu-id="895fe-138">值</span><span class="sxs-lookup"><span data-stu-id="895fe-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="895fe-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="895fe-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="895fe-141">System-Only</span></span>            | <span data-ttu-id="895fe-142">否</span><span class="sxs-lookup"><span data-stu-id="895fe-142">False</span></span>                             |
| <span data-ttu-id="895fe-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="895fe-143">Is-Single-Valued</span></span>       | <span data-ttu-id="895fe-144">對</span><span class="sxs-lookup"><span data-stu-id="895fe-144">True</span></span>                              |
| <span data-ttu-id="895fe-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="895fe-145">Is Indexed</span></span>             | <span data-ttu-id="895fe-146">對</span><span class="sxs-lookup"><span data-stu-id="895fe-146">True</span></span>                              |
| <span data-ttu-id="895fe-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="895fe-147">In Global Catalog</span></span>      | <span data-ttu-id="895fe-148">對</span><span class="sxs-lookup"><span data-stu-id="895fe-148">True</span></span>                              |
| <span data-ttu-id="895fe-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="895fe-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="895fe-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="895fe-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="895fe-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="895fe-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="895fe-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="895fe-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="895fe-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-153">Search-Flags</span></span>           | <span data-ttu-id="895fe-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="895fe-154">0x00000001</span></span>                        |
| <span data-ttu-id="895fe-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-155">System-Flags</span></span>           | <span data-ttu-id="895fe-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="895fe-156">0x00000012</span></span>                        |
| <span data-ttu-id="895fe-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="895fe-157">Classes used in</span></span>        | [<span data-ttu-id="895fe-158">**User**</span><span class="sxs-lookup"><span data-stu-id="895fe-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="895fe-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="895fe-159">Windows Server 2003</span></span>



| <span data-ttu-id="895fe-160">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-160">Entry</span></span> | <span data-ttu-id="895fe-161">值</span><span class="sxs-lookup"><span data-stu-id="895fe-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="895fe-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="895fe-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="895fe-164">System-Only</span></span>            | <span data-ttu-id="895fe-165">否</span><span class="sxs-lookup"><span data-stu-id="895fe-165">False</span></span>                             |
| <span data-ttu-id="895fe-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="895fe-166">Is-Single-Valued</span></span>       | <span data-ttu-id="895fe-167">對</span><span class="sxs-lookup"><span data-stu-id="895fe-167">True</span></span>                              |
| <span data-ttu-id="895fe-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="895fe-168">Is Indexed</span></span>             | <span data-ttu-id="895fe-169">對</span><span class="sxs-lookup"><span data-stu-id="895fe-169">True</span></span>                              |
| <span data-ttu-id="895fe-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="895fe-170">In Global Catalog</span></span>      | <span data-ttu-id="895fe-171">對</span><span class="sxs-lookup"><span data-stu-id="895fe-171">True</span></span>                              |
| <span data-ttu-id="895fe-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="895fe-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="895fe-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="895fe-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="895fe-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="895fe-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="895fe-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="895fe-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="895fe-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-176">Search-Flags</span></span>           | <span data-ttu-id="895fe-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="895fe-177">0x00000001</span></span>                        |
| <span data-ttu-id="895fe-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-178">System-Flags</span></span>           | <span data-ttu-id="895fe-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="895fe-179">0x00000012</span></span>                        |
| <span data-ttu-id="895fe-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="895fe-180">Classes used in</span></span>        | [<span data-ttu-id="895fe-181">**User**</span><span class="sxs-lookup"><span data-stu-id="895fe-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="895fe-182">亞當</span><span class="sxs-lookup"><span data-stu-id="895fe-182">ADAM</span></span>



| <span data-ttu-id="895fe-183">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-183">Entry</span></span> | <span data-ttu-id="895fe-184">值</span><span class="sxs-lookup"><span data-stu-id="895fe-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="895fe-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="895fe-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="895fe-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="895fe-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="895fe-187">System-Only</span></span>            | <span data-ttu-id="895fe-188">否</span><span class="sxs-lookup"><span data-stu-id="895fe-188">False</span></span>        |
| <span data-ttu-id="895fe-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="895fe-189">Is-Single-Valued</span></span>       | <span data-ttu-id="895fe-190">對</span><span class="sxs-lookup"><span data-stu-id="895fe-190">True</span></span>         |
| <span data-ttu-id="895fe-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="895fe-191">Is Indexed</span></span>             | <span data-ttu-id="895fe-192">對</span><span class="sxs-lookup"><span data-stu-id="895fe-192">True</span></span>         |
| <span data-ttu-id="895fe-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="895fe-193">In Global Catalog</span></span>      | <span data-ttu-id="895fe-194">對</span><span class="sxs-lookup"><span data-stu-id="895fe-194">True</span></span>         |
| <span data-ttu-id="895fe-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="895fe-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="895fe-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="895fe-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="895fe-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="895fe-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="895fe-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="895fe-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="895fe-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-199">Search-Flags</span></span>           | <span data-ttu-id="895fe-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="895fe-200">0x00000001</span></span>   |
| <span data-ttu-id="895fe-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-201">System-Flags</span></span>           | <span data-ttu-id="895fe-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="895fe-202">0x00000012</span></span>   |
| <span data-ttu-id="895fe-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="895fe-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="895fe-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="895fe-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="895fe-205">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-205">Entry</span></span> | <span data-ttu-id="895fe-206">值</span><span class="sxs-lookup"><span data-stu-id="895fe-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="895fe-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="895fe-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="895fe-209">System-Only</span></span>            | <span data-ttu-id="895fe-210">否</span><span class="sxs-lookup"><span data-stu-id="895fe-210">False</span></span>                             |
| <span data-ttu-id="895fe-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="895fe-211">Is-Single-Valued</span></span>       | <span data-ttu-id="895fe-212">對</span><span class="sxs-lookup"><span data-stu-id="895fe-212">True</span></span>                              |
| <span data-ttu-id="895fe-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="895fe-213">Is Indexed</span></span>             | <span data-ttu-id="895fe-214">對</span><span class="sxs-lookup"><span data-stu-id="895fe-214">True</span></span>                              |
| <span data-ttu-id="895fe-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="895fe-215">In Global Catalog</span></span>      | <span data-ttu-id="895fe-216">對</span><span class="sxs-lookup"><span data-stu-id="895fe-216">True</span></span>                              |
| <span data-ttu-id="895fe-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="895fe-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="895fe-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="895fe-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="895fe-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="895fe-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="895fe-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="895fe-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="895fe-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-221">Search-Flags</span></span>           | <span data-ttu-id="895fe-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="895fe-222">0x00000001</span></span>                        |
| <span data-ttu-id="895fe-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-223">System-Flags</span></span>           | <span data-ttu-id="895fe-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="895fe-224">0x00000012</span></span>                        |
| <span data-ttu-id="895fe-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="895fe-225">Classes used in</span></span>        | [<span data-ttu-id="895fe-226">**User**</span><span class="sxs-lookup"><span data-stu-id="895fe-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="895fe-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="895fe-227">Windows Server 2008</span></span>



| <span data-ttu-id="895fe-228">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-228">Entry</span></span> | <span data-ttu-id="895fe-229">值</span><span class="sxs-lookup"><span data-stu-id="895fe-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="895fe-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="895fe-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="895fe-232">System-Only</span></span>            | <span data-ttu-id="895fe-233">否</span><span class="sxs-lookup"><span data-stu-id="895fe-233">False</span></span>                             |
| <span data-ttu-id="895fe-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="895fe-234">Is-Single-Valued</span></span>       | <span data-ttu-id="895fe-235">對</span><span class="sxs-lookup"><span data-stu-id="895fe-235">True</span></span>                              |
| <span data-ttu-id="895fe-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="895fe-236">Is Indexed</span></span>             | <span data-ttu-id="895fe-237">對</span><span class="sxs-lookup"><span data-stu-id="895fe-237">True</span></span>                              |
| <span data-ttu-id="895fe-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="895fe-238">In Global Catalog</span></span>      | <span data-ttu-id="895fe-239">對</span><span class="sxs-lookup"><span data-stu-id="895fe-239">True</span></span>                              |
| <span data-ttu-id="895fe-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="895fe-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="895fe-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="895fe-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="895fe-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="895fe-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="895fe-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="895fe-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="895fe-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-244">Search-Flags</span></span>           | <span data-ttu-id="895fe-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="895fe-245">0x00000001</span></span>                        |
| <span data-ttu-id="895fe-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-246">System-Flags</span></span>           | <span data-ttu-id="895fe-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="895fe-247">0x00000012</span></span>                        |
| <span data-ttu-id="895fe-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="895fe-248">Classes used in</span></span>        | [<span data-ttu-id="895fe-249">**User**</span><span class="sxs-lookup"><span data-stu-id="895fe-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="895fe-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="895fe-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="895fe-251">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-251">Entry</span></span> | <span data-ttu-id="895fe-252">值</span><span class="sxs-lookup"><span data-stu-id="895fe-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="895fe-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="895fe-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="895fe-255">System-Only</span></span>            | <span data-ttu-id="895fe-256">否</span><span class="sxs-lookup"><span data-stu-id="895fe-256">False</span></span>                             |
| <span data-ttu-id="895fe-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="895fe-257">Is-Single-Valued</span></span>       | <span data-ttu-id="895fe-258">對</span><span class="sxs-lookup"><span data-stu-id="895fe-258">True</span></span>                              |
| <span data-ttu-id="895fe-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="895fe-259">Is Indexed</span></span>             | <span data-ttu-id="895fe-260">對</span><span class="sxs-lookup"><span data-stu-id="895fe-260">True</span></span>                              |
| <span data-ttu-id="895fe-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="895fe-261">In Global Catalog</span></span>      | <span data-ttu-id="895fe-262">對</span><span class="sxs-lookup"><span data-stu-id="895fe-262">True</span></span>                              |
| <span data-ttu-id="895fe-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="895fe-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="895fe-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="895fe-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="895fe-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="895fe-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="895fe-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="895fe-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="895fe-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-267">Search-Flags</span></span>           | <span data-ttu-id="895fe-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="895fe-268">0x00000001</span></span>                        |
| <span data-ttu-id="895fe-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-269">System-Flags</span></span>           | <span data-ttu-id="895fe-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="895fe-270">0x00000012</span></span>                        |
| <span data-ttu-id="895fe-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="895fe-271">Classes used in</span></span>        | [<span data-ttu-id="895fe-272">**User**</span><span class="sxs-lookup"><span data-stu-id="895fe-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="895fe-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="895fe-273">Windows Server 2012</span></span>



| <span data-ttu-id="895fe-274">進入</span><span class="sxs-lookup"><span data-stu-id="895fe-274">Entry</span></span> | <span data-ttu-id="895fe-275">值</span><span class="sxs-lookup"><span data-stu-id="895fe-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="895fe-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="895fe-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="895fe-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="895fe-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="895fe-278">System-Only</span></span>            | <span data-ttu-id="895fe-279">否</span><span class="sxs-lookup"><span data-stu-id="895fe-279">False</span></span>                             |
| <span data-ttu-id="895fe-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="895fe-280">Is-Single-Valued</span></span>       | <span data-ttu-id="895fe-281">對</span><span class="sxs-lookup"><span data-stu-id="895fe-281">True</span></span>                              |
| <span data-ttu-id="895fe-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="895fe-282">Is Indexed</span></span>             | <span data-ttu-id="895fe-283">對</span><span class="sxs-lookup"><span data-stu-id="895fe-283">True</span></span>                              |
| <span data-ttu-id="895fe-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="895fe-284">In Global Catalog</span></span>      | <span data-ttu-id="895fe-285">對</span><span class="sxs-lookup"><span data-stu-id="895fe-285">True</span></span>                              |
| <span data-ttu-id="895fe-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="895fe-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="895fe-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="895fe-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="895fe-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="895fe-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="895fe-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="895fe-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="895fe-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-290">Search-Flags</span></span>           | <span data-ttu-id="895fe-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="895fe-291">0x00000001</span></span>                        |
| <span data-ttu-id="895fe-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="895fe-292">System-Flags</span></span>           | <span data-ttu-id="895fe-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="895fe-293">0x00000012</span></span>                        |
| <span data-ttu-id="895fe-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="895fe-294">Classes used in</span></span>        | [<span data-ttu-id="895fe-295">**User**</span><span class="sxs-lookup"><span data-stu-id="895fe-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="895fe-296">備註</span><span class="sxs-lookup"><span data-stu-id="895fe-296">Remarks</span></span>

<span data-ttu-id="895fe-297">在 ADAM 中，此屬性不需要採用網際網路標準 RFC 822 格式;它可以是簡單名稱。</span><span class="sxs-lookup"><span data-stu-id="895fe-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 

