---
title: ACS-許可權-Bits 屬性
description: 允許指定使用者的多播流程來源。
ms.assetid: c7e7866d-b906-4a64-bd51-4e9cc7b8fb86
ms.tgt_platform: multiple
keywords:
- ACS-許可權-Bits 屬性 AD 架構
- aCSPermissionBits 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Permission-Bits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a27370178dd46fd50df44b1226686db5a70a846
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107322"
---
# <a name="acs-permission-bits-attribute"></a><span data-ttu-id="77c01-105">ACS-許可權-Bits 屬性</span><span class="sxs-lookup"><span data-stu-id="77c01-105">ACS-Permission-Bits attribute</span></span>

<span data-ttu-id="77c01-106">允許指定使用者的多播流程來源。</span><span class="sxs-lookup"><span data-stu-id="77c01-106">Allows multicast flow origination for a given user.</span></span>



| <span data-ttu-id="77c01-107">進入</span><span class="sxs-lookup"><span data-stu-id="77c01-107">Entry</span></span> | <span data-ttu-id="77c01-108">值</span><span class="sxs-lookup"><span data-stu-id="77c01-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="77c01-109">CN</span><span class="sxs-lookup"><span data-stu-id="77c01-109">CN</span></span>                | <span data-ttu-id="77c01-110">ACS-許可權位</span><span class="sxs-lookup"><span data-stu-id="77c01-110">ACS-Permission-Bits</span></span>                  |
| <span data-ttu-id="77c01-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="77c01-111">Ldap-Display-Name</span></span> | <span data-ttu-id="77c01-112">aCSPermissionBits</span><span class="sxs-lookup"><span data-stu-id="77c01-112">aCSPermissionBits</span></span>                    |
| <span data-ttu-id="77c01-113">大小</span><span class="sxs-lookup"><span data-stu-id="77c01-113">Size</span></span>              | <span data-ttu-id="77c01-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="77c01-114">8 bytes</span></span>                              |
| <span data-ttu-id="77c01-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="77c01-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="77c01-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="77c01-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="77c01-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="77c01-117">Attribute-Id</span></span>      | <span data-ttu-id="77c01-118">1.2.840.113556.1.4.765</span><span class="sxs-lookup"><span data-stu-id="77c01-118">1.2.840.113556.1.4.765</span></span>               |
| <span data-ttu-id="77c01-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="77c01-119">System-Id-Guid</span></span>    | <span data-ttu-id="77c01-120">7f561282-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="77c01-120">7f561282-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="77c01-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="77c01-121">Syntax</span></span>            | [<span data-ttu-id="77c01-122">**間隔**</span><span class="sxs-lookup"><span data-stu-id="77c01-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="77c01-123">實作</span><span class="sxs-lookup"><span data-stu-id="77c01-123">Implementations</span></span>

-   [<span data-ttu-id="77c01-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="77c01-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="77c01-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="77c01-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="77c01-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="77c01-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="77c01-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="77c01-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="77c01-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="77c01-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="77c01-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="77c01-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="77c01-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77c01-130">Windows 2000 Server</span></span>



| <span data-ttu-id="77c01-131">進入</span><span class="sxs-lookup"><span data-stu-id="77c01-131">Entry</span></span> | <span data-ttu-id="77c01-132">值</span><span class="sxs-lookup"><span data-stu-id="77c01-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77c01-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77c01-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77c01-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="77c01-135">System-Only</span></span>            | <span data-ttu-id="77c01-136">否</span><span class="sxs-lookup"><span data-stu-id="77c01-136">False</span></span>                                        |
| <span data-ttu-id="77c01-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77c01-137">Is-Single-Valued</span></span>       | <span data-ttu-id="77c01-138">對</span><span class="sxs-lookup"><span data-stu-id="77c01-138">True</span></span>                                         |
| <span data-ttu-id="77c01-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77c01-139">Is Indexed</span></span>             | <span data-ttu-id="77c01-140">否</span><span class="sxs-lookup"><span data-stu-id="77c01-140">False</span></span>                                        |
| <span data-ttu-id="77c01-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77c01-141">In Global Catalog</span></span>      | <span data-ttu-id="77c01-142">否</span><span class="sxs-lookup"><span data-stu-id="77c01-142">False</span></span>                                        |
| <span data-ttu-id="77c01-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77c01-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="77c01-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77c01-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77c01-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77c01-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77c01-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77c01-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77c01-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-147">Search-Flags</span></span>           | <span data-ttu-id="77c01-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77c01-148">0x00000000</span></span>                                   |
| <span data-ttu-id="77c01-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-149">System-Flags</span></span>           | <span data-ttu-id="77c01-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77c01-150">0x00000010</span></span>                                   |
| <span data-ttu-id="77c01-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77c01-151">Classes used in</span></span>        | [<span data-ttu-id="77c01-152">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="77c01-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="77c01-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77c01-153">Windows Server 2003</span></span>



| <span data-ttu-id="77c01-154">進入</span><span class="sxs-lookup"><span data-stu-id="77c01-154">Entry</span></span> | <span data-ttu-id="77c01-155">值</span><span class="sxs-lookup"><span data-stu-id="77c01-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77c01-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77c01-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77c01-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="77c01-158">System-Only</span></span>            | <span data-ttu-id="77c01-159">否</span><span class="sxs-lookup"><span data-stu-id="77c01-159">False</span></span>                                        |
| <span data-ttu-id="77c01-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77c01-160">Is-Single-Valued</span></span>       | <span data-ttu-id="77c01-161">對</span><span class="sxs-lookup"><span data-stu-id="77c01-161">True</span></span>                                         |
| <span data-ttu-id="77c01-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77c01-162">Is Indexed</span></span>             | <span data-ttu-id="77c01-163">否</span><span class="sxs-lookup"><span data-stu-id="77c01-163">False</span></span>                                        |
| <span data-ttu-id="77c01-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77c01-164">In Global Catalog</span></span>      | <span data-ttu-id="77c01-165">否</span><span class="sxs-lookup"><span data-stu-id="77c01-165">False</span></span>                                        |
| <span data-ttu-id="77c01-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77c01-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="77c01-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77c01-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77c01-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77c01-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77c01-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77c01-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77c01-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-170">Search-Flags</span></span>           | <span data-ttu-id="77c01-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77c01-171">0x00000000</span></span>                                   |
| <span data-ttu-id="77c01-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-172">System-Flags</span></span>           | <span data-ttu-id="77c01-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77c01-173">0x00000010</span></span>                                   |
| <span data-ttu-id="77c01-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77c01-174">Classes used in</span></span>        | [<span data-ttu-id="77c01-175">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="77c01-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="77c01-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="77c01-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="77c01-177">進入</span><span class="sxs-lookup"><span data-stu-id="77c01-177">Entry</span></span> | <span data-ttu-id="77c01-178">值</span><span class="sxs-lookup"><span data-stu-id="77c01-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77c01-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77c01-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77c01-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="77c01-181">System-Only</span></span>            | <span data-ttu-id="77c01-182">否</span><span class="sxs-lookup"><span data-stu-id="77c01-182">False</span></span>                                        |
| <span data-ttu-id="77c01-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77c01-183">Is-Single-Valued</span></span>       | <span data-ttu-id="77c01-184">對</span><span class="sxs-lookup"><span data-stu-id="77c01-184">True</span></span>                                         |
| <span data-ttu-id="77c01-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77c01-185">Is Indexed</span></span>             | <span data-ttu-id="77c01-186">否</span><span class="sxs-lookup"><span data-stu-id="77c01-186">False</span></span>                                        |
| <span data-ttu-id="77c01-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77c01-187">In Global Catalog</span></span>      | <span data-ttu-id="77c01-188">否</span><span class="sxs-lookup"><span data-stu-id="77c01-188">False</span></span>                                        |
| <span data-ttu-id="77c01-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77c01-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="77c01-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77c01-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77c01-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77c01-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77c01-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77c01-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77c01-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-193">Search-Flags</span></span>           | <span data-ttu-id="77c01-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77c01-194">0x00000000</span></span>                                   |
| <span data-ttu-id="77c01-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-195">System-Flags</span></span>           | <span data-ttu-id="77c01-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77c01-196">0x00000010</span></span>                                   |
| <span data-ttu-id="77c01-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77c01-197">Classes used in</span></span>        | [<span data-ttu-id="77c01-198">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="77c01-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="77c01-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77c01-199">Windows Server 2008</span></span>



| <span data-ttu-id="77c01-200">進入</span><span class="sxs-lookup"><span data-stu-id="77c01-200">Entry</span></span> | <span data-ttu-id="77c01-201">值</span><span class="sxs-lookup"><span data-stu-id="77c01-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77c01-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77c01-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77c01-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="77c01-204">System-Only</span></span>            | <span data-ttu-id="77c01-205">否</span><span class="sxs-lookup"><span data-stu-id="77c01-205">False</span></span>                                        |
| <span data-ttu-id="77c01-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77c01-206">Is-Single-Valued</span></span>       | <span data-ttu-id="77c01-207">對</span><span class="sxs-lookup"><span data-stu-id="77c01-207">True</span></span>                                         |
| <span data-ttu-id="77c01-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77c01-208">Is Indexed</span></span>             | <span data-ttu-id="77c01-209">否</span><span class="sxs-lookup"><span data-stu-id="77c01-209">False</span></span>                                        |
| <span data-ttu-id="77c01-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77c01-210">In Global Catalog</span></span>      | <span data-ttu-id="77c01-211">否</span><span class="sxs-lookup"><span data-stu-id="77c01-211">False</span></span>                                        |
| <span data-ttu-id="77c01-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77c01-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="77c01-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77c01-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77c01-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77c01-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77c01-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77c01-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77c01-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-216">Search-Flags</span></span>           | <span data-ttu-id="77c01-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77c01-217">0x00000000</span></span>                                   |
| <span data-ttu-id="77c01-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-218">System-Flags</span></span>           | <span data-ttu-id="77c01-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77c01-219">0x00000010</span></span>                                   |
| <span data-ttu-id="77c01-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77c01-220">Classes used in</span></span>        | [<span data-ttu-id="77c01-221">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="77c01-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="77c01-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77c01-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="77c01-223">進入</span><span class="sxs-lookup"><span data-stu-id="77c01-223">Entry</span></span> | <span data-ttu-id="77c01-224">值</span><span class="sxs-lookup"><span data-stu-id="77c01-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77c01-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77c01-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77c01-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="77c01-227">System-Only</span></span>            | <span data-ttu-id="77c01-228">否</span><span class="sxs-lookup"><span data-stu-id="77c01-228">False</span></span>                                        |
| <span data-ttu-id="77c01-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77c01-229">Is-Single-Valued</span></span>       | <span data-ttu-id="77c01-230">對</span><span class="sxs-lookup"><span data-stu-id="77c01-230">True</span></span>                                         |
| <span data-ttu-id="77c01-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77c01-231">Is Indexed</span></span>             | <span data-ttu-id="77c01-232">否</span><span class="sxs-lookup"><span data-stu-id="77c01-232">False</span></span>                                        |
| <span data-ttu-id="77c01-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77c01-233">In Global Catalog</span></span>      | <span data-ttu-id="77c01-234">否</span><span class="sxs-lookup"><span data-stu-id="77c01-234">False</span></span>                                        |
| <span data-ttu-id="77c01-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77c01-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="77c01-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77c01-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77c01-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77c01-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77c01-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77c01-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77c01-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-239">Search-Flags</span></span>           | <span data-ttu-id="77c01-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77c01-240">0x00000000</span></span>                                   |
| <span data-ttu-id="77c01-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-241">System-Flags</span></span>           | <span data-ttu-id="77c01-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77c01-242">0x00000010</span></span>                                   |
| <span data-ttu-id="77c01-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77c01-243">Classes used in</span></span>        | [<span data-ttu-id="77c01-244">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="77c01-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="77c01-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77c01-245">Windows Server 2012</span></span>



| <span data-ttu-id="77c01-246">進入</span><span class="sxs-lookup"><span data-stu-id="77c01-246">Entry</span></span> | <span data-ttu-id="77c01-247">值</span><span class="sxs-lookup"><span data-stu-id="77c01-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77c01-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77c01-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77c01-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77c01-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="77c01-250">System-Only</span></span>            | <span data-ttu-id="77c01-251">否</span><span class="sxs-lookup"><span data-stu-id="77c01-251">False</span></span>                                        |
| <span data-ttu-id="77c01-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77c01-252">Is-Single-Valued</span></span>       | <span data-ttu-id="77c01-253">對</span><span class="sxs-lookup"><span data-stu-id="77c01-253">True</span></span>                                         |
| <span data-ttu-id="77c01-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77c01-254">Is Indexed</span></span>             | <span data-ttu-id="77c01-255">否</span><span class="sxs-lookup"><span data-stu-id="77c01-255">False</span></span>                                        |
| <span data-ttu-id="77c01-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77c01-256">In Global Catalog</span></span>      | <span data-ttu-id="77c01-257">否</span><span class="sxs-lookup"><span data-stu-id="77c01-257">False</span></span>                                        |
| <span data-ttu-id="77c01-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77c01-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="77c01-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77c01-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77c01-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77c01-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77c01-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77c01-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77c01-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-262">Search-Flags</span></span>           | <span data-ttu-id="77c01-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77c01-263">0x00000000</span></span>                                   |
| <span data-ttu-id="77c01-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77c01-264">System-Flags</span></span>           | <span data-ttu-id="77c01-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77c01-265">0x00000010</span></span>                                   |
| <span data-ttu-id="77c01-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77c01-266">Classes used in</span></span>        | [<span data-ttu-id="77c01-267">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="77c01-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





