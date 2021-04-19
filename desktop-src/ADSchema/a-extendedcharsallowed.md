---
title: 擴充字元-允許的屬性
description: 指出這個屬性的值是否允許擴充字元。 只適用于 IA5、Numeric、可列印和 Teletex 字串屬性。
ms.assetid: aeacb5ef-9af2-498b-ae53-b3095de0d0c6
ms.tgt_platform: multiple
keywords:
- 擴充字元-允許的屬性 AD 架構
- extendedCharsAllowed 屬性 AD 架構
topic_type:
- apiref
api_name:
- Extended-Chars-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e26194232387f27f3177f13edeab90efc97a4bb3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972492"
---
# <a name="extended-chars-allowed-attribute"></a><span data-ttu-id="c2eaa-106">擴充字元-允許的屬性</span><span class="sxs-lookup"><span data-stu-id="c2eaa-106">Extended-Chars-Allowed attribute</span></span>

<span data-ttu-id="c2eaa-107">指出這個屬性的值是否允許擴充字元。</span><span class="sxs-lookup"><span data-stu-id="c2eaa-107">Indicates whether extended characters are allowed in the value of this attribute.</span></span> <span data-ttu-id="c2eaa-108">只適用于 IA5、Numeric、可列印和 Teletex 字串屬性。</span><span class="sxs-lookup"><span data-stu-id="c2eaa-108">Only applies to IA5, Numeric, Printable, and Teletex string attributes.</span></span>



| <span data-ttu-id="c2eaa-109">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-109">Entry</span></span> | <span data-ttu-id="c2eaa-110">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c2eaa-111">CN</span><span class="sxs-lookup"><span data-stu-id="c2eaa-111">CN</span></span>                | <span data-ttu-id="c2eaa-112">擴充字元-允許</span><span class="sxs-lookup"><span data-stu-id="c2eaa-112">Extended-Chars-Allowed</span></span>               |
| <span data-ttu-id="c2eaa-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c2eaa-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c2eaa-114">extendedCharsAllowed</span><span class="sxs-lookup"><span data-stu-id="c2eaa-114">extendedCharsAllowed</span></span>                 |
| <span data-ttu-id="c2eaa-115">大小</span><span class="sxs-lookup"><span data-stu-id="c2eaa-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="c2eaa-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c2eaa-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c2eaa-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c2eaa-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c2eaa-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-118">Attribute-Id</span></span>      | <span data-ttu-id="c2eaa-119">1.2.840.113556.1.2.380</span><span class="sxs-lookup"><span data-stu-id="c2eaa-119">1.2.840.113556.1.2.380</span></span>               |
| <span data-ttu-id="c2eaa-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c2eaa-120">System-Id-Guid</span></span>    | <span data-ttu-id="c2eaa-121">bf967966-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c2eaa-121">bf967966-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c2eaa-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2eaa-122">Syntax</span></span>            | [<span data-ttu-id="c2eaa-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c2eaa-124">實作</span><span class="sxs-lookup"><span data-stu-id="c2eaa-124">Implementations</span></span>

-   [<span data-ttu-id="c2eaa-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c2eaa-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c2eaa-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c2eaa-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c2eaa-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c2eaa-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c2eaa-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c2eaa-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2eaa-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c2eaa-133">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-133">Entry</span></span> | <span data-ttu-id="c2eaa-134">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c2eaa-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2eaa-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c2eaa-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-136">MAPI-Id</span></span>                | <span data-ttu-id="c2eaa-137">0x80A7</span><span class="sxs-lookup"><span data-stu-id="c2eaa-137">0x80A7</span></span>                                                   |
| <span data-ttu-id="c2eaa-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2eaa-138">System-Only</span></span>            | <span data-ttu-id="c2eaa-139">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-139">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c2eaa-141">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-141">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2eaa-142">Is Indexed</span></span>             | <span data-ttu-id="c2eaa-143">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-143">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2eaa-144">In Global Catalog</span></span>      | <span data-ttu-id="c2eaa-145">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-145">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2eaa-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2eaa-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2eaa-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c2eaa-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2eaa-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2eaa-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-150">Search-Flags</span></span>           | <span data-ttu-id="c2eaa-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2eaa-151">0x00000000</span></span>                                               |
| <span data-ttu-id="c2eaa-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-152">System-Flags</span></span>           | <span data-ttu-id="c2eaa-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2eaa-153">0x00000010</span></span>                                               |
| <span data-ttu-id="c2eaa-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2eaa-154">Classes used in</span></span>        | [<span data-ttu-id="c2eaa-155">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c2eaa-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2eaa-156">Windows Server 2003</span></span>



| <span data-ttu-id="c2eaa-157">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-157">Entry</span></span> | <span data-ttu-id="c2eaa-158">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c2eaa-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2eaa-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c2eaa-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-160">MAPI-Id</span></span>                | <span data-ttu-id="c2eaa-161">0x80A7</span><span class="sxs-lookup"><span data-stu-id="c2eaa-161">0x80A7</span></span>                                                   |
| <span data-ttu-id="c2eaa-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2eaa-162">System-Only</span></span>            | <span data-ttu-id="c2eaa-163">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-163">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c2eaa-165">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-165">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2eaa-166">Is Indexed</span></span>             | <span data-ttu-id="c2eaa-167">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-167">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2eaa-168">In Global Catalog</span></span>      | <span data-ttu-id="c2eaa-169">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-169">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2eaa-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2eaa-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2eaa-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c2eaa-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2eaa-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2eaa-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-174">Search-Flags</span></span>           | <span data-ttu-id="c2eaa-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2eaa-175">0x00000000</span></span>                                               |
| <span data-ttu-id="c2eaa-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-176">System-Flags</span></span>           | <span data-ttu-id="c2eaa-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2eaa-177">0x00000010</span></span>                                               |
| <span data-ttu-id="c2eaa-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2eaa-178">Classes used in</span></span>        | [<span data-ttu-id="c2eaa-179">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c2eaa-180">亞當</span><span class="sxs-lookup"><span data-stu-id="c2eaa-180">ADAM</span></span>



| <span data-ttu-id="c2eaa-181">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-181">Entry</span></span> | <span data-ttu-id="c2eaa-182">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c2eaa-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2eaa-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c2eaa-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-184">MAPI-Id</span></span>                | <span data-ttu-id="c2eaa-185">0x80A7</span><span class="sxs-lookup"><span data-stu-id="c2eaa-185">0x80A7</span></span>                                                   |
| <span data-ttu-id="c2eaa-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2eaa-186">System-Only</span></span>            | <span data-ttu-id="c2eaa-187">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-187">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-188">Is-Single-Valued</span></span>       | <span data-ttu-id="c2eaa-189">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-189">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2eaa-190">Is Indexed</span></span>             | <span data-ttu-id="c2eaa-191">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-191">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2eaa-192">In Global Catalog</span></span>      | <span data-ttu-id="c2eaa-193">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-193">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2eaa-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2eaa-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2eaa-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c2eaa-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2eaa-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2eaa-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-198">Search-Flags</span></span>           | <span data-ttu-id="c2eaa-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2eaa-199">0x00000000</span></span>                                               |
| <span data-ttu-id="c2eaa-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-200">System-Flags</span></span>           | <span data-ttu-id="c2eaa-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2eaa-201">0x00000010</span></span>                                               |
| <span data-ttu-id="c2eaa-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2eaa-202">Classes used in</span></span>        | [<span data-ttu-id="c2eaa-203">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c2eaa-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c2eaa-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c2eaa-205">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-205">Entry</span></span> | <span data-ttu-id="c2eaa-206">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c2eaa-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2eaa-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c2eaa-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-208">MAPI-Id</span></span>                | <span data-ttu-id="c2eaa-209">0x80A7</span><span class="sxs-lookup"><span data-stu-id="c2eaa-209">0x80A7</span></span>                                                   |
| <span data-ttu-id="c2eaa-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2eaa-210">System-Only</span></span>            | <span data-ttu-id="c2eaa-211">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-211">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c2eaa-213">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-213">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2eaa-214">Is Indexed</span></span>             | <span data-ttu-id="c2eaa-215">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-215">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2eaa-216">In Global Catalog</span></span>      | <span data-ttu-id="c2eaa-217">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-217">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2eaa-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2eaa-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2eaa-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c2eaa-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2eaa-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2eaa-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-222">Search-Flags</span></span>           | <span data-ttu-id="c2eaa-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2eaa-223">0x00000000</span></span>                                               |
| <span data-ttu-id="c2eaa-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-224">System-Flags</span></span>           | <span data-ttu-id="c2eaa-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2eaa-225">0x00000010</span></span>                                               |
| <span data-ttu-id="c2eaa-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2eaa-226">Classes used in</span></span>        | [<span data-ttu-id="c2eaa-227">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c2eaa-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2eaa-228">Windows Server 2008</span></span>



| <span data-ttu-id="c2eaa-229">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-229">Entry</span></span> | <span data-ttu-id="c2eaa-230">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c2eaa-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2eaa-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c2eaa-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-232">MAPI-Id</span></span>                | <span data-ttu-id="c2eaa-233">0x80A7</span><span class="sxs-lookup"><span data-stu-id="c2eaa-233">0x80A7</span></span>                                                   |
| <span data-ttu-id="c2eaa-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2eaa-234">System-Only</span></span>            | <span data-ttu-id="c2eaa-235">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-235">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-236">Is-Single-Valued</span></span>       | <span data-ttu-id="c2eaa-237">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-237">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2eaa-238">Is Indexed</span></span>             | <span data-ttu-id="c2eaa-239">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-239">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2eaa-240">In Global Catalog</span></span>      | <span data-ttu-id="c2eaa-241">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-241">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2eaa-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2eaa-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2eaa-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c2eaa-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2eaa-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2eaa-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-246">Search-Flags</span></span>           | <span data-ttu-id="c2eaa-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2eaa-247">0x00000000</span></span>                                               |
| <span data-ttu-id="c2eaa-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-248">System-Flags</span></span>           | <span data-ttu-id="c2eaa-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2eaa-249">0x00000010</span></span>                                               |
| <span data-ttu-id="c2eaa-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2eaa-250">Classes used in</span></span>        | [<span data-ttu-id="c2eaa-251">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c2eaa-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2eaa-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c2eaa-253">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-253">Entry</span></span> | <span data-ttu-id="c2eaa-254">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c2eaa-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2eaa-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c2eaa-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-256">MAPI-Id</span></span>                | <span data-ttu-id="c2eaa-257">0x80A7</span><span class="sxs-lookup"><span data-stu-id="c2eaa-257">0x80A7</span></span>                                                   |
| <span data-ttu-id="c2eaa-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2eaa-258">System-Only</span></span>            | <span data-ttu-id="c2eaa-259">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-259">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-260">Is-Single-Valued</span></span>       | <span data-ttu-id="c2eaa-261">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-261">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2eaa-262">Is Indexed</span></span>             | <span data-ttu-id="c2eaa-263">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-263">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2eaa-264">In Global Catalog</span></span>      | <span data-ttu-id="c2eaa-265">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-265">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2eaa-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2eaa-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2eaa-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c2eaa-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2eaa-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2eaa-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-270">Search-Flags</span></span>           | <span data-ttu-id="c2eaa-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2eaa-271">0x00000000</span></span>                                               |
| <span data-ttu-id="c2eaa-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-272">System-Flags</span></span>           | <span data-ttu-id="c2eaa-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2eaa-273">0x00000010</span></span>                                               |
| <span data-ttu-id="c2eaa-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2eaa-274">Classes used in</span></span>        | [<span data-ttu-id="c2eaa-275">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c2eaa-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2eaa-276">Windows Server 2012</span></span>



| <span data-ttu-id="c2eaa-277">進入</span><span class="sxs-lookup"><span data-stu-id="c2eaa-277">Entry</span></span> | <span data-ttu-id="c2eaa-278">值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c2eaa-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c2eaa-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c2eaa-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c2eaa-280">MAPI-Id</span></span>                | <span data-ttu-id="c2eaa-281">0x80A7</span><span class="sxs-lookup"><span data-stu-id="c2eaa-281">0x80A7</span></span>                                                   |
| <span data-ttu-id="c2eaa-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="c2eaa-282">System-Only</span></span>            | <span data-ttu-id="c2eaa-283">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-283">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c2eaa-284">Is-Single-Valued</span></span>       | <span data-ttu-id="c2eaa-285">對</span><span class="sxs-lookup"><span data-stu-id="c2eaa-285">True</span></span>                                                     |
| <span data-ttu-id="c2eaa-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c2eaa-286">Is Indexed</span></span>             | <span data-ttu-id="c2eaa-287">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-287">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c2eaa-288">In Global Catalog</span></span>      | <span data-ttu-id="c2eaa-289">否</span><span class="sxs-lookup"><span data-stu-id="c2eaa-289">False</span></span>                                                    |
| <span data-ttu-id="c2eaa-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c2eaa-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="c2eaa-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c2eaa-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c2eaa-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c2eaa-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c2eaa-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="c2eaa-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-294">Search-Flags</span></span>           | <span data-ttu-id="c2eaa-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c2eaa-295">0x00000000</span></span>                                               |
| <span data-ttu-id="c2eaa-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c2eaa-296">System-Flags</span></span>           | <span data-ttu-id="c2eaa-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c2eaa-297">0x00000010</span></span>                                               |
| <span data-ttu-id="c2eaa-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c2eaa-298">Classes used in</span></span>        | [<span data-ttu-id="c2eaa-299">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="c2eaa-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





