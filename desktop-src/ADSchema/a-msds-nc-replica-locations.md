---
title: ms DS-NC-複本-位置屬性
description: 伺服器的清單，這些伺服器是對應非網域命名內容的複本集。
ms.assetid: b0379bb6-feee-432a-b484-1a6c8100d027
ms.tgt_platform: multiple
keywords:
- ms DS-NC-複本-位置屬性 AD 架構
- 高階 NC-複本位置屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-NC-Replica-Locations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4adc3d3ca3553c8e57cdc114eb045206c1501060
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935542"
---
# <a name="ms-ds-nc-replica-locations-attribute"></a><span data-ttu-id="e65bd-105">ms DS-NC-複本-位置屬性</span><span class="sxs-lookup"><span data-stu-id="e65bd-105">ms-DS-NC-Replica-Locations attribute</span></span>

<span data-ttu-id="e65bd-106">伺服器的清單，這些伺服器是對應非網域命名內容的複本集。</span><span class="sxs-lookup"><span data-stu-id="e65bd-106">A list of servers that are the replica set for the corresponding Non-Domain Naming Context.</span></span>



| <span data-ttu-id="e65bd-107">進入</span><span class="sxs-lookup"><span data-stu-id="e65bd-107">Entry</span></span> | <span data-ttu-id="e65bd-108">值</span><span class="sxs-lookup"><span data-stu-id="e65bd-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e65bd-109">CN</span><span class="sxs-lookup"><span data-stu-id="e65bd-109">CN</span></span>                | <span data-ttu-id="e65bd-110">ms DS-----複本-位置</span><span class="sxs-lookup"><span data-stu-id="e65bd-110">ms-DS-NC-Replica-Locations</span></span>              |
| <span data-ttu-id="e65bd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e65bd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e65bd-112">高階 NC-複本-位置</span><span class="sxs-lookup"><span data-stu-id="e65bd-112">msDS-NC-Replica-Locations</span></span>               |
| <span data-ttu-id="e65bd-113">大小</span><span class="sxs-lookup"><span data-stu-id="e65bd-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e65bd-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e65bd-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="e65bd-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e65bd-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="e65bd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e65bd-116">Attribute-Id</span></span>      | <span data-ttu-id="e65bd-117">1.2.840.113556.1.4.1661</span><span class="sxs-lookup"><span data-stu-id="e65bd-117">1.2.840.113556.1.4.1661</span></span>                 |
| <span data-ttu-id="e65bd-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e65bd-118">System-Id-Guid</span></span>    | <span data-ttu-id="e65bd-119">97de9615-b537-46bc-ac0f-10720f3909f3</span><span class="sxs-lookup"><span data-stu-id="e65bd-119">97de9615-b537-46bc-ac0f-10720f3909f3</span></span>    |
| <span data-ttu-id="e65bd-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e65bd-120">Syntax</span></span>            | [<span data-ttu-id="e65bd-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e65bd-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="e65bd-122">實作</span><span class="sxs-lookup"><span data-stu-id="e65bd-122">Implementations</span></span>

-   [<span data-ttu-id="e65bd-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e65bd-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e65bd-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e65bd-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e65bd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e65bd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e65bd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e65bd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e65bd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e65bd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e65bd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e65bd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e65bd-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e65bd-129">Windows Server 2003</span></span>



| <span data-ttu-id="e65bd-130">進入</span><span class="sxs-lookup"><span data-stu-id="e65bd-130">Entry</span></span> | <span data-ttu-id="e65bd-131">值</span><span class="sxs-lookup"><span data-stu-id="e65bd-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e65bd-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e65bd-132">Link-Id</span></span>                | <span data-ttu-id="e65bd-133">1044</span><span class="sxs-lookup"><span data-stu-id="e65bd-133">1044</span></span>                                       |
| <span data-ttu-id="e65bd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e65bd-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e65bd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e65bd-135">System-Only</span></span>            | <span data-ttu-id="e65bd-136">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-136">False</span></span>                                      |
| <span data-ttu-id="e65bd-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e65bd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e65bd-138">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-138">False</span></span>                                      |
| <span data-ttu-id="e65bd-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e65bd-139">Is Indexed</span></span>             | <span data-ttu-id="e65bd-140">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-140">False</span></span>                                      |
| <span data-ttu-id="e65bd-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e65bd-141">In Global Catalog</span></span>      | <span data-ttu-id="e65bd-142">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-142">False</span></span>                                      |
| <span data-ttu-id="e65bd-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e65bd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e65bd-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e65bd-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e65bd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e65bd-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e65bd-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-147">Search-Flags</span></span>           | <span data-ttu-id="e65bd-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e65bd-148">0x00000000</span></span>                                 |
| <span data-ttu-id="e65bd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-149">System-Flags</span></span>           | <span data-ttu-id="e65bd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e65bd-150">0x00000010</span></span>                                 |
| <span data-ttu-id="e65bd-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e65bd-151">Classes used in</span></span>        | [<span data-ttu-id="e65bd-152">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e65bd-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e65bd-153">亞當</span><span class="sxs-lookup"><span data-stu-id="e65bd-153">ADAM</span></span>



| <span data-ttu-id="e65bd-154">進入</span><span class="sxs-lookup"><span data-stu-id="e65bd-154">Entry</span></span> | <span data-ttu-id="e65bd-155">值</span><span class="sxs-lookup"><span data-stu-id="e65bd-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e65bd-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e65bd-156">Link-Id</span></span>                | <span data-ttu-id="e65bd-157">1044</span><span class="sxs-lookup"><span data-stu-id="e65bd-157">1044</span></span>                                       |
| <span data-ttu-id="e65bd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e65bd-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e65bd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e65bd-159">System-Only</span></span>            | <span data-ttu-id="e65bd-160">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-160">False</span></span>                                      |
| <span data-ttu-id="e65bd-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e65bd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e65bd-162">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-162">False</span></span>                                      |
| <span data-ttu-id="e65bd-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e65bd-163">Is Indexed</span></span>             | <span data-ttu-id="e65bd-164">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-164">False</span></span>                                      |
| <span data-ttu-id="e65bd-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e65bd-165">In Global Catalog</span></span>      | <span data-ttu-id="e65bd-166">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-166">False</span></span>                                      |
| <span data-ttu-id="e65bd-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e65bd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e65bd-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e65bd-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e65bd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e65bd-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e65bd-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-171">Search-Flags</span></span>           | <span data-ttu-id="e65bd-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e65bd-172">0x00000000</span></span>                                 |
| <span data-ttu-id="e65bd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-173">System-Flags</span></span>           | <span data-ttu-id="e65bd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e65bd-174">0x00000010</span></span>                                 |
| <span data-ttu-id="e65bd-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e65bd-175">Classes used in</span></span>        | [<span data-ttu-id="e65bd-176">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e65bd-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e65bd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e65bd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e65bd-178">進入</span><span class="sxs-lookup"><span data-stu-id="e65bd-178">Entry</span></span> | <span data-ttu-id="e65bd-179">值</span><span class="sxs-lookup"><span data-stu-id="e65bd-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e65bd-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e65bd-180">Link-Id</span></span>                | <span data-ttu-id="e65bd-181">1044</span><span class="sxs-lookup"><span data-stu-id="e65bd-181">1044</span></span>                                       |
| <span data-ttu-id="e65bd-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e65bd-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e65bd-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e65bd-183">System-Only</span></span>            | <span data-ttu-id="e65bd-184">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-184">False</span></span>                                      |
| <span data-ttu-id="e65bd-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e65bd-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e65bd-186">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-186">False</span></span>                                      |
| <span data-ttu-id="e65bd-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e65bd-187">Is Indexed</span></span>             | <span data-ttu-id="e65bd-188">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-188">False</span></span>                                      |
| <span data-ttu-id="e65bd-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e65bd-189">In Global Catalog</span></span>      | <span data-ttu-id="e65bd-190">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-190">False</span></span>                                      |
| <span data-ttu-id="e65bd-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e65bd-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e65bd-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e65bd-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e65bd-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e65bd-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e65bd-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-195">Search-Flags</span></span>           | <span data-ttu-id="e65bd-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e65bd-196">0x00000000</span></span>                                 |
| <span data-ttu-id="e65bd-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-197">System-Flags</span></span>           | <span data-ttu-id="e65bd-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e65bd-198">0x00000010</span></span>                                 |
| <span data-ttu-id="e65bd-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e65bd-199">Classes used in</span></span>        | [<span data-ttu-id="e65bd-200">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e65bd-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e65bd-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e65bd-201">Windows Server 2008</span></span>



| <span data-ttu-id="e65bd-202">進入</span><span class="sxs-lookup"><span data-stu-id="e65bd-202">Entry</span></span> | <span data-ttu-id="e65bd-203">值</span><span class="sxs-lookup"><span data-stu-id="e65bd-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e65bd-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e65bd-204">Link-Id</span></span>                | <span data-ttu-id="e65bd-205">1044</span><span class="sxs-lookup"><span data-stu-id="e65bd-205">1044</span></span>                                       |
| <span data-ttu-id="e65bd-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e65bd-206">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e65bd-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e65bd-207">System-Only</span></span>            | <span data-ttu-id="e65bd-208">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-208">False</span></span>                                      |
| <span data-ttu-id="e65bd-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e65bd-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e65bd-210">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-210">False</span></span>                                      |
| <span data-ttu-id="e65bd-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e65bd-211">Is Indexed</span></span>             | <span data-ttu-id="e65bd-212">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-212">False</span></span>                                      |
| <span data-ttu-id="e65bd-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e65bd-213">In Global Catalog</span></span>      | <span data-ttu-id="e65bd-214">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-214">False</span></span>                                      |
| <span data-ttu-id="e65bd-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e65bd-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e65bd-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e65bd-216">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e65bd-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e65bd-217">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e65bd-218">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-219">Search-Flags</span></span>           | <span data-ttu-id="e65bd-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e65bd-220">0x00000000</span></span>                                 |
| <span data-ttu-id="e65bd-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-221">System-Flags</span></span>           | <span data-ttu-id="e65bd-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e65bd-222">0x00000010</span></span>                                 |
| <span data-ttu-id="e65bd-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e65bd-223">Classes used in</span></span>        | [<span data-ttu-id="e65bd-224">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e65bd-224">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e65bd-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e65bd-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e65bd-226">進入</span><span class="sxs-lookup"><span data-stu-id="e65bd-226">Entry</span></span> | <span data-ttu-id="e65bd-227">值</span><span class="sxs-lookup"><span data-stu-id="e65bd-227">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e65bd-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e65bd-228">Link-Id</span></span>                | <span data-ttu-id="e65bd-229">1044</span><span class="sxs-lookup"><span data-stu-id="e65bd-229">1044</span></span>                                       |
| <span data-ttu-id="e65bd-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e65bd-230">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e65bd-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e65bd-231">System-Only</span></span>            | <span data-ttu-id="e65bd-232">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-232">False</span></span>                                      |
| <span data-ttu-id="e65bd-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e65bd-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e65bd-234">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-234">False</span></span>                                      |
| <span data-ttu-id="e65bd-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e65bd-235">Is Indexed</span></span>             | <span data-ttu-id="e65bd-236">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-236">False</span></span>                                      |
| <span data-ttu-id="e65bd-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e65bd-237">In Global Catalog</span></span>      | <span data-ttu-id="e65bd-238">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-238">False</span></span>                                      |
| <span data-ttu-id="e65bd-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e65bd-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e65bd-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e65bd-240">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e65bd-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e65bd-241">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e65bd-242">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-243">Search-Flags</span></span>           | <span data-ttu-id="e65bd-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e65bd-244">0x00000000</span></span>                                 |
| <span data-ttu-id="e65bd-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-245">System-Flags</span></span>           | <span data-ttu-id="e65bd-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e65bd-246">0x00000010</span></span>                                 |
| <span data-ttu-id="e65bd-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e65bd-247">Classes used in</span></span>        | [<span data-ttu-id="e65bd-248">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e65bd-248">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e65bd-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e65bd-249">Windows Server 2012</span></span>



| <span data-ttu-id="e65bd-250">進入</span><span class="sxs-lookup"><span data-stu-id="e65bd-250">Entry</span></span> | <span data-ttu-id="e65bd-251">值</span><span class="sxs-lookup"><span data-stu-id="e65bd-251">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e65bd-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e65bd-252">Link-Id</span></span>                | <span data-ttu-id="e65bd-253">1044</span><span class="sxs-lookup"><span data-stu-id="e65bd-253">1044</span></span>                                       |
| <span data-ttu-id="e65bd-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e65bd-254">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e65bd-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="e65bd-255">System-Only</span></span>            | <span data-ttu-id="e65bd-256">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-256">False</span></span>                                      |
| <span data-ttu-id="e65bd-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e65bd-257">Is-Single-Valued</span></span>       | <span data-ttu-id="e65bd-258">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-258">False</span></span>                                      |
| <span data-ttu-id="e65bd-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e65bd-259">Is Indexed</span></span>             | <span data-ttu-id="e65bd-260">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-260">False</span></span>                                      |
| <span data-ttu-id="e65bd-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e65bd-261">In Global Catalog</span></span>      | <span data-ttu-id="e65bd-262">否</span><span class="sxs-lookup"><span data-stu-id="e65bd-262">False</span></span>                                      |
| <span data-ttu-id="e65bd-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e65bd-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="e65bd-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e65bd-264">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e65bd-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e65bd-265">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e65bd-266">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e65bd-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-267">Search-Flags</span></span>           | <span data-ttu-id="e65bd-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e65bd-268">0x00000000</span></span>                                 |
| <span data-ttu-id="e65bd-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e65bd-269">System-Flags</span></span>           | <span data-ttu-id="e65bd-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e65bd-270">0x00000010</span></span>                                 |
| <span data-ttu-id="e65bd-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e65bd-271">Classes used in</span></span>        | [<span data-ttu-id="e65bd-272">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="e65bd-272">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





