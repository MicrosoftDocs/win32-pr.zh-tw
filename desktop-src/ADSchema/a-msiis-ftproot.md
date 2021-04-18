---
title: ms-IIS-FTP-根屬性
description: 這個屬性會決定檔案伺服器共用。 它會與 ms-IIS-FTP-Dir 搭配使用，以判斷 FTP 使用者主目錄。
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- ms-IIS-FTP-根屬性 AD 架構
- msIIS-FTPRoot 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55980b8b08865889f7567fa6bdb4dcf7bde1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467343"
---
# <a name="ms-iis-ftp-root-attribute"></a><span data-ttu-id="cef61-106">ms-IIS-FTP-根屬性</span><span class="sxs-lookup"><span data-stu-id="cef61-106">ms-IIS-FTP-Root attribute</span></span>

<span data-ttu-id="cef61-107">這個屬性會決定檔案伺服器共用。</span><span class="sxs-lookup"><span data-stu-id="cef61-107">This attribute determines the file server share.</span></span> <span data-ttu-id="cef61-108">它會與 ms-IIS-FTP-Dir 搭配使用，以判斷 FTP 使用者主目錄。</span><span class="sxs-lookup"><span data-stu-id="cef61-108">It is used in conjunction with ms-IIS-FTP-Dir to determine the FTP user home directory.</span></span>



| <span data-ttu-id="cef61-109">進入</span><span class="sxs-lookup"><span data-stu-id="cef61-109">Entry</span></span> | <span data-ttu-id="cef61-110">值</span><span class="sxs-lookup"><span data-stu-id="cef61-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef61-111">CN</span><span class="sxs-lookup"><span data-stu-id="cef61-111">CN</span></span>                | <span data-ttu-id="cef61-112">ms-IIS-FTP-根目錄</span><span class="sxs-lookup"><span data-stu-id="cef61-112">ms-IIS-FTP-Root</span></span>                                                                                                                 |
| <span data-ttu-id="cef61-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cef61-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cef61-114">msIIS-FTPRoot</span><span class="sxs-lookup"><span data-stu-id="cef61-114">msIIS-FTPRoot</span></span>                                                                                                                   |
| <span data-ttu-id="cef61-115">大小</span><span class="sxs-lookup"><span data-stu-id="cef61-115">Size</span></span>              | <span data-ttu-id="cef61-116">30-50 個字元針對每個屬性 (15-25 Unicode 字元) </span><span class="sxs-lookup"><span data-stu-id="cef61-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="cef61-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="cef61-117">Update Privilege</span></span>  | <span data-ttu-id="cef61-118">網域系統管理員 & 本機系統</span><span class="sxs-lookup"><span data-stu-id="cef61-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="cef61-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="cef61-119">Update Frequency</span></span>  | <span data-ttu-id="cef61-120">當系統管理員建立網站並設定 FTP 隔離時，會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="cef61-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="cef61-121">這麼做之後很少會變更。</span><span class="sxs-lookup"><span data-stu-id="cef61-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="cef61-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cef61-122">Attribute-Id</span></span>      | <span data-ttu-id="cef61-123">1.2.840.113556.1.4.1785</span><span class="sxs-lookup"><span data-stu-id="cef61-123">1.2.840.113556.1.4.1785</span></span>                                                                                                         |
| <span data-ttu-id="cef61-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="cef61-124">System-Id-Guid</span></span>    | <span data-ttu-id="cef61-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span><span class="sxs-lookup"><span data-stu-id="cef61-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span></span>                                                                                            |
| <span data-ttu-id="cef61-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="cef61-126">Syntax</span></span>            | [<span data-ttu-id="cef61-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cef61-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="cef61-128">實作</span><span class="sxs-lookup"><span data-stu-id="cef61-128">Implementations</span></span>

-   [<span data-ttu-id="cef61-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cef61-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cef61-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cef61-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cef61-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cef61-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cef61-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cef61-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cef61-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cef61-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cef61-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cef61-134">Windows Server 2003</span></span>



| <span data-ttu-id="cef61-135">進入</span><span class="sxs-lookup"><span data-stu-id="cef61-135">Entry</span></span> | <span data-ttu-id="cef61-136">值</span><span class="sxs-lookup"><span data-stu-id="cef61-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cef61-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cef61-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cef61-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cef61-139">System-Only</span></span>            | <span data-ttu-id="cef61-140">否</span><span class="sxs-lookup"><span data-stu-id="cef61-140">False</span></span>                             |
| <span data-ttu-id="cef61-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cef61-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cef61-142">對</span><span class="sxs-lookup"><span data-stu-id="cef61-142">True</span></span>                              |
| <span data-ttu-id="cef61-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cef61-143">Is Indexed</span></span>             | <span data-ttu-id="cef61-144">否</span><span class="sxs-lookup"><span data-stu-id="cef61-144">False</span></span>                             |
| <span data-ttu-id="cef61-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cef61-145">In Global Catalog</span></span>      | <span data-ttu-id="cef61-146">否</span><span class="sxs-lookup"><span data-stu-id="cef61-146">False</span></span>                             |
| <span data-ttu-id="cef61-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cef61-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cef61-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cef61-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cef61-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cef61-149">Range-Lower</span></span>            | <span data-ttu-id="cef61-150">1</span><span class="sxs-lookup"><span data-stu-id="cef61-150">1</span></span>                                 |
| <span data-ttu-id="cef61-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cef61-151">Range-Upper</span></span>            | <span data-ttu-id="cef61-152">256</span><span class="sxs-lookup"><span data-stu-id="cef61-152">256</span></span>                               |
| <span data-ttu-id="cef61-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-153">Search-Flags</span></span>           | <span data-ttu-id="cef61-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cef61-154">0x00000000</span></span>                        |
| <span data-ttu-id="cef61-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-155">System-Flags</span></span>           | <span data-ttu-id="cef61-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cef61-156">0x00000010</span></span>                        |
| <span data-ttu-id="cef61-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cef61-157">Classes used in</span></span>        | [<span data-ttu-id="cef61-158">**User**</span><span class="sxs-lookup"><span data-stu-id="cef61-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cef61-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cef61-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cef61-160">進入</span><span class="sxs-lookup"><span data-stu-id="cef61-160">Entry</span></span> | <span data-ttu-id="cef61-161">值</span><span class="sxs-lookup"><span data-stu-id="cef61-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cef61-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cef61-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cef61-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="cef61-164">System-Only</span></span>            | <span data-ttu-id="cef61-165">否</span><span class="sxs-lookup"><span data-stu-id="cef61-165">False</span></span>                             |
| <span data-ttu-id="cef61-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cef61-166">Is-Single-Valued</span></span>       | <span data-ttu-id="cef61-167">對</span><span class="sxs-lookup"><span data-stu-id="cef61-167">True</span></span>                              |
| <span data-ttu-id="cef61-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cef61-168">Is Indexed</span></span>             | <span data-ttu-id="cef61-169">否</span><span class="sxs-lookup"><span data-stu-id="cef61-169">False</span></span>                             |
| <span data-ttu-id="cef61-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cef61-170">In Global Catalog</span></span>      | <span data-ttu-id="cef61-171">否</span><span class="sxs-lookup"><span data-stu-id="cef61-171">False</span></span>                             |
| <span data-ttu-id="cef61-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cef61-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="cef61-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cef61-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cef61-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cef61-174">Range-Lower</span></span>            | <span data-ttu-id="cef61-175">1</span><span class="sxs-lookup"><span data-stu-id="cef61-175">1</span></span>                                 |
| <span data-ttu-id="cef61-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cef61-176">Range-Upper</span></span>            | <span data-ttu-id="cef61-177">256</span><span class="sxs-lookup"><span data-stu-id="cef61-177">256</span></span>                               |
| <span data-ttu-id="cef61-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-178">Search-Flags</span></span>           | <span data-ttu-id="cef61-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cef61-179">0x00000000</span></span>                        |
| <span data-ttu-id="cef61-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-180">System-Flags</span></span>           | <span data-ttu-id="cef61-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cef61-181">0x00000010</span></span>                        |
| <span data-ttu-id="cef61-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cef61-182">Classes used in</span></span>        | [<span data-ttu-id="cef61-183">**User**</span><span class="sxs-lookup"><span data-stu-id="cef61-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cef61-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cef61-184">Windows Server 2008</span></span>



| <span data-ttu-id="cef61-185">進入</span><span class="sxs-lookup"><span data-stu-id="cef61-185">Entry</span></span> | <span data-ttu-id="cef61-186">值</span><span class="sxs-lookup"><span data-stu-id="cef61-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cef61-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cef61-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cef61-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="cef61-189">System-Only</span></span>            | <span data-ttu-id="cef61-190">否</span><span class="sxs-lookup"><span data-stu-id="cef61-190">False</span></span>                             |
| <span data-ttu-id="cef61-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cef61-191">Is-Single-Valued</span></span>       | <span data-ttu-id="cef61-192">對</span><span class="sxs-lookup"><span data-stu-id="cef61-192">True</span></span>                              |
| <span data-ttu-id="cef61-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cef61-193">Is Indexed</span></span>             | <span data-ttu-id="cef61-194">否</span><span class="sxs-lookup"><span data-stu-id="cef61-194">False</span></span>                             |
| <span data-ttu-id="cef61-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cef61-195">In Global Catalog</span></span>      | <span data-ttu-id="cef61-196">否</span><span class="sxs-lookup"><span data-stu-id="cef61-196">False</span></span>                             |
| <span data-ttu-id="cef61-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cef61-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="cef61-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cef61-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cef61-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cef61-199">Range-Lower</span></span>            | <span data-ttu-id="cef61-200">1</span><span class="sxs-lookup"><span data-stu-id="cef61-200">1</span></span>                                 |
| <span data-ttu-id="cef61-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cef61-201">Range-Upper</span></span>            | <span data-ttu-id="cef61-202">256</span><span class="sxs-lookup"><span data-stu-id="cef61-202">256</span></span>                               |
| <span data-ttu-id="cef61-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-203">Search-Flags</span></span>           | <span data-ttu-id="cef61-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cef61-204">0x00000000</span></span>                        |
| <span data-ttu-id="cef61-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-205">System-Flags</span></span>           | <span data-ttu-id="cef61-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cef61-206">0x00000010</span></span>                        |
| <span data-ttu-id="cef61-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cef61-207">Classes used in</span></span>        | [<span data-ttu-id="cef61-208">**User**</span><span class="sxs-lookup"><span data-stu-id="cef61-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cef61-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cef61-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cef61-210">進入</span><span class="sxs-lookup"><span data-stu-id="cef61-210">Entry</span></span> | <span data-ttu-id="cef61-211">值</span><span class="sxs-lookup"><span data-stu-id="cef61-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cef61-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cef61-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cef61-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="cef61-214">System-Only</span></span>            | <span data-ttu-id="cef61-215">否</span><span class="sxs-lookup"><span data-stu-id="cef61-215">False</span></span>                             |
| <span data-ttu-id="cef61-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cef61-216">Is-Single-Valued</span></span>       | <span data-ttu-id="cef61-217">對</span><span class="sxs-lookup"><span data-stu-id="cef61-217">True</span></span>                              |
| <span data-ttu-id="cef61-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cef61-218">Is Indexed</span></span>             | <span data-ttu-id="cef61-219">否</span><span class="sxs-lookup"><span data-stu-id="cef61-219">False</span></span>                             |
| <span data-ttu-id="cef61-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cef61-220">In Global Catalog</span></span>      | <span data-ttu-id="cef61-221">否</span><span class="sxs-lookup"><span data-stu-id="cef61-221">False</span></span>                             |
| <span data-ttu-id="cef61-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cef61-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="cef61-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cef61-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cef61-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cef61-224">Range-Lower</span></span>            | <span data-ttu-id="cef61-225">1</span><span class="sxs-lookup"><span data-stu-id="cef61-225">1</span></span>                                 |
| <span data-ttu-id="cef61-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cef61-226">Range-Upper</span></span>            | <span data-ttu-id="cef61-227">256</span><span class="sxs-lookup"><span data-stu-id="cef61-227">256</span></span>                               |
| <span data-ttu-id="cef61-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-228">Search-Flags</span></span>           | <span data-ttu-id="cef61-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cef61-229">0x00000000</span></span>                        |
| <span data-ttu-id="cef61-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-230">System-Flags</span></span>           | <span data-ttu-id="cef61-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cef61-231">0x00000010</span></span>                        |
| <span data-ttu-id="cef61-232">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cef61-232">Classes used in</span></span>        | [<span data-ttu-id="cef61-233">**User**</span><span class="sxs-lookup"><span data-stu-id="cef61-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cef61-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cef61-234">Windows Server 2012</span></span>



| <span data-ttu-id="cef61-235">進入</span><span class="sxs-lookup"><span data-stu-id="cef61-235">Entry</span></span> | <span data-ttu-id="cef61-236">值</span><span class="sxs-lookup"><span data-stu-id="cef61-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="cef61-237">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="cef61-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cef61-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="cef61-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="cef61-239">System-Only</span></span>            | <span data-ttu-id="cef61-240">否</span><span class="sxs-lookup"><span data-stu-id="cef61-240">False</span></span>                             |
| <span data-ttu-id="cef61-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="cef61-241">Is-Single-Valued</span></span>       | <span data-ttu-id="cef61-242">對</span><span class="sxs-lookup"><span data-stu-id="cef61-242">True</span></span>                              |
| <span data-ttu-id="cef61-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="cef61-243">Is Indexed</span></span>             | <span data-ttu-id="cef61-244">否</span><span class="sxs-lookup"><span data-stu-id="cef61-244">False</span></span>                             |
| <span data-ttu-id="cef61-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="cef61-245">In Global Catalog</span></span>      | <span data-ttu-id="cef61-246">否</span><span class="sxs-lookup"><span data-stu-id="cef61-246">False</span></span>                             |
| <span data-ttu-id="cef61-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="cef61-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="cef61-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="cef61-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="cef61-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cef61-249">Range-Lower</span></span>            | <span data-ttu-id="cef61-250">1</span><span class="sxs-lookup"><span data-stu-id="cef61-250">1</span></span>                                 |
| <span data-ttu-id="cef61-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cef61-251">Range-Upper</span></span>            | <span data-ttu-id="cef61-252">256</span><span class="sxs-lookup"><span data-stu-id="cef61-252">256</span></span>                               |
| <span data-ttu-id="cef61-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-253">Search-Flags</span></span>           | <span data-ttu-id="cef61-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cef61-254">0x00000000</span></span>                        |
| <span data-ttu-id="cef61-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cef61-255">System-Flags</span></span>           | <span data-ttu-id="cef61-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cef61-256">0x00000010</span></span>                        |
| <span data-ttu-id="cef61-257">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="cef61-257">Classes used in</span></span>        | [<span data-ttu-id="cef61-258">**User**</span><span class="sxs-lookup"><span data-stu-id="cef61-258">**User**</span></span>](c-user.md)<br/> |



 

 





