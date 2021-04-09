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
# <a name="has-partial-replica-ncs-attribute"></a><span data-ttu-id="7732f-106">具有-Partial-Replica-Nc 屬性</span><span class="sxs-lookup"><span data-stu-id="7732f-106">Has-Partial-Replica-NCs attribute</span></span>

<span data-ttu-id="7732f-107">Nc 的同級。</span><span class="sxs-lookup"><span data-stu-id="7732f-107">Sibling to Has-Master-NCs.</span></span> <span data-ttu-id="7732f-108">具有-Partial-Nc 會反映所有其他已複寫到通用類別目錄的網域 Nc 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="7732f-108">Has-Partial-Replica-NCs reflects the distinguished name for all other-domain NCs that have been replicated into a global catalog.</span></span>



| <span data-ttu-id="7732f-109">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-109">Entry</span></span> | <span data-ttu-id="7732f-110">值</span><span class="sxs-lookup"><span data-stu-id="7732f-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7732f-111">CN</span><span class="sxs-lookup"><span data-stu-id="7732f-111">CN</span></span>                | <span data-ttu-id="7732f-112">具有-Partial-Replica-Nc</span><span class="sxs-lookup"><span data-stu-id="7732f-112">Has-Partial-Replica-NCs</span></span>                 |
| <span data-ttu-id="7732f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7732f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7732f-114">hasPartialReplicaNCs</span><span class="sxs-lookup"><span data-stu-id="7732f-114">hasPartialReplicaNCs</span></span>                    |
| <span data-ttu-id="7732f-115">大小</span><span class="sxs-lookup"><span data-stu-id="7732f-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="7732f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7732f-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7732f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7732f-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7732f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-118">Attribute-Id</span></span>      | <span data-ttu-id="7732f-119">1.2.840.113556.1.2.15</span><span class="sxs-lookup"><span data-stu-id="7732f-119">1.2.840.113556.1.2.15</span></span>                   |
| <span data-ttu-id="7732f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7732f-120">System-Id-Guid</span></span>    | <span data-ttu-id="7732f-121">bf967981-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7732f-121">bf967981-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="7732f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7732f-122">Syntax</span></span>            | [<span data-ttu-id="7732f-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7732f-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7732f-124">實作</span><span class="sxs-lookup"><span data-stu-id="7732f-124">Implementations</span></span>

-   [<span data-ttu-id="7732f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7732f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7732f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7732f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7732f-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7732f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7732f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7732f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7732f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7732f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7732f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7732f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7732f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7732f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7732f-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7732f-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7732f-133">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-133">Entry</span></span> | <span data-ttu-id="7732f-134">值</span><span class="sxs-lookup"><span data-stu-id="7732f-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7732f-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7732f-135">Link-Id</span></span>                | <span data-ttu-id="7732f-136">74</span><span class="sxs-lookup"><span data-stu-id="7732f-136">74</span></span>                                       |
| <span data-ttu-id="7732f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-137">MAPI-Id</span></span>                | <span data-ttu-id="7732f-138">0x80B5</span><span class="sxs-lookup"><span data-stu-id="7732f-138">0x80B5</span></span>                                   |
| <span data-ttu-id="7732f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7732f-139">System-Only</span></span>            | <span data-ttu-id="7732f-140">對</span><span class="sxs-lookup"><span data-stu-id="7732f-140">True</span></span>                                     |
| <span data-ttu-id="7732f-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7732f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7732f-142">否</span><span class="sxs-lookup"><span data-stu-id="7732f-142">False</span></span>                                    |
| <span data-ttu-id="7732f-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7732f-143">Is Indexed</span></span>             | <span data-ttu-id="7732f-144">否</span><span class="sxs-lookup"><span data-stu-id="7732f-144">False</span></span>                                    |
| <span data-ttu-id="7732f-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7732f-145">In Global Catalog</span></span>      | <span data-ttu-id="7732f-146">否</span><span class="sxs-lookup"><span data-stu-id="7732f-146">False</span></span>                                    |
| <span data-ttu-id="7732f-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7732f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7732f-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7732f-148">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7732f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7732f-149">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7732f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7732f-150">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7732f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-151">Search-Flags</span></span>           | <span data-ttu-id="7732f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7732f-152">0x00000000</span></span>                               |
| <span data-ttu-id="7732f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-153">System-Flags</span></span>           | <span data-ttu-id="7732f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7732f-154">0x00000010</span></span>                               |
| <span data-ttu-id="7732f-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7732f-155">Classes used in</span></span>        | [<span data-ttu-id="7732f-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7732f-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7732f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7732f-157">Windows Server 2003</span></span>



| <span data-ttu-id="7732f-158">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-158">Entry</span></span> | <span data-ttu-id="7732f-159">值</span><span class="sxs-lookup"><span data-stu-id="7732f-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7732f-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7732f-160">Link-Id</span></span>                | <span data-ttu-id="7732f-161">74</span><span class="sxs-lookup"><span data-stu-id="7732f-161">74</span></span>                                       |
| <span data-ttu-id="7732f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-162">MAPI-Id</span></span>                | <span data-ttu-id="7732f-163">0x80B5</span><span class="sxs-lookup"><span data-stu-id="7732f-163">0x80B5</span></span>                                   |
| <span data-ttu-id="7732f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="7732f-164">System-Only</span></span>            | <span data-ttu-id="7732f-165">對</span><span class="sxs-lookup"><span data-stu-id="7732f-165">True</span></span>                                     |
| <span data-ttu-id="7732f-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7732f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="7732f-167">否</span><span class="sxs-lookup"><span data-stu-id="7732f-167">False</span></span>                                    |
| <span data-ttu-id="7732f-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7732f-168">Is Indexed</span></span>             | <span data-ttu-id="7732f-169">否</span><span class="sxs-lookup"><span data-stu-id="7732f-169">False</span></span>                                    |
| <span data-ttu-id="7732f-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7732f-170">In Global Catalog</span></span>      | <span data-ttu-id="7732f-171">否</span><span class="sxs-lookup"><span data-stu-id="7732f-171">False</span></span>                                    |
| <span data-ttu-id="7732f-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7732f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="7732f-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7732f-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7732f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7732f-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7732f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7732f-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7732f-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-176">Search-Flags</span></span>           | <span data-ttu-id="7732f-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7732f-177">0x00000000</span></span>                               |
| <span data-ttu-id="7732f-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-178">System-Flags</span></span>           | <span data-ttu-id="7732f-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7732f-179">0x00000010</span></span>                               |
| <span data-ttu-id="7732f-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7732f-180">Classes used in</span></span>        | [<span data-ttu-id="7732f-181">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7732f-181">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7732f-182">亞當</span><span class="sxs-lookup"><span data-stu-id="7732f-182">ADAM</span></span>



| <span data-ttu-id="7732f-183">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-183">Entry</span></span> | <span data-ttu-id="7732f-184">值</span><span class="sxs-lookup"><span data-stu-id="7732f-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7732f-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7732f-185">Link-Id</span></span>                | <span data-ttu-id="7732f-186">74</span><span class="sxs-lookup"><span data-stu-id="7732f-186">74</span></span>                                       |
| <span data-ttu-id="7732f-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-187">MAPI-Id</span></span>                | <span data-ttu-id="7732f-188">0x80B5</span><span class="sxs-lookup"><span data-stu-id="7732f-188">0x80B5</span></span>                                   |
| <span data-ttu-id="7732f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="7732f-189">System-Only</span></span>            | <span data-ttu-id="7732f-190">對</span><span class="sxs-lookup"><span data-stu-id="7732f-190">True</span></span>                                     |
| <span data-ttu-id="7732f-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7732f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="7732f-192">否</span><span class="sxs-lookup"><span data-stu-id="7732f-192">False</span></span>                                    |
| <span data-ttu-id="7732f-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7732f-193">Is Indexed</span></span>             | <span data-ttu-id="7732f-194">否</span><span class="sxs-lookup"><span data-stu-id="7732f-194">False</span></span>                                    |
| <span data-ttu-id="7732f-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7732f-195">In Global Catalog</span></span>      | <span data-ttu-id="7732f-196">否</span><span class="sxs-lookup"><span data-stu-id="7732f-196">False</span></span>                                    |
| <span data-ttu-id="7732f-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7732f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="7732f-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7732f-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7732f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7732f-199">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7732f-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7732f-200">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7732f-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-201">Search-Flags</span></span>           | <span data-ttu-id="7732f-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7732f-202">0x00000000</span></span>                               |
| <span data-ttu-id="7732f-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-203">System-Flags</span></span>           | <span data-ttu-id="7732f-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7732f-204">0x00000010</span></span>                               |
| <span data-ttu-id="7732f-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7732f-205">Classes used in</span></span>        | [<span data-ttu-id="7732f-206">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7732f-206">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7732f-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7732f-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7732f-208">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-208">Entry</span></span> | <span data-ttu-id="7732f-209">值</span><span class="sxs-lookup"><span data-stu-id="7732f-209">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7732f-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7732f-210">Link-Id</span></span>                | <span data-ttu-id="7732f-211">74</span><span class="sxs-lookup"><span data-stu-id="7732f-211">74</span></span>                                       |
| <span data-ttu-id="7732f-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-212">MAPI-Id</span></span>                | <span data-ttu-id="7732f-213">0x80B5</span><span class="sxs-lookup"><span data-stu-id="7732f-213">0x80B5</span></span>                                   |
| <span data-ttu-id="7732f-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="7732f-214">System-Only</span></span>            | <span data-ttu-id="7732f-215">對</span><span class="sxs-lookup"><span data-stu-id="7732f-215">True</span></span>                                     |
| <span data-ttu-id="7732f-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7732f-216">Is-Single-Valued</span></span>       | <span data-ttu-id="7732f-217">否</span><span class="sxs-lookup"><span data-stu-id="7732f-217">False</span></span>                                    |
| <span data-ttu-id="7732f-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7732f-218">Is Indexed</span></span>             | <span data-ttu-id="7732f-219">否</span><span class="sxs-lookup"><span data-stu-id="7732f-219">False</span></span>                                    |
| <span data-ttu-id="7732f-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7732f-220">In Global Catalog</span></span>      | <span data-ttu-id="7732f-221">否</span><span class="sxs-lookup"><span data-stu-id="7732f-221">False</span></span>                                    |
| <span data-ttu-id="7732f-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7732f-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="7732f-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7732f-223">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7732f-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7732f-224">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7732f-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7732f-225">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7732f-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-226">Search-Flags</span></span>           | <span data-ttu-id="7732f-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7732f-227">0x00000000</span></span>                               |
| <span data-ttu-id="7732f-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-228">System-Flags</span></span>           | <span data-ttu-id="7732f-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7732f-229">0x00000010</span></span>                               |
| <span data-ttu-id="7732f-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7732f-230">Classes used in</span></span>        | [<span data-ttu-id="7732f-231">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7732f-231">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7732f-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7732f-232">Windows Server 2008</span></span>



| <span data-ttu-id="7732f-233">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-233">Entry</span></span> | <span data-ttu-id="7732f-234">值</span><span class="sxs-lookup"><span data-stu-id="7732f-234">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7732f-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7732f-235">Link-Id</span></span>                | <span data-ttu-id="7732f-236">74</span><span class="sxs-lookup"><span data-stu-id="7732f-236">74</span></span>                                       |
| <span data-ttu-id="7732f-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-237">MAPI-Id</span></span>                | <span data-ttu-id="7732f-238">0x80B5</span><span class="sxs-lookup"><span data-stu-id="7732f-238">0x80B5</span></span>                                   |
| <span data-ttu-id="7732f-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="7732f-239">System-Only</span></span>            | <span data-ttu-id="7732f-240">對</span><span class="sxs-lookup"><span data-stu-id="7732f-240">True</span></span>                                     |
| <span data-ttu-id="7732f-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7732f-241">Is-Single-Valued</span></span>       | <span data-ttu-id="7732f-242">否</span><span class="sxs-lookup"><span data-stu-id="7732f-242">False</span></span>                                    |
| <span data-ttu-id="7732f-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7732f-243">Is Indexed</span></span>             | <span data-ttu-id="7732f-244">否</span><span class="sxs-lookup"><span data-stu-id="7732f-244">False</span></span>                                    |
| <span data-ttu-id="7732f-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7732f-245">In Global Catalog</span></span>      | <span data-ttu-id="7732f-246">否</span><span class="sxs-lookup"><span data-stu-id="7732f-246">False</span></span>                                    |
| <span data-ttu-id="7732f-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7732f-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="7732f-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7732f-248">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7732f-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7732f-249">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7732f-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7732f-250">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7732f-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-251">Search-Flags</span></span>           | <span data-ttu-id="7732f-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7732f-252">0x00000000</span></span>                               |
| <span data-ttu-id="7732f-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-253">System-Flags</span></span>           | <span data-ttu-id="7732f-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7732f-254">0x00000010</span></span>                               |
| <span data-ttu-id="7732f-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7732f-255">Classes used in</span></span>        | [<span data-ttu-id="7732f-256">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7732f-256">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7732f-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7732f-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7732f-258">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-258">Entry</span></span> | <span data-ttu-id="7732f-259">值</span><span class="sxs-lookup"><span data-stu-id="7732f-259">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7732f-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7732f-260">Link-Id</span></span>                | <span data-ttu-id="7732f-261">74</span><span class="sxs-lookup"><span data-stu-id="7732f-261">74</span></span>                                       |
| <span data-ttu-id="7732f-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-262">MAPI-Id</span></span>                | <span data-ttu-id="7732f-263">0x80B5</span><span class="sxs-lookup"><span data-stu-id="7732f-263">0x80B5</span></span>                                   |
| <span data-ttu-id="7732f-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="7732f-264">System-Only</span></span>            | <span data-ttu-id="7732f-265">對</span><span class="sxs-lookup"><span data-stu-id="7732f-265">True</span></span>                                     |
| <span data-ttu-id="7732f-266">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7732f-266">Is-Single-Valued</span></span>       | <span data-ttu-id="7732f-267">否</span><span class="sxs-lookup"><span data-stu-id="7732f-267">False</span></span>                                    |
| <span data-ttu-id="7732f-268">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7732f-268">Is Indexed</span></span>             | <span data-ttu-id="7732f-269">否</span><span class="sxs-lookup"><span data-stu-id="7732f-269">False</span></span>                                    |
| <span data-ttu-id="7732f-270">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7732f-270">In Global Catalog</span></span>      | <span data-ttu-id="7732f-271">否</span><span class="sxs-lookup"><span data-stu-id="7732f-271">False</span></span>                                    |
| <span data-ttu-id="7732f-272">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7732f-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="7732f-273">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7732f-273">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7732f-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7732f-274">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7732f-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7732f-275">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7732f-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-276">Search-Flags</span></span>           | <span data-ttu-id="7732f-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7732f-277">0x00000000</span></span>                               |
| <span data-ttu-id="7732f-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-278">System-Flags</span></span>           | <span data-ttu-id="7732f-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7732f-279">0x00000010</span></span>                               |
| <span data-ttu-id="7732f-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7732f-280">Classes used in</span></span>        | [<span data-ttu-id="7732f-281">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7732f-281">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7732f-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7732f-282">Windows Server 2012</span></span>



| <span data-ttu-id="7732f-283">進入</span><span class="sxs-lookup"><span data-stu-id="7732f-283">Entry</span></span> | <span data-ttu-id="7732f-284">值</span><span class="sxs-lookup"><span data-stu-id="7732f-284">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7732f-285">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7732f-285">Link-Id</span></span>                | <span data-ttu-id="7732f-286">74</span><span class="sxs-lookup"><span data-stu-id="7732f-286">74</span></span>                                       |
| <span data-ttu-id="7732f-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7732f-287">MAPI-Id</span></span>                | <span data-ttu-id="7732f-288">0x80B5</span><span class="sxs-lookup"><span data-stu-id="7732f-288">0x80B5</span></span>                                   |
| <span data-ttu-id="7732f-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="7732f-289">System-Only</span></span>            | <span data-ttu-id="7732f-290">對</span><span class="sxs-lookup"><span data-stu-id="7732f-290">True</span></span>                                     |
| <span data-ttu-id="7732f-291">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7732f-291">Is-Single-Valued</span></span>       | <span data-ttu-id="7732f-292">否</span><span class="sxs-lookup"><span data-stu-id="7732f-292">False</span></span>                                    |
| <span data-ttu-id="7732f-293">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7732f-293">Is Indexed</span></span>             | <span data-ttu-id="7732f-294">否</span><span class="sxs-lookup"><span data-stu-id="7732f-294">False</span></span>                                    |
| <span data-ttu-id="7732f-295">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7732f-295">In Global Catalog</span></span>      | <span data-ttu-id="7732f-296">否</span><span class="sxs-lookup"><span data-stu-id="7732f-296">False</span></span>                                    |
| <span data-ttu-id="7732f-297">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7732f-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="7732f-298">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7732f-298">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7732f-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7732f-299">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7732f-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7732f-300">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7732f-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-301">Search-Flags</span></span>           | <span data-ttu-id="7732f-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7732f-302">0x00000000</span></span>                               |
| <span data-ttu-id="7732f-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7732f-303">System-Flags</span></span>           | <span data-ttu-id="7732f-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7732f-304">0x00000010</span></span>                               |
| <span data-ttu-id="7732f-305">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7732f-305">Classes used in</span></span>        | [<span data-ttu-id="7732f-306">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7732f-306">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





