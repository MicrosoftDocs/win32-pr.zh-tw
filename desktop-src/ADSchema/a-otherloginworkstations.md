---
title: 其他-登入工作站屬性
description: 非 8211;可供使用者登入的 Windows NT 或 LAN Manager 工作站。
ms.assetid: feaa1ade-f340-4bca-8787-5ae5aa10d51c
ms.tgt_platform: multiple
keywords:
- 其他-登入工作站屬性 AD 架構
- otherLoginWorkstations 屬性 AD 架構
topic_type:
- apiref
api_name:
- Other-Login-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b71032e96de9ac8d323da8a94e4c50c5cace27c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844972"
---
# <a name="other-login-workstations-attribute"></a><span data-ttu-id="6a131-105">其他-登入工作站屬性</span><span class="sxs-lookup"><span data-stu-id="6a131-105">Other-Login-Workstations attribute</span></span>

<span data-ttu-id="6a131-106">使用者可以登入的非 Windows NT 或 LAN Manager 工作站。</span><span class="sxs-lookup"><span data-stu-id="6a131-106">Non Windows NT or LAN Manager workstations from which a user can log on.</span></span>

> [!Note]  
> <span data-ttu-id="6a131-107">Active Directory 不會使用或填入此欄位。</span><span class="sxs-lookup"><span data-stu-id="6a131-107">Active Directory does not use or populate this field.</span></span>

 



| <span data-ttu-id="6a131-108">進入</span><span class="sxs-lookup"><span data-stu-id="6a131-108">Entry</span></span> | <span data-ttu-id="6a131-109">值</span><span class="sxs-lookup"><span data-stu-id="6a131-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6a131-110">CN</span><span class="sxs-lookup"><span data-stu-id="6a131-110">CN</span></span>                | <span data-ttu-id="6a131-111">其他-登入工作站</span><span class="sxs-lookup"><span data-stu-id="6a131-111">Other-Login-Workstations</span></span>                    |
| <span data-ttu-id="6a131-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6a131-112">Ldap-Display-Name</span></span> | <span data-ttu-id="6a131-113">otherLoginWorkstations</span><span class="sxs-lookup"><span data-stu-id="6a131-113">otherLoginWorkstations</span></span>                      |
| <span data-ttu-id="6a131-114">大小</span><span class="sxs-lookup"><span data-stu-id="6a131-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="6a131-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6a131-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6a131-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6a131-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6a131-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a131-117">Attribute-Id</span></span>      | <span data-ttu-id="6a131-118">1.2.840.113556.1.4.91</span><span class="sxs-lookup"><span data-stu-id="6a131-118">1.2.840.113556.1.4.91</span></span>                       |
| <span data-ttu-id="6a131-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6a131-119">System-Id-Guid</span></span>    | <span data-ttu-id="6a131-120">bf9679f1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6a131-120">bf9679f1-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="6a131-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a131-121">Syntax</span></span>            | [<span data-ttu-id="6a131-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6a131-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6a131-123">實作</span><span class="sxs-lookup"><span data-stu-id="6a131-123">Implementations</span></span>

-   [<span data-ttu-id="6a131-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6a131-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6a131-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a131-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a131-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a131-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a131-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a131-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a131-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a131-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a131-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a131-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6a131-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a131-130">Windows 2000 Server</span></span>



| <span data-ttu-id="6a131-131">進入</span><span class="sxs-lookup"><span data-stu-id="6a131-131">Entry</span></span> | <span data-ttu-id="6a131-132">值</span><span class="sxs-lookup"><span data-stu-id="6a131-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a131-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a131-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a131-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a131-135">System-Only</span></span>            | <span data-ttu-id="6a131-136">否</span><span class="sxs-lookup"><span data-stu-id="6a131-136">False</span></span>                             |
| <span data-ttu-id="6a131-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a131-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6a131-138">否</span><span class="sxs-lookup"><span data-stu-id="6a131-138">False</span></span>                             |
| <span data-ttu-id="6a131-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a131-139">Is Indexed</span></span>             | <span data-ttu-id="6a131-140">否</span><span class="sxs-lookup"><span data-stu-id="6a131-140">False</span></span>                             |
| <span data-ttu-id="6a131-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a131-141">In Global Catalog</span></span>      | <span data-ttu-id="6a131-142">否</span><span class="sxs-lookup"><span data-stu-id="6a131-142">False</span></span>                             |
| <span data-ttu-id="6a131-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a131-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a131-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a131-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a131-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a131-145">Range-Lower</span></span>            | <span data-ttu-id="6a131-146">0</span><span class="sxs-lookup"><span data-stu-id="6a131-146">0</span></span>                                 |
| <span data-ttu-id="6a131-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a131-147">Range-Upper</span></span>            | <span data-ttu-id="6a131-148">1024</span><span class="sxs-lookup"><span data-stu-id="6a131-148">1024</span></span>                              |
| <span data-ttu-id="6a131-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-149">Search-Flags</span></span>           | <span data-ttu-id="6a131-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-150">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-151">System-Flags</span></span>           | <span data-ttu-id="6a131-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-152">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a131-153">Classes used in</span></span>        | [<span data-ttu-id="6a131-154">**User**</span><span class="sxs-lookup"><span data-stu-id="6a131-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6a131-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a131-155">Windows Server 2003</span></span>



| <span data-ttu-id="6a131-156">進入</span><span class="sxs-lookup"><span data-stu-id="6a131-156">Entry</span></span> | <span data-ttu-id="6a131-157">值</span><span class="sxs-lookup"><span data-stu-id="6a131-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a131-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a131-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a131-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a131-160">System-Only</span></span>            | <span data-ttu-id="6a131-161">否</span><span class="sxs-lookup"><span data-stu-id="6a131-161">False</span></span>                             |
| <span data-ttu-id="6a131-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a131-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6a131-163">否</span><span class="sxs-lookup"><span data-stu-id="6a131-163">False</span></span>                             |
| <span data-ttu-id="6a131-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a131-164">Is Indexed</span></span>             | <span data-ttu-id="6a131-165">否</span><span class="sxs-lookup"><span data-stu-id="6a131-165">False</span></span>                             |
| <span data-ttu-id="6a131-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a131-166">In Global Catalog</span></span>      | <span data-ttu-id="6a131-167">否</span><span class="sxs-lookup"><span data-stu-id="6a131-167">False</span></span>                             |
| <span data-ttu-id="6a131-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a131-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a131-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a131-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a131-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a131-170">Range-Lower</span></span>            | <span data-ttu-id="6a131-171">0</span><span class="sxs-lookup"><span data-stu-id="6a131-171">0</span></span>                                 |
| <span data-ttu-id="6a131-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a131-172">Range-Upper</span></span>            | <span data-ttu-id="6a131-173">1024</span><span class="sxs-lookup"><span data-stu-id="6a131-173">1024</span></span>                              |
| <span data-ttu-id="6a131-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-174">Search-Flags</span></span>           | <span data-ttu-id="6a131-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-175">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-176">System-Flags</span></span>           | <span data-ttu-id="6a131-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-177">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a131-178">Classes used in</span></span>        | [<span data-ttu-id="6a131-179">**User**</span><span class="sxs-lookup"><span data-stu-id="6a131-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a131-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a131-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a131-181">進入</span><span class="sxs-lookup"><span data-stu-id="6a131-181">Entry</span></span> | <span data-ttu-id="6a131-182">值</span><span class="sxs-lookup"><span data-stu-id="6a131-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a131-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a131-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a131-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a131-185">System-Only</span></span>            | <span data-ttu-id="6a131-186">否</span><span class="sxs-lookup"><span data-stu-id="6a131-186">False</span></span>                             |
| <span data-ttu-id="6a131-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a131-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6a131-188">否</span><span class="sxs-lookup"><span data-stu-id="6a131-188">False</span></span>                             |
| <span data-ttu-id="6a131-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a131-189">Is Indexed</span></span>             | <span data-ttu-id="6a131-190">否</span><span class="sxs-lookup"><span data-stu-id="6a131-190">False</span></span>                             |
| <span data-ttu-id="6a131-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a131-191">In Global Catalog</span></span>      | <span data-ttu-id="6a131-192">否</span><span class="sxs-lookup"><span data-stu-id="6a131-192">False</span></span>                             |
| <span data-ttu-id="6a131-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a131-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a131-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a131-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a131-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a131-195">Range-Lower</span></span>            | <span data-ttu-id="6a131-196">0</span><span class="sxs-lookup"><span data-stu-id="6a131-196">0</span></span>                                 |
| <span data-ttu-id="6a131-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a131-197">Range-Upper</span></span>            | <span data-ttu-id="6a131-198">1024</span><span class="sxs-lookup"><span data-stu-id="6a131-198">1024</span></span>                              |
| <span data-ttu-id="6a131-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-199">Search-Flags</span></span>           | <span data-ttu-id="6a131-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-200">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-201">System-Flags</span></span>           | <span data-ttu-id="6a131-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-202">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a131-203">Classes used in</span></span>        | [<span data-ttu-id="6a131-204">**User**</span><span class="sxs-lookup"><span data-stu-id="6a131-204">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a131-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a131-205">Windows Server 2008</span></span>



| <span data-ttu-id="6a131-206">進入</span><span class="sxs-lookup"><span data-stu-id="6a131-206">Entry</span></span> | <span data-ttu-id="6a131-207">值</span><span class="sxs-lookup"><span data-stu-id="6a131-207">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a131-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a131-208">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a131-209">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a131-210">System-Only</span></span>            | <span data-ttu-id="6a131-211">否</span><span class="sxs-lookup"><span data-stu-id="6a131-211">False</span></span>                             |
| <span data-ttu-id="6a131-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a131-212">Is-Single-Valued</span></span>       | <span data-ttu-id="6a131-213">否</span><span class="sxs-lookup"><span data-stu-id="6a131-213">False</span></span>                             |
| <span data-ttu-id="6a131-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a131-214">Is Indexed</span></span>             | <span data-ttu-id="6a131-215">否</span><span class="sxs-lookup"><span data-stu-id="6a131-215">False</span></span>                             |
| <span data-ttu-id="6a131-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a131-216">In Global Catalog</span></span>      | <span data-ttu-id="6a131-217">否</span><span class="sxs-lookup"><span data-stu-id="6a131-217">False</span></span>                             |
| <span data-ttu-id="6a131-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a131-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a131-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a131-219">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a131-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a131-220">Range-Lower</span></span>            | <span data-ttu-id="6a131-221">0</span><span class="sxs-lookup"><span data-stu-id="6a131-221">0</span></span>                                 |
| <span data-ttu-id="6a131-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a131-222">Range-Upper</span></span>            | <span data-ttu-id="6a131-223">1024</span><span class="sxs-lookup"><span data-stu-id="6a131-223">1024</span></span>                              |
| <span data-ttu-id="6a131-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-224">Search-Flags</span></span>           | <span data-ttu-id="6a131-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-225">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-226">System-Flags</span></span>           | <span data-ttu-id="6a131-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-227">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a131-228">Classes used in</span></span>        | [<span data-ttu-id="6a131-229">**User**</span><span class="sxs-lookup"><span data-stu-id="6a131-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a131-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a131-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a131-231">進入</span><span class="sxs-lookup"><span data-stu-id="6a131-231">Entry</span></span> | <span data-ttu-id="6a131-232">值</span><span class="sxs-lookup"><span data-stu-id="6a131-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a131-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a131-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a131-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a131-235">System-Only</span></span>            | <span data-ttu-id="6a131-236">否</span><span class="sxs-lookup"><span data-stu-id="6a131-236">False</span></span>                             |
| <span data-ttu-id="6a131-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a131-237">Is-Single-Valued</span></span>       | <span data-ttu-id="6a131-238">否</span><span class="sxs-lookup"><span data-stu-id="6a131-238">False</span></span>                             |
| <span data-ttu-id="6a131-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a131-239">Is Indexed</span></span>             | <span data-ttu-id="6a131-240">否</span><span class="sxs-lookup"><span data-stu-id="6a131-240">False</span></span>                             |
| <span data-ttu-id="6a131-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a131-241">In Global Catalog</span></span>      | <span data-ttu-id="6a131-242">否</span><span class="sxs-lookup"><span data-stu-id="6a131-242">False</span></span>                             |
| <span data-ttu-id="6a131-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a131-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a131-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a131-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a131-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a131-245">Range-Lower</span></span>            | <span data-ttu-id="6a131-246">0</span><span class="sxs-lookup"><span data-stu-id="6a131-246">0</span></span>                                 |
| <span data-ttu-id="6a131-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a131-247">Range-Upper</span></span>            | <span data-ttu-id="6a131-248">1024</span><span class="sxs-lookup"><span data-stu-id="6a131-248">1024</span></span>                              |
| <span data-ttu-id="6a131-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-249">Search-Flags</span></span>           | <span data-ttu-id="6a131-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-250">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-251">System-Flags</span></span>           | <span data-ttu-id="6a131-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-252">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a131-253">Classes used in</span></span>        | [<span data-ttu-id="6a131-254">**User**</span><span class="sxs-lookup"><span data-stu-id="6a131-254">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a131-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a131-255">Windows Server 2012</span></span>



| <span data-ttu-id="6a131-256">進入</span><span class="sxs-lookup"><span data-stu-id="6a131-256">Entry</span></span> | <span data-ttu-id="6a131-257">值</span><span class="sxs-lookup"><span data-stu-id="6a131-257">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6a131-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a131-258">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a131-259">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6a131-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a131-260">System-Only</span></span>            | <span data-ttu-id="6a131-261">否</span><span class="sxs-lookup"><span data-stu-id="6a131-261">False</span></span>                             |
| <span data-ttu-id="6a131-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a131-262">Is-Single-Valued</span></span>       | <span data-ttu-id="6a131-263">否</span><span class="sxs-lookup"><span data-stu-id="6a131-263">False</span></span>                             |
| <span data-ttu-id="6a131-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a131-264">Is Indexed</span></span>             | <span data-ttu-id="6a131-265">否</span><span class="sxs-lookup"><span data-stu-id="6a131-265">False</span></span>                             |
| <span data-ttu-id="6a131-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a131-266">In Global Catalog</span></span>      | <span data-ttu-id="6a131-267">否</span><span class="sxs-lookup"><span data-stu-id="6a131-267">False</span></span>                             |
| <span data-ttu-id="6a131-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a131-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a131-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a131-269">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6a131-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a131-270">Range-Lower</span></span>            | <span data-ttu-id="6a131-271">0</span><span class="sxs-lookup"><span data-stu-id="6a131-271">0</span></span>                                 |
| <span data-ttu-id="6a131-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a131-272">Range-Upper</span></span>            | <span data-ttu-id="6a131-273">1024</span><span class="sxs-lookup"><span data-stu-id="6a131-273">1024</span></span>                              |
| <span data-ttu-id="6a131-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-274">Search-Flags</span></span>           | <span data-ttu-id="6a131-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-275">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a131-276">System-Flags</span></span>           | <span data-ttu-id="6a131-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a131-277">0x00000010</span></span>                        |
| <span data-ttu-id="6a131-278">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a131-278">Classes used in</span></span>        | [<span data-ttu-id="6a131-279">**User**</span><span class="sxs-lookup"><span data-stu-id="6a131-279">**User**</span></span>](c-user.md)<br/> |



 

 





