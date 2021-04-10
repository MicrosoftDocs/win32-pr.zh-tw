---
title: MS-CHAP-Language 屬性
description: SQL Server 目前實例的語言。
ms.assetid: 70ab1e8f-aff0-4a1e-ab2c-676a77b0c229
ms.tgt_platform: multiple
keywords:
- MS-CHAP-Language 屬性 AD 架構
- Ms-chap-Language 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Language
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fd9a4fb6ede4e656b7cebbfe7c5c920e19d9123
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107171"
---
# <a name="ms-sql-language-attribute"></a><span data-ttu-id="bad5f-105">MS-CHAP-Language 屬性</span><span class="sxs-lookup"><span data-stu-id="bad5f-105">MS-SQL-Language attribute</span></span>

<span data-ttu-id="bad5f-106">SQL Server 目前實例的語言。</span><span class="sxs-lookup"><span data-stu-id="bad5f-106">The language for the current instance of SQL Server.</span></span>



| <span data-ttu-id="bad5f-107">進入</span><span class="sxs-lookup"><span data-stu-id="bad5f-107">Entry</span></span> | <span data-ttu-id="bad5f-108">值</span><span class="sxs-lookup"><span data-stu-id="bad5f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bad5f-109">CN</span><span class="sxs-lookup"><span data-stu-id="bad5f-109">CN</span></span>                | <span data-ttu-id="bad5f-110">MS-CHAP-語言</span><span class="sxs-lookup"><span data-stu-id="bad5f-110">MS-SQL-Language</span></span>                             |
| <span data-ttu-id="bad5f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bad5f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bad5f-112">Ms-chap-語言</span><span class="sxs-lookup"><span data-stu-id="bad5f-112">mS-SQL-Language</span></span>                             |
| <span data-ttu-id="bad5f-113">大小</span><span class="sxs-lookup"><span data-stu-id="bad5f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="bad5f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bad5f-114">Update Privilege</span></span>  | <span data-ttu-id="bad5f-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="bad5f-115">Domain administrator</span></span>                        |
| <span data-ttu-id="bad5f-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bad5f-116">Update Frequency</span></span>  | <span data-ttu-id="bad5f-117">在系統設定時。</span><span class="sxs-lookup"><span data-stu-id="bad5f-117">At system setup.</span></span>                            |
| <span data-ttu-id="bad5f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bad5f-118">Attribute-Id</span></span>      | <span data-ttu-id="bad5f-119">1.2.840.113556.1.4.1389</span><span class="sxs-lookup"><span data-stu-id="bad5f-119">1.2.840.113556.1.4.1389</span></span>                     |
| <span data-ttu-id="bad5f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bad5f-120">System-Id-Guid</span></span>    | <span data-ttu-id="bad5f-121">c57f72f4-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="bad5f-121">c57f72f4-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="bad5f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="bad5f-122">Syntax</span></span>            | [<span data-ttu-id="bad5f-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bad5f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bad5f-124">實作</span><span class="sxs-lookup"><span data-stu-id="bad5f-124">Implementations</span></span>

-   [<span data-ttu-id="bad5f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bad5f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bad5f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bad5f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bad5f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bad5f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bad5f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bad5f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bad5f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bad5f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bad5f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bad5f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bad5f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bad5f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bad5f-132">進入</span><span class="sxs-lookup"><span data-stu-id="bad5f-132">Entry</span></span> | <span data-ttu-id="bad5f-133">值</span><span class="sxs-lookup"><span data-stu-id="bad5f-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bad5f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bad5f-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad5f-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad5f-136">System-Only</span></span>            | <span data-ttu-id="bad5f-137">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-137">False</span></span>                                                       |
| <span data-ttu-id="bad5f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bad5f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bad5f-139">對</span><span class="sxs-lookup"><span data-stu-id="bad5f-139">True</span></span>                                                        |
| <span data-ttu-id="bad5f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bad5f-140">Is Indexed</span></span>             | <span data-ttu-id="bad5f-141">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-141">False</span></span>                                                       |
| <span data-ttu-id="bad5f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bad5f-142">In Global Catalog</span></span>      | <span data-ttu-id="bad5f-143">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-143">False</span></span>                                                       |
| <span data-ttu-id="bad5f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bad5f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad5f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bad5f-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bad5f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad5f-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad5f-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-148">Search-Flags</span></span>           | <span data-ttu-id="bad5f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad5f-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="bad5f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-150">System-Flags</span></span>           | <span data-ttu-id="bad5f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad5f-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="bad5f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bad5f-152">Classes used in</span></span>        | [<span data-ttu-id="bad5f-153">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="bad5f-153">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bad5f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bad5f-154">Windows Server 2003</span></span>



| <span data-ttu-id="bad5f-155">進入</span><span class="sxs-lookup"><span data-stu-id="bad5f-155">Entry</span></span> | <span data-ttu-id="bad5f-156">值</span><span class="sxs-lookup"><span data-stu-id="bad5f-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bad5f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bad5f-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad5f-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad5f-159">System-Only</span></span>            | <span data-ttu-id="bad5f-160">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-160">False</span></span>                                                       |
| <span data-ttu-id="bad5f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bad5f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="bad5f-162">對</span><span class="sxs-lookup"><span data-stu-id="bad5f-162">True</span></span>                                                        |
| <span data-ttu-id="bad5f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bad5f-163">Is Indexed</span></span>             | <span data-ttu-id="bad5f-164">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-164">False</span></span>                                                       |
| <span data-ttu-id="bad5f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bad5f-165">In Global Catalog</span></span>      | <span data-ttu-id="bad5f-166">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-166">False</span></span>                                                       |
| <span data-ttu-id="bad5f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bad5f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad5f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bad5f-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bad5f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad5f-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad5f-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-171">Search-Flags</span></span>           | <span data-ttu-id="bad5f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad5f-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="bad5f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-173">System-Flags</span></span>           | <span data-ttu-id="bad5f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad5f-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="bad5f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bad5f-175">Classes used in</span></span>        | [<span data-ttu-id="bad5f-176">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="bad5f-176">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bad5f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bad5f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bad5f-178">進入</span><span class="sxs-lookup"><span data-stu-id="bad5f-178">Entry</span></span> | <span data-ttu-id="bad5f-179">值</span><span class="sxs-lookup"><span data-stu-id="bad5f-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bad5f-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bad5f-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad5f-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad5f-182">System-Only</span></span>            | <span data-ttu-id="bad5f-183">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-183">False</span></span>                                                       |
| <span data-ttu-id="bad5f-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bad5f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="bad5f-185">對</span><span class="sxs-lookup"><span data-stu-id="bad5f-185">True</span></span>                                                        |
| <span data-ttu-id="bad5f-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bad5f-186">Is Indexed</span></span>             | <span data-ttu-id="bad5f-187">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-187">False</span></span>                                                       |
| <span data-ttu-id="bad5f-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bad5f-188">In Global Catalog</span></span>      | <span data-ttu-id="bad5f-189">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-189">False</span></span>                                                       |
| <span data-ttu-id="bad5f-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bad5f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad5f-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bad5f-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bad5f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad5f-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad5f-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-194">Search-Flags</span></span>           | <span data-ttu-id="bad5f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad5f-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="bad5f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-196">System-Flags</span></span>           | <span data-ttu-id="bad5f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad5f-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="bad5f-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bad5f-198">Classes used in</span></span>        | [<span data-ttu-id="bad5f-199">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="bad5f-199">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bad5f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bad5f-200">Windows Server 2008</span></span>



| <span data-ttu-id="bad5f-201">進入</span><span class="sxs-lookup"><span data-stu-id="bad5f-201">Entry</span></span> | <span data-ttu-id="bad5f-202">值</span><span class="sxs-lookup"><span data-stu-id="bad5f-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bad5f-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bad5f-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad5f-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad5f-205">System-Only</span></span>            | <span data-ttu-id="bad5f-206">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-206">False</span></span>                                                       |
| <span data-ttu-id="bad5f-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bad5f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="bad5f-208">對</span><span class="sxs-lookup"><span data-stu-id="bad5f-208">True</span></span>                                                        |
| <span data-ttu-id="bad5f-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bad5f-209">Is Indexed</span></span>             | <span data-ttu-id="bad5f-210">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-210">False</span></span>                                                       |
| <span data-ttu-id="bad5f-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bad5f-211">In Global Catalog</span></span>      | <span data-ttu-id="bad5f-212">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-212">False</span></span>                                                       |
| <span data-ttu-id="bad5f-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bad5f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad5f-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bad5f-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bad5f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad5f-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad5f-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-217">Search-Flags</span></span>           | <span data-ttu-id="bad5f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad5f-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="bad5f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-219">System-Flags</span></span>           | <span data-ttu-id="bad5f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad5f-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="bad5f-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bad5f-221">Classes used in</span></span>        | [<span data-ttu-id="bad5f-222">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="bad5f-222">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bad5f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bad5f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bad5f-224">進入</span><span class="sxs-lookup"><span data-stu-id="bad5f-224">Entry</span></span> | <span data-ttu-id="bad5f-225">值</span><span class="sxs-lookup"><span data-stu-id="bad5f-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bad5f-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bad5f-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad5f-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad5f-228">System-Only</span></span>            | <span data-ttu-id="bad5f-229">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-229">False</span></span>                                                       |
| <span data-ttu-id="bad5f-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bad5f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="bad5f-231">對</span><span class="sxs-lookup"><span data-stu-id="bad5f-231">True</span></span>                                                        |
| <span data-ttu-id="bad5f-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bad5f-232">Is Indexed</span></span>             | <span data-ttu-id="bad5f-233">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-233">False</span></span>                                                       |
| <span data-ttu-id="bad5f-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bad5f-234">In Global Catalog</span></span>      | <span data-ttu-id="bad5f-235">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-235">False</span></span>                                                       |
| <span data-ttu-id="bad5f-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bad5f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad5f-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bad5f-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bad5f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad5f-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad5f-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-240">Search-Flags</span></span>           | <span data-ttu-id="bad5f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad5f-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="bad5f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-242">System-Flags</span></span>           | <span data-ttu-id="bad5f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad5f-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="bad5f-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bad5f-244">Classes used in</span></span>        | [<span data-ttu-id="bad5f-245">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="bad5f-245">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bad5f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bad5f-246">Windows Server 2012</span></span>



| <span data-ttu-id="bad5f-247">進入</span><span class="sxs-lookup"><span data-stu-id="bad5f-247">Entry</span></span> | <span data-ttu-id="bad5f-248">值</span><span class="sxs-lookup"><span data-stu-id="bad5f-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bad5f-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bad5f-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bad5f-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bad5f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="bad5f-251">System-Only</span></span>            | <span data-ttu-id="bad5f-252">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-252">False</span></span>                                                       |
| <span data-ttu-id="bad5f-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bad5f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="bad5f-254">對</span><span class="sxs-lookup"><span data-stu-id="bad5f-254">True</span></span>                                                        |
| <span data-ttu-id="bad5f-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bad5f-255">Is Indexed</span></span>             | <span data-ttu-id="bad5f-256">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-256">False</span></span>                                                       |
| <span data-ttu-id="bad5f-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bad5f-257">In Global Catalog</span></span>      | <span data-ttu-id="bad5f-258">否</span><span class="sxs-lookup"><span data-stu-id="bad5f-258">False</span></span>                                                       |
| <span data-ttu-id="bad5f-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bad5f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="bad5f-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bad5f-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bad5f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bad5f-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bad5f-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="bad5f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-263">Search-Flags</span></span>           | <span data-ttu-id="bad5f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bad5f-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="bad5f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bad5f-265">System-Flags</span></span>           | <span data-ttu-id="bad5f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bad5f-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="bad5f-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bad5f-267">Classes used in</span></span>        | [<span data-ttu-id="bad5f-268">**Olapserver.server**</span><span class="sxs-lookup"><span data-stu-id="bad5f-268">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





