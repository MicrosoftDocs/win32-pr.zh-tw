---
title: Site-Object 屬性
description: 此子網所屬網站的分辨名稱。
ms.assetid: 4533c742-4276-48df-b0cd-7ba1641737a7
ms.tgt_platform: multiple
keywords:
- Site-Object 屬性 AD 架構
- siteObject 屬性 AD 架構
topic_type:
- apiref
api_name:
- Site-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac43fb4ee0718aec855de4b7eb251a5d67c1a5fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845295"
---
# <a name="site-object-attribute"></a><span data-ttu-id="927f3-105">Site-Object 屬性</span><span class="sxs-lookup"><span data-stu-id="927f3-105">Site-Object attribute</span></span>

<span data-ttu-id="927f3-106">此子網所屬網站的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="927f3-106">The distinguished name for the site to which this subnet belongs.</span></span>



| <span data-ttu-id="927f3-107">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-107">Entry</span></span> | <span data-ttu-id="927f3-108">值</span><span class="sxs-lookup"><span data-stu-id="927f3-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="927f3-109">CN</span><span class="sxs-lookup"><span data-stu-id="927f3-109">CN</span></span>                | <span data-ttu-id="927f3-110">Site-Object</span><span class="sxs-lookup"><span data-stu-id="927f3-110">Site-Object</span></span>                             |
| <span data-ttu-id="927f3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="927f3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="927f3-112">siteObject</span><span class="sxs-lookup"><span data-stu-id="927f3-112">siteObject</span></span>                              |
| <span data-ttu-id="927f3-113">大小</span><span class="sxs-lookup"><span data-stu-id="927f3-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="927f3-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="927f3-114">Update Privilege</span></span>  | <span data-ttu-id="927f3-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="927f3-115">Domain administrator</span></span>                    |
| <span data-ttu-id="927f3-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="927f3-116">Update Frequency</span></span>  | <span data-ttu-id="927f3-117">每次建立網站時。</span><span class="sxs-lookup"><span data-stu-id="927f3-117">Whenever a site is created.</span></span>             |
| <span data-ttu-id="927f3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-118">Attribute-Id</span></span>      | <span data-ttu-id="927f3-119">1.2.840.113556.1.4.512</span><span class="sxs-lookup"><span data-stu-id="927f3-119">1.2.840.113556.1.4.512</span></span>                  |
| <span data-ttu-id="927f3-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="927f3-120">System-Id-Guid</span></span>    | <span data-ttu-id="927f3-121">3e10944c-c354-11d0-aff8-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="927f3-121">3e10944c-c354-11d0-aff8-0000f80367c1</span></span>    |
| <span data-ttu-id="927f3-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="927f3-122">Syntax</span></span>            | [<span data-ttu-id="927f3-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="927f3-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="927f3-124">實作</span><span class="sxs-lookup"><span data-stu-id="927f3-124">Implementations</span></span>

-   [<span data-ttu-id="927f3-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="927f3-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="927f3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="927f3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="927f3-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="927f3-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="927f3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="927f3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="927f3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="927f3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="927f3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="927f3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="927f3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="927f3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="927f3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="927f3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="927f3-133">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-133">Entry</span></span> | <span data-ttu-id="927f3-134">值</span><span class="sxs-lookup"><span data-stu-id="927f3-134">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="927f3-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="927f3-135">Link-Id</span></span>                | <span data-ttu-id="927f3-136">46</span><span class="sxs-lookup"><span data-stu-id="927f3-136">46</span></span>                                    |
| <span data-ttu-id="927f3-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-137">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="927f3-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="927f3-138">System-Only</span></span>            | <span data-ttu-id="927f3-139">否</span><span class="sxs-lookup"><span data-stu-id="927f3-139">False</span></span>                                 |
| <span data-ttu-id="927f3-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="927f3-140">Is-Single-Valued</span></span>       | <span data-ttu-id="927f3-141">對</span><span class="sxs-lookup"><span data-stu-id="927f3-141">True</span></span>                                  |
| <span data-ttu-id="927f3-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="927f3-142">Is Indexed</span></span>             | <span data-ttu-id="927f3-143">否</span><span class="sxs-lookup"><span data-stu-id="927f3-143">False</span></span>                                 |
| <span data-ttu-id="927f3-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="927f3-144">In Global Catalog</span></span>      | <span data-ttu-id="927f3-145">否</span><span class="sxs-lookup"><span data-stu-id="927f3-145">False</span></span>                                 |
| <span data-ttu-id="927f3-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="927f3-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="927f3-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="927f3-147">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="927f3-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927f3-148">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="927f3-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927f3-149">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="927f3-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-150">Search-Flags</span></span>           | <span data-ttu-id="927f3-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927f3-151">0x00000000</span></span>                            |
| <span data-ttu-id="927f3-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-152">System-Flags</span></span>           | <span data-ttu-id="927f3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927f3-153">0x00000010</span></span>                            |
| <span data-ttu-id="927f3-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="927f3-154">Classes used in</span></span>        | [<span data-ttu-id="927f3-155">**子**</span><span class="sxs-lookup"><span data-stu-id="927f3-155">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="927f3-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="927f3-156">Windows Server 2003</span></span>



| <span data-ttu-id="927f3-157">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-157">Entry</span></span> | <span data-ttu-id="927f3-158">值</span><span class="sxs-lookup"><span data-stu-id="927f3-158">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="927f3-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="927f3-159">Link-Id</span></span>                | <span data-ttu-id="927f3-160">46</span><span class="sxs-lookup"><span data-stu-id="927f3-160">46</span></span>                                    |
| <span data-ttu-id="927f3-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="927f3-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="927f3-162">System-Only</span></span>            | <span data-ttu-id="927f3-163">否</span><span class="sxs-lookup"><span data-stu-id="927f3-163">False</span></span>                                 |
| <span data-ttu-id="927f3-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="927f3-164">Is-Single-Valued</span></span>       | <span data-ttu-id="927f3-165">對</span><span class="sxs-lookup"><span data-stu-id="927f3-165">True</span></span>                                  |
| <span data-ttu-id="927f3-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="927f3-166">Is Indexed</span></span>             | <span data-ttu-id="927f3-167">否</span><span class="sxs-lookup"><span data-stu-id="927f3-167">False</span></span>                                 |
| <span data-ttu-id="927f3-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="927f3-168">In Global Catalog</span></span>      | <span data-ttu-id="927f3-169">否</span><span class="sxs-lookup"><span data-stu-id="927f3-169">False</span></span>                                 |
| <span data-ttu-id="927f3-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="927f3-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="927f3-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="927f3-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="927f3-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927f3-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="927f3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927f3-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="927f3-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-174">Search-Flags</span></span>           | <span data-ttu-id="927f3-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927f3-175">0x00000000</span></span>                            |
| <span data-ttu-id="927f3-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-176">System-Flags</span></span>           | <span data-ttu-id="927f3-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927f3-177">0x00000010</span></span>                            |
| <span data-ttu-id="927f3-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="927f3-178">Classes used in</span></span>        | [<span data-ttu-id="927f3-179">**子**</span><span class="sxs-lookup"><span data-stu-id="927f3-179">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="adam"></a><span data-ttu-id="927f3-180">亞當</span><span class="sxs-lookup"><span data-stu-id="927f3-180">ADAM</span></span>



| <span data-ttu-id="927f3-181">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-181">Entry</span></span> | <span data-ttu-id="927f3-182">值</span><span class="sxs-lookup"><span data-stu-id="927f3-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="927f3-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="927f3-183">Link-Id</span></span>                | <span data-ttu-id="927f3-184">46</span><span class="sxs-lookup"><span data-stu-id="927f3-184">46</span></span>                                    |
| <span data-ttu-id="927f3-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-185">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="927f3-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="927f3-186">System-Only</span></span>            | <span data-ttu-id="927f3-187">否</span><span class="sxs-lookup"><span data-stu-id="927f3-187">False</span></span>                                 |
| <span data-ttu-id="927f3-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="927f3-188">Is-Single-Valued</span></span>       | <span data-ttu-id="927f3-189">對</span><span class="sxs-lookup"><span data-stu-id="927f3-189">True</span></span>                                  |
| <span data-ttu-id="927f3-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="927f3-190">Is Indexed</span></span>             | <span data-ttu-id="927f3-191">否</span><span class="sxs-lookup"><span data-stu-id="927f3-191">False</span></span>                                 |
| <span data-ttu-id="927f3-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="927f3-192">In Global Catalog</span></span>      | <span data-ttu-id="927f3-193">否</span><span class="sxs-lookup"><span data-stu-id="927f3-193">False</span></span>                                 |
| <span data-ttu-id="927f3-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="927f3-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="927f3-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="927f3-195">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="927f3-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927f3-196">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="927f3-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927f3-197">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="927f3-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-198">Search-Flags</span></span>           | <span data-ttu-id="927f3-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927f3-199">0x00000000</span></span>                            |
| <span data-ttu-id="927f3-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-200">System-Flags</span></span>           | <span data-ttu-id="927f3-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927f3-201">0x00000010</span></span>                            |
| <span data-ttu-id="927f3-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="927f3-202">Classes used in</span></span>        | [<span data-ttu-id="927f3-203">**子**</span><span class="sxs-lookup"><span data-stu-id="927f3-203">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="927f3-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="927f3-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="927f3-205">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-205">Entry</span></span> | <span data-ttu-id="927f3-206">值</span><span class="sxs-lookup"><span data-stu-id="927f3-206">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="927f3-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="927f3-207">Link-Id</span></span>                | <span data-ttu-id="927f3-208">46</span><span class="sxs-lookup"><span data-stu-id="927f3-208">46</span></span>                                    |
| <span data-ttu-id="927f3-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-209">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="927f3-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="927f3-210">System-Only</span></span>            | <span data-ttu-id="927f3-211">否</span><span class="sxs-lookup"><span data-stu-id="927f3-211">False</span></span>                                 |
| <span data-ttu-id="927f3-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="927f3-212">Is-Single-Valued</span></span>       | <span data-ttu-id="927f3-213">對</span><span class="sxs-lookup"><span data-stu-id="927f3-213">True</span></span>                                  |
| <span data-ttu-id="927f3-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="927f3-214">Is Indexed</span></span>             | <span data-ttu-id="927f3-215">否</span><span class="sxs-lookup"><span data-stu-id="927f3-215">False</span></span>                                 |
| <span data-ttu-id="927f3-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="927f3-216">In Global Catalog</span></span>      | <span data-ttu-id="927f3-217">否</span><span class="sxs-lookup"><span data-stu-id="927f3-217">False</span></span>                                 |
| <span data-ttu-id="927f3-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="927f3-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="927f3-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="927f3-219">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="927f3-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927f3-220">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="927f3-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927f3-221">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="927f3-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-222">Search-Flags</span></span>           | <span data-ttu-id="927f3-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927f3-223">0x00000000</span></span>                            |
| <span data-ttu-id="927f3-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-224">System-Flags</span></span>           | <span data-ttu-id="927f3-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927f3-225">0x00000010</span></span>                            |
| <span data-ttu-id="927f3-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="927f3-226">Classes used in</span></span>        | [<span data-ttu-id="927f3-227">**子**</span><span class="sxs-lookup"><span data-stu-id="927f3-227">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="927f3-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="927f3-228">Windows Server 2008</span></span>



| <span data-ttu-id="927f3-229">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-229">Entry</span></span> | <span data-ttu-id="927f3-230">值</span><span class="sxs-lookup"><span data-stu-id="927f3-230">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="927f3-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="927f3-231">Link-Id</span></span>                | <span data-ttu-id="927f3-232">46</span><span class="sxs-lookup"><span data-stu-id="927f3-232">46</span></span>                                    |
| <span data-ttu-id="927f3-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-233">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="927f3-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="927f3-234">System-Only</span></span>            | <span data-ttu-id="927f3-235">否</span><span class="sxs-lookup"><span data-stu-id="927f3-235">False</span></span>                                 |
| <span data-ttu-id="927f3-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="927f3-236">Is-Single-Valued</span></span>       | <span data-ttu-id="927f3-237">對</span><span class="sxs-lookup"><span data-stu-id="927f3-237">True</span></span>                                  |
| <span data-ttu-id="927f3-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="927f3-238">Is Indexed</span></span>             | <span data-ttu-id="927f3-239">否</span><span class="sxs-lookup"><span data-stu-id="927f3-239">False</span></span>                                 |
| <span data-ttu-id="927f3-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="927f3-240">In Global Catalog</span></span>      | <span data-ttu-id="927f3-241">否</span><span class="sxs-lookup"><span data-stu-id="927f3-241">False</span></span>                                 |
| <span data-ttu-id="927f3-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="927f3-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="927f3-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="927f3-243">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="927f3-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927f3-244">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="927f3-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927f3-245">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="927f3-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-246">Search-Flags</span></span>           | <span data-ttu-id="927f3-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927f3-247">0x00000000</span></span>                            |
| <span data-ttu-id="927f3-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-248">System-Flags</span></span>           | <span data-ttu-id="927f3-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927f3-249">0x00000010</span></span>                            |
| <span data-ttu-id="927f3-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="927f3-250">Classes used in</span></span>        | [<span data-ttu-id="927f3-251">**子**</span><span class="sxs-lookup"><span data-stu-id="927f3-251">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="927f3-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="927f3-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="927f3-253">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-253">Entry</span></span> | <span data-ttu-id="927f3-254">值</span><span class="sxs-lookup"><span data-stu-id="927f3-254">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="927f3-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="927f3-255">Link-Id</span></span>                | <span data-ttu-id="927f3-256">46</span><span class="sxs-lookup"><span data-stu-id="927f3-256">46</span></span>                                    |
| <span data-ttu-id="927f3-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-257">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="927f3-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="927f3-258">System-Only</span></span>            | <span data-ttu-id="927f3-259">否</span><span class="sxs-lookup"><span data-stu-id="927f3-259">False</span></span>                                 |
| <span data-ttu-id="927f3-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="927f3-260">Is-Single-Valued</span></span>       | <span data-ttu-id="927f3-261">對</span><span class="sxs-lookup"><span data-stu-id="927f3-261">True</span></span>                                  |
| <span data-ttu-id="927f3-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="927f3-262">Is Indexed</span></span>             | <span data-ttu-id="927f3-263">否</span><span class="sxs-lookup"><span data-stu-id="927f3-263">False</span></span>                                 |
| <span data-ttu-id="927f3-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="927f3-264">In Global Catalog</span></span>      | <span data-ttu-id="927f3-265">否</span><span class="sxs-lookup"><span data-stu-id="927f3-265">False</span></span>                                 |
| <span data-ttu-id="927f3-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="927f3-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="927f3-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="927f3-267">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="927f3-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927f3-268">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="927f3-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927f3-269">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="927f3-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-270">Search-Flags</span></span>           | <span data-ttu-id="927f3-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927f3-271">0x00000000</span></span>                            |
| <span data-ttu-id="927f3-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-272">System-Flags</span></span>           | <span data-ttu-id="927f3-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927f3-273">0x00000010</span></span>                            |
| <span data-ttu-id="927f3-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="927f3-274">Classes used in</span></span>        | [<span data-ttu-id="927f3-275">**子**</span><span class="sxs-lookup"><span data-stu-id="927f3-275">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="927f3-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="927f3-276">Windows Server 2012</span></span>



| <span data-ttu-id="927f3-277">進入</span><span class="sxs-lookup"><span data-stu-id="927f3-277">Entry</span></span> | <span data-ttu-id="927f3-278">值</span><span class="sxs-lookup"><span data-stu-id="927f3-278">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="927f3-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="927f3-279">Link-Id</span></span>                | <span data-ttu-id="927f3-280">46</span><span class="sxs-lookup"><span data-stu-id="927f3-280">46</span></span>                                    |
| <span data-ttu-id="927f3-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="927f3-281">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="927f3-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="927f3-282">System-Only</span></span>            | <span data-ttu-id="927f3-283">否</span><span class="sxs-lookup"><span data-stu-id="927f3-283">False</span></span>                                 |
| <span data-ttu-id="927f3-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="927f3-284">Is-Single-Valued</span></span>       | <span data-ttu-id="927f3-285">對</span><span class="sxs-lookup"><span data-stu-id="927f3-285">True</span></span>                                  |
| <span data-ttu-id="927f3-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="927f3-286">Is Indexed</span></span>             | <span data-ttu-id="927f3-287">否</span><span class="sxs-lookup"><span data-stu-id="927f3-287">False</span></span>                                 |
| <span data-ttu-id="927f3-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="927f3-288">In Global Catalog</span></span>      | <span data-ttu-id="927f3-289">否</span><span class="sxs-lookup"><span data-stu-id="927f3-289">False</span></span>                                 |
| <span data-ttu-id="927f3-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="927f3-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="927f3-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="927f3-291">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="927f3-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="927f3-292">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="927f3-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="927f3-293">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="927f3-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-294">Search-Flags</span></span>           | <span data-ttu-id="927f3-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="927f3-295">0x00000000</span></span>                            |
| <span data-ttu-id="927f3-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="927f3-296">System-Flags</span></span>           | <span data-ttu-id="927f3-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="927f3-297">0x00000010</span></span>                            |
| <span data-ttu-id="927f3-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="927f3-298">Classes used in</span></span>        | [<span data-ttu-id="927f3-299">**子**</span><span class="sxs-lookup"><span data-stu-id="927f3-299">**Subnet**</span></span>](c-subnet.md)<br/> |



 

 





