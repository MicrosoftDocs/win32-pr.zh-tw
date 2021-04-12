---
title: Trust-Type 屬性
description: 信任類型，例如 Windows NT 或 MIT。
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Trust-Type 屬性 AD 架構
- trustType 屬性 AD 架構
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b8a8f59f7df976f968bb4f2915e667a06e95bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935345"
---
# <a name="trust-type-attribute"></a><span data-ttu-id="ffc69-105">Trust-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="ffc69-105">Trust-Type attribute</span></span>

<span data-ttu-id="ffc69-106">信任類型，例如 Windows NT 或 MIT。</span><span class="sxs-lookup"><span data-stu-id="ffc69-106">The type of trust, for example, Windows NT or MIT.</span></span>



| <span data-ttu-id="ffc69-107">進入</span><span class="sxs-lookup"><span data-stu-id="ffc69-107">Entry</span></span> | <span data-ttu-id="ffc69-108">值</span><span class="sxs-lookup"><span data-stu-id="ffc69-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ffc69-109">CN</span><span class="sxs-lookup"><span data-stu-id="ffc69-109">CN</span></span>                | <span data-ttu-id="ffc69-110">Trust-Type</span><span class="sxs-lookup"><span data-stu-id="ffc69-110">Trust-Type</span></span>                           |
| <span data-ttu-id="ffc69-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ffc69-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ffc69-112">trustType</span><span class="sxs-lookup"><span data-stu-id="ffc69-112">trustType</span></span>                            |
| <span data-ttu-id="ffc69-113">大小</span><span class="sxs-lookup"><span data-stu-id="ffc69-113">Size</span></span>              | <span data-ttu-id="ffc69-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ffc69-114">4 bytes</span></span>                              |
| <span data-ttu-id="ffc69-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ffc69-115">Update Privilege</span></span>  | <span data-ttu-id="ffc69-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ffc69-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ffc69-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ffc69-117">Update Frequency</span></span>  | <span data-ttu-id="ffc69-118">當新的信任建立時。</span><span class="sxs-lookup"><span data-stu-id="ffc69-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="ffc69-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffc69-119">Attribute-Id</span></span>      | <span data-ttu-id="ffc69-120">1.2.840.113556.1.4.136</span><span class="sxs-lookup"><span data-stu-id="ffc69-120">1.2.840.113556.1.4.136</span></span>               |
| <span data-ttu-id="ffc69-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ffc69-121">System-Id-Guid</span></span>    | <span data-ttu-id="ffc69-122">bf967a60-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ffc69-122">bf967a60-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ffc69-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffc69-123">Syntax</span></span>            | [<span data-ttu-id="ffc69-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ffc69-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ffc69-125">實作</span><span class="sxs-lookup"><span data-stu-id="ffc69-125">Implementations</span></span>

-   [<span data-ttu-id="ffc69-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ffc69-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ffc69-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ffc69-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ffc69-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffc69-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffc69-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffc69-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffc69-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffc69-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffc69-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffc69-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ffc69-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffc69-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ffc69-133">進入</span><span class="sxs-lookup"><span data-stu-id="ffc69-133">Entry</span></span> | <span data-ttu-id="ffc69-134">值</span><span class="sxs-lookup"><span data-stu-id="ffc69-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ffc69-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffc69-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffc69-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffc69-137">System-Only</span></span>            | <span data-ttu-id="ffc69-138">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-138">False</span></span>                                                |
| <span data-ttu-id="ffc69-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffc69-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ffc69-140">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-140">True</span></span>                                                 |
| <span data-ttu-id="ffc69-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffc69-141">Is Indexed</span></span>             | <span data-ttu-id="ffc69-142">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-142">False</span></span>                                                |
| <span data-ttu-id="ffc69-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffc69-143">In Global Catalog</span></span>      | <span data-ttu-id="ffc69-144">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-144">False</span></span>                                                |
| <span data-ttu-id="ffc69-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffc69-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffc69-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffc69-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ffc69-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffc69-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffc69-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-149">Search-Flags</span></span>           | <span data-ttu-id="ffc69-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffc69-150">0x00000000</span></span>                                           |
| <span data-ttu-id="ffc69-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-151">System-Flags</span></span>           | <span data-ttu-id="ffc69-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffc69-152">0x00000010</span></span>                                           |
| <span data-ttu-id="ffc69-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffc69-153">Classes used in</span></span>        | [<span data-ttu-id="ffc69-154">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ffc69-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ffc69-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffc69-155">Windows Server 2003</span></span>



| <span data-ttu-id="ffc69-156">進入</span><span class="sxs-lookup"><span data-stu-id="ffc69-156">Entry</span></span> | <span data-ttu-id="ffc69-157">值</span><span class="sxs-lookup"><span data-stu-id="ffc69-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ffc69-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffc69-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffc69-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffc69-160">System-Only</span></span>            | <span data-ttu-id="ffc69-161">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-161">False</span></span>                                                |
| <span data-ttu-id="ffc69-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffc69-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ffc69-163">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-163">True</span></span>                                                 |
| <span data-ttu-id="ffc69-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffc69-164">Is Indexed</span></span>             | <span data-ttu-id="ffc69-165">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-165">False</span></span>                                                |
| <span data-ttu-id="ffc69-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffc69-166">In Global Catalog</span></span>      | <span data-ttu-id="ffc69-167">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-167">True</span></span>                                                 |
| <span data-ttu-id="ffc69-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffc69-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffc69-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffc69-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ffc69-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffc69-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffc69-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-172">Search-Flags</span></span>           | <span data-ttu-id="ffc69-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffc69-173">0x00000000</span></span>                                           |
| <span data-ttu-id="ffc69-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-174">System-Flags</span></span>           | <span data-ttu-id="ffc69-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffc69-175">0x00000010</span></span>                                           |
| <span data-ttu-id="ffc69-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffc69-176">Classes used in</span></span>        | [<span data-ttu-id="ffc69-177">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ffc69-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffc69-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffc69-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffc69-179">進入</span><span class="sxs-lookup"><span data-stu-id="ffc69-179">Entry</span></span> | <span data-ttu-id="ffc69-180">值</span><span class="sxs-lookup"><span data-stu-id="ffc69-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ffc69-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffc69-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffc69-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffc69-183">System-Only</span></span>            | <span data-ttu-id="ffc69-184">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-184">False</span></span>                                                |
| <span data-ttu-id="ffc69-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffc69-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ffc69-186">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-186">True</span></span>                                                 |
| <span data-ttu-id="ffc69-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffc69-187">Is Indexed</span></span>             | <span data-ttu-id="ffc69-188">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-188">False</span></span>                                                |
| <span data-ttu-id="ffc69-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffc69-189">In Global Catalog</span></span>      | <span data-ttu-id="ffc69-190">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-190">True</span></span>                                                 |
| <span data-ttu-id="ffc69-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffc69-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffc69-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffc69-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ffc69-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffc69-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffc69-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-195">Search-Flags</span></span>           | <span data-ttu-id="ffc69-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffc69-196">0x00000000</span></span>                                           |
| <span data-ttu-id="ffc69-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-197">System-Flags</span></span>           | <span data-ttu-id="ffc69-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffc69-198">0x00000010</span></span>                                           |
| <span data-ttu-id="ffc69-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffc69-199">Classes used in</span></span>        | [<span data-ttu-id="ffc69-200">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ffc69-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffc69-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffc69-201">Windows Server 2008</span></span>



| <span data-ttu-id="ffc69-202">進入</span><span class="sxs-lookup"><span data-stu-id="ffc69-202">Entry</span></span> | <span data-ttu-id="ffc69-203">值</span><span class="sxs-lookup"><span data-stu-id="ffc69-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ffc69-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffc69-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffc69-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffc69-206">System-Only</span></span>            | <span data-ttu-id="ffc69-207">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-207">False</span></span>                                                |
| <span data-ttu-id="ffc69-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffc69-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ffc69-209">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-209">True</span></span>                                                 |
| <span data-ttu-id="ffc69-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffc69-210">Is Indexed</span></span>             | <span data-ttu-id="ffc69-211">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-211">False</span></span>                                                |
| <span data-ttu-id="ffc69-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffc69-212">In Global Catalog</span></span>      | <span data-ttu-id="ffc69-213">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-213">True</span></span>                                                 |
| <span data-ttu-id="ffc69-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffc69-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffc69-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffc69-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ffc69-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffc69-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffc69-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-218">Search-Flags</span></span>           | <span data-ttu-id="ffc69-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffc69-219">0x00000000</span></span>                                           |
| <span data-ttu-id="ffc69-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-220">System-Flags</span></span>           | <span data-ttu-id="ffc69-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffc69-221">0x00000010</span></span>                                           |
| <span data-ttu-id="ffc69-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffc69-222">Classes used in</span></span>        | [<span data-ttu-id="ffc69-223">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ffc69-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffc69-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffc69-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffc69-225">進入</span><span class="sxs-lookup"><span data-stu-id="ffc69-225">Entry</span></span> | <span data-ttu-id="ffc69-226">值</span><span class="sxs-lookup"><span data-stu-id="ffc69-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ffc69-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffc69-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffc69-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffc69-229">System-Only</span></span>            | <span data-ttu-id="ffc69-230">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-230">False</span></span>                                                |
| <span data-ttu-id="ffc69-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffc69-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ffc69-232">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-232">True</span></span>                                                 |
| <span data-ttu-id="ffc69-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffc69-233">Is Indexed</span></span>             | <span data-ttu-id="ffc69-234">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-234">False</span></span>                                                |
| <span data-ttu-id="ffc69-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffc69-235">In Global Catalog</span></span>      | <span data-ttu-id="ffc69-236">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-236">True</span></span>                                                 |
| <span data-ttu-id="ffc69-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffc69-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffc69-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffc69-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ffc69-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffc69-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffc69-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-241">Search-Flags</span></span>           | <span data-ttu-id="ffc69-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffc69-242">0x00000000</span></span>                                           |
| <span data-ttu-id="ffc69-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-243">System-Flags</span></span>           | <span data-ttu-id="ffc69-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffc69-244">0x00000010</span></span>                                           |
| <span data-ttu-id="ffc69-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffc69-245">Classes used in</span></span>        | [<span data-ttu-id="ffc69-246">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ffc69-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffc69-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffc69-247">Windows Server 2012</span></span>



| <span data-ttu-id="ffc69-248">進入</span><span class="sxs-lookup"><span data-stu-id="ffc69-248">Entry</span></span> | <span data-ttu-id="ffc69-249">值</span><span class="sxs-lookup"><span data-stu-id="ffc69-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ffc69-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ffc69-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffc69-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ffc69-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffc69-252">System-Only</span></span>            | <span data-ttu-id="ffc69-253">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-253">False</span></span>                                                |
| <span data-ttu-id="ffc69-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ffc69-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ffc69-255">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-255">True</span></span>                                                 |
| <span data-ttu-id="ffc69-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ffc69-256">Is Indexed</span></span>             | <span data-ttu-id="ffc69-257">否</span><span class="sxs-lookup"><span data-stu-id="ffc69-257">False</span></span>                                                |
| <span data-ttu-id="ffc69-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ffc69-258">In Global Catalog</span></span>      | <span data-ttu-id="ffc69-259">對</span><span class="sxs-lookup"><span data-stu-id="ffc69-259">True</span></span>                                                 |
| <span data-ttu-id="ffc69-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ffc69-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffc69-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ffc69-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ffc69-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffc69-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffc69-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ffc69-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-264">Search-Flags</span></span>           | <span data-ttu-id="ffc69-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffc69-265">0x00000000</span></span>                                           |
| <span data-ttu-id="ffc69-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffc69-266">System-Flags</span></span>           | <span data-ttu-id="ffc69-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffc69-267">0x00000010</span></span>                                           |
| <span data-ttu-id="ffc69-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ffc69-268">Classes used in</span></span>        | [<span data-ttu-id="ffc69-269">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ffc69-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





