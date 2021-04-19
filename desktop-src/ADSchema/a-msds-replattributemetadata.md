---
title: ms-DS-複寫-屬性中繼資料屬性
description: 每個已複寫屬性的中繼資料清單。 中繼資料會指出最後變更屬性的人員。
ms.assetid: 07cfd323-eb90-4715-9307-583cf7e9f63e
ms.tgt_platform: multiple
keywords:
- ms-DS-複寫-屬性中繼資料屬性 AD 架構
- ReplAttributeMetaData 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Repl-Attribute-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc991ead7104d8b9b4c023882d39adf1d53446
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972078"
---
# <a name="ms-ds-repl-attribute-meta-data-attribute"></a><span data-ttu-id="f45cf-106">ms-DS-複寫-屬性中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="f45cf-106">ms-DS-Repl-Attribute-Meta-Data attribute</span></span>

<span data-ttu-id="f45cf-107">每個已複寫屬性的中繼資料清單。</span><span class="sxs-lookup"><span data-stu-id="f45cf-107">A list of metadata for each replicated attribute.</span></span> <span data-ttu-id="f45cf-108">中繼資料會指出最後變更屬性的人員。</span><span class="sxs-lookup"><span data-stu-id="f45cf-108">The metadata indicates who changed the attribute last.</span></span>



| <span data-ttu-id="f45cf-109">進入</span><span class="sxs-lookup"><span data-stu-id="f45cf-109">Entry</span></span> | <span data-ttu-id="f45cf-110">值</span><span class="sxs-lookup"><span data-stu-id="f45cf-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f45cf-111">CN</span><span class="sxs-lookup"><span data-stu-id="f45cf-111">CN</span></span>                | <span data-ttu-id="f45cf-112">ms-DS-複寫-屬性中繼資料</span><span class="sxs-lookup"><span data-stu-id="f45cf-112">ms-DS-Repl-Attribute-Meta-Data</span></span>              |
| <span data-ttu-id="f45cf-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f45cf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f45cf-114">ReplAttributeMetaData</span><span class="sxs-lookup"><span data-stu-id="f45cf-114">msDS-ReplAttributeMetaData</span></span>                  |
| <span data-ttu-id="f45cf-115">大小</span><span class="sxs-lookup"><span data-stu-id="f45cf-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="f45cf-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f45cf-116">Update Privilege</span></span>  | <span data-ttu-id="f45cf-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="f45cf-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="f45cf-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f45cf-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f45cf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f45cf-119">Attribute-Id</span></span>      | <span data-ttu-id="f45cf-120">1.2.840.113556.1.4.1707</span><span class="sxs-lookup"><span data-stu-id="f45cf-120">1.2.840.113556.1.4.1707</span></span>                     |
| <span data-ttu-id="f45cf-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f45cf-121">System-Id-Guid</span></span>    | <span data-ttu-id="f45cf-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span><span class="sxs-lookup"><span data-stu-id="f45cf-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span></span>        |
| <span data-ttu-id="f45cf-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f45cf-123">Syntax</span></span>            | [<span data-ttu-id="f45cf-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f45cf-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f45cf-125">實作</span><span class="sxs-lookup"><span data-stu-id="f45cf-125">Implementations</span></span>

-   [<span data-ttu-id="f45cf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f45cf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f45cf-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f45cf-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f45cf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f45cf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f45cf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f45cf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f45cf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f45cf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f45cf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f45cf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f45cf-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f45cf-132">Windows Server 2003</span></span>



| <span data-ttu-id="f45cf-133">進入</span><span class="sxs-lookup"><span data-stu-id="f45cf-133">Entry</span></span> | <span data-ttu-id="f45cf-134">值</span><span class="sxs-lookup"><span data-stu-id="f45cf-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f45cf-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f45cf-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f45cf-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f45cf-137">System-Only</span></span>            | <span data-ttu-id="f45cf-138">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-138">False</span></span>                           |
| <span data-ttu-id="f45cf-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f45cf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f45cf-140">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-140">False</span></span>                           |
| <span data-ttu-id="f45cf-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f45cf-141">Is Indexed</span></span>             | <span data-ttu-id="f45cf-142">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-142">False</span></span>                           |
| <span data-ttu-id="f45cf-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f45cf-143">In Global Catalog</span></span>      | <span data-ttu-id="f45cf-144">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-144">False</span></span>                           |
| <span data-ttu-id="f45cf-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f45cf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f45cf-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f45cf-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f45cf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f45cf-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f45cf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f45cf-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f45cf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-149">Search-Flags</span></span>           | <span data-ttu-id="f45cf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f45cf-150">0x00000000</span></span>                      |
| <span data-ttu-id="f45cf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-151">System-Flags</span></span>           | <span data-ttu-id="f45cf-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f45cf-152">0x00000014</span></span>                      |
| <span data-ttu-id="f45cf-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f45cf-153">Classes used in</span></span>        | [<span data-ttu-id="f45cf-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f45cf-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f45cf-155">亞當</span><span class="sxs-lookup"><span data-stu-id="f45cf-155">ADAM</span></span>



| <span data-ttu-id="f45cf-156">進入</span><span class="sxs-lookup"><span data-stu-id="f45cf-156">Entry</span></span> | <span data-ttu-id="f45cf-157">值</span><span class="sxs-lookup"><span data-stu-id="f45cf-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f45cf-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f45cf-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f45cf-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f45cf-160">System-Only</span></span>            | <span data-ttu-id="f45cf-161">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-161">False</span></span>                           |
| <span data-ttu-id="f45cf-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f45cf-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f45cf-163">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-163">False</span></span>                           |
| <span data-ttu-id="f45cf-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f45cf-164">Is Indexed</span></span>             | <span data-ttu-id="f45cf-165">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-165">False</span></span>                           |
| <span data-ttu-id="f45cf-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f45cf-166">In Global Catalog</span></span>      | <span data-ttu-id="f45cf-167">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-167">False</span></span>                           |
| <span data-ttu-id="f45cf-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f45cf-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f45cf-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f45cf-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f45cf-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f45cf-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f45cf-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f45cf-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f45cf-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-172">Search-Flags</span></span>           | <span data-ttu-id="f45cf-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f45cf-173">0x00000000</span></span>                      |
| <span data-ttu-id="f45cf-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-174">System-Flags</span></span>           | <span data-ttu-id="f45cf-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f45cf-175">0x00000014</span></span>                      |
| <span data-ttu-id="f45cf-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f45cf-176">Classes used in</span></span>        | [<span data-ttu-id="f45cf-177">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f45cf-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f45cf-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f45cf-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f45cf-179">進入</span><span class="sxs-lookup"><span data-stu-id="f45cf-179">Entry</span></span> | <span data-ttu-id="f45cf-180">值</span><span class="sxs-lookup"><span data-stu-id="f45cf-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f45cf-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f45cf-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f45cf-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f45cf-183">System-Only</span></span>            | <span data-ttu-id="f45cf-184">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-184">False</span></span>                           |
| <span data-ttu-id="f45cf-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f45cf-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f45cf-186">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-186">False</span></span>                           |
| <span data-ttu-id="f45cf-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f45cf-187">Is Indexed</span></span>             | <span data-ttu-id="f45cf-188">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-188">False</span></span>                           |
| <span data-ttu-id="f45cf-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f45cf-189">In Global Catalog</span></span>      | <span data-ttu-id="f45cf-190">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-190">False</span></span>                           |
| <span data-ttu-id="f45cf-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f45cf-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f45cf-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f45cf-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f45cf-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f45cf-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f45cf-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f45cf-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f45cf-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-195">Search-Flags</span></span>           | <span data-ttu-id="f45cf-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f45cf-196">0x00000000</span></span>                      |
| <span data-ttu-id="f45cf-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-197">System-Flags</span></span>           | <span data-ttu-id="f45cf-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f45cf-198">0x00000014</span></span>                      |
| <span data-ttu-id="f45cf-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f45cf-199">Classes used in</span></span>        | [<span data-ttu-id="f45cf-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f45cf-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f45cf-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f45cf-201">Windows Server 2008</span></span>



| <span data-ttu-id="f45cf-202">進入</span><span class="sxs-lookup"><span data-stu-id="f45cf-202">Entry</span></span> | <span data-ttu-id="f45cf-203">值</span><span class="sxs-lookup"><span data-stu-id="f45cf-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f45cf-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f45cf-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f45cf-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f45cf-206">System-Only</span></span>            | <span data-ttu-id="f45cf-207">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-207">False</span></span>                           |
| <span data-ttu-id="f45cf-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f45cf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f45cf-209">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-209">False</span></span>                           |
| <span data-ttu-id="f45cf-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f45cf-210">Is Indexed</span></span>             | <span data-ttu-id="f45cf-211">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-211">False</span></span>                           |
| <span data-ttu-id="f45cf-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f45cf-212">In Global Catalog</span></span>      | <span data-ttu-id="f45cf-213">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-213">False</span></span>                           |
| <span data-ttu-id="f45cf-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f45cf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f45cf-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f45cf-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f45cf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f45cf-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f45cf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f45cf-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f45cf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-218">Search-Flags</span></span>           | <span data-ttu-id="f45cf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f45cf-219">0x00000000</span></span>                      |
| <span data-ttu-id="f45cf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-220">System-Flags</span></span>           | <span data-ttu-id="f45cf-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f45cf-221">0x00000014</span></span>                      |
| <span data-ttu-id="f45cf-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f45cf-222">Classes used in</span></span>        | [<span data-ttu-id="f45cf-223">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f45cf-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f45cf-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f45cf-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f45cf-225">進入</span><span class="sxs-lookup"><span data-stu-id="f45cf-225">Entry</span></span> | <span data-ttu-id="f45cf-226">值</span><span class="sxs-lookup"><span data-stu-id="f45cf-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f45cf-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f45cf-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f45cf-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f45cf-229">System-Only</span></span>            | <span data-ttu-id="f45cf-230">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-230">False</span></span>                           |
| <span data-ttu-id="f45cf-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f45cf-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f45cf-232">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-232">False</span></span>                           |
| <span data-ttu-id="f45cf-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f45cf-233">Is Indexed</span></span>             | <span data-ttu-id="f45cf-234">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-234">False</span></span>                           |
| <span data-ttu-id="f45cf-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f45cf-235">In Global Catalog</span></span>      | <span data-ttu-id="f45cf-236">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-236">False</span></span>                           |
| <span data-ttu-id="f45cf-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f45cf-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f45cf-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f45cf-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f45cf-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f45cf-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f45cf-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f45cf-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f45cf-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-241">Search-Flags</span></span>           | <span data-ttu-id="f45cf-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f45cf-242">0x00000000</span></span>                      |
| <span data-ttu-id="f45cf-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-243">System-Flags</span></span>           | <span data-ttu-id="f45cf-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f45cf-244">0x00000014</span></span>                      |
| <span data-ttu-id="f45cf-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f45cf-245">Classes used in</span></span>        | [<span data-ttu-id="f45cf-246">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f45cf-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f45cf-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f45cf-247">Windows Server 2012</span></span>



| <span data-ttu-id="f45cf-248">進入</span><span class="sxs-lookup"><span data-stu-id="f45cf-248">Entry</span></span> | <span data-ttu-id="f45cf-249">值</span><span class="sxs-lookup"><span data-stu-id="f45cf-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f45cf-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f45cf-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f45cf-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f45cf-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f45cf-252">System-Only</span></span>            | <span data-ttu-id="f45cf-253">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-253">False</span></span>                           |
| <span data-ttu-id="f45cf-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f45cf-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f45cf-255">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-255">False</span></span>                           |
| <span data-ttu-id="f45cf-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f45cf-256">Is Indexed</span></span>             | <span data-ttu-id="f45cf-257">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-257">False</span></span>                           |
| <span data-ttu-id="f45cf-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f45cf-258">In Global Catalog</span></span>      | <span data-ttu-id="f45cf-259">否</span><span class="sxs-lookup"><span data-stu-id="f45cf-259">False</span></span>                           |
| <span data-ttu-id="f45cf-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f45cf-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f45cf-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f45cf-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f45cf-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f45cf-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f45cf-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f45cf-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f45cf-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-264">Search-Flags</span></span>           | <span data-ttu-id="f45cf-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f45cf-265">0x00000000</span></span>                      |
| <span data-ttu-id="f45cf-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f45cf-266">System-Flags</span></span>           | <span data-ttu-id="f45cf-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f45cf-267">0x00000014</span></span>                      |
| <span data-ttu-id="f45cf-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f45cf-268">Classes used in</span></span>        | [<span data-ttu-id="f45cf-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f45cf-269">**Top**</span></span>](c-top.md)<br/> |



 

 





