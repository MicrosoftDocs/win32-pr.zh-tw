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
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="9dfc7-105">>registeredowner 屬性</span><span class="sxs-lookup"><span data-stu-id="9dfc7-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="9dfc7-106">SQL Server 目前實例的註冊擁有者。</span><span class="sxs-lookup"><span data-stu-id="9dfc7-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="9dfc7-107">進入</span><span class="sxs-lookup"><span data-stu-id="9dfc7-107">Entry</span></span> | <span data-ttu-id="9dfc7-108">值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9dfc7-109">CN</span><span class="sxs-lookup"><span data-stu-id="9dfc7-109">CN</span></span>                | <span data-ttu-id="9dfc7-110">>registeredowner</span><span class="sxs-lookup"><span data-stu-id="9dfc7-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="9dfc7-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9dfc7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9dfc7-112">>registeredowner</span><span class="sxs-lookup"><span data-stu-id="9dfc7-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="9dfc7-113">大小</span><span class="sxs-lookup"><span data-stu-id="9dfc7-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9dfc7-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9dfc7-114">Update Privilege</span></span>  | <span data-ttu-id="9dfc7-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="9dfc7-115">Domain administrator</span></span>                        |
| <span data-ttu-id="9dfc7-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9dfc7-116">Update Frequency</span></span>  | <span data-ttu-id="9dfc7-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="9dfc7-117">At system setup.</span></span>                            |
| <span data-ttu-id="9dfc7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9dfc7-118">Attribute-Id</span></span>      | <span data-ttu-id="9dfc7-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="9dfc7-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="9dfc7-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9dfc7-120">System-Id-Guid</span></span>    | <span data-ttu-id="9dfc7-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9dfc7-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="9dfc7-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dfc7-122">Syntax</span></span>            | [<span data-ttu-id="9dfc7-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9dfc7-124">實作</span><span class="sxs-lookup"><span data-stu-id="9dfc7-124">Implementations</span></span>

-   [<span data-ttu-id="9dfc7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9dfc7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9dfc7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9dfc7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9dfc7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9dfc7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9dfc7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9dfc7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9dfc7-132">進入</span><span class="sxs-lookup"><span data-stu-id="9dfc7-132">Entry</span></span> | <span data-ttu-id="9dfc7-133">值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfc7-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfc7-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfc7-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfc7-136">System-Only</span></span>            | <span data-ttu-id="9dfc7-137">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfc7-139">對</span><span class="sxs-lookup"><span data-stu-id="9dfc7-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="9dfc7-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfc7-140">Is Indexed</span></span>             | <span data-ttu-id="9dfc7-141">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfc7-142">In Global Catalog</span></span>      | <span data-ttu-id="9dfc7-143">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfc7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfc7-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfc7-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9dfc7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfc7-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfc7-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-148">Search-Flags</span></span>           | <span data-ttu-id="9dfc7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfc7-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-150">System-Flags</span></span>           | <span data-ttu-id="9dfc7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfc7-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfc7-152">Classes used in</span></span>        | [<span data-ttu-id="9dfc7-153">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9dfc7-154">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9dfc7-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9dfc7-155">Windows Server 2003</span></span>



| <span data-ttu-id="9dfc7-156">進入</span><span class="sxs-lookup"><span data-stu-id="9dfc7-156">Entry</span></span> | <span data-ttu-id="9dfc7-157">值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfc7-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfc7-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfc7-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfc7-160">System-Only</span></span>            | <span data-ttu-id="9dfc7-161">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-162">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfc7-163">對</span><span class="sxs-lookup"><span data-stu-id="9dfc7-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="9dfc7-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfc7-164">Is Indexed</span></span>             | <span data-ttu-id="9dfc7-165">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfc7-166">In Global Catalog</span></span>      | <span data-ttu-id="9dfc7-167">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfc7-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfc7-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfc7-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9dfc7-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfc7-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfc7-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-172">Search-Flags</span></span>           | <span data-ttu-id="9dfc7-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfc7-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-174">System-Flags</span></span>           | <span data-ttu-id="9dfc7-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfc7-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfc7-176">Classes used in</span></span>        | [<span data-ttu-id="9dfc7-177">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9dfc7-178">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9dfc7-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9dfc7-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9dfc7-180">進入</span><span class="sxs-lookup"><span data-stu-id="9dfc7-180">Entry</span></span> | <span data-ttu-id="9dfc7-181">值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfc7-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfc7-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfc7-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfc7-184">System-Only</span></span>            | <span data-ttu-id="9dfc7-185">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfc7-187">對</span><span class="sxs-lookup"><span data-stu-id="9dfc7-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="9dfc7-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfc7-188">Is Indexed</span></span>             | <span data-ttu-id="9dfc7-189">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfc7-190">In Global Catalog</span></span>      | <span data-ttu-id="9dfc7-191">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfc7-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfc7-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfc7-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9dfc7-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfc7-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfc7-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-196">Search-Flags</span></span>           | <span data-ttu-id="9dfc7-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfc7-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-198">System-Flags</span></span>           | <span data-ttu-id="9dfc7-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfc7-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfc7-200">Classes used in</span></span>        | [<span data-ttu-id="9dfc7-201">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9dfc7-202">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9dfc7-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dfc7-203">Windows Server 2008</span></span>



| <span data-ttu-id="9dfc7-204">進入</span><span class="sxs-lookup"><span data-stu-id="9dfc7-204">Entry</span></span> | <span data-ttu-id="9dfc7-205">值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfc7-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfc7-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfc7-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfc7-208">System-Only</span></span>            | <span data-ttu-id="9dfc7-209">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-210">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfc7-211">對</span><span class="sxs-lookup"><span data-stu-id="9dfc7-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="9dfc7-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfc7-212">Is Indexed</span></span>             | <span data-ttu-id="9dfc7-213">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfc7-214">In Global Catalog</span></span>      | <span data-ttu-id="9dfc7-215">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfc7-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfc7-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfc7-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9dfc7-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfc7-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfc7-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-220">Search-Flags</span></span>           | <span data-ttu-id="9dfc7-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfc7-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-222">System-Flags</span></span>           | <span data-ttu-id="9dfc7-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfc7-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfc7-224">Classes used in</span></span>        | [<span data-ttu-id="9dfc7-225">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9dfc7-226">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9dfc7-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9dfc7-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9dfc7-228">進入</span><span class="sxs-lookup"><span data-stu-id="9dfc7-228">Entry</span></span> | <span data-ttu-id="9dfc7-229">值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfc7-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfc7-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfc7-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfc7-232">System-Only</span></span>            | <span data-ttu-id="9dfc7-233">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-234">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfc7-235">對</span><span class="sxs-lookup"><span data-stu-id="9dfc7-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="9dfc7-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfc7-236">Is Indexed</span></span>             | <span data-ttu-id="9dfc7-237">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfc7-238">In Global Catalog</span></span>      | <span data-ttu-id="9dfc7-239">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfc7-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfc7-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfc7-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9dfc7-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfc7-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfc7-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-244">Search-Flags</span></span>           | <span data-ttu-id="9dfc7-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfc7-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-246">System-Flags</span></span>           | <span data-ttu-id="9dfc7-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfc7-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfc7-248">Classes used in</span></span>        | [<span data-ttu-id="9dfc7-249">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9dfc7-250">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9dfc7-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9dfc7-251">Windows Server 2012</span></span>



| <span data-ttu-id="9dfc7-252">進入</span><span class="sxs-lookup"><span data-stu-id="9dfc7-252">Entry</span></span> | <span data-ttu-id="9dfc7-253">值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfc7-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9dfc7-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9dfc7-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="9dfc7-256">System-Only</span></span>            | <span data-ttu-id="9dfc7-257">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9dfc7-258">Is-Single-Valued</span></span>       | <span data-ttu-id="9dfc7-259">對</span><span class="sxs-lookup"><span data-stu-id="9dfc7-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="9dfc7-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9dfc7-260">Is Indexed</span></span>             | <span data-ttu-id="9dfc7-261">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9dfc7-262">In Global Catalog</span></span>      | <span data-ttu-id="9dfc7-263">否</span><span class="sxs-lookup"><span data-stu-id="9dfc7-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="9dfc7-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9dfc7-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="9dfc7-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9dfc7-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="9dfc7-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9dfc7-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9dfc7-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="9dfc7-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-268">Search-Flags</span></span>           | <span data-ttu-id="9dfc7-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dfc7-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9dfc7-270">System-Flags</span></span>           | <span data-ttu-id="9dfc7-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dfc7-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="9dfc7-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9dfc7-272">Classes used in</span></span>        | [<span data-ttu-id="9dfc7-273">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="9dfc7-274">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="9dfc7-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





