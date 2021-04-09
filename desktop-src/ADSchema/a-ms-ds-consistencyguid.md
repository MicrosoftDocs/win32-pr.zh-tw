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
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="50980-105">MS DS-一致性-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="50980-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="50980-106">這個屬性是用來藉由比較 Guid 來檢查目錄與另一個物件、資料庫或應用程式之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="50980-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="50980-107">進入</span><span class="sxs-lookup"><span data-stu-id="50980-107">Entry</span></span> | <span data-ttu-id="50980-108">值</span><span class="sxs-lookup"><span data-stu-id="50980-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="50980-109">CN</span><span class="sxs-lookup"><span data-stu-id="50980-109">CN</span></span>                | <span data-ttu-id="50980-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="50980-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="50980-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="50980-111">Ldap-Display-Name</span></span> | <span data-ttu-id="50980-112">ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="50980-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="50980-113">大小</span><span class="sxs-lookup"><span data-stu-id="50980-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="50980-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="50980-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="50980-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="50980-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="50980-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50980-116">Attribute-Id</span></span>      | <span data-ttu-id="50980-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="50980-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="50980-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="50980-118">System-Id-Guid</span></span>    | <span data-ttu-id="50980-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="50980-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="50980-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="50980-120">Syntax</span></span>            | [<span data-ttu-id="50980-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="50980-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="50980-122">實作</span><span class="sxs-lookup"><span data-stu-id="50980-122">Implementations</span></span>

-   [<span data-ttu-id="50980-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="50980-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="50980-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50980-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50980-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="50980-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="50980-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50980-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50980-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50980-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50980-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50980-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50980-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50980-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="50980-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="50980-130">Windows 2000 Server</span></span>



| <span data-ttu-id="50980-131">進入</span><span class="sxs-lookup"><span data-stu-id="50980-131">Entry</span></span> | <span data-ttu-id="50980-132">值</span><span class="sxs-lookup"><span data-stu-id="50980-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="50980-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50980-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50980-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="50980-135">System-Only</span></span>            | <span data-ttu-id="50980-136">否</span><span class="sxs-lookup"><span data-stu-id="50980-136">False</span></span>                           |
| <span data-ttu-id="50980-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50980-137">Is-Single-Valued</span></span>       | <span data-ttu-id="50980-138">對</span><span class="sxs-lookup"><span data-stu-id="50980-138">True</span></span>                            |
| <span data-ttu-id="50980-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50980-139">Is Indexed</span></span>             | <span data-ttu-id="50980-140">否</span><span class="sxs-lookup"><span data-stu-id="50980-140">False</span></span>                           |
| <span data-ttu-id="50980-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50980-141">In Global Catalog</span></span>      | <span data-ttu-id="50980-142">否</span><span class="sxs-lookup"><span data-stu-id="50980-142">False</span></span>                           |
| <span data-ttu-id="50980-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50980-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="50980-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50980-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="50980-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50980-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="50980-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50980-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="50980-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-147">Search-Flags</span></span>           | <span data-ttu-id="50980-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50980-148">0x00000000</span></span>                      |
| <span data-ttu-id="50980-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-149">System-Flags</span></span>           | <span data-ttu-id="50980-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50980-150">0x00000010</span></span>                      |
| <span data-ttu-id="50980-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50980-151">Classes used in</span></span>        | [<span data-ttu-id="50980-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="50980-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="50980-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50980-153">Windows Server 2003</span></span>



| <span data-ttu-id="50980-154">進入</span><span class="sxs-lookup"><span data-stu-id="50980-154">Entry</span></span> | <span data-ttu-id="50980-155">值</span><span class="sxs-lookup"><span data-stu-id="50980-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="50980-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50980-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50980-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="50980-158">System-Only</span></span>            | <span data-ttu-id="50980-159">否</span><span class="sxs-lookup"><span data-stu-id="50980-159">False</span></span>                           |
| <span data-ttu-id="50980-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50980-160">Is-Single-Valued</span></span>       | <span data-ttu-id="50980-161">對</span><span class="sxs-lookup"><span data-stu-id="50980-161">True</span></span>                            |
| <span data-ttu-id="50980-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50980-162">Is Indexed</span></span>             | <span data-ttu-id="50980-163">否</span><span class="sxs-lookup"><span data-stu-id="50980-163">False</span></span>                           |
| <span data-ttu-id="50980-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50980-164">In Global Catalog</span></span>      | <span data-ttu-id="50980-165">否</span><span class="sxs-lookup"><span data-stu-id="50980-165">False</span></span>                           |
| <span data-ttu-id="50980-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50980-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="50980-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50980-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="50980-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50980-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="50980-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50980-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="50980-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-170">Search-Flags</span></span>           | <span data-ttu-id="50980-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50980-171">0x00000000</span></span>                      |
| <span data-ttu-id="50980-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-172">System-Flags</span></span>           | <span data-ttu-id="50980-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50980-173">0x00000010</span></span>                      |
| <span data-ttu-id="50980-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50980-174">Classes used in</span></span>        | [<span data-ttu-id="50980-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="50980-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="50980-176">亞當</span><span class="sxs-lookup"><span data-stu-id="50980-176">ADAM</span></span>



| <span data-ttu-id="50980-177">進入</span><span class="sxs-lookup"><span data-stu-id="50980-177">Entry</span></span> | <span data-ttu-id="50980-178">值</span><span class="sxs-lookup"><span data-stu-id="50980-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="50980-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50980-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50980-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="50980-181">System-Only</span></span>            | <span data-ttu-id="50980-182">否</span><span class="sxs-lookup"><span data-stu-id="50980-182">False</span></span>                           |
| <span data-ttu-id="50980-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50980-183">Is-Single-Valued</span></span>       | <span data-ttu-id="50980-184">對</span><span class="sxs-lookup"><span data-stu-id="50980-184">True</span></span>                            |
| <span data-ttu-id="50980-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50980-185">Is Indexed</span></span>             | <span data-ttu-id="50980-186">否</span><span class="sxs-lookup"><span data-stu-id="50980-186">False</span></span>                           |
| <span data-ttu-id="50980-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50980-187">In Global Catalog</span></span>      | <span data-ttu-id="50980-188">否</span><span class="sxs-lookup"><span data-stu-id="50980-188">False</span></span>                           |
| <span data-ttu-id="50980-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50980-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="50980-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50980-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="50980-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50980-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="50980-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50980-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="50980-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-193">Search-Flags</span></span>           | <span data-ttu-id="50980-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50980-194">0x00000000</span></span>                      |
| <span data-ttu-id="50980-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-195">System-Flags</span></span>           | <span data-ttu-id="50980-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50980-196">0x00000010</span></span>                      |
| <span data-ttu-id="50980-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50980-197">Classes used in</span></span>        | [<span data-ttu-id="50980-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="50980-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50980-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50980-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50980-200">進入</span><span class="sxs-lookup"><span data-stu-id="50980-200">Entry</span></span> | <span data-ttu-id="50980-201">值</span><span class="sxs-lookup"><span data-stu-id="50980-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="50980-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50980-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50980-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="50980-204">System-Only</span></span>            | <span data-ttu-id="50980-205">否</span><span class="sxs-lookup"><span data-stu-id="50980-205">False</span></span>                           |
| <span data-ttu-id="50980-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50980-206">Is-Single-Valued</span></span>       | <span data-ttu-id="50980-207">對</span><span class="sxs-lookup"><span data-stu-id="50980-207">True</span></span>                            |
| <span data-ttu-id="50980-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50980-208">Is Indexed</span></span>             | <span data-ttu-id="50980-209">否</span><span class="sxs-lookup"><span data-stu-id="50980-209">False</span></span>                           |
| <span data-ttu-id="50980-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50980-210">In Global Catalog</span></span>      | <span data-ttu-id="50980-211">否</span><span class="sxs-lookup"><span data-stu-id="50980-211">False</span></span>                           |
| <span data-ttu-id="50980-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50980-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="50980-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50980-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="50980-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50980-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="50980-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50980-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="50980-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-216">Search-Flags</span></span>           | <span data-ttu-id="50980-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50980-217">0x00000000</span></span>                      |
| <span data-ttu-id="50980-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-218">System-Flags</span></span>           | <span data-ttu-id="50980-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50980-219">0x00000010</span></span>                      |
| <span data-ttu-id="50980-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50980-220">Classes used in</span></span>        | [<span data-ttu-id="50980-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="50980-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="50980-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50980-222">Windows Server 2008</span></span>



| <span data-ttu-id="50980-223">進入</span><span class="sxs-lookup"><span data-stu-id="50980-223">Entry</span></span> | <span data-ttu-id="50980-224">值</span><span class="sxs-lookup"><span data-stu-id="50980-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="50980-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50980-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50980-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="50980-227">System-Only</span></span>            | <span data-ttu-id="50980-228">否</span><span class="sxs-lookup"><span data-stu-id="50980-228">False</span></span>                           |
| <span data-ttu-id="50980-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50980-229">Is-Single-Valued</span></span>       | <span data-ttu-id="50980-230">對</span><span class="sxs-lookup"><span data-stu-id="50980-230">True</span></span>                            |
| <span data-ttu-id="50980-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50980-231">Is Indexed</span></span>             | <span data-ttu-id="50980-232">否</span><span class="sxs-lookup"><span data-stu-id="50980-232">False</span></span>                           |
| <span data-ttu-id="50980-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50980-233">In Global Catalog</span></span>      | <span data-ttu-id="50980-234">否</span><span class="sxs-lookup"><span data-stu-id="50980-234">False</span></span>                           |
| <span data-ttu-id="50980-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50980-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="50980-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50980-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="50980-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50980-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="50980-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50980-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="50980-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-239">Search-Flags</span></span>           | <span data-ttu-id="50980-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50980-240">0x00000000</span></span>                      |
| <span data-ttu-id="50980-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-241">System-Flags</span></span>           | <span data-ttu-id="50980-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50980-242">0x00000010</span></span>                      |
| <span data-ttu-id="50980-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50980-243">Classes used in</span></span>        | [<span data-ttu-id="50980-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="50980-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50980-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50980-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50980-246">進入</span><span class="sxs-lookup"><span data-stu-id="50980-246">Entry</span></span> | <span data-ttu-id="50980-247">值</span><span class="sxs-lookup"><span data-stu-id="50980-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="50980-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50980-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50980-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="50980-250">System-Only</span></span>            | <span data-ttu-id="50980-251">否</span><span class="sxs-lookup"><span data-stu-id="50980-251">False</span></span>                           |
| <span data-ttu-id="50980-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50980-252">Is-Single-Valued</span></span>       | <span data-ttu-id="50980-253">對</span><span class="sxs-lookup"><span data-stu-id="50980-253">True</span></span>                            |
| <span data-ttu-id="50980-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50980-254">Is Indexed</span></span>             | <span data-ttu-id="50980-255">否</span><span class="sxs-lookup"><span data-stu-id="50980-255">False</span></span>                           |
| <span data-ttu-id="50980-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50980-256">In Global Catalog</span></span>      | <span data-ttu-id="50980-257">否</span><span class="sxs-lookup"><span data-stu-id="50980-257">False</span></span>                           |
| <span data-ttu-id="50980-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50980-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="50980-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50980-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="50980-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50980-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="50980-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50980-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="50980-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-262">Search-Flags</span></span>           | <span data-ttu-id="50980-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50980-263">0x00000000</span></span>                      |
| <span data-ttu-id="50980-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-264">System-Flags</span></span>           | <span data-ttu-id="50980-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50980-265">0x00000010</span></span>                      |
| <span data-ttu-id="50980-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50980-266">Classes used in</span></span>        | [<span data-ttu-id="50980-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="50980-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50980-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50980-268">Windows Server 2012</span></span>



| <span data-ttu-id="50980-269">進入</span><span class="sxs-lookup"><span data-stu-id="50980-269">Entry</span></span> | <span data-ttu-id="50980-270">值</span><span class="sxs-lookup"><span data-stu-id="50980-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="50980-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50980-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50980-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="50980-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="50980-273">System-Only</span></span>            | <span data-ttu-id="50980-274">否</span><span class="sxs-lookup"><span data-stu-id="50980-274">False</span></span>                           |
| <span data-ttu-id="50980-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50980-275">Is-Single-Valued</span></span>       | <span data-ttu-id="50980-276">對</span><span class="sxs-lookup"><span data-stu-id="50980-276">True</span></span>                            |
| <span data-ttu-id="50980-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50980-277">Is Indexed</span></span>             | <span data-ttu-id="50980-278">否</span><span class="sxs-lookup"><span data-stu-id="50980-278">False</span></span>                           |
| <span data-ttu-id="50980-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50980-279">In Global Catalog</span></span>      | <span data-ttu-id="50980-280">否</span><span class="sxs-lookup"><span data-stu-id="50980-280">False</span></span>                           |
| <span data-ttu-id="50980-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50980-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="50980-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50980-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="50980-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50980-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="50980-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50980-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="50980-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-285">Search-Flags</span></span>           | <span data-ttu-id="50980-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50980-286">0x00000000</span></span>                      |
| <span data-ttu-id="50980-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50980-287">System-Flags</span></span>           | <span data-ttu-id="50980-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50980-288">0x00000010</span></span>                      |
| <span data-ttu-id="50980-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50980-289">Classes used in</span></span>        | [<span data-ttu-id="50980-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="50980-290">**Top**</span></span>](c-top.md)<br/> |



 

 





