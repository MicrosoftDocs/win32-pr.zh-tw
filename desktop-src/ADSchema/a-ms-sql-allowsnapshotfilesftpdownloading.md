---
title: AllowSnapshotFilesFTPDownloading 屬性
description: 如果發行集允許使用 FTP 下載快照集檔案，則為 True。
ms.assetid: 227e1438-db8d-4e8f-b2dd-ffc6ef50e0d1
ms.tgt_platform: multiple
keywords:
- AllowSnapshotFilesFTPDownloading 屬性 AD 架構
- AllowSnapshotFilesFTPDownloading 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-AllowSnapshotFilesFTPDownloading
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed32d824f4832294b3484da4e871303b31820878
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108208"
---
# <a name="ms-sql-allowsnapshotfilesftpdownloading-attribute"></a><span data-ttu-id="de2d4-105">AllowSnapshotFilesFTPDownloading 屬性</span><span class="sxs-lookup"><span data-stu-id="de2d4-105">MS-SQL-AllowSnapshotFilesFTPDownloading attribute</span></span>

<span data-ttu-id="de2d4-106">如果發行集允許使用 FTP 下載快照集檔案，則為 True。</span><span class="sxs-lookup"><span data-stu-id="de2d4-106">True if the publication allows snapshot files to be downloaded by using FTP.</span></span>



| <span data-ttu-id="de2d4-107">進入</span><span class="sxs-lookup"><span data-stu-id="de2d4-107">Entry</span></span> | <span data-ttu-id="de2d4-108">值</span><span class="sxs-lookup"><span data-stu-id="de2d4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="de2d4-109">CN</span><span class="sxs-lookup"><span data-stu-id="de2d4-109">CN</span></span>                | <span data-ttu-id="de2d4-110">AllowSnapshotFilesFTPDownloading</span><span class="sxs-lookup"><span data-stu-id="de2d4-110">MS-SQL-AllowSnapshotFilesFTPDownloading</span></span> |
| <span data-ttu-id="de2d4-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="de2d4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="de2d4-112">AllowSnapshotFilesFTPDownloading</span><span class="sxs-lookup"><span data-stu-id="de2d4-112">mS-SQL-AllowSnapshotFilesFTPDownloading</span></span> |
| <span data-ttu-id="de2d4-113">大小</span><span class="sxs-lookup"><span data-stu-id="de2d4-113">Size</span></span>              | <span data-ttu-id="de2d4-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="de2d4-114">4 bytes</span></span>                                 |
| <span data-ttu-id="de2d4-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="de2d4-115">Update Privilege</span></span>  | <span data-ttu-id="de2d4-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="de2d4-116">This value is set by the system.</span></span>        |
| <span data-ttu-id="de2d4-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="de2d4-117">Update Frequency</span></span>  | <span data-ttu-id="de2d4-118">當複寫設定時。</span><span class="sxs-lookup"><span data-stu-id="de2d4-118">When replication is setup.</span></span>              |
| <span data-ttu-id="de2d4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de2d4-119">Attribute-Id</span></span>      | <span data-ttu-id="de2d4-120">1.2.840.113556.1.4.1406</span><span class="sxs-lookup"><span data-stu-id="de2d4-120">1.2.840.113556.1.4.1406</span></span>                 |
| <span data-ttu-id="de2d4-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="de2d4-121">System-Id-Guid</span></span>    | <span data-ttu-id="de2d4-122">c49b8be8-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="de2d4-122">c49b8be8-d34b-11d2-999a-0000f87a57d4</span></span>    |
| <span data-ttu-id="de2d4-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="de2d4-123">Syntax</span></span>            | [<span data-ttu-id="de2d4-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="de2d4-124">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="de2d4-125">實作</span><span class="sxs-lookup"><span data-stu-id="de2d4-125">Implementations</span></span>

-   [<span data-ttu-id="de2d4-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="de2d4-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="de2d4-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="de2d4-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="de2d4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="de2d4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="de2d4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de2d4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de2d4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de2d4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de2d4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de2d4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="de2d4-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de2d4-132">Windows 2000 Server</span></span>



| <span data-ttu-id="de2d4-133">進入</span><span class="sxs-lookup"><span data-stu-id="de2d4-133">Entry</span></span> | <span data-ttu-id="de2d4-134">值</span><span class="sxs-lookup"><span data-stu-id="de2d4-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="de2d4-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de2d4-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de2d4-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="de2d4-137">System-Only</span></span>            | <span data-ttu-id="de2d4-138">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-138">False</span></span>                                                               |
| <span data-ttu-id="de2d4-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de2d4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="de2d4-140">對</span><span class="sxs-lookup"><span data-stu-id="de2d4-140">True</span></span>                                                                |
| <span data-ttu-id="de2d4-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de2d4-141">Is Indexed</span></span>             | <span data-ttu-id="de2d4-142">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-142">False</span></span>                                                               |
| <span data-ttu-id="de2d4-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de2d4-143">In Global Catalog</span></span>      | <span data-ttu-id="de2d4-144">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-144">False</span></span>                                                               |
| <span data-ttu-id="de2d4-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de2d4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="de2d4-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de2d4-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="de2d4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de2d4-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de2d4-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-149">Search-Flags</span></span>           | <span data-ttu-id="de2d4-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de2d4-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="de2d4-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-151">System-Flags</span></span>           | <span data-ttu-id="de2d4-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de2d4-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="de2d4-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de2d4-153">Classes used in</span></span>        | [<span data-ttu-id="de2d4-154">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="de2d4-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="de2d4-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de2d4-155">Windows Server 2003</span></span>



| <span data-ttu-id="de2d4-156">進入</span><span class="sxs-lookup"><span data-stu-id="de2d4-156">Entry</span></span> | <span data-ttu-id="de2d4-157">值</span><span class="sxs-lookup"><span data-stu-id="de2d4-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="de2d4-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de2d4-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de2d4-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="de2d4-160">System-Only</span></span>            | <span data-ttu-id="de2d4-161">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-161">False</span></span>                                                               |
| <span data-ttu-id="de2d4-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de2d4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="de2d4-163">對</span><span class="sxs-lookup"><span data-stu-id="de2d4-163">True</span></span>                                                                |
| <span data-ttu-id="de2d4-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de2d4-164">Is Indexed</span></span>             | <span data-ttu-id="de2d4-165">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-165">False</span></span>                                                               |
| <span data-ttu-id="de2d4-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de2d4-166">In Global Catalog</span></span>      | <span data-ttu-id="de2d4-167">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-167">False</span></span>                                                               |
| <span data-ttu-id="de2d4-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de2d4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="de2d4-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de2d4-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="de2d4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de2d4-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de2d4-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-172">Search-Flags</span></span>           | <span data-ttu-id="de2d4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de2d4-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="de2d4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-174">System-Flags</span></span>           | <span data-ttu-id="de2d4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de2d4-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="de2d4-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de2d4-176">Classes used in</span></span>        | [<span data-ttu-id="de2d4-177">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="de2d4-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="de2d4-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="de2d4-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="de2d4-179">進入</span><span class="sxs-lookup"><span data-stu-id="de2d4-179">Entry</span></span> | <span data-ttu-id="de2d4-180">值</span><span class="sxs-lookup"><span data-stu-id="de2d4-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="de2d4-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de2d4-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de2d4-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="de2d4-183">System-Only</span></span>            | <span data-ttu-id="de2d4-184">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-184">False</span></span>                                                               |
| <span data-ttu-id="de2d4-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de2d4-185">Is-Single-Valued</span></span>       | <span data-ttu-id="de2d4-186">對</span><span class="sxs-lookup"><span data-stu-id="de2d4-186">True</span></span>                                                                |
| <span data-ttu-id="de2d4-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de2d4-187">Is Indexed</span></span>             | <span data-ttu-id="de2d4-188">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-188">False</span></span>                                                               |
| <span data-ttu-id="de2d4-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de2d4-189">In Global Catalog</span></span>      | <span data-ttu-id="de2d4-190">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-190">False</span></span>                                                               |
| <span data-ttu-id="de2d4-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de2d4-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="de2d4-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de2d4-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="de2d4-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de2d4-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de2d4-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-195">Search-Flags</span></span>           | <span data-ttu-id="de2d4-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de2d4-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="de2d4-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-197">System-Flags</span></span>           | <span data-ttu-id="de2d4-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de2d4-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="de2d4-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de2d4-199">Classes used in</span></span>        | [<span data-ttu-id="de2d4-200">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="de2d4-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="de2d4-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de2d4-201">Windows Server 2008</span></span>



| <span data-ttu-id="de2d4-202">進入</span><span class="sxs-lookup"><span data-stu-id="de2d4-202">Entry</span></span> | <span data-ttu-id="de2d4-203">值</span><span class="sxs-lookup"><span data-stu-id="de2d4-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="de2d4-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de2d4-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de2d4-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="de2d4-206">System-Only</span></span>            | <span data-ttu-id="de2d4-207">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-207">False</span></span>                                                               |
| <span data-ttu-id="de2d4-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de2d4-208">Is-Single-Valued</span></span>       | <span data-ttu-id="de2d4-209">對</span><span class="sxs-lookup"><span data-stu-id="de2d4-209">True</span></span>                                                                |
| <span data-ttu-id="de2d4-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de2d4-210">Is Indexed</span></span>             | <span data-ttu-id="de2d4-211">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-211">False</span></span>                                                               |
| <span data-ttu-id="de2d4-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de2d4-212">In Global Catalog</span></span>      | <span data-ttu-id="de2d4-213">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-213">False</span></span>                                                               |
| <span data-ttu-id="de2d4-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de2d4-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="de2d4-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de2d4-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="de2d4-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de2d4-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de2d4-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-218">Search-Flags</span></span>           | <span data-ttu-id="de2d4-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de2d4-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="de2d4-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-220">System-Flags</span></span>           | <span data-ttu-id="de2d4-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de2d4-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="de2d4-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de2d4-222">Classes used in</span></span>        | [<span data-ttu-id="de2d4-223">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="de2d4-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de2d4-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de2d4-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de2d4-225">進入</span><span class="sxs-lookup"><span data-stu-id="de2d4-225">Entry</span></span> | <span data-ttu-id="de2d4-226">值</span><span class="sxs-lookup"><span data-stu-id="de2d4-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="de2d4-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de2d4-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de2d4-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="de2d4-229">System-Only</span></span>            | <span data-ttu-id="de2d4-230">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-230">False</span></span>                                                               |
| <span data-ttu-id="de2d4-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de2d4-231">Is-Single-Valued</span></span>       | <span data-ttu-id="de2d4-232">對</span><span class="sxs-lookup"><span data-stu-id="de2d4-232">True</span></span>                                                                |
| <span data-ttu-id="de2d4-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de2d4-233">Is Indexed</span></span>             | <span data-ttu-id="de2d4-234">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-234">False</span></span>                                                               |
| <span data-ttu-id="de2d4-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de2d4-235">In Global Catalog</span></span>      | <span data-ttu-id="de2d4-236">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-236">False</span></span>                                                               |
| <span data-ttu-id="de2d4-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de2d4-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="de2d4-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de2d4-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="de2d4-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de2d4-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de2d4-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-241">Search-Flags</span></span>           | <span data-ttu-id="de2d4-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de2d4-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="de2d4-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-243">System-Flags</span></span>           | <span data-ttu-id="de2d4-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de2d4-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="de2d4-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de2d4-245">Classes used in</span></span>        | [<span data-ttu-id="de2d4-246">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="de2d4-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de2d4-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de2d4-247">Windows Server 2012</span></span>



| <span data-ttu-id="de2d4-248">進入</span><span class="sxs-lookup"><span data-stu-id="de2d4-248">Entry</span></span> | <span data-ttu-id="de2d4-249">值</span><span class="sxs-lookup"><span data-stu-id="de2d4-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="de2d4-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="de2d4-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de2d4-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="de2d4-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="de2d4-252">System-Only</span></span>            | <span data-ttu-id="de2d4-253">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-253">False</span></span>                                                               |
| <span data-ttu-id="de2d4-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="de2d4-254">Is-Single-Valued</span></span>       | <span data-ttu-id="de2d4-255">對</span><span class="sxs-lookup"><span data-stu-id="de2d4-255">True</span></span>                                                                |
| <span data-ttu-id="de2d4-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="de2d4-256">Is Indexed</span></span>             | <span data-ttu-id="de2d4-257">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-257">False</span></span>                                                               |
| <span data-ttu-id="de2d4-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="de2d4-258">In Global Catalog</span></span>      | <span data-ttu-id="de2d4-259">否</span><span class="sxs-lookup"><span data-stu-id="de2d4-259">False</span></span>                                                               |
| <span data-ttu-id="de2d4-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="de2d4-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="de2d4-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="de2d4-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="de2d4-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de2d4-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de2d4-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="de2d4-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-264">Search-Flags</span></span>           | <span data-ttu-id="de2d4-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de2d4-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="de2d4-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de2d4-266">System-Flags</span></span>           | <span data-ttu-id="de2d4-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de2d4-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="de2d4-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="de2d4-268">Classes used in</span></span>        | [<span data-ttu-id="de2d4-269">**SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="de2d4-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





