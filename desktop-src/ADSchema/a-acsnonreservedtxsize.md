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
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="8b007-105">ACS-非保留的 Tx 大小屬性</span><span class="sxs-lookup"><span data-stu-id="8b007-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="8b007-106">應用程式可以在保留備妥之前使用的權杖 bucket 大小。</span><span class="sxs-lookup"><span data-stu-id="8b007-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="8b007-107">進入</span><span class="sxs-lookup"><span data-stu-id="8b007-107">Entry</span></span> | <span data-ttu-id="8b007-108">值</span><span class="sxs-lookup"><span data-stu-id="8b007-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8b007-109">CN</span><span class="sxs-lookup"><span data-stu-id="8b007-109">CN</span></span>                | <span data-ttu-id="8b007-110">ACS-非保留-德克薩斯維大小</span><span class="sxs-lookup"><span data-stu-id="8b007-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="8b007-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8b007-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8b007-112">aCSNonReservedTxSize</span><span class="sxs-lookup"><span data-stu-id="8b007-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="8b007-113">大小</span><span class="sxs-lookup"><span data-stu-id="8b007-113">Size</span></span>              | <span data-ttu-id="8b007-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="8b007-114">8 bytes</span></span>                              |
| <span data-ttu-id="8b007-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8b007-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8b007-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8b007-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8b007-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b007-117">Attribute-Id</span></span>      | <span data-ttu-id="8b007-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="8b007-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="8b007-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8b007-119">System-Id-Guid</span></span>    | <span data-ttu-id="8b007-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8b007-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="8b007-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b007-121">Syntax</span></span>            | [<span data-ttu-id="8b007-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="8b007-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8b007-123">實作</span><span class="sxs-lookup"><span data-stu-id="8b007-123">Implementations</span></span>

-   [<span data-ttu-id="8b007-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8b007-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8b007-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b007-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b007-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b007-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b007-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b007-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b007-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b007-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b007-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b007-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8b007-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b007-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8b007-131">進入</span><span class="sxs-lookup"><span data-stu-id="8b007-131">Entry</span></span> | <span data-ttu-id="8b007-132">值</span><span class="sxs-lookup"><span data-stu-id="8b007-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b007-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b007-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b007-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b007-135">System-Only</span></span>            | <span data-ttu-id="8b007-136">否</span><span class="sxs-lookup"><span data-stu-id="8b007-136">False</span></span>                                        |
| <span data-ttu-id="8b007-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b007-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8b007-138">對</span><span class="sxs-lookup"><span data-stu-id="8b007-138">True</span></span>                                         |
| <span data-ttu-id="8b007-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b007-139">Is Indexed</span></span>             | <span data-ttu-id="8b007-140">否</span><span class="sxs-lookup"><span data-stu-id="8b007-140">False</span></span>                                        |
| <span data-ttu-id="8b007-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b007-141">In Global Catalog</span></span>      | <span data-ttu-id="8b007-142">否</span><span class="sxs-lookup"><span data-stu-id="8b007-142">False</span></span>                                        |
| <span data-ttu-id="8b007-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b007-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b007-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b007-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b007-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b007-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b007-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b007-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b007-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-147">Search-Flags</span></span>           | <span data-ttu-id="8b007-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b007-148">0x00000000</span></span>                                   |
| <span data-ttu-id="8b007-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-149">System-Flags</span></span>           | <span data-ttu-id="8b007-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b007-150">0x00000010</span></span>                                   |
| <span data-ttu-id="8b007-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b007-151">Classes used in</span></span>        | [<span data-ttu-id="8b007-152">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="8b007-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8b007-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b007-153">Windows Server 2003</span></span>



| <span data-ttu-id="8b007-154">進入</span><span class="sxs-lookup"><span data-stu-id="8b007-154">Entry</span></span> | <span data-ttu-id="8b007-155">值</span><span class="sxs-lookup"><span data-stu-id="8b007-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b007-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b007-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b007-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b007-158">System-Only</span></span>            | <span data-ttu-id="8b007-159">否</span><span class="sxs-lookup"><span data-stu-id="8b007-159">False</span></span>                                        |
| <span data-ttu-id="8b007-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b007-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8b007-161">對</span><span class="sxs-lookup"><span data-stu-id="8b007-161">True</span></span>                                         |
| <span data-ttu-id="8b007-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b007-162">Is Indexed</span></span>             | <span data-ttu-id="8b007-163">否</span><span class="sxs-lookup"><span data-stu-id="8b007-163">False</span></span>                                        |
| <span data-ttu-id="8b007-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b007-164">In Global Catalog</span></span>      | <span data-ttu-id="8b007-165">否</span><span class="sxs-lookup"><span data-stu-id="8b007-165">False</span></span>                                        |
| <span data-ttu-id="8b007-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b007-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b007-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b007-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b007-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b007-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b007-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b007-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b007-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-170">Search-Flags</span></span>           | <span data-ttu-id="8b007-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b007-171">0x00000000</span></span>                                   |
| <span data-ttu-id="8b007-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-172">System-Flags</span></span>           | <span data-ttu-id="8b007-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b007-173">0x00000010</span></span>                                   |
| <span data-ttu-id="8b007-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b007-174">Classes used in</span></span>        | [<span data-ttu-id="8b007-175">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="8b007-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b007-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b007-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b007-177">進入</span><span class="sxs-lookup"><span data-stu-id="8b007-177">Entry</span></span> | <span data-ttu-id="8b007-178">值</span><span class="sxs-lookup"><span data-stu-id="8b007-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b007-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b007-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b007-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b007-181">System-Only</span></span>            | <span data-ttu-id="8b007-182">否</span><span class="sxs-lookup"><span data-stu-id="8b007-182">False</span></span>                                        |
| <span data-ttu-id="8b007-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b007-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8b007-184">對</span><span class="sxs-lookup"><span data-stu-id="8b007-184">True</span></span>                                         |
| <span data-ttu-id="8b007-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b007-185">Is Indexed</span></span>             | <span data-ttu-id="8b007-186">否</span><span class="sxs-lookup"><span data-stu-id="8b007-186">False</span></span>                                        |
| <span data-ttu-id="8b007-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b007-187">In Global Catalog</span></span>      | <span data-ttu-id="8b007-188">否</span><span class="sxs-lookup"><span data-stu-id="8b007-188">False</span></span>                                        |
| <span data-ttu-id="8b007-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b007-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b007-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b007-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b007-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b007-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b007-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b007-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b007-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-193">Search-Flags</span></span>           | <span data-ttu-id="8b007-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b007-194">0x00000000</span></span>                                   |
| <span data-ttu-id="8b007-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-195">System-Flags</span></span>           | <span data-ttu-id="8b007-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b007-196">0x00000010</span></span>                                   |
| <span data-ttu-id="8b007-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b007-197">Classes used in</span></span>        | [<span data-ttu-id="8b007-198">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="8b007-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b007-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b007-199">Windows Server 2008</span></span>



| <span data-ttu-id="8b007-200">進入</span><span class="sxs-lookup"><span data-stu-id="8b007-200">Entry</span></span> | <span data-ttu-id="8b007-201">值</span><span class="sxs-lookup"><span data-stu-id="8b007-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b007-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b007-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b007-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b007-204">System-Only</span></span>            | <span data-ttu-id="8b007-205">否</span><span class="sxs-lookup"><span data-stu-id="8b007-205">False</span></span>                                        |
| <span data-ttu-id="8b007-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b007-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8b007-207">對</span><span class="sxs-lookup"><span data-stu-id="8b007-207">True</span></span>                                         |
| <span data-ttu-id="8b007-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b007-208">Is Indexed</span></span>             | <span data-ttu-id="8b007-209">否</span><span class="sxs-lookup"><span data-stu-id="8b007-209">False</span></span>                                        |
| <span data-ttu-id="8b007-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b007-210">In Global Catalog</span></span>      | <span data-ttu-id="8b007-211">否</span><span class="sxs-lookup"><span data-stu-id="8b007-211">False</span></span>                                        |
| <span data-ttu-id="8b007-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b007-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b007-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b007-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b007-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b007-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b007-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b007-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b007-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-216">Search-Flags</span></span>           | <span data-ttu-id="8b007-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b007-217">0x00000000</span></span>                                   |
| <span data-ttu-id="8b007-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-218">System-Flags</span></span>           | <span data-ttu-id="8b007-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b007-219">0x00000010</span></span>                                   |
| <span data-ttu-id="8b007-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b007-220">Classes used in</span></span>        | [<span data-ttu-id="8b007-221">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="8b007-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b007-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b007-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b007-223">進入</span><span class="sxs-lookup"><span data-stu-id="8b007-223">Entry</span></span> | <span data-ttu-id="8b007-224">值</span><span class="sxs-lookup"><span data-stu-id="8b007-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b007-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b007-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b007-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b007-227">System-Only</span></span>            | <span data-ttu-id="8b007-228">否</span><span class="sxs-lookup"><span data-stu-id="8b007-228">False</span></span>                                        |
| <span data-ttu-id="8b007-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b007-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8b007-230">對</span><span class="sxs-lookup"><span data-stu-id="8b007-230">True</span></span>                                         |
| <span data-ttu-id="8b007-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b007-231">Is Indexed</span></span>             | <span data-ttu-id="8b007-232">否</span><span class="sxs-lookup"><span data-stu-id="8b007-232">False</span></span>                                        |
| <span data-ttu-id="8b007-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b007-233">In Global Catalog</span></span>      | <span data-ttu-id="8b007-234">否</span><span class="sxs-lookup"><span data-stu-id="8b007-234">False</span></span>                                        |
| <span data-ttu-id="8b007-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b007-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b007-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b007-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b007-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b007-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b007-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b007-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b007-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-239">Search-Flags</span></span>           | <span data-ttu-id="8b007-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b007-240">0x00000000</span></span>                                   |
| <span data-ttu-id="8b007-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-241">System-Flags</span></span>           | <span data-ttu-id="8b007-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b007-242">0x00000010</span></span>                                   |
| <span data-ttu-id="8b007-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b007-243">Classes used in</span></span>        | [<span data-ttu-id="8b007-244">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="8b007-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b007-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b007-245">Windows Server 2012</span></span>



| <span data-ttu-id="8b007-246">進入</span><span class="sxs-lookup"><span data-stu-id="8b007-246">Entry</span></span> | <span data-ttu-id="8b007-247">值</span><span class="sxs-lookup"><span data-stu-id="8b007-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8b007-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8b007-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b007-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8b007-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b007-250">System-Only</span></span>            | <span data-ttu-id="8b007-251">否</span><span class="sxs-lookup"><span data-stu-id="8b007-251">False</span></span>                                        |
| <span data-ttu-id="8b007-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8b007-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8b007-253">對</span><span class="sxs-lookup"><span data-stu-id="8b007-253">True</span></span>                                         |
| <span data-ttu-id="8b007-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8b007-254">Is Indexed</span></span>             | <span data-ttu-id="8b007-255">否</span><span class="sxs-lookup"><span data-stu-id="8b007-255">False</span></span>                                        |
| <span data-ttu-id="8b007-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8b007-256">In Global Catalog</span></span>      | <span data-ttu-id="8b007-257">否</span><span class="sxs-lookup"><span data-stu-id="8b007-257">False</span></span>                                        |
| <span data-ttu-id="8b007-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8b007-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b007-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8b007-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8b007-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b007-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8b007-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b007-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8b007-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-262">Search-Flags</span></span>           | <span data-ttu-id="8b007-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b007-263">0x00000000</span></span>                                   |
| <span data-ttu-id="8b007-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b007-264">System-Flags</span></span>           | <span data-ttu-id="8b007-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b007-265">0x00000010</span></span>                                   |
| <span data-ttu-id="8b007-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8b007-266">Classes used in</span></span>        | [<span data-ttu-id="8b007-267">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="8b007-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





