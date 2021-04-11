---
title: ACS-非保留-Token 大小屬性
description: ACS 非保留的 Token 大小屬性僅供內部使用。
ms.assetid: 50c11f5f-2188-43ab-9d40-094ca8a3d526
ms.tgt_platform: multiple
keywords:
- ACS-非保留-權杖大小的屬性 AD 架構
- aCSNonReservedTokenSize 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Token-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90351a660cfbeafbcd468edb1e6eca8c589b5d72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108308"
---
# <a name="acs-non-reserved-token-size-attribute"></a><span data-ttu-id="5f382-105">ACS-非保留-Token 大小屬性</span><span class="sxs-lookup"><span data-stu-id="5f382-105">ACS-Non-Reserved-Token-Size attribute</span></span>

<span data-ttu-id="5f382-106">**ACS 非保留的 Token 大小** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="5f382-106">The **ACS-Non-Reserved-Token-Size** attribute is for internal use only.</span></span> <span data-ttu-id="5f382-107">以 RFC2814 為基礎。</span><span class="sxs-lookup"><span data-stu-id="5f382-107">Based on RFC2814.</span></span>



| <span data-ttu-id="5f382-108">進入</span><span class="sxs-lookup"><span data-stu-id="5f382-108">Entry</span></span> | <span data-ttu-id="5f382-109">值</span><span class="sxs-lookup"><span data-stu-id="5f382-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5f382-110">CN</span><span class="sxs-lookup"><span data-stu-id="5f382-110">CN</span></span>                | <span data-ttu-id="5f382-111">ACS-非保留-權杖-大小</span><span class="sxs-lookup"><span data-stu-id="5f382-111">ACS-Non-Reserved-Token-Size</span></span>          |
| <span data-ttu-id="5f382-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5f382-112">Ldap-Display-Name</span></span> | <span data-ttu-id="5f382-113">aCSNonReservedTokenSize</span><span class="sxs-lookup"><span data-stu-id="5f382-113">aCSNonReservedTokenSize</span></span>              |
| <span data-ttu-id="5f382-114">大小</span><span class="sxs-lookup"><span data-stu-id="5f382-114">Size</span></span>              | <span data-ttu-id="5f382-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="5f382-115">8 bytes</span></span>                              |
| <span data-ttu-id="5f382-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5f382-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5f382-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5f382-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5f382-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5f382-118">Attribute-Id</span></span>      | <span data-ttu-id="5f382-119">1.2.840.113556.1.4.1319</span><span class="sxs-lookup"><span data-stu-id="5f382-119">1.2.840.113556.1.4.1319</span></span>              |
| <span data-ttu-id="5f382-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5f382-120">System-Id-Guid</span></span>    | <span data-ttu-id="5f382-121">a916d7c9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="5f382-121">a916d7c9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="5f382-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f382-122">Syntax</span></span>            | [<span data-ttu-id="5f382-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="5f382-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5f382-124">實作</span><span class="sxs-lookup"><span data-stu-id="5f382-124">Implementations</span></span>

-   [<span data-ttu-id="5f382-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5f382-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5f382-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5f382-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5f382-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5f382-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5f382-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5f382-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5f382-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5f382-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5f382-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5f382-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5f382-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f382-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5f382-132">進入</span><span class="sxs-lookup"><span data-stu-id="5f382-132">Entry</span></span> | <span data-ttu-id="5f382-133">值</span><span class="sxs-lookup"><span data-stu-id="5f382-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f382-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5f382-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f382-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f382-136">System-Only</span></span>            | <span data-ttu-id="5f382-137">否</span><span class="sxs-lookup"><span data-stu-id="5f382-137">False</span></span>                                        |
| <span data-ttu-id="5f382-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5f382-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5f382-139">對</span><span class="sxs-lookup"><span data-stu-id="5f382-139">True</span></span>                                         |
| <span data-ttu-id="5f382-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5f382-140">Is Indexed</span></span>             | <span data-ttu-id="5f382-141">否</span><span class="sxs-lookup"><span data-stu-id="5f382-141">False</span></span>                                        |
| <span data-ttu-id="5f382-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5f382-142">In Global Catalog</span></span>      | <span data-ttu-id="5f382-143">否</span><span class="sxs-lookup"><span data-stu-id="5f382-143">False</span></span>                                        |
| <span data-ttu-id="5f382-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5f382-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f382-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5f382-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f382-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f382-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f382-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f382-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f382-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-148">Search-Flags</span></span>           | <span data-ttu-id="5f382-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f382-149">0x00000000</span></span>                                   |
| <span data-ttu-id="5f382-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-150">System-Flags</span></span>           | <span data-ttu-id="5f382-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f382-151">0x00000010</span></span>                                   |
| <span data-ttu-id="5f382-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5f382-152">Classes used in</span></span>        | [<span data-ttu-id="5f382-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="5f382-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5f382-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f382-154">Windows Server 2003</span></span>



| <span data-ttu-id="5f382-155">進入</span><span class="sxs-lookup"><span data-stu-id="5f382-155">Entry</span></span> | <span data-ttu-id="5f382-156">值</span><span class="sxs-lookup"><span data-stu-id="5f382-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f382-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5f382-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f382-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f382-159">System-Only</span></span>            | <span data-ttu-id="5f382-160">否</span><span class="sxs-lookup"><span data-stu-id="5f382-160">False</span></span>                                        |
| <span data-ttu-id="5f382-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5f382-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5f382-162">對</span><span class="sxs-lookup"><span data-stu-id="5f382-162">True</span></span>                                         |
| <span data-ttu-id="5f382-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5f382-163">Is Indexed</span></span>             | <span data-ttu-id="5f382-164">否</span><span class="sxs-lookup"><span data-stu-id="5f382-164">False</span></span>                                        |
| <span data-ttu-id="5f382-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5f382-165">In Global Catalog</span></span>      | <span data-ttu-id="5f382-166">否</span><span class="sxs-lookup"><span data-stu-id="5f382-166">False</span></span>                                        |
| <span data-ttu-id="5f382-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5f382-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f382-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5f382-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f382-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f382-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f382-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f382-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f382-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-171">Search-Flags</span></span>           | <span data-ttu-id="5f382-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f382-172">0x00000000</span></span>                                   |
| <span data-ttu-id="5f382-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-173">System-Flags</span></span>           | <span data-ttu-id="5f382-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f382-174">0x00000010</span></span>                                   |
| <span data-ttu-id="5f382-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5f382-175">Classes used in</span></span>        | [<span data-ttu-id="5f382-176">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="5f382-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5f382-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5f382-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5f382-178">進入</span><span class="sxs-lookup"><span data-stu-id="5f382-178">Entry</span></span> | <span data-ttu-id="5f382-179">值</span><span class="sxs-lookup"><span data-stu-id="5f382-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f382-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5f382-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f382-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f382-182">System-Only</span></span>            | <span data-ttu-id="5f382-183">否</span><span class="sxs-lookup"><span data-stu-id="5f382-183">False</span></span>                                        |
| <span data-ttu-id="5f382-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5f382-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5f382-185">對</span><span class="sxs-lookup"><span data-stu-id="5f382-185">True</span></span>                                         |
| <span data-ttu-id="5f382-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5f382-186">Is Indexed</span></span>             | <span data-ttu-id="5f382-187">否</span><span class="sxs-lookup"><span data-stu-id="5f382-187">False</span></span>                                        |
| <span data-ttu-id="5f382-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5f382-188">In Global Catalog</span></span>      | <span data-ttu-id="5f382-189">否</span><span class="sxs-lookup"><span data-stu-id="5f382-189">False</span></span>                                        |
| <span data-ttu-id="5f382-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5f382-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f382-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5f382-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f382-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f382-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f382-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f382-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f382-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-194">Search-Flags</span></span>           | <span data-ttu-id="5f382-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f382-195">0x00000000</span></span>                                   |
| <span data-ttu-id="5f382-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-196">System-Flags</span></span>           | <span data-ttu-id="5f382-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f382-197">0x00000010</span></span>                                   |
| <span data-ttu-id="5f382-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5f382-198">Classes used in</span></span>        | [<span data-ttu-id="5f382-199">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="5f382-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5f382-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f382-200">Windows Server 2008</span></span>



| <span data-ttu-id="5f382-201">進入</span><span class="sxs-lookup"><span data-stu-id="5f382-201">Entry</span></span> | <span data-ttu-id="5f382-202">值</span><span class="sxs-lookup"><span data-stu-id="5f382-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f382-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5f382-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f382-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f382-205">System-Only</span></span>            | <span data-ttu-id="5f382-206">否</span><span class="sxs-lookup"><span data-stu-id="5f382-206">False</span></span>                                        |
| <span data-ttu-id="5f382-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5f382-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5f382-208">對</span><span class="sxs-lookup"><span data-stu-id="5f382-208">True</span></span>                                         |
| <span data-ttu-id="5f382-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5f382-209">Is Indexed</span></span>             | <span data-ttu-id="5f382-210">否</span><span class="sxs-lookup"><span data-stu-id="5f382-210">False</span></span>                                        |
| <span data-ttu-id="5f382-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5f382-211">In Global Catalog</span></span>      | <span data-ttu-id="5f382-212">否</span><span class="sxs-lookup"><span data-stu-id="5f382-212">False</span></span>                                        |
| <span data-ttu-id="5f382-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5f382-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f382-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5f382-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f382-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f382-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f382-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f382-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f382-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-217">Search-Flags</span></span>           | <span data-ttu-id="5f382-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f382-218">0x00000000</span></span>                                   |
| <span data-ttu-id="5f382-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-219">System-Flags</span></span>           | <span data-ttu-id="5f382-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f382-220">0x00000010</span></span>                                   |
| <span data-ttu-id="5f382-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5f382-221">Classes used in</span></span>        | [<span data-ttu-id="5f382-222">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="5f382-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5f382-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f382-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5f382-224">進入</span><span class="sxs-lookup"><span data-stu-id="5f382-224">Entry</span></span> | <span data-ttu-id="5f382-225">值</span><span class="sxs-lookup"><span data-stu-id="5f382-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f382-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5f382-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f382-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f382-228">System-Only</span></span>            | <span data-ttu-id="5f382-229">否</span><span class="sxs-lookup"><span data-stu-id="5f382-229">False</span></span>                                        |
| <span data-ttu-id="5f382-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5f382-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5f382-231">對</span><span class="sxs-lookup"><span data-stu-id="5f382-231">True</span></span>                                         |
| <span data-ttu-id="5f382-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5f382-232">Is Indexed</span></span>             | <span data-ttu-id="5f382-233">否</span><span class="sxs-lookup"><span data-stu-id="5f382-233">False</span></span>                                        |
| <span data-ttu-id="5f382-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5f382-234">In Global Catalog</span></span>      | <span data-ttu-id="5f382-235">否</span><span class="sxs-lookup"><span data-stu-id="5f382-235">False</span></span>                                        |
| <span data-ttu-id="5f382-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5f382-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f382-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5f382-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f382-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f382-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f382-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f382-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f382-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-240">Search-Flags</span></span>           | <span data-ttu-id="5f382-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f382-241">0x00000000</span></span>                                   |
| <span data-ttu-id="5f382-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-242">System-Flags</span></span>           | <span data-ttu-id="5f382-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f382-243">0x00000010</span></span>                                   |
| <span data-ttu-id="5f382-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5f382-244">Classes used in</span></span>        | [<span data-ttu-id="5f382-245">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="5f382-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5f382-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f382-246">Windows Server 2012</span></span>



| <span data-ttu-id="5f382-247">進入</span><span class="sxs-lookup"><span data-stu-id="5f382-247">Entry</span></span> | <span data-ttu-id="5f382-248">值</span><span class="sxs-lookup"><span data-stu-id="5f382-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f382-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5f382-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f382-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f382-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f382-251">System-Only</span></span>            | <span data-ttu-id="5f382-252">否</span><span class="sxs-lookup"><span data-stu-id="5f382-252">False</span></span>                                        |
| <span data-ttu-id="5f382-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5f382-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5f382-254">對</span><span class="sxs-lookup"><span data-stu-id="5f382-254">True</span></span>                                         |
| <span data-ttu-id="5f382-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5f382-255">Is Indexed</span></span>             | <span data-ttu-id="5f382-256">否</span><span class="sxs-lookup"><span data-stu-id="5f382-256">False</span></span>                                        |
| <span data-ttu-id="5f382-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5f382-257">In Global Catalog</span></span>      | <span data-ttu-id="5f382-258">否</span><span class="sxs-lookup"><span data-stu-id="5f382-258">False</span></span>                                        |
| <span data-ttu-id="5f382-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5f382-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f382-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5f382-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f382-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f382-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f382-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f382-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f382-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-263">Search-Flags</span></span>           | <span data-ttu-id="5f382-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f382-264">0x00000000</span></span>                                   |
| <span data-ttu-id="5f382-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f382-265">System-Flags</span></span>           | <span data-ttu-id="5f382-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f382-266">0x00000010</span></span>                                   |
| <span data-ttu-id="5f382-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5f382-267">Classes used in</span></span>        | [<span data-ttu-id="5f382-268">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="5f382-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





