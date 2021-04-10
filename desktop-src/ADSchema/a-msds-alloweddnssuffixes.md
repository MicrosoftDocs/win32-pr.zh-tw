---
title: 允許的 ms-DS-DNS 尾碼屬性
description: 電腦物件中 dNSHostName 屬性允許的尾碼清單。
ms.assetid: acd57af8-a021-4704-8a56-304126cd3d4b
ms.tgt_platform: multiple
keywords:
- ms-DS-允許的 DNS 尾碼屬性 AD 架構
- '>msds-alloweddnssuffixes 屬性 AD 架構'
topic_type:
- apiref
api_name:
- ms-DS-Allowed-DNS-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46c3e4848f96c68041bfdc5f3f1cc9533b52d3e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687051"
---
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="e00ae-105">允許的 ms-DS-DNS 尾碼屬性</span><span class="sxs-lookup"><span data-stu-id="e00ae-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="e00ae-106">電腦物件中 dNSHostName 屬性允許的尾碼清單。</span><span class="sxs-lookup"><span data-stu-id="e00ae-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="e00ae-107">進入</span><span class="sxs-lookup"><span data-stu-id="e00ae-107">Entry</span></span> | <span data-ttu-id="e00ae-108">值</span><span class="sxs-lookup"><span data-stu-id="e00ae-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e00ae-109">CN</span><span class="sxs-lookup"><span data-stu-id="e00ae-109">CN</span></span>                | <span data-ttu-id="e00ae-110">ms-DS-允許的 DNS 尾碼</span><span class="sxs-lookup"><span data-stu-id="e00ae-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="e00ae-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e00ae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e00ae-112">>msds-alloweddnssuffixes</span><span class="sxs-lookup"><span data-stu-id="e00ae-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="e00ae-113">大小</span><span class="sxs-lookup"><span data-stu-id="e00ae-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e00ae-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e00ae-114">Update Privilege</span></span>  | <span data-ttu-id="e00ae-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="e00ae-115">Domain administrator</span></span>                        |
| <span data-ttu-id="e00ae-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e00ae-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e00ae-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e00ae-117">Attribute-Id</span></span>      | <span data-ttu-id="e00ae-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="e00ae-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="e00ae-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e00ae-119">System-Id-Guid</span></span>    | <span data-ttu-id="e00ae-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="e00ae-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="e00ae-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e00ae-121">Syntax</span></span>            | [<span data-ttu-id="e00ae-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e00ae-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e00ae-123">實作</span><span class="sxs-lookup"><span data-stu-id="e00ae-123">Implementations</span></span>

-   [<span data-ttu-id="e00ae-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e00ae-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e00ae-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e00ae-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e00ae-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e00ae-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e00ae-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e00ae-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e00ae-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e00ae-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e00ae-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e00ae-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e00ae-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e00ae-130">Windows Server 2003</span></span>



| <span data-ttu-id="e00ae-131">進入</span><span class="sxs-lookup"><span data-stu-id="e00ae-131">Entry</span></span> | <span data-ttu-id="e00ae-132">值</span><span class="sxs-lookup"><span data-stu-id="e00ae-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e00ae-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e00ae-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e00ae-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e00ae-135">System-Only</span></span>            | <span data-ttu-id="e00ae-136">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-136">False</span></span>                                        |
| <span data-ttu-id="e00ae-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e00ae-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e00ae-138">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-138">False</span></span>                                        |
| <span data-ttu-id="e00ae-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e00ae-139">Is Indexed</span></span>             | <span data-ttu-id="e00ae-140">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-140">False</span></span>                                        |
| <span data-ttu-id="e00ae-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e00ae-141">In Global Catalog</span></span>      | <span data-ttu-id="e00ae-142">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-142">False</span></span>                                        |
| <span data-ttu-id="e00ae-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e00ae-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e00ae-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e00ae-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e00ae-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e00ae-145">Range-Lower</span></span>            | <span data-ttu-id="e00ae-146">0</span><span class="sxs-lookup"><span data-stu-id="e00ae-146">0</span></span>                                            |
| <span data-ttu-id="e00ae-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e00ae-147">Range-Upper</span></span>            | <span data-ttu-id="e00ae-148">2048</span><span class="sxs-lookup"><span data-stu-id="e00ae-148">2048</span></span>                                         |
| <span data-ttu-id="e00ae-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-149">Search-Flags</span></span>           | <span data-ttu-id="e00ae-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e00ae-150">0x00000000</span></span>                                   |
| <span data-ttu-id="e00ae-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-151">System-Flags</span></span>           | <span data-ttu-id="e00ae-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e00ae-152">0x00000010</span></span>                                   |
| <span data-ttu-id="e00ae-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e00ae-153">Classes used in</span></span>        | [<span data-ttu-id="e00ae-154">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="e00ae-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e00ae-155">亞當</span><span class="sxs-lookup"><span data-stu-id="e00ae-155">ADAM</span></span>



| <span data-ttu-id="e00ae-156">進入</span><span class="sxs-lookup"><span data-stu-id="e00ae-156">Entry</span></span> | <span data-ttu-id="e00ae-157">值</span><span class="sxs-lookup"><span data-stu-id="e00ae-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e00ae-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e00ae-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e00ae-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e00ae-160">System-Only</span></span>            | <span data-ttu-id="e00ae-161">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-161">False</span></span>                                        |
| <span data-ttu-id="e00ae-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e00ae-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e00ae-163">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-163">False</span></span>                                        |
| <span data-ttu-id="e00ae-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e00ae-164">Is Indexed</span></span>             | <span data-ttu-id="e00ae-165">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-165">False</span></span>                                        |
| <span data-ttu-id="e00ae-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e00ae-166">In Global Catalog</span></span>      | <span data-ttu-id="e00ae-167">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-167">False</span></span>                                        |
| <span data-ttu-id="e00ae-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e00ae-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e00ae-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e00ae-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e00ae-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e00ae-170">Range-Lower</span></span>            | <span data-ttu-id="e00ae-171">0</span><span class="sxs-lookup"><span data-stu-id="e00ae-171">0</span></span>                                            |
| <span data-ttu-id="e00ae-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e00ae-172">Range-Upper</span></span>            | <span data-ttu-id="e00ae-173">2048</span><span class="sxs-lookup"><span data-stu-id="e00ae-173">2048</span></span>                                         |
| <span data-ttu-id="e00ae-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-174">Search-Flags</span></span>           | <span data-ttu-id="e00ae-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e00ae-175">0x00000000</span></span>                                   |
| <span data-ttu-id="e00ae-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-176">System-Flags</span></span>           | <span data-ttu-id="e00ae-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e00ae-177">0x00000010</span></span>                                   |
| <span data-ttu-id="e00ae-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e00ae-178">Classes used in</span></span>        | [<span data-ttu-id="e00ae-179">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="e00ae-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e00ae-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e00ae-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e00ae-181">進入</span><span class="sxs-lookup"><span data-stu-id="e00ae-181">Entry</span></span> | <span data-ttu-id="e00ae-182">值</span><span class="sxs-lookup"><span data-stu-id="e00ae-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e00ae-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e00ae-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e00ae-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e00ae-185">System-Only</span></span>            | <span data-ttu-id="e00ae-186">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-186">False</span></span>                                        |
| <span data-ttu-id="e00ae-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e00ae-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e00ae-188">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-188">False</span></span>                                        |
| <span data-ttu-id="e00ae-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e00ae-189">Is Indexed</span></span>             | <span data-ttu-id="e00ae-190">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-190">False</span></span>                                        |
| <span data-ttu-id="e00ae-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e00ae-191">In Global Catalog</span></span>      | <span data-ttu-id="e00ae-192">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-192">False</span></span>                                        |
| <span data-ttu-id="e00ae-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e00ae-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e00ae-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e00ae-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e00ae-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e00ae-195">Range-Lower</span></span>            | <span data-ttu-id="e00ae-196">0</span><span class="sxs-lookup"><span data-stu-id="e00ae-196">0</span></span>                                            |
| <span data-ttu-id="e00ae-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e00ae-197">Range-Upper</span></span>            | <span data-ttu-id="e00ae-198">2048</span><span class="sxs-lookup"><span data-stu-id="e00ae-198">2048</span></span>                                         |
| <span data-ttu-id="e00ae-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-199">Search-Flags</span></span>           | <span data-ttu-id="e00ae-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e00ae-200">0x00000000</span></span>                                   |
| <span data-ttu-id="e00ae-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-201">System-Flags</span></span>           | <span data-ttu-id="e00ae-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e00ae-202">0x00000010</span></span>                                   |
| <span data-ttu-id="e00ae-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e00ae-203">Classes used in</span></span>        | [<span data-ttu-id="e00ae-204">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="e00ae-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e00ae-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e00ae-205">Windows Server 2008</span></span>



| <span data-ttu-id="e00ae-206">進入</span><span class="sxs-lookup"><span data-stu-id="e00ae-206">Entry</span></span> | <span data-ttu-id="e00ae-207">值</span><span class="sxs-lookup"><span data-stu-id="e00ae-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e00ae-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e00ae-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e00ae-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="e00ae-210">System-Only</span></span>            | <span data-ttu-id="e00ae-211">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-211">False</span></span>                                        |
| <span data-ttu-id="e00ae-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e00ae-212">Is-Single-Valued</span></span>       | <span data-ttu-id="e00ae-213">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-213">False</span></span>                                        |
| <span data-ttu-id="e00ae-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e00ae-214">Is Indexed</span></span>             | <span data-ttu-id="e00ae-215">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-215">False</span></span>                                        |
| <span data-ttu-id="e00ae-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e00ae-216">In Global Catalog</span></span>      | <span data-ttu-id="e00ae-217">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-217">False</span></span>                                        |
| <span data-ttu-id="e00ae-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e00ae-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="e00ae-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e00ae-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e00ae-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e00ae-220">Range-Lower</span></span>            | <span data-ttu-id="e00ae-221">0</span><span class="sxs-lookup"><span data-stu-id="e00ae-221">0</span></span>                                            |
| <span data-ttu-id="e00ae-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e00ae-222">Range-Upper</span></span>            | <span data-ttu-id="e00ae-223">2048</span><span class="sxs-lookup"><span data-stu-id="e00ae-223">2048</span></span>                                         |
| <span data-ttu-id="e00ae-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-224">Search-Flags</span></span>           | <span data-ttu-id="e00ae-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e00ae-225">0x00000000</span></span>                                   |
| <span data-ttu-id="e00ae-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-226">System-Flags</span></span>           | <span data-ttu-id="e00ae-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e00ae-227">0x00000010</span></span>                                   |
| <span data-ttu-id="e00ae-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e00ae-228">Classes used in</span></span>        | [<span data-ttu-id="e00ae-229">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="e00ae-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e00ae-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e00ae-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e00ae-231">進入</span><span class="sxs-lookup"><span data-stu-id="e00ae-231">Entry</span></span> | <span data-ttu-id="e00ae-232">值</span><span class="sxs-lookup"><span data-stu-id="e00ae-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e00ae-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e00ae-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e00ae-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="e00ae-235">System-Only</span></span>            | <span data-ttu-id="e00ae-236">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-236">False</span></span>                                        |
| <span data-ttu-id="e00ae-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e00ae-237">Is-Single-Valued</span></span>       | <span data-ttu-id="e00ae-238">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-238">False</span></span>                                        |
| <span data-ttu-id="e00ae-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e00ae-239">Is Indexed</span></span>             | <span data-ttu-id="e00ae-240">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-240">False</span></span>                                        |
| <span data-ttu-id="e00ae-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e00ae-241">In Global Catalog</span></span>      | <span data-ttu-id="e00ae-242">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-242">False</span></span>                                        |
| <span data-ttu-id="e00ae-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e00ae-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="e00ae-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e00ae-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e00ae-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e00ae-245">Range-Lower</span></span>            | <span data-ttu-id="e00ae-246">0</span><span class="sxs-lookup"><span data-stu-id="e00ae-246">0</span></span>                                            |
| <span data-ttu-id="e00ae-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e00ae-247">Range-Upper</span></span>            | <span data-ttu-id="e00ae-248">2048</span><span class="sxs-lookup"><span data-stu-id="e00ae-248">2048</span></span>                                         |
| <span data-ttu-id="e00ae-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-249">Search-Flags</span></span>           | <span data-ttu-id="e00ae-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e00ae-250">0x00000000</span></span>                                   |
| <span data-ttu-id="e00ae-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-251">System-Flags</span></span>           | <span data-ttu-id="e00ae-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e00ae-252">0x00000010</span></span>                                   |
| <span data-ttu-id="e00ae-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e00ae-253">Classes used in</span></span>        | [<span data-ttu-id="e00ae-254">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="e00ae-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e00ae-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e00ae-255">Windows Server 2012</span></span>



| <span data-ttu-id="e00ae-256">進入</span><span class="sxs-lookup"><span data-stu-id="e00ae-256">Entry</span></span> | <span data-ttu-id="e00ae-257">值</span><span class="sxs-lookup"><span data-stu-id="e00ae-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e00ae-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e00ae-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e00ae-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e00ae-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="e00ae-260">System-Only</span></span>            | <span data-ttu-id="e00ae-261">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-261">False</span></span>                                        |
| <span data-ttu-id="e00ae-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e00ae-262">Is-Single-Valued</span></span>       | <span data-ttu-id="e00ae-263">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-263">False</span></span>                                        |
| <span data-ttu-id="e00ae-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e00ae-264">Is Indexed</span></span>             | <span data-ttu-id="e00ae-265">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-265">False</span></span>                                        |
| <span data-ttu-id="e00ae-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e00ae-266">In Global Catalog</span></span>      | <span data-ttu-id="e00ae-267">否</span><span class="sxs-lookup"><span data-stu-id="e00ae-267">False</span></span>                                        |
| <span data-ttu-id="e00ae-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e00ae-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="e00ae-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e00ae-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e00ae-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e00ae-270">Range-Lower</span></span>            | <span data-ttu-id="e00ae-271">0</span><span class="sxs-lookup"><span data-stu-id="e00ae-271">0</span></span>                                            |
| <span data-ttu-id="e00ae-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e00ae-272">Range-Upper</span></span>            | <span data-ttu-id="e00ae-273">2048</span><span class="sxs-lookup"><span data-stu-id="e00ae-273">2048</span></span>                                         |
| <span data-ttu-id="e00ae-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-274">Search-Flags</span></span>           | <span data-ttu-id="e00ae-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e00ae-275">0x00000000</span></span>                                   |
| <span data-ttu-id="e00ae-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e00ae-276">System-Flags</span></span>           | <span data-ttu-id="e00ae-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e00ae-277">0x00000010</span></span>                                   |
| <span data-ttu-id="e00ae-278">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e00ae-278">Classes used in</span></span>        | [<span data-ttu-id="e00ae-279">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="e00ae-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





