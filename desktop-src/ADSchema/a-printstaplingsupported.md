---
title: 列印裝訂-支援的屬性
description: 如果印表機支援裝訂，則為 TRUE。 由驅動程式提供。
ms.assetid: c0d1cbc5-7657-45a8-b154-a67f57386f52
ms.tgt_platform: multiple
keywords:
- 列印裝訂-支援的屬性 AD 架構
- printStaplingSupported 屬性 AD 架構
topic_type:
- apiref
api_name:
- Print-Stapling-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12303d9a18f267ec4eaef3a33dc8ec7350967aa6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970241"
---
# <a name="print-stapling-supported-attribute"></a><span data-ttu-id="080e9-106">列印裝訂-支援的屬性</span><span class="sxs-lookup"><span data-stu-id="080e9-106">Print-Stapling-Supported attribute</span></span>

<span data-ttu-id="080e9-107">如果印表機支援裝訂，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="080e9-107">**TRUE** if the printer supports stapling.</span></span> <span data-ttu-id="080e9-108">由驅動程式提供。</span><span class="sxs-lookup"><span data-stu-id="080e9-108">Supplied by the driver.</span></span>



| <span data-ttu-id="080e9-109">進入</span><span class="sxs-lookup"><span data-stu-id="080e9-109">Entry</span></span> | <span data-ttu-id="080e9-110">值</span><span class="sxs-lookup"><span data-stu-id="080e9-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="080e9-111">CN</span><span class="sxs-lookup"><span data-stu-id="080e9-111">CN</span></span>                | <span data-ttu-id="080e9-112">列印-裝訂-支援</span><span class="sxs-lookup"><span data-stu-id="080e9-112">Print-Stapling-Supported</span></span>             |
| <span data-ttu-id="080e9-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="080e9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="080e9-114">printStaplingSupported</span><span class="sxs-lookup"><span data-stu-id="080e9-114">printStaplingSupported</span></span>               |
| <span data-ttu-id="080e9-115">大小</span><span class="sxs-lookup"><span data-stu-id="080e9-115">Size</span></span>              | <span data-ttu-id="080e9-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="080e9-116">4 bytes</span></span>                              |
| <span data-ttu-id="080e9-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="080e9-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="080e9-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="080e9-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="080e9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="080e9-119">Attribute-Id</span></span>      | <span data-ttu-id="080e9-120">1.2.840.113556.1.4.281</span><span class="sxs-lookup"><span data-stu-id="080e9-120">1.2.840.113556.1.4.281</span></span>               |
| <span data-ttu-id="080e9-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="080e9-121">System-Id-Guid</span></span>    | <span data-ttu-id="080e9-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="080e9-122">ba305f73-47e3-11d0-a1a6-00c04fd930c9</span></span> |
| <span data-ttu-id="080e9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="080e9-123">Syntax</span></span>            | [<span data-ttu-id="080e9-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="080e9-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="080e9-125">實作</span><span class="sxs-lookup"><span data-stu-id="080e9-125">Implementations</span></span>

-   [<span data-ttu-id="080e9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="080e9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="080e9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="080e9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="080e9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="080e9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="080e9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="080e9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="080e9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="080e9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="080e9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="080e9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="080e9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="080e9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="080e9-133">進入</span><span class="sxs-lookup"><span data-stu-id="080e9-133">Entry</span></span> | <span data-ttu-id="080e9-134">值</span><span class="sxs-lookup"><span data-stu-id="080e9-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="080e9-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="080e9-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080e9-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="080e9-137">System-Only</span></span>            | <span data-ttu-id="080e9-138">否</span><span class="sxs-lookup"><span data-stu-id="080e9-138">False</span></span>                                          |
| <span data-ttu-id="080e9-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="080e9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="080e9-140">對</span><span class="sxs-lookup"><span data-stu-id="080e9-140">True</span></span>                                           |
| <span data-ttu-id="080e9-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="080e9-141">Is Indexed</span></span>             | <span data-ttu-id="080e9-142">否</span><span class="sxs-lookup"><span data-stu-id="080e9-142">False</span></span>                                          |
| <span data-ttu-id="080e9-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="080e9-143">In Global Catalog</span></span>      | <span data-ttu-id="080e9-144">對</span><span class="sxs-lookup"><span data-stu-id="080e9-144">True</span></span>                                           |
| <span data-ttu-id="080e9-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="080e9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="080e9-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="080e9-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="080e9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080e9-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="080e9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080e9-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="080e9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-149">Search-Flags</span></span>           | <span data-ttu-id="080e9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080e9-150">0x00000000</span></span>                                     |
| <span data-ttu-id="080e9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-151">System-Flags</span></span>           | <span data-ttu-id="080e9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080e9-152">0x00000010</span></span>                                     |
| <span data-ttu-id="080e9-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="080e9-153">Classes used in</span></span>        | [<span data-ttu-id="080e9-154">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="080e9-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="080e9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="080e9-155">Windows Server 2003</span></span>



| <span data-ttu-id="080e9-156">進入</span><span class="sxs-lookup"><span data-stu-id="080e9-156">Entry</span></span> | <span data-ttu-id="080e9-157">值</span><span class="sxs-lookup"><span data-stu-id="080e9-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="080e9-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="080e9-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080e9-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="080e9-160">System-Only</span></span>            | <span data-ttu-id="080e9-161">否</span><span class="sxs-lookup"><span data-stu-id="080e9-161">False</span></span>                                          |
| <span data-ttu-id="080e9-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="080e9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="080e9-163">對</span><span class="sxs-lookup"><span data-stu-id="080e9-163">True</span></span>                                           |
| <span data-ttu-id="080e9-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="080e9-164">Is Indexed</span></span>             | <span data-ttu-id="080e9-165">否</span><span class="sxs-lookup"><span data-stu-id="080e9-165">False</span></span>                                          |
| <span data-ttu-id="080e9-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="080e9-166">In Global Catalog</span></span>      | <span data-ttu-id="080e9-167">對</span><span class="sxs-lookup"><span data-stu-id="080e9-167">True</span></span>                                           |
| <span data-ttu-id="080e9-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="080e9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="080e9-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="080e9-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="080e9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080e9-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="080e9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080e9-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="080e9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-172">Search-Flags</span></span>           | <span data-ttu-id="080e9-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080e9-173">0x00000000</span></span>                                     |
| <span data-ttu-id="080e9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-174">System-Flags</span></span>           | <span data-ttu-id="080e9-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080e9-175">0x00000010</span></span>                                     |
| <span data-ttu-id="080e9-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="080e9-176">Classes used in</span></span>        | [<span data-ttu-id="080e9-177">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="080e9-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="080e9-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="080e9-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="080e9-179">進入</span><span class="sxs-lookup"><span data-stu-id="080e9-179">Entry</span></span> | <span data-ttu-id="080e9-180">值</span><span class="sxs-lookup"><span data-stu-id="080e9-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="080e9-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="080e9-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080e9-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="080e9-183">System-Only</span></span>            | <span data-ttu-id="080e9-184">否</span><span class="sxs-lookup"><span data-stu-id="080e9-184">False</span></span>                                          |
| <span data-ttu-id="080e9-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="080e9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="080e9-186">對</span><span class="sxs-lookup"><span data-stu-id="080e9-186">True</span></span>                                           |
| <span data-ttu-id="080e9-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="080e9-187">Is Indexed</span></span>             | <span data-ttu-id="080e9-188">否</span><span class="sxs-lookup"><span data-stu-id="080e9-188">False</span></span>                                          |
| <span data-ttu-id="080e9-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="080e9-189">In Global Catalog</span></span>      | <span data-ttu-id="080e9-190">對</span><span class="sxs-lookup"><span data-stu-id="080e9-190">True</span></span>                                           |
| <span data-ttu-id="080e9-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="080e9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="080e9-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="080e9-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="080e9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080e9-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="080e9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080e9-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="080e9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-195">Search-Flags</span></span>           | <span data-ttu-id="080e9-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080e9-196">0x00000000</span></span>                                     |
| <span data-ttu-id="080e9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-197">System-Flags</span></span>           | <span data-ttu-id="080e9-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080e9-198">0x00000010</span></span>                                     |
| <span data-ttu-id="080e9-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="080e9-199">Classes used in</span></span>        | [<span data-ttu-id="080e9-200">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="080e9-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="080e9-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="080e9-201">Windows Server 2008</span></span>



| <span data-ttu-id="080e9-202">進入</span><span class="sxs-lookup"><span data-stu-id="080e9-202">Entry</span></span> | <span data-ttu-id="080e9-203">值</span><span class="sxs-lookup"><span data-stu-id="080e9-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="080e9-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="080e9-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080e9-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="080e9-206">System-Only</span></span>            | <span data-ttu-id="080e9-207">否</span><span class="sxs-lookup"><span data-stu-id="080e9-207">False</span></span>                                          |
| <span data-ttu-id="080e9-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="080e9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="080e9-209">對</span><span class="sxs-lookup"><span data-stu-id="080e9-209">True</span></span>                                           |
| <span data-ttu-id="080e9-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="080e9-210">Is Indexed</span></span>             | <span data-ttu-id="080e9-211">否</span><span class="sxs-lookup"><span data-stu-id="080e9-211">False</span></span>                                          |
| <span data-ttu-id="080e9-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="080e9-212">In Global Catalog</span></span>      | <span data-ttu-id="080e9-213">對</span><span class="sxs-lookup"><span data-stu-id="080e9-213">True</span></span>                                           |
| <span data-ttu-id="080e9-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="080e9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="080e9-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="080e9-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="080e9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080e9-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="080e9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080e9-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="080e9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-218">Search-Flags</span></span>           | <span data-ttu-id="080e9-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080e9-219">0x00000000</span></span>                                     |
| <span data-ttu-id="080e9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-220">System-Flags</span></span>           | <span data-ttu-id="080e9-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080e9-221">0x00000010</span></span>                                     |
| <span data-ttu-id="080e9-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="080e9-222">Classes used in</span></span>        | [<span data-ttu-id="080e9-223">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="080e9-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="080e9-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="080e9-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="080e9-225">進入</span><span class="sxs-lookup"><span data-stu-id="080e9-225">Entry</span></span> | <span data-ttu-id="080e9-226">值</span><span class="sxs-lookup"><span data-stu-id="080e9-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="080e9-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="080e9-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080e9-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="080e9-229">System-Only</span></span>            | <span data-ttu-id="080e9-230">否</span><span class="sxs-lookup"><span data-stu-id="080e9-230">False</span></span>                                          |
| <span data-ttu-id="080e9-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="080e9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="080e9-232">對</span><span class="sxs-lookup"><span data-stu-id="080e9-232">True</span></span>                                           |
| <span data-ttu-id="080e9-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="080e9-233">Is Indexed</span></span>             | <span data-ttu-id="080e9-234">否</span><span class="sxs-lookup"><span data-stu-id="080e9-234">False</span></span>                                          |
| <span data-ttu-id="080e9-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="080e9-235">In Global Catalog</span></span>      | <span data-ttu-id="080e9-236">對</span><span class="sxs-lookup"><span data-stu-id="080e9-236">True</span></span>                                           |
| <span data-ttu-id="080e9-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="080e9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="080e9-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="080e9-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="080e9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080e9-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="080e9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080e9-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="080e9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-241">Search-Flags</span></span>           | <span data-ttu-id="080e9-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080e9-242">0x00000000</span></span>                                     |
| <span data-ttu-id="080e9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-243">System-Flags</span></span>           | <span data-ttu-id="080e9-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080e9-244">0x00000010</span></span>                                     |
| <span data-ttu-id="080e9-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="080e9-245">Classes used in</span></span>        | [<span data-ttu-id="080e9-246">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="080e9-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="080e9-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="080e9-247">Windows Server 2012</span></span>



| <span data-ttu-id="080e9-248">進入</span><span class="sxs-lookup"><span data-stu-id="080e9-248">Entry</span></span> | <span data-ttu-id="080e9-249">值</span><span class="sxs-lookup"><span data-stu-id="080e9-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="080e9-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="080e9-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080e9-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="080e9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="080e9-252">System-Only</span></span>            | <span data-ttu-id="080e9-253">否</span><span class="sxs-lookup"><span data-stu-id="080e9-253">False</span></span>                                          |
| <span data-ttu-id="080e9-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="080e9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="080e9-255">對</span><span class="sxs-lookup"><span data-stu-id="080e9-255">True</span></span>                                           |
| <span data-ttu-id="080e9-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="080e9-256">Is Indexed</span></span>             | <span data-ttu-id="080e9-257">否</span><span class="sxs-lookup"><span data-stu-id="080e9-257">False</span></span>                                          |
| <span data-ttu-id="080e9-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="080e9-258">In Global Catalog</span></span>      | <span data-ttu-id="080e9-259">對</span><span class="sxs-lookup"><span data-stu-id="080e9-259">True</span></span>                                           |
| <span data-ttu-id="080e9-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="080e9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="080e9-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="080e9-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="080e9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080e9-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="080e9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080e9-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="080e9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-264">Search-Flags</span></span>           | <span data-ttu-id="080e9-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080e9-265">0x00000000</span></span>                                     |
| <span data-ttu-id="080e9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080e9-266">System-Flags</span></span>           | <span data-ttu-id="080e9-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080e9-267">0x00000010</span></span>                                     |
| <span data-ttu-id="080e9-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="080e9-268">Classes used in</span></span>        | [<span data-ttu-id="080e9-269">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="080e9-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





