---
title: 全電腦原則屬性
description: 用來將使用者可延伸的原則複寫至用戶端。
ms.assetid: e8ce40b8-7658-4e4b-b0e1-b68031811dd1
ms.tgt_platform: multiple
keywords:
- 全電腦原則屬性 AD 架構
- machineWidePolicy 屬性 AD 架構
topic_type:
- apiref
api_name:
- Machine-Wide-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd3af77dfb501000369b3c4ae23b3f5f64f0da9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935282"
---
# <a name="machine-wide-policy-attribute"></a><span data-ttu-id="152ff-105">全電腦原則屬性</span><span class="sxs-lookup"><span data-stu-id="152ff-105">Machine-Wide-Policy attribute</span></span>

<span data-ttu-id="152ff-106">用來將使用者可延伸的原則複寫至用戶端。</span><span class="sxs-lookup"><span data-stu-id="152ff-106">Used to replicate the user-extensible policy to the clients.</span></span>



| <span data-ttu-id="152ff-107">進入</span><span class="sxs-lookup"><span data-stu-id="152ff-107">Entry</span></span> | <span data-ttu-id="152ff-108">值</span><span class="sxs-lookup"><span data-stu-id="152ff-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="152ff-109">CN</span><span class="sxs-lookup"><span data-stu-id="152ff-109">CN</span></span>                | <span data-ttu-id="152ff-110">全電腦原則</span><span class="sxs-lookup"><span data-stu-id="152ff-110">Machine-Wide-Policy</span></span>                                   |
| <span data-ttu-id="152ff-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="152ff-111">Ldap-Display-Name</span></span> | <span data-ttu-id="152ff-112">machineWidePolicy</span><span class="sxs-lookup"><span data-stu-id="152ff-112">machineWidePolicy</span></span>                                     |
| <span data-ttu-id="152ff-113">大小</span><span class="sxs-lookup"><span data-stu-id="152ff-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="152ff-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="152ff-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="152ff-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="152ff-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="152ff-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="152ff-116">Attribute-Id</span></span>      | <span data-ttu-id="152ff-117">1.2.840.113556.1.4.459</span><span class="sxs-lookup"><span data-stu-id="152ff-117">1.2.840.113556.1.4.459</span></span>                                |
| <span data-ttu-id="152ff-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="152ff-118">System-Id-Guid</span></span>    | <span data-ttu-id="152ff-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="152ff-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="152ff-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="152ff-120">Syntax</span></span>            | [<span data-ttu-id="152ff-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="152ff-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="152ff-122">實作</span><span class="sxs-lookup"><span data-stu-id="152ff-122">Implementations</span></span>

-   [<span data-ttu-id="152ff-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="152ff-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="152ff-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="152ff-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="152ff-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="152ff-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="152ff-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="152ff-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="152ff-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="152ff-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="152ff-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="152ff-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="152ff-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="152ff-129">Windows 2000 Server</span></span>



| <span data-ttu-id="152ff-130">進入</span><span class="sxs-lookup"><span data-stu-id="152ff-130">Entry</span></span> | <span data-ttu-id="152ff-131">值</span><span class="sxs-lookup"><span data-stu-id="152ff-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="152ff-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="152ff-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152ff-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="152ff-134">System-Only</span></span>            | <span data-ttu-id="152ff-135">否</span><span class="sxs-lookup"><span data-stu-id="152ff-135">False</span></span>        |
| <span data-ttu-id="152ff-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="152ff-136">Is-Single-Valued</span></span>       | <span data-ttu-id="152ff-137">否</span><span class="sxs-lookup"><span data-stu-id="152ff-137">False</span></span>        |
| <span data-ttu-id="152ff-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="152ff-138">Is Indexed</span></span>             | <span data-ttu-id="152ff-139">否</span><span class="sxs-lookup"><span data-stu-id="152ff-139">False</span></span>        |
| <span data-ttu-id="152ff-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="152ff-140">In Global Catalog</span></span>      | <span data-ttu-id="152ff-141">否</span><span class="sxs-lookup"><span data-stu-id="152ff-141">False</span></span>        |
| <span data-ttu-id="152ff-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="152ff-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="152ff-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="152ff-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="152ff-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152ff-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="152ff-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152ff-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="152ff-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-146">Search-Flags</span></span>           | <span data-ttu-id="152ff-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152ff-147">0x00000000</span></span>   |
| <span data-ttu-id="152ff-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-148">System-Flags</span></span>           | <span data-ttu-id="152ff-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="152ff-149">0x00000010</span></span>   |
| <span data-ttu-id="152ff-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="152ff-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="152ff-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="152ff-151">Windows Server 2003</span></span>



| <span data-ttu-id="152ff-152">進入</span><span class="sxs-lookup"><span data-stu-id="152ff-152">Entry</span></span> | <span data-ttu-id="152ff-153">值</span><span class="sxs-lookup"><span data-stu-id="152ff-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="152ff-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="152ff-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152ff-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="152ff-156">System-Only</span></span>            | <span data-ttu-id="152ff-157">否</span><span class="sxs-lookup"><span data-stu-id="152ff-157">False</span></span>        |
| <span data-ttu-id="152ff-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="152ff-158">Is-Single-Valued</span></span>       | <span data-ttu-id="152ff-159">否</span><span class="sxs-lookup"><span data-stu-id="152ff-159">False</span></span>        |
| <span data-ttu-id="152ff-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="152ff-160">Is Indexed</span></span>             | <span data-ttu-id="152ff-161">否</span><span class="sxs-lookup"><span data-stu-id="152ff-161">False</span></span>        |
| <span data-ttu-id="152ff-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="152ff-162">In Global Catalog</span></span>      | <span data-ttu-id="152ff-163">否</span><span class="sxs-lookup"><span data-stu-id="152ff-163">False</span></span>        |
| <span data-ttu-id="152ff-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="152ff-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="152ff-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="152ff-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="152ff-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152ff-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="152ff-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152ff-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="152ff-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-168">Search-Flags</span></span>           | <span data-ttu-id="152ff-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152ff-169">0x00000000</span></span>   |
| <span data-ttu-id="152ff-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-170">System-Flags</span></span>           | <span data-ttu-id="152ff-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="152ff-171">0x00000010</span></span>   |
| <span data-ttu-id="152ff-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="152ff-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="152ff-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="152ff-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="152ff-174">進入</span><span class="sxs-lookup"><span data-stu-id="152ff-174">Entry</span></span> | <span data-ttu-id="152ff-175">值</span><span class="sxs-lookup"><span data-stu-id="152ff-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="152ff-176">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="152ff-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152ff-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="152ff-178">System-Only</span></span>            | <span data-ttu-id="152ff-179">否</span><span class="sxs-lookup"><span data-stu-id="152ff-179">False</span></span>        |
| <span data-ttu-id="152ff-180">是-單一值</span><span class="sxs-lookup"><span data-stu-id="152ff-180">Is-Single-Valued</span></span>       | <span data-ttu-id="152ff-181">否</span><span class="sxs-lookup"><span data-stu-id="152ff-181">False</span></span>        |
| <span data-ttu-id="152ff-182">已編制索引</span><span class="sxs-lookup"><span data-stu-id="152ff-182">Is Indexed</span></span>             | <span data-ttu-id="152ff-183">否</span><span class="sxs-lookup"><span data-stu-id="152ff-183">False</span></span>        |
| <span data-ttu-id="152ff-184">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="152ff-184">In Global Catalog</span></span>      | <span data-ttu-id="152ff-185">否</span><span class="sxs-lookup"><span data-stu-id="152ff-185">False</span></span>        |
| <span data-ttu-id="152ff-186">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="152ff-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="152ff-187">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="152ff-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="152ff-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152ff-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="152ff-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152ff-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="152ff-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-190">Search-Flags</span></span>           | <span data-ttu-id="152ff-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152ff-191">0x00000000</span></span>   |
| <span data-ttu-id="152ff-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-192">System-Flags</span></span>           | <span data-ttu-id="152ff-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="152ff-193">0x00000010</span></span>   |
| <span data-ttu-id="152ff-194">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="152ff-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="152ff-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="152ff-195">Windows Server 2008</span></span>



| <span data-ttu-id="152ff-196">進入</span><span class="sxs-lookup"><span data-stu-id="152ff-196">Entry</span></span> | <span data-ttu-id="152ff-197">值</span><span class="sxs-lookup"><span data-stu-id="152ff-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="152ff-198">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="152ff-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152ff-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="152ff-200">System-Only</span></span>            | <span data-ttu-id="152ff-201">否</span><span class="sxs-lookup"><span data-stu-id="152ff-201">False</span></span>        |
| <span data-ttu-id="152ff-202">是-單一值</span><span class="sxs-lookup"><span data-stu-id="152ff-202">Is-Single-Valued</span></span>       | <span data-ttu-id="152ff-203">否</span><span class="sxs-lookup"><span data-stu-id="152ff-203">False</span></span>        |
| <span data-ttu-id="152ff-204">已編制索引</span><span class="sxs-lookup"><span data-stu-id="152ff-204">Is Indexed</span></span>             | <span data-ttu-id="152ff-205">否</span><span class="sxs-lookup"><span data-stu-id="152ff-205">False</span></span>        |
| <span data-ttu-id="152ff-206">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="152ff-206">In Global Catalog</span></span>      | <span data-ttu-id="152ff-207">否</span><span class="sxs-lookup"><span data-stu-id="152ff-207">False</span></span>        |
| <span data-ttu-id="152ff-208">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="152ff-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="152ff-209">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="152ff-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="152ff-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152ff-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="152ff-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152ff-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="152ff-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-212">Search-Flags</span></span>           | <span data-ttu-id="152ff-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152ff-213">0x00000000</span></span>   |
| <span data-ttu-id="152ff-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-214">System-Flags</span></span>           | <span data-ttu-id="152ff-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="152ff-215">0x00000010</span></span>   |
| <span data-ttu-id="152ff-216">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="152ff-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="152ff-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="152ff-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="152ff-218">進入</span><span class="sxs-lookup"><span data-stu-id="152ff-218">Entry</span></span> | <span data-ttu-id="152ff-219">值</span><span class="sxs-lookup"><span data-stu-id="152ff-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="152ff-220">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="152ff-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152ff-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="152ff-222">System-Only</span></span>            | <span data-ttu-id="152ff-223">否</span><span class="sxs-lookup"><span data-stu-id="152ff-223">False</span></span>        |
| <span data-ttu-id="152ff-224">是-單一值</span><span class="sxs-lookup"><span data-stu-id="152ff-224">Is-Single-Valued</span></span>       | <span data-ttu-id="152ff-225">否</span><span class="sxs-lookup"><span data-stu-id="152ff-225">False</span></span>        |
| <span data-ttu-id="152ff-226">已編制索引</span><span class="sxs-lookup"><span data-stu-id="152ff-226">Is Indexed</span></span>             | <span data-ttu-id="152ff-227">否</span><span class="sxs-lookup"><span data-stu-id="152ff-227">False</span></span>        |
| <span data-ttu-id="152ff-228">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="152ff-228">In Global Catalog</span></span>      | <span data-ttu-id="152ff-229">否</span><span class="sxs-lookup"><span data-stu-id="152ff-229">False</span></span>        |
| <span data-ttu-id="152ff-230">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="152ff-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="152ff-231">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="152ff-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="152ff-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152ff-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="152ff-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152ff-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="152ff-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-234">Search-Flags</span></span>           | <span data-ttu-id="152ff-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152ff-235">0x00000000</span></span>   |
| <span data-ttu-id="152ff-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-236">System-Flags</span></span>           | <span data-ttu-id="152ff-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="152ff-237">0x00000010</span></span>   |
| <span data-ttu-id="152ff-238">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="152ff-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="152ff-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="152ff-239">Windows Server 2012</span></span>



| <span data-ttu-id="152ff-240">進入</span><span class="sxs-lookup"><span data-stu-id="152ff-240">Entry</span></span> | <span data-ttu-id="152ff-241">值</span><span class="sxs-lookup"><span data-stu-id="152ff-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="152ff-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="152ff-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152ff-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="152ff-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="152ff-244">System-Only</span></span>            | <span data-ttu-id="152ff-245">否</span><span class="sxs-lookup"><span data-stu-id="152ff-245">False</span></span>        |
| <span data-ttu-id="152ff-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="152ff-246">Is-Single-Valued</span></span>       | <span data-ttu-id="152ff-247">否</span><span class="sxs-lookup"><span data-stu-id="152ff-247">False</span></span>        |
| <span data-ttu-id="152ff-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="152ff-248">Is Indexed</span></span>             | <span data-ttu-id="152ff-249">否</span><span class="sxs-lookup"><span data-stu-id="152ff-249">False</span></span>        |
| <span data-ttu-id="152ff-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="152ff-250">In Global Catalog</span></span>      | <span data-ttu-id="152ff-251">否</span><span class="sxs-lookup"><span data-stu-id="152ff-251">False</span></span>        |
| <span data-ttu-id="152ff-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="152ff-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="152ff-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="152ff-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="152ff-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152ff-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="152ff-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152ff-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="152ff-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-256">Search-Flags</span></span>           | <span data-ttu-id="152ff-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152ff-257">0x00000000</span></span>   |
| <span data-ttu-id="152ff-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152ff-258">System-Flags</span></span>           | <span data-ttu-id="152ff-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="152ff-259">0x00000010</span></span>   |
| <span data-ttu-id="152ff-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="152ff-260">Classes used in</span></span>        | \-           |



 

 




