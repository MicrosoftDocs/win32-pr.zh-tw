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
# <a name="msmq-queue-quota-attribute"></a><span data-ttu-id="9d1b5-105">MSMQ-佇列-配額屬性</span><span class="sxs-lookup"><span data-stu-id="9d1b5-105">MSMQ-Queue-Quota attribute</span></span>

<span data-ttu-id="9d1b5-106">佇列的訊息配額。</span><span class="sxs-lookup"><span data-stu-id="9d1b5-106">A message quota of the queue.</span></span>



| <span data-ttu-id="9d1b5-107">進入</span><span class="sxs-lookup"><span data-stu-id="9d1b5-107">Entry</span></span> | <span data-ttu-id="9d1b5-108">值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9d1b5-109">CN</span><span class="sxs-lookup"><span data-stu-id="9d1b5-109">CN</span></span>                | <span data-ttu-id="9d1b5-110">MSMQ-佇列-配額</span><span class="sxs-lookup"><span data-stu-id="9d1b5-110">MSMQ-Queue-Quota</span></span>                     |
| <span data-ttu-id="9d1b5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9d1b5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9d1b5-112">mSMQQueueQuota</span><span class="sxs-lookup"><span data-stu-id="9d1b5-112">mSMQQueueQuota</span></span>                       |
| <span data-ttu-id="9d1b5-113">大小</span><span class="sxs-lookup"><span data-stu-id="9d1b5-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9d1b5-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9d1b5-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9d1b5-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9d1b5-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9d1b5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9d1b5-116">Attribute-Id</span></span>      | <span data-ttu-id="9d1b5-117">1.2.840.113556.1.4.962</span><span class="sxs-lookup"><span data-stu-id="9d1b5-117">1.2.840.113556.1.4.962</span></span>               |
| <span data-ttu-id="9d1b5-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9d1b5-118">System-Id-Guid</span></span>    | <span data-ttu-id="9d1b5-119">3f6b8e12-d57f-11d1-90a2-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="9d1b5-119">3f6b8e12-d57f-11d1-90a2-00c04fd91ab1</span></span> |
| <span data-ttu-id="9d1b5-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d1b5-120">Syntax</span></span>            | [<span data-ttu-id="9d1b5-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="9d1b5-122">實作</span><span class="sxs-lookup"><span data-stu-id="9d1b5-122">Implementations</span></span>

-   [<span data-ttu-id="9d1b5-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9d1b5-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9d1b5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9d1b5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9d1b5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9d1b5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9d1b5-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d1b5-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9d1b5-130">進入</span><span class="sxs-lookup"><span data-stu-id="9d1b5-130">Entry</span></span> | <span data-ttu-id="9d1b5-131">值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d1b5-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d1b5-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d1b5-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d1b5-134">System-Only</span></span>            | <span data-ttu-id="9d1b5-135">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-135">False</span></span>                                        |
| <span data-ttu-id="9d1b5-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9d1b5-137">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-137">True</span></span>                                         |
| <span data-ttu-id="9d1b5-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d1b5-138">Is Indexed</span></span>             | <span data-ttu-id="9d1b5-139">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-139">False</span></span>                                        |
| <span data-ttu-id="9d1b5-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d1b5-140">In Global Catalog</span></span>      | <span data-ttu-id="9d1b5-141">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-141">True</span></span>                                         |
| <span data-ttu-id="9d1b5-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d1b5-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d1b5-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d1b5-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d1b5-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d1b5-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d1b5-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-146">Search-Flags</span></span>           | <span data-ttu-id="9d1b5-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d1b5-147">0x00000000</span></span>                                   |
| <span data-ttu-id="9d1b5-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-148">System-Flags</span></span>           | <span data-ttu-id="9d1b5-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d1b5-149">0x00000010</span></span>                                   |
| <span data-ttu-id="9d1b5-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d1b5-150">Classes used in</span></span>        | [<span data-ttu-id="9d1b5-151">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9d1b5-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d1b5-152">Windows Server 2003</span></span>



| <span data-ttu-id="9d1b5-153">進入</span><span class="sxs-lookup"><span data-stu-id="9d1b5-153">Entry</span></span> | <span data-ttu-id="9d1b5-154">值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d1b5-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d1b5-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d1b5-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d1b5-157">System-Only</span></span>            | <span data-ttu-id="9d1b5-158">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-158">False</span></span>                                        |
| <span data-ttu-id="9d1b5-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9d1b5-160">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-160">True</span></span>                                         |
| <span data-ttu-id="9d1b5-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d1b5-161">Is Indexed</span></span>             | <span data-ttu-id="9d1b5-162">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-162">False</span></span>                                        |
| <span data-ttu-id="9d1b5-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d1b5-163">In Global Catalog</span></span>      | <span data-ttu-id="9d1b5-164">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-164">True</span></span>                                         |
| <span data-ttu-id="9d1b5-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d1b5-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d1b5-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d1b5-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d1b5-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d1b5-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d1b5-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-169">Search-Flags</span></span>           | <span data-ttu-id="9d1b5-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d1b5-170">0x00000000</span></span>                                   |
| <span data-ttu-id="9d1b5-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-171">System-Flags</span></span>           | <span data-ttu-id="9d1b5-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d1b5-172">0x00000010</span></span>                                   |
| <span data-ttu-id="9d1b5-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d1b5-173">Classes used in</span></span>        | [<span data-ttu-id="9d1b5-174">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9d1b5-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9d1b5-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9d1b5-176">進入</span><span class="sxs-lookup"><span data-stu-id="9d1b5-176">Entry</span></span> | <span data-ttu-id="9d1b5-177">值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d1b5-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d1b5-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d1b5-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d1b5-180">System-Only</span></span>            | <span data-ttu-id="9d1b5-181">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-181">False</span></span>                                        |
| <span data-ttu-id="9d1b5-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9d1b5-183">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-183">True</span></span>                                         |
| <span data-ttu-id="9d1b5-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d1b5-184">Is Indexed</span></span>             | <span data-ttu-id="9d1b5-185">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-185">False</span></span>                                        |
| <span data-ttu-id="9d1b5-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d1b5-186">In Global Catalog</span></span>      | <span data-ttu-id="9d1b5-187">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-187">True</span></span>                                         |
| <span data-ttu-id="9d1b5-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d1b5-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d1b5-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d1b5-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d1b5-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d1b5-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d1b5-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-192">Search-Flags</span></span>           | <span data-ttu-id="9d1b5-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d1b5-193">0x00000000</span></span>                                   |
| <span data-ttu-id="9d1b5-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-194">System-Flags</span></span>           | <span data-ttu-id="9d1b5-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d1b5-195">0x00000010</span></span>                                   |
| <span data-ttu-id="9d1b5-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d1b5-196">Classes used in</span></span>        | [<span data-ttu-id="9d1b5-197">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9d1b5-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d1b5-198">Windows Server 2008</span></span>



| <span data-ttu-id="9d1b5-199">進入</span><span class="sxs-lookup"><span data-stu-id="9d1b5-199">Entry</span></span> | <span data-ttu-id="9d1b5-200">值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d1b5-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d1b5-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d1b5-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d1b5-203">System-Only</span></span>            | <span data-ttu-id="9d1b5-204">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-204">False</span></span>                                        |
| <span data-ttu-id="9d1b5-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9d1b5-206">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-206">True</span></span>                                         |
| <span data-ttu-id="9d1b5-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d1b5-207">Is Indexed</span></span>             | <span data-ttu-id="9d1b5-208">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-208">False</span></span>                                        |
| <span data-ttu-id="9d1b5-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d1b5-209">In Global Catalog</span></span>      | <span data-ttu-id="9d1b5-210">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-210">True</span></span>                                         |
| <span data-ttu-id="9d1b5-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d1b5-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d1b5-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d1b5-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d1b5-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d1b5-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d1b5-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-215">Search-Flags</span></span>           | <span data-ttu-id="9d1b5-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d1b5-216">0x00000000</span></span>                                   |
| <span data-ttu-id="9d1b5-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-217">System-Flags</span></span>           | <span data-ttu-id="9d1b5-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d1b5-218">0x00000010</span></span>                                   |
| <span data-ttu-id="9d1b5-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d1b5-219">Classes used in</span></span>        | [<span data-ttu-id="9d1b5-220">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9d1b5-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d1b5-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9d1b5-222">進入</span><span class="sxs-lookup"><span data-stu-id="9d1b5-222">Entry</span></span> | <span data-ttu-id="9d1b5-223">值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d1b5-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d1b5-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d1b5-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d1b5-226">System-Only</span></span>            | <span data-ttu-id="9d1b5-227">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-227">False</span></span>                                        |
| <span data-ttu-id="9d1b5-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9d1b5-229">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-229">True</span></span>                                         |
| <span data-ttu-id="9d1b5-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d1b5-230">Is Indexed</span></span>             | <span data-ttu-id="9d1b5-231">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-231">False</span></span>                                        |
| <span data-ttu-id="9d1b5-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d1b5-232">In Global Catalog</span></span>      | <span data-ttu-id="9d1b5-233">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-233">True</span></span>                                         |
| <span data-ttu-id="9d1b5-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d1b5-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d1b5-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d1b5-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d1b5-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d1b5-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d1b5-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-238">Search-Flags</span></span>           | <span data-ttu-id="9d1b5-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d1b5-239">0x00000000</span></span>                                   |
| <span data-ttu-id="9d1b5-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-240">System-Flags</span></span>           | <span data-ttu-id="9d1b5-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d1b5-241">0x00000010</span></span>                                   |
| <span data-ttu-id="9d1b5-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d1b5-242">Classes used in</span></span>        | [<span data-ttu-id="9d1b5-243">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9d1b5-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d1b5-244">Windows Server 2012</span></span>



| <span data-ttu-id="9d1b5-245">進入</span><span class="sxs-lookup"><span data-stu-id="9d1b5-245">Entry</span></span> | <span data-ttu-id="9d1b5-246">值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9d1b5-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9d1b5-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9d1b5-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9d1b5-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9d1b5-249">System-Only</span></span>            | <span data-ttu-id="9d1b5-250">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-250">False</span></span>                                        |
| <span data-ttu-id="9d1b5-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9d1b5-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9d1b5-252">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-252">True</span></span>                                         |
| <span data-ttu-id="9d1b5-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9d1b5-253">Is Indexed</span></span>             | <span data-ttu-id="9d1b5-254">否</span><span class="sxs-lookup"><span data-stu-id="9d1b5-254">False</span></span>                                        |
| <span data-ttu-id="9d1b5-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9d1b5-255">In Global Catalog</span></span>      | <span data-ttu-id="9d1b5-256">對</span><span class="sxs-lookup"><span data-stu-id="9d1b5-256">True</span></span>                                         |
| <span data-ttu-id="9d1b5-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9d1b5-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9d1b5-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9d1b5-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9d1b5-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9d1b5-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9d1b5-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9d1b5-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-261">Search-Flags</span></span>           | <span data-ttu-id="9d1b5-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9d1b5-262">0x00000000</span></span>                                   |
| <span data-ttu-id="9d1b5-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9d1b5-263">System-Flags</span></span>           | <span data-ttu-id="9d1b5-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9d1b5-264">0x00000010</span></span>                                   |
| <span data-ttu-id="9d1b5-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9d1b5-265">Classes used in</span></span>        | [<span data-ttu-id="9d1b5-266">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="9d1b5-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





