---
title: ACS-非保留的尖峰率屬性
description: ACS-非保留的尖峰率屬性僅供內部使用。
ms.assetid: 4080839c-d99e-4527-8c81-6d23ab0d3d70
ms.tgt_platform: multiple
keywords:
- ACS-非保留的尖峰速率屬性 AD 架構
- aCSNonReservedPeakRate 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Peak-Rate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3d2075e90648388a9a1277dbbe768a3fc616f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107327"
---
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="0b629-105">ACS-非保留的尖峰率屬性</span><span class="sxs-lookup"><span data-stu-id="0b629-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="0b629-106">**ACS-非保留的尖峰率** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="0b629-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="0b629-107">以 RFC2814 為基礎。</span><span class="sxs-lookup"><span data-stu-id="0b629-107">Based on RFC2814.</span></span>



| <span data-ttu-id="0b629-108">進入</span><span class="sxs-lookup"><span data-stu-id="0b629-108">Entry</span></span> | <span data-ttu-id="0b629-109">值</span><span class="sxs-lookup"><span data-stu-id="0b629-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0b629-110">CN</span><span class="sxs-lookup"><span data-stu-id="0b629-110">CN</span></span>                | <span data-ttu-id="0b629-111">ACS-非保留的尖峰率</span><span class="sxs-lookup"><span data-stu-id="0b629-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="0b629-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="0b629-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0b629-113">aCSNonReservedPeakRate</span><span class="sxs-lookup"><span data-stu-id="0b629-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="0b629-114">大小</span><span class="sxs-lookup"><span data-stu-id="0b629-114">Size</span></span>              | <span data-ttu-id="0b629-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="0b629-115">8 bytes</span></span>                              |
| <span data-ttu-id="0b629-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="0b629-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0b629-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="0b629-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0b629-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b629-118">Attribute-Id</span></span>      | <span data-ttu-id="0b629-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="0b629-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="0b629-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="0b629-120">System-Id-Guid</span></span>    | <span data-ttu-id="0b629-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="0b629-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="0b629-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b629-122">Syntax</span></span>            | [<span data-ttu-id="0b629-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="0b629-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="0b629-124">實作</span><span class="sxs-lookup"><span data-stu-id="0b629-124">Implementations</span></span>

-   [<span data-ttu-id="0b629-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b629-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b629-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b629-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b629-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b629-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b629-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b629-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b629-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b629-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b629-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b629-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b629-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b629-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0b629-132">進入</span><span class="sxs-lookup"><span data-stu-id="0b629-132">Entry</span></span> | <span data-ttu-id="0b629-133">值</span><span class="sxs-lookup"><span data-stu-id="0b629-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0b629-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b629-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b629-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b629-136">System-Only</span></span>            | <span data-ttu-id="0b629-137">否</span><span class="sxs-lookup"><span data-stu-id="0b629-137">False</span></span>                                        |
| <span data-ttu-id="0b629-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b629-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0b629-139">對</span><span class="sxs-lookup"><span data-stu-id="0b629-139">True</span></span>                                         |
| <span data-ttu-id="0b629-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b629-140">Is Indexed</span></span>             | <span data-ttu-id="0b629-141">否</span><span class="sxs-lookup"><span data-stu-id="0b629-141">False</span></span>                                        |
| <span data-ttu-id="0b629-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b629-142">In Global Catalog</span></span>      | <span data-ttu-id="0b629-143">否</span><span class="sxs-lookup"><span data-stu-id="0b629-143">False</span></span>                                        |
| <span data-ttu-id="0b629-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b629-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b629-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b629-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0b629-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b629-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0b629-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b629-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0b629-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-148">Search-Flags</span></span>           | <span data-ttu-id="0b629-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b629-149">0x00000000</span></span>                                   |
| <span data-ttu-id="0b629-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-150">System-Flags</span></span>           | <span data-ttu-id="0b629-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b629-151">0x00000010</span></span>                                   |
| <span data-ttu-id="0b629-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b629-152">Classes used in</span></span>        | [<span data-ttu-id="0b629-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0b629-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b629-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b629-154">Windows Server 2003</span></span>



| <span data-ttu-id="0b629-155">進入</span><span class="sxs-lookup"><span data-stu-id="0b629-155">Entry</span></span> | <span data-ttu-id="0b629-156">值</span><span class="sxs-lookup"><span data-stu-id="0b629-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0b629-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b629-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b629-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b629-159">System-Only</span></span>            | <span data-ttu-id="0b629-160">否</span><span class="sxs-lookup"><span data-stu-id="0b629-160">False</span></span>                                        |
| <span data-ttu-id="0b629-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b629-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0b629-162">對</span><span class="sxs-lookup"><span data-stu-id="0b629-162">True</span></span>                                         |
| <span data-ttu-id="0b629-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b629-163">Is Indexed</span></span>             | <span data-ttu-id="0b629-164">否</span><span class="sxs-lookup"><span data-stu-id="0b629-164">False</span></span>                                        |
| <span data-ttu-id="0b629-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b629-165">In Global Catalog</span></span>      | <span data-ttu-id="0b629-166">否</span><span class="sxs-lookup"><span data-stu-id="0b629-166">False</span></span>                                        |
| <span data-ttu-id="0b629-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b629-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b629-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b629-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0b629-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b629-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0b629-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b629-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0b629-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-171">Search-Flags</span></span>           | <span data-ttu-id="0b629-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b629-172">0x00000000</span></span>                                   |
| <span data-ttu-id="0b629-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-173">System-Flags</span></span>           | <span data-ttu-id="0b629-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b629-174">0x00000010</span></span>                                   |
| <span data-ttu-id="0b629-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b629-175">Classes used in</span></span>        | [<span data-ttu-id="0b629-176">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0b629-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b629-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b629-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b629-178">進入</span><span class="sxs-lookup"><span data-stu-id="0b629-178">Entry</span></span> | <span data-ttu-id="0b629-179">值</span><span class="sxs-lookup"><span data-stu-id="0b629-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0b629-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b629-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b629-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b629-182">System-Only</span></span>            | <span data-ttu-id="0b629-183">否</span><span class="sxs-lookup"><span data-stu-id="0b629-183">False</span></span>                                        |
| <span data-ttu-id="0b629-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b629-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0b629-185">對</span><span class="sxs-lookup"><span data-stu-id="0b629-185">True</span></span>                                         |
| <span data-ttu-id="0b629-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b629-186">Is Indexed</span></span>             | <span data-ttu-id="0b629-187">否</span><span class="sxs-lookup"><span data-stu-id="0b629-187">False</span></span>                                        |
| <span data-ttu-id="0b629-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b629-188">In Global Catalog</span></span>      | <span data-ttu-id="0b629-189">否</span><span class="sxs-lookup"><span data-stu-id="0b629-189">False</span></span>                                        |
| <span data-ttu-id="0b629-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b629-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b629-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b629-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0b629-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b629-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0b629-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b629-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0b629-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-194">Search-Flags</span></span>           | <span data-ttu-id="0b629-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b629-195">0x00000000</span></span>                                   |
| <span data-ttu-id="0b629-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-196">System-Flags</span></span>           | <span data-ttu-id="0b629-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b629-197">0x00000010</span></span>                                   |
| <span data-ttu-id="0b629-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b629-198">Classes used in</span></span>        | [<span data-ttu-id="0b629-199">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0b629-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b629-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b629-200">Windows Server 2008</span></span>



| <span data-ttu-id="0b629-201">進入</span><span class="sxs-lookup"><span data-stu-id="0b629-201">Entry</span></span> | <span data-ttu-id="0b629-202">值</span><span class="sxs-lookup"><span data-stu-id="0b629-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0b629-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b629-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b629-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b629-205">System-Only</span></span>            | <span data-ttu-id="0b629-206">否</span><span class="sxs-lookup"><span data-stu-id="0b629-206">False</span></span>                                        |
| <span data-ttu-id="0b629-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b629-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0b629-208">對</span><span class="sxs-lookup"><span data-stu-id="0b629-208">True</span></span>                                         |
| <span data-ttu-id="0b629-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b629-209">Is Indexed</span></span>             | <span data-ttu-id="0b629-210">否</span><span class="sxs-lookup"><span data-stu-id="0b629-210">False</span></span>                                        |
| <span data-ttu-id="0b629-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b629-211">In Global Catalog</span></span>      | <span data-ttu-id="0b629-212">否</span><span class="sxs-lookup"><span data-stu-id="0b629-212">False</span></span>                                        |
| <span data-ttu-id="0b629-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b629-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b629-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b629-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0b629-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b629-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0b629-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b629-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0b629-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-217">Search-Flags</span></span>           | <span data-ttu-id="0b629-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b629-218">0x00000000</span></span>                                   |
| <span data-ttu-id="0b629-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-219">System-Flags</span></span>           | <span data-ttu-id="0b629-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b629-220">0x00000010</span></span>                                   |
| <span data-ttu-id="0b629-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b629-221">Classes used in</span></span>        | [<span data-ttu-id="0b629-222">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0b629-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b629-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b629-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b629-224">進入</span><span class="sxs-lookup"><span data-stu-id="0b629-224">Entry</span></span> | <span data-ttu-id="0b629-225">值</span><span class="sxs-lookup"><span data-stu-id="0b629-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0b629-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b629-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b629-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b629-228">System-Only</span></span>            | <span data-ttu-id="0b629-229">否</span><span class="sxs-lookup"><span data-stu-id="0b629-229">False</span></span>                                        |
| <span data-ttu-id="0b629-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b629-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0b629-231">對</span><span class="sxs-lookup"><span data-stu-id="0b629-231">True</span></span>                                         |
| <span data-ttu-id="0b629-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b629-232">Is Indexed</span></span>             | <span data-ttu-id="0b629-233">否</span><span class="sxs-lookup"><span data-stu-id="0b629-233">False</span></span>                                        |
| <span data-ttu-id="0b629-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b629-234">In Global Catalog</span></span>      | <span data-ttu-id="0b629-235">否</span><span class="sxs-lookup"><span data-stu-id="0b629-235">False</span></span>                                        |
| <span data-ttu-id="0b629-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b629-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b629-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b629-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0b629-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b629-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0b629-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b629-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0b629-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-240">Search-Flags</span></span>           | <span data-ttu-id="0b629-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b629-241">0x00000000</span></span>                                   |
| <span data-ttu-id="0b629-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-242">System-Flags</span></span>           | <span data-ttu-id="0b629-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b629-243">0x00000010</span></span>                                   |
| <span data-ttu-id="0b629-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b629-244">Classes used in</span></span>        | [<span data-ttu-id="0b629-245">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0b629-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b629-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b629-246">Windows Server 2012</span></span>



| <span data-ttu-id="0b629-247">進入</span><span class="sxs-lookup"><span data-stu-id="0b629-247">Entry</span></span> | <span data-ttu-id="0b629-248">值</span><span class="sxs-lookup"><span data-stu-id="0b629-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0b629-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="0b629-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b629-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0b629-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b629-251">System-Only</span></span>            | <span data-ttu-id="0b629-252">否</span><span class="sxs-lookup"><span data-stu-id="0b629-252">False</span></span>                                        |
| <span data-ttu-id="0b629-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="0b629-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0b629-254">對</span><span class="sxs-lookup"><span data-stu-id="0b629-254">True</span></span>                                         |
| <span data-ttu-id="0b629-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="0b629-255">Is Indexed</span></span>             | <span data-ttu-id="0b629-256">否</span><span class="sxs-lookup"><span data-stu-id="0b629-256">False</span></span>                                        |
| <span data-ttu-id="0b629-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="0b629-257">In Global Catalog</span></span>      | <span data-ttu-id="0b629-258">否</span><span class="sxs-lookup"><span data-stu-id="0b629-258">False</span></span>                                        |
| <span data-ttu-id="0b629-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="0b629-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b629-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="0b629-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0b629-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b629-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0b629-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b629-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0b629-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-263">Search-Flags</span></span>           | <span data-ttu-id="0b629-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b629-264">0x00000000</span></span>                                   |
| <span data-ttu-id="0b629-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b629-265">System-Flags</span></span>           | <span data-ttu-id="0b629-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b629-266">0x00000010</span></span>                                   |
| <span data-ttu-id="0b629-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="0b629-267">Classes used in</span></span>        | [<span data-ttu-id="0b629-268">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="0b629-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





