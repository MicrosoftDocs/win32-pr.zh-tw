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
# <a name="ms-sql-publisher-attribute"></a><span data-ttu-id="c60a4-105">TRANSACT-SQL-發行者屬性</span><span class="sxs-lookup"><span data-stu-id="c60a4-105">MS-SQL-Publisher attribute</span></span>

<span data-ttu-id="c60a4-106">用於複寫的發行者資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c60a4-106">The name of the publisher database for replication.</span></span>



| <span data-ttu-id="c60a4-107">進入</span><span class="sxs-lookup"><span data-stu-id="c60a4-107">Entry</span></span> | <span data-ttu-id="c60a4-108">值</span><span class="sxs-lookup"><span data-stu-id="c60a4-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c60a4-109">CN</span><span class="sxs-lookup"><span data-stu-id="c60a4-109">CN</span></span>                | <span data-ttu-id="c60a4-110">TRANSACT-SQL-發行者</span><span class="sxs-lookup"><span data-stu-id="c60a4-110">MS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="c60a4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c60a4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c60a4-112">TRANSACT-SQL-發行者</span><span class="sxs-lookup"><span data-stu-id="c60a4-112">mS-SQL-Publisher</span></span>                            |
| <span data-ttu-id="c60a4-113">大小</span><span class="sxs-lookup"><span data-stu-id="c60a4-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c60a4-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c60a4-114">Update Privilege</span></span>  | <span data-ttu-id="c60a4-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="c60a4-115">Domain administrator</span></span>                        |
| <span data-ttu-id="c60a4-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c60a4-116">Update Frequency</span></span>  | <span data-ttu-id="c60a4-117">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="c60a4-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="c60a4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c60a4-118">Attribute-Id</span></span>      | <span data-ttu-id="c60a4-119">1.2.840.113556.1.4.1402</span><span class="sxs-lookup"><span data-stu-id="c60a4-119">1.2.840.113556.1.4.1402</span></span>                     |
| <span data-ttu-id="c60a4-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c60a4-120">System-Id-Guid</span></span>    | <span data-ttu-id="c60a4-121">c1676858-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c60a4-121">c1676858-d34b-11d2-999a-0000f87a57d4</span></span>        |
| <span data-ttu-id="c60a4-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c60a4-122">Syntax</span></span>            | [<span data-ttu-id="c60a4-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c60a4-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c60a4-124">實作</span><span class="sxs-lookup"><span data-stu-id="c60a4-124">Implementations</span></span>

-   [<span data-ttu-id="c60a4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c60a4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c60a4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c60a4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c60a4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c60a4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c60a4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c60a4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c60a4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c60a4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c60a4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c60a4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c60a4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c60a4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c60a4-132">進入</span><span class="sxs-lookup"><span data-stu-id="c60a4-132">Entry</span></span> | <span data-ttu-id="c60a4-133">值</span><span class="sxs-lookup"><span data-stu-id="c60a4-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c60a4-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c60a4-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c60a4-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c60a4-136">System-Only</span></span>            | <span data-ttu-id="c60a4-137">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-137">False</span></span>                                                               |
| <span data-ttu-id="c60a4-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c60a4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c60a4-139">對</span><span class="sxs-lookup"><span data-stu-id="c60a4-139">True</span></span>                                                                |
| <span data-ttu-id="c60a4-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c60a4-140">Is Indexed</span></span>             | <span data-ttu-id="c60a4-141">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-141">False</span></span>                                                               |
| <span data-ttu-id="c60a4-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c60a4-142">In Global Catalog</span></span>      | <span data-ttu-id="c60a4-143">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-143">False</span></span>                                                               |
| <span data-ttu-id="c60a4-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c60a4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c60a4-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c60a4-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c60a4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c60a4-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c60a4-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-148">Search-Flags</span></span>           | <span data-ttu-id="c60a4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c60a4-149">0x00000000</span></span>                                                          |
| <span data-ttu-id="c60a4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-150">System-Flags</span></span>           | <span data-ttu-id="c60a4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c60a4-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="c60a4-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c60a4-152">Classes used in</span></span>        | [<span data-ttu-id="c60a4-153">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c60a4-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c60a4-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c60a4-154">Windows Server 2003</span></span>



| <span data-ttu-id="c60a4-155">進入</span><span class="sxs-lookup"><span data-stu-id="c60a4-155">Entry</span></span> | <span data-ttu-id="c60a4-156">值</span><span class="sxs-lookup"><span data-stu-id="c60a4-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c60a4-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c60a4-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c60a4-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c60a4-159">System-Only</span></span>            | <span data-ttu-id="c60a4-160">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-160">False</span></span>                                                               |
| <span data-ttu-id="c60a4-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c60a4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c60a4-162">對</span><span class="sxs-lookup"><span data-stu-id="c60a4-162">True</span></span>                                                                |
| <span data-ttu-id="c60a4-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c60a4-163">Is Indexed</span></span>             | <span data-ttu-id="c60a4-164">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-164">False</span></span>                                                               |
| <span data-ttu-id="c60a4-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c60a4-165">In Global Catalog</span></span>      | <span data-ttu-id="c60a4-166">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-166">False</span></span>                                                               |
| <span data-ttu-id="c60a4-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c60a4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c60a4-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c60a4-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c60a4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c60a4-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c60a4-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-171">Search-Flags</span></span>           | <span data-ttu-id="c60a4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c60a4-172">0x00000000</span></span>                                                          |
| <span data-ttu-id="c60a4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-173">System-Flags</span></span>           | <span data-ttu-id="c60a4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c60a4-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="c60a4-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c60a4-175">Classes used in</span></span>        | [<span data-ttu-id="c60a4-176">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c60a4-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c60a4-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c60a4-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c60a4-178">進入</span><span class="sxs-lookup"><span data-stu-id="c60a4-178">Entry</span></span> | <span data-ttu-id="c60a4-179">值</span><span class="sxs-lookup"><span data-stu-id="c60a4-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c60a4-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c60a4-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c60a4-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c60a4-182">System-Only</span></span>            | <span data-ttu-id="c60a4-183">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-183">False</span></span>                                                               |
| <span data-ttu-id="c60a4-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c60a4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c60a4-185">對</span><span class="sxs-lookup"><span data-stu-id="c60a4-185">True</span></span>                                                                |
| <span data-ttu-id="c60a4-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c60a4-186">Is Indexed</span></span>             | <span data-ttu-id="c60a4-187">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-187">False</span></span>                                                               |
| <span data-ttu-id="c60a4-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c60a4-188">In Global Catalog</span></span>      | <span data-ttu-id="c60a4-189">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-189">False</span></span>                                                               |
| <span data-ttu-id="c60a4-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c60a4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c60a4-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c60a4-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c60a4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c60a4-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c60a4-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-194">Search-Flags</span></span>           | <span data-ttu-id="c60a4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c60a4-195">0x00000000</span></span>                                                          |
| <span data-ttu-id="c60a4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-196">System-Flags</span></span>           | <span data-ttu-id="c60a4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c60a4-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="c60a4-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c60a4-198">Classes used in</span></span>        | [<span data-ttu-id="c60a4-199">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c60a4-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c60a4-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c60a4-200">Windows Server 2008</span></span>



| <span data-ttu-id="c60a4-201">進入</span><span class="sxs-lookup"><span data-stu-id="c60a4-201">Entry</span></span> | <span data-ttu-id="c60a4-202">值</span><span class="sxs-lookup"><span data-stu-id="c60a4-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c60a4-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c60a4-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c60a4-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c60a4-205">System-Only</span></span>            | <span data-ttu-id="c60a4-206">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-206">False</span></span>                                                               |
| <span data-ttu-id="c60a4-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c60a4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c60a4-208">對</span><span class="sxs-lookup"><span data-stu-id="c60a4-208">True</span></span>                                                                |
| <span data-ttu-id="c60a4-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c60a4-209">Is Indexed</span></span>             | <span data-ttu-id="c60a4-210">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-210">False</span></span>                                                               |
| <span data-ttu-id="c60a4-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c60a4-211">In Global Catalog</span></span>      | <span data-ttu-id="c60a4-212">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-212">False</span></span>                                                               |
| <span data-ttu-id="c60a4-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c60a4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c60a4-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c60a4-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c60a4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c60a4-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c60a4-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-217">Search-Flags</span></span>           | <span data-ttu-id="c60a4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c60a4-218">0x00000000</span></span>                                                          |
| <span data-ttu-id="c60a4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-219">System-Flags</span></span>           | <span data-ttu-id="c60a4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c60a4-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="c60a4-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c60a4-221">Classes used in</span></span>        | [<span data-ttu-id="c60a4-222">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c60a4-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c60a4-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c60a4-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c60a4-224">進入</span><span class="sxs-lookup"><span data-stu-id="c60a4-224">Entry</span></span> | <span data-ttu-id="c60a4-225">值</span><span class="sxs-lookup"><span data-stu-id="c60a4-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c60a4-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c60a4-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c60a4-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c60a4-228">System-Only</span></span>            | <span data-ttu-id="c60a4-229">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-229">False</span></span>                                                               |
| <span data-ttu-id="c60a4-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c60a4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c60a4-231">對</span><span class="sxs-lookup"><span data-stu-id="c60a4-231">True</span></span>                                                                |
| <span data-ttu-id="c60a4-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c60a4-232">Is Indexed</span></span>             | <span data-ttu-id="c60a4-233">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-233">False</span></span>                                                               |
| <span data-ttu-id="c60a4-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c60a4-234">In Global Catalog</span></span>      | <span data-ttu-id="c60a4-235">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-235">False</span></span>                                                               |
| <span data-ttu-id="c60a4-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c60a4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c60a4-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c60a4-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c60a4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c60a4-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c60a4-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-240">Search-Flags</span></span>           | <span data-ttu-id="c60a4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c60a4-241">0x00000000</span></span>                                                          |
| <span data-ttu-id="c60a4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-242">System-Flags</span></span>           | <span data-ttu-id="c60a4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c60a4-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="c60a4-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c60a4-244">Classes used in</span></span>        | [<span data-ttu-id="c60a4-245">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c60a4-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c60a4-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c60a4-246">Windows Server 2012</span></span>



| <span data-ttu-id="c60a4-247">進入</span><span class="sxs-lookup"><span data-stu-id="c60a4-247">Entry</span></span> | <span data-ttu-id="c60a4-248">值</span><span class="sxs-lookup"><span data-stu-id="c60a4-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c60a4-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c60a4-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c60a4-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="c60a4-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c60a4-251">System-Only</span></span>            | <span data-ttu-id="c60a4-252">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-252">False</span></span>                                                               |
| <span data-ttu-id="c60a4-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c60a4-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c60a4-254">對</span><span class="sxs-lookup"><span data-stu-id="c60a4-254">True</span></span>                                                                |
| <span data-ttu-id="c60a4-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c60a4-255">Is Indexed</span></span>             | <span data-ttu-id="c60a4-256">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-256">False</span></span>                                                               |
| <span data-ttu-id="c60a4-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c60a4-257">In Global Catalog</span></span>      | <span data-ttu-id="c60a4-258">否</span><span class="sxs-lookup"><span data-stu-id="c60a4-258">False</span></span>                                                               |
| <span data-ttu-id="c60a4-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c60a4-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c60a4-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c60a4-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="c60a4-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c60a4-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c60a4-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="c60a4-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-263">Search-Flags</span></span>           | <span data-ttu-id="c60a4-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c60a4-264">0x00000000</span></span>                                                          |
| <span data-ttu-id="c60a4-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c60a4-265">System-Flags</span></span>           | <span data-ttu-id="c60a4-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c60a4-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="c60a4-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c60a4-267">Classes used in</span></span>        | [<span data-ttu-id="c60a4-268">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="c60a4-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





