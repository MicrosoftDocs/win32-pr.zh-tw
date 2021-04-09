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
# <a name="site-object-attribute"></a><span data-ttu-id="1406b-105">Site-Object 屬性</span><span class="sxs-lookup"><span data-stu-id="1406b-105">Site-Object attribute</span></span>

<span data-ttu-id="1406b-106">此子網所屬網站的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="1406b-106">The distinguished name for the site to which this subnet belongs.</span></span>



| <span data-ttu-id="1406b-107">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-107">Entry</span></span> | <span data-ttu-id="1406b-108">值</span><span class="sxs-lookup"><span data-stu-id="1406b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1406b-109">CN</span><span class="sxs-lookup"><span data-stu-id="1406b-109">CN</span></span>                | <span data-ttu-id="1406b-110">Site-Object</span><span class="sxs-lookup"><span data-stu-id="1406b-110">Site-Object</span></span>                             |
| <span data-ttu-id="1406b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1406b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1406b-112">siteObject</span><span class="sxs-lookup"><span data-stu-id="1406b-112">siteObject</span></span>                              |
| <span data-ttu-id="1406b-113">大小</span><span class="sxs-lookup"><span data-stu-id="1406b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="1406b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1406b-114">Update Privilege</span></span>  | <span data-ttu-id="1406b-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="1406b-115">Domain administrator</span></span>                    |
| <span data-ttu-id="1406b-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1406b-116">Update Frequency</span></span>  | <span data-ttu-id="1406b-117">每次建立網站時。</span><span class="sxs-lookup"><span data-stu-id="1406b-117">Whenever a site is created.</span></span>             |
| <span data-ttu-id="1406b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-118">Attribute-Id</span></span>      | <span data-ttu-id="1406b-119">1.2.840.113556.1.4.512</span><span class="sxs-lookup"><span data-stu-id="1406b-119">1.2.840.113556.1.4.512</span></span>                  |
| <span data-ttu-id="1406b-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1406b-120">System-Id-Guid</span></span>    | <span data-ttu-id="1406b-121">3e10944c-c354-11d0-aff8-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1406b-121">3e10944c-c354-11d0-aff8-0000f80367c1</span></span>    |
| <span data-ttu-id="1406b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1406b-122">Syntax</span></span>            | [<span data-ttu-id="1406b-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1406b-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1406b-124">實作</span><span class="sxs-lookup"><span data-stu-id="1406b-124">Implementations</span></span>

-   [<span data-ttu-id="1406b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1406b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1406b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1406b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1406b-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="1406b-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1406b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1406b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1406b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1406b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1406b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1406b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1406b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1406b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1406b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1406b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1406b-133">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-133">Entry</span></span> | <span data-ttu-id="1406b-134">值</span><span class="sxs-lookup"><span data-stu-id="1406b-134">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="1406b-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1406b-135">Link-Id</span></span>                | <span data-ttu-id="1406b-136">46</span><span class="sxs-lookup"><span data-stu-id="1406b-136">46</span></span>                                    |
| <span data-ttu-id="1406b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-137">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="1406b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="1406b-138">System-Only</span></span>            | <span data-ttu-id="1406b-139">否</span><span class="sxs-lookup"><span data-stu-id="1406b-139">False</span></span>                                 |
| <span data-ttu-id="1406b-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1406b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="1406b-141">對</span><span class="sxs-lookup"><span data-stu-id="1406b-141">True</span></span>                                  |
| <span data-ttu-id="1406b-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1406b-142">Is Indexed</span></span>             | <span data-ttu-id="1406b-143">否</span><span class="sxs-lookup"><span data-stu-id="1406b-143">False</span></span>                                 |
| <span data-ttu-id="1406b-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1406b-144">In Global Catalog</span></span>      | <span data-ttu-id="1406b-145">否</span><span class="sxs-lookup"><span data-stu-id="1406b-145">False</span></span>                                 |
| <span data-ttu-id="1406b-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1406b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="1406b-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1406b-147">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="1406b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1406b-148">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="1406b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1406b-149">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="1406b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-150">Search-Flags</span></span>           | <span data-ttu-id="1406b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1406b-151">0x00000000</span></span>                            |
| <span data-ttu-id="1406b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-152">System-Flags</span></span>           | <span data-ttu-id="1406b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1406b-153">0x00000010</span></span>                            |
| <span data-ttu-id="1406b-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1406b-154">Classes used in</span></span>        | [<span data-ttu-id="1406b-155">**子**</span><span class="sxs-lookup"><span data-stu-id="1406b-155">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1406b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1406b-156">Windows Server 2003</span></span>



| <span data-ttu-id="1406b-157">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-157">Entry</span></span> | <span data-ttu-id="1406b-158">值</span><span class="sxs-lookup"><span data-stu-id="1406b-158">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="1406b-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1406b-159">Link-Id</span></span>                | <span data-ttu-id="1406b-160">46</span><span class="sxs-lookup"><span data-stu-id="1406b-160">46</span></span>                                    |
| <span data-ttu-id="1406b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="1406b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="1406b-162">System-Only</span></span>            | <span data-ttu-id="1406b-163">否</span><span class="sxs-lookup"><span data-stu-id="1406b-163">False</span></span>                                 |
| <span data-ttu-id="1406b-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1406b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="1406b-165">對</span><span class="sxs-lookup"><span data-stu-id="1406b-165">True</span></span>                                  |
| <span data-ttu-id="1406b-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1406b-166">Is Indexed</span></span>             | <span data-ttu-id="1406b-167">否</span><span class="sxs-lookup"><span data-stu-id="1406b-167">False</span></span>                                 |
| <span data-ttu-id="1406b-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1406b-168">In Global Catalog</span></span>      | <span data-ttu-id="1406b-169">否</span><span class="sxs-lookup"><span data-stu-id="1406b-169">False</span></span>                                 |
| <span data-ttu-id="1406b-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1406b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="1406b-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1406b-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="1406b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1406b-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="1406b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1406b-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="1406b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-174">Search-Flags</span></span>           | <span data-ttu-id="1406b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1406b-175">0x00000000</span></span>                            |
| <span data-ttu-id="1406b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-176">System-Flags</span></span>           | <span data-ttu-id="1406b-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1406b-177">0x00000010</span></span>                            |
| <span data-ttu-id="1406b-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1406b-178">Classes used in</span></span>        | [<span data-ttu-id="1406b-179">**子**</span><span class="sxs-lookup"><span data-stu-id="1406b-179">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1406b-180">亞當</span><span class="sxs-lookup"><span data-stu-id="1406b-180">ADAM</span></span>



| <span data-ttu-id="1406b-181">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-181">Entry</span></span> | <span data-ttu-id="1406b-182">值</span><span class="sxs-lookup"><span data-stu-id="1406b-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="1406b-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1406b-183">Link-Id</span></span>                | <span data-ttu-id="1406b-184">46</span><span class="sxs-lookup"><span data-stu-id="1406b-184">46</span></span>                                    |
| <span data-ttu-id="1406b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-185">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="1406b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="1406b-186">System-Only</span></span>            | <span data-ttu-id="1406b-187">否</span><span class="sxs-lookup"><span data-stu-id="1406b-187">False</span></span>                                 |
| <span data-ttu-id="1406b-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1406b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="1406b-189">對</span><span class="sxs-lookup"><span data-stu-id="1406b-189">True</span></span>                                  |
| <span data-ttu-id="1406b-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1406b-190">Is Indexed</span></span>             | <span data-ttu-id="1406b-191">否</span><span class="sxs-lookup"><span data-stu-id="1406b-191">False</span></span>                                 |
| <span data-ttu-id="1406b-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1406b-192">In Global Catalog</span></span>      | <span data-ttu-id="1406b-193">否</span><span class="sxs-lookup"><span data-stu-id="1406b-193">False</span></span>                                 |
| <span data-ttu-id="1406b-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1406b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="1406b-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1406b-195">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="1406b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1406b-196">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="1406b-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1406b-197">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="1406b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-198">Search-Flags</span></span>           | <span data-ttu-id="1406b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1406b-199">0x00000000</span></span>                            |
| <span data-ttu-id="1406b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-200">System-Flags</span></span>           | <span data-ttu-id="1406b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1406b-201">0x00000010</span></span>                            |
| <span data-ttu-id="1406b-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1406b-202">Classes used in</span></span>        | [<span data-ttu-id="1406b-203">**子**</span><span class="sxs-lookup"><span data-stu-id="1406b-203">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1406b-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1406b-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1406b-205">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-205">Entry</span></span> | <span data-ttu-id="1406b-206">值</span><span class="sxs-lookup"><span data-stu-id="1406b-206">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="1406b-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1406b-207">Link-Id</span></span>                | <span data-ttu-id="1406b-208">46</span><span class="sxs-lookup"><span data-stu-id="1406b-208">46</span></span>                                    |
| <span data-ttu-id="1406b-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-209">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="1406b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="1406b-210">System-Only</span></span>            | <span data-ttu-id="1406b-211">否</span><span class="sxs-lookup"><span data-stu-id="1406b-211">False</span></span>                                 |
| <span data-ttu-id="1406b-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1406b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="1406b-213">對</span><span class="sxs-lookup"><span data-stu-id="1406b-213">True</span></span>                                  |
| <span data-ttu-id="1406b-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1406b-214">Is Indexed</span></span>             | <span data-ttu-id="1406b-215">否</span><span class="sxs-lookup"><span data-stu-id="1406b-215">False</span></span>                                 |
| <span data-ttu-id="1406b-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1406b-216">In Global Catalog</span></span>      | <span data-ttu-id="1406b-217">否</span><span class="sxs-lookup"><span data-stu-id="1406b-217">False</span></span>                                 |
| <span data-ttu-id="1406b-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1406b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="1406b-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1406b-219">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="1406b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1406b-220">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="1406b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1406b-221">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="1406b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-222">Search-Flags</span></span>           | <span data-ttu-id="1406b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1406b-223">0x00000000</span></span>                            |
| <span data-ttu-id="1406b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-224">System-Flags</span></span>           | <span data-ttu-id="1406b-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1406b-225">0x00000010</span></span>                            |
| <span data-ttu-id="1406b-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1406b-226">Classes used in</span></span>        | [<span data-ttu-id="1406b-227">**子**</span><span class="sxs-lookup"><span data-stu-id="1406b-227">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1406b-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1406b-228">Windows Server 2008</span></span>



| <span data-ttu-id="1406b-229">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-229">Entry</span></span> | <span data-ttu-id="1406b-230">值</span><span class="sxs-lookup"><span data-stu-id="1406b-230">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="1406b-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1406b-231">Link-Id</span></span>                | <span data-ttu-id="1406b-232">46</span><span class="sxs-lookup"><span data-stu-id="1406b-232">46</span></span>                                    |
| <span data-ttu-id="1406b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-233">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="1406b-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="1406b-234">System-Only</span></span>            | <span data-ttu-id="1406b-235">否</span><span class="sxs-lookup"><span data-stu-id="1406b-235">False</span></span>                                 |
| <span data-ttu-id="1406b-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1406b-236">Is-Single-Valued</span></span>       | <span data-ttu-id="1406b-237">對</span><span class="sxs-lookup"><span data-stu-id="1406b-237">True</span></span>                                  |
| <span data-ttu-id="1406b-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1406b-238">Is Indexed</span></span>             | <span data-ttu-id="1406b-239">否</span><span class="sxs-lookup"><span data-stu-id="1406b-239">False</span></span>                                 |
| <span data-ttu-id="1406b-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1406b-240">In Global Catalog</span></span>      | <span data-ttu-id="1406b-241">否</span><span class="sxs-lookup"><span data-stu-id="1406b-241">False</span></span>                                 |
| <span data-ttu-id="1406b-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1406b-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="1406b-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1406b-243">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="1406b-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1406b-244">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="1406b-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1406b-245">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="1406b-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-246">Search-Flags</span></span>           | <span data-ttu-id="1406b-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1406b-247">0x00000000</span></span>                            |
| <span data-ttu-id="1406b-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-248">System-Flags</span></span>           | <span data-ttu-id="1406b-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1406b-249">0x00000010</span></span>                            |
| <span data-ttu-id="1406b-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1406b-250">Classes used in</span></span>        | [<span data-ttu-id="1406b-251">**子**</span><span class="sxs-lookup"><span data-stu-id="1406b-251">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1406b-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1406b-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1406b-253">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-253">Entry</span></span> | <span data-ttu-id="1406b-254">值</span><span class="sxs-lookup"><span data-stu-id="1406b-254">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="1406b-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1406b-255">Link-Id</span></span>                | <span data-ttu-id="1406b-256">46</span><span class="sxs-lookup"><span data-stu-id="1406b-256">46</span></span>                                    |
| <span data-ttu-id="1406b-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-257">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="1406b-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="1406b-258">System-Only</span></span>            | <span data-ttu-id="1406b-259">否</span><span class="sxs-lookup"><span data-stu-id="1406b-259">False</span></span>                                 |
| <span data-ttu-id="1406b-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1406b-260">Is-Single-Valued</span></span>       | <span data-ttu-id="1406b-261">對</span><span class="sxs-lookup"><span data-stu-id="1406b-261">True</span></span>                                  |
| <span data-ttu-id="1406b-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1406b-262">Is Indexed</span></span>             | <span data-ttu-id="1406b-263">否</span><span class="sxs-lookup"><span data-stu-id="1406b-263">False</span></span>                                 |
| <span data-ttu-id="1406b-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1406b-264">In Global Catalog</span></span>      | <span data-ttu-id="1406b-265">否</span><span class="sxs-lookup"><span data-stu-id="1406b-265">False</span></span>                                 |
| <span data-ttu-id="1406b-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1406b-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="1406b-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1406b-267">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="1406b-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1406b-268">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="1406b-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1406b-269">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="1406b-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-270">Search-Flags</span></span>           | <span data-ttu-id="1406b-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1406b-271">0x00000000</span></span>                            |
| <span data-ttu-id="1406b-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-272">System-Flags</span></span>           | <span data-ttu-id="1406b-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1406b-273">0x00000010</span></span>                            |
| <span data-ttu-id="1406b-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1406b-274">Classes used in</span></span>        | [<span data-ttu-id="1406b-275">**子**</span><span class="sxs-lookup"><span data-stu-id="1406b-275">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1406b-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1406b-276">Windows Server 2012</span></span>



| <span data-ttu-id="1406b-277">進入</span><span class="sxs-lookup"><span data-stu-id="1406b-277">Entry</span></span> | <span data-ttu-id="1406b-278">值</span><span class="sxs-lookup"><span data-stu-id="1406b-278">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="1406b-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1406b-279">Link-Id</span></span>                | <span data-ttu-id="1406b-280">46</span><span class="sxs-lookup"><span data-stu-id="1406b-280">46</span></span>                                    |
| <span data-ttu-id="1406b-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1406b-281">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="1406b-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="1406b-282">System-Only</span></span>            | <span data-ttu-id="1406b-283">否</span><span class="sxs-lookup"><span data-stu-id="1406b-283">False</span></span>                                 |
| <span data-ttu-id="1406b-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1406b-284">Is-Single-Valued</span></span>       | <span data-ttu-id="1406b-285">對</span><span class="sxs-lookup"><span data-stu-id="1406b-285">True</span></span>                                  |
| <span data-ttu-id="1406b-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1406b-286">Is Indexed</span></span>             | <span data-ttu-id="1406b-287">否</span><span class="sxs-lookup"><span data-stu-id="1406b-287">False</span></span>                                 |
| <span data-ttu-id="1406b-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1406b-288">In Global Catalog</span></span>      | <span data-ttu-id="1406b-289">否</span><span class="sxs-lookup"><span data-stu-id="1406b-289">False</span></span>                                 |
| <span data-ttu-id="1406b-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1406b-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="1406b-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1406b-291">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="1406b-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1406b-292">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="1406b-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1406b-293">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="1406b-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-294">Search-Flags</span></span>           | <span data-ttu-id="1406b-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1406b-295">0x00000000</span></span>                            |
| <span data-ttu-id="1406b-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1406b-296">System-Flags</span></span>           | <span data-ttu-id="1406b-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1406b-297">0x00000010</span></span>                            |
| <span data-ttu-id="1406b-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1406b-298">Classes used in</span></span>        | [<span data-ttu-id="1406b-299">**子**</span><span class="sxs-lookup"><span data-stu-id="1406b-299">**Subnet**</span></span>](c-subnet.md)<br/> |



 

 





