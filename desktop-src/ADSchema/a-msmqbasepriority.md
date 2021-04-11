---
title: MSMQ-基底優先順序屬性
description: 傳送至此佇列之訊息的基本優先權。
ms.assetid: bcb2b13d-67f0-44d1-ae2c-129528fdf36d
ms.tgt_platform: multiple
keywords:
- MSMQ-基底優先順序屬性 AD 架構
- mSMQBasePriority 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Base-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ea41f559b6fe9c9ef3dd43aed8ad5df3809702
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935401"
---
# <a name="msmq-base-priority-attribute"></a><span data-ttu-id="95938-105">MSMQ-基底優先順序屬性</span><span class="sxs-lookup"><span data-stu-id="95938-105">MSMQ-Base-Priority attribute</span></span>

<span data-ttu-id="95938-106">傳送至此佇列之訊息的基本優先權。</span><span class="sxs-lookup"><span data-stu-id="95938-106">The base priority of messages transmitted to this queue.</span></span>



| <span data-ttu-id="95938-107">進入</span><span class="sxs-lookup"><span data-stu-id="95938-107">Entry</span></span> | <span data-ttu-id="95938-108">值</span><span class="sxs-lookup"><span data-stu-id="95938-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="95938-109">CN</span><span class="sxs-lookup"><span data-stu-id="95938-109">CN</span></span>                | <span data-ttu-id="95938-110">MSMQ-基本優先順序</span><span class="sxs-lookup"><span data-stu-id="95938-110">MSMQ-Base-Priority</span></span>                   |
| <span data-ttu-id="95938-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="95938-111">Ldap-Display-Name</span></span> | <span data-ttu-id="95938-112">mSMQBasePriority</span><span class="sxs-lookup"><span data-stu-id="95938-112">mSMQBasePriority</span></span>                     |
| <span data-ttu-id="95938-113">大小</span><span class="sxs-lookup"><span data-stu-id="95938-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="95938-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="95938-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="95938-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="95938-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="95938-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="95938-116">Attribute-Id</span></span>      | <span data-ttu-id="95938-117">1.2.840.113556.1.4.920</span><span class="sxs-lookup"><span data-stu-id="95938-117">1.2.840.113556.1.4.920</span></span>               |
| <span data-ttu-id="95938-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="95938-118">System-Id-Guid</span></span>    | <span data-ttu-id="95938-119">9a0dc323-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="95938-119">9a0dc323-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="95938-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="95938-120">Syntax</span></span>            | [<span data-ttu-id="95938-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="95938-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="95938-122">實作</span><span class="sxs-lookup"><span data-stu-id="95938-122">Implementations</span></span>

-   [<span data-ttu-id="95938-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="95938-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="95938-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="95938-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="95938-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="95938-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="95938-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="95938-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="95938-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="95938-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="95938-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="95938-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="95938-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95938-129">Windows 2000 Server</span></span>



| <span data-ttu-id="95938-130">進入</span><span class="sxs-lookup"><span data-stu-id="95938-130">Entry</span></span> | <span data-ttu-id="95938-131">值</span><span class="sxs-lookup"><span data-stu-id="95938-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="95938-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95938-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95938-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="95938-134">System-Only</span></span>            | <span data-ttu-id="95938-135">否</span><span class="sxs-lookup"><span data-stu-id="95938-135">False</span></span>                                        |
| <span data-ttu-id="95938-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95938-136">Is-Single-Valued</span></span>       | <span data-ttu-id="95938-137">對</span><span class="sxs-lookup"><span data-stu-id="95938-137">True</span></span>                                         |
| <span data-ttu-id="95938-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95938-138">Is Indexed</span></span>             | <span data-ttu-id="95938-139">否</span><span class="sxs-lookup"><span data-stu-id="95938-139">False</span></span>                                        |
| <span data-ttu-id="95938-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95938-140">In Global Catalog</span></span>      | <span data-ttu-id="95938-141">對</span><span class="sxs-lookup"><span data-stu-id="95938-141">True</span></span>                                         |
| <span data-ttu-id="95938-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95938-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="95938-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95938-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="95938-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95938-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="95938-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95938-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="95938-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-146">Search-Flags</span></span>           | <span data-ttu-id="95938-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95938-147">0x00000000</span></span>                                   |
| <span data-ttu-id="95938-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-148">System-Flags</span></span>           | <span data-ttu-id="95938-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95938-149">0x00000010</span></span>                                   |
| <span data-ttu-id="95938-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95938-150">Classes used in</span></span>        | [<span data-ttu-id="95938-151">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="95938-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="95938-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95938-152">Windows Server 2003</span></span>



| <span data-ttu-id="95938-153">進入</span><span class="sxs-lookup"><span data-stu-id="95938-153">Entry</span></span> | <span data-ttu-id="95938-154">值</span><span class="sxs-lookup"><span data-stu-id="95938-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="95938-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95938-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95938-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="95938-157">System-Only</span></span>            | <span data-ttu-id="95938-158">否</span><span class="sxs-lookup"><span data-stu-id="95938-158">False</span></span>                                        |
| <span data-ttu-id="95938-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95938-159">Is-Single-Valued</span></span>       | <span data-ttu-id="95938-160">對</span><span class="sxs-lookup"><span data-stu-id="95938-160">True</span></span>                                         |
| <span data-ttu-id="95938-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95938-161">Is Indexed</span></span>             | <span data-ttu-id="95938-162">否</span><span class="sxs-lookup"><span data-stu-id="95938-162">False</span></span>                                        |
| <span data-ttu-id="95938-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95938-163">In Global Catalog</span></span>      | <span data-ttu-id="95938-164">對</span><span class="sxs-lookup"><span data-stu-id="95938-164">True</span></span>                                         |
| <span data-ttu-id="95938-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95938-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="95938-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95938-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="95938-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95938-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="95938-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95938-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="95938-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-169">Search-Flags</span></span>           | <span data-ttu-id="95938-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95938-170">0x00000000</span></span>                                   |
| <span data-ttu-id="95938-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-171">System-Flags</span></span>           | <span data-ttu-id="95938-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95938-172">0x00000010</span></span>                                   |
| <span data-ttu-id="95938-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95938-173">Classes used in</span></span>        | [<span data-ttu-id="95938-174">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="95938-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="95938-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="95938-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="95938-176">進入</span><span class="sxs-lookup"><span data-stu-id="95938-176">Entry</span></span> | <span data-ttu-id="95938-177">值</span><span class="sxs-lookup"><span data-stu-id="95938-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="95938-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95938-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95938-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="95938-180">System-Only</span></span>            | <span data-ttu-id="95938-181">否</span><span class="sxs-lookup"><span data-stu-id="95938-181">False</span></span>                                        |
| <span data-ttu-id="95938-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95938-182">Is-Single-Valued</span></span>       | <span data-ttu-id="95938-183">對</span><span class="sxs-lookup"><span data-stu-id="95938-183">True</span></span>                                         |
| <span data-ttu-id="95938-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95938-184">Is Indexed</span></span>             | <span data-ttu-id="95938-185">否</span><span class="sxs-lookup"><span data-stu-id="95938-185">False</span></span>                                        |
| <span data-ttu-id="95938-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95938-186">In Global Catalog</span></span>      | <span data-ttu-id="95938-187">對</span><span class="sxs-lookup"><span data-stu-id="95938-187">True</span></span>                                         |
| <span data-ttu-id="95938-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95938-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="95938-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95938-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="95938-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95938-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="95938-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95938-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="95938-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-192">Search-Flags</span></span>           | <span data-ttu-id="95938-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95938-193">0x00000000</span></span>                                   |
| <span data-ttu-id="95938-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-194">System-Flags</span></span>           | <span data-ttu-id="95938-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95938-195">0x00000010</span></span>                                   |
| <span data-ttu-id="95938-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95938-196">Classes used in</span></span>        | [<span data-ttu-id="95938-197">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="95938-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="95938-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95938-198">Windows Server 2008</span></span>



| <span data-ttu-id="95938-199">進入</span><span class="sxs-lookup"><span data-stu-id="95938-199">Entry</span></span> | <span data-ttu-id="95938-200">值</span><span class="sxs-lookup"><span data-stu-id="95938-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="95938-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95938-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95938-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="95938-203">System-Only</span></span>            | <span data-ttu-id="95938-204">否</span><span class="sxs-lookup"><span data-stu-id="95938-204">False</span></span>                                        |
| <span data-ttu-id="95938-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95938-205">Is-Single-Valued</span></span>       | <span data-ttu-id="95938-206">對</span><span class="sxs-lookup"><span data-stu-id="95938-206">True</span></span>                                         |
| <span data-ttu-id="95938-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95938-207">Is Indexed</span></span>             | <span data-ttu-id="95938-208">否</span><span class="sxs-lookup"><span data-stu-id="95938-208">False</span></span>                                        |
| <span data-ttu-id="95938-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95938-209">In Global Catalog</span></span>      | <span data-ttu-id="95938-210">對</span><span class="sxs-lookup"><span data-stu-id="95938-210">True</span></span>                                         |
| <span data-ttu-id="95938-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95938-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="95938-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95938-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="95938-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95938-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="95938-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95938-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="95938-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-215">Search-Flags</span></span>           | <span data-ttu-id="95938-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95938-216">0x00000000</span></span>                                   |
| <span data-ttu-id="95938-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-217">System-Flags</span></span>           | <span data-ttu-id="95938-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95938-218">0x00000010</span></span>                                   |
| <span data-ttu-id="95938-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95938-219">Classes used in</span></span>        | [<span data-ttu-id="95938-220">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="95938-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="95938-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="95938-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="95938-222">進入</span><span class="sxs-lookup"><span data-stu-id="95938-222">Entry</span></span> | <span data-ttu-id="95938-223">值</span><span class="sxs-lookup"><span data-stu-id="95938-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="95938-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95938-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95938-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="95938-226">System-Only</span></span>            | <span data-ttu-id="95938-227">否</span><span class="sxs-lookup"><span data-stu-id="95938-227">False</span></span>                                        |
| <span data-ttu-id="95938-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95938-228">Is-Single-Valued</span></span>       | <span data-ttu-id="95938-229">對</span><span class="sxs-lookup"><span data-stu-id="95938-229">True</span></span>                                         |
| <span data-ttu-id="95938-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95938-230">Is Indexed</span></span>             | <span data-ttu-id="95938-231">否</span><span class="sxs-lookup"><span data-stu-id="95938-231">False</span></span>                                        |
| <span data-ttu-id="95938-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95938-232">In Global Catalog</span></span>      | <span data-ttu-id="95938-233">對</span><span class="sxs-lookup"><span data-stu-id="95938-233">True</span></span>                                         |
| <span data-ttu-id="95938-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95938-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="95938-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95938-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="95938-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95938-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="95938-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95938-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="95938-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-238">Search-Flags</span></span>           | <span data-ttu-id="95938-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95938-239">0x00000000</span></span>                                   |
| <span data-ttu-id="95938-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-240">System-Flags</span></span>           | <span data-ttu-id="95938-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95938-241">0x00000010</span></span>                                   |
| <span data-ttu-id="95938-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95938-242">Classes used in</span></span>        | [<span data-ttu-id="95938-243">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="95938-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="95938-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95938-244">Windows Server 2012</span></span>



| <span data-ttu-id="95938-245">進入</span><span class="sxs-lookup"><span data-stu-id="95938-245">Entry</span></span> | <span data-ttu-id="95938-246">值</span><span class="sxs-lookup"><span data-stu-id="95938-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="95938-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="95938-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95938-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="95938-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="95938-249">System-Only</span></span>            | <span data-ttu-id="95938-250">否</span><span class="sxs-lookup"><span data-stu-id="95938-250">False</span></span>                                        |
| <span data-ttu-id="95938-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="95938-251">Is-Single-Valued</span></span>       | <span data-ttu-id="95938-252">對</span><span class="sxs-lookup"><span data-stu-id="95938-252">True</span></span>                                         |
| <span data-ttu-id="95938-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="95938-253">Is Indexed</span></span>             | <span data-ttu-id="95938-254">否</span><span class="sxs-lookup"><span data-stu-id="95938-254">False</span></span>                                        |
| <span data-ttu-id="95938-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="95938-255">In Global Catalog</span></span>      | <span data-ttu-id="95938-256">對</span><span class="sxs-lookup"><span data-stu-id="95938-256">True</span></span>                                         |
| <span data-ttu-id="95938-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="95938-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="95938-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="95938-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="95938-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95938-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="95938-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95938-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="95938-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-261">Search-Flags</span></span>           | <span data-ttu-id="95938-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95938-262">0x00000000</span></span>                                   |
| <span data-ttu-id="95938-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95938-263">System-Flags</span></span>           | <span data-ttu-id="95938-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95938-264">0x00000010</span></span>                                   |
| <span data-ttu-id="95938-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="95938-265">Classes used in</span></span>        | [<span data-ttu-id="95938-266">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="95938-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





