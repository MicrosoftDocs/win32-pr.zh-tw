---
title: Object-Category 屬性
description: 物件類別名稱，用來將這個或衍生類別的物件分組。
ms.assetid: 06fd0314-08b0-49eb-867c-463f7e0afee4
ms.tgt_platform: multiple
keywords:
- Object-Category 屬性 AD 架構
- objectCategory 屬性 AD 架構
topic_type:
- apiref
api_name:
- Object-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b828e4d466b1013ab3854232859a69707553775f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107645"
---
# <a name="object-category-attribute"></a><span data-ttu-id="18bf1-105">Object-Category 屬性</span><span class="sxs-lookup"><span data-stu-id="18bf1-105">Object-Category attribute</span></span>

<span data-ttu-id="18bf1-106">物件類別名稱，用來將這個或衍生類別的物件分組。</span><span class="sxs-lookup"><span data-stu-id="18bf1-106">An object class name used to group objects of this or derived classes.</span></span>



| <span data-ttu-id="18bf1-107">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-107">Entry</span></span> | <span data-ttu-id="18bf1-108">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="18bf1-109">CN</span><span class="sxs-lookup"><span data-stu-id="18bf1-109">CN</span></span>                | <span data-ttu-id="18bf1-110">Object-Category</span><span class="sxs-lookup"><span data-stu-id="18bf1-110">Object-Category</span></span>                                  |
| <span data-ttu-id="18bf1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="18bf1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18bf1-112">objectCategory</span><span class="sxs-lookup"><span data-stu-id="18bf1-112">objectCategory</span></span>                                   |
| <span data-ttu-id="18bf1-113">大小</span><span class="sxs-lookup"><span data-stu-id="18bf1-113">Size</span></span>              | <span data-ttu-id="18bf1-114">平均大約20個位元組。</span><span class="sxs-lookup"><span data-stu-id="18bf1-114">About 20 bytes on average.</span></span>                       |
| <span data-ttu-id="18bf1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="18bf1-115">Update Privilege</span></span>  | <span data-ttu-id="18bf1-116">物件的設計工具會設定此值。</span><span class="sxs-lookup"><span data-stu-id="18bf1-116">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="18bf1-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="18bf1-117">Update Frequency</span></span>  | <span data-ttu-id="18bf1-118">此值永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="18bf1-118">This value should never change.</span></span>                  |
| <span data-ttu-id="18bf1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-119">Attribute-Id</span></span>      | <span data-ttu-id="18bf1-120">1.2.840.113556.1.4.782</span><span class="sxs-lookup"><span data-stu-id="18bf1-120">1.2.840.113556.1.4.782</span></span>                           |
| <span data-ttu-id="18bf1-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="18bf1-121">System-Id-Guid</span></span>    | <span data-ttu-id="18bf1-122">26d97369-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="18bf1-122">26d97369-6070-11d1-a9c6-0000f80367c1</span></span>             |
| <span data-ttu-id="18bf1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="18bf1-123">Syntax</span></span>            | [<span data-ttu-id="18bf1-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="18bf1-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)          |



## <a name="implementations"></a><span data-ttu-id="18bf1-125">實作</span><span class="sxs-lookup"><span data-stu-id="18bf1-125">Implementations</span></span>

-   [<span data-ttu-id="18bf1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="18bf1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="18bf1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18bf1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18bf1-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="18bf1-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="18bf1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18bf1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18bf1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18bf1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18bf1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18bf1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18bf1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18bf1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="18bf1-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18bf1-133">Windows 2000 Server</span></span>



| <span data-ttu-id="18bf1-134">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-134">Entry</span></span> | <span data-ttu-id="18bf1-135">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18bf1-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18bf1-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="18bf1-138">System-Only</span></span>            | <span data-ttu-id="18bf1-139">否</span><span class="sxs-lookup"><span data-stu-id="18bf1-139">False</span></span>                           |
| <span data-ttu-id="18bf1-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18bf1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="18bf1-141">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-141">True</span></span>                            |
| <span data-ttu-id="18bf1-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18bf1-142">Is Indexed</span></span>             | <span data-ttu-id="18bf1-143">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-143">True</span></span>                            |
| <span data-ttu-id="18bf1-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18bf1-144">In Global Catalog</span></span>      | <span data-ttu-id="18bf1-145">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-145">True</span></span>                            |
| <span data-ttu-id="18bf1-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18bf1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="18bf1-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18bf1-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18bf1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18bf1-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18bf1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18bf1-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18bf1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-150">Search-Flags</span></span>           | <span data-ttu-id="18bf1-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18bf1-151">0x00000001</span></span>                      |
| <span data-ttu-id="18bf1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-152">System-Flags</span></span>           | <span data-ttu-id="18bf1-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="18bf1-153">0x00000012</span></span>                      |
| <span data-ttu-id="18bf1-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18bf1-154">Classes used in</span></span>        | [<span data-ttu-id="18bf1-155">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="18bf1-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="18bf1-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18bf1-156">Windows Server 2003</span></span>



| <span data-ttu-id="18bf1-157">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-157">Entry</span></span> | <span data-ttu-id="18bf1-158">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18bf1-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18bf1-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="18bf1-161">System-Only</span></span>            | <span data-ttu-id="18bf1-162">否</span><span class="sxs-lookup"><span data-stu-id="18bf1-162">False</span></span>                           |
| <span data-ttu-id="18bf1-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18bf1-163">Is-Single-Valued</span></span>       | <span data-ttu-id="18bf1-164">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-164">True</span></span>                            |
| <span data-ttu-id="18bf1-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18bf1-165">Is Indexed</span></span>             | <span data-ttu-id="18bf1-166">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-166">True</span></span>                            |
| <span data-ttu-id="18bf1-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18bf1-167">In Global Catalog</span></span>      | <span data-ttu-id="18bf1-168">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-168">True</span></span>                            |
| <span data-ttu-id="18bf1-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18bf1-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="18bf1-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18bf1-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18bf1-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18bf1-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18bf1-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18bf1-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18bf1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-173">Search-Flags</span></span>           | <span data-ttu-id="18bf1-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18bf1-174">0x00000001</span></span>                      |
| <span data-ttu-id="18bf1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-175">System-Flags</span></span>           | <span data-ttu-id="18bf1-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="18bf1-176">0x00000012</span></span>                      |
| <span data-ttu-id="18bf1-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18bf1-177">Classes used in</span></span>        | [<span data-ttu-id="18bf1-178">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="18bf1-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="18bf1-179">亞當</span><span class="sxs-lookup"><span data-stu-id="18bf1-179">ADAM</span></span>



| <span data-ttu-id="18bf1-180">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-180">Entry</span></span> | <span data-ttu-id="18bf1-181">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18bf1-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18bf1-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="18bf1-184">System-Only</span></span>            | <span data-ttu-id="18bf1-185">否</span><span class="sxs-lookup"><span data-stu-id="18bf1-185">False</span></span>                           |
| <span data-ttu-id="18bf1-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18bf1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="18bf1-187">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-187">True</span></span>                            |
| <span data-ttu-id="18bf1-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18bf1-188">Is Indexed</span></span>             | <span data-ttu-id="18bf1-189">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-189">True</span></span>                            |
| <span data-ttu-id="18bf1-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18bf1-190">In Global Catalog</span></span>      | <span data-ttu-id="18bf1-191">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-191">True</span></span>                            |
| <span data-ttu-id="18bf1-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18bf1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="18bf1-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18bf1-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18bf1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18bf1-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18bf1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18bf1-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18bf1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-196">Search-Flags</span></span>           | <span data-ttu-id="18bf1-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18bf1-197">0x00000001</span></span>                      |
| <span data-ttu-id="18bf1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-198">System-Flags</span></span>           | <span data-ttu-id="18bf1-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="18bf1-199">0x00000012</span></span>                      |
| <span data-ttu-id="18bf1-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18bf1-200">Classes used in</span></span>        | [<span data-ttu-id="18bf1-201">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="18bf1-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18bf1-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18bf1-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18bf1-203">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-203">Entry</span></span> | <span data-ttu-id="18bf1-204">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18bf1-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18bf1-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="18bf1-207">System-Only</span></span>            | <span data-ttu-id="18bf1-208">否</span><span class="sxs-lookup"><span data-stu-id="18bf1-208">False</span></span>                           |
| <span data-ttu-id="18bf1-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18bf1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="18bf1-210">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-210">True</span></span>                            |
| <span data-ttu-id="18bf1-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18bf1-211">Is Indexed</span></span>             | <span data-ttu-id="18bf1-212">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-212">True</span></span>                            |
| <span data-ttu-id="18bf1-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18bf1-213">In Global Catalog</span></span>      | <span data-ttu-id="18bf1-214">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-214">True</span></span>                            |
| <span data-ttu-id="18bf1-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18bf1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="18bf1-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18bf1-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18bf1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18bf1-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18bf1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18bf1-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18bf1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-219">Search-Flags</span></span>           | <span data-ttu-id="18bf1-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18bf1-220">0x00000001</span></span>                      |
| <span data-ttu-id="18bf1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-221">System-Flags</span></span>           | <span data-ttu-id="18bf1-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="18bf1-222">0x00000012</span></span>                      |
| <span data-ttu-id="18bf1-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18bf1-223">Classes used in</span></span>        | [<span data-ttu-id="18bf1-224">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="18bf1-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18bf1-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18bf1-225">Windows Server 2008</span></span>



| <span data-ttu-id="18bf1-226">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-226">Entry</span></span> | <span data-ttu-id="18bf1-227">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18bf1-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18bf1-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="18bf1-230">System-Only</span></span>            | <span data-ttu-id="18bf1-231">否</span><span class="sxs-lookup"><span data-stu-id="18bf1-231">False</span></span>                           |
| <span data-ttu-id="18bf1-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18bf1-232">Is-Single-Valued</span></span>       | <span data-ttu-id="18bf1-233">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-233">True</span></span>                            |
| <span data-ttu-id="18bf1-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18bf1-234">Is Indexed</span></span>             | <span data-ttu-id="18bf1-235">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-235">True</span></span>                            |
| <span data-ttu-id="18bf1-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18bf1-236">In Global Catalog</span></span>      | <span data-ttu-id="18bf1-237">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-237">True</span></span>                            |
| <span data-ttu-id="18bf1-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18bf1-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="18bf1-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18bf1-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18bf1-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18bf1-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18bf1-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18bf1-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18bf1-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-242">Search-Flags</span></span>           | <span data-ttu-id="18bf1-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18bf1-243">0x00000001</span></span>                      |
| <span data-ttu-id="18bf1-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-244">System-Flags</span></span>           | <span data-ttu-id="18bf1-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="18bf1-245">0x00000012</span></span>                      |
| <span data-ttu-id="18bf1-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18bf1-246">Classes used in</span></span>        | [<span data-ttu-id="18bf1-247">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="18bf1-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18bf1-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18bf1-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18bf1-249">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-249">Entry</span></span> | <span data-ttu-id="18bf1-250">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18bf1-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18bf1-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="18bf1-253">System-Only</span></span>            | <span data-ttu-id="18bf1-254">否</span><span class="sxs-lookup"><span data-stu-id="18bf1-254">False</span></span>                           |
| <span data-ttu-id="18bf1-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18bf1-255">Is-Single-Valued</span></span>       | <span data-ttu-id="18bf1-256">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-256">True</span></span>                            |
| <span data-ttu-id="18bf1-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18bf1-257">Is Indexed</span></span>             | <span data-ttu-id="18bf1-258">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-258">True</span></span>                            |
| <span data-ttu-id="18bf1-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18bf1-259">In Global Catalog</span></span>      | <span data-ttu-id="18bf1-260">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-260">True</span></span>                            |
| <span data-ttu-id="18bf1-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18bf1-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="18bf1-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18bf1-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18bf1-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18bf1-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18bf1-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18bf1-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18bf1-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-265">Search-Flags</span></span>           | <span data-ttu-id="18bf1-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18bf1-266">0x00000001</span></span>                      |
| <span data-ttu-id="18bf1-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-267">System-Flags</span></span>           | <span data-ttu-id="18bf1-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="18bf1-268">0x00000012</span></span>                      |
| <span data-ttu-id="18bf1-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18bf1-269">Classes used in</span></span>        | [<span data-ttu-id="18bf1-270">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="18bf1-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18bf1-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18bf1-271">Windows Server 2012</span></span>



| <span data-ttu-id="18bf1-272">進入</span><span class="sxs-lookup"><span data-stu-id="18bf1-272">Entry</span></span> | <span data-ttu-id="18bf1-273">值</span><span class="sxs-lookup"><span data-stu-id="18bf1-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18bf1-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="18bf1-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18bf1-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18bf1-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="18bf1-276">System-Only</span></span>            | <span data-ttu-id="18bf1-277">否</span><span class="sxs-lookup"><span data-stu-id="18bf1-277">False</span></span>                           |
| <span data-ttu-id="18bf1-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="18bf1-278">Is-Single-Valued</span></span>       | <span data-ttu-id="18bf1-279">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-279">True</span></span>                            |
| <span data-ttu-id="18bf1-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="18bf1-280">Is Indexed</span></span>             | <span data-ttu-id="18bf1-281">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-281">True</span></span>                            |
| <span data-ttu-id="18bf1-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="18bf1-282">In Global Catalog</span></span>      | <span data-ttu-id="18bf1-283">對</span><span class="sxs-lookup"><span data-stu-id="18bf1-283">True</span></span>                            |
| <span data-ttu-id="18bf1-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="18bf1-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="18bf1-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="18bf1-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18bf1-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18bf1-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18bf1-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18bf1-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18bf1-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-288">Search-Flags</span></span>           | <span data-ttu-id="18bf1-289">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18bf1-289">0x00000001</span></span>                      |
| <span data-ttu-id="18bf1-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18bf1-290">System-Flags</span></span>           | <span data-ttu-id="18bf1-291">0x00000012</span><span class="sxs-lookup"><span data-stu-id="18bf1-291">0x00000012</span></span>                      |
| <span data-ttu-id="18bf1-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="18bf1-292">Classes used in</span></span>        | [<span data-ttu-id="18bf1-293">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="18bf1-293">**Top**</span></span>](c-top.md)<br/> |



 

 





