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
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="37bc8-105">MS-CHAP 類型屬性</span><span class="sxs-lookup"><span data-stu-id="37bc8-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="37bc8-106">此 SQL server 使用的複寫類型。</span><span class="sxs-lookup"><span data-stu-id="37bc8-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="37bc8-107">下列值是這個屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="37bc8-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="37bc8-108">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-108">Value</span></span>        | <span data-ttu-id="37bc8-109">描述</span><span class="sxs-lookup"><span data-stu-id="37bc8-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="37bc8-110">0</span><span class="sxs-lookup"><span data-stu-id="37bc8-110">0</span></span><br/> | <span data-ttu-id="37bc8-111">異動複寫。</span><span class="sxs-lookup"><span data-stu-id="37bc8-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="37bc8-112">1</span><span class="sxs-lookup"><span data-stu-id="37bc8-112">1</span></span><br/> | <span data-ttu-id="37bc8-113">快照式複寫。</span><span class="sxs-lookup"><span data-stu-id="37bc8-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="37bc8-114">2</span><span class="sxs-lookup"><span data-stu-id="37bc8-114">2</span></span><br/> | <span data-ttu-id="37bc8-115">合併式複寫。</span><span class="sxs-lookup"><span data-stu-id="37bc8-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="37bc8-116">進入</span><span class="sxs-lookup"><span data-stu-id="37bc8-116">Entry</span></span> | <span data-ttu-id="37bc8-117">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="37bc8-118">CN</span><span class="sxs-lookup"><span data-stu-id="37bc8-118">CN</span></span>                | <span data-ttu-id="37bc8-119">MS-CHAP 類型</span><span class="sxs-lookup"><span data-stu-id="37bc8-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="37bc8-120">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="37bc8-120">Ldap-Display-Name</span></span> | <span data-ttu-id="37bc8-121">Ms-chap 類型</span><span class="sxs-lookup"><span data-stu-id="37bc8-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="37bc8-122">大小</span><span class="sxs-lookup"><span data-stu-id="37bc8-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="37bc8-123">更新許可權</span><span class="sxs-lookup"><span data-stu-id="37bc8-123">Update Privilege</span></span>  | <span data-ttu-id="37bc8-124">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="37bc8-124">Domain administrator</span></span>                        |
| <span data-ttu-id="37bc8-125">更新頻率</span><span class="sxs-lookup"><span data-stu-id="37bc8-125">Update Frequency</span></span>  | <span data-ttu-id="37bc8-126">當複寫設定完成時。</span><span class="sxs-lookup"><span data-stu-id="37bc8-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="37bc8-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37bc8-127">Attribute-Id</span></span>      | <span data-ttu-id="37bc8-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="37bc8-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="37bc8-129">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="37bc8-129">System-Id-Guid</span></span>    | <span data-ttu-id="37bc8-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="37bc8-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="37bc8-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="37bc8-131">Syntax</span></span>            | [<span data-ttu-id="37bc8-132">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="37bc8-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="37bc8-133">實作</span><span class="sxs-lookup"><span data-stu-id="37bc8-133">Implementations</span></span>

-   [<span data-ttu-id="37bc8-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="37bc8-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="37bc8-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37bc8-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37bc8-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37bc8-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37bc8-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37bc8-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37bc8-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37bc8-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37bc8-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37bc8-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="37bc8-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37bc8-140">Windows 2000 Server</span></span>



| <span data-ttu-id="37bc8-141">進入</span><span class="sxs-lookup"><span data-stu-id="37bc8-141">Entry</span></span> | <span data-ttu-id="37bc8-142">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc8-143">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37bc8-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37bc8-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="37bc8-145">System-Only</span></span>            | <span data-ttu-id="37bc8-146">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-147">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37bc8-147">Is-Single-Valued</span></span>       | <span data-ttu-id="37bc8-148">對</span><span class="sxs-lookup"><span data-stu-id="37bc8-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="37bc8-149">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37bc8-149">Is Indexed</span></span>             | <span data-ttu-id="37bc8-150">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-151">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37bc8-151">In Global Catalog</span></span>      | <span data-ttu-id="37bc8-152">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-153">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37bc8-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="37bc8-154">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37bc8-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="37bc8-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37bc8-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37bc8-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-157">Search-Flags</span></span>           | <span data-ttu-id="37bc8-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37bc8-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-159">System-Flags</span></span>           | <span data-ttu-id="37bc8-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37bc8-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-161">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37bc8-161">Classes used in</span></span>        | [<span data-ttu-id="37bc8-162">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37bc8-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="37bc8-163">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="37bc8-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="37bc8-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37bc8-164">Windows Server 2003</span></span>



| <span data-ttu-id="37bc8-165">進入</span><span class="sxs-lookup"><span data-stu-id="37bc8-165">Entry</span></span> | <span data-ttu-id="37bc8-166">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc8-167">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37bc8-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37bc8-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="37bc8-169">System-Only</span></span>            | <span data-ttu-id="37bc8-170">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-171">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37bc8-171">Is-Single-Valued</span></span>       | <span data-ttu-id="37bc8-172">對</span><span class="sxs-lookup"><span data-stu-id="37bc8-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="37bc8-173">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37bc8-173">Is Indexed</span></span>             | <span data-ttu-id="37bc8-174">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-175">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37bc8-175">In Global Catalog</span></span>      | <span data-ttu-id="37bc8-176">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-177">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37bc8-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="37bc8-178">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37bc8-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="37bc8-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37bc8-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37bc8-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-181">Search-Flags</span></span>           | <span data-ttu-id="37bc8-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37bc8-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-183">System-Flags</span></span>           | <span data-ttu-id="37bc8-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37bc8-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-185">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37bc8-185">Classes used in</span></span>        | [<span data-ttu-id="37bc8-186">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37bc8-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="37bc8-187">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="37bc8-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37bc8-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37bc8-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37bc8-189">進入</span><span class="sxs-lookup"><span data-stu-id="37bc8-189">Entry</span></span> | <span data-ttu-id="37bc8-190">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc8-191">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37bc8-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37bc8-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="37bc8-193">System-Only</span></span>            | <span data-ttu-id="37bc8-194">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37bc8-195">Is-Single-Valued</span></span>       | <span data-ttu-id="37bc8-196">對</span><span class="sxs-lookup"><span data-stu-id="37bc8-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="37bc8-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37bc8-197">Is Indexed</span></span>             | <span data-ttu-id="37bc8-198">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37bc8-199">In Global Catalog</span></span>      | <span data-ttu-id="37bc8-200">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37bc8-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="37bc8-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37bc8-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="37bc8-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37bc8-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37bc8-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-205">Search-Flags</span></span>           | <span data-ttu-id="37bc8-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37bc8-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-207">System-Flags</span></span>           | <span data-ttu-id="37bc8-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37bc8-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37bc8-209">Classes used in</span></span>        | [<span data-ttu-id="37bc8-210">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37bc8-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="37bc8-211">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="37bc8-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37bc8-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37bc8-212">Windows Server 2008</span></span>



| <span data-ttu-id="37bc8-213">進入</span><span class="sxs-lookup"><span data-stu-id="37bc8-213">Entry</span></span> | <span data-ttu-id="37bc8-214">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc8-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37bc8-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37bc8-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="37bc8-217">System-Only</span></span>            | <span data-ttu-id="37bc8-218">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37bc8-219">Is-Single-Valued</span></span>       | <span data-ttu-id="37bc8-220">對</span><span class="sxs-lookup"><span data-stu-id="37bc8-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="37bc8-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37bc8-221">Is Indexed</span></span>             | <span data-ttu-id="37bc8-222">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37bc8-223">In Global Catalog</span></span>      | <span data-ttu-id="37bc8-224">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37bc8-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="37bc8-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37bc8-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="37bc8-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37bc8-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37bc8-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-229">Search-Flags</span></span>           | <span data-ttu-id="37bc8-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37bc8-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-231">System-Flags</span></span>           | <span data-ttu-id="37bc8-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37bc8-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37bc8-233">Classes used in</span></span>        | [<span data-ttu-id="37bc8-234">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37bc8-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="37bc8-235">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="37bc8-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37bc8-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37bc8-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37bc8-237">進入</span><span class="sxs-lookup"><span data-stu-id="37bc8-237">Entry</span></span> | <span data-ttu-id="37bc8-238">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc8-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37bc8-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37bc8-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="37bc8-241">System-Only</span></span>            | <span data-ttu-id="37bc8-242">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37bc8-243">Is-Single-Valued</span></span>       | <span data-ttu-id="37bc8-244">對</span><span class="sxs-lookup"><span data-stu-id="37bc8-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="37bc8-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37bc8-245">Is Indexed</span></span>             | <span data-ttu-id="37bc8-246">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37bc8-247">In Global Catalog</span></span>      | <span data-ttu-id="37bc8-248">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37bc8-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="37bc8-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37bc8-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="37bc8-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37bc8-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37bc8-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-253">Search-Flags</span></span>           | <span data-ttu-id="37bc8-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37bc8-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-255">System-Flags</span></span>           | <span data-ttu-id="37bc8-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37bc8-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-257">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37bc8-257">Classes used in</span></span>        | [<span data-ttu-id="37bc8-258">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37bc8-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="37bc8-259">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="37bc8-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37bc8-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37bc8-260">Windows Server 2012</span></span>



| <span data-ttu-id="37bc8-261">進入</span><span class="sxs-lookup"><span data-stu-id="37bc8-261">Entry</span></span> | <span data-ttu-id="37bc8-262">值</span><span class="sxs-lookup"><span data-stu-id="37bc8-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc8-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37bc8-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37bc8-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="37bc8-265">System-Only</span></span>            | <span data-ttu-id="37bc8-266">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37bc8-267">Is-Single-Valued</span></span>       | <span data-ttu-id="37bc8-268">對</span><span class="sxs-lookup"><span data-stu-id="37bc8-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="37bc8-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37bc8-269">Is Indexed</span></span>             | <span data-ttu-id="37bc8-270">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37bc8-271">In Global Catalog</span></span>      | <span data-ttu-id="37bc8-272">否</span><span class="sxs-lookup"><span data-stu-id="37bc8-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="37bc8-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37bc8-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="37bc8-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37bc8-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="37bc8-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37bc8-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37bc8-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="37bc8-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-277">Search-Flags</span></span>           | <span data-ttu-id="37bc8-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37bc8-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37bc8-279">System-Flags</span></span>           | <span data-ttu-id="37bc8-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37bc8-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="37bc8-281">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37bc8-281">Classes used in</span></span>        | [<span data-ttu-id="37bc8-282">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="37bc8-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="37bc8-283">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="37bc8-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





