---
title: USN-Intersite 屬性
description: 網站間複寫的更新序號 (USN) 。
ms.assetid: c4a4640b-2890-46ea-9eb9-8acb9e749499
ms.tgt_platform: multiple
keywords:
- USN-Intersite 屬性 AD 架構
- USNIntersite 屬性 AD 架構
topic_type:
- apiref
api_name:
- USN-Intersite
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d101d854650a689679b95282734865ac19f6ced1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467232"
---
# <a name="usn-intersite-attribute"></a><span data-ttu-id="e83d5-105">USN-Intersite 屬性</span><span class="sxs-lookup"><span data-stu-id="e83d5-105">USN-Intersite attribute</span></span>

<span data-ttu-id="e83d5-106">網站間複寫的更新序號 (USN) 。</span><span class="sxs-lookup"><span data-stu-id="e83d5-106">The update sequence number (USN) for inter-site replication.</span></span>



| <span data-ttu-id="e83d5-107">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-107">Entry</span></span> | <span data-ttu-id="e83d5-108">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e83d5-109">CN</span><span class="sxs-lookup"><span data-stu-id="e83d5-109">CN</span></span>                | <span data-ttu-id="e83d5-110">USN-Intersite</span><span class="sxs-lookup"><span data-stu-id="e83d5-110">USN-Intersite</span></span>                        |
| <span data-ttu-id="e83d5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e83d5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e83d5-112">USNIntersite</span><span class="sxs-lookup"><span data-stu-id="e83d5-112">USNIntersite</span></span>                         |
| <span data-ttu-id="e83d5-113">大小</span><span class="sxs-lookup"><span data-stu-id="e83d5-113">Size</span></span>              | <span data-ttu-id="e83d5-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="e83d5-114">4 bytes</span></span>                              |
| <span data-ttu-id="e83d5-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e83d5-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e83d5-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e83d5-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e83d5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-117">Attribute-Id</span></span>      | <span data-ttu-id="e83d5-118">1.2.840.113556.1.2.469</span><span class="sxs-lookup"><span data-stu-id="e83d5-118">1.2.840.113556.1.2.469</span></span>               |
| <span data-ttu-id="e83d5-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e83d5-119">System-Id-Guid</span></span>    | <span data-ttu-id="e83d5-120">a8df7498-c5ea-11d1-bbcb-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="e83d5-120">a8df7498-c5ea-11d1-bbcb-0080c76670c0</span></span> |
| <span data-ttu-id="e83d5-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e83d5-121">Syntax</span></span>            | [<span data-ttu-id="e83d5-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e83d5-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e83d5-123">實作</span><span class="sxs-lookup"><span data-stu-id="e83d5-123">Implementations</span></span>

-   [<span data-ttu-id="e83d5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e83d5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e83d5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e83d5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e83d5-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e83d5-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e83d5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e83d5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e83d5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e83d5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e83d5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e83d5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e83d5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e83d5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e83d5-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e83d5-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e83d5-132">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-132">Entry</span></span> | <span data-ttu-id="e83d5-133">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e83d5-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e83d5-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e83d5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-135">MAPI-Id</span></span>                | <span data-ttu-id="e83d5-136">0x817A</span><span class="sxs-lookup"><span data-stu-id="e83d5-136">0x817A</span></span>                          |
| <span data-ttu-id="e83d5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e83d5-137">System-Only</span></span>            | <span data-ttu-id="e83d5-138">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-138">False</span></span>                           |
| <span data-ttu-id="e83d5-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e83d5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e83d5-140">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-140">True</span></span>                            |
| <span data-ttu-id="e83d5-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e83d5-141">Is Indexed</span></span>             | <span data-ttu-id="e83d5-142">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-142">True</span></span>                            |
| <span data-ttu-id="e83d5-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e83d5-143">In Global Catalog</span></span>      | <span data-ttu-id="e83d5-144">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-144">False</span></span>                           |
| <span data-ttu-id="e83d5-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e83d5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e83d5-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e83d5-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e83d5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e83d5-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e83d5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e83d5-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e83d5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-149">Search-Flags</span></span>           | <span data-ttu-id="e83d5-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e83d5-150">0x00000001</span></span>                      |
| <span data-ttu-id="e83d5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-151">System-Flags</span></span>           | <span data-ttu-id="e83d5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e83d5-152">0x00000010</span></span>                      |
| <span data-ttu-id="e83d5-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e83d5-153">Classes used in</span></span>        | [<span data-ttu-id="e83d5-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e83d5-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e83d5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e83d5-155">Windows Server 2003</span></span>



| <span data-ttu-id="e83d5-156">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-156">Entry</span></span> | <span data-ttu-id="e83d5-157">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e83d5-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e83d5-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e83d5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-159">MAPI-Id</span></span>                | <span data-ttu-id="e83d5-160">0x817A</span><span class="sxs-lookup"><span data-stu-id="e83d5-160">0x817A</span></span>                          |
| <span data-ttu-id="e83d5-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e83d5-161">System-Only</span></span>            | <span data-ttu-id="e83d5-162">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-162">False</span></span>                           |
| <span data-ttu-id="e83d5-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e83d5-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e83d5-164">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-164">True</span></span>                            |
| <span data-ttu-id="e83d5-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e83d5-165">Is Indexed</span></span>             | <span data-ttu-id="e83d5-166">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-166">True</span></span>                            |
| <span data-ttu-id="e83d5-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e83d5-167">In Global Catalog</span></span>      | <span data-ttu-id="e83d5-168">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-168">False</span></span>                           |
| <span data-ttu-id="e83d5-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e83d5-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e83d5-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e83d5-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e83d5-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e83d5-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e83d5-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e83d5-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e83d5-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-173">Search-Flags</span></span>           | <span data-ttu-id="e83d5-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e83d5-174">0x00000001</span></span>                      |
| <span data-ttu-id="e83d5-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-175">System-Flags</span></span>           | <span data-ttu-id="e83d5-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e83d5-176">0x00000010</span></span>                      |
| <span data-ttu-id="e83d5-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e83d5-177">Classes used in</span></span>        | [<span data-ttu-id="e83d5-178">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e83d5-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e83d5-179">亞當</span><span class="sxs-lookup"><span data-stu-id="e83d5-179">ADAM</span></span>



| <span data-ttu-id="e83d5-180">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-180">Entry</span></span> | <span data-ttu-id="e83d5-181">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e83d5-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e83d5-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e83d5-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-183">MAPI-Id</span></span>                | <span data-ttu-id="e83d5-184">0x817A</span><span class="sxs-lookup"><span data-stu-id="e83d5-184">0x817A</span></span>                          |
| <span data-ttu-id="e83d5-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e83d5-185">System-Only</span></span>            | <span data-ttu-id="e83d5-186">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-186">False</span></span>                           |
| <span data-ttu-id="e83d5-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e83d5-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e83d5-188">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-188">True</span></span>                            |
| <span data-ttu-id="e83d5-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e83d5-189">Is Indexed</span></span>             | <span data-ttu-id="e83d5-190">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-190">True</span></span>                            |
| <span data-ttu-id="e83d5-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e83d5-191">In Global Catalog</span></span>      | <span data-ttu-id="e83d5-192">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-192">False</span></span>                           |
| <span data-ttu-id="e83d5-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e83d5-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e83d5-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e83d5-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e83d5-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e83d5-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e83d5-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e83d5-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e83d5-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-197">Search-Flags</span></span>           | <span data-ttu-id="e83d5-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e83d5-198">0x00000001</span></span>                      |
| <span data-ttu-id="e83d5-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-199">System-Flags</span></span>           | <span data-ttu-id="e83d5-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e83d5-200">0x00000010</span></span>                      |
| <span data-ttu-id="e83d5-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e83d5-201">Classes used in</span></span>        | [<span data-ttu-id="e83d5-202">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e83d5-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e83d5-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e83d5-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e83d5-204">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-204">Entry</span></span> | <span data-ttu-id="e83d5-205">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e83d5-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e83d5-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e83d5-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-207">MAPI-Id</span></span>                | <span data-ttu-id="e83d5-208">0x817A</span><span class="sxs-lookup"><span data-stu-id="e83d5-208">0x817A</span></span>                          |
| <span data-ttu-id="e83d5-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e83d5-209">System-Only</span></span>            | <span data-ttu-id="e83d5-210">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-210">False</span></span>                           |
| <span data-ttu-id="e83d5-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e83d5-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e83d5-212">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-212">True</span></span>                            |
| <span data-ttu-id="e83d5-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e83d5-213">Is Indexed</span></span>             | <span data-ttu-id="e83d5-214">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-214">True</span></span>                            |
| <span data-ttu-id="e83d5-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e83d5-215">In Global Catalog</span></span>      | <span data-ttu-id="e83d5-216">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-216">False</span></span>                           |
| <span data-ttu-id="e83d5-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e83d5-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e83d5-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e83d5-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e83d5-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e83d5-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e83d5-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e83d5-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e83d5-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-221">Search-Flags</span></span>           | <span data-ttu-id="e83d5-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e83d5-222">0x00000001</span></span>                      |
| <span data-ttu-id="e83d5-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-223">System-Flags</span></span>           | <span data-ttu-id="e83d5-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e83d5-224">0x00000010</span></span>                      |
| <span data-ttu-id="e83d5-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e83d5-225">Classes used in</span></span>        | [<span data-ttu-id="e83d5-226">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e83d5-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e83d5-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e83d5-227">Windows Server 2008</span></span>



| <span data-ttu-id="e83d5-228">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-228">Entry</span></span> | <span data-ttu-id="e83d5-229">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e83d5-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e83d5-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e83d5-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-231">MAPI-Id</span></span>                | <span data-ttu-id="e83d5-232">0x817A</span><span class="sxs-lookup"><span data-stu-id="e83d5-232">0x817A</span></span>                          |
| <span data-ttu-id="e83d5-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="e83d5-233">System-Only</span></span>            | <span data-ttu-id="e83d5-234">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-234">False</span></span>                           |
| <span data-ttu-id="e83d5-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e83d5-235">Is-Single-Valued</span></span>       | <span data-ttu-id="e83d5-236">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-236">True</span></span>                            |
| <span data-ttu-id="e83d5-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e83d5-237">Is Indexed</span></span>             | <span data-ttu-id="e83d5-238">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-238">True</span></span>                            |
| <span data-ttu-id="e83d5-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e83d5-239">In Global Catalog</span></span>      | <span data-ttu-id="e83d5-240">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-240">False</span></span>                           |
| <span data-ttu-id="e83d5-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e83d5-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="e83d5-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e83d5-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e83d5-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e83d5-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e83d5-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e83d5-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e83d5-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-245">Search-Flags</span></span>           | <span data-ttu-id="e83d5-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e83d5-246">0x00000001</span></span>                      |
| <span data-ttu-id="e83d5-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-247">System-Flags</span></span>           | <span data-ttu-id="e83d5-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e83d5-248">0x00000010</span></span>                      |
| <span data-ttu-id="e83d5-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e83d5-249">Classes used in</span></span>        | [<span data-ttu-id="e83d5-250">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e83d5-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e83d5-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e83d5-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e83d5-252">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-252">Entry</span></span> | <span data-ttu-id="e83d5-253">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e83d5-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e83d5-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e83d5-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-255">MAPI-Id</span></span>                | <span data-ttu-id="e83d5-256">0x817A</span><span class="sxs-lookup"><span data-stu-id="e83d5-256">0x817A</span></span>                          |
| <span data-ttu-id="e83d5-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="e83d5-257">System-Only</span></span>            | <span data-ttu-id="e83d5-258">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-258">False</span></span>                           |
| <span data-ttu-id="e83d5-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e83d5-259">Is-Single-Valued</span></span>       | <span data-ttu-id="e83d5-260">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-260">True</span></span>                            |
| <span data-ttu-id="e83d5-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e83d5-261">Is Indexed</span></span>             | <span data-ttu-id="e83d5-262">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-262">True</span></span>                            |
| <span data-ttu-id="e83d5-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e83d5-263">In Global Catalog</span></span>      | <span data-ttu-id="e83d5-264">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-264">False</span></span>                           |
| <span data-ttu-id="e83d5-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e83d5-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="e83d5-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e83d5-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e83d5-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e83d5-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e83d5-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e83d5-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e83d5-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-269">Search-Flags</span></span>           | <span data-ttu-id="e83d5-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e83d5-270">0x00000001</span></span>                      |
| <span data-ttu-id="e83d5-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-271">System-Flags</span></span>           | <span data-ttu-id="e83d5-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e83d5-272">0x00000010</span></span>                      |
| <span data-ttu-id="e83d5-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e83d5-273">Classes used in</span></span>        | [<span data-ttu-id="e83d5-274">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e83d5-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e83d5-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e83d5-275">Windows Server 2012</span></span>



| <span data-ttu-id="e83d5-276">進入</span><span class="sxs-lookup"><span data-stu-id="e83d5-276">Entry</span></span> | <span data-ttu-id="e83d5-277">值</span><span class="sxs-lookup"><span data-stu-id="e83d5-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="e83d5-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e83d5-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="e83d5-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e83d5-279">MAPI-Id</span></span>                | <span data-ttu-id="e83d5-280">0x817A</span><span class="sxs-lookup"><span data-stu-id="e83d5-280">0x817A</span></span>                          |
| <span data-ttu-id="e83d5-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="e83d5-281">System-Only</span></span>            | <span data-ttu-id="e83d5-282">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-282">False</span></span>                           |
| <span data-ttu-id="e83d5-283">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e83d5-283">Is-Single-Valued</span></span>       | <span data-ttu-id="e83d5-284">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-284">True</span></span>                            |
| <span data-ttu-id="e83d5-285">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e83d5-285">Is Indexed</span></span>             | <span data-ttu-id="e83d5-286">對</span><span class="sxs-lookup"><span data-stu-id="e83d5-286">True</span></span>                            |
| <span data-ttu-id="e83d5-287">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e83d5-287">In Global Catalog</span></span>      | <span data-ttu-id="e83d5-288">否</span><span class="sxs-lookup"><span data-stu-id="e83d5-288">False</span></span>                           |
| <span data-ttu-id="e83d5-289">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e83d5-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="e83d5-290">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e83d5-290">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="e83d5-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e83d5-291">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="e83d5-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e83d5-292">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="e83d5-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-293">Search-Flags</span></span>           | <span data-ttu-id="e83d5-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e83d5-294">0x00000001</span></span>                      |
| <span data-ttu-id="e83d5-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e83d5-295">System-Flags</span></span>           | <span data-ttu-id="e83d5-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e83d5-296">0x00000010</span></span>                      |
| <span data-ttu-id="e83d5-297">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e83d5-297">Classes used in</span></span>        | [<span data-ttu-id="e83d5-298">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="e83d5-298">**Top**</span></span>](c-top.md)<br/> |



 

 





