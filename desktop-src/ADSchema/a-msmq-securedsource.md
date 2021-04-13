---
title: MSMQ 保護的-來源屬性
description: 這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。 它會控制 MSMQ 是否只接受來自安全來源的訊息 (例如，此佇列的 HTTPs) 。
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- MSMQ 保護-來源屬性 AD 架構
- MSMQ-SecuredSource 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509604"
---
# <a name="msmq-secured-source-attribute"></a><span data-ttu-id="b0678-106">MSMQ 保護的-來源屬性</span><span class="sxs-lookup"><span data-stu-id="b0678-106">MSMQ-Secured-Source attribute</span></span>

<span data-ttu-id="b0678-107">這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。</span><span class="sxs-lookup"><span data-stu-id="b0678-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="b0678-108">它會控制 MSMQ 是否只接受來自安全來源的訊息 (例如，此佇列的 HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="b0678-108">It controls whether MSMQ accepts messages only from a secured source (for example, https) for this queue.</span></span>



| <span data-ttu-id="b0678-109">進入</span><span class="sxs-lookup"><span data-stu-id="b0678-109">Entry</span></span> | <span data-ttu-id="b0678-110">值</span><span class="sxs-lookup"><span data-stu-id="b0678-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b0678-111">CN</span><span class="sxs-lookup"><span data-stu-id="b0678-111">CN</span></span>                | <span data-ttu-id="b0678-112">MSMQ 安全-來源</span><span class="sxs-lookup"><span data-stu-id="b0678-112">MSMQ-Secured-Source</span></span>                  |
| <span data-ttu-id="b0678-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b0678-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b0678-114">MSMQ-SecuredSource</span><span class="sxs-lookup"><span data-stu-id="b0678-114">MSMQ-SecuredSource</span></span>                   |
| <span data-ttu-id="b0678-115">大小</span><span class="sxs-lookup"><span data-stu-id="b0678-115">Size</span></span>              | <span data-ttu-id="b0678-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="b0678-116">4 bytes</span></span>                              |
| <span data-ttu-id="b0678-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b0678-117">Update Privilege</span></span>  | <span data-ttu-id="b0678-118">佇列擁有者。</span><span class="sxs-lookup"><span data-stu-id="b0678-118">The queue owner.</span></span>                     |
| <span data-ttu-id="b0678-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b0678-119">Update Frequency</span></span>  | <span data-ttu-id="b0678-120">當佇列建立時。</span><span class="sxs-lookup"><span data-stu-id="b0678-120">When a queue is created.</span></span>             |
| <span data-ttu-id="b0678-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b0678-121">Attribute-Id</span></span>      | <span data-ttu-id="b0678-122">1.2.840.113556.1.4.1713</span><span class="sxs-lookup"><span data-stu-id="b0678-122">1.2.840.113556.1.4.1713</span></span>              |
| <span data-ttu-id="b0678-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b0678-123">System-Id-Guid</span></span>    | <span data-ttu-id="b0678-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span><span class="sxs-lookup"><span data-stu-id="b0678-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span></span> |
| <span data-ttu-id="b0678-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0678-125">Syntax</span></span>            | [<span data-ttu-id="b0678-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b0678-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b0678-127">實作</span><span class="sxs-lookup"><span data-stu-id="b0678-127">Implementations</span></span>

-   [<span data-ttu-id="b0678-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b0678-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b0678-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b0678-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b0678-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b0678-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b0678-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b0678-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b0678-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b0678-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b0678-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0678-133">Windows Server 2003</span></span>



| <span data-ttu-id="b0678-134">進入</span><span class="sxs-lookup"><span data-stu-id="b0678-134">Entry</span></span> | <span data-ttu-id="b0678-135">值</span><span class="sxs-lookup"><span data-stu-id="b0678-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0678-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0678-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0678-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0678-138">System-Only</span></span>            | <span data-ttu-id="b0678-139">否</span><span class="sxs-lookup"><span data-stu-id="b0678-139">False</span></span>                                        |
| <span data-ttu-id="b0678-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0678-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b0678-141">對</span><span class="sxs-lookup"><span data-stu-id="b0678-141">True</span></span>                                         |
| <span data-ttu-id="b0678-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0678-142">Is Indexed</span></span>             | <span data-ttu-id="b0678-143">否</span><span class="sxs-lookup"><span data-stu-id="b0678-143">False</span></span>                                        |
| <span data-ttu-id="b0678-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0678-144">In Global Catalog</span></span>      | <span data-ttu-id="b0678-145">對</span><span class="sxs-lookup"><span data-stu-id="b0678-145">True</span></span>                                         |
| <span data-ttu-id="b0678-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0678-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0678-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0678-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0678-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0678-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0678-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0678-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0678-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-150">Search-Flags</span></span>           | <span data-ttu-id="b0678-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0678-151">0x00000000</span></span>                                   |
| <span data-ttu-id="b0678-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-152">System-Flags</span></span>           | <span data-ttu-id="b0678-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0678-153">0x00000010</span></span>                                   |
| <span data-ttu-id="b0678-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0678-154">Classes used in</span></span>        | [<span data-ttu-id="b0678-155">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b0678-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b0678-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b0678-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b0678-157">進入</span><span class="sxs-lookup"><span data-stu-id="b0678-157">Entry</span></span> | <span data-ttu-id="b0678-158">值</span><span class="sxs-lookup"><span data-stu-id="b0678-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0678-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0678-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0678-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0678-161">System-Only</span></span>            | <span data-ttu-id="b0678-162">否</span><span class="sxs-lookup"><span data-stu-id="b0678-162">False</span></span>                                        |
| <span data-ttu-id="b0678-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0678-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b0678-164">對</span><span class="sxs-lookup"><span data-stu-id="b0678-164">True</span></span>                                         |
| <span data-ttu-id="b0678-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0678-165">Is Indexed</span></span>             | <span data-ttu-id="b0678-166">否</span><span class="sxs-lookup"><span data-stu-id="b0678-166">False</span></span>                                        |
| <span data-ttu-id="b0678-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0678-167">In Global Catalog</span></span>      | <span data-ttu-id="b0678-168">對</span><span class="sxs-lookup"><span data-stu-id="b0678-168">True</span></span>                                         |
| <span data-ttu-id="b0678-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0678-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0678-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0678-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0678-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0678-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0678-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0678-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0678-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-173">Search-Flags</span></span>           | <span data-ttu-id="b0678-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0678-174">0x00000000</span></span>                                   |
| <span data-ttu-id="b0678-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-175">System-Flags</span></span>           | <span data-ttu-id="b0678-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0678-176">0x00000010</span></span>                                   |
| <span data-ttu-id="b0678-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0678-177">Classes used in</span></span>        | [<span data-ttu-id="b0678-178">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b0678-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b0678-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0678-179">Windows Server 2008</span></span>



| <span data-ttu-id="b0678-180">進入</span><span class="sxs-lookup"><span data-stu-id="b0678-180">Entry</span></span> | <span data-ttu-id="b0678-181">值</span><span class="sxs-lookup"><span data-stu-id="b0678-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0678-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0678-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0678-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0678-184">System-Only</span></span>            | <span data-ttu-id="b0678-185">否</span><span class="sxs-lookup"><span data-stu-id="b0678-185">False</span></span>                                        |
| <span data-ttu-id="b0678-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0678-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b0678-187">對</span><span class="sxs-lookup"><span data-stu-id="b0678-187">True</span></span>                                         |
| <span data-ttu-id="b0678-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0678-188">Is Indexed</span></span>             | <span data-ttu-id="b0678-189">否</span><span class="sxs-lookup"><span data-stu-id="b0678-189">False</span></span>                                        |
| <span data-ttu-id="b0678-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0678-190">In Global Catalog</span></span>      | <span data-ttu-id="b0678-191">對</span><span class="sxs-lookup"><span data-stu-id="b0678-191">True</span></span>                                         |
| <span data-ttu-id="b0678-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0678-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0678-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0678-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0678-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0678-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0678-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0678-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0678-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-196">Search-Flags</span></span>           | <span data-ttu-id="b0678-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0678-197">0x00000000</span></span>                                   |
| <span data-ttu-id="b0678-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-198">System-Flags</span></span>           | <span data-ttu-id="b0678-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0678-199">0x00000010</span></span>                                   |
| <span data-ttu-id="b0678-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0678-200">Classes used in</span></span>        | [<span data-ttu-id="b0678-201">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b0678-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b0678-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0678-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b0678-203">進入</span><span class="sxs-lookup"><span data-stu-id="b0678-203">Entry</span></span> | <span data-ttu-id="b0678-204">值</span><span class="sxs-lookup"><span data-stu-id="b0678-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0678-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0678-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0678-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0678-207">System-Only</span></span>            | <span data-ttu-id="b0678-208">否</span><span class="sxs-lookup"><span data-stu-id="b0678-208">False</span></span>                                        |
| <span data-ttu-id="b0678-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0678-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b0678-210">對</span><span class="sxs-lookup"><span data-stu-id="b0678-210">True</span></span>                                         |
| <span data-ttu-id="b0678-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0678-211">Is Indexed</span></span>             | <span data-ttu-id="b0678-212">否</span><span class="sxs-lookup"><span data-stu-id="b0678-212">False</span></span>                                        |
| <span data-ttu-id="b0678-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0678-213">In Global Catalog</span></span>      | <span data-ttu-id="b0678-214">對</span><span class="sxs-lookup"><span data-stu-id="b0678-214">True</span></span>                                         |
| <span data-ttu-id="b0678-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0678-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0678-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0678-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0678-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0678-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0678-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0678-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0678-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-219">Search-Flags</span></span>           | <span data-ttu-id="b0678-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0678-220">0x00000000</span></span>                                   |
| <span data-ttu-id="b0678-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-221">System-Flags</span></span>           | <span data-ttu-id="b0678-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0678-222">0x00000010</span></span>                                   |
| <span data-ttu-id="b0678-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0678-223">Classes used in</span></span>        | [<span data-ttu-id="b0678-224">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b0678-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b0678-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0678-225">Windows Server 2012</span></span>



| <span data-ttu-id="b0678-226">進入</span><span class="sxs-lookup"><span data-stu-id="b0678-226">Entry</span></span> | <span data-ttu-id="b0678-227">值</span><span class="sxs-lookup"><span data-stu-id="b0678-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b0678-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0678-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0678-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b0678-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0678-230">System-Only</span></span>            | <span data-ttu-id="b0678-231">否</span><span class="sxs-lookup"><span data-stu-id="b0678-231">False</span></span>                                        |
| <span data-ttu-id="b0678-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0678-232">Is-Single-Valued</span></span>       | <span data-ttu-id="b0678-233">對</span><span class="sxs-lookup"><span data-stu-id="b0678-233">True</span></span>                                         |
| <span data-ttu-id="b0678-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0678-234">Is Indexed</span></span>             | <span data-ttu-id="b0678-235">否</span><span class="sxs-lookup"><span data-stu-id="b0678-235">False</span></span>                                        |
| <span data-ttu-id="b0678-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0678-236">In Global Catalog</span></span>      | <span data-ttu-id="b0678-237">對</span><span class="sxs-lookup"><span data-stu-id="b0678-237">True</span></span>                                         |
| <span data-ttu-id="b0678-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0678-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0678-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0678-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b0678-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0678-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b0678-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0678-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b0678-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-242">Search-Flags</span></span>           | <span data-ttu-id="b0678-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0678-243">0x00000000</span></span>                                   |
| <span data-ttu-id="b0678-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0678-244">System-Flags</span></span>           | <span data-ttu-id="b0678-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0678-245">0x00000010</span></span>                                   |
| <span data-ttu-id="b0678-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0678-246">Classes used in</span></span>        | [<span data-ttu-id="b0678-247">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b0678-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





