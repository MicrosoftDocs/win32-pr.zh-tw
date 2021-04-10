---
title: ACS-非保留的 Tx 大小屬性
description: 應用程式可以在保留備妥之前使用的權杖 bucket 大小。
ms.assetid: 67a0d6fd-b556-49d2-8c5b-6efebf1052c3
ms.tgt_platform: multiple
keywords:
- ACS-非保留的 Tx-Size 屬性 AD 架構
- aCSNonReservedTxSize 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cd19dde97e3a9fc6ef58165c8dbcbfbebba729
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845647"
---
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="2ee82-105">ACS-非保留的 Tx 大小屬性</span><span class="sxs-lookup"><span data-stu-id="2ee82-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="2ee82-106">應用程式可以在保留備妥之前使用的權杖 bucket 大小。</span><span class="sxs-lookup"><span data-stu-id="2ee82-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="2ee82-107">進入</span><span class="sxs-lookup"><span data-stu-id="2ee82-107">Entry</span></span> | <span data-ttu-id="2ee82-108">值</span><span class="sxs-lookup"><span data-stu-id="2ee82-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2ee82-109">CN</span><span class="sxs-lookup"><span data-stu-id="2ee82-109">CN</span></span>                | <span data-ttu-id="2ee82-110">ACS-非保留-德克薩斯維大小</span><span class="sxs-lookup"><span data-stu-id="2ee82-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="2ee82-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2ee82-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2ee82-112">aCSNonReservedTxSize</span><span class="sxs-lookup"><span data-stu-id="2ee82-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="2ee82-113">大小</span><span class="sxs-lookup"><span data-stu-id="2ee82-113">Size</span></span>              | <span data-ttu-id="2ee82-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="2ee82-114">8 bytes</span></span>                              |
| <span data-ttu-id="2ee82-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2ee82-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2ee82-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2ee82-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2ee82-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ee82-117">Attribute-Id</span></span>      | <span data-ttu-id="2ee82-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="2ee82-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="2ee82-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2ee82-119">System-Id-Guid</span></span>    | <span data-ttu-id="2ee82-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2ee82-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="2ee82-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ee82-121">Syntax</span></span>            | [<span data-ttu-id="2ee82-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="2ee82-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2ee82-123">實作</span><span class="sxs-lookup"><span data-stu-id="2ee82-123">Implementations</span></span>

-   [<span data-ttu-id="2ee82-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2ee82-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2ee82-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ee82-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ee82-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ee82-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ee82-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ee82-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ee82-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ee82-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ee82-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ee82-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2ee82-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ee82-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2ee82-131">進入</span><span class="sxs-lookup"><span data-stu-id="2ee82-131">Entry</span></span> | <span data-ttu-id="2ee82-132">值</span><span class="sxs-lookup"><span data-stu-id="2ee82-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2ee82-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2ee82-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ee82-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ee82-135">System-Only</span></span>            | <span data-ttu-id="2ee82-136">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-136">False</span></span>                                        |
| <span data-ttu-id="2ee82-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2ee82-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2ee82-138">對</span><span class="sxs-lookup"><span data-stu-id="2ee82-138">True</span></span>                                         |
| <span data-ttu-id="2ee82-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2ee82-139">Is Indexed</span></span>             | <span data-ttu-id="2ee82-140">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-140">False</span></span>                                        |
| <span data-ttu-id="2ee82-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2ee82-141">In Global Catalog</span></span>      | <span data-ttu-id="2ee82-142">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-142">False</span></span>                                        |
| <span data-ttu-id="2ee82-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2ee82-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ee82-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2ee82-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2ee82-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ee82-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ee82-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-147">Search-Flags</span></span>           | <span data-ttu-id="2ee82-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee82-148">0x00000000</span></span>                                   |
| <span data-ttu-id="2ee82-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-149">System-Flags</span></span>           | <span data-ttu-id="2ee82-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ee82-150">0x00000010</span></span>                                   |
| <span data-ttu-id="2ee82-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2ee82-151">Classes used in</span></span>        | [<span data-ttu-id="2ee82-152">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="2ee82-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2ee82-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ee82-153">Windows Server 2003</span></span>



| <span data-ttu-id="2ee82-154">進入</span><span class="sxs-lookup"><span data-stu-id="2ee82-154">Entry</span></span> | <span data-ttu-id="2ee82-155">值</span><span class="sxs-lookup"><span data-stu-id="2ee82-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2ee82-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2ee82-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ee82-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ee82-158">System-Only</span></span>            | <span data-ttu-id="2ee82-159">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-159">False</span></span>                                        |
| <span data-ttu-id="2ee82-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2ee82-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2ee82-161">對</span><span class="sxs-lookup"><span data-stu-id="2ee82-161">True</span></span>                                         |
| <span data-ttu-id="2ee82-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2ee82-162">Is Indexed</span></span>             | <span data-ttu-id="2ee82-163">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-163">False</span></span>                                        |
| <span data-ttu-id="2ee82-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2ee82-164">In Global Catalog</span></span>      | <span data-ttu-id="2ee82-165">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-165">False</span></span>                                        |
| <span data-ttu-id="2ee82-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2ee82-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ee82-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2ee82-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2ee82-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ee82-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ee82-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-170">Search-Flags</span></span>           | <span data-ttu-id="2ee82-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee82-171">0x00000000</span></span>                                   |
| <span data-ttu-id="2ee82-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-172">System-Flags</span></span>           | <span data-ttu-id="2ee82-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ee82-173">0x00000010</span></span>                                   |
| <span data-ttu-id="2ee82-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2ee82-174">Classes used in</span></span>        | [<span data-ttu-id="2ee82-175">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="2ee82-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ee82-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ee82-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ee82-177">進入</span><span class="sxs-lookup"><span data-stu-id="2ee82-177">Entry</span></span> | <span data-ttu-id="2ee82-178">值</span><span class="sxs-lookup"><span data-stu-id="2ee82-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2ee82-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2ee82-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ee82-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ee82-181">System-Only</span></span>            | <span data-ttu-id="2ee82-182">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-182">False</span></span>                                        |
| <span data-ttu-id="2ee82-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2ee82-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2ee82-184">對</span><span class="sxs-lookup"><span data-stu-id="2ee82-184">True</span></span>                                         |
| <span data-ttu-id="2ee82-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2ee82-185">Is Indexed</span></span>             | <span data-ttu-id="2ee82-186">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-186">False</span></span>                                        |
| <span data-ttu-id="2ee82-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2ee82-187">In Global Catalog</span></span>      | <span data-ttu-id="2ee82-188">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-188">False</span></span>                                        |
| <span data-ttu-id="2ee82-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2ee82-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ee82-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2ee82-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2ee82-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ee82-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ee82-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-193">Search-Flags</span></span>           | <span data-ttu-id="2ee82-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee82-194">0x00000000</span></span>                                   |
| <span data-ttu-id="2ee82-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-195">System-Flags</span></span>           | <span data-ttu-id="2ee82-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ee82-196">0x00000010</span></span>                                   |
| <span data-ttu-id="2ee82-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2ee82-197">Classes used in</span></span>        | [<span data-ttu-id="2ee82-198">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="2ee82-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ee82-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ee82-199">Windows Server 2008</span></span>



| <span data-ttu-id="2ee82-200">進入</span><span class="sxs-lookup"><span data-stu-id="2ee82-200">Entry</span></span> | <span data-ttu-id="2ee82-201">值</span><span class="sxs-lookup"><span data-stu-id="2ee82-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2ee82-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2ee82-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ee82-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ee82-204">System-Only</span></span>            | <span data-ttu-id="2ee82-205">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-205">False</span></span>                                        |
| <span data-ttu-id="2ee82-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2ee82-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2ee82-207">對</span><span class="sxs-lookup"><span data-stu-id="2ee82-207">True</span></span>                                         |
| <span data-ttu-id="2ee82-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2ee82-208">Is Indexed</span></span>             | <span data-ttu-id="2ee82-209">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-209">False</span></span>                                        |
| <span data-ttu-id="2ee82-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2ee82-210">In Global Catalog</span></span>      | <span data-ttu-id="2ee82-211">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-211">False</span></span>                                        |
| <span data-ttu-id="2ee82-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2ee82-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ee82-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2ee82-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2ee82-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ee82-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ee82-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-216">Search-Flags</span></span>           | <span data-ttu-id="2ee82-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee82-217">0x00000000</span></span>                                   |
| <span data-ttu-id="2ee82-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-218">System-Flags</span></span>           | <span data-ttu-id="2ee82-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ee82-219">0x00000010</span></span>                                   |
| <span data-ttu-id="2ee82-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2ee82-220">Classes used in</span></span>        | [<span data-ttu-id="2ee82-221">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="2ee82-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ee82-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ee82-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ee82-223">進入</span><span class="sxs-lookup"><span data-stu-id="2ee82-223">Entry</span></span> | <span data-ttu-id="2ee82-224">值</span><span class="sxs-lookup"><span data-stu-id="2ee82-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2ee82-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2ee82-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ee82-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ee82-227">System-Only</span></span>            | <span data-ttu-id="2ee82-228">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-228">False</span></span>                                        |
| <span data-ttu-id="2ee82-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2ee82-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2ee82-230">對</span><span class="sxs-lookup"><span data-stu-id="2ee82-230">True</span></span>                                         |
| <span data-ttu-id="2ee82-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2ee82-231">Is Indexed</span></span>             | <span data-ttu-id="2ee82-232">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-232">False</span></span>                                        |
| <span data-ttu-id="2ee82-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2ee82-233">In Global Catalog</span></span>      | <span data-ttu-id="2ee82-234">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-234">False</span></span>                                        |
| <span data-ttu-id="2ee82-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2ee82-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ee82-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2ee82-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2ee82-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ee82-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ee82-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-239">Search-Flags</span></span>           | <span data-ttu-id="2ee82-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee82-240">0x00000000</span></span>                                   |
| <span data-ttu-id="2ee82-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-241">System-Flags</span></span>           | <span data-ttu-id="2ee82-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ee82-242">0x00000010</span></span>                                   |
| <span data-ttu-id="2ee82-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2ee82-243">Classes used in</span></span>        | [<span data-ttu-id="2ee82-244">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="2ee82-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ee82-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ee82-245">Windows Server 2012</span></span>



| <span data-ttu-id="2ee82-246">進入</span><span class="sxs-lookup"><span data-stu-id="2ee82-246">Entry</span></span> | <span data-ttu-id="2ee82-247">值</span><span class="sxs-lookup"><span data-stu-id="2ee82-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2ee82-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2ee82-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ee82-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2ee82-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ee82-250">System-Only</span></span>            | <span data-ttu-id="2ee82-251">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-251">False</span></span>                                        |
| <span data-ttu-id="2ee82-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2ee82-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2ee82-253">對</span><span class="sxs-lookup"><span data-stu-id="2ee82-253">True</span></span>                                         |
| <span data-ttu-id="2ee82-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2ee82-254">Is Indexed</span></span>             | <span data-ttu-id="2ee82-255">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-255">False</span></span>                                        |
| <span data-ttu-id="2ee82-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2ee82-256">In Global Catalog</span></span>      | <span data-ttu-id="2ee82-257">否</span><span class="sxs-lookup"><span data-stu-id="2ee82-257">False</span></span>                                        |
| <span data-ttu-id="2ee82-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2ee82-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ee82-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2ee82-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2ee82-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ee82-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ee82-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2ee82-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-262">Search-Flags</span></span>           | <span data-ttu-id="2ee82-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee82-263">0x00000000</span></span>                                   |
| <span data-ttu-id="2ee82-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ee82-264">System-Flags</span></span>           | <span data-ttu-id="2ee82-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ee82-265">0x00000010</span></span>                                   |
| <span data-ttu-id="2ee82-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2ee82-266">Classes used in</span></span>        | [<span data-ttu-id="2ee82-267">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="2ee82-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





