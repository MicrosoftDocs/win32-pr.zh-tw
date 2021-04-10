---
title: 使用者共用資料夾屬性
description: 指定使用者的 [共用文件] 資料夾的 UNC 路徑。 路徑必須是表單 \\ \\ 伺服器 \\ 共用目錄的網路 UNC 路徑 \\ 。 這個值可以是 null 字串。
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- 使用者共用資料夾屬性 AD 架構
- userSharedFolder 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20e9772302e79837fccd301943554191cf3b862
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935473"
---
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="432ed-107">使用者共用資料夾屬性</span><span class="sxs-lookup"><span data-stu-id="432ed-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="432ed-108">指定使用者的 [共用文件] 資料夾的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="432ed-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="432ed-109">路徑必須是表單 **\\\\** _伺服器_ *_\\_* _共用_ *_\\_* _目錄_ 的網路 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="432ed-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="432ed-110">這個值可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="432ed-110">This value can be a null string.</span></span>



| <span data-ttu-id="432ed-111">進入</span><span class="sxs-lookup"><span data-stu-id="432ed-111">Entry</span></span> | <span data-ttu-id="432ed-112">值</span><span class="sxs-lookup"><span data-stu-id="432ed-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="432ed-113">CN</span><span class="sxs-lookup"><span data-stu-id="432ed-113">CN</span></span>                | <span data-ttu-id="432ed-114">使用者共用資料夾</span><span class="sxs-lookup"><span data-stu-id="432ed-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="432ed-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="432ed-115">Ldap-Display-Name</span></span> | <span data-ttu-id="432ed-116">userSharedFolder</span><span class="sxs-lookup"><span data-stu-id="432ed-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="432ed-117">大小</span><span class="sxs-lookup"><span data-stu-id="432ed-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="432ed-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="432ed-118">Update Privilege</span></span>  | <span data-ttu-id="432ed-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="432ed-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="432ed-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="432ed-120">Update Frequency</span></span>  | <span data-ttu-id="432ed-121">當使用者的記錄建立時，以及每次共用資料夾需要變更時。</span><span class="sxs-lookup"><span data-stu-id="432ed-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="432ed-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="432ed-122">Attribute-Id</span></span>      | <span data-ttu-id="432ed-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="432ed-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="432ed-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="432ed-124">System-Id-Guid</span></span>    | <span data-ttu-id="432ed-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="432ed-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="432ed-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="432ed-126">Syntax</span></span>            | [<span data-ttu-id="432ed-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="432ed-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="432ed-128">實作</span><span class="sxs-lookup"><span data-stu-id="432ed-128">Implementations</span></span>

-   [<span data-ttu-id="432ed-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="432ed-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="432ed-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="432ed-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="432ed-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="432ed-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="432ed-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="432ed-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="432ed-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="432ed-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="432ed-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="432ed-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="432ed-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="432ed-135">Windows 2000 Server</span></span>



| <span data-ttu-id="432ed-136">進入</span><span class="sxs-lookup"><span data-stu-id="432ed-136">Entry</span></span> | <span data-ttu-id="432ed-137">值</span><span class="sxs-lookup"><span data-stu-id="432ed-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="432ed-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="432ed-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="432ed-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="432ed-140">System-Only</span></span>            | <span data-ttu-id="432ed-141">否</span><span class="sxs-lookup"><span data-stu-id="432ed-141">False</span></span>                             |
| <span data-ttu-id="432ed-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="432ed-142">Is-Single-Valued</span></span>       | <span data-ttu-id="432ed-143">對</span><span class="sxs-lookup"><span data-stu-id="432ed-143">True</span></span>                              |
| <span data-ttu-id="432ed-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="432ed-144">Is Indexed</span></span>             | <span data-ttu-id="432ed-145">否</span><span class="sxs-lookup"><span data-stu-id="432ed-145">False</span></span>                             |
| <span data-ttu-id="432ed-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="432ed-146">In Global Catalog</span></span>      | <span data-ttu-id="432ed-147">否</span><span class="sxs-lookup"><span data-stu-id="432ed-147">False</span></span>                             |
| <span data-ttu-id="432ed-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="432ed-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="432ed-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="432ed-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="432ed-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="432ed-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="432ed-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="432ed-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="432ed-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-152">Search-Flags</span></span>           | <span data-ttu-id="432ed-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="432ed-153">0x00000000</span></span>                        |
| <span data-ttu-id="432ed-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-154">System-Flags</span></span>           | <span data-ttu-id="432ed-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="432ed-155">0x00000010</span></span>                        |
| <span data-ttu-id="432ed-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="432ed-156">Classes used in</span></span>        | [<span data-ttu-id="432ed-157">**User**</span><span class="sxs-lookup"><span data-stu-id="432ed-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="432ed-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="432ed-158">Windows Server 2003</span></span>



| <span data-ttu-id="432ed-159">進入</span><span class="sxs-lookup"><span data-stu-id="432ed-159">Entry</span></span> | <span data-ttu-id="432ed-160">值</span><span class="sxs-lookup"><span data-stu-id="432ed-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="432ed-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="432ed-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="432ed-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="432ed-163">System-Only</span></span>            | <span data-ttu-id="432ed-164">否</span><span class="sxs-lookup"><span data-stu-id="432ed-164">False</span></span>                             |
| <span data-ttu-id="432ed-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="432ed-165">Is-Single-Valued</span></span>       | <span data-ttu-id="432ed-166">對</span><span class="sxs-lookup"><span data-stu-id="432ed-166">True</span></span>                              |
| <span data-ttu-id="432ed-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="432ed-167">Is Indexed</span></span>             | <span data-ttu-id="432ed-168">否</span><span class="sxs-lookup"><span data-stu-id="432ed-168">False</span></span>                             |
| <span data-ttu-id="432ed-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="432ed-169">In Global Catalog</span></span>      | <span data-ttu-id="432ed-170">否</span><span class="sxs-lookup"><span data-stu-id="432ed-170">False</span></span>                             |
| <span data-ttu-id="432ed-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="432ed-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="432ed-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="432ed-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="432ed-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="432ed-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="432ed-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="432ed-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="432ed-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-175">Search-Flags</span></span>           | <span data-ttu-id="432ed-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="432ed-176">0x00000000</span></span>                        |
| <span data-ttu-id="432ed-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-177">System-Flags</span></span>           | <span data-ttu-id="432ed-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="432ed-178">0x00000010</span></span>                        |
| <span data-ttu-id="432ed-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="432ed-179">Classes used in</span></span>        | [<span data-ttu-id="432ed-180">**User**</span><span class="sxs-lookup"><span data-stu-id="432ed-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="432ed-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="432ed-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="432ed-182">進入</span><span class="sxs-lookup"><span data-stu-id="432ed-182">Entry</span></span> | <span data-ttu-id="432ed-183">值</span><span class="sxs-lookup"><span data-stu-id="432ed-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="432ed-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="432ed-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="432ed-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="432ed-186">System-Only</span></span>            | <span data-ttu-id="432ed-187">否</span><span class="sxs-lookup"><span data-stu-id="432ed-187">False</span></span>                             |
| <span data-ttu-id="432ed-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="432ed-188">Is-Single-Valued</span></span>       | <span data-ttu-id="432ed-189">對</span><span class="sxs-lookup"><span data-stu-id="432ed-189">True</span></span>                              |
| <span data-ttu-id="432ed-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="432ed-190">Is Indexed</span></span>             | <span data-ttu-id="432ed-191">否</span><span class="sxs-lookup"><span data-stu-id="432ed-191">False</span></span>                             |
| <span data-ttu-id="432ed-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="432ed-192">In Global Catalog</span></span>      | <span data-ttu-id="432ed-193">否</span><span class="sxs-lookup"><span data-stu-id="432ed-193">False</span></span>                             |
| <span data-ttu-id="432ed-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="432ed-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="432ed-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="432ed-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="432ed-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="432ed-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="432ed-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="432ed-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="432ed-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-198">Search-Flags</span></span>           | <span data-ttu-id="432ed-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="432ed-199">0x00000000</span></span>                        |
| <span data-ttu-id="432ed-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-200">System-Flags</span></span>           | <span data-ttu-id="432ed-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="432ed-201">0x00000010</span></span>                        |
| <span data-ttu-id="432ed-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="432ed-202">Classes used in</span></span>        | [<span data-ttu-id="432ed-203">**User**</span><span class="sxs-lookup"><span data-stu-id="432ed-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="432ed-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="432ed-204">Windows Server 2008</span></span>



| <span data-ttu-id="432ed-205">進入</span><span class="sxs-lookup"><span data-stu-id="432ed-205">Entry</span></span> | <span data-ttu-id="432ed-206">值</span><span class="sxs-lookup"><span data-stu-id="432ed-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="432ed-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="432ed-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="432ed-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="432ed-209">System-Only</span></span>            | <span data-ttu-id="432ed-210">否</span><span class="sxs-lookup"><span data-stu-id="432ed-210">False</span></span>                             |
| <span data-ttu-id="432ed-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="432ed-211">Is-Single-Valued</span></span>       | <span data-ttu-id="432ed-212">對</span><span class="sxs-lookup"><span data-stu-id="432ed-212">True</span></span>                              |
| <span data-ttu-id="432ed-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="432ed-213">Is Indexed</span></span>             | <span data-ttu-id="432ed-214">否</span><span class="sxs-lookup"><span data-stu-id="432ed-214">False</span></span>                             |
| <span data-ttu-id="432ed-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="432ed-215">In Global Catalog</span></span>      | <span data-ttu-id="432ed-216">否</span><span class="sxs-lookup"><span data-stu-id="432ed-216">False</span></span>                             |
| <span data-ttu-id="432ed-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="432ed-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="432ed-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="432ed-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="432ed-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="432ed-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="432ed-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="432ed-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="432ed-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-221">Search-Flags</span></span>           | <span data-ttu-id="432ed-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="432ed-222">0x00000000</span></span>                        |
| <span data-ttu-id="432ed-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-223">System-Flags</span></span>           | <span data-ttu-id="432ed-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="432ed-224">0x00000010</span></span>                        |
| <span data-ttu-id="432ed-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="432ed-225">Classes used in</span></span>        | [<span data-ttu-id="432ed-226">**User**</span><span class="sxs-lookup"><span data-stu-id="432ed-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="432ed-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="432ed-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="432ed-228">進入</span><span class="sxs-lookup"><span data-stu-id="432ed-228">Entry</span></span> | <span data-ttu-id="432ed-229">值</span><span class="sxs-lookup"><span data-stu-id="432ed-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="432ed-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="432ed-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="432ed-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="432ed-232">System-Only</span></span>            | <span data-ttu-id="432ed-233">否</span><span class="sxs-lookup"><span data-stu-id="432ed-233">False</span></span>                             |
| <span data-ttu-id="432ed-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="432ed-234">Is-Single-Valued</span></span>       | <span data-ttu-id="432ed-235">對</span><span class="sxs-lookup"><span data-stu-id="432ed-235">True</span></span>                              |
| <span data-ttu-id="432ed-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="432ed-236">Is Indexed</span></span>             | <span data-ttu-id="432ed-237">否</span><span class="sxs-lookup"><span data-stu-id="432ed-237">False</span></span>                             |
| <span data-ttu-id="432ed-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="432ed-238">In Global Catalog</span></span>      | <span data-ttu-id="432ed-239">否</span><span class="sxs-lookup"><span data-stu-id="432ed-239">False</span></span>                             |
| <span data-ttu-id="432ed-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="432ed-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="432ed-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="432ed-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="432ed-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="432ed-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="432ed-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="432ed-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="432ed-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-244">Search-Flags</span></span>           | <span data-ttu-id="432ed-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="432ed-245">0x00000000</span></span>                        |
| <span data-ttu-id="432ed-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-246">System-Flags</span></span>           | <span data-ttu-id="432ed-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="432ed-247">0x00000010</span></span>                        |
| <span data-ttu-id="432ed-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="432ed-248">Classes used in</span></span>        | [<span data-ttu-id="432ed-249">**User**</span><span class="sxs-lookup"><span data-stu-id="432ed-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="432ed-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="432ed-250">Windows Server 2012</span></span>



| <span data-ttu-id="432ed-251">進入</span><span class="sxs-lookup"><span data-stu-id="432ed-251">Entry</span></span> | <span data-ttu-id="432ed-252">值</span><span class="sxs-lookup"><span data-stu-id="432ed-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="432ed-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="432ed-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="432ed-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="432ed-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="432ed-255">System-Only</span></span>            | <span data-ttu-id="432ed-256">否</span><span class="sxs-lookup"><span data-stu-id="432ed-256">False</span></span>                             |
| <span data-ttu-id="432ed-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="432ed-257">Is-Single-Valued</span></span>       | <span data-ttu-id="432ed-258">對</span><span class="sxs-lookup"><span data-stu-id="432ed-258">True</span></span>                              |
| <span data-ttu-id="432ed-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="432ed-259">Is Indexed</span></span>             | <span data-ttu-id="432ed-260">否</span><span class="sxs-lookup"><span data-stu-id="432ed-260">False</span></span>                             |
| <span data-ttu-id="432ed-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="432ed-261">In Global Catalog</span></span>      | <span data-ttu-id="432ed-262">否</span><span class="sxs-lookup"><span data-stu-id="432ed-262">False</span></span>                             |
| <span data-ttu-id="432ed-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="432ed-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="432ed-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="432ed-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="432ed-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="432ed-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="432ed-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="432ed-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="432ed-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-267">Search-Flags</span></span>           | <span data-ttu-id="432ed-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="432ed-268">0x00000000</span></span>                        |
| <span data-ttu-id="432ed-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="432ed-269">System-Flags</span></span>           | <span data-ttu-id="432ed-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="432ed-270">0x00000010</span></span>                        |
| <span data-ttu-id="432ed-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="432ed-271">Classes used in</span></span>        | [<span data-ttu-id="432ed-272">**User**</span><span class="sxs-lookup"><span data-stu-id="432ed-272">**User**</span></span>](c-user.md)<br/> |



 

 





