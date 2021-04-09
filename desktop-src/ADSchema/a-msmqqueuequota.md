---
title: MSMQ-佇列-配額屬性
description: 佇列的訊息配額。
ms.assetid: 45a9d6f0-5cd7-414d-97c5-18a7e41a5062
ms.tgt_platform: multiple
keywords:
- MSMQ-佇列-配額屬性 AD 架構
- mSMQQueueQuota 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Queue-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70e2719b6bfe738a0bc6646716582e9dcc72fe7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687211"
---
# <a name="msmq-queue-quota-attribute"></a><span data-ttu-id="ec0e2-105">MSMQ-佇列-配額屬性</span><span class="sxs-lookup"><span data-stu-id="ec0e2-105">MSMQ-Queue-Quota attribute</span></span>

<span data-ttu-id="ec0e2-106">佇列的訊息配額。</span><span class="sxs-lookup"><span data-stu-id="ec0e2-106">A message quota of the queue.</span></span>



| <span data-ttu-id="ec0e2-107">進入</span><span class="sxs-lookup"><span data-stu-id="ec0e2-107">Entry</span></span> | <span data-ttu-id="ec0e2-108">值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ec0e2-109">CN</span><span class="sxs-lookup"><span data-stu-id="ec0e2-109">CN</span></span>                | <span data-ttu-id="ec0e2-110">MSMQ-佇列-配額</span><span class="sxs-lookup"><span data-stu-id="ec0e2-110">MSMQ-Queue-Quota</span></span>                     |
| <span data-ttu-id="ec0e2-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ec0e2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ec0e2-112">mSMQQueueQuota</span><span class="sxs-lookup"><span data-stu-id="ec0e2-112">mSMQQueueQuota</span></span>                       |
| <span data-ttu-id="ec0e2-113">大小</span><span class="sxs-lookup"><span data-stu-id="ec0e2-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="ec0e2-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ec0e2-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ec0e2-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ec0e2-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ec0e2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec0e2-116">Attribute-Id</span></span>      | <span data-ttu-id="ec0e2-117">1.2.840.113556.1.4.962</span><span class="sxs-lookup"><span data-stu-id="ec0e2-117">1.2.840.113556.1.4.962</span></span>               |
| <span data-ttu-id="ec0e2-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ec0e2-118">System-Id-Guid</span></span>    | <span data-ttu-id="ec0e2-119">3f6b8e12-d57f-11d1-90a2-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ec0e2-119">3f6b8e12-d57f-11d1-90a2-00c04fd91ab1</span></span> |
| <span data-ttu-id="ec0e2-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec0e2-120">Syntax</span></span>            | [<span data-ttu-id="ec0e2-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ec0e2-122">實作</span><span class="sxs-lookup"><span data-stu-id="ec0e2-122">Implementations</span></span>

-   [<span data-ttu-id="ec0e2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec0e2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec0e2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec0e2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec0e2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec0e2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec0e2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec0e2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ec0e2-130">進入</span><span class="sxs-lookup"><span data-stu-id="ec0e2-130">Entry</span></span> | <span data-ttu-id="ec0e2-131">值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec0e2-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec0e2-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec0e2-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec0e2-134">System-Only</span></span>            | <span data-ttu-id="ec0e2-135">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-135">False</span></span>                                        |
| <span data-ttu-id="ec0e2-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="ec0e2-137">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-137">True</span></span>                                         |
| <span data-ttu-id="ec0e2-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec0e2-138">Is Indexed</span></span>             | <span data-ttu-id="ec0e2-139">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-139">False</span></span>                                        |
| <span data-ttu-id="ec0e2-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec0e2-140">In Global Catalog</span></span>      | <span data-ttu-id="ec0e2-141">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-141">True</span></span>                                         |
| <span data-ttu-id="ec0e2-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec0e2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec0e2-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec0e2-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec0e2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec0e2-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec0e2-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-146">Search-Flags</span></span>           | <span data-ttu-id="ec0e2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec0e2-147">0x00000000</span></span>                                   |
| <span data-ttu-id="ec0e2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-148">System-Flags</span></span>           | <span data-ttu-id="ec0e2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec0e2-149">0x00000010</span></span>                                   |
| <span data-ttu-id="ec0e2-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec0e2-150">Classes used in</span></span>        | [<span data-ttu-id="ec0e2-151">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec0e2-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec0e2-152">Windows Server 2003</span></span>



| <span data-ttu-id="ec0e2-153">進入</span><span class="sxs-lookup"><span data-stu-id="ec0e2-153">Entry</span></span> | <span data-ttu-id="ec0e2-154">值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec0e2-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec0e2-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec0e2-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec0e2-157">System-Only</span></span>            | <span data-ttu-id="ec0e2-158">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-158">False</span></span>                                        |
| <span data-ttu-id="ec0e2-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-159">Is-Single-Valued</span></span>       | <span data-ttu-id="ec0e2-160">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-160">True</span></span>                                         |
| <span data-ttu-id="ec0e2-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec0e2-161">Is Indexed</span></span>             | <span data-ttu-id="ec0e2-162">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-162">False</span></span>                                        |
| <span data-ttu-id="ec0e2-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec0e2-163">In Global Catalog</span></span>      | <span data-ttu-id="ec0e2-164">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-164">True</span></span>                                         |
| <span data-ttu-id="ec0e2-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec0e2-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec0e2-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec0e2-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec0e2-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec0e2-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec0e2-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-169">Search-Flags</span></span>           | <span data-ttu-id="ec0e2-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec0e2-170">0x00000000</span></span>                                   |
| <span data-ttu-id="ec0e2-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-171">System-Flags</span></span>           | <span data-ttu-id="ec0e2-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec0e2-172">0x00000010</span></span>                                   |
| <span data-ttu-id="ec0e2-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec0e2-173">Classes used in</span></span>        | [<span data-ttu-id="ec0e2-174">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec0e2-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec0e2-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec0e2-176">進入</span><span class="sxs-lookup"><span data-stu-id="ec0e2-176">Entry</span></span> | <span data-ttu-id="ec0e2-177">值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec0e2-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec0e2-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec0e2-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec0e2-180">System-Only</span></span>            | <span data-ttu-id="ec0e2-181">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-181">False</span></span>                                        |
| <span data-ttu-id="ec0e2-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-182">Is-Single-Valued</span></span>       | <span data-ttu-id="ec0e2-183">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-183">True</span></span>                                         |
| <span data-ttu-id="ec0e2-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec0e2-184">Is Indexed</span></span>             | <span data-ttu-id="ec0e2-185">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-185">False</span></span>                                        |
| <span data-ttu-id="ec0e2-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec0e2-186">In Global Catalog</span></span>      | <span data-ttu-id="ec0e2-187">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-187">True</span></span>                                         |
| <span data-ttu-id="ec0e2-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec0e2-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec0e2-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec0e2-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec0e2-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec0e2-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec0e2-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-192">Search-Flags</span></span>           | <span data-ttu-id="ec0e2-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec0e2-193">0x00000000</span></span>                                   |
| <span data-ttu-id="ec0e2-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-194">System-Flags</span></span>           | <span data-ttu-id="ec0e2-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec0e2-195">0x00000010</span></span>                                   |
| <span data-ttu-id="ec0e2-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec0e2-196">Classes used in</span></span>        | [<span data-ttu-id="ec0e2-197">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec0e2-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec0e2-198">Windows Server 2008</span></span>



| <span data-ttu-id="ec0e2-199">進入</span><span class="sxs-lookup"><span data-stu-id="ec0e2-199">Entry</span></span> | <span data-ttu-id="ec0e2-200">值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec0e2-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec0e2-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec0e2-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec0e2-203">System-Only</span></span>            | <span data-ttu-id="ec0e2-204">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-204">False</span></span>                                        |
| <span data-ttu-id="ec0e2-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-205">Is-Single-Valued</span></span>       | <span data-ttu-id="ec0e2-206">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-206">True</span></span>                                         |
| <span data-ttu-id="ec0e2-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec0e2-207">Is Indexed</span></span>             | <span data-ttu-id="ec0e2-208">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-208">False</span></span>                                        |
| <span data-ttu-id="ec0e2-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec0e2-209">In Global Catalog</span></span>      | <span data-ttu-id="ec0e2-210">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-210">True</span></span>                                         |
| <span data-ttu-id="ec0e2-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec0e2-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec0e2-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec0e2-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec0e2-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec0e2-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec0e2-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-215">Search-Flags</span></span>           | <span data-ttu-id="ec0e2-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec0e2-216">0x00000000</span></span>                                   |
| <span data-ttu-id="ec0e2-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-217">System-Flags</span></span>           | <span data-ttu-id="ec0e2-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec0e2-218">0x00000010</span></span>                                   |
| <span data-ttu-id="ec0e2-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec0e2-219">Classes used in</span></span>        | [<span data-ttu-id="ec0e2-220">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec0e2-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec0e2-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec0e2-222">進入</span><span class="sxs-lookup"><span data-stu-id="ec0e2-222">Entry</span></span> | <span data-ttu-id="ec0e2-223">值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec0e2-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec0e2-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec0e2-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec0e2-226">System-Only</span></span>            | <span data-ttu-id="ec0e2-227">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-227">False</span></span>                                        |
| <span data-ttu-id="ec0e2-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-228">Is-Single-Valued</span></span>       | <span data-ttu-id="ec0e2-229">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-229">True</span></span>                                         |
| <span data-ttu-id="ec0e2-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec0e2-230">Is Indexed</span></span>             | <span data-ttu-id="ec0e2-231">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-231">False</span></span>                                        |
| <span data-ttu-id="ec0e2-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec0e2-232">In Global Catalog</span></span>      | <span data-ttu-id="ec0e2-233">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-233">True</span></span>                                         |
| <span data-ttu-id="ec0e2-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec0e2-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec0e2-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec0e2-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec0e2-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec0e2-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec0e2-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-238">Search-Flags</span></span>           | <span data-ttu-id="ec0e2-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec0e2-239">0x00000000</span></span>                                   |
| <span data-ttu-id="ec0e2-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-240">System-Flags</span></span>           | <span data-ttu-id="ec0e2-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec0e2-241">0x00000010</span></span>                                   |
| <span data-ttu-id="ec0e2-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec0e2-242">Classes used in</span></span>        | [<span data-ttu-id="ec0e2-243">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec0e2-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec0e2-244">Windows Server 2012</span></span>



| <span data-ttu-id="ec0e2-245">進入</span><span class="sxs-lookup"><span data-stu-id="ec0e2-245">Entry</span></span> | <span data-ttu-id="ec0e2-246">值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ec0e2-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec0e2-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec0e2-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ec0e2-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec0e2-249">System-Only</span></span>            | <span data-ttu-id="ec0e2-250">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-250">False</span></span>                                        |
| <span data-ttu-id="ec0e2-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec0e2-251">Is-Single-Valued</span></span>       | <span data-ttu-id="ec0e2-252">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-252">True</span></span>                                         |
| <span data-ttu-id="ec0e2-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec0e2-253">Is Indexed</span></span>             | <span data-ttu-id="ec0e2-254">否</span><span class="sxs-lookup"><span data-stu-id="ec0e2-254">False</span></span>                                        |
| <span data-ttu-id="ec0e2-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec0e2-255">In Global Catalog</span></span>      | <span data-ttu-id="ec0e2-256">對</span><span class="sxs-lookup"><span data-stu-id="ec0e2-256">True</span></span>                                         |
| <span data-ttu-id="ec0e2-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec0e2-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec0e2-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec0e2-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ec0e2-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec0e2-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec0e2-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ec0e2-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-261">Search-Flags</span></span>           | <span data-ttu-id="ec0e2-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec0e2-262">0x00000000</span></span>                                   |
| <span data-ttu-id="ec0e2-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec0e2-263">System-Flags</span></span>           | <span data-ttu-id="ec0e2-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec0e2-264">0x00000010</span></span>                                   |
| <span data-ttu-id="ec0e2-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec0e2-265">Classes used in</span></span>        | [<span data-ttu-id="ec0e2-266">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="ec0e2-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





