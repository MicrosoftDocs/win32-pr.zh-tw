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
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="8b207-105">允許的 ms-DS-DNS 尾碼屬性</span><span class="sxs-lookup"><span data-stu-id="8b207-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="8b207-106">電腦物件中 dNSHostName 屬性允許的尾碼清單。</span><span class="sxs-lookup"><span data-stu-id="8b207-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="8b207-107">進入</span><span class="sxs-lookup"><span data-stu-id="8b207-107">Entry</span></span> | <span data-ttu-id="8b207-108">值</span><span class="sxs-lookup"><span data-stu-id="8b207-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8b207-109">CN</span><span class="sxs-lookup"><span data-stu-id="8b207-109">CN</span></span>                | <span data-ttu-id="8b207-110">ms-DS-允許的 DNS 尾碼</span><span class="sxs-lookup"><span data-stu-id="8b207-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="8b207-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8b207-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8b207-112">>msds-alloweddnssuffixes</span><span class="sxs-lookup"><span data-stu-id="8b207-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="8b207-113">大小</span><span class="sxs-lookup"><span data-stu-id="8b207-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8b207-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8b207-114">Update Privilege</span></span>  | <span data-ttu-id="8b207-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="8b207-115">Domain administrator</span></span>                        |
| <span data-ttu-id="8b207-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8b207-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8b207-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b207-117">Attribute-Id</span></span>      | <span data-ttu-id="8b207-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="8b207-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="8b207-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8b207-119">System-Id-Guid</span></span>    | <span data-ttu-id="8b207-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="8b207-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="8b207-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b207-121">Syntax</span></span>            | [<span data-ttu-id="8b207-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8b207-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8b207-123">實作</span><span class="sxs-lookup"><span data-stu-id="8b207-123">Implementations</span></span>

-   [<span data-ttu-id="8b207-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b207-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b207-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="8b207-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8b207-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b207-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b207-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b207-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b207-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b207-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b207-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b207-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8b207-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b207-130">Windows Server 2003</span></span>



| <span data-ttu-id="8b207-131">進入</span><span class="sxs-lookup"><span data-stu-id="8b207-131">Entry</span></span> | <span data-ttu-id="8b207-132">值</span><span class="sxs-lookup"><span data-stu-id="8b207-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b207-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b207-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b207-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b207-135">System-Only</span></span>            | <span data-ttu-id="8b207-136">否</span><span class="sxs-lookup"><span data-stu-id="8b207-136">False</span></span>                                        |
| <span data-ttu-id="8b207-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b207-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8b207-138">否</span><span class="sxs-lookup"><span data-stu-id="8b207-138">False</span></span>                                        |
| <span data-ttu-id="8b207-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b207-139">Is Indexed</span></span>             | <span data-ttu-id="8b207-140">否</span><span class="sxs-lookup"><span data-stu-id="8b207-140">False</span></span>                                        |
| <span data-ttu-id="8b207-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b207-141">In Global Catalog</span></span>      | <span data-ttu-id="8b207-142">否</span><span class="sxs-lookup"><span data-stu-id="8b207-142">False</span></span>                                        |
| <span data-ttu-id="8b207-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b207-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b207-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b207-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b207-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b207-145">Range-Lower</span></span>            | <span data-ttu-id="8b207-146">0</span><span class="sxs-lookup"><span data-stu-id="8b207-146">0</span></span>                                            |
| <span data-ttu-id="8b207-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b207-147">Range-Upper</span></span>            | <span data-ttu-id="8b207-148">2048</span><span class="sxs-lookup"><span data-stu-id="8b207-148">2048</span></span>                                         |
| <span data-ttu-id="8b207-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-149">Search-Flags</span></span>           | <span data-ttu-id="8b207-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b207-150">0x00000000</span></span>                                   |
| <span data-ttu-id="8b207-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-151">System-Flags</span></span>           | <span data-ttu-id="8b207-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b207-152">0x00000010</span></span>                                   |
| <span data-ttu-id="8b207-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b207-153">Classes used in</span></span>        | [<span data-ttu-id="8b207-154">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="8b207-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8b207-155">亞當</span><span class="sxs-lookup"><span data-stu-id="8b207-155">ADAM</span></span>



| <span data-ttu-id="8b207-156">進入</span><span class="sxs-lookup"><span data-stu-id="8b207-156">Entry</span></span> | <span data-ttu-id="8b207-157">值</span><span class="sxs-lookup"><span data-stu-id="8b207-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b207-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b207-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b207-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b207-160">System-Only</span></span>            | <span data-ttu-id="8b207-161">否</span><span class="sxs-lookup"><span data-stu-id="8b207-161">False</span></span>                                        |
| <span data-ttu-id="8b207-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b207-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8b207-163">否</span><span class="sxs-lookup"><span data-stu-id="8b207-163">False</span></span>                                        |
| <span data-ttu-id="8b207-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b207-164">Is Indexed</span></span>             | <span data-ttu-id="8b207-165">否</span><span class="sxs-lookup"><span data-stu-id="8b207-165">False</span></span>                                        |
| <span data-ttu-id="8b207-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b207-166">In Global Catalog</span></span>      | <span data-ttu-id="8b207-167">否</span><span class="sxs-lookup"><span data-stu-id="8b207-167">False</span></span>                                        |
| <span data-ttu-id="8b207-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b207-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b207-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b207-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b207-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b207-170">Range-Lower</span></span>            | <span data-ttu-id="8b207-171">0</span><span class="sxs-lookup"><span data-stu-id="8b207-171">0</span></span>                                            |
| <span data-ttu-id="8b207-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b207-172">Range-Upper</span></span>            | <span data-ttu-id="8b207-173">2048</span><span class="sxs-lookup"><span data-stu-id="8b207-173">2048</span></span>                                         |
| <span data-ttu-id="8b207-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-174">Search-Flags</span></span>           | <span data-ttu-id="8b207-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b207-175">0x00000000</span></span>                                   |
| <span data-ttu-id="8b207-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-176">System-Flags</span></span>           | <span data-ttu-id="8b207-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b207-177">0x00000010</span></span>                                   |
| <span data-ttu-id="8b207-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b207-178">Classes used in</span></span>        | [<span data-ttu-id="8b207-179">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="8b207-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b207-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b207-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b207-181">進入</span><span class="sxs-lookup"><span data-stu-id="8b207-181">Entry</span></span> | <span data-ttu-id="8b207-182">值</span><span class="sxs-lookup"><span data-stu-id="8b207-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b207-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b207-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b207-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b207-185">System-Only</span></span>            | <span data-ttu-id="8b207-186">否</span><span class="sxs-lookup"><span data-stu-id="8b207-186">False</span></span>                                        |
| <span data-ttu-id="8b207-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b207-187">Is-Single-Valued</span></span>       | <span data-ttu-id="8b207-188">否</span><span class="sxs-lookup"><span data-stu-id="8b207-188">False</span></span>                                        |
| <span data-ttu-id="8b207-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b207-189">Is Indexed</span></span>             | <span data-ttu-id="8b207-190">否</span><span class="sxs-lookup"><span data-stu-id="8b207-190">False</span></span>                                        |
| <span data-ttu-id="8b207-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b207-191">In Global Catalog</span></span>      | <span data-ttu-id="8b207-192">否</span><span class="sxs-lookup"><span data-stu-id="8b207-192">False</span></span>                                        |
| <span data-ttu-id="8b207-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b207-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b207-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b207-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b207-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b207-195">Range-Lower</span></span>            | <span data-ttu-id="8b207-196">0</span><span class="sxs-lookup"><span data-stu-id="8b207-196">0</span></span>                                            |
| <span data-ttu-id="8b207-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b207-197">Range-Upper</span></span>            | <span data-ttu-id="8b207-198">2048</span><span class="sxs-lookup"><span data-stu-id="8b207-198">2048</span></span>                                         |
| <span data-ttu-id="8b207-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-199">Search-Flags</span></span>           | <span data-ttu-id="8b207-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b207-200">0x00000000</span></span>                                   |
| <span data-ttu-id="8b207-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-201">System-Flags</span></span>           | <span data-ttu-id="8b207-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b207-202">0x00000010</span></span>                                   |
| <span data-ttu-id="8b207-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b207-203">Classes used in</span></span>        | [<span data-ttu-id="8b207-204">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="8b207-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b207-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b207-205">Windows Server 2008</span></span>



| <span data-ttu-id="8b207-206">進入</span><span class="sxs-lookup"><span data-stu-id="8b207-206">Entry</span></span> | <span data-ttu-id="8b207-207">值</span><span class="sxs-lookup"><span data-stu-id="8b207-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b207-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b207-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b207-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b207-210">System-Only</span></span>            | <span data-ttu-id="8b207-211">否</span><span class="sxs-lookup"><span data-stu-id="8b207-211">False</span></span>                                        |
| <span data-ttu-id="8b207-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b207-212">Is-Single-Valued</span></span>       | <span data-ttu-id="8b207-213">否</span><span class="sxs-lookup"><span data-stu-id="8b207-213">False</span></span>                                        |
| <span data-ttu-id="8b207-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b207-214">Is Indexed</span></span>             | <span data-ttu-id="8b207-215">否</span><span class="sxs-lookup"><span data-stu-id="8b207-215">False</span></span>                                        |
| <span data-ttu-id="8b207-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b207-216">In Global Catalog</span></span>      | <span data-ttu-id="8b207-217">否</span><span class="sxs-lookup"><span data-stu-id="8b207-217">False</span></span>                                        |
| <span data-ttu-id="8b207-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b207-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b207-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b207-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b207-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b207-220">Range-Lower</span></span>            | <span data-ttu-id="8b207-221">0</span><span class="sxs-lookup"><span data-stu-id="8b207-221">0</span></span>                                            |
| <span data-ttu-id="8b207-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b207-222">Range-Upper</span></span>            | <span data-ttu-id="8b207-223">2048</span><span class="sxs-lookup"><span data-stu-id="8b207-223">2048</span></span>                                         |
| <span data-ttu-id="8b207-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-224">Search-Flags</span></span>           | <span data-ttu-id="8b207-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b207-225">0x00000000</span></span>                                   |
| <span data-ttu-id="8b207-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-226">System-Flags</span></span>           | <span data-ttu-id="8b207-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b207-227">0x00000010</span></span>                                   |
| <span data-ttu-id="8b207-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b207-228">Classes used in</span></span>        | [<span data-ttu-id="8b207-229">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="8b207-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b207-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b207-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b207-231">進入</span><span class="sxs-lookup"><span data-stu-id="8b207-231">Entry</span></span> | <span data-ttu-id="8b207-232">值</span><span class="sxs-lookup"><span data-stu-id="8b207-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b207-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b207-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b207-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b207-235">System-Only</span></span>            | <span data-ttu-id="8b207-236">否</span><span class="sxs-lookup"><span data-stu-id="8b207-236">False</span></span>                                        |
| <span data-ttu-id="8b207-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b207-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8b207-238">否</span><span class="sxs-lookup"><span data-stu-id="8b207-238">False</span></span>                                        |
| <span data-ttu-id="8b207-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b207-239">Is Indexed</span></span>             | <span data-ttu-id="8b207-240">否</span><span class="sxs-lookup"><span data-stu-id="8b207-240">False</span></span>                                        |
| <span data-ttu-id="8b207-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b207-241">In Global Catalog</span></span>      | <span data-ttu-id="8b207-242">否</span><span class="sxs-lookup"><span data-stu-id="8b207-242">False</span></span>                                        |
| <span data-ttu-id="8b207-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b207-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b207-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b207-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b207-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b207-245">Range-Lower</span></span>            | <span data-ttu-id="8b207-246">0</span><span class="sxs-lookup"><span data-stu-id="8b207-246">0</span></span>                                            |
| <span data-ttu-id="8b207-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b207-247">Range-Upper</span></span>            | <span data-ttu-id="8b207-248">2048</span><span class="sxs-lookup"><span data-stu-id="8b207-248">2048</span></span>                                         |
| <span data-ttu-id="8b207-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-249">Search-Flags</span></span>           | <span data-ttu-id="8b207-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b207-250">0x00000000</span></span>                                   |
| <span data-ttu-id="8b207-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-251">System-Flags</span></span>           | <span data-ttu-id="8b207-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b207-252">0x00000010</span></span>                                   |
| <span data-ttu-id="8b207-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b207-253">Classes used in</span></span>        | [<span data-ttu-id="8b207-254">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="8b207-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b207-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b207-255">Windows Server 2012</span></span>



| <span data-ttu-id="8b207-256">進入</span><span class="sxs-lookup"><span data-stu-id="8b207-256">Entry</span></span> | <span data-ttu-id="8b207-257">值</span><span class="sxs-lookup"><span data-stu-id="8b207-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b207-258">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b207-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b207-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b207-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b207-260">System-Only</span></span>            | <span data-ttu-id="8b207-261">否</span><span class="sxs-lookup"><span data-stu-id="8b207-261">False</span></span>                                        |
| <span data-ttu-id="8b207-262">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b207-262">Is-Single-Valued</span></span>       | <span data-ttu-id="8b207-263">否</span><span class="sxs-lookup"><span data-stu-id="8b207-263">False</span></span>                                        |
| <span data-ttu-id="8b207-264">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b207-264">Is Indexed</span></span>             | <span data-ttu-id="8b207-265">否</span><span class="sxs-lookup"><span data-stu-id="8b207-265">False</span></span>                                        |
| <span data-ttu-id="8b207-266">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b207-266">In Global Catalog</span></span>      | <span data-ttu-id="8b207-267">否</span><span class="sxs-lookup"><span data-stu-id="8b207-267">False</span></span>                                        |
| <span data-ttu-id="8b207-268">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b207-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b207-269">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b207-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b207-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b207-270">Range-Lower</span></span>            | <span data-ttu-id="8b207-271">0</span><span class="sxs-lookup"><span data-stu-id="8b207-271">0</span></span>                                            |
| <span data-ttu-id="8b207-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b207-272">Range-Upper</span></span>            | <span data-ttu-id="8b207-273">2048</span><span class="sxs-lookup"><span data-stu-id="8b207-273">2048</span></span>                                         |
| <span data-ttu-id="8b207-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-274">Search-Flags</span></span>           | <span data-ttu-id="8b207-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b207-275">0x00000000</span></span>                                   |
| <span data-ttu-id="8b207-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b207-276">System-Flags</span></span>           | <span data-ttu-id="8b207-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b207-277">0x00000010</span></span>                                   |
| <span data-ttu-id="8b207-278">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b207-278">Classes used in</span></span>        | [<span data-ttu-id="8b207-279">**網域 DNS**</span><span class="sxs-lookup"><span data-stu-id="8b207-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





