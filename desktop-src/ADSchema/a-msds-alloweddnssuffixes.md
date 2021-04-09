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
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="99bff-105">允許的 ms-DS-DNS 尾碼屬性</span><span class="sxs-lookup"><span data-stu-id="99bff-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="99bff-106">電腦物件中 dNSHostName 屬性允許的尾碼清單。</span><span class="sxs-lookup"><span data-stu-id="99bff-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="99bff-107">進入</span><span class="sxs-lookup"><span data-stu-id="99bff-107">Entry</span></span> | <span data-ttu-id="99bff-108">值</span><span class="sxs-lookup"><span data-stu-id="99bff-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="99bff-109">CN</span><span class="sxs-lookup"><span data-stu-id="99bff-109">CN</span></span>                | <span data-ttu-id="99bff-110">ms-DS-允許的 DNS 尾碼</span><span class="sxs-lookup"><span data-stu-id="99bff-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="99bff-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="99bff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="99bff-112">>msds-alloweddnssuffixes</span><span class="sxs-lookup"><span data-stu-id="99bff-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="99bff-113">大小</span><span class="sxs-lookup"><span data-stu-id="99bff-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="99bff-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="99bff-114">Update Privilege</span></span>  | <span data-ttu-id="99bff-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="99bff-115">Domain administrator</span></span>                        |
| <span data-ttu-id="99bff-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="99bff-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="99bff-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99bff-117">Attribute-Id</span></span>      | <span data-ttu-id="99bff-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="99bff-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="99bff-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="99bff-119">System-Id-Guid</span></span>    | <span data-ttu-id="99bff-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="99bff-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="99bff-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="99bff-121">Syntax</span></span>            | [<span data-ttu-id="99bff-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="99bff-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="99bff-123">實作</span><span class="sxs-lookup"><span data-stu-id="99bff-123">Implementations</span></span>

-   [<span data-ttu-id="99bff-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99bff-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99bff-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="99bff-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="99bff-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99bff-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99bff-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99bff-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99bff-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99bff-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99bff-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99bff-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="99bff-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99bff-130">Windows Server 2003</span></span>



| <span data-ttu-id="99bff-131">進入</span><span class="sxs-lookup"><span data-stu-id="99bff-131">Entry</span></span> | <span data-ttu-id="99bff-132">值</span><span class="sxs-lookup"><span data-stu-id="99bff-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99bff-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bff-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bff-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bff-135">System-Only</span></span>            | <span data-ttu-id="99bff-136">否</span><span class="sxs-lookup"><span data-stu-id="99bff-136">False</span></span>                                        |
| <span data-ttu-id="99bff-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bff-137">Is-Single-Valued</span></span>       | <span data-ttu-id="99bff-138">否</span><span class="sxs-lookup"><span data-stu-id="99bff-138">False</span></span>                                        |
| <span data-ttu-id="99bff-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bff-139">Is Indexed</span></span>             | <span data-ttu-id="99bff-140">否</span><span class="sxs-lookup"><span data-stu-id="99bff-140">False</span></span>                                        |
| <span data-ttu-id="99bff-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bff-141">In Global Catalog</span></span>      | <span data-ttu-id="99bff-142">否</span><span class="sxs-lookup"><span data-stu-id="99bff-142">False</span></span>                                        |
| <span data-ttu-id="99bff-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bff-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bff-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bff-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99bff-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bff-145">Range-Lower</span></span>            | <span data-ttu-id="99bff-146">0</span><span class="sxs-lookup"><span data-stu-id="99bff-146">0</span></span>                                            |
| <span data-ttu-id="99bff-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bff-147">Range-Upper</span></span>            | <span data-ttu-id="99bff-148">2048</span><span class="sxs-lookup"><span data-stu-id="99bff-148">2048</span></span>                                         |
| <span data-ttu-id="99bff-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-149">Search-Flags</span></span>           | <span data-ttu-id="99bff-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bff-150">0x00000000</span></span>                                   |
| <span data-ttu-id="99bff-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-151">System-Flags</span></span>           | <span data-ttu-id="99bff-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bff-152">0x00000010</span></span>                                   |
| <span data-ttu-id="99bff-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bff-153">Classes used in</span></span>        | [<span data-ttu-id="99bff-154">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="99bff-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="99bff-155">亞當</span><span class="sxs-lookup"><span data-stu-id="99bff-155">ADAM</span></span>



| <span data-ttu-id="99bff-156">進入</span><span class="sxs-lookup"><span data-stu-id="99bff-156">Entry</span></span> | <span data-ttu-id="99bff-157">值</span><span class="sxs-lookup"><span data-stu-id="99bff-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99bff-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bff-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bff-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bff-160">System-Only</span></span>            | <span data-ttu-id="99bff-161">否</span><span class="sxs-lookup"><span data-stu-id="99bff-161">False</span></span>                                        |
| <span data-ttu-id="99bff-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bff-162">Is-Single-Valued</span></span>       | <span data-ttu-id="99bff-163">否</span><span class="sxs-lookup"><span data-stu-id="99bff-163">False</span></span>                                        |
| <span data-ttu-id="99bff-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bff-164">Is Indexed</span></span>             | <span data-ttu-id="99bff-165">否</span><span class="sxs-lookup"><span data-stu-id="99bff-165">False</span></span>                                        |
| <span data-ttu-id="99bff-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bff-166">In Global Catalog</span></span>      | <span data-ttu-id="99bff-167">否</span><span class="sxs-lookup"><span data-stu-id="99bff-167">False</span></span>                                        |
| <span data-ttu-id="99bff-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bff-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bff-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bff-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99bff-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bff-170">Range-Lower</span></span>            | <span data-ttu-id="99bff-171">0</span><span class="sxs-lookup"><span data-stu-id="99bff-171">0</span></span>                                            |
| <span data-ttu-id="99bff-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bff-172">Range-Upper</span></span>            | <span data-ttu-id="99bff-173">2048</span><span class="sxs-lookup"><span data-stu-id="99bff-173">2048</span></span>                                         |
| <span data-ttu-id="99bff-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-174">Search-Flags</span></span>           | <span data-ttu-id="99bff-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bff-175">0x00000000</span></span>                                   |
| <span data-ttu-id="99bff-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-176">System-Flags</span></span>           | <span data-ttu-id="99bff-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bff-177">0x00000010</span></span>                                   |
| <span data-ttu-id="99bff-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bff-178">Classes used in</span></span>        | [<span data-ttu-id="99bff-179">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="99bff-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99bff-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99bff-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99bff-181">進入</span><span class="sxs-lookup"><span data-stu-id="99bff-181">Entry</span></span> | <span data-ttu-id="99bff-182">值</span><span class="sxs-lookup"><span data-stu-id="99bff-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99bff-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bff-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bff-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bff-185">System-Only</span></span>            | <span data-ttu-id="99bff-186">否</span><span class="sxs-lookup"><span data-stu-id="99bff-186">False</span></span>                                        |
| <span data-ttu-id="99bff-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bff-187">Is-Single-Valued</span></span>       | <span data-ttu-id="99bff-188">否</span><span class="sxs-lookup"><span data-stu-id="99bff-188">False</span></span>                                        |
| <span data-ttu-id="99bff-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bff-189">Is Indexed</span></span>             | <span data-ttu-id="99bff-190">否</span><span class="sxs-lookup"><span data-stu-id="99bff-190">False</span></span>                                        |
| <span data-ttu-id="99bff-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bff-191">In Global Catalog</span></span>      | <span data-ttu-id="99bff-192">否</span><span class="sxs-lookup"><span data-stu-id="99bff-192">False</span></span>                                        |
| <span data-ttu-id="99bff-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bff-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bff-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bff-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99bff-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bff-195">Range-Lower</span></span>            | <span data-ttu-id="99bff-196">0</span><span class="sxs-lookup"><span data-stu-id="99bff-196">0</span></span>                                            |
| <span data-ttu-id="99bff-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bff-197">Range-Upper</span></span>            | <span data-ttu-id="99bff-198">2048</span><span class="sxs-lookup"><span data-stu-id="99bff-198">2048</span></span>                                         |
| <span data-ttu-id="99bff-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-199">Search-Flags</span></span>           | <span data-ttu-id="99bff-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bff-200">0x00000000</span></span>                                   |
| <span data-ttu-id="99bff-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-201">System-Flags</span></span>           | <span data-ttu-id="99bff-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bff-202">0x00000010</span></span>                                   |
| <span data-ttu-id="99bff-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bff-203">Classes used in</span></span>        | [<span data-ttu-id="99bff-204">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="99bff-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99bff-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99bff-205">Windows Server 2008</span></span>



| <span data-ttu-id="99bff-206">進入</span><span class="sxs-lookup"><span data-stu-id="99bff-206">Entry</span></span> | <span data-ttu-id="99bff-207">值</span><span class="sxs-lookup"><span data-stu-id="99bff-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99bff-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bff-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bff-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bff-210">System-Only</span></span>            | <span data-ttu-id="99bff-211">否</span><span class="sxs-lookup"><span data-stu-id="99bff-211">False</span></span>                                        |
| <span data-ttu-id="99bff-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bff-212">Is-Single-Valued</span></span>       | <span data-ttu-id="99bff-213">否</span><span class="sxs-lookup"><span data-stu-id="99bff-213">False</span></span>                                        |
| <span data-ttu-id="99bff-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bff-214">Is Indexed</span></span>             | <span data-ttu-id="99bff-215">否</span><span class="sxs-lookup"><span data-stu-id="99bff-215">False</span></span>                                        |
| <span data-ttu-id="99bff-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bff-216">In Global Catalog</span></span>      | <span data-ttu-id="99bff-217">否</span><span class="sxs-lookup"><span data-stu-id="99bff-217">False</span></span>                                        |
| <span data-ttu-id="99bff-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bff-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bff-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bff-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99bff-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bff-220">Range-Lower</span></span>            | <span data-ttu-id="99bff-221">0</span><span class="sxs-lookup"><span data-stu-id="99bff-221">0</span></span>                                            |
| <span data-ttu-id="99bff-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bff-222">Range-Upper</span></span>            | <span data-ttu-id="99bff-223">2048</span><span class="sxs-lookup"><span data-stu-id="99bff-223">2048</span></span>                                         |
| <span data-ttu-id="99bff-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-224">Search-Flags</span></span>           | <span data-ttu-id="99bff-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bff-225">0x00000000</span></span>                                   |
| <span data-ttu-id="99bff-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-226">System-Flags</span></span>           | <span data-ttu-id="99bff-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bff-227">0x00000010</span></span>                                   |
| <span data-ttu-id="99bff-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bff-228">Classes used in</span></span>        | [<span data-ttu-id="99bff-229">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="99bff-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99bff-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99bff-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99bff-231">進入</span><span class="sxs-lookup"><span data-stu-id="99bff-231">Entry</span></span> | <span data-ttu-id="99bff-232">值</span><span class="sxs-lookup"><span data-stu-id="99bff-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99bff-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bff-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bff-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bff-235">System-Only</span></span>            | <span data-ttu-id="99bff-236">否</span><span class="sxs-lookup"><span data-stu-id="99bff-236">False</span></span>                                        |
| <span data-ttu-id="99bff-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bff-237">Is-Single-Valued</span></span>       | <span data-ttu-id="99bff-238">否</span><span class="sxs-lookup"><span data-stu-id="99bff-238">False</span></span>                                        |
| <span data-ttu-id="99bff-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bff-239">Is Indexed</span></span>             | <span data-ttu-id="99bff-240">否</span><span class="sxs-lookup"><span data-stu-id="99bff-240">False</span></span>                                        |
| <span data-ttu-id="99bff-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bff-241">In Global Catalog</span></span>      | <span data-ttu-id="99bff-242">否</span><span class="sxs-lookup"><span data-stu-id="99bff-242">False</span></span>                                        |
| <span data-ttu-id="99bff-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bff-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bff-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bff-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99bff-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bff-245">Range-Lower</span></span>            | <span data-ttu-id="99bff-246">0</span><span class="sxs-lookup"><span data-stu-id="99bff-246">0</span></span>                                            |
| <span data-ttu-id="99bff-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bff-247">Range-Upper</span></span>            | <span data-ttu-id="99bff-248">2048</span><span class="sxs-lookup"><span data-stu-id="99bff-248">2048</span></span>                                         |
| <span data-ttu-id="99bff-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-249">Search-Flags</span></span>           | <span data-ttu-id="99bff-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bff-250">0x00000000</span></span>                                   |
| <span data-ttu-id="99bff-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-251">System-Flags</span></span>           | <span data-ttu-id="99bff-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bff-252">0x00000010</span></span>                                   |
| <span data-ttu-id="99bff-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bff-253">Classes used in</span></span>        | [<span data-ttu-id="99bff-254">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="99bff-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99bff-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99bff-255">Windows Server 2012</span></span>



| <span data-ttu-id="99bff-256">進入</span><span class="sxs-lookup"><span data-stu-id="99bff-256">Entry</span></span> | <span data-ttu-id="99bff-257">值</span><span class="sxs-lookup"><span data-stu-id="99bff-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="99bff-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99bff-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99bff-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="99bff-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="99bff-260">System-Only</span></span>            | <span data-ttu-id="99bff-261">否</span><span class="sxs-lookup"><span data-stu-id="99bff-261">False</span></span>                                        |
| <span data-ttu-id="99bff-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99bff-262">Is-Single-Valued</span></span>       | <span data-ttu-id="99bff-263">否</span><span class="sxs-lookup"><span data-stu-id="99bff-263">False</span></span>                                        |
| <span data-ttu-id="99bff-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99bff-264">Is Indexed</span></span>             | <span data-ttu-id="99bff-265">否</span><span class="sxs-lookup"><span data-stu-id="99bff-265">False</span></span>                                        |
| <span data-ttu-id="99bff-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99bff-266">In Global Catalog</span></span>      | <span data-ttu-id="99bff-267">否</span><span class="sxs-lookup"><span data-stu-id="99bff-267">False</span></span>                                        |
| <span data-ttu-id="99bff-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99bff-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="99bff-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99bff-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="99bff-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99bff-270">Range-Lower</span></span>            | <span data-ttu-id="99bff-271">0</span><span class="sxs-lookup"><span data-stu-id="99bff-271">0</span></span>                                            |
| <span data-ttu-id="99bff-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99bff-272">Range-Upper</span></span>            | <span data-ttu-id="99bff-273">2048</span><span class="sxs-lookup"><span data-stu-id="99bff-273">2048</span></span>                                         |
| <span data-ttu-id="99bff-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-274">Search-Flags</span></span>           | <span data-ttu-id="99bff-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99bff-275">0x00000000</span></span>                                   |
| <span data-ttu-id="99bff-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99bff-276">System-Flags</span></span>           | <span data-ttu-id="99bff-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99bff-277">0x00000010</span></span>                                   |
| <span data-ttu-id="99bff-278">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99bff-278">Classes used in</span></span>        | [<span data-ttu-id="99bff-279">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="99bff-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





