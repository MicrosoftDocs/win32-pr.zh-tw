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
# <a name="trust-type-attribute"></a><span data-ttu-id="ea765-105">Trust-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="ea765-105">Trust-Type attribute</span></span>

<span data-ttu-id="ea765-106">信任類型，例如 Windows NT 或 MIT。</span><span class="sxs-lookup"><span data-stu-id="ea765-106">The type of trust, for example, Windows NT or MIT.</span></span>



| <span data-ttu-id="ea765-107">進入</span><span class="sxs-lookup"><span data-stu-id="ea765-107">Entry</span></span> | <span data-ttu-id="ea765-108">值</span><span class="sxs-lookup"><span data-stu-id="ea765-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ea765-109">CN</span><span class="sxs-lookup"><span data-stu-id="ea765-109">CN</span></span>                | <span data-ttu-id="ea765-110">Trust-Type</span><span class="sxs-lookup"><span data-stu-id="ea765-110">Trust-Type</span></span>                           |
| <span data-ttu-id="ea765-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ea765-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ea765-112">trustType</span><span class="sxs-lookup"><span data-stu-id="ea765-112">trustType</span></span>                            |
| <span data-ttu-id="ea765-113">大小</span><span class="sxs-lookup"><span data-stu-id="ea765-113">Size</span></span>              | <span data-ttu-id="ea765-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ea765-114">4 bytes</span></span>                              |
| <span data-ttu-id="ea765-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ea765-115">Update Privilege</span></span>  | <span data-ttu-id="ea765-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="ea765-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="ea765-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ea765-117">Update Frequency</span></span>  | <span data-ttu-id="ea765-118">當新的信任建立時。</span><span class="sxs-lookup"><span data-stu-id="ea765-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="ea765-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ea765-119">Attribute-Id</span></span>      | <span data-ttu-id="ea765-120">1.2.840.113556.1.4.136</span><span class="sxs-lookup"><span data-stu-id="ea765-120">1.2.840.113556.1.4.136</span></span>               |
| <span data-ttu-id="ea765-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ea765-121">System-Id-Guid</span></span>    | <span data-ttu-id="ea765-122">bf967a60-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ea765-122">bf967a60-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ea765-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea765-123">Syntax</span></span>            | [<span data-ttu-id="ea765-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="ea765-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ea765-125">實作</span><span class="sxs-lookup"><span data-stu-id="ea765-125">Implementations</span></span>

-   [<span data-ttu-id="ea765-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ea765-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ea765-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ea765-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ea765-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ea765-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ea765-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ea765-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ea765-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ea765-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ea765-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ea765-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ea765-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea765-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ea765-133">進入</span><span class="sxs-lookup"><span data-stu-id="ea765-133">Entry</span></span> | <span data-ttu-id="ea765-134">值</span><span class="sxs-lookup"><span data-stu-id="ea765-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ea765-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ea765-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea765-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea765-137">System-Only</span></span>            | <span data-ttu-id="ea765-138">否</span><span class="sxs-lookup"><span data-stu-id="ea765-138">False</span></span>                                                |
| <span data-ttu-id="ea765-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ea765-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ea765-140">對</span><span class="sxs-lookup"><span data-stu-id="ea765-140">True</span></span>                                                 |
| <span data-ttu-id="ea765-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ea765-141">Is Indexed</span></span>             | <span data-ttu-id="ea765-142">否</span><span class="sxs-lookup"><span data-stu-id="ea765-142">False</span></span>                                                |
| <span data-ttu-id="ea765-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ea765-143">In Global Catalog</span></span>      | <span data-ttu-id="ea765-144">否</span><span class="sxs-lookup"><span data-stu-id="ea765-144">False</span></span>                                                |
| <span data-ttu-id="ea765-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ea765-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea765-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ea765-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ea765-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea765-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea765-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-149">Search-Flags</span></span>           | <span data-ttu-id="ea765-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea765-150">0x00000000</span></span>                                           |
| <span data-ttu-id="ea765-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-151">System-Flags</span></span>           | <span data-ttu-id="ea765-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea765-152">0x00000010</span></span>                                           |
| <span data-ttu-id="ea765-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ea765-153">Classes used in</span></span>        | [<span data-ttu-id="ea765-154">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ea765-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ea765-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea765-155">Windows Server 2003</span></span>



| <span data-ttu-id="ea765-156">進入</span><span class="sxs-lookup"><span data-stu-id="ea765-156">Entry</span></span> | <span data-ttu-id="ea765-157">值</span><span class="sxs-lookup"><span data-stu-id="ea765-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ea765-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ea765-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea765-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea765-160">System-Only</span></span>            | <span data-ttu-id="ea765-161">否</span><span class="sxs-lookup"><span data-stu-id="ea765-161">False</span></span>                                                |
| <span data-ttu-id="ea765-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ea765-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ea765-163">對</span><span class="sxs-lookup"><span data-stu-id="ea765-163">True</span></span>                                                 |
| <span data-ttu-id="ea765-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ea765-164">Is Indexed</span></span>             | <span data-ttu-id="ea765-165">否</span><span class="sxs-lookup"><span data-stu-id="ea765-165">False</span></span>                                                |
| <span data-ttu-id="ea765-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ea765-166">In Global Catalog</span></span>      | <span data-ttu-id="ea765-167">對</span><span class="sxs-lookup"><span data-stu-id="ea765-167">True</span></span>                                                 |
| <span data-ttu-id="ea765-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ea765-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea765-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ea765-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ea765-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea765-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea765-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-172">Search-Flags</span></span>           | <span data-ttu-id="ea765-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea765-173">0x00000000</span></span>                                           |
| <span data-ttu-id="ea765-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-174">System-Flags</span></span>           | <span data-ttu-id="ea765-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea765-175">0x00000010</span></span>                                           |
| <span data-ttu-id="ea765-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ea765-176">Classes used in</span></span>        | [<span data-ttu-id="ea765-177">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ea765-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ea765-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ea765-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ea765-179">進入</span><span class="sxs-lookup"><span data-stu-id="ea765-179">Entry</span></span> | <span data-ttu-id="ea765-180">值</span><span class="sxs-lookup"><span data-stu-id="ea765-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ea765-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ea765-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea765-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea765-183">System-Only</span></span>            | <span data-ttu-id="ea765-184">否</span><span class="sxs-lookup"><span data-stu-id="ea765-184">False</span></span>                                                |
| <span data-ttu-id="ea765-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ea765-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ea765-186">對</span><span class="sxs-lookup"><span data-stu-id="ea765-186">True</span></span>                                                 |
| <span data-ttu-id="ea765-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ea765-187">Is Indexed</span></span>             | <span data-ttu-id="ea765-188">否</span><span class="sxs-lookup"><span data-stu-id="ea765-188">False</span></span>                                                |
| <span data-ttu-id="ea765-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ea765-189">In Global Catalog</span></span>      | <span data-ttu-id="ea765-190">對</span><span class="sxs-lookup"><span data-stu-id="ea765-190">True</span></span>                                                 |
| <span data-ttu-id="ea765-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ea765-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea765-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ea765-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ea765-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea765-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea765-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-195">Search-Flags</span></span>           | <span data-ttu-id="ea765-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea765-196">0x00000000</span></span>                                           |
| <span data-ttu-id="ea765-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-197">System-Flags</span></span>           | <span data-ttu-id="ea765-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea765-198">0x00000010</span></span>                                           |
| <span data-ttu-id="ea765-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ea765-199">Classes used in</span></span>        | [<span data-ttu-id="ea765-200">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ea765-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ea765-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea765-201">Windows Server 2008</span></span>



| <span data-ttu-id="ea765-202">進入</span><span class="sxs-lookup"><span data-stu-id="ea765-202">Entry</span></span> | <span data-ttu-id="ea765-203">值</span><span class="sxs-lookup"><span data-stu-id="ea765-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ea765-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ea765-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea765-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea765-206">System-Only</span></span>            | <span data-ttu-id="ea765-207">否</span><span class="sxs-lookup"><span data-stu-id="ea765-207">False</span></span>                                                |
| <span data-ttu-id="ea765-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ea765-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ea765-209">對</span><span class="sxs-lookup"><span data-stu-id="ea765-209">True</span></span>                                                 |
| <span data-ttu-id="ea765-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ea765-210">Is Indexed</span></span>             | <span data-ttu-id="ea765-211">否</span><span class="sxs-lookup"><span data-stu-id="ea765-211">False</span></span>                                                |
| <span data-ttu-id="ea765-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ea765-212">In Global Catalog</span></span>      | <span data-ttu-id="ea765-213">對</span><span class="sxs-lookup"><span data-stu-id="ea765-213">True</span></span>                                                 |
| <span data-ttu-id="ea765-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ea765-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea765-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ea765-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ea765-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea765-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea765-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-218">Search-Flags</span></span>           | <span data-ttu-id="ea765-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea765-219">0x00000000</span></span>                                           |
| <span data-ttu-id="ea765-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-220">System-Flags</span></span>           | <span data-ttu-id="ea765-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea765-221">0x00000010</span></span>                                           |
| <span data-ttu-id="ea765-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ea765-222">Classes used in</span></span>        | [<span data-ttu-id="ea765-223">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ea765-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ea765-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ea765-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ea765-225">進入</span><span class="sxs-lookup"><span data-stu-id="ea765-225">Entry</span></span> | <span data-ttu-id="ea765-226">值</span><span class="sxs-lookup"><span data-stu-id="ea765-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ea765-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ea765-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea765-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea765-229">System-Only</span></span>            | <span data-ttu-id="ea765-230">否</span><span class="sxs-lookup"><span data-stu-id="ea765-230">False</span></span>                                                |
| <span data-ttu-id="ea765-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ea765-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ea765-232">對</span><span class="sxs-lookup"><span data-stu-id="ea765-232">True</span></span>                                                 |
| <span data-ttu-id="ea765-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ea765-233">Is Indexed</span></span>             | <span data-ttu-id="ea765-234">否</span><span class="sxs-lookup"><span data-stu-id="ea765-234">False</span></span>                                                |
| <span data-ttu-id="ea765-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ea765-235">In Global Catalog</span></span>      | <span data-ttu-id="ea765-236">對</span><span class="sxs-lookup"><span data-stu-id="ea765-236">True</span></span>                                                 |
| <span data-ttu-id="ea765-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ea765-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea765-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ea765-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ea765-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea765-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea765-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-241">Search-Flags</span></span>           | <span data-ttu-id="ea765-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea765-242">0x00000000</span></span>                                           |
| <span data-ttu-id="ea765-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-243">System-Flags</span></span>           | <span data-ttu-id="ea765-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea765-244">0x00000010</span></span>                                           |
| <span data-ttu-id="ea765-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ea765-245">Classes used in</span></span>        | [<span data-ttu-id="ea765-246">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ea765-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ea765-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea765-247">Windows Server 2012</span></span>



| <span data-ttu-id="ea765-248">進入</span><span class="sxs-lookup"><span data-stu-id="ea765-248">Entry</span></span> | <span data-ttu-id="ea765-249">值</span><span class="sxs-lookup"><span data-stu-id="ea765-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ea765-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ea765-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea765-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ea765-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea765-252">System-Only</span></span>            | <span data-ttu-id="ea765-253">否</span><span class="sxs-lookup"><span data-stu-id="ea765-253">False</span></span>                                                |
| <span data-ttu-id="ea765-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ea765-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ea765-255">對</span><span class="sxs-lookup"><span data-stu-id="ea765-255">True</span></span>                                                 |
| <span data-ttu-id="ea765-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ea765-256">Is Indexed</span></span>             | <span data-ttu-id="ea765-257">否</span><span class="sxs-lookup"><span data-stu-id="ea765-257">False</span></span>                                                |
| <span data-ttu-id="ea765-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ea765-258">In Global Catalog</span></span>      | <span data-ttu-id="ea765-259">對</span><span class="sxs-lookup"><span data-stu-id="ea765-259">True</span></span>                                                 |
| <span data-ttu-id="ea765-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ea765-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea765-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ea765-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ea765-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea765-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea765-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ea765-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-264">Search-Flags</span></span>           | <span data-ttu-id="ea765-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea765-265">0x00000000</span></span>                                           |
| <span data-ttu-id="ea765-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea765-266">System-Flags</span></span>           | <span data-ttu-id="ea765-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea765-267">0x00000010</span></span>                                           |
| <span data-ttu-id="ea765-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ea765-268">Classes used in</span></span>        | [<span data-ttu-id="ea765-269">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="ea765-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





