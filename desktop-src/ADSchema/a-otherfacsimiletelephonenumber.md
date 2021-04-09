---
title: 電話-傳真-其他屬性
description: 替代傳真號碼的清單。
ms.assetid: b5e4ef38-ce91-4943-bad5-c299f83387d3
ms.tgt_platform: multiple
keywords:
- 電話-傳真-其他屬性 AD 架構
- otherFacsimileTelephoneNumber 屬性 AD 架構
topic_type:
- apiref
api_name:
- Phone-Fax-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12e765ce2c3f9b74b894714b99ae87deadd760d6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845363"
---
# <a name="phone-fax-other-attribute"></a><span data-ttu-id="548eb-105">電話-傳真-其他屬性</span><span class="sxs-lookup"><span data-stu-id="548eb-105">Phone-Fax-Other attribute</span></span>

<span data-ttu-id="548eb-106">替代傳真號碼的清單。</span><span class="sxs-lookup"><span data-stu-id="548eb-106">A list of alternate facsimile numbers.</span></span>



| <span data-ttu-id="548eb-107">進入</span><span class="sxs-lookup"><span data-stu-id="548eb-107">Entry</span></span> | <span data-ttu-id="548eb-108">值</span><span class="sxs-lookup"><span data-stu-id="548eb-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="548eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="548eb-109">CN</span></span>                | <span data-ttu-id="548eb-110">電話-傳真-其他</span><span class="sxs-lookup"><span data-stu-id="548eb-110">Phone-Fax-Other</span></span>                                                                  |
| <span data-ttu-id="548eb-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="548eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="548eb-112">otherFacsimileTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="548eb-112">otherFacsimileTelephoneNumber</span></span>                                                    |
| <span data-ttu-id="548eb-113">大小</span><span class="sxs-lookup"><span data-stu-id="548eb-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="548eb-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="548eb-114">Update Privilege</span></span>  | <span data-ttu-id="548eb-115">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="548eb-115">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="548eb-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="548eb-116">Update Frequency</span></span>  | <span data-ttu-id="548eb-117">當使用者的記錄建立時，以及每次電話號碼需要變更時。</span><span class="sxs-lookup"><span data-stu-id="548eb-117">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="548eb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="548eb-118">Attribute-Id</span></span>      | <span data-ttu-id="548eb-119">1.2.840.113556.1.4.646</span><span class="sxs-lookup"><span data-stu-id="548eb-119">1.2.840.113556.1.4.646</span></span>                                                           |
| <span data-ttu-id="548eb-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="548eb-120">System-Id-Guid</span></span>    | <span data-ttu-id="548eb-121">0296c11d-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="548eb-121">0296c11d-40da-11d1-a9c0-0000f80367c1</span></span>                                             |
| <span data-ttu-id="548eb-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="548eb-122">Syntax</span></span>            | [<span data-ttu-id="548eb-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="548eb-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="548eb-124">實作</span><span class="sxs-lookup"><span data-stu-id="548eb-124">Implementations</span></span>

-   [<span data-ttu-id="548eb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="548eb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="548eb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="548eb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="548eb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="548eb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="548eb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="548eb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="548eb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="548eb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="548eb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="548eb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="548eb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="548eb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="548eb-132">進入</span><span class="sxs-lookup"><span data-stu-id="548eb-132">Entry</span></span> | <span data-ttu-id="548eb-133">值</span><span class="sxs-lookup"><span data-stu-id="548eb-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="548eb-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548eb-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548eb-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="548eb-136">System-Only</span></span>            | <span data-ttu-id="548eb-137">否</span><span class="sxs-lookup"><span data-stu-id="548eb-137">False</span></span>                                                              |
| <span data-ttu-id="548eb-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548eb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="548eb-139">否</span><span class="sxs-lookup"><span data-stu-id="548eb-139">False</span></span>                                                              |
| <span data-ttu-id="548eb-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548eb-140">Is Indexed</span></span>             | <span data-ttu-id="548eb-141">否</span><span class="sxs-lookup"><span data-stu-id="548eb-141">False</span></span>                                                              |
| <span data-ttu-id="548eb-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548eb-142">In Global Catalog</span></span>      | <span data-ttu-id="548eb-143">否</span><span class="sxs-lookup"><span data-stu-id="548eb-143">False</span></span>                                                              |
| <span data-ttu-id="548eb-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548eb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="548eb-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548eb-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="548eb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548eb-146">Range-Lower</span></span>            | <span data-ttu-id="548eb-147">1</span><span class="sxs-lookup"><span data-stu-id="548eb-147">1</span></span>                                                                  |
| <span data-ttu-id="548eb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548eb-148">Range-Upper</span></span>            | <span data-ttu-id="548eb-149">64</span><span class="sxs-lookup"><span data-stu-id="548eb-149">64</span></span>                                                                 |
| <span data-ttu-id="548eb-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-150">Search-Flags</span></span>           | <span data-ttu-id="548eb-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548eb-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="548eb-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-152">System-Flags</span></span>           | <span data-ttu-id="548eb-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548eb-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="548eb-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548eb-154">Classes used in</span></span>        | [<span data-ttu-id="548eb-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="548eb-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="548eb-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="548eb-156">Windows Server 2003</span></span>



| <span data-ttu-id="548eb-157">進入</span><span class="sxs-lookup"><span data-stu-id="548eb-157">Entry</span></span> | <span data-ttu-id="548eb-158">值</span><span class="sxs-lookup"><span data-stu-id="548eb-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="548eb-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548eb-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548eb-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="548eb-161">System-Only</span></span>            | <span data-ttu-id="548eb-162">否</span><span class="sxs-lookup"><span data-stu-id="548eb-162">False</span></span>                                                              |
| <span data-ttu-id="548eb-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548eb-163">Is-Single-Valued</span></span>       | <span data-ttu-id="548eb-164">否</span><span class="sxs-lookup"><span data-stu-id="548eb-164">False</span></span>                                                              |
| <span data-ttu-id="548eb-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548eb-165">Is Indexed</span></span>             | <span data-ttu-id="548eb-166">否</span><span class="sxs-lookup"><span data-stu-id="548eb-166">False</span></span>                                                              |
| <span data-ttu-id="548eb-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548eb-167">In Global Catalog</span></span>      | <span data-ttu-id="548eb-168">否</span><span class="sxs-lookup"><span data-stu-id="548eb-168">False</span></span>                                                              |
| <span data-ttu-id="548eb-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548eb-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="548eb-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548eb-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="548eb-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548eb-171">Range-Lower</span></span>            | <span data-ttu-id="548eb-172">1</span><span class="sxs-lookup"><span data-stu-id="548eb-172">1</span></span>                                                                  |
| <span data-ttu-id="548eb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548eb-173">Range-Upper</span></span>            | <span data-ttu-id="548eb-174">64</span><span class="sxs-lookup"><span data-stu-id="548eb-174">64</span></span>                                                                 |
| <span data-ttu-id="548eb-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-175">Search-Flags</span></span>           | <span data-ttu-id="548eb-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548eb-176">0x00000000</span></span>                                                         |
| <span data-ttu-id="548eb-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-177">System-Flags</span></span>           | <span data-ttu-id="548eb-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548eb-178">0x00000010</span></span>                                                         |
| <span data-ttu-id="548eb-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548eb-179">Classes used in</span></span>        | [<span data-ttu-id="548eb-180">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="548eb-180">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="548eb-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="548eb-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="548eb-182">進入</span><span class="sxs-lookup"><span data-stu-id="548eb-182">Entry</span></span> | <span data-ttu-id="548eb-183">值</span><span class="sxs-lookup"><span data-stu-id="548eb-183">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="548eb-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548eb-184">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548eb-185">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="548eb-186">System-Only</span></span>            | <span data-ttu-id="548eb-187">否</span><span class="sxs-lookup"><span data-stu-id="548eb-187">False</span></span>                                                              |
| <span data-ttu-id="548eb-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548eb-188">Is-Single-Valued</span></span>       | <span data-ttu-id="548eb-189">否</span><span class="sxs-lookup"><span data-stu-id="548eb-189">False</span></span>                                                              |
| <span data-ttu-id="548eb-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548eb-190">Is Indexed</span></span>             | <span data-ttu-id="548eb-191">否</span><span class="sxs-lookup"><span data-stu-id="548eb-191">False</span></span>                                                              |
| <span data-ttu-id="548eb-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548eb-192">In Global Catalog</span></span>      | <span data-ttu-id="548eb-193">否</span><span class="sxs-lookup"><span data-stu-id="548eb-193">False</span></span>                                                              |
| <span data-ttu-id="548eb-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548eb-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="548eb-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548eb-195">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="548eb-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548eb-196">Range-Lower</span></span>            | <span data-ttu-id="548eb-197">1</span><span class="sxs-lookup"><span data-stu-id="548eb-197">1</span></span>                                                                  |
| <span data-ttu-id="548eb-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548eb-198">Range-Upper</span></span>            | <span data-ttu-id="548eb-199">64</span><span class="sxs-lookup"><span data-stu-id="548eb-199">64</span></span>                                                                 |
| <span data-ttu-id="548eb-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-200">Search-Flags</span></span>           | <span data-ttu-id="548eb-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548eb-201">0x00000000</span></span>                                                         |
| <span data-ttu-id="548eb-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-202">System-Flags</span></span>           | <span data-ttu-id="548eb-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548eb-203">0x00000010</span></span>                                                         |
| <span data-ttu-id="548eb-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548eb-204">Classes used in</span></span>        | [<span data-ttu-id="548eb-205">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="548eb-205">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="548eb-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="548eb-206">Windows Server 2008</span></span>



| <span data-ttu-id="548eb-207">進入</span><span class="sxs-lookup"><span data-stu-id="548eb-207">Entry</span></span> | <span data-ttu-id="548eb-208">值</span><span class="sxs-lookup"><span data-stu-id="548eb-208">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="548eb-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548eb-209">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548eb-210">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="548eb-211">System-Only</span></span>            | <span data-ttu-id="548eb-212">否</span><span class="sxs-lookup"><span data-stu-id="548eb-212">False</span></span>                                                              |
| <span data-ttu-id="548eb-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548eb-213">Is-Single-Valued</span></span>       | <span data-ttu-id="548eb-214">否</span><span class="sxs-lookup"><span data-stu-id="548eb-214">False</span></span>                                                              |
| <span data-ttu-id="548eb-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548eb-215">Is Indexed</span></span>             | <span data-ttu-id="548eb-216">否</span><span class="sxs-lookup"><span data-stu-id="548eb-216">False</span></span>                                                              |
| <span data-ttu-id="548eb-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548eb-217">In Global Catalog</span></span>      | <span data-ttu-id="548eb-218">否</span><span class="sxs-lookup"><span data-stu-id="548eb-218">False</span></span>                                                              |
| <span data-ttu-id="548eb-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548eb-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="548eb-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548eb-220">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="548eb-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548eb-221">Range-Lower</span></span>            | <span data-ttu-id="548eb-222">1</span><span class="sxs-lookup"><span data-stu-id="548eb-222">1</span></span>                                                                  |
| <span data-ttu-id="548eb-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548eb-223">Range-Upper</span></span>            | <span data-ttu-id="548eb-224">64</span><span class="sxs-lookup"><span data-stu-id="548eb-224">64</span></span>                                                                 |
| <span data-ttu-id="548eb-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-225">Search-Flags</span></span>           | <span data-ttu-id="548eb-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548eb-226">0x00000000</span></span>                                                         |
| <span data-ttu-id="548eb-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-227">System-Flags</span></span>           | <span data-ttu-id="548eb-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548eb-228">0x00000010</span></span>                                                         |
| <span data-ttu-id="548eb-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548eb-229">Classes used in</span></span>        | [<span data-ttu-id="548eb-230">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="548eb-230">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="548eb-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="548eb-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="548eb-232">進入</span><span class="sxs-lookup"><span data-stu-id="548eb-232">Entry</span></span> | <span data-ttu-id="548eb-233">值</span><span class="sxs-lookup"><span data-stu-id="548eb-233">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="548eb-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548eb-234">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548eb-235">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="548eb-236">System-Only</span></span>            | <span data-ttu-id="548eb-237">否</span><span class="sxs-lookup"><span data-stu-id="548eb-237">False</span></span>                                                              |
| <span data-ttu-id="548eb-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548eb-238">Is-Single-Valued</span></span>       | <span data-ttu-id="548eb-239">否</span><span class="sxs-lookup"><span data-stu-id="548eb-239">False</span></span>                                                              |
| <span data-ttu-id="548eb-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548eb-240">Is Indexed</span></span>             | <span data-ttu-id="548eb-241">否</span><span class="sxs-lookup"><span data-stu-id="548eb-241">False</span></span>                                                              |
| <span data-ttu-id="548eb-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548eb-242">In Global Catalog</span></span>      | <span data-ttu-id="548eb-243">否</span><span class="sxs-lookup"><span data-stu-id="548eb-243">False</span></span>                                                              |
| <span data-ttu-id="548eb-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548eb-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="548eb-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548eb-245">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="548eb-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548eb-246">Range-Lower</span></span>            | <span data-ttu-id="548eb-247">1</span><span class="sxs-lookup"><span data-stu-id="548eb-247">1</span></span>                                                                  |
| <span data-ttu-id="548eb-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548eb-248">Range-Upper</span></span>            | <span data-ttu-id="548eb-249">64</span><span class="sxs-lookup"><span data-stu-id="548eb-249">64</span></span>                                                                 |
| <span data-ttu-id="548eb-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-250">Search-Flags</span></span>           | <span data-ttu-id="548eb-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548eb-251">0x00000000</span></span>                                                         |
| <span data-ttu-id="548eb-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-252">System-Flags</span></span>           | <span data-ttu-id="548eb-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548eb-253">0x00000010</span></span>                                                         |
| <span data-ttu-id="548eb-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548eb-254">Classes used in</span></span>        | [<span data-ttu-id="548eb-255">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="548eb-255">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="548eb-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="548eb-256">Windows Server 2012</span></span>



| <span data-ttu-id="548eb-257">進入</span><span class="sxs-lookup"><span data-stu-id="548eb-257">Entry</span></span> | <span data-ttu-id="548eb-258">值</span><span class="sxs-lookup"><span data-stu-id="548eb-258">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="548eb-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548eb-259">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548eb-260">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="548eb-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="548eb-261">System-Only</span></span>            | <span data-ttu-id="548eb-262">否</span><span class="sxs-lookup"><span data-stu-id="548eb-262">False</span></span>                                                              |
| <span data-ttu-id="548eb-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548eb-263">Is-Single-Valued</span></span>       | <span data-ttu-id="548eb-264">否</span><span class="sxs-lookup"><span data-stu-id="548eb-264">False</span></span>                                                              |
| <span data-ttu-id="548eb-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548eb-265">Is Indexed</span></span>             | <span data-ttu-id="548eb-266">否</span><span class="sxs-lookup"><span data-stu-id="548eb-266">False</span></span>                                                              |
| <span data-ttu-id="548eb-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548eb-267">In Global Catalog</span></span>      | <span data-ttu-id="548eb-268">否</span><span class="sxs-lookup"><span data-stu-id="548eb-268">False</span></span>                                                              |
| <span data-ttu-id="548eb-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548eb-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="548eb-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548eb-270">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="548eb-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548eb-271">Range-Lower</span></span>            | <span data-ttu-id="548eb-272">1</span><span class="sxs-lookup"><span data-stu-id="548eb-272">1</span></span>                                                                  |
| <span data-ttu-id="548eb-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548eb-273">Range-Upper</span></span>            | <span data-ttu-id="548eb-274">64</span><span class="sxs-lookup"><span data-stu-id="548eb-274">64</span></span>                                                                 |
| <span data-ttu-id="548eb-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-275">Search-Flags</span></span>           | <span data-ttu-id="548eb-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548eb-276">0x00000000</span></span>                                                         |
| <span data-ttu-id="548eb-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548eb-277">System-Flags</span></span>           | <span data-ttu-id="548eb-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548eb-278">0x00000010</span></span>                                                         |
| <span data-ttu-id="548eb-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548eb-279">Classes used in</span></span>        | [<span data-ttu-id="548eb-280">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="548eb-280">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





