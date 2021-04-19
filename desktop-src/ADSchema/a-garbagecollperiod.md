---
title: Coll 期間屬性
description: 這個屬性位於 CN 目錄服務、CN Windows NT、CN Services、CN Configuration,.。。物件。 它代表 DS 垃圾收集執行之間的時間（以小時為單位）。
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- 垃圾 Coll 期間屬性 AD 架構
- garbageCollPeriod 屬性 AD 架構
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106967578"
---
# <a name="garbage-coll-period-attribute"></a><span data-ttu-id="472e9-106">Coll 期間屬性</span><span class="sxs-lookup"><span data-stu-id="472e9-106">Garbage-Coll-Period attribute</span></span>

<span data-ttu-id="472e9-107">這個屬性位於 CN = Directory 服務，CN = Windows NT，CN = Services，CN = Configuration,.。。物件。</span><span class="sxs-lookup"><span data-stu-id="472e9-107">This attribute is located on the CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,... object.</span></span> <span data-ttu-id="472e9-108">它代表 DS 垃圾收集執行之間的時間（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="472e9-108">It represents the time, in hours, between DS garbage collection runs.</span></span>



| <span data-ttu-id="472e9-109">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-109">Entry</span></span> | <span data-ttu-id="472e9-110">值</span><span class="sxs-lookup"><span data-stu-id="472e9-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="472e9-111">CN</span><span class="sxs-lookup"><span data-stu-id="472e9-111">CN</span></span>                | <span data-ttu-id="472e9-112">垃圾 Coll 期間</span><span class="sxs-lookup"><span data-stu-id="472e9-112">Garbage-Coll-Period</span></span>                  |
| <span data-ttu-id="472e9-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="472e9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="472e9-114">garbageCollPeriod</span><span class="sxs-lookup"><span data-stu-id="472e9-114">garbageCollPeriod</span></span>                    |
| <span data-ttu-id="472e9-115">大小</span><span class="sxs-lookup"><span data-stu-id="472e9-115">Size</span></span>              | <span data-ttu-id="472e9-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="472e9-116">4 bytes</span></span>                              |
| <span data-ttu-id="472e9-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="472e9-117">Update Privilege</span></span>  | <span data-ttu-id="472e9-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="472e9-118">Domain administrator</span></span>                 |
| <span data-ttu-id="472e9-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="472e9-119">Update Frequency</span></span>  | <span data-ttu-id="472e9-120">非常罕見。</span><span class="sxs-lookup"><span data-stu-id="472e9-120">Very rare.</span></span>                           |
| <span data-ttu-id="472e9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-121">Attribute-Id</span></span>      | <span data-ttu-id="472e9-122">1.2.840.113556.1.2.301</span><span class="sxs-lookup"><span data-stu-id="472e9-122">1.2.840.113556.1.2.301</span></span>               |
| <span data-ttu-id="472e9-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="472e9-123">System-Id-Guid</span></span>    | <span data-ttu-id="472e9-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="472e9-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span></span> |
| <span data-ttu-id="472e9-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="472e9-125">Syntax</span></span>            | [<span data-ttu-id="472e9-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="472e9-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="472e9-127">實作</span><span class="sxs-lookup"><span data-stu-id="472e9-127">Implementations</span></span>

-   [<span data-ttu-id="472e9-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="472e9-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="472e9-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="472e9-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="472e9-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="472e9-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="472e9-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="472e9-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="472e9-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="472e9-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="472e9-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="472e9-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="472e9-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="472e9-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="472e9-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="472e9-135">Windows 2000 Server</span></span>



| <span data-ttu-id="472e9-136">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-136">Entry</span></span> | <span data-ttu-id="472e9-137">值</span><span class="sxs-lookup"><span data-stu-id="472e9-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="472e9-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="472e9-138">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="472e9-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-139">MAPI-Id</span></span>                | <span data-ttu-id="472e9-140">0x80AF</span><span class="sxs-lookup"><span data-stu-id="472e9-140">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="472e9-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="472e9-141">System-Only</span></span>            | <span data-ttu-id="472e9-142">否</span><span class="sxs-lookup"><span data-stu-id="472e9-142">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="472e9-143">Is-Single-Valued</span></span>       | <span data-ttu-id="472e9-144">對</span><span class="sxs-lookup"><span data-stu-id="472e9-144">True</span></span>                                                                                                  |
| <span data-ttu-id="472e9-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="472e9-145">Is Indexed</span></span>             | <span data-ttu-id="472e9-146">否</span><span class="sxs-lookup"><span data-stu-id="472e9-146">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="472e9-147">In Global Catalog</span></span>      | <span data-ttu-id="472e9-148">否</span><span class="sxs-lookup"><span data-stu-id="472e9-148">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="472e9-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="472e9-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="472e9-150">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="472e9-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="472e9-151">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="472e9-152">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-153">Search-Flags</span></span>           | <span data-ttu-id="472e9-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="472e9-154">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="472e9-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-155">System-Flags</span></span>           | <span data-ttu-id="472e9-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="472e9-156">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="472e9-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="472e9-157">Classes used in</span></span>        | [<span data-ttu-id="472e9-158">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="472e9-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="472e9-159">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="472e9-159">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="472e9-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="472e9-160">Windows Server 2003</span></span>



| <span data-ttu-id="472e9-161">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-161">Entry</span></span> | <span data-ttu-id="472e9-162">值</span><span class="sxs-lookup"><span data-stu-id="472e9-162">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="472e9-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="472e9-163">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="472e9-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-164">MAPI-Id</span></span>                | <span data-ttu-id="472e9-165">0x80AF</span><span class="sxs-lookup"><span data-stu-id="472e9-165">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="472e9-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="472e9-166">System-Only</span></span>            | <span data-ttu-id="472e9-167">否</span><span class="sxs-lookup"><span data-stu-id="472e9-167">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="472e9-168">Is-Single-Valued</span></span>       | <span data-ttu-id="472e9-169">對</span><span class="sxs-lookup"><span data-stu-id="472e9-169">True</span></span>                                                                                                  |
| <span data-ttu-id="472e9-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="472e9-170">Is Indexed</span></span>             | <span data-ttu-id="472e9-171">否</span><span class="sxs-lookup"><span data-stu-id="472e9-171">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="472e9-172">In Global Catalog</span></span>      | <span data-ttu-id="472e9-173">否</span><span class="sxs-lookup"><span data-stu-id="472e9-173">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="472e9-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="472e9-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="472e9-175">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="472e9-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="472e9-176">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="472e9-177">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-178">Search-Flags</span></span>           | <span data-ttu-id="472e9-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="472e9-179">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="472e9-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-180">System-Flags</span></span>           | <span data-ttu-id="472e9-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="472e9-181">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="472e9-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="472e9-182">Classes used in</span></span>        | [<span data-ttu-id="472e9-183">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="472e9-183">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="472e9-184">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="472e9-184">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="472e9-185">亞當</span><span class="sxs-lookup"><span data-stu-id="472e9-185">ADAM</span></span>



| <span data-ttu-id="472e9-186">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-186">Entry</span></span> | <span data-ttu-id="472e9-187">值</span><span class="sxs-lookup"><span data-stu-id="472e9-187">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="472e9-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="472e9-188">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="472e9-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-189">MAPI-Id</span></span>                | <span data-ttu-id="472e9-190">0x80AF</span><span class="sxs-lookup"><span data-stu-id="472e9-190">0x80AF</span></span>                                           |
| <span data-ttu-id="472e9-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="472e9-191">System-Only</span></span>            | <span data-ttu-id="472e9-192">否</span><span class="sxs-lookup"><span data-stu-id="472e9-192">False</span></span>                                            |
| <span data-ttu-id="472e9-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="472e9-193">Is-Single-Valued</span></span>       | <span data-ttu-id="472e9-194">對</span><span class="sxs-lookup"><span data-stu-id="472e9-194">True</span></span>                                             |
| <span data-ttu-id="472e9-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="472e9-195">Is Indexed</span></span>             | <span data-ttu-id="472e9-196">否</span><span class="sxs-lookup"><span data-stu-id="472e9-196">False</span></span>                                            |
| <span data-ttu-id="472e9-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="472e9-197">In Global Catalog</span></span>      | <span data-ttu-id="472e9-198">否</span><span class="sxs-lookup"><span data-stu-id="472e9-198">False</span></span>                                            |
| <span data-ttu-id="472e9-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="472e9-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="472e9-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="472e9-200">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="472e9-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="472e9-201">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="472e9-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="472e9-202">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="472e9-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-203">Search-Flags</span></span>           | <span data-ttu-id="472e9-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="472e9-204">0x00000000</span></span>                                       |
| <span data-ttu-id="472e9-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-205">System-Flags</span></span>           | <span data-ttu-id="472e9-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="472e9-206">0x00000010</span></span>                                       |
| <span data-ttu-id="472e9-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="472e9-207">Classes used in</span></span>        | [<span data-ttu-id="472e9-208">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="472e9-208">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="472e9-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="472e9-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="472e9-210">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-210">Entry</span></span> | <span data-ttu-id="472e9-211">值</span><span class="sxs-lookup"><span data-stu-id="472e9-211">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="472e9-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="472e9-212">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="472e9-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-213">MAPI-Id</span></span>                | <span data-ttu-id="472e9-214">0x80AF</span><span class="sxs-lookup"><span data-stu-id="472e9-214">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="472e9-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="472e9-215">System-Only</span></span>            | <span data-ttu-id="472e9-216">否</span><span class="sxs-lookup"><span data-stu-id="472e9-216">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="472e9-217">Is-Single-Valued</span></span>       | <span data-ttu-id="472e9-218">對</span><span class="sxs-lookup"><span data-stu-id="472e9-218">True</span></span>                                                                                                  |
| <span data-ttu-id="472e9-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="472e9-219">Is Indexed</span></span>             | <span data-ttu-id="472e9-220">否</span><span class="sxs-lookup"><span data-stu-id="472e9-220">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="472e9-221">In Global Catalog</span></span>      | <span data-ttu-id="472e9-222">否</span><span class="sxs-lookup"><span data-stu-id="472e9-222">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="472e9-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="472e9-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="472e9-224">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="472e9-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="472e9-225">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="472e9-226">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-227">Search-Flags</span></span>           | <span data-ttu-id="472e9-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="472e9-228">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="472e9-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-229">System-Flags</span></span>           | <span data-ttu-id="472e9-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="472e9-230">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="472e9-231">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="472e9-231">Classes used in</span></span>        | [<span data-ttu-id="472e9-232">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="472e9-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="472e9-233">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="472e9-233">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="472e9-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="472e9-234">Windows Server 2008</span></span>



| <span data-ttu-id="472e9-235">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-235">Entry</span></span> | <span data-ttu-id="472e9-236">值</span><span class="sxs-lookup"><span data-stu-id="472e9-236">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="472e9-237">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="472e9-237">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="472e9-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-238">MAPI-Id</span></span>                | <span data-ttu-id="472e9-239">0x80AF</span><span class="sxs-lookup"><span data-stu-id="472e9-239">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="472e9-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="472e9-240">System-Only</span></span>            | <span data-ttu-id="472e9-241">否</span><span class="sxs-lookup"><span data-stu-id="472e9-241">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-242">是-單一值</span><span class="sxs-lookup"><span data-stu-id="472e9-242">Is-Single-Valued</span></span>       | <span data-ttu-id="472e9-243">對</span><span class="sxs-lookup"><span data-stu-id="472e9-243">True</span></span>                                                                                                  |
| <span data-ttu-id="472e9-244">已編制索引</span><span class="sxs-lookup"><span data-stu-id="472e9-244">Is Indexed</span></span>             | <span data-ttu-id="472e9-245">否</span><span class="sxs-lookup"><span data-stu-id="472e9-245">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-246">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="472e9-246">In Global Catalog</span></span>      | <span data-ttu-id="472e9-247">否</span><span class="sxs-lookup"><span data-stu-id="472e9-247">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-248">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="472e9-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="472e9-249">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="472e9-249">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="472e9-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="472e9-250">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="472e9-251">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-252">Search-Flags</span></span>           | <span data-ttu-id="472e9-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="472e9-253">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="472e9-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-254">System-Flags</span></span>           | <span data-ttu-id="472e9-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="472e9-255">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="472e9-256">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="472e9-256">Classes used in</span></span>        | [<span data-ttu-id="472e9-257">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="472e9-257">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="472e9-258">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="472e9-258">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="472e9-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="472e9-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="472e9-260">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-260">Entry</span></span> | <span data-ttu-id="472e9-261">值</span><span class="sxs-lookup"><span data-stu-id="472e9-261">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="472e9-262">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="472e9-262">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="472e9-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-263">MAPI-Id</span></span>                | <span data-ttu-id="472e9-264">0x80AF</span><span class="sxs-lookup"><span data-stu-id="472e9-264">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="472e9-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="472e9-265">System-Only</span></span>            | <span data-ttu-id="472e9-266">否</span><span class="sxs-lookup"><span data-stu-id="472e9-266">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="472e9-267">Is-Single-Valued</span></span>       | <span data-ttu-id="472e9-268">對</span><span class="sxs-lookup"><span data-stu-id="472e9-268">True</span></span>                                                                                                  |
| <span data-ttu-id="472e9-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="472e9-269">Is Indexed</span></span>             | <span data-ttu-id="472e9-270">否</span><span class="sxs-lookup"><span data-stu-id="472e9-270">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="472e9-271">In Global Catalog</span></span>      | <span data-ttu-id="472e9-272">否</span><span class="sxs-lookup"><span data-stu-id="472e9-272">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="472e9-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="472e9-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="472e9-274">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="472e9-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="472e9-275">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="472e9-276">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-277">Search-Flags</span></span>           | <span data-ttu-id="472e9-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="472e9-278">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="472e9-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-279">System-Flags</span></span>           | <span data-ttu-id="472e9-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="472e9-280">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="472e9-281">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="472e9-281">Classes used in</span></span>        | [<span data-ttu-id="472e9-282">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="472e9-282">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="472e9-283">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="472e9-283">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="472e9-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="472e9-284">Windows Server 2012</span></span>



| <span data-ttu-id="472e9-285">進入</span><span class="sxs-lookup"><span data-stu-id="472e9-285">Entry</span></span> | <span data-ttu-id="472e9-286">值</span><span class="sxs-lookup"><span data-stu-id="472e9-286">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="472e9-287">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="472e9-287">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="472e9-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="472e9-288">MAPI-Id</span></span>                | <span data-ttu-id="472e9-289">0x80AF</span><span class="sxs-lookup"><span data-stu-id="472e9-289">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="472e9-290">System-Only</span><span class="sxs-lookup"><span data-stu-id="472e9-290">System-Only</span></span>            | <span data-ttu-id="472e9-291">否</span><span class="sxs-lookup"><span data-stu-id="472e9-291">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-292">是-單一值</span><span class="sxs-lookup"><span data-stu-id="472e9-292">Is-Single-Valued</span></span>       | <span data-ttu-id="472e9-293">對</span><span class="sxs-lookup"><span data-stu-id="472e9-293">True</span></span>                                                                                                  |
| <span data-ttu-id="472e9-294">已編制索引</span><span class="sxs-lookup"><span data-stu-id="472e9-294">Is Indexed</span></span>             | <span data-ttu-id="472e9-295">否</span><span class="sxs-lookup"><span data-stu-id="472e9-295">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-296">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="472e9-296">In Global Catalog</span></span>      | <span data-ttu-id="472e9-297">否</span><span class="sxs-lookup"><span data-stu-id="472e9-297">False</span></span>                                                                                                 |
| <span data-ttu-id="472e9-298">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="472e9-298">NT-Security-Descriptor</span></span> | <span data-ttu-id="472e9-299">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="472e9-299">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="472e9-300">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="472e9-300">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="472e9-301">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="472e9-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-302">Search-Flags</span></span>           | <span data-ttu-id="472e9-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="472e9-303">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="472e9-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="472e9-304">System-Flags</span></span>           | <span data-ttu-id="472e9-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="472e9-305">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="472e9-306">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="472e9-306">Classes used in</span></span>        | [<span data-ttu-id="472e9-307">**郵件收件者**</span><span class="sxs-lookup"><span data-stu-id="472e9-307">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="472e9-308">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="472e9-308">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





