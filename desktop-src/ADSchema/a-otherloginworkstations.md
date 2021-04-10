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
# <a name="other-login-workstations-attribute"></a><span data-ttu-id="42a42-105">其他-登入工作站屬性</span><span class="sxs-lookup"><span data-stu-id="42a42-105">Other-Login-Workstations attribute</span></span>

<span data-ttu-id="42a42-106">使用者可以登入的非 Windows NT 或 LAN Manager 工作站。</span><span class="sxs-lookup"><span data-stu-id="42a42-106">Non Windows NT or LAN Manager workstations from which a user can log on.</span></span>

> [!Note]  
> <span data-ttu-id="42a42-107">Active Directory 不會使用或填入此欄位。</span><span class="sxs-lookup"><span data-stu-id="42a42-107">Active Directory does not use or populate this field.</span></span>

 



| <span data-ttu-id="42a42-108">進入</span><span class="sxs-lookup"><span data-stu-id="42a42-108">Entry</span></span> | <span data-ttu-id="42a42-109">值</span><span class="sxs-lookup"><span data-stu-id="42a42-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="42a42-110">CN</span><span class="sxs-lookup"><span data-stu-id="42a42-110">CN</span></span>                | <span data-ttu-id="42a42-111">其他-登入工作站</span><span class="sxs-lookup"><span data-stu-id="42a42-111">Other-Login-Workstations</span></span>                    |
| <span data-ttu-id="42a42-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="42a42-112">Ldap-Display-Name</span></span> | <span data-ttu-id="42a42-113">otherLoginWorkstations</span><span class="sxs-lookup"><span data-stu-id="42a42-113">otherLoginWorkstations</span></span>                      |
| <span data-ttu-id="42a42-114">大小</span><span class="sxs-lookup"><span data-stu-id="42a42-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="42a42-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="42a42-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="42a42-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="42a42-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="42a42-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42a42-117">Attribute-Id</span></span>      | <span data-ttu-id="42a42-118">1.2.840.113556.1.4.91</span><span class="sxs-lookup"><span data-stu-id="42a42-118">1.2.840.113556.1.4.91</span></span>                       |
| <span data-ttu-id="42a42-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="42a42-119">System-Id-Guid</span></span>    | <span data-ttu-id="42a42-120">bf9679f1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="42a42-120">bf9679f1-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="42a42-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a42-121">Syntax</span></span>            | [<span data-ttu-id="42a42-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="42a42-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="42a42-123">實作</span><span class="sxs-lookup"><span data-stu-id="42a42-123">Implementations</span></span>

-   [<span data-ttu-id="42a42-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42a42-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42a42-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42a42-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42a42-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42a42-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42a42-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42a42-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42a42-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42a42-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42a42-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42a42-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42a42-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42a42-130">Windows 2000 Server</span></span>



| <span data-ttu-id="42a42-131">進入</span><span class="sxs-lookup"><span data-stu-id="42a42-131">Entry</span></span> | <span data-ttu-id="42a42-132">值</span><span class="sxs-lookup"><span data-stu-id="42a42-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="42a42-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42a42-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a42-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a42-135">System-Only</span></span>            | <span data-ttu-id="42a42-136">否</span><span class="sxs-lookup"><span data-stu-id="42a42-136">False</span></span>                             |
| <span data-ttu-id="42a42-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42a42-137">Is-Single-Valued</span></span>       | <span data-ttu-id="42a42-138">否</span><span class="sxs-lookup"><span data-stu-id="42a42-138">False</span></span>                             |
| <span data-ttu-id="42a42-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42a42-139">Is Indexed</span></span>             | <span data-ttu-id="42a42-140">否</span><span class="sxs-lookup"><span data-stu-id="42a42-140">False</span></span>                             |
| <span data-ttu-id="42a42-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42a42-141">In Global Catalog</span></span>      | <span data-ttu-id="42a42-142">否</span><span class="sxs-lookup"><span data-stu-id="42a42-142">False</span></span>                             |
| <span data-ttu-id="42a42-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42a42-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a42-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42a42-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="42a42-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a42-145">Range-Lower</span></span>            | <span data-ttu-id="42a42-146">0</span><span class="sxs-lookup"><span data-stu-id="42a42-146">0</span></span>                                 |
| <span data-ttu-id="42a42-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a42-147">Range-Upper</span></span>            | <span data-ttu-id="42a42-148">1024</span><span class="sxs-lookup"><span data-stu-id="42a42-148">1024</span></span>                              |
| <span data-ttu-id="42a42-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-149">Search-Flags</span></span>           | <span data-ttu-id="42a42-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-150">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-151">System-Flags</span></span>           | <span data-ttu-id="42a42-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-152">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42a42-153">Classes used in</span></span>        | [<span data-ttu-id="42a42-154">**User**</span><span class="sxs-lookup"><span data-stu-id="42a42-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42a42-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42a42-155">Windows Server 2003</span></span>



| <span data-ttu-id="42a42-156">進入</span><span class="sxs-lookup"><span data-stu-id="42a42-156">Entry</span></span> | <span data-ttu-id="42a42-157">值</span><span class="sxs-lookup"><span data-stu-id="42a42-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="42a42-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42a42-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a42-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a42-160">System-Only</span></span>            | <span data-ttu-id="42a42-161">否</span><span class="sxs-lookup"><span data-stu-id="42a42-161">False</span></span>                             |
| <span data-ttu-id="42a42-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42a42-162">Is-Single-Valued</span></span>       | <span data-ttu-id="42a42-163">否</span><span class="sxs-lookup"><span data-stu-id="42a42-163">False</span></span>                             |
| <span data-ttu-id="42a42-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42a42-164">Is Indexed</span></span>             | <span data-ttu-id="42a42-165">否</span><span class="sxs-lookup"><span data-stu-id="42a42-165">False</span></span>                             |
| <span data-ttu-id="42a42-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42a42-166">In Global Catalog</span></span>      | <span data-ttu-id="42a42-167">否</span><span class="sxs-lookup"><span data-stu-id="42a42-167">False</span></span>                             |
| <span data-ttu-id="42a42-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42a42-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a42-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42a42-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="42a42-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a42-170">Range-Lower</span></span>            | <span data-ttu-id="42a42-171">0</span><span class="sxs-lookup"><span data-stu-id="42a42-171">0</span></span>                                 |
| <span data-ttu-id="42a42-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a42-172">Range-Upper</span></span>            | <span data-ttu-id="42a42-173">1024</span><span class="sxs-lookup"><span data-stu-id="42a42-173">1024</span></span>                              |
| <span data-ttu-id="42a42-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-174">Search-Flags</span></span>           | <span data-ttu-id="42a42-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-175">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-176">System-Flags</span></span>           | <span data-ttu-id="42a42-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-177">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42a42-178">Classes used in</span></span>        | [<span data-ttu-id="42a42-179">**User**</span><span class="sxs-lookup"><span data-stu-id="42a42-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42a42-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42a42-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42a42-181">進入</span><span class="sxs-lookup"><span data-stu-id="42a42-181">Entry</span></span> | <span data-ttu-id="42a42-182">值</span><span class="sxs-lookup"><span data-stu-id="42a42-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="42a42-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42a42-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a42-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a42-185">System-Only</span></span>            | <span data-ttu-id="42a42-186">否</span><span class="sxs-lookup"><span data-stu-id="42a42-186">False</span></span>                             |
| <span data-ttu-id="42a42-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42a42-187">Is-Single-Valued</span></span>       | <span data-ttu-id="42a42-188">否</span><span class="sxs-lookup"><span data-stu-id="42a42-188">False</span></span>                             |
| <span data-ttu-id="42a42-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42a42-189">Is Indexed</span></span>             | <span data-ttu-id="42a42-190">否</span><span class="sxs-lookup"><span data-stu-id="42a42-190">False</span></span>                             |
| <span data-ttu-id="42a42-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42a42-191">In Global Catalog</span></span>      | <span data-ttu-id="42a42-192">否</span><span class="sxs-lookup"><span data-stu-id="42a42-192">False</span></span>                             |
| <span data-ttu-id="42a42-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42a42-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a42-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42a42-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="42a42-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a42-195">Range-Lower</span></span>            | <span data-ttu-id="42a42-196">0</span><span class="sxs-lookup"><span data-stu-id="42a42-196">0</span></span>                                 |
| <span data-ttu-id="42a42-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a42-197">Range-Upper</span></span>            | <span data-ttu-id="42a42-198">1024</span><span class="sxs-lookup"><span data-stu-id="42a42-198">1024</span></span>                              |
| <span data-ttu-id="42a42-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-199">Search-Flags</span></span>           | <span data-ttu-id="42a42-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-200">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-201">System-Flags</span></span>           | <span data-ttu-id="42a42-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-202">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42a42-203">Classes used in</span></span>        | [<span data-ttu-id="42a42-204">**User**</span><span class="sxs-lookup"><span data-stu-id="42a42-204">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42a42-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42a42-205">Windows Server 2008</span></span>



| <span data-ttu-id="42a42-206">進入</span><span class="sxs-lookup"><span data-stu-id="42a42-206">Entry</span></span> | <span data-ttu-id="42a42-207">值</span><span class="sxs-lookup"><span data-stu-id="42a42-207">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="42a42-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42a42-208">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a42-209">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a42-210">System-Only</span></span>            | <span data-ttu-id="42a42-211">否</span><span class="sxs-lookup"><span data-stu-id="42a42-211">False</span></span>                             |
| <span data-ttu-id="42a42-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42a42-212">Is-Single-Valued</span></span>       | <span data-ttu-id="42a42-213">否</span><span class="sxs-lookup"><span data-stu-id="42a42-213">False</span></span>                             |
| <span data-ttu-id="42a42-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42a42-214">Is Indexed</span></span>             | <span data-ttu-id="42a42-215">否</span><span class="sxs-lookup"><span data-stu-id="42a42-215">False</span></span>                             |
| <span data-ttu-id="42a42-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42a42-216">In Global Catalog</span></span>      | <span data-ttu-id="42a42-217">否</span><span class="sxs-lookup"><span data-stu-id="42a42-217">False</span></span>                             |
| <span data-ttu-id="42a42-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42a42-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a42-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42a42-219">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="42a42-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a42-220">Range-Lower</span></span>            | <span data-ttu-id="42a42-221">0</span><span class="sxs-lookup"><span data-stu-id="42a42-221">0</span></span>                                 |
| <span data-ttu-id="42a42-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a42-222">Range-Upper</span></span>            | <span data-ttu-id="42a42-223">1024</span><span class="sxs-lookup"><span data-stu-id="42a42-223">1024</span></span>                              |
| <span data-ttu-id="42a42-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-224">Search-Flags</span></span>           | <span data-ttu-id="42a42-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-225">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-226">System-Flags</span></span>           | <span data-ttu-id="42a42-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-227">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42a42-228">Classes used in</span></span>        | [<span data-ttu-id="42a42-229">**User**</span><span class="sxs-lookup"><span data-stu-id="42a42-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42a42-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42a42-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42a42-231">進入</span><span class="sxs-lookup"><span data-stu-id="42a42-231">Entry</span></span> | <span data-ttu-id="42a42-232">值</span><span class="sxs-lookup"><span data-stu-id="42a42-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="42a42-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42a42-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a42-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a42-235">System-Only</span></span>            | <span data-ttu-id="42a42-236">否</span><span class="sxs-lookup"><span data-stu-id="42a42-236">False</span></span>                             |
| <span data-ttu-id="42a42-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42a42-237">Is-Single-Valued</span></span>       | <span data-ttu-id="42a42-238">否</span><span class="sxs-lookup"><span data-stu-id="42a42-238">False</span></span>                             |
| <span data-ttu-id="42a42-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42a42-239">Is Indexed</span></span>             | <span data-ttu-id="42a42-240">否</span><span class="sxs-lookup"><span data-stu-id="42a42-240">False</span></span>                             |
| <span data-ttu-id="42a42-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42a42-241">In Global Catalog</span></span>      | <span data-ttu-id="42a42-242">否</span><span class="sxs-lookup"><span data-stu-id="42a42-242">False</span></span>                             |
| <span data-ttu-id="42a42-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42a42-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a42-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42a42-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="42a42-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a42-245">Range-Lower</span></span>            | <span data-ttu-id="42a42-246">0</span><span class="sxs-lookup"><span data-stu-id="42a42-246">0</span></span>                                 |
| <span data-ttu-id="42a42-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a42-247">Range-Upper</span></span>            | <span data-ttu-id="42a42-248">1024</span><span class="sxs-lookup"><span data-stu-id="42a42-248">1024</span></span>                              |
| <span data-ttu-id="42a42-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-249">Search-Flags</span></span>           | <span data-ttu-id="42a42-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-250">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-251">System-Flags</span></span>           | <span data-ttu-id="42a42-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-252">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42a42-253">Classes used in</span></span>        | [<span data-ttu-id="42a42-254">**User**</span><span class="sxs-lookup"><span data-stu-id="42a42-254">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42a42-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42a42-255">Windows Server 2012</span></span>



| <span data-ttu-id="42a42-256">進入</span><span class="sxs-lookup"><span data-stu-id="42a42-256">Entry</span></span> | <span data-ttu-id="42a42-257">值</span><span class="sxs-lookup"><span data-stu-id="42a42-257">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="42a42-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42a42-258">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a42-259">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="42a42-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a42-260">System-Only</span></span>            | <span data-ttu-id="42a42-261">否</span><span class="sxs-lookup"><span data-stu-id="42a42-261">False</span></span>                             |
| <span data-ttu-id="42a42-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42a42-262">Is-Single-Valued</span></span>       | <span data-ttu-id="42a42-263">否</span><span class="sxs-lookup"><span data-stu-id="42a42-263">False</span></span>                             |
| <span data-ttu-id="42a42-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42a42-264">Is Indexed</span></span>             | <span data-ttu-id="42a42-265">否</span><span class="sxs-lookup"><span data-stu-id="42a42-265">False</span></span>                             |
| <span data-ttu-id="42a42-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42a42-266">In Global Catalog</span></span>      | <span data-ttu-id="42a42-267">否</span><span class="sxs-lookup"><span data-stu-id="42a42-267">False</span></span>                             |
| <span data-ttu-id="42a42-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42a42-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a42-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42a42-269">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="42a42-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a42-270">Range-Lower</span></span>            | <span data-ttu-id="42a42-271">0</span><span class="sxs-lookup"><span data-stu-id="42a42-271">0</span></span>                                 |
| <span data-ttu-id="42a42-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a42-272">Range-Upper</span></span>            | <span data-ttu-id="42a42-273">1024</span><span class="sxs-lookup"><span data-stu-id="42a42-273">1024</span></span>                              |
| <span data-ttu-id="42a42-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-274">Search-Flags</span></span>           | <span data-ttu-id="42a42-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-275">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a42-276">System-Flags</span></span>           | <span data-ttu-id="42a42-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a42-277">0x00000010</span></span>                        |
| <span data-ttu-id="42a42-278">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42a42-278">Classes used in</span></span>        | [<span data-ttu-id="42a42-279">**User**</span><span class="sxs-lookup"><span data-stu-id="42a42-279">**User**</span></span>](c-user.md)<br/> |



 

 





