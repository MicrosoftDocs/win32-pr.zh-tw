---
title: rpc-Ns-Entry 旗標屬性
description: 表示已明確建立 RPC NS 專案的旗標。
ms.assetid: a8339920-778a-4539-b65d-c575eb047d18
ms.tgt_platform: multiple
keywords:
- rpc-Ns-Entry-Flags 屬性 AD 架構
- rpcNsEntryFlags 屬性 AD 架構
topic_type:
- apiref
api_name:
- rpc-Ns-Entry-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5cfd4f6879126337c18c8af300db91d3b774f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107561"
---
# <a name="rpc-ns-entry-flags-attribute"></a><span data-ttu-id="fa1e1-105">rpc-Ns-Entry 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="fa1e1-105">rpc-Ns-Entry-Flags attribute</span></span>

<span data-ttu-id="fa1e1-106">表示已明確建立 RPC NS 專案的旗標。</span><span class="sxs-lookup"><span data-stu-id="fa1e1-106">Flag to indicate that the RPC NS entry was explicitly created.</span></span>



| <span data-ttu-id="fa1e1-107">進入</span><span class="sxs-lookup"><span data-stu-id="fa1e1-107">Entry</span></span> | <span data-ttu-id="fa1e1-108">值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fa1e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="fa1e1-109">CN</span></span>                | <span data-ttu-id="fa1e1-110">rpc-Ns-Entry-旗標</span><span class="sxs-lookup"><span data-stu-id="fa1e1-110">rpc-Ns-Entry-Flags</span></span>                   |
| <span data-ttu-id="fa1e1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fa1e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fa1e1-112">rpcNsEntryFlags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-112">rpcNsEntryFlags</span></span>                      |
| <span data-ttu-id="fa1e1-113">大小</span><span class="sxs-lookup"><span data-stu-id="fa1e1-113">Size</span></span>              | <span data-ttu-id="fa1e1-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="fa1e1-114">4 bytes</span></span>                              |
| <span data-ttu-id="fa1e1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fa1e1-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fa1e1-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fa1e1-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fa1e1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fa1e1-117">Attribute-Id</span></span>      | <span data-ttu-id="fa1e1-118">1.2.840.113556.1.4.754</span><span class="sxs-lookup"><span data-stu-id="fa1e1-118">1.2.840.113556.1.4.754</span></span>               |
| <span data-ttu-id="fa1e1-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fa1e1-119">System-Id-Guid</span></span>    | <span data-ttu-id="fa1e1-120">80212841-4bdc-11d1-a9c4-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fa1e1-120">80212841-4bdc-11d1-a9c4-0000f80367c1</span></span> |
| <span data-ttu-id="fa1e1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa1e1-121">Syntax</span></span>            | [<span data-ttu-id="fa1e1-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="fa1e1-123">實作</span><span class="sxs-lookup"><span data-stu-id="fa1e1-123">Implementations</span></span>

-   [<span data-ttu-id="fa1e1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fa1e1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fa1e1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fa1e1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fa1e1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fa1e1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fa1e1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fa1e1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fa1e1-131">進入</span><span class="sxs-lookup"><span data-stu-id="fa1e1-131">Entry</span></span> | <span data-ttu-id="fa1e1-132">值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fa1e1-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa1e1-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa1e1-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa1e1-135">System-Only</span></span>            | <span data-ttu-id="fa1e1-136">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-136">False</span></span>                                        |
| <span data-ttu-id="fa1e1-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fa1e1-138">對</span><span class="sxs-lookup"><span data-stu-id="fa1e1-138">True</span></span>                                         |
| <span data-ttu-id="fa1e1-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa1e1-139">Is Indexed</span></span>             | <span data-ttu-id="fa1e1-140">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-140">False</span></span>                                        |
| <span data-ttu-id="fa1e1-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa1e1-141">In Global Catalog</span></span>      | <span data-ttu-id="fa1e1-142">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-142">False</span></span>                                        |
| <span data-ttu-id="fa1e1-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa1e1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa1e1-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa1e1-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fa1e1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa1e1-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa1e1-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-147">Search-Flags</span></span>           | <span data-ttu-id="fa1e1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa1e1-148">0x00000000</span></span>                                   |
| <span data-ttu-id="fa1e1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-149">System-Flags</span></span>           | <span data-ttu-id="fa1e1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa1e1-150">0x00000010</span></span>                                   |
| <span data-ttu-id="fa1e1-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa1e1-151">Classes used in</span></span>        | [<span data-ttu-id="fa1e1-152">**rpc-伺服器**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-152">**rpc-Server**</span></span>](c-rpcserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fa1e1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa1e1-153">Windows Server 2003</span></span>



| <span data-ttu-id="fa1e1-154">進入</span><span class="sxs-lookup"><span data-stu-id="fa1e1-154">Entry</span></span> | <span data-ttu-id="fa1e1-155">值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fa1e1-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa1e1-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa1e1-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa1e1-158">System-Only</span></span>            | <span data-ttu-id="fa1e1-159">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-159">False</span></span>                                        |
| <span data-ttu-id="fa1e1-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fa1e1-161">對</span><span class="sxs-lookup"><span data-stu-id="fa1e1-161">True</span></span>                                         |
| <span data-ttu-id="fa1e1-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa1e1-162">Is Indexed</span></span>             | <span data-ttu-id="fa1e1-163">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-163">False</span></span>                                        |
| <span data-ttu-id="fa1e1-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa1e1-164">In Global Catalog</span></span>      | <span data-ttu-id="fa1e1-165">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-165">False</span></span>                                        |
| <span data-ttu-id="fa1e1-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa1e1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa1e1-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa1e1-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fa1e1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa1e1-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa1e1-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-170">Search-Flags</span></span>           | <span data-ttu-id="fa1e1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa1e1-171">0x00000000</span></span>                                   |
| <span data-ttu-id="fa1e1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-172">System-Flags</span></span>           | <span data-ttu-id="fa1e1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa1e1-173">0x00000010</span></span>                                   |
| <span data-ttu-id="fa1e1-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa1e1-174">Classes used in</span></span>        | [<span data-ttu-id="fa1e1-175">**rpc-伺服器**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-175">**rpc-Server**</span></span>](c-rpcserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fa1e1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fa1e1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fa1e1-177">進入</span><span class="sxs-lookup"><span data-stu-id="fa1e1-177">Entry</span></span> | <span data-ttu-id="fa1e1-178">值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fa1e1-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa1e1-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa1e1-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa1e1-181">System-Only</span></span>            | <span data-ttu-id="fa1e1-182">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-182">False</span></span>                                        |
| <span data-ttu-id="fa1e1-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="fa1e1-184">對</span><span class="sxs-lookup"><span data-stu-id="fa1e1-184">True</span></span>                                         |
| <span data-ttu-id="fa1e1-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa1e1-185">Is Indexed</span></span>             | <span data-ttu-id="fa1e1-186">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-186">False</span></span>                                        |
| <span data-ttu-id="fa1e1-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa1e1-187">In Global Catalog</span></span>      | <span data-ttu-id="fa1e1-188">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-188">False</span></span>                                        |
| <span data-ttu-id="fa1e1-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa1e1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa1e1-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa1e1-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fa1e1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa1e1-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa1e1-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-193">Search-Flags</span></span>           | <span data-ttu-id="fa1e1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa1e1-194">0x00000000</span></span>                                   |
| <span data-ttu-id="fa1e1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-195">System-Flags</span></span>           | <span data-ttu-id="fa1e1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa1e1-196">0x00000010</span></span>                                   |
| <span data-ttu-id="fa1e1-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa1e1-197">Classes used in</span></span>        | [<span data-ttu-id="fa1e1-198">**rpc-伺服器**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-198">**rpc-Server**</span></span>](c-rpcserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fa1e1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa1e1-199">Windows Server 2008</span></span>



| <span data-ttu-id="fa1e1-200">進入</span><span class="sxs-lookup"><span data-stu-id="fa1e1-200">Entry</span></span> | <span data-ttu-id="fa1e1-201">值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fa1e1-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa1e1-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa1e1-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa1e1-204">System-Only</span></span>            | <span data-ttu-id="fa1e1-205">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-205">False</span></span>                                        |
| <span data-ttu-id="fa1e1-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="fa1e1-207">對</span><span class="sxs-lookup"><span data-stu-id="fa1e1-207">True</span></span>                                         |
| <span data-ttu-id="fa1e1-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa1e1-208">Is Indexed</span></span>             | <span data-ttu-id="fa1e1-209">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-209">False</span></span>                                        |
| <span data-ttu-id="fa1e1-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa1e1-210">In Global Catalog</span></span>      | <span data-ttu-id="fa1e1-211">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-211">False</span></span>                                        |
| <span data-ttu-id="fa1e1-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa1e1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa1e1-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa1e1-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fa1e1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa1e1-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa1e1-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-216">Search-Flags</span></span>           | <span data-ttu-id="fa1e1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa1e1-217">0x00000000</span></span>                                   |
| <span data-ttu-id="fa1e1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-218">System-Flags</span></span>           | <span data-ttu-id="fa1e1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa1e1-219">0x00000010</span></span>                                   |
| <span data-ttu-id="fa1e1-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa1e1-220">Classes used in</span></span>        | [<span data-ttu-id="fa1e1-221">**rpc-伺服器**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-221">**rpc-Server**</span></span>](c-rpcserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fa1e1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa1e1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fa1e1-223">進入</span><span class="sxs-lookup"><span data-stu-id="fa1e1-223">Entry</span></span> | <span data-ttu-id="fa1e1-224">值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fa1e1-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa1e1-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa1e1-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa1e1-227">System-Only</span></span>            | <span data-ttu-id="fa1e1-228">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-228">False</span></span>                                        |
| <span data-ttu-id="fa1e1-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="fa1e1-230">對</span><span class="sxs-lookup"><span data-stu-id="fa1e1-230">True</span></span>                                         |
| <span data-ttu-id="fa1e1-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa1e1-231">Is Indexed</span></span>             | <span data-ttu-id="fa1e1-232">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-232">False</span></span>                                        |
| <span data-ttu-id="fa1e1-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa1e1-233">In Global Catalog</span></span>      | <span data-ttu-id="fa1e1-234">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-234">False</span></span>                                        |
| <span data-ttu-id="fa1e1-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa1e1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa1e1-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa1e1-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fa1e1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa1e1-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa1e1-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-239">Search-Flags</span></span>           | <span data-ttu-id="fa1e1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa1e1-240">0x00000000</span></span>                                   |
| <span data-ttu-id="fa1e1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-241">System-Flags</span></span>           | <span data-ttu-id="fa1e1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa1e1-242">0x00000010</span></span>                                   |
| <span data-ttu-id="fa1e1-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa1e1-243">Classes used in</span></span>        | [<span data-ttu-id="fa1e1-244">**rpc-伺服器**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-244">**rpc-Server**</span></span>](c-rpcserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fa1e1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa1e1-245">Windows Server 2012</span></span>



| <span data-ttu-id="fa1e1-246">進入</span><span class="sxs-lookup"><span data-stu-id="fa1e1-246">Entry</span></span> | <span data-ttu-id="fa1e1-247">值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fa1e1-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fa1e1-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fa1e1-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fa1e1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="fa1e1-250">System-Only</span></span>            | <span data-ttu-id="fa1e1-251">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-251">False</span></span>                                        |
| <span data-ttu-id="fa1e1-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fa1e1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="fa1e1-253">對</span><span class="sxs-lookup"><span data-stu-id="fa1e1-253">True</span></span>                                         |
| <span data-ttu-id="fa1e1-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fa1e1-254">Is Indexed</span></span>             | <span data-ttu-id="fa1e1-255">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-255">False</span></span>                                        |
| <span data-ttu-id="fa1e1-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fa1e1-256">In Global Catalog</span></span>      | <span data-ttu-id="fa1e1-257">否</span><span class="sxs-lookup"><span data-stu-id="fa1e1-257">False</span></span>                                        |
| <span data-ttu-id="fa1e1-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fa1e1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="fa1e1-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fa1e1-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fa1e1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fa1e1-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fa1e1-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fa1e1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-262">Search-Flags</span></span>           | <span data-ttu-id="fa1e1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fa1e1-263">0x00000000</span></span>                                   |
| <span data-ttu-id="fa1e1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fa1e1-264">System-Flags</span></span>           | <span data-ttu-id="fa1e1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fa1e1-265">0x00000010</span></span>                                   |
| <span data-ttu-id="fa1e1-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fa1e1-266">Classes used in</span></span>        | [<span data-ttu-id="fa1e1-267">**rpc-伺服器**</span><span class="sxs-lookup"><span data-stu-id="fa1e1-267">**rpc-Server**</span></span>](c-rpcserver.md)<br/> |



 

 





