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
# <a name="ms-sql-version-attribute"></a><span data-ttu-id="14ced-105">TRANSACT-SQL-Version 屬性</span><span class="sxs-lookup"><span data-stu-id="14ced-105">MS-SQL-Version attribute</span></span>

<span data-ttu-id="14ced-106">SQL Server 目前實例的版本。</span><span class="sxs-lookup"><span data-stu-id="14ced-106">The version for the current instance of SQL Server.</span></span>



| <span data-ttu-id="14ced-107">進入</span><span class="sxs-lookup"><span data-stu-id="14ced-107">Entry</span></span> | <span data-ttu-id="14ced-108">值</span><span class="sxs-lookup"><span data-stu-id="14ced-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="14ced-109">CN</span><span class="sxs-lookup"><span data-stu-id="14ced-109">CN</span></span>                | <span data-ttu-id="14ced-110">MS-SQL-版本</span><span class="sxs-lookup"><span data-stu-id="14ced-110">MS-SQL-Version</span></span>                              |
| <span data-ttu-id="14ced-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="14ced-111">Ldap-Display-Name</span></span> | <span data-ttu-id="14ced-112">mS-SQL-版本</span><span class="sxs-lookup"><span data-stu-id="14ced-112">mS-SQL-Version</span></span>                              |
| <span data-ttu-id="14ced-113">大小</span><span class="sxs-lookup"><span data-stu-id="14ced-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="14ced-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="14ced-114">Update Privilege</span></span>  | <span data-ttu-id="14ced-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="14ced-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="14ced-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="14ced-116">Update Frequency</span></span>  | <span data-ttu-id="14ced-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="14ced-117">At system setup.</span></span>                            |
| <span data-ttu-id="14ced-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14ced-118">Attribute-Id</span></span>      | <span data-ttu-id="14ced-119">1.2.840.113556.1.4.1388</span><span class="sxs-lookup"><span data-stu-id="14ced-119">1.2.840.113556.1.4.1388</span></span>                     |
| <span data-ttu-id="14ced-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="14ced-120">System-Id-Guid</span></span>    | <span data-ttu-id="14ced-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="14ced-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="14ced-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="14ced-122">Syntax</span></span>            | [<span data-ttu-id="14ced-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="14ced-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="14ced-124">實作</span><span class="sxs-lookup"><span data-stu-id="14ced-124">Implementations</span></span>

-   [<span data-ttu-id="14ced-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14ced-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14ced-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14ced-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14ced-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14ced-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14ced-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14ced-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14ced-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14ced-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14ced-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14ced-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14ced-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14ced-131">Windows 2000 Server</span></span>



| <span data-ttu-id="14ced-132">進入</span><span class="sxs-lookup"><span data-stu-id="14ced-132">Entry</span></span> | <span data-ttu-id="14ced-133">值</span><span class="sxs-lookup"><span data-stu-id="14ced-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ced-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14ced-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14ced-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="14ced-136">System-Only</span></span>            | <span data-ttu-id="14ced-137">否</span><span class="sxs-lookup"><span data-stu-id="14ced-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="14ced-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14ced-138">Is-Single-Valued</span></span>       | <span data-ttu-id="14ced-139">對</span><span class="sxs-lookup"><span data-stu-id="14ced-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14ced-140">Is Indexed</span></span>             | <span data-ttu-id="14ced-141">對</span><span class="sxs-lookup"><span data-stu-id="14ced-141">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14ced-142">In Global Catalog</span></span>      | <span data-ttu-id="14ced-143">對</span><span class="sxs-lookup"><span data-stu-id="14ced-143">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14ced-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="14ced-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14ced-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="14ced-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14ced-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14ced-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-148">Search-Flags</span></span>           | <span data-ttu-id="14ced-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="14ced-149">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-150">System-Flags</span></span>           | <span data-ttu-id="14ced-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14ced-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14ced-152">Classes used in</span></span>        | [<span data-ttu-id="14ced-153">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="14ced-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="14ced-154">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="14ced-154">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14ced-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14ced-155">Windows Server 2003</span></span>



| <span data-ttu-id="14ced-156">進入</span><span class="sxs-lookup"><span data-stu-id="14ced-156">Entry</span></span> | <span data-ttu-id="14ced-157">值</span><span class="sxs-lookup"><span data-stu-id="14ced-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ced-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14ced-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14ced-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="14ced-160">System-Only</span></span>            | <span data-ttu-id="14ced-161">否</span><span class="sxs-lookup"><span data-stu-id="14ced-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="14ced-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14ced-162">Is-Single-Valued</span></span>       | <span data-ttu-id="14ced-163">對</span><span class="sxs-lookup"><span data-stu-id="14ced-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14ced-164">Is Indexed</span></span>             | <span data-ttu-id="14ced-165">對</span><span class="sxs-lookup"><span data-stu-id="14ced-165">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14ced-166">In Global Catalog</span></span>      | <span data-ttu-id="14ced-167">對</span><span class="sxs-lookup"><span data-stu-id="14ced-167">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14ced-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="14ced-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14ced-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="14ced-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14ced-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14ced-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-172">Search-Flags</span></span>           | <span data-ttu-id="14ced-173">0x00000001</span><span class="sxs-lookup"><span data-stu-id="14ced-173">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-174">System-Flags</span></span>           | <span data-ttu-id="14ced-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14ced-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14ced-176">Classes used in</span></span>        | [<span data-ttu-id="14ced-177">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="14ced-177">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="14ced-178">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="14ced-178">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14ced-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14ced-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14ced-180">進入</span><span class="sxs-lookup"><span data-stu-id="14ced-180">Entry</span></span> | <span data-ttu-id="14ced-181">值</span><span class="sxs-lookup"><span data-stu-id="14ced-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ced-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14ced-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14ced-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="14ced-184">System-Only</span></span>            | <span data-ttu-id="14ced-185">否</span><span class="sxs-lookup"><span data-stu-id="14ced-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="14ced-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14ced-186">Is-Single-Valued</span></span>       | <span data-ttu-id="14ced-187">對</span><span class="sxs-lookup"><span data-stu-id="14ced-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14ced-188">Is Indexed</span></span>             | <span data-ttu-id="14ced-189">對</span><span class="sxs-lookup"><span data-stu-id="14ced-189">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14ced-190">In Global Catalog</span></span>      | <span data-ttu-id="14ced-191">對</span><span class="sxs-lookup"><span data-stu-id="14ced-191">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14ced-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="14ced-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14ced-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="14ced-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14ced-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14ced-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-196">Search-Flags</span></span>           | <span data-ttu-id="14ced-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="14ced-197">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-198">System-Flags</span></span>           | <span data-ttu-id="14ced-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14ced-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14ced-200">Classes used in</span></span>        | [<span data-ttu-id="14ced-201">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="14ced-201">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="14ced-202">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="14ced-202">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14ced-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14ced-203">Windows Server 2008</span></span>



| <span data-ttu-id="14ced-204">進入</span><span class="sxs-lookup"><span data-stu-id="14ced-204">Entry</span></span> | <span data-ttu-id="14ced-205">值</span><span class="sxs-lookup"><span data-stu-id="14ced-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ced-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14ced-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14ced-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="14ced-208">System-Only</span></span>            | <span data-ttu-id="14ced-209">否</span><span class="sxs-lookup"><span data-stu-id="14ced-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="14ced-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14ced-210">Is-Single-Valued</span></span>       | <span data-ttu-id="14ced-211">對</span><span class="sxs-lookup"><span data-stu-id="14ced-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14ced-212">Is Indexed</span></span>             | <span data-ttu-id="14ced-213">對</span><span class="sxs-lookup"><span data-stu-id="14ced-213">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14ced-214">In Global Catalog</span></span>      | <span data-ttu-id="14ced-215">對</span><span class="sxs-lookup"><span data-stu-id="14ced-215">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14ced-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="14ced-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14ced-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="14ced-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14ced-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14ced-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-220">Search-Flags</span></span>           | <span data-ttu-id="14ced-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="14ced-221">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-222">System-Flags</span></span>           | <span data-ttu-id="14ced-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14ced-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14ced-224">Classes used in</span></span>        | [<span data-ttu-id="14ced-225">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="14ced-225">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="14ced-226">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="14ced-226">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14ced-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14ced-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14ced-228">進入</span><span class="sxs-lookup"><span data-stu-id="14ced-228">Entry</span></span> | <span data-ttu-id="14ced-229">值</span><span class="sxs-lookup"><span data-stu-id="14ced-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ced-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14ced-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14ced-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="14ced-232">System-Only</span></span>            | <span data-ttu-id="14ced-233">否</span><span class="sxs-lookup"><span data-stu-id="14ced-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="14ced-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14ced-234">Is-Single-Valued</span></span>       | <span data-ttu-id="14ced-235">對</span><span class="sxs-lookup"><span data-stu-id="14ced-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14ced-236">Is Indexed</span></span>             | <span data-ttu-id="14ced-237">對</span><span class="sxs-lookup"><span data-stu-id="14ced-237">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14ced-238">In Global Catalog</span></span>      | <span data-ttu-id="14ced-239">對</span><span class="sxs-lookup"><span data-stu-id="14ced-239">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14ced-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="14ced-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14ced-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="14ced-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14ced-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14ced-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-244">Search-Flags</span></span>           | <span data-ttu-id="14ced-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="14ced-245">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-246">System-Flags</span></span>           | <span data-ttu-id="14ced-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14ced-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14ced-248">Classes used in</span></span>        | [<span data-ttu-id="14ced-249">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="14ced-249">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="14ced-250">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="14ced-250">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14ced-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14ced-251">Windows Server 2012</span></span>



| <span data-ttu-id="14ced-252">進入</span><span class="sxs-lookup"><span data-stu-id="14ced-252">Entry</span></span> | <span data-ttu-id="14ced-253">值</span><span class="sxs-lookup"><span data-stu-id="14ced-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ced-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="14ced-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14ced-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="14ced-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="14ced-256">System-Only</span></span>            | <span data-ttu-id="14ced-257">否</span><span class="sxs-lookup"><span data-stu-id="14ced-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="14ced-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="14ced-258">Is-Single-Valued</span></span>       | <span data-ttu-id="14ced-259">對</span><span class="sxs-lookup"><span data-stu-id="14ced-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="14ced-260">Is Indexed</span></span>             | <span data-ttu-id="14ced-261">對</span><span class="sxs-lookup"><span data-stu-id="14ced-261">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="14ced-262">In Global Catalog</span></span>      | <span data-ttu-id="14ced-263">對</span><span class="sxs-lookup"><span data-stu-id="14ced-263">True</span></span>                                                                                                                          |
| <span data-ttu-id="14ced-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="14ced-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="14ced-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="14ced-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="14ced-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14ced-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14ced-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="14ced-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-268">Search-Flags</span></span>           | <span data-ttu-id="14ced-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="14ced-269">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14ced-270">System-Flags</span></span>           | <span data-ttu-id="14ced-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14ced-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="14ced-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="14ced-272">Classes used in</span></span>        | [<span data-ttu-id="14ced-273">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="14ced-273">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="14ced-274">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="14ced-274">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





