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
# <a name="server-reference-attribute"></a><span data-ttu-id="9ff9f-106">Server-Reference 屬性</span><span class="sxs-lookup"><span data-stu-id="9ff9f-106">Server-Reference attribute</span></span>

<span data-ttu-id="9ff9f-107">在網站電腦物件中找到。</span><span class="sxs-lookup"><span data-stu-id="9ff9f-107">Found in a site computer object.</span></span> <span data-ttu-id="9ff9f-108">包含網域命名內容中網域控制站的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="9ff9f-108">Contains the distinguished name of the domain controller in the domain naming context.</span></span>



| <span data-ttu-id="9ff9f-109">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-109">Entry</span></span> | <span data-ttu-id="9ff9f-110">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9ff9f-111">CN</span><span class="sxs-lookup"><span data-stu-id="9ff9f-111">CN</span></span>                | <span data-ttu-id="9ff9f-112">Server-Reference</span><span class="sxs-lookup"><span data-stu-id="9ff9f-112">Server-Reference</span></span>                        |
| <span data-ttu-id="9ff9f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9ff9f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9ff9f-114">serverReference</span><span class="sxs-lookup"><span data-stu-id="9ff9f-114">serverReference</span></span>                         |
| <span data-ttu-id="9ff9f-115">大小</span><span class="sxs-lookup"><span data-stu-id="9ff9f-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="9ff9f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9ff9f-116">Update Privilege</span></span>  | <span data-ttu-id="9ff9f-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9ff9f-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="9ff9f-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9ff9f-118">Update Frequency</span></span>  | <span data-ttu-id="9ff9f-119">每次建立網站時。</span><span class="sxs-lookup"><span data-stu-id="9ff9f-119">Whenever a site is created.</span></span>             |
| <span data-ttu-id="9ff9f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-120">Attribute-Id</span></span>      | <span data-ttu-id="9ff9f-121">1.2.840.113556.1.4.515</span><span class="sxs-lookup"><span data-stu-id="9ff9f-121">1.2.840.113556.1.4.515</span></span>                  |
| <span data-ttu-id="9ff9f-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9ff9f-122">System-Id-Guid</span></span>    | <span data-ttu-id="9ff9f-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9ff9f-123">26d9736d-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="9ff9f-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ff9f-124">Syntax</span></span>            | [<span data-ttu-id="9ff9f-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="9ff9f-126">實作</span><span class="sxs-lookup"><span data-stu-id="9ff9f-126">Implementations</span></span>

-   [<span data-ttu-id="9ff9f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9ff9f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ff9f-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9ff9f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ff9f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ff9f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ff9f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9ff9f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ff9f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="9ff9f-135">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-135">Entry</span></span> | <span data-ttu-id="9ff9f-136">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff9f-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ff9f-137">Link-Id</span></span>                | <span data-ttu-id="9ff9f-138">94</span><span class="sxs-lookup"><span data-stu-id="9ff9f-138">94</span></span>                                                                                                                              |
| <span data-ttu-id="9ff9f-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-139">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ff9f-140">System-Only</span></span>            | <span data-ttu-id="9ff9f-141">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-141">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="9ff9f-143">對</span><span class="sxs-lookup"><span data-stu-id="9ff9f-143">True</span></span>                                                                                                                            |
| <span data-ttu-id="9ff9f-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ff9f-144">Is Indexed</span></span>             | <span data-ttu-id="9ff9f-145">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-145">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ff9f-146">In Global Catalog</span></span>      | <span data-ttu-id="9ff9f-147">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-147">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ff9f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ff9f-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ff9f-149">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="9ff9f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ff9f-150">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ff9f-151">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-152">Search-Flags</span></span>           | <span data-ttu-id="9ff9f-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ff9f-153">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-154">System-Flags</span></span>           | <span data-ttu-id="9ff9f-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ff9f-155">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ff9f-156">Classes used in</span></span>        | [<span data-ttu-id="9ff9f-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="9ff9f-158">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-158">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="9ff9f-159">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-159">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9ff9f-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ff9f-160">Windows Server 2003</span></span>



| <span data-ttu-id="9ff9f-161">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-161">Entry</span></span> | <span data-ttu-id="9ff9f-162">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-162">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff9f-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ff9f-163">Link-Id</span></span>                | <span data-ttu-id="9ff9f-164">94</span><span class="sxs-lookup"><span data-stu-id="9ff9f-164">94</span></span>                                                                                                                              |
| <span data-ttu-id="9ff9f-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-165">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ff9f-166">System-Only</span></span>            | <span data-ttu-id="9ff9f-167">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-167">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-168">Is-Single-Valued</span></span>       | <span data-ttu-id="9ff9f-169">對</span><span class="sxs-lookup"><span data-stu-id="9ff9f-169">True</span></span>                                                                                                                            |
| <span data-ttu-id="9ff9f-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ff9f-170">Is Indexed</span></span>             | <span data-ttu-id="9ff9f-171">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ff9f-172">In Global Catalog</span></span>      | <span data-ttu-id="9ff9f-173">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-173">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ff9f-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ff9f-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ff9f-175">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="9ff9f-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ff9f-176">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ff9f-177">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-178">Search-Flags</span></span>           | <span data-ttu-id="9ff9f-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ff9f-179">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-180">System-Flags</span></span>           | <span data-ttu-id="9ff9f-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ff9f-181">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ff9f-182">Classes used in</span></span>        | [<span data-ttu-id="9ff9f-183">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-183">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="9ff9f-184">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-184">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="9ff9f-185">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-185">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9ff9f-186">亞當</span><span class="sxs-lookup"><span data-stu-id="9ff9f-186">ADAM</span></span>



| <span data-ttu-id="9ff9f-187">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-187">Entry</span></span> | <span data-ttu-id="9ff9f-188">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-188">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="9ff9f-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ff9f-189">Link-Id</span></span>                | <span data-ttu-id="9ff9f-190">94</span><span class="sxs-lookup"><span data-stu-id="9ff9f-190">94</span></span>                                                                             |
| <span data-ttu-id="9ff9f-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-191">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="9ff9f-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ff9f-192">System-Only</span></span>            | <span data-ttu-id="9ff9f-193">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-193">False</span></span>                                                                          |
| <span data-ttu-id="9ff9f-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-194">Is-Single-Valued</span></span>       | <span data-ttu-id="9ff9f-195">對</span><span class="sxs-lookup"><span data-stu-id="9ff9f-195">True</span></span>                                                                           |
| <span data-ttu-id="9ff9f-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ff9f-196">Is Indexed</span></span>             | <span data-ttu-id="9ff9f-197">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-197">False</span></span>                                                                          |
| <span data-ttu-id="9ff9f-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ff9f-198">In Global Catalog</span></span>      | <span data-ttu-id="9ff9f-199">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-199">False</span></span>                                                                          |
| <span data-ttu-id="9ff9f-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ff9f-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ff9f-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ff9f-201">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="9ff9f-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ff9f-202">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="9ff9f-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ff9f-203">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="9ff9f-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-204">Search-Flags</span></span>           | <span data-ttu-id="9ff9f-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ff9f-205">0x00000000</span></span>                                                                     |
| <span data-ttu-id="9ff9f-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-206">System-Flags</span></span>           | <span data-ttu-id="9ff9f-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ff9f-207">0x00000010</span></span>                                                                     |
| <span data-ttu-id="9ff9f-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ff9f-208">Classes used in</span></span>        | [<span data-ttu-id="9ff9f-209">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-209">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="9ff9f-210">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-210">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ff9f-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ff9f-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ff9f-212">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-212">Entry</span></span> | <span data-ttu-id="9ff9f-213">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-213">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff9f-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ff9f-214">Link-Id</span></span>                | <span data-ttu-id="9ff9f-215">94</span><span class="sxs-lookup"><span data-stu-id="9ff9f-215">94</span></span>                                                                                                                              |
| <span data-ttu-id="9ff9f-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-216">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ff9f-217">System-Only</span></span>            | <span data-ttu-id="9ff9f-218">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-218">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-219">Is-Single-Valued</span></span>       | <span data-ttu-id="9ff9f-220">對</span><span class="sxs-lookup"><span data-stu-id="9ff9f-220">True</span></span>                                                                                                                            |
| <span data-ttu-id="9ff9f-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ff9f-221">Is Indexed</span></span>             | <span data-ttu-id="9ff9f-222">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-222">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ff9f-223">In Global Catalog</span></span>      | <span data-ttu-id="9ff9f-224">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-224">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ff9f-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ff9f-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ff9f-226">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="9ff9f-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ff9f-227">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ff9f-228">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-229">Search-Flags</span></span>           | <span data-ttu-id="9ff9f-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ff9f-230">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-231">System-Flags</span></span>           | <span data-ttu-id="9ff9f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ff9f-232">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ff9f-233">Classes used in</span></span>        | [<span data-ttu-id="9ff9f-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="9ff9f-235">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-235">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="9ff9f-236">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-236">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ff9f-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ff9f-237">Windows Server 2008</span></span>



| <span data-ttu-id="9ff9f-238">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-238">Entry</span></span> | <span data-ttu-id="9ff9f-239">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-239">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff9f-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ff9f-240">Link-Id</span></span>                | <span data-ttu-id="9ff9f-241">94</span><span class="sxs-lookup"><span data-stu-id="9ff9f-241">94</span></span>                                                                                                                              |
| <span data-ttu-id="9ff9f-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-242">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ff9f-243">System-Only</span></span>            | <span data-ttu-id="9ff9f-244">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-244">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-245">Is-Single-Valued</span></span>       | <span data-ttu-id="9ff9f-246">對</span><span class="sxs-lookup"><span data-stu-id="9ff9f-246">True</span></span>                                                                                                                            |
| <span data-ttu-id="9ff9f-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ff9f-247">Is Indexed</span></span>             | <span data-ttu-id="9ff9f-248">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-248">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ff9f-249">In Global Catalog</span></span>      | <span data-ttu-id="9ff9f-250">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-250">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ff9f-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ff9f-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ff9f-252">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="9ff9f-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ff9f-253">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ff9f-254">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-255">Search-Flags</span></span>           | <span data-ttu-id="9ff9f-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ff9f-256">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-257">System-Flags</span></span>           | <span data-ttu-id="9ff9f-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ff9f-258">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ff9f-259">Classes used in</span></span>        | [<span data-ttu-id="9ff9f-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="9ff9f-261">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-261">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="9ff9f-262">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-262">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ff9f-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ff9f-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ff9f-264">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-264">Entry</span></span> | <span data-ttu-id="9ff9f-265">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-265">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff9f-266">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ff9f-266">Link-Id</span></span>                | <span data-ttu-id="9ff9f-267">94</span><span class="sxs-lookup"><span data-stu-id="9ff9f-267">94</span></span>                                                                                                                              |
| <span data-ttu-id="9ff9f-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-268">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ff9f-269">System-Only</span></span>            | <span data-ttu-id="9ff9f-270">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-270">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-271">Is-Single-Valued</span></span>       | <span data-ttu-id="9ff9f-272">對</span><span class="sxs-lookup"><span data-stu-id="9ff9f-272">True</span></span>                                                                                                                            |
| <span data-ttu-id="9ff9f-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ff9f-273">Is Indexed</span></span>             | <span data-ttu-id="9ff9f-274">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-274">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ff9f-275">In Global Catalog</span></span>      | <span data-ttu-id="9ff9f-276">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-276">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ff9f-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ff9f-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ff9f-278">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="9ff9f-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ff9f-279">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ff9f-280">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-281">Search-Flags</span></span>           | <span data-ttu-id="9ff9f-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ff9f-282">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-283">System-Flags</span></span>           | <span data-ttu-id="9ff9f-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ff9f-284">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ff9f-285">Classes used in</span></span>        | [<span data-ttu-id="9ff9f-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="9ff9f-287">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-287">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="9ff9f-288">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-288">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ff9f-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ff9f-289">Windows Server 2012</span></span>



| <span data-ttu-id="9ff9f-290">進入</span><span class="sxs-lookup"><span data-stu-id="9ff9f-290">Entry</span></span> | <span data-ttu-id="9ff9f-291">值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-291">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff9f-292">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9ff9f-292">Link-Id</span></span>                | <span data-ttu-id="9ff9f-293">94</span><span class="sxs-lookup"><span data-stu-id="9ff9f-293">94</span></span>                                                                                                                              |
| <span data-ttu-id="9ff9f-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ff9f-294">MAPI-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ff9f-295">System-Only</span></span>            | <span data-ttu-id="9ff9f-296">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-296">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-297">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9ff9f-297">Is-Single-Valued</span></span>       | <span data-ttu-id="9ff9f-298">對</span><span class="sxs-lookup"><span data-stu-id="9ff9f-298">True</span></span>                                                                                                                            |
| <span data-ttu-id="9ff9f-299">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9ff9f-299">Is Indexed</span></span>             | <span data-ttu-id="9ff9f-300">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-300">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-301">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9ff9f-301">In Global Catalog</span></span>      | <span data-ttu-id="9ff9f-302">否</span><span class="sxs-lookup"><span data-stu-id="9ff9f-302">False</span></span>                                                                                                                           |
| <span data-ttu-id="9ff9f-303">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9ff9f-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ff9f-304">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9ff9f-304">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="9ff9f-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ff9f-305">Range-Lower</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ff9f-306">Range-Upper</span></span>            | \-                                                                                                                              |
| <span data-ttu-id="9ff9f-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-307">Search-Flags</span></span>           | <span data-ttu-id="9ff9f-308">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ff9f-308">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ff9f-309">System-Flags</span></span>           | <span data-ttu-id="9ff9f-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ff9f-310">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="9ff9f-311">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9ff9f-311">Classes used in</span></span>        | [<span data-ttu-id="9ff9f-312">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-312">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="9ff9f-313">**NTFRS-成員**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-313">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="9ff9f-314">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="9ff9f-314">**Server**</span></span>](c-server.md)<br/> |



 

 





