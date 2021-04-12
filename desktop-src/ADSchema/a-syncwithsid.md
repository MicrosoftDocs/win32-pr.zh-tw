---
title: Sync-With-SID 屬性
description: 針對 SAM 內建群組物件/本機原則同步處理，這是物件所對應的本機群組。
ms.assetid: b983210d-1c54-4355-bc37-771e51016175
ms.tgt_platform: multiple
keywords:
- Sync-With-SID 屬性 AD 架構
- syncWithSID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Sync-With-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845a95b737a56a853fa7fb4e77d5612f1efc3c37
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107937"
---
# <a name="sync-with-sid-attribute"></a><span data-ttu-id="1e81b-105">Sync-With-SID 屬性</span><span class="sxs-lookup"><span data-stu-id="1e81b-105">Sync-With-SID attribute</span></span>

<span data-ttu-id="1e81b-106">針對 SAM 內建群組物件/本機原則同步處理，這是物件所對應的本機群組。</span><span class="sxs-lookup"><span data-stu-id="1e81b-106">For the SAM builtin group object/ local policy synchronization, this is the local group to which an object corresponds.</span></span>



| <span data-ttu-id="1e81b-107">進入</span><span class="sxs-lookup"><span data-stu-id="1e81b-107">Entry</span></span> | <span data-ttu-id="1e81b-108">值</span><span class="sxs-lookup"><span data-stu-id="1e81b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1e81b-109">CN</span><span class="sxs-lookup"><span data-stu-id="1e81b-109">CN</span></span>                | <span data-ttu-id="1e81b-110">同步-使用-SID</span><span class="sxs-lookup"><span data-stu-id="1e81b-110">Sync-With-SID</span></span>                        |
| <span data-ttu-id="1e81b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1e81b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1e81b-112">syncWithSID</span><span class="sxs-lookup"><span data-stu-id="1e81b-112">syncWithSID</span></span>                          |
| <span data-ttu-id="1e81b-113">大小</span><span class="sxs-lookup"><span data-stu-id="1e81b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="1e81b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1e81b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1e81b-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1e81b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1e81b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1e81b-116">Attribute-Id</span></span>      | <span data-ttu-id="1e81b-117">1.2.840.113556.1.4.667</span><span class="sxs-lookup"><span data-stu-id="1e81b-117">1.2.840.113556.1.4.667</span></span>               |
| <span data-ttu-id="1e81b-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1e81b-118">System-Id-Guid</span></span>    | <span data-ttu-id="1e81b-119">037651e5-441d-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1e81b-119">037651e5-441d-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="1e81b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e81b-120">Syntax</span></span>            | [<span data-ttu-id="1e81b-121">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="1e81b-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="1e81b-122">實作</span><span class="sxs-lookup"><span data-stu-id="1e81b-122">Implementations</span></span>

-   [<span data-ttu-id="1e81b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1e81b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1e81b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1e81b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1e81b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1e81b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1e81b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1e81b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1e81b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1e81b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1e81b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1e81b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1e81b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e81b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1e81b-130">進入</span><span class="sxs-lookup"><span data-stu-id="1e81b-130">Entry</span></span> | <span data-ttu-id="1e81b-131">值</span><span class="sxs-lookup"><span data-stu-id="1e81b-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="1e81b-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e81b-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e81b-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e81b-134">System-Only</span></span>            | <span data-ttu-id="1e81b-135">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-135">False</span></span>        |
| <span data-ttu-id="1e81b-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e81b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1e81b-137">對</span><span class="sxs-lookup"><span data-stu-id="1e81b-137">True</span></span>         |
| <span data-ttu-id="1e81b-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e81b-138">Is Indexed</span></span>             | <span data-ttu-id="1e81b-139">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-139">False</span></span>        |
| <span data-ttu-id="1e81b-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e81b-140">In Global Catalog</span></span>      | <span data-ttu-id="1e81b-141">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-141">False</span></span>        |
| <span data-ttu-id="1e81b-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e81b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e81b-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e81b-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="1e81b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e81b-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="1e81b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e81b-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="1e81b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-146">Search-Flags</span></span>           | <span data-ttu-id="1e81b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e81b-147">0x00000000</span></span>   |
| <span data-ttu-id="1e81b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-148">System-Flags</span></span>           | <span data-ttu-id="1e81b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e81b-149">0x00000010</span></span>   |
| <span data-ttu-id="1e81b-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e81b-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="1e81b-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e81b-151">Windows Server 2003</span></span>



| <span data-ttu-id="1e81b-152">進入</span><span class="sxs-lookup"><span data-stu-id="1e81b-152">Entry</span></span> | <span data-ttu-id="1e81b-153">值</span><span class="sxs-lookup"><span data-stu-id="1e81b-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="1e81b-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e81b-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e81b-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e81b-156">System-Only</span></span>            | <span data-ttu-id="1e81b-157">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-157">False</span></span>        |
| <span data-ttu-id="1e81b-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e81b-158">Is-Single-Valued</span></span>       | <span data-ttu-id="1e81b-159">對</span><span class="sxs-lookup"><span data-stu-id="1e81b-159">True</span></span>         |
| <span data-ttu-id="1e81b-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e81b-160">Is Indexed</span></span>             | <span data-ttu-id="1e81b-161">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-161">False</span></span>        |
| <span data-ttu-id="1e81b-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e81b-162">In Global Catalog</span></span>      | <span data-ttu-id="1e81b-163">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-163">False</span></span>        |
| <span data-ttu-id="1e81b-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e81b-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e81b-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e81b-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="1e81b-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e81b-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="1e81b-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e81b-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="1e81b-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-168">Search-Flags</span></span>           | <span data-ttu-id="1e81b-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e81b-169">0x00000000</span></span>   |
| <span data-ttu-id="1e81b-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-170">System-Flags</span></span>           | <span data-ttu-id="1e81b-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e81b-171">0x00000010</span></span>   |
| <span data-ttu-id="1e81b-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e81b-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1e81b-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e81b-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1e81b-174">進入</span><span class="sxs-lookup"><span data-stu-id="1e81b-174">Entry</span></span> | <span data-ttu-id="1e81b-175">值</span><span class="sxs-lookup"><span data-stu-id="1e81b-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="1e81b-176">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e81b-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e81b-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e81b-178">System-Only</span></span>            | <span data-ttu-id="1e81b-179">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-179">False</span></span>        |
| <span data-ttu-id="1e81b-180">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e81b-180">Is-Single-Valued</span></span>       | <span data-ttu-id="1e81b-181">對</span><span class="sxs-lookup"><span data-stu-id="1e81b-181">True</span></span>         |
| <span data-ttu-id="1e81b-182">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e81b-182">Is Indexed</span></span>             | <span data-ttu-id="1e81b-183">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-183">False</span></span>        |
| <span data-ttu-id="1e81b-184">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e81b-184">In Global Catalog</span></span>      | <span data-ttu-id="1e81b-185">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-185">False</span></span>        |
| <span data-ttu-id="1e81b-186">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e81b-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e81b-187">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e81b-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="1e81b-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e81b-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="1e81b-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e81b-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="1e81b-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-190">Search-Flags</span></span>           | <span data-ttu-id="1e81b-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e81b-191">0x00000000</span></span>   |
| <span data-ttu-id="1e81b-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-192">System-Flags</span></span>           | <span data-ttu-id="1e81b-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e81b-193">0x00000010</span></span>   |
| <span data-ttu-id="1e81b-194">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e81b-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="1e81b-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e81b-195">Windows Server 2008</span></span>



| <span data-ttu-id="1e81b-196">進入</span><span class="sxs-lookup"><span data-stu-id="1e81b-196">Entry</span></span> | <span data-ttu-id="1e81b-197">值</span><span class="sxs-lookup"><span data-stu-id="1e81b-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="1e81b-198">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e81b-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e81b-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e81b-200">System-Only</span></span>            | <span data-ttu-id="1e81b-201">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-201">False</span></span>        |
| <span data-ttu-id="1e81b-202">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e81b-202">Is-Single-Valued</span></span>       | <span data-ttu-id="1e81b-203">對</span><span class="sxs-lookup"><span data-stu-id="1e81b-203">True</span></span>         |
| <span data-ttu-id="1e81b-204">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e81b-204">Is Indexed</span></span>             | <span data-ttu-id="1e81b-205">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-205">False</span></span>        |
| <span data-ttu-id="1e81b-206">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e81b-206">In Global Catalog</span></span>      | <span data-ttu-id="1e81b-207">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-207">False</span></span>        |
| <span data-ttu-id="1e81b-208">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e81b-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e81b-209">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e81b-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="1e81b-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e81b-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="1e81b-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e81b-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="1e81b-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-212">Search-Flags</span></span>           | <span data-ttu-id="1e81b-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e81b-213">0x00000000</span></span>   |
| <span data-ttu-id="1e81b-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-214">System-Flags</span></span>           | <span data-ttu-id="1e81b-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e81b-215">0x00000010</span></span>   |
| <span data-ttu-id="1e81b-216">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e81b-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1e81b-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e81b-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1e81b-218">進入</span><span class="sxs-lookup"><span data-stu-id="1e81b-218">Entry</span></span> | <span data-ttu-id="1e81b-219">值</span><span class="sxs-lookup"><span data-stu-id="1e81b-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="1e81b-220">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e81b-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e81b-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e81b-222">System-Only</span></span>            | <span data-ttu-id="1e81b-223">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-223">False</span></span>        |
| <span data-ttu-id="1e81b-224">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e81b-224">Is-Single-Valued</span></span>       | <span data-ttu-id="1e81b-225">對</span><span class="sxs-lookup"><span data-stu-id="1e81b-225">True</span></span>         |
| <span data-ttu-id="1e81b-226">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e81b-226">Is Indexed</span></span>             | <span data-ttu-id="1e81b-227">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-227">False</span></span>        |
| <span data-ttu-id="1e81b-228">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e81b-228">In Global Catalog</span></span>      | <span data-ttu-id="1e81b-229">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-229">False</span></span>        |
| <span data-ttu-id="1e81b-230">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e81b-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e81b-231">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e81b-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="1e81b-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e81b-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="1e81b-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e81b-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="1e81b-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-234">Search-Flags</span></span>           | <span data-ttu-id="1e81b-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e81b-235">0x00000000</span></span>   |
| <span data-ttu-id="1e81b-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-236">System-Flags</span></span>           | <span data-ttu-id="1e81b-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e81b-237">0x00000010</span></span>   |
| <span data-ttu-id="1e81b-238">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e81b-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="1e81b-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e81b-239">Windows Server 2012</span></span>



| <span data-ttu-id="1e81b-240">進入</span><span class="sxs-lookup"><span data-stu-id="1e81b-240">Entry</span></span> | <span data-ttu-id="1e81b-241">值</span><span class="sxs-lookup"><span data-stu-id="1e81b-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="1e81b-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1e81b-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e81b-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="1e81b-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e81b-244">System-Only</span></span>            | <span data-ttu-id="1e81b-245">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-245">False</span></span>        |
| <span data-ttu-id="1e81b-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1e81b-246">Is-Single-Valued</span></span>       | <span data-ttu-id="1e81b-247">對</span><span class="sxs-lookup"><span data-stu-id="1e81b-247">True</span></span>         |
| <span data-ttu-id="1e81b-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1e81b-248">Is Indexed</span></span>             | <span data-ttu-id="1e81b-249">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-249">False</span></span>        |
| <span data-ttu-id="1e81b-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1e81b-250">In Global Catalog</span></span>      | <span data-ttu-id="1e81b-251">否</span><span class="sxs-lookup"><span data-stu-id="1e81b-251">False</span></span>        |
| <span data-ttu-id="1e81b-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1e81b-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e81b-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1e81b-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="1e81b-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e81b-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="1e81b-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e81b-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="1e81b-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-256">Search-Flags</span></span>           | <span data-ttu-id="1e81b-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e81b-257">0x00000000</span></span>   |
| <span data-ttu-id="1e81b-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e81b-258">System-Flags</span></span>           | <span data-ttu-id="1e81b-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e81b-259">0x00000010</span></span>   |
| <span data-ttu-id="1e81b-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1e81b-260">Classes used in</span></span>        | \-           |



 

 




