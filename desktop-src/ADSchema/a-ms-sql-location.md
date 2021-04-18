---
title: TRANSACT-SQL-Location 屬性
description: 使用者定義的字串。 預設值是設定為 [位置]。
ms.assetid: e0d8a83f-a979-49a8-a92d-842c18c8f9fd
ms.tgt_platform: multiple
keywords:
- TRANSACT-SQL-Location 屬性 AD 架構
- TRANSACT-SQL-Location 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ffa71a40e7deff12385e0e45eb16d8dcc998269
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106968604"
---
# <a name="ms-sql-location-attribute"></a><span data-ttu-id="32355-106">TRANSACT-SQL-Location 屬性</span><span class="sxs-lookup"><span data-stu-id="32355-106">MS-SQL-Location attribute</span></span>

<span data-ttu-id="32355-107">使用者定義的字串。</span><span class="sxs-lookup"><span data-stu-id="32355-107">A user defined string.</span></span> <span data-ttu-id="32355-108">預設值是設定為 [位置]。</span><span class="sxs-lookup"><span data-stu-id="32355-108">Default is set to Location.</span></span>



| <span data-ttu-id="32355-109">進入</span><span class="sxs-lookup"><span data-stu-id="32355-109">Entry</span></span> | <span data-ttu-id="32355-110">值</span><span class="sxs-lookup"><span data-stu-id="32355-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="32355-111">CN</span><span class="sxs-lookup"><span data-stu-id="32355-111">CN</span></span>                | <span data-ttu-id="32355-112">MS-CHAP-位置</span><span class="sxs-lookup"><span data-stu-id="32355-112">MS-SQL-Location</span></span>                             |
| <span data-ttu-id="32355-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="32355-113">Ldap-Display-Name</span></span> | <span data-ttu-id="32355-114">Ms-chap-位置</span><span class="sxs-lookup"><span data-stu-id="32355-114">mS-SQL-Location</span></span>                             |
| <span data-ttu-id="32355-115">大小</span><span class="sxs-lookup"><span data-stu-id="32355-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="32355-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="32355-116">Update Privilege</span></span>  | <span data-ttu-id="32355-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="32355-117">Domain administrator</span></span>                        |
| <span data-ttu-id="32355-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="32355-118">Update Frequency</span></span>  | <span data-ttu-id="32355-119">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="32355-119">At system setup.</span></span>                            |
| <span data-ttu-id="32355-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="32355-120">Attribute-Id</span></span>      | <span data-ttu-id="32355-121">1.2.840.113556.1.4.1366</span><span class="sxs-lookup"><span data-stu-id="32355-121">1.2.840.113556.1.4.1366</span></span>                     |
| <span data-ttu-id="32355-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="32355-122">System-Id-Guid</span></span>    | <span data-ttu-id="32355-123">561c9644-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="32355-123">561c9644-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="32355-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="32355-124">Syntax</span></span>            | [<span data-ttu-id="32355-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="32355-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="32355-126">實作</span><span class="sxs-lookup"><span data-stu-id="32355-126">Implementations</span></span>

-   [<span data-ttu-id="32355-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="32355-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="32355-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="32355-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="32355-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="32355-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="32355-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="32355-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="32355-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="32355-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="32355-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="32355-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="32355-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32355-133">Windows 2000 Server</span></span>



| <span data-ttu-id="32355-134">進入</span><span class="sxs-lookup"><span data-stu-id="32355-134">Entry</span></span> | <span data-ttu-id="32355-135">值</span><span class="sxs-lookup"><span data-stu-id="32355-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="32355-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32355-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32355-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="32355-138">System-Only</span></span>            | <span data-ttu-id="32355-139">否</span><span class="sxs-lookup"><span data-stu-id="32355-139">False</span></span>                                                     |
| <span data-ttu-id="32355-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32355-140">Is-Single-Valued</span></span>       | <span data-ttu-id="32355-141">對</span><span class="sxs-lookup"><span data-stu-id="32355-141">True</span></span>                                                      |
| <span data-ttu-id="32355-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32355-142">Is Indexed</span></span>             | <span data-ttu-id="32355-143">否</span><span class="sxs-lookup"><span data-stu-id="32355-143">False</span></span>                                                     |
| <span data-ttu-id="32355-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32355-144">In Global Catalog</span></span>      | <span data-ttu-id="32355-145">否</span><span class="sxs-lookup"><span data-stu-id="32355-145">False</span></span>                                                     |
| <span data-ttu-id="32355-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32355-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="32355-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32355-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="32355-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32355-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="32355-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32355-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="32355-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-150">Search-Flags</span></span>           | <span data-ttu-id="32355-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32355-151">0x00000000</span></span>                                                |
| <span data-ttu-id="32355-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-152">System-Flags</span></span>           | <span data-ttu-id="32355-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32355-153">0x00000010</span></span>                                                |
| <span data-ttu-id="32355-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32355-154">Classes used in</span></span>        | [<span data-ttu-id="32355-155">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="32355-155">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="32355-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32355-156">Windows Server 2003</span></span>



| <span data-ttu-id="32355-157">進入</span><span class="sxs-lookup"><span data-stu-id="32355-157">Entry</span></span> | <span data-ttu-id="32355-158">值</span><span class="sxs-lookup"><span data-stu-id="32355-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="32355-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32355-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32355-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="32355-161">System-Only</span></span>            | <span data-ttu-id="32355-162">否</span><span class="sxs-lookup"><span data-stu-id="32355-162">False</span></span>                                                     |
| <span data-ttu-id="32355-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32355-163">Is-Single-Valued</span></span>       | <span data-ttu-id="32355-164">對</span><span class="sxs-lookup"><span data-stu-id="32355-164">True</span></span>                                                      |
| <span data-ttu-id="32355-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32355-165">Is Indexed</span></span>             | <span data-ttu-id="32355-166">否</span><span class="sxs-lookup"><span data-stu-id="32355-166">False</span></span>                                                     |
| <span data-ttu-id="32355-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32355-167">In Global Catalog</span></span>      | <span data-ttu-id="32355-168">否</span><span class="sxs-lookup"><span data-stu-id="32355-168">False</span></span>                                                     |
| <span data-ttu-id="32355-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32355-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="32355-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32355-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="32355-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32355-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="32355-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32355-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="32355-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-173">Search-Flags</span></span>           | <span data-ttu-id="32355-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32355-174">0x00000000</span></span>                                                |
| <span data-ttu-id="32355-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-175">System-Flags</span></span>           | <span data-ttu-id="32355-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32355-176">0x00000010</span></span>                                                |
| <span data-ttu-id="32355-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32355-177">Classes used in</span></span>        | [<span data-ttu-id="32355-178">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="32355-178">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="32355-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="32355-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="32355-180">進入</span><span class="sxs-lookup"><span data-stu-id="32355-180">Entry</span></span> | <span data-ttu-id="32355-181">值</span><span class="sxs-lookup"><span data-stu-id="32355-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="32355-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32355-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32355-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="32355-184">System-Only</span></span>            | <span data-ttu-id="32355-185">否</span><span class="sxs-lookup"><span data-stu-id="32355-185">False</span></span>                                                     |
| <span data-ttu-id="32355-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32355-186">Is-Single-Valued</span></span>       | <span data-ttu-id="32355-187">對</span><span class="sxs-lookup"><span data-stu-id="32355-187">True</span></span>                                                      |
| <span data-ttu-id="32355-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32355-188">Is Indexed</span></span>             | <span data-ttu-id="32355-189">否</span><span class="sxs-lookup"><span data-stu-id="32355-189">False</span></span>                                                     |
| <span data-ttu-id="32355-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32355-190">In Global Catalog</span></span>      | <span data-ttu-id="32355-191">否</span><span class="sxs-lookup"><span data-stu-id="32355-191">False</span></span>                                                     |
| <span data-ttu-id="32355-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32355-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="32355-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32355-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="32355-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32355-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="32355-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32355-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="32355-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-196">Search-Flags</span></span>           | <span data-ttu-id="32355-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32355-197">0x00000000</span></span>                                                |
| <span data-ttu-id="32355-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-198">System-Flags</span></span>           | <span data-ttu-id="32355-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32355-199">0x00000010</span></span>                                                |
| <span data-ttu-id="32355-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32355-200">Classes used in</span></span>        | [<span data-ttu-id="32355-201">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="32355-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="32355-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32355-202">Windows Server 2008</span></span>



| <span data-ttu-id="32355-203">進入</span><span class="sxs-lookup"><span data-stu-id="32355-203">Entry</span></span> | <span data-ttu-id="32355-204">值</span><span class="sxs-lookup"><span data-stu-id="32355-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="32355-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32355-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32355-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="32355-207">System-Only</span></span>            | <span data-ttu-id="32355-208">否</span><span class="sxs-lookup"><span data-stu-id="32355-208">False</span></span>                                                     |
| <span data-ttu-id="32355-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32355-209">Is-Single-Valued</span></span>       | <span data-ttu-id="32355-210">對</span><span class="sxs-lookup"><span data-stu-id="32355-210">True</span></span>                                                      |
| <span data-ttu-id="32355-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32355-211">Is Indexed</span></span>             | <span data-ttu-id="32355-212">否</span><span class="sxs-lookup"><span data-stu-id="32355-212">False</span></span>                                                     |
| <span data-ttu-id="32355-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32355-213">In Global Catalog</span></span>      | <span data-ttu-id="32355-214">否</span><span class="sxs-lookup"><span data-stu-id="32355-214">False</span></span>                                                     |
| <span data-ttu-id="32355-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32355-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="32355-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32355-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="32355-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32355-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="32355-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32355-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="32355-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-219">Search-Flags</span></span>           | <span data-ttu-id="32355-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32355-220">0x00000000</span></span>                                                |
| <span data-ttu-id="32355-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-221">System-Flags</span></span>           | <span data-ttu-id="32355-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32355-222">0x00000010</span></span>                                                |
| <span data-ttu-id="32355-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32355-223">Classes used in</span></span>        | [<span data-ttu-id="32355-224">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="32355-224">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="32355-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32355-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="32355-226">進入</span><span class="sxs-lookup"><span data-stu-id="32355-226">Entry</span></span> | <span data-ttu-id="32355-227">值</span><span class="sxs-lookup"><span data-stu-id="32355-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="32355-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32355-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32355-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="32355-230">System-Only</span></span>            | <span data-ttu-id="32355-231">否</span><span class="sxs-lookup"><span data-stu-id="32355-231">False</span></span>                                                     |
| <span data-ttu-id="32355-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32355-232">Is-Single-Valued</span></span>       | <span data-ttu-id="32355-233">對</span><span class="sxs-lookup"><span data-stu-id="32355-233">True</span></span>                                                      |
| <span data-ttu-id="32355-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32355-234">Is Indexed</span></span>             | <span data-ttu-id="32355-235">否</span><span class="sxs-lookup"><span data-stu-id="32355-235">False</span></span>                                                     |
| <span data-ttu-id="32355-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32355-236">In Global Catalog</span></span>      | <span data-ttu-id="32355-237">否</span><span class="sxs-lookup"><span data-stu-id="32355-237">False</span></span>                                                     |
| <span data-ttu-id="32355-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32355-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="32355-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32355-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="32355-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32355-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="32355-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32355-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="32355-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-242">Search-Flags</span></span>           | <span data-ttu-id="32355-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32355-243">0x00000000</span></span>                                                |
| <span data-ttu-id="32355-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-244">System-Flags</span></span>           | <span data-ttu-id="32355-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32355-245">0x00000010</span></span>                                                |
| <span data-ttu-id="32355-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32355-246">Classes used in</span></span>        | [<span data-ttu-id="32355-247">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="32355-247">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="32355-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32355-248">Windows Server 2012</span></span>



| <span data-ttu-id="32355-249">進入</span><span class="sxs-lookup"><span data-stu-id="32355-249">Entry</span></span> | <span data-ttu-id="32355-250">值</span><span class="sxs-lookup"><span data-stu-id="32355-250">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="32355-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32355-251">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32355-252">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="32355-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="32355-253">System-Only</span></span>            | <span data-ttu-id="32355-254">否</span><span class="sxs-lookup"><span data-stu-id="32355-254">False</span></span>                                                     |
| <span data-ttu-id="32355-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32355-255">Is-Single-Valued</span></span>       | <span data-ttu-id="32355-256">對</span><span class="sxs-lookup"><span data-stu-id="32355-256">True</span></span>                                                      |
| <span data-ttu-id="32355-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32355-257">Is Indexed</span></span>             | <span data-ttu-id="32355-258">否</span><span class="sxs-lookup"><span data-stu-id="32355-258">False</span></span>                                                     |
| <span data-ttu-id="32355-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32355-259">In Global Catalog</span></span>      | <span data-ttu-id="32355-260">否</span><span class="sxs-lookup"><span data-stu-id="32355-260">False</span></span>                                                     |
| <span data-ttu-id="32355-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32355-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="32355-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32355-262">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="32355-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32355-263">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="32355-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32355-264">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="32355-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-265">Search-Flags</span></span>           | <span data-ttu-id="32355-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32355-266">0x00000000</span></span>                                                |
| <span data-ttu-id="32355-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32355-267">System-Flags</span></span>           | <span data-ttu-id="32355-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32355-268">0x00000010</span></span>                                                |
| <span data-ttu-id="32355-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32355-269">Classes used in</span></span>        | [<span data-ttu-id="32355-270">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="32355-270">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





