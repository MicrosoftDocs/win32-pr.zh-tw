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
# <a name="profile-path-attribute"></a><span data-ttu-id="51273-106">Profile-Path 屬性</span><span class="sxs-lookup"><span data-stu-id="51273-106">Profile-Path attribute</span></span>

<span data-ttu-id="51273-107">指定使用者設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="51273-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="51273-108">這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="51273-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="51273-109">進入</span><span class="sxs-lookup"><span data-stu-id="51273-109">Entry</span></span> | <span data-ttu-id="51273-110">值</span><span class="sxs-lookup"><span data-stu-id="51273-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="51273-111">CN</span><span class="sxs-lookup"><span data-stu-id="51273-111">CN</span></span>                | <span data-ttu-id="51273-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="51273-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="51273-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="51273-113">Ldap-Display-Name</span></span> | <span data-ttu-id="51273-114">profilePath</span><span class="sxs-lookup"><span data-stu-id="51273-114">profilePath</span></span>                                                              |
| <span data-ttu-id="51273-115">大小</span><span class="sxs-lookup"><span data-stu-id="51273-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="51273-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="51273-116">Update Privilege</span></span>  | <span data-ttu-id="51273-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="51273-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="51273-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="51273-118">Update Frequency</span></span>  | <span data-ttu-id="51273-119">當使用者的記錄建立時，以及每次需要變更路徑時。</span><span class="sxs-lookup"><span data-stu-id="51273-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="51273-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51273-120">Attribute-Id</span></span>      | <span data-ttu-id="51273-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="51273-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="51273-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="51273-122">System-Id-Guid</span></span>    | <span data-ttu-id="51273-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="51273-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="51273-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="51273-124">Syntax</span></span>            | [<span data-ttu-id="51273-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="51273-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="51273-126">實作</span><span class="sxs-lookup"><span data-stu-id="51273-126">Implementations</span></span>

-   [<span data-ttu-id="51273-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="51273-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="51273-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51273-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51273-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51273-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51273-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51273-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51273-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51273-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51273-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51273-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="51273-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51273-133">Windows 2000 Server</span></span>



| <span data-ttu-id="51273-134">進入</span><span class="sxs-lookup"><span data-stu-id="51273-134">Entry</span></span> | <span data-ttu-id="51273-135">值</span><span class="sxs-lookup"><span data-stu-id="51273-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51273-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51273-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51273-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="51273-138">System-Only</span></span>            | <span data-ttu-id="51273-139">否</span><span class="sxs-lookup"><span data-stu-id="51273-139">False</span></span>                             |
| <span data-ttu-id="51273-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51273-140">Is-Single-Valued</span></span>       | <span data-ttu-id="51273-141">對</span><span class="sxs-lookup"><span data-stu-id="51273-141">True</span></span>                              |
| <span data-ttu-id="51273-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51273-142">Is Indexed</span></span>             | <span data-ttu-id="51273-143">否</span><span class="sxs-lookup"><span data-stu-id="51273-143">False</span></span>                             |
| <span data-ttu-id="51273-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51273-144">In Global Catalog</span></span>      | <span data-ttu-id="51273-145">否</span><span class="sxs-lookup"><span data-stu-id="51273-145">False</span></span>                             |
| <span data-ttu-id="51273-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51273-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="51273-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51273-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51273-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51273-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51273-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51273-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51273-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-150">Search-Flags</span></span>           | <span data-ttu-id="51273-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-151">0x00000010</span></span>                        |
| <span data-ttu-id="51273-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-152">System-Flags</span></span>           | <span data-ttu-id="51273-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-153">0x00000010</span></span>                        |
| <span data-ttu-id="51273-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51273-154">Classes used in</span></span>        | [<span data-ttu-id="51273-155">**User**</span><span class="sxs-lookup"><span data-stu-id="51273-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="51273-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51273-156">Windows Server 2003</span></span>



| <span data-ttu-id="51273-157">進入</span><span class="sxs-lookup"><span data-stu-id="51273-157">Entry</span></span> | <span data-ttu-id="51273-158">值</span><span class="sxs-lookup"><span data-stu-id="51273-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51273-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51273-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51273-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="51273-161">System-Only</span></span>            | <span data-ttu-id="51273-162">否</span><span class="sxs-lookup"><span data-stu-id="51273-162">False</span></span>                             |
| <span data-ttu-id="51273-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51273-163">Is-Single-Valued</span></span>       | <span data-ttu-id="51273-164">對</span><span class="sxs-lookup"><span data-stu-id="51273-164">True</span></span>                              |
| <span data-ttu-id="51273-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51273-165">Is Indexed</span></span>             | <span data-ttu-id="51273-166">否</span><span class="sxs-lookup"><span data-stu-id="51273-166">False</span></span>                             |
| <span data-ttu-id="51273-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51273-167">In Global Catalog</span></span>      | <span data-ttu-id="51273-168">否</span><span class="sxs-lookup"><span data-stu-id="51273-168">False</span></span>                             |
| <span data-ttu-id="51273-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51273-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="51273-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51273-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51273-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51273-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51273-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51273-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51273-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-173">Search-Flags</span></span>           | <span data-ttu-id="51273-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-174">0x00000010</span></span>                        |
| <span data-ttu-id="51273-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-175">System-Flags</span></span>           | <span data-ttu-id="51273-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-176">0x00000010</span></span>                        |
| <span data-ttu-id="51273-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51273-177">Classes used in</span></span>        | [<span data-ttu-id="51273-178">**User**</span><span class="sxs-lookup"><span data-stu-id="51273-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51273-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51273-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51273-180">進入</span><span class="sxs-lookup"><span data-stu-id="51273-180">Entry</span></span> | <span data-ttu-id="51273-181">值</span><span class="sxs-lookup"><span data-stu-id="51273-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51273-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51273-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51273-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="51273-184">System-Only</span></span>            | <span data-ttu-id="51273-185">否</span><span class="sxs-lookup"><span data-stu-id="51273-185">False</span></span>                             |
| <span data-ttu-id="51273-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51273-186">Is-Single-Valued</span></span>       | <span data-ttu-id="51273-187">對</span><span class="sxs-lookup"><span data-stu-id="51273-187">True</span></span>                              |
| <span data-ttu-id="51273-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51273-188">Is Indexed</span></span>             | <span data-ttu-id="51273-189">否</span><span class="sxs-lookup"><span data-stu-id="51273-189">False</span></span>                             |
| <span data-ttu-id="51273-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51273-190">In Global Catalog</span></span>      | <span data-ttu-id="51273-191">否</span><span class="sxs-lookup"><span data-stu-id="51273-191">False</span></span>                             |
| <span data-ttu-id="51273-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51273-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="51273-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51273-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51273-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51273-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51273-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51273-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51273-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-196">Search-Flags</span></span>           | <span data-ttu-id="51273-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-197">0x00000010</span></span>                        |
| <span data-ttu-id="51273-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-198">System-Flags</span></span>           | <span data-ttu-id="51273-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-199">0x00000010</span></span>                        |
| <span data-ttu-id="51273-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51273-200">Classes used in</span></span>        | [<span data-ttu-id="51273-201">**User**</span><span class="sxs-lookup"><span data-stu-id="51273-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="51273-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51273-202">Windows Server 2008</span></span>



| <span data-ttu-id="51273-203">進入</span><span class="sxs-lookup"><span data-stu-id="51273-203">Entry</span></span> | <span data-ttu-id="51273-204">值</span><span class="sxs-lookup"><span data-stu-id="51273-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51273-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51273-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51273-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="51273-207">System-Only</span></span>            | <span data-ttu-id="51273-208">否</span><span class="sxs-lookup"><span data-stu-id="51273-208">False</span></span>                             |
| <span data-ttu-id="51273-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51273-209">Is-Single-Valued</span></span>       | <span data-ttu-id="51273-210">對</span><span class="sxs-lookup"><span data-stu-id="51273-210">True</span></span>                              |
| <span data-ttu-id="51273-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51273-211">Is Indexed</span></span>             | <span data-ttu-id="51273-212">否</span><span class="sxs-lookup"><span data-stu-id="51273-212">False</span></span>                             |
| <span data-ttu-id="51273-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51273-213">In Global Catalog</span></span>      | <span data-ttu-id="51273-214">否</span><span class="sxs-lookup"><span data-stu-id="51273-214">False</span></span>                             |
| <span data-ttu-id="51273-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51273-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="51273-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51273-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51273-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51273-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51273-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51273-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51273-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-219">Search-Flags</span></span>           | <span data-ttu-id="51273-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-220">0x00000010</span></span>                        |
| <span data-ttu-id="51273-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-221">System-Flags</span></span>           | <span data-ttu-id="51273-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-222">0x00000010</span></span>                        |
| <span data-ttu-id="51273-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51273-223">Classes used in</span></span>        | [<span data-ttu-id="51273-224">**User**</span><span class="sxs-lookup"><span data-stu-id="51273-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51273-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51273-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51273-226">進入</span><span class="sxs-lookup"><span data-stu-id="51273-226">Entry</span></span> | <span data-ttu-id="51273-227">值</span><span class="sxs-lookup"><span data-stu-id="51273-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51273-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51273-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51273-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="51273-230">System-Only</span></span>            | <span data-ttu-id="51273-231">否</span><span class="sxs-lookup"><span data-stu-id="51273-231">False</span></span>                             |
| <span data-ttu-id="51273-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51273-232">Is-Single-Valued</span></span>       | <span data-ttu-id="51273-233">對</span><span class="sxs-lookup"><span data-stu-id="51273-233">True</span></span>                              |
| <span data-ttu-id="51273-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51273-234">Is Indexed</span></span>             | <span data-ttu-id="51273-235">否</span><span class="sxs-lookup"><span data-stu-id="51273-235">False</span></span>                             |
| <span data-ttu-id="51273-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51273-236">In Global Catalog</span></span>      | <span data-ttu-id="51273-237">否</span><span class="sxs-lookup"><span data-stu-id="51273-237">False</span></span>                             |
| <span data-ttu-id="51273-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51273-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="51273-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51273-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51273-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51273-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51273-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51273-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51273-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-242">Search-Flags</span></span>           | <span data-ttu-id="51273-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-243">0x00000010</span></span>                        |
| <span data-ttu-id="51273-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-244">System-Flags</span></span>           | <span data-ttu-id="51273-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-245">0x00000010</span></span>                        |
| <span data-ttu-id="51273-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51273-246">Classes used in</span></span>        | [<span data-ttu-id="51273-247">**User**</span><span class="sxs-lookup"><span data-stu-id="51273-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="51273-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51273-248">Windows Server 2012</span></span>



| <span data-ttu-id="51273-249">進入</span><span class="sxs-lookup"><span data-stu-id="51273-249">Entry</span></span> | <span data-ttu-id="51273-250">值</span><span class="sxs-lookup"><span data-stu-id="51273-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51273-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="51273-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51273-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51273-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="51273-253">System-Only</span></span>            | <span data-ttu-id="51273-254">否</span><span class="sxs-lookup"><span data-stu-id="51273-254">False</span></span>                             |
| <span data-ttu-id="51273-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="51273-255">Is-Single-Valued</span></span>       | <span data-ttu-id="51273-256">對</span><span class="sxs-lookup"><span data-stu-id="51273-256">True</span></span>                              |
| <span data-ttu-id="51273-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="51273-257">Is Indexed</span></span>             | <span data-ttu-id="51273-258">否</span><span class="sxs-lookup"><span data-stu-id="51273-258">False</span></span>                             |
| <span data-ttu-id="51273-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="51273-259">In Global Catalog</span></span>      | <span data-ttu-id="51273-260">否</span><span class="sxs-lookup"><span data-stu-id="51273-260">False</span></span>                             |
| <span data-ttu-id="51273-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="51273-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="51273-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="51273-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51273-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51273-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51273-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51273-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51273-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-265">Search-Flags</span></span>           | <span data-ttu-id="51273-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-266">0x00000010</span></span>                        |
| <span data-ttu-id="51273-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51273-267">System-Flags</span></span>           | <span data-ttu-id="51273-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51273-268">0x00000010</span></span>                        |
| <span data-ttu-id="51273-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="51273-269">Classes used in</span></span>        | [<span data-ttu-id="51273-270">**User**</span><span class="sxs-lookup"><span data-stu-id="51273-270">**User**</span></span>](c-user.md)<br/> |



 

 





