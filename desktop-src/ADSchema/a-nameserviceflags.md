---
title: 名稱-服務-旗標屬性
description: RPC 名稱服務的設定旗標。
ms.assetid: f32cd2fb-4a0a-4a1b-873b-3e4d893f80cd
ms.tgt_platform: multiple
keywords:
- 名稱-服務-旗標屬性 AD 架構
- nameServiceFlags 屬性 AD 架構
topic_type:
- apiref
api_name:
- Name-Service-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e0b8bec096a8dce43df7bb71658c90bbfd98a4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935372"
---
# <a name="name-service-flags-attribute"></a><span data-ttu-id="e2d5c-105">名稱-服務-旗標屬性</span><span class="sxs-lookup"><span data-stu-id="e2d5c-105">Name-Service-Flags attribute</span></span>

<span data-ttu-id="e2d5c-106">RPC 名稱服務的設定旗標。</span><span class="sxs-lookup"><span data-stu-id="e2d5c-106">Configuration flags for RPC Name Service.</span></span>



| <span data-ttu-id="e2d5c-107">進入</span><span class="sxs-lookup"><span data-stu-id="e2d5c-107">Entry</span></span> | <span data-ttu-id="e2d5c-108">值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e2d5c-109">CN</span><span class="sxs-lookup"><span data-stu-id="e2d5c-109">CN</span></span>                | <span data-ttu-id="e2d5c-110">名稱-服務-旗標</span><span class="sxs-lookup"><span data-stu-id="e2d5c-110">Name-Service-Flags</span></span>                   |
| <span data-ttu-id="e2d5c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e2d5c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e2d5c-112">nameServiceFlags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-112">nameServiceFlags</span></span>                     |
| <span data-ttu-id="e2d5c-113">大小</span><span class="sxs-lookup"><span data-stu-id="e2d5c-113">Size</span></span>              | <span data-ttu-id="e2d5c-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="e2d5c-114">4 bytes</span></span>                              |
| <span data-ttu-id="e2d5c-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e2d5c-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e2d5c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e2d5c-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e2d5c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e2d5c-117">Attribute-Id</span></span>      | <span data-ttu-id="e2d5c-118">1.2.840.113556.1.4.753</span><span class="sxs-lookup"><span data-stu-id="e2d5c-118">1.2.840.113556.1.4.753</span></span>               |
| <span data-ttu-id="e2d5c-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e2d5c-119">System-Id-Guid</span></span>    | <span data-ttu-id="e2d5c-120">80212840-4bdc-11d1-a9c4-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e2d5c-120">80212840-4bdc-11d1-a9c4-0000f80367c1</span></span> |
| <span data-ttu-id="e2d5c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2d5c-121">Syntax</span></span>            | [<span data-ttu-id="e2d5c-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e2d5c-123">實作</span><span class="sxs-lookup"><span data-stu-id="e2d5c-123">Implementations</span></span>

-   [<span data-ttu-id="e2d5c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e2d5c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e2d5c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e2d5c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e2d5c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e2d5c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e2d5c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2d5c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e2d5c-131">進入</span><span class="sxs-lookup"><span data-stu-id="e2d5c-131">Entry</span></span> | <span data-ttu-id="e2d5c-132">值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-132">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e2d5c-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2d5c-133">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2d5c-134">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2d5c-135">System-Only</span></span>            | <span data-ttu-id="e2d5c-136">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-136">False</span></span>                                              |
| <span data-ttu-id="e2d5c-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e2d5c-138">對</span><span class="sxs-lookup"><span data-stu-id="e2d5c-138">True</span></span>                                               |
| <span data-ttu-id="e2d5c-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2d5c-139">Is Indexed</span></span>             | <span data-ttu-id="e2d5c-140">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-140">False</span></span>                                              |
| <span data-ttu-id="e2d5c-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2d5c-141">In Global Catalog</span></span>      | <span data-ttu-id="e2d5c-142">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-142">False</span></span>                                              |
| <span data-ttu-id="e2d5c-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2d5c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2d5c-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2d5c-144">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e2d5c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2d5c-145">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2d5c-146">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-147">Search-Flags</span></span>           | <span data-ttu-id="e2d5c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2d5c-148">0x00000000</span></span>                                         |
| <span data-ttu-id="e2d5c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-149">System-Flags</span></span>           | <span data-ttu-id="e2d5c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2d5c-150">0x00000010</span></span>                                         |
| <span data-ttu-id="e2d5c-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2d5c-151">Classes used in</span></span>        | [<span data-ttu-id="e2d5c-152">**Rpc-容器**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-152">**Rpc-Container**</span></span>](c-rpccontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e2d5c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2d5c-153">Windows Server 2003</span></span>



| <span data-ttu-id="e2d5c-154">進入</span><span class="sxs-lookup"><span data-stu-id="e2d5c-154">Entry</span></span> | <span data-ttu-id="e2d5c-155">值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-155">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e2d5c-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2d5c-156">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2d5c-157">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2d5c-158">System-Only</span></span>            | <span data-ttu-id="e2d5c-159">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-159">False</span></span>                                              |
| <span data-ttu-id="e2d5c-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e2d5c-161">對</span><span class="sxs-lookup"><span data-stu-id="e2d5c-161">True</span></span>                                               |
| <span data-ttu-id="e2d5c-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2d5c-162">Is Indexed</span></span>             | <span data-ttu-id="e2d5c-163">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-163">False</span></span>                                              |
| <span data-ttu-id="e2d5c-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2d5c-164">In Global Catalog</span></span>      | <span data-ttu-id="e2d5c-165">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-165">False</span></span>                                              |
| <span data-ttu-id="e2d5c-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2d5c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2d5c-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2d5c-167">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e2d5c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2d5c-168">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2d5c-169">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-170">Search-Flags</span></span>           | <span data-ttu-id="e2d5c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2d5c-171">0x00000000</span></span>                                         |
| <span data-ttu-id="e2d5c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-172">System-Flags</span></span>           | <span data-ttu-id="e2d5c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2d5c-173">0x00000010</span></span>                                         |
| <span data-ttu-id="e2d5c-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2d5c-174">Classes used in</span></span>        | [<span data-ttu-id="e2d5c-175">**Rpc-容器**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-175">**Rpc-Container**</span></span>](c-rpccontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e2d5c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e2d5c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e2d5c-177">進入</span><span class="sxs-lookup"><span data-stu-id="e2d5c-177">Entry</span></span> | <span data-ttu-id="e2d5c-178">值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-178">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e2d5c-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2d5c-179">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2d5c-180">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2d5c-181">System-Only</span></span>            | <span data-ttu-id="e2d5c-182">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-182">False</span></span>                                              |
| <span data-ttu-id="e2d5c-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e2d5c-184">對</span><span class="sxs-lookup"><span data-stu-id="e2d5c-184">True</span></span>                                               |
| <span data-ttu-id="e2d5c-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2d5c-185">Is Indexed</span></span>             | <span data-ttu-id="e2d5c-186">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-186">False</span></span>                                              |
| <span data-ttu-id="e2d5c-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2d5c-187">In Global Catalog</span></span>      | <span data-ttu-id="e2d5c-188">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-188">False</span></span>                                              |
| <span data-ttu-id="e2d5c-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2d5c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2d5c-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2d5c-190">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e2d5c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2d5c-191">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2d5c-192">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-193">Search-Flags</span></span>           | <span data-ttu-id="e2d5c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2d5c-194">0x00000000</span></span>                                         |
| <span data-ttu-id="e2d5c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-195">System-Flags</span></span>           | <span data-ttu-id="e2d5c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2d5c-196">0x00000010</span></span>                                         |
| <span data-ttu-id="e2d5c-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2d5c-197">Classes used in</span></span>        | [<span data-ttu-id="e2d5c-198">**Rpc-容器**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-198">**Rpc-Container**</span></span>](c-rpccontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e2d5c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2d5c-199">Windows Server 2008</span></span>



| <span data-ttu-id="e2d5c-200">進入</span><span class="sxs-lookup"><span data-stu-id="e2d5c-200">Entry</span></span> | <span data-ttu-id="e2d5c-201">值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-201">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e2d5c-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2d5c-202">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2d5c-203">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2d5c-204">System-Only</span></span>            | <span data-ttu-id="e2d5c-205">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-205">False</span></span>                                              |
| <span data-ttu-id="e2d5c-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e2d5c-207">對</span><span class="sxs-lookup"><span data-stu-id="e2d5c-207">True</span></span>                                               |
| <span data-ttu-id="e2d5c-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2d5c-208">Is Indexed</span></span>             | <span data-ttu-id="e2d5c-209">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-209">False</span></span>                                              |
| <span data-ttu-id="e2d5c-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2d5c-210">In Global Catalog</span></span>      | <span data-ttu-id="e2d5c-211">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-211">False</span></span>                                              |
| <span data-ttu-id="e2d5c-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2d5c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2d5c-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2d5c-213">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e2d5c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2d5c-214">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2d5c-215">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-216">Search-Flags</span></span>           | <span data-ttu-id="e2d5c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2d5c-217">0x00000000</span></span>                                         |
| <span data-ttu-id="e2d5c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-218">System-Flags</span></span>           | <span data-ttu-id="e2d5c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2d5c-219">0x00000010</span></span>                                         |
| <span data-ttu-id="e2d5c-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2d5c-220">Classes used in</span></span>        | [<span data-ttu-id="e2d5c-221">**Rpc-容器**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-221">**Rpc-Container**</span></span>](c-rpccontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e2d5c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2d5c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e2d5c-223">進入</span><span class="sxs-lookup"><span data-stu-id="e2d5c-223">Entry</span></span> | <span data-ttu-id="e2d5c-224">值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-224">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e2d5c-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2d5c-225">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2d5c-226">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2d5c-227">System-Only</span></span>            | <span data-ttu-id="e2d5c-228">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-228">False</span></span>                                              |
| <span data-ttu-id="e2d5c-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e2d5c-230">對</span><span class="sxs-lookup"><span data-stu-id="e2d5c-230">True</span></span>                                               |
| <span data-ttu-id="e2d5c-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2d5c-231">Is Indexed</span></span>             | <span data-ttu-id="e2d5c-232">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-232">False</span></span>                                              |
| <span data-ttu-id="e2d5c-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2d5c-233">In Global Catalog</span></span>      | <span data-ttu-id="e2d5c-234">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-234">False</span></span>                                              |
| <span data-ttu-id="e2d5c-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2d5c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2d5c-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2d5c-236">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e2d5c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2d5c-237">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2d5c-238">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-239">Search-Flags</span></span>           | <span data-ttu-id="e2d5c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2d5c-240">0x00000000</span></span>                                         |
| <span data-ttu-id="e2d5c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-241">System-Flags</span></span>           | <span data-ttu-id="e2d5c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2d5c-242">0x00000010</span></span>                                         |
| <span data-ttu-id="e2d5c-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2d5c-243">Classes used in</span></span>        | [<span data-ttu-id="e2d5c-244">**Rpc-容器**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-244">**Rpc-Container**</span></span>](c-rpccontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e2d5c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2d5c-245">Windows Server 2012</span></span>



| <span data-ttu-id="e2d5c-246">進入</span><span class="sxs-lookup"><span data-stu-id="e2d5c-246">Entry</span></span> | <span data-ttu-id="e2d5c-247">值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-247">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e2d5c-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e2d5c-248">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2d5c-249">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e2d5c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2d5c-250">System-Only</span></span>            | <span data-ttu-id="e2d5c-251">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-251">False</span></span>                                              |
| <span data-ttu-id="e2d5c-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e2d5c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e2d5c-253">對</span><span class="sxs-lookup"><span data-stu-id="e2d5c-253">True</span></span>                                               |
| <span data-ttu-id="e2d5c-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e2d5c-254">Is Indexed</span></span>             | <span data-ttu-id="e2d5c-255">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-255">False</span></span>                                              |
| <span data-ttu-id="e2d5c-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e2d5c-256">In Global Catalog</span></span>      | <span data-ttu-id="e2d5c-257">否</span><span class="sxs-lookup"><span data-stu-id="e2d5c-257">False</span></span>                                              |
| <span data-ttu-id="e2d5c-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e2d5c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2d5c-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e2d5c-259">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e2d5c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2d5c-260">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2d5c-261">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e2d5c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-262">Search-Flags</span></span>           | <span data-ttu-id="e2d5c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2d5c-263">0x00000000</span></span>                                         |
| <span data-ttu-id="e2d5c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2d5c-264">System-Flags</span></span>           | <span data-ttu-id="e2d5c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2d5c-265">0x00000010</span></span>                                         |
| <span data-ttu-id="e2d5c-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e2d5c-266">Classes used in</span></span>        | [<span data-ttu-id="e2d5c-267">**Rpc-容器**</span><span class="sxs-lookup"><span data-stu-id="e2d5c-267">**Rpc-Container**</span></span>](c-rpccontainer.md)<br/> |



 

 





