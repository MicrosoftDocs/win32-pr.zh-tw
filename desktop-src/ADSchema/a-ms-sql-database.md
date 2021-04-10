---
title: TRANSACT-SQL-Database 屬性
description: 複寫所涉及的 SQL Server 資料庫名稱。
ms.assetid: 624705d9-df3f-458e-98f4-fb8da073efd6
ms.tgt_platform: multiple
keywords:
- MS-CHAP-資料庫屬性 AD 架構
- Ms-chap-資料庫屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Database
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6c448213bee18fede3cc8a77cabf607c3b2ee3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844703"
---
# <a name="ms-sql-database-attribute"></a><span data-ttu-id="2c0bc-105">TRANSACT-SQL-Database 屬性</span><span class="sxs-lookup"><span data-stu-id="2c0bc-105">MS-SQL-Database attribute</span></span>

<span data-ttu-id="2c0bc-106">複寫所涉及的 SQL Server 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2c0bc-106">The name of the SQL Server database involved in replication.</span></span>



| <span data-ttu-id="2c0bc-107">進入</span><span class="sxs-lookup"><span data-stu-id="2c0bc-107">Entry</span></span> | <span data-ttu-id="2c0bc-108">值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2c0bc-109">CN</span><span class="sxs-lookup"><span data-stu-id="2c0bc-109">CN</span></span>                | <span data-ttu-id="2c0bc-110">MS-SQL-資料庫</span><span class="sxs-lookup"><span data-stu-id="2c0bc-110">MS-SQL-Database</span></span>                             |
| <span data-ttu-id="2c0bc-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2c0bc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2c0bc-112">mS-SQL-資料庫</span><span class="sxs-lookup"><span data-stu-id="2c0bc-112">mS-SQL-Database</span></span>                             |
| <span data-ttu-id="2c0bc-113">大小</span><span class="sxs-lookup"><span data-stu-id="2c0bc-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2c0bc-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2c0bc-114">Update Privilege</span></span>  | <span data-ttu-id="2c0bc-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="2c0bc-115">Domain administrator</span></span>                        |
| <span data-ttu-id="2c0bc-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2c0bc-116">Update Frequency</span></span>  | <span data-ttu-id="2c0bc-117">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="2c0bc-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="2c0bc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c0bc-118">Attribute-Id</span></span>      | <span data-ttu-id="2c0bc-119">1.2.840.113556.1.4.1393</span><span class="sxs-lookup"><span data-stu-id="2c0bc-119">1.2.840.113556.1.4.1393</span></span>                     |
| <span data-ttu-id="2c0bc-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2c0bc-120">System-Id-Guid</span></span>    | <span data-ttu-id="2c0bc-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2c0bc-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="2c0bc-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c0bc-122">Syntax</span></span>            | [<span data-ttu-id="2c0bc-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2c0bc-124">實作</span><span class="sxs-lookup"><span data-stu-id="2c0bc-124">Implementations</span></span>

-   [<span data-ttu-id="2c0bc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2c0bc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2c0bc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2c0bc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2c0bc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2c0bc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2c0bc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c0bc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2c0bc-132">進入</span><span class="sxs-lookup"><span data-stu-id="2c0bc-132">Entry</span></span> | <span data-ttu-id="2c0bc-133">值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c0bc-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c0bc-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c0bc-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c0bc-136">System-Only</span></span>            | <span data-ttu-id="2c0bc-137">否</span><span class="sxs-lookup"><span data-stu-id="2c0bc-137">False</span></span>                                                               |
| <span data-ttu-id="2c0bc-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2c0bc-139">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-139">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c0bc-140">Is Indexed</span></span>             | <span data-ttu-id="2c0bc-141">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-141">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c0bc-142">In Global Catalog</span></span>      | <span data-ttu-id="2c0bc-143">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-143">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c0bc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c0bc-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c0bc-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2c0bc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c0bc-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c0bc-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-148">Search-Flags</span></span>           | <span data-ttu-id="2c0bc-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c0bc-149">0x00000001</span></span>                                                          |
| <span data-ttu-id="2c0bc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-150">System-Flags</span></span>           | <span data-ttu-id="2c0bc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c0bc-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="2c0bc-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c0bc-152">Classes used in</span></span>        | [<span data-ttu-id="2c0bc-153">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2c0bc-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c0bc-154">Windows Server 2003</span></span>



| <span data-ttu-id="2c0bc-155">進入</span><span class="sxs-lookup"><span data-stu-id="2c0bc-155">Entry</span></span> | <span data-ttu-id="2c0bc-156">值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c0bc-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c0bc-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c0bc-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c0bc-159">System-Only</span></span>            | <span data-ttu-id="2c0bc-160">否</span><span class="sxs-lookup"><span data-stu-id="2c0bc-160">False</span></span>                                                               |
| <span data-ttu-id="2c0bc-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2c0bc-162">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-162">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c0bc-163">Is Indexed</span></span>             | <span data-ttu-id="2c0bc-164">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-164">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c0bc-165">In Global Catalog</span></span>      | <span data-ttu-id="2c0bc-166">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-166">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c0bc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c0bc-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c0bc-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2c0bc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c0bc-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c0bc-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-171">Search-Flags</span></span>           | <span data-ttu-id="2c0bc-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c0bc-172">0x00000001</span></span>                                                          |
| <span data-ttu-id="2c0bc-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-173">System-Flags</span></span>           | <span data-ttu-id="2c0bc-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c0bc-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="2c0bc-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c0bc-175">Classes used in</span></span>        | [<span data-ttu-id="2c0bc-176">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2c0bc-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2c0bc-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2c0bc-178">進入</span><span class="sxs-lookup"><span data-stu-id="2c0bc-178">Entry</span></span> | <span data-ttu-id="2c0bc-179">值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c0bc-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c0bc-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c0bc-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c0bc-182">System-Only</span></span>            | <span data-ttu-id="2c0bc-183">否</span><span class="sxs-lookup"><span data-stu-id="2c0bc-183">False</span></span>                                                               |
| <span data-ttu-id="2c0bc-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2c0bc-185">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-185">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c0bc-186">Is Indexed</span></span>             | <span data-ttu-id="2c0bc-187">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-187">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c0bc-188">In Global Catalog</span></span>      | <span data-ttu-id="2c0bc-189">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-189">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c0bc-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c0bc-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c0bc-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2c0bc-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c0bc-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c0bc-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-194">Search-Flags</span></span>           | <span data-ttu-id="2c0bc-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c0bc-195">0x00000001</span></span>                                                          |
| <span data-ttu-id="2c0bc-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-196">System-Flags</span></span>           | <span data-ttu-id="2c0bc-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c0bc-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="2c0bc-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c0bc-198">Classes used in</span></span>        | [<span data-ttu-id="2c0bc-199">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2c0bc-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c0bc-200">Windows Server 2008</span></span>



| <span data-ttu-id="2c0bc-201">進入</span><span class="sxs-lookup"><span data-stu-id="2c0bc-201">Entry</span></span> | <span data-ttu-id="2c0bc-202">值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c0bc-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c0bc-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c0bc-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c0bc-205">System-Only</span></span>            | <span data-ttu-id="2c0bc-206">否</span><span class="sxs-lookup"><span data-stu-id="2c0bc-206">False</span></span>                                                               |
| <span data-ttu-id="2c0bc-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2c0bc-208">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-208">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c0bc-209">Is Indexed</span></span>             | <span data-ttu-id="2c0bc-210">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-210">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c0bc-211">In Global Catalog</span></span>      | <span data-ttu-id="2c0bc-212">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-212">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c0bc-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c0bc-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c0bc-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2c0bc-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c0bc-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c0bc-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-217">Search-Flags</span></span>           | <span data-ttu-id="2c0bc-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c0bc-218">0x00000001</span></span>                                                          |
| <span data-ttu-id="2c0bc-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-219">System-Flags</span></span>           | <span data-ttu-id="2c0bc-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c0bc-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="2c0bc-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c0bc-221">Classes used in</span></span>        | [<span data-ttu-id="2c0bc-222">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2c0bc-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c0bc-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2c0bc-224">進入</span><span class="sxs-lookup"><span data-stu-id="2c0bc-224">Entry</span></span> | <span data-ttu-id="2c0bc-225">值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c0bc-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c0bc-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c0bc-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c0bc-228">System-Only</span></span>            | <span data-ttu-id="2c0bc-229">否</span><span class="sxs-lookup"><span data-stu-id="2c0bc-229">False</span></span>                                                               |
| <span data-ttu-id="2c0bc-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2c0bc-231">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-231">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c0bc-232">Is Indexed</span></span>             | <span data-ttu-id="2c0bc-233">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-233">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c0bc-234">In Global Catalog</span></span>      | <span data-ttu-id="2c0bc-235">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-235">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c0bc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c0bc-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c0bc-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2c0bc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c0bc-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c0bc-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-240">Search-Flags</span></span>           | <span data-ttu-id="2c0bc-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c0bc-241">0x00000001</span></span>                                                          |
| <span data-ttu-id="2c0bc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-242">System-Flags</span></span>           | <span data-ttu-id="2c0bc-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c0bc-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="2c0bc-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c0bc-244">Classes used in</span></span>        | [<span data-ttu-id="2c0bc-245">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2c0bc-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c0bc-246">Windows Server 2012</span></span>



| <span data-ttu-id="2c0bc-247">進入</span><span class="sxs-lookup"><span data-stu-id="2c0bc-247">Entry</span></span> | <span data-ttu-id="2c0bc-248">值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c0bc-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c0bc-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c0bc-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2c0bc-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c0bc-251">System-Only</span></span>            | <span data-ttu-id="2c0bc-252">否</span><span class="sxs-lookup"><span data-stu-id="2c0bc-252">False</span></span>                                                               |
| <span data-ttu-id="2c0bc-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c0bc-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2c0bc-254">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-254">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c0bc-255">Is Indexed</span></span>             | <span data-ttu-id="2c0bc-256">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-256">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c0bc-257">In Global Catalog</span></span>      | <span data-ttu-id="2c0bc-258">對</span><span class="sxs-lookup"><span data-stu-id="2c0bc-258">True</span></span>                                                                |
| <span data-ttu-id="2c0bc-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c0bc-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c0bc-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c0bc-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2c0bc-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c0bc-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c0bc-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2c0bc-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-263">Search-Flags</span></span>           | <span data-ttu-id="2c0bc-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c0bc-264">0x00000001</span></span>                                                          |
| <span data-ttu-id="2c0bc-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c0bc-265">System-Flags</span></span>           | <span data-ttu-id="2c0bc-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c0bc-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="2c0bc-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c0bc-267">Classes used in</span></span>        | [<span data-ttu-id="2c0bc-268">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="2c0bc-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





