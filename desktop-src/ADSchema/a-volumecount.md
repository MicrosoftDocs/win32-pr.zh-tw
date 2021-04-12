---
title: Volume-Count 屬性
description: 指定電腦的追蹤磁片區配額。
ms.assetid: a764a650-2cce-4df4-9a5e-d5fc8de196cb
ms.tgt_platform: multiple
keywords:
- Volume-Count 屬性 AD 架構
- volumeCount 屬性 AD 架構
topic_type:
- apiref
api_name:
- Volume-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2242926ce379cdba9a19ae1ad0dc2612a3375f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935338"
---
# <a name="volume-count-attribute"></a><span data-ttu-id="be9a1-105">Volume-Count 屬性</span><span class="sxs-lookup"><span data-stu-id="be9a1-105">Volume-Count attribute</span></span>

<span data-ttu-id="be9a1-106">指定電腦的追蹤磁片區配額。</span><span class="sxs-lookup"><span data-stu-id="be9a1-106">The tracked volume quota for a given computer.</span></span>



| <span data-ttu-id="be9a1-107">進入</span><span class="sxs-lookup"><span data-stu-id="be9a1-107">Entry</span></span> | <span data-ttu-id="be9a1-108">值</span><span class="sxs-lookup"><span data-stu-id="be9a1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="be9a1-109">CN</span><span class="sxs-lookup"><span data-stu-id="be9a1-109">CN</span></span>                | <span data-ttu-id="be9a1-110">Volume-Count</span><span class="sxs-lookup"><span data-stu-id="be9a1-110">Volume-Count</span></span>                         |
| <span data-ttu-id="be9a1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="be9a1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="be9a1-112">volumeCount</span><span class="sxs-lookup"><span data-stu-id="be9a1-112">volumeCount</span></span>                          |
| <span data-ttu-id="be9a1-113">大小</span><span class="sxs-lookup"><span data-stu-id="be9a1-113">Size</span></span>              | <span data-ttu-id="be9a1-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="be9a1-114">4 bytes</span></span>                              |
| <span data-ttu-id="be9a1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="be9a1-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="be9a1-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="be9a1-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="be9a1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be9a1-117">Attribute-Id</span></span>      | <span data-ttu-id="be9a1-118">1.2.840.113556.1.4.507</span><span class="sxs-lookup"><span data-stu-id="be9a1-118">1.2.840.113556.1.4.507</span></span>               |
| <span data-ttu-id="be9a1-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="be9a1-119">System-Id-Guid</span></span>    | <span data-ttu-id="be9a1-120">34aaa217-b699-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="be9a1-120">34aaa217-b699-11d0-afee-0000f80367c1</span></span> |
| <span data-ttu-id="be9a1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="be9a1-121">Syntax</span></span>            | [<span data-ttu-id="be9a1-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="be9a1-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="be9a1-123">實作</span><span class="sxs-lookup"><span data-stu-id="be9a1-123">Implementations</span></span>

-   [<span data-ttu-id="be9a1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="be9a1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="be9a1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="be9a1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="be9a1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be9a1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be9a1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be9a1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be9a1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be9a1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be9a1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be9a1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="be9a1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be9a1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="be9a1-131">進入</span><span class="sxs-lookup"><span data-stu-id="be9a1-131">Entry</span></span> | <span data-ttu-id="be9a1-132">值</span><span class="sxs-lookup"><span data-stu-id="be9a1-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="be9a1-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be9a1-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be9a1-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="be9a1-135">System-Only</span></span>            | <span data-ttu-id="be9a1-136">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-136">False</span></span>                                     |
| <span data-ttu-id="be9a1-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be9a1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="be9a1-138">對</span><span class="sxs-lookup"><span data-stu-id="be9a1-138">True</span></span>                                      |
| <span data-ttu-id="be9a1-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be9a1-139">Is Indexed</span></span>             | <span data-ttu-id="be9a1-140">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-140">False</span></span>                                     |
| <span data-ttu-id="be9a1-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be9a1-141">In Global Catalog</span></span>      | <span data-ttu-id="be9a1-142">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-142">False</span></span>                                     |
| <span data-ttu-id="be9a1-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be9a1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="be9a1-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be9a1-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="be9a1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be9a1-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be9a1-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-147">Search-Flags</span></span>           | <span data-ttu-id="be9a1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be9a1-148">0x00000000</span></span>                                |
| <span data-ttu-id="be9a1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-149">System-Flags</span></span>           | <span data-ttu-id="be9a1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be9a1-150">0x00000010</span></span>                                |
| <span data-ttu-id="be9a1-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be9a1-151">Classes used in</span></span>        | [<span data-ttu-id="be9a1-152">**電腦**</span><span class="sxs-lookup"><span data-stu-id="be9a1-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="be9a1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be9a1-153">Windows Server 2003</span></span>



| <span data-ttu-id="be9a1-154">進入</span><span class="sxs-lookup"><span data-stu-id="be9a1-154">Entry</span></span> | <span data-ttu-id="be9a1-155">值</span><span class="sxs-lookup"><span data-stu-id="be9a1-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="be9a1-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be9a1-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be9a1-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="be9a1-158">System-Only</span></span>            | <span data-ttu-id="be9a1-159">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-159">False</span></span>                                     |
| <span data-ttu-id="be9a1-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be9a1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="be9a1-161">對</span><span class="sxs-lookup"><span data-stu-id="be9a1-161">True</span></span>                                      |
| <span data-ttu-id="be9a1-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be9a1-162">Is Indexed</span></span>             | <span data-ttu-id="be9a1-163">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-163">False</span></span>                                     |
| <span data-ttu-id="be9a1-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be9a1-164">In Global Catalog</span></span>      | <span data-ttu-id="be9a1-165">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-165">False</span></span>                                     |
| <span data-ttu-id="be9a1-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be9a1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="be9a1-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be9a1-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="be9a1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be9a1-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be9a1-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-170">Search-Flags</span></span>           | <span data-ttu-id="be9a1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be9a1-171">0x00000000</span></span>                                |
| <span data-ttu-id="be9a1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-172">System-Flags</span></span>           | <span data-ttu-id="be9a1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be9a1-173">0x00000010</span></span>                                |
| <span data-ttu-id="be9a1-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be9a1-174">Classes used in</span></span>        | [<span data-ttu-id="be9a1-175">**電腦**</span><span class="sxs-lookup"><span data-stu-id="be9a1-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="be9a1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be9a1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be9a1-177">進入</span><span class="sxs-lookup"><span data-stu-id="be9a1-177">Entry</span></span> | <span data-ttu-id="be9a1-178">值</span><span class="sxs-lookup"><span data-stu-id="be9a1-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="be9a1-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be9a1-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be9a1-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="be9a1-181">System-Only</span></span>            | <span data-ttu-id="be9a1-182">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-182">False</span></span>                                     |
| <span data-ttu-id="be9a1-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be9a1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="be9a1-184">對</span><span class="sxs-lookup"><span data-stu-id="be9a1-184">True</span></span>                                      |
| <span data-ttu-id="be9a1-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be9a1-185">Is Indexed</span></span>             | <span data-ttu-id="be9a1-186">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-186">False</span></span>                                     |
| <span data-ttu-id="be9a1-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be9a1-187">In Global Catalog</span></span>      | <span data-ttu-id="be9a1-188">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-188">False</span></span>                                     |
| <span data-ttu-id="be9a1-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be9a1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="be9a1-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be9a1-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="be9a1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be9a1-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be9a1-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-193">Search-Flags</span></span>           | <span data-ttu-id="be9a1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be9a1-194">0x00000000</span></span>                                |
| <span data-ttu-id="be9a1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-195">System-Flags</span></span>           | <span data-ttu-id="be9a1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be9a1-196">0x00000010</span></span>                                |
| <span data-ttu-id="be9a1-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be9a1-197">Classes used in</span></span>        | [<span data-ttu-id="be9a1-198">**電腦**</span><span class="sxs-lookup"><span data-stu-id="be9a1-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be9a1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be9a1-199">Windows Server 2008</span></span>



| <span data-ttu-id="be9a1-200">進入</span><span class="sxs-lookup"><span data-stu-id="be9a1-200">Entry</span></span> | <span data-ttu-id="be9a1-201">值</span><span class="sxs-lookup"><span data-stu-id="be9a1-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="be9a1-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be9a1-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be9a1-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="be9a1-204">System-Only</span></span>            | <span data-ttu-id="be9a1-205">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-205">False</span></span>                                     |
| <span data-ttu-id="be9a1-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be9a1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="be9a1-207">對</span><span class="sxs-lookup"><span data-stu-id="be9a1-207">True</span></span>                                      |
| <span data-ttu-id="be9a1-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be9a1-208">Is Indexed</span></span>             | <span data-ttu-id="be9a1-209">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-209">False</span></span>                                     |
| <span data-ttu-id="be9a1-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be9a1-210">In Global Catalog</span></span>      | <span data-ttu-id="be9a1-211">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-211">False</span></span>                                     |
| <span data-ttu-id="be9a1-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be9a1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="be9a1-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be9a1-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="be9a1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be9a1-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be9a1-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-216">Search-Flags</span></span>           | <span data-ttu-id="be9a1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be9a1-217">0x00000000</span></span>                                |
| <span data-ttu-id="be9a1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-218">System-Flags</span></span>           | <span data-ttu-id="be9a1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be9a1-219">0x00000010</span></span>                                |
| <span data-ttu-id="be9a1-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be9a1-220">Classes used in</span></span>        | [<span data-ttu-id="be9a1-221">**電腦**</span><span class="sxs-lookup"><span data-stu-id="be9a1-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be9a1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be9a1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be9a1-223">進入</span><span class="sxs-lookup"><span data-stu-id="be9a1-223">Entry</span></span> | <span data-ttu-id="be9a1-224">值</span><span class="sxs-lookup"><span data-stu-id="be9a1-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="be9a1-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be9a1-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be9a1-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="be9a1-227">System-Only</span></span>            | <span data-ttu-id="be9a1-228">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-228">False</span></span>                                     |
| <span data-ttu-id="be9a1-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be9a1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="be9a1-230">對</span><span class="sxs-lookup"><span data-stu-id="be9a1-230">True</span></span>                                      |
| <span data-ttu-id="be9a1-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be9a1-231">Is Indexed</span></span>             | <span data-ttu-id="be9a1-232">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-232">False</span></span>                                     |
| <span data-ttu-id="be9a1-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be9a1-233">In Global Catalog</span></span>      | <span data-ttu-id="be9a1-234">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-234">False</span></span>                                     |
| <span data-ttu-id="be9a1-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be9a1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="be9a1-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be9a1-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="be9a1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be9a1-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be9a1-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-239">Search-Flags</span></span>           | <span data-ttu-id="be9a1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be9a1-240">0x00000000</span></span>                                |
| <span data-ttu-id="be9a1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-241">System-Flags</span></span>           | <span data-ttu-id="be9a1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be9a1-242">0x00000010</span></span>                                |
| <span data-ttu-id="be9a1-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be9a1-243">Classes used in</span></span>        | [<span data-ttu-id="be9a1-244">**電腦**</span><span class="sxs-lookup"><span data-stu-id="be9a1-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be9a1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be9a1-245">Windows Server 2012</span></span>



| <span data-ttu-id="be9a1-246">進入</span><span class="sxs-lookup"><span data-stu-id="be9a1-246">Entry</span></span> | <span data-ttu-id="be9a1-247">值</span><span class="sxs-lookup"><span data-stu-id="be9a1-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="be9a1-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="be9a1-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be9a1-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="be9a1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="be9a1-250">System-Only</span></span>            | <span data-ttu-id="be9a1-251">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-251">False</span></span>                                     |
| <span data-ttu-id="be9a1-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="be9a1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="be9a1-253">對</span><span class="sxs-lookup"><span data-stu-id="be9a1-253">True</span></span>                                      |
| <span data-ttu-id="be9a1-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="be9a1-254">Is Indexed</span></span>             | <span data-ttu-id="be9a1-255">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-255">False</span></span>                                     |
| <span data-ttu-id="be9a1-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="be9a1-256">In Global Catalog</span></span>      | <span data-ttu-id="be9a1-257">否</span><span class="sxs-lookup"><span data-stu-id="be9a1-257">False</span></span>                                     |
| <span data-ttu-id="be9a1-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="be9a1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="be9a1-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="be9a1-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="be9a1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be9a1-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be9a1-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="be9a1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-262">Search-Flags</span></span>           | <span data-ttu-id="be9a1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be9a1-263">0x00000000</span></span>                                |
| <span data-ttu-id="be9a1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be9a1-264">System-Flags</span></span>           | <span data-ttu-id="be9a1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="be9a1-265">0x00000010</span></span>                                |
| <span data-ttu-id="be9a1-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="be9a1-266">Classes used in</span></span>        | [<span data-ttu-id="be9a1-267">**電腦**</span><span class="sxs-lookup"><span data-stu-id="be9a1-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





