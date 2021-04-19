---
title: ACS-非保留-最大 SDU 大小屬性
description: ACS-非保留-最大 SDU 大小屬性僅供內部使用。
ms.assetid: 1c65ed0e-d4ac-466d-8cb3-83db1f829535
ms.tgt_platform: multiple
keywords:
- ACS-非保留-最大 SDU 大小的屬性 AD 架構
- aCSNonReservedMaxSDUSize 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Max-SDU-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc5cac772bb94197e5492e9f45f62ec592567d9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106983322"
---
# <a name="acs-non-reserved-max-sdu-size-attribute"></a><span data-ttu-id="41741-105">ACS-非保留-最大 SDU 大小屬性</span><span class="sxs-lookup"><span data-stu-id="41741-105">ACS-Non-Reserved-Max-SDU-Size attribute</span></span>

<span data-ttu-id="41741-106">**ACS-非保留-最大 SDU 大小** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="41741-106">The **ACS-Non-Reserved-Max-SDU-Size** attribute is for internal use only.</span></span> <span data-ttu-id="41741-107">以 RFC2814 為基礎。</span><span class="sxs-lookup"><span data-stu-id="41741-107">Based on RFC2814.</span></span>



| <span data-ttu-id="41741-108">進入</span><span class="sxs-lookup"><span data-stu-id="41741-108">Entry</span></span> | <span data-ttu-id="41741-109">值</span><span class="sxs-lookup"><span data-stu-id="41741-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="41741-110">CN</span><span class="sxs-lookup"><span data-stu-id="41741-110">CN</span></span>                | <span data-ttu-id="41741-111">ACS-非保留-最大 SDU-大小</span><span class="sxs-lookup"><span data-stu-id="41741-111">ACS-Non-Reserved-Max-SDU-Size</span></span>        |
| <span data-ttu-id="41741-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="41741-112">Ldap-Display-Name</span></span> | <span data-ttu-id="41741-113">aCSNonReservedMaxSDUSize</span><span class="sxs-lookup"><span data-stu-id="41741-113">aCSNonReservedMaxSDUSize</span></span>             |
| <span data-ttu-id="41741-114">大小</span><span class="sxs-lookup"><span data-stu-id="41741-114">Size</span></span>              | <span data-ttu-id="41741-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="41741-115">8 bytes</span></span>                              |
| <span data-ttu-id="41741-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="41741-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="41741-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="41741-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="41741-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="41741-118">Attribute-Id</span></span>      | <span data-ttu-id="41741-119">1.2.840.113556.1.4.1320</span><span class="sxs-lookup"><span data-stu-id="41741-119">1.2.840.113556.1.4.1320</span></span>              |
| <span data-ttu-id="41741-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="41741-120">System-Id-Guid</span></span>    | <span data-ttu-id="41741-121">aec2cfe3-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="41741-121">aec2cfe3-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="41741-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="41741-122">Syntax</span></span>            | [<span data-ttu-id="41741-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="41741-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="41741-124">實作</span><span class="sxs-lookup"><span data-stu-id="41741-124">Implementations</span></span>

-   [<span data-ttu-id="41741-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="41741-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="41741-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="41741-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="41741-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="41741-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="41741-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="41741-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="41741-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="41741-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="41741-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="41741-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="41741-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41741-131">Windows 2000 Server</span></span>



| <span data-ttu-id="41741-132">進入</span><span class="sxs-lookup"><span data-stu-id="41741-132">Entry</span></span> | <span data-ttu-id="41741-133">值</span><span class="sxs-lookup"><span data-stu-id="41741-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="41741-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41741-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41741-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="41741-136">System-Only</span></span>            | <span data-ttu-id="41741-137">否</span><span class="sxs-lookup"><span data-stu-id="41741-137">False</span></span>                                        |
| <span data-ttu-id="41741-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41741-138">Is-Single-Valued</span></span>       | <span data-ttu-id="41741-139">對</span><span class="sxs-lookup"><span data-stu-id="41741-139">True</span></span>                                         |
| <span data-ttu-id="41741-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41741-140">Is Indexed</span></span>             | <span data-ttu-id="41741-141">否</span><span class="sxs-lookup"><span data-stu-id="41741-141">False</span></span>                                        |
| <span data-ttu-id="41741-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41741-142">In Global Catalog</span></span>      | <span data-ttu-id="41741-143">否</span><span class="sxs-lookup"><span data-stu-id="41741-143">False</span></span>                                        |
| <span data-ttu-id="41741-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41741-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="41741-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41741-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="41741-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41741-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="41741-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41741-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="41741-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-148">Search-Flags</span></span>           | <span data-ttu-id="41741-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41741-149">0x00000000</span></span>                                   |
| <span data-ttu-id="41741-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-150">System-Flags</span></span>           | <span data-ttu-id="41741-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41741-151">0x00000010</span></span>                                   |
| <span data-ttu-id="41741-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41741-152">Classes used in</span></span>        | [<span data-ttu-id="41741-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="41741-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="41741-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41741-154">Windows Server 2003</span></span>



| <span data-ttu-id="41741-155">進入</span><span class="sxs-lookup"><span data-stu-id="41741-155">Entry</span></span> | <span data-ttu-id="41741-156">值</span><span class="sxs-lookup"><span data-stu-id="41741-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="41741-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41741-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41741-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="41741-159">System-Only</span></span>            | <span data-ttu-id="41741-160">否</span><span class="sxs-lookup"><span data-stu-id="41741-160">False</span></span>                                        |
| <span data-ttu-id="41741-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41741-161">Is-Single-Valued</span></span>       | <span data-ttu-id="41741-162">對</span><span class="sxs-lookup"><span data-stu-id="41741-162">True</span></span>                                         |
| <span data-ttu-id="41741-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41741-163">Is Indexed</span></span>             | <span data-ttu-id="41741-164">否</span><span class="sxs-lookup"><span data-stu-id="41741-164">False</span></span>                                        |
| <span data-ttu-id="41741-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41741-165">In Global Catalog</span></span>      | <span data-ttu-id="41741-166">否</span><span class="sxs-lookup"><span data-stu-id="41741-166">False</span></span>                                        |
| <span data-ttu-id="41741-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41741-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="41741-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41741-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="41741-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41741-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="41741-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41741-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="41741-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-171">Search-Flags</span></span>           | <span data-ttu-id="41741-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41741-172">0x00000000</span></span>                                   |
| <span data-ttu-id="41741-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-173">System-Flags</span></span>           | <span data-ttu-id="41741-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41741-174">0x00000010</span></span>                                   |
| <span data-ttu-id="41741-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41741-175">Classes used in</span></span>        | [<span data-ttu-id="41741-176">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="41741-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="41741-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="41741-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="41741-178">進入</span><span class="sxs-lookup"><span data-stu-id="41741-178">Entry</span></span> | <span data-ttu-id="41741-179">值</span><span class="sxs-lookup"><span data-stu-id="41741-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="41741-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41741-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41741-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="41741-182">System-Only</span></span>            | <span data-ttu-id="41741-183">否</span><span class="sxs-lookup"><span data-stu-id="41741-183">False</span></span>                                        |
| <span data-ttu-id="41741-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41741-184">Is-Single-Valued</span></span>       | <span data-ttu-id="41741-185">對</span><span class="sxs-lookup"><span data-stu-id="41741-185">True</span></span>                                         |
| <span data-ttu-id="41741-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41741-186">Is Indexed</span></span>             | <span data-ttu-id="41741-187">否</span><span class="sxs-lookup"><span data-stu-id="41741-187">False</span></span>                                        |
| <span data-ttu-id="41741-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41741-188">In Global Catalog</span></span>      | <span data-ttu-id="41741-189">否</span><span class="sxs-lookup"><span data-stu-id="41741-189">False</span></span>                                        |
| <span data-ttu-id="41741-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41741-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="41741-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41741-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="41741-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41741-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="41741-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41741-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="41741-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-194">Search-Flags</span></span>           | <span data-ttu-id="41741-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41741-195">0x00000000</span></span>                                   |
| <span data-ttu-id="41741-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-196">System-Flags</span></span>           | <span data-ttu-id="41741-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41741-197">0x00000010</span></span>                                   |
| <span data-ttu-id="41741-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41741-198">Classes used in</span></span>        | [<span data-ttu-id="41741-199">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="41741-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="41741-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41741-200">Windows Server 2008</span></span>



| <span data-ttu-id="41741-201">進入</span><span class="sxs-lookup"><span data-stu-id="41741-201">Entry</span></span> | <span data-ttu-id="41741-202">值</span><span class="sxs-lookup"><span data-stu-id="41741-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="41741-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41741-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41741-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="41741-205">System-Only</span></span>            | <span data-ttu-id="41741-206">否</span><span class="sxs-lookup"><span data-stu-id="41741-206">False</span></span>                                        |
| <span data-ttu-id="41741-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41741-207">Is-Single-Valued</span></span>       | <span data-ttu-id="41741-208">對</span><span class="sxs-lookup"><span data-stu-id="41741-208">True</span></span>                                         |
| <span data-ttu-id="41741-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41741-209">Is Indexed</span></span>             | <span data-ttu-id="41741-210">否</span><span class="sxs-lookup"><span data-stu-id="41741-210">False</span></span>                                        |
| <span data-ttu-id="41741-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41741-211">In Global Catalog</span></span>      | <span data-ttu-id="41741-212">否</span><span class="sxs-lookup"><span data-stu-id="41741-212">False</span></span>                                        |
| <span data-ttu-id="41741-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41741-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="41741-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41741-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="41741-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41741-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="41741-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41741-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="41741-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-217">Search-Flags</span></span>           | <span data-ttu-id="41741-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41741-218">0x00000000</span></span>                                   |
| <span data-ttu-id="41741-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-219">System-Flags</span></span>           | <span data-ttu-id="41741-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41741-220">0x00000010</span></span>                                   |
| <span data-ttu-id="41741-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41741-221">Classes used in</span></span>        | [<span data-ttu-id="41741-222">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="41741-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="41741-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="41741-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="41741-224">進入</span><span class="sxs-lookup"><span data-stu-id="41741-224">Entry</span></span> | <span data-ttu-id="41741-225">值</span><span class="sxs-lookup"><span data-stu-id="41741-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="41741-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41741-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41741-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="41741-228">System-Only</span></span>            | <span data-ttu-id="41741-229">否</span><span class="sxs-lookup"><span data-stu-id="41741-229">False</span></span>                                        |
| <span data-ttu-id="41741-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41741-230">Is-Single-Valued</span></span>       | <span data-ttu-id="41741-231">對</span><span class="sxs-lookup"><span data-stu-id="41741-231">True</span></span>                                         |
| <span data-ttu-id="41741-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41741-232">Is Indexed</span></span>             | <span data-ttu-id="41741-233">否</span><span class="sxs-lookup"><span data-stu-id="41741-233">False</span></span>                                        |
| <span data-ttu-id="41741-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41741-234">In Global Catalog</span></span>      | <span data-ttu-id="41741-235">否</span><span class="sxs-lookup"><span data-stu-id="41741-235">False</span></span>                                        |
| <span data-ttu-id="41741-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41741-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="41741-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41741-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="41741-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41741-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="41741-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41741-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="41741-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-240">Search-Flags</span></span>           | <span data-ttu-id="41741-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41741-241">0x00000000</span></span>                                   |
| <span data-ttu-id="41741-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-242">System-Flags</span></span>           | <span data-ttu-id="41741-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41741-243">0x00000010</span></span>                                   |
| <span data-ttu-id="41741-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41741-244">Classes used in</span></span>        | [<span data-ttu-id="41741-245">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="41741-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="41741-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41741-246">Windows Server 2012</span></span>



| <span data-ttu-id="41741-247">進入</span><span class="sxs-lookup"><span data-stu-id="41741-247">Entry</span></span> | <span data-ttu-id="41741-248">值</span><span class="sxs-lookup"><span data-stu-id="41741-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="41741-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="41741-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="41741-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="41741-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="41741-251">System-Only</span></span>            | <span data-ttu-id="41741-252">否</span><span class="sxs-lookup"><span data-stu-id="41741-252">False</span></span>                                        |
| <span data-ttu-id="41741-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="41741-253">Is-Single-Valued</span></span>       | <span data-ttu-id="41741-254">對</span><span class="sxs-lookup"><span data-stu-id="41741-254">True</span></span>                                         |
| <span data-ttu-id="41741-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="41741-255">Is Indexed</span></span>             | <span data-ttu-id="41741-256">否</span><span class="sxs-lookup"><span data-stu-id="41741-256">False</span></span>                                        |
| <span data-ttu-id="41741-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="41741-257">In Global Catalog</span></span>      | <span data-ttu-id="41741-258">否</span><span class="sxs-lookup"><span data-stu-id="41741-258">False</span></span>                                        |
| <span data-ttu-id="41741-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="41741-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="41741-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="41741-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="41741-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="41741-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="41741-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="41741-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="41741-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-263">Search-Flags</span></span>           | <span data-ttu-id="41741-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41741-264">0x00000000</span></span>                                   |
| <span data-ttu-id="41741-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="41741-265">System-Flags</span></span>           | <span data-ttu-id="41741-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41741-266">0x00000010</span></span>                                   |
| <span data-ttu-id="41741-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="41741-267">Classes used in</span></span>        | [<span data-ttu-id="41741-268">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="41741-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





