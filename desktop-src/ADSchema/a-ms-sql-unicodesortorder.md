---
title: UnicodeSortOrder 屬性
description: SQL Server 目前實例的 Unicode 排序次序。
ms.assetid: c7f9d81d-a9c3-4be9-8ead-cf3d59352dbb
ms.tgt_platform: multiple
keywords:
- UnicodeSortOrder 屬性 AD 架構
- UnicodeSortOrder 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-UnicodeSortOrder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9240844a45e8e4ea567ff96df0eb992f316a7787
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509538"
---
# <a name="ms-sql-unicodesortorder-attribute"></a><span data-ttu-id="07a51-105">UnicodeSortOrder 屬性</span><span class="sxs-lookup"><span data-stu-id="07a51-105">MS-SQL-UnicodeSortOrder attribute</span></span>

<span data-ttu-id="07a51-106">SQL Server 目前實例的 Unicode 排序次序。</span><span class="sxs-lookup"><span data-stu-id="07a51-106">The Unicode sort order for the current instance of SQL Server.</span></span>



| <span data-ttu-id="07a51-107">進入</span><span class="sxs-lookup"><span data-stu-id="07a51-107">Entry</span></span> | <span data-ttu-id="07a51-108">值</span><span class="sxs-lookup"><span data-stu-id="07a51-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="07a51-109">CN</span><span class="sxs-lookup"><span data-stu-id="07a51-109">CN</span></span>                | <span data-ttu-id="07a51-110">UnicodeSortOrder</span><span class="sxs-lookup"><span data-stu-id="07a51-110">MS-SQL-UnicodeSortOrder</span></span>              |
| <span data-ttu-id="07a51-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="07a51-111">Ldap-Display-Name</span></span> | <span data-ttu-id="07a51-112">UnicodeSortOrder</span><span class="sxs-lookup"><span data-stu-id="07a51-112">mS-SQL-UnicodeSortOrder</span></span>              |
| <span data-ttu-id="07a51-113">大小</span><span class="sxs-lookup"><span data-stu-id="07a51-113">Size</span></span>              | <span data-ttu-id="07a51-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="07a51-114">4 bytes</span></span>                              |
| <span data-ttu-id="07a51-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="07a51-115">Update Privilege</span></span>  | <span data-ttu-id="07a51-116">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="07a51-116">Domain administrator</span></span>                 |
| <span data-ttu-id="07a51-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="07a51-117">Update Frequency</span></span>  | <span data-ttu-id="07a51-118">在系統啟動時。</span><span class="sxs-lookup"><span data-stu-id="07a51-118">At system startup.</span></span>                   |
| <span data-ttu-id="07a51-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="07a51-119">Attribute-Id</span></span>      | <span data-ttu-id="07a51-120">1.2.840.113556.1.4.1372</span><span class="sxs-lookup"><span data-stu-id="07a51-120">1.2.840.113556.1.4.1372</span></span>              |
| <span data-ttu-id="07a51-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="07a51-121">System-Id-Guid</span></span>    | <span data-ttu-id="07a51-122">72dc918a-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="07a51-122">72dc918a-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="07a51-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="07a51-123">Syntax</span></span>            | [<span data-ttu-id="07a51-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="07a51-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="07a51-125">實作</span><span class="sxs-lookup"><span data-stu-id="07a51-125">Implementations</span></span>

-   [<span data-ttu-id="07a51-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="07a51-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="07a51-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="07a51-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="07a51-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="07a51-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="07a51-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="07a51-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="07a51-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="07a51-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="07a51-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="07a51-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="07a51-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="07a51-132">Windows 2000 Server</span></span>



| <span data-ttu-id="07a51-133">進入</span><span class="sxs-lookup"><span data-stu-id="07a51-133">Entry</span></span> | <span data-ttu-id="07a51-134">值</span><span class="sxs-lookup"><span data-stu-id="07a51-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="07a51-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="07a51-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a51-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a51-137">System-Only</span></span>            | <span data-ttu-id="07a51-138">否</span><span class="sxs-lookup"><span data-stu-id="07a51-138">False</span></span>                                                     |
| <span data-ttu-id="07a51-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="07a51-139">Is-Single-Valued</span></span>       | <span data-ttu-id="07a51-140">對</span><span class="sxs-lookup"><span data-stu-id="07a51-140">True</span></span>                                                      |
| <span data-ttu-id="07a51-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="07a51-141">Is Indexed</span></span>             | <span data-ttu-id="07a51-142">否</span><span class="sxs-lookup"><span data-stu-id="07a51-142">False</span></span>                                                     |
| <span data-ttu-id="07a51-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="07a51-143">In Global Catalog</span></span>      | <span data-ttu-id="07a51-144">否</span><span class="sxs-lookup"><span data-stu-id="07a51-144">False</span></span>                                                     |
| <span data-ttu-id="07a51-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="07a51-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a51-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="07a51-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="07a51-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a51-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a51-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-149">Search-Flags</span></span>           | <span data-ttu-id="07a51-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a51-150">0x00000000</span></span>                                                |
| <span data-ttu-id="07a51-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-151">System-Flags</span></span>           | <span data-ttu-id="07a51-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a51-152">0x00000010</span></span>                                                |
| <span data-ttu-id="07a51-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="07a51-153">Classes used in</span></span>        | [<span data-ttu-id="07a51-154">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="07a51-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="07a51-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07a51-155">Windows Server 2003</span></span>



| <span data-ttu-id="07a51-156">進入</span><span class="sxs-lookup"><span data-stu-id="07a51-156">Entry</span></span> | <span data-ttu-id="07a51-157">值</span><span class="sxs-lookup"><span data-stu-id="07a51-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="07a51-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="07a51-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a51-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a51-160">System-Only</span></span>            | <span data-ttu-id="07a51-161">否</span><span class="sxs-lookup"><span data-stu-id="07a51-161">False</span></span>                                                     |
| <span data-ttu-id="07a51-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="07a51-162">Is-Single-Valued</span></span>       | <span data-ttu-id="07a51-163">對</span><span class="sxs-lookup"><span data-stu-id="07a51-163">True</span></span>                                                      |
| <span data-ttu-id="07a51-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="07a51-164">Is Indexed</span></span>             | <span data-ttu-id="07a51-165">否</span><span class="sxs-lookup"><span data-stu-id="07a51-165">False</span></span>                                                     |
| <span data-ttu-id="07a51-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="07a51-166">In Global Catalog</span></span>      | <span data-ttu-id="07a51-167">否</span><span class="sxs-lookup"><span data-stu-id="07a51-167">False</span></span>                                                     |
| <span data-ttu-id="07a51-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="07a51-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a51-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="07a51-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="07a51-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a51-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a51-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-172">Search-Flags</span></span>           | <span data-ttu-id="07a51-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a51-173">0x00000000</span></span>                                                |
| <span data-ttu-id="07a51-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-174">System-Flags</span></span>           | <span data-ttu-id="07a51-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a51-175">0x00000010</span></span>                                                |
| <span data-ttu-id="07a51-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="07a51-176">Classes used in</span></span>        | [<span data-ttu-id="07a51-177">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="07a51-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="07a51-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="07a51-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="07a51-179">進入</span><span class="sxs-lookup"><span data-stu-id="07a51-179">Entry</span></span> | <span data-ttu-id="07a51-180">值</span><span class="sxs-lookup"><span data-stu-id="07a51-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="07a51-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="07a51-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a51-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a51-183">System-Only</span></span>            | <span data-ttu-id="07a51-184">否</span><span class="sxs-lookup"><span data-stu-id="07a51-184">False</span></span>                                                     |
| <span data-ttu-id="07a51-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="07a51-185">Is-Single-Valued</span></span>       | <span data-ttu-id="07a51-186">對</span><span class="sxs-lookup"><span data-stu-id="07a51-186">True</span></span>                                                      |
| <span data-ttu-id="07a51-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="07a51-187">Is Indexed</span></span>             | <span data-ttu-id="07a51-188">否</span><span class="sxs-lookup"><span data-stu-id="07a51-188">False</span></span>                                                     |
| <span data-ttu-id="07a51-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="07a51-189">In Global Catalog</span></span>      | <span data-ttu-id="07a51-190">否</span><span class="sxs-lookup"><span data-stu-id="07a51-190">False</span></span>                                                     |
| <span data-ttu-id="07a51-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="07a51-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a51-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="07a51-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="07a51-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a51-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a51-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-195">Search-Flags</span></span>           | <span data-ttu-id="07a51-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a51-196">0x00000000</span></span>                                                |
| <span data-ttu-id="07a51-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-197">System-Flags</span></span>           | <span data-ttu-id="07a51-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a51-198">0x00000010</span></span>                                                |
| <span data-ttu-id="07a51-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="07a51-199">Classes used in</span></span>        | [<span data-ttu-id="07a51-200">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="07a51-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="07a51-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07a51-201">Windows Server 2008</span></span>



| <span data-ttu-id="07a51-202">進入</span><span class="sxs-lookup"><span data-stu-id="07a51-202">Entry</span></span> | <span data-ttu-id="07a51-203">值</span><span class="sxs-lookup"><span data-stu-id="07a51-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="07a51-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="07a51-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a51-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a51-206">System-Only</span></span>            | <span data-ttu-id="07a51-207">否</span><span class="sxs-lookup"><span data-stu-id="07a51-207">False</span></span>                                                     |
| <span data-ttu-id="07a51-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="07a51-208">Is-Single-Valued</span></span>       | <span data-ttu-id="07a51-209">對</span><span class="sxs-lookup"><span data-stu-id="07a51-209">True</span></span>                                                      |
| <span data-ttu-id="07a51-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="07a51-210">Is Indexed</span></span>             | <span data-ttu-id="07a51-211">否</span><span class="sxs-lookup"><span data-stu-id="07a51-211">False</span></span>                                                     |
| <span data-ttu-id="07a51-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="07a51-212">In Global Catalog</span></span>      | <span data-ttu-id="07a51-213">否</span><span class="sxs-lookup"><span data-stu-id="07a51-213">False</span></span>                                                     |
| <span data-ttu-id="07a51-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="07a51-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a51-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="07a51-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="07a51-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a51-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a51-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-218">Search-Flags</span></span>           | <span data-ttu-id="07a51-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a51-219">0x00000000</span></span>                                                |
| <span data-ttu-id="07a51-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-220">System-Flags</span></span>           | <span data-ttu-id="07a51-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a51-221">0x00000010</span></span>                                                |
| <span data-ttu-id="07a51-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="07a51-222">Classes used in</span></span>        | [<span data-ttu-id="07a51-223">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="07a51-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="07a51-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07a51-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="07a51-225">進入</span><span class="sxs-lookup"><span data-stu-id="07a51-225">Entry</span></span> | <span data-ttu-id="07a51-226">值</span><span class="sxs-lookup"><span data-stu-id="07a51-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="07a51-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="07a51-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a51-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a51-229">System-Only</span></span>            | <span data-ttu-id="07a51-230">否</span><span class="sxs-lookup"><span data-stu-id="07a51-230">False</span></span>                                                     |
| <span data-ttu-id="07a51-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="07a51-231">Is-Single-Valued</span></span>       | <span data-ttu-id="07a51-232">對</span><span class="sxs-lookup"><span data-stu-id="07a51-232">True</span></span>                                                      |
| <span data-ttu-id="07a51-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="07a51-233">Is Indexed</span></span>             | <span data-ttu-id="07a51-234">否</span><span class="sxs-lookup"><span data-stu-id="07a51-234">False</span></span>                                                     |
| <span data-ttu-id="07a51-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="07a51-235">In Global Catalog</span></span>      | <span data-ttu-id="07a51-236">否</span><span class="sxs-lookup"><span data-stu-id="07a51-236">False</span></span>                                                     |
| <span data-ttu-id="07a51-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="07a51-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a51-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="07a51-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="07a51-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a51-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a51-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-241">Search-Flags</span></span>           | <span data-ttu-id="07a51-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a51-242">0x00000000</span></span>                                                |
| <span data-ttu-id="07a51-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-243">System-Flags</span></span>           | <span data-ttu-id="07a51-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a51-244">0x00000010</span></span>                                                |
| <span data-ttu-id="07a51-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="07a51-245">Classes used in</span></span>        | [<span data-ttu-id="07a51-246">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="07a51-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="07a51-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07a51-247">Windows Server 2012</span></span>



| <span data-ttu-id="07a51-248">進入</span><span class="sxs-lookup"><span data-stu-id="07a51-248">Entry</span></span> | <span data-ttu-id="07a51-249">值</span><span class="sxs-lookup"><span data-stu-id="07a51-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="07a51-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="07a51-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a51-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="07a51-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a51-252">System-Only</span></span>            | <span data-ttu-id="07a51-253">否</span><span class="sxs-lookup"><span data-stu-id="07a51-253">False</span></span>                                                     |
| <span data-ttu-id="07a51-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="07a51-254">Is-Single-Valued</span></span>       | <span data-ttu-id="07a51-255">對</span><span class="sxs-lookup"><span data-stu-id="07a51-255">True</span></span>                                                      |
| <span data-ttu-id="07a51-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="07a51-256">Is Indexed</span></span>             | <span data-ttu-id="07a51-257">否</span><span class="sxs-lookup"><span data-stu-id="07a51-257">False</span></span>                                                     |
| <span data-ttu-id="07a51-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="07a51-258">In Global Catalog</span></span>      | <span data-ttu-id="07a51-259">否</span><span class="sxs-lookup"><span data-stu-id="07a51-259">False</span></span>                                                     |
| <span data-ttu-id="07a51-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="07a51-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a51-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="07a51-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="07a51-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a51-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a51-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="07a51-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-264">Search-Flags</span></span>           | <span data-ttu-id="07a51-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a51-265">0x00000000</span></span>                                                |
| <span data-ttu-id="07a51-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a51-266">System-Flags</span></span>           | <span data-ttu-id="07a51-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a51-267">0x00000010</span></span>                                                |
| <span data-ttu-id="07a51-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="07a51-268">Classes used in</span></span>        | [<span data-ttu-id="07a51-269">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="07a51-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





