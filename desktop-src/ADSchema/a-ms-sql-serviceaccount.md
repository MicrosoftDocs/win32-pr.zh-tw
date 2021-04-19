---
title: ServiceAccount 屬性
description: 使用者定義的字串。 預設值設定為 ServiceAccount。
ms.assetid: 0db095c8-8492-45c0-b509-d4082cec2c13
ms.tgt_platform: multiple
keywords:
- ServiceAccount 屬性 AD 架構
- ServiceAccount 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-ServiceAccount
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab96de3d56dedd3178e579e100f00b77df4edb7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970024"
---
# <a name="ms-sql-serviceaccount-attribute"></a><span data-ttu-id="668eb-106">ServiceAccount 屬性</span><span class="sxs-lookup"><span data-stu-id="668eb-106">MS-SQL-ServiceAccount attribute</span></span>

<span data-ttu-id="668eb-107">使用者定義的字串。</span><span class="sxs-lookup"><span data-stu-id="668eb-107">A user defined string.</span></span> <span data-ttu-id="668eb-108">預設值設定為 ServiceAccount。</span><span class="sxs-lookup"><span data-stu-id="668eb-108">The default is set to ServiceAccount.</span></span>



| <span data-ttu-id="668eb-109">進入</span><span class="sxs-lookup"><span data-stu-id="668eb-109">Entry</span></span> | <span data-ttu-id="668eb-110">值</span><span class="sxs-lookup"><span data-stu-id="668eb-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="668eb-111">CN</span><span class="sxs-lookup"><span data-stu-id="668eb-111">CN</span></span>                | <span data-ttu-id="668eb-112">ServiceAccount</span><span class="sxs-lookup"><span data-stu-id="668eb-112">MS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="668eb-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="668eb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="668eb-114">ServiceAccount</span><span class="sxs-lookup"><span data-stu-id="668eb-114">mS-SQL-ServiceAccount</span></span>                       |
| <span data-ttu-id="668eb-115">大小</span><span class="sxs-lookup"><span data-stu-id="668eb-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="668eb-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="668eb-116">Update Privilege</span></span>  | <span data-ttu-id="668eb-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="668eb-117">Domain administrator</span></span>                        |
| <span data-ttu-id="668eb-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="668eb-118">Update Frequency</span></span>  | <span data-ttu-id="668eb-119">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="668eb-119">At system setup.</span></span>                            |
| <span data-ttu-id="668eb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="668eb-120">Attribute-Id</span></span>      | <span data-ttu-id="668eb-121">1.2.840.113556.1.4.1369</span><span class="sxs-lookup"><span data-stu-id="668eb-121">1.2.840.113556.1.4.1369</span></span>                     |
| <span data-ttu-id="668eb-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="668eb-122">System-Id-Guid</span></span>    | <span data-ttu-id="668eb-123">64933a3e-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="668eb-123">64933a3e-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="668eb-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="668eb-124">Syntax</span></span>            | [<span data-ttu-id="668eb-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="668eb-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="668eb-126">實作</span><span class="sxs-lookup"><span data-stu-id="668eb-126">Implementations</span></span>

-   [<span data-ttu-id="668eb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="668eb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="668eb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="668eb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="668eb-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="668eb-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="668eb-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="668eb-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="668eb-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="668eb-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="668eb-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="668eb-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="668eb-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="668eb-133">Windows 2000 Server</span></span>



| <span data-ttu-id="668eb-134">進入</span><span class="sxs-lookup"><span data-stu-id="668eb-134">Entry</span></span> | <span data-ttu-id="668eb-135">值</span><span class="sxs-lookup"><span data-stu-id="668eb-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668eb-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="668eb-136">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="668eb-137">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="668eb-138">System-Only</span></span>            | <span data-ttu-id="668eb-139">否</span><span class="sxs-lookup"><span data-stu-id="668eb-139">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="668eb-140">Is-Single-Valued</span></span>       | <span data-ttu-id="668eb-141">對</span><span class="sxs-lookup"><span data-stu-id="668eb-141">True</span></span>                                                                                                                  |
| <span data-ttu-id="668eb-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="668eb-142">Is Indexed</span></span>             | <span data-ttu-id="668eb-143">否</span><span class="sxs-lookup"><span data-stu-id="668eb-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="668eb-144">In Global Catalog</span></span>      | <span data-ttu-id="668eb-145">否</span><span class="sxs-lookup"><span data-stu-id="668eb-145">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="668eb-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="668eb-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="668eb-147">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="668eb-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="668eb-148">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="668eb-149">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-150">Search-Flags</span></span>           | <span data-ttu-id="668eb-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="668eb-151">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="668eb-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-152">System-Flags</span></span>           | <span data-ttu-id="668eb-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="668eb-153">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="668eb-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="668eb-154">Classes used in</span></span>        | [<span data-ttu-id="668eb-155">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="668eb-155">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="668eb-156">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="668eb-156">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="668eb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="668eb-157">Windows Server 2003</span></span>



| <span data-ttu-id="668eb-158">進入</span><span class="sxs-lookup"><span data-stu-id="668eb-158">Entry</span></span> | <span data-ttu-id="668eb-159">值</span><span class="sxs-lookup"><span data-stu-id="668eb-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668eb-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="668eb-160">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="668eb-161">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="668eb-162">System-Only</span></span>            | <span data-ttu-id="668eb-163">否</span><span class="sxs-lookup"><span data-stu-id="668eb-163">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="668eb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="668eb-165">對</span><span class="sxs-lookup"><span data-stu-id="668eb-165">True</span></span>                                                                                                                  |
| <span data-ttu-id="668eb-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="668eb-166">Is Indexed</span></span>             | <span data-ttu-id="668eb-167">否</span><span class="sxs-lookup"><span data-stu-id="668eb-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="668eb-168">In Global Catalog</span></span>      | <span data-ttu-id="668eb-169">否</span><span class="sxs-lookup"><span data-stu-id="668eb-169">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="668eb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="668eb-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="668eb-171">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="668eb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="668eb-172">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="668eb-173">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-174">Search-Flags</span></span>           | <span data-ttu-id="668eb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="668eb-175">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="668eb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-176">System-Flags</span></span>           | <span data-ttu-id="668eb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="668eb-177">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="668eb-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="668eb-178">Classes used in</span></span>        | [<span data-ttu-id="668eb-179">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="668eb-179">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="668eb-180">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="668eb-180">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="668eb-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="668eb-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="668eb-182">進入</span><span class="sxs-lookup"><span data-stu-id="668eb-182">Entry</span></span> | <span data-ttu-id="668eb-183">值</span><span class="sxs-lookup"><span data-stu-id="668eb-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668eb-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="668eb-184">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="668eb-185">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="668eb-186">System-Only</span></span>            | <span data-ttu-id="668eb-187">否</span><span class="sxs-lookup"><span data-stu-id="668eb-187">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="668eb-188">Is-Single-Valued</span></span>       | <span data-ttu-id="668eb-189">對</span><span class="sxs-lookup"><span data-stu-id="668eb-189">True</span></span>                                                                                                                  |
| <span data-ttu-id="668eb-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="668eb-190">Is Indexed</span></span>             | <span data-ttu-id="668eb-191">否</span><span class="sxs-lookup"><span data-stu-id="668eb-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="668eb-192">In Global Catalog</span></span>      | <span data-ttu-id="668eb-193">否</span><span class="sxs-lookup"><span data-stu-id="668eb-193">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="668eb-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="668eb-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="668eb-195">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="668eb-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="668eb-196">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="668eb-197">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-198">Search-Flags</span></span>           | <span data-ttu-id="668eb-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="668eb-199">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="668eb-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-200">System-Flags</span></span>           | <span data-ttu-id="668eb-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="668eb-201">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="668eb-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="668eb-202">Classes used in</span></span>        | [<span data-ttu-id="668eb-203">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="668eb-203">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="668eb-204">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="668eb-204">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="668eb-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="668eb-205">Windows Server 2008</span></span>



| <span data-ttu-id="668eb-206">進入</span><span class="sxs-lookup"><span data-stu-id="668eb-206">Entry</span></span> | <span data-ttu-id="668eb-207">值</span><span class="sxs-lookup"><span data-stu-id="668eb-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668eb-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="668eb-208">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="668eb-209">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="668eb-210">System-Only</span></span>            | <span data-ttu-id="668eb-211">否</span><span class="sxs-lookup"><span data-stu-id="668eb-211">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="668eb-212">Is-Single-Valued</span></span>       | <span data-ttu-id="668eb-213">對</span><span class="sxs-lookup"><span data-stu-id="668eb-213">True</span></span>                                                                                                                  |
| <span data-ttu-id="668eb-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="668eb-214">Is Indexed</span></span>             | <span data-ttu-id="668eb-215">否</span><span class="sxs-lookup"><span data-stu-id="668eb-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="668eb-216">In Global Catalog</span></span>      | <span data-ttu-id="668eb-217">否</span><span class="sxs-lookup"><span data-stu-id="668eb-217">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="668eb-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="668eb-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="668eb-219">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="668eb-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="668eb-220">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="668eb-221">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-222">Search-Flags</span></span>           | <span data-ttu-id="668eb-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="668eb-223">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="668eb-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-224">System-Flags</span></span>           | <span data-ttu-id="668eb-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="668eb-225">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="668eb-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="668eb-226">Classes used in</span></span>        | [<span data-ttu-id="668eb-227">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="668eb-227">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="668eb-228">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="668eb-228">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="668eb-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="668eb-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="668eb-230">進入</span><span class="sxs-lookup"><span data-stu-id="668eb-230">Entry</span></span> | <span data-ttu-id="668eb-231">值</span><span class="sxs-lookup"><span data-stu-id="668eb-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668eb-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="668eb-232">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="668eb-233">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="668eb-234">System-Only</span></span>            | <span data-ttu-id="668eb-235">否</span><span class="sxs-lookup"><span data-stu-id="668eb-235">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="668eb-236">Is-Single-Valued</span></span>       | <span data-ttu-id="668eb-237">對</span><span class="sxs-lookup"><span data-stu-id="668eb-237">True</span></span>                                                                                                                  |
| <span data-ttu-id="668eb-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="668eb-238">Is Indexed</span></span>             | <span data-ttu-id="668eb-239">否</span><span class="sxs-lookup"><span data-stu-id="668eb-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="668eb-240">In Global Catalog</span></span>      | <span data-ttu-id="668eb-241">否</span><span class="sxs-lookup"><span data-stu-id="668eb-241">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="668eb-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="668eb-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="668eb-243">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="668eb-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="668eb-244">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="668eb-245">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-246">Search-Flags</span></span>           | <span data-ttu-id="668eb-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="668eb-247">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="668eb-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-248">System-Flags</span></span>           | <span data-ttu-id="668eb-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="668eb-249">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="668eb-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="668eb-250">Classes used in</span></span>        | [<span data-ttu-id="668eb-251">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="668eb-251">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="668eb-252">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="668eb-252">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="668eb-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="668eb-253">Windows Server 2012</span></span>



| <span data-ttu-id="668eb-254">進入</span><span class="sxs-lookup"><span data-stu-id="668eb-254">Entry</span></span> | <span data-ttu-id="668eb-255">值</span><span class="sxs-lookup"><span data-stu-id="668eb-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668eb-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="668eb-256">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="668eb-257">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="668eb-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="668eb-258">System-Only</span></span>            | <span data-ttu-id="668eb-259">否</span><span class="sxs-lookup"><span data-stu-id="668eb-259">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="668eb-260">Is-Single-Valued</span></span>       | <span data-ttu-id="668eb-261">對</span><span class="sxs-lookup"><span data-stu-id="668eb-261">True</span></span>                                                                                                                  |
| <span data-ttu-id="668eb-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="668eb-262">Is Indexed</span></span>             | <span data-ttu-id="668eb-263">否</span><span class="sxs-lookup"><span data-stu-id="668eb-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="668eb-264">In Global Catalog</span></span>      | <span data-ttu-id="668eb-265">否</span><span class="sxs-lookup"><span data-stu-id="668eb-265">False</span></span>                                                                                                                 |
| <span data-ttu-id="668eb-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="668eb-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="668eb-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="668eb-267">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="668eb-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="668eb-268">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="668eb-269">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="668eb-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-270">Search-Flags</span></span>           | <span data-ttu-id="668eb-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="668eb-271">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="668eb-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="668eb-272">System-Flags</span></span>           | <span data-ttu-id="668eb-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="668eb-273">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="668eb-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="668eb-274">Classes used in</span></span>        | [<span data-ttu-id="668eb-275">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="668eb-275">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="668eb-276">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="668eb-276">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





