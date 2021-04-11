---
title: TRANSACT-SQL-Version 屬性
description: SQL Server 目前實例的版本。
ms.assetid: 0003892c-906d-429b-bc98-bbc441b2d58b
ms.tgt_platform: multiple
keywords:
- MS-SQL-Version 屬性 AD 架構
- mS-SQL-Version 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a436a30311f5696d8ed63334b0cf796eb2767
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845543"
---
# <a name="ms-sql-version-attribute"></a><span data-ttu-id="ead66-105">TRANSACT-SQL-Version 屬性</span><span class="sxs-lookup"><span data-stu-id="ead66-105">MS-SQL-Version attribute</span></span>

<span data-ttu-id="ead66-106">SQL Server 目前實例的版本。</span><span class="sxs-lookup"><span data-stu-id="ead66-106">The version for the current instance of SQL Server.</span></span>



| <span data-ttu-id="ead66-107">進入</span><span class="sxs-lookup"><span data-stu-id="ead66-107">Entry</span></span> | <span data-ttu-id="ead66-108">值</span><span class="sxs-lookup"><span data-stu-id="ead66-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ead66-109">CN</span><span class="sxs-lookup"><span data-stu-id="ead66-109">CN</span></span>                | <span data-ttu-id="ead66-110">MS-SQL-版本</span><span class="sxs-lookup"><span data-stu-id="ead66-110">MS-SQL-Version</span></span>                              |
| <span data-ttu-id="ead66-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ead66-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ead66-112">mS-SQL-版本</span><span class="sxs-lookup"><span data-stu-id="ead66-112">mS-SQL-Version</span></span>                              |
| <span data-ttu-id="ead66-113">大小</span><span class="sxs-lookup"><span data-stu-id="ead66-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="ead66-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ead66-114">Update Privilege</span></span>  | <span data-ttu-id="ead66-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ead66-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="ead66-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ead66-116">Update Frequency</span></span>  | <span data-ttu-id="ead66-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="ead66-117">At system setup.</span></span>                            |
| <span data-ttu-id="ead66-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ead66-118">Attribute-Id</span></span>      | <span data-ttu-id="ead66-119">1.2.840.113556.1.4.1388</span><span class="sxs-lookup"><span data-stu-id="ead66-119">1.2.840.113556.1.4.1388</span></span>                     |
| <span data-ttu-id="ead66-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ead66-120">System-Id-Guid</span></span>    | <span data-ttu-id="ead66-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ead66-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="ead66-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead66-122">Syntax</span></span>            | [<span data-ttu-id="ead66-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ead66-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ead66-124">實作</span><span class="sxs-lookup"><span data-stu-id="ead66-124">Implementations</span></span>

-   [<span data-ttu-id="ead66-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ead66-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ead66-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ead66-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ead66-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ead66-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ead66-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ead66-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ead66-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ead66-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ead66-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ead66-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ead66-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ead66-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ead66-132">進入</span><span class="sxs-lookup"><span data-stu-id="ead66-132">Entry</span></span> | <span data-ttu-id="ead66-133">值</span><span class="sxs-lookup"><span data-stu-id="ead66-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead66-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ead66-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead66-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead66-136">System-Only</span></span>            | <span data-ttu-id="ead66-137">否</span><span class="sxs-lookup"><span data-stu-id="ead66-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="ead66-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ead66-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ead66-139">對</span><span class="sxs-lookup"><span data-stu-id="ead66-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ead66-140">Is Indexed</span></span>             | <span data-ttu-id="ead66-141">對</span><span class="sxs-lookup"><span data-stu-id="ead66-141">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ead66-142">In Global Catalog</span></span>      | <span data-ttu-id="ead66-143">對</span><span class="sxs-lookup"><span data-stu-id="ead66-143">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ead66-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead66-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ead66-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ead66-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead66-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead66-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-148">Search-Flags</span></span>           | <span data-ttu-id="ead66-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ead66-149">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-150">System-Flags</span></span>           | <span data-ttu-id="ead66-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead66-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ead66-152">Classes used in</span></span>        | [<span data-ttu-id="ead66-153">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="ead66-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="ead66-154">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ead66-154">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ead66-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ead66-155">Windows Server 2003</span></span>



| <span data-ttu-id="ead66-156">進入</span><span class="sxs-lookup"><span data-stu-id="ead66-156">Entry</span></span> | <span data-ttu-id="ead66-157">值</span><span class="sxs-lookup"><span data-stu-id="ead66-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead66-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ead66-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead66-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead66-160">System-Only</span></span>            | <span data-ttu-id="ead66-161">否</span><span class="sxs-lookup"><span data-stu-id="ead66-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="ead66-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ead66-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ead66-163">對</span><span class="sxs-lookup"><span data-stu-id="ead66-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ead66-164">Is Indexed</span></span>             | <span data-ttu-id="ead66-165">對</span><span class="sxs-lookup"><span data-stu-id="ead66-165">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ead66-166">In Global Catalog</span></span>      | <span data-ttu-id="ead66-167">對</span><span class="sxs-lookup"><span data-stu-id="ead66-167">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ead66-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead66-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ead66-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ead66-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead66-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead66-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-172">Search-Flags</span></span>           | <span data-ttu-id="ead66-173">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ead66-173">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-174">System-Flags</span></span>           | <span data-ttu-id="ead66-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead66-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ead66-176">Classes used in</span></span>        | [<span data-ttu-id="ead66-177">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="ead66-177">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="ead66-178">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ead66-178">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ead66-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ead66-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ead66-180">進入</span><span class="sxs-lookup"><span data-stu-id="ead66-180">Entry</span></span> | <span data-ttu-id="ead66-181">值</span><span class="sxs-lookup"><span data-stu-id="ead66-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead66-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ead66-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead66-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead66-184">System-Only</span></span>            | <span data-ttu-id="ead66-185">否</span><span class="sxs-lookup"><span data-stu-id="ead66-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="ead66-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ead66-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ead66-187">對</span><span class="sxs-lookup"><span data-stu-id="ead66-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ead66-188">Is Indexed</span></span>             | <span data-ttu-id="ead66-189">對</span><span class="sxs-lookup"><span data-stu-id="ead66-189">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ead66-190">In Global Catalog</span></span>      | <span data-ttu-id="ead66-191">對</span><span class="sxs-lookup"><span data-stu-id="ead66-191">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ead66-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead66-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ead66-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ead66-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead66-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead66-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-196">Search-Flags</span></span>           | <span data-ttu-id="ead66-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ead66-197">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-198">System-Flags</span></span>           | <span data-ttu-id="ead66-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead66-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ead66-200">Classes used in</span></span>        | [<span data-ttu-id="ead66-201">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="ead66-201">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="ead66-202">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ead66-202">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ead66-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ead66-203">Windows Server 2008</span></span>



| <span data-ttu-id="ead66-204">進入</span><span class="sxs-lookup"><span data-stu-id="ead66-204">Entry</span></span> | <span data-ttu-id="ead66-205">值</span><span class="sxs-lookup"><span data-stu-id="ead66-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead66-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ead66-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead66-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead66-208">System-Only</span></span>            | <span data-ttu-id="ead66-209">否</span><span class="sxs-lookup"><span data-stu-id="ead66-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="ead66-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ead66-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ead66-211">對</span><span class="sxs-lookup"><span data-stu-id="ead66-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ead66-212">Is Indexed</span></span>             | <span data-ttu-id="ead66-213">對</span><span class="sxs-lookup"><span data-stu-id="ead66-213">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ead66-214">In Global Catalog</span></span>      | <span data-ttu-id="ead66-215">對</span><span class="sxs-lookup"><span data-stu-id="ead66-215">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ead66-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead66-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ead66-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ead66-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead66-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead66-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-220">Search-Flags</span></span>           | <span data-ttu-id="ead66-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ead66-221">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-222">System-Flags</span></span>           | <span data-ttu-id="ead66-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead66-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ead66-224">Classes used in</span></span>        | [<span data-ttu-id="ead66-225">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="ead66-225">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="ead66-226">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ead66-226">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ead66-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ead66-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ead66-228">進入</span><span class="sxs-lookup"><span data-stu-id="ead66-228">Entry</span></span> | <span data-ttu-id="ead66-229">值</span><span class="sxs-lookup"><span data-stu-id="ead66-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead66-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ead66-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead66-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead66-232">System-Only</span></span>            | <span data-ttu-id="ead66-233">否</span><span class="sxs-lookup"><span data-stu-id="ead66-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="ead66-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ead66-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ead66-235">對</span><span class="sxs-lookup"><span data-stu-id="ead66-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ead66-236">Is Indexed</span></span>             | <span data-ttu-id="ead66-237">對</span><span class="sxs-lookup"><span data-stu-id="ead66-237">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ead66-238">In Global Catalog</span></span>      | <span data-ttu-id="ead66-239">對</span><span class="sxs-lookup"><span data-stu-id="ead66-239">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ead66-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead66-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ead66-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ead66-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead66-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead66-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-244">Search-Flags</span></span>           | <span data-ttu-id="ead66-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ead66-245">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-246">System-Flags</span></span>           | <span data-ttu-id="ead66-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead66-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ead66-248">Classes used in</span></span>        | [<span data-ttu-id="ead66-249">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="ead66-249">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="ead66-250">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ead66-250">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ead66-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ead66-251">Windows Server 2012</span></span>



| <span data-ttu-id="ead66-252">進入</span><span class="sxs-lookup"><span data-stu-id="ead66-252">Entry</span></span> | <span data-ttu-id="ead66-253">值</span><span class="sxs-lookup"><span data-stu-id="ead66-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead66-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ead66-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ead66-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="ead66-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ead66-256">System-Only</span></span>            | <span data-ttu-id="ead66-257">否</span><span class="sxs-lookup"><span data-stu-id="ead66-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="ead66-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ead66-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ead66-259">對</span><span class="sxs-lookup"><span data-stu-id="ead66-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ead66-260">Is Indexed</span></span>             | <span data-ttu-id="ead66-261">對</span><span class="sxs-lookup"><span data-stu-id="ead66-261">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ead66-262">In Global Catalog</span></span>      | <span data-ttu-id="ead66-263">對</span><span class="sxs-lookup"><span data-stu-id="ead66-263">True</span></span>                                                                                                                          |
| <span data-ttu-id="ead66-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ead66-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ead66-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ead66-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="ead66-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ead66-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ead66-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="ead66-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-268">Search-Flags</span></span>           | <span data-ttu-id="ead66-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ead66-269">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ead66-270">System-Flags</span></span>           | <span data-ttu-id="ead66-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ead66-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="ead66-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ead66-272">Classes used in</span></span>        | [<span data-ttu-id="ead66-273">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="ead66-273">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="ead66-274">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ead66-274">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





