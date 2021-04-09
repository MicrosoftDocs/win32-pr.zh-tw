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
# <a name="ms-sql-publisher-attribute"></a><span data-ttu-id="a3446-105">TRANSACT-SQL-發行者屬性</span><span class="sxs-lookup"><span data-stu-id="a3446-105">MS-SQL-Publisher attribute</span></span>

<span data-ttu-id="a3446-106">用於複寫的發行者資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a3446-106">The name of the publisher database for replication.</span></span>



| <span data-ttu-id="a3446-107">進入</span><span class="sxs-lookup"><span data-stu-id="a3446-107">Entry</span></span> | <span data-ttu-id="a3446-108">值</span><span class="sxs-lookup"><span data-stu-id="a3446-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a3446-109">CN</span><span class="sxs-lookup"><span data-stu-id="a3446-109">CN</span></span>                | <span data-ttu-id="a3446-110">TRANSACT-SQL-發行者</span><span class="sxs-lookup"><span data-stu-id="a3446-110">MS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="a3446-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a3446-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a3446-112">TRANSACT-SQL-發行者</span><span class="sxs-lookup"><span data-stu-id="a3446-112">mS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="a3446-113">大小</span><span class="sxs-lookup"><span data-stu-id="a3446-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a3446-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a3446-114">Update Privilege</span></span>  | <span data-ttu-id="a3446-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="a3446-115">Domain administrator</span></span>                        |
| <span data-ttu-id="a3446-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a3446-116">Update Frequency</span></span>  | <span data-ttu-id="a3446-117">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="a3446-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="a3446-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3446-118">Attribute-Id</span></span>      | <span data-ttu-id="a3446-119">1.2.840.113556.1.4.1402</span><span class="sxs-lookup"><span data-stu-id="a3446-119">1.2.840.113556.1.4.1402</span></span>                     |
| <span data-ttu-id="a3446-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a3446-120">System-Id-Guid</span></span>    | <span data-ttu-id="a3446-121">c1676858-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a3446-121">c1676858-d34b-11d2-999a-0000f87a57d4</span></span>        |
| <span data-ttu-id="a3446-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3446-122">Syntax</span></span>            | [<span data-ttu-id="a3446-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a3446-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a3446-124">實作</span><span class="sxs-lookup"><span data-stu-id="a3446-124">Implementations</span></span>

-   [<span data-ttu-id="a3446-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a3446-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a3446-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3446-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3446-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3446-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3446-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3446-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3446-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3446-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3446-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3446-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a3446-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3446-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a3446-132">進入</span><span class="sxs-lookup"><span data-stu-id="a3446-132">Entry</span></span> | <span data-ttu-id="a3446-133">值</span><span class="sxs-lookup"><span data-stu-id="a3446-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a3446-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3446-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3446-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3446-136">System-Only</span></span>            | <span data-ttu-id="a3446-137">否</span><span class="sxs-lookup"><span data-stu-id="a3446-137">False</span></span>                                                               |
| <span data-ttu-id="a3446-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3446-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a3446-139">對</span><span class="sxs-lookup"><span data-stu-id="a3446-139">True</span></span>                                                                |
| <span data-ttu-id="a3446-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3446-140">Is Indexed</span></span>             | <span data-ttu-id="a3446-141">否</span><span class="sxs-lookup"><span data-stu-id="a3446-141">False</span></span>                                                               |
| <span data-ttu-id="a3446-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3446-142">In Global Catalog</span></span>      | <span data-ttu-id="a3446-143">否</span><span class="sxs-lookup"><span data-stu-id="a3446-143">False</span></span>                                                               |
| <span data-ttu-id="a3446-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3446-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3446-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3446-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a3446-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3446-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3446-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-148">Search-Flags</span></span>           | <span data-ttu-id="a3446-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3446-149">0x00000000</span></span>                                                          |
| <span data-ttu-id="a3446-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-150">System-Flags</span></span>           | <span data-ttu-id="a3446-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3446-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="a3446-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3446-152">Classes used in</span></span>        | [<span data-ttu-id="a3446-153">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a3446-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a3446-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3446-154">Windows Server 2003</span></span>



| <span data-ttu-id="a3446-155">進入</span><span class="sxs-lookup"><span data-stu-id="a3446-155">Entry</span></span> | <span data-ttu-id="a3446-156">值</span><span class="sxs-lookup"><span data-stu-id="a3446-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a3446-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3446-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3446-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3446-159">System-Only</span></span>            | <span data-ttu-id="a3446-160">否</span><span class="sxs-lookup"><span data-stu-id="a3446-160">False</span></span>                                                               |
| <span data-ttu-id="a3446-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3446-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a3446-162">對</span><span class="sxs-lookup"><span data-stu-id="a3446-162">True</span></span>                                                                |
| <span data-ttu-id="a3446-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3446-163">Is Indexed</span></span>             | <span data-ttu-id="a3446-164">否</span><span class="sxs-lookup"><span data-stu-id="a3446-164">False</span></span>                                                               |
| <span data-ttu-id="a3446-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3446-165">In Global Catalog</span></span>      | <span data-ttu-id="a3446-166">否</span><span class="sxs-lookup"><span data-stu-id="a3446-166">False</span></span>                                                               |
| <span data-ttu-id="a3446-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3446-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3446-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3446-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a3446-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3446-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3446-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-171">Search-Flags</span></span>           | <span data-ttu-id="a3446-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3446-172">0x00000000</span></span>                                                          |
| <span data-ttu-id="a3446-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-173">System-Flags</span></span>           | <span data-ttu-id="a3446-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3446-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="a3446-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3446-175">Classes used in</span></span>        | [<span data-ttu-id="a3446-176">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a3446-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3446-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3446-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3446-178">進入</span><span class="sxs-lookup"><span data-stu-id="a3446-178">Entry</span></span> | <span data-ttu-id="a3446-179">值</span><span class="sxs-lookup"><span data-stu-id="a3446-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a3446-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3446-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3446-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3446-182">System-Only</span></span>            | <span data-ttu-id="a3446-183">否</span><span class="sxs-lookup"><span data-stu-id="a3446-183">False</span></span>                                                               |
| <span data-ttu-id="a3446-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3446-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a3446-185">對</span><span class="sxs-lookup"><span data-stu-id="a3446-185">True</span></span>                                                                |
| <span data-ttu-id="a3446-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3446-186">Is Indexed</span></span>             | <span data-ttu-id="a3446-187">否</span><span class="sxs-lookup"><span data-stu-id="a3446-187">False</span></span>                                                               |
| <span data-ttu-id="a3446-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3446-188">In Global Catalog</span></span>      | <span data-ttu-id="a3446-189">否</span><span class="sxs-lookup"><span data-stu-id="a3446-189">False</span></span>                                                               |
| <span data-ttu-id="a3446-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3446-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3446-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3446-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a3446-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3446-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3446-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-194">Search-Flags</span></span>           | <span data-ttu-id="a3446-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3446-195">0x00000000</span></span>                                                          |
| <span data-ttu-id="a3446-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-196">System-Flags</span></span>           | <span data-ttu-id="a3446-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3446-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="a3446-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3446-198">Classes used in</span></span>        | [<span data-ttu-id="a3446-199">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a3446-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3446-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3446-200">Windows Server 2008</span></span>



| <span data-ttu-id="a3446-201">進入</span><span class="sxs-lookup"><span data-stu-id="a3446-201">Entry</span></span> | <span data-ttu-id="a3446-202">值</span><span class="sxs-lookup"><span data-stu-id="a3446-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a3446-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3446-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3446-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3446-205">System-Only</span></span>            | <span data-ttu-id="a3446-206">否</span><span class="sxs-lookup"><span data-stu-id="a3446-206">False</span></span>                                                               |
| <span data-ttu-id="a3446-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3446-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a3446-208">對</span><span class="sxs-lookup"><span data-stu-id="a3446-208">True</span></span>                                                                |
| <span data-ttu-id="a3446-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3446-209">Is Indexed</span></span>             | <span data-ttu-id="a3446-210">否</span><span class="sxs-lookup"><span data-stu-id="a3446-210">False</span></span>                                                               |
| <span data-ttu-id="a3446-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3446-211">In Global Catalog</span></span>      | <span data-ttu-id="a3446-212">否</span><span class="sxs-lookup"><span data-stu-id="a3446-212">False</span></span>                                                               |
| <span data-ttu-id="a3446-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3446-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3446-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3446-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a3446-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3446-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3446-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-217">Search-Flags</span></span>           | <span data-ttu-id="a3446-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3446-218">0x00000000</span></span>                                                          |
| <span data-ttu-id="a3446-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-219">System-Flags</span></span>           | <span data-ttu-id="a3446-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3446-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="a3446-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3446-221">Classes used in</span></span>        | [<span data-ttu-id="a3446-222">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a3446-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3446-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3446-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3446-224">進入</span><span class="sxs-lookup"><span data-stu-id="a3446-224">Entry</span></span> | <span data-ttu-id="a3446-225">值</span><span class="sxs-lookup"><span data-stu-id="a3446-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a3446-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3446-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3446-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3446-228">System-Only</span></span>            | <span data-ttu-id="a3446-229">否</span><span class="sxs-lookup"><span data-stu-id="a3446-229">False</span></span>                                                               |
| <span data-ttu-id="a3446-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3446-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a3446-231">對</span><span class="sxs-lookup"><span data-stu-id="a3446-231">True</span></span>                                                                |
| <span data-ttu-id="a3446-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3446-232">Is Indexed</span></span>             | <span data-ttu-id="a3446-233">否</span><span class="sxs-lookup"><span data-stu-id="a3446-233">False</span></span>                                                               |
| <span data-ttu-id="a3446-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3446-234">In Global Catalog</span></span>      | <span data-ttu-id="a3446-235">否</span><span class="sxs-lookup"><span data-stu-id="a3446-235">False</span></span>                                                               |
| <span data-ttu-id="a3446-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3446-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3446-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3446-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a3446-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3446-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3446-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-240">Search-Flags</span></span>           | <span data-ttu-id="a3446-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3446-241">0x00000000</span></span>                                                          |
| <span data-ttu-id="a3446-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-242">System-Flags</span></span>           | <span data-ttu-id="a3446-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3446-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="a3446-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3446-244">Classes used in</span></span>        | [<span data-ttu-id="a3446-245">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a3446-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3446-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3446-246">Windows Server 2012</span></span>



| <span data-ttu-id="a3446-247">進入</span><span class="sxs-lookup"><span data-stu-id="a3446-247">Entry</span></span> | <span data-ttu-id="a3446-248">值</span><span class="sxs-lookup"><span data-stu-id="a3446-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a3446-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3446-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3446-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="a3446-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3446-251">System-Only</span></span>            | <span data-ttu-id="a3446-252">否</span><span class="sxs-lookup"><span data-stu-id="a3446-252">False</span></span>                                                               |
| <span data-ttu-id="a3446-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3446-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a3446-254">對</span><span class="sxs-lookup"><span data-stu-id="a3446-254">True</span></span>                                                                |
| <span data-ttu-id="a3446-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3446-255">Is Indexed</span></span>             | <span data-ttu-id="a3446-256">否</span><span class="sxs-lookup"><span data-stu-id="a3446-256">False</span></span>                                                               |
| <span data-ttu-id="a3446-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3446-257">In Global Catalog</span></span>      | <span data-ttu-id="a3446-258">否</span><span class="sxs-lookup"><span data-stu-id="a3446-258">False</span></span>                                                               |
| <span data-ttu-id="a3446-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3446-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3446-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3446-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="a3446-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3446-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3446-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="a3446-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-263">Search-Flags</span></span>           | <span data-ttu-id="a3446-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3446-264">0x00000000</span></span>                                                          |
| <span data-ttu-id="a3446-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3446-265">System-Flags</span></span>           | <span data-ttu-id="a3446-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3446-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="a3446-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3446-267">Classes used in</span></span>        | [<span data-ttu-id="a3446-268">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="a3446-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





