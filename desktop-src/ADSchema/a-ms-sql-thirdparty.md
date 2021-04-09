---
title: ThirdParty 屬性
description: 這個屬性會指出發行集資料是否來自 SQL Server 以外的資料來源。 如果是來自另一個來源，則會設定為 TRUE。
ms.assetid: 84d93b9f-0acc-47da-9f1b-44d8468ad53e
ms.tgt_platform: multiple
keywords:
- ThirdParty 屬性 AD 架構
- ThirdParty 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-ThirdParty
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc2b60f9589990f6357ee3c4cd24215e8af21df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686827"
---
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="37068-106">ThirdParty 屬性</span><span class="sxs-lookup"><span data-stu-id="37068-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="37068-107">這個屬性會指出發行集資料是否來自 SQL Server 以外的資料來源。</span><span class="sxs-lookup"><span data-stu-id="37068-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="37068-108">如果是來自另一個來源，則會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="37068-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="37068-109">進入</span><span class="sxs-lookup"><span data-stu-id="37068-109">Entry</span></span> | <span data-ttu-id="37068-110">值</span><span class="sxs-lookup"><span data-stu-id="37068-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="37068-111">CN</span><span class="sxs-lookup"><span data-stu-id="37068-111">CN</span></span>                | <span data-ttu-id="37068-112">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="37068-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="37068-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="37068-113">Ldap-Display-Name</span></span> | <span data-ttu-id="37068-114">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="37068-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="37068-115">大小</span><span class="sxs-lookup"><span data-stu-id="37068-115">Size</span></span>              | <span data-ttu-id="37068-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="37068-116">4 bytes</span></span>                              |
| <span data-ttu-id="37068-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="37068-117">Update Privilege</span></span>  | <span data-ttu-id="37068-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="37068-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="37068-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="37068-119">Update Frequency</span></span>  | <span data-ttu-id="37068-120">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="37068-120">When replication is setup.</span></span>           |
| <span data-ttu-id="37068-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37068-121">Attribute-Id</span></span>      | <span data-ttu-id="37068-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="37068-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="37068-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="37068-123">System-Id-Guid</span></span>    | <span data-ttu-id="37068-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="37068-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="37068-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="37068-125">Syntax</span></span>            | [<span data-ttu-id="37068-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="37068-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="37068-127">實作</span><span class="sxs-lookup"><span data-stu-id="37068-127">Implementations</span></span>

-   [<span data-ttu-id="37068-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="37068-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="37068-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37068-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37068-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37068-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37068-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37068-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37068-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37068-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37068-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37068-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="37068-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37068-134">Windows 2000 Server</span></span>



| <span data-ttu-id="37068-135">進入</span><span class="sxs-lookup"><span data-stu-id="37068-135">Entry</span></span> | <span data-ttu-id="37068-136">值</span><span class="sxs-lookup"><span data-stu-id="37068-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="37068-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37068-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37068-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="37068-139">System-Only</span></span>            | <span data-ttu-id="37068-140">否</span><span class="sxs-lookup"><span data-stu-id="37068-140">False</span></span>                                                               |
| <span data-ttu-id="37068-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37068-141">Is-Single-Valued</span></span>       | <span data-ttu-id="37068-142">對</span><span class="sxs-lookup"><span data-stu-id="37068-142">True</span></span>                                                                |
| <span data-ttu-id="37068-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37068-143">Is Indexed</span></span>             | <span data-ttu-id="37068-144">否</span><span class="sxs-lookup"><span data-stu-id="37068-144">False</span></span>                                                               |
| <span data-ttu-id="37068-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37068-145">In Global Catalog</span></span>      | <span data-ttu-id="37068-146">否</span><span class="sxs-lookup"><span data-stu-id="37068-146">False</span></span>                                                               |
| <span data-ttu-id="37068-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37068-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="37068-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37068-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="37068-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37068-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37068-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-151">Search-Flags</span></span>           | <span data-ttu-id="37068-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37068-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="37068-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-153">System-Flags</span></span>           | <span data-ttu-id="37068-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37068-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="37068-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37068-155">Classes used in</span></span>        | [<span data-ttu-id="37068-156">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37068-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="37068-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37068-157">Windows Server 2003</span></span>



| <span data-ttu-id="37068-158">進入</span><span class="sxs-lookup"><span data-stu-id="37068-158">Entry</span></span> | <span data-ttu-id="37068-159">值</span><span class="sxs-lookup"><span data-stu-id="37068-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="37068-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37068-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37068-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="37068-162">System-Only</span></span>            | <span data-ttu-id="37068-163">否</span><span class="sxs-lookup"><span data-stu-id="37068-163">False</span></span>                                                               |
| <span data-ttu-id="37068-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37068-164">Is-Single-Valued</span></span>       | <span data-ttu-id="37068-165">對</span><span class="sxs-lookup"><span data-stu-id="37068-165">True</span></span>                                                                |
| <span data-ttu-id="37068-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37068-166">Is Indexed</span></span>             | <span data-ttu-id="37068-167">否</span><span class="sxs-lookup"><span data-stu-id="37068-167">False</span></span>                                                               |
| <span data-ttu-id="37068-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37068-168">In Global Catalog</span></span>      | <span data-ttu-id="37068-169">否</span><span class="sxs-lookup"><span data-stu-id="37068-169">False</span></span>                                                               |
| <span data-ttu-id="37068-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37068-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="37068-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37068-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="37068-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37068-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37068-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-174">Search-Flags</span></span>           | <span data-ttu-id="37068-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37068-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="37068-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-176">System-Flags</span></span>           | <span data-ttu-id="37068-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37068-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="37068-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37068-178">Classes used in</span></span>        | [<span data-ttu-id="37068-179">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37068-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37068-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37068-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37068-181">進入</span><span class="sxs-lookup"><span data-stu-id="37068-181">Entry</span></span> | <span data-ttu-id="37068-182">值</span><span class="sxs-lookup"><span data-stu-id="37068-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="37068-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37068-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37068-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="37068-185">System-Only</span></span>            | <span data-ttu-id="37068-186">否</span><span class="sxs-lookup"><span data-stu-id="37068-186">False</span></span>                                                               |
| <span data-ttu-id="37068-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37068-187">Is-Single-Valued</span></span>       | <span data-ttu-id="37068-188">對</span><span class="sxs-lookup"><span data-stu-id="37068-188">True</span></span>                                                                |
| <span data-ttu-id="37068-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37068-189">Is Indexed</span></span>             | <span data-ttu-id="37068-190">否</span><span class="sxs-lookup"><span data-stu-id="37068-190">False</span></span>                                                               |
| <span data-ttu-id="37068-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37068-191">In Global Catalog</span></span>      | <span data-ttu-id="37068-192">否</span><span class="sxs-lookup"><span data-stu-id="37068-192">False</span></span>                                                               |
| <span data-ttu-id="37068-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37068-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="37068-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37068-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="37068-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37068-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37068-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-197">Search-Flags</span></span>           | <span data-ttu-id="37068-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37068-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="37068-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-199">System-Flags</span></span>           | <span data-ttu-id="37068-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37068-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="37068-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37068-201">Classes used in</span></span>        | [<span data-ttu-id="37068-202">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37068-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37068-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37068-203">Windows Server 2008</span></span>



| <span data-ttu-id="37068-204">進入</span><span class="sxs-lookup"><span data-stu-id="37068-204">Entry</span></span> | <span data-ttu-id="37068-205">值</span><span class="sxs-lookup"><span data-stu-id="37068-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="37068-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37068-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37068-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="37068-208">System-Only</span></span>            | <span data-ttu-id="37068-209">否</span><span class="sxs-lookup"><span data-stu-id="37068-209">False</span></span>                                                               |
| <span data-ttu-id="37068-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37068-210">Is-Single-Valued</span></span>       | <span data-ttu-id="37068-211">對</span><span class="sxs-lookup"><span data-stu-id="37068-211">True</span></span>                                                                |
| <span data-ttu-id="37068-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37068-212">Is Indexed</span></span>             | <span data-ttu-id="37068-213">否</span><span class="sxs-lookup"><span data-stu-id="37068-213">False</span></span>                                                               |
| <span data-ttu-id="37068-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37068-214">In Global Catalog</span></span>      | <span data-ttu-id="37068-215">否</span><span class="sxs-lookup"><span data-stu-id="37068-215">False</span></span>                                                               |
| <span data-ttu-id="37068-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37068-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="37068-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37068-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="37068-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37068-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37068-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-220">Search-Flags</span></span>           | <span data-ttu-id="37068-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37068-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="37068-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-222">System-Flags</span></span>           | <span data-ttu-id="37068-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37068-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="37068-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37068-224">Classes used in</span></span>        | [<span data-ttu-id="37068-225">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37068-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37068-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37068-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37068-227">進入</span><span class="sxs-lookup"><span data-stu-id="37068-227">Entry</span></span> | <span data-ttu-id="37068-228">值</span><span class="sxs-lookup"><span data-stu-id="37068-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="37068-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37068-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37068-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="37068-231">System-Only</span></span>            | <span data-ttu-id="37068-232">否</span><span class="sxs-lookup"><span data-stu-id="37068-232">False</span></span>                                                               |
| <span data-ttu-id="37068-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37068-233">Is-Single-Valued</span></span>       | <span data-ttu-id="37068-234">對</span><span class="sxs-lookup"><span data-stu-id="37068-234">True</span></span>                                                                |
| <span data-ttu-id="37068-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37068-235">Is Indexed</span></span>             | <span data-ttu-id="37068-236">否</span><span class="sxs-lookup"><span data-stu-id="37068-236">False</span></span>                                                               |
| <span data-ttu-id="37068-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37068-237">In Global Catalog</span></span>      | <span data-ttu-id="37068-238">否</span><span class="sxs-lookup"><span data-stu-id="37068-238">False</span></span>                                                               |
| <span data-ttu-id="37068-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37068-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="37068-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37068-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="37068-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37068-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37068-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-243">Search-Flags</span></span>           | <span data-ttu-id="37068-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37068-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="37068-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-245">System-Flags</span></span>           | <span data-ttu-id="37068-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37068-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="37068-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37068-247">Classes used in</span></span>        | [<span data-ttu-id="37068-248">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37068-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37068-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37068-249">Windows Server 2012</span></span>



| <span data-ttu-id="37068-250">進入</span><span class="sxs-lookup"><span data-stu-id="37068-250">Entry</span></span> | <span data-ttu-id="37068-251">值</span><span class="sxs-lookup"><span data-stu-id="37068-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="37068-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37068-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37068-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="37068-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="37068-254">System-Only</span></span>            | <span data-ttu-id="37068-255">否</span><span class="sxs-lookup"><span data-stu-id="37068-255">False</span></span>                                                               |
| <span data-ttu-id="37068-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37068-256">Is-Single-Valued</span></span>       | <span data-ttu-id="37068-257">對</span><span class="sxs-lookup"><span data-stu-id="37068-257">True</span></span>                                                                |
| <span data-ttu-id="37068-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37068-258">Is Indexed</span></span>             | <span data-ttu-id="37068-259">否</span><span class="sxs-lookup"><span data-stu-id="37068-259">False</span></span>                                                               |
| <span data-ttu-id="37068-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37068-260">In Global Catalog</span></span>      | <span data-ttu-id="37068-261">否</span><span class="sxs-lookup"><span data-stu-id="37068-261">False</span></span>                                                               |
| <span data-ttu-id="37068-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37068-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="37068-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37068-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="37068-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37068-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37068-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="37068-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-266">Search-Flags</span></span>           | <span data-ttu-id="37068-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37068-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="37068-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37068-268">System-Flags</span></span>           | <span data-ttu-id="37068-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37068-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="37068-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37068-270">Classes used in</span></span>        | [<span data-ttu-id="37068-271">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37068-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





