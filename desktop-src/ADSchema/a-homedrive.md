---
title: Home-Drive 屬性
description: 指定要對應 homeDirectory 所指定之 UNC 路徑的磁碟機號。
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- Home-Drive 屬性 AD 架構
- homeDrive 屬性 AD 架構
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce9bff87662cc3b9da962b0c5647e79e90a3068
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966362"
---
# <a name="home-drive-attribute"></a><span data-ttu-id="de194-105">Home-Drive 屬性</span><span class="sxs-lookup"><span data-stu-id="de194-105">Home-Drive attribute</span></span>

<span data-ttu-id="de194-106">指定要對應 [**homeDirectory**](a-homedirectory.md)所指定之 UNC 路徑的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="de194-106">Specifies the drive letter to which to map the UNC path specified by [**homeDirectory**](a-homedirectory.md).</span></span> <span data-ttu-id="de194-107">磁碟機號必須以 *r \* \* *：** 格式指定，其中 *r* 是要對應之磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="de194-107">The drive letter must be specified in the form *DriveLetter\*\*\*:*\* where *DriveLetter* is the letter of the drive to map.</span></span> <span data-ttu-id="de194-108">*R* 必須是單一大寫字母和冒號 (： ) 是必要的。</span><span class="sxs-lookup"><span data-stu-id="de194-108">The *DriveLetter* must be a single, uppercase letter and the colon (:) is required.</span></span>



| <span data-ttu-id="de194-109">進入</span><span class="sxs-lookup"><span data-stu-id="de194-109">Entry</span></span> | <span data-ttu-id="de194-110">值</span><span class="sxs-lookup"><span data-stu-id="de194-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="de194-111">CN</span><span class="sxs-lookup"><span data-stu-id="de194-111">CN</span></span>                | <span data-ttu-id="de194-112">Home-Drive</span><span class="sxs-lookup"><span data-stu-id="de194-112">Home-Drive</span></span>                                                                        |
| <span data-ttu-id="de194-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="de194-113">Ldap-Display-Name</span></span> | <span data-ttu-id="de194-114">homeDrive</span><span class="sxs-lookup"><span data-stu-id="de194-114">homeDrive</span></span>                                                                         |
| <span data-ttu-id="de194-115">大小</span><span class="sxs-lookup"><span data-stu-id="de194-115">Size</span></span>              | <span data-ttu-id="de194-116">2 個位元組</span><span class="sxs-lookup"><span data-stu-id="de194-116">2 bytes</span></span>                                                                           |
| <span data-ttu-id="de194-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="de194-117">Update Privilege</span></span>  | <span data-ttu-id="de194-118">網域系統管理員會設定此值。</span><span class="sxs-lookup"><span data-stu-id="de194-118">The domain administrator sets this value.</span></span>                                         |
| <span data-ttu-id="de194-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="de194-119">Update Frequency</span></span>  | <span data-ttu-id="de194-120">當使用者的記錄建立時，以及每次主要磁碟磁碟機需要變更時。</span><span class="sxs-lookup"><span data-stu-id="de194-120">When the record of a user is created and whenever the home drive needs to change.</span></span> |
| <span data-ttu-id="de194-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de194-121">Attribute-Id</span></span>      | <span data-ttu-id="de194-122">1.2.840.113556.1.4.45</span><span class="sxs-lookup"><span data-stu-id="de194-122">1.2.840.113556.1.4.45</span></span>                                                             |
| <span data-ttu-id="de194-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="de194-123">System-Id-Guid</span></span>    | <span data-ttu-id="de194-124">bf967986-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="de194-124">bf967986-0de6-11d0-a285-00aa003049e2</span></span>                                              |
| <span data-ttu-id="de194-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="de194-125">Syntax</span></span>            | [<span data-ttu-id="de194-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="de194-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="de194-127">實作</span><span class="sxs-lookup"><span data-stu-id="de194-127">Implementations</span></span>

-   [<span data-ttu-id="de194-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="de194-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="de194-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="de194-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="de194-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="de194-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="de194-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de194-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de194-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de194-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de194-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de194-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="de194-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de194-134">Windows 2000 Server</span></span>



| <span data-ttu-id="de194-135">進入</span><span class="sxs-lookup"><span data-stu-id="de194-135">Entry</span></span> | <span data-ttu-id="de194-136">值</span><span class="sxs-lookup"><span data-stu-id="de194-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de194-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de194-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de194-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="de194-139">System-Only</span></span>            | <span data-ttu-id="de194-140">否</span><span class="sxs-lookup"><span data-stu-id="de194-140">False</span></span>                             |
| <span data-ttu-id="de194-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de194-141">Is-Single-Valued</span></span>       | <span data-ttu-id="de194-142">對</span><span class="sxs-lookup"><span data-stu-id="de194-142">True</span></span>                              |
| <span data-ttu-id="de194-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de194-143">Is Indexed</span></span>             | <span data-ttu-id="de194-144">否</span><span class="sxs-lookup"><span data-stu-id="de194-144">False</span></span>                             |
| <span data-ttu-id="de194-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de194-145">In Global Catalog</span></span>      | <span data-ttu-id="de194-146">否</span><span class="sxs-lookup"><span data-stu-id="de194-146">False</span></span>                             |
| <span data-ttu-id="de194-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de194-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="de194-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de194-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de194-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de194-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de194-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de194-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de194-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-151">Search-Flags</span></span>           | <span data-ttu-id="de194-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-152">0x00000010</span></span>                        |
| <span data-ttu-id="de194-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-153">System-Flags</span></span>           | <span data-ttu-id="de194-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-154">0x00000010</span></span>                        |
| <span data-ttu-id="de194-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de194-155">Classes used in</span></span>        | [<span data-ttu-id="de194-156">**User**</span><span class="sxs-lookup"><span data-stu-id="de194-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="de194-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de194-157">Windows Server 2003</span></span>



| <span data-ttu-id="de194-158">進入</span><span class="sxs-lookup"><span data-stu-id="de194-158">Entry</span></span> | <span data-ttu-id="de194-159">值</span><span class="sxs-lookup"><span data-stu-id="de194-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de194-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de194-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de194-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="de194-162">System-Only</span></span>            | <span data-ttu-id="de194-163">否</span><span class="sxs-lookup"><span data-stu-id="de194-163">False</span></span>                             |
| <span data-ttu-id="de194-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de194-164">Is-Single-Valued</span></span>       | <span data-ttu-id="de194-165">對</span><span class="sxs-lookup"><span data-stu-id="de194-165">True</span></span>                              |
| <span data-ttu-id="de194-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de194-166">Is Indexed</span></span>             | <span data-ttu-id="de194-167">否</span><span class="sxs-lookup"><span data-stu-id="de194-167">False</span></span>                             |
| <span data-ttu-id="de194-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de194-168">In Global Catalog</span></span>      | <span data-ttu-id="de194-169">否</span><span class="sxs-lookup"><span data-stu-id="de194-169">False</span></span>                             |
| <span data-ttu-id="de194-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de194-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="de194-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de194-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de194-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de194-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de194-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de194-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de194-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-174">Search-Flags</span></span>           | <span data-ttu-id="de194-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-175">0x00000010</span></span>                        |
| <span data-ttu-id="de194-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-176">System-Flags</span></span>           | <span data-ttu-id="de194-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-177">0x00000010</span></span>                        |
| <span data-ttu-id="de194-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de194-178">Classes used in</span></span>        | [<span data-ttu-id="de194-179">**User**</span><span class="sxs-lookup"><span data-stu-id="de194-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="de194-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="de194-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="de194-181">進入</span><span class="sxs-lookup"><span data-stu-id="de194-181">Entry</span></span> | <span data-ttu-id="de194-182">值</span><span class="sxs-lookup"><span data-stu-id="de194-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de194-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de194-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de194-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="de194-185">System-Only</span></span>            | <span data-ttu-id="de194-186">否</span><span class="sxs-lookup"><span data-stu-id="de194-186">False</span></span>                             |
| <span data-ttu-id="de194-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de194-187">Is-Single-Valued</span></span>       | <span data-ttu-id="de194-188">對</span><span class="sxs-lookup"><span data-stu-id="de194-188">True</span></span>                              |
| <span data-ttu-id="de194-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de194-189">Is Indexed</span></span>             | <span data-ttu-id="de194-190">否</span><span class="sxs-lookup"><span data-stu-id="de194-190">False</span></span>                             |
| <span data-ttu-id="de194-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de194-191">In Global Catalog</span></span>      | <span data-ttu-id="de194-192">否</span><span class="sxs-lookup"><span data-stu-id="de194-192">False</span></span>                             |
| <span data-ttu-id="de194-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de194-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="de194-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de194-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de194-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de194-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de194-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de194-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de194-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-197">Search-Flags</span></span>           | <span data-ttu-id="de194-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-198">0x00000010</span></span>                        |
| <span data-ttu-id="de194-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-199">System-Flags</span></span>           | <span data-ttu-id="de194-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-200">0x00000010</span></span>                        |
| <span data-ttu-id="de194-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de194-201">Classes used in</span></span>        | [<span data-ttu-id="de194-202">**User**</span><span class="sxs-lookup"><span data-stu-id="de194-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="de194-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de194-203">Windows Server 2008</span></span>



| <span data-ttu-id="de194-204">進入</span><span class="sxs-lookup"><span data-stu-id="de194-204">Entry</span></span> | <span data-ttu-id="de194-205">值</span><span class="sxs-lookup"><span data-stu-id="de194-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de194-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de194-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de194-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="de194-208">System-Only</span></span>            | <span data-ttu-id="de194-209">否</span><span class="sxs-lookup"><span data-stu-id="de194-209">False</span></span>                             |
| <span data-ttu-id="de194-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de194-210">Is-Single-Valued</span></span>       | <span data-ttu-id="de194-211">對</span><span class="sxs-lookup"><span data-stu-id="de194-211">True</span></span>                              |
| <span data-ttu-id="de194-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de194-212">Is Indexed</span></span>             | <span data-ttu-id="de194-213">否</span><span class="sxs-lookup"><span data-stu-id="de194-213">False</span></span>                             |
| <span data-ttu-id="de194-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de194-214">In Global Catalog</span></span>      | <span data-ttu-id="de194-215">否</span><span class="sxs-lookup"><span data-stu-id="de194-215">False</span></span>                             |
| <span data-ttu-id="de194-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de194-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="de194-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de194-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de194-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de194-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de194-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de194-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de194-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-220">Search-Flags</span></span>           | <span data-ttu-id="de194-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-221">0x00000010</span></span>                        |
| <span data-ttu-id="de194-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-222">System-Flags</span></span>           | <span data-ttu-id="de194-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-223">0x00000010</span></span>                        |
| <span data-ttu-id="de194-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de194-224">Classes used in</span></span>        | [<span data-ttu-id="de194-225">**User**</span><span class="sxs-lookup"><span data-stu-id="de194-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de194-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de194-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de194-227">進入</span><span class="sxs-lookup"><span data-stu-id="de194-227">Entry</span></span> | <span data-ttu-id="de194-228">值</span><span class="sxs-lookup"><span data-stu-id="de194-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de194-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de194-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de194-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="de194-231">System-Only</span></span>            | <span data-ttu-id="de194-232">否</span><span class="sxs-lookup"><span data-stu-id="de194-232">False</span></span>                             |
| <span data-ttu-id="de194-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de194-233">Is-Single-Valued</span></span>       | <span data-ttu-id="de194-234">對</span><span class="sxs-lookup"><span data-stu-id="de194-234">True</span></span>                              |
| <span data-ttu-id="de194-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de194-235">Is Indexed</span></span>             | <span data-ttu-id="de194-236">否</span><span class="sxs-lookup"><span data-stu-id="de194-236">False</span></span>                             |
| <span data-ttu-id="de194-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de194-237">In Global Catalog</span></span>      | <span data-ttu-id="de194-238">否</span><span class="sxs-lookup"><span data-stu-id="de194-238">False</span></span>                             |
| <span data-ttu-id="de194-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de194-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="de194-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de194-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de194-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de194-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de194-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de194-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de194-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-243">Search-Flags</span></span>           | <span data-ttu-id="de194-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-244">0x00000010</span></span>                        |
| <span data-ttu-id="de194-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-245">System-Flags</span></span>           | <span data-ttu-id="de194-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-246">0x00000010</span></span>                        |
| <span data-ttu-id="de194-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de194-247">Classes used in</span></span>        | [<span data-ttu-id="de194-248">**User**</span><span class="sxs-lookup"><span data-stu-id="de194-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de194-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de194-249">Windows Server 2012</span></span>



| <span data-ttu-id="de194-250">進入</span><span class="sxs-lookup"><span data-stu-id="de194-250">Entry</span></span> | <span data-ttu-id="de194-251">值</span><span class="sxs-lookup"><span data-stu-id="de194-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de194-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de194-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de194-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de194-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="de194-254">System-Only</span></span>            | <span data-ttu-id="de194-255">否</span><span class="sxs-lookup"><span data-stu-id="de194-255">False</span></span>                             |
| <span data-ttu-id="de194-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de194-256">Is-Single-Valued</span></span>       | <span data-ttu-id="de194-257">對</span><span class="sxs-lookup"><span data-stu-id="de194-257">True</span></span>                              |
| <span data-ttu-id="de194-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de194-258">Is Indexed</span></span>             | <span data-ttu-id="de194-259">否</span><span class="sxs-lookup"><span data-stu-id="de194-259">False</span></span>                             |
| <span data-ttu-id="de194-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de194-260">In Global Catalog</span></span>      | <span data-ttu-id="de194-261">否</span><span class="sxs-lookup"><span data-stu-id="de194-261">False</span></span>                             |
| <span data-ttu-id="de194-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de194-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="de194-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de194-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de194-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de194-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de194-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de194-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de194-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-266">Search-Flags</span></span>           | <span data-ttu-id="de194-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-267">0x00000010</span></span>                        |
| <span data-ttu-id="de194-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de194-268">System-Flags</span></span>           | <span data-ttu-id="de194-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de194-269">0x00000010</span></span>                        |
| <span data-ttu-id="de194-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de194-270">Classes used in</span></span>        | [<span data-ttu-id="de194-271">**User**</span><span class="sxs-lookup"><span data-stu-id="de194-271">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="de194-272">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de194-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de194-273">**homeDirectory**</span><span class="sxs-lookup"><span data-stu-id="de194-273">**homeDirectory**</span></span>](a-homedirectory.md)
</dt> </dl>

 

 





