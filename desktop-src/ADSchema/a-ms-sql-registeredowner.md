---
title: '>registeredowner 屬性'
description: SQL Server 目前實例的註冊擁有者。
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- '>registeredowner 屬性 AD 架構'
- '>registeredowner 屬性 AD 架構'
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e201494afffdfea59b75bc1901a474469871351
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687279"
---
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="d3634-105">>registeredowner 屬性</span><span class="sxs-lookup"><span data-stu-id="d3634-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="d3634-106">SQL Server 目前實例的註冊擁有者。</span><span class="sxs-lookup"><span data-stu-id="d3634-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="d3634-107">進入</span><span class="sxs-lookup"><span data-stu-id="d3634-107">Entry</span></span> | <span data-ttu-id="d3634-108">值</span><span class="sxs-lookup"><span data-stu-id="d3634-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d3634-109">CN</span><span class="sxs-lookup"><span data-stu-id="d3634-109">CN</span></span>                | <span data-ttu-id="d3634-110">>registeredowner</span><span class="sxs-lookup"><span data-stu-id="d3634-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="d3634-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d3634-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d3634-112">>registeredowner</span><span class="sxs-lookup"><span data-stu-id="d3634-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="d3634-113">大小</span><span class="sxs-lookup"><span data-stu-id="d3634-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d3634-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d3634-114">Update Privilege</span></span>  | <span data-ttu-id="d3634-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="d3634-115">Domain administrator</span></span>                        |
| <span data-ttu-id="d3634-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d3634-116">Update Frequency</span></span>  | <span data-ttu-id="d3634-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="d3634-117">At system setup.</span></span>                            |
| <span data-ttu-id="d3634-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3634-118">Attribute-Id</span></span>      | <span data-ttu-id="d3634-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="d3634-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="d3634-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d3634-120">System-Id-Guid</span></span>    | <span data-ttu-id="d3634-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d3634-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="d3634-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3634-122">Syntax</span></span>            | [<span data-ttu-id="d3634-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d3634-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d3634-124">實作</span><span class="sxs-lookup"><span data-stu-id="d3634-124">Implementations</span></span>

-   [<span data-ttu-id="d3634-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d3634-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d3634-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3634-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3634-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3634-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3634-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3634-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3634-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3634-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3634-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3634-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d3634-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3634-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d3634-132">進入</span><span class="sxs-lookup"><span data-stu-id="d3634-132">Entry</span></span> | <span data-ttu-id="d3634-133">值</span><span class="sxs-lookup"><span data-stu-id="d3634-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3634-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3634-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3634-136">System-Only</span></span>            | <span data-ttu-id="d3634-137">否</span><span class="sxs-lookup"><span data-stu-id="d3634-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3634-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d3634-139">對</span><span class="sxs-lookup"><span data-stu-id="d3634-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="d3634-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3634-140">Is Indexed</span></span>             | <span data-ttu-id="d3634-141">否</span><span class="sxs-lookup"><span data-stu-id="d3634-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3634-142">In Global Catalog</span></span>      | <span data-ttu-id="d3634-143">否</span><span class="sxs-lookup"><span data-stu-id="d3634-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3634-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3634-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3634-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="d3634-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3634-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3634-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-148">Search-Flags</span></span>           | <span data-ttu-id="d3634-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3634-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="d3634-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-150">System-Flags</span></span>           | <span data-ttu-id="d3634-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3634-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="d3634-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3634-152">Classes used in</span></span>        | [<span data-ttu-id="d3634-153">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d3634-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="d3634-154">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="d3634-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d3634-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3634-155">Windows Server 2003</span></span>



| <span data-ttu-id="d3634-156">進入</span><span class="sxs-lookup"><span data-stu-id="d3634-156">Entry</span></span> | <span data-ttu-id="d3634-157">值</span><span class="sxs-lookup"><span data-stu-id="d3634-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3634-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3634-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3634-160">System-Only</span></span>            | <span data-ttu-id="d3634-161">否</span><span class="sxs-lookup"><span data-stu-id="d3634-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3634-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d3634-163">對</span><span class="sxs-lookup"><span data-stu-id="d3634-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="d3634-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3634-164">Is Indexed</span></span>             | <span data-ttu-id="d3634-165">否</span><span class="sxs-lookup"><span data-stu-id="d3634-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3634-166">In Global Catalog</span></span>      | <span data-ttu-id="d3634-167">否</span><span class="sxs-lookup"><span data-stu-id="d3634-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3634-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3634-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3634-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="d3634-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3634-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3634-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-172">Search-Flags</span></span>           | <span data-ttu-id="d3634-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3634-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="d3634-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-174">System-Flags</span></span>           | <span data-ttu-id="d3634-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3634-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="d3634-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3634-176">Classes used in</span></span>        | [<span data-ttu-id="d3634-177">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d3634-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="d3634-178">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="d3634-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3634-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3634-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3634-180">進入</span><span class="sxs-lookup"><span data-stu-id="d3634-180">Entry</span></span> | <span data-ttu-id="d3634-181">值</span><span class="sxs-lookup"><span data-stu-id="d3634-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3634-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3634-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3634-184">System-Only</span></span>            | <span data-ttu-id="d3634-185">否</span><span class="sxs-lookup"><span data-stu-id="d3634-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3634-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d3634-187">對</span><span class="sxs-lookup"><span data-stu-id="d3634-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="d3634-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3634-188">Is Indexed</span></span>             | <span data-ttu-id="d3634-189">否</span><span class="sxs-lookup"><span data-stu-id="d3634-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3634-190">In Global Catalog</span></span>      | <span data-ttu-id="d3634-191">否</span><span class="sxs-lookup"><span data-stu-id="d3634-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3634-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3634-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3634-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="d3634-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3634-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3634-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-196">Search-Flags</span></span>           | <span data-ttu-id="d3634-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3634-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="d3634-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-198">System-Flags</span></span>           | <span data-ttu-id="d3634-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3634-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="d3634-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3634-200">Classes used in</span></span>        | [<span data-ttu-id="d3634-201">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d3634-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="d3634-202">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="d3634-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3634-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3634-203">Windows Server 2008</span></span>



| <span data-ttu-id="d3634-204">進入</span><span class="sxs-lookup"><span data-stu-id="d3634-204">Entry</span></span> | <span data-ttu-id="d3634-205">值</span><span class="sxs-lookup"><span data-stu-id="d3634-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3634-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3634-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3634-208">System-Only</span></span>            | <span data-ttu-id="d3634-209">否</span><span class="sxs-lookup"><span data-stu-id="d3634-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3634-210">Is-Single-Valued</span></span>       | <span data-ttu-id="d3634-211">對</span><span class="sxs-lookup"><span data-stu-id="d3634-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="d3634-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3634-212">Is Indexed</span></span>             | <span data-ttu-id="d3634-213">否</span><span class="sxs-lookup"><span data-stu-id="d3634-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3634-214">In Global Catalog</span></span>      | <span data-ttu-id="d3634-215">否</span><span class="sxs-lookup"><span data-stu-id="d3634-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3634-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3634-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3634-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="d3634-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3634-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3634-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-220">Search-Flags</span></span>           | <span data-ttu-id="d3634-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3634-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="d3634-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-222">System-Flags</span></span>           | <span data-ttu-id="d3634-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3634-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="d3634-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3634-224">Classes used in</span></span>        | [<span data-ttu-id="d3634-225">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d3634-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="d3634-226">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="d3634-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3634-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3634-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3634-228">進入</span><span class="sxs-lookup"><span data-stu-id="d3634-228">Entry</span></span> | <span data-ttu-id="d3634-229">值</span><span class="sxs-lookup"><span data-stu-id="d3634-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3634-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3634-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3634-232">System-Only</span></span>            | <span data-ttu-id="d3634-233">否</span><span class="sxs-lookup"><span data-stu-id="d3634-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3634-234">Is-Single-Valued</span></span>       | <span data-ttu-id="d3634-235">對</span><span class="sxs-lookup"><span data-stu-id="d3634-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="d3634-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3634-236">Is Indexed</span></span>             | <span data-ttu-id="d3634-237">否</span><span class="sxs-lookup"><span data-stu-id="d3634-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3634-238">In Global Catalog</span></span>      | <span data-ttu-id="d3634-239">否</span><span class="sxs-lookup"><span data-stu-id="d3634-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3634-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3634-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3634-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="d3634-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3634-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3634-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-244">Search-Flags</span></span>           | <span data-ttu-id="d3634-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3634-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="d3634-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-246">System-Flags</span></span>           | <span data-ttu-id="d3634-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3634-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="d3634-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3634-248">Classes used in</span></span>        | [<span data-ttu-id="d3634-249">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d3634-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="d3634-250">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="d3634-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3634-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3634-251">Windows Server 2012</span></span>



| <span data-ttu-id="d3634-252">進入</span><span class="sxs-lookup"><span data-stu-id="d3634-252">Entry</span></span> | <span data-ttu-id="d3634-253">值</span><span class="sxs-lookup"><span data-stu-id="d3634-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d3634-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3634-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="d3634-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3634-256">System-Only</span></span>            | <span data-ttu-id="d3634-257">否</span><span class="sxs-lookup"><span data-stu-id="d3634-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d3634-258">Is-Single-Valued</span></span>       | <span data-ttu-id="d3634-259">對</span><span class="sxs-lookup"><span data-stu-id="d3634-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="d3634-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d3634-260">Is Indexed</span></span>             | <span data-ttu-id="d3634-261">否</span><span class="sxs-lookup"><span data-stu-id="d3634-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d3634-262">In Global Catalog</span></span>      | <span data-ttu-id="d3634-263">否</span><span class="sxs-lookup"><span data-stu-id="d3634-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="d3634-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d3634-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3634-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d3634-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="d3634-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3634-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3634-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="d3634-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-268">Search-Flags</span></span>           | <span data-ttu-id="d3634-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3634-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="d3634-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3634-270">System-Flags</span></span>           | <span data-ttu-id="d3634-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3634-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="d3634-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d3634-272">Classes used in</span></span>        | [<span data-ttu-id="d3634-273">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="d3634-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="d3634-274">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="d3634-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





