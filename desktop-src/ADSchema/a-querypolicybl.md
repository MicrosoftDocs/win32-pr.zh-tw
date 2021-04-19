---
title: 查詢原則-BL 屬性
description: 保留指定查詢-原則參考的所有物件清單。
ms.assetid: af421d00-2cc8-4ea1-8374-148db58c493b
ms.tgt_platform: multiple
keywords:
- BL 屬性 AD 架構的查詢原則
- queryPolicyBL 屬性 AD 架構
topic_type:
- apiref
api_name:
- Query-Policy-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739abe3dbf67e5e8d154ef1424db81476f153858
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106968404"
---
# <a name="query-policy-bl-attribute"></a><span data-ttu-id="6499c-105">查詢原則-BL 屬性</span><span class="sxs-lookup"><span data-stu-id="6499c-105">Query-Policy-BL attribute</span></span>

<span data-ttu-id="6499c-106">保留指定查詢-原則參考的所有物件清單。</span><span class="sxs-lookup"><span data-stu-id="6499c-106">List of all objects holding references to a given Query-Policy.</span></span>



| <span data-ttu-id="6499c-107">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-107">Entry</span></span> | <span data-ttu-id="6499c-108">值</span><span class="sxs-lookup"><span data-stu-id="6499c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6499c-109">CN</span><span class="sxs-lookup"><span data-stu-id="6499c-109">CN</span></span>                | <span data-ttu-id="6499c-110">查詢-原則-BL</span><span class="sxs-lookup"><span data-stu-id="6499c-110">Query-Policy-BL</span></span>                         |
| <span data-ttu-id="6499c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6499c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6499c-112">queryPolicyBL</span><span class="sxs-lookup"><span data-stu-id="6499c-112">queryPolicyBL</span></span>                           |
| <span data-ttu-id="6499c-113">大小</span><span class="sxs-lookup"><span data-stu-id="6499c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="6499c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6499c-114">Update Privilege</span></span>  | <span data-ttu-id="6499c-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="6499c-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="6499c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6499c-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="6499c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-117">Attribute-Id</span></span>      | <span data-ttu-id="6499c-118">1.2.840.113556.1.4.608</span><span class="sxs-lookup"><span data-stu-id="6499c-118">1.2.840.113556.1.4.608</span></span>                  |
| <span data-ttu-id="6499c-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6499c-119">System-Id-Guid</span></span>    | <span data-ttu-id="6499c-120">e1aea404-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6499c-120">e1aea404-cd5b-11d0-afff-0000f80367c1</span></span>    |
| <span data-ttu-id="6499c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="6499c-121">Syntax</span></span>            | [<span data-ttu-id="6499c-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6499c-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="6499c-123">實作</span><span class="sxs-lookup"><span data-stu-id="6499c-123">Implementations</span></span>

-   [<span data-ttu-id="6499c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6499c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6499c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6499c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6499c-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6499c-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6499c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6499c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6499c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6499c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6499c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6499c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6499c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6499c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6499c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6499c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6499c-132">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-132">Entry</span></span> | <span data-ttu-id="6499c-133">值</span><span class="sxs-lookup"><span data-stu-id="6499c-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6499c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6499c-134">Link-Id</span></span>                | <span data-ttu-id="6499c-135">69</span><span class="sxs-lookup"><span data-stu-id="6499c-135">69</span></span>                              |
| <span data-ttu-id="6499c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6499c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6499c-137">System-Only</span></span>            | <span data-ttu-id="6499c-138">對</span><span class="sxs-lookup"><span data-stu-id="6499c-138">True</span></span>                            |
| <span data-ttu-id="6499c-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6499c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6499c-140">否</span><span class="sxs-lookup"><span data-stu-id="6499c-140">False</span></span>                           |
| <span data-ttu-id="6499c-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6499c-141">Is Indexed</span></span>             | <span data-ttu-id="6499c-142">否</span><span class="sxs-lookup"><span data-stu-id="6499c-142">False</span></span>                           |
| <span data-ttu-id="6499c-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6499c-143">In Global Catalog</span></span>      | <span data-ttu-id="6499c-144">否</span><span class="sxs-lookup"><span data-stu-id="6499c-144">False</span></span>                           |
| <span data-ttu-id="6499c-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6499c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6499c-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6499c-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6499c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6499c-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6499c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6499c-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6499c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-149">Search-Flags</span></span>           | <span data-ttu-id="6499c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6499c-150">0x00000000</span></span>                      |
| <span data-ttu-id="6499c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-151">System-Flags</span></span>           | <span data-ttu-id="6499c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6499c-152">0x00000010</span></span>                      |
| <span data-ttu-id="6499c-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6499c-153">Classes used in</span></span>        | [<span data-ttu-id="6499c-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6499c-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6499c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6499c-155">Windows Server 2003</span></span>



| <span data-ttu-id="6499c-156">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-156">Entry</span></span> | <span data-ttu-id="6499c-157">值</span><span class="sxs-lookup"><span data-stu-id="6499c-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6499c-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6499c-158">Link-Id</span></span>                | <span data-ttu-id="6499c-159">69</span><span class="sxs-lookup"><span data-stu-id="6499c-159">69</span></span>                              |
| <span data-ttu-id="6499c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6499c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6499c-161">System-Only</span></span>            | <span data-ttu-id="6499c-162">對</span><span class="sxs-lookup"><span data-stu-id="6499c-162">True</span></span>                            |
| <span data-ttu-id="6499c-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6499c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6499c-164">否</span><span class="sxs-lookup"><span data-stu-id="6499c-164">False</span></span>                           |
| <span data-ttu-id="6499c-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6499c-165">Is Indexed</span></span>             | <span data-ttu-id="6499c-166">否</span><span class="sxs-lookup"><span data-stu-id="6499c-166">False</span></span>                           |
| <span data-ttu-id="6499c-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6499c-167">In Global Catalog</span></span>      | <span data-ttu-id="6499c-168">否</span><span class="sxs-lookup"><span data-stu-id="6499c-168">False</span></span>                           |
| <span data-ttu-id="6499c-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6499c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6499c-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6499c-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6499c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6499c-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6499c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6499c-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6499c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-173">Search-Flags</span></span>           | <span data-ttu-id="6499c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6499c-174">0x00000000</span></span>                      |
| <span data-ttu-id="6499c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-175">System-Flags</span></span>           | <span data-ttu-id="6499c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6499c-176">0x00000010</span></span>                      |
| <span data-ttu-id="6499c-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6499c-177">Classes used in</span></span>        | [<span data-ttu-id="6499c-178">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6499c-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6499c-179">亞當</span><span class="sxs-lookup"><span data-stu-id="6499c-179">ADAM</span></span>



| <span data-ttu-id="6499c-180">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-180">Entry</span></span> | <span data-ttu-id="6499c-181">值</span><span class="sxs-lookup"><span data-stu-id="6499c-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6499c-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6499c-182">Link-Id</span></span>                | <span data-ttu-id="6499c-183">69</span><span class="sxs-lookup"><span data-stu-id="6499c-183">69</span></span>                              |
| <span data-ttu-id="6499c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6499c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6499c-185">System-Only</span></span>            | <span data-ttu-id="6499c-186">對</span><span class="sxs-lookup"><span data-stu-id="6499c-186">True</span></span>                            |
| <span data-ttu-id="6499c-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6499c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6499c-188">否</span><span class="sxs-lookup"><span data-stu-id="6499c-188">False</span></span>                           |
| <span data-ttu-id="6499c-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6499c-189">Is Indexed</span></span>             | <span data-ttu-id="6499c-190">否</span><span class="sxs-lookup"><span data-stu-id="6499c-190">False</span></span>                           |
| <span data-ttu-id="6499c-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6499c-191">In Global Catalog</span></span>      | <span data-ttu-id="6499c-192">否</span><span class="sxs-lookup"><span data-stu-id="6499c-192">False</span></span>                           |
| <span data-ttu-id="6499c-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6499c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6499c-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6499c-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6499c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6499c-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6499c-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6499c-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6499c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-197">Search-Flags</span></span>           | <span data-ttu-id="6499c-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6499c-198">0x00000000</span></span>                      |
| <span data-ttu-id="6499c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-199">System-Flags</span></span>           | <span data-ttu-id="6499c-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6499c-200">0x00000010</span></span>                      |
| <span data-ttu-id="6499c-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6499c-201">Classes used in</span></span>        | [<span data-ttu-id="6499c-202">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6499c-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6499c-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6499c-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6499c-204">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-204">Entry</span></span> | <span data-ttu-id="6499c-205">值</span><span class="sxs-lookup"><span data-stu-id="6499c-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6499c-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6499c-206">Link-Id</span></span>                | <span data-ttu-id="6499c-207">69</span><span class="sxs-lookup"><span data-stu-id="6499c-207">69</span></span>                              |
| <span data-ttu-id="6499c-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6499c-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6499c-209">System-Only</span></span>            | <span data-ttu-id="6499c-210">對</span><span class="sxs-lookup"><span data-stu-id="6499c-210">True</span></span>                            |
| <span data-ttu-id="6499c-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6499c-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6499c-212">否</span><span class="sxs-lookup"><span data-stu-id="6499c-212">False</span></span>                           |
| <span data-ttu-id="6499c-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6499c-213">Is Indexed</span></span>             | <span data-ttu-id="6499c-214">否</span><span class="sxs-lookup"><span data-stu-id="6499c-214">False</span></span>                           |
| <span data-ttu-id="6499c-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6499c-215">In Global Catalog</span></span>      | <span data-ttu-id="6499c-216">否</span><span class="sxs-lookup"><span data-stu-id="6499c-216">False</span></span>                           |
| <span data-ttu-id="6499c-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6499c-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6499c-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6499c-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6499c-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6499c-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6499c-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6499c-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6499c-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-221">Search-Flags</span></span>           | <span data-ttu-id="6499c-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6499c-222">0x00000000</span></span>                      |
| <span data-ttu-id="6499c-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-223">System-Flags</span></span>           | <span data-ttu-id="6499c-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6499c-224">0x00000010</span></span>                      |
| <span data-ttu-id="6499c-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6499c-225">Classes used in</span></span>        | [<span data-ttu-id="6499c-226">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6499c-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6499c-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6499c-227">Windows Server 2008</span></span>



| <span data-ttu-id="6499c-228">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-228">Entry</span></span> | <span data-ttu-id="6499c-229">值</span><span class="sxs-lookup"><span data-stu-id="6499c-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6499c-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6499c-230">Link-Id</span></span>                | <span data-ttu-id="6499c-231">69</span><span class="sxs-lookup"><span data-stu-id="6499c-231">69</span></span>                              |
| <span data-ttu-id="6499c-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6499c-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="6499c-233">System-Only</span></span>            | <span data-ttu-id="6499c-234">對</span><span class="sxs-lookup"><span data-stu-id="6499c-234">True</span></span>                            |
| <span data-ttu-id="6499c-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6499c-235">Is-Single-Valued</span></span>       | <span data-ttu-id="6499c-236">否</span><span class="sxs-lookup"><span data-stu-id="6499c-236">False</span></span>                           |
| <span data-ttu-id="6499c-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6499c-237">Is Indexed</span></span>             | <span data-ttu-id="6499c-238">否</span><span class="sxs-lookup"><span data-stu-id="6499c-238">False</span></span>                           |
| <span data-ttu-id="6499c-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6499c-239">In Global Catalog</span></span>      | <span data-ttu-id="6499c-240">否</span><span class="sxs-lookup"><span data-stu-id="6499c-240">False</span></span>                           |
| <span data-ttu-id="6499c-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6499c-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="6499c-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6499c-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6499c-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6499c-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6499c-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6499c-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6499c-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-245">Search-Flags</span></span>           | <span data-ttu-id="6499c-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6499c-246">0x00000000</span></span>                      |
| <span data-ttu-id="6499c-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-247">System-Flags</span></span>           | <span data-ttu-id="6499c-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6499c-248">0x00000010</span></span>                      |
| <span data-ttu-id="6499c-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6499c-249">Classes used in</span></span>        | [<span data-ttu-id="6499c-250">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6499c-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6499c-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6499c-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6499c-252">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-252">Entry</span></span> | <span data-ttu-id="6499c-253">值</span><span class="sxs-lookup"><span data-stu-id="6499c-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6499c-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6499c-254">Link-Id</span></span>                | <span data-ttu-id="6499c-255">69</span><span class="sxs-lookup"><span data-stu-id="6499c-255">69</span></span>                              |
| <span data-ttu-id="6499c-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6499c-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="6499c-257">System-Only</span></span>            | <span data-ttu-id="6499c-258">對</span><span class="sxs-lookup"><span data-stu-id="6499c-258">True</span></span>                            |
| <span data-ttu-id="6499c-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6499c-259">Is-Single-Valued</span></span>       | <span data-ttu-id="6499c-260">否</span><span class="sxs-lookup"><span data-stu-id="6499c-260">False</span></span>                           |
| <span data-ttu-id="6499c-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6499c-261">Is Indexed</span></span>             | <span data-ttu-id="6499c-262">否</span><span class="sxs-lookup"><span data-stu-id="6499c-262">False</span></span>                           |
| <span data-ttu-id="6499c-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6499c-263">In Global Catalog</span></span>      | <span data-ttu-id="6499c-264">否</span><span class="sxs-lookup"><span data-stu-id="6499c-264">False</span></span>                           |
| <span data-ttu-id="6499c-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6499c-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="6499c-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6499c-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6499c-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6499c-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6499c-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6499c-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6499c-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-269">Search-Flags</span></span>           | <span data-ttu-id="6499c-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6499c-270">0x00000000</span></span>                      |
| <span data-ttu-id="6499c-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-271">System-Flags</span></span>           | <span data-ttu-id="6499c-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6499c-272">0x00000010</span></span>                      |
| <span data-ttu-id="6499c-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6499c-273">Classes used in</span></span>        | [<span data-ttu-id="6499c-274">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6499c-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6499c-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6499c-275">Windows Server 2012</span></span>



| <span data-ttu-id="6499c-276">進入</span><span class="sxs-lookup"><span data-stu-id="6499c-276">Entry</span></span> | <span data-ttu-id="6499c-277">值</span><span class="sxs-lookup"><span data-stu-id="6499c-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6499c-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6499c-278">Link-Id</span></span>                | <span data-ttu-id="6499c-279">69</span><span class="sxs-lookup"><span data-stu-id="6499c-279">69</span></span>                              |
| <span data-ttu-id="6499c-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6499c-280">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6499c-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="6499c-281">System-Only</span></span>            | <span data-ttu-id="6499c-282">對</span><span class="sxs-lookup"><span data-stu-id="6499c-282">True</span></span>                            |
| <span data-ttu-id="6499c-283">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6499c-283">Is-Single-Valued</span></span>       | <span data-ttu-id="6499c-284">否</span><span class="sxs-lookup"><span data-stu-id="6499c-284">False</span></span>                           |
| <span data-ttu-id="6499c-285">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6499c-285">Is Indexed</span></span>             | <span data-ttu-id="6499c-286">否</span><span class="sxs-lookup"><span data-stu-id="6499c-286">False</span></span>                           |
| <span data-ttu-id="6499c-287">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6499c-287">In Global Catalog</span></span>      | <span data-ttu-id="6499c-288">否</span><span class="sxs-lookup"><span data-stu-id="6499c-288">False</span></span>                           |
| <span data-ttu-id="6499c-289">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6499c-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="6499c-290">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6499c-290">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6499c-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6499c-291">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6499c-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6499c-292">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6499c-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-293">Search-Flags</span></span>           | <span data-ttu-id="6499c-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6499c-294">0x00000000</span></span>                      |
| <span data-ttu-id="6499c-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6499c-295">System-Flags</span></span>           | <span data-ttu-id="6499c-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6499c-296">0x00000010</span></span>                      |
| <span data-ttu-id="6499c-297">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6499c-297">Classes used in</span></span>        | [<span data-ttu-id="6499c-298">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="6499c-298">**Top**</span></span>](c-top.md)<br/> |



 

 





