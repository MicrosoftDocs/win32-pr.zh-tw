---
title: 擴充類別資訊屬性
description: 多值屬性，其中包含代表每個類別之其他資訊的字串。 每個值都包含類別的 governsID、lDAPDisplayName 和 schemaIDGUID。
ms.assetid: f0f07950-28f8-4fe7-b030-1ab7632569e1
ms.tgt_platform: multiple
keywords:
- 擴充類別資訊屬性 AD 架構
- extendedClassInfo 屬性 AD 架構
topic_type:
- apiref
api_name:
- Extended-Class-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1b3320f547a3dbb41a151a33765cf9729e82c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385350"
---
# <a name="extended-class-info-attribute"></a><span data-ttu-id="46f9d-106">擴充類別資訊屬性</span><span class="sxs-lookup"><span data-stu-id="46f9d-106">Extended-Class-Info attribute</span></span>

<span data-ttu-id="46f9d-107">多值屬性，其中包含代表每個類別之其他資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="46f9d-107">A multi-valued property that contains strings that represent additional information for each class.</span></span> <span data-ttu-id="46f9d-108">每個值都包含類別的 governsID、lDAPDisplayName 和 schemaIDGUID。</span><span class="sxs-lookup"><span data-stu-id="46f9d-108">Each value contains the governsID, lDAPDisplayName, and schemaIDGUID of the class.</span></span>



| <span data-ttu-id="46f9d-109">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-109">Entry</span></span> | <span data-ttu-id="46f9d-110">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-111">CN</span><span class="sxs-lookup"><span data-stu-id="46f9d-111">CN</span></span>                | <span data-ttu-id="46f9d-112">擴充類別資訊</span><span class="sxs-lookup"><span data-stu-id="46f9d-112">Extended-Class-Info</span></span>                         |
| <span data-ttu-id="46f9d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="46f9d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="46f9d-114">extendedClassInfo</span><span class="sxs-lookup"><span data-stu-id="46f9d-114">extendedClassInfo</span></span>                           |
| <span data-ttu-id="46f9d-115">大小</span><span class="sxs-lookup"><span data-stu-id="46f9d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="46f9d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="46f9d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="46f9d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="46f9d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="46f9d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-118">Attribute-Id</span></span>      | <span data-ttu-id="46f9d-119">1.2.840.113556.1.4.908</span><span class="sxs-lookup"><span data-stu-id="46f9d-119">1.2.840.113556.1.4.908</span></span>                      |
| <span data-ttu-id="46f9d-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="46f9d-120">System-Id-Guid</span></span>    | <span data-ttu-id="46f9d-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="46f9d-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="46f9d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="46f9d-122">Syntax</span></span>            | [<span data-ttu-id="46f9d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="46f9d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="46f9d-124">實作</span><span class="sxs-lookup"><span data-stu-id="46f9d-124">Implementations</span></span>

-   [<span data-ttu-id="46f9d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="46f9d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="46f9d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46f9d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46f9d-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="46f9d-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="46f9d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46f9d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46f9d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46f9d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46f9d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46f9d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46f9d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46f9d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="46f9d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46f9d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="46f9d-133">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-133">Entry</span></span> | <span data-ttu-id="46f9d-134">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-134">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46f9d-135">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-136">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="46f9d-137">System-Only</span></span>            | <span data-ttu-id="46f9d-138">對</span><span class="sxs-lookup"><span data-stu-id="46f9d-138">True</span></span>                                        |
| <span data-ttu-id="46f9d-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46f9d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="46f9d-140">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-140">False</span></span>                                       |
| <span data-ttu-id="46f9d-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46f9d-141">Is Indexed</span></span>             | <span data-ttu-id="46f9d-142">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-142">False</span></span>                                       |
| <span data-ttu-id="46f9d-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46f9d-143">In Global Catalog</span></span>      | <span data-ttu-id="46f9d-144">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-144">False</span></span>                                       |
| <span data-ttu-id="46f9d-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46f9d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="46f9d-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46f9d-146">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="46f9d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46f9d-147">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46f9d-148">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-149">Search-Flags</span></span>           | <span data-ttu-id="46f9d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46f9d-150">0x00000000</span></span>                                  |
| <span data-ttu-id="46f9d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-151">System-Flags</span></span>           | <span data-ttu-id="46f9d-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="46f9d-152">0x08000014</span></span>                                  |
| <span data-ttu-id="46f9d-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46f9d-153">Classes used in</span></span>        | [<span data-ttu-id="46f9d-154">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="46f9d-154">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="46f9d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46f9d-155">Windows Server 2003</span></span>



| <span data-ttu-id="46f9d-156">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-156">Entry</span></span> | <span data-ttu-id="46f9d-157">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-157">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46f9d-158">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-159">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="46f9d-160">System-Only</span></span>            | <span data-ttu-id="46f9d-161">對</span><span class="sxs-lookup"><span data-stu-id="46f9d-161">True</span></span>                                        |
| <span data-ttu-id="46f9d-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46f9d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="46f9d-163">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-163">False</span></span>                                       |
| <span data-ttu-id="46f9d-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46f9d-164">Is Indexed</span></span>             | <span data-ttu-id="46f9d-165">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-165">False</span></span>                                       |
| <span data-ttu-id="46f9d-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46f9d-166">In Global Catalog</span></span>      | <span data-ttu-id="46f9d-167">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-167">False</span></span>                                       |
| <span data-ttu-id="46f9d-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46f9d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="46f9d-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46f9d-169">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="46f9d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46f9d-170">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46f9d-171">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-172">Search-Flags</span></span>           | <span data-ttu-id="46f9d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46f9d-173">0x00000000</span></span>                                  |
| <span data-ttu-id="46f9d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-174">System-Flags</span></span>           | <span data-ttu-id="46f9d-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="46f9d-175">0x08000014</span></span>                                  |
| <span data-ttu-id="46f9d-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46f9d-176">Classes used in</span></span>        | [<span data-ttu-id="46f9d-177">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="46f9d-177">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="46f9d-178">亞當</span><span class="sxs-lookup"><span data-stu-id="46f9d-178">ADAM</span></span>



| <span data-ttu-id="46f9d-179">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-179">Entry</span></span> | <span data-ttu-id="46f9d-180">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-180">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46f9d-181">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-182">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="46f9d-183">System-Only</span></span>            | <span data-ttu-id="46f9d-184">對</span><span class="sxs-lookup"><span data-stu-id="46f9d-184">True</span></span>                                        |
| <span data-ttu-id="46f9d-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46f9d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="46f9d-186">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-186">False</span></span>                                       |
| <span data-ttu-id="46f9d-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46f9d-187">Is Indexed</span></span>             | <span data-ttu-id="46f9d-188">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-188">False</span></span>                                       |
| <span data-ttu-id="46f9d-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46f9d-189">In Global Catalog</span></span>      | <span data-ttu-id="46f9d-190">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-190">False</span></span>                                       |
| <span data-ttu-id="46f9d-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46f9d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="46f9d-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46f9d-192">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="46f9d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46f9d-193">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46f9d-194">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-195">Search-Flags</span></span>           | <span data-ttu-id="46f9d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46f9d-196">0x00000000</span></span>                                  |
| <span data-ttu-id="46f9d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-197">System-Flags</span></span>           | <span data-ttu-id="46f9d-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="46f9d-198">0x08000014</span></span>                                  |
| <span data-ttu-id="46f9d-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46f9d-199">Classes used in</span></span>        | [<span data-ttu-id="46f9d-200">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="46f9d-200">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46f9d-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46f9d-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46f9d-202">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-202">Entry</span></span> | <span data-ttu-id="46f9d-203">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-203">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46f9d-204">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-205">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="46f9d-206">System-Only</span></span>            | <span data-ttu-id="46f9d-207">對</span><span class="sxs-lookup"><span data-stu-id="46f9d-207">True</span></span>                                        |
| <span data-ttu-id="46f9d-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46f9d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="46f9d-209">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-209">False</span></span>                                       |
| <span data-ttu-id="46f9d-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46f9d-210">Is Indexed</span></span>             | <span data-ttu-id="46f9d-211">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-211">False</span></span>                                       |
| <span data-ttu-id="46f9d-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46f9d-212">In Global Catalog</span></span>      | <span data-ttu-id="46f9d-213">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-213">False</span></span>                                       |
| <span data-ttu-id="46f9d-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46f9d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="46f9d-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46f9d-215">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="46f9d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46f9d-216">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46f9d-217">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-218">Search-Flags</span></span>           | <span data-ttu-id="46f9d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46f9d-219">0x00000000</span></span>                                  |
| <span data-ttu-id="46f9d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-220">System-Flags</span></span>           | <span data-ttu-id="46f9d-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="46f9d-221">0x08000014</span></span>                                  |
| <span data-ttu-id="46f9d-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46f9d-222">Classes used in</span></span>        | [<span data-ttu-id="46f9d-223">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="46f9d-223">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46f9d-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46f9d-224">Windows Server 2008</span></span>



| <span data-ttu-id="46f9d-225">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-225">Entry</span></span> | <span data-ttu-id="46f9d-226">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-226">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46f9d-227">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-228">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="46f9d-229">System-Only</span></span>            | <span data-ttu-id="46f9d-230">對</span><span class="sxs-lookup"><span data-stu-id="46f9d-230">True</span></span>                                        |
| <span data-ttu-id="46f9d-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46f9d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="46f9d-232">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-232">False</span></span>                                       |
| <span data-ttu-id="46f9d-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46f9d-233">Is Indexed</span></span>             | <span data-ttu-id="46f9d-234">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-234">False</span></span>                                       |
| <span data-ttu-id="46f9d-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46f9d-235">In Global Catalog</span></span>      | <span data-ttu-id="46f9d-236">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-236">False</span></span>                                       |
| <span data-ttu-id="46f9d-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46f9d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="46f9d-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46f9d-238">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="46f9d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46f9d-239">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46f9d-240">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-241">Search-Flags</span></span>           | <span data-ttu-id="46f9d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46f9d-242">0x00000000</span></span>                                  |
| <span data-ttu-id="46f9d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-243">System-Flags</span></span>           | <span data-ttu-id="46f9d-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="46f9d-244">0x08000014</span></span>                                  |
| <span data-ttu-id="46f9d-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46f9d-245">Classes used in</span></span>        | [<span data-ttu-id="46f9d-246">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="46f9d-246">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46f9d-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46f9d-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46f9d-248">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-248">Entry</span></span> | <span data-ttu-id="46f9d-249">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-249">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46f9d-250">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-251">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="46f9d-252">System-Only</span></span>            | <span data-ttu-id="46f9d-253">對</span><span class="sxs-lookup"><span data-stu-id="46f9d-253">True</span></span>                                        |
| <span data-ttu-id="46f9d-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46f9d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="46f9d-255">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-255">False</span></span>                                       |
| <span data-ttu-id="46f9d-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46f9d-256">Is Indexed</span></span>             | <span data-ttu-id="46f9d-257">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-257">False</span></span>                                       |
| <span data-ttu-id="46f9d-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46f9d-258">In Global Catalog</span></span>      | <span data-ttu-id="46f9d-259">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-259">False</span></span>                                       |
| <span data-ttu-id="46f9d-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46f9d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="46f9d-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46f9d-261">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="46f9d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46f9d-262">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46f9d-263">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-264">Search-Flags</span></span>           | <span data-ttu-id="46f9d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46f9d-265">0x00000000</span></span>                                  |
| <span data-ttu-id="46f9d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-266">System-Flags</span></span>           | <span data-ttu-id="46f9d-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="46f9d-267">0x08000014</span></span>                                  |
| <span data-ttu-id="46f9d-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46f9d-268">Classes used in</span></span>        | [<span data-ttu-id="46f9d-269">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="46f9d-269">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46f9d-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46f9d-270">Windows Server 2012</span></span>



| <span data-ttu-id="46f9d-271">進入</span><span class="sxs-lookup"><span data-stu-id="46f9d-271">Entry</span></span> | <span data-ttu-id="46f9d-272">值</span><span class="sxs-lookup"><span data-stu-id="46f9d-272">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="46f9d-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="46f9d-273">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46f9d-274">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="46f9d-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="46f9d-275">System-Only</span></span>            | <span data-ttu-id="46f9d-276">對</span><span class="sxs-lookup"><span data-stu-id="46f9d-276">True</span></span>                                        |
| <span data-ttu-id="46f9d-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="46f9d-277">Is-Single-Valued</span></span>       | <span data-ttu-id="46f9d-278">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-278">False</span></span>                                       |
| <span data-ttu-id="46f9d-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="46f9d-279">Is Indexed</span></span>             | <span data-ttu-id="46f9d-280">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-280">False</span></span>                                       |
| <span data-ttu-id="46f9d-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="46f9d-281">In Global Catalog</span></span>      | <span data-ttu-id="46f9d-282">否</span><span class="sxs-lookup"><span data-stu-id="46f9d-282">False</span></span>                                       |
| <span data-ttu-id="46f9d-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="46f9d-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="46f9d-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="46f9d-284">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="46f9d-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46f9d-285">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46f9d-286">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="46f9d-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-287">Search-Flags</span></span>           | <span data-ttu-id="46f9d-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46f9d-288">0x00000000</span></span>                                  |
| <span data-ttu-id="46f9d-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46f9d-289">System-Flags</span></span>           | <span data-ttu-id="46f9d-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="46f9d-290">0x08000014</span></span>                                  |
| <span data-ttu-id="46f9d-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="46f9d-291">Classes used in</span></span>        | [<span data-ttu-id="46f9d-292">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="46f9d-292">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





