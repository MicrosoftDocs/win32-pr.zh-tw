---
title: Script-Path 屬性
description: 這個屬性會指定使用者登入腳本的路徑。 字串可以是 null。
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Script-Path 屬性 AD 架構
- scriptPath 屬性 AD 架構
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0909c35c41ae65f75481910d1377aa2761e99487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107956"
---
# <a name="script-path-attribute"></a><span data-ttu-id="97aa0-106">Script-Path 屬性</span><span class="sxs-lookup"><span data-stu-id="97aa0-106">Script-Path attribute</span></span>

<span data-ttu-id="97aa0-107">這個屬性會指定使用者登入腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="97aa0-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="97aa0-108">字串可以是 null。</span><span class="sxs-lookup"><span data-stu-id="97aa0-108">The string can be null.</span></span>



| <span data-ttu-id="97aa0-109">進入</span><span class="sxs-lookup"><span data-stu-id="97aa0-109">Entry</span></span> | <span data-ttu-id="97aa0-110">值</span><span class="sxs-lookup"><span data-stu-id="97aa0-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="97aa0-111">CN</span><span class="sxs-lookup"><span data-stu-id="97aa0-111">CN</span></span>                | <span data-ttu-id="97aa0-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="97aa0-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="97aa0-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="97aa0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="97aa0-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="97aa0-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="97aa0-115">大小</span><span class="sxs-lookup"><span data-stu-id="97aa0-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="97aa0-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="97aa0-116">Update Privilege</span></span>  | <span data-ttu-id="97aa0-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="97aa0-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="97aa0-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="97aa0-118">Update Frequency</span></span>  | <span data-ttu-id="97aa0-119">當使用者記錄建立時，以及每次需要變更路徑時。</span><span class="sxs-lookup"><span data-stu-id="97aa0-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="97aa0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="97aa0-120">Attribute-Id</span></span>      | <span data-ttu-id="97aa0-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="97aa0-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="97aa0-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="97aa0-122">System-Id-Guid</span></span>    | <span data-ttu-id="97aa0-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="97aa0-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="97aa0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="97aa0-124">Syntax</span></span>            | [<span data-ttu-id="97aa0-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="97aa0-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="97aa0-126">實作</span><span class="sxs-lookup"><span data-stu-id="97aa0-126">Implementations</span></span>

-   [<span data-ttu-id="97aa0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="97aa0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="97aa0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="97aa0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="97aa0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="97aa0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="97aa0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="97aa0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="97aa0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="97aa0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="97aa0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="97aa0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="97aa0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="97aa0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="97aa0-134">進入</span><span class="sxs-lookup"><span data-stu-id="97aa0-134">Entry</span></span> | <span data-ttu-id="97aa0-135">值</span><span class="sxs-lookup"><span data-stu-id="97aa0-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97aa0-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97aa0-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97aa0-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="97aa0-138">System-Only</span></span>            | <span data-ttu-id="97aa0-139">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-139">False</span></span>                             |
| <span data-ttu-id="97aa0-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97aa0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="97aa0-141">對</span><span class="sxs-lookup"><span data-stu-id="97aa0-141">True</span></span>                              |
| <span data-ttu-id="97aa0-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97aa0-142">Is Indexed</span></span>             | <span data-ttu-id="97aa0-143">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-143">False</span></span>                             |
| <span data-ttu-id="97aa0-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97aa0-144">In Global Catalog</span></span>      | <span data-ttu-id="97aa0-145">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-145">False</span></span>                             |
| <span data-ttu-id="97aa0-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97aa0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="97aa0-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97aa0-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97aa0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97aa0-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="97aa0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97aa0-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="97aa0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-150">Search-Flags</span></span>           | <span data-ttu-id="97aa0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-151">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-152">System-Flags</span></span>           | <span data-ttu-id="97aa0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-153">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97aa0-154">Classes used in</span></span>        | [<span data-ttu-id="97aa0-155">**User**</span><span class="sxs-lookup"><span data-stu-id="97aa0-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="97aa0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97aa0-156">Windows Server 2003</span></span>



| <span data-ttu-id="97aa0-157">進入</span><span class="sxs-lookup"><span data-stu-id="97aa0-157">Entry</span></span> | <span data-ttu-id="97aa0-158">值</span><span class="sxs-lookup"><span data-stu-id="97aa0-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97aa0-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97aa0-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97aa0-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="97aa0-161">System-Only</span></span>            | <span data-ttu-id="97aa0-162">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-162">False</span></span>                             |
| <span data-ttu-id="97aa0-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97aa0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="97aa0-164">對</span><span class="sxs-lookup"><span data-stu-id="97aa0-164">True</span></span>                              |
| <span data-ttu-id="97aa0-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97aa0-165">Is Indexed</span></span>             | <span data-ttu-id="97aa0-166">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-166">False</span></span>                             |
| <span data-ttu-id="97aa0-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97aa0-167">In Global Catalog</span></span>      | <span data-ttu-id="97aa0-168">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-168">False</span></span>                             |
| <span data-ttu-id="97aa0-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97aa0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="97aa0-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97aa0-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97aa0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97aa0-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="97aa0-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97aa0-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="97aa0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-173">Search-Flags</span></span>           | <span data-ttu-id="97aa0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-174">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-175">System-Flags</span></span>           | <span data-ttu-id="97aa0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-176">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97aa0-177">Classes used in</span></span>        | [<span data-ttu-id="97aa0-178">**User**</span><span class="sxs-lookup"><span data-stu-id="97aa0-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="97aa0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="97aa0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="97aa0-180">進入</span><span class="sxs-lookup"><span data-stu-id="97aa0-180">Entry</span></span> | <span data-ttu-id="97aa0-181">值</span><span class="sxs-lookup"><span data-stu-id="97aa0-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97aa0-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97aa0-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97aa0-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="97aa0-184">System-Only</span></span>            | <span data-ttu-id="97aa0-185">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-185">False</span></span>                             |
| <span data-ttu-id="97aa0-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97aa0-186">Is-Single-Valued</span></span>       | <span data-ttu-id="97aa0-187">對</span><span class="sxs-lookup"><span data-stu-id="97aa0-187">True</span></span>                              |
| <span data-ttu-id="97aa0-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97aa0-188">Is Indexed</span></span>             | <span data-ttu-id="97aa0-189">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-189">False</span></span>                             |
| <span data-ttu-id="97aa0-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97aa0-190">In Global Catalog</span></span>      | <span data-ttu-id="97aa0-191">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-191">False</span></span>                             |
| <span data-ttu-id="97aa0-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97aa0-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="97aa0-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97aa0-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97aa0-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97aa0-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="97aa0-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97aa0-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="97aa0-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-196">Search-Flags</span></span>           | <span data-ttu-id="97aa0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-197">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-198">System-Flags</span></span>           | <span data-ttu-id="97aa0-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-199">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97aa0-200">Classes used in</span></span>        | [<span data-ttu-id="97aa0-201">**User**</span><span class="sxs-lookup"><span data-stu-id="97aa0-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="97aa0-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97aa0-202">Windows Server 2008</span></span>



| <span data-ttu-id="97aa0-203">進入</span><span class="sxs-lookup"><span data-stu-id="97aa0-203">Entry</span></span> | <span data-ttu-id="97aa0-204">值</span><span class="sxs-lookup"><span data-stu-id="97aa0-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97aa0-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97aa0-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97aa0-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="97aa0-207">System-Only</span></span>            | <span data-ttu-id="97aa0-208">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-208">False</span></span>                             |
| <span data-ttu-id="97aa0-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97aa0-209">Is-Single-Valued</span></span>       | <span data-ttu-id="97aa0-210">對</span><span class="sxs-lookup"><span data-stu-id="97aa0-210">True</span></span>                              |
| <span data-ttu-id="97aa0-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97aa0-211">Is Indexed</span></span>             | <span data-ttu-id="97aa0-212">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-212">False</span></span>                             |
| <span data-ttu-id="97aa0-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97aa0-213">In Global Catalog</span></span>      | <span data-ttu-id="97aa0-214">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-214">False</span></span>                             |
| <span data-ttu-id="97aa0-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97aa0-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="97aa0-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97aa0-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97aa0-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97aa0-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="97aa0-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97aa0-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="97aa0-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-219">Search-Flags</span></span>           | <span data-ttu-id="97aa0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-220">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-221">System-Flags</span></span>           | <span data-ttu-id="97aa0-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-222">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97aa0-223">Classes used in</span></span>        | [<span data-ttu-id="97aa0-224">**User**</span><span class="sxs-lookup"><span data-stu-id="97aa0-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="97aa0-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97aa0-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="97aa0-226">進入</span><span class="sxs-lookup"><span data-stu-id="97aa0-226">Entry</span></span> | <span data-ttu-id="97aa0-227">值</span><span class="sxs-lookup"><span data-stu-id="97aa0-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97aa0-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97aa0-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97aa0-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="97aa0-230">System-Only</span></span>            | <span data-ttu-id="97aa0-231">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-231">False</span></span>                             |
| <span data-ttu-id="97aa0-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97aa0-232">Is-Single-Valued</span></span>       | <span data-ttu-id="97aa0-233">對</span><span class="sxs-lookup"><span data-stu-id="97aa0-233">True</span></span>                              |
| <span data-ttu-id="97aa0-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97aa0-234">Is Indexed</span></span>             | <span data-ttu-id="97aa0-235">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-235">False</span></span>                             |
| <span data-ttu-id="97aa0-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97aa0-236">In Global Catalog</span></span>      | <span data-ttu-id="97aa0-237">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-237">False</span></span>                             |
| <span data-ttu-id="97aa0-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97aa0-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="97aa0-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97aa0-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97aa0-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97aa0-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="97aa0-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97aa0-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="97aa0-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-242">Search-Flags</span></span>           | <span data-ttu-id="97aa0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-243">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-244">System-Flags</span></span>           | <span data-ttu-id="97aa0-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-245">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97aa0-246">Classes used in</span></span>        | [<span data-ttu-id="97aa0-247">**User**</span><span class="sxs-lookup"><span data-stu-id="97aa0-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="97aa0-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97aa0-248">Windows Server 2012</span></span>



| <span data-ttu-id="97aa0-249">進入</span><span class="sxs-lookup"><span data-stu-id="97aa0-249">Entry</span></span> | <span data-ttu-id="97aa0-250">值</span><span class="sxs-lookup"><span data-stu-id="97aa0-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="97aa0-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="97aa0-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="97aa0-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="97aa0-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="97aa0-253">System-Only</span></span>            | <span data-ttu-id="97aa0-254">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-254">False</span></span>                             |
| <span data-ttu-id="97aa0-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="97aa0-255">Is-Single-Valued</span></span>       | <span data-ttu-id="97aa0-256">對</span><span class="sxs-lookup"><span data-stu-id="97aa0-256">True</span></span>                              |
| <span data-ttu-id="97aa0-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="97aa0-257">Is Indexed</span></span>             | <span data-ttu-id="97aa0-258">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-258">False</span></span>                             |
| <span data-ttu-id="97aa0-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="97aa0-259">In Global Catalog</span></span>      | <span data-ttu-id="97aa0-260">否</span><span class="sxs-lookup"><span data-stu-id="97aa0-260">False</span></span>                             |
| <span data-ttu-id="97aa0-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="97aa0-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="97aa0-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="97aa0-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="97aa0-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="97aa0-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="97aa0-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="97aa0-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="97aa0-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-265">Search-Flags</span></span>           | <span data-ttu-id="97aa0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-266">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="97aa0-267">System-Flags</span></span>           | <span data-ttu-id="97aa0-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="97aa0-268">0x00000010</span></span>                        |
| <span data-ttu-id="97aa0-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="97aa0-269">Classes used in</span></span>        | [<span data-ttu-id="97aa0-270">**User**</span><span class="sxs-lookup"><span data-stu-id="97aa0-270">**User**</span></span>](c-user.md)<br/> |



 

 





