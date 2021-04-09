---
title: 使用者共用資料夾-其他屬性
description: 指定使用者的 [其他共用檔] 資料夾的 UNC 路徑。 路徑必須是表單 \\ \\ 伺服器 \\ 共用目錄的網路 UNC 路徑 \\ 。 這個值可以是 null 字串。
ms.assetid: 7d546cda-b2c1-46a6-a3cf-a7c78ddb1422
ms.tgt_platform: multiple
keywords:
- 使用者共用資料夾-其他屬性 AD 架構
- userSharedFolderOther 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Shared-Folder-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6087a28df474ff06c1d8bf54d694176df8591b5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686935"
---
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="a59d3-107">使用者共用資料夾-其他屬性</span><span class="sxs-lookup"><span data-stu-id="a59d3-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="a59d3-108">指定使用者的 [其他共用檔] 資料夾的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="a59d3-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="a59d3-109">路徑必須是表單 **\\\\** _伺服器_ *_\\_* _共用_ *_\\_* _目錄_ 的網路 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="a59d3-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="a59d3-110">這個值可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="a59d3-110">This value can be a null string.</span></span>



| <span data-ttu-id="a59d3-111">進入</span><span class="sxs-lookup"><span data-stu-id="a59d3-111">Entry</span></span> | <span data-ttu-id="a59d3-112">值</span><span class="sxs-lookup"><span data-stu-id="a59d3-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a59d3-113">CN</span><span class="sxs-lookup"><span data-stu-id="a59d3-113">CN</span></span>                | <span data-ttu-id="a59d3-114">使用者共用資料夾-其他</span><span class="sxs-lookup"><span data-stu-id="a59d3-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="a59d3-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a59d3-115">Ldap-Display-Name</span></span> | <span data-ttu-id="a59d3-116">userSharedFolderOther</span><span class="sxs-lookup"><span data-stu-id="a59d3-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="a59d3-117">大小</span><span class="sxs-lookup"><span data-stu-id="a59d3-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="a59d3-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a59d3-118">Update Privilege</span></span>  | <span data-ttu-id="a59d3-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="a59d3-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="a59d3-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a59d3-120">Update Frequency</span></span>  | <span data-ttu-id="a59d3-121">當使用者的記錄建立時，以及每次共用資料夾需要變更時。</span><span class="sxs-lookup"><span data-stu-id="a59d3-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="a59d3-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a59d3-122">Attribute-Id</span></span>      | <span data-ttu-id="a59d3-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="a59d3-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="a59d3-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a59d3-124">System-Id-Guid</span></span>    | <span data-ttu-id="a59d3-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a59d3-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="a59d3-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="a59d3-126">Syntax</span></span>            | [<span data-ttu-id="a59d3-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a59d3-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="a59d3-128">實作</span><span class="sxs-lookup"><span data-stu-id="a59d3-128">Implementations</span></span>

-   [<span data-ttu-id="a59d3-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a59d3-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a59d3-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a59d3-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a59d3-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a59d3-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a59d3-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a59d3-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a59d3-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a59d3-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a59d3-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a59d3-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a59d3-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a59d3-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a59d3-136">進入</span><span class="sxs-lookup"><span data-stu-id="a59d3-136">Entry</span></span> | <span data-ttu-id="a59d3-137">值</span><span class="sxs-lookup"><span data-stu-id="a59d3-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a59d3-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a59d3-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a59d3-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="a59d3-140">System-Only</span></span>            | <span data-ttu-id="a59d3-141">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-141">False</span></span>                             |
| <span data-ttu-id="a59d3-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a59d3-142">Is-Single-Valued</span></span>       | <span data-ttu-id="a59d3-143">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-143">False</span></span>                             |
| <span data-ttu-id="a59d3-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a59d3-144">Is Indexed</span></span>             | <span data-ttu-id="a59d3-145">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-145">False</span></span>                             |
| <span data-ttu-id="a59d3-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a59d3-146">In Global Catalog</span></span>      | <span data-ttu-id="a59d3-147">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-147">False</span></span>                             |
| <span data-ttu-id="a59d3-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a59d3-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="a59d3-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a59d3-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a59d3-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a59d3-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a59d3-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a59d3-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a59d3-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-152">Search-Flags</span></span>           | <span data-ttu-id="a59d3-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a59d3-153">0x00000000</span></span>                        |
| <span data-ttu-id="a59d3-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-154">System-Flags</span></span>           | <span data-ttu-id="a59d3-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a59d3-155">0x00000010</span></span>                        |
| <span data-ttu-id="a59d3-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a59d3-156">Classes used in</span></span>        | [<span data-ttu-id="a59d3-157">**User**</span><span class="sxs-lookup"><span data-stu-id="a59d3-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a59d3-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a59d3-158">Windows Server 2003</span></span>



| <span data-ttu-id="a59d3-159">進入</span><span class="sxs-lookup"><span data-stu-id="a59d3-159">Entry</span></span> | <span data-ttu-id="a59d3-160">值</span><span class="sxs-lookup"><span data-stu-id="a59d3-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a59d3-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a59d3-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a59d3-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a59d3-163">System-Only</span></span>            | <span data-ttu-id="a59d3-164">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-164">False</span></span>                             |
| <span data-ttu-id="a59d3-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a59d3-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a59d3-166">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-166">False</span></span>                             |
| <span data-ttu-id="a59d3-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a59d3-167">Is Indexed</span></span>             | <span data-ttu-id="a59d3-168">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-168">False</span></span>                             |
| <span data-ttu-id="a59d3-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a59d3-169">In Global Catalog</span></span>      | <span data-ttu-id="a59d3-170">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-170">False</span></span>                             |
| <span data-ttu-id="a59d3-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a59d3-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a59d3-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a59d3-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a59d3-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a59d3-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a59d3-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a59d3-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a59d3-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-175">Search-Flags</span></span>           | <span data-ttu-id="a59d3-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a59d3-176">0x00000000</span></span>                        |
| <span data-ttu-id="a59d3-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-177">System-Flags</span></span>           | <span data-ttu-id="a59d3-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a59d3-178">0x00000010</span></span>                        |
| <span data-ttu-id="a59d3-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a59d3-179">Classes used in</span></span>        | [<span data-ttu-id="a59d3-180">**User**</span><span class="sxs-lookup"><span data-stu-id="a59d3-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a59d3-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a59d3-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a59d3-182">進入</span><span class="sxs-lookup"><span data-stu-id="a59d3-182">Entry</span></span> | <span data-ttu-id="a59d3-183">值</span><span class="sxs-lookup"><span data-stu-id="a59d3-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a59d3-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a59d3-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a59d3-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a59d3-186">System-Only</span></span>            | <span data-ttu-id="a59d3-187">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-187">False</span></span>                             |
| <span data-ttu-id="a59d3-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a59d3-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a59d3-189">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-189">False</span></span>                             |
| <span data-ttu-id="a59d3-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a59d3-190">Is Indexed</span></span>             | <span data-ttu-id="a59d3-191">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-191">False</span></span>                             |
| <span data-ttu-id="a59d3-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a59d3-192">In Global Catalog</span></span>      | <span data-ttu-id="a59d3-193">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-193">False</span></span>                             |
| <span data-ttu-id="a59d3-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a59d3-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a59d3-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a59d3-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a59d3-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a59d3-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a59d3-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a59d3-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a59d3-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-198">Search-Flags</span></span>           | <span data-ttu-id="a59d3-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a59d3-199">0x00000000</span></span>                        |
| <span data-ttu-id="a59d3-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-200">System-Flags</span></span>           | <span data-ttu-id="a59d3-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a59d3-201">0x00000010</span></span>                        |
| <span data-ttu-id="a59d3-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a59d3-202">Classes used in</span></span>        | [<span data-ttu-id="a59d3-203">**User**</span><span class="sxs-lookup"><span data-stu-id="a59d3-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a59d3-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a59d3-204">Windows Server 2008</span></span>



| <span data-ttu-id="a59d3-205">進入</span><span class="sxs-lookup"><span data-stu-id="a59d3-205">Entry</span></span> | <span data-ttu-id="a59d3-206">值</span><span class="sxs-lookup"><span data-stu-id="a59d3-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a59d3-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a59d3-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a59d3-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a59d3-209">System-Only</span></span>            | <span data-ttu-id="a59d3-210">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-210">False</span></span>                             |
| <span data-ttu-id="a59d3-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a59d3-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a59d3-212">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-212">False</span></span>                             |
| <span data-ttu-id="a59d3-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a59d3-213">Is Indexed</span></span>             | <span data-ttu-id="a59d3-214">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-214">False</span></span>                             |
| <span data-ttu-id="a59d3-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a59d3-215">In Global Catalog</span></span>      | <span data-ttu-id="a59d3-216">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-216">False</span></span>                             |
| <span data-ttu-id="a59d3-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a59d3-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a59d3-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a59d3-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a59d3-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a59d3-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a59d3-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a59d3-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a59d3-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-221">Search-Flags</span></span>           | <span data-ttu-id="a59d3-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a59d3-222">0x00000000</span></span>                        |
| <span data-ttu-id="a59d3-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-223">System-Flags</span></span>           | <span data-ttu-id="a59d3-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a59d3-224">0x00000010</span></span>                        |
| <span data-ttu-id="a59d3-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a59d3-225">Classes used in</span></span>        | [<span data-ttu-id="a59d3-226">**User**</span><span class="sxs-lookup"><span data-stu-id="a59d3-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a59d3-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a59d3-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a59d3-228">進入</span><span class="sxs-lookup"><span data-stu-id="a59d3-228">Entry</span></span> | <span data-ttu-id="a59d3-229">值</span><span class="sxs-lookup"><span data-stu-id="a59d3-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a59d3-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a59d3-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a59d3-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="a59d3-232">System-Only</span></span>            | <span data-ttu-id="a59d3-233">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-233">False</span></span>                             |
| <span data-ttu-id="a59d3-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a59d3-234">Is-Single-Valued</span></span>       | <span data-ttu-id="a59d3-235">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-235">False</span></span>                             |
| <span data-ttu-id="a59d3-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a59d3-236">Is Indexed</span></span>             | <span data-ttu-id="a59d3-237">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-237">False</span></span>                             |
| <span data-ttu-id="a59d3-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a59d3-238">In Global Catalog</span></span>      | <span data-ttu-id="a59d3-239">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-239">False</span></span>                             |
| <span data-ttu-id="a59d3-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a59d3-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="a59d3-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a59d3-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a59d3-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a59d3-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a59d3-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a59d3-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a59d3-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-244">Search-Flags</span></span>           | <span data-ttu-id="a59d3-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a59d3-245">0x00000000</span></span>                        |
| <span data-ttu-id="a59d3-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-246">System-Flags</span></span>           | <span data-ttu-id="a59d3-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a59d3-247">0x00000010</span></span>                        |
| <span data-ttu-id="a59d3-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a59d3-248">Classes used in</span></span>        | [<span data-ttu-id="a59d3-249">**User**</span><span class="sxs-lookup"><span data-stu-id="a59d3-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a59d3-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a59d3-250">Windows Server 2012</span></span>



| <span data-ttu-id="a59d3-251">進入</span><span class="sxs-lookup"><span data-stu-id="a59d3-251">Entry</span></span> | <span data-ttu-id="a59d3-252">值</span><span class="sxs-lookup"><span data-stu-id="a59d3-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a59d3-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a59d3-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a59d3-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a59d3-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="a59d3-255">System-Only</span></span>            | <span data-ttu-id="a59d3-256">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-256">False</span></span>                             |
| <span data-ttu-id="a59d3-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a59d3-257">Is-Single-Valued</span></span>       | <span data-ttu-id="a59d3-258">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-258">False</span></span>                             |
| <span data-ttu-id="a59d3-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a59d3-259">Is Indexed</span></span>             | <span data-ttu-id="a59d3-260">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-260">False</span></span>                             |
| <span data-ttu-id="a59d3-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a59d3-261">In Global Catalog</span></span>      | <span data-ttu-id="a59d3-262">否</span><span class="sxs-lookup"><span data-stu-id="a59d3-262">False</span></span>                             |
| <span data-ttu-id="a59d3-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a59d3-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="a59d3-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a59d3-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a59d3-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a59d3-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a59d3-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a59d3-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a59d3-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-267">Search-Flags</span></span>           | <span data-ttu-id="a59d3-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a59d3-268">0x00000000</span></span>                        |
| <span data-ttu-id="a59d3-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a59d3-269">System-Flags</span></span>           | <span data-ttu-id="a59d3-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a59d3-270">0x00000010</span></span>                        |
| <span data-ttu-id="a59d3-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a59d3-271">Classes used in</span></span>        | [<span data-ttu-id="a59d3-272">**User**</span><span class="sxs-lookup"><span data-stu-id="a59d3-272">**User**</span></span>](c-user.md)<br/> |



 

 





