---
title: MS-CHAP 類型屬性
description: 此 SQL server 使用的複寫類型。
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- MS-SQL 類型屬性 AD 架構
- mS-SQL 類型屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845544"
---
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="27d45-105">MS-CHAP 類型屬性</span><span class="sxs-lookup"><span data-stu-id="27d45-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="27d45-106">此 SQL server 使用的複寫類型。</span><span class="sxs-lookup"><span data-stu-id="27d45-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="27d45-107">下列值是這個屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="27d45-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="27d45-108">值</span><span class="sxs-lookup"><span data-stu-id="27d45-108">Value</span></span>        | <span data-ttu-id="27d45-109">描述</span><span class="sxs-lookup"><span data-stu-id="27d45-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="27d45-110">0</span><span class="sxs-lookup"><span data-stu-id="27d45-110">0</span></span><br/> | <span data-ttu-id="27d45-111">異動複寫。</span><span class="sxs-lookup"><span data-stu-id="27d45-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="27d45-112">1</span><span class="sxs-lookup"><span data-stu-id="27d45-112">1</span></span><br/> | <span data-ttu-id="27d45-113">快照式複寫。</span><span class="sxs-lookup"><span data-stu-id="27d45-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="27d45-114">2</span><span class="sxs-lookup"><span data-stu-id="27d45-114">2</span></span><br/> | <span data-ttu-id="27d45-115">合併式複寫。</span><span class="sxs-lookup"><span data-stu-id="27d45-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="27d45-116">進入</span><span class="sxs-lookup"><span data-stu-id="27d45-116">Entry</span></span> | <span data-ttu-id="27d45-117">值</span><span class="sxs-lookup"><span data-stu-id="27d45-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="27d45-118">CN</span><span class="sxs-lookup"><span data-stu-id="27d45-118">CN</span></span>                | <span data-ttu-id="27d45-119">MS-CHAP 類型</span><span class="sxs-lookup"><span data-stu-id="27d45-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="27d45-120">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="27d45-120">Ldap-Display-Name</span></span> | <span data-ttu-id="27d45-121">Ms-chap 類型</span><span class="sxs-lookup"><span data-stu-id="27d45-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="27d45-122">大小</span><span class="sxs-lookup"><span data-stu-id="27d45-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="27d45-123">更新許可權</span><span class="sxs-lookup"><span data-stu-id="27d45-123">Update Privilege</span></span>  | <span data-ttu-id="27d45-124">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="27d45-124">Domain administrator</span></span>                        |
| <span data-ttu-id="27d45-125">更新頻率</span><span class="sxs-lookup"><span data-stu-id="27d45-125">Update Frequency</span></span>  | <span data-ttu-id="27d45-126">當複寫設定完成時。</span><span class="sxs-lookup"><span data-stu-id="27d45-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="27d45-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27d45-127">Attribute-Id</span></span>      | <span data-ttu-id="27d45-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="27d45-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="27d45-129">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="27d45-129">System-Id-Guid</span></span>    | <span data-ttu-id="27d45-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="27d45-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="27d45-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="27d45-131">Syntax</span></span>            | [<span data-ttu-id="27d45-132">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="27d45-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="27d45-133">實作</span><span class="sxs-lookup"><span data-stu-id="27d45-133">Implementations</span></span>

-   [<span data-ttu-id="27d45-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27d45-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27d45-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27d45-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27d45-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27d45-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27d45-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27d45-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27d45-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27d45-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27d45-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27d45-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27d45-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27d45-140">Windows 2000 Server</span></span>



| <span data-ttu-id="27d45-141">進入</span><span class="sxs-lookup"><span data-stu-id="27d45-141">Entry</span></span> | <span data-ttu-id="27d45-142">值</span><span class="sxs-lookup"><span data-stu-id="27d45-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d45-143">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27d45-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d45-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d45-145">System-Only</span></span>            | <span data-ttu-id="27d45-146">否</span><span class="sxs-lookup"><span data-stu-id="27d45-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-147">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27d45-147">Is-Single-Valued</span></span>       | <span data-ttu-id="27d45-148">對</span><span class="sxs-lookup"><span data-stu-id="27d45-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="27d45-149">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27d45-149">Is Indexed</span></span>             | <span data-ttu-id="27d45-150">否</span><span class="sxs-lookup"><span data-stu-id="27d45-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-151">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27d45-151">In Global Catalog</span></span>      | <span data-ttu-id="27d45-152">否</span><span class="sxs-lookup"><span data-stu-id="27d45-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-153">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27d45-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d45-154">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27d45-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="27d45-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d45-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d45-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-157">Search-Flags</span></span>           | <span data-ttu-id="27d45-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d45-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-159">System-Flags</span></span>           | <span data-ttu-id="27d45-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d45-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-161">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27d45-161">Classes used in</span></span>        | [<span data-ttu-id="27d45-162">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="27d45-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="27d45-163">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="27d45-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27d45-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27d45-164">Windows Server 2003</span></span>



| <span data-ttu-id="27d45-165">進入</span><span class="sxs-lookup"><span data-stu-id="27d45-165">Entry</span></span> | <span data-ttu-id="27d45-166">值</span><span class="sxs-lookup"><span data-stu-id="27d45-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d45-167">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27d45-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d45-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d45-169">System-Only</span></span>            | <span data-ttu-id="27d45-170">否</span><span class="sxs-lookup"><span data-stu-id="27d45-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-171">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27d45-171">Is-Single-Valued</span></span>       | <span data-ttu-id="27d45-172">對</span><span class="sxs-lookup"><span data-stu-id="27d45-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="27d45-173">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27d45-173">Is Indexed</span></span>             | <span data-ttu-id="27d45-174">否</span><span class="sxs-lookup"><span data-stu-id="27d45-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-175">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27d45-175">In Global Catalog</span></span>      | <span data-ttu-id="27d45-176">否</span><span class="sxs-lookup"><span data-stu-id="27d45-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-177">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27d45-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d45-178">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27d45-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="27d45-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d45-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d45-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-181">Search-Flags</span></span>           | <span data-ttu-id="27d45-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d45-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-183">System-Flags</span></span>           | <span data-ttu-id="27d45-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d45-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-185">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27d45-185">Classes used in</span></span>        | [<span data-ttu-id="27d45-186">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="27d45-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="27d45-187">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="27d45-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27d45-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27d45-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27d45-189">進入</span><span class="sxs-lookup"><span data-stu-id="27d45-189">Entry</span></span> | <span data-ttu-id="27d45-190">值</span><span class="sxs-lookup"><span data-stu-id="27d45-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d45-191">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27d45-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d45-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d45-193">System-Only</span></span>            | <span data-ttu-id="27d45-194">否</span><span class="sxs-lookup"><span data-stu-id="27d45-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27d45-195">Is-Single-Valued</span></span>       | <span data-ttu-id="27d45-196">對</span><span class="sxs-lookup"><span data-stu-id="27d45-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="27d45-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27d45-197">Is Indexed</span></span>             | <span data-ttu-id="27d45-198">否</span><span class="sxs-lookup"><span data-stu-id="27d45-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27d45-199">In Global Catalog</span></span>      | <span data-ttu-id="27d45-200">否</span><span class="sxs-lookup"><span data-stu-id="27d45-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27d45-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d45-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27d45-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="27d45-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d45-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d45-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-205">Search-Flags</span></span>           | <span data-ttu-id="27d45-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d45-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-207">System-Flags</span></span>           | <span data-ttu-id="27d45-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d45-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27d45-209">Classes used in</span></span>        | [<span data-ttu-id="27d45-210">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="27d45-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="27d45-211">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="27d45-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27d45-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27d45-212">Windows Server 2008</span></span>



| <span data-ttu-id="27d45-213">進入</span><span class="sxs-lookup"><span data-stu-id="27d45-213">Entry</span></span> | <span data-ttu-id="27d45-214">值</span><span class="sxs-lookup"><span data-stu-id="27d45-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d45-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27d45-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d45-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d45-217">System-Only</span></span>            | <span data-ttu-id="27d45-218">否</span><span class="sxs-lookup"><span data-stu-id="27d45-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27d45-219">Is-Single-Valued</span></span>       | <span data-ttu-id="27d45-220">對</span><span class="sxs-lookup"><span data-stu-id="27d45-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="27d45-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27d45-221">Is Indexed</span></span>             | <span data-ttu-id="27d45-222">否</span><span class="sxs-lookup"><span data-stu-id="27d45-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27d45-223">In Global Catalog</span></span>      | <span data-ttu-id="27d45-224">否</span><span class="sxs-lookup"><span data-stu-id="27d45-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27d45-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d45-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27d45-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="27d45-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d45-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d45-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-229">Search-Flags</span></span>           | <span data-ttu-id="27d45-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d45-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-231">System-Flags</span></span>           | <span data-ttu-id="27d45-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d45-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27d45-233">Classes used in</span></span>        | [<span data-ttu-id="27d45-234">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="27d45-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="27d45-235">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="27d45-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27d45-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27d45-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27d45-237">進入</span><span class="sxs-lookup"><span data-stu-id="27d45-237">Entry</span></span> | <span data-ttu-id="27d45-238">值</span><span class="sxs-lookup"><span data-stu-id="27d45-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d45-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27d45-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d45-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d45-241">System-Only</span></span>            | <span data-ttu-id="27d45-242">否</span><span class="sxs-lookup"><span data-stu-id="27d45-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27d45-243">Is-Single-Valued</span></span>       | <span data-ttu-id="27d45-244">對</span><span class="sxs-lookup"><span data-stu-id="27d45-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="27d45-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27d45-245">Is Indexed</span></span>             | <span data-ttu-id="27d45-246">否</span><span class="sxs-lookup"><span data-stu-id="27d45-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27d45-247">In Global Catalog</span></span>      | <span data-ttu-id="27d45-248">否</span><span class="sxs-lookup"><span data-stu-id="27d45-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27d45-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d45-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27d45-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="27d45-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d45-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d45-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-253">Search-Flags</span></span>           | <span data-ttu-id="27d45-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d45-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-255">System-Flags</span></span>           | <span data-ttu-id="27d45-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d45-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-257">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27d45-257">Classes used in</span></span>        | [<span data-ttu-id="27d45-258">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="27d45-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="27d45-259">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="27d45-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27d45-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27d45-260">Windows Server 2012</span></span>



| <span data-ttu-id="27d45-261">進入</span><span class="sxs-lookup"><span data-stu-id="27d45-261">Entry</span></span> | <span data-ttu-id="27d45-262">值</span><span class="sxs-lookup"><span data-stu-id="27d45-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d45-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27d45-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27d45-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="27d45-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="27d45-265">System-Only</span></span>            | <span data-ttu-id="27d45-266">否</span><span class="sxs-lookup"><span data-stu-id="27d45-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27d45-267">Is-Single-Valued</span></span>       | <span data-ttu-id="27d45-268">對</span><span class="sxs-lookup"><span data-stu-id="27d45-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="27d45-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27d45-269">Is Indexed</span></span>             | <span data-ttu-id="27d45-270">否</span><span class="sxs-lookup"><span data-stu-id="27d45-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27d45-271">In Global Catalog</span></span>      | <span data-ttu-id="27d45-272">否</span><span class="sxs-lookup"><span data-stu-id="27d45-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="27d45-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27d45-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="27d45-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27d45-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="27d45-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27d45-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27d45-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="27d45-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-277">Search-Flags</span></span>           | <span data-ttu-id="27d45-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27d45-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27d45-279">System-Flags</span></span>           | <span data-ttu-id="27d45-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27d45-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="27d45-281">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27d45-281">Classes used in</span></span>        | [<span data-ttu-id="27d45-282">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="27d45-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="27d45-283">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="27d45-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





