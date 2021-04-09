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
# <a name="acs-rsvp-account-files-location-attribute"></a><span data-ttu-id="d3b81-106">ACS-RSVP-帳戶-檔案-位置屬性</span><span class="sxs-lookup"><span data-stu-id="d3b81-106">ACS-RSVP-Account-Files-Location attribute</span></span>

<span data-ttu-id="d3b81-107">RSVP 帳戶檔案的目錄位置。</span><span class="sxs-lookup"><span data-stu-id="d3b81-107">The directory location of RSVP account files.</span></span> <span data-ttu-id="d3b81-108">預設為位於預設系統目錄中的 "system32" 子目錄。</span><span class="sxs-lookup"><span data-stu-id="d3b81-108">Defaults to the "system32" subdirectory located in the default system directory.</span></span>



| <span data-ttu-id="d3b81-109">進入</span><span class="sxs-lookup"><span data-stu-id="d3b81-109">Entry</span></span> | <span data-ttu-id="d3b81-110">值</span><span class="sxs-lookup"><span data-stu-id="d3b81-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d3b81-111">CN</span><span class="sxs-lookup"><span data-stu-id="d3b81-111">CN</span></span>                | <span data-ttu-id="d3b81-112">ACS-RSVP-帳戶-檔案-位置</span><span class="sxs-lookup"><span data-stu-id="d3b81-112">ACS-RSVP-Account-Files-Location</span></span>             |
| <span data-ttu-id="d3b81-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d3b81-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d3b81-114">aCSRSVPAccountFilesLocation</span><span class="sxs-lookup"><span data-stu-id="d3b81-114">aCSRSVPAccountFilesLocation</span></span>                 |
| <span data-ttu-id="d3b81-115">大小</span><span class="sxs-lookup"><span data-stu-id="d3b81-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="d3b81-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d3b81-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d3b81-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d3b81-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d3b81-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3b81-118">Attribute-Id</span></span>      | <span data-ttu-id="d3b81-119">1.2.840.113556.1.4.900</span><span class="sxs-lookup"><span data-stu-id="d3b81-119">1.2.840.113556.1.4.900</span></span>                      |
| <span data-ttu-id="d3b81-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d3b81-120">System-Id-Guid</span></span>    | <span data-ttu-id="d3b81-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d3b81-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span></span>        |
| <span data-ttu-id="d3b81-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3b81-122">Syntax</span></span>            | [<span data-ttu-id="d3b81-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d3b81-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d3b81-124">實作</span><span class="sxs-lookup"><span data-stu-id="d3b81-124">Implementations</span></span>

-   [<span data-ttu-id="d3b81-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d3b81-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d3b81-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3b81-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3b81-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3b81-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3b81-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3b81-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3b81-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3b81-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3b81-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3b81-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d3b81-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3b81-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d3b81-132">進入</span><span class="sxs-lookup"><span data-stu-id="d3b81-132">Entry</span></span> | <span data-ttu-id="d3b81-133">值</span><span class="sxs-lookup"><span data-stu-id="d3b81-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d3b81-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b81-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b81-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b81-136">System-Only</span></span>            | <span data-ttu-id="d3b81-137">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-137">False</span></span>                                        |
| <span data-ttu-id="d3b81-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b81-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b81-139">對</span><span class="sxs-lookup"><span data-stu-id="d3b81-139">True</span></span>                                         |
| <span data-ttu-id="d3b81-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b81-140">Is Indexed</span></span>             | <span data-ttu-id="d3b81-141">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-141">False</span></span>                                        |
| <span data-ttu-id="d3b81-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b81-142">In Global Catalog</span></span>      | <span data-ttu-id="d3b81-143">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-143">False</span></span>                                        |
| <span data-ttu-id="d3b81-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b81-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b81-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b81-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d3b81-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b81-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b81-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-148">Search-Flags</span></span>           | <span data-ttu-id="d3b81-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b81-149">0x00000000</span></span>                                   |
| <span data-ttu-id="d3b81-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-150">System-Flags</span></span>           | <span data-ttu-id="d3b81-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b81-151">0x00000010</span></span>                                   |
| <span data-ttu-id="d3b81-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b81-152">Classes used in</span></span>        | [<span data-ttu-id="d3b81-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="d3b81-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d3b81-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3b81-154">Windows Server 2003</span></span>



| <span data-ttu-id="d3b81-155">進入</span><span class="sxs-lookup"><span data-stu-id="d3b81-155">Entry</span></span> | <span data-ttu-id="d3b81-156">值</span><span class="sxs-lookup"><span data-stu-id="d3b81-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d3b81-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b81-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b81-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b81-159">System-Only</span></span>            | <span data-ttu-id="d3b81-160">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-160">False</span></span>                                        |
| <span data-ttu-id="d3b81-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b81-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b81-162">對</span><span class="sxs-lookup"><span data-stu-id="d3b81-162">True</span></span>                                         |
| <span data-ttu-id="d3b81-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b81-163">Is Indexed</span></span>             | <span data-ttu-id="d3b81-164">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-164">False</span></span>                                        |
| <span data-ttu-id="d3b81-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b81-165">In Global Catalog</span></span>      | <span data-ttu-id="d3b81-166">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-166">False</span></span>                                        |
| <span data-ttu-id="d3b81-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b81-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b81-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b81-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d3b81-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b81-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b81-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-171">Search-Flags</span></span>           | <span data-ttu-id="d3b81-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b81-172">0x00000000</span></span>                                   |
| <span data-ttu-id="d3b81-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-173">System-Flags</span></span>           | <span data-ttu-id="d3b81-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b81-174">0x00000010</span></span>                                   |
| <span data-ttu-id="d3b81-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b81-175">Classes used in</span></span>        | [<span data-ttu-id="d3b81-176">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="d3b81-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3b81-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3b81-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3b81-178">進入</span><span class="sxs-lookup"><span data-stu-id="d3b81-178">Entry</span></span> | <span data-ttu-id="d3b81-179">值</span><span class="sxs-lookup"><span data-stu-id="d3b81-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d3b81-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b81-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b81-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b81-182">System-Only</span></span>            | <span data-ttu-id="d3b81-183">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-183">False</span></span>                                        |
| <span data-ttu-id="d3b81-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b81-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b81-185">對</span><span class="sxs-lookup"><span data-stu-id="d3b81-185">True</span></span>                                         |
| <span data-ttu-id="d3b81-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b81-186">Is Indexed</span></span>             | <span data-ttu-id="d3b81-187">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-187">False</span></span>                                        |
| <span data-ttu-id="d3b81-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b81-188">In Global Catalog</span></span>      | <span data-ttu-id="d3b81-189">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-189">False</span></span>                                        |
| <span data-ttu-id="d3b81-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b81-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b81-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b81-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d3b81-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b81-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b81-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-194">Search-Flags</span></span>           | <span data-ttu-id="d3b81-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b81-195">0x00000000</span></span>                                   |
| <span data-ttu-id="d3b81-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-196">System-Flags</span></span>           | <span data-ttu-id="d3b81-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b81-197">0x00000010</span></span>                                   |
| <span data-ttu-id="d3b81-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b81-198">Classes used in</span></span>        | [<span data-ttu-id="d3b81-199">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="d3b81-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3b81-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3b81-200">Windows Server 2008</span></span>



| <span data-ttu-id="d3b81-201">進入</span><span class="sxs-lookup"><span data-stu-id="d3b81-201">Entry</span></span> | <span data-ttu-id="d3b81-202">值</span><span class="sxs-lookup"><span data-stu-id="d3b81-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d3b81-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b81-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b81-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b81-205">System-Only</span></span>            | <span data-ttu-id="d3b81-206">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-206">False</span></span>                                        |
| <span data-ttu-id="d3b81-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b81-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b81-208">對</span><span class="sxs-lookup"><span data-stu-id="d3b81-208">True</span></span>                                         |
| <span data-ttu-id="d3b81-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b81-209">Is Indexed</span></span>             | <span data-ttu-id="d3b81-210">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-210">False</span></span>                                        |
| <span data-ttu-id="d3b81-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b81-211">In Global Catalog</span></span>      | <span data-ttu-id="d3b81-212">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-212">False</span></span>                                        |
| <span data-ttu-id="d3b81-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b81-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b81-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b81-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d3b81-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b81-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b81-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-217">Search-Flags</span></span>           | <span data-ttu-id="d3b81-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b81-218">0x00000000</span></span>                                   |
| <span data-ttu-id="d3b81-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-219">System-Flags</span></span>           | <span data-ttu-id="d3b81-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b81-220">0x00000010</span></span>                                   |
| <span data-ttu-id="d3b81-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b81-221">Classes used in</span></span>        | [<span data-ttu-id="d3b81-222">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="d3b81-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3b81-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3b81-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3b81-224">進入</span><span class="sxs-lookup"><span data-stu-id="d3b81-224">Entry</span></span> | <span data-ttu-id="d3b81-225">值</span><span class="sxs-lookup"><span data-stu-id="d3b81-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d3b81-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b81-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b81-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b81-228">System-Only</span></span>            | <span data-ttu-id="d3b81-229">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-229">False</span></span>                                        |
| <span data-ttu-id="d3b81-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b81-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b81-231">對</span><span class="sxs-lookup"><span data-stu-id="d3b81-231">True</span></span>                                         |
| <span data-ttu-id="d3b81-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b81-232">Is Indexed</span></span>             | <span data-ttu-id="d3b81-233">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-233">False</span></span>                                        |
| <span data-ttu-id="d3b81-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b81-234">In Global Catalog</span></span>      | <span data-ttu-id="d3b81-235">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-235">False</span></span>                                        |
| <span data-ttu-id="d3b81-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b81-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b81-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b81-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d3b81-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b81-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b81-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-240">Search-Flags</span></span>           | <span data-ttu-id="d3b81-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b81-241">0x00000000</span></span>                                   |
| <span data-ttu-id="d3b81-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-242">System-Flags</span></span>           | <span data-ttu-id="d3b81-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b81-243">0x00000010</span></span>                                   |
| <span data-ttu-id="d3b81-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b81-244">Classes used in</span></span>        | [<span data-ttu-id="d3b81-245">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="d3b81-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3b81-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3b81-246">Windows Server 2012</span></span>



| <span data-ttu-id="d3b81-247">進入</span><span class="sxs-lookup"><span data-stu-id="d3b81-247">Entry</span></span> | <span data-ttu-id="d3b81-248">值</span><span class="sxs-lookup"><span data-stu-id="d3b81-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d3b81-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b81-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3b81-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d3b81-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3b81-251">System-Only</span></span>            | <span data-ttu-id="d3b81-252">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-252">False</span></span>                                        |
| <span data-ttu-id="d3b81-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3b81-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d3b81-254">對</span><span class="sxs-lookup"><span data-stu-id="d3b81-254">True</span></span>                                         |
| <span data-ttu-id="d3b81-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3b81-255">Is Indexed</span></span>             | <span data-ttu-id="d3b81-256">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-256">False</span></span>                                        |
| <span data-ttu-id="d3b81-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3b81-257">In Global Catalog</span></span>      | <span data-ttu-id="d3b81-258">否</span><span class="sxs-lookup"><span data-stu-id="d3b81-258">False</span></span>                                        |
| <span data-ttu-id="d3b81-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3b81-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3b81-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3b81-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d3b81-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3b81-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3b81-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d3b81-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-263">Search-Flags</span></span>           | <span data-ttu-id="d3b81-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3b81-264">0x00000000</span></span>                                   |
| <span data-ttu-id="d3b81-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3b81-265">System-Flags</span></span>           | <span data-ttu-id="d3b81-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3b81-266">0x00000010</span></span>                                   |
| <span data-ttu-id="d3b81-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3b81-267">Classes used in</span></span>        | [<span data-ttu-id="d3b81-268">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="d3b81-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





