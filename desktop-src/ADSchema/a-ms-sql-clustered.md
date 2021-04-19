---
title: MS-SQL-叢集屬性
description: 如果伺服器已叢集化，則為 True。
ms.assetid: 066609a4-fdf1-422b-9b26-445f617c99d4
ms.tgt_platform: multiple
keywords:
- MS-SQL-叢集屬性 AD 架構
- mS-SQL-叢集屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Clustered
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ba701168f3dff5b3809818a6df987855a08e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106988043"
---
# <a name="ms-sql-clustered-attribute"></a><span data-ttu-id="e212d-105">MS-SQL-叢集屬性</span><span class="sxs-lookup"><span data-stu-id="e212d-105">MS-SQL-Clustered attribute</span></span>

<span data-ttu-id="e212d-106">如果伺服器已叢集化，則為 True。</span><span class="sxs-lookup"><span data-stu-id="e212d-106">True if the server is clustered.</span></span>



| <span data-ttu-id="e212d-107">進入</span><span class="sxs-lookup"><span data-stu-id="e212d-107">Entry</span></span> | <span data-ttu-id="e212d-108">值</span><span class="sxs-lookup"><span data-stu-id="e212d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e212d-109">CN</span><span class="sxs-lookup"><span data-stu-id="e212d-109">CN</span></span>                | <span data-ttu-id="e212d-110">MS-CHAP-叢集</span><span class="sxs-lookup"><span data-stu-id="e212d-110">MS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="e212d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e212d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e212d-112">Ms-chap-叢集</span><span class="sxs-lookup"><span data-stu-id="e212d-112">mS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="e212d-113">大小</span><span class="sxs-lookup"><span data-stu-id="e212d-113">Size</span></span>              | <span data-ttu-id="e212d-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="e212d-114">4 bytes</span></span>                              |
| <span data-ttu-id="e212d-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e212d-115">Update Privilege</span></span>  | <span data-ttu-id="e212d-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="e212d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="e212d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e212d-117">Update Frequency</span></span>  | <span data-ttu-id="e212d-118">在系統啟動時。</span><span class="sxs-lookup"><span data-stu-id="e212d-118">At system startup.</span></span>                   |
| <span data-ttu-id="e212d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e212d-119">Attribute-Id</span></span>      | <span data-ttu-id="e212d-120">1.2.840.113556.1.4.1373</span><span class="sxs-lookup"><span data-stu-id="e212d-120">1.2.840.113556.1.4.1373</span></span>              |
| <span data-ttu-id="e212d-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e212d-121">System-Id-Guid</span></span>    | <span data-ttu-id="e212d-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e212d-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="e212d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e212d-123">Syntax</span></span>            | [<span data-ttu-id="e212d-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e212d-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="e212d-125">實作</span><span class="sxs-lookup"><span data-stu-id="e212d-125">Implementations</span></span>

-   [<span data-ttu-id="e212d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e212d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e212d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e212d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e212d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e212d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e212d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e212d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e212d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e212d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e212d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e212d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e212d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e212d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e212d-133">進入</span><span class="sxs-lookup"><span data-stu-id="e212d-133">Entry</span></span> | <span data-ttu-id="e212d-134">值</span><span class="sxs-lookup"><span data-stu-id="e212d-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e212d-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e212d-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e212d-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e212d-137">System-Only</span></span>            | <span data-ttu-id="e212d-138">否</span><span class="sxs-lookup"><span data-stu-id="e212d-138">False</span></span>                                                     |
| <span data-ttu-id="e212d-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e212d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e212d-140">對</span><span class="sxs-lookup"><span data-stu-id="e212d-140">True</span></span>                                                      |
| <span data-ttu-id="e212d-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e212d-141">Is Indexed</span></span>             | <span data-ttu-id="e212d-142">否</span><span class="sxs-lookup"><span data-stu-id="e212d-142">False</span></span>                                                     |
| <span data-ttu-id="e212d-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e212d-143">In Global Catalog</span></span>      | <span data-ttu-id="e212d-144">否</span><span class="sxs-lookup"><span data-stu-id="e212d-144">False</span></span>                                                     |
| <span data-ttu-id="e212d-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e212d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e212d-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e212d-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e212d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e212d-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e212d-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-149">Search-Flags</span></span>           | <span data-ttu-id="e212d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e212d-150">0x00000000</span></span>                                                |
| <span data-ttu-id="e212d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-151">System-Flags</span></span>           | <span data-ttu-id="e212d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e212d-152">0x00000010</span></span>                                                |
| <span data-ttu-id="e212d-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e212d-153">Classes used in</span></span>        | [<span data-ttu-id="e212d-154">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e212d-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e212d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e212d-155">Windows Server 2003</span></span>



| <span data-ttu-id="e212d-156">進入</span><span class="sxs-lookup"><span data-stu-id="e212d-156">Entry</span></span> | <span data-ttu-id="e212d-157">值</span><span class="sxs-lookup"><span data-stu-id="e212d-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e212d-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e212d-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e212d-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e212d-160">System-Only</span></span>            | <span data-ttu-id="e212d-161">否</span><span class="sxs-lookup"><span data-stu-id="e212d-161">False</span></span>                                                     |
| <span data-ttu-id="e212d-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e212d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e212d-163">對</span><span class="sxs-lookup"><span data-stu-id="e212d-163">True</span></span>                                                      |
| <span data-ttu-id="e212d-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e212d-164">Is Indexed</span></span>             | <span data-ttu-id="e212d-165">否</span><span class="sxs-lookup"><span data-stu-id="e212d-165">False</span></span>                                                     |
| <span data-ttu-id="e212d-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e212d-166">In Global Catalog</span></span>      | <span data-ttu-id="e212d-167">否</span><span class="sxs-lookup"><span data-stu-id="e212d-167">False</span></span>                                                     |
| <span data-ttu-id="e212d-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e212d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e212d-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e212d-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e212d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e212d-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e212d-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-172">Search-Flags</span></span>           | <span data-ttu-id="e212d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e212d-173">0x00000000</span></span>                                                |
| <span data-ttu-id="e212d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-174">System-Flags</span></span>           | <span data-ttu-id="e212d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e212d-175">0x00000010</span></span>                                                |
| <span data-ttu-id="e212d-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e212d-176">Classes used in</span></span>        | [<span data-ttu-id="e212d-177">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e212d-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e212d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e212d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e212d-179">進入</span><span class="sxs-lookup"><span data-stu-id="e212d-179">Entry</span></span> | <span data-ttu-id="e212d-180">值</span><span class="sxs-lookup"><span data-stu-id="e212d-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e212d-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e212d-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e212d-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e212d-183">System-Only</span></span>            | <span data-ttu-id="e212d-184">否</span><span class="sxs-lookup"><span data-stu-id="e212d-184">False</span></span>                                                     |
| <span data-ttu-id="e212d-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e212d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e212d-186">對</span><span class="sxs-lookup"><span data-stu-id="e212d-186">True</span></span>                                                      |
| <span data-ttu-id="e212d-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e212d-187">Is Indexed</span></span>             | <span data-ttu-id="e212d-188">否</span><span class="sxs-lookup"><span data-stu-id="e212d-188">False</span></span>                                                     |
| <span data-ttu-id="e212d-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e212d-189">In Global Catalog</span></span>      | <span data-ttu-id="e212d-190">否</span><span class="sxs-lookup"><span data-stu-id="e212d-190">False</span></span>                                                     |
| <span data-ttu-id="e212d-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e212d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e212d-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e212d-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e212d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e212d-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e212d-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-195">Search-Flags</span></span>           | <span data-ttu-id="e212d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e212d-196">0x00000000</span></span>                                                |
| <span data-ttu-id="e212d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-197">System-Flags</span></span>           | <span data-ttu-id="e212d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e212d-198">0x00000010</span></span>                                                |
| <span data-ttu-id="e212d-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e212d-199">Classes used in</span></span>        | [<span data-ttu-id="e212d-200">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e212d-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e212d-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e212d-201">Windows Server 2008</span></span>



| <span data-ttu-id="e212d-202">進入</span><span class="sxs-lookup"><span data-stu-id="e212d-202">Entry</span></span> | <span data-ttu-id="e212d-203">值</span><span class="sxs-lookup"><span data-stu-id="e212d-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e212d-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e212d-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e212d-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e212d-206">System-Only</span></span>            | <span data-ttu-id="e212d-207">否</span><span class="sxs-lookup"><span data-stu-id="e212d-207">False</span></span>                                                     |
| <span data-ttu-id="e212d-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e212d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e212d-209">對</span><span class="sxs-lookup"><span data-stu-id="e212d-209">True</span></span>                                                      |
| <span data-ttu-id="e212d-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e212d-210">Is Indexed</span></span>             | <span data-ttu-id="e212d-211">否</span><span class="sxs-lookup"><span data-stu-id="e212d-211">False</span></span>                                                     |
| <span data-ttu-id="e212d-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e212d-212">In Global Catalog</span></span>      | <span data-ttu-id="e212d-213">否</span><span class="sxs-lookup"><span data-stu-id="e212d-213">False</span></span>                                                     |
| <span data-ttu-id="e212d-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e212d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e212d-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e212d-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e212d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e212d-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e212d-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-218">Search-Flags</span></span>           | <span data-ttu-id="e212d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e212d-219">0x00000000</span></span>                                                |
| <span data-ttu-id="e212d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-220">System-Flags</span></span>           | <span data-ttu-id="e212d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e212d-221">0x00000010</span></span>                                                |
| <span data-ttu-id="e212d-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e212d-222">Classes used in</span></span>        | [<span data-ttu-id="e212d-223">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e212d-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e212d-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e212d-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e212d-225">進入</span><span class="sxs-lookup"><span data-stu-id="e212d-225">Entry</span></span> | <span data-ttu-id="e212d-226">值</span><span class="sxs-lookup"><span data-stu-id="e212d-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e212d-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e212d-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e212d-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="e212d-229">System-Only</span></span>            | <span data-ttu-id="e212d-230">否</span><span class="sxs-lookup"><span data-stu-id="e212d-230">False</span></span>                                                     |
| <span data-ttu-id="e212d-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e212d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="e212d-232">對</span><span class="sxs-lookup"><span data-stu-id="e212d-232">True</span></span>                                                      |
| <span data-ttu-id="e212d-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e212d-233">Is Indexed</span></span>             | <span data-ttu-id="e212d-234">否</span><span class="sxs-lookup"><span data-stu-id="e212d-234">False</span></span>                                                     |
| <span data-ttu-id="e212d-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e212d-235">In Global Catalog</span></span>      | <span data-ttu-id="e212d-236">否</span><span class="sxs-lookup"><span data-stu-id="e212d-236">False</span></span>                                                     |
| <span data-ttu-id="e212d-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e212d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="e212d-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e212d-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e212d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e212d-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e212d-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-241">Search-Flags</span></span>           | <span data-ttu-id="e212d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e212d-242">0x00000000</span></span>                                                |
| <span data-ttu-id="e212d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-243">System-Flags</span></span>           | <span data-ttu-id="e212d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e212d-244">0x00000010</span></span>                                                |
| <span data-ttu-id="e212d-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e212d-245">Classes used in</span></span>        | [<span data-ttu-id="e212d-246">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e212d-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e212d-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e212d-247">Windows Server 2012</span></span>



| <span data-ttu-id="e212d-248">進入</span><span class="sxs-lookup"><span data-stu-id="e212d-248">Entry</span></span> | <span data-ttu-id="e212d-249">值</span><span class="sxs-lookup"><span data-stu-id="e212d-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e212d-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e212d-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e212d-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="e212d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="e212d-252">System-Only</span></span>            | <span data-ttu-id="e212d-253">否</span><span class="sxs-lookup"><span data-stu-id="e212d-253">False</span></span>                                                     |
| <span data-ttu-id="e212d-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e212d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="e212d-255">對</span><span class="sxs-lookup"><span data-stu-id="e212d-255">True</span></span>                                                      |
| <span data-ttu-id="e212d-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e212d-256">Is Indexed</span></span>             | <span data-ttu-id="e212d-257">否</span><span class="sxs-lookup"><span data-stu-id="e212d-257">False</span></span>                                                     |
| <span data-ttu-id="e212d-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e212d-258">In Global Catalog</span></span>      | <span data-ttu-id="e212d-259">否</span><span class="sxs-lookup"><span data-stu-id="e212d-259">False</span></span>                                                     |
| <span data-ttu-id="e212d-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e212d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="e212d-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e212d-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="e212d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e212d-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e212d-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="e212d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-264">Search-Flags</span></span>           | <span data-ttu-id="e212d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e212d-265">0x00000000</span></span>                                                |
| <span data-ttu-id="e212d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e212d-266">System-Flags</span></span>           | <span data-ttu-id="e212d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e212d-267">0x00000010</span></span>                                                |
| <span data-ttu-id="e212d-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e212d-268">Classes used in</span></span>        | [<span data-ttu-id="e212d-269">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="e212d-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





