---
title: 具有-Partial-Replica-Nc 屬性
description: Nc 的同級。 具有-Partial-Nc 會反映所有其他已複寫到通用類別目錄的網域 Nc 的分辨名稱。
ms.assetid: 2501bbb3-74b5-4604-b0c0-8653fc092e1c
ms.tgt_platform: multiple
keywords:
- 具有-Partial-Replica-Nc 屬性 AD 架構
- hasPartialReplicaNCs 屬性 AD 架構
topic_type:
- apiref
api_name:
- Has-Partial-Replica-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f284df094c909b01b88a4853ed7c4a41dee9f31a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686787"
---
# <a name="has-partial-replica-ncs-attribute"></a><span data-ttu-id="2cb93-106">具有-Partial-Replica-Nc 屬性</span><span class="sxs-lookup"><span data-stu-id="2cb93-106">Has-Partial-Replica-NCs attribute</span></span>

<span data-ttu-id="2cb93-107">Nc 的同級。</span><span class="sxs-lookup"><span data-stu-id="2cb93-107">Sibling to Has-Master-NCs.</span></span> <span data-ttu-id="2cb93-108">具有-Partial-Nc 會反映所有其他已複寫到通用類別目錄的網域 Nc 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="2cb93-108">Has-Partial-Replica-NCs reflects the distinguished name for all other-domain NCs that have been replicated into a global catalog.</span></span>



| <span data-ttu-id="2cb93-109">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-109">Entry</span></span> | <span data-ttu-id="2cb93-110">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2cb93-111">CN</span><span class="sxs-lookup"><span data-stu-id="2cb93-111">CN</span></span>                | <span data-ttu-id="2cb93-112">具有-Partial-Replica-Nc</span><span class="sxs-lookup"><span data-stu-id="2cb93-112">Has-Partial-Replica-NCs</span></span>                 |
| <span data-ttu-id="2cb93-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2cb93-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2cb93-114">hasPartialReplicaNCs</span><span class="sxs-lookup"><span data-stu-id="2cb93-114">hasPartialReplicaNCs</span></span>                    |
| <span data-ttu-id="2cb93-115">大小</span><span class="sxs-lookup"><span data-stu-id="2cb93-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="2cb93-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2cb93-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2cb93-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2cb93-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2cb93-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-118">Attribute-Id</span></span>      | <span data-ttu-id="2cb93-119">1.2.840.113556.1.2.15</span><span class="sxs-lookup"><span data-stu-id="2cb93-119">1.2.840.113556.1.2.15</span></span>                   |
| <span data-ttu-id="2cb93-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2cb93-120">System-Id-Guid</span></span>    | <span data-ttu-id="2cb93-121">bf967981-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2cb93-121">bf967981-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="2cb93-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cb93-122">Syntax</span></span>            | [<span data-ttu-id="2cb93-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2cb93-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2cb93-124">實作</span><span class="sxs-lookup"><span data-stu-id="2cb93-124">Implementations</span></span>

-   [<span data-ttu-id="2cb93-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2cb93-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2cb93-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2cb93-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2cb93-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="2cb93-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2cb93-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2cb93-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2cb93-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2cb93-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2cb93-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2cb93-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2cb93-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2cb93-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2cb93-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2cb93-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2cb93-133">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-133">Entry</span></span> | <span data-ttu-id="2cb93-134">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb93-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2cb93-135">Link-Id</span></span>                | <span data-ttu-id="2cb93-136">74</span><span class="sxs-lookup"><span data-stu-id="2cb93-136">74</span></span>                                       |
| <span data-ttu-id="2cb93-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-137">MAPI-Id</span></span>                | <span data-ttu-id="2cb93-138">0x80B5</span><span class="sxs-lookup"><span data-stu-id="2cb93-138">0x80B5</span></span>                                   |
| <span data-ttu-id="2cb93-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb93-139">System-Only</span></span>            | <span data-ttu-id="2cb93-140">對</span><span class="sxs-lookup"><span data-stu-id="2cb93-140">True</span></span>                                     |
| <span data-ttu-id="2cb93-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2cb93-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb93-142">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-142">False</span></span>                                    |
| <span data-ttu-id="2cb93-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2cb93-143">Is Indexed</span></span>             | <span data-ttu-id="2cb93-144">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-144">False</span></span>                                    |
| <span data-ttu-id="2cb93-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2cb93-145">In Global Catalog</span></span>      | <span data-ttu-id="2cb93-146">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-146">False</span></span>                                    |
| <span data-ttu-id="2cb93-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2cb93-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb93-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2cb93-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb93-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb93-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb93-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-151">Search-Flags</span></span>           | <span data-ttu-id="2cb93-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cb93-152">0x00000000</span></span>                               |
| <span data-ttu-id="2cb93-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-153">System-Flags</span></span>           | <span data-ttu-id="2cb93-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb93-154">0x00000010</span></span>                               |
| <span data-ttu-id="2cb93-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2cb93-155">Classes used in</span></span>        | [<span data-ttu-id="2cb93-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2cb93-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2cb93-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2cb93-157">Windows Server 2003</span></span>



| <span data-ttu-id="2cb93-158">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-158">Entry</span></span> | <span data-ttu-id="2cb93-159">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb93-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2cb93-160">Link-Id</span></span>                | <span data-ttu-id="2cb93-161">74</span><span class="sxs-lookup"><span data-stu-id="2cb93-161">74</span></span>                                       |
| <span data-ttu-id="2cb93-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-162">MAPI-Id</span></span>                | <span data-ttu-id="2cb93-163">0x80B5</span><span class="sxs-lookup"><span data-stu-id="2cb93-163">0x80B5</span></span>                                   |
| <span data-ttu-id="2cb93-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb93-164">System-Only</span></span>            | <span data-ttu-id="2cb93-165">對</span><span class="sxs-lookup"><span data-stu-id="2cb93-165">True</span></span>                                     |
| <span data-ttu-id="2cb93-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2cb93-166">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb93-167">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-167">False</span></span>                                    |
| <span data-ttu-id="2cb93-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2cb93-168">Is Indexed</span></span>             | <span data-ttu-id="2cb93-169">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-169">False</span></span>                                    |
| <span data-ttu-id="2cb93-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2cb93-170">In Global Catalog</span></span>      | <span data-ttu-id="2cb93-171">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-171">False</span></span>                                    |
| <span data-ttu-id="2cb93-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2cb93-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb93-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2cb93-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb93-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb93-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb93-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-176">Search-Flags</span></span>           | <span data-ttu-id="2cb93-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cb93-177">0x00000000</span></span>                               |
| <span data-ttu-id="2cb93-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-178">System-Flags</span></span>           | <span data-ttu-id="2cb93-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb93-179">0x00000010</span></span>                               |
| <span data-ttu-id="2cb93-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2cb93-180">Classes used in</span></span>        | [<span data-ttu-id="2cb93-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2cb93-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2cb93-182">亞當</span><span class="sxs-lookup"><span data-stu-id="2cb93-182">ADAM</span></span>



| <span data-ttu-id="2cb93-183">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-183">Entry</span></span> | <span data-ttu-id="2cb93-184">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb93-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2cb93-185">Link-Id</span></span>                | <span data-ttu-id="2cb93-186">74</span><span class="sxs-lookup"><span data-stu-id="2cb93-186">74</span></span>                                       |
| <span data-ttu-id="2cb93-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-187">MAPI-Id</span></span>                | <span data-ttu-id="2cb93-188">0x80B5</span><span class="sxs-lookup"><span data-stu-id="2cb93-188">0x80B5</span></span>                                   |
| <span data-ttu-id="2cb93-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb93-189">System-Only</span></span>            | <span data-ttu-id="2cb93-190">對</span><span class="sxs-lookup"><span data-stu-id="2cb93-190">True</span></span>                                     |
| <span data-ttu-id="2cb93-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2cb93-191">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb93-192">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-192">False</span></span>                                    |
| <span data-ttu-id="2cb93-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2cb93-193">Is Indexed</span></span>             | <span data-ttu-id="2cb93-194">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-194">False</span></span>                                    |
| <span data-ttu-id="2cb93-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2cb93-195">In Global Catalog</span></span>      | <span data-ttu-id="2cb93-196">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-196">False</span></span>                                    |
| <span data-ttu-id="2cb93-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2cb93-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb93-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2cb93-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb93-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb93-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb93-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-201">Search-Flags</span></span>           | <span data-ttu-id="2cb93-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cb93-202">0x00000000</span></span>                               |
| <span data-ttu-id="2cb93-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-203">System-Flags</span></span>           | <span data-ttu-id="2cb93-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb93-204">0x00000010</span></span>                               |
| <span data-ttu-id="2cb93-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2cb93-205">Classes used in</span></span>        | [<span data-ttu-id="2cb93-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2cb93-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2cb93-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2cb93-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2cb93-208">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-208">Entry</span></span> | <span data-ttu-id="2cb93-209">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb93-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2cb93-210">Link-Id</span></span>                | <span data-ttu-id="2cb93-211">74</span><span class="sxs-lookup"><span data-stu-id="2cb93-211">74</span></span>                                       |
| <span data-ttu-id="2cb93-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-212">MAPI-Id</span></span>                | <span data-ttu-id="2cb93-213">0x80B5</span><span class="sxs-lookup"><span data-stu-id="2cb93-213">0x80B5</span></span>                                   |
| <span data-ttu-id="2cb93-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb93-214">System-Only</span></span>            | <span data-ttu-id="2cb93-215">對</span><span class="sxs-lookup"><span data-stu-id="2cb93-215">True</span></span>                                     |
| <span data-ttu-id="2cb93-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2cb93-216">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb93-217">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-217">False</span></span>                                    |
| <span data-ttu-id="2cb93-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2cb93-218">Is Indexed</span></span>             | <span data-ttu-id="2cb93-219">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-219">False</span></span>                                    |
| <span data-ttu-id="2cb93-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2cb93-220">In Global Catalog</span></span>      | <span data-ttu-id="2cb93-221">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-221">False</span></span>                                    |
| <span data-ttu-id="2cb93-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2cb93-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb93-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2cb93-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb93-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb93-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb93-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-226">Search-Flags</span></span>           | <span data-ttu-id="2cb93-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cb93-227">0x00000000</span></span>                               |
| <span data-ttu-id="2cb93-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-228">System-Flags</span></span>           | <span data-ttu-id="2cb93-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb93-229">0x00000010</span></span>                               |
| <span data-ttu-id="2cb93-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2cb93-230">Classes used in</span></span>        | [<span data-ttu-id="2cb93-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2cb93-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2cb93-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cb93-232">Windows Server 2008</span></span>



| <span data-ttu-id="2cb93-233">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-233">Entry</span></span> | <span data-ttu-id="2cb93-234">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb93-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2cb93-235">Link-Id</span></span>                | <span data-ttu-id="2cb93-236">74</span><span class="sxs-lookup"><span data-stu-id="2cb93-236">74</span></span>                                       |
| <span data-ttu-id="2cb93-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-237">MAPI-Id</span></span>                | <span data-ttu-id="2cb93-238">0x80B5</span><span class="sxs-lookup"><span data-stu-id="2cb93-238">0x80B5</span></span>                                   |
| <span data-ttu-id="2cb93-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb93-239">System-Only</span></span>            | <span data-ttu-id="2cb93-240">對</span><span class="sxs-lookup"><span data-stu-id="2cb93-240">True</span></span>                                     |
| <span data-ttu-id="2cb93-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2cb93-241">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb93-242">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-242">False</span></span>                                    |
| <span data-ttu-id="2cb93-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2cb93-243">Is Indexed</span></span>             | <span data-ttu-id="2cb93-244">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-244">False</span></span>                                    |
| <span data-ttu-id="2cb93-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2cb93-245">In Global Catalog</span></span>      | <span data-ttu-id="2cb93-246">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-246">False</span></span>                                    |
| <span data-ttu-id="2cb93-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2cb93-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb93-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2cb93-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb93-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb93-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb93-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-251">Search-Flags</span></span>           | <span data-ttu-id="2cb93-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cb93-252">0x00000000</span></span>                               |
| <span data-ttu-id="2cb93-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-253">System-Flags</span></span>           | <span data-ttu-id="2cb93-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb93-254">0x00000010</span></span>                               |
| <span data-ttu-id="2cb93-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2cb93-255">Classes used in</span></span>        | [<span data-ttu-id="2cb93-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2cb93-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2cb93-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2cb93-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2cb93-258">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-258">Entry</span></span> | <span data-ttu-id="2cb93-259">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb93-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2cb93-260">Link-Id</span></span>                | <span data-ttu-id="2cb93-261">74</span><span class="sxs-lookup"><span data-stu-id="2cb93-261">74</span></span>                                       |
| <span data-ttu-id="2cb93-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-262">MAPI-Id</span></span>                | <span data-ttu-id="2cb93-263">0x80B5</span><span class="sxs-lookup"><span data-stu-id="2cb93-263">0x80B5</span></span>                                   |
| <span data-ttu-id="2cb93-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb93-264">System-Only</span></span>            | <span data-ttu-id="2cb93-265">對</span><span class="sxs-lookup"><span data-stu-id="2cb93-265">True</span></span>                                     |
| <span data-ttu-id="2cb93-266">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2cb93-266">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb93-267">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-267">False</span></span>                                    |
| <span data-ttu-id="2cb93-268">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2cb93-268">Is Indexed</span></span>             | <span data-ttu-id="2cb93-269">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-269">False</span></span>                                    |
| <span data-ttu-id="2cb93-270">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2cb93-270">In Global Catalog</span></span>      | <span data-ttu-id="2cb93-271">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-271">False</span></span>                                    |
| <span data-ttu-id="2cb93-272">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2cb93-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb93-273">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2cb93-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb93-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb93-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb93-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-276">Search-Flags</span></span>           | <span data-ttu-id="2cb93-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cb93-277">0x00000000</span></span>                               |
| <span data-ttu-id="2cb93-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-278">System-Flags</span></span>           | <span data-ttu-id="2cb93-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb93-279">0x00000010</span></span>                               |
| <span data-ttu-id="2cb93-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2cb93-280">Classes used in</span></span>        | [<span data-ttu-id="2cb93-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2cb93-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2cb93-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cb93-282">Windows Server 2012</span></span>



| <span data-ttu-id="2cb93-283">進入</span><span class="sxs-lookup"><span data-stu-id="2cb93-283">Entry</span></span> | <span data-ttu-id="2cb93-284">值</span><span class="sxs-lookup"><span data-stu-id="2cb93-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb93-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2cb93-285">Link-Id</span></span>                | <span data-ttu-id="2cb93-286">74</span><span class="sxs-lookup"><span data-stu-id="2cb93-286">74</span></span>                                       |
| <span data-ttu-id="2cb93-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb93-287">MAPI-Id</span></span>                | <span data-ttu-id="2cb93-288">0x80B5</span><span class="sxs-lookup"><span data-stu-id="2cb93-288">0x80B5</span></span>                                   |
| <span data-ttu-id="2cb93-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb93-289">System-Only</span></span>            | <span data-ttu-id="2cb93-290">對</span><span class="sxs-lookup"><span data-stu-id="2cb93-290">True</span></span>                                     |
| <span data-ttu-id="2cb93-291">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2cb93-291">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb93-292">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-292">False</span></span>                                    |
| <span data-ttu-id="2cb93-293">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2cb93-293">Is Indexed</span></span>             | <span data-ttu-id="2cb93-294">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-294">False</span></span>                                    |
| <span data-ttu-id="2cb93-295">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2cb93-295">In Global Catalog</span></span>      | <span data-ttu-id="2cb93-296">否</span><span class="sxs-lookup"><span data-stu-id="2cb93-296">False</span></span>                                    |
| <span data-ttu-id="2cb93-297">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2cb93-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb93-298">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2cb93-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb93-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb93-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb93-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb93-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-301">Search-Flags</span></span>           | <span data-ttu-id="2cb93-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2cb93-302">0x00000000</span></span>                               |
| <span data-ttu-id="2cb93-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb93-303">System-Flags</span></span>           | <span data-ttu-id="2cb93-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb93-304">0x00000010</span></span>                               |
| <span data-ttu-id="2cb93-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2cb93-305">Classes used in</span></span>        | [<span data-ttu-id="2cb93-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2cb93-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





