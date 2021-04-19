---
title: MS-CHAP-多重通訊協定屬性
description: RPC 連接點。
ms.assetid: 70cb9f80-7140-4c26-a1a4-f78a60de430f
ms.tgt_platform: multiple
keywords:
- MS-CHAP-多重通訊協定屬性 AD 架構
- Ms-chap-多重通訊協定屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-MultiProtocol
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cdfb8e42d8e3d533090b7b0bf49dcefc5492a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106979699"
---
# <a name="ms-sql-multiprotocol-attribute"></a><span data-ttu-id="8dd31-105">MS-CHAP-多重通訊協定屬性</span><span class="sxs-lookup"><span data-stu-id="8dd31-105">MS-SQL-MultiProtocol attribute</span></span>

<span data-ttu-id="8dd31-106">RPC 連接點。</span><span class="sxs-lookup"><span data-stu-id="8dd31-106">The RPC connection point.</span></span>



| <span data-ttu-id="8dd31-107">進入</span><span class="sxs-lookup"><span data-stu-id="8dd31-107">Entry</span></span> | <span data-ttu-id="8dd31-108">值</span><span class="sxs-lookup"><span data-stu-id="8dd31-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8dd31-109">CN</span><span class="sxs-lookup"><span data-stu-id="8dd31-109">CN</span></span>                | <span data-ttu-id="8dd31-110">MS-CHAP-多重通訊協定</span><span class="sxs-lookup"><span data-stu-id="8dd31-110">MS-SQL-MultiProtocol</span></span>                        |
| <span data-ttu-id="8dd31-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8dd31-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8dd31-112">Ms-chap-多重通訊協定</span><span class="sxs-lookup"><span data-stu-id="8dd31-112">mS-SQL-MultiProtocol</span></span>                        |
| <span data-ttu-id="8dd31-113">大小</span><span class="sxs-lookup"><span data-stu-id="8dd31-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8dd31-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8dd31-114">Update Privilege</span></span>  | <span data-ttu-id="8dd31-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="8dd31-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="8dd31-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8dd31-116">Update Frequency</span></span>  | <span data-ttu-id="8dd31-117">在系統啟動時。</span><span class="sxs-lookup"><span data-stu-id="8dd31-117">At system startup.</span></span>                          |
| <span data-ttu-id="8dd31-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8dd31-118">Attribute-Id</span></span>      | <span data-ttu-id="8dd31-119">1.2.840.113556.1.4.1375</span><span class="sxs-lookup"><span data-stu-id="8dd31-119">1.2.840.113556.1.4.1375</span></span>                     |
| <span data-ttu-id="8dd31-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8dd31-120">System-Id-Guid</span></span>    | <span data-ttu-id="8dd31-121">8157fa38-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="8dd31-121">8157fa38-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="8dd31-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dd31-122">Syntax</span></span>            | [<span data-ttu-id="8dd31-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8dd31-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8dd31-124">實作</span><span class="sxs-lookup"><span data-stu-id="8dd31-124">Implementations</span></span>

-   [<span data-ttu-id="8dd31-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8dd31-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8dd31-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8dd31-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8dd31-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8dd31-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8dd31-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8dd31-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8dd31-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8dd31-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8dd31-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8dd31-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8dd31-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8dd31-131">Windows 2000 Server</span></span>



| <span data-ttu-id="8dd31-132">進入</span><span class="sxs-lookup"><span data-stu-id="8dd31-132">Entry</span></span> | <span data-ttu-id="8dd31-133">值</span><span class="sxs-lookup"><span data-stu-id="8dd31-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8dd31-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8dd31-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dd31-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dd31-136">System-Only</span></span>            | <span data-ttu-id="8dd31-137">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-137">False</span></span>                                                     |
| <span data-ttu-id="8dd31-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8dd31-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8dd31-139">對</span><span class="sxs-lookup"><span data-stu-id="8dd31-139">True</span></span>                                                      |
| <span data-ttu-id="8dd31-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8dd31-140">Is Indexed</span></span>             | <span data-ttu-id="8dd31-141">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-141">False</span></span>                                                     |
| <span data-ttu-id="8dd31-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8dd31-142">In Global Catalog</span></span>      | <span data-ttu-id="8dd31-143">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-143">False</span></span>                                                     |
| <span data-ttu-id="8dd31-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8dd31-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dd31-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8dd31-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8dd31-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dd31-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dd31-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-148">Search-Flags</span></span>           | <span data-ttu-id="8dd31-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dd31-149">0x00000000</span></span>                                                |
| <span data-ttu-id="8dd31-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-150">System-Flags</span></span>           | <span data-ttu-id="8dd31-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dd31-151">0x00000010</span></span>                                                |
| <span data-ttu-id="8dd31-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8dd31-152">Classes used in</span></span>        | [<span data-ttu-id="8dd31-153">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8dd31-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8dd31-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8dd31-154">Windows Server 2003</span></span>



| <span data-ttu-id="8dd31-155">進入</span><span class="sxs-lookup"><span data-stu-id="8dd31-155">Entry</span></span> | <span data-ttu-id="8dd31-156">值</span><span class="sxs-lookup"><span data-stu-id="8dd31-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8dd31-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8dd31-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dd31-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dd31-159">System-Only</span></span>            | <span data-ttu-id="8dd31-160">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-160">False</span></span>                                                     |
| <span data-ttu-id="8dd31-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8dd31-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8dd31-162">對</span><span class="sxs-lookup"><span data-stu-id="8dd31-162">True</span></span>                                                      |
| <span data-ttu-id="8dd31-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8dd31-163">Is Indexed</span></span>             | <span data-ttu-id="8dd31-164">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-164">False</span></span>                                                     |
| <span data-ttu-id="8dd31-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8dd31-165">In Global Catalog</span></span>      | <span data-ttu-id="8dd31-166">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-166">False</span></span>                                                     |
| <span data-ttu-id="8dd31-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8dd31-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dd31-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8dd31-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8dd31-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dd31-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dd31-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-171">Search-Flags</span></span>           | <span data-ttu-id="8dd31-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dd31-172">0x00000000</span></span>                                                |
| <span data-ttu-id="8dd31-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-173">System-Flags</span></span>           | <span data-ttu-id="8dd31-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dd31-174">0x00000010</span></span>                                                |
| <span data-ttu-id="8dd31-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8dd31-175">Classes used in</span></span>        | [<span data-ttu-id="8dd31-176">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8dd31-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8dd31-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8dd31-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8dd31-178">進入</span><span class="sxs-lookup"><span data-stu-id="8dd31-178">Entry</span></span> | <span data-ttu-id="8dd31-179">值</span><span class="sxs-lookup"><span data-stu-id="8dd31-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8dd31-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8dd31-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dd31-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dd31-182">System-Only</span></span>            | <span data-ttu-id="8dd31-183">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-183">False</span></span>                                                     |
| <span data-ttu-id="8dd31-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8dd31-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8dd31-185">對</span><span class="sxs-lookup"><span data-stu-id="8dd31-185">True</span></span>                                                      |
| <span data-ttu-id="8dd31-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8dd31-186">Is Indexed</span></span>             | <span data-ttu-id="8dd31-187">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-187">False</span></span>                                                     |
| <span data-ttu-id="8dd31-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8dd31-188">In Global Catalog</span></span>      | <span data-ttu-id="8dd31-189">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-189">False</span></span>                                                     |
| <span data-ttu-id="8dd31-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8dd31-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dd31-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8dd31-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8dd31-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dd31-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dd31-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-194">Search-Flags</span></span>           | <span data-ttu-id="8dd31-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dd31-195">0x00000000</span></span>                                                |
| <span data-ttu-id="8dd31-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-196">System-Flags</span></span>           | <span data-ttu-id="8dd31-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dd31-197">0x00000010</span></span>                                                |
| <span data-ttu-id="8dd31-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8dd31-198">Classes used in</span></span>        | [<span data-ttu-id="8dd31-199">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8dd31-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8dd31-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dd31-200">Windows Server 2008</span></span>



| <span data-ttu-id="8dd31-201">進入</span><span class="sxs-lookup"><span data-stu-id="8dd31-201">Entry</span></span> | <span data-ttu-id="8dd31-202">值</span><span class="sxs-lookup"><span data-stu-id="8dd31-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8dd31-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8dd31-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dd31-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dd31-205">System-Only</span></span>            | <span data-ttu-id="8dd31-206">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-206">False</span></span>                                                     |
| <span data-ttu-id="8dd31-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8dd31-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8dd31-208">對</span><span class="sxs-lookup"><span data-stu-id="8dd31-208">True</span></span>                                                      |
| <span data-ttu-id="8dd31-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8dd31-209">Is Indexed</span></span>             | <span data-ttu-id="8dd31-210">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-210">False</span></span>                                                     |
| <span data-ttu-id="8dd31-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8dd31-211">In Global Catalog</span></span>      | <span data-ttu-id="8dd31-212">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-212">False</span></span>                                                     |
| <span data-ttu-id="8dd31-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8dd31-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dd31-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8dd31-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8dd31-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dd31-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dd31-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-217">Search-Flags</span></span>           | <span data-ttu-id="8dd31-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dd31-218">0x00000000</span></span>                                                |
| <span data-ttu-id="8dd31-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-219">System-Flags</span></span>           | <span data-ttu-id="8dd31-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dd31-220">0x00000010</span></span>                                                |
| <span data-ttu-id="8dd31-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8dd31-221">Classes used in</span></span>        | [<span data-ttu-id="8dd31-222">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8dd31-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8dd31-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8dd31-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8dd31-224">進入</span><span class="sxs-lookup"><span data-stu-id="8dd31-224">Entry</span></span> | <span data-ttu-id="8dd31-225">值</span><span class="sxs-lookup"><span data-stu-id="8dd31-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8dd31-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8dd31-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dd31-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dd31-228">System-Only</span></span>            | <span data-ttu-id="8dd31-229">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-229">False</span></span>                                                     |
| <span data-ttu-id="8dd31-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8dd31-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8dd31-231">對</span><span class="sxs-lookup"><span data-stu-id="8dd31-231">True</span></span>                                                      |
| <span data-ttu-id="8dd31-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8dd31-232">Is Indexed</span></span>             | <span data-ttu-id="8dd31-233">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-233">False</span></span>                                                     |
| <span data-ttu-id="8dd31-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8dd31-234">In Global Catalog</span></span>      | <span data-ttu-id="8dd31-235">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-235">False</span></span>                                                     |
| <span data-ttu-id="8dd31-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8dd31-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dd31-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8dd31-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8dd31-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dd31-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dd31-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-240">Search-Flags</span></span>           | <span data-ttu-id="8dd31-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dd31-241">0x00000000</span></span>                                                |
| <span data-ttu-id="8dd31-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-242">System-Flags</span></span>           | <span data-ttu-id="8dd31-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dd31-243">0x00000010</span></span>                                                |
| <span data-ttu-id="8dd31-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8dd31-244">Classes used in</span></span>        | [<span data-ttu-id="8dd31-245">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8dd31-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8dd31-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8dd31-246">Windows Server 2012</span></span>



| <span data-ttu-id="8dd31-247">進入</span><span class="sxs-lookup"><span data-stu-id="8dd31-247">Entry</span></span> | <span data-ttu-id="8dd31-248">值</span><span class="sxs-lookup"><span data-stu-id="8dd31-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8dd31-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8dd31-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dd31-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="8dd31-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dd31-251">System-Only</span></span>            | <span data-ttu-id="8dd31-252">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-252">False</span></span>                                                     |
| <span data-ttu-id="8dd31-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8dd31-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8dd31-254">對</span><span class="sxs-lookup"><span data-stu-id="8dd31-254">True</span></span>                                                      |
| <span data-ttu-id="8dd31-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8dd31-255">Is Indexed</span></span>             | <span data-ttu-id="8dd31-256">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-256">False</span></span>                                                     |
| <span data-ttu-id="8dd31-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8dd31-257">In Global Catalog</span></span>      | <span data-ttu-id="8dd31-258">否</span><span class="sxs-lookup"><span data-stu-id="8dd31-258">False</span></span>                                                     |
| <span data-ttu-id="8dd31-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8dd31-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dd31-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8dd31-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="8dd31-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dd31-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dd31-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="8dd31-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-263">Search-Flags</span></span>           | <span data-ttu-id="8dd31-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dd31-264">0x00000000</span></span>                                                |
| <span data-ttu-id="8dd31-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dd31-265">System-Flags</span></span>           | <span data-ttu-id="8dd31-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dd31-266">0x00000010</span></span>                                                |
| <span data-ttu-id="8dd31-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8dd31-267">Classes used in</span></span>        | [<span data-ttu-id="8dd31-268">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="8dd31-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





