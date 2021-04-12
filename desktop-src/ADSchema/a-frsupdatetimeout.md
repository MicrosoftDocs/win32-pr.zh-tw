---
title: FRS-更新-Timeout 屬性
description: 在放棄之前，要等候完成更新的最長時間（以分鐘為單位）。
ms.assetid: 0c06510e-d4a8-42f8-bf81-13a9f103e237
ms.tgt_platform: multiple
keywords:
- FRS-更新-Timeout 屬性 AD 架構
- fRSUpdateTimeout 屬性 AD 架構
topic_type:
- apiref
api_name:
- FRS-Update-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73730ec18942f98c07c0a4756bb8c7716e6abfd2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509645"
---
# <a name="frs-update-timeout-attribute"></a><span data-ttu-id="ace3a-105">FRS-更新-Timeout 屬性</span><span class="sxs-lookup"><span data-stu-id="ace3a-105">FRS-Update-Timeout attribute</span></span>

<span data-ttu-id="ace3a-106">在放棄之前，要等候完成更新的最長時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="ace3a-106">The maximum time, in minutes, to wait to complete an update before giving up.</span></span>



| <span data-ttu-id="ace3a-107">進入</span><span class="sxs-lookup"><span data-stu-id="ace3a-107">Entry</span></span> | <span data-ttu-id="ace3a-108">值</span><span class="sxs-lookup"><span data-stu-id="ace3a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ace3a-109">CN</span><span class="sxs-lookup"><span data-stu-id="ace3a-109">CN</span></span>                | <span data-ttu-id="ace3a-110">FRS-更新-超時</span><span class="sxs-lookup"><span data-stu-id="ace3a-110">FRS-Update-Timeout</span></span>                   |
| <span data-ttu-id="ace3a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ace3a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ace3a-112">fRSUpdateTimeout</span><span class="sxs-lookup"><span data-stu-id="ace3a-112">fRSUpdateTimeout</span></span>                     |
| <span data-ttu-id="ace3a-113">大小</span><span class="sxs-lookup"><span data-stu-id="ace3a-113">Size</span></span>              | <span data-ttu-id="ace3a-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ace3a-114">4 bytes</span></span>                              |
| <span data-ttu-id="ace3a-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ace3a-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ace3a-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ace3a-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ace3a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ace3a-117">Attribute-Id</span></span>      | <span data-ttu-id="ace3a-118">1.2.840.113556.1.4.485</span><span class="sxs-lookup"><span data-stu-id="ace3a-118">1.2.840.113556.1.4.485</span></span>               |
| <span data-ttu-id="ace3a-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ace3a-119">System-Id-Guid</span></span>    | <span data-ttu-id="ace3a-120">1be8f172-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="ace3a-120">1be8f172-a9ff-11d0-afe2-00c04fd930c9</span></span> |
| <span data-ttu-id="ace3a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ace3a-121">Syntax</span></span>            | [<span data-ttu-id="ace3a-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ace3a-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ace3a-123">實作</span><span class="sxs-lookup"><span data-stu-id="ace3a-123">Implementations</span></span>

-   [<span data-ttu-id="ace3a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ace3a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ace3a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ace3a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ace3a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ace3a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ace3a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ace3a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ace3a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ace3a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ace3a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ace3a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ace3a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ace3a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ace3a-131">進入</span><span class="sxs-lookup"><span data-stu-id="ace3a-131">Entry</span></span> | <span data-ttu-id="ace3a-132">值</span><span class="sxs-lookup"><span data-stu-id="ace3a-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace3a-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ace3a-133">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ace3a-134">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ace3a-135">System-Only</span></span>            | <span data-ttu-id="ace3a-136">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-136">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ace3a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ace3a-138">對</span><span class="sxs-lookup"><span data-stu-id="ace3a-138">True</span></span>                                                                                                      |
| <span data-ttu-id="ace3a-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ace3a-139">Is Indexed</span></span>             | <span data-ttu-id="ace3a-140">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-140">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ace3a-141">In Global Catalog</span></span>      | <span data-ttu-id="ace3a-142">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-142">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ace3a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ace3a-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ace3a-144">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ace3a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ace3a-145">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ace3a-146">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-147">Search-Flags</span></span>           | <span data-ttu-id="ace3a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ace3a-148">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ace3a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-149">System-Flags</span></span>           | <span data-ttu-id="ace3a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ace3a-150">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ace3a-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ace3a-151">Classes used in</span></span>        | [<span data-ttu-id="ace3a-152">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="ace3a-152">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="ace3a-153">**NTFRS-訂閱者**</span><span class="sxs-lookup"><span data-stu-id="ace3a-153">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ace3a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ace3a-154">Windows Server 2003</span></span>



| <span data-ttu-id="ace3a-155">進入</span><span class="sxs-lookup"><span data-stu-id="ace3a-155">Entry</span></span> | <span data-ttu-id="ace3a-156">值</span><span class="sxs-lookup"><span data-stu-id="ace3a-156">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace3a-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ace3a-157">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ace3a-158">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ace3a-159">System-Only</span></span>            | <span data-ttu-id="ace3a-160">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-160">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ace3a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ace3a-162">對</span><span class="sxs-lookup"><span data-stu-id="ace3a-162">True</span></span>                                                                                                      |
| <span data-ttu-id="ace3a-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ace3a-163">Is Indexed</span></span>             | <span data-ttu-id="ace3a-164">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-164">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ace3a-165">In Global Catalog</span></span>      | <span data-ttu-id="ace3a-166">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-166">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ace3a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ace3a-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ace3a-168">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ace3a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ace3a-169">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ace3a-170">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-171">Search-Flags</span></span>           | <span data-ttu-id="ace3a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ace3a-172">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ace3a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-173">System-Flags</span></span>           | <span data-ttu-id="ace3a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ace3a-174">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ace3a-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ace3a-175">Classes used in</span></span>        | [<span data-ttu-id="ace3a-176">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="ace3a-176">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="ace3a-177">**NTFRS-訂閱者**</span><span class="sxs-lookup"><span data-stu-id="ace3a-177">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ace3a-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ace3a-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ace3a-179">進入</span><span class="sxs-lookup"><span data-stu-id="ace3a-179">Entry</span></span> | <span data-ttu-id="ace3a-180">值</span><span class="sxs-lookup"><span data-stu-id="ace3a-180">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace3a-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ace3a-181">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ace3a-182">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ace3a-183">System-Only</span></span>            | <span data-ttu-id="ace3a-184">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-184">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ace3a-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ace3a-186">對</span><span class="sxs-lookup"><span data-stu-id="ace3a-186">True</span></span>                                                                                                      |
| <span data-ttu-id="ace3a-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ace3a-187">Is Indexed</span></span>             | <span data-ttu-id="ace3a-188">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-188">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ace3a-189">In Global Catalog</span></span>      | <span data-ttu-id="ace3a-190">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-190">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ace3a-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ace3a-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ace3a-192">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ace3a-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ace3a-193">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ace3a-194">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-195">Search-Flags</span></span>           | <span data-ttu-id="ace3a-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ace3a-196">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ace3a-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-197">System-Flags</span></span>           | <span data-ttu-id="ace3a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ace3a-198">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ace3a-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ace3a-199">Classes used in</span></span>        | [<span data-ttu-id="ace3a-200">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="ace3a-200">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="ace3a-201">**NTFRS-訂閱者**</span><span class="sxs-lookup"><span data-stu-id="ace3a-201">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ace3a-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ace3a-202">Windows Server 2008</span></span>



| <span data-ttu-id="ace3a-203">進入</span><span class="sxs-lookup"><span data-stu-id="ace3a-203">Entry</span></span> | <span data-ttu-id="ace3a-204">值</span><span class="sxs-lookup"><span data-stu-id="ace3a-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace3a-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ace3a-205">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ace3a-206">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ace3a-207">System-Only</span></span>            | <span data-ttu-id="ace3a-208">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-208">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ace3a-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ace3a-210">對</span><span class="sxs-lookup"><span data-stu-id="ace3a-210">True</span></span>                                                                                                      |
| <span data-ttu-id="ace3a-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ace3a-211">Is Indexed</span></span>             | <span data-ttu-id="ace3a-212">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-212">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ace3a-213">In Global Catalog</span></span>      | <span data-ttu-id="ace3a-214">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-214">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ace3a-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ace3a-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ace3a-216">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ace3a-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ace3a-217">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ace3a-218">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-219">Search-Flags</span></span>           | <span data-ttu-id="ace3a-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ace3a-220">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ace3a-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-221">System-Flags</span></span>           | <span data-ttu-id="ace3a-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ace3a-222">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ace3a-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ace3a-223">Classes used in</span></span>        | [<span data-ttu-id="ace3a-224">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="ace3a-224">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="ace3a-225">**NTFRS-訂閱者**</span><span class="sxs-lookup"><span data-stu-id="ace3a-225">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ace3a-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ace3a-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ace3a-227">進入</span><span class="sxs-lookup"><span data-stu-id="ace3a-227">Entry</span></span> | <span data-ttu-id="ace3a-228">值</span><span class="sxs-lookup"><span data-stu-id="ace3a-228">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace3a-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ace3a-229">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ace3a-230">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="ace3a-231">System-Only</span></span>            | <span data-ttu-id="ace3a-232">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-232">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ace3a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="ace3a-234">對</span><span class="sxs-lookup"><span data-stu-id="ace3a-234">True</span></span>                                                                                                      |
| <span data-ttu-id="ace3a-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ace3a-235">Is Indexed</span></span>             | <span data-ttu-id="ace3a-236">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-236">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ace3a-237">In Global Catalog</span></span>      | <span data-ttu-id="ace3a-238">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-238">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ace3a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="ace3a-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ace3a-240">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ace3a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ace3a-241">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ace3a-242">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-243">Search-Flags</span></span>           | <span data-ttu-id="ace3a-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ace3a-244">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ace3a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-245">System-Flags</span></span>           | <span data-ttu-id="ace3a-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ace3a-246">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ace3a-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ace3a-247">Classes used in</span></span>        | [<span data-ttu-id="ace3a-248">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="ace3a-248">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="ace3a-249">**NTFRS-訂閱者**</span><span class="sxs-lookup"><span data-stu-id="ace3a-249">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ace3a-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ace3a-250">Windows Server 2012</span></span>



| <span data-ttu-id="ace3a-251">進入</span><span class="sxs-lookup"><span data-stu-id="ace3a-251">Entry</span></span> | <span data-ttu-id="ace3a-252">值</span><span class="sxs-lookup"><span data-stu-id="ace3a-252">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace3a-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ace3a-253">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ace3a-254">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ace3a-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="ace3a-255">System-Only</span></span>            | <span data-ttu-id="ace3a-256">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-256">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ace3a-257">Is-Single-Valued</span></span>       | <span data-ttu-id="ace3a-258">對</span><span class="sxs-lookup"><span data-stu-id="ace3a-258">True</span></span>                                                                                                      |
| <span data-ttu-id="ace3a-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ace3a-259">Is Indexed</span></span>             | <span data-ttu-id="ace3a-260">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-260">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ace3a-261">In Global Catalog</span></span>      | <span data-ttu-id="ace3a-262">否</span><span class="sxs-lookup"><span data-stu-id="ace3a-262">False</span></span>                                                                                                     |
| <span data-ttu-id="ace3a-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ace3a-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="ace3a-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ace3a-264">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ace3a-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ace3a-265">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ace3a-266">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ace3a-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-267">Search-Flags</span></span>           | <span data-ttu-id="ace3a-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ace3a-268">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ace3a-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ace3a-269">System-Flags</span></span>           | <span data-ttu-id="ace3a-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ace3a-270">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ace3a-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ace3a-271">Classes used in</span></span>        | [<span data-ttu-id="ace3a-272">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="ace3a-272">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="ace3a-273">**NTFRS-訂閱者**</span><span class="sxs-lookup"><span data-stu-id="ace3a-273">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



 

 





