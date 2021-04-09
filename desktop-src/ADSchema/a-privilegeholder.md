---
title: Privilege-Holder 屬性
description: 授與此許可權之主體的辨別名稱清單。
ms.assetid: d7ae6de8-6725-436f-93e0-1dd966aa7c07
ms.tgt_platform: multiple
keywords:
- Privilege-Holder 屬性 AD 架構
- privilegeHolder 屬性 AD 架構
topic_type:
- apiref
api_name:
- Privilege-Holder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f414e92f092eb6cb60f11807c9c5f3cdb20ef
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687140"
---
# <a name="privilege-holder-attribute"></a><span data-ttu-id="f883e-105">Privilege-Holder 屬性</span><span class="sxs-lookup"><span data-stu-id="f883e-105">Privilege-Holder attribute</span></span>

<span data-ttu-id="f883e-106">授與此許可權之主體的辨別名稱清單。</span><span class="sxs-lookup"><span data-stu-id="f883e-106">List of Distinguished Names of principals granted this privilege.</span></span>



| <span data-ttu-id="f883e-107">進入</span><span class="sxs-lookup"><span data-stu-id="f883e-107">Entry</span></span> | <span data-ttu-id="f883e-108">值</span><span class="sxs-lookup"><span data-stu-id="f883e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f883e-109">CN</span><span class="sxs-lookup"><span data-stu-id="f883e-109">CN</span></span>                | <span data-ttu-id="f883e-110">Privilege-Holder</span><span class="sxs-lookup"><span data-stu-id="f883e-110">Privilege-Holder</span></span>                        |
| <span data-ttu-id="f883e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f883e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f883e-112">privilegeHolder</span><span class="sxs-lookup"><span data-stu-id="f883e-112">privilegeHolder</span></span>                         |
| <span data-ttu-id="f883e-113">大小</span><span class="sxs-lookup"><span data-stu-id="f883e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f883e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f883e-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f883e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f883e-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f883e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f883e-116">Attribute-Id</span></span>      | <span data-ttu-id="f883e-117">1.2.840.113556.1.4.637</span><span class="sxs-lookup"><span data-stu-id="f883e-117">1.2.840.113556.1.4.637</span></span>                  |
| <span data-ttu-id="f883e-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f883e-118">System-Id-Guid</span></span>    | <span data-ttu-id="f883e-119">19405b9b-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f883e-119">19405b9b-3cfa-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="f883e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f883e-120">Syntax</span></span>            | [<span data-ttu-id="f883e-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f883e-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f883e-122">實作</span><span class="sxs-lookup"><span data-stu-id="f883e-122">Implementations</span></span>

-   [<span data-ttu-id="f883e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f883e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f883e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f883e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f883e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f883e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f883e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f883e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f883e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f883e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f883e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f883e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f883e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f883e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f883e-130">進入</span><span class="sxs-lookup"><span data-stu-id="f883e-130">Entry</span></span> | <span data-ttu-id="f883e-131">值</span><span class="sxs-lookup"><span data-stu-id="f883e-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f883e-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f883e-132">Link-Id</span></span>                | <span data-ttu-id="f883e-133">70</span><span class="sxs-lookup"><span data-stu-id="f883e-133">70</span></span>           |
| <span data-ttu-id="f883e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f883e-134">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="f883e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f883e-135">System-Only</span></span>            | <span data-ttu-id="f883e-136">否</span><span class="sxs-lookup"><span data-stu-id="f883e-136">False</span></span>        |
| <span data-ttu-id="f883e-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f883e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f883e-138">否</span><span class="sxs-lookup"><span data-stu-id="f883e-138">False</span></span>        |
| <span data-ttu-id="f883e-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f883e-139">Is Indexed</span></span>             | <span data-ttu-id="f883e-140">否</span><span class="sxs-lookup"><span data-stu-id="f883e-140">False</span></span>        |
| <span data-ttu-id="f883e-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f883e-141">In Global Catalog</span></span>      | <span data-ttu-id="f883e-142">否</span><span class="sxs-lookup"><span data-stu-id="f883e-142">False</span></span>        |
| <span data-ttu-id="f883e-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f883e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f883e-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f883e-144">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="f883e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f883e-145">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="f883e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f883e-146">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="f883e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-147">Search-Flags</span></span>           | <span data-ttu-id="f883e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f883e-148">0x00000000</span></span>   |
| <span data-ttu-id="f883e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-149">System-Flags</span></span>           | <span data-ttu-id="f883e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f883e-150">0x00000010</span></span>   |
| <span data-ttu-id="f883e-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f883e-151">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="f883e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f883e-152">Windows Server 2003</span></span>



| <span data-ttu-id="f883e-153">進入</span><span class="sxs-lookup"><span data-stu-id="f883e-153">Entry</span></span> | <span data-ttu-id="f883e-154">值</span><span class="sxs-lookup"><span data-stu-id="f883e-154">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f883e-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f883e-155">Link-Id</span></span>                | <span data-ttu-id="f883e-156">70</span><span class="sxs-lookup"><span data-stu-id="f883e-156">70</span></span>           |
| <span data-ttu-id="f883e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f883e-157">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="f883e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f883e-158">System-Only</span></span>            | <span data-ttu-id="f883e-159">否</span><span class="sxs-lookup"><span data-stu-id="f883e-159">False</span></span>        |
| <span data-ttu-id="f883e-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f883e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f883e-161">否</span><span class="sxs-lookup"><span data-stu-id="f883e-161">False</span></span>        |
| <span data-ttu-id="f883e-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f883e-162">Is Indexed</span></span>             | <span data-ttu-id="f883e-163">否</span><span class="sxs-lookup"><span data-stu-id="f883e-163">False</span></span>        |
| <span data-ttu-id="f883e-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f883e-164">In Global Catalog</span></span>      | <span data-ttu-id="f883e-165">否</span><span class="sxs-lookup"><span data-stu-id="f883e-165">False</span></span>        |
| <span data-ttu-id="f883e-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f883e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f883e-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f883e-167">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="f883e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f883e-168">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="f883e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f883e-169">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="f883e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-170">Search-Flags</span></span>           | <span data-ttu-id="f883e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f883e-171">0x00000000</span></span>   |
| <span data-ttu-id="f883e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-172">System-Flags</span></span>           | <span data-ttu-id="f883e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f883e-173">0x00000010</span></span>   |
| <span data-ttu-id="f883e-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f883e-174">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f883e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f883e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f883e-176">進入</span><span class="sxs-lookup"><span data-stu-id="f883e-176">Entry</span></span> | <span data-ttu-id="f883e-177">值</span><span class="sxs-lookup"><span data-stu-id="f883e-177">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f883e-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f883e-178">Link-Id</span></span>                | <span data-ttu-id="f883e-179">70</span><span class="sxs-lookup"><span data-stu-id="f883e-179">70</span></span>           |
| <span data-ttu-id="f883e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f883e-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="f883e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="f883e-181">System-Only</span></span>            | <span data-ttu-id="f883e-182">否</span><span class="sxs-lookup"><span data-stu-id="f883e-182">False</span></span>        |
| <span data-ttu-id="f883e-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f883e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="f883e-184">否</span><span class="sxs-lookup"><span data-stu-id="f883e-184">False</span></span>        |
| <span data-ttu-id="f883e-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f883e-185">Is Indexed</span></span>             | <span data-ttu-id="f883e-186">否</span><span class="sxs-lookup"><span data-stu-id="f883e-186">False</span></span>        |
| <span data-ttu-id="f883e-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f883e-187">In Global Catalog</span></span>      | <span data-ttu-id="f883e-188">否</span><span class="sxs-lookup"><span data-stu-id="f883e-188">False</span></span>        |
| <span data-ttu-id="f883e-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f883e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="f883e-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f883e-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="f883e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f883e-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="f883e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f883e-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="f883e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-193">Search-Flags</span></span>           | <span data-ttu-id="f883e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f883e-194">0x00000000</span></span>   |
| <span data-ttu-id="f883e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-195">System-Flags</span></span>           | <span data-ttu-id="f883e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f883e-196">0x00000010</span></span>   |
| <span data-ttu-id="f883e-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f883e-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="f883e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f883e-198">Windows Server 2008</span></span>



| <span data-ttu-id="f883e-199">進入</span><span class="sxs-lookup"><span data-stu-id="f883e-199">Entry</span></span> | <span data-ttu-id="f883e-200">值</span><span class="sxs-lookup"><span data-stu-id="f883e-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f883e-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f883e-201">Link-Id</span></span>                | <span data-ttu-id="f883e-202">70</span><span class="sxs-lookup"><span data-stu-id="f883e-202">70</span></span>           |
| <span data-ttu-id="f883e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f883e-203">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="f883e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="f883e-204">System-Only</span></span>            | <span data-ttu-id="f883e-205">否</span><span class="sxs-lookup"><span data-stu-id="f883e-205">False</span></span>        |
| <span data-ttu-id="f883e-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f883e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="f883e-207">否</span><span class="sxs-lookup"><span data-stu-id="f883e-207">False</span></span>        |
| <span data-ttu-id="f883e-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f883e-208">Is Indexed</span></span>             | <span data-ttu-id="f883e-209">否</span><span class="sxs-lookup"><span data-stu-id="f883e-209">False</span></span>        |
| <span data-ttu-id="f883e-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f883e-210">In Global Catalog</span></span>      | <span data-ttu-id="f883e-211">否</span><span class="sxs-lookup"><span data-stu-id="f883e-211">False</span></span>        |
| <span data-ttu-id="f883e-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f883e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="f883e-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f883e-213">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="f883e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f883e-214">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="f883e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f883e-215">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="f883e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-216">Search-Flags</span></span>           | <span data-ttu-id="f883e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f883e-217">0x00000000</span></span>   |
| <span data-ttu-id="f883e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-218">System-Flags</span></span>           | <span data-ttu-id="f883e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f883e-219">0x00000010</span></span>   |
| <span data-ttu-id="f883e-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f883e-220">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f883e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f883e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f883e-222">進入</span><span class="sxs-lookup"><span data-stu-id="f883e-222">Entry</span></span> | <span data-ttu-id="f883e-223">值</span><span class="sxs-lookup"><span data-stu-id="f883e-223">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f883e-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f883e-224">Link-Id</span></span>                | <span data-ttu-id="f883e-225">70</span><span class="sxs-lookup"><span data-stu-id="f883e-225">70</span></span>           |
| <span data-ttu-id="f883e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f883e-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="f883e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f883e-227">System-Only</span></span>            | <span data-ttu-id="f883e-228">否</span><span class="sxs-lookup"><span data-stu-id="f883e-228">False</span></span>        |
| <span data-ttu-id="f883e-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f883e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f883e-230">否</span><span class="sxs-lookup"><span data-stu-id="f883e-230">False</span></span>        |
| <span data-ttu-id="f883e-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f883e-231">Is Indexed</span></span>             | <span data-ttu-id="f883e-232">否</span><span class="sxs-lookup"><span data-stu-id="f883e-232">False</span></span>        |
| <span data-ttu-id="f883e-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f883e-233">In Global Catalog</span></span>      | <span data-ttu-id="f883e-234">否</span><span class="sxs-lookup"><span data-stu-id="f883e-234">False</span></span>        |
| <span data-ttu-id="f883e-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f883e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f883e-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f883e-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="f883e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f883e-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="f883e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f883e-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="f883e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-239">Search-Flags</span></span>           | <span data-ttu-id="f883e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f883e-240">0x00000000</span></span>   |
| <span data-ttu-id="f883e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-241">System-Flags</span></span>           | <span data-ttu-id="f883e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f883e-242">0x00000010</span></span>   |
| <span data-ttu-id="f883e-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f883e-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="f883e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f883e-244">Windows Server 2012</span></span>



| <span data-ttu-id="f883e-245">進入</span><span class="sxs-lookup"><span data-stu-id="f883e-245">Entry</span></span> | <span data-ttu-id="f883e-246">值</span><span class="sxs-lookup"><span data-stu-id="f883e-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f883e-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f883e-247">Link-Id</span></span>                | <span data-ttu-id="f883e-248">70</span><span class="sxs-lookup"><span data-stu-id="f883e-248">70</span></span>           |
| <span data-ttu-id="f883e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f883e-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="f883e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f883e-250">System-Only</span></span>            | <span data-ttu-id="f883e-251">否</span><span class="sxs-lookup"><span data-stu-id="f883e-251">False</span></span>        |
| <span data-ttu-id="f883e-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f883e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f883e-253">否</span><span class="sxs-lookup"><span data-stu-id="f883e-253">False</span></span>        |
| <span data-ttu-id="f883e-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f883e-254">Is Indexed</span></span>             | <span data-ttu-id="f883e-255">否</span><span class="sxs-lookup"><span data-stu-id="f883e-255">False</span></span>        |
| <span data-ttu-id="f883e-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f883e-256">In Global Catalog</span></span>      | <span data-ttu-id="f883e-257">否</span><span class="sxs-lookup"><span data-stu-id="f883e-257">False</span></span>        |
| <span data-ttu-id="f883e-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f883e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f883e-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f883e-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="f883e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f883e-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="f883e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f883e-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="f883e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-262">Search-Flags</span></span>           | <span data-ttu-id="f883e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f883e-263">0x00000000</span></span>   |
| <span data-ttu-id="f883e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f883e-264">System-Flags</span></span>           | <span data-ttu-id="f883e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f883e-265">0x00000010</span></span>   |
| <span data-ttu-id="f883e-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f883e-266">Classes used in</span></span>        | \-           |



 

 




