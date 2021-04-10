---
title: Invocation-Id 屬性
description: 用來唯一識別組織中的每個 Microsoft Exchange Server 目錄。
ms.assetid: c069a57c-b9d0-49e9-8096-39b43f378573
ms.tgt_platform: multiple
keywords:
- Invocation-Id 屬性 AD 架構
- invocationId 屬性 AD 架構
topic_type:
- apiref
api_name:
- Invocation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611589c466013ad46c0920a2da1e2250cf596214
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107028"
---
# <a name="invocation-id-attribute"></a><span data-ttu-id="3d07e-105">Invocation-Id 屬性</span><span class="sxs-lookup"><span data-stu-id="3d07e-105">Invocation-Id attribute</span></span>

<span data-ttu-id="3d07e-106">用來唯一識別組織中的每個 Microsoft Exchange Server 目錄。</span><span class="sxs-lookup"><span data-stu-id="3d07e-106">Used to uniquely identify each Microsoft Exchange Server directory in the organization.</span></span>



| <span data-ttu-id="3d07e-107">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-107">Entry</span></span> | <span data-ttu-id="3d07e-108">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="3d07e-109">CN</span><span class="sxs-lookup"><span data-stu-id="3d07e-109">CN</span></span>                | <span data-ttu-id="3d07e-110">Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-110">Invocation-Id</span></span>                                         |
| <span data-ttu-id="3d07e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3d07e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3d07e-112">invocationId</span><span class="sxs-lookup"><span data-stu-id="3d07e-112">invocationId</span></span>                                          |
| <span data-ttu-id="3d07e-113">大小</span><span class="sxs-lookup"><span data-stu-id="3d07e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="3d07e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3d07e-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="3d07e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3d07e-115">Update Frequency</span></span>  | <span data-ttu-id="3d07e-116">安裝 Exchange Server 時。</span><span class="sxs-lookup"><span data-stu-id="3d07e-116">When the Exchange Server is installed.</span></span>                |
| <span data-ttu-id="3d07e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-117">Attribute-Id</span></span>      | <span data-ttu-id="3d07e-118">1.2.840.113556.1.2.115</span><span class="sxs-lookup"><span data-stu-id="3d07e-118">1.2.840.113556.1.2.115</span></span>                                |
| <span data-ttu-id="3d07e-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3d07e-119">System-Id-Guid</span></span>    | <span data-ttu-id="3d07e-120">bf96798e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3d07e-120">bf96798e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="3d07e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d07e-121">Syntax</span></span>            | [<span data-ttu-id="3d07e-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="3d07e-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="3d07e-123">實作</span><span class="sxs-lookup"><span data-stu-id="3d07e-123">Implementations</span></span>

-   [<span data-ttu-id="3d07e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3d07e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3d07e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d07e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d07e-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="3d07e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3d07e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d07e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d07e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d07e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d07e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d07e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d07e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d07e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3d07e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d07e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3d07e-132">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-132">Entry</span></span> | <span data-ttu-id="3d07e-133">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d07e-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d07e-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d07e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-135">MAPI-Id</span></span>                | <span data-ttu-id="3d07e-136">0x80BF</span><span class="sxs-lookup"><span data-stu-id="3d07e-136">0x80BF</span></span>                                   |
| <span data-ttu-id="3d07e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d07e-137">System-Only</span></span>            | <span data-ttu-id="3d07e-138">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-138">True</span></span>                                     |
| <span data-ttu-id="3d07e-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d07e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3d07e-140">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-140">True</span></span>                                     |
| <span data-ttu-id="3d07e-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d07e-141">Is Indexed</span></span>             | <span data-ttu-id="3d07e-142">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-142">False</span></span>                                    |
| <span data-ttu-id="3d07e-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d07e-143">In Global Catalog</span></span>      | <span data-ttu-id="3d07e-144">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-144">False</span></span>                                    |
| <span data-ttu-id="3d07e-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d07e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d07e-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d07e-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d07e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d07e-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d07e-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-149">Search-Flags</span></span>           | <span data-ttu-id="3d07e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d07e-150">0x00000000</span></span>                               |
| <span data-ttu-id="3d07e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-151">System-Flags</span></span>           | <span data-ttu-id="3d07e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d07e-152">0x00000010</span></span>                               |
| <span data-ttu-id="3d07e-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d07e-153">Classes used in</span></span>        | [<span data-ttu-id="3d07e-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d07e-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3d07e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d07e-155">Windows Server 2003</span></span>



| <span data-ttu-id="3d07e-156">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-156">Entry</span></span> | <span data-ttu-id="3d07e-157">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d07e-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d07e-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d07e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-159">MAPI-Id</span></span>                | <span data-ttu-id="3d07e-160">0x80BF</span><span class="sxs-lookup"><span data-stu-id="3d07e-160">0x80BF</span></span>                                   |
| <span data-ttu-id="3d07e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d07e-161">System-Only</span></span>            | <span data-ttu-id="3d07e-162">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-162">True</span></span>                                     |
| <span data-ttu-id="3d07e-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d07e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="3d07e-164">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-164">True</span></span>                                     |
| <span data-ttu-id="3d07e-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d07e-165">Is Indexed</span></span>             | <span data-ttu-id="3d07e-166">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-166">True</span></span>                                     |
| <span data-ttu-id="3d07e-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d07e-167">In Global Catalog</span></span>      | <span data-ttu-id="3d07e-168">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-168">False</span></span>                                    |
| <span data-ttu-id="3d07e-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d07e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d07e-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d07e-170">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d07e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d07e-171">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d07e-172">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-173">Search-Flags</span></span>           | <span data-ttu-id="3d07e-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d07e-174">0x00000001</span></span>                               |
| <span data-ttu-id="3d07e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-175">System-Flags</span></span>           | <span data-ttu-id="3d07e-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d07e-176">0x00000010</span></span>                               |
| <span data-ttu-id="3d07e-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d07e-177">Classes used in</span></span>        | [<span data-ttu-id="3d07e-178">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d07e-178">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3d07e-179">亞當</span><span class="sxs-lookup"><span data-stu-id="3d07e-179">ADAM</span></span>



| <span data-ttu-id="3d07e-180">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-180">Entry</span></span> | <span data-ttu-id="3d07e-181">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-181">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d07e-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d07e-182">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d07e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-183">MAPI-Id</span></span>                | <span data-ttu-id="3d07e-184">0x80BF</span><span class="sxs-lookup"><span data-stu-id="3d07e-184">0x80BF</span></span>                                   |
| <span data-ttu-id="3d07e-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d07e-185">System-Only</span></span>            | <span data-ttu-id="3d07e-186">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-186">True</span></span>                                     |
| <span data-ttu-id="3d07e-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d07e-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3d07e-188">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-188">True</span></span>                                     |
| <span data-ttu-id="3d07e-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d07e-189">Is Indexed</span></span>             | <span data-ttu-id="3d07e-190">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-190">True</span></span>                                     |
| <span data-ttu-id="3d07e-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d07e-191">In Global Catalog</span></span>      | <span data-ttu-id="3d07e-192">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-192">False</span></span>                                    |
| <span data-ttu-id="3d07e-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d07e-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d07e-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d07e-194">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d07e-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d07e-195">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d07e-196">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-197">Search-Flags</span></span>           | <span data-ttu-id="3d07e-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d07e-198">0x00000001</span></span>                               |
| <span data-ttu-id="3d07e-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-199">System-Flags</span></span>           | <span data-ttu-id="3d07e-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d07e-200">0x00000010</span></span>                               |
| <span data-ttu-id="3d07e-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d07e-201">Classes used in</span></span>        | [<span data-ttu-id="3d07e-202">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d07e-202">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d07e-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d07e-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d07e-204">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-204">Entry</span></span> | <span data-ttu-id="3d07e-205">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-205">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d07e-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d07e-206">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d07e-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-207">MAPI-Id</span></span>                | <span data-ttu-id="3d07e-208">0x80BF</span><span class="sxs-lookup"><span data-stu-id="3d07e-208">0x80BF</span></span>                                   |
| <span data-ttu-id="3d07e-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d07e-209">System-Only</span></span>            | <span data-ttu-id="3d07e-210">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-210">True</span></span>                                     |
| <span data-ttu-id="3d07e-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d07e-211">Is-Single-Valued</span></span>       | <span data-ttu-id="3d07e-212">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-212">True</span></span>                                     |
| <span data-ttu-id="3d07e-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d07e-213">Is Indexed</span></span>             | <span data-ttu-id="3d07e-214">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-214">True</span></span>                                     |
| <span data-ttu-id="3d07e-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d07e-215">In Global Catalog</span></span>      | <span data-ttu-id="3d07e-216">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-216">False</span></span>                                    |
| <span data-ttu-id="3d07e-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d07e-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d07e-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d07e-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d07e-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d07e-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d07e-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-221">Search-Flags</span></span>           | <span data-ttu-id="3d07e-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d07e-222">0x00000001</span></span>                               |
| <span data-ttu-id="3d07e-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-223">System-Flags</span></span>           | <span data-ttu-id="3d07e-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d07e-224">0x00000010</span></span>                               |
| <span data-ttu-id="3d07e-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d07e-225">Classes used in</span></span>        | [<span data-ttu-id="3d07e-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d07e-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d07e-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d07e-227">Windows Server 2008</span></span>



| <span data-ttu-id="3d07e-228">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-228">Entry</span></span> | <span data-ttu-id="3d07e-229">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d07e-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d07e-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d07e-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-231">MAPI-Id</span></span>                | <span data-ttu-id="3d07e-232">0x80BF</span><span class="sxs-lookup"><span data-stu-id="3d07e-232">0x80BF</span></span>                                   |
| <span data-ttu-id="3d07e-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d07e-233">System-Only</span></span>            | <span data-ttu-id="3d07e-234">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-234">True</span></span>                                     |
| <span data-ttu-id="3d07e-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d07e-235">Is-Single-Valued</span></span>       | <span data-ttu-id="3d07e-236">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-236">True</span></span>                                     |
| <span data-ttu-id="3d07e-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d07e-237">Is Indexed</span></span>             | <span data-ttu-id="3d07e-238">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-238">True</span></span>                                     |
| <span data-ttu-id="3d07e-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d07e-239">In Global Catalog</span></span>      | <span data-ttu-id="3d07e-240">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-240">False</span></span>                                    |
| <span data-ttu-id="3d07e-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d07e-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d07e-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d07e-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d07e-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d07e-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d07e-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-245">Search-Flags</span></span>           | <span data-ttu-id="3d07e-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d07e-246">0x00000001</span></span>                               |
| <span data-ttu-id="3d07e-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-247">System-Flags</span></span>           | <span data-ttu-id="3d07e-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d07e-248">0x00000010</span></span>                               |
| <span data-ttu-id="3d07e-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d07e-249">Classes used in</span></span>        | [<span data-ttu-id="3d07e-250">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d07e-250">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d07e-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d07e-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d07e-252">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-252">Entry</span></span> | <span data-ttu-id="3d07e-253">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d07e-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d07e-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d07e-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-255">MAPI-Id</span></span>                | <span data-ttu-id="3d07e-256">0x80BF</span><span class="sxs-lookup"><span data-stu-id="3d07e-256">0x80BF</span></span>                                   |
| <span data-ttu-id="3d07e-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d07e-257">System-Only</span></span>            | <span data-ttu-id="3d07e-258">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-258">True</span></span>                                     |
| <span data-ttu-id="3d07e-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d07e-259">Is-Single-Valued</span></span>       | <span data-ttu-id="3d07e-260">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-260">True</span></span>                                     |
| <span data-ttu-id="3d07e-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d07e-261">Is Indexed</span></span>             | <span data-ttu-id="3d07e-262">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-262">True</span></span>                                     |
| <span data-ttu-id="3d07e-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d07e-263">In Global Catalog</span></span>      | <span data-ttu-id="3d07e-264">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-264">False</span></span>                                    |
| <span data-ttu-id="3d07e-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d07e-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d07e-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d07e-266">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d07e-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d07e-267">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d07e-268">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-269">Search-Flags</span></span>           | <span data-ttu-id="3d07e-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d07e-270">0x00000001</span></span>                               |
| <span data-ttu-id="3d07e-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-271">System-Flags</span></span>           | <span data-ttu-id="3d07e-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d07e-272">0x00000010</span></span>                               |
| <span data-ttu-id="3d07e-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d07e-273">Classes used in</span></span>        | [<span data-ttu-id="3d07e-274">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d07e-274">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d07e-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d07e-275">Windows Server 2012</span></span>



| <span data-ttu-id="3d07e-276">進入</span><span class="sxs-lookup"><span data-stu-id="3d07e-276">Entry</span></span> | <span data-ttu-id="3d07e-277">值</span><span class="sxs-lookup"><span data-stu-id="3d07e-277">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3d07e-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3d07e-278">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3d07e-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d07e-279">MAPI-Id</span></span>                | <span data-ttu-id="3d07e-280">0x80BF</span><span class="sxs-lookup"><span data-stu-id="3d07e-280">0x80BF</span></span>                                   |
| <span data-ttu-id="3d07e-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d07e-281">System-Only</span></span>            | <span data-ttu-id="3d07e-282">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-282">True</span></span>                                     |
| <span data-ttu-id="3d07e-283">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3d07e-283">Is-Single-Valued</span></span>       | <span data-ttu-id="3d07e-284">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-284">True</span></span>                                     |
| <span data-ttu-id="3d07e-285">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3d07e-285">Is Indexed</span></span>             | <span data-ttu-id="3d07e-286">對</span><span class="sxs-lookup"><span data-stu-id="3d07e-286">True</span></span>                                     |
| <span data-ttu-id="3d07e-287">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3d07e-287">In Global Catalog</span></span>      | <span data-ttu-id="3d07e-288">否</span><span class="sxs-lookup"><span data-stu-id="3d07e-288">False</span></span>                                    |
| <span data-ttu-id="3d07e-289">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3d07e-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d07e-290">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3d07e-290">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3d07e-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d07e-291">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d07e-292">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3d07e-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-293">Search-Flags</span></span>           | <span data-ttu-id="3d07e-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3d07e-294">0x00000001</span></span>                               |
| <span data-ttu-id="3d07e-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d07e-295">System-Flags</span></span>           | <span data-ttu-id="3d07e-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d07e-296">0x00000010</span></span>                               |
| <span data-ttu-id="3d07e-297">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3d07e-297">Classes used in</span></span>        | [<span data-ttu-id="3d07e-298">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="3d07e-298">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





