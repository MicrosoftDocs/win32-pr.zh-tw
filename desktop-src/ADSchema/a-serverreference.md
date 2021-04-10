---
title: Server-Reference 屬性
description: 在網站電腦物件中找到。 包含網域命名內容中網域控制站的分辨名稱。
ms.assetid: 6c0ebe85-b4ed-4284-ad96-0b711d5acce7
ms.tgt_platform: multiple
keywords:
- Server-Reference 屬性 AD 架構
- serverReference 屬性 AD 架構
topic_type:
- apiref
api_name:
- Server-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83fed3b44feeaccb87cb1f55435bbac915c1c262
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845304"
---
# <a name="server-reference-attribute"></a><span data-ttu-id="a3816-106">Server-Reference 屬性</span><span class="sxs-lookup"><span data-stu-id="a3816-106">Server-Reference attribute</span></span>

<span data-ttu-id="a3816-107">在網站電腦物件中找到。</span><span class="sxs-lookup"><span data-stu-id="a3816-107">Found in a site computer object.</span></span> <span data-ttu-id="a3816-108">包含網域命名內容中網域控制站的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="a3816-108">Contains the distinguished name of the domain controller in the domain naming context.</span></span>



| <span data-ttu-id="a3816-109">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-109">Entry</span></span> | <span data-ttu-id="a3816-110">值</span><span class="sxs-lookup"><span data-stu-id="a3816-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a3816-111">CN</span><span class="sxs-lookup"><span data-stu-id="a3816-111">CN</span></span>                | <span data-ttu-id="a3816-112">Server-Reference</span><span class="sxs-lookup"><span data-stu-id="a3816-112">Server-Reference</span></span>                        |
| <span data-ttu-id="a3816-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a3816-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a3816-114">serverReference</span><span class="sxs-lookup"><span data-stu-id="a3816-114">serverReference</span></span>                         |
| <span data-ttu-id="a3816-115">大小</span><span class="sxs-lookup"><span data-stu-id="a3816-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="a3816-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a3816-116">Update Privilege</span></span>  | <span data-ttu-id="a3816-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a3816-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="a3816-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a3816-118">Update Frequency</span></span>  | <span data-ttu-id="a3816-119">每次建立網站時。</span><span class="sxs-lookup"><span data-stu-id="a3816-119">Whenever a site is created.</span></span>             |
| <span data-ttu-id="a3816-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-120">Attribute-Id</span></span>      | <span data-ttu-id="a3816-121">1.2.840.113556.1.4.515</span><span class="sxs-lookup"><span data-stu-id="a3816-121">1.2.840.113556.1.4.515</span></span>                  |
| <span data-ttu-id="a3816-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a3816-122">System-Id-Guid</span></span>    | <span data-ttu-id="a3816-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a3816-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="a3816-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3816-124">Syntax</span></span>            | [<span data-ttu-id="a3816-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a3816-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a3816-126">實作</span><span class="sxs-lookup"><span data-stu-id="a3816-126">Implementations</span></span>

-   [<span data-ttu-id="a3816-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a3816-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a3816-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3816-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3816-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a3816-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a3816-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3816-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3816-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3816-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3816-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3816-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3816-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3816-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a3816-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3816-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a3816-135">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-135">Entry</span></span> | <span data-ttu-id="a3816-136">值</span><span class="sxs-lookup"><span data-stu-id="a3816-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3816-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3816-137">Link-Id</span></span>                | <span data-ttu-id="a3816-138">94</span><span class="sxs-lookup"><span data-stu-id="a3816-138">94</span></span>                                                                                                                              |
| <span data-ttu-id="a3816-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-139">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="a3816-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3816-140">System-Only</span></span>            | <span data-ttu-id="a3816-141">否</span><span class="sxs-lookup"><span data-stu-id="a3816-141">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3816-142">Is-Single-Valued</span></span>       | <span data-ttu-id="a3816-143">對</span><span class="sxs-lookup"><span data-stu-id="a3816-143">True</span></span>                                                                                                                            |
| <span data-ttu-id="a3816-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3816-144">Is Indexed</span></span>             | <span data-ttu-id="a3816-145">否</span><span class="sxs-lookup"><span data-stu-id="a3816-145">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3816-146">In Global Catalog</span></span>      | <span data-ttu-id="a3816-147">否</span><span class="sxs-lookup"><span data-stu-id="a3816-147">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3816-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3816-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3816-149">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="a3816-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3816-150">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3816-151">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-152">Search-Flags</span></span>           | <span data-ttu-id="a3816-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3816-153">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-154">System-Flags</span></span>           | <span data-ttu-id="a3816-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3816-155">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3816-156">Classes used in</span></span>        | [<span data-ttu-id="a3816-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a3816-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a3816-158">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="a3816-158">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="a3816-159">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a3816-159">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a3816-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3816-160">Windows Server 2003</span></span>



| <span data-ttu-id="a3816-161">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-161">Entry</span></span> | <span data-ttu-id="a3816-162">值</span><span class="sxs-lookup"><span data-stu-id="a3816-162">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3816-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3816-163">Link-Id</span></span>                | <span data-ttu-id="a3816-164">94</span><span class="sxs-lookup"><span data-stu-id="a3816-164">94</span></span>                                                                                                                              |
| <span data-ttu-id="a3816-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-165">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="a3816-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3816-166">System-Only</span></span>            | <span data-ttu-id="a3816-167">否</span><span class="sxs-lookup"><span data-stu-id="a3816-167">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3816-168">Is-Single-Valued</span></span>       | <span data-ttu-id="a3816-169">對</span><span class="sxs-lookup"><span data-stu-id="a3816-169">True</span></span>                                                                                                                            |
| <span data-ttu-id="a3816-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3816-170">Is Indexed</span></span>             | <span data-ttu-id="a3816-171">否</span><span class="sxs-lookup"><span data-stu-id="a3816-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3816-172">In Global Catalog</span></span>      | <span data-ttu-id="a3816-173">否</span><span class="sxs-lookup"><span data-stu-id="a3816-173">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3816-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3816-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3816-175">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="a3816-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3816-176">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3816-177">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-178">Search-Flags</span></span>           | <span data-ttu-id="a3816-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3816-179">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-180">System-Flags</span></span>           | <span data-ttu-id="a3816-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3816-181">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3816-182">Classes used in</span></span>        | [<span data-ttu-id="a3816-183">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a3816-183">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a3816-184">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="a3816-184">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="a3816-185">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a3816-185">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a3816-186">亞當</span><span class="sxs-lookup"><span data-stu-id="a3816-186">ADAM</span></span>



| <span data-ttu-id="a3816-187">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-187">Entry</span></span> | <span data-ttu-id="a3816-188">值</span><span class="sxs-lookup"><span data-stu-id="a3816-188">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a3816-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3816-189">Link-Id</span></span>                | <span data-ttu-id="a3816-190">94</span><span class="sxs-lookup"><span data-stu-id="a3816-190">94</span></span>                                                                             |
| <span data-ttu-id="a3816-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-191">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="a3816-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3816-192">System-Only</span></span>            | <span data-ttu-id="a3816-193">否</span><span class="sxs-lookup"><span data-stu-id="a3816-193">False</span></span>                                                                          |
| <span data-ttu-id="a3816-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3816-194">Is-Single-Valued</span></span>       | <span data-ttu-id="a3816-195">對</span><span class="sxs-lookup"><span data-stu-id="a3816-195">True</span></span>                                                                           |
| <span data-ttu-id="a3816-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3816-196">Is Indexed</span></span>             | <span data-ttu-id="a3816-197">否</span><span class="sxs-lookup"><span data-stu-id="a3816-197">False</span></span>                                                                          |
| <span data-ttu-id="a3816-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3816-198">In Global Catalog</span></span>      | <span data-ttu-id="a3816-199">否</span><span class="sxs-lookup"><span data-stu-id="a3816-199">False</span></span>                                                                          |
| <span data-ttu-id="a3816-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3816-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3816-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3816-201">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="a3816-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3816-202">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="a3816-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3816-203">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="a3816-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-204">Search-Flags</span></span>           | <span data-ttu-id="a3816-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3816-205">0x00000000</span></span>                                                                     |
| <span data-ttu-id="a3816-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-206">System-Flags</span></span>           | <span data-ttu-id="a3816-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3816-207">0x00000010</span></span>                                                                     |
| <span data-ttu-id="a3816-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3816-208">Classes used in</span></span>        | [<span data-ttu-id="a3816-209">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a3816-209">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a3816-210">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a3816-210">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3816-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3816-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3816-212">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-212">Entry</span></span> | <span data-ttu-id="a3816-213">值</span><span class="sxs-lookup"><span data-stu-id="a3816-213">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3816-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3816-214">Link-Id</span></span>                | <span data-ttu-id="a3816-215">94</span><span class="sxs-lookup"><span data-stu-id="a3816-215">94</span></span>                                                                                                                              |
| <span data-ttu-id="a3816-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-216">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="a3816-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3816-217">System-Only</span></span>            | <span data-ttu-id="a3816-218">否</span><span class="sxs-lookup"><span data-stu-id="a3816-218">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3816-219">Is-Single-Valued</span></span>       | <span data-ttu-id="a3816-220">對</span><span class="sxs-lookup"><span data-stu-id="a3816-220">True</span></span>                                                                                                                            |
| <span data-ttu-id="a3816-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3816-221">Is Indexed</span></span>             | <span data-ttu-id="a3816-222">否</span><span class="sxs-lookup"><span data-stu-id="a3816-222">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3816-223">In Global Catalog</span></span>      | <span data-ttu-id="a3816-224">否</span><span class="sxs-lookup"><span data-stu-id="a3816-224">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3816-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3816-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3816-226">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="a3816-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3816-227">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3816-228">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-229">Search-Flags</span></span>           | <span data-ttu-id="a3816-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3816-230">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-231">System-Flags</span></span>           | <span data-ttu-id="a3816-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3816-232">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3816-233">Classes used in</span></span>        | [<span data-ttu-id="a3816-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a3816-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a3816-235">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="a3816-235">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="a3816-236">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a3816-236">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3816-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3816-237">Windows Server 2008</span></span>



| <span data-ttu-id="a3816-238">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-238">Entry</span></span> | <span data-ttu-id="a3816-239">值</span><span class="sxs-lookup"><span data-stu-id="a3816-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3816-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3816-240">Link-Id</span></span>                | <span data-ttu-id="a3816-241">94</span><span class="sxs-lookup"><span data-stu-id="a3816-241">94</span></span>                                                                                                                              |
| <span data-ttu-id="a3816-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-242">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="a3816-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3816-243">System-Only</span></span>            | <span data-ttu-id="a3816-244">否</span><span class="sxs-lookup"><span data-stu-id="a3816-244">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3816-245">Is-Single-Valued</span></span>       | <span data-ttu-id="a3816-246">對</span><span class="sxs-lookup"><span data-stu-id="a3816-246">True</span></span>                                                                                                                            |
| <span data-ttu-id="a3816-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3816-247">Is Indexed</span></span>             | <span data-ttu-id="a3816-248">否</span><span class="sxs-lookup"><span data-stu-id="a3816-248">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3816-249">In Global Catalog</span></span>      | <span data-ttu-id="a3816-250">否</span><span class="sxs-lookup"><span data-stu-id="a3816-250">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3816-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3816-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3816-252">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="a3816-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3816-253">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3816-254">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-255">Search-Flags</span></span>           | <span data-ttu-id="a3816-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3816-256">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-257">System-Flags</span></span>           | <span data-ttu-id="a3816-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3816-258">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3816-259">Classes used in</span></span>        | [<span data-ttu-id="a3816-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a3816-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a3816-261">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="a3816-261">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="a3816-262">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a3816-262">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3816-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3816-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3816-264">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-264">Entry</span></span> | <span data-ttu-id="a3816-265">值</span><span class="sxs-lookup"><span data-stu-id="a3816-265">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3816-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3816-266">Link-Id</span></span>                | <span data-ttu-id="a3816-267">94</span><span class="sxs-lookup"><span data-stu-id="a3816-267">94</span></span>                                                                                                                              |
| <span data-ttu-id="a3816-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-268">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="a3816-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3816-269">System-Only</span></span>            | <span data-ttu-id="a3816-270">否</span><span class="sxs-lookup"><span data-stu-id="a3816-270">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3816-271">Is-Single-Valued</span></span>       | <span data-ttu-id="a3816-272">對</span><span class="sxs-lookup"><span data-stu-id="a3816-272">True</span></span>                                                                                                                            |
| <span data-ttu-id="a3816-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3816-273">Is Indexed</span></span>             | <span data-ttu-id="a3816-274">否</span><span class="sxs-lookup"><span data-stu-id="a3816-274">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3816-275">In Global Catalog</span></span>      | <span data-ttu-id="a3816-276">否</span><span class="sxs-lookup"><span data-stu-id="a3816-276">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3816-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3816-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3816-278">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="a3816-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3816-279">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3816-280">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-281">Search-Flags</span></span>           | <span data-ttu-id="a3816-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3816-282">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-283">System-Flags</span></span>           | <span data-ttu-id="a3816-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3816-284">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3816-285">Classes used in</span></span>        | [<span data-ttu-id="a3816-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a3816-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a3816-287">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="a3816-287">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="a3816-288">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a3816-288">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3816-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3816-289">Windows Server 2012</span></span>



| <span data-ttu-id="a3816-290">進入</span><span class="sxs-lookup"><span data-stu-id="a3816-290">Entry</span></span> | <span data-ttu-id="a3816-291">值</span><span class="sxs-lookup"><span data-stu-id="a3816-291">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3816-292">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a3816-292">Link-Id</span></span>                | <span data-ttu-id="a3816-293">94</span><span class="sxs-lookup"><span data-stu-id="a3816-293">94</span></span>                                                                                                                              |
| <span data-ttu-id="a3816-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3816-294">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="a3816-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3816-295">System-Only</span></span>            | <span data-ttu-id="a3816-296">否</span><span class="sxs-lookup"><span data-stu-id="a3816-296">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-297">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a3816-297">Is-Single-Valued</span></span>       | <span data-ttu-id="a3816-298">對</span><span class="sxs-lookup"><span data-stu-id="a3816-298">True</span></span>                                                                                                                            |
| <span data-ttu-id="a3816-299">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a3816-299">Is Indexed</span></span>             | <span data-ttu-id="a3816-300">否</span><span class="sxs-lookup"><span data-stu-id="a3816-300">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-301">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a3816-301">In Global Catalog</span></span>      | <span data-ttu-id="a3816-302">否</span><span class="sxs-lookup"><span data-stu-id="a3816-302">False</span></span>                                                                                                                           |
| <span data-ttu-id="a3816-303">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a3816-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3816-304">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a3816-304">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="a3816-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3816-305">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3816-306">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="a3816-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-307">Search-Flags</span></span>           | <span data-ttu-id="a3816-308">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3816-308">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3816-309">System-Flags</span></span>           | <span data-ttu-id="a3816-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a3816-310">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="a3816-311">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a3816-311">Classes used in</span></span>        | [<span data-ttu-id="a3816-312">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="a3816-312">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="a3816-313">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="a3816-313">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="a3816-314">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="a3816-314">**Server**</span></span>](c-server.md)<br/> |



 

 





