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
# <a name="machine-wide-policy-attribute"></a><span data-ttu-id="aa5f0-105">全電腦原則屬性</span><span class="sxs-lookup"><span data-stu-id="aa5f0-105">Machine-Wide-Policy attribute</span></span>

<span data-ttu-id="aa5f0-106">用來將使用者可延伸的原則複寫至用戶端。</span><span class="sxs-lookup"><span data-stu-id="aa5f0-106">Used to replicate the user-extensible policy to the clients.</span></span>



| <span data-ttu-id="aa5f0-107">進入</span><span class="sxs-lookup"><span data-stu-id="aa5f0-107">Entry</span></span> | <span data-ttu-id="aa5f0-108">值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="aa5f0-109">CN</span><span class="sxs-lookup"><span data-stu-id="aa5f0-109">CN</span></span>                | <span data-ttu-id="aa5f0-110">全電腦原則</span><span class="sxs-lookup"><span data-stu-id="aa5f0-110">Machine-Wide-Policy</span></span>                                   |
| <span data-ttu-id="aa5f0-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="aa5f0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aa5f0-112">machineWidePolicy</span><span class="sxs-lookup"><span data-stu-id="aa5f0-112">machineWidePolicy</span></span>                                     |
| <span data-ttu-id="aa5f0-113">大小</span><span class="sxs-lookup"><span data-stu-id="aa5f0-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="aa5f0-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="aa5f0-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="aa5f0-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="aa5f0-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="aa5f0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aa5f0-116">Attribute-Id</span></span>      | <span data-ttu-id="aa5f0-117">1.2.840.113556.1.4.459</span><span class="sxs-lookup"><span data-stu-id="aa5f0-117">1.2.840.113556.1.4.459</span></span>                                |
| <span data-ttu-id="aa5f0-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="aa5f0-118">System-Id-Guid</span></span>    | <span data-ttu-id="aa5f0-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="aa5f0-119">80a67e4f-9f22-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="aa5f0-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5f0-120">Syntax</span></span>            | [<span data-ttu-id="aa5f0-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="aa5f0-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="aa5f0-122">實作</span><span class="sxs-lookup"><span data-stu-id="aa5f0-122">Implementations</span></span>

-   [<span data-ttu-id="aa5f0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aa5f0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aa5f0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aa5f0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aa5f0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aa5f0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aa5f0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aa5f0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aa5f0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aa5f0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aa5f0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aa5f0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aa5f0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa5f0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="aa5f0-130">進入</span><span class="sxs-lookup"><span data-stu-id="aa5f0-130">Entry</span></span> | <span data-ttu-id="aa5f0-131">值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="aa5f0-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="aa5f0-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa5f0-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa5f0-134">System-Only</span></span>            | <span data-ttu-id="aa5f0-135">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-135">False</span></span>        |
| <span data-ttu-id="aa5f0-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="aa5f0-137">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-137">False</span></span>        |
| <span data-ttu-id="aa5f0-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="aa5f0-138">Is Indexed</span></span>             | <span data-ttu-id="aa5f0-139">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-139">False</span></span>        |
| <span data-ttu-id="aa5f0-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="aa5f0-140">In Global Catalog</span></span>      | <span data-ttu-id="aa5f0-141">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-141">False</span></span>        |
| <span data-ttu-id="aa5f0-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="aa5f0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa5f0-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="aa5f0-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="aa5f0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa5f0-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="aa5f0-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa5f0-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="aa5f0-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-146">Search-Flags</span></span>           | <span data-ttu-id="aa5f0-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa5f0-147">0x00000000</span></span>   |
| <span data-ttu-id="aa5f0-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-148">System-Flags</span></span>           | <span data-ttu-id="aa5f0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa5f0-149">0x00000010</span></span>   |
| <span data-ttu-id="aa5f0-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="aa5f0-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="aa5f0-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa5f0-151">Windows Server 2003</span></span>



| <span data-ttu-id="aa5f0-152">進入</span><span class="sxs-lookup"><span data-stu-id="aa5f0-152">Entry</span></span> | <span data-ttu-id="aa5f0-153">值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="aa5f0-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="aa5f0-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa5f0-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa5f0-156">System-Only</span></span>            | <span data-ttu-id="aa5f0-157">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-157">False</span></span>        |
| <span data-ttu-id="aa5f0-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-158">Is-Single-Valued</span></span>       | <span data-ttu-id="aa5f0-159">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-159">False</span></span>        |
| <span data-ttu-id="aa5f0-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="aa5f0-160">Is Indexed</span></span>             | <span data-ttu-id="aa5f0-161">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-161">False</span></span>        |
| <span data-ttu-id="aa5f0-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="aa5f0-162">In Global Catalog</span></span>      | <span data-ttu-id="aa5f0-163">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-163">False</span></span>        |
| <span data-ttu-id="aa5f0-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="aa5f0-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa5f0-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="aa5f0-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="aa5f0-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa5f0-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="aa5f0-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa5f0-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="aa5f0-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-168">Search-Flags</span></span>           | <span data-ttu-id="aa5f0-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa5f0-169">0x00000000</span></span>   |
| <span data-ttu-id="aa5f0-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-170">System-Flags</span></span>           | <span data-ttu-id="aa5f0-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa5f0-171">0x00000010</span></span>   |
| <span data-ttu-id="aa5f0-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="aa5f0-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aa5f0-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aa5f0-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aa5f0-174">進入</span><span class="sxs-lookup"><span data-stu-id="aa5f0-174">Entry</span></span> | <span data-ttu-id="aa5f0-175">值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="aa5f0-176">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="aa5f0-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa5f0-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa5f0-178">System-Only</span></span>            | <span data-ttu-id="aa5f0-179">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-179">False</span></span>        |
| <span data-ttu-id="aa5f0-180">是-單一值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-180">Is-Single-Valued</span></span>       | <span data-ttu-id="aa5f0-181">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-181">False</span></span>        |
| <span data-ttu-id="aa5f0-182">已編制索引</span><span class="sxs-lookup"><span data-stu-id="aa5f0-182">Is Indexed</span></span>             | <span data-ttu-id="aa5f0-183">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-183">False</span></span>        |
| <span data-ttu-id="aa5f0-184">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="aa5f0-184">In Global Catalog</span></span>      | <span data-ttu-id="aa5f0-185">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-185">False</span></span>        |
| <span data-ttu-id="aa5f0-186">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="aa5f0-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa5f0-187">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="aa5f0-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="aa5f0-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa5f0-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="aa5f0-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa5f0-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="aa5f0-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-190">Search-Flags</span></span>           | <span data-ttu-id="aa5f0-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa5f0-191">0x00000000</span></span>   |
| <span data-ttu-id="aa5f0-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-192">System-Flags</span></span>           | <span data-ttu-id="aa5f0-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa5f0-193">0x00000010</span></span>   |
| <span data-ttu-id="aa5f0-194">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="aa5f0-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="aa5f0-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa5f0-195">Windows Server 2008</span></span>



| <span data-ttu-id="aa5f0-196">進入</span><span class="sxs-lookup"><span data-stu-id="aa5f0-196">Entry</span></span> | <span data-ttu-id="aa5f0-197">值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="aa5f0-198">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="aa5f0-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa5f0-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa5f0-200">System-Only</span></span>            | <span data-ttu-id="aa5f0-201">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-201">False</span></span>        |
| <span data-ttu-id="aa5f0-202">是-單一值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-202">Is-Single-Valued</span></span>       | <span data-ttu-id="aa5f0-203">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-203">False</span></span>        |
| <span data-ttu-id="aa5f0-204">已編制索引</span><span class="sxs-lookup"><span data-stu-id="aa5f0-204">Is Indexed</span></span>             | <span data-ttu-id="aa5f0-205">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-205">False</span></span>        |
| <span data-ttu-id="aa5f0-206">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="aa5f0-206">In Global Catalog</span></span>      | <span data-ttu-id="aa5f0-207">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-207">False</span></span>        |
| <span data-ttu-id="aa5f0-208">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="aa5f0-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa5f0-209">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="aa5f0-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="aa5f0-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa5f0-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="aa5f0-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa5f0-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="aa5f0-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-212">Search-Flags</span></span>           | <span data-ttu-id="aa5f0-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa5f0-213">0x00000000</span></span>   |
| <span data-ttu-id="aa5f0-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-214">System-Flags</span></span>           | <span data-ttu-id="aa5f0-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa5f0-215">0x00000010</span></span>   |
| <span data-ttu-id="aa5f0-216">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="aa5f0-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aa5f0-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa5f0-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aa5f0-218">進入</span><span class="sxs-lookup"><span data-stu-id="aa5f0-218">Entry</span></span> | <span data-ttu-id="aa5f0-219">值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="aa5f0-220">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="aa5f0-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa5f0-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa5f0-222">System-Only</span></span>            | <span data-ttu-id="aa5f0-223">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-223">False</span></span>        |
| <span data-ttu-id="aa5f0-224">是-單一值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-224">Is-Single-Valued</span></span>       | <span data-ttu-id="aa5f0-225">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-225">False</span></span>        |
| <span data-ttu-id="aa5f0-226">已編制索引</span><span class="sxs-lookup"><span data-stu-id="aa5f0-226">Is Indexed</span></span>             | <span data-ttu-id="aa5f0-227">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-227">False</span></span>        |
| <span data-ttu-id="aa5f0-228">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="aa5f0-228">In Global Catalog</span></span>      | <span data-ttu-id="aa5f0-229">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-229">False</span></span>        |
| <span data-ttu-id="aa5f0-230">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="aa5f0-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa5f0-231">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="aa5f0-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="aa5f0-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa5f0-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="aa5f0-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa5f0-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="aa5f0-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-234">Search-Flags</span></span>           | <span data-ttu-id="aa5f0-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa5f0-235">0x00000000</span></span>   |
| <span data-ttu-id="aa5f0-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-236">System-Flags</span></span>           | <span data-ttu-id="aa5f0-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa5f0-237">0x00000010</span></span>   |
| <span data-ttu-id="aa5f0-238">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="aa5f0-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="aa5f0-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa5f0-239">Windows Server 2012</span></span>



| <span data-ttu-id="aa5f0-240">進入</span><span class="sxs-lookup"><span data-stu-id="aa5f0-240">Entry</span></span> | <span data-ttu-id="aa5f0-241">值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="aa5f0-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="aa5f0-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa5f0-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="aa5f0-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa5f0-244">System-Only</span></span>            | <span data-ttu-id="aa5f0-245">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-245">False</span></span>        |
| <span data-ttu-id="aa5f0-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="aa5f0-246">Is-Single-Valued</span></span>       | <span data-ttu-id="aa5f0-247">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-247">False</span></span>        |
| <span data-ttu-id="aa5f0-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="aa5f0-248">Is Indexed</span></span>             | <span data-ttu-id="aa5f0-249">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-249">False</span></span>        |
| <span data-ttu-id="aa5f0-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="aa5f0-250">In Global Catalog</span></span>      | <span data-ttu-id="aa5f0-251">否</span><span class="sxs-lookup"><span data-stu-id="aa5f0-251">False</span></span>        |
| <span data-ttu-id="aa5f0-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="aa5f0-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa5f0-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="aa5f0-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="aa5f0-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa5f0-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="aa5f0-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa5f0-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="aa5f0-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-256">Search-Flags</span></span>           | <span data-ttu-id="aa5f0-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa5f0-257">0x00000000</span></span>   |
| <span data-ttu-id="aa5f0-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa5f0-258">System-Flags</span></span>           | <span data-ttu-id="aa5f0-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa5f0-259">0x00000010</span></span>   |
| <span data-ttu-id="aa5f0-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="aa5f0-260">Classes used in</span></span>        | \-           |



 

 




