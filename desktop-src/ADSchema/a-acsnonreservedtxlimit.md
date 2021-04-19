---
title: ACS-非保留的 Tx-Limit 屬性
description: 使用者應用程式可以在保留備妥之前傳輸的最大頻寬。
ms.assetid: 5ead8e5b-31e8-438e-8d1b-9aae8601dfc9
ms.tgt_platform: multiple
keywords:
- ACS-非保留的 Tx-Limit 屬性 AD 架構
- aCSNonReservedTxLimit 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999b1775640624b7825b38ae1632d70773bc75b3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106969011"
---
# <a name="acs-non-reserved-tx-limit-attribute"></a><span data-ttu-id="4631e-105">ACS-非保留的 Tx-Limit 屬性</span><span class="sxs-lookup"><span data-stu-id="4631e-105">ACS-Non-Reserved-Tx-Limit attribute</span></span>

<span data-ttu-id="4631e-106">使用者應用程式可以在保留備妥之前傳輸的最大頻寬。</span><span class="sxs-lookup"><span data-stu-id="4631e-106">The maximum bandwidth a user application can transmit before a reservation is in place.</span></span>



| <span data-ttu-id="4631e-107">進入</span><span class="sxs-lookup"><span data-stu-id="4631e-107">Entry</span></span> | <span data-ttu-id="4631e-108">值</span><span class="sxs-lookup"><span data-stu-id="4631e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4631e-109">CN</span><span class="sxs-lookup"><span data-stu-id="4631e-109">CN</span></span>                | <span data-ttu-id="4631e-110">ACS-非保留的 Tx-限制</span><span class="sxs-lookup"><span data-stu-id="4631e-110">ACS-Non-Reserved-Tx-Limit</span></span>            |
| <span data-ttu-id="4631e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4631e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4631e-112">aCSNonReservedTxLimit</span><span class="sxs-lookup"><span data-stu-id="4631e-112">aCSNonReservedTxLimit</span></span>                |
| <span data-ttu-id="4631e-113">大小</span><span class="sxs-lookup"><span data-stu-id="4631e-113">Size</span></span>              | <span data-ttu-id="4631e-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="4631e-114">8 bytes</span></span>                              |
| <span data-ttu-id="4631e-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4631e-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4631e-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4631e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4631e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4631e-117">Attribute-Id</span></span>      | <span data-ttu-id="4631e-118">1.2.840.113556.1.4.780</span><span class="sxs-lookup"><span data-stu-id="4631e-118">1.2.840.113556.1.4.780</span></span>               |
| <span data-ttu-id="4631e-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4631e-119">System-Id-Guid</span></span>    | <span data-ttu-id="4631e-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4631e-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="4631e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="4631e-121">Syntax</span></span>            | [<span data-ttu-id="4631e-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="4631e-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4631e-123">實作</span><span class="sxs-lookup"><span data-stu-id="4631e-123">Implementations</span></span>

-   [<span data-ttu-id="4631e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4631e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4631e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4631e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4631e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4631e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4631e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4631e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4631e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4631e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4631e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4631e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4631e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4631e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4631e-131">進入</span><span class="sxs-lookup"><span data-stu-id="4631e-131">Entry</span></span> | <span data-ttu-id="4631e-132">值</span><span class="sxs-lookup"><span data-stu-id="4631e-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4631e-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4631e-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4631e-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="4631e-135">System-Only</span></span>            | <span data-ttu-id="4631e-136">否</span><span class="sxs-lookup"><span data-stu-id="4631e-136">False</span></span>                                        |
| <span data-ttu-id="4631e-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4631e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="4631e-138">對</span><span class="sxs-lookup"><span data-stu-id="4631e-138">True</span></span>                                         |
| <span data-ttu-id="4631e-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4631e-139">Is Indexed</span></span>             | <span data-ttu-id="4631e-140">否</span><span class="sxs-lookup"><span data-stu-id="4631e-140">False</span></span>                                        |
| <span data-ttu-id="4631e-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4631e-141">In Global Catalog</span></span>      | <span data-ttu-id="4631e-142">否</span><span class="sxs-lookup"><span data-stu-id="4631e-142">False</span></span>                                        |
| <span data-ttu-id="4631e-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4631e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="4631e-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4631e-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4631e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4631e-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4631e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4631e-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4631e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-147">Search-Flags</span></span>           | <span data-ttu-id="4631e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4631e-148">0x00000000</span></span>                                   |
| <span data-ttu-id="4631e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-149">System-Flags</span></span>           | <span data-ttu-id="4631e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4631e-150">0x00000010</span></span>                                   |
| <span data-ttu-id="4631e-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4631e-151">Classes used in</span></span>        | [<span data-ttu-id="4631e-152">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4631e-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4631e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4631e-153">Windows Server 2003</span></span>



| <span data-ttu-id="4631e-154">進入</span><span class="sxs-lookup"><span data-stu-id="4631e-154">Entry</span></span> | <span data-ttu-id="4631e-155">值</span><span class="sxs-lookup"><span data-stu-id="4631e-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4631e-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4631e-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4631e-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="4631e-158">System-Only</span></span>            | <span data-ttu-id="4631e-159">否</span><span class="sxs-lookup"><span data-stu-id="4631e-159">False</span></span>                                        |
| <span data-ttu-id="4631e-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4631e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="4631e-161">對</span><span class="sxs-lookup"><span data-stu-id="4631e-161">True</span></span>                                         |
| <span data-ttu-id="4631e-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4631e-162">Is Indexed</span></span>             | <span data-ttu-id="4631e-163">否</span><span class="sxs-lookup"><span data-stu-id="4631e-163">False</span></span>                                        |
| <span data-ttu-id="4631e-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4631e-164">In Global Catalog</span></span>      | <span data-ttu-id="4631e-165">否</span><span class="sxs-lookup"><span data-stu-id="4631e-165">False</span></span>                                        |
| <span data-ttu-id="4631e-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4631e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="4631e-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4631e-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4631e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4631e-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4631e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4631e-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4631e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-170">Search-Flags</span></span>           | <span data-ttu-id="4631e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4631e-171">0x00000000</span></span>                                   |
| <span data-ttu-id="4631e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-172">System-Flags</span></span>           | <span data-ttu-id="4631e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4631e-173">0x00000010</span></span>                                   |
| <span data-ttu-id="4631e-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4631e-174">Classes used in</span></span>        | [<span data-ttu-id="4631e-175">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4631e-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4631e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4631e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4631e-177">進入</span><span class="sxs-lookup"><span data-stu-id="4631e-177">Entry</span></span> | <span data-ttu-id="4631e-178">值</span><span class="sxs-lookup"><span data-stu-id="4631e-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4631e-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4631e-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4631e-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="4631e-181">System-Only</span></span>            | <span data-ttu-id="4631e-182">否</span><span class="sxs-lookup"><span data-stu-id="4631e-182">False</span></span>                                        |
| <span data-ttu-id="4631e-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4631e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="4631e-184">對</span><span class="sxs-lookup"><span data-stu-id="4631e-184">True</span></span>                                         |
| <span data-ttu-id="4631e-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4631e-185">Is Indexed</span></span>             | <span data-ttu-id="4631e-186">否</span><span class="sxs-lookup"><span data-stu-id="4631e-186">False</span></span>                                        |
| <span data-ttu-id="4631e-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4631e-187">In Global Catalog</span></span>      | <span data-ttu-id="4631e-188">否</span><span class="sxs-lookup"><span data-stu-id="4631e-188">False</span></span>                                        |
| <span data-ttu-id="4631e-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4631e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="4631e-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4631e-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4631e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4631e-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4631e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4631e-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4631e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-193">Search-Flags</span></span>           | <span data-ttu-id="4631e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4631e-194">0x00000000</span></span>                                   |
| <span data-ttu-id="4631e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-195">System-Flags</span></span>           | <span data-ttu-id="4631e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4631e-196">0x00000010</span></span>                                   |
| <span data-ttu-id="4631e-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4631e-197">Classes used in</span></span>        | [<span data-ttu-id="4631e-198">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4631e-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4631e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4631e-199">Windows Server 2008</span></span>



| <span data-ttu-id="4631e-200">進入</span><span class="sxs-lookup"><span data-stu-id="4631e-200">Entry</span></span> | <span data-ttu-id="4631e-201">值</span><span class="sxs-lookup"><span data-stu-id="4631e-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4631e-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4631e-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4631e-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="4631e-204">System-Only</span></span>            | <span data-ttu-id="4631e-205">否</span><span class="sxs-lookup"><span data-stu-id="4631e-205">False</span></span>                                        |
| <span data-ttu-id="4631e-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4631e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="4631e-207">對</span><span class="sxs-lookup"><span data-stu-id="4631e-207">True</span></span>                                         |
| <span data-ttu-id="4631e-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4631e-208">Is Indexed</span></span>             | <span data-ttu-id="4631e-209">否</span><span class="sxs-lookup"><span data-stu-id="4631e-209">False</span></span>                                        |
| <span data-ttu-id="4631e-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4631e-210">In Global Catalog</span></span>      | <span data-ttu-id="4631e-211">否</span><span class="sxs-lookup"><span data-stu-id="4631e-211">False</span></span>                                        |
| <span data-ttu-id="4631e-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4631e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="4631e-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4631e-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4631e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4631e-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4631e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4631e-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4631e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-216">Search-Flags</span></span>           | <span data-ttu-id="4631e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4631e-217">0x00000000</span></span>                                   |
| <span data-ttu-id="4631e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-218">System-Flags</span></span>           | <span data-ttu-id="4631e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4631e-219">0x00000010</span></span>                                   |
| <span data-ttu-id="4631e-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4631e-220">Classes used in</span></span>        | [<span data-ttu-id="4631e-221">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4631e-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4631e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4631e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4631e-223">進入</span><span class="sxs-lookup"><span data-stu-id="4631e-223">Entry</span></span> | <span data-ttu-id="4631e-224">值</span><span class="sxs-lookup"><span data-stu-id="4631e-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4631e-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4631e-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4631e-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="4631e-227">System-Only</span></span>            | <span data-ttu-id="4631e-228">否</span><span class="sxs-lookup"><span data-stu-id="4631e-228">False</span></span>                                        |
| <span data-ttu-id="4631e-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4631e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="4631e-230">對</span><span class="sxs-lookup"><span data-stu-id="4631e-230">True</span></span>                                         |
| <span data-ttu-id="4631e-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4631e-231">Is Indexed</span></span>             | <span data-ttu-id="4631e-232">否</span><span class="sxs-lookup"><span data-stu-id="4631e-232">False</span></span>                                        |
| <span data-ttu-id="4631e-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4631e-233">In Global Catalog</span></span>      | <span data-ttu-id="4631e-234">否</span><span class="sxs-lookup"><span data-stu-id="4631e-234">False</span></span>                                        |
| <span data-ttu-id="4631e-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4631e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="4631e-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4631e-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4631e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4631e-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4631e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4631e-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4631e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-239">Search-Flags</span></span>           | <span data-ttu-id="4631e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4631e-240">0x00000000</span></span>                                   |
| <span data-ttu-id="4631e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-241">System-Flags</span></span>           | <span data-ttu-id="4631e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4631e-242">0x00000010</span></span>                                   |
| <span data-ttu-id="4631e-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4631e-243">Classes used in</span></span>        | [<span data-ttu-id="4631e-244">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4631e-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4631e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4631e-245">Windows Server 2012</span></span>



| <span data-ttu-id="4631e-246">進入</span><span class="sxs-lookup"><span data-stu-id="4631e-246">Entry</span></span> | <span data-ttu-id="4631e-247">值</span><span class="sxs-lookup"><span data-stu-id="4631e-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4631e-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4631e-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4631e-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4631e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="4631e-250">System-Only</span></span>            | <span data-ttu-id="4631e-251">否</span><span class="sxs-lookup"><span data-stu-id="4631e-251">False</span></span>                                        |
| <span data-ttu-id="4631e-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4631e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="4631e-253">對</span><span class="sxs-lookup"><span data-stu-id="4631e-253">True</span></span>                                         |
| <span data-ttu-id="4631e-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4631e-254">Is Indexed</span></span>             | <span data-ttu-id="4631e-255">否</span><span class="sxs-lookup"><span data-stu-id="4631e-255">False</span></span>                                        |
| <span data-ttu-id="4631e-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4631e-256">In Global Catalog</span></span>      | <span data-ttu-id="4631e-257">否</span><span class="sxs-lookup"><span data-stu-id="4631e-257">False</span></span>                                        |
| <span data-ttu-id="4631e-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4631e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="4631e-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4631e-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4631e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4631e-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4631e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4631e-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4631e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-262">Search-Flags</span></span>           | <span data-ttu-id="4631e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4631e-263">0x00000000</span></span>                                   |
| <span data-ttu-id="4631e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4631e-264">System-Flags</span></span>           | <span data-ttu-id="4631e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4631e-265">0x00000010</span></span>                                   |
| <span data-ttu-id="4631e-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4631e-266">Classes used in</span></span>        | [<span data-ttu-id="4631e-267">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="4631e-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





