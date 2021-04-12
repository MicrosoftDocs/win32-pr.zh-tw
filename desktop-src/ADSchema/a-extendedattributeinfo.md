---
title: 擴充屬性-Info 屬性
description: 多值屬性，其中包含代表每個屬性之其他資訊的字串。
ms.assetid: 38f87907-a328-473f-bc9c-f3573bc05af5
ms.tgt_platform: multiple
keywords:
- 擴充屬性資訊屬性 AD 架構
- extendedAttributeInfo 屬性 AD 架構
topic_type:
- apiref
api_name:
- Extended-Attribute-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2c5e1498716dfbac2a1c539f7c9a5bfb48fb41
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385353"
---
# <a name="extended-attribute-info-attribute"></a><span data-ttu-id="b7b88-105">擴充屬性-Info 屬性</span><span class="sxs-lookup"><span data-stu-id="b7b88-105">Extended-Attribute-Info attribute</span></span>

<span data-ttu-id="b7b88-106">多值屬性，其中包含代表每個屬性之其他資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="b7b88-106">A multi-valued property that contains strings that represent additional information for each attribute.</span></span>



| <span data-ttu-id="b7b88-107">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-107">Entry</span></span> | <span data-ttu-id="b7b88-108">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-109">CN</span><span class="sxs-lookup"><span data-stu-id="b7b88-109">CN</span></span>                | <span data-ttu-id="b7b88-110">擴充屬性資訊</span><span class="sxs-lookup"><span data-stu-id="b7b88-110">Extended-Attribute-Info</span></span>                     |
| <span data-ttu-id="b7b88-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b7b88-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b7b88-112">extendedAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="b7b88-112">extendedAttributeInfo</span></span>                       |
| <span data-ttu-id="b7b88-113">大小</span><span class="sxs-lookup"><span data-stu-id="b7b88-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="b7b88-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b7b88-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b7b88-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b7b88-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b7b88-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-116">Attribute-Id</span></span>      | <span data-ttu-id="b7b88-117">1.2.840.113556.1.4.909</span><span class="sxs-lookup"><span data-stu-id="b7b88-117">1.2.840.113556.1.4.909</span></span>                      |
| <span data-ttu-id="b7b88-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b7b88-118">System-Id-Guid</span></span>    | <span data-ttu-id="b7b88-119">9a7ad947-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b7b88-119">9a7ad947-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="b7b88-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b88-120">Syntax</span></span>            | [<span data-ttu-id="b7b88-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b7b88-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b7b88-122">實作</span><span class="sxs-lookup"><span data-stu-id="b7b88-122">Implementations</span></span>

-   [<span data-ttu-id="b7b88-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b7b88-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b7b88-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7b88-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7b88-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b7b88-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b7b88-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7b88-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7b88-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7b88-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7b88-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7b88-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7b88-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7b88-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b7b88-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7b88-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b7b88-131">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-131">Entry</span></span> | <span data-ttu-id="b7b88-132">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-132">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b7b88-133">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-134">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7b88-135">System-Only</span></span>            | <span data-ttu-id="b7b88-136">對</span><span class="sxs-lookup"><span data-stu-id="b7b88-136">True</span></span>                                        |
| <span data-ttu-id="b7b88-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b7b88-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b7b88-138">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-138">False</span></span>                                       |
| <span data-ttu-id="b7b88-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b7b88-139">Is Indexed</span></span>             | <span data-ttu-id="b7b88-140">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-140">False</span></span>                                       |
| <span data-ttu-id="b7b88-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b7b88-141">In Global Catalog</span></span>      | <span data-ttu-id="b7b88-142">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-142">False</span></span>                                       |
| <span data-ttu-id="b7b88-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b7b88-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7b88-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b7b88-144">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b7b88-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7b88-145">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7b88-146">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-147">Search-Flags</span></span>           | <span data-ttu-id="b7b88-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7b88-148">0x00000000</span></span>                                  |
| <span data-ttu-id="b7b88-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-149">System-Flags</span></span>           | <span data-ttu-id="b7b88-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b7b88-150">0x08000014</span></span>                                  |
| <span data-ttu-id="b7b88-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b7b88-151">Classes used in</span></span>        | [<span data-ttu-id="b7b88-152">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b7b88-152">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b7b88-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7b88-153">Windows Server 2003</span></span>



| <span data-ttu-id="b7b88-154">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-154">Entry</span></span> | <span data-ttu-id="b7b88-155">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-155">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b7b88-156">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-157">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7b88-158">System-Only</span></span>            | <span data-ttu-id="b7b88-159">對</span><span class="sxs-lookup"><span data-stu-id="b7b88-159">True</span></span>                                        |
| <span data-ttu-id="b7b88-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b7b88-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b7b88-161">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-161">False</span></span>                                       |
| <span data-ttu-id="b7b88-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b7b88-162">Is Indexed</span></span>             | <span data-ttu-id="b7b88-163">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-163">False</span></span>                                       |
| <span data-ttu-id="b7b88-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b7b88-164">In Global Catalog</span></span>      | <span data-ttu-id="b7b88-165">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-165">False</span></span>                                       |
| <span data-ttu-id="b7b88-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b7b88-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7b88-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b7b88-167">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b7b88-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7b88-168">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7b88-169">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-170">Search-Flags</span></span>           | <span data-ttu-id="b7b88-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7b88-171">0x00000000</span></span>                                  |
| <span data-ttu-id="b7b88-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-172">System-Flags</span></span>           | <span data-ttu-id="b7b88-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b7b88-173">0x08000014</span></span>                                  |
| <span data-ttu-id="b7b88-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b7b88-174">Classes used in</span></span>        | [<span data-ttu-id="b7b88-175">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b7b88-175">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b7b88-176">亞當</span><span class="sxs-lookup"><span data-stu-id="b7b88-176">ADAM</span></span>



| <span data-ttu-id="b7b88-177">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-177">Entry</span></span> | <span data-ttu-id="b7b88-178">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-178">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b7b88-179">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-180">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7b88-181">System-Only</span></span>            | <span data-ttu-id="b7b88-182">對</span><span class="sxs-lookup"><span data-stu-id="b7b88-182">True</span></span>                                        |
| <span data-ttu-id="b7b88-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b7b88-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b7b88-184">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-184">False</span></span>                                       |
| <span data-ttu-id="b7b88-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b7b88-185">Is Indexed</span></span>             | <span data-ttu-id="b7b88-186">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-186">False</span></span>                                       |
| <span data-ttu-id="b7b88-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b7b88-187">In Global Catalog</span></span>      | <span data-ttu-id="b7b88-188">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-188">False</span></span>                                       |
| <span data-ttu-id="b7b88-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b7b88-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7b88-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b7b88-190">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b7b88-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7b88-191">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7b88-192">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-193">Search-Flags</span></span>           | <span data-ttu-id="b7b88-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7b88-194">0x00000000</span></span>                                  |
| <span data-ttu-id="b7b88-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-195">System-Flags</span></span>           | <span data-ttu-id="b7b88-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b7b88-196">0x08000014</span></span>                                  |
| <span data-ttu-id="b7b88-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b7b88-197">Classes used in</span></span>        | [<span data-ttu-id="b7b88-198">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b7b88-198">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7b88-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7b88-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7b88-200">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-200">Entry</span></span> | <span data-ttu-id="b7b88-201">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-201">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b7b88-202">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-203">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7b88-204">System-Only</span></span>            | <span data-ttu-id="b7b88-205">對</span><span class="sxs-lookup"><span data-stu-id="b7b88-205">True</span></span>                                        |
| <span data-ttu-id="b7b88-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b7b88-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b7b88-207">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-207">False</span></span>                                       |
| <span data-ttu-id="b7b88-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b7b88-208">Is Indexed</span></span>             | <span data-ttu-id="b7b88-209">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-209">False</span></span>                                       |
| <span data-ttu-id="b7b88-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b7b88-210">In Global Catalog</span></span>      | <span data-ttu-id="b7b88-211">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-211">False</span></span>                                       |
| <span data-ttu-id="b7b88-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b7b88-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7b88-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b7b88-213">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b7b88-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7b88-214">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7b88-215">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-216">Search-Flags</span></span>           | <span data-ttu-id="b7b88-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7b88-217">0x00000000</span></span>                                  |
| <span data-ttu-id="b7b88-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-218">System-Flags</span></span>           | <span data-ttu-id="b7b88-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b7b88-219">0x08000014</span></span>                                  |
| <span data-ttu-id="b7b88-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b7b88-220">Classes used in</span></span>        | [<span data-ttu-id="b7b88-221">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b7b88-221">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7b88-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7b88-222">Windows Server 2008</span></span>



| <span data-ttu-id="b7b88-223">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-223">Entry</span></span> | <span data-ttu-id="b7b88-224">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-224">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b7b88-225">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-226">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7b88-227">System-Only</span></span>            | <span data-ttu-id="b7b88-228">對</span><span class="sxs-lookup"><span data-stu-id="b7b88-228">True</span></span>                                        |
| <span data-ttu-id="b7b88-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b7b88-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b7b88-230">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-230">False</span></span>                                       |
| <span data-ttu-id="b7b88-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b7b88-231">Is Indexed</span></span>             | <span data-ttu-id="b7b88-232">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-232">False</span></span>                                       |
| <span data-ttu-id="b7b88-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b7b88-233">In Global Catalog</span></span>      | <span data-ttu-id="b7b88-234">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-234">False</span></span>                                       |
| <span data-ttu-id="b7b88-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b7b88-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7b88-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b7b88-236">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b7b88-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7b88-237">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7b88-238">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-239">Search-Flags</span></span>           | <span data-ttu-id="b7b88-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7b88-240">0x00000000</span></span>                                  |
| <span data-ttu-id="b7b88-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-241">System-Flags</span></span>           | <span data-ttu-id="b7b88-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b7b88-242">0x08000014</span></span>                                  |
| <span data-ttu-id="b7b88-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b7b88-243">Classes used in</span></span>        | [<span data-ttu-id="b7b88-244">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b7b88-244">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7b88-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7b88-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7b88-246">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-246">Entry</span></span> | <span data-ttu-id="b7b88-247">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-247">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b7b88-248">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-249">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7b88-250">System-Only</span></span>            | <span data-ttu-id="b7b88-251">對</span><span class="sxs-lookup"><span data-stu-id="b7b88-251">True</span></span>                                        |
| <span data-ttu-id="b7b88-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b7b88-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b7b88-253">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-253">False</span></span>                                       |
| <span data-ttu-id="b7b88-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b7b88-254">Is Indexed</span></span>             | <span data-ttu-id="b7b88-255">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-255">False</span></span>                                       |
| <span data-ttu-id="b7b88-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b7b88-256">In Global Catalog</span></span>      | <span data-ttu-id="b7b88-257">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-257">False</span></span>                                       |
| <span data-ttu-id="b7b88-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b7b88-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7b88-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b7b88-259">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b7b88-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7b88-260">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7b88-261">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-262">Search-Flags</span></span>           | <span data-ttu-id="b7b88-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7b88-263">0x00000000</span></span>                                  |
| <span data-ttu-id="b7b88-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-264">System-Flags</span></span>           | <span data-ttu-id="b7b88-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b7b88-265">0x08000014</span></span>                                  |
| <span data-ttu-id="b7b88-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b7b88-266">Classes used in</span></span>        | [<span data-ttu-id="b7b88-267">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b7b88-267">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7b88-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7b88-268">Windows Server 2012</span></span>



| <span data-ttu-id="b7b88-269">進入</span><span class="sxs-lookup"><span data-stu-id="b7b88-269">Entry</span></span> | <span data-ttu-id="b7b88-270">值</span><span class="sxs-lookup"><span data-stu-id="b7b88-270">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7b88-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b7b88-271">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7b88-272">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b7b88-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7b88-273">System-Only</span></span>            | <span data-ttu-id="b7b88-274">對</span><span class="sxs-lookup"><span data-stu-id="b7b88-274">True</span></span>                                        |
| <span data-ttu-id="b7b88-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b7b88-275">Is-Single-Valued</span></span>       | <span data-ttu-id="b7b88-276">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-276">False</span></span>                                       |
| <span data-ttu-id="b7b88-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b7b88-277">Is Indexed</span></span>             | <span data-ttu-id="b7b88-278">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-278">False</span></span>                                       |
| <span data-ttu-id="b7b88-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b7b88-279">In Global Catalog</span></span>      | <span data-ttu-id="b7b88-280">否</span><span class="sxs-lookup"><span data-stu-id="b7b88-280">False</span></span>                                       |
| <span data-ttu-id="b7b88-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b7b88-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7b88-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b7b88-282">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b7b88-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7b88-283">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7b88-284">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b7b88-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-285">Search-Flags</span></span>           | <span data-ttu-id="b7b88-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7b88-286">0x00000000</span></span>                                  |
| <span data-ttu-id="b7b88-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7b88-287">System-Flags</span></span>           | <span data-ttu-id="b7b88-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b7b88-288">0x08000014</span></span>                                  |
| <span data-ttu-id="b7b88-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b7b88-289">Classes used in</span></span>        | [<span data-ttu-id="b7b88-290">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="b7b88-290">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





