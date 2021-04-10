---
title: MS DS-一致性-子計數屬性
description: 這個屬性是用來藉由比較子物件的計數，來檢查目錄與另一個物件、資料庫或應用程式之間的一致性。
ms.assetid: f7d6e8f0-963b-45a9-86af-8e51d6de32bb
ms.tgt_platform: multiple
keywords:
- MS DS-一致性-子計數屬性 AD 架構
- ConsistencyChildCount 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Child-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b9c46d1c4519550a91d92d0a82f726a20572490
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107190"
---
# <a name="ms-ds-consistency-child-count-attribute"></a><span data-ttu-id="7de3a-105">MS DS-一致性-子計數屬性</span><span class="sxs-lookup"><span data-stu-id="7de3a-105">MS-DS-Consistency-Child-Count attribute</span></span>

<span data-ttu-id="7de3a-106">這個屬性是用來藉由比較子物件的計數，來檢查目錄與另一個物件、資料庫或應用程式之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="7de3a-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing a count of child objects.</span></span>



| <span data-ttu-id="7de3a-107">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-107">Entry</span></span> | <span data-ttu-id="7de3a-108">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7de3a-109">CN</span><span class="sxs-lookup"><span data-stu-id="7de3a-109">CN</span></span>                | <span data-ttu-id="7de3a-110">MS DS-一致性-子計數</span><span class="sxs-lookup"><span data-stu-id="7de3a-110">MS-DS-Consistency-Child-Count</span></span>        |
| <span data-ttu-id="7de3a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7de3a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7de3a-112">ConsistencyChildCount</span><span class="sxs-lookup"><span data-stu-id="7de3a-112">mS-DS-ConsistencyChildCount</span></span>          |
| <span data-ttu-id="7de3a-113">大小</span><span class="sxs-lookup"><span data-stu-id="7de3a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="7de3a-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7de3a-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7de3a-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7de3a-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7de3a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-116">Attribute-Id</span></span>      | <span data-ttu-id="7de3a-117">1.2.840.113556.1.4.1361</span><span class="sxs-lookup"><span data-stu-id="7de3a-117">1.2.840.113556.1.4.1361</span></span>              |
| <span data-ttu-id="7de3a-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7de3a-118">System-Id-Guid</span></span>    | <span data-ttu-id="7de3a-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="7de3a-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span></span> |
| <span data-ttu-id="7de3a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de3a-120">Syntax</span></span>            | [<span data-ttu-id="7de3a-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="7de3a-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7de3a-122">實作</span><span class="sxs-lookup"><span data-stu-id="7de3a-122">Implementations</span></span>

-   [<span data-ttu-id="7de3a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7de3a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7de3a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7de3a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7de3a-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7de3a-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7de3a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7de3a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7de3a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7de3a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7de3a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7de3a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7de3a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7de3a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7de3a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7de3a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7de3a-131">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-131">Entry</span></span> | <span data-ttu-id="7de3a-132">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7de3a-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de3a-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de3a-135">System-Only</span></span>            | <span data-ttu-id="7de3a-136">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-136">False</span></span>                           |
| <span data-ttu-id="7de3a-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de3a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7de3a-138">對</span><span class="sxs-lookup"><span data-stu-id="7de3a-138">True</span></span>                            |
| <span data-ttu-id="7de3a-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de3a-139">Is Indexed</span></span>             | <span data-ttu-id="7de3a-140">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-140">False</span></span>                           |
| <span data-ttu-id="7de3a-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de3a-141">In Global Catalog</span></span>      | <span data-ttu-id="7de3a-142">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-142">False</span></span>                           |
| <span data-ttu-id="7de3a-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de3a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de3a-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de3a-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7de3a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de3a-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7de3a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de3a-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7de3a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-147">Search-Flags</span></span>           | <span data-ttu-id="7de3a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de3a-148">0x00000000</span></span>                      |
| <span data-ttu-id="7de3a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-149">System-Flags</span></span>           | <span data-ttu-id="7de3a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de3a-150">0x00000010</span></span>                      |
| <span data-ttu-id="7de3a-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de3a-151">Classes used in</span></span>        | [<span data-ttu-id="7de3a-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7de3a-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7de3a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7de3a-153">Windows Server 2003</span></span>



| <span data-ttu-id="7de3a-154">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-154">Entry</span></span> | <span data-ttu-id="7de3a-155">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7de3a-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de3a-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de3a-158">System-Only</span></span>            | <span data-ttu-id="7de3a-159">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-159">False</span></span>                           |
| <span data-ttu-id="7de3a-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de3a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7de3a-161">對</span><span class="sxs-lookup"><span data-stu-id="7de3a-161">True</span></span>                            |
| <span data-ttu-id="7de3a-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de3a-162">Is Indexed</span></span>             | <span data-ttu-id="7de3a-163">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-163">False</span></span>                           |
| <span data-ttu-id="7de3a-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de3a-164">In Global Catalog</span></span>      | <span data-ttu-id="7de3a-165">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-165">False</span></span>                           |
| <span data-ttu-id="7de3a-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de3a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de3a-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de3a-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7de3a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de3a-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7de3a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de3a-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7de3a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-170">Search-Flags</span></span>           | <span data-ttu-id="7de3a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de3a-171">0x00000000</span></span>                      |
| <span data-ttu-id="7de3a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-172">System-Flags</span></span>           | <span data-ttu-id="7de3a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de3a-173">0x00000010</span></span>                      |
| <span data-ttu-id="7de3a-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de3a-174">Classes used in</span></span>        | [<span data-ttu-id="7de3a-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7de3a-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7de3a-176">亞當</span><span class="sxs-lookup"><span data-stu-id="7de3a-176">ADAM</span></span>



| <span data-ttu-id="7de3a-177">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-177">Entry</span></span> | <span data-ttu-id="7de3a-178">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7de3a-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de3a-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de3a-181">System-Only</span></span>            | <span data-ttu-id="7de3a-182">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-182">False</span></span>                           |
| <span data-ttu-id="7de3a-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de3a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7de3a-184">對</span><span class="sxs-lookup"><span data-stu-id="7de3a-184">True</span></span>                            |
| <span data-ttu-id="7de3a-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de3a-185">Is Indexed</span></span>             | <span data-ttu-id="7de3a-186">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-186">False</span></span>                           |
| <span data-ttu-id="7de3a-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de3a-187">In Global Catalog</span></span>      | <span data-ttu-id="7de3a-188">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-188">False</span></span>                           |
| <span data-ttu-id="7de3a-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de3a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de3a-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de3a-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7de3a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de3a-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7de3a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de3a-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7de3a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-193">Search-Flags</span></span>           | <span data-ttu-id="7de3a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de3a-194">0x00000000</span></span>                      |
| <span data-ttu-id="7de3a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-195">System-Flags</span></span>           | <span data-ttu-id="7de3a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de3a-196">0x00000010</span></span>                      |
| <span data-ttu-id="7de3a-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de3a-197">Classes used in</span></span>        | [<span data-ttu-id="7de3a-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7de3a-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7de3a-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7de3a-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7de3a-200">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-200">Entry</span></span> | <span data-ttu-id="7de3a-201">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7de3a-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de3a-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de3a-204">System-Only</span></span>            | <span data-ttu-id="7de3a-205">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-205">False</span></span>                           |
| <span data-ttu-id="7de3a-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de3a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7de3a-207">對</span><span class="sxs-lookup"><span data-stu-id="7de3a-207">True</span></span>                            |
| <span data-ttu-id="7de3a-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de3a-208">Is Indexed</span></span>             | <span data-ttu-id="7de3a-209">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-209">False</span></span>                           |
| <span data-ttu-id="7de3a-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de3a-210">In Global Catalog</span></span>      | <span data-ttu-id="7de3a-211">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-211">False</span></span>                           |
| <span data-ttu-id="7de3a-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de3a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de3a-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de3a-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7de3a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de3a-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7de3a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de3a-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7de3a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-216">Search-Flags</span></span>           | <span data-ttu-id="7de3a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de3a-217">0x00000000</span></span>                      |
| <span data-ttu-id="7de3a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-218">System-Flags</span></span>           | <span data-ttu-id="7de3a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de3a-219">0x00000010</span></span>                      |
| <span data-ttu-id="7de3a-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de3a-220">Classes used in</span></span>        | [<span data-ttu-id="7de3a-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7de3a-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7de3a-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7de3a-222">Windows Server 2008</span></span>



| <span data-ttu-id="7de3a-223">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-223">Entry</span></span> | <span data-ttu-id="7de3a-224">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7de3a-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de3a-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de3a-227">System-Only</span></span>            | <span data-ttu-id="7de3a-228">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-228">False</span></span>                           |
| <span data-ttu-id="7de3a-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de3a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7de3a-230">對</span><span class="sxs-lookup"><span data-stu-id="7de3a-230">True</span></span>                            |
| <span data-ttu-id="7de3a-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de3a-231">Is Indexed</span></span>             | <span data-ttu-id="7de3a-232">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-232">False</span></span>                           |
| <span data-ttu-id="7de3a-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de3a-233">In Global Catalog</span></span>      | <span data-ttu-id="7de3a-234">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-234">False</span></span>                           |
| <span data-ttu-id="7de3a-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de3a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de3a-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de3a-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7de3a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de3a-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7de3a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de3a-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7de3a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-239">Search-Flags</span></span>           | <span data-ttu-id="7de3a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de3a-240">0x00000000</span></span>                      |
| <span data-ttu-id="7de3a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-241">System-Flags</span></span>           | <span data-ttu-id="7de3a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de3a-242">0x00000010</span></span>                      |
| <span data-ttu-id="7de3a-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de3a-243">Classes used in</span></span>        | [<span data-ttu-id="7de3a-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7de3a-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7de3a-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7de3a-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7de3a-246">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-246">Entry</span></span> | <span data-ttu-id="7de3a-247">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7de3a-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de3a-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de3a-250">System-Only</span></span>            | <span data-ttu-id="7de3a-251">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-251">False</span></span>                           |
| <span data-ttu-id="7de3a-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de3a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7de3a-253">對</span><span class="sxs-lookup"><span data-stu-id="7de3a-253">True</span></span>                            |
| <span data-ttu-id="7de3a-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de3a-254">Is Indexed</span></span>             | <span data-ttu-id="7de3a-255">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-255">False</span></span>                           |
| <span data-ttu-id="7de3a-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de3a-256">In Global Catalog</span></span>      | <span data-ttu-id="7de3a-257">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-257">False</span></span>                           |
| <span data-ttu-id="7de3a-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de3a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de3a-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de3a-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7de3a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de3a-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7de3a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de3a-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7de3a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-262">Search-Flags</span></span>           | <span data-ttu-id="7de3a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de3a-263">0x00000000</span></span>                      |
| <span data-ttu-id="7de3a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-264">System-Flags</span></span>           | <span data-ttu-id="7de3a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de3a-265">0x00000010</span></span>                      |
| <span data-ttu-id="7de3a-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de3a-266">Classes used in</span></span>        | [<span data-ttu-id="7de3a-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7de3a-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7de3a-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7de3a-268">Windows Server 2012</span></span>



| <span data-ttu-id="7de3a-269">進入</span><span class="sxs-lookup"><span data-stu-id="7de3a-269">Entry</span></span> | <span data-ttu-id="7de3a-270">值</span><span class="sxs-lookup"><span data-stu-id="7de3a-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7de3a-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7de3a-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7de3a-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7de3a-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="7de3a-273">System-Only</span></span>            | <span data-ttu-id="7de3a-274">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-274">False</span></span>                           |
| <span data-ttu-id="7de3a-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7de3a-275">Is-Single-Valued</span></span>       | <span data-ttu-id="7de3a-276">對</span><span class="sxs-lookup"><span data-stu-id="7de3a-276">True</span></span>                            |
| <span data-ttu-id="7de3a-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7de3a-277">Is Indexed</span></span>             | <span data-ttu-id="7de3a-278">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-278">False</span></span>                           |
| <span data-ttu-id="7de3a-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7de3a-279">In Global Catalog</span></span>      | <span data-ttu-id="7de3a-280">否</span><span class="sxs-lookup"><span data-stu-id="7de3a-280">False</span></span>                           |
| <span data-ttu-id="7de3a-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7de3a-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="7de3a-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7de3a-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7de3a-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7de3a-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7de3a-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7de3a-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7de3a-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-285">Search-Flags</span></span>           | <span data-ttu-id="7de3a-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7de3a-286">0x00000000</span></span>                      |
| <span data-ttu-id="7de3a-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7de3a-287">System-Flags</span></span>           | <span data-ttu-id="7de3a-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7de3a-288">0x00000010</span></span>                      |
| <span data-ttu-id="7de3a-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7de3a-289">Classes used in</span></span>        | [<span data-ttu-id="7de3a-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="7de3a-290">**Top**</span></span>](c-top.md)<br/> |



 

 





