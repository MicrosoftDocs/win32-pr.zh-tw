---
title: 本機原則旗標屬性
description: 判斷電腦取得其原則之位置的旗標。 本機原則參考。
ms.assetid: 1f2fa723-507a-4e27-a325-8bd6f6cb6bd6
ms.tgt_platform: multiple
keywords:
- 本機原則-旗標屬性 AD 架構
- localPolicyFlags 屬性 AD 架構
topic_type:
- apiref
api_name:
- Local-Policy-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc077fe793a523b41974280ada7e54b82335d733
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971076"
---
# <a name="local-policy-flags-attribute"></a><span data-ttu-id="db155-106">本機原則旗標屬性</span><span class="sxs-lookup"><span data-stu-id="db155-106">Local-Policy-Flags attribute</span></span>

<span data-ttu-id="db155-107">判斷電腦取得其原則之位置的旗標。</span><span class="sxs-lookup"><span data-stu-id="db155-107">Flags that determine where a computer gets its policy.</span></span> <span data-ttu-id="db155-108">本機原則參考。</span><span class="sxs-lookup"><span data-stu-id="db155-108">Local-Policy-Reference.</span></span>



| <span data-ttu-id="db155-109">進入</span><span class="sxs-lookup"><span data-stu-id="db155-109">Entry</span></span> | <span data-ttu-id="db155-110">值</span><span class="sxs-lookup"><span data-stu-id="db155-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="db155-111">CN</span><span class="sxs-lookup"><span data-stu-id="db155-111">CN</span></span>                | <span data-ttu-id="db155-112">本機原則-旗標</span><span class="sxs-lookup"><span data-stu-id="db155-112">Local-Policy-Flags</span></span>                   |
| <span data-ttu-id="db155-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="db155-113">Ldap-Display-Name</span></span> | <span data-ttu-id="db155-114">localPolicyFlags</span><span class="sxs-lookup"><span data-stu-id="db155-114">localPolicyFlags</span></span>                     |
| <span data-ttu-id="db155-115">大小</span><span class="sxs-lookup"><span data-stu-id="db155-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="db155-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="db155-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="db155-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="db155-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="db155-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db155-118">Attribute-Id</span></span>      | <span data-ttu-id="db155-119">1.2.840.113556.1.4.56</span><span class="sxs-lookup"><span data-stu-id="db155-119">1.2.840.113556.1.4.56</span></span>                |
| <span data-ttu-id="db155-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="db155-120">System-Id-Guid</span></span>    | <span data-ttu-id="db155-121">bf96799e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="db155-121">bf96799e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="db155-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="db155-122">Syntax</span></span>            | [<span data-ttu-id="db155-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="db155-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="db155-124">實作</span><span class="sxs-lookup"><span data-stu-id="db155-124">Implementations</span></span>

-   [<span data-ttu-id="db155-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="db155-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="db155-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db155-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db155-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db155-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db155-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db155-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db155-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db155-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db155-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db155-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="db155-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db155-131">Windows 2000 Server</span></span>



| <span data-ttu-id="db155-132">進入</span><span class="sxs-lookup"><span data-stu-id="db155-132">Entry</span></span> | <span data-ttu-id="db155-133">值</span><span class="sxs-lookup"><span data-stu-id="db155-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="db155-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db155-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db155-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="db155-136">System-Only</span></span>            | <span data-ttu-id="db155-137">否</span><span class="sxs-lookup"><span data-stu-id="db155-137">False</span></span>                                     |
| <span data-ttu-id="db155-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db155-138">Is-Single-Valued</span></span>       | <span data-ttu-id="db155-139">對</span><span class="sxs-lookup"><span data-stu-id="db155-139">True</span></span>                                      |
| <span data-ttu-id="db155-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db155-140">Is Indexed</span></span>             | <span data-ttu-id="db155-141">否</span><span class="sxs-lookup"><span data-stu-id="db155-141">False</span></span>                                     |
| <span data-ttu-id="db155-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db155-142">In Global Catalog</span></span>      | <span data-ttu-id="db155-143">否</span><span class="sxs-lookup"><span data-stu-id="db155-143">False</span></span>                                     |
| <span data-ttu-id="db155-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db155-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="db155-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db155-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="db155-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db155-146">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="db155-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db155-147">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="db155-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-148">Search-Flags</span></span>           | <span data-ttu-id="db155-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db155-149">0x00000000</span></span>                                |
| <span data-ttu-id="db155-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-150">System-Flags</span></span>           | <span data-ttu-id="db155-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db155-151">0x00000010</span></span>                                |
| <span data-ttu-id="db155-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db155-152">Classes used in</span></span>        | [<span data-ttu-id="db155-153">**電腦**</span><span class="sxs-lookup"><span data-stu-id="db155-153">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="db155-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db155-154">Windows Server 2003</span></span>



| <span data-ttu-id="db155-155">進入</span><span class="sxs-lookup"><span data-stu-id="db155-155">Entry</span></span> | <span data-ttu-id="db155-156">值</span><span class="sxs-lookup"><span data-stu-id="db155-156">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="db155-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db155-157">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db155-158">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="db155-159">System-Only</span></span>            | <span data-ttu-id="db155-160">否</span><span class="sxs-lookup"><span data-stu-id="db155-160">False</span></span>                                     |
| <span data-ttu-id="db155-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db155-161">Is-Single-Valued</span></span>       | <span data-ttu-id="db155-162">對</span><span class="sxs-lookup"><span data-stu-id="db155-162">True</span></span>                                      |
| <span data-ttu-id="db155-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db155-163">Is Indexed</span></span>             | <span data-ttu-id="db155-164">否</span><span class="sxs-lookup"><span data-stu-id="db155-164">False</span></span>                                     |
| <span data-ttu-id="db155-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db155-165">In Global Catalog</span></span>      | <span data-ttu-id="db155-166">否</span><span class="sxs-lookup"><span data-stu-id="db155-166">False</span></span>                                     |
| <span data-ttu-id="db155-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db155-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="db155-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db155-168">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="db155-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db155-169">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="db155-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db155-170">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="db155-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-171">Search-Flags</span></span>           | <span data-ttu-id="db155-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db155-172">0x00000000</span></span>                                |
| <span data-ttu-id="db155-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-173">System-Flags</span></span>           | <span data-ttu-id="db155-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db155-174">0x00000010</span></span>                                |
| <span data-ttu-id="db155-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db155-175">Classes used in</span></span>        | [<span data-ttu-id="db155-176">**電腦**</span><span class="sxs-lookup"><span data-stu-id="db155-176">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db155-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db155-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db155-178">進入</span><span class="sxs-lookup"><span data-stu-id="db155-178">Entry</span></span> | <span data-ttu-id="db155-179">值</span><span class="sxs-lookup"><span data-stu-id="db155-179">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="db155-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db155-180">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db155-181">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="db155-182">System-Only</span></span>            | <span data-ttu-id="db155-183">否</span><span class="sxs-lookup"><span data-stu-id="db155-183">False</span></span>                                     |
| <span data-ttu-id="db155-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db155-184">Is-Single-Valued</span></span>       | <span data-ttu-id="db155-185">對</span><span class="sxs-lookup"><span data-stu-id="db155-185">True</span></span>                                      |
| <span data-ttu-id="db155-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db155-186">Is Indexed</span></span>             | <span data-ttu-id="db155-187">否</span><span class="sxs-lookup"><span data-stu-id="db155-187">False</span></span>                                     |
| <span data-ttu-id="db155-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db155-188">In Global Catalog</span></span>      | <span data-ttu-id="db155-189">否</span><span class="sxs-lookup"><span data-stu-id="db155-189">False</span></span>                                     |
| <span data-ttu-id="db155-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db155-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="db155-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db155-191">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="db155-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db155-192">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="db155-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db155-193">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="db155-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-194">Search-Flags</span></span>           | <span data-ttu-id="db155-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db155-195">0x00000000</span></span>                                |
| <span data-ttu-id="db155-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-196">System-Flags</span></span>           | <span data-ttu-id="db155-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db155-197">0x00000010</span></span>                                |
| <span data-ttu-id="db155-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db155-198">Classes used in</span></span>        | [<span data-ttu-id="db155-199">**電腦**</span><span class="sxs-lookup"><span data-stu-id="db155-199">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db155-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db155-200">Windows Server 2008</span></span>



| <span data-ttu-id="db155-201">進入</span><span class="sxs-lookup"><span data-stu-id="db155-201">Entry</span></span> | <span data-ttu-id="db155-202">值</span><span class="sxs-lookup"><span data-stu-id="db155-202">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="db155-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db155-203">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db155-204">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="db155-205">System-Only</span></span>            | <span data-ttu-id="db155-206">否</span><span class="sxs-lookup"><span data-stu-id="db155-206">False</span></span>                                     |
| <span data-ttu-id="db155-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db155-207">Is-Single-Valued</span></span>       | <span data-ttu-id="db155-208">對</span><span class="sxs-lookup"><span data-stu-id="db155-208">True</span></span>                                      |
| <span data-ttu-id="db155-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db155-209">Is Indexed</span></span>             | <span data-ttu-id="db155-210">否</span><span class="sxs-lookup"><span data-stu-id="db155-210">False</span></span>                                     |
| <span data-ttu-id="db155-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db155-211">In Global Catalog</span></span>      | <span data-ttu-id="db155-212">否</span><span class="sxs-lookup"><span data-stu-id="db155-212">False</span></span>                                     |
| <span data-ttu-id="db155-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db155-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="db155-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db155-214">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="db155-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db155-215">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="db155-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db155-216">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="db155-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-217">Search-Flags</span></span>           | <span data-ttu-id="db155-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db155-218">0x00000000</span></span>                                |
| <span data-ttu-id="db155-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-219">System-Flags</span></span>           | <span data-ttu-id="db155-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db155-220">0x00000010</span></span>                                |
| <span data-ttu-id="db155-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db155-221">Classes used in</span></span>        | [<span data-ttu-id="db155-222">**電腦**</span><span class="sxs-lookup"><span data-stu-id="db155-222">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db155-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db155-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db155-224">進入</span><span class="sxs-lookup"><span data-stu-id="db155-224">Entry</span></span> | <span data-ttu-id="db155-225">值</span><span class="sxs-lookup"><span data-stu-id="db155-225">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="db155-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db155-226">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db155-227">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="db155-228">System-Only</span></span>            | <span data-ttu-id="db155-229">否</span><span class="sxs-lookup"><span data-stu-id="db155-229">False</span></span>                                     |
| <span data-ttu-id="db155-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db155-230">Is-Single-Valued</span></span>       | <span data-ttu-id="db155-231">對</span><span class="sxs-lookup"><span data-stu-id="db155-231">True</span></span>                                      |
| <span data-ttu-id="db155-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db155-232">Is Indexed</span></span>             | <span data-ttu-id="db155-233">否</span><span class="sxs-lookup"><span data-stu-id="db155-233">False</span></span>                                     |
| <span data-ttu-id="db155-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db155-234">In Global Catalog</span></span>      | <span data-ttu-id="db155-235">否</span><span class="sxs-lookup"><span data-stu-id="db155-235">False</span></span>                                     |
| <span data-ttu-id="db155-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db155-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="db155-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db155-237">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="db155-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db155-238">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="db155-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db155-239">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="db155-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-240">Search-Flags</span></span>           | <span data-ttu-id="db155-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db155-241">0x00000000</span></span>                                |
| <span data-ttu-id="db155-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-242">System-Flags</span></span>           | <span data-ttu-id="db155-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db155-243">0x00000010</span></span>                                |
| <span data-ttu-id="db155-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db155-244">Classes used in</span></span>        | [<span data-ttu-id="db155-245">**電腦**</span><span class="sxs-lookup"><span data-stu-id="db155-245">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db155-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db155-246">Windows Server 2012</span></span>



| <span data-ttu-id="db155-247">進入</span><span class="sxs-lookup"><span data-stu-id="db155-247">Entry</span></span> | <span data-ttu-id="db155-248">值</span><span class="sxs-lookup"><span data-stu-id="db155-248">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="db155-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db155-249">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db155-250">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="db155-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="db155-251">System-Only</span></span>            | <span data-ttu-id="db155-252">否</span><span class="sxs-lookup"><span data-stu-id="db155-252">False</span></span>                                     |
| <span data-ttu-id="db155-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db155-253">Is-Single-Valued</span></span>       | <span data-ttu-id="db155-254">對</span><span class="sxs-lookup"><span data-stu-id="db155-254">True</span></span>                                      |
| <span data-ttu-id="db155-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db155-255">Is Indexed</span></span>             | <span data-ttu-id="db155-256">否</span><span class="sxs-lookup"><span data-stu-id="db155-256">False</span></span>                                     |
| <span data-ttu-id="db155-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db155-257">In Global Catalog</span></span>      | <span data-ttu-id="db155-258">否</span><span class="sxs-lookup"><span data-stu-id="db155-258">False</span></span>                                     |
| <span data-ttu-id="db155-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db155-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="db155-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db155-260">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="db155-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db155-261">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="db155-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db155-262">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="db155-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-263">Search-Flags</span></span>           | <span data-ttu-id="db155-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db155-264">0x00000000</span></span>                                |
| <span data-ttu-id="db155-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db155-265">System-Flags</span></span>           | <span data-ttu-id="db155-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db155-266">0x00000010</span></span>                                |
| <span data-ttu-id="db155-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db155-267">Classes used in</span></span>        | [<span data-ttu-id="db155-268">**電腦**</span><span class="sxs-lookup"><span data-stu-id="db155-268">**Computer**</span></span>](c-computer.md)<br/> |



 

 





