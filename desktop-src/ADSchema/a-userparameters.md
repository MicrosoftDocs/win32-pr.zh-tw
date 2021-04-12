---
title: User-Parameters 屬性
description: 使用者的參數。
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- User-Parameters 屬性 AD 架構
- userParameters 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c1d593f0a655dea4fa3ddb25753de712ab83cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509652"
---
# <a name="user-parameters-attribute"></a><span data-ttu-id="ec4f2-105">User-Parameters 屬性</span><span class="sxs-lookup"><span data-stu-id="ec4f2-105">User-Parameters attribute</span></span>

<span data-ttu-id="ec4f2-106">使用者的參數。</span><span class="sxs-lookup"><span data-stu-id="ec4f2-106">Parameters of the user.</span></span> <span data-ttu-id="ec4f2-107">指向保留給應用程式使用的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="ec4f2-107">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="ec4f2-108">這個字串可以是 null 字串，也可以在終止的 null 字元之前有任意數目的字元。</span><span class="sxs-lookup"><span data-stu-id="ec4f2-108">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="ec4f2-109">Microsoft 產品會使用這個成員來儲存個別程式專用的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="ec4f2-109">Microsoft products use this member to store user data specific to the individual program.</span></span>



| <span data-ttu-id="ec4f2-110">進入</span><span class="sxs-lookup"><span data-stu-id="ec4f2-110">Entry</span></span> | <span data-ttu-id="ec4f2-111">值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ec4f2-112">CN</span><span class="sxs-lookup"><span data-stu-id="ec4f2-112">CN</span></span>                | <span data-ttu-id="ec4f2-113">User-Parameters</span><span class="sxs-lookup"><span data-stu-id="ec4f2-113">User-Parameters</span></span>                             |
| <span data-ttu-id="ec4f2-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ec4f2-114">Ldap-Display-Name</span></span> | <span data-ttu-id="ec4f2-115">userParameters</span><span class="sxs-lookup"><span data-stu-id="ec4f2-115">userParameters</span></span>                              |
| <span data-ttu-id="ec4f2-116">大小</span><span class="sxs-lookup"><span data-stu-id="ec4f2-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="ec4f2-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ec4f2-117">Update Privilege</span></span>  | <span data-ttu-id="ec4f2-118">由應用程式修改。</span><span class="sxs-lookup"><span data-stu-id="ec4f2-118">Modified by applications.</span></span>                   |
| <span data-ttu-id="ec4f2-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ec4f2-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ec4f2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec4f2-120">Attribute-Id</span></span>      | <span data-ttu-id="ec4f2-121">1.2.840.113556.1.4.138</span><span class="sxs-lookup"><span data-stu-id="ec4f2-121">1.2.840.113556.1.4.138</span></span>                      |
| <span data-ttu-id="ec4f2-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ec4f2-122">System-Id-Guid</span></span>    | <span data-ttu-id="ec4f2-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ec4f2-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="ec4f2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec4f2-124">Syntax</span></span>            | [<span data-ttu-id="ec4f2-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ec4f2-126">實作</span><span class="sxs-lookup"><span data-stu-id="ec4f2-126">Implementations</span></span>

-   [<span data-ttu-id="ec4f2-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec4f2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec4f2-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec4f2-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec4f2-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec4f2-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec4f2-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec4f2-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ec4f2-134">進入</span><span class="sxs-lookup"><span data-stu-id="ec4f2-134">Entry</span></span> | <span data-ttu-id="ec4f2-135">值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec4f2-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec4f2-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4f2-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4f2-138">System-Only</span></span>            | <span data-ttu-id="ec4f2-139">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-139">False</span></span>                             |
| <span data-ttu-id="ec4f2-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4f2-141">對</span><span class="sxs-lookup"><span data-stu-id="ec4f2-141">True</span></span>                              |
| <span data-ttu-id="ec4f2-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec4f2-142">Is Indexed</span></span>             | <span data-ttu-id="ec4f2-143">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-143">False</span></span>                             |
| <span data-ttu-id="ec4f2-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec4f2-144">In Global Catalog</span></span>      | <span data-ttu-id="ec4f2-145">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-145">False</span></span>                             |
| <span data-ttu-id="ec4f2-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec4f2-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4f2-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec4f2-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec4f2-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4f2-148">Range-Lower</span></span>            | <span data-ttu-id="ec4f2-149">0</span><span class="sxs-lookup"><span data-stu-id="ec4f2-149">0</span></span>                                 |
| <span data-ttu-id="ec4f2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4f2-150">Range-Upper</span></span>            | <span data-ttu-id="ec4f2-151">32767</span><span class="sxs-lookup"><span data-stu-id="ec4f2-151">32767</span></span>                             |
| <span data-ttu-id="ec4f2-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-152">Search-Flags</span></span>           | <span data-ttu-id="ec4f2-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4f2-153">0x00000000</span></span>                        |
| <span data-ttu-id="ec4f2-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-154">System-Flags</span></span>           | <span data-ttu-id="ec4f2-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4f2-155">0x00000010</span></span>                        |
| <span data-ttu-id="ec4f2-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec4f2-156">Classes used in</span></span>        | [<span data-ttu-id="ec4f2-157">**User**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec4f2-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec4f2-158">Windows Server 2003</span></span>



| <span data-ttu-id="ec4f2-159">進入</span><span class="sxs-lookup"><span data-stu-id="ec4f2-159">Entry</span></span> | <span data-ttu-id="ec4f2-160">值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec4f2-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec4f2-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4f2-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4f2-163">System-Only</span></span>            | <span data-ttu-id="ec4f2-164">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-164">False</span></span>                             |
| <span data-ttu-id="ec4f2-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4f2-166">對</span><span class="sxs-lookup"><span data-stu-id="ec4f2-166">True</span></span>                              |
| <span data-ttu-id="ec4f2-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec4f2-167">Is Indexed</span></span>             | <span data-ttu-id="ec4f2-168">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-168">False</span></span>                             |
| <span data-ttu-id="ec4f2-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec4f2-169">In Global Catalog</span></span>      | <span data-ttu-id="ec4f2-170">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-170">False</span></span>                             |
| <span data-ttu-id="ec4f2-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec4f2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4f2-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec4f2-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec4f2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4f2-173">Range-Lower</span></span>            | <span data-ttu-id="ec4f2-174">0</span><span class="sxs-lookup"><span data-stu-id="ec4f2-174">0</span></span>                                 |
| <span data-ttu-id="ec4f2-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4f2-175">Range-Upper</span></span>            | <span data-ttu-id="ec4f2-176">32767</span><span class="sxs-lookup"><span data-stu-id="ec4f2-176">32767</span></span>                             |
| <span data-ttu-id="ec4f2-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-177">Search-Flags</span></span>           | <span data-ttu-id="ec4f2-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4f2-178">0x00000000</span></span>                        |
| <span data-ttu-id="ec4f2-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-179">System-Flags</span></span>           | <span data-ttu-id="ec4f2-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4f2-180">0x00000010</span></span>                        |
| <span data-ttu-id="ec4f2-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec4f2-181">Classes used in</span></span>        | [<span data-ttu-id="ec4f2-182">**User**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec4f2-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec4f2-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec4f2-184">進入</span><span class="sxs-lookup"><span data-stu-id="ec4f2-184">Entry</span></span> | <span data-ttu-id="ec4f2-185">值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-185">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec4f2-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec4f2-186">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4f2-187">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4f2-188">System-Only</span></span>            | <span data-ttu-id="ec4f2-189">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-189">False</span></span>                             |
| <span data-ttu-id="ec4f2-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-190">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4f2-191">對</span><span class="sxs-lookup"><span data-stu-id="ec4f2-191">True</span></span>                              |
| <span data-ttu-id="ec4f2-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec4f2-192">Is Indexed</span></span>             | <span data-ttu-id="ec4f2-193">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-193">False</span></span>                             |
| <span data-ttu-id="ec4f2-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec4f2-194">In Global Catalog</span></span>      | <span data-ttu-id="ec4f2-195">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-195">False</span></span>                             |
| <span data-ttu-id="ec4f2-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec4f2-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4f2-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec4f2-197">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec4f2-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4f2-198">Range-Lower</span></span>            | <span data-ttu-id="ec4f2-199">0</span><span class="sxs-lookup"><span data-stu-id="ec4f2-199">0</span></span>                                 |
| <span data-ttu-id="ec4f2-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4f2-200">Range-Upper</span></span>            | <span data-ttu-id="ec4f2-201">32767</span><span class="sxs-lookup"><span data-stu-id="ec4f2-201">32767</span></span>                             |
| <span data-ttu-id="ec4f2-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-202">Search-Flags</span></span>           | <span data-ttu-id="ec4f2-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4f2-203">0x00000000</span></span>                        |
| <span data-ttu-id="ec4f2-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-204">System-Flags</span></span>           | <span data-ttu-id="ec4f2-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4f2-205">0x00000010</span></span>                        |
| <span data-ttu-id="ec4f2-206">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec4f2-206">Classes used in</span></span>        | [<span data-ttu-id="ec4f2-207">**User**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-207">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec4f2-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec4f2-208">Windows Server 2008</span></span>



| <span data-ttu-id="ec4f2-209">進入</span><span class="sxs-lookup"><span data-stu-id="ec4f2-209">Entry</span></span> | <span data-ttu-id="ec4f2-210">值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-210">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec4f2-211">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec4f2-211">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4f2-212">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4f2-213">System-Only</span></span>            | <span data-ttu-id="ec4f2-214">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-214">False</span></span>                             |
| <span data-ttu-id="ec4f2-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-215">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4f2-216">對</span><span class="sxs-lookup"><span data-stu-id="ec4f2-216">True</span></span>                              |
| <span data-ttu-id="ec4f2-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec4f2-217">Is Indexed</span></span>             | <span data-ttu-id="ec4f2-218">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-218">False</span></span>                             |
| <span data-ttu-id="ec4f2-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec4f2-219">In Global Catalog</span></span>      | <span data-ttu-id="ec4f2-220">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-220">False</span></span>                             |
| <span data-ttu-id="ec4f2-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec4f2-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4f2-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec4f2-222">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec4f2-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4f2-223">Range-Lower</span></span>            | <span data-ttu-id="ec4f2-224">0</span><span class="sxs-lookup"><span data-stu-id="ec4f2-224">0</span></span>                                 |
| <span data-ttu-id="ec4f2-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4f2-225">Range-Upper</span></span>            | <span data-ttu-id="ec4f2-226">32767</span><span class="sxs-lookup"><span data-stu-id="ec4f2-226">32767</span></span>                             |
| <span data-ttu-id="ec4f2-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-227">Search-Flags</span></span>           | <span data-ttu-id="ec4f2-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4f2-228">0x00000000</span></span>                        |
| <span data-ttu-id="ec4f2-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-229">System-Flags</span></span>           | <span data-ttu-id="ec4f2-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4f2-230">0x00000010</span></span>                        |
| <span data-ttu-id="ec4f2-231">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec4f2-231">Classes used in</span></span>        | [<span data-ttu-id="ec4f2-232">**User**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec4f2-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec4f2-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec4f2-234">進入</span><span class="sxs-lookup"><span data-stu-id="ec4f2-234">Entry</span></span> | <span data-ttu-id="ec4f2-235">值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec4f2-236">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec4f2-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4f2-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4f2-238">System-Only</span></span>            | <span data-ttu-id="ec4f2-239">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-239">False</span></span>                             |
| <span data-ttu-id="ec4f2-240">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-240">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4f2-241">對</span><span class="sxs-lookup"><span data-stu-id="ec4f2-241">True</span></span>                              |
| <span data-ttu-id="ec4f2-242">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec4f2-242">Is Indexed</span></span>             | <span data-ttu-id="ec4f2-243">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-243">False</span></span>                             |
| <span data-ttu-id="ec4f2-244">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec4f2-244">In Global Catalog</span></span>      | <span data-ttu-id="ec4f2-245">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-245">False</span></span>                             |
| <span data-ttu-id="ec4f2-246">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec4f2-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4f2-247">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec4f2-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec4f2-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4f2-248">Range-Lower</span></span>            | <span data-ttu-id="ec4f2-249">0</span><span class="sxs-lookup"><span data-stu-id="ec4f2-249">0</span></span>                                 |
| <span data-ttu-id="ec4f2-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4f2-250">Range-Upper</span></span>            | <span data-ttu-id="ec4f2-251">32767</span><span class="sxs-lookup"><span data-stu-id="ec4f2-251">32767</span></span>                             |
| <span data-ttu-id="ec4f2-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-252">Search-Flags</span></span>           | <span data-ttu-id="ec4f2-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4f2-253">0x00000000</span></span>                        |
| <span data-ttu-id="ec4f2-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-254">System-Flags</span></span>           | <span data-ttu-id="ec4f2-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4f2-255">0x00000010</span></span>                        |
| <span data-ttu-id="ec4f2-256">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec4f2-256">Classes used in</span></span>        | [<span data-ttu-id="ec4f2-257">**User**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-257">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec4f2-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec4f2-258">Windows Server 2012</span></span>



| <span data-ttu-id="ec4f2-259">進入</span><span class="sxs-lookup"><span data-stu-id="ec4f2-259">Entry</span></span> | <span data-ttu-id="ec4f2-260">值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-260">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ec4f2-261">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec4f2-261">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec4f2-262">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ec4f2-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec4f2-263">System-Only</span></span>            | <span data-ttu-id="ec4f2-264">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-264">False</span></span>                             |
| <span data-ttu-id="ec4f2-265">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec4f2-265">Is-Single-Valued</span></span>       | <span data-ttu-id="ec4f2-266">對</span><span class="sxs-lookup"><span data-stu-id="ec4f2-266">True</span></span>                              |
| <span data-ttu-id="ec4f2-267">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec4f2-267">Is Indexed</span></span>             | <span data-ttu-id="ec4f2-268">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-268">False</span></span>                             |
| <span data-ttu-id="ec4f2-269">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec4f2-269">In Global Catalog</span></span>      | <span data-ttu-id="ec4f2-270">否</span><span class="sxs-lookup"><span data-stu-id="ec4f2-270">False</span></span>                             |
| <span data-ttu-id="ec4f2-271">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec4f2-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec4f2-272">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec4f2-272">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ec4f2-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec4f2-273">Range-Lower</span></span>            | <span data-ttu-id="ec4f2-274">0</span><span class="sxs-lookup"><span data-stu-id="ec4f2-274">0</span></span>                                 |
| <span data-ttu-id="ec4f2-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec4f2-275">Range-Upper</span></span>            | <span data-ttu-id="ec4f2-276">32767</span><span class="sxs-lookup"><span data-stu-id="ec4f2-276">32767</span></span>                             |
| <span data-ttu-id="ec4f2-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-277">Search-Flags</span></span>           | <span data-ttu-id="ec4f2-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec4f2-278">0x00000000</span></span>                        |
| <span data-ttu-id="ec4f2-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec4f2-279">System-Flags</span></span>           | <span data-ttu-id="ec4f2-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec4f2-280">0x00000010</span></span>                        |
| <span data-ttu-id="ec4f2-281">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec4f2-281">Classes used in</span></span>        | [<span data-ttu-id="ec4f2-282">**User**</span><span class="sxs-lookup"><span data-stu-id="ec4f2-282">**User**</span></span>](c-user.md)<br/> |



 

 





