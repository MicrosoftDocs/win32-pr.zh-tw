---
title: Home-Directory 屬性
description: 帳戶的主目錄。
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Home-Directory 屬性 AD 架構
- homeDirectory 屬性 AD 架構
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687103"
---
# <a name="home-directory-attribute"></a><span data-ttu-id="269a0-105">Home-Directory 屬性</span><span class="sxs-lookup"><span data-stu-id="269a0-105">Home-Directory attribute</span></span>

<span data-ttu-id="269a0-106">帳戶的主目錄。</span><span class="sxs-lookup"><span data-stu-id="269a0-106">The home directory for the account.</span></span> <span data-ttu-id="269a0-107">如果已設定 [**homeDrive**](a-homedrive.md) 並指定磁碟機號， **HOMEDIRECTORY** 必須是 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="269a0-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="269a0-108">否則， **homeDirectory** 是完整的本機路徑，包括磁碟機號 (例如 \*r ***： \\** _Directory_* _\\_ \* _資料夾_) 。</span><span class="sxs-lookup"><span data-stu-id="269a0-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="269a0-109">這個值可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="269a0-109">This value can be a null string.</span></span>



| <span data-ttu-id="269a0-110">進入</span><span class="sxs-lookup"><span data-stu-id="269a0-110">Entry</span></span> | <span data-ttu-id="269a0-111">值</span><span class="sxs-lookup"><span data-stu-id="269a0-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="269a0-112">CN</span><span class="sxs-lookup"><span data-stu-id="269a0-112">CN</span></span>                | <span data-ttu-id="269a0-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="269a0-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="269a0-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="269a0-114">Ldap-Display-Name</span></span> | <span data-ttu-id="269a0-115">homeDirectory</span><span class="sxs-lookup"><span data-stu-id="269a0-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="269a0-116">大小</span><span class="sxs-lookup"><span data-stu-id="269a0-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="269a0-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="269a0-117">Update Privilege</span></span>  | <span data-ttu-id="269a0-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="269a0-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="269a0-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="269a0-119">Update Frequency</span></span>  | <span data-ttu-id="269a0-120">當使用者的記錄建立時，以及每次主目錄需要變更時。</span><span class="sxs-lookup"><span data-stu-id="269a0-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="269a0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="269a0-121">Attribute-Id</span></span>      | <span data-ttu-id="269a0-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="269a0-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="269a0-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="269a0-123">System-Id-Guid</span></span>    | <span data-ttu-id="269a0-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="269a0-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="269a0-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="269a0-125">Syntax</span></span>            | [<span data-ttu-id="269a0-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="269a0-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="269a0-127">實作</span><span class="sxs-lookup"><span data-stu-id="269a0-127">Implementations</span></span>

-   [<span data-ttu-id="269a0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="269a0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="269a0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="269a0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="269a0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="269a0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="269a0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="269a0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="269a0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="269a0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="269a0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="269a0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="269a0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="269a0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="269a0-135">進入</span><span class="sxs-lookup"><span data-stu-id="269a0-135">Entry</span></span> | <span data-ttu-id="269a0-136">值</span><span class="sxs-lookup"><span data-stu-id="269a0-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="269a0-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="269a0-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="269a0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="269a0-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="269a0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="269a0-139">System-Only</span></span>            | <span data-ttu-id="269a0-140">否</span><span class="sxs-lookup"><span data-stu-id="269a0-140">False</span></span>                             |
| <span data-ttu-id="269a0-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="269a0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="269a0-142">對</span><span class="sxs-lookup"><span data-stu-id="269a0-142">True</span></span>                              |
| <span data-ttu-id="269a0-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="269a0-143">Is Indexed</span></span>             | <span data-ttu-id="269a0-144">否</span><span class="sxs-lookup"><span data-stu-id="269a0-144">False</span></span>                             |
| <span data-ttu-id="269a0-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="269a0-145">In Global Catalog</span></span>      | <span data-ttu-id="269a0-146">否</span><span class="sxs-lookup"><span data-stu-id="269a0-146">False</span></span>                             |
| <span data-ttu-id="269a0-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="269a0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="269a0-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="269a0-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="269a0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="269a0-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="269a0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="269a0-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="269a0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-151">Search-Flags</span></span>           | <span data-ttu-id="269a0-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-152">0x00000010</span></span>                        |
| <span data-ttu-id="269a0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-153">System-Flags</span></span>           | <span data-ttu-id="269a0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-154">0x00000010</span></span>                        |
| <span data-ttu-id="269a0-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="269a0-155">Classes used in</span></span>        | [<span data-ttu-id="269a0-156">**User**</span><span class="sxs-lookup"><span data-stu-id="269a0-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="269a0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="269a0-157">Windows Server 2003</span></span>



| <span data-ttu-id="269a0-158">進入</span><span class="sxs-lookup"><span data-stu-id="269a0-158">Entry</span></span> | <span data-ttu-id="269a0-159">值</span><span class="sxs-lookup"><span data-stu-id="269a0-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="269a0-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="269a0-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="269a0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="269a0-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="269a0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="269a0-162">System-Only</span></span>            | <span data-ttu-id="269a0-163">否</span><span class="sxs-lookup"><span data-stu-id="269a0-163">False</span></span>                             |
| <span data-ttu-id="269a0-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="269a0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="269a0-165">對</span><span class="sxs-lookup"><span data-stu-id="269a0-165">True</span></span>                              |
| <span data-ttu-id="269a0-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="269a0-166">Is Indexed</span></span>             | <span data-ttu-id="269a0-167">否</span><span class="sxs-lookup"><span data-stu-id="269a0-167">False</span></span>                             |
| <span data-ttu-id="269a0-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="269a0-168">In Global Catalog</span></span>      | <span data-ttu-id="269a0-169">否</span><span class="sxs-lookup"><span data-stu-id="269a0-169">False</span></span>                             |
| <span data-ttu-id="269a0-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="269a0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="269a0-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="269a0-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="269a0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="269a0-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="269a0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="269a0-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="269a0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-174">Search-Flags</span></span>           | <span data-ttu-id="269a0-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-175">0x00000010</span></span>                        |
| <span data-ttu-id="269a0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-176">System-Flags</span></span>           | <span data-ttu-id="269a0-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-177">0x00000010</span></span>                        |
| <span data-ttu-id="269a0-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="269a0-178">Classes used in</span></span>        | [<span data-ttu-id="269a0-179">**User**</span><span class="sxs-lookup"><span data-stu-id="269a0-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="269a0-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="269a0-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="269a0-181">進入</span><span class="sxs-lookup"><span data-stu-id="269a0-181">Entry</span></span> | <span data-ttu-id="269a0-182">值</span><span class="sxs-lookup"><span data-stu-id="269a0-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="269a0-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="269a0-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="269a0-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="269a0-185">System-Only</span></span>            | <span data-ttu-id="269a0-186">否</span><span class="sxs-lookup"><span data-stu-id="269a0-186">False</span></span>                                                                               |
| <span data-ttu-id="269a0-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="269a0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="269a0-188">對</span><span class="sxs-lookup"><span data-stu-id="269a0-188">True</span></span>                                                                                |
| <span data-ttu-id="269a0-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="269a0-189">Is Indexed</span></span>             | <span data-ttu-id="269a0-190">否</span><span class="sxs-lookup"><span data-stu-id="269a0-190">False</span></span>                                                                               |
| <span data-ttu-id="269a0-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="269a0-191">In Global Catalog</span></span>      | <span data-ttu-id="269a0-192">否</span><span class="sxs-lookup"><span data-stu-id="269a0-192">False</span></span>                                                                               |
| <span data-ttu-id="269a0-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="269a0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="269a0-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="269a0-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="269a0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="269a0-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="269a0-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-197">Search-Flags</span></span>           | <span data-ttu-id="269a0-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-199">System-Flags</span></span>           | <span data-ttu-id="269a0-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="269a0-201">Classes used in</span></span>        | [<span data-ttu-id="269a0-202">**User**</span><span class="sxs-lookup"><span data-stu-id="269a0-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="269a0-203">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="269a0-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="269a0-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="269a0-204">Windows Server 2008</span></span>



| <span data-ttu-id="269a0-205">進入</span><span class="sxs-lookup"><span data-stu-id="269a0-205">Entry</span></span> | <span data-ttu-id="269a0-206">值</span><span class="sxs-lookup"><span data-stu-id="269a0-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="269a0-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="269a0-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="269a0-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="269a0-209">System-Only</span></span>            | <span data-ttu-id="269a0-210">否</span><span class="sxs-lookup"><span data-stu-id="269a0-210">False</span></span>                                                                               |
| <span data-ttu-id="269a0-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="269a0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="269a0-212">對</span><span class="sxs-lookup"><span data-stu-id="269a0-212">True</span></span>                                                                                |
| <span data-ttu-id="269a0-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="269a0-213">Is Indexed</span></span>             | <span data-ttu-id="269a0-214">否</span><span class="sxs-lookup"><span data-stu-id="269a0-214">False</span></span>                                                                               |
| <span data-ttu-id="269a0-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="269a0-215">In Global Catalog</span></span>      | <span data-ttu-id="269a0-216">否</span><span class="sxs-lookup"><span data-stu-id="269a0-216">False</span></span>                                                                               |
| <span data-ttu-id="269a0-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="269a0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="269a0-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="269a0-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="269a0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="269a0-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="269a0-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-221">Search-Flags</span></span>           | <span data-ttu-id="269a0-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-223">System-Flags</span></span>           | <span data-ttu-id="269a0-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="269a0-225">Classes used in</span></span>        | [<span data-ttu-id="269a0-226">**User**</span><span class="sxs-lookup"><span data-stu-id="269a0-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="269a0-227">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="269a0-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="269a0-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="269a0-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="269a0-229">進入</span><span class="sxs-lookup"><span data-stu-id="269a0-229">Entry</span></span> | <span data-ttu-id="269a0-230">值</span><span class="sxs-lookup"><span data-stu-id="269a0-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="269a0-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="269a0-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="269a0-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="269a0-233">System-Only</span></span>            | <span data-ttu-id="269a0-234">否</span><span class="sxs-lookup"><span data-stu-id="269a0-234">False</span></span>                                                                               |
| <span data-ttu-id="269a0-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="269a0-235">Is-Single-Valued</span></span>       | <span data-ttu-id="269a0-236">對</span><span class="sxs-lookup"><span data-stu-id="269a0-236">True</span></span>                                                                                |
| <span data-ttu-id="269a0-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="269a0-237">Is Indexed</span></span>             | <span data-ttu-id="269a0-238">否</span><span class="sxs-lookup"><span data-stu-id="269a0-238">False</span></span>                                                                               |
| <span data-ttu-id="269a0-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="269a0-239">In Global Catalog</span></span>      | <span data-ttu-id="269a0-240">否</span><span class="sxs-lookup"><span data-stu-id="269a0-240">False</span></span>                                                                               |
| <span data-ttu-id="269a0-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="269a0-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="269a0-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="269a0-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="269a0-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="269a0-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="269a0-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-245">Search-Flags</span></span>           | <span data-ttu-id="269a0-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-247">System-Flags</span></span>           | <span data-ttu-id="269a0-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="269a0-249">Classes used in</span></span>        | [<span data-ttu-id="269a0-250">**User**</span><span class="sxs-lookup"><span data-stu-id="269a0-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="269a0-251">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="269a0-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="269a0-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="269a0-252">Windows Server 2012</span></span>



| <span data-ttu-id="269a0-253">進入</span><span class="sxs-lookup"><span data-stu-id="269a0-253">Entry</span></span> | <span data-ttu-id="269a0-254">值</span><span class="sxs-lookup"><span data-stu-id="269a0-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="269a0-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="269a0-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="269a0-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="269a0-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="269a0-257">System-Only</span></span>            | <span data-ttu-id="269a0-258">否</span><span class="sxs-lookup"><span data-stu-id="269a0-258">False</span></span>                                                                               |
| <span data-ttu-id="269a0-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="269a0-259">Is-Single-Valued</span></span>       | <span data-ttu-id="269a0-260">對</span><span class="sxs-lookup"><span data-stu-id="269a0-260">True</span></span>                                                                                |
| <span data-ttu-id="269a0-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="269a0-261">Is Indexed</span></span>             | <span data-ttu-id="269a0-262">否</span><span class="sxs-lookup"><span data-stu-id="269a0-262">False</span></span>                                                                               |
| <span data-ttu-id="269a0-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="269a0-263">In Global Catalog</span></span>      | <span data-ttu-id="269a0-264">否</span><span class="sxs-lookup"><span data-stu-id="269a0-264">False</span></span>                                                                               |
| <span data-ttu-id="269a0-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="269a0-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="269a0-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="269a0-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="269a0-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="269a0-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="269a0-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="269a0-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-269">Search-Flags</span></span>           | <span data-ttu-id="269a0-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="269a0-271">System-Flags</span></span>           | <span data-ttu-id="269a0-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="269a0-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="269a0-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="269a0-273">Classes used in</span></span>        | [<span data-ttu-id="269a0-274">**User**</span><span class="sxs-lookup"><span data-stu-id="269a0-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="269a0-275">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="269a0-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="269a0-276">另請參閱</span><span class="sxs-lookup"><span data-stu-id="269a0-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="269a0-277">**homeDrive**</span><span class="sxs-lookup"><span data-stu-id="269a0-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 





