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
# <a name="profile-path-attribute"></a><span data-ttu-id="28c34-106">Profile-Path 屬性</span><span class="sxs-lookup"><span data-stu-id="28c34-106">Profile-Path attribute</span></span>

<span data-ttu-id="28c34-107">指定使用者設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="28c34-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="28c34-108">這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="28c34-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="28c34-109">進入</span><span class="sxs-lookup"><span data-stu-id="28c34-109">Entry</span></span> | <span data-ttu-id="28c34-110">值</span><span class="sxs-lookup"><span data-stu-id="28c34-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="28c34-111">CN</span><span class="sxs-lookup"><span data-stu-id="28c34-111">CN</span></span>                | <span data-ttu-id="28c34-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="28c34-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="28c34-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="28c34-113">Ldap-Display-Name</span></span> | <span data-ttu-id="28c34-114">profilePath</span><span class="sxs-lookup"><span data-stu-id="28c34-114">profilePath</span></span>                                                              |
| <span data-ttu-id="28c34-115">大小</span><span class="sxs-lookup"><span data-stu-id="28c34-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="28c34-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="28c34-116">Update Privilege</span></span>  | <span data-ttu-id="28c34-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="28c34-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="28c34-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="28c34-118">Update Frequency</span></span>  | <span data-ttu-id="28c34-119">當使用者的記錄建立時，以及每次需要變更路徑時。</span><span class="sxs-lookup"><span data-stu-id="28c34-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="28c34-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28c34-120">Attribute-Id</span></span>      | <span data-ttu-id="28c34-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="28c34-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="28c34-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="28c34-122">System-Id-Guid</span></span>    | <span data-ttu-id="28c34-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="28c34-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="28c34-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="28c34-124">Syntax</span></span>            | [<span data-ttu-id="28c34-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="28c34-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="28c34-126">實作</span><span class="sxs-lookup"><span data-stu-id="28c34-126">Implementations</span></span>

-   [<span data-ttu-id="28c34-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28c34-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28c34-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28c34-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28c34-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28c34-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28c34-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28c34-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28c34-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28c34-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28c34-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28c34-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28c34-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28c34-133">Windows 2000 Server</span></span>



| <span data-ttu-id="28c34-134">進入</span><span class="sxs-lookup"><span data-stu-id="28c34-134">Entry</span></span> | <span data-ttu-id="28c34-135">值</span><span class="sxs-lookup"><span data-stu-id="28c34-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28c34-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28c34-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c34-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c34-138">System-Only</span></span>            | <span data-ttu-id="28c34-139">否</span><span class="sxs-lookup"><span data-stu-id="28c34-139">False</span></span>                             |
| <span data-ttu-id="28c34-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28c34-140">Is-Single-Valued</span></span>       | <span data-ttu-id="28c34-141">對</span><span class="sxs-lookup"><span data-stu-id="28c34-141">True</span></span>                              |
| <span data-ttu-id="28c34-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28c34-142">Is Indexed</span></span>             | <span data-ttu-id="28c34-143">否</span><span class="sxs-lookup"><span data-stu-id="28c34-143">False</span></span>                             |
| <span data-ttu-id="28c34-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28c34-144">In Global Catalog</span></span>      | <span data-ttu-id="28c34-145">否</span><span class="sxs-lookup"><span data-stu-id="28c34-145">False</span></span>                             |
| <span data-ttu-id="28c34-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28c34-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c34-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28c34-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28c34-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c34-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28c34-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c34-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28c34-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-150">Search-Flags</span></span>           | <span data-ttu-id="28c34-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-151">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-152">System-Flags</span></span>           | <span data-ttu-id="28c34-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-153">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28c34-154">Classes used in</span></span>        | [<span data-ttu-id="28c34-155">**User**</span><span class="sxs-lookup"><span data-stu-id="28c34-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="28c34-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28c34-156">Windows Server 2003</span></span>



| <span data-ttu-id="28c34-157">進入</span><span class="sxs-lookup"><span data-stu-id="28c34-157">Entry</span></span> | <span data-ttu-id="28c34-158">值</span><span class="sxs-lookup"><span data-stu-id="28c34-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28c34-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28c34-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c34-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c34-161">System-Only</span></span>            | <span data-ttu-id="28c34-162">否</span><span class="sxs-lookup"><span data-stu-id="28c34-162">False</span></span>                             |
| <span data-ttu-id="28c34-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28c34-163">Is-Single-Valued</span></span>       | <span data-ttu-id="28c34-164">對</span><span class="sxs-lookup"><span data-stu-id="28c34-164">True</span></span>                              |
| <span data-ttu-id="28c34-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28c34-165">Is Indexed</span></span>             | <span data-ttu-id="28c34-166">否</span><span class="sxs-lookup"><span data-stu-id="28c34-166">False</span></span>                             |
| <span data-ttu-id="28c34-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28c34-167">In Global Catalog</span></span>      | <span data-ttu-id="28c34-168">否</span><span class="sxs-lookup"><span data-stu-id="28c34-168">False</span></span>                             |
| <span data-ttu-id="28c34-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28c34-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c34-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28c34-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28c34-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c34-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28c34-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c34-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28c34-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-173">Search-Flags</span></span>           | <span data-ttu-id="28c34-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-174">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-175">System-Flags</span></span>           | <span data-ttu-id="28c34-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-176">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28c34-177">Classes used in</span></span>        | [<span data-ttu-id="28c34-178">**User**</span><span class="sxs-lookup"><span data-stu-id="28c34-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28c34-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28c34-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28c34-180">進入</span><span class="sxs-lookup"><span data-stu-id="28c34-180">Entry</span></span> | <span data-ttu-id="28c34-181">值</span><span class="sxs-lookup"><span data-stu-id="28c34-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28c34-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28c34-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c34-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c34-184">System-Only</span></span>            | <span data-ttu-id="28c34-185">否</span><span class="sxs-lookup"><span data-stu-id="28c34-185">False</span></span>                             |
| <span data-ttu-id="28c34-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28c34-186">Is-Single-Valued</span></span>       | <span data-ttu-id="28c34-187">對</span><span class="sxs-lookup"><span data-stu-id="28c34-187">True</span></span>                              |
| <span data-ttu-id="28c34-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28c34-188">Is Indexed</span></span>             | <span data-ttu-id="28c34-189">否</span><span class="sxs-lookup"><span data-stu-id="28c34-189">False</span></span>                             |
| <span data-ttu-id="28c34-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28c34-190">In Global Catalog</span></span>      | <span data-ttu-id="28c34-191">否</span><span class="sxs-lookup"><span data-stu-id="28c34-191">False</span></span>                             |
| <span data-ttu-id="28c34-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28c34-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c34-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28c34-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28c34-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c34-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28c34-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c34-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28c34-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-196">Search-Flags</span></span>           | <span data-ttu-id="28c34-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-197">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-198">System-Flags</span></span>           | <span data-ttu-id="28c34-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-199">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28c34-200">Classes used in</span></span>        | [<span data-ttu-id="28c34-201">**User**</span><span class="sxs-lookup"><span data-stu-id="28c34-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28c34-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28c34-202">Windows Server 2008</span></span>



| <span data-ttu-id="28c34-203">進入</span><span class="sxs-lookup"><span data-stu-id="28c34-203">Entry</span></span> | <span data-ttu-id="28c34-204">值</span><span class="sxs-lookup"><span data-stu-id="28c34-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28c34-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28c34-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c34-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c34-207">System-Only</span></span>            | <span data-ttu-id="28c34-208">否</span><span class="sxs-lookup"><span data-stu-id="28c34-208">False</span></span>                             |
| <span data-ttu-id="28c34-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28c34-209">Is-Single-Valued</span></span>       | <span data-ttu-id="28c34-210">對</span><span class="sxs-lookup"><span data-stu-id="28c34-210">True</span></span>                              |
| <span data-ttu-id="28c34-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28c34-211">Is Indexed</span></span>             | <span data-ttu-id="28c34-212">否</span><span class="sxs-lookup"><span data-stu-id="28c34-212">False</span></span>                             |
| <span data-ttu-id="28c34-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28c34-213">In Global Catalog</span></span>      | <span data-ttu-id="28c34-214">否</span><span class="sxs-lookup"><span data-stu-id="28c34-214">False</span></span>                             |
| <span data-ttu-id="28c34-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28c34-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c34-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28c34-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28c34-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c34-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28c34-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c34-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28c34-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-219">Search-Flags</span></span>           | <span data-ttu-id="28c34-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-220">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-221">System-Flags</span></span>           | <span data-ttu-id="28c34-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-222">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28c34-223">Classes used in</span></span>        | [<span data-ttu-id="28c34-224">**User**</span><span class="sxs-lookup"><span data-stu-id="28c34-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28c34-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28c34-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28c34-226">進入</span><span class="sxs-lookup"><span data-stu-id="28c34-226">Entry</span></span> | <span data-ttu-id="28c34-227">值</span><span class="sxs-lookup"><span data-stu-id="28c34-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28c34-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28c34-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c34-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c34-230">System-Only</span></span>            | <span data-ttu-id="28c34-231">否</span><span class="sxs-lookup"><span data-stu-id="28c34-231">False</span></span>                             |
| <span data-ttu-id="28c34-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28c34-232">Is-Single-Valued</span></span>       | <span data-ttu-id="28c34-233">對</span><span class="sxs-lookup"><span data-stu-id="28c34-233">True</span></span>                              |
| <span data-ttu-id="28c34-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28c34-234">Is Indexed</span></span>             | <span data-ttu-id="28c34-235">否</span><span class="sxs-lookup"><span data-stu-id="28c34-235">False</span></span>                             |
| <span data-ttu-id="28c34-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28c34-236">In Global Catalog</span></span>      | <span data-ttu-id="28c34-237">否</span><span class="sxs-lookup"><span data-stu-id="28c34-237">False</span></span>                             |
| <span data-ttu-id="28c34-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28c34-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c34-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28c34-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28c34-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c34-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28c34-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c34-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28c34-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-242">Search-Flags</span></span>           | <span data-ttu-id="28c34-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-243">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-244">System-Flags</span></span>           | <span data-ttu-id="28c34-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-245">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28c34-246">Classes used in</span></span>        | [<span data-ttu-id="28c34-247">**User**</span><span class="sxs-lookup"><span data-stu-id="28c34-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28c34-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28c34-248">Windows Server 2012</span></span>



| <span data-ttu-id="28c34-249">進入</span><span class="sxs-lookup"><span data-stu-id="28c34-249">Entry</span></span> | <span data-ttu-id="28c34-250">值</span><span class="sxs-lookup"><span data-stu-id="28c34-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="28c34-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="28c34-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c34-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="28c34-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c34-253">System-Only</span></span>            | <span data-ttu-id="28c34-254">否</span><span class="sxs-lookup"><span data-stu-id="28c34-254">False</span></span>                             |
| <span data-ttu-id="28c34-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="28c34-255">Is-Single-Valued</span></span>       | <span data-ttu-id="28c34-256">對</span><span class="sxs-lookup"><span data-stu-id="28c34-256">True</span></span>                              |
| <span data-ttu-id="28c34-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="28c34-257">Is Indexed</span></span>             | <span data-ttu-id="28c34-258">否</span><span class="sxs-lookup"><span data-stu-id="28c34-258">False</span></span>                             |
| <span data-ttu-id="28c34-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="28c34-259">In Global Catalog</span></span>      | <span data-ttu-id="28c34-260">否</span><span class="sxs-lookup"><span data-stu-id="28c34-260">False</span></span>                             |
| <span data-ttu-id="28c34-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="28c34-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c34-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="28c34-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="28c34-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c34-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="28c34-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c34-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="28c34-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-265">Search-Flags</span></span>           | <span data-ttu-id="28c34-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-266">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c34-267">System-Flags</span></span>           | <span data-ttu-id="28c34-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c34-268">0x00000010</span></span>                        |
| <span data-ttu-id="28c34-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="28c34-269">Classes used in</span></span>        | [<span data-ttu-id="28c34-270">**User**</span><span class="sxs-lookup"><span data-stu-id="28c34-270">**User**</span></span>](c-user.md)<br/> |



 

 





