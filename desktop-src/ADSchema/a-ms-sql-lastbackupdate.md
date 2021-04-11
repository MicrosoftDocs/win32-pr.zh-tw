---
title: LastBackupDate 屬性
description: 上次備份資料庫的日期。
ms.assetid: 09bd6c2a-85fe-46af-8569-5bc3cbc8411d
ms.tgt_platform: multiple
keywords:
- LastBackupDate 屬性 AD 架構
- LastBackupDate 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-LastBackupDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d91cadf953ab51185882c73d4d999a5ccb3fed9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935568"
---
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="5c819-105">LastBackupDate 屬性</span><span class="sxs-lookup"><span data-stu-id="5c819-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="5c819-106">上次備份資料庫的日期。</span><span class="sxs-lookup"><span data-stu-id="5c819-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="5c819-107">進入</span><span class="sxs-lookup"><span data-stu-id="5c819-107">Entry</span></span> | <span data-ttu-id="5c819-108">值</span><span class="sxs-lookup"><span data-stu-id="5c819-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5c819-109">CN</span><span class="sxs-lookup"><span data-stu-id="5c819-109">CN</span></span>                | <span data-ttu-id="5c819-110">LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="5c819-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="5c819-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5c819-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5c819-112">LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="5c819-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="5c819-113">大小</span><span class="sxs-lookup"><span data-stu-id="5c819-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5c819-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5c819-114">Update Privilege</span></span>  | <span data-ttu-id="5c819-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="5c819-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="5c819-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5c819-116">Update Frequency</span></span>  | <span data-ttu-id="5c819-117">備份資料庫時。</span><span class="sxs-lookup"><span data-stu-id="5c819-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="5c819-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5c819-118">Attribute-Id</span></span>      | <span data-ttu-id="5c819-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="5c819-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="5c819-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5c819-120">System-Id-Guid</span></span>    | <span data-ttu-id="5c819-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="5c819-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="5c819-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c819-122">Syntax</span></span>            | [<span data-ttu-id="5c819-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5c819-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5c819-124">實作</span><span class="sxs-lookup"><span data-stu-id="5c819-124">Implementations</span></span>

-   [<span data-ttu-id="5c819-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5c819-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5c819-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5c819-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5c819-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5c819-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5c819-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5c819-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5c819-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5c819-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5c819-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5c819-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5c819-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c819-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5c819-132">進入</span><span class="sxs-lookup"><span data-stu-id="5c819-132">Entry</span></span> | <span data-ttu-id="5c819-133">值</span><span class="sxs-lookup"><span data-stu-id="5c819-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c819-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5c819-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c819-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c819-136">System-Only</span></span>            | <span data-ttu-id="5c819-137">否</span><span class="sxs-lookup"><span data-stu-id="5c819-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5c819-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5c819-139">對</span><span class="sxs-lookup"><span data-stu-id="5c819-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="5c819-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5c819-140">Is Indexed</span></span>             | <span data-ttu-id="5c819-141">否</span><span class="sxs-lookup"><span data-stu-id="5c819-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5c819-142">In Global Catalog</span></span>      | <span data-ttu-id="5c819-143">否</span><span class="sxs-lookup"><span data-stu-id="5c819-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5c819-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c819-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5c819-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="5c819-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c819-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c819-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-148">Search-Flags</span></span>           | <span data-ttu-id="5c819-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c819-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-150">System-Flags</span></span>           | <span data-ttu-id="5c819-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c819-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5c819-152">Classes used in</span></span>        | [<span data-ttu-id="5c819-153">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="5c819-154">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5c819-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c819-155">Windows Server 2003</span></span>



| <span data-ttu-id="5c819-156">進入</span><span class="sxs-lookup"><span data-stu-id="5c819-156">Entry</span></span> | <span data-ttu-id="5c819-157">值</span><span class="sxs-lookup"><span data-stu-id="5c819-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c819-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5c819-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c819-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c819-160">System-Only</span></span>            | <span data-ttu-id="5c819-161">否</span><span class="sxs-lookup"><span data-stu-id="5c819-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5c819-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5c819-163">對</span><span class="sxs-lookup"><span data-stu-id="5c819-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="5c819-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5c819-164">Is Indexed</span></span>             | <span data-ttu-id="5c819-165">否</span><span class="sxs-lookup"><span data-stu-id="5c819-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5c819-166">In Global Catalog</span></span>      | <span data-ttu-id="5c819-167">否</span><span class="sxs-lookup"><span data-stu-id="5c819-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5c819-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c819-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5c819-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="5c819-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c819-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c819-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-172">Search-Flags</span></span>           | <span data-ttu-id="5c819-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c819-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-174">System-Flags</span></span>           | <span data-ttu-id="5c819-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c819-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5c819-176">Classes used in</span></span>        | [<span data-ttu-id="5c819-177">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="5c819-178">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5c819-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5c819-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5c819-180">進入</span><span class="sxs-lookup"><span data-stu-id="5c819-180">Entry</span></span> | <span data-ttu-id="5c819-181">值</span><span class="sxs-lookup"><span data-stu-id="5c819-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c819-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5c819-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c819-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c819-184">System-Only</span></span>            | <span data-ttu-id="5c819-185">否</span><span class="sxs-lookup"><span data-stu-id="5c819-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5c819-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5c819-187">對</span><span class="sxs-lookup"><span data-stu-id="5c819-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="5c819-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5c819-188">Is Indexed</span></span>             | <span data-ttu-id="5c819-189">否</span><span class="sxs-lookup"><span data-stu-id="5c819-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5c819-190">In Global Catalog</span></span>      | <span data-ttu-id="5c819-191">否</span><span class="sxs-lookup"><span data-stu-id="5c819-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5c819-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c819-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5c819-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="5c819-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c819-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c819-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-196">Search-Flags</span></span>           | <span data-ttu-id="5c819-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c819-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-198">System-Flags</span></span>           | <span data-ttu-id="5c819-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c819-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5c819-200">Classes used in</span></span>        | [<span data-ttu-id="5c819-201">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="5c819-202">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5c819-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c819-203">Windows Server 2008</span></span>



| <span data-ttu-id="5c819-204">進入</span><span class="sxs-lookup"><span data-stu-id="5c819-204">Entry</span></span> | <span data-ttu-id="5c819-205">值</span><span class="sxs-lookup"><span data-stu-id="5c819-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c819-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5c819-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c819-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c819-208">System-Only</span></span>            | <span data-ttu-id="5c819-209">否</span><span class="sxs-lookup"><span data-stu-id="5c819-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5c819-210">Is-Single-Valued</span></span>       | <span data-ttu-id="5c819-211">對</span><span class="sxs-lookup"><span data-stu-id="5c819-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="5c819-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5c819-212">Is Indexed</span></span>             | <span data-ttu-id="5c819-213">否</span><span class="sxs-lookup"><span data-stu-id="5c819-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5c819-214">In Global Catalog</span></span>      | <span data-ttu-id="5c819-215">否</span><span class="sxs-lookup"><span data-stu-id="5c819-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5c819-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c819-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5c819-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="5c819-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c819-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c819-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-220">Search-Flags</span></span>           | <span data-ttu-id="5c819-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c819-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-222">System-Flags</span></span>           | <span data-ttu-id="5c819-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c819-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5c819-224">Classes used in</span></span>        | [<span data-ttu-id="5c819-225">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="5c819-226">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5c819-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c819-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5c819-228">進入</span><span class="sxs-lookup"><span data-stu-id="5c819-228">Entry</span></span> | <span data-ttu-id="5c819-229">值</span><span class="sxs-lookup"><span data-stu-id="5c819-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c819-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5c819-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c819-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c819-232">System-Only</span></span>            | <span data-ttu-id="5c819-233">否</span><span class="sxs-lookup"><span data-stu-id="5c819-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5c819-234">Is-Single-Valued</span></span>       | <span data-ttu-id="5c819-235">對</span><span class="sxs-lookup"><span data-stu-id="5c819-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="5c819-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5c819-236">Is Indexed</span></span>             | <span data-ttu-id="5c819-237">否</span><span class="sxs-lookup"><span data-stu-id="5c819-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5c819-238">In Global Catalog</span></span>      | <span data-ttu-id="5c819-239">否</span><span class="sxs-lookup"><span data-stu-id="5c819-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5c819-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c819-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5c819-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="5c819-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c819-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c819-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-244">Search-Flags</span></span>           | <span data-ttu-id="5c819-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c819-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-246">System-Flags</span></span>           | <span data-ttu-id="5c819-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c819-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5c819-248">Classes used in</span></span>        | [<span data-ttu-id="5c819-249">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="5c819-250">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5c819-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c819-251">Windows Server 2012</span></span>



| <span data-ttu-id="5c819-252">進入</span><span class="sxs-lookup"><span data-stu-id="5c819-252">Entry</span></span> | <span data-ttu-id="5c819-253">值</span><span class="sxs-lookup"><span data-stu-id="5c819-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c819-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5c819-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c819-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="5c819-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c819-256">System-Only</span></span>            | <span data-ttu-id="5c819-257">否</span><span class="sxs-lookup"><span data-stu-id="5c819-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5c819-258">Is-Single-Valued</span></span>       | <span data-ttu-id="5c819-259">對</span><span class="sxs-lookup"><span data-stu-id="5c819-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="5c819-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5c819-260">Is Indexed</span></span>             | <span data-ttu-id="5c819-261">否</span><span class="sxs-lookup"><span data-stu-id="5c819-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5c819-262">In Global Catalog</span></span>      | <span data-ttu-id="5c819-263">否</span><span class="sxs-lookup"><span data-stu-id="5c819-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="5c819-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5c819-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c819-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5c819-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="5c819-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c819-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c819-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="5c819-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-268">Search-Flags</span></span>           | <span data-ttu-id="5c819-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c819-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c819-270">System-Flags</span></span>           | <span data-ttu-id="5c819-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c819-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="5c819-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5c819-272">Classes used in</span></span>        | [<span data-ttu-id="5c819-273">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="5c819-274">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="5c819-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





