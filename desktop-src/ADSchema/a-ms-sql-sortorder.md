---
title: TRANSACT-SQL-SortOrder 屬性
description: SQL Server 目前實例的排序次序。
ms.assetid: cd58cb56-19aa-4ee6-b241-1198b3e9e097
ms.tgt_platform: multiple
keywords:
- MS-SQL-SortOrder 屬性 AD 架構
- mS-SQL-SortOrder 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-SortOrder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940dafa4cc9bfce15ae1a5df472720e6e779f19e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106990915"
---
# <a name="ms-sql-sortorder-attribute"></a><span data-ttu-id="8c0d1-105">TRANSACT-SQL-SortOrder 屬性</span><span class="sxs-lookup"><span data-stu-id="8c0d1-105">MS-SQL-SortOrder attribute</span></span>

<span data-ttu-id="8c0d1-106">SQL Server 目前實例的排序次序。</span><span class="sxs-lookup"><span data-stu-id="8c0d1-106">The sort order for the current instance of SQL Server.</span></span>



| <span data-ttu-id="8c0d1-107">進入</span><span class="sxs-lookup"><span data-stu-id="8c0d1-107">Entry</span></span> | <span data-ttu-id="8c0d1-108">值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8c0d1-109">CN</span><span class="sxs-lookup"><span data-stu-id="8c0d1-109">CN</span></span>                | <span data-ttu-id="8c0d1-110">MS-CHAP-SortOrder</span><span class="sxs-lookup"><span data-stu-id="8c0d1-110">MS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="8c0d1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8c0d1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8c0d1-112">Ms-chap-SortOrder</span><span class="sxs-lookup"><span data-stu-id="8c0d1-112">mS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="8c0d1-113">大小</span><span class="sxs-lookup"><span data-stu-id="8c0d1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8c0d1-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8c0d1-114">Update Privilege</span></span>  | <span data-ttu-id="8c0d1-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="8c0d1-115">Domain administrator</span></span>                        |
| <span data-ttu-id="8c0d1-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8c0d1-116">Update Frequency</span></span>  | <span data-ttu-id="8c0d1-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="8c0d1-117">At system setup.</span></span>                            |
| <span data-ttu-id="8c0d1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8c0d1-118">Attribute-Id</span></span>      | <span data-ttu-id="8c0d1-119">1.2.840.113556.1.4.1371</span><span class="sxs-lookup"><span data-stu-id="8c0d1-119">1.2.840.113556.1.4.1371</span></span>                     |
| <span data-ttu-id="8c0d1-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8c0d1-120">System-Id-Guid</span></span>    | <span data-ttu-id="8c0d1-121">6ddc42c0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="8c0d1-121">6ddc42c0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="8c0d1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c0d1-122">Syntax</span></span>            | [<span data-ttu-id="8c0d1-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8c0d1-124">實作</span><span class="sxs-lookup"><span data-stu-id="8c0d1-124">Implementations</span></span>

-   [<span data-ttu-id="8c0d1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8c0d1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8c0d1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8c0d1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8c0d1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8c0d1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8c0d1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c0d1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8c0d1-132">進入</span><span class="sxs-lookup"><span data-stu-id="8c0d1-132">Entry</span></span> | <span data-ttu-id="8c0d1-133">值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c0d1-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c0d1-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c0d1-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c0d1-136">System-Only</span></span>            | <span data-ttu-id="8c0d1-137">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-137">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8c0d1-139">對</span><span class="sxs-lookup"><span data-stu-id="8c0d1-139">True</span></span>                                                      |
| <span data-ttu-id="8c0d1-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c0d1-140">Is Indexed</span></span>             | <span data-ttu-id="8c0d1-141">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-141">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c0d1-142">In Global Catalog</span></span>      | <span data-ttu-id="8c0d1-143">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-143">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c0d1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c0d1-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c0d1-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8c0d1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c0d1-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c0d1-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-148">Search-Flags</span></span>           | <span data-ttu-id="8c0d1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c0d1-149">0x00000000</span></span>                                                |
| <span data-ttu-id="8c0d1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-150">System-Flags</span></span>           | <span data-ttu-id="8c0d1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c0d1-151">0x00000010</span></span>                                                |
| <span data-ttu-id="8c0d1-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c0d1-152">Classes used in</span></span>        | [<span data-ttu-id="8c0d1-153">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8c0d1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c0d1-154">Windows Server 2003</span></span>



| <span data-ttu-id="8c0d1-155">進入</span><span class="sxs-lookup"><span data-stu-id="8c0d1-155">Entry</span></span> | <span data-ttu-id="8c0d1-156">值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c0d1-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c0d1-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c0d1-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c0d1-159">System-Only</span></span>            | <span data-ttu-id="8c0d1-160">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-160">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8c0d1-162">對</span><span class="sxs-lookup"><span data-stu-id="8c0d1-162">True</span></span>                                                      |
| <span data-ttu-id="8c0d1-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c0d1-163">Is Indexed</span></span>             | <span data-ttu-id="8c0d1-164">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-164">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c0d1-165">In Global Catalog</span></span>      | <span data-ttu-id="8c0d1-166">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-166">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c0d1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c0d1-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c0d1-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8c0d1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c0d1-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c0d1-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-171">Search-Flags</span></span>           | <span data-ttu-id="8c0d1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c0d1-172">0x00000000</span></span>                                                |
| <span data-ttu-id="8c0d1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-173">System-Flags</span></span>           | <span data-ttu-id="8c0d1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c0d1-174">0x00000010</span></span>                                                |
| <span data-ttu-id="8c0d1-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c0d1-175">Classes used in</span></span>        | [<span data-ttu-id="8c0d1-176">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8c0d1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8c0d1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8c0d1-178">進入</span><span class="sxs-lookup"><span data-stu-id="8c0d1-178">Entry</span></span> | <span data-ttu-id="8c0d1-179">值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c0d1-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c0d1-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c0d1-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c0d1-182">System-Only</span></span>            | <span data-ttu-id="8c0d1-183">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-183">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8c0d1-185">對</span><span class="sxs-lookup"><span data-stu-id="8c0d1-185">True</span></span>                                                      |
| <span data-ttu-id="8c0d1-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c0d1-186">Is Indexed</span></span>             | <span data-ttu-id="8c0d1-187">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-187">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c0d1-188">In Global Catalog</span></span>      | <span data-ttu-id="8c0d1-189">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-189">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c0d1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c0d1-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c0d1-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8c0d1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c0d1-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c0d1-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-194">Search-Flags</span></span>           | <span data-ttu-id="8c0d1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c0d1-195">0x00000000</span></span>                                                |
| <span data-ttu-id="8c0d1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-196">System-Flags</span></span>           | <span data-ttu-id="8c0d1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c0d1-197">0x00000010</span></span>                                                |
| <span data-ttu-id="8c0d1-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c0d1-198">Classes used in</span></span>        | [<span data-ttu-id="8c0d1-199">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8c0d1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c0d1-200">Windows Server 2008</span></span>



| <span data-ttu-id="8c0d1-201">進入</span><span class="sxs-lookup"><span data-stu-id="8c0d1-201">Entry</span></span> | <span data-ttu-id="8c0d1-202">值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c0d1-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c0d1-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c0d1-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c0d1-205">System-Only</span></span>            | <span data-ttu-id="8c0d1-206">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-206">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8c0d1-208">對</span><span class="sxs-lookup"><span data-stu-id="8c0d1-208">True</span></span>                                                      |
| <span data-ttu-id="8c0d1-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c0d1-209">Is Indexed</span></span>             | <span data-ttu-id="8c0d1-210">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-210">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c0d1-211">In Global Catalog</span></span>      | <span data-ttu-id="8c0d1-212">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-212">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c0d1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c0d1-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c0d1-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8c0d1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c0d1-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c0d1-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-217">Search-Flags</span></span>           | <span data-ttu-id="8c0d1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c0d1-218">0x00000000</span></span>                                                |
| <span data-ttu-id="8c0d1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-219">System-Flags</span></span>           | <span data-ttu-id="8c0d1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c0d1-220">0x00000010</span></span>                                                |
| <span data-ttu-id="8c0d1-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c0d1-221">Classes used in</span></span>        | [<span data-ttu-id="8c0d1-222">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8c0d1-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8c0d1-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8c0d1-224">進入</span><span class="sxs-lookup"><span data-stu-id="8c0d1-224">Entry</span></span> | <span data-ttu-id="8c0d1-225">值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c0d1-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c0d1-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c0d1-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c0d1-228">System-Only</span></span>            | <span data-ttu-id="8c0d1-229">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-229">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8c0d1-231">對</span><span class="sxs-lookup"><span data-stu-id="8c0d1-231">True</span></span>                                                      |
| <span data-ttu-id="8c0d1-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c0d1-232">Is Indexed</span></span>             | <span data-ttu-id="8c0d1-233">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-233">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c0d1-234">In Global Catalog</span></span>      | <span data-ttu-id="8c0d1-235">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-235">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c0d1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c0d1-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c0d1-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8c0d1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c0d1-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c0d1-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-240">Search-Flags</span></span>           | <span data-ttu-id="8c0d1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c0d1-241">0x00000000</span></span>                                                |
| <span data-ttu-id="8c0d1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-242">System-Flags</span></span>           | <span data-ttu-id="8c0d1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c0d1-243">0x00000010</span></span>                                                |
| <span data-ttu-id="8c0d1-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c0d1-244">Classes used in</span></span>        | [<span data-ttu-id="8c0d1-245">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8c0d1-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c0d1-246">Windows Server 2012</span></span>



| <span data-ttu-id="8c0d1-247">進入</span><span class="sxs-lookup"><span data-stu-id="8c0d1-247">Entry</span></span> | <span data-ttu-id="8c0d1-248">值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8c0d1-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c0d1-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c0d1-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8c0d1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c0d1-251">System-Only</span></span>            | <span data-ttu-id="8c0d1-252">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-252">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c0d1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8c0d1-254">對</span><span class="sxs-lookup"><span data-stu-id="8c0d1-254">True</span></span>                                                      |
| <span data-ttu-id="8c0d1-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c0d1-255">Is Indexed</span></span>             | <span data-ttu-id="8c0d1-256">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-256">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c0d1-257">In Global Catalog</span></span>      | <span data-ttu-id="8c0d1-258">否</span><span class="sxs-lookup"><span data-stu-id="8c0d1-258">False</span></span>                                                     |
| <span data-ttu-id="8c0d1-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c0d1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c0d1-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c0d1-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8c0d1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c0d1-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c0d1-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8c0d1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-263">Search-Flags</span></span>           | <span data-ttu-id="8c0d1-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c0d1-264">0x00000000</span></span>                                                |
| <span data-ttu-id="8c0d1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c0d1-265">System-Flags</span></span>           | <span data-ttu-id="8c0d1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c0d1-266">0x00000010</span></span>                                                |
| <span data-ttu-id="8c0d1-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c0d1-267">Classes used in</span></span>        | [<span data-ttu-id="8c0d1-268">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8c0d1-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





