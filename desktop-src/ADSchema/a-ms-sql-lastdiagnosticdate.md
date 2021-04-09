---
title: LastDiagnosticDate 屬性
description: DBCC checkdb 上次執行的日期。
ms.assetid: 7060e111-e4cb-4c5a-bce1-32712cbea00e
ms.tgt_platform: multiple
keywords:
- LastDiagnosticDate 屬性 AD 架構
- LastDiagnosticDate 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-LastDiagnosticDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f25b8322a9f83b96c0ab4883478e6c0ffa2f3b49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686836"
---
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="daf39-105">LastDiagnosticDate 屬性</span><span class="sxs-lookup"><span data-stu-id="daf39-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="daf39-106">DBCC checkdb 上次執行的日期。</span><span class="sxs-lookup"><span data-stu-id="daf39-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="daf39-107">進入</span><span class="sxs-lookup"><span data-stu-id="daf39-107">Entry</span></span> | <span data-ttu-id="daf39-108">值</span><span class="sxs-lookup"><span data-stu-id="daf39-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="daf39-109">CN</span><span class="sxs-lookup"><span data-stu-id="daf39-109">CN</span></span>                | <span data-ttu-id="daf39-110">LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="daf39-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="daf39-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="daf39-111">Ldap-Display-Name</span></span> | <span data-ttu-id="daf39-112">LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="daf39-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="daf39-113">大小</span><span class="sxs-lookup"><span data-stu-id="daf39-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="daf39-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="daf39-114">Update Privilege</span></span>  | <span data-ttu-id="daf39-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="daf39-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="daf39-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="daf39-116">Update Frequency</span></span>  | <span data-ttu-id="daf39-117">當 DBCC checkdb 執行時。</span><span class="sxs-lookup"><span data-stu-id="daf39-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="daf39-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="daf39-118">Attribute-Id</span></span>      | <span data-ttu-id="daf39-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="daf39-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="daf39-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="daf39-120">System-Id-Guid</span></span>    | <span data-ttu-id="daf39-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="daf39-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="daf39-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="daf39-122">Syntax</span></span>            | [<span data-ttu-id="daf39-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="daf39-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="daf39-124">實作</span><span class="sxs-lookup"><span data-stu-id="daf39-124">Implementations</span></span>

-   [<span data-ttu-id="daf39-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="daf39-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="daf39-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="daf39-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="daf39-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="daf39-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="daf39-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="daf39-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="daf39-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="daf39-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="daf39-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="daf39-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="daf39-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="daf39-131">Windows 2000 Server</span></span>



| <span data-ttu-id="daf39-132">進入</span><span class="sxs-lookup"><span data-stu-id="daf39-132">Entry</span></span> | <span data-ttu-id="daf39-133">值</span><span class="sxs-lookup"><span data-stu-id="daf39-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="daf39-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="daf39-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daf39-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="daf39-136">System-Only</span></span>            | <span data-ttu-id="daf39-137">否</span><span class="sxs-lookup"><span data-stu-id="daf39-137">False</span></span>                                                         |
| <span data-ttu-id="daf39-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="daf39-138">Is-Single-Valued</span></span>       | <span data-ttu-id="daf39-139">對</span><span class="sxs-lookup"><span data-stu-id="daf39-139">True</span></span>                                                          |
| <span data-ttu-id="daf39-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="daf39-140">Is Indexed</span></span>             | <span data-ttu-id="daf39-141">否</span><span class="sxs-lookup"><span data-stu-id="daf39-141">False</span></span>                                                         |
| <span data-ttu-id="daf39-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="daf39-142">In Global Catalog</span></span>      | <span data-ttu-id="daf39-143">否</span><span class="sxs-lookup"><span data-stu-id="daf39-143">False</span></span>                                                         |
| <span data-ttu-id="daf39-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="daf39-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="daf39-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="daf39-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="daf39-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daf39-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daf39-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-148">Search-Flags</span></span>           | <span data-ttu-id="daf39-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daf39-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="daf39-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-150">System-Flags</span></span>           | <span data-ttu-id="daf39-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daf39-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="daf39-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="daf39-152">Classes used in</span></span>        | [<span data-ttu-id="daf39-153">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="daf39-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="daf39-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="daf39-154">Windows Server 2003</span></span>



| <span data-ttu-id="daf39-155">進入</span><span class="sxs-lookup"><span data-stu-id="daf39-155">Entry</span></span> | <span data-ttu-id="daf39-156">值</span><span class="sxs-lookup"><span data-stu-id="daf39-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="daf39-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="daf39-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daf39-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="daf39-159">System-Only</span></span>            | <span data-ttu-id="daf39-160">否</span><span class="sxs-lookup"><span data-stu-id="daf39-160">False</span></span>                                                         |
| <span data-ttu-id="daf39-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="daf39-161">Is-Single-Valued</span></span>       | <span data-ttu-id="daf39-162">對</span><span class="sxs-lookup"><span data-stu-id="daf39-162">True</span></span>                                                          |
| <span data-ttu-id="daf39-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="daf39-163">Is Indexed</span></span>             | <span data-ttu-id="daf39-164">否</span><span class="sxs-lookup"><span data-stu-id="daf39-164">False</span></span>                                                         |
| <span data-ttu-id="daf39-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="daf39-165">In Global Catalog</span></span>      | <span data-ttu-id="daf39-166">否</span><span class="sxs-lookup"><span data-stu-id="daf39-166">False</span></span>                                                         |
| <span data-ttu-id="daf39-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="daf39-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="daf39-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="daf39-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="daf39-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daf39-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daf39-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-171">Search-Flags</span></span>           | <span data-ttu-id="daf39-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daf39-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="daf39-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-173">System-Flags</span></span>           | <span data-ttu-id="daf39-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daf39-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="daf39-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="daf39-175">Classes used in</span></span>        | [<span data-ttu-id="daf39-176">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="daf39-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="daf39-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="daf39-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="daf39-178">進入</span><span class="sxs-lookup"><span data-stu-id="daf39-178">Entry</span></span> | <span data-ttu-id="daf39-179">值</span><span class="sxs-lookup"><span data-stu-id="daf39-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="daf39-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="daf39-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daf39-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="daf39-182">System-Only</span></span>            | <span data-ttu-id="daf39-183">否</span><span class="sxs-lookup"><span data-stu-id="daf39-183">False</span></span>                                                         |
| <span data-ttu-id="daf39-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="daf39-184">Is-Single-Valued</span></span>       | <span data-ttu-id="daf39-185">對</span><span class="sxs-lookup"><span data-stu-id="daf39-185">True</span></span>                                                          |
| <span data-ttu-id="daf39-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="daf39-186">Is Indexed</span></span>             | <span data-ttu-id="daf39-187">否</span><span class="sxs-lookup"><span data-stu-id="daf39-187">False</span></span>                                                         |
| <span data-ttu-id="daf39-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="daf39-188">In Global Catalog</span></span>      | <span data-ttu-id="daf39-189">否</span><span class="sxs-lookup"><span data-stu-id="daf39-189">False</span></span>                                                         |
| <span data-ttu-id="daf39-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="daf39-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="daf39-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="daf39-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="daf39-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daf39-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daf39-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-194">Search-Flags</span></span>           | <span data-ttu-id="daf39-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daf39-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="daf39-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-196">System-Flags</span></span>           | <span data-ttu-id="daf39-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daf39-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="daf39-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="daf39-198">Classes used in</span></span>        | [<span data-ttu-id="daf39-199">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="daf39-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="daf39-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="daf39-200">Windows Server 2008</span></span>



| <span data-ttu-id="daf39-201">進入</span><span class="sxs-lookup"><span data-stu-id="daf39-201">Entry</span></span> | <span data-ttu-id="daf39-202">值</span><span class="sxs-lookup"><span data-stu-id="daf39-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="daf39-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="daf39-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daf39-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="daf39-205">System-Only</span></span>            | <span data-ttu-id="daf39-206">否</span><span class="sxs-lookup"><span data-stu-id="daf39-206">False</span></span>                                                         |
| <span data-ttu-id="daf39-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="daf39-207">Is-Single-Valued</span></span>       | <span data-ttu-id="daf39-208">對</span><span class="sxs-lookup"><span data-stu-id="daf39-208">True</span></span>                                                          |
| <span data-ttu-id="daf39-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="daf39-209">Is Indexed</span></span>             | <span data-ttu-id="daf39-210">否</span><span class="sxs-lookup"><span data-stu-id="daf39-210">False</span></span>                                                         |
| <span data-ttu-id="daf39-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="daf39-211">In Global Catalog</span></span>      | <span data-ttu-id="daf39-212">否</span><span class="sxs-lookup"><span data-stu-id="daf39-212">False</span></span>                                                         |
| <span data-ttu-id="daf39-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="daf39-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="daf39-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="daf39-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="daf39-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daf39-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daf39-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-217">Search-Flags</span></span>           | <span data-ttu-id="daf39-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daf39-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="daf39-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-219">System-Flags</span></span>           | <span data-ttu-id="daf39-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daf39-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="daf39-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="daf39-221">Classes used in</span></span>        | [<span data-ttu-id="daf39-222">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="daf39-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="daf39-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="daf39-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="daf39-224">進入</span><span class="sxs-lookup"><span data-stu-id="daf39-224">Entry</span></span> | <span data-ttu-id="daf39-225">值</span><span class="sxs-lookup"><span data-stu-id="daf39-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="daf39-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="daf39-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daf39-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="daf39-228">System-Only</span></span>            | <span data-ttu-id="daf39-229">否</span><span class="sxs-lookup"><span data-stu-id="daf39-229">False</span></span>                                                         |
| <span data-ttu-id="daf39-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="daf39-230">Is-Single-Valued</span></span>       | <span data-ttu-id="daf39-231">對</span><span class="sxs-lookup"><span data-stu-id="daf39-231">True</span></span>                                                          |
| <span data-ttu-id="daf39-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="daf39-232">Is Indexed</span></span>             | <span data-ttu-id="daf39-233">否</span><span class="sxs-lookup"><span data-stu-id="daf39-233">False</span></span>                                                         |
| <span data-ttu-id="daf39-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="daf39-234">In Global Catalog</span></span>      | <span data-ttu-id="daf39-235">否</span><span class="sxs-lookup"><span data-stu-id="daf39-235">False</span></span>                                                         |
| <span data-ttu-id="daf39-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="daf39-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="daf39-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="daf39-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="daf39-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daf39-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daf39-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-240">Search-Flags</span></span>           | <span data-ttu-id="daf39-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daf39-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="daf39-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-242">System-Flags</span></span>           | <span data-ttu-id="daf39-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daf39-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="daf39-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="daf39-244">Classes used in</span></span>        | [<span data-ttu-id="daf39-245">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="daf39-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="daf39-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="daf39-246">Windows Server 2012</span></span>



| <span data-ttu-id="daf39-247">進入</span><span class="sxs-lookup"><span data-stu-id="daf39-247">Entry</span></span> | <span data-ttu-id="daf39-248">值</span><span class="sxs-lookup"><span data-stu-id="daf39-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="daf39-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="daf39-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="daf39-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="daf39-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="daf39-251">System-Only</span></span>            | <span data-ttu-id="daf39-252">否</span><span class="sxs-lookup"><span data-stu-id="daf39-252">False</span></span>                                                         |
| <span data-ttu-id="daf39-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="daf39-253">Is-Single-Valued</span></span>       | <span data-ttu-id="daf39-254">對</span><span class="sxs-lookup"><span data-stu-id="daf39-254">True</span></span>                                                          |
| <span data-ttu-id="daf39-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="daf39-255">Is Indexed</span></span>             | <span data-ttu-id="daf39-256">否</span><span class="sxs-lookup"><span data-stu-id="daf39-256">False</span></span>                                                         |
| <span data-ttu-id="daf39-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="daf39-257">In Global Catalog</span></span>      | <span data-ttu-id="daf39-258">否</span><span class="sxs-lookup"><span data-stu-id="daf39-258">False</span></span>                                                         |
| <span data-ttu-id="daf39-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="daf39-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="daf39-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="daf39-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="daf39-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="daf39-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="daf39-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="daf39-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-263">Search-Flags</span></span>           | <span data-ttu-id="daf39-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="daf39-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="daf39-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="daf39-265">System-Flags</span></span>           | <span data-ttu-id="daf39-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="daf39-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="daf39-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="daf39-267">Classes used in</span></span>        | [<span data-ttu-id="daf39-268">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="daf39-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





