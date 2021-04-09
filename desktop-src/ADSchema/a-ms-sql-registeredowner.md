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
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="4c50f-105">>registeredowner 屬性</span><span class="sxs-lookup"><span data-stu-id="4c50f-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="4c50f-106">SQL Server 目前實例的註冊擁有者。</span><span class="sxs-lookup"><span data-stu-id="4c50f-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="4c50f-107">進入</span><span class="sxs-lookup"><span data-stu-id="4c50f-107">Entry</span></span> | <span data-ttu-id="4c50f-108">值</span><span class="sxs-lookup"><span data-stu-id="4c50f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4c50f-109">CN</span><span class="sxs-lookup"><span data-stu-id="4c50f-109">CN</span></span>                | <span data-ttu-id="4c50f-110">>registeredowner</span><span class="sxs-lookup"><span data-stu-id="4c50f-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="4c50f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4c50f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4c50f-112">>registeredowner</span><span class="sxs-lookup"><span data-stu-id="4c50f-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="4c50f-113">大小</span><span class="sxs-lookup"><span data-stu-id="4c50f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="4c50f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4c50f-114">Update Privilege</span></span>  | <span data-ttu-id="4c50f-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="4c50f-115">Domain administrator</span></span>                        |
| <span data-ttu-id="4c50f-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4c50f-116">Update Frequency</span></span>  | <span data-ttu-id="4c50f-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="4c50f-117">At system setup.</span></span>                            |
| <span data-ttu-id="4c50f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4c50f-118">Attribute-Id</span></span>      | <span data-ttu-id="4c50f-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="4c50f-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="4c50f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4c50f-120">System-Id-Guid</span></span>    | <span data-ttu-id="4c50f-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="4c50f-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="4c50f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c50f-122">Syntax</span></span>            | [<span data-ttu-id="4c50f-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4c50f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4c50f-124">實作</span><span class="sxs-lookup"><span data-stu-id="4c50f-124">Implementations</span></span>

-   [<span data-ttu-id="4c50f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4c50f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4c50f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4c50f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4c50f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4c50f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4c50f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4c50f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4c50f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4c50f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4c50f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4c50f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4c50f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c50f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4c50f-132">進入</span><span class="sxs-lookup"><span data-stu-id="4c50f-132">Entry</span></span> | <span data-ttu-id="4c50f-133">值</span><span class="sxs-lookup"><span data-stu-id="4c50f-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c50f-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c50f-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c50f-136">System-Only</span></span>            | <span data-ttu-id="4c50f-137">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c50f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4c50f-139">對</span><span class="sxs-lookup"><span data-stu-id="4c50f-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="4c50f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c50f-140">Is Indexed</span></span>             | <span data-ttu-id="4c50f-141">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c50f-142">In Global Catalog</span></span>      | <span data-ttu-id="4c50f-143">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c50f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c50f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c50f-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="4c50f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c50f-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c50f-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-148">Search-Flags</span></span>           | <span data-ttu-id="4c50f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c50f-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-150">System-Flags</span></span>           | <span data-ttu-id="4c50f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c50f-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c50f-152">Classes used in</span></span>        | [<span data-ttu-id="4c50f-153">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4c50f-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="4c50f-154">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="4c50f-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4c50f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c50f-155">Windows Server 2003</span></span>



| <span data-ttu-id="4c50f-156">進入</span><span class="sxs-lookup"><span data-stu-id="4c50f-156">Entry</span></span> | <span data-ttu-id="4c50f-157">值</span><span class="sxs-lookup"><span data-stu-id="4c50f-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50f-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c50f-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c50f-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c50f-160">System-Only</span></span>            | <span data-ttu-id="4c50f-161">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c50f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4c50f-163">對</span><span class="sxs-lookup"><span data-stu-id="4c50f-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="4c50f-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c50f-164">Is Indexed</span></span>             | <span data-ttu-id="4c50f-165">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c50f-166">In Global Catalog</span></span>      | <span data-ttu-id="4c50f-167">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c50f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c50f-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c50f-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="4c50f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c50f-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c50f-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-172">Search-Flags</span></span>           | <span data-ttu-id="4c50f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c50f-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-174">System-Flags</span></span>           | <span data-ttu-id="4c50f-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c50f-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c50f-176">Classes used in</span></span>        | [<span data-ttu-id="4c50f-177">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4c50f-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="4c50f-178">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="4c50f-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4c50f-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4c50f-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4c50f-180">進入</span><span class="sxs-lookup"><span data-stu-id="4c50f-180">Entry</span></span> | <span data-ttu-id="4c50f-181">值</span><span class="sxs-lookup"><span data-stu-id="4c50f-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50f-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c50f-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c50f-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c50f-184">System-Only</span></span>            | <span data-ttu-id="4c50f-185">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c50f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4c50f-187">對</span><span class="sxs-lookup"><span data-stu-id="4c50f-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="4c50f-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c50f-188">Is Indexed</span></span>             | <span data-ttu-id="4c50f-189">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c50f-190">In Global Catalog</span></span>      | <span data-ttu-id="4c50f-191">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c50f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c50f-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c50f-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="4c50f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c50f-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c50f-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-196">Search-Flags</span></span>           | <span data-ttu-id="4c50f-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c50f-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-198">System-Flags</span></span>           | <span data-ttu-id="4c50f-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c50f-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c50f-200">Classes used in</span></span>        | [<span data-ttu-id="4c50f-201">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4c50f-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="4c50f-202">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="4c50f-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4c50f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c50f-203">Windows Server 2008</span></span>



| <span data-ttu-id="4c50f-204">進入</span><span class="sxs-lookup"><span data-stu-id="4c50f-204">Entry</span></span> | <span data-ttu-id="4c50f-205">值</span><span class="sxs-lookup"><span data-stu-id="4c50f-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50f-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c50f-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c50f-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c50f-208">System-Only</span></span>            | <span data-ttu-id="4c50f-209">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c50f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="4c50f-211">對</span><span class="sxs-lookup"><span data-stu-id="4c50f-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="4c50f-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c50f-212">Is Indexed</span></span>             | <span data-ttu-id="4c50f-213">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c50f-214">In Global Catalog</span></span>      | <span data-ttu-id="4c50f-215">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c50f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c50f-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c50f-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="4c50f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c50f-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c50f-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-220">Search-Flags</span></span>           | <span data-ttu-id="4c50f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c50f-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-222">System-Flags</span></span>           | <span data-ttu-id="4c50f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c50f-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c50f-224">Classes used in</span></span>        | [<span data-ttu-id="4c50f-225">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4c50f-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="4c50f-226">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="4c50f-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4c50f-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c50f-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4c50f-228">進入</span><span class="sxs-lookup"><span data-stu-id="4c50f-228">Entry</span></span> | <span data-ttu-id="4c50f-229">值</span><span class="sxs-lookup"><span data-stu-id="4c50f-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50f-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c50f-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c50f-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c50f-232">System-Only</span></span>            | <span data-ttu-id="4c50f-233">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c50f-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4c50f-235">對</span><span class="sxs-lookup"><span data-stu-id="4c50f-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="4c50f-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c50f-236">Is Indexed</span></span>             | <span data-ttu-id="4c50f-237">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c50f-238">In Global Catalog</span></span>      | <span data-ttu-id="4c50f-239">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c50f-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c50f-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c50f-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="4c50f-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c50f-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c50f-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-244">Search-Flags</span></span>           | <span data-ttu-id="4c50f-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c50f-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-246">System-Flags</span></span>           | <span data-ttu-id="4c50f-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c50f-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c50f-248">Classes used in</span></span>        | [<span data-ttu-id="4c50f-249">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4c50f-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="4c50f-250">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="4c50f-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4c50f-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c50f-251">Windows Server 2012</span></span>



| <span data-ttu-id="4c50f-252">進入</span><span class="sxs-lookup"><span data-stu-id="4c50f-252">Entry</span></span> | <span data-ttu-id="4c50f-253">值</span><span class="sxs-lookup"><span data-stu-id="4c50f-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50f-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c50f-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c50f-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="4c50f-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c50f-256">System-Only</span></span>            | <span data-ttu-id="4c50f-257">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c50f-258">Is-Single-Valued</span></span>       | <span data-ttu-id="4c50f-259">對</span><span class="sxs-lookup"><span data-stu-id="4c50f-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="4c50f-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c50f-260">Is Indexed</span></span>             | <span data-ttu-id="4c50f-261">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c50f-262">In Global Catalog</span></span>      | <span data-ttu-id="4c50f-263">否</span><span class="sxs-lookup"><span data-stu-id="4c50f-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="4c50f-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c50f-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c50f-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c50f-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="4c50f-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c50f-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c50f-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="4c50f-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-268">Search-Flags</span></span>           | <span data-ttu-id="4c50f-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c50f-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c50f-270">System-Flags</span></span>           | <span data-ttu-id="4c50f-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c50f-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="4c50f-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c50f-272">Classes used in</span></span>        | [<span data-ttu-id="4c50f-273">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4c50f-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="4c50f-274">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="4c50f-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





