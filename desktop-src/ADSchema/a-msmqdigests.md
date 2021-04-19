---
title: MSMQ-Digests 屬性
description: 屬性 mSMQ 簽署憑證中對應憑證的摘要陣列。 它們是用來將摘要對應至憑證。
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- MSMQ-Digests 屬性 AD 架構
- mSMQDigests 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970484"
---
# <a name="msmq-digests-attribute"></a><span data-ttu-id="91e6b-106">MSMQ-Digests 屬性</span><span class="sxs-lookup"><span data-stu-id="91e6b-106">MSMQ-Digests attribute</span></span>

<span data-ttu-id="91e6b-107">屬性 mSMQ 簽署憑證中對應憑證的摘要陣列。</span><span class="sxs-lookup"><span data-stu-id="91e6b-107">An array of digests of the corresponding certificates in attribute mSMQ-Sign-Certificates.</span></span> <span data-ttu-id="91e6b-108">它們是用來將摘要對應至憑證。</span><span class="sxs-lookup"><span data-stu-id="91e6b-108">They are used for mapping a digest into a certificate.</span></span>



| <span data-ttu-id="91e6b-109">進入</span><span class="sxs-lookup"><span data-stu-id="91e6b-109">Entry</span></span> | <span data-ttu-id="91e6b-110">值</span><span class="sxs-lookup"><span data-stu-id="91e6b-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="91e6b-111">CN</span><span class="sxs-lookup"><span data-stu-id="91e6b-111">CN</span></span>                | <span data-ttu-id="91e6b-112">MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="91e6b-112">MSMQ-Digests</span></span>                                          |
| <span data-ttu-id="91e6b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="91e6b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="91e6b-114">mSMQDigests</span><span class="sxs-lookup"><span data-stu-id="91e6b-114">mSMQDigests</span></span>                                           |
| <span data-ttu-id="91e6b-115">大小</span><span class="sxs-lookup"><span data-stu-id="91e6b-115">Size</span></span>              | <span data-ttu-id="91e6b-116">每個摘要都是16個位元組。</span><span class="sxs-lookup"><span data-stu-id="91e6b-116">Each digest is 16 bytes.</span></span>                              |
| <span data-ttu-id="91e6b-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="91e6b-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="91e6b-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="91e6b-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="91e6b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91e6b-119">Attribute-Id</span></span>      | <span data-ttu-id="91e6b-120">1.2.840.113556.1.4.948</span><span class="sxs-lookup"><span data-stu-id="91e6b-120">1.2.840.113556.1.4.948</span></span>                                |
| <span data-ttu-id="91e6b-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="91e6b-121">System-Id-Guid</span></span>    | <span data-ttu-id="91e6b-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="91e6b-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="91e6b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="91e6b-123">Syntax</span></span>            | [<span data-ttu-id="91e6b-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="91e6b-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="91e6b-125">實作</span><span class="sxs-lookup"><span data-stu-id="91e6b-125">Implementations</span></span>

-   [<span data-ttu-id="91e6b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="91e6b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="91e6b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="91e6b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="91e6b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="91e6b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="91e6b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="91e6b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="91e6b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="91e6b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="91e6b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="91e6b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="91e6b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91e6b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="91e6b-133">進入</span><span class="sxs-lookup"><span data-stu-id="91e6b-133">Entry</span></span> | <span data-ttu-id="91e6b-134">值</span><span class="sxs-lookup"><span data-stu-id="91e6b-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e6b-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="91e6b-135">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91e6b-136">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="91e6b-137">System-Only</span></span>            | <span data-ttu-id="91e6b-138">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-138">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="91e6b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="91e6b-140">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-140">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="91e6b-141">Is Indexed</span></span>             | <span data-ttu-id="91e6b-142">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-142">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="91e6b-143">In Global Catalog</span></span>      | <span data-ttu-id="91e6b-144">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-144">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="91e6b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="91e6b-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="91e6b-146">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="91e6b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91e6b-147">Range-Lower</span></span>            | <span data-ttu-id="91e6b-148">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-148">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91e6b-149">Range-Upper</span></span>            | <span data-ttu-id="91e6b-150">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-150">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-151">Search-Flags</span></span>           | <span data-ttu-id="91e6b-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="91e6b-152">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="91e6b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-153">System-Flags</span></span>           | <span data-ttu-id="91e6b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91e6b-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="91e6b-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="91e6b-155">Classes used in</span></span>        | [<span data-ttu-id="91e6b-156">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="91e6b-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="91e6b-157">**User**</span><span class="sxs-lookup"><span data-stu-id="91e6b-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="91e6b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91e6b-158">Windows Server 2003</span></span>



| <span data-ttu-id="91e6b-159">進入</span><span class="sxs-lookup"><span data-stu-id="91e6b-159">Entry</span></span> | <span data-ttu-id="91e6b-160">值</span><span class="sxs-lookup"><span data-stu-id="91e6b-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e6b-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="91e6b-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91e6b-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="91e6b-163">System-Only</span></span>            | <span data-ttu-id="91e6b-164">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-164">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="91e6b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="91e6b-166">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-166">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="91e6b-167">Is Indexed</span></span>             | <span data-ttu-id="91e6b-168">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-168">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="91e6b-169">In Global Catalog</span></span>      | <span data-ttu-id="91e6b-170">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-170">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="91e6b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="91e6b-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="91e6b-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="91e6b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91e6b-173">Range-Lower</span></span>            | <span data-ttu-id="91e6b-174">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-174">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91e6b-175">Range-Upper</span></span>            | <span data-ttu-id="91e6b-176">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-176">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-177">Search-Flags</span></span>           | <span data-ttu-id="91e6b-178">0x00000001</span><span class="sxs-lookup"><span data-stu-id="91e6b-178">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="91e6b-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-179">System-Flags</span></span>           | <span data-ttu-id="91e6b-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91e6b-180">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="91e6b-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="91e6b-181">Classes used in</span></span>        | [<span data-ttu-id="91e6b-182">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="91e6b-182">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="91e6b-183">**User**</span><span class="sxs-lookup"><span data-stu-id="91e6b-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="91e6b-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="91e6b-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="91e6b-185">進入</span><span class="sxs-lookup"><span data-stu-id="91e6b-185">Entry</span></span> | <span data-ttu-id="91e6b-186">值</span><span class="sxs-lookup"><span data-stu-id="91e6b-186">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e6b-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="91e6b-187">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91e6b-188">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="91e6b-189">System-Only</span></span>            | <span data-ttu-id="91e6b-190">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-190">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="91e6b-191">Is-Single-Valued</span></span>       | <span data-ttu-id="91e6b-192">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-192">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="91e6b-193">Is Indexed</span></span>             | <span data-ttu-id="91e6b-194">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-194">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="91e6b-195">In Global Catalog</span></span>      | <span data-ttu-id="91e6b-196">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-196">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="91e6b-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="91e6b-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="91e6b-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="91e6b-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91e6b-199">Range-Lower</span></span>            | <span data-ttu-id="91e6b-200">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-200">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91e6b-201">Range-Upper</span></span>            | <span data-ttu-id="91e6b-202">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-202">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-203">Search-Flags</span></span>           | <span data-ttu-id="91e6b-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="91e6b-204">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="91e6b-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-205">System-Flags</span></span>           | <span data-ttu-id="91e6b-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91e6b-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="91e6b-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="91e6b-207">Classes used in</span></span>        | [<span data-ttu-id="91e6b-208">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="91e6b-208">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="91e6b-209">**User**</span><span class="sxs-lookup"><span data-stu-id="91e6b-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="91e6b-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91e6b-210">Windows Server 2008</span></span>



| <span data-ttu-id="91e6b-211">進入</span><span class="sxs-lookup"><span data-stu-id="91e6b-211">Entry</span></span> | <span data-ttu-id="91e6b-212">值</span><span class="sxs-lookup"><span data-stu-id="91e6b-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e6b-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="91e6b-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91e6b-214">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="91e6b-215">System-Only</span></span>            | <span data-ttu-id="91e6b-216">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-216">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="91e6b-217">Is-Single-Valued</span></span>       | <span data-ttu-id="91e6b-218">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-218">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="91e6b-219">Is Indexed</span></span>             | <span data-ttu-id="91e6b-220">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-220">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="91e6b-221">In Global Catalog</span></span>      | <span data-ttu-id="91e6b-222">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-222">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="91e6b-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="91e6b-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="91e6b-224">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="91e6b-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91e6b-225">Range-Lower</span></span>            | <span data-ttu-id="91e6b-226">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-226">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91e6b-227">Range-Upper</span></span>            | <span data-ttu-id="91e6b-228">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-228">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-229">Search-Flags</span></span>           | <span data-ttu-id="91e6b-230">0x00000001</span><span class="sxs-lookup"><span data-stu-id="91e6b-230">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="91e6b-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-231">System-Flags</span></span>           | <span data-ttu-id="91e6b-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91e6b-232">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="91e6b-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="91e6b-233">Classes used in</span></span>        | [<span data-ttu-id="91e6b-234">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="91e6b-234">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="91e6b-235">**User**</span><span class="sxs-lookup"><span data-stu-id="91e6b-235">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="91e6b-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91e6b-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="91e6b-237">進入</span><span class="sxs-lookup"><span data-stu-id="91e6b-237">Entry</span></span> | <span data-ttu-id="91e6b-238">值</span><span class="sxs-lookup"><span data-stu-id="91e6b-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e6b-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="91e6b-239">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91e6b-240">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="91e6b-241">System-Only</span></span>            | <span data-ttu-id="91e6b-242">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-242">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="91e6b-243">Is-Single-Valued</span></span>       | <span data-ttu-id="91e6b-244">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-244">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="91e6b-245">Is Indexed</span></span>             | <span data-ttu-id="91e6b-246">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-246">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="91e6b-247">In Global Catalog</span></span>      | <span data-ttu-id="91e6b-248">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-248">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="91e6b-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="91e6b-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="91e6b-250">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="91e6b-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91e6b-251">Range-Lower</span></span>            | <span data-ttu-id="91e6b-252">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-252">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91e6b-253">Range-Upper</span></span>            | <span data-ttu-id="91e6b-254">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-254">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-255">Search-Flags</span></span>           | <span data-ttu-id="91e6b-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="91e6b-256">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="91e6b-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-257">System-Flags</span></span>           | <span data-ttu-id="91e6b-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91e6b-258">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="91e6b-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="91e6b-259">Classes used in</span></span>        | [<span data-ttu-id="91e6b-260">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="91e6b-260">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="91e6b-261">**User**</span><span class="sxs-lookup"><span data-stu-id="91e6b-261">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="91e6b-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91e6b-262">Windows Server 2012</span></span>



| <span data-ttu-id="91e6b-263">進入</span><span class="sxs-lookup"><span data-stu-id="91e6b-263">Entry</span></span> | <span data-ttu-id="91e6b-264">值</span><span class="sxs-lookup"><span data-stu-id="91e6b-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e6b-265">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="91e6b-265">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91e6b-266">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="91e6b-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="91e6b-267">System-Only</span></span>            | <span data-ttu-id="91e6b-268">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-268">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-269">是-單一值</span><span class="sxs-lookup"><span data-stu-id="91e6b-269">Is-Single-Valued</span></span>       | <span data-ttu-id="91e6b-270">否</span><span class="sxs-lookup"><span data-stu-id="91e6b-270">False</span></span>                                                                                         |
| <span data-ttu-id="91e6b-271">已編制索引</span><span class="sxs-lookup"><span data-stu-id="91e6b-271">Is Indexed</span></span>             | <span data-ttu-id="91e6b-272">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-272">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-273">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="91e6b-273">In Global Catalog</span></span>      | <span data-ttu-id="91e6b-274">對</span><span class="sxs-lookup"><span data-stu-id="91e6b-274">True</span></span>                                                                                          |
| <span data-ttu-id="91e6b-275">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="91e6b-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="91e6b-276">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="91e6b-276">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="91e6b-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91e6b-277">Range-Lower</span></span>            | <span data-ttu-id="91e6b-278">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-278">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91e6b-279">Range-Upper</span></span>            | <span data-ttu-id="91e6b-280">16</span><span class="sxs-lookup"><span data-stu-id="91e6b-280">16</span></span>                                                                                            |
| <span data-ttu-id="91e6b-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-281">Search-Flags</span></span>           | <span data-ttu-id="91e6b-282">0x00000001</span><span class="sxs-lookup"><span data-stu-id="91e6b-282">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="91e6b-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91e6b-283">System-Flags</span></span>           | <span data-ttu-id="91e6b-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91e6b-284">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="91e6b-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="91e6b-285">Classes used in</span></span>        | [<span data-ttu-id="91e6b-286">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="91e6b-286">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="91e6b-287">**User**</span><span class="sxs-lookup"><span data-stu-id="91e6b-287">**User**</span></span>](c-user.md)<br/> |



 

 





