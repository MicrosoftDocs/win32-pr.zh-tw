---
title: 網站 GUID 屬性
description: 網站的唯一識別碼。
ms.assetid: 1baa967e-5aa3-495f-aa4f-14eac74f70e4
ms.tgt_platform: multiple
keywords:
- 網站 GUID 屬性 AD 架構
- siteGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Site-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3932eb2ced2fe14480010c1120266619cc34456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935349"
---
# <a name="site-guid-attribute"></a><span data-ttu-id="a046b-105">網站 GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="a046b-105">Site-GUID attribute</span></span>

<span data-ttu-id="a046b-106">網站的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a046b-106">The unique identifier for a site.</span></span>



| <span data-ttu-id="a046b-107">進入</span><span class="sxs-lookup"><span data-stu-id="a046b-107">Entry</span></span> | <span data-ttu-id="a046b-108">值</span><span class="sxs-lookup"><span data-stu-id="a046b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a046b-109">CN</span><span class="sxs-lookup"><span data-stu-id="a046b-109">CN</span></span>                | <span data-ttu-id="a046b-110">網站-GUID</span><span class="sxs-lookup"><span data-stu-id="a046b-110">Site-GUID</span></span>                                             |
| <span data-ttu-id="a046b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a046b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a046b-112">siteGUID</span><span class="sxs-lookup"><span data-stu-id="a046b-112">siteGUID</span></span>                                              |
| <span data-ttu-id="a046b-113">大小</span><span class="sxs-lookup"><span data-stu-id="a046b-113">Size</span></span>              | <span data-ttu-id="a046b-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="a046b-114">16 bytes</span></span>                                              |
| <span data-ttu-id="a046b-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a046b-115">Update Privilege</span></span>  | <span data-ttu-id="a046b-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a046b-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="a046b-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a046b-117">Update Frequency</span></span>  | <span data-ttu-id="a046b-118">每次建立新的網站時。</span><span class="sxs-lookup"><span data-stu-id="a046b-118">Whenever a new site is created.</span></span>                       |
| <span data-ttu-id="a046b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a046b-119">Attribute-Id</span></span>      | <span data-ttu-id="a046b-120">1.2.840.113556.1.4.362</span><span class="sxs-lookup"><span data-stu-id="a046b-120">1.2.840.113556.1.4.362</span></span>                                |
| <span data-ttu-id="a046b-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a046b-121">System-Id-Guid</span></span>    | <span data-ttu-id="a046b-122">3e978924-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="a046b-122">3e978924-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="a046b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a046b-123">Syntax</span></span>            | [<span data-ttu-id="a046b-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="a046b-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a046b-125">實作</span><span class="sxs-lookup"><span data-stu-id="a046b-125">Implementations</span></span>

-   [<span data-ttu-id="a046b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a046b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a046b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a046b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a046b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a046b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a046b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a046b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a046b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a046b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a046b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a046b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a046b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a046b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a046b-133">進入</span><span class="sxs-lookup"><span data-stu-id="a046b-133">Entry</span></span> | <span data-ttu-id="a046b-134">值</span><span class="sxs-lookup"><span data-stu-id="a046b-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a046b-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a046b-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a046b-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a046b-137">System-Only</span></span>            | <span data-ttu-id="a046b-138">否</span><span class="sxs-lookup"><span data-stu-id="a046b-138">False</span></span>                                     |
| <span data-ttu-id="a046b-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a046b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a046b-140">對</span><span class="sxs-lookup"><span data-stu-id="a046b-140">True</span></span>                                      |
| <span data-ttu-id="a046b-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a046b-141">Is Indexed</span></span>             | <span data-ttu-id="a046b-142">否</span><span class="sxs-lookup"><span data-stu-id="a046b-142">False</span></span>                                     |
| <span data-ttu-id="a046b-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a046b-143">In Global Catalog</span></span>      | <span data-ttu-id="a046b-144">否</span><span class="sxs-lookup"><span data-stu-id="a046b-144">False</span></span>                                     |
| <span data-ttu-id="a046b-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a046b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a046b-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a046b-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a046b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a046b-147">Range-Lower</span></span>            | <span data-ttu-id="a046b-148">16</span><span class="sxs-lookup"><span data-stu-id="a046b-148">16</span></span>                                        |
| <span data-ttu-id="a046b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a046b-149">Range-Upper</span></span>            | <span data-ttu-id="a046b-150">16</span><span class="sxs-lookup"><span data-stu-id="a046b-150">16</span></span>                                        |
| <span data-ttu-id="a046b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-151">Search-Flags</span></span>           | <span data-ttu-id="a046b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a046b-152">0x00000000</span></span>                                |
| <span data-ttu-id="a046b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-153">System-Flags</span></span>           | <span data-ttu-id="a046b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a046b-154">0x00000010</span></span>                                |
| <span data-ttu-id="a046b-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a046b-155">Classes used in</span></span>        | [<span data-ttu-id="a046b-156">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a046b-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a046b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a046b-157">Windows Server 2003</span></span>



| <span data-ttu-id="a046b-158">進入</span><span class="sxs-lookup"><span data-stu-id="a046b-158">Entry</span></span> | <span data-ttu-id="a046b-159">值</span><span class="sxs-lookup"><span data-stu-id="a046b-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a046b-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a046b-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a046b-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a046b-162">System-Only</span></span>            | <span data-ttu-id="a046b-163">否</span><span class="sxs-lookup"><span data-stu-id="a046b-163">False</span></span>                                     |
| <span data-ttu-id="a046b-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a046b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a046b-165">對</span><span class="sxs-lookup"><span data-stu-id="a046b-165">True</span></span>                                      |
| <span data-ttu-id="a046b-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a046b-166">Is Indexed</span></span>             | <span data-ttu-id="a046b-167">否</span><span class="sxs-lookup"><span data-stu-id="a046b-167">False</span></span>                                     |
| <span data-ttu-id="a046b-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a046b-168">In Global Catalog</span></span>      | <span data-ttu-id="a046b-169">否</span><span class="sxs-lookup"><span data-stu-id="a046b-169">False</span></span>                                     |
| <span data-ttu-id="a046b-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a046b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a046b-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a046b-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a046b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a046b-172">Range-Lower</span></span>            | <span data-ttu-id="a046b-173">16</span><span class="sxs-lookup"><span data-stu-id="a046b-173">16</span></span>                                        |
| <span data-ttu-id="a046b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a046b-174">Range-Upper</span></span>            | <span data-ttu-id="a046b-175">16</span><span class="sxs-lookup"><span data-stu-id="a046b-175">16</span></span>                                        |
| <span data-ttu-id="a046b-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-176">Search-Flags</span></span>           | <span data-ttu-id="a046b-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a046b-177">0x00000000</span></span>                                |
| <span data-ttu-id="a046b-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-178">System-Flags</span></span>           | <span data-ttu-id="a046b-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a046b-179">0x00000010</span></span>                                |
| <span data-ttu-id="a046b-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a046b-180">Classes used in</span></span>        | [<span data-ttu-id="a046b-181">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a046b-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a046b-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a046b-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a046b-183">進入</span><span class="sxs-lookup"><span data-stu-id="a046b-183">Entry</span></span> | <span data-ttu-id="a046b-184">值</span><span class="sxs-lookup"><span data-stu-id="a046b-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a046b-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a046b-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a046b-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="a046b-187">System-Only</span></span>            | <span data-ttu-id="a046b-188">否</span><span class="sxs-lookup"><span data-stu-id="a046b-188">False</span></span>                                     |
| <span data-ttu-id="a046b-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a046b-189">Is-Single-Valued</span></span>       | <span data-ttu-id="a046b-190">對</span><span class="sxs-lookup"><span data-stu-id="a046b-190">True</span></span>                                      |
| <span data-ttu-id="a046b-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a046b-191">Is Indexed</span></span>             | <span data-ttu-id="a046b-192">否</span><span class="sxs-lookup"><span data-stu-id="a046b-192">False</span></span>                                     |
| <span data-ttu-id="a046b-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a046b-193">In Global Catalog</span></span>      | <span data-ttu-id="a046b-194">否</span><span class="sxs-lookup"><span data-stu-id="a046b-194">False</span></span>                                     |
| <span data-ttu-id="a046b-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a046b-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="a046b-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a046b-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a046b-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a046b-197">Range-Lower</span></span>            | <span data-ttu-id="a046b-198">16</span><span class="sxs-lookup"><span data-stu-id="a046b-198">16</span></span>                                        |
| <span data-ttu-id="a046b-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a046b-199">Range-Upper</span></span>            | <span data-ttu-id="a046b-200">16</span><span class="sxs-lookup"><span data-stu-id="a046b-200">16</span></span>                                        |
| <span data-ttu-id="a046b-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-201">Search-Flags</span></span>           | <span data-ttu-id="a046b-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a046b-202">0x00000000</span></span>                                |
| <span data-ttu-id="a046b-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-203">System-Flags</span></span>           | <span data-ttu-id="a046b-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a046b-204">0x00000010</span></span>                                |
| <span data-ttu-id="a046b-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a046b-205">Classes used in</span></span>        | [<span data-ttu-id="a046b-206">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a046b-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a046b-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a046b-207">Windows Server 2008</span></span>



| <span data-ttu-id="a046b-208">進入</span><span class="sxs-lookup"><span data-stu-id="a046b-208">Entry</span></span> | <span data-ttu-id="a046b-209">值</span><span class="sxs-lookup"><span data-stu-id="a046b-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a046b-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a046b-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a046b-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="a046b-212">System-Only</span></span>            | <span data-ttu-id="a046b-213">否</span><span class="sxs-lookup"><span data-stu-id="a046b-213">False</span></span>                                     |
| <span data-ttu-id="a046b-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a046b-214">Is-Single-Valued</span></span>       | <span data-ttu-id="a046b-215">對</span><span class="sxs-lookup"><span data-stu-id="a046b-215">True</span></span>                                      |
| <span data-ttu-id="a046b-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a046b-216">Is Indexed</span></span>             | <span data-ttu-id="a046b-217">否</span><span class="sxs-lookup"><span data-stu-id="a046b-217">False</span></span>                                     |
| <span data-ttu-id="a046b-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a046b-218">In Global Catalog</span></span>      | <span data-ttu-id="a046b-219">否</span><span class="sxs-lookup"><span data-stu-id="a046b-219">False</span></span>                                     |
| <span data-ttu-id="a046b-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a046b-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="a046b-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a046b-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a046b-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a046b-222">Range-Lower</span></span>            | <span data-ttu-id="a046b-223">16</span><span class="sxs-lookup"><span data-stu-id="a046b-223">16</span></span>                                        |
| <span data-ttu-id="a046b-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a046b-224">Range-Upper</span></span>            | <span data-ttu-id="a046b-225">16</span><span class="sxs-lookup"><span data-stu-id="a046b-225">16</span></span>                                        |
| <span data-ttu-id="a046b-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-226">Search-Flags</span></span>           | <span data-ttu-id="a046b-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a046b-227">0x00000000</span></span>                                |
| <span data-ttu-id="a046b-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-228">System-Flags</span></span>           | <span data-ttu-id="a046b-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a046b-229">0x00000010</span></span>                                |
| <span data-ttu-id="a046b-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a046b-230">Classes used in</span></span>        | [<span data-ttu-id="a046b-231">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a046b-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a046b-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a046b-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a046b-233">進入</span><span class="sxs-lookup"><span data-stu-id="a046b-233">Entry</span></span> | <span data-ttu-id="a046b-234">值</span><span class="sxs-lookup"><span data-stu-id="a046b-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a046b-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a046b-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a046b-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="a046b-237">System-Only</span></span>            | <span data-ttu-id="a046b-238">否</span><span class="sxs-lookup"><span data-stu-id="a046b-238">False</span></span>                                     |
| <span data-ttu-id="a046b-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a046b-239">Is-Single-Valued</span></span>       | <span data-ttu-id="a046b-240">對</span><span class="sxs-lookup"><span data-stu-id="a046b-240">True</span></span>                                      |
| <span data-ttu-id="a046b-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a046b-241">Is Indexed</span></span>             | <span data-ttu-id="a046b-242">否</span><span class="sxs-lookup"><span data-stu-id="a046b-242">False</span></span>                                     |
| <span data-ttu-id="a046b-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a046b-243">In Global Catalog</span></span>      | <span data-ttu-id="a046b-244">否</span><span class="sxs-lookup"><span data-stu-id="a046b-244">False</span></span>                                     |
| <span data-ttu-id="a046b-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a046b-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="a046b-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a046b-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a046b-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a046b-247">Range-Lower</span></span>            | <span data-ttu-id="a046b-248">16</span><span class="sxs-lookup"><span data-stu-id="a046b-248">16</span></span>                                        |
| <span data-ttu-id="a046b-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a046b-249">Range-Upper</span></span>            | <span data-ttu-id="a046b-250">16</span><span class="sxs-lookup"><span data-stu-id="a046b-250">16</span></span>                                        |
| <span data-ttu-id="a046b-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-251">Search-Flags</span></span>           | <span data-ttu-id="a046b-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a046b-252">0x00000000</span></span>                                |
| <span data-ttu-id="a046b-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-253">System-Flags</span></span>           | <span data-ttu-id="a046b-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a046b-254">0x00000010</span></span>                                |
| <span data-ttu-id="a046b-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a046b-255">Classes used in</span></span>        | [<span data-ttu-id="a046b-256">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a046b-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a046b-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a046b-257">Windows Server 2012</span></span>



| <span data-ttu-id="a046b-258">進入</span><span class="sxs-lookup"><span data-stu-id="a046b-258">Entry</span></span> | <span data-ttu-id="a046b-259">值</span><span class="sxs-lookup"><span data-stu-id="a046b-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a046b-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a046b-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a046b-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a046b-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="a046b-262">System-Only</span></span>            | <span data-ttu-id="a046b-263">否</span><span class="sxs-lookup"><span data-stu-id="a046b-263">False</span></span>                                     |
| <span data-ttu-id="a046b-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a046b-264">Is-Single-Valued</span></span>       | <span data-ttu-id="a046b-265">對</span><span class="sxs-lookup"><span data-stu-id="a046b-265">True</span></span>                                      |
| <span data-ttu-id="a046b-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a046b-266">Is Indexed</span></span>             | <span data-ttu-id="a046b-267">否</span><span class="sxs-lookup"><span data-stu-id="a046b-267">False</span></span>                                     |
| <span data-ttu-id="a046b-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a046b-268">In Global Catalog</span></span>      | <span data-ttu-id="a046b-269">否</span><span class="sxs-lookup"><span data-stu-id="a046b-269">False</span></span>                                     |
| <span data-ttu-id="a046b-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a046b-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="a046b-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a046b-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a046b-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a046b-272">Range-Lower</span></span>            | <span data-ttu-id="a046b-273">16</span><span class="sxs-lookup"><span data-stu-id="a046b-273">16</span></span>                                        |
| <span data-ttu-id="a046b-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a046b-274">Range-Upper</span></span>            | <span data-ttu-id="a046b-275">16</span><span class="sxs-lookup"><span data-stu-id="a046b-275">16</span></span>                                        |
| <span data-ttu-id="a046b-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-276">Search-Flags</span></span>           | <span data-ttu-id="a046b-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a046b-277">0x00000000</span></span>                                |
| <span data-ttu-id="a046b-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a046b-278">System-Flags</span></span>           | <span data-ttu-id="a046b-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a046b-279">0x00000010</span></span>                                |
| <span data-ttu-id="a046b-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a046b-280">Classes used in</span></span>        | [<span data-ttu-id="a046b-281">**電腦**</span><span class="sxs-lookup"><span data-stu-id="a046b-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





