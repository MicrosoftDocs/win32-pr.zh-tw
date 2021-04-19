---
title: Country-Code 屬性
description: 指定使用者選擇之語言的國家/地區代碼。 Windows 2000 不會使用這個值。
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Country-Code 屬性 AD 架構
- countryCode 屬性 AD 架構
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970671"
---
# <a name="country-code-attribute"></a><span data-ttu-id="329f7-106">Country-Code 屬性</span><span class="sxs-lookup"><span data-stu-id="329f7-106">Country-Code attribute</span></span>

<span data-ttu-id="329f7-107">指定使用者選擇之語言的國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="329f7-107">Specifies the country/region code for the user's language of choice.</span></span> <span data-ttu-id="329f7-108">Windows 2000 不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="329f7-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="329f7-109">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-109">Entry</span></span> | <span data-ttu-id="329f7-110">值</span><span class="sxs-lookup"><span data-stu-id="329f7-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="329f7-111">CN</span><span class="sxs-lookup"><span data-stu-id="329f7-111">CN</span></span>                | <span data-ttu-id="329f7-112">Country-Code</span><span class="sxs-lookup"><span data-stu-id="329f7-112">Country-Code</span></span>                            |
| <span data-ttu-id="329f7-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="329f7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="329f7-114">countryCode</span><span class="sxs-lookup"><span data-stu-id="329f7-114">countryCode</span></span>                             |
| <span data-ttu-id="329f7-115">大小</span><span class="sxs-lookup"><span data-stu-id="329f7-115">Size</span></span>              | <span data-ttu-id="329f7-116">2 個位元組</span><span class="sxs-lookup"><span data-stu-id="329f7-116">2 bytes</span></span>                                 |
| <span data-ttu-id="329f7-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="329f7-117">Update Privilege</span></span>  | <span data-ttu-id="329f7-118">帳戶擁有者或網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="329f7-118">Account owner or domain administrator</span></span>   |
| <span data-ttu-id="329f7-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="329f7-119">Update Frequency</span></span>  | <span data-ttu-id="329f7-120">當使用者的國家/地區變更時。</span><span class="sxs-lookup"><span data-stu-id="329f7-120">When the user's country/region changes.</span></span> |
| <span data-ttu-id="329f7-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-121">Attribute-Id</span></span>      | <span data-ttu-id="329f7-122">1.2.840.113556.1.4.25</span><span class="sxs-lookup"><span data-stu-id="329f7-122">1.2.840.113556.1.4.25</span></span>                   |
| <span data-ttu-id="329f7-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="329f7-123">System-Id-Guid</span></span>    | <span data-ttu-id="329f7-124">5fd42471-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="329f7-124">5fd42471-1262-11d0-a060-00aa006c33ed</span></span>    |
| <span data-ttu-id="329f7-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="329f7-125">Syntax</span></span>            | [<span data-ttu-id="329f7-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="329f7-126">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="329f7-127">實作</span><span class="sxs-lookup"><span data-stu-id="329f7-127">Implementations</span></span>

-   [<span data-ttu-id="329f7-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="329f7-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="329f7-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="329f7-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="329f7-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="329f7-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="329f7-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="329f7-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="329f7-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="329f7-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="329f7-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="329f7-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="329f7-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="329f7-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="329f7-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="329f7-135">Windows 2000 Server</span></span>



| <span data-ttu-id="329f7-136">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-136">Entry</span></span> | <span data-ttu-id="329f7-137">值</span><span class="sxs-lookup"><span data-stu-id="329f7-137">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329f7-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="329f7-138">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-139">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="329f7-140">System-Only</span></span>            | <span data-ttu-id="329f7-141">否</span><span class="sxs-lookup"><span data-stu-id="329f7-141">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="329f7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="329f7-143">對</span><span class="sxs-lookup"><span data-stu-id="329f7-143">True</span></span>                                                                                                                              |
| <span data-ttu-id="329f7-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="329f7-144">Is Indexed</span></span>             | <span data-ttu-id="329f7-145">否</span><span class="sxs-lookup"><span data-stu-id="329f7-145">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="329f7-146">In Global Catalog</span></span>      | <span data-ttu-id="329f7-147">否</span><span class="sxs-lookup"><span data-stu-id="329f7-147">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="329f7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="329f7-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="329f7-149">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="329f7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="329f7-150">Range-Lower</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="329f7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="329f7-151">Range-Upper</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="329f7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-152">Search-Flags</span></span>           | <span data-ttu-id="329f7-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-153">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-154">System-Flags</span></span>           | <span data-ttu-id="329f7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-155">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="329f7-156">Classes used in</span></span>        | [<span data-ttu-id="329f7-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="329f7-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="329f7-158">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="329f7-158">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="329f7-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="329f7-159">Windows Server 2003</span></span>



| <span data-ttu-id="329f7-160">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-160">Entry</span></span> | <span data-ttu-id="329f7-161">值</span><span class="sxs-lookup"><span data-stu-id="329f7-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329f7-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="329f7-162">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-163">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="329f7-164">System-Only</span></span>            | <span data-ttu-id="329f7-165">否</span><span class="sxs-lookup"><span data-stu-id="329f7-165">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="329f7-166">Is-Single-Valued</span></span>       | <span data-ttu-id="329f7-167">對</span><span class="sxs-lookup"><span data-stu-id="329f7-167">True</span></span>                                                                                                                              |
| <span data-ttu-id="329f7-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="329f7-168">Is Indexed</span></span>             | <span data-ttu-id="329f7-169">否</span><span class="sxs-lookup"><span data-stu-id="329f7-169">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="329f7-170">In Global Catalog</span></span>      | <span data-ttu-id="329f7-171">否</span><span class="sxs-lookup"><span data-stu-id="329f7-171">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="329f7-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="329f7-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="329f7-173">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="329f7-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="329f7-174">Range-Lower</span></span>            | <span data-ttu-id="329f7-175">0</span><span class="sxs-lookup"><span data-stu-id="329f7-175">0</span></span>                                                                                                                                 |
| <span data-ttu-id="329f7-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="329f7-176">Range-Upper</span></span>            | <span data-ttu-id="329f7-177">65535</span><span class="sxs-lookup"><span data-stu-id="329f7-177">65535</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-178">Search-Flags</span></span>           | <span data-ttu-id="329f7-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-179">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-180">System-Flags</span></span>           | <span data-ttu-id="329f7-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-181">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="329f7-182">Classes used in</span></span>        | [<span data-ttu-id="329f7-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="329f7-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="329f7-184">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="329f7-184">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="329f7-185">亞當</span><span class="sxs-lookup"><span data-stu-id="329f7-185">ADAM</span></span>



| <span data-ttu-id="329f7-186">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-186">Entry</span></span> | <span data-ttu-id="329f7-187">值</span><span class="sxs-lookup"><span data-stu-id="329f7-187">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="329f7-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="329f7-188">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="329f7-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-189">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="329f7-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="329f7-190">System-Only</span></span>            | <span data-ttu-id="329f7-191">否</span><span class="sxs-lookup"><span data-stu-id="329f7-191">False</span></span>                                                          |
| <span data-ttu-id="329f7-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="329f7-192">Is-Single-Valued</span></span>       | <span data-ttu-id="329f7-193">對</span><span class="sxs-lookup"><span data-stu-id="329f7-193">True</span></span>                                                           |
| <span data-ttu-id="329f7-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="329f7-194">Is Indexed</span></span>             | <span data-ttu-id="329f7-195">否</span><span class="sxs-lookup"><span data-stu-id="329f7-195">False</span></span>                                                          |
| <span data-ttu-id="329f7-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="329f7-196">In Global Catalog</span></span>      | <span data-ttu-id="329f7-197">否</span><span class="sxs-lookup"><span data-stu-id="329f7-197">False</span></span>                                                          |
| <span data-ttu-id="329f7-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="329f7-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="329f7-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="329f7-199">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="329f7-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="329f7-200">Range-Lower</span></span>            | <span data-ttu-id="329f7-201">0</span><span class="sxs-lookup"><span data-stu-id="329f7-201">0</span></span>                                                              |
| <span data-ttu-id="329f7-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="329f7-202">Range-Upper</span></span>            | <span data-ttu-id="329f7-203">65535</span><span class="sxs-lookup"><span data-stu-id="329f7-203">65535</span></span>                                                          |
| <span data-ttu-id="329f7-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-204">Search-Flags</span></span>           | <span data-ttu-id="329f7-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-205">0x00000010</span></span>                                                     |
| <span data-ttu-id="329f7-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-206">System-Flags</span></span>           | <span data-ttu-id="329f7-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-207">0x00000010</span></span>                                                     |
| <span data-ttu-id="329f7-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="329f7-208">Classes used in</span></span>        | [<span data-ttu-id="329f7-209">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="329f7-209">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="329f7-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="329f7-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="329f7-211">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-211">Entry</span></span> | <span data-ttu-id="329f7-212">值</span><span class="sxs-lookup"><span data-stu-id="329f7-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329f7-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="329f7-213">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-214">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="329f7-215">System-Only</span></span>            | <span data-ttu-id="329f7-216">否</span><span class="sxs-lookup"><span data-stu-id="329f7-216">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="329f7-217">Is-Single-Valued</span></span>       | <span data-ttu-id="329f7-218">對</span><span class="sxs-lookup"><span data-stu-id="329f7-218">True</span></span>                                                                                                                              |
| <span data-ttu-id="329f7-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="329f7-219">Is Indexed</span></span>             | <span data-ttu-id="329f7-220">否</span><span class="sxs-lookup"><span data-stu-id="329f7-220">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="329f7-221">In Global Catalog</span></span>      | <span data-ttu-id="329f7-222">否</span><span class="sxs-lookup"><span data-stu-id="329f7-222">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="329f7-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="329f7-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="329f7-224">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="329f7-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="329f7-225">Range-Lower</span></span>            | <span data-ttu-id="329f7-226">0</span><span class="sxs-lookup"><span data-stu-id="329f7-226">0</span></span>                                                                                                                                 |
| <span data-ttu-id="329f7-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="329f7-227">Range-Upper</span></span>            | <span data-ttu-id="329f7-228">65535</span><span class="sxs-lookup"><span data-stu-id="329f7-228">65535</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-229">Search-Flags</span></span>           | <span data-ttu-id="329f7-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-230">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-231">System-Flags</span></span>           | <span data-ttu-id="329f7-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-232">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="329f7-233">Classes used in</span></span>        | [<span data-ttu-id="329f7-234">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="329f7-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="329f7-235">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="329f7-235">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="329f7-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="329f7-236">Windows Server 2008</span></span>



| <span data-ttu-id="329f7-237">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-237">Entry</span></span> | <span data-ttu-id="329f7-238">值</span><span class="sxs-lookup"><span data-stu-id="329f7-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329f7-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="329f7-239">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-240">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="329f7-241">System-Only</span></span>            | <span data-ttu-id="329f7-242">否</span><span class="sxs-lookup"><span data-stu-id="329f7-242">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="329f7-243">Is-Single-Valued</span></span>       | <span data-ttu-id="329f7-244">對</span><span class="sxs-lookup"><span data-stu-id="329f7-244">True</span></span>                                                                                                                              |
| <span data-ttu-id="329f7-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="329f7-245">Is Indexed</span></span>             | <span data-ttu-id="329f7-246">否</span><span class="sxs-lookup"><span data-stu-id="329f7-246">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="329f7-247">In Global Catalog</span></span>      | <span data-ttu-id="329f7-248">否</span><span class="sxs-lookup"><span data-stu-id="329f7-248">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="329f7-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="329f7-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="329f7-250">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="329f7-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="329f7-251">Range-Lower</span></span>            | <span data-ttu-id="329f7-252">0</span><span class="sxs-lookup"><span data-stu-id="329f7-252">0</span></span>                                                                                                                                 |
| <span data-ttu-id="329f7-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="329f7-253">Range-Upper</span></span>            | <span data-ttu-id="329f7-254">65535</span><span class="sxs-lookup"><span data-stu-id="329f7-254">65535</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-255">Search-Flags</span></span>           | <span data-ttu-id="329f7-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-256">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-257">System-Flags</span></span>           | <span data-ttu-id="329f7-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-258">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="329f7-259">Classes used in</span></span>        | [<span data-ttu-id="329f7-260">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="329f7-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="329f7-261">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="329f7-261">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="329f7-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="329f7-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="329f7-263">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-263">Entry</span></span> | <span data-ttu-id="329f7-264">值</span><span class="sxs-lookup"><span data-stu-id="329f7-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329f7-265">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="329f7-265">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-266">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="329f7-267">System-Only</span></span>            | <span data-ttu-id="329f7-268">否</span><span class="sxs-lookup"><span data-stu-id="329f7-268">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="329f7-269">Is-Single-Valued</span></span>       | <span data-ttu-id="329f7-270">對</span><span class="sxs-lookup"><span data-stu-id="329f7-270">True</span></span>                                                                                                                              |
| <span data-ttu-id="329f7-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="329f7-271">Is Indexed</span></span>             | <span data-ttu-id="329f7-272">否</span><span class="sxs-lookup"><span data-stu-id="329f7-272">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="329f7-273">In Global Catalog</span></span>      | <span data-ttu-id="329f7-274">否</span><span class="sxs-lookup"><span data-stu-id="329f7-274">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="329f7-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="329f7-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="329f7-276">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="329f7-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="329f7-277">Range-Lower</span></span>            | <span data-ttu-id="329f7-278">0</span><span class="sxs-lookup"><span data-stu-id="329f7-278">0</span></span>                                                                                                                                 |
| <span data-ttu-id="329f7-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="329f7-279">Range-Upper</span></span>            | <span data-ttu-id="329f7-280">65535</span><span class="sxs-lookup"><span data-stu-id="329f7-280">65535</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-281">Search-Flags</span></span>           | <span data-ttu-id="329f7-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-282">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-283">System-Flags</span></span>           | <span data-ttu-id="329f7-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-284">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="329f7-285">Classes used in</span></span>        | [<span data-ttu-id="329f7-286">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="329f7-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="329f7-287">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="329f7-287">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="329f7-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="329f7-288">Windows Server 2012</span></span>



| <span data-ttu-id="329f7-289">進入</span><span class="sxs-lookup"><span data-stu-id="329f7-289">Entry</span></span> | <span data-ttu-id="329f7-290">值</span><span class="sxs-lookup"><span data-stu-id="329f7-290">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329f7-291">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="329f7-291">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="329f7-292">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="329f7-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="329f7-293">System-Only</span></span>            | <span data-ttu-id="329f7-294">否</span><span class="sxs-lookup"><span data-stu-id="329f7-294">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-295">是-單一值</span><span class="sxs-lookup"><span data-stu-id="329f7-295">Is-Single-Valued</span></span>       | <span data-ttu-id="329f7-296">對</span><span class="sxs-lookup"><span data-stu-id="329f7-296">True</span></span>                                                                                                                              |
| <span data-ttu-id="329f7-297">已編制索引</span><span class="sxs-lookup"><span data-stu-id="329f7-297">Is Indexed</span></span>             | <span data-ttu-id="329f7-298">否</span><span class="sxs-lookup"><span data-stu-id="329f7-298">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-299">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="329f7-299">In Global Catalog</span></span>      | <span data-ttu-id="329f7-300">否</span><span class="sxs-lookup"><span data-stu-id="329f7-300">False</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-301">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="329f7-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="329f7-302">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="329f7-302">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="329f7-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="329f7-303">Range-Lower</span></span>            | <span data-ttu-id="329f7-304">0</span><span class="sxs-lookup"><span data-stu-id="329f7-304">0</span></span>                                                                                                                                 |
| <span data-ttu-id="329f7-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="329f7-305">Range-Upper</span></span>            | <span data-ttu-id="329f7-306">65535</span><span class="sxs-lookup"><span data-stu-id="329f7-306">65535</span></span>                                                                                                                             |
| <span data-ttu-id="329f7-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-307">Search-Flags</span></span>           | <span data-ttu-id="329f7-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-308">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="329f7-309">System-Flags</span></span>           | <span data-ttu-id="329f7-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="329f7-310">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="329f7-311">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="329f7-311">Classes used in</span></span>        | [<span data-ttu-id="329f7-312">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="329f7-312">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="329f7-313">**組織單位**</span><span class="sxs-lookup"><span data-stu-id="329f7-313">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





