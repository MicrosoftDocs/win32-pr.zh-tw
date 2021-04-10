---
title: ACS-RSVP-帳戶-檔案-位置屬性
description: RSVP 帳戶檔案的目錄位置。 預設值為 \ 0034; system32 \ 0034;位於預設系統目錄中的子目錄。
ms.assetid: 84303766-0d17-4728-aa61-6a5377b7de04
ms.tgt_platform: multiple
keywords:
- ACS-RSVP-帳戶-檔案-位置屬性 AD 架構
- aCSRSVPAccountFilesLocation 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-RSVP-Account-Files-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40876018ffeeacc49fe666ab1a9d69363edb73c4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845644"
---
# <a name="acs-rsvp-account-files-location-attribute"></a><span data-ttu-id="4bca8-106">ACS-RSVP-帳戶-檔案-位置屬性</span><span class="sxs-lookup"><span data-stu-id="4bca8-106">ACS-RSVP-Account-Files-Location attribute</span></span>

<span data-ttu-id="4bca8-107">RSVP 帳戶檔案的目錄位置。</span><span class="sxs-lookup"><span data-stu-id="4bca8-107">The directory location of RSVP account files.</span></span> <span data-ttu-id="4bca8-108">預設為位於預設系統目錄中的 "system32" 子目錄。</span><span class="sxs-lookup"><span data-stu-id="4bca8-108">Defaults to the "system32" subdirectory located in the default system directory.</span></span>



| <span data-ttu-id="4bca8-109">進入</span><span class="sxs-lookup"><span data-stu-id="4bca8-109">Entry</span></span> | <span data-ttu-id="4bca8-110">值</span><span class="sxs-lookup"><span data-stu-id="4bca8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4bca8-111">CN</span><span class="sxs-lookup"><span data-stu-id="4bca8-111">CN</span></span>                | <span data-ttu-id="4bca8-112">ACS-RSVP-帳戶-檔案-位置</span><span class="sxs-lookup"><span data-stu-id="4bca8-112">ACS-RSVP-Account-Files-Location</span></span>             |
| <span data-ttu-id="4bca8-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4bca8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4bca8-114">aCSRSVPAccountFilesLocation</span><span class="sxs-lookup"><span data-stu-id="4bca8-114">aCSRSVPAccountFilesLocation</span></span>                 |
| <span data-ttu-id="4bca8-115">大小</span><span class="sxs-lookup"><span data-stu-id="4bca8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="4bca8-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4bca8-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4bca8-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4bca8-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4bca8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4bca8-118">Attribute-Id</span></span>      | <span data-ttu-id="4bca8-119">1.2.840.113556.1.4.900</span><span class="sxs-lookup"><span data-stu-id="4bca8-119">1.2.840.113556.1.4.900</span></span>                      |
| <span data-ttu-id="4bca8-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4bca8-120">System-Id-Guid</span></span>    | <span data-ttu-id="4bca8-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4bca8-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span></span>        |
| <span data-ttu-id="4bca8-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bca8-122">Syntax</span></span>            | [<span data-ttu-id="4bca8-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4bca8-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4bca8-124">實作</span><span class="sxs-lookup"><span data-stu-id="4bca8-124">Implementations</span></span>

-   [<span data-ttu-id="4bca8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4bca8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4bca8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4bca8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4bca8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4bca8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4bca8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4bca8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4bca8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4bca8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4bca8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4bca8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4bca8-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4bca8-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4bca8-132">進入</span><span class="sxs-lookup"><span data-stu-id="4bca8-132">Entry</span></span> | <span data-ttu-id="4bca8-133">值</span><span class="sxs-lookup"><span data-stu-id="4bca8-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4bca8-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4bca8-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bca8-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bca8-136">System-Only</span></span>            | <span data-ttu-id="4bca8-137">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-137">False</span></span>                                        |
| <span data-ttu-id="4bca8-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4bca8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4bca8-139">對</span><span class="sxs-lookup"><span data-stu-id="4bca8-139">True</span></span>                                         |
| <span data-ttu-id="4bca8-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4bca8-140">Is Indexed</span></span>             | <span data-ttu-id="4bca8-141">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-141">False</span></span>                                        |
| <span data-ttu-id="4bca8-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4bca8-142">In Global Catalog</span></span>      | <span data-ttu-id="4bca8-143">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-143">False</span></span>                                        |
| <span data-ttu-id="4bca8-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4bca8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bca8-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4bca8-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4bca8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bca8-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bca8-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-148">Search-Flags</span></span>           | <span data-ttu-id="4bca8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bca8-149">0x00000000</span></span>                                   |
| <span data-ttu-id="4bca8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-150">System-Flags</span></span>           | <span data-ttu-id="4bca8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bca8-151">0x00000010</span></span>                                   |
| <span data-ttu-id="4bca8-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4bca8-152">Classes used in</span></span>        | [<span data-ttu-id="4bca8-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4bca8-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4bca8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4bca8-154">Windows Server 2003</span></span>



| <span data-ttu-id="4bca8-155">進入</span><span class="sxs-lookup"><span data-stu-id="4bca8-155">Entry</span></span> | <span data-ttu-id="4bca8-156">值</span><span class="sxs-lookup"><span data-stu-id="4bca8-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4bca8-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4bca8-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bca8-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bca8-159">System-Only</span></span>            | <span data-ttu-id="4bca8-160">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-160">False</span></span>                                        |
| <span data-ttu-id="4bca8-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4bca8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4bca8-162">對</span><span class="sxs-lookup"><span data-stu-id="4bca8-162">True</span></span>                                         |
| <span data-ttu-id="4bca8-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4bca8-163">Is Indexed</span></span>             | <span data-ttu-id="4bca8-164">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-164">False</span></span>                                        |
| <span data-ttu-id="4bca8-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4bca8-165">In Global Catalog</span></span>      | <span data-ttu-id="4bca8-166">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-166">False</span></span>                                        |
| <span data-ttu-id="4bca8-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4bca8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bca8-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4bca8-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4bca8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bca8-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bca8-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-171">Search-Flags</span></span>           | <span data-ttu-id="4bca8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bca8-172">0x00000000</span></span>                                   |
| <span data-ttu-id="4bca8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-173">System-Flags</span></span>           | <span data-ttu-id="4bca8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bca8-174">0x00000010</span></span>                                   |
| <span data-ttu-id="4bca8-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4bca8-175">Classes used in</span></span>        | [<span data-ttu-id="4bca8-176">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4bca8-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4bca8-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4bca8-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4bca8-178">進入</span><span class="sxs-lookup"><span data-stu-id="4bca8-178">Entry</span></span> | <span data-ttu-id="4bca8-179">值</span><span class="sxs-lookup"><span data-stu-id="4bca8-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4bca8-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4bca8-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bca8-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bca8-182">System-Only</span></span>            | <span data-ttu-id="4bca8-183">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-183">False</span></span>                                        |
| <span data-ttu-id="4bca8-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4bca8-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4bca8-185">對</span><span class="sxs-lookup"><span data-stu-id="4bca8-185">True</span></span>                                         |
| <span data-ttu-id="4bca8-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4bca8-186">Is Indexed</span></span>             | <span data-ttu-id="4bca8-187">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-187">False</span></span>                                        |
| <span data-ttu-id="4bca8-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4bca8-188">In Global Catalog</span></span>      | <span data-ttu-id="4bca8-189">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-189">False</span></span>                                        |
| <span data-ttu-id="4bca8-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4bca8-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bca8-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4bca8-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4bca8-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bca8-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bca8-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-194">Search-Flags</span></span>           | <span data-ttu-id="4bca8-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bca8-195">0x00000000</span></span>                                   |
| <span data-ttu-id="4bca8-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-196">System-Flags</span></span>           | <span data-ttu-id="4bca8-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bca8-197">0x00000010</span></span>                                   |
| <span data-ttu-id="4bca8-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4bca8-198">Classes used in</span></span>        | [<span data-ttu-id="4bca8-199">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4bca8-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4bca8-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bca8-200">Windows Server 2008</span></span>



| <span data-ttu-id="4bca8-201">進入</span><span class="sxs-lookup"><span data-stu-id="4bca8-201">Entry</span></span> | <span data-ttu-id="4bca8-202">值</span><span class="sxs-lookup"><span data-stu-id="4bca8-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4bca8-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4bca8-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bca8-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bca8-205">System-Only</span></span>            | <span data-ttu-id="4bca8-206">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-206">False</span></span>                                        |
| <span data-ttu-id="4bca8-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4bca8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4bca8-208">對</span><span class="sxs-lookup"><span data-stu-id="4bca8-208">True</span></span>                                         |
| <span data-ttu-id="4bca8-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4bca8-209">Is Indexed</span></span>             | <span data-ttu-id="4bca8-210">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-210">False</span></span>                                        |
| <span data-ttu-id="4bca8-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4bca8-211">In Global Catalog</span></span>      | <span data-ttu-id="4bca8-212">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-212">False</span></span>                                        |
| <span data-ttu-id="4bca8-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4bca8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bca8-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4bca8-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4bca8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bca8-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bca8-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-217">Search-Flags</span></span>           | <span data-ttu-id="4bca8-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bca8-218">0x00000000</span></span>                                   |
| <span data-ttu-id="4bca8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-219">System-Flags</span></span>           | <span data-ttu-id="4bca8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bca8-220">0x00000010</span></span>                                   |
| <span data-ttu-id="4bca8-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4bca8-221">Classes used in</span></span>        | [<span data-ttu-id="4bca8-222">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4bca8-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4bca8-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4bca8-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4bca8-224">進入</span><span class="sxs-lookup"><span data-stu-id="4bca8-224">Entry</span></span> | <span data-ttu-id="4bca8-225">值</span><span class="sxs-lookup"><span data-stu-id="4bca8-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4bca8-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4bca8-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bca8-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bca8-228">System-Only</span></span>            | <span data-ttu-id="4bca8-229">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-229">False</span></span>                                        |
| <span data-ttu-id="4bca8-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4bca8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4bca8-231">對</span><span class="sxs-lookup"><span data-stu-id="4bca8-231">True</span></span>                                         |
| <span data-ttu-id="4bca8-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4bca8-232">Is Indexed</span></span>             | <span data-ttu-id="4bca8-233">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-233">False</span></span>                                        |
| <span data-ttu-id="4bca8-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4bca8-234">In Global Catalog</span></span>      | <span data-ttu-id="4bca8-235">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-235">False</span></span>                                        |
| <span data-ttu-id="4bca8-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4bca8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bca8-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4bca8-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4bca8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bca8-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bca8-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-240">Search-Flags</span></span>           | <span data-ttu-id="4bca8-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bca8-241">0x00000000</span></span>                                   |
| <span data-ttu-id="4bca8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-242">System-Flags</span></span>           | <span data-ttu-id="4bca8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bca8-243">0x00000010</span></span>                                   |
| <span data-ttu-id="4bca8-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4bca8-244">Classes used in</span></span>        | [<span data-ttu-id="4bca8-245">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4bca8-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4bca8-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4bca8-246">Windows Server 2012</span></span>



| <span data-ttu-id="4bca8-247">進入</span><span class="sxs-lookup"><span data-stu-id="4bca8-247">Entry</span></span> | <span data-ttu-id="4bca8-248">值</span><span class="sxs-lookup"><span data-stu-id="4bca8-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4bca8-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4bca8-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bca8-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4bca8-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bca8-251">System-Only</span></span>            | <span data-ttu-id="4bca8-252">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-252">False</span></span>                                        |
| <span data-ttu-id="4bca8-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4bca8-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4bca8-254">對</span><span class="sxs-lookup"><span data-stu-id="4bca8-254">True</span></span>                                         |
| <span data-ttu-id="4bca8-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4bca8-255">Is Indexed</span></span>             | <span data-ttu-id="4bca8-256">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-256">False</span></span>                                        |
| <span data-ttu-id="4bca8-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4bca8-257">In Global Catalog</span></span>      | <span data-ttu-id="4bca8-258">否</span><span class="sxs-lookup"><span data-stu-id="4bca8-258">False</span></span>                                        |
| <span data-ttu-id="4bca8-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4bca8-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bca8-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4bca8-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4bca8-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bca8-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bca8-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4bca8-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-263">Search-Flags</span></span>           | <span data-ttu-id="4bca8-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bca8-264">0x00000000</span></span>                                   |
| <span data-ttu-id="4bca8-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bca8-265">System-Flags</span></span>           | <span data-ttu-id="4bca8-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bca8-266">0x00000010</span></span>                                   |
| <span data-ttu-id="4bca8-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4bca8-267">Classes used in</span></span>        | [<span data-ttu-id="4bca8-268">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4bca8-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





