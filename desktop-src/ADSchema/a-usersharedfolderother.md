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
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="fbb0e-107">使用者共用資料夾-其他屬性</span><span class="sxs-lookup"><span data-stu-id="fbb0e-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="fbb0e-108">指定使用者的 [其他共用檔] 資料夾的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="fbb0e-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="fbb0e-109">路徑必須是表單 **\\\\** _伺服器_ *_\\_* _共用_ *_\\_* _目錄_ 的網路 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="fbb0e-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="fbb0e-110">這個值可以是 null 字串。</span><span class="sxs-lookup"><span data-stu-id="fbb0e-110">This value can be a null string.</span></span>



| <span data-ttu-id="fbb0e-111">進入</span><span class="sxs-lookup"><span data-stu-id="fbb0e-111">Entry</span></span> | <span data-ttu-id="fbb0e-112">值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fbb0e-113">CN</span><span class="sxs-lookup"><span data-stu-id="fbb0e-113">CN</span></span>                | <span data-ttu-id="fbb0e-114">使用者共用資料夾-其他</span><span class="sxs-lookup"><span data-stu-id="fbb0e-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="fbb0e-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fbb0e-115">Ldap-Display-Name</span></span> | <span data-ttu-id="fbb0e-116">userSharedFolderOther</span><span class="sxs-lookup"><span data-stu-id="fbb0e-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="fbb0e-117">大小</span><span class="sxs-lookup"><span data-stu-id="fbb0e-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="fbb0e-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fbb0e-118">Update Privilege</span></span>  | <span data-ttu-id="fbb0e-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="fbb0e-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="fbb0e-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fbb0e-120">Update Frequency</span></span>  | <span data-ttu-id="fbb0e-121">當使用者的記錄建立時，以及每次共用資料夾需要變更時。</span><span class="sxs-lookup"><span data-stu-id="fbb0e-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="fbb0e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fbb0e-122">Attribute-Id</span></span>      | <span data-ttu-id="fbb0e-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="fbb0e-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="fbb0e-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fbb0e-124">System-Id-Guid</span></span>    | <span data-ttu-id="fbb0e-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fbb0e-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="fbb0e-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbb0e-126">Syntax</span></span>            | [<span data-ttu-id="fbb0e-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="fbb0e-128">實作</span><span class="sxs-lookup"><span data-stu-id="fbb0e-128">Implementations</span></span>

-   [<span data-ttu-id="fbb0e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fbb0e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fbb0e-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fbb0e-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fbb0e-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fbb0e-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fbb0e-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fbb0e-135">Windows 2000 Server</span></span>



| <span data-ttu-id="fbb0e-136">進入</span><span class="sxs-lookup"><span data-stu-id="fbb0e-136">Entry</span></span> | <span data-ttu-id="fbb0e-137">值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fbb0e-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fbb0e-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbb0e-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbb0e-140">System-Only</span></span>            | <span data-ttu-id="fbb0e-141">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-141">False</span></span>                             |
| <span data-ttu-id="fbb0e-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-142">Is-Single-Valued</span></span>       | <span data-ttu-id="fbb0e-143">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-143">False</span></span>                             |
| <span data-ttu-id="fbb0e-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fbb0e-144">Is Indexed</span></span>             | <span data-ttu-id="fbb0e-145">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-145">False</span></span>                             |
| <span data-ttu-id="fbb0e-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fbb0e-146">In Global Catalog</span></span>      | <span data-ttu-id="fbb0e-147">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-147">False</span></span>                             |
| <span data-ttu-id="fbb0e-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fbb0e-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbb0e-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fbb0e-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fbb0e-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbb0e-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbb0e-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-152">Search-Flags</span></span>           | <span data-ttu-id="fbb0e-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbb0e-153">0x00000000</span></span>                        |
| <span data-ttu-id="fbb0e-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-154">System-Flags</span></span>           | <span data-ttu-id="fbb0e-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbb0e-155">0x00000010</span></span>                        |
| <span data-ttu-id="fbb0e-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fbb0e-156">Classes used in</span></span>        | [<span data-ttu-id="fbb0e-157">**User**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fbb0e-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbb0e-158">Windows Server 2003</span></span>



| <span data-ttu-id="fbb0e-159">進入</span><span class="sxs-lookup"><span data-stu-id="fbb0e-159">Entry</span></span> | <span data-ttu-id="fbb0e-160">值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fbb0e-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fbb0e-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbb0e-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbb0e-163">System-Only</span></span>            | <span data-ttu-id="fbb0e-164">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-164">False</span></span>                             |
| <span data-ttu-id="fbb0e-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-165">Is-Single-Valued</span></span>       | <span data-ttu-id="fbb0e-166">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-166">False</span></span>                             |
| <span data-ttu-id="fbb0e-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fbb0e-167">Is Indexed</span></span>             | <span data-ttu-id="fbb0e-168">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-168">False</span></span>                             |
| <span data-ttu-id="fbb0e-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fbb0e-169">In Global Catalog</span></span>      | <span data-ttu-id="fbb0e-170">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-170">False</span></span>                             |
| <span data-ttu-id="fbb0e-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fbb0e-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbb0e-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fbb0e-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fbb0e-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbb0e-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbb0e-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-175">Search-Flags</span></span>           | <span data-ttu-id="fbb0e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbb0e-176">0x00000000</span></span>                        |
| <span data-ttu-id="fbb0e-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-177">System-Flags</span></span>           | <span data-ttu-id="fbb0e-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbb0e-178">0x00000010</span></span>                        |
| <span data-ttu-id="fbb0e-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fbb0e-179">Classes used in</span></span>        | [<span data-ttu-id="fbb0e-180">**User**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fbb0e-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fbb0e-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fbb0e-182">進入</span><span class="sxs-lookup"><span data-stu-id="fbb0e-182">Entry</span></span> | <span data-ttu-id="fbb0e-183">值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fbb0e-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fbb0e-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbb0e-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbb0e-186">System-Only</span></span>            | <span data-ttu-id="fbb0e-187">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-187">False</span></span>                             |
| <span data-ttu-id="fbb0e-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="fbb0e-189">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-189">False</span></span>                             |
| <span data-ttu-id="fbb0e-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fbb0e-190">Is Indexed</span></span>             | <span data-ttu-id="fbb0e-191">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-191">False</span></span>                             |
| <span data-ttu-id="fbb0e-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fbb0e-192">In Global Catalog</span></span>      | <span data-ttu-id="fbb0e-193">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-193">False</span></span>                             |
| <span data-ttu-id="fbb0e-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fbb0e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbb0e-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fbb0e-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fbb0e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbb0e-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbb0e-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-198">Search-Flags</span></span>           | <span data-ttu-id="fbb0e-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbb0e-199">0x00000000</span></span>                        |
| <span data-ttu-id="fbb0e-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-200">System-Flags</span></span>           | <span data-ttu-id="fbb0e-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbb0e-201">0x00000010</span></span>                        |
| <span data-ttu-id="fbb0e-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fbb0e-202">Classes used in</span></span>        | [<span data-ttu-id="fbb0e-203">**User**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fbb0e-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbb0e-204">Windows Server 2008</span></span>



| <span data-ttu-id="fbb0e-205">進入</span><span class="sxs-lookup"><span data-stu-id="fbb0e-205">Entry</span></span> | <span data-ttu-id="fbb0e-206">值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fbb0e-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fbb0e-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbb0e-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbb0e-209">System-Only</span></span>            | <span data-ttu-id="fbb0e-210">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-210">False</span></span>                             |
| <span data-ttu-id="fbb0e-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-211">Is-Single-Valued</span></span>       | <span data-ttu-id="fbb0e-212">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-212">False</span></span>                             |
| <span data-ttu-id="fbb0e-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fbb0e-213">Is Indexed</span></span>             | <span data-ttu-id="fbb0e-214">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-214">False</span></span>                             |
| <span data-ttu-id="fbb0e-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fbb0e-215">In Global Catalog</span></span>      | <span data-ttu-id="fbb0e-216">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-216">False</span></span>                             |
| <span data-ttu-id="fbb0e-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fbb0e-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbb0e-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fbb0e-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fbb0e-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbb0e-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbb0e-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-221">Search-Flags</span></span>           | <span data-ttu-id="fbb0e-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbb0e-222">0x00000000</span></span>                        |
| <span data-ttu-id="fbb0e-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-223">System-Flags</span></span>           | <span data-ttu-id="fbb0e-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbb0e-224">0x00000010</span></span>                        |
| <span data-ttu-id="fbb0e-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fbb0e-225">Classes used in</span></span>        | [<span data-ttu-id="fbb0e-226">**User**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fbb0e-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbb0e-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fbb0e-228">進入</span><span class="sxs-lookup"><span data-stu-id="fbb0e-228">Entry</span></span> | <span data-ttu-id="fbb0e-229">值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fbb0e-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fbb0e-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbb0e-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbb0e-232">System-Only</span></span>            | <span data-ttu-id="fbb0e-233">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-233">False</span></span>                             |
| <span data-ttu-id="fbb0e-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-234">Is-Single-Valued</span></span>       | <span data-ttu-id="fbb0e-235">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-235">False</span></span>                             |
| <span data-ttu-id="fbb0e-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fbb0e-236">Is Indexed</span></span>             | <span data-ttu-id="fbb0e-237">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-237">False</span></span>                             |
| <span data-ttu-id="fbb0e-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fbb0e-238">In Global Catalog</span></span>      | <span data-ttu-id="fbb0e-239">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-239">False</span></span>                             |
| <span data-ttu-id="fbb0e-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fbb0e-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbb0e-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fbb0e-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fbb0e-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbb0e-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbb0e-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-244">Search-Flags</span></span>           | <span data-ttu-id="fbb0e-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbb0e-245">0x00000000</span></span>                        |
| <span data-ttu-id="fbb0e-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-246">System-Flags</span></span>           | <span data-ttu-id="fbb0e-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbb0e-247">0x00000010</span></span>                        |
| <span data-ttu-id="fbb0e-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fbb0e-248">Classes used in</span></span>        | [<span data-ttu-id="fbb0e-249">**User**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fbb0e-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbb0e-250">Windows Server 2012</span></span>



| <span data-ttu-id="fbb0e-251">進入</span><span class="sxs-lookup"><span data-stu-id="fbb0e-251">Entry</span></span> | <span data-ttu-id="fbb0e-252">值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="fbb0e-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fbb0e-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbb0e-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="fbb0e-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbb0e-255">System-Only</span></span>            | <span data-ttu-id="fbb0e-256">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-256">False</span></span>                             |
| <span data-ttu-id="fbb0e-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fbb0e-257">Is-Single-Valued</span></span>       | <span data-ttu-id="fbb0e-258">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-258">False</span></span>                             |
| <span data-ttu-id="fbb0e-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fbb0e-259">Is Indexed</span></span>             | <span data-ttu-id="fbb0e-260">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-260">False</span></span>                             |
| <span data-ttu-id="fbb0e-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fbb0e-261">In Global Catalog</span></span>      | <span data-ttu-id="fbb0e-262">否</span><span class="sxs-lookup"><span data-stu-id="fbb0e-262">False</span></span>                             |
| <span data-ttu-id="fbb0e-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fbb0e-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbb0e-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fbb0e-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="fbb0e-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbb0e-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbb0e-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="fbb0e-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-267">Search-Flags</span></span>           | <span data-ttu-id="fbb0e-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbb0e-268">0x00000000</span></span>                        |
| <span data-ttu-id="fbb0e-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbb0e-269">System-Flags</span></span>           | <span data-ttu-id="fbb0e-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbb0e-270">0x00000010</span></span>                        |
| <span data-ttu-id="fbb0e-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fbb0e-271">Classes used in</span></span>        | [<span data-ttu-id="fbb0e-272">**User**</span><span class="sxs-lookup"><span data-stu-id="fbb0e-272">**User**</span></span>](c-user.md)<br/> |



 

 





