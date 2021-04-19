---
title: ACS-非保留-最小-Policed-大小屬性
description: ACS-非保留-最小 Policed 大小屬性僅供內部使用。
ms.assetid: f5ee29ec-d2a9-4026-a4d1-0484d353efdc
ms.tgt_platform: multiple
keywords:
- ACS-非保留-最小-Policed-大小的屬性 AD 架構
- aCSNonReservedMinPolicedSize 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Min-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9fa7794343929aa0f7d7d86f4fc1f1e9a8a5b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973120"
---
# <a name="acs-non-reserved-min-policed-size-attribute"></a><span data-ttu-id="670f7-105">ACS-非保留-最小-Policed-大小屬性</span><span class="sxs-lookup"><span data-stu-id="670f7-105">ACS-Non-Reserved-Min-Policed-Size attribute</span></span>

<span data-ttu-id="670f7-106">**ACS-非保留-最小 Policed 大小** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="670f7-106">The **ACS-Non-Reserved-Min-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="670f7-107">以 RFC2814 為基礎。</span><span class="sxs-lookup"><span data-stu-id="670f7-107">Based on RFC2814.</span></span>



| <span data-ttu-id="670f7-108">進入</span><span class="sxs-lookup"><span data-stu-id="670f7-108">Entry</span></span> | <span data-ttu-id="670f7-109">值</span><span class="sxs-lookup"><span data-stu-id="670f7-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="670f7-110">CN</span><span class="sxs-lookup"><span data-stu-id="670f7-110">CN</span></span>                | <span data-ttu-id="670f7-111">ACS-非保留-最小-Policed-大小</span><span class="sxs-lookup"><span data-stu-id="670f7-111">ACS-Non-Reserved-Min-Policed-Size</span></span>    |
| <span data-ttu-id="670f7-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="670f7-112">Ldap-Display-Name</span></span> | <span data-ttu-id="670f7-113">aCSNonReservedMinPolicedSize</span><span class="sxs-lookup"><span data-stu-id="670f7-113">aCSNonReservedMinPolicedSize</span></span>         |
| <span data-ttu-id="670f7-114">大小</span><span class="sxs-lookup"><span data-stu-id="670f7-114">Size</span></span>              | <span data-ttu-id="670f7-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="670f7-115">8 bytes</span></span>                              |
| <span data-ttu-id="670f7-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="670f7-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="670f7-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="670f7-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="670f7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="670f7-118">Attribute-Id</span></span>      | <span data-ttu-id="670f7-119">1.2.840.113556.1.4.1321</span><span class="sxs-lookup"><span data-stu-id="670f7-119">1.2.840.113556.1.4.1321</span></span>              |
| <span data-ttu-id="670f7-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="670f7-120">System-Id-Guid</span></span>    | <span data-ttu-id="670f7-121">b6873917-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="670f7-121">b6873917-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="670f7-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="670f7-122">Syntax</span></span>            | [<span data-ttu-id="670f7-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="670f7-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="670f7-124">實作</span><span class="sxs-lookup"><span data-stu-id="670f7-124">Implementations</span></span>

-   [<span data-ttu-id="670f7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="670f7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="670f7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="670f7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="670f7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="670f7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="670f7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="670f7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="670f7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="670f7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="670f7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="670f7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="670f7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="670f7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="670f7-132">進入</span><span class="sxs-lookup"><span data-stu-id="670f7-132">Entry</span></span> | <span data-ttu-id="670f7-133">值</span><span class="sxs-lookup"><span data-stu-id="670f7-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="670f7-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="670f7-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="670f7-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="670f7-136">System-Only</span></span>            | <span data-ttu-id="670f7-137">否</span><span class="sxs-lookup"><span data-stu-id="670f7-137">False</span></span>                                        |
| <span data-ttu-id="670f7-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="670f7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="670f7-139">對</span><span class="sxs-lookup"><span data-stu-id="670f7-139">True</span></span>                                         |
| <span data-ttu-id="670f7-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="670f7-140">Is Indexed</span></span>             | <span data-ttu-id="670f7-141">否</span><span class="sxs-lookup"><span data-stu-id="670f7-141">False</span></span>                                        |
| <span data-ttu-id="670f7-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="670f7-142">In Global Catalog</span></span>      | <span data-ttu-id="670f7-143">否</span><span class="sxs-lookup"><span data-stu-id="670f7-143">False</span></span>                                        |
| <span data-ttu-id="670f7-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="670f7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="670f7-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="670f7-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="670f7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="670f7-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="670f7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="670f7-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="670f7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-148">Search-Flags</span></span>           | <span data-ttu-id="670f7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="670f7-149">0x00000000</span></span>                                   |
| <span data-ttu-id="670f7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-150">System-Flags</span></span>           | <span data-ttu-id="670f7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="670f7-151">0x00000010</span></span>                                   |
| <span data-ttu-id="670f7-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="670f7-152">Classes used in</span></span>        | [<span data-ttu-id="670f7-153">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="670f7-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="670f7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="670f7-154">Windows Server 2003</span></span>



| <span data-ttu-id="670f7-155">進入</span><span class="sxs-lookup"><span data-stu-id="670f7-155">Entry</span></span> | <span data-ttu-id="670f7-156">值</span><span class="sxs-lookup"><span data-stu-id="670f7-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="670f7-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="670f7-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="670f7-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="670f7-159">System-Only</span></span>            | <span data-ttu-id="670f7-160">否</span><span class="sxs-lookup"><span data-stu-id="670f7-160">False</span></span>                                        |
| <span data-ttu-id="670f7-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="670f7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="670f7-162">對</span><span class="sxs-lookup"><span data-stu-id="670f7-162">True</span></span>                                         |
| <span data-ttu-id="670f7-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="670f7-163">Is Indexed</span></span>             | <span data-ttu-id="670f7-164">否</span><span class="sxs-lookup"><span data-stu-id="670f7-164">False</span></span>                                        |
| <span data-ttu-id="670f7-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="670f7-165">In Global Catalog</span></span>      | <span data-ttu-id="670f7-166">否</span><span class="sxs-lookup"><span data-stu-id="670f7-166">False</span></span>                                        |
| <span data-ttu-id="670f7-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="670f7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="670f7-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="670f7-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="670f7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="670f7-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="670f7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="670f7-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="670f7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-171">Search-Flags</span></span>           | <span data-ttu-id="670f7-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="670f7-172">0x00000000</span></span>                                   |
| <span data-ttu-id="670f7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-173">System-Flags</span></span>           | <span data-ttu-id="670f7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="670f7-174">0x00000010</span></span>                                   |
| <span data-ttu-id="670f7-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="670f7-175">Classes used in</span></span>        | [<span data-ttu-id="670f7-176">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="670f7-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="670f7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="670f7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="670f7-178">進入</span><span class="sxs-lookup"><span data-stu-id="670f7-178">Entry</span></span> | <span data-ttu-id="670f7-179">值</span><span class="sxs-lookup"><span data-stu-id="670f7-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="670f7-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="670f7-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="670f7-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="670f7-182">System-Only</span></span>            | <span data-ttu-id="670f7-183">否</span><span class="sxs-lookup"><span data-stu-id="670f7-183">False</span></span>                                        |
| <span data-ttu-id="670f7-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="670f7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="670f7-185">對</span><span class="sxs-lookup"><span data-stu-id="670f7-185">True</span></span>                                         |
| <span data-ttu-id="670f7-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="670f7-186">Is Indexed</span></span>             | <span data-ttu-id="670f7-187">否</span><span class="sxs-lookup"><span data-stu-id="670f7-187">False</span></span>                                        |
| <span data-ttu-id="670f7-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="670f7-188">In Global Catalog</span></span>      | <span data-ttu-id="670f7-189">否</span><span class="sxs-lookup"><span data-stu-id="670f7-189">False</span></span>                                        |
| <span data-ttu-id="670f7-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="670f7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="670f7-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="670f7-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="670f7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="670f7-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="670f7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="670f7-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="670f7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-194">Search-Flags</span></span>           | <span data-ttu-id="670f7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="670f7-195">0x00000000</span></span>                                   |
| <span data-ttu-id="670f7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-196">System-Flags</span></span>           | <span data-ttu-id="670f7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="670f7-197">0x00000010</span></span>                                   |
| <span data-ttu-id="670f7-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="670f7-198">Classes used in</span></span>        | [<span data-ttu-id="670f7-199">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="670f7-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="670f7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="670f7-200">Windows Server 2008</span></span>



| <span data-ttu-id="670f7-201">進入</span><span class="sxs-lookup"><span data-stu-id="670f7-201">Entry</span></span> | <span data-ttu-id="670f7-202">值</span><span class="sxs-lookup"><span data-stu-id="670f7-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="670f7-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="670f7-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="670f7-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="670f7-205">System-Only</span></span>            | <span data-ttu-id="670f7-206">否</span><span class="sxs-lookup"><span data-stu-id="670f7-206">False</span></span>                                        |
| <span data-ttu-id="670f7-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="670f7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="670f7-208">對</span><span class="sxs-lookup"><span data-stu-id="670f7-208">True</span></span>                                         |
| <span data-ttu-id="670f7-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="670f7-209">Is Indexed</span></span>             | <span data-ttu-id="670f7-210">否</span><span class="sxs-lookup"><span data-stu-id="670f7-210">False</span></span>                                        |
| <span data-ttu-id="670f7-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="670f7-211">In Global Catalog</span></span>      | <span data-ttu-id="670f7-212">否</span><span class="sxs-lookup"><span data-stu-id="670f7-212">False</span></span>                                        |
| <span data-ttu-id="670f7-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="670f7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="670f7-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="670f7-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="670f7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="670f7-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="670f7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="670f7-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="670f7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-217">Search-Flags</span></span>           | <span data-ttu-id="670f7-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="670f7-218">0x00000000</span></span>                                   |
| <span data-ttu-id="670f7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-219">System-Flags</span></span>           | <span data-ttu-id="670f7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="670f7-220">0x00000010</span></span>                                   |
| <span data-ttu-id="670f7-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="670f7-221">Classes used in</span></span>        | [<span data-ttu-id="670f7-222">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="670f7-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="670f7-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="670f7-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="670f7-224">進入</span><span class="sxs-lookup"><span data-stu-id="670f7-224">Entry</span></span> | <span data-ttu-id="670f7-225">值</span><span class="sxs-lookup"><span data-stu-id="670f7-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="670f7-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="670f7-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="670f7-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="670f7-228">System-Only</span></span>            | <span data-ttu-id="670f7-229">否</span><span class="sxs-lookup"><span data-stu-id="670f7-229">False</span></span>                                        |
| <span data-ttu-id="670f7-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="670f7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="670f7-231">對</span><span class="sxs-lookup"><span data-stu-id="670f7-231">True</span></span>                                         |
| <span data-ttu-id="670f7-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="670f7-232">Is Indexed</span></span>             | <span data-ttu-id="670f7-233">否</span><span class="sxs-lookup"><span data-stu-id="670f7-233">False</span></span>                                        |
| <span data-ttu-id="670f7-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="670f7-234">In Global Catalog</span></span>      | <span data-ttu-id="670f7-235">否</span><span class="sxs-lookup"><span data-stu-id="670f7-235">False</span></span>                                        |
| <span data-ttu-id="670f7-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="670f7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="670f7-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="670f7-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="670f7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="670f7-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="670f7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="670f7-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="670f7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-240">Search-Flags</span></span>           | <span data-ttu-id="670f7-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="670f7-241">0x00000000</span></span>                                   |
| <span data-ttu-id="670f7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-242">System-Flags</span></span>           | <span data-ttu-id="670f7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="670f7-243">0x00000010</span></span>                                   |
| <span data-ttu-id="670f7-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="670f7-244">Classes used in</span></span>        | [<span data-ttu-id="670f7-245">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="670f7-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="670f7-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="670f7-246">Windows Server 2012</span></span>



| <span data-ttu-id="670f7-247">進入</span><span class="sxs-lookup"><span data-stu-id="670f7-247">Entry</span></span> | <span data-ttu-id="670f7-248">值</span><span class="sxs-lookup"><span data-stu-id="670f7-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="670f7-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="670f7-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="670f7-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="670f7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="670f7-251">System-Only</span></span>            | <span data-ttu-id="670f7-252">否</span><span class="sxs-lookup"><span data-stu-id="670f7-252">False</span></span>                                        |
| <span data-ttu-id="670f7-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="670f7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="670f7-254">對</span><span class="sxs-lookup"><span data-stu-id="670f7-254">True</span></span>                                         |
| <span data-ttu-id="670f7-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="670f7-255">Is Indexed</span></span>             | <span data-ttu-id="670f7-256">否</span><span class="sxs-lookup"><span data-stu-id="670f7-256">False</span></span>                                        |
| <span data-ttu-id="670f7-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="670f7-257">In Global Catalog</span></span>      | <span data-ttu-id="670f7-258">否</span><span class="sxs-lookup"><span data-stu-id="670f7-258">False</span></span>                                        |
| <span data-ttu-id="670f7-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="670f7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="670f7-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="670f7-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="670f7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="670f7-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="670f7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="670f7-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="670f7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-263">Search-Flags</span></span>           | <span data-ttu-id="670f7-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="670f7-264">0x00000000</span></span>                                   |
| <span data-ttu-id="670f7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="670f7-265">System-Flags</span></span>           | <span data-ttu-id="670f7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="670f7-266">0x00000010</span></span>                                   |
| <span data-ttu-id="670f7-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="670f7-267">Classes used in</span></span>        | [<span data-ttu-id="670f7-268">**ACS-子網**</span><span class="sxs-lookup"><span data-stu-id="670f7-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





