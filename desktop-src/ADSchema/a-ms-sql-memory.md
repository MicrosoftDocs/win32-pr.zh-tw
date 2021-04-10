---
title: MS-CHAP-Memory 屬性
description: 電腦上的記憶體數量。
ms.assetid: 36d69b8a-669b-4488-a75e-3b0af7f9845a
ms.tgt_platform: multiple
keywords:
- MS-SQL-Memory 屬性 AD 架構
- mS-SQL-Memory 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Memory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7f6b96f2a591e05df8bf325b028172ef713dc5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108197"
---
# <a name="ms-sql-memory-attribute"></a><span data-ttu-id="1ace1-105">MS-CHAP-Memory 屬性</span><span class="sxs-lookup"><span data-stu-id="1ace1-105">MS-SQL-Memory attribute</span></span>

<span data-ttu-id="1ace1-106">電腦上的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="1ace1-106">The amount of memory on the computer.</span></span>



| <span data-ttu-id="1ace1-107">進入</span><span class="sxs-lookup"><span data-stu-id="1ace1-107">Entry</span></span> | <span data-ttu-id="1ace1-108">值</span><span class="sxs-lookup"><span data-stu-id="1ace1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1ace1-109">CN</span><span class="sxs-lookup"><span data-stu-id="1ace1-109">CN</span></span>                | <span data-ttu-id="1ace1-110">MS-CHAP-記憶體</span><span class="sxs-lookup"><span data-stu-id="1ace1-110">MS-SQL-Memory</span></span>                        |
| <span data-ttu-id="1ace1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1ace1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1ace1-112">Ms-chap-記憶體</span><span class="sxs-lookup"><span data-stu-id="1ace1-112">mS-SQL-Memory</span></span>                        |
| <span data-ttu-id="1ace1-113">大小</span><span class="sxs-lookup"><span data-stu-id="1ace1-113">Size</span></span>              | <span data-ttu-id="1ace1-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="1ace1-114">8 bytes</span></span>                              |
| <span data-ttu-id="1ace1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1ace1-115">Update Privilege</span></span>  | <span data-ttu-id="1ace1-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="1ace1-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="1ace1-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1ace1-117">Update Frequency</span></span>  | <span data-ttu-id="1ace1-118">在系統啟動時。</span><span class="sxs-lookup"><span data-stu-id="1ace1-118">At system startup.</span></span>                   |
| <span data-ttu-id="1ace1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ace1-119">Attribute-Id</span></span>      | <span data-ttu-id="1ace1-120">1.2.840.113556.1.4.1367</span><span class="sxs-lookup"><span data-stu-id="1ace1-120">1.2.840.113556.1.4.1367</span></span>              |
| <span data-ttu-id="1ace1-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1ace1-121">System-Id-Guid</span></span>    | <span data-ttu-id="1ace1-122">5b5d448c-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="1ace1-122">5b5d448c-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="1ace1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ace1-123">Syntax</span></span>            | [<span data-ttu-id="1ace1-124">**間隔**</span><span class="sxs-lookup"><span data-stu-id="1ace1-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1ace1-125">實作</span><span class="sxs-lookup"><span data-stu-id="1ace1-125">Implementations</span></span>

-   [<span data-ttu-id="1ace1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ace1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ace1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ace1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ace1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ace1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ace1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ace1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ace1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ace1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ace1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ace1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ace1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ace1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1ace1-133">進入</span><span class="sxs-lookup"><span data-stu-id="1ace1-133">Entry</span></span> | <span data-ttu-id="1ace1-134">值</span><span class="sxs-lookup"><span data-stu-id="1ace1-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1ace1-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ace1-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ace1-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ace1-137">System-Only</span></span>            | <span data-ttu-id="1ace1-138">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-138">False</span></span>                                                     |
| <span data-ttu-id="1ace1-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ace1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1ace1-140">對</span><span class="sxs-lookup"><span data-stu-id="1ace1-140">True</span></span>                                                      |
| <span data-ttu-id="1ace1-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ace1-141">Is Indexed</span></span>             | <span data-ttu-id="1ace1-142">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-142">False</span></span>                                                     |
| <span data-ttu-id="1ace1-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ace1-143">In Global Catalog</span></span>      | <span data-ttu-id="1ace1-144">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-144">False</span></span>                                                     |
| <span data-ttu-id="1ace1-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ace1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ace1-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ace1-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1ace1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ace1-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ace1-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-149">Search-Flags</span></span>           | <span data-ttu-id="1ace1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ace1-150">0x00000000</span></span>                                                |
| <span data-ttu-id="1ace1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-151">System-Flags</span></span>           | <span data-ttu-id="1ace1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ace1-152">0x00000010</span></span>                                                |
| <span data-ttu-id="1ace1-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ace1-153">Classes used in</span></span>        | [<span data-ttu-id="1ace1-154">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ace1-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ace1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ace1-155">Windows Server 2003</span></span>



| <span data-ttu-id="1ace1-156">進入</span><span class="sxs-lookup"><span data-stu-id="1ace1-156">Entry</span></span> | <span data-ttu-id="1ace1-157">值</span><span class="sxs-lookup"><span data-stu-id="1ace1-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1ace1-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ace1-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ace1-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ace1-160">System-Only</span></span>            | <span data-ttu-id="1ace1-161">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-161">False</span></span>                                                     |
| <span data-ttu-id="1ace1-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ace1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1ace1-163">對</span><span class="sxs-lookup"><span data-stu-id="1ace1-163">True</span></span>                                                      |
| <span data-ttu-id="1ace1-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ace1-164">Is Indexed</span></span>             | <span data-ttu-id="1ace1-165">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-165">False</span></span>                                                     |
| <span data-ttu-id="1ace1-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ace1-166">In Global Catalog</span></span>      | <span data-ttu-id="1ace1-167">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-167">False</span></span>                                                     |
| <span data-ttu-id="1ace1-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ace1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ace1-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ace1-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1ace1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ace1-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ace1-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-172">Search-Flags</span></span>           | <span data-ttu-id="1ace1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ace1-173">0x00000000</span></span>                                                |
| <span data-ttu-id="1ace1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-174">System-Flags</span></span>           | <span data-ttu-id="1ace1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ace1-175">0x00000010</span></span>                                                |
| <span data-ttu-id="1ace1-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ace1-176">Classes used in</span></span>        | [<span data-ttu-id="1ace1-177">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ace1-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ace1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ace1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ace1-179">進入</span><span class="sxs-lookup"><span data-stu-id="1ace1-179">Entry</span></span> | <span data-ttu-id="1ace1-180">值</span><span class="sxs-lookup"><span data-stu-id="1ace1-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1ace1-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ace1-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ace1-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ace1-183">System-Only</span></span>            | <span data-ttu-id="1ace1-184">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-184">False</span></span>                                                     |
| <span data-ttu-id="1ace1-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ace1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="1ace1-186">對</span><span class="sxs-lookup"><span data-stu-id="1ace1-186">True</span></span>                                                      |
| <span data-ttu-id="1ace1-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ace1-187">Is Indexed</span></span>             | <span data-ttu-id="1ace1-188">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-188">False</span></span>                                                     |
| <span data-ttu-id="1ace1-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ace1-189">In Global Catalog</span></span>      | <span data-ttu-id="1ace1-190">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-190">False</span></span>                                                     |
| <span data-ttu-id="1ace1-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ace1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ace1-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ace1-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1ace1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ace1-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ace1-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-195">Search-Flags</span></span>           | <span data-ttu-id="1ace1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ace1-196">0x00000000</span></span>                                                |
| <span data-ttu-id="1ace1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-197">System-Flags</span></span>           | <span data-ttu-id="1ace1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ace1-198">0x00000010</span></span>                                                |
| <span data-ttu-id="1ace1-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ace1-199">Classes used in</span></span>        | [<span data-ttu-id="1ace1-200">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ace1-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ace1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ace1-201">Windows Server 2008</span></span>



| <span data-ttu-id="1ace1-202">進入</span><span class="sxs-lookup"><span data-stu-id="1ace1-202">Entry</span></span> | <span data-ttu-id="1ace1-203">值</span><span class="sxs-lookup"><span data-stu-id="1ace1-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1ace1-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ace1-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ace1-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ace1-206">System-Only</span></span>            | <span data-ttu-id="1ace1-207">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-207">False</span></span>                                                     |
| <span data-ttu-id="1ace1-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ace1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="1ace1-209">對</span><span class="sxs-lookup"><span data-stu-id="1ace1-209">True</span></span>                                                      |
| <span data-ttu-id="1ace1-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ace1-210">Is Indexed</span></span>             | <span data-ttu-id="1ace1-211">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-211">False</span></span>                                                     |
| <span data-ttu-id="1ace1-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ace1-212">In Global Catalog</span></span>      | <span data-ttu-id="1ace1-213">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-213">False</span></span>                                                     |
| <span data-ttu-id="1ace1-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ace1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ace1-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ace1-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1ace1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ace1-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ace1-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-218">Search-Flags</span></span>           | <span data-ttu-id="1ace1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ace1-219">0x00000000</span></span>                                                |
| <span data-ttu-id="1ace1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-220">System-Flags</span></span>           | <span data-ttu-id="1ace1-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ace1-221">0x00000010</span></span>                                                |
| <span data-ttu-id="1ace1-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ace1-222">Classes used in</span></span>        | [<span data-ttu-id="1ace1-223">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ace1-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ace1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ace1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ace1-225">進入</span><span class="sxs-lookup"><span data-stu-id="1ace1-225">Entry</span></span> | <span data-ttu-id="1ace1-226">值</span><span class="sxs-lookup"><span data-stu-id="1ace1-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1ace1-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ace1-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ace1-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ace1-229">System-Only</span></span>            | <span data-ttu-id="1ace1-230">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-230">False</span></span>                                                     |
| <span data-ttu-id="1ace1-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ace1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="1ace1-232">對</span><span class="sxs-lookup"><span data-stu-id="1ace1-232">True</span></span>                                                      |
| <span data-ttu-id="1ace1-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ace1-233">Is Indexed</span></span>             | <span data-ttu-id="1ace1-234">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-234">False</span></span>                                                     |
| <span data-ttu-id="1ace1-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ace1-235">In Global Catalog</span></span>      | <span data-ttu-id="1ace1-236">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-236">False</span></span>                                                     |
| <span data-ttu-id="1ace1-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ace1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ace1-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ace1-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1ace1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ace1-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ace1-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-241">Search-Flags</span></span>           | <span data-ttu-id="1ace1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ace1-242">0x00000000</span></span>                                                |
| <span data-ttu-id="1ace1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-243">System-Flags</span></span>           | <span data-ttu-id="1ace1-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ace1-244">0x00000010</span></span>                                                |
| <span data-ttu-id="1ace1-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ace1-245">Classes used in</span></span>        | [<span data-ttu-id="1ace1-246">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ace1-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ace1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ace1-247">Windows Server 2012</span></span>



| <span data-ttu-id="1ace1-248">進入</span><span class="sxs-lookup"><span data-stu-id="1ace1-248">Entry</span></span> | <span data-ttu-id="1ace1-249">值</span><span class="sxs-lookup"><span data-stu-id="1ace1-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1ace1-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1ace1-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ace1-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="1ace1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ace1-252">System-Only</span></span>            | <span data-ttu-id="1ace1-253">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-253">False</span></span>                                                     |
| <span data-ttu-id="1ace1-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1ace1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="1ace1-255">對</span><span class="sxs-lookup"><span data-stu-id="1ace1-255">True</span></span>                                                      |
| <span data-ttu-id="1ace1-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1ace1-256">Is Indexed</span></span>             | <span data-ttu-id="1ace1-257">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-257">False</span></span>                                                     |
| <span data-ttu-id="1ace1-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1ace1-258">In Global Catalog</span></span>      | <span data-ttu-id="1ace1-259">否</span><span class="sxs-lookup"><span data-stu-id="1ace1-259">False</span></span>                                                     |
| <span data-ttu-id="1ace1-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1ace1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ace1-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1ace1-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="1ace1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ace1-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ace1-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="1ace1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-264">Search-Flags</span></span>           | <span data-ttu-id="1ace1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ace1-265">0x00000000</span></span>                                                |
| <span data-ttu-id="1ace1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ace1-266">System-Flags</span></span>           | <span data-ttu-id="1ace1-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ace1-267">0x00000010</span></span>                                                |
| <span data-ttu-id="1ace1-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1ace1-268">Classes used in</span></span>        | [<span data-ttu-id="1ace1-269">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ace1-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





