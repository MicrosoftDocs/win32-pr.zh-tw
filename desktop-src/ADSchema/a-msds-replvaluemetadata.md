---
title: ms-DS-複寫-值-中繼資料屬性
description: 屬性之每個值的中繼資料清單。 中繼資料會指出上次變更值的人員。
ms.assetid: 79c01bda-ea1b-41ca-b4de-c16c5167b270
ms.tgt_platform: multiple
keywords:
- ms-DS-複寫-值-中繼資料屬性 AD 架構
- ReplValueMetaData 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Repl-Value-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e90cb5fd462fc75126b6ba80f10638826811d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973334"
---
# <a name="ms-ds-repl-value-meta-data-attribute"></a><span data-ttu-id="a78c7-106">ms-DS-複寫-值-中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="a78c7-106">ms-DS-Repl-Value-Meta-Data attribute</span></span>

<span data-ttu-id="a78c7-107">屬性之每個值的中繼資料清單。</span><span class="sxs-lookup"><span data-stu-id="a78c7-107">A list of metadata for each value of an attribute.</span></span> <span data-ttu-id="a78c7-108">中繼資料會指出上次變更值的人員。</span><span class="sxs-lookup"><span data-stu-id="a78c7-108">The metadata indicates who changed the value last.</span></span>



| <span data-ttu-id="a78c7-109">進入</span><span class="sxs-lookup"><span data-stu-id="a78c7-109">Entry</span></span> | <span data-ttu-id="a78c7-110">值</span><span class="sxs-lookup"><span data-stu-id="a78c7-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a78c7-111">CN</span><span class="sxs-lookup"><span data-stu-id="a78c7-111">CN</span></span>                | <span data-ttu-id="a78c7-112">ms-DS-複製-值中繼資料</span><span class="sxs-lookup"><span data-stu-id="a78c7-112">ms-DS-Repl-Value-Meta-Data</span></span>                  |
| <span data-ttu-id="a78c7-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a78c7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a78c7-114">ReplValueMetaData</span><span class="sxs-lookup"><span data-stu-id="a78c7-114">msDS-ReplValueMetaData</span></span>                      |
| <span data-ttu-id="a78c7-115">大小</span><span class="sxs-lookup"><span data-stu-id="a78c7-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a78c7-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a78c7-116">Update Privilege</span></span>  | <span data-ttu-id="a78c7-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a78c7-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="a78c7-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a78c7-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a78c7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a78c7-119">Attribute-Id</span></span>      | <span data-ttu-id="a78c7-120">1.2.840.113556.1.4.1708</span><span class="sxs-lookup"><span data-stu-id="a78c7-120">1.2.840.113556.1.4.1708</span></span>                     |
| <span data-ttu-id="a78c7-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a78c7-121">System-Id-Guid</span></span>    | <span data-ttu-id="a78c7-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span><span class="sxs-lookup"><span data-stu-id="a78c7-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span></span>        |
| <span data-ttu-id="a78c7-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a78c7-123">Syntax</span></span>            | [<span data-ttu-id="a78c7-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a78c7-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a78c7-125">實作</span><span class="sxs-lookup"><span data-stu-id="a78c7-125">Implementations</span></span>

-   [<span data-ttu-id="a78c7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a78c7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a78c7-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a78c7-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a78c7-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a78c7-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a78c7-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a78c7-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a78c7-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a78c7-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a78c7-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a78c7-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a78c7-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a78c7-132">Windows Server 2003</span></span>



| <span data-ttu-id="a78c7-133">進入</span><span class="sxs-lookup"><span data-stu-id="a78c7-133">Entry</span></span> | <span data-ttu-id="a78c7-134">值</span><span class="sxs-lookup"><span data-stu-id="a78c7-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a78c7-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a78c7-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a78c7-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a78c7-137">System-Only</span></span>            | <span data-ttu-id="a78c7-138">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-138">False</span></span>                           |
| <span data-ttu-id="a78c7-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a78c7-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a78c7-140">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-140">False</span></span>                           |
| <span data-ttu-id="a78c7-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a78c7-141">Is Indexed</span></span>             | <span data-ttu-id="a78c7-142">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-142">False</span></span>                           |
| <span data-ttu-id="a78c7-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a78c7-143">In Global Catalog</span></span>      | <span data-ttu-id="a78c7-144">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-144">False</span></span>                           |
| <span data-ttu-id="a78c7-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a78c7-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a78c7-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a78c7-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a78c7-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a78c7-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a78c7-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a78c7-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a78c7-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-149">Search-Flags</span></span>           | <span data-ttu-id="a78c7-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a78c7-150">0x00000000</span></span>                      |
| <span data-ttu-id="a78c7-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-151">System-Flags</span></span>           | <span data-ttu-id="a78c7-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a78c7-152">0x00000014</span></span>                      |
| <span data-ttu-id="a78c7-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a78c7-153">Classes used in</span></span>        | [<span data-ttu-id="a78c7-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a78c7-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a78c7-155">亞當</span><span class="sxs-lookup"><span data-stu-id="a78c7-155">ADAM</span></span>



| <span data-ttu-id="a78c7-156">進入</span><span class="sxs-lookup"><span data-stu-id="a78c7-156">Entry</span></span> | <span data-ttu-id="a78c7-157">值</span><span class="sxs-lookup"><span data-stu-id="a78c7-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a78c7-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a78c7-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a78c7-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a78c7-160">System-Only</span></span>            | <span data-ttu-id="a78c7-161">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-161">False</span></span>                           |
| <span data-ttu-id="a78c7-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a78c7-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a78c7-163">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-163">False</span></span>                           |
| <span data-ttu-id="a78c7-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a78c7-164">Is Indexed</span></span>             | <span data-ttu-id="a78c7-165">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-165">False</span></span>                           |
| <span data-ttu-id="a78c7-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a78c7-166">In Global Catalog</span></span>      | <span data-ttu-id="a78c7-167">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-167">False</span></span>                           |
| <span data-ttu-id="a78c7-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a78c7-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a78c7-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a78c7-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a78c7-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a78c7-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a78c7-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a78c7-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a78c7-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-172">Search-Flags</span></span>           | <span data-ttu-id="a78c7-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a78c7-173">0x00000000</span></span>                      |
| <span data-ttu-id="a78c7-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-174">System-Flags</span></span>           | <span data-ttu-id="a78c7-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a78c7-175">0x00000014</span></span>                      |
| <span data-ttu-id="a78c7-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a78c7-176">Classes used in</span></span>        | [<span data-ttu-id="a78c7-177">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a78c7-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a78c7-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a78c7-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a78c7-179">進入</span><span class="sxs-lookup"><span data-stu-id="a78c7-179">Entry</span></span> | <span data-ttu-id="a78c7-180">值</span><span class="sxs-lookup"><span data-stu-id="a78c7-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a78c7-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a78c7-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a78c7-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a78c7-183">System-Only</span></span>            | <span data-ttu-id="a78c7-184">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-184">False</span></span>                           |
| <span data-ttu-id="a78c7-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a78c7-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a78c7-186">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-186">False</span></span>                           |
| <span data-ttu-id="a78c7-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a78c7-187">Is Indexed</span></span>             | <span data-ttu-id="a78c7-188">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-188">False</span></span>                           |
| <span data-ttu-id="a78c7-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a78c7-189">In Global Catalog</span></span>      | <span data-ttu-id="a78c7-190">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-190">False</span></span>                           |
| <span data-ttu-id="a78c7-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a78c7-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a78c7-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a78c7-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a78c7-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a78c7-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a78c7-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a78c7-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a78c7-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-195">Search-Flags</span></span>           | <span data-ttu-id="a78c7-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a78c7-196">0x00000000</span></span>                      |
| <span data-ttu-id="a78c7-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-197">System-Flags</span></span>           | <span data-ttu-id="a78c7-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a78c7-198">0x00000014</span></span>                      |
| <span data-ttu-id="a78c7-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a78c7-199">Classes used in</span></span>        | [<span data-ttu-id="a78c7-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a78c7-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a78c7-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a78c7-201">Windows Server 2008</span></span>



| <span data-ttu-id="a78c7-202">進入</span><span class="sxs-lookup"><span data-stu-id="a78c7-202">Entry</span></span> | <span data-ttu-id="a78c7-203">值</span><span class="sxs-lookup"><span data-stu-id="a78c7-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a78c7-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a78c7-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a78c7-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a78c7-206">System-Only</span></span>            | <span data-ttu-id="a78c7-207">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-207">False</span></span>                           |
| <span data-ttu-id="a78c7-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a78c7-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a78c7-209">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-209">False</span></span>                           |
| <span data-ttu-id="a78c7-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a78c7-210">Is Indexed</span></span>             | <span data-ttu-id="a78c7-211">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-211">False</span></span>                           |
| <span data-ttu-id="a78c7-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a78c7-212">In Global Catalog</span></span>      | <span data-ttu-id="a78c7-213">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-213">False</span></span>                           |
| <span data-ttu-id="a78c7-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a78c7-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a78c7-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a78c7-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a78c7-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a78c7-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a78c7-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a78c7-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a78c7-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-218">Search-Flags</span></span>           | <span data-ttu-id="a78c7-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a78c7-219">0x00000000</span></span>                      |
| <span data-ttu-id="a78c7-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-220">System-Flags</span></span>           | <span data-ttu-id="a78c7-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a78c7-221">0x00000014</span></span>                      |
| <span data-ttu-id="a78c7-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a78c7-222">Classes used in</span></span>        | [<span data-ttu-id="a78c7-223">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a78c7-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a78c7-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a78c7-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a78c7-225">進入</span><span class="sxs-lookup"><span data-stu-id="a78c7-225">Entry</span></span> | <span data-ttu-id="a78c7-226">值</span><span class="sxs-lookup"><span data-stu-id="a78c7-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a78c7-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a78c7-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a78c7-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a78c7-229">System-Only</span></span>            | <span data-ttu-id="a78c7-230">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-230">False</span></span>                           |
| <span data-ttu-id="a78c7-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a78c7-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a78c7-232">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-232">False</span></span>                           |
| <span data-ttu-id="a78c7-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a78c7-233">Is Indexed</span></span>             | <span data-ttu-id="a78c7-234">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-234">False</span></span>                           |
| <span data-ttu-id="a78c7-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a78c7-235">In Global Catalog</span></span>      | <span data-ttu-id="a78c7-236">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-236">False</span></span>                           |
| <span data-ttu-id="a78c7-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a78c7-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a78c7-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a78c7-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a78c7-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a78c7-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a78c7-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a78c7-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a78c7-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-241">Search-Flags</span></span>           | <span data-ttu-id="a78c7-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a78c7-242">0x00000000</span></span>                      |
| <span data-ttu-id="a78c7-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-243">System-Flags</span></span>           | <span data-ttu-id="a78c7-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a78c7-244">0x00000014</span></span>                      |
| <span data-ttu-id="a78c7-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a78c7-245">Classes used in</span></span>        | [<span data-ttu-id="a78c7-246">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a78c7-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a78c7-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a78c7-247">Windows Server 2012</span></span>



| <span data-ttu-id="a78c7-248">進入</span><span class="sxs-lookup"><span data-stu-id="a78c7-248">Entry</span></span> | <span data-ttu-id="a78c7-249">值</span><span class="sxs-lookup"><span data-stu-id="a78c7-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a78c7-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a78c7-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a78c7-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a78c7-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a78c7-252">System-Only</span></span>            | <span data-ttu-id="a78c7-253">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-253">False</span></span>                           |
| <span data-ttu-id="a78c7-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a78c7-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a78c7-255">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-255">False</span></span>                           |
| <span data-ttu-id="a78c7-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a78c7-256">Is Indexed</span></span>             | <span data-ttu-id="a78c7-257">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-257">False</span></span>                           |
| <span data-ttu-id="a78c7-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a78c7-258">In Global Catalog</span></span>      | <span data-ttu-id="a78c7-259">否</span><span class="sxs-lookup"><span data-stu-id="a78c7-259">False</span></span>                           |
| <span data-ttu-id="a78c7-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a78c7-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a78c7-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a78c7-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a78c7-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a78c7-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a78c7-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a78c7-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a78c7-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-264">Search-Flags</span></span>           | <span data-ttu-id="a78c7-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a78c7-265">0x00000000</span></span>                      |
| <span data-ttu-id="a78c7-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a78c7-266">System-Flags</span></span>           | <span data-ttu-id="a78c7-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a78c7-267">0x00000014</span></span>                      |
| <span data-ttu-id="a78c7-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a78c7-268">Classes used in</span></span>        | [<span data-ttu-id="a78c7-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a78c7-269">**Top**</span></span>](c-top.md)<br/> |



 

 





