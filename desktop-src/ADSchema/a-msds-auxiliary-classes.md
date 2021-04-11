---
title: ms DS 輔助類別屬性
description: 這個屬性會列出已動態附加至物件的輔助類別。 這個屬性與類別沒有關聯。 系統會自動填入此檔案。
ms.assetid: bf41f15d-9af9-43de-8425-33d50880c3fa
ms.tgt_platform: multiple
keywords:
- ms DS 輔助類別屬性 AD 架構
- 輔助類別屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Auxiliary-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24608d0626ae4bcd6adb70a646d95121615c29e5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845183"
---
# <a name="ms-ds-auxiliary-classes-attribute"></a><span data-ttu-id="33552-107">ms DS 輔助類別屬性</span><span class="sxs-lookup"><span data-stu-id="33552-107">ms-DS-Auxiliary-Classes attribute</span></span>

<span data-ttu-id="33552-108">這個屬性會列出已動態附加至物件的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="33552-108">This attribute lists the auxiliary classes that have been dynamically attached to an object.</span></span> <span data-ttu-id="33552-109">這個屬性與類別沒有關聯。</span><span class="sxs-lookup"><span data-stu-id="33552-109">This attribute is not associated with a class.</span></span> <span data-ttu-id="33552-110">系統會自動填入此檔案。</span><span class="sxs-lookup"><span data-stu-id="33552-110">It is automatically populated by the system.</span></span>



| <span data-ttu-id="33552-111">進入</span><span class="sxs-lookup"><span data-stu-id="33552-111">Entry</span></span> | <span data-ttu-id="33552-112">值</span><span class="sxs-lookup"><span data-stu-id="33552-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="33552-113">CN</span><span class="sxs-lookup"><span data-stu-id="33552-113">CN</span></span>                | <span data-ttu-id="33552-114">ms DS 輔助類別</span><span class="sxs-lookup"><span data-stu-id="33552-114">ms-DS-Auxiliary-Classes</span></span>                                         |
| <span data-ttu-id="33552-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="33552-115">Ldap-Display-Name</span></span> | <span data-ttu-id="33552-116">輔助類別</span><span class="sxs-lookup"><span data-stu-id="33552-116">msDS-Auxiliary-Classes</span></span>                                          |
| <span data-ttu-id="33552-117">大小</span><span class="sxs-lookup"><span data-stu-id="33552-117">Size</span></span>              | \-                                                              |
| <span data-ttu-id="33552-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="33552-118">Update Privilege</span></span>  | <span data-ttu-id="33552-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="33552-119">This value is set by the system.</span></span>                                |
| <span data-ttu-id="33552-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="33552-120">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="33552-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="33552-121">Attribute-Id</span></span>      | <span data-ttu-id="33552-122">1.2.840.113556.1.4.1458</span><span class="sxs-lookup"><span data-stu-id="33552-122">1.2.840.113556.1.4.1458</span></span>                                         |
| <span data-ttu-id="33552-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="33552-123">System-Id-Guid</span></span>    | <span data-ttu-id="33552-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span><span class="sxs-lookup"><span data-stu-id="33552-124">c4af1073-ee50-4be0-b8c0-89a41fe99abe</span></span>                            |
| <span data-ttu-id="33552-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="33552-125">Syntax</span></span>            | [<span data-ttu-id="33552-126">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="33552-126">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="33552-127">實作</span><span class="sxs-lookup"><span data-stu-id="33552-127">Implementations</span></span>

-   [<span data-ttu-id="33552-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="33552-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="33552-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="33552-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="33552-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="33552-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="33552-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="33552-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="33552-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="33552-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="33552-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="33552-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="33552-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="33552-134">Windows Server 2003</span></span>



| <span data-ttu-id="33552-135">進入</span><span class="sxs-lookup"><span data-stu-id="33552-135">Entry</span></span> | <span data-ttu-id="33552-136">值</span><span class="sxs-lookup"><span data-stu-id="33552-136">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="33552-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33552-137">Link-Id</span></span>                | \-           |
| <span data-ttu-id="33552-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33552-138">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="33552-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="33552-139">System-Only</span></span>            | <span data-ttu-id="33552-140">對</span><span class="sxs-lookup"><span data-stu-id="33552-140">True</span></span>         |
| <span data-ttu-id="33552-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33552-141">Is-Single-Valued</span></span>       | <span data-ttu-id="33552-142">否</span><span class="sxs-lookup"><span data-stu-id="33552-142">False</span></span>        |
| <span data-ttu-id="33552-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33552-143">Is Indexed</span></span>             | <span data-ttu-id="33552-144">否</span><span class="sxs-lookup"><span data-stu-id="33552-144">False</span></span>        |
| <span data-ttu-id="33552-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33552-145">In Global Catalog</span></span>      | <span data-ttu-id="33552-146">否</span><span class="sxs-lookup"><span data-stu-id="33552-146">False</span></span>        |
| <span data-ttu-id="33552-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33552-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="33552-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33552-148">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="33552-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33552-149">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="33552-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33552-150">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="33552-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-151">Search-Flags</span></span>           | <span data-ttu-id="33552-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="33552-152">0x00000008</span></span>   |
| <span data-ttu-id="33552-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-153">System-Flags</span></span>           | <span data-ttu-id="33552-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33552-154">0x00000014</span></span>   |
| <span data-ttu-id="33552-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33552-155">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="33552-156">亞當</span><span class="sxs-lookup"><span data-stu-id="33552-156">ADAM</span></span>



| <span data-ttu-id="33552-157">進入</span><span class="sxs-lookup"><span data-stu-id="33552-157">Entry</span></span> | <span data-ttu-id="33552-158">值</span><span class="sxs-lookup"><span data-stu-id="33552-158">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="33552-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33552-159">Link-Id</span></span>                | \-           |
| <span data-ttu-id="33552-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33552-160">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="33552-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="33552-161">System-Only</span></span>            | <span data-ttu-id="33552-162">對</span><span class="sxs-lookup"><span data-stu-id="33552-162">True</span></span>         |
| <span data-ttu-id="33552-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33552-163">Is-Single-Valued</span></span>       | <span data-ttu-id="33552-164">否</span><span class="sxs-lookup"><span data-stu-id="33552-164">False</span></span>        |
| <span data-ttu-id="33552-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33552-165">Is Indexed</span></span>             | <span data-ttu-id="33552-166">否</span><span class="sxs-lookup"><span data-stu-id="33552-166">False</span></span>        |
| <span data-ttu-id="33552-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33552-167">In Global Catalog</span></span>      | <span data-ttu-id="33552-168">否</span><span class="sxs-lookup"><span data-stu-id="33552-168">False</span></span>        |
| <span data-ttu-id="33552-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33552-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="33552-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33552-170">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="33552-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33552-171">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="33552-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33552-172">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="33552-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-173">Search-Flags</span></span>           | <span data-ttu-id="33552-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="33552-174">0x00000008</span></span>   |
| <span data-ttu-id="33552-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-175">System-Flags</span></span>           | <span data-ttu-id="33552-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33552-176">0x00000014</span></span>   |
| <span data-ttu-id="33552-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33552-177">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="33552-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="33552-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="33552-179">進入</span><span class="sxs-lookup"><span data-stu-id="33552-179">Entry</span></span> | <span data-ttu-id="33552-180">值</span><span class="sxs-lookup"><span data-stu-id="33552-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="33552-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33552-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="33552-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33552-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="33552-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="33552-183">System-Only</span></span>            | <span data-ttu-id="33552-184">對</span><span class="sxs-lookup"><span data-stu-id="33552-184">True</span></span>         |
| <span data-ttu-id="33552-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33552-185">Is-Single-Valued</span></span>       | <span data-ttu-id="33552-186">否</span><span class="sxs-lookup"><span data-stu-id="33552-186">False</span></span>        |
| <span data-ttu-id="33552-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33552-187">Is Indexed</span></span>             | <span data-ttu-id="33552-188">否</span><span class="sxs-lookup"><span data-stu-id="33552-188">False</span></span>        |
| <span data-ttu-id="33552-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33552-189">In Global Catalog</span></span>      | <span data-ttu-id="33552-190">否</span><span class="sxs-lookup"><span data-stu-id="33552-190">False</span></span>        |
| <span data-ttu-id="33552-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33552-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="33552-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33552-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="33552-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33552-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="33552-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33552-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="33552-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-195">Search-Flags</span></span>           | <span data-ttu-id="33552-196">0x00000008</span><span class="sxs-lookup"><span data-stu-id="33552-196">0x00000008</span></span>   |
| <span data-ttu-id="33552-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-197">System-Flags</span></span>           | <span data-ttu-id="33552-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33552-198">0x00000014</span></span>   |
| <span data-ttu-id="33552-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33552-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="33552-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33552-200">Windows Server 2008</span></span>



| <span data-ttu-id="33552-201">進入</span><span class="sxs-lookup"><span data-stu-id="33552-201">Entry</span></span> | <span data-ttu-id="33552-202">值</span><span class="sxs-lookup"><span data-stu-id="33552-202">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="33552-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33552-203">Link-Id</span></span>                | \-           |
| <span data-ttu-id="33552-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33552-204">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="33552-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="33552-205">System-Only</span></span>            | <span data-ttu-id="33552-206">對</span><span class="sxs-lookup"><span data-stu-id="33552-206">True</span></span>         |
| <span data-ttu-id="33552-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33552-207">Is-Single-Valued</span></span>       | <span data-ttu-id="33552-208">否</span><span class="sxs-lookup"><span data-stu-id="33552-208">False</span></span>        |
| <span data-ttu-id="33552-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33552-209">Is Indexed</span></span>             | <span data-ttu-id="33552-210">否</span><span class="sxs-lookup"><span data-stu-id="33552-210">False</span></span>        |
| <span data-ttu-id="33552-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33552-211">In Global Catalog</span></span>      | <span data-ttu-id="33552-212">否</span><span class="sxs-lookup"><span data-stu-id="33552-212">False</span></span>        |
| <span data-ttu-id="33552-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33552-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="33552-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33552-214">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="33552-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33552-215">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="33552-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33552-216">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="33552-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-217">Search-Flags</span></span>           | <span data-ttu-id="33552-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="33552-218">0x00000008</span></span>   |
| <span data-ttu-id="33552-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-219">System-Flags</span></span>           | <span data-ttu-id="33552-220">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33552-220">0x00000014</span></span>   |
| <span data-ttu-id="33552-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33552-221">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="33552-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33552-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="33552-223">進入</span><span class="sxs-lookup"><span data-stu-id="33552-223">Entry</span></span> | <span data-ttu-id="33552-224">值</span><span class="sxs-lookup"><span data-stu-id="33552-224">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="33552-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33552-225">Link-Id</span></span>                | \-           |
| <span data-ttu-id="33552-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33552-226">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="33552-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="33552-227">System-Only</span></span>            | <span data-ttu-id="33552-228">對</span><span class="sxs-lookup"><span data-stu-id="33552-228">True</span></span>         |
| <span data-ttu-id="33552-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33552-229">Is-Single-Valued</span></span>       | <span data-ttu-id="33552-230">否</span><span class="sxs-lookup"><span data-stu-id="33552-230">False</span></span>        |
| <span data-ttu-id="33552-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33552-231">Is Indexed</span></span>             | <span data-ttu-id="33552-232">否</span><span class="sxs-lookup"><span data-stu-id="33552-232">False</span></span>        |
| <span data-ttu-id="33552-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33552-233">In Global Catalog</span></span>      | <span data-ttu-id="33552-234">否</span><span class="sxs-lookup"><span data-stu-id="33552-234">False</span></span>        |
| <span data-ttu-id="33552-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33552-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="33552-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33552-236">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="33552-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33552-237">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="33552-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33552-238">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="33552-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-239">Search-Flags</span></span>           | <span data-ttu-id="33552-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="33552-240">0x00000008</span></span>   |
| <span data-ttu-id="33552-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-241">System-Flags</span></span>           | <span data-ttu-id="33552-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33552-242">0x00000014</span></span>   |
| <span data-ttu-id="33552-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33552-243">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="33552-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33552-244">Windows Server 2012</span></span>



| <span data-ttu-id="33552-245">進入</span><span class="sxs-lookup"><span data-stu-id="33552-245">Entry</span></span> | <span data-ttu-id="33552-246">值</span><span class="sxs-lookup"><span data-stu-id="33552-246">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="33552-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="33552-247">Link-Id</span></span>                | \-           |
| <span data-ttu-id="33552-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33552-248">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="33552-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="33552-249">System-Only</span></span>            | <span data-ttu-id="33552-250">對</span><span class="sxs-lookup"><span data-stu-id="33552-250">True</span></span>         |
| <span data-ttu-id="33552-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="33552-251">Is-Single-Valued</span></span>       | <span data-ttu-id="33552-252">否</span><span class="sxs-lookup"><span data-stu-id="33552-252">False</span></span>        |
| <span data-ttu-id="33552-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="33552-253">Is Indexed</span></span>             | <span data-ttu-id="33552-254">否</span><span class="sxs-lookup"><span data-stu-id="33552-254">False</span></span>        |
| <span data-ttu-id="33552-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="33552-255">In Global Catalog</span></span>      | <span data-ttu-id="33552-256">否</span><span class="sxs-lookup"><span data-stu-id="33552-256">False</span></span>        |
| <span data-ttu-id="33552-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="33552-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="33552-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="33552-258">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="33552-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33552-259">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="33552-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33552-260">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="33552-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-261">Search-Flags</span></span>           | <span data-ttu-id="33552-262">0x00000008</span><span class="sxs-lookup"><span data-stu-id="33552-262">0x00000008</span></span>   |
| <span data-ttu-id="33552-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33552-263">System-Flags</span></span>           | <span data-ttu-id="33552-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33552-264">0x00000014</span></span>   |
| <span data-ttu-id="33552-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="33552-265">Classes used in</span></span>        | \-           |



 

 




