---
title: 縮寫屬性
description: 包含使用者全名部分的縮寫。 這可以用來做為 Windows 通訊錄中的初始初始部分。
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- 縮寫屬性 AD 架構
- 縮寫屬性 AD 架構
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970864"
---
# <a name="initials-attribute"></a><span data-ttu-id="c9ee5-106">縮寫屬性</span><span class="sxs-lookup"><span data-stu-id="c9ee5-106">Initials attribute</span></span>

<span data-ttu-id="c9ee5-107">包含使用者全名部分的縮寫。</span><span class="sxs-lookup"><span data-stu-id="c9ee5-107">Contains the initials for parts of the user's full name.</span></span> <span data-ttu-id="c9ee5-108">這可以用來做為 Windows 通訊錄中的初始初始部分。</span><span class="sxs-lookup"><span data-stu-id="c9ee5-108">This may be used as the middle initial in the Windows Address Book.</span></span>



| <span data-ttu-id="c9ee5-109">進入</span><span class="sxs-lookup"><span data-stu-id="c9ee5-109">Entry</span></span> | <span data-ttu-id="c9ee5-110">值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c9ee5-111">CN</span><span class="sxs-lookup"><span data-stu-id="c9ee5-111">CN</span></span>                | <span data-ttu-id="c9ee5-112">縮寫</span><span class="sxs-lookup"><span data-stu-id="c9ee5-112">Initials</span></span>                                    |
| <span data-ttu-id="c9ee5-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c9ee5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c9ee5-114">Initials</span><span class="sxs-lookup"><span data-stu-id="c9ee5-114">initials</span></span>                                    |
| <span data-ttu-id="c9ee5-115">大小</span><span class="sxs-lookup"><span data-stu-id="c9ee5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="c9ee5-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c9ee5-116">Update Privilege</span></span>  | <span data-ttu-id="c9ee5-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="c9ee5-117">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="c9ee5-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c9ee5-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c9ee5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee5-119">Attribute-Id</span></span>      | <span data-ttu-id="c9ee5-120">2.5.4.43</span><span class="sxs-lookup"><span data-stu-id="c9ee5-120">2.5.4.43</span></span>                                    |
| <span data-ttu-id="c9ee5-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c9ee5-121">System-Id-Guid</span></span>    | <span data-ttu-id="c9ee5-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="c9ee5-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="c9ee5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9ee5-123">Syntax</span></span>            | [<span data-ttu-id="c9ee5-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c9ee5-125">實作</span><span class="sxs-lookup"><span data-stu-id="c9ee5-125">Implementations</span></span>

-   [<span data-ttu-id="c9ee5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9ee5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9ee5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9ee5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9ee5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9ee5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9ee5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9ee5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c9ee5-133">進入</span><span class="sxs-lookup"><span data-stu-id="c9ee5-133">Entry</span></span> | <span data-ttu-id="c9ee5-134">值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c9ee5-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9ee5-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="c9ee5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee5-136">MAPI-Id</span></span>                | <span data-ttu-id="c9ee5-137">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="c9ee5-137">0x3A0A</span></span>                                                             |
| <span data-ttu-id="c9ee5-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee5-138">System-Only</span></span>            | <span data-ttu-id="c9ee5-139">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-139">False</span></span>                                                              |
| <span data-ttu-id="c9ee5-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee5-141">對</span><span class="sxs-lookup"><span data-stu-id="c9ee5-141">True</span></span>                                                               |
| <span data-ttu-id="c9ee5-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9ee5-142">Is Indexed</span></span>             | <span data-ttu-id="c9ee5-143">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-143">False</span></span>                                                              |
| <span data-ttu-id="c9ee5-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9ee5-144">In Global Catalog</span></span>      | <span data-ttu-id="c9ee5-145">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-145">False</span></span>                                                              |
| <span data-ttu-id="c9ee5-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9ee5-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee5-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9ee5-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="c9ee5-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee5-148">Range-Lower</span></span>            | <span data-ttu-id="c9ee5-149">1</span><span class="sxs-lookup"><span data-stu-id="c9ee5-149">1</span></span>                                                                  |
| <span data-ttu-id="c9ee5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee5-150">Range-Upper</span></span>            | <span data-ttu-id="c9ee5-151">6</span><span class="sxs-lookup"><span data-stu-id="c9ee5-151">6</span></span>                                                                  |
| <span data-ttu-id="c9ee5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-152">Search-Flags</span></span>           | <span data-ttu-id="c9ee5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee5-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="c9ee5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-154">System-Flags</span></span>           | <span data-ttu-id="c9ee5-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee5-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="c9ee5-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9ee5-156">Classes used in</span></span>        | [<span data-ttu-id="c9ee5-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9ee5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9ee5-158">Windows Server 2003</span></span>



| <span data-ttu-id="c9ee5-159">進入</span><span class="sxs-lookup"><span data-stu-id="c9ee5-159">Entry</span></span> | <span data-ttu-id="c9ee5-160">值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ee5-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9ee5-161">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="c9ee5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee5-162">MAPI-Id</span></span>                | <span data-ttu-id="c9ee5-163">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="c9ee5-163">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="c9ee5-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee5-164">System-Only</span></span>            | <span data-ttu-id="c9ee5-165">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-165">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee5-167">對</span><span class="sxs-lookup"><span data-stu-id="c9ee5-167">True</span></span>                                                                                                                   |
| <span data-ttu-id="c9ee5-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9ee5-168">Is Indexed</span></span>             | <span data-ttu-id="c9ee5-169">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-169">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9ee5-170">In Global Catalog</span></span>      | <span data-ttu-id="c9ee5-171">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-171">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9ee5-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee5-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9ee5-173">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="c9ee5-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee5-174">Range-Lower</span></span>            | <span data-ttu-id="c9ee5-175">1</span><span class="sxs-lookup"><span data-stu-id="c9ee5-175">1</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee5-176">Range-Upper</span></span>            | <span data-ttu-id="c9ee5-177">6</span><span class="sxs-lookup"><span data-stu-id="c9ee5-177">6</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-178">Search-Flags</span></span>           | <span data-ttu-id="c9ee5-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee5-179">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-180">System-Flags</span></span>           | <span data-ttu-id="c9ee5-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee5-181">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9ee5-182">Classes used in</span></span>        | [<span data-ttu-id="c9ee5-183">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-183">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="c9ee5-184">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-184">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9ee5-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9ee5-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9ee5-186">進入</span><span class="sxs-lookup"><span data-stu-id="c9ee5-186">Entry</span></span> | <span data-ttu-id="c9ee5-187">值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-187">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ee5-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9ee5-188">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="c9ee5-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee5-189">MAPI-Id</span></span>                | <span data-ttu-id="c9ee5-190">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="c9ee5-190">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="c9ee5-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee5-191">System-Only</span></span>            | <span data-ttu-id="c9ee5-192">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-193">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee5-194">對</span><span class="sxs-lookup"><span data-stu-id="c9ee5-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="c9ee5-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9ee5-195">Is Indexed</span></span>             | <span data-ttu-id="c9ee5-196">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9ee5-197">In Global Catalog</span></span>      | <span data-ttu-id="c9ee5-198">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-198">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9ee5-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee5-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9ee5-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="c9ee5-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee5-201">Range-Lower</span></span>            | <span data-ttu-id="c9ee5-202">1</span><span class="sxs-lookup"><span data-stu-id="c9ee5-202">1</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee5-203">Range-Upper</span></span>            | <span data-ttu-id="c9ee5-204">6</span><span class="sxs-lookup"><span data-stu-id="c9ee5-204">6</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-205">Search-Flags</span></span>           | <span data-ttu-id="c9ee5-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee5-206">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-207">System-Flags</span></span>           | <span data-ttu-id="c9ee5-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee5-208">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9ee5-209">Classes used in</span></span>        | [<span data-ttu-id="c9ee5-210">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-210">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="c9ee5-211">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-211">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9ee5-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9ee5-212">Windows Server 2008</span></span>



| <span data-ttu-id="c9ee5-213">進入</span><span class="sxs-lookup"><span data-stu-id="c9ee5-213">Entry</span></span> | <span data-ttu-id="c9ee5-214">值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-214">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ee5-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9ee5-215">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="c9ee5-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee5-216">MAPI-Id</span></span>                | <span data-ttu-id="c9ee5-217">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="c9ee5-217">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="c9ee5-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee5-218">System-Only</span></span>            | <span data-ttu-id="c9ee5-219">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-219">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-220">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee5-221">對</span><span class="sxs-lookup"><span data-stu-id="c9ee5-221">True</span></span>                                                                                                                   |
| <span data-ttu-id="c9ee5-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9ee5-222">Is Indexed</span></span>             | <span data-ttu-id="c9ee5-223">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-223">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9ee5-224">In Global Catalog</span></span>      | <span data-ttu-id="c9ee5-225">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-225">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9ee5-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee5-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9ee5-227">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="c9ee5-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee5-228">Range-Lower</span></span>            | <span data-ttu-id="c9ee5-229">1</span><span class="sxs-lookup"><span data-stu-id="c9ee5-229">1</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee5-230">Range-Upper</span></span>            | <span data-ttu-id="c9ee5-231">6</span><span class="sxs-lookup"><span data-stu-id="c9ee5-231">6</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-232">Search-Flags</span></span>           | <span data-ttu-id="c9ee5-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee5-233">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-234">System-Flags</span></span>           | <span data-ttu-id="c9ee5-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee5-235">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9ee5-236">Classes used in</span></span>        | [<span data-ttu-id="c9ee5-237">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-237">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="c9ee5-238">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-238">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9ee5-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9ee5-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9ee5-240">進入</span><span class="sxs-lookup"><span data-stu-id="c9ee5-240">Entry</span></span> | <span data-ttu-id="c9ee5-241">值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-241">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ee5-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9ee5-242">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="c9ee5-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee5-243">MAPI-Id</span></span>                | <span data-ttu-id="c9ee5-244">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="c9ee5-244">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="c9ee5-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee5-245">System-Only</span></span>            | <span data-ttu-id="c9ee5-246">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-246">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-247">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-247">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee5-248">對</span><span class="sxs-lookup"><span data-stu-id="c9ee5-248">True</span></span>                                                                                                                   |
| <span data-ttu-id="c9ee5-249">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9ee5-249">Is Indexed</span></span>             | <span data-ttu-id="c9ee5-250">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-250">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-251">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9ee5-251">In Global Catalog</span></span>      | <span data-ttu-id="c9ee5-252">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-252">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-253">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9ee5-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee5-254">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9ee5-254">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="c9ee5-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee5-255">Range-Lower</span></span>            | <span data-ttu-id="c9ee5-256">1</span><span class="sxs-lookup"><span data-stu-id="c9ee5-256">1</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee5-257">Range-Upper</span></span>            | <span data-ttu-id="c9ee5-258">6</span><span class="sxs-lookup"><span data-stu-id="c9ee5-258">6</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-259">Search-Flags</span></span>           | <span data-ttu-id="c9ee5-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee5-260">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-261">System-Flags</span></span>           | <span data-ttu-id="c9ee5-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee5-262">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9ee5-263">Classes used in</span></span>        | [<span data-ttu-id="c9ee5-264">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-264">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="c9ee5-265">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-265">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9ee5-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9ee5-266">Windows Server 2012</span></span>



| <span data-ttu-id="c9ee5-267">進入</span><span class="sxs-lookup"><span data-stu-id="c9ee5-267">Entry</span></span> | <span data-ttu-id="c9ee5-268">值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-268">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ee5-269">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c9ee5-269">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="c9ee5-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9ee5-270">MAPI-Id</span></span>                | <span data-ttu-id="c9ee5-271">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="c9ee5-271">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="c9ee5-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9ee5-272">System-Only</span></span>            | <span data-ttu-id="c9ee5-273">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-273">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c9ee5-274">Is-Single-Valued</span></span>       | <span data-ttu-id="c9ee5-275">對</span><span class="sxs-lookup"><span data-stu-id="c9ee5-275">True</span></span>                                                                                                                   |
| <span data-ttu-id="c9ee5-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c9ee5-276">Is Indexed</span></span>             | <span data-ttu-id="c9ee5-277">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-277">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c9ee5-278">In Global Catalog</span></span>      | <span data-ttu-id="c9ee5-279">否</span><span class="sxs-lookup"><span data-stu-id="c9ee5-279">False</span></span>                                                                                                                  |
| <span data-ttu-id="c9ee5-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c9ee5-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9ee5-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c9ee5-281">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="c9ee5-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9ee5-282">Range-Lower</span></span>            | <span data-ttu-id="c9ee5-283">1</span><span class="sxs-lookup"><span data-stu-id="c9ee5-283">1</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9ee5-284">Range-Upper</span></span>            | <span data-ttu-id="c9ee5-285">6</span><span class="sxs-lookup"><span data-stu-id="c9ee5-285">6</span></span>                                                                                                                      |
| <span data-ttu-id="c9ee5-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-286">Search-Flags</span></span>           | <span data-ttu-id="c9ee5-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9ee5-287">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9ee5-288">System-Flags</span></span>           | <span data-ttu-id="c9ee5-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9ee5-289">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="c9ee5-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c9ee5-290">Classes used in</span></span>        | [<span data-ttu-id="c9ee5-291">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-291">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="c9ee5-292">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="c9ee5-292">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





