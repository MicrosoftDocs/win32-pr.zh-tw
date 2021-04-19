---
title: InformationDirectory 屬性
description: SQL Server 目前實例的資訊目錄。
ms.assetid: fec29b94-b136-4862-8615-7190b3b45ec3
ms.tgt_platform: multiple
keywords:
- InformationDirectory 屬性 AD 架構
- InformationDirectory 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-InformationDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a5ca19d6c746e6e5874e82010fcbca367c1157
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106980302"
---
# <a name="ms-sql-informationdirectory-attribute"></a><span data-ttu-id="ef4bf-105">InformationDirectory 屬性</span><span class="sxs-lookup"><span data-stu-id="ef4bf-105">MS-SQL-InformationDirectory attribute</span></span>

<span data-ttu-id="ef4bf-106">SQL Server 目前實例的資訊目錄。</span><span class="sxs-lookup"><span data-stu-id="ef4bf-106">The informational directory for the current instance of SQL Server.</span></span>



| <span data-ttu-id="ef4bf-107">進入</span><span class="sxs-lookup"><span data-stu-id="ef4bf-107">Entry</span></span> | <span data-ttu-id="ef4bf-108">值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="ef4bf-109">CN</span><span class="sxs-lookup"><span data-stu-id="ef4bf-109">CN</span></span>                | <span data-ttu-id="ef4bf-110">InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="ef4bf-110">MS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="ef4bf-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ef4bf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ef4bf-112">InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="ef4bf-112">mS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="ef4bf-113">大小</span><span class="sxs-lookup"><span data-stu-id="ef4bf-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="ef4bf-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ef4bf-114">Update Privilege</span></span>  | <span data-ttu-id="ef4bf-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="ef4bf-115">Domain administrator</span></span>                     |
| <span data-ttu-id="ef4bf-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ef4bf-116">Update Frequency</span></span>  | <span data-ttu-id="ef4bf-117">當系統啟動或更新 AD 時。</span><span class="sxs-lookup"><span data-stu-id="ef4bf-117">At system startup or when AD is updated.</span></span> |
| <span data-ttu-id="ef4bf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ef4bf-118">Attribute-Id</span></span>      | <span data-ttu-id="ef4bf-119">1.2.840.113556.1.4.1392</span><span class="sxs-lookup"><span data-stu-id="ef4bf-119">1.2.840.113556.1.4.1392</span></span>                  |
| <span data-ttu-id="ef4bf-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ef4bf-120">System-Id-Guid</span></span>    | <span data-ttu-id="ef4bf-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ef4bf-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span></span>     |
| <span data-ttu-id="ef4bf-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef4bf-122">Syntax</span></span>            | [<span data-ttu-id="ef4bf-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-123">**Boolean**</span></span>](s-boolean.md)             |



## <a name="implementations"></a><span data-ttu-id="ef4bf-124">實作</span><span class="sxs-lookup"><span data-stu-id="ef4bf-124">Implementations</span></span>

-   [<span data-ttu-id="ef4bf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ef4bf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ef4bf-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ef4bf-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ef4bf-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ef4bf-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ef4bf-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef4bf-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ef4bf-132">進入</span><span class="sxs-lookup"><span data-stu-id="ef4bf-132">Entry</span></span> | <span data-ttu-id="ef4bf-133">值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ef4bf-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ef4bf-134">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef4bf-135">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef4bf-136">System-Only</span></span>            | <span data-ttu-id="ef4bf-137">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-137">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ef4bf-139">對</span><span class="sxs-lookup"><span data-stu-id="ef4bf-139">True</span></span>                                                              |
| <span data-ttu-id="ef4bf-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ef4bf-140">Is Indexed</span></span>             | <span data-ttu-id="ef4bf-141">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-141">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ef4bf-142">In Global Catalog</span></span>      | <span data-ttu-id="ef4bf-143">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-143">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ef4bf-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef4bf-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ef4bf-145">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ef4bf-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef4bf-146">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef4bf-147">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-148">Search-Flags</span></span>           | <span data-ttu-id="ef4bf-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef4bf-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="ef4bf-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-150">System-Flags</span></span>           | <span data-ttu-id="ef4bf-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef4bf-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="ef4bf-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ef4bf-152">Classes used in</span></span>        | [<span data-ttu-id="ef4bf-153">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-153">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ef4bf-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef4bf-154">Windows Server 2003</span></span>



| <span data-ttu-id="ef4bf-155">進入</span><span class="sxs-lookup"><span data-stu-id="ef4bf-155">Entry</span></span> | <span data-ttu-id="ef4bf-156">值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ef4bf-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ef4bf-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef4bf-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef4bf-159">System-Only</span></span>            | <span data-ttu-id="ef4bf-160">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-160">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ef4bf-162">對</span><span class="sxs-lookup"><span data-stu-id="ef4bf-162">True</span></span>                                                              |
| <span data-ttu-id="ef4bf-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ef4bf-163">Is Indexed</span></span>             | <span data-ttu-id="ef4bf-164">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-164">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ef4bf-165">In Global Catalog</span></span>      | <span data-ttu-id="ef4bf-166">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-166">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ef4bf-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef4bf-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ef4bf-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ef4bf-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef4bf-169">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef4bf-170">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-171">Search-Flags</span></span>           | <span data-ttu-id="ef4bf-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef4bf-172">0x00000000</span></span>                                                        |
| <span data-ttu-id="ef4bf-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-173">System-Flags</span></span>           | <span data-ttu-id="ef4bf-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef4bf-174">0x00000010</span></span>                                                        |
| <span data-ttu-id="ef4bf-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ef4bf-175">Classes used in</span></span>        | [<span data-ttu-id="ef4bf-176">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-176">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ef4bf-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ef4bf-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ef4bf-178">進入</span><span class="sxs-lookup"><span data-stu-id="ef4bf-178">Entry</span></span> | <span data-ttu-id="ef4bf-179">值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ef4bf-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ef4bf-180">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef4bf-181">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef4bf-182">System-Only</span></span>            | <span data-ttu-id="ef4bf-183">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-183">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ef4bf-185">對</span><span class="sxs-lookup"><span data-stu-id="ef4bf-185">True</span></span>                                                              |
| <span data-ttu-id="ef4bf-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ef4bf-186">Is Indexed</span></span>             | <span data-ttu-id="ef4bf-187">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-187">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ef4bf-188">In Global Catalog</span></span>      | <span data-ttu-id="ef4bf-189">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-189">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ef4bf-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef4bf-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ef4bf-191">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ef4bf-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef4bf-192">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef4bf-193">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-194">Search-Flags</span></span>           | <span data-ttu-id="ef4bf-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef4bf-195">0x00000000</span></span>                                                        |
| <span data-ttu-id="ef4bf-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-196">System-Flags</span></span>           | <span data-ttu-id="ef4bf-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef4bf-197">0x00000010</span></span>                                                        |
| <span data-ttu-id="ef4bf-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ef4bf-198">Classes used in</span></span>        | [<span data-ttu-id="ef4bf-199">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-199">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ef4bf-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef4bf-200">Windows Server 2008</span></span>



| <span data-ttu-id="ef4bf-201">進入</span><span class="sxs-lookup"><span data-stu-id="ef4bf-201">Entry</span></span> | <span data-ttu-id="ef4bf-202">值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ef4bf-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ef4bf-203">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef4bf-204">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef4bf-205">System-Only</span></span>            | <span data-ttu-id="ef4bf-206">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-206">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ef4bf-208">對</span><span class="sxs-lookup"><span data-stu-id="ef4bf-208">True</span></span>                                                              |
| <span data-ttu-id="ef4bf-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ef4bf-209">Is Indexed</span></span>             | <span data-ttu-id="ef4bf-210">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-210">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ef4bf-211">In Global Catalog</span></span>      | <span data-ttu-id="ef4bf-212">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-212">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ef4bf-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef4bf-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ef4bf-214">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ef4bf-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef4bf-215">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef4bf-216">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-217">Search-Flags</span></span>           | <span data-ttu-id="ef4bf-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef4bf-218">0x00000000</span></span>                                                        |
| <span data-ttu-id="ef4bf-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-219">System-Flags</span></span>           | <span data-ttu-id="ef4bf-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef4bf-220">0x00000010</span></span>                                                        |
| <span data-ttu-id="ef4bf-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ef4bf-221">Classes used in</span></span>        | [<span data-ttu-id="ef4bf-222">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-222">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ef4bf-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef4bf-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ef4bf-224">進入</span><span class="sxs-lookup"><span data-stu-id="ef4bf-224">Entry</span></span> | <span data-ttu-id="ef4bf-225">值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ef4bf-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ef4bf-226">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef4bf-227">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef4bf-228">System-Only</span></span>            | <span data-ttu-id="ef4bf-229">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-229">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ef4bf-231">對</span><span class="sxs-lookup"><span data-stu-id="ef4bf-231">True</span></span>                                                              |
| <span data-ttu-id="ef4bf-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ef4bf-232">Is Indexed</span></span>             | <span data-ttu-id="ef4bf-233">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-233">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ef4bf-234">In Global Catalog</span></span>      | <span data-ttu-id="ef4bf-235">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-235">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ef4bf-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef4bf-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ef4bf-237">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ef4bf-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef4bf-238">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef4bf-239">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-240">Search-Flags</span></span>           | <span data-ttu-id="ef4bf-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef4bf-241">0x00000000</span></span>                                                        |
| <span data-ttu-id="ef4bf-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-242">System-Flags</span></span>           | <span data-ttu-id="ef4bf-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef4bf-243">0x00000010</span></span>                                                        |
| <span data-ttu-id="ef4bf-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ef4bf-244">Classes used in</span></span>        | [<span data-ttu-id="ef4bf-245">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-245">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ef4bf-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef4bf-246">Windows Server 2012</span></span>



| <span data-ttu-id="ef4bf-247">進入</span><span class="sxs-lookup"><span data-stu-id="ef4bf-247">Entry</span></span> | <span data-ttu-id="ef4bf-248">值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-248">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ef4bf-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ef4bf-249">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef4bf-250">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ef4bf-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef4bf-251">System-Only</span></span>            | <span data-ttu-id="ef4bf-252">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-252">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ef4bf-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ef4bf-254">對</span><span class="sxs-lookup"><span data-stu-id="ef4bf-254">True</span></span>                                                              |
| <span data-ttu-id="ef4bf-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ef4bf-255">Is Indexed</span></span>             | <span data-ttu-id="ef4bf-256">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-256">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ef4bf-257">In Global Catalog</span></span>      | <span data-ttu-id="ef4bf-258">否</span><span class="sxs-lookup"><span data-stu-id="ef4bf-258">False</span></span>                                                             |
| <span data-ttu-id="ef4bf-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ef4bf-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef4bf-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ef4bf-260">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ef4bf-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef4bf-261">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef4bf-262">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ef4bf-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-263">Search-Flags</span></span>           | <span data-ttu-id="ef4bf-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef4bf-264">0x00000000</span></span>                                                        |
| <span data-ttu-id="ef4bf-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef4bf-265">System-Flags</span></span>           | <span data-ttu-id="ef4bf-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef4bf-266">0x00000010</span></span>                                                        |
| <span data-ttu-id="ef4bf-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ef4bf-267">Classes used in</span></span>        | [<span data-ttu-id="ef4bf-268">**SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="ef4bf-268">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





