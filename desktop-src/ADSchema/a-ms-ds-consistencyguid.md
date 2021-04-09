---
title: MS DS-一致性-Guid 屬性
description: 這個屬性是用來藉由比較 Guid 來檢查目錄與另一個物件、資料庫或應用程式之間的一致性。
ms.assetid: 1372f46a-5569-4b06-9803-7d3862cdb745
ms.tgt_platform: multiple
keywords:
- MS DS-一致性-Guid 屬性 AD 架構
- ConsistencyGuid 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbea1e9fba4ac28f968fdd61a054f55fe47deb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845211"
---
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="db136-105">MS DS-一致性-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="db136-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="db136-106">這個屬性是用來藉由比較 Guid 來檢查目錄與另一個物件、資料庫或應用程式之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="db136-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="db136-107">進入</span><span class="sxs-lookup"><span data-stu-id="db136-107">Entry</span></span> | <span data-ttu-id="db136-108">值</span><span class="sxs-lookup"><span data-stu-id="db136-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="db136-109">CN</span><span class="sxs-lookup"><span data-stu-id="db136-109">CN</span></span>                | <span data-ttu-id="db136-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="db136-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="db136-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="db136-111">Ldap-Display-Name</span></span> | <span data-ttu-id="db136-112">ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="db136-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="db136-113">大小</span><span class="sxs-lookup"><span data-stu-id="db136-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="db136-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="db136-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="db136-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="db136-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="db136-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db136-116">Attribute-Id</span></span>      | <span data-ttu-id="db136-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="db136-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="db136-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="db136-118">System-Id-Guid</span></span>    | <span data-ttu-id="db136-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="db136-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="db136-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="db136-120">Syntax</span></span>            | [<span data-ttu-id="db136-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="db136-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="db136-122">實作</span><span class="sxs-lookup"><span data-stu-id="db136-122">Implementations</span></span>

-   [<span data-ttu-id="db136-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="db136-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="db136-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db136-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db136-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="db136-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="db136-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db136-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db136-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db136-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db136-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db136-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db136-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db136-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="db136-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db136-130">Windows 2000 Server</span></span>



| <span data-ttu-id="db136-131">進入</span><span class="sxs-lookup"><span data-stu-id="db136-131">Entry</span></span> | <span data-ttu-id="db136-132">值</span><span class="sxs-lookup"><span data-stu-id="db136-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db136-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-135">System-Only</span></span>            | <span data-ttu-id="db136-136">否</span><span class="sxs-lookup"><span data-stu-id="db136-136">False</span></span>                           |
| <span data-ttu-id="db136-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-137">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-138">對</span><span class="sxs-lookup"><span data-stu-id="db136-138">True</span></span>                            |
| <span data-ttu-id="db136-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-139">Is Indexed</span></span>             | <span data-ttu-id="db136-140">否</span><span class="sxs-lookup"><span data-stu-id="db136-140">False</span></span>                           |
| <span data-ttu-id="db136-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-141">In Global Catalog</span></span>      | <span data-ttu-id="db136-142">否</span><span class="sxs-lookup"><span data-stu-id="db136-142">False</span></span>                           |
| <span data-ttu-id="db136-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db136-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db136-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db136-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-147">Search-Flags</span></span>           | <span data-ttu-id="db136-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-148">0x00000000</span></span>                      |
| <span data-ttu-id="db136-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-149">System-Flags</span></span>           | <span data-ttu-id="db136-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-150">0x00000010</span></span>                      |
| <span data-ttu-id="db136-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-151">Classes used in</span></span>        | [<span data-ttu-id="db136-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="db136-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="db136-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db136-153">Windows Server 2003</span></span>



| <span data-ttu-id="db136-154">進入</span><span class="sxs-lookup"><span data-stu-id="db136-154">Entry</span></span> | <span data-ttu-id="db136-155">值</span><span class="sxs-lookup"><span data-stu-id="db136-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db136-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-158">System-Only</span></span>            | <span data-ttu-id="db136-159">否</span><span class="sxs-lookup"><span data-stu-id="db136-159">False</span></span>                           |
| <span data-ttu-id="db136-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-160">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-161">對</span><span class="sxs-lookup"><span data-stu-id="db136-161">True</span></span>                            |
| <span data-ttu-id="db136-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-162">Is Indexed</span></span>             | <span data-ttu-id="db136-163">否</span><span class="sxs-lookup"><span data-stu-id="db136-163">False</span></span>                           |
| <span data-ttu-id="db136-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-164">In Global Catalog</span></span>      | <span data-ttu-id="db136-165">否</span><span class="sxs-lookup"><span data-stu-id="db136-165">False</span></span>                           |
| <span data-ttu-id="db136-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db136-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db136-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db136-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-170">Search-Flags</span></span>           | <span data-ttu-id="db136-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-171">0x00000000</span></span>                      |
| <span data-ttu-id="db136-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-172">System-Flags</span></span>           | <span data-ttu-id="db136-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-173">0x00000010</span></span>                      |
| <span data-ttu-id="db136-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-174">Classes used in</span></span>        | [<span data-ttu-id="db136-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="db136-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="db136-176">亞當</span><span class="sxs-lookup"><span data-stu-id="db136-176">ADAM</span></span>



| <span data-ttu-id="db136-177">進入</span><span class="sxs-lookup"><span data-stu-id="db136-177">Entry</span></span> | <span data-ttu-id="db136-178">值</span><span class="sxs-lookup"><span data-stu-id="db136-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db136-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-181">System-Only</span></span>            | <span data-ttu-id="db136-182">否</span><span class="sxs-lookup"><span data-stu-id="db136-182">False</span></span>                           |
| <span data-ttu-id="db136-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-183">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-184">對</span><span class="sxs-lookup"><span data-stu-id="db136-184">True</span></span>                            |
| <span data-ttu-id="db136-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-185">Is Indexed</span></span>             | <span data-ttu-id="db136-186">否</span><span class="sxs-lookup"><span data-stu-id="db136-186">False</span></span>                           |
| <span data-ttu-id="db136-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-187">In Global Catalog</span></span>      | <span data-ttu-id="db136-188">否</span><span class="sxs-lookup"><span data-stu-id="db136-188">False</span></span>                           |
| <span data-ttu-id="db136-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db136-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db136-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db136-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-193">Search-Flags</span></span>           | <span data-ttu-id="db136-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-194">0x00000000</span></span>                      |
| <span data-ttu-id="db136-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-195">System-Flags</span></span>           | <span data-ttu-id="db136-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-196">0x00000010</span></span>                      |
| <span data-ttu-id="db136-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-197">Classes used in</span></span>        | [<span data-ttu-id="db136-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="db136-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db136-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db136-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db136-200">進入</span><span class="sxs-lookup"><span data-stu-id="db136-200">Entry</span></span> | <span data-ttu-id="db136-201">值</span><span class="sxs-lookup"><span data-stu-id="db136-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db136-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-204">System-Only</span></span>            | <span data-ttu-id="db136-205">否</span><span class="sxs-lookup"><span data-stu-id="db136-205">False</span></span>                           |
| <span data-ttu-id="db136-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-206">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-207">對</span><span class="sxs-lookup"><span data-stu-id="db136-207">True</span></span>                            |
| <span data-ttu-id="db136-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-208">Is Indexed</span></span>             | <span data-ttu-id="db136-209">否</span><span class="sxs-lookup"><span data-stu-id="db136-209">False</span></span>                           |
| <span data-ttu-id="db136-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-210">In Global Catalog</span></span>      | <span data-ttu-id="db136-211">否</span><span class="sxs-lookup"><span data-stu-id="db136-211">False</span></span>                           |
| <span data-ttu-id="db136-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db136-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db136-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db136-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-216">Search-Flags</span></span>           | <span data-ttu-id="db136-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-217">0x00000000</span></span>                      |
| <span data-ttu-id="db136-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-218">System-Flags</span></span>           | <span data-ttu-id="db136-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-219">0x00000010</span></span>                      |
| <span data-ttu-id="db136-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-220">Classes used in</span></span>        | [<span data-ttu-id="db136-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="db136-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db136-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db136-222">Windows Server 2008</span></span>



| <span data-ttu-id="db136-223">進入</span><span class="sxs-lookup"><span data-stu-id="db136-223">Entry</span></span> | <span data-ttu-id="db136-224">值</span><span class="sxs-lookup"><span data-stu-id="db136-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db136-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-227">System-Only</span></span>            | <span data-ttu-id="db136-228">否</span><span class="sxs-lookup"><span data-stu-id="db136-228">False</span></span>                           |
| <span data-ttu-id="db136-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-229">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-230">對</span><span class="sxs-lookup"><span data-stu-id="db136-230">True</span></span>                            |
| <span data-ttu-id="db136-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-231">Is Indexed</span></span>             | <span data-ttu-id="db136-232">否</span><span class="sxs-lookup"><span data-stu-id="db136-232">False</span></span>                           |
| <span data-ttu-id="db136-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-233">In Global Catalog</span></span>      | <span data-ttu-id="db136-234">否</span><span class="sxs-lookup"><span data-stu-id="db136-234">False</span></span>                           |
| <span data-ttu-id="db136-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db136-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db136-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db136-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-239">Search-Flags</span></span>           | <span data-ttu-id="db136-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-240">0x00000000</span></span>                      |
| <span data-ttu-id="db136-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-241">System-Flags</span></span>           | <span data-ttu-id="db136-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-242">0x00000010</span></span>                      |
| <span data-ttu-id="db136-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-243">Classes used in</span></span>        | [<span data-ttu-id="db136-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="db136-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db136-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db136-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db136-246">進入</span><span class="sxs-lookup"><span data-stu-id="db136-246">Entry</span></span> | <span data-ttu-id="db136-247">值</span><span class="sxs-lookup"><span data-stu-id="db136-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db136-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-250">System-Only</span></span>            | <span data-ttu-id="db136-251">否</span><span class="sxs-lookup"><span data-stu-id="db136-251">False</span></span>                           |
| <span data-ttu-id="db136-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-252">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-253">對</span><span class="sxs-lookup"><span data-stu-id="db136-253">True</span></span>                            |
| <span data-ttu-id="db136-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-254">Is Indexed</span></span>             | <span data-ttu-id="db136-255">否</span><span class="sxs-lookup"><span data-stu-id="db136-255">False</span></span>                           |
| <span data-ttu-id="db136-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-256">In Global Catalog</span></span>      | <span data-ttu-id="db136-257">否</span><span class="sxs-lookup"><span data-stu-id="db136-257">False</span></span>                           |
| <span data-ttu-id="db136-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db136-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db136-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db136-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-262">Search-Flags</span></span>           | <span data-ttu-id="db136-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-263">0x00000000</span></span>                      |
| <span data-ttu-id="db136-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-264">System-Flags</span></span>           | <span data-ttu-id="db136-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-265">0x00000010</span></span>                      |
| <span data-ttu-id="db136-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-266">Classes used in</span></span>        | [<span data-ttu-id="db136-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="db136-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db136-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db136-268">Windows Server 2012</span></span>



| <span data-ttu-id="db136-269">進入</span><span class="sxs-lookup"><span data-stu-id="db136-269">Entry</span></span> | <span data-ttu-id="db136-270">值</span><span class="sxs-lookup"><span data-stu-id="db136-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="db136-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="db136-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db136-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="db136-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="db136-273">System-Only</span></span>            | <span data-ttu-id="db136-274">否</span><span class="sxs-lookup"><span data-stu-id="db136-274">False</span></span>                           |
| <span data-ttu-id="db136-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="db136-275">Is-Single-Valued</span></span>       | <span data-ttu-id="db136-276">對</span><span class="sxs-lookup"><span data-stu-id="db136-276">True</span></span>                            |
| <span data-ttu-id="db136-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="db136-277">Is Indexed</span></span>             | <span data-ttu-id="db136-278">否</span><span class="sxs-lookup"><span data-stu-id="db136-278">False</span></span>                           |
| <span data-ttu-id="db136-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="db136-279">In Global Catalog</span></span>      | <span data-ttu-id="db136-280">否</span><span class="sxs-lookup"><span data-stu-id="db136-280">False</span></span>                           |
| <span data-ttu-id="db136-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="db136-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="db136-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="db136-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="db136-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db136-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="db136-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db136-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="db136-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-285">Search-Flags</span></span>           | <span data-ttu-id="db136-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db136-286">0x00000000</span></span>                      |
| <span data-ttu-id="db136-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db136-287">System-Flags</span></span>           | <span data-ttu-id="db136-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db136-288">0x00000010</span></span>                      |
| <span data-ttu-id="db136-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="db136-289">Classes used in</span></span>        | [<span data-ttu-id="db136-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="db136-290">**Top**</span></span>](c-top.md)<br/> |



 

 





