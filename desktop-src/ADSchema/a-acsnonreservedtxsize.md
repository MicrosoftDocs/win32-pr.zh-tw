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
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="a41c1-105">ACS-非保留的 Tx 大小屬性</span><span class="sxs-lookup"><span data-stu-id="a41c1-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="a41c1-106">應用程式可以在保留備妥之前使用的權杖 bucket 大小。</span><span class="sxs-lookup"><span data-stu-id="a41c1-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="a41c1-107">進入</span><span class="sxs-lookup"><span data-stu-id="a41c1-107">Entry</span></span> | <span data-ttu-id="a41c1-108">值</span><span class="sxs-lookup"><span data-stu-id="a41c1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a41c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="a41c1-109">CN</span></span>                | <span data-ttu-id="a41c1-110">ACS-非保留-德克薩斯維大小</span><span class="sxs-lookup"><span data-stu-id="a41c1-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="a41c1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a41c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a41c1-112">aCSNonReservedTxSize</span><span class="sxs-lookup"><span data-stu-id="a41c1-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="a41c1-113">大小</span><span class="sxs-lookup"><span data-stu-id="a41c1-113">Size</span></span>              | <span data-ttu-id="a41c1-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="a41c1-114">8 bytes</span></span>                              |
| <span data-ttu-id="a41c1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a41c1-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a41c1-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a41c1-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a41c1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a41c1-117">Attribute-Id</span></span>      | <span data-ttu-id="a41c1-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="a41c1-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="a41c1-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a41c1-119">System-Id-Guid</span></span>    | <span data-ttu-id="a41c1-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a41c1-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="a41c1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="a41c1-121">Syntax</span></span>            | [<span data-ttu-id="a41c1-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="a41c1-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="a41c1-123">實作</span><span class="sxs-lookup"><span data-stu-id="a41c1-123">Implementations</span></span>

-   [<span data-ttu-id="a41c1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a41c1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a41c1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a41c1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a41c1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a41c1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a41c1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a41c1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a41c1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a41c1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a41c1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a41c1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a41c1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a41c1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a41c1-131">進入</span><span class="sxs-lookup"><span data-stu-id="a41c1-131">Entry</span></span> | <span data-ttu-id="a41c1-132">值</span><span class="sxs-lookup"><span data-stu-id="a41c1-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a41c1-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a41c1-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a41c1-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a41c1-135">System-Only</span></span>            | <span data-ttu-id="a41c1-136">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-136">False</span></span>                                        |
| <span data-ttu-id="a41c1-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a41c1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a41c1-138">對</span><span class="sxs-lookup"><span data-stu-id="a41c1-138">True</span></span>                                         |
| <span data-ttu-id="a41c1-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a41c1-139">Is Indexed</span></span>             | <span data-ttu-id="a41c1-140">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-140">False</span></span>                                        |
| <span data-ttu-id="a41c1-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a41c1-141">In Global Catalog</span></span>      | <span data-ttu-id="a41c1-142">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-142">False</span></span>                                        |
| <span data-ttu-id="a41c1-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a41c1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a41c1-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a41c1-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a41c1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a41c1-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a41c1-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-147">Search-Flags</span></span>           | <span data-ttu-id="a41c1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a41c1-148">0x00000000</span></span>                                   |
| <span data-ttu-id="a41c1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-149">System-Flags</span></span>           | <span data-ttu-id="a41c1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a41c1-150">0x00000010</span></span>                                   |
| <span data-ttu-id="a41c1-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a41c1-151">Classes used in</span></span>        | [<span data-ttu-id="a41c1-152">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="a41c1-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a41c1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a41c1-153">Windows Server 2003</span></span>



| <span data-ttu-id="a41c1-154">進入</span><span class="sxs-lookup"><span data-stu-id="a41c1-154">Entry</span></span> | <span data-ttu-id="a41c1-155">值</span><span class="sxs-lookup"><span data-stu-id="a41c1-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a41c1-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a41c1-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a41c1-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a41c1-158">System-Only</span></span>            | <span data-ttu-id="a41c1-159">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-159">False</span></span>                                        |
| <span data-ttu-id="a41c1-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a41c1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a41c1-161">對</span><span class="sxs-lookup"><span data-stu-id="a41c1-161">True</span></span>                                         |
| <span data-ttu-id="a41c1-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a41c1-162">Is Indexed</span></span>             | <span data-ttu-id="a41c1-163">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-163">False</span></span>                                        |
| <span data-ttu-id="a41c1-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a41c1-164">In Global Catalog</span></span>      | <span data-ttu-id="a41c1-165">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-165">False</span></span>                                        |
| <span data-ttu-id="a41c1-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a41c1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a41c1-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a41c1-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a41c1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a41c1-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a41c1-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-170">Search-Flags</span></span>           | <span data-ttu-id="a41c1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a41c1-171">0x00000000</span></span>                                   |
| <span data-ttu-id="a41c1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-172">System-Flags</span></span>           | <span data-ttu-id="a41c1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a41c1-173">0x00000010</span></span>                                   |
| <span data-ttu-id="a41c1-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a41c1-174">Classes used in</span></span>        | [<span data-ttu-id="a41c1-175">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="a41c1-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a41c1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a41c1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a41c1-177">進入</span><span class="sxs-lookup"><span data-stu-id="a41c1-177">Entry</span></span> | <span data-ttu-id="a41c1-178">值</span><span class="sxs-lookup"><span data-stu-id="a41c1-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a41c1-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a41c1-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a41c1-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a41c1-181">System-Only</span></span>            | <span data-ttu-id="a41c1-182">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-182">False</span></span>                                        |
| <span data-ttu-id="a41c1-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a41c1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a41c1-184">對</span><span class="sxs-lookup"><span data-stu-id="a41c1-184">True</span></span>                                         |
| <span data-ttu-id="a41c1-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a41c1-185">Is Indexed</span></span>             | <span data-ttu-id="a41c1-186">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-186">False</span></span>                                        |
| <span data-ttu-id="a41c1-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a41c1-187">In Global Catalog</span></span>      | <span data-ttu-id="a41c1-188">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-188">False</span></span>                                        |
| <span data-ttu-id="a41c1-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a41c1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a41c1-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a41c1-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a41c1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a41c1-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a41c1-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-193">Search-Flags</span></span>           | <span data-ttu-id="a41c1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a41c1-194">0x00000000</span></span>                                   |
| <span data-ttu-id="a41c1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-195">System-Flags</span></span>           | <span data-ttu-id="a41c1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a41c1-196">0x00000010</span></span>                                   |
| <span data-ttu-id="a41c1-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a41c1-197">Classes used in</span></span>        | [<span data-ttu-id="a41c1-198">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="a41c1-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a41c1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a41c1-199">Windows Server 2008</span></span>



| <span data-ttu-id="a41c1-200">進入</span><span class="sxs-lookup"><span data-stu-id="a41c1-200">Entry</span></span> | <span data-ttu-id="a41c1-201">值</span><span class="sxs-lookup"><span data-stu-id="a41c1-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a41c1-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a41c1-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a41c1-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a41c1-204">System-Only</span></span>            | <span data-ttu-id="a41c1-205">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-205">False</span></span>                                        |
| <span data-ttu-id="a41c1-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a41c1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a41c1-207">對</span><span class="sxs-lookup"><span data-stu-id="a41c1-207">True</span></span>                                         |
| <span data-ttu-id="a41c1-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a41c1-208">Is Indexed</span></span>             | <span data-ttu-id="a41c1-209">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-209">False</span></span>                                        |
| <span data-ttu-id="a41c1-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a41c1-210">In Global Catalog</span></span>      | <span data-ttu-id="a41c1-211">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-211">False</span></span>                                        |
| <span data-ttu-id="a41c1-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a41c1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a41c1-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a41c1-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a41c1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a41c1-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a41c1-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-216">Search-Flags</span></span>           | <span data-ttu-id="a41c1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a41c1-217">0x00000000</span></span>                                   |
| <span data-ttu-id="a41c1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-218">System-Flags</span></span>           | <span data-ttu-id="a41c1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a41c1-219">0x00000010</span></span>                                   |
| <span data-ttu-id="a41c1-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a41c1-220">Classes used in</span></span>        | [<span data-ttu-id="a41c1-221">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="a41c1-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a41c1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a41c1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a41c1-223">進入</span><span class="sxs-lookup"><span data-stu-id="a41c1-223">Entry</span></span> | <span data-ttu-id="a41c1-224">值</span><span class="sxs-lookup"><span data-stu-id="a41c1-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a41c1-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a41c1-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a41c1-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a41c1-227">System-Only</span></span>            | <span data-ttu-id="a41c1-228">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-228">False</span></span>                                        |
| <span data-ttu-id="a41c1-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a41c1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a41c1-230">對</span><span class="sxs-lookup"><span data-stu-id="a41c1-230">True</span></span>                                         |
| <span data-ttu-id="a41c1-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a41c1-231">Is Indexed</span></span>             | <span data-ttu-id="a41c1-232">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-232">False</span></span>                                        |
| <span data-ttu-id="a41c1-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a41c1-233">In Global Catalog</span></span>      | <span data-ttu-id="a41c1-234">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-234">False</span></span>                                        |
| <span data-ttu-id="a41c1-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a41c1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a41c1-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a41c1-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a41c1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a41c1-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a41c1-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-239">Search-Flags</span></span>           | <span data-ttu-id="a41c1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a41c1-240">0x00000000</span></span>                                   |
| <span data-ttu-id="a41c1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-241">System-Flags</span></span>           | <span data-ttu-id="a41c1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a41c1-242">0x00000010</span></span>                                   |
| <span data-ttu-id="a41c1-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a41c1-243">Classes used in</span></span>        | [<span data-ttu-id="a41c1-244">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="a41c1-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a41c1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a41c1-245">Windows Server 2012</span></span>



| <span data-ttu-id="a41c1-246">進入</span><span class="sxs-lookup"><span data-stu-id="a41c1-246">Entry</span></span> | <span data-ttu-id="a41c1-247">值</span><span class="sxs-lookup"><span data-stu-id="a41c1-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a41c1-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a41c1-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a41c1-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a41c1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a41c1-250">System-Only</span></span>            | <span data-ttu-id="a41c1-251">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-251">False</span></span>                                        |
| <span data-ttu-id="a41c1-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a41c1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a41c1-253">對</span><span class="sxs-lookup"><span data-stu-id="a41c1-253">True</span></span>                                         |
| <span data-ttu-id="a41c1-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a41c1-254">Is Indexed</span></span>             | <span data-ttu-id="a41c1-255">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-255">False</span></span>                                        |
| <span data-ttu-id="a41c1-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a41c1-256">In Global Catalog</span></span>      | <span data-ttu-id="a41c1-257">否</span><span class="sxs-lookup"><span data-stu-id="a41c1-257">False</span></span>                                        |
| <span data-ttu-id="a41c1-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a41c1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a41c1-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a41c1-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a41c1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a41c1-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a41c1-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a41c1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-262">Search-Flags</span></span>           | <span data-ttu-id="a41c1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a41c1-263">0x00000000</span></span>                                   |
| <span data-ttu-id="a41c1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a41c1-264">System-Flags</span></span>           | <span data-ttu-id="a41c1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a41c1-265">0x00000010</span></span>                                   |
| <span data-ttu-id="a41c1-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a41c1-266">Classes used in</span></span>        | [<span data-ttu-id="a41c1-267">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="a41c1-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





