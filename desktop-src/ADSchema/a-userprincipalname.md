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
# <a name="user-principal-name-attribute"></a><span data-ttu-id="bc9af-105">使用者主體名稱屬性</span><span class="sxs-lookup"><span data-stu-id="bc9af-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="bc9af-106">此屬性包含 UPN，其為以網際網路標準 [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)為基礎之使用者的網際網路樣式登入名稱。</span><span class="sxs-lookup"><span data-stu-id="bc9af-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="bc9af-107">UPN 比分辨名稱短，而且更容易記住。</span><span class="sxs-lookup"><span data-stu-id="bc9af-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="bc9af-108">依照慣例，這應該對應到使用者的電子郵件名稱。</span><span class="sxs-lookup"><span data-stu-id="bc9af-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="bc9af-109">為此屬性設定的值等於使用者識別碼和功能變數名稱的長度。</span><span class="sxs-lookup"><span data-stu-id="bc9af-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="bc9af-110">如需此屬性的詳細資訊，請參閱 [使用者命名屬性](/windows/desktop/AD/naming-properties)。</span><span class="sxs-lookup"><span data-stu-id="bc9af-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="bc9af-111">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-111">Entry</span></span> | <span data-ttu-id="bc9af-112">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bc9af-113">CN</span><span class="sxs-lookup"><span data-stu-id="bc9af-113">CN</span></span>                | <span data-ttu-id="bc9af-114">使用者主體名稱</span><span class="sxs-lookup"><span data-stu-id="bc9af-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="bc9af-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bc9af-115">Ldap-Display-Name</span></span> | <span data-ttu-id="bc9af-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bc9af-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="bc9af-117">大小</span><span class="sxs-lookup"><span data-stu-id="bc9af-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="bc9af-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bc9af-118">Update Privilege</span></span>  | <span data-ttu-id="bc9af-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="bc9af-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="bc9af-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bc9af-120">Update Frequency</span></span>  | <span data-ttu-id="bc9af-121">理論上，這絕對不會改變。</span><span class="sxs-lookup"><span data-stu-id="bc9af-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="bc9af-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-122">Attribute-Id</span></span>      | <span data-ttu-id="bc9af-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="bc9af-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="bc9af-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bc9af-124">System-Id-Guid</span></span>    | <span data-ttu-id="bc9af-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="bc9af-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="bc9af-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc9af-126">Syntax</span></span>            | [<span data-ttu-id="bc9af-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bc9af-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bc9af-128">實作</span><span class="sxs-lookup"><span data-stu-id="bc9af-128">Implementations</span></span>

-   [<span data-ttu-id="bc9af-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bc9af-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bc9af-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc9af-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc9af-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="bc9af-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bc9af-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc9af-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc9af-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc9af-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc9af-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc9af-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc9af-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc9af-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bc9af-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc9af-136">Windows 2000 Server</span></span>



| <span data-ttu-id="bc9af-137">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-137">Entry</span></span> | <span data-ttu-id="bc9af-138">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc9af-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bc9af-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc9af-141">System-Only</span></span>            | <span data-ttu-id="bc9af-142">否</span><span class="sxs-lookup"><span data-stu-id="bc9af-142">False</span></span>                             |
| <span data-ttu-id="bc9af-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bc9af-143">Is-Single-Valued</span></span>       | <span data-ttu-id="bc9af-144">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-144">True</span></span>                              |
| <span data-ttu-id="bc9af-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bc9af-145">Is Indexed</span></span>             | <span data-ttu-id="bc9af-146">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-146">True</span></span>                              |
| <span data-ttu-id="bc9af-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bc9af-147">In Global Catalog</span></span>      | <span data-ttu-id="bc9af-148">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-148">True</span></span>                              |
| <span data-ttu-id="bc9af-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bc9af-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc9af-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bc9af-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc9af-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc9af-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc9af-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc9af-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc9af-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-153">Search-Flags</span></span>           | <span data-ttu-id="bc9af-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc9af-154">0x00000001</span></span>                        |
| <span data-ttu-id="bc9af-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-155">System-Flags</span></span>           | <span data-ttu-id="bc9af-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bc9af-156">0x00000012</span></span>                        |
| <span data-ttu-id="bc9af-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bc9af-157">Classes used in</span></span>        | [<span data-ttu-id="bc9af-158">**User**</span><span class="sxs-lookup"><span data-stu-id="bc9af-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bc9af-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc9af-159">Windows Server 2003</span></span>



| <span data-ttu-id="bc9af-160">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-160">Entry</span></span> | <span data-ttu-id="bc9af-161">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc9af-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bc9af-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc9af-164">System-Only</span></span>            | <span data-ttu-id="bc9af-165">否</span><span class="sxs-lookup"><span data-stu-id="bc9af-165">False</span></span>                             |
| <span data-ttu-id="bc9af-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bc9af-166">Is-Single-Valued</span></span>       | <span data-ttu-id="bc9af-167">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-167">True</span></span>                              |
| <span data-ttu-id="bc9af-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bc9af-168">Is Indexed</span></span>             | <span data-ttu-id="bc9af-169">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-169">True</span></span>                              |
| <span data-ttu-id="bc9af-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bc9af-170">In Global Catalog</span></span>      | <span data-ttu-id="bc9af-171">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-171">True</span></span>                              |
| <span data-ttu-id="bc9af-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bc9af-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc9af-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bc9af-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc9af-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc9af-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc9af-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc9af-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc9af-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-176">Search-Flags</span></span>           | <span data-ttu-id="bc9af-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc9af-177">0x00000001</span></span>                        |
| <span data-ttu-id="bc9af-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-178">System-Flags</span></span>           | <span data-ttu-id="bc9af-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bc9af-179">0x00000012</span></span>                        |
| <span data-ttu-id="bc9af-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bc9af-180">Classes used in</span></span>        | [<span data-ttu-id="bc9af-181">**User**</span><span class="sxs-lookup"><span data-stu-id="bc9af-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bc9af-182">亞當</span><span class="sxs-lookup"><span data-stu-id="bc9af-182">ADAM</span></span>



| <span data-ttu-id="bc9af-183">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-183">Entry</span></span> | <span data-ttu-id="bc9af-184">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="bc9af-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bc9af-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="bc9af-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="bc9af-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc9af-187">System-Only</span></span>            | <span data-ttu-id="bc9af-188">否</span><span class="sxs-lookup"><span data-stu-id="bc9af-188">False</span></span>        |
| <span data-ttu-id="bc9af-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bc9af-189">Is-Single-Valued</span></span>       | <span data-ttu-id="bc9af-190">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-190">True</span></span>         |
| <span data-ttu-id="bc9af-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bc9af-191">Is Indexed</span></span>             | <span data-ttu-id="bc9af-192">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-192">True</span></span>         |
| <span data-ttu-id="bc9af-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bc9af-193">In Global Catalog</span></span>      | <span data-ttu-id="bc9af-194">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-194">True</span></span>         |
| <span data-ttu-id="bc9af-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bc9af-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc9af-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bc9af-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="bc9af-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc9af-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="bc9af-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc9af-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="bc9af-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-199">Search-Flags</span></span>           | <span data-ttu-id="bc9af-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc9af-200">0x00000001</span></span>   |
| <span data-ttu-id="bc9af-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-201">System-Flags</span></span>           | <span data-ttu-id="bc9af-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bc9af-202">0x00000012</span></span>   |
| <span data-ttu-id="bc9af-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bc9af-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc9af-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc9af-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc9af-205">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-205">Entry</span></span> | <span data-ttu-id="bc9af-206">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc9af-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bc9af-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc9af-209">System-Only</span></span>            | <span data-ttu-id="bc9af-210">否</span><span class="sxs-lookup"><span data-stu-id="bc9af-210">False</span></span>                             |
| <span data-ttu-id="bc9af-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bc9af-211">Is-Single-Valued</span></span>       | <span data-ttu-id="bc9af-212">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-212">True</span></span>                              |
| <span data-ttu-id="bc9af-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bc9af-213">Is Indexed</span></span>             | <span data-ttu-id="bc9af-214">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-214">True</span></span>                              |
| <span data-ttu-id="bc9af-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bc9af-215">In Global Catalog</span></span>      | <span data-ttu-id="bc9af-216">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-216">True</span></span>                              |
| <span data-ttu-id="bc9af-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bc9af-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc9af-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bc9af-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc9af-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc9af-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc9af-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc9af-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc9af-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-221">Search-Flags</span></span>           | <span data-ttu-id="bc9af-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc9af-222">0x00000001</span></span>                        |
| <span data-ttu-id="bc9af-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-223">System-Flags</span></span>           | <span data-ttu-id="bc9af-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bc9af-224">0x00000012</span></span>                        |
| <span data-ttu-id="bc9af-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bc9af-225">Classes used in</span></span>        | [<span data-ttu-id="bc9af-226">**User**</span><span class="sxs-lookup"><span data-stu-id="bc9af-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc9af-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc9af-227">Windows Server 2008</span></span>



| <span data-ttu-id="bc9af-228">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-228">Entry</span></span> | <span data-ttu-id="bc9af-229">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc9af-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bc9af-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc9af-232">System-Only</span></span>            | <span data-ttu-id="bc9af-233">否</span><span class="sxs-lookup"><span data-stu-id="bc9af-233">False</span></span>                             |
| <span data-ttu-id="bc9af-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bc9af-234">Is-Single-Valued</span></span>       | <span data-ttu-id="bc9af-235">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-235">True</span></span>                              |
| <span data-ttu-id="bc9af-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bc9af-236">Is Indexed</span></span>             | <span data-ttu-id="bc9af-237">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-237">True</span></span>                              |
| <span data-ttu-id="bc9af-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bc9af-238">In Global Catalog</span></span>      | <span data-ttu-id="bc9af-239">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-239">True</span></span>                              |
| <span data-ttu-id="bc9af-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bc9af-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc9af-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bc9af-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc9af-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc9af-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc9af-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc9af-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc9af-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-244">Search-Flags</span></span>           | <span data-ttu-id="bc9af-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc9af-245">0x00000001</span></span>                        |
| <span data-ttu-id="bc9af-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-246">System-Flags</span></span>           | <span data-ttu-id="bc9af-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bc9af-247">0x00000012</span></span>                        |
| <span data-ttu-id="bc9af-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bc9af-248">Classes used in</span></span>        | [<span data-ttu-id="bc9af-249">**User**</span><span class="sxs-lookup"><span data-stu-id="bc9af-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc9af-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc9af-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc9af-251">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-251">Entry</span></span> | <span data-ttu-id="bc9af-252">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc9af-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bc9af-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc9af-255">System-Only</span></span>            | <span data-ttu-id="bc9af-256">否</span><span class="sxs-lookup"><span data-stu-id="bc9af-256">False</span></span>                             |
| <span data-ttu-id="bc9af-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bc9af-257">Is-Single-Valued</span></span>       | <span data-ttu-id="bc9af-258">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-258">True</span></span>                              |
| <span data-ttu-id="bc9af-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bc9af-259">Is Indexed</span></span>             | <span data-ttu-id="bc9af-260">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-260">True</span></span>                              |
| <span data-ttu-id="bc9af-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bc9af-261">In Global Catalog</span></span>      | <span data-ttu-id="bc9af-262">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-262">True</span></span>                              |
| <span data-ttu-id="bc9af-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bc9af-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc9af-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bc9af-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc9af-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc9af-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc9af-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc9af-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc9af-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-267">Search-Flags</span></span>           | <span data-ttu-id="bc9af-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc9af-268">0x00000001</span></span>                        |
| <span data-ttu-id="bc9af-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-269">System-Flags</span></span>           | <span data-ttu-id="bc9af-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bc9af-270">0x00000012</span></span>                        |
| <span data-ttu-id="bc9af-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bc9af-271">Classes used in</span></span>        | [<span data-ttu-id="bc9af-272">**User**</span><span class="sxs-lookup"><span data-stu-id="bc9af-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc9af-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc9af-273">Windows Server 2012</span></span>



| <span data-ttu-id="bc9af-274">進入</span><span class="sxs-lookup"><span data-stu-id="bc9af-274">Entry</span></span> | <span data-ttu-id="bc9af-275">值</span><span class="sxs-lookup"><span data-stu-id="bc9af-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bc9af-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bc9af-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc9af-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bc9af-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc9af-278">System-Only</span></span>            | <span data-ttu-id="bc9af-279">否</span><span class="sxs-lookup"><span data-stu-id="bc9af-279">False</span></span>                             |
| <span data-ttu-id="bc9af-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bc9af-280">Is-Single-Valued</span></span>       | <span data-ttu-id="bc9af-281">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-281">True</span></span>                              |
| <span data-ttu-id="bc9af-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bc9af-282">Is Indexed</span></span>             | <span data-ttu-id="bc9af-283">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-283">True</span></span>                              |
| <span data-ttu-id="bc9af-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bc9af-284">In Global Catalog</span></span>      | <span data-ttu-id="bc9af-285">對</span><span class="sxs-lookup"><span data-stu-id="bc9af-285">True</span></span>                              |
| <span data-ttu-id="bc9af-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bc9af-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc9af-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bc9af-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bc9af-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc9af-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bc9af-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc9af-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bc9af-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-290">Search-Flags</span></span>           | <span data-ttu-id="bc9af-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bc9af-291">0x00000001</span></span>                        |
| <span data-ttu-id="bc9af-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc9af-292">System-Flags</span></span>           | <span data-ttu-id="bc9af-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bc9af-293">0x00000012</span></span>                        |
| <span data-ttu-id="bc9af-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bc9af-294">Classes used in</span></span>        | [<span data-ttu-id="bc9af-295">**User**</span><span class="sxs-lookup"><span data-stu-id="bc9af-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bc9af-296">備註</span><span class="sxs-lookup"><span data-stu-id="bc9af-296">Remarks</span></span>

<span data-ttu-id="bc9af-297">在 ADAM 中，此屬性不需要採用網際網路標準 RFC 822 格式;它可以是簡單名稱。</span><span class="sxs-lookup"><span data-stu-id="bc9af-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 

