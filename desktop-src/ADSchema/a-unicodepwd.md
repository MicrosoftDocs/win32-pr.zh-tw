---
title: Unicode-Pwd 屬性
description: Windows NT 單向格式的使用者密碼 (OWF) 。 Windows 2000 使用 Windows NT OWF。 這個屬性僅供作業系統使用。 請注意，您無法從密碼的 OWF 形式衍生出純文字密碼。
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Unicode-Pwd 屬性 AD 架構
- unicodePwd 屬性 AD 架構
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107929"
---
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="e9cde-108">Unicode-Pwd 屬性</span><span class="sxs-lookup"><span data-stu-id="e9cde-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="e9cde-109">Windows NT 單向格式的使用者密碼 (OWF) 。</span><span class="sxs-lookup"><span data-stu-id="e9cde-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="e9cde-110">Windows 2000 使用 Windows NT OWF。</span><span class="sxs-lookup"><span data-stu-id="e9cde-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="e9cde-111">這個屬性僅供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="e9cde-111">This property is used only by the operating system.</span></span> <span data-ttu-id="e9cde-112">請注意，您無法從密碼的 OWF 形式衍生出純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="e9cde-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="e9cde-113">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-113">Entry</span></span> | <span data-ttu-id="e9cde-114">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e9cde-115">CN</span><span class="sxs-lookup"><span data-stu-id="e9cde-115">CN</span></span>                | <span data-ttu-id="e9cde-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="e9cde-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="e9cde-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e9cde-117">Ldap-Display-Name</span></span> | <span data-ttu-id="e9cde-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="e9cde-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="e9cde-119">大小</span><span class="sxs-lookup"><span data-stu-id="e9cde-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="e9cde-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e9cde-120">Update Privilege</span></span>  | <span data-ttu-id="e9cde-121">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="e9cde-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="e9cde-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e9cde-122">Update Frequency</span></span>  | <span data-ttu-id="e9cde-123">當使用者的記錄建立時，以及每次需要變更密碼時。</span><span class="sxs-lookup"><span data-stu-id="e9cde-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="e9cde-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-124">Attribute-Id</span></span>      | <span data-ttu-id="e9cde-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="e9cde-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="e9cde-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e9cde-126">System-Id-Guid</span></span>    | <span data-ttu-id="e9cde-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e9cde-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="e9cde-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9cde-128">Syntax</span></span>            | [<span data-ttu-id="e9cde-129">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e9cde-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="e9cde-130">實作</span><span class="sxs-lookup"><span data-stu-id="e9cde-130">Implementations</span></span>

-   [<span data-ttu-id="e9cde-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9cde-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9cde-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9cde-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9cde-133">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e9cde-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e9cde-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9cde-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9cde-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9cde-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9cde-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9cde-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9cde-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9cde-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9cde-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9cde-138">Windows 2000 Server</span></span>



| <span data-ttu-id="e9cde-139">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-139">Entry</span></span> | <span data-ttu-id="e9cde-140">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9cde-141">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e9cde-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9cde-143">System-Only</span></span>            | <span data-ttu-id="e9cde-144">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-144">False</span></span>                             |
| <span data-ttu-id="e9cde-145">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e9cde-145">Is-Single-Valued</span></span>       | <span data-ttu-id="e9cde-146">對</span><span class="sxs-lookup"><span data-stu-id="e9cde-146">True</span></span>                              |
| <span data-ttu-id="e9cde-147">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e9cde-147">Is Indexed</span></span>             | <span data-ttu-id="e9cde-148">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-148">False</span></span>                             |
| <span data-ttu-id="e9cde-149">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e9cde-149">In Global Catalog</span></span>      | <span data-ttu-id="e9cde-150">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-150">False</span></span>                             |
| <span data-ttu-id="e9cde-151">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e9cde-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9cde-152">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e9cde-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9cde-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9cde-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9cde-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9cde-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9cde-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-155">Search-Flags</span></span>           | <span data-ttu-id="e9cde-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9cde-156">0x00000000</span></span>                        |
| <span data-ttu-id="e9cde-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-157">System-Flags</span></span>           | <span data-ttu-id="e9cde-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9cde-158">0x00000010</span></span>                        |
| <span data-ttu-id="e9cde-159">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e9cde-159">Classes used in</span></span>        | [<span data-ttu-id="e9cde-160">**User**</span><span class="sxs-lookup"><span data-stu-id="e9cde-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9cde-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9cde-161">Windows Server 2003</span></span>



| <span data-ttu-id="e9cde-162">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-162">Entry</span></span> | <span data-ttu-id="e9cde-163">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9cde-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e9cde-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9cde-166">System-Only</span></span>            | <span data-ttu-id="e9cde-167">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-167">False</span></span>                             |
| <span data-ttu-id="e9cde-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e9cde-168">Is-Single-Valued</span></span>       | <span data-ttu-id="e9cde-169">對</span><span class="sxs-lookup"><span data-stu-id="e9cde-169">True</span></span>                              |
| <span data-ttu-id="e9cde-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e9cde-170">Is Indexed</span></span>             | <span data-ttu-id="e9cde-171">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-171">False</span></span>                             |
| <span data-ttu-id="e9cde-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e9cde-172">In Global Catalog</span></span>      | <span data-ttu-id="e9cde-173">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-173">False</span></span>                             |
| <span data-ttu-id="e9cde-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e9cde-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9cde-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e9cde-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9cde-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9cde-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9cde-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9cde-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9cde-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-178">Search-Flags</span></span>           | <span data-ttu-id="e9cde-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9cde-179">0x00000000</span></span>                        |
| <span data-ttu-id="e9cde-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-180">System-Flags</span></span>           | <span data-ttu-id="e9cde-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9cde-181">0x00000010</span></span>                        |
| <span data-ttu-id="e9cde-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e9cde-182">Classes used in</span></span>        | [<span data-ttu-id="e9cde-183">**User**</span><span class="sxs-lookup"><span data-stu-id="e9cde-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e9cde-184">亞當</span><span class="sxs-lookup"><span data-stu-id="e9cde-184">ADAM</span></span>



| <span data-ttu-id="e9cde-185">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-185">Entry</span></span> | <span data-ttu-id="e9cde-186">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e9cde-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e9cde-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e9cde-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e9cde-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9cde-189">System-Only</span></span>            | <span data-ttu-id="e9cde-190">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-190">False</span></span>                                                             |
| <span data-ttu-id="e9cde-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e9cde-191">Is-Single-Valued</span></span>       | <span data-ttu-id="e9cde-192">對</span><span class="sxs-lookup"><span data-stu-id="e9cde-192">True</span></span>                                                              |
| <span data-ttu-id="e9cde-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e9cde-193">Is Indexed</span></span>             | <span data-ttu-id="e9cde-194">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-194">False</span></span>                                                             |
| <span data-ttu-id="e9cde-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e9cde-195">In Global Catalog</span></span>      | <span data-ttu-id="e9cde-196">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-196">False</span></span>                                                             |
| <span data-ttu-id="e9cde-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e9cde-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9cde-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e9cde-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e9cde-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9cde-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e9cde-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9cde-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e9cde-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-201">Search-Flags</span></span>           | <span data-ttu-id="e9cde-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9cde-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="e9cde-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-203">System-Flags</span></span>           | <span data-ttu-id="e9cde-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9cde-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="e9cde-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e9cde-205">Classes used in</span></span>        | [<span data-ttu-id="e9cde-206">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="e9cde-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9cde-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9cde-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9cde-208">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-208">Entry</span></span> | <span data-ttu-id="e9cde-209">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9cde-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e9cde-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9cde-212">System-Only</span></span>            | <span data-ttu-id="e9cde-213">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-213">False</span></span>                             |
| <span data-ttu-id="e9cde-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e9cde-214">Is-Single-Valued</span></span>       | <span data-ttu-id="e9cde-215">對</span><span class="sxs-lookup"><span data-stu-id="e9cde-215">True</span></span>                              |
| <span data-ttu-id="e9cde-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e9cde-216">Is Indexed</span></span>             | <span data-ttu-id="e9cde-217">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-217">False</span></span>                             |
| <span data-ttu-id="e9cde-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e9cde-218">In Global Catalog</span></span>      | <span data-ttu-id="e9cde-219">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-219">False</span></span>                             |
| <span data-ttu-id="e9cde-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e9cde-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9cde-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e9cde-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9cde-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9cde-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9cde-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9cde-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9cde-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-224">Search-Flags</span></span>           | <span data-ttu-id="e9cde-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9cde-225">0x00000000</span></span>                        |
| <span data-ttu-id="e9cde-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-226">System-Flags</span></span>           | <span data-ttu-id="e9cde-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9cde-227">0x00000010</span></span>                        |
| <span data-ttu-id="e9cde-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e9cde-228">Classes used in</span></span>        | [<span data-ttu-id="e9cde-229">**User**</span><span class="sxs-lookup"><span data-stu-id="e9cde-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9cde-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9cde-230">Windows Server 2008</span></span>



| <span data-ttu-id="e9cde-231">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-231">Entry</span></span> | <span data-ttu-id="e9cde-232">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9cde-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e9cde-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9cde-235">System-Only</span></span>            | <span data-ttu-id="e9cde-236">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-236">False</span></span>                             |
| <span data-ttu-id="e9cde-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e9cde-237">Is-Single-Valued</span></span>       | <span data-ttu-id="e9cde-238">對</span><span class="sxs-lookup"><span data-stu-id="e9cde-238">True</span></span>                              |
| <span data-ttu-id="e9cde-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e9cde-239">Is Indexed</span></span>             | <span data-ttu-id="e9cde-240">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-240">False</span></span>                             |
| <span data-ttu-id="e9cde-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e9cde-241">In Global Catalog</span></span>      | <span data-ttu-id="e9cde-242">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-242">False</span></span>                             |
| <span data-ttu-id="e9cde-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e9cde-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9cde-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e9cde-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9cde-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9cde-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9cde-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9cde-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9cde-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-247">Search-Flags</span></span>           | <span data-ttu-id="e9cde-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9cde-248">0x00000000</span></span>                        |
| <span data-ttu-id="e9cde-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-249">System-Flags</span></span>           | <span data-ttu-id="e9cde-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9cde-250">0x00000010</span></span>                        |
| <span data-ttu-id="e9cde-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e9cde-251">Classes used in</span></span>        | [<span data-ttu-id="e9cde-252">**User**</span><span class="sxs-lookup"><span data-stu-id="e9cde-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9cde-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9cde-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9cde-254">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-254">Entry</span></span> | <span data-ttu-id="e9cde-255">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9cde-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e9cde-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9cde-258">System-Only</span></span>            | <span data-ttu-id="e9cde-259">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-259">False</span></span>                             |
| <span data-ttu-id="e9cde-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e9cde-260">Is-Single-Valued</span></span>       | <span data-ttu-id="e9cde-261">對</span><span class="sxs-lookup"><span data-stu-id="e9cde-261">True</span></span>                              |
| <span data-ttu-id="e9cde-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e9cde-262">Is Indexed</span></span>             | <span data-ttu-id="e9cde-263">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-263">False</span></span>                             |
| <span data-ttu-id="e9cde-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e9cde-264">In Global Catalog</span></span>      | <span data-ttu-id="e9cde-265">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-265">False</span></span>                             |
| <span data-ttu-id="e9cde-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e9cde-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9cde-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e9cde-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9cde-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9cde-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9cde-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9cde-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9cde-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-270">Search-Flags</span></span>           | <span data-ttu-id="e9cde-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9cde-271">0x00000000</span></span>                        |
| <span data-ttu-id="e9cde-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-272">System-Flags</span></span>           | <span data-ttu-id="e9cde-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9cde-273">0x00000010</span></span>                        |
| <span data-ttu-id="e9cde-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e9cde-274">Classes used in</span></span>        | [<span data-ttu-id="e9cde-275">**User**</span><span class="sxs-lookup"><span data-stu-id="e9cde-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9cde-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9cde-276">Windows Server 2012</span></span>



| <span data-ttu-id="e9cde-277">進入</span><span class="sxs-lookup"><span data-stu-id="e9cde-277">Entry</span></span> | <span data-ttu-id="e9cde-278">值</span><span class="sxs-lookup"><span data-stu-id="e9cde-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9cde-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e9cde-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9cde-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9cde-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9cde-281">System-Only</span></span>            | <span data-ttu-id="e9cde-282">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-282">False</span></span>                             |
| <span data-ttu-id="e9cde-283">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e9cde-283">Is-Single-Valued</span></span>       | <span data-ttu-id="e9cde-284">對</span><span class="sxs-lookup"><span data-stu-id="e9cde-284">True</span></span>                              |
| <span data-ttu-id="e9cde-285">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e9cde-285">Is Indexed</span></span>             | <span data-ttu-id="e9cde-286">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-286">False</span></span>                             |
| <span data-ttu-id="e9cde-287">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e9cde-287">In Global Catalog</span></span>      | <span data-ttu-id="e9cde-288">否</span><span class="sxs-lookup"><span data-stu-id="e9cde-288">False</span></span>                             |
| <span data-ttu-id="e9cde-289">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e9cde-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9cde-290">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e9cde-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9cde-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9cde-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9cde-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9cde-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9cde-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-293">Search-Flags</span></span>           | <span data-ttu-id="e9cde-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9cde-294">0x00000000</span></span>                        |
| <span data-ttu-id="e9cde-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9cde-295">System-Flags</span></span>           | <span data-ttu-id="e9cde-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9cde-296">0x00000010</span></span>                        |
| <span data-ttu-id="e9cde-297">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e9cde-297">Classes used in</span></span>        | [<span data-ttu-id="e9cde-298">**User**</span><span class="sxs-lookup"><span data-stu-id="e9cde-298">**User**</span></span>](c-user.md)<br/> |



 

 





