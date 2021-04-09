---
title: MS-CHAP-Alias 屬性
description: 用來連接到資料庫的別名。 預設值設定為 [別名]。
ms.assetid: d129813c-9871-4ed5-968a-b05ab2b96f10
ms.tgt_platform: multiple
keywords:
- MS-SQL-Alias 屬性 AD 架構
- mS-SQL-Alias 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Alias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31d32697534a2a01358dc9cb724760588687f6f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686843"
---
# <a name="ms-sql-alias-attribute"></a><span data-ttu-id="59e7c-106">MS-CHAP-Alias 屬性</span><span class="sxs-lookup"><span data-stu-id="59e7c-106">MS-SQL-Alias attribute</span></span>

<span data-ttu-id="59e7c-107">用來連接到資料庫的別名。</span><span class="sxs-lookup"><span data-stu-id="59e7c-107">An alias used to connect to the database.</span></span> <span data-ttu-id="59e7c-108">預設值設定為 [別名]。</span><span class="sxs-lookup"><span data-stu-id="59e7c-108">Default is set to Alias.</span></span>



| <span data-ttu-id="59e7c-109">進入</span><span class="sxs-lookup"><span data-stu-id="59e7c-109">Entry</span></span> | <span data-ttu-id="59e7c-110">值</span><span class="sxs-lookup"><span data-stu-id="59e7c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="59e7c-111">CN</span><span class="sxs-lookup"><span data-stu-id="59e7c-111">CN</span></span>                | <span data-ttu-id="59e7c-112">MS-SQL-別名</span><span class="sxs-lookup"><span data-stu-id="59e7c-112">MS-SQL-Alias</span></span>                                |
| <span data-ttu-id="59e7c-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="59e7c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="59e7c-114">mS-SQL-別名</span><span class="sxs-lookup"><span data-stu-id="59e7c-114">mS-SQL-Alias</span></span>                                |
| <span data-ttu-id="59e7c-115">大小</span><span class="sxs-lookup"><span data-stu-id="59e7c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="59e7c-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="59e7c-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="59e7c-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="59e7c-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="59e7c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="59e7c-118">Attribute-Id</span></span>      | <span data-ttu-id="59e7c-119">1.2.840.113556.1.4.1395</span><span class="sxs-lookup"><span data-stu-id="59e7c-119">1.2.840.113556.1.4.1395</span></span>                     |
| <span data-ttu-id="59e7c-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="59e7c-120">System-Id-Guid</span></span>    | <span data-ttu-id="59e7c-121">e0c6baae-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="59e7c-121">e0c6baae-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="59e7c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="59e7c-122">Syntax</span></span>            | [<span data-ttu-id="59e7c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="59e7c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="59e7c-124">實作</span><span class="sxs-lookup"><span data-stu-id="59e7c-124">Implementations</span></span>

-   [<span data-ttu-id="59e7c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="59e7c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="59e7c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="59e7c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="59e7c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="59e7c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="59e7c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="59e7c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="59e7c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="59e7c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="59e7c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="59e7c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="59e7c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59e7c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="59e7c-132">進入</span><span class="sxs-lookup"><span data-stu-id="59e7c-132">Entry</span></span> | <span data-ttu-id="59e7c-133">值</span><span class="sxs-lookup"><span data-stu-id="59e7c-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="59e7c-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="59e7c-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59e7c-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="59e7c-136">System-Only</span></span>            | <span data-ttu-id="59e7c-137">否</span><span class="sxs-lookup"><span data-stu-id="59e7c-137">False</span></span>                                                         |
| <span data-ttu-id="59e7c-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="59e7c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="59e7c-139">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-139">True</span></span>                                                          |
| <span data-ttu-id="59e7c-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="59e7c-140">Is Indexed</span></span>             | <span data-ttu-id="59e7c-141">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-141">True</span></span>                                                          |
| <span data-ttu-id="59e7c-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="59e7c-142">In Global Catalog</span></span>      | <span data-ttu-id="59e7c-143">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-143">True</span></span>                                                          |
| <span data-ttu-id="59e7c-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="59e7c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="59e7c-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="59e7c-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="59e7c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59e7c-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59e7c-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-148">Search-Flags</span></span>           | <span data-ttu-id="59e7c-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59e7c-149">0x00000001</span></span>                                                    |
| <span data-ttu-id="59e7c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-150">System-Flags</span></span>           | <span data-ttu-id="59e7c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59e7c-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="59e7c-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="59e7c-152">Classes used in</span></span>        | [<span data-ttu-id="59e7c-153">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="59e7c-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="59e7c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59e7c-154">Windows Server 2003</span></span>



| <span data-ttu-id="59e7c-155">進入</span><span class="sxs-lookup"><span data-stu-id="59e7c-155">Entry</span></span> | <span data-ttu-id="59e7c-156">值</span><span class="sxs-lookup"><span data-stu-id="59e7c-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="59e7c-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="59e7c-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59e7c-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="59e7c-159">System-Only</span></span>            | <span data-ttu-id="59e7c-160">否</span><span class="sxs-lookup"><span data-stu-id="59e7c-160">False</span></span>                                                         |
| <span data-ttu-id="59e7c-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="59e7c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="59e7c-162">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-162">True</span></span>                                                          |
| <span data-ttu-id="59e7c-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="59e7c-163">Is Indexed</span></span>             | <span data-ttu-id="59e7c-164">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-164">True</span></span>                                                          |
| <span data-ttu-id="59e7c-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="59e7c-165">In Global Catalog</span></span>      | <span data-ttu-id="59e7c-166">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-166">True</span></span>                                                          |
| <span data-ttu-id="59e7c-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="59e7c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="59e7c-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="59e7c-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="59e7c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59e7c-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59e7c-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-171">Search-Flags</span></span>           | <span data-ttu-id="59e7c-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59e7c-172">0x00000001</span></span>                                                    |
| <span data-ttu-id="59e7c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-173">System-Flags</span></span>           | <span data-ttu-id="59e7c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59e7c-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="59e7c-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="59e7c-175">Classes used in</span></span>        | [<span data-ttu-id="59e7c-176">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="59e7c-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="59e7c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="59e7c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="59e7c-178">進入</span><span class="sxs-lookup"><span data-stu-id="59e7c-178">Entry</span></span> | <span data-ttu-id="59e7c-179">值</span><span class="sxs-lookup"><span data-stu-id="59e7c-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="59e7c-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="59e7c-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59e7c-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="59e7c-182">System-Only</span></span>            | <span data-ttu-id="59e7c-183">否</span><span class="sxs-lookup"><span data-stu-id="59e7c-183">False</span></span>                                                         |
| <span data-ttu-id="59e7c-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="59e7c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="59e7c-185">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-185">True</span></span>                                                          |
| <span data-ttu-id="59e7c-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="59e7c-186">Is Indexed</span></span>             | <span data-ttu-id="59e7c-187">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-187">True</span></span>                                                          |
| <span data-ttu-id="59e7c-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="59e7c-188">In Global Catalog</span></span>      | <span data-ttu-id="59e7c-189">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-189">True</span></span>                                                          |
| <span data-ttu-id="59e7c-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="59e7c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="59e7c-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="59e7c-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="59e7c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59e7c-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59e7c-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-194">Search-Flags</span></span>           | <span data-ttu-id="59e7c-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59e7c-195">0x00000001</span></span>                                                    |
| <span data-ttu-id="59e7c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-196">System-Flags</span></span>           | <span data-ttu-id="59e7c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59e7c-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="59e7c-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="59e7c-198">Classes used in</span></span>        | [<span data-ttu-id="59e7c-199">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="59e7c-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="59e7c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59e7c-200">Windows Server 2008</span></span>



| <span data-ttu-id="59e7c-201">進入</span><span class="sxs-lookup"><span data-stu-id="59e7c-201">Entry</span></span> | <span data-ttu-id="59e7c-202">值</span><span class="sxs-lookup"><span data-stu-id="59e7c-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="59e7c-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="59e7c-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59e7c-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="59e7c-205">System-Only</span></span>            | <span data-ttu-id="59e7c-206">否</span><span class="sxs-lookup"><span data-stu-id="59e7c-206">False</span></span>                                                         |
| <span data-ttu-id="59e7c-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="59e7c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="59e7c-208">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-208">True</span></span>                                                          |
| <span data-ttu-id="59e7c-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="59e7c-209">Is Indexed</span></span>             | <span data-ttu-id="59e7c-210">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-210">True</span></span>                                                          |
| <span data-ttu-id="59e7c-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="59e7c-211">In Global Catalog</span></span>      | <span data-ttu-id="59e7c-212">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-212">True</span></span>                                                          |
| <span data-ttu-id="59e7c-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="59e7c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="59e7c-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="59e7c-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="59e7c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59e7c-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59e7c-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-217">Search-Flags</span></span>           | <span data-ttu-id="59e7c-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59e7c-218">0x00000001</span></span>                                                    |
| <span data-ttu-id="59e7c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-219">System-Flags</span></span>           | <span data-ttu-id="59e7c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59e7c-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="59e7c-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="59e7c-221">Classes used in</span></span>        | [<span data-ttu-id="59e7c-222">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="59e7c-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="59e7c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59e7c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="59e7c-224">進入</span><span class="sxs-lookup"><span data-stu-id="59e7c-224">Entry</span></span> | <span data-ttu-id="59e7c-225">值</span><span class="sxs-lookup"><span data-stu-id="59e7c-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="59e7c-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="59e7c-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59e7c-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="59e7c-228">System-Only</span></span>            | <span data-ttu-id="59e7c-229">否</span><span class="sxs-lookup"><span data-stu-id="59e7c-229">False</span></span>                                                         |
| <span data-ttu-id="59e7c-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="59e7c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="59e7c-231">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-231">True</span></span>                                                          |
| <span data-ttu-id="59e7c-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="59e7c-232">Is Indexed</span></span>             | <span data-ttu-id="59e7c-233">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-233">True</span></span>                                                          |
| <span data-ttu-id="59e7c-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="59e7c-234">In Global Catalog</span></span>      | <span data-ttu-id="59e7c-235">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-235">True</span></span>                                                          |
| <span data-ttu-id="59e7c-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="59e7c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="59e7c-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="59e7c-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="59e7c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59e7c-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59e7c-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-240">Search-Flags</span></span>           | <span data-ttu-id="59e7c-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59e7c-241">0x00000001</span></span>                                                    |
| <span data-ttu-id="59e7c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-242">System-Flags</span></span>           | <span data-ttu-id="59e7c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59e7c-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="59e7c-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="59e7c-244">Classes used in</span></span>        | [<span data-ttu-id="59e7c-245">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="59e7c-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="59e7c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59e7c-246">Windows Server 2012</span></span>



| <span data-ttu-id="59e7c-247">進入</span><span class="sxs-lookup"><span data-stu-id="59e7c-247">Entry</span></span> | <span data-ttu-id="59e7c-248">值</span><span class="sxs-lookup"><span data-stu-id="59e7c-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="59e7c-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="59e7c-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59e7c-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="59e7c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="59e7c-251">System-Only</span></span>            | <span data-ttu-id="59e7c-252">否</span><span class="sxs-lookup"><span data-stu-id="59e7c-252">False</span></span>                                                         |
| <span data-ttu-id="59e7c-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="59e7c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="59e7c-254">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-254">True</span></span>                                                          |
| <span data-ttu-id="59e7c-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="59e7c-255">Is Indexed</span></span>             | <span data-ttu-id="59e7c-256">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-256">True</span></span>                                                          |
| <span data-ttu-id="59e7c-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="59e7c-257">In Global Catalog</span></span>      | <span data-ttu-id="59e7c-258">對</span><span class="sxs-lookup"><span data-stu-id="59e7c-258">True</span></span>                                                          |
| <span data-ttu-id="59e7c-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="59e7c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="59e7c-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="59e7c-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="59e7c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59e7c-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59e7c-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="59e7c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-263">Search-Flags</span></span>           | <span data-ttu-id="59e7c-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="59e7c-264">0x00000001</span></span>                                                    |
| <span data-ttu-id="59e7c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59e7c-265">System-Flags</span></span>           | <span data-ttu-id="59e7c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59e7c-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="59e7c-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="59e7c-267">Classes used in</span></span>        | [<span data-ttu-id="59e7c-268">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="59e7c-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





