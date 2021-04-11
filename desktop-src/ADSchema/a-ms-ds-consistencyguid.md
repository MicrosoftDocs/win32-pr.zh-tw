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
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="93f33-105">MS DS-一致性-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="93f33-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="93f33-106">這個屬性是用來藉由比較 Guid 來檢查目錄與另一個物件、資料庫或應用程式之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="93f33-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="93f33-107">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-107">Entry</span></span> | <span data-ttu-id="93f33-108">值</span><span class="sxs-lookup"><span data-stu-id="93f33-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="93f33-109">CN</span><span class="sxs-lookup"><span data-stu-id="93f33-109">CN</span></span>                | <span data-ttu-id="93f33-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="93f33-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="93f33-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="93f33-111">Ldap-Display-Name</span></span> | <span data-ttu-id="93f33-112">ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="93f33-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="93f33-113">大小</span><span class="sxs-lookup"><span data-stu-id="93f33-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="93f33-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="93f33-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="93f33-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="93f33-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="93f33-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-116">Attribute-Id</span></span>      | <span data-ttu-id="93f33-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="93f33-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="93f33-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="93f33-118">System-Id-Guid</span></span>    | <span data-ttu-id="93f33-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="93f33-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="93f33-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="93f33-120">Syntax</span></span>            | [<span data-ttu-id="93f33-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="93f33-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="93f33-122">實作</span><span class="sxs-lookup"><span data-stu-id="93f33-122">Implementations</span></span>

-   [<span data-ttu-id="93f33-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="93f33-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="93f33-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="93f33-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="93f33-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="93f33-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="93f33-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="93f33-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="93f33-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="93f33-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="93f33-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="93f33-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="93f33-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="93f33-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="93f33-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93f33-130">Windows 2000 Server</span></span>



| <span data-ttu-id="93f33-131">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-131">Entry</span></span> | <span data-ttu-id="93f33-132">值</span><span class="sxs-lookup"><span data-stu-id="93f33-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="93f33-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="93f33-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f33-135">System-Only</span></span>            | <span data-ttu-id="93f33-136">否</span><span class="sxs-lookup"><span data-stu-id="93f33-136">False</span></span>                           |
| <span data-ttu-id="93f33-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="93f33-137">Is-Single-Valued</span></span>       | <span data-ttu-id="93f33-138">對</span><span class="sxs-lookup"><span data-stu-id="93f33-138">True</span></span>                            |
| <span data-ttu-id="93f33-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="93f33-139">Is Indexed</span></span>             | <span data-ttu-id="93f33-140">否</span><span class="sxs-lookup"><span data-stu-id="93f33-140">False</span></span>                           |
| <span data-ttu-id="93f33-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="93f33-141">In Global Catalog</span></span>      | <span data-ttu-id="93f33-142">否</span><span class="sxs-lookup"><span data-stu-id="93f33-142">False</span></span>                           |
| <span data-ttu-id="93f33-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="93f33-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f33-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="93f33-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="93f33-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f33-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="93f33-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f33-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="93f33-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-147">Search-Flags</span></span>           | <span data-ttu-id="93f33-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f33-148">0x00000000</span></span>                      |
| <span data-ttu-id="93f33-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-149">System-Flags</span></span>           | <span data-ttu-id="93f33-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f33-150">0x00000010</span></span>                      |
| <span data-ttu-id="93f33-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="93f33-151">Classes used in</span></span>        | [<span data-ttu-id="93f33-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="93f33-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="93f33-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93f33-153">Windows Server 2003</span></span>



| <span data-ttu-id="93f33-154">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-154">Entry</span></span> | <span data-ttu-id="93f33-155">值</span><span class="sxs-lookup"><span data-stu-id="93f33-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="93f33-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="93f33-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f33-158">System-Only</span></span>            | <span data-ttu-id="93f33-159">否</span><span class="sxs-lookup"><span data-stu-id="93f33-159">False</span></span>                           |
| <span data-ttu-id="93f33-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="93f33-160">Is-Single-Valued</span></span>       | <span data-ttu-id="93f33-161">對</span><span class="sxs-lookup"><span data-stu-id="93f33-161">True</span></span>                            |
| <span data-ttu-id="93f33-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="93f33-162">Is Indexed</span></span>             | <span data-ttu-id="93f33-163">否</span><span class="sxs-lookup"><span data-stu-id="93f33-163">False</span></span>                           |
| <span data-ttu-id="93f33-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="93f33-164">In Global Catalog</span></span>      | <span data-ttu-id="93f33-165">否</span><span class="sxs-lookup"><span data-stu-id="93f33-165">False</span></span>                           |
| <span data-ttu-id="93f33-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="93f33-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f33-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="93f33-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="93f33-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f33-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="93f33-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f33-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="93f33-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-170">Search-Flags</span></span>           | <span data-ttu-id="93f33-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f33-171">0x00000000</span></span>                      |
| <span data-ttu-id="93f33-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-172">System-Flags</span></span>           | <span data-ttu-id="93f33-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f33-173">0x00000010</span></span>                      |
| <span data-ttu-id="93f33-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="93f33-174">Classes used in</span></span>        | [<span data-ttu-id="93f33-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="93f33-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="93f33-176">亞當</span><span class="sxs-lookup"><span data-stu-id="93f33-176">ADAM</span></span>



| <span data-ttu-id="93f33-177">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-177">Entry</span></span> | <span data-ttu-id="93f33-178">值</span><span class="sxs-lookup"><span data-stu-id="93f33-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="93f33-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="93f33-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f33-181">System-Only</span></span>            | <span data-ttu-id="93f33-182">否</span><span class="sxs-lookup"><span data-stu-id="93f33-182">False</span></span>                           |
| <span data-ttu-id="93f33-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="93f33-183">Is-Single-Valued</span></span>       | <span data-ttu-id="93f33-184">對</span><span class="sxs-lookup"><span data-stu-id="93f33-184">True</span></span>                            |
| <span data-ttu-id="93f33-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="93f33-185">Is Indexed</span></span>             | <span data-ttu-id="93f33-186">否</span><span class="sxs-lookup"><span data-stu-id="93f33-186">False</span></span>                           |
| <span data-ttu-id="93f33-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="93f33-187">In Global Catalog</span></span>      | <span data-ttu-id="93f33-188">否</span><span class="sxs-lookup"><span data-stu-id="93f33-188">False</span></span>                           |
| <span data-ttu-id="93f33-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="93f33-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f33-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="93f33-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="93f33-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f33-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="93f33-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f33-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="93f33-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-193">Search-Flags</span></span>           | <span data-ttu-id="93f33-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f33-194">0x00000000</span></span>                      |
| <span data-ttu-id="93f33-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-195">System-Flags</span></span>           | <span data-ttu-id="93f33-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f33-196">0x00000010</span></span>                      |
| <span data-ttu-id="93f33-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="93f33-197">Classes used in</span></span>        | [<span data-ttu-id="93f33-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="93f33-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="93f33-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="93f33-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="93f33-200">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-200">Entry</span></span> | <span data-ttu-id="93f33-201">值</span><span class="sxs-lookup"><span data-stu-id="93f33-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="93f33-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="93f33-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f33-204">System-Only</span></span>            | <span data-ttu-id="93f33-205">否</span><span class="sxs-lookup"><span data-stu-id="93f33-205">False</span></span>                           |
| <span data-ttu-id="93f33-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="93f33-206">Is-Single-Valued</span></span>       | <span data-ttu-id="93f33-207">對</span><span class="sxs-lookup"><span data-stu-id="93f33-207">True</span></span>                            |
| <span data-ttu-id="93f33-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="93f33-208">Is Indexed</span></span>             | <span data-ttu-id="93f33-209">否</span><span class="sxs-lookup"><span data-stu-id="93f33-209">False</span></span>                           |
| <span data-ttu-id="93f33-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="93f33-210">In Global Catalog</span></span>      | <span data-ttu-id="93f33-211">否</span><span class="sxs-lookup"><span data-stu-id="93f33-211">False</span></span>                           |
| <span data-ttu-id="93f33-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="93f33-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f33-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="93f33-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="93f33-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f33-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="93f33-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f33-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="93f33-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-216">Search-Flags</span></span>           | <span data-ttu-id="93f33-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f33-217">0x00000000</span></span>                      |
| <span data-ttu-id="93f33-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-218">System-Flags</span></span>           | <span data-ttu-id="93f33-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f33-219">0x00000010</span></span>                      |
| <span data-ttu-id="93f33-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="93f33-220">Classes used in</span></span>        | [<span data-ttu-id="93f33-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="93f33-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="93f33-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93f33-222">Windows Server 2008</span></span>



| <span data-ttu-id="93f33-223">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-223">Entry</span></span> | <span data-ttu-id="93f33-224">值</span><span class="sxs-lookup"><span data-stu-id="93f33-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="93f33-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="93f33-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f33-227">System-Only</span></span>            | <span data-ttu-id="93f33-228">否</span><span class="sxs-lookup"><span data-stu-id="93f33-228">False</span></span>                           |
| <span data-ttu-id="93f33-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="93f33-229">Is-Single-Valued</span></span>       | <span data-ttu-id="93f33-230">對</span><span class="sxs-lookup"><span data-stu-id="93f33-230">True</span></span>                            |
| <span data-ttu-id="93f33-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="93f33-231">Is Indexed</span></span>             | <span data-ttu-id="93f33-232">否</span><span class="sxs-lookup"><span data-stu-id="93f33-232">False</span></span>                           |
| <span data-ttu-id="93f33-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="93f33-233">In Global Catalog</span></span>      | <span data-ttu-id="93f33-234">否</span><span class="sxs-lookup"><span data-stu-id="93f33-234">False</span></span>                           |
| <span data-ttu-id="93f33-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="93f33-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f33-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="93f33-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="93f33-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f33-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="93f33-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f33-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="93f33-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-239">Search-Flags</span></span>           | <span data-ttu-id="93f33-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f33-240">0x00000000</span></span>                      |
| <span data-ttu-id="93f33-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-241">System-Flags</span></span>           | <span data-ttu-id="93f33-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f33-242">0x00000010</span></span>                      |
| <span data-ttu-id="93f33-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="93f33-243">Classes used in</span></span>        | [<span data-ttu-id="93f33-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="93f33-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="93f33-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93f33-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="93f33-246">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-246">Entry</span></span> | <span data-ttu-id="93f33-247">值</span><span class="sxs-lookup"><span data-stu-id="93f33-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="93f33-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="93f33-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f33-250">System-Only</span></span>            | <span data-ttu-id="93f33-251">否</span><span class="sxs-lookup"><span data-stu-id="93f33-251">False</span></span>                           |
| <span data-ttu-id="93f33-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="93f33-252">Is-Single-Valued</span></span>       | <span data-ttu-id="93f33-253">對</span><span class="sxs-lookup"><span data-stu-id="93f33-253">True</span></span>                            |
| <span data-ttu-id="93f33-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="93f33-254">Is Indexed</span></span>             | <span data-ttu-id="93f33-255">否</span><span class="sxs-lookup"><span data-stu-id="93f33-255">False</span></span>                           |
| <span data-ttu-id="93f33-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="93f33-256">In Global Catalog</span></span>      | <span data-ttu-id="93f33-257">否</span><span class="sxs-lookup"><span data-stu-id="93f33-257">False</span></span>                           |
| <span data-ttu-id="93f33-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="93f33-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f33-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="93f33-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="93f33-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f33-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="93f33-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f33-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="93f33-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-262">Search-Flags</span></span>           | <span data-ttu-id="93f33-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f33-263">0x00000000</span></span>                      |
| <span data-ttu-id="93f33-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-264">System-Flags</span></span>           | <span data-ttu-id="93f33-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f33-265">0x00000010</span></span>                      |
| <span data-ttu-id="93f33-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="93f33-266">Classes used in</span></span>        | [<span data-ttu-id="93f33-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="93f33-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="93f33-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93f33-268">Windows Server 2012</span></span>



| <span data-ttu-id="93f33-269">進入</span><span class="sxs-lookup"><span data-stu-id="93f33-269">Entry</span></span> | <span data-ttu-id="93f33-270">值</span><span class="sxs-lookup"><span data-stu-id="93f33-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="93f33-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="93f33-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f33-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="93f33-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f33-273">System-Only</span></span>            | <span data-ttu-id="93f33-274">否</span><span class="sxs-lookup"><span data-stu-id="93f33-274">False</span></span>                           |
| <span data-ttu-id="93f33-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="93f33-275">Is-Single-Valued</span></span>       | <span data-ttu-id="93f33-276">對</span><span class="sxs-lookup"><span data-stu-id="93f33-276">True</span></span>                            |
| <span data-ttu-id="93f33-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="93f33-277">Is Indexed</span></span>             | <span data-ttu-id="93f33-278">否</span><span class="sxs-lookup"><span data-stu-id="93f33-278">False</span></span>                           |
| <span data-ttu-id="93f33-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="93f33-279">In Global Catalog</span></span>      | <span data-ttu-id="93f33-280">否</span><span class="sxs-lookup"><span data-stu-id="93f33-280">False</span></span>                           |
| <span data-ttu-id="93f33-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="93f33-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f33-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="93f33-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="93f33-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f33-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="93f33-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f33-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="93f33-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-285">Search-Flags</span></span>           | <span data-ttu-id="93f33-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f33-286">0x00000000</span></span>                      |
| <span data-ttu-id="93f33-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f33-287">System-Flags</span></span>           | <span data-ttu-id="93f33-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f33-288">0x00000010</span></span>                      |
| <span data-ttu-id="93f33-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="93f33-289">Classes used in</span></span>        | [<span data-ttu-id="93f33-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="93f33-290">**Top**</span></span>](c-top.md)<br/> |



 

 





