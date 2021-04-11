---
title: Print-Spooling 屬性
description: 代表印表機幕後處理類型的字串。
ms.assetid: cbfa0a3f-dec1-4b7b-855d-426733bcd7f2
ms.tgt_platform: multiple
keywords:
- Print-Spooling 屬性 AD 架構
- printSpooling 屬性 AD 架構
topic_type:
- apiref
api_name:
- Print-Spooling
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c669a00ab523051d3708cc485f65ba484df003c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845336"
---
# <a name="print-spooling-attribute"></a><span data-ttu-id="4c23e-105">Print-Spooling 屬性</span><span class="sxs-lookup"><span data-stu-id="4c23e-105">Print-Spooling attribute</span></span>

<span data-ttu-id="4c23e-106">代表印表機幕後處理類型的字串。</span><span class="sxs-lookup"><span data-stu-id="4c23e-106">A string that represents the type of printer spooling.</span></span>



| <span data-ttu-id="4c23e-107">進入</span><span class="sxs-lookup"><span data-stu-id="4c23e-107">Entry</span></span> | <span data-ttu-id="4c23e-108">值</span><span class="sxs-lookup"><span data-stu-id="4c23e-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="4c23e-109">CN</span><span class="sxs-lookup"><span data-stu-id="4c23e-109">CN</span></span>                | <span data-ttu-id="4c23e-110">Print-Spooling</span><span class="sxs-lookup"><span data-stu-id="4c23e-110">Print-Spooling</span></span>                                                       |
| <span data-ttu-id="4c23e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4c23e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4c23e-112">printSpooling</span><span class="sxs-lookup"><span data-stu-id="4c23e-112">printSpooling</span></span>                                                        |
| <span data-ttu-id="4c23e-113">大小</span><span class="sxs-lookup"><span data-stu-id="4c23e-113">Size</span></span>              | <span data-ttu-id="4c23e-114">可能的值： PrintDirect、PrintWhileSpooling、PrintAfterSpooled。</span><span class="sxs-lookup"><span data-stu-id="4c23e-114">Possible values: PrintDirect, PrintWhileSpooling, PrintAfterSpooled.</span></span> |
| <span data-ttu-id="4c23e-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4c23e-115">Update Privilege</span></span>  | \-                                                                   |
| <span data-ttu-id="4c23e-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4c23e-116">Update Frequency</span></span>  | \-                                                                   |
| <span data-ttu-id="4c23e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4c23e-117">Attribute-Id</span></span>      | <span data-ttu-id="4c23e-118">1.2.840.113556.1.4.274</span><span class="sxs-lookup"><span data-stu-id="4c23e-118">1.2.840.113556.1.4.274</span></span>                                               |
| <span data-ttu-id="4c23e-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4c23e-119">System-Id-Guid</span></span>    | <span data-ttu-id="4c23e-120">ba305f6c-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="4c23e-120">ba305f6c-47e3-11d0-a1a6-00c04fd930c9</span></span>                                 |
| <span data-ttu-id="4c23e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c23e-121">Syntax</span></span>            | [<span data-ttu-id="4c23e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4c23e-122">**String(Unicode)**</span></span>](s-string-unicode.md)                          |



## <a name="implementations"></a><span data-ttu-id="4c23e-123">實作</span><span class="sxs-lookup"><span data-stu-id="4c23e-123">Implementations</span></span>

-   [<span data-ttu-id="4c23e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4c23e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4c23e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4c23e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4c23e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4c23e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4c23e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4c23e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4c23e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4c23e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4c23e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4c23e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4c23e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c23e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4c23e-131">進入</span><span class="sxs-lookup"><span data-stu-id="4c23e-131">Entry</span></span> | <span data-ttu-id="4c23e-132">值</span><span class="sxs-lookup"><span data-stu-id="4c23e-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4c23e-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c23e-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c23e-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c23e-135">System-Only</span></span>            | <span data-ttu-id="4c23e-136">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-136">False</span></span>                                          |
| <span data-ttu-id="4c23e-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c23e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4c23e-138">對</span><span class="sxs-lookup"><span data-stu-id="4c23e-138">True</span></span>                                           |
| <span data-ttu-id="4c23e-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c23e-139">Is Indexed</span></span>             | <span data-ttu-id="4c23e-140">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-140">False</span></span>                                          |
| <span data-ttu-id="4c23e-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c23e-141">In Global Catalog</span></span>      | <span data-ttu-id="4c23e-142">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-142">False</span></span>                                          |
| <span data-ttu-id="4c23e-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c23e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c23e-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c23e-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4c23e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c23e-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c23e-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-147">Search-Flags</span></span>           | <span data-ttu-id="4c23e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c23e-148">0x00000000</span></span>                                     |
| <span data-ttu-id="4c23e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-149">System-Flags</span></span>           | <span data-ttu-id="4c23e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c23e-150">0x00000010</span></span>                                     |
| <span data-ttu-id="4c23e-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c23e-151">Classes used in</span></span>        | [<span data-ttu-id="4c23e-152">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="4c23e-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4c23e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c23e-153">Windows Server 2003</span></span>



| <span data-ttu-id="4c23e-154">進入</span><span class="sxs-lookup"><span data-stu-id="4c23e-154">Entry</span></span> | <span data-ttu-id="4c23e-155">值</span><span class="sxs-lookup"><span data-stu-id="4c23e-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4c23e-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c23e-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c23e-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c23e-158">System-Only</span></span>            | <span data-ttu-id="4c23e-159">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-159">False</span></span>                                          |
| <span data-ttu-id="4c23e-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c23e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4c23e-161">對</span><span class="sxs-lookup"><span data-stu-id="4c23e-161">True</span></span>                                           |
| <span data-ttu-id="4c23e-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c23e-162">Is Indexed</span></span>             | <span data-ttu-id="4c23e-163">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-163">False</span></span>                                          |
| <span data-ttu-id="4c23e-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c23e-164">In Global Catalog</span></span>      | <span data-ttu-id="4c23e-165">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-165">False</span></span>                                          |
| <span data-ttu-id="4c23e-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c23e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c23e-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c23e-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4c23e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c23e-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c23e-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-170">Search-Flags</span></span>           | <span data-ttu-id="4c23e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c23e-171">0x00000000</span></span>                                     |
| <span data-ttu-id="4c23e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-172">System-Flags</span></span>           | <span data-ttu-id="4c23e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c23e-173">0x00000010</span></span>                                     |
| <span data-ttu-id="4c23e-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c23e-174">Classes used in</span></span>        | [<span data-ttu-id="4c23e-175">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="4c23e-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4c23e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4c23e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4c23e-177">進入</span><span class="sxs-lookup"><span data-stu-id="4c23e-177">Entry</span></span> | <span data-ttu-id="4c23e-178">值</span><span class="sxs-lookup"><span data-stu-id="4c23e-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4c23e-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c23e-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c23e-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c23e-181">System-Only</span></span>            | <span data-ttu-id="4c23e-182">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-182">False</span></span>                                          |
| <span data-ttu-id="4c23e-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c23e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4c23e-184">對</span><span class="sxs-lookup"><span data-stu-id="4c23e-184">True</span></span>                                           |
| <span data-ttu-id="4c23e-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c23e-185">Is Indexed</span></span>             | <span data-ttu-id="4c23e-186">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-186">False</span></span>                                          |
| <span data-ttu-id="4c23e-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c23e-187">In Global Catalog</span></span>      | <span data-ttu-id="4c23e-188">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-188">False</span></span>                                          |
| <span data-ttu-id="4c23e-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c23e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c23e-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c23e-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4c23e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c23e-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c23e-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-193">Search-Flags</span></span>           | <span data-ttu-id="4c23e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c23e-194">0x00000000</span></span>                                     |
| <span data-ttu-id="4c23e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-195">System-Flags</span></span>           | <span data-ttu-id="4c23e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c23e-196">0x00000010</span></span>                                     |
| <span data-ttu-id="4c23e-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c23e-197">Classes used in</span></span>        | [<span data-ttu-id="4c23e-198">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="4c23e-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4c23e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c23e-199">Windows Server 2008</span></span>



| <span data-ttu-id="4c23e-200">進入</span><span class="sxs-lookup"><span data-stu-id="4c23e-200">Entry</span></span> | <span data-ttu-id="4c23e-201">值</span><span class="sxs-lookup"><span data-stu-id="4c23e-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4c23e-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c23e-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c23e-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c23e-204">System-Only</span></span>            | <span data-ttu-id="4c23e-205">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-205">False</span></span>                                          |
| <span data-ttu-id="4c23e-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c23e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4c23e-207">對</span><span class="sxs-lookup"><span data-stu-id="4c23e-207">True</span></span>                                           |
| <span data-ttu-id="4c23e-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c23e-208">Is Indexed</span></span>             | <span data-ttu-id="4c23e-209">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-209">False</span></span>                                          |
| <span data-ttu-id="4c23e-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c23e-210">In Global Catalog</span></span>      | <span data-ttu-id="4c23e-211">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-211">False</span></span>                                          |
| <span data-ttu-id="4c23e-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c23e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c23e-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c23e-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4c23e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c23e-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c23e-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-216">Search-Flags</span></span>           | <span data-ttu-id="4c23e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c23e-217">0x00000000</span></span>                                     |
| <span data-ttu-id="4c23e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-218">System-Flags</span></span>           | <span data-ttu-id="4c23e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c23e-219">0x00000010</span></span>                                     |
| <span data-ttu-id="4c23e-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c23e-220">Classes used in</span></span>        | [<span data-ttu-id="4c23e-221">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="4c23e-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4c23e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c23e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4c23e-223">進入</span><span class="sxs-lookup"><span data-stu-id="4c23e-223">Entry</span></span> | <span data-ttu-id="4c23e-224">值</span><span class="sxs-lookup"><span data-stu-id="4c23e-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4c23e-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c23e-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c23e-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c23e-227">System-Only</span></span>            | <span data-ttu-id="4c23e-228">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-228">False</span></span>                                          |
| <span data-ttu-id="4c23e-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c23e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4c23e-230">對</span><span class="sxs-lookup"><span data-stu-id="4c23e-230">True</span></span>                                           |
| <span data-ttu-id="4c23e-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c23e-231">Is Indexed</span></span>             | <span data-ttu-id="4c23e-232">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-232">False</span></span>                                          |
| <span data-ttu-id="4c23e-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c23e-233">In Global Catalog</span></span>      | <span data-ttu-id="4c23e-234">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-234">False</span></span>                                          |
| <span data-ttu-id="4c23e-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c23e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c23e-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c23e-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4c23e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c23e-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c23e-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-239">Search-Flags</span></span>           | <span data-ttu-id="4c23e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c23e-240">0x00000000</span></span>                                     |
| <span data-ttu-id="4c23e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-241">System-Flags</span></span>           | <span data-ttu-id="4c23e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c23e-242">0x00000010</span></span>                                     |
| <span data-ttu-id="4c23e-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c23e-243">Classes used in</span></span>        | [<span data-ttu-id="4c23e-244">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="4c23e-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4c23e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c23e-245">Windows Server 2012</span></span>



| <span data-ttu-id="4c23e-246">進入</span><span class="sxs-lookup"><span data-stu-id="4c23e-246">Entry</span></span> | <span data-ttu-id="4c23e-247">值</span><span class="sxs-lookup"><span data-stu-id="4c23e-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4c23e-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c23e-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c23e-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4c23e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c23e-250">System-Only</span></span>            | <span data-ttu-id="4c23e-251">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-251">False</span></span>                                          |
| <span data-ttu-id="4c23e-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c23e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4c23e-253">對</span><span class="sxs-lookup"><span data-stu-id="4c23e-253">True</span></span>                                           |
| <span data-ttu-id="4c23e-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c23e-254">Is Indexed</span></span>             | <span data-ttu-id="4c23e-255">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-255">False</span></span>                                          |
| <span data-ttu-id="4c23e-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c23e-256">In Global Catalog</span></span>      | <span data-ttu-id="4c23e-257">否</span><span class="sxs-lookup"><span data-stu-id="4c23e-257">False</span></span>                                          |
| <span data-ttu-id="4c23e-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c23e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c23e-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c23e-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4c23e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c23e-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c23e-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="4c23e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-262">Search-Flags</span></span>           | <span data-ttu-id="4c23e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c23e-263">0x00000000</span></span>                                     |
| <span data-ttu-id="4c23e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c23e-264">System-Flags</span></span>           | <span data-ttu-id="4c23e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c23e-265">0x00000010</span></span>                                     |
| <span data-ttu-id="4c23e-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c23e-266">Classes used in</span></span>        | [<span data-ttu-id="4c23e-267">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="4c23e-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





