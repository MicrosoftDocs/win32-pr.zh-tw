---
title: ms-IIS-FTP-Dir 屬性
description: 這個屬性會決定相對於檔案伺服器共用的使用者主目錄。 它會與 ms-IIS-FTP 根目錄搭配使用，以判斷 FTP 使用者主目錄。
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- ms-IIS-FTP-Dir 屬性 AD 架構
- msIIS-FTPDir 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509608"
---
# <a name="ms-iis-ftp-dir-attribute"></a><span data-ttu-id="1a17b-106">ms-IIS-FTP-Dir 屬性</span><span class="sxs-lookup"><span data-stu-id="1a17b-106">ms-IIS-FTP-Dir attribute</span></span>

<span data-ttu-id="1a17b-107">這個屬性會決定相對於檔案伺服器共用的使用者主目錄。</span><span class="sxs-lookup"><span data-stu-id="1a17b-107">This attribute determines the user home directory relative to the file server share.</span></span> <span data-ttu-id="1a17b-108">它會與 ms-IIS-FTP 根目錄搭配使用，以判斷 FTP 使用者主目錄。</span><span class="sxs-lookup"><span data-stu-id="1a17b-108">It is used in conjunction with ms-IIS-FTP-Root to determine the FTP user home directory.</span></span>



| <span data-ttu-id="1a17b-109">進入</span><span class="sxs-lookup"><span data-stu-id="1a17b-109">Entry</span></span> | <span data-ttu-id="1a17b-110">值</span><span class="sxs-lookup"><span data-stu-id="1a17b-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a17b-111">CN</span><span class="sxs-lookup"><span data-stu-id="1a17b-111">CN</span></span>                | <span data-ttu-id="1a17b-112">ms-IIS-FTP-Dir</span><span class="sxs-lookup"><span data-stu-id="1a17b-112">ms-IIS-FTP-Dir</span></span>                                                                                                                  |
| <span data-ttu-id="1a17b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1a17b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1a17b-114">msIIS-FTPDir</span><span class="sxs-lookup"><span data-stu-id="1a17b-114">msIIS-FTPDir</span></span>                                                                                                                    |
| <span data-ttu-id="1a17b-115">大小</span><span class="sxs-lookup"><span data-stu-id="1a17b-115">Size</span></span>              | <span data-ttu-id="1a17b-116">30-50 個字元針對每個屬性 (15-25 Unicode 字元) </span><span class="sxs-lookup"><span data-stu-id="1a17b-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="1a17b-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1a17b-117">Update Privilege</span></span>  | <span data-ttu-id="1a17b-118">網域系統管理員 & 本機系統</span><span class="sxs-lookup"><span data-stu-id="1a17b-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="1a17b-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1a17b-119">Update Frequency</span></span>  | <span data-ttu-id="1a17b-120">當系統管理員建立網站並設定 FTP 隔離時，會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="1a17b-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="1a17b-121">這麼做之後很少會變更。</span><span class="sxs-lookup"><span data-stu-id="1a17b-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="1a17b-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1a17b-122">Attribute-Id</span></span>      | <span data-ttu-id="1a17b-123">1.2.840.113556.1.4.1786</span><span class="sxs-lookup"><span data-stu-id="1a17b-123">1.2.840.113556.1.4.1786</span></span>                                                                                                         |
| <span data-ttu-id="1a17b-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1a17b-124">System-Id-Guid</span></span>    | <span data-ttu-id="1a17b-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span><span class="sxs-lookup"><span data-stu-id="1a17b-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span></span>                                                                                            |
| <span data-ttu-id="1a17b-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a17b-126">Syntax</span></span>            | [<span data-ttu-id="1a17b-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1a17b-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="1a17b-128">實作</span><span class="sxs-lookup"><span data-stu-id="1a17b-128">Implementations</span></span>

-   [<span data-ttu-id="1a17b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1a17b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1a17b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1a17b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1a17b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1a17b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1a17b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1a17b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1a17b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1a17b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1a17b-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a17b-134">Windows Server 2003</span></span>



| <span data-ttu-id="1a17b-135">進入</span><span class="sxs-lookup"><span data-stu-id="1a17b-135">Entry</span></span> | <span data-ttu-id="1a17b-136">值</span><span class="sxs-lookup"><span data-stu-id="1a17b-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1a17b-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a17b-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a17b-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a17b-139">System-Only</span></span>            | <span data-ttu-id="1a17b-140">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-140">False</span></span>                             |
| <span data-ttu-id="1a17b-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a17b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1a17b-142">對</span><span class="sxs-lookup"><span data-stu-id="1a17b-142">True</span></span>                              |
| <span data-ttu-id="1a17b-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a17b-143">Is Indexed</span></span>             | <span data-ttu-id="1a17b-144">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-144">False</span></span>                             |
| <span data-ttu-id="1a17b-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a17b-145">In Global Catalog</span></span>      | <span data-ttu-id="1a17b-146">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-146">False</span></span>                             |
| <span data-ttu-id="1a17b-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a17b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a17b-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a17b-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1a17b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a17b-149">Range-Lower</span></span>            | <span data-ttu-id="1a17b-150">1</span><span class="sxs-lookup"><span data-stu-id="1a17b-150">1</span></span>                                 |
| <span data-ttu-id="1a17b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a17b-151">Range-Upper</span></span>            | <span data-ttu-id="1a17b-152">256</span><span class="sxs-lookup"><span data-stu-id="1a17b-152">256</span></span>                               |
| <span data-ttu-id="1a17b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-153">Search-Flags</span></span>           | <span data-ttu-id="1a17b-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a17b-154">0x00000000</span></span>                        |
| <span data-ttu-id="1a17b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-155">System-Flags</span></span>           | <span data-ttu-id="1a17b-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a17b-156">0x00000010</span></span>                        |
| <span data-ttu-id="1a17b-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a17b-157">Classes used in</span></span>        | [<span data-ttu-id="1a17b-158">**User**</span><span class="sxs-lookup"><span data-stu-id="1a17b-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1a17b-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1a17b-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1a17b-160">進入</span><span class="sxs-lookup"><span data-stu-id="1a17b-160">Entry</span></span> | <span data-ttu-id="1a17b-161">值</span><span class="sxs-lookup"><span data-stu-id="1a17b-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1a17b-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a17b-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a17b-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a17b-164">System-Only</span></span>            | <span data-ttu-id="1a17b-165">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-165">False</span></span>                             |
| <span data-ttu-id="1a17b-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a17b-166">Is-Single-Valued</span></span>       | <span data-ttu-id="1a17b-167">對</span><span class="sxs-lookup"><span data-stu-id="1a17b-167">True</span></span>                              |
| <span data-ttu-id="1a17b-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a17b-168">Is Indexed</span></span>             | <span data-ttu-id="1a17b-169">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-169">False</span></span>                             |
| <span data-ttu-id="1a17b-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a17b-170">In Global Catalog</span></span>      | <span data-ttu-id="1a17b-171">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-171">False</span></span>                             |
| <span data-ttu-id="1a17b-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a17b-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a17b-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a17b-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1a17b-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a17b-174">Range-Lower</span></span>            | <span data-ttu-id="1a17b-175">1</span><span class="sxs-lookup"><span data-stu-id="1a17b-175">1</span></span>                                 |
| <span data-ttu-id="1a17b-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a17b-176">Range-Upper</span></span>            | <span data-ttu-id="1a17b-177">256</span><span class="sxs-lookup"><span data-stu-id="1a17b-177">256</span></span>                               |
| <span data-ttu-id="1a17b-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-178">Search-Flags</span></span>           | <span data-ttu-id="1a17b-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a17b-179">0x00000000</span></span>                        |
| <span data-ttu-id="1a17b-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-180">System-Flags</span></span>           | <span data-ttu-id="1a17b-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a17b-181">0x00000010</span></span>                        |
| <span data-ttu-id="1a17b-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a17b-182">Classes used in</span></span>        | [<span data-ttu-id="1a17b-183">**User**</span><span class="sxs-lookup"><span data-stu-id="1a17b-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1a17b-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a17b-184">Windows Server 2008</span></span>



| <span data-ttu-id="1a17b-185">進入</span><span class="sxs-lookup"><span data-stu-id="1a17b-185">Entry</span></span> | <span data-ttu-id="1a17b-186">值</span><span class="sxs-lookup"><span data-stu-id="1a17b-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1a17b-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a17b-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a17b-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a17b-189">System-Only</span></span>            | <span data-ttu-id="1a17b-190">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-190">False</span></span>                             |
| <span data-ttu-id="1a17b-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a17b-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1a17b-192">對</span><span class="sxs-lookup"><span data-stu-id="1a17b-192">True</span></span>                              |
| <span data-ttu-id="1a17b-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a17b-193">Is Indexed</span></span>             | <span data-ttu-id="1a17b-194">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-194">False</span></span>                             |
| <span data-ttu-id="1a17b-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a17b-195">In Global Catalog</span></span>      | <span data-ttu-id="1a17b-196">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-196">False</span></span>                             |
| <span data-ttu-id="1a17b-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a17b-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a17b-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a17b-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1a17b-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a17b-199">Range-Lower</span></span>            | <span data-ttu-id="1a17b-200">1</span><span class="sxs-lookup"><span data-stu-id="1a17b-200">1</span></span>                                 |
| <span data-ttu-id="1a17b-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a17b-201">Range-Upper</span></span>            | <span data-ttu-id="1a17b-202">256</span><span class="sxs-lookup"><span data-stu-id="1a17b-202">256</span></span>                               |
| <span data-ttu-id="1a17b-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-203">Search-Flags</span></span>           | <span data-ttu-id="1a17b-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a17b-204">0x00000000</span></span>                        |
| <span data-ttu-id="1a17b-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-205">System-Flags</span></span>           | <span data-ttu-id="1a17b-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a17b-206">0x00000010</span></span>                        |
| <span data-ttu-id="1a17b-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a17b-207">Classes used in</span></span>        | [<span data-ttu-id="1a17b-208">**User**</span><span class="sxs-lookup"><span data-stu-id="1a17b-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1a17b-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1a17b-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1a17b-210">進入</span><span class="sxs-lookup"><span data-stu-id="1a17b-210">Entry</span></span> | <span data-ttu-id="1a17b-211">值</span><span class="sxs-lookup"><span data-stu-id="1a17b-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1a17b-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a17b-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a17b-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a17b-214">System-Only</span></span>            | <span data-ttu-id="1a17b-215">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-215">False</span></span>                             |
| <span data-ttu-id="1a17b-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a17b-216">Is-Single-Valued</span></span>       | <span data-ttu-id="1a17b-217">對</span><span class="sxs-lookup"><span data-stu-id="1a17b-217">True</span></span>                              |
| <span data-ttu-id="1a17b-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a17b-218">Is Indexed</span></span>             | <span data-ttu-id="1a17b-219">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-219">False</span></span>                             |
| <span data-ttu-id="1a17b-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a17b-220">In Global Catalog</span></span>      | <span data-ttu-id="1a17b-221">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-221">False</span></span>                             |
| <span data-ttu-id="1a17b-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a17b-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a17b-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a17b-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1a17b-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a17b-224">Range-Lower</span></span>            | <span data-ttu-id="1a17b-225">1</span><span class="sxs-lookup"><span data-stu-id="1a17b-225">1</span></span>                                 |
| <span data-ttu-id="1a17b-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a17b-226">Range-Upper</span></span>            | <span data-ttu-id="1a17b-227">256</span><span class="sxs-lookup"><span data-stu-id="1a17b-227">256</span></span>                               |
| <span data-ttu-id="1a17b-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-228">Search-Flags</span></span>           | <span data-ttu-id="1a17b-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a17b-229">0x00000000</span></span>                        |
| <span data-ttu-id="1a17b-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-230">System-Flags</span></span>           | <span data-ttu-id="1a17b-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a17b-231">0x00000010</span></span>                        |
| <span data-ttu-id="1a17b-232">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a17b-232">Classes used in</span></span>        | [<span data-ttu-id="1a17b-233">**User**</span><span class="sxs-lookup"><span data-stu-id="1a17b-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1a17b-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a17b-234">Windows Server 2012</span></span>



| <span data-ttu-id="1a17b-235">進入</span><span class="sxs-lookup"><span data-stu-id="1a17b-235">Entry</span></span> | <span data-ttu-id="1a17b-236">值</span><span class="sxs-lookup"><span data-stu-id="1a17b-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1a17b-237">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1a17b-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1a17b-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1a17b-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="1a17b-239">System-Only</span></span>            | <span data-ttu-id="1a17b-240">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-240">False</span></span>                             |
| <span data-ttu-id="1a17b-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1a17b-241">Is-Single-Valued</span></span>       | <span data-ttu-id="1a17b-242">對</span><span class="sxs-lookup"><span data-stu-id="1a17b-242">True</span></span>                              |
| <span data-ttu-id="1a17b-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1a17b-243">Is Indexed</span></span>             | <span data-ttu-id="1a17b-244">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-244">False</span></span>                             |
| <span data-ttu-id="1a17b-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1a17b-245">In Global Catalog</span></span>      | <span data-ttu-id="1a17b-246">否</span><span class="sxs-lookup"><span data-stu-id="1a17b-246">False</span></span>                             |
| <span data-ttu-id="1a17b-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1a17b-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="1a17b-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1a17b-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1a17b-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1a17b-249">Range-Lower</span></span>            | <span data-ttu-id="1a17b-250">1</span><span class="sxs-lookup"><span data-stu-id="1a17b-250">1</span></span>                                 |
| <span data-ttu-id="1a17b-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1a17b-251">Range-Upper</span></span>            | <span data-ttu-id="1a17b-252">256</span><span class="sxs-lookup"><span data-stu-id="1a17b-252">256</span></span>                               |
| <span data-ttu-id="1a17b-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-253">Search-Flags</span></span>           | <span data-ttu-id="1a17b-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a17b-254">0x00000000</span></span>                        |
| <span data-ttu-id="1a17b-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1a17b-255">System-Flags</span></span>           | <span data-ttu-id="1a17b-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1a17b-256">0x00000010</span></span>                        |
| <span data-ttu-id="1a17b-257">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1a17b-257">Classes used in</span></span>        | [<span data-ttu-id="1a17b-258">**User**</span><span class="sxs-lookup"><span data-stu-id="1a17b-258">**User**</span></span>](c-user.md)<br/> |



 

 





