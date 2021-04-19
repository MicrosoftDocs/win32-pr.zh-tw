---
title: MSMQ-Journal 屬性
description: 指出從佇列中取出的訊息是否應該保留在日誌中。
ms.assetid: fb1f73eb-57f4-413f-bd7a-9dfd5e5c797f
ms.tgt_platform: multiple
keywords:
- MSMQ-Journal 屬性 AD 架構
- mSMQJournal 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Journal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a28e7740e41f8209e37345e934a36d10512bc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970474"
---
# <a name="msmq-journal-attribute"></a><span data-ttu-id="69b83-105">MSMQ-Journal 屬性</span><span class="sxs-lookup"><span data-stu-id="69b83-105">MSMQ-Journal attribute</span></span>

<span data-ttu-id="69b83-106">指出從佇列中取出的訊息是否應該保留在日誌中。</span><span class="sxs-lookup"><span data-stu-id="69b83-106">Indicates whether messages retrieved form the queue should be kept in journal.</span></span>



| <span data-ttu-id="69b83-107">進入</span><span class="sxs-lookup"><span data-stu-id="69b83-107">Entry</span></span> | <span data-ttu-id="69b83-108">值</span><span class="sxs-lookup"><span data-stu-id="69b83-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="69b83-109">CN</span><span class="sxs-lookup"><span data-stu-id="69b83-109">CN</span></span>                | <span data-ttu-id="69b83-110">MSMQ-Journal</span><span class="sxs-lookup"><span data-stu-id="69b83-110">MSMQ-Journal</span></span>                         |
| <span data-ttu-id="69b83-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="69b83-111">Ldap-Display-Name</span></span> | <span data-ttu-id="69b83-112">mSMQJournal</span><span class="sxs-lookup"><span data-stu-id="69b83-112">mSMQJournal</span></span>                          |
| <span data-ttu-id="69b83-113">大小</span><span class="sxs-lookup"><span data-stu-id="69b83-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="69b83-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="69b83-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="69b83-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="69b83-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="69b83-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="69b83-116">Attribute-Id</span></span>      | <span data-ttu-id="69b83-117">1.2.840.113556.1.4.918</span><span class="sxs-lookup"><span data-stu-id="69b83-117">1.2.840.113556.1.4.918</span></span>               |
| <span data-ttu-id="69b83-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="69b83-118">System-Id-Guid</span></span>    | <span data-ttu-id="69b83-119">9a0dc321-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="69b83-119">9a0dc321-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="69b83-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="69b83-120">Syntax</span></span>            | [<span data-ttu-id="69b83-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="69b83-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="69b83-122">實作</span><span class="sxs-lookup"><span data-stu-id="69b83-122">Implementations</span></span>

-   [<span data-ttu-id="69b83-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="69b83-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="69b83-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="69b83-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="69b83-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="69b83-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="69b83-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="69b83-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="69b83-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="69b83-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="69b83-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="69b83-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="69b83-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69b83-129">Windows 2000 Server</span></span>



| <span data-ttu-id="69b83-130">進入</span><span class="sxs-lookup"><span data-stu-id="69b83-130">Entry</span></span> | <span data-ttu-id="69b83-131">值</span><span class="sxs-lookup"><span data-stu-id="69b83-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69b83-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69b83-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69b83-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="69b83-134">System-Only</span></span>            | <span data-ttu-id="69b83-135">否</span><span class="sxs-lookup"><span data-stu-id="69b83-135">False</span></span>                                        |
| <span data-ttu-id="69b83-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69b83-136">Is-Single-Valued</span></span>       | <span data-ttu-id="69b83-137">對</span><span class="sxs-lookup"><span data-stu-id="69b83-137">True</span></span>                                         |
| <span data-ttu-id="69b83-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69b83-138">Is Indexed</span></span>             | <span data-ttu-id="69b83-139">否</span><span class="sxs-lookup"><span data-stu-id="69b83-139">False</span></span>                                        |
| <span data-ttu-id="69b83-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69b83-140">In Global Catalog</span></span>      | <span data-ttu-id="69b83-141">對</span><span class="sxs-lookup"><span data-stu-id="69b83-141">True</span></span>                                         |
| <span data-ttu-id="69b83-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69b83-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="69b83-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69b83-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69b83-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69b83-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69b83-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69b83-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69b83-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-146">Search-Flags</span></span>           | <span data-ttu-id="69b83-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69b83-147">0x00000000</span></span>                                   |
| <span data-ttu-id="69b83-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-148">System-Flags</span></span>           | <span data-ttu-id="69b83-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69b83-149">0x00000010</span></span>                                   |
| <span data-ttu-id="69b83-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69b83-150">Classes used in</span></span>        | [<span data-ttu-id="69b83-151">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="69b83-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="69b83-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69b83-152">Windows Server 2003</span></span>



| <span data-ttu-id="69b83-153">進入</span><span class="sxs-lookup"><span data-stu-id="69b83-153">Entry</span></span> | <span data-ttu-id="69b83-154">值</span><span class="sxs-lookup"><span data-stu-id="69b83-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69b83-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69b83-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69b83-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="69b83-157">System-Only</span></span>            | <span data-ttu-id="69b83-158">否</span><span class="sxs-lookup"><span data-stu-id="69b83-158">False</span></span>                                        |
| <span data-ttu-id="69b83-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69b83-159">Is-Single-Valued</span></span>       | <span data-ttu-id="69b83-160">對</span><span class="sxs-lookup"><span data-stu-id="69b83-160">True</span></span>                                         |
| <span data-ttu-id="69b83-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69b83-161">Is Indexed</span></span>             | <span data-ttu-id="69b83-162">否</span><span class="sxs-lookup"><span data-stu-id="69b83-162">False</span></span>                                        |
| <span data-ttu-id="69b83-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69b83-163">In Global Catalog</span></span>      | <span data-ttu-id="69b83-164">對</span><span class="sxs-lookup"><span data-stu-id="69b83-164">True</span></span>                                         |
| <span data-ttu-id="69b83-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69b83-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="69b83-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69b83-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69b83-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69b83-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69b83-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69b83-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69b83-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-169">Search-Flags</span></span>           | <span data-ttu-id="69b83-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69b83-170">0x00000000</span></span>                                   |
| <span data-ttu-id="69b83-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-171">System-Flags</span></span>           | <span data-ttu-id="69b83-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69b83-172">0x00000010</span></span>                                   |
| <span data-ttu-id="69b83-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69b83-173">Classes used in</span></span>        | [<span data-ttu-id="69b83-174">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="69b83-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="69b83-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="69b83-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="69b83-176">進入</span><span class="sxs-lookup"><span data-stu-id="69b83-176">Entry</span></span> | <span data-ttu-id="69b83-177">值</span><span class="sxs-lookup"><span data-stu-id="69b83-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69b83-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69b83-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69b83-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="69b83-180">System-Only</span></span>            | <span data-ttu-id="69b83-181">否</span><span class="sxs-lookup"><span data-stu-id="69b83-181">False</span></span>                                        |
| <span data-ttu-id="69b83-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69b83-182">Is-Single-Valued</span></span>       | <span data-ttu-id="69b83-183">對</span><span class="sxs-lookup"><span data-stu-id="69b83-183">True</span></span>                                         |
| <span data-ttu-id="69b83-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69b83-184">Is Indexed</span></span>             | <span data-ttu-id="69b83-185">否</span><span class="sxs-lookup"><span data-stu-id="69b83-185">False</span></span>                                        |
| <span data-ttu-id="69b83-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69b83-186">In Global Catalog</span></span>      | <span data-ttu-id="69b83-187">對</span><span class="sxs-lookup"><span data-stu-id="69b83-187">True</span></span>                                         |
| <span data-ttu-id="69b83-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69b83-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="69b83-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69b83-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69b83-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69b83-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69b83-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69b83-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69b83-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-192">Search-Flags</span></span>           | <span data-ttu-id="69b83-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69b83-193">0x00000000</span></span>                                   |
| <span data-ttu-id="69b83-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-194">System-Flags</span></span>           | <span data-ttu-id="69b83-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69b83-195">0x00000010</span></span>                                   |
| <span data-ttu-id="69b83-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69b83-196">Classes used in</span></span>        | [<span data-ttu-id="69b83-197">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="69b83-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="69b83-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69b83-198">Windows Server 2008</span></span>



| <span data-ttu-id="69b83-199">進入</span><span class="sxs-lookup"><span data-stu-id="69b83-199">Entry</span></span> | <span data-ttu-id="69b83-200">值</span><span class="sxs-lookup"><span data-stu-id="69b83-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69b83-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69b83-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69b83-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="69b83-203">System-Only</span></span>            | <span data-ttu-id="69b83-204">否</span><span class="sxs-lookup"><span data-stu-id="69b83-204">False</span></span>                                        |
| <span data-ttu-id="69b83-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69b83-205">Is-Single-Valued</span></span>       | <span data-ttu-id="69b83-206">對</span><span class="sxs-lookup"><span data-stu-id="69b83-206">True</span></span>                                         |
| <span data-ttu-id="69b83-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69b83-207">Is Indexed</span></span>             | <span data-ttu-id="69b83-208">否</span><span class="sxs-lookup"><span data-stu-id="69b83-208">False</span></span>                                        |
| <span data-ttu-id="69b83-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69b83-209">In Global Catalog</span></span>      | <span data-ttu-id="69b83-210">對</span><span class="sxs-lookup"><span data-stu-id="69b83-210">True</span></span>                                         |
| <span data-ttu-id="69b83-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69b83-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="69b83-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69b83-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69b83-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69b83-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69b83-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69b83-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69b83-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-215">Search-Flags</span></span>           | <span data-ttu-id="69b83-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69b83-216">0x00000000</span></span>                                   |
| <span data-ttu-id="69b83-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-217">System-Flags</span></span>           | <span data-ttu-id="69b83-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69b83-218">0x00000010</span></span>                                   |
| <span data-ttu-id="69b83-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69b83-219">Classes used in</span></span>        | [<span data-ttu-id="69b83-220">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="69b83-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="69b83-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69b83-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="69b83-222">進入</span><span class="sxs-lookup"><span data-stu-id="69b83-222">Entry</span></span> | <span data-ttu-id="69b83-223">值</span><span class="sxs-lookup"><span data-stu-id="69b83-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69b83-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69b83-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69b83-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="69b83-226">System-Only</span></span>            | <span data-ttu-id="69b83-227">否</span><span class="sxs-lookup"><span data-stu-id="69b83-227">False</span></span>                                        |
| <span data-ttu-id="69b83-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69b83-228">Is-Single-Valued</span></span>       | <span data-ttu-id="69b83-229">對</span><span class="sxs-lookup"><span data-stu-id="69b83-229">True</span></span>                                         |
| <span data-ttu-id="69b83-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69b83-230">Is Indexed</span></span>             | <span data-ttu-id="69b83-231">否</span><span class="sxs-lookup"><span data-stu-id="69b83-231">False</span></span>                                        |
| <span data-ttu-id="69b83-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69b83-232">In Global Catalog</span></span>      | <span data-ttu-id="69b83-233">對</span><span class="sxs-lookup"><span data-stu-id="69b83-233">True</span></span>                                         |
| <span data-ttu-id="69b83-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69b83-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="69b83-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69b83-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69b83-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69b83-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69b83-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69b83-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69b83-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-238">Search-Flags</span></span>           | <span data-ttu-id="69b83-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69b83-239">0x00000000</span></span>                                   |
| <span data-ttu-id="69b83-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-240">System-Flags</span></span>           | <span data-ttu-id="69b83-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69b83-241">0x00000010</span></span>                                   |
| <span data-ttu-id="69b83-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69b83-242">Classes used in</span></span>        | [<span data-ttu-id="69b83-243">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="69b83-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="69b83-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69b83-244">Windows Server 2012</span></span>



| <span data-ttu-id="69b83-245">進入</span><span class="sxs-lookup"><span data-stu-id="69b83-245">Entry</span></span> | <span data-ttu-id="69b83-246">值</span><span class="sxs-lookup"><span data-stu-id="69b83-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="69b83-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="69b83-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="69b83-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="69b83-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="69b83-249">System-Only</span></span>            | <span data-ttu-id="69b83-250">否</span><span class="sxs-lookup"><span data-stu-id="69b83-250">False</span></span>                                        |
| <span data-ttu-id="69b83-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="69b83-251">Is-Single-Valued</span></span>       | <span data-ttu-id="69b83-252">對</span><span class="sxs-lookup"><span data-stu-id="69b83-252">True</span></span>                                         |
| <span data-ttu-id="69b83-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="69b83-253">Is Indexed</span></span>             | <span data-ttu-id="69b83-254">否</span><span class="sxs-lookup"><span data-stu-id="69b83-254">False</span></span>                                        |
| <span data-ttu-id="69b83-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="69b83-255">In Global Catalog</span></span>      | <span data-ttu-id="69b83-256">對</span><span class="sxs-lookup"><span data-stu-id="69b83-256">True</span></span>                                         |
| <span data-ttu-id="69b83-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="69b83-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="69b83-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="69b83-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="69b83-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="69b83-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="69b83-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="69b83-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="69b83-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-261">Search-Flags</span></span>           | <span data-ttu-id="69b83-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="69b83-262">0x00000000</span></span>                                   |
| <span data-ttu-id="69b83-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="69b83-263">System-Flags</span></span>           | <span data-ttu-id="69b83-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69b83-264">0x00000010</span></span>                                   |
| <span data-ttu-id="69b83-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="69b83-265">Classes used in</span></span>        | [<span data-ttu-id="69b83-266">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="69b83-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





