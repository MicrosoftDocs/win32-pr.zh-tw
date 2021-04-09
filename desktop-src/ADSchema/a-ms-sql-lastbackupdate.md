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
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="0e36c-105">LastBackupDate 屬性</span><span class="sxs-lookup"><span data-stu-id="0e36c-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="0e36c-106">上次備份資料庫的日期。</span><span class="sxs-lookup"><span data-stu-id="0e36c-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="0e36c-107">進入</span><span class="sxs-lookup"><span data-stu-id="0e36c-107">Entry</span></span> | <span data-ttu-id="0e36c-108">值</span><span class="sxs-lookup"><span data-stu-id="0e36c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0e36c-109">CN</span><span class="sxs-lookup"><span data-stu-id="0e36c-109">CN</span></span>                | <span data-ttu-id="0e36c-110">LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="0e36c-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="0e36c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0e36c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0e36c-112">LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="0e36c-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="0e36c-113">大小</span><span class="sxs-lookup"><span data-stu-id="0e36c-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0e36c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0e36c-114">Update Privilege</span></span>  | <span data-ttu-id="0e36c-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="0e36c-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="0e36c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0e36c-116">Update Frequency</span></span>  | <span data-ttu-id="0e36c-117">備份資料庫時。</span><span class="sxs-lookup"><span data-stu-id="0e36c-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="0e36c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0e36c-118">Attribute-Id</span></span>      | <span data-ttu-id="0e36c-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="0e36c-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="0e36c-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0e36c-120">System-Id-Guid</span></span>    | <span data-ttu-id="0e36c-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="0e36c-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="0e36c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e36c-122">Syntax</span></span>            | [<span data-ttu-id="0e36c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0e36c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0e36c-124">實作</span><span class="sxs-lookup"><span data-stu-id="0e36c-124">Implementations</span></span>

-   [<span data-ttu-id="0e36c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0e36c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0e36c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0e36c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0e36c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0e36c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0e36c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0e36c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0e36c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0e36c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0e36c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0e36c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0e36c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0e36c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0e36c-132">進入</span><span class="sxs-lookup"><span data-stu-id="0e36c-132">Entry</span></span> | <span data-ttu-id="0e36c-133">值</span><span class="sxs-lookup"><span data-stu-id="0e36c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e36c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e36c-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e36c-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e36c-136">System-Only</span></span>            | <span data-ttu-id="0e36c-137">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e36c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0e36c-139">對</span><span class="sxs-lookup"><span data-stu-id="0e36c-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="0e36c-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e36c-140">Is Indexed</span></span>             | <span data-ttu-id="0e36c-141">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e36c-142">In Global Catalog</span></span>      | <span data-ttu-id="0e36c-143">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e36c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e36c-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e36c-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0e36c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e36c-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e36c-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-148">Search-Flags</span></span>           | <span data-ttu-id="0e36c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e36c-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-150">System-Flags</span></span>           | <span data-ttu-id="0e36c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e36c-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e36c-152">Classes used in</span></span>        | [<span data-ttu-id="0e36c-153">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0e36c-154">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0e36c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e36c-155">Windows Server 2003</span></span>



| <span data-ttu-id="0e36c-156">進入</span><span class="sxs-lookup"><span data-stu-id="0e36c-156">Entry</span></span> | <span data-ttu-id="0e36c-157">值</span><span class="sxs-lookup"><span data-stu-id="0e36c-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e36c-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e36c-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e36c-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e36c-160">System-Only</span></span>            | <span data-ttu-id="0e36c-161">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e36c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0e36c-163">對</span><span class="sxs-lookup"><span data-stu-id="0e36c-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="0e36c-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e36c-164">Is Indexed</span></span>             | <span data-ttu-id="0e36c-165">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e36c-166">In Global Catalog</span></span>      | <span data-ttu-id="0e36c-167">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e36c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e36c-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e36c-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0e36c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e36c-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e36c-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-172">Search-Flags</span></span>           | <span data-ttu-id="0e36c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e36c-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-174">System-Flags</span></span>           | <span data-ttu-id="0e36c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e36c-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e36c-176">Classes used in</span></span>        | [<span data-ttu-id="0e36c-177">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0e36c-178">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0e36c-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0e36c-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0e36c-180">進入</span><span class="sxs-lookup"><span data-stu-id="0e36c-180">Entry</span></span> | <span data-ttu-id="0e36c-181">值</span><span class="sxs-lookup"><span data-stu-id="0e36c-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e36c-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e36c-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e36c-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e36c-184">System-Only</span></span>            | <span data-ttu-id="0e36c-185">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e36c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0e36c-187">對</span><span class="sxs-lookup"><span data-stu-id="0e36c-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="0e36c-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e36c-188">Is Indexed</span></span>             | <span data-ttu-id="0e36c-189">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e36c-190">In Global Catalog</span></span>      | <span data-ttu-id="0e36c-191">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e36c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e36c-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e36c-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0e36c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e36c-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e36c-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-196">Search-Flags</span></span>           | <span data-ttu-id="0e36c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e36c-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-198">System-Flags</span></span>           | <span data-ttu-id="0e36c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e36c-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e36c-200">Classes used in</span></span>        | [<span data-ttu-id="0e36c-201">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0e36c-202">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0e36c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e36c-203">Windows Server 2008</span></span>



| <span data-ttu-id="0e36c-204">進入</span><span class="sxs-lookup"><span data-stu-id="0e36c-204">Entry</span></span> | <span data-ttu-id="0e36c-205">值</span><span class="sxs-lookup"><span data-stu-id="0e36c-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e36c-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e36c-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e36c-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e36c-208">System-Only</span></span>            | <span data-ttu-id="0e36c-209">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e36c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="0e36c-211">對</span><span class="sxs-lookup"><span data-stu-id="0e36c-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="0e36c-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e36c-212">Is Indexed</span></span>             | <span data-ttu-id="0e36c-213">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e36c-214">In Global Catalog</span></span>      | <span data-ttu-id="0e36c-215">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e36c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e36c-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e36c-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0e36c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e36c-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e36c-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-220">Search-Flags</span></span>           | <span data-ttu-id="0e36c-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e36c-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-222">System-Flags</span></span>           | <span data-ttu-id="0e36c-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e36c-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e36c-224">Classes used in</span></span>        | [<span data-ttu-id="0e36c-225">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0e36c-226">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0e36c-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e36c-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0e36c-228">進入</span><span class="sxs-lookup"><span data-stu-id="0e36c-228">Entry</span></span> | <span data-ttu-id="0e36c-229">值</span><span class="sxs-lookup"><span data-stu-id="0e36c-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e36c-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e36c-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e36c-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e36c-232">System-Only</span></span>            | <span data-ttu-id="0e36c-233">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e36c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0e36c-235">對</span><span class="sxs-lookup"><span data-stu-id="0e36c-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="0e36c-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e36c-236">Is Indexed</span></span>             | <span data-ttu-id="0e36c-237">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e36c-238">In Global Catalog</span></span>      | <span data-ttu-id="0e36c-239">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e36c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e36c-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e36c-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0e36c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e36c-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e36c-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-244">Search-Flags</span></span>           | <span data-ttu-id="0e36c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e36c-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-246">System-Flags</span></span>           | <span data-ttu-id="0e36c-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e36c-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e36c-248">Classes used in</span></span>        | [<span data-ttu-id="0e36c-249">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0e36c-250">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0e36c-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e36c-251">Windows Server 2012</span></span>



| <span data-ttu-id="0e36c-252">進入</span><span class="sxs-lookup"><span data-stu-id="0e36c-252">Entry</span></span> | <span data-ttu-id="0e36c-253">值</span><span class="sxs-lookup"><span data-stu-id="0e36c-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e36c-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0e36c-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e36c-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="0e36c-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e36c-256">System-Only</span></span>            | <span data-ttu-id="0e36c-257">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0e36c-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0e36c-259">對</span><span class="sxs-lookup"><span data-stu-id="0e36c-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="0e36c-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0e36c-260">Is Indexed</span></span>             | <span data-ttu-id="0e36c-261">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0e36c-262">In Global Catalog</span></span>      | <span data-ttu-id="0e36c-263">否</span><span class="sxs-lookup"><span data-stu-id="0e36c-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="0e36c-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0e36c-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e36c-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0e36c-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="0e36c-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e36c-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e36c-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="0e36c-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-268">Search-Flags</span></span>           | <span data-ttu-id="0e36c-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e36c-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e36c-270">System-Flags</span></span>           | <span data-ttu-id="0e36c-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e36c-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="0e36c-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0e36c-272">Classes used in</span></span>        | [<span data-ttu-id="0e36c-273">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="0e36c-274">**OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="0e36c-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





