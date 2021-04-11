---
title: NamedPipe 屬性
description: 具名管道連接。
ms.assetid: d18c911d-06ed-4d08-b584-7b2748620770
ms.tgt_platform: multiple
keywords:
- NamedPipe 屬性 AD 架構
- NamedPipe 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-NamedPipe
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33e231be0561ae8c0e885911cb92954d6ff0d20d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385334"
---
# <a name="ms-sql-namedpipe-attribute"></a><span data-ttu-id="99e3b-105">NamedPipe 屬性</span><span class="sxs-lookup"><span data-stu-id="99e3b-105">MS-SQL-NamedPipe attribute</span></span>

<span data-ttu-id="99e3b-106">具名管道連接。</span><span class="sxs-lookup"><span data-stu-id="99e3b-106">The named pipe connection.</span></span>



| <span data-ttu-id="99e3b-107">進入</span><span class="sxs-lookup"><span data-stu-id="99e3b-107">Entry</span></span> | <span data-ttu-id="99e3b-108">值</span><span class="sxs-lookup"><span data-stu-id="99e3b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="99e3b-109">CN</span><span class="sxs-lookup"><span data-stu-id="99e3b-109">CN</span></span>                | <span data-ttu-id="99e3b-110">NamedPipe</span><span class="sxs-lookup"><span data-stu-id="99e3b-110">MS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="99e3b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="99e3b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="99e3b-112">NamedPipe</span><span class="sxs-lookup"><span data-stu-id="99e3b-112">mS-SQL-NamedPipe</span></span>                            |
| <span data-ttu-id="99e3b-113">大小</span><span class="sxs-lookup"><span data-stu-id="99e3b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="99e3b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="99e3b-114">Update Privilege</span></span>  | <span data-ttu-id="99e3b-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="99e3b-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="99e3b-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="99e3b-116">Update Frequency</span></span>  | <span data-ttu-id="99e3b-117">在系統啟動時。</span><span class="sxs-lookup"><span data-stu-id="99e3b-117">At system startup.</span></span>                          |
| <span data-ttu-id="99e3b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99e3b-118">Attribute-Id</span></span>      | <span data-ttu-id="99e3b-119">1.2.840.113556.1.4.1374</span><span class="sxs-lookup"><span data-stu-id="99e3b-119">1.2.840.113556.1.4.1374</span></span>                     |
| <span data-ttu-id="99e3b-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="99e3b-120">System-Id-Guid</span></span>    | <span data-ttu-id="99e3b-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="99e3b-121">7b91c840-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="99e3b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="99e3b-122">Syntax</span></span>            | [<span data-ttu-id="99e3b-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="99e3b-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="99e3b-124">實作</span><span class="sxs-lookup"><span data-stu-id="99e3b-124">Implementations</span></span>

-   [<span data-ttu-id="99e3b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="99e3b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="99e3b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99e3b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99e3b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99e3b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99e3b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99e3b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99e3b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99e3b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99e3b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99e3b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="99e3b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99e3b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="99e3b-132">進入</span><span class="sxs-lookup"><span data-stu-id="99e3b-132">Entry</span></span> | <span data-ttu-id="99e3b-133">值</span><span class="sxs-lookup"><span data-stu-id="99e3b-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="99e3b-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99e3b-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99e3b-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="99e3b-136">System-Only</span></span>            | <span data-ttu-id="99e3b-137">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-137">False</span></span>                                                     |
| <span data-ttu-id="99e3b-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99e3b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="99e3b-139">對</span><span class="sxs-lookup"><span data-stu-id="99e3b-139">True</span></span>                                                      |
| <span data-ttu-id="99e3b-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99e3b-140">Is Indexed</span></span>             | <span data-ttu-id="99e3b-141">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-141">False</span></span>                                                     |
| <span data-ttu-id="99e3b-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99e3b-142">In Global Catalog</span></span>      | <span data-ttu-id="99e3b-143">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-143">False</span></span>                                                     |
| <span data-ttu-id="99e3b-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99e3b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="99e3b-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99e3b-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="99e3b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99e3b-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99e3b-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-148">Search-Flags</span></span>           | <span data-ttu-id="99e3b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99e3b-149">0x00000000</span></span>                                                |
| <span data-ttu-id="99e3b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-150">System-Flags</span></span>           | <span data-ttu-id="99e3b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99e3b-151">0x00000010</span></span>                                                |
| <span data-ttu-id="99e3b-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99e3b-152">Classes used in</span></span>        | [<span data-ttu-id="99e3b-153">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="99e3b-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="99e3b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99e3b-154">Windows Server 2003</span></span>



| <span data-ttu-id="99e3b-155">進入</span><span class="sxs-lookup"><span data-stu-id="99e3b-155">Entry</span></span> | <span data-ttu-id="99e3b-156">值</span><span class="sxs-lookup"><span data-stu-id="99e3b-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="99e3b-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99e3b-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99e3b-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="99e3b-159">System-Only</span></span>            | <span data-ttu-id="99e3b-160">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-160">False</span></span>                                                     |
| <span data-ttu-id="99e3b-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99e3b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="99e3b-162">對</span><span class="sxs-lookup"><span data-stu-id="99e3b-162">True</span></span>                                                      |
| <span data-ttu-id="99e3b-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99e3b-163">Is Indexed</span></span>             | <span data-ttu-id="99e3b-164">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-164">False</span></span>                                                     |
| <span data-ttu-id="99e3b-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99e3b-165">In Global Catalog</span></span>      | <span data-ttu-id="99e3b-166">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-166">False</span></span>                                                     |
| <span data-ttu-id="99e3b-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99e3b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="99e3b-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99e3b-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="99e3b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99e3b-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99e3b-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-171">Search-Flags</span></span>           | <span data-ttu-id="99e3b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99e3b-172">0x00000000</span></span>                                                |
| <span data-ttu-id="99e3b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-173">System-Flags</span></span>           | <span data-ttu-id="99e3b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99e3b-174">0x00000010</span></span>                                                |
| <span data-ttu-id="99e3b-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99e3b-175">Classes used in</span></span>        | [<span data-ttu-id="99e3b-176">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="99e3b-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99e3b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99e3b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99e3b-178">進入</span><span class="sxs-lookup"><span data-stu-id="99e3b-178">Entry</span></span> | <span data-ttu-id="99e3b-179">值</span><span class="sxs-lookup"><span data-stu-id="99e3b-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="99e3b-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99e3b-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99e3b-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="99e3b-182">System-Only</span></span>            | <span data-ttu-id="99e3b-183">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-183">False</span></span>                                                     |
| <span data-ttu-id="99e3b-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99e3b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="99e3b-185">對</span><span class="sxs-lookup"><span data-stu-id="99e3b-185">True</span></span>                                                      |
| <span data-ttu-id="99e3b-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99e3b-186">Is Indexed</span></span>             | <span data-ttu-id="99e3b-187">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-187">False</span></span>                                                     |
| <span data-ttu-id="99e3b-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99e3b-188">In Global Catalog</span></span>      | <span data-ttu-id="99e3b-189">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-189">False</span></span>                                                     |
| <span data-ttu-id="99e3b-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99e3b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="99e3b-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99e3b-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="99e3b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99e3b-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99e3b-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-194">Search-Flags</span></span>           | <span data-ttu-id="99e3b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99e3b-195">0x00000000</span></span>                                                |
| <span data-ttu-id="99e3b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-196">System-Flags</span></span>           | <span data-ttu-id="99e3b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99e3b-197">0x00000010</span></span>                                                |
| <span data-ttu-id="99e3b-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99e3b-198">Classes used in</span></span>        | [<span data-ttu-id="99e3b-199">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="99e3b-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99e3b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99e3b-200">Windows Server 2008</span></span>



| <span data-ttu-id="99e3b-201">進入</span><span class="sxs-lookup"><span data-stu-id="99e3b-201">Entry</span></span> | <span data-ttu-id="99e3b-202">值</span><span class="sxs-lookup"><span data-stu-id="99e3b-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="99e3b-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99e3b-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99e3b-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="99e3b-205">System-Only</span></span>            | <span data-ttu-id="99e3b-206">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-206">False</span></span>                                                     |
| <span data-ttu-id="99e3b-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99e3b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="99e3b-208">對</span><span class="sxs-lookup"><span data-stu-id="99e3b-208">True</span></span>                                                      |
| <span data-ttu-id="99e3b-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99e3b-209">Is Indexed</span></span>             | <span data-ttu-id="99e3b-210">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-210">False</span></span>                                                     |
| <span data-ttu-id="99e3b-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99e3b-211">In Global Catalog</span></span>      | <span data-ttu-id="99e3b-212">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-212">False</span></span>                                                     |
| <span data-ttu-id="99e3b-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99e3b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="99e3b-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99e3b-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="99e3b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99e3b-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99e3b-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-217">Search-Flags</span></span>           | <span data-ttu-id="99e3b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99e3b-218">0x00000000</span></span>                                                |
| <span data-ttu-id="99e3b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-219">System-Flags</span></span>           | <span data-ttu-id="99e3b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99e3b-220">0x00000010</span></span>                                                |
| <span data-ttu-id="99e3b-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99e3b-221">Classes used in</span></span>        | [<span data-ttu-id="99e3b-222">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="99e3b-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99e3b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99e3b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99e3b-224">進入</span><span class="sxs-lookup"><span data-stu-id="99e3b-224">Entry</span></span> | <span data-ttu-id="99e3b-225">值</span><span class="sxs-lookup"><span data-stu-id="99e3b-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="99e3b-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99e3b-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99e3b-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="99e3b-228">System-Only</span></span>            | <span data-ttu-id="99e3b-229">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-229">False</span></span>                                                     |
| <span data-ttu-id="99e3b-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99e3b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="99e3b-231">對</span><span class="sxs-lookup"><span data-stu-id="99e3b-231">True</span></span>                                                      |
| <span data-ttu-id="99e3b-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99e3b-232">Is Indexed</span></span>             | <span data-ttu-id="99e3b-233">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-233">False</span></span>                                                     |
| <span data-ttu-id="99e3b-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99e3b-234">In Global Catalog</span></span>      | <span data-ttu-id="99e3b-235">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-235">False</span></span>                                                     |
| <span data-ttu-id="99e3b-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99e3b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="99e3b-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99e3b-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="99e3b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99e3b-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99e3b-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-240">Search-Flags</span></span>           | <span data-ttu-id="99e3b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99e3b-241">0x00000000</span></span>                                                |
| <span data-ttu-id="99e3b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-242">System-Flags</span></span>           | <span data-ttu-id="99e3b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99e3b-243">0x00000010</span></span>                                                |
| <span data-ttu-id="99e3b-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99e3b-244">Classes used in</span></span>        | [<span data-ttu-id="99e3b-245">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="99e3b-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99e3b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99e3b-246">Windows Server 2012</span></span>



| <span data-ttu-id="99e3b-247">進入</span><span class="sxs-lookup"><span data-stu-id="99e3b-247">Entry</span></span> | <span data-ttu-id="99e3b-248">值</span><span class="sxs-lookup"><span data-stu-id="99e3b-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="99e3b-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="99e3b-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99e3b-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="99e3b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="99e3b-251">System-Only</span></span>            | <span data-ttu-id="99e3b-252">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-252">False</span></span>                                                     |
| <span data-ttu-id="99e3b-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="99e3b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="99e3b-254">對</span><span class="sxs-lookup"><span data-stu-id="99e3b-254">True</span></span>                                                      |
| <span data-ttu-id="99e3b-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="99e3b-255">Is Indexed</span></span>             | <span data-ttu-id="99e3b-256">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-256">False</span></span>                                                     |
| <span data-ttu-id="99e3b-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="99e3b-257">In Global Catalog</span></span>      | <span data-ttu-id="99e3b-258">否</span><span class="sxs-lookup"><span data-stu-id="99e3b-258">False</span></span>                                                     |
| <span data-ttu-id="99e3b-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="99e3b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="99e3b-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="99e3b-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="99e3b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99e3b-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99e3b-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="99e3b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-263">Search-Flags</span></span>           | <span data-ttu-id="99e3b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99e3b-264">0x00000000</span></span>                                                |
| <span data-ttu-id="99e3b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99e3b-265">System-Flags</span></span>           | <span data-ttu-id="99e3b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99e3b-266">0x00000010</span></span>                                                |
| <span data-ttu-id="99e3b-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="99e3b-267">Classes used in</span></span>        | [<span data-ttu-id="99e3b-268">**MS-CHAP-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="99e3b-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





