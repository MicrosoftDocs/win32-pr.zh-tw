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
# <a name="privilege-holder-attribute"></a><span data-ttu-id="ebf4d-105">Privilege-Holder 屬性</span><span class="sxs-lookup"><span data-stu-id="ebf4d-105">Privilege-Holder attribute</span></span>

<span data-ttu-id="ebf4d-106">授與此許可權之主體的辨別名稱清單。</span><span class="sxs-lookup"><span data-stu-id="ebf4d-106">List of Distinguished Names of principals granted this privilege.</span></span>



| <span data-ttu-id="ebf4d-107">進入</span><span class="sxs-lookup"><span data-stu-id="ebf4d-107">Entry</span></span> | <span data-ttu-id="ebf4d-108">值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ebf4d-109">CN</span><span class="sxs-lookup"><span data-stu-id="ebf4d-109">CN</span></span>                | <span data-ttu-id="ebf4d-110">Privilege-Holder</span><span class="sxs-lookup"><span data-stu-id="ebf4d-110">Privilege-Holder</span></span>                        |
| <span data-ttu-id="ebf4d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ebf4d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ebf4d-112">privilegeHolder</span><span class="sxs-lookup"><span data-stu-id="ebf4d-112">privilegeHolder</span></span>                         |
| <span data-ttu-id="ebf4d-113">大小</span><span class="sxs-lookup"><span data-stu-id="ebf4d-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="ebf4d-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ebf4d-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="ebf4d-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ebf4d-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="ebf4d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ebf4d-116">Attribute-Id</span></span>      | <span data-ttu-id="ebf4d-117">1.2.840.113556.1.4.637</span><span class="sxs-lookup"><span data-stu-id="ebf4d-117">1.2.840.113556.1.4.637</span></span>                  |
| <span data-ttu-id="ebf4d-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ebf4d-118">System-Id-Guid</span></span>    | <span data-ttu-id="ebf4d-119">19405b9b-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ebf4d-119">19405b9b-3cfa-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="ebf4d-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebf4d-120">Syntax</span></span>            | [<span data-ttu-id="ebf4d-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ebf4d-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="ebf4d-122">實作</span><span class="sxs-lookup"><span data-stu-id="ebf4d-122">Implementations</span></span>

-   [<span data-ttu-id="ebf4d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ebf4d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ebf4d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ebf4d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ebf4d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ebf4d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ebf4d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ebf4d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ebf4d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ebf4d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ebf4d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ebf4d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ebf4d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ebf4d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ebf4d-130">進入</span><span class="sxs-lookup"><span data-stu-id="ebf4d-130">Entry</span></span> | <span data-ttu-id="ebf4d-131">值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="ebf4d-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ebf4d-132">Link-Id</span></span>                | <span data-ttu-id="ebf4d-133">70</span><span class="sxs-lookup"><span data-stu-id="ebf4d-133">70</span></span>           |
| <span data-ttu-id="ebf4d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf4d-134">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="ebf4d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf4d-135">System-Only</span></span>            | <span data-ttu-id="ebf4d-136">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-136">False</span></span>        |
| <span data-ttu-id="ebf4d-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf4d-138">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-138">False</span></span>        |
| <span data-ttu-id="ebf4d-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ebf4d-139">Is Indexed</span></span>             | <span data-ttu-id="ebf4d-140">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-140">False</span></span>        |
| <span data-ttu-id="ebf4d-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ebf4d-141">In Global Catalog</span></span>      | <span data-ttu-id="ebf4d-142">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-142">False</span></span>        |
| <span data-ttu-id="ebf4d-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ebf4d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf4d-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ebf4d-144">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="ebf4d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf4d-145">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="ebf4d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf4d-146">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="ebf4d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-147">Search-Flags</span></span>           | <span data-ttu-id="ebf4d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf4d-148">0x00000000</span></span>   |
| <span data-ttu-id="ebf4d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-149">System-Flags</span></span>           | <span data-ttu-id="ebf4d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebf4d-150">0x00000010</span></span>   |
| <span data-ttu-id="ebf4d-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ebf4d-151">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="ebf4d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebf4d-152">Windows Server 2003</span></span>



| <span data-ttu-id="ebf4d-153">進入</span><span class="sxs-lookup"><span data-stu-id="ebf4d-153">Entry</span></span> | <span data-ttu-id="ebf4d-154">值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-154">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="ebf4d-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ebf4d-155">Link-Id</span></span>                | <span data-ttu-id="ebf4d-156">70</span><span class="sxs-lookup"><span data-stu-id="ebf4d-156">70</span></span>           |
| <span data-ttu-id="ebf4d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf4d-157">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="ebf4d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf4d-158">System-Only</span></span>            | <span data-ttu-id="ebf4d-159">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-159">False</span></span>        |
| <span data-ttu-id="ebf4d-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf4d-161">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-161">False</span></span>        |
| <span data-ttu-id="ebf4d-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ebf4d-162">Is Indexed</span></span>             | <span data-ttu-id="ebf4d-163">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-163">False</span></span>        |
| <span data-ttu-id="ebf4d-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ebf4d-164">In Global Catalog</span></span>      | <span data-ttu-id="ebf4d-165">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-165">False</span></span>        |
| <span data-ttu-id="ebf4d-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ebf4d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf4d-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ebf4d-167">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="ebf4d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf4d-168">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="ebf4d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf4d-169">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="ebf4d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-170">Search-Flags</span></span>           | <span data-ttu-id="ebf4d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf4d-171">0x00000000</span></span>   |
| <span data-ttu-id="ebf4d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-172">System-Flags</span></span>           | <span data-ttu-id="ebf4d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebf4d-173">0x00000010</span></span>   |
| <span data-ttu-id="ebf4d-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ebf4d-174">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ebf4d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ebf4d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ebf4d-176">進入</span><span class="sxs-lookup"><span data-stu-id="ebf4d-176">Entry</span></span> | <span data-ttu-id="ebf4d-177">值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-177">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="ebf4d-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ebf4d-178">Link-Id</span></span>                | <span data-ttu-id="ebf4d-179">70</span><span class="sxs-lookup"><span data-stu-id="ebf4d-179">70</span></span>           |
| <span data-ttu-id="ebf4d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf4d-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="ebf4d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf4d-181">System-Only</span></span>            | <span data-ttu-id="ebf4d-182">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-182">False</span></span>        |
| <span data-ttu-id="ebf4d-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf4d-184">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-184">False</span></span>        |
| <span data-ttu-id="ebf4d-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ebf4d-185">Is Indexed</span></span>             | <span data-ttu-id="ebf4d-186">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-186">False</span></span>        |
| <span data-ttu-id="ebf4d-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ebf4d-187">In Global Catalog</span></span>      | <span data-ttu-id="ebf4d-188">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-188">False</span></span>        |
| <span data-ttu-id="ebf4d-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ebf4d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf4d-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ebf4d-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="ebf4d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf4d-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="ebf4d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf4d-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="ebf4d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-193">Search-Flags</span></span>           | <span data-ttu-id="ebf4d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf4d-194">0x00000000</span></span>   |
| <span data-ttu-id="ebf4d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-195">System-Flags</span></span>           | <span data-ttu-id="ebf4d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebf4d-196">0x00000010</span></span>   |
| <span data-ttu-id="ebf4d-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ebf4d-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="ebf4d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebf4d-198">Windows Server 2008</span></span>



| <span data-ttu-id="ebf4d-199">進入</span><span class="sxs-lookup"><span data-stu-id="ebf4d-199">Entry</span></span> | <span data-ttu-id="ebf4d-200">值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="ebf4d-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ebf4d-201">Link-Id</span></span>                | <span data-ttu-id="ebf4d-202">70</span><span class="sxs-lookup"><span data-stu-id="ebf4d-202">70</span></span>           |
| <span data-ttu-id="ebf4d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf4d-203">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="ebf4d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf4d-204">System-Only</span></span>            | <span data-ttu-id="ebf4d-205">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-205">False</span></span>        |
| <span data-ttu-id="ebf4d-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf4d-207">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-207">False</span></span>        |
| <span data-ttu-id="ebf4d-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ebf4d-208">Is Indexed</span></span>             | <span data-ttu-id="ebf4d-209">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-209">False</span></span>        |
| <span data-ttu-id="ebf4d-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ebf4d-210">In Global Catalog</span></span>      | <span data-ttu-id="ebf4d-211">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-211">False</span></span>        |
| <span data-ttu-id="ebf4d-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ebf4d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf4d-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ebf4d-213">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="ebf4d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf4d-214">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="ebf4d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf4d-215">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="ebf4d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-216">Search-Flags</span></span>           | <span data-ttu-id="ebf4d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf4d-217">0x00000000</span></span>   |
| <span data-ttu-id="ebf4d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-218">System-Flags</span></span>           | <span data-ttu-id="ebf4d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebf4d-219">0x00000010</span></span>   |
| <span data-ttu-id="ebf4d-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ebf4d-220">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ebf4d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebf4d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ebf4d-222">進入</span><span class="sxs-lookup"><span data-stu-id="ebf4d-222">Entry</span></span> | <span data-ttu-id="ebf4d-223">值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-223">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="ebf4d-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ebf4d-224">Link-Id</span></span>                | <span data-ttu-id="ebf4d-225">70</span><span class="sxs-lookup"><span data-stu-id="ebf4d-225">70</span></span>           |
| <span data-ttu-id="ebf4d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf4d-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="ebf4d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf4d-227">System-Only</span></span>            | <span data-ttu-id="ebf4d-228">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-228">False</span></span>        |
| <span data-ttu-id="ebf4d-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf4d-230">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-230">False</span></span>        |
| <span data-ttu-id="ebf4d-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ebf4d-231">Is Indexed</span></span>             | <span data-ttu-id="ebf4d-232">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-232">False</span></span>        |
| <span data-ttu-id="ebf4d-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ebf4d-233">In Global Catalog</span></span>      | <span data-ttu-id="ebf4d-234">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-234">False</span></span>        |
| <span data-ttu-id="ebf4d-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ebf4d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf4d-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ebf4d-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="ebf4d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf4d-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="ebf4d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf4d-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="ebf4d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-239">Search-Flags</span></span>           | <span data-ttu-id="ebf4d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf4d-240">0x00000000</span></span>   |
| <span data-ttu-id="ebf4d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-241">System-Flags</span></span>           | <span data-ttu-id="ebf4d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebf4d-242">0x00000010</span></span>   |
| <span data-ttu-id="ebf4d-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ebf4d-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="ebf4d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ebf4d-244">Windows Server 2012</span></span>



| <span data-ttu-id="ebf4d-245">進入</span><span class="sxs-lookup"><span data-stu-id="ebf4d-245">Entry</span></span> | <span data-ttu-id="ebf4d-246">值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="ebf4d-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ebf4d-247">Link-Id</span></span>                | <span data-ttu-id="ebf4d-248">70</span><span class="sxs-lookup"><span data-stu-id="ebf4d-248">70</span></span>           |
| <span data-ttu-id="ebf4d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebf4d-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="ebf4d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebf4d-250">System-Only</span></span>            | <span data-ttu-id="ebf4d-251">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-251">False</span></span>        |
| <span data-ttu-id="ebf4d-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ebf4d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ebf4d-253">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-253">False</span></span>        |
| <span data-ttu-id="ebf4d-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ebf4d-254">Is Indexed</span></span>             | <span data-ttu-id="ebf4d-255">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-255">False</span></span>        |
| <span data-ttu-id="ebf4d-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ebf4d-256">In Global Catalog</span></span>      | <span data-ttu-id="ebf4d-257">否</span><span class="sxs-lookup"><span data-stu-id="ebf4d-257">False</span></span>        |
| <span data-ttu-id="ebf4d-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ebf4d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebf4d-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ebf4d-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="ebf4d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebf4d-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="ebf4d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebf4d-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="ebf4d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-262">Search-Flags</span></span>           | <span data-ttu-id="ebf4d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebf4d-263">0x00000000</span></span>   |
| <span data-ttu-id="ebf4d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebf4d-264">System-Flags</span></span>           | <span data-ttu-id="ebf4d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebf4d-265">0x00000010</span></span>   |
| <span data-ttu-id="ebf4d-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ebf4d-266">Classes used in</span></span>        | \-           |



 

 




