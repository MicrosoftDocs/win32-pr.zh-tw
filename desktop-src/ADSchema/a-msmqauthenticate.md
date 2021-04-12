---
title: MSMQ-Authenticate 屬性
description: 指出佇列是否只接受已驗證的訊息。
ms.assetid: f03316e3-daae-4d1e-b135-8b4c3c2765b2
ms.tgt_platform: multiple
keywords:
- MSMQ-Authenticate 屬性 AD 架構
- mSMQAuthenticate 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a2d3744a01834cde181f5cfcf3804a0c765415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509693"
---
# <a name="msmq-authenticate-attribute"></a><span data-ttu-id="b4b5f-105">MSMQ-Authenticate 屬性</span><span class="sxs-lookup"><span data-stu-id="b4b5f-105">MSMQ-Authenticate attribute</span></span>

<span data-ttu-id="b4b5f-106">指出佇列是否只接受已驗證的訊息。</span><span class="sxs-lookup"><span data-stu-id="b4b5f-106">Indicates whether the queue accepts only authenticated messages.</span></span>



| <span data-ttu-id="b4b5f-107">進入</span><span class="sxs-lookup"><span data-stu-id="b4b5f-107">Entry</span></span> | <span data-ttu-id="b4b5f-108">值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b4b5f-109">CN</span><span class="sxs-lookup"><span data-stu-id="b4b5f-109">CN</span></span>                | <span data-ttu-id="b4b5f-110">MSMQ-Authenticate</span><span class="sxs-lookup"><span data-stu-id="b4b5f-110">MSMQ-Authenticate</span></span>                    |
| <span data-ttu-id="b4b5f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b4b5f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b4b5f-112">mSMQAuthenticate</span><span class="sxs-lookup"><span data-stu-id="b4b5f-112">mSMQAuthenticate</span></span>                     |
| <span data-ttu-id="b4b5f-113">大小</span><span class="sxs-lookup"><span data-stu-id="b4b5f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="b4b5f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b4b5f-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b4b5f-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b4b5f-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b4b5f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4b5f-116">Attribute-Id</span></span>      | <span data-ttu-id="b4b5f-117">1.2.840.113556.1.4.923</span><span class="sxs-lookup"><span data-stu-id="b4b5f-117">1.2.840.113556.1.4.923</span></span>               |
| <span data-ttu-id="b4b5f-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b4b5f-118">System-Id-Guid</span></span>    | <span data-ttu-id="b4b5f-119">9a0dc326-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b4b5f-119">9a0dc326-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="b4b5f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4b5f-120">Syntax</span></span>            | [<span data-ttu-id="b4b5f-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b4b5f-122">實作</span><span class="sxs-lookup"><span data-stu-id="b4b5f-122">Implementations</span></span>

-   [<span data-ttu-id="b4b5f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4b5f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4b5f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4b5f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4b5f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4b5f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4b5f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4b5f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b4b5f-130">進入</span><span class="sxs-lookup"><span data-stu-id="b4b5f-130">Entry</span></span> | <span data-ttu-id="b4b5f-131">值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b4b5f-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b5f-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4b5f-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4b5f-134">System-Only</span></span>            | <span data-ttu-id="b4b5f-135">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-135">False</span></span>                                        |
| <span data-ttu-id="b4b5f-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b4b5f-137">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-137">True</span></span>                                         |
| <span data-ttu-id="b4b5f-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4b5f-138">Is Indexed</span></span>             | <span data-ttu-id="b4b5f-139">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-139">False</span></span>                                        |
| <span data-ttu-id="b4b5f-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4b5f-140">In Global Catalog</span></span>      | <span data-ttu-id="b4b5f-141">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-141">True</span></span>                                         |
| <span data-ttu-id="b4b5f-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4b5f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4b5f-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4b5f-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b4b5f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4b5f-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4b5f-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-146">Search-Flags</span></span>           | <span data-ttu-id="b4b5f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4b5f-147">0x00000000</span></span>                                   |
| <span data-ttu-id="b4b5f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-148">System-Flags</span></span>           | <span data-ttu-id="b4b5f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4b5f-149">0x00000010</span></span>                                   |
| <span data-ttu-id="b4b5f-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4b5f-150">Classes used in</span></span>        | [<span data-ttu-id="b4b5f-151">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4b5f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4b5f-152">Windows Server 2003</span></span>



| <span data-ttu-id="b4b5f-153">進入</span><span class="sxs-lookup"><span data-stu-id="b4b5f-153">Entry</span></span> | <span data-ttu-id="b4b5f-154">值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b4b5f-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b5f-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4b5f-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4b5f-157">System-Only</span></span>            | <span data-ttu-id="b4b5f-158">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-158">False</span></span>                                        |
| <span data-ttu-id="b4b5f-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="b4b5f-160">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-160">True</span></span>                                         |
| <span data-ttu-id="b4b5f-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4b5f-161">Is Indexed</span></span>             | <span data-ttu-id="b4b5f-162">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-162">False</span></span>                                        |
| <span data-ttu-id="b4b5f-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4b5f-163">In Global Catalog</span></span>      | <span data-ttu-id="b4b5f-164">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-164">True</span></span>                                         |
| <span data-ttu-id="b4b5f-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4b5f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4b5f-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4b5f-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b4b5f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4b5f-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4b5f-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-169">Search-Flags</span></span>           | <span data-ttu-id="b4b5f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4b5f-170">0x00000000</span></span>                                   |
| <span data-ttu-id="b4b5f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-171">System-Flags</span></span>           | <span data-ttu-id="b4b5f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4b5f-172">0x00000010</span></span>                                   |
| <span data-ttu-id="b4b5f-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4b5f-173">Classes used in</span></span>        | [<span data-ttu-id="b4b5f-174">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4b5f-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4b5f-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4b5f-176">進入</span><span class="sxs-lookup"><span data-stu-id="b4b5f-176">Entry</span></span> | <span data-ttu-id="b4b5f-177">值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b4b5f-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b5f-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4b5f-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4b5f-180">System-Only</span></span>            | <span data-ttu-id="b4b5f-181">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-181">False</span></span>                                        |
| <span data-ttu-id="b4b5f-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="b4b5f-183">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-183">True</span></span>                                         |
| <span data-ttu-id="b4b5f-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4b5f-184">Is Indexed</span></span>             | <span data-ttu-id="b4b5f-185">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-185">False</span></span>                                        |
| <span data-ttu-id="b4b5f-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4b5f-186">In Global Catalog</span></span>      | <span data-ttu-id="b4b5f-187">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-187">True</span></span>                                         |
| <span data-ttu-id="b4b5f-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4b5f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4b5f-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4b5f-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b4b5f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4b5f-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4b5f-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-192">Search-Flags</span></span>           | <span data-ttu-id="b4b5f-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4b5f-193">0x00000000</span></span>                                   |
| <span data-ttu-id="b4b5f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-194">System-Flags</span></span>           | <span data-ttu-id="b4b5f-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4b5f-195">0x00000010</span></span>                                   |
| <span data-ttu-id="b4b5f-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4b5f-196">Classes used in</span></span>        | [<span data-ttu-id="b4b5f-197">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4b5f-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4b5f-198">Windows Server 2008</span></span>



| <span data-ttu-id="b4b5f-199">進入</span><span class="sxs-lookup"><span data-stu-id="b4b5f-199">Entry</span></span> | <span data-ttu-id="b4b5f-200">值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b4b5f-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b5f-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4b5f-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4b5f-203">System-Only</span></span>            | <span data-ttu-id="b4b5f-204">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-204">False</span></span>                                        |
| <span data-ttu-id="b4b5f-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="b4b5f-206">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-206">True</span></span>                                         |
| <span data-ttu-id="b4b5f-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4b5f-207">Is Indexed</span></span>             | <span data-ttu-id="b4b5f-208">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-208">False</span></span>                                        |
| <span data-ttu-id="b4b5f-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4b5f-209">In Global Catalog</span></span>      | <span data-ttu-id="b4b5f-210">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-210">True</span></span>                                         |
| <span data-ttu-id="b4b5f-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4b5f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4b5f-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4b5f-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b4b5f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4b5f-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4b5f-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-215">Search-Flags</span></span>           | <span data-ttu-id="b4b5f-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4b5f-216">0x00000000</span></span>                                   |
| <span data-ttu-id="b4b5f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-217">System-Flags</span></span>           | <span data-ttu-id="b4b5f-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4b5f-218">0x00000010</span></span>                                   |
| <span data-ttu-id="b4b5f-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4b5f-219">Classes used in</span></span>        | [<span data-ttu-id="b4b5f-220">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4b5f-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4b5f-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4b5f-222">進入</span><span class="sxs-lookup"><span data-stu-id="b4b5f-222">Entry</span></span> | <span data-ttu-id="b4b5f-223">值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b4b5f-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b5f-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4b5f-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4b5f-226">System-Only</span></span>            | <span data-ttu-id="b4b5f-227">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-227">False</span></span>                                        |
| <span data-ttu-id="b4b5f-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-228">Is-Single-Valued</span></span>       | <span data-ttu-id="b4b5f-229">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-229">True</span></span>                                         |
| <span data-ttu-id="b4b5f-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4b5f-230">Is Indexed</span></span>             | <span data-ttu-id="b4b5f-231">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-231">False</span></span>                                        |
| <span data-ttu-id="b4b5f-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4b5f-232">In Global Catalog</span></span>      | <span data-ttu-id="b4b5f-233">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-233">True</span></span>                                         |
| <span data-ttu-id="b4b5f-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4b5f-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4b5f-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4b5f-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b4b5f-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4b5f-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4b5f-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-238">Search-Flags</span></span>           | <span data-ttu-id="b4b5f-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4b5f-239">0x00000000</span></span>                                   |
| <span data-ttu-id="b4b5f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-240">System-Flags</span></span>           | <span data-ttu-id="b4b5f-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4b5f-241">0x00000010</span></span>                                   |
| <span data-ttu-id="b4b5f-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4b5f-242">Classes used in</span></span>        | [<span data-ttu-id="b4b5f-243">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4b5f-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4b5f-244">Windows Server 2012</span></span>



| <span data-ttu-id="b4b5f-245">進入</span><span class="sxs-lookup"><span data-stu-id="b4b5f-245">Entry</span></span> | <span data-ttu-id="b4b5f-246">值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b4b5f-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b5f-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4b5f-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b4b5f-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4b5f-249">System-Only</span></span>            | <span data-ttu-id="b4b5f-250">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-250">False</span></span>                                        |
| <span data-ttu-id="b4b5f-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b4b5f-251">Is-Single-Valued</span></span>       | <span data-ttu-id="b4b5f-252">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-252">True</span></span>                                         |
| <span data-ttu-id="b4b5f-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b4b5f-253">Is Indexed</span></span>             | <span data-ttu-id="b4b5f-254">否</span><span class="sxs-lookup"><span data-stu-id="b4b5f-254">False</span></span>                                        |
| <span data-ttu-id="b4b5f-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b4b5f-255">In Global Catalog</span></span>      | <span data-ttu-id="b4b5f-256">對</span><span class="sxs-lookup"><span data-stu-id="b4b5f-256">True</span></span>                                         |
| <span data-ttu-id="b4b5f-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b4b5f-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4b5f-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b4b5f-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b4b5f-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4b5f-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4b5f-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b4b5f-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-261">Search-Flags</span></span>           | <span data-ttu-id="b4b5f-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4b5f-262">0x00000000</span></span>                                   |
| <span data-ttu-id="b4b5f-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4b5f-263">System-Flags</span></span>           | <span data-ttu-id="b4b5f-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4b5f-264">0x00000010</span></span>                                   |
| <span data-ttu-id="b4b5f-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b4b5f-265">Classes used in</span></span>        | [<span data-ttu-id="b4b5f-266">**MSMQ-佇列**</span><span class="sxs-lookup"><span data-stu-id="b4b5f-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





