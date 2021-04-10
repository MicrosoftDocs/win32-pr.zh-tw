---
title: CharacterSet 屬性
description: SQL Server 目前實例的字元集。
ms.assetid: 5c45058f-e883-455c-8e18-415ddae149f8
ms.tgt_platform: multiple
keywords:
- CharacterSet 屬性 AD 架構
- CharacterSet 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-CharacterSet
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2f3718c9e47393498e42c4091283ea768d5072
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845559"
---
# <a name="ms-sql-characterset-attribute"></a><span data-ttu-id="74f5b-105">CharacterSet 屬性</span><span class="sxs-lookup"><span data-stu-id="74f5b-105">MS-SQL-CharacterSet attribute</span></span>

<span data-ttu-id="74f5b-106">SQL Server 目前實例的字元集。</span><span class="sxs-lookup"><span data-stu-id="74f5b-106">The character set for the current instance of SQL Server.</span></span>



| <span data-ttu-id="74f5b-107">進入</span><span class="sxs-lookup"><span data-stu-id="74f5b-107">Entry</span></span> | <span data-ttu-id="74f5b-108">值</span><span class="sxs-lookup"><span data-stu-id="74f5b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="74f5b-109">CN</span><span class="sxs-lookup"><span data-stu-id="74f5b-109">CN</span></span>                | <span data-ttu-id="74f5b-110">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="74f5b-110">MS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="74f5b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="74f5b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="74f5b-112">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="74f5b-112">mS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="74f5b-113">大小</span><span class="sxs-lookup"><span data-stu-id="74f5b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="74f5b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="74f5b-114">Update Privilege</span></span>  | <span data-ttu-id="74f5b-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="74f5b-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="74f5b-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="74f5b-116">Update Frequency</span></span>  | <span data-ttu-id="74f5b-117">在系統啟動時。</span><span class="sxs-lookup"><span data-stu-id="74f5b-117">At system startup.</span></span>                   |
| <span data-ttu-id="74f5b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74f5b-118">Attribute-Id</span></span>      | <span data-ttu-id="74f5b-119">1.2.840.113556.1.4.1370</span><span class="sxs-lookup"><span data-stu-id="74f5b-119">1.2.840.113556.1.4.1370</span></span>              |
| <span data-ttu-id="74f5b-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="74f5b-120">System-Id-Guid</span></span>    | <span data-ttu-id="74f5b-121">696177a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="74f5b-121">696177a6-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="74f5b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f5b-122">Syntax</span></span>            | [<span data-ttu-id="74f5b-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="74f5b-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="74f5b-124">實作</span><span class="sxs-lookup"><span data-stu-id="74f5b-124">Implementations</span></span>

-   [<span data-ttu-id="74f5b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="74f5b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="74f5b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="74f5b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="74f5b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="74f5b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="74f5b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="74f5b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="74f5b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="74f5b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="74f5b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74f5b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="74f5b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74f5b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="74f5b-132">進入</span><span class="sxs-lookup"><span data-stu-id="74f5b-132">Entry</span></span> | <span data-ttu-id="74f5b-133">值</span><span class="sxs-lookup"><span data-stu-id="74f5b-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="74f5b-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74f5b-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74f5b-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="74f5b-136">System-Only</span></span>            | <span data-ttu-id="74f5b-137">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-137">False</span></span>                                                     |
| <span data-ttu-id="74f5b-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74f5b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="74f5b-139">對</span><span class="sxs-lookup"><span data-stu-id="74f5b-139">True</span></span>                                                      |
| <span data-ttu-id="74f5b-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74f5b-140">Is Indexed</span></span>             | <span data-ttu-id="74f5b-141">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-141">False</span></span>                                                     |
| <span data-ttu-id="74f5b-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74f5b-142">In Global Catalog</span></span>      | <span data-ttu-id="74f5b-143">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-143">False</span></span>                                                     |
| <span data-ttu-id="74f5b-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74f5b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="74f5b-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74f5b-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="74f5b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74f5b-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74f5b-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-148">Search-Flags</span></span>           | <span data-ttu-id="74f5b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74f5b-149">0x00000000</span></span>                                                |
| <span data-ttu-id="74f5b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-150">System-Flags</span></span>           | <span data-ttu-id="74f5b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74f5b-151">0x00000010</span></span>                                                |
| <span data-ttu-id="74f5b-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74f5b-152">Classes used in</span></span>        | [<span data-ttu-id="74f5b-153">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="74f5b-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="74f5b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74f5b-154">Windows Server 2003</span></span>



| <span data-ttu-id="74f5b-155">進入</span><span class="sxs-lookup"><span data-stu-id="74f5b-155">Entry</span></span> | <span data-ttu-id="74f5b-156">值</span><span class="sxs-lookup"><span data-stu-id="74f5b-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="74f5b-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74f5b-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74f5b-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="74f5b-159">System-Only</span></span>            | <span data-ttu-id="74f5b-160">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-160">False</span></span>                                                     |
| <span data-ttu-id="74f5b-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74f5b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="74f5b-162">對</span><span class="sxs-lookup"><span data-stu-id="74f5b-162">True</span></span>                                                      |
| <span data-ttu-id="74f5b-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74f5b-163">Is Indexed</span></span>             | <span data-ttu-id="74f5b-164">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-164">False</span></span>                                                     |
| <span data-ttu-id="74f5b-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74f5b-165">In Global Catalog</span></span>      | <span data-ttu-id="74f5b-166">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-166">False</span></span>                                                     |
| <span data-ttu-id="74f5b-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74f5b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="74f5b-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74f5b-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="74f5b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74f5b-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74f5b-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-171">Search-Flags</span></span>           | <span data-ttu-id="74f5b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74f5b-172">0x00000000</span></span>                                                |
| <span data-ttu-id="74f5b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-173">System-Flags</span></span>           | <span data-ttu-id="74f5b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74f5b-174">0x00000010</span></span>                                                |
| <span data-ttu-id="74f5b-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74f5b-175">Classes used in</span></span>        | [<span data-ttu-id="74f5b-176">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="74f5b-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="74f5b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="74f5b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="74f5b-178">進入</span><span class="sxs-lookup"><span data-stu-id="74f5b-178">Entry</span></span> | <span data-ttu-id="74f5b-179">值</span><span class="sxs-lookup"><span data-stu-id="74f5b-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="74f5b-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74f5b-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74f5b-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="74f5b-182">System-Only</span></span>            | <span data-ttu-id="74f5b-183">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-183">False</span></span>                                                     |
| <span data-ttu-id="74f5b-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74f5b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="74f5b-185">對</span><span class="sxs-lookup"><span data-stu-id="74f5b-185">True</span></span>                                                      |
| <span data-ttu-id="74f5b-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74f5b-186">Is Indexed</span></span>             | <span data-ttu-id="74f5b-187">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-187">False</span></span>                                                     |
| <span data-ttu-id="74f5b-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74f5b-188">In Global Catalog</span></span>      | <span data-ttu-id="74f5b-189">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-189">False</span></span>                                                     |
| <span data-ttu-id="74f5b-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74f5b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="74f5b-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74f5b-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="74f5b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74f5b-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74f5b-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-194">Search-Flags</span></span>           | <span data-ttu-id="74f5b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74f5b-195">0x00000000</span></span>                                                |
| <span data-ttu-id="74f5b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-196">System-Flags</span></span>           | <span data-ttu-id="74f5b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74f5b-197">0x00000010</span></span>                                                |
| <span data-ttu-id="74f5b-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74f5b-198">Classes used in</span></span>        | [<span data-ttu-id="74f5b-199">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="74f5b-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="74f5b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74f5b-200">Windows Server 2008</span></span>



| <span data-ttu-id="74f5b-201">進入</span><span class="sxs-lookup"><span data-stu-id="74f5b-201">Entry</span></span> | <span data-ttu-id="74f5b-202">值</span><span class="sxs-lookup"><span data-stu-id="74f5b-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="74f5b-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74f5b-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74f5b-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="74f5b-205">System-Only</span></span>            | <span data-ttu-id="74f5b-206">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-206">False</span></span>                                                     |
| <span data-ttu-id="74f5b-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74f5b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="74f5b-208">對</span><span class="sxs-lookup"><span data-stu-id="74f5b-208">True</span></span>                                                      |
| <span data-ttu-id="74f5b-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74f5b-209">Is Indexed</span></span>             | <span data-ttu-id="74f5b-210">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-210">False</span></span>                                                     |
| <span data-ttu-id="74f5b-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74f5b-211">In Global Catalog</span></span>      | <span data-ttu-id="74f5b-212">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-212">False</span></span>                                                     |
| <span data-ttu-id="74f5b-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74f5b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="74f5b-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74f5b-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="74f5b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74f5b-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74f5b-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-217">Search-Flags</span></span>           | <span data-ttu-id="74f5b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74f5b-218">0x00000000</span></span>                                                |
| <span data-ttu-id="74f5b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-219">System-Flags</span></span>           | <span data-ttu-id="74f5b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74f5b-220">0x00000010</span></span>                                                |
| <span data-ttu-id="74f5b-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74f5b-221">Classes used in</span></span>        | [<span data-ttu-id="74f5b-222">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="74f5b-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="74f5b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74f5b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="74f5b-224">進入</span><span class="sxs-lookup"><span data-stu-id="74f5b-224">Entry</span></span> | <span data-ttu-id="74f5b-225">值</span><span class="sxs-lookup"><span data-stu-id="74f5b-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="74f5b-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74f5b-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74f5b-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="74f5b-228">System-Only</span></span>            | <span data-ttu-id="74f5b-229">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-229">False</span></span>                                                     |
| <span data-ttu-id="74f5b-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74f5b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="74f5b-231">對</span><span class="sxs-lookup"><span data-stu-id="74f5b-231">True</span></span>                                                      |
| <span data-ttu-id="74f5b-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74f5b-232">Is Indexed</span></span>             | <span data-ttu-id="74f5b-233">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-233">False</span></span>                                                     |
| <span data-ttu-id="74f5b-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74f5b-234">In Global Catalog</span></span>      | <span data-ttu-id="74f5b-235">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-235">False</span></span>                                                     |
| <span data-ttu-id="74f5b-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74f5b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="74f5b-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74f5b-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="74f5b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74f5b-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74f5b-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-240">Search-Flags</span></span>           | <span data-ttu-id="74f5b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74f5b-241">0x00000000</span></span>                                                |
| <span data-ttu-id="74f5b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-242">System-Flags</span></span>           | <span data-ttu-id="74f5b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74f5b-243">0x00000010</span></span>                                                |
| <span data-ttu-id="74f5b-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74f5b-244">Classes used in</span></span>        | [<span data-ttu-id="74f5b-245">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="74f5b-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="74f5b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74f5b-246">Windows Server 2012</span></span>



| <span data-ttu-id="74f5b-247">進入</span><span class="sxs-lookup"><span data-stu-id="74f5b-247">Entry</span></span> | <span data-ttu-id="74f5b-248">值</span><span class="sxs-lookup"><span data-stu-id="74f5b-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="74f5b-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="74f5b-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74f5b-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="74f5b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="74f5b-251">System-Only</span></span>            | <span data-ttu-id="74f5b-252">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-252">False</span></span>                                                     |
| <span data-ttu-id="74f5b-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="74f5b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="74f5b-254">對</span><span class="sxs-lookup"><span data-stu-id="74f5b-254">True</span></span>                                                      |
| <span data-ttu-id="74f5b-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="74f5b-255">Is Indexed</span></span>             | <span data-ttu-id="74f5b-256">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-256">False</span></span>                                                     |
| <span data-ttu-id="74f5b-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="74f5b-257">In Global Catalog</span></span>      | <span data-ttu-id="74f5b-258">否</span><span class="sxs-lookup"><span data-stu-id="74f5b-258">False</span></span>                                                     |
| <span data-ttu-id="74f5b-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="74f5b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="74f5b-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="74f5b-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="74f5b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74f5b-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74f5b-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="74f5b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-263">Search-Flags</span></span>           | <span data-ttu-id="74f5b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74f5b-264">0x00000000</span></span>                                                |
| <span data-ttu-id="74f5b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74f5b-265">System-Flags</span></span>           | <span data-ttu-id="74f5b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74f5b-266">0x00000010</span></span>                                                |
| <span data-ttu-id="74f5b-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="74f5b-267">Classes used in</span></span>        | [<span data-ttu-id="74f5b-268">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="74f5b-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





