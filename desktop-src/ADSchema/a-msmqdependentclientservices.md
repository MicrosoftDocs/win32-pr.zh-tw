---
title: MSMQ 相依-用戶端服務屬性
description: 指出安裝在這部電腦上的 MSMQ 是否提供 MSMQ 相依用戶端服務。
ms.assetid: 6f16db7f-f328-4fe2-9ecc-b40c1c845064
ms.tgt_platform: multiple
keywords:
- MSMQ 相依-用戶端服務屬性 AD 架構
- mSMQDependentClientServices 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Dependent-Client-Services
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ea2ccae62904fd4fc25e9ffaa5f93f2de0ab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935400"
---
# <a name="msmq-dependent-client-services-attribute"></a><span data-ttu-id="fd7ac-105">MSMQ 相依-用戶端服務屬性</span><span class="sxs-lookup"><span data-stu-id="fd7ac-105">MSMQ-Dependent-Client-Services attribute</span></span>

<span data-ttu-id="fd7ac-106">指出安裝在這部電腦上的 MSMQ 是否提供 MSMQ 相依用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="fd7ac-106">Indicates whether the MSMQ installed on this computer provides MSMQ dependent client services.</span></span>



| <span data-ttu-id="fd7ac-107">進入</span><span class="sxs-lookup"><span data-stu-id="fd7ac-107">Entry</span></span> | <span data-ttu-id="fd7ac-108">值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fd7ac-109">CN</span><span class="sxs-lookup"><span data-stu-id="fd7ac-109">CN</span></span>                | <span data-ttu-id="fd7ac-110">MSMQ 相依-用戶端服務</span><span class="sxs-lookup"><span data-stu-id="fd7ac-110">MSMQ-Dependent-Client-Services</span></span>       |
| <span data-ttu-id="fd7ac-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fd7ac-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fd7ac-112">mSMQDependentClientServices</span><span class="sxs-lookup"><span data-stu-id="fd7ac-112">mSMQDependentClientServices</span></span>          |
| <span data-ttu-id="fd7ac-113">大小</span><span class="sxs-lookup"><span data-stu-id="fd7ac-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="fd7ac-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fd7ac-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fd7ac-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fd7ac-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fd7ac-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fd7ac-116">Attribute-Id</span></span>      | <span data-ttu-id="fd7ac-117">1.2.840.113556.1.4.1226</span><span class="sxs-lookup"><span data-stu-id="fd7ac-117">1.2.840.113556.1.4.1226</span></span>              |
| <span data-ttu-id="fd7ac-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fd7ac-118">System-Id-Guid</span></span>    | <span data-ttu-id="fd7ac-119">2df90d76-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="fd7ac-119">2df90d76-009f-11d2-aa4c-00c04fd7d83a</span></span> |
| <span data-ttu-id="fd7ac-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd7ac-120">Syntax</span></span>            | [<span data-ttu-id="fd7ac-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="fd7ac-122">實作</span><span class="sxs-lookup"><span data-stu-id="fd7ac-122">Implementations</span></span>

-   [<span data-ttu-id="fd7ac-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fd7ac-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fd7ac-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fd7ac-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fd7ac-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fd7ac-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fd7ac-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd7ac-129">Windows 2000 Server</span></span>



| <span data-ttu-id="fd7ac-130">進入</span><span class="sxs-lookup"><span data-stu-id="fd7ac-130">Entry</span></span> | <span data-ttu-id="fd7ac-131">值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd7ac-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fd7ac-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7ac-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7ac-134">System-Only</span></span>            | <span data-ttu-id="fd7ac-135">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-135">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-136">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7ac-137">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-137">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fd7ac-138">Is Indexed</span></span>             | <span data-ttu-id="fd7ac-139">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-139">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fd7ac-140">In Global Catalog</span></span>      | <span data-ttu-id="fd7ac-141">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-141">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fd7ac-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7ac-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fd7ac-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd7ac-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7ac-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7ac-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-146">Search-Flags</span></span>           | <span data-ttu-id="fd7ac-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7ac-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="fd7ac-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-148">System-Flags</span></span>           | <span data-ttu-id="fd7ac-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7ac-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="fd7ac-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fd7ac-150">Classes used in</span></span>        | [<span data-ttu-id="fd7ac-151">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fd7ac-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd7ac-152">Windows Server 2003</span></span>



| <span data-ttu-id="fd7ac-153">進入</span><span class="sxs-lookup"><span data-stu-id="fd7ac-153">Entry</span></span> | <span data-ttu-id="fd7ac-154">值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd7ac-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fd7ac-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7ac-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7ac-157">System-Only</span></span>            | <span data-ttu-id="fd7ac-158">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-158">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-159">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7ac-160">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-160">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fd7ac-161">Is Indexed</span></span>             | <span data-ttu-id="fd7ac-162">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-162">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fd7ac-163">In Global Catalog</span></span>      | <span data-ttu-id="fd7ac-164">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-164">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fd7ac-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7ac-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fd7ac-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd7ac-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7ac-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7ac-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-169">Search-Flags</span></span>           | <span data-ttu-id="fd7ac-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7ac-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="fd7ac-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-171">System-Flags</span></span>           | <span data-ttu-id="fd7ac-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7ac-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="fd7ac-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fd7ac-173">Classes used in</span></span>        | [<span data-ttu-id="fd7ac-174">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fd7ac-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fd7ac-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fd7ac-176">進入</span><span class="sxs-lookup"><span data-stu-id="fd7ac-176">Entry</span></span> | <span data-ttu-id="fd7ac-177">值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd7ac-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fd7ac-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7ac-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7ac-180">System-Only</span></span>            | <span data-ttu-id="fd7ac-181">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-181">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-182">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7ac-183">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-183">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fd7ac-184">Is Indexed</span></span>             | <span data-ttu-id="fd7ac-185">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-185">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fd7ac-186">In Global Catalog</span></span>      | <span data-ttu-id="fd7ac-187">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-187">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fd7ac-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7ac-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fd7ac-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd7ac-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7ac-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7ac-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-192">Search-Flags</span></span>           | <span data-ttu-id="fd7ac-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7ac-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="fd7ac-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-194">System-Flags</span></span>           | <span data-ttu-id="fd7ac-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7ac-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="fd7ac-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fd7ac-196">Classes used in</span></span>        | [<span data-ttu-id="fd7ac-197">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fd7ac-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd7ac-198">Windows Server 2008</span></span>



| <span data-ttu-id="fd7ac-199">進入</span><span class="sxs-lookup"><span data-stu-id="fd7ac-199">Entry</span></span> | <span data-ttu-id="fd7ac-200">值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd7ac-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fd7ac-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7ac-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7ac-203">System-Only</span></span>            | <span data-ttu-id="fd7ac-204">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-204">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-205">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7ac-206">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-206">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fd7ac-207">Is Indexed</span></span>             | <span data-ttu-id="fd7ac-208">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-208">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fd7ac-209">In Global Catalog</span></span>      | <span data-ttu-id="fd7ac-210">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-210">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fd7ac-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7ac-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fd7ac-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd7ac-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7ac-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7ac-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-215">Search-Flags</span></span>           | <span data-ttu-id="fd7ac-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7ac-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="fd7ac-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-217">System-Flags</span></span>           | <span data-ttu-id="fd7ac-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7ac-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="fd7ac-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fd7ac-219">Classes used in</span></span>        | [<span data-ttu-id="fd7ac-220">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fd7ac-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fd7ac-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fd7ac-222">進入</span><span class="sxs-lookup"><span data-stu-id="fd7ac-222">Entry</span></span> | <span data-ttu-id="fd7ac-223">值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd7ac-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fd7ac-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7ac-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7ac-226">System-Only</span></span>            | <span data-ttu-id="fd7ac-227">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-227">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-228">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7ac-229">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-229">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fd7ac-230">Is Indexed</span></span>             | <span data-ttu-id="fd7ac-231">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-231">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fd7ac-232">In Global Catalog</span></span>      | <span data-ttu-id="fd7ac-233">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-233">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fd7ac-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7ac-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fd7ac-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd7ac-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7ac-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7ac-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-238">Search-Flags</span></span>           | <span data-ttu-id="fd7ac-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7ac-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="fd7ac-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-240">System-Flags</span></span>           | <span data-ttu-id="fd7ac-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7ac-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="fd7ac-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fd7ac-242">Classes used in</span></span>        | [<span data-ttu-id="fd7ac-243">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fd7ac-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd7ac-244">Windows Server 2012</span></span>



| <span data-ttu-id="fd7ac-245">進入</span><span class="sxs-lookup"><span data-stu-id="fd7ac-245">Entry</span></span> | <span data-ttu-id="fd7ac-246">值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="fd7ac-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fd7ac-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd7ac-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="fd7ac-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd7ac-249">System-Only</span></span>            | <span data-ttu-id="fd7ac-250">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-250">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fd7ac-251">Is-Single-Valued</span></span>       | <span data-ttu-id="fd7ac-252">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-252">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fd7ac-253">Is Indexed</span></span>             | <span data-ttu-id="fd7ac-254">否</span><span class="sxs-lookup"><span data-stu-id="fd7ac-254">False</span></span>                                                        |
| <span data-ttu-id="fd7ac-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fd7ac-255">In Global Catalog</span></span>      | <span data-ttu-id="fd7ac-256">對</span><span class="sxs-lookup"><span data-stu-id="fd7ac-256">True</span></span>                                                         |
| <span data-ttu-id="fd7ac-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fd7ac-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd7ac-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fd7ac-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="fd7ac-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd7ac-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd7ac-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="fd7ac-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-261">Search-Flags</span></span>           | <span data-ttu-id="fd7ac-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd7ac-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="fd7ac-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd7ac-263">System-Flags</span></span>           | <span data-ttu-id="fd7ac-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd7ac-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="fd7ac-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fd7ac-265">Classes used in</span></span>        | [<span data-ttu-id="fd7ac-266">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="fd7ac-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





