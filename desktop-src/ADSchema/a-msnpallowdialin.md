---
title: msNPAllowDialin 屬性
description: 指出帳戶是否有權撥入 RAS 伺服器。
ms.assetid: 8e0d98b4-93b1-4a76-a8b7-d6017028b48a
ms.tgt_platform: multiple
keywords:
- msNPAllowDialin 屬性 AD 架構
topic_type:
- apiref
api_name:
- msNPAllowDialin
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e56f9fe3817053e3e1e49611fb76934acbbcba9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108077"
---
# <a name="msnpallowdialin-attribute"></a><span data-ttu-id="46074-104">msNPAllowDialin 屬性</span><span class="sxs-lookup"><span data-stu-id="46074-104">msNPAllowDialin attribute</span></span>

<span data-ttu-id="46074-105">指出帳戶是否有權撥入 RAS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="46074-105">Indicates whether the account has permission to dial in to the RAS server.</span></span> <span data-ttu-id="46074-106">請勿直接修改此值。</span><span class="sxs-lookup"><span data-stu-id="46074-106">Do not modify this value directly.</span></span> <span data-ttu-id="46074-107">使用適當的 [RAS 管理功能](/windows/desktop/RRAS/ras-administration-functions) 來修改此值。</span><span class="sxs-lookup"><span data-stu-id="46074-107">Use the appropriate [RAS administration function](/windows/desktop/RRAS/ras-administration-functions) to modify this value.</span></span>



| <span data-ttu-id="46074-108">進入</span><span class="sxs-lookup"><span data-stu-id="46074-108">Entry</span></span> | <span data-ttu-id="46074-109">值</span><span class="sxs-lookup"><span data-stu-id="46074-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="46074-110">CN</span><span class="sxs-lookup"><span data-stu-id="46074-110">CN</span></span>                | <span data-ttu-id="46074-111">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="46074-111">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="46074-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="46074-112">Ldap-Display-Name</span></span> | <span data-ttu-id="46074-113">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="46074-113">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="46074-114">大小</span><span class="sxs-lookup"><span data-stu-id="46074-114">Size</span></span>              | <span data-ttu-id="46074-115">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="46074-115">4 bytes</span></span>                              |
| <span data-ttu-id="46074-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="46074-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="46074-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="46074-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="46074-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46074-118">Attribute-Id</span></span>      | <span data-ttu-id="46074-119">1.2.840.113556.1.4.1119</span><span class="sxs-lookup"><span data-stu-id="46074-119">1.2.840.113556.1.4.1119</span></span>              |
| <span data-ttu-id="46074-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="46074-120">System-Id-Guid</span></span>    | <span data-ttu-id="46074-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="46074-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="46074-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="46074-122">Syntax</span></span>            | [<span data-ttu-id="46074-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="46074-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="46074-124">實作</span><span class="sxs-lookup"><span data-stu-id="46074-124">Implementations</span></span>

-   [<span data-ttu-id="46074-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="46074-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="46074-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46074-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46074-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46074-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46074-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46074-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46074-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46074-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46074-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46074-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="46074-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46074-131">Windows 2000 Server</span></span>



| <span data-ttu-id="46074-132">進入</span><span class="sxs-lookup"><span data-stu-id="46074-132">Entry</span></span> | <span data-ttu-id="46074-133">值</span><span class="sxs-lookup"><span data-stu-id="46074-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46074-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46074-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46074-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="46074-136">System-Only</span></span>            | <span data-ttu-id="46074-137">否</span><span class="sxs-lookup"><span data-stu-id="46074-137">False</span></span>                             |
| <span data-ttu-id="46074-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46074-138">Is-Single-Valued</span></span>       | <span data-ttu-id="46074-139">對</span><span class="sxs-lookup"><span data-stu-id="46074-139">True</span></span>                              |
| <span data-ttu-id="46074-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46074-140">Is Indexed</span></span>             | <span data-ttu-id="46074-141">否</span><span class="sxs-lookup"><span data-stu-id="46074-141">False</span></span>                             |
| <span data-ttu-id="46074-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46074-142">In Global Catalog</span></span>      | <span data-ttu-id="46074-143">否</span><span class="sxs-lookup"><span data-stu-id="46074-143">False</span></span>                             |
| <span data-ttu-id="46074-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46074-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="46074-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46074-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46074-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46074-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46074-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46074-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46074-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-148">Search-Flags</span></span>           | <span data-ttu-id="46074-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46074-149">0x00000000</span></span>                        |
| <span data-ttu-id="46074-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-150">System-Flags</span></span>           | <span data-ttu-id="46074-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-151">0x00000010</span></span>                        |
| <span data-ttu-id="46074-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46074-152">Classes used in</span></span>        | [<span data-ttu-id="46074-153">**User**</span><span class="sxs-lookup"><span data-stu-id="46074-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="46074-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46074-154">Windows Server 2003</span></span>



| <span data-ttu-id="46074-155">進入</span><span class="sxs-lookup"><span data-stu-id="46074-155">Entry</span></span> | <span data-ttu-id="46074-156">值</span><span class="sxs-lookup"><span data-stu-id="46074-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46074-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46074-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46074-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="46074-159">System-Only</span></span>            | <span data-ttu-id="46074-160">否</span><span class="sxs-lookup"><span data-stu-id="46074-160">False</span></span>                             |
| <span data-ttu-id="46074-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46074-161">Is-Single-Valued</span></span>       | <span data-ttu-id="46074-162">對</span><span class="sxs-lookup"><span data-stu-id="46074-162">True</span></span>                              |
| <span data-ttu-id="46074-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46074-163">Is Indexed</span></span>             | <span data-ttu-id="46074-164">否</span><span class="sxs-lookup"><span data-stu-id="46074-164">False</span></span>                             |
| <span data-ttu-id="46074-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46074-165">In Global Catalog</span></span>      | <span data-ttu-id="46074-166">否</span><span class="sxs-lookup"><span data-stu-id="46074-166">False</span></span>                             |
| <span data-ttu-id="46074-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46074-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="46074-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46074-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46074-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46074-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46074-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46074-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46074-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-171">Search-Flags</span></span>           | <span data-ttu-id="46074-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46074-172">0x00000000</span></span>                        |
| <span data-ttu-id="46074-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-173">System-Flags</span></span>           | <span data-ttu-id="46074-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-174">0x00000010</span></span>                        |
| <span data-ttu-id="46074-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46074-175">Classes used in</span></span>        | [<span data-ttu-id="46074-176">**User**</span><span class="sxs-lookup"><span data-stu-id="46074-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46074-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46074-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46074-178">進入</span><span class="sxs-lookup"><span data-stu-id="46074-178">Entry</span></span> | <span data-ttu-id="46074-179">值</span><span class="sxs-lookup"><span data-stu-id="46074-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46074-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46074-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46074-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="46074-182">System-Only</span></span>            | <span data-ttu-id="46074-183">否</span><span class="sxs-lookup"><span data-stu-id="46074-183">False</span></span>                             |
| <span data-ttu-id="46074-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46074-184">Is-Single-Valued</span></span>       | <span data-ttu-id="46074-185">對</span><span class="sxs-lookup"><span data-stu-id="46074-185">True</span></span>                              |
| <span data-ttu-id="46074-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46074-186">Is Indexed</span></span>             | <span data-ttu-id="46074-187">否</span><span class="sxs-lookup"><span data-stu-id="46074-187">False</span></span>                             |
| <span data-ttu-id="46074-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46074-188">In Global Catalog</span></span>      | <span data-ttu-id="46074-189">否</span><span class="sxs-lookup"><span data-stu-id="46074-189">False</span></span>                             |
| <span data-ttu-id="46074-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46074-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="46074-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46074-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46074-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46074-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46074-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46074-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46074-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-194">Search-Flags</span></span>           | <span data-ttu-id="46074-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46074-195">0x00000000</span></span>                        |
| <span data-ttu-id="46074-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-196">System-Flags</span></span>           | <span data-ttu-id="46074-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-197">0x00000010</span></span>                        |
| <span data-ttu-id="46074-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46074-198">Classes used in</span></span>        | [<span data-ttu-id="46074-199">**User**</span><span class="sxs-lookup"><span data-stu-id="46074-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46074-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46074-200">Windows Server 2008</span></span>



| <span data-ttu-id="46074-201">進入</span><span class="sxs-lookup"><span data-stu-id="46074-201">Entry</span></span> | <span data-ttu-id="46074-202">值</span><span class="sxs-lookup"><span data-stu-id="46074-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46074-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46074-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46074-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="46074-205">System-Only</span></span>            | <span data-ttu-id="46074-206">否</span><span class="sxs-lookup"><span data-stu-id="46074-206">False</span></span>                             |
| <span data-ttu-id="46074-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46074-207">Is-Single-Valued</span></span>       | <span data-ttu-id="46074-208">對</span><span class="sxs-lookup"><span data-stu-id="46074-208">True</span></span>                              |
| <span data-ttu-id="46074-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46074-209">Is Indexed</span></span>             | <span data-ttu-id="46074-210">否</span><span class="sxs-lookup"><span data-stu-id="46074-210">False</span></span>                             |
| <span data-ttu-id="46074-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46074-211">In Global Catalog</span></span>      | <span data-ttu-id="46074-212">否</span><span class="sxs-lookup"><span data-stu-id="46074-212">False</span></span>                             |
| <span data-ttu-id="46074-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46074-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="46074-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46074-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46074-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46074-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46074-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46074-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46074-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-217">Search-Flags</span></span>           | <span data-ttu-id="46074-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-218">0x00000010</span></span>                        |
| <span data-ttu-id="46074-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-219">System-Flags</span></span>           | <span data-ttu-id="46074-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-220">0x00000010</span></span>                        |
| <span data-ttu-id="46074-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46074-221">Classes used in</span></span>        | [<span data-ttu-id="46074-222">**User**</span><span class="sxs-lookup"><span data-stu-id="46074-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46074-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46074-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46074-224">進入</span><span class="sxs-lookup"><span data-stu-id="46074-224">Entry</span></span> | <span data-ttu-id="46074-225">值</span><span class="sxs-lookup"><span data-stu-id="46074-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46074-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46074-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46074-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="46074-228">System-Only</span></span>            | <span data-ttu-id="46074-229">否</span><span class="sxs-lookup"><span data-stu-id="46074-229">False</span></span>                             |
| <span data-ttu-id="46074-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46074-230">Is-Single-Valued</span></span>       | <span data-ttu-id="46074-231">對</span><span class="sxs-lookup"><span data-stu-id="46074-231">True</span></span>                              |
| <span data-ttu-id="46074-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46074-232">Is Indexed</span></span>             | <span data-ttu-id="46074-233">否</span><span class="sxs-lookup"><span data-stu-id="46074-233">False</span></span>                             |
| <span data-ttu-id="46074-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46074-234">In Global Catalog</span></span>      | <span data-ttu-id="46074-235">否</span><span class="sxs-lookup"><span data-stu-id="46074-235">False</span></span>                             |
| <span data-ttu-id="46074-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46074-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="46074-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46074-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46074-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46074-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46074-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46074-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46074-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-240">Search-Flags</span></span>           | <span data-ttu-id="46074-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-241">0x00000010</span></span>                        |
| <span data-ttu-id="46074-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-242">System-Flags</span></span>           | <span data-ttu-id="46074-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-243">0x00000010</span></span>                        |
| <span data-ttu-id="46074-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46074-244">Classes used in</span></span>        | [<span data-ttu-id="46074-245">**User**</span><span class="sxs-lookup"><span data-stu-id="46074-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46074-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46074-246">Windows Server 2012</span></span>



| <span data-ttu-id="46074-247">進入</span><span class="sxs-lookup"><span data-stu-id="46074-247">Entry</span></span> | <span data-ttu-id="46074-248">值</span><span class="sxs-lookup"><span data-stu-id="46074-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="46074-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46074-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46074-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="46074-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="46074-251">System-Only</span></span>            | <span data-ttu-id="46074-252">否</span><span class="sxs-lookup"><span data-stu-id="46074-252">False</span></span>                             |
| <span data-ttu-id="46074-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46074-253">Is-Single-Valued</span></span>       | <span data-ttu-id="46074-254">對</span><span class="sxs-lookup"><span data-stu-id="46074-254">True</span></span>                              |
| <span data-ttu-id="46074-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46074-255">Is Indexed</span></span>             | <span data-ttu-id="46074-256">否</span><span class="sxs-lookup"><span data-stu-id="46074-256">False</span></span>                             |
| <span data-ttu-id="46074-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46074-257">In Global Catalog</span></span>      | <span data-ttu-id="46074-258">否</span><span class="sxs-lookup"><span data-stu-id="46074-258">False</span></span>                             |
| <span data-ttu-id="46074-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46074-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="46074-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46074-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="46074-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46074-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="46074-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46074-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="46074-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-263">Search-Flags</span></span>           | <span data-ttu-id="46074-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-264">0x00000010</span></span>                        |
| <span data-ttu-id="46074-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46074-265">System-Flags</span></span>           | <span data-ttu-id="46074-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46074-266">0x00000010</span></span>                        |
| <span data-ttu-id="46074-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46074-267">Classes used in</span></span>        | [<span data-ttu-id="46074-268">**User**</span><span class="sxs-lookup"><span data-stu-id="46074-268">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="46074-269">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46074-269">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46074-270">RAS 管理功能</span><span class="sxs-lookup"><span data-stu-id="46074-270">RAS Administration Functions</span></span>](/windows/desktop/RRAS/ras-administration-functions)
</dt> </dl>

 

