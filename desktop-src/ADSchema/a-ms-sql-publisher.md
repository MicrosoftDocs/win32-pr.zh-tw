---
title: TRANSACT-SQL-發行者屬性
description: 用於複寫的發行者資料庫名稱。
ms.assetid: f5efb16d-ea0a-4015-aa6f-de7bf7401eb4
ms.tgt_platform: multiple
keywords:
- TRANSACT-SQL-發行者屬性 AD 架構
- TRANSACT-SQL-發行者屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Publisher
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f12a9833918e540877bf58978c5c314165d60044
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686831"
---
# <a name="ms-sql-publisher-attribute"></a><span data-ttu-id="69203-105">TRANSACT-SQL-發行者屬性</span><span class="sxs-lookup"><span data-stu-id="69203-105">MS-SQL-Publisher attribute</span></span>

<span data-ttu-id="69203-106">用於複寫的發行者資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="69203-106">The name of the publisher database for replication.</span></span>



| <span data-ttu-id="69203-107">進入</span><span class="sxs-lookup"><span data-stu-id="69203-107">Entry</span></span> | <span data-ttu-id="69203-108">值</span><span class="sxs-lookup"><span data-stu-id="69203-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="69203-109">CN</span><span class="sxs-lookup"><span data-stu-id="69203-109">CN</span></span>                | <span data-ttu-id="69203-110">TRANSACT-SQL-發行者</span><span class="sxs-lookup"><span data-stu-id="69203-110">MS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="69203-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="69203-111">Ldap-Display-Name</span></span> | <span data-ttu-id="69203-112">TRANSACT-SQL-發行者</span><span class="sxs-lookup"><span data-stu-id="69203-112">mS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="69203-113">大小</span><span class="sxs-lookup"><span data-stu-id="69203-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="69203-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="69203-114">Update Privilege</span></span>  | <span data-ttu-id="69203-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="69203-115">Domain administrator</span></span>                        |
| <span data-ttu-id="69203-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="69203-116">Update Frequency</span></span>  | <span data-ttu-id="69203-117">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="69203-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="69203-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69203-118">Attribute-Id</span></span>      | <span data-ttu-id="69203-119">1.2.840.113556.1.4.1402</span><span class="sxs-lookup"><span data-stu-id="69203-119">1.2.840.113556.1.4.1402</span></span>                     |
| <span data-ttu-id="69203-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="69203-120">System-Id-Guid</span></span>    | <span data-ttu-id="69203-121">c1676858-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="69203-121">c1676858-d34b-11d2-999a-0000f87a57d4</span></span>        |
| <span data-ttu-id="69203-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="69203-122">Syntax</span></span>            | [<span data-ttu-id="69203-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="69203-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="69203-124">實作</span><span class="sxs-lookup"><span data-stu-id="69203-124">Implementations</span></span>

-   [<span data-ttu-id="69203-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="69203-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="69203-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69203-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69203-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69203-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69203-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69203-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69203-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69203-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69203-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69203-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="69203-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69203-131">Windows 2000 Server</span></span>



| <span data-ttu-id="69203-132">進入</span><span class="sxs-lookup"><span data-stu-id="69203-132">Entry</span></span> | <span data-ttu-id="69203-133">值</span><span class="sxs-lookup"><span data-stu-id="69203-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="69203-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69203-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69203-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="69203-136">System-Only</span></span>            | <span data-ttu-id="69203-137">否</span><span class="sxs-lookup"><span data-stu-id="69203-137">False</span></span>                                                               |
| <span data-ttu-id="69203-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69203-138">Is-Single-Valued</span></span>       | <span data-ttu-id="69203-139">對</span><span class="sxs-lookup"><span data-stu-id="69203-139">True</span></span>                                                                |
| <span data-ttu-id="69203-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69203-140">Is Indexed</span></span>             | <span data-ttu-id="69203-141">否</span><span class="sxs-lookup"><span data-stu-id="69203-141">False</span></span>                                                               |
| <span data-ttu-id="69203-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69203-142">In Global Catalog</span></span>      | <span data-ttu-id="69203-143">否</span><span class="sxs-lookup"><span data-stu-id="69203-143">False</span></span>                                                               |
| <span data-ttu-id="69203-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69203-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="69203-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69203-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="69203-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69203-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69203-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-148">Search-Flags</span></span>           | <span data-ttu-id="69203-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69203-149">0x00000000</span></span>                                                          |
| <span data-ttu-id="69203-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-150">System-Flags</span></span>           | <span data-ttu-id="69203-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69203-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="69203-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69203-152">Classes used in</span></span>        | [<span data-ttu-id="69203-153">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="69203-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="69203-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69203-154">Windows Server 2003</span></span>



| <span data-ttu-id="69203-155">進入</span><span class="sxs-lookup"><span data-stu-id="69203-155">Entry</span></span> | <span data-ttu-id="69203-156">值</span><span class="sxs-lookup"><span data-stu-id="69203-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="69203-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69203-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69203-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="69203-159">System-Only</span></span>            | <span data-ttu-id="69203-160">否</span><span class="sxs-lookup"><span data-stu-id="69203-160">False</span></span>                                                               |
| <span data-ttu-id="69203-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69203-161">Is-Single-Valued</span></span>       | <span data-ttu-id="69203-162">對</span><span class="sxs-lookup"><span data-stu-id="69203-162">True</span></span>                                                                |
| <span data-ttu-id="69203-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69203-163">Is Indexed</span></span>             | <span data-ttu-id="69203-164">否</span><span class="sxs-lookup"><span data-stu-id="69203-164">False</span></span>                                                               |
| <span data-ttu-id="69203-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69203-165">In Global Catalog</span></span>      | <span data-ttu-id="69203-166">否</span><span class="sxs-lookup"><span data-stu-id="69203-166">False</span></span>                                                               |
| <span data-ttu-id="69203-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69203-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="69203-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69203-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="69203-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69203-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69203-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-171">Search-Flags</span></span>           | <span data-ttu-id="69203-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69203-172">0x00000000</span></span>                                                          |
| <span data-ttu-id="69203-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-173">System-Flags</span></span>           | <span data-ttu-id="69203-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69203-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="69203-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69203-175">Classes used in</span></span>        | [<span data-ttu-id="69203-176">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="69203-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69203-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69203-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69203-178">進入</span><span class="sxs-lookup"><span data-stu-id="69203-178">Entry</span></span> | <span data-ttu-id="69203-179">值</span><span class="sxs-lookup"><span data-stu-id="69203-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="69203-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69203-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69203-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="69203-182">System-Only</span></span>            | <span data-ttu-id="69203-183">否</span><span class="sxs-lookup"><span data-stu-id="69203-183">False</span></span>                                                               |
| <span data-ttu-id="69203-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69203-184">Is-Single-Valued</span></span>       | <span data-ttu-id="69203-185">對</span><span class="sxs-lookup"><span data-stu-id="69203-185">True</span></span>                                                                |
| <span data-ttu-id="69203-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69203-186">Is Indexed</span></span>             | <span data-ttu-id="69203-187">否</span><span class="sxs-lookup"><span data-stu-id="69203-187">False</span></span>                                                               |
| <span data-ttu-id="69203-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69203-188">In Global Catalog</span></span>      | <span data-ttu-id="69203-189">否</span><span class="sxs-lookup"><span data-stu-id="69203-189">False</span></span>                                                               |
| <span data-ttu-id="69203-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69203-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="69203-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69203-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="69203-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69203-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69203-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-194">Search-Flags</span></span>           | <span data-ttu-id="69203-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69203-195">0x00000000</span></span>                                                          |
| <span data-ttu-id="69203-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-196">System-Flags</span></span>           | <span data-ttu-id="69203-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69203-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="69203-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69203-198">Classes used in</span></span>        | [<span data-ttu-id="69203-199">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="69203-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69203-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69203-200">Windows Server 2008</span></span>



| <span data-ttu-id="69203-201">進入</span><span class="sxs-lookup"><span data-stu-id="69203-201">Entry</span></span> | <span data-ttu-id="69203-202">值</span><span class="sxs-lookup"><span data-stu-id="69203-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="69203-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69203-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69203-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="69203-205">System-Only</span></span>            | <span data-ttu-id="69203-206">否</span><span class="sxs-lookup"><span data-stu-id="69203-206">False</span></span>                                                               |
| <span data-ttu-id="69203-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69203-207">Is-Single-Valued</span></span>       | <span data-ttu-id="69203-208">對</span><span class="sxs-lookup"><span data-stu-id="69203-208">True</span></span>                                                                |
| <span data-ttu-id="69203-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69203-209">Is Indexed</span></span>             | <span data-ttu-id="69203-210">否</span><span class="sxs-lookup"><span data-stu-id="69203-210">False</span></span>                                                               |
| <span data-ttu-id="69203-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69203-211">In Global Catalog</span></span>      | <span data-ttu-id="69203-212">否</span><span class="sxs-lookup"><span data-stu-id="69203-212">False</span></span>                                                               |
| <span data-ttu-id="69203-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69203-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="69203-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69203-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="69203-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69203-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69203-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-217">Search-Flags</span></span>           | <span data-ttu-id="69203-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69203-218">0x00000000</span></span>                                                          |
| <span data-ttu-id="69203-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-219">System-Flags</span></span>           | <span data-ttu-id="69203-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69203-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="69203-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69203-221">Classes used in</span></span>        | [<span data-ttu-id="69203-222">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="69203-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69203-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69203-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69203-224">進入</span><span class="sxs-lookup"><span data-stu-id="69203-224">Entry</span></span> | <span data-ttu-id="69203-225">值</span><span class="sxs-lookup"><span data-stu-id="69203-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="69203-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69203-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69203-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="69203-228">System-Only</span></span>            | <span data-ttu-id="69203-229">否</span><span class="sxs-lookup"><span data-stu-id="69203-229">False</span></span>                                                               |
| <span data-ttu-id="69203-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69203-230">Is-Single-Valued</span></span>       | <span data-ttu-id="69203-231">對</span><span class="sxs-lookup"><span data-stu-id="69203-231">True</span></span>                                                                |
| <span data-ttu-id="69203-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69203-232">Is Indexed</span></span>             | <span data-ttu-id="69203-233">否</span><span class="sxs-lookup"><span data-stu-id="69203-233">False</span></span>                                                               |
| <span data-ttu-id="69203-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69203-234">In Global Catalog</span></span>      | <span data-ttu-id="69203-235">否</span><span class="sxs-lookup"><span data-stu-id="69203-235">False</span></span>                                                               |
| <span data-ttu-id="69203-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69203-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="69203-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69203-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="69203-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69203-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69203-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-240">Search-Flags</span></span>           | <span data-ttu-id="69203-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69203-241">0x00000000</span></span>                                                          |
| <span data-ttu-id="69203-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-242">System-Flags</span></span>           | <span data-ttu-id="69203-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69203-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="69203-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69203-244">Classes used in</span></span>        | [<span data-ttu-id="69203-245">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="69203-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69203-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69203-246">Windows Server 2012</span></span>



| <span data-ttu-id="69203-247">進入</span><span class="sxs-lookup"><span data-stu-id="69203-247">Entry</span></span> | <span data-ttu-id="69203-248">值</span><span class="sxs-lookup"><span data-stu-id="69203-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="69203-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69203-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69203-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="69203-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="69203-251">System-Only</span></span>            | <span data-ttu-id="69203-252">否</span><span class="sxs-lookup"><span data-stu-id="69203-252">False</span></span>                                                               |
| <span data-ttu-id="69203-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69203-253">Is-Single-Valued</span></span>       | <span data-ttu-id="69203-254">對</span><span class="sxs-lookup"><span data-stu-id="69203-254">True</span></span>                                                                |
| <span data-ttu-id="69203-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69203-255">Is Indexed</span></span>             | <span data-ttu-id="69203-256">否</span><span class="sxs-lookup"><span data-stu-id="69203-256">False</span></span>                                                               |
| <span data-ttu-id="69203-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69203-257">In Global Catalog</span></span>      | <span data-ttu-id="69203-258">否</span><span class="sxs-lookup"><span data-stu-id="69203-258">False</span></span>                                                               |
| <span data-ttu-id="69203-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69203-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="69203-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69203-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="69203-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69203-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69203-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="69203-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-263">Search-Flags</span></span>           | <span data-ttu-id="69203-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69203-264">0x00000000</span></span>                                                          |
| <span data-ttu-id="69203-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69203-265">System-Flags</span></span>           | <span data-ttu-id="69203-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69203-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="69203-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69203-267">Classes used in</span></span>        | [<span data-ttu-id="69203-268">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="69203-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





