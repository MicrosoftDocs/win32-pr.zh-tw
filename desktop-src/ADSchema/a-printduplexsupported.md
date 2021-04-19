---
title: 列印-雙工支援的屬性
description: 指出印表機所擁有的雙工支援類型。
ms.assetid: c7d3e3f1-d6a1-41b7-a54d-c932a00b2a68
ms.tgt_platform: multiple
keywords:
- 列印-雙工支援的屬性 AD 架構
- printDuplexSupported 屬性 AD 架構
topic_type:
- apiref
api_name:
- Print-Duplex-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027b5af8d2c2bc8ece810a00c17060608b7824c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970856"
---
# <a name="print-duplex-supported-attribute"></a><span data-ttu-id="36bca-105">列印-雙工支援的屬性</span><span class="sxs-lookup"><span data-stu-id="36bca-105">Print-Duplex-Supported attribute</span></span>

<span data-ttu-id="36bca-106">指出印表機所擁有的雙工支援類型。</span><span class="sxs-lookup"><span data-stu-id="36bca-106">Indicates the type of duplex support a printer has.</span></span>



| <span data-ttu-id="36bca-107">進入</span><span class="sxs-lookup"><span data-stu-id="36bca-107">Entry</span></span> | <span data-ttu-id="36bca-108">值</span><span class="sxs-lookup"><span data-stu-id="36bca-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="36bca-109">CN</span><span class="sxs-lookup"><span data-stu-id="36bca-109">CN</span></span>                | <span data-ttu-id="36bca-110">列印-雙工-支援</span><span class="sxs-lookup"><span data-stu-id="36bca-110">Print-Duplex-Supported</span></span>                                |
| <span data-ttu-id="36bca-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="36bca-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36bca-112">printDuplexSupported</span><span class="sxs-lookup"><span data-stu-id="36bca-112">printDuplexSupported</span></span>                                  |
| <span data-ttu-id="36bca-113">大小</span><span class="sxs-lookup"><span data-stu-id="36bca-113">Size</span></span>              | <span data-ttu-id="36bca-114">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="36bca-114">4 bytes.</span></span> <span data-ttu-id="36bca-115">雙工支援 = 2。</span><span class="sxs-lookup"><span data-stu-id="36bca-115">Duplex supported = 2.</span></span> <span data-ttu-id="36bca-116">單工 = 1 或0。</span><span class="sxs-lookup"><span data-stu-id="36bca-116">Simplex only = 1 or 0.</span></span> |
| <span data-ttu-id="36bca-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="36bca-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="36bca-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="36bca-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="36bca-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36bca-119">Attribute-Id</span></span>      | <span data-ttu-id="36bca-120">1.2.840.113556.1.4.1311</span><span class="sxs-lookup"><span data-stu-id="36bca-120">1.2.840.113556.1.4.1311</span></span>                               |
| <span data-ttu-id="36bca-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="36bca-121">System-Id-Guid</span></span>    | <span data-ttu-id="36bca-122">281416cc-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="36bca-122">281416cc-1968-11d0-a28f-00aa003049e2</span></span>                  |
| <span data-ttu-id="36bca-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="36bca-123">Syntax</span></span>            | [<span data-ttu-id="36bca-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="36bca-124">**Boolean**</span></span>](s-boolean.md)                          |



## <a name="implementations"></a><span data-ttu-id="36bca-125">實作</span><span class="sxs-lookup"><span data-stu-id="36bca-125">Implementations</span></span>

-   [<span data-ttu-id="36bca-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="36bca-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="36bca-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36bca-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36bca-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36bca-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36bca-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36bca-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36bca-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36bca-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36bca-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36bca-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="36bca-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36bca-132">Windows 2000 Server</span></span>



| <span data-ttu-id="36bca-133">進入</span><span class="sxs-lookup"><span data-stu-id="36bca-133">Entry</span></span> | <span data-ttu-id="36bca-134">值</span><span class="sxs-lookup"><span data-stu-id="36bca-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="36bca-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="36bca-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36bca-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="36bca-137">System-Only</span></span>            | <span data-ttu-id="36bca-138">否</span><span class="sxs-lookup"><span data-stu-id="36bca-138">False</span></span>                                          |
| <span data-ttu-id="36bca-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="36bca-139">Is-Single-Valued</span></span>       | <span data-ttu-id="36bca-140">對</span><span class="sxs-lookup"><span data-stu-id="36bca-140">True</span></span>                                           |
| <span data-ttu-id="36bca-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="36bca-141">Is Indexed</span></span>             | <span data-ttu-id="36bca-142">否</span><span class="sxs-lookup"><span data-stu-id="36bca-142">False</span></span>                                          |
| <span data-ttu-id="36bca-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="36bca-143">In Global Catalog</span></span>      | <span data-ttu-id="36bca-144">對</span><span class="sxs-lookup"><span data-stu-id="36bca-144">True</span></span>                                           |
| <span data-ttu-id="36bca-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="36bca-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="36bca-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="36bca-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="36bca-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36bca-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="36bca-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36bca-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="36bca-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-149">Search-Flags</span></span>           | <span data-ttu-id="36bca-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36bca-150">0x00000000</span></span>                                     |
| <span data-ttu-id="36bca-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-151">System-Flags</span></span>           | <span data-ttu-id="36bca-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36bca-152">0x00000010</span></span>                                     |
| <span data-ttu-id="36bca-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="36bca-153">Classes used in</span></span>        | [<span data-ttu-id="36bca-154">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="36bca-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="36bca-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36bca-155">Windows Server 2003</span></span>



| <span data-ttu-id="36bca-156">進入</span><span class="sxs-lookup"><span data-stu-id="36bca-156">Entry</span></span> | <span data-ttu-id="36bca-157">值</span><span class="sxs-lookup"><span data-stu-id="36bca-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="36bca-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="36bca-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36bca-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="36bca-160">System-Only</span></span>            | <span data-ttu-id="36bca-161">否</span><span class="sxs-lookup"><span data-stu-id="36bca-161">False</span></span>                                          |
| <span data-ttu-id="36bca-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="36bca-162">Is-Single-Valued</span></span>       | <span data-ttu-id="36bca-163">對</span><span class="sxs-lookup"><span data-stu-id="36bca-163">True</span></span>                                           |
| <span data-ttu-id="36bca-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="36bca-164">Is Indexed</span></span>             | <span data-ttu-id="36bca-165">否</span><span class="sxs-lookup"><span data-stu-id="36bca-165">False</span></span>                                          |
| <span data-ttu-id="36bca-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="36bca-166">In Global Catalog</span></span>      | <span data-ttu-id="36bca-167">對</span><span class="sxs-lookup"><span data-stu-id="36bca-167">True</span></span>                                           |
| <span data-ttu-id="36bca-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="36bca-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="36bca-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="36bca-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="36bca-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36bca-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="36bca-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36bca-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="36bca-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-172">Search-Flags</span></span>           | <span data-ttu-id="36bca-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36bca-173">0x00000000</span></span>                                     |
| <span data-ttu-id="36bca-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-174">System-Flags</span></span>           | <span data-ttu-id="36bca-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36bca-175">0x00000010</span></span>                                     |
| <span data-ttu-id="36bca-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="36bca-176">Classes used in</span></span>        | [<span data-ttu-id="36bca-177">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="36bca-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36bca-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36bca-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36bca-179">進入</span><span class="sxs-lookup"><span data-stu-id="36bca-179">Entry</span></span> | <span data-ttu-id="36bca-180">值</span><span class="sxs-lookup"><span data-stu-id="36bca-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="36bca-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="36bca-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36bca-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="36bca-183">System-Only</span></span>            | <span data-ttu-id="36bca-184">否</span><span class="sxs-lookup"><span data-stu-id="36bca-184">False</span></span>                                          |
| <span data-ttu-id="36bca-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="36bca-185">Is-Single-Valued</span></span>       | <span data-ttu-id="36bca-186">對</span><span class="sxs-lookup"><span data-stu-id="36bca-186">True</span></span>                                           |
| <span data-ttu-id="36bca-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="36bca-187">Is Indexed</span></span>             | <span data-ttu-id="36bca-188">否</span><span class="sxs-lookup"><span data-stu-id="36bca-188">False</span></span>                                          |
| <span data-ttu-id="36bca-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="36bca-189">In Global Catalog</span></span>      | <span data-ttu-id="36bca-190">對</span><span class="sxs-lookup"><span data-stu-id="36bca-190">True</span></span>                                           |
| <span data-ttu-id="36bca-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="36bca-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="36bca-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="36bca-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="36bca-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36bca-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="36bca-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36bca-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="36bca-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-195">Search-Flags</span></span>           | <span data-ttu-id="36bca-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36bca-196">0x00000000</span></span>                                     |
| <span data-ttu-id="36bca-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-197">System-Flags</span></span>           | <span data-ttu-id="36bca-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36bca-198">0x00000010</span></span>                                     |
| <span data-ttu-id="36bca-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="36bca-199">Classes used in</span></span>        | [<span data-ttu-id="36bca-200">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="36bca-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36bca-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36bca-201">Windows Server 2008</span></span>



| <span data-ttu-id="36bca-202">進入</span><span class="sxs-lookup"><span data-stu-id="36bca-202">Entry</span></span> | <span data-ttu-id="36bca-203">值</span><span class="sxs-lookup"><span data-stu-id="36bca-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="36bca-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="36bca-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36bca-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="36bca-206">System-Only</span></span>            | <span data-ttu-id="36bca-207">否</span><span class="sxs-lookup"><span data-stu-id="36bca-207">False</span></span>                                          |
| <span data-ttu-id="36bca-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="36bca-208">Is-Single-Valued</span></span>       | <span data-ttu-id="36bca-209">對</span><span class="sxs-lookup"><span data-stu-id="36bca-209">True</span></span>                                           |
| <span data-ttu-id="36bca-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="36bca-210">Is Indexed</span></span>             | <span data-ttu-id="36bca-211">否</span><span class="sxs-lookup"><span data-stu-id="36bca-211">False</span></span>                                          |
| <span data-ttu-id="36bca-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="36bca-212">In Global Catalog</span></span>      | <span data-ttu-id="36bca-213">對</span><span class="sxs-lookup"><span data-stu-id="36bca-213">True</span></span>                                           |
| <span data-ttu-id="36bca-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="36bca-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="36bca-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="36bca-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="36bca-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36bca-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="36bca-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36bca-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="36bca-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-218">Search-Flags</span></span>           | <span data-ttu-id="36bca-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36bca-219">0x00000000</span></span>                                     |
| <span data-ttu-id="36bca-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-220">System-Flags</span></span>           | <span data-ttu-id="36bca-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36bca-221">0x00000010</span></span>                                     |
| <span data-ttu-id="36bca-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="36bca-222">Classes used in</span></span>        | [<span data-ttu-id="36bca-223">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="36bca-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36bca-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36bca-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36bca-225">進入</span><span class="sxs-lookup"><span data-stu-id="36bca-225">Entry</span></span> | <span data-ttu-id="36bca-226">值</span><span class="sxs-lookup"><span data-stu-id="36bca-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="36bca-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="36bca-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36bca-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="36bca-229">System-Only</span></span>            | <span data-ttu-id="36bca-230">否</span><span class="sxs-lookup"><span data-stu-id="36bca-230">False</span></span>                                          |
| <span data-ttu-id="36bca-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="36bca-231">Is-Single-Valued</span></span>       | <span data-ttu-id="36bca-232">對</span><span class="sxs-lookup"><span data-stu-id="36bca-232">True</span></span>                                           |
| <span data-ttu-id="36bca-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="36bca-233">Is Indexed</span></span>             | <span data-ttu-id="36bca-234">否</span><span class="sxs-lookup"><span data-stu-id="36bca-234">False</span></span>                                          |
| <span data-ttu-id="36bca-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="36bca-235">In Global Catalog</span></span>      | <span data-ttu-id="36bca-236">對</span><span class="sxs-lookup"><span data-stu-id="36bca-236">True</span></span>                                           |
| <span data-ttu-id="36bca-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="36bca-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="36bca-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="36bca-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="36bca-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36bca-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="36bca-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36bca-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="36bca-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-241">Search-Flags</span></span>           | <span data-ttu-id="36bca-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36bca-242">0x00000000</span></span>                                     |
| <span data-ttu-id="36bca-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-243">System-Flags</span></span>           | <span data-ttu-id="36bca-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36bca-244">0x00000010</span></span>                                     |
| <span data-ttu-id="36bca-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="36bca-245">Classes used in</span></span>        | [<span data-ttu-id="36bca-246">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="36bca-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36bca-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36bca-247">Windows Server 2012</span></span>



| <span data-ttu-id="36bca-248">進入</span><span class="sxs-lookup"><span data-stu-id="36bca-248">Entry</span></span> | <span data-ttu-id="36bca-249">值</span><span class="sxs-lookup"><span data-stu-id="36bca-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="36bca-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="36bca-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36bca-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="36bca-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="36bca-252">System-Only</span></span>            | <span data-ttu-id="36bca-253">否</span><span class="sxs-lookup"><span data-stu-id="36bca-253">False</span></span>                                          |
| <span data-ttu-id="36bca-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="36bca-254">Is-Single-Valued</span></span>       | <span data-ttu-id="36bca-255">對</span><span class="sxs-lookup"><span data-stu-id="36bca-255">True</span></span>                                           |
| <span data-ttu-id="36bca-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="36bca-256">Is Indexed</span></span>             | <span data-ttu-id="36bca-257">否</span><span class="sxs-lookup"><span data-stu-id="36bca-257">False</span></span>                                          |
| <span data-ttu-id="36bca-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="36bca-258">In Global Catalog</span></span>      | <span data-ttu-id="36bca-259">對</span><span class="sxs-lookup"><span data-stu-id="36bca-259">True</span></span>                                           |
| <span data-ttu-id="36bca-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="36bca-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="36bca-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="36bca-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="36bca-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36bca-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="36bca-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36bca-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="36bca-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-264">Search-Flags</span></span>           | <span data-ttu-id="36bca-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36bca-265">0x00000000</span></span>                                     |
| <span data-ttu-id="36bca-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36bca-266">System-Flags</span></span>           | <span data-ttu-id="36bca-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36bca-267">0x00000010</span></span>                                     |
| <span data-ttu-id="36bca-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="36bca-268">Classes used in</span></span>        | [<span data-ttu-id="36bca-269">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="36bca-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





