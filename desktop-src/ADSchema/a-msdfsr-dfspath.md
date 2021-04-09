---
title: ms-chap-DfsPath 屬性
description: 包含相關分散式檔案系統 (DFS) 連結的完整路徑。
ms.assetid: bd596110-b156-4640-a6d0-ace9e4e30909
ms.tgt_platform: multiple
keywords:
- ms-DFSR-DfsPath 屬性 AD 架構
- msDFSR-DfsPath 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DFSR-DfsPath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718c052ea89df9d8c237c4ef73a6d6d6af13ee49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108176"
---
# <a name="ms-dfsr-dfspath-attribute"></a><span data-ttu-id="be3c5-105">ms-chap-DfsPath 屬性</span><span class="sxs-lookup"><span data-stu-id="be3c5-105">ms-DFSR-DfsPath attribute</span></span>

<span data-ttu-id="be3c5-106">包含 DFS 複寫服務支援之相關聯分散式檔案系統 (DFS) 連結的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="be3c5-106">Contains the full path of the associated Distributed File System (DFS) link for DFS Replication service support.</span></span>



| <span data-ttu-id="be3c5-107">進入</span><span class="sxs-lookup"><span data-stu-id="be3c5-107">Entry</span></span> | <span data-ttu-id="be3c5-108">值</span><span class="sxs-lookup"><span data-stu-id="be3c5-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="be3c5-109">CN</span><span class="sxs-lookup"><span data-stu-id="be3c5-109">CN</span></span>                | <span data-ttu-id="be3c5-110">ms-DFSR-DfsPath</span><span class="sxs-lookup"><span data-stu-id="be3c5-110">ms-DFSR-DfsPath</span></span>                             |
| <span data-ttu-id="be3c5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="be3c5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="be3c5-112">msDFSR-DfsPath</span><span class="sxs-lookup"><span data-stu-id="be3c5-112">msDFSR-DfsPath</span></span>                              |
| <span data-ttu-id="be3c5-113">大小</span><span class="sxs-lookup"><span data-stu-id="be3c5-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="be3c5-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="be3c5-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="be3c5-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="be3c5-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="be3c5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be3c5-116">Attribute-Id</span></span>      | <span data-ttu-id="be3c5-117">1.2.840.113556.1.6.13.3.21</span><span class="sxs-lookup"><span data-stu-id="be3c5-117">1.2.840.113556.1.6.13.3.21</span></span>                  |
| <span data-ttu-id="be3c5-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="be3c5-118">System-Id-Guid</span></span>    | <span data-ttu-id="be3c5-119">2cc903e2-398c-443b-ac86-ff6b01eac7ba</span><span class="sxs-lookup"><span data-stu-id="be3c5-119">2cc903e2-398c-443b-ac86-ff6b01eac7ba</span></span>        |
| <span data-ttu-id="be3c5-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="be3c5-120">Syntax</span></span>            | [<span data-ttu-id="be3c5-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="be3c5-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="be3c5-122">實作</span><span class="sxs-lookup"><span data-stu-id="be3c5-122">Implementations</span></span>

-   [<span data-ttu-id="be3c5-123">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be3c5-123">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be3c5-124">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be3c5-124">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be3c5-125">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be3c5-125">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be3c5-126">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be3c5-126">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="be3c5-127">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be3c5-127">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be3c5-128">進入</span><span class="sxs-lookup"><span data-stu-id="be3c5-128">Entry</span></span> | <span data-ttu-id="be3c5-129">值</span><span class="sxs-lookup"><span data-stu-id="be3c5-129">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="be3c5-130">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be3c5-130">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be3c5-131">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="be3c5-132">System-Only</span></span>            | <span data-ttu-id="be3c5-133">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-133">False</span></span>                                                        |
| <span data-ttu-id="be3c5-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be3c5-134">Is-Single-Valued</span></span>       | <span data-ttu-id="be3c5-135">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-135">True</span></span>                                                         |
| <span data-ttu-id="be3c5-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be3c5-136">Is Indexed</span></span>             | <span data-ttu-id="be3c5-137">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-137">True</span></span>                                                         |
| <span data-ttu-id="be3c5-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be3c5-138">In Global Catalog</span></span>      | <span data-ttu-id="be3c5-139">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-139">False</span></span>                                                        |
| <span data-ttu-id="be3c5-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be3c5-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="be3c5-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be3c5-141">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="be3c5-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be3c5-142">Range-Lower</span></span>            | <span data-ttu-id="be3c5-143">0</span><span class="sxs-lookup"><span data-stu-id="be3c5-143">0</span></span>                                                            |
| <span data-ttu-id="be3c5-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be3c5-144">Range-Upper</span></span>            | <span data-ttu-id="be3c5-145">32767</span><span class="sxs-lookup"><span data-stu-id="be3c5-145">32767</span></span>                                                        |
| <span data-ttu-id="be3c5-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-146">Search-Flags</span></span>           | <span data-ttu-id="be3c5-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be3c5-147">0x00000001</span></span>                                                   |
| <span data-ttu-id="be3c5-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-148">System-Flags</span></span>           | <span data-ttu-id="be3c5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be3c5-149">0x00000000</span></span>                                                   |
| <span data-ttu-id="be3c5-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be3c5-150">Classes used in</span></span>        | [<span data-ttu-id="be3c5-151">**ms-DFSR-ContentSet**</span><span class="sxs-lookup"><span data-stu-id="be3c5-151">**ms-DFSR-ContentSet**</span></span>](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be3c5-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be3c5-152">Windows Server 2008</span></span>



| <span data-ttu-id="be3c5-153">進入</span><span class="sxs-lookup"><span data-stu-id="be3c5-153">Entry</span></span> | <span data-ttu-id="be3c5-154">值</span><span class="sxs-lookup"><span data-stu-id="be3c5-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="be3c5-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be3c5-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be3c5-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="be3c5-157">System-Only</span></span>            | <span data-ttu-id="be3c5-158">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-158">False</span></span>                                                        |
| <span data-ttu-id="be3c5-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be3c5-159">Is-Single-Valued</span></span>       | <span data-ttu-id="be3c5-160">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-160">True</span></span>                                                         |
| <span data-ttu-id="be3c5-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be3c5-161">Is Indexed</span></span>             | <span data-ttu-id="be3c5-162">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-162">True</span></span>                                                         |
| <span data-ttu-id="be3c5-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be3c5-163">In Global Catalog</span></span>      | <span data-ttu-id="be3c5-164">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-164">False</span></span>                                                        |
| <span data-ttu-id="be3c5-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be3c5-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="be3c5-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be3c5-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="be3c5-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be3c5-167">Range-Lower</span></span>            | <span data-ttu-id="be3c5-168">0</span><span class="sxs-lookup"><span data-stu-id="be3c5-168">0</span></span>                                                            |
| <span data-ttu-id="be3c5-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be3c5-169">Range-Upper</span></span>            | <span data-ttu-id="be3c5-170">32767</span><span class="sxs-lookup"><span data-stu-id="be3c5-170">32767</span></span>                                                        |
| <span data-ttu-id="be3c5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-171">Search-Flags</span></span>           | <span data-ttu-id="be3c5-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be3c5-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="be3c5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-173">System-Flags</span></span>           | <span data-ttu-id="be3c5-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be3c5-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="be3c5-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be3c5-175">Classes used in</span></span>        | [<span data-ttu-id="be3c5-176">**ms-DFSR-ContentSet**</span><span class="sxs-lookup"><span data-stu-id="be3c5-176">**ms-DFSR-ContentSet**</span></span>](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be3c5-177">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be3c5-177">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be3c5-178">進入</span><span class="sxs-lookup"><span data-stu-id="be3c5-178">Entry</span></span> | <span data-ttu-id="be3c5-179">值</span><span class="sxs-lookup"><span data-stu-id="be3c5-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="be3c5-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be3c5-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be3c5-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="be3c5-182">System-Only</span></span>            | <span data-ttu-id="be3c5-183">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-183">False</span></span>                                                        |
| <span data-ttu-id="be3c5-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be3c5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="be3c5-185">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-185">True</span></span>                                                         |
| <span data-ttu-id="be3c5-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be3c5-186">Is Indexed</span></span>             | <span data-ttu-id="be3c5-187">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-187">True</span></span>                                                         |
| <span data-ttu-id="be3c5-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be3c5-188">In Global Catalog</span></span>      | <span data-ttu-id="be3c5-189">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-189">False</span></span>                                                        |
| <span data-ttu-id="be3c5-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be3c5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="be3c5-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be3c5-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="be3c5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be3c5-192">Range-Lower</span></span>            | <span data-ttu-id="be3c5-193">0</span><span class="sxs-lookup"><span data-stu-id="be3c5-193">0</span></span>                                                            |
| <span data-ttu-id="be3c5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be3c5-194">Range-Upper</span></span>            | <span data-ttu-id="be3c5-195">32767</span><span class="sxs-lookup"><span data-stu-id="be3c5-195">32767</span></span>                                                        |
| <span data-ttu-id="be3c5-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-196">Search-Flags</span></span>           | <span data-ttu-id="be3c5-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be3c5-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="be3c5-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-198">System-Flags</span></span>           | <span data-ttu-id="be3c5-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be3c5-199">0x00000000</span></span>                                                   |
| <span data-ttu-id="be3c5-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be3c5-200">Classes used in</span></span>        | [<span data-ttu-id="be3c5-201">**ms-DFSR-ContentSet**</span><span class="sxs-lookup"><span data-stu-id="be3c5-201">**ms-DFSR-ContentSet**</span></span>](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be3c5-202">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be3c5-202">Windows Server 2012</span></span>



| <span data-ttu-id="be3c5-203">進入</span><span class="sxs-lookup"><span data-stu-id="be3c5-203">Entry</span></span> | <span data-ttu-id="be3c5-204">值</span><span class="sxs-lookup"><span data-stu-id="be3c5-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="be3c5-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be3c5-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be3c5-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="be3c5-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="be3c5-207">System-Only</span></span>            | <span data-ttu-id="be3c5-208">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-208">False</span></span>                                                        |
| <span data-ttu-id="be3c5-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be3c5-209">Is-Single-Valued</span></span>       | <span data-ttu-id="be3c5-210">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-210">True</span></span>                                                         |
| <span data-ttu-id="be3c5-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be3c5-211">Is Indexed</span></span>             | <span data-ttu-id="be3c5-212">對</span><span class="sxs-lookup"><span data-stu-id="be3c5-212">True</span></span>                                                         |
| <span data-ttu-id="be3c5-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be3c5-213">In Global Catalog</span></span>      | <span data-ttu-id="be3c5-214">否</span><span class="sxs-lookup"><span data-stu-id="be3c5-214">False</span></span>                                                        |
| <span data-ttu-id="be3c5-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be3c5-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="be3c5-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be3c5-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="be3c5-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be3c5-217">Range-Lower</span></span>            | <span data-ttu-id="be3c5-218">0</span><span class="sxs-lookup"><span data-stu-id="be3c5-218">0</span></span>                                                            |
| <span data-ttu-id="be3c5-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be3c5-219">Range-Upper</span></span>            | <span data-ttu-id="be3c5-220">32767</span><span class="sxs-lookup"><span data-stu-id="be3c5-220">32767</span></span>                                                        |
| <span data-ttu-id="be3c5-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-221">Search-Flags</span></span>           | <span data-ttu-id="be3c5-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="be3c5-222">0x00000001</span></span>                                                   |
| <span data-ttu-id="be3c5-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be3c5-223">System-Flags</span></span>           | <span data-ttu-id="be3c5-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be3c5-224">0x00000000</span></span>                                                   |
| <span data-ttu-id="be3c5-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be3c5-225">Classes used in</span></span>        | [<span data-ttu-id="be3c5-226">**ms-DFSR-ContentSet**</span><span class="sxs-lookup"><span data-stu-id="be3c5-226">**ms-DFSR-ContentSet**</span></span>](c-msdfsr-contentset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="be3c5-227">備註</span><span class="sxs-lookup"><span data-stu-id="be3c5-227">Remarks</span></span>

<span data-ttu-id="be3c5-228">**DfsPath** 屬性屬於分散式檔案系統 (DFS) Replication service 支援的一部分。</span><span class="sxs-lookup"><span data-stu-id="be3c5-228">The **ms-DFSR-DfsPath** attribute is a part of the Distributed File System (DFS) Replication service support.</span></span>

 

 





