---
title: Seq-Notification 屬性
description: 此屬性包含每日遞增的計數器。 此計數器值會提供給連結追蹤服務，這會將值新增至其磁片區，並在重新整理時連結原始程式檔。 網域控制站會維護此值。
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- Seq-Notification 屬性 AD 架構
- seqNotification 屬性 AD 架構
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fc3abc61a8102ced02c87897d5e7a4f706dbbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107537"
---
# <a name="seq-notification-attribute"></a><span data-ttu-id="7e296-107">Seq-Notification 屬性</span><span class="sxs-lookup"><span data-stu-id="7e296-107">Seq-Notification attribute</span></span>

<span data-ttu-id="7e296-108">此屬性包含每日遞增的計數器。</span><span class="sxs-lookup"><span data-stu-id="7e296-108">This attribute contains a counter that is incremented daily.</span></span> <span data-ttu-id="7e296-109">此計數器值會提供給連結追蹤服務，這會將值新增至其磁片區，並在重新整理時連結原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="7e296-109">This counter value is given to the link tracking service which adds the value to its volumes and link source files when they are refreshed.</span></span> <span data-ttu-id="7e296-110">網域控制站會維護此值。</span><span class="sxs-lookup"><span data-stu-id="7e296-110">The domain controller maintains this value.</span></span>



| <span data-ttu-id="7e296-111">進入</span><span class="sxs-lookup"><span data-stu-id="7e296-111">Entry</span></span> | <span data-ttu-id="7e296-112">值</span><span class="sxs-lookup"><span data-stu-id="7e296-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7e296-113">CN</span><span class="sxs-lookup"><span data-stu-id="7e296-113">CN</span></span>                | <span data-ttu-id="7e296-114">Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="7e296-114">Seq-Notification</span></span>                     |
| <span data-ttu-id="7e296-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7e296-115">Ldap-Display-Name</span></span> | <span data-ttu-id="7e296-116">seqNotification</span><span class="sxs-lookup"><span data-stu-id="7e296-116">seqNotification</span></span>                      |
| <span data-ttu-id="7e296-117">大小</span><span class="sxs-lookup"><span data-stu-id="7e296-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="7e296-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7e296-118">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7e296-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7e296-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7e296-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e296-120">Attribute-Id</span></span>      | <span data-ttu-id="7e296-121">1.2.840.113556.1.4.504</span><span class="sxs-lookup"><span data-stu-id="7e296-121">1.2.840.113556.1.4.504</span></span>               |
| <span data-ttu-id="7e296-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7e296-122">System-Id-Guid</span></span>    | <span data-ttu-id="7e296-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7e296-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="7e296-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e296-124">Syntax</span></span>            | [<span data-ttu-id="7e296-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="7e296-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7e296-126">實作</span><span class="sxs-lookup"><span data-stu-id="7e296-126">Implementations</span></span>

-   [<span data-ttu-id="7e296-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e296-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e296-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e296-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e296-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e296-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e296-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e296-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e296-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e296-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e296-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e296-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e296-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e296-133">Windows 2000 Server</span></span>



| <span data-ttu-id="7e296-134">進入</span><span class="sxs-lookup"><span data-stu-id="7e296-134">Entry</span></span> | <span data-ttu-id="7e296-135">值</span><span class="sxs-lookup"><span data-stu-id="7e296-135">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e296-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e296-136">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e296-137">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e296-138">System-Only</span></span>            | <span data-ttu-id="7e296-139">否</span><span class="sxs-lookup"><span data-stu-id="7e296-139">False</span></span>                                                          |
| <span data-ttu-id="7e296-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e296-140">Is-Single-Valued</span></span>       | <span data-ttu-id="7e296-141">對</span><span class="sxs-lookup"><span data-stu-id="7e296-141">True</span></span>                                                           |
| <span data-ttu-id="7e296-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e296-142">Is Indexed</span></span>             | <span data-ttu-id="7e296-143">否</span><span class="sxs-lookup"><span data-stu-id="7e296-143">False</span></span>                                                          |
| <span data-ttu-id="7e296-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e296-144">In Global Catalog</span></span>      | <span data-ttu-id="7e296-145">否</span><span class="sxs-lookup"><span data-stu-id="7e296-145">False</span></span>                                                          |
| <span data-ttu-id="7e296-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e296-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e296-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e296-147">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e296-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e296-148">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e296-149">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-150">Search-Flags</span></span>           | <span data-ttu-id="7e296-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e296-151">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e296-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-152">System-Flags</span></span>           | <span data-ttu-id="7e296-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e296-153">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e296-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e296-154">Classes used in</span></span>        | [<span data-ttu-id="7e296-155">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="7e296-155">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e296-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e296-156">Windows Server 2003</span></span>



| <span data-ttu-id="7e296-157">進入</span><span class="sxs-lookup"><span data-stu-id="7e296-157">Entry</span></span> | <span data-ttu-id="7e296-158">值</span><span class="sxs-lookup"><span data-stu-id="7e296-158">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e296-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e296-159">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e296-160">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e296-161">System-Only</span></span>            | <span data-ttu-id="7e296-162">否</span><span class="sxs-lookup"><span data-stu-id="7e296-162">False</span></span>                                                          |
| <span data-ttu-id="7e296-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e296-163">Is-Single-Valued</span></span>       | <span data-ttu-id="7e296-164">對</span><span class="sxs-lookup"><span data-stu-id="7e296-164">True</span></span>                                                           |
| <span data-ttu-id="7e296-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e296-165">Is Indexed</span></span>             | <span data-ttu-id="7e296-166">否</span><span class="sxs-lookup"><span data-stu-id="7e296-166">False</span></span>                                                          |
| <span data-ttu-id="7e296-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e296-167">In Global Catalog</span></span>      | <span data-ttu-id="7e296-168">否</span><span class="sxs-lookup"><span data-stu-id="7e296-168">False</span></span>                                                          |
| <span data-ttu-id="7e296-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e296-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e296-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e296-170">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e296-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e296-171">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e296-172">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-173">Search-Flags</span></span>           | <span data-ttu-id="7e296-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e296-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e296-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-175">System-Flags</span></span>           | <span data-ttu-id="7e296-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e296-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e296-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e296-177">Classes used in</span></span>        | [<span data-ttu-id="7e296-178">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="7e296-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e296-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e296-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e296-180">進入</span><span class="sxs-lookup"><span data-stu-id="7e296-180">Entry</span></span> | <span data-ttu-id="7e296-181">值</span><span class="sxs-lookup"><span data-stu-id="7e296-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e296-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e296-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e296-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e296-184">System-Only</span></span>            | <span data-ttu-id="7e296-185">否</span><span class="sxs-lookup"><span data-stu-id="7e296-185">False</span></span>                                                          |
| <span data-ttu-id="7e296-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e296-186">Is-Single-Valued</span></span>       | <span data-ttu-id="7e296-187">對</span><span class="sxs-lookup"><span data-stu-id="7e296-187">True</span></span>                                                           |
| <span data-ttu-id="7e296-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e296-188">Is Indexed</span></span>             | <span data-ttu-id="7e296-189">否</span><span class="sxs-lookup"><span data-stu-id="7e296-189">False</span></span>                                                          |
| <span data-ttu-id="7e296-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e296-190">In Global Catalog</span></span>      | <span data-ttu-id="7e296-191">否</span><span class="sxs-lookup"><span data-stu-id="7e296-191">False</span></span>                                                          |
| <span data-ttu-id="7e296-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e296-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e296-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e296-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e296-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e296-194">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e296-195">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-196">Search-Flags</span></span>           | <span data-ttu-id="7e296-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e296-197">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e296-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-198">System-Flags</span></span>           | <span data-ttu-id="7e296-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e296-199">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e296-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e296-200">Classes used in</span></span>        | [<span data-ttu-id="7e296-201">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="7e296-201">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e296-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e296-202">Windows Server 2008</span></span>



| <span data-ttu-id="7e296-203">進入</span><span class="sxs-lookup"><span data-stu-id="7e296-203">Entry</span></span> | <span data-ttu-id="7e296-204">值</span><span class="sxs-lookup"><span data-stu-id="7e296-204">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e296-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e296-205">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e296-206">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e296-207">System-Only</span></span>            | <span data-ttu-id="7e296-208">否</span><span class="sxs-lookup"><span data-stu-id="7e296-208">False</span></span>                                                          |
| <span data-ttu-id="7e296-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e296-209">Is-Single-Valued</span></span>       | <span data-ttu-id="7e296-210">對</span><span class="sxs-lookup"><span data-stu-id="7e296-210">True</span></span>                                                           |
| <span data-ttu-id="7e296-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e296-211">Is Indexed</span></span>             | <span data-ttu-id="7e296-212">否</span><span class="sxs-lookup"><span data-stu-id="7e296-212">False</span></span>                                                          |
| <span data-ttu-id="7e296-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e296-213">In Global Catalog</span></span>      | <span data-ttu-id="7e296-214">否</span><span class="sxs-lookup"><span data-stu-id="7e296-214">False</span></span>                                                          |
| <span data-ttu-id="7e296-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e296-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e296-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e296-216">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e296-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e296-217">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e296-218">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-219">Search-Flags</span></span>           | <span data-ttu-id="7e296-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e296-220">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e296-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-221">System-Flags</span></span>           | <span data-ttu-id="7e296-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e296-222">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e296-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e296-223">Classes used in</span></span>        | [<span data-ttu-id="7e296-224">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="7e296-224">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e296-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e296-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e296-226">進入</span><span class="sxs-lookup"><span data-stu-id="7e296-226">Entry</span></span> | <span data-ttu-id="7e296-227">值</span><span class="sxs-lookup"><span data-stu-id="7e296-227">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e296-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e296-228">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e296-229">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e296-230">System-Only</span></span>            | <span data-ttu-id="7e296-231">否</span><span class="sxs-lookup"><span data-stu-id="7e296-231">False</span></span>                                                          |
| <span data-ttu-id="7e296-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e296-232">Is-Single-Valued</span></span>       | <span data-ttu-id="7e296-233">對</span><span class="sxs-lookup"><span data-stu-id="7e296-233">True</span></span>                                                           |
| <span data-ttu-id="7e296-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e296-234">Is Indexed</span></span>             | <span data-ttu-id="7e296-235">否</span><span class="sxs-lookup"><span data-stu-id="7e296-235">False</span></span>                                                          |
| <span data-ttu-id="7e296-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e296-236">In Global Catalog</span></span>      | <span data-ttu-id="7e296-237">否</span><span class="sxs-lookup"><span data-stu-id="7e296-237">False</span></span>                                                          |
| <span data-ttu-id="7e296-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e296-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e296-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e296-239">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e296-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e296-240">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e296-241">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-242">Search-Flags</span></span>           | <span data-ttu-id="7e296-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e296-243">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e296-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-244">System-Flags</span></span>           | <span data-ttu-id="7e296-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e296-245">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e296-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e296-246">Classes used in</span></span>        | [<span data-ttu-id="7e296-247">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="7e296-247">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e296-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e296-248">Windows Server 2012</span></span>



| <span data-ttu-id="7e296-249">進入</span><span class="sxs-lookup"><span data-stu-id="7e296-249">Entry</span></span> | <span data-ttu-id="7e296-250">值</span><span class="sxs-lookup"><span data-stu-id="7e296-250">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7e296-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e296-251">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e296-252">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="7e296-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e296-253">System-Only</span></span>            | <span data-ttu-id="7e296-254">否</span><span class="sxs-lookup"><span data-stu-id="7e296-254">False</span></span>                                                          |
| <span data-ttu-id="7e296-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e296-255">Is-Single-Valued</span></span>       | <span data-ttu-id="7e296-256">對</span><span class="sxs-lookup"><span data-stu-id="7e296-256">True</span></span>                                                           |
| <span data-ttu-id="7e296-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e296-257">Is Indexed</span></span>             | <span data-ttu-id="7e296-258">否</span><span class="sxs-lookup"><span data-stu-id="7e296-258">False</span></span>                                                          |
| <span data-ttu-id="7e296-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e296-259">In Global Catalog</span></span>      | <span data-ttu-id="7e296-260">否</span><span class="sxs-lookup"><span data-stu-id="7e296-260">False</span></span>                                                          |
| <span data-ttu-id="7e296-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e296-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e296-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e296-262">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="7e296-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e296-263">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e296-264">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="7e296-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-265">Search-Flags</span></span>           | <span data-ttu-id="7e296-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e296-266">0x00000000</span></span>                                                     |
| <span data-ttu-id="7e296-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e296-267">System-Flags</span></span>           | <span data-ttu-id="7e296-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e296-268">0x00000010</span></span>                                                     |
| <span data-ttu-id="7e296-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e296-269">Classes used in</span></span>        | [<span data-ttu-id="7e296-270">**連結-追蹤-音量-進入**</span><span class="sxs-lookup"><span data-stu-id="7e296-270">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





