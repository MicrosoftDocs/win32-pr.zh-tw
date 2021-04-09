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
# <a name="ms-sql-alias-attribute"></a><span data-ttu-id="4edd7-106">MS-CHAP-Alias 屬性</span><span class="sxs-lookup"><span data-stu-id="4edd7-106">MS-SQL-Alias attribute</span></span>

<span data-ttu-id="4edd7-107">用來連接到資料庫的別名。</span><span class="sxs-lookup"><span data-stu-id="4edd7-107">An alias used to connect to the database.</span></span> <span data-ttu-id="4edd7-108">預設值設定為 [別名]。</span><span class="sxs-lookup"><span data-stu-id="4edd7-108">Default is set to Alias.</span></span>



| <span data-ttu-id="4edd7-109">進入</span><span class="sxs-lookup"><span data-stu-id="4edd7-109">Entry</span></span> | <span data-ttu-id="4edd7-110">值</span><span class="sxs-lookup"><span data-stu-id="4edd7-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4edd7-111">CN</span><span class="sxs-lookup"><span data-stu-id="4edd7-111">CN</span></span>                | <span data-ttu-id="4edd7-112">MS-SQL-別名</span><span class="sxs-lookup"><span data-stu-id="4edd7-112">MS-SQL-Alias</span></span>                                |
| <span data-ttu-id="4edd7-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4edd7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4edd7-114">mS-SQL-別名</span><span class="sxs-lookup"><span data-stu-id="4edd7-114">mS-SQL-Alias</span></span>                                |
| <span data-ttu-id="4edd7-115">大小</span><span class="sxs-lookup"><span data-stu-id="4edd7-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="4edd7-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4edd7-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4edd7-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4edd7-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4edd7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4edd7-118">Attribute-Id</span></span>      | <span data-ttu-id="4edd7-119">1.2.840.113556.1.4.1395</span><span class="sxs-lookup"><span data-stu-id="4edd7-119">1.2.840.113556.1.4.1395</span></span>                     |
| <span data-ttu-id="4edd7-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4edd7-120">System-Id-Guid</span></span>    | <span data-ttu-id="4edd7-121">e0c6baae-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="4edd7-121">e0c6baae-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="4edd7-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4edd7-122">Syntax</span></span>            | [<span data-ttu-id="4edd7-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4edd7-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4edd7-124">實作</span><span class="sxs-lookup"><span data-stu-id="4edd7-124">Implementations</span></span>

-   [<span data-ttu-id="4edd7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4edd7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4edd7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4edd7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4edd7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4edd7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4edd7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4edd7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4edd7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4edd7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4edd7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4edd7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4edd7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4edd7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4edd7-132">進入</span><span class="sxs-lookup"><span data-stu-id="4edd7-132">Entry</span></span> | <span data-ttu-id="4edd7-133">值</span><span class="sxs-lookup"><span data-stu-id="4edd7-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4edd7-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4edd7-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4edd7-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4edd7-136">System-Only</span></span>            | <span data-ttu-id="4edd7-137">否</span><span class="sxs-lookup"><span data-stu-id="4edd7-137">False</span></span>                                                         |
| <span data-ttu-id="4edd7-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4edd7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4edd7-139">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-139">True</span></span>                                                          |
| <span data-ttu-id="4edd7-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4edd7-140">Is Indexed</span></span>             | <span data-ttu-id="4edd7-141">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-141">True</span></span>                                                          |
| <span data-ttu-id="4edd7-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4edd7-142">In Global Catalog</span></span>      | <span data-ttu-id="4edd7-143">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-143">True</span></span>                                                          |
| <span data-ttu-id="4edd7-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4edd7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4edd7-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4edd7-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4edd7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4edd7-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4edd7-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-148">Search-Flags</span></span>           | <span data-ttu-id="4edd7-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4edd7-149">0x00000001</span></span>                                                    |
| <span data-ttu-id="4edd7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-150">System-Flags</span></span>           | <span data-ttu-id="4edd7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4edd7-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="4edd7-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4edd7-152">Classes used in</span></span>        | [<span data-ttu-id="4edd7-153">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="4edd7-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4edd7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4edd7-154">Windows Server 2003</span></span>



| <span data-ttu-id="4edd7-155">進入</span><span class="sxs-lookup"><span data-stu-id="4edd7-155">Entry</span></span> | <span data-ttu-id="4edd7-156">值</span><span class="sxs-lookup"><span data-stu-id="4edd7-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4edd7-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4edd7-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4edd7-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4edd7-159">System-Only</span></span>            | <span data-ttu-id="4edd7-160">否</span><span class="sxs-lookup"><span data-stu-id="4edd7-160">False</span></span>                                                         |
| <span data-ttu-id="4edd7-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4edd7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4edd7-162">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-162">True</span></span>                                                          |
| <span data-ttu-id="4edd7-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4edd7-163">Is Indexed</span></span>             | <span data-ttu-id="4edd7-164">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-164">True</span></span>                                                          |
| <span data-ttu-id="4edd7-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4edd7-165">In Global Catalog</span></span>      | <span data-ttu-id="4edd7-166">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-166">True</span></span>                                                          |
| <span data-ttu-id="4edd7-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4edd7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4edd7-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4edd7-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4edd7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4edd7-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4edd7-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-171">Search-Flags</span></span>           | <span data-ttu-id="4edd7-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4edd7-172">0x00000001</span></span>                                                    |
| <span data-ttu-id="4edd7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-173">System-Flags</span></span>           | <span data-ttu-id="4edd7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4edd7-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="4edd7-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4edd7-175">Classes used in</span></span>        | [<span data-ttu-id="4edd7-176">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="4edd7-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4edd7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4edd7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4edd7-178">進入</span><span class="sxs-lookup"><span data-stu-id="4edd7-178">Entry</span></span> | <span data-ttu-id="4edd7-179">值</span><span class="sxs-lookup"><span data-stu-id="4edd7-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4edd7-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4edd7-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4edd7-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4edd7-182">System-Only</span></span>            | <span data-ttu-id="4edd7-183">否</span><span class="sxs-lookup"><span data-stu-id="4edd7-183">False</span></span>                                                         |
| <span data-ttu-id="4edd7-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4edd7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4edd7-185">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-185">True</span></span>                                                          |
| <span data-ttu-id="4edd7-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4edd7-186">Is Indexed</span></span>             | <span data-ttu-id="4edd7-187">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-187">True</span></span>                                                          |
| <span data-ttu-id="4edd7-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4edd7-188">In Global Catalog</span></span>      | <span data-ttu-id="4edd7-189">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-189">True</span></span>                                                          |
| <span data-ttu-id="4edd7-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4edd7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4edd7-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4edd7-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4edd7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4edd7-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4edd7-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-194">Search-Flags</span></span>           | <span data-ttu-id="4edd7-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4edd7-195">0x00000001</span></span>                                                    |
| <span data-ttu-id="4edd7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-196">System-Flags</span></span>           | <span data-ttu-id="4edd7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4edd7-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="4edd7-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4edd7-198">Classes used in</span></span>        | [<span data-ttu-id="4edd7-199">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="4edd7-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4edd7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4edd7-200">Windows Server 2008</span></span>



| <span data-ttu-id="4edd7-201">進入</span><span class="sxs-lookup"><span data-stu-id="4edd7-201">Entry</span></span> | <span data-ttu-id="4edd7-202">值</span><span class="sxs-lookup"><span data-stu-id="4edd7-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4edd7-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4edd7-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4edd7-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4edd7-205">System-Only</span></span>            | <span data-ttu-id="4edd7-206">否</span><span class="sxs-lookup"><span data-stu-id="4edd7-206">False</span></span>                                                         |
| <span data-ttu-id="4edd7-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4edd7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4edd7-208">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-208">True</span></span>                                                          |
| <span data-ttu-id="4edd7-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4edd7-209">Is Indexed</span></span>             | <span data-ttu-id="4edd7-210">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-210">True</span></span>                                                          |
| <span data-ttu-id="4edd7-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4edd7-211">In Global Catalog</span></span>      | <span data-ttu-id="4edd7-212">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-212">True</span></span>                                                          |
| <span data-ttu-id="4edd7-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4edd7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4edd7-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4edd7-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4edd7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4edd7-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4edd7-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-217">Search-Flags</span></span>           | <span data-ttu-id="4edd7-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4edd7-218">0x00000001</span></span>                                                    |
| <span data-ttu-id="4edd7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-219">System-Flags</span></span>           | <span data-ttu-id="4edd7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4edd7-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="4edd7-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4edd7-221">Classes used in</span></span>        | [<span data-ttu-id="4edd7-222">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="4edd7-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4edd7-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4edd7-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4edd7-224">進入</span><span class="sxs-lookup"><span data-stu-id="4edd7-224">Entry</span></span> | <span data-ttu-id="4edd7-225">值</span><span class="sxs-lookup"><span data-stu-id="4edd7-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4edd7-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4edd7-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4edd7-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4edd7-228">System-Only</span></span>            | <span data-ttu-id="4edd7-229">否</span><span class="sxs-lookup"><span data-stu-id="4edd7-229">False</span></span>                                                         |
| <span data-ttu-id="4edd7-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4edd7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4edd7-231">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-231">True</span></span>                                                          |
| <span data-ttu-id="4edd7-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4edd7-232">Is Indexed</span></span>             | <span data-ttu-id="4edd7-233">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-233">True</span></span>                                                          |
| <span data-ttu-id="4edd7-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4edd7-234">In Global Catalog</span></span>      | <span data-ttu-id="4edd7-235">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-235">True</span></span>                                                          |
| <span data-ttu-id="4edd7-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4edd7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4edd7-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4edd7-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4edd7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4edd7-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4edd7-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-240">Search-Flags</span></span>           | <span data-ttu-id="4edd7-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4edd7-241">0x00000001</span></span>                                                    |
| <span data-ttu-id="4edd7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-242">System-Flags</span></span>           | <span data-ttu-id="4edd7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4edd7-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="4edd7-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4edd7-244">Classes used in</span></span>        | [<span data-ttu-id="4edd7-245">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="4edd7-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4edd7-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4edd7-246">Windows Server 2012</span></span>



| <span data-ttu-id="4edd7-247">進入</span><span class="sxs-lookup"><span data-stu-id="4edd7-247">Entry</span></span> | <span data-ttu-id="4edd7-248">值</span><span class="sxs-lookup"><span data-stu-id="4edd7-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4edd7-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4edd7-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4edd7-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4edd7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4edd7-251">System-Only</span></span>            | <span data-ttu-id="4edd7-252">否</span><span class="sxs-lookup"><span data-stu-id="4edd7-252">False</span></span>                                                         |
| <span data-ttu-id="4edd7-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4edd7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4edd7-254">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-254">True</span></span>                                                          |
| <span data-ttu-id="4edd7-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4edd7-255">Is Indexed</span></span>             | <span data-ttu-id="4edd7-256">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-256">True</span></span>                                                          |
| <span data-ttu-id="4edd7-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4edd7-257">In Global Catalog</span></span>      | <span data-ttu-id="4edd7-258">對</span><span class="sxs-lookup"><span data-stu-id="4edd7-258">True</span></span>                                                          |
| <span data-ttu-id="4edd7-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4edd7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4edd7-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4edd7-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4edd7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4edd7-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4edd7-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="4edd7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-263">Search-Flags</span></span>           | <span data-ttu-id="4edd7-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4edd7-264">0x00000001</span></span>                                                    |
| <span data-ttu-id="4edd7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4edd7-265">System-Flags</span></span>           | <span data-ttu-id="4edd7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4edd7-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="4edd7-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4edd7-267">Classes used in</span></span>        | [<span data-ttu-id="4edd7-268">**SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="4edd7-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





