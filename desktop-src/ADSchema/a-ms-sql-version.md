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
# <a name="ms-sql-version-attribute"></a><span data-ttu-id="72196-105">TRANSACT-SQL-Version 屬性</span><span class="sxs-lookup"><span data-stu-id="72196-105">MS-SQL-Version attribute</span></span>

<span data-ttu-id="72196-106">SQL Server 目前實例的版本。</span><span class="sxs-lookup"><span data-stu-id="72196-106">The version for the current instance of SQL Server.</span></span>



| <span data-ttu-id="72196-107">進入</span><span class="sxs-lookup"><span data-stu-id="72196-107">Entry</span></span> | <span data-ttu-id="72196-108">值</span><span class="sxs-lookup"><span data-stu-id="72196-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="72196-109">CN</span><span class="sxs-lookup"><span data-stu-id="72196-109">CN</span></span>                | <span data-ttu-id="72196-110">MS-SQL-版本</span><span class="sxs-lookup"><span data-stu-id="72196-110">MS-SQL-Version</span></span>                              |
| <span data-ttu-id="72196-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="72196-111">Ldap-Display-Name</span></span> | <span data-ttu-id="72196-112">mS-SQL-版本</span><span class="sxs-lookup"><span data-stu-id="72196-112">mS-SQL-Version</span></span>                              |
| <span data-ttu-id="72196-113">大小</span><span class="sxs-lookup"><span data-stu-id="72196-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="72196-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="72196-114">Update Privilege</span></span>  | <span data-ttu-id="72196-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="72196-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="72196-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="72196-116">Update Frequency</span></span>  | <span data-ttu-id="72196-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="72196-117">At system setup.</span></span>                            |
| <span data-ttu-id="72196-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72196-118">Attribute-Id</span></span>      | <span data-ttu-id="72196-119">1.2.840.113556.1.4.1388</span><span class="sxs-lookup"><span data-stu-id="72196-119">1.2.840.113556.1.4.1388</span></span>                     |
| <span data-ttu-id="72196-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="72196-120">System-Id-Guid</span></span>    | <span data-ttu-id="72196-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="72196-121">c07cc1d0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="72196-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="72196-122">Syntax</span></span>            | [<span data-ttu-id="72196-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="72196-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="72196-124">實作</span><span class="sxs-lookup"><span data-stu-id="72196-124">Implementations</span></span>

-   [<span data-ttu-id="72196-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72196-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72196-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72196-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72196-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72196-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72196-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72196-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72196-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72196-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72196-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72196-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72196-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72196-131">Windows 2000 Server</span></span>



| <span data-ttu-id="72196-132">進入</span><span class="sxs-lookup"><span data-stu-id="72196-132">Entry</span></span> | <span data-ttu-id="72196-133">值</span><span class="sxs-lookup"><span data-stu-id="72196-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72196-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72196-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72196-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="72196-136">System-Only</span></span>            | <span data-ttu-id="72196-137">否</span><span class="sxs-lookup"><span data-stu-id="72196-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="72196-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72196-138">Is-Single-Valued</span></span>       | <span data-ttu-id="72196-139">對</span><span class="sxs-lookup"><span data-stu-id="72196-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72196-140">Is Indexed</span></span>             | <span data-ttu-id="72196-141">對</span><span class="sxs-lookup"><span data-stu-id="72196-141">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72196-142">In Global Catalog</span></span>      | <span data-ttu-id="72196-143">對</span><span class="sxs-lookup"><span data-stu-id="72196-143">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72196-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="72196-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72196-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="72196-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72196-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72196-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-148">Search-Flags</span></span>           | <span data-ttu-id="72196-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72196-149">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="72196-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-150">System-Flags</span></span>           | <span data-ttu-id="72196-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72196-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="72196-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72196-152">Classes used in</span></span>        | [<span data-ttu-id="72196-153">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="72196-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="72196-154">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="72196-154">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72196-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72196-155">Windows Server 2003</span></span>



| <span data-ttu-id="72196-156">進入</span><span class="sxs-lookup"><span data-stu-id="72196-156">Entry</span></span> | <span data-ttu-id="72196-157">值</span><span class="sxs-lookup"><span data-stu-id="72196-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72196-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72196-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72196-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="72196-160">System-Only</span></span>            | <span data-ttu-id="72196-161">否</span><span class="sxs-lookup"><span data-stu-id="72196-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="72196-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72196-162">Is-Single-Valued</span></span>       | <span data-ttu-id="72196-163">對</span><span class="sxs-lookup"><span data-stu-id="72196-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72196-164">Is Indexed</span></span>             | <span data-ttu-id="72196-165">對</span><span class="sxs-lookup"><span data-stu-id="72196-165">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72196-166">In Global Catalog</span></span>      | <span data-ttu-id="72196-167">對</span><span class="sxs-lookup"><span data-stu-id="72196-167">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72196-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="72196-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72196-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="72196-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72196-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72196-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-172">Search-Flags</span></span>           | <span data-ttu-id="72196-173">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72196-173">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="72196-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-174">System-Flags</span></span>           | <span data-ttu-id="72196-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72196-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="72196-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72196-176">Classes used in</span></span>        | [<span data-ttu-id="72196-177">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="72196-177">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="72196-178">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="72196-178">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72196-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72196-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72196-180">進入</span><span class="sxs-lookup"><span data-stu-id="72196-180">Entry</span></span> | <span data-ttu-id="72196-181">值</span><span class="sxs-lookup"><span data-stu-id="72196-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72196-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72196-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72196-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="72196-184">System-Only</span></span>            | <span data-ttu-id="72196-185">否</span><span class="sxs-lookup"><span data-stu-id="72196-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="72196-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72196-186">Is-Single-Valued</span></span>       | <span data-ttu-id="72196-187">對</span><span class="sxs-lookup"><span data-stu-id="72196-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72196-188">Is Indexed</span></span>             | <span data-ttu-id="72196-189">對</span><span class="sxs-lookup"><span data-stu-id="72196-189">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72196-190">In Global Catalog</span></span>      | <span data-ttu-id="72196-191">對</span><span class="sxs-lookup"><span data-stu-id="72196-191">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72196-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="72196-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72196-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="72196-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72196-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72196-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-196">Search-Flags</span></span>           | <span data-ttu-id="72196-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72196-197">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="72196-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-198">System-Flags</span></span>           | <span data-ttu-id="72196-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72196-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="72196-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72196-200">Classes used in</span></span>        | [<span data-ttu-id="72196-201">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="72196-201">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="72196-202">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="72196-202">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72196-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72196-203">Windows Server 2008</span></span>



| <span data-ttu-id="72196-204">進入</span><span class="sxs-lookup"><span data-stu-id="72196-204">Entry</span></span> | <span data-ttu-id="72196-205">值</span><span class="sxs-lookup"><span data-stu-id="72196-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72196-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72196-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72196-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="72196-208">System-Only</span></span>            | <span data-ttu-id="72196-209">否</span><span class="sxs-lookup"><span data-stu-id="72196-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="72196-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72196-210">Is-Single-Valued</span></span>       | <span data-ttu-id="72196-211">對</span><span class="sxs-lookup"><span data-stu-id="72196-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72196-212">Is Indexed</span></span>             | <span data-ttu-id="72196-213">對</span><span class="sxs-lookup"><span data-stu-id="72196-213">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72196-214">In Global Catalog</span></span>      | <span data-ttu-id="72196-215">對</span><span class="sxs-lookup"><span data-stu-id="72196-215">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72196-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="72196-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72196-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="72196-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72196-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72196-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-220">Search-Flags</span></span>           | <span data-ttu-id="72196-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72196-221">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="72196-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-222">System-Flags</span></span>           | <span data-ttu-id="72196-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72196-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="72196-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72196-224">Classes used in</span></span>        | [<span data-ttu-id="72196-225">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="72196-225">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="72196-226">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="72196-226">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72196-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72196-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72196-228">進入</span><span class="sxs-lookup"><span data-stu-id="72196-228">Entry</span></span> | <span data-ttu-id="72196-229">值</span><span class="sxs-lookup"><span data-stu-id="72196-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72196-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72196-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72196-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="72196-232">System-Only</span></span>            | <span data-ttu-id="72196-233">否</span><span class="sxs-lookup"><span data-stu-id="72196-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="72196-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72196-234">Is-Single-Valued</span></span>       | <span data-ttu-id="72196-235">對</span><span class="sxs-lookup"><span data-stu-id="72196-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72196-236">Is Indexed</span></span>             | <span data-ttu-id="72196-237">對</span><span class="sxs-lookup"><span data-stu-id="72196-237">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72196-238">In Global Catalog</span></span>      | <span data-ttu-id="72196-239">對</span><span class="sxs-lookup"><span data-stu-id="72196-239">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72196-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="72196-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72196-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="72196-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72196-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72196-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-244">Search-Flags</span></span>           | <span data-ttu-id="72196-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72196-245">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="72196-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-246">System-Flags</span></span>           | <span data-ttu-id="72196-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72196-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="72196-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72196-248">Classes used in</span></span>        | [<span data-ttu-id="72196-249">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="72196-249">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="72196-250">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="72196-250">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72196-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72196-251">Windows Server 2012</span></span>



| <span data-ttu-id="72196-252">進入</span><span class="sxs-lookup"><span data-stu-id="72196-252">Entry</span></span> | <span data-ttu-id="72196-253">值</span><span class="sxs-lookup"><span data-stu-id="72196-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72196-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="72196-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72196-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="72196-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="72196-256">System-Only</span></span>            | <span data-ttu-id="72196-257">否</span><span class="sxs-lookup"><span data-stu-id="72196-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="72196-258">是-單一值</span><span class="sxs-lookup"><span data-stu-id="72196-258">Is-Single-Valued</span></span>       | <span data-ttu-id="72196-259">對</span><span class="sxs-lookup"><span data-stu-id="72196-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-260">已編制索引</span><span class="sxs-lookup"><span data-stu-id="72196-260">Is Indexed</span></span>             | <span data-ttu-id="72196-261">對</span><span class="sxs-lookup"><span data-stu-id="72196-261">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-262">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="72196-262">In Global Catalog</span></span>      | <span data-ttu-id="72196-263">對</span><span class="sxs-lookup"><span data-stu-id="72196-263">True</span></span>                                                                                                                          |
| <span data-ttu-id="72196-264">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="72196-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="72196-265">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="72196-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="72196-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72196-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72196-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="72196-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-268">Search-Flags</span></span>           | <span data-ttu-id="72196-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72196-269">0x00000001</span></span>                                                                                                                    |
| <span data-ttu-id="72196-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72196-270">System-Flags</span></span>           | <span data-ttu-id="72196-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72196-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="72196-272">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="72196-272">Classes used in</span></span>        | [<span data-ttu-id="72196-273">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="72196-273">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> [<span data-ttu-id="72196-274">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="72196-274">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





