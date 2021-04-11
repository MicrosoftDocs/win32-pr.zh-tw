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
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="a58d7-107">使用者共用資料夾屬性</span><span class="sxs-lookup"><span data-stu-id="a58d7-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="a58d7-108">指定使用者的 [共用文件] 資料夾的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="a58d7-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="a58d7-109">路徑必須是表單 **\\\\** _伺服器_ *_\\_* _共用_ *_\\_* _目錄_ 的網路 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="a58d7-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="a58d7-110">這個值可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="a58d7-110">This value can be a null string.</span></span>



| <span data-ttu-id="a58d7-111">進入</span><span class="sxs-lookup"><span data-stu-id="a58d7-111">Entry</span></span> | <span data-ttu-id="a58d7-112">值</span><span class="sxs-lookup"><span data-stu-id="a58d7-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a58d7-113">CN</span><span class="sxs-lookup"><span data-stu-id="a58d7-113">CN</span></span>                | <span data-ttu-id="a58d7-114">使用者共用資料夾</span><span class="sxs-lookup"><span data-stu-id="a58d7-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="a58d7-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a58d7-115">Ldap-Display-Name</span></span> | <span data-ttu-id="a58d7-116">userSharedFolder</span><span class="sxs-lookup"><span data-stu-id="a58d7-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="a58d7-117">大小</span><span class="sxs-lookup"><span data-stu-id="a58d7-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="a58d7-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a58d7-118">Update Privilege</span></span>  | <span data-ttu-id="a58d7-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="a58d7-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="a58d7-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a58d7-120">Update Frequency</span></span>  | <span data-ttu-id="a58d7-121">當使用者的記錄建立時，以及每次共用資料夾需要變更時。</span><span class="sxs-lookup"><span data-stu-id="a58d7-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="a58d7-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a58d7-122">Attribute-Id</span></span>      | <span data-ttu-id="a58d7-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="a58d7-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="a58d7-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a58d7-124">System-Id-Guid</span></span>    | <span data-ttu-id="a58d7-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a58d7-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="a58d7-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="a58d7-126">Syntax</span></span>            | [<span data-ttu-id="a58d7-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a58d7-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="a58d7-128">實作</span><span class="sxs-lookup"><span data-stu-id="a58d7-128">Implementations</span></span>

-   [<span data-ttu-id="a58d7-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a58d7-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a58d7-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a58d7-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a58d7-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a58d7-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a58d7-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a58d7-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a58d7-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a58d7-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a58d7-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a58d7-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a58d7-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a58d7-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a58d7-136">進入</span><span class="sxs-lookup"><span data-stu-id="a58d7-136">Entry</span></span> | <span data-ttu-id="a58d7-137">值</span><span class="sxs-lookup"><span data-stu-id="a58d7-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a58d7-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a58d7-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a58d7-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="a58d7-140">System-Only</span></span>            | <span data-ttu-id="a58d7-141">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-141">False</span></span>                             |
| <span data-ttu-id="a58d7-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a58d7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="a58d7-143">對</span><span class="sxs-lookup"><span data-stu-id="a58d7-143">True</span></span>                              |
| <span data-ttu-id="a58d7-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a58d7-144">Is Indexed</span></span>             | <span data-ttu-id="a58d7-145">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-145">False</span></span>                             |
| <span data-ttu-id="a58d7-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a58d7-146">In Global Catalog</span></span>      | <span data-ttu-id="a58d7-147">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-147">False</span></span>                             |
| <span data-ttu-id="a58d7-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a58d7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="a58d7-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a58d7-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a58d7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a58d7-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a58d7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a58d7-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a58d7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-152">Search-Flags</span></span>           | <span data-ttu-id="a58d7-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a58d7-153">0x00000000</span></span>                        |
| <span data-ttu-id="a58d7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-154">System-Flags</span></span>           | <span data-ttu-id="a58d7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a58d7-155">0x00000010</span></span>                        |
| <span data-ttu-id="a58d7-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a58d7-156">Classes used in</span></span>        | [<span data-ttu-id="a58d7-157">**User**</span><span class="sxs-lookup"><span data-stu-id="a58d7-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a58d7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a58d7-158">Windows Server 2003</span></span>



| <span data-ttu-id="a58d7-159">進入</span><span class="sxs-lookup"><span data-stu-id="a58d7-159">Entry</span></span> | <span data-ttu-id="a58d7-160">值</span><span class="sxs-lookup"><span data-stu-id="a58d7-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a58d7-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a58d7-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a58d7-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a58d7-163">System-Only</span></span>            | <span data-ttu-id="a58d7-164">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-164">False</span></span>                             |
| <span data-ttu-id="a58d7-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a58d7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a58d7-166">對</span><span class="sxs-lookup"><span data-stu-id="a58d7-166">True</span></span>                              |
| <span data-ttu-id="a58d7-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a58d7-167">Is Indexed</span></span>             | <span data-ttu-id="a58d7-168">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-168">False</span></span>                             |
| <span data-ttu-id="a58d7-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a58d7-169">In Global Catalog</span></span>      | <span data-ttu-id="a58d7-170">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-170">False</span></span>                             |
| <span data-ttu-id="a58d7-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a58d7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a58d7-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a58d7-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a58d7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a58d7-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a58d7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a58d7-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a58d7-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-175">Search-Flags</span></span>           | <span data-ttu-id="a58d7-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a58d7-176">0x00000000</span></span>                        |
| <span data-ttu-id="a58d7-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-177">System-Flags</span></span>           | <span data-ttu-id="a58d7-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a58d7-178">0x00000010</span></span>                        |
| <span data-ttu-id="a58d7-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a58d7-179">Classes used in</span></span>        | [<span data-ttu-id="a58d7-180">**User**</span><span class="sxs-lookup"><span data-stu-id="a58d7-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a58d7-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a58d7-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a58d7-182">進入</span><span class="sxs-lookup"><span data-stu-id="a58d7-182">Entry</span></span> | <span data-ttu-id="a58d7-183">值</span><span class="sxs-lookup"><span data-stu-id="a58d7-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a58d7-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a58d7-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a58d7-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a58d7-186">System-Only</span></span>            | <span data-ttu-id="a58d7-187">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-187">False</span></span>                             |
| <span data-ttu-id="a58d7-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a58d7-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a58d7-189">對</span><span class="sxs-lookup"><span data-stu-id="a58d7-189">True</span></span>                              |
| <span data-ttu-id="a58d7-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a58d7-190">Is Indexed</span></span>             | <span data-ttu-id="a58d7-191">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-191">False</span></span>                             |
| <span data-ttu-id="a58d7-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a58d7-192">In Global Catalog</span></span>      | <span data-ttu-id="a58d7-193">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-193">False</span></span>                             |
| <span data-ttu-id="a58d7-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a58d7-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a58d7-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a58d7-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a58d7-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a58d7-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a58d7-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a58d7-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a58d7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-198">Search-Flags</span></span>           | <span data-ttu-id="a58d7-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a58d7-199">0x00000000</span></span>                        |
| <span data-ttu-id="a58d7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-200">System-Flags</span></span>           | <span data-ttu-id="a58d7-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a58d7-201">0x00000010</span></span>                        |
| <span data-ttu-id="a58d7-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a58d7-202">Classes used in</span></span>        | [<span data-ttu-id="a58d7-203">**User**</span><span class="sxs-lookup"><span data-stu-id="a58d7-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a58d7-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a58d7-204">Windows Server 2008</span></span>



| <span data-ttu-id="a58d7-205">進入</span><span class="sxs-lookup"><span data-stu-id="a58d7-205">Entry</span></span> | <span data-ttu-id="a58d7-206">值</span><span class="sxs-lookup"><span data-stu-id="a58d7-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a58d7-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a58d7-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a58d7-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a58d7-209">System-Only</span></span>            | <span data-ttu-id="a58d7-210">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-210">False</span></span>                             |
| <span data-ttu-id="a58d7-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a58d7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a58d7-212">對</span><span class="sxs-lookup"><span data-stu-id="a58d7-212">True</span></span>                              |
| <span data-ttu-id="a58d7-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a58d7-213">Is Indexed</span></span>             | <span data-ttu-id="a58d7-214">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-214">False</span></span>                             |
| <span data-ttu-id="a58d7-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a58d7-215">In Global Catalog</span></span>      | <span data-ttu-id="a58d7-216">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-216">False</span></span>                             |
| <span data-ttu-id="a58d7-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a58d7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a58d7-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a58d7-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a58d7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a58d7-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a58d7-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a58d7-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a58d7-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-221">Search-Flags</span></span>           | <span data-ttu-id="a58d7-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a58d7-222">0x00000000</span></span>                        |
| <span data-ttu-id="a58d7-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-223">System-Flags</span></span>           | <span data-ttu-id="a58d7-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a58d7-224">0x00000010</span></span>                        |
| <span data-ttu-id="a58d7-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a58d7-225">Classes used in</span></span>        | [<span data-ttu-id="a58d7-226">**User**</span><span class="sxs-lookup"><span data-stu-id="a58d7-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a58d7-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a58d7-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a58d7-228">進入</span><span class="sxs-lookup"><span data-stu-id="a58d7-228">Entry</span></span> | <span data-ttu-id="a58d7-229">值</span><span class="sxs-lookup"><span data-stu-id="a58d7-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a58d7-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a58d7-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a58d7-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="a58d7-232">System-Only</span></span>            | <span data-ttu-id="a58d7-233">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-233">False</span></span>                             |
| <span data-ttu-id="a58d7-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a58d7-234">Is-Single-Valued</span></span>       | <span data-ttu-id="a58d7-235">對</span><span class="sxs-lookup"><span data-stu-id="a58d7-235">True</span></span>                              |
| <span data-ttu-id="a58d7-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a58d7-236">Is Indexed</span></span>             | <span data-ttu-id="a58d7-237">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-237">False</span></span>                             |
| <span data-ttu-id="a58d7-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a58d7-238">In Global Catalog</span></span>      | <span data-ttu-id="a58d7-239">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-239">False</span></span>                             |
| <span data-ttu-id="a58d7-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a58d7-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="a58d7-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a58d7-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a58d7-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a58d7-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a58d7-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a58d7-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a58d7-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-244">Search-Flags</span></span>           | <span data-ttu-id="a58d7-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a58d7-245">0x00000000</span></span>                        |
| <span data-ttu-id="a58d7-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-246">System-Flags</span></span>           | <span data-ttu-id="a58d7-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a58d7-247">0x00000010</span></span>                        |
| <span data-ttu-id="a58d7-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a58d7-248">Classes used in</span></span>        | [<span data-ttu-id="a58d7-249">**User**</span><span class="sxs-lookup"><span data-stu-id="a58d7-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a58d7-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a58d7-250">Windows Server 2012</span></span>



| <span data-ttu-id="a58d7-251">進入</span><span class="sxs-lookup"><span data-stu-id="a58d7-251">Entry</span></span> | <span data-ttu-id="a58d7-252">值</span><span class="sxs-lookup"><span data-stu-id="a58d7-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a58d7-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a58d7-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a58d7-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a58d7-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="a58d7-255">System-Only</span></span>            | <span data-ttu-id="a58d7-256">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-256">False</span></span>                             |
| <span data-ttu-id="a58d7-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a58d7-257">Is-Single-Valued</span></span>       | <span data-ttu-id="a58d7-258">對</span><span class="sxs-lookup"><span data-stu-id="a58d7-258">True</span></span>                              |
| <span data-ttu-id="a58d7-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a58d7-259">Is Indexed</span></span>             | <span data-ttu-id="a58d7-260">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-260">False</span></span>                             |
| <span data-ttu-id="a58d7-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a58d7-261">In Global Catalog</span></span>      | <span data-ttu-id="a58d7-262">否</span><span class="sxs-lookup"><span data-stu-id="a58d7-262">False</span></span>                             |
| <span data-ttu-id="a58d7-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a58d7-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="a58d7-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a58d7-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a58d7-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a58d7-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a58d7-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a58d7-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a58d7-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-267">Search-Flags</span></span>           | <span data-ttu-id="a58d7-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a58d7-268">0x00000000</span></span>                        |
| <span data-ttu-id="a58d7-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a58d7-269">System-Flags</span></span>           | <span data-ttu-id="a58d7-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a58d7-270">0x00000010</span></span>                        |
| <span data-ttu-id="a58d7-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a58d7-271">Classes used in</span></span>        | [<span data-ttu-id="a58d7-272">**User**</span><span class="sxs-lookup"><span data-stu-id="a58d7-272">**User**</span></span>](c-user.md)<br/> |



 

 





