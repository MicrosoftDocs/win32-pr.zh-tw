---
title: 預設-物件-類別目錄屬性
description: 如果未指定物件，則為物件使用的物件類別。
ms.assetid: ebb99527-8d4e-4c11-a16d-2145d9cce566
ms.tgt_platform: multiple
keywords:
- 預設-物件-類別目錄屬性 AD 架構
- defaultObjectCategory 屬性 AD 架構
topic_type:
- apiref
api_name:
- Default-Object-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290a9a8c7c1f930a9115d02d6bab7c968ecbdc86
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970469"
---
# <a name="default-object-category-attribute"></a><span data-ttu-id="32a02-105">預設-物件-類別目錄屬性</span><span class="sxs-lookup"><span data-stu-id="32a02-105">Default-Object-Category attribute</span></span>

<span data-ttu-id="32a02-106">如果未指定物件，則為物件使用的物件類別。</span><span class="sxs-lookup"><span data-stu-id="32a02-106">The object category to use for the object if one is not specified.</span></span>



| <span data-ttu-id="32a02-107">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-107">Entry</span></span> | <span data-ttu-id="32a02-108">值</span><span class="sxs-lookup"><span data-stu-id="32a02-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="32a02-109">CN</span><span class="sxs-lookup"><span data-stu-id="32a02-109">CN</span></span>                | <span data-ttu-id="32a02-110">預設-物件-類別</span><span class="sxs-lookup"><span data-stu-id="32a02-110">Default-Object-Category</span></span>                 |
| <span data-ttu-id="32a02-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="32a02-111">Ldap-Display-Name</span></span> | <span data-ttu-id="32a02-112">defaultObjectCategory</span><span class="sxs-lookup"><span data-stu-id="32a02-112">defaultObjectCategory</span></span>                   |
| <span data-ttu-id="32a02-113">大小</span><span class="sxs-lookup"><span data-stu-id="32a02-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="32a02-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="32a02-114">Update Privilege</span></span>  | <span data-ttu-id="32a02-115">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="32a02-115">Schema administrator</span></span>                    |
| <span data-ttu-id="32a02-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="32a02-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="32a02-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-117">Attribute-Id</span></span>      | <span data-ttu-id="32a02-118">1.2.840.113556.1.4.783</span><span class="sxs-lookup"><span data-stu-id="32a02-118">1.2.840.113556.1.4.783</span></span>                  |
| <span data-ttu-id="32a02-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="32a02-119">System-Id-Guid</span></span>    | <span data-ttu-id="32a02-120">26d97367-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="32a02-120">26d97367-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="32a02-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="32a02-121">Syntax</span></span>            | [<span data-ttu-id="32a02-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="32a02-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="32a02-123">實作</span><span class="sxs-lookup"><span data-stu-id="32a02-123">Implementations</span></span>

-   [<span data-ttu-id="32a02-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="32a02-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="32a02-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="32a02-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="32a02-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="32a02-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="32a02-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="32a02-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="32a02-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="32a02-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="32a02-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="32a02-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="32a02-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="32a02-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="32a02-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32a02-131">Windows 2000 Server</span></span>



| <span data-ttu-id="32a02-132">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-132">Entry</span></span> | <span data-ttu-id="32a02-133">值</span><span class="sxs-lookup"><span data-stu-id="32a02-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="32a02-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32a02-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a02-136">System-Only</span></span>            | <span data-ttu-id="32a02-137">否</span><span class="sxs-lookup"><span data-stu-id="32a02-137">False</span></span>                                            |
| <span data-ttu-id="32a02-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32a02-138">Is-Single-Valued</span></span>       | <span data-ttu-id="32a02-139">對</span><span class="sxs-lookup"><span data-stu-id="32a02-139">True</span></span>                                             |
| <span data-ttu-id="32a02-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32a02-140">Is Indexed</span></span>             | <span data-ttu-id="32a02-141">否</span><span class="sxs-lookup"><span data-stu-id="32a02-141">False</span></span>                                            |
| <span data-ttu-id="32a02-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32a02-142">In Global Catalog</span></span>      | <span data-ttu-id="32a02-143">否</span><span class="sxs-lookup"><span data-stu-id="32a02-143">False</span></span>                                            |
| <span data-ttu-id="32a02-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32a02-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a02-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32a02-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="32a02-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a02-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="32a02-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a02-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="32a02-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-148">Search-Flags</span></span>           | <span data-ttu-id="32a02-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a02-149">0x00000000</span></span>                                       |
| <span data-ttu-id="32a02-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-150">System-Flags</span></span>           | <span data-ttu-id="32a02-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a02-151">0x00000010</span></span>                                       |
| <span data-ttu-id="32a02-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32a02-152">Classes used in</span></span>        | [<span data-ttu-id="32a02-153">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="32a02-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="32a02-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32a02-154">Windows Server 2003</span></span>



| <span data-ttu-id="32a02-155">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-155">Entry</span></span> | <span data-ttu-id="32a02-156">值</span><span class="sxs-lookup"><span data-stu-id="32a02-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="32a02-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32a02-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a02-159">System-Only</span></span>            | <span data-ttu-id="32a02-160">否</span><span class="sxs-lookup"><span data-stu-id="32a02-160">False</span></span>                                            |
| <span data-ttu-id="32a02-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32a02-161">Is-Single-Valued</span></span>       | <span data-ttu-id="32a02-162">對</span><span class="sxs-lookup"><span data-stu-id="32a02-162">True</span></span>                                             |
| <span data-ttu-id="32a02-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32a02-163">Is Indexed</span></span>             | <span data-ttu-id="32a02-164">否</span><span class="sxs-lookup"><span data-stu-id="32a02-164">False</span></span>                                            |
| <span data-ttu-id="32a02-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32a02-165">In Global Catalog</span></span>      | <span data-ttu-id="32a02-166">否</span><span class="sxs-lookup"><span data-stu-id="32a02-166">False</span></span>                                            |
| <span data-ttu-id="32a02-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32a02-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a02-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32a02-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="32a02-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a02-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="32a02-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a02-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="32a02-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-171">Search-Flags</span></span>           | <span data-ttu-id="32a02-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a02-172">0x00000000</span></span>                                       |
| <span data-ttu-id="32a02-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-173">System-Flags</span></span>           | <span data-ttu-id="32a02-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a02-174">0x00000010</span></span>                                       |
| <span data-ttu-id="32a02-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32a02-175">Classes used in</span></span>        | [<span data-ttu-id="32a02-176">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="32a02-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="32a02-177">亞當</span><span class="sxs-lookup"><span data-stu-id="32a02-177">ADAM</span></span>



| <span data-ttu-id="32a02-178">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-178">Entry</span></span> | <span data-ttu-id="32a02-179">值</span><span class="sxs-lookup"><span data-stu-id="32a02-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="32a02-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32a02-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a02-182">System-Only</span></span>            | <span data-ttu-id="32a02-183">否</span><span class="sxs-lookup"><span data-stu-id="32a02-183">False</span></span>                                            |
| <span data-ttu-id="32a02-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32a02-184">Is-Single-Valued</span></span>       | <span data-ttu-id="32a02-185">對</span><span class="sxs-lookup"><span data-stu-id="32a02-185">True</span></span>                                             |
| <span data-ttu-id="32a02-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32a02-186">Is Indexed</span></span>             | <span data-ttu-id="32a02-187">否</span><span class="sxs-lookup"><span data-stu-id="32a02-187">False</span></span>                                            |
| <span data-ttu-id="32a02-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32a02-188">In Global Catalog</span></span>      | <span data-ttu-id="32a02-189">否</span><span class="sxs-lookup"><span data-stu-id="32a02-189">False</span></span>                                            |
| <span data-ttu-id="32a02-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32a02-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a02-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32a02-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="32a02-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a02-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="32a02-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a02-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="32a02-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-194">Search-Flags</span></span>           | <span data-ttu-id="32a02-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a02-195">0x00000000</span></span>                                       |
| <span data-ttu-id="32a02-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-196">System-Flags</span></span>           | <span data-ttu-id="32a02-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a02-197">0x00000010</span></span>                                       |
| <span data-ttu-id="32a02-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32a02-198">Classes used in</span></span>        | [<span data-ttu-id="32a02-199">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="32a02-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="32a02-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="32a02-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="32a02-201">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-201">Entry</span></span> | <span data-ttu-id="32a02-202">值</span><span class="sxs-lookup"><span data-stu-id="32a02-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="32a02-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32a02-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a02-205">System-Only</span></span>            | <span data-ttu-id="32a02-206">否</span><span class="sxs-lookup"><span data-stu-id="32a02-206">False</span></span>                                            |
| <span data-ttu-id="32a02-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32a02-207">Is-Single-Valued</span></span>       | <span data-ttu-id="32a02-208">對</span><span class="sxs-lookup"><span data-stu-id="32a02-208">True</span></span>                                             |
| <span data-ttu-id="32a02-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32a02-209">Is Indexed</span></span>             | <span data-ttu-id="32a02-210">否</span><span class="sxs-lookup"><span data-stu-id="32a02-210">False</span></span>                                            |
| <span data-ttu-id="32a02-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32a02-211">In Global Catalog</span></span>      | <span data-ttu-id="32a02-212">否</span><span class="sxs-lookup"><span data-stu-id="32a02-212">False</span></span>                                            |
| <span data-ttu-id="32a02-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32a02-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a02-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32a02-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="32a02-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a02-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="32a02-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a02-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="32a02-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-217">Search-Flags</span></span>           | <span data-ttu-id="32a02-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a02-218">0x00000000</span></span>                                       |
| <span data-ttu-id="32a02-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-219">System-Flags</span></span>           | <span data-ttu-id="32a02-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a02-220">0x00000010</span></span>                                       |
| <span data-ttu-id="32a02-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32a02-221">Classes used in</span></span>        | [<span data-ttu-id="32a02-222">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="32a02-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="32a02-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32a02-223">Windows Server 2008</span></span>



| <span data-ttu-id="32a02-224">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-224">Entry</span></span> | <span data-ttu-id="32a02-225">值</span><span class="sxs-lookup"><span data-stu-id="32a02-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="32a02-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32a02-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a02-228">System-Only</span></span>            | <span data-ttu-id="32a02-229">否</span><span class="sxs-lookup"><span data-stu-id="32a02-229">False</span></span>                                            |
| <span data-ttu-id="32a02-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32a02-230">Is-Single-Valued</span></span>       | <span data-ttu-id="32a02-231">對</span><span class="sxs-lookup"><span data-stu-id="32a02-231">True</span></span>                                             |
| <span data-ttu-id="32a02-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32a02-232">Is Indexed</span></span>             | <span data-ttu-id="32a02-233">否</span><span class="sxs-lookup"><span data-stu-id="32a02-233">False</span></span>                                            |
| <span data-ttu-id="32a02-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32a02-234">In Global Catalog</span></span>      | <span data-ttu-id="32a02-235">否</span><span class="sxs-lookup"><span data-stu-id="32a02-235">False</span></span>                                            |
| <span data-ttu-id="32a02-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32a02-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a02-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32a02-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="32a02-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a02-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="32a02-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a02-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="32a02-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-240">Search-Flags</span></span>           | <span data-ttu-id="32a02-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a02-241">0x00000000</span></span>                                       |
| <span data-ttu-id="32a02-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-242">System-Flags</span></span>           | <span data-ttu-id="32a02-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a02-243">0x00000010</span></span>                                       |
| <span data-ttu-id="32a02-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32a02-244">Classes used in</span></span>        | [<span data-ttu-id="32a02-245">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="32a02-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="32a02-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32a02-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="32a02-247">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-247">Entry</span></span> | <span data-ttu-id="32a02-248">值</span><span class="sxs-lookup"><span data-stu-id="32a02-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="32a02-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32a02-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a02-251">System-Only</span></span>            | <span data-ttu-id="32a02-252">否</span><span class="sxs-lookup"><span data-stu-id="32a02-252">False</span></span>                                            |
| <span data-ttu-id="32a02-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32a02-253">Is-Single-Valued</span></span>       | <span data-ttu-id="32a02-254">對</span><span class="sxs-lookup"><span data-stu-id="32a02-254">True</span></span>                                             |
| <span data-ttu-id="32a02-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32a02-255">Is Indexed</span></span>             | <span data-ttu-id="32a02-256">否</span><span class="sxs-lookup"><span data-stu-id="32a02-256">False</span></span>                                            |
| <span data-ttu-id="32a02-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32a02-257">In Global Catalog</span></span>      | <span data-ttu-id="32a02-258">否</span><span class="sxs-lookup"><span data-stu-id="32a02-258">False</span></span>                                            |
| <span data-ttu-id="32a02-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32a02-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a02-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32a02-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="32a02-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a02-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="32a02-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a02-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="32a02-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-263">Search-Flags</span></span>           | <span data-ttu-id="32a02-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a02-264">0x00000000</span></span>                                       |
| <span data-ttu-id="32a02-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-265">System-Flags</span></span>           | <span data-ttu-id="32a02-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a02-266">0x00000010</span></span>                                       |
| <span data-ttu-id="32a02-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32a02-267">Classes used in</span></span>        | [<span data-ttu-id="32a02-268">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="32a02-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="32a02-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32a02-269">Windows Server 2012</span></span>



| <span data-ttu-id="32a02-270">進入</span><span class="sxs-lookup"><span data-stu-id="32a02-270">Entry</span></span> | <span data-ttu-id="32a02-271">值</span><span class="sxs-lookup"><span data-stu-id="32a02-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="32a02-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32a02-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a02-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="32a02-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a02-274">System-Only</span></span>            | <span data-ttu-id="32a02-275">否</span><span class="sxs-lookup"><span data-stu-id="32a02-275">False</span></span>                                            |
| <span data-ttu-id="32a02-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32a02-276">Is-Single-Valued</span></span>       | <span data-ttu-id="32a02-277">對</span><span class="sxs-lookup"><span data-stu-id="32a02-277">True</span></span>                                             |
| <span data-ttu-id="32a02-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32a02-278">Is Indexed</span></span>             | <span data-ttu-id="32a02-279">否</span><span class="sxs-lookup"><span data-stu-id="32a02-279">False</span></span>                                            |
| <span data-ttu-id="32a02-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32a02-280">In Global Catalog</span></span>      | <span data-ttu-id="32a02-281">否</span><span class="sxs-lookup"><span data-stu-id="32a02-281">False</span></span>                                            |
| <span data-ttu-id="32a02-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32a02-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a02-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32a02-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="32a02-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a02-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="32a02-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a02-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="32a02-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-286">Search-Flags</span></span>           | <span data-ttu-id="32a02-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a02-287">0x00000000</span></span>                                       |
| <span data-ttu-id="32a02-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a02-288">System-Flags</span></span>           | <span data-ttu-id="32a02-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a02-289">0x00000010</span></span>                                       |
| <span data-ttu-id="32a02-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32a02-290">Classes used in</span></span>        | [<span data-ttu-id="32a02-291">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="32a02-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





