---
title: ms-DS-Immed-從屬屬性
description: 這個屬性所傳回的值是以索引大小為基礎。 這可能是由 +/\ 8211、在大型容器上為10，而此錯誤理論上是未系結的，但使用此屬性可協助 UI 顯示容器的內容。
ms.assetid: 0d6e3b53-dfad-49ac-bbb3-e53c33ea9cd8
ms.tgt_platform: multiple
keywords:
- ms-DS-Immed-從屬屬性 AD 架構
- Immed-從屬屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Approx-Immed-Subordinates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb51ef642c216d8e41b774ffc596a8f3d4feb28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509710"
---
# <a name="ms-ds-approx-immed-subordinates-attribute"></a><span data-ttu-id="449dc-106">ms-DS-Immed-從屬屬性</span><span class="sxs-lookup"><span data-stu-id="449dc-106">ms-DS-Approx-Immed-Subordinates attribute</span></span>

<span data-ttu-id="449dc-107">這個屬性所傳回的值是以索引大小為基礎。</span><span class="sxs-lookup"><span data-stu-id="449dc-107">The value returned by this attribute is based on index sizes.</span></span> <span data-ttu-id="449dc-108">這可能是因為大型容器上的 +/10%，而且理論上未系結錯誤，但使用此屬性可協助 UI 顯示容器的內容。</span><span class="sxs-lookup"><span data-stu-id="449dc-108">This may be off by +/ 10% on large containers, and the error is theoretically unbounded, but using this attribute helps the UI display the contents of a container.</span></span>



| <span data-ttu-id="449dc-109">進入</span><span class="sxs-lookup"><span data-stu-id="449dc-109">Entry</span></span> | <span data-ttu-id="449dc-110">值</span><span class="sxs-lookup"><span data-stu-id="449dc-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="449dc-111">CN</span><span class="sxs-lookup"><span data-stu-id="449dc-111">CN</span></span>                | <span data-ttu-id="449dc-112">ms-DS-Immed-從屬</span><span class="sxs-lookup"><span data-stu-id="449dc-112">ms-DS-Approx-Immed-Subordinates</span></span>      |
| <span data-ttu-id="449dc-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="449dc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="449dc-114">Immed-附屬</span><span class="sxs-lookup"><span data-stu-id="449dc-114">msDS-Approx-Immed-Subordinates</span></span>       |
| <span data-ttu-id="449dc-115">大小</span><span class="sxs-lookup"><span data-stu-id="449dc-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="449dc-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="449dc-116">Update Privilege</span></span>  | <span data-ttu-id="449dc-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="449dc-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="449dc-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="449dc-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="449dc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="449dc-119">Attribute-Id</span></span>      | <span data-ttu-id="449dc-120">1.2.840.113556.1.4.1669</span><span class="sxs-lookup"><span data-stu-id="449dc-120">1.2.840.113556.1.4.1669</span></span>              |
| <span data-ttu-id="449dc-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="449dc-121">System-Id-Guid</span></span>    | <span data-ttu-id="449dc-122">e185d243-f6ce-4adb-b496-b0c005d7823c</span><span class="sxs-lookup"><span data-stu-id="449dc-122">e185d243-f6ce-4adb-b496-b0c005d7823c</span></span> |
| <span data-ttu-id="449dc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="449dc-123">Syntax</span></span>            | [<span data-ttu-id="449dc-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="449dc-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="449dc-125">實作</span><span class="sxs-lookup"><span data-stu-id="449dc-125">Implementations</span></span>

-   [<span data-ttu-id="449dc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="449dc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="449dc-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="449dc-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="449dc-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="449dc-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="449dc-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="449dc-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="449dc-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="449dc-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="449dc-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="449dc-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="449dc-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="449dc-132">Windows Server 2003</span></span>



| <span data-ttu-id="449dc-133">進入</span><span class="sxs-lookup"><span data-stu-id="449dc-133">Entry</span></span> | <span data-ttu-id="449dc-134">值</span><span class="sxs-lookup"><span data-stu-id="449dc-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="449dc-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="449dc-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449dc-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="449dc-137">System-Only</span></span>            | <span data-ttu-id="449dc-138">對</span><span class="sxs-lookup"><span data-stu-id="449dc-138">True</span></span>                            |
| <span data-ttu-id="449dc-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="449dc-139">Is-Single-Valued</span></span>       | <span data-ttu-id="449dc-140">對</span><span class="sxs-lookup"><span data-stu-id="449dc-140">True</span></span>                            |
| <span data-ttu-id="449dc-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="449dc-141">Is Indexed</span></span>             | <span data-ttu-id="449dc-142">否</span><span class="sxs-lookup"><span data-stu-id="449dc-142">False</span></span>                           |
| <span data-ttu-id="449dc-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="449dc-143">In Global Catalog</span></span>      | <span data-ttu-id="449dc-144">否</span><span class="sxs-lookup"><span data-stu-id="449dc-144">False</span></span>                           |
| <span data-ttu-id="449dc-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="449dc-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="449dc-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="449dc-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="449dc-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449dc-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="449dc-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449dc-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="449dc-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-149">Search-Flags</span></span>           | <span data-ttu-id="449dc-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449dc-150">0x00000000</span></span>                      |
| <span data-ttu-id="449dc-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-151">System-Flags</span></span>           | <span data-ttu-id="449dc-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="449dc-152">0x00000014</span></span>                      |
| <span data-ttu-id="449dc-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="449dc-153">Classes used in</span></span>        | [<span data-ttu-id="449dc-154">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="449dc-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="449dc-155">亞當</span><span class="sxs-lookup"><span data-stu-id="449dc-155">ADAM</span></span>



| <span data-ttu-id="449dc-156">進入</span><span class="sxs-lookup"><span data-stu-id="449dc-156">Entry</span></span> | <span data-ttu-id="449dc-157">值</span><span class="sxs-lookup"><span data-stu-id="449dc-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="449dc-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="449dc-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449dc-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="449dc-160">System-Only</span></span>            | <span data-ttu-id="449dc-161">對</span><span class="sxs-lookup"><span data-stu-id="449dc-161">True</span></span>                            |
| <span data-ttu-id="449dc-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="449dc-162">Is-Single-Valued</span></span>       | <span data-ttu-id="449dc-163">對</span><span class="sxs-lookup"><span data-stu-id="449dc-163">True</span></span>                            |
| <span data-ttu-id="449dc-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="449dc-164">Is Indexed</span></span>             | <span data-ttu-id="449dc-165">否</span><span class="sxs-lookup"><span data-stu-id="449dc-165">False</span></span>                           |
| <span data-ttu-id="449dc-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="449dc-166">In Global Catalog</span></span>      | <span data-ttu-id="449dc-167">否</span><span class="sxs-lookup"><span data-stu-id="449dc-167">False</span></span>                           |
| <span data-ttu-id="449dc-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="449dc-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="449dc-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="449dc-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="449dc-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449dc-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="449dc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449dc-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="449dc-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-172">Search-Flags</span></span>           | <span data-ttu-id="449dc-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449dc-173">0x00000000</span></span>                      |
| <span data-ttu-id="449dc-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-174">System-Flags</span></span>           | <span data-ttu-id="449dc-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="449dc-175">0x00000014</span></span>                      |
| <span data-ttu-id="449dc-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="449dc-176">Classes used in</span></span>        | [<span data-ttu-id="449dc-177">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="449dc-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="449dc-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="449dc-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="449dc-179">進入</span><span class="sxs-lookup"><span data-stu-id="449dc-179">Entry</span></span> | <span data-ttu-id="449dc-180">值</span><span class="sxs-lookup"><span data-stu-id="449dc-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="449dc-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="449dc-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449dc-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="449dc-183">System-Only</span></span>            | <span data-ttu-id="449dc-184">對</span><span class="sxs-lookup"><span data-stu-id="449dc-184">True</span></span>                            |
| <span data-ttu-id="449dc-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="449dc-185">Is-Single-Valued</span></span>       | <span data-ttu-id="449dc-186">對</span><span class="sxs-lookup"><span data-stu-id="449dc-186">True</span></span>                            |
| <span data-ttu-id="449dc-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="449dc-187">Is Indexed</span></span>             | <span data-ttu-id="449dc-188">否</span><span class="sxs-lookup"><span data-stu-id="449dc-188">False</span></span>                           |
| <span data-ttu-id="449dc-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="449dc-189">In Global Catalog</span></span>      | <span data-ttu-id="449dc-190">否</span><span class="sxs-lookup"><span data-stu-id="449dc-190">False</span></span>                           |
| <span data-ttu-id="449dc-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="449dc-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="449dc-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="449dc-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="449dc-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449dc-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="449dc-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449dc-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="449dc-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-195">Search-Flags</span></span>           | <span data-ttu-id="449dc-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449dc-196">0x00000000</span></span>                      |
| <span data-ttu-id="449dc-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-197">System-Flags</span></span>           | <span data-ttu-id="449dc-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="449dc-198">0x00000014</span></span>                      |
| <span data-ttu-id="449dc-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="449dc-199">Classes used in</span></span>        | [<span data-ttu-id="449dc-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="449dc-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="449dc-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="449dc-201">Windows Server 2008</span></span>



| <span data-ttu-id="449dc-202">進入</span><span class="sxs-lookup"><span data-stu-id="449dc-202">Entry</span></span> | <span data-ttu-id="449dc-203">值</span><span class="sxs-lookup"><span data-stu-id="449dc-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="449dc-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="449dc-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449dc-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="449dc-206">System-Only</span></span>            | <span data-ttu-id="449dc-207">對</span><span class="sxs-lookup"><span data-stu-id="449dc-207">True</span></span>                            |
| <span data-ttu-id="449dc-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="449dc-208">Is-Single-Valued</span></span>       | <span data-ttu-id="449dc-209">對</span><span class="sxs-lookup"><span data-stu-id="449dc-209">True</span></span>                            |
| <span data-ttu-id="449dc-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="449dc-210">Is Indexed</span></span>             | <span data-ttu-id="449dc-211">否</span><span class="sxs-lookup"><span data-stu-id="449dc-211">False</span></span>                           |
| <span data-ttu-id="449dc-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="449dc-212">In Global Catalog</span></span>      | <span data-ttu-id="449dc-213">否</span><span class="sxs-lookup"><span data-stu-id="449dc-213">False</span></span>                           |
| <span data-ttu-id="449dc-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="449dc-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="449dc-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="449dc-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="449dc-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449dc-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="449dc-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449dc-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="449dc-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-218">Search-Flags</span></span>           | <span data-ttu-id="449dc-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449dc-219">0x00000000</span></span>                      |
| <span data-ttu-id="449dc-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-220">System-Flags</span></span>           | <span data-ttu-id="449dc-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="449dc-221">0x00000014</span></span>                      |
| <span data-ttu-id="449dc-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="449dc-222">Classes used in</span></span>        | [<span data-ttu-id="449dc-223">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="449dc-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="449dc-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="449dc-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="449dc-225">進入</span><span class="sxs-lookup"><span data-stu-id="449dc-225">Entry</span></span> | <span data-ttu-id="449dc-226">值</span><span class="sxs-lookup"><span data-stu-id="449dc-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="449dc-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="449dc-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449dc-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="449dc-229">System-Only</span></span>            | <span data-ttu-id="449dc-230">對</span><span class="sxs-lookup"><span data-stu-id="449dc-230">True</span></span>                            |
| <span data-ttu-id="449dc-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="449dc-231">Is-Single-Valued</span></span>       | <span data-ttu-id="449dc-232">對</span><span class="sxs-lookup"><span data-stu-id="449dc-232">True</span></span>                            |
| <span data-ttu-id="449dc-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="449dc-233">Is Indexed</span></span>             | <span data-ttu-id="449dc-234">否</span><span class="sxs-lookup"><span data-stu-id="449dc-234">False</span></span>                           |
| <span data-ttu-id="449dc-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="449dc-235">In Global Catalog</span></span>      | <span data-ttu-id="449dc-236">否</span><span class="sxs-lookup"><span data-stu-id="449dc-236">False</span></span>                           |
| <span data-ttu-id="449dc-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="449dc-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="449dc-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="449dc-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="449dc-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449dc-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="449dc-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449dc-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="449dc-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-241">Search-Flags</span></span>           | <span data-ttu-id="449dc-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449dc-242">0x00000000</span></span>                      |
| <span data-ttu-id="449dc-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-243">System-Flags</span></span>           | <span data-ttu-id="449dc-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="449dc-244">0x00000014</span></span>                      |
| <span data-ttu-id="449dc-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="449dc-245">Classes used in</span></span>        | [<span data-ttu-id="449dc-246">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="449dc-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="449dc-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="449dc-247">Windows Server 2012</span></span>



| <span data-ttu-id="449dc-248">進入</span><span class="sxs-lookup"><span data-stu-id="449dc-248">Entry</span></span> | <span data-ttu-id="449dc-249">值</span><span class="sxs-lookup"><span data-stu-id="449dc-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="449dc-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="449dc-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="449dc-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="449dc-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="449dc-252">System-Only</span></span>            | <span data-ttu-id="449dc-253">對</span><span class="sxs-lookup"><span data-stu-id="449dc-253">True</span></span>                            |
| <span data-ttu-id="449dc-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="449dc-254">Is-Single-Valued</span></span>       | <span data-ttu-id="449dc-255">對</span><span class="sxs-lookup"><span data-stu-id="449dc-255">True</span></span>                            |
| <span data-ttu-id="449dc-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="449dc-256">Is Indexed</span></span>             | <span data-ttu-id="449dc-257">否</span><span class="sxs-lookup"><span data-stu-id="449dc-257">False</span></span>                           |
| <span data-ttu-id="449dc-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="449dc-258">In Global Catalog</span></span>      | <span data-ttu-id="449dc-259">否</span><span class="sxs-lookup"><span data-stu-id="449dc-259">False</span></span>                           |
| <span data-ttu-id="449dc-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="449dc-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="449dc-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="449dc-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="449dc-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="449dc-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="449dc-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="449dc-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="449dc-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-264">Search-Flags</span></span>           | <span data-ttu-id="449dc-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="449dc-265">0x00000000</span></span>                      |
| <span data-ttu-id="449dc-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="449dc-266">System-Flags</span></span>           | <span data-ttu-id="449dc-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="449dc-267">0x00000014</span></span>                      |
| <span data-ttu-id="449dc-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="449dc-268">Classes used in</span></span>        | [<span data-ttu-id="449dc-269">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="449dc-269">**Top**</span></span>](c-top.md)<br/> |



 

 





