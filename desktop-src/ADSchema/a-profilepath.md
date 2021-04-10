---
title: Profile-Path 屬性
description: 指定使用者設定檔的路徑。 這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。
ms.assetid: 03891152-52c6-4799-ae79-3be284204391
ms.tgt_platform: multiple
keywords:
- Profile-Path 屬性 AD 架構
- profilePath 屬性 AD 架構
topic_type:
- apiref
api_name:
- Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d1c255843cf578301ce330b79f3ca983030952
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935500"
---
# <a name="profile-path-attribute"></a><span data-ttu-id="e672b-106">Profile-Path 屬性</span><span class="sxs-lookup"><span data-stu-id="e672b-106">Profile-Path attribute</span></span>

<span data-ttu-id="e672b-107">指定使用者設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="e672b-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="e672b-108">這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="e672b-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="e672b-109">進入</span><span class="sxs-lookup"><span data-stu-id="e672b-109">Entry</span></span> | <span data-ttu-id="e672b-110">值</span><span class="sxs-lookup"><span data-stu-id="e672b-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="e672b-111">CN</span><span class="sxs-lookup"><span data-stu-id="e672b-111">CN</span></span>                | <span data-ttu-id="e672b-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="e672b-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="e672b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e672b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e672b-114">profilePath</span><span class="sxs-lookup"><span data-stu-id="e672b-114">profilePath</span></span>                                                              |
| <span data-ttu-id="e672b-115">大小</span><span class="sxs-lookup"><span data-stu-id="e672b-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="e672b-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e672b-116">Update Privilege</span></span>  | <span data-ttu-id="e672b-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="e672b-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="e672b-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e672b-118">Update Frequency</span></span>  | <span data-ttu-id="e672b-119">當使用者的記錄建立時，以及每次需要變更路徑時。</span><span class="sxs-lookup"><span data-stu-id="e672b-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="e672b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e672b-120">Attribute-Id</span></span>      | <span data-ttu-id="e672b-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="e672b-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="e672b-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e672b-122">System-Id-Guid</span></span>    | <span data-ttu-id="e672b-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e672b-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="e672b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="e672b-124">Syntax</span></span>            | [<span data-ttu-id="e672b-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e672b-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="e672b-126">實作</span><span class="sxs-lookup"><span data-stu-id="e672b-126">Implementations</span></span>

-   [<span data-ttu-id="e672b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e672b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e672b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e672b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e672b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e672b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e672b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e672b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e672b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e672b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e672b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e672b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e672b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e672b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="e672b-134">進入</span><span class="sxs-lookup"><span data-stu-id="e672b-134">Entry</span></span> | <span data-ttu-id="e672b-135">值</span><span class="sxs-lookup"><span data-stu-id="e672b-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e672b-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e672b-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e672b-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e672b-138">System-Only</span></span>            | <span data-ttu-id="e672b-139">否</span><span class="sxs-lookup"><span data-stu-id="e672b-139">False</span></span>                             |
| <span data-ttu-id="e672b-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e672b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e672b-141">對</span><span class="sxs-lookup"><span data-stu-id="e672b-141">True</span></span>                              |
| <span data-ttu-id="e672b-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e672b-142">Is Indexed</span></span>             | <span data-ttu-id="e672b-143">否</span><span class="sxs-lookup"><span data-stu-id="e672b-143">False</span></span>                             |
| <span data-ttu-id="e672b-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e672b-144">In Global Catalog</span></span>      | <span data-ttu-id="e672b-145">否</span><span class="sxs-lookup"><span data-stu-id="e672b-145">False</span></span>                             |
| <span data-ttu-id="e672b-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e672b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e672b-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e672b-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e672b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e672b-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e672b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e672b-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e672b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-150">Search-Flags</span></span>           | <span data-ttu-id="e672b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-151">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-152">System-Flags</span></span>           | <span data-ttu-id="e672b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-153">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e672b-154">Classes used in</span></span>        | [<span data-ttu-id="e672b-155">**User**</span><span class="sxs-lookup"><span data-stu-id="e672b-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e672b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e672b-156">Windows Server 2003</span></span>



| <span data-ttu-id="e672b-157">進入</span><span class="sxs-lookup"><span data-stu-id="e672b-157">Entry</span></span> | <span data-ttu-id="e672b-158">值</span><span class="sxs-lookup"><span data-stu-id="e672b-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e672b-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e672b-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e672b-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e672b-161">System-Only</span></span>            | <span data-ttu-id="e672b-162">否</span><span class="sxs-lookup"><span data-stu-id="e672b-162">False</span></span>                             |
| <span data-ttu-id="e672b-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e672b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e672b-164">對</span><span class="sxs-lookup"><span data-stu-id="e672b-164">True</span></span>                              |
| <span data-ttu-id="e672b-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e672b-165">Is Indexed</span></span>             | <span data-ttu-id="e672b-166">否</span><span class="sxs-lookup"><span data-stu-id="e672b-166">False</span></span>                             |
| <span data-ttu-id="e672b-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e672b-167">In Global Catalog</span></span>      | <span data-ttu-id="e672b-168">否</span><span class="sxs-lookup"><span data-stu-id="e672b-168">False</span></span>                             |
| <span data-ttu-id="e672b-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e672b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e672b-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e672b-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e672b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e672b-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e672b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e672b-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e672b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-173">Search-Flags</span></span>           | <span data-ttu-id="e672b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-174">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-175">System-Flags</span></span>           | <span data-ttu-id="e672b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-176">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e672b-177">Classes used in</span></span>        | [<span data-ttu-id="e672b-178">**User**</span><span class="sxs-lookup"><span data-stu-id="e672b-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e672b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e672b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e672b-180">進入</span><span class="sxs-lookup"><span data-stu-id="e672b-180">Entry</span></span> | <span data-ttu-id="e672b-181">值</span><span class="sxs-lookup"><span data-stu-id="e672b-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e672b-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e672b-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e672b-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e672b-184">System-Only</span></span>            | <span data-ttu-id="e672b-185">否</span><span class="sxs-lookup"><span data-stu-id="e672b-185">False</span></span>                             |
| <span data-ttu-id="e672b-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e672b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e672b-187">對</span><span class="sxs-lookup"><span data-stu-id="e672b-187">True</span></span>                              |
| <span data-ttu-id="e672b-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e672b-188">Is Indexed</span></span>             | <span data-ttu-id="e672b-189">否</span><span class="sxs-lookup"><span data-stu-id="e672b-189">False</span></span>                             |
| <span data-ttu-id="e672b-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e672b-190">In Global Catalog</span></span>      | <span data-ttu-id="e672b-191">否</span><span class="sxs-lookup"><span data-stu-id="e672b-191">False</span></span>                             |
| <span data-ttu-id="e672b-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e672b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e672b-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e672b-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e672b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e672b-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e672b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e672b-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e672b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-196">Search-Flags</span></span>           | <span data-ttu-id="e672b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-197">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-198">System-Flags</span></span>           | <span data-ttu-id="e672b-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-199">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e672b-200">Classes used in</span></span>        | [<span data-ttu-id="e672b-201">**User**</span><span class="sxs-lookup"><span data-stu-id="e672b-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e672b-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e672b-202">Windows Server 2008</span></span>



| <span data-ttu-id="e672b-203">進入</span><span class="sxs-lookup"><span data-stu-id="e672b-203">Entry</span></span> | <span data-ttu-id="e672b-204">值</span><span class="sxs-lookup"><span data-stu-id="e672b-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e672b-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e672b-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e672b-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e672b-207">System-Only</span></span>            | <span data-ttu-id="e672b-208">否</span><span class="sxs-lookup"><span data-stu-id="e672b-208">False</span></span>                             |
| <span data-ttu-id="e672b-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e672b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e672b-210">對</span><span class="sxs-lookup"><span data-stu-id="e672b-210">True</span></span>                              |
| <span data-ttu-id="e672b-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e672b-211">Is Indexed</span></span>             | <span data-ttu-id="e672b-212">否</span><span class="sxs-lookup"><span data-stu-id="e672b-212">False</span></span>                             |
| <span data-ttu-id="e672b-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e672b-213">In Global Catalog</span></span>      | <span data-ttu-id="e672b-214">否</span><span class="sxs-lookup"><span data-stu-id="e672b-214">False</span></span>                             |
| <span data-ttu-id="e672b-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e672b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e672b-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e672b-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e672b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e672b-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e672b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e672b-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e672b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-219">Search-Flags</span></span>           | <span data-ttu-id="e672b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-220">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-221">System-Flags</span></span>           | <span data-ttu-id="e672b-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-222">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e672b-223">Classes used in</span></span>        | [<span data-ttu-id="e672b-224">**User**</span><span class="sxs-lookup"><span data-stu-id="e672b-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e672b-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e672b-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e672b-226">進入</span><span class="sxs-lookup"><span data-stu-id="e672b-226">Entry</span></span> | <span data-ttu-id="e672b-227">值</span><span class="sxs-lookup"><span data-stu-id="e672b-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e672b-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e672b-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e672b-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="e672b-230">System-Only</span></span>            | <span data-ttu-id="e672b-231">否</span><span class="sxs-lookup"><span data-stu-id="e672b-231">False</span></span>                             |
| <span data-ttu-id="e672b-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e672b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="e672b-233">對</span><span class="sxs-lookup"><span data-stu-id="e672b-233">True</span></span>                              |
| <span data-ttu-id="e672b-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e672b-234">Is Indexed</span></span>             | <span data-ttu-id="e672b-235">否</span><span class="sxs-lookup"><span data-stu-id="e672b-235">False</span></span>                             |
| <span data-ttu-id="e672b-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e672b-236">In Global Catalog</span></span>      | <span data-ttu-id="e672b-237">否</span><span class="sxs-lookup"><span data-stu-id="e672b-237">False</span></span>                             |
| <span data-ttu-id="e672b-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e672b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="e672b-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e672b-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e672b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e672b-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e672b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e672b-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e672b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-242">Search-Flags</span></span>           | <span data-ttu-id="e672b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-243">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-244">System-Flags</span></span>           | <span data-ttu-id="e672b-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-245">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e672b-246">Classes used in</span></span>        | [<span data-ttu-id="e672b-247">**User**</span><span class="sxs-lookup"><span data-stu-id="e672b-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e672b-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e672b-248">Windows Server 2012</span></span>



| <span data-ttu-id="e672b-249">進入</span><span class="sxs-lookup"><span data-stu-id="e672b-249">Entry</span></span> | <span data-ttu-id="e672b-250">值</span><span class="sxs-lookup"><span data-stu-id="e672b-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e672b-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e672b-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e672b-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e672b-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="e672b-253">System-Only</span></span>            | <span data-ttu-id="e672b-254">否</span><span class="sxs-lookup"><span data-stu-id="e672b-254">False</span></span>                             |
| <span data-ttu-id="e672b-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e672b-255">Is-Single-Valued</span></span>       | <span data-ttu-id="e672b-256">對</span><span class="sxs-lookup"><span data-stu-id="e672b-256">True</span></span>                              |
| <span data-ttu-id="e672b-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e672b-257">Is Indexed</span></span>             | <span data-ttu-id="e672b-258">否</span><span class="sxs-lookup"><span data-stu-id="e672b-258">False</span></span>                             |
| <span data-ttu-id="e672b-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e672b-259">In Global Catalog</span></span>      | <span data-ttu-id="e672b-260">否</span><span class="sxs-lookup"><span data-stu-id="e672b-260">False</span></span>                             |
| <span data-ttu-id="e672b-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e672b-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="e672b-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e672b-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e672b-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e672b-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e672b-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e672b-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e672b-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-265">Search-Flags</span></span>           | <span data-ttu-id="e672b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-266">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e672b-267">System-Flags</span></span>           | <span data-ttu-id="e672b-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e672b-268">0x00000010</span></span>                        |
| <span data-ttu-id="e672b-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e672b-269">Classes used in</span></span>        | [<span data-ttu-id="e672b-270">**User**</span><span class="sxs-lookup"><span data-stu-id="e672b-270">**User**</span></span>](c-user.md)<br/> |



 

 





