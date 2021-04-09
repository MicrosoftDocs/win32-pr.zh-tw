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
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="a7e82-105">MS-CHAP 類型屬性</span><span class="sxs-lookup"><span data-stu-id="a7e82-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="a7e82-106">此 SQL server 使用的複寫類型。</span><span class="sxs-lookup"><span data-stu-id="a7e82-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="a7e82-107">下列值是這個屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="a7e82-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="a7e82-108">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-108">Value</span></span>        | <span data-ttu-id="a7e82-109">描述</span><span class="sxs-lookup"><span data-stu-id="a7e82-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="a7e82-110">0</span><span class="sxs-lookup"><span data-stu-id="a7e82-110">0</span></span><br/> | <span data-ttu-id="a7e82-111">異動複寫。</span><span class="sxs-lookup"><span data-stu-id="a7e82-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="a7e82-112">1</span><span class="sxs-lookup"><span data-stu-id="a7e82-112">1</span></span><br/> | <span data-ttu-id="a7e82-113">快照式複寫。</span><span class="sxs-lookup"><span data-stu-id="a7e82-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="a7e82-114">2</span><span class="sxs-lookup"><span data-stu-id="a7e82-114">2</span></span><br/> | <span data-ttu-id="a7e82-115">合併式複寫。</span><span class="sxs-lookup"><span data-stu-id="a7e82-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="a7e82-116">進入</span><span class="sxs-lookup"><span data-stu-id="a7e82-116">Entry</span></span> | <span data-ttu-id="a7e82-117">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a7e82-118">CN</span><span class="sxs-lookup"><span data-stu-id="a7e82-118">CN</span></span>                | <span data-ttu-id="a7e82-119">MS-CHAP 類型</span><span class="sxs-lookup"><span data-stu-id="a7e82-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="a7e82-120">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a7e82-120">Ldap-Display-Name</span></span> | <span data-ttu-id="a7e82-121">Ms-chap 類型</span><span class="sxs-lookup"><span data-stu-id="a7e82-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="a7e82-122">大小</span><span class="sxs-lookup"><span data-stu-id="a7e82-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="a7e82-123">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a7e82-123">Update Privilege</span></span>  | <span data-ttu-id="a7e82-124">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="a7e82-124">Domain administrator</span></span>                        |
| <span data-ttu-id="a7e82-125">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a7e82-125">Update Frequency</span></span>  | <span data-ttu-id="a7e82-126">當複寫設定完成時。</span><span class="sxs-lookup"><span data-stu-id="a7e82-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="a7e82-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7e82-127">Attribute-Id</span></span>      | <span data-ttu-id="a7e82-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="a7e82-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="a7e82-129">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a7e82-129">System-Id-Guid</span></span>    | <span data-ttu-id="a7e82-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a7e82-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="a7e82-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7e82-131">Syntax</span></span>            | [<span data-ttu-id="a7e82-132">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a7e82-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a7e82-133">實作</span><span class="sxs-lookup"><span data-stu-id="a7e82-133">Implementations</span></span>

-   [<span data-ttu-id="a7e82-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a7e82-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a7e82-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7e82-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7e82-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7e82-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7e82-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7e82-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7e82-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7e82-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7e82-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7e82-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a7e82-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7e82-140">Windows 2000 Server</span></span>



| <span data-ttu-id="a7e82-141">進入</span><span class="sxs-lookup"><span data-stu-id="a7e82-141">Entry</span></span> | <span data-ttu-id="a7e82-142">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e82-143">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7e82-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e82-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e82-145">System-Only</span></span>            | <span data-ttu-id="a7e82-146">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-147">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7e82-147">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e82-148">對</span><span class="sxs-lookup"><span data-stu-id="a7e82-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="a7e82-149">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7e82-149">Is Indexed</span></span>             | <span data-ttu-id="a7e82-150">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-151">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7e82-151">In Global Catalog</span></span>      | <span data-ttu-id="a7e82-152">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-153">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7e82-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e82-154">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7e82-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="a7e82-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e82-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e82-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-157">Search-Flags</span></span>           | <span data-ttu-id="a7e82-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e82-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-159">System-Flags</span></span>           | <span data-ttu-id="a7e82-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7e82-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-161">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7e82-161">Classes used in</span></span>        | [<span data-ttu-id="a7e82-162">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a7e82-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="a7e82-163">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="a7e82-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a7e82-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7e82-164">Windows Server 2003</span></span>



| <span data-ttu-id="a7e82-165">進入</span><span class="sxs-lookup"><span data-stu-id="a7e82-165">Entry</span></span> | <span data-ttu-id="a7e82-166">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e82-167">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7e82-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e82-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e82-169">System-Only</span></span>            | <span data-ttu-id="a7e82-170">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-171">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7e82-171">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e82-172">對</span><span class="sxs-lookup"><span data-stu-id="a7e82-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="a7e82-173">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7e82-173">Is Indexed</span></span>             | <span data-ttu-id="a7e82-174">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-175">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7e82-175">In Global Catalog</span></span>      | <span data-ttu-id="a7e82-176">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-177">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7e82-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e82-178">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7e82-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="a7e82-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e82-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e82-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-181">Search-Flags</span></span>           | <span data-ttu-id="a7e82-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e82-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-183">System-Flags</span></span>           | <span data-ttu-id="a7e82-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7e82-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-185">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7e82-185">Classes used in</span></span>        | [<span data-ttu-id="a7e82-186">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a7e82-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="a7e82-187">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="a7e82-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7e82-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7e82-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7e82-189">進入</span><span class="sxs-lookup"><span data-stu-id="a7e82-189">Entry</span></span> | <span data-ttu-id="a7e82-190">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e82-191">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7e82-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e82-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e82-193">System-Only</span></span>            | <span data-ttu-id="a7e82-194">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7e82-195">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e82-196">對</span><span class="sxs-lookup"><span data-stu-id="a7e82-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="a7e82-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7e82-197">Is Indexed</span></span>             | <span data-ttu-id="a7e82-198">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7e82-199">In Global Catalog</span></span>      | <span data-ttu-id="a7e82-200">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7e82-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e82-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7e82-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="a7e82-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e82-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e82-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-205">Search-Flags</span></span>           | <span data-ttu-id="a7e82-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e82-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-207">System-Flags</span></span>           | <span data-ttu-id="a7e82-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7e82-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7e82-209">Classes used in</span></span>        | [<span data-ttu-id="a7e82-210">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a7e82-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="a7e82-211">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="a7e82-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7e82-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7e82-212">Windows Server 2008</span></span>



| <span data-ttu-id="a7e82-213">進入</span><span class="sxs-lookup"><span data-stu-id="a7e82-213">Entry</span></span> | <span data-ttu-id="a7e82-214">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e82-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7e82-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e82-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e82-217">System-Only</span></span>            | <span data-ttu-id="a7e82-218">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7e82-219">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e82-220">對</span><span class="sxs-lookup"><span data-stu-id="a7e82-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="a7e82-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7e82-221">Is Indexed</span></span>             | <span data-ttu-id="a7e82-222">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7e82-223">In Global Catalog</span></span>      | <span data-ttu-id="a7e82-224">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7e82-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e82-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7e82-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="a7e82-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e82-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e82-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-229">Search-Flags</span></span>           | <span data-ttu-id="a7e82-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e82-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-231">System-Flags</span></span>           | <span data-ttu-id="a7e82-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7e82-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7e82-233">Classes used in</span></span>        | [<span data-ttu-id="a7e82-234">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a7e82-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="a7e82-235">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="a7e82-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7e82-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7e82-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7e82-237">進入</span><span class="sxs-lookup"><span data-stu-id="a7e82-237">Entry</span></span> | <span data-ttu-id="a7e82-238">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e82-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7e82-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e82-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e82-241">System-Only</span></span>            | <span data-ttu-id="a7e82-242">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7e82-243">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e82-244">對</span><span class="sxs-lookup"><span data-stu-id="a7e82-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="a7e82-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7e82-245">Is Indexed</span></span>             | <span data-ttu-id="a7e82-246">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7e82-247">In Global Catalog</span></span>      | <span data-ttu-id="a7e82-248">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7e82-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e82-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7e82-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="a7e82-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e82-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e82-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-253">Search-Flags</span></span>           | <span data-ttu-id="a7e82-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e82-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-255">System-Flags</span></span>           | <span data-ttu-id="a7e82-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7e82-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-257">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7e82-257">Classes used in</span></span>        | [<span data-ttu-id="a7e82-258">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a7e82-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="a7e82-259">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="a7e82-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7e82-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7e82-260">Windows Server 2012</span></span>



| <span data-ttu-id="a7e82-261">進入</span><span class="sxs-lookup"><span data-stu-id="a7e82-261">Entry</span></span> | <span data-ttu-id="a7e82-262">值</span><span class="sxs-lookup"><span data-stu-id="a7e82-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e82-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a7e82-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7e82-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7e82-265">System-Only</span></span>            | <span data-ttu-id="a7e82-266">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a7e82-267">Is-Single-Valued</span></span>       | <span data-ttu-id="a7e82-268">對</span><span class="sxs-lookup"><span data-stu-id="a7e82-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="a7e82-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a7e82-269">Is Indexed</span></span>             | <span data-ttu-id="a7e82-270">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a7e82-271">In Global Catalog</span></span>      | <span data-ttu-id="a7e82-272">否</span><span class="sxs-lookup"><span data-stu-id="a7e82-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="a7e82-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a7e82-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7e82-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a7e82-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="a7e82-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7e82-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7e82-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="a7e82-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-277">Search-Flags</span></span>           | <span data-ttu-id="a7e82-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7e82-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e82-279">System-Flags</span></span>           | <span data-ttu-id="a7e82-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7e82-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="a7e82-281">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a7e82-281">Classes used in</span></span>        | [<span data-ttu-id="a7e82-282">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a7e82-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="a7e82-283">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="a7e82-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





