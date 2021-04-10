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
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="9129b-105">LastDiagnosticDate 屬性</span><span class="sxs-lookup"><span data-stu-id="9129b-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="9129b-106">DBCC checkdb 上次執行的日期。</span><span class="sxs-lookup"><span data-stu-id="9129b-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="9129b-107">進入</span><span class="sxs-lookup"><span data-stu-id="9129b-107">Entry</span></span> | <span data-ttu-id="9129b-108">值</span><span class="sxs-lookup"><span data-stu-id="9129b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9129b-109">CN</span><span class="sxs-lookup"><span data-stu-id="9129b-109">CN</span></span>                | <span data-ttu-id="9129b-110">LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="9129b-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="9129b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9129b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9129b-112">LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="9129b-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="9129b-113">大小</span><span class="sxs-lookup"><span data-stu-id="9129b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9129b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9129b-114">Update Privilege</span></span>  | <span data-ttu-id="9129b-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9129b-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="9129b-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9129b-116">Update Frequency</span></span>  | <span data-ttu-id="9129b-117">當 DBCC checkdb 執行時。</span><span class="sxs-lookup"><span data-stu-id="9129b-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="9129b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9129b-118">Attribute-Id</span></span>      | <span data-ttu-id="9129b-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="9129b-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="9129b-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9129b-120">System-Id-Guid</span></span>    | <span data-ttu-id="9129b-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9129b-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="9129b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9129b-122">Syntax</span></span>            | [<span data-ttu-id="9129b-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9129b-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9129b-124">實作</span><span class="sxs-lookup"><span data-stu-id="9129b-124">Implementations</span></span>

-   [<span data-ttu-id="9129b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9129b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9129b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9129b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9129b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9129b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9129b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9129b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9129b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9129b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9129b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9129b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9129b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9129b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9129b-132">進入</span><span class="sxs-lookup"><span data-stu-id="9129b-132">Entry</span></span> | <span data-ttu-id="9129b-133">值</span><span class="sxs-lookup"><span data-stu-id="9129b-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9129b-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9129b-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9129b-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9129b-136">System-Only</span></span>            | <span data-ttu-id="9129b-137">否</span><span class="sxs-lookup"><span data-stu-id="9129b-137">False</span></span>                                                         |
| <span data-ttu-id="9129b-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9129b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9129b-139">對</span><span class="sxs-lookup"><span data-stu-id="9129b-139">True</span></span>                                                          |
| <span data-ttu-id="9129b-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9129b-140">Is Indexed</span></span>             | <span data-ttu-id="9129b-141">否</span><span class="sxs-lookup"><span data-stu-id="9129b-141">False</span></span>                                                         |
| <span data-ttu-id="9129b-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9129b-142">In Global Catalog</span></span>      | <span data-ttu-id="9129b-143">否</span><span class="sxs-lookup"><span data-stu-id="9129b-143">False</span></span>                                                         |
| <span data-ttu-id="9129b-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9129b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9129b-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9129b-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9129b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9129b-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9129b-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-148">Search-Flags</span></span>           | <span data-ttu-id="9129b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9129b-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="9129b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-150">System-Flags</span></span>           | <span data-ttu-id="9129b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9129b-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="9129b-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9129b-152">Classes used in</span></span>        | [<span data-ttu-id="9129b-153">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="9129b-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9129b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9129b-154">Windows Server 2003</span></span>



| <span data-ttu-id="9129b-155">進入</span><span class="sxs-lookup"><span data-stu-id="9129b-155">Entry</span></span> | <span data-ttu-id="9129b-156">值</span><span class="sxs-lookup"><span data-stu-id="9129b-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9129b-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9129b-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9129b-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9129b-159">System-Only</span></span>            | <span data-ttu-id="9129b-160">否</span><span class="sxs-lookup"><span data-stu-id="9129b-160">False</span></span>                                                         |
| <span data-ttu-id="9129b-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9129b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9129b-162">對</span><span class="sxs-lookup"><span data-stu-id="9129b-162">True</span></span>                                                          |
| <span data-ttu-id="9129b-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9129b-163">Is Indexed</span></span>             | <span data-ttu-id="9129b-164">否</span><span class="sxs-lookup"><span data-stu-id="9129b-164">False</span></span>                                                         |
| <span data-ttu-id="9129b-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9129b-165">In Global Catalog</span></span>      | <span data-ttu-id="9129b-166">否</span><span class="sxs-lookup"><span data-stu-id="9129b-166">False</span></span>                                                         |
| <span data-ttu-id="9129b-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9129b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9129b-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9129b-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9129b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9129b-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9129b-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-171">Search-Flags</span></span>           | <span data-ttu-id="9129b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9129b-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="9129b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-173">System-Flags</span></span>           | <span data-ttu-id="9129b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9129b-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="9129b-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9129b-175">Classes used in</span></span>        | [<span data-ttu-id="9129b-176">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="9129b-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9129b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9129b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9129b-178">進入</span><span class="sxs-lookup"><span data-stu-id="9129b-178">Entry</span></span> | <span data-ttu-id="9129b-179">值</span><span class="sxs-lookup"><span data-stu-id="9129b-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9129b-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9129b-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9129b-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9129b-182">System-Only</span></span>            | <span data-ttu-id="9129b-183">否</span><span class="sxs-lookup"><span data-stu-id="9129b-183">False</span></span>                                                         |
| <span data-ttu-id="9129b-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9129b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9129b-185">對</span><span class="sxs-lookup"><span data-stu-id="9129b-185">True</span></span>                                                          |
| <span data-ttu-id="9129b-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9129b-186">Is Indexed</span></span>             | <span data-ttu-id="9129b-187">否</span><span class="sxs-lookup"><span data-stu-id="9129b-187">False</span></span>                                                         |
| <span data-ttu-id="9129b-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9129b-188">In Global Catalog</span></span>      | <span data-ttu-id="9129b-189">否</span><span class="sxs-lookup"><span data-stu-id="9129b-189">False</span></span>                                                         |
| <span data-ttu-id="9129b-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9129b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9129b-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9129b-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9129b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9129b-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9129b-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-194">Search-Flags</span></span>           | <span data-ttu-id="9129b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9129b-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="9129b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-196">System-Flags</span></span>           | <span data-ttu-id="9129b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9129b-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="9129b-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9129b-198">Classes used in</span></span>        | [<span data-ttu-id="9129b-199">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="9129b-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9129b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9129b-200">Windows Server 2008</span></span>



| <span data-ttu-id="9129b-201">進入</span><span class="sxs-lookup"><span data-stu-id="9129b-201">Entry</span></span> | <span data-ttu-id="9129b-202">值</span><span class="sxs-lookup"><span data-stu-id="9129b-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9129b-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9129b-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9129b-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9129b-205">System-Only</span></span>            | <span data-ttu-id="9129b-206">否</span><span class="sxs-lookup"><span data-stu-id="9129b-206">False</span></span>                                                         |
| <span data-ttu-id="9129b-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9129b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9129b-208">對</span><span class="sxs-lookup"><span data-stu-id="9129b-208">True</span></span>                                                          |
| <span data-ttu-id="9129b-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9129b-209">Is Indexed</span></span>             | <span data-ttu-id="9129b-210">否</span><span class="sxs-lookup"><span data-stu-id="9129b-210">False</span></span>                                                         |
| <span data-ttu-id="9129b-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9129b-211">In Global Catalog</span></span>      | <span data-ttu-id="9129b-212">否</span><span class="sxs-lookup"><span data-stu-id="9129b-212">False</span></span>                                                         |
| <span data-ttu-id="9129b-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9129b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9129b-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9129b-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9129b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9129b-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9129b-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-217">Search-Flags</span></span>           | <span data-ttu-id="9129b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9129b-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="9129b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-219">System-Flags</span></span>           | <span data-ttu-id="9129b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9129b-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="9129b-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9129b-221">Classes used in</span></span>        | [<span data-ttu-id="9129b-222">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="9129b-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9129b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9129b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9129b-224">進入</span><span class="sxs-lookup"><span data-stu-id="9129b-224">Entry</span></span> | <span data-ttu-id="9129b-225">值</span><span class="sxs-lookup"><span data-stu-id="9129b-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9129b-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9129b-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9129b-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9129b-228">System-Only</span></span>            | <span data-ttu-id="9129b-229">否</span><span class="sxs-lookup"><span data-stu-id="9129b-229">False</span></span>                                                         |
| <span data-ttu-id="9129b-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9129b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9129b-231">對</span><span class="sxs-lookup"><span data-stu-id="9129b-231">True</span></span>                                                          |
| <span data-ttu-id="9129b-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9129b-232">Is Indexed</span></span>             | <span data-ttu-id="9129b-233">否</span><span class="sxs-lookup"><span data-stu-id="9129b-233">False</span></span>                                                         |
| <span data-ttu-id="9129b-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9129b-234">In Global Catalog</span></span>      | <span data-ttu-id="9129b-235">否</span><span class="sxs-lookup"><span data-stu-id="9129b-235">False</span></span>                                                         |
| <span data-ttu-id="9129b-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9129b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9129b-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9129b-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9129b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9129b-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9129b-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-240">Search-Flags</span></span>           | <span data-ttu-id="9129b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9129b-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="9129b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-242">System-Flags</span></span>           | <span data-ttu-id="9129b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9129b-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="9129b-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9129b-244">Classes used in</span></span>        | [<span data-ttu-id="9129b-245">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="9129b-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9129b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9129b-246">Windows Server 2012</span></span>



| <span data-ttu-id="9129b-247">進入</span><span class="sxs-lookup"><span data-stu-id="9129b-247">Entry</span></span> | <span data-ttu-id="9129b-248">值</span><span class="sxs-lookup"><span data-stu-id="9129b-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9129b-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9129b-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9129b-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="9129b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9129b-251">System-Only</span></span>            | <span data-ttu-id="9129b-252">否</span><span class="sxs-lookup"><span data-stu-id="9129b-252">False</span></span>                                                         |
| <span data-ttu-id="9129b-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9129b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9129b-254">對</span><span class="sxs-lookup"><span data-stu-id="9129b-254">True</span></span>                                                          |
| <span data-ttu-id="9129b-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9129b-255">Is Indexed</span></span>             | <span data-ttu-id="9129b-256">否</span><span class="sxs-lookup"><span data-stu-id="9129b-256">False</span></span>                                                         |
| <span data-ttu-id="9129b-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9129b-257">In Global Catalog</span></span>      | <span data-ttu-id="9129b-258">否</span><span class="sxs-lookup"><span data-stu-id="9129b-258">False</span></span>                                                         |
| <span data-ttu-id="9129b-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9129b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9129b-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9129b-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="9129b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9129b-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9129b-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="9129b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-263">Search-Flags</span></span>           | <span data-ttu-id="9129b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9129b-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="9129b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9129b-265">System-Flags</span></span>           | <span data-ttu-id="9129b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9129b-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="9129b-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9129b-267">Classes used in</span></span>        | [<span data-ttu-id="9129b-268">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="9129b-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





