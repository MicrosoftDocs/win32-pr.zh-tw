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
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="805c3-105">MS DS-一致性-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="805c3-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="805c3-106">這個屬性是用來藉由比較 Guid 來檢查目錄與另一個物件、資料庫或應用程式之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="805c3-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="805c3-107">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-107">Entry</span></span> | <span data-ttu-id="805c3-108">值</span><span class="sxs-lookup"><span data-stu-id="805c3-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="805c3-109">CN</span><span class="sxs-lookup"><span data-stu-id="805c3-109">CN</span></span>                | <span data-ttu-id="805c3-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="805c3-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="805c3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="805c3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="805c3-112">ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="805c3-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="805c3-113">大小</span><span class="sxs-lookup"><span data-stu-id="805c3-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="805c3-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="805c3-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="805c3-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="805c3-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="805c3-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-116">Attribute-Id</span></span>      | <span data-ttu-id="805c3-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="805c3-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="805c3-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="805c3-118">System-Id-Guid</span></span>    | <span data-ttu-id="805c3-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="805c3-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="805c3-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="805c3-120">Syntax</span></span>            | [<span data-ttu-id="805c3-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="805c3-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="805c3-122">實作</span><span class="sxs-lookup"><span data-stu-id="805c3-122">Implementations</span></span>

-   [<span data-ttu-id="805c3-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="805c3-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="805c3-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="805c3-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="805c3-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="805c3-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="805c3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="805c3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="805c3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="805c3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="805c3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="805c3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="805c3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="805c3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="805c3-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="805c3-130">Windows 2000 Server</span></span>



| <span data-ttu-id="805c3-131">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-131">Entry</span></span> | <span data-ttu-id="805c3-132">值</span><span class="sxs-lookup"><span data-stu-id="805c3-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="805c3-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="805c3-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="805c3-135">System-Only</span></span>            | <span data-ttu-id="805c3-136">否</span><span class="sxs-lookup"><span data-stu-id="805c3-136">False</span></span>                           |
| <span data-ttu-id="805c3-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="805c3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="805c3-138">對</span><span class="sxs-lookup"><span data-stu-id="805c3-138">True</span></span>                            |
| <span data-ttu-id="805c3-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="805c3-139">Is Indexed</span></span>             | <span data-ttu-id="805c3-140">否</span><span class="sxs-lookup"><span data-stu-id="805c3-140">False</span></span>                           |
| <span data-ttu-id="805c3-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="805c3-141">In Global Catalog</span></span>      | <span data-ttu-id="805c3-142">否</span><span class="sxs-lookup"><span data-stu-id="805c3-142">False</span></span>                           |
| <span data-ttu-id="805c3-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="805c3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="805c3-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="805c3-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="805c3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="805c3-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="805c3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="805c3-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="805c3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-147">Search-Flags</span></span>           | <span data-ttu-id="805c3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="805c3-148">0x00000000</span></span>                      |
| <span data-ttu-id="805c3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-149">System-Flags</span></span>           | <span data-ttu-id="805c3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="805c3-150">0x00000010</span></span>                      |
| <span data-ttu-id="805c3-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="805c3-151">Classes used in</span></span>        | [<span data-ttu-id="805c3-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="805c3-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="805c3-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="805c3-153">Windows Server 2003</span></span>



| <span data-ttu-id="805c3-154">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-154">Entry</span></span> | <span data-ttu-id="805c3-155">值</span><span class="sxs-lookup"><span data-stu-id="805c3-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="805c3-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="805c3-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="805c3-158">System-Only</span></span>            | <span data-ttu-id="805c3-159">否</span><span class="sxs-lookup"><span data-stu-id="805c3-159">False</span></span>                           |
| <span data-ttu-id="805c3-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="805c3-160">Is-Single-Valued</span></span>       | <span data-ttu-id="805c3-161">對</span><span class="sxs-lookup"><span data-stu-id="805c3-161">True</span></span>                            |
| <span data-ttu-id="805c3-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="805c3-162">Is Indexed</span></span>             | <span data-ttu-id="805c3-163">否</span><span class="sxs-lookup"><span data-stu-id="805c3-163">False</span></span>                           |
| <span data-ttu-id="805c3-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="805c3-164">In Global Catalog</span></span>      | <span data-ttu-id="805c3-165">否</span><span class="sxs-lookup"><span data-stu-id="805c3-165">False</span></span>                           |
| <span data-ttu-id="805c3-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="805c3-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="805c3-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="805c3-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="805c3-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="805c3-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="805c3-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="805c3-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="805c3-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-170">Search-Flags</span></span>           | <span data-ttu-id="805c3-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="805c3-171">0x00000000</span></span>                      |
| <span data-ttu-id="805c3-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-172">System-Flags</span></span>           | <span data-ttu-id="805c3-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="805c3-173">0x00000010</span></span>                      |
| <span data-ttu-id="805c3-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="805c3-174">Classes used in</span></span>        | [<span data-ttu-id="805c3-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="805c3-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="805c3-176">亞當</span><span class="sxs-lookup"><span data-stu-id="805c3-176">ADAM</span></span>



| <span data-ttu-id="805c3-177">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-177">Entry</span></span> | <span data-ttu-id="805c3-178">值</span><span class="sxs-lookup"><span data-stu-id="805c3-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="805c3-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="805c3-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="805c3-181">System-Only</span></span>            | <span data-ttu-id="805c3-182">否</span><span class="sxs-lookup"><span data-stu-id="805c3-182">False</span></span>                           |
| <span data-ttu-id="805c3-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="805c3-183">Is-Single-Valued</span></span>       | <span data-ttu-id="805c3-184">對</span><span class="sxs-lookup"><span data-stu-id="805c3-184">True</span></span>                            |
| <span data-ttu-id="805c3-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="805c3-185">Is Indexed</span></span>             | <span data-ttu-id="805c3-186">否</span><span class="sxs-lookup"><span data-stu-id="805c3-186">False</span></span>                           |
| <span data-ttu-id="805c3-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="805c3-187">In Global Catalog</span></span>      | <span data-ttu-id="805c3-188">否</span><span class="sxs-lookup"><span data-stu-id="805c3-188">False</span></span>                           |
| <span data-ttu-id="805c3-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="805c3-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="805c3-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="805c3-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="805c3-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="805c3-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="805c3-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="805c3-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="805c3-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-193">Search-Flags</span></span>           | <span data-ttu-id="805c3-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="805c3-194">0x00000000</span></span>                      |
| <span data-ttu-id="805c3-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-195">System-Flags</span></span>           | <span data-ttu-id="805c3-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="805c3-196">0x00000010</span></span>                      |
| <span data-ttu-id="805c3-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="805c3-197">Classes used in</span></span>        | [<span data-ttu-id="805c3-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="805c3-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="805c3-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="805c3-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="805c3-200">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-200">Entry</span></span> | <span data-ttu-id="805c3-201">值</span><span class="sxs-lookup"><span data-stu-id="805c3-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="805c3-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="805c3-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="805c3-204">System-Only</span></span>            | <span data-ttu-id="805c3-205">否</span><span class="sxs-lookup"><span data-stu-id="805c3-205">False</span></span>                           |
| <span data-ttu-id="805c3-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="805c3-206">Is-Single-Valued</span></span>       | <span data-ttu-id="805c3-207">對</span><span class="sxs-lookup"><span data-stu-id="805c3-207">True</span></span>                            |
| <span data-ttu-id="805c3-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="805c3-208">Is Indexed</span></span>             | <span data-ttu-id="805c3-209">否</span><span class="sxs-lookup"><span data-stu-id="805c3-209">False</span></span>                           |
| <span data-ttu-id="805c3-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="805c3-210">In Global Catalog</span></span>      | <span data-ttu-id="805c3-211">否</span><span class="sxs-lookup"><span data-stu-id="805c3-211">False</span></span>                           |
| <span data-ttu-id="805c3-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="805c3-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="805c3-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="805c3-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="805c3-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="805c3-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="805c3-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="805c3-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="805c3-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-216">Search-Flags</span></span>           | <span data-ttu-id="805c3-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="805c3-217">0x00000000</span></span>                      |
| <span data-ttu-id="805c3-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-218">System-Flags</span></span>           | <span data-ttu-id="805c3-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="805c3-219">0x00000010</span></span>                      |
| <span data-ttu-id="805c3-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="805c3-220">Classes used in</span></span>        | [<span data-ttu-id="805c3-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="805c3-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="805c3-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="805c3-222">Windows Server 2008</span></span>



| <span data-ttu-id="805c3-223">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-223">Entry</span></span> | <span data-ttu-id="805c3-224">值</span><span class="sxs-lookup"><span data-stu-id="805c3-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="805c3-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="805c3-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="805c3-227">System-Only</span></span>            | <span data-ttu-id="805c3-228">否</span><span class="sxs-lookup"><span data-stu-id="805c3-228">False</span></span>                           |
| <span data-ttu-id="805c3-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="805c3-229">Is-Single-Valued</span></span>       | <span data-ttu-id="805c3-230">對</span><span class="sxs-lookup"><span data-stu-id="805c3-230">True</span></span>                            |
| <span data-ttu-id="805c3-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="805c3-231">Is Indexed</span></span>             | <span data-ttu-id="805c3-232">否</span><span class="sxs-lookup"><span data-stu-id="805c3-232">False</span></span>                           |
| <span data-ttu-id="805c3-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="805c3-233">In Global Catalog</span></span>      | <span data-ttu-id="805c3-234">否</span><span class="sxs-lookup"><span data-stu-id="805c3-234">False</span></span>                           |
| <span data-ttu-id="805c3-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="805c3-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="805c3-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="805c3-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="805c3-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="805c3-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="805c3-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="805c3-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="805c3-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-239">Search-Flags</span></span>           | <span data-ttu-id="805c3-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="805c3-240">0x00000000</span></span>                      |
| <span data-ttu-id="805c3-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-241">System-Flags</span></span>           | <span data-ttu-id="805c3-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="805c3-242">0x00000010</span></span>                      |
| <span data-ttu-id="805c3-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="805c3-243">Classes used in</span></span>        | [<span data-ttu-id="805c3-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="805c3-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="805c3-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="805c3-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="805c3-246">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-246">Entry</span></span> | <span data-ttu-id="805c3-247">值</span><span class="sxs-lookup"><span data-stu-id="805c3-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="805c3-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="805c3-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="805c3-250">System-Only</span></span>            | <span data-ttu-id="805c3-251">否</span><span class="sxs-lookup"><span data-stu-id="805c3-251">False</span></span>                           |
| <span data-ttu-id="805c3-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="805c3-252">Is-Single-Valued</span></span>       | <span data-ttu-id="805c3-253">對</span><span class="sxs-lookup"><span data-stu-id="805c3-253">True</span></span>                            |
| <span data-ttu-id="805c3-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="805c3-254">Is Indexed</span></span>             | <span data-ttu-id="805c3-255">否</span><span class="sxs-lookup"><span data-stu-id="805c3-255">False</span></span>                           |
| <span data-ttu-id="805c3-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="805c3-256">In Global Catalog</span></span>      | <span data-ttu-id="805c3-257">否</span><span class="sxs-lookup"><span data-stu-id="805c3-257">False</span></span>                           |
| <span data-ttu-id="805c3-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="805c3-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="805c3-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="805c3-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="805c3-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="805c3-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="805c3-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="805c3-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="805c3-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-262">Search-Flags</span></span>           | <span data-ttu-id="805c3-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="805c3-263">0x00000000</span></span>                      |
| <span data-ttu-id="805c3-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-264">System-Flags</span></span>           | <span data-ttu-id="805c3-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="805c3-265">0x00000010</span></span>                      |
| <span data-ttu-id="805c3-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="805c3-266">Classes used in</span></span>        | [<span data-ttu-id="805c3-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="805c3-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="805c3-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="805c3-268">Windows Server 2012</span></span>



| <span data-ttu-id="805c3-269">進入</span><span class="sxs-lookup"><span data-stu-id="805c3-269">Entry</span></span> | <span data-ttu-id="805c3-270">值</span><span class="sxs-lookup"><span data-stu-id="805c3-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="805c3-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="805c3-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="805c3-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="805c3-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="805c3-273">System-Only</span></span>            | <span data-ttu-id="805c3-274">否</span><span class="sxs-lookup"><span data-stu-id="805c3-274">False</span></span>                           |
| <span data-ttu-id="805c3-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="805c3-275">Is-Single-Valued</span></span>       | <span data-ttu-id="805c3-276">對</span><span class="sxs-lookup"><span data-stu-id="805c3-276">True</span></span>                            |
| <span data-ttu-id="805c3-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="805c3-277">Is Indexed</span></span>             | <span data-ttu-id="805c3-278">否</span><span class="sxs-lookup"><span data-stu-id="805c3-278">False</span></span>                           |
| <span data-ttu-id="805c3-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="805c3-279">In Global Catalog</span></span>      | <span data-ttu-id="805c3-280">否</span><span class="sxs-lookup"><span data-stu-id="805c3-280">False</span></span>                           |
| <span data-ttu-id="805c3-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="805c3-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="805c3-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="805c3-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="805c3-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="805c3-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="805c3-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="805c3-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="805c3-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-285">Search-Flags</span></span>           | <span data-ttu-id="805c3-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="805c3-286">0x00000000</span></span>                      |
| <span data-ttu-id="805c3-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="805c3-287">System-Flags</span></span>           | <span data-ttu-id="805c3-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="805c3-288">0x00000010</span></span>                      |
| <span data-ttu-id="805c3-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="805c3-289">Classes used in</span></span>        | [<span data-ttu-id="805c3-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="805c3-290">**Top**</span></span>](c-top.md)<br/> |



 

 





