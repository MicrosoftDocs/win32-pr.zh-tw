---
title: MSMQ-多播-位址屬性
description: 這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。 它會控制 MSMQ 是否接受來自多播位址的訊息。
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- MSMQ-多播-位址屬性 AD 架構
- MSMQ-MulticastAddress 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509605"
---
# <a name="msmq-multicast-address-attribute"></a><span data-ttu-id="13a89-106">MSMQ-多播-位址屬性</span><span class="sxs-lookup"><span data-stu-id="13a89-106">MSMQ-Multicast-Address attribute</span></span>

<span data-ttu-id="13a89-107">這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。</span><span class="sxs-lookup"><span data-stu-id="13a89-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="13a89-108">它會控制 MSMQ 是否接受來自多播位址的訊息。</span><span class="sxs-lookup"><span data-stu-id="13a89-108">It controls whether MSMQ will accept messages from a multicast address.</span></span>



| <span data-ttu-id="13a89-109">進入</span><span class="sxs-lookup"><span data-stu-id="13a89-109">Entry</span></span> | <span data-ttu-id="13a89-110">值</span><span class="sxs-lookup"><span data-stu-id="13a89-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="13a89-111">CN</span><span class="sxs-lookup"><span data-stu-id="13a89-111">CN</span></span>                | <span data-ttu-id="13a89-112">MSMQ-多播-位址</span><span class="sxs-lookup"><span data-stu-id="13a89-112">MSMQ-Multicast-Address</span></span>                      |
| <span data-ttu-id="13a89-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="13a89-113">Ldap-Display-Name</span></span> | <span data-ttu-id="13a89-114">MSMQ-MulticastAddress</span><span class="sxs-lookup"><span data-stu-id="13a89-114">MSMQ-MulticastAddress</span></span>                       |
| <span data-ttu-id="13a89-115">大小</span><span class="sxs-lookup"><span data-stu-id="13a89-115">Size</span></span>              | <span data-ttu-id="13a89-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="13a89-116">4 bytes</span></span>                                     |
| <span data-ttu-id="13a89-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="13a89-117">Update Privilege</span></span>  | <span data-ttu-id="13a89-118">佇列擁有者。</span><span class="sxs-lookup"><span data-stu-id="13a89-118">The queue owner.</span></span>                            |
| <span data-ttu-id="13a89-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="13a89-119">Update Frequency</span></span>  | <span data-ttu-id="13a89-120">當佇列建立時。</span><span class="sxs-lookup"><span data-stu-id="13a89-120">When a queue is created.</span></span>                    |
| <span data-ttu-id="13a89-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13a89-121">Attribute-Id</span></span>      | <span data-ttu-id="13a89-122">1.2.840.113556.1.4.1714</span><span class="sxs-lookup"><span data-stu-id="13a89-122">1.2.840.113556.1.4.1714</span></span>                     |
| <span data-ttu-id="13a89-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="13a89-123">System-Id-Guid</span></span>    | <span data-ttu-id="13a89-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span><span class="sxs-lookup"><span data-stu-id="13a89-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span></span>        |
| <span data-ttu-id="13a89-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="13a89-125">Syntax</span></span>            | [<span data-ttu-id="13a89-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="13a89-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="13a89-127">實作</span><span class="sxs-lookup"><span data-stu-id="13a89-127">Implementations</span></span>

-   [<span data-ttu-id="13a89-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="13a89-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="13a89-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="13a89-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="13a89-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13a89-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13a89-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13a89-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13a89-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13a89-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="13a89-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13a89-133">Windows Server 2003</span></span>



| <span data-ttu-id="13a89-134">進入</span><span class="sxs-lookup"><span data-stu-id="13a89-134">Entry</span></span> | <span data-ttu-id="13a89-135">值</span><span class="sxs-lookup"><span data-stu-id="13a89-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a89-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13a89-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a89-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a89-138">System-Only</span></span>            | <span data-ttu-id="13a89-139">否</span><span class="sxs-lookup"><span data-stu-id="13a89-139">False</span></span>                                        |
| <span data-ttu-id="13a89-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13a89-140">Is-Single-Valued</span></span>       | <span data-ttu-id="13a89-141">對</span><span class="sxs-lookup"><span data-stu-id="13a89-141">True</span></span>                                         |
| <span data-ttu-id="13a89-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13a89-142">Is Indexed</span></span>             | <span data-ttu-id="13a89-143">否</span><span class="sxs-lookup"><span data-stu-id="13a89-143">False</span></span>                                        |
| <span data-ttu-id="13a89-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13a89-144">In Global Catalog</span></span>      | <span data-ttu-id="13a89-145">對</span><span class="sxs-lookup"><span data-stu-id="13a89-145">True</span></span>                                         |
| <span data-ttu-id="13a89-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13a89-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a89-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13a89-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a89-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a89-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a89-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a89-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a89-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-150">Search-Flags</span></span>           | <span data-ttu-id="13a89-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a89-151">0x00000000</span></span>                                   |
| <span data-ttu-id="13a89-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-152">System-Flags</span></span>           | <span data-ttu-id="13a89-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a89-153">0x00000010</span></span>                                   |
| <span data-ttu-id="13a89-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13a89-154">Classes used in</span></span>        | [<span data-ttu-id="13a89-155">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="13a89-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="13a89-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="13a89-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="13a89-157">進入</span><span class="sxs-lookup"><span data-stu-id="13a89-157">Entry</span></span> | <span data-ttu-id="13a89-158">值</span><span class="sxs-lookup"><span data-stu-id="13a89-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a89-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13a89-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a89-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a89-161">System-Only</span></span>            | <span data-ttu-id="13a89-162">否</span><span class="sxs-lookup"><span data-stu-id="13a89-162">False</span></span>                                        |
| <span data-ttu-id="13a89-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13a89-163">Is-Single-Valued</span></span>       | <span data-ttu-id="13a89-164">對</span><span class="sxs-lookup"><span data-stu-id="13a89-164">True</span></span>                                         |
| <span data-ttu-id="13a89-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13a89-165">Is Indexed</span></span>             | <span data-ttu-id="13a89-166">否</span><span class="sxs-lookup"><span data-stu-id="13a89-166">False</span></span>                                        |
| <span data-ttu-id="13a89-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13a89-167">In Global Catalog</span></span>      | <span data-ttu-id="13a89-168">對</span><span class="sxs-lookup"><span data-stu-id="13a89-168">True</span></span>                                         |
| <span data-ttu-id="13a89-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13a89-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a89-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13a89-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a89-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a89-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a89-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a89-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a89-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-173">Search-Flags</span></span>           | <span data-ttu-id="13a89-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a89-174">0x00000000</span></span>                                   |
| <span data-ttu-id="13a89-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-175">System-Flags</span></span>           | <span data-ttu-id="13a89-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a89-176">0x00000010</span></span>                                   |
| <span data-ttu-id="13a89-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13a89-177">Classes used in</span></span>        | [<span data-ttu-id="13a89-178">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="13a89-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="13a89-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13a89-179">Windows Server 2008</span></span>



| <span data-ttu-id="13a89-180">進入</span><span class="sxs-lookup"><span data-stu-id="13a89-180">Entry</span></span> | <span data-ttu-id="13a89-181">值</span><span class="sxs-lookup"><span data-stu-id="13a89-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a89-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13a89-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a89-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a89-184">System-Only</span></span>            | <span data-ttu-id="13a89-185">否</span><span class="sxs-lookup"><span data-stu-id="13a89-185">False</span></span>                                        |
| <span data-ttu-id="13a89-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13a89-186">Is-Single-Valued</span></span>       | <span data-ttu-id="13a89-187">對</span><span class="sxs-lookup"><span data-stu-id="13a89-187">True</span></span>                                         |
| <span data-ttu-id="13a89-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13a89-188">Is Indexed</span></span>             | <span data-ttu-id="13a89-189">否</span><span class="sxs-lookup"><span data-stu-id="13a89-189">False</span></span>                                        |
| <span data-ttu-id="13a89-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13a89-190">In Global Catalog</span></span>      | <span data-ttu-id="13a89-191">對</span><span class="sxs-lookup"><span data-stu-id="13a89-191">True</span></span>                                         |
| <span data-ttu-id="13a89-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13a89-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a89-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13a89-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a89-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a89-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a89-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a89-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a89-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-196">Search-Flags</span></span>           | <span data-ttu-id="13a89-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a89-197">0x00000000</span></span>                                   |
| <span data-ttu-id="13a89-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-198">System-Flags</span></span>           | <span data-ttu-id="13a89-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a89-199">0x00000010</span></span>                                   |
| <span data-ttu-id="13a89-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13a89-200">Classes used in</span></span>        | [<span data-ttu-id="13a89-201">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="13a89-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13a89-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13a89-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13a89-203">進入</span><span class="sxs-lookup"><span data-stu-id="13a89-203">Entry</span></span> | <span data-ttu-id="13a89-204">值</span><span class="sxs-lookup"><span data-stu-id="13a89-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a89-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13a89-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a89-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a89-207">System-Only</span></span>            | <span data-ttu-id="13a89-208">否</span><span class="sxs-lookup"><span data-stu-id="13a89-208">False</span></span>                                        |
| <span data-ttu-id="13a89-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13a89-209">Is-Single-Valued</span></span>       | <span data-ttu-id="13a89-210">對</span><span class="sxs-lookup"><span data-stu-id="13a89-210">True</span></span>                                         |
| <span data-ttu-id="13a89-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13a89-211">Is Indexed</span></span>             | <span data-ttu-id="13a89-212">否</span><span class="sxs-lookup"><span data-stu-id="13a89-212">False</span></span>                                        |
| <span data-ttu-id="13a89-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13a89-213">In Global Catalog</span></span>      | <span data-ttu-id="13a89-214">對</span><span class="sxs-lookup"><span data-stu-id="13a89-214">True</span></span>                                         |
| <span data-ttu-id="13a89-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13a89-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a89-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13a89-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a89-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a89-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a89-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a89-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a89-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-219">Search-Flags</span></span>           | <span data-ttu-id="13a89-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a89-220">0x00000000</span></span>                                   |
| <span data-ttu-id="13a89-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-221">System-Flags</span></span>           | <span data-ttu-id="13a89-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a89-222">0x00000010</span></span>                                   |
| <span data-ttu-id="13a89-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13a89-223">Classes used in</span></span>        | [<span data-ttu-id="13a89-224">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="13a89-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13a89-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13a89-225">Windows Server 2012</span></span>



| <span data-ttu-id="13a89-226">進入</span><span class="sxs-lookup"><span data-stu-id="13a89-226">Entry</span></span> | <span data-ttu-id="13a89-227">值</span><span class="sxs-lookup"><span data-stu-id="13a89-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="13a89-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13a89-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13a89-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="13a89-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="13a89-230">System-Only</span></span>            | <span data-ttu-id="13a89-231">否</span><span class="sxs-lookup"><span data-stu-id="13a89-231">False</span></span>                                        |
| <span data-ttu-id="13a89-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13a89-232">Is-Single-Valued</span></span>       | <span data-ttu-id="13a89-233">對</span><span class="sxs-lookup"><span data-stu-id="13a89-233">True</span></span>                                         |
| <span data-ttu-id="13a89-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13a89-234">Is Indexed</span></span>             | <span data-ttu-id="13a89-235">否</span><span class="sxs-lookup"><span data-stu-id="13a89-235">False</span></span>                                        |
| <span data-ttu-id="13a89-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13a89-236">In Global Catalog</span></span>      | <span data-ttu-id="13a89-237">對</span><span class="sxs-lookup"><span data-stu-id="13a89-237">True</span></span>                                         |
| <span data-ttu-id="13a89-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13a89-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="13a89-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13a89-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="13a89-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13a89-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="13a89-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13a89-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="13a89-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-242">Search-Flags</span></span>           | <span data-ttu-id="13a89-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13a89-243">0x00000000</span></span>                                   |
| <span data-ttu-id="13a89-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13a89-244">System-Flags</span></span>           | <span data-ttu-id="13a89-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="13a89-245">0x00000010</span></span>                                   |
| <span data-ttu-id="13a89-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13a89-246">Classes used in</span></span>        | [<span data-ttu-id="13a89-247">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="13a89-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





