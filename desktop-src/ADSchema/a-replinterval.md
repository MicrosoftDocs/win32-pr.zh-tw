---
title: Repl-Interval 屬性
description: Site-Link 物件的屬性，可定義網站清單中網站之間的複寫間隔（以分鐘為單位）。
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Repl-Interval 屬性 AD 架構
- replInterval 屬性 AD 架構
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107591"
---
# <a name="repl-interval-attribute"></a><span data-ttu-id="e7447-105">Repl-Interval 屬性</span><span class="sxs-lookup"><span data-stu-id="e7447-105">Repl-Interval attribute</span></span>

<span data-ttu-id="e7447-106">Site-Link 物件的屬性，可定義網站清單中網站之間的複寫間隔（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="e7447-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="e7447-107">必須是15分鐘的倍數 (跨網站 DS 複寫) 的細微性、最少15分鐘，以及最多10080分鐘 (一周) 。</span><span class="sxs-lookup"><span data-stu-id="e7447-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="e7447-108">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-108">Entry</span></span> | <span data-ttu-id="e7447-109">值</span><span class="sxs-lookup"><span data-stu-id="e7447-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="e7447-110">CN</span><span class="sxs-lookup"><span data-stu-id="e7447-110">CN</span></span>                | <span data-ttu-id="e7447-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="e7447-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="e7447-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e7447-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e7447-113">replInterval</span><span class="sxs-lookup"><span data-stu-id="e7447-113">replInterval</span></span>                                   |
| <span data-ttu-id="e7447-114">大小</span><span class="sxs-lookup"><span data-stu-id="e7447-114">Size</span></span>              | <span data-ttu-id="e7447-115">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="e7447-115">4 bytes</span></span>                                        |
| <span data-ttu-id="e7447-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e7447-116">Update Privilege</span></span>  | <span data-ttu-id="e7447-117">企業系統管理員</span><span class="sxs-lookup"><span data-stu-id="e7447-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="e7447-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e7447-118">Update Frequency</span></span>  | <span data-ttu-id="e7447-119">當複寫間隔需要變更時。</span><span class="sxs-lookup"><span data-stu-id="e7447-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="e7447-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-120">Attribute-Id</span></span>      | <span data-ttu-id="e7447-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="e7447-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="e7447-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e7447-122">System-Id-Guid</span></span>    | <span data-ttu-id="e7447-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="e7447-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="e7447-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7447-124">Syntax</span></span>            | [<span data-ttu-id="e7447-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e7447-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="e7447-126">實作</span><span class="sxs-lookup"><span data-stu-id="e7447-126">Implementations</span></span>

-   [<span data-ttu-id="e7447-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e7447-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e7447-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7447-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7447-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e7447-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e7447-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7447-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7447-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7447-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7447-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7447-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7447-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7447-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e7447-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7447-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e7447-135">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-135">Entry</span></span> | <span data-ttu-id="e7447-136">值</span><span class="sxs-lookup"><span data-stu-id="e7447-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7447-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e7447-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7447-139">System-Only</span></span>            | <span data-ttu-id="e7447-140">否</span><span class="sxs-lookup"><span data-stu-id="e7447-140">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e7447-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e7447-142">對</span><span class="sxs-lookup"><span data-stu-id="e7447-142">True</span></span>                                                                                                       |
| <span data-ttu-id="e7447-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e7447-143">Is Indexed</span></span>             | <span data-ttu-id="e7447-144">否</span><span class="sxs-lookup"><span data-stu-id="e7447-144">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e7447-145">In Global Catalog</span></span>      | <span data-ttu-id="e7447-146">否</span><span class="sxs-lookup"><span data-stu-id="e7447-146">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e7447-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7447-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e7447-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e7447-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7447-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7447-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-151">Search-Flags</span></span>           | <span data-ttu-id="e7447-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7447-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e7447-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-153">System-Flags</span></span>           | <span data-ttu-id="e7447-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7447-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e7447-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e7447-155">Classes used in</span></span>        | [<span data-ttu-id="e7447-156">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="e7447-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="e7447-157">**站台連結**</span><span class="sxs-lookup"><span data-stu-id="e7447-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e7447-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7447-158">Windows Server 2003</span></span>



| <span data-ttu-id="e7447-159">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-159">Entry</span></span> | <span data-ttu-id="e7447-160">值</span><span class="sxs-lookup"><span data-stu-id="e7447-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7447-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e7447-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7447-163">System-Only</span></span>            | <span data-ttu-id="e7447-164">否</span><span class="sxs-lookup"><span data-stu-id="e7447-164">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e7447-165">Is-Single-Valued</span></span>       | <span data-ttu-id="e7447-166">對</span><span class="sxs-lookup"><span data-stu-id="e7447-166">True</span></span>                                                                                                       |
| <span data-ttu-id="e7447-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e7447-167">Is Indexed</span></span>             | <span data-ttu-id="e7447-168">否</span><span class="sxs-lookup"><span data-stu-id="e7447-168">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e7447-169">In Global Catalog</span></span>      | <span data-ttu-id="e7447-170">否</span><span class="sxs-lookup"><span data-stu-id="e7447-170">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e7447-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7447-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e7447-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e7447-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7447-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7447-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-175">Search-Flags</span></span>           | <span data-ttu-id="e7447-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7447-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e7447-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-177">System-Flags</span></span>           | <span data-ttu-id="e7447-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7447-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e7447-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e7447-179">Classes used in</span></span>        | [<span data-ttu-id="e7447-180">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="e7447-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="e7447-181">**站台連結**</span><span class="sxs-lookup"><span data-stu-id="e7447-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e7447-182">亞當</span><span class="sxs-lookup"><span data-stu-id="e7447-182">ADAM</span></span>



| <span data-ttu-id="e7447-183">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-183">Entry</span></span> | <span data-ttu-id="e7447-184">值</span><span class="sxs-lookup"><span data-stu-id="e7447-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7447-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e7447-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7447-187">System-Only</span></span>            | <span data-ttu-id="e7447-188">否</span><span class="sxs-lookup"><span data-stu-id="e7447-188">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e7447-189">Is-Single-Valued</span></span>       | <span data-ttu-id="e7447-190">對</span><span class="sxs-lookup"><span data-stu-id="e7447-190">True</span></span>                                                                                                       |
| <span data-ttu-id="e7447-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e7447-191">Is Indexed</span></span>             | <span data-ttu-id="e7447-192">否</span><span class="sxs-lookup"><span data-stu-id="e7447-192">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e7447-193">In Global Catalog</span></span>      | <span data-ttu-id="e7447-194">否</span><span class="sxs-lookup"><span data-stu-id="e7447-194">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e7447-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7447-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e7447-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e7447-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7447-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7447-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-199">Search-Flags</span></span>           | <span data-ttu-id="e7447-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7447-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e7447-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-201">System-Flags</span></span>           | <span data-ttu-id="e7447-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7447-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e7447-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e7447-203">Classes used in</span></span>        | [<span data-ttu-id="e7447-204">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="e7447-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="e7447-205">**站台連結**</span><span class="sxs-lookup"><span data-stu-id="e7447-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7447-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7447-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7447-207">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-207">Entry</span></span> | <span data-ttu-id="e7447-208">值</span><span class="sxs-lookup"><span data-stu-id="e7447-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7447-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e7447-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7447-211">System-Only</span></span>            | <span data-ttu-id="e7447-212">否</span><span class="sxs-lookup"><span data-stu-id="e7447-212">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e7447-213">Is-Single-Valued</span></span>       | <span data-ttu-id="e7447-214">對</span><span class="sxs-lookup"><span data-stu-id="e7447-214">True</span></span>                                                                                                       |
| <span data-ttu-id="e7447-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e7447-215">Is Indexed</span></span>             | <span data-ttu-id="e7447-216">否</span><span class="sxs-lookup"><span data-stu-id="e7447-216">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e7447-217">In Global Catalog</span></span>      | <span data-ttu-id="e7447-218">否</span><span class="sxs-lookup"><span data-stu-id="e7447-218">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e7447-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7447-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e7447-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e7447-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7447-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7447-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-223">Search-Flags</span></span>           | <span data-ttu-id="e7447-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7447-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e7447-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-225">System-Flags</span></span>           | <span data-ttu-id="e7447-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7447-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e7447-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e7447-227">Classes used in</span></span>        | [<span data-ttu-id="e7447-228">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="e7447-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="e7447-229">**站台連結**</span><span class="sxs-lookup"><span data-stu-id="e7447-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e7447-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7447-230">Windows Server 2008</span></span>



| <span data-ttu-id="e7447-231">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-231">Entry</span></span> | <span data-ttu-id="e7447-232">值</span><span class="sxs-lookup"><span data-stu-id="e7447-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7447-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e7447-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7447-235">System-Only</span></span>            | <span data-ttu-id="e7447-236">否</span><span class="sxs-lookup"><span data-stu-id="e7447-236">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e7447-237">Is-Single-Valued</span></span>       | <span data-ttu-id="e7447-238">對</span><span class="sxs-lookup"><span data-stu-id="e7447-238">True</span></span>                                                                                                       |
| <span data-ttu-id="e7447-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e7447-239">Is Indexed</span></span>             | <span data-ttu-id="e7447-240">否</span><span class="sxs-lookup"><span data-stu-id="e7447-240">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e7447-241">In Global Catalog</span></span>      | <span data-ttu-id="e7447-242">否</span><span class="sxs-lookup"><span data-stu-id="e7447-242">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e7447-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7447-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e7447-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e7447-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7447-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7447-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-247">Search-Flags</span></span>           | <span data-ttu-id="e7447-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7447-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e7447-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-249">System-Flags</span></span>           | <span data-ttu-id="e7447-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7447-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e7447-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e7447-251">Classes used in</span></span>        | [<span data-ttu-id="e7447-252">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="e7447-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="e7447-253">**站台連結**</span><span class="sxs-lookup"><span data-stu-id="e7447-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7447-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7447-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7447-255">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-255">Entry</span></span> | <span data-ttu-id="e7447-256">值</span><span class="sxs-lookup"><span data-stu-id="e7447-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7447-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e7447-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7447-259">System-Only</span></span>            | <span data-ttu-id="e7447-260">否</span><span class="sxs-lookup"><span data-stu-id="e7447-260">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e7447-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e7447-262">對</span><span class="sxs-lookup"><span data-stu-id="e7447-262">True</span></span>                                                                                                       |
| <span data-ttu-id="e7447-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e7447-263">Is Indexed</span></span>             | <span data-ttu-id="e7447-264">否</span><span class="sxs-lookup"><span data-stu-id="e7447-264">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e7447-265">In Global Catalog</span></span>      | <span data-ttu-id="e7447-266">否</span><span class="sxs-lookup"><span data-stu-id="e7447-266">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e7447-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7447-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e7447-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e7447-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7447-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7447-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-271">Search-Flags</span></span>           | <span data-ttu-id="e7447-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7447-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e7447-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-273">System-Flags</span></span>           | <span data-ttu-id="e7447-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7447-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e7447-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e7447-275">Classes used in</span></span>        | [<span data-ttu-id="e7447-276">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="e7447-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="e7447-277">**站台連結**</span><span class="sxs-lookup"><span data-stu-id="e7447-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e7447-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7447-278">Windows Server 2012</span></span>



| <span data-ttu-id="e7447-279">進入</span><span class="sxs-lookup"><span data-stu-id="e7447-279">Entry</span></span> | <span data-ttu-id="e7447-280">值</span><span class="sxs-lookup"><span data-stu-id="e7447-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7447-281">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e7447-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7447-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="e7447-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7447-283">System-Only</span></span>            | <span data-ttu-id="e7447-284">否</span><span class="sxs-lookup"><span data-stu-id="e7447-284">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e7447-285">Is-Single-Valued</span></span>       | <span data-ttu-id="e7447-286">對</span><span class="sxs-lookup"><span data-stu-id="e7447-286">True</span></span>                                                                                                       |
| <span data-ttu-id="e7447-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e7447-287">Is Indexed</span></span>             | <span data-ttu-id="e7447-288">否</span><span class="sxs-lookup"><span data-stu-id="e7447-288">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e7447-289">In Global Catalog</span></span>      | <span data-ttu-id="e7447-290">否</span><span class="sxs-lookup"><span data-stu-id="e7447-290">False</span></span>                                                                                                      |
| <span data-ttu-id="e7447-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e7447-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7447-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e7447-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="e7447-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7447-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7447-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="e7447-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-295">Search-Flags</span></span>           | <span data-ttu-id="e7447-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7447-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="e7447-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7447-297">System-Flags</span></span>           | <span data-ttu-id="e7447-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7447-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="e7447-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e7447-299">Classes used in</span></span>        | [<span data-ttu-id="e7447-300">**站間-傳輸**</span><span class="sxs-lookup"><span data-stu-id="e7447-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="e7447-301">**站台連結**</span><span class="sxs-lookup"><span data-stu-id="e7447-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





